---
title: Справочник по командам подсистемы Windows для Linux
description: Список команд, управляющих подсистемой Windows для Linux
keywords: Башонвиндовс, bash, WSL, Windows, подсистема Windows для Linux, виндовссубсистем, Ubuntu
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.openlocfilehash: 465f55f8ba210cd366adc66d433f1873e295136f
ms.sourcegitcommit: ead64b13501d6cb7170adafbb5624f4984a0af16
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/21/2019
ms.locfileid: "67307658"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="4d087-104">Справочник по командам для подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="4d087-104">Command Reference for Windows Subsystem for Linux</span></span>

<span data-ttu-id="4d087-105">Лучшим способом взаимодействия с подсистемой Windows для Linux является использование `wsl.exe` команды.</span><span class="sxs-lookup"><span data-stu-id="4d087-105">The best way to interact with the Windows Subsystem for Linux is to use the `wsl.exe` command.</span></span> 

## `wsl.exe` 

<span data-ttu-id="4d087-106">Ниже приведен список, содержащий все варианты использования `wsl.exe` версии 1903 для Windows.</span><span class="sxs-lookup"><span data-stu-id="4d087-106">Below is a list containing all options when using `wsl.exe` as of Windows Version 1903.</span></span>

* <span data-ttu-id="4d087-107">Аргументы для запуска двоичных файлов Linux:</span><span class="sxs-lookup"><span data-stu-id="4d087-107">Arguments for running Linux binaries:</span></span>

    * <span data-ttu-id="4d087-108">Если командная строка не указана, WSL. exe запускает оболочку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4d087-108">If no command line is provided, wsl.exe launches the default shell.</span></span>

    * <span data-ttu-id="4d087-109">--Exec,-e<CommandLine></span><span class="sxs-lookup"><span data-stu-id="4d087-109">--exec, -e <CommandLine></span></span>
        * <span data-ttu-id="4d087-110">Выполните указанную команду без использования оболочки Linux по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4d087-110">Execute the specified command without using the default Linux shell.</span></span>

    * --
        * <span data-ttu-id="4d087-111">Передайте оставшуюся строку команд как есть.</span><span class="sxs-lookup"><span data-stu-id="4d087-111">Pass the remaining command line as is.</span></span>

* <span data-ttu-id="4d087-112">Параметры:</span><span class="sxs-lookup"><span data-stu-id="4d087-112">Options:</span></span>
    * <span data-ttu-id="4d087-113">--Distribution,-d<Distro></span><span class="sxs-lookup"><span data-stu-id="4d087-113">--distribution, -d <Distro></span></span>
        * <span data-ttu-id="4d087-114">Запустить указанное распределение.</span><span class="sxs-lookup"><span data-stu-id="4d087-114">Run the specified distribution.</span></span>

    * <span data-ttu-id="4d087-115">--пользователь,-u<UserName></span><span class="sxs-lookup"><span data-stu-id="4d087-115">--user, -u <UserName></span></span>
        * <span data-ttu-id="4d087-116">Запуск от имени указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="4d087-116">Run as the specified user.</span></span>

