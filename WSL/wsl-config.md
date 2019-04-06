---
title: Управление дистрибутивы Linux
description: Ссылки на перечисление и настройка несколько дистрибутивов Linux, запущенных в подсистеме Windows для Linux.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, wsl.conf, wslconfig
author: scooley
ms.author: scooley
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.openlocfilehash: c806552750f413fcb75f989d868a57cc939af64a
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063502"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a><span data-ttu-id="5e3b9-104">Управление и настройку подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="5e3b9-104">Manage and configure Windows Subsystem for Linux</span></span>

> <span data-ttu-id="5e3b9-105">Применяется к Windows 10 Fall Creators Update и более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-105">Applies to Windows 10 Fall Creators Update and later.</span></span>  <span data-ttu-id="5e3b9-106">См. в разделе нашей обновленной [руководство по установке](./install_guide.md) попробовать новые возможности управления и запустить несколько дистрибутивов Linux из Windows Store.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-106">See our updated [installation guide](./install_guide.md) to try new management features and start running multiple Linux distributions from the Windows Store.</span></span>

## <a name="ways-to-run-wsl"></a><span data-ttu-id="5e3b9-107">Способы выполнения WSL</span><span class="sxs-lookup"><span data-stu-id="5e3b9-107">Ways to run WSL</span></span>

<span data-ttu-id="5e3b9-108">Существует много способов для запуска Linux с подсистемой Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-108">There are many ways to run Linux with the Windows Subsystem for Linux.</span></span>

1. `[distro]` <span data-ttu-id="5e3b9-109">IE</span><span class="sxs-lookup"><span data-stu-id="5e3b9-109">ie</span></span> `ubuntu`
1. `wsl.exe` <span data-ttu-id="5e3b9-110">или диспетчер конфигурации служб</span><span class="sxs-lookup"><span data-stu-id="5e3b9-110">or</span></span> `bash.exe`
1. `wsl [command]` <span data-ttu-id="5e3b9-111">или диспетчер конфигурации служб</span><span class="sxs-lookup"><span data-stu-id="5e3b9-111">or</span></span> `bash -c [command]`

<span data-ttu-id="5e3b9-112">Какой метод следует использовать зависит от того, что он делает.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-112">Which method you should use depends on what you're doing.</span></span>

### <a name="launch-wsl-by-distribution"></a><span data-ttu-id="5e3b9-113">Запустите WSL, распространения</span><span class="sxs-lookup"><span data-stu-id="5e3b9-113">Launch WSL by distribution</span></span>

<span data-ttu-id="5e3b9-114">Под управлением дистрибутива, с помощью приложения конкретного дистрибутива запускает дистрибутива в собственном окне консоли.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-114">Running a distribution using it's distro-specific application launches that distribution in it's own console window.</span></span>

![Из меню "Пуск" запустите WSL](media/start-launch.png)

<span data-ttu-id="5e3b9-116">Это же, как нажать кнопку «Запуск» в Windows Store.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-116">It is the same as clicking "Launch" in the Windows Store.</span></span>

![Запустите WSL из Windows Store](media/store-launch.png)

<span data-ttu-id="5e3b9-118">Распределение можно также запустить из командной строки, выполнив `[distribution].exe`.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-118">You can also run the distribution from the command line by running `[distribution].exe`.</span></span>

<span data-ttu-id="5e3b9-119">Недостатком под управлением дистрибутива из командной строки таким образом является, что вы автоматически измените рабочий каталог из текущего каталога на домашний каталог дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-119">The disadvantage of running a distribution from the command line in this way is that it will automatically change your working directory from the current directory to the distribution's home directory.</span></span>

**<span data-ttu-id="5e3b9-120">Пример.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-120">Example:</span></span>**

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

### <a name="wsl-and-wsl-command"></a><span data-ttu-id="5e3b9-121">wsl и wsl [команда]</span><span class="sxs-lookup"><span data-stu-id="5e3b9-121">wsl and wsl [command]</span></span>

