---
title: Установить или удалить на Юбилейное обновление Windows 10 или Creators Update
description: Инструкции по установке и отмены установки для прежних версий, а также бета-версии дистрибутива на Юбилейное обновление Windows 10 или Creators Update
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, debian, suse, windows 10, прежних версий, бета-версия, установки, удаления, удаление, удалить, удаление, устаревшие
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: b31bb3a542b8481c723df42292e20e364680722d
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063592"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a><span data-ttu-id="8b2f9-104">Руководство по установке или удалении подсистемы Windows для Linux в юбилейном обновлении Windows 10 и Creators Update</span><span class="sxs-lookup"><span data-stu-id="8b2f9-104">Guide to install or uninstall Windows Subsystem for Linux on Windows 10 Anniversary Update and Creators Update</span></span> 

<span data-ttu-id="8b2f9-105">Если вы используете Windows 10 Creators Update или более поздней версии, можно [следуйте инструкциям по установке Windows 10](install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="8b2f9-105">If you're running Windows 10 Creators Update or later, please [follow the Windows 10 installation instructions](install-win10.md).</span></span>

<span data-ttu-id="8b2f9-106"><strong><em><span style="color: #f28014">Ниже приведены инструкции для пользователей, выполняющих Юбилейное обновление Windows 10 или Windows 10 Creators Update</span></em></strong></span><span class="sxs-lookup"><span data-stu-id="8b2f9-106"><strong><em><span style="color: #f28014">The following instructions are for users running Windows 10 Anniversary Update or Windows 10 Creators Update</span></em></strong></span></span>

<span data-ttu-id="8b2f9-107">До Windows 10 Fall Creators Update (версия 1709) WSL была выпущена в виде бета-функции и установить один экземпляр Ubuntu, при первом запуске «Bash на Ubuntu в Windows» (или Bash.exe).</span><span class="sxs-lookup"><span data-stu-id="8b2f9-107">Prior to Windows 10 Fall Creators Update (version 1709), WSL was released as a beta feature and installed a single Ubuntu instance when "Bash on Ubuntu on Windows" (or Bash.exe) was first run.</span></span>

> <span data-ttu-id="8b2f9-108">Хотя вы МОЖЕТЕ использовать WSL в более ранних выпусках Windows 10, бета-версии «прежних версий дистрибутива» считается устаревшим.</span><span class="sxs-lookup"><span data-stu-id="8b2f9-108">While you CAN use WSL on earlier Windows 10 releases, this beta "legacy distro" is now considered obsolete.</span></span> <span data-ttu-id="8b2f9-109">Настоятельно рекомендуется для выполнения самой последней версии Windows 10 доступна.</span><span class="sxs-lookup"><span data-stu-id="8b2f9-109">We strongly encourage you to run the most recent version of Windows 10 available.</span></span> <span data-ttu-id="8b2f9-110">Каждым новым выпуском Windows 10 включает многие сотни исправления и улучшения в WSL только, когда-либо дополнительные средства Linux и приложений для корректной работы в WSL.</span><span class="sxs-lookup"><span data-stu-id="8b2f9-110">Each new Windows 10 release includes many hundreds of fixes and improvements in WSL alone, allowing ever more Linux tools and apps to run correctly on WSL.</span></span>

<span data-ttu-id="8b2f9-111">Если не удается обновить Fall Creators Update или более поздней версии, выполните следующие действия, чтобы включить и использовать WSL.</span><span class="sxs-lookup"><span data-stu-id="8b2f9-111">If you cannot upgrade to Fall Creators Update or later, follow the steps below to enable and use WSL:</span></span>

1. <span data-ttu-id="8b2f9-112">Включение разработчиков режиме для запуска WSL на Юбилейное обновление Windows 10 Creators Update, то необходимо включить режим разработчика:</span><span class="sxs-lookup"><span data-stu-id="8b2f9-112">Turn on Developer Mode  To run WSL on Windows 10 Anniversary Update or Creators Update, you must enable Developer Mode:</span></span>

    <span data-ttu-id="8b2f9-113">Откройте **параметры** -> **обновление и безопасность** -> **для разработчиков**</span><span class="sxs-lookup"><span data-stu-id="8b2f9-113">Open **Settings** -> **Update and Security** -> **For developers**</span></span>

    <span data-ttu-id="8b2f9-114">Установите переключатель в режим разработчика.</span><span class="sxs-lookup"><span data-stu-id="8b2f9-114">Select the Developer Mode radio button</span></span>  
    ![Включение режима разработчика](media/updateAndSecurity.png)

    > <span data-ttu-id="8b2f9-116">Требование, чтобы включить режим разработчика была [удален в Windows 10 Fall Creators Update](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)</span><span class="sxs-lookup"><span data-stu-id="8b2f9-116">The requirement to enable Developer Mode was [removed in Windows 10 Fall Creators Update](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)</span></span>

1. <span data-ttu-id="8b2f9-117">Откройте командную строку.</span><span class="sxs-lookup"><span data-stu-id="8b2f9-117">Open a command prompt.</span></span>  <span data-ttu-id="8b2f9-118">Тип `bash` и нажмите клавишу ВВОД</span><span class="sxs-lookup"><span data-stu-id="8b2f9-118">Type `bash` and hit enter</span></span>

    <span data-ttu-id="8b2f9-119">Первый раз выполнять Bash на Ubuntu в Windows, вам будет предложено принять условия лицензионного соглашения Canonical.</span><span class="sxs-lookup"><span data-stu-id="8b2f9-119">The first time you run Bash on Ubuntu on Windows, you'll be prompted to accept Canonical's license.</span></span> <span data-ttu-id="8b2f9-120">После accpted, WSL загрузит и установит экземпляре Ubuntu на компьютер, а также будет добавлен ярлык «Bash на Ubuntu в Windows» в меню «Пуск».</span><span class="sxs-lookup"><span data-stu-id="8b2f9-120">Once accpted, WSL will download and install the Ubuntu instance onto your machine, and a "Bash on Ubuntu on Windows" shortcut will be added to your start menu.</span></span>

    ![Запрос на установку Ubuntu](media/bashShellInstall.png)

    <span data-ttu-id="8b2f9-122">При первом выполнении Bash на Ubuntu в Windows, будет предложено создать UNIX имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="8b2f9-122">The first time you run Bash on Ubuntu on Windows, you will be prompted to create a UNIX username and password.</span></span> <span data-ttu-id="8b2f9-123">Выполните [инструкции по созданию экземпляра дистрибутива](initialize-distro.md) для завершения установки</span><span class="sxs-lookup"><span data-stu-id="8b2f9-123">Follow the [new distro instance instructions](initialize-distro.md) to complete your installation</span></span>

1. <span data-ttu-id="8b2f9-124">Для запуска новой оболочки Ubuntu либо:</span><span class="sxs-lookup"><span data-stu-id="8b2f9-124">Launch a new Ubuntu shell by either:</span></span>
    * <span data-ttu-id="8b2f9-125">Под управлением `bash` из командной строки</span><span class="sxs-lookup"><span data-stu-id="8b2f9-125">Running `bash` from a command-prompt</span></span>
    * <span data-ttu-id="8b2f9-126">Щелкнув главное меню «Bash на Ubuntu в Windows»</span><span class="sxs-lookup"><span data-stu-id="8b2f9-126">Clicking the start menu "Bash on Ubuntu on Windows" shortcut</span></span>

    
## <a name="uninstallingremoving-the-legacy-distro"></a><span data-ttu-id="8b2f9-127">При удалении/удаление предыдущих версий дистрибутива</span><span class="sxs-lookup"><span data-stu-id="8b2f9-127">Uninstalling/Removing the legacy distro</span></span>
<span data-ttu-id="8b2f9-128">При обновлении до Windows 10 Fall Creators Update более ранней версии Windows 10, на котором установлен WSL, ваши существующие дистрибутива останется без изменений.</span><span class="sxs-lookup"><span data-stu-id="8b2f9-128">If you upgrade to Windows 10 Fall Creators Update from an earlier Windows 10 release upon which you installed WSL, your existing distro will remain intact.</span></span> <span data-ttu-id="8b2f9-129">Тем не менее мы настоятельно рекомендуем вам установить дистрибутив новые доставляемые Store кратчайшие СРОКИ и перенести все необходимые файлы, данные, и т.д. из вашего дистрибутива прежних версий для вашего нового дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="8b2f9-129">However, we STRONGLY encourage you to install a new Store-delivered distro ASAP, and migrate any necessary files, data, etc. from your legacy distro to your new distro.</span></span>

<span data-ttu-id="8b2f9-130">Чтобы удалить устаревшие дистрибутива с компьютера, выполните следующую команду из командной строки или PowerShell экземпляр:</span><span class="sxs-lookup"><span data-stu-id="8b2f9-130">To remove the legacy distro from your machine, run the following from a Command Line or PowerShell instance:</span></span>

```console
lxrun /uninstall /full
```

### <a name="manually-deleting-the-legacy-distro"></a><span data-ttu-id="8b2f9-131">Удаление устаревших дистрибутива вручную</span><span class="sxs-lookup"><span data-stu-id="8b2f9-131">Manually deleting the legacy distro</span></span>
<span data-ttu-id="8b2f9-132">При желании можно вручную удалить устаревший экземпляр.</span><span class="sxs-lookup"><span data-stu-id="8b2f9-132">If you wish, you can manually delete your legacy instance.</span></span> <span data-ttu-id="8b2f9-133">Это может потребоваться при возникновении проблем, при удалении устаревших дистрибутив с помощью `lxrun.exe`, или работает под управлением Windows 10 весна 2018 с обновлением (или более поздней версии) которого не поставляются с `lxrun.exe`.</span><span class="sxs-lookup"><span data-stu-id="8b2f9-133">This may be required if you encounter issues uninstalling the legacy distro using `lxrun.exe`, or are running Windows 10 Spring 2018 Update (or later) which do not ship with `lxrun.exe`.</span></span>

<span data-ttu-id="8b2f9-134">Чтобы принудительно удалить вашего прежних версий дистрибутива WSL, удалите `%localappdata%\lxss\` папки (и всех его в содержимое вложенного) с помощью проводника Windows, или из командной строки:</span><span class="sxs-lookup"><span data-stu-id="8b2f9-134">To forcefully delete your legacy WSL distro, delete the `%localappdata%\lxss\` folder (and all it's sub-contents) using Windows' File Explorer, or the command-line:</span></span>

<span data-ttu-id="8b2f9-135">Использование PowerShell</span><span class="sxs-lookup"><span data-stu-id="8b2f9-135">Using PowerShell</span></span>
```powershell
rm -Recurse $env:localappdata/lxss/
```

<span data-ttu-id="8b2f9-136">С использованием командной строки:</span><span class="sxs-lookup"><span data-stu-id="8b2f9-136">Using Cmd:</span></span>
```console
DEL /S %localappdata%\lxss\
```
