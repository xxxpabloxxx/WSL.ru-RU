---
title: Взаимодействие Windows с Linux
description: Описывается взаимодействие Windows с дистрибутивами Linux, работающими в подсистеме Windows для Linux.
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 3f3df3337ece75d7af77313f5fc55eb4e18e31cb
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122735"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a><span data-ttu-id="61c46-103">Подсистема Windows для взаимодействия Linux с Windows</span><span class="sxs-lookup"><span data-stu-id="61c46-103">Windows Subsystem for Linux interoperability with Windows</span></span>

> <span data-ttu-id="61c46-104">**Статья обновлена с учетом Fall Creators Update.**</span><span class="sxs-lookup"><span data-stu-id="61c46-104">**Updated for Fall Creators Update.**</span></span>  
<span data-ttu-id="61c46-105">Если вы используете Creators Update или юбилейное обновление, перейдите к разделу [Обновление Creators Update и юбилейное обновление](interop.md#creators-update-and-anniversary-update).</span><span class="sxs-lookup"><span data-stu-id="61c46-105">If you're running Creators Update or Anniversary Update, jump to the [Creators/Anniversary Update section](interop.md#creators-update-and-anniversary-update).</span></span>

<span data-ttu-id="61c46-106">В подсистеме Windows для Linux (WSL) постоянно улучшается интеграция между Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="61c46-106">The Windows Subsystem for Linux (WSL) is continuously improving integration between Windows and Linux.</span></span>  <span data-ttu-id="61c46-107">Можно сделать следующее.</span><span class="sxs-lookup"><span data-stu-id="61c46-107">You can:</span></span>

1. <span data-ttu-id="61c46-108">Вызов двоичных файлов Windows из консоли Linux.</span><span class="sxs-lookup"><span data-stu-id="61c46-108">Invoke Windows binaries from the Linux console.</span></span>
1. <span data-ttu-id="61c46-109">Вызов двоичных файлов Linux из консоли Windows.</span><span class="sxs-lookup"><span data-stu-id="61c46-109">Invoke Linux binaries from a Windows console.</span></span>
1. <span data-ttu-id="61c46-110">**Сборки для программы предварительной оценки Windows (17063 и выше)** : совместное использование переменных среды между Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="61c46-110">**Windows Insiders Builds 17063+** Share environment variables between Linux and Windows.</span></span>

<span data-ttu-id="61c46-111">Это обеспечивает эффективное взаимодействие между Windows и WSL.</span><span class="sxs-lookup"><span data-stu-id="61c46-111">This delivers a seamless experience between Windows and WSL.</span></span>  <span data-ttu-id="61c46-112">Технические сведения доступны в [блоге по WSL](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span><span class="sxs-lookup"><span data-stu-id="61c46-112">Technical details are on the [WSL blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span></span>

## <a name="run-linux-tools-from-a-windows-command-line"></a><span data-ttu-id="61c46-113">Запуск инструментов Linux из командной строки Windows</span><span class="sxs-lookup"><span data-stu-id="61c46-113">Run Linux tools from a Windows command line</span></span>

<span data-ttu-id="61c46-114">Запускайте двоичные файлы Linux из командной строки Windows (CMD или PowerShell), используя `wsl.exe <command>`.</span><span class="sxs-lookup"><span data-stu-id="61c46-114">Run Linux binaries from the Windows Command Prompt (CMD or PowerShell) using `wsl.exe <command>`.</span></span>

<span data-ttu-id="61c46-115">Двоичные файлы вызываются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="61c46-115">Binaries invoked in this way:</span></span>

1. <span data-ttu-id="61c46-116">Используется тот же рабочий каталог, что и для текущей командной строки или сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="61c46-116">Use the same working directory as the current CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="61c46-117">Файл выполняется от имени пользователя WSL по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="61c46-117">Run as the WSL default user.</span></span>
1. <span data-ttu-id="61c46-118">Требуются те же права администратора Windows, что и у вызывающего процесса и терминала.</span><span class="sxs-lookup"><span data-stu-id="61c46-118">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="61c46-119">Например:</span><span class="sxs-lookup"><span data-stu-id="61c46-119">For example:</span></span>

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

<span data-ttu-id="61c46-120">Команда Linux после `wsl.exe` обрабатывается как любая команда, выполняемая в WSL.</span><span class="sxs-lookup"><span data-stu-id="61c46-120">The Linux command following `wsl.exe` is handled like any command run in WSL.</span></span>  <span data-ttu-id="61c46-121">Можно выполнять sudo, конвейерную передачу и перенаправление файлов.</span><span class="sxs-lookup"><span data-stu-id="61c46-121">Things such as sudo, piping, and file redirection work.</span></span>

<span data-ttu-id="61c46-122">Пример использования sudo.</span><span class="sxs-lookup"><span data-stu-id="61c46-122">Example using sudo:</span></span>

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

<span data-ttu-id="61c46-123">Примеры совместного выполнения команд WSL и Windows.</span><span class="sxs-lookup"><span data-stu-id="61c46-123">Examples mixing WSL and Windows commands:</span></span>

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

<span data-ttu-id="61c46-124">Команды, передаваемые в `wsl.exe`, перенаправляются в процесс WSL без изменения.</span><span class="sxs-lookup"><span data-stu-id="61c46-124">The commands passed into `wsl.exe` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="61c46-125">Пути к файлам должны быть указаны в формате WSL.</span><span class="sxs-lookup"><span data-stu-id="61c46-125">File paths must be specified in the WSL format.</span></span>

<span data-ttu-id="61c46-126">Пример с путями.</span><span class="sxs-lookup"><span data-stu-id="61c46-126">Example with paths:</span></span>

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a><span data-ttu-id="61c46-127">Запуск инструментов Windows из WSL</span><span class="sxs-lookup"><span data-stu-id="61c46-127">Run Windows tools from WSL</span></span>

<span data-ttu-id="61c46-128">WSL может вызывать двоичные файлы Windows непосредственно из командной строки WSL с помощью `[binary name].exe`.</span><span class="sxs-lookup"><span data-stu-id="61c46-128">WSL can invoke Windows binaries directly from the WSL command line using `[binary name].exe`.</span></span>  <span data-ttu-id="61c46-129">Например, `notepad.exe`.</span><span class="sxs-lookup"><span data-stu-id="61c46-129">For example, `notepad.exe`.</span></span>  <span data-ttu-id="61c46-130">Чтобы упростить запуск исполняемых файлов Windows, в обновлении Fall Creators Update путь Windows добавлен в переменную `$PATH` Linux.</span><span class="sxs-lookup"><span data-stu-id="61c46-130">To make Windows executables easier to run, Windows path is included in the Linux `$PATH` in Fall Creators Update.</span></span>

<span data-ttu-id="61c46-131">Приложения, выполняемые таким образом, обладают следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="61c46-131">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="61c46-132">Рабочим каталогом остается каталог командной строки WSL (в большинстве случаев; исключения описаны ниже).</span><span class="sxs-lookup"><span data-stu-id="61c46-132">Retain the working directory as the WSL command prompt (for the most part -- exceptions are explained below).</span></span>
1. <span data-ttu-id="61c46-133">Они имеют те же разрешения, что и процесс WSL.</span><span class="sxs-lookup"><span data-stu-id="61c46-133">Have the same permission rights as the WSL process.</span></span>
1. <span data-ttu-id="61c46-134">Они выполняются от имени активного пользователя Windows.</span><span class="sxs-lookup"><span data-stu-id="61c46-134">Run as the active Windows user.</span></span>
1. <span data-ttu-id="61c46-135">Они отображаются в диспетчере задач Windows так, как если бы они выполнялись непосредственно из командной строки.</span><span class="sxs-lookup"><span data-stu-id="61c46-135">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="61c46-136">Пример.</span><span class="sxs-lookup"><span data-stu-id="61c46-136">Example:</span></span>

``` BASH
$ notepad.exe
```

<span data-ttu-id="61c46-137">Исполняемые файлы Windows, выполняемые в WSL, обрабатываются аналогично собственным исполняемым файлам Linux — конвейерной передаче, перенаправлению и даже фоновому режиму работы.</span><span class="sxs-lookup"><span data-stu-id="61c46-137">Windows executables run in WSL are handled similarly to native Linux executables -- piping, redirects, and even backgrounding work as expected.</span></span>

<span data-ttu-id="61c46-138">Примеры использования каналов.</span><span class="sxs-lookup"><span data-stu-id="61c46-138">Examples using pipes:</span></span>

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

<span data-ttu-id="61c46-139">Пример использования сочетания команд Windows и WSL.</span><span class="sxs-lookup"><span data-stu-id="61c46-139">Example using mixed Windows and WSL commands:</span></span>

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

<span data-ttu-id="61c46-140">Двоичные файлы Windows должны иметь расширение файла, его регистр символов должен совпадать с регистром в имени файла и эти файлы должны быть исполняемыми.</span><span class="sxs-lookup"><span data-stu-id="61c46-140">Windows binaries must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="61c46-141">Неисполняемые файлы, в том числе сценарии пакетного выполнения и</span><span class="sxs-lookup"><span data-stu-id="61c46-141">Non-executables including batch scripts.</span></span>  <span data-ttu-id="61c46-142">собственные команды командной строки, такие как `dir`, можно выполнять с помощью команды `cmd.exe /C`.</span><span class="sxs-lookup"><span data-stu-id="61c46-142">CMD native commands like `dir` can be run with `cmd.exe /C` command.</span></span>

<span data-ttu-id="61c46-143">Примеры</span><span class="sxs-lookup"><span data-stu-id="61c46-143">Examples:</span></span>

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

<span data-ttu-id="61c46-144">Параметры передаются в двоичный файл Windows без изменений.</span><span class="sxs-lookup"><span data-stu-id="61c46-144">Parameters are passed to the Windows binary unmodified.</span></span>

<span data-ttu-id="61c46-145">Например, следующие команды откроют `C:\temp\foo.txt` в `notepad.exe`.</span><span class="sxs-lookup"><span data-stu-id="61c46-145">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="61c46-146">Изменение файлов, находящихся в VolFs (файлы не в `/mnt/<x>`), приложением для Windows в WSL не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="61c46-146">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application in WSL is not supported.</span></span>

<span data-ttu-id="61c46-147">По умолчанию WSL пытается оставить рабочий каталог двоичного файла Windows в качестве текущего каталога WSL, но если рабочий каталог находится в VolFs, то WSL вернется к каталогу создания экземпляра.</span><span class="sxs-lookup"><span data-stu-id="61c46-147">By default, WSL tries to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="61c46-148">Например, `wsl.exe` изначально запускается из `C:\temp`, а текущим каталогом WSL становится корневая папка пользователя.</span><span class="sxs-lookup"><span data-stu-id="61c46-148">As an example; `wsl.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="61c46-149">При вызове `notepad.exe` из корневого каталога пользователя WSL автоматически возвращается к `C:\temp` в качестве рабочего каталога Notepad.exe.</span><span class="sxs-lookup"><span data-stu-id="61c46-149">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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

## <a name="share-environment-variables-between-windows-and-wsl"></a><span data-ttu-id="61c46-150">Совместное использование переменных среды между Windows и WSL</span><span class="sxs-lookup"><span data-stu-id="61c46-150">Share environment variables between Windows and WSL</span></span>

> <span data-ttu-id="61c46-151">Доступно в выпусках для программы предварительной оценки Windows, начиная со сборки 17063.</span><span class="sxs-lookup"><span data-stu-id="61c46-151">Available in Windows Insider builds 17063 and later.</span></span>

<span data-ttu-id="61c46-152">До выпуска сборки 17063 единственной переменной среды Windows,, к которой могла получить доступ WSL, была `PATH` (это позволяло запускать исполняемые файлы Win32 из WSL).</span><span class="sxs-lookup"><span data-stu-id="61c46-152">Prior to 17063, only Windows environment variable that WSL could access was `PATH` (so you could launch Win32 executables from under WSL).</span></span>

<span data-ttu-id="61c46-153">Начиная со сборки 17063 решение WSL и Windows совместно используют `WSLENV` — специальную переменную среды, созданную для взаимодействия Windows и дистрибутивов Linux, запущенных в WSL.</span><span class="sxs-lookup"><span data-stu-id="61c46-153">Starting in 17063, WSL and Windows share `WSLENV`, a special environment variable created to bridge Windows and Linux distros running on WSL.</span></span>

<span data-ttu-id="61c46-154">Свойства `WSLENV`:</span><span class="sxs-lookup"><span data-stu-id="61c46-154">Properties of `WSLENV`:</span></span>

* <span data-ttu-id="61c46-155">она используется совместно и существует в средах Windows и WSL;</span><span class="sxs-lookup"><span data-stu-id="61c46-155">It is shared; it exists in both Windows and WSL environments.</span></span>
* <span data-ttu-id="61c46-156">это список переменных среды, которые совместно используют Windows и WSL;</span><span class="sxs-lookup"><span data-stu-id="61c46-156">It is a list of environment variables to share between Windows and WSL.</span></span>
* <span data-ttu-id="61c46-157">она позволяет форматировать список переменных среды для корректного использования в Windows и WSL.</span><span class="sxs-lookup"><span data-stu-id="61c46-157">It can format environment variables to work well in Windows and WSL.</span></span>

<span data-ttu-id="61c46-158">В `WSLENV` доступны четыре флага, влияющие на способ преобразования переменной среды.</span><span class="sxs-lookup"><span data-stu-id="61c46-158">There are four flags available in `WSLENV` to influence how that environment variable is translated.</span></span>

<span data-ttu-id="61c46-159">Флаги `WSLENV`:</span><span class="sxs-lookup"><span data-stu-id="61c46-159">`WSLENV` flags:</span></span>

* <span data-ttu-id="61c46-160">`/p` преобразовывает пути WSL и Linux в пути Win32 и наоборот;</span><span class="sxs-lookup"><span data-stu-id="61c46-160">`/p` - translates the path between WSL/Linux style paths and Win32 paths.</span></span>
* <span data-ttu-id="61c46-161">`/l` указывает, что переменная среды представляет собой список путей;</span><span class="sxs-lookup"><span data-stu-id="61c46-161">`/l` - indicates the environment variable is a list of paths.</span></span>
* <span data-ttu-id="61c46-162">`/u` указывает, что эту переменную среды следует добавлять только при запуске WSL из Win32;</span><span class="sxs-lookup"><span data-stu-id="61c46-162">`/u` - indicates that this environment variable should only be included when running WSL from Win32.</span></span>
* <span data-ttu-id="61c46-163">`/w` указывает, что эту переменную среды следует добавлять только при запуске Win32 из WSL.</span><span class="sxs-lookup"><span data-stu-id="61c46-163">`/w` - indicates that this environment variable should only be included when running Win32 from WSL.</span></span>

<span data-ttu-id="61c46-164">При необходимости флаги можно комбинировать.</span><span class="sxs-lookup"><span data-stu-id="61c46-164">Flags can be combined as needed.</span></span>

## <a name="disable-interop"></a><span data-ttu-id="61c46-165">Отключение взаимодействия</span><span class="sxs-lookup"><span data-stu-id="61c46-165">Disable Interop</span></span>

<span data-ttu-id="61c46-166">Пользователи могут отключить возможность запуска двоичных файлов Windows для отдельного сеанса WSL, выполнив следующую команду в качестве привилегированного пользователя.</span><span class="sxs-lookup"><span data-stu-id="61c46-166">Users may disable the ability to run Windows binaries for a single WSL session by running the following command as root:</span></span>

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="61c46-167">Чтобы повторно включить возможность запуска двоичных файлов Windows, закройте все сеансы WSL и повторно запустите bash.exe или выполните следующую команду от имени привилегированного пользователя.</span><span class="sxs-lookup"><span data-stu-id="61c46-167">To reenable Windows binaries either exit all WSL sessions and re-run bash.exe or run the following command as root:</span></span>

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="61c46-168">Отключение взаимодействия не будет сохраняться между сеансами WSL, оно снова будет включено при запуске нового сеанса.</span><span class="sxs-lookup"><span data-stu-id="61c46-168">Disabling interop will not persist between WSL sessions -- interop will be enabled again when a new session is launched.</span></span>

## <a name="creators-update-and-anniversary-update"></a><span data-ttu-id="61c46-169">Обновление Creators Update и юбилейное обновление</span><span class="sxs-lookup"><span data-stu-id="61c46-169">Creators Update and Anniversary Update</span></span>

<span data-ttu-id="61c46-170">Несмотря на то, что возможности взаимодействия до выпуска обновления Fall Creators Update схожи с возможностями последней версии взаимодействия, существует несколько основных отличий.</span><span class="sxs-lookup"><span data-stu-id="61c46-170">While the interop experience pre-Fall Creators Update is similar to more recent interop experiences, there are a handful of major differences.</span></span>

<span data-ttu-id="61c46-171">Вот о чем речь:</span><span class="sxs-lookup"><span data-stu-id="61c46-171">To summarize:</span></span>

* <span data-ttu-id="61c46-172">`bash.exe` является нерекомендуемым и заменен на `wsl.exe`;</span><span class="sxs-lookup"><span data-stu-id="61c46-172">`bash.exe` has been deprecated and replaced with `wsl.exe`.</span></span>
* <span data-ttu-id="61c46-173">параметр `-c` не требуется для выполнения одной команды `wsl.exe`;</span><span class="sxs-lookup"><span data-stu-id="61c46-173">`-c` option for running a single command isn't needed with `wsl.exe`.</span></span>
* <span data-ttu-id="61c46-174">путь Windows включен в переменную `$PATH` WSL.</span><span class="sxs-lookup"><span data-stu-id="61c46-174">Windows path is included in the WSL `$PATH`</span></span>

<span data-ttu-id="61c46-175">Процесс отключения взаимодействия не изменяется.</span><span class="sxs-lookup"><span data-stu-id="61c46-175">The process for disabling interop is unchanged.</span></span>

### <a name="invoking-wsl-from-the-windows-command-line"></a><span data-ttu-id="61c46-176">Вызов WSL из командной строки Windows</span><span class="sxs-lookup"><span data-stu-id="61c46-176">Invoking WSL from the Windows Command Line</span></span>

<span data-ttu-id="61c46-177">Двоичные файлы Linux можно вызывать из командной строки Windows или PowerShell.</span><span class="sxs-lookup"><span data-stu-id="61c46-177">Linux binaries can be invoked from the Windows Command Prompt or from PowerShell.</span></span>  <span data-ttu-id="61c46-178">Двоичные файлы, вызываемые таким способом, обладают следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="61c46-178">Binaries invoked in this way have the following properties:</span></span>

1. <span data-ttu-id="61c46-179">Используется тот же рабочий каталог, что в командной строке или сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="61c46-179">Use the same working directory as the CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="61c46-180">Файл выполняется от имени пользователя WSL по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="61c46-180">Run as the WSL default user.</span></span>
1. <span data-ttu-id="61c46-181">Требуются те же права администратора Windows, что и у вызывающего процесса и терминала.</span><span class="sxs-lookup"><span data-stu-id="61c46-181">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="61c46-182">Пример.</span><span class="sxs-lookup"><span data-stu-id="61c46-182">Example:</span></span>

```console
C:\temp> bash -c "ls -la"
```

<span data-ttu-id="61c46-183">Команды Linux, вызываемые таким образом, обрабатываются как любые другие приложения Windows.</span><span class="sxs-lookup"><span data-stu-id="61c46-183">Linux commands called in this way are handled like any other Windows application.</span></span>  <span data-ttu-id="61c46-184">Такие функции, как ввод, конвейерная передача и перенаправление файлов, работают должным образом.</span><span class="sxs-lookup"><span data-stu-id="61c46-184">Things such as input, piping, and file redirection work as expected.</span></span>

<span data-ttu-id="61c46-185">Примеры</span><span class="sxs-lookup"><span data-stu-id="61c46-185">Examples:</span></span>

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

<span data-ttu-id="61c46-186">Команды WSL, передаваемые в `bash -c`, перенаправляются в процесс WSL без изменения.</span><span class="sxs-lookup"><span data-stu-id="61c46-186">The WSL commands passed into `bash -c` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="61c46-187">Пути к файлам должны быть указаны в формате WSL, кроме того, необходимо внимательно экранировать соответствующие знаки.</span><span class="sxs-lookup"><span data-stu-id="61c46-187">File paths must be specified in the WSL format and care must be taken to escape relevant characters.</span></span> <span data-ttu-id="61c46-188">Пример.</span><span class="sxs-lookup"><span data-stu-id="61c46-188">Example:</span></span>

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a><span data-ttu-id="61c46-189">Вызов двоичных файлов Windows из WSL</span><span class="sxs-lookup"><span data-stu-id="61c46-189">Invoking Windows binaries from WSL</span></span>

<span data-ttu-id="61c46-190">Подсистема Windows для Linux может вызывать двоичные файлы Windows непосредственно из командной строки WSL.</span><span class="sxs-lookup"><span data-stu-id="61c46-190">The Windows Subsystem for Linux can invoke Windows binaries directly from the WSL command line.</span></span>  <span data-ttu-id="61c46-191">Приложения, выполняемые таким образом, обладают следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="61c46-191">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="61c46-192">Используется тот же рабочий каталог, что и в командной строке WSL, за исключением сценария, описанного ниже.</span><span class="sxs-lookup"><span data-stu-id="61c46-192">Retain the working directory as the WSL command prompt except in the scenario explained below.</span></span>
1. <span data-ttu-id="61c46-193">Они имеют те же разрешения, что и процесс `bash.exe`.</span><span class="sxs-lookup"><span data-stu-id="61c46-193">Have the same permission rights as the `bash.exe` process.</span></span> 
1. <span data-ttu-id="61c46-194">Они выполняются от имени активного пользователя Windows.</span><span class="sxs-lookup"><span data-stu-id="61c46-194">Run as the active Windows user.</span></span>
1. <span data-ttu-id="61c46-195">Они отображаются в диспетчере задач Windows так, как если бы они выполнялись непосредственно из командной строки.</span><span class="sxs-lookup"><span data-stu-id="61c46-195">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="61c46-196">Пример.</span><span class="sxs-lookup"><span data-stu-id="61c46-196">Example:</span></span>

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

<span data-ttu-id="61c46-197">В WSL эти исполняемые файлы обрабатываются аналогично собственным исполняемым файлам Linux.</span><span class="sxs-lookup"><span data-stu-id="61c46-197">In WSL, these executables are handled similar to native Linux executables.</span></span>  <span data-ttu-id="61c46-198">Это означает, что добавление каталогов в путь Linux и их конвейерная передача между командами выполняется должным образом.</span><span class="sxs-lookup"><span data-stu-id="61c46-198">This means adding directories to the Linux path and piping between commands works as expected.</span></span>  <span data-ttu-id="61c46-199">Примеры</span><span class="sxs-lookup"><span data-stu-id="61c46-199">Examples:</span></span>

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

<span data-ttu-id="61c46-200">Двоичный файл Windows должен иметь расширение файла, его регистр символов должен совпадать с регистром в имени файла и этот файл должен быть исполняемым.</span><span class="sxs-lookup"><span data-stu-id="61c46-200">The Windows binary must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="61c46-201">Неисполняемые файлы, включая сценарии пакетной службы и команды, такие как `dir`, могут выполняться с помощью команды `/mnt/c/Windows/System32/cmd.exe /C`.</span><span class="sxs-lookup"><span data-stu-id="61c46-201">Non-executables including batch scripts and command like `dir` can be run with `/mnt/c/Windows/System32/cmd.exe /C` command.</span></span>

<span data-ttu-id="61c46-202">Примеры</span><span class="sxs-lookup"><span data-stu-id="61c46-202">Examples:</span></span>

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

<span data-ttu-id="61c46-203">Параметры передаются в двоичный файл Windows без изменений.</span><span class="sxs-lookup"><span data-stu-id="61c46-203">Parameters are passed to the Windows binary unmodified.</span></span>  

<span data-ttu-id="61c46-204">Например, следующие команды откроют `C:\temp\foo.txt` в `notepad.exe`.</span><span class="sxs-lookup"><span data-stu-id="61c46-204">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="61c46-205">Изменение файлов, расположенных в VolFs (файлы не в `/mnt/<x>`), приложением Windows не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="61c46-205">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application is not supported.</span></span>  <span data-ttu-id="61c46-206">По умолчанию WSL пытается сохранить рабочий каталог двоичного файла Windows в качестве текущего каталога WSL, но если рабочий каталог находится в VolFs, то WSL вернется к каталогу создания экземпляра.</span><span class="sxs-lookup"><span data-stu-id="61c46-206">By default, WSL attempts to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="61c46-207">Например, `bash.exe` изначально запускается из `C:\temp`, а текущим каталогом WSL становится корневая папка пользователя.</span><span class="sxs-lookup"><span data-stu-id="61c46-207">As an example; `bash.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="61c46-208">При вызове `notepad.exe` из корневого каталога пользователя WSL автоматически возвращается к `C:\temp` в качестве рабочего каталога Notepad.exe.</span><span class="sxs-lookup"><span data-stu-id="61c46-208">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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
