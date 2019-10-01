---
title: Управление дистрибутивами Linux
description: Список ссылок на справочные материалы и инструкции по настройке нескольких дистрибутивов Linux, работающих в подсистеме Windows для Linux.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, wsl.conf, wslconfig
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 51099f21fe44fd8c7e8682332c939fbe6d5e5827
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269866"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a><span data-ttu-id="bd720-104">Управление подсистемой Windows для Linux и ее настройка</span><span class="sxs-lookup"><span data-stu-id="bd720-104">Manage and configure Windows Subsystem for Linux</span></span>

> <span data-ttu-id="bd720-105">Относится к Windows 10 Fall Creators Update и более поздним версиям.</span><span class="sxs-lookup"><span data-stu-id="bd720-105">Applies to Windows 10 Fall Creators Update and later.</span></span>  <span data-ttu-id="bd720-106">Ознакомьтесь с нашим обновленным [руководством по установке](./install_guide.md), чтобы попробовать новые функции управления и запустить несколько дистрибутивов Linux из Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="bd720-106">See our updated [installation guide](./install_guide.md) to try new management features and start running multiple Linux distributions from the Microsoft store.</span></span>

## <a name="ways-to-run-wsl"></a><span data-ttu-id="bd720-107">Способы запуска WSL</span><span class="sxs-lookup"><span data-stu-id="bd720-107">Ways to run WSL</span></span>

<span data-ttu-id="bd720-108">Существует множество способов запуска Linux с помощью подсистемы Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="bd720-108">There are many ways to run Linux with the Windows Subsystem for Linux.</span></span>

1. <span data-ttu-id="bd720-109">`[distro]`, например `ubuntu`.</span><span class="sxs-lookup"><span data-stu-id="bd720-109">`[distro]`, for example `ubuntu`</span></span>
1. <span data-ttu-id="bd720-110">`wsl.exe` или `bash.exe`</span><span class="sxs-lookup"><span data-stu-id="bd720-110">`wsl.exe` or `bash.exe`</span></span>
1. <span data-ttu-id="bd720-111">`wsl [command]` или `bash -c [command]`</span><span class="sxs-lookup"><span data-stu-id="bd720-111">`wsl [command]` or `bash -c [command]`</span></span>

<span data-ttu-id="bd720-112">Применяемый метод зависит от того, что вы делаете.</span><span class="sxs-lookup"><span data-stu-id="bd720-112">Which method you should use depends on what you're doing.</span></span>

### <a name="launch-wsl-by-distribution"></a><span data-ttu-id="bd720-113">Запуск WSL с помощью дистрибутива</span><span class="sxs-lookup"><span data-stu-id="bd720-113">Launch WSL by distribution</span></span>

<span data-ttu-id="bd720-114">При запуске дистрибутива с помощью специального приложения он запускается в собственном окне консоли.</span><span class="sxs-lookup"><span data-stu-id="bd720-114">Running a distribution using it's distro-specific application launches that distribution in it's own console window.</span></span>

![Запуск WSL из меню "Пуск"](media/start-launch.png)

<span data-ttu-id="bd720-116">Это то же самое, что нажать кнопку "Запустить" в Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="bd720-116">It is the same as clicking "Launch" in the Microsoft store.</span></span>

![Запуск WSL из Microsoft Store](media/store-launch.png)

<span data-ttu-id="bd720-118">Можно также запустить дистрибутив из командной строки, выполнив команду `[distribution].exe`.</span><span class="sxs-lookup"><span data-stu-id="bd720-118">You can also run the distribution from the command line by running `[distribution].exe`.</span></span>

<span data-ttu-id="bd720-119">Недостаток запуска дистрибутива из командной строки заключается в том, что при этом рабочим каталогом станет не текущий каталог, а корневой каталог дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="bd720-119">The disadvantage of running a distribution from the command line in this way is that it will automatically change your working directory from the current directory to the distribution's home directory.</span></span>

<span data-ttu-id="bd720-120">**Пример.**</span><span class="sxs-lookup"><span data-stu-id="bd720-120">**Example:**</span></span>

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

### <a name="wsl-and-wsl-command"></a><span data-ttu-id="bd720-121">Использование wsl и wsl [команда]</span><span class="sxs-lookup"><span data-stu-id="bd720-121">wsl and wsl [command]</span></span>

