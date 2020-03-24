---
title: Установка подсистемы Windows для Linux (WSL) в Windows 10
description: Инструкции по установке подсистемы Windows для Linux в Windows 10.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, debian, suse, windows 10, установка
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 17ca32db23b426ef1367ff9444b5924d9d7e1716
ms.sourcegitcommit: 3be576f946611cf36e27745bdb7c4c52af1b9928
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "74200235"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="2aeec-104">Руководство по установке подсистемы Windows для Linux в Windows 10</span><span class="sxs-lookup"><span data-stu-id="2aeec-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="2aeec-105">Установка подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="2aeec-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="2aeec-106">Перед установкой каких-либо дистрибутивов Linux для WSL необходимо убедиться, что включен дополнительный компонент "Подсистема Windows для Linux".</span><span class="sxs-lookup"><span data-stu-id="2aeec-106">Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:</span></span>

1. <span data-ttu-id="2aeec-107">Запустите PowerShell с правами администратора и выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="2aeec-107">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="2aeec-108">При появлении соответствующего запроса перезагрузите компьютер.</span><span class="sxs-lookup"><span data-stu-id="2aeec-108">Restart your computer when prompted.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="2aeec-109">Установка дистрибутива Linux по выбору</span><span class="sxs-lookup"><span data-stu-id="2aeec-109">Install your Linux Distribution of Choice</span></span>
<span data-ttu-id="2aeec-110">Чтобы скачать и установить предпочтительные дистрибутивы, у вас есть три варианта:</span><span class="sxs-lookup"><span data-stu-id="2aeec-110">To download and install your preferred distro(s), you have three choices:</span></span>
* <span data-ttu-id="2aeec-111">Скачайте и установите их из Microsoft Store (см. ниже).</span><span class="sxs-lookup"><span data-stu-id="2aeec-111">Download and install from the Microsoft Store (see below)</span></span>
* <span data-ttu-id="2aeec-112">Скачайте и установите их с помощью командной строки или сценария ([ознакомьтесь с инструкциями по установке вручную](install-manual.md)).</span><span class="sxs-lookup"><span data-stu-id="2aeec-112">Download and install from the Command-Line/Script ([read the manual installation instructions](install-manual.md))</span></span>
* <span data-ttu-id="2aeec-113">Скачайте их, а затем вручную распакуйте и установите (инструкции для Windows Server доступны [здесь](install-on-server.md)).</span><span class="sxs-lookup"><span data-stu-id="2aeec-113">Download and manually unpack and install (for Windows Server - [instructions here](install-on-server.md))</span></span>

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a><span data-ttu-id="2aeec-114">Windows 10 Fall Creators Update и более поздние версии: установка из Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="2aeec-114">Windows 10 Fall Creators Update and later: Install from the Microsoft Store</span></span>

