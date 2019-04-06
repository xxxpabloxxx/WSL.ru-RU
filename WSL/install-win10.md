---
title: Установка подсистемы Windows для Linux (WSL) на в Windows 10
description: Инструкции по установке подсистемы Windows для Linux в Windows 10.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, debian, suse, windows 10, установка
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 40bbe73acbfd0483e18ab6ff1696fdb44eaff2e4
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063292"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="6e60a-104">Подсистема Windows для Linux руководство по установке для Windows 10</span><span class="sxs-lookup"><span data-stu-id="6e60a-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="6e60a-105">Установите подсистему Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="6e60a-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="6e60a-106">Прежде чем устанавливать все дистрибутивы Linux для WSL, необходимо убедиться, что «Windows подсистемы для Linux» необязательный параметр:</span><span class="sxs-lookup"><span data-stu-id="6e60a-106">Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:</span></span>

1. <span data-ttu-id="6e60a-107">Откройте PowerShell от имени администратора и выполните:</span><span class="sxs-lookup"><span data-stu-id="6e60a-107">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="6e60a-108">Перезагрузите компьютер при появлении запроса.</span><span class="sxs-lookup"><span data-stu-id="6e60a-108">Restart your computer when prompted.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="6e60a-109">Установка дистрибутива Linux по выбору</span><span class="sxs-lookup"><span data-stu-id="6e60a-109">Install your Linux Distribution of Choice</span></span>
<span data-ttu-id="6e60a-110">Чтобы скачать и установить ваш предпочитаемый distro(s), у вас есть три варианта:</span><span class="sxs-lookup"><span data-stu-id="6e60a-110">To download and install your preferred distro(s), you have three choices:</span></span>
1. <span data-ttu-id="6e60a-111">Загрузите и установите Windows Store (см. ниже)</span><span class="sxs-lookup"><span data-stu-id="6e60a-111">Download and install from the Windows Store (see below)</span></span>
1. <span data-ttu-id="6e60a-112">Загрузить и установить из командной-строки или сценария ([прочитать инструкции по ручной установке](install-manual.md))</span><span class="sxs-lookup"><span data-stu-id="6e60a-112">Download and install from the Command-Line/Script ([read the manual installation instructions](install-manual.md))</span></span>
1. <span data-ttu-id="6e60a-113">Скачайте и распакуйте и установить вручную (для Windows Server - [приведенным ниже указаниям](install-on-server.md))</span><span class="sxs-lookup"><span data-stu-id="6e60a-113">Download and manually unpack and install (for Windows Server - [instructions here](install-on-server.md))</span></span>

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a><span data-ttu-id="6e60a-114">Windows 10 Fall Creators Update и более поздних версий: Установка из Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="6e60a-114">Windows 10 Fall Creators Update and later: Install from the Microsoft Store</span></span>

> <span data-ttu-id="6e60a-115">Этот раздел предназначен для построения 16215 или более поздней версии Windows.</span><span class="sxs-lookup"><span data-stu-id="6e60a-115">This section is for Windows build 16215 or later.</span></span>  <span data-ttu-id="6e60a-116">Выполните следующие действия для [проверьте построения](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="6e60a-116">Follow these steps to [check your build](troubleshooting.md#check-your-build-number).</span></span> 

1. <span data-ttu-id="6e60a-117">Откройте Microsoft Store и выберите избранные дистрибутива Linux.</span><span class="sxs-lookup"><span data-stu-id="6e60a-117">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Представление из дистрибутивов Linux в магазине Windows](media/store.png)

    <span data-ttu-id="6e60a-119">Приведенные ниже ссылки откроется на странице магазина Windows для каждого распределения:</span><span class="sxs-lookup"><span data-stu-id="6e60a-119">The following links will open the Windows store page for each distribution:</span></span>

    * [<span data-ttu-id="6e60a-120">Ubuntu</span><span class="sxs-lookup"><span data-stu-id="6e60a-120">Ubuntu</span></span>](https://www.microsoft.com/store/p/ubuntu/9nblggh4msv6)
    * [<span data-ttu-id="6e60a-121">openSUSE</span><span class="sxs-lookup"><span data-stu-id="6e60a-121">OpenSUSE</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [<span data-ttu-id="6e60a-122">SLES</span><span class="sxs-lookup"><span data-stu-id="6e60a-122">SLES</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [<span data-ttu-id="6e60a-123">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="6e60a-123">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [<span data-ttu-id="6e60a-124">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="6e60a-124">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)

1. <span data-ttu-id="6e60a-125">На странице дистрибутива выберите «Получить»</span><span class="sxs-lookup"><span data-stu-id="6e60a-125">From the distro's page, select "Get"</span></span>

    ![Представление из дистрибутивов Linux в магазине Windows](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="6e60a-127">Завершения инициализации из вашего дистрибутива</span><span class="sxs-lookup"><span data-stu-id="6e60a-127">Complete initialization of your distro</span></span>
<span data-ttu-id="6e60a-128">Теперь, когда устанавливается дистрибутив Linux, необходимо [инициализации в новом экземпляре дистрибутива](initialize-distro.md) один раз, прежде чем можно будет использовать.</span><span class="sxs-lookup"><span data-stu-id="6e60a-128">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) once, before it can be used.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="6e60a-129">Устранение неполадок:</span><span class="sxs-lookup"><span data-stu-id="6e60a-129">Troubleshooting:</span></span> 

<span data-ttu-id="6e60a-130">Ниже приведены ошибки, связанные с и предлагаемые исправления.</span><span class="sxs-lookup"><span data-stu-id="6e60a-130">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="6e60a-131">Ссылаться на [WSL странице](troubleshooting.md) для других распространенных ошибок и способы их решения.</span><span class="sxs-lookup"><span data-stu-id="6e60a-131">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

* **<span data-ttu-id="6e60a-132">Установка завершилась ошибкой 0x80070003</span><span class="sxs-lookup"><span data-stu-id="6e60a-132">Installation failed with error 0x80070003</span></span>**
    * <span data-ttu-id="6e60a-133">Подсистема Windows для Linux выполняется только на системном диске (обычно это ваш `C:` диска).</span><span class="sxs-lookup"><span data-stu-id="6e60a-133">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="6e60a-134">Убедитесь, что на системном диске хранятся дистрибутивов:</span><span class="sxs-lookup"><span data-stu-id="6e60a-134">Make sure that distros are stored on your system drive:</span></span>  
    * <span data-ttu-id="6e60a-135">Откройте **параметры** -> **хранения** -> **Дополнительные параметры хранилища: Изменение, где сохраняется новое содержимое**
    ![картину системных параметров для установки приложений на диске C:](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="6e60a-135">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>
