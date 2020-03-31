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
# <a name="windows-server-installation-guide"></a>Руководство по установке Windows Server

> Область применения: Windows Server 2019 и более поздних версий

Корпорация Майкрософт объявила, что в сборке 2017 г. подсистема Windows для Linux будет [доступна в Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).  В этих инструкциях рассматривается запуск подсистемы Windows для Linux на Windows Server 1709 и более поздних версий.

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a>Включение подсистемы Windows для Linux (WSL)

Перед запуском дистрибутивов Linux в Windows необходимо включить дополнительный компонент "Подсистема Windows для Linux" и перезагрузить компьютер.

1. Запустите PowerShell с правами администратора и выполните следующую команду.
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. При появлении соответствующего запроса перезагрузите компьютер. **Эта перезагрузка необходима**, чтобы гарантировать, что WSL может инициировать доверенную среду выполнения.

## <a name="download-a-linux-distro"></a>Скачивание дистрибутива Linux

Выполните [эти инструкции](install-manual.md), чтобы скачать избранный дистрибутив Linux.

## <a name="extract-and-install-a-linux-distro"></a>Извлечение и установка дистрибутива Linux
Теперь, когда вы загрузили дистрибутив, извлеките его содержимое и установите его вручную:

1. Извлеките содержимое пакета `<distro>.appx`, например, с помощью PowerShell:

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. Запустите средство запуска дистрибутива. Чтобы завершить установку, запустите приложение средства запуска дистрибутива в целевой папке `<distro>.exe`. Например: `ubuntu.exe` и т. д.

    ![Расширенный дистрибутив Ubuntu в Windows Server](media/server-appx-expand.png)

    > **Устранение неполадок**
    > * **Сбой установки с ошибкой 0x8007007e**. Эта ошибка возникает, если система не поддерживает WSL. Убедитесь в следующем.
    >   * Вы используете сборку Windows 16215 или более позднюю версию. [Проверьте используемую сборку](troubleshooting.md#check-your-build-number).
    >   * Дополнительный компонент "Подсистема Windows для Linux" включен, а компьютер был перезагружен.  [Убедитесь, что WSL включен](troubleshooting.md#confirm-wsl-is-enabled).
    
3. Добавьте путь дистрибутива в путь среды Windows (в этом примере: `C:\Users\Administrator\Ubuntu`), например, с помощью PowerShell:
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    Теперь вы можете запустить дистрибутив из любого пути, введя `<distro>.exe`. Пример: `ubuntu.exe`

После установки дистрибутива Linux необходимо [инициализировать новый экземпляр дистрибутива](initialize-distro.md), прежде чем его можно будет использовать.
