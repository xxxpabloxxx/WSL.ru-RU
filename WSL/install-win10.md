---
title: Установка подсистемы Windows для Linux (WSL) в Windows 10
description: Инструкции по установке подсистемы Windows для Linux в Windows 10.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, debian, suse, windows 10, установка
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: d30a5883d648e084193659e997c55d203eb5a735
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/12/2019
ms.locfileid: "67035050"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="9a95b-104">Подсистема Windows для Linux руководство по установке для Windows 10</span><span class="sxs-lookup"><span data-stu-id="9a95b-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="9a95b-105">Установите подсистему Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="9a95b-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="9a95b-106">Прежде чем устанавливать все дистрибутивы Linux для WSL, необходимо убедиться, что «Windows подсистемы для Linux» необязательный параметр:</span><span class="sxs-lookup"><span data-stu-id="9a95b-106">Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:</span></span>

1. <span data-ttu-id="9a95b-107">Откройте PowerShell от имени администратора и выполните:</span><span class="sxs-lookup"><span data-stu-id="9a95b-107">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="9a95b-108">Перезагрузите компьютер при появлении запроса.</span><span class="sxs-lookup"><span data-stu-id="9a95b-108">Restart your computer when prompted.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="9a95b-109">Установка дистрибутива Linux по выбору</span><span class="sxs-lookup"><span data-stu-id="9a95b-109">Install your Linux Distribution of Choice</span></span>
<span data-ttu-id="9a95b-110">Чтобы скачать и установить ваш предпочитаемый distro(s), у вас есть три варианта:</span><span class="sxs-lookup"><span data-stu-id="9a95b-110">To download and install your preferred distro(s), you have three choices:</span></span>
1. <span data-ttu-id="9a95b-111">Загрузите и установите Windows Store (см. ниже)</span><span class="sxs-lookup"><span data-stu-id="9a95b-111">Download and install from the Windows Store (see below)</span></span>
1. <span data-ttu-id="9a95b-112">Загрузить и установить из командной-строки или сценария ([прочитать инструкции по ручной установке](install-manual.md))</span><span class="sxs-lookup"><span data-stu-id="9a95b-112">Download and install from the Command-Line/Script ([read the manual installation instructions](install-manual.md))</span></span>
1. <span data-ttu-id="9a95b-113">Скачайте и распакуйте и установить вручную (для Windows Server - [приведенным ниже указаниям](install-on-server.md))</span><span class="sxs-lookup"><span data-stu-id="9a95b-113">Download and manually unpack and install (for Windows Server - [instructions here](install-on-server.md))</span></span>

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a><span data-ttu-id="9a95b-114">Windows 10 Fall Creators Update и более поздних версий: Установка из Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="9a95b-114">Windows 10 Fall Creators Update and later: Install from the Microsoft Store</span></span>

