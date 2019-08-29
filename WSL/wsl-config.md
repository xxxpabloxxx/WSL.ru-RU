---
title: Управление дистрибутивами Linux
description: Список ссылок и настройка нескольких дистрибутивов Linux, работающих в подсистеме Windows для Linux.
keywords: Башонвиндовс, bash, WSL, Windows, подсистема Windows для Linux, виндовссубсистем, Ubuntu, WSL. conf, вслконфиг
author: scooley
ms.author: scooley
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: ca65cf6fde3e0ba4750ffc44f5aec542be6cfabf
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122706"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a><span data-ttu-id="3730e-104">Управление подсистемой Windows для Linux и ее настройка</span><span class="sxs-lookup"><span data-stu-id="3730e-104">Manage and configure Windows Subsystem for Linux</span></span>

> <span data-ttu-id="3730e-105">Применяется к обновлениям Windows 10 для дизайнеров и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="3730e-105">Applies to Windows 10 Fall Creators Update and later.</span></span>  <span data-ttu-id="3730e-106">Ознакомьтесь с нашим обновленным [руководством по установке](./install_guide.md) , чтобы опробовать новые функции управления и запустить несколько дистрибутивов Linux из Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="3730e-106">See our updated [installation guide](./install_guide.md) to try new management features and start running multiple Linux distributions from the Microsoft store.</span></span>

## <a name="ways-to-run-wsl"></a><span data-ttu-id="3730e-107">Способы запуска WSL</span><span class="sxs-lookup"><span data-stu-id="3730e-107">Ways to run WSL</span></span>

<span data-ttu-id="3730e-108">Существует множество способов запуска Linux с подсистемой Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="3730e-108">There are many ways to run Linux with the Windows Subsystem for Linux.</span></span>

1. <span data-ttu-id="3730e-109">`[distro]`Например`ubuntu`</span><span class="sxs-lookup"><span data-stu-id="3730e-109">`[distro]`, for example `ubuntu`</span></span>
1. <span data-ttu-id="3730e-110">`wsl.exe` или `bash.exe`</span><span class="sxs-lookup"><span data-stu-id="3730e-110">`wsl.exe` or `bash.exe`</span></span>
1. <span data-ttu-id="3730e-111">`wsl [command]` или `bash -c [command]`</span><span class="sxs-lookup"><span data-stu-id="3730e-111">`wsl [command]` or `bash -c [command]`</span></span>

<span data-ttu-id="3730e-112">Какой метод следует использовать, зависит от того, что вы делаете.</span><span class="sxs-lookup"><span data-stu-id="3730e-112">Which method you should use depends on what you're doing.</span></span>

### <a name="launch-wsl-by-distribution"></a><span data-ttu-id="3730e-113">Запустить WSL по распределению</span><span class="sxs-lookup"><span data-stu-id="3730e-113">Launch WSL by distribution</span></span>

<span data-ttu-id="3730e-114">Запуск распространения с помощью приложения дистрибутив запускает это распространение в собственном окне консоли.</span><span class="sxs-lookup"><span data-stu-id="3730e-114">Running a distribution using it's distro-specific application launches that distribution in it's own console window.</span></span>

![Запуск WSL из меню "Пуск"](media/start-launch.png)

<span data-ttu-id="3730e-116">Это то же самое, что и при нажатии кнопки "запустить" в Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="3730e-116">It is the same as clicking "Launch" in the Microsoft store.</span></span>

![Запуск WSL из Microsoft Store](media/store-launch.png)

<span data-ttu-id="3730e-118">Можно также запустить распространение из командной строки, выполнив `[distribution].exe`команду.</span><span class="sxs-lookup"><span data-stu-id="3730e-118">You can also run the distribution from the command line by running `[distribution].exe`.</span></span>

<span data-ttu-id="3730e-119">Недостаток выполнения дистрибутива из командной строки заключается в том, что он автоматически изменит рабочий каталог из текущего каталога на домашний каталог дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="3730e-119">The disadvantage of running a distribution from the command line in this way is that it will automatically change your working directory from the current directory to the distribution's home directory.</span></span>

<span data-ttu-id="3730e-120">**Например**</span><span class="sxs-lookup"><span data-stu-id="3730e-120">**Example:**</span></span>

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

