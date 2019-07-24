---
title: Установка WSL 2
description: Инструкции по установке WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, подсистема Windows для Linux, windowssubsystem, ubuntu, debian, suse, windows 10, установка
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 3ad180ecc9deaa1566e9870700b26f82f631c7f1
ms.sourcegitcommit: 9ad7a54668f39677e9660186e4f5172ea2597e2b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2019
ms.locfileid: "68246867"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="badba-104">Инструкции по установке WSL 2</span><span class="sxs-lookup"><span data-stu-id="badba-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="badba-105">Чтобы установить подсистему WSL 2 и начать с ней работу, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="badba-105">To install and start using WSL 2 complete the following steps:</span></span>

- <span data-ttu-id="badba-106">включите необязательный компонент "Virtual Machine Platform" (Платформа виртуальной машины);</span><span class="sxs-lookup"><span data-stu-id="badba-106">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="badba-107">с помощью командной строки задайте поддержку дистрибутива в WSL 2;</span><span class="sxs-lookup"><span data-stu-id="badba-107">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="badba-108">проверьте, какие версии WSL используют ваши дистрибутивы.</span><span class="sxs-lookup"><span data-stu-id="badba-108">Verify what versions of WSL your distros are using</span></span>

<span data-ttu-id="badba-109">Обратите внимание, что для использования WSL 2 требуется сборка Windows 10 18917 или более поздней версии, а также предварительно установленная подсистема WSL (инструкцию по установке см. [здесь](./install-win10.md)).</span><span class="sxs-lookup"><span data-stu-id="badba-109">Please note that you'll need to be running Windows 10 build 18917 or higher to use WSL 2, and that you will need to have WSL already installed (you can find instructions to do so [here](./install-win10.md)).</span></span> 

## <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="badba-110">Включение необязательного компонента "Virtual Machine Platform" (Платформа виртуальной машины)</span><span class="sxs-lookup"><span data-stu-id="badba-110">Enable the 'Virtual Machine Platform' optional component</span></span>

<span data-ttu-id="badba-111">Запустите PowerShell с правами администратора и выполните такую команду:</span><span class="sxs-lookup"><span data-stu-id="badba-111">Open PowerShell as an Administrator and run:</span></span>

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

<span data-ttu-id="badba-112">Когда вы внесете эти изменения, нужно будет перезагрузить компьютер.</span><span class="sxs-lookup"><span data-stu-id="badba-112">After these changes are enabled you will need to restart your computer.</span></span>

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="badba-113">Настройка поддержки дистрибутива в WSL 2 с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="badba-113">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="badba-114">В PowerShell выполните такую команду:</span><span class="sxs-lookup"><span data-stu-id="badba-114">In PowerShell run:</span></span>

`wsl --set-version <Distro> 2`

<span data-ttu-id="badba-115">Замените `<Distro>` фактическим именем дистрибутива</span><span class="sxs-lookup"><span data-stu-id="badba-115">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="badba-116">(узнать имя можно с помощью команды `wsl -l`).</span><span class="sxs-lookup"><span data-stu-id="badba-116">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="badba-117">Вы можете всегда вернуться к WSL версии 1, выполнив эту команду и заменив "2" на "1".</span><span class="sxs-lookup"><span data-stu-id="badba-117">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="badba-118">Кроме того, если вы хотите сделать WSL 2 архитектурой по умолчанию, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="badba-118">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

`wsl --set-default-version 2`

<span data-ttu-id="badba-119">Впоследствии все новые дистрибутивы после установки будут инициализированы как дистрибутивы WSL 2.</span><span class="sxs-lookup"><span data-stu-id="badba-119">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="badba-120">Проверка используемой дистрибутивом версии WSL</span><span class="sxs-lookup"><span data-stu-id="badba-120">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="badba-121">Чтобы проверить, какие версии WSL использует каждый дистрибутив, выполните такую команду:</span><span class="sxs-lookup"><span data-stu-id="badba-121">To verify what versions of WSL each distro is using use the following command:</span></span>

<span data-ttu-id="badba-122">`wsl --list --verbose` или `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="badba-122">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="badba-123">В дистрибутиве, который вы выбрали ранее, в столбце версии должно отображаться значение "2".</span><span class="sxs-lookup"><span data-stu-id="badba-123">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="badba-124">Теперь все готово к работе с дистрибутивом WSL 2.</span><span class="sxs-lookup"><span data-stu-id="badba-124">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="badba-125">Устранение неполадок:</span><span class="sxs-lookup"><span data-stu-id="badba-125">Troubleshooting:</span></span> 

<span data-ttu-id="badba-126">Ниже перечислены возможные ошибки при установке WSL 2 и способы их устранения</span><span class="sxs-lookup"><span data-stu-id="badba-126">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="badba-127">(дополнительные сведения см. в статье об [устранении неполадок с WSL](troubleshooting.md)):</span><span class="sxs-lookup"><span data-stu-id="badba-127">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="badba-128">**Сбой установки с ошибкой 0x80070003 или ошибкой 0x80370102.**</span><span class="sxs-lookup"><span data-stu-id="badba-128">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="badba-129">Убедитесь, что в BIOS вашего компьютера включена виртуализация.</span><span class="sxs-lookup"><span data-stu-id="badba-129">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="badba-130">Расположение этого параметра зависит от компьютера, но обычно он находится в разделе настроек ЦП в BIOS.</span><span class="sxs-lookup"><span data-stu-id="badba-130">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="badba-131">**При попытке обновления возникает ошибка `Invalid command line option: wsl --set-version Ubuntu 2`.**</span><span class="sxs-lookup"><span data-stu-id="badba-131">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="badba-132">Убедитесь, что у вас включена подсистема Windows для Linux и используется сборка Windows 10 18917 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="badba-132">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="badba-133">Чтобы включить WSL, выполните эту команду в командной строке PowerShell с правами администратора: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="badba-133">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="badba-134">Полную инструкцию по установке WSL см. [здесь](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="badba-134">You can find the full WSL install instructions [here](./install-win10.md).</span></span>