---
title: Устранение неполадок Windows Susbystem для Linux
description: Предоставляет подробные сведения о распространенных ошибок и людей, возникли проблемы при использовании Linux на платформе Windows Susbystem для Linux.
keywords: BashOnWindows, bash, wsl, Microsoft windows, windowssubsystem ubuntu
author: scooley
ms.author: scooley
ms.date: 11/15/2017
ms.topic: article
ms.assetid: 6753f1b2-200e-49cc-93a5-4323e1117246
ms.custom: seodec18
ms.openlocfilehash: 055bdc02dcf8f078caa014abd6dd755a47c99cfe
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063302"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a>Устранение неполадок подсистемы Windows для Linux

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a>Bash теряет сетевое подключение, подключитесь к виртуальной частной сети

Если после подключения к виртуальной частной сети в Windows, bash теряет сетевое подключение, попробуйте следующее из в bash. Это решение позволит вам вручную переопределить разрешения DNS происходит через `/etc/resolv.conf`.

1. Запишите DNS-сервер VPN от выполнения `ipconfig.exe /all`
2. Создайте копию существующего resolv.conf `sudo cp /etc/resolv.conf /etc/resolv.conf.new`
3. Удалить связь с текущей resolv.con `sudo unlink /etc/resolv.conf`
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. Откройте `/etc/resolv.conf` и <br/>
   1. Удалите первую строку из файла, который говорит: «\# этот файл был автоматически создан с WSL. Чтобы остановить автоматическое создание этого файла, удалите эту строку.». <br/>
   2. Добавьте запись DNS из (1) выше в качестве самой первой записи в список DNS-серверов. <br/>
   В. Закройте файл. <br/>

После отключения виртуальной частной сети, необходимо отменить изменения, внесенные `/etc/resolv.conf`. Чтобы сделать это, выполните следующую команду:
1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a>Запуск WSL или установке дистрибутив возвращает код ошибки

Выполните [эти инструкции](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs) собирать подробные журналы и сообщите о проблеме на GitHub.

### <a name="updating-bash-on-ubuntu-on-windows"></a>Обновление Bash на Ubuntu в Windows

Есть два компонента из Bash на Ubuntu в Windows, может потребоваться обновление. 

