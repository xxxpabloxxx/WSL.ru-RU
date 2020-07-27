---
title: Вопросы и ответы
description: Часто задаваемые вопросы о подсистеме Windows для Linux.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, часто задаваемые вопросы
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.localizationpriority: high
ms.openlocfilehash: 8e3ebb44c139b5e7b8c25e8e813766b0107426dc
ms.sourcegitcommit: 97cc93f8e26391c09a31a4ab42c4b5e9d98d1c32
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/22/2020
ms.locfileid: "86948638"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a><span data-ttu-id="c9137-104">Часто задаваемые вопросы о подсистеме Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="c9137-104">Frequently Asked Questions about Windows Subsystem for Linux</span></span>

## <a name="what-is-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="c9137-105">Что такое подсистема Windows для Linux (WSL)?</span><span class="sxs-lookup"><span data-stu-id="c9137-105">What is Windows Subsystem for Linux (WSL)?</span></span>

<span data-ttu-id="c9137-106">Подсистема Windows для Linux (WSL) — это новый компонент Windows 10, который позволяет запускать собственные программы командной строки Linux непосредственно в Windows, как классические приложения для Windows и современные приложения Store.</span><span class="sxs-lookup"><span data-stu-id="c9137-106">The Windows Subsystem for Linux (WSL) is a new Windows 10 feature that enables you to run native Linux command-line tools directly on Windows, alongside your traditional Windows desktop and modern store apps.</span></span>

<span data-ttu-id="c9137-107">Чтобы узнать больше, ознакомьтесь со [страницей сведений](./about.md).</span><span class="sxs-lookup"><span data-stu-id="c9137-107">See the [about page](./about.md) for more details.</span></span>

## <a name="who-is-wsl-for"></a><span data-ttu-id="c9137-108">Для кого предназначена WSL?</span><span class="sxs-lookup"><span data-stu-id="c9137-108">Who is WSL for?</span></span>

<span data-ttu-id="c9137-109">В первую очередь, этот инструмент предназначен для разработчиков, особенно для веб-разработчиков и тех, кто работает над проектами с открытым кодом или участвует в них.</span><span class="sxs-lookup"><span data-stu-id="c9137-109">This is primarily a tool for developers -- especially web developers and those who work on or with open source projects.</span></span> <span data-ttu-id="c9137-110">Это позволяет всем, кто хочет использовать Bash, общие инструменты Linux (`sed`, `awk` и т. д.) и многие специализированные инструменты Linux (Ruby, Python и т. д.), пользоваться своей цепочкой инструментов в Windows.</span><span class="sxs-lookup"><span data-stu-id="c9137-110">This allows those who want/need to use Bash, common Linux tools (`sed`, `awk`, etc.) and many Linux-first tools (Ruby, Python, etc.) to use their toolchain on Windows.</span></span>

## <a name="what-can-i-do-with-wsl"></a><span data-ttu-id="c9137-111">Что можно сделать с помощью WSL?</span><span class="sxs-lookup"><span data-stu-id="c9137-111">What can I do with WSL?</span></span>

<span data-ttu-id="c9137-112">WSL предоставляет приложение Bash.exe, которое при запуске открывает консоль Windows, в которой выполняется оболочка Bash.</span><span class="sxs-lookup"><span data-stu-id="c9137-112">WSL provides an application called Bash.exe that, when started, opens a Windows console running the Bash shell.</span></span> <span data-ttu-id="c9137-113">С помощью Bash можно запускать программы командной строки и приложения Linux.</span><span class="sxs-lookup"><span data-stu-id="c9137-113">Using Bash, you can run command-line Linux tools and apps.</span></span> <span data-ttu-id="c9137-114">Например, введите `lsb_release -a` и нажмите клавишу ВВОД. Вы увидите сведения о текущем запущенном дистрибутиве Linux.</span><span class="sxs-lookup"><span data-stu-id="c9137-114">For example, type `lsb_release -a` and hit enter; you’ll see details of the Linux distro currently running:</span></span>

![Снимок экрана со сведениями о дистрибутиве](media/distro.png)

<span data-ttu-id="c9137-116">Вы можете также получить доступ к файловой системе локального компьютера из оболочки Bash в Linux — ваши локальные диски будут подключены в папке `/mnt`.</span><span class="sxs-lookup"><span data-stu-id="c9137-116">You can also access your local machine’s filesystem from within the Linux Bash shell – you’ll find your local drives mounted under the `/mnt` folder.</span></span> <span data-ttu-id="c9137-117">Например, диск `C:` подключается в `/mnt/c`.</span><span class="sxs-lookup"><span data-stu-id="c9137-117">For example, your `C:` drive is mounted under `/mnt/c`:</span></span>  

![Снимок экрана подключенного диска C](media/ls.png)

## <a name="could-you-describe-a-typical-development-workflow-that-incorporates-wsl"></a><span data-ttu-id="c9137-119">Опишите типичный рабочий процесс разработки с использованием WSL</span><span class="sxs-lookup"><span data-stu-id="c9137-119">Could you describe a typical development workflow that incorporates WSL?</span></span>

