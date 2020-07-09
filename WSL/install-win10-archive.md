---
title: Архивные инструкции WSL
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ROBOTS: NOINDEX
ms.openlocfilehash: 1de614dccbbb8d0ef1b9ac070f6ec90281339858
ms.sourcegitcommit: 16ffb1a096a4a7fbb77c58f92258051930cc82da
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2020
ms.locfileid: "86157960"
---
# <a name="archived-instructions"></a><span data-ttu-id="f35c2-102">Архивированные инструкции</span><span class="sxs-lookup"><span data-stu-id="f35c2-102">Archived instructions</span></span>

<span data-ttu-id="f35c2-103">В этом руководстве описано, как установить подсистему Windows для Linux (WSL) на компьютере под управлением Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f35c2-103">The following guide will walk through the steps required to install the Windows Subsystem for Linux (WSL) on a computer running Windows 10.</span></span>

## <a name="enable-the-windows-subsystem-for-linux-optional-feature"></a><span data-ttu-id="f35c2-104">Включение дополнительного компонента "Подсистема Windows для Linux"</span><span class="sxs-lookup"><span data-stu-id="f35c2-104">Enable the Windows Subsystem for Linux optional feature</span></span>

<span data-ttu-id="f35c2-105">Перед установкой дистрибутива Linux необходимо включить дополнительный компонент "Подсистема Windows для Linux" в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f35c2-105">Before installing a Linux distribution, you must enable the "Windows Subsystem for Linux" optional feature on Windows 10:</span></span>

1. <span data-ttu-id="f35c2-106">Запустите PowerShell от имени администратора и введите такой скрипт:</span><span class="sxs-lookup"><span data-stu-id="f35c2-106">Open PowerShell as Administrator and enter this script:</span></span>

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

1. <span data-ttu-id="f35c2-107">При появлении соответствующего запроса перезагрузите компьютер.</span><span class="sxs-lookup"><span data-stu-id="f35c2-107">Restart your computer when prompted.</span></span>

## <a name="install-a-linux-distribution"></a><span data-ttu-id="f35c2-108">Установка дистрибутива Linux</span><span class="sxs-lookup"><span data-stu-id="f35c2-108">Install a Linux distribution</span></span>

<span data-ttu-id="f35c2-109">Скачать и установить предпочтительные дистрибутивы Linux можно тремя способами:</span><span class="sxs-lookup"><span data-stu-id="f35c2-109">There are three ways to download and install your preferred Linux distribution(s):</span></span>

- <span data-ttu-id="f35c2-110">Скачайте и установите их из Microsoft Store (см. ниже).</span><span class="sxs-lookup"><span data-stu-id="f35c2-110">Download and install from the Microsoft Store (see below)</span></span>
- [<span data-ttu-id="f35c2-111">Скачайте и установите вручную с помощью командной строки.</span><span class="sxs-lookup"><span data-stu-id="f35c2-111">Download and manually install from command line</span></span>](install-manual.md)
- [<span data-ttu-id="f35c2-112">Установка в Windows Server</span><span class="sxs-lookup"><span data-stu-id="f35c2-112">Install on Windows Server</span></span>](install-on-server.md)

### <a name="install-from-the-microsoft-store"></a><span data-ttu-id="f35c2-113">установка из Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="f35c2-113">Install from the Microsoft Store</span></span>

<span data-ttu-id="f35c2-114">Дистрибутивы Linux можно установить из Microsoft Store в Windows 10 (сборка 16215 и выше).</span><span class="sxs-lookup"><span data-stu-id="f35c2-114">Linux distributions can be installed from the Microsoft Store on Windows 10 (Build 16215+).</span></span>

