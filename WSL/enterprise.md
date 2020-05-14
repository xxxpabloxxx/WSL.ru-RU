---
title: Подсистема Windows для Linux для предприятий
description: Ресурсы и инструкции для оптимального использования подсистемы Windows для Linux в корпоративной среде.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, debian, suse, windows 10, корпоративный, развертывание, автономный, упаковка, магазин, распространение, установка, установить
ms.date: 05/15/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 02f4ff41614f78c0e588f329c777a87f8b416233
ms.sourcegitcommit: 3fb40fd65b34a5eb26b213a0df6a3b2746b7a9b4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2020
ms.locfileid: "83235833"
---
# <a name="set-up-windows-subsystem-for-linux-for-your-enterprise-company"></a>Настройка подсистемы Windows для Linux для вашего предприятия

Microsoft Store для бизнеса предлагает различные решения для предприятий, которые хотят развернуть WSL в своей компании. Документация [Microsoft Store для бизнеса и образования](https://docs.microsoft.com/microsoft-store/) является отличным ресурсом для поиска общих сведений о магазине.

Если вы представляете компанию, которая только собирается начать установку WSL, выполните следующие шаги:

* [Зарегистрируйтесь в Microsoft Store для бизнеса и приступайте к работе](https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business-overview)
* [Получите сведения об управлении своими продуктами и услугами (включая тем, кто может получать доступ к каким приложениям в вашем личном магазине)](https://docs.microsoft.com/microsoft-store/manage-apps-microsoft-store-for-business-overview). Здесь вы можете добавлять дистрибутивы WSL в свое хранилище и контролировать, кто может их устанавливать
* [Используйте выбранный метод распространения для развертывания программного обеспечения в компании](https://docs.microsoft.com/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* Свяжитесь с сотрудниками вашей компании, чтобы они могли использовать эту ссылку на эту документацию для установки WSL: [Установка подсистемы Windows для Linux](./install-win10.md)

## <a name="how-to-distribute-a-linux-distribution-on-windows-offline"></a>Как распределять дистрибутив Linux в Windows в автономном режиме

Если компьютеры в вашей организации не имеют доступа к Microsoft Store или Microsoft Store для бизнеса, можно скачать установщик дистрибутива Linux с автономной лицензией, выполнив следующие действия.

### <a name="set-up-an-azure-active-directory-account"></a>Настройка учетной записи Azure Active Directory.

Чтобы получить установщик приложений Microsoft Store необходимо [зарегистрироваться для использования учетной записи Azure AD](https://docs.microsoft.com/azure/active-directory/fundamentals/sign-up-organization?WT.mc_id=windows-c9-niner) и быть глобальным администратором организации. Если у вас уже есть учетная запись, этот шаг можно пропустить.

### <a name="set-up-wsl-using-your-microsoft-store-for-business-account"></a>Настройка WSL с помощью учетной записи Microsoft Store для бизнеса

Инструкции по регистрации учетной записи можно найти здесь: https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business

1. Войдите в Store для бизнеса и перейдите на домашнюю страницу: https://www.microsoft.com/business-store

    ![Домашняя страница MS Store для бизнеса](media/offlineinstallscreens/1-screen.png)

2. Перейдите в меню "Управление" > "Настройки" и включите параметр Show offline apps (Показывать автономные приложения).

    ![Страница параметров MS Store для бизнеса](media/offlineinstallscreens/2-screen.png)

3. Вернитесь на главную страницу, выбрав "Магазин для моей группы".

    ![Домашняя страница MS Store для бизнеса](media/offlineinstallscreens/1-screen.png)

4. Найдите нужный дистрибутив и выберите его.

    ![Домашняя страница MS Store для бизнеса с активным поиском](media/offlineinstallscreens/3-screen.png)

5. Выберите "Автономная" лицензия в раскрывающемся меню "Тип лицензии" и выберите "Получить приложение". (Некоторые дистрибутивы Linux могут не предоставлять автономную лицензию).

    ![Страница продукта Ubuntu для MS Store для бизнеса](media/offlineinstallscreens/4-screen.png)

6. Нажмите кнопку "Управление", чтобы перейти на страницу продукта приложения.

    ![Страница продукта Ubuntu для MS Store для бизнеса](media/offlineinstallscreens/5-screen.png)

7. Выберите архитектуру и скачайте пакет для использования в автономном режиме.

    ![Страница сведений о продукте Ubuntu для Microsoft Store для бизнеса](media/offlineinstallscreens/6-screen.png)

Затем этот установщик можно распространить на любой компьютер, на который необходимо установить WSL.
