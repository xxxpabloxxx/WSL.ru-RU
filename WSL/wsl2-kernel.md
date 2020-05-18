---
title: Обновление ядра Linux в WSL 2
description: Инструкции по обновлению ядра Linux в WSL 2 вручную
keywords: WSL, Windows, ядро Linux, подсистема Windows для Linux, ядро
ms.date: 03/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 89e5755699938b7797aa65a5f3131f93e3e31796
ms.sourcegitcommit: e6e888f2b88a2d9c105cee46e5ab5b70aa43dd80
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/13/2020
ms.locfileid: "83343836"
---
# <a name="updating-the-wsl-2-linux-kernel"></a><span data-ttu-id="8d657-104">Обновление ядра Linux в WSL 2</span><span class="sxs-lookup"><span data-stu-id="8d657-104">Updating the WSL 2 Linux kernel</span></span>

<span data-ttu-id="8d657-105">Чтобы вручную обновить ядро Linux в WSL 2, выполните описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="8d657-105">To manually update the Linux kernel inside of WSL 2 please follow these steps.</span></span>

> [!NOTE] 
> <span data-ttu-id="8d657-106">Если установщику не удается найти WSL 1, щелкните правой кнопкой мыши установщик обновления ядра Linux, а затем нажмите кнопку "Удалить" и запустите установщик повторно.</span><span class="sxs-lookup"><span data-stu-id="8d657-106">If the installer cant find WSL 1 right click the Linux kernel update installer, then press uninstall then rerun the installer</span></span>

## <a name="download-the-linux-kernel-update-package"></a><span data-ttu-id="8d657-107">Скачивание пакета обновления ядра Linux</span><span class="sxs-lookup"><span data-stu-id="8d657-107">Download the Linux kernel update package</span></span>

<span data-ttu-id="8d657-108">[Скачайте последнюю версию пакета обновления ядра Linux в WSL 2](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) для 64-разрядных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="8d657-108">Please [download the latest WSL2 Linux kernel](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) update package for x64 machines.</span></span>

> [!NOTE]
> <span data-ttu-id="8d657-109">Если вы используете компьютер ARM64, вместо этого скачайте [пакет ARM64](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi).</span><span class="sxs-lookup"><span data-stu-id="8d657-109">If you're using an ARM64 machine, please download the [ARM64 package](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) instead.</span></span>

## <a name="install-the-linux-kernel-update-package"></a><span data-ttu-id="8d657-110">Установка пакета обновления ядра Linux</span><span class="sxs-lookup"><span data-stu-id="8d657-110">Install the Linux kernel update package</span></span>

<span data-ttu-id="8d657-111">Чтобы установить пакет обновления ядра Linux:</span><span class="sxs-lookup"><span data-stu-id="8d657-111">To install the Linux kernel update package:</span></span>

  1. <span data-ttu-id="8d657-112">Запустите пакет обновления, скачанный на предыдущем этапе.</span><span class="sxs-lookup"><span data-stu-id="8d657-112">Run the update package downloaded in the previous step.</span></span>

  2. <span data-ttu-id="8d657-113">Появится запрос на повышение уровня разрешений. Нажмите кнопку "Да", чтобы утвердить эту установку.</span><span class="sxs-lookup"><span data-stu-id="8d657-113">You will be prompted for elevated permissions, select ‘yes’ to approve this installation.</span></span>

  3. <span data-ttu-id="8d657-114">По завершении установки можно приступить к использованию WSL 2.</span><span class="sxs-lookup"><span data-stu-id="8d657-114">Once the installation is complete, you are ready to begin using WSL2!</span></span>

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a><span data-ttu-id="8d657-115">Дальнейшие планы по обновлению ядра Linux в WSL 2</span><span class="sxs-lookup"><span data-stu-id="8d657-115">Future plans for updating the WSL2 Linux kernel</span></span>

<span data-ttu-id="8d657-116">Дополнительные сведения см. в статье об [изменениях процесса установки обновления ядра Linux в WSL 2](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), доступной в блоге, [посвященному командной строке Windows](https://aka.ms/cliblog).</span><span class="sxs-lookup"><span data-stu-id="8d657-116">For more information, read the article [changes to updating the WSL2 Linux kernel](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), available on the [Windows Command Line Blog](https://aka.ms/cliblog).</span></span>
