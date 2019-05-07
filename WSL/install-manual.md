---
title: Вручную Загрузите подсистемы Windows для дистрибутивов Linux (WSL)
description: Инструкции по как вручную загрузить подсистемы Windows для дистрибутивов Linux.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, WSL, подсистеме windows дистрибутива, ubuntu, openSUSE, SLES, debian, kali
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: be1c1331183317d4f970696464110b9968208d21
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063572"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a><span data-ttu-id="6f4dc-104">Скачивание подсистемы Windows для пакетов дистрибутив Linux вручную</span><span class="sxs-lookup"><span data-stu-id="6f4dc-104">Manually download Windows Subsystem for Linux distro packages</span></span>

<span data-ttu-id="6f4dc-105">Существует несколько сценариев, в которых может не удастся (или хотите), устанавливаемого дистрибутивов WSL Linux через Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="6f4dc-105">There are several scenarios in which you may not be able (or want) to, install WSL Linux distros via the Microsoft Store.</span></span> <span data-ttu-id="6f4dc-106">В частности вы может работать под управлением Windows Server или Long-Term Servicing (LTSB или LTSC) desktop SKU операционной системы, который не поддерживает Microsoft Store или вашей корпоративной сети политик и/или "Администраторы" не допускать использование Microsoft Store в вашей среде.</span><span class="sxs-lookup"><span data-stu-id="6f4dc-106">Specifically, you may be running a Windows Server or Long-Term Servicing (LTSB/LTSC) desktop OS SKU that doesn't support Microsoft Store, or your corporate network policies and/or admins to not permit Microsoft Store usage in your environment.</span></span>

<span data-ttu-id="6f4dc-107">В этих случаях то время как WSL сам доступен, как загрузить и установить в WSL дистрибутивов Linux, если нет доступа к хранилищу?</span><span class="sxs-lookup"><span data-stu-id="6f4dc-107">In these cases, while WSL itself is available, how do you download and install Linux distros in WSL if you can't access the store?</span></span>

> <span data-ttu-id="6f4dc-108">Примечание. **Оболочка командной строки сред, включая дистрибутивов Linux, WSL, Cmd и PowerShell не допускаются под управлением Windows 10 S режим**.</span><span class="sxs-lookup"><span data-stu-id="6f4dc-108">Note: **Command-line shell environments including Cmd, PowerShell, and Linux/WSL distros are not permitted to run on Windows 10 S Mode**.</span></span> <span data-ttu-id="6f4dc-109">Это ограничение существует, чтобы обеспечить целостность и безопасность цели, которые предоставляет режим S: Чтение [блога](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) Дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="6f4dc-109">This restriction exists in order to ensure the integrity and safety goals that S Mode delivers: Read [this post](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) for more information.</span></span>

## <a name="downloading-distros"></a><span data-ttu-id="6f4dc-110">Загрузка дистрибутивы</span><span class="sxs-lookup"><span data-stu-id="6f4dc-110">Downloading distros</span></span>

