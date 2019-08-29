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
ms.localizationpriority: high
ms.openlocfilehash: edd4b8216a25f519e36b8b99b626b0a4315f6039
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122738"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="91077-104">Справочник по командам для подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="91077-104">Command Reference for Windows Subsystem for Linux</span></span>

<span data-ttu-id="91077-105">Лучшим способом взаимодействия с подсистемой Windows для Linux является использование `wsl.exe` команды.</span><span class="sxs-lookup"><span data-stu-id="91077-105">The best way to interact with the Windows Subsystem for Linux is to use the `wsl.exe` command.</span></span> 


## `wsl.exe`

<span data-ttu-id="91077-106">Ниже приведен список, содержащий все варианты использования `wsl.exe` версии 1903 для Windows.</span><span class="sxs-lookup"><span data-stu-id="91077-106">Below is a list containing all options when using `wsl.exe` as of Windows Version 1903.</span></span>

<span data-ttu-id="91077-107">Использующ`wsl [Argument] [Options...] [CommandLine]`</span><span class="sxs-lookup"><span data-stu-id="91077-107">Using: `wsl [Argument] [Options...] [CommandLine]`</span></span>

### <a name="arguments-for-running-linux-binaries"></a><span data-ttu-id="91077-108">Аргументы для запуска двоичных файлов Linux</span><span class="sxs-lookup"><span data-stu-id="91077-108">Arguments for running Linux binaries</span></span>

* <span data-ttu-id="91077-109">**Без аргументов**</span><span class="sxs-lookup"><span data-stu-id="91077-109">**Without arguments**</span></span>

  <span data-ttu-id="91077-110">Если командная строка не указана, WSL. exe запускает оболочку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="91077-110">If no command line is provided, wsl.exe launches the default shell.</span></span>

* <span data-ttu-id="91077-111">**--Exec,-e \<Командная строка >**</span><span class="sxs-lookup"><span data-stu-id="91077-111">**--exec, -e \<CommandLine>**</span></span>
  
  <span data-ttu-id="91077-112">Выполните указанную команду без использования оболочки Linux по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="91077-112">Execute the specified command without using the default Linux shell.</span></span>

* **--**
  
  <span data-ttu-id="91077-113">Передайте оставшуюся строку команд как есть.</span><span class="sxs-lookup"><span data-stu-id="91077-113">Pass the remaining command line as is.</span></span>

<span data-ttu-id="91077-114">Приведенные выше команды также принимают следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="91077-114">The above commands also accept the following options:</span></span>

* <span data-ttu-id="91077-115">**--Distribution,-d \<дистрибутив >**</span><span class="sxs-lookup"><span data-stu-id="91077-115">**--distribution, -d \<Distro>**</span></span>

  <span data-ttu-id="91077-116">Запустить указанное распределение.</span><span class="sxs-lookup"><span data-stu-id="91077-116">Run the specified distribution.</span></span>

* <span data-ttu-id="91077-117">**--User,-u \<имя_пользователя >**</span><span class="sxs-lookup"><span data-stu-id="91077-117">**--user, -u \<UserName>**</span></span>

  <span data-ttu-id="91077-118">Запуск от имени указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="91077-118">Run as the specified user.</span></span>

### <a name="arguments-for-managing-windows-subsystem-for-linux"></a><span data-ttu-id="91077-119">Аргументы для управления подсистемой Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="91077-119">Arguments for managing Windows Subsystem for Linux</span></span>

* <span data-ttu-id="91077-120">**--Export \<дистрибутив имя \<файла > >**</span><span class="sxs-lookup"><span data-stu-id="91077-120">**--export \<Distro> \<FileName>**</span></span>
  
  <span data-ttu-id="91077-121">Экспортирует распределение в tar-файл.</span><span class="sxs-lookup"><span data-stu-id="91077-121">Exports the distribution to a tar file.</span></span> <span data-ttu-id="91077-122">Имя файла может быть равно-для стандартного вывода.</span><span class="sxs-lookup"><span data-stu-id="91077-122">The filename can be - for standard output.</span></span>