<span data-ttu-id="bd720-122">Лучший способ запуска WSL из командной строки — использовать `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="bd720-122">The best way to run WSL from the command line is using `wsl.exe`.</span></span>

<span data-ttu-id="bd720-123">**Пример.**</span><span class="sxs-lookup"><span data-stu-id="bd720-123">**Example:**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

<span data-ttu-id="bd720-124">Инструмент `wsl` не только сохраняет текущий рабочий каталог, но и позволяет выполнить одну команду помимо команд Windows.</span><span class="sxs-lookup"><span data-stu-id="bd720-124">Not only does `wsl` keep the current working directory in place, it lets you run a single command along side Windows commands.</span></span>

<span data-ttu-id="bd720-125">**Пример.**</span><span class="sxs-lookup"><span data-stu-id="bd720-125">**Example:**</span></span>

```console
PS C:\Users\sarah> Get-Date

Sunday, March 11, 2018 7:54:05 PM

PS C:\Users\sarah> wsl
scooley@scooley-elmer:/mnt/c/Users/sarah$ date
Sun Mar 11 19:56:57 DST 2018
scooley@scooley-elmer:/mnt/c/Users/sarah$ exit
logout

PS C:\Users\sarah> wsl date
Sun Mar 11 19:55:47 DST 2018
```

<span data-ttu-id="bd720-126">**Пример.**</span><span class="sxs-lookup"><span data-stu-id="bd720-126">**Example:**</span></span>

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


## <a name="managing-multiple-linux-distributions"></a><span data-ttu-id="bd720-127">Управление несколькими дистрибутивами Linux</span><span class="sxs-lookup"><span data-stu-id="bd720-127">Managing multiple Linux Distributions</span></span>

### <a name="windows-10-version-1903-and-later"></a><span data-ttu-id="bd720-128">Windows 10 версии 1903 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="bd720-128">Windows 10 Version 1903 and later</span></span>

<span data-ttu-id="bd720-129">Можно использовать `wsl.exe` для управления дистрибутивами в подсистеме Windows для Linux (WSL), включая вывод списка доступных дистрибутивов, настройку дистрибутива по умолчанию и удаление дистрибутивов.</span><span class="sxs-lookup"><span data-stu-id="bd720-129">You can use `wsl.exe` to manage your distributions in the Windows Subsystem for Linux (WSL), including listing available distributions, setting a default distribution, and uninstalling distributions.</span></span>

<span data-ttu-id="bd720-130">Каждый дистрибутив Linux независимо управляет собственными конфигурациями.</span><span class="sxs-lookup"><span data-stu-id="bd720-130">Each Linux distribution independently manages its own configurations.</span></span> <span data-ttu-id="bd720-131">Чтобы просмотреть команды, относящиеся к определенному дистрибутиву, выполните команду `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="bd720-131">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="bd720-132">Пример: `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="bd720-132">For example `ubuntu /?`.</span></span>

#### <a name="list-distributions"></a><span data-ttu-id="bd720-133">Вывод списка дистрибутивов</span><span class="sxs-lookup"><span data-stu-id="bd720-133">List distributions</span></span>

<span data-ttu-id="bd720-134">`wsl -l` , `wsl --list`</span><span class="sxs-lookup"><span data-stu-id="bd720-134">`wsl -l` , `wsl --list`</span></span>  
<span data-ttu-id="bd720-135">Выводит список доступных дистрибутивов Linux, совместимых с WSL.</span><span class="sxs-lookup"><span data-stu-id="bd720-135">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="bd720-136">Если дистрибутив есть в списке, он установлен и готов к использованию.</span><span class="sxs-lookup"><span data-stu-id="bd720-136">If a distribution is listed, it's installed and ready to use.</span></span>

`wsl --list --all`   
<span data-ttu-id="bd720-137">Выводит список всех дистрибутивов, включая те, которые сейчас не используются.</span><span class="sxs-lookup"><span data-stu-id="bd720-137">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="bd720-138">Они могут находиться в процессе установки, удаления или в неработающем состоянии.</span><span class="sxs-lookup"><span data-stu-id="bd720-138">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

`wsl --list --running`   
<span data-ttu-id="bd720-139">Выводит список всех дистрибутивов, выполняемых в данный момент.</span><span class="sxs-lookup"><span data-stu-id="bd720-139">Lists all distributions that are currently running.</span></span>

#### <a name="set-a-default-distribution"></a><span data-ttu-id="bd720-140">Настройка дистрибутива по умолчанию</span><span class="sxs-lookup"><span data-stu-id="bd720-140">Set a default distribution</span></span>

<span data-ttu-id="bd720-141">Дистрибутив по умолчанию WSL запускается при выполнении `wsl` в командной строке.</span><span class="sxs-lookup"><span data-stu-id="bd720-141">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

<span data-ttu-id="bd720-142">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="bd720-142">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span></span>

<span data-ttu-id="bd720-143">Задает для дистрибутив по умолчанию с помощью значения `<DistributionName>`.</span><span class="sxs-lookup"><span data-stu-id="bd720-143">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="bd720-144">**Пример.**</span><span class="sxs-lookup"><span data-stu-id="bd720-144">**Example:**</span></span>  
<span data-ttu-id="bd720-145">Команда `wsl -s Ubuntu` в качестве дистрибутива по умолчанию установит Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="bd720-145">`wsl -s Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="bd720-146">Теперь при выполнении `wsl npm init` эта команда будет выполняться в Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="bd720-146">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="bd720-147">Если выполнить `wsl`, откроется сеанс Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="bd720-147">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="bd720-148">Отмена регистрации и повторная установка дистрибутива</span><span class="sxs-lookup"><span data-stu-id="bd720-148">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="bd720-149">Хотя дистрибутивы Linux можно устанавливать из Microsoft Store, их невозможно удалить в Store.</span><span class="sxs-lookup"><span data-stu-id="bd720-149">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="bd720-150">С помощью WSL Config можно отменить регистрацию дистрибутивов или удалить их.</span><span class="sxs-lookup"><span data-stu-id="bd720-150">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="bd720-151">Отмена регистрации также позволяет переустановить дистрибутивы.</span><span class="sxs-lookup"><span data-stu-id="bd720-151">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="bd720-152">**Внимание!** После отмены регистрации все данные, параметры и программное обеспечение, связанные с этим дистрибутивом, будут безвозвратно утеряны.</span><span class="sxs-lookup"><span data-stu-id="bd720-152">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="bd720-153">При переустановке из Store будет установлена чистая копия дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="bd720-153">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wsl --unregister <DistributionName>`  
<span data-ttu-id="bd720-154">Отменяет регистрацию дистрибутива в WSL, чтобы его можно было переустановить или очистить.</span><span class="sxs-lookup"><span data-stu-id="bd720-154">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="bd720-155">Например: `wsl --unregister Ubuntu` приведет к удалению Ubuntu из дистрибутивов, доступных в WSL.</span><span class="sxs-lookup"><span data-stu-id="bd720-155">For example: `wsl --unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="bd720-156">При выполнении команды `wsl --list` этот дистрибутив не будет присутствовать в списке.</span><span class="sxs-lookup"><span data-stu-id="bd720-156">When I run `wsl --list` it will not be listed.</span></span>

