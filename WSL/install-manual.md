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
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a>Скачивание пакетов дистрибутива подсистемы Windows для Linux вручную

Существует несколько сценариев, в которых вы не сможете (или не захотите) устанавливать дистрибутивы WSL Linux с помощью Microsoft Store. В частности, вы можете использовать номер SKU классической ОС Windows Server или Long-Term Servicing (LTSC), который не поддерживает Microsoft Store, или политики корпоративной сети и административные параметры, запрещающие использовать Microsoft Store в вашей среде.

В таких случаях, когда подсистема WSL доступна, как скачать и установить дистрибутивы Linux в WSL, если нет доступа к магазину?

> Примечание. **Среды оболочки командной строки, в том числе дистрибутивы Linux/WSL, Cmd и PowerShell не могут выполняться в S-режиме Windows 10**. Это ограничение существует, чтобы обеспечить целостность и безопасность, которые предоставляет S-режим. Дополнительные сведения см. в [этой записи блога](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/).

## <a name="downloading-distros"></a>Скачивание дистрибутивов

Если приложение Microsoft Store недоступно, вы можете скачать и вручную установить дистрибутивы Linux, щелкнув следующие ссылки:
<!-- * [Ubuntu 18.04](https://aka.ms/wsl-ubuntu-1804)
* [Ubuntu 18.04 ARM](https://aka.ms/wsl-ubuntu-1804-arm) -->
* Ubuntu 18.04
* Ubuntu 18.04 ARM
* [Ubuntu 16.04](https://aka.ms/wsl-ubuntu-1604)
* [Debian GNU/Linux](https://aka.ms/wsl-debian-gnulinux)
* [Kali Linux](https://aka.ms/wsl-kali-linux-new)
* [OpenSUSE Leap 42](https://aka.ms/wsl-opensuse-42)
* [SUSE Linux Enterprise Server 12](https://aka.ms/wsl-sles-12)
* [Fedora Remix for WSL](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

Это приведет к скачиванию пакетов `<distro>.appx` в выбранную папку. Следуйте [инструкциям по установке](#installing-your-distro) скачанных дистрибутивов.

## <a name="downloading-distros-via-the-command-line"></a>Скачивание дистрибутивов с помощью командной строки
При желании вы также можете скачать предпочтительные дистрибутивы с помощью командной строки.

 ### <a name="download-using-powershell"></a>Скачивание с помощью PowerShell
 Чтобы скачать дистрибутивы с помощью PowerShell, используйте командлет [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest). Ниже приведены инструкции по скачиванию Ubuntu 16.04.

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> Если загрузка занимает много времени, выключите индикатор выполнения, задав `$ProgressPreference = 'SilentlyContinue'`.

### <a name="download-using-curl"></a>Скачивание с помощью cURL
Обновление Windows 10 Spring 2018 (или более поздней версии) содержит популярную [служебную программу командной строки cURL](https://curl.haxx.se/), с помощью которой можно вызывать веб-запросы (например, команды HTTP GET, POST, PUT и т. д.) из командной строки. Вы можете использовать `curl.exe`, чтобы скачать приведенные выше дистрибутивы:

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

В приведенном выше примере выполняется `curl.exe` (а не только `curl`), чтобы убедиться, что в PowerShell вызывается реальный исполняемый файл cURL, а не его псевдоним для [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6).

> Примечание. Использование `curl` может быть предпочтительным, если необходимо вызвать или создать сценарий для скачивания с помощью командлетов командной строки и сценариев `.bat` / `.cmd`.

## <a name="installing-your-distro"></a>Установка дистрибутива
Если вы используете Windows 10, вы можете установить дистрибутив с помощью PowerShell. Просто перейдите в папку, содержащую скачанный выше дистрибутив, и в этом каталоге выполните следующую команду, в которой `app_name` — это имя APPX-файла дистрибутива.  
```Powershell
Add-AppxPackage .\app_name.appx
```

Если вы используете сервер Windows, инструкции по установке можно найти на странице документации [Windows Server](install-on-server.md).

После установки дистрибутива ознакомьтесь со страницей c [этапами инициализации](initialize-distro.md), чтобы инициализировать новый дистрибутив.