* <span data-ttu-id="4d087-117">Аргументы для управления подсистемой Windows для Linux:</span><span class="sxs-lookup"><span data-stu-id="4d087-117">Arguments for managing Windows Subsystem for Linux:</span></span>

    * <span data-ttu-id="4d087-118">--Export <Distro><FileName></span><span class="sxs-lookup"><span data-stu-id="4d087-118">--export <Distro> <FileName></span></span>
        * <span data-ttu-id="4d087-119">Экспортирует распределение в tar-файл.</span><span class="sxs-lookup"><span data-stu-id="4d087-119">Exports the distribution to a tar file.</span></span>
        <span data-ttu-id="4d087-120">Имя файла может быть равно-для стандартного вывода.</span><span class="sxs-lookup"><span data-stu-id="4d087-120">The filename can be - for standard output.</span></span>

    * <span data-ttu-id="4d087-121">--Import <Distro> <InstallLocation>[параметры <FileName> ]</span><span class="sxs-lookup"><span data-stu-id="4d087-121">--import <Distro> <InstallLocation> <FileName> [Options]</span></span>
        * <span data-ttu-id="4d087-122">Импортирует указанный tar-файл в качестве нового распространения.</span><span class="sxs-lookup"><span data-stu-id="4d087-122">Imports the specified tar file as a new distribution.</span></span>
        <span data-ttu-id="4d087-123">Имя файла может быть равно-для стандартного ввода.</span><span class="sxs-lookup"><span data-stu-id="4d087-123">The filename can be - for standard input.</span></span>

        * <span data-ttu-id="4d087-124">Параметры:</span><span class="sxs-lookup"><span data-stu-id="4d087-124">Options:</span></span>
            * <span data-ttu-id="4d087-125">--Version <Version> указывает версию, используемую для нового распространения.</span><span class="sxs-lookup"><span data-stu-id="4d087-125">--version <Version> Specifies the version to use for the new distribution.</span></span>

    * <span data-ttu-id="4d087-126">--List,-l [параметры]</span><span class="sxs-lookup"><span data-stu-id="4d087-126">--list, -l [Options]</span></span>
        * <span data-ttu-id="4d087-127">Выводит список распределений.</span><span class="sxs-lookup"><span data-stu-id="4d087-127">Lists distributions.</span></span>

        * <span data-ttu-id="4d087-128">Параметры:</span><span class="sxs-lookup"><span data-stu-id="4d087-128">Options:</span></span>
            * <span data-ttu-id="4d087-129">--все</span><span class="sxs-lookup"><span data-stu-id="4d087-129">--all</span></span>
                * <span data-ttu-id="4d087-130">Список всех дистрибутивов, включая дистрибутивы, которые сейчас устанавливаются или удаляются.</span><span class="sxs-lookup"><span data-stu-id="4d087-130">List all distributions, including distributions that are currently being installed or uninstalled.</span></span>

            * <span data-ttu-id="4d087-131">--Запуск</span><span class="sxs-lookup"><span data-stu-id="4d087-131">--running</span></span>
                * <span data-ttu-id="4d087-132">Перечислите только те дистрибутивы, которые выполняются в данный момент.</span><span class="sxs-lookup"><span data-stu-id="4d087-132">List only distributions that are currently running.</span></span>

    * <span data-ttu-id="4d087-133">--Set-Default,-s<Distro></span><span class="sxs-lookup"><span data-stu-id="4d087-133">--set-default, -s <Distro></span></span>
        * <span data-ttu-id="4d087-134">Задает распределение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4d087-134">Sets the distribution as the default.</span></span>

    * <span data-ttu-id="4d087-135">--Set-Default-версия<Version></span><span class="sxs-lookup"><span data-stu-id="4d087-135">--set-default-version <Version></span></span>
        * <span data-ttu-id="4d087-136">Изменяет версию установки по умолчанию для новых дистрибутивов.</span><span class="sxs-lookup"><span data-stu-id="4d087-136">Changes the default install version for new distributions.</span></span>

    * <span data-ttu-id="4d087-137">--Set-Version <Distro><Version></span><span class="sxs-lookup"><span data-stu-id="4d087-137">--set-version <Distro> <Version></span></span>
        * <span data-ttu-id="4d087-138">Изменяет версию указанного распространения.</span><span class="sxs-lookup"><span data-stu-id="4d087-138">Changes the version of the specified distribution.</span></span>

    * <span data-ttu-id="4d087-139">--Terminate,-t<Distro></span><span class="sxs-lookup"><span data-stu-id="4d087-139">--terminate, -t <Distro></span></span>
        * <span data-ttu-id="4d087-140">Завершает указанное распределение.</span><span class="sxs-lookup"><span data-stu-id="4d087-140">Terminates the specified distribution.</span></span>

    * <span data-ttu-id="4d087-141">--Отмена регистрации<Distro></span><span class="sxs-lookup"><span data-stu-id="4d087-141">--unregister <Distro></span></span>
        * <span data-ttu-id="4d087-142">Отменяет регистрацию распределения.</span><span class="sxs-lookup"><span data-stu-id="4d087-142">Unregisters the distribution.</span></span>

    * <span data-ttu-id="4d087-143">--help</span><span class="sxs-lookup"><span data-stu-id="4d087-143">--help</span></span>
        * <span data-ttu-id="4d087-144">Отображение сведений об использовании.</span><span class="sxs-lookup"><span data-stu-id="4d087-144">Display usage information.</span></span>

