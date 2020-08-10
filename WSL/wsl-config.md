---
title: Управление дистрибутивами Linux
description: Список ссылок на справочные материалы и инструкции по настройке нескольких дистрибутивов Linux, работающих в подсистеме Windows для Linux.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, wsl.conf, wslconfig
ms.date: 05/12/2020
ms.topic: article
ms.openlocfilehash: b8aa740233f3ac9517744212eb7b362a18378822
ms.sourcegitcommit: 90577817a9321949da2a3971b4c78bb00f6d977f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/10/2020
ms.locfileid: "88039417"
---
# <a name="wsl-commands-and-launch-configurations"></a><span data-ttu-id="f8801-104">Команды WSL и конфигурации запуска</span><span class="sxs-lookup"><span data-stu-id="f8801-104">WSL commands and launch configurations</span></span>

## <a name="ways-to-run-wsl"></a><span data-ttu-id="f8801-105">Способы запуска WSL</span><span class="sxs-lookup"><span data-stu-id="f8801-105">Ways to run WSL</span></span>

<span data-ttu-id="f8801-106">Существует несколько способов запустить дистрибутив Linux с WSL после [установки](install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="f8801-106">There are several ways to run a Linux distribution with WSL once it's [installed](install-win10.md).</span></span>

1. <span data-ttu-id="f8801-107">Откройте дистрибутив Linux, перейдя в меню Пуск Windows и введя имя установленных дистрибутивов.</span><span class="sxs-lookup"><span data-stu-id="f8801-107">Open your Linux distribution by visiting the Windows Start menu and typing the name of your installed distributions.</span></span> <span data-ttu-id="f8801-108">Например: Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="f8801-108">For example: "Ubuntu".</span></span>
2. <span data-ttu-id="f8801-109">В командной строке Windows или PowerShell введите имя установленного дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="f8801-109">From Windows Command Prompt or PowerShell, enter the name of your installed distribution.</span></span> <span data-ttu-id="f8801-110">Пример: `ubuntu`</span><span class="sxs-lookup"><span data-stu-id="f8801-110">For example: `ubuntu`</span></span>
3. <span data-ttu-id="f8801-111">В командной строке Windows или PowerShell чтобы открыть дистрибутив Linux по умолчанию в текущей командной строке, введите: `wsl.exe` .</span><span class="sxs-lookup"><span data-stu-id="f8801-111">From Windows Command Prompt or PowerShell, to open your default Linux distribution inside your current command line, enter: `wsl.exe`.</span></span>
4. <span data-ttu-id="f8801-112">В командной строке Windows или PowerShell чтобы открыть дистрибутив Linux по умолчанию в текущей командной строке, введите: `wsl [command]` .</span><span class="sxs-lookup"><span data-stu-id="f8801-112">From Windows Command Prompt or PowerShell, to open your default Linux distribution inside your current command line, enter:`wsl [command]`.</span></span>

<span data-ttu-id="f8801-113">Применяемый метод зависит от того, что вы делаете.</span><span class="sxs-lookup"><span data-stu-id="f8801-113">Which method you should use depends on what you're doing.</span></span> <span data-ttu-id="f8801-114">Если вы открыли командную строку WSL в командной строке Windows или окне PowerShell и хотите выйти, введите команду: `exit` .</span><span class="sxs-lookup"><span data-stu-id="f8801-114">If you've opened a WSL command line within a Windows Prompt or PowerShell window and want to exit, enter the command: `exit`.</span></span>

## <a name="launch-wsl-by-distribution"></a><span data-ttu-id="f8801-115">Запуск WSL с помощью дистрибутива</span><span class="sxs-lookup"><span data-stu-id="f8801-115">Launch WSL by distribution</span></span>

<span data-ttu-id="f8801-116">При запуске дистрибутива с помощью специального приложения он запускается в собственном окне консоли.</span><span class="sxs-lookup"><span data-stu-id="f8801-116">Running a distribution using it's distro-specific application launches that distribution in it's own console window.</span></span>

![Запуск WSL из меню "Пуск"](media/start-launch.png)

<span data-ttu-id="f8801-118">Это то же самое, что нажать кнопку "Запустить" в Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="f8801-118">It is the same as clicking "Launch" in the Microsoft store.</span></span>

![Запуск WSL из Microsoft Store](media/store-launch.png)

<span data-ttu-id="f8801-120">Можно также запустить дистрибутив из командной строки, выполнив команду `[distribution].exe`.</span><span class="sxs-lookup"><span data-stu-id="f8801-120">You can also run the distribution from the command line by running `[distribution].exe`.</span></span>

<span data-ttu-id="f8801-121">Недостаток запуска дистрибутива из командной строки заключается в том, что при этом рабочим каталогом станет не текущий каталог, а корневой каталог дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="f8801-121">The disadvantage of running a distribution from the command line in this way is that it will automatically change your working directory from the current directory to the distribution's home directory.</span></span>

<span data-ttu-id="f8801-122">**Пример: (с помощью PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="f8801-122">**Example: (using PowerShell)**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> ubuntu

scooley@scooley-elmer:~$ pwd
/home/scooley
scooley@scooley-elmer:~$ exit
logout

PS C:\Users\sarah>
```

### <a name="wsl-and-wsl-command"></a><span data-ttu-id="f8801-123">Использование wsl и wsl [команда]</span><span class="sxs-lookup"><span data-stu-id="f8801-123">wsl and wsl [command]</span></span>

<span data-ttu-id="f8801-124">Лучший способ запуска WSL из командной строки — использовать `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="f8801-124">The best way to run WSL from the command line is using `wsl.exe`.</span></span>

<span data-ttu-id="f8801-125">**Пример: (с помощью PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="f8801-125">**Example: (using PowerShell)**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

<span data-ttu-id="f8801-126">Инструмент `wsl` не только сохраняет текущий рабочий каталог, но и позволяет выполнить одну команду помимо команд Windows.</span><span class="sxs-lookup"><span data-stu-id="f8801-126">Not only does `wsl` keep the current working directory in place, it lets you run a single command along side Windows commands.</span></span>

<span data-ttu-id="f8801-127">**Пример: (с помощью PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="f8801-127">**Example: (using PowerShell)**</span></span>

```console
PS C:\Users\sarah> Get-Date

Sunday, March 11, 2018 7:54:05 PM

PS C:\Users\sarah> wsl
scooley@scooley-elmer:/mnt/c/Users/sarah$ date
Sun Mar 11 19:55:47 DST 2018
scooley@scooley-elmer:/mnt/c/Users/sarah$ exit
logout

PS C:\Users\sarah> wsl date
Sun Mar 11 19:56:57 DST 2018
```

<span data-ttu-id="f8801-128">**Пример: (с помощью PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="f8801-128">**Example: (using PowerShell)**</span></span>

```console
PS C:\Users\sarah> Get-VM

Name            State CPUUsage(%) MemoryAssigned(M) Uptime   Status
----            ----- ----------- ----------------- ------   ------
Server17093     Off   0           0                 00:00:00 Opera...
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
Windows         Off   0           0                 00:00:00 Opera...


PS C:\Users\sarah> Get-VM | wsl grep "Ubuntu"
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
PS C:\Users\sarah>
```

## <a name="managing-multiple-linux-distributions"></a><span data-ttu-id="f8801-129">Управление несколькими дистрибутивами Linux</span><span class="sxs-lookup"><span data-stu-id="f8801-129">Managing multiple Linux Distributions</span></span>

<span data-ttu-id="f8801-130">В Windows 10 версии 1903 [и более поздних](ms-settings:windowsupdate)можно использовать `wsl.exe` для управления дистрибутивами в подсистеме Windows для Linux (WSL), включая список доступных дистрибутивов, настройку распределения по умолчанию и удаление дистрибутивов.</span><span class="sxs-lookup"><span data-stu-id="f8801-130">In Windows 10 Version 1903 [and later](ms-settings:windowsupdate), you can use `wsl.exe` to manage your distributions in the Windows Subsystem for Linux (WSL), including listing available distributions, setting a default distribution, and uninstalling distributions.</span></span>

<span data-ttu-id="f8801-131">Каждый дистрибутив Linux независимо управляет собственными конфигурациями.</span><span class="sxs-lookup"><span data-stu-id="f8801-131">Each Linux distribution independently manages its own configurations.</span></span> <span data-ttu-id="f8801-132">Чтобы просмотреть команды, относящиеся к определенному дистрибутиву, выполните команду `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="f8801-132">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="f8801-133">Например, `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="f8801-133">For example `ubuntu /?`.</span></span>

## <a name="list-distributions"></a><span data-ttu-id="f8801-134">Вывод списка дистрибутивов</span><span class="sxs-lookup"><span data-stu-id="f8801-134">List distributions</span></span>

<span data-ttu-id="f8801-135">`wsl -l` , `wsl --list`</span><span class="sxs-lookup"><span data-stu-id="f8801-135">`wsl -l` , `wsl --list`</span></span>  
<span data-ttu-id="f8801-136">Выводит список доступных дистрибутивов Linux, совместимых с WSL.</span><span class="sxs-lookup"><span data-stu-id="f8801-136">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="f8801-137">Если дистрибутив есть в списке, он установлен и готов к использованию.</span><span class="sxs-lookup"><span data-stu-id="f8801-137">If a distribution is listed, it's installed and ready to use.</span></span>

<span data-ttu-id="f8801-138">`wsl --list --all`Список всех дистрибутивов, включая те, которые сейчас не используются.</span><span class="sxs-lookup"><span data-stu-id="f8801-138">`wsl --list --all` Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="f8801-139">Они могут находиться в процессе установки, удаления или в неработающем состоянии.</span><span class="sxs-lookup"><span data-stu-id="f8801-139">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

<span data-ttu-id="f8801-140">`wsl --list --running`Список всех распределений, выполняемых в данный момент.</span><span class="sxs-lookup"><span data-stu-id="f8801-140">`wsl --list --running` Lists all distributions that are currently running.</span></span>

## <a name="set-a-default-distribution"></a><span data-ttu-id="f8801-141">Настройка дистрибутива по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f8801-141">Set a default distribution</span></span>

<span data-ttu-id="f8801-142">Дистрибутив по умолчанию WSL запускается при выполнении `wsl` в командной строке.</span><span class="sxs-lookup"><span data-stu-id="f8801-142">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

<span data-ttu-id="f8801-143">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="f8801-143">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span></span>

<span data-ttu-id="f8801-144">Задает для дистрибутив по умолчанию с помощью значения `<DistributionName>`.</span><span class="sxs-lookup"><span data-stu-id="f8801-144">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="f8801-145">**Пример: (с помощью PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="f8801-145">**Example: (using PowerShell)**</span></span>  
<span data-ttu-id="f8801-146">Команда `wsl -s Ubuntu` в качестве дистрибутива по умолчанию установит Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="f8801-146">`wsl -s Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="f8801-147">Теперь при выполнении `wsl npm init` эта команда будет выполняться в Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="f8801-147">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="f8801-148">Если выполнить `wsl`, откроется сеанс Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="f8801-148">If I run `wsl` it will open an Ubuntu session.</span></span>

## <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="f8801-149">Отмена регистрации и повторная установка дистрибутива</span><span class="sxs-lookup"><span data-stu-id="f8801-149">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="f8801-150">Хотя дистрибутивы Linux можно устанавливать из Microsoft Store, их невозможно удалить в Store.</span><span class="sxs-lookup"><span data-stu-id="f8801-150">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="f8801-151">С помощью WSL Config можно отменить регистрацию дистрибутивов или удалить их.</span><span class="sxs-lookup"><span data-stu-id="f8801-151">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="f8801-152">Отмена регистрации также позволяет переустановить дистрибутивы.</span><span class="sxs-lookup"><span data-stu-id="f8801-152">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="f8801-153">**Внимание!** После отмены регистрации все данные, параметры и программное обеспечение, связанные с этим распределением, будут безвозвратно утеряны.</span><span class="sxs-lookup"><span data-stu-id="f8801-153">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="f8801-154">При переустановке из Store будет установлена чистая копия дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="f8801-154">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wsl --unregister <DistributionName>`  
<span data-ttu-id="f8801-155">Отменяет регистрацию дистрибутива в WSL, чтобы его можно было переустановить или очистить.</span><span class="sxs-lookup"><span data-stu-id="f8801-155">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="f8801-156">Например: `wsl --unregister Ubuntu` приведет к удалению Ubuntu из дистрибутивов, доступных в WSL.</span><span class="sxs-lookup"><span data-stu-id="f8801-156">For example: `wsl --unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="f8801-157">При выполнении команды `wsl --list` этот дистрибутив не будет присутствовать в списке.</span><span class="sxs-lookup"><span data-stu-id="f8801-157">When I run `wsl --list` it will not be listed.</span></span>

<span data-ttu-id="f8801-158">Чтобы переустановить его, найдите этот дистрибутив в Microsoft Store и нажмите кнопку "Запустить".</span><span class="sxs-lookup"><span data-stu-id="f8801-158">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="run-as-a-specific-user"></a><span data-ttu-id="f8801-159">Выполнение от имени определенного пользователя</span><span class="sxs-lookup"><span data-stu-id="f8801-159">Run as a specific user</span></span>

<span data-ttu-id="f8801-160">`wsl -u <Username>`, `wsl --user <Username>`</span><span class="sxs-lookup"><span data-stu-id="f8801-160">`wsl -u <Username>`, `wsl --user <Username>`</span></span>

<span data-ttu-id="f8801-161">Выполняет WSL от имени указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="f8801-161">Run WSL as the specified user.</span></span> <span data-ttu-id="f8801-162">Обратите внимание на то, что этот пользователь должен существовать в дистрибутиве WSL.</span><span class="sxs-lookup"><span data-stu-id="f8801-162">Please note that user must exist inside of the WSL distribution.</span></span>

## <a name="change-the-default-user-for-a-distribution"></a><span data-ttu-id="f8801-163">Изменение пользователя по умолчанию для распределения</span><span class="sxs-lookup"><span data-stu-id="f8801-163">Change the default user for a distribution</span></span>

`<DistributionName> config --default-user <Username>`

<span data-ttu-id="f8801-164">Изменение пользователя по умолчанию, который используется для входа в дистрибутив.</span><span class="sxs-lookup"><span data-stu-id="f8801-164">Change the default user that for your distribution log-in.</span></span> <span data-ttu-id="f8801-165">Пользователь должен уже существовать в распределении, чтобы стать пользователем по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f8801-165">The user has to already exist inside the distribution in order to become the default user.</span></span> 

<span data-ttu-id="f8801-166">Например, `ubuntu config --default-user johndoe` изменит пользователя по умолчанию для дистрибутива Ubuntu на пользователя "JohnDoe".</span><span class="sxs-lookup"><span data-stu-id="f8801-166">For example: `ubuntu config --default-user johndoe` would change the default user for the Ubuntu distribution to the "johndoe" user.</span></span>

> [!NOTE]
> <span data-ttu-id="f8801-167">Если у вас возникли проблемы с определением имени дистрибутива, см. [Список дистрибутивов](https://docs.microsoft.com/windows/wsl/wsl-config#list-distributions) для команды, чтобы получить список официальных названий установленных дистрибутивов.</span><span class="sxs-lookup"><span data-stu-id="f8801-167">If you are having trouble figuring out the name of your distribution, see [List distributions](https://docs.microsoft.com/windows/wsl/wsl-config#list-distributions) for the command to list the official name of the installed distributions.</span></span> 

## <a name="run-a-specific-distribution"></a><span data-ttu-id="f8801-168">Запуск определенного дистрибутива</span><span class="sxs-lookup"><span data-stu-id="f8801-168">Run a specific distribution</span></span>

<span data-ttu-id="f8801-169">`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="f8801-169">`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`</span></span>

<span data-ttu-id="f8801-170">Запускает указанный дистрибутив WSL. Эту команду можно использовать для отправки команд в определенный дистрибутив без необходимости изменения дистрибутива по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f8801-170">Run a specified distribution of WSL, can be used to send commands to a specific distribution without having to change your default.</span></span>

## <a name="managing-multiple-linux-distributions-in-earlier-windows-versions"></a><span data-ttu-id="f8801-171">Управление несколькими дистрибутивами Linux в более ранних версиях Windows</span><span class="sxs-lookup"><span data-stu-id="f8801-171">Managing multiple Linux Distributions in earlier Windows versions</span></span>

<span data-ttu-id="f8801-172">В Windows 10 до версии 1903 программа командной строки WSL config ( `wslconfig.exe` ) должна использоваться для управления дистрибутивами Linux, работающими в подсистеме Windows для Linux (WSL).</span><span class="sxs-lookup"><span data-stu-id="f8801-172">In Windows 10 prior to version 1903, the WSL Config (`wslconfig.exe`) command-line tool should be used to manage Linux distributions running on the Windows Subsystem for Linux (WSL).</span></span>  <span data-ttu-id="f8801-173">Она позволяет получить список доступных дистрибутивов, настроить дистрибутив по умолчанию и удалить дистрибутивы.</span><span class="sxs-lookup"><span data-stu-id="f8801-173">It lets you list available distributions, set a default distribution, and uninstall distributions.</span></span>

<span data-ttu-id="f8801-174">Хотя WSL Config удобно использовать для параметров, охватывающих или координирующих несколько дистрибутивов, каждый дистрибутив Linux независимо управляет собственными конфигурациями.</span><span class="sxs-lookup"><span data-stu-id="f8801-174">While WSL Config is helpful for settings that span or coordinate distributions, each Linux distribution independently manages its own configurations.</span></span>  <span data-ttu-id="f8801-175">Чтобы просмотреть команды, относящиеся к определенному дистрибутиву, выполните команду `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="f8801-175">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="f8801-176">Например, `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="f8801-176">For example `ubuntu /?`.</span></span>

<span data-ttu-id="f8801-177">Чтобы просмотреть все доступные параметры для wslconfig, выполните команду `wslconfig /?`</span><span class="sxs-lookup"><span data-stu-id="f8801-177">To see all available options for wslconfig, run:  `wslconfig /?`</span></span>

```console
wslconfig.exe
Performs administrative operations on Windows Subsystem for Linux

Usage:
    /l, /list [/all] - Lists registered distributions.
        /all - Optionally list all distributions, including distributions that
               are currently being installed or uninstalled.
    /s, /setdefault <DistributionName> - Sets the specified distribution as the default.
    /u, /unregister <DistributionName> - Unregisters a distribution.
```

<span data-ttu-id="f8801-178">Чтобы вывести список дистрибутивов, используйте:</span><span class="sxs-lookup"><span data-stu-id="f8801-178">To list distributions, use:</span></span>

`wslconfig /list`  
<span data-ttu-id="f8801-179">Выводит список доступных дистрибутивов Linux, совместимых с WSL.</span><span class="sxs-lookup"><span data-stu-id="f8801-179">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="f8801-180">Если дистрибутив есть в списке, он установлен и готов к использованию.</span><span class="sxs-lookup"><span data-stu-id="f8801-180">If a distribution is listed, it's installed and ready to use.</span></span>

`wslconfig /list /all`  
<span data-ttu-id="f8801-181">Выводит список всех дистрибутивов, включая те, которые сейчас не используются.</span><span class="sxs-lookup"><span data-stu-id="f8801-181">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="f8801-182">Они могут находиться в процессе установки, удаления или в неработающем состоянии.</span><span class="sxs-lookup"><span data-stu-id="f8801-182">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

<span data-ttu-id="f8801-183">Настройка распределения по умолчанию, выполняемого при выполнении `wsl` в командной строке:</span><span class="sxs-lookup"><span data-stu-id="f8801-183">To set a default distribution that runs when you run `wsl` on a command line:</span></span>

<span data-ttu-id="f8801-184">`wslconfig /setdefault <DistributionName>`Задает для распределения по умолчанию значение `<DistributionName>` .</span><span class="sxs-lookup"><span data-stu-id="f8801-184">`wslconfig /setdefault <DistributionName>` Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="f8801-185">**Пример: (с помощью PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="f8801-185">**Example: (using PowerShell)**</span></span>  
<span data-ttu-id="f8801-186">Команда `wslconfig /setdefault Ubuntu` в качестве дистрибутива по умолчанию установит Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="f8801-186">`wslconfig /setdefault Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="f8801-187">Теперь при выполнении `wsl npm init` эта команда будет выполняться в Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="f8801-187">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="f8801-188">Если выполнить `wsl`, откроется сеанс Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="f8801-188">If I run `wsl` it will open an Ubuntu session.</span></span>

<span data-ttu-id="f8801-189">Чтобы отменить регистрацию и переустановить распространение, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f8801-189">To unregister and reinstall a distribution:</span></span>

`wslconfig /unregister <DistributionName>`  
<span data-ttu-id="f8801-190">Отменяет регистрацию дистрибутива в WSL, чтобы его можно было переустановить или очистить.</span><span class="sxs-lookup"><span data-stu-id="f8801-190">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="f8801-191">Например: `wslconfig /unregister Ubuntu` приведет к удалению Ubuntu из дистрибутивов, доступных в WSL.</span><span class="sxs-lookup"><span data-stu-id="f8801-191">For example: `wslconfig /unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="f8801-192">При выполнении команды `wslconfig /list` этот дистрибутив не будет присутствовать в списке.</span><span class="sxs-lookup"><span data-stu-id="f8801-192">When I run `wslconfig /list` it will not be listed.</span></span>

<span data-ttu-id="f8801-193">Чтобы переустановить его, найдите этот дистрибутив в Microsoft Store и нажмите кнопку "Запустить".</span><span class="sxs-lookup"><span data-stu-id="f8801-193">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="configure-per-distro-launch-settings-with-wslconf"></a><span data-ttu-id="f8801-194">Настройка параметров запуска дистрибутив с помощью вслконф</span><span class="sxs-lookup"><span data-stu-id="f8801-194">Configure per distro launch settings with wslconf</span></span>

> <span data-ttu-id="f8801-195">**Доступно в Windows Build 17093 и более поздних версиях**</span><span class="sxs-lookup"><span data-stu-id="f8801-195">**Available in Windows Build 17093 and later**</span></span>

<span data-ttu-id="f8801-196">Автоматическая настройка определенных функций в WSL, которые будут применяться при каждом запуске подсистемы с помощью `wsl.conf`.</span><span class="sxs-lookup"><span data-stu-id="f8801-196">Automatically configure certain functionality in WSL that will be applied every time you launch the subsystem using `wsl.conf`.</span></span>

<span data-ttu-id="f8801-197">Сейчас сюда входят параметры автоподключения и конфигурация сети.</span><span class="sxs-lookup"><span data-stu-id="f8801-197">Right now, this includes automount options and network configuration.</span></span>

<span data-ttu-id="f8801-198">Файл `wsl.conf` в каждом дистрибутиве Linux находится в папке `/etc/wsl.conf`.</span><span class="sxs-lookup"><span data-stu-id="f8801-198">`wsl.conf` is located in each Linux distribution in `/etc/wsl.conf`.</span></span> <span data-ttu-id="f8801-199">Если этот файл отсутствует, его можно создать самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="f8801-199">If the file is not there, you can create it yourself.</span></span> <span data-ttu-id="f8801-200">WSL обнаружит наличие файла и прочитает его содержимое.</span><span class="sxs-lookup"><span data-stu-id="f8801-200">WSL will detect the existence of the file and will read its contents.</span></span> <span data-ttu-id="f8801-201">Если этот файл отсутствует или имеет неправильный формат (т. е. неправильное форматирование разметки), WSL продолжит запуск в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="f8801-201">If the file is missing or malformed (that is, improper markup formatting), WSL will continue to launch as normal.</span></span>

<span data-ttu-id="f8801-202">Ниже приведен пример `wsl.conf` файла, который можно добавить в дистрибутивы.</span><span class="sxs-lookup"><span data-stu-id="f8801-202">Here is a sample `wsl.conf` file you could add into your distributions:</span></span>

```console
# Enable extra metadata options by default
[automount]
enabled = true
root = /windir/
options = "metadata,umask=22,fmask=11"
mountFsTab = false

# Enable DNS – even though these are turned on by default, we'll specify here just to be explicit.
[network]
generateHosts = true
generateResolvConf = true
```

### <a name="configuration-options"></a><span data-ttu-id="f8801-203">Параметры конфигурации</span><span class="sxs-lookup"><span data-stu-id="f8801-203">Configuration Options</span></span>

<span data-ttu-id="f8801-204">В соответствии с соглашениями об INI-файлах ключи объявляются в разделе.</span><span class="sxs-lookup"><span data-stu-id="f8801-204">In keeping with .ini conventions, keys are declared under a section.</span></span> 

<span data-ttu-id="f8801-205">WSL поддерживает два раздела: `automount` и `network`.</span><span class="sxs-lookup"><span data-stu-id="f8801-205">WSL supports two sections: `automount` and `network`.</span></span>

#### <a name="automount"></a><span data-ttu-id="f8801-206">automount</span><span class="sxs-lookup"><span data-stu-id="f8801-206">automount</span></span>

<span data-ttu-id="f8801-207">Раздел: `[automount]`</span><span class="sxs-lookup"><span data-stu-id="f8801-207">Section: `[automount]`</span></span>

| <span data-ttu-id="f8801-208">key</span><span class="sxs-lookup"><span data-stu-id="f8801-208">key</span></span>        | <span data-ttu-id="f8801-209">value</span><span class="sxs-lookup"><span data-stu-id="f8801-209">value</span></span>                          | <span data-ttu-id="f8801-210">по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f8801-210">default</span></span>      | <span data-ttu-id="f8801-211">Примечания</span><span class="sxs-lookup"><span data-stu-id="f8801-211">notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8801-212">enabled</span><span class="sxs-lookup"><span data-stu-id="f8801-212">enabled</span></span>    | <span data-ttu-id="f8801-213">Логический</span><span class="sxs-lookup"><span data-stu-id="f8801-213">boolean</span></span>                        | <span data-ttu-id="f8801-214">верно</span><span class="sxs-lookup"><span data-stu-id="f8801-214">true</span></span>         | <span data-ttu-id="f8801-215">Значение `true` обеспечивает автоматическое подключение</span><span class="sxs-lookup"><span data-stu-id="f8801-215">`true` causes fixed drives (i.e</span></span> <span data-ttu-id="f8801-216">несъемных дисков (например, `C:/` или `D:/`) DrvFs в `/mnt`.</span><span class="sxs-lookup"><span data-stu-id="f8801-216">`C:/` or `D:/`) to be automatically mounted with DrvFs under `/mnt`.</span></span>  <span data-ttu-id="f8801-217">`false`означает, что диски не будут подключены автоматически, но их можно подключать вручную или через `fstab` .</span><span class="sxs-lookup"><span data-stu-id="f8801-217">`false` means drives won't be mounted automatically, but you could still mount them manually or via `fstab`.</span></span>                                                                                                             |
| <span data-ttu-id="f8801-218">mountFsTab</span><span class="sxs-lookup"><span data-stu-id="f8801-218">mountFsTab</span></span> | <span data-ttu-id="f8801-219">Логический</span><span class="sxs-lookup"><span data-stu-id="f8801-219">boolean</span></span>                        | <span data-ttu-id="f8801-220">верно</span><span class="sxs-lookup"><span data-stu-id="f8801-220">true</span></span>         | <span data-ttu-id="f8801-221">Значение `true` задает `/etc/fstab` для обработки при запуске WSL.</span><span class="sxs-lookup"><span data-stu-id="f8801-221">`true` sets `/etc/fstab` to be processed on WSL start.</span></span> <span data-ttu-id="f8801-222">/etc/fstab — это файл, в котором можно объявлять другие файловые системы, например общий ресурс SMB.</span><span class="sxs-lookup"><span data-stu-id="f8801-222">/etc/fstab is a file where you can declare other filesystems, like an SMB share.</span></span> <span data-ttu-id="f8801-223">Поэтому вы можете автоматически подключать эти файловые системы в WSL при запуске.</span><span class="sxs-lookup"><span data-stu-id="f8801-223">Thus, you can mount these filesystems automatically in WSL on start up.</span></span>                                                                                                                |
| <span data-ttu-id="f8801-224">root</span><span class="sxs-lookup"><span data-stu-id="f8801-224">root</span></span>       | <span data-ttu-id="f8801-225">Строка</span><span class="sxs-lookup"><span data-stu-id="f8801-225">String</span></span>                         | `/mnt/`      | <span data-ttu-id="f8801-226">Задает каталог, в который будут автоматически подключены несъемные диски.</span><span class="sxs-lookup"><span data-stu-id="f8801-226">Sets the directory where fixed drives will be automatically mounted.</span></span> <span data-ttu-id="f8801-227">Например, если у вас есть каталог в WSL в `/windir/` и вы указали его в качестве корневого каталога, то ваши несъемные диски будут подключены в `/windir/c`</span><span class="sxs-lookup"><span data-stu-id="f8801-227">For example, if you have a directory in WSL at `/windir/` and you specify that as the root, you would expect to see your fixed drives mounted at `/windir/c`</span></span>                                                                                              |
| <span data-ttu-id="f8801-228">параметры</span><span class="sxs-lookup"><span data-stu-id="f8801-228">options</span></span>    | <span data-ttu-id="f8801-229">разделенный запятыми список значений</span><span class="sxs-lookup"><span data-stu-id="f8801-229">comma-separated list of values</span></span> | <span data-ttu-id="f8801-230">пустая строка</span><span class="sxs-lookup"><span data-stu-id="f8801-230">empty string</span></span> | <span data-ttu-id="f8801-231">Это значение добавляется в строку параметров подключения по умолчанию DrvFs.</span><span class="sxs-lookup"><span data-stu-id="f8801-231">This value is appended to the default DrvFs mount options string.</span></span> <span data-ttu-id="f8801-232">**Можно указать только параметры, относящиеся к DrvFs.**</span><span class="sxs-lookup"><span data-stu-id="f8801-232">**Only DrvFs-specific options can be specified.**</span></span> <span data-ttu-id="f8801-233">Параметры, которые двоичный файл подключения обычно анализирует и преобразовывает во флаг, не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="f8801-233">Options that the mount binary would normally parse into a flag are not supported.</span></span> <span data-ttu-id="f8801-234">Если вы хотите явно указать эти параметры, необходимо добавить каждый диск, для которого вы хотите это сделать, в /etc/fstab.</span><span class="sxs-lookup"><span data-stu-id="f8801-234">If you want to explicitly specify those options, you must include every drive for which you want to do so in /etc/fstab.</span></span> |

<span data-ttu-id="f8801-235">По умолчанию WSL задает для идентификаторов UID и GID значения пользователя по умолчанию (в дистрибутиве Ubuntu пользователь по умолчанию создается с идентификаторами UID = 1000 и GID = 1000).</span><span class="sxs-lookup"><span data-stu-id="f8801-235">By default, WSL sets the uid and gid to the value of the default user (in Ubuntu distro, the default user is created with uid=1000,gid=1000).</span></span> <span data-ttu-id="f8801-236">Если пользователь явно указывает параметр GID или UID с помощью этого ключа, связанное значение будет перезаписано.</span><span class="sxs-lookup"><span data-stu-id="f8801-236">If the user specifies a gid or uid option explicitly via this key, the associated value will be overwritten.</span></span> <span data-ttu-id="f8801-237">В противном случае всегда будет добавляться значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f8801-237">Otherwise, the default value will always be appended.</span></span>

<span data-ttu-id="f8801-238">**Примечание**. Эти параметры применяются в качестве параметров подключения для всех автоматически подключаемых дисков.</span><span class="sxs-lookup"><span data-stu-id="f8801-238">**Note:** These options are applied as the mount options for all automatically mounted drives.</span></span> <span data-ttu-id="f8801-239">Чтобы изменить параметры для конкретного диска, используйте /etc/fstab.</span><span class="sxs-lookup"><span data-stu-id="f8801-239">To change the options for a specific drive only, use /etc/fstab instead.</span></span>

#### <a name="mount-options"></a><span data-ttu-id="f8801-240">Параметры подключения</span><span class="sxs-lookup"><span data-stu-id="f8801-240">Mount options</span></span>

<span data-ttu-id="f8801-241">Задание различных параметров подключения для дисков Windows (DrvFs) позволяет контролировать определение разрешений для файлов Windows.</span><span class="sxs-lookup"><span data-stu-id="f8801-241">Setting different mount options for Windows drives (DrvFs) can control how file permissions are calculated for Windows files.</span></span> <span data-ttu-id="f8801-242">Доступны следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="f8801-242">The following options are available:</span></span>

| <span data-ttu-id="f8801-243">Клавиши</span><span class="sxs-lookup"><span data-stu-id="f8801-243">Key</span></span> | <span data-ttu-id="f8801-244">Описание</span><span class="sxs-lookup"><span data-stu-id="f8801-244">Description</span></span> | <span data-ttu-id="f8801-245">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f8801-245">Default</span></span> |
|:----|:----|:----|
|<span data-ttu-id="f8801-246">uid</span><span class="sxs-lookup"><span data-stu-id="f8801-246">uid</span></span>| <span data-ttu-id="f8801-247">ИД пользователя, используемый для владельца всех файлов.</span><span class="sxs-lookup"><span data-stu-id="f8801-247">The User ID used for the owner of all files</span></span> | <span data-ttu-id="f8801-248">ИД пользователя по умолчанию для дистрибутива WSL (при первой установке имеет значение по умолчанию — 1000).</span><span class="sxs-lookup"><span data-stu-id="f8801-248">The default User ID of your WSL distro (On first installation this defaults to 1000)</span></span>
|<span data-ttu-id="f8801-249">gid</span><span class="sxs-lookup"><span data-stu-id="f8801-249">gid</span></span>| <span data-ttu-id="f8801-250">Идентификатор группы, используемый для владельца всех файлов.</span><span class="sxs-lookup"><span data-stu-id="f8801-250">The Group ID used for the owner of all files</span></span> | <span data-ttu-id="f8801-251">Идентификатор группы по умолчанию для дистрибутива WSL (при первой установке имеет значение по умолчанию — 1000).</span><span class="sxs-lookup"><span data-stu-id="f8801-251">The default group ID of your WSL distro (On first installation this defaults to 1000)</span></span>
|<span data-ttu-id="f8801-252">umask</span><span class="sxs-lookup"><span data-stu-id="f8801-252">umask</span></span> | <span data-ttu-id="f8801-253">Восьмеричная маска разрешений, исключаемых для всех файлов и каталогов.</span><span class="sxs-lookup"><span data-stu-id="f8801-253">An octal mask of permissions to exclude for all files and directories</span></span> | <span data-ttu-id="f8801-254">000</span><span class="sxs-lookup"><span data-stu-id="f8801-254">000</span></span>
|<span data-ttu-id="f8801-255">fmask</span><span class="sxs-lookup"><span data-stu-id="f8801-255">fmask</span></span> | <span data-ttu-id="f8801-256">Восьмеричная маска разрешений, исключаемых для всех файлов.</span><span class="sxs-lookup"><span data-stu-id="f8801-256">An octal mask of permissions to exclude for all files</span></span> | <span data-ttu-id="f8801-257">000</span><span class="sxs-lookup"><span data-stu-id="f8801-257">000</span></span>
|<span data-ttu-id="f8801-258">dmask</span><span class="sxs-lookup"><span data-stu-id="f8801-258">dmask</span></span> | <span data-ttu-id="f8801-259">Восьмеричная маска разрешений, исключаемых для всех каталогов.</span><span class="sxs-lookup"><span data-stu-id="f8801-259">An octal mask of permissions to exclude for all directories</span></span> | <span data-ttu-id="f8801-260">000</span><span class="sxs-lookup"><span data-stu-id="f8801-260">000</span></span>

<span data-ttu-id="f8801-261">**Примечание**. Маски разрешений подвергаются логической операции ИЛИ перед применением к файлам или каталогам.</span><span class="sxs-lookup"><span data-stu-id="f8801-261">**Note:** The permission masks are put through a logical OR operation before being applied to files or directories.</span></span> 

#### <a name="network"></a><span data-ttu-id="f8801-262">сеть</span><span class="sxs-lookup"><span data-stu-id="f8801-262">network</span></span>

<span data-ttu-id="f8801-263">Метка раздела: `[network]`</span><span class="sxs-lookup"><span data-stu-id="f8801-263">Section label: `[network]`</span></span>

| <span data-ttu-id="f8801-264">key</span><span class="sxs-lookup"><span data-stu-id="f8801-264">key</span></span> | <span data-ttu-id="f8801-265">value</span><span class="sxs-lookup"><span data-stu-id="f8801-265">value</span></span> | <span data-ttu-id="f8801-266">по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f8801-266">default</span></span> | <span data-ttu-id="f8801-267">Примечания</span><span class="sxs-lookup"><span data-stu-id="f8801-267">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="f8801-268">generateHosts</span><span class="sxs-lookup"><span data-stu-id="f8801-268">generateHosts</span></span> | <span data-ttu-id="f8801-269">Логический</span><span class="sxs-lookup"><span data-stu-id="f8801-269">boolean</span></span> | `true` | <span data-ttu-id="f8801-270">Значение `true` указывает WSL создать `/etc/hosts`.</span><span class="sxs-lookup"><span data-stu-id="f8801-270">`true` sets WSL to generate `/etc/hosts`.</span></span> <span data-ttu-id="f8801-271">Файл `hosts` содержит статическую карту имен узлов и соответствующих IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="f8801-271">The `hosts` file contains a static map of hostnames corresponding IP address.</span></span> |
| <span data-ttu-id="f8801-272">generateResolvConf</span><span class="sxs-lookup"><span data-stu-id="f8801-272">generateResolvConf</span></span> | <span data-ttu-id="f8801-273">Логический</span><span class="sxs-lookup"><span data-stu-id="f8801-273">boolean</span></span> | `true` | <span data-ttu-id="f8801-274">Значение `true` указывает WSL создать `/etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="f8801-274">`true` set WSL to generate `/etc/resolv.conf`.</span></span> <span data-ttu-id="f8801-275">Файл `resolv.conf` содержит список DNS-серверов, которые способны разрешить заданное имя узла в его IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="f8801-275">The `resolv.conf` contains a DNS list that are capable of resolving a given hostname to its IP address.</span></span> | 

#### <a name="interop"></a><span data-ttu-id="f8801-276">interop</span><span class="sxs-lookup"><span data-stu-id="f8801-276">interop</span></span>

<span data-ttu-id="f8801-277">Метка раздела: `[interop]`</span><span class="sxs-lookup"><span data-stu-id="f8801-277">Section label: `[interop]`</span></span>

<span data-ttu-id="f8801-278">Эти параметры доступны в выпусках для программы предварительной оценки, начиная со сборки 17713.</span><span class="sxs-lookup"><span data-stu-id="f8801-278">These options are available in Insider Build 17713 and later.</span></span>

| <span data-ttu-id="f8801-279">key</span><span class="sxs-lookup"><span data-stu-id="f8801-279">key</span></span> | <span data-ttu-id="f8801-280">value</span><span class="sxs-lookup"><span data-stu-id="f8801-280">value</span></span> | <span data-ttu-id="f8801-281">по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f8801-281">default</span></span> | <span data-ttu-id="f8801-282">Примечания</span><span class="sxs-lookup"><span data-stu-id="f8801-282">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="f8801-283">enabled</span><span class="sxs-lookup"><span data-stu-id="f8801-283">enabled</span></span> | <span data-ttu-id="f8801-284">Логический</span><span class="sxs-lookup"><span data-stu-id="f8801-284">boolean</span></span> | `true` | <span data-ttu-id="f8801-285">Установка этого ключа определяет, будет ли WSL поддерживать запуск процессов Windows.</span><span class="sxs-lookup"><span data-stu-id="f8801-285">Setting this key will determine whether WSL will support launching Windows processes.</span></span> |
| <span data-ttu-id="f8801-286">appendWindowsPath</span><span class="sxs-lookup"><span data-stu-id="f8801-286">appendWindowsPath</span></span> | <span data-ttu-id="f8801-287">Логический</span><span class="sxs-lookup"><span data-stu-id="f8801-287">boolean</span></span> | `true` | <span data-ttu-id="f8801-288">Задание этого ключа определяет, будет ли WSL добавлять элементы пути Windows в переменную среды $PATH.</span><span class="sxs-lookup"><span data-stu-id="f8801-288">Setting this key will determine whether WSL will add Windows path elements to the $PATH environment variable.</span></span> |

#### <a name="user"></a><span data-ttu-id="f8801-289">пользователь</span><span class="sxs-lookup"><span data-stu-id="f8801-289">user</span></span>

<span data-ttu-id="f8801-290">Метка раздела: `[user]`</span><span class="sxs-lookup"><span data-stu-id="f8801-290">Section label: `[user]`</span></span>

<span data-ttu-id="f8801-291">Эти параметры доступны в сборках 18980 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="f8801-291">These options are available in Build 18980 and later.</span></span>

| <span data-ttu-id="f8801-292">ключ</span><span class="sxs-lookup"><span data-stu-id="f8801-292">key</span></span> | <span data-ttu-id="f8801-293">value</span><span class="sxs-lookup"><span data-stu-id="f8801-293">value</span></span> | <span data-ttu-id="f8801-294">default</span><span class="sxs-lookup"><span data-stu-id="f8801-294">default</span></span> | <span data-ttu-id="f8801-295">HDInsight</span><span class="sxs-lookup"><span data-stu-id="f8801-295">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="f8801-296">default</span><span class="sxs-lookup"><span data-stu-id="f8801-296">default</span></span> | <span data-ttu-id="f8801-297">строка</span><span class="sxs-lookup"><span data-stu-id="f8801-297">string</span></span> | <span data-ttu-id="f8801-298">Начальное имя пользователя, созданное при первом запуске</span><span class="sxs-lookup"><span data-stu-id="f8801-298">The initial username created on first run</span></span> | <span data-ttu-id="f8801-299">Задание этого параметра указывает, какой пользователь будет запускать, как при первом запуске сеанса WSL.</span><span class="sxs-lookup"><span data-stu-id="f8801-299">Setting this key specifies which user to run as when first starting a WSL session.</span></span> |

## <a name="configure-global-options-with-wslconfig"></a><span data-ttu-id="f8801-300">Настройка глобальных параметров с помощью. вслконфиг</span><span class="sxs-lookup"><span data-stu-id="f8801-300">Configure global options with .wslconfig</span></span>

> <span data-ttu-id="f8801-301">**Доступно в Windows Build 19041 и более поздних версиях**</span><span class="sxs-lookup"><span data-stu-id="f8801-301">**Available in Windows Build 19041 and later**</span></span>

<span data-ttu-id="f8801-302">Вы можете настроить глобальные параметры WSL, поместив `.wslconfig` файл в корневой каталог папки "Пользователи": `C:\Users\<yourUserName>\.wslconfig` .</span><span class="sxs-lookup"><span data-stu-id="f8801-302">You can configure global WSL options by placing a `.wslconfig` file into the root directory of your users folder: `C:\Users\<yourUserName>\.wslconfig`.</span></span> <span data-ttu-id="f8801-303">Многие из этих файлов связаны с WSL 2. Помните, что для `wsl --shutdown` завершения работы виртуальной машины WSL 2 может потребоваться запустить, а затем перезапустить экземпляр WSL, чтобы эти изменения вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="f8801-303">Many of these files are related to WSL 2, please keep in mind you may need to run `wsl --shutdown` to shut down the WSL 2 VM and then restart your WSL instance for these changes to take affect.</span></span>

<span data-ttu-id="f8801-304">Ниже приведен пример файла. вслконфиг:</span><span class="sxs-lookup"><span data-stu-id="f8801-304">Here is a sample .wslconfig file:</span></span>

```console
[wsl2]
kernel=C:\\temp\\myCustomKernel
memory=4GB # Limits VM memory in WSL 2 to 4 GB
processors=2 # Makes the WSL 2 VM use two virtual processors
```

<span data-ttu-id="f8801-305">Этот файл может содержать следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="f8801-305">This file can contain the following options:</span></span>

### <a name="wsl-2-settings"></a><span data-ttu-id="f8801-306">Параметры WSL 2</span><span class="sxs-lookup"><span data-stu-id="f8801-306">WSL 2 Settings</span></span>

<span data-ttu-id="f8801-307">Метка раздела: `[wsl2]`</span><span class="sxs-lookup"><span data-stu-id="f8801-307">Section label: `[wsl2]`</span></span>

<span data-ttu-id="f8801-308">Эти параметры влияют на виртуальную машину, на которой распространяется любое WSL 2.</span><span class="sxs-lookup"><span data-stu-id="f8801-308">These settings affect the VM that powers any WSL 2 distribution.</span></span>

| <span data-ttu-id="f8801-309">ключ</span><span class="sxs-lookup"><span data-stu-id="f8801-309">key</span></span> | <span data-ttu-id="f8801-310">value</span><span class="sxs-lookup"><span data-stu-id="f8801-310">value</span></span> | <span data-ttu-id="f8801-311">default</span><span class="sxs-lookup"><span data-stu-id="f8801-311">default</span></span> | <span data-ttu-id="f8801-312">HDInsight</span><span class="sxs-lookup"><span data-stu-id="f8801-312">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="f8801-313">ядро</span><span class="sxs-lookup"><span data-stu-id="f8801-313">kernel</span></span> | <span data-ttu-id="f8801-314">строка</span><span class="sxs-lookup"><span data-stu-id="f8801-314">string</span></span> | <span data-ttu-id="f8801-315">Входящие в состав ядра Microsoft</span><span class="sxs-lookup"><span data-stu-id="f8801-315">The Microsoft built kernel provided inbox</span></span> | <span data-ttu-id="f8801-316">Абсолютный путь Windows к пользовательскому ядру Linux.</span><span class="sxs-lookup"><span data-stu-id="f8801-316">An absolute Windows path to a custom Linux kernel.</span></span> |
| <span data-ttu-id="f8801-317">Память</span><span class="sxs-lookup"><span data-stu-id="f8801-317">memory</span></span> | <span data-ttu-id="f8801-318">размер;</span><span class="sxs-lookup"><span data-stu-id="f8801-318">size</span></span> | <span data-ttu-id="f8801-319">80% общего объема памяти в Windows \*</span><span class="sxs-lookup"><span data-stu-id="f8801-319">80% of your total memory on Windows \*</span></span> | <span data-ttu-id="f8801-320">Объем памяти, назначаемый виртуальной машине WSL 2.</span><span class="sxs-lookup"><span data-stu-id="f8801-320">How much memory to assign to the WSL 2 VM.</span></span> |
| <span data-ttu-id="f8801-321">обработчики</span><span class="sxs-lookup"><span data-stu-id="f8801-321">processors</span></span> | <span data-ttu-id="f8801-322">число</span><span class="sxs-lookup"><span data-stu-id="f8801-322">number</span></span> | <span data-ttu-id="f8801-323">Одинаковое число процессоров в Windows</span><span class="sxs-lookup"><span data-stu-id="f8801-323">The same number of processors on Windows</span></span> | <span data-ttu-id="f8801-324">Количество процессоров, назначаемых виртуальной машине WSL 2.</span><span class="sxs-lookup"><span data-stu-id="f8801-324">How many processors to assign to the WSL 2 VM.</span></span> |
| <span data-ttu-id="f8801-325">локалхостфорвардинг</span><span class="sxs-lookup"><span data-stu-id="f8801-325">localhostForwarding</span></span> | <span data-ttu-id="f8801-326">Логическое</span><span class="sxs-lookup"><span data-stu-id="f8801-326">boolean</span></span> | `true` | <span data-ttu-id="f8801-327">Логическое значение, указывающее, должны ли порты, привязанные к подстановочным знакам или localhost на виртуальной машине WSL 2, подключаться с узла через порт localhost:.</span><span class="sxs-lookup"><span data-stu-id="f8801-327">Boolean specifying if ports bound to wildcard or localhost in the WSL 2 VM should be connectable from the host via localhost:port.</span></span> |
| <span data-ttu-id="f8801-328">кернелкоммандлине</span><span class="sxs-lookup"><span data-stu-id="f8801-328">kernelCommandLine</span></span> | <span data-ttu-id="f8801-329">строка</span><span class="sxs-lookup"><span data-stu-id="f8801-329">string</span></span> | <span data-ttu-id="f8801-330">Пустое</span><span class="sxs-lookup"><span data-stu-id="f8801-330">Blank</span></span> | <span data-ttu-id="f8801-331">Дополнительные аргументы командной строки ядра.</span><span class="sxs-lookup"><span data-stu-id="f8801-331">Additional kernel command line arguments.</span></span> |
| <span data-ttu-id="f8801-332">swap</span><span class="sxs-lookup"><span data-stu-id="f8801-332">swap</span></span> | <span data-ttu-id="f8801-333">размер;</span><span class="sxs-lookup"><span data-stu-id="f8801-333">size</span></span> | <span data-ttu-id="f8801-334">25% размера памяти в Windows округляется до ближайших ГБ</span><span class="sxs-lookup"><span data-stu-id="f8801-334">25% of memory size on Windows rounded up to the nearest GB</span></span> | <span data-ttu-id="f8801-335">Объем пространства подкачки для добавления в виртуальную машину WSL 2, 0 для файла подкачки.</span><span class="sxs-lookup"><span data-stu-id="f8801-335">How much swap space to add to the WSL 2 VM, 0 for no swap file.</span></span> |
| <span data-ttu-id="f8801-336">Файл подкачки</span><span class="sxs-lookup"><span data-stu-id="f8801-336">swapFile</span></span> | <span data-ttu-id="f8801-337">строка</span><span class="sxs-lookup"><span data-stu-id="f8801-337">string</span></span> | <span data-ttu-id="f8801-338">%усерпрофиле%\аппдата\локал\темп\свап.вхдкс</span><span class="sxs-lookup"><span data-stu-id="f8801-338">%USERPROFILE%\AppData\Local\Temp\swap.vhdx</span></span> | <span data-ttu-id="f8801-339">Абсолютный путь Windows к виртуальному жесткому диску для переключения.</span><span class="sxs-lookup"><span data-stu-id="f8801-339">An absolute Windows path to the swap virtual hard disk.</span></span> |

* <span data-ttu-id="f8801-340">Примечание. это значение true для Windows Build 19041 и может отличаться в сборках Windows в программе "предварительные оценки"</span><span class="sxs-lookup"><span data-stu-id="f8801-340">Note: This value is true for Windows Build 19041 and may be different in Windows builds in the Insiders program</span></span>

<span data-ttu-id="f8801-341">Записи со `path` значением должны быть путями Windows с escape-символами обратной косой черты, например:`C:\\Temp\\myCustomKernel`</span><span class="sxs-lookup"><span data-stu-id="f8801-341">Entries with the `path` value must be Windows paths with escaped backslashes, e.g: `C:\\Temp\\myCustomKernel`</span></span>

<span data-ttu-id="f8801-342">Записи со `size` значением должны быть размером, за которым следует единица, например `8GB` или `512MB` .</span><span class="sxs-lookup"><span data-stu-id="f8801-342">Entries with the `size` value must be a size followed by a unit, for example `8GB` or `512MB`.</span></span>