<span data-ttu-id="bd720-157">Чтобы переустановить его, найдите этот дистрибутив в Microsoft Store и нажмите кнопку "Запустить".</span><span class="sxs-lookup"><span data-stu-id="bd720-157">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

#### <a name="run-as-a-specific-user"></a><span data-ttu-id="bd720-158">Выполнение от имени определенного пользователя</span><span class="sxs-lookup"><span data-stu-id="bd720-158">Run as a specific user</span></span>

<span data-ttu-id="bd720-159">`wsl -u <Username>`, `wsl --user <Username>`</span><span class="sxs-lookup"><span data-stu-id="bd720-159">`wsl -u <Username>`, `wsl --user <Username>`</span></span>

<span data-ttu-id="bd720-160">Выполняет WSL от имени указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="bd720-160">Run WSL as the specified user.</span></span> <span data-ttu-id="bd720-161">Обратите внимание на то, что этот пользователь должен существовать в дистрибутиве WSL.</span><span class="sxs-lookup"><span data-stu-id="bd720-161">Please note that user must exist inside of the WSL distribution.</span></span>

#### <a name="run-a-specific-distribution"></a><span data-ttu-id="bd720-162">Запуск определенного дистрибутива</span><span class="sxs-lookup"><span data-stu-id="bd720-162">Run a specific distribution</span></span>

