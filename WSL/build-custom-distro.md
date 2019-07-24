---
title: Создание пользовательской дистрибутив Linux для WSL
description: Узнайте, как создать настраиваемый дистрибутив Linux для подсистемы Windows для Linux.
keywords: Башонвиндовс, bash, WSL, Windows, подсистема Windows, дистрибутив, настраиваемый
author: taraj
ms.author: taraj
ms.date: 03/27/2018
ms.topic: article
ms.assetid: a5095219-0c82-4ce5-9a6d-5c2fc00835a3
ms.custom: seodec18
ms.openlocfilehash: 4072df5fa81f65fd9a3ff875ab887c03b234bce1
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/14/2019
ms.locfileid: "67040773"
---
# <a name="creating-a-custom-linux-distro-for-wsl"></a>Создание пользовательской дистрибутив Linux для WSL

Используйте наш пример WSL с открытым исходным кодом для создания пакетов WSL дистрибутив для Microsoft Store и (или) для создания пользовательских пакетов Linux дистрибутив для загрузки неопубликованных приложений. [Репозиторий запуска дистрибутив](https://github.com/Microsoft/WSL-DistroLauncher) можно найти на сайте GitHub.

Этот проект включает:
* Служба поддержки распространения Linux для упаковки и отправки дистрибутива Linux в качестве appx-пакета, работающего на WSL
* Разработчики могут создавать настраиваемые дистрибутивы Linux, которые можно загруженные неопубликованные на свой компьютер разработки.

## <a name="background"></a>Фон
Мы распространяем дистрибутивов Linux для WSL как приложения UWP с помощью Microsoft Store. Можно установить приложения, которые будут запускаться на WSL — подсистему, расположенной в ядре Windows. Этот механизм доставки имеет много преимуществ, как описано в [предыдущей записи блога](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/).

## <a name="sideloading-a-custom-linux-distro-package"></a>Неопубликованная загрузка пользовательского пакета дистрибутив для Linux
Вы можете создать пользовательский пакет дистрибутив для Linux в качестве приложения для загружать неопубликованные на личном компьютере. Обратите внимание, что пользовательский пакет не будет распространяться с помощью Microsoft Store, пока не будет отправлен в качестве обслуживания распространения.
Чтобы настроить компьютер для загружать неопубликованные приложений, его необходимо включить в параметрах системы в разделе "для разработчиков".  Убедитесь, что выбран режим разработчика или загружать неопубликованные приложения.

## <a name="for-linux-distro-maintainers"></a>Для дистрибутив обслуживания Linux
Для отправки в магазин необходимо работать с нами, чтобы получить утверждение публикации. Если вы являетесь владельцем дистрибутива Linux, который заинтересован в добавлении дистрибутива в Microsoft Store, обратитесь wslpartners@microsoft.comпо адресу.

## <a name="getting-started"></a>Начало работы
Следуйте инструкциям в репозитории [GitHub дистрибутив Launcher](https://github.com/Microsoft/WSL-DistroLauncher) , чтобы создать пользовательский пакет дистрибутив для Linux.

 
## <a name="team-blogs"></a>Блоги группы
*  [Открытие источника. пример WSL для обслуживания распространения Linux и пользовательских дистрибутивов Linux для загрузки неопубликованных приложений](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
* [Блог командной строки](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a>Предоставление отзыва
* [Репозиторий GitHub дистрибутив Launcher](https://github.com/Microsoft/WSL-DistroLauncher)
* [Средство регистрации проблем GitHub для WSL](https://github.com/Microsoft/BashOnWindows/issues)
* [Портал UserVoice для командной строки](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
