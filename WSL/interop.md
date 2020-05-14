---
title: Взаимодействие Windows с Linux
description: Описывается взаимодействие Windows с дистрибутивами Linux, работающими в подсистеме Windows для Linux.
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: b1c7a64a86cf088159d1abee3b341328151428f6
ms.sourcegitcommit: 1b6191351bbf9e95f3c28fc67abe4bf1bcfd3336
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/13/2020
ms.locfileid: "83270848"
---
# <a name="windows-interoperability-with-linux"></a><span data-ttu-id="c54d8-103">Взаимодействие Windows с Linux</span><span class="sxs-lookup"><span data-stu-id="c54d8-103">Windows interoperability with Linux</span></span>

<span data-ttu-id="c54d8-104">В подсистеме Windows для Linux (WSL) постоянно улучшается интеграция между Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="c54d8-104">The Windows Subsystem for Linux (WSL) is continuously improving integration between Windows and Linux.</span></span>  <span data-ttu-id="c54d8-105">Можно сделать следующее.</span><span class="sxs-lookup"><span data-stu-id="c54d8-105">You can:</span></span>

* <span data-ttu-id="c54d8-106">Запустить средства Windows (например, notepad.exe) из командной строки Linux (например, Ubuntu).</span><span class="sxs-lookup"><span data-stu-id="c54d8-106">Run Windows tools (ie. notepad.exe) from a Linux command line (ie. Ubuntu).</span></span>
* <span data-ttu-id="c54d8-107">Запустить средства Linux (например, grep) из командной строки Windows (например, PowerShell).</span><span class="sxs-lookup"><span data-stu-id="c54d8-107">Run Linux tools (ie. grep) from a Windows command line (ie. PowerShell).</span></span>
* <span data-ttu-id="c54d8-108">Совместное использование переменных среды между Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="c54d8-108">Share environment variables between Linux and Windows.</span></span> <span data-ttu-id="c54d8-109">(сборка 17063+)</span><span class="sxs-lookup"><span data-stu-id="c54d8-109">(Build 17063+)</span></span>

