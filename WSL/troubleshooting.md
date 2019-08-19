---
title: Устранение неполадок в подсистеме Windows для Linux
description: Подробные сведения об общих ошибках и проблемах, с которыми пользователи работают во время работы Linux в подсистеме Windows для Linux.
keywords: Башонвиндовс, bash, WSL, Windows, виндовссубсистем, Ubuntu
author: scooley
ms.author: scooley
ms.date: 11/15/2017
ms.topic: article
ms.assetid: 6753f1b2-200e-49cc-93a5-4323e1117246
ms.custom: seodec18
ms.openlocfilehash: 0c84fb710eca1b0ffabe437f98d5c17edbd6ea39
ms.sourcegitcommit: ead64b13501d6cb7170adafbb5624f4984a0af16
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/21/2019
ms.locfileid: "67307650"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a>Устранение неполадок подсистемы Windows для Linux

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a>Bash теряет сетевое подключение после подключения к VPN

Если после подключения к VPN в Windows служба Bash теряет подключение к сети, попробуйте воспользоваться этим обходным способом в bash. Это решение позволит вручную переопределить разрешение DNS с помощью `/etc/resolv.conf`.

1. Запишите DNS-сервер виртуальной частной сети.`ipconfig.exe /all`
2. Создать копию существующего resolv. conf`sudo cp /etc/resolv.conf /etc/resolv.conf.new`
3. Удалить связь с текущим resolv. Con`sudo unlink /etc/resolv.conf`
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. Откройте `/etc/resolv.conf` и <br/>
   1\. Удалите первую строку из файла, в которой говорится: «\# этот файл был автоматически создан WSL. Чтобы отключить автоматическое создание этого файла, удалите эту строку. ". <br/>
   2\. Добавьте запись DNS (1) выше в качестве первой записи в списке DNS-серверов. <br/>
   В. Закройте файл. <br/>

После отключения VPN необходимо будет отменить изменения, внесенные `/etc/resolv.conf`в. Для этого выполните следующие действия.
1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a>Запуск WSL или установка распространения возвращает код ошибки

Выполните [эти инструкции](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs) , чтобы получить подробные сведения о журналах и дать сообщение о возникшей ошибке в GitHub.

### <a name="updating-bash-on-ubuntu-on-windows"></a>Обновление Bash в Ubuntu в Windows

В системе Ubuntu в Windows есть два компонента bash, которые могут требовать обновления. 

