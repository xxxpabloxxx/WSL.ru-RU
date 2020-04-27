---
title: Установка WSL 2
description: Инструкции по установке WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, подсистема Windows для Linux, windowssubsystem, ubuntu, debian, suse, windows 10, установка
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 7c031b1348a77e1dac967fae5e4df772e10a9084
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/24/2020
ms.locfileid: "80256347"
---
# <a name="installation-instructions-for-wsl-2"></a>Инструкции по установке WSL 2

Просмотрите приведенное ниже видео или изучите эту статью, чтобы узнать, как установить WSL 2. 

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Learn-how-to-install-WSL-2/player]

Чтобы установить подсистему WSL 2 и начать с ней работу, выполните следующие действия:

> Подсистема WSL 2 доступна только в Windows 10 сборки 18917 или выше.

- Убедитесь, что установлено WSL (инструкции по установке см. [здесь](./install-win10.md)) и что вы используете Windows 10 **сборки 18917** или выше.
   - Чтобы убедиться, что вы используете сборку 18917 или выше, присоединитесь к [программе предварительной оценки Windows](https://insider.windows.com/en-us/) и выберите круг раннего или позднего доступа. 
   - Вы можете проверить версию Windows, открыв командную строку и выполнив команду `ver`.
- Включение необязательного компонента "Virtual Machine Platform" (Платформа виртуальной машины)
- с помощью командной строки задайте поддержку дистрибутива в WSL 2;
- проверьте, какие версии WSL используют ваши дистрибутивы.

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a>Включение дополнительного компонента Virtual Machine Platform (Платформа виртуальной машины) и подтверждение включения WSL

Убедиться, что установлены дополнительные компоненты подсистемы Windows для Linux и Virtual Machine Platform (Платформа виртуальной машины). Это можно сделать, выполнив следующую команду в PowerShell: 

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

Перезагрузите компьютер, чтобы завершить установку обоих компонентов.


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>Настройка поддержки дистрибутива в WSL 2 с помощью командной строки

Если у вас не установлен дистрибутив Linux, ознакомьтесь с инструкциями по установке Windows 10 на [этой странице](./install-win10.md#install-your-linux-distribution-of-choice). 

Чтобы задать дистрибутив, выполните следующую команду: 

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

Чтобы проверить, какие версии WSL использует каждый дистрибутив, выполните приведенную ниже команду (доступную только в Windows сборки 18917 или более поздней версии):

`wsl --list --verbose` или `wsl -l -v`

В дистрибутиве, который вы выбрали ранее, в столбце версии должно отображаться значение "2". Теперь все готово к работе с дистрибутивом WSL 2. 

## <a name="troubleshooting"></a>Устранение неполадок: 

Ниже перечислены возможные ошибки при установке WSL 2 и способы их устранения (дополнительные сведения см. в статье об [устранении неполадок с WSL](troubleshooting.md)):

* **Сбой установки с ошибкой 0x80070003 или ошибкой 0x80370102.**
    * Убедитесь, что в BIOS вашего компьютера включена виртуализация. Расположение этого параметра зависит от компьютера, но обычно он находится в разделе настроек ЦП в BIOS.
   
* **При попытке обновления возникает ошибка `Invalid command line option: wsl --set-version Ubuntu 2`.**
    * Убедитесь, что у вас включена подсистема Windows для Linux и используется сборка Windows 10 18917 или более поздней версии. Чтобы включить WSL, выполните эту команду в командной строке PowerShell с правами администратора: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`. Полную инструкцию по установке WSL см. [здесь](./install-win10.md).

* **Запрошенную операцию не удалось выполнить из-за ограничения системы виртуального диска. Файлы виртуального жесткого диска должны быть распакованными, незашифрованными и не разреженными.**
    * Чтобы получить обновленные сведения, проверьте [поток GitHub WSL #4103](https://github.com/microsoft/WSL/issues/4103), где отслеживается эта проблема.

* **Термин WSL не распознан как имя командлета, функции, файла скрипта или действующей программы.** 
    * Убедитесь, что установлен дополнительный компонент [Подсистема Windows для Linux](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled).<br> Кроме того, если вы используете устройство Arm64 и выполняете эту команду в PowerShell, вы получите эту ошибку. Вместо этого запустите `wsl.exe` из [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6) или командной строки. 
