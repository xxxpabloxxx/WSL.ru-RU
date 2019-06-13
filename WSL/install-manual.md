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
ms.openlocfilehash: 669c017c97aba70c107484b32acd99296265d84a
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/12/2019
ms.locfileid: "67035038"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a>Скачивание подсистемы Windows для пакетов дистрибутив Linux вручную

Существует несколько сценариев, в которых может не удастся (или хотите), устанавливаемого дистрибутивов WSL Linux через Microsoft Store. В частности вы может работать под управлением Windows Server или Long-Term Servicing (LTSB или LTSC) desktop SKU операционной системы, который не поддерживает Microsoft Store или вашей корпоративной сети политик и/или "Администраторы" не допускать использование Microsoft Store в вашей среде.

В этих случаях то время как WSL сам доступен, как загрузить и установить в WSL дистрибутивов Linux, если нет доступа к хранилищу?

> Примечание. **Оболочка командной строки сред, включая дистрибутивов Linux, WSL, Cmd и PowerShell не допускаются под управлением Windows 10 S режим**. Это ограничение существует, чтобы обеспечить целостность и безопасность цели, которые предоставляет режим S: Чтение [блога](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) Дополнительные сведения.

## <a name="downloading-distros"></a>Загрузка дистрибутивы

Если приложение Microsoft Store недоступен, можно загрузить и установить дистрибутивов Linux вручную с помощью этих ссылок:
* [Ubuntu 18.04](https://aka.ms/wsl-ubuntu-1804)
* [Ubuntu 18.04 ARM](https://aka.ms/wsl-ubuntu-1804-arm)
* [Ubuntu 16.04](https://aka.ms/wsl-ubuntu-1604)
* [Debian GNU/Linux](https://aka.ms/wsl-debian-gnulinux)
* [Kali Linux](https://aka.ms/wsl-kali-linux)
* [OpenSUSE Leap 42](https://aka.ms/wsl-opensuse-42)
* [SUSE Linux Enterprise Server 12](https://aka.ms/wsl-sles-12)
* [Remix Fedora для WSL](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

Это приведет к `<distro>.appx` пакетов для скачивания в папку по своему выбору. Выполните [инструкции по установке](#installing-your-distro) для установки вашей Скачанный distro(s).

## <a name="downloading-distros-via-the-command-line"></a>Загрузка дистрибутивов с помощью командной строки
При желании вы также можете скачать Ваш предпочитаемый distro(s) через командную строку:

 ### <a name="download-using-powershell"></a>Скачать с помощью PowerShell
 Чтобы скачать дистрибутивов, с помощью PowerShell, используйте [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) командлета. Ниже приведен пример инструкции для загрузки Ubuntu 16.04.

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> Если загрузка занимает много времени, отключите индикатор хода выполнения, задав `$ProgressPreference = 'SilentlyContinue'`

### <a name="download-using-curl"></a>Скачайте с помощью curl
Windows 10 весна 2018 с обновлением (или более поздней версии) включает в себя популярные [программы командной строки curl](https://curl.haxx.se/) с помощью которого можно вызвать веб-запросов (т. е. HTTP GET, POST, PUT, команды и т.д.) из командной строки. Можно использовать `curl.exe` для загрузки выше дистрибутивов:

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

В приведенном выше примере `curl.exe` выполняется (а не только `curl`) для обеспечения, в PowerShell, исполняемый файл реальных curl вызове не curl PowerShell псевдоним для [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)

> Примечание. С помощью `curl` , можно использовать в том случае, если необходимо вызвать скрипт действия загрузки, с помощью командной оболочки расширенных процедур и/или `.bat`  /  `.cmd` сценариев.

## <a name="installing-your-distro"></a>Установка вашего дистрибутива
Инструкции по установке вашей Скачанный distro(s), обратитесь к [Windows Desktop](install-win10.md) или [Windows Server](install-on-server.md) инструкции по установке.
