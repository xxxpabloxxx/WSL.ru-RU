---
title: Сведения о подсистеме Windows для Linux
description: Дополнительные сведения о работе подсистемы Windows для Linux.
keywords: Башонвиндовс, bash, WSL, Windows, виндовссубсистем, GNU, Linux
author: scooley
ms.author: scooley
ms.date: 07/11/2016
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: High
ms.openlocfilehash: edff78b1447aa382253417d27df52fe497c58b08
ms.sourcegitcommit: e17038c166b69f73e593ae3ac351c9d66e2ba64b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2019
ms.locfileid: "67694628"
---
# <a name="windows-subsystem-for-linux-documentation"></a><span data-ttu-id="8f72f-104">Документация по подсистеме Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="8f72f-104">Windows Subsystem for Linux Documentation</span></span>

<span data-ttu-id="8f72f-105">Подсистема Windows для Linux позволяет разработчикам запускать среду GNU/Linux, включая большинство программ командной строки, служебные программы и приложения, непосредственно в Windows, без изменений, не изменяя нагрузку на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="8f72f-105">The Windows Subsystem for Linux lets developers run a GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a virtual machine.</span></span>  

<span data-ttu-id="8f72f-106">Можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="8f72f-106">You can:</span></span>

1. <span data-ttu-id="8f72f-107">Выберите предпочтительные дистрибутивы GNU/Linux [из Microsoft Store](https://aka.ms/wslstore).</span><span class="sxs-lookup"><span data-stu-id="8f72f-107">Choose your favorite GNU/Linux distributions [from the Microsoft Store](https://aka.ms/wslstore).</span></span>
1. <span data-ttu-id="8f72f-108">Запустите общедоступное программное обеспечение для `grep`командной строки `sed` `awk`, например,, или другие двоичные файлы ELF-64.</span><span class="sxs-lookup"><span data-stu-id="8f72f-108">Run common command-line free software such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span> 
1. <span data-ttu-id="8f72f-109">Запускайте скрипты Bash Shell и приложения командной строки GNU/Linux, включая:</span><span class="sxs-lookup"><span data-stu-id="8f72f-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="8f72f-110">Средства: vim, Emacs, тмукс</span><span class="sxs-lookup"><span data-stu-id="8f72f-110">Tools: vim, emacs, tmux</span></span>
    * <span data-ttu-id="8f72f-111">Языки: JavaScript/Node. js, Ruby, Python, C/C++, C# & F#, Руст, Go и т. д.</span><span class="sxs-lookup"><span data-stu-id="8f72f-111">Languages: Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go, etc.</span></span>
    * <span data-ttu-id="8f72f-112">Службы: sshd, MySQL, Apache, лигхттпд</span><span class="sxs-lookup"><span data-stu-id="8f72f-112">Services: sshd, MySQL, Apache, lighttpd</span></span>
1. <span data-ttu-id="8f72f-113">Установка дополнительного программного обеспечения с помощью собственного диспетчера пакетов для GNU/Linux.</span><span class="sxs-lookup"><span data-stu-id="8f72f-113">Install additional software using own GNU/Linux distribution package manager.</span></span>
1. <span data-ttu-id="8f72f-114">Вызов приложений Windows с помощью оболочки командной строки, похожей на UNIX.</span><span class="sxs-lookup"><span data-stu-id="8f72f-114">Invoke Windows applications using a Unix-like command-line shell.</span></span>
1. <span data-ttu-id="8f72f-115">Вызывайте приложения GNU/Linux в Windows.</span><span class="sxs-lookup"><span data-stu-id="8f72f-115">Invoke GNU/Linux applications on Windows.</span></span>

## <a name="getting-started"></a><span data-ttu-id="8f72f-116">Начало работы</span><span class="sxs-lookup"><span data-stu-id="8f72f-116">Getting Started</span></span>

* [<span data-ttu-id="8f72f-117">Установка Linux в Windows 10</span><span class="sxs-lookup"><span data-stu-id="8f72f-117">Install Linux on Windows 10</span></span>](install-win10.md)
* [<span data-ttu-id="8f72f-118">См. Справочник по командам</span><span class="sxs-lookup"><span data-stu-id="8f72f-118">Visit the command reference</span></span>](reference.md)
* [<span data-ttu-id="8f72f-119">Ознакомьтесь с часто задаваемыми вопросами</span><span class="sxs-lookup"><span data-stu-id="8f72f-119">Read frequently asked questions</span></span>](faq.md)

## <a name="team-blogs"></a><span data-ttu-id="8f72f-120">Блоги группы</span><span class="sxs-lookup"><span data-stu-id="8f72f-120">Team Blogs</span></span>
*  [<span data-ttu-id="8f72f-121">Обзор записи с коллекцией видео и блогов</span><span class="sxs-lookup"><span data-stu-id="8f72f-121">Overview post with a collection of videos and blogs</span></span>](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* <span data-ttu-id="8f72f-122">[Блог командной строки](https://blogs.msdn.microsoft.com/commandline/) Active</span><span class="sxs-lookup"><span data-stu-id="8f72f-122">[Command-Line blog](https://blogs.msdn.microsoft.com/commandline/) (Active)</span></span>
* <span data-ttu-id="8f72f-123">[Блог подсистемы Windows для Linux](https://blogs.msdn.microsoft.com/wsl/) Исторических</span><span class="sxs-lookup"><span data-stu-id="8f72f-123">[Windows Subsystem for Linux Blog](https://blogs.msdn.microsoft.com/wsl/) (Historical)</span></span>

## <a name="posts--articles"></a><span data-ttu-id="8f72f-124">Записи & статьи</span><span class="sxs-lookup"><span data-stu-id="8f72f-124">Posts & Articles</span></span>
* [<span data-ttu-id="8f72f-125">Запуск Bash в Ubuntu в Windows</span><span class="sxs-lookup"><span data-stu-id="8f72f-125">Run Bash on Ubuntu on Windows</span></span>](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [<span data-ttu-id="8f72f-126">Разработчики могут запускать двоичные файлы Bash и Ubuntu Linux пользовательского режима в Windows 10</span><span class="sxs-lookup"><span data-stu-id="8f72f-126">Developers Can Run Bash And Usermode Ubuntu Linux Binaries On Windows 10</span></span>](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [<span data-ttu-id="8f72f-127">Ubuntu в Windows — Усерспаце Ubuntu для разработчиков Windows</span><span class="sxs-lookup"><span data-stu-id="8f72f-127">Ubuntu on Windows – The Ubuntu Userspace for Windows Developers</span></span>](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a><span data-ttu-id="8f72f-128">Предоставление отзыва</span><span class="sxs-lookup"><span data-stu-id="8f72f-128">Provide Feedback</span></span>
* [<span data-ttu-id="8f72f-129">Средство записи проблем GitHub</span><span class="sxs-lookup"><span data-stu-id="8f72f-129">GitHub issue tracker</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="8f72f-130">Портал UserVoice для командной строки</span><span class="sxs-lookup"><span data-stu-id="8f72f-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
