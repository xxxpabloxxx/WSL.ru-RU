---
title: Установка WSL 2
description: Инструкции по установке WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, подсистема Windows для Linux, windowssubsystem, ubuntu, debian, suse, windows 10, установка
author: craigloewen-msft
ms.author: crloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 4ae5b8452ae2aec679c2f0450dc48644b77fc1c9
ms.sourcegitcommit: ed5cf72d5ceb92edd50cf9260ac31fd4d95a02c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "71020940"
---
# <a name="installation-instructions-for-wsl-2"></a>Инструкции по установке WSL 2

Чтобы установить подсистему WSL 2 и начать с ней работу, выполните следующие действия:

- Убедитесь, что установлен WSL (вы можете найти инструкции [здесь](./install-win10.md)) и вы используете Windows 10 Build 18917 или более поздней версии.
   - Чтобы убедиться, что вы используете сборку 18917 или более позднюю версию, присоединитесь к [программе предварительной оценки Windows](https://insider.windows.com/en-us/) и выберите Быстрый звонок. 
   - Вы можете проверить версию Windows, открыв командную строку и выполнив `ver` команду.
- Включение необязательного компонента "Virtual Machine Platform" (Платформа виртуальной машины)
- с помощью командной строки задайте поддержку дистрибутива в WSL 2;
- проверьте, какие версии WSL используют ваши дистрибутивы.

## <a name="enable-the-virtual-machine-platform-optional-component"></a>Включение необязательного компонента "Virtual Machine Platform" (Платформа виртуальной машины)

Запустите PowerShell с правами администратора и выполните такую команду:

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

Когда вы внесете эти изменения, нужно будет перезагрузить компьютер.

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>Настройка поддержки дистрибутива в WSL 2 с помощью командной строки

В PowerShell выполните такую команду:

`wsl --set-version <Distro> 2`

Замените `<Distro>` фактическим именем дистрибутива (узнать имя можно с помощью команды `wsl -l`). Вы можете всегда вернуться к WSL версии 1, выполнив эту команду и заменив "2" на "1".

Кроме того, если вы хотите сделать WSL 2 архитектурой по умолчанию, выполните следующую команду:

`wsl --set-default-version 2`

Впоследствии все новые дистрибутивы после установки будут инициализированы как дистрибутивы WSL 2.

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a>Проверка используемой дистрибутивом версии WSL

Чтобы проверить, какие версии WSL использует каждый дистрибутив, выполните такую команду:

`wsl --list --verbose` или `wsl -l -v`

В дистрибутиве, который вы выбрали ранее, в столбце версии должно отображаться значение "2". Теперь все готово к работе с дистрибутивом WSL 2. 

## <a name="troubleshooting"></a>Устранение неполадок: 

Ниже перечислены возможные ошибки при установке WSL 2 и способы их устранения (дополнительные сведения см. в статье об [устранении неполадок с WSL](troubleshooting.md)):

* **Сбой установки с ошибкой 0x80070003 или ошибкой 0x80370102.**
    * Убедитесь, что в BIOS вашего компьютера включена виртуализация. Расположение этого параметра зависит от компьютера, но обычно он находится в разделе настроек ЦП в BIOS.
   
* **При попытке обновления возникает ошибка `Invalid command line option: wsl --set-version Ubuntu 2`.**
    * Убедитесь, что у вас включена подсистема Windows для Linux и используется сборка Windows 10 18917 или более поздней версии. Чтобы включить WSL, выполните эту команду в командной строке PowerShell с правами администратора: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`. Полную инструкцию по установке WSL см. [здесь](./install-win10.md).