### <a name="wsl-and-wsl-command"></a><span data-ttu-id="3730e-121">WSL и WSL [команда]</span><span class="sxs-lookup"><span data-stu-id="3730e-121">wsl and wsl [command]</span></span>

<span data-ttu-id="3730e-122">Лучший способ запуска WSL из командной строки — использовать `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="3730e-122">The best way to run WSL from the command line is using `wsl.exe`.</span></span>

<span data-ttu-id="3730e-123">**Например**</span><span class="sxs-lookup"><span data-stu-id="3730e-123">**Example:**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

<span data-ttu-id="3730e-124">Текущий рабочий каталог `wsl` не только сохраняется, но и позволяет выполнять одну команду с командами Windows.</span><span class="sxs-lookup"><span data-stu-id="3730e-124">Not only does `wsl` keep the current working directory in place, it lets you run a single command along side Windows commands.</span></span>

<span data-ttu-id="3730e-125">**Например**</span><span class="sxs-lookup"><span data-stu-id="3730e-125">**Example:**</span></span>

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

<span data-ttu-id="3730e-126">**Например**</span><span class="sxs-lookup"><span data-stu-id="3730e-126">**Example:**</span></span>

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


## <a name="managing-multiple-linux-distributions"></a><span data-ttu-id="3730e-127">Управление несколькими дистрибутивами Linux</span><span class="sxs-lookup"><span data-stu-id="3730e-127">Managing multiple Linux Distributions</span></span>

### <a name="windows-10-version-1903-and-later"></a><span data-ttu-id="3730e-128">Windows 10 версии 1903 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="3730e-128">Windows 10 Version 1903 and later</span></span>

<span data-ttu-id="3730e-129">Вы можете использовать `wsl.exe` для управления дистрибутивами в подсистеме Windows для Linux (WSL), включая список доступных дистрибутивов, настройку распределения по умолчанию и удаление дистрибутивов.</span><span class="sxs-lookup"><span data-stu-id="3730e-129">You can use `wsl.exe` to manage your distributions in the Windows Subsystem for Linux (WSL), including listing available distributions, setting a default distribution, and uninstalling distributions.</span></span>

<span data-ttu-id="3730e-130">Каждый дистрибутив Linux независимо управляет собственными конфигурациями.</span><span class="sxs-lookup"><span data-stu-id="3730e-130">Each Linux distribution independently manages its own configurations.</span></span> <span data-ttu-id="3730e-131">Чтобы просмотреть команды, относящиеся к распространению `[distro.exe] /?`, выполните команду.</span><span class="sxs-lookup"><span data-stu-id="3730e-131">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="3730e-132">Например: `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="3730e-132">For example `ubuntu /?`.</span></span>

#### <a name="list-distributions"></a><span data-ttu-id="3730e-133">Вывод списка распределений</span><span class="sxs-lookup"><span data-stu-id="3730e-133">List distributions</span></span>

<span data-ttu-id="3730e-134">`wsl -l`,`wsl --list`</span><span class="sxs-lookup"><span data-stu-id="3730e-134">`wsl -l` , `wsl --list`</span></span>  
<span data-ttu-id="3730e-135">Список доступных дистрибутивов Linux, доступных для WSL.</span><span class="sxs-lookup"><span data-stu-id="3730e-135">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="3730e-136">Если распространение указано, оно будет установлено и готово к использованию.</span><span class="sxs-lookup"><span data-stu-id="3730e-136">If a distribution is listed, it's installed and ready to use.</span></span>

`wsl --list --all`   
<span data-ttu-id="3730e-137">Список всех дистрибутивов, включая те, которые сейчас не используются.</span><span class="sxs-lookup"><span data-stu-id="3730e-137">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="3730e-138">Возможно, они находятся в процессе установки, удаления или находятся в неработающем состоянии.</span><span class="sxs-lookup"><span data-stu-id="3730e-138">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

`wsl --list --running`   
<span data-ttu-id="3730e-139">Список всех распределений, выполняемых в данный момент.</span><span class="sxs-lookup"><span data-stu-id="3730e-139">Lists all distributions that are currently running.</span></span>

#### <a name="set-a-default-distribution"></a><span data-ttu-id="3730e-140">Настройка распределения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3730e-140">Set a default distribution</span></span>

