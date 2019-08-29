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
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a><span data-ttu-id="82802-103">Подсистема Windows для взаимодействия Linux с Windows</span><span class="sxs-lookup"><span data-stu-id="82802-103">Windows Subsystem for Linux interoperability with Windows</span></span>

> <span data-ttu-id="82802-104">**Обновлены обновления для создателей попадают.**</span><span class="sxs-lookup"><span data-stu-id="82802-104">**Updated for Fall Creators Update.**</span></span>  
<span data-ttu-id="82802-105">Если вы используете авторские обновления или годовщины, перейдите к разделу [Создатели/годовщина обновления](interop.md#creators-update-and-anniversary-update).</span><span class="sxs-lookup"><span data-stu-id="82802-105">If you're running Creators Update or Anniversary Update, jump to the [Creators/Anniversary Update section](interop.md#creators-update-and-anniversary-update).</span></span>

<span data-ttu-id="82802-106">Подсистема Windows для Linux (WSL) постоянно улучшает интеграцию между Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="82802-106">The Windows Subsystem for Linux (WSL) is continuously improving integration between Windows and Linux.</span></span>  <span data-ttu-id="82802-107">Можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="82802-107">You can:</span></span>

1. <span data-ttu-id="82802-108">Вызов двоичных файлов Windows из консоли Linux.</span><span class="sxs-lookup"><span data-stu-id="82802-108">Invoke Windows binaries from the Linux console.</span></span>
1. <span data-ttu-id="82802-109">Вызов двоичных файлов Linux из консоли Windows.</span><span class="sxs-lookup"><span data-stu-id="82802-109">Invoke Linux binaries from a Windows console.</span></span>
1. <span data-ttu-id="82802-110">**Программа предварительной оценки Windows создает 17063 +** Совместное использование переменных среды между Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="82802-110">**Windows Insiders Builds 17063+** Share environment variables between Linux and Windows.</span></span>

<span data-ttu-id="82802-111">Это обеспечивает эффективное взаимодействие между Windows и WSL.</span><span class="sxs-lookup"><span data-stu-id="82802-111">This delivers a seamless experience between Windows and WSL.</span></span>  <span data-ttu-id="82802-112">Технические сведения содержатся в [блоге WSL](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span><span class="sxs-lookup"><span data-stu-id="82802-112">Technical details are on the [WSL blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span></span>

## <a name="run-linux-tools-from-a-windows-command-line"></a><span data-ttu-id="82802-113">Запуск средств Linux из командной строки Windows</span><span class="sxs-lookup"><span data-stu-id="82802-113">Run Linux tools from a Windows command line</span></span>

<span data-ttu-id="82802-114">Запускайте двоичные файлы Linux из командной строки Windows (CMD или PowerShell `wsl.exe <command>`) с помощью команды.</span><span class="sxs-lookup"><span data-stu-id="82802-114">Run Linux binaries from the Windows Command Prompt (CMD or PowerShell) using `wsl.exe <command>`.</span></span>

<span data-ttu-id="82802-115">Двоичные файлы, которые вызываются таким образом:</span><span class="sxs-lookup"><span data-stu-id="82802-115">Binaries invoked in this way:</span></span>

1. <span data-ttu-id="82802-116">Используйте тот же рабочий каталог, что и для текущего ИНТЕРПРЕТАТОРа команд или командной строки PowerShell.</span><span class="sxs-lookup"><span data-stu-id="82802-116">Use the same working directory as the current CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="82802-117">Выполните команду от имени пользователя WSL по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="82802-117">Run as the WSL default user.</span></span>
1. <span data-ttu-id="82802-118">Имеют те же права администратора Windows, что и вызывающий процесс и терминал.</span><span class="sxs-lookup"><span data-stu-id="82802-118">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="82802-119">Пример:</span><span class="sxs-lookup"><span data-stu-id="82802-119">For example:</span></span>

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

<span data-ttu-id="82802-120">Следующая `wsl.exe` команда Linux обрабатывается как любая команда, выполняемая в WSL.</span><span class="sxs-lookup"><span data-stu-id="82802-120">The Linux command following `wsl.exe` is handled like any command run in WSL.</span></span>  <span data-ttu-id="82802-121">Действия sudo, трубопроводов и перенаправления файлов.</span><span class="sxs-lookup"><span data-stu-id="82802-121">Things such as sudo, piping, and file redirection work.</span></span>

<span data-ttu-id="82802-122">Пример использования sudo:</span><span class="sxs-lookup"><span data-stu-id="82802-122">Example using sudo:</span></span>

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

<span data-ttu-id="82802-123">Примеры смешивания команд WSL и Windows:</span><span class="sxs-lookup"><span data-stu-id="82802-123">Examples mixing WSL and Windows commands:</span></span>

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

<span data-ttu-id="82802-124">Команды, передаваемые `wsl.exe` в, перенаправляются в процесс WSL без изменения.</span><span class="sxs-lookup"><span data-stu-id="82802-124">The commands passed into `wsl.exe` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="82802-125">Пути к файлам должны быть указаны в формате WSL.</span><span class="sxs-lookup"><span data-stu-id="82802-125">File paths must be specified in the WSL format.</span></span>

<span data-ttu-id="82802-126">Пример с путями:</span><span class="sxs-lookup"><span data-stu-id="82802-126">Example with paths:</span></span>

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a><span data-ttu-id="82802-127">Запуск инструментов Windows из WSL</span><span class="sxs-lookup"><span data-stu-id="82802-127">Run Windows tools from WSL</span></span>

<span data-ttu-id="82802-128">WSL может вызывать двоичные файлы Windows непосредственно из командной строки WSL `[binary name].exe`с помощью.</span><span class="sxs-lookup"><span data-stu-id="82802-128">WSL can invoke Windows binaries directly from the WSL command line using `[binary name].exe`.</span></span>  <span data-ttu-id="82802-129">Например, `notepad.exe`.</span><span class="sxs-lookup"><span data-stu-id="82802-129">For example, `notepad.exe`.</span></span>  <span data-ttu-id="82802-130">Чтобы упростить запуск исполняемых файлов Windows, путь Windows включается в обновление для создателей Linux `$PATH` .</span><span class="sxs-lookup"><span data-stu-id="82802-130">To make Windows executables easier to run, Windows path is included in the Linux `$PATH` in Fall Creators Update.</span></span>

<span data-ttu-id="82802-131">Приложения выполняются таким образом и имеют следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="82802-131">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="82802-132">Храните рабочий каталог в качестве командной строки WSL (наиболее частые исключения описаны ниже).</span><span class="sxs-lookup"><span data-stu-id="82802-132">Retain the working directory as the WSL command prompt (for the most part -- exceptions are explained below).</span></span>
1. <span data-ttu-id="82802-133">Имеют те же права разрешений, что и процесс WSL.</span><span class="sxs-lookup"><span data-stu-id="82802-133">Have the same permission rights as the WSL process.</span></span>
1. <span data-ttu-id="82802-134">Запуск от имени активного пользователя Windows.</span><span class="sxs-lookup"><span data-stu-id="82802-134">Run as the active Windows user.</span></span>
1. <span data-ttu-id="82802-135">Отображаются в диспетчере задач Windows так, как если бы они выполнялись непосредственно из командной строки.</span><span class="sxs-lookup"><span data-stu-id="82802-135">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="82802-136">Пример.</span><span class="sxs-lookup"><span data-stu-id="82802-136">Example:</span></span>

``` BASH
$ notepad.exe
```

<span data-ttu-id="82802-137">Исполняемые файлы Windows, выполняемые в WSL, обрабатываются аналогично собственным исполняемым файлам Linux — конвейеру, перенаправлениям и даже фоновому режиму работы должным образом.</span><span class="sxs-lookup"><span data-stu-id="82802-137">Windows executables run in WSL are handled similarly to native Linux executables -- piping, redirects, and even backgrounding work as expected.</span></span>

<span data-ttu-id="82802-138">Примеры использования каналов:</span><span class="sxs-lookup"><span data-stu-id="82802-138">Examples using pipes:</span></span>

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

<span data-ttu-id="82802-139">Пример использования смешанных команд Windows и WSL:</span><span class="sxs-lookup"><span data-stu-id="82802-139">Example using mixed Windows and WSL commands:</span></span>

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

<span data-ttu-id="82802-140">Двоичные файлы Windows должны включать расширение файла, сопоставлять регистр файлов и быть исполняемыми.</span><span class="sxs-lookup"><span data-stu-id="82802-140">Windows binaries must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="82802-141">Не исполняемые файлы, включая скрипты пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="82802-141">Non-executables including batch scripts.</span></span>  <span data-ttu-id="82802-142">Машинные команды cmd `dir` , например, можно `cmd.exe /C` выполнять с помощью команды.</span><span class="sxs-lookup"><span data-stu-id="82802-142">CMD native commands like `dir` can be run with `cmd.exe /C` command.</span></span>

<span data-ttu-id="82802-143">Примеры:</span><span class="sxs-lookup"><span data-stu-id="82802-143">Examples:</span></span>

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

<span data-ttu-id="82802-144">Параметры передаются в двоичный файл Windows без изменений.</span><span class="sxs-lookup"><span data-stu-id="82802-144">Parameters are passed to the Windows binary unmodified.</span></span>

<span data-ttu-id="82802-145">Например, следующие команды будут открыты `C:\temp\foo.txt` в: `notepad.exe`</span><span class="sxs-lookup"><span data-stu-id="82802-145">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="82802-146">Изменение файлов, расположенных в волфс (файлы, `/mnt/<x>`не включенные в файл) с помощью приложения Windows в WSL, не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="82802-146">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application in WSL is not supported.</span></span>

<span data-ttu-id="82802-147">По умолчанию WSL пытается удержать рабочий каталог двоичного файла Windows в качестве текущего каталога WSL, но если рабочий каталог находится в Волфс, он вернется к каталогу создания экземпляра.</span><span class="sxs-lookup"><span data-stu-id="82802-147">By default, WSL tries to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="82802-148">Пример; изначально запускается из `C:\temp` , а текущий каталог WSL изменяется на домашнюю страницу пользователя. `wsl.exe`</span><span class="sxs-lookup"><span data-stu-id="82802-148">As an example; `wsl.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="82802-149">Когда `notepad.exe` вызывается из домашнего каталога пользователя, WSL автоматически возвращается в `C:\temp` качестве рабочего каталога Notepad. exe:</span><span class="sxs-lookup"><span data-stu-id="82802-149">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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

## <a name="share-environment-variables-between-windows-and-wsl"></a><span data-ttu-id="82802-150">Совместное использование переменных среды между Windows и WSL</span><span class="sxs-lookup"><span data-stu-id="82802-150">Share environment variables between Windows and WSL</span></span>

> <span data-ttu-id="82802-151">Доступно в сборке Windows Insider 17063 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="82802-151">Available in Windows Insider builds 17063 and later.</span></span>

<span data-ttu-id="82802-152">До 17063 только переменная среды Windows, к которой имеет доступ WSL, `PATH` была доступна (так что можно было запускать исполняемые файлы Win32 из раздела WSL).</span><span class="sxs-lookup"><span data-stu-id="82802-152">Prior to 17063, only Windows environment variable that WSL could access was `PATH` (so you could launch Win32 executables from under WSL).</span></span>

<span data-ttu-id="82802-153">Начиная с 17063, WSL и общей папки `WSLENV`Windows, можно создать специальную переменную среды, созданную для моста Windows и Linux дистрибутивов, запущенные на WSL.</span><span class="sxs-lookup"><span data-stu-id="82802-153">Starting in 17063, WSL and Windows share `WSLENV`, a special environment variable created to bridge Windows and Linux distros running on WSL.</span></span>

<span data-ttu-id="82802-154">`WSLENV`Свойства:</span><span class="sxs-lookup"><span data-stu-id="82802-154">Properties of `WSLENV`:</span></span>

* <span data-ttu-id="82802-155">Он является общим; он существует в средах Windows и WSL.</span><span class="sxs-lookup"><span data-stu-id="82802-155">It is shared; it exists in both Windows and WSL environments.</span></span>
* <span data-ttu-id="82802-156">Это список переменных среды, которые совместно используют Windows и WSL.</span><span class="sxs-lookup"><span data-stu-id="82802-156">It is a list of environment variables to share between Windows and WSL.</span></span>
* <span data-ttu-id="82802-157">Он может форматировать переменные среды для корректной работы в Windows и WSL.</span><span class="sxs-lookup"><span data-stu-id="82802-157">It can format environment variables to work well in Windows and WSL.</span></span>

<span data-ttu-id="82802-158">В `WSLENV` предусмотрено четыре флага, влияющих на способ перевода переменной среды.</span><span class="sxs-lookup"><span data-stu-id="82802-158">There are four flags available in `WSLENV` to influence how that environment variable is translated.</span></span>

<span data-ttu-id="82802-159">`WSLENV`Метки</span><span class="sxs-lookup"><span data-stu-id="82802-159">`WSLENV` flags:</span></span>

* <span data-ttu-id="82802-160">`/p`— переводит путь между путями в стиле WSL/Linux и путями Win32.</span><span class="sxs-lookup"><span data-stu-id="82802-160">`/p` - translates the path between WSL/Linux style paths and Win32 paths.</span></span>
* <span data-ttu-id="82802-161">`/l`— Указывает, что переменная среды представляет собой список путей.</span><span class="sxs-lookup"><span data-stu-id="82802-161">`/l` - indicates the environment variable is a list of paths.</span></span>
* <span data-ttu-id="82802-162">`/u`— Указывает, что эта переменная среды должна быть включена только при запуске WSL из Win32.</span><span class="sxs-lookup"><span data-stu-id="82802-162">`/u` - indicates that this environment variable should only be included when running WSL from Win32.</span></span>
* <span data-ttu-id="82802-163">`/w`— Указывает, что эту переменную среды следует включать только при запуске Win32 из WSL.</span><span class="sxs-lookup"><span data-stu-id="82802-163">`/w` - indicates that this environment variable should only be included when running Win32 from WSL.</span></span>

<span data-ttu-id="82802-164">При необходимости флаги можно комбинировать.</span><span class="sxs-lookup"><span data-stu-id="82802-164">Flags can be combined as needed.</span></span>

## <a name="disable-interop"></a><span data-ttu-id="82802-165">Отключить взаимодействие</span><span class="sxs-lookup"><span data-stu-id="82802-165">Disable Interop</span></span>

<span data-ttu-id="82802-166">Пользователи могут отключить возможность запуска двоичных файлов Windows для одного сеанса WSL, выполнив следующую команду в качестве корневого:</span><span class="sxs-lookup"><span data-stu-id="82802-166">Users may disable the ability to run Windows binaries for a single WSL session by running the following command as root:</span></span>

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="82802-167">Чтобы повторно включить двоичные файлы Windows, закройте все сеансы WSL и перезапустите bash. exe или выполните следующую команду в качестве корневого:</span><span class="sxs-lookup"><span data-stu-id="82802-167">To reenable Windows binaries either exit all WSL sessions and re-run bash.exe or run the following command as root:</span></span>

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="82802-168">Отключение взаимодействия не будет сохраняться между сеансами WSL--взаимодействие будет включено повторно при запуске нового сеанса.</span><span class="sxs-lookup"><span data-stu-id="82802-168">Disabling interop will not persist between WSL sessions -- interop will be enabled again when a new session is launched.</span></span>

## <a name="creators-update-and-anniversary-update"></a><span data-ttu-id="82802-169">Авторские обновления и годовщины</span><span class="sxs-lookup"><span data-stu-id="82802-169">Creators Update and Anniversary Update</span></span>

<span data-ttu-id="82802-170">Несмотря на то, что обновление с предварительной приначальным взаимодействием в области взаимодействия аналогично более недавнему взаимодействию, существует несколько основных отличий.</span><span class="sxs-lookup"><span data-stu-id="82802-170">While the interop experience pre-Fall Creators Update is similar to more recent interop experiences, there are a handful of major differences.</span></span>

<span data-ttu-id="82802-171">Итоги:</span><span class="sxs-lookup"><span data-stu-id="82802-171">To summarize:</span></span>

* <span data-ttu-id="82802-172">`bash.exe`является нерекомендуемым и заменяется на `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="82802-172">`bash.exe` has been deprecated and replaced with `wsl.exe`.</span></span>
* <span data-ttu-id="82802-173">`-c`параметр для выполнения одной команды не требуется с `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="82802-173">`-c` option for running a single command isn't needed with `wsl.exe`.</span></span>
* <span data-ttu-id="82802-174">Путь Windows включен в WSL`$PATH`</span><span class="sxs-lookup"><span data-stu-id="82802-174">Windows path is included in the WSL `$PATH`</span></span>

<span data-ttu-id="82802-175">Процесс отключения взаимодействия не изменяется.</span><span class="sxs-lookup"><span data-stu-id="82802-175">The process for disabling interop is unchanged.</span></span>

### <a name="invoking-wsl-from-the-windows-command-line"></a><span data-ttu-id="82802-176">Вызов WSL из командной строки Windows</span><span class="sxs-lookup"><span data-stu-id="82802-176">Invoking WSL from the Windows Command Line</span></span>

<span data-ttu-id="82802-177">Двоичные файлы Linux можно вызывать из командной строки Windows или из PowerShell.</span><span class="sxs-lookup"><span data-stu-id="82802-177">Linux binaries can be invoked from the Windows Command Prompt or from PowerShell.</span></span>  <span data-ttu-id="82802-178">Двоичные файлы, вызываемые таким способом, имеют следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="82802-178">Binaries invoked in this way have the following properties:</span></span>

1. <span data-ttu-id="82802-179">Используйте тот же рабочий каталог, что и в командной строке CMD или PowerShell.</span><span class="sxs-lookup"><span data-stu-id="82802-179">Use the same working directory as the CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="82802-180">Выполните команду от имени пользователя WSL по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="82802-180">Run as the WSL default user.</span></span>
1. <span data-ttu-id="82802-181">Имеют те же права администратора Windows, что и вызывающий процесс и терминал.</span><span class="sxs-lookup"><span data-stu-id="82802-181">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="82802-182">Пример.</span><span class="sxs-lookup"><span data-stu-id="82802-182">Example:</span></span>

```console
C:\temp> bash -c "ls -la"
```

<span data-ttu-id="82802-183">Команды Linux, вызываемые таким образом, обрабатываются как любые другие приложения Windows.</span><span class="sxs-lookup"><span data-stu-id="82802-183">Linux commands called in this way are handled like any other Windows application.</span></span>  <span data-ttu-id="82802-184">Такие вещи, как входные данные, конвейеры и перенаправление файлов, работают должным образом.</span><span class="sxs-lookup"><span data-stu-id="82802-184">Things such as input, piping, and file redirection work as expected.</span></span>

<span data-ttu-id="82802-185">Примеры:</span><span class="sxs-lookup"><span data-stu-id="82802-185">Examples:</span></span>

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

<span data-ttu-id="82802-186">Команды WSL, передаваемые `bash -c` в, пересылаются в процесс WSL без изменения.</span><span class="sxs-lookup"><span data-stu-id="82802-186">The WSL commands passed into `bash -c` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="82802-187">Пути к файлам должны быть указаны в формате WSL, и необходимо соблюдать осторожность для экранирования соответствующих символов.</span><span class="sxs-lookup"><span data-stu-id="82802-187">File paths must be specified in the WSL format and care must be taken to escape relevant characters.</span></span> <span data-ttu-id="82802-188">Пример.</span><span class="sxs-lookup"><span data-stu-id="82802-188">Example:</span></span>

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a><span data-ttu-id="82802-189">Вызов двоичных файлов Windows из WSL</span><span class="sxs-lookup"><span data-stu-id="82802-189">Invoking Windows binaries from WSL</span></span>

<span data-ttu-id="82802-190">Подсистема Windows для Linux может вызывать двоичные файлы Windows непосредственно из командной строки WSL.</span><span class="sxs-lookup"><span data-stu-id="82802-190">The Windows Subsystem for Linux can invoke Windows binaries directly from the WSL command line.</span></span>  <span data-ttu-id="82802-191">Приложения выполняются таким образом и имеют следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="82802-191">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="82802-192">Храните рабочий каталог в командной строке WSL, за исключением сценария, описанного ниже.</span><span class="sxs-lookup"><span data-stu-id="82802-192">Retain the working directory as the WSL command prompt except in the scenario explained below.</span></span>
1. <span data-ttu-id="82802-193">Имеют те же права разрешений, что `bash.exe` и процесс.</span><span class="sxs-lookup"><span data-stu-id="82802-193">Have the same permission rights as the `bash.exe` process.</span></span> 
1. <span data-ttu-id="82802-194">Запуск от имени активного пользователя Windows.</span><span class="sxs-lookup"><span data-stu-id="82802-194">Run as the active Windows user.</span></span>
1. <span data-ttu-id="82802-195">Отображаются в диспетчере задач Windows так, как если бы они выполнялись непосредственно из командной строки.</span><span class="sxs-lookup"><span data-stu-id="82802-195">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="82802-196">Пример.</span><span class="sxs-lookup"><span data-stu-id="82802-196">Example:</span></span>

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

<span data-ttu-id="82802-197">В WSL эти исполняемые файлы обрабатываются аналогично собственным исполняемым файлам Linux.</span><span class="sxs-lookup"><span data-stu-id="82802-197">In WSL, these executables are handled similar to native Linux executables.</span></span>  <span data-ttu-id="82802-198">Это означает, что добавление каталогов в путь Linux и передача между командами выполняется должным образом.</span><span class="sxs-lookup"><span data-stu-id="82802-198">This means adding directories to the Linux path and piping between commands works as expected.</span></span>  <span data-ttu-id="82802-199">Примеры:</span><span class="sxs-lookup"><span data-stu-id="82802-199">Examples:</span></span>

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

<span data-ttu-id="82802-200">Двоичный файл Windows должен включать расширение файла, соответствовать регистру файла и быть исполняемым.</span><span class="sxs-lookup"><span data-stu-id="82802-200">The Windows binary must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="82802-201">Кроме исполняемых файлов, включая скрипты пакетной `dir` службы и команду, `/mnt/c/Windows/System32/cmd.exe /C` можно выполнить команду с помощью команды.</span><span class="sxs-lookup"><span data-stu-id="82802-201">Non-executables including batch scripts and command like `dir` can be run with `/mnt/c/Windows/System32/cmd.exe /C` command.</span></span>

<span data-ttu-id="82802-202">Примеры:</span><span class="sxs-lookup"><span data-stu-id="82802-202">Examples:</span></span>

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

<span data-ttu-id="82802-203">Параметры передаются в двоичный файл Windows без изменений.</span><span class="sxs-lookup"><span data-stu-id="82802-203">Parameters are passed to the Windows binary unmodified.</span></span>  

<span data-ttu-id="82802-204">Например, следующие команды будут открыты `C:\temp\foo.txt` в: `notepad.exe`</span><span class="sxs-lookup"><span data-stu-id="82802-204">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="82802-205">Изменение файлов, расположенных в волфс (файлы, `/mnt/<x>`отсутствующие в папке), с приложением Windows не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="82802-205">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application is not supported.</span></span>  <span data-ttu-id="82802-206">По умолчанию WSL пытается использовать рабочий каталог двоичного файла Windows в качестве текущего каталога WSL, но если рабочий каталог находится в Волфс, то он вернется к каталогу создания экземпляра.</span><span class="sxs-lookup"><span data-stu-id="82802-206">By default, WSL attempts to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="82802-207">Пример; изначально запускается из `C:\temp` , а текущий каталог WSL изменяется на домашнюю страницу пользователя. `bash.exe`</span><span class="sxs-lookup"><span data-stu-id="82802-207">As an example; `bash.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="82802-208">Когда `notepad.exe` вызывается из домашнего каталога пользователя, WSL автоматически возвращается в `C:\temp` качестве рабочего каталога Notepad. exe:</span><span class="sxs-lookup"><span data-stu-id="82802-208">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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