* <span data-ttu-id="91077-123">**--Import \<дистрибутив > \<InstallLocation > \<имя файла >**</span><span class="sxs-lookup"><span data-stu-id="91077-123">**--import \<Distro> \<InstallLocation> \<FileName>**</span></span>
  
  <span data-ttu-id="91077-124">Импортирует указанный tar-файл в качестве нового распространения.</span><span class="sxs-lookup"><span data-stu-id="91077-124">Imports the specified tar file as a new distribution.</span></span> <span data-ttu-id="91077-125">Имя файла может быть равно-для стандартного ввода.</span><span class="sxs-lookup"><span data-stu-id="91077-125">The filename can be - for standard input.</span></span>

* <span data-ttu-id="91077-126">**--List,-l [параметры]**</span><span class="sxs-lookup"><span data-stu-id="91077-126">**--list, -l [Options]**</span></span>
  
  <span data-ttu-id="91077-127">Выводит список распределений.</span><span class="sxs-lookup"><span data-stu-id="91077-127">Lists distributions.</span></span>

  <span data-ttu-id="91077-128">Параметры:</span><span class="sxs-lookup"><span data-stu-id="91077-128">Options:</span></span>
  * <span data-ttu-id="91077-129">**--все**</span><span class="sxs-lookup"><span data-stu-id="91077-129">**--all**</span></span>
      
    <span data-ttu-id="91077-130">Список всех дистрибутивов, включая дистрибутивы, которые сейчас устанавливаются или удаляются.</span><span class="sxs-lookup"><span data-stu-id="91077-130">List all distributions, including distributions that are currently being installed or uninstalled.</span></span>

  * <span data-ttu-id="91077-131">**--Запуск**</span><span class="sxs-lookup"><span data-stu-id="91077-131">**--running**</span></span>
      
    <span data-ttu-id="91077-132">Перечислите только те дистрибутивы, которые выполняются в данный момент.</span><span class="sxs-lookup"><span data-stu-id="91077-132">List only distributions that are currently running.</span></span>

* <span data-ttu-id="91077-133">**--Set-Default,-s \<дистрибутив >**</span><span class="sxs-lookup"><span data-stu-id="91077-133">**--set-default, -s \<Distro>**</span></span>
  
  <span data-ttu-id="91077-134">Задает распределение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="91077-134">Sets the distribution as the default.</span></span>

* <span data-ttu-id="91077-135">**--Terminate,-t \<дистрибутив >**</span><span class="sxs-lookup"><span data-stu-id="91077-135">**--terminate, -t \<Distro>**</span></span>
  
  <span data-ttu-id="91077-136">Завершает указанное распределение.</span><span class="sxs-lookup"><span data-stu-id="91077-136">Terminates the specified distribution.</span></span>

* <span data-ttu-id="91077-137">**--Отмена регистрации \<дистрибутив >**</span><span class="sxs-lookup"><span data-stu-id="91077-137">**--unregister \<Distro>**</span></span>
  
  <span data-ttu-id="91077-138">Отменяет регистрацию распределения.</span><span class="sxs-lookup"><span data-stu-id="91077-138">Unregisters the distribution.</span></span>
   
* <span data-ttu-id="91077-139">**--Справка** Отображение сведений об использовании.</span><span class="sxs-lookup"><span data-stu-id="91077-139">**--help** Display usage information.</span></span>

## <a name="additional-commands"></a><span data-ttu-id="91077-140">Дополнительные команды</span><span class="sxs-lookup"><span data-stu-id="91077-140">Additional Commands</span></span>

<span data-ttu-id="91077-141">Существуют также исторические команды для взаимодействия с подсистемой Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="91077-141">There are also historic commands to interact with the Windows Subsystem for Linux.</span></span> <span data-ttu-id="91077-142">Их функциональность включается в `wsl.exe`, но они по-прежнему доступны для использования.</span><span class="sxs-lookup"><span data-stu-id="91077-142">Their functionality is encompassed within `wsl.exe`, but they are still available for use.</span></span> 

### `wslconfig.exe`

<span data-ttu-id="91077-143">Эта команда позволяет настроить дистрибутив WSL.</span><span class="sxs-lookup"><span data-stu-id="91077-143">This command lets you configure your WSL distribution.</span></span> <span data-ttu-id="91077-144">Ниже приведен список параметров.</span><span class="sxs-lookup"><span data-stu-id="91077-144">Below is a list of its options.</span></span>

<span data-ttu-id="91077-145">Использующ`wslconfig [Argument] [Options...]`</span><span class="sxs-lookup"><span data-stu-id="91077-145">Using: `wslconfig [Argument] [Options...]`</span></span>