<span data-ttu-id="3730e-141">По умолчанию используется дистрибутив WSL, который выполняется при выполнении `wsl` в командной строке.</span><span class="sxs-lookup"><span data-stu-id="3730e-141">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

<span data-ttu-id="3730e-142">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="3730e-142">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span></span>

<span data-ttu-id="3730e-143">Задает для распределения по умолчанию значение `<DistributionName>`.</span><span class="sxs-lookup"><span data-stu-id="3730e-143">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="3730e-144">**Например**</span><span class="sxs-lookup"><span data-stu-id="3730e-144">**Example:**</span></span>  
<span data-ttu-id="3730e-145">`wsl -s Ubuntu`в качестве дистрибутива по умолчанию устанавливается Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="3730e-145">`wsl -s Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="3730e-146">Теперь, когда я `wsl npm init` запускаю, он будет запущен в Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="3730e-146">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="3730e-147">При запуске `wsl` откроется сеанс Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="3730e-147">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="3730e-148">Отмена регистрации и повторная установка распространения</span><span class="sxs-lookup"><span data-stu-id="3730e-148">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="3730e-149">Хотя дистрибутивы Linux можно устанавливать через Microsoft Store, их нельзя удалить в магазине.</span><span class="sxs-lookup"><span data-stu-id="3730e-149">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="3730e-150">WSL config позволяет отменить регистрацию или удаление дистрибутивов.</span><span class="sxs-lookup"><span data-stu-id="3730e-150">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="3730e-151">Отмена регистрации также позволяет переустановить дистрибутивы.</span><span class="sxs-lookup"><span data-stu-id="3730e-151">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="3730e-152">**Внимание!** После отмены регистрации все данные, параметры и программное обеспечение, связанные с этим распределением, будут безвозвратно утеряны.</span><span class="sxs-lookup"><span data-stu-id="3730e-152">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="3730e-153">При переустановке из хранилища будет установлена чистая копия дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="3730e-153">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wsl --unregister <DistributionName>`  
<span data-ttu-id="3730e-154">Отменяет регистрацию дистрибутива в WSL, чтобы его можно было переустановить или очистить.</span><span class="sxs-lookup"><span data-stu-id="3730e-154">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="3730e-155">Например: `wsl --unregister Ubuntu` приведет к удалению Ubuntu из дистрибутивов, доступных в WSL.</span><span class="sxs-lookup"><span data-stu-id="3730e-155">For example: `wsl --unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="3730e-156">При запуске `wsl --list` он не будет перечислен.</span><span class="sxs-lookup"><span data-stu-id="3730e-156">When I run `wsl --list` it will not be listed.</span></span>

<span data-ttu-id="3730e-157">Чтобы переустановить, найдите дистрибутив в Microsoft Store и нажмите кнопку "запустить".</span><span class="sxs-lookup"><span data-stu-id="3730e-157">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

#### <a name="run-as-a-specific-user"></a><span data-ttu-id="3730e-158">Запуск от имени определенного пользователя</span><span class="sxs-lookup"><span data-stu-id="3730e-158">Run as a specific user</span></span>

<span data-ttu-id="3730e-159">`wsl -u <Username>`, `wsl --user <Username>`</span><span class="sxs-lookup"><span data-stu-id="3730e-159">`wsl -u <Username>`, `wsl --user <Username>`</span></span>

<span data-ttu-id="3730e-160">Запустите WSL от имени указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="3730e-160">Run WSL as the specified user.</span></span> <span data-ttu-id="3730e-161">Обратите внимание, что пользователь должен существовать в дистрибутиве WSL.</span><span class="sxs-lookup"><span data-stu-id="3730e-161">Please note that user must exist inside of the WSL distribution.</span></span>

#### <a name="run-a-specific-distribution"></a><span data-ttu-id="3730e-162">Запуск определенного распределения</span><span class="sxs-lookup"><span data-stu-id="3730e-162">Run a specific distribution</span></span>

<span data-ttu-id="3730e-163">`wsl --d <DistributionName>`, `wsl --distribution <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="3730e-163">`wsl --d <DistributionName>`, `wsl --distribution <DistributionName>`</span></span>

