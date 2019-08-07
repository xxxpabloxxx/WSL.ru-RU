---
title: Ручная загрузка подсистемы Windows для Linux (WSL) дистрибутивов
description: Инструкции по загрузке подсистемы Windows для дистрибутивов Linux вручную.
keywords: Башонвиндовс, bash, WSL, Windows, подсистема Windows для Linux, WSL, подсистема Windows, дистрибутив, Ubuntu, openSUSE, SLES, Debian, Kali
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: ded81ec9672d75203e0d289c551c86cd90bde606
ms.sourcegitcommit: 9175a28f04573f25338358faf61d73b1a5d1ade6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2019
ms.locfileid: "68832094"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a><span data-ttu-id="d0c7b-104">Ручная загрузка подсистемы Windows для пакетов дистрибутив для Linux</span><span class="sxs-lookup"><span data-stu-id="d0c7b-104">Manually download Windows Subsystem for Linux distro packages</span></span>

<span data-ttu-id="d0c7b-105">Существует несколько сценариев, в которых может быть недоступно (или требуется) Установка WSL Linux дистрибутивов с помощью Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="d0c7b-105">There are several scenarios in which you may not be able (or want) to, install WSL Linux distros via the Microsoft Store.</span></span> <span data-ttu-id="d0c7b-106">В частности, вы можете использовать номер SKU ОС Windows Server или долгосрочного обслуживания (LTSC), который не поддерживает Microsoft Store, или политики корпоративной сети и (или) администраторы, чтобы не допускать использование Microsoft Store в вашей среде.</span><span class="sxs-lookup"><span data-stu-id="d0c7b-106">Specifically, you may be running a Windows Server or Long-Term Servicing (LTSC) desktop OS SKU that doesn't support Microsoft Store, or your corporate network policies and/or admins to not permit Microsoft Store usage in your environment.</span></span>

<span data-ttu-id="d0c7b-107">В таких случаях, когда доступ к магазину WSL, как скачать и установить Linux дистрибутивов в WSL?</span><span class="sxs-lookup"><span data-stu-id="d0c7b-107">In these cases, while WSL itself is available, how do you download and install Linux distros in WSL if you can't access the store?</span></span>

> <span data-ttu-id="d0c7b-108">Примечание. **Среды оболочки командной строки, в том числе cmd, PowerShell и Linux/WSL дистрибутивов, не могут выполняться в режиме Windows 10 S**.</span><span class="sxs-lookup"><span data-stu-id="d0c7b-108">Note: **Command-line shell environments including Cmd, PowerShell, and Linux/WSL distros are not permitted to run on Windows 10 S Mode**.</span></span> <span data-ttu-id="d0c7b-109">Это ограничение существует, чтобы обеспечить целостность и безопасность, которые предоставляет режим S: Дополнительные сведения см. в [этой записи](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) .</span><span class="sxs-lookup"><span data-stu-id="d0c7b-109">This restriction exists in order to ensure the integrity and safety goals that S Mode delivers: Read [this post](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) for more information.</span></span>

## <a name="downloading-distros"></a><span data-ttu-id="d0c7b-110">Скачивание дистрибутивов</span><span class="sxs-lookup"><span data-stu-id="d0c7b-110">Downloading distros</span></span>

