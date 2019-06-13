---
title: Учетная запись пользователя Linux и разрешения
description: Ссылка для учетных записей пользователей и управление разрешениями в подсистеме Windows для Linux.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, учетные записи пользователей
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.openlocfilehash: 0d00b43d059e72edd4e2a5b9591c29441f461fca
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040832"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a><span data-ttu-id="93914-104">Учетные записи пользователей и разрешения для подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="93914-104">User Accounts and Permissions for Windows Subsystem for Linux</span></span>

<span data-ttu-id="93914-105">Создание пользователя Linux является первым шагом в настройке дистрибутив Linux на WSL.</span><span class="sxs-lookup"><span data-stu-id="93914-105">Creating your Linux user is the first step in setting up a new Linux distribution on WSL.</span></span>  <span data-ttu-id="93914-106">Создаваемая учетная запись первого пользователя автоматически настраивается несколько специальных атрибутов:</span><span class="sxs-lookup"><span data-stu-id="93914-106">The first user account you create is automatically configured with a few special attributes:</span></span>

1. <span data-ttu-id="93914-107">Это ваш пользователь по умолчанию — он выполняет вход автоматически при запуске.</span><span class="sxs-lookup"><span data-stu-id="93914-107">It is your default user -- it signs-in automatically on launch.</span></span>
1. <span data-ttu-id="93914-108">Это администратор Linux (член группы sudo) по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="93914-108">It is Linux administrator (a member of the sudo group) by default.</span></span>

<span data-ttu-id="93914-109">Каждый дистрибутив Linux, запущенных в подсистеме Windows для Linux имеет свои собственные учетные записи пользователей для Linux и пароли.</span><span class="sxs-lookup"><span data-stu-id="93914-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="93914-110">Необходимо настроить учетную запись пользователя Linux любое время добавить дистрибутив, переустановите или сброса.</span><span class="sxs-lookup"><span data-stu-id="93914-110">You will have to configure a Linux user account any time you add a distribution, reinstall, or reset.</span></span>  <span data-ttu-id="93914-111">Учетные записи пользователей Linux не только не зависят от каждого распределения, они также не зависят от учетной записи пользователя Windows.</span><span class="sxs-lookup"><span data-stu-id="93914-111">Linux user accounts are not only independent per distribution, they are also independent from your Windows user account.</span></span>

## <a name="resetting-your-linux-password"></a><span data-ttu-id="93914-112">Сброс пароля Linux</span><span class="sxs-lookup"><span data-stu-id="93914-112">Resetting your Linux password</span></span>

<span data-ttu-id="93914-113">Если нет доступа к вашей учетной записью пользователя Linux и знать текущий пароль, измените его с помощью Linux сброса пароля средства дистрибутива — скорее всего, `passwd`.</span><span class="sxs-lookup"><span data-stu-id="93914-113">If you have access to your Linux user account and know your current password, change it using Linux password reset tools of that distribution -- most likely `passwd`.</span></span>

<span data-ttu-id="93914-114">Если это не параметр, в зависимости от распределения, можно сбросить пароль, сбросив пользователя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="93914-114">If that's not an option, depending on the distribution, you may be able to reset your password by resetting the default user.</span></span>

<span data-ttu-id="93914-115">WSL предлагает входе тег пользователя по умолчанию, чтобы определить какая пользовательская учетная запись автоматически при запуске WSL.</span><span class="sxs-lookup"><span data-stu-id="93914-115">WSL offers a default user tag to identify which user account automatically logs in when you start a WSL.</span></span>  <span data-ttu-id="93914-116">Так как многие дистрибутивы включают в себя команды, чтобы задать пользователя по умолчанию для корня и также привилегированного пользователя с набором без пароля, изменение пользователя по умолчанию корневой каталог является удобным инструментом для таких вещей, как сброс пароля.</span><span class="sxs-lookup"><span data-stu-id="93914-116">Since many distributions include commands to set the default user to root and also a root user with no password set, changing the default user to root is a handy tool for things like password reset.</span></span>

### <a name="for-creators-update-and-earlier"></a><span data-ttu-id="93914-117">Для Creators Update и более ранних версий</span><span class="sxs-lookup"><span data-stu-id="93914-117">For Creators Update and earlier</span></span>
<span data-ttu-id="93914-118">Если вы используете Windows 10 Creators update или более ранних версиях Bash пользователя по умолчанию можно изменить, выполнив следующие команды:</span><span class="sxs-lookup"><span data-stu-id="93914-118">If you're running Windows 10 Creators update or earlier, you can change the default Bash user by running the following commands:</span></span>

