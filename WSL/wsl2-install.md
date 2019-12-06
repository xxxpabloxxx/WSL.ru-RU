---
title: Установка WSL 2
description: Инструкции по установке WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, подсистема Windows для Linux, windowssubsystem, ubuntu, debian, suse, windows 10, установка
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 65c0440a95637708881c00558cba6c7985f89ec0
ms.sourcegitcommit: 522af20edfba4d4a9e429327389967a83e6d1156
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/06/2019
ms.locfileid: "74881377"
---
# <a name="installation-instructions-for-wsl-2"></a>Инструкции по установке WSL 2

Чтобы установить подсистему WSL 2 и начать с ней работу, выполните следующие действия:

> WSL 2 доступен только в сборках Windows 10 18917 или более поздней версии.

- Убедитесь, что установлен WSL (вы можете найти инструкции [здесь](./install-win10.md)) и вы используете Windows 10 **Build 18917** или более поздней версии.
   - Чтобы убедиться, что вы используете сборку 18917 или более позднюю версию, присоединитесь к [программе предварительной оценки Windows](https://insider.windows.com/en-us/) и выберите "быстрый Звонок" или "медленный" звонок. 
   - Вы можете проверить версию Windows, открыв командную строку и выполнив команду `ver`.
- Включение необязательного компонента "Virtual Machine Platform" (Платформа виртуальной машины)
- Настройка поддержки дистрибутива в WSL 2 с помощью командной строки
- проверьте, какие версии WSL используют ваши дистрибутивы.

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a>Включите дополнительный компонент "платформа виртуальной машины" и убедитесь, что WSL включен.

Необходимо убедиться в том, что установлены как подсистемы Windows для Linux, так и дополнительные компоненты платформы виртуальных машин. Это можно сделать, выполнив следующую команду в PowerShell: 

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

Перезагрузите компьютер, чтобы завершить установку обоих компонентов.


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>Настройка поддержки дистрибутива в WSL 2 с помощью командной строки

Если у вас нет дистрибутив Linux, ознакомьтесь с инструкциями по установке на странице документации по [установке на Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) . 

Чтобы задать дистрибутив, выполните команду: 

```
wsl --set-version <Distro> 2
```

Замените `<Distro>` фактическим именем дистрибутива (узнать имя можно с помощью команды `wsl -l`). Вы можете всегда вернуться к WSL версии 1, выполнив эту команду и заменив "2" на "1".

Кроме того, если вы хотите сделать WSL 2 архитектурой по умолчанию, выполните следующую команду:

```
wsl --set-default-version 2
```

Впоследствии все новые дистрибутивы после установки будут инициализированы как дистрибутивы WSL 2.

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a>Проверка используемой дистрибутивом версии WSL

Чтобы проверить, какая версия WSL используется для каждого дистрибутив, используйте следующую команду (доступно только в Windows Build 18917 или более поздней версии):

`wsl --list --verbose` или `wsl -l -v`

В дистрибутиве, который вы выбрали ранее, в столбце версии должно отображаться значение "2". Теперь все готово к работе с дистрибутивом WSL 2. 

## <a name="troubleshooting"></a>Устранение неполадок: 

Ниже перечислены возможные ошибки при установке WSL 2 и способы их устранения (дополнительные сведения см. в статье об [устранении неполадок с WSL](troubleshooting.md)):

* **Сбой установки с ошибкой 0x80070003 или ошибкой 0x80370102.**
    * Убедитесь, что в BIOS вашего компьютера включена виртуализация. Расположение этого параметра зависит от компьютера, но обычно он находится в разделе настроек ЦП в BIOS.
   
* **При попытке обновления возникает ошибка `Invalid command line option: wsl --set-version Ubuntu 2`.**
    * Убедитесь, что у вас включена подсистема Windows для Linux и используется сборка Windows 10 18917 или более поздней версии. Чтобы включить WSL, выполните эту команду в командной строке PowerShell с правами администратора: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`. Полную инструкцию по установке WSL см. [здесь](./install-win10.md).

* **Не удалось завершить запрошенную операцию из-за ограничения системы виртуальных дисков. Файлы виртуального жесткого диска должны быть несжатыми и незашифрованными и не должны быть разреженными.**
    * Проверьте [#4103 потока GitHub WSL](https://github.com/microsoft/WSL/issues/4103) , где эта проблема отслеживается для получения обновленной информации.

* **Термин "WSL" не распознан как имя командлета, функции, файла скрипта или исполняемой программы.** 
    * Убедитесь, что [установлен дополнительный компонент подсистемы Windows для Linux](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled).<br> Кроме того, если вы используете устройство Arm64 и выполняете эту команду из PowerShell, вы получите эту ошибку. Вместо этого запустите `wsl.exe` из [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6)или командной строки. 
