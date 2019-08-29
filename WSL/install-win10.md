---
title: Установка подсистемы Windows для Linux (WSL) в Windows 10
description: Инструкции по установке для подсистемы Windows для Linux в Windows 10.
keywords: Башонвиндовс, bash, WSL, Windows, подсистема Windows для Linux, виндовссубсистем, Ubuntu, Debian, SUSE, Windows 10, install
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 218e3e652d0849f944e8aaceef3fb954294222be
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122768"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="3cb8c-104">Руководства по установке подсистемы Windows для Linux для Windows 10</span><span class="sxs-lookup"><span data-stu-id="3cb8c-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="3cb8c-105">Установка подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="3cb8c-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="3cb8c-106">Перед установкой дистрибутивов Linux для WSL необходимо убедиться, что включена дополнительная функция "подсистема Windows для Linux":</span><span class="sxs-lookup"><span data-stu-id="3cb8c-106">Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:</span></span>

1. <span data-ttu-id="3cb8c-107">Откройте PowerShell от имени администратора и выполните команду:</span><span class="sxs-lookup"><span data-stu-id="3cb8c-107">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="3cb8c-108">При появлении запроса перезагрузите компьютер.</span><span class="sxs-lookup"><span data-stu-id="3cb8c-108">Restart your computer when prompted.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="3cb8c-109">Установка дистрибутива Linux по выбору</span><span class="sxs-lookup"><span data-stu-id="3cb8c-109">Install your Linux Distribution of Choice</span></span>
<span data-ttu-id="3cb8c-110">Чтобы скачать и установить предпочтительные дистрибутив, вы можете выбрать три варианта:</span><span class="sxs-lookup"><span data-stu-id="3cb8c-110">To download and install your preferred distro(s), you have three choices:</span></span>
1. <span data-ttu-id="3cb8c-111">Скачать и установить из Microsoft Store (см. ниже)</span><span class="sxs-lookup"><span data-stu-id="3cb8c-111">Download and install from the Microsoft Store (see below)</span></span>
1. <span data-ttu-id="3cb8c-112">Скачайте и установите из командной строки или сценария (см.[инструкции по установке вручную](install-manual.md)).</span><span class="sxs-lookup"><span data-stu-id="3cb8c-112">Download and install from the Command-Line/Script ([read the manual installation instructions](install-manual.md))</span></span>
1. <span data-ttu-id="3cb8c-113">Загрузка и ручное Распаковка и установка (для Windows Server — [инструкции здесь](install-on-server.md))</span><span class="sxs-lookup"><span data-stu-id="3cb8c-113">Download and manually unpack and install (for Windows Server - [instructions here](install-on-server.md))</span></span>

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a><span data-ttu-id="3cb8c-114">Обновления Windows 10 для дизайнеров и более поздних версий: Установка из Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="3cb8c-114">Windows 10 Fall Creators Update and later: Install from the Microsoft Store</span></span>

