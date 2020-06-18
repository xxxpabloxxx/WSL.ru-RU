---
title: Приступая к работе с Git в подсистеме Windows для Linux
description: Узнайте, как настроить Git для контроля версий в подсистеме Windows для Linux.
keywords: WSL, Windows, виндовссубсистем, GNU, Linux, bash, Git, GitHub, управление версиями
ms.date: 06/04/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: 550355ea77c97d68130c8d85e9aef2a6b49ffe63
ms.sourcegitcommit: eaceda3589b9bd777e0fead5ef33bb16060a55d2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "84978247"
---
# <a name="get-started-using-git-on-windows-subsystem-for-linux"></a><span data-ttu-id="83b6c-104">Приступая к работе с Git в подсистеме Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="83b6c-104">Get started using Git on Windows Subsystem for Linux</span></span>

<span data-ttu-id="83b6c-105">Git — это наиболее часто используемая система управления версиями.</span><span class="sxs-lookup"><span data-stu-id="83b6c-105">Git is the most commonly used version control system.</span></span> <span data-ttu-id="83b6c-106">С помощью Git вы можете отслеживание изменений, внесенных в файлы, поэтому у вас есть запись о том, что было сделано, и возможность вернуться к более ранним версиям файлов при необходимости.</span><span class="sxs-lookup"><span data-stu-id="83b6c-106">With Git, you can track changes you make to files, so you have a record of what has been done, and have the ability to revert to earlier versions of the files if needed.</span></span> <span data-ttu-id="83b6c-107">Кроме того, Git упрощает совместную работу, позволяя объединить изменения, внесенные несколькими людьми, в один источник.</span><span class="sxs-lookup"><span data-stu-id="83b6c-107">Git also makes collaboration easier, allowing changes by multiple people to all be merged into one source.</span></span>

## <a name="git-can-be-installed-on-windows-and-on-wsl"></a><span data-ttu-id="83b6c-108">Git можно установить в Windows и на WSL</span><span class="sxs-lookup"><span data-stu-id="83b6c-108">Git can be installed on Windows AND on WSL</span></span>

<span data-ttu-id="83b6c-109">Важно. при включении WSL и установке дистрибутива Linux устанавливается новая файловая система, отделенная от Windows NTFS C:\. диск на компьютере.</span><span class="sxs-lookup"><span data-stu-id="83b6c-109">An important consideration: when you enable WSL and install a Linux distribution, you are installing a new file system, separated from the Windows NTFS C:\ drive on your machine.</span></span> <span data-ttu-id="83b6c-110">В Linux буквы дисков не задаются.</span><span class="sxs-lookup"><span data-stu-id="83b6c-110">In Linux, drives are not given letters.</span></span> <span data-ttu-id="83b6c-111">Они получают точки подключения.</span><span class="sxs-lookup"><span data-stu-id="83b6c-111">They are given mount points.</span></span> <span data-ttu-id="83b6c-112">Корневой каталог файловой системы `/` — это точка подключения корневого раздела или папки в случае с WSL.</span><span class="sxs-lookup"><span data-stu-id="83b6c-112">The root of your file system `/` is the mount point of your root partition, or folder, in the case of WSL.</span></span> <span data-ttu-id="83b6c-113">Не все в разделе `/` — это один и тот же диск.</span><span class="sxs-lookup"><span data-stu-id="83b6c-113">Not everything under `/` is the same drive.</span></span> <span data-ttu-id="83b6c-114">Например, на моем ноутбуке я установил две версии Ubuntu (20,04 и 18,04), а также Debian.</span><span class="sxs-lookup"><span data-stu-id="83b6c-114">For example, on my laptop, I've installed two version of Ubuntu (20.04 and 18.04), as well as Debian.</span></span> <span data-ttu-id="83b6c-115">Если открыть эти дистрибутивы, выберите корневой каталог с командой `cd ~` , а затем введите команду `explorer.exe .` , откроется Проводник Windows и отобразится путь к каталогу для этого дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="83b6c-115">If I open those distributions, select the root directory with the command `cd ~`, and then enter the command `explorer.exe .`, Windows File Explorer will open and show me the directory path for that distribution.</span></span>