<span data-ttu-id="bd720-163">`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="bd720-163">`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`</span></span>

<span data-ttu-id="bd720-164">Запускает указанный дистрибутив WSL. Эту команду можно использовать для отправки команд в определенный дистрибутив без необходимости изменения дистрибутива по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bd720-164">Run a specified distribution of WSL, can be used to send commands to a specific distribution without having to change your default.</span></span>

### <a name="versions-earlier-than-windows-10-version-1903"></a><span data-ttu-id="bd720-165">Версии, предшествующие Windows 10 версии 1903</span><span class="sxs-lookup"><span data-stu-id="bd720-165">Versions Earlier than Windows 10 Version 1903</span></span>

<span data-ttu-id="bd720-166">WSL Config (`wslconfig.exe`) — это программа командной строки для управления дистрибутивами Linux, работающими в подсистеме Windows для Linux (WSL).</span><span class="sxs-lookup"><span data-stu-id="bd720-166">WSL Config (`wslconfig.exe`) is a command-line tool for managing Linux distributions running on the Windows Subsystem for Linux (WSL).</span></span>  <span data-ttu-id="bd720-167">Она позволяет получить список доступных дистрибутивов, настроить дистрибутив по умолчанию и удалить дистрибутивы.</span><span class="sxs-lookup"><span data-stu-id="bd720-167">It lets you list available distributions, set a default distribution, and uninstall distributions.</span></span>

<span data-ttu-id="bd720-168">Хотя WSL Config удобно использовать для параметров, охватывающих или координирующих несколько дистрибутивов, каждый дистрибутив Linux независимо управляет собственными конфигурациями.</span><span class="sxs-lookup"><span data-stu-id="bd720-168">While WSL Config is helpful for settings that span or coordinate distributions, each Linux distribution independently manages its own configurations.</span></span>  <span data-ttu-id="bd720-169">Чтобы просмотреть команды, относящиеся к определенному дистрибутиву, выполните команду `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="bd720-169">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="bd720-170">Пример: `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="bd720-170">For example `ubuntu /?`.</span></span>

<span data-ttu-id="bd720-171">Чтобы просмотреть все доступные параметры для wslconfig, выполните команду `wslconfig /?`</span><span class="sxs-lookup"><span data-stu-id="bd720-171">To see all available options for wslconfig, run:  `wslconfig /?`</span></span>

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

#### <a name="list-distributions"></a><span data-ttu-id="bd720-172">Вывод списка дистрибутивов</span><span class="sxs-lookup"><span data-stu-id="bd720-172">List distributions</span></span>

`wslconfig /list`  
<span data-ttu-id="bd720-173">Выводит список доступных дистрибутивов Linux, совместимых с WSL.</span><span class="sxs-lookup"><span data-stu-id="bd720-173">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="bd720-174">Если дистрибутив есть в списке, он установлен и готов к использованию.</span><span class="sxs-lookup"><span data-stu-id="bd720-174">If a distribution is listed, it's installed and ready to use.</span></span>

`wslconfig /list /all`  
<span data-ttu-id="bd720-175">Выводит список всех дистрибутивов, включая те, которые сейчас не используются.</span><span class="sxs-lookup"><span data-stu-id="bd720-175">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="bd720-176">Они могут находиться в процессе установки, удаления или в неработающем состоянии.</span><span class="sxs-lookup"><span data-stu-id="bd720-176">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

#### <a name="set-a-default-distribution"></a><span data-ttu-id="bd720-177">Настройка дистрибутива по умолчанию</span><span class="sxs-lookup"><span data-stu-id="bd720-177">Set a default distribution</span></span>

<span data-ttu-id="bd720-178">Дистрибутив по умолчанию WSL запускается при выполнении `wsl` в командной строке.</span><span class="sxs-lookup"><span data-stu-id="bd720-178">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

`wslconfig /setdefault <DistributionName>`

<span data-ttu-id="bd720-179">Задает для дистрибутив по умолчанию с помощью значения `<DistributionName>`.</span><span class="sxs-lookup"><span data-stu-id="bd720-179">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="bd720-180">**Пример.**</span><span class="sxs-lookup"><span data-stu-id="bd720-180">**Example:**</span></span>  
<span data-ttu-id="bd720-181">Команда `wslconfig /setdefault Ubuntu` в качестве дистрибутива по умолчанию установит Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="bd720-181">`wslconfig /setdefault Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="bd720-182">Теперь при выполнении `wsl npm init` эта команда будет выполняться в Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="bd720-182">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="bd720-183">Если выполнить `wsl`, откроется сеанс Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="bd720-183">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="bd720-184">Отмена регистрации и повторная установка дистрибутива</span><span class="sxs-lookup"><span data-stu-id="bd720-184">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="bd720-185">Хотя дистрибутивы Linux можно устанавливать из Microsoft Store, их невозможно удалить в Store.</span><span class="sxs-lookup"><span data-stu-id="bd720-185">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="bd720-186">С помощью WSL Config можно отменить регистрацию дистрибутивов или удалить их.</span><span class="sxs-lookup"><span data-stu-id="bd720-186">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="bd720-187">Отмена регистрации также позволяет переустановить дистрибутивы.</span><span class="sxs-lookup"><span data-stu-id="bd720-187">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="bd720-188">**Внимание!** После отмены регистрации все данные, параметры и программное обеспечение, связанные с этим дистрибутивом, будут безвозвратно утеряны.</span><span class="sxs-lookup"><span data-stu-id="bd720-188">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="bd720-189">При переустановке из Store будет установлена чистая копия дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="bd720-189">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wslconfig /unregister <DistributionName>`  
<span data-ttu-id="bd720-190">Отменяет регистрацию дистрибутива в WSL, чтобы его можно было переустановить или очистить.</span><span class="sxs-lookup"><span data-stu-id="bd720-190">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="bd720-191">Например: `wslconfig /unregister Ubuntu` приведет к удалению Ubuntu из дистрибутивов, доступных в WSL.</span><span class="sxs-lookup"><span data-stu-id="bd720-191">For example: `wslconfig /unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="bd720-192">При выполнении команды `wslconfig /list` этот дистрибутив не будет присутствовать в списке.</span><span class="sxs-lookup"><span data-stu-id="bd720-192">When I run `wslconfig /list` it will not be listed.</span></span>