<span data-ttu-id="5e3b9-122">Лучший способ запуска WSL из командной строки используется `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-122">The best way to run WSL from the command line is using `wsl.exe`.</span></span>

**<span data-ttu-id="5e3b9-123">Пример.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-123">Example:</span></span>**

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

<span data-ttu-id="5e3b9-124">Не только `wsl` сохранить текущий рабочий каталог на месте, он позволяет выполнить одну команду вдоль стороны команд Windows.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-124">Not only does `wsl` keep the current working directory in place, it lets you run a single command along side Windows commands.</span></span>

**<span data-ttu-id="5e3b9-125">Пример.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-125">Example:</span></span>**

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

**<span data-ttu-id="5e3b9-126">Пример.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-126">Example:</span></span>**

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


## <a name="managing-multiple-linux-distributions"></a><span data-ttu-id="5e3b9-127">Управление несколько дистрибутивов Linux</span><span class="sxs-lookup"><span data-stu-id="5e3b9-127">Managing multiple Linux Distributions</span></span>

### <a name="windows-10-version-1903-and-later"></a><span data-ttu-id="5e3b9-128">1903 и более поздних версий Windows 10</span><span class="sxs-lookup"><span data-stu-id="5e3b9-128">Windows 10 Version 1903 and later</span></span>

<span data-ttu-id="5e3b9-129">Можно использовать `wsl.exe` для управления вашей дистрибутивов в подсистеме Windows для Linux (WSL), включая список дистрибутивов, доступных, задание распространения по умолчанию и при удалении распределений.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-129">You can use `wsl.exe` to manage your distributions in the Windows Subsystem for Linux (WSL), including listing available distributions, setting a default distribution, and uninstalling distributions.</span></span>

<span data-ttu-id="5e3b9-130">Каждый дистрибутив Linux независимо друг от друга управляет свой собственный конфигурациями.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-130">Each Linux distribution independently manages its own configurations.</span></span> <span data-ttu-id="5e3b9-131">Чтобы просмотреть команды конкретного дистрибутива, запустите `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-131">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="5e3b9-132">Например: `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-132">For example `ubuntu /?`.</span></span>

#### <a name="list-distributions"></a><span data-ttu-id="5e3b9-133">Список дистрибутивов</span><span class="sxs-lookup"><span data-stu-id="5e3b9-133">List distributions</span></span>

`wsl -l` <span data-ttu-id="5e3b9-134">,</span><span class="sxs-lookup"><span data-stu-id="5e3b9-134">,</span></span> `wsl --list`  
<span data-ttu-id="5e3b9-135">Перечисляет доступные дистрибутивы Linux, доступных для WSL.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-135">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="5e3b9-136">Если дистрибутив присутствует в списке, он устанавливается и готовую к использованию.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-136">If a distribution is listed, it's installed and ready to use.</span></span>

`wsl --list --all`   
<span data-ttu-id="5e3b9-137">Список всех дистрибутивов, включая те, которые невозможно использовать в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-137">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="5e3b9-138">Они могут быть находится в процессе установки, удаления, или в поврежденном состоянии.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-138">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

`wsl --list --running`   
<span data-ttu-id="5e3b9-139">Список всех дистрибутивов, работающих в данный момент.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-139">Lists all distributions that are currently running.</span></span>

#### <a name="set-a-default-distribution"></a><span data-ttu-id="5e3b9-140">Задайте значение распределения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5e3b9-140">Set a default distribution</span></span>

<span data-ttu-id="5e3b9-141">Распределение WSL по умолчанию является тот, который выполняется при запуске `wsl` в командной строке.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-141">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

`wsl -s <DistributionName>`<span data-ttu-id="5e3b9-142">,</span><span class="sxs-lookup"><span data-stu-id="5e3b9-142">,</span></span> `wsl --setdefault <DistributionName>`

<span data-ttu-id="5e3b9-143">Задает распределение по умолчанию `<DistributionName>`.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-143">Sets the default distribution to `<DistributionName>`.</span></span>

