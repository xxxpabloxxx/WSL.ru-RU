---
title: Приступая к работе с VS Code с подсистемой Windows для Linux
description: Узнайте, как настроить VS Code для создания и отладки кода с помощью подсистемы Windows для Linux.
keywords: WSL, Windows, виндовссубсистем, GNU, Linux, bash, VS Code, удаленное расширение, отладка, путь, Visual Studio
ms.date: 05/28/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: f5d7bd4f582f504ea3c4bd814454b1dc881ffed2
ms.sourcegitcommit: 97cc93f8e26391c09a31a4ab42c4b5e9d98d1c32
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/22/2020
ms.locfileid: "86948658"
---
# <a name="get-started-using-visual-studio-code-with-windows-subsystem-for-linux"></a>Приступая к работе с Visual Studio Code с подсистемой Windows для Linux

Visual Studio Code, вместе с расширением Remote-WSL, позволяет использовать WSL в качестве среды разработки для полной времени непосредственно из VS Code. Вы можете выбрать один из следующих вариантов.

* Разработка в среде под управлением Linux
* Использование цепочек инструментов и служебных программ для Linux
* Запуск и отладка приложений Linux с помощью Windows с сохранением доступа к средствам повышения производительности, таким как Outlook и Office
* Использование встроенного терминала VS Code для запуска дистрибутива Linux по выбору
* Воспользуйтесь преимуществами VS Code функций, таких как [завершение кода IntelliSense](https://code.visualstudio.com/docs/editor/intellisense), [linting](https://code.visualstudio.com/docs/python/linting), [Поддержка отладки](https://code.visualstudio.com/docs/nodejs/nodejs-debugging), [фрагменты кода](https://code.visualstudio.com/docs/editor/userdefinedsnippets)и [модульное тестирование](https://code.visualstudio.com/docs/python/testing) .
* Простота управления версиями с помощью встроенной [поддержки Git](https://code.visualstudio.com/docs/editor/versioncontrol#_git-support) VS Code
* выполнение команд и VS Code расширений непосредственно в проектах WSL
* Измените файлы в Linux или смонтированной файловой системе Windows (например,/МНТ/к), не беспокоясь о проблемах с путями, двоичной совместимости или других задачах, связанных с разными операционными системами.

## <a name="install-vs-code-and-the-remote-wsl-extension"></a>Установка VS Code и расширения Remote WSL

* Перейдите на [страницу установки VS Code](https://code.visualstudio.com/download) и выберите двоичный установщик 32 или 64. Установите Visual Studio Code в Windows (не в файловой системе WSL).

* При появлении запроса на **Выбор дополнительных задач** во время установки обязательно установите флажок **Добавить в путь** , чтобы можно было легко открыть папку в WSL с помощью команды Code.

* Установите [Пакет расширений для удаленной разработки](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack). Этот пакет расширений включает расширение Remote-WSL в дополнение к расширениям Remote-SSH и Remote-Container, что позволяет открывать любую папку в контейнере, на удаленном компьютере или в WSL.

> [!IMPORTANT]
> Чтобы установить расширение Remote-WSL, потребуется версия [1,35](https://code.visualstudio.com/updates/v1_35) или более поздняя VS Code. Не рекомендуется использовать WSL в VS Code без расширения Remote-WSL, так как будет потеряна поддержка автоматического завершения, отладки, linting и т. д. Забавный факт. это расширение WSL устанавливается в $HOME/.вскоде/екстенсионс (введите команду `ls $HOME\.vscode\extensions\` в PowerShell).

## <a name="update-your-linux-distribution"></a>Обновление дистрибутива Linux

В некоторых дистрибутивах WSL Linux отсутствуют библиотеки, необходимые для запуска сервера VS Code. Вы можете добавить дополнительные библиотеки в дистрибутив Linux с помощью диспетчера пакетов.

Например, чтобы обновить Debian или Ubuntu, используйте:

```bash
sudo apt-get update
```

Чтобы добавить wget (для получения содержимого с веб-серверов) и CA-Certificates (чтобы разрешить приложениям на основе SSL проверять подлинность SSL-соединений), введите:

```bash
sudo apt-get install wget ca-certificates
```

## <a name="open-a-wsl-project-in-visual-studio-code"></a>Откройте проект WSL в Visual Studio Code

### <a name="from-the-command-line"></a>Из командной строки

Чтобы открыть проект из дистрибутива WSL, откройте командную строку распространения и введите:`code .`

![Открыть проект WSL с VS Code удаленным сервером](../media/wsl-open-vs-code.gif)

### <a name="from-vs-code"></a>Из VS Code

Кроме того, можно получить доступ к дополнительным VS Code удаленным параметрам с помощью ярлыка: `CTRL+SHIFT+P` в VS Code, чтобы открыть палитру команд. Если затем ввести, `VSCODE-REMOTE` вы увидите все доступные VS Code удаленные параметры, что позволит повторно открыть папку в удаленном сеансе, указать, какое распространение следует открыть в, и многое другое.

![Палитра команд VS Code](../media/vscode-remote-command-palette.png)

## <a name="extensions-inside-of-vs-code-remote"></a>Расширения в VS Code Remote

Расширение Remote-WSL разделяет VS Code в архитектуру "клиент-сервер" с помощью клиента (пользовательского интерфейса), работающего на компьютере Windows, и сервера (код, Git, подключаемые модули и т. д.), запускаемые удаленно.

При запуске VS Code удаленно на вкладке "расширения" отобразится список расширений, разделенных между локальным компьютером и дистрибутивом WSL.

Установка локального расширения, например [темы](https://marketplace.visualstudio.com/search?target=VSCode&category=Themes&sortBy=Installs), должна быть установлена только один раз.

Некоторые расширения, такие как [расширение Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python) или все, что обрабатывает такие действия, как linting или Отладка, должны устанавливаться отдельно на каждом удаленном распределении WSL. VS Code отобразит значок предупреждения ⚠ , а также зеленую кнопку "установить в WSL", если установлено локальное расширение, которое не установлено на удаленном компьютере WSL.

![VS Code с расширениями Remote-WSL и локальными расширениями](../media/vscode-remote-wsl-extensions.png)

Дополнительные сведения см. в VS Code документах:

* При запуске VS Code Remote в WSL сценарии запуска оболочки запускаться не будут. Дополнительные сведения о выполнении дополнительных команд или изменении среды см. в этой [статье о сценариях расширенной настройки среды](https://code.visualstudio.com/docs/remote/wsl#_advanced-environment-setup-script) .

* Возникли проблемы при запуске VS Code из командной строки WSL? В этом [руководство по устранению неполадок](https://code.visualstudio.com/docs/remote/troubleshooting#_fixing-problems-with-the-code-command-not-working) содержатся советы по изменению переменных пути, устранению ошибок расширения, связанных с отсутствием зависимостей, устранению проблем с завершением строк Git, установке локального VSIX на удаленном компьютере, запуску окна браузера, порту localhost для блокировки, веб-сокеты не работают, ошибки при хранении данных расширения и многое другое.

## <a name="install-git-optional"></a>Установка Git (необязательно)

Если вы планируете работать совместно с другими пользователями или размещать проект на сайте с открытым исходным кодом (например, GitHub), примите во внимание, что VS Code поддерживает [управление версиями с помощью Git](https://code.visualstudio.com/docs/editor/versioncontrol#_git-support). Вкладка системы управления версиями в VS Code отслеживает все изменения и содержит общие команды Git (добавление, фиксация, принудительная отправка, извлечение) прямо в пользовательском интерфейсе.

Сведения об установке Git см. в статье [Настройка Git для работы с подсистемой Windows для Linux](./wsl-git.md).

## <a name="install-windows-terminal-optional"></a>Установка Терминала Windows (необязательно)

Новый терминал Windows включает несколько вкладок (для быстрого переключения между командной строкой, PowerShell или несколькими дистрибутивами Linux), настраиваемыми пользовательскими привязками клавиш (создайте собственные сочетания клавиш для открытия и закрытия вкладок, копирования и вставки и т. д.), эмодзи ☺ и пользовательские темы (цветовые схемы, стили и размеры шрифтов, фоновое изображение, размытие и прозрачность). Дополнительные сведения см. в документации по [терминалу Windows](https://docs.microsoft.com/windows/terminal).

1. Скачайте [Терминал Windows из Microsoft Store](https://www.microsoft.com/store/apps/9n0dx20hk701): При установке через магазин обновления выполняются автоматически.

2. После установки откройте Терминал Windows и щелкните **Параметры**, чтобы настроить Терминал использовать файл `profile.json`.

## <a name="additional-resources"></a>Дополнительные ресурсы

* [VS Code Удаленная разработка](https://code.visualstudio.com/docs/remote/remote-overview)
* [Советы и рекомендации по удаленной разработке](https://code.visualstudio.com/docs/remote/troubleshooting)
* [Руководство по удаленной разработке с помощью WSL](https://code.visualstudio.com/remote-tutorials/wsl/getting-started)
* [Использование DOCKER с WSL 2 и VS Code](https://code.visualstudio.com/blogs/2020/03/02/docker-in-wsl2)
* [Использование C++ и WSL в VS Code](https://code.visualstudio.com/docs/cpp/config-wsl)
* [Удаленная служба R для Linux](https://docs.microsoft.com/visualstudio/rtvs/setting-up-remote-r-service-on-linux?view=vs-2017)

К дополнительным рекомендуемым расширениям относятся следующие:

* [Раскладки клавиатуры других редакторов](https://marketplace.visualstudio.com/search?target=VSCode&category=Keymaps&sortBy=Downloads) — эти расширения позволят использовать необходимую раскладку при переходе в другой текстовый редактор (например, Atom, Sublime, Vim, eMacs, Notepad++ и т. п.).
* [Расширение синхронизации параметров](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync) — позволяет синхронизировать параметры VS Code в разных установках, используя GitHub. Если вы работаете на разных компьютерах, это обеспечит согласованность среды между ними.
* [Отладчик для Chrome](https://code.visualstudio.com/blogs/2016/02/23/introducing-chrome-debugger-for-vs-code): после завершения разработки на стороне сервера с Linux необходимо разработать и протестировать клиентскую часть. Это расширение интегрирует редактор VS Code со службой отладки браузера Chrome, что увеличивает эффективность выполнения операций.