> [!NOTE]
> <span data-ttu-id="f35c2-115">Чтобы узнать номер сборки Windows 10, выполните [эти действия](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="f35c2-115">Follow these steps to [check your Windows 10 build number](troubleshooting.md#check-your-build-number).</span></span>

1. <span data-ttu-id="f35c2-116">Откройте Microsoft Store и выберите предпочтительный дистрибутив Linux.</span><span class="sxs-lookup"><span data-stu-id="f35c2-116">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Представление дистрибутивов Linux в Microsoft Store](media/store.png)

    <span data-ttu-id="f35c2-118">Ниже приведены ссылки на страницы Microsoft Store для каждого дистрибутива:</span><span class="sxs-lookup"><span data-stu-id="f35c2-118">The following links will open the Microsoft store page for each distribution:</span></span>

    - [<span data-ttu-id="f35c2-119">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="f35c2-119">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [<span data-ttu-id="f35c2-120">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="f35c2-120">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [<span data-ttu-id="f35c2-121">OpenSUSE Leap 15</span><span class="sxs-lookup"><span data-stu-id="f35c2-121">OpenSUSE Leap 15</span></span>](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    - [<span data-ttu-id="f35c2-122">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="f35c2-122">OpenSUSE Leap 42</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    - [<span data-ttu-id="f35c2-123">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="f35c2-123">SUSE Linux Enterprise Server 12</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    - [<span data-ttu-id="f35c2-124">SUSE Linux Enterprise Server 15</span><span class="sxs-lookup"><span data-stu-id="f35c2-124">SUSE Linux Enterprise Server 15</span></span>](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    - [<span data-ttu-id="f35c2-125">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="f35c2-125">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [<span data-ttu-id="f35c2-126">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="f35c2-126">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [<span data-ttu-id="f35c2-127">Fedora Remix for WSL</span><span class="sxs-lookup"><span data-stu-id="f35c2-127">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [<span data-ttu-id="f35c2-128">Pengwin</span><span class="sxs-lookup"><span data-stu-id="f35c2-128">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [<span data-ttu-id="f35c2-129">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="f35c2-129">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [<span data-ttu-id="f35c2-130">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="f35c2-130">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

1. <span data-ttu-id="f35c2-131">Выберите "Получить". Когда скачивание дистрибутива завершится, выберите "Запустить".</span><span class="sxs-lookup"><span data-stu-id="f35c2-131">Select "Get" and once the distribution has finished downloading, select "Launch".</span></span>

    ![Представление дистрибутивов Linux в Microsoft Store](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="f35c2-133">Завершение инициализации дистрибутива</span><span class="sxs-lookup"><span data-stu-id="f35c2-133">Complete initialization of your distro</span></span>

<span data-ttu-id="f35c2-134">После запуска дистрибутива Linux следуйте инструкциям на экране, чтобы инициализировать дистрибутив.</span><span class="sxs-lookup"><span data-stu-id="f35c2-134">After launching your Linux distribution, follow the onscreen instructions to initialize your distro.</span></span>

> [!NOTE]
> <span data-ttu-id="f35c2-135">В Windows Server запустите дистрибутив с помощью исполняемого файла `<distro>.exe` в папке установки.</span><span class="sxs-lookup"><span data-stu-id="f35c2-135">For Windows Server, launch your distribution using the executable, `<distro>.exe`, in the installation folder.</span></span>

<span data-ttu-id="f35c2-136">При первом запуске недавно установленного дистрибутива откроется окно консоли и вам будет предложено подождать одну или две минуты до завершения установки.</span><span class="sxs-lookup"><span data-stu-id="f35c2-136">The first time a newly installed distribution runs, a console window will open and you'll be asked to wait for a minute or two for the installation to complete.</span></span> <span data-ttu-id="f35c2-137">На этом последнем этапе установки файлы дистрибутива будут распакованы и сохранены на компьютере, полностью готовые к использованию.</span><span class="sxs-lookup"><span data-stu-id="f35c2-137">During this final stage of installation, the distro's files are de-compressed and stored on your PC, ready for use.</span></span> <span data-ttu-id="f35c2-138">Это может занять около минуты, в зависимости от производительности накопителей на компьютере.</span><span class="sxs-lookup"><span data-stu-id="f35c2-138">This may take around a minute or more depending on the performance of your PC's storage devices.</span></span> <span data-ttu-id="f35c2-139">Этот начальный этап установки требуется только в том случае, если выполняется чистая установка дистрибутива. Все последующие запуски должны занимать меньше секунды.</span><span class="sxs-lookup"><span data-stu-id="f35c2-139">This initial installation phase is only required when a distro is clean-installed - all future launches should take less than a second.</span></span>

## <a name="set-up-a-new-linux-user-account"></a><span data-ttu-id="f35c2-140">Настройка новой учетной записи пользователя Linux</span><span class="sxs-lookup"><span data-stu-id="f35c2-140">Set up a new Linux user account</span></span>

<span data-ttu-id="f35c2-141">После завершения установки вам будет предложено создать учетную запись пользователя (и ее пароль).</span><span class="sxs-lookup"><span data-stu-id="f35c2-141">Once installation is complete, you will be prompted to create a new user account (and its password).</span></span>

![Распаковка Ubuntu в консоли Windows](media/UbuntuInstall.png)

<span data-ttu-id="f35c2-143">Эта учетная запись представляет обычного пользователя без прав администратора, который будет по умолчанию входить в систему при запуске дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="f35c2-143">This user account is for the normal non-admin user that you'll be logged-in as by default when launching a distribution.</span></span> <span data-ttu-id="f35c2-144">Вы можете выбрать любые имя пользователя и пароль, которые не связаны с именем пользователя Windows.</span><span class="sxs-lookup"><span data-stu-id="f35c2-144">You can choose any username and password you wish - they have no bearing on your Windows username.</span></span>

<span data-ttu-id="f35c2-145">Когда вы открываете новый экземпляр дистрибутива, вам не будет предложено ввести пароль, но **если вы повысите привилегии процесса, используя `sudo`, вам нужно будет указать пароль**. Поэтому убедитесь, что вы выбрали пароль, который вы можете легко запомнить.</span><span class="sxs-lookup"><span data-stu-id="f35c2-145">When you open a new distro instance, you won't be prompted for your password, but **if you elevate a process using `sudo`, you will need to enter your password**, so make sure you choose a password you can easily remember!</span></span> <span data-ttu-id="f35c2-146">Дополнительные сведения приведены на странице [Учетные записи пользователей и разрешения для подсистемы Windows для Linux](user-support.md).</span><span class="sxs-lookup"><span data-stu-id="f35c2-146">See the [User Support](user-support.md) page for more info.</span></span>

## <a name="update--upgrade-packages"></a><span data-ttu-id="f35c2-147">Обновление пакетов</span><span class="sxs-lookup"><span data-stu-id="f35c2-147">Update & upgrade packages</span></span>

<span data-ttu-id="f35c2-148">Большинство дистрибутивов поставляется с пустым или минимально наполненным каталогом пакетов.</span><span class="sxs-lookup"><span data-stu-id="f35c2-148">Most distributions ship with an empty or minimal package catalog.</span></span> <span data-ttu-id="f35c2-149">Мы настоятельно рекомендуем регулярно обновлять каталог пакетов и установленные пакеты с помощью предпочитаемого диспетчера пакетов дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="f35c2-149">We strongly recommend regularly updating your package catalog and upgrading your installed packages using your distro's preferred package manager.</span></span> <span data-ttu-id="f35c2-150">Для Debian или Ubuntu используется функция apt.</span><span class="sxs-lookup"><span data-stu-id="f35c2-150">For Debian/Ubuntu, use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

<span data-ttu-id="f35c2-151">Windows не выполняет автоматическую установку новых версий или обновление дистрибутивов Linux.</span><span class="sxs-lookup"><span data-stu-id="f35c2-151">Windows does not automatically update or upgrade your Linux distro(s).</span></span> <span data-ttu-id="f35c2-152">Это задача, выполнение которой большинство пользователей Linux предпочитают контролировать самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="f35c2-152">This is a task that the most Linux users prefer to control themselves.</span></span>

<span data-ttu-id="f35c2-153">Наслаждайтесь новыми дистрибутивами Linux в WSL.</span><span class="sxs-lookup"><span data-stu-id="f35c2-153">Enjoy using your new Linux distro on WSL!</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="f35c2-154">Диагностика</span><span class="sxs-lookup"><span data-stu-id="f35c2-154">Troubleshooting</span></span>

<span data-ttu-id="f35c2-155">Ниже перечислены ошибки, связанные с установкой, и способы их устранения.</span><span class="sxs-lookup"><span data-stu-id="f35c2-155">Below are related installation errors and suggested fixes.</span></span> <span data-ttu-id="f35c2-156">Другие распространенные ошибки и способы их устранения приведены в разделе [Устранение неполадок подсистемы Windows для Linux](troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="f35c2-156">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

### <a name="installation-failed-with-error-0x8007007e"></a><span data-ttu-id="f35c2-157">Сбой установки с ошибкой 0x8007007e.</span><span class="sxs-lookup"><span data-stu-id="f35c2-157">Installation failed with error 0x8007007e</span></span>

<span data-ttu-id="f35c2-158">Эта ошибка возникает, когда система не поддерживает Linux из Store.</span><span class="sxs-lookup"><span data-stu-id="f35c2-158">This error occurs when your system doesn't support Linux from the store.</span></span>  <span data-ttu-id="f35c2-159">Убедитесь в следующем.</span><span class="sxs-lookup"><span data-stu-id="f35c2-159">Make sure that:</span></span>

- <span data-ttu-id="f35c2-160">Вы используете сборку Windows 16215 или более позднюю версию.</span><span class="sxs-lookup"><span data-stu-id="f35c2-160">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="f35c2-161">[Проверьте используемую сборку](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="f35c2-161">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
- <span data-ttu-id="f35c2-162">Дополнительный компонент "Подсистема Windows для Linux" включен, а компьютер был перезагружен.</span><span class="sxs-lookup"><span data-stu-id="f35c2-162">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="f35c2-163">[Убедитесь, что WSL включен](troubleshooting.md#confirm-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="f35c2-163">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>

### <a name="installation-failed-with-error-0x80070003"></a><span data-ttu-id="f35c2-164">Сбой установки с ошибкой 0x80070003.</span><span class="sxs-lookup"><span data-stu-id="f35c2-164">Installation failed with error 0x80070003</span></span>

<span data-ttu-id="f35c2-165">Подсистема Windows для Linux работает только на системном диске (обычно это диск `C:`).</span><span class="sxs-lookup"><span data-stu-id="f35c2-165">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="f35c2-166">Убедитесь, что дистрибутивы хранятся на системном диске.</span><span class="sxs-lookup"><span data-stu-id="f35c2-166">Make sure that distros are stored on your system drive:</span></span>

- <span data-ttu-id="f35c2-167">Выберите **Параметры** -> **Хранилище** -> **Другие параметры хранилища: изменить место сохранения нового содержимого**.</span><span class="sxs-lookup"><span data-stu-id="f35c2-167">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**</span></span>
  
    ![Изображение параметров системы для установки приложений на диске C.](media/AppStorage.png)

### <a name="wslregisterdistribution-failed-with-error-0x8007019e"></a><span data-ttu-id="f35c2-169">Сбой WslRegisterDistribution с ошибкой 0x8007019e.</span><span class="sxs-lookup"><span data-stu-id="f35c2-169">WslRegisterDistribution failed with error 0x8007019e</span></span>

<span data-ttu-id="f35c2-170">Дополнительный компонент "Подсистема Windows для Linux" не включен.</span><span class="sxs-lookup"><span data-stu-id="f35c2-170">The Windows Subsystem for Linux optional component is not enabled:</span></span>

- <span data-ttu-id="f35c2-171">Выберите **Панель управления** -> **Программы и компоненты** -> **Включение или отключение компонентов Windows** и установите флажок **Подсистема Windows для Linux** или используйте командлет PowerShell, упомянутый в начале этой статьи.</span><span class="sxs-lookup"><span data-stu-id="f35c2-171">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>
