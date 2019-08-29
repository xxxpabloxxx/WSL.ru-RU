---
title: Учетная запись пользователя и разрешения Linux
description: Справочник по учетным записям пользователей и управлению разрешениями с помощью подсистемы Windows для Linux.
keywords: Башонвиндовс, bash, WSL, Windows, подсистема Windows для Linux, виндовссубсистем, Ubuntu, учетные записи пользователей
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: de18c128854ef9a39a26551db2ea0aee97b8ab4f
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122687"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a><span data-ttu-id="7d774-104">Учетные записи пользователей и разрешения для подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="7d774-104">User Accounts and Permissions for Windows Subsystem for Linux</span></span>

<span data-ttu-id="7d774-105">Создание пользователя Linux — это первый шаг в настройке нового дистрибутива Linux в WSL.</span><span class="sxs-lookup"><span data-stu-id="7d774-105">Creating your Linux user is the first step in setting up a new Linux distribution on WSL.</span></span>  <span data-ttu-id="7d774-106">Первая созданная учетная запись пользователя автоматически настраивается с помощью нескольких специальных атрибутов:</span><span class="sxs-lookup"><span data-stu-id="7d774-106">The first user account you create is automatically configured with a few special attributes:</span></span>

1. <span data-ttu-id="7d774-107">Это пользователь по умолчанию — он автоматически подписывается при запуске.</span><span class="sxs-lookup"><span data-stu-id="7d774-107">It is your default user -- it signs-in automatically on launch.</span></span>
1. <span data-ttu-id="7d774-108">По умолчанию это администратор Linux (член группы sudo).</span><span class="sxs-lookup"><span data-stu-id="7d774-108">It is Linux administrator (a member of the sudo group) by default.</span></span>

<span data-ttu-id="7d774-109">Каждый дистрибутив Linux, работающий в подсистеме Windows для Linux, имеет собственные учетные записи пользователей и пароли Linux.</span><span class="sxs-lookup"><span data-stu-id="7d774-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="7d774-110">Вам потребуется настроить учетную запись пользователя Linux при каждом добавлении, переустановке или сбросе.</span><span class="sxs-lookup"><span data-stu-id="7d774-110">You will have to configure a Linux user account any time you add a distribution, reinstall, or reset.</span></span>  <span data-ttu-id="7d774-111">Учетные записи пользователей Linux не только независимы для каждого распределения, но и не зависят от учетной записи пользователя Windows.</span><span class="sxs-lookup"><span data-stu-id="7d774-111">Linux user accounts are not only independent per distribution, they are also independent from your Windows user account.</span></span>

## <a name="resetting-your-linux-password"></a><span data-ttu-id="7d774-112">Сброс пароля Linux</span><span class="sxs-lookup"><span data-stu-id="7d774-112">Resetting your Linux password</span></span>

<span data-ttu-id="7d774-113">Если у вас есть доступ к учетной записи пользователя Linux и ваш текущий пароль, измените его с помощью средств сброса паролей Linux этого распространения, скорее всего `passwd`,.</span><span class="sxs-lookup"><span data-stu-id="7d774-113">If you have access to your Linux user account and know your current password, change it using Linux password reset tools of that distribution -- most likely `passwd`.</span></span>

<span data-ttu-id="7d774-114">Если это не так, то в зависимости от распространения вы можете сбросить пароль, переустановив пользователя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7d774-114">If that's not an option, depending on the distribution, you may be able to reset your password by resetting the default user.</span></span>

<span data-ttu-id="7d774-115">WSL предлагает тег пользователя по умолчанию, который определяет, какая учетная запись пользователя автоматически входит в систему при запуске WSL.</span><span class="sxs-lookup"><span data-stu-id="7d774-115">WSL offers a default user tag to identify which user account automatically logs in when you start a WSL.</span></span>  <span data-ttu-id="7d774-116">Так как многие дистрибутивы включают команды для задания корневого пользователя по умолчанию, а также привилегированного пользователя без пароля, изменение пользователя по умолчанию на root — это удобное средство для сброса пароля.</span><span class="sxs-lookup"><span data-stu-id="7d774-116">Since many distributions include commands to set the default user to root and also a root user with no password set, changing the default user to root is a handy tool for things like password reset.</span></span>

