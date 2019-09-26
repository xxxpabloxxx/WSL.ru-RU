---
title: Ручная загрузка подсистемы Windows для Linux (WSL) дистрибутивов
description: Инструкции по загрузке подсистемы Windows для дистрибутивов Linux вручную.
keywords: Башонвиндовс, bash, WSL, Windows, подсистема Windows для Linux, WSL, подсистема Windows, дистрибутив, Ubuntu, openSUSE, SLES, Debian, Kali
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: df47e656cf83e0b13aa8eb3f210e010d6a85bfd8
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269792"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a>Ручная загрузка подсистемы Windows для пакетов дистрибутив для Linux

Существует несколько сценариев, в которых может быть недоступно (или требуется) Установка WSL Linux дистрибутивов с помощью Microsoft Store. В частности, вы можете использовать номер SKU ОС Windows Server или долгосрочного обслуживания (LTSC), который не поддерживает Microsoft Store, или политики корпоративной сети и (или) администраторы, чтобы не допускать использование Microsoft Store в вашей среде.

В таких случаях, когда доступ к магазину WSL, как скачать и установить Linux дистрибутивов в WSL?

> Примечание. **Среды оболочки командной строки, в том числе cmd, PowerShell и Linux/WSL дистрибутивов, не могут выполняться в режиме Windows 10 S**. Это ограничение существует, чтобы обеспечить целостность и безопасность, которые предоставляет режим S: Дополнительные сведения см. в [этой записи](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) .

## <a name="downloading-distros"></a>Скачивание дистрибутивов

Если Microsoft Store приложение недоступно, вы можете скачать и вручную установить дистрибутивов Linux, щелкнув следующие ссылки:
* [Ubuntu 18,04](https://aka.ms/wsl-ubuntu-1804)
* [Ubuntu 18,04 ARM](https://aka.ms/wsl-ubuntu-1804-arm)
* [Ubuntu 16,04](https://aka.ms/wsl-ubuntu-1604)
* [Debian GNU/Linux](https://aka.ms/wsl-debian-gnulinux)
* [Kali Linux](https://aka.ms/wsl-kali-linux-new)
* [OpenSUSE LEAP 42](https://aka.ms/wsl-opensuse-42)
* [SUSE Linux Enterprise Server 12](https://aka.ms/wsl-sles-12)
* [Fedora Remix для WSL](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

Это приведет `<distro>.appx` к скачиванию пакетов в выбранную папку. Следуйте [инструкциям по установке](#installing-your-distro) , чтобы установить Скачанные дистрибутив.

## <a name="downloading-distros-via-the-command-line"></a>Скачивание дистрибутивов с помощью командной строки
При желании вы также можете скачать предпочтительные дистрибутив с помощью командной строки:

 ### <a name="download-using-powershell"></a>Скачать с помощью PowerShell
 Чтобы скачать дистрибутивов с помощью PowerShell, используйте командлет [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) . Ниже приведен пример инструкции по скачиванию Ubuntu 16,04.

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> Если загрузка занимает много времени, отключите индикатор выполнения, задав`$ProgressPreference = 'SilentlyContinue'`

### <a name="download-using-curl"></a>Скачать с помощью функции "перелистывание"
Обновление Windows 10 пружины 2018 (или более поздней версии) включает в себя популярную [программу командной строки](https://curl.haxx.se/) , с помощью которой можно вызывать веб-запросы (например, команды HTTP GET, POST, WHERE и т. д.) из командной строки. Можно использовать `curl.exe` для загрузки указанного выше дистрибутивов:

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

В приведенном выше примере `curl.exe` выполняется (не только `curl`), чтобы убедиться в том, что в PowerShell вызывается фактический исполняемый файл, а не псевдоним оболочки PowerShell для [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6) .

> Примечание. Использование `curl` может быть предпочтительным, если необходимо вызвать или создать скрипт для загрузки с помощью оболочки `.bat`  /  `.cmd` cmd или сценариев.

## <a name="installing-your-distro"></a>Установка дистрибутив
Если вы используете Windows 10, вы можете установить дистрибутив с помощью PowerShell. Просто перейдите в папку, содержащую дистрибутив, скачанный выше, и в этом каталоге выполните следующую команду, `app_name` где — это имя файла дистрибутив. appx.  
```Powershell
Add-AppxPackage .\app_name.appx
```

Если вы используете Windows Server, инструкции по установке можно найти на странице документации по [Windows Server](install-on-server.md) .

После установки дистрибутив ознакомьтесь со страницей [действия интилизатион](initialize-distro.md) , чтобы инициализировать новый дистрибутив.