## <a name="additional-commands"></a><span data-ttu-id="4d087-145">Дополнительные команды</span><span class="sxs-lookup"><span data-stu-id="4d087-145">Additional Commands</span></span>

<span data-ttu-id="4d087-146">Существуют также исторические команды для взаимодействия с подсистемой Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="4d087-146">There are also historic commands to interact with the Windows Subsystem for Linux.</span></span> <span data-ttu-id="4d087-147">Их функциональность включается в `wsl.exe`, но они по-прежнему доступны для использования.</span><span class="sxs-lookup"><span data-stu-id="4d087-147">Their functionality is encompassed within `wsl.exe`, but they are still available for use.</span></span> 

### `wslconfig.exe`

<span data-ttu-id="4d087-148">Эта команда позволяет настроить дистрибутив WSL.</span><span class="sxs-lookup"><span data-stu-id="4d087-148">This command lets you configure your WSL distribution.</span></span> <span data-ttu-id="4d087-149">Ниже приведен список параметров.</span><span class="sxs-lookup"><span data-stu-id="4d087-149">Below is a list of its options.</span></span>

* <span data-ttu-id="4d087-150">/l,/List [параметр]</span><span class="sxs-lookup"><span data-stu-id="4d087-150">/l, /list [Option]</span></span>
    * <span data-ttu-id="4d087-151">Выводит список зарегистрированных распределений.</span><span class="sxs-lookup"><span data-stu-id="4d087-151">Lists registered distributions.</span></span>
        * <span data-ttu-id="4d087-152">/All — при необходимости перечисление всех дистрибутивов, включая дистрибутивы, которые в данный момент устанавливаются или удаляются.</span><span class="sxs-lookup"><span data-stu-id="4d087-152">/all - Optionally list all distributions, including distributions that       are currently being installed or uninstalled.</span></span>

        * <span data-ttu-id="4d087-153">/руннинг — перечисление только тех распределений, которые выполняются в данный момент.</span><span class="sxs-lookup"><span data-stu-id="4d087-153">/running - List only distributions that are currently running.</span></span>

* <span data-ttu-id="4d087-154">/s,/сетдефаулт<DistributionName></span><span class="sxs-lookup"><span data-stu-id="4d087-154">/s, /setdefault <DistributionName></span></span>
    * <span data-ttu-id="4d087-155">Задает распределение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4d087-155">Sets the distribution as the default.</span></span>

* <span data-ttu-id="4d087-156">/t,/терминате<DistributionName></span><span class="sxs-lookup"><span data-stu-id="4d087-156">/t, /terminate <DistributionName></span></span>
    * <span data-ttu-id="4d087-157">Завершает распределение.</span><span class="sxs-lookup"><span data-stu-id="4d087-157">Terminates the distribution.</span></span>

* <span data-ttu-id="4d087-158">/u,/Unregister<DistributionName></span><span class="sxs-lookup"><span data-stu-id="4d087-158">/u, /unregister <DistributionName></span></span>
    * <span data-ttu-id="4d087-159">Отменяет регистрацию распределения.</span><span class="sxs-lookup"><span data-stu-id="4d087-159">Unregisters the distribution.</span></span>

### `bash.exe`

<span data-ttu-id="4d087-160">Эта команда используется для запуска оболочки bash.</span><span class="sxs-lookup"><span data-stu-id="4d087-160">This command is used to start a bash shell.</span></span> <span data-ttu-id="4d087-161">Ниже приведены параметры, которые можно использовать с этой командой.</span><span class="sxs-lookup"><span data-stu-id="4d087-161">Below are the options you can use with this command.</span></span>

* <span data-ttu-id="4d087-162">Параметр не задан</span><span class="sxs-lookup"><span data-stu-id="4d087-162">No Option given</span></span>
    * <span data-ttu-id="4d087-163">Запускает оболочку Bash в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="4d087-163">Launches the Bash shell in the current directory.</span></span> <span data-ttu-id="4d087-164">Если оболочка Bash не установлена автоматически`lxrun /install`</span><span class="sxs-lookup"><span data-stu-id="4d087-164">If the Bash shell is not installed automatically runs `lxrun /install`</span></span>