1. <span data-ttu-id="93914-119">Изменить пользователя по умолчанию для `root`:</span><span class="sxs-lookup"><span data-stu-id="93914-119">Change the default user to `root`:</span></span>

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. <span data-ttu-id="93914-120">Запустите `bash.exe` теперь войти как `root`:</span><span class="sxs-lookup"><span data-stu-id="93914-120">Run `bash.exe` to now login as `root`:</span></span>

    ```console
    C:\> bash.exe
    ```

1. <span data-ttu-id="93914-121">Сбросить пароль с помощью дистрибутива парольная команда и закройте консоль Linux:</span><span class="sxs-lookup"><span data-stu-id="93914-121">Reset your password using the distribution's password command, and close the Linux Console:</span></span>

    ```BASH
    $ passwd username
    $ exit
    ```

1. <span data-ttu-id="93914-122">Из командной строки Windows сбросьте пользователя по умолчанию в учетной записи обычного пользователя Linux:</span><span class="sxs-lookup"><span data-stu-id="93914-122">From Windows CMD, reset your default user back to your normal Linux user account:</span></span>

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a><span data-ttu-id="93914-123">Fall Creators Update и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="93914-123">For Fall Creators Update and later</span></span>
<span data-ttu-id="93914-124">Чтобы узнать, какие команды доступны для определенного распределения, запустите `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="93914-124">To see what commands are available for a particular distribution, run `[distro.exe] /?`.</span></span>
    
<span data-ttu-id="93914-125">Например с Ubuntu установлены:</span><span class="sxs-lookup"><span data-stu-id="93914-125">For example, with Ubuntu installed:</span></span>

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

<span data-ttu-id="93914-126">Пошаговые инструкции с помощью Ubuntu:</span><span class="sxs-lookup"><span data-stu-id="93914-126">Step by step instructions using Ubuntu:</span></span>

1. <span data-ttu-id="93914-127">Откройте CMD</span><span class="sxs-lookup"><span data-stu-id="93914-127">Open CMD</span></span>
1. <span data-ttu-id="93914-128">Значение по умолчанию пользователь Linux `root`:</span><span class="sxs-lookup"><span data-stu-id="93914-128">Set the default Linux user to `root`:</span></span>

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. <span data-ttu-id="93914-129">Запустите дистрибутива Linux (`ubuntu`).</span><span class="sxs-lookup"><span data-stu-id="93914-129">Launch your Linux distribution (`ubuntu`).</span></span>  <span data-ttu-id="93914-130">Вы будете автоматически войдите в систему как `root`:</span><span class="sxs-lookup"><span data-stu-id="93914-130">You will automatically login as `root`:</span></span>

1. <span data-ttu-id="93914-131">Сбросить пароль с помощью `passwd` команды:</span><span class="sxs-lookup"><span data-stu-id="93914-131">Reset your password using the `passwd` command:</span></span>

    ```BASH
    $ passwd username
    ```

1. <span data-ttu-id="93914-132">Из командной строки Windows сбросьте пользователя по умолчанию в учетной записи обычного пользователя Linux.</span><span class="sxs-lookup"><span data-stu-id="93914-132">From Windows CMD, reset your default user back to your normal Linux user account.</span></span>

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a><span data-ttu-id="93914-133">Разрешения</span><span class="sxs-lookup"><span data-stu-id="93914-133">Permissions</span></span>

<span data-ttu-id="93914-134">Существует два важных понятий Имейте в виду, когда дело доходит до разрешения в WSL:</span><span class="sxs-lookup"><span data-stu-id="93914-134">There are two important concepts to keep in mind when it comes to permissions in WSL:</span></span>

1. <span data-ttu-id="93914-135">Модель разрешений Windows управляет процесса права к ресурсам Windows</span><span class="sxs-lookup"><span data-stu-id="93914-135">The Windows permission model governs a process' rights to Windows resources</span></span>
2. <span data-ttu-id="93914-136">Модель разрешений Linux управляет правами процесса для ресурсов под управлением Linux</span><span class="sxs-lookup"><span data-stu-id="93914-136">The Linux permission model controls a process' rights to Linux resources</span></span>

<span data-ttu-id="93914-137">При использовании Linux на платформе WSL, Linux будет иметь те же разрешения Windows, что и запустившая его процесс.</span><span class="sxs-lookup"><span data-stu-id="93914-137">When running Linux on WSL, Linux will have the same Windows permissions as the process that launches it.</span></span> <span data-ttu-id="93914-138">Linux могут запускаться в одном из двух уровней разрешений:</span><span class="sxs-lookup"><span data-stu-id="93914-138">Linux can be launched in one of two permission levels:</span></span>

* <span data-ttu-id="93914-139">Обычный (без повышенных прав): Linux выполняется с разрешениями пользователя, вошедшего в систему</span><span class="sxs-lookup"><span data-stu-id="93914-139">Normal (non-elevated): Linux runs with the permissions of the logged-in user</span></span>
* <span data-ttu-id="93914-140">Повышенных привилегий/admin: Linux выполняется с повышенным уровнем разрешений администратору Windows</span><span class="sxs-lookup"><span data-stu-id="93914-140">Elevated/admin: Linux runs with elevated/admin Windows permissions</span></span>

> <span data-ttu-id="93914-141">Так как процессов с повышенными правами можно доступ и изменение (и поэтому повредить) параметры уровня системы и системы расширенных/защищенные данные, **ИЗБЕГАЙТЕ** запуск процессов с повышенными правами, если совершенно необходимо - находятся ли они Windows или Linux приложения/tools/оболочек!</span><span class="sxs-lookup"><span data-stu-id="93914-141">Because elevated processes can access/modify (and therefore damage) system-wide settings and system-wide/protected data, **AVOID** launching elevated processes unless you absolutely have to - whether they're Windows or Linux applications/tools/shells!</span></span>

<span data-ttu-id="93914-142">Эти разрешения Windows не зависят от разрешений в экземпляре Linux: «Привилегированного Linux» затрагивается только права пользователя в среде Linux & файловой системы; они не оказывают влияния на привилегиях Windows.</span><span class="sxs-lookup"><span data-stu-id="93914-142">The above Windows permissions are independent of the permissions within a Linux instance: Linux "Root privileges" only impact the user’s rights within the Linux environment & filesystem; they have no impact on the Windows privileges granted.</span></span> <span data-ttu-id="93914-143">Таким образом, выполнение процесса Linux в качестве привилегированного пользователя (например, через `sudo`) предоставляет только разрешение, которые обрабатывают права администратора в среде Linux.</span><span class="sxs-lookup"><span data-stu-id="93914-143">Thus, running a Linux process as root (e.g. via `sudo`) only grants that process admin rights within the Linux environment.</span></span>

<span data-ttu-id="93914-144">**Пример:**   </span><span class="sxs-lookup"><span data-stu-id="93914-144">**Example:**  </span></span>  
<span data-ttu-id="93914-145">Сеанс Bash с правами администратора Windows могут получить доступ к `cd /mnt/c/Users/Administrator` во время сеанса Bash без прав администратора увидит сообщение об ошибке «Отказано в доступе».</span><span class="sxs-lookup"><span data-stu-id="93914-145">A Bash session with Windows admin privileges may access `cd /mnt/c/Users/Administrator` while a Bash session without admin privileges would see a "Permission Denied" error.</span></span>

<span data-ttu-id="93914-146">В Linux введя `sudo cd /mnt/c/Users/Administrator` не предоставит доступ к каталогу администратора, так как Windows управляет разрешения в Windows.</span><span class="sxs-lookup"><span data-stu-id="93914-146">In Linux, typing `sudo cd /mnt/c/Users/Administrator` will not grant access to the Administrator’s directory since permissions within Windows are managed by Windows.</span></span>

<span data-ttu-id="93914-147">Модель разрешений Linux важно при работе в среде Linux, в которых пользователь имеет разрешения на основе текущего пользователя Linux.</span><span class="sxs-lookup"><span data-stu-id="93914-147">The Linux permission model is important when inside the Linux environment where the user has permissions based on the current Linux user.</span></span>

<span data-ttu-id="93914-148">**Пример:**</span><span class="sxs-lookup"><span data-stu-id="93914-148">**Example:**</span></span>  
<span data-ttu-id="93914-149">Пользователь в группу sudo может запустить `sudo apt update`.</span><span class="sxs-lookup"><span data-stu-id="93914-149">A user in the sudo group may run `sudo apt update`.</span></span>