<span data-ttu-id="c9137-120">Подсистема WSL нацелена на аудиторию разработчиков и предназначена для использования в рамках внутреннего цикла разработки.</span><span class="sxs-lookup"><span data-stu-id="c9137-120">WSL targets a developer audience with the intent to be used as part of an inner development loop.</span></span> <span data-ttu-id="c9137-121">Предположим, Семен создает конвейер CI/CD (непрерывной интеграции и непрерывной поставки) и хочет сначала протестировать его на локальном компьютере (ноутбуке) перед развертыванием в облаке.</span><span class="sxs-lookup"><span data-stu-id="c9137-121">Let's say that Sam is creating a CI/CD pipeline (Continuous Integration & Continuous Delivery) and wants to test it first on a local machine (laptop) before deploying it to the cloud.</span></span> <span data-ttu-id="c9137-122">Семен может включить WSL (а также WSL 2, чтобы повысить скорость и производительность), а затем использовать подлинный экземпляр Linux Ubuntu на локальном компьютере (ноутбуке) с любыми командами Bash и инструментами по своему выбору.</span><span class="sxs-lookup"><span data-stu-id="c9137-122">Sam can enable WSL (& WSL 2 to improve speed and performance), and then use a genuine Linux Ubuntu instance locally (on the laptop) with whatever Bash commands and tools they prefer.</span></span> <span data-ttu-id="c9137-123">После проверки конвейера разработки в локальной среде Семен может отправить этот конвейер CI/CD в облако (т. е. в Azure), сделав его контейнером Docker и отправив в облачный экземпляр, где он будет выполняться на рабочей виртуальной машине Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="c9137-123">Once the development pipeline is verified locally, Sam can then push that CI/CD pipeline up to the cloud (ie Azure) by making it into a Docker container and pushing the container to a cloud instance where it runs on a production-ready Ubuntu VM.</span></span>

## <a name="what-is-bash"></a><span data-ttu-id="c9137-124">Что такое Bash?</span><span class="sxs-lookup"><span data-stu-id="c9137-124">What is Bash?</span></span>

<span data-ttu-id="c9137-125">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) — это популярная текстовая оболочка и язык команд.</span><span class="sxs-lookup"><span data-stu-id="c9137-125">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) is a popular text-based shell and command-language.</span></span> <span data-ttu-id="c9137-126">Это оболочка по умолчанию, входящая в состав Ubuntu и других дистрибутивов Linux, а также в macOS.</span><span class="sxs-lookup"><span data-stu-id="c9137-126">It is the default shell included within Ubuntu and other Linux distros, and in macOS.</span></span> <span data-ttu-id="c9137-127">Пользователи могут вводить команды в оболочке для выполнения сценариев и (или) команд и инструментов, чтобы выполнять множество задач.</span><span class="sxs-lookup"><span data-stu-id="c9137-127">Users type commands into a shell to execute scripts and/or run commands and tools to accomplish many tasks.</span></span>

## <a name="how-does-this-work"></a><span data-ttu-id="c9137-128">Как это работает?</span><span class="sxs-lookup"><span data-stu-id="c9137-128">How does this work?</span></span>

