---
title: Вопросы и ответы
description: Часто задаваемые вопросы о подсистеме Windows для Linux.
keywords: Башонвиндовс, bash, WSL, Windows, виндовссубсистем, вопросы и ответы
author: taraj
ms.author: taraj
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.openlocfilehash: 2bbcec661146fcb570209fd895e6543657e98996
ms.sourcegitcommit: 939fe561d178454219adbee96c0ad3f768db2208
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2019
ms.locfileid: "67237385"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a><span data-ttu-id="54bb5-104">Часто задаваемые вопросы о подсистеме Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="54bb5-104">Frequently Asked Questions about Windows Subsystem for Linux</span></span>

## <a name="what-is-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="54bb5-105">Что такое подсистема Windows для Linux (WSL)?</span><span class="sxs-lookup"><span data-stu-id="54bb5-105">What is Windows Subsystem for Linux (WSL)?</span></span>
<span data-ttu-id="54bb5-106">Подсистема Windows для Linux (WSL) — это новая функция Windows 10, которая позволяет запускать собственные средства командной строки Linux непосредственно в Windows, наряду с традиционными приложениями Windows Desktop и современными магазинами.</span><span class="sxs-lookup"><span data-stu-id="54bb5-106">The Windows Subsystem for Linux (WSL) is a new Windows 10 feature that enables you to run native Linux command-line tools directly on Windows, alongside your traditional Windows desktop and modern store apps.</span></span>

<span data-ttu-id="54bb5-107">Дополнительные сведения см. на [странице о программе](./about.md) .</span><span class="sxs-lookup"><span data-stu-id="54bb5-107">See the [about page](./about.md) for more details.</span></span>

## <a name="who-is-wsl-for"></a><span data-ttu-id="54bb5-108">Кто WSL?</span><span class="sxs-lookup"><span data-stu-id="54bb5-108">Who is WSL for?</span></span>
<span data-ttu-id="54bb5-109">Это, в первую очередь, средство для разработчиков, особенно веб-разработчиков и тех, кто работает над проектами с открытым исходным кодом или с ними.</span><span class="sxs-lookup"><span data-stu-id="54bb5-109">This is primarily a tool for developers -- especially web developers and those who work on or with open source projects.</span></span> <span data-ttu-id="54bb5-110">Это позволяет пользователям, которые хотят использовать Bash, общие инструменты Linux (`sed`и `awk`т. д.) и многие инструменты Linux (Ruby, Python и т. д.), использовать их цепочки инструментов в Windows.</span><span class="sxs-lookup"><span data-stu-id="54bb5-110">This allows those who want/need to use Bash, common Linux tools (`sed`, `awk`, etc.) and many Linux-first tools (Ruby, Python, etc.) to use their toolchain on Windows.</span></span>

## <a name="what-can-i-do-with-wsl"></a><span data-ttu-id="54bb5-111">Что можно сделать с помощью WSL?</span><span class="sxs-lookup"><span data-stu-id="54bb5-111">What can I do with WSL?</span></span>
<span data-ttu-id="54bb5-112">WSL предоставляет приложение с именем bash. exe, которое при запуске открывает консоль Windows, на которой выполняется оболочка bash.</span><span class="sxs-lookup"><span data-stu-id="54bb5-112">WSL provides an application called Bash.exe that, when started, opens a Windows console running the Bash shell.</span></span> <span data-ttu-id="54bb5-113">С помощью bash можно запускать средства и приложения командной строки Linux.</span><span class="sxs-lookup"><span data-stu-id="54bb5-113">Using Bash, you can run command-line Linux tools and apps.</span></span> <span data-ttu-id="54bb5-114">Например, введите `lsb_release -a` и нажмите клавишу ВВОД. Вы увидите сведения о дистрибутив Linux в настоящее время:</span><span class="sxs-lookup"><span data-stu-id="54bb5-114">For example, type `lsb_release -a` and hit enter; you’ll see details of the Linux distro currently running:</span></span>

![Снимок экрана со сведениями о дистрибутив](media/distro.png)

<span data-ttu-id="54bb5-116">Вы также можете получить доступ к файловой системе локального компьютера из оболочки bash для Linux — вы найдете локальные диски, `/mnt` смонтированные в папке.</span><span class="sxs-lookup"><span data-stu-id="54bb5-116">You can also access your local machine’s filesystem from within the Linux Bash shell – you’ll find your local drives mounted under the `/mnt` folder.</span></span> <span data-ttu-id="54bb5-117">Например, `C:` диск монтируется в `/mnt/c`:</span><span class="sxs-lookup"><span data-stu-id="54bb5-117">For example, your `C:` drive is mounted under `/mnt/c`:</span></span>  

