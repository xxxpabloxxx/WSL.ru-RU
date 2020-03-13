---
title: Обновление ядра Linux для WSL 2
description: Инструкции по обновлению ядра Linux для WSL 2 вручную
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, wsl.conf, wslconfig
ms.date: 03/12/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: edc7ea35d8ebe0c71488763017cde2bb45c53b6d
ms.sourcegitcommit: 8795e1c4c5d2efdc8a9c78af05fb7be3ac1eef3d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/12/2020
ms.locfileid: "79138193"
---
# <a name="updating-the-wsl-2-linux-kernel"></a>Обновление ядра Linux для WSL 2

Чтобы вручную обновить ядро Linux в WSL 2, выполните следующие действия. 

## <a name="download-the-linux-kernel-update-package"></a>Загрузка пакета обновления ядра Linux

Щелкните [эту ссылку](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) , чтобы скачать последнюю версию пакета обновления ядра Linux для WSL2 для компьютеров AMD64.

> [!NOTE] Если вы используете компьютер ARM64, скачайте [Этот пакет](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) .

## <a name="install-the-linux-kernel-update-package"></a>Установка пакета обновления ядра Linux

Чтобы установить пакет обновления ядра Linux, выполните следующие действия.
    1. Запустите пакет обновления, скачанный на предыдущем шаге.
    2. Появится запрос на повышение прав, нажмите кнопку "Да", чтобы утвердить эту установку.
    3. После завершения установки можно приступить к использованию WSL2!

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a>Будущие планы обновления ядра Linux для WSL2

Дополнительные сведения об этих изменениях см. в [этой записи блога](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) в [блоге командной строки Windows](https://aka.ms/cliblog).