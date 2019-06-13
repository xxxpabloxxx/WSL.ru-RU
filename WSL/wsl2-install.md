---
title: Установка WSL 2
description: Инструкции по установке WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, подсистема windows для linux, windowssubsystem, ubuntu, debian, suse, windows 10, установка
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 2af43a046333fc8c7b4142cdc5077cdfbf29fea7
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038084"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="67ea4-104">Инструкции по установке для WSL 2</span><span class="sxs-lookup"><span data-stu-id="67ea4-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="67ea4-105">Для установки и начать использовать WSL 2 выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="67ea4-105">To install and start using WSL 2 complete the following steps:</span></span>

- <span data-ttu-id="67ea4-106">Включить дополнительный компонент «Платформы виртуальной машины»</span><span class="sxs-lookup"><span data-stu-id="67ea4-106">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="67ea4-107">Установить дистрибутив, резервному WSL 2, с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="67ea4-107">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="67ea4-108">Проверка версии WSL вашей дистрибутивов, которые могут использовать</span><span class="sxs-lookup"><span data-stu-id="67ea4-108">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="67ea4-109">Включить дополнительный компонент «Платформы виртуальной машины»</span><span class="sxs-lookup"><span data-stu-id="67ea4-109">Enable the 'Virtual Machine Platform' optional component</span></span>

<span data-ttu-id="67ea4-110">Откройте PowerShell с правами администратора и выполните:</span><span class="sxs-lookup"><span data-stu-id="67ea4-110">Open PowerShell as an Administrator and run:</span></span>

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

<span data-ttu-id="67ea4-111">После включения этих изменений необходимо будет перезагрузить компьютер.</span><span class="sxs-lookup"><span data-stu-id="67ea4-111">After these changes are enabled you will need to restart your computer.</span></span>

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="67ea4-112">Установить дистрибутив, резервному WSL 2, с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="67ea4-112">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="67ea4-113">В PowerShell выполните:</span><span class="sxs-lookup"><span data-stu-id="67ea4-113">In PowerShell run:</span></span>

`wsl --set-version <Distro> 2`

<span data-ttu-id="67ea4-114">и не забудьте заменить `<Distro>` с фактическим именем вашего дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="67ea4-114">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="67ea4-115">(Их можно найти с помощью команды: `wsl -l`).</span><span class="sxs-lookup"><span data-stu-id="67ea4-115">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="67ea4-116">Можно изменить на 1 WSL в любое время, выполнив ту же команду, как описано выше, но замена "2" с "1".</span><span class="sxs-lookup"><span data-stu-id="67ea4-116">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="67ea4-117">Кроме того Если вы хотите сделать WSL 2 архитектуры по умолчанию это можно сделать с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="67ea4-117">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

`wsl --set-default-version 2`

<span data-ttu-id="67ea4-118">Это сделает любой новый дистрибутива, который вы устанавливаете следует инициализировать как дистрибутив WSL 2.</span><span class="sxs-lookup"><span data-stu-id="67ea4-118">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="67ea4-119">Завершение проверки версии WSL вашего дистрибутива, которые могут использовать</span><span class="sxs-lookup"><span data-stu-id="67ea4-119">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="67ea4-120">Чтобы проверить, какие версии дистрибутивов используется WSL используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="67ea4-120">To verify what versions of WSL each distro is using use the following command:</span></span>

<span data-ttu-id="67ea4-121">`wsl --list --verbose` или `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="67ea4-121">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="67ea4-122">Дистрибутив, который вы выбрали выше должно отображаться "2" в столбце «version».</span><span class="sxs-lookup"><span data-stu-id="67ea4-122">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="67ea4-123">Теперь, когда вы закончите, вы можете начать использовать вашего дистрибутива WSL 2!</span><span class="sxs-lookup"><span data-stu-id="67ea4-123">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 