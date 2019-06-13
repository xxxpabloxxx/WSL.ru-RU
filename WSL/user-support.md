---
title: Учетная запись пользователя Linux и разрешения
description: Ссылка для учетных записей пользователей и управление разрешениями в подсистеме Windows для Linux.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, учетные записи пользователей
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.openlocfilehash: 0d00b43d059e72edd4e2a5b9591c29441f461fca
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040832"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a>Учетные записи пользователей и разрешения для подсистемы Windows для Linux

Создание пользователя Linux является первым шагом в настройке дистрибутив Linux на WSL.  Создаваемая учетная запись первого пользователя автоматически настраивается несколько специальных атрибутов:

1. Это ваш пользователь по умолчанию — он выполняет вход автоматически при запуске.
1. Это администратор Linux (член группы sudo) по умолчанию.

Каждый дистрибутив Linux, запущенных в подсистеме Windows для Linux имеет свои собственные учетные записи пользователей для Linux и пароли.  Необходимо настроить учетную запись пользователя Linux любое время добавить дистрибутив, переустановите или сброса.  Учетные записи пользователей Linux не только не зависят от каждого распределения, они также не зависят от учетной записи пользователя Windows.

## <a name="resetting-your-linux-password"></a>Сброс пароля Linux

Если нет доступа к вашей учетной записью пользователя Linux и знать текущий пароль, измените его с помощью Linux сброса пароля средства дистрибутива — скорее всего, `passwd`.

Если это не параметр, в зависимости от распределения, можно сбросить пароль, сбросив пользователя по умолчанию.

WSL предлагает входе тег пользователя по умолчанию, чтобы определить какая пользовательская учетная запись автоматически при запуске WSL.  Так как многие дистрибутивы включают в себя команды, чтобы задать пользователя по умолчанию для корня и также привилегированного пользователя с набором без пароля, изменение пользователя по умолчанию корневой каталог является удобным инструментом для таких вещей, как сброс пароля.

### <a name="for-creators-update-and-earlier"></a>Для Creators Update и более ранних версий
Если вы используете Windows 10 Creators update или более ранних версиях Bash пользователя по умолчанию можно изменить, выполнив следующие команды:

1. Изменить пользователя по умолчанию для `root`:

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. Запустите `bash.exe` теперь войти как `root`:

    ```console
    C:\> bash.exe
    ```

1. Сбросить пароль с помощью дистрибутива парольная команда и закройте консоль Linux:

    ```BASH
    $ passwd username
    $ exit
    ```

1. Из командной строки Windows сбросьте пользователя по умолчанию в учетной записи обычного пользователя Linux:

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a>Fall Creators Update и более поздних версий
Чтобы узнать, какие команды доступны для определенного распределения, запустите `[distro.exe] /?`.
    
Например с Ubuntu установлены:

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

Пошаговые инструкции с помощью Ubuntu:

1. Откройте CMD
1. Значение по умолчанию пользователь Linux `root`:

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. Запустите дистрибутива Linux (`ubuntu`).  Вы будете автоматически войдите в систему как `root`:

1. Сбросить пароль с помощью `passwd` команды:

    ```BASH
    $ passwd username
    ```

1. Из командной строки Windows сбросьте пользователя по умолчанию в учетной записи обычного пользователя Linux.

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a>Разрешения

Существует два важных понятий Имейте в виду, когда дело доходит до разрешения в WSL:

1. Модель разрешений Windows управляет процесса права к ресурсам Windows
2. Модель разрешений Linux управляет правами процесса для ресурсов под управлением Linux

При использовании Linux на платформе WSL, Linux будет иметь те же разрешения Windows, что и запустившая его процесс. Linux могут запускаться в одном из двух уровней разрешений:

* Обычный (без повышенных прав): Linux выполняется с разрешениями пользователя, вошедшего в систему
* Повышенных привилегий/admin: Linux выполняется с повышенным уровнем разрешений администратору Windows

> Так как процессов с повышенными правами можно доступ и изменение (и поэтому повредить) параметры уровня системы и системы расширенных/защищенные данные, **ИЗБЕГАЙТЕ** запуск процессов с повышенными правами, если совершенно необходимо - находятся ли они Windows или Linux приложения/tools/оболочек!

Эти разрешения Windows не зависят от разрешений в экземпляре Linux: «Привилегированного Linux» затрагивается только права пользователя в среде Linux & файловой системы; они не оказывают влияния на привилегиях Windows. Таким образом, выполнение процесса Linux в качестве привилегированного пользователя (например, через `sudo`) предоставляет только разрешение, которые обрабатывают права администратора в среде Linux.

**Пример:**     
Сеанс Bash с правами администратора Windows могут получить доступ к `cd /mnt/c/Users/Administrator` во время сеанса Bash без прав администратора увидит сообщение об ошибке «Отказано в доступе».

В Linux введя `sudo cd /mnt/c/Users/Administrator` не предоставит доступ к каталогу администратора, так как Windows управляет разрешения в Windows.

Модель разрешений Linux важно при работе в среде Linux, в которых пользователь имеет разрешения на основе текущего пользователя Linux.

**Пример:**  
Пользователь в группу sudo может запустить `sudo apt update`.