> [!NOTE]
> <span data-ttu-id="c54d8-110">Если вы используете Creators Update (октябрь 2017 г., сборка 16299) или Юбилейное обновление (август 2016 г., сборка 14393), перейдите к [более ранним версиям Windows 10](#earlier-versions-of-windows-10).</span><span class="sxs-lookup"><span data-stu-id="c54d8-110">If you're running Creators Update (Oct 2017, Build 16299) or Anniversary Update (Aug 2016, Build 14393), jump to the [Earlier versions of Windows 10](#earlier-versions-of-windows-10).</span></span>

## <a name="run-linux-tools-from-a-windows-command-line"></a><span data-ttu-id="c54d8-111">Запуск инструментов Linux из командной строки Windows</span><span class="sxs-lookup"><span data-stu-id="c54d8-111">Run Linux tools from a Windows command line</span></span>

<span data-ttu-id="c54d8-112">Запускайте двоичные файлы Linux из командной строки Windows (CMD или PowerShell), используя `wsl <command>` (или `wsl.exe <command>`).</span><span class="sxs-lookup"><span data-stu-id="c54d8-112">Run Linux binaries from the Windows Command Prompt (CMD) or PowerShell using `wsl <command>` (or `wsl.exe <command>`).</span></span>

<span data-ttu-id="c54d8-113">Например:</span><span class="sxs-lookup"><span data-stu-id="c54d8-113">For example:</span></span>

```powershell
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

<span data-ttu-id="c54d8-114">Двоичные файлы вызываются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="c54d8-114">Binaries invoked in this way:</span></span>

* <span data-ttu-id="c54d8-115">Используется тот же рабочий каталог, что и для текущей командной строки или сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c54d8-115">Use the same working directory as the current CMD or PowerShell prompt.</span></span>
* <span data-ttu-id="c54d8-116">Файл выполняется от имени пользователя WSL по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c54d8-116">Run as the WSL default user.</span></span>
* <span data-ttu-id="c54d8-117">Требуются те же права администратора Windows, что и у вызывающего процесса и терминала.</span><span class="sxs-lookup"><span data-stu-id="c54d8-117">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="c54d8-118">Команда Linux после `wsl` (или `wsl.exe`) обрабатывается как любая команда, выполняемая в WSL.</span><span class="sxs-lookup"><span data-stu-id="c54d8-118">The Linux command following `wsl` (or `wsl.exe`) is handled like any command run in WSL.</span></span>  <span data-ttu-id="c54d8-119">Можно выполнять sudo, конвейерную передачу и перенаправление файлов.</span><span class="sxs-lookup"><span data-stu-id="c54d8-119">Things such as sudo, piping, and file redirection work.</span></span>

<span data-ttu-id="c54d8-120">Пример использования sudo для обновления дистрибутива Linux по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="c54d8-120">Example using sudo to update your default Linux distribution:</span></span>

```powershell
C:\temp> wsl sudo apt-get update
```

<span data-ttu-id="c54d8-121">Имя пользователя дистрибутива Linux по умолчанию будет указано после выполнения этой команды, и вам будет предложено указать пароль.</span><span class="sxs-lookup"><span data-stu-id="c54d8-121">Your default Linux distribution user name will be listed after running this command and you will be asked for your password.</span></span> <span data-ttu-id="c54d8-122">После правильного ввода пароля дистрибутив скачает обновления.</span><span class="sxs-lookup"><span data-stu-id="c54d8-122">After entering your password correctly, your distribution will download updates.</span></span>

## <a name="mixing-linux-and-windows-commands"></a><span data-ttu-id="c54d8-123">Смешивание команд Linux и Windows</span><span class="sxs-lookup"><span data-stu-id="c54d8-123">Mixing Linux and Windows commands</span></span>

<span data-ttu-id="c54d8-124">Ниже приведено несколько примеров смешиваний команд Linux и Windows с помощью PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c54d8-124">Here are a few examples of mixing Linux and Windows commands using PowerShell.</span></span>

<span data-ttu-id="c54d8-125">Чтобы выполнить команду Linux `ls -la` для вывода списка файлов и команду PowerShell `findstr` для фильтрации результатов слов, содержащих git, объедините команды:</span><span class="sxs-lookup"><span data-stu-id="c54d8-125">To use the Linux command `ls -la` to list files and the PowerShell command `findstr` to filter the results for words containing "git", combine the commands:</span></span>

```powershell
wsl ls -la | findstr "git"
```

<span data-ttu-id="c54d8-126">Чтобы выполнить команду PowerShell `dir` для вывода списка файлов и команду Linux `grep` для фильтрации результатов слов, содержащих git, объедините команды:</span><span class="sxs-lookup"><span data-stu-id="c54d8-126">To use the PowerShell command `dir` to list files and the Linux command `grep` to filter the results for words containing "git", combine the commands:</span></span>

```powershell
C:\temp> dir | wsl grep git
```

<span data-ttu-id="c54d8-127">Чтобы использовать команду Linux `ls -la` для вывода списка файлов и команду PowerShell `> out.txt` для вывода этого списка в текстовый файл с именем out.txt, объедините команды:</span><span class="sxs-lookup"><span data-stu-id="c54d8-127">To use the Linux command `ls -la` to list files and the PowerShell command `> out.txt` to print that list to a text file named "out.txt", combine the commands:</span></span>

```powershell
C:\temp> wsl ls -la > out.txt
```

<span data-ttu-id="c54d8-128">Команды, передаваемые в `wsl.exe`, перенаправляются в процесс WSL без изменения.</span><span class="sxs-lookup"><span data-stu-id="c54d8-128">The commands passed into `wsl.exe` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="c54d8-129">Пути к файлам должны быть указаны в формате WSL.</span><span class="sxs-lookup"><span data-stu-id="c54d8-129">File paths must be specified in the WSL format.</span></span>

<span data-ttu-id="c54d8-130">Чтобы выполнить команду Linux `ls -la` для вывода списка файлов в пути файловой системы Linux `/proc/cpuinfo` с помощью PowerShell, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="c54d8-130">To use the Linux command `ls -la` to list files in the `/proc/cpuinfo` Linux file system path, using PowerShell:</span></span>

```powershell
C:\temp> wsl ls -la /proc/cpuinfo
```

<span data-ttu-id="c54d8-131">Чтобы выполнить команду Linux `ls -la` для вывода списка файлов в пути файловой системы Windows `C:\Program Files` с помощью PowerShell, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="c54d8-131">To use the Linux command `ls -la` to list files in the `C:\Program Files` Windows file system path, using PowerShell:</span></span>

```powershell
C:\temp> wsl ls -la "/mnt/c/Program Files"
```

## <a name="run-windows-tools-from-linux"></a><span data-ttu-id="c54d8-132">Запуск инструментов Windows из Linux</span><span class="sxs-lookup"><span data-stu-id="c54d8-132">Run Windows tools from Linux</span></span>

<span data-ttu-id="c54d8-133">WSL может запускать средства Windows непосредственно из командной строки WSL с помощью `[tool-name].exe`.</span><span class="sxs-lookup"><span data-stu-id="c54d8-133">WSL can run Windows tools directly from the WSL command line using `[tool-name].exe`.</span></span>  <span data-ttu-id="c54d8-134">Например, `notepad.exe`.</span><span class="sxs-lookup"><span data-stu-id="c54d8-134">For example, `notepad.exe`.</span></span>

<!-- Craig - could you help add a section with an example here to explain this scenario: "To access your Linux files using a Windows tool, use `\\wsl$\<distroName>\'` as the file path." Currently it I can just enter `notepad.exe foo.txt` and it seems to work fine, so explaining a situation where the file path is needed would be helpful. -->

<span data-ttu-id="c54d8-135">Приложения, выполняемые таким образом, обладают следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="c54d8-135">Applications run this way have the following properties:</span></span>

* <span data-ttu-id="c54d8-136">Рабочим каталогом остается каталог командной строки WSL (в большинстве случаев; исключения описаны ниже).</span><span class="sxs-lookup"><span data-stu-id="c54d8-136">Retain the working directory as the WSL command prompt (for the most part -- exceptions are explained below).</span></span>
* <span data-ttu-id="c54d8-137">Они имеют те же разрешения, что и процесс WSL.</span><span class="sxs-lookup"><span data-stu-id="c54d8-137">Have the same permission rights as the WSL process.</span></span>
* <span data-ttu-id="c54d8-138">Они выполняются от имени активного пользователя Windows.</span><span class="sxs-lookup"><span data-stu-id="c54d8-138">Run as the active Windows user.</span></span>
* <span data-ttu-id="c54d8-139">Они отображаются в диспетчере задач Windows так, как если бы они выполнялись непосредственно из командной строки.</span><span class="sxs-lookup"><span data-stu-id="c54d8-139">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="c54d8-140">Исполняемые файлы Windows, выполняемые в WSL, обрабатываются аналогично собственным исполняемым файлам Linux — конвейерной передаче, перенаправлению и даже фоновому режиму работы.</span><span class="sxs-lookup"><span data-stu-id="c54d8-140">Windows executables run in WSL are handled similarly to native Linux executables -- piping, redirects, and even backgrounding work as expected.</span></span>

<span data-ttu-id="c54d8-141">Чтобы запустить средство Windows `ipconfig.exe`, использовать средство Linux `grep` для фильтрации результатов IPv4, а также средство Linux `cut` для удаления полей столбцов из дистрибутива Linux (например, Ubuntu), введите:</span><span class="sxs-lookup"><span data-stu-id="c54d8-141">To run the Windows tool `ipconfig.exe`, use the Linux tool `grep` to filter the "IPv4" results, and use the Linux tool `cut` to remove the column fields, from a Linux distribution (for example, Ubuntu) enter:</span></span>

```bash
ipconfig.exe | grep IPv4 | cut -d: -f2
```

<span data-ttu-id="c54d8-142">Давайте рассмотрим пример сочетания команд Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="c54d8-142">Let's try an example mixing Windows and Linux commands.</span></span> <span data-ttu-id="c54d8-143">Откройте дистрибутив Linux (например, Ubuntu) и создайте текстовый файл: `touch foo.txt`.</span><span class="sxs-lookup"><span data-stu-id="c54d8-143">Open your Linux distribution (ie. Ubuntu) and create a text file: `touch foo.txt`.</span></span> <span data-ttu-id="c54d8-144">Теперь используйте команду Linux `ls -la`, чтобы отобразить список файлов прямого доступа и сведения об их создании, а также средство Windows PowerShell `findstr.exe`, чтобы отфильтровать результаты и отобразить только файл `foo.txt`:</span><span class="sxs-lookup"><span data-stu-id="c54d8-144">Now use the Linux command `ls -la` to list the direct files and their creation details, plus the Windows PowerShell tool `findstr.exe` to filter the results so only your `foo.txt` file shows in the results:</span></span>

```bash
ls -la | findstr.exe foo.txt
```

<span data-ttu-id="c54d8-145">Средства Windows должны иметь расширение файла, его регистр символов должен совпадать с регистром в имени файла и эти файлы должны быть исполняемыми.</span><span class="sxs-lookup"><span data-stu-id="c54d8-145">Windows tools must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="c54d8-146">Неисполняемые файлы, в том числе сценарии пакетного выполнения и</span><span class="sxs-lookup"><span data-stu-id="c54d8-146">Non-executables including batch scripts.</span></span>  <span data-ttu-id="c54d8-147">собственные команды командной строки, такие как `dir`, можно выполнять с помощью команды `cmd.exe /C`.</span><span class="sxs-lookup"><span data-stu-id="c54d8-147">CMD native commands like `dir` can be run with `cmd.exe /C` command.</span></span>

<span data-ttu-id="c54d8-148">Например, отобразите список содержимого каталога C:\ файловой системы Windows, введя:</span><span class="sxs-lookup"><span data-stu-id="c54d8-148">For example, list the contents of your Windows files system C:\ directory, by entering:</span></span>

```bash
cmd.exe /C dir
```

<span data-ttu-id="c54d8-149">Или выполните команду `ping`, чтобы отправить запрос проверки связи на веб-сайт microsoft.com:</span><span class="sxs-lookup"><span data-stu-id="c54d8-149">Or use the `ping` command to send an echo request to the microsoft.com website:</span></span>

```bash
ping.exe www.microsoft.com
```

<span data-ttu-id="c54d8-150">Параметры передаются в двоичный файл Windows без изменений.</span><span class="sxs-lookup"><span data-stu-id="c54d8-150">Parameters are passed to the Windows binary unmodified.</span></span> <span data-ttu-id="c54d8-151">Например, следующая команда откроет `C:\temp\foo.txt` в `notepad.exe`.</span><span class="sxs-lookup"><span data-stu-id="c54d8-151">As an example, the following command will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

```bash
notepad.exe "C:\temp\foo.txt"
```

<span data-ttu-id="c54d8-152">Этот способ также будет работать:</span><span class="sxs-lookup"><span data-stu-id="c54d8-152">This will also work:</span></span>

```bash
notepad.exe C:\\temp\\foo.txt
```

## <a name="share-environment-variables-between-windows-and-wsl"></a><span data-ttu-id="c54d8-153">Совместное использование переменных среды между Windows и WSL</span><span class="sxs-lookup"><span data-stu-id="c54d8-153">Share environment variables between Windows and WSL</span></span>

<span data-ttu-id="c54d8-154">Решение WSL и Windows совместно используют `WSLENV` — специальную переменную среды, созданную для взаимодействия Windows и дистрибутивов Linux, запущенных в WSL.</span><span class="sxs-lookup"><span data-stu-id="c54d8-154">WSL and Windows share a special environment variable, `WSLENV`, created to bridge Windows and Linux distributions running on WSL.</span></span>

<span data-ttu-id="c54d8-155">Свойства переменной `WSLENV`:</span><span class="sxs-lookup"><span data-stu-id="c54d8-155">Properties of `WSLENV` variable:</span></span>

* <span data-ttu-id="c54d8-156">она используется совместно и существует в средах Windows и WSL;</span><span class="sxs-lookup"><span data-stu-id="c54d8-156">It is shared; it exists in both Windows and WSL environments.</span></span>
* <span data-ttu-id="c54d8-157">это список переменных среды, которые совместно используют Windows и WSL;</span><span class="sxs-lookup"><span data-stu-id="c54d8-157">It is a list of environment variables to share between Windows and WSL.</span></span>
* <span data-ttu-id="c54d8-158">она позволяет форматировать список переменных среды для корректного использования в Windows и WSL.</span><span class="sxs-lookup"><span data-stu-id="c54d8-158">It can format environment variables to work well in Windows and WSL.</span></span>

> [!NOTE]
> <span data-ttu-id="c54d8-159">До выпуска сборки 17063 единственной переменной среды Windows,, к которой могла получить доступ WSL, была `PATH` (это позволяло запускать исполняемые файлы Win32 из WSL).</span><span class="sxs-lookup"><span data-stu-id="c54d8-159">Prior to 17063, only Windows environment variable that WSL could access was `PATH` (so you could launch Win32 executables from under WSL).</span></span> <span data-ttu-id="c54d8-160">Начиная со сборки 17063, `WSLENV` поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c54d8-160">Starting in 17063, `WSLENV` begins being supported.</span></span>

## <a name="wslenv-flags"></a><span data-ttu-id="c54d8-161">Флаги WSLENV</span><span class="sxs-lookup"><span data-stu-id="c54d8-161">WSLENV flags</span></span>

<span data-ttu-id="c54d8-162">В `WSLENV` доступны четыре флага, влияющие на способ преобразования переменной среды.</span><span class="sxs-lookup"><span data-stu-id="c54d8-162">There are four flags available in `WSLENV` to influence how the environment variable is translated.</span></span>

<span data-ttu-id="c54d8-163">Флаги `WSLENV`:</span><span class="sxs-lookup"><span data-stu-id="c54d8-163">`WSLENV` flags:</span></span>

* <span data-ttu-id="c54d8-164">`/p` преобразовывает пути WSL и Linux в пути Win32 и наоборот;</span><span class="sxs-lookup"><span data-stu-id="c54d8-164">`/p` - translates the path between WSL/Linux style paths and Win32 paths.</span></span>
* <span data-ttu-id="c54d8-165">`/l` указывает, что переменная среды представляет собой список путей;</span><span class="sxs-lookup"><span data-stu-id="c54d8-165">`/l` - indicates the environment variable is a list of paths.</span></span>
* <span data-ttu-id="c54d8-166">`/u` указывает, что эту переменную среды следует добавлять только при запуске WSL из Win32;</span><span class="sxs-lookup"><span data-stu-id="c54d8-166">`/u` - indicates that this environment variable should only be included when running WSL from Win32.</span></span>
* <span data-ttu-id="c54d8-167">`/w` указывает, что эту переменную среды следует добавлять только при запуске Win32 из WSL.</span><span class="sxs-lookup"><span data-stu-id="c54d8-167">`/w` - indicates that this environment variable should only be included when running Win32 from WSL.</span></span>

<span data-ttu-id="c54d8-168">При необходимости флаги можно комбинировать.</span><span class="sxs-lookup"><span data-stu-id="c54d8-168">Flags can be combined as needed.</span></span>

## <a name="disable-interoperability"></a><span data-ttu-id="c54d8-169">Отключение взаимодействия</span><span class="sxs-lookup"><span data-stu-id="c54d8-169">Disable interoperability</span></span>

<span data-ttu-id="c54d8-170">Пользователи могут отключить возможность запуска средств Windows для отдельного сеанса WSL, выполнив следующую команду в качестве привилегированного пользователя.</span><span class="sxs-lookup"><span data-stu-id="c54d8-170">Users may disable the ability to run Windows tools for a single WSL session by running the following command as root:</span></span>

```bash
echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="c54d8-171">Чтобы повторно включить возможность запуска двоичных файлов Windows, закройте все сеансы WSL и повторно запустите bash.exe или выполните следующую команду от имени привилегированного пользователя.</span><span class="sxs-lookup"><span data-stu-id="c54d8-171">To re-enable Windows binaries, exit all WSL sessions and re-run bash.exe or run the following command as root:</span></span>

```bash
echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="c54d8-172">Отключение взаимодействия не будет сохраняться между сеансами WSL, оно снова будет включено при запуске нового сеанса.</span><span class="sxs-lookup"><span data-stu-id="c54d8-172">Disabling interop will not persist between WSL sessions -- interop will be enabled again when a new session is launched.</span></span>

## <a name="earlier-versions-of-windows-10"></a><span data-ttu-id="c54d8-173">Предшествующие версии Windows 10</span><span class="sxs-lookup"><span data-stu-id="c54d8-173">Earlier versions of Windows 10</span></span>

<span data-ttu-id="c54d8-174">В предшествующих версиях Windows 10 для команд взаимодействия существует несколько различий.</span><span class="sxs-lookup"><span data-stu-id="c54d8-174">There are several differences for the interoperability commands on earlier Windows 10 versions.</span></span> <span data-ttu-id="c54d8-175">Если вы используете версию Creators Update (октябрь 2017 г., сборка 16299) или Юбилейного обновления (август 2016 г., сборка 14393) Windows 10, мы рекомендуем [выполнить обновление до последней версии Windows](ms-settings:windowsupdate). Если это невозможно, мы выделили некоторые отличия при взаимодействии ниже.</span><span class="sxs-lookup"><span data-stu-id="c54d8-175">If you're running a Creators Update (Oct 2017, Build 16299), or Anniversary Update (Aug 2016, Build 14393) version of Windows 10, we recommend you [update to the latest Windows version](ms-settings:windowsupdate), but if that's not possible, we have outlined some of the interop differences below.</span></span>

<span data-ttu-id="c54d8-176">Сводка:</span><span class="sxs-lookup"><span data-stu-id="c54d8-176">Summary:</span></span>

* <span data-ttu-id="c54d8-177">`bash.exe` заменен на `wsl.exe`;</span><span class="sxs-lookup"><span data-stu-id="c54d8-177">`bash.exe` has been replaced with `wsl.exe`.</span></span>
* <span data-ttu-id="c54d8-178">параметр `-c` не требуется для выполнения одной команды `wsl.exe`;</span><span class="sxs-lookup"><span data-stu-id="c54d8-178">`-c` option for running a single command isn't needed with `wsl.exe`.</span></span>
* <span data-ttu-id="c54d8-179">путь Windows включен в переменную `$PATH` WSL.</span><span class="sxs-lookup"><span data-stu-id="c54d8-179">Windows path is included in the WSL `$PATH`.</span></span>
* <span data-ttu-id="c54d8-180">Процесс отключения взаимодействия не изменяется.</span><span class="sxs-lookup"><span data-stu-id="c54d8-180">The process for disabling interop is unchanged.</span></span>

<span data-ttu-id="c54d8-181">Команды Linux можно запускать из командной строки Windows или из PowerShell, но для ранних версий Windows необходимо использовать команду `bash`.</span><span class="sxs-lookup"><span data-stu-id="c54d8-181">Linux commands can be run from the Windows Command Prompt or from PowerShell, but for early Windows versions, you man need to use the `bash` command.</span></span> <span data-ttu-id="c54d8-182">Например:</span><span class="sxs-lookup"><span data-stu-id="c54d8-182">For example:</span></span>

```powershell
C:\temp> bash -c "ls -la"
```

<span data-ttu-id="c54d8-183">Такие функции, как ввод, конвейерная передача и перенаправление файлов, работают должным образом.</span><span class="sxs-lookup"><span data-stu-id="c54d8-183">Things such as input, piping, and file redirection work as expected.</span></span>

<span data-ttu-id="c54d8-184">Команды WSL, передаваемые в `bash -c`, перенаправляются в процесс WSL без изменения.</span><span class="sxs-lookup"><span data-stu-id="c54d8-184">The WSL commands passed into `bash -c` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="c54d8-185">Пути к файлам должны быть указаны в формате WSL, кроме того, необходимо внимательно экранировать соответствующие знаки.</span><span class="sxs-lookup"><span data-stu-id="c54d8-185">File paths must be specified in the WSL format and care must be taken to escape relevant characters.</span></span> <span data-ttu-id="c54d8-186">Пример:</span><span class="sxs-lookup"><span data-stu-id="c54d8-186">Example:</span></span>

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
```

<span data-ttu-id="c54d8-187">–или–</span><span class="sxs-lookup"><span data-stu-id="c54d8-187">Or...</span></span>

```powershell
C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
```

<span data-ttu-id="c54d8-188">При вызове средства Windows из дистрибутива WSL в ранних версиях Windows 10 необходимо указать путь к каталогу.</span><span class="sxs-lookup"><span data-stu-id="c54d8-188">When calling a Windows tool from a WSL distribution in an earlier version of Windows 10, you will need to specify the directory path.</span></span> <span data-ttu-id="c54d8-189">Например, в командной строке WSL введите:</span><span class="sxs-lookup"><span data-stu-id="c54d8-189">For example, from your WSL command line, enter:</span></span>

```bash
/mnt/c/Windows/System32/notepad.exe
```

<span data-ttu-id="c54d8-190">В WSL эти исполняемые файлы обрабатываются аналогично собственным исполняемым файлам Linux.</span><span class="sxs-lookup"><span data-stu-id="c54d8-190">In WSL, these executables are handled similar to native Linux executables.</span></span>  <span data-ttu-id="c54d8-191">Это означает, что добавление каталогов в путь Linux и их конвейерная передача между командами выполняется должным образом.</span><span class="sxs-lookup"><span data-stu-id="c54d8-191">This means adding directories to the Linux path and piping between commands works as expected.</span></span>  <span data-ttu-id="c54d8-192">Например:</span><span class="sxs-lookup"><span data-stu-id="c54d8-192">For example:</span></span>

```bash
export PATH=$PATH:/mnt/c/Windows/System32
```
<span data-ttu-id="c54d8-193">Или</span><span class="sxs-lookup"><span data-stu-id="c54d8-193">Or</span></span>

```bash
ipconfig.exe | grep IPv4 | cut -d: -f2
```

<span data-ttu-id="c54d8-194">Двоичный файл Windows должен иметь расширение файла, его регистр символов должен совпадать с регистром в имени файла и этот файл должен быть исполняемым.</span><span class="sxs-lookup"><span data-stu-id="c54d8-194">The Windows binary must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="c54d8-195">Неисполняемые файлы, включая сценарии пакетной службы и команды, такие как `dir`, могут выполняться с помощью команды `/mnt/c/Windows/System32/cmd.exe /C`.</span><span class="sxs-lookup"><span data-stu-id="c54d8-195">Non-executables including batch scripts and command like `dir` can be run with `/mnt/c/Windows/System32/cmd.exe /C` command.</span></span> <span data-ttu-id="c54d8-196">Например:</span><span class="sxs-lookup"><span data-stu-id="c54d8-196">For example:</span></span>

```bash
/mnt/c/Windows/System32/cmd.exe /C dir
```

## <a name="additional-resources"></a><span data-ttu-id="c54d8-197">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c54d8-197">Additional resources</span></span>

* [<span data-ttu-id="c54d8-198">Запись блога WSL о взаимодействии за 2016 год</span><span class="sxs-lookup"><span data-stu-id="c54d8-198">WSL blog post on interoperability from 2016</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)
