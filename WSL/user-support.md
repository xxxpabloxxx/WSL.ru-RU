---
title: Учетная запись пользователя и разрешения Linux
description: Справочник по учетным записям пользователей и управлению разрешениями с помощью подсистемы Windows для Linux.
keywords: Башонвиндовс, bash, WSL, Windows, подсистема Windows для Linux, виндовссубсистем, Ubuntu, учетные записи пользователей
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.openlocfilehash: 0d00b43d059e72edd4e2a5b9591c29441f461fca
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/14/2019
ms.locfileid: "67040832"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a>Учетные записи пользователей и разрешения для подсистемы Windows для Linux

Создание пользователя Linux — это первый шаг в настройке нового дистрибутива Linux в WSL.  Первая созданная учетная запись пользователя автоматически настраивается с помощью нескольких специальных атрибутов:

1. Это пользователь по умолчанию — он автоматически подписывается при запуске.
1. По умолчанию это администратор Linux (член группы sudo).

Каждый дистрибутив Linux, работающий в подсистеме Windows для Linux, имеет собственные учетные записи пользователей и пароли Linux.  Вам потребуется настроить учетную запись пользователя Linux при каждом добавлении, переустановке или сбросе.  Учетные записи пользователей Linux не только независимы для каждого распределения, но и не зависят от учетной записи пользователя Windows.

## <a name="resetting-your-linux-password"></a>Сброс пароля Linux

Если у вас есть доступ к учетной записи пользователя Linux и ваш текущий пароль, измените его с помощью средств сброса паролей Linux этого распространения, скорее всего `passwd`,.

Если это не так, то в зависимости от распространения вы можете сбросить пароль, переустановив пользователя по умолчанию.

WSL предлагает тег пользователя по умолчанию, который определяет, какая учетная запись пользователя автоматически входит в систему при запуске WSL.  Так как многие дистрибутивы включают команды для задания корневого пользователя по умолчанию, а также привилегированного пользователя без пароля, изменение пользователя по умолчанию на root — это удобное средство для сброса пароля.

### <a name="for-creators-update-and-earlier"></a>Для авторов, обновление и более ранние версии
Если вы используете Windows 10 Creators Update или более раннюю версию, вы можете изменить пользователя bash по умолчанию, выполнив следующие команды:

1. Измените пользователя по умолчанию `root`на:

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. Выполните `bash.exe` команду, чтобы войти `root`в систему как:

    ```console
    C:\> bash.exe
    ```

1. Сбросьте пароль с помощью команды для распространения пароля и закройте консоль Linux:

    ```BASH
    $ passwd username
    $ exit
    ```

1. В Windows CMD верните пользователя по умолчанию в обычную учетную запись пользователя Linux:

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a>Для создателей попадают обновление и более поздние версии
Чтобы узнать, какие команды доступны для определенного распределения, выполните команду `[distro.exe] /?`.
    
Например, при установке Ubuntu:

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

Пошаговые инструкции по использованию Ubuntu:

1. Открыть CMD
1. Задайте для `root`пользователя Linux по умолчанию следующее:

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. Запустите дистрибутив Linux (`ubuntu`).  Вы будете автоматически входить в `root`систему как:

1. Сбросьте пароль с помощью `passwd` команды:

    ```BASH
    $ passwd username
    ```

1. В Windows CMD верните пользователя по умолчанию в обычную учетную запись пользователя Linux.

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a>Разрешения

Есть два важных понятия, которые следует помнить при получении разрешений в WSL:

1. Модель разрешений Windows управляет правами процесса для ресурсов Windows
2. Модель разрешений Linux управляет правами процесса для ресурсов Linux

При запуске Linux на WSL Linux будет иметь те же разрешения Windows, что и процесс, запускающий ее. Linux можно запустить на одном из двух уровней разрешений:

* Обычная (без повышенных привилегий): Linux работает с разрешениями вошедшего в систему пользователя
* Повышенная привилегия или администратор: Linux работает с разрешениями Windows с повышенными правами или администратором

> Так как процессы с повышенными правами могут получать доступ к (и, таким образом, повредить) параметры на уровне системы и данные, защищенные системой или на уровне системы, **не** запускайте процессы с повышенными правами, если только вы не хотите, чтобы они были приложениями Windows или Linux или средствами или команд!

Указанные выше разрешения Windows не зависят от разрешений в экземпляре Linux. Linux "root Privileges" влияет только на права пользователя в среде Linux & файловой системе. они не влияют на предоставленные привилегии Windows. Таким образом, запуск процесса Linux в качестве корневого (например `sudo`, Via) предоставляет только права администратора процесса в среде Linux.

**Пример:**      
Сеанс bash с привилегиями администратора Windows может получить `cd /mnt/c/Users/Administrator` доступ, в то время как сеанс Bash без прав администратора будет видеть ошибку "отказано в разрешении".

В Linux ввод `sudo cd /mnt/c/Users/Administrator` не будет предоставлять доступ к каталогу администратора, так как разрешения в Windows управляются Windows.

Модель разрешений Linux важна в среде Linux, в которой пользователь имеет разрешения на основе текущего пользователя Linux.

**Например**  
Может выполняться `sudo apt update`пользователь в группе sudo.
