---
title: Установите или удалите на годовщине Windows 10 обновление или создатели
description: Инструкции по установке и отмене установки для устаревших, бета-версий дистрибутив в Windows 10 с годовщиной обновления или авторов
keywords: Башонвиндовс, bash, WSL, Windows, подсистема Windows для Linux, виндовссубсистем, Ubuntu, Debian, SUSE, Windows 10, устаревшая, бета-версия, установка, удаление, удаление, отмена установки, удаление, устарело
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 416bed3ed3a0470da2eb5e6beb75e73eb6836200
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269774"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a><span data-ttu-id="4b966-104">Инструкции по установке или удалению подсистемы Windows для Linux в Windows 10 годовщина обновления и создателей</span><span class="sxs-lookup"><span data-stu-id="4b966-104">Guide to install or uninstall Windows Subsystem for Linux on Windows 10 Anniversary Update and Creators Update</span></span> 

<span data-ttu-id="4b966-105">Если вы используете Windows 10 для дизайнеров Update или более поздней версии, [следуйте инструкциям по установке Windows 10](install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="4b966-105">If you're running Windows 10 Creators Update or later, please [follow the Windows 10 installation instructions](install-win10.md).</span></span>

<span data-ttu-id="4b966-106"><strong><em><span style="color: #f28014">Приведенные ниже инструкции предназначены для пользователей, использующих Windows 10 с Годовщинным обновлением или Windows 10 Creators Update.</span></em></strong></span><span class="sxs-lookup"><span data-stu-id="4b966-106"><strong><em><span style="color: #f28014">The following instructions are for users running Windows 10 Anniversary Update or Windows 10 Creators Update</span></em></strong></span></span>

<span data-ttu-id="4b966-107">До обновления Windows 10 с обновлением (версия 1709) WSL был выпущен в качестве бета-версии и установил один экземпляр Ubuntu при первом запуске "Bash on Ubuntu on Windows" (или bash. exe).</span><span class="sxs-lookup"><span data-stu-id="4b966-107">Prior to Windows 10 Fall Creators Update (version 1709), WSL was released as a beta feature and installed a single Ubuntu instance when "Bash on Ubuntu on Windows" (or Bash.exe) was first run.</span></span>

> <span data-ttu-id="4b966-108">Хотя вы можете использовать WSL в предыдущих выпусках Windows 10, эта бета-версия "Legacy дистрибутив" теперь считается устаревшей.</span><span class="sxs-lookup"><span data-stu-id="4b966-108">While you CAN use WSL on earlier Windows 10 releases, this beta "legacy distro" is now considered obsolete.</span></span> <span data-ttu-id="4b966-109">Мы настоятельно рекомендуем использовать самую последнюю версию Windows 10.</span><span class="sxs-lookup"><span data-stu-id="4b966-109">We strongly encourage you to run the most recent version of Windows 10 available.</span></span> <span data-ttu-id="4b966-110">Каждый новый выпуск Windows 10 включает множество сотен исправлений и усовершенствований в WSL, позволяя правильно работать с WSL.</span><span class="sxs-lookup"><span data-stu-id="4b966-110">Each new Windows 10 release includes many hundreds of fixes and improvements in WSL alone, allowing ever more Linux tools and apps to run correctly on WSL.</span></span>

<span data-ttu-id="4b966-111">Если не удается выполнить обновление до последующего обновления или более поздней версии, выполните следующие действия, чтобы включить и использовать WSL:</span><span class="sxs-lookup"><span data-stu-id="4b966-111">If you cannot upgrade to Fall Creators Update or later, follow the steps below to enable and use WSL:</span></span>

1. <span data-ttu-id="4b966-112">Включите режим разработчика, чтобы запустить WSL в юбилейном обновлении или авторских обновлениях Windows 10, необходимо включить режим разработчика:</span><span class="sxs-lookup"><span data-stu-id="4b966-112">Turn on Developer Mode  To run WSL on Windows 10 Anniversary Update or Creators Update, you must enable Developer Mode:</span></span>

    <span data-ttu-id="4b966-113">Откройте **параметры** -> **обновления -> и безопасности** **для разработчиков**</span><span class="sxs-lookup"><span data-stu-id="4b966-113">Open **Settings** -> **Update and Security** -> **For developers**</span></span>

    <span data-ttu-id="4b966-114">Выберите переключатель режим разработчика</span><span class="sxs-lookup"><span data-stu-id="4b966-114">Select the Developer Mode radio button</span></span>  
    ![Включение режима разработчика](media/updateAndSecurity.png)

    > <span data-ttu-id="4b966-116">Требование включения режима разработчика было [удалено в обновлении Windows 10 для дизайнеров](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)</span><span class="sxs-lookup"><span data-stu-id="4b966-116">The requirement to enable Developer Mode was [removed in Windows 10 Fall Creators Update](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)</span></span>

1. <span data-ttu-id="4b966-117">Откройте командную строку.</span><span class="sxs-lookup"><span data-stu-id="4b966-117">Open a command prompt.</span></span>  <span data-ttu-id="4b966-118">Введите `bash` и нажмите клавишу ВВОД</span><span class="sxs-lookup"><span data-stu-id="4b966-118">Type `bash` and hit enter</span></span>

    <span data-ttu-id="4b966-119">При первом запуске Bash в системе Ubuntu в Windows вам будет предложено принять каноническую лицензию.</span><span class="sxs-lookup"><span data-stu-id="4b966-119">The first time you run Bash on Ubuntu on Windows, you'll be prompted to accept Canonical's license.</span></span> <span data-ttu-id="4b966-120">После принятия WSL загрузит и установит экземпляр Ubuntu на компьютере, и ярлык "Bash on Ubuntu on Windows" будет добавлен в меню "Пуск".</span><span class="sxs-lookup"><span data-stu-id="4b966-120">Once accepted, WSL will download and install the Ubuntu instance onto your machine, and a "Bash on Ubuntu on Windows" shortcut will be added to your start menu.</span></span>

    ![Запрос на установку Ubuntu](media/bashShellInstall.png)

    <span data-ttu-id="4b966-122">При первом запуске Bash в системе Ubuntu в Windows вам будет предложено создать имя пользователя и пароль UNIX.</span><span class="sxs-lookup"><span data-stu-id="4b966-122">The first time you run Bash on Ubuntu on Windows, you will be prompted to create a UNIX username and password.</span></span> <span data-ttu-id="4b966-123">Выполните [инструкции по новым экземплярам дистрибутив](initialize-distro.md) , чтобы завершить установку.</span><span class="sxs-lookup"><span data-stu-id="4b966-123">Follow the [new distro instance instructions](initialize-distro.md) to complete your installation</span></span>

1. <span data-ttu-id="4b966-124">Запустите новую оболочку Ubuntu одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="4b966-124">Launch a new Ubuntu shell by either:</span></span>
    * <span data-ttu-id="4b966-125">Запуск `bash` из командной строки</span><span class="sxs-lookup"><span data-stu-id="4b966-125">Running `bash` from a command-prompt</span></span>
    * <span data-ttu-id="4b966-126">Нажатие клавиши "Пуск" Bash в Ubuntu в Windows "</span><span class="sxs-lookup"><span data-stu-id="4b966-126">Clicking the start menu "Bash on Ubuntu on Windows" shortcut</span></span>

    
## <a name="uninstallingremoving-the-legacy-distro"></a><span data-ttu-id="4b966-127">Удаление устаревших дистрибутив</span><span class="sxs-lookup"><span data-stu-id="4b966-127">Uninstalling/Removing the legacy distro</span></span>
<span data-ttu-id="4b966-128">Если вы обновляете Windows 10 до версии для дизайнеров, начиная с предыдущего выпуска Windows 10, на котором вы установили WSL, существующие дистрибутив останутся без изменений.</span><span class="sxs-lookup"><span data-stu-id="4b966-128">If you upgrade to Windows 10 Fall Creators Update from an earlier Windows 10 release upon which you installed WSL, your existing distro will remain intact.</span></span> <span data-ttu-id="4b966-129">Однако мы настоятельно рекомендуем вам установить новое хранилище дистрибутив ASAP и перенести необходимые файлы, данные и т. д. из устаревшей дистрибутив в новую дистрибутив.</span><span class="sxs-lookup"><span data-stu-id="4b966-129">However, we STRONGLY encourage you to install a new Store-delivered distro ASAP, and migrate any necessary files, data, etc. from your legacy distro to your new distro.</span></span>

<span data-ttu-id="4b966-130">Чтобы удалить устаревшие дистрибутив с компьютера, выполните следующую команду из командной строки или экземпляра PowerShell:</span><span class="sxs-lookup"><span data-stu-id="4b966-130">To remove the legacy distro from your machine, run the following from a Command Line or PowerShell instance:</span></span>

```console
wsl --unregister Legacy
```

<span data-ttu-id="4b966-131">Если вы не используете Windows версии 1903 или более поздней, возможно, потребуется запустить `wslconfig /u Legacy` или `lxrun /uninstall /full`.</span><span class="sxs-lookup"><span data-stu-id="4b966-131">If you are not using Windows Version 1903 or higher, you may need to run `wslconfig /u Legacy` or `lxrun /uninstall /full` instead.</span></span> 

### <a name="manually-deleting-the-legacy-distro"></a><span data-ttu-id="4b966-132">Удаление устаревшей дистрибутив вручную</span><span class="sxs-lookup"><span data-stu-id="4b966-132">Manually deleting the legacy distro</span></span>
<span data-ttu-id="4b966-133">При необходимости можно вручную удалить устаревший экземпляр.</span><span class="sxs-lookup"><span data-stu-id="4b966-133">If you wish, you can manually delete your legacy instance.</span></span> <span data-ttu-id="4b966-134">Это может потребоваться при удалении устаревших дистрибутив с помощью `lxrun.exe`или при использовании обновления Windows 10 пружины 2018 (или более поздней версии), которые не поставляются с `lxrun.exe`.</span><span class="sxs-lookup"><span data-stu-id="4b966-134">This may be required if you encounter issues uninstalling the legacy distro using `lxrun.exe`, or are running Windows 10 Spring 2018 Update (or later) which do not ship with `lxrun.exe`.</span></span>

<span data-ttu-id="4b966-135">Чтобы принудительно удалить устаревшую WSL дистрибутив, удалите папку `%localappdata%\lxss\` (и все ее вложенное содержимое) с помощью проводника Windows или командной строки:</span><span class="sxs-lookup"><span data-stu-id="4b966-135">To forcefully delete your legacy WSL distro, delete the `%localappdata%\lxss\` folder (and all it's sub-contents) using Windows' File Explorer, or the command-line:</span></span>

<span data-ttu-id="4b966-136">Использование PowerShell</span><span class="sxs-lookup"><span data-stu-id="4b966-136">Using PowerShell</span></span>
```powershell
rm -Recurse $env:localappdata/lxss/
```

<span data-ttu-id="4b966-137">С помощью cmd:</span><span class="sxs-lookup"><span data-stu-id="4b966-137">Using Cmd:</span></span>
```console
DEL /S %localappdata%\lxss\
```
