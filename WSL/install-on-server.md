---
title: Установка подсистемы Linux в Windows Server
description: Инструкции по установке для подсистемы Linux на Windows Server.
keywords: Башонвиндовс, bash, WSL, Windows, подсистема Windows для Linux, виндовссубсистем, Ubuntu, Windows Server
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: 51a2e3f3443ed9b1ba3d8ab79977f22839ee0283
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269784"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="a556f-104">Руководства по установке Windows Server</span><span class="sxs-lookup"><span data-stu-id="a556f-104">Windows Server Installation Guide</span></span>

> <span data-ttu-id="a556f-105">Применимо к Windows Server 2019 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="a556f-105">Applies to Windows Server 2019 and later</span></span>

<span data-ttu-id="a556f-106">В//Build2017 Корпорация Майкрософт объявила, что подсистема Windows для Linux будет [доступна в Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span><span class="sxs-lookup"><span data-stu-id="a556f-106">At //Build2017, Microsoft announced that Windows Subsystem for Linux will be [available on Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span></span>  <span data-ttu-id="a556f-107">В этих инструкциях рассматривается запуск подсистемы Windows для Linux на Windows Server 1709 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="a556f-107">These instructions walk through running the Windows Subsystem for Linux on Windows Server 1709 and later.</span></span>

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="a556f-108">Включение подсистемы Windows для Linux (WSL)</span><span class="sxs-lookup"><span data-stu-id="a556f-108">Enable the Windows Subsystem for Linux (WSL)</span></span>

<span data-ttu-id="a556f-109">Перед запуском Linux дистрибутивов в Windows необходимо включить дополнительный компонент "подсистема Windows для Linux" и перезагрузить компьютер.</span><span class="sxs-lookup"><span data-stu-id="a556f-109">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

1. <span data-ttu-id="a556f-110">Откройте PowerShell от имени администратора и выполните команду:</span><span class="sxs-lookup"><span data-stu-id="a556f-110">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="a556f-111">При появлении запроса перезагрузите компьютер.</span><span class="sxs-lookup"><span data-stu-id="a556f-111">Restart your computer when prompted.</span></span> <span data-ttu-id="a556f-112">**Эта перезагрузка необходима** для того, чтобы WSL мог инициировать доверенную среду выполнения.</span><span class="sxs-lookup"><span data-stu-id="a556f-112">**This reboot is required** in order to ensure that WSL can initiate a trusted execution environment.</span></span>

## <a name="download-a-linux-distro"></a><span data-ttu-id="a556f-113">Загрузка дистрибутив Linux</span><span class="sxs-lookup"><span data-stu-id="a556f-113">Download a Linux distro</span></span>

<span data-ttu-id="a556f-114">Для загрузки избранного дистрибутива Linux выполните следующие [инструкции](install-manual.md) .</span><span class="sxs-lookup"><span data-stu-id="a556f-114">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distro"></a><span data-ttu-id="a556f-115">Извлечение и установка дистрибутив Linux</span><span class="sxs-lookup"><span data-stu-id="a556f-115">Extract and install a Linux distro</span></span>
<span data-ttu-id="a556f-116">Теперь, когда вы загрузили дистрибутив, извлеките его содержимое и вручную установите дистрибутив:</span><span class="sxs-lookup"><span data-stu-id="a556f-116">Now that you've downloaded a distro, extract its contents and manually install the distro:</span></span>

1. <span data-ttu-id="a556f-117">Извлеките `<distro>.appx` содержимое пакета, например с помощью PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a556f-117">Extract the `<distro>.appx` package's contents, e.g. using PowerShell:</span></span>

    ```powershell
    Rename-Item ./Ubuntu.appx ./Ubuntu.zip
    Expand-Archive ./Ubuntu.zip ./Ubuntu
    ```

2. <span data-ttu-id="a556f-118">Запустите средство запуска дистрибутив для завершения установки, запустите приложение запуска дистрибутив в целевой папке с именем `<distro>.exe`.</span><span class="sxs-lookup"><span data-stu-id="a556f-118">Run the distro launcher To complete installation, run the distro launcher application in the target folder, named `<distro>.exe`.</span></span> <span data-ttu-id="a556f-119">Например: `ubuntu.exe`и т. д.</span><span class="sxs-lookup"><span data-stu-id="a556f-119">For example: `ubuntu.exe`, etc.</span></span>

    ![Расширенная дистрибутив Ubuntu в Windows Server](media/server-appx-expand.png)

    > <span data-ttu-id="a556f-121">**Устранение неполадок**</span><span class="sxs-lookup"><span data-stu-id="a556f-121">**Troubleshooting**</span></span>
    > * <span data-ttu-id="a556f-122">**Сбой установки с ошибкой 0x8007007e**: Эта ошибка возникает, когда система не поддерживает WSL.</span><span class="sxs-lookup"><span data-stu-id="a556f-122">**Installation failed with error 0x8007007e**: This error occurs when your system doesn't support WSL.</span></span> <span data-ttu-id="a556f-123">Убедитесь в следующем.</span><span class="sxs-lookup"><span data-stu-id="a556f-123">Make sure that:</span></span>
    >   * <span data-ttu-id="a556f-124">Вы используете Windows Build 16215 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a556f-124">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="a556f-125">[Проверьте сборку](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="a556f-125">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
    >   * <span data-ttu-id="a556f-126">Дополнительный компонент подсистемы Windows для Linux включен и компьютер перезагружен.</span><span class="sxs-lookup"><span data-stu-id="a556f-126">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="a556f-127">[Убедитесь, что WSL включен](troubleshooting.md#confirm-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="a556f-127">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
    
3. <span data-ttu-id="a556f-128">Добавьте путь дистрибутив в путь среды Windows (`C:\Users\Administrator\Ubuntu` в этом примере это), например с помощью PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a556f-128">Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), e.g. using Powershell:</span></span>
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    <span data-ttu-id="a556f-129">Теперь можно запустить дистрибутив из любого пути, введя `<distro>.exe`.</span><span class="sxs-lookup"><span data-stu-id="a556f-129">You can now launch your distro from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="a556f-130">Пример: `ubuntu.exe`</span><span class="sxs-lookup"><span data-stu-id="a556f-130">For example: `ubuntu.exe`</span></span>

<span data-ttu-id="a556f-131">После установки дистрибутив для Linux необходимо [инициализировать новый экземпляр дистрибутив](initialize-distro.md) перед использованием дистрибутив.</span><span class="sxs-lookup"><span data-stu-id="a556f-131">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) before using your distro.</span></span>
