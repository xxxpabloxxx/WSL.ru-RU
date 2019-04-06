---
title: Подсистема Windows для ссылки на команды Linux
description: Список команд, которые управляют подсистема Windows для Linux
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.openlocfilehash: 978a35d593e37877949c24cbd833a519888d54bf
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063582"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a>Справочник по командам подсистемы Windows для Linux

> `lxrun.exe` — не рекомендуется, начиная с Windows 10 версии 1803 и более поздних версий.

Команда `lxrun.exe` может использоваться для взаимодействия с [подсистемы Windows для Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) напрямую.  Эти команды устанавливаются в `\Windows\System32` каталога и может быть запущена из командной строки Windows или в PowerShell.

* `lxrun.exe` используется для управления WSL.  Эту команду можно использовать для установки или удаления образа Ubuntu.


| Command                     | Описание                     |
|:----------------------------|:---------------------------|
| `bash`                      | Запускает оболочку Bash, в текущем каталоге.  Если оболочка Bash не устанавливается автоматически выполняется `lxrun /install` |
| `bash ~`                    | Запускает оболочку bash в домашнем каталоге пользователя Ubuntu.  Аналогично выполнению компакт-диска ~            |
| `bash -c "<command>"`       | Выполняет команду, выводит выходные данные и завершает работу обратно в командной строке Windows. <br/> <br/> Пример: **bash -c «ls»** |

<p>

| Command                     | Описание                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | Команда lxrun используется для управления экземпляром WSL. |
| `lxrun /install`            | Начнется загрузка и процесс установки. <br/> **/y** может быть добавлена к обойти все запросы.  Запрос на подтверждение принимаются автоматически и пользователь по умолчанию имеет значение root.          |
| `lxrun /uninstall`          | Удаляет и удаляет образ Ubuntu.  По умолчанию не будет удален домашний каталог пользователя Ubuntu. <br/> **/y** может добавляться автоматически принимать запрос на подтверждение <br/>**/ full** удаляет и удаляет домашний каталог пользователя Ubuntu         |
| `lxrun /setdefaultuser <userName>`     | Устанавливает по умолчанию Bash на Ubuntu пользователя. Предложит ввести пароль, если указанный пользователь не существует.  Дополнительные сведения см. в статье: https://aka.ms/wslusers. <br/> **/y** promping обходит пароля.  Пользователь будет создаваться без пароля.|
| `lxrun /update`            | Обновляет индекс пакета подсистемы          |
