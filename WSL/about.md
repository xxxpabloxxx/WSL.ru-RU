---
title: Подробнее о подсистеме Windows для Linux
description: Узнайте больше о том, как работает подсистема Windows для Linux.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, gnu, linux
author: scooley
ms.author: scooley
ms.date: 07/11/2016
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 7c8e3b3f7ec13109485d7efa29739dadc8bfacf7
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122671"
---
# <a name="windows-subsystem-for-linux-documentation"></a>Документация по подсистеме Windows для Linux

Подсистема Windows для Linux позволяет разработчикам запускать среду GNU/Linux, включая большинство программ командной строки, служебных программ и приложений, непосредственно в Windows без каких-либо изменений, избавляя от необходимости использовать отдельную виртуальную машину.  

Можно сделать следующее.

1. Выберите предпочтительные дистрибутивы GNU/Linux [из Microsoft Store](https://aka.ms/wslstore).
1. Запускайте бесплатные программы командной строки, например `grep`, `sed`, `awk`, или другие двоичные файлы ELF-64. 
1. Запускайте сценарии Bash Shell и приложения командной строки GNU/Linux, включая:  
    * инструменты: vim, emacs, tmux;
    * языки: JavaScript/Node.js, Ruby, Python, C/C++, C# и F#, Rust, Go и т. д.;
    * службы: sshd, MySQL, Apache, lighttpd.
1. Установите дополнительное программное обеспечение с помощью собственного диспетчера пакетов дистрибутивов GNU/Linux.
1. Вызывайте приложения Windows с помощью оболочки командной строки, похожей на UNIX.
1. Вызывайте приложения GNU/Linux в Windows.

## <a name="getting-started"></a>начало работы

* [Установка Linux в Windows 10](install-win10.md)
* [Справочные материалы по командам](reference.md)
* [Часто задаваемые вопросы](faq.md)

## <a name="team-blogs"></a>Блоги группы
*  [Обзор записи с коллекцией видео и блогов](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* [Блог по командной строке](https://blogs.msdn.microsoft.com/commandline/) (активный)
* [Блог о подсистеме Windows для Linux](https://blogs.msdn.microsoft.com/wsl/) (хронологический)

## <a name="posts--articles"></a>Записи и статьи
* [Запуск Bash для Ubuntu в Windows](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [Разработчики могут запускать Bash и двоичные файлы Ubuntu Linux пользовательского режима в Windows 10](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [Ubuntu в Windows: пространство пользователей Ubuntu для разработчиков Windows](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a>Предоставление отзыва
* [Средство отслеживания проблем GitHub](https://github.com/Microsoft/BashOnWindows/issues)
* [Портал UserVoice для командной строки](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
