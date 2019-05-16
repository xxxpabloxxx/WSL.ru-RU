---
title: Вопросы и ответы
description: Часто задаваемые вопросы о подсистеме Windows для Linux.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, часто задаваемые вопросы
author: taraj
ms.author: taraj
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.openlocfilehash: 80675d8452b626ebe1d235774167c5ff27e4b44d
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063272"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a><span data-ttu-id="08832-104">Часто задаваемые вопросы о подсистеме Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="08832-104">Frequently Asked Questions about Windows Subsystem for Linux</span></span>

## <a name="what-is-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="08832-105">Что такое подсистема Windows для Linux (WSL)?</span><span class="sxs-lookup"><span data-stu-id="08832-105">What is Windows Subsystem for Linux (WSL)?</span></span>
<span data-ttu-id="08832-106">Подсистема Windows для Linux (WSL) — это новая функция Windows 10, которая позволяет запускать собственные программы командной строки Linux непосредственно в Windows, вместе с вашей традиционными настольными Windows и современные приложения из магазина.</span><span class="sxs-lookup"><span data-stu-id="08832-106">The Windows Subsystem for Linux (WSL) is a new Windows 10 feature that enables you to run native Linux command-line tools directly on Windows, alongside your traditional Windows desktop and modern store apps.</span></span>

<span data-ttu-id="08832-107">См. в разделе [о странице](./about.md) для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="08832-107">See the [about page](./about.md) for more details.</span></span>

## <a name="who-is-wsl-for"></a><span data-ttu-id="08832-108">Кто является WSL для?</span><span class="sxs-lookup"><span data-stu-id="08832-108">Who is WSL for?</span></span>
<span data-ttu-id="08832-109">Это в первую очередь инструмент для разработчиков — особенно веб-разработчиков и тех, кто работает и с проектами с открытым исходным кодом.</span><span class="sxs-lookup"><span data-stu-id="08832-109">This is primarily a tool for developers -- especially web developers and those who work on or with open source projects.</span></span> <span data-ttu-id="08832-110">Это позволяет пользователям нужно использовать Bash, Общие средства Linux (`sed`, `awk`т. д.) и множество средств Linux-first (Ruby, Python и др.), выполнять их цепочка инструментов для Windows.</span><span class="sxs-lookup"><span data-stu-id="08832-110">This allows those who want/need to use Bash, common Linux tools (`sed`, `awk`, etc.) and many Linux-first tools (Ruby, Python, etc.) to use their toolchain on Windows.</span></span>

## <a name="what-can-i-do-with-wsl"></a><span data-ttu-id="08832-111">Что можно делать с WSL?</span><span class="sxs-lookup"><span data-stu-id="08832-111">What can I do with WSL?</span></span>
<span data-ttu-id="08832-112">WSL предоставляет приложение с именем Bash.exe, при запуске, откроется консоли Windows, запущенной в оболочке Bash.</span><span class="sxs-lookup"><span data-stu-id="08832-112">WSL provides an application called Bash.exe that, when started, opens a Windows console running the Bash shell.</span></span> <span data-ttu-id="08832-113">С помощью Bash, можно использовать средства командной строки Linux и приложений.</span><span class="sxs-lookup"><span data-stu-id="08832-113">Using Bash, you can run command-line Linux tools and apps.</span></span> <span data-ttu-id="08832-114">Например, введите `lsb_release -a` и нажмите клавишу ВВОД; вы увидите сведения о текущих дистрибутива Linux:</span><span class="sxs-lookup"><span data-stu-id="08832-114">For example, type `lsb_release -a` and hit enter; you’ll see details of the Linux distro currently running:</span></span>

![Снимок экрана сведений о дистрибутива](media/distro.png)

<span data-ttu-id="08832-116">Также можно получить доступ к файловой системы локального компьютера из в оболочке Bash в Linux — вы найдете локальные диски подключены в `/mnt` папку.</span><span class="sxs-lookup"><span data-stu-id="08832-116">You can also access your local machine’s filesystem from within the Linux Bash shell – you’ll find your local drives mounted under the `/mnt` folder.</span></span> <span data-ttu-id="08832-117">Например ваш `C:` диск подключается в разделе `/mnt/c`:</span><span class="sxs-lookup"><span data-stu-id="08832-117">For example, your `C:` drive is mounted under `/mnt/c`:</span></span>  