### <a name="for-creators-update-and-earlier"></a><span data-ttu-id="7d774-117">Для авторов, обновление и более ранние версии</span><span class="sxs-lookup"><span data-stu-id="7d774-117">For Creators Update and earlier</span></span>
<span data-ttu-id="7d774-118">Если вы используете Windows 10 Creators Update или более раннюю версию, вы можете изменить пользователя bash по умолчанию, выполнив следующие команды:</span><span class="sxs-lookup"><span data-stu-id="7d774-118">If you're running Windows 10 Creators update or earlier, you can change the default Bash user by running the following commands:</span></span>

1. <span data-ttu-id="7d774-119">Измените пользователя по умолчанию `root`на:</span><span class="sxs-lookup"><span data-stu-id="7d774-119">Change the default user to `root`:</span></span>

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. <span data-ttu-id="7d774-120">Выполните `bash.exe` команду, чтобы войти `root`в систему как:</span><span class="sxs-lookup"><span data-stu-id="7d774-120">Run `bash.exe` to now login as `root`:</span></span>

    ```console
    C:\> bash.exe
    ```

1. <span data-ttu-id="7d774-121">Сбросьте пароль с помощью команды для распространения пароля и закройте консоль Linux:</span><span class="sxs-lookup"><span data-stu-id="7d774-121">Reset your password using the distribution's password command, and close the Linux Console:</span></span>

    ```BASH
    $ passwd username
    $ exit
    ```