> <span data-ttu-id="9a95b-115">Этот раздел предназначен для построения 16215 или более поздней версии Windows.</span><span class="sxs-lookup"><span data-stu-id="9a95b-115">This section is for Windows build 16215 or later.</span></span>  <span data-ttu-id="9a95b-116">Выполните следующие действия для [проверьте построения](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="9a95b-116">Follow these steps to [check your build](troubleshooting.md#check-your-build-number).</span></span> 

1. <span data-ttu-id="9a95b-117">Откройте Microsoft Store и выберите избранные дистрибутива Linux.</span><span class="sxs-lookup"><span data-stu-id="9a95b-117">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Представление из дистрибутивов Linux в магазине Windows](media/store.png)

    <span data-ttu-id="9a95b-119">Приведенные ниже ссылки откроется на странице магазина Windows для каждого распределения:</span><span class="sxs-lookup"><span data-stu-id="9a95b-119">The following links will open the Windows store page for each distribution:</span></span>

    * [<span data-ttu-id="9a95b-120">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="9a95b-120">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [<span data-ttu-id="9a95b-121">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="9a95b-121">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [<span data-ttu-id="9a95b-122">OpenSUSE Leap 15</span><span class="sxs-lookup"><span data-stu-id="9a95b-122">OpenSUSE Leap 15</span></span>](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [<span data-ttu-id="9a95b-123">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="9a95b-123">OpenSUSE Leap 42</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [<span data-ttu-id="9a95b-124">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="9a95b-124">SUSE Linux Enterprise Server 12</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [<span data-ttu-id="9a95b-125">SUSE Linux Enterprise Server 15</span><span class="sxs-lookup"><span data-stu-id="9a95b-125">SUSE Linux Enterprise Server 15</span></span>](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [<span data-ttu-id="9a95b-126">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="9a95b-126">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [<span data-ttu-id="9a95b-127">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="9a95b-127">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [<span data-ttu-id="9a95b-128">Remix Fedora для WSL</span><span class="sxs-lookup"><span data-stu-id="9a95b-128">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [<span data-ttu-id="9a95b-129">WLinux</span><span class="sxs-lookup"><span data-stu-id="9a95b-129">WLinux</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [<span data-ttu-id="9a95b-130">WLinux Enterprise</span><span class="sxs-lookup"><span data-stu-id="9a95b-130">WLinux Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [<span data-ttu-id="9a95b-131">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="9a95b-131">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

1. <span data-ttu-id="9a95b-132">На странице дистрибутива выберите «Получить»</span><span class="sxs-lookup"><span data-stu-id="9a95b-132">From the distro's page, select "Get"</span></span>

    ![Представление из дистрибутивов Linux в магазине Windows](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="9a95b-134">Завершения инициализации из вашего дистрибутива</span><span class="sxs-lookup"><span data-stu-id="9a95b-134">Complete initialization of your distro</span></span>
<span data-ttu-id="9a95b-135">Теперь, когда устанавливается дистрибутив Linux, необходимо [инициализации в новом экземпляре дистрибутива](initialize-distro.md) один раз, прежде чем можно будет использовать.</span><span class="sxs-lookup"><span data-stu-id="9a95b-135">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) once, before it can be used.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="9a95b-136">Устранение неполадок:</span><span class="sxs-lookup"><span data-stu-id="9a95b-136">Troubleshooting:</span></span> 

<span data-ttu-id="9a95b-137">Ниже приведены ошибки, связанные с и предлагаемые исправления.</span><span class="sxs-lookup"><span data-stu-id="9a95b-137">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="9a95b-138">Ссылаться на [WSL странице](troubleshooting.md) для других распространенных ошибок и способы их решения.</span><span class="sxs-lookup"><span data-stu-id="9a95b-138">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

* <span data-ttu-id="9a95b-139">**Установка завершилась ошибкой 0x80070003**</span><span class="sxs-lookup"><span data-stu-id="9a95b-139">**Installation failed with error 0x80070003**</span></span>
    * <span data-ttu-id="9a95b-140">Подсистема Windows для Linux выполняется только на системном диске (обычно это ваш `C:` диска).</span><span class="sxs-lookup"><span data-stu-id="9a95b-140">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="9a95b-141">Убедитесь, что на системном диске хранятся дистрибутивов:</span><span class="sxs-lookup"><span data-stu-id="9a95b-141">Make sure that distros are stored on your system drive:</span></span>  
    * <span data-ttu-id="9a95b-142">Откройте **параметры** -> **хранения** -> **Дополнительные параметры хранилища: Изменение, где сохраняется новое содержимое**
    ![картину системных параметров для установки приложений на диске C:](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="9a95b-142">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>
    
    
 * <span data-ttu-id="9a95b-143">**Сбой с ошибкой 0x8007019e WslRegisterDistribution**</span><span class="sxs-lookup"><span data-stu-id="9a95b-143">**WslRegisterDistribution failed with error 0x8007019e**</span></span>   
  * <span data-ttu-id="9a95b-144">Подсистема Windows для Linux, дополнительный компонент не включен:</span><span class="sxs-lookup"><span data-stu-id="9a95b-144">The Windows Subsystem for Linux optional component is not enabled:</span></span> 
   * <span data-ttu-id="9a95b-145">Откройте **панели управления** -> **программы и компоненты** "->" \*\* Включение или отключение компонентов Windows \*\* -> Проверка **подсистема Windows для Linux** или с помощью Командлет PowerShell, упомянутых в начале этой статьи.</span><span class="sxs-lookup"><span data-stu-id="9a95b-145">Open **Control Panel** -> **Programs and Features** -> \*\*Turn Windows Feature on or off \*\* -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>
