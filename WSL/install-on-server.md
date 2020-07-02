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
# <a name="windows-server-installation-guide"></a>Руководство по установке Windows Server

Подсистема Windows для Linux доступна для установки на Windows Server 2019 (версия 1709) и более поздних версий. В этом руководстве рассматриваются действия по включению WSL на компьютере.

## <a name="enable-the-windows-subsystem-for-linux"></a>Включение подсистемы Windows для Linux

Перед запуском дистрибутивов Linux в Windows необходимо включить дополнительный компонент "Подсистема Windows для Linux" и перезагрузить компьютер.

Запустите PowerShell с правами администратора и выполните следующую команду.

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

```

## <a name="download-a-linux-distribution"></a>Скачивание дистрибутива Linux

Выполните [эти инструкции](install-manual.md), чтобы скачать избранный дистрибутив Linux.

## <a name="extract-and-install-a-linux-distribution"></a>Извлечение и установка дистрибутива Linux

После загрузки дистрибутива Linux для извлечения его содержимого и установки вручную выполните следующие действия.

1. Извлеките содержимое пакета `<distro>.appx`, с помощью PowerShell:

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. Запустите средство запуска приложения дистрибутива в целевой папке. Средство запуска обычно называется `<distro>.exe` (например, `ubuntu.exe`).

    ![Расширенный дистрибутив Ubuntu в Windows Server](media/server-appx-expand.png)

> [!CAUTION]
> **Сбой установки с ошибкой 0x8007007e**. При возникновении этой ошибки система не поддерживает WSL. Убедитесь, что вы используете сборку Windows 16215 или более позднюю версию. [Проверьте используемую сборку](troubleshooting.md#check-your-build-number). Также убедитесь, [что WSL включен](troubleshooting.md#confirm-wsl-is-enabled) и ваш компьютер перезагружен после включения этой функции.  

3. Добавьте путь дистрибутива в путь среды Windows (в этом примере: `C:\Users\Administrator\Ubuntu`), с помощью PowerShell:

```powershell
$userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
[System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
```

Теперь вы можете запустить дистрибутив из любого пути, введя `<distro>.exe`. Например: `ubuntu.exe`.

После установки необходимо [инициализировать новый экземпляр дистрибутива](initialize-distro.md), прежде чем его можно будет использовать.
