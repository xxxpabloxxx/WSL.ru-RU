---
title: Установка подсистемы Windows для Linux (WSL) в Windows 10
description: Инструкции по установке для подсистемы Windows для Linux в Windows 10.
keywords: Башонвиндовс, bash, WSL, Windows, подсистема Windows для Linux, виндовссубсистем, Ubuntu, Debian, SUSE, Windows 10, install
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 82b5c0ccba7a444f13f186a2e33f210ac2cf48da
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499283"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Руководства по установке подсистемы Windows для Linux для Windows 10

## <a name="install-the-windows-subsystem-for-linux"></a>Установка подсистемы Windows для Linux

Перед установкой дистрибутивов Linux для WSL необходимо убедиться, что включена дополнительная функция "подсистема Windows для Linux":

1. Откройте PowerShell от имени администратора и выполните команду:
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. При появлении запроса перезагрузите компьютер.

## <a name="install-your-linux-distribution-of-choice"></a>Установка дистрибутива Linux по выбору
Чтобы скачать и установить предпочтительные дистрибутив, вы можете выбрать три варианта:
1. Скачать и установить из Microsoft Store (см. ниже)
1. Скачайте и установите из командной строки или сценария (см.[инструкции по установке вручную](install-manual.md)).
1. Загрузка и ручное Распаковка и установка (для Windows Server — [инструкции здесь](install-on-server.md))

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a>Обновления Windows 10 для дизайнеров и более поздних версий: Установка из Microsoft Store

> Этот раздел предназначен для Windows Build 16215 или более поздней версии.  Выполните следующие действия, чтобы [проверить сборку](troubleshooting.md#check-your-build-number). 

1. Откройте Microsoft Store и выберите предпочтительный дистрибутив Linux.

    ![Представление дистрибутивов Linux в Microsoft Store](media/store.png)

    Следующие ссылки открывают страницу Microsoft Store для каждого дистрибутива:

    * [Ubuntu 16,04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [Ubuntu 18,04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [OpenSUSE LEAP 15](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [OpenSUSE LEAP 42](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [SUSE Linux Enterprise Server 12](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [SUSE Linux Enterprise Server 15](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [Fedora Remix для WSL](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [Pengwin Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [Alpine WSL](https://www.microsoft.com/store/apps/9p804crf0395)

1. На странице дистрибутив выберите Get (получить).

    ![Представление дистрибутивов Linux в Microsoft Store](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>Завершение инициализации дистрибутив
После установки дистрибутив для Linux необходимо [инициализировать новый экземпляр дистрибутив](initialize-distro.md) , прежде чем его можно будет использовать.

## <a name="troubleshooting"></a>Устранение неполадок: 

Ниже приведены связанные ошибки и предлагаемые исправления. Другие распространенные ошибки и их решения см. на [странице Устранение неполадок WSL](troubleshooting.md) .

* **Сбой установки с ошибкой 0x80070003**
    * Подсистема Windows для Linux работает только на системном диске (обычно это `C:` диск). Убедитесь, что дистрибутивов хранятся на системном диске:  
    * Откройте **Параметры** -> хранилище Дополнительныепараметры->хранилища: ** Изменение места сохранения**
    новогосодержимогорисунокпараметровсистемыдляустановкиприложенийнадискеC:![](media/AppStorage.png)
    
    
 * **Сбой Вслрегистердистрибутион с ошибкой 0x8007019e**   
  * Необязательный компонент подсистемы Windows для Linux не включен: 
   * Откройте **панель** -> управления**программы и компоненты** — > * * Включение или отключение компонента Windows * *-> проверить подсистему **Windows для Linux** или использовать командлет PowerShell, упомянутый в начале этой статьи.
