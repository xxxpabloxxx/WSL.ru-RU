---
title: Обновление учетной записи пользователя WSL в предыдущих версиях Windows
description: Справочник по предыдущим версиям Windows для обновления учетных записей пользователей Linux с помощью подсистемы Windows для Linux.
ms.date: 01/20/2020
ms.topic: article
ROBOTS: NOINDEX
ms.openlocfilehash: 406158d769c4b465b6168d7cca45b48ff1f201fe
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520843"
---
# <a name="wsl-user-account-updates-on-previous-windows-versions"></a>Обновление учетной записи пользователя WSL в предыдущих версиях Windows

Это содержимое архивируется для пользователей более ранних версий операционной системы Windows, которые поддерживают подсистему для Linux и нуждаются в поддержке обновления учетных записей пользователей Linux.

Сведения о текущей документации см. в разделе [учетные записи пользователей для подсистемы Windows для Linux](../user-support.md).

### <a name="for-creators-update-version-of-windows-and-earlier"></a>Для создателя обновлений Windows и более ранних версий

Если вы используете Windows 10 Creators Update или более раннюю версию, то вы можете изменить пользователя Bash по умолчанию, выполнив следующие команды.

1. Измените пользователя по умолчанию на `root`.

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. Теперь выполните команду `bash.exe`, чтобы войти в систему как `root`.

    ```console
    C:\> bash.exe
    ```

1. Сбросьте пароль с помощью команды управления паролем для дистрибутива и закройте консоль Linux.

    ```BASH
    $ passwd username
    $ exit
    ```

1. В командной строке Windows сбросьте пользователя по умолчанию, превратив его в обычную учетную запись пользователя Linux.

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a>Для выпусков Fall Creators Update и более поздних версий

Чтобы узнать, какие команды доступны для определенного дистрибутива, выполните команду `[distro.exe] /?`.
    
Например, если установлен дистрибутив Ubuntu:

```console
C:\> ubuntu.exe /?

Launches or configures a linux distribution.

Usage:
    <no args>
      - Launches the distro's default behavior. By default, this launches your default shell.

    run <command line>
      - Run the given command line in that distro, using the default configuration.
      - Everything after `run ` is passed to the linux LaunchProcess cal

    config [setting [value]]
      - Configure certain settings for this distro.
      - Settings are any of the following (by default)
        - `--default-user <username>`: Set the default user for this distro to <username>

    clean
      - Uninstalls the distro. The appx remains on your machine. This can be
        useful for "factory resetting" your instance. This removes the linux
        filesystem from the disk, but not the app from your PC, so you don't
        need to redownload the entire tar.gz again.

    help
      - Print this usage message.
```

Пошаговые инструкции по использованию Ubuntu.

1. Открытие командной строки
1. Задайте пользователя по умолчанию Linux: `root`.

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. Запустите дистрибутив Linux (`ubuntu`).  Вы автоматически войдете в систему как `root`.

1. Сбросьте пароль с помощью команды `passwd`.

    ```BASH
    $ passwd username
    ```

1. В командной строке Windows сбросьте пользователя по умолчанию, превратив его в обычную учетную запись пользователя Linux.

    ```console
    C:\> ubuntu config --default-user username
    ```