<span data-ttu-id="bd720-193">Чтобы переустановить его, найдите этот дистрибутив в Microsoft Store и нажмите кнопку "Запустить".</span><span class="sxs-lookup"><span data-stu-id="bd720-193">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="set-wsl-launch-settings"></a><span data-ttu-id="bd720-194">Параметры запуска WSL</span><span class="sxs-lookup"><span data-stu-id="bd720-194">Set WSL launch settings</span></span>

> <span data-ttu-id="bd720-195">**Доступно в выпусках для программы предварительной оценки Windows, начиная со сборки 17093**</span><span class="sxs-lookup"><span data-stu-id="bd720-195">**Available in Windows Insider Build 17093 and later**</span></span>

<span data-ttu-id="bd720-196">Автоматическая настройка определенных функций в WSL, которые будут применяться при каждом запуске подсистемы с помощью `wsl.conf`.</span><span class="sxs-lookup"><span data-stu-id="bd720-196">Automatically configure certain functionality in WSL that will be applied every time you launch the subsystem using `wsl.conf`.</span></span> 

<span data-ttu-id="bd720-197">Сейчас сюда входят параметры автоподключения и конфигурация сети.</span><span class="sxs-lookup"><span data-stu-id="bd720-197">Right now, this includes automount options and network configuration.</span></span>

<span data-ttu-id="bd720-198">Файл `wsl.conf` в каждом дистрибутиве Linux находится в папке `/etc/wsl.conf`.</span><span class="sxs-lookup"><span data-stu-id="bd720-198">`wsl.conf` is located in each Linux distribution in `/etc/wsl.conf`.</span></span> <span data-ttu-id="bd720-199">Если этот файл отсутствует, его можно создать самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="bd720-199">If the file is not there, you can create it yourself.</span></span> <span data-ttu-id="bd720-200">WSL обнаружит наличие файла и прочитает его содержимое.</span><span class="sxs-lookup"><span data-stu-id="bd720-200">WSL will detect the existence of the file and will read its contents.</span></span> <span data-ttu-id="bd720-201">Если этот файл отсутствует или имеет неправильный формат (т. е. неправильное форматирование разметки), WSL продолжит запуск в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="bd720-201">If the file is missing or malformed (that is, improper markup formatting), WSL will continue to launch as normal.</span></span>

<span data-ttu-id="bd720-202">Ниже приведен пример файла `wsl.conf`, который можно добавить в свои дистрибутивы.</span><span class="sxs-lookup"><span data-stu-id="bd720-202">Here is a sample `wsl.conf` file you could add into your distros:</span></span>

