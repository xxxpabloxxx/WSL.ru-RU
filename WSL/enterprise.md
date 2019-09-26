---
title: Подсистема Windows для Linux для предприятий
description: Ресурсы и инструкции по оптимальному использованию подсистемы Windows для Linux в корпоративной среде.
keywords: Башонвиндовс, bash, WSL, Windows, подсистема Windows для Linux, виндовссубсистем, Ubuntu, Debian, SUSE, Windows 10, предприятие, развертывание, автономный, упаковка, хранение, распространение, установка, установка
ms.date: 09/04/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: c32d62267c77d87fb200cfe43b8e6f43b4e3a56d
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269862"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a>Подсистема Windows для Linux для предприятий

Microsoft Store для бизнеса предлагают разнообразные решения для предприятий, желающих развернуть WSL в своей компании. [Документы в Интернете](https://docs.microsoft.com/en-us/microsoft-store/) для Microsoft Store для бизнеса — это отличный ресурс для поиска общих сведений о магазине.

Если вы только хотите настроить для начала развертывания WSL, выполните следующие действия, которые объясняются в Microsoft Store документах:

* [Подпишитесь на Microsoft Store для бизнеса и приступайте к работе](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* [Управляйте своими продуктами и службами (включая пользователей, которые могут получать доступ к каким приложениям в частном хранилище)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview). Здесь можно добавить WSL дистрибутивов в магазин и контролировать, кто их может устанавливать.
* [Использование выбранного метода распространения для развертывания программного обеспечения в компании](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* Обмен данными с пользователями, имеющими доступ к WSL дистрибутивов, которые могут [использовать эти действия](https://docs.microsoft.com/en-us/windows/wsl/install-win10) для установки дистрибутив или дистрибутивов по своему выбору 

## <a name="how-to-distribute-a-distro-offline"></a>Как распределить дистрибутив в автономном режиме

Если компьютеры в Организации не имеют доступа к Microsoft Store или Microsoft Store для бизнеса, то можно скачать установщик Linux дистрибутив с автономной лицензией, выполнив следующие действия. 

### <a name="set-up-an-azure-active-directory-ad-account"></a>Настройка учетной записи Azure Active Directory (AD) 

Для получения установщика Microsoft Store приложений необходимо иметь учетную запись Azure AD и быть глобальным администратором организации. Если у вас уже есть учетная запись, этот шаг можно пропустить.

Инструкции по регистрации учетной записи можно найти здесь: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a>Войдите в магазин для бизнеса и перейдите на домашнюю страницу.
Вход в систему: www.microsoft.com/business-store

![Домашняя страница магазина MS Store для бизнеса](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a>Перейдите в раздел Управление настройками > и включите параметр "показывать автономные приложения".

![Страница параметров магазина MS Store для бизнеса](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a>Вернитесь на главную страницу, щелкнув "магазин для моей группы".

![Домашняя страница магазина MS Store для бизнеса](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a>Выполните поиск нужных дистрибутив и выберите его.

![Домашняя страница магазина MS Store для бизнеса с активным поиском](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a>Выберите лицензию "вне сети" в раскрывающемся меню тип лицензии и щелкните "получить приложение".

![Страница продукта Ubuntu для магазина MS Store для бизнеса](media/offlineinstallscreens/4-screen.png)

Примечание. Некоторые дистрибутивов могут отказаться от автономной лицензии.

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a>Нажмите кнопку "Управление", чтобы перейти на страницу продукта приложения

![Страница продукта Ubuntu для магазина MS Store для бизнеса](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a>Выберите архитектуру и скачайте пакет для использования в автономном режиме

![Страница сведений о продукте для Microsoft Store для бизнеса Ubuntu](media/offlineinstallscreens/6-screen.png)

Затем этот установщик можно распространить на любой компьютер, на который необходимо установить WSL.