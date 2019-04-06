---
title: Дополнительные сведения о подсистеме Windows для Linux
description: Дополнительные сведения о работе подсистемы Windows для Linux.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, gnu, linux
author: scooley
ms.author: scooley
ms.date: 07/11/2016
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.openlocfilehash: a9c8d32f2b87319b45b1b757b4d71c0a4c41292c
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063512"
---
# <a name="windows-subsystem-for-linux-documentation"></a><span data-ttu-id="03921-104">Подсистема Windows для документации Linux</span><span class="sxs-lookup"><span data-stu-id="03921-104">Windows Subsystem for Linux Documentation</span></span>

<span data-ttu-id="03921-105">Подсистема Windows для Linux позволяет разработчикам запускать среду GNU/Linux — в том числе наиболее командной строки средства, служебные программы и приложения — непосредственно на Windows, без издержек на виртуальную машину в неизмененном.</span><span class="sxs-lookup"><span data-stu-id="03921-105">The Windows Subsystem for Linux lets developers run GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a virtual machine.</span></span>  

<span data-ttu-id="03921-106">Можно выполнить следующие действия: </span><span class="sxs-lookup"><span data-stu-id="03921-106">You can:</span></span>

1. <span data-ttu-id="03921-107">Выберите нужные вам дистрибутивы GNU/Linux [из Windows Store](https://aka.ms/wslstore).</span><span class="sxs-lookup"><span data-stu-id="03921-107">Choose your favorite GNU/Linux distributions [from the Windows Store](https://aka.ms/wslstore).</span></span>
1. <span data-ttu-id="03921-108">Выполнять распространенные командной строки бесплатное программное обеспечение, например `grep`, `sed`, `awk`, или другие двоичные файлы ELF-64.</span><span class="sxs-lookup"><span data-stu-id="03921-108">Run common command-line free software such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span> 
1. <span data-ttu-id="03921-109">Выполнение сценариев оболочки Bash и включая приложения командной строки GNU/Linux:</span><span class="sxs-lookup"><span data-stu-id="03921-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="03921-110">Средства: vim, emacs, tmux</span><span class="sxs-lookup"><span data-stu-id="03921-110">Tools: vim, emacs, tmux</span></span>
    * <span data-ttu-id="03921-111">Языки: JavaScript/node.js, Ruby, Python, C/C++, C# & F#, доверять, Go и т. п.</span><span class="sxs-lookup"><span data-stu-id="03921-111">Languages: Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go, etc.</span></span>
    * <span data-ttu-id="03921-112">Службы: sshd, MySQL, Apache, lighttpd</span><span class="sxs-lookup"><span data-stu-id="03921-112">Services: sshd, MySQL, Apache, lighttpd</span></span>
1. <span data-ttu-id="03921-113">Установка дополнительного программного обеспечения, с помощью диспетчера пакетов распространения собственных GNU/Linux.</span><span class="sxs-lookup"><span data-stu-id="03921-113">Install additional software using own GNU/Linux distribution package manager.</span></span>
1. <span data-ttu-id="03921-114">Вызовите с помощью это оболочка командной строки Unix подобных приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="03921-114">Invoke Windows applications using a Unix-like command-line shell.</span></span>
1. <span data-ttu-id="03921-115">Вызов приложения GNU/Linux на Windows.</span><span class="sxs-lookup"><span data-stu-id="03921-115">Invoke GNU/Linux applications on Windows.</span></span>

## <a name="getting-started"></a><span data-ttu-id="03921-116">Начало работы</span><span class="sxs-lookup"><span data-stu-id="03921-116">Getting started</span></span>

* [<span data-ttu-id="03921-117">Установка Linux на Windows</span><span class="sxs-lookup"><span data-stu-id="03921-117">Install Linux on Windows</span></span>](install_guide.md)
* [<span data-ttu-id="03921-118">Посетите Справочник по командам</span><span class="sxs-lookup"><span data-stu-id="03921-118">Visit the command reference</span></span>](reference.md)
* [<span data-ttu-id="03921-119">Часто задаваемые вопросы</span><span class="sxs-lookup"><span data-stu-id="03921-119">Read frequently asked questions</span></span>](faq.md)

## <a name="team-blogs"></a><span data-ttu-id="03921-120">Блоги группы разработчиков</span><span class="sxs-lookup"><span data-stu-id="03921-120">Team Blogs</span></span>
*  [<span data-ttu-id="03921-121">Общие сведения о post с коллекцией видеоматериалы и блоги</span><span class="sxs-lookup"><span data-stu-id="03921-121">Overview post with a collection of videos and blogs</span></span>](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* <span data-ttu-id="03921-122">[Блог командной строки](https://blogs.msdn.microsoft.com/commandline/) (активно)</span><span class="sxs-lookup"><span data-stu-id="03921-122">[Command-Line blog](https://blogs.msdn.microsoft.com/commandline/) (Active)</span></span>
* <span data-ttu-id="03921-123">[Подсистема Windows для Linux блог](https://blogs.msdn.microsoft.com/wsl/) (историческая)</span><span class="sxs-lookup"><span data-stu-id="03921-123">[Windows Subsystem for Linux Blog](https://blogs.msdn.microsoft.com/wsl/) (Historical)</span></span>

## <a name="posts--articles"></a><span data-ttu-id="03921-124">Сообщения и статьи</span><span class="sxs-lookup"><span data-stu-id="03921-124">Posts & Articles</span></span>
* [<span data-ttu-id="03921-125">Запуск Bash для Ubuntu в Windows</span><span class="sxs-lookup"><span data-stu-id="03921-125">Run Bash on Ubuntu on Windows</span></span>](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [<span data-ttu-id="03921-126">Разработчикам использовать Bash и двоичные файлы Usermode Ubuntu Linux в Windows 10</span><span class="sxs-lookup"><span data-stu-id="03921-126">Developers Can Run Bash And Usermode Ubuntu Linux Binaries On Windows 10</span></span>](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [<span data-ttu-id="03921-127">Ubuntu в Windows — Ubuntu Userspace для разработчиков Windows</span><span class="sxs-lookup"><span data-stu-id="03921-127">Ubuntu on Windows – The Ubuntu Userspace for Windows Developers</span></span>](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a><span data-ttu-id="03921-128">Предоставление отзыва</span><span class="sxs-lookup"><span data-stu-id="03921-128">Provide Feedback</span></span>
* [<span data-ttu-id="03921-129">Средство отслеживания вопросов GitHub</span><span class="sxs-lookup"><span data-stu-id="03921-129">GitHub issue tracker</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="03921-130">Командной строки портал UserVoice</span><span class="sxs-lookup"><span data-stu-id="03921-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
