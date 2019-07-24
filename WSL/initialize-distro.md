---
title: Инициализация нового WSL Linux дистрибутив
description: После установки Linux дистрибутив для WSL завершите инициализацию, выполнив следующие простые действия.
keywords: Башонвиндовс, bash, WSL, Windows, подсистема Windows для Linux, виндовссубсистем, Ubuntu, Debian, SUSE, Windows 10
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 30cb1de0a01fd46bc434061cd36794f4ece77e4b
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499296"
---
# <a name="initializing-a-newly-installed-distro"></a><span data-ttu-id="239b6-104">Инициализация недавно установленного дистрибутив</span><span class="sxs-lookup"><span data-stu-id="239b6-104">Initializing a newly installed distro</span></span>
<span data-ttu-id="239b6-105">После загрузки и установки дистрибутив необходимо выполнить инициализацию нового дистрибутив:</span><span class="sxs-lookup"><span data-stu-id="239b6-105">Once your distro has been downloaded and installed, you'll need to complete initialization of the new distro:</span></span>

## <a name="launch-a-distro"></a><span data-ttu-id="239b6-106">Запуск дистрибутив</span><span class="sxs-lookup"><span data-stu-id="239b6-106">Launch a distro</span></span>
<span data-ttu-id="239b6-107">Чтобы завершить инициализацию недавно установленного дистрибутив, запустите новый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="239b6-107">To complete the initialization of your newly installed distro, launch a new instance.</span></span> <span data-ttu-id="239b6-108">Для этого нажмите кнопку "запустить" в приложении Microsoft Store или запустите дистрибутив из меню "Пуск":</span><span class="sxs-lookup"><span data-stu-id="239b6-108">You can do this by clicking the "launch" button in the Microsoft Store app, or launching the distro from the Start menu:</span></span>

> <span data-ttu-id="239b6-109">Совет. Вам может потребоваться закрепить наиболее часто используемые дистрибутивов в меню "Пуск" и (или) на панели задач!</span><span class="sxs-lookup"><span data-stu-id="239b6-109">Tip: You might want to pin your most frequently used distros to your Start menu, and/or to your taskbar!</span></span>

![Запуск дистрибутивов из меню "Пуск"](media/start-menu.png)

> <span data-ttu-id="239b6-111">В Windows Server исполняемый файл `<distro>.exe` средства запуска дистрибутив можно запустить из папки установки дистрибутив.</span><span class="sxs-lookup"><span data-stu-id="239b6-111">On Windows Server, you can launch your distro's launcher executable `<distro>.exe` from the distro installation folder.</span></span>

<span data-ttu-id="239b6-112">При первом запуске недавно установленного дистрибутив откроется окно консоли, и вам будет предложено подождать одну или две минуты для завершения установки.</span><span class="sxs-lookup"><span data-stu-id="239b6-112">The first time a newly installed distro runs, a Console window will open, and you'll be asked to wait for a minute or two for the installation to complete.</span></span>

> <span data-ttu-id="239b6-113">На последнем этапе установки файлы дистрибутив будут распакованы и сохранены на компьютере и готовы к использованию.</span><span class="sxs-lookup"><span data-stu-id="239b6-113">During this final stage of installation, the distro's files are de-compressed and stored on your PC, ready for use.</span></span> <span data-ttu-id="239b6-114">Это может занять около минуты, в зависимости от производительности устройств хранения на компьютере.</span><span class="sxs-lookup"><span data-stu-id="239b6-114">This may take around a minute or more depending on the performance of your PC's storage devices.</span></span> <span data-ttu-id="239b6-115">Этот этап начальной установки требуется только в том случае, если дистрибутив является чистой установкой. все будущие запуски должны занимать меньше секунды.</span><span class="sxs-lookup"><span data-stu-id="239b6-115">This initial installation phase is only required when a distro is clean-installed - all future launches should take less than a second.</span></span>

## <a name="setting-up-a-new-linux-user-account"></a><span data-ttu-id="239b6-116">Настройка новой учетной записи пользователя Linux</span><span class="sxs-lookup"><span data-stu-id="239b6-116">Setting up a new Linux user account</span></span>

<span data-ttu-id="239b6-117">После завершения установки вам будет предложено создать новую учетную запись пользователя (и ее пароль).</span><span class="sxs-lookup"><span data-stu-id="239b6-117">Once installation is complete, you will be prompted to create a new user account (and its password).</span></span> 

![Распаковка Ubuntu в консоли Windows](media/UbuntuInstall.png)

<span data-ttu-id="239b6-119">Эта учетная запись пользователя предназначена для обычного пользователя без прав администратора, который вы будете входить в систему как по умолчанию при запуске дистрибутив.</span><span class="sxs-lookup"><span data-stu-id="239b6-119">This user account is for the normal non-admin user that you'll be logged-in as by default when launching a distro.</span></span>

