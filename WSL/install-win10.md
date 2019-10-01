---
title: Установка подсистемы Windows для Linux (WSL) в Windows 10
description: Инструкции по установке подсистемы Windows для Linux в Windows 10.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, debian, suse, windows 10, установка
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: c53c4507fb56f8e4a3456963b1d6f50ceac8ef37
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269812"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Руководство по установке подсистемы Windows для Linux в Windows 10

## <a name="install-the-windows-subsystem-for-linux"></a>Установка подсистемы Windows для Linux

Перед установкой каких-либо дистрибутивов Linux для WSL необходимо убедиться, что включен дополнительный компонент "Подсистема Windows для Linux".

1. Запустите PowerShell с правами администратора и выполните следующую команду.
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. При появлении соответствующего запроса перезагрузите компьютер.

## <a name="install-your-linux-distribution-of-choice"></a>Установка дистрибутива Linux по выбору
Чтобы скачать и установить предпочтительные дистрибутивы, у вас есть три варианта:
1. Скачайте и установите их из Microsoft Store (см. ниже).
1. Скачайте и установите их с помощью командной строки или сценария ([ознакомьтесь с инструкциями по установке вручную](install-manual.md)).
1. Скачайте их, а затем вручную распакуйте и установите (инструкции для Windows Server доступны [здесь](install-on-server.md)).

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a>Windows 10 Fall Creators Update и более поздние версии: установка из Microsoft Store

> Этот раздел предназначен для сборки 16215 Windows или более поздней версии.  Выполните следующие действия, чтобы [узнать номер своей сборки](troubleshooting.md#check-your-build-number). 

1. Откройте Microsoft Store и выберите предпочтительный дистрибутив Linux.

    ![Представление дистрибутивов Linux в Microsoft Store](media/store.png)

    Ниже приведены ссылки на страницы Microsoft Store для каждого дистрибутива:

    * [Ubuntu 16.04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [Ubuntu 18.04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [OpenSUSE Leap 15](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [OpenSUSE Leap 42](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [SUSE Linux Enterprise Server 12](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [SUSE Linux Enterprise Server 15](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [Fedora Remix for WSL](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [Pengwin Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [Alpine WSL](https://www.microsoft.com/store/apps/9p804crf0395)

1. На странице дистрибутива щелкните "Получить".

    ![Представление дистрибутивов Linux в Microsoft Store](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>Завершение инициализации дистрибутива
После установки дистрибутива Linux необходимо [единоразово инициализировать новый экземпляр дистрибутива](initialize-distro.md), прежде чем его можно будет использовать.

## <a name="troubleshooting"></a>Устранение неполадок: 

Ниже перечислены возможные ошибки и способы их устранения. Другие распространенные ошибки и способы их устранения приведены в разделе [Устранение неполадок подсистемы Windows для Linux](troubleshooting.md).

* **Сбой установки с ошибкой 0x80070003**
    * Подсистема Windows для Linux работает только на системном диске (обычно это диск `C:`). Убедитесь, что дистрибутивы хранятся на системном диске.  
    * Выберите **Параметры** -> **Хранилище** -> **Другие параметры хранилища: Изменить место сохранения нового содержимого**.
    ![Изображение параметров системы для установки приложений на диске C:](media/AppStorage.png)
    
    
 * **Сбой WslRegisterDistribution с ошибкой 0x8007019e**   
  * Дополнительный компонент "Подсистема Windows для Linux" не включен. 
   * Выберите **Панель управления** -> **Программы и компоненты** -> **Включение или отключение компонентов Windows** и установите флажок **Подсистема Windows для Linux** или используйте командлет PowerShell, упомянутый в начале этой статьи.
