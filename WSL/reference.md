---
title: Подсистема Windows для ссылки на команды Linux
description: Список команд, которые управляют подсистема Windows для Linux
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.openlocfilehash: 978a35d593e37877949c24cbd833a519888d54bf
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063582"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="0b047-104">Справочник по командам подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="0b047-104">Command Reference for Windows Subsystem for Linux</span></span>

> `lxrun.exe` <span data-ttu-id="0b047-105">— не рекомендуется, начиная с Windows 10 версии 1803 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="0b047-105">is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="0b047-106">Команда `lxrun.exe` может использоваться для взаимодействия с [подсистемы Windows для Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) напрямую.</span><span class="sxs-lookup"><span data-stu-id="0b047-106">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="0b047-107">Эти команды устанавливаются в `\Windows\System32` каталога и может быть запущена из командной строки Windows или в PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0b047-107">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

* `lxrun.exe` <span data-ttu-id="0b047-108">используется для управления WSL.</span><span class="sxs-lookup"><span data-stu-id="0b047-108">is used to manage WSL.</span></span>  <span data-ttu-id="0b047-109">Эту команду можно использовать для установки или удаления образа Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="0b047-109">This command can be used to install or uninstall the Ubuntu image.</span></span>


| <span data-ttu-id="0b047-110">Command</span><span class="sxs-lookup"><span data-stu-id="0b047-110">Command</span></span>                     | <span data-ttu-id="0b047-111">Описание</span><span class="sxs-lookup"><span data-stu-id="0b047-111">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `bash`                      | <span data-ttu-id="0b047-112">Запускает оболочку Bash, в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="0b047-112">Launches the Bash shell in the current directory.</span></span>  <span data-ttu-id="0b047-113">Если оболочка Bash не устанавливается автоматически выполняется</span><span class="sxs-lookup"><span data-stu-id="0b047-113">If the Bash shell is not installed automatically runs</span></span> `lxrun /install` |
| `bash ~`                    | <span data-ttu-id="0b047-114">Запускает оболочку bash в домашнем каталоге пользователя Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="0b047-114">Launches the bash shell into the user's Ubuntu home directory.</span></span>  <span data-ttu-id="0b047-115">Аналогично выполнению компакт-диска ~</span><span class="sxs-lookup"><span data-stu-id="0b047-115">Similar to running cd ~</span></span>            |
| `bash -c "<command>"`       | <span data-ttu-id="0b047-116">Выполняет команду, выводит выходные данные и завершает работу обратно в командной строке Windows.</span><span class="sxs-lookup"><span data-stu-id="0b047-116">Runs the command, prints the output and exits back to the Windows command prompt.</span></span> <br/> <br/> <span data-ttu-id="0b047-117">Пример: **bash -c «ls»**</span><span class="sxs-lookup"><span data-stu-id="0b047-117">Example:  **bash -c "ls"**</span></span> |

<p>

| <span data-ttu-id="0b047-118">Command</span><span class="sxs-lookup"><span data-stu-id="0b047-118">Command</span></span>                     | <span data-ttu-id="0b047-119">Описание</span><span class="sxs-lookup"><span data-stu-id="0b047-119">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="0b047-120">Команда lxrun используется для управления экземпляром WSL.</span><span class="sxs-lookup"><span data-stu-id="0b047-120">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="0b047-121">Начнется загрузка и процесс установки.</span><span class="sxs-lookup"><span data-stu-id="0b047-121">Starts the download and install process.</span></span> <br/> <span data-ttu-id="0b047-122">**/y** может быть добавлена к обойти все запросы.</span><span class="sxs-lookup"><span data-stu-id="0b047-122">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="0b047-123">Запрос на подтверждение принимаются автоматически и пользователь по умолчанию имеет значение root.</span><span class="sxs-lookup"><span data-stu-id="0b047-123">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="0b047-124">Удаляет и удаляет образ Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="0b047-124">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="0b047-125">По умолчанию не будет удален домашний каталог пользователя Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="0b047-125">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="0b047-126">**/y** может добавляться автоматически принимать запрос на подтверждение</span><span class="sxs-lookup"><span data-stu-id="0b047-126">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="0b047-127">**/ full** удаляет и удаляет домашний каталог пользователя Ubuntu</span><span class="sxs-lookup"><span data-stu-id="0b047-127">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="0b047-128">Устанавливает по умолчанию Bash на Ubuntu пользователя.</span><span class="sxs-lookup"><span data-stu-id="0b047-128">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="0b047-129">Предложит ввести пароль, если указанный пользователь не существует.</span><span class="sxs-lookup"><span data-stu-id="0b047-129">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="0b047-130">Дополнительные сведения см. в статье: https://aka.ms/wslusers.</span><span class="sxs-lookup"><span data-stu-id="0b047-130">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="0b047-131">**/y** promping обходит пароля.</span><span class="sxs-lookup"><span data-stu-id="0b047-131">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="0b047-132">Пользователь будет создаваться без пароля.</span><span class="sxs-lookup"><span data-stu-id="0b047-132">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="0b047-133">Обновляет индекс пакета подсистемы</span><span class="sxs-lookup"><span data-stu-id="0b047-133">Updates the subsystem's package index</span></span>          |