> <span data-ttu-id="239b6-120">Вы можете выбрать любое имя пользователя и пароль, которые не влияют на имя пользователя Windows.</span><span class="sxs-lookup"><span data-stu-id="239b6-120">You can choose any username and password you wish - they have no bearing on your Windows username.</span></span> 

<span data-ttu-id="239b6-121">Когда вы открываете новый экземпляр дистрибутив, вам не будет предложено ввести пароль, но **Если вы потребуете повысить уровень `sudo`процесса с помощью, вам нужно будет указать**пароль, поэтому убедитесь, что вы выберете его.</span><span class="sxs-lookup"><span data-stu-id="239b6-121">When you open a new distro instance, you won't be prompted for your password, but **if you elevate a process using `sudo`, you will need to enter your password**, so make sure you choose a password you can easily remember!</span></span> <span data-ttu-id="239b6-122">Дополнительные сведения см. на странице [поддержки пользователей](user-support.md) .</span><span class="sxs-lookup"><span data-stu-id="239b6-122">See the [User Support](user-support.md) page for more info.</span></span>

## <a name="update--upgrade-your-distros-packages"></a><span data-ttu-id="239b6-123">Обновление & Обновление пакетов дистрибутив</span><span class="sxs-lookup"><span data-stu-id="239b6-123">Update & upgrade your distro's packages</span></span>

<span data-ttu-id="239b6-124">Большинство дистрибутивов поставляются с пустым или минимальным каталогом пакетов.</span><span class="sxs-lookup"><span data-stu-id="239b6-124">Most distros ship with an empty/minimal package catalog.</span></span> <span data-ttu-id="239b6-125">Мы настоятельно рекомендуем регулярно обновлять каталог пакетов и обновлять установленные пакеты с помощью предпочтительного диспетчера пакетов дистрибутив.</span><span class="sxs-lookup"><span data-stu-id="239b6-125">We strongly recommend regularly updating your package catalog, and upgrading your installed packages using your distro's preferred package manager.</span></span> <span data-ttu-id="239b6-126">В Debian или Ubuntu вы используете APT:</span><span class="sxs-lookup"><span data-stu-id="239b6-126">On Debian/Ubuntu, you use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

> <span data-ttu-id="239b6-127">Windows не выполняет автоматическое обновление или обновление дистрибутив Linux. Это задача, которую пользователи Linux предпочитают контролировать самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="239b6-127">Windows does not automatically update or upgrade your Linux distro(s): This is a task that the Linux users prefer to control themselves.</span></span>

<span data-ttu-id="239b6-128">Готово!</span><span class="sxs-lookup"><span data-stu-id="239b6-128">You're done!</span></span> <span data-ttu-id="239b6-129">Воспользуйтесь новыми дистрибутивами Linux на WSL!</span><span class="sxs-lookup"><span data-stu-id="239b6-129">Enjoy using your new Linux distro on WSL!</span></span> <span data-ttu-id="239b6-130">Дополнительные сведения о WSL см. в других [документах WSL](https://aka.ms/wsldocs)или на [странице учебных материалов по WSL](https://aka.ms/learnwsl).</span><span class="sxs-lookup"><span data-stu-id="239b6-130">To learn more about WSL, review the other [WSL docs](https://aka.ms/wsldocs), or the [WSL learning resources page](https://aka.ms/learnwsl).</span></span>

![Воспользуйтесь Linux на WSL](media/linux-on-wsl.png)

## <a name="troubleshooting"></a><span data-ttu-id="239b6-132">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="239b6-132">Troubleshooting</span></span>

<span data-ttu-id="239b6-133">Ниже приведены связанные ошибки и предлагаемые исправления.</span><span class="sxs-lookup"><span data-stu-id="239b6-133">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="239b6-134">Другие распространенные ошибки и их решения см. на [странице Устранение неполадок WSL](troubleshooting.md) .</span><span class="sxs-lookup"><span data-stu-id="239b6-134">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

> <span data-ttu-id="239b6-135">**Сбой установки с ошибкой 0x8007007e** Эта ошибка возникает, когда система не поддерживает Linux из хранилища.</span><span class="sxs-lookup"><span data-stu-id="239b6-135">**Installation failed with error 0x8007007e** This error occurs when your system doesn't support Linux from the store.</span></span>  <span data-ttu-id="239b6-136">Убедитесь в следующем.</span><span class="sxs-lookup"><span data-stu-id="239b6-136">Make sure that:</span></span>
> * <span data-ttu-id="239b6-137">Вы используете Windows Build 16215 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="239b6-137">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="239b6-138">[Проверьте сборку](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="239b6-138">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
> * <span data-ttu-id="239b6-139">Дополнительный компонент подсистемы Windows для Linux включен и компьютер перезагружен.</span><span class="sxs-lookup"><span data-stu-id="239b6-139">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="239b6-140">[Убедитесь, что WSL включен](troubleshooting.md#confirm-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="239b6-140">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