```console
# Enable extra metadata options by default
[automount]
enabled = true
root = /windir/
options = "metadata,umask=22,fmask=11"
mountFsTab = false

# Enable DNS – even though these are turned on by default, we’ll specify here just to be explicit.
[network]
generateHosts = true
generateResolvConf = true
```

### <a name="configuration-options"></a><span data-ttu-id="bd720-203">Параметры конфигурации</span><span class="sxs-lookup"><span data-stu-id="bd720-203">Configuration Options</span></span>

<span data-ttu-id="bd720-204">В соответствии с соглашениями об INI-файлах ключи объявляются в разделе.</span><span class="sxs-lookup"><span data-stu-id="bd720-204">In keeping with .ini conventions, keys are declared under a section.</span></span> 

<span data-ttu-id="bd720-205">WSL поддерживает два раздела: `automount` и `network`.</span><span class="sxs-lookup"><span data-stu-id="bd720-205">WSL supports two sections: `automount` and `network`.</span></span>

#### <a name="automount"></a><span data-ttu-id="bd720-206">automount</span><span class="sxs-lookup"><span data-stu-id="bd720-206">automount</span></span>

<span data-ttu-id="bd720-207">Раздел: `[automount]`</span><span class="sxs-lookup"><span data-stu-id="bd720-207">Section: `[automount]`</span></span>


| <span data-ttu-id="bd720-208">key</span><span class="sxs-lookup"><span data-stu-id="bd720-208">key</span></span>        | <span data-ttu-id="bd720-209">value</span><span class="sxs-lookup"><span data-stu-id="bd720-209">value</span></span>                          | <span data-ttu-id="bd720-210">по умолчанию</span><span class="sxs-lookup"><span data-stu-id="bd720-210">default</span></span>      | <span data-ttu-id="bd720-211">Примечания</span><span class="sxs-lookup"><span data-stu-id="bd720-211">notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd720-212">enabled</span><span class="sxs-lookup"><span data-stu-id="bd720-212">enabled</span></span>    | <span data-ttu-id="bd720-213">Логический</span><span class="sxs-lookup"><span data-stu-id="bd720-213">boolean</span></span>                        | <span data-ttu-id="bd720-214">true</span><span class="sxs-lookup"><span data-stu-id="bd720-214">true</span></span>         | <span data-ttu-id="bd720-215">Значение `true` обеспечивает автоматическое подключение</span><span class="sxs-lookup"><span data-stu-id="bd720-215">`true` causes fixed drives (i.e</span></span> <span data-ttu-id="bd720-216">несъемных дисков (например, `C:/` или `D:/`) DrvFs в `/mnt`.</span><span class="sxs-lookup"><span data-stu-id="bd720-216">`C:/` or `D:/`) to be automatically mounted with DrvFs under `/mnt`.</span></span>  <span data-ttu-id="bd720-217">Значение `false` означает, что диски не будут подключены автоматически, но их можно будет подключить вручную или с помощью `fstab`.</span><span class="sxs-lookup"><span data-stu-id="bd720-217">`false` means drives won’t be mounted automatically, but you could still mount them manually or via `fstab`.</span></span>                                                                                                             |
| <span data-ttu-id="bd720-218">mountFsTab</span><span class="sxs-lookup"><span data-stu-id="bd720-218">mountFsTab</span></span> | <span data-ttu-id="bd720-219">Логический</span><span class="sxs-lookup"><span data-stu-id="bd720-219">boolean</span></span>                        | <span data-ttu-id="bd720-220">true</span><span class="sxs-lookup"><span data-stu-id="bd720-220">true</span></span>         | <span data-ttu-id="bd720-221">Значение `true` задает `/etc/fstab` для обработки при запуске WSL.</span><span class="sxs-lookup"><span data-stu-id="bd720-221">`true` sets `/etc/fstab` to be processed on WSL start.</span></span> <span data-ttu-id="bd720-222">/etc/fstab — это файл, в котором можно объявлять другие файловые системы, например общий ресурс SMB.</span><span class="sxs-lookup"><span data-stu-id="bd720-222">/etc/fstab is a file where you can declare other filesystems, like an SMB share.</span></span> <span data-ttu-id="bd720-223">Поэтому вы можете автоматически подключать эти файловые системы в WSL при запуске.</span><span class="sxs-lookup"><span data-stu-id="bd720-223">Thus, you can mount these filesystems automatically in WSL on start up.</span></span>                                                                                                                |
| <span data-ttu-id="bd720-224">root</span><span class="sxs-lookup"><span data-stu-id="bd720-224">root</span></span>       | <span data-ttu-id="bd720-225">Строка</span><span class="sxs-lookup"><span data-stu-id="bd720-225">String</span></span>                         | `/mnt/`      | <span data-ttu-id="bd720-226">Задает каталог, в который будут автоматически подключены несъемные диски.</span><span class="sxs-lookup"><span data-stu-id="bd720-226">Sets the directory where fixed drives will be automatically mounted.</span></span> <span data-ttu-id="bd720-227">Например, если у вас есть каталог в WSL в `/windir/` и вы указали его в качестве корневого каталога, то ваши несъемные диски будут подключены в `/windir/c`</span><span class="sxs-lookup"><span data-stu-id="bd720-227">For example, if you have a directory in WSL at `/windir/` and you specify that as the root, you would expect to see your fixed drives mounted at `/windir/c`</span></span>                                                                                              |
| <span data-ttu-id="bd720-228">параметры</span><span class="sxs-lookup"><span data-stu-id="bd720-228">options</span></span>    | <span data-ttu-id="bd720-229">разделенный запятыми список значений</span><span class="sxs-lookup"><span data-stu-id="bd720-229">comma-separated list of values</span></span> | <span data-ttu-id="bd720-230">пустая строка</span><span class="sxs-lookup"><span data-stu-id="bd720-230">empty string</span></span> | <span data-ttu-id="bd720-231">Это значение добавляется в строку параметров подключения по умолчанию DrvFs.</span><span class="sxs-lookup"><span data-stu-id="bd720-231">This value is appended to the default DrvFs mount options string.</span></span> <span data-ttu-id="bd720-232">**Можно указать только параметры, относящиеся к DrvFs.**</span><span class="sxs-lookup"><span data-stu-id="bd720-232">**Only DrvFs-specific options can be specified.**</span></span> <span data-ttu-id="bd720-233">Параметры, которые двоичный файл подключения обычно анализирует и преобразовывает во флаг, не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="bd720-233">Options that the mount binary would normally parse into a flag are not supported.</span></span> <span data-ttu-id="bd720-234">Если вы хотите явно указать эти параметры, необходимо добавить каждый диск, для которого вы хотите это сделать, в /etc/fstab.</span><span class="sxs-lookup"><span data-stu-id="bd720-234">If you want to explicitly specify those options, you must include every drive for which you want to do so in /etc/fstab.</span></span> |