<span data-ttu-id="3730e-164">Выполнение указанного распределения WSL можно использовать для отправки команд в определенное распределение без необходимости изменения значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3730e-164">Run a specified distribution of WSL, can be used to send commands to a specific distribution without having to change your default.</span></span>

### <a name="versions-earlier-than-windows-10-version-1903"></a><span data-ttu-id="3730e-165">Версии более ранние, чем Windows 10 версии 1903</span><span class="sxs-lookup"><span data-stu-id="3730e-165">Versions Earlier than Windows 10 Version 1903</span></span>

<span data-ttu-id="3730e-166">WSL config (`wslconfig.exe`) — это программа командной строки для управления дистрибутивами Linux, работающими в подсистеме Windows для Linux (WSL).</span><span class="sxs-lookup"><span data-stu-id="3730e-166">WSL Config (`wslconfig.exe`) is a command-line tool for managing Linux distributions running on the Windows Subsystem for Linux (WSL).</span></span>  <span data-ttu-id="3730e-167">Он позволяет перечислить доступные дистрибутивы, настроить распределение по умолчанию и удалить дистрибутивы.</span><span class="sxs-lookup"><span data-stu-id="3730e-167">It lets you list available distributions, set a default distribution, and uninstall distributions.</span></span>

<span data-ttu-id="3730e-168">Хотя WSL config полезен для параметров, охватывающих или координирующих распределения, каждый дистрибутив Linux независимо управляет собственными конфигурациями.</span><span class="sxs-lookup"><span data-stu-id="3730e-168">While WSL Config is helpful for settings that span or coordinate distributions, each Linux distribution independently manages its own configurations.</span></span>  <span data-ttu-id="3730e-169">Чтобы просмотреть команды, относящиеся к распространению `[distro.exe] /?`, выполните команду.</span><span class="sxs-lookup"><span data-stu-id="3730e-169">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="3730e-170">Например: `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="3730e-170">For example `ubuntu /?`.</span></span>

<span data-ttu-id="3730e-171">Чтобы просмотреть все доступные параметры для вслконфиг, выполните команду:`wslconfig /?`</span><span class="sxs-lookup"><span data-stu-id="3730e-171">To see all available options for wslconfig, run:  `wslconfig /?`</span></span>

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

#### <a name="list-distributions"></a><span data-ttu-id="3730e-172">Вывод списка распределений</span><span class="sxs-lookup"><span data-stu-id="3730e-172">List distributions</span></span>

`wslconfig /list`  
<span data-ttu-id="3730e-173">Список доступных дистрибутивов Linux, доступных для WSL.</span><span class="sxs-lookup"><span data-stu-id="3730e-173">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="3730e-174">Если распространение указано, оно будет установлено и готово к использованию.</span><span class="sxs-lookup"><span data-stu-id="3730e-174">If a distribution is listed, it's installed and ready to use.</span></span>

`wslconfig /list /all`  
<span data-ttu-id="3730e-175">Список всех дистрибутивов, включая те, которые сейчас не используются.</span><span class="sxs-lookup"><span data-stu-id="3730e-175">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="3730e-176">Возможно, они находятся в процессе установки, удаления или находятся в неработающем состоянии.</span><span class="sxs-lookup"><span data-stu-id="3730e-176">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

#### <a name="set-a-default-distribution"></a><span data-ttu-id="3730e-177">Настройка распределения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3730e-177">Set a default distribution</span></span>

<span data-ttu-id="3730e-178">По умолчанию используется дистрибутив WSL, который выполняется при выполнении `wsl` в командной строке.</span><span class="sxs-lookup"><span data-stu-id="3730e-178">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

`wslconfig /setdefault <DistributionName>`

<span data-ttu-id="3730e-179">Задает для распределения по умолчанию значение `<DistributionName>`.</span><span class="sxs-lookup"><span data-stu-id="3730e-179">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="3730e-180">**Например**</span><span class="sxs-lookup"><span data-stu-id="3730e-180">**Example:**</span></span>  
<span data-ttu-id="3730e-181">`wslconfig /setdefault Ubuntu`в качестве дистрибутива по умолчанию устанавливается Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="3730e-181">`wslconfig /setdefault Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="3730e-182">Теперь, когда я `wsl npm init` запускаю, он будет запущен в Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="3730e-182">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="3730e-183">При запуске `wsl` откроется сеанс Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="3730e-183">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="3730e-184">Отмена регистрации и повторная установка распространения</span><span class="sxs-lookup"><span data-stu-id="3730e-184">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="3730e-185">Хотя дистрибутивы Linux можно устанавливать через Microsoft Store, их нельзя удалить в магазине.</span><span class="sxs-lookup"><span data-stu-id="3730e-185">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="3730e-186">WSL config позволяет отменить регистрацию или удаление дистрибутивов.</span><span class="sxs-lookup"><span data-stu-id="3730e-186">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="3730e-187">Отмена регистрации также позволяет переустановить дистрибутивы.</span><span class="sxs-lookup"><span data-stu-id="3730e-187">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="3730e-188">**Внимание!** После отмены регистрации все данные, параметры и программное обеспечение, связанные с этим распределением, будут безвозвратно утеряны.</span><span class="sxs-lookup"><span data-stu-id="3730e-188">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="3730e-189">При переустановке из хранилища будет установлена чистая копия дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="3730e-189">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wslconfig /unregister <DistributionName>`  
<span data-ttu-id="3730e-190">Отменяет регистрацию дистрибутива в WSL, чтобы его можно было переустановить или очистить.</span><span class="sxs-lookup"><span data-stu-id="3730e-190">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="3730e-191">Например: `wslconfig /unregister Ubuntu` приведет к удалению Ubuntu из дистрибутивов, доступных в WSL.</span><span class="sxs-lookup"><span data-stu-id="3730e-191">For example: `wslconfig /unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="3730e-192">При запуске `wslconfig /list` он не будет перечислен.</span><span class="sxs-lookup"><span data-stu-id="3730e-192">When I run `wslconfig /list` it will not be listed.</span></span>

