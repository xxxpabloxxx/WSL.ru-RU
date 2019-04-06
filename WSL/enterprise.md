---
title: Подсистема Windows для Linux для предприятия
description: Ресурсы и инструкции о том, как лучше использовать подсистему Windows для Linux в среде предприятия.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, debian, suse, windows 10, enterprise, развертывания, автономной, упаковки, хранилище, распространения, установка, установка
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 09/04/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 9d867654d1b66fc14b58bc5e111986a7d38ef79c
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063282"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a>Подсистема Windows для Linux для предприятия

Microsoft Store для бизнеса предлагает широкий набор решений для предприятий, желающих развернуть WSL для своей компании. [Онлайн-документации](https://docs.microsoft.com/en-us/microsoft-store/) для Microsoft Store для бизнеса — это отличный ресурс, общие сведения о работе с Store.

Если вы — компании, которая просто хотите установить до начала развертывания WSL помогут следующие действия, которые описаны в документы Microsoft Store:

* [Зарегистрируйтесь для Microsoft Store для бизнеса и приступить к работе](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* [Управление продуктов и служб (включая, кто имеет доступ к каким приложениям в частного магазина)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview). Здесь можно добавить дистрибутивов WSL хранилище и управлять тем, кто их можно установить
* [Используйте метод распространения по своему усмотрению для развертывания программного обеспечения в вашей компании](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* Для пользователей, имеющих доступ к WSL дистрибутивов, они могут взаимодействовать [выполните следующие действия,](https://docs.microsoft.com/en-us/windows/wsl/install-win10) для установки дистрибутива или дистрибутивов по своему выбору 

## <a name="how-to-distribute-a-distro-offline"></a>Способ распределения дистрибутив автономный режим

Если компьютеры в вашей организации не имеют доступ к Microsoft Store или Microsoft Store для бизнеса, то можете скачать установщик дистрибутив Linux с автономной лицензией, выполнив следующие действия. 

### <a name="set-up-an-azure-active-directory-ad-account"></a>Настроить учетную запись Azure Active Directory (AD) 

Необходимо иметь учетную запись Azure AD и быть глобальным администратором для вашей организации, чтобы получить установщик приложений Microsoft Store. Если вы уже есть учетная запись, этот шаг можно пропустить.

Инструкции для регистрации учетной записи можно найти здесь: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a>Войдите в Store для бизнеса и перейдите на домашнюю страницу
Войдите здесь: www.microsoft.com/business-store

![MS Store для бизнеса домашней страницы](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a>Перейдите на управление -> Параметры и включить «Показывать автономные приложения»

![MS Store для бизнеса странице "Параметры"](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a>Вернитесь на главную страницу, нажав кнопку «Приобрести Моя группа»

![MS Store для бизнеса домашней страницы](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a>Найдите свой дистрибутив нужный и выберите его

![MS Store для бизнеса Домашняя страница с поиск в active](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a>Выберите лицензию «Вне сети» в раскрывающемся списке Тип лицензии и нажмите кнопку «Получить приложения»

![MS Store для бизнеса Ubuntu продукта страницы](media/offlineinstallscreens/4-screen.png)

Обратите внимание: Некоторые дистрибутивы может отказаться быть автономной лицензией

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a>Нажмите кнопку «Управление», чтобы получить доступ к странице продукта приложения

![MS Store для бизнеса Ubuntu продукта страницы](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a>Выберите архитектуру и загрузить пакет в автономном режиме

![MS Store для странице сведений о продукте Ubuntu бизнеса](media/offlineinstallscreens/6-screen.png)

Затем этот установщик можно распространять на любом компьютере, где вы хотите установить WSL.