<span data-ttu-id="d0c7b-111">Если Microsoft Store приложение недоступно, вы можете скачать и вручную установить дистрибутивов Linux, щелкнув следующие ссылки:</span><span class="sxs-lookup"><span data-stu-id="d0c7b-111">If the Microsoft Store app is not available, you can download and manually install Linux distros by clicking these links:</span></span>
* [<span data-ttu-id="d0c7b-112">Ubuntu 18,04</span><span class="sxs-lookup"><span data-stu-id="d0c7b-112">Ubuntu 18.04</span></span>](https://aka.ms/wsl-ubuntu-1804)
* [<span data-ttu-id="d0c7b-113">Ubuntu 18,04 ARM</span><span class="sxs-lookup"><span data-stu-id="d0c7b-113">Ubuntu 18.04 ARM</span></span>](https://aka.ms/wsl-ubuntu-1804-arm)
* [<span data-ttu-id="d0c7b-114">Ubuntu 16,04</span><span class="sxs-lookup"><span data-stu-id="d0c7b-114">Ubuntu 16.04</span></span>](https://aka.ms/wsl-ubuntu-1604)
* [<span data-ttu-id="d0c7b-115">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="d0c7b-115">Debian GNU/Linux</span></span>](https://aka.ms/wsl-debian-gnulinux)
* [<span data-ttu-id="d0c7b-116">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="d0c7b-116">Kali Linux</span></span>](https://aka.ms/wsl-kali-linux-new)
* [<span data-ttu-id="d0c7b-117">OpenSUSE LEAP 42</span><span class="sxs-lookup"><span data-stu-id="d0c7b-117">OpenSUSE Leap 42</span></span>](https://aka.ms/wsl-opensuse-42)
* [<span data-ttu-id="d0c7b-118">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="d0c7b-118">SUSE Linux Enterprise Server 12</span></span>](https://aka.ms/wsl-sles-12)
* [<span data-ttu-id="d0c7b-119">Fedora Remix для WSL</span><span class="sxs-lookup"><span data-stu-id="d0c7b-119">Fedora Remix for WSL</span></span>](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

<span data-ttu-id="d0c7b-120">Это приведет `<distro>.appx` к скачиванию пакетов в выбранную папку.</span><span class="sxs-lookup"><span data-stu-id="d0c7b-120">This will cause the `<distro>.appx` packages to download to a folder of your choosing.</span></span> <span data-ttu-id="d0c7b-121">Следуйте [инструкциям по установке](#Installing-your-distro) , чтобы установить Скачанные дистрибутив.</span><span class="sxs-lookup"><span data-stu-id="d0c7b-121">Follow the [installation instructions](#Installing-your-distro) to install your downloaded distro(s).</span></span>

## <a name="downloading-distros-via-the-command-line"></a><span data-ttu-id="d0c7b-122">Скачивание дистрибутивов с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="d0c7b-122">Downloading distros via the command line</span></span>
<span data-ttu-id="d0c7b-123">При желании вы также можете скачать предпочтительные дистрибутив с помощью командной строки:</span><span class="sxs-lookup"><span data-stu-id="d0c7b-123">If you prefer, you can also download your preferred distro(s) via the command line:</span></span>

 ### <a name="download-using-powershell"></a><span data-ttu-id="d0c7b-124">Скачать с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="d0c7b-124">Download using PowerShell</span></span>
 <span data-ttu-id="d0c7b-125">Чтобы скачать дистрибутивов с помощью PowerShell, используйте командлет [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) .</span><span class="sxs-lookup"><span data-stu-id="d0c7b-125">To download distros using PowerShell, use the [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet.</span></span> <span data-ttu-id="d0c7b-126">Ниже приведен пример инструкции по скачиванию Ubuntu 16,04.</span><span class="sxs-lookup"><span data-stu-id="d0c7b-126">Here's a sample instruction to download Ubuntu 16.04.</span></span>

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> <span data-ttu-id="d0c7b-127">Если загрузка занимает много времени, отключите индикатор выполнения, задав`$ProgressPreference = 'SilentlyContinue'`</span><span class="sxs-lookup"><span data-stu-id="d0c7b-127">If the download is taking a long time, turn off the progress bar by setting `$ProgressPreference = 'SilentlyContinue'`</span></span>

### <a name="download-using-curl"></a><span data-ttu-id="d0c7b-128">Скачать с помощью функции "перелистывание"</span><span class="sxs-lookup"><span data-stu-id="d0c7b-128">Download using curl</span></span>
<span data-ttu-id="d0c7b-129">Обновление Windows 10 пружины 2018 (или более поздней версии) включает в себя популярную [программу командной строки](https://curl.haxx.se/) , с помощью которой можно вызывать веб-запросы (например, команды HTTP GET, POST, WHERE и т. д.) из командной строки.</span><span class="sxs-lookup"><span data-stu-id="d0c7b-129">Windows 10 Spring 2018 Update (or later) includes the popular [curl command-line utility](https://curl.haxx.se/) with which you can invoke web requests (i.e. HTTP GET, POST, PUT, etc. commands) from the command line.</span></span> <span data-ttu-id="d0c7b-130">Можно использовать `curl.exe` для загрузки указанного выше дистрибутивов:</span><span class="sxs-lookup"><span data-stu-id="d0c7b-130">You can use `curl.exe` to download the above distros:</span></span>

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

<span data-ttu-id="d0c7b-131">В приведенном выше примере `curl.exe` выполняется (не только `curl`), чтобы убедиться в том, что в PowerShell вызывается фактический исполняемый файл, а не псевдоним оболочки PowerShell для [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6) .</span><span class="sxs-lookup"><span data-stu-id="d0c7b-131">In the above example, `curl.exe` is executed (not just `curl`) to ensure that, in PowerShell, the real curl executable is invoked, not the PowerShell curl alias for [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)</span></span>

> <span data-ttu-id="d0c7b-132">Примечание. Использование `curl` может быть предпочтительным, если необходимо вызвать или создать скрипт для загрузки с помощью оболочки `.bat`  /  `.cmd` cmd или сценариев.</span><span class="sxs-lookup"><span data-stu-id="d0c7b-132">Note: Using `curl` might be preferable if you have to invoke/script download steps using Cmd shell and/or `.bat` / `.cmd` scripts.</span></span>

## <a name="installing-your-distro"></a><span data-ttu-id="d0c7b-133">Установка дистрибутив</span><span class="sxs-lookup"><span data-stu-id="d0c7b-133">Installing your distro</span></span>
<span data-ttu-id="d0c7b-134">Если вы используете Windows 10, вы можете установить дистрибутив с помощью PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d0c7b-134">If you're using Windows 10 you can install your distro with PowerShell.</span></span> <span data-ttu-id="d0c7b-135">Просто перейдите в папку, содержащую дистрибутив, скачанный выше, и в этом каталоге выполните следующую команду, `app_name` где — это имя файла дистрибутив. appx.</span><span class="sxs-lookup"><span data-stu-id="d0c7b-135">Simply navigate to folder containing the distro downloaded from above, and in that directory run the following command where `app_name` is the name of your distro .appx file.</span></span>  
```Powershell
Add-AppxPackage .\app_name.appx
```

<span data-ttu-id="d0c7b-136">Если вы используете Windows Server, инструкции по установке можно найти на странице документации по [Windows Server](install-on-server.md) .</span><span class="sxs-lookup"><span data-stu-id="d0c7b-136">If you are using Windows server you can find the install instructions on the [Windows Server](install-on-server.md) documentation page.</span></span>

<span data-ttu-id="d0c7b-137">После установки дистрибутив ознакомьтесь со страницей [действия интилизатион](initialize-distro.md) , чтобы инициализировать новый дистрибутив.</span><span class="sxs-lookup"><span data-stu-id="d0c7b-137">Once your distro is installed please refer to the [Intilization Steps](initialize-distro.md) page to initialize your new distro.</span></span>
