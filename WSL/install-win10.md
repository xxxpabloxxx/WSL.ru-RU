---
title: Установка подсистемы Windows для Linux (WSL) на в Windows 10
description: Инструкции по установке подсистемы Windows для Linux в Windows 10.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, debian, suse, windows 10, установка
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 40bbe73acbfd0483e18ab6ff1696fdb44eaff2e4
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063292"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Подсистема Windows для Linux руководство по установке для Windows 10

## <a name="install-the-windows-subsystem-for-linux"></a>Установите подсистему Windows для Linux

Прежде чем устанавливать все дистрибутивы Linux для WSL, необходимо убедиться, что «Windows подсистемы для Linux» необязательный параметр:

1. Откройте PowerShell от имени администратора и выполните:
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. Перезагрузите компьютер при появлении запроса.

## <a name="install-your-linux-distribution-of-choice"></a>Установка дистрибутива Linux по выбору
Чтобы скачать и установить ваш предпочитаемый distro(s), у вас есть три варианта:
1. Загрузите и установите Windows Store (см. ниже)
1. Загрузить и установить из командной-строки или сценария ([прочитать инструкции по ручной установке](install-manual.md))
1. Скачайте и распакуйте и установить вручную (для Windows Server - [приведенным ниже указаниям](install-on-server.md))

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a>Windows 10 Fall Creators Update и более поздних версий: Установка из Microsoft Store

> Этот раздел предназначен для построения 16215 или более поздней версии Windows.  Выполните следующие действия для [проверьте построения](troubleshooting.md#check-your-build-number). 

1. Откройте Microsoft Store и выберите избранные дистрибутива Linux.

    ![Представление из дистрибутивов Linux в магазине Windows](media/store.png)

    Приведенные ниже ссылки откроется на странице магазина Windows для каждого распределения:

    * [Ubuntu](https://www.microsoft.com/store/p/ubuntu/9nblggh4msv6)
    * [openSUSE](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [SLES](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)

1. На странице дистрибутива выберите «Получить»

    ![Представление из дистрибутивов Linux в магазине Windows](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>Завершения инициализации из вашего дистрибутива
Теперь, когда устанавливается дистрибутив Linux, необходимо [инициализации в новом экземпляре дистрибутива](initialize-distro.md) один раз, прежде чем можно будет использовать.

## <a name="troubleshooting"></a>Устранение неполадок: 

Ниже приведены ошибки, связанные с и предлагаемые исправления. Ссылаться на [WSL странице](troubleshooting.md) для других распространенных ошибок и способы их решения.

* **Установка завершилась ошибкой 0x80070003**
    * Подсистема Windows для Linux выполняется только на системном диске (обычно это ваш `C:` диска). Убедитесь, что на системном диске хранятся дистрибутивов:  
    * Откройте **параметры** -> **хранения** -> **Дополнительные параметры хранилища: Изменение, где сохраняется новое содержимое**
    ![картину системных параметров для установки приложений на диске C:](media/AppStorage.png)