<span data-ttu-id="3730e-193">Чтобы переустановить, найдите дистрибутив в Microsoft Store и нажмите кнопку "запустить".</span><span class="sxs-lookup"><span data-stu-id="3730e-193">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="set-wsl-launch-settings"></a><span data-ttu-id="3730e-194">Задать параметры запуска WSL</span><span class="sxs-lookup"><span data-stu-id="3730e-194">Set WSL launch settings</span></span>

> <span data-ttu-id="3730e-195">**Доступно в сборке Windows Insider Build 17093 и более поздних версий**</span><span class="sxs-lookup"><span data-stu-id="3730e-195">**Available in Windows Insider Build 17093 and later**</span></span>

<span data-ttu-id="3730e-196">Автоматическая настройка определенных функций в WSL, которые будут применяться при каждом запуске подсистемы с помощью `wsl.conf`.</span><span class="sxs-lookup"><span data-stu-id="3730e-196">Automatically configure certain functionality in WSL that will be applied every time you launch the subsystem using `wsl.conf`.</span></span> 

<span data-ttu-id="3730e-197">Сейчас сюда входят параметры автоподключения и конфигурация сети.</span><span class="sxs-lookup"><span data-stu-id="3730e-197">Right now, this includes automount options and network configuration.</span></span>

<span data-ttu-id="3730e-198">`wsl.conf`находится в каждом дистрибутиве Linux в `/etc/wsl.conf`.</span><span class="sxs-lookup"><span data-stu-id="3730e-198">`wsl.conf` is located in each Linux distribution in `/etc/wsl.conf`.</span></span> <span data-ttu-id="3730e-199">Если файл отсутствует, его можно создать самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="3730e-199">If the file is not there, you can create it yourself.</span></span> <span data-ttu-id="3730e-200">WSL обнаружит наличие файла и прочитает его содержимое.</span><span class="sxs-lookup"><span data-stu-id="3730e-200">WSL will detect the existence of the file and will read its contents.</span></span> <span data-ttu-id="3730e-201">Если файл отсутствует или имеет неправильный формат (т. е. неправильное форматирование разметки), WSL будет продолжать запускаться как обычная.</span><span class="sxs-lookup"><span data-stu-id="3730e-201">If the file is missing or malformed (that is, improper markup formatting), WSL will continue to launch as normal.</span></span>

<span data-ttu-id="3730e-202">Ниже приведен пример `wsl.conf` файла, который можно добавить в дистрибутивов:</span><span class="sxs-lookup"><span data-stu-id="3730e-202">Here is a sample `wsl.conf` file you could add into your distros:</span></span>

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

