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
# <a name="windows-subsystem-for-linux-for-enterprise"></a><span data-ttu-id="ccf6e-104">Подсистема Windows для Linux для предприятий</span><span class="sxs-lookup"><span data-stu-id="ccf6e-104">Windows Subsystem for Linux for Enterprise</span></span>

<span data-ttu-id="ccf6e-105">Microsoft Store для бизнеса предлагают разнообразные решения для предприятий, желающих развернуть WSL в своей компании.</span><span class="sxs-lookup"><span data-stu-id="ccf6e-105">The Microsoft Store for Business offers a variety of solutions to Enterprises who want to deploy WSL to their company.</span></span> <span data-ttu-id="ccf6e-106">[Документы в Интернете](https://docs.microsoft.com/en-us/microsoft-store/) для Microsoft Store для бизнеса — это отличный ресурс для поиска общих сведений о магазине.</span><span class="sxs-lookup"><span data-stu-id="ccf6e-106">The [online docs](https://docs.microsoft.com/en-us/microsoft-store/) for the Microsoft Store for Business are a great resource to find out general information about the Store experience.</span></span>

<span data-ttu-id="ccf6e-107">Если вы только хотите настроить для начала развертывания WSL, выполните следующие действия, которые объясняются в Microsoft Store документах:</span><span class="sxs-lookup"><span data-stu-id="ccf6e-107">If you’re a company that’s just looking to get set up to start deploying WSL you can follow these steps, which are explained inside of the Microsoft Store docs:</span></span>

* [<span data-ttu-id="ccf6e-108">Подпишитесь на Microsoft Store для бизнеса и приступайте к работе</span><span class="sxs-lookup"><span data-stu-id="ccf6e-108">Sign up for the Microsoft Store for Business and get started</span></span>](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* <span data-ttu-id="ccf6e-109">[Управляйте своими продуктами и службами (включая пользователей, которые могут получать доступ к каким приложениям в частном хранилище)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span><span class="sxs-lookup"><span data-stu-id="ccf6e-109">[Manage your products and services (including who can access which apps in your private store)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span></span> <span data-ttu-id="ccf6e-110">Здесь можно добавить WSL дистрибутивов в магазин и контролировать, кто их может устанавливать.</span><span class="sxs-lookup"><span data-stu-id="ccf6e-110">Here you can add WSL distros to your store and control who can install them</span></span>
* [<span data-ttu-id="ccf6e-111">Использование выбранного метода распространения для развертывания программного обеспечения в компании</span><span class="sxs-lookup"><span data-stu-id="ccf6e-111">Use a distribution method of your choice to deploy the software to your company</span></span>](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* <span data-ttu-id="ccf6e-112">Обмен данными с пользователями, имеющими доступ к WSL дистрибутивов, которые могут [использовать эти действия](https://docs.microsoft.com/en-us/windows/wsl/install-win10) для установки дистрибутив или дистрибутивов по своему выбору</span><span class="sxs-lookup"><span data-stu-id="ccf6e-112">Communicate to users who have access to WSL distros that they can [use these steps](https://docs.microsoft.com/en-us/windows/wsl/install-win10) to install the distro or distros of their choice</span></span> 

## <a name="how-to-distribute-a-distro-offline"></a><span data-ttu-id="ccf6e-113">Как распределить дистрибутив в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="ccf6e-113">How to Distribute a Distro Offline</span></span>

<span data-ttu-id="ccf6e-114">Если компьютеры в Организации не имеют доступа к Microsoft Store или Microsoft Store для бизнеса, то можно скачать установщик Linux дистрибутив с автономной лицензией, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ccf6e-114">If the computers in your company don’t have access to the Microsoft Store or the Microsoft Store for Business, then you can download the installer of a Linux distro that has an offline license by following these steps.</span></span> 

### <a name="set-up-an-azure-active-directory-ad-account"></a><span data-ttu-id="ccf6e-115">Настройка учетной записи Azure Active Directory (AD)</span><span class="sxs-lookup"><span data-stu-id="ccf6e-115">Set up an Azure Active Directory (AD) Account</span></span> 

<span data-ttu-id="ccf6e-116">Для получения установщика Microsoft Store приложений необходимо иметь учетную запись Azure AD и быть глобальным администратором организации.</span><span class="sxs-lookup"><span data-stu-id="ccf6e-116">You need to have an Azure AD account and be the global administrator for your organization to get the installer of Microsoft Store apps.</span></span> <span data-ttu-id="ccf6e-117">Если у вас уже есть учетная запись, этот шаг можно пропустить.</span><span class="sxs-lookup"><span data-stu-id="ccf6e-117">If you already have an account, you can skip this step.</span></span>

<span data-ttu-id="ccf6e-118">Инструкции по регистрации учетной записи можно найти здесь: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span><span class="sxs-lookup"><span data-stu-id="ccf6e-118">The instructions to register an account can be found here: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span></span>

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a><span data-ttu-id="ccf6e-119">Войдите в магазин для бизнеса и перейдите на домашнюю страницу.</span><span class="sxs-lookup"><span data-stu-id="ccf6e-119">Sign into the Store for Business and go to the homepage</span></span>
<span data-ttu-id="ccf6e-120">Вход в систему: www.microsoft.com/business-store</span><span class="sxs-lookup"><span data-stu-id="ccf6e-120">Sign in here: www.microsoft.com/business-store</span></span>

![Домашняя страница магазина MS Store для бизнеса](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a><span data-ttu-id="ccf6e-122">Перейдите в раздел Управление настройками > и включите параметр "показывать автономные приложения".</span><span class="sxs-lookup"><span data-stu-id="ccf6e-122">Go to Manage->Settings and enable 'Show offline apps'</span></span>

![Страница параметров магазина MS Store для бизнеса](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a><span data-ttu-id="ccf6e-124">Вернитесь на главную страницу, щелкнув "магазин для моей группы".</span><span class="sxs-lookup"><span data-stu-id="ccf6e-124">Go back to the main page by clicking 'Shop for my group'</span></span>

![Домашняя страница магазина MS Store для бизнеса](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a><span data-ttu-id="ccf6e-126">Выполните поиск нужных дистрибутив и выберите его.</span><span class="sxs-lookup"><span data-stu-id="ccf6e-126">Search for your desired distro and select it</span></span>

![Домашняя страница магазина MS Store для бизнеса с активным поиском](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a><span data-ttu-id="ccf6e-128">Выберите лицензию "вне сети" в раскрывающемся меню тип лицензии и щелкните "получить приложение".</span><span class="sxs-lookup"><span data-stu-id="ccf6e-128">Select an ‘Offline’ license in the License type dropdown menu and click ‘Get the app’</span></span>

![Страница продукта Ubuntu для магазина MS Store для бизнеса](media/offlineinstallscreens/4-screen.png)

<span data-ttu-id="ccf6e-130">Примечание. Некоторые дистрибутивов могут отказаться от автономной лицензии.</span><span class="sxs-lookup"><span data-stu-id="ccf6e-130">Please note: some distros may elect not to have an offline license</span></span>

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a><span data-ttu-id="ccf6e-131">Нажмите кнопку "Управление", чтобы перейти на страницу продукта приложения</span><span class="sxs-lookup"><span data-stu-id="ccf6e-131">Click the ‘Manage’ button to get to the app’s product page</span></span>

![Страница продукта Ubuntu для магазина MS Store для бизнеса](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a><span data-ttu-id="ccf6e-133">Выберите архитектуру и скачайте пакет для использования в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="ccf6e-133">Select your architecture and download the package for offline use</span></span>

![Страница сведений о продукте для Microsoft Store для бизнеса Ubuntu](media/offlineinstallscreens/6-screen.png)

<span data-ttu-id="ccf6e-135">Затем этот установщик можно распространить на любой компьютер, на который необходимо установить WSL.</span><span class="sxs-lookup"><span data-stu-id="ccf6e-135">This installer can then be distributed to any computer where you would like to install WSL.</span></span>