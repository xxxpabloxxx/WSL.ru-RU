---
title: Создание и обновление учетных записей пользователей для дистрибутивов WSL
description: Справочные материалы по управлению учетными записями пользователей и разрешениями для подсистемы Windows для Linux.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, учетные записи пользователей
ms.date: 01/20/2020
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 30dea11adb68639f645ca800a695b0404661845a
ms.sourcegitcommit: e5fb773dd44abab7bcf289340da00f59528b88f7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "76973684"
---
# <a name="create-and-update-user-accounts-for-wsl-distributions"></a><span data-ttu-id="f4d5b-104">Создание и обновление учетных записей пользователей для дистрибутивов WSL</span><span class="sxs-lookup"><span data-stu-id="f4d5b-104">Create and update user accounts for WSL distributions</span></span>

<span data-ttu-id="f4d5b-105">Когда вы включите WSL и установите дистрибутив Linux из Microsoft Store, при открытии установленного дистрибутива Linux вам нужно будет сразу создать учетную запись и указать **имя пользователя** и **пароль**.</span><span class="sxs-lookup"><span data-stu-id="f4d5b-105">Once you have enabled WSL and installed a Linux distribution from the Microsoft Store, the first step you will be asked to complete when opening your newly installed Linux distribution is to create an account, including a **User Name** and **Password**.</span></span>

- <span data-ttu-id="f4d5b-106">Эти **имя пользователя** и **пароль** относятся к дистрибутиву Linux и не связаны с именем пользователя Windows.</span><span class="sxs-lookup"><span data-stu-id="f4d5b-106">This **User Name** and **Password** is specific to your Linux distribution and has no bearing on your Windows user name.</span></span>

- <span data-ttu-id="f4d5b-107">После создания этого **имени пользователя** и **пароля** учетная запись будет использоваться по умолчанию для этого дистрибутива, и вы сможете автоматически входить в систему при запуске.</span><span class="sxs-lookup"><span data-stu-id="f4d5b-107">Once you create this **User Name** and **Password**, the account will be your default user for the distribution and automatically sign-in on launch.</span></span>

- <span data-ttu-id="f4d5b-108">Эта учетная запись будет считаться администратором Linux с возможностью запуска административных команд `sudo` (команд суперпользователя).</span><span class="sxs-lookup"><span data-stu-id="f4d5b-108">This account will be considered the Linux administrator, with the ability to run `sudo` (Super User Do) administrative commands.</span></span>

- <span data-ttu-id="f4d5b-109">Каждый дистрибутив Linux, работающий в подсистеме Windows для Linux, имеет собственные учетные записи пользователей Linux с паролями.</span><span class="sxs-lookup"><span data-stu-id="f4d5b-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="f4d5b-110">Учетную запись пользователя Linux нужно настраивать при каждом добавлении, переустановке или сбросе дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="f4d5b-110">You will have to configure a Linux user account every time you add a distribution, reinstall, or reset.</span></span>

## <a name="reset-your-linux-password"></a><span data-ttu-id="f4d5b-111">Сброс пароля Linux</span><span class="sxs-lookup"><span data-stu-id="f4d5b-111">Reset your Linux password</span></span>

<span data-ttu-id="f4d5b-112">Чтобы изменить пароль, откройте дистрибутив Linux (например, Ubuntu) и выполните команду `passwd`.</span><span class="sxs-lookup"><span data-stu-id="f4d5b-112">To change your password, open your Linux distribution (Ubuntu for example) and enter the command: `passwd`</span></span>

<span data-ttu-id="f4d5b-113">Вам будет предложено ввести текущий пароль, а затем появится запрос на ввод нового пароля, который нужно подтвердить.</span><span class="sxs-lookup"><span data-stu-id="f4d5b-113">You will be asked to enter your current password, then asked to enter your new password, and then to confirm your new password.</span></span>

### <a name="forgot-your-password"></a><span data-ttu-id="f4d5b-114">Пароль утерян</span><span class="sxs-lookup"><span data-stu-id="f4d5b-114">Forgot your password</span></span>

<span data-ttu-id="f4d5b-115">Если вы забыли пароль для дистрибутива Linux, сделайте следующее.</span><span class="sxs-lookup"><span data-stu-id="f4d5b-115">If you forgot the password for your Linux distribution:</span></span>

1. <span data-ttu-id="f4d5b-116">Откройте PowerShell и перейдите в корень дистрибутива WSL по умолчанию с помощью команды `wsl -u root`.</span><span class="sxs-lookup"><span data-stu-id="f4d5b-116">Open PowerShell and enter the root of your default WSL distribution using the command: `wsl -u root`</span></span>

> <span data-ttu-id="f4d5b-117">Если вам нужно обновить забытый пароль в дистрибутиве, который не используется по умолчанию, используйте команду `wsl -d Debian -u root`, заменив `Debian` именем целевого дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="f4d5b-117">If you need to update the forgotten password on a distribution that is not your default, use the command: `wsl -d Debian -u root`, replacing `Debian` with the name of your targeted distribution.</span></span>

2. <span data-ttu-id="f4d5b-118">Открыв дистрибутив WSL на корневом уровне в PowerShell, вы можете использовать для обновления пароля команду `passwd`.</span><span class="sxs-lookup"><span data-stu-id="f4d5b-118">Once your WSL distribution has been opened at the root level inside PowerShell, you can use this command to update your password: `passwd`</span></span>

3. <span data-ttu-id="f4d5b-119">Вам будет предложено ввести новый пароль UNIX, а затем подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f4d5b-119">You will be prompted to enter a new UNIX password and then confirm that password.</span></span> <span data-ttu-id="f4d5b-120">Когда пароль будет обновлен, закройте WSL в PowerShell, выполнив команду `exit`.</span><span class="sxs-lookup"><span data-stu-id="f4d5b-120">Once you're told that the password has updated successfully, close WSL inside of PowerShell using the command: `exit`</span></span>

> [!NOTE]
> <span data-ttu-id="f4d5b-121">Если вы используете раннюю версию ОС Windows, например 1703 (Creators Update) или 1709 (Fall Creators Update), см. [архивный документ по обновлению такой учетной записи](./user-support-archived.md).</span><span class="sxs-lookup"><span data-stu-id="f4d5b-121">If you are running an early version of Windows operating system, like 1703 (Creators Update) or 1709 (Fall Creators Update), see the [archived version of this user account update doc](./user-support-archived.md).</span></span>