**<span data-ttu-id="5e3b9-144">Пример.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-144">Example:</span></span>**  
`wsl -s Ubuntu` <span data-ttu-id="5e3b9-145">нужно задать моей распространения по умолчанию Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-145">would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="5e3b9-146">Теперь при выполнении `wsl npm init` оно будет выполняться в Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-146">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="5e3b9-147">Если я запущу `wsl` он будет открыт сеанс Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-147">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="5e3b9-148">Отменить регистрацию и повторно установить дистрибутив</span><span class="sxs-lookup"><span data-stu-id="5e3b9-148">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="5e3b9-149">Во время Linux на дистрибутивах можно установить с помощью Windows хранилище, они не предусмотрена в магазине.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-149">While Linux distributions can be installed through the Windows store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="5e3b9-150">WSL Config позволяет дистрибутивов следует отменять регистрацию или удалено.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-150">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="5e3b9-151">При отмене регистрации позволяет дистрибутивов переустановка.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-151">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="5e3b9-152">**Внимание!** После отмены регистрации, все данные, параметры и программное обеспечение, связанное с этой будут безвозвратно утрачены.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-152">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="5e3b9-153">Переустановка в магазине установит чистую копию распределение.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-153">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wsl --unregister <DistributionName>`  
<span data-ttu-id="5e3b9-154">Отменяет регистрацию распространения из WSL для переустановки или очищена.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-154">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="5e3b9-155">Например: `wsl -unregister Ubuntu` удалить из дистрибутивов, доступных в WSL Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-155">For example: `wsl -unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="5e3b9-156">При выполнении `wsl --list` его там нет.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-156">When I run `wsl --list` it will not be listed.</span></span>

<span data-ttu-id="5e3b9-157">Чтобы переустановить, получите распределение в Windows Store и выберите «Запустить».</span><span class="sxs-lookup"><span data-stu-id="5e3b9-157">To reinstall, find the distribution in the Windows Store and select "Launch".</span></span>

#### <a name="run-as-a-specific-user"></a><span data-ttu-id="5e3b9-158">Запуск от имени определенного пользователя</span><span class="sxs-lookup"><span data-stu-id="5e3b9-158">Run as a specific user</span></span>

`wsl -u <Username>`<span data-ttu-id="5e3b9-159">,</span><span class="sxs-lookup"><span data-stu-id="5e3b9-159">,</span></span> `wsl --user <Username>`

<span data-ttu-id="5e3b9-160">WSL Запуск от имени указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-160">Run WSL as the specified user.</span></span> <span data-ttu-id="5e3b9-161">Учтите, что этот пользователь должен существовать внутри WSL распространения.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-161">Please note that user must exist inside of the WSL distribution.</span></span>

#### <a name="run-a-specific-distribution"></a><span data-ttu-id="5e3b9-162">Запустите конкретного распределения</span><span class="sxs-lookup"><span data-stu-id="5e3b9-162">Run a specific distribution</span></span>

`wsl --d <DistributionName>`<span data-ttu-id="5e3b9-163">,</span><span class="sxs-lookup"><span data-stu-id="5e3b9-163">,</span></span> `wsl --distribution <DistributionName>`

<span data-ttu-id="5e3b9-164">Запустите указанный распределение WSL, можно использовать для отправки команд для конкретного распределения не придется менять по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-164">Run a specified distribution of WSL, can be used to send commands to a specific distribution without having to change your default.</span></span>

### <a name="versions-earlier-than-windows-10-version-1903"></a><span data-ttu-id="5e3b9-165">Версии более ранней, чем Windows 10 версии 1903</span><span class="sxs-lookup"><span data-stu-id="5e3b9-165">Versions Earlier than Windows 10 Version 1903</span></span>

<span data-ttu-id="5e3b9-166">WSL Config (`wslconfig.exe`) является средством командной строки для управления дистрибутивов Linux, работающих на подсистеме Windows для Linux (WSL).</span><span class="sxs-lookup"><span data-stu-id="5e3b9-166">WSL Config (`wslconfig.exe`) is a command-line tool for managing Linux distributions running on the Windows Subsystem for Linux (WSL).</span></span>  <span data-ttu-id="5e3b9-167">Он позволяет список дистрибутивов, доступных, задайте значение распределения по умолчанию и удалите распределений.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-167">It lets you list available distributions, set a default distribution, and uninstall distributions.</span></span>

