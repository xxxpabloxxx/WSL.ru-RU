---
title: Обновление учетной записи пользователя WSL в предыдущих версиях Windows
description: Справочник по предыдущим версиям Windows для обновления учетных записей пользователей Linux с помощью подсистемы Windows для Linux.
ms.date: 01/20/2020
ms.topic: article
ROBOTS: NOINDEX
ms.openlocfilehash: 406158d769c4b465b6168d7cca45b48ff1f201fe
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520843"
---
# <a name="wsl-user-account-updates-on-previous-windows-versions"></a><span data-ttu-id="e817c-103">Обновление учетной записи пользователя WSL в предыдущих версиях Windows</span><span class="sxs-lookup"><span data-stu-id="e817c-103">WSL User Account updates on Previous Windows Versions</span></span>

<span data-ttu-id="e817c-104">Это содержимое архивируется для пользователей более ранних версий операционной системы Windows, которые поддерживают подсистему для Linux и нуждаются в поддержке обновления учетных записей пользователей Linux.</span><span class="sxs-lookup"><span data-stu-id="e817c-104">This content is archived for users of earlier versions of Windows operating system that support the subsystem for Linux and need support with updating Linux user accounts.</span></span>

<span data-ttu-id="e817c-105">Сведения о текущей документации см. в разделе [учетные записи пользователей для подсистемы Windows для Linux](../user-support.md).</span><span class="sxs-lookup"><span data-stu-id="e817c-105">For current documentation, see [User Accounts for Windows Subsystem for Linux](../user-support.md).</span></span>

### <a name="for-creators-update-version-of-windows-and-earlier"></a><span data-ttu-id="e817c-106">Для создателя обновлений Windows и более ранних версий</span><span class="sxs-lookup"><span data-stu-id="e817c-106">For Creators Update version of Windows and earlier</span></span>

<span data-ttu-id="e817c-107">Если вы используете Windows 10 Creators Update или более раннюю версию, то вы можете изменить пользователя Bash по умолчанию, выполнив следующие команды.</span><span class="sxs-lookup"><span data-stu-id="e817c-107">If you're running Windows 10 Creators update or earlier, you can change the default Bash user by running the following commands:</span></span>

1. <span data-ttu-id="e817c-108">Измените пользователя по умолчанию на `root`.</span><span class="sxs-lookup"><span data-stu-id="e817c-108">Change the default user to `root`:</span></span>

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. <span data-ttu-id="e817c-109">Теперь выполните команду `bash.exe`, чтобы войти в систему как `root`.</span><span class="sxs-lookup"><span data-stu-id="e817c-109">Run `bash.exe` to now login as `root`:</span></span>

    ```console
    C:\> bash.exe
    ```

1. <span data-ttu-id="e817c-110">Сбросьте пароль с помощью команды управления паролем для дистрибутива и закройте консоль Linux.</span><span class="sxs-lookup"><span data-stu-id="e817c-110">Reset your password using the distribution's password command, and close the Linux Console:</span></span>

    ```BASH
    $ passwd username
    $ exit
    ```

1. <span data-ttu-id="e817c-111">В командной строке Windows сбросьте пользователя по умолчанию, превратив его в обычную учетную запись пользователя Linux.</span><span class="sxs-lookup"><span data-stu-id="e817c-111">From Windows CMD, reset your default user back to your normal Linux user account:</span></span>

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a><span data-ttu-id="e817c-112">Для выпусков Fall Creators Update и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="e817c-112">For Fall Creators Update and later</span></span>

<span data-ttu-id="e817c-113">Чтобы узнать, какие команды доступны для определенного дистрибутива, выполните команду `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="e817c-113">To see what commands are available for a particular distribution, run `[distro.exe] /?`.</span></span>
    
<span data-ttu-id="e817c-114">Например, если установлен дистрибутив Ubuntu:</span><span class="sxs-lookup"><span data-stu-id="e817c-114">For example, with Ubuntu installed:</span></span>

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

<span data-ttu-id="e817c-115">Пошаговые инструкции по использованию Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="e817c-115">Step by step instructions using Ubuntu:</span></span>

1. <span data-ttu-id="e817c-116">Открытие командной строки</span><span class="sxs-lookup"><span data-stu-id="e817c-116">Open CMD</span></span>
1. <span data-ttu-id="e817c-117">Задайте пользователя по умолчанию Linux: `root`.</span><span class="sxs-lookup"><span data-stu-id="e817c-117">Set the default Linux user to `root`:</span></span>

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. <span data-ttu-id="e817c-118">Запустите дистрибутив Linux (`ubuntu`).</span><span class="sxs-lookup"><span data-stu-id="e817c-118">Launch your Linux distribution (`ubuntu`).</span></span>  <span data-ttu-id="e817c-119">Вы автоматически войдете в систему как `root`.</span><span class="sxs-lookup"><span data-stu-id="e817c-119">You will automatically login as `root`:</span></span>

1. <span data-ttu-id="e817c-120">Сбросьте пароль с помощью команды `passwd`.</span><span class="sxs-lookup"><span data-stu-id="e817c-120">Reset your password using the `passwd` command:</span></span>

    ```BASH
    $ passwd username
    ```

1. <span data-ttu-id="e817c-121">В командной строке Windows сбросьте пользователя по умолчанию, превратив его в обычную учетную запись пользователя Linux.</span><span class="sxs-lookup"><span data-stu-id="e817c-121">From Windows CMD, reset your default user back to your normal Linux user account.</span></span>

    ```console
    C:\> ubuntu config --default-user username
    ```
