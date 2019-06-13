---
title: Создание дистрибутив Linux, настраиваемые для WSL
description: Узнайте, как создать пользовательский дистрибутив Linux для подсистемы Windows для Linux.
keywords: BashOnWindows, bash, wsl, windows, windows подсистеме дистрибутива, пользовательский
author: taraj
ms.author: taraj
ms.date: 03/27/2018
ms.topic: article
ms.assetid: a5095219-0c82-4ce5-9a6d-5c2fc00835a3
ms.custom: seodec18
ms.openlocfilehash: 4072df5fa81f65fd9a3ff875ab887c03b234bce1
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040773"
---
# <a name="creating-a-custom-linux-distro-for-wsl"></a><span data-ttu-id="6786e-104">Создание дистрибутив Linux, настраиваемые для WSL</span><span class="sxs-lookup"><span data-stu-id="6786e-104">Creating a Custom Linux Distro for WSL</span></span>

<span data-ttu-id="6786e-105">Используйте наш пример WSL открытым исходным кодом для создания WSL дистрибутив пакетов для Microsoft Store и/или для создания пользовательских пакетов дистрибутив Linux для загрузки неопубликованных приложений.</span><span class="sxs-lookup"><span data-stu-id="6786e-105">Use our open source WSL sample to build WSL distro packages for the Microsoft Store and/or to create custom Linux distro packages for sideloading.</span></span> <span data-ttu-id="6786e-106">Можно найти [репозитория дистрибутивов запуска](https://github.com/Microsoft/WSL-DistroLauncher) на сайте GitHub.</span><span class="sxs-lookup"><span data-stu-id="6786e-106">You can find the [distro launcher repo](https://github.com/Microsoft/WSL-DistroLauncher) on GitHub.</span></span>

<span data-ttu-id="6786e-107">Этот проект включает:</span><span class="sxs-lookup"><span data-stu-id="6786e-107">This project enables:</span></span>
* <span data-ttu-id="6786e-108">Распространители дистрибутивов Linux для упаковки и отправки дистрибутив Linux как appx, который выполняется на WSL</span><span class="sxs-lookup"><span data-stu-id="6786e-108">Linux distribution maintainers to package and submit a Linux distribution as an appx that runs on WSL</span></span>
* <span data-ttu-id="6786e-109">Разработчикам создавать пользовательские дистрибутивы Linux, которые могут быть заливается на своем компьютере разработки</span><span class="sxs-lookup"><span data-stu-id="6786e-109">Developers to create custom Linux distributions that can be sideloaded onto their dev machine</span></span>

## <a name="background"></a><span data-ttu-id="6786e-110">Фон</span><span class="sxs-lookup"><span data-stu-id="6786e-110">Background</span></span>
<span data-ttu-id="6786e-111">Мы распространять дистрибутивов Linux для WSL как приложений универсальной платформы Windows с помощью Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="6786e-111">We distribute Linux distros for WSL as UWP applications through the Microsoft Store.</span></span> <span data-ttu-id="6786e-112">Вы можете установить эти приложения, которые будут выполняться на WSL - подсистема, которая размещается в ядре Windows.</span><span class="sxs-lookup"><span data-stu-id="6786e-112">You can install those applications that will then run on WSL - the subsystem that sits in the Windows kernel.</span></span> <span data-ttu-id="6786e-113">Этот механизм доставки имеет множество преимуществ, как описано в [более ранние записи блога](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/).</span><span class="sxs-lookup"><span data-stu-id="6786e-113">This delivery mechanism has many benefits as discussed in an [earlier blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/).</span></span>

## <a name="sideloading-a-custom-linux-distro-package"></a><span data-ttu-id="6786e-114">Для загрузки неопубликованных приложений пакета дистрибутив Linux, пользовательские</span><span class="sxs-lookup"><span data-stu-id="6786e-114">Sideloading a Custom Linux Distro Package</span></span>
<span data-ttu-id="6786e-115">Можно создать пользовательский пакет дистрибутив Linux как приложение для загрузки неопубликованных приложений на персональных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="6786e-115">You can create a custom Linux distro package as an application to sideload on your personal machine.</span></span> <span data-ttu-id="6786e-116">Обратите внимание на то, что пользовательский пакет бы не распространяется через Microsoft Store, если вы отправляете в виде распространения программы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="6786e-116">Please note that your custom package would not be distributed through the Microsoft Store unless you submit as a distribution maintainer.</span></span>
<span data-ttu-id="6786e-117">Чтобы настроить компьютер для загрузки неопубликованных приложений, необходимо включить отслеживание на системные параметры в разделе «Для разработчиков».</span><span class="sxs-lookup"><span data-stu-id="6786e-117">To set up your machine to sideload apps, you will need to enable this in the system settings under “For Developers”.</span></span>  <span data-ttu-id="6786e-118">Убедитесь, что иметь режим разработчика или выбрано загрузка неопубликованных приложений</span><span class="sxs-lookup"><span data-stu-id="6786e-118">Be sure to either have developer mode, or sideload apps selected</span></span>

## <a name="for-linux-distro-maintainers"></a><span data-ttu-id="6786e-119">Для дистрибутивов Linux издатели</span><span class="sxs-lookup"><span data-stu-id="6786e-119">For Linux Distro Maintainers</span></span>
<span data-ttu-id="6786e-120">Чтобы отправить Store, необходимо будет работать с нами, получившей публикации.</span><span class="sxs-lookup"><span data-stu-id="6786e-120">To submit to the Store, you will need to work with us to receive publishing approval.</span></span> <span data-ttu-id="6786e-121">Если вы являетесь владельцем распространения Linux заинтересован в добавлении распространения в Microsoft Store, обратитесь в службу wslpartners@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="6786e-121">If you are a Linux distribution owner interested in adding your distribution to the Microsoft Store, please contact wslpartners@microsoft.com.</span></span>

## <a name="getting-started"></a><span data-ttu-id="6786e-122">начало работы</span><span class="sxs-lookup"><span data-stu-id="6786e-122">Getting Started</span></span>
<span data-ttu-id="6786e-123">Следуйте инструкциям на [репозиторий GitHub запуска дистрибутива](https://github.com/Microsoft/WSL-DistroLauncher) для создания пользовательского пакета дистрибутива Linux.</span><span class="sxs-lookup"><span data-stu-id="6786e-123">Follow the instructions on the [Distro Launcher GitHub repo](https://github.com/Microsoft/WSL-DistroLauncher) to create a custom Linux distro package.</span></span>

 
## <a name="team-blogs"></a><span data-ttu-id="6786e-124">Блоги группы разработчиков</span><span class="sxs-lookup"><span data-stu-id="6786e-124">Team Blogs</span></span>
*  [<span data-ttu-id="6786e-125">Откройте Sourcing пример WSL для дистрибутивов Linux и дистрибутивы Linux Custom для загрузки неопубликованных приложений</span><span class="sxs-lookup"><span data-stu-id="6786e-125">Open Sourcing a WSL Sample for Linux Distribution Maintainers and Sideloading Custom Linux Distributions</span></span>](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
* [<span data-ttu-id="6786e-126">Блог командной строки</span><span class="sxs-lookup"><span data-stu-id="6786e-126">Command-Line blog</span></span>](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a><span data-ttu-id="6786e-127">Предоставление отзыва</span><span class="sxs-lookup"><span data-stu-id="6786e-127">Provide Feedback</span></span>
* [<span data-ttu-id="6786e-128">Репозитории дистрибутива запуска GitHub</span><span class="sxs-lookup"><span data-stu-id="6786e-128">Distro Launcher GitHub repo</span></span>](https://github.com/Microsoft/WSL-DistroLauncher)
* [<span data-ttu-id="6786e-129">Средство отслеживания вопросов GitHub для WSL</span><span class="sxs-lookup"><span data-stu-id="6786e-129">GitHub issue tracker for WSL</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="6786e-130">Командной строки портал UserVoice</span><span class="sxs-lookup"><span data-stu-id="6786e-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
