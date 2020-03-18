---
title: Обновление ядра Linux в WSL 2
description: Инструкции по обновлению ядра Linux в WSL 2 вручную
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, wsl.conf, wslconfig
ms.date: 03/12/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.localizationpriority: high
ms.custom: seodec18
ms.openlocfilehash: f7fce13c2acc65e3afa2cc56873e40bc55a460bc
ms.sourcegitcommit: 506272bd7fc1cbda7e32146d54a8bdd02af3e0c4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/13/2020
ms.locfileid: "79319714"
---
# <a name="updating-the-wsl-2-linux-kernel"></a>Обновление ядра Linux в WSL 2

Чтобы вручную обновить ядро Linux в WSL 2, выполните описанные ниже действия. 

## <a name="download-the-linux-kernel-update-package"></a>Скачивание пакета обновления ядра Linux

Щелкните [эту ссылку](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi), чтобы скачать последнюю версию пакета обновления ядра Linux в WSL 2 для компьютеров AMD64.

> [!NOTE] 
> Если вы используете компьютер ARM64, вместо этого скачайте [этот пакет](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi).

## <a name="install-the-linux-kernel-update-package"></a>Установка пакета обновления ядра Linux

Чтобы установить пакет обновления ядра Linux:

    1. Запустите пакет обновления, скачанный на предыдущем этапе.
    2. Появится запрос на повышение уровня разрешений. Нажмите кнопку "Да", чтобы утвердить эту установку.
    3. По завершении установки можно приступить к использованию WSL 2.

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a>Дальнейшие планы по обновлению ядра Linux в WSL 2

Дополнительные сведения об этих изменениях см. в [этой записи](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) блога, посвященного [командной строке Windows](https://aka.ms/cliblog).
