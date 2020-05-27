---
title: Установка подсистемы Windows для Linux (WSL) в Windows 10
description: Инструкции по установке подсистемы Windows для Linux в Windows 10.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, debian, suse, windows 10, установка, включить, WSL2, версия 2
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: ec24bbe6ed3ecc4413e623d12d12f9a92c6db9e6
ms.sourcegitcommit: f0b33cdd1ce7b461e7f657d44e9798094ef55b55
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/20/2020
ms.locfileid: "83683029"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="4c084-104">Руководство по установке подсистемы Windows для Linux в Windows 10</span><span class="sxs-lookup"><span data-stu-id="4c084-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="4c084-105">Установка подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="4c084-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="4c084-106">Перед установкой дистрибутивов Linux в Windows необходимо включить дополнительный компонент "Подсистема Windows для Linux".</span><span class="sxs-lookup"><span data-stu-id="4c084-106">Before installing any Linux distributions on Windows, you must enable the "Windows Subsystem for Linux" optional feature.</span></span>

<span data-ttu-id="4c084-107">Запустите PowerShell с правами администратора и выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="4c084-107">Open PowerShell as Administrator and run:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

<span data-ttu-id="4c084-108">Чтобы установить только WSL 1, необходимо перезагрузить компьютер и перейти к пункту [Install your Linux distribution of choice](./install-win10.md#install-your-linux-distribution-of-choice) (Установить дистрибутив Linux), в противном случае дождитесь перезапуска и переходите к обновлению до WSL 2.</span><span class="sxs-lookup"><span data-stu-id="4c084-108">To only install WSL 1, you should now restart your machine and move on to [Install your Linux distribution of choice](./install-win10.md#install-your-linux-distribution-of-choice), otherwise wait to restart and move on to update to WSL 2.</span></span> <span data-ttu-id="4c084-109">Узнайте больше о [сравнении WSL 2 и WSL 1](./compare-versions.md).</span><span class="sxs-lookup"><span data-stu-id="4c084-109">Read more about [Comparing WSL 2 and WSL 1](./compare-versions.md).</span></span>

## <a name="update-to-wsl-2"></a><span data-ttu-id="4c084-110">Обновление до WSL 2</span><span class="sxs-lookup"><span data-stu-id="4c084-110">Update to WSL 2</span></span>

<span data-ttu-id="4c084-111">Чтобы выполнить обновление до WSL 2, необходимо выполнить следующие условия:</span><span class="sxs-lookup"><span data-stu-id="4c084-111">To update to WSL 2, you must meet the follow criteria:</span></span>

- <span data-ttu-id="4c084-112">Использовать Windows 10 с [обновлением до версии 2004](ms-settings:windowsupdate), **сборкой 19041** или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="4c084-112">Running Windows 10, [updated to version 2004](ms-settings:windowsupdate), **Build 19041** or higher.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4c084-113">Сейчас для обновления до Windows 10 версии 2004 (сборка 19041) потребуется [присоединиться к Программе предварительной оценки Windows](https://insider.windows.com/insidersigninboth/) и выбрать круг Release Preview.</span><span class="sxs-lookup"><span data-stu-id="4c084-113">Currently to update to Windows 10, version 2004 (Build 19041), you will need to [join the Windows Insider program](https://insider.windows.com/insidersigninboth/) and select the "Release Preview" ring.</span></span> <span data-ttu-id="4c084-114">Общедоступный выпуск должен появиться в конце мая.</span><span class="sxs-lookup"><span data-stu-id="4c084-114">The public release should arrive by late May.</span></span>

- <span data-ttu-id="4c084-115">Проверьте версию Windows, нажав **Windows + R**, введите **winver**, выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="4c084-115">Check your Windows version by selecting the **Windows logo key + R**, type **winver**, select **OK**.</span></span> <span data-ttu-id="4c084-116">(Или введите команду `ver` в командной строке Windows).</span><span class="sxs-lookup"><span data-stu-id="4c084-116">(Or enter the `ver` command in Windows Command Prompt).</span></span> <span data-ttu-id="4c084-117">[Обновите последнюю версию Windows](ms-settings:windowsupdate), если сборка ниже 19041.</span><span class="sxs-lookup"><span data-stu-id="4c084-117">Please [update to the latest Windows version](ms-settings:windowsupdate) if your build is lower than 19041.</span></span> <span data-ttu-id="4c084-118">[Получите помощник по Центру обновления Windows](https://www.microsoft.com/software-download/windows10).</span><span class="sxs-lookup"><span data-stu-id="4c084-118">[Get Windows Update Assistant](https://www.microsoft.com/software-download/windows10).</span></span>

### <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="4c084-119">Включение необязательного компонента "Virtual Machine Platform" (Платформа виртуальной машины)</span><span class="sxs-lookup"><span data-stu-id="4c084-119">Enable the 'Virtual Machine Platform' optional component</span></span>

<span data-ttu-id="4c084-120">Перед установкой WSL 2 необходимо включить необязательный компонент "Virtual Machine Platform" (Платформа виртуальных машин).</span><span class="sxs-lookup"><span data-stu-id="4c084-120">Before installing WSL 2, you must enable the "Virtual Machine Platform" optional feature.</span></span>

<span data-ttu-id="4c084-121">Запустите PowerShell с правами администратора и выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="4c084-121">Open PowerShell as Administrator and run:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

<span data-ttu-id="4c084-122">**Перезапустите** компьютер, чтобы завершить установку и обновление WSL до WSL 2.</span><span class="sxs-lookup"><span data-stu-id="4c084-122">**Restart** your machine to complete the WSL install and update to WSL 2.</span></span>

### <a name="set-wsl-2-as-your-default-version"></a><span data-ttu-id="4c084-123">Задать WSL 2 в качестве версии по умолчанию</span><span class="sxs-lookup"><span data-stu-id="4c084-123">Set WSL 2 as your default version</span></span>

<span data-ttu-id="4c084-124">Выполните следующую команду в PowerShell, чтобы задать WSL 2 в качестве версии по умолчанию при установке нового дистрибутива Linux:</span><span class="sxs-lookup"><span data-stu-id="4c084-124">Run the following command in Powershell to set WSL 2 as the default version when installing a new Linux distribution:</span></span>

```powershell
wsl --set-default-version 2
```

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="4c084-125">Установка дистрибутива Linux по выбору</span><span class="sxs-lookup"><span data-stu-id="4c084-125">Install your Linux distribution of choice</span></span>

1. <span data-ttu-id="4c084-126">Откройте [Microsoft Store](https://aka.ms/wslstore) и выберите предпочтительный дистрибутив Linux.</span><span class="sxs-lookup"><span data-stu-id="4c084-126">Open the [Microsoft Store](https://aka.ms/wslstore) and select your favorite Linux distribution.</span></span>

    ![Представление дистрибутивов Linux в Microsoft Store](media/store.png)

    <span data-ttu-id="4c084-128">Ниже приведены ссылки на страницы Microsoft Store для каждого дистрибутива:</span><span class="sxs-lookup"><span data-stu-id="4c084-128">The following links will open the Microsoft store page for each distribution:</span></span>

    - [<span data-ttu-id="4c084-129">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="4c084-129">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [<span data-ttu-id="4c084-130">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="4c084-130">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [<span data-ttu-id="4c084-131">openSUSE Leap 15.1</span><span class="sxs-lookup"><span data-stu-id="4c084-131">openSUSE Leap 15.1</span></span>](https://www.microsoft.com/store/apps/9NJFZK00FGKV)
    - [<span data-ttu-id="4c084-132">SUSE Linux Enterprise Server 12 SP5</span><span class="sxs-lookup"><span data-stu-id="4c084-132">SUSE Linux Enterprise Server 12 SP5</span></span>](https://www.microsoft.com/store/apps/9MZ3D1TRP8T1)
    - [<span data-ttu-id="4c084-133">SUSE Linux Enterprise Server 15 SP1</span><span class="sxs-lookup"><span data-stu-id="4c084-133">SUSE Linux Enterprise Server 15 SP1</span></span>](https://www.microsoft.com/store/apps/9PN498VPMF3Z)
    - [<span data-ttu-id="4c084-134">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="4c084-134">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [<span data-ttu-id="4c084-135">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="4c084-135">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [<span data-ttu-id="4c084-136">Fedora Remix for WSL</span><span class="sxs-lookup"><span data-stu-id="4c084-136">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [<span data-ttu-id="4c084-137">Pengwin</span><span class="sxs-lookup"><span data-stu-id="4c084-137">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [<span data-ttu-id="4c084-138">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="4c084-138">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [<span data-ttu-id="4c084-139">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="4c084-139">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

2. <span data-ttu-id="4c084-140">На странице дистрибутива щелкните "Получить".</span><span class="sxs-lookup"><span data-stu-id="4c084-140">From the distribution's page, select "Get".</span></span>

    ![Дистрибутивы Linux в Microsoft Store](media/UbuntuStore.png)

## <a name="set-up-a-new-distribution"></a><span data-ttu-id="4c084-142">Настройка нового дистрибутива</span><span class="sxs-lookup"><span data-stu-id="4c084-142">Set up a new distribution</span></span>

<span data-ttu-id="4c084-143">При первом запуске недавно установленного дистрибутива Linux откроется окно консоли, и вам будет предложено подождать минуту или две, чтобы файлы распаковались и сохранились на компьютере.</span><span class="sxs-lookup"><span data-stu-id="4c084-143">The first time you launch a newly installed Linux distribution, a console window will open and you'll be asked to wait for a minute or two for files to de-compress and be stored on your PC.</span></span> <span data-ttu-id="4c084-144">Все будущие запуски должны занимать меньше секунды.</span><span class="sxs-lookup"><span data-stu-id="4c084-144">All future launches should take less than a second.</span></span>

<span data-ttu-id="4c084-145">Затем необходимо будет [создать учетную запись пользователя и пароль для нового дистрибутива Linux](./user-support.md).</span><span class="sxs-lookup"><span data-stu-id="4c084-145">You will then need to [create a user account and password for your new Linux distribution](./user-support.md).</span></span>

![Распаковка Ubuntu в консоли Windows](media/UbuntuInstall.png)

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a><span data-ttu-id="4c084-147">Установите вашу версию дистрибутива на WSL 1 или WSL 2</span><span class="sxs-lookup"><span data-stu-id="4c084-147">Set your distribution version to WSL 1 or WSL 2</span></span>

<span data-ttu-id="4c084-148">Вы можете проверить версию WSL, назначенную каждому из установленных дистрибутивов Linux, открыв командную строку PowerShell и введя команду (доступна только в [сборке Windows 19041](ms-settings:windowsupdate) или более поздней версии): `wsl -l -v`.</span><span class="sxs-lookup"><span data-stu-id="4c084-148">You can check the WSL version assigned to each of the Linux distributions you have installed by opening the PowerShell command line and entering the command (only available in [Windows Build 19041 or higher](ms-settings:windowsupdate)): `wsl -l -v`</span></span>

```powershell
wsl --list --verbose
```

<span data-ttu-id="4c084-149">Чтобы настроить дистрибутив для одной из версий WSL, выполните:</span><span class="sxs-lookup"><span data-stu-id="4c084-149">To set a distribution to be backed by either version of WSL please run:</span></span>

```powershell
wsl --set-version <distribution name> <versionNumber>
```

<span data-ttu-id="4c084-150">Не забудьте заменить `<distribution name>` на фактическое имя дистрибутива и `<versionNumber>` с номером "1" или "2".</span><span class="sxs-lookup"><span data-stu-id="4c084-150">Make sure to replace `<distribution name>` with the actual name of your distribution and `<versionNumber>` with the number '1' or '2'.</span></span> <span data-ttu-id="4c084-151">Вы можете всегда вернуться к WSL версии 1, выполнив эту команду и заменив "2" на "1".</span><span class="sxs-lookup"><span data-stu-id="4c084-151">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="4c084-152">Кроме того, если вы хотите сделать WSL 2 архитектурой по умолчанию, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="4c084-152">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```powershell
wsl --set-default-version 2
```

<span data-ttu-id="4c084-153">Будет установлена версия любого нового дистрибутива, установленного в WSL 2.</span><span class="sxs-lookup"><span data-stu-id="4c084-153">This will set the version of any new distribution installed to WSL 2.</span></span>

## <a name="troubleshooting-installation"></a><span data-ttu-id="4c084-154">Устранение неполадок установки</span><span class="sxs-lookup"><span data-stu-id="4c084-154">Troubleshooting installation</span></span>

<span data-ttu-id="4c084-155">Ниже перечислены возможные ошибки и способы их устранения.</span><span class="sxs-lookup"><span data-stu-id="4c084-155">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="4c084-156">Другие распространенные ошибки и способы их устранения приведены в разделе [Устранение неполадок подсистемы Windows для Linux](troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="4c084-156">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

- <span data-ttu-id="4c084-157">**Сбой установки с ошибкой 0x80070003**</span><span class="sxs-lookup"><span data-stu-id="4c084-157">**Installation failed with error 0x80070003**</span></span>
  - <span data-ttu-id="4c084-158">Подсистема Windows для Linux работает только на системном диске (обычно это диск `C:`).</span><span class="sxs-lookup"><span data-stu-id="4c084-158">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="4c084-159">Убедитесь, что дистрибутивы хранятся на системном диске.</span><span class="sxs-lookup"><span data-stu-id="4c084-159">Make sure that distributions are stored on your system drive:</span></span>  
  - <span data-ttu-id="4c084-160">Выберите **Параметры** -> **Хранилище** -> **More Storage Settings: (Другие параметры хранилища:) Изменить место сохранения нового содержимого**.
    ![Изображение параметров системы для установки приложений на диске C:](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="4c084-160">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>

- <span data-ttu-id="4c084-161">**Сбой WslRegisterDistribution с ошибкой 0x8007019e**</span><span class="sxs-lookup"><span data-stu-id="4c084-161">**WslRegisterDistribution failed with error 0x8007019e**</span></span>
  - <span data-ttu-id="4c084-162">Дополнительный компонент "Подсистема Windows для Linux" не включен.</span><span class="sxs-lookup"><span data-stu-id="4c084-162">The Windows Subsystem for Linux optional component is not enabled:</span></span>
  - <span data-ttu-id="4c084-163">Выберите **Панель управления** -> **Программы и компоненты** -> **Включение или отключение компонентов Windows** и установите флажок **Подсистема Windows для Linux** или используйте командлет PowerShell, упомянутый в начале этой статьи.</span><span class="sxs-lookup"><span data-stu-id="4c084-163">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>

- <span data-ttu-id="4c084-164">**Сбой установки с ошибкой 0x80070003 или ошибкой 0x80370102.**</span><span class="sxs-lookup"><span data-stu-id="4c084-164">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
  - <span data-ttu-id="4c084-165">Убедитесь, что в BIOS вашего компьютера включена виртуализация.</span><span class="sxs-lookup"><span data-stu-id="4c084-165">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="4c084-166">Расположение этого параметра зависит от компьютера, но обычно он находится в разделе настроек ЦП в BIOS.</span><span class="sxs-lookup"><span data-stu-id="4c084-166">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>

- <span data-ttu-id="4c084-167">**При попытке обновления возникает ошибка `Invalid command line option: wsl --set-version Ubuntu 2`.**</span><span class="sxs-lookup"><span data-stu-id="4c084-167">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
  - <span data-ttu-id="4c084-168">Убедитесь, что у вас включена подсистема Windows для Linux и используется сборка Windows 19041 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="4c084-168">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 19041 or higher.</span></span> <span data-ttu-id="4c084-169">Чтобы включить WSL, выполните эту команду в командной строке PowerShell с правами администратора: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="4c084-169">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="4c084-170">Полную инструкцию по установке WSL см. [здесь](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="4c084-170">You can find the full WSL install instructions [here](./install-win10.md).</span></span>

- <span data-ttu-id="4c084-171">**Запрошенную операцию не удалось выполнить из-за ограничения системы виртуального диска. Файлы виртуального жесткого диска должны быть распакованными, незашифрованными и не разреженными.**</span><span class="sxs-lookup"><span data-stu-id="4c084-171">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
  - <span data-ttu-id="4c084-172">Чтобы получить обновленные сведения, проверьте [поток GitHub WSL #4103](https://github.com/microsoft/WSL/issues/4103), где отслеживается эта проблема.</span><span class="sxs-lookup"><span data-stu-id="4c084-172">Please check [WSL Github thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>

- <span data-ttu-id="4c084-173">**Термин WSL не распознан как имя командлета, функции, файла скрипта или действующей программы.**</span><span class="sxs-lookup"><span data-stu-id="4c084-173">**The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.**</span></span>
  - <span data-ttu-id="4c084-174">Убедитесь, что установлен дополнительный компонент [Подсистема Windows для Linux](./install-win10.md#enable-the-virtual-machine-platform-optional-component).</span><span class="sxs-lookup"><span data-stu-id="4c084-174">Ensure that the [Windows Subsystem for Linux Optional Component is installed](./install-win10.md#enable-the-virtual-machine-platform-optional-component).</span></span> <span data-ttu-id="4c084-175">Кроме того, если вы используете устройство Arm64 и выполняете эту команду в PowerShell, вы получите эту ошибку.</span><span class="sxs-lookup"><span data-stu-id="4c084-175">Additionally, if you are using an Arm64 device and running this command from PowerShell, you will receive this error.</span></span> <span data-ttu-id="4c084-176">Вместо этого запустите `wsl.exe` из [PowerShell Core](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6) или командной строки.</span><span class="sxs-lookup"><span data-stu-id="4c084-176">Instead run `wsl.exe` from [PowerShell Core](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6), or Command Prompt.</span></span>
