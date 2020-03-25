---
title: Скачивание дистрибутивов подсистемы Windows для Linux (WSL) вручную
description: Инструкции по скачиванию дистрибутивов подсистемы Windows для Linux вручную.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, WSL, подсистема windows, дистрибутив, ubuntu, openSUSE, SLES, debian, kali
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: aa0b42748115045105bb4e6eae91493bfee11d09
ms.sourcegitcommit: 467b6c8e9716d1a60dbf9f7658fd9579da365b58
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/26/2020
ms.locfileid: "77624928"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a><span data-ttu-id="a17bc-104">Скачивание пакетов дистрибутива подсистемы Windows для Linux вручную</span><span class="sxs-lookup"><span data-stu-id="a17bc-104">Manually download Windows Subsystem for Linux distro packages</span></span>

<span data-ttu-id="a17bc-105">Существует несколько сценариев, в которых вы не сможете (или не захотите) устанавливать дистрибутивы WSL Linux с помощью Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="a17bc-105">There are several scenarios in which you may not be able (or want) to, install WSL Linux distros via the Microsoft Store.</span></span> <span data-ttu-id="a17bc-106">В частности, вы можете использовать номер SKU классической ОС Windows Server или Long-Term Servicing (LTSC), который не поддерживает Microsoft Store, или политики корпоративной сети и административные параметры, запрещающие использовать Microsoft Store в вашей среде.</span><span class="sxs-lookup"><span data-stu-id="a17bc-106">Specifically, you may be running a Windows Server or Long-Term Servicing (LTSC) desktop OS SKU that doesn't support Microsoft Store, or your corporate network policies and/or admins to not permit Microsoft Store usage in your environment.</span></span>

<span data-ttu-id="a17bc-107">В таких случаях, когда подсистема WSL доступна, как скачать и установить дистрибутивы Linux в WSL, если нет доступа к магазину?</span><span class="sxs-lookup"><span data-stu-id="a17bc-107">In these cases, while WSL itself is available, how do you download and install Linux distros in WSL if you can't access the store?</span></span>

> <span data-ttu-id="a17bc-108">Примечание. **Среды оболочки командной строки, в том числе дистрибутивы Linux/WSL, Cmd и PowerShell не могут выполняться в S-режиме Windows 10**.</span><span class="sxs-lookup"><span data-stu-id="a17bc-108">Note: **Command-line shell environments including Cmd, PowerShell, and Linux/WSL distros are not permitted to run on Windows 10 S Mode**.</span></span> <span data-ttu-id="a17bc-109">Это ограничение существует, чтобы обеспечить целостность и безопасность, которые предоставляет S-режим. Дополнительные сведения см. в [этой записи блога](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/).</span><span class="sxs-lookup"><span data-stu-id="a17bc-109">This restriction exists in order to ensure the integrity and safety goals that S Mode delivers: Read [this post](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) for more information.</span></span>

## <a name="downloading-distros"></a><span data-ttu-id="a17bc-110">Скачивание дистрибутивов</span><span class="sxs-lookup"><span data-stu-id="a17bc-110">Downloading distros</span></span>