* <span data-ttu-id="4d087-165">Bash ~</span><span class="sxs-lookup"><span data-stu-id="4d087-165">bash ~</span></span>
    * <span data-ttu-id="4d087-166">Запускает оболочку Bash в домашнем каталоге пользователя.</span><span class="sxs-lookup"><span data-stu-id="4d087-166">Launches the bash shell into the user's home directory.</span></span>  <span data-ttu-id="4d087-167">Аналогично запуску `cd ~`.</span><span class="sxs-lookup"><span data-stu-id="4d087-167">Similar to running `cd ~`.</span></span>

* <span data-ttu-id="4d087-168">Bash-c "&lt;Command&gt;"</span><span class="sxs-lookup"><span data-stu-id="4d087-168">bash -c "&lt;command&gt;"</span></span>
    * <span data-ttu-id="4d087-169">Выполняет команду, выводит выходные данные и выходит обратно в командную строку Windows.</span><span class="sxs-lookup"><span data-stu-id="4d087-169">Runs the command, prints the output and exits back to the Windows command prompt.</span></span> <br/> <br/> <span data-ttu-id="4d087-170">Например`bash -c "ls"`</span><span class="sxs-lookup"><span data-stu-id="4d087-170">Example:  `bash -c "ls"`</span></span>

## <a name="deprecated-commands"></a><span data-ttu-id="4d087-171">Устаревшие команды</span><span class="sxs-lookup"><span data-stu-id="4d087-171">Deprecated Commands</span></span>

<span data-ttu-id="4d087-172">`lxrun.exe` Была первой командой, используемой для установки и управления подсистемой Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="4d087-172">The `lxrun.exe` was the first command used to install and manage the Windows Subsystem for Linux.</span></span> <span data-ttu-id="4d087-173">Она устарела в Windows 10 1803 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="4d087-173">It is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="4d087-174">Команду `lxrun.exe` можно использовать для взаимодействия с подсистемой [Windows для Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) напрямую.</span><span class="sxs-lookup"><span data-stu-id="4d087-174">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="4d087-175">Эти команды устанавливаются в `\Windows\System32` каталог и могут выполняться в командной строке Windows или в PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4d087-175">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

| <span data-ttu-id="4d087-176">Command</span><span class="sxs-lookup"><span data-stu-id="4d087-176">Command</span></span>                     | <span data-ttu-id="4d087-177">Описание</span><span class="sxs-lookup"><span data-stu-id="4d087-177">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="4d087-178">Команда лксрун используется для управления экземпляром WSL.</span><span class="sxs-lookup"><span data-stu-id="4d087-178">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="4d087-179">Запускает процесс загрузки и установки.</span><span class="sxs-lookup"><span data-stu-id="4d087-179">Starts the download and install process.</span></span> <br/> <span data-ttu-id="4d087-180">**/y** можно добавить, чтобы обойти все запросы.</span><span class="sxs-lookup"><span data-stu-id="4d087-180">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="4d087-181">Запрос на подтверждение будет принят автоматически, и пользователь по умолчанию будет иметь значение root.</span><span class="sxs-lookup"><span data-stu-id="4d087-181">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="4d087-182">Удаляет образ Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="4d087-182">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="4d087-183">По умолчанию это не приводит к удалению домашнего каталога пользователя Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="4d087-183">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="4d087-184">параметр **/y** можно добавить для автоматического принятия запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="4d087-184">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="4d087-185">**/Full** удалит и удаляет домашний каталог Ubuntu пользователя.</span><span class="sxs-lookup"><span data-stu-id="4d087-185">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="4d087-186">Задает bash по умолчанию для пользователя Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="4d087-186">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="4d087-187">Запрашивает пароль, если указанный пользователь не существует.</span><span class="sxs-lookup"><span data-stu-id="4d087-187">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="4d087-188">Дополнительные сведения см https://aka.ms/wslusers. по адресу.</span><span class="sxs-lookup"><span data-stu-id="4d087-188">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="4d087-189">**/y** Обходит промпинг для пароля.</span><span class="sxs-lookup"><span data-stu-id="4d087-189">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="4d087-190">Пользователь будет создан без пароля.</span><span class="sxs-lookup"><span data-stu-id="4d087-190">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="4d087-191">Обновляет индекс пакета подсистемы.</span><span class="sxs-lookup"><span data-stu-id="4d087-191">Updates the subsystem's package index</span></span>          |