1. <span data-ttu-id="7d774-122">В Windows CMD верните пользователя по умолчанию в обычную учетную запись пользователя Linux:</span><span class="sxs-lookup"><span data-stu-id="7d774-122">From Windows CMD, reset your default user back to your normal Linux user account:</span></span>

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a><span data-ttu-id="7d774-123">Для создателей попадают обновление и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="7d774-123">For Fall Creators Update and later</span></span>
<span data-ttu-id="7d774-124">Чтобы узнать, какие команды доступны для определенного распределения, выполните команду `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="7d774-124">To see what commands are available for a particular distribution, run `[distro.exe] /?`.</span></span>
    
<span data-ttu-id="7d774-125">Например, при установке Ubuntu:</span><span class="sxs-lookup"><span data-stu-id="7d774-125">For example, with Ubuntu installed:</span></span>

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

<span data-ttu-id="7d774-126">Пошаговые инструкции по использованию Ubuntu:</span><span class="sxs-lookup"><span data-stu-id="7d774-126">Step by step instructions using Ubuntu:</span></span>

1. <span data-ttu-id="7d774-127">Открыть CMD</span><span class="sxs-lookup"><span data-stu-id="7d774-127">Open CMD</span></span>
1. <span data-ttu-id="7d774-128">Задайте для `root`пользователя Linux по умолчанию следующее:</span><span class="sxs-lookup"><span data-stu-id="7d774-128">Set the default Linux user to `root`:</span></span>

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. <span data-ttu-id="7d774-129">Запустите дистрибутив Linux (`ubuntu`).</span><span class="sxs-lookup"><span data-stu-id="7d774-129">Launch your Linux distribution (`ubuntu`).</span></span>  <span data-ttu-id="7d774-130">Вы будете автоматически входить в `root`систему как:</span><span class="sxs-lookup"><span data-stu-id="7d774-130">You will automatically login as `root`:</span></span>

1. <span data-ttu-id="7d774-131">Сбросьте пароль с помощью `passwd` команды:</span><span class="sxs-lookup"><span data-stu-id="7d774-131">Reset your password using the `passwd` command:</span></span>

    ```BASH
    $ passwd username
    ```

1. <span data-ttu-id="7d774-132">В Windows CMD верните пользователя по умолчанию в обычную учетную запись пользователя Linux.</span><span class="sxs-lookup"><span data-stu-id="7d774-132">From Windows CMD, reset your default user back to your normal Linux user account.</span></span>

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a><span data-ttu-id="7d774-133">Разрешения</span><span class="sxs-lookup"><span data-stu-id="7d774-133">Permissions</span></span>

<span data-ttu-id="7d774-134">Есть два важных понятия, которые следует помнить при получении разрешений в WSL:</span><span class="sxs-lookup"><span data-stu-id="7d774-134">There are two important concepts to keep in mind when it comes to permissions in WSL:</span></span>

1. <span data-ttu-id="7d774-135">Модель разрешений Windows управляет правами процесса для ресурсов Windows</span><span class="sxs-lookup"><span data-stu-id="7d774-135">The Windows permission model governs a process' rights to Windows resources</span></span>
2. <span data-ttu-id="7d774-136">Модель разрешений Linux управляет правами процесса для ресурсов Linux</span><span class="sxs-lookup"><span data-stu-id="7d774-136">The Linux permission model controls a process' rights to Linux resources</span></span>

<span data-ttu-id="7d774-137">При запуске Linux на WSL Linux будет иметь те же разрешения Windows, что и процесс, запускающий ее.</span><span class="sxs-lookup"><span data-stu-id="7d774-137">When running Linux on WSL, Linux will have the same Windows permissions as the process that launches it.</span></span> <span data-ttu-id="7d774-138">Linux можно запустить на одном из двух уровней разрешений:</span><span class="sxs-lookup"><span data-stu-id="7d774-138">Linux can be launched in one of two permission levels:</span></span>

* <span data-ttu-id="7d774-139">Обычная (без повышенных привилегий): Linux работает с разрешениями вошедшего в систему пользователя</span><span class="sxs-lookup"><span data-stu-id="7d774-139">Normal (non-elevated): Linux runs with the permissions of the logged-in user</span></span>
* <span data-ttu-id="7d774-140">Повышенная привилегия или администратор: Linux работает с разрешениями Windows с повышенными правами или администратором</span><span class="sxs-lookup"><span data-stu-id="7d774-140">Elevated/admin: Linux runs with elevated/admin Windows permissions</span></span>

> <span data-ttu-id="7d774-141">Так как процессы с повышенными правами могут получать доступ к (и, таким образом, повредить) параметры на уровне системы и данные, защищенные системой или на уровне системы, **не** запускайте процессы с повышенными правами, если только вы не хотите, чтобы они были приложениями Windows или Linux или средствами или команд!</span><span class="sxs-lookup"><span data-stu-id="7d774-141">Because elevated processes can access/modify (and therefore damage) system-wide settings and system-wide/protected data, **AVOID** launching elevated processes unless you absolutely have to - whether they're Windows or Linux applications/tools/shells!</span></span>

<span data-ttu-id="7d774-142">Указанные выше разрешения Windows не зависят от разрешений в экземпляре Linux. Linux "root Privileges" влияет только на права пользователя в среде Linux & файловой системе. они не влияют на предоставленные привилегии Windows.</span><span class="sxs-lookup"><span data-stu-id="7d774-142">The above Windows permissions are independent of the permissions within a Linux instance: Linux "Root privileges" only impact the user’s rights within the Linux environment & filesystem; they have no impact on the Windows privileges granted.</span></span> <span data-ttu-id="7d774-143">Таким образом, запуск процесса Linux в качестве корневого (например `sudo`, Via) предоставляет только права администратора процесса в среде Linux.</span><span class="sxs-lookup"><span data-stu-id="7d774-143">Thus, running a Linux process as root (e.g. via `sudo`) only grants that process admin rights within the Linux environment.</span></span>

<span data-ttu-id="7d774-144">**Пример:**    </span><span class="sxs-lookup"><span data-stu-id="7d774-144">**Example:**  </span></span>  
<span data-ttu-id="7d774-145">Сеанс bash с привилегиями администратора Windows может получить `cd /mnt/c/Users/Administrator` доступ, в то время как сеанс Bash без прав администратора будет видеть ошибку "отказано в разрешении".</span><span class="sxs-lookup"><span data-stu-id="7d774-145">A Bash session with Windows admin privileges may access `cd /mnt/c/Users/Administrator` while a Bash session without admin privileges would see a "Permission Denied" error.</span></span>

<span data-ttu-id="7d774-146">В Linux ввод `sudo cd /mnt/c/Users/Administrator` не будет предоставлять доступ к каталогу администратора, так как разрешения в Windows управляются Windows.</span><span class="sxs-lookup"><span data-stu-id="7d774-146">In Linux, typing `sudo cd /mnt/c/Users/Administrator` will not grant access to the Administrator’s directory since permissions within Windows are managed by Windows.</span></span>

<span data-ttu-id="7d774-147">Модель разрешений Linux важна в среде Linux, в которой пользователь имеет разрешения на основе текущего пользователя Linux.</span><span class="sxs-lookup"><span data-stu-id="7d774-147">The Linux permission model is important when inside the Linux environment where the user has permissions based on the current Linux user.</span></span>

<span data-ttu-id="7d774-148">**Например**</span><span class="sxs-lookup"><span data-stu-id="7d774-148">**Example:**</span></span>  
<span data-ttu-id="7d774-149">Может выполняться `sudo apt update`пользователь в группе sudo.</span><span class="sxs-lookup"><span data-stu-id="7d774-149">A user in the sudo group may run `sudo apt update`.</span></span>
