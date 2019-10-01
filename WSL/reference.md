---
title: Справочные материалы по командам подсистемы Windows для Linux
description: Список команд для управления подсистемой Windows для Linux.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: d74a6926fd797f2e1ede0fd5d8d080d0f1ce3f6b
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269844"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="92192-104">Справочные материалы по командам подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="92192-104">Command Reference for Windows Subsystem for Linux</span></span>

<span data-ttu-id="92192-105">Лучший способ взаимодействовать с подсистемой Windows для Linux — использовать команду `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="92192-105">The best way to interact with the Windows Subsystem for Linux is to use the `wsl.exe` command.</span></span> 


## `wsl.exe`

<span data-ttu-id="92192-106">Ниже приведен список, содержащий все параметры `wsl.exe` при использовании в Windows версии 1903.</span><span class="sxs-lookup"><span data-stu-id="92192-106">Below is a list containing all options when using `wsl.exe` as of Windows Version 1903.</span></span>

<span data-ttu-id="92192-107">Использование: `wsl [Argument] [Options...] [CommandLine]`</span><span class="sxs-lookup"><span data-stu-id="92192-107">Using: `wsl [Argument] [Options...] [CommandLine]`</span></span>

### <a name="arguments-for-running-linux-binaries"></a><span data-ttu-id="92192-108">Аргументы для выполнения двоичных файлов Linux</span><span class="sxs-lookup"><span data-stu-id="92192-108">Arguments for running Linux binaries</span></span>

* <span data-ttu-id="92192-109">**Без аргументов**</span><span class="sxs-lookup"><span data-stu-id="92192-109">**Without arguments**</span></span>

  <span data-ttu-id="92192-110">Если командная строка не указана, wsl.exe запускает оболочку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="92192-110">If no command line is provided, wsl.exe launches the default shell.</span></span>

* <span data-ttu-id="92192-111">**--exec, -e \<командная_строка>**</span><span class="sxs-lookup"><span data-stu-id="92192-111">**--exec, -e \<CommandLine>**</span></span>
  
  <span data-ttu-id="92192-112">Выполнение указанной команды без использования оболочки Linux по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="92192-112">Execute the specified command without using the default Linux shell.</span></span>

* **--**
  
  <span data-ttu-id="92192-113">Остальная часть командной строки передается "как есть".</span><span class="sxs-lookup"><span data-stu-id="92192-113">Pass the remaining command line as is.</span></span>

<span data-ttu-id="92192-114">Приведенные выше команды также принимают следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="92192-114">The above commands also accept the following options:</span></span>

* <span data-ttu-id="92192-115">**--distribution, -d \<дистрибутив>**</span><span class="sxs-lookup"><span data-stu-id="92192-115">**--distribution, -d \<Distro>**</span></span>

  <span data-ttu-id="92192-116">Запуск указанного дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="92192-116">Run the specified distribution.</span></span>

* <span data-ttu-id="92192-117">**--user, -u \<имя_пользователя>**</span><span class="sxs-lookup"><span data-stu-id="92192-117">**--user, -u \<UserName>**</span></span>

  <span data-ttu-id="92192-118">Выполнение от имени указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="92192-118">Run as the specified user.</span></span>

### <a name="arguments-for-managing-windows-subsystem-for-linux"></a><span data-ttu-id="92192-119">Аргументы для управления подсистемой Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="92192-119">Arguments for managing Windows Subsystem for Linux</span></span>

* <span data-ttu-id="92192-120">**--export \<дистрибутив> \<имя_файла>**</span><span class="sxs-lookup"><span data-stu-id="92192-120">**--export \<Distro> \<FileName>**</span></span>
  
  <span data-ttu-id="92192-121">Экспорт дистрибутива в TAR-файл.</span><span class="sxs-lookup"><span data-stu-id="92192-121">Exports the distribution to a tar file.</span></span> <span data-ttu-id="92192-122">Именем файла может быть "-" для стандартного вывода.</span><span class="sxs-lookup"><span data-stu-id="92192-122">The filename can be - for standard output.</span></span>

* <span data-ttu-id="92192-123">**--import \<дистрибутив> \<расположение_установки> \<имя_файла>**</span><span class="sxs-lookup"><span data-stu-id="92192-123">**--import \<Distro> \<InstallLocation> \<FileName>**</span></span>
  
  <span data-ttu-id="92192-124">Импорт указанного TAR-файла в качестве нового дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="92192-124">Imports the specified tar file as a new distribution.</span></span> <span data-ttu-id="92192-125">Именем файла может быть "-" для стандартного ввода.</span><span class="sxs-lookup"><span data-stu-id="92192-125">The filename can be - for standard input.</span></span>

* <span data-ttu-id="92192-126">**--list, -l [параметры]**</span><span class="sxs-lookup"><span data-stu-id="92192-126">**--list, -l [Options]**</span></span>
  
  <span data-ttu-id="92192-127">Вывод списка дистрибутивов.</span><span class="sxs-lookup"><span data-stu-id="92192-127">Lists distributions.</span></span>

  <span data-ttu-id="92192-128">Параметры:</span><span class="sxs-lookup"><span data-stu-id="92192-128">Options:</span></span>
  * <span data-ttu-id="92192-129">**--all**</span><span class="sxs-lookup"><span data-stu-id="92192-129">**--all**</span></span>
      
    <span data-ttu-id="92192-130">Вывод списка всех дистрибутивов, включая дистрибутивы, которые сейчас устанавливаются или удаляются.</span><span class="sxs-lookup"><span data-stu-id="92192-130">List all distributions, including distributions that are currently being installed or uninstalled.</span></span>

  * <span data-ttu-id="92192-131">**--running**</span><span class="sxs-lookup"><span data-stu-id="92192-131">**--running**</span></span>
      
    <span data-ttu-id="92192-132">Вывод списка всех дистрибутивов, выполняемых в данный момент.</span><span class="sxs-lookup"><span data-stu-id="92192-132">List only distributions that are currently running.</span></span>

* <span data-ttu-id="92192-133">**--set-default, -s \<дистрибутив>**</span><span class="sxs-lookup"><span data-stu-id="92192-133">**--set-default, -s \<Distro>**</span></span>
  
  <span data-ttu-id="92192-134">Указание дистрибутива, используемого по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="92192-134">Sets the distribution as the default.</span></span>

* <span data-ttu-id="92192-135">**--terminate, -t \<дистрибутив>**</span><span class="sxs-lookup"><span data-stu-id="92192-135">**--terminate, -t \<Distro>**</span></span>
  
  <span data-ttu-id="92192-136">Завершение указанного дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="92192-136">Terminates the specified distribution.</span></span>

* <span data-ttu-id="92192-137">**--unregister \<дистрибутив>**</span><span class="sxs-lookup"><span data-stu-id="92192-137">**--unregister \<Distro>**</span></span>
  
  <span data-ttu-id="92192-138">Отмена регистрации дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="92192-138">Unregisters the distribution.</span></span>
   
* <span data-ttu-id="92192-139">**--help** отображает сведения об использовании.</span><span class="sxs-lookup"><span data-stu-id="92192-139">**--help** Display usage information.</span></span>

## <a name="additional-commands"></a><span data-ttu-id="92192-140">Дополнительные команды</span><span class="sxs-lookup"><span data-stu-id="92192-140">Additional Commands</span></span>

<span data-ttu-id="92192-141">Доступны также устоявшиеся команды для взаимодействия с подсистемой Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="92192-141">There are also historic commands to interact with the Windows Subsystem for Linux.</span></span> <span data-ttu-id="92192-142">Их функциональные возможности реализованы в `wsl.exe`, но эти команды по-прежнему можно использовать.</span><span class="sxs-lookup"><span data-stu-id="92192-142">Their functionality is encompassed within `wsl.exe`, but they are still available for use.</span></span> 

### `wslconfig.exe`

<span data-ttu-id="92192-143">Эта команда позволяет настроить дистрибутив WSL.</span><span class="sxs-lookup"><span data-stu-id="92192-143">This command lets you configure your WSL distribution.</span></span> <span data-ttu-id="92192-144">Ниже приводится список ее параметров.</span><span class="sxs-lookup"><span data-stu-id="92192-144">Below is a list of its options.</span></span>

<span data-ttu-id="92192-145">Использование: `wslconfig [Argument] [Options...]`</span><span class="sxs-lookup"><span data-stu-id="92192-145">Using: `wslconfig [Argument] [Options...]`</span></span>

#### <a name="arguments"></a><span data-ttu-id="92192-146">Arguments</span><span class="sxs-lookup"><span data-stu-id="92192-146">Arguments</span></span>
* <span data-ttu-id="92192-147">**/l, /list [параметры]**</span><span class="sxs-lookup"><span data-stu-id="92192-147">**/l, /list [Options]**</span></span>
  
  <span data-ttu-id="92192-148">Вывод списка зарегистрированных дистрибутивов.</span><span class="sxs-lookup"><span data-stu-id="92192-148">Lists registered distributions.</span></span>
  
  <span data-ttu-id="92192-149">Параметры:</span><span class="sxs-lookup"><span data-stu-id="92192-149">Options:</span></span>
    * <span data-ttu-id="92192-150">**/all**</span><span class="sxs-lookup"><span data-stu-id="92192-150">**/all**</span></span>
    
      <span data-ttu-id="92192-151">Дополнительный вывод списка всех дистрибутивов, включая дистрибутивы, которые сейчас устанавливаются или удаляются.</span><span class="sxs-lookup"><span data-stu-id="92192-151">Optionally list all distributions, including distributions that are currently being installed or uninstalled.</span></span>

    * <span data-ttu-id="92192-152">**/running**</span><span class="sxs-lookup"><span data-stu-id="92192-152">**/running**</span></span>
      
      <span data-ttu-id="92192-153">Вывод списка всех дистрибутивов, выполняемых в данный момент.</span><span class="sxs-lookup"><span data-stu-id="92192-153">List only distributions that are currently running.</span></span>

* <span data-ttu-id="92192-154">**/s, /setdefault \<дистрибутив>**</span><span class="sxs-lookup"><span data-stu-id="92192-154">**/s, /setdefault \<Distro>**</span></span>
  
  <span data-ttu-id="92192-155">Указание дистрибутива, используемого по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="92192-155">Sets the distribution as the default.</span></span>

* <span data-ttu-id="92192-156">**/t, /terminate \<дистрибутив>**</span><span class="sxs-lookup"><span data-stu-id="92192-156">**/t, /terminate \<Distro>**</span></span>
  
  <span data-ttu-id="92192-157">Завершение дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="92192-157">Terminates the distribution.</span></span>

* <span data-ttu-id="92192-158">**/u, /unregister \<дистрибутив>**</span><span class="sxs-lookup"><span data-stu-id="92192-158">**/u, /unregister \<Distro>**</span></span>
  
  <span data-ttu-id="92192-159">Отмена регистрации дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="92192-159">Unregisters the distribution.</span></span>
   
* <span data-ttu-id="92192-160">**/upgrade \<дистрибутив>**</span><span class="sxs-lookup"><span data-stu-id="92192-160">**/upgrade \<Distro>**</span></span>
  
  <span data-ttu-id="92192-161">Обновление дистрибутива до файловой системы WslFs.</span><span class="sxs-lookup"><span data-stu-id="92192-161">Upgrades the distribution to the WslFs file system format.</span></span>

### `bash.exe`

<span data-ttu-id="92192-162">Эта команда используется для запуска оболочки Bash.</span><span class="sxs-lookup"><span data-stu-id="92192-162">This command is used to start a bash shell.</span></span> <span data-ttu-id="92192-163">Ниже приведены параметры, которые можно использовать с этой командой.</span><span class="sxs-lookup"><span data-stu-id="92192-163">Below are the options you can use with this command.</span></span>

<span data-ttu-id="92192-164">Использование: `bash [Options...]`</span><span class="sxs-lookup"><span data-stu-id="92192-164">Using: `bash [Options...]`</span></span>

* <span data-ttu-id="92192-165">**Параметр не задан**</span><span class="sxs-lookup"><span data-stu-id="92192-165">**No Option given**</span></span>
  
  <span data-ttu-id="92192-166">Запуск оболочки Bash в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="92192-166">Launches the Bash shell in the current directory.</span></span> <span data-ttu-id="92192-167">Если оболочка Bash не установлена, автоматически запускается `lxrun /install`.</span><span class="sxs-lookup"><span data-stu-id="92192-167">If the Bash shell is not installed automatically runs `lxrun /install`</span></span>

* **~**
  
  <span data-ttu-id="92192-168">Команда `bash ~` запускает оболочку Bash в корневом каталоге пользователя.</span><span class="sxs-lookup"><span data-stu-id="92192-168">`bash ~` launches the bash shell into the user's home directory.</span></span>  <span data-ttu-id="92192-169">Это аналог команды `cd ~`.</span><span class="sxs-lookup"><span data-stu-id="92192-169">Similar to running `cd ~`.</span></span>

* <span data-ttu-id="92192-170">**-c "\<команда>"**</span><span class="sxs-lookup"><span data-stu-id="92192-170">**-c "\<command>"**</span></span>
  
  <span data-ttu-id="92192-171">Выполнение команды, вывод выходных данных и возврат в командную строку Windows.</span><span class="sxs-lookup"><span data-stu-id="92192-171">Runs the command, prints the output and exits back to the Windows command prompt.</span></span>
    
  <span data-ttu-id="92192-172">Пример: `bash -c "ls"`.</span><span class="sxs-lookup"><span data-stu-id="92192-172">Example:  `bash -c "ls"`.</span></span>

## <a name="deprecated-commands"></a><span data-ttu-id="92192-173">Нерекомендуемые команды</span><span class="sxs-lookup"><span data-stu-id="92192-173">Deprecated Commands</span></span>

<span data-ttu-id="92192-174">Команда `lxrun.exe` была первой командой, используемой для установки подсистемы Windows для Linux и управления ею.</span><span class="sxs-lookup"><span data-stu-id="92192-174">The `lxrun.exe` was the first command used to install and manage the Windows Subsystem for Linux.</span></span> <span data-ttu-id="92192-175">Она считается нерекомендуемой в Windows 10 версии 1803 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="92192-175">It is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="92192-176">С помощью команды `lxrun.exe` можно взаимодействовать с [подсистемой Windows для Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) напрямую.</span><span class="sxs-lookup"><span data-stu-id="92192-176">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="92192-177">Эти команды устанавливаются в каталог `\Windows\System32` и могут выполняться в командной строке Windows или PowerShell.</span><span class="sxs-lookup"><span data-stu-id="92192-177">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

| <span data-ttu-id="92192-178">Команда</span><span class="sxs-lookup"><span data-stu-id="92192-178">Command</span></span>                     | <span data-ttu-id="92192-179">Описание</span><span class="sxs-lookup"><span data-stu-id="92192-179">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="92192-180">Команда lxrun используется для управления экземпляром WSL.</span><span class="sxs-lookup"><span data-stu-id="92192-180">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="92192-181">Запускает процесс скачивания и установки.</span><span class="sxs-lookup"><span data-stu-id="92192-181">Starts the download and install process.</span></span> <br/> <span data-ttu-id="92192-182">Можно добавить параметр **/y** для обхода всех запросов.</span><span class="sxs-lookup"><span data-stu-id="92192-182">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="92192-183">Запрос на подтверждение будет принят автоматически, а в качестве привилегированного пользователя будет задан пользователь по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="92192-183">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="92192-184">Удаляет дистрибутив и образ Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="92192-184">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="92192-185">По умолчанию это не приводит к удалению корневого каталога пользователя Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="92192-185">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="92192-186">Можно добавить параметр **/y** для автоматического принятия запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="92192-186">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="92192-187">Параметр **/full** позволяет удалить дистрибутив вместе с корневым каталогом пользователя Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="92192-187">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="92192-188">Задает использование Bash по умолчанию для пользователя Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="92192-188">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="92192-189">Запрашивает пароль, если указанный пользователь не существует.</span><span class="sxs-lookup"><span data-stu-id="92192-189">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="92192-190">Дополнительные сведения: https://aka.ms/wslusers.</span><span class="sxs-lookup"><span data-stu-id="92192-190">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="92192-191">Параметр **/y** позволяет обойти запрос пароля.</span><span class="sxs-lookup"><span data-stu-id="92192-191">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="92192-192">Пользователь будет создан без пароля.</span><span class="sxs-lookup"><span data-stu-id="92192-192">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="92192-193">Обновляет индекс пакетов подсистемы.</span><span class="sxs-lookup"><span data-stu-id="92192-193">Updates the subsystem's package index</span></span>          |