> <span data-ttu-id="3cb8c-115">Этот раздел предназначен для Windows Build 16215 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="3cb8c-115">This section is for Windows build 16215 or later.</span></span>  <span data-ttu-id="3cb8c-116">Выполните следующие действия, чтобы [проверить сборку](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="3cb8c-116">Follow these steps to [check your build](troubleshooting.md#check-your-build-number).</span></span> 

1. <span data-ttu-id="3cb8c-117">Откройте Microsoft Store и выберите предпочтительный дистрибутив Linux.</span><span class="sxs-lookup"><span data-stu-id="3cb8c-117">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Представление дистрибутивов Linux в Microsoft Store](media/store.png)

    <span data-ttu-id="3cb8c-119">Следующие ссылки открывают страницу Microsoft Store для каждого дистрибутива:</span><span class="sxs-lookup"><span data-stu-id="3cb8c-119">The following links will open the Microsoft store page for each distribution:</span></span>

    * [<span data-ttu-id="3cb8c-120">Ubuntu 16,04 LTS</span><span class="sxs-lookup"><span data-stu-id="3cb8c-120">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [<span data-ttu-id="3cb8c-121">Ubuntu 18,04 LTS</span><span class="sxs-lookup"><span data-stu-id="3cb8c-121">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [<span data-ttu-id="3cb8c-122">OpenSUSE LEAP 15</span><span class="sxs-lookup"><span data-stu-id="3cb8c-122">OpenSUSE Leap 15</span></span>](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [<span data-ttu-id="3cb8c-123">OpenSUSE LEAP 42</span><span class="sxs-lookup"><span data-stu-id="3cb8c-123">OpenSUSE Leap 42</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [<span data-ttu-id="3cb8c-124">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="3cb8c-124">SUSE Linux Enterprise Server 12</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [<span data-ttu-id="3cb8c-125">SUSE Linux Enterprise Server 15</span><span class="sxs-lookup"><span data-stu-id="3cb8c-125">SUSE Linux Enterprise Server 15</span></span>](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [<span data-ttu-id="3cb8c-126">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="3cb8c-126">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [<span data-ttu-id="3cb8c-127">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="3cb8c-127">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [<span data-ttu-id="3cb8c-128">Fedora Remix для WSL</span><span class="sxs-lookup"><span data-stu-id="3cb8c-128">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [<span data-ttu-id="3cb8c-129">пенгвин</span><span class="sxs-lookup"><span data-stu-id="3cb8c-129">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [<span data-ttu-id="3cb8c-130">Пенгвин Enterprise</span><span class="sxs-lookup"><span data-stu-id="3cb8c-130">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [<span data-ttu-id="3cb8c-131">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="3cb8c-131">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

1. <span data-ttu-id="3cb8c-132">На странице дистрибутив выберите Get (получить).</span><span class="sxs-lookup"><span data-stu-id="3cb8c-132">From the distro's page, select "Get"</span></span>

    ![Представление дистрибутивов Linux в Microsoft Store](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="3cb8c-134">Завершение инициализации дистрибутив</span><span class="sxs-lookup"><span data-stu-id="3cb8c-134">Complete initialization of your distro</span></span>
<span data-ttu-id="3cb8c-135">После установки дистрибутив для Linux необходимо [инициализировать новый экземпляр дистрибутив](initialize-distro.md) , прежде чем его можно будет использовать.</span><span class="sxs-lookup"><span data-stu-id="3cb8c-135">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) once, before it can be used.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="3cb8c-136">Устранение неполадок:</span><span class="sxs-lookup"><span data-stu-id="3cb8c-136">Troubleshooting:</span></span> 

<span data-ttu-id="3cb8c-137">Ниже приведены связанные ошибки и предлагаемые исправления.</span><span class="sxs-lookup"><span data-stu-id="3cb8c-137">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="3cb8c-138">Другие распространенные ошибки и их решения см. на [странице Устранение неполадок WSL](troubleshooting.md) .</span><span class="sxs-lookup"><span data-stu-id="3cb8c-138">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

* <span data-ttu-id="3cb8c-139">**Сбой установки с ошибкой 0x80070003**</span><span class="sxs-lookup"><span data-stu-id="3cb8c-139">**Installation failed with error 0x80070003**</span></span>
    * <span data-ttu-id="3cb8c-140">Подсистема Windows для Linux работает только на системном диске (обычно это `C:` диск).</span><span class="sxs-lookup"><span data-stu-id="3cb8c-140">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="3cb8c-141">Убедитесь, что дистрибутивов хранятся на системном диске:</span><span class="sxs-lookup"><span data-stu-id="3cb8c-141">Make sure that distros are stored on your system drive:</span></span>  
    * <span data-ttu-id="3cb8c-142">Откройте **Параметры** -> хранилище Дополнительныепараметры->хранилища: \*\* Изменение места сохранения\*\*
    новогосодержимогорисунокпараметровсистемыдляустановкиприложенийнадискеC:![](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="3cb8c-142">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>
    
    
 * <span data-ttu-id="3cb8c-143">**Сбой Вслрегистердистрибутион с ошибкой 0x8007019e**</span><span class="sxs-lookup"><span data-stu-id="3cb8c-143">**WslRegisterDistribution failed with error 0x8007019e**</span></span>   
  * <span data-ttu-id="3cb8c-144">Необязательный компонент подсистемы Windows для Linux не включен:</span><span class="sxs-lookup"><span data-stu-id="3cb8c-144">The Windows Subsystem for Linux optional component is not enabled:</span></span> 
   * <span data-ttu-id="3cb8c-145">Откройте **панель** -> управления**программы и компоненты** -> **Включение или отключение компонента Windows** . > проверить подсистему **Windows для Linux** или использовать командлет PowerShell, упомянутый в начале этой статьи.</span><span class="sxs-lookup"><span data-stu-id="3cb8c-145">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>
