---
title: Учетная запись пользователя Linux и разрешения
description: Справочные материалы по управлению учетными записями пользователей и разрешениями для подсистемы Windows для Linux.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, учетные записи пользователей
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: de18c128854ef9a39a26551db2ea0aee97b8ab4f
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122687"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a><span data-ttu-id="af728-104">Учетные записи пользователей и разрешения для подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="af728-104">User Accounts and Permissions for Windows Subsystem for Linux</span></span>

<span data-ttu-id="af728-105">Создание пользователя Linux — это первый шаг в настройке нового дистрибутива Linux в WSL.</span><span class="sxs-lookup"><span data-stu-id="af728-105">Creating your Linux user is the first step in setting up a new Linux distribution on WSL.</span></span>  <span data-ttu-id="af728-106">Для первой созданной учетной записи пользователя автоматически настраивается несколько специальных атрибутов:</span><span class="sxs-lookup"><span data-stu-id="af728-106">The first user account you create is automatically configured with a few special attributes:</span></span>

1. <span data-ttu-id="af728-107">это пользователь по умолчанию — он автоматически используется для входа при запуске;</span><span class="sxs-lookup"><span data-stu-id="af728-107">It is your default user -- it signs-in automatically on launch.</span></span>
1. <span data-ttu-id="af728-108">по умолчанию это администратор Linux (участник группы sudo).</span><span class="sxs-lookup"><span data-stu-id="af728-108">It is Linux administrator (a member of the sudo group) by default.</span></span>

<span data-ttu-id="af728-109">Каждый дистрибутив Linux, работающий в подсистеме Windows для Linux, имеет собственные учетные записи пользователей Linux с паролями.</span><span class="sxs-lookup"><span data-stu-id="af728-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="af728-110">Вам потребуется настраивать учетную запись пользователя Linux при каждом добавлении, переустановке или сбросе дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="af728-110">You will have to configure a Linux user account any time you add a distribution, reinstall, or reset.</span></span>  <span data-ttu-id="af728-111">Учетные записи пользователей Linux не только являются независимыми для каждого дистрибутива, но и не зависят от учетной записи пользователя Windows.</span><span class="sxs-lookup"><span data-stu-id="af728-111">Linux user accounts are not only independent per distribution, they are also independent from your Windows user account.</span></span>

## <a name="resetting-your-linux-password"></a><span data-ttu-id="af728-112">Сброс пароля Linux</span><span class="sxs-lookup"><span data-stu-id="af728-112">Resetting your Linux password</span></span>

<span data-ttu-id="af728-113">Если у вас есть доступ к учетной записи пользователя Linux и вам известен ее пароль, измените его с помощью средств сброса пароля Linux для этого дистрибутива (как правило, это `passwd`).</span><span class="sxs-lookup"><span data-stu-id="af728-113">If you have access to your Linux user account and know your current password, change it using Linux password reset tools of that distribution -- most likely `passwd`.</span></span>

<span data-ttu-id="af728-114">Если это не так, то, в зависимости от дистрибутива, вы можете сбросить пароль, сбросив параметры пользователя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="af728-114">If that's not an option, depending on the distribution, you may be able to reset your password by resetting the default user.</span></span>

<span data-ttu-id="af728-115">WSL предлагает тег пользователя по умолчанию, который определяет, какая учетная запись пользователя автоматически входит в систему при запуске WSL.</span><span class="sxs-lookup"><span data-stu-id="af728-115">WSL offers a default user tag to identify which user account automatically logs in when you start a WSL.</span></span>  <span data-ttu-id="af728-116">Так как многие дистрибутивы содержат команды для задания пользователя по умолчанию в качестве привилегированного пользователя, а также привилегированного пользователя без пароля, изменение пользователя по умолчанию на привилегированного пользователя — это удобный способ сброса пароля.</span><span class="sxs-lookup"><span data-stu-id="af728-116">Since many distributions include commands to set the default user to root and also a root user with no password set, changing the default user to root is a handy tool for things like password reset.</span></span>

### <a name="for-creators-update-and-earlier"></a><span data-ttu-id="af728-117">Для выпуска Creators Update и более ранних версий</span><span class="sxs-lookup"><span data-stu-id="af728-117">For Creators Update and earlier</span></span>
<span data-ttu-id="af728-118">Если вы используете Windows 10 Creators Update или более раннюю версию, то вы можете изменить пользователя Bash по умолчанию, выполнив следующие команды.</span><span class="sxs-lookup"><span data-stu-id="af728-118">If you're running Windows 10 Creators update or earlier, you can change the default Bash user by running the following commands:</span></span>

