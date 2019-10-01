---
title: Взаимодействие Windows с Linux
description: Описывается взаимодействие Windows с дистрибутивами Linux, работающими в подсистеме Windows для Linux.
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: f8b0150c044f5011b84e80cac4befd752c4dc552
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269796"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a>Подсистема Windows для взаимодействия Linux с Windows

> **Статья обновлена с учетом Fall Creators Update.**  
Если вы используете Creators Update или юбилейное обновление, перейдите к разделу [Обновление Creators Update и юбилейное обновление](interop.md#creators-update-and-anniversary-update).

В подсистеме Windows для Linux (WSL) постоянно улучшается интеграция между Windows и Linux.  Можно сделать следующее.

1. Вызов двоичных файлов Windows из консоли Linux.
1. Вызов двоичных файлов Linux из консоли Windows.
1. **Сборки для программы предварительной оценки Windows (17063 и выше)** : совместное использование переменных среды между Linux и Windows.

Это обеспечивает эффективное взаимодействие между Windows и WSL.  Технические сведения доступны в [блоге по WSL](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).

## <a name="run-linux-tools-from-a-windows-command-line"></a>Запуск инструментов Linux из командной строки Windows

Запускайте двоичные файлы Linux из командной строки Windows (CMD или PowerShell), используя `wsl.exe <command>`.

Двоичные файлы вызываются следующим образом.

1. Используется тот же рабочий каталог, что и для текущей командной строки или сеанса PowerShell.
1. Файл выполняется от имени пользователя WSL по умолчанию.
1. Требуются те же права администратора Windows, что и у вызывающего процесса и терминала.

Например:

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

Команда Linux после `wsl.exe` обрабатывается как любая команда, выполняемая в WSL.  Можно выполнять sudo, конвейерную передачу и перенаправление файлов.

Пример использования sudo.

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

Примеры совместного выполнения команд WSL и Windows.

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

Команды, передаваемые в `wsl.exe`, перенаправляются в процесс WSL без изменения.  Пути к файлам должны быть указаны в формате WSL.

Пример с путями.

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a>Запуск инструментов Windows из WSL

WSL может вызывать двоичные файлы Windows непосредственно из командной строки WSL с помощью `[binary name].exe`.  Например, `notepad.exe`.  Чтобы упростить запуск исполняемых файлов Windows, в обновлении Fall Creators Update путь Windows добавлен в переменную `$PATH` Linux.

Приложения, выполняемые таким образом, обладают следующими свойствами.

1. Рабочим каталогом остается каталог командной строки WSL (в большинстве случаев; исключения описаны ниже).
1. Они имеют те же разрешения, что и процесс WSL.
1. Они выполняются от имени активного пользователя Windows.
1. Они отображаются в диспетчере задач Windows так, как если бы они выполнялись непосредственно из командной строки.

Пример.

``` BASH
$ notepad.exe
```

Исполняемые файлы Windows, выполняемые в WSL, обрабатываются аналогично собственным исполняемым файлам Linux — конвейерной передаче, перенаправлению и даже фоновому режиму работы.

Примеры использования каналов.

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

Пример использования сочетания команд Windows и WSL.

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

Двоичные файлы Windows должны иметь расширение файла, его регистр символов должен совпадать с регистром в имени файла и эти файлы должны быть исполняемыми.  Неисполняемые файлы, в том числе сценарии пакетного выполнения и  собственные команды командной строки, такие как `dir`, можно выполнять с помощью команды `cmd.exe /C`.

Примеры

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

Параметры передаются в двоичный файл Windows без изменений.

Например, следующие команды откроют `C:\temp\foo.txt` в `notepad.exe`.

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

Изменение файлов, находящихся в VolFs (файлы не в `/mnt/<x>`), приложением для Windows в WSL не поддерживается.

По умолчанию WSL пытается оставить рабочий каталог двоичного файла Windows в качестве текущего каталога WSL, но если рабочий каталог находится в VolFs, то WSL вернется к каталогу создания экземпляра.

Например, `wsl.exe` изначально запускается из `C:\temp`, а текущим каталогом WSL становится корневая папка пользователя.  При вызове `notepad.exe` из корневого каталога пользователя WSL автоматически возвращается к `C:\temp` в качестве рабочего каталога Notepad.exe.

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

> Доступно в выпусках для программы предварительной оценки Windows, начиная со сборки 17063.

До выпуска сборки 17063 единственной переменной среды Windows,, к которой могла получить доступ WSL, была `PATH` (это позволяло запускать исполняемые файлы Win32 из WSL).

Начиная со сборки 17063 решение WSL и Windows совместно используют `WSLENV` — специальную переменную среды, созданную для взаимодействия Windows и дистрибутивов Linux, запущенных в WSL.

Свойства `WSLENV`:

* она используется совместно и существует в средах Windows и WSL;
* это список переменных среды, которые совместно используют Windows и WSL;
* она позволяет форматировать список переменных среды для корректного использования в Windows и WSL.

В `WSLENV` доступны четыре флага, влияющие на способ преобразования переменной среды.

Флаги `WSLENV`:

* `/p` преобразовывает пути WSL и Linux в пути Win32 и наоборот;
* `/l` указывает, что переменная среды представляет собой список путей;
* `/u` указывает, что эту переменную среды следует добавлять только при запуске WSL из Win32;
* `/w` указывает, что эту переменную среды следует добавлять только при запуске Win32 из WSL.

При необходимости флаги можно комбинировать.

## <a name="disable-interop"></a>Отключение взаимодействия

Пользователи могут отключить возможность запуска двоичных файлов Windows для отдельного сеанса WSL, выполнив следующую команду в качестве привилегированного пользователя.

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Чтобы повторно включить возможность запуска двоичных файлов Windows, закройте все сеансы WSL и повторно запустите bash.exe или выполните следующую команду от имени привилегированного пользователя.

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Отключение взаимодействия не будет сохраняться между сеансами WSL, оно снова будет включено при запуске нового сеанса.

## <a name="creators-update-and-anniversary-update"></a>Обновление Creators Update и юбилейное обновление

Несмотря на то, что возможности взаимодействия до выпуска обновления Fall Creators Update схожи с возможностями последней версии взаимодействия, существует несколько основных отличий.

Вот о чем речь:

* `bash.exe` является нерекомендуемым и заменен на `wsl.exe`;
* параметр `-c` не требуется для выполнения одной команды `wsl.exe`;
* путь Windows включен в переменную `$PATH` WSL.

Процесс отключения взаимодействия не изменяется.

### <a name="invoking-wsl-from-the-windows-command-line"></a>Вызов WSL из командной строки Windows

Двоичные файлы Linux можно вызывать из командной строки Windows или PowerShell.  Двоичные файлы, вызываемые таким способом, обладают следующими свойствами.

1. Используется тот же рабочий каталог, что в командной строке или сеансе PowerShell.
1. Файл выполняется от имени пользователя WSL по умолчанию.
1. Требуются те же права администратора Windows, что и у вызывающего процесса и терминала.

Пример.

```console
C:\temp> bash -c "ls -la"
```

Команды Linux, вызываемые таким образом, обрабатываются как любые другие приложения Windows.  Такие функции, как ввод, конвейерная передача и перенаправление файлов, работают должным образом.

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

Команды WSL, передаваемые в `bash -c`, перенаправляются в процесс WSL без изменения.  Пути к файлам должны быть указаны в формате WSL, кроме того, необходимо внимательно экранировать соответствующие знаки. Пример.

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a>Вызов двоичных файлов Windows из WSL

Подсистема Windows для Linux может вызывать двоичные файлы Windows непосредственно из командной строки WSL.  Приложения, выполняемые таким образом, обладают следующими свойствами.

1. Используется тот же рабочий каталог, что и в командной строке WSL, за исключением сценария, описанного ниже.
1. Они имеют те же разрешения, что и процесс `bash.exe`. 
1. Они выполняются от имени активного пользователя Windows.
1. Они отображаются в диспетчере задач Windows так, как если бы они выполнялись непосредственно из командной строки.

Пример.

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

В WSL эти исполняемые файлы обрабатываются аналогично собственным исполняемым файлам Linux.  Это означает, что добавление каталогов в путь Linux и их конвейерная передача между командами выполняется должным образом.  Примеры

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

Двоичный файл Windows должен иметь расширение файла, его регистр символов должен совпадать с регистром в имени файла и этот файл должен быть исполняемым.  Неисполняемые файлы, включая сценарии пакетной службы и команды, такие как `dir`, могут выполняться с помощью команды `/mnt/c/Windows/System32/cmd.exe /C`.

Примеры

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

Параметры передаются в двоичный файл Windows без изменений.  

Например, следующие команды откроют `C:\temp\foo.txt` в `notepad.exe`.

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

Изменение файлов, расположенных в VolFs (файлы не в `/mnt/<x>`), приложением Windows не поддерживается.  По умолчанию WSL пытается сохранить рабочий каталог двоичного файла Windows в качестве текущего каталога WSL, но если рабочий каталог находится в VolFs, то WSL вернется к каталогу создания экземпляра.

Например, `bash.exe` изначально запускается из `C:\temp`, а текущим каталогом WSL становится корневая папка пользователя.  При вызове `notepad.exe` из корневого каталога пользователя WSL автоматически возвращается к `C:\temp` в качестве рабочего каталога Notepad.exe.

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