| <span data-ttu-id="83b6c-116">Дистрибутив Linux</span><span class="sxs-lookup"><span data-stu-id="83b6c-116">Linux distro</span></span> | <span data-ttu-id="83b6c-117">Путь Windows к домашней папке Access</span><span class="sxs-lookup"><span data-stu-id="83b6c-117">Windows Path to access home folder</span></span> |
| ----------- | ----------- |
| <span data-ttu-id="83b6c-118">Ubuntu 20.04</span><span class="sxs-lookup"><span data-stu-id="83b6c-118">Ubuntu 20.04</span></span> | `\\wsl$\Ubuntu-20.04\home\username` |
| <span data-ttu-id="83b6c-119">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="83b6c-119">Ubuntu 18.04</span></span> | `\\wsl$\Ubuntu-18.04\home\username` |
| <span data-ttu-id="83b6c-120">Debian</span><span class="sxs-lookup"><span data-stu-id="83b6c-120">Debian</span></span> | `\\wsl$\Debian\home\username` |
| <span data-ttu-id="83b6c-121">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="83b6c-121">Windows PowerShell</span></span> | `C:\Users\username` |

> [!TIP]
> <span data-ttu-id="83b6c-122">Если вы ищете доступ к каталогу файлов Windows из командной строки WSL Distribution, а не к `C:\Users\username` каталогу, то доступ к нему будет осуществляться с помощью `/mnt/c/Users/username` , поскольку дистрибутив Linux просматривает файловую систему Windows как подключенный диск.</span><span class="sxs-lookup"><span data-stu-id="83b6c-122">If you are seeking to access the Windows file directory from your WSL distribution command line, instead of `C:\Users\username`, the directory would be accessed using `/mnt/c/Users/username`, because the Linux distribution views your Windows file system as a mounted drive.</span></span>

<span data-ttu-id="83b6c-123">Необходимо установить Git в каждой файловой системе, с которой планируется использовать.</span><span class="sxs-lookup"><span data-stu-id="83b6c-123">You will need to install Git on each file system that you intend to use it with.</span></span>

![Отображение версий Git по дистрибутив](../media/git-versions.gif)

## <a name="installing-git"></a><span data-ttu-id="83b6c-125">Установка Git</span><span class="sxs-lookup"><span data-stu-id="83b6c-125">Installing Git</span></span>

<span data-ttu-id="83b6c-126">Git уже установлен с большей частью подсистемы Windows для дистрибутивов Linux, однако может потребоваться обновление до последней версии.</span><span class="sxs-lookup"><span data-stu-id="83b6c-126">Git comes already installed with most of the Windows Subsystem for Linux distributions, however, you may want to update to the latest version.</span></span> <span data-ttu-id="83b6c-127">Вам также потребуется настроить файл конфигурации Git.</span><span class="sxs-lookup"><span data-stu-id="83b6c-127">You also will need to set up your git config file.</span></span>