1. Подсистема Windows для Linux
  
   При обновлении этой части bash в системе Ubuntu в Windows будут включены все новые исправления, описанные в [заметках о](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes)выпуске. Убедитесь, что вы подписаны на программу предварительной оценки Windows и что ваша сборка обновлена. Для более точного контроля детализации, включая сброс экземпляра Ubuntu, ознакомьтесь со страницей [справочника по командам](https://msdn.microsoft.com/en-us/commandline/wsl/reference).

2. Двоичные файлы пользователя Ubuntu 

   При обновлении этой части bash в системе Ubuntu в Windows будут установлены все обновления двоичных файлов пользователя Ubuntu, включая приложения, установленные с помощью apt-get. Чтобы обновить, выполните следующие команды Bash:
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a>APT-получить ошибки обновления
Некоторые пакеты используют функции, которые еще не реализованы. `udev`, например, пока не поддерживается и вызывает несколько `apt-get upgrade` ошибок.

Чтобы устранить проблемы `udev`, связанные с, выполните следующие действия.

1. Напишите следующее в `/usr/sbin/policy-rc.d` и сохраните изменения.
  
   ``` BASH
   #!/bin/sh
   exit 101
   ```
  
2. Добавить разрешения на выполнение в`/usr/sbin/policy-rc.d`
   ``` BASH
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. Выполните следующие команды.
   ``` BASH
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a>План 0x80040306 "при установке
Это необходимо сделать с тем, что не поддерживает устаревшую консоль.
Чтобы отключить устаревшую консоль, выполните следующие действия.

1. Открыть CMD. exe
1. Щелкните правой кнопкой мыши заголовок окна, > Свойства — > снять флажок использовать устаревшую консоль
1. Нажмите кнопку "ОК".

### <a name="error-0x80040154-after-windows-update"></a>План 0x80040154 "после обновления Windows
Функция подсистемы Windows для Linux может быть отключена во время обновления Windows. В этом случае компонент Windows необходимо включить заново. Инструкции по включению подсистемы Windows для Linux можно найти в разделе [руководства по установке](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui).

### <a name="changing-the-display-language"></a>Изменение языка интерфейса
WSL Install попытается автоматически изменить языковой стандарт Ubuntu в соответствии с языковым стандартом установки Windows.  Если это поведение нежелательно, можно выполнить эту команду, чтобы изменить языковой стандарт Ubuntu после завершения установки.  Чтобы это изменение вступило в силу, необходимо повторно запустить Bash. exe.

В приведенном ниже примере языковой стандарт меняется на EN-US:
``` BASH
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a>Проблемы установки после восстановления системы Windows
1.  `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux` Удалите папку. <br/>
  **Примечание. Не выполняя это действие, если дополнительный компонент полностью установлен и работает.**
2.  Включение дополнительного компонента WSL (если он еще не создан)
3.  Reboot
4.  лксрун/uninstall/Full
5.  Установка bash

### <a name="no-internet-access-in-wsl"></a>Нет доступа к Интернету в WSL
Некоторые пользователи сообщили о проблемах с определенными приложениями брандмауэра, блокирующими доступ к Интернету в WSL.  В отчет включены следующие брандмауэры:

1. Kaspersky
1. ОБРАЩЕНИЯ
1. аваст

В некоторых случаях отключение брандмауэра разрешает доступ.  В некоторых случаях просто, когда брандмауэр установлен, будет блокировать доступ.

### <a name="permission-denied-error-when-using-ping"></a>Ошибка отказа в разрешении при использовании проверки связи
#### <a name="anniversary-updatehttpsmsdnmicrosoftcomen-uscommandlinewslrelease_notesbuild-14388-to-windows-10-anniversary-update"></a>[Годовщина обновления](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14388-to-windows-10-anniversary-update) 

Для запуска проверки связи в WSL требуются права администратора в Windows.  Чтобы выполнить команду ping, запустите bash для Ubuntu в Windows в качестве администратора или запустите bash. exe из командной строки CMD/PowerShell с правами администратора.

#### <a name="build-14926httpsmsdnmicrosoftcomen-uscommandlinewslrelease_notesbuild-14926"></a>[Сборка 14926 +](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14926)
  Права администратора больше не требуются.

### <a name="bash-is-hung"></a>Bash завис
Если при работе с bash вы обнаружите, что bash зависает (или взаимозаблокирована) и не отвечает на входные данные, помогите нам диагностировать проблему путем сбора и создания отчетов о дампе памяти. Обратите внимание, что выполнение этих действий приведет к сбою системы. Не выполняя это действие, если вы не знакомы с этим, или сохраните работу перед этим.  <br/>
Чтобы получить дамп памяти, сделайте следующее:
1. Измените тип дампа памяти на "полный дамп памяти". При изменении типа дампа Запишите текущий тип.
2. Выполните [действия](https://blogs.technet.microsoft.com/askpfeplat/2015/04/05/how-to-force-a-diagnostic-memory-dump-when-a-computer-hangs/) , чтобы настроить аварийное завершение с помощью управления клавиатурой.
3. Воспроизводить зависание или взаимоблокировку.
4. Произошел сбой системы с использованием последовательности ключей из (2).
5. Произойдет сбой системы и будет собран дамп памяти.
6. После перезагрузки системы сообщите Memory. dmp к secure@microsoft.com. По умолчанию файл дампа находится в папке%Системрут%\мемори.ДМП или К:\виндовс\мемори.ДМП, если C: является системным диском. Обратите внимание, что в сообщении электронной почты дамп предназначен для WSL или Bash в группе Windows.
7. Восстановите тип дампа памяти в исходном параметре.

### <a name="check-your-build-number"></a>Проверка номера сборки

Чтобы найти архитектуру компьютера и номер сборки Windows, откройте  
**Параметры** > **системы** о > 

Найдите поля **Сборка ОС** и **тип системы** .  
    ![Снимок экрана: поля сборки и системного типа](media/system.png) 


Чтобы найти номер сборки Windows Server, выполните следующую команду в PowerShell:  
``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a>Подтверждение включения WSL
Вы можете убедиться, что подсистема Windows для Linux включена, выполнив следующую команду в PowerShell:  
``` PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a>OpenSSH — проблемы с подключением к серверу
Попытка подключения к серверу SSH завершилась следующей ошибкой: "Соединение закрыто через 127.0.0.1 порт 22".
1. Убедитесь, что сервер OpenSSH работает:
   ``` BASH
   sudo service ssh status
   ```
   и вы проверили этот учебник: https://help.ubuntu.com/lts/serverguide/openssh-server.html.en
2. Завершите работу службы sshd и запустите sshd в режиме отладки:
   ``` BASH
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```
3. Проверьте журналы запуска и убедитесь, что Хосткэйс доступны, и вы не видите сообщения журнала, например:
   ```
   debug1: sshd version OpenSSH_7.2, OpenSSL 1.0.2g  1 Mar 2016
   debug1: key_load_private: incorrect passphrase supplied to decrypt private key
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_rsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_dsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_ecdsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_ed25519_key
   ```

Если вы видите такие сообщения и в разделе `/etc/ssh/`отсутствуют ключи, потребуется повторно создать ключи или просто очистить & установить OpenSSH-Server:
```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

