---
title: Установка подсистемы Windows для Linux (WSL) в Windows 10
description: Инструкции по установке подсистемы Windows для Linux в Windows 10.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, debian, suse, windows 10, установка
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 6ed12ba9d63d3f4038b67489035e13113a372928
ms.sourcegitcommit: 9f12e168b80775cd967f22f97376e51043c3667e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/02/2020
ms.locfileid: "84301205"
---
# <a name="install-windows-subsystem-for-linux"></a><span data-ttu-id="948e8-104">Установка подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="948e8-104">Install Windows Subsystem for Linux</span></span>

<span data-ttu-id="948e8-105">В этом руководстве описано, как установить подсистему Windows для Linux (WSL) на компьютере под управлением Windows 10.</span><span class="sxs-lookup"><span data-stu-id="948e8-105">The following guide will walk through the steps required to install the Windows Subsystem for Linux (WSL) on a computer running Windows 10.</span></span>

## <a name="enable-the-windows-subsystem-for-linux-optional-feature"></a><span data-ttu-id="948e8-106">Включение дополнительного компонента "Подсистема Windows для Linux"</span><span class="sxs-lookup"><span data-stu-id="948e8-106">Enable the Windows Subsystem for Linux optional feature</span></span>

<span data-ttu-id="948e8-107">Перед установкой дистрибутива Linux необходимо включить дополнительный компонент "Подсистема Windows для Linux" в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="948e8-107">Before installing a Linux distribution, you must enable the "Windows Subsystem for Linux" optional feature on Windows 10:</span></span>

1. <span data-ttu-id="948e8-108">Запустите PowerShell от имени администратора и введите такой скрипт:</span><span class="sxs-lookup"><span data-stu-id="948e8-108">Open PowerShell as Administrator and enter this script:</span></span>

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

1. <span data-ttu-id="948e8-109">При появлении соответствующего запроса перезагрузите компьютер.</span><span class="sxs-lookup"><span data-stu-id="948e8-109">Restart your computer when prompted.</span></span>

## <a name="install-a-linux-distribution"></a><span data-ttu-id="948e8-110">Установка дистрибутива Linux</span><span class="sxs-lookup"><span data-stu-id="948e8-110">Install a Linux distribution</span></span>

<span data-ttu-id="948e8-111">Скачать и установить предпочтительные дистрибутивы Linux можно тремя способами:</span><span class="sxs-lookup"><span data-stu-id="948e8-111">There are three ways to download and install your preferred Linux distribution(s):</span></span>

- <span data-ttu-id="948e8-112">Скачайте и установите их из Microsoft Store (см. ниже).</span><span class="sxs-lookup"><span data-stu-id="948e8-112">Download and install from the Microsoft Store (see below)</span></span>
- [<span data-ttu-id="948e8-113">Скачайте и установите вручную с помощью командной строки.</span><span class="sxs-lookup"><span data-stu-id="948e8-113">Download and manually install from command line</span></span>](install-manual.md)
- [<span data-ttu-id="948e8-114">Установка в Windows Server</span><span class="sxs-lookup"><span data-stu-id="948e8-114">Install on Windows Server</span></span>](install-on-server.md)

### <a name="install-from-the-microsoft-store"></a><span data-ttu-id="948e8-115">установка из Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="948e8-115">Install from the Microsoft Store</span></span>

<span data-ttu-id="948e8-116">Дистрибутивы Linux можно установить из Microsoft Store в Windows 10 (сборка 16215 и выше).</span><span class="sxs-lookup"><span data-stu-id="948e8-116">Linux distributions can be installed from the Microsoft Store on Windows 10 (Build 16215+).</span></span>

