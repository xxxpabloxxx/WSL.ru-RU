---
title: Установить или удалить на Юбилейное обновление Windows 10 или Creators Update
description: Инструкции по установке и отмены установки для прежних версий, а также бета-версии дистрибутива на Юбилейное обновление Windows 10 или Creators Update
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, debian, suse, windows 10, прежних версий, бета-версия, установки, удаления, удаление, удалить, удаление, устаревшие
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: fbb5bdc401a013b0853774cff6ad2dc84a36e412
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040836"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a>Руководство по установке или удалении подсистемы Windows для Linux в юбилейном обновлении Windows 10 и Creators Update 

Если вы используете Windows 10 Creators Update или более поздней версии, можно [следуйте инструкциям по установке Windows 10](install-win10.md).

<strong><em><span style="color: #f28014">Ниже приведены инструкции для пользователей, выполняющих Юбилейное обновление Windows 10 или Windows 10 Creators Update</span></em></strong>

До Windows 10 Fall Creators Update (версия 1709) WSL была выпущена в виде бета-функции и установить один экземпляр Ubuntu, при первом запуске «Bash на Ubuntu в Windows» (или Bash.exe).

> Хотя вы МОЖЕТЕ использовать WSL в более ранних выпусках Windows 10, бета-версии «прежних версий дистрибутива» считается устаревшим. Настоятельно рекомендуется для выполнения самой последней версии Windows 10 доступна. Каждым новым выпуском Windows 10 включает многие сотни исправления и улучшения в WSL только, когда-либо дополнительные средства Linux и приложений для корректной работы в WSL.

Если не удается обновить Fall Creators Update или более поздней версии, выполните следующие действия, чтобы включить и использовать WSL.

1. Включение разработчиков режиме для запуска WSL на Юбилейное обновление Windows 10 Creators Update, то необходимо включить режим разработчика:

    Откройте **параметры** -> **обновление и безопасность** -> **для разработчиков**

    Установите переключатель в режим разработчика.  
    ![Включение режима разработчика](media/updateAndSecurity.png)

    > Требование, чтобы включить режим разработчика была [удален в Windows 10 Fall Creators Update](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)

1. Откройте командную строку.  Тип `bash` и нажмите клавишу ВВОД

    Первый раз выполнять Bash на Ubuntu в Windows, вам будет предложено принять условия лицензионного соглашения Canonical. После принятия WSL загрузит и установит экземпляре Ubuntu на вашем компьютере, и в меню "Пуск" будет добавлен ярлык «Bash на Ubuntu в Windows».

    ![Запрос на установку Ubuntu](media/bashShellInstall.png)

    При первом выполнении Bash на Ubuntu в Windows, будет предложено создать UNIX имя пользователя и пароль. Выполните [инструкции по созданию экземпляра дистрибутива](initialize-distro.md) для завершения установки

1. Для запуска новой оболочки Ubuntu либо:
    * Под управлением `bash` из командной строки
    * Щелкнув главное меню «Bash на Ubuntu в Windows»

    
## <a name="uninstallingremoving-the-legacy-distro"></a>При удалении/удаление предыдущих версий дистрибутива
При обновлении до Windows 10 Fall Creators Update более ранней версии Windows 10, на котором установлен WSL, ваши существующие дистрибутива останется без изменений. Тем не менее мы настоятельно рекомендуем вам установить дистрибутив новые доставляемые Store кратчайшие СРОКИ и перенести все необходимые файлы, данные, и т.д. из вашего дистрибутива прежних версий для вашего нового дистрибутива.

Чтобы удалить устаревшие дистрибутива с компьютера, выполните следующую команду из командной строки или PowerShell экземпляр:

```console
lxrun /uninstall /full
```

### <a name="manually-deleting-the-legacy-distro"></a>Удаление устаревших дистрибутива вручную
При желании можно вручную удалить устаревший экземпляр. Это может потребоваться при возникновении проблем, при удалении устаревших дистрибутив с помощью `lxrun.exe`, или работает под управлением Windows 10 весна 2018 с обновлением (или более поздней версии) которого не поставляются с `lxrun.exe`.

Чтобы принудительно удалить вашего прежних версий дистрибутива WSL, удалите `%localappdata%\lxss\` папки (и всех его в содержимое вложенного) с помощью проводника Windows, или из командной строки:

Использование PowerShell
```powershell
rm -Recurse $env:localappdata/lxss/
```

С использованием командной строки:
```console
DEL /S %localappdata%\lxss\
```
