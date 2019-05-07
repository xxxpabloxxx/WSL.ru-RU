---
title: Инициализируйте новый дистрибутив WSL Linux
description: После установки это дистрибутив Linux для WSL, завершения инициализации, выполнив следующие простые действия
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, debian, suse, windows 10
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 7f1ce521b248c873fa7f81c6363eb506c0363fed
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2019
ms.locfileid: "59902051"
---
# <a name="initializing-a-newly-installed-distro"></a><span data-ttu-id="57c9e-104">Инициализация установленный дистрибутив</span><span class="sxs-lookup"><span data-stu-id="57c9e-104">Initializing a newly installed distro</span></span>
<span data-ttu-id="57c9e-105">После загрузки и установки вашего дистрибутива необходимо завершить инициализацию новый дистрибутива:</span><span class="sxs-lookup"><span data-stu-id="57c9e-105">Once your distro has been downloaded and installed, you'll need to complete initialization of the new distro:</span></span>

## <a name="launch-a-distro"></a><span data-ttu-id="57c9e-106">Запустите дистрибутив</span><span class="sxs-lookup"><span data-stu-id="57c9e-106">Launch a distro</span></span>
<span data-ttu-id="57c9e-107">Чтобы завершить инициализацию вашего недавно установленные дистрибутива, запустите новый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="57c9e-107">To complete the initialization of your newly installed distro, launch a new instance.</span></span> <span data-ttu-id="57c9e-108">Это можно сделать, щелкнув кнопку «запустить» в приложении Windows Store, или запустив дистрибутива из меню "Пуск":</span><span class="sxs-lookup"><span data-stu-id="57c9e-108">You can do this by clicking the "launch" button in the Windows Store app, or launching the distro from the Start menu:</span></span>

> <span data-ttu-id="57c9e-109">Совет. Вы можете закрепить на наиболее часто используемые дистрибутивов, в меню "Пуск" и/или на панель задач!</span><span class="sxs-lookup"><span data-stu-id="57c9e-109">Tip: You might want to pin your most frequently used distros to your Start menu, and/or to your taskbar!</span></span>

![Запустите дистрибутивы из меню "Пуск"](media/start-menu.png)

> <span data-ttu-id="57c9e-111">В Windows Server, можно запустить исполняемый файл запуска вашего дистрибутива `<distro>.exe` из папки установки дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="57c9e-111">On Windows Server, you can launch your distro's launcher executable `<distro>.exe` from the distro installation folder.</span></span>

<span data-ttu-id="57c9e-112">Первый раз дистрибутив только что установленного консолью, будет открыто окно, и вам будет предложено ожидания-две минуты для завершения установки.</span><span class="sxs-lookup"><span data-stu-id="57c9e-112">The first time a newly installed distro runs, a Console window will open, and you'll be asked to wait for a minute or two for the installation to complete.</span></span>

> <span data-ttu-id="57c9e-113">На этом этапе окончательной установки дистрибутива файлы отзыва сжаты и хранить на Компьютере, готовой к использованию.</span><span class="sxs-lookup"><span data-stu-id="57c9e-113">During this final stage of installation, the distro's files are de-compressed and stored on your PC, ready for use.</span></span> <span data-ttu-id="57c9e-114">Это может занять минуты или более в зависимости от производительности компьютера запоминающих устройств.</span><span class="sxs-lookup"><span data-stu-id="57c9e-114">This may take around a minute or more depending on the performance of your PC's storage devices.</span></span> <span data-ttu-id="57c9e-115">Начального этапа установки только в том случае требуется при непосредственной установке — это дистрибутив всех будущих запусков занимает менее секунды.</span><span class="sxs-lookup"><span data-stu-id="57c9e-115">This initial installation phase is only required when a distro is clean-installed - all future launches should take less than a second.</span></span>

## <a name="setting-up-a-new-linux-user-account"></a><span data-ttu-id="57c9e-116">Настройка учетной записи пользователя Linux</span><span class="sxs-lookup"><span data-stu-id="57c9e-116">Setting up a new Linux user account</span></span>

<span data-ttu-id="57c9e-117">После завершения установки вам будет предложено создать учетную запись пользователя (и пароль).</span><span class="sxs-lookup"><span data-stu-id="57c9e-117">Once installation is complete, you will be prompted to create a new user account (and its password).</span></span> 

![Ubuntu, распаковать его в консоли Windows](media/UbuntuInstall.png)

<span data-ttu-id="57c9e-119">Этой учетной записи пользователя является для пользователя обычной без прав администратора, вы будете вошедшего в систему как по умолчанию, при запуске дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="57c9e-119">This user account is for the normal non-admin user that you'll be logged-in as by default when launching a distro.</span></span>

> <span data-ttu-id="57c9e-120">Можно выбрать любое имя пользователя и пароль, которые будут — они никак не влияют на ваше имя пользователя Windows.</span><span class="sxs-lookup"><span data-stu-id="57c9e-120">You can choose any username and password you wish - they have no bearing on your Windows username.</span></span> 