1. <span data-ttu-id="af728-119">Измените пользователя по умолчанию на `root`.</span><span class="sxs-lookup"><span data-stu-id="af728-119">Change the default user to `root`:</span></span>

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. <span data-ttu-id="af728-120">Теперь выполните команду `bash.exe`, чтобы войти в систему как `root`.</span><span class="sxs-lookup"><span data-stu-id="af728-120">Run `bash.exe` to now login as `root`:</span></span>

    ```console
    C:\> bash.exe
    ```

1. <span data-ttu-id="af728-121">Сбросьте пароль с помощью команды управления паролем для дистрибутива и закройте консоль Linux.</span><span class="sxs-lookup"><span data-stu-id="af728-121">Reset your password using the distribution's password command, and close the Linux Console:</span></span>

    ```BASH
    $ passwd username
    $ exit
    ```

1. <span data-ttu-id="af728-122">В командной строке Windows сбросьте пользователя по умолчанию, превратив его в обычную учетную запись пользователя Linux.</span><span class="sxs-lookup"><span data-stu-id="af728-122">From Windows CMD, reset your default user back to your normal Linux user account:</span></span>

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a><span data-ttu-id="af728-123">Для выпусков Fall Creators Update и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="af728-123">For Fall Creators Update and later</span></span>
<span data-ttu-id="af728-124">Чтобы узнать, какие команды доступны для определенного дистрибутива, выполните команду `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="af728-124">To see what commands are available for a particular distribution, run `[distro.exe] /?`.</span></span>
    
<span data-ttu-id="af728-125">Например, если установлен дистрибутив Ubuntu:</span><span class="sxs-lookup"><span data-stu-id="af728-125">For example, with Ubuntu installed:</span></span>

```console
C:\> ubuntu.exe /?

Launches or configures a linux distribution.

Usage:
    <no args>
      - Launches the distro's default behavior. By default, this launches your default shell.

    run <command line>
      - Run the given command line in that distro, using the default configuration.
      - Everything after `run ` is passed to the linux LaunchProcess cal

    config [setting [value]]
      - Configure certain settings for this distro.
      - Settings are any of the following (by default)
        - `--default-user <username>`: Set the default user for this distro to <username>

    clean
      - Uninstalls the distro. The appx remains on your machine. This can be
        useful for "factory resetting" your instance. This removes the linux
        filesystem from the disk, but not the app from your PC, so you don't
        need to redownload the entire tar.gz again.

    help
      - Print this usage message.
