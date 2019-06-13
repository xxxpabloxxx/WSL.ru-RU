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
ms.localizationpriority: High
ms.openlocfilehash: f2df3c06d6c56aa8bc5a41ea9f075635b70c8685
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040804"
---
# <a name="windows-subsystem-for-linux-documentation"></a><span data-ttu-id="28801-104">Подсистема Windows для документации Linux</span><span class="sxs-lookup"><span data-stu-id="28801-104">Windows Subsystem for Linux Documentation</span></span>

<span data-ttu-id="28801-105">Подсистема Windows для Linux позволяет разработчикам запускать среду GNU/Linux — в том числе наиболее командной строки средства, служебные программы и приложения — непосредственно на Windows, без издержек на виртуальную машину в неизмененном.</span><span class="sxs-lookup"><span data-stu-id="28801-105">The Windows Subsystem for Linux lets developers run GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a virtual machine.</span></span>  

<span data-ttu-id="28801-106">Можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="28801-106">You can:</span></span>

1. <span data-ttu-id="28801-107">Выберите нужные вам дистрибутивы GNU/Linux [из Windows Store](https://aka.ms/wslstore).</span><span class="sxs-lookup"><span data-stu-id="28801-107">Choose your favorite GNU/Linux distributions [from the Windows Store](https://aka.ms/wslstore).</span></span>
1. <span data-ttu-id="28801-108">Выполнять распространенные командной строки бесплатное программное обеспечение, например `grep`, `sed`, `awk`, или другие двоичные файлы ELF-64.</span><span class="sxs-lookup"><span data-stu-id="28801-108">Run common command-line free software such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span> 
1. <span data-ttu-id="28801-109">Выполнение сценариев оболочки Bash и включая приложения командной строки GNU/Linux:</span><span class="sxs-lookup"><span data-stu-id="28801-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="28801-110">Средства: vim, emacs, tmux</span><span class="sxs-lookup"><span data-stu-id="28801-110">Tools: vim, emacs, tmux</span></span>
    * <span data-ttu-id="28801-111">Языки: JavaScript/node.js, Ruby, Python, C/C++, C# & F#, доверять, Go и т. п.</span><span class="sxs-lookup"><span data-stu-id="28801-111">Languages: Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go, etc.</span></span>
    * <span data-ttu-id="28801-112">Службы: sshd, MySQL, Apache, lighttpd</span><span class="sxs-lookup"><span data-stu-id="28801-112">Services: sshd, MySQL, Apache, lighttpd</span></span>
1. <span data-ttu-id="28801-113">Установка дополнительного программного обеспечения, с помощью диспетчера пакетов распространения собственных GNU/Linux.</span><span class="sxs-lookup"><span data-stu-id="28801-113">Install additional software using own GNU/Linux distribution package manager.</span></span>
1. <span data-ttu-id="28801-114">Вызовите с помощью это оболочка командной строки Unix подобных приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="28801-114">Invoke Windows applications using a Unix-like command-line shell.</span></span>
1. <span data-ttu-id="28801-115">Вызов приложения GNU/Linux на Windows.</span><span class="sxs-lookup"><span data-stu-id="28801-115">Invoke GNU/Linux applications on Windows.</span></span>

## <a name="getting-started"></a><span data-ttu-id="28801-116">начало работы</span><span class="sxs-lookup"><span data-stu-id="28801-116">Getting Started</span></span>

* [<span data-ttu-id="28801-117">Установка Linux в Windows 10</span><span class="sxs-lookup"><span data-stu-id="28801-117">Install Linux on Windows 10</span></span>](install-win10.md)
* [<span data-ttu-id="28801-118">Посетите Справочник по командам</span><span class="sxs-lookup"><span data-stu-id="28801-118">Visit the command reference</span></span>](reference.md)
* [<span data-ttu-id="28801-119">Часто задаваемые вопросы</span><span class="sxs-lookup"><span data-stu-id="28801-119">Read frequently asked questions</span></span>](faq.md)

## <a name="team-blogs"></a><span data-ttu-id="28801-120">Блоги группы разработчиков</span><span class="sxs-lookup"><span data-stu-id="28801-120">Team Blogs</span></span>
*  [<span data-ttu-id="28801-121">Общие сведения о post с коллекцией видеоматериалы и блоги</span><span class="sxs-lookup"><span data-stu-id="28801-121">Overview post with a collection of videos and blogs</span></span>](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* <span data-ttu-id="28801-122">[Блог командной строки](https://blogs.msdn.microsoft.com/commandline/) (активно)</span><span class="sxs-lookup"><span data-stu-id="28801-122">[Command-Line blog](https://blogs.msdn.microsoft.com/commandline/) (Active)</span></span>
* <span data-ttu-id="28801-123">[Подсистема Windows для Linux блог](https://blogs.msdn.microsoft.com/wsl/) (историческая)</span><span class="sxs-lookup"><span data-stu-id="28801-123">[Windows Subsystem for Linux Blog](https://blogs.msdn.microsoft.com/wsl/) (Historical)</span></span>

## <a name="posts--articles"></a><span data-ttu-id="28801-124">Сообщения и статьи</span><span class="sxs-lookup"><span data-stu-id="28801-124">Posts & Articles</span></span>
* [<span data-ttu-id="28801-125">Выполнения Bash на Ubuntu в Windows</span><span class="sxs-lookup"><span data-stu-id="28801-125">Run Bash on Ubuntu on Windows</span></span>](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [<span data-ttu-id="28801-126">Разработчикам использовать Bash и двоичные файлы Usermode Ubuntu Linux в Windows 10</span><span class="sxs-lookup"><span data-stu-id="28801-126">Developers Can Run Bash And Usermode Ubuntu Linux Binaries On Windows 10</span></span>](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [<span data-ttu-id="28801-127">Ubuntu в Windows — Ubuntu Userspace для разработчиков Windows</span><span class="sxs-lookup"><span data-stu-id="28801-127">Ubuntu on Windows – The Ubuntu Userspace for Windows Developers</span></span>](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a><span data-ttu-id="28801-128">Предоставление отзыва</span><span class="sxs-lookup"><span data-stu-id="28801-128">Provide Feedback</span></span>
* [<span data-ttu-id="28801-129">Средство отслеживания вопросов GitHub</span><span class="sxs-lookup"><span data-stu-id="28801-129">GitHub issue tracker</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="28801-130">Командной строки портал UserVoice</span><span class="sxs-lookup"><span data-stu-id="28801-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