> <span data-ttu-id="2aeec-115">Этот раздел предназначен для сборки 16215 Windows или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="2aeec-115">This section is for Windows build 16215 or later.</span></span>  <span data-ttu-id="2aeec-116">Выполните следующие действия, чтобы [узнать номер своей сборки](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="2aeec-116">Follow these steps to [check your build](troubleshooting.md#check-your-build-number).</span></span> 

1. <span data-ttu-id="2aeec-117">Откройте Microsoft Store и выберите предпочтительный дистрибутив Linux.</span><span class="sxs-lookup"><span data-stu-id="2aeec-117">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Представление дистрибутивов Linux в Microsoft Store](media/store.png)

    <span data-ttu-id="2aeec-119">Ниже приведены ссылки на страницы Microsoft Store для каждого дистрибутива:</span><span class="sxs-lookup"><span data-stu-id="2aeec-119">The following links will open the Microsoft store page for each distribution:</span></span>

    * [<span data-ttu-id="2aeec-120">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="2aeec-120">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [<span data-ttu-id="2aeec-121">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="2aeec-121">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [<span data-ttu-id="2aeec-122">OpenSUSE Leap 15</span><span class="sxs-lookup"><span data-stu-id="2aeec-122">OpenSUSE Leap 15</span></span>](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [<span data-ttu-id="2aeec-123">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="2aeec-123">OpenSUSE Leap 42</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [<span data-ttu-id="2aeec-124">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="2aeec-124">SUSE Linux Enterprise Server 12</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [<span data-ttu-id="2aeec-125">SUSE Linux Enterprise Server 15</span><span class="sxs-lookup"><span data-stu-id="2aeec-125">SUSE Linux Enterprise Server 15</span></span>](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [<span data-ttu-id="2aeec-126">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="2aeec-126">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [<span data-ttu-id="2aeec-127">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="2aeec-127">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [<span data-ttu-id="2aeec-128">Fedora Remix for WSL</span><span class="sxs-lookup"><span data-stu-id="2aeec-128">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [<span data-ttu-id="2aeec-129">Pengwin</span><span class="sxs-lookup"><span data-stu-id="2aeec-129">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [<span data-ttu-id="2aeec-130">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="2aeec-130">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [<span data-ttu-id="2aeec-131">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="2aeec-131">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

1. <span data-ttu-id="2aeec-132">На странице дистрибутива щелкните "Получить".</span><span class="sxs-lookup"><span data-stu-id="2aeec-132">From the distro's page, select "Get"</span></span>

    ![Представление дистрибутивов Linux в Microsoft Store](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="2aeec-134">Завершение инициализации дистрибутива</span><span class="sxs-lookup"><span data-stu-id="2aeec-134">Complete initialization of your distro</span></span>
<span data-ttu-id="2aeec-135">После установки дистрибутива Linux необходимо [единоразово инициализировать новый экземпляр дистрибутива](initialize-distro.md), прежде чем его можно будет использовать.</span><span class="sxs-lookup"><span data-stu-id="2aeec-135">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) once, before it can be used.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="2aeec-136">Устранение неполадок:</span><span class="sxs-lookup"><span data-stu-id="2aeec-136">Troubleshooting:</span></span> 

<span data-ttu-id="2aeec-137">Ниже перечислены возможные ошибки и способы их устранения.</span><span class="sxs-lookup"><span data-stu-id="2aeec-137">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="2aeec-138">Другие распространенные ошибки и способы их устранения приведены в разделе [Устранение неполадок подсистемы Windows для Linux](troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="2aeec-138">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

* <span data-ttu-id="2aeec-139">**Сбой установки с ошибкой 0x80070003**</span><span class="sxs-lookup"><span data-stu-id="2aeec-139">**Installation failed with error 0x80070003**</span></span>
    * <span data-ttu-id="2aeec-140">Подсистема Windows для Linux работает только на системном диске (обычно это диск `C:`).</span><span class="sxs-lookup"><span data-stu-id="2aeec-140">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="2aeec-141">Убедитесь, что дистрибутивы хранятся на системном диске.</span><span class="sxs-lookup"><span data-stu-id="2aeec-141">Make sure that distros are stored on your system drive:</span></span>  
    * <span data-ttu-id="2aeec-142">Выберите **Параметры** -> **Хранилище** -> **More Storage Settings: (Другие параметры хранилища:) Изменить место сохранения нового содержимого**.
    ![Изображение параметров системы для установки приложений на диске C:](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="2aeec-142">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>
    
    
 * <span data-ttu-id="2aeec-143">**Сбой WslRegisterDistribution с ошибкой 0x8007019e**</span><span class="sxs-lookup"><span data-stu-id="2aeec-143">**WslRegisterDistribution failed with error 0x8007019e**</span></span>   
  * <span data-ttu-id="2aeec-144">Дополнительный компонент "Подсистема Windows для Linux" не включен.</span><span class="sxs-lookup"><span data-stu-id="2aeec-144">The Windows Subsystem for Linux optional component is not enabled:</span></span> 
   * <span data-ttu-id="2aeec-145">Выберите **Панель управления** -> **Программы и компоненты** -> **Включение или отключение компонентов Windows** и установите флажок **Подсистема Windows для Linux** или используйте командлет PowerShell, упомянутый в начале этой статьи.</span><span class="sxs-lookup"><span data-stu-id="2aeec-145">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>
