---
title: Учетная запись пользователя Linux и разрешения
description: Справочные материалы по управлению учетными записями пользователей и разрешениями для подсистемы Windows для Linux.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, учетные записи пользователей
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: de18c128854ef9a39a26551db2ea0aee97b8ab4f
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122687"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a>Учетные записи пользователей и разрешения для подсистемы Windows для Linux

Создание пользователя Linux — это первый шаг в настройке нового дистрибутива Linux в WSL.  Для первой созданной учетной записи пользователя автоматически настраивается несколько специальных атрибутов:

1. это пользователь по умолчанию — он автоматически используется для входа при запуске;
1. по умолчанию это администратор Linux (участник группы sudo).

Каждый дистрибутив Linux, работающий в подсистеме Windows для Linux, имеет собственные учетные записи пользователей Linux с паролями.  Вам потребуется настраивать учетную запись пользователя Linux при каждом добавлении, переустановке или сбросе дистрибутива.  Учетные записи пользователей Linux не только являются независимыми для каждого дистрибутива, но и не зависят от учетной записи пользователя Windows.

## <a name="resetting-your-linux-password"></a>Сброс пароля Linux

Если у вас есть доступ к учетной записи пользователя Linux и вам известен ее пароль, измените его с помощью средств сброса пароля Linux для этого дистрибутива (как правило, это `passwd`).

Если это не так, то, в зависимости от дистрибутива, вы можете сбросить пароль, сбросив параметры пользователя по умолчанию.

WSL предлагает тег пользователя по умолчанию, который определяет, какая учетная запись пользователя автоматически входит в систему при запуске WSL.  Так как многие дистрибутивы содержат команды для задания пользователя по умолчанию в качестве привилегированного пользователя, а также привилегированного пользователя без пароля, изменение пользователя по умолчанию на привилегированного пользователя — это удобный способ сброса пароля.

### <a name="for-creators-update-and-earlier"></a>Для выпуска Creators Update и более ранних версий
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

## <a name="permissions"></a>Разрешения

При управлении разрешениями в WSL следует помнить два важных понятия.

1. Модель разрешений Windows управляет правами процесса для ресурсов Windows.
2. Модель разрешений Linux управляет правами процесса для ресурсов Linux.

При запуске Linux в WSL операционная система Linux будет иметь те же разрешения Windows, что и процесс, запускающий ее. Linux можно запустить с одним из двух уровней разрешений.

* Обычный (без повышенных привилегий): Linux работает с разрешениями вошедшего в систему пользователя.
* Повышенные привилегии или администратор: Linux работает с повышенными разрешениями Windows или правами администратора.

> Так как процессы с повышенными привилегиями могут получить доступ и изменить (а, следовательно, повредить) параметры уровня системы и данные уровня системы или защищенные данные, **не запускайте** какие-либо процессы (приложения, инструменты или оболочки Windows либо Linux) с повышенными привилегиями, если только это не связано с крайней необходимостью!

Указанные выше разрешения Windows не зависят от разрешений в экземпляре Linux. "Корневые привилегии" Linux влияют только на права пользователя в среде и файловой системе Linux. Они не влияют на предоставленные привилегии Windows. Таким образом, запуск процесса Linux в качестве корневого (например, с помощью `sudo`) предоставляет этому процессу права администратора только в среде Linux.

**Пример:**      
Сеанс Bash с привилегиями администратора Windows может обращаться к `cd /mnt/c/Users/Administrator`, в то время как сеанс Bash без привилегий администратора будет порождать ошибку "Отказ в разрешении".

Ввод `sudo cd /mnt/c/Users/Administrator` в Linux не предоставит доступ к каталогу администратора, так как разрешениями в Windows управляет Windows.

Модель разрешений Linux важна в среде Linux, в которой разрешения предоставляются в соответствии с текущим пользователем Linux.

**Пример.**  
Пользователь в группе sudo может выполнить команду `sudo apt update`.
