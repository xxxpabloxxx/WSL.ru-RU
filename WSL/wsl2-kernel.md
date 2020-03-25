---
title: Обновление ядра Linux в WSL 2
description: Инструкции по обновлению ядра Linux в WSL 2 вручную
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, wsl.conf, wslconfig
ms.date: 03/12/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.localizationpriority: high
ms.custom: seodec18
ms.openlocfilehash: a1a2f23fb05c426f80878e12e82026a96c71354e
ms.sourcegitcommit: 4b7b8bb0ac20c2336fcdbf44e6b3b2ed336bf4d6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/17/2020
ms.locfileid: "79447741"
---
# <a name="updating-the-wsl-2-linux-kernel"></a><span data-ttu-id="15d2f-104">Обновление ядра Linux в WSL 2</span><span class="sxs-lookup"><span data-stu-id="15d2f-104">Updating the WSL 2 Linux kernel</span></span>

<span data-ttu-id="15d2f-105">Чтобы вручную обновить ядро Linux в WSL 2, выполните описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="15d2f-105">To manually update the Linux kernel inside of WSL 2 please follow these steps.</span></span> 

## <a name="download-the-linux-kernel-update-package"></a><span data-ttu-id="15d2f-106">Скачивание пакета обновления ядра Linux</span><span class="sxs-lookup"><span data-stu-id="15d2f-106">Download the Linux kernel update package</span></span>

<span data-ttu-id="15d2f-107">Щелкните [эту ссылку](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi), чтобы скачать последнюю версию пакета обновления ядра Linux в WSL 2 для компьютеров x64.</span><span class="sxs-lookup"><span data-stu-id="15d2f-107">Please click on [this link](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) to download the latest WSL2 Linux kernel update package for x64 machines.</span></span>

> [!NOTE] 
> <span data-ttu-id="15d2f-108">Если вы используете компьютер ARM64, вместо этого скачайте [этот пакет](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi).</span><span class="sxs-lookup"><span data-stu-id="15d2f-108">If you're using an ARM64 machine, please download [this package](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) instead.</span></span>

## <a name="install-the-linux-kernel-update-package"></a><span data-ttu-id="15d2f-109">Установка пакета обновления ядра Linux</span><span class="sxs-lookup"><span data-stu-id="15d2f-109">Install the Linux kernel update package</span></span>

<span data-ttu-id="15d2f-110">Чтобы установить пакет обновления ядра Linux:</span><span class="sxs-lookup"><span data-stu-id="15d2f-110">To install the Linux kernel update package:</span></span>

    1. <span data-ttu-id="15d2f-111">Запустите пакет обновления, скачанный на предыдущем этапе.</span><span class="sxs-lookup"><span data-stu-id="15d2f-111">Run the update package downloaded in the previous step.</span></span>
    2. <span data-ttu-id="15d2f-112">Появится запрос на повышение уровня разрешений. Нажмите кнопку "Да", чтобы утвердить эту установку.</span><span class="sxs-lookup"><span data-stu-id="15d2f-112">You will be prompted for elevated permissions, select ‘yes’ to approve this installation.</span></span>
    3. <span data-ttu-id="15d2f-113">По завершении установки можно приступить к использованию WSL 2.</span><span class="sxs-lookup"><span data-stu-id="15d2f-113">Once the installation is complete, you are ready to begin using WSL2!</span></span>

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a><span data-ttu-id="15d2f-114">Дальнейшие планы по обновлению ядра Linux в WSL 2</span><span class="sxs-lookup"><span data-stu-id="15d2f-114">Future plans for updating the WSL2 Linux kernel</span></span>

<span data-ttu-id="15d2f-115">Дополнительные сведения об этих изменениях см. в [этой записи](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) блога, посвященного [командной строке Windows](https://aka.ms/cliblog).</span><span class="sxs-lookup"><span data-stu-id="15d2f-115">For more info on these changes, please read [this blog post](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) on the [Windows Command Line Blog](https://aka.ms/cliblog).</span></span>