<span data-ttu-id="bd720-235">По умолчанию WSL задает для идентификаторов UID и GID значения пользователя по умолчанию (в дистрибутиве Ubuntu пользователь по умолчанию создается с идентификаторами UID = 1000 и GID = 1000).</span><span class="sxs-lookup"><span data-stu-id="bd720-235">By default, WSL sets the uid and gid to the value of the default user (in Ubuntu distro, the default user is created with uid=1000,gid=1000).</span></span> <span data-ttu-id="bd720-236">Если пользователь явно указывает параметр GID или UID с помощью этого ключа, связанное значение будет перезаписано.</span><span class="sxs-lookup"><span data-stu-id="bd720-236">If the user specifies a gid or uid option explicitly via this key, the associated value will be overwritten.</span></span> <span data-ttu-id="bd720-237">В противном случае всегда будет добавляться значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bd720-237">Otherwise, the default value will always be appended.</span></span>

<span data-ttu-id="bd720-238">**Примечание.** Эти параметры применяются в качестве параметров подключения для всех автоматически подключаемых дисков.</span><span class="sxs-lookup"><span data-stu-id="bd720-238">**Note:** These options are applied as the mount options for all automatically mounted drives.</span></span> <span data-ttu-id="bd720-239">Чтобы изменить параметры для конкретного диска, используйте /etc/fstab.</span><span class="sxs-lookup"><span data-stu-id="bd720-239">To change the options for a specific drive only, use /etc/fstab instead.</span></span>

#### <a name="network"></a><span data-ttu-id="bd720-240">сеть</span><span class="sxs-lookup"><span data-stu-id="bd720-240">network</span></span>

<span data-ttu-id="bd720-241">Метка раздела: `[network]`</span><span class="sxs-lookup"><span data-stu-id="bd720-241">Section label: `[network]`</span></span>

