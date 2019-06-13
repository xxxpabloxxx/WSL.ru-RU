---
title: Установка подсистемы Windows для Linux (WSL) в Windows 10
description: Инструкции по установке подсистемы Windows для Linux в Windows 10.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, debian, suse, windows 10, установка
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: d30a5883d648e084193659e997c55d203eb5a735
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/12/2019
ms.locfileid: "67035050"
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

    * [Ubuntu 16.04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [Ubuntu 18.04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [OpenSUSE Leap 15](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [OpenSUSE Leap 42](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [SUSE Linux Enterprise Server 12](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [SUSE Linux Enterprise Server 15](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [Remix Fedora для WSL](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [WLinux](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [WLinux Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [Alpine WSL](https://www.microsoft.com/store/apps/9p804crf0395)

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
    
    
 * **Сбой с ошибкой 0x8007019e WslRegisterDistribution**   
  * Подсистема Windows для Linux, дополнительный компонент не включен: 
   * Откройте **панели управления** -> **программы и компоненты** "->" ** Включение или отключение компонентов Windows ** -> Проверка **подсистема Windows для Linux** или с помощью Командлет PowerShell, упомянутых в начале этой статьи.