<span data-ttu-id="57c9e-121">При открытии нового экземпляра дистрибутива, нет необходимости в поле пароля, но **если повысить процесс, используя `sudo`, необходимо будет ввести пароль**, поэтому убедитесь, что выбрать пароль, вы можете легко запомнить!</span><span class="sxs-lookup"><span data-stu-id="57c9e-121">When you open a new distro instance, you won't be prompted for your password, but **if you elevate a process using `sudo`, you will need to enter your password**, so make sure you choose a password you can easily remember!</span></span> <span data-ttu-id="57c9e-122">См. в разделе [поддержка пользователей](user-support.md) страницу Дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="57c9e-122">See the [User Support](user-support.md) page for more info.</span></span>

## <a name="update--upgrade-your-distros-packages"></a><span data-ttu-id="57c9e-123">Обновить & вашего дистрибутива пакеты обновления</span><span class="sxs-lookup"><span data-stu-id="57c9e-123">Update & upgrade your distro's packages</span></span>

<span data-ttu-id="57c9e-124">Большинство дистрибутивов в поставку в каталоге минимальный/пустой пакет.</span><span class="sxs-lookup"><span data-stu-id="57c9e-124">Most distros ship with an empty/minimal package catalog.</span></span> <span data-ttu-id="57c9e-125">Настоятельно рекомендуется регулярно обновление каталога пакета и обновление установленных пакетов с помощью вашего дистрибутива предпочтительным диспетчером пакетов.</span><span class="sxs-lookup"><span data-stu-id="57c9e-125">We strongly recommend regularly updating your package catalog, and upgrading your installed packages using your distro's preferred package manager.</span></span> <span data-ttu-id="57c9e-126">В Debian и Ubuntu используйте apt:</span><span class="sxs-lookup"><span data-stu-id="57c9e-126">On Debian/Ubuntu, you use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

> <span data-ttu-id="57c9e-127">Windows автоматически обновлять или обновить ваш distro(s) Linux: Это задача, которая пользователей Linux предпочитаете управлять сами.</span><span class="sxs-lookup"><span data-stu-id="57c9e-127">Windows does not automatically update or upgrade your Linux distro(s): This is a task that the Linux users prefer to control themselves.</span></span>

<span data-ttu-id="57c9e-128">Готово!</span><span class="sxs-lookup"><span data-stu-id="57c9e-128">You're done!</span></span> <span data-ttu-id="57c9e-129">Наслаждайтесь, с помощью нового дистрибутив Linux на WSL!</span><span class="sxs-lookup"><span data-stu-id="57c9e-129">Enjoy using your new Linux distro on WSL!</span></span> <span data-ttu-id="57c9e-130">Дополнительные сведения о WSL, просмотрите и другие [документация WSL](https://aka.ms/wsldocs), или [WSL обучения странице ресурсов](https://aka.ms/learnwsl).</span><span class="sxs-lookup"><span data-stu-id="57c9e-130">To learn more about WSL, review the other [WSL docs](https://aka.ms/wsldocs), or the [WSL learning resources page](https://aka.ms/learnwsl).</span></span>

![Понравится работать с Linux на WSL](media/linux-on-wsl.png)

## <a name="troubleshooting"></a><span data-ttu-id="57c9e-132">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="57c9e-132">Troubleshooting</span></span>

<span data-ttu-id="57c9e-133">Ниже приведены ошибки, связанные с и предлагаемые исправления.</span><span class="sxs-lookup"><span data-stu-id="57c9e-133">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="57c9e-134">Ссылаться на [WSL странице](troubleshooting.md) для других распространенных ошибок и способы их решения.</span><span class="sxs-lookup"><span data-stu-id="57c9e-134">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

> <span data-ttu-id="57c9e-135">**Установка завершилась ошибкой 0x8007007e** Эта ошибка возникает, когда ваша система не поддерживает Linux в магазине.</span><span class="sxs-lookup"><span data-stu-id="57c9e-135">**Installation failed with error 0x8007007e** This error occurs when your system doesn't support Linux from the store.</span></span>  <span data-ttu-id="57c9e-136">Убедитесь в следующем.</span><span class="sxs-lookup"><span data-stu-id="57c9e-136">Make sure that:</span></span>
> * <span data-ttu-id="57c9e-137">Вы используете Windows сборки 16215 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="57c9e-137">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="57c9e-138">[Проверьте сборку](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="57c9e-138">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
> * <span data-ttu-id="57c9e-139">Подсистема Windows для Linux дополнительный компонент включен и перезагрузки компьютера.</span><span class="sxs-lookup"><span data-stu-id="57c9e-139">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="57c9e-140">[Убедитесь, что включен WSL](troubleshooting.md#confirm-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="57c9e-140">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
