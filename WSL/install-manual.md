---
title: Ручная загрузка подсистемы Windows для Linux (WSL) дистрибутивов
description: Инструкции по загрузке подсистемы Windows для дистрибутивов Linux вручную.
keywords: Башонвиндовс, bash, WSL, Windows, подсистема Windows для Linux, WSL, подсистема Windows, дистрибутив, Ubuntu, openSUSE, SLES, Debian, Kali
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: aa0b42748115045105bb4e6eae91493bfee11d09
ms.sourcegitcommit: 467b6c8e9716d1a60dbf9f7658fd9579da365b58
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/26/2020
ms.locfileid: "77624928"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a>Ручная загрузка подсистемы Windows для пакетов дистрибутив для Linux

Существует несколько сценариев, в которых может быть недоступно (или требуется) Установка WSL Linux дистрибутивов с помощью Microsoft Store. В частности, вы можете использовать номер SKU ОС Windows Server или долгосрочного обслуживания (LTSC), который не поддерживает Microsoft Store, или политики корпоративной сети и (или) администраторы, чтобы не допускать использование Microsoft Store в вашей среде.

В таких случаях, когда доступ к магазину WSL, как скачать и установить Linux дистрибутивов в WSL?

> Примечание. **среды оболочки командной строки, в том числе cmd, PowerShell и Linux/WSL дистрибутивов, не могут выполняться в режиме Windows 10 S**. Это ограничение существует, чтобы обеспечить целостность и безопасность, которые предоставляет режим S. Дополнительные сведения см. в [этой записи](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) .

## <a name="downloading-distros"></a>Скачивание дистрибутивов

Если Microsoft Store приложение недоступно, вы можете скачать и вручную установить дистрибутивов Linux, щелкнув следующие ссылки:
<!-- * [Ubuntu 18.04](https://aka.ms/wsl-ubuntu-1804)
* [Ubuntu 18.04 ARM](https://aka.ms/wsl-ubuntu-1804-arm) -->
* Ubuntu 18,04
* Ubuntu 18,04 ARM
* [Ubuntu 16,04](https://aka.ms/wsl-ubuntu-1604)
* [Debian GNU/Linux](https://aka.ms/wsl-debian-gnulinux)
* [Kali Linux](https://aka.ms/wsl-kali-linux-new)
* [OpenSUSE Leap 42](https://aka.ms/wsl-opensuse-42)
* [SUSE Linux Enterprise Server 12](https://aka.ms/wsl-sles-12)
* [Fedora Remix for WSL](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

Это приведет к скачиванию пакетов `<distro>.appx` в выбранную папку. Следуйте [инструкциям по установке](#installing-your-distro) , чтобы установить Скачанные дистрибутив.

## <a name="downloading-distros-via-the-command-line"></a>Скачивание дистрибутивов с помощью командной строки
При желании вы также можете скачать предпочтительные дистрибутив с помощью командной строки:

 ### <a name="download-using-powershell"></a>Скачать с помощью PowerShell
 Чтобы скачать дистрибутивов с помощью PowerShell, используйте командлет [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) . Ниже приведен пример инструкции по скачиванию Ubuntu 16,04.

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> Если загрузка занимает много времени, отключите индикатор выполнения, задав `$ProgressPreference = 'SilentlyContinue'`

### <a name="download-using-curl"></a>Скачать с помощью функции "перелистывание"
Обновление Windows 10 пружины 2018 (или более поздней версии) включает в себя популярную [программу командной строки](https://curl.haxx.se/) , с помощью которой можно вызывать веб-запросы (например, команды HTTP GET, POST, WHERE и т. д.) из командной строки. Вы можете использовать `curl.exe`, чтобы скачать приведенную выше дистрибутивов:

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

В приведенном выше примере выполняется `curl.exe` (не только `curl`), чтобы убедиться, что в PowerShell вызывается фактический исполняемый файл, а не псевдоним PowerShell для [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6) .

> Примечание. Использование `curl` может быть предпочтительнее, если необходимо вызвать или создать скрипт для загрузки с помощью оболочки cmd и (или) `.bat` / `.cmd` сценариев.

## <a name="installing-your-distro"></a>Установка дистрибутив
Если вы используете Windows 10, вы можете установить дистрибутив с помощью PowerShell. Просто перейдите в папку, содержащую дистрибутив, скачанный выше, и в этом каталоге выполните следующую команду, где `app_name` — имя файла дистрибутив. appx.  
```Powershell
Add-AppxPackage .\app_name.appx
```

Если вы используете Windows Server, инструкции по установке можно найти на странице документации по [Windows Server](install-on-server.md) .

После установки дистрибутив ознакомьтесь со страницей [этапы инициализации](initialize-distro.md) , чтобы инициализировать новый дистрибутив.
