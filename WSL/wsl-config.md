---
title: Управление дистрибутивами Linux
description: Список ссылок на справочные материалы и инструкции по настройке нескольких дистрибутивов Linux, работающих в подсистеме Windows для Linux.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, wsl.conf, wslconfig
ms.date: 05/12/2020
ms.topic: article
ms.openlocfilehash: 59419919be138a20ab57e1a6d26a411e1531bf9f
ms.sourcegitcommit: 3fb40fd65b34a5eb26b213a0df6a3b2746b7a9b4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2020
ms.locfileid: "83235902"
---
# <a name="wsl-commands-and-launch-configurations"></a><span data-ttu-id="b35c6-104">Команды WSL и конфигурации запуска</span><span class="sxs-lookup"><span data-stu-id="b35c6-104">WSL commands and launch configurations</span></span>

## <a name="ways-to-run-wsl"></a><span data-ttu-id="b35c6-105">Способы запуска WSL</span><span class="sxs-lookup"><span data-stu-id="b35c6-105">Ways to run WSL</span></span>

<span data-ttu-id="b35c6-106">Существует несколько способов запустить дистрибутив Linux с WSL после [установки](install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="b35c6-106">There are several ways to run a Linux distribution with WSL once it's [installed](install-win10.md).</span></span>

1. <span data-ttu-id="b35c6-107">Откройте дистрибутив Linux, перейдя в меню Пуск Windows и введя имя установленных дистрибутивов.</span><span class="sxs-lookup"><span data-stu-id="b35c6-107">Open your Linux distribution by visiting the Windows Start menu and typing the name of your installed distributions.</span></span> <span data-ttu-id="b35c6-108">Например: Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="b35c6-108">For example: "Ubuntu".</span></span>
2. <span data-ttu-id="b35c6-109">В командной строке Windows или PowerShell введите имя установленного дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="b35c6-109">From Windows Command Prompt or PowerShell, enter the name of your installed distribution.</span></span> <span data-ttu-id="b35c6-110">Например: `ubuntu`</span><span class="sxs-lookup"><span data-stu-id="b35c6-110">For example: `ubuntu`</span></span>
3. <span data-ttu-id="b35c6-111">В командной строке Windows или PowerShell чтобы открыть дистрибутив Linux по умолчанию в текущей командной строке, введите: `wsl.exe` .</span><span class="sxs-lookup"><span data-stu-id="b35c6-111">From Windows Command Prompt or PowerShell, to open your default Linux distribution inside your current command line, enter: `wsl.exe`.</span></span>
4. <span data-ttu-id="b35c6-112">В командной строке Windows или PowerShell чтобы открыть дистрибутив Linux по умолчанию в текущей командной строке, введите: `wsl [command]` .</span><span class="sxs-lookup"><span data-stu-id="b35c6-112">From Windows Command Prompt or PowerShell, to open your default Linux distribution inside your current command line, enter:`wsl [command]`.</span></span>

<span data-ttu-id="b35c6-113">Применяемый метод зависит от того, что вы делаете.</span><span class="sxs-lookup"><span data-stu-id="b35c6-113">Which method you should use depends on what you're doing.</span></span> <span data-ttu-id="b35c6-114">Если вы открыли командную строку WSL в командной строке Windows или окне PowerShell и хотите выйти, введите команду: `exit` .</span><span class="sxs-lookup"><span data-stu-id="b35c6-114">If you've opened a WSL command line within a Windows Prompt or PowerShell window and want to exit, enter the command: `exit`.</span></span>

## <a name="launch-wsl-by-distribution"></a><span data-ttu-id="b35c6-115">Запуск WSL с помощью дистрибутива</span><span class="sxs-lookup"><span data-stu-id="b35c6-115">Launch WSL by distribution</span></span>

<span data-ttu-id="b35c6-116">При запуске дистрибутива с помощью специального приложения он запускается в собственном окне консоли.</span><span class="sxs-lookup"><span data-stu-id="b35c6-116">Running a distribution using it's distro-specific application launches that distribution in it's own console window.</span></span>

![Запуск WSL из меню "Пуск"](media/start-launch.png)

<span data-ttu-id="b35c6-118">Это то же самое, что нажать кнопку "Запустить" в Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="b35c6-118">It is the same as clicking "Launch" in the Microsoft store.</span></span>

![Запуск WSL из Microsoft Store](media/store-launch.png)

<span data-ttu-id="b35c6-120">Можно также запустить дистрибутив из командной строки, выполнив команду `[distribution].exe`.</span><span class="sxs-lookup"><span data-stu-id="b35c6-120">You can also run the distribution from the command line by running `[distribution].exe`.</span></span>

<span data-ttu-id="b35c6-121">Недостаток запуска дистрибутива из командной строки заключается в том, что при этом рабочим каталогом станет не текущий каталог, а корневой каталог дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="b35c6-121">The disadvantage of running a distribution from the command line in this way is that it will automatically change your working directory from the current directory to the distribution's home directory.</span></span>

<span data-ttu-id="b35c6-122">**Пример: (с помощью PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="b35c6-122">**Example: (using PowerShell)**</span></span>

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

### <a name="wsl-and-wsl-command"></a><span data-ttu-id="b35c6-123">Использование wsl и wsl [команда]</span><span class="sxs-lookup"><span data-stu-id="b35c6-123">wsl and wsl [command]</span></span>

<span data-ttu-id="b35c6-124">Лучший способ запуска WSL из командной строки — использовать `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="b35c6-124">The best way to run WSL from the command line is using `wsl.exe`.</span></span>

<span data-ttu-id="b35c6-125">**Пример: (с помощью PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="b35c6-125">**Example: (using PowerShell)**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

<span data-ttu-id="b35c6-126">Инструмент `wsl` не только сохраняет текущий рабочий каталог, но и позволяет выполнить одну команду помимо команд Windows.</span><span class="sxs-lookup"><span data-stu-id="b35c6-126">Not only does `wsl` keep the current working directory in place, it lets you run a single command along side Windows commands.</span></span>

<span data-ttu-id="b35c6-127">**Пример: (с помощью PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="b35c6-127">**Example: (using PowerShell)**</span></span>

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

<span data-ttu-id="b35c6-128">**Пример: (с помощью PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="b35c6-128">**Example: (using PowerShell)**</span></span>

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

## <a name="managing-multiple-linux-distributions"></a><span data-ttu-id="b35c6-129">Управление несколькими дистрибутивами Linux</span><span class="sxs-lookup"><span data-stu-id="b35c6-129">Managing multiple Linux Distributions</span></span>

<span data-ttu-id="b35c6-130">В Windows 10 версии 1903 [и более поздних](ms-settings:windowsupdate)можно использовать `wsl.exe` для управления дистрибутивами в подсистеме Windows для Linux (WSL), включая список доступных дистрибутивов, настройку распределения по умолчанию и удаление дистрибутивов.</span><span class="sxs-lookup"><span data-stu-id="b35c6-130">In Windows 10 Version 1903 [and later](ms-settings:windowsupdate), you can use `wsl.exe` to manage your distributions in the Windows Subsystem for Linux (WSL), including listing available distributions, setting a default distribution, and uninstalling distributions.</span></span>

<span data-ttu-id="b35c6-131">Каждый дистрибутив Linux независимо управляет собственными конфигурациями.</span><span class="sxs-lookup"><span data-stu-id="b35c6-131">Each Linux distribution independently manages its own configurations.</span></span> <span data-ttu-id="b35c6-132">Чтобы просмотреть команды, относящиеся к определенному дистрибутиву, выполните команду `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="b35c6-132">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="b35c6-133">Например, `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="b35c6-133">For example `ubuntu /?`.</span></span>

## <a name="list-distributions"></a><span data-ttu-id="b35c6-134">Вывод списка дистрибутивов</span><span class="sxs-lookup"><span data-stu-id="b35c6-134">List distributions</span></span>

<span data-ttu-id="b35c6-135">`wsl -l` , `wsl --list`</span><span class="sxs-lookup"><span data-stu-id="b35c6-135">`wsl -l` , `wsl --list`</span></span>  
<span data-ttu-id="b35c6-136">Выводит список доступных дистрибутивов Linux, совместимых с WSL.</span><span class="sxs-lookup"><span data-stu-id="b35c6-136">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="b35c6-137">Если дистрибутив есть в списке, он установлен и готов к использованию.</span><span class="sxs-lookup"><span data-stu-id="b35c6-137">If a distribution is listed, it's installed and ready to use.</span></span>

<span data-ttu-id="b35c6-138">`wsl --list --all`Список всех дистрибутивов, включая те, которые сейчас не используются.</span><span class="sxs-lookup"><span data-stu-id="b35c6-138">`wsl --list --all` Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="b35c6-139">Они могут находиться в процессе установки, удаления или в неработающем состоянии.</span><span class="sxs-lookup"><span data-stu-id="b35c6-139">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

<span data-ttu-id="b35c6-140">`wsl --list --running`Список всех распределений, выполняемых в данный момент.</span><span class="sxs-lookup"><span data-stu-id="b35c6-140">`wsl --list --running` Lists all distributions that are currently running.</span></span>

## <a name="set-a-default-distribution"></a><span data-ttu-id="b35c6-141">Настройка дистрибутива по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b35c6-141">Set a default distribution</span></span>

<span data-ttu-id="b35c6-142">Дистрибутив по умолчанию WSL запускается при выполнении `wsl` в командной строке.</span><span class="sxs-lookup"><span data-stu-id="b35c6-142">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

<span data-ttu-id="b35c6-143">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="b35c6-143">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span></span>

<span data-ttu-id="b35c6-144">Задает для дистрибутив по умолчанию с помощью значения `<DistributionName>`.</span><span class="sxs-lookup"><span data-stu-id="b35c6-144">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="b35c6-145">**Пример: (с помощью PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="b35c6-145">**Example: (using PowerShell)**</span></span>  
<span data-ttu-id="b35c6-146">Команда `wsl -s Ubuntu` в качестве дистрибутива по умолчанию установит Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="b35c6-146">`wsl -s Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="b35c6-147">Теперь при выполнении `wsl npm init` эта команда будет выполняться в Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="b35c6-147">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="b35c6-148">Если выполнить `wsl`, откроется сеанс Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="b35c6-148">If I run `wsl` it will open an Ubuntu session.</span></span>

## <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="b35c6-149">Отмена регистрации и повторная установка дистрибутива</span><span class="sxs-lookup"><span data-stu-id="b35c6-149">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="b35c6-150">Хотя дистрибутивы Linux можно устанавливать из Microsoft Store, их невозможно удалить в Store.</span><span class="sxs-lookup"><span data-stu-id="b35c6-150">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="b35c6-151">С помощью WSL Config можно отменить регистрацию дистрибутивов или удалить их.</span><span class="sxs-lookup"><span data-stu-id="b35c6-151">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="b35c6-152">Отмена регистрации также позволяет переустановить дистрибутивы.</span><span class="sxs-lookup"><span data-stu-id="b35c6-152">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="b35c6-153">**Внимание!** После отмены регистрации все данные, параметры и программное обеспечение, связанные с этим распределением, будут безвозвратно утеряны.</span><span class="sxs-lookup"><span data-stu-id="b35c6-153">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="b35c6-154">При переустановке из Store будет установлена чистая копия дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="b35c6-154">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wsl --unregister <DistributionName>`  
<span data-ttu-id="b35c6-155">Отменяет регистрацию дистрибутива в WSL, чтобы его можно было переустановить или очистить.</span><span class="sxs-lookup"><span data-stu-id="b35c6-155">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="b35c6-156">Например: `wsl --unregister Ubuntu` приведет к удалению Ubuntu из дистрибутивов, доступных в WSL.</span><span class="sxs-lookup"><span data-stu-id="b35c6-156">For example: `wsl --unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="b35c6-157">При выполнении команды `wsl --list` этот дистрибутив не будет присутствовать в списке.</span><span class="sxs-lookup"><span data-stu-id="b35c6-157">When I run `wsl --list` it will not be listed.</span></span>

<span data-ttu-id="b35c6-158">Чтобы переустановить его, найдите этот дистрибутив в Microsoft Store и нажмите кнопку "Запустить".</span><span class="sxs-lookup"><span data-stu-id="b35c6-158">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="run-as-a-specific-user"></a><span data-ttu-id="b35c6-159">Выполнение от имени определенного пользователя</span><span class="sxs-lookup"><span data-stu-id="b35c6-159">Run as a specific user</span></span>

<span data-ttu-id="b35c6-160">`wsl -u <Username>`, `wsl --user <Username>`</span><span class="sxs-lookup"><span data-stu-id="b35c6-160">`wsl -u <Username>`, `wsl --user <Username>`</span></span>

<span data-ttu-id="b35c6-161">Выполняет WSL от имени указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="b35c6-161">Run WSL as the specified user.</span></span> <span data-ttu-id="b35c6-162">Обратите внимание на то, что этот пользователь должен существовать в дистрибутиве WSL.</span><span class="sxs-lookup"><span data-stu-id="b35c6-162">Please note that user must exist inside of the WSL distribution.</span></span>

## <a name="run-a-specific-distribution"></a><span data-ttu-id="b35c6-163">Запуск определенного дистрибутива</span><span class="sxs-lookup"><span data-stu-id="b35c6-163">Run a specific distribution</span></span>

<span data-ttu-id="b35c6-164">`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="b35c6-164">`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`</span></span>

<span data-ttu-id="b35c6-165">Запускает указанный дистрибутив WSL. Эту команду можно использовать для отправки команд в определенный дистрибутив без необходимости изменения дистрибутива по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b35c6-165">Run a specified distribution of WSL, can be used to send commands to a specific distribution without having to change your default.</span></span>

## <a name="managing-multiple-linux-distributions-in-earlier-windows-versions"></a><span data-ttu-id="b35c6-166">Управление несколькими дистрибутивами Linux в более ранних версиях Windows</span><span class="sxs-lookup"><span data-stu-id="b35c6-166">Managing multiple Linux Distributions in earlier Windows versions</span></span>

<span data-ttu-id="b35c6-167">В Windows 10 до версии 1903 программа командной строки WSL config ( `wslconfig.exe` ) должна использоваться для управления дистрибутивами Linux, работающими в подсистеме Windows для Linux (WSL).</span><span class="sxs-lookup"><span data-stu-id="b35c6-167">In Windows 10 prior to version 1903, the WSL Config (`wslconfig.exe`) command-line tool should be used to manage Linux distributions running on the Windows Subsystem for Linux (WSL).</span></span>  <span data-ttu-id="b35c6-168">Она позволяет получить список доступных дистрибутивов, настроить дистрибутив по умолчанию и удалить дистрибутивы.</span><span class="sxs-lookup"><span data-stu-id="b35c6-168">It lets you list available distributions, set a default distribution, and uninstall distributions.</span></span>

<span data-ttu-id="b35c6-169">Хотя WSL Config удобно использовать для параметров, охватывающих или координирующих несколько дистрибутивов, каждый дистрибутив Linux независимо управляет собственными конфигурациями.</span><span class="sxs-lookup"><span data-stu-id="b35c6-169">While WSL Config is helpful for settings that span or coordinate distributions, each Linux distribution independently manages its own configurations.</span></span>  <span data-ttu-id="b35c6-170">Чтобы просмотреть команды, относящиеся к определенному дистрибутиву, выполните команду `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="b35c6-170">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="b35c6-171">Например, `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="b35c6-171">For example `ubuntu /?`.</span></span>

<span data-ttu-id="b35c6-172">Чтобы просмотреть все доступные параметры для wslconfig, выполните команду `wslconfig /?`</span><span class="sxs-lookup"><span data-stu-id="b35c6-172">To see all available options for wslconfig, run:  `wslconfig /?`</span></span>

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

<span data-ttu-id="b35c6-173">Чтобы вывести список дистрибутивов, используйте:</span><span class="sxs-lookup"><span data-stu-id="b35c6-173">To list distributions, use:</span></span>

`wslconfig /list`  
<span data-ttu-id="b35c6-174">Выводит список доступных дистрибутивов Linux, совместимых с WSL.</span><span class="sxs-lookup"><span data-stu-id="b35c6-174">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="b35c6-175">Если дистрибутив есть в списке, он установлен и готов к использованию.</span><span class="sxs-lookup"><span data-stu-id="b35c6-175">If a distribution is listed, it's installed and ready to use.</span></span>

`wslconfig /list /all`  
<span data-ttu-id="b35c6-176">Выводит список всех дистрибутивов, включая те, которые сейчас не используются.</span><span class="sxs-lookup"><span data-stu-id="b35c6-176">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="b35c6-177">Они могут находиться в процессе установки, удаления или в неработающем состоянии.</span><span class="sxs-lookup"><span data-stu-id="b35c6-177">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

<span data-ttu-id="b35c6-178">Настройка распределения по умолчанию, выполняемого при выполнении `wsl` в командной строке:</span><span class="sxs-lookup"><span data-stu-id="b35c6-178">To set a default distribution that runs when you run `wsl` on a command line:</span></span>

<span data-ttu-id="b35c6-179">`wslconfig /setdefault <DistributionName>`Задает для распределения по умолчанию значение `<DistributionName>` .</span><span class="sxs-lookup"><span data-stu-id="b35c6-179">`wslconfig /setdefault <DistributionName>` Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="b35c6-180">**Пример: (с помощью PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="b35c6-180">**Example: (using PowerShell)**</span></span>  
<span data-ttu-id="b35c6-181">Команда `wslconfig /setdefault Ubuntu` в качестве дистрибутива по умолчанию установит Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="b35c6-181">`wslconfig /setdefault Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="b35c6-182">Теперь при выполнении `wsl npm init` эта команда будет выполняться в Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="b35c6-182">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="b35c6-183">Если выполнить `wsl`, откроется сеанс Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="b35c6-183">If I run `wsl` it will open an Ubuntu session.</span></span>

<span data-ttu-id="b35c6-184">Чтобы отменить регистрацию и переустановить распространение, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b35c6-184">To unregister and reinstall a distribution:</span></span>

`wslconfig /unregister <DistributionName>`  
<span data-ttu-id="b35c6-185">Отменяет регистрацию дистрибутива в WSL, чтобы его можно было переустановить или очистить.</span><span class="sxs-lookup"><span data-stu-id="b35c6-185">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="b35c6-186">Например: `wslconfig /unregister Ubuntu` приведет к удалению Ubuntu из дистрибутивов, доступных в WSL.</span><span class="sxs-lookup"><span data-stu-id="b35c6-186">For example: `wslconfig /unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="b35c6-187">При выполнении команды `wslconfig /list` этот дистрибутив не будет присутствовать в списке.</span><span class="sxs-lookup"><span data-stu-id="b35c6-187">When I run `wslconfig /list` it will not be listed.</span></span>

<span data-ttu-id="b35c6-188">Чтобы переустановить его, найдите этот дистрибутив в Microsoft Store и нажмите кнопку "Запустить".</span><span class="sxs-lookup"><span data-stu-id="b35c6-188">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="configure-per-distro-launch-settings-with-wslconf"></a><span data-ttu-id="b35c6-189">Настройка параметров запуска дистрибутив с помощью вслконф</span><span class="sxs-lookup"><span data-stu-id="b35c6-189">Configure per distro launch settings with wslconf</span></span>

> <span data-ttu-id="b35c6-190">**Доступно в Windows Build 17093 и более поздних версиях**</span><span class="sxs-lookup"><span data-stu-id="b35c6-190">**Available in Windows Build 17093 and later**</span></span>

<span data-ttu-id="b35c6-191">Автоматическая настройка определенных функций в WSL, которые будут применяться при каждом запуске подсистемы с помощью `wsl.conf`.</span><span class="sxs-lookup"><span data-stu-id="b35c6-191">Automatically configure certain functionality in WSL that will be applied every time you launch the subsystem using `wsl.conf`.</span></span>

<span data-ttu-id="b35c6-192">Сейчас сюда входят параметры автоподключения и конфигурация сети.</span><span class="sxs-lookup"><span data-stu-id="b35c6-192">Right now, this includes automount options and network configuration.</span></span>

<span data-ttu-id="b35c6-193">Файл `wsl.conf` в каждом дистрибутиве Linux находится в папке `/etc/wsl.conf`.</span><span class="sxs-lookup"><span data-stu-id="b35c6-193">`wsl.conf` is located in each Linux distribution in `/etc/wsl.conf`.</span></span> <span data-ttu-id="b35c6-194">Если этот файл отсутствует, его можно создать самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="b35c6-194">If the file is not there, you can create it yourself.</span></span> <span data-ttu-id="b35c6-195">WSL обнаружит наличие файла и прочитает его содержимое.</span><span class="sxs-lookup"><span data-stu-id="b35c6-195">WSL will detect the existence of the file and will read its contents.</span></span> <span data-ttu-id="b35c6-196">Если этот файл отсутствует или имеет неправильный формат (т. е. неправильное форматирование разметки), WSL продолжит запуск в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="b35c6-196">If the file is missing or malformed (that is, improper markup formatting), WSL will continue to launch as normal.</span></span>

<span data-ttu-id="b35c6-197">Ниже приведен пример `wsl.conf` файла, который можно добавить в дистрибутивы.</span><span class="sxs-lookup"><span data-stu-id="b35c6-197">Here is a sample `wsl.conf` file you could add into your distributions:</span></span>

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

### <a name="configuration-options"></a><span data-ttu-id="b35c6-198">Параметры конфигурации</span><span class="sxs-lookup"><span data-stu-id="b35c6-198">Configuration Options</span></span>

<span data-ttu-id="b35c6-199">В соответствии с соглашениями об INI-файлах ключи объявляются в разделе.</span><span class="sxs-lookup"><span data-stu-id="b35c6-199">In keeping with .ini conventions, keys are declared under a section.</span></span> 

<span data-ttu-id="b35c6-200">WSL поддерживает два раздела: `automount` и `network`.</span><span class="sxs-lookup"><span data-stu-id="b35c6-200">WSL supports two sections: `automount` and `network`.</span></span>

#### <a name="automount"></a><span data-ttu-id="b35c6-201">automount</span><span class="sxs-lookup"><span data-stu-id="b35c6-201">automount</span></span>

<span data-ttu-id="b35c6-202">Раздел: `[automount]`</span><span class="sxs-lookup"><span data-stu-id="b35c6-202">Section: `[automount]`</span></span>

| <span data-ttu-id="b35c6-203">ключ</span><span class="sxs-lookup"><span data-stu-id="b35c6-203">key</span></span>        | <span data-ttu-id="b35c6-204">значение</span><span class="sxs-lookup"><span data-stu-id="b35c6-204">value</span></span>                          | <span data-ttu-id="b35c6-205">default</span><span class="sxs-lookup"><span data-stu-id="b35c6-205">default</span></span>      | <span data-ttu-id="b35c6-206">HDInsight</span><span class="sxs-lookup"><span data-stu-id="b35c6-206">notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b35c6-207">Включено</span><span class="sxs-lookup"><span data-stu-id="b35c6-207">enabled</span></span>    | <span data-ttu-id="b35c6-208">boolean</span><span class="sxs-lookup"><span data-stu-id="b35c6-208">boolean</span></span>                        | <span data-ttu-id="b35c6-209">true</span><span class="sxs-lookup"><span data-stu-id="b35c6-209">true</span></span>         | <span data-ttu-id="b35c6-210">Значение `true` обеспечивает автоматическое подключение</span><span class="sxs-lookup"><span data-stu-id="b35c6-210">`true` causes fixed drives (i.e</span></span> <span data-ttu-id="b35c6-211">несъемных дисков (например, `C:/` или `D:/`) DrvFs в `/mnt`.</span><span class="sxs-lookup"><span data-stu-id="b35c6-211">`C:/` or `D:/`) to be automatically mounted with DrvFs under `/mnt`.</span></span>  <span data-ttu-id="b35c6-212">`false`означает, что диски не будут подключены автоматически, но их можно подключать вручную или через `fstab` .</span><span class="sxs-lookup"><span data-stu-id="b35c6-212">`false` means drives won't be mounted automatically, but you could still mount them manually or via `fstab`.</span></span>                                                                                                             |
| <span data-ttu-id="b35c6-213">mountFsTab</span><span class="sxs-lookup"><span data-stu-id="b35c6-213">mountFsTab</span></span> | <span data-ttu-id="b35c6-214">boolean</span><span class="sxs-lookup"><span data-stu-id="b35c6-214">boolean</span></span>                        | <span data-ttu-id="b35c6-215">true</span><span class="sxs-lookup"><span data-stu-id="b35c6-215">true</span></span>         | <span data-ttu-id="b35c6-216">Значение `true` задает `/etc/fstab` для обработки при запуске WSL.</span><span class="sxs-lookup"><span data-stu-id="b35c6-216">`true` sets `/etc/fstab` to be processed on WSL start.</span></span> <span data-ttu-id="b35c6-217">/etc/fstab — это файл, в котором можно объявлять другие файловые системы, например общий ресурс SMB.</span><span class="sxs-lookup"><span data-stu-id="b35c6-217">/etc/fstab is a file where you can declare other filesystems, like an SMB share.</span></span> <span data-ttu-id="b35c6-218">Поэтому вы можете автоматически подключать эти файловые системы в WSL при запуске.</span><span class="sxs-lookup"><span data-stu-id="b35c6-218">Thus, you can mount these filesystems automatically in WSL on start up.</span></span>                                                                                                                |
| <span data-ttu-id="b35c6-219">root</span><span class="sxs-lookup"><span data-stu-id="b35c6-219">root</span></span>       | <span data-ttu-id="b35c6-220">Строка</span><span class="sxs-lookup"><span data-stu-id="b35c6-220">String</span></span>                         | `/mnt/`      | <span data-ttu-id="b35c6-221">Задает каталог, в который будут автоматически подключены несъемные диски.</span><span class="sxs-lookup"><span data-stu-id="b35c6-221">Sets the directory where fixed drives will be automatically mounted.</span></span> <span data-ttu-id="b35c6-222">Например, если у вас есть каталог в WSL в `/windir/` и вы указали его в качестве корневого каталога, то ваши несъемные диски будут подключены в `/windir/c`</span><span class="sxs-lookup"><span data-stu-id="b35c6-222">For example, if you have a directory in WSL at `/windir/` and you specify that as the root, you would expect to see your fixed drives mounted at `/windir/c`</span></span>                                                                                              |
| <span data-ttu-id="b35c6-223">options</span><span class="sxs-lookup"><span data-stu-id="b35c6-223">options</span></span>    | <span data-ttu-id="b35c6-224">разделенный запятыми список значений</span><span class="sxs-lookup"><span data-stu-id="b35c6-224">comma-separated list of values</span></span> | <span data-ttu-id="b35c6-225">пустая строка</span><span class="sxs-lookup"><span data-stu-id="b35c6-225">empty string</span></span> | <span data-ttu-id="b35c6-226">Это значение добавляется в строку параметров подключения по умолчанию DrvFs.</span><span class="sxs-lookup"><span data-stu-id="b35c6-226">This value is appended to the default DrvFs mount options string.</span></span> <span data-ttu-id="b35c6-227">**Можно указать только параметры, относящиеся к DrvFs.**</span><span class="sxs-lookup"><span data-stu-id="b35c6-227">**Only DrvFs-specific options can be specified.**</span></span> <span data-ttu-id="b35c6-228">Параметры, которые двоичный файл подключения обычно анализирует и преобразовывает во флаг, не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="b35c6-228">Options that the mount binary would normally parse into a flag are not supported.</span></span> <span data-ttu-id="b35c6-229">Если вы хотите явно указать эти параметры, необходимо добавить каждый диск, для которого вы хотите это сделать, в /etc/fstab.</span><span class="sxs-lookup"><span data-stu-id="b35c6-229">If you want to explicitly specify those options, you must include every drive for which you want to do so in /etc/fstab.</span></span> |

<span data-ttu-id="b35c6-230">По умолчанию WSL задает для идентификаторов UID и GID значения пользователя по умолчанию (в дистрибутиве Ubuntu пользователь по умолчанию создается с идентификаторами UID = 1000 и GID = 1000).</span><span class="sxs-lookup"><span data-stu-id="b35c6-230">By default, WSL sets the uid and gid to the value of the default user (in Ubuntu distro, the default user is created with uid=1000,gid=1000).</span></span> <span data-ttu-id="b35c6-231">Если пользователь явно указывает параметр GID или UID с помощью этого ключа, связанное значение будет перезаписано.</span><span class="sxs-lookup"><span data-stu-id="b35c6-231">If the user specifies a gid or uid option explicitly via this key, the associated value will be overwritten.</span></span> <span data-ttu-id="b35c6-232">В противном случае всегда будет добавляться значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b35c6-232">Otherwise, the default value will always be appended.</span></span>

<span data-ttu-id="b35c6-233">**Примечание.** Эти параметры применяются в качестве параметров подключения для всех автоматически подключенных дисков.</span><span class="sxs-lookup"><span data-stu-id="b35c6-233">**Note:** These options are applied as the mount options for all automatically mounted drives.</span></span> <span data-ttu-id="b35c6-234">Чтобы изменить параметры для конкретного диска, используйте /etc/fstab.</span><span class="sxs-lookup"><span data-stu-id="b35c6-234">To change the options for a specific drive only, use /etc/fstab instead.</span></span>

#### <a name="mount-options"></a><span data-ttu-id="b35c6-235">Параметры подключения</span><span class="sxs-lookup"><span data-stu-id="b35c6-235">Mount options</span></span>

<span data-ttu-id="b35c6-236">Задание различных параметров подключения для дисков Windows (DrvFs) позволяет контролировать определение разрешений для файлов Windows.</span><span class="sxs-lookup"><span data-stu-id="b35c6-236">Setting different mount options for Windows drives (DrvFs) can control how file permissions are calculated for Windows files.</span></span> <span data-ttu-id="b35c6-237">Доступны следующие варианты:</span><span class="sxs-lookup"><span data-stu-id="b35c6-237">The following options are available:</span></span>

| <span data-ttu-id="b35c6-238">Клавиши</span><span class="sxs-lookup"><span data-stu-id="b35c6-238">Key</span></span> | <span data-ttu-id="b35c6-239">Описание</span><span class="sxs-lookup"><span data-stu-id="b35c6-239">Description</span></span> | <span data-ttu-id="b35c6-240">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b35c6-240">Default</span></span> |
|:----|:----|:----|
|<span data-ttu-id="b35c6-241">uid</span><span class="sxs-lookup"><span data-stu-id="b35c6-241">uid</span></span>| <span data-ttu-id="b35c6-242">ИД пользователя, используемый для владельца всех файлов.</span><span class="sxs-lookup"><span data-stu-id="b35c6-242">The User ID used for the owner of all files</span></span> | <span data-ttu-id="b35c6-243">ИД пользователя по умолчанию для дистрибутива WSL (при первой установке имеет значение по умолчанию — 1000).</span><span class="sxs-lookup"><span data-stu-id="b35c6-243">The default User ID of your WSL distro (On first installation this defaults to 1000)</span></span>
|<span data-ttu-id="b35c6-244">gid</span><span class="sxs-lookup"><span data-stu-id="b35c6-244">gid</span></span>| <span data-ttu-id="b35c6-245">Идентификатор группы, используемый для владельца всех файлов.</span><span class="sxs-lookup"><span data-stu-id="b35c6-245">The Group ID used for the owner of all files</span></span> | <span data-ttu-id="b35c6-246">Идентификатор группы по умолчанию для дистрибутива WSL (при первой установке имеет значение по умолчанию — 1000).</span><span class="sxs-lookup"><span data-stu-id="b35c6-246">The default group ID of your WSL distro (On first installation this defaults to 1000)</span></span>
|<span data-ttu-id="b35c6-247">umask</span><span class="sxs-lookup"><span data-stu-id="b35c6-247">umask</span></span> | <span data-ttu-id="b35c6-248">Восьмеричная маска разрешений, исключаемых для всех файлов и каталогов.</span><span class="sxs-lookup"><span data-stu-id="b35c6-248">An octal mask of permissions to exclude for all files and directories</span></span> | <span data-ttu-id="b35c6-249">000</span><span class="sxs-lookup"><span data-stu-id="b35c6-249">000</span></span>
|<span data-ttu-id="b35c6-250">fmask</span><span class="sxs-lookup"><span data-stu-id="b35c6-250">fmask</span></span> | <span data-ttu-id="b35c6-251">Восьмеричная маска разрешений, исключаемых для всех файлов.</span><span class="sxs-lookup"><span data-stu-id="b35c6-251">An octal mask of permissions to exclude for all files</span></span> | <span data-ttu-id="b35c6-252">000</span><span class="sxs-lookup"><span data-stu-id="b35c6-252">000</span></span>
|<span data-ttu-id="b35c6-253">dmask</span><span class="sxs-lookup"><span data-stu-id="b35c6-253">dmask</span></span> | <span data-ttu-id="b35c6-254">Восьмеричная маска разрешений, исключаемых для всех каталогов.</span><span class="sxs-lookup"><span data-stu-id="b35c6-254">An octal mask of permissions to exclude for all directories</span></span> | <span data-ttu-id="b35c6-255">000</span><span class="sxs-lookup"><span data-stu-id="b35c6-255">000</span></span>

<span data-ttu-id="b35c6-256">**Примечание.** Маски разрешений помещаются в логическую операцию или перед применением к файлам или каталогам.</span><span class="sxs-lookup"><span data-stu-id="b35c6-256">**Note:** The permission masks are put through a logical OR operation before being applied to files or directories.</span></span> 

#### <a name="network"></a><span data-ttu-id="b35c6-257">Сеть</span><span class="sxs-lookup"><span data-stu-id="b35c6-257">network</span></span>

<span data-ttu-id="b35c6-258">Метка раздела: `[network]`</span><span class="sxs-lookup"><span data-stu-id="b35c6-258">Section label: `[network]`</span></span>

| <span data-ttu-id="b35c6-259">ключ</span><span class="sxs-lookup"><span data-stu-id="b35c6-259">key</span></span> | <span data-ttu-id="b35c6-260">значение</span><span class="sxs-lookup"><span data-stu-id="b35c6-260">value</span></span> | <span data-ttu-id="b35c6-261">default</span><span class="sxs-lookup"><span data-stu-id="b35c6-261">default</span></span> | <span data-ttu-id="b35c6-262">HDInsight</span><span class="sxs-lookup"><span data-stu-id="b35c6-262">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="b35c6-263">generateHosts</span><span class="sxs-lookup"><span data-stu-id="b35c6-263">generateHosts</span></span> | <span data-ttu-id="b35c6-264">boolean</span><span class="sxs-lookup"><span data-stu-id="b35c6-264">boolean</span></span> | `true` | <span data-ttu-id="b35c6-265">Значение `true` указывает WSL создать `/etc/hosts`.</span><span class="sxs-lookup"><span data-stu-id="b35c6-265">`true` sets WSL to generate `/etc/hosts`.</span></span> <span data-ttu-id="b35c6-266">Файл `hosts` содержит статическую карту имен узлов и соответствующих IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="b35c6-266">The `hosts` file contains a static map of hostnames corresponding IP address.</span></span> |
| <span data-ttu-id="b35c6-267">generateResolvConf</span><span class="sxs-lookup"><span data-stu-id="b35c6-267">generateResolvConf</span></span> | <span data-ttu-id="b35c6-268">boolean</span><span class="sxs-lookup"><span data-stu-id="b35c6-268">boolean</span></span> | `true` | <span data-ttu-id="b35c6-269">Значение `true` указывает WSL создать `/etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="b35c6-269">`true` set WSL to generate `/etc/resolv.conf`.</span></span> <span data-ttu-id="b35c6-270">Файл `resolv.conf` содержит список DNS-серверов, которые способны разрешить заданное имя узла в его IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="b35c6-270">The `resolv.conf` contains a DNS list that are capable of resolving a given hostname to its IP address.</span></span> | 

#### <a name="interop"></a><span data-ttu-id="b35c6-271">interop</span><span class="sxs-lookup"><span data-stu-id="b35c6-271">interop</span></span>

<span data-ttu-id="b35c6-272">Метка раздела: `[interop]`</span><span class="sxs-lookup"><span data-stu-id="b35c6-272">Section label: `[interop]`</span></span>

<span data-ttu-id="b35c6-273">Эти параметры доступны в выпусках для программы предварительной оценки, начиная со сборки 17713.</span><span class="sxs-lookup"><span data-stu-id="b35c6-273">These options are available in Insider Build 17713 and later.</span></span>

| <span data-ttu-id="b35c6-274">ключ</span><span class="sxs-lookup"><span data-stu-id="b35c6-274">key</span></span> | <span data-ttu-id="b35c6-275">значение</span><span class="sxs-lookup"><span data-stu-id="b35c6-275">value</span></span> | <span data-ttu-id="b35c6-276">default</span><span class="sxs-lookup"><span data-stu-id="b35c6-276">default</span></span> | <span data-ttu-id="b35c6-277">HDInsight</span><span class="sxs-lookup"><span data-stu-id="b35c6-277">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="b35c6-278">Включено</span><span class="sxs-lookup"><span data-stu-id="b35c6-278">enabled</span></span> | <span data-ttu-id="b35c6-279">boolean</span><span class="sxs-lookup"><span data-stu-id="b35c6-279">boolean</span></span> | `true` | <span data-ttu-id="b35c6-280">Установка этого ключа определяет, будет ли WSL поддерживать запуск процессов Windows.</span><span class="sxs-lookup"><span data-stu-id="b35c6-280">Setting this key will determine whether WSL will support launching Windows processes.</span></span> |
| <span data-ttu-id="b35c6-281">appendWindowsPath</span><span class="sxs-lookup"><span data-stu-id="b35c6-281">appendWindowsPath</span></span> | <span data-ttu-id="b35c6-282">boolean</span><span class="sxs-lookup"><span data-stu-id="b35c6-282">boolean</span></span> | `true` | <span data-ttu-id="b35c6-283">Задание этого ключа определяет, будет ли WSL добавлять элементы пути Windows в переменную среды $PATH.</span><span class="sxs-lookup"><span data-stu-id="b35c6-283">Setting this key will determine whether WSL will add Windows path elements to the $PATH environment variable.</span></span> |

#### <a name="user"></a><span data-ttu-id="b35c6-284">пользователь</span><span class="sxs-lookup"><span data-stu-id="b35c6-284">user</span></span>

<span data-ttu-id="b35c6-285">Метка раздела: `[user]`</span><span class="sxs-lookup"><span data-stu-id="b35c6-285">Section label: `[user]`</span></span>

<span data-ttu-id="b35c6-286">Эти параметры доступны в сборках 18980 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="b35c6-286">These options are available in Build 18980 and later.</span></span>

| <span data-ttu-id="b35c6-287">ключ</span><span class="sxs-lookup"><span data-stu-id="b35c6-287">key</span></span> | <span data-ttu-id="b35c6-288">значение</span><span class="sxs-lookup"><span data-stu-id="b35c6-288">value</span></span> | <span data-ttu-id="b35c6-289">default</span><span class="sxs-lookup"><span data-stu-id="b35c6-289">default</span></span> | <span data-ttu-id="b35c6-290">HDInsight</span><span class="sxs-lookup"><span data-stu-id="b35c6-290">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="b35c6-291">default</span><span class="sxs-lookup"><span data-stu-id="b35c6-291">default</span></span> | <span data-ttu-id="b35c6-292">строка</span><span class="sxs-lookup"><span data-stu-id="b35c6-292">string</span></span> | <span data-ttu-id="b35c6-293">Начальное имя пользователя, созданное при первом запуске</span><span class="sxs-lookup"><span data-stu-id="b35c6-293">The initial username created on first run</span></span> | <span data-ttu-id="b35c6-294">Задание этого параметра указывает, какой пользователь будет запускать, как при первом запуске сеанса WSL.</span><span class="sxs-lookup"><span data-stu-id="b35c6-294">Setting this key specifies which user to run as when first starting a WSL session.</span></span> |

## <a name="configure-global-options-with-wslconfig"></a><span data-ttu-id="b35c6-295">Настройка глобальных параметров с помощью. вслконфиг</span><span class="sxs-lookup"><span data-stu-id="b35c6-295">Configure global options with .wslconfig</span></span>

> <span data-ttu-id="b35c6-296">**Доступно в Windows Build 19041 и более поздних версиях**</span><span class="sxs-lookup"><span data-stu-id="b35c6-296">**Available in Windows Build 19041 and later**</span></span>

<span data-ttu-id="b35c6-297">Вы можете настроить глобальные параметры WSL, поместив `.wslconfig` файл в корневой каталог папки "Пользователи": `C:\Users\<yourUserName>\.wslconfig` .</span><span class="sxs-lookup"><span data-stu-id="b35c6-297">You can configure global WSL options by placing a `.wslconfig` file into the root directory of your users folder: `C:\Users\<yourUserName>\.wslconfig`.</span></span> <span data-ttu-id="b35c6-298">Этот файл может содержать следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="b35c6-298">This file can contain the following options:</span></span>

### <a name="wsl-2-settings"></a><span data-ttu-id="b35c6-299">Параметры WSL 2</span><span class="sxs-lookup"><span data-stu-id="b35c6-299">WSL 2 Settings</span></span>

<span data-ttu-id="b35c6-300">Эти параметры влияют на виртуальную машину, на которой распространяется любое WSL 2.</span><span class="sxs-lookup"><span data-stu-id="b35c6-300">These settings affect the VM that powers any WSL 2 distribution.</span></span> 

| <span data-ttu-id="b35c6-301">ключ</span><span class="sxs-lookup"><span data-stu-id="b35c6-301">key</span></span> | <span data-ttu-id="b35c6-302">значение</span><span class="sxs-lookup"><span data-stu-id="b35c6-302">value</span></span> | <span data-ttu-id="b35c6-303">default</span><span class="sxs-lookup"><span data-stu-id="b35c6-303">default</span></span> | <span data-ttu-id="b35c6-304">HDInsight</span><span class="sxs-lookup"><span data-stu-id="b35c6-304">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="b35c6-305">ядро</span><span class="sxs-lookup"><span data-stu-id="b35c6-305">kernel</span></span> | <span data-ttu-id="b35c6-306">строка</span><span class="sxs-lookup"><span data-stu-id="b35c6-306">string</span></span> | <span data-ttu-id="b35c6-307">Входящие в состав ядра Microsoft</span><span class="sxs-lookup"><span data-stu-id="b35c6-307">The Microsoft built kernel provided inbox</span></span> | <span data-ttu-id="b35c6-308">Абсолютный путь Windows к пользовательскому ядру Linux.</span><span class="sxs-lookup"><span data-stu-id="b35c6-308">An absolute Windows path to a custom Linux kernel.</span></span> |
| <span data-ttu-id="b35c6-309">memory.</span><span class="sxs-lookup"><span data-stu-id="b35c6-309">memory</span></span> | <span data-ttu-id="b35c6-310">размер;</span><span class="sxs-lookup"><span data-stu-id="b35c6-310">size</span></span> | <span data-ttu-id="b35c6-311">80% общего объема памяти в Windows</span><span class="sxs-lookup"><span data-stu-id="b35c6-311">80% of your total memory on Windows</span></span> | <span data-ttu-id="b35c6-312">Объем памяти, назначаемый виртуальной машине WSL 2.</span><span class="sxs-lookup"><span data-stu-id="b35c6-312">How much memory to assign to the WSL 2 VM.</span></span> |
| <span data-ttu-id="b35c6-313">обработчики</span><span class="sxs-lookup"><span data-stu-id="b35c6-313">processors</span></span> | <span data-ttu-id="b35c6-314">number</span><span class="sxs-lookup"><span data-stu-id="b35c6-314">number</span></span> | <span data-ttu-id="b35c6-315">Одинаковое число процессоров в Windows</span><span class="sxs-lookup"><span data-stu-id="b35c6-315">The same number of processors on Windows</span></span> | <span data-ttu-id="b35c6-316">Количество процессоров, назначаемых виртуальной машине WSL 2.</span><span class="sxs-lookup"><span data-stu-id="b35c6-316">How many processors to assign ot the WSL 2 VM.</span></span> |
| <span data-ttu-id="b35c6-317">локалхостфорвардинг</span><span class="sxs-lookup"><span data-stu-id="b35c6-317">localhostForwarding</span></span> | <span data-ttu-id="b35c6-318">boolean</span><span class="sxs-lookup"><span data-stu-id="b35c6-318">boolean</span></span> | `true` | <span data-ttu-id="b35c6-319">Логическое значение, указывающее, должны ли порты, привязанные к подстановочным знакам или localhost на виртуальной машине WSL 2, подключаться с узла через порт localhost:.</span><span class="sxs-lookup"><span data-stu-id="b35c6-319">Boolean specifying if ports bound to wildcard or localhost in the WSL 2 VM should be connectable from the host via localhost:port.</span></span> |
| <span data-ttu-id="b35c6-320">кернелкоммандлине</span><span class="sxs-lookup"><span data-stu-id="b35c6-320">kernelCommandLine</span></span> | <span data-ttu-id="b35c6-321">строка</span><span class="sxs-lookup"><span data-stu-id="b35c6-321">string</span></span> | <span data-ttu-id="b35c6-322">Пусто</span><span class="sxs-lookup"><span data-stu-id="b35c6-322">Blank</span></span> | <span data-ttu-id="b35c6-323">Дополнительные аргументы командной строки ядра.</span><span class="sxs-lookup"><span data-stu-id="b35c6-323">Additional kernel command line arguments.</span></span> |
| <span data-ttu-id="b35c6-324">swap</span><span class="sxs-lookup"><span data-stu-id="b35c6-324">swap</span></span> | <span data-ttu-id="b35c6-325">размер;</span><span class="sxs-lookup"><span data-stu-id="b35c6-325">size</span></span> | <span data-ttu-id="b35c6-326">25% размера памяти в Windows округляется до ближайших ГБ</span><span class="sxs-lookup"><span data-stu-id="b35c6-326">25% of memory size on Windows rounded up to the nearest GB</span></span> | <span data-ttu-id="b35c6-327">Объем пространства подкачки для добавления в виртуальную машину WSL 2, 0 для файла подкачки.</span><span class="sxs-lookup"><span data-stu-id="b35c6-327">How much swap space to add to the WSL 2 VM, 0 for no swap file.</span></span> |
| <span data-ttu-id="b35c6-328">Файл подкачки</span><span class="sxs-lookup"><span data-stu-id="b35c6-328">swapFile</span></span> | <span data-ttu-id="b35c6-329">размер;</span><span class="sxs-lookup"><span data-stu-id="b35c6-329">size</span></span> | <span data-ttu-id="b35c6-330">%усерпрофиле%\аппдата\локал\темп\свап.вхдкс</span><span class="sxs-lookup"><span data-stu-id="b35c6-330">%USERPROFILE%\AppData\Local\Temp\swap.vhdx</span></span> | <span data-ttu-id="b35c6-331">Абсолютный путь Windows к виртуальному жесткому диску для переключения.</span><span class="sxs-lookup"><span data-stu-id="b35c6-331">An absolute Windows path to the swap virtual hard disk.</span></span> |

<span data-ttu-id="b35c6-332">Записи со `path` значением должны быть путями Windows с escape-символами обратной косой черты, например:`C:\\Temp\\myCustomKernel`</span><span class="sxs-lookup"><span data-stu-id="b35c6-332">Entries with the `path` value must be Windows paths with escaped backslashes, e.g: `C:\\Temp\\myCustomKernel`</span></span>

<span data-ttu-id="b35c6-333">Записи со `size` значением должны быть размером, за которым следует единица, например `8GB` или `512MB` .</span><span class="sxs-lookup"><span data-stu-id="b35c6-333">Entries with the `size` value must be a size followed by a unit, for example `8GB` or `512MB`.</span></span>