### <a name="configuration-options"></a><span data-ttu-id="3730e-203">Параметры конфигурации</span><span class="sxs-lookup"><span data-stu-id="3730e-203">Configuration Options</span></span>

<span data-ttu-id="3730e-204">В соответствии с соглашениями. ini ключи объявляются в разделе.</span><span class="sxs-lookup"><span data-stu-id="3730e-204">In keeping with .ini conventions, keys are declared under a section.</span></span> 

<span data-ttu-id="3730e-205">WSL поддерживает два раздела: `automount` и `network`.</span><span class="sxs-lookup"><span data-stu-id="3730e-205">WSL supports two sections: `automount` and `network`.</span></span>

#### <a name="automount"></a><span data-ttu-id="3730e-206">автоподключения</span><span class="sxs-lookup"><span data-stu-id="3730e-206">automount</span></span>

<span data-ttu-id="3730e-207">Раздела`[automount]`</span><span class="sxs-lookup"><span data-stu-id="3730e-207">Section: `[automount]`</span></span>


| <span data-ttu-id="3730e-208">ключ</span><span class="sxs-lookup"><span data-stu-id="3730e-208">key</span></span>        | <span data-ttu-id="3730e-209">value</span><span class="sxs-lookup"><span data-stu-id="3730e-209">value</span></span>                          | <span data-ttu-id="3730e-210">значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3730e-210">default</span></span>      | <span data-ttu-id="3730e-211">Заметки о</span><span class="sxs-lookup"><span data-stu-id="3730e-211">notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3730e-212">enabled</span><span class="sxs-lookup"><span data-stu-id="3730e-212">enabled</span></span>    | <span data-ttu-id="3730e-213">boolean</span><span class="sxs-lookup"><span data-stu-id="3730e-213">boolean</span></span>                        | <span data-ttu-id="3730e-214">true</span><span class="sxs-lookup"><span data-stu-id="3730e-214">true</span></span>         | <span data-ttu-id="3730e-215">`true`вызывает фиксированные диски (например,</span><span class="sxs-lookup"><span data-stu-id="3730e-215">`true` causes fixed drives (i.e</span></span> <span data-ttu-id="3730e-216">`C:/`или `D:/`) для автоматической монтирования с дрвфс в `/mnt`.</span><span class="sxs-lookup"><span data-stu-id="3730e-216">`C:/` or `D:/`) to be automatically mounted with DrvFs under `/mnt`.</span></span>  <span data-ttu-id="3730e-217">`false`означает, что диски не будут подключены автоматически, но их можно подключать вручную или `fstab`через.</span><span class="sxs-lookup"><span data-stu-id="3730e-217">`false` means drives won’t be mounted automatically, but you could still mount them manually or via `fstab`.</span></span>                                                                                                             |
| <span data-ttu-id="3730e-218">маунтфстаб</span><span class="sxs-lookup"><span data-stu-id="3730e-218">mountFsTab</span></span> | <span data-ttu-id="3730e-219">boolean</span><span class="sxs-lookup"><span data-stu-id="3730e-219">boolean</span></span>                        | <span data-ttu-id="3730e-220">true</span><span class="sxs-lookup"><span data-stu-id="3730e-220">true</span></span>         | <span data-ttu-id="3730e-221">`true`наборы `/etc/fstab` , обрабатываемые при запуске WSL.</span><span class="sxs-lookup"><span data-stu-id="3730e-221">`true` sets `/etc/fstab` to be processed on WSL start.</span></span> <span data-ttu-id="3730e-222">/etc/fstab — это файл, в котором можно объявлять другие файловые системы, например общий ресурс SMB.</span><span class="sxs-lookup"><span data-stu-id="3730e-222">/etc/fstab is a file where you can declare other filesystems, like an SMB share.</span></span> <span data-ttu-id="3730e-223">Поэтому вы можете автоматически подключать эти файловые системы в WSL при запуске.</span><span class="sxs-lookup"><span data-stu-id="3730e-223">Thus, you can mount these filesystems automatically in WSL on start up.</span></span>                                                                                                                |
| <span data-ttu-id="3730e-224">корневой</span><span class="sxs-lookup"><span data-stu-id="3730e-224">root</span></span>       | <span data-ttu-id="3730e-225">Строка</span><span class="sxs-lookup"><span data-stu-id="3730e-225">String</span></span>                         | `/mnt/`      | <span data-ttu-id="3730e-226">Задает каталог, в который будут автоматически подключены фиксированные диски.</span><span class="sxs-lookup"><span data-stu-id="3730e-226">Sets the directory where fixed drives will be automatically mounted.</span></span> <span data-ttu-id="3730e-227">Например, если у вас есть каталог в WSL `/windir/` и вы указали его в качестве корневого, вы должны увидеть, что жесткие диски подключены в`/windir/c`</span><span class="sxs-lookup"><span data-stu-id="3730e-227">For example, if you have a directory in WSL at `/windir/` and you specify that as the root, you would expect to see your fixed drives mounted at `/windir/c`</span></span>                                                                                              |
| <span data-ttu-id="3730e-228">параметры</span><span class="sxs-lookup"><span data-stu-id="3730e-228">options</span></span>    | <span data-ttu-id="3730e-229">список значений с разделителями-запятыми</span><span class="sxs-lookup"><span data-stu-id="3730e-229">comma-separated list of values</span></span> | <span data-ttu-id="3730e-230">пустая строка</span><span class="sxs-lookup"><span data-stu-id="3730e-230">empty string</span></span> | <span data-ttu-id="3730e-231">Это значение добавляется в строку параметров подключения по умолчанию Дрвфс.</span><span class="sxs-lookup"><span data-stu-id="3730e-231">This value is appended to the default DrvFs mount options string.</span></span> <span data-ttu-id="3730e-232">**Можно указать только параметры, относящиеся к Дрвфс.**</span><span class="sxs-lookup"><span data-stu-id="3730e-232">**Only DrvFs-specific options can be specified.**</span></span> <span data-ttu-id="3730e-233">Параметры, которые двоичный файл подключения обычно будет анализировать в флаг, не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="3730e-233">Options that the mount binary would normally parse into a flag are not supported.</span></span> <span data-ttu-id="3730e-234">Если вы хотите явно указать эти параметры, необходимо включить каждый диск, для которого вы хотите сделать это в/etc/fstab.</span><span class="sxs-lookup"><span data-stu-id="3730e-234">If you want to explicitly specify those options, you must include every drive for which you want to do so in /etc/fstab.</span></span> |