| <span data-ttu-id="bd720-242">key</span><span class="sxs-lookup"><span data-stu-id="bd720-242">key</span></span> | <span data-ttu-id="bd720-243">value</span><span class="sxs-lookup"><span data-stu-id="bd720-243">value</span></span> | <span data-ttu-id="bd720-244">по умолчанию</span><span class="sxs-lookup"><span data-stu-id="bd720-244">default</span></span> | <span data-ttu-id="bd720-245">Примечания</span><span class="sxs-lookup"><span data-stu-id="bd720-245">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="bd720-246">generateHosts</span><span class="sxs-lookup"><span data-stu-id="bd720-246">generateHosts</span></span> | <span data-ttu-id="bd720-247">Логический</span><span class="sxs-lookup"><span data-stu-id="bd720-247">boolean</span></span> | `true` | <span data-ttu-id="bd720-248">Значение `true` указывает WSL создать `/etc/hosts`.</span><span class="sxs-lookup"><span data-stu-id="bd720-248">`true` sets WSL to generate `/etc/hosts`.</span></span> <span data-ttu-id="bd720-249">Файл `hosts` содержит статическую карту имен узлов и соответствующих IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="bd720-249">The `hosts` file contains a static map of hostnames corresponding IP address.</span></span> |
| <span data-ttu-id="bd720-250">generateResolvConf</span><span class="sxs-lookup"><span data-stu-id="bd720-250">generateResolvConf</span></span> | <span data-ttu-id="bd720-251">Логический</span><span class="sxs-lookup"><span data-stu-id="bd720-251">boolean</span></span> | `true` | <span data-ttu-id="bd720-252">Значение `true` указывает WSL создать `/etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="bd720-252">`true` set WSL to generate `/etc/resolv.conf`.</span></span> <span data-ttu-id="bd720-253">Файл `resolv.conf` содержит список DNS-серверов, которые способны разрешить заданное имя узла в его IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="bd720-253">The `resolv.conf` contains a DNS list that are capable of resolving a given hostname to its IP address.</span></span> | 

#### <a name="interop"></a><span data-ttu-id="bd720-254">interop</span><span class="sxs-lookup"><span data-stu-id="bd720-254">interop</span></span>

<span data-ttu-id="bd720-255">Метка раздела: `[interop]`</span><span class="sxs-lookup"><span data-stu-id="bd720-255">Section label: `[interop]`</span></span>

<span data-ttu-id="bd720-256">Эти параметры доступны в выпусках для программы предварительной оценки, начиная со сборки 17713.</span><span class="sxs-lookup"><span data-stu-id="bd720-256">These options are available in Insider Build 17713 and later.</span></span>

| <span data-ttu-id="bd720-257">key</span><span class="sxs-lookup"><span data-stu-id="bd720-257">key</span></span> | <span data-ttu-id="bd720-258">value</span><span class="sxs-lookup"><span data-stu-id="bd720-258">value</span></span> | <span data-ttu-id="bd720-259">по умолчанию</span><span class="sxs-lookup"><span data-stu-id="bd720-259">default</span></span> | <span data-ttu-id="bd720-260">Примечания</span><span class="sxs-lookup"><span data-stu-id="bd720-260">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="bd720-261">enabled</span><span class="sxs-lookup"><span data-stu-id="bd720-261">enabled</span></span> | <span data-ttu-id="bd720-262">Логический</span><span class="sxs-lookup"><span data-stu-id="bd720-262">boolean</span></span> | `true` | <span data-ttu-id="bd720-263">Установка этого ключа определяет, будет ли WSL поддерживать запуск процессов Windows.</span><span class="sxs-lookup"><span data-stu-id="bd720-263">Setting this key will determine whether WSL will support launching Windows processes.</span></span> |
| <span data-ttu-id="bd720-264">appendWindowsPath</span><span class="sxs-lookup"><span data-stu-id="bd720-264">appendWindowsPath</span></span> | <span data-ttu-id="bd720-265">Логический</span><span class="sxs-lookup"><span data-stu-id="bd720-265">boolean</span></span> | `true` | <span data-ttu-id="bd720-266">Задание этого ключа определяет, будет ли WSL добавлять элементы пути Windows в переменную среды $PATH.</span><span class="sxs-lookup"><span data-stu-id="bd720-266">Setting this key will determine whether WSL will add Windows path elements to the $PATH environment variable.</span></span> | 
