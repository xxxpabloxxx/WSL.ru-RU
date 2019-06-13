---
title: Установка WSL 2
description: Инструкции по установке WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, подсистема windows для linux, windowssubsystem, ubuntu, debian, suse, windows 10, установка
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 2af43a046333fc8c7b4142cdc5077cdfbf29fea7
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038084"
---
# <a name="installation-instructions-for-wsl-2"></a>Инструкции по установке для WSL 2

Для установки и начать использовать WSL 2 выполните следующие действия:

- Включить дополнительный компонент «Платформы виртуальной машины»
- Установить дистрибутив, резервному WSL 2, с помощью командной строки
- Проверка версии WSL вашей дистрибутивов, которые могут использовать

## <a name="enable-the-virtual-machine-platform-optional-component"></a>Включить дополнительный компонент «Платформы виртуальной машины»

Откройте PowerShell с правами администратора и выполните:

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

После включения этих изменений необходимо будет перезагрузить компьютер.

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>Установить дистрибутив, резервному WSL 2, с помощью командной строки

В PowerShell выполните:

`wsl --set-version <Distro> 2`

и не забудьте заменить `<Distro>` с фактическим именем вашего дистрибутива. (Их можно найти с помощью команды: `wsl -l`). Можно изменить на 1 WSL в любое время, выполнив ту же команду, как описано выше, но замена "2" с "1".

Кроме того Если вы хотите сделать WSL 2 архитектуры по умолчанию это можно сделать с помощью следующей команды:

`wsl --set-default-version 2`

Это сделает любой новый дистрибутива, который вы устанавливаете следует инициализировать как дистрибутив WSL 2.

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a>Завершение проверки версии WSL вашего дистрибутива, которые могут использовать

Чтобы проверить, какие версии дистрибутивов используется WSL используйте следующую команду:

`wsl --list --verbose` или `wsl -l -v`

Дистрибутив, который вы выбрали выше должно отображаться "2" в столбце «version». Теперь, когда вы закончите, вы можете начать использовать вашего дистрибутива WSL 2! 