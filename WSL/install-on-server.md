---
title: Установка подсистемы Linux в Windows Server
description: Инструкции по установке для подсистемы Linux в Windows Server.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, windows server
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 86fd7de0ef45af760f46bb2a18932f513b813609
ms.sourcegitcommit: 1b6191351bbf9e95f3c28fc67abe4bf1bcfd3336
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/13/2020
ms.locfileid: "83270888"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="3fc39-104">Руководство по установке Windows Server</span><span class="sxs-lookup"><span data-stu-id="3fc39-104">Windows Server Installation Guide</span></span>

<span data-ttu-id="3fc39-105">Подсистема Windows для Linux доступна для установки на Windows Server 2019 (версия 1709) и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="3fc39-105">The Windows Subsystem for Linux is available for installation on Windows Server 2019 (version 1709) and later.</span></span> <span data-ttu-id="3fc39-106">В этом руководстве рассматриваются действия по включению WSL на компьютере.</span><span class="sxs-lookup"><span data-stu-id="3fc39-106">This guide will walk through the steps of enabling WSL on your machine.</span></span>

## <a name="enable-the-windows-subsystem-for-linux"></a><span data-ttu-id="3fc39-107">Включение подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="3fc39-107">Enable the Windows Subsystem for Linux</span></span>

<span data-ttu-id="3fc39-108">Перед запуском дистрибутивов Linux в Windows необходимо включить дополнительный компонент "Подсистема Windows для Linux" и перезагрузить компьютер.</span><span class="sxs-lookup"><span data-stu-id="3fc39-108">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

<span data-ttu-id="3fc39-109">Запустите PowerShell с правами администратора и выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="3fc39-109">Open PowerShell as Administrator and run:</span></span>

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