<span data-ttu-id="5e3b9-168">Несмотря на то полезные параметры, охватывающие или координировать дистрибутивов WSL Config, каждый дистрибутив Linux независимо друг от друга управляет свой собственный конфигурациями.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-168">While WSL Config is helpful for settings that span or coordinate distributions, each Linux distribution independently manages its own configurations.</span></span>  <span data-ttu-id="5e3b9-169">Чтобы просмотреть команды конкретного дистрибутива, запустите `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-169">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="5e3b9-170">Например: `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-170">For example `ubuntu /?`.</span></span>

<span data-ttu-id="5e3b9-171">Чтобы просмотреть все доступные параметры для wslconfig, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="5e3b9-171">To see all available options for wslconfig, run:</span></span>  `wslconfig /?`

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

#### <a name="list-distributions"></a><span data-ttu-id="5e3b9-172">Список дистрибутивов</span><span class="sxs-lookup"><span data-stu-id="5e3b9-172">List distributions</span></span>

`wslconfig /list`  
<span data-ttu-id="5e3b9-173">Перечисляет доступные дистрибутивы Linux, доступных для WSL.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-173">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="5e3b9-174">Если дистрибутив присутствует в списке, он устанавливается и готовую к использованию.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-174">If a distribution is listed, it's installed and ready to use.</span></span>

`wslconfig /list /all`  
<span data-ttu-id="5e3b9-175">Список всех дистрибутивов, включая те, которые невозможно использовать в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-175">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="5e3b9-176">Они могут быть находится в процессе установки, удаления, или в поврежденном состоянии.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-176">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

#### <a name="set-a-default-distribution"></a><span data-ttu-id="5e3b9-177">Задайте значение распределения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5e3b9-177">Set a default distribution</span></span>

<span data-ttu-id="5e3b9-178">Распределение WSL по умолчанию является тот, который выполняется при запуске `wsl` в командной строке.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-178">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

`wslconfig /setdefault <DistributionName>`

<span data-ttu-id="5e3b9-179">Задает распределение по умолчанию `<DistributionName>`.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-179">Sets the default distribution to `<DistributionName>`.</span></span>

**<span data-ttu-id="5e3b9-180">Пример.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-180">Example:</span></span>**  
`wslconfig /setdefault Ubuntu` <span data-ttu-id="5e3b9-181">нужно задать моей распространения по умолчанию Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-181">would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="5e3b9-182">Теперь при выполнении `wsl npm init` оно будет выполняться в Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-182">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="5e3b9-183">Если я запущу `wsl` он будет открыт сеанс Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-183">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="5e3b9-184">Отменить регистрацию и повторно установить дистрибутив</span><span class="sxs-lookup"><span data-stu-id="5e3b9-184">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="5e3b9-185">Во время Linux на дистрибутивах можно установить с помощью Windows хранилище, они не предусмотрена в магазине.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-185">While Linux distributions can be installed through the Windows store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="5e3b9-186">WSL Config позволяет дистрибутивов следует отменять регистрацию или удалено.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-186">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="5e3b9-187">При отмене регистрации позволяет дистрибутивов переустановка.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-187">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="5e3b9-188">**Внимание!** После отмены регистрации, все данные, параметры и программное обеспечение, связанное с этой будут безвозвратно утрачены.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-188">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="5e3b9-189">Переустановка в магазине установит чистую копию распределение.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-189">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wslconfig /unregister <DistributionName>`  
<span data-ttu-id="5e3b9-190">Отменяет регистрацию распространения из WSL для переустановки или очищена.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-190">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="5e3b9-191">Например: `wslconfig /unregister Ubuntu` удалить из дистрибутивов, доступных в WSL Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-191">For example: `wslconfig /unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="5e3b9-192">При выполнении `wslconfig /list` его там нет.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-192">When I run `wslconfig /list` it will not be listed.</span></span>

<span data-ttu-id="5e3b9-193">Чтобы переустановить, получите распределение в Windows Store и выберите «Запустить».</span><span class="sxs-lookup"><span data-stu-id="5e3b9-193">To reinstall, find the distribution in the Windows Store and select "Launch".</span></span>

## <a name="set-wsl-launch-settings"></a><span data-ttu-id="5e3b9-194">Задать параметры запуска WSL</span><span class="sxs-lookup"><span data-stu-id="5e3b9-194">Set WSL launch settings</span></span>

> **<span data-ttu-id="5e3b9-195">В 17093 сборки программы предварительной оценки Windows и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="5e3b9-195">Available in Windows Insider Build 17093 and later</span></span>**

<span data-ttu-id="5e3b9-196">Автоматическая настройка определенных функций в WSL, которая будет применяться каждый раз при запуске подсистемы с помощью `wsl.conf`.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-196">Automatically configure certain functionality in WSL that will be applied every time you launch the subsystem using `wsl.conf`.</span></span> 

<span data-ttu-id="5e3b9-197">Право, это включает в себя автоподключения параметры и конфигурации сети.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-197">Right now, this includes automount options and network configuration.</span></span>

`wsl.conf` <span data-ttu-id="5e3b9-198">расположен в каждый дистрибутив Linux в `/etc/wsl.conf`.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-198">is located in each Linux distribution in `/etc/wsl.conf`.</span></span> <span data-ttu-id="5e3b9-199">Если файл не существует, можно создать его самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-199">If the file is not there, you can create it yourself.</span></span> <span data-ttu-id="5e3b9-200">WSL будет проверки существования файла и будет считать его содержимое.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-200">WSL will detect the existence of the file and will read its contents.</span></span> <span data-ttu-id="5e3b9-201">Если файл отсутствует или имеет неправильный формат (то есть неправильного форматирования разметки), WSL по-прежнему запустить в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-201">If the file is missing or malformed (that is, improper markup formatting), WSL will continue to launch as normal.</span></span>

<span data-ttu-id="5e3b9-202">Ниже приведен пример `wsl.conf` файл, можно добавить в ваш дистрибутивов:</span><span class="sxs-lookup"><span data-stu-id="5e3b9-202">Here is a sample `wsl.conf` file you could add into your distros:</span></span>

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

### <a name="configuration-options"></a><span data-ttu-id="5e3b9-203">Параметры конфигурации</span><span class="sxs-lookup"><span data-stu-id="5e3b9-203">Configuration Options</span></span>

<span data-ttu-id="5e3b9-204">В соответствии с соглашения INI-файле ключи, объявляются в разделе.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-204">In keeping with .ini conventions, keys are declared under a section.</span></span> 

<span data-ttu-id="5e3b9-205">WSL поддерживает два раздела: `automount` и `network`.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-205">WSL supports two sections: `automount` and `network`.</span></span>

#### <a name="automount"></a><span data-ttu-id="5e3b9-206">Автоподключение</span><span class="sxs-lookup"><span data-stu-id="5e3b9-206">automount</span></span>

<span data-ttu-id="5e3b9-207">Раздел:</span><span class="sxs-lookup"><span data-stu-id="5e3b9-207">Section:</span></span> `[automount]`


| <span data-ttu-id="5e3b9-208">ключ</span><span class="sxs-lookup"><span data-stu-id="5e3b9-208">key</span></span>        | <span data-ttu-id="5e3b9-209">value</span><span class="sxs-lookup"><span data-stu-id="5e3b9-209">value</span></span>                          | <span data-ttu-id="5e3b9-210">значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5e3b9-210">default</span></span>      | <span data-ttu-id="5e3b9-211">Примечания</span><span class="sxs-lookup"><span data-stu-id="5e3b9-211">notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e3b9-212">enabled</span><span class="sxs-lookup"><span data-stu-id="5e3b9-212">enabled</span></span>    | <span data-ttu-id="5e3b9-213">Логический</span><span class="sxs-lookup"><span data-stu-id="5e3b9-213">boolean</span></span>                        | <span data-ttu-id="5e3b9-214">true</span><span class="sxs-lookup"><span data-stu-id="5e3b9-214">true</span></span>         | `true` <span data-ttu-id="5e3b9-215">причины жесткими дисками (например)</span><span class="sxs-lookup"><span data-stu-id="5e3b9-215">causes fixed drives (i.e</span></span> `C:/` <span data-ttu-id="5e3b9-216">или `D:/`) автоматически монтируется с DrvFs под `/mnt`.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-216">or `D:/`) to be automatically mounted with DrvFs under `/mnt`.</span></span>  `false` <span data-ttu-id="5e3b9-217">означает, что диски не будут устанавливаться автоматически, но вы может по-прежнему подключить их вручную или с помощью `fstab`.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-217">means drives won’t be mounted automatically, but you could still mount them manually or via `fstab`.</span></span>                                                                                                             |
| <span data-ttu-id="5e3b9-218">mountFsTab</span><span class="sxs-lookup"><span data-stu-id="5e3b9-218">mountFsTab</span></span> | <span data-ttu-id="5e3b9-219">Логический</span><span class="sxs-lookup"><span data-stu-id="5e3b9-219">boolean</span></span>                        | <span data-ttu-id="5e3b9-220">true</span><span class="sxs-lookup"><span data-stu-id="5e3b9-220">true</span></span>         | `true` <span data-ttu-id="5e3b9-221">Задает `/etc/fstab` должны быть обработаны при запуске WSL.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-221">sets `/etc/fstab` to be processed on WSL start.</span></span> <span data-ttu-id="5e3b9-222">/ etc/fstab — это файл, где можно объявить другие файловые системы, таких как SMB-ресурса.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-222">/etc/fstab is a file where you can declare other filesystems, like an SMB share.</span></span> <span data-ttu-id="5e3b9-223">Таким образом вы можете подключить эти файловые системы автоматически в WSL при запуске копирования.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-223">Thus, you can mount these filesystems automatically in WSL on start up.</span></span>                                                                                                                |
| <span data-ttu-id="5e3b9-224">Корневой</span><span class="sxs-lookup"><span data-stu-id="5e3b9-224">root</span></span>       | <span data-ttu-id="5e3b9-225">Строка</span><span class="sxs-lookup"><span data-stu-id="5e3b9-225">String</span></span>                         | `/mnt/`      | <span data-ttu-id="5e3b9-226">Задает каталог, куда будет автоматически подключен фиксированных дисков.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-226">Sets the directory where fixed drives will be automatically mounted.</span></span> <span data-ttu-id="5e3b9-227">Например, если имеется каталог в WSL в `/windir/` и указать, что в качестве привилегированного пользователя, можно ожидать см. в разделе основных дисков, подключенный к</span><span class="sxs-lookup"><span data-stu-id="5e3b9-227">For example, if you have a directory in WSL at `/windir/` and you specify that as the root, you would expect to see your fixed drives mounted at</span></span> `/windir/c`                                                                                              |
| <span data-ttu-id="5e3b9-228">параметры</span><span class="sxs-lookup"><span data-stu-id="5e3b9-228">options</span></span>    | <span data-ttu-id="5e3b9-229">Разделенный запятыми список значений</span><span class="sxs-lookup"><span data-stu-id="5e3b9-229">comma-separated list of values</span></span> | <span data-ttu-id="5e3b9-230">Пустая строка</span><span class="sxs-lookup"><span data-stu-id="5e3b9-230">empty string</span></span> | <span data-ttu-id="5e3b9-231">Это значение добавляется к строке по умолчанию DrvFs подключения параметры.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-231">This value is appended to the default DrvFs mount options string.</span></span> **<span data-ttu-id="5e3b9-232">Можно указать только параметры, относящиеся к DrvFs.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-232">Only DrvFs-specific options can be specified.</span></span>** <span data-ttu-id="5e3b9-233">Параметры, которые двоичный подключения обычно синтаксического анализа, в флаг не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-233">Options that the mount binary would normally parse into a flag are not supported.</span></span> <span data-ttu-id="5e3b9-234">Если вы хотите явно указать эти параметры, необходимо включить каждый диск, для которого вы хотите сделать это в/etc/fstab.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-234">If you want to explicitly specify those options, you must include every drive for which you want to do so in /etc/fstab.</span></span> |

<span data-ttu-id="5e3b9-235">По умолчанию WSL задает uid и gid значению пользователя по умолчанию (в дистрибутивах Ubuntu пользователя по умолчанию создается с uid = 1000, gid = 1000).</span><span class="sxs-lookup"><span data-stu-id="5e3b9-235">By default, WSL sets the uid and gid to the value of the default user (in Ubuntu distro, the default user is created with uid=1000,gid=1000).</span></span> <span data-ttu-id="5e3b9-236">Если пользователь задал параметр gid или uid, явно с помощью этого ключа, связанного значения будут перезаписаны.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-236">If the user specifies a gid or uid option explicitly via this key, the associated value will be overwritten.</span></span> <span data-ttu-id="5e3b9-237">В противном случае — значение по умолчанию всегда быть добавлены.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-237">Otherwise, the default value will always be appended.</span></span>

<span data-ttu-id="5e3b9-238">**Примечание.** Эти параметры применяются как параметры подключения для всех автоматически подключенные диски.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-238">**Note:** These options are applied as the mount options for all automatically mounted drives.</span></span> <span data-ttu-id="5e3b9-239">Чтобы изменить параметры для определенных дисках, вместо этого используйте/etc/fstab.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-239">To change the options for a specific drive only, use /etc/fstab instead.</span></span>

#### <a name="network"></a><span data-ttu-id="5e3b9-240">сеть</span><span class="sxs-lookup"><span data-stu-id="5e3b9-240">network</span></span>

<span data-ttu-id="5e3b9-241">Метка раздел:</span><span class="sxs-lookup"><span data-stu-id="5e3b9-241">Section label:</span></span> `[network]`

| <span data-ttu-id="5e3b9-242">ключ</span><span class="sxs-lookup"><span data-stu-id="5e3b9-242">key</span></span> | <span data-ttu-id="5e3b9-243">value</span><span class="sxs-lookup"><span data-stu-id="5e3b9-243">value</span></span> | <span data-ttu-id="5e3b9-244">значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5e3b9-244">default</span></span> | <span data-ttu-id="5e3b9-245">Примечания</span><span class="sxs-lookup"><span data-stu-id="5e3b9-245">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="5e3b9-246">generateHosts</span><span class="sxs-lookup"><span data-stu-id="5e3b9-246">generateHosts</span></span> | <span data-ttu-id="5e3b9-247">Логический</span><span class="sxs-lookup"><span data-stu-id="5e3b9-247">boolean</span></span> | `true` | `true` <span data-ttu-id="5e3b9-248">Задает WSL для создания `/etc/hosts`.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-248">sets WSL to generate `/etc/hosts`.</span></span> <span data-ttu-id="5e3b9-249">`hosts` Файл содержит карту статические IP-адреса, соответствующие имена узлов.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-249">The `hosts` file contains a static map of hostnames corresponding IP address.</span></span> |
| <span data-ttu-id="5e3b9-250">generateResolvConf</span><span class="sxs-lookup"><span data-stu-id="5e3b9-250">generateResolvConf</span></span> | <span data-ttu-id="5e3b9-251">Логический</span><span class="sxs-lookup"><span data-stu-id="5e3b9-251">boolean</span></span> | `true` | `true` <span data-ttu-id="5e3b9-252">Задайте WSL для создания `/etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-252">set WSL to generate `/etc/resolv.conf`.</span></span> <span data-ttu-id="5e3b9-253">`resolv.conf` Со списком DNS, которые может разрешить данное имя узла, IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-253">The `resolv.conf` contains a DNS list that are capable of resolving a given hostname to its IP address.</span></span> | 