<span data-ttu-id="3730e-235">По умолчанию WSL устанавливает идентификатор UID и GID в значение пользователя по умолчанию (в Ubuntu дистрибутив пользователь по умолчанию создается с идентификатором UID = 1000, GID = 1000).</span><span class="sxs-lookup"><span data-stu-id="3730e-235">By default, WSL sets the uid and gid to the value of the default user (in Ubuntu distro, the default user is created with uid=1000,gid=1000).</span></span> <span data-ttu-id="3730e-236">Если пользователь явно указывает параметр gid или UID с помощью этого ключа, связанное значение будет перезаписано.</span><span class="sxs-lookup"><span data-stu-id="3730e-236">If the user specifies a gid or uid option explicitly via this key, the associated value will be overwritten.</span></span> <span data-ttu-id="3730e-237">В противном случае всегда будет добавляться значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3730e-237">Otherwise, the default value will always be appended.</span></span>

<span data-ttu-id="3730e-238">**Примечание.** Эти параметры применяются в качестве параметров подключения для всех автоматически подключенных дисков.</span><span class="sxs-lookup"><span data-stu-id="3730e-238">**Note:** These options are applied as the mount options for all automatically mounted drives.</span></span> <span data-ttu-id="3730e-239">Чтобы изменить параметры только для конкретного диска, используйте вместо него/etc/fstab.</span><span class="sxs-lookup"><span data-stu-id="3730e-239">To change the options for a specific drive only, use /etc/fstab instead.</span></span>

#### <a name="network"></a><span data-ttu-id="3730e-240">сеть</span><span class="sxs-lookup"><span data-stu-id="3730e-240">network</span></span>

<span data-ttu-id="3730e-241">Метка раздела:`[network]`</span><span class="sxs-lookup"><span data-stu-id="3730e-241">Section label: `[network]`</span></span>

