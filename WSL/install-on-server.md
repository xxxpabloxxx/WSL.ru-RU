---
title: Установка подсистемы Linux в Windows Server
description: Инструкции по установке для подсистемы Linux в Windows Server.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, windows server
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 805b7d266020c62e0c6f58889541517d44db3726
ms.sourcegitcommit: 90f7caeefe886bf6c0ba2b90c1b56b5f9795ad1b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/28/2020
ms.locfileid: "84153079"
---
# <a name="windows-server-installation-guide"></a>Руководство по установке Windows Server

Подсистема Windows для Linux доступна для установки на Windows Server 2019 (версия 1709) и более поздних версий. В этом руководстве рассматриваются действия по включению WSL на компьютере.

## <a name="enable-the-windows-subsystem-for-linux"></a>Включение подсистемы Windows для Linux

Перед запуском дистрибутивов Linux в Windows необходимо включить дополнительный компонент "Подсистема Windows для Linux" и перезагрузить компьютер.

Запустите PowerShell с правами администратора и выполните следующую команду.

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

```

**Если вам нужна 100 % совместимость с системными вызовами и более быстрая производительность ввода-вывода, ознакомьтесь со сведениями ниже, чтобы установить WSL 2!**

Подсистема WSL 2 доступна только в Windows 10 версии 2004, сборки 19041 или выше. Может потребоваться [обновить версию Windows](ms-settings:windowsupdate).

**В случае продолжения работы с WSL 1 перезагрузите компьютер, когда появится соответствующее сообщение, и продолжите установку [здесь](./install-on-server.md#download-a-linux-distribution)** .

## <a name="enable-the-virtual-machine-platform-optional-component"></a>Включение необязательного компонента "Virtual Machine Platform" (Платформа виртуальной машины)

Убедитесь, что установлен дополнительный компонент "Virtual Machine Platform" (Платформа виртуальных машин). Это можно сделать, выполнив следующую команду в PowerShell:

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
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