1. Подсистема Windows для Linux
  
   Обновление этой части Bash на Ubuntu в Windows включит все новые исправления контурами [заметки о выпуске](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes). Убедитесь, что вы будете подписаны на программе предварительной оценки Windows и в актуальном состоянии построения. Для более точного управления детализации, включая сброс вашей Ubuntu экземпляра извлечение [команды справочной странице](https://msdn.microsoft.com/en-us/commandline/wsl/reference).

2. Двоичные файлы пользователя Ubuntu 

   Обновление этой части Bash на Ubuntu в Windows установите все обновления, в том числе приложений, установленных с помощью apt-get двоичные файлы пользователя Ubuntu. Для обновления выполнить следующие команды в Bash:
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a>Ошибки обновления apt-get
Некоторые пакеты используют функции, которые мы еще не реализована. `udev`, например, сейчас не поддерживается и приводит несколько `apt-get upgrade` ошибки.

Чтобы устранить проблемы, связанные с `udev`, выполните следующие действия:

1. Написать следующую команду, чтобы `/usr/sbin/policy-rc.d` и сохраните изменения.
  
   ``` BASH
   #!/bin/sh
   exit 101
   ```
  
2. Добавить разрешения на выполнение `/usr/sbin/policy-rc.d`
   ``` BASH
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. Выполните следующие команды
   ``` BASH
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a>«Ошибка: 0x80040306» при установке
Это связано с тем, что мы не поддерживаем прежнюю версию консоли.
Чтобы отключить прежнюю версию консоли:

1. Откройте cmd.exe
1. Щелкните правой кнопкой мыши заголовок строки "->" Свойства "->" снимите флажок использовать прежнюю версию консоли
1. Нажмите кнопку "ОК".

### <a name="error-0x80040154-after-windows-update"></a>«Ошибка: 0x80040154» после обновления Windows
Подсистема Windows для Linux функции могут быть отключены во время обновления Windows. В этом случае необходимо снова включить функцию Windows. Инструкции по включению в подсистеме Windows для Linux можно найти в [руководство по установке](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui).

### <a name="changing-the-display-language"></a>Изменение отображаемого языка
Установка WSL попытается автоматически изменить языковой стандарт Ubuntu в соответствии с языковой стандарт для текущей установки Windows.  Если не хотите, чтобы это поведение, можно выполнить следующую команду, чтобы изменить языковой стандарт Ubuntu, после завершения установки.  Необходимо будет перезапустить bash.exe это изменение вступило в силу.

Ниже примере изменения языкового стандарта en-US:
``` BASH
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a>Проблемы установки после восстановления системы Windows
1.  Удалить `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux` папки. <br/>
  **Примечание. Не делайте этого, если ваш дополнительный компонент полностью установлена и работает.**
2.  Включите дополнительный компонент WSL (если он еще не)
3.  Reboot
4.  lxrun / uninstall/full
5.  Установить bash

### <a name="no-internet-access-in-wsl"></a>Нет доступа к Интернету в WSL
Некоторые пользователи сообщали о проблемах с приложениями брандмауэров, блокировать доступ к Интернету в WSL.  Брандмауэры сообщил являются:

1. Kaspersky
1. AVG
1. Приложении avast

В некоторых случаях отключение брандмауэра разрешает доступ к.  В некоторых случаях простое наличие установлен брандмауэр проверяет блокировать доступ.

### <a name="permission-denied-error-when-using-ping"></a>Ошибка предоставления разрешений отказано в доступе при использовании команды ping
#### [<a name="anniversary-update"></a>Юбилейное обновление](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14388-to-windows-10-anniversary-update) 

Для выполнения проверки связи в WSL, необходимы права администратора в Windows.  Для выполнения проверки связи, выполнять Bash на Ubuntu в Windows с правами администратора или выполнения bash.exe в командной строке CMD/PowerShell с правами администратора.

#### [<a name="build-14926"></a>Сборки 14926 +](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14926)
  Больше не требуются права администратора.

### <a name="bash-is-hung"></a>Зависание bash
Если при работе с bash, что bash зависание (или блокируют) и не отвечает на входные данные, Помогите нам диагностировать проблему, для сбора и отправки дамп памяти. Обратите внимание на то, что эти действия произойдет сбой системы. Не делайте это, если вы не удовлетворены, или сохранить результаты работы, прежде чем делать это.  <br/>
Сбор дампа памяти:
1. Измените тип дампа памяти на «полный дамп памяти». При изменении типа дампа, запишите вашего текущего типа.
2. Используйте [действия](https://blogs.technet.microsoft.com/askpfeplat/2015/04/05/how-to-force-a-diagnostic-memory-dump-when-a-computer-hangs/) для настройки аварийного завершения с помощью элемента управления с клавиатуры.
3. Для воспроизведения, зависает или взаимоблокировки.
4. Аварийно завершить работу системы с помощью клавиш из (2).
5. Система будет о сбоях и собирать дамп памяти.
6. После перезагрузки системы отчетов memory.dmp для secure@microsoft.com. По умолчанию файл дампа располагается %SystemRoot%\memory.dmp или C:\Windows\memory.dmp в случае системного диска C:. В сообщении электронной почты, обратите внимание, что дамп WSL или Bash в группе Windows.
7. Тип дампа памяти восстановите исходное значение.

### <a name="check-your-build-number"></a>Проверьте свой номер сборки

Чтобы найти номер построения архитектуры и Windows компьютера, откройте  
**Параметры** > **системы** > **о**

Найдите **сборка ОС** и **системный тип** поля.  
    ![Снимок экрана сборки и системный тип поля](media/system.png) 


Чтобы найти номер сборки Windows Server, в выполните следующую команду PowerShell:  
``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a>Убедитесь, что включен WSL
Можно проверить, включена, подсистема Windows для Linux, выполнив следующую в PowerShell:  
``` PowerShell
PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a>Проблемы с подключением OpenSSH-Server
При попытке подключиться к серверу SSH на сбой со следующей ошибкой: «Подключение закрыто, 127.0.0.1 порт 22».
1. Убедитесь, что на сервере OpenSSH выполняется:
   ``` BASH
   sudo service ssh status
   ```
   и вы выполнили в этом руководстве: https://help.ubuntu.com/lts/serverguide/openssh-server.html.en
2. Остановите службу sshd и запустите sshd в режиме отладки:
   ``` BASH
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```
3. Проверьте журналы запуска и убедитесь, что доступны ключей хоста и вы не видите сообщения журнала, такие как: debug1: sshd версии OpenSSH_7.2 debug1 1 марта 2016 1.0.2g OpenSSL: key_load_private: указано неверное парольную фразу для расшифровки закрытого ключа debug1: key_load_public : Нет такого файла или каталога не удалось загрузить ключ узла: /etc/ssh/ssh_host_rsa_key debug1: key_load_private: Нет такого файла или каталога debug1: key_load_public: Нет такого файла или каталога не удалось загрузить ключ узла: /etc/ssh/ssh_host_dsa_key debug1: key_load_private: Нет такого файла или каталога debug1: key_load_public: Нет такого файла или каталога не удалось загрузить ключ узла: /etc/ssh/ssh_host_ecdsa_key debug1: key_load_private: Нет такого файла или каталога debug1: key_load_public: Нет такого файла или каталога не удалось загрузить ключ узла: /etc/ssh/ssh_host_ed25519_key

Если вы видите такие сообщения, а в списке отсутствуют ключи `/etc/ssh/`, необходимо будет повторно создавать ключи или только Очистка и установка openssh-server:
```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

