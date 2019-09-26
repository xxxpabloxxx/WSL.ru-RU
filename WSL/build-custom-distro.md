---
title: Создание пользовательской дистрибутив Linux для WSL
description: Узнайте, как создать настраиваемый дистрибутив Linux для подсистемы Windows для Linux.
keywords: Башонвиндовс, bash, WSL, Windows, подсистема Windows, дистрибутив, настраиваемый
ms.date: 03/27/2018
ms.topic: article
ms.assetid: a5095219-0c82-4ce5-9a6d-5c2fc00835a3
ms.custom: seodec18
ms.openlocfilehash: 181badd4ee2f69e904099c12b54dfbdf3a37e294
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269705"
---
# <a name="creating-a-custom-linux-distro-for-wsl"></a><span data-ttu-id="c2074-104">Создание пользовательской дистрибутив Linux для WSL</span><span class="sxs-lookup"><span data-stu-id="c2074-104">Creating a Custom Linux Distro for WSL</span></span>

<span data-ttu-id="c2074-105">Используйте наш пример WSL с открытым исходным кодом для создания пакетов WSL дистрибутив для Microsoft Store и (или) для создания пользовательских пакетов Linux дистрибутив для загрузки неопубликованных приложений.</span><span class="sxs-lookup"><span data-stu-id="c2074-105">Use our open source WSL sample to build WSL distro packages for the Microsoft Store and/or to create custom Linux distro packages for sideloading.</span></span> <span data-ttu-id="c2074-106">[Репозиторий запуска дистрибутив](https://github.com/Microsoft/WSL-DistroLauncher) можно найти на сайте GitHub.</span><span class="sxs-lookup"><span data-stu-id="c2074-106">You can find the [distro launcher repo](https://github.com/Microsoft/WSL-DistroLauncher) on GitHub.</span></span>

<span data-ttu-id="c2074-107">Этот проект включает:</span><span class="sxs-lookup"><span data-stu-id="c2074-107">This project enables:</span></span>
* <span data-ttu-id="c2074-108">Служба поддержки распространения Linux для упаковки и отправки дистрибутива Linux в качестве appx-пакета, работающего на WSL</span><span class="sxs-lookup"><span data-stu-id="c2074-108">Linux distribution maintainers to package and submit a Linux distribution as an appx that runs on WSL</span></span>
* <span data-ttu-id="c2074-109">Разработчики могут создавать настраиваемые дистрибутивы Linux, которые можно загруженные неопубликованные на свой компьютер разработки.</span><span class="sxs-lookup"><span data-stu-id="c2074-109">Developers to create custom Linux distributions that can be sideloaded onto their dev machine</span></span>

## <a name="background"></a><span data-ttu-id="c2074-110">Фон</span><span class="sxs-lookup"><span data-stu-id="c2074-110">Background</span></span>
<span data-ttu-id="c2074-111">Мы распространяем дистрибутивов Linux для WSL как приложения UWP с помощью Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="c2074-111">We distribute Linux distros for WSL as UWP applications through the Microsoft Store.</span></span> <span data-ttu-id="c2074-112">Можно установить приложения, которые будут запускаться на WSL — подсистему, расположенной в ядре Windows.</span><span class="sxs-lookup"><span data-stu-id="c2074-112">You can install those applications that will then run on WSL - the subsystem that sits in the Windows kernel.</span></span> <span data-ttu-id="c2074-113">Этот механизм доставки имеет много преимуществ, как описано в [предыдущей записи блога](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/).</span><span class="sxs-lookup"><span data-stu-id="c2074-113">This delivery mechanism has many benefits as discussed in an [earlier blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/).</span></span>

## <a name="sideloading-a-custom-linux-distro-package"></a><span data-ttu-id="c2074-114">Неопубликованная загрузка пользовательского пакета дистрибутив для Linux</span><span class="sxs-lookup"><span data-stu-id="c2074-114">Sideloading a Custom Linux Distro Package</span></span>
<span data-ttu-id="c2074-115">Вы можете создать пользовательский пакет дистрибутив для Linux в качестве приложения для загружать неопубликованные на личном компьютере.</span><span class="sxs-lookup"><span data-stu-id="c2074-115">You can create a custom Linux distro package as an application to sideload on your personal machine.</span></span> <span data-ttu-id="c2074-116">Обратите внимание, что пользовательский пакет не будет распространяться с помощью Microsoft Store, пока не будет отправлен в качестве обслуживания распространения.</span><span class="sxs-lookup"><span data-stu-id="c2074-116">Please note that your custom package would not be distributed through the Microsoft Store unless you submit as a distribution maintainer.</span></span>
<span data-ttu-id="c2074-117">Чтобы настроить компьютер для загружать неопубликованные приложений, его необходимо включить в параметрах системы в разделе "для разработчиков".</span><span class="sxs-lookup"><span data-stu-id="c2074-117">To set up your machine to sideload apps, you will need to enable this in the system settings under “For Developers”.</span></span>  <span data-ttu-id="c2074-118">Убедитесь, что выбран режим разработчика или загружать неопубликованные приложения.</span><span class="sxs-lookup"><span data-stu-id="c2074-118">Be sure to either have developer mode, or sideload apps selected</span></span>

## <a name="for-linux-distro-maintainers"></a><span data-ttu-id="c2074-119">Для дистрибутив обслуживания Linux</span><span class="sxs-lookup"><span data-stu-id="c2074-119">For Linux Distro Maintainers</span></span>
<span data-ttu-id="c2074-120">Для отправки в магазин необходимо работать с нами, чтобы получить утверждение публикации.</span><span class="sxs-lookup"><span data-stu-id="c2074-120">To submit to the Store, you will need to work with us to receive publishing approval.</span></span> <span data-ttu-id="c2074-121">Если вы являетесь владельцем дистрибутива Linux, который заинтересован в добавлении дистрибутива в Microsoft Store, обратитесь wslpartners@microsoft.comпо адресу.</span><span class="sxs-lookup"><span data-stu-id="c2074-121">If you are a Linux distribution owner interested in adding your distribution to the Microsoft Store, please contact wslpartners@microsoft.com.</span></span>

## <a name="getting-started"></a><span data-ttu-id="c2074-122">начало работы</span><span class="sxs-lookup"><span data-stu-id="c2074-122">Getting Started</span></span>
<span data-ttu-id="c2074-123">Следуйте инструкциям в [репозитории GitHub дистрибутив Launcher](https://github.com/Microsoft/WSL-DistroLauncher) , чтобы создать пользовательский пакет дистрибутив для Linux.</span><span class="sxs-lookup"><span data-stu-id="c2074-123">Follow the instructions on the [Distro Launcher GitHub repo](https://github.com/Microsoft/WSL-DistroLauncher) to create a custom Linux distro package.</span></span>

 
## <a name="team-blogs"></a><span data-ttu-id="c2074-124">Блоги группы</span><span class="sxs-lookup"><span data-stu-id="c2074-124">Team Blogs</span></span>
*  [<span data-ttu-id="c2074-125">Открытие источника. пример WSL для обслуживания распространения Linux и пользовательских дистрибутивов Linux для загрузки неопубликованных приложений</span><span class="sxs-lookup"><span data-stu-id="c2074-125">Open Sourcing a WSL Sample for Linux Distribution Maintainers and Sideloading Custom Linux Distributions</span></span>](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
* [<span data-ttu-id="c2074-126">Блог командной строки</span><span class="sxs-lookup"><span data-stu-id="c2074-126">Command-Line blog</span></span>](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a><span data-ttu-id="c2074-127">Предоставление отзыва</span><span class="sxs-lookup"><span data-stu-id="c2074-127">Provide Feedback</span></span>
* [<span data-ttu-id="c2074-128">Репозиторий GitHub дистрибутив Launcher</span><span class="sxs-lookup"><span data-stu-id="c2074-128">Distro Launcher GitHub repo</span></span>](https://github.com/Microsoft/WSL-DistroLauncher)
* [<span data-ttu-id="c2074-129">Средство регистрации проблем GitHub для WSL</span><span class="sxs-lookup"><span data-stu-id="c2074-129">GitHub issue tracker for WSL</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="c2074-130">Портал UserVoice для командной строки</span><span class="sxs-lookup"><span data-stu-id="c2074-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