<span data-ttu-id="a17bc-111">Если приложение Microsoft Store недоступно, вы можете скачать и вручную установить дистрибутивы Linux, щелкнув следующие ссылки:</span><span class="sxs-lookup"><span data-stu-id="a17bc-111">If the Microsoft Store app is not available, you can download and manually install Linux distros by clicking these links:</span></span>
<!-- * [Ubuntu 18.04](https://aka.ms/wsl-ubuntu-1804)
* [Ubuntu 18.04 ARM](https://aka.ms/wsl-ubuntu-1804-arm) -->
* <span data-ttu-id="a17bc-112">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="a17bc-112">Ubuntu 18.04</span></span>
* <span data-ttu-id="a17bc-113">Ubuntu 18.04 ARM</span><span class="sxs-lookup"><span data-stu-id="a17bc-113">Ubuntu 18.04 ARM</span></span>
* [<span data-ttu-id="a17bc-114">Ubuntu 16.04</span><span class="sxs-lookup"><span data-stu-id="a17bc-114">Ubuntu 16.04</span></span>](https://aka.ms/wsl-ubuntu-1604)
* [<span data-ttu-id="a17bc-115">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="a17bc-115">Debian GNU/Linux</span></span>](https://aka.ms/wsl-debian-gnulinux)
* [<span data-ttu-id="a17bc-116">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="a17bc-116">Kali Linux</span></span>](https://aka.ms/wsl-kali-linux-new)
* [<span data-ttu-id="a17bc-117">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="a17bc-117">OpenSUSE Leap 42</span></span>](https://aka.ms/wsl-opensuse-42)
* [<span data-ttu-id="a17bc-118">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="a17bc-118">SUSE Linux Enterprise Server 12</span></span>](https://aka.ms/wsl-sles-12)
* [<span data-ttu-id="a17bc-119">Fedora Remix for WSL</span><span class="sxs-lookup"><span data-stu-id="a17bc-119">Fedora Remix for WSL</span></span>](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

<span data-ttu-id="a17bc-120">Это приведет к скачиванию пакетов `<distro>.appx` в выбранную папку.</span><span class="sxs-lookup"><span data-stu-id="a17bc-120">This will cause the `<distro>.appx` packages to download to a folder of your choosing.</span></span> <span data-ttu-id="a17bc-121">Следуйте [инструкциям по установке](#installing-your-distro) скачанных дистрибутивов.</span><span class="sxs-lookup"><span data-stu-id="a17bc-121">Follow the [installation instructions](#installing-your-distro) to install your downloaded distro(s).</span></span>

## <a name="downloading-distros-via-the-command-line"></a><span data-ttu-id="a17bc-122">Скачивание дистрибутивов с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="a17bc-122">Downloading distros via the command line</span></span>
<span data-ttu-id="a17bc-123">При желании вы также можете скачать предпочтительные дистрибутивы с помощью командной строки.</span><span class="sxs-lookup"><span data-stu-id="a17bc-123">If you prefer, you can also download your preferred distro(s) via the command line:</span></span>

 ### <a name="download-using-powershell"></a><span data-ttu-id="a17bc-124">Скачивание с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="a17bc-124">Download using PowerShell</span></span>
 <span data-ttu-id="a17bc-125">Чтобы скачать дистрибутивы с помощью PowerShell, используйте командлет [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest).</span><span class="sxs-lookup"><span data-stu-id="a17bc-125">To download distros using PowerShell, use the [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet.</span></span> <span data-ttu-id="a17bc-126">Ниже приведены инструкции по скачиванию Ubuntu 16.04.</span><span class="sxs-lookup"><span data-stu-id="a17bc-126">Here's a sample instruction to download Ubuntu 16.04.</span></span>

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> <span data-ttu-id="a17bc-127">Если загрузка занимает много времени, выключите индикатор выполнения, задав `$ProgressPreference = 'SilentlyContinue'`.</span><span class="sxs-lookup"><span data-stu-id="a17bc-127">If the download is taking a long time, turn off the progress bar by setting `$ProgressPreference = 'SilentlyContinue'`</span></span>

### <a name="download-using-curl"></a><span data-ttu-id="a17bc-128">Скачивание с помощью cURL</span><span class="sxs-lookup"><span data-stu-id="a17bc-128">Download using curl</span></span>
<span data-ttu-id="a17bc-129">Обновление Windows 10 Spring 2018 (или более поздней версии) содержит популярную [служебную программу командной строки cURL](https://curl.haxx.se/), с помощью которой можно вызывать веб-запросы (например, команды HTTP GET, POST, PUT и т. д.) из командной строки.</span><span class="sxs-lookup"><span data-stu-id="a17bc-129">Windows 10 Spring 2018 Update (or later) includes the popular [curl command-line utility](https://curl.haxx.se/) with which you can invoke web requests (i.e. HTTP GET, POST, PUT, etc. commands) from the command line.</span></span> <span data-ttu-id="a17bc-130">Вы можете использовать `curl.exe`, чтобы скачать приведенные выше дистрибутивы:</span><span class="sxs-lookup"><span data-stu-id="a17bc-130">You can use `curl.exe` to download the above distros:</span></span>

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

<span data-ttu-id="a17bc-131">В приведенном выше примере выполняется `curl.exe` (а не только `curl`), чтобы убедиться, что в PowerShell вызывается реальный исполняемый файл cURL, а не его псевдоним для [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6).</span><span class="sxs-lookup"><span data-stu-id="a17bc-131">In the above example, `curl.exe` is executed (not just `curl`) to ensure that, in PowerShell, the real curl executable is invoked, not the PowerShell curl alias for [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)</span></span>

> <span data-ttu-id="a17bc-132">Примечание. Использование `curl` может быть предпочтительным, если необходимо вызвать или создать сценарий для скачивания с помощью командлетов командной строки и сценариев `.bat` / `.cmd`.</span><span class="sxs-lookup"><span data-stu-id="a17bc-132">Note: Using `curl` might be preferable if you have to invoke/script download steps using Cmd shell and/or `.bat` / `.cmd` scripts.</span></span>

## <a name="installing-your-distro"></a><span data-ttu-id="a17bc-133">Установка дистрибутива</span><span class="sxs-lookup"><span data-stu-id="a17bc-133">Installing your distro</span></span>
<span data-ttu-id="a17bc-134">Если вы используете Windows 10, вы можете установить дистрибутив с помощью PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a17bc-134">If you're using Windows 10 you can install your distro with PowerShell.</span></span> <span data-ttu-id="a17bc-135">Просто перейдите в папку, содержащую скачанный выше дистрибутив, и в этом каталоге выполните следующую команду, в которой `app_name` — это имя APPX-файла дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="a17bc-135">Simply navigate to folder containing the distro downloaded from above, and in that directory run the following command where `app_name` is the name of your distro .appx file.</span></span>  
```Powershell
Add-AppxPackage .\app_name.appx
```

<span data-ttu-id="a17bc-136">Если вы используете сервер Windows, инструкции по установке можно найти на странице документации [Windows Server](install-on-server.md).</span><span class="sxs-lookup"><span data-stu-id="a17bc-136">If you are using Windows server you can find the install instructions on the [Windows Server](install-on-server.md) documentation page.</span></span>

<span data-ttu-id="a17bc-137">После установки дистрибутива ознакомьтесь со страницей c [этапами инициализации](initialize-distro.md), чтобы инициализировать новый дистрибутив.</span><span class="sxs-lookup"><span data-stu-id="a17bc-137">Once your distro is installed please refer to the [Initialization Steps](initialize-distro.md) page to initialize your new distro.</span></span>