<span data-ttu-id="83b6c-128">Сведения об установке Git см. на сайте [скачивания Git для Linux](https://git-scm.com/download/linux) .</span><span class="sxs-lookup"><span data-stu-id="83b6c-128">To install Git, see the [Git Download for Linux](https://git-scm.com/download/linux) site.</span></span> <span data-ttu-id="83b6c-129">Каждый дистрибутив Linux имеет собственный диспетчер пакетов и команду install.</span><span class="sxs-lookup"><span data-stu-id="83b6c-129">Each Linux distribution has their own package manager and install command.</span></span>

<span data-ttu-id="83b6c-130">Для получения последней стабильной версии GIt в Ubuntu/Debian введите команду:</span><span class="sxs-lookup"><span data-stu-id="83b6c-130">For the latest stable GIt version in Ubuntu/Debian, enter the command:</span></span>

```bash
sudo apt-get install git
```

> [!NOTE]
> <span data-ttu-id="83b6c-131">Также может потребоваться [установить Git для Windows](https://git-scm.com/download/win) , если вы этого еще не сделали.</span><span class="sxs-lookup"><span data-stu-id="83b6c-131">You also may want to [install Git for Windows](https://git-scm.com/download/win) if you haven't already.</span></span>

## <a name="git-config-file-setup"></a><span data-ttu-id="83b6c-132">Настройка файла конфигурации Git</span><span class="sxs-lookup"><span data-stu-id="83b6c-132">Git config file setup</span></span>

<span data-ttu-id="83b6c-133">Чтобы настроить файл конфигурации Git, откройте командную строку, в которой вы работаете, и задайте свое имя с помощью этой команды (заменив "Ваше имя" на имя пользователя Git):</span><span class="sxs-lookup"><span data-stu-id="83b6c-133">To set up your Git config file, open a command line for the distribution you're working in and set your name with this command (replacing "Your Name" with your Git username):</span></span>

```bash
 `git config --global user.name "Your Name"`
```

<span data-ttu-id="83b6c-134">Задайте свою электронную почту с помощью этой команды (заменив " youremail@domain.com " на адрес электронной почты, используемый в вашей учетной записи Git):</span><span class="sxs-lookup"><span data-stu-id="83b6c-134">Set your email with this command (replacing "youremail@domain.com" with the email you use on your Git account):</span></span>

```bash
`git config --global user.email "youremail@domain.com"`
```

> [!TIP]
> <span data-ttu-id="83b6c-135">Если у вас еще нет учетной записи Git, вы можете [зарегистрироваться на сайте GitHub](https://github.com/join).</span><span class="sxs-lookup"><span data-stu-id="83b6c-135">If you don't yet have a Git account, you can [sign-up for one on GitHub](https://github.com/join).</span></span> <span data-ttu-id="83b6c-136">Если вы никогда не использовали Git, обратитесь к [руководствам по GitHub](https://guides.github.com/). Они помогут вам приступить к работе.</span><span class="sxs-lookup"><span data-stu-id="83b6c-136">If you've never worked with Git before, [GitHub Guides](https://guides.github.com/) can help you get started.</span></span> <span data-ttu-id="83b6c-137">Если вам нужно изменить файл конфигурации Git, это можно сделать с помощью встроенного текстового редактора, такого как nano: `nano ~/.gitconfig`.</span><span class="sxs-lookup"><span data-stu-id="83b6c-137">If you need to edit your git config, you can do so with a built-in text editor like nano: `nano ~/.gitconfig`.</span></span>

<span data-ttu-id="83b6c-138">Рекомендуется [защитить учетную запись с помощью двухфакторной проверки подлинности (2FA)](https://help.github.com/en/github/authenticating-to-github/securing-your-account-with-two-factor-authentication-2fa).</span><span class="sxs-lookup"><span data-stu-id="83b6c-138">We recommend that you [secure your account with two-factor authentication (2FA)](https://help.github.com/en/github/authenticating-to-github/securing-your-account-with-two-factor-authentication-2fa).</span></span>

## <a name="git-credential-manager-setup"></a><span data-ttu-id="83b6c-139">Установка диспетчера учетных данных Git</span><span class="sxs-lookup"><span data-stu-id="83b6c-139">Git Credential Manager setup</span></span>

<span data-ttu-id="83b6c-140">Диспетчер учетных данных Git позволяет выполнять проверку подлинности на удаленном сервере Git, даже если имеется сложная модель проверки подлинности, например двухфакторная проверка подлинности, Azure Active Directory или использование удаленных URL-адресов SSH, требующих пароля ключа SSH для каждой принудительной отправки Git.</span><span class="sxs-lookup"><span data-stu-id="83b6c-140">Git Credential Manager enables you to authenticate a remote Git server, even if you have a complex authentication pattern like two-factor authentication, Azure Active Directory, or using SSH remote URLs that require an SSH key password for every git push.</span></span> <span data-ttu-id="83b6c-141">Диспетчер учетных данных Git интегрируется в поток проверки подлинности для таких служб, как GitHub, и после проверки подлинности в поставщике услуг размещения запрашивает новый маркер проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="83b6c-141">Git Credential Manager integrates into the authentication flow for services like GitHub and, once you're authenticated to your hosting provider, requests a new authentication token.</span></span> <span data-ttu-id="83b6c-142">Затем маркер сохраняется в [диспетчере учетных данных Windows](https://support.microsoft.com/help/4026814/windows-accessing-credential-manager)в безопасном режиме.</span><span class="sxs-lookup"><span data-stu-id="83b6c-142">It then stores the token securely in the [Windows Credential Manager](https://support.microsoft.com/help/4026814/windows-accessing-credential-manager).</span></span> <span data-ttu-id="83b6c-143">В дальнейшем диспетчер учетных данных Git можно использовать для взаимодействия с поставщиком услуг размещения без повторной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="83b6c-143">After the first time, you can use git to talk to your hosting provider without needing to re-authenticate.</span></span> <span data-ttu-id="83b6c-144">Он просто обратится к маркеру в диспетчере учетных данных Windows.</span><span class="sxs-lookup"><span data-stu-id="83b6c-144">It will just access the token in the Windows Credential Manager.</span></span>

<span data-ttu-id="83b6c-145">Чтобы настроить диспетчер учетных данных Git для использования с дистрибутивом WSL, откройте дистрибутив и введите такую команду:</span><span class="sxs-lookup"><span data-stu-id="83b6c-145">To set up Git Credential Manager for use with a WSL distribution, open your distribution and enter this command:</span></span>

```Bash
git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/libexec/git-core/git-credential-manager.exe"
```

<span data-ttu-id="83b6c-146">Теперь при всех операциях Git, выполняемых в дистрибутиве WSL, будет использоваться диспетчер учетных данных.</span><span class="sxs-lookup"><span data-stu-id="83b6c-146">Now any git operation you perform within your WSL distribution will use the credential manager.</span></span> <span data-ttu-id="83b6c-147">Если у вас уже есть кэшированные учетные данные для узла, к ним будет выполняться доступ из диспетчера учетных данных.</span><span class="sxs-lookup"><span data-stu-id="83b6c-147">If you already have credentials cached for a host, it will access them from the credential manager.</span></span> <span data-ttu-id="83b6c-148">В противном случае отобразится диалоговое окно с запросом учетных данных, даже если вы работаете в консоли Linux.</span><span class="sxs-lookup"><span data-stu-id="83b6c-148">If not, you'll receive a dialog response requesting your credentials, even if you're in a Linux console.</span></span>

> [!NOTE]
> <span data-ttu-id="83b6c-149">Если вы используете ключ GPG для защиты подписывания кода, вам может потребоваться [связать ключ GPG с вашим адресом электронной почты GitHub](https://help.github.com/en/github/authenticating-to-github/associating-an-email-with-your-gpg-key).</span><span class="sxs-lookup"><span data-stu-id="83b6c-149">If you are using a GPG key for code signing security, you may need to [associate your GPG key with your GitHub email](https://help.github.com/en/github/authenticating-to-github/associating-an-email-with-your-gpg-key).</span></span>

## <a name="adding-a-git-ignore-file"></a><span data-ttu-id="83b6c-150">Добавление файла игнорирования Git</span><span class="sxs-lookup"><span data-stu-id="83b6c-150">Adding a Git Ignore file</span></span>

<span data-ttu-id="83b6c-151">Рекомендуется добавить gitignore- [файл](https://help.github.com/en/articles/ignoring-files) в проекты.</span><span class="sxs-lookup"><span data-stu-id="83b6c-151">We recommend adding a [.gitignore file](https://help.github.com/en/articles/ignoring-files) to your projects.</span></span> <span data-ttu-id="83b6c-152">GitHub предлагает [набор полезных шаблонов. gitignore](https://github.com/github/gitignore) с рекомендуемыми настройками файлов gitignore, организованными в соответствии с вашим вариантом использования.</span><span class="sxs-lookup"><span data-stu-id="83b6c-152">GitHub offers [a collection of useful .gitignore templates](https://github.com/github/gitignore) with recommended .gitignore file setups organized according to your use-case.</span></span> <span data-ttu-id="83b6c-153">Например, вот [шаблон gitignore по умолчанию GitHub для проекта Node.js](https://github.com/github/gitignore/blob/master/Node.gitignore).</span><span class="sxs-lookup"><span data-stu-id="83b6c-153">For example, here is [GitHub's default gitignore template for a Node.js project](https://github.com/github/gitignore/blob/master/Node.gitignore).</span></span>

<span data-ttu-id="83b6c-154">Если вы решили [создать репозиторий с помощью веб-сайта GitHub](https://help.github.com/articles/create-a-repo), доступны флажки для инициализации репозитория с файлом readme, gitignore-файлом, настроенным для конкретного типа проекта, и вариантами добавления лицензии, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="83b6c-154">If you choose to [create a new repo using the GitHub website](https://help.github.com/articles/create-a-repo), there are check boxes available to initialize your repo with a README file, .gitignore file set up for your specific project type, and options to add a license if you need one.</span></span>

## <a name="git-and-vs-code"></a><span data-ttu-id="83b6c-155">Git и VS Code</span><span class="sxs-lookup"><span data-stu-id="83b6c-155">Git and VS Code</span></span>

<span data-ttu-id="83b6c-156">Visual Studio Code поставляется со встроенной поддержкой Git, включая вкладку управления исходным кодом, в которой будут отображаться изменения и работать с различными командами Git.</span><span class="sxs-lookup"><span data-stu-id="83b6c-156">Visual Studio Code comes with built-in support for Git, including a source control tab that will show your changes and handle a variety of git commands for you.</span></span> <span data-ttu-id="83b6c-157">Дополнительные сведения о [поддержке Git VS Code](https://code.visualstudio.com/docs/editor/versioncontrol#_git-support).</span><span class="sxs-lookup"><span data-stu-id="83b6c-157">Learn more about [VS Code's Git support](https://code.visualstudio.com/docs/editor/versioncontrol#_git-support).</span></span>

## <a name="git-line-endings"></a><span data-ttu-id="83b6c-158">Окончания строк Git</span><span class="sxs-lookup"><span data-stu-id="83b6c-158">Git line endings</span></span>

<span data-ttu-id="83b6c-159">Если вы работаете с одной и той же папкой репозитория между Windows, WSL или контейнером, обязательно настройте согласованные окончания строк.</span><span class="sxs-lookup"><span data-stu-id="83b6c-159">If you are working with the same repository folder between Windows, WSL, or a container, be sure to set up consistent line endings.</span></span>

<span data-ttu-id="83b6c-160">Поскольку Windows и Linux используют разные окончания строк по умолчанию, Git может сообщить о большом количестве измененных файлов, которые не отличаются от их концов строк.</span><span class="sxs-lookup"><span data-stu-id="83b6c-160">Since Windows and Linux use different default line endings, Git may report a large number of modified files that have no differences aside from their line endings.</span></span> <span data-ttu-id="83b6c-161">Чтобы предотвратить это, можно отключить преобразование конца строки с помощью `.gitattributes` файла или глобально на стороне Windows.</span><span class="sxs-lookup"><span data-stu-id="83b6c-161">To prevent this from happening, you can disable line ending conversion using a `.gitattributes` file or globally on the Windows side.</span></span> <span data-ttu-id="83b6c-162">См. Этот [VS Code документ об устранении проблем с завершением строк Git](https://code.visualstudio.com/docs/remote/troubleshooting#_resolving-git-line-ending-issues-in-containers-resulting-in-many-modified-files).</span><span class="sxs-lookup"><span data-stu-id="83b6c-162">See this [VS Code doc about resolving Git line ending issues](https://code.visualstudio.com/docs/remote/troubleshooting#_resolving-git-line-ending-issues-in-containers-resulting-in-many-modified-files).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="83b6c-163">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="83b6c-163">Additional resources</span></span>

* [<span data-ttu-id="83b6c-164">WSL & VS Code</span><span class="sxs-lookup"><span data-stu-id="83b6c-164">WSL & VS Code</span></span>](./wsl-vscode.md)
* [<span data-ttu-id="83b6c-165">Учебная лаборатория GitHub: онлайн-курсы</span><span class="sxs-lookup"><span data-stu-id="83b6c-165">GitHub Learning Lab: Online courses</span></span>](https://lab.github.com/)
* [<span data-ttu-id="83b6c-166">Средство визуализации Git</span><span class="sxs-lookup"><span data-stu-id="83b6c-166">Git Visualization Tool</span></span>](http://git-school.github.io/visualizing-git/)
* [<span data-ttu-id="83b6c-167">Средства Git — хранилище учетных данных</span><span class="sxs-lookup"><span data-stu-id="83b6c-167">Git Tools - Credential Storage</span></span>](https://git-scm.com/book/it/v2/Git-Tools-Credential-Storage)
