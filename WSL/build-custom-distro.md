---
title: Создание дистрибутив Linux, настраиваемые для WSL
description: Узнайте, как создать пользовательский дистрибутив Linux для подсистемы Windows для Linux.
keywords: BashOnWindows, bash, wsl, windows, windows подсистеме дистрибутива, пользовательский
author: taraj
ms.author: taraj
ms.date: 03/27/2018
ms.topic: article
ms.assetid: a5095219-0c82-4ce5-9a6d-5c2fc00835a3
ms.custom: seodec18
ms.openlocfilehash: b98101c19d7d450548531521c3f8ee15ce62f9f1
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063262"
---
# <a name="creating-a-custom-linux-distro-for-wsl"></a>Создание дистрибутив Linux, настраиваемые для WSL

Используйте наш пример WSL открытым исходным кодом для создания WSL дистрибутив пакетов для Microsoft Store и/или для создания пользовательских пакетов дистрибутив Linux для загрузки неопубликованных приложений. Можно найти [репозитория дистрибутивов запуска](https://github.com/Microsoft/WSL-DistroLauncher) на сайте GitHub.

Этот проект включает:
* Распространители дистрибутивов Linux для упаковки и отправки дистрибутив Linux как appx, который выполняется на WSL
* Разработчикам создавать пользовательские дистрибутивы Linux, которые могут быть заливается на своем компьютере разработки

## <a name="background"></a>Фон
Мы распространять дистрибутивов Linux для WSL как приложений универсальной платформы Windows с помощью Microsoft Store. Вы можете установить эти приложения, которые будут выполняться на WSL - подсистема, которая размещается в ядре Windows. Этот механизм доставки имеет множество преимуществ, как описано в предыдущих записи блога.

## <a name="sideloading-a-custom-linux-distro-package"></a>Для загрузки неопубликованных приложений пакета дистрибутив Linux, пользовательские
Можно создать пользовательский пакет дистрибутив Linux как приложение для загрузки неопубликованных приложений на персональных компьютеров. Обратите внимание на то, что пользовательский пакет бы не распространяется через Microsoft Store, если вы отправляете в виде распространения программы обслуживания.
Чтобы настроить компьютер для загрузки неопубликованных приложений, необходимо включить отслеживание на системные параметры в разделе «Для разработчиков».  Убедитесь, что иметь режим разработчика или выбрано загрузка неопубликованных приложений

## <a name="for-linux-distro-maintainers"></a>Для дистрибутивов Linux издатели
Чтобы отправить Store, необходимо будет работать с нами, получившей публикации. Если вы являетесь владельцем распространения Linux заинтересован в добавлении распространения в Microsoft Store, обратитесь в службу wslpartners@microsoft.com.

## <a name="getting-started"></a>начало работы
Следуйте инструкциям на [репозиторий GitHub запуска дистрибутива](https://github.com/Microsoft/WSL-DistroLauncher) для создания пользовательского пакета дистрибутива Linux.

 
## <a name="team-blogs"></a>Блоги группы разработчиков
*  [Откройте Sourcing пример WSL для дистрибутивов Linux и дистрибутивы Linux Custom для загрузки неопубликованных приложений](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
* [Блог командной строки](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a>Предоставление отзыва
* [Репозиторий дистрибутива запуска Gitub](https://github.com/Microsoft/WSL-DistroLauncher)
* [Средство отслеживания вопросов GitHub для WSL](https://github.com/Microsoft/BashOnWindows/issues)
* [Командной строки портал UserVoice](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