#### <a name="arguments"></a><span data-ttu-id="91077-146">Аргументы</span><span class="sxs-lookup"><span data-stu-id="91077-146">Arguments</span></span>
* <span data-ttu-id="91077-147">**/l,/List [параметры]**</span><span class="sxs-lookup"><span data-stu-id="91077-147">**/l, /list [Options]**</span></span>
  
  <span data-ttu-id="91077-148">Выводит список зарегистрированных распределений.</span><span class="sxs-lookup"><span data-stu-id="91077-148">Lists registered distributions.</span></span>
  
  <span data-ttu-id="91077-149">Параметры:</span><span class="sxs-lookup"><span data-stu-id="91077-149">Options:</span></span>
    * <span data-ttu-id="91077-150">**/ALL**</span><span class="sxs-lookup"><span data-stu-id="91077-150">**/all**</span></span>
    
      <span data-ttu-id="91077-151">При необходимости перечислите все дистрибутивы, включая дистрибутивы, которые сейчас устанавливаются или удаляются.</span><span class="sxs-lookup"><span data-stu-id="91077-151">Optionally list all distributions, including distributions that are currently being installed or uninstalled.</span></span>

    * <span data-ttu-id="91077-152">**/руннинг**</span><span class="sxs-lookup"><span data-stu-id="91077-152">**/running**</span></span>
      
      <span data-ttu-id="91077-153">Перечислите только те дистрибутивы, которые выполняются в данный момент.</span><span class="sxs-lookup"><span data-stu-id="91077-153">List only distributions that are currently running.</span></span>

* <span data-ttu-id="91077-154">**/s,/сетдефаулт \<дистрибутив >**</span><span class="sxs-lookup"><span data-stu-id="91077-154">**/s, /setdefault \<Distro>**</span></span>
  
  <span data-ttu-id="91077-155">Задает распределение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="91077-155">Sets the distribution as the default.</span></span>

* <span data-ttu-id="91077-156">**/t,/терминате \<дистрибутив >**</span><span class="sxs-lookup"><span data-stu-id="91077-156">**/t, /terminate \<Distro>**</span></span>
  
  <span data-ttu-id="91077-157">Завершает распределение.</span><span class="sxs-lookup"><span data-stu-id="91077-157">Terminates the distribution.</span></span>

* <span data-ttu-id="91077-158">**/u,/Unregister \<дистрибутив >**</span><span class="sxs-lookup"><span data-stu-id="91077-158">**/u, /unregister \<Distro>**</span></span>
  
  <span data-ttu-id="91077-159">Отменяет регистрацию распределения.</span><span class="sxs-lookup"><span data-stu-id="91077-159">Unregisters the distribution.</span></span>
   
* <span data-ttu-id="91077-160">**/Upgrade \<дистрибутив >**</span><span class="sxs-lookup"><span data-stu-id="91077-160">**/upgrade \<Distro>**</span></span>
  
  <span data-ttu-id="91077-161">Обновляет дистрибутив до формата файловой системы Вслфс.</span><span class="sxs-lookup"><span data-stu-id="91077-161">Upgrades the distribution to the WslFs file system format.</span></span>

### `bash.exe`

<span data-ttu-id="91077-162">Эта команда используется для запуска оболочки bash.</span><span class="sxs-lookup"><span data-stu-id="91077-162">This command is used to start a bash shell.</span></span> <span data-ttu-id="91077-163">Ниже приведены параметры, которые можно использовать с этой командой.</span><span class="sxs-lookup"><span data-stu-id="91077-163">Below are the options you can use with this command.</span></span>

<span data-ttu-id="91077-164">Использующ`bash [Options...]`</span><span class="sxs-lookup"><span data-stu-id="91077-164">Using: `bash [Options...]`</span></span>

* <span data-ttu-id="91077-165">**Параметр не задан**</span><span class="sxs-lookup"><span data-stu-id="91077-165">**No Option given**</span></span>
  
  <span data-ttu-id="91077-166">Запускает оболочку Bash в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="91077-166">Launches the Bash shell in the current directory.</span></span> <span data-ttu-id="91077-167">Если оболочка Bash не установлена автоматически`lxrun /install`</span><span class="sxs-lookup"><span data-stu-id="91077-167">If the Bash shell is not installed automatically runs `lxrun /install`</span></span>

* **~**
  
  <span data-ttu-id="91077-168">`bash ~`запускает оболочку Bash в домашнем каталоге пользователя.</span><span class="sxs-lookup"><span data-stu-id="91077-168">`bash ~` launches the bash shell into the user's home directory.</span></span>  <span data-ttu-id="91077-169">Аналогично запуску `cd ~`.</span><span class="sxs-lookup"><span data-stu-id="91077-169">Similar to running `cd ~`.</span></span>

* <span data-ttu-id="91077-170">**-c "\<Command >"**</span><span class="sxs-lookup"><span data-stu-id="91077-170">**-c "\<command>"**</span></span>
  
  <span data-ttu-id="91077-171">Выполняет команду, выводит выходные данные и выходит обратно в командную строку Windows.</span><span class="sxs-lookup"><span data-stu-id="91077-171">Runs the command, prints the output and exits back to the Windows command prompt.</span></span>
    
  <span data-ttu-id="91077-172">Пример: `bash -c "ls"`.</span><span class="sxs-lookup"><span data-stu-id="91077-172">Example:  `bash -c "ls"`.</span></span>

## <a name="deprecated-commands"></a><span data-ttu-id="91077-173">Устаревшие команды</span><span class="sxs-lookup"><span data-stu-id="91077-173">Deprecated Commands</span></span>

<span data-ttu-id="91077-174">`lxrun.exe` Была первой командой, используемой для установки и управления подсистемой Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="91077-174">The `lxrun.exe` was the first command used to install and manage the Windows Subsystem for Linux.</span></span> <span data-ttu-id="91077-175">Она устарела в Windows 10 1803 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="91077-175">It is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="91077-176">Команду `lxrun.exe` можно использовать для взаимодействия с подсистемой [Windows для Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) напрямую.</span><span class="sxs-lookup"><span data-stu-id="91077-176">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="91077-177">Эти команды устанавливаются в `\Windows\System32` каталог и могут выполняться в командной строке Windows или в PowerShell.</span><span class="sxs-lookup"><span data-stu-id="91077-177">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

| <span data-ttu-id="91077-178">Command</span><span class="sxs-lookup"><span data-stu-id="91077-178">Command</span></span>                     | <span data-ttu-id="91077-179">Описание</span><span class="sxs-lookup"><span data-stu-id="91077-179">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="91077-180">Команда лксрун используется для управления экземпляром WSL.</span><span class="sxs-lookup"><span data-stu-id="91077-180">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="91077-181">Запускает процесс загрузки и установки.</span><span class="sxs-lookup"><span data-stu-id="91077-181">Starts the download and install process.</span></span> <br/> <span data-ttu-id="91077-182">**/y** можно добавить, чтобы обойти все запросы.</span><span class="sxs-lookup"><span data-stu-id="91077-182">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="91077-183">Запрос на подтверждение будет принят автоматически, и пользователь по умолчанию будет иметь значение root.</span><span class="sxs-lookup"><span data-stu-id="91077-183">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="91077-184">Удаляет образ Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="91077-184">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="91077-185">По умолчанию это не приводит к удалению домашнего каталога пользователя Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="91077-185">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="91077-186">параметр **/y** можно добавить для автоматического принятия запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="91077-186">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="91077-187">**/Full** удалит и удаляет домашний каталог Ubuntu пользователя.</span><span class="sxs-lookup"><span data-stu-id="91077-187">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="91077-188">Задает bash по умолчанию для пользователя Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="91077-188">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="91077-189">Запрашивает пароль, если указанный пользователь не существует.</span><span class="sxs-lookup"><span data-stu-id="91077-189">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="91077-190">Дополнительные сведения см https://aka.ms/wslusers. по адресу.</span><span class="sxs-lookup"><span data-stu-id="91077-190">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="91077-191">**/y** Обходит промпинг для пароля.</span><span class="sxs-lookup"><span data-stu-id="91077-191">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="91077-192">Пользователь будет создан без пароля.</span><span class="sxs-lookup"><span data-stu-id="91077-192">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="91077-193">Обновляет индекс пакета подсистемы.</span><span class="sxs-lookup"><span data-stu-id="91077-193">Updates the subsystem's package index</span></span>          |
