---
title: Подробнее о подсистеме Windows для Linux
description: Узнайте больше о том, как работает подсистема Windows для Linux.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, gnu, linux
ms.date: 07/11/2016
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: fbb1ce5cf5d5c83e25d0a6a0cece7b70537a44a1
ms.sourcegitcommit: 3be576f946611cf36e27745bdb7c4c52af1b9928
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "74200193"
---
# <a name="windows-subsystem-for-linux-documentation"></a><span data-ttu-id="2af21-104">Документация по подсистеме Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="2af21-104">Windows Subsystem for Linux Documentation</span></span>

<span data-ttu-id="2af21-105">Подсистема Windows для Linux позволяет разработчикам запускать среду GNU/Linux, включая большинство программ командной строки, служебных программ и приложений, непосредственно в Windows без каких-либо изменений, избавляя от необходимости использовать отдельную виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="2af21-105">The Windows Subsystem for Linux lets developers run a GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a virtual machine.</span></span>  

<span data-ttu-id="2af21-106">Можно сделать следующее.</span><span class="sxs-lookup"><span data-stu-id="2af21-106">You can:</span></span>

1. <span data-ttu-id="2af21-107">Выберите предпочтительные дистрибутивы GNU/Linux [из Microsoft Store](https://aka.ms/wslstore).</span><span class="sxs-lookup"><span data-stu-id="2af21-107">Choose your favorite GNU/Linux distributions [from the Microsoft Store](https://aka.ms/wslstore).</span></span>
1. <span data-ttu-id="2af21-108">Запускайте бесплатные программы командной строки, например `grep`, `sed`, `awk`, или другие двоичные файлы ELF-64.</span><span class="sxs-lookup"><span data-stu-id="2af21-108">Run common command-line free software such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span> 
1. <span data-ttu-id="2af21-109">Запускайте сценарии Bash Shell и приложения командной строки GNU/Linux, включая:</span><span class="sxs-lookup"><span data-stu-id="2af21-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="2af21-110">инструменты: vim, emacs, tmux;</span><span class="sxs-lookup"><span data-stu-id="2af21-110">Tools: vim, emacs, tmux</span></span>
    * <span data-ttu-id="2af21-111">языки: JavaScript/Node.js, Ruby, Python, C/C++, C# и F#, Rust, Go и т. д.;</span><span class="sxs-lookup"><span data-stu-id="2af21-111">Languages: Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go, etc.</span></span>
    * <span data-ttu-id="2af21-112">службы: sshd, MySQL, Apache, lighttpd.</span><span class="sxs-lookup"><span data-stu-id="2af21-112">Services: sshd, MySQL, Apache, lighttpd</span></span>
1. <span data-ttu-id="2af21-113">Установите дополнительное программное обеспечение с помощью собственного диспетчера пакетов дистрибутивов GNU/Linux.</span><span class="sxs-lookup"><span data-stu-id="2af21-113">Install additional software using own GNU/Linux distribution package manager.</span></span>
1. <span data-ttu-id="2af21-114">Вызывайте приложения Windows с помощью оболочки командной строки, похожей на UNIX.</span><span class="sxs-lookup"><span data-stu-id="2af21-114">Invoke Windows applications using a Unix-like command-line shell.</span></span>
1. <span data-ttu-id="2af21-115">Вызывайте приложения GNU/Linux в Windows.</span><span class="sxs-lookup"><span data-stu-id="2af21-115">Invoke GNU/Linux applications on Windows.</span></span>

## <a name="getting-started"></a><span data-ttu-id="2af21-116">Начало работы</span><span class="sxs-lookup"><span data-stu-id="2af21-116">Getting Started</span></span>

* [<span data-ttu-id="2af21-117">Установка Linux в Windows 10</span><span class="sxs-lookup"><span data-stu-id="2af21-117">Install Linux on Windows 10</span></span>](install-win10.md)
* [<span data-ttu-id="2af21-118">Справочные материалы по командам</span><span class="sxs-lookup"><span data-stu-id="2af21-118">Visit the command reference</span></span>](reference.md)
* [<span data-ttu-id="2af21-119">Часто задаваемые вопросы</span><span class="sxs-lookup"><span data-stu-id="2af21-119">Read frequently asked questions</span></span>](faq.md)

## <a name="team-blogs"></a><span data-ttu-id="2af21-120">Блоги группы</span><span class="sxs-lookup"><span data-stu-id="2af21-120">Team Blogs</span></span>
*  [<span data-ttu-id="2af21-121">Обзор записи с коллекцией видео и блогов</span><span class="sxs-lookup"><span data-stu-id="2af21-121">Overview post with a collection of videos and blogs</span></span>](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* <span data-ttu-id="2af21-122">[Блог по командной строке](https://blogs.msdn.microsoft.com/commandline/) (активный)</span><span class="sxs-lookup"><span data-stu-id="2af21-122">[Command-Line blog](https://blogs.msdn.microsoft.com/commandline/) (Active)</span></span>
* <span data-ttu-id="2af21-123">[Блог о подсистеме Windows для Linux](https://blogs.msdn.microsoft.com/wsl/) (хронологический)</span><span class="sxs-lookup"><span data-stu-id="2af21-123">[Windows Subsystem for Linux Blog](https://blogs.msdn.microsoft.com/wsl/) (Historical)</span></span>

## <a name="posts--articles"></a><span data-ttu-id="2af21-124">Записи и статьи</span><span class="sxs-lookup"><span data-stu-id="2af21-124">Posts & Articles</span></span>
* [<span data-ttu-id="2af21-125">Запуск Bash для Ubuntu в Windows</span><span class="sxs-lookup"><span data-stu-id="2af21-125">Run Bash on Ubuntu on Windows</span></span>](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [<span data-ttu-id="2af21-126">Разработчики могут запускать Bash и двоичные файлы Ubuntu Linux пользовательского режима в Windows 10</span><span class="sxs-lookup"><span data-stu-id="2af21-126">Developers Can Run Bash And Usermode Ubuntu Linux Binaries On Windows 10</span></span>](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [<span data-ttu-id="2af21-127">Ubuntu в Windows: пространство пользователей Ubuntu для разработчиков Windows</span><span class="sxs-lookup"><span data-stu-id="2af21-127">Ubuntu on Windows – The Ubuntu Userspace for Windows Developers</span></span>](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a><span data-ttu-id="2af21-128">Предоставление отзыва</span><span class="sxs-lookup"><span data-stu-id="2af21-128">Provide Feedback</span></span>
* [<span data-ttu-id="2af21-129">Средство отслеживания проблем GitHub</span><span class="sxs-lookup"><span data-stu-id="2af21-129">GitHub issue tracker</span></span>](https://github.com/Microsoft/BashOnWindows/issues)

