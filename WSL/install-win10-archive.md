---
title: Установка подсистемы Windows для Linux (WSL) в Windows 10
description: Инструкции по установке подсистемы Windows для Linux в Windows 10.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, debian, suse, windows 10, установка
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 9cd38fbe3781fd0cd45bcd52c278de548d3da38f
ms.sourcegitcommit: 3fb40fd65b34a5eb26b213a0df6a3b2746b7a9b4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2020
ms.locfileid: "83270552"
---
# <a name="install-windows-subsystem-for-linux"></a>Установка подсистемы Windows для Linux

В этом руководстве описано, как установить подсистему Windows для Linux (WSL) на компьютере под управлением Windows 10.

## <a name="enable-the-windows-subsystem-for-linux-optional-feature"></a>Включение дополнительного компонента "Подсистема Windows для Linux"

Перед установкой дистрибутива Linux необходимо включить дополнительный компонент "Подсистема Windows для Linux" в Windows 10.

1. Запустите PowerShell от имени администратора и введите такой скрипт:

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

1. При появлении соответствующего запроса перезагрузите компьютер.

## <a name="install-a-linux-distribution"></a>Установка дистрибутива Linux

Скачать и установить предпочтительные дистрибутивы Linux можно тремя способами:

- Скачайте и установите их из Microsoft Store (см. ниже).
- [Скачайте и установите вручную с помощью командной строки.](install-manual.md)
- [Установите в Windows Server]](install-on-server.md).

### <a name="install-from-the-microsoft-store"></a>установка из Microsoft Store

Дистрибутивы Linux можно установить из Microsoft Store в Windows 10 (сборка 16215 и выше).

> [!NOTE]
> Чтобы узнать номер сборки Windows 10, выполните [эти действия](troubleshooting.md#check-your-build-number).

1. Откройте Microsoft Store и выберите предпочтительный дистрибутив Linux.

    ![Представление дистрибутивов Linux в Microsoft Store](media/store.png)

    Ниже приведены ссылки на страницы Microsoft Store для каждого дистрибутива:

    - [Ubuntu 16.04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [Ubuntu 18.04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [OpenSUSE Leap 15](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    - [OpenSUSE Leap 42](https://www.microsoft.com/store/apps/9njvjts82tjx)
    - [SUSE Linux Enterprise Server 12](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    - [SUSE Linux Enterprise Server 15](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    - [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [Fedora Remix for WSL](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [Pengwin Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [Alpine WSL](https://www.microsoft.com/store/apps/9p804crf0395)

1. Выберите "Получить". Когда скачивание дистрибутива завершится, выберите "Запустить".

    ![Представление дистрибутивов Linux в Microsoft Store](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>Завершение инициализации дистрибутива

После запуска дистрибутива Linux следуйте инструкциям на экране, чтобы инициализировать дистрибутив.

> [!NOTE]
> В Windows Server запустите дистрибутив с помощью исполняемого файла `<distro>.exe` в папке установки.

При первом запуске недавно установленного дистрибутива откроется окно консоли и вам будет предложено подождать одну или две минуты до завершения установки. На этом последнем этапе установки файлы дистрибутива будут распакованы и сохранены на компьютере, полностью готовые к использованию. Это может занять около минуты, в зависимости от производительности накопителей на компьютере. Этот начальный этап установки требуется только в том случае, если выполняется чистая установка дистрибутива. Все последующие запуски должны занимать меньше секунды.

## <a name="set-up-a-new-linux-user-account"></a>Настройка новой учетной записи пользователя Linux

После завершения установки вам будет предложено создать учетную запись пользователя (и ее пароль).

![Распаковка Ubuntu в консоли Windows](media/UbuntuInstall.png)

Эта учетная запись представляет обычного пользователя без прав администратора, который будет по умолчанию входить в систему при запуске дистрибутива. Вы можете выбрать любые имя пользователя и пароль, которые не связаны с именем пользователя Windows.

Когда вы открываете новый экземпляр дистрибутива, вам не будет предложено ввести пароль, но **если вы повысите привилегии процесса, используя `sudo`, вам нужно будет указать пароль**. Поэтому убедитесь, что вы выбрали пароль, который вы можете легко запомнить. Дополнительные сведения приведены на странице [Учетные записи пользователей и разрешения для подсистемы Windows для Linux](user-support.md).

## <a name="update--upgrade-packages"></a>Обновление пакетов

Большинство дистрибутивов поставляется с пустым или минимально наполненным каталогом пакетов. Мы настоятельно рекомендуем регулярно обновлять каталог пакетов и установленные пакеты с помощью предпочитаемого диспетчера пакетов дистрибутива. Для Debian или Ubuntu используется функция apt.

```bash
sudo apt update && sudo apt upgrade
```

Windows не выполняет автоматическую установку новых версий или обновление дистрибутивов Linux. Это задача, выполнение которой большинство пользователей Linux предпочитают контролировать самостоятельно.

Наслаждайтесь новыми дистрибутивами Linux в WSL.

## <a name="troubleshooting"></a>Диагностика

Ниже перечислены ошибки, связанные с установкой, и способы их устранения. Другие распространенные ошибки и способы их устранения приведены в разделе [Устранение неполадок подсистемы Windows для Linux](troubleshooting.md).

### <a name="installation-failed-with-error-0x8007007e"></a>Сбой установки с ошибкой 0x8007007e.

Эта ошибка возникает, когда система не поддерживает Linux из Store.  Убедитесь в следующем.

- Вы используете сборку Windows 16215 или более позднюю версию. [Проверьте используемую сборку](troubleshooting.md#check-your-build-number).
- Дополнительный компонент "Подсистема Windows для Linux" включен, а компьютер был перезагружен.  [Убедитесь, что WSL включен](troubleshooting.md#confirm-wsl-is-enabled).

### <a name="installation-failed-with-error-0x80070003"></a>Сбой установки с ошибкой 0x80070003.

Подсистема Windows для Linux работает только на системном диске (обычно это диск `C:`). Убедитесь, что дистрибутивы хранятся на системном диске.

- Выберите **Параметры** -> **Хранилище** -> **Другие параметры хранилища: изменить место сохранения нового содержимого**.
  
    ![Изображение параметров системы для установки приложений на диске C.](media/AppStorage.png)

### <a name="wslregisterdistribution-failed-with-error-0x8007019e"></a>Сбой WslRegisterDistribution с ошибкой 0x8007019e.

Дополнительный компонент "Подсистема Windows для Linux" не включен.

- Выберите **Панель управления** -> **Программы и компоненты** -> **Включение или отключение компонентов Windows** и установите флажок **Подсистема Windows для Linux** или используйте командлет PowerShell, упомянутый в начале этой статьи.
