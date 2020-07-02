---
title: Установка подсистемы Linux в Windows Server
description: Инструкции по установке для подсистемы Linux в Windows Server.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, windows server
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: ebcd7f6b10d2b734b1f2a66f64a5e3292855bcf4
ms.sourcegitcommit: 5d3898772851e6ac9a310f219cc0d71278f95d22
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2020
ms.locfileid: "84671024"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="afc84-104">Руководство по установке Windows Server</span><span class="sxs-lookup"><span data-stu-id="afc84-104">Windows Server Installation Guide</span></span>

<span data-ttu-id="afc84-105">Подсистема Windows для Linux доступна для установки на Windows Server 2019 (версия 1709) и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="afc84-105">The Windows Subsystem for Linux is available for installation on Windows Server 2019 (version 1709) and later.</span></span> <span data-ttu-id="afc84-106">В этом руководстве рассматриваются действия по включению WSL на компьютере.</span><span class="sxs-lookup"><span data-stu-id="afc84-106">This guide will walk through the steps of enabling WSL on your machine.</span></span>

## <a name="enable-the-windows-subsystem-for-linux"></a><span data-ttu-id="afc84-107">Включение подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="afc84-107">Enable the Windows Subsystem for Linux</span></span>

<span data-ttu-id="afc84-108">Перед запуском дистрибутивов Linux в Windows необходимо включить дополнительный компонент "Подсистема Windows для Linux" и перезагрузить компьютер.</span><span class="sxs-lookup"><span data-stu-id="afc84-108">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

<span data-ttu-id="afc84-109">Запустите PowerShell с правами администратора и выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="afc84-109">Open PowerShell as Administrator and run:</span></span>

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

```

## <a name="download-a-linux-distribution"></a><span data-ttu-id="afc84-110">Скачивание дистрибутива Linux</span><span class="sxs-lookup"><span data-stu-id="afc84-110">Download a Linux distribution</span></span>

<span data-ttu-id="afc84-111">Выполните [эти инструкции](install-manual.md), чтобы скачать избранный дистрибутив Linux.</span><span class="sxs-lookup"><span data-stu-id="afc84-111">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distribution"></a><span data-ttu-id="afc84-112">Извлечение и установка дистрибутива Linux</span><span class="sxs-lookup"><span data-stu-id="afc84-112">Extract and install a Linux distribution</span></span>

<span data-ttu-id="afc84-113">После загрузки дистрибутива Linux для извлечения его содержимого и установки вручную выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="afc84-113">Now that you've downloaded a Linux distribution, in order to extract its contents and manually install, follow these steps:</span></span>

1. <span data-ttu-id="afc84-114">Извлеките содержимое пакета `<distro>.appx`, с помощью PowerShell:</span><span class="sxs-lookup"><span data-stu-id="afc84-114">Extract the `<distro>.appx` package's contents, using PowerShell:</span></span>

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. <span data-ttu-id="afc84-115">Запустите средство запуска приложения дистрибутива в целевой папке.</span><span class="sxs-lookup"><span data-stu-id="afc84-115">Run the distribution launcher application in the target folder.</span></span> <span data-ttu-id="afc84-116">Средство запуска обычно называется `<distro>.exe` (например, `ubuntu.exe`).</span><span class="sxs-lookup"><span data-stu-id="afc84-116">The launcher is typically named `<distro>.exe` (for example, `ubuntu.exe`).</span></span>

    ![Расширенный дистрибутив Ubuntu в Windows Server](media/server-appx-expand.png)

> [!CAUTION]
> <span data-ttu-id="afc84-118">**Сбой установки с ошибкой 0x8007007e**. При возникновении этой ошибки система не поддерживает WSL.</span><span class="sxs-lookup"><span data-stu-id="afc84-118">**Installation failed with error 0x8007007e**: If you receive this error, then your system doesn't support WSL.</span></span> <span data-ttu-id="afc84-119">Убедитесь, что вы используете сборку Windows 16215 или более позднюю версию.</span><span class="sxs-lookup"><span data-stu-id="afc84-119">Ensure that you're running Windows build 16215 or later.</span></span> <span data-ttu-id="afc84-120">[Проверьте используемую сборку](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="afc84-120">[Check your build](troubleshooting.md#check-your-build-number).</span></span> <span data-ttu-id="afc84-121">Также убедитесь, [что WSL включен](troubleshooting.md#confirm-wsl-is-enabled) и ваш компьютер перезагружен после включения этой функции.</span><span class="sxs-lookup"><span data-stu-id="afc84-121">Also check to [confirm that WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled) and your computer was restarted after the feature was enabled.</span></span>  

<span data-ttu-id="afc84-122">3. Добавьте путь дистрибутива в путь среды Windows (в этом примере: `C:\Users\Administrator\Ubuntu`), с помощью PowerShell:</span><span class="sxs-lookup"><span data-stu-id="afc84-122">3.Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), using PowerShell:</span></span>

```powershell
$userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
[System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
```

<span data-ttu-id="afc84-123">Теперь вы можете запустить дистрибутив из любого пути, введя `<distro>.exe`.</span><span class="sxs-lookup"><span data-stu-id="afc84-123">You can now launch your distribution from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="afc84-124">Например: `ubuntu.exe`.</span><span class="sxs-lookup"><span data-stu-id="afc84-124">For example: `ubuntu.exe`.</span></span>

<span data-ttu-id="afc84-125">После установки необходимо [инициализировать новый экземпляр дистрибутива](initialize-distro.md), прежде чем его можно будет использовать.</span><span class="sxs-lookup"><span data-stu-id="afc84-125">Now that it is installed, you must [initialize your new distribution instance](initialize-distro.md) before using it.</span></span>
