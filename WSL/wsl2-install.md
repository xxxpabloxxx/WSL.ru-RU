---
title: Установка WSL 2
description: Инструкции по установке WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, подсистема Windows для Linux, windowssubsystem, ubuntu, debian, suse, windows 10, установка
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 8af5ffeffdeedc5298af8125cea5c7428c8f29f8
ms.sourcegitcommit: 3c9ebe5f9ef5fb64070e21b479c2f2d31243f310
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "74248764"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="322a1-104">Инструкции по установке WSL 2</span><span class="sxs-lookup"><span data-stu-id="322a1-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="322a1-105">Чтобы установить подсистему WSL 2 и начать с ней работу, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="322a1-105">To install and start using WSL 2 complete the following steps:</span></span>

> <span data-ttu-id="322a1-106">WSL 2 доступен только в сборках Windows 10 18917 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="322a1-106">WSL 2 is only available in Windows 10 builds 18917 or higher</span></span>

- <span data-ttu-id="322a1-107">Убедитесь, что установлен WSL (вы можете найти инструкции [здесь](./install-win10.md)) и вы используете Windows 10 **Build 18917** или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="322a1-107">Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 **build 18917** or higher</span></span>
   - <span data-ttu-id="322a1-108">Чтобы убедиться, что вы используете сборку 18917 или более позднюю версию, присоединитесь к [программе предварительной оценки Windows](https://insider.windows.com/en-us/) и выберите Быстрый звонок.</span><span class="sxs-lookup"><span data-stu-id="322a1-108">To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring.</span></span> 
   - <span data-ttu-id="322a1-109">Вы можете проверить версию Windows, открыв командную строку и выполнив команду `ver`.</span><span class="sxs-lookup"><span data-stu-id="322a1-109">You can check your Windows version by opening Command Prompt and running the `ver` command.</span></span>
- <span data-ttu-id="322a1-110">включите необязательный компонент "Virtual Machine Platform" (Платформа виртуальной машины);</span><span class="sxs-lookup"><span data-stu-id="322a1-110">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="322a1-111">с помощью командной строки задайте поддержку дистрибутива в WSL 2;</span><span class="sxs-lookup"><span data-stu-id="322a1-111">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="322a1-112">проверьте, какие версии WSL используют ваши дистрибутивы.</span><span class="sxs-lookup"><span data-stu-id="322a1-112">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a><span data-ttu-id="322a1-113">Включите дополнительный компонент "платформа виртуальной машины" и убедитесь, что WSL включен.</span><span class="sxs-lookup"><span data-stu-id="322a1-113">Enable the 'Virtual Machine Platform' optional component and make sure WSL is enabled</span></span>

<span data-ttu-id="322a1-114">Необходимо убедиться в том, что установлены как подсистемы Windows для Linux, так и дополнительные компоненты платформы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="322a1-114">You will need to make sure that you have both the Windows Subsystem for Linux and the Virtual Machine Platform optional components installed.</span></span> <span data-ttu-id="322a1-115">Это можно сделать, выполнив следующую команду в PowerShell:</span><span class="sxs-lookup"><span data-stu-id="322a1-115">You can do that by running the following command in PowerShell:</span></span> 

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

<span data-ttu-id="322a1-116">Перезагрузите компьютер, чтобы завершить установку обоих компонентов.</span><span class="sxs-lookup"><span data-stu-id="322a1-116">Please restart your machine to finish installing both components.</span></span>


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="322a1-117">с помощью командной строки задайте поддержку дистрибутива в WSL 2;</span><span class="sxs-lookup"><span data-stu-id="322a1-117">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="322a1-118">Если у вас нет дистрибутив Linux, ознакомьтесь с инструкциями по установке на странице документации по [установке на Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) .</span><span class="sxs-lookup"><span data-stu-id="322a1-118">If you do not have a Linux distro installed, please refer to the [Install on Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) docs page for instructions on installing one.</span></span> 

<span data-ttu-id="322a1-119">Чтобы задать дистрибутив, выполните команду:</span><span class="sxs-lookup"><span data-stu-id="322a1-119">To set a distro please run:</span></span> 

```
wsl --set-version <Distro> 2
```

<span data-ttu-id="322a1-120">Замените `<Distro>` фактическим именем дистрибутива</span><span class="sxs-lookup"><span data-stu-id="322a1-120">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="322a1-121">(узнать имя можно с помощью команды `wsl -l`).</span><span class="sxs-lookup"><span data-stu-id="322a1-121">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="322a1-122">Вы можете всегда вернуться к WSL версии 1, выполнив эту команду и заменив "2" на "1".</span><span class="sxs-lookup"><span data-stu-id="322a1-122">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="322a1-123">Кроме того, если вы хотите сделать WSL 2 архитектурой по умолчанию, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="322a1-123">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```
wsl --set-default-version 2`
```

<span data-ttu-id="322a1-124">Впоследствии все новые дистрибутивы после установки будут инициализированы как дистрибутивы WSL 2.</span><span class="sxs-lookup"><span data-stu-id="322a1-124">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="322a1-125">Проверка используемой дистрибутивом версии WSL</span><span class="sxs-lookup"><span data-stu-id="322a1-125">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="322a1-126">Чтобы проверить, какая версия WSL используется для каждого дистрибутив, используйте следующую команду (доступно только в Windows Build 18917 или более поздней версии):</span><span class="sxs-lookup"><span data-stu-id="322a1-126">To verify what versions of WSL each distro is using use the following command (only available in Windows Build 18917 or higher):</span></span>

<span data-ttu-id="322a1-127">`wsl --list --verbose` или `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="322a1-127">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="322a1-128">В дистрибутиве, который вы выбрали ранее, в столбце версии должно отображаться значение "2".</span><span class="sxs-lookup"><span data-stu-id="322a1-128">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="322a1-129">Теперь все готово к работе с дистрибутивом WSL 2.</span><span class="sxs-lookup"><span data-stu-id="322a1-129">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="322a1-130">Устранение неполадок:</span><span class="sxs-lookup"><span data-stu-id="322a1-130">Troubleshooting:</span></span> 

<span data-ttu-id="322a1-131">Ниже перечислены возможные ошибки при установке WSL 2 и способы их устранения</span><span class="sxs-lookup"><span data-stu-id="322a1-131">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="322a1-132">(дополнительные сведения см. в статье об [устранении неполадок с WSL](troubleshooting.md)):</span><span class="sxs-lookup"><span data-stu-id="322a1-132">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="322a1-133">**Сбой установки с ошибкой 0x80070003 или ошибкой 0x80370102.**</span><span class="sxs-lookup"><span data-stu-id="322a1-133">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="322a1-134">Убедитесь, что в BIOS вашего компьютера включена виртуализация.</span><span class="sxs-lookup"><span data-stu-id="322a1-134">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="322a1-135">Расположение этого параметра зависит от компьютера, но обычно он находится в разделе настроек ЦП в BIOS.</span><span class="sxs-lookup"><span data-stu-id="322a1-135">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="322a1-136">**При попытке обновления возникает ошибка `Invalid command line option: wsl --set-version Ubuntu 2`.**</span><span class="sxs-lookup"><span data-stu-id="322a1-136">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="322a1-137">Убедитесь, что у вас включена подсистема Windows для Linux и используется сборка Windows 10 18917 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="322a1-137">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="322a1-138">Чтобы включить WSL, выполните эту команду в командной строке PowerShell с правами администратора: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="322a1-138">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="322a1-139">Полную инструкцию по установке WSL см. [здесь](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="322a1-139">You can find the full WSL install instructions [here](./install-win10.md).</span></span>

* <span data-ttu-id="322a1-140">**Не удалось завершить запрошенную операцию из-за ограничения системы виртуальных дисков. Файлы виртуального жесткого диска должны быть несжатыми и незашифрованными и не должны быть разреженными.**</span><span class="sxs-lookup"><span data-stu-id="322a1-140">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
    * <span data-ttu-id="322a1-141">Проверьте [#4103 потока GitHub WSL](https://github.com/microsoft/WSL/issues/4103) , где эта проблема отслеживается для получения обновленной информации.</span><span class="sxs-lookup"><span data-stu-id="322a1-141">Please check [WSL Github thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>

* <span data-ttu-id="322a1-142">**Термин "WSL" не распознан как имя командлета, функции, файла скрипта или исполняемой программы.**</span><span class="sxs-lookup"><span data-stu-id="322a1-142">**The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.**</span></span> 
    * <span data-ttu-id="322a1-143">Убедитесь, что [установлен дополнительный компонент подсистемы Windows для Linux](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="322a1-143">Ensure that the [Windows Subsystem for Linux Optional Component is installed](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled).</span></span><br> <span data-ttu-id="322a1-144">Кроме того, если вы используете устройство Arm64 и выполняете эту команду из PowerShell, вы получите эту ошибку.</span><span class="sxs-lookup"><span data-stu-id="322a1-144">Additionally, if you are using an Arm64 device and running this command from PowerShell, you will receive this error.</span></span> <span data-ttu-id="322a1-145">Вместо этого запустите `wsl.exe` из [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6)или командной строки.</span><span class="sxs-lookup"><span data-stu-id="322a1-145">Instead run `wsl.exe` from [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6), or Command Prompt.</span></span> 