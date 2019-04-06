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
# <a name="windows-server-installation-guide"></a>Руководство по установке Windows Server

> Применяется к Windows Server 2019 и более поздних версий

В / / Build2017, корпорация Microsoft объявила, что подсистема Windows для Linux будет [доступный в Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).  Эти инструкции показано, как запуск подсистемы Windows для Linux на Windows Server 1709 и более поздних версий.

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a>Включение подсистемы Windows для Linux (WSL)

Перед запуском дистрибутивов Linux на Windows, необходимо включить дополнительный компонент «Windows подсистемы для Linux» и перезагрузите.

1. Откройте PowerShell от имени администратора и выполните:
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. Перезагрузите компьютер при появлении запроса. **Требуется перезагрузка, этот** чтобы гарантировать, что WSL может инициировать резервной доверенной среде выполнения.

## <a name="download-a-linux-distro"></a>Скачать дистрибутив Linux

Выполните [эти инструкции](install-manual.md) загрузить избранные дистрибутива Linux.

## <a name="extract-and-install-a-linux-distro"></a>Распаковать и установить дистрибутив Linux
Теперь, когда вы скачали дистрибутив, извлеките его содержимое и вручную установите дистрибутива:

1. Извлеките `<distro>.appx` содержимое пакета, например с помощью PowerShell:

    ```powershell
    Rename-Item ~/Ubuntu.appx ~/Ubuntu.zip
    Expand-Archive ~/Ubuntu.zip ~/Ubuntu
    ```

2. Запустите средство запуска дистрибутива для завершения установки, запустите приложение запуска дистрибутива в целевой папке с именем `<distro>.exe`. Например: `ubuntu.exe`и т. д.

    ![Расширенный дистрибутив Ubuntu в Windows Server](media/server-appx-expand.png)

    > **Устранение неполадок**
    > * **Установка завершилась ошибкой 0x8007007e**: Эта ошибка возникает, когда ваша система не поддерживает WSL. Убедитесь в следующем.
    >   * Вы используете Windows сборки 16215 или более поздней версии. [Проверьте сборку](troubleshooting.md#check-your-build-number).
    >   * Подсистема Windows для Linux дополнительный компонент включен и перезагрузки компьютера.  [Убедитесь, что включен WSL](troubleshooting.md#confirm-wsl-is-enabled).
    
3. Добавить путь к дистрибутива в среде Windows путь (`C:\Users\Administrator\Ubuntu` в этом примере), например, с помощью Powershell:
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + "C:\Users\Administrator\Ubuntu", "User")
    ```
    Теперь вы можете запускать вашего дистрибутива из любой путь, введя `<distro>.exe`. Пример: `ubuntu.exe`

Теперь, когда устанавливается дистрибутив Linux, необходимо [инициализации в новом экземпляре дистрибутива](initialize-distro.md) перед использованием вашего дистрибутива.