```

<span data-ttu-id="af728-126">Пошаговые инструкции по использованию Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="af728-126">Step by step instructions using Ubuntu:</span></span>

1. <span data-ttu-id="af728-127">Открытие командной строки</span><span class="sxs-lookup"><span data-stu-id="af728-127">Open CMD</span></span>
1. <span data-ttu-id="af728-128">Задайте пользователя по умолчанию Linux: `root`.</span><span class="sxs-lookup"><span data-stu-id="af728-128">Set the default Linux user to `root`:</span></span>

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. <span data-ttu-id="af728-129">Запустите дистрибутив Linux (`ubuntu`).</span><span class="sxs-lookup"><span data-stu-id="af728-129">Launch your Linux distribution (`ubuntu`).</span></span>  <span data-ttu-id="af728-130">Вы автоматически войдете в систему как `root`.</span><span class="sxs-lookup"><span data-stu-id="af728-130">You will automatically login as `root`:</span></span>

1. <span data-ttu-id="af728-131">Сбросьте пароль с помощью команды `passwd`.</span><span class="sxs-lookup"><span data-stu-id="af728-131">Reset your password using the `passwd` command:</span></span>

    ```BASH
    $ passwd username
    ```

1. <span data-ttu-id="af728-132">В командной строке Windows сбросьте пользователя по умолчанию, превратив его в обычную учетную запись пользователя Linux.</span><span class="sxs-lookup"><span data-stu-id="af728-132">From Windows CMD, reset your default user back to your normal Linux user account.</span></span>

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a><span data-ttu-id="af728-133">Разрешения</span><span class="sxs-lookup"><span data-stu-id="af728-133">Permissions</span></span>

<span data-ttu-id="af728-134">При управлении разрешениями в WSL следует помнить два важных понятия.</span><span class="sxs-lookup"><span data-stu-id="af728-134">There are two important concepts to keep in mind when it comes to permissions in WSL:</span></span>

1. <span data-ttu-id="af728-135">Модель разрешений Windows управляет правами процесса для ресурсов Windows.</span><span class="sxs-lookup"><span data-stu-id="af728-135">The Windows permission model governs a process' rights to Windows resources</span></span>
2. <span data-ttu-id="af728-136">Модель разрешений Linux управляет правами процесса для ресурсов Linux.</span><span class="sxs-lookup"><span data-stu-id="af728-136">The Linux permission model controls a process' rights to Linux resources</span></span>

<span data-ttu-id="af728-137">При запуске Linux в WSL операционная система Linux будет иметь те же разрешения Windows, что и процесс, запускающий ее.</span><span class="sxs-lookup"><span data-stu-id="af728-137">When running Linux on WSL, Linux will have the same Windows permissions as the process that launches it.</span></span> <span data-ttu-id="af728-138">Linux можно запустить с одним из двух уровней разрешений.</span><span class="sxs-lookup"><span data-stu-id="af728-138">Linux can be launched in one of two permission levels:</span></span>

* <span data-ttu-id="af728-139">Обычный (без повышенных привилегий): Linux работает с разрешениями вошедшего в систему пользователя.</span><span class="sxs-lookup"><span data-stu-id="af728-139">Normal (non-elevated): Linux runs with the permissions of the logged-in user</span></span>
* <span data-ttu-id="af728-140">Повышенные привилегии или администратор: Linux работает с повышенными разрешениями Windows или правами администратора.</span><span class="sxs-lookup"><span data-stu-id="af728-140">Elevated/admin: Linux runs with elevated/admin Windows permissions</span></span>

> <span data-ttu-id="af728-141">Так как процессы с повышенными привилегиями могут получить доступ и изменить (а, следовательно, повредить) параметры уровня системы и данные уровня системы или защищенные данные, **не запускайте** какие-либо процессы (приложения, инструменты или оболочки Windows либо Linux) с повышенными привилегиями, если только это не связано с крайней необходимостью!</span><span class="sxs-lookup"><span data-stu-id="af728-141">Because elevated processes can access/modify (and therefore damage) system-wide settings and system-wide/protected data, **AVOID** launching elevated processes unless you absolutely have to - whether they're Windows or Linux applications/tools/shells!</span></span>

<span data-ttu-id="af728-142">Указанные выше разрешения Windows не зависят от разрешений в экземпляре Linux. "Корневые привилегии" Linux влияют только на права пользователя в среде и файловой системе Linux. Они не влияют на предоставленные привилегии Windows.</span><span class="sxs-lookup"><span data-stu-id="af728-142">The above Windows permissions are independent of the permissions within a Linux instance: Linux "Root privileges" only impact the user’s rights within the Linux environment & filesystem; they have no impact on the Windows privileges granted.</span></span> <span data-ttu-id="af728-143">Таким образом, запуск процесса Linux в качестве корневого (например, с помощью `sudo`) предоставляет этому процессу права администратора только в среде Linux.</span><span class="sxs-lookup"><span data-stu-id="af728-143">Thus, running a Linux process as root (e.g. via `sudo`) only grants that process admin rights within the Linux environment.</span></span>

<span data-ttu-id="af728-144">**Пример:**    </span><span class="sxs-lookup"><span data-stu-id="af728-144">**Example:**  </span></span>  
<span data-ttu-id="af728-145">Сеанс Bash с привилегиями администратора Windows может обращаться к `cd /mnt/c/Users/Administrator`, в то время как сеанс Bash без привилегий администратора будет порождать ошибку "Отказ в разрешении".</span><span class="sxs-lookup"><span data-stu-id="af728-145">A Bash session with Windows admin privileges may access `cd /mnt/c/Users/Administrator` while a Bash session without admin privileges would see a "Permission Denied" error.</span></span>

<span data-ttu-id="af728-146">Ввод `sudo cd /mnt/c/Users/Administrator` в Linux не предоставит доступ к каталогу администратора, так как разрешениями в Windows управляет Windows.</span><span class="sxs-lookup"><span data-stu-id="af728-146">In Linux, typing `sudo cd /mnt/c/Users/Administrator` will not grant access to the Administrator’s directory since permissions within Windows are managed by Windows.</span></span>

<span data-ttu-id="af728-147">Модель разрешений Linux важна в среде Linux, в которой разрешения предоставляются в соответствии с текущим пользователем Linux.</span><span class="sxs-lookup"><span data-stu-id="af728-147">The Linux permission model is important when inside the Linux environment where the user has permissions based on the current Linux user.</span></span>

<span data-ttu-id="af728-148">**Пример.**</span><span class="sxs-lookup"><span data-stu-id="af728-148">**Example:**</span></span>  
<span data-ttu-id="af728-149">Пользователь в группе sudo может выполнить команду `sudo apt update`.</span><span class="sxs-lookup"><span data-stu-id="af728-149">A user in the sudo group may run `sudo apt update`.</span></span>
