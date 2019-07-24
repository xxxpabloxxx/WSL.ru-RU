---
title: Установка подсистемы Linux в Windows Server
description: Инструкции по установке для подсистемы Linux на Windows Server.
keywords: Башонвиндовс, bash, WSL, Windows, подсистема Windows для Linux, виндовссубсистем, Ubuntu, Windows Server
author: scooley
ms.author: scooley
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: d295cf3db99fb45b943369f532f7e807a603061c
ms.sourcegitcommit: 8b5a8d49b63441478dd540887f534dcc6dd0ba41
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/21/2019
ms.locfileid: "67308793"
---
# <a name="windows-server-installation-guide"></a>Руководства по установке Windows Server

> Применимо к Windows Server 2019 и более поздних версий

В//Build2017 Корпорация Майкрософт объявила, что подсистема Windows для Linux будет [доступна в Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).  В этих инструкциях рассматривается запуск подсистемы Windows для Linux на Windows Server 1709 и более поздних версий.

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a>Включение подсистемы Windows для Linux (WSL)

Перед запуском Linux дистрибутивов в Windows необходимо включить дополнительный компонент "подсистема Windows для Linux" и перезагрузить компьютер.

1. Откройте PowerShell от имени администратора и выполните команду:
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. При появлении запроса перезагрузите компьютер. **Эта перезагрузка необходима** для того, чтобы WSL мог инициировать доверенную среду выполнения.

## <a name="download-a-linux-distro"></a>Загрузка дистрибутив Linux

Для загрузки избранного дистрибутива Linux выполните следующие [инструкции](install-manual.md) .

## <a name="extract-and-install-a-linux-distro"></a>Извлечение и установка дистрибутив Linux
Теперь, когда вы загрузили дистрибутив, извлеките его содержимое и вручную установите дистрибутив:

1. Извлеките `<distro>.appx` содержимое пакета, например с помощью PowerShell:

    ```powershell
    Rename-Item ./Ubuntu.appx ./Ubuntu.zip
    Expand-Archive ./Ubuntu.zip ./Ubuntu
    ```

2. Запустите средство запуска дистрибутив для завершения установки, запустите приложение запуска дистрибутив в целевой папке с именем `<distro>.exe`. Например: `ubuntu.exe`и т. д.

    ![Расширенная дистрибутив Ubuntu в Windows Server](media/server-appx-expand.png)

    > **Устранение неполадок**
    > * **Сбой установки с ошибкой 0x8007007e**: Эта ошибка возникает, когда система не поддерживает WSL. Убедитесь в следующем.
    >   * Вы используете Windows Build 16215 или более поздней версии. [Проверьте сборку](troubleshooting.md#check-your-build-number).
    >   * Дополнительный компонент подсистемы Windows для Linux включен и компьютер перезагружен.  [Убедитесь, что WSL включен](troubleshooting.md#confirm-wsl-is-enabled).
    
3. Добавьте путь дистрибутив в путь среды Windows (`C:\Users\Administrator\Ubuntu` в этом примере это), например с помощью PowerShell:
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    Теперь можно запустить дистрибутив из любого пути, введя `<distro>.exe`. Пример: `ubuntu.exe`

После установки дистрибутив для Linux необходимо [инициализировать новый экземпляр дистрибутив](initialize-distro.md) перед использованием дистрибутив.
