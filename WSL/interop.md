---
title: Взаимодействие Windows с Linux
description: Описывает взаимодействие Windows с дистрибутивами Linux, работающими в подсистеме Windows для Linux.
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 3f3df3337ece75d7af77313f5fc55eb4e18e31cb
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122735"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a>Подсистема Windows для взаимодействия Linux с Windows

> **Обновлены обновления для создателей попадают.**  
Если вы используете авторские обновления или годовщины, перейдите к разделу [Создатели/годовщина обновления](interop.md#creators-update-and-anniversary-update).

Подсистема Windows для Linux (WSL) постоянно улучшает интеграцию между Windows и Linux.  Можно выполнить следующие действия:

1. Вызов двоичных файлов Windows из консоли Linux.
1. Вызов двоичных файлов Linux из консоли Windows.
1. **Программа предварительной оценки Windows создает 17063 +** Совместное использование переменных среды между Linux и Windows.

Это обеспечивает эффективное взаимодействие между Windows и WSL.  Технические сведения содержатся в [блоге WSL](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).

## <a name="run-linux-tools-from-a-windows-command-line"></a>Запуск средств Linux из командной строки Windows

Запускайте двоичные файлы Linux из командной строки Windows (CMD или PowerShell `wsl.exe <command>`) с помощью команды.

Двоичные файлы, которые вызываются таким образом:

1. Используйте тот же рабочий каталог, что и для текущего ИНТЕРПРЕТАТОРа команд или командной строки PowerShell.
1. Выполните команду от имени пользователя WSL по умолчанию.
1. Имеют те же права администратора Windows, что и вызывающий процесс и терминал.

Пример:

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

Следующая `wsl.exe` команда Linux обрабатывается как любая команда, выполняемая в WSL.  Действия sudo, трубопроводов и перенаправления файлов.

Пример использования sudo:

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

Примеры смешивания команд WSL и Windows:

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

Команды, передаваемые `wsl.exe` в, перенаправляются в процесс WSL без изменения.  Пути к файлам должны быть указаны в формате WSL.

Пример с путями:

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a>Запуск инструментов Windows из WSL

WSL может вызывать двоичные файлы Windows непосредственно из командной строки WSL `[binary name].exe`с помощью.  Например, `notepad.exe`.  Чтобы упростить запуск исполняемых файлов Windows, путь Windows включается в обновление для создателей Linux `$PATH` .

Приложения выполняются таким образом и имеют следующие свойства:

1. Храните рабочий каталог в качестве командной строки WSL (наиболее частые исключения описаны ниже).
1. Имеют те же права разрешений, что и процесс WSL.
1. Запуск от имени активного пользователя Windows.
1. Отображаются в диспетчере задач Windows так, как если бы они выполнялись непосредственно из командной строки.

Пример.

``` BASH
$ notepad.exe
```

Исполняемые файлы Windows, выполняемые в WSL, обрабатываются аналогично собственным исполняемым файлам Linux — конвейеру, перенаправлениям и даже фоновому режиму работы должным образом.

Примеры использования каналов:

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

Пример использования смешанных команд Windows и WSL:

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

Двоичные файлы Windows должны включать расширение файла, сопоставлять регистр файлов и быть исполняемыми.  Не исполняемые файлы, включая скрипты пакетной службы.  Машинные команды cmd `dir` , например, можно `cmd.exe /C` выполнять с помощью команды.

Примеры:

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

Параметры передаются в двоичный файл Windows без изменений.

Например, следующие команды будут открыты `C:\temp\foo.txt` в: `notepad.exe`

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

Изменение файлов, расположенных в волфс (файлы, `/mnt/<x>`не включенные в файл) с помощью приложения Windows в WSL, не поддерживается.

По умолчанию WSL пытается удержать рабочий каталог двоичного файла Windows в качестве текущего каталога WSL, но если рабочий каталог находится в Волфс, он вернется к каталогу создания экземпляра.

Пример; изначально запускается из `C:\temp` , а текущий каталог WSL изменяется на домашнюю страницу пользователя. `wsl.exe`  Когда `notepad.exe` вызывается из домашнего каталога пользователя, WSL автоматически возвращается в `C:\temp` качестве рабочего каталога Notepad. exe:

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

> Доступно в сборке Windows Insider 17063 и более поздних версий.

До 17063 только переменная среды Windows, к которой имеет доступ WSL, `PATH` была доступна (так что можно было запускать исполняемые файлы Win32 из раздела WSL).

Начиная с 17063, WSL и общей папки `WSLENV`Windows, можно создать специальную переменную среды, созданную для моста Windows и Linux дистрибутивов, запущенные на WSL.

`WSLENV`Свойства:

* Он является общим; он существует в средах Windows и WSL.
* Это список переменных среды, которые совместно используют Windows и WSL.
* Он может форматировать переменные среды для корректной работы в Windows и WSL.

В `WSLENV` предусмотрено четыре флага, влияющих на способ перевода переменной среды.

`WSLENV`Метки

* `/p`— переводит путь между путями в стиле WSL/Linux и путями Win32.
* `/l`— Указывает, что переменная среды представляет собой список путей.
* `/u`— Указывает, что эта переменная среды должна быть включена только при запуске WSL из Win32.
* `/w`— Указывает, что эту переменную среды следует включать только при запуске Win32 из WSL.

При необходимости флаги можно комбинировать.

## <a name="disable-interop"></a>Отключить взаимодействие

Пользователи могут отключить возможность запуска двоичных файлов Windows для одного сеанса WSL, выполнив следующую команду в качестве корневого:

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Чтобы повторно включить двоичные файлы Windows, закройте все сеансы WSL и перезапустите bash. exe или выполните следующую команду в качестве корневого:

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Отключение взаимодействия не будет сохраняться между сеансами WSL--взаимодействие будет включено повторно при запуске нового сеанса.

## <a name="creators-update-and-anniversary-update"></a>Авторские обновления и годовщины

Несмотря на то, что обновление с предварительной приначальным взаимодействием в области взаимодействия аналогично более недавнему взаимодействию, существует несколько основных отличий.

Итоги:

* `bash.exe`является нерекомендуемым и заменяется на `wsl.exe`.
* `-c`параметр для выполнения одной команды не требуется с `wsl.exe`.
* Путь Windows включен в WSL`$PATH`

Процесс отключения взаимодействия не изменяется.

### <a name="invoking-wsl-from-the-windows-command-line"></a>Вызов WSL из командной строки Windows

Двоичные файлы Linux можно вызывать из командной строки Windows или из PowerShell.  Двоичные файлы, вызываемые таким способом, имеют следующие свойства:

1. Используйте тот же рабочий каталог, что и в командной строке CMD или PowerShell.
1. Выполните команду от имени пользователя WSL по умолчанию.
1. Имеют те же права администратора Windows, что и вызывающий процесс и терминал.

Пример.

```console
C:\temp> bash -c "ls -la"
```

Команды Linux, вызываемые таким образом, обрабатываются как любые другие приложения Windows.  Такие вещи, как входные данные, конвейеры и перенаправление файлов, работают должным образом.

Примеры:

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

Команды WSL, передаваемые `bash -c` в, пересылаются в процесс WSL без изменения.  Пути к файлам должны быть указаны в формате WSL, и необходимо соблюдать осторожность для экранирования соответствующих символов. Пример.

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a>Вызов двоичных файлов Windows из WSL

Подсистема Windows для Linux может вызывать двоичные файлы Windows непосредственно из командной строки WSL.  Приложения выполняются таким образом и имеют следующие свойства:

1. Храните рабочий каталог в командной строке WSL, за исключением сценария, описанного ниже.
1. Имеют те же права разрешений, что `bash.exe` и процесс. 
1. Запуск от имени активного пользователя Windows.
1. Отображаются в диспетчере задач Windows так, как если бы они выполнялись непосредственно из командной строки.

Пример.

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

В WSL эти исполняемые файлы обрабатываются аналогично собственным исполняемым файлам Linux.  Это означает, что добавление каталогов в путь Linux и передача между командами выполняется должным образом.  Примеры:

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

Двоичный файл Windows должен включать расширение файла, соответствовать регистру файла и быть исполняемым.  Кроме исполняемых файлов, включая скрипты пакетной `dir` службы и команду, `/mnt/c/Windows/System32/cmd.exe /C` можно выполнить команду с помощью команды.

Примеры:

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

Параметры передаются в двоичный файл Windows без изменений.  

Например, следующие команды будут открыты `C:\temp\foo.txt` в: `notepad.exe`

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

Изменение файлов, расположенных в волфс (файлы, `/mnt/<x>`отсутствующие в папке), с приложением Windows не поддерживается.  По умолчанию WSL пытается использовать рабочий каталог двоичного файла Windows в качестве текущего каталога WSL, но если рабочий каталог находится в Волфс, то он вернется к каталогу создания экземпляра.

Пример; изначально запускается из `C:\temp` , а текущий каталог WSL изменяется на домашнюю страницу пользователя. `bash.exe`  Когда `notepad.exe` вызывается из домашнего каталога пользователя, WSL автоматически возвращается в `C:\temp` качестве рабочего каталога Notepad. exe:

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
