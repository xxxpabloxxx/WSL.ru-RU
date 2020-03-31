---
title: Установка подсистемы Linux в Windows Server
description: Инструкции по установке для подсистемы Linux в Windows Server.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, windows server
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 8859929fe45c9989d367af5f82191162963e6b4f
ms.sourcegitcommit: 0a001ada2131f80dd77b114fc14f2fde43c947ad
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/25/2020
ms.locfileid: "80256397"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="89f67-104">Руководство по установке Windows Server</span><span class="sxs-lookup"><span data-stu-id="89f67-104">Windows Server Installation Guide</span></span>

> <span data-ttu-id="89f67-105">Область применения: Windows Server 2019 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="89f67-105">Applies to Windows Server 2019 and later</span></span>

<span data-ttu-id="89f67-106">Корпорация Майкрософт объявила, что в сборке 2017 г. подсистема Windows для Linux будет [доступна в Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span><span class="sxs-lookup"><span data-stu-id="89f67-106">At //Build2017, Microsoft announced that Windows Subsystem for Linux will be [available on Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span></span>  <span data-ttu-id="89f67-107">В этих инструкциях рассматривается запуск подсистемы Windows для Linux на Windows Server 1709 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="89f67-107">These instructions walk through running the Windows Subsystem for Linux on Windows Server 1709 and later.</span></span>

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="89f67-108">Включение подсистемы Windows для Linux (WSL)</span><span class="sxs-lookup"><span data-stu-id="89f67-108">Enable the Windows Subsystem for Linux (WSL)</span></span>

<span data-ttu-id="89f67-109">Перед запуском дистрибутивов Linux в Windows необходимо включить дополнительный компонент "Подсистема Windows для Linux" и перезагрузить компьютер.</span><span class="sxs-lookup"><span data-stu-id="89f67-109">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

1. <span data-ttu-id="89f67-110">Запустите PowerShell с правами администратора и выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="89f67-110">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="89f67-111">При появлении соответствующего запроса перезагрузите компьютер.</span><span class="sxs-lookup"><span data-stu-id="89f67-111">Restart your computer when prompted.</span></span> <span data-ttu-id="89f67-112">**Эта перезагрузка необходима**, чтобы гарантировать, что WSL может инициировать доверенную среду выполнения.</span><span class="sxs-lookup"><span data-stu-id="89f67-112">**This reboot is required** in order to ensure that WSL can initiate a trusted execution environment.</span></span>

## <a name="download-a-linux-distro"></a><span data-ttu-id="89f67-113">Скачивание дистрибутива Linux</span><span class="sxs-lookup"><span data-stu-id="89f67-113">Download a Linux distro</span></span>

<span data-ttu-id="89f67-114">Выполните [эти инструкции](install-manual.md), чтобы скачать избранный дистрибутив Linux.</span><span class="sxs-lookup"><span data-stu-id="89f67-114">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distro"></a><span data-ttu-id="89f67-115">Извлечение и установка дистрибутива Linux</span><span class="sxs-lookup"><span data-stu-id="89f67-115">Extract and install a Linux distro</span></span>
<span data-ttu-id="89f67-116">Теперь, когда вы загрузили дистрибутив, извлеките его содержимое и установите его вручную:</span><span class="sxs-lookup"><span data-stu-id="89f67-116">Now that you've downloaded a distro, extract its contents and manually install the distro:</span></span>

1. <span data-ttu-id="89f67-117">Извлеките содержимое пакета `<distro>.appx`, например, с помощью PowerShell:</span><span class="sxs-lookup"><span data-stu-id="89f67-117">Extract the `<distro>.appx` package's contents, e.g. using PowerShell:</span></span>

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. <span data-ttu-id="89f67-118">Запустите средство запуска дистрибутива. Чтобы завершить установку, запустите приложение средства запуска дистрибутива в целевой папке `<distro>.exe`.</span><span class="sxs-lookup"><span data-stu-id="89f67-118">Run the distro launcher To complete installation, run the distro launcher application in the target folder, named `<distro>.exe`.</span></span> <span data-ttu-id="89f67-119">Например: `ubuntu.exe` и т. д.</span><span class="sxs-lookup"><span data-stu-id="89f67-119">For example: `ubuntu.exe`, etc.</span></span>

    ![Расширенный дистрибутив Ubuntu в Windows Server](media/server-appx-expand.png)

    > <span data-ttu-id="89f67-121">**Устранение неполадок**</span><span class="sxs-lookup"><span data-stu-id="89f67-121">**Troubleshooting**</span></span>
    > * <span data-ttu-id="89f67-122">**Сбой установки с ошибкой 0x8007007e**. Эта ошибка возникает, если система не поддерживает WSL.</span><span class="sxs-lookup"><span data-stu-id="89f67-122">**Installation failed with error 0x8007007e**: This error occurs when your system doesn't support WSL.</span></span> <span data-ttu-id="89f67-123">Убедитесь в следующем.</span><span class="sxs-lookup"><span data-stu-id="89f67-123">Make sure that:</span></span>
    >   * <span data-ttu-id="89f67-124">Вы используете сборку Windows 16215 или более позднюю версию.</span><span class="sxs-lookup"><span data-stu-id="89f67-124">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="89f67-125">[Проверьте используемую сборку](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="89f67-125">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
    >   * <span data-ttu-id="89f67-126">Дополнительный компонент "Подсистема Windows для Linux" включен, а компьютер был перезагружен.</span><span class="sxs-lookup"><span data-stu-id="89f67-126">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="89f67-127">[Убедитесь, что WSL включен](troubleshooting.md#confirm-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="89f67-127">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
    
3. <span data-ttu-id="89f67-128">Добавьте путь дистрибутива в путь среды Windows (в этом примере: `C:\Users\Administrator\Ubuntu`), например, с помощью PowerShell:</span><span class="sxs-lookup"><span data-stu-id="89f67-128">Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), e.g. using Powershell:</span></span>
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    <span data-ttu-id="89f67-129">Теперь вы можете запустить дистрибутив из любого пути, введя `<distro>.exe`.</span><span class="sxs-lookup"><span data-stu-id="89f67-129">You can now launch your distro from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="89f67-130">Пример: `ubuntu.exe`</span><span class="sxs-lookup"><span data-stu-id="89f67-130">For example: `ubuntu.exe`</span></span>

<span data-ttu-id="89f67-131">После установки дистрибутива Linux необходимо [инициализировать новый экземпляр дистрибутива](initialize-distro.md), прежде чем его можно будет использовать.</span><span class="sxs-lookup"><span data-stu-id="89f67-131">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) before using your distro.</span></span>
