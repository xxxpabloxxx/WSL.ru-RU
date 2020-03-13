---
title: Обновление ядра Linux для WSL 2
description: Инструкции по обновлению ядра Linux для WSL 2 вручную
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, wsl.conf, wslconfig
ms.date: 03/12/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: edc7ea35d8ebe0c71488763017cde2bb45c53b6d
ms.sourcegitcommit: 8795e1c4c5d2efdc8a9c78af05fb7be3ac1eef3d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/12/2020
ms.locfileid: "79138193"
---
# <a name="updating-the-wsl-2-linux-kernel"></a><span data-ttu-id="c25e0-104">Обновление ядра Linux для WSL 2</span><span class="sxs-lookup"><span data-stu-id="c25e0-104">Updating the WSL 2 Linux kernel</span></span>

<span data-ttu-id="c25e0-105">Чтобы вручную обновить ядро Linux в WSL 2, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c25e0-105">To manually update the Linux kernel inside of WSL 2 please follow these steps.</span></span> 

## <a name="download-the-linux-kernel-update-package"></a><span data-ttu-id="c25e0-106">Загрузка пакета обновления ядра Linux</span><span class="sxs-lookup"><span data-stu-id="c25e0-106">Download the Linux kernel update package</span></span>

<span data-ttu-id="c25e0-107">Щелкните [эту ссылку](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) , чтобы скачать последнюю версию пакета обновления ядра Linux для WSL2 для компьютеров AMD64.</span><span class="sxs-lookup"><span data-stu-id="c25e0-107">Please click on [this link](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) to download the latest WSL2 Linux kernel update package for AMD64 machines.</span></span>

> [!NOTE] <span data-ttu-id="c25e0-108">Если вы используете компьютер ARM64, скачайте [Этот пакет](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) .</span><span class="sxs-lookup"><span data-stu-id="c25e0-108">if you're using an ARM64 machine, please download [this package](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) instead.</span></span>

## <a name="install-the-linux-kernel-update-package"></a><span data-ttu-id="c25e0-109">Установка пакета обновления ядра Linux</span><span class="sxs-lookup"><span data-stu-id="c25e0-109">Install the Linux kernel update package</span></span>

<span data-ttu-id="c25e0-110">Чтобы установить пакет обновления ядра Linux, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c25e0-110">To install the Linux kernel update package:</span></span>
    1. <span data-ttu-id="c25e0-111">Запустите пакет обновления, скачанный на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="c25e0-111">Run the update package downloaded in the previous step.</span></span>
    2. <span data-ttu-id="c25e0-112">Появится запрос на повышение прав, нажмите кнопку "Да", чтобы утвердить эту установку.</span><span class="sxs-lookup"><span data-stu-id="c25e0-112">You will be prompted for elevated permissions, select ‘yes’ to approve this installation.</span></span>
    3. <span data-ttu-id="c25e0-113">После завершения установки можно приступить к использованию WSL2!</span><span class="sxs-lookup"><span data-stu-id="c25e0-113">Once the installation is complete, you are ready to begin using WSL2!</span></span>

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a><span data-ttu-id="c25e0-114">Будущие планы обновления ядра Linux для WSL2</span><span class="sxs-lookup"><span data-stu-id="c25e0-114">Future plans for updating the WSL2 Linux kernel</span></span>

<span data-ttu-id="c25e0-115">Дополнительные сведения об этих изменениях см. в [этой записи блога](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) в [блоге командной строки Windows](https://aka.ms/cliblog).</span><span class="sxs-lookup"><span data-stu-id="c25e0-115">For more info on these changes, please read [this blog post](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) on the [Windows Command Line Blog](https://aka.ms/cliblog).</span></span>