| <span data-ttu-id="3730e-242">ключ</span><span class="sxs-lookup"><span data-stu-id="3730e-242">key</span></span> | <span data-ttu-id="3730e-243">value</span><span class="sxs-lookup"><span data-stu-id="3730e-243">value</span></span> | <span data-ttu-id="3730e-244">значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3730e-244">default</span></span> | <span data-ttu-id="3730e-245">Заметки о</span><span class="sxs-lookup"><span data-stu-id="3730e-245">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="3730e-246">женератехостс</span><span class="sxs-lookup"><span data-stu-id="3730e-246">generateHosts</span></span> | <span data-ttu-id="3730e-247">boolean</span><span class="sxs-lookup"><span data-stu-id="3730e-247">boolean</span></span> | `true` | <span data-ttu-id="3730e-248">`true`Задает WSL для создания `/etc/hosts`.</span><span class="sxs-lookup"><span data-stu-id="3730e-248">`true` sets WSL to generate `/etc/hosts`.</span></span> <span data-ttu-id="3730e-249">`hosts` Файл содержит статическую карту имен узлов, соответствующий IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="3730e-249">The `hosts` file contains a static map of hostnames corresponding IP address.</span></span> |
| <span data-ttu-id="3730e-250">женератересолвконф</span><span class="sxs-lookup"><span data-stu-id="3730e-250">generateResolvConf</span></span> | <span data-ttu-id="3730e-251">boolean</span><span class="sxs-lookup"><span data-stu-id="3730e-251">boolean</span></span> | `true` | <span data-ttu-id="3730e-252">`true`Задайте для WSL значение `/etc/resolv.conf`Generate.</span><span class="sxs-lookup"><span data-stu-id="3730e-252">`true` set WSL to generate `/etc/resolv.conf`.</span></span> <span data-ttu-id="3730e-253">`resolv.conf` Содержит список DNS, который способен разрешать данному имени узла по его IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="3730e-253">The `resolv.conf` contains a DNS list that are capable of resolving a given hostname to its IP address.</span></span> | 

#### <a name="interop"></a><span data-ttu-id="3730e-254">com</span><span class="sxs-lookup"><span data-stu-id="3730e-254">interop</span></span>

<span data-ttu-id="3730e-255">Метка раздела:`[interop]`</span><span class="sxs-lookup"><span data-stu-id="3730e-255">Section label: `[interop]`</span></span>

<span data-ttu-id="3730e-256">Эти параметры доступны в сборке Insider Build 17713 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="3730e-256">These options are available in Insider Build 17713 and later.</span></span>

| <span data-ttu-id="3730e-257">ключ</span><span class="sxs-lookup"><span data-stu-id="3730e-257">key</span></span> | <span data-ttu-id="3730e-258">value</span><span class="sxs-lookup"><span data-stu-id="3730e-258">value</span></span> | <span data-ttu-id="3730e-259">значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3730e-259">default</span></span> | <span data-ttu-id="3730e-260">Заметки о</span><span class="sxs-lookup"><span data-stu-id="3730e-260">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="3730e-261">enabled</span><span class="sxs-lookup"><span data-stu-id="3730e-261">enabled</span></span> | <span data-ttu-id="3730e-262">boolean</span><span class="sxs-lookup"><span data-stu-id="3730e-262">boolean</span></span> | `true` | <span data-ttu-id="3730e-263">Установка этого ключа определяет, будет ли WSL поддерживать запуск процессов Windows.</span><span class="sxs-lookup"><span data-stu-id="3730e-263">Setting this key will determine whether WSL will support launching Windows processes.</span></span> |
| <span data-ttu-id="3730e-264">аппендвиндовспас</span><span class="sxs-lookup"><span data-stu-id="3730e-264">appendWindowsPath</span></span> | <span data-ttu-id="3730e-265">boolean</span><span class="sxs-lookup"><span data-stu-id="3730e-265">boolean</span></span> | `true` | <span data-ttu-id="3730e-266">Задание этого ключа определит, будет ли WSL добавлять элементы пути Windows в переменную среды $PATH.</span><span class="sxs-lookup"><span data-stu-id="3730e-266">Setting this key will determine whether WSL will add Windows path elements to the $PATH environment variable.</span></span> | 
