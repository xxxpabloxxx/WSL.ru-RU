---
title: Установите подсистему Linux в Windows Server
description: Инструкции по установке для подсистемы Linux на Windows Server.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, windows server
author: scooley
ms.author: scooley
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: c0b8af08a06428ebd292b8c6b9b275726988bdbe
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063622"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="ab402-104">Руководство по установке Windows Server</span><span class="sxs-lookup"><span data-stu-id="ab402-104">Windows Server Installation Guide</span></span>

> <span data-ttu-id="ab402-105">Применяется к Windows Server 2019 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="ab402-105">Applies to Windows Server 2019 and later</span></span>

<span data-ttu-id="ab402-106">В / / Build2017, корпорация Microsoft объявила, что подсистема Windows для Linux будет [доступный в Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span><span class="sxs-lookup"><span data-stu-id="ab402-106">At //Build2017, Microsoft announced that Windows Subsystem for Linux will be [available on Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span></span>  <span data-ttu-id="ab402-107">Эти инструкции показано, как запуск подсистемы Windows для Linux на Windows Server 1709 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="ab402-107">These instructions walk through running the Windows Subsystem for Linux on Windows Server 1709 and later.</span></span>

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="ab402-108">Включение подсистемы Windows для Linux (WSL)</span><span class="sxs-lookup"><span data-stu-id="ab402-108">Enable the Windows Subsystem for Linux (WSL)</span></span>

<span data-ttu-id="ab402-109">Перед запуском дистрибутивов Linux на Windows, необходимо включить дополнительный компонент «Windows подсистемы для Linux» и перезагрузите.</span><span class="sxs-lookup"><span data-stu-id="ab402-109">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

1. <span data-ttu-id="ab402-110">Откройте PowerShell от имени администратора и выполните:</span><span class="sxs-lookup"><span data-stu-id="ab402-110">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="ab402-111">Перезагрузите компьютер при появлении запроса.</span><span class="sxs-lookup"><span data-stu-id="ab402-111">Restart your computer when prompted.</span></span> <span data-ttu-id="ab402-112">**Требуется перезагрузка, этот** чтобы гарантировать, что WSL может инициировать резервной доверенной среде выполнения.</span><span class="sxs-lookup"><span data-stu-id="ab402-112">**This reboot is required** in order to ensure that WSL can initiate a trusted execution environment.</span></span>

## <a name="download-a-linux-distro"></a><span data-ttu-id="ab402-113">Скачать дистрибутив Linux</span><span class="sxs-lookup"><span data-stu-id="ab402-113">Download a Linux distro</span></span>

<span data-ttu-id="ab402-114">Выполните [эти инструкции](install-manual.md) загрузить избранные дистрибутива Linux.</span><span class="sxs-lookup"><span data-stu-id="ab402-114">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distro"></a><span data-ttu-id="ab402-115">Распаковать и установить дистрибутив Linux</span><span class="sxs-lookup"><span data-stu-id="ab402-115">Extract and install a Linux distro</span></span>
<span data-ttu-id="ab402-116">Теперь, когда вы скачали дистрибутив, извлеките его содержимое и вручную установите дистрибутива:</span><span class="sxs-lookup"><span data-stu-id="ab402-116">Now that you've downloaded a distro, extract its contents and manually install the distro:</span></span>

1. <span data-ttu-id="ab402-117">Извлеките `<distro>.appx` содержимое пакета, например с помощью PowerShell:</span><span class="sxs-lookup"><span data-stu-id="ab402-117">Extract the `<distro>.appx` package's contents, e.g. using PowerShell:</span></span>

    ```powershell
    Rename-Item ~/Ubuntu.appx ~/Ubuntu.zip
    Expand-Archive ~/Ubuntu.zip ~/Ubuntu
    ```

2. <span data-ttu-id="ab402-118">Запустите средство запуска дистрибутива для завершения установки, запустите приложение запуска дистрибутива в целевой папке с именем `<distro>.exe`.</span><span class="sxs-lookup"><span data-stu-id="ab402-118">Run the distro launcher To complete installation, run the distro launcher application in the target folder, named `<distro>.exe`.</span></span> <span data-ttu-id="ab402-119">Например: `ubuntu.exe`и т. д.</span><span class="sxs-lookup"><span data-stu-id="ab402-119">For example: `ubuntu.exe`, etc.</span></span>

    ![Расширенный дистрибутив Ubuntu в Windows Server](media/server-appx-expand.png)

    > **<span data-ttu-id="ab402-121">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="ab402-121">Troubleshooting</span></span>**
    > * <span data-ttu-id="ab402-122">**Установка завершилась ошибкой 0x8007007e**: Эта ошибка возникает, когда ваша система не поддерживает WSL.</span><span class="sxs-lookup"><span data-stu-id="ab402-122">**Installation failed with error 0x8007007e**: This error occurs when your system doesn't support WSL.</span></span> <span data-ttu-id="ab402-123">Убедитесь в следующем.</span><span class="sxs-lookup"><span data-stu-id="ab402-123">Make sure that:</span></span>
    >   * <span data-ttu-id="ab402-124">Вы используете Windows сборки 16215 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ab402-124">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="ab402-125">[Проверьте сборку](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="ab402-125">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
    >   * <span data-ttu-id="ab402-126">Подсистема Windows для Linux дополнительный компонент включен и перезагрузки компьютера.</span><span class="sxs-lookup"><span data-stu-id="ab402-126">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="ab402-127">[Убедитесь, что включен WSL](troubleshooting.md#confirm-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="ab402-127">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
    
3. <span data-ttu-id="ab402-128">Добавить путь к дистрибутива в среде Windows путь (`C:\Users\Administrator\Ubuntu` в этом примере), например, с помощью Powershell:</span><span class="sxs-lookup"><span data-stu-id="ab402-128">Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), e.g. using Powershell:</span></span>
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + "C:\Users\Administrator\Ubuntu", "User")
    ```
    <span data-ttu-id="ab402-129">Теперь вы можете запускать вашего дистрибутива из любой путь, введя `<distro>.exe`.</span><span class="sxs-lookup"><span data-stu-id="ab402-129">You can now launch your distro from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="ab402-130">Пример:</span><span class="sxs-lookup"><span data-stu-id="ab402-130">For example:</span></span> `ubuntu.exe`

<span data-ttu-id="ab402-131">Теперь, когда устанавливается дистрибутив Linux, необходимо [инициализации в новом экземпляре дистрибутива](initialize-distro.md) перед использованием вашего дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="ab402-131">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) before using your distro.</span></span>
