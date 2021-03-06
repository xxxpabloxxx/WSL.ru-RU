---
title: Создание и обновление учетных записей пользователей для дистрибутивов Linux
description: Справочные материалы по управлению учетными записями пользователей и разрешениями для подсистемы Windows для Linux.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, учетные записи пользователей
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 551cc66b1648a66717163d1d8e19a78d28bff342
ms.sourcegitcommit: 3fb40fd65b34a5eb26b213a0df6a3b2746b7a9b4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2020
ms.locfileid: "83235911"
---
# <a name="create-a-user-account-and-password-for-your-new-linux-distribution"></a>Создание учетной записи пользователя и пароля для нового дистрибутива Linux

Когда вы [включите WSL и установите дистрибутив Linux из Microsoft Store](./install-win10.md), при открытии установленного дистрибутива Linux вам нужно будет сразу создать учетную запись и указать **имя пользователя** и **пароль**.

- Эти **имя пользователя** и **пароль** относятся к дистрибутиву Linux и не связаны с именем пользователя Windows.

- После создания этого **имени пользователя** и **пароля** учетная запись будет использоваться по умолчанию для этого дистрибутива, и вы сможете автоматически входить в систему при запуске.

- Эта учетная запись будет считаться администратором Linux с возможностью запуска административных команд `sudo` (команд суперпользователя).

- Каждый дистрибутив Linux, работающий в подсистеме Windows для Linux, имеет собственные учетные записи пользователей Linux с паролями.  Учетную запись пользователя Linux нужно настраивать при каждом добавлении, переустановке или сбросе дистрибутива.

![Распаковка Ubuntu в консоли Windows](media/UbuntuInstall.png)

## <a name="update-and-upgrade-packages"></a>Обновление и модификация пакетов

Большинство дистрибутивов поставляется с пустым или минимально наполненным каталогом пакетов. Мы настоятельно рекомендуем регулярно обновлять каталог пакетов и установленные пакеты с помощью предпочтительного диспетчера пакетов дистрибутива. Для Debian или Ubuntu используется функция apt.

```bash
sudo apt update && sudo apt upgrade
```

Windows не выполняет автоматическую установку обновлений или обновление дистрибутивов Linux. Это задача, выполнение которой большинство пользователей Linux предпочитают контролировать самостоятельно.

## <a name="reset-your-linux-password"></a>Сброс пароля Linux

Чтобы изменить пароль, откройте дистрибутив Linux (например, Ubuntu) и выполните команду `passwd`.

Вам будет предложено ввести текущий пароль, а затем появится запрос на ввод нового пароля, который нужно подтвердить.

## <a name="forgot-your-password"></a>Пароль утерян

Если вы забыли пароль для дистрибутива Linux, сделайте следующее.

1. Откройте PowerShell и перейдите в корень дистрибутива WSL по умолчанию с помощью команды `wsl -u root`.

    > Если вам нужно обновить забытый пароль в дистрибутиве, который не используется по умолчанию, используйте команду `wsl -d Debian -u root`, заменив `Debian` именем целевого дистрибутива.

2. Открыв дистрибутив WSL на корневом уровне в PowerShell, вы можете использовать для обновления пароля команду `passwd`.

3. Вам будет предложено ввести новый пароль UNIX, а затем подтвердить его. Когда пароль будет обновлен, закройте WSL в PowerShell, выполнив команду `exit`.

> [!NOTE]
> Если вы используете раннюю версию ОС Windows, например 1703 (Creators Update) или 1709 (Fall Creators Update), см. [архивный документ по обновлению такой учетной записи](./user-support-archived.md).