#### <a name="interop"></a><span data-ttu-id="5e3b9-254">Взаимодействия</span><span class="sxs-lookup"><span data-stu-id="5e3b9-254">interop</span></span>

<span data-ttu-id="5e3b9-255">Метка раздел:</span><span class="sxs-lookup"><span data-stu-id="5e3b9-255">Section label:</span></span> `[interop]`

<span data-ttu-id="5e3b9-256">Эти параметры становятся доступными в 17713 сборки программы предварительной оценки и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-256">These options are available in Insider Build 17713 and later.</span></span>

| <span data-ttu-id="5e3b9-257">ключ</span><span class="sxs-lookup"><span data-stu-id="5e3b9-257">key</span></span> | <span data-ttu-id="5e3b9-258">value</span><span class="sxs-lookup"><span data-stu-id="5e3b9-258">value</span></span> | <span data-ttu-id="5e3b9-259">значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5e3b9-259">default</span></span> | <span data-ttu-id="5e3b9-260">Примечания</span><span class="sxs-lookup"><span data-stu-id="5e3b9-260">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="5e3b9-261">enabled</span><span class="sxs-lookup"><span data-stu-id="5e3b9-261">enabled</span></span> | <span data-ttu-id="5e3b9-262">Логический</span><span class="sxs-lookup"><span data-stu-id="5e3b9-262">boolean</span></span> | `true` | <span data-ttu-id="5e3b9-263">Параметр этот ключ будет определить, поддерживает ли WSL запуска процессов Windows.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-263">Setting this key will determine whether WSL will support launching Windows processes.</span></span> |
| <span data-ttu-id="5e3b9-264">appendWindowsPath</span><span class="sxs-lookup"><span data-stu-id="5e3b9-264">appendWindowsPath</span></span> | <span data-ttu-id="5e3b9-265">Логический</span><span class="sxs-lookup"><span data-stu-id="5e3b9-265">boolean</span></span> | `true` | <span data-ttu-id="5e3b9-266">Параметр этот ключ будет определять, добавит ли WSL элементы Windows пути в переменную $PATH.</span><span class="sxs-lookup"><span data-stu-id="5e3b9-266">Setting this key will determine whether WSL will add Windows path elements to the $PATH environment variable.</span></span> | 
