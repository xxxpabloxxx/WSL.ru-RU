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
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a><span data-ttu-id="f959a-103">Подсистема Windows для Linux взаимодействие с Windows</span><span class="sxs-lookup"><span data-stu-id="f959a-103">Windows Subsystem for Linux interoperability with Windows</span></span>

> <span data-ttu-id="f959a-104">**Обновлено для Fall Creators Update.**</span><span class="sxs-lookup"><span data-stu-id="f959a-104">**Updated for Fall Creators Update.**</span></span>  
<span data-ttu-id="f959a-105">Если вы используете Creators Update или Юбилейное обновление, перейдите к [Creators/Юбилейное обновление раздела](interop.md#creators-update-and-anniversary-update).</span><span class="sxs-lookup"><span data-stu-id="f959a-105">If you're running Creators Update or Anniversary Update, jump to the [Creators/Anniversary Update section](interop.md#creators-update-and-anniversary-update).</span></span>

<span data-ttu-id="f959a-106">Подсистема Windows для Linux (WSL) мы постоянно улучшаем методы интеграции между Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="f959a-106">The Windows Subsystem for Linux (WSL) is continuously improving integration between Windows and Linux.</span></span>  <span data-ttu-id="f959a-107">Можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="f959a-107">You can:</span></span>

1. <span data-ttu-id="f959a-108">Вызовите двоичные файлы Windows из консоли Linux.</span><span class="sxs-lookup"><span data-stu-id="f959a-108">Invoke Windows binaries from the Linux console.</span></span>
1. <span data-ttu-id="f959a-109">Вызовите двоичные файлы Linux с помощью консоли Windows.</span><span class="sxs-lookup"><span data-stu-id="f959a-109">Invoke Linux binaries from a Windows console.</span></span>
1. <span data-ttu-id="f959a-110">**Сборки для предварительной оценки Windows 17063 +** совместного использования переменных среды между Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="f959a-110">**Windows Insiders Builds 17063+** Share environment variables between Linux and Windows.</span></span>

<span data-ttu-id="f959a-111">Это обеспечивает удобную работу между Windows и WSL.</span><span class="sxs-lookup"><span data-stu-id="f959a-111">This delivers a seamless experience between Windows and WSL.</span></span>  <span data-ttu-id="f959a-112">Технические сведения приведены в [WSL блог](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span><span class="sxs-lookup"><span data-stu-id="f959a-112">Technical details are on the [WSL blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span></span>

## <a name="run-linux-tools-from-a-windows-command-line"></a><span data-ttu-id="f959a-113">Запуск средств Linux из командной строки Windows</span><span class="sxs-lookup"><span data-stu-id="f959a-113">Run Linux tools from a Windows command line</span></span>

<span data-ttu-id="f959a-114">Запускать исполняемые файлы Linux из командной строки Windows (CMD или PowerShell), используя `wsl.exe <command>`.</span><span class="sxs-lookup"><span data-stu-id="f959a-114">Run Linux binaries from the Windows Command Prompt (CMD or PowerShell) using `wsl.exe <command>`.</span></span>

<span data-ttu-id="f959a-115">Двоичные файлы, вызывается таким образом:</span><span class="sxs-lookup"><span data-stu-id="f959a-115">Binaries invoked in this way:</span></span>

1. <span data-ttu-id="f959a-116">Используйте тот же рабочий каталог, как в текущей строке CMD или PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f959a-116">Use the same working directory as the current CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="f959a-117">Запуск от имени пользователя по умолчанию WSL.</span><span class="sxs-lookup"><span data-stu-id="f959a-117">Run as the WSL default user.</span></span>
1. <span data-ttu-id="f959a-118">Иметь те же права администратора Windows как вызывающий процесс и терминал.</span><span class="sxs-lookup"><span data-stu-id="f959a-118">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="f959a-119">Пример:</span><span class="sxs-lookup"><span data-stu-id="f959a-119">For example:</span></span>

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

<span data-ttu-id="f959a-120">Следующие команды Linux `wsl.exe` обрабатывается как любой команде, выполняемых в WSL.</span><span class="sxs-lookup"><span data-stu-id="f959a-120">The Linux command following `wsl.exe` is handled like any command run in WSL.</span></span>  <span data-ttu-id="f959a-121">Sudo, конвейерная передача и перенаправление файловой работать.</span><span class="sxs-lookup"><span data-stu-id="f959a-121">Things such as sudo, piping, and file redirection work.</span></span>

<span data-ttu-id="f959a-122">Пример, используя "sudo".</span><span class="sxs-lookup"><span data-stu-id="f959a-122">Example using sudo:</span></span>

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

<span data-ttu-id="f959a-123">Примеры смешивание команды WSL и Windows.</span><span class="sxs-lookup"><span data-stu-id="f959a-123">Examples mixing WSL and Windows commands:</span></span>

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

<span data-ttu-id="f959a-124">Переданные команды `wsl.exe` перенаправляются к процессу WSL без изменений.</span><span class="sxs-lookup"><span data-stu-id="f959a-124">The commands passed into `wsl.exe` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="f959a-125">Пути к файлам должен быть указан в формате WSL.</span><span class="sxs-lookup"><span data-stu-id="f959a-125">File paths must be specified in the WSL format.</span></span>

<span data-ttu-id="f959a-126">Пример с путями.</span><span class="sxs-lookup"><span data-stu-id="f959a-126">Example with paths:</span></span>

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a><span data-ttu-id="f959a-127">Запуск средств Windows из WSL</span><span class="sxs-lookup"><span data-stu-id="f959a-127">Run Windows tools from WSL</span></span>

<span data-ttu-id="f959a-128">WSL можно вызвать двоичные файлы Windows непосредственно с помощью командной строки WSL `[binary name].exe`.</span><span class="sxs-lookup"><span data-stu-id="f959a-128">WSL can invoke Windows binaries directly from the WSL command line using `[binary name].exe`.</span></span>  <span data-ttu-id="f959a-129">Например, `notepad.exe`.</span><span class="sxs-lookup"><span data-stu-id="f959a-129">For example, `notepad.exe`.</span></span>  <span data-ttu-id="f959a-130">Чтобы упростить исполняемых файлов Windows для запуска, путь Windows содержится в Linux `$PATH` в Fall Creators Update.</span><span class="sxs-lookup"><span data-stu-id="f959a-130">To make Windows executables easier to run, Windows path is included in the Linux `$PATH` in Fall Creators Update.</span></span>

<span data-ttu-id="f959a-131">Приложения, этот способ выполнения имеют следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="f959a-131">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="f959a-132">Сохранить рабочий каталог как WSL командной строки (в большинстве случаев — исключения как описано ниже).</span><span class="sxs-lookup"><span data-stu-id="f959a-132">Retain the working directory as the WSL command prompt (for the most part -- exceptions are explained below).</span></span>
1. <span data-ttu-id="f959a-133">Имеют одинаковые права разрешение как WSL процесс.</span><span class="sxs-lookup"><span data-stu-id="f959a-133">Have the same permission rights as the WSL process.</span></span>
1. <span data-ttu-id="f959a-134">Запуск от имени активного пользователя Windows.</span><span class="sxs-lookup"><span data-stu-id="f959a-134">Run as the active Windows user.</span></span>
1. <span data-ttu-id="f959a-135">Отображаются в диспетчере задач Windows так, как если бы выполняться непосредственно из Командной строки.</span><span class="sxs-lookup"><span data-stu-id="f959a-135">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="f959a-136">Пример.</span><span class="sxs-lookup"><span data-stu-id="f959a-136">Example:</span></span>

``` BASH
$ notepad.exe
```

<span data-ttu-id="f959a-137">Исполняемые файлы Windows, выполните в WSL обрабатываются аналогичным образом в собственном Linux исполняемые файлы--направление, перенаправление и даже фоновый режим работы должным образом.</span><span class="sxs-lookup"><span data-stu-id="f959a-137">Windows executables run in WSL are handled similarly to native Linux executables -- piping, redirects, and even backgrounding work as expected.</span></span>

<span data-ttu-id="f959a-138">Примеры использования каналов:</span><span class="sxs-lookup"><span data-stu-id="f959a-138">Examples using pipes:</span></span>

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

<span data-ttu-id="f959a-139">Пример использования смешанных команд Windows и WSL.</span><span class="sxs-lookup"><span data-stu-id="f959a-139">Example using mixed Windows and WSL commands:</span></span>

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

<span data-ttu-id="f959a-140">Двоичные файлы Windows должен включать расширение файла совпадает по регистру файла и быть исполняемым.</span><span class="sxs-lookup"><span data-stu-id="f959a-140">Windows binaries must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="f959a-141">Non-исполняемые файлы включая сценарии пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="f959a-141">Non-executables including batch scripts.</span></span>  <span data-ttu-id="f959a-142">CMD собственные команды, такие как `dir` можно запускать с `cmd.exe /C` команды.</span><span class="sxs-lookup"><span data-stu-id="f959a-142">CMD native commands like `dir` can be run with `cmd.exe /C` command.</span></span>

<span data-ttu-id="f959a-143">Примеры</span><span class="sxs-lookup"><span data-stu-id="f959a-143">Examples:</span></span>

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

<span data-ttu-id="f959a-144">Параметры передаются в Windows двоичный без изменений.</span><span class="sxs-lookup"><span data-stu-id="f959a-144">Parameters are passed to the Windows binary unmodified.</span></span>

<span data-ttu-id="f959a-145">Например, следующие команды откроется `C:\temp\foo.txt` в `notepad.exe`:</span><span class="sxs-lookup"><span data-stu-id="f959a-145">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="f959a-146">Изменение файлов, расположенных на VolFs (не при использовании файлов `/mnt/<x>`) с Windows приложение в WSL не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f959a-146">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application in WSL is not supported.</span></span>

<span data-ttu-id="f959a-147">По умолчанию WSL пытается сохранить рабочий каталог Windows двоичные значения как текущего каталога WSL, но если рабочий каталог находится на VolFs вернется на каталог создания экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f959a-147">By default, WSL tries to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="f959a-148">В качестве примера; `wsl.exe` первоначально запускается из `C:\temp` и текущий каталог WSL изменяется на домашнюю страницу пользователя.</span><span class="sxs-lookup"><span data-stu-id="f959a-148">As an example; `wsl.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="f959a-149">Когда `notepad.exe` вызывается из корневого каталога документов пользователя, WSL автоматический возврат к `C:\temp` качестве рабочего каталога notepad.exe:</span><span class="sxs-lookup"><span data-stu-id="f959a-149">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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

## <a name="share-environment-variables-between-windows-and-wsl"></a><span data-ttu-id="f959a-150">Совместное использование переменных среды между Windows и WSL</span><span class="sxs-lookup"><span data-stu-id="f959a-150">Share environment variables between Windows and WSL</span></span>

> <span data-ttu-id="f959a-151">Доступно в сборках Windows Insider 17063 и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="f959a-151">Available in Windows Insider builds 17063 and later.</span></span>

<span data-ttu-id="f959a-152">До появления 17063, было только Windows переменная среды, которая может получить доступ к WSL `PATH` (поэтому мог запускать исполняемые файлы Win32 из WSL).</span><span class="sxs-lookup"><span data-stu-id="f959a-152">Prior to 17063, only Windows environment variable that WSL could access was `PATH` (so you could launch Win32 executables from under WSL).</span></span>

<span data-ttu-id="f959a-153">Начиная с 17063, WSL и Windows используют `WSLENV`, специальные среды переменная, созданная на дистрибутивы Windows и Linux, на WSL.</span><span class="sxs-lookup"><span data-stu-id="f959a-153">Starting in 17063, WSL and Windows share `WSLENV`, a special environment variable created to bridge Windows and Linux distros running on WSL.</span></span>

<span data-ttu-id="f959a-154">Свойства `WSLENV`:</span><span class="sxs-lookup"><span data-stu-id="f959a-154">Properties of `WSLENV`:</span></span>

* <span data-ttu-id="f959a-155">Он является общим; он существует в средах Windows и WSL.</span><span class="sxs-lookup"><span data-stu-id="f959a-155">It is shared; it exists in both Windows and WSL environments.</span></span>
* <span data-ttu-id="f959a-156">Это список переменных среды для совместного использования между Windows и WSL.</span><span class="sxs-lookup"><span data-stu-id="f959a-156">It is a list of environment variables to share between Windows and WSL.</span></span>
* <span data-ttu-id="f959a-157">Его можно отформатировать переменные среды, работают в Windows и WSL.</span><span class="sxs-lookup"><span data-stu-id="f959a-157">It can format environment variables to work well in Windows and WSL.</span></span>

<span data-ttu-id="f959a-158">Существует четыре флаги в `WSLENV` на преобразование этой переменной среды.</span><span class="sxs-lookup"><span data-stu-id="f959a-158">There are four flags available in `WSLENV` to influence how that environment variable is translated.</span></span>

<span data-ttu-id="f959a-159">`WSLENV` флаги:</span><span class="sxs-lookup"><span data-stu-id="f959a-159">`WSLENV` flags:</span></span>

* <span data-ttu-id="f959a-160">`/p` — Преобразует путь между WSL/Linux стиля пути и пути Win32.</span><span class="sxs-lookup"><span data-stu-id="f959a-160">`/p` - translates the path between WSL/Linux style paths and Win32 paths.</span></span>
* <span data-ttu-id="f959a-161">`/l` — Указывает список путей переменной среды.</span><span class="sxs-lookup"><span data-stu-id="f959a-161">`/l` - indicates the environment variable is a list of paths.</span></span>
* <span data-ttu-id="f959a-162">`/u` — Указывает, что эта переменная среды должны быть включены только при запуске WSL из Win32.</span><span class="sxs-lookup"><span data-stu-id="f959a-162">`/u` - indicates that this environment variable should only be included when running WSL from Win32.</span></span>
* <span data-ttu-id="f959a-163">`/w` — Указывает, что эта переменная среды должны быть включены только при запуске из WSL Win32.</span><span class="sxs-lookup"><span data-stu-id="f959a-163">`/w` - indicates that this environment variable should only be included when running Win32 from WSL.</span></span>

<span data-ttu-id="f959a-164">Флаги могут быть объединены, при необходимости.</span><span class="sxs-lookup"><span data-stu-id="f959a-164">Flags can be combined as needed.</span></span>

## <a name="disable-interop"></a><span data-ttu-id="f959a-165">Отключить взаимодействия</span><span class="sxs-lookup"><span data-stu-id="f959a-165">Disable Interop</span></span>

<span data-ttu-id="f959a-166">Пользователи могут отключить возможность запускать исполняемые файлы Windows на WSL время одного сеанса, выполнив следующую команду в качестве привилегированного пользователя:</span><span class="sxs-lookup"><span data-stu-id="f959a-166">Users may disable the ability to run Windows binaries for a single WSL session by running the following command as root:</span></span>

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="f959a-167">Чтобы включить Windows двоичные файлы либо выйти из всех сеансов WSL и повторно запустите bash.exe либо выполните следующую команду в качестве привилегированного пользователя:</span><span class="sxs-lookup"><span data-stu-id="f959a-167">To reenable Windows binaries either exit all WSL sessions and re-run bash.exe or run the following command as root:</span></span>

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="f959a-168">Отключение взаимодействия не сохраняются между сеансами WSL--взаимодействия включаются снова при запуске нового сеанса.</span><span class="sxs-lookup"><span data-stu-id="f959a-168">Disabling interop will not persist between WSL sessions -- interop will be enabled again when a new session is launched.</span></span>

## <a name="creators-update-and-anniversary-update"></a><span data-ttu-id="f959a-169">Creators Update и Центр обновления Годовщина</span><span class="sxs-lookup"><span data-stu-id="f959a-169">Creators Update and Anniversary Update</span></span>

<span data-ttu-id="f959a-170">Во время предварительной осенью взаимодействия качества Creators Update похожа на более новый опыт взаимодействия, доступно несколько существенных различий.</span><span class="sxs-lookup"><span data-stu-id="f959a-170">While the interop experience pre-Fall Creators Update is similar to more recent interop experiences, there are a handful of major differences.</span></span>

<span data-ttu-id="f959a-171">Подведем итоги.</span><span class="sxs-lookup"><span data-stu-id="f959a-171">To summarize:</span></span>

* <span data-ttu-id="f959a-172">`bash.exe` устарели и заменены `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="f959a-172">`bash.exe` has been deprecated and replaced with `wsl.exe`.</span></span>
* <span data-ttu-id="f959a-173">`-c` параметр для выполнения одной команды с не нужен `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="f959a-173">`-c` option for running a single command isn't needed with `wsl.exe`.</span></span>
* <span data-ttu-id="f959a-174">Путь Windows содержится в WSL `$PATH`</span><span class="sxs-lookup"><span data-stu-id="f959a-174">Windows path is included in the WSL `$PATH`</span></span>

<span data-ttu-id="f959a-175">Процесс отключения взаимодействия не изменяется.</span><span class="sxs-lookup"><span data-stu-id="f959a-175">The process for disabling interop is unchanged.</span></span>

### <a name="invoking-wsl-from-the-windows-command-line"></a><span data-ttu-id="f959a-176">Вызов WSL из командной строки Windows</span><span class="sxs-lookup"><span data-stu-id="f959a-176">Invoking WSL from the Windows Command Line</span></span>

<span data-ttu-id="f959a-177">Двоичные файлы Linux могут вызываться из командной строки Windows или с помощью PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f959a-177">Linux binaries can be invoked from the Windows Command Prompt or from PowerShell.</span></span>  <span data-ttu-id="f959a-178">Двоичные файлы, вызывается таким образом, имеют следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="f959a-178">Binaries invoked in this way have the following properties:</span></span>

1. <span data-ttu-id="f959a-179">Используйте тот же рабочий каталог в командной строке команду CMD и PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f959a-179">Use the same working directory as the CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="f959a-180">Запуск от имени пользователя по умолчанию WSL.</span><span class="sxs-lookup"><span data-stu-id="f959a-180">Run as the WSL default user.</span></span>
1. <span data-ttu-id="f959a-181">Иметь те же права администратора Windows как вызывающий процесс и терминал.</span><span class="sxs-lookup"><span data-stu-id="f959a-181">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="f959a-182">Пример.</span><span class="sxs-lookup"><span data-stu-id="f959a-182">Example:</span></span>

```console
C:\temp> bash -c "ls -la"
```

<span data-ttu-id="f959a-183">Команды Linux, называемые таким образом, обрабатываются как и любое другое приложение Windows.</span><span class="sxs-lookup"><span data-stu-id="f959a-183">Linux commands called in this way are handled like any other Windows application.</span></span>  <span data-ttu-id="f959a-184">Входные данные, конвейерная передача и перенаправление файловой работать должным образом.</span><span class="sxs-lookup"><span data-stu-id="f959a-184">Things such as input, piping, and file redirection work as expected.</span></span>

<span data-ttu-id="f959a-185">Примеры</span><span class="sxs-lookup"><span data-stu-id="f959a-185">Examples:</span></span>

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

<span data-ttu-id="f959a-186">Переданные команды WSL `bash -c` перенаправляются к процессу WSL без изменений.</span><span class="sxs-lookup"><span data-stu-id="f959a-186">The WSL commands passed into `bash -c` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="f959a-187">Пути к файлам должен быть указан в формате WSL и будьте осторожны в escape-символы, соответствующие.</span><span class="sxs-lookup"><span data-stu-id="f959a-187">File paths must be specified in the WSL format and care must be taken to escape relevant characters.</span></span> <span data-ttu-id="f959a-188">Пример.</span><span class="sxs-lookup"><span data-stu-id="f959a-188">Example:</span></span>

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a><span data-ttu-id="f959a-189">Вызов WSL двоичных файлов Windows</span><span class="sxs-lookup"><span data-stu-id="f959a-189">Invoking Windows binaries from WSL</span></span>

<span data-ttu-id="f959a-190">Подсистема Windows для Linux можно вызвать двоичные файлы Windows непосредственно из командной строки WSL.</span><span class="sxs-lookup"><span data-stu-id="f959a-190">The Windows Subsystem for Linux can invoke Windows binaries directly from the WSL command line.</span></span>  <span data-ttu-id="f959a-191">Приложения, этот способ выполнения имеют следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="f959a-191">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="f959a-192">Оставлять рабочий каталог WSL командной строки за исключением сценарий, описанный ниже.</span><span class="sxs-lookup"><span data-stu-id="f959a-192">Retain the working directory as the WSL command prompt except in the scenario explained below.</span></span>
1. <span data-ttu-id="f959a-193">Имеют те же права разрешение, что `bash.exe` процесса.</span><span class="sxs-lookup"><span data-stu-id="f959a-193">Have the same permission rights as the `bash.exe` process.</span></span> 
1. <span data-ttu-id="f959a-194">Запуск от имени активного пользователя Windows.</span><span class="sxs-lookup"><span data-stu-id="f959a-194">Run as the active Windows user.</span></span>
1. <span data-ttu-id="f959a-195">Отображаются в диспетчере задач Windows так, как если бы выполняться непосредственно из Командной строки.</span><span class="sxs-lookup"><span data-stu-id="f959a-195">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="f959a-196">Пример.</span><span class="sxs-lookup"><span data-stu-id="f959a-196">Example:</span></span>

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

<span data-ttu-id="f959a-197">В WSL эти исполняемые файлы обрабатываются аналогично собственного исполняемых файлов Linux.</span><span class="sxs-lookup"><span data-stu-id="f959a-197">In WSL, these executables are handled similar to native Linux executables.</span></span>  <span data-ttu-id="f959a-198">Это означает, что добавление каталогов в пути Linux и передачи между команды работает должным образом.</span><span class="sxs-lookup"><span data-stu-id="f959a-198">This means adding directories to the Linux path and piping between commands works as expected.</span></span>  <span data-ttu-id="f959a-199">Примеры</span><span class="sxs-lookup"><span data-stu-id="f959a-199">Examples:</span></span>

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

<span data-ttu-id="f959a-200">Двоичный файл Windows должен включать расширение файла совпадает по регистру файла и быть исполняемым.</span><span class="sxs-lookup"><span data-stu-id="f959a-200">The Windows binary must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="f959a-201">Non-исполняемых файлов включая сценарии пакетной обработки и команды, такие как `dir` можно запускать с `/mnt/c/Windows/System32/cmd.exe /C` команды.</span><span class="sxs-lookup"><span data-stu-id="f959a-201">Non-executables including batch scripts and command like `dir` can be run with `/mnt/c/Windows/System32/cmd.exe /C` command.</span></span>

<span data-ttu-id="f959a-202">Примеры</span><span class="sxs-lookup"><span data-stu-id="f959a-202">Examples:</span></span>

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

<span data-ttu-id="f959a-203">Параметры передаются в Windows двоичный без изменений.</span><span class="sxs-lookup"><span data-stu-id="f959a-203">Parameters are passed to the Windows binary unmodified.</span></span>  

<span data-ttu-id="f959a-204">Например, следующие команды откроется `C:\temp\foo.txt` в `notepad.exe`:</span><span class="sxs-lookup"><span data-stu-id="f959a-204">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="f959a-205">Изменение файлов, расположенных на VolFs (не при использовании файлов `/mnt/<x>`) с Windows приложение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f959a-205">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application is not supported.</span></span>  <span data-ttu-id="f959a-206">По умолчанию WSL пытается сохранить рабочий каталог Windows двоичные значения как текущего каталога WSL, но если рабочий каталог находится на VolFs вернется на каталог создания экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f959a-206">By default, WSL attempts to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="f959a-207">В качестве примера; `bash.exe` первоначально запускается из `C:\temp` и текущий каталог WSL изменяется на домашнюю страницу пользователя.</span><span class="sxs-lookup"><span data-stu-id="f959a-207">As an example; `bash.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="f959a-208">Когда `notepad.exe` вызывается из корневого каталога документов пользователя, WSL автоматический возврат к `C:\temp` качестве рабочего каталога notepad.exe:</span><span class="sxs-lookup"><span data-stu-id="f959a-208">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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
