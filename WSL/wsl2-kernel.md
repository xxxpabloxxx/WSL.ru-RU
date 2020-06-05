---
title: Обновление ядра Linux в WSL 2
description: Инструкции по обновлению ядра Linux в WSL 2 вручную
keywords: WSL, Windows, ядро Linux, подсистема Windows для Linux, ядро
ms.date: 03/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 1628bea2f1bae590928b055425413e5b085dffef
ms.sourcegitcommit: 90f7caeefe886bf6c0ba2b90c1b56b5f9795ad1b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/28/2020
ms.locfileid: "84153044"
---
# <a name="updating-the-wsl-2-linux-kernel"></a>Обновление ядра Linux в WSL 2

Чтобы вручную обновить ядро Linux в WSL 2, выполните описанные ниже действия.

> [!NOTE] 
> Если установщику не удается найти WSL 1, щелкните правой кнопкой мыши установщик обновления ядра Linux, а затем нажмите кнопку "Удалить" и запустите установщик повторно.

## <a name="download-the-linux-kernel-update-package"></a>Скачивание пакета обновления ядра Linux

[Скачайте последнюю версию пакета обновления ядра Linux в WSL 2](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) для 64-разрядных компьютеров.

> [!NOTE]
> Если вы используете компьютер ARM64, вместо этого скачайте [пакет ARM64](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi).

## <a name="install-the-linux-kernel-update-package"></a>Установка пакета обновления ядра Linux

Чтобы установить пакет обновления ядра Linux:

  1. Запустите пакет обновления, скачанный на предыдущем этапе.

  2. Появится запрос на повышение уровня разрешений. Нажмите кнопку "Да", чтобы утвердить эту установку.

  3. По завершении установки можно приступить к использованию WSL 2.

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a>Дальнейшие планы по обновлению ядра Linux в WSL 2

Дополнительные сведения см. в статье об [изменениях процесса установки обновления ядра Linux в WSL 2](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), доступной в блоге, [посвященному командной строке Windows](https://aka.ms/cliblog).
