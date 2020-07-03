---
title: Заметки о выпуске подсистемы Windows для ядра Linux
description: Заметки о выпуске подсистемы Windows для Linux.  Обновляется ежемесячно.
keywords: заметки о выпуске, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, ядро
ms.date: 06/09/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: e2409fccada9077adbeac3843c31b8faa2c93208
ms.sourcegitcommit: f1b049a1276782d4f2754f46a8d2025b598a0784
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "85336057"
---
# <a name="release-notes-for-windows-subsystem-for-linux-kernel"></a><span data-ttu-id="c7cb7-105">Заметки о выпуске подсистемы Windows для ядра Linux</span><span class="sxs-lookup"><span data-stu-id="c7cb7-105">Release Notes for Windows Subsystem for Linux kernel</span></span>

<span data-ttu-id="c7cb7-106">Включена поддержка дистрибутивов WSL 2, [использующих полнофункциональное ядро Linux](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/).</span><span class="sxs-lookup"><span data-stu-id="c7cb7-106">We've added support for WSL 2 distributions, [which use a full Linux kernel](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/).</span></span> <span data-ttu-id="c7cb7-107">Это ядро Linux имеет открытый кодом. Исходный код доступен в репозитории [WSL2-Linux-Kernel](https://github.com/microsoft/WSL2-Linux-Kernel).</span><span class="sxs-lookup"><span data-stu-id="c7cb7-107">This Linux kernel is open source, with its source code available at the [WSL2-Linux-Kernel](https://github.com/microsoft/WSL2-Linux-Kernel) repository.</span></span> <span data-ttu-id="c7cb7-108">Это ядро Linux доставляется на компьютер через Центр обновления Майкрософт в соответствии с отдельным графиком выпуска подсистемы Windows для Linux (поставляется в составе образа Windows).</span><span class="sxs-lookup"><span data-stu-id="c7cb7-108">This Linux kernel is delivered to your machine via Microsoft Update, and follows a separate release schedule to the Windows Subsystem for Linux which is delivered as part of the Windows image.</span></span>

## <a name="419121-microsoft-standard"></a><span data-ttu-id="c7cb7-109">4.19.121-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="c7cb7-109">4.19.121-microsoft-standard</span></span>
<span data-ttu-id="c7cb7-110">*Дата выпуска:* Предварительный выпуск</span><span class="sxs-lookup"><span data-stu-id="c7cb7-110">*Release Date*: Prerelease</span></span>

<span data-ttu-id="c7cb7-111">[Официальная ссылка на выпуск GitHub.](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.121-microsoft-standard)</span><span class="sxs-lookup"><span data-stu-id="c7cb7-111">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.121-microsoft-standard).</span></span>

* <span data-ttu-id="c7cb7-112">Drivers: hv: vmbus: hook up dxgkrnl</span><span class="sxs-lookup"><span data-stu-id="c7cb7-112">Drivers: hv: vmbus: hook up dxgkrnl</span></span>
* <span data-ttu-id="c7cb7-113">Включена поддержка вычислений GPU</span><span class="sxs-lookup"><span data-stu-id="c7cb7-113">Added support for GPU Compute</span></span>

## <a name="419104-microsoft-standard"></a><span data-ttu-id="c7cb7-114">4.19.104-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="c7cb7-114">4.19.104-microsoft-standard</span></span>
<span data-ttu-id="c7cb7-115">*Дата выпуска:* 09.06.2020</span><span class="sxs-lookup"><span data-stu-id="c7cb7-115">*Release Date*: 06/09/2020</span></span> 

<span data-ttu-id="c7cb7-116">[Официальная ссылка на выпуск GitHub.](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.104-microsoft-standard)</span><span class="sxs-lookup"><span data-stu-id="c7cb7-116">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.104-microsoft-standard).</span></span>

* <span data-ttu-id="c7cb7-117">Обновление конфигурации WSL для выпуска 4.19.104</span><span class="sxs-lookup"><span data-stu-id="c7cb7-117">Update WSL config for 4.19.104</span></span>

## <a name="41984-microsoft-standard"></a><span data-ttu-id="c7cb7-118">4.19.84-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="c7cb7-118">4.19.84-microsoft-standard</span></span>
<span data-ttu-id="c7cb7-119">*Дата выпуска:* 12.11.2019</span><span class="sxs-lookup"><span data-stu-id="c7cb7-119">*Release Date*: 11/12/2019</span></span> 

<span data-ttu-id="c7cb7-120">[Официальная ссылка на выпуск GitHub.](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.84-microsoft-standard)</span><span class="sxs-lookup"><span data-stu-id="c7cb7-120">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.84-microsoft-standard).</span></span>

* <span data-ttu-id="c7cb7-121">Это стабильный выпуск 4.19.84</span><span class="sxs-lookup"><span data-stu-id="c7cb7-121">This is the 4.19.84 stable release</span></span>

