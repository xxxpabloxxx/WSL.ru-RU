---
title: Установка WSL 2
description: Инструкции по установке WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, подсистема Windows для Linux, windowssubsystem, ubuntu, debian, suse, windows 10, установка
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 91bd479e922fc29bf11b89dcfe06fa381632c4fa
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520553"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="0054e-104">Инструкции по установке WSL 2</span><span class="sxs-lookup"><span data-stu-id="0054e-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="0054e-105">Просмотрите приведенное ниже видео или изучите эту статью, чтобы узнать, как установить WSL 2.</span><span class="sxs-lookup"><span data-stu-id="0054e-105">You can watch the video below, or read on in this article to learn how to install WSL2.</span></span> 

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Learn-how-to-install-WSL-2/player]

<span data-ttu-id="0054e-106">Чтобы установить подсистему WSL 2 и начать с ней работу, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="0054e-106">To install and start using WSL 2 complete the following steps:</span></span>

> <span data-ttu-id="0054e-107">Подсистема WSL 2 доступна только в Windows 10 сборки 18917 или выше.</span><span class="sxs-lookup"><span data-stu-id="0054e-107">WSL 2 is only available in Windows 10 builds 18917 or higher</span></span>

- <span data-ttu-id="0054e-108">Убедитесь, что установлено WSL (инструкции по установке см. [здесь](./install-win10.md)) и что вы используете Windows 10 **сборки 18917** или выше.</span><span class="sxs-lookup"><span data-stu-id="0054e-108">Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 **build 18917** or higher</span></span>
   - <span data-ttu-id="0054e-109">Чтобы убедиться, что вы используете сборку 18917 или выше, присоединитесь к [программе предварительной оценки Windows](https://insider.windows.com/en-us/) и выберите круг раннего или позднего доступа.</span><span class="sxs-lookup"><span data-stu-id="0054e-109">To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring or the 'Slow' ring.</span></span> 
   - <span data-ttu-id="0054e-110">Вы можете проверить версию Windows, открыв командную строку и выполнив команду `ver`.</span><span class="sxs-lookup"><span data-stu-id="0054e-110">You can check your Windows version by opening Command Prompt and running the `ver` command.</span></span>
- <span data-ttu-id="0054e-111">Включение необязательного компонента "Virtual Machine Platform" (Платформа виртуальной машины)</span><span class="sxs-lookup"><span data-stu-id="0054e-111">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="0054e-112">с помощью командной строки задайте поддержку дистрибутива в WSL 2;</span><span class="sxs-lookup"><span data-stu-id="0054e-112">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="0054e-113">проверьте, какие версии WSL используют ваши дистрибутивы.</span><span class="sxs-lookup"><span data-stu-id="0054e-113">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a><span data-ttu-id="0054e-114">Включение дополнительного компонента Virtual Machine Platform (Платформа виртуальной машины) и подтверждение включения WSL</span><span class="sxs-lookup"><span data-stu-id="0054e-114">Enable the 'Virtual Machine Platform' optional component and make sure WSL is enabled</span></span>

<span data-ttu-id="0054e-115">Убедиться, что установлены дополнительные компоненты подсистемы Windows для Linux и Virtual Machine Platform (Платформа виртуальной машины).</span><span class="sxs-lookup"><span data-stu-id="0054e-115">You will need to make sure that you have both the Windows Subsystem for Linux and the Virtual Machine Platform optional components installed.</span></span> <span data-ttu-id="0054e-116">Это можно сделать, выполнив следующую команду в PowerShell:</span><span class="sxs-lookup"><span data-stu-id="0054e-116">You can do that by running the following command in PowerShell:</span></span> 

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

<span data-ttu-id="0054e-117">Перезагрузите компьютер, чтобы завершить установку обоих компонентов.</span><span class="sxs-lookup"><span data-stu-id="0054e-117">Please restart your machine to finish installing both components.</span></span>


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="0054e-118">Настройка поддержки дистрибутива в WSL 2 с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="0054e-118">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="0054e-119">Если у вас не установлен дистрибутив Linux, ознакомьтесь с инструкциями по установке Windows 10 на [этой странице](./install-win10.md#install-your-linux-distribution-of-choice).</span><span class="sxs-lookup"><span data-stu-id="0054e-119">If you do not have a Linux distro installed, please refer to the [Install on Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) docs page for instructions on installing one.</span></span> 

<span data-ttu-id="0054e-120">Чтобы задать дистрибутив, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0054e-120">To set a distro please run:</span></span> 

```
wsl --set-version <Distro> 2
```

<span data-ttu-id="0054e-121">Замените `<Distro>` фактическим именем дистрибутива</span><span class="sxs-lookup"><span data-stu-id="0054e-121">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="0054e-122">(узнать имя можно с помощью команды `wsl -l`).</span><span class="sxs-lookup"><span data-stu-id="0054e-122">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="0054e-123">Вы можете всегда вернуться к WSL версии 1, выполнив эту команду и заменив "2" на "1".</span><span class="sxs-lookup"><span data-stu-id="0054e-123">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="0054e-124">Кроме того, если вы хотите сделать WSL 2 архитектурой по умолчанию, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0054e-124">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```
wsl --set-default-version 2
```

<span data-ttu-id="0054e-125">Впоследствии все новые дистрибутивы после установки будут инициализированы как дистрибутивы WSL 2.</span><span class="sxs-lookup"><span data-stu-id="0054e-125">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="0054e-126">Проверка используемой дистрибутивом версии WSL</span><span class="sxs-lookup"><span data-stu-id="0054e-126">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="0054e-127">Чтобы проверить, какие версии WSL использует каждый дистрибутив, выполните приведенную ниже команду (доступную только в Windows сборки 18917 или более поздней версии):</span><span class="sxs-lookup"><span data-stu-id="0054e-127">To verify what versions of WSL each distro is using use the following command (only available in Windows Build 18917 or higher):</span></span>

<span data-ttu-id="0054e-128">`wsl --list --verbose` или `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="0054e-128">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="0054e-129">В дистрибутиве, который вы выбрали ранее, в столбце версии должно отображаться значение "2".</span><span class="sxs-lookup"><span data-stu-id="0054e-129">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="0054e-130">Теперь все готово к работе с дистрибутивом WSL 2.</span><span class="sxs-lookup"><span data-stu-id="0054e-130">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="0054e-131">Устранение неполадок:</span><span class="sxs-lookup"><span data-stu-id="0054e-131">Troubleshooting:</span></span> 

<span data-ttu-id="0054e-132">Ниже перечислены возможные ошибки при установке WSL 2 и способы их устранения</span><span class="sxs-lookup"><span data-stu-id="0054e-132">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="0054e-133">(дополнительные сведения см. в статье об [устранении неполадок с WSL](troubleshooting.md)):</span><span class="sxs-lookup"><span data-stu-id="0054e-133">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="0054e-134">**Сбой установки с ошибкой 0x80070003 или ошибкой 0x80370102.**</span><span class="sxs-lookup"><span data-stu-id="0054e-134">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="0054e-135">Убедитесь, что в BIOS вашего компьютера включена виртуализация.</span><span class="sxs-lookup"><span data-stu-id="0054e-135">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="0054e-136">Расположение этого параметра зависит от компьютера, но обычно он находится в разделе настроек ЦП в BIOS.</span><span class="sxs-lookup"><span data-stu-id="0054e-136">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="0054e-137">**При попытке обновления возникает ошибка `Invalid command line option: wsl --set-version Ubuntu 2`.**</span><span class="sxs-lookup"><span data-stu-id="0054e-137">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="0054e-138">Убедитесь, что у вас включена подсистема Windows для Linux и используется сборка Windows 10 18917 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="0054e-138">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="0054e-139">Чтобы включить WSL, выполните эту команду в командной строке PowerShell с правами администратора: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="0054e-139">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="0054e-140">Полную инструкцию по установке WSL см. [здесь](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="0054e-140">You can find the full WSL install instructions [here](./install-win10.md).</span></span>

* <span data-ttu-id="0054e-141">**Запрошенную операцию не удалось выполнить из-за ограничения системы виртуального диска. Файлы виртуального жесткого диска должны быть распакованными, незашифрованными и не разреженными.**</span><span class="sxs-lookup"><span data-stu-id="0054e-141">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
    * <span data-ttu-id="0054e-142">Чтобы получить обновленные сведения, проверьте [поток GitHub WSL #4103](https://github.com/microsoft/WSL/issues/4103), где отслеживается эта проблема.</span><span class="sxs-lookup"><span data-stu-id="0054e-142">Please check [WSL Github thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>

* <span data-ttu-id="0054e-143">**Термин WSL не распознан как имя командлета, функции, файла скрипта или действующей программы.**</span><span class="sxs-lookup"><span data-stu-id="0054e-143">**The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.**</span></span> 
    * <span data-ttu-id="0054e-144">Убедитесь, что установлен дополнительный компонент [Подсистема Windows для Linux](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="0054e-144">Ensure that the [Windows Subsystem for Linux Optional Component is installed](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled).</span></span><br> <span data-ttu-id="0054e-145">Кроме того, если вы используете устройство Arm64 и выполняете эту команду в PowerShell, вы получите эту ошибку.</span><span class="sxs-lookup"><span data-stu-id="0054e-145">Additionally, if you are using an Arm64 device and running this command from PowerShell, you will receive this error.</span></span> <span data-ttu-id="0054e-146">Вместо этого запустите `wsl.exe` из [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6) или командной строки.</span><span class="sxs-lookup"><span data-stu-id="0054e-146">Instead run `wsl.exe` from [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6), or Command Prompt.</span></span> 
