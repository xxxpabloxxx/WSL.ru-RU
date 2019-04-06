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
# <a name="windows-subsystem-for-linux-for-enterprise"></a><span data-ttu-id="3c6de-104">Подсистема Windows для Linux для предприятия</span><span class="sxs-lookup"><span data-stu-id="3c6de-104">Windows Subsystem for Linux for Enterprise</span></span>

<span data-ttu-id="3c6de-105">Microsoft Store для бизнеса предлагает широкий набор решений для предприятий, желающих развернуть WSL для своей компании.</span><span class="sxs-lookup"><span data-stu-id="3c6de-105">The Microsoft Store for Business offers a variety of solutions to Enterprises who want to deploy WSL to their company.</span></span> <span data-ttu-id="3c6de-106">[Онлайн-документации](https://docs.microsoft.com/en-us/microsoft-store/) для Microsoft Store для бизнеса — это отличный ресурс, общие сведения о работе с Store.</span><span class="sxs-lookup"><span data-stu-id="3c6de-106">The [online docs](https://docs.microsoft.com/en-us/microsoft-store/) for the Microsoft Store for Business are a great resource to find out general information about the Store experience.</span></span>

<span data-ttu-id="3c6de-107">Если вы — компании, которая просто хотите установить до начала развертывания WSL помогут следующие действия, которые описаны в документы Microsoft Store:</span><span class="sxs-lookup"><span data-stu-id="3c6de-107">If you’re a company that’s just looking to get set up to start deploying WSL you can follow these steps, which are explained inside of the Microsoft Store docs:</span></span>

* [<span data-ttu-id="3c6de-108">Зарегистрируйтесь для Microsoft Store для бизнеса и приступить к работе</span><span class="sxs-lookup"><span data-stu-id="3c6de-108">Sign up for the Microsoft Store for Business and get started</span></span>](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* <span data-ttu-id="3c6de-109">[Управление продуктов и служб (включая, кто имеет доступ к каким приложениям в частного магазина)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span><span class="sxs-lookup"><span data-stu-id="3c6de-109">[Manage your products and services (including who can access which apps in your private store)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span></span> <span data-ttu-id="3c6de-110">Здесь можно добавить дистрибутивов WSL хранилище и управлять тем, кто их можно установить</span><span class="sxs-lookup"><span data-stu-id="3c6de-110">Here you can add WSL distros to your store and control who can install them</span></span>
* [<span data-ttu-id="3c6de-111">Используйте метод распространения по своему усмотрению для развертывания программного обеспечения в вашей компании</span><span class="sxs-lookup"><span data-stu-id="3c6de-111">Use a distribution method of your choice to deploy the software to your company</span></span>](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* <span data-ttu-id="3c6de-112">Для пользователей, имеющих доступ к WSL дистрибутивов, они могут взаимодействовать [выполните следующие действия,](https://docs.microsoft.com/en-us/windows/wsl/install-win10) для установки дистрибутива или дистрибутивов по своему выбору</span><span class="sxs-lookup"><span data-stu-id="3c6de-112">Communicate to users who have access to WSL distros that they can [use these steps](https://docs.microsoft.com/en-us/windows/wsl/install-win10) to install the distro or distros of their choice</span></span> 

## <a name="how-to-distribute-a-distro-offline"></a><span data-ttu-id="3c6de-113">Способ распределения дистрибутив автономный режим</span><span class="sxs-lookup"><span data-stu-id="3c6de-113">How to Distribute a Distro Offline</span></span>

<span data-ttu-id="3c6de-114">Если компьютеры в вашей организации не имеют доступ к Microsoft Store или Microsoft Store для бизнеса, то можете скачать установщик дистрибутив Linux с автономной лицензией, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3c6de-114">If the computers in your company don’t have access to the Microsoft Store or the Microsoft Store for Business, then you can download the installer of a Linux distro that has an offline license by following these steps.</span></span> 

### <a name="set-up-an-azure-active-directory-ad-account"></a><span data-ttu-id="3c6de-115">Настроить учетную запись Azure Active Directory (AD)</span><span class="sxs-lookup"><span data-stu-id="3c6de-115">Set up an Azure Active Directory (AD) Account</span></span> 

<span data-ttu-id="3c6de-116">Необходимо иметь учетную запись Azure AD и быть глобальным администратором для вашей организации, чтобы получить установщик приложений Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="3c6de-116">You need to have an Azure AD account and be the global administrator for your organization to get the installer of Microsoft Store apps.</span></span> <span data-ttu-id="3c6de-117">Если вы уже есть учетная запись, этот шаг можно пропустить.</span><span class="sxs-lookup"><span data-stu-id="3c6de-117">If you already have an account, you can skip this step.</span></span>

<span data-ttu-id="3c6de-118">Инструкции для регистрации учетной записи можно найти здесь: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span><span class="sxs-lookup"><span data-stu-id="3c6de-118">The instructions to register an account can be found here: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span></span>

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a><span data-ttu-id="3c6de-119">Войдите в Store для бизнеса и перейдите на домашнюю страницу</span><span class="sxs-lookup"><span data-stu-id="3c6de-119">Sign into the Store for Business and go to the homepage</span></span>
<span data-ttu-id="3c6de-120">Войдите здесь: www.microsoft.com/business-store</span><span class="sxs-lookup"><span data-stu-id="3c6de-120">Sign in here: www.microsoft.com/business-store</span></span>

![MS Store для бизнеса домашней страницы](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a><span data-ttu-id="3c6de-122">Перейдите на управление -> Параметры и включить «Показывать автономные приложения»</span><span class="sxs-lookup"><span data-stu-id="3c6de-122">Go to Manage->Settings and enable 'Show offline apps'</span></span>

![MS Store для бизнеса странице "Параметры"](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a><span data-ttu-id="3c6de-124">Вернитесь на главную страницу, нажав кнопку «Приобрести Моя группа»</span><span class="sxs-lookup"><span data-stu-id="3c6de-124">Go back to the main page by clicking 'Shop for my group'</span></span>

![MS Store для бизнеса домашней страницы](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a><span data-ttu-id="3c6de-126">Найдите свой дистрибутив нужный и выберите его</span><span class="sxs-lookup"><span data-stu-id="3c6de-126">Search for your desired distro and select it</span></span>

![MS Store для бизнеса Домашняя страница с поиск в active](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a><span data-ttu-id="3c6de-128">Выберите лицензию «Вне сети» в раскрывающемся списке Тип лицензии и нажмите кнопку «Получить приложения»</span><span class="sxs-lookup"><span data-stu-id="3c6de-128">Select an ‘Offline’ license in the License type dropdown menu and click ‘Get the app’</span></span>

![MS Store для бизнеса Ubuntu продукта страницы](media/offlineinstallscreens/4-screen.png)

<span data-ttu-id="3c6de-130">Обратите внимание: Некоторые дистрибутивы может отказаться быть автономной лицензией</span><span class="sxs-lookup"><span data-stu-id="3c6de-130">Please note: some distros may elect not to have an offline license</span></span>

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a><span data-ttu-id="3c6de-131">Нажмите кнопку «Управление», чтобы получить доступ к странице продукта приложения</span><span class="sxs-lookup"><span data-stu-id="3c6de-131">Click the ‘Manage’ button to get to the app’s product page</span></span>

![MS Store для бизнеса Ubuntu продукта страницы](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a><span data-ttu-id="3c6de-133">Выберите архитектуру и загрузить пакет в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="3c6de-133">Select your architecture and download the package for offline use</span></span>

![MS Store для странице сведений о продукте Ubuntu бизнеса](media/offlineinstallscreens/6-screen.png)

<span data-ttu-id="3c6de-135">Затем этот установщик можно распространять на любом компьютере, где вы хотите установить WSL.</span><span class="sxs-lookup"><span data-stu-id="3c6de-135">This installer can then be distributed to any computer where you would like to install WSL.</span></span>