```

<span data-ttu-id="3fc39-110">**Если вам нужна 100 % совместимость с системными вызовами и более быстрая производительность ввода-вывода, ознакомьтесь со сведениями ниже, чтобы установить WSL 2!**</span><span class="sxs-lookup"><span data-stu-id="3fc39-110">**If you're looking for 100% system call compatibility and faster IO performance, read below to install WSL 2!**</span></span>

<span data-ttu-id="3fc39-111">Подсистема WSL 2 доступна только в Windows 10 версии 2004, сборки 19041 или выше.</span><span class="sxs-lookup"><span data-stu-id="3fc39-111">WSL 2 is only available in Windows 10, Version 2004, Build 19041 or higher.</span></span> <span data-ttu-id="3fc39-112">Вам потребуется [обновить версию Windows](ms-settings:windowsupdate), а также [присоединиться к Программе предварительной оценки Windows](https://insider.windows.com/insidersigninboth/) и выбрать круг Release Preview, пока в мае не выйдет общедоступный выпуск.</span><span class="sxs-lookup"><span data-stu-id="3fc39-112">You will need to [update your Windows version](ms-settings:windowsupdate) and [join the Windows Insider program](https://insider.windows.com/insidersigninboth/) on the "Release Preview" ring until the public release in late May.</span></span>

<span data-ttu-id="3fc39-113">**В случае продолжения работы с WSL 1 перезагрузите компьютер, когда появится соответствующее сообщение, и продолжите установку [здесь](./install-on-server.md#download-a-linux-distribution)** .</span><span class="sxs-lookup"><span data-stu-id="3fc39-113">**If continuing with WSL 1, restart your machine when prompted and continue with installation [here](./install-on-server.md#download-a-linux-distribution)**</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="3fc39-114">Включение необязательного компонента "Virtual Machine Platform" (Платформа виртуальной машины)</span><span class="sxs-lookup"><span data-stu-id="3fc39-114">Enable the Virtual Machine Platform optional component</span></span>

<span data-ttu-id="3fc39-115">Убедитесь, что установлен дополнительный компонент "Virtual Machine Platform" (Платформа виртуальных машин).</span><span class="sxs-lookup"><span data-stu-id="3fc39-115">Ensure the 'Virtual Machine Platform' optional component is installed.</span></span> <span data-ttu-id="3fc39-116">Это можно сделать, выполнив следующую команду в PowerShell:</span><span class="sxs-lookup"><span data-stu-id="3fc39-116">You can do that by running the following command in PowerShell:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

## <a name="download-a-linux-distribution"></a><span data-ttu-id="3fc39-117">Скачивание дистрибутива Linux</span><span class="sxs-lookup"><span data-stu-id="3fc39-117">Download a Linux distribution</span></span>

<span data-ttu-id="3fc39-118">Выполните [эти инструкции](install-manual.md), чтобы скачать избранный дистрибутив Linux.</span><span class="sxs-lookup"><span data-stu-id="3fc39-118">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distribution"></a><span data-ttu-id="3fc39-119">Извлечение и установка дистрибутива Linux</span><span class="sxs-lookup"><span data-stu-id="3fc39-119">Extract and install a Linux distribution</span></span>

<span data-ttu-id="3fc39-120">После загрузки дистрибутива Linux для извлечения его содержимого и установки вручную выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3fc39-120">Now that you've downloaded a Linux distribution, in order to extract its contents and manually install, follow these steps:</span></span>

1. <span data-ttu-id="3fc39-121">Извлеките содержимое пакета `<distro>.appx`, с помощью PowerShell:</span><span class="sxs-lookup"><span data-stu-id="3fc39-121">Extract the `<distro>.appx` package's contents, using PowerShell:</span></span>

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. <span data-ttu-id="3fc39-122">Запустите средство запуска приложения дистрибутива в целевой папке.</span><span class="sxs-lookup"><span data-stu-id="3fc39-122">Run the distribution launcher application in the target folder.</span></span> <span data-ttu-id="3fc39-123">Средство запуска обычно называется `<distro>.exe` (например, `ubuntu.exe`).</span><span class="sxs-lookup"><span data-stu-id="3fc39-123">The launcher is typically named `<distro>.exe` (for example, `ubuntu.exe`).</span></span>

    ![Расширенный дистрибутив Ubuntu в Windows Server](media/server-appx-expand.png)

> [!CAUTION]
> <span data-ttu-id="3fc39-125">**Сбой установки с ошибкой 0x8007007e**. При возникновении этой ошибки система не поддерживает WSL.</span><span class="sxs-lookup"><span data-stu-id="3fc39-125">**Installation failed with error 0x8007007e**: If you receive this error, then your system doesn't support WSL.</span></span> <span data-ttu-id="3fc39-126">Убедитесь, что вы используете сборку Windows 16215 или более позднюю версию.</span><span class="sxs-lookup"><span data-stu-id="3fc39-126">Ensure that you're running Windows build 16215 or later.</span></span> <span data-ttu-id="3fc39-127">[Проверьте используемую сборку](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="3fc39-127">[Check your build](troubleshooting.md#check-your-build-number).</span></span> <span data-ttu-id="3fc39-128">Также убедитесь, [что WSL включен](troubleshooting.md#confirm-wsl-is-enabled) и ваш компьютер перезагружен после включения этой функции.</span><span class="sxs-lookup"><span data-stu-id="3fc39-128">Also check to [confirm that WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled) and your computer was restarted after the feature was enabled.</span></span>  

<span data-ttu-id="3fc39-129">3. Добавьте путь дистрибутива в путь среды Windows (в этом примере: `C:\Users\Administrator\Ubuntu`), с помощью PowerShell:</span><span class="sxs-lookup"><span data-stu-id="3fc39-129">3.Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), using PowerShell:</span></span>

```powershell
$userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
[System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
```

<span data-ttu-id="3fc39-130">Теперь вы можете запустить дистрибутив из любого пути, введя `<distro>.exe`.</span><span class="sxs-lookup"><span data-stu-id="3fc39-130">You can now launch your distribution from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="3fc39-131">Например: `ubuntu.exe`.</span><span class="sxs-lookup"><span data-stu-id="3fc39-131">For example: `ubuntu.exe`.</span></span>

<span data-ttu-id="3fc39-132">После установки необходимо [инициализировать новый экземпляр дистрибутива](initialize-distro.md), прежде чем его можно будет использовать.</span><span class="sxs-lookup"><span data-stu-id="3fc39-132">Now that it is installed, you must [initialize your new distribution instance](initialize-distro.md) before using it.</span></span>