<span data-ttu-id="6f4dc-111">Если приложение Microsoft Store недоступен, можно загрузить и установить дистрибутивов Linux вручную с помощью этих ссылок:</span><span class="sxs-lookup"><span data-stu-id="6f4dc-111">If the Microsoft Store app is not available, you can download and manually install Linux distros by clicking these links:</span></span>
* [<span data-ttu-id="6f4dc-112">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="6f4dc-112">Ubuntu 18.04</span></span>](https://aka.ms/wsl-ubuntu-1804)
* [<span data-ttu-id="6f4dc-113">Ubuntu 18.04 ARM</span><span class="sxs-lookup"><span data-stu-id="6f4dc-113">Ubuntu 18.04 ARM</span></span>](https://aka.ms/wsl-ubuntu-1804-arm)
* [<span data-ttu-id="6f4dc-114">Ubuntu 16.04</span><span class="sxs-lookup"><span data-stu-id="6f4dc-114">Ubuntu 16.04</span></span>](https://aka.ms/wsl-ubuntu-1604)
* [<span data-ttu-id="6f4dc-115">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="6f4dc-115">Debian GNU/Linux</span></span>](https://aka.ms/wsl-debian-gnulinux)
* [<span data-ttu-id="6f4dc-116">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="6f4dc-116">Kali Linux</span></span>](https://aka.ms/wsl-kali-linux)
* [<span data-ttu-id="6f4dc-117">openSUSE</span><span class="sxs-lookup"><span data-stu-id="6f4dc-117">OpenSUSE</span></span>](https://aka.ms/wsl-opensuse-42)
* [<span data-ttu-id="6f4dc-118">SLES</span><span class="sxs-lookup"><span data-stu-id="6f4dc-118">SLES</span></span>](https://aka.ms/wsl-sles-12)

<span data-ttu-id="6f4dc-119">Это приведет к `<distro>.appx` пакетов для скачивания в папку по своему выбору.</span><span class="sxs-lookup"><span data-stu-id="6f4dc-119">This will cause the `<distro>.appx` packages to download to a folder of your choosing.</span></span> <span data-ttu-id="6f4dc-120">Выполните [инструкции по установке](#installing-your-distro) для установки вашей Скачанный distro(s).</span><span class="sxs-lookup"><span data-stu-id="6f4dc-120">Follow the [installation instructions](#installing-your-distro) to install your downloaded distro(s).</span></span>

## <a name="downloading-distros-via-the-command-line"></a><span data-ttu-id="6f4dc-121">Загрузка дистрибутивов с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="6f4dc-121">Downloading distros via the command line</span></span>
<span data-ttu-id="6f4dc-122">При желании вы также можете скачать Ваш предпочитаемый distro(s) через командную строку:</span><span class="sxs-lookup"><span data-stu-id="6f4dc-122">If you prefer, you can also download your preferred distro(s) via the command line:</span></span>

 ### <a name="download-using-powershell"></a><span data-ttu-id="6f4dc-123">Скачать с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f4dc-123">Download using PowerShell</span></span>
 <span data-ttu-id="6f4dc-124">Чтобы скачать дистрибутивов, с помощью PowerShell, используйте [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) командлета.</span><span class="sxs-lookup"><span data-stu-id="6f4dc-124">To download distros using PowerShell, use the [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet.</span></span> <span data-ttu-id="6f4dc-125">Ниже приведен пример инструкции для загрузки Ubuntu 16.04.</span><span class="sxs-lookup"><span data-stu-id="6f4dc-125">Here's a sample instruction to download Ubuntu 16.04.</span></span>

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> <span data-ttu-id="6f4dc-126">Если загрузка занимает много времени, отключите индикатор хода выполнения, задав `$ProgressPreference = 'SilentlyContinue'`</span><span class="sxs-lookup"><span data-stu-id="6f4dc-126">If the download is taking a long time, turn off the progress bar by setting `$ProgressPreference = 'SilentlyContinue'`</span></span>

### <a name="download-using-curl"></a><span data-ttu-id="6f4dc-127">Скачайте с помощью curl</span><span class="sxs-lookup"><span data-stu-id="6f4dc-127">Download using curl</span></span>
<span data-ttu-id="6f4dc-128">Windows 10 весна 2018 с обновлением (или более поздней версии) включает в себя популярные [программы командной строки curl](https://curl.haxx.se/) с помощью которого можно вызвать веб-запросов (т. е. HTTP GET, POST, PUT, команды и т.д.) из командной строки.</span><span class="sxs-lookup"><span data-stu-id="6f4dc-128">Windows 10 Spring 2018 Update (or later) includes the popular [curl command-line utility](https://curl.haxx.se/) with which you can invoke web requests (i.e. HTTP GET, POST, PUT, etc. commands) from the command line.</span></span> <span data-ttu-id="6f4dc-129">Можно использовать `curl.exe` для загрузки выше дистрибутивов:</span><span class="sxs-lookup"><span data-stu-id="6f4dc-129">You can use `curl.exe` to download the above distros:</span></span>

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

<span data-ttu-id="6f4dc-130">В приведенном выше примере `curl.exe` выполняется (а не только `curl`) для обеспечения, в PowerShell, исполняемый файл реальных curl вызове не curl PowerShell псевдоним для [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)</span><span class="sxs-lookup"><span data-stu-id="6f4dc-130">In the above example, `curl.exe` is executed (not just `curl`) to ensure that, in PowerShell, the real curl executable is invoked, not the PowerShell curl alias for [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)</span></span>

> <span data-ttu-id="6f4dc-131">Примечание. С помощью `curl` , можно использовать в том случае, если необходимо вызвать скрипт действия загрузки, с помощью командной оболочки расширенных процедур и/или `.bat`  /  `.cmd` сценариев.</span><span class="sxs-lookup"><span data-stu-id="6f4dc-131">Note: Using `curl` might be preferable if you have to invoke/script download steps using Cmd shell and/or `.bat` / `.cmd` scripts.</span></span>

## <a name="installing-your-distro"></a><span data-ttu-id="6f4dc-132">Установка вашего дистрибутива</span><span class="sxs-lookup"><span data-stu-id="6f4dc-132">Installing your distro</span></span>
<span data-ttu-id="6f4dc-133">Инструкции по установке вашей Скачанный distro(s), обратитесь к [Windows Desktop](install-win10.md) или [Windows Server](install-on-server.md) инструкции по установке.</span><span class="sxs-lookup"><span data-stu-id="6f4dc-133">For instructions on how to install your downloaded distro(s), please refer to the [Windows Desktop](install-win10.md) or [Windows Server](install-on-server.md) installation instructions.</span></span>