> [!NOTE]
> <span data-ttu-id="948e8-117">Чтобы узнать номер сборки Windows 10, выполните [эти действия](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="948e8-117">Follow these steps to [check your Windows 10 build number](troubleshooting.md#check-your-build-number).</span></span>

1. <span data-ttu-id="948e8-118">Откройте Microsoft Store и выберите предпочтительный дистрибутив Linux.</span><span class="sxs-lookup"><span data-stu-id="948e8-118">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Представление дистрибутивов Linux в Microsoft Store](media/store.png)

    <span data-ttu-id="948e8-120">Ниже приведены ссылки на страницы Microsoft Store для каждого дистрибутива:</span><span class="sxs-lookup"><span data-stu-id="948e8-120">The following links will open the Microsoft store page for each distribution:</span></span>

    - [<span data-ttu-id="948e8-121">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="948e8-121">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [<span data-ttu-id="948e8-122">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="948e8-122">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [<span data-ttu-id="948e8-123">OpenSUSE Leap 15</span><span class="sxs-lookup"><span data-stu-id="948e8-123">OpenSUSE Leap 15</span></span>](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    - [<span data-ttu-id="948e8-124">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="948e8-124">OpenSUSE Leap 42</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    - [<span data-ttu-id="948e8-125">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="948e8-125">SUSE Linux Enterprise Server 12</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    - [<span data-ttu-id="948e8-126">SUSE Linux Enterprise Server 15</span><span class="sxs-lookup"><span data-stu-id="948e8-126">SUSE Linux Enterprise Server 15</span></span>](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    - [<span data-ttu-id="948e8-127">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="948e8-127">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [<span data-ttu-id="948e8-128">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="948e8-128">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [<span data-ttu-id="948e8-129">Fedora Remix for WSL</span><span class="sxs-lookup"><span data-stu-id="948e8-129">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [<span data-ttu-id="948e8-130">Pengwin</span><span class="sxs-lookup"><span data-stu-id="948e8-130">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [<span data-ttu-id="948e8-131">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="948e8-131">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [<span data-ttu-id="948e8-132">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="948e8-132">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

1. <span data-ttu-id="948e8-133">Выберите "Получить". Когда скачивание дистрибутива завершится, выберите "Запустить".</span><span class="sxs-lookup"><span data-stu-id="948e8-133">Select "Get" and once the distribution has finished downloading, select "Launch".</span></span>

    ![Представление дистрибутивов Linux в Microsoft Store](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="948e8-135">Завершение инициализации дистрибутива</span><span class="sxs-lookup"><span data-stu-id="948e8-135">Complete initialization of your distro</span></span>

<span data-ttu-id="948e8-136">После запуска дистрибутива Linux следуйте инструкциям на экране, чтобы инициализировать дистрибутив.</span><span class="sxs-lookup"><span data-stu-id="948e8-136">After launching your Linux distribution, follow the onscreen instructions to initialize your distro.</span></span>

> [!NOTE]
> <span data-ttu-id="948e8-137">В Windows Server запустите дистрибутив с помощью исполняемого файла `<distro>.exe` в папке установки.</span><span class="sxs-lookup"><span data-stu-id="948e8-137">For Windows Server, launch your distribution using the executable, `<distro>.exe`, in the installation folder.</span></span>

<span data-ttu-id="948e8-138">При первом запуске недавно установленного дистрибутива откроется окно консоли и вам будет предложено подождать одну или две минуты до завершения установки.</span><span class="sxs-lookup"><span data-stu-id="948e8-138">The first time a newly installed distribution runs, a console window will open and you'll be asked to wait for a minute or two for the installation to complete.</span></span> <span data-ttu-id="948e8-139">На этом последнем этапе установки файлы дистрибутива будут распакованы и сохранены на компьютере, полностью готовые к использованию.</span><span class="sxs-lookup"><span data-stu-id="948e8-139">During this final stage of installation, the distro's files are de-compressed and stored on your PC, ready for use.</span></span> <span data-ttu-id="948e8-140">Это может занять около минуты, в зависимости от производительности накопителей на компьютере.</span><span class="sxs-lookup"><span data-stu-id="948e8-140">This may take around a minute or more depending on the performance of your PC's storage devices.</span></span> <span data-ttu-id="948e8-141">Этот начальный этап установки требуется только в том случае, если выполняется чистая установка дистрибутива. Все последующие запуски должны занимать меньше секунды.</span><span class="sxs-lookup"><span data-stu-id="948e8-141">This initial installation phase is only required when a distro is clean-installed - all future launches should take less than a second.</span></span>

## <a name="set-up-a-new-linux-user-account"></a><span data-ttu-id="948e8-142">Настройка новой учетной записи пользователя Linux</span><span class="sxs-lookup"><span data-stu-id="948e8-142">Set up a new Linux user account</span></span>

<span data-ttu-id="948e8-143">После завершения установки вам будет предложено создать учетную запись пользователя (и ее пароль).</span><span class="sxs-lookup"><span data-stu-id="948e8-143">Once installation is complete, you will be prompted to create a new user account (and its password).</span></span>

![Распаковка Ubuntu в консоли Windows](media/UbuntuInstall.png)

<span data-ttu-id="948e8-145">Эта учетная запись представляет обычного пользователя без прав администратора, который будет по умолчанию входить в систему при запуске дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="948e8-145">This user account is for the normal non-admin user that you'll be logged-in as by default when launching a distribution.</span></span> <span data-ttu-id="948e8-146">Вы можете выбрать любые имя пользователя и пароль, которые не связаны с именем пользователя Windows.</span><span class="sxs-lookup"><span data-stu-id="948e8-146">You can choose any username and password you wish - they have no bearing on your Windows username.</span></span>

<span data-ttu-id="948e8-147">Когда вы открываете новый экземпляр дистрибутива, вам не будет предложено ввести пароль, но **если вы повысите привилегии процесса, используя `sudo`, вам нужно будет указать пароль**. Поэтому убедитесь, что вы выбрали пароль, который вы можете легко запомнить.</span><span class="sxs-lookup"><span data-stu-id="948e8-147">When you open a new distro instance, you won't be prompted for your password, but **if you elevate a process using `sudo`, you will need to enter your password**, so make sure you choose a password you can easily remember!</span></span> <span data-ttu-id="948e8-148">Дополнительные сведения приведены на странице [Учетные записи пользователей и разрешения для подсистемы Windows для Linux](user-support.md).</span><span class="sxs-lookup"><span data-stu-id="948e8-148">See the [User Support](user-support.md) page for more info.</span></span>

## <a name="update--upgrade-packages"></a><span data-ttu-id="948e8-149">Обновление пакетов</span><span class="sxs-lookup"><span data-stu-id="948e8-149">Update & upgrade packages</span></span>

<span data-ttu-id="948e8-150">Большинство дистрибутивов поставляется с пустым или минимально наполненным каталогом пакетов.</span><span class="sxs-lookup"><span data-stu-id="948e8-150">Most distributions ship with an empty or minimal package catalog.</span></span> <span data-ttu-id="948e8-151">Мы настоятельно рекомендуем регулярно обновлять каталог пакетов и установленные пакеты с помощью предпочитаемого диспетчера пакетов дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="948e8-151">We strongly recommend regularly updating your package catalog and upgrading your installed packages using your distro's preferred package manager.</span></span> <span data-ttu-id="948e8-152">Для Debian или Ubuntu используется функция apt.</span><span class="sxs-lookup"><span data-stu-id="948e8-152">For Debian/Ubuntu, use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

<span data-ttu-id="948e8-153">Windows не выполняет автоматическую установку новых версий или обновление дистрибутивов Linux.</span><span class="sxs-lookup"><span data-stu-id="948e8-153">Windows does not automatically update or upgrade your Linux distro(s).</span></span> <span data-ttu-id="948e8-154">Это задача, выполнение которой большинство пользователей Linux предпочитают контролировать самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="948e8-154">This is a task that the most Linux users prefer to control themselves.</span></span>

<span data-ttu-id="948e8-155">Наслаждайтесь новыми дистрибутивами Linux в WSL.</span><span class="sxs-lookup"><span data-stu-id="948e8-155">Enjoy using your new Linux distro on WSL!</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="948e8-156">Диагностика</span><span class="sxs-lookup"><span data-stu-id="948e8-156">Troubleshooting</span></span>

<span data-ttu-id="948e8-157">Ниже перечислены ошибки, связанные с установкой, и способы их устранения.</span><span class="sxs-lookup"><span data-stu-id="948e8-157">Below are related installation errors and suggested fixes.</span></span> <span data-ttu-id="948e8-158">Другие распространенные ошибки и способы их устранения приведены в разделе [Устранение неполадок подсистемы Windows для Linux](troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="948e8-158">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

### <a name="installation-failed-with-error-0x8007007e"></a><span data-ttu-id="948e8-159">Сбой установки с ошибкой 0x8007007e.</span><span class="sxs-lookup"><span data-stu-id="948e8-159">Installation failed with error 0x8007007e</span></span>

<span data-ttu-id="948e8-160">Эта ошибка возникает, когда система не поддерживает Linux из Store.</span><span class="sxs-lookup"><span data-stu-id="948e8-160">This error occurs when your system doesn't support Linux from the store.</span></span>  <span data-ttu-id="948e8-161">Убедитесь в следующем.</span><span class="sxs-lookup"><span data-stu-id="948e8-161">Make sure that:</span></span>

- <span data-ttu-id="948e8-162">Вы используете сборку Windows 16215 или более позднюю версию.</span><span class="sxs-lookup"><span data-stu-id="948e8-162">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="948e8-163">[Проверьте используемую сборку](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="948e8-163">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
- <span data-ttu-id="948e8-164">Дополнительный компонент "Подсистема Windows для Linux" включен, а компьютер был перезагружен.</span><span class="sxs-lookup"><span data-stu-id="948e8-164">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="948e8-165">[Убедитесь, что WSL включен](troubleshooting.md#confirm-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="948e8-165">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>

### <a name="installation-failed-with-error-0x80070003"></a><span data-ttu-id="948e8-166">Сбой установки с ошибкой 0x80070003.</span><span class="sxs-lookup"><span data-stu-id="948e8-166">Installation failed with error 0x80070003</span></span>

<span data-ttu-id="948e8-167">Подсистема Windows для Linux работает только на системном диске (обычно это диск `C:`).</span><span class="sxs-lookup"><span data-stu-id="948e8-167">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="948e8-168">Убедитесь, что дистрибутивы хранятся на системном диске.</span><span class="sxs-lookup"><span data-stu-id="948e8-168">Make sure that distros are stored on your system drive:</span></span>

- <span data-ttu-id="948e8-169">Выберите **Параметры** -> **Хранилище** -> **Другие параметры хранилища: изменить место сохранения нового содержимого**.</span><span class="sxs-lookup"><span data-stu-id="948e8-169">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**</span></span>
  
    ![Изображение параметров системы для установки приложений на диске C.](media/AppStorage.png)

### <a name="wslregisterdistribution-failed-with-error-0x8007019e"></a><span data-ttu-id="948e8-171">Сбой WslRegisterDistribution с ошибкой 0x8007019e.</span><span class="sxs-lookup"><span data-stu-id="948e8-171">WslRegisterDistribution failed with error 0x8007019e</span></span>

<span data-ttu-id="948e8-172">Дополнительный компонент "Подсистема Windows для Linux" не включен.</span><span class="sxs-lookup"><span data-stu-id="948e8-172">The Windows Subsystem for Linux optional component is not enabled:</span></span>

- <span data-ttu-id="948e8-173">Выберите **Панель управления** -> **Программы и компоненты** -> **Включение или отключение компонентов Windows** и установите флажок **Подсистема Windows для Linux** или используйте командлет PowerShell, упомянутый в начале этой статьи.</span><span class="sxs-lookup"><span data-stu-id="948e8-173">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>