![Снимок экрана подключенный диск C](media/ls.png)

## <a name="what-is-bash"></a><span data-ttu-id="08832-119">Что такое Bash</span><span class="sxs-lookup"><span data-stu-id="08832-119">What is Bash?</span></span>
<span data-ttu-id="08832-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) — это популярный текстовой оболочки и командный язык.</span><span class="sxs-lookup"><span data-stu-id="08832-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) is a popular text-based shell and command-language.</span></span> <span data-ttu-id="08832-121">Это оболочка по умолчанию, включенных в Ubuntu и других дистрибутивов Linux, а также в macOS.</span><span class="sxs-lookup"><span data-stu-id="08832-121">It is the default shell included within Ubuntu and other Linux distros, and in macOS.</span></span> <span data-ttu-id="08832-122">Пользователи в оболочку для выполнения скриптов или выполнять команды и средства для выполнения многих задач команды.</span><span class="sxs-lookup"><span data-stu-id="08832-122">Users type commands into a shell to execute scripts and/or run commands and tools to accomplish many tasks.</span></span>

## <a name="how-does-this-work"></a><span data-ttu-id="08832-123">Как это работает?</span><span class="sxs-lookup"><span data-stu-id="08832-123">How does this work?</span></span>
<span data-ttu-id="08832-124">Ознакомьтесь с нашей [блог](https://blogs.msdn.microsoft.com/wsl/) где мы подробно базовой технологии.</span><span class="sxs-lookup"><span data-stu-id="08832-124">Check out our [blog](https://blogs.msdn.microsoft.com/wsl/) where we go into detail about the underlying technology.</span></span>

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a><span data-ttu-id="08832-125">Почему бы использовать WSL, а не в Linux на виртуальной Машине?</span><span class="sxs-lookup"><span data-stu-id="08832-125">Why would I use WSL rather than Linux in a VM?</span></span>
<span data-ttu-id="08832-126">WSL требует меньше ресурсов (ЦП, памяти и хранилища), чем полный виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="08832-126">WSL requires fewer resources (CPU, memory, and storage) than a full virtual machine.</span></span> <span data-ttu-id="08832-127">WSL позволяет также для запуска программы командной строки Linux и приложений, рядом с приложениями командной строки, рабочего стола и магазина Windows, а также для доступа к файлам Windows из в Linux.</span><span class="sxs-lookup"><span data-stu-id="08832-127">WSL also allows you to run Linux command-line tools and apps alongside your Windows command-line, desktop and store apps, and to access your Windows files from within Linux.</span></span> <span data-ttu-id="08832-128">Это позволяет использовать приложения Windows и программы командной строки Linux на тот же набор файлов, при необходимости.</span><span class="sxs-lookup"><span data-stu-id="08832-128">This enables you to use Windows apps and Linux command-line tools on the same set of files if you wish.</span></span>

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a><span data-ttu-id="08832-129">Почему следует использовать, например, Ruby on Linux, а не в Windows?</span><span class="sxs-lookup"><span data-stu-id="08832-129">Why would I use, for example, Ruby on Linux instead of on Windows?</span></span>
<span data-ttu-id="08832-130">Некоторые кросс платформенные средства были созданы при условии, что среды, в котором они выполняются ведет себя как Linux.</span><span class="sxs-lookup"><span data-stu-id="08832-130">Some cross-platform tools were built assuming that the environment in which they run behaves like Linux.</span></span> <span data-ttu-id="08832-131">Некоторые средства Предположим, например, что они смогут получить доступ к очень длинные пути к файлам или что существуют определенные файлы и папки.</span><span class="sxs-lookup"><span data-stu-id="08832-131">For example, some tools assume that they are able to access very long file paths or that specific files/folders exist.</span></span> <span data-ttu-id="08832-132">Это часто создает проблемы в Windows, который часто ведет себя по-разному в среде Linux.</span><span class="sxs-lookup"><span data-stu-id="08832-132">This often causes problems on Windows which often behaves differently from Linux.</span></span>

<span data-ttu-id="08832-133">Многие языки, такие как Ruby и узел часто перенесена. они отлично, работать на Windows.</span><span class="sxs-lookup"><span data-stu-id="08832-133">Many languages like Ruby and node are often ported to, and run great, on Windows.</span></span> <span data-ttu-id="08832-134">Однако не все Ruby Gem или владельцев узлов или NPM библиотеки перенос их библиотеки для поддержки Windows и многие имеют зависимости специфичный для Linux.</span><span class="sxs-lookup"><span data-stu-id="08832-134">However, not all of the Ruby Gem or node/NPM library owners port their libraries to support Windows, and many have Linux-specific dependencies.</span></span> <span data-ttu-id="08832-135">Часто, это может привести в системах, созданных с помощью таких средств и библиотек, страдающие от сборки и иногда ошибки времени выполнения или нежелательного поведения в Windows.</span><span class="sxs-lookup"><span data-stu-id="08832-135">This can often result in systems built using such tools and libraries suffering from build and sometimes runtime errors or unwanted behaviors on Windows.</span></span>

<span data-ttu-id="08832-136">Это только некоторые из проблем, вызвавших появление большому числу пользователей, спросите у Майкрософт для улучшения средств командной строки Windows и что послужило нам для сотрудничества с помощью Canonical, чтобы включить собственный Bash и командной строки средств Linux под управлением Windows.</span><span class="sxs-lookup"><span data-stu-id="08832-136">These are just some of issues that caused many people to ask Microsoft to improve Windows’ command-line tools and what drove us to partner with Canonical to enable native Bash and Linux command-line tools to run on Windows.</span></span>

## <a name="what-does-this-mean-for-powershell"></a><span data-ttu-id="08832-137">Что это означает для PowerShell?</span><span class="sxs-lookup"><span data-stu-id="08832-137">What does this mean for PowerShell?</span></span>
<span data-ttu-id="08832-138">При работе с проектами с открытым исходным кодом, существует множество сценариев, где чрезвычайно полезным, помещающий в Bash из PowerShell prompt.</span><span class="sxs-lookup"><span data-stu-id="08832-138">While working with OSS projects, there are numerous scenarios where it’s immensely useful to drop into Bash from a PowerShell prompt.</span></span> <span data-ttu-id="08832-139">Поддержка bash дополняет и повышает параметра командной строки Windows, что позволяет использовать другие популярные технологии PowerShell и сообществе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="08832-139">Bash support is complementary and strengthens the value of the command-line on Windows, allowing PowerShell and the PowerShell community to leverage other popular technologies.</span></span>

<span data-ttu-id="08832-140">Узнайте больше о блоге группы разработчиков PowerShell-- [Bash для Windows: Почему это замечательно, и что это значит для PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span><span class="sxs-lookup"><span data-stu-id="08832-140">Read more on the PowerShell team blog -- [Bash for Windows: Why it’s awesome and what it means for PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span></span>

## <a name="can-i-run-all-linux-apps-in-wsl"></a><span data-ttu-id="08832-141">Можно ли запускать приложения под управлением Linux все в WSL?</span><span class="sxs-lookup"><span data-stu-id="08832-141">Can I run ALL Linux apps in WSL?</span></span>
<span data-ttu-id="08832-142">Нет!</span><span class="sxs-lookup"><span data-stu-id="08832-142">No!</span></span> <span data-ttu-id="08832-143">WSL — это средство, предназначенных для включения пользователей, которым требуется их выполнить Bash, а также описываются средства командной строки Linux на Windows.</span><span class="sxs-lookup"><span data-stu-id="08832-143">WSL is a tool aimed at enabling users who need them to run Bash and core Linux command-line tools on Windows.</span></span> 

<span data-ttu-id="08832-144">WSL **не** предназначены для поддержки настольных систем графического интерфейса пользователя или приложения (например Gnome, KDE т. д.)</span><span class="sxs-lookup"><span data-stu-id="08832-144">WSL does **not** aim to support GUI desktops or applications (e.g. Gnome, KDE, etc.)</span></span>  

<span data-ttu-id="08832-145">Кроме того, даже если вы сможете запускать многие популярные серверные приложения (например Redis), мы не рекомендуем WSL для размещения служб в рабочей среде — Корпорация Майкрософт предлагает различные решения для выполнения производственных рабочих нагрузок Linux в Azure, Hyper-V и Docker.</span><span class="sxs-lookup"><span data-stu-id="08832-145">Also, even though you will be able to run many popular server applications (e.g. Redis), we do not recommend WSL for hosting production services – Microsoft offers a variety of solutions for running production Linux workloads in Azure, Hyper-V, and Docker.</span></span> 

## <a name="what-windows-skus-is-wsl-included-in"></a><span data-ttu-id="08832-146">Какие SKU Windows включает WSL?</span><span class="sxs-lookup"><span data-stu-id="08832-146">What Windows SKUs is WSL included in?</span></span>
<span data-ttu-id="08832-147">Подсистема Windows для Linux можно найти в настольных систем Windows для Windows 10 Anniversary и Creators update или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="08832-147">Windows Subsystem for Linux is available on the desktop version of Windows for Windows 10 Anniversary and Creators update or later.</span></span>

<span data-ttu-id="08832-148">Начиная с Fall Creators update WSL будут доступны на сервер и настольных систем номера SKU для Windows.</span><span class="sxs-lookup"><span data-stu-id="08832-148">Beginning in the Fall Creators update WSL will be available on both the desktop and server SKUs of Windows.</span></span>

## <a name="what-processors-does-wsl-support"></a><span data-ttu-id="08832-149">Какой процессор поддерживает WSL?</span><span class="sxs-lookup"><span data-stu-id="08832-149">What processors does WSL support?</span></span>
<span data-ttu-id="08832-150">WSL поддерживает x64 и процессоров ARM.</span><span class="sxs-lookup"><span data-stu-id="08832-150">WSL supports x64 and ARM CPUs.</span></span>

## <a name="how-do-i-access-my-c-drive"></a><span data-ttu-id="08832-151">Как получить доступ к диске?</span><span class="sxs-lookup"><span data-stu-id="08832-151">How do I access my C: drive?</span></span>
<span data-ttu-id="08832-152">Точки подключения для жестких дисков на локальном компьютере автоматически создаются и обеспечивают легкий доступ к файловой системе Windows.</span><span class="sxs-lookup"><span data-stu-id="08832-152">Mount points for hard drives on the local machine are automatically created and provide easy access to the Windows filesystem.</span></span> 
 
<span data-ttu-id="08832-153">**/mnt/\<буква диска > /**</span><span class="sxs-lookup"><span data-stu-id="08832-153">**/mnt/\<drive letter>/**</span></span>
 
<span data-ttu-id="08832-154">Пример его использования `cd /mnt/c` для доступа к c:\\</span><span class="sxs-lookup"><span data-stu-id="08832-154">Example usage would be `cd /mnt/c` to access c:\\</span></span>

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a><span data-ttu-id="08832-155">Как использовать файл Windows с помощью приложения для Linux?</span><span class="sxs-lookup"><span data-stu-id="08832-155">How do I use a Windows file with a Linux app?</span></span>

<span data-ttu-id="08832-156">Одним из преимуществ WSL является возможность доступа к файлам с помощью приложения для Windows и Linux или средства.</span><span class="sxs-lookup"><span data-stu-id="08832-156">One of the benefits of WSL is being able to access your files via both Windows and Linux apps or tools.</span></span> 

<span data-ttu-id="08832-157">WSL подключает на компьютере, и фиксированным дискам `/mnt/<drive>` папку в вашей дистрибутивов Linux.</span><span class="sxs-lookup"><span data-stu-id="08832-157">WSL mounts your machine's fixed drives under the `/mnt/<drive>` folder in your Linux distros.</span></span> <span data-ttu-id="08832-158">Например ваш `C:` диск подключается в разделе `/mnt/c/`</span><span class="sxs-lookup"><span data-stu-id="08832-158">For example, your `C:` drive is mounted under `/mnt/c/`</span></span> 

<span data-ttu-id="08832-159">С помощью подключенных дисков, можно изменить код, например, `C:\dev\myproj\` с помощью [Visual Studio](https://visualstudio.microsoft.com/vs/) / или [VS Code](https://code.visualstudio.com/)и сборка и тестирование кода в Linux, доступ к тем же файлам через `\mnt\c\dev\myproj`.</span><span class="sxs-lookup"><span data-stu-id="08832-159">Using your mounted drives, you can edit code in, for example, `C:\dev\myproj\` using [Visual Studio](https://visualstudio.microsoft.com/vs/) / or [VS Code](https://code.visualstudio.com/), and build/test that code in Linux by accessing the same files via `\mnt\c\dev\myproj`.</span></span>

> <span data-ttu-id="08832-160">**ВАЖНОЕ ПРИМЕЧАНИЕ**: Одним из ключевых ограничение на использование WSL является не поддерживается напрямую доступ и изменение файлов в файловой системе дистрибутивов Linux, с помощью приложения Windows или средств.</span><span class="sxs-lookup"><span data-stu-id="08832-160">**IMPORTANT NOTE**: One of the key limitations of using WSL is that directly accessing/changing files in your Linux distros' filesystem using Windows apps or tools is not supported.</span></span> <span data-ttu-id="08832-161">Пример [Не изменяйте файлы Linux, с помощью инструментов и приложений Windows](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span><span class="sxs-lookup"><span data-stu-id="08832-161">See: [Do not change Linux files using Windows apps and tools](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span></span>

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a><span data-ttu-id="08832-162">Файлы на диске Linux, отличаются от подключенного диска Windows?</span><span class="sxs-lookup"><span data-stu-id="08832-162">Are files in the Linux drive different from the mounted Windows drive?</span></span>

1. <span data-ttu-id="08832-163">Файлы в корневом каталоге Linux (т. е. `/`) управляются WSL, который имитирует особое поведение Linux, включая, но не ограничиваясь ими:</span><span class="sxs-lookup"><span data-stu-id="08832-163">Files under the Linux root (i.e. `/`) are controlled by WSL which mimics Linux specific behavior, including but not limited to:</span></span>
   * <span data-ttu-id="08832-164">Файлы, которые содержат недопустимые символы имени файла Windows</span><span class="sxs-lookup"><span data-stu-id="08832-164">Files which contain invalid Windows filename characters</span></span>
   * <span data-ttu-id="08832-165">Символических ссылок, созданным для пользователей без прав администратора</span><span class="sxs-lookup"><span data-stu-id="08832-165">Symlinks created for non-admin users</span></span>
   * <span data-ttu-id="08832-166">Изменение атрибутов файла через chmod и сменить</span><span class="sxs-lookup"><span data-stu-id="08832-166">Changing file attributes through chmod and chown</span></span>
   * <span data-ttu-id="08832-167">Чувствительность к регистру, файл или папку</span><span class="sxs-lookup"><span data-stu-id="08832-167">File/folder case sensitivity</span></span>

2. <span data-ttu-id="08832-168">Файлы на подключенных дисках, настраиваемые в Windows и ведут себя следующим:</span><span class="sxs-lookup"><span data-stu-id="08832-168">Files in mounted drives are controlled by Windows and have the following behaviors:</span></span>
   * <span data-ttu-id="08832-169">Поддерживают учет регистра</span><span class="sxs-lookup"><span data-stu-id="08832-169">Support case sensitivity</span></span>
   * <span data-ttu-id="08832-170">Все разрешения лучше всего отражают разрешения Windows</span><span class="sxs-lookup"><span data-stu-id="08832-170">All permissions are set to best reflect the Windows permissions</span></span>

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a><span data-ttu-id="08832-171">Почему существует так много ошибок при запуске обновления apt-get?</span><span class="sxs-lookup"><span data-stu-id="08832-171">Why are there so many errors when I run apt-get upgrade?</span></span>
<span data-ttu-id="08832-172">Некоторые пакеты используют функции, которые мы еще не реализована.</span><span class="sxs-lookup"><span data-stu-id="08832-172">Some packages use features that we haven't implemented yet.</span></span> <span data-ttu-id="08832-173">`udev`, например, сейчас не поддерживается и приводит несколько `apt-get upgrade` ошибки.</span><span class="sxs-lookup"><span data-stu-id="08832-173">`udev`, for example, isn't supported yet and causes several `apt-get upgrade` errors.</span></span>

<span data-ttu-id="08832-174">Чтобы устранить проблемы, связанные с `udev`, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="08832-174">To fix issues related to `udev`, follow the following steps:</span></span>

1. <span data-ttu-id="08832-175">Написать следующую команду, чтобы `/usr/sbin/policy-rc.d` и сохраните изменения.</span><span class="sxs-lookup"><span data-stu-id="08832-175">Write the following to `/usr/sbin/policy-rc.d` and save your changes.</span></span>

    ```bash
    #!/bin/sh
    exit 101
    ```

2. <span data-ttu-id="08832-176">Добавить разрешения на выполнение `/usr/sbin/policy-rc.d`</span><span class="sxs-lookup"><span data-stu-id="08832-176">Add execute permissions to `/usr/sbin/policy-rc.d`</span></span>

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. <span data-ttu-id="08832-177">Выполните следующие команды</span><span class="sxs-lookup"><span data-stu-id="08832-177">Run the following commands</span></span>

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a><span data-ttu-id="08832-178">Как удалить дистрибутив WSL?</span><span class="sxs-lookup"><span data-stu-id="08832-178">How do I uninstall a WSL Distribution?</span></span>

<span data-ttu-id="08832-179">На сборки до версии 1709 (16299) откройте командную строку и выполните:</span><span class="sxs-lookup"><span data-stu-id="08832-179">On builds prior to 1709 (16299) open a command prompt and run:</span></span>
  ```batchfile
  lxrun /uninstall /full
  ```
  
<span data-ttu-id="08832-180">Дистрибутивы WSL, установленные из магазина можно удалить как любое другое приложение Windows, щелкнув плитку приложения и удалить или с помощью PowerShell, используя [ `Remove-AppxPackage` командлет](https://technet.microsoft.com/en-us/library/hh856038.aspx).</span><span class="sxs-lookup"><span data-stu-id="08832-180">WSL distributions installed from the store can be uninstalled like any other Windows app, by right-clicking on the app tile and clicking Uninstall, or via PowerShell using the [`Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx).</span></span>

## <a name="why-does-ping-generate-permission-denied-errors"></a><span data-ttu-id="08832-181">Почему ping создать отказано в разрешении ошибок?</span><span class="sxs-lookup"><span data-stu-id="08832-181">Why does ping generate permission denied errors?</span></span>
<span data-ttu-id="08832-182">В WSL сборки < 14926, ping необходимые WSL для выполнения через консоль с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="08832-182">In WSL builds < 14926, ping required WSL to run via an elevated Console.</span></span> <span data-ttu-id="08832-183">Эта проблема была исправлена в 14926 сборки и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="08832-183">This issue was fixed in Build 14926 and later.</span></span>

## <a name="how-do-i-run-an-openssh-server"></a><span data-ttu-id="08832-184">Как запустить сервер OpenSSH?</span><span class="sxs-lookup"><span data-stu-id="08832-184">How do I run an OpenSSH server?</span></span>
<span data-ttu-id="08832-185">Для запуска в WSL OpenSSH, необходимы права администратора в Windows.</span><span class="sxs-lookup"><span data-stu-id="08832-185">Administrator privileges in Windows are required to run OpenSSH in WSL.</span></span> <span data-ttu-id="08832-186">Чтобы запустить сервер OpenSSH, выполнять Bash на Ubuntu в Windows с правами администратора, или запустите bash.exe в командной строке CMD/PowerShell с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="08832-186">To run an OpenSSH server, run Bash on Ubuntu on Windows as an administrator, or run bash.exe from a CMD/PowerShell prompt with administrator privileges.</span></span>

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a><span data-ttu-id="08832-187">Почему я получаю «ошибка: 0x80040306» при попытке установить?</span><span class="sxs-lookup"><span data-stu-id="08832-187">Why do I get "Error: 0x80040306" when I try to install?</span></span>
<span data-ttu-id="08832-188">WSL не поддерживает запуск в прежнюю версию консоли.</span><span class="sxs-lookup"><span data-stu-id="08832-188">WSL does not support running in a legacy console.</span></span> <span data-ttu-id="08832-189">Чтобы отключить прежнюю версию консоли:</span><span class="sxs-lookup"><span data-stu-id="08832-189">To turn off legacy console:</span></span>

1. <span data-ttu-id="08832-190">Откройте WSL, PowerShell или Cmd</span><span class="sxs-lookup"><span data-stu-id="08832-190">Open WSL, PowerShell, or Cmd</span></span>
1. <span data-ttu-id="08832-191">Щелкните правой кнопкой мыши заголовок строки "->" Свойства "->" снимите флажок «Использовать прежнюю версию консоли»</span><span class="sxs-lookup"><span data-stu-id="08832-191">Right click title bar -> Properties -> Uncheck "Use legacy console"</span></span>
1. <span data-ttu-id="08832-192">Нажмите кнопку "ОК".</span><span class="sxs-lookup"><span data-stu-id="08832-192">Click OK</span></span>

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a><span data-ttu-id="08832-193">Почему я получаю «ошибка: 0x80040154» при выполнении bash.exe после обновления Windows?</span><span class="sxs-lookup"><span data-stu-id="08832-193">Why do I get "Error: 0x80040154" when I run bash.exe after upgrading Windows?</span></span>
<span data-ttu-id="08832-194">Функцию «Windows подсистемы для Linux» можно отключить во время обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="08832-194">The "Windows Subsystem for Linux" feature may be disabled during a Windows update.</span></span> <span data-ttu-id="08832-195">В этом случае необходимо снова включить функцию Windows.</span><span class="sxs-lookup"><span data-stu-id="08832-195">If this happens the Windows feature must be re-enabled.</span></span> <span data-ttu-id="08832-196">Инструкции для включения функции «Windows подсистемы для Linux» можно найти в [руководство по установке](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-guihttps://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui).</span><span class="sxs-lookup"><span data-stu-id="08832-196">Instructions for enabling the "Windows Subsystem for Linux" feature can be found in the [Installation Guide](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-guihttps://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui).</span></span>

## <a name="how-do-i-change-the-display-language-of-wsl"></a><span data-ttu-id="08832-197">Как изменить язык интерфейса WSL?</span><span class="sxs-lookup"><span data-stu-id="08832-197">How do I change the display language of WSL?</span></span>
<span data-ttu-id="08832-198">Установка WSL попытается автоматически изменить языковой стандарт Ubuntu в соответствии с языковой стандарт для текущей установки Windows.</span><span class="sxs-lookup"><span data-stu-id="08832-198">WSL install will try to automatically change the Ubuntu locale to match the locale of your Windows install.</span></span> <span data-ttu-id="08832-199">Если не хотите, чтобы это поведение, можно выполнить следующую команду, чтобы изменить языковой стандарт Ubuntu, после завершения установки.</span><span class="sxs-lookup"><span data-stu-id="08832-199">If you do not want this behavior you can run this command to change the Ubuntu locale after install completes.</span></span> <span data-ttu-id="08832-200">Необходимо будет перезапустить bash.exe это изменение вступило в силу.</span><span class="sxs-lookup"><span data-stu-id="08832-200">You will have to relaunch bash.exe for this change to take effect.</span></span>

<span data-ttu-id="08832-201">Ниже примере изменения языкового стандарта en-US:</span><span class="sxs-lookup"><span data-stu-id="08832-201">The below example changes to locale to en-US:</span></span>
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a><span data-ttu-id="08832-202">Почему не имеют доступа к Интернету из WSL?</span><span class="sxs-lookup"><span data-stu-id="08832-202">Why do I not have internet access from WSL?</span></span>
<span data-ttu-id="08832-203">Некоторые пользователи сообщали о проблемах с приложениями брандмауэров, блокировать доступ к Интернету в WSL.</span><span class="sxs-lookup"><span data-stu-id="08832-203">Some users have reported issues with specific firewall applications blocking internet access in WSL.</span></span> <span data-ttu-id="08832-204">Брандмауэры сообщил являются:</span><span class="sxs-lookup"><span data-stu-id="08832-204">The firewalls reported are:</span></span>

1. <span data-ttu-id="08832-205">Kaspersky</span><span class="sxs-lookup"><span data-stu-id="08832-205">Kaspersky</span></span>
1. <span data-ttu-id="08832-206">AVG</span><span class="sxs-lookup"><span data-stu-id="08832-206">AVG</span></span>
1. <span data-ttu-id="08832-207">Приложении avast</span><span class="sxs-lookup"><span data-stu-id="08832-207">Avast</span></span>

<span data-ttu-id="08832-208">В некоторых случаях отключение брандмауэра разрешает доступ к.</span><span class="sxs-lookup"><span data-stu-id="08832-208">In some cases turning off the firewall allows for access.</span></span> <span data-ttu-id="08832-209">В некоторых случаях простое наличие установлен брандмауэр проверяет блокировать доступ.</span><span class="sxs-lookup"><span data-stu-id="08832-209">In some cases simply having the firewall installed looks to block access.</span></span>

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a><span data-ttu-id="08832-210">Как открыть порт из WSL в Windows?</span><span class="sxs-lookup"><span data-stu-id="08832-210">How do I access a port from WSL in Windows?</span></span>
<span data-ttu-id="08832-211">WSL предоставляет IP-адрес Windows, как он работает под управлением Windows.</span><span class="sxs-lookup"><span data-stu-id="08832-211">WSL shares the IP address of Windows, as it is running on Windows.</span></span> <span data-ttu-id="08832-212">Таким образом вы может получить доступ к какие-либо порты на локальном узле. Например если имеется веб-содержимого на порту 1234, вы могли бы https://localhost:1234 в браузере Windows.</span><span class="sxs-lookup"><span data-stu-id="08832-212">As such you can access any ports on localhost e.g. if you had web content on port 1234 you could https://localhost:1234 into your Windows browser.</span></span>

## <a name="where-can-i-provide-feedback"></a><span data-ttu-id="08832-213">Где можно оставить отзыв?</span><span class="sxs-lookup"><span data-stu-id="08832-213">Where can I provide feedback?</span></span>

<span data-ttu-id="08832-214">Можно отправить свои отзывы и задавайте вопросы, через несколько каналов: Отзывы и вопросы следует направлять:</span><span class="sxs-lookup"><span data-stu-id="08832-214">You can share feedback and ask questions through multiple channels: Feedback and questions should be directed to:</span></span>
* <span data-ttu-id="08832-215">Наши [средство отслеживания вопросов GitHub](https://github.com/Microsoft/BashOnWindows/issues)</span><span class="sxs-lookup"><span data-stu-id="08832-215">Our [GitHub issue tracker](https://github.com/Microsoft/BashOnWindows/issues)</span></span>
* <span data-ttu-id="08832-216">Наши [командной строки портал UserVoice](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)</span><span class="sxs-lookup"><span data-stu-id="08832-216">Our [command-line UserVoice portal](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)</span></span>
* <span data-ttu-id="08832-217">Наши [блог группы командной строки](https://blogs.msdn.microsoft.com/commandline/)</span><span class="sxs-lookup"><span data-stu-id="08832-217">Our [command-line team blog](https://blogs.msdn.microsoft.com/commandline/)</span></span>
* <span data-ttu-id="08832-218">С помощью Twitter.</span><span class="sxs-lookup"><span data-stu-id="08832-218">Via Twitter.</span></span> <span data-ttu-id="08832-219">Следуйте [ @richturn_ms ](https://twitter.com/richturn_MS) в Twitter, чтобы узнать новости, обновления, и т.д.</span><span class="sxs-lookup"><span data-stu-id="08832-219">Please follow [@richturn_ms](https://twitter.com/richturn_MS) on Twitter to learn of news, updates, etc.</span></span>