<span data-ttu-id="c9137-129">Ознакомьтесь с нашим [блогом](https://blogs.msdn.microsoft.com/wsl/), где мы подробно рассматриваем базовую технологию.</span><span class="sxs-lookup"><span data-stu-id="c9137-129">Check out our [blog](https://blogs.msdn.microsoft.com/wsl/) where we go into detail about the underlying technology.</span></span>

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a><span data-ttu-id="c9137-130">Зачем использовать WSL вместо Linux в виртуальной машине?</span><span class="sxs-lookup"><span data-stu-id="c9137-130">Why would I use WSL rather than Linux in a VM?</span></span>

<span data-ttu-id="c9137-131">WSL требует меньше ресурсов (ЦП, памяти и хранилища), чем полноценная виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="c9137-131">WSL requires fewer resources (CPU, memory, and storage) than a full virtual machine.</span></span> <span data-ttu-id="c9137-132">WSL также позволяет запускать программы командной строки и приложения Linux вместе с приложениями командной строки, классическими приложениями и приложениями Store для Windows, а также позволяет обращаться к файлам Windows в Linux.</span><span class="sxs-lookup"><span data-stu-id="c9137-132">WSL also allows you to run Linux command-line tools and apps alongside your Windows command-line, desktop and store apps, and to access your Windows files from within Linux.</span></span> <span data-ttu-id="c9137-133">Это позволяет использовать приложения для Windows и программы командной строки Linux для одного и того же набора файлов, если требуется.</span><span class="sxs-lookup"><span data-stu-id="c9137-133">This enables you to use Windows apps and Linux command-line tools on the same set of files if you wish.</span></span>

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a><span data-ttu-id="c9137-134">Зачем использовать, например, Ruby в Linux, а не Ruby в Windows?</span><span class="sxs-lookup"><span data-stu-id="c9137-134">Why would I use, for example, Ruby on Linux instead of on Windows?</span></span>

<span data-ttu-id="c9137-135">Некоторые кроссплатформенные инструменты были созданы, исходя из предположения, что среда, в которой они выполняются, работает как Linux.</span><span class="sxs-lookup"><span data-stu-id="c9137-135">Some cross-platform tools were built assuming that the environment in which they run behaves like Linux.</span></span> <span data-ttu-id="c9137-136">Например, некоторые инструменты предполагают, что имеют доступ к очень длинным путям к файлам или что существуют определенные файлы и папки.</span><span class="sxs-lookup"><span data-stu-id="c9137-136">For example, some tools assume that they are able to access very long file paths or that specific files/folders exist.</span></span> <span data-ttu-id="c9137-137">Это часто вызывает проблемы в среде Windows, которая нередко ведет себя иначе, чем в Linux.</span><span class="sxs-lookup"><span data-stu-id="c9137-137">This often causes problems on Windows which often behaves differently from Linux.</span></span>

<span data-ttu-id="c9137-138">Многие языки, такие как Ruby и Node, часто переносятся в Windows и работают отлично.</span><span class="sxs-lookup"><span data-stu-id="c9137-138">Many languages like Ruby and node are often ported to, and run great, on Windows.</span></span> <span data-ttu-id="c9137-139">Тем не менее, не все владельцы библиотек Ruby Gem или node/NPM переносят свои библиотеки для поддержки Windows, и многие из них имеют зависимости, относящиеся к Linux.</span><span class="sxs-lookup"><span data-stu-id="c9137-139">However, not all of the Ruby Gem or node/NPM library owners port their libraries to support Windows, and many have Linux-specific dependencies.</span></span> <span data-ttu-id="c9137-140">Это часто может привести к тому, что системы, созданные с помощью таких инструментов и библиотек, становятся подвержены ошибкам во время сборки, а иногда — во время выполнения, либо не работают в Windows требуемым образом.</span><span class="sxs-lookup"><span data-stu-id="c9137-140">This can often result in systems built using such tools and libraries suffering from build and sometimes runtime errors or unwanted behaviors on Windows.</span></span>

<span data-ttu-id="c9137-141">Это лишь часть проблем, из-за которых многие пользователи просят корпорацию Майкрософт улучшить программы командной строки Windows, а мы стали партнерами с Canonical, чтобы обеспечить выполнение собственных программ командной строки Linux и Bash в Windows.</span><span class="sxs-lookup"><span data-stu-id="c9137-141">These are just some of issues that caused many people to ask Microsoft to improve Windows’ command-line tools and what drove us to partner with Canonical to enable native Bash and Linux command-line tools to run on Windows.</span></span>

## <a name="what-does-this-mean-for-powershell"></a><span data-ttu-id="c9137-142">Что это означает для PowerShell?</span><span class="sxs-lookup"><span data-stu-id="c9137-142">What does this mean for PowerShell?</span></span>

<span data-ttu-id="c9137-143">При работе с проектами OSS существует множество сценариев, в которых чрезвычайно полезно перейти в Bash из командной строки PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c9137-143">While working with OSS projects, there are numerous scenarios where it’s immensely useful to drop into Bash from a PowerShell prompt.</span></span> <span data-ttu-id="c9137-144">Поддержка Bash дополняет и расширяет возможности командной строки в Windows, позволяя использовать PowerShell, а сообществу PowerShell — применять другие популярные технологии.</span><span class="sxs-lookup"><span data-stu-id="c9137-144">Bash support is complementary and strengthens the value of the command-line on Windows, allowing PowerShell and the PowerShell community to leverage other popular technologies.</span></span>

<span data-ttu-id="c9137-145">Дополнительные сведения см. в блоге группы разработчиков PowerShell: [Bash for Windows: Why it’s awesome and what it means for PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/) (Bash для Windows: почему это здорово и что это значит для PowerShell)</span><span class="sxs-lookup"><span data-stu-id="c9137-145">Read more on the PowerShell team blog -- [Bash for Windows: Why it’s awesome and what it means for PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span></span>

## <a name="can-i-run-all-linux-apps-in-wsl"></a><span data-ttu-id="c9137-146">Можно ли запускать ВСЕ приложения Linux в WSL?</span><span class="sxs-lookup"><span data-stu-id="c9137-146">Can I run ALL Linux apps in WSL?</span></span>

<span data-ttu-id="c9137-147">Нет.</span><span class="sxs-lookup"><span data-stu-id="c9137-147">No!</span></span> <span data-ttu-id="c9137-148">WSL — это инструмент, предназначенный для того, чтобы позволить пользователям запускать необходимые основные программы командной строки Linux и Bash в Windows.</span><span class="sxs-lookup"><span data-stu-id="c9137-148">WSL is a tool aimed at enabling users who need them to run Bash and core Linux command-line tools on Windows.</span></span>

<span data-ttu-id="c9137-149">WSL **не** предназначен для поддержки рабочих столов или приложений с графическим пользовательским интерфейсом (например, GNOME, KDE и т. д.).</span><span class="sxs-lookup"><span data-stu-id="c9137-149">WSL does **not** aim to support GUI desktops or applications (e.g. Gnome, KDE, etc.)</span></span>  

<span data-ttu-id="c9137-150">Кроме того, хотя вы сможете запускать многие популярные серверные приложения (например, Redis), мы не рекомендуем применять WSL для размещения рабочих служб. Корпорация Майкрософт предлагает ряд других решений для запуска производственных рабочих нагрузок Linux в Azure, Hyper-V и Docker.</span><span class="sxs-lookup"><span data-stu-id="c9137-150">Also, even though you will be able to run many popular server applications (e.g. Redis), we do not recommend WSL for hosting production services – Microsoft offers a variety of solutions for running production Linux workloads in Azure, Hyper-V, and Docker.</span></span> 

## <a name="what-windows-skus-is-wsl-included-in"></a><span data-ttu-id="c9137-151">Какие номера SKU Windows входят в WSL?</span><span class="sxs-lookup"><span data-stu-id="c9137-151">What Windows SKUs is WSL included in?</span></span>

<span data-ttu-id="c9137-152">Подсистема Windows для Linux доступна для юбилейного обновления Windows 10 и Windows 10 Creators Update для настольных компьютеров (а также для более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="c9137-152">Windows Subsystem for Linux is available on the desktop version of Windows for Windows 10 Anniversary and Creators update or later.</span></span>

<span data-ttu-id="c9137-153">Начиная с версии Fall Creators Update компонент WSL будет доступен как для номеров SKU настольных компьютеров, так и для номеров SKU серверных продуктов Windows.</span><span class="sxs-lookup"><span data-stu-id="c9137-153">Beginning in the Fall Creators update WSL will be available on both the desktop and server SKUs of Windows.</span></span>

## <a name="what-processors-does-wsl-support"></a><span data-ttu-id="c9137-154">Какие процессоры поддерживает WSL?</span><span class="sxs-lookup"><span data-stu-id="c9137-154">What processors does WSL support?</span></span>

<span data-ttu-id="c9137-155">WSL поддерживает процессоры x64 и ARM.</span><span class="sxs-lookup"><span data-stu-id="c9137-155">WSL supports x64 and ARM CPUs.</span></span>

## <a name="how-do-i-access-my-c-drive"></a><span data-ttu-id="c9137-156">Как получить доступ к моему диску C?</span><span class="sxs-lookup"><span data-stu-id="c9137-156">How do I access my C: drive?</span></span>

<span data-ttu-id="c9137-157">Точки подключения для жестких дисков на локальном компьютере создаются автоматически и обеспечивают простой доступ к файловой системе Windows.</span><span class="sxs-lookup"><span data-stu-id="c9137-157">Mount points for hard drives on the local machine are automatically created and provide easy access to the Windows filesystem.</span></span>

<span data-ttu-id="c9137-158">**/mnt/\<drive letter>/**</span><span class="sxs-lookup"><span data-stu-id="c9137-158">**/mnt/\<drive letter>/**</span></span>

<span data-ttu-id="c9137-159">Пример использования — команда `cd /mnt/c` для доступа к диску C:</span><span class="sxs-lookup"><span data-stu-id="c9137-159">Example usage would be `cd /mnt/c` to access c:</span></span>\

## <a name="how-do-i-set-up-git-credential-manager-how-do-i-use-my-windows-git-permissions-in-wsl"></a><span data-ttu-id="c9137-160">Как настроить диспетчер учетных данных Git?</span><span class="sxs-lookup"><span data-stu-id="c9137-160">How do I set up Git Credential Manager?</span></span> <span data-ttu-id="c9137-161">(Как использовать разрешения Windows Git в WSL?)</span><span class="sxs-lookup"><span data-stu-id="c9137-161">(How do I use my Windows Git permissions in WSL?)</span></span> 

<span data-ttu-id="c9137-162">Диспетчер учетных данных Git позволяет выполнять проверку подлинности на удаленном сервере Git, даже если используется сложная модель проверки подлинности, например Azure Active Directory или двухфакторная проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="c9137-162">Git Credential Manager enables you to authenticate a remote Git server, even if you have a complex authentication pattern like Azure Active Directory or two-factor authentication.</span></span> <span data-ttu-id="c9137-163">Диспетчер учетных данных Git интегрируется в поток проверки подлинности для таких служб, как GitHub, и после проверки подлинности в поставщике услуг размещения запрашивает новый маркер проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="c9137-163">Git Credential Manager integrates into the authentication flow for services like GitHub and, once you're authenticated to your hosting provider, requests a new authentication token.</span></span> <span data-ttu-id="c9137-164">Затем маркер сохраняется в диспетчере учетных данных Windows с поддержкой высокого уровня безопасности.</span><span class="sxs-lookup"><span data-stu-id="c9137-164">It then stores the token securely in the Windows Credential Manager.</span></span> <span data-ttu-id="c9137-165">В дальнейшем диспетчер учетных данных Git можно использовать для взаимодействия с поставщиком услуг размещения без повторной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="c9137-165">After the first time, you can use git to talk to your hosting provider without needing to re-authenticate.</span></span> <span data-ttu-id="c9137-166">Он просто обратится к маркеру в диспетчере учетных данных Windows.</span><span class="sxs-lookup"><span data-stu-id="c9137-166">It will just access the token in the Windows Credential Manager.</span></span>

<span data-ttu-id="c9137-167">Чтобы настроить диспетчер учетных данных Git для использования с дистрибутивом WSL, откройте дистрибутив и введите такую команду:</span><span class="sxs-lookup"><span data-stu-id="c9137-167">To set up Git Credential Manager for use with a WSL distribution, open your distribution and enter this command:</span></span>

```Bash
git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/libexec/git-core/git-credential-manager.exe"
```

<span data-ttu-id="c9137-168">Теперь при всех операциях Git, выполняемых в дистрибутиве WSL, будет использоваться диспетчер учетных данных.</span><span class="sxs-lookup"><span data-stu-id="c9137-168">Now any git operation you perform within your WSL distribution will use the credential manager.</span></span> <span data-ttu-id="c9137-169">Если у вас уже есть кэшированные учетные данные для узла, к ним будет выполняться доступ из диспетчера учетных данных.</span><span class="sxs-lookup"><span data-stu-id="c9137-169">If you already have credentials cached for a host, it will access them from the credential manager.</span></span> <span data-ttu-id="c9137-170">В противном случае отобразится диалоговое окно с запросом учетных данных, даже если вы работаете в консоли Linux.</span><span class="sxs-lookup"><span data-stu-id="c9137-170">If not, you'll receive a dialog response requesting your credentials, even if you're in a Linux console.</span></span>

<span data-ttu-id="c9137-171">Поддержка этих действий зависит от [взаимодействия между подсистемой Windows для Linux и собственно ОС Windows](https://docs.microsoft.com/windows/wsl/interop).</span><span class="sxs-lookup"><span data-stu-id="c9137-171">This support relies on the [interoperability between Windows Subsystem for Linux and Windows itself](https://docs.microsoft.com/windows/wsl/interop).</span></span>

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a><span data-ttu-id="c9137-172">Как использовать файл Windows в приложении Linux?</span><span class="sxs-lookup"><span data-stu-id="c9137-172">How do I use a Windows file with a Linux app?</span></span>

<span data-ttu-id="c9137-173">Одним из преимуществ WSL является возможность доступа к файлам с помощью приложений или инструментов Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="c9137-173">One of the benefits of WSL is being able to access your files via both Windows and Linux apps or tools.</span></span> 

<span data-ttu-id="c9137-174">WSL подключает несъемные диски вашего компьютера к папке `/mnt/<drive>` в ваших дистрибутивах Linux.</span><span class="sxs-lookup"><span data-stu-id="c9137-174">WSL mounts your machine's fixed drives under the `/mnt/<drive>` folder in your Linux distros.</span></span> <span data-ttu-id="c9137-175">Например, диск `C:` подключается в `/mnt/c/`.</span><span class="sxs-lookup"><span data-stu-id="c9137-175">For example, your `C:` drive is mounted under `/mnt/c/`</span></span>

<span data-ttu-id="c9137-176">Используя подключенные диски, можно изменить код, например, в `C:\dev\myproj\` с помощью [Visual Studio](https://visualstudio.microsoft.com/vs/) или [VS Code](https://code.visualstudio.com/), а также выполнить сборку или тестирование этого кода в Linux, воспользовавшись этими же файлами в `/mnt/c/dev/myproj`.</span><span class="sxs-lookup"><span data-stu-id="c9137-176">Using your mounted drives, you can edit code in, for example, `C:\dev\myproj\` using [Visual Studio](https://visualstudio.microsoft.com/vs/) / or [VS Code](https://code.visualstudio.com/), and build/test that code in Linux by accessing the same files via `/mnt/c/dev/myproj`.</span></span>

> <span data-ttu-id="c9137-177">**Важное примечание.** Одним из основных ограничений использования WSL является то, что непосредственный доступ и изменение файлов в файловой системе дистрибутивов Linux с помощью приложений или инструментов Windows не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c9137-177">**IMPORTANT NOTE**: One of the key limitations of using WSL is that directly accessing/changing files in your Linux distros' filesystem using Windows apps or tools is not supported.</span></span> <span data-ttu-id="c9137-178">См. раздел [Не изменяйте файлы Linux с помощью приложений и инструментов Windows](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span><span class="sxs-lookup"><span data-stu-id="c9137-178">See: [Do not change Linux files using Windows apps and tools](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span></span>

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a><span data-ttu-id="c9137-179">Отличаются ли файлы на диске Linux от файлов на подключенном диске Windows?</span><span class="sxs-lookup"><span data-stu-id="c9137-179">Are files in the Linux drive different from the mounted Windows drive?</span></span>

1. <span data-ttu-id="c9137-180">Файлы в корне Linux (т. е. `/`) контролируются подсистемой WSL, которая имитирует поведение Linux, включая, помимо прочего, следующее:</span><span class="sxs-lookup"><span data-stu-id="c9137-180">Files under the Linux root (i.e. `/`) are controlled by WSL which mimics Linux specific behavior, including but not limited to:</span></span>
   * <span data-ttu-id="c9137-181">файлы, содержащие в имени файла недопустимые знаки для Windows;</span><span class="sxs-lookup"><span data-stu-id="c9137-181">Files which contain invalid Windows filename characters</span></span>
   * <span data-ttu-id="c9137-182">символические ссылки, созданные для пользователей без прав администратора;</span><span class="sxs-lookup"><span data-stu-id="c9137-182">Symlinks created for non-admin users</span></span>
   * <span data-ttu-id="c9137-183">изменение атрибутов файла с помощью chmod и chown;</span><span class="sxs-lookup"><span data-stu-id="c9137-183">Changing file attributes through chmod and chown</span></span>
   * <span data-ttu-id="c9137-184">учет регистра в именах файлов и папок.</span><span class="sxs-lookup"><span data-stu-id="c9137-184">File/folder case sensitivity</span></span>

2. <span data-ttu-id="c9137-185">Файлы на подключенных дисках контролируются Windows и имеют следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="c9137-185">Files in mounted drives are controlled by Windows and have the following behaviors:</span></span>
   * <span data-ttu-id="c9137-186">поддерживают учет регистра;</span><span class="sxs-lookup"><span data-stu-id="c9137-186">Support case sensitivity</span></span>
   * <span data-ttu-id="c9137-187">все разрешения заданы для наилучшего отражения разрешений Windows.</span><span class="sxs-lookup"><span data-stu-id="c9137-187">All permissions are set to best reflect the Windows permissions</span></span>

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a><span data-ttu-id="c9137-188">Почему при выполнении apt-get upgrade возникает много ошибок?</span><span class="sxs-lookup"><span data-stu-id="c9137-188">Why are there so many errors when I run apt-get upgrade?</span></span>

<span data-ttu-id="c9137-189">Некоторые пакеты используют функции, которые еще не реализованы.</span><span class="sxs-lookup"><span data-stu-id="c9137-189">Some packages use features that we haven't implemented yet.</span></span> <span data-ttu-id="c9137-190">Например, `udev`пока не поддерживается и вызывает несколько ошибок `apt-get upgrade`.</span><span class="sxs-lookup"><span data-stu-id="c9137-190">`udev`, for example, isn't supported yet and causes several `apt-get upgrade` errors.</span></span>

<span data-ttu-id="c9137-191">Чтобы устранить проблемы, связанные с `udev`, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c9137-191">To fix issues related to `udev`, follow the following steps:</span></span>

1. <span data-ttu-id="c9137-192">Введите приведенный ниже код в `/usr/sbin/policy-rc.d` и сохраните изменения.</span><span class="sxs-lookup"><span data-stu-id="c9137-192">Write the following to `/usr/sbin/policy-rc.d` and save your changes.</span></span>

    ```bash
    #!/bin/sh
    exit 101
    ```

2. <span data-ttu-id="c9137-193">Добавьте разрешения на выполнение в `/usr/sbin/policy-rc.d`</span><span class="sxs-lookup"><span data-stu-id="c9137-193">Add execute permissions to `/usr/sbin/policy-rc.d`</span></span>

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
3. <span data-ttu-id="c9137-194">Выполните следующие команды.</span><span class="sxs-lookup"><span data-stu-id="c9137-194">Run the following commands</span></span>

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a><span data-ttu-id="c9137-195">Как удалить дистрибутив WSL?</span><span class="sxs-lookup"><span data-stu-id="c9137-195">How do I uninstall a WSL Distribution?</span></span>

<span data-ttu-id="c9137-196">В сборках, предшествующих сборке 1709 (16299), откройте командную строку и выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="c9137-196">On builds prior to 1709 (16299) open a command prompt and run:</span></span>

  ```batchfile
  lxrun /uninstall /full
  ```
  
<span data-ttu-id="c9137-197">Дистрибутивы WSL, установленные из Store, можно удалить как и любое другое приложение Windows. Для этого щелкните плитку приложения правой кнопкой мыши и выберите "Удалить". Можно также воспользоваться PowerShell и выполнить [`Remove-AppxPackage` командлет ](https://technet.microsoft.com/library/hh856038.aspx).</span><span class="sxs-lookup"><span data-stu-id="c9137-197">WSL distributions installed from the store can be uninstalled like any other Windows app, by right-clicking on the app tile and clicking Uninstall, or via PowerShell using the [`Remove-AppxPackage` cmdlet](https://technet.microsoft.com/library/hh856038.aspx).</span></span>

## <a name="why-does-ping-generate-permission-denied-errors"></a><span data-ttu-id="c9137-198">Почему проверка связи порождает создает ошибки "Отказ в разрешении"?</span><span class="sxs-lookup"><span data-stu-id="c9137-198">Why does ping generate permission denied errors?</span></span>

<span data-ttu-id="c9137-199">В сборках WSL, предшествующих сборке 14926, для проверки связи нужно запустить WSL из консоли с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="c9137-199">In WSL builds < 14926, ping required WSL to run via an elevated Console.</span></span> <span data-ttu-id="c9137-200">Эта проблема была устранена в сборке 14926 и более поздних сборках.</span><span class="sxs-lookup"><span data-stu-id="c9137-200">This issue was fixed in Build 14926 and later.</span></span>

## <a name="how-do-i-run-an-openssh-server"></a><span data-ttu-id="c9137-201">Как запустить сервер OpenSSH?</span><span class="sxs-lookup"><span data-stu-id="c9137-201">How do I run an OpenSSH server?</span></span>

<span data-ttu-id="c9137-202">Для запуска OpenSSH в WSL требуются привилегии администратора в Windows.</span><span class="sxs-lookup"><span data-stu-id="c9137-202">Administrator privileges in Windows are required to run OpenSSH in WSL.</span></span> <span data-ttu-id="c9137-203">Чтобы запустить сервер OpenSSH, запустите Bash для Ubuntu в Windows от имени администратора или запустите bash.exe из командной строки или сеанса PowerShell с привилегиями администратора.</span><span class="sxs-lookup"><span data-stu-id="c9137-203">To run an OpenSSH server, run Bash on Ubuntu on Windows as an administrator, or run bash.exe from a CMD/PowerShell prompt with administrator privileges.</span></span>

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a><span data-ttu-id="c9137-204">Почему при попытке установки появляется сообщение "Ошибка:0x80040306"?</span><span class="sxs-lookup"><span data-stu-id="c9137-204">Why do I get "Error: 0x80040306" when I try to install?</span></span>

<span data-ttu-id="c9137-205">WSL не поддерживает выполнение в устаревшей консоли.</span><span class="sxs-lookup"><span data-stu-id="c9137-205">WSL does not support running in a legacy console.</span></span> <span data-ttu-id="c9137-206">Чтобы отключить устаревшую консоль, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c9137-206">To turn off legacy console:</span></span>

1. <span data-ttu-id="c9137-207">Откройте WSL, PowerShell или командную строку.</span><span class="sxs-lookup"><span data-stu-id="c9137-207">Open WSL, PowerShell, or Cmd</span></span>
1. <span data-ttu-id="c9137-208">Щелкните правой кнопкой мыши строку заголовка и выберите "Свойства", затем снимите флажок "Использовать прежнюю версию консоли".</span><span class="sxs-lookup"><span data-stu-id="c9137-208">Right click title bar -> Properties -> Uncheck "Use legacy console"</span></span>
1. <span data-ttu-id="c9137-209">Нажмите кнопку "ОК".</span><span class="sxs-lookup"><span data-stu-id="c9137-209">Click OK</span></span>

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a><span data-ttu-id="c9137-210">Почему при запуске bash.exe после обновления Windows появляется сообщение "Ошибка: 0x80040154"?</span><span class="sxs-lookup"><span data-stu-id="c9137-210">Why do I get "Error: 0x80040154" when I run bash.exe after upgrading Windows?</span></span>

<span data-ttu-id="c9137-211">Компонент "Подсистема Windows для Linux" может быть отключен во время обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="c9137-211">The "Windows Subsystem for Linux" feature may be disabled during a Windows update.</span></span> <span data-ttu-id="c9137-212">В этом случае данную функцию Windows необходимо включить заново.</span><span class="sxs-lookup"><span data-stu-id="c9137-212">If this happens the Windows feature must be re-enabled.</span></span> <span data-ttu-id="c9137-213">Инструкции по включению компонента "Подсистема Windows для Linux" можно найти в [руководстве по установке](https://docs.microsoft.com/windows/wsl/install-win10#install-the-windows-subsystem-for-linux).</span><span class="sxs-lookup"><span data-stu-id="c9137-213">Instructions for enabling the "Windows Subsystem for Linux" feature can be found in the [Installation Guide](https://docs.microsoft.com/windows/wsl/install-win10#install-the-windows-subsystem-for-linux).</span></span>

## <a name="how-do-i-change-the-display-language-of-wsl"></a><span data-ttu-id="c9137-214">Как изменить язык интерфейса WSL?</span><span class="sxs-lookup"><span data-stu-id="c9137-214">How do I change the display language of WSL?</span></span>

<span data-ttu-id="c9137-215">Установщик WSL попытается автоматически изменить языковой стандарт Ubuntu в соответствии с языковым стандартом установки Windows.</span><span class="sxs-lookup"><span data-stu-id="c9137-215">WSL install will try to automatically change the Ubuntu locale to match the locale of your Windows install.</span></span> <span data-ttu-id="c9137-216">Если это нежелательно, можно выполнить приведенную ниже команду, чтобы изменить языковой стандарт Ubuntu после завершения установки.</span><span class="sxs-lookup"><span data-stu-id="c9137-216">If you do not want this behavior you can run this command to change the Ubuntu locale after install completes.</span></span> <span data-ttu-id="c9137-217">Чтобы это изменение вступило в силу, потребуется повторно запустить bash.exe.</span><span class="sxs-lookup"><span data-stu-id="c9137-217">You will have to relaunch bash.exe for this change to take effect.</span></span>

<span data-ttu-id="c9137-218">В приведенном ниже примере языковой стандарт изменяется на EN-US.</span><span class="sxs-lookup"><span data-stu-id="c9137-218">The below example changes to locale to en-US:</span></span>

```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a><span data-ttu-id="c9137-219">Почему у меня нет доступа к Интернету из WSL?</span><span class="sxs-lookup"><span data-stu-id="c9137-219">Why do I not have internet access from WSL?</span></span>

<span data-ttu-id="c9137-220">Некоторые пользователи сообщили о проблемах с определенными приложениями брандмауэра, блокирующими доступ к Интернету в WSL.</span><span class="sxs-lookup"><span data-stu-id="c9137-220">Some users have reported issues with specific firewall applications blocking internet access in WSL.</span></span> <span data-ttu-id="c9137-221">Сообщили о следующих брандмауэрах:</span><span class="sxs-lookup"><span data-stu-id="c9137-221">The firewalls reported are:</span></span>

1. <span data-ttu-id="c9137-222">Kaspersky;</span><span class="sxs-lookup"><span data-stu-id="c9137-222">Kaspersky</span></span>
1. <span data-ttu-id="c9137-223">AVG;</span><span class="sxs-lookup"><span data-stu-id="c9137-223">AVG</span></span>
1. <span data-ttu-id="c9137-224">Avast.</span><span class="sxs-lookup"><span data-stu-id="c9137-224">Avast</span></span>

<span data-ttu-id="c9137-225">В некоторых случаях отключение брандмауэра обеспечивает доступ.</span><span class="sxs-lookup"><span data-stu-id="c9137-225">In some cases turning off the firewall allows for access.</span></span> <span data-ttu-id="c9137-226">В некоторых случаях доступ блокируется просто при наличии установленного брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="c9137-226">In some cases simply having the firewall installed looks to block access.</span></span>

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a><span data-ttu-id="c9137-227">Как получить доступ к порту из WSL в Windows?</span><span class="sxs-lookup"><span data-stu-id="c9137-227">How do I access a port from WSL in Windows?</span></span>
<span data-ttu-id="c9137-228">WSL использует IP-адрес Windows, так как работает в Windows.</span><span class="sxs-lookup"><span data-stu-id="c9137-228">WSL shares the IP address of Windows, as it is running on Windows.</span></span> <span data-ttu-id="c9137-229">Поэтому вы можете получить доступ к любым портам на localhost. Например, если вы предоставляете веб-содержимое через порт 1234, то вы можете открыть адрес https://localhost:1234 в браузере для Windows.</span><span class="sxs-lookup"><span data-stu-id="c9137-229">As such you can access any ports on localhost e.g. if you had web content on port 1234 you could https://localhost:1234 into your Windows browser.</span></span>

## <a name="how-can-i-back-up-my-wsl-distros-or-move-them-from-one-drive-to-another"></a><span data-ttu-id="c9137-230">Как выполнить резервное копирование дистрибутивов WSL или переместить их с одного диска на другой?</span><span class="sxs-lookup"><span data-stu-id="c9137-230">How can I back up my WSL distros, or move them from one drive to another?</span></span>

<span data-ttu-id="c9137-231">Лучший способ резервного копирования или переноса дистрибутивов — использование команд импорта и экспорта, доступных в Windows версии 1809 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="c9137-231">The best way to backup or move your distros is via the export/import commands available in Windows Version 1809 and later.</span></span> <span data-ttu-id="c9137-232">Вы можете экспортировать весь дистрибутив в архив tarball с помощью команды `wsl --export`.</span><span class="sxs-lookup"><span data-stu-id="c9137-232">You can export your entire distribution to a tarball using the `wsl --export` command.</span></span> <span data-ttu-id="c9137-233">Затем этот дистрибутив можно импортировать обратно в WSL с помощью команды `wsl --import`, которая позволяет присвоить имя новому расположению на диске для импорта. Благодаря этому можно создавать резервные копии и сохранять состояния дистрибутивов WSL или переносить дистрибутивы.</span><span class="sxs-lookup"><span data-stu-id="c9137-233">You can then import this distro back into WSL using the `wsl --import` command, which can name a new drive location for the import, allowing you to backup and save states of (or move) your WSL distributions.</span></span> 

<span data-ttu-id="c9137-234">Обратите внимание на то, что традиционные службы резервного копирования, которые создают резервные копии файлов в папках AppData (например, программа архивации данных), не повредят файлы Linux.</span><span class="sxs-lookup"><span data-stu-id="c9137-234">Please note that traditional backup services that backup files in your Appdata folders (like Windows Backup) will not corrupt your Linux files.</span></span>

## <a name="where-can-i-provide-feedback"></a><span data-ttu-id="c9137-235">Куда можно отправить отзыв?</span><span class="sxs-lookup"><span data-stu-id="c9137-235">Where can I provide feedback?</span></span>

<span data-ttu-id="c9137-236">Вы можете оставлять свои отзывы и задавать вопросы, используя несколько каналов.</span><span class="sxs-lookup"><span data-stu-id="c9137-236">You can share feedback and ask questions through multiple channels.</span></span>

<span data-ttu-id="c9137-237">Если у вас возникли технические проблемы или вы хотите запросить новые функции, перейдите к нашему средству записи проблем GitHub:</span><span class="sxs-lookup"><span data-stu-id="c9137-237">If you have technical issues, or want to request new features please go to our Github issue tracker:</span></span>

* [<span data-ttu-id="c9137-238">Средство отслеживания проблем GitHub</span><span class="sxs-lookup"><span data-stu-id="c9137-238">GitHub issue tracker</span></span>](https://github.com/Microsoft/BashOnWindows/issues)

<span data-ttu-id="c9137-239">Если вы хотите оставаться в курсе последних новостей WSL, используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="c9137-239">If you'd like to stay up to date with the latest WSL news you can do so with:</span></span>

* <span data-ttu-id="c9137-240">в наш [блог команды разработчиков для командной строки](https://blogs.msdn.microsoft.com/commandline/);</span><span class="sxs-lookup"><span data-stu-id="c9137-240">Our [command-line team blog](https://blogs.msdn.microsoft.com/commandline/)</span></span>
* <span data-ttu-id="c9137-241">Twitter.</span><span class="sxs-lookup"><span data-stu-id="c9137-241">Twitter.</span></span> <span data-ttu-id="c9137-242">подпишитесь на [@craigaloewen](https://twitter.com/craigaloewen) в Twitter, чтобы получать новости, узнавать об обновлениях и т. д.</span><span class="sxs-lookup"><span data-stu-id="c9137-242">Please follow [@craigaloewen](https://twitter.com/craigaloewen) on Twitter to learn of news, updates, etc.</span></span>