![Снимок экрана подключенного диска C](media/ls.png)

## <a name="what-is-bash"></a><span data-ttu-id="54bb5-119">Что такое bash?</span><span class="sxs-lookup"><span data-stu-id="54bb5-119">What is Bash?</span></span>
<span data-ttu-id="54bb5-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) — это популярная текстовая оболочка и язык команд.</span><span class="sxs-lookup"><span data-stu-id="54bb5-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) is a popular text-based shell and command-language.</span></span> <span data-ttu-id="54bb5-121">Это оболочка по умолчанию, входящая в Ubuntu и другие дистрибутивов Linux и в macOS.</span><span class="sxs-lookup"><span data-stu-id="54bb5-121">It is the default shell included within Ubuntu and other Linux distros, and in macOS.</span></span> <span data-ttu-id="54bb5-122">Пользователи могут вводить команды в оболочку для выполнения скриптов и/или выполнения команд и средств для выполнения многих задач.</span><span class="sxs-lookup"><span data-stu-id="54bb5-122">Users type commands into a shell to execute scripts and/or run commands and tools to accomplish many tasks.</span></span>

## <a name="how-does-this-work"></a><span data-ttu-id="54bb5-123">Как это работает?</span><span class="sxs-lookup"><span data-stu-id="54bb5-123">How does this work?</span></span>
<span data-ttu-id="54bb5-124">Ознакомьтесь с нашим [блогом](https://blogs.msdn.microsoft.com/wsl/) , где мы подробно рассмотрим базовую технологию.</span><span class="sxs-lookup"><span data-stu-id="54bb5-124">Check out our [blog](https://blogs.msdn.microsoft.com/wsl/) where we go into detail about the underlying technology.</span></span>

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a><span data-ttu-id="54bb5-125">Зачем использовать WSL вместо Linux в виртуальной машине?</span><span class="sxs-lookup"><span data-stu-id="54bb5-125">Why would I use WSL rather than Linux in a VM?</span></span>
<span data-ttu-id="54bb5-126">WSL требует меньше ресурсов (ЦП, памяти и хранилища), чем полная виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="54bb5-126">WSL requires fewer resources (CPU, memory, and storage) than a full virtual machine.</span></span> <span data-ttu-id="54bb5-127">WSL также позволяет запускать программные средства и приложения командной строки Linux вместе с приложениями командной строки Windows, настольным компьютером и магазином, а также для доступа к файлам Windows в Linux.</span><span class="sxs-lookup"><span data-stu-id="54bb5-127">WSL also allows you to run Linux command-line tools and apps alongside your Windows command-line, desktop and store apps, and to access your Windows files from within Linux.</span></span> <span data-ttu-id="54bb5-128">Это позволяет использовать приложения Windows и программы командной строки Linux на одном и том же наборе файлов при желании.</span><span class="sxs-lookup"><span data-stu-id="54bb5-128">This enables you to use Windows apps and Linux command-line tools on the same set of files if you wish.</span></span>

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a><span data-ttu-id="54bb5-129">Зачем использовать, например, Ruby в Linux вместо Windows?</span><span class="sxs-lookup"><span data-stu-id="54bb5-129">Why would I use, for example, Ruby on Linux instead of on Windows?</span></span>
<span data-ttu-id="54bb5-130">Некоторые межплатформенные средства были созданы при условии, что среда, в которой они работают, работает так же, как Linux.</span><span class="sxs-lookup"><span data-stu-id="54bb5-130">Some cross-platform tools were built assuming that the environment in which they run behaves like Linux.</span></span> <span data-ttu-id="54bb5-131">Например, некоторые средства предполагают, что они имеют доступ к очень длинным путям файлов или существуют определенные файлы и папки.</span><span class="sxs-lookup"><span data-stu-id="54bb5-131">For example, some tools assume that they are able to access very long file paths or that specific files/folders exist.</span></span> <span data-ttu-id="54bb5-132">Это часто вызывает проблемы в Windows, которые часто ведет себя иначе, чем в Linux.</span><span class="sxs-lookup"><span data-stu-id="54bb5-132">This often causes problems on Windows which often behaves differently from Linux.</span></span>

<span data-ttu-id="54bb5-133">Многие языки, такие как Ruby и Node, часто переносятся в Windows и работают отлично.</span><span class="sxs-lookup"><span data-stu-id="54bb5-133">Many languages like Ruby and node are often ported to, and run great, on Windows.</span></span> <span data-ttu-id="54bb5-134">Тем не менее, не все владельцы-драгоценные и NPMные библиотеки узлов и библиотек node/не заправляют свои библиотеки для поддержки Windows, и многие из них имеют зависимости, относящиеся к Linux.</span><span class="sxs-lookup"><span data-stu-id="54bb5-134">However, not all of the Ruby Gem or node/NPM library owners port their libraries to support Windows, and many have Linux-specific dependencies.</span></span> <span data-ttu-id="54bb5-135">Это часто может привести к тому, что системы, созданные с помощью таких средств и библиотек, низкий от сборки и иногда могут вызвать ошибки во время выполнения или нежелательные поведения в Windows.</span><span class="sxs-lookup"><span data-stu-id="54bb5-135">This can often result in systems built using such tools and libraries suffering from build and sometimes runtime errors or unwanted behaviors on Windows.</span></span>

<span data-ttu-id="54bb5-136">Это лишь часть проблем, из-за которых многие пользователи запрашивают у корпорации Майкрософт улучшения средств командной строки Windows, а также то, что привело к появлению канонических данных, чтобы обеспечить выполнение собственных программ Bash и командной строки Linux в Windows.</span><span class="sxs-lookup"><span data-stu-id="54bb5-136">These are just some of issues that caused many people to ask Microsoft to improve Windows’ command-line tools and what drove us to partner with Canonical to enable native Bash and Linux command-line tools to run on Windows.</span></span>

## <a name="what-does-this-mean-for-powershell"></a><span data-ttu-id="54bb5-137">Что это означает для PowerShell?</span><span class="sxs-lookup"><span data-stu-id="54bb5-137">What does this mean for PowerShell?</span></span>
<span data-ttu-id="54bb5-138">При работе с проектами OSS существует множество сценариев, в которых чрезвычайно полезно удалить bash из командной строки PowerShell.</span><span class="sxs-lookup"><span data-stu-id="54bb5-138">While working with OSS projects, there are numerous scenarios where it’s immensely useful to drop into Bash from a PowerShell prompt.</span></span> <span data-ttu-id="54bb5-139">Поддержка Bash дополняется и усиливает значение командной строки в Windows, позволяя PowerShell и сообществу PowerShell использовать другие популярные технологии.</span><span class="sxs-lookup"><span data-stu-id="54bb5-139">Bash support is complementary and strengthens the value of the command-line on Windows, allowing PowerShell and the PowerShell community to leverage other popular technologies.</span></span>

<span data-ttu-id="54bb5-140">Дополнительные сведения см. в блоге группы разработчиков PowerShell [— bash для Windows: Зачем это замечательно и что означает PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span><span class="sxs-lookup"><span data-stu-id="54bb5-140">Read more on the PowerShell team blog -- [Bash for Windows: Why it’s awesome and what it means for PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span></span>

## <a name="can-i-run-all-linux-apps-in-wsl"></a><span data-ttu-id="54bb5-141">Можно ли запускать все приложения Linux в WSL?</span><span class="sxs-lookup"><span data-stu-id="54bb5-141">Can I run ALL Linux apps in WSL?</span></span>
<span data-ttu-id="54bb5-142">Нет!</span><span class="sxs-lookup"><span data-stu-id="54bb5-142">No!</span></span> <span data-ttu-id="54bb5-143">WSL — это средство, предназначенное для предоставления пользователям, которым требуется запускать программы командной строки Bash и Core Linux в Windows.</span><span class="sxs-lookup"><span data-stu-id="54bb5-143">WSL is a tool aimed at enabling users who need them to run Bash and core Linux command-line tools on Windows.</span></span> 

<span data-ttu-id="54bb5-144">WSL **не** поддерживает рабочие столы и приложения графического пользовательского интерфейса (например, GNOME, KDE и т. д.).</span><span class="sxs-lookup"><span data-stu-id="54bb5-144">WSL does **not** aim to support GUI desktops or applications (e.g. Gnome, KDE, etc.)</span></span>  

<span data-ttu-id="54bb5-145">Кроме того, несмотря на то, что вы сможете запускать многие популярные серверные приложения (например, Redis), мы не рекомендуем WSL для размещения производственных служб — корпорация Майкрософт предлагает разнообразные решения для запуска рабочих нагрузок Linux в Azure, Hyper-V и DOCKER.</span><span class="sxs-lookup"><span data-stu-id="54bb5-145">Also, even though you will be able to run many popular server applications (e.g. Redis), we do not recommend WSL for hosting production services – Microsoft offers a variety of solutions for running production Linux workloads in Azure, Hyper-V, and Docker.</span></span> 

## <a name="what-windows-skus-is-wsl-included-in"></a><span data-ttu-id="54bb5-146">Какие номера SKU Windows входят в WSL?</span><span class="sxs-lookup"><span data-stu-id="54bb5-146">What Windows SKUs is WSL included in?</span></span>
<span data-ttu-id="54bb5-147">Подсистема Windows для Linux доступна на настольной версии Windows для Windows 10 годовщина и авторские обновления или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="54bb5-147">Windows Subsystem for Linux is available on the desktop version of Windows for Windows 10 Anniversary and Creators update or later.</span></span>

<span data-ttu-id="54bb5-148">Начиная с версии, авторы WSL Update будут доступны как для настольных, так и для серверных продуктов Windows.</span><span class="sxs-lookup"><span data-stu-id="54bb5-148">Beginning in the Fall Creators update WSL will be available on both the desktop and server SKUs of Windows.</span></span>

## <a name="what-processors-does-wsl-support"></a><span data-ttu-id="54bb5-149">Какие процессоры поддерживает WSL?</span><span class="sxs-lookup"><span data-stu-id="54bb5-149">What processors does WSL support?</span></span>
<span data-ttu-id="54bb5-150">WSL поддерживает процессоры x64 и ARM.</span><span class="sxs-lookup"><span data-stu-id="54bb5-150">WSL supports x64 and ARM CPUs.</span></span>

## <a name="how-do-i-access-my-c-drive"></a><span data-ttu-id="54bb5-151">Разделы справки получить доступ к диску C:</span><span class="sxs-lookup"><span data-stu-id="54bb5-151">How do I access my C: drive?</span></span>
<span data-ttu-id="54bb5-152">Точки подключения для жестких дисков на локальном компьютере создаются автоматически и обеспечивают простой доступ к файловой системе Windows.</span><span class="sxs-lookup"><span data-stu-id="54bb5-152">Mount points for hard drives on the local machine are automatically created and provide easy access to the Windows filesystem.</span></span> 
 
<span data-ttu-id="54bb5-153">**/МНТ/\<буква диска >/**</span><span class="sxs-lookup"><span data-stu-id="54bb5-153">**/mnt/\<drive letter>/**</span></span>
 
<span data-ttu-id="54bb5-154">Пример использования — `cd /mnt/c` доступ к c:</span><span class="sxs-lookup"><span data-stu-id="54bb5-154">Example usage would be `cd /mnt/c` to access c:</span></span>\

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a><span data-ttu-id="54bb5-155">Разделы справки использовать файл Windows с приложением Linux?</span><span class="sxs-lookup"><span data-stu-id="54bb5-155">How do I use a Windows file with a Linux app?</span></span>

<span data-ttu-id="54bb5-156">Одним из преимуществ WSL является возможность доступа к файлам с помощью приложений Windows и Linux или средств.</span><span class="sxs-lookup"><span data-stu-id="54bb5-156">One of the benefits of WSL is being able to access your files via both Windows and Linux apps or tools.</span></span> 

<span data-ttu-id="54bb5-157">WSL подключает фиксированные диски `/mnt/<drive>` вашего компьютера к папке в дистрибутивов Linux.</span><span class="sxs-lookup"><span data-stu-id="54bb5-157">WSL mounts your machine's fixed drives under the `/mnt/<drive>` folder in your Linux distros.</span></span> <span data-ttu-id="54bb5-158">Например, `C:` диск монтируется в`/mnt/c/`</span><span class="sxs-lookup"><span data-stu-id="54bb5-158">For example, your `C:` drive is mounted under `/mnt/c/`</span></span> 

<span data-ttu-id="54bb5-159">Используя подключенные диски, можно редактировать код в, например `C:\dev\myproj\` , с помощью [Visual Studio](https://visualstudio.microsoft.com/vs/) или [VS Code](https://code.visualstudio.com/), а также создавать и тестировать код в Linux, обращаясь к тем же файлам через `/mnt/c/dev/myproj`.</span><span class="sxs-lookup"><span data-stu-id="54bb5-159">Using your mounted drives, you can edit code in, for example, `C:\dev\myproj\` using [Visual Studio](https://visualstudio.microsoft.com/vs/) / or [VS Code](https://code.visualstudio.com/), and build/test that code in Linux by accessing the same files via `/mnt/c/dev/myproj`.</span></span>

> <span data-ttu-id="54bb5-160">**ВАЖНОЕ ЗАМЕЧАНИЕ**. Одним из основных ограничений использования WSL является то, что прямой доступ и изменение файлов в файловой системе Linux дистрибутивов с помощью приложений или средств Windows не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="54bb5-160">**IMPORTANT NOTE**: One of the key limitations of using WSL is that directly accessing/changing files in your Linux distros' filesystem using Windows apps or tools is not supported.</span></span> <span data-ttu-id="54bb5-161">Пример [Не изменяйте файлы Linux с помощью приложений и средств Windows](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span><span class="sxs-lookup"><span data-stu-id="54bb5-161">See: [Do not change Linux files using Windows apps and tools](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span></span>

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a><span data-ttu-id="54bb5-162">Отличаются ли файлы на диске Linux от подключенного диска Windows?</span><span class="sxs-lookup"><span data-stu-id="54bb5-162">Are files in the Linux drive different from the mounted Windows drive?</span></span>

1. <span data-ttu-id="54bb5-163">Файлы в корне Linux (т. `/`е.) контролируются WSL, который имитирует поведение, характерное для Linux, включая, помимо прочего, следующие:</span><span class="sxs-lookup"><span data-stu-id="54bb5-163">Files under the Linux root (i.e. `/`) are controlled by WSL which mimics Linux specific behavior, including but not limited to:</span></span>
   * <span data-ttu-id="54bb5-164">Файлы, содержащие недопустимые символы имени файла Windows</span><span class="sxs-lookup"><span data-stu-id="54bb5-164">Files which contain invalid Windows filename characters</span></span>
   * <span data-ttu-id="54bb5-165">Символических ссылок, созданные для пользователей без прав администратора</span><span class="sxs-lookup"><span data-stu-id="54bb5-165">Symlinks created for non-admin users</span></span>
   * <span data-ttu-id="54bb5-166">Изменение атрибутов файла с помощью chmod и човн</span><span class="sxs-lookup"><span data-stu-id="54bb5-166">Changing file attributes through chmod and chown</span></span>
   * <span data-ttu-id="54bb5-167">Чувствительность к регистру файлов и папок</span><span class="sxs-lookup"><span data-stu-id="54bb5-167">File/folder case sensitivity</span></span>

2. <span data-ttu-id="54bb5-168">Файлы на подключенных дисках управляются Windows и имеют следующие характеристики.</span><span class="sxs-lookup"><span data-stu-id="54bb5-168">Files in mounted drives are controlled by Windows and have the following behaviors:</span></span>
   * <span data-ttu-id="54bb5-169">Учитывать регистр в поддержке</span><span class="sxs-lookup"><span data-stu-id="54bb5-169">Support case sensitivity</span></span>
   * <span data-ttu-id="54bb5-170">Все разрешения настроены для наилучшего отражения разрешений Windows.</span><span class="sxs-lookup"><span data-stu-id="54bb5-170">All permissions are set to best reflect the Windows permissions</span></span>

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a><span data-ttu-id="54bb5-171">Почему при выполнении apt-get upgrade возникает много ошибок?</span><span class="sxs-lookup"><span data-stu-id="54bb5-171">Why are there so many errors when I run apt-get upgrade?</span></span>
<span data-ttu-id="54bb5-172">Некоторые пакеты используют функции, которые еще не реализованы.</span><span class="sxs-lookup"><span data-stu-id="54bb5-172">Some packages use features that we haven't implemented yet.</span></span> <span data-ttu-id="54bb5-173">`udev`, например, пока не поддерживается и вызывает несколько `apt-get upgrade` ошибок.</span><span class="sxs-lookup"><span data-stu-id="54bb5-173">`udev`, for example, isn't supported yet and causes several `apt-get upgrade` errors.</span></span>

<span data-ttu-id="54bb5-174">Чтобы устранить проблемы `udev`, связанные с, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="54bb5-174">To fix issues related to `udev`, follow the following steps:</span></span>

1. <span data-ttu-id="54bb5-175">Напишите следующее в `/usr/sbin/policy-rc.d` и сохраните изменения.</span><span class="sxs-lookup"><span data-stu-id="54bb5-175">Write the following to `/usr/sbin/policy-rc.d` and save your changes.</span></span>

    ```bash
    #!/bin/sh
    exit 101
    ```

2. <span data-ttu-id="54bb5-176">Добавить разрешения на выполнение в`/usr/sbin/policy-rc.d`</span><span class="sxs-lookup"><span data-stu-id="54bb5-176">Add execute permissions to `/usr/sbin/policy-rc.d`</span></span>

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. <span data-ttu-id="54bb5-177">Выполните следующие команды.</span><span class="sxs-lookup"><span data-stu-id="54bb5-177">Run the following commands</span></span>

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a><span data-ttu-id="54bb5-178">Разделы справки удалить дистрибутив WSL?</span><span class="sxs-lookup"><span data-stu-id="54bb5-178">How do I uninstall a WSL Distribution?</span></span>

<span data-ttu-id="54bb5-179">В сборках, предшествовавших 1709 (16299), откройте командную строку и выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="54bb5-179">On builds prior to 1709 (16299) open a command prompt and run:</span></span>
  ```batchfile
  lxrun /uninstall /full
  ```
  
<span data-ttu-id="54bb5-180">Дистрибутивы WSL, установленные из магазина, можно удалить, как и любое другое приложение Windows. для этого щелкните плитку приложения правой кнопкой мыши и выберите команду "Удалить" или через [ `Remove-AppxPackage` ](https://technet.microsoft.com/en-us/library/hh856038.aspx)PowerShell с помощью командлета.</span><span class="sxs-lookup"><span data-stu-id="54bb5-180">WSL distributions installed from the store can be uninstalled like any other Windows app, by right-clicking on the app tile and clicking Uninstall, or via PowerShell using the [`Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx).</span></span>

## <a name="why-does-ping-generate-permission-denied-errors"></a><span data-ttu-id="54bb5-181">Почему команда ping создает ошибки отказа в разрешении?</span><span class="sxs-lookup"><span data-stu-id="54bb5-181">Why does ping generate permission denied errors?</span></span>
<span data-ttu-id="54bb5-182">В WSL Builds < 14926, требуется проверка связи WSL для запуска через консоль с повышенными правами.</span><span class="sxs-lookup"><span data-stu-id="54bb5-182">In WSL builds < 14926, ping required WSL to run via an elevated Console.</span></span> <span data-ttu-id="54bb5-183">Эта проблема была исправлена в сборке 14926 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="54bb5-183">This issue was fixed in Build 14926 and later.</span></span>

## <a name="how-do-i-run-an-openssh-server"></a><span data-ttu-id="54bb5-184">Разделы справки запустить сервер OpenSSH?</span><span class="sxs-lookup"><span data-stu-id="54bb5-184">How do I run an OpenSSH server?</span></span>
<span data-ttu-id="54bb5-185">Для запуска OpenSSH в WSL требуются права администратора в Windows.</span><span class="sxs-lookup"><span data-stu-id="54bb5-185">Administrator privileges in Windows are required to run OpenSSH in WSL.</span></span> <span data-ttu-id="54bb5-186">Чтобы запустить сервер OpenSSH, запустите Bash в Ubuntu в Windows в качестве администратора или запустите bash. exe из командной строки CMD/PowerShell с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="54bb5-186">To run an OpenSSH server, run Bash on Ubuntu on Windows as an administrator, or run bash.exe from a CMD/PowerShell prompt with administrator privileges.</span></span>

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a><span data-ttu-id="54bb5-187">Почему выдается сообщение об ошибке: 0x80040306 "при попытке установить?</span><span class="sxs-lookup"><span data-stu-id="54bb5-187">Why do I get "Error: 0x80040306" when I try to install?</span></span>
<span data-ttu-id="54bb5-188">WSL не поддерживает выполнение в устаревшей консоли.</span><span class="sxs-lookup"><span data-stu-id="54bb5-188">WSL does not support running in a legacy console.</span></span> <span data-ttu-id="54bb5-189">Чтобы отключить устаревшую консоль, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="54bb5-189">To turn off legacy console:</span></span>

1. <span data-ttu-id="54bb5-190">Открытие WSL, PowerShell или cmd</span><span class="sxs-lookup"><span data-stu-id="54bb5-190">Open WSL, PowerShell, or Cmd</span></span>
1. <span data-ttu-id="54bb5-191">Щелкните правой кнопкой мыши заголовок окна, > Свойства — > снимите флажок "использовать устаревшую консоль".</span><span class="sxs-lookup"><span data-stu-id="54bb5-191">Right click title bar -> Properties -> Uncheck "Use legacy console"</span></span>
1. <span data-ttu-id="54bb5-192">Нажмите кнопку "ОК".</span><span class="sxs-lookup"><span data-stu-id="54bb5-192">Click OK</span></span>

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a><span data-ttu-id="54bb5-193">Почему выдается сообщение об ошибке: 0x80040154 при запуске bash. exe после обновления Windows?</span><span class="sxs-lookup"><span data-stu-id="54bb5-193">Why do I get "Error: 0x80040154" when I run bash.exe after upgrading Windows?</span></span>
<span data-ttu-id="54bb5-194">Функция "подсистема Windows для Linux" может быть отключена во время обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="54bb5-194">The "Windows Subsystem for Linux" feature may be disabled during a Windows update.</span></span> <span data-ttu-id="54bb5-195">В этом случае компонент Windows необходимо включить заново.</span><span class="sxs-lookup"><span data-stu-id="54bb5-195">If this happens the Windows feature must be re-enabled.</span></span> <span data-ttu-id="54bb5-196">Инструкции по включению функции "подсистема Windows для Linux" можно найти в разделе [руководства по установке](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui).</span><span class="sxs-lookup"><span data-stu-id="54bb5-196">Instructions for enabling the "Windows Subsystem for Linux" feature can be found in the [Installation Guide](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-guihttps://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui).</span></span>

## <a name="how-do-i-change-the-display-language-of-wsl"></a><span data-ttu-id="54bb5-197">Разделы справки изменить язык интерфейса WSL?</span><span class="sxs-lookup"><span data-stu-id="54bb5-197">How do I change the display language of WSL?</span></span>
<span data-ttu-id="54bb5-198">WSL Install попытается автоматически изменить языковой стандарт Ubuntu в соответствии с языковым стандартом установки Windows.</span><span class="sxs-lookup"><span data-stu-id="54bb5-198">WSL install will try to automatically change the Ubuntu locale to match the locale of your Windows install.</span></span> <span data-ttu-id="54bb5-199">Если это поведение нежелательно, можно выполнить эту команду, чтобы изменить языковой стандарт Ubuntu после завершения установки.</span><span class="sxs-lookup"><span data-stu-id="54bb5-199">If you do not want this behavior you can run this command to change the Ubuntu locale after install completes.</span></span> <span data-ttu-id="54bb5-200">Чтобы это изменение вступило в силу, необходимо повторно запустить Bash. exe.</span><span class="sxs-lookup"><span data-stu-id="54bb5-200">You will have to relaunch bash.exe for this change to take effect.</span></span>

<span data-ttu-id="54bb5-201">В приведенном ниже примере языковой стандарт меняется на EN-US:</span><span class="sxs-lookup"><span data-stu-id="54bb5-201">The below example changes to locale to en-US:</span></span>
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a><span data-ttu-id="54bb5-202">Почему у меня нет доступа к Интернету из WSL?</span><span class="sxs-lookup"><span data-stu-id="54bb5-202">Why do I not have internet access from WSL?</span></span>
<span data-ttu-id="54bb5-203">Некоторые пользователи сообщили о проблемах с определенными приложениями брандмауэра, блокирующими доступ к Интернету в WSL.</span><span class="sxs-lookup"><span data-stu-id="54bb5-203">Some users have reported issues with specific firewall applications blocking internet access in WSL.</span></span> <span data-ttu-id="54bb5-204">В отчет включены следующие брандмауэры:</span><span class="sxs-lookup"><span data-stu-id="54bb5-204">The firewalls reported are:</span></span>

1. <span data-ttu-id="54bb5-205">Kaspersky</span><span class="sxs-lookup"><span data-stu-id="54bb5-205">Kaspersky</span></span>
1. <span data-ttu-id="54bb5-206">ОБРАЩЕНИЯ</span><span class="sxs-lookup"><span data-stu-id="54bb5-206">AVG</span></span>
1. <span data-ttu-id="54bb5-207">аваст</span><span class="sxs-lookup"><span data-stu-id="54bb5-207">Avast</span></span>

<span data-ttu-id="54bb5-208">В некоторых случаях отключение брандмауэра разрешает доступ.</span><span class="sxs-lookup"><span data-stu-id="54bb5-208">In some cases turning off the firewall allows for access.</span></span> <span data-ttu-id="54bb5-209">В некоторых случаях просто, когда брандмауэр установлен, будет блокировать доступ.</span><span class="sxs-lookup"><span data-stu-id="54bb5-209">In some cases simply having the firewall installed looks to block access.</span></span>

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a><span data-ttu-id="54bb5-210">Разделы справки доступ к порту из WSL в Windows?</span><span class="sxs-lookup"><span data-stu-id="54bb5-210">How do I access a port from WSL in Windows?</span></span>
<span data-ttu-id="54bb5-211">WSL использует IP-адрес Windows, так как он работает в Windows.</span><span class="sxs-lookup"><span data-stu-id="54bb5-211">WSL shares the IP address of Windows, as it is running on Windows.</span></span> <span data-ttu-id="54bb5-212">Таким образом, вы можете получить доступ к любым портам на localhost, например, если у вас есть веб https://localhost:1234 -содержимое через порт 1234, можно в браузере Windows.</span><span class="sxs-lookup"><span data-stu-id="54bb5-212">As such you can access any ports on localhost e.g. if you had web content on port 1234 you could https://localhost:1234 into your Windows browser.</span></span>

## <a name="how-can-i-back-up-my-wsl-distros"></a><span data-ttu-id="54bb5-213">Как можно создать резервную копию WSL дистрибутивов?</span><span class="sxs-lookup"><span data-stu-id="54bb5-213">How can I back up my WSL distros?</span></span>

<span data-ttu-id="54bb5-214">Лучший способ резервного копирования дистрибутивов доступен в Windows версии 1809 и более поздних.</span><span class="sxs-lookup"><span data-stu-id="54bb5-214">The best way to backup your distros is available in Windows Version 1809 and later.</span></span> <span data-ttu-id="54bb5-215">Вы можете экспортировать полное распространение в tarball с помощью `wsl --export` команды.</span><span class="sxs-lookup"><span data-stu-id="54bb5-215">You can export your entire distribution to a tarball using the `wsl --export` command.</span></span> <span data-ttu-id="54bb5-216">Затем можно импортировать этот дистрибутив обратно в WSL с помощью `wsl --import` команды, что позволяет создавать резервные копии и сохранять состояния дистрибутивов WSL.</span><span class="sxs-lookup"><span data-stu-id="54bb5-216">You can then import this distro back into WSL using the `wsl --import` command, allowing you to backup and save states of your WSL distributions.</span></span> 

<span data-ttu-id="54bb5-217">Обратите внимание, что традиционные службы резервного копирования, которые файлы резервных копий в папках AppData (например, Windows Backup), не будут повредить файлы Linux.</span><span class="sxs-lookup"><span data-stu-id="54bb5-217">Please note that traditional backup services that backup files in your Appdata folders (like Windows Backup) will not corrupt your Linux files.</span></span> 



## <a name="where-can-i-provide-feedback"></a><span data-ttu-id="54bb5-218">Где можно отправить отзыв?</span><span class="sxs-lookup"><span data-stu-id="54bb5-218">Where can I provide feedback?</span></span>

<span data-ttu-id="54bb5-219">Вы можете поделиться отзывами и задать вопросы по нескольким каналам: Отзывы и вопросы должны быть направлены:</span><span class="sxs-lookup"><span data-stu-id="54bb5-219">You can share feedback and ask questions through multiple channels: Feedback and questions should be directed to:</span></span>
* <span data-ttu-id="54bb5-220">Наш [средство записи проблем GitHub](https://github.com/Microsoft/BashOnWindows/issues)</span><span class="sxs-lookup"><span data-stu-id="54bb5-220">Our [GitHub issue tracker](https://github.com/Microsoft/BashOnWindows/issues)</span></span>
* <span data-ttu-id="54bb5-221">Наш [портал командной строки UserVoice](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)</span><span class="sxs-lookup"><span data-stu-id="54bb5-221">Our [command-line UserVoice portal](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)</span></span>
* <span data-ttu-id="54bb5-222">[Блог команды командной строки](https://blogs.msdn.microsoft.com/commandline/)</span><span class="sxs-lookup"><span data-stu-id="54bb5-222">Our [command-line team blog](https://blogs.msdn.microsoft.com/commandline/)</span></span>
* <span data-ttu-id="54bb5-223">Через Twitter.</span><span class="sxs-lookup"><span data-stu-id="54bb5-223">Via Twitter.</span></span> <span data-ttu-id="54bb5-224">[@richturn_ms](https://twitter.com/richturn_MS) Ознакомьтесь с Twitter, чтобы узнать о новостях, обновлениях и т. д.</span><span class="sxs-lookup"><span data-stu-id="54bb5-224">Please follow [@richturn_ms](https://twitter.com/richturn_MS) on Twitter to learn of news, updates, etc.</span></span>
