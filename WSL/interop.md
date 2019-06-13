---
title: Взаимодействие Windows с Linux
description: Описывает взаимодействие Windows с дистрибутивов Linux, запущенных в подсистеме Windows для Linux.
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.openlocfilehash: e4608c25c6bcc63413d53b2c808c16fe2a62dd5c
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040815"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a>Подсистема Windows для Linux взаимодействие с Windows

> **Обновлено для Fall Creators Update.**  
Если вы используете Creators Update или Юбилейное обновление, перейдите к [Creators/Юбилейное обновление раздела](interop.md#creators-update-and-anniversary-update).

Подсистема Windows для Linux (WSL) мы постоянно улучшаем методы интеграции между Windows и Linux.  Можно выполнить следующие действия:

1. Вызовите двоичные файлы Windows из консоли Linux.
1. Вызовите двоичные файлы Linux с помощью консоли Windows.
1. **Сборки для предварительной оценки Windows 17063 +** совместного использования переменных среды между Linux и Windows.

Это обеспечивает удобную работу между Windows и WSL.  Технические сведения приведены в [WSL блог](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).

## <a name="run-linux-tools-from-a-windows-command-line"></a>Запуск средств Linux из командной строки Windows

Запускать исполняемые файлы Linux из командной строки Windows (CMD или PowerShell), используя `wsl.exe <command>`.

Двоичные файлы, вызывается таким образом:

1. Используйте тот же рабочий каталог, как в текущей строке CMD или PowerShell.
1. Запуск от имени пользователя по умолчанию WSL.
1. Иметь те же права администратора Windows как вызывающий процесс и терминал.

Пример:

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

Следующие команды Linux `wsl.exe` обрабатывается как любой команде, выполняемых в WSL.  Sudo, конвейерная передача и перенаправление файловой работать.

Пример, используя "sudo".

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

Примеры смешивание команды WSL и Windows.

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

Переданные команды `wsl.exe` перенаправляются к процессу WSL без изменений.  Пути к файлам должен быть указан в формате WSL.

Пример с путями.

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a>Запуск средств Windows из WSL

WSL можно вызвать двоичные файлы Windows непосредственно с помощью командной строки WSL `[binary name].exe`.  Например, `notepad.exe`.  Чтобы упростить исполняемых файлов Windows для запуска, путь Windows содержится в Linux `$PATH` в Fall Creators Update.

Приложения, этот способ выполнения имеют следующие свойства:

1. Сохранить рабочий каталог как WSL командной строки (в большинстве случаев — исключения как описано ниже).
1. Имеют одинаковые права разрешение как WSL процесс.
1. Запуск от имени активного пользователя Windows.
1. Отображаются в диспетчере задач Windows так, как если бы выполняться непосредственно из Командной строки.

Пример.

``` BASH
$ notepad.exe
```

Исполняемые файлы Windows, выполните в WSL обрабатываются аналогичным образом в собственном Linux исполняемые файлы--направление, перенаправление и даже фоновый режим работы должным образом.

Примеры использования каналов:

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

Пример использования смешанных команд Windows и WSL.

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

Двоичные файлы Windows должен включать расширение файла совпадает по регистру файла и быть исполняемым.  Non-исполняемые файлы включая сценарии пакетной обработки.  CMD собственные команды, такие как `dir` можно запускать с `cmd.exe /C` команды.

Примеры

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

Параметры передаются в Windows двоичный без изменений.

Например, следующие команды откроется `C:\temp\foo.txt` в `notepad.exe`:

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

Изменение файлов, расположенных на VolFs (не при использовании файлов `/mnt/<x>`) с Windows приложение в WSL не поддерживается.

По умолчанию WSL пытается сохранить рабочий каталог Windows двоичные значения как текущего каталога WSL, но если рабочий каталог находится на VolFs вернется на каталог создания экземпляра.

В качестве примера; `wsl.exe` первоначально запускается из `C:\temp` и текущий каталог WSL изменяется на домашнюю страницу пользователя.  Когда `notepad.exe` вызывается из корневого каталога документов пользователя, WSL автоматический возврат к `C:\temp` качестве рабочего каталога notepad.exe:

``` BASH
C:\temp> wsl
/mnt/c/temp/$ cd ~
~$ notepad.exe foo.txt
~$ ls | grep foo.txt
~$ exit

exit
C:\temp>dir | findstr foo.txt
09/27/2016  02:15 PM                14 foo.txt
```

## <a name="share-environment-variables-between-windows-and-wsl"></a>Совместное использование переменных среды между Windows и WSL

> Доступно в сборках Windows Insider 17063 и более поздние версии.

До появления 17063, было только Windows переменная среды, которая может получить доступ к WSL `PATH` (поэтому мог запускать исполняемые файлы Win32 из WSL).

Начиная с 17063, WSL и Windows используют `WSLENV`, специальные среды переменная, созданная на дистрибутивы Windows и Linux, на WSL.

Свойства `WSLENV`:

* Он является общим; он существует в средах Windows и WSL.
* Это список переменных среды для совместного использования между Windows и WSL.
* Его можно отформатировать переменные среды, работают в Windows и WSL.

Существует четыре флаги в `WSLENV` на преобразование этой переменной среды.

`WSLENV` флаги:

* `/p` — Преобразует путь между WSL/Linux стиля пути и пути Win32.
* `/l` — Указывает список путей переменной среды.
* `/u` — Указывает, что эта переменная среды должны быть включены только при запуске WSL из Win32.
* `/w` — Указывает, что эта переменная среды должны быть включены только при запуске из WSL Win32.

Флаги могут быть объединены, при необходимости.

## <a name="disable-interop"></a>Отключить взаимодействия

Пользователи могут отключить возможность запускать исполняемые файлы Windows на WSL время одного сеанса, выполнив следующую команду в качестве привилегированного пользователя:

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Чтобы включить Windows двоичные файлы либо выйти из всех сеансов WSL и повторно запустите bash.exe либо выполните следующую команду в качестве привилегированного пользователя:

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Отключение взаимодействия не сохраняются между сеансами WSL--взаимодействия включаются снова при запуске нового сеанса.

## <a name="creators-update-and-anniversary-update"></a>Creators Update и Центр обновления Годовщина

Во время предварительной осенью взаимодействия качества Creators Update похожа на более новый опыт взаимодействия, доступно несколько существенных различий.

Подведем итоги.

* `bash.exe` устарели и заменены `wsl.exe`.
* `-c` параметр для выполнения одной команды с не нужен `wsl.exe`.
* Путь Windows содержится в WSL `$PATH`

Процесс отключения взаимодействия не изменяется.

### <a name="invoking-wsl-from-the-windows-command-line"></a>Вызов WSL из командной строки Windows

Двоичные файлы Linux могут вызываться из командной строки Windows или с помощью PowerShell.  Двоичные файлы, вызывается таким образом, имеют следующие свойства:

1. Используйте тот же рабочий каталог в командной строке команду CMD и PowerShell.
1. Запуск от имени пользователя по умолчанию WSL.
1. Иметь те же права администратора Windows как вызывающий процесс и терминал.

Пример.

```console
C:\temp> bash -c "ls -la"
```

Команды Linux, называемые таким образом, обрабатываются как и любое другое приложение Windows.  Входные данные, конвейерная передача и перенаправление файловой работать должным образом.

Примеры

```console
C:\temp>bash -c "sudo apt-get update"
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

```console
C:\temp> bash -c "ls -la" | findstr foo
C:\temp> dir | bash -c "grep foo"
C:\temp> bash -c "ls -la" > out.txt
```

Переданные команды WSL `bash -c` перенаправляются к процессу WSL без изменений.  Пути к файлам должен быть указан в формате WSL и будьте осторожны в escape-символы, соответствующие. Пример.

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a>Вызов WSL двоичных файлов Windows

Подсистема Windows для Linux можно вызвать двоичные файлы Windows непосредственно из командной строки WSL.  Приложения, этот способ выполнения имеют следующие свойства:

1. Оставлять рабочий каталог WSL командной строки за исключением сценарий, описанный ниже.
1. Имеют те же права разрешение, что `bash.exe` процесса. 
1. Запуск от имени активного пользователя Windows.
1. Отображаются в диспетчере задач Windows так, как если бы выполняться непосредственно из Командной строки.

Пример.

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

В WSL эти исполняемые файлы обрабатываются аналогично собственного исполняемых файлов Linux.  Это означает, что добавление каталогов в пути Linux и передачи между команды работает должным образом.  Примеры

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

Двоичный файл Windows должен включать расширение файла совпадает по регистру файла и быть исполняемым.  Non-исполняемых файлов включая сценарии пакетной обработки и команды, такие как `dir` можно запускать с `/mnt/c/Windows/System32/cmd.exe /C` команды.

Примеры

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

Параметры передаются в Windows двоичный без изменений.  

Например, следующие команды откроется `C:\temp\foo.txt` в `notepad.exe`:

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

Изменение файлов, расположенных на VolFs (не при использовании файлов `/mnt/<x>`) с Windows приложение не поддерживается.  По умолчанию WSL пытается сохранить рабочий каталог Windows двоичные значения как текущего каталога WSL, но если рабочий каталог находится на VolFs вернется на каталог создания экземпляра.

В качестве примера; `bash.exe` первоначально запускается из `C:\temp` и текущий каталог WSL изменяется на домашнюю страницу пользователя.  Когда `notepad.exe` вызывается из корневого каталога документов пользователя, WSL автоматический возврат к `C:\temp` качестве рабочего каталога notepad.exe:

``` BASH
C:\temp> bash
/mnt/c/temp/$ cd ~
~$ notepad.exe foo.txt
~$ ls | grep foo.txt
~$ exit
exit

C:\temp> dir | findstr foo.txt
09/27/2016  02:15 PM                14 foo.txt
```
