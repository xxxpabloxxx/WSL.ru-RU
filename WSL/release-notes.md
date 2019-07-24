---
title: Заметки о выпуске для подсистемы Windows для Linux
description: Заметки о выпуске для подсистемы Windows для Linux.  Обновлено еженедельно.
keywords: Башонвиндовс, bash, WSL, Windows, подсистема Windows для Linux, виндовссубсистем, Ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: e2d9d5fc70c173e9b516ab7af01599b623b40b39
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/14/2019
ms.locfileid: "67042423"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="a848e-105">Заметки о выпуске для подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="a848e-105">Release Notes for Windows Subsystem for Linux</span></span>


## <a name="build-18917"></a><span data-ttu-id="a848e-106">Сборка 18917</span><span class="sxs-lookup"><span data-stu-id="a848e-106">Build 18917</span></span>
<span data-ttu-id="a848e-107">Общие сведения о Windows в сборке 18917 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span><span class="sxs-lookup"><span data-stu-id="a848e-107">For general Windows information on build 18917 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-108">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-108">WSL</span></span>
* <span data-ttu-id="a848e-109">WSL 2 теперь доступен!</span><span class="sxs-lookup"><span data-stu-id="a848e-109">WSL 2 is now available!</span></span> <span data-ttu-id="a848e-110">Дополнительные сведения см. в [блоге](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) .</span><span class="sxs-lookup"><span data-stu-id="a848e-110">Please see [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) for more details.</span></span>
* <span data-ttu-id="a848e-111">Исправление регрессии, при которой запуск процессов Windows через символических ссылок был некорректно выполнен [GH 3999]</span><span class="sxs-lookup"><span data-stu-id="a848e-111">Fix a regression where launching Windows processes via symlinks did not work correctly [GH 3999]</span></span>
* <span data-ttu-id="a848e-112">Добавьте WSL. exe--List--Verbose, WSL. exe--List--quiet и WSL. exe--Import--Version параметры в WSL. exe.</span><span class="sxs-lookup"><span data-stu-id="a848e-112">Add wsl.exe --list --verbose, wsl.exe --list --quiet, and wsl.exe --import --version options to wsl.exe</span></span>
* <span data-ttu-id="a848e-113">Добавление WSL. exe--параметр завершения работы</span><span class="sxs-lookup"><span data-stu-id="a848e-113">Add wsl.exe --shutdown option</span></span>
* <span data-ttu-id="a848e-114">План 9. Разрешить успешный запуск каталога для записи</span><span class="sxs-lookup"><span data-stu-id="a848e-114">Plan 9: Allow opening a directory for write to succeed</span></span>

## <a name="build-18890"></a><span data-ttu-id="a848e-115">Сборка 18890</span><span class="sxs-lookup"><span data-stu-id="a848e-115">Build 18890</span></span>
<span data-ttu-id="a848e-116">Общие сведения о Windows в сборке 18890 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span><span class="sxs-lookup"><span data-stu-id="a848e-116">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-117">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-117">WSL</span></span>
* <span data-ttu-id="a848e-118">Утечка неблокирующих сокетов [GH 2913]</span><span class="sxs-lookup"><span data-stu-id="a848e-118">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="a848e-119">Входные данные EOF в терминал могут блокировать последующие операции чтения [GH 3421]</span><span class="sxs-lookup"><span data-stu-id="a848e-119">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="a848e-120">Обновите заголовок resolv. conf, чтобы он ссылался на WSL. conf [рассматривается в GH 3928]</span><span class="sxs-lookup"><span data-stu-id="a848e-120">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="a848e-121">Взаимоблокировка в еполл удаление кода [GH 3922]</span><span class="sxs-lookup"><span data-stu-id="a848e-121">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="a848e-122">Обработку пробелов в аргументах для параметров--Import и – Export [GH 3932]</span><span class="sxs-lookup"><span data-stu-id="a848e-122">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="a848e-123">Расширение файлов mmap не работает должным образом [GH 3939]</span><span class="sxs-lookup"><span data-stu-id="a848e-123">Extending mmap’d files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="a848e-124">Устранение проблемы с \\ARM64 WSL $ Access не работает должным образом</span><span class="sxs-lookup"><span data-stu-id="a848e-124">Fix issue with ARM64 \\wsl$ access not working properly</span></span>
* <span data-ttu-id="a848e-125">Добавить Улучшенный значок по умолчанию для WSL. exe</span><span class="sxs-lookup"><span data-stu-id="a848e-125">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="a848e-126">Сборка 18342</span><span class="sxs-lookup"><span data-stu-id="a848e-126">Build 18342</span></span>
<span data-ttu-id="a848e-127">Общие сведения о Windows в сборке 18342 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span><span class="sxs-lookup"><span data-stu-id="a848e-127">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-128">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-128">WSL</span></span>
* <span data-ttu-id="a848e-129">Мы добавили возможность доступа пользователей к файлам Linux в WSL дистрибутив из Windows.</span><span class="sxs-lookup"><span data-stu-id="a848e-129">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="a848e-130">Доступ к этим файлам можно получить с помощью командной строки, а также приложений Windows, таких как проводник, VSCode и т. д., могут взаимодействовать с этими файлами.</span><span class="sxs-lookup"><span data-stu-id="a848e-130">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="a848e-131">Чтобы получить доступ к файлам, перейдите \\ \\по адресу WSL $\\< distro_name > или просмотрите список выполняющихся дистрибутивов, перейдя \\ \\по адресу WSL $</span><span class="sxs-lookup"><span data-stu-id="a848e-131">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="a848e-132">Добавление дополнительных тегов сведений о ЦП и исправление значений Cpus_allowed [_list] [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="a848e-132">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="a848e-133">Поддержка EXEC из потока, отличного от лидера [GH 3800]</span><span class="sxs-lookup"><span data-stu-id="a848e-133">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="a848e-134">Считать ошибки обновления конфигурации некритическими [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="a848e-134">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="a848e-135">Обновление бинфмт для правильной обработки смещений [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="a848e-135">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="a848e-136">Включение сопоставления сетевых дисков для плана 9 [GH 3854]</span><span class="sxs-lookup"><span data-stu-id="a848e-136">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="a848e-137">Поддержка Windows > Linux и Linux — > Преобразование пути Windows для подключений привязок</span><span class="sxs-lookup"><span data-stu-id="a848e-137">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="a848e-138">Создавать разделы только для чтения для сопоставлений файлов, открытых только для чтения</span><span class="sxs-lookup"><span data-stu-id="a848e-138">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="a848e-139">Сборка 18334</span><span class="sxs-lookup"><span data-stu-id="a848e-139">Build 18334</span></span>
<span data-ttu-id="a848e-140">Общие сведения о Windows в сборке 18334 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span><span class="sxs-lookup"><span data-stu-id="a848e-140">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-141">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-141">WSL</span></span>
* <span data-ttu-id="a848e-142">Перепроектирование способа сопоставления часового пояса Windows с часовым поясом Linux [GH 3747]</span><span class="sxs-lookup"><span data-stu-id="a848e-142">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="a848e-143">Устранение утечек памяти и добавление новых функций перевода строки [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="a848e-143">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="a848e-144">СИГКОНТ в среадграуп без потоков — это No-Op [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="a848e-144">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="a848e-145">Правильное отображение дескрипторов файлов Socket и еполл в/прок/Селф/ФД</span><span class="sxs-lookup"><span data-stu-id="a848e-145">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="a848e-146">Сборка 18305</span><span class="sxs-lookup"><span data-stu-id="a848e-146">Build 18305</span></span>
<span data-ttu-id="a848e-147">Общие сведения о Windows в сборке 18305 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span><span class="sxs-lookup"><span data-stu-id="a848e-147">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-148">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-148">WSL</span></span>
* <span data-ttu-id="a848e-149">псреадс теряет доступ к файлам, когда основной поток завершает работу [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="a848e-149">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="a848e-150">ТИОКСКТТИ должен игнорировать параметр Force, если он не требуется [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="a848e-150">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="a848e-151">усовершенствования командной строки WSL. exe и добавление функций импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="a848e-151">wsl.exe command line improvements and addition of import / export functionality.</span></span>
```
Usage: wsl.exe [Argument] [Options...] [CommandLine]

Arguments to run Linux binaries:

    If no command line is provided, wsl.exe launches the default shell.

    --exec, -e <CommandLine>
        Execute the specified command without using the default Linux shell.

    --
        Pass the remaining command line as is.

Options:
    --distribution, -d <DistributionName>
        Run the specified distribution.

    --user, -u <UserName>
        Run as the specified user.

Arguments to manage Windows Subsystem for Linux:

    --export <DistributionName> <FileName>
        Exports the distribution to a tar file.
        The filename can be - for standard output.

    --import <DistributionName> <InstallLocation> <FileName>
        Imports the specified tar file as a new distribution.
        The filename can be - for standard input.

    --list, -l [Options]
        Lists distributions.

        Options:
            --all
                List all distributions, including distributions that are currently
                being installed or uninstalled.

            --running
                List only distributions that are currently running.

    -setdefault, -s <DistributionName>
        Sets the distribution as the default.

    --terminate, -t <DistributionName>
        Terminates the distribution.

    --unregister <DistributionName>
        Unregisters the distribution.

    --upgrade <DistributionName>
        Upgrades the distribution to the WslFs file system format.

    --help
        Display usage information.
```

## <a name="build-18277"></a><span data-ttu-id="a848e-152">Сборка 18277</span><span class="sxs-lookup"><span data-stu-id="a848e-152">Build 18277</span></span>
<span data-ttu-id="a848e-153">Общие сведения о Windows в сборке 18277 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span><span class="sxs-lookup"><span data-stu-id="a848e-153">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-154">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-154">WSL</span></span>
* <span data-ttu-id="a848e-155">Исправлено сообщение об ошибке "не поддерживается такой интерфейс" в сборке 18272 [GH 3645]</span><span class="sxs-lookup"><span data-stu-id="a848e-155">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="a848e-156">Игнорировать флаг MNT_FORCE для umount syscall [GH 3605]</span><span class="sxs-lookup"><span data-stu-id="a848e-156">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="a848e-157">Переключение взаимодействия WSL для использования официального API Креатепсеудоконсоле</span><span class="sxs-lookup"><span data-stu-id="a848e-157">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="a848e-158">Не сохранять значение времени ожидания при перезапуске FUTEX_WAIT</span><span class="sxs-lookup"><span data-stu-id="a848e-158">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="a848e-159">Сборка 18272</span><span class="sxs-lookup"><span data-stu-id="a848e-159">Build 18272</span></span>
<span data-ttu-id="a848e-160">Общие сведения о Windows в сборке 18272 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span><span class="sxs-lookup"><span data-stu-id="a848e-160">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-161">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-161">WSL</span></span>
* <span data-ttu-id="a848e-162">**!** В этой сборке есть проблема, делающая WSL неработоспособной.</span><span class="sxs-lookup"><span data-stu-id="a848e-162">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="a848e-163">При попытке запустить распространение появится сообщение об ошибке "не поддерживается такой интерфейс".</span><span class="sxs-lookup"><span data-stu-id="a848e-163">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="a848e-164">Проблема исправлена и будет в рамках быстрой сборки программы предварительной оценки следующей недели.</span><span class="sxs-lookup"><span data-stu-id="a848e-164">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="a848e-165">Если вы установили эту сборку, вы можете вернуться к предыдущей сборке Windows с помощью команды "вернуться к предыдущей версии Windows 10" в окне "Параметры-> Обновление & безопасность-> Восстановление".</span><span class="sxs-lookup"><span data-stu-id="a848e-165">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="a848e-166">Сборка 18267</span><span class="sxs-lookup"><span data-stu-id="a848e-166">Build 18267</span></span>
<span data-ttu-id="a848e-167">Общие сведения о Windows в сборке 18267 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span><span class="sxs-lookup"><span data-stu-id="a848e-167">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-168">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-168">WSL</span></span>
* <span data-ttu-id="a848e-169">Устранение проблемы, когда процесс зомби может быть недоступен и оставаться неограниченным.</span><span class="sxs-lookup"><span data-stu-id="a848e-169">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="a848e-170">Вслрегистердистрибутион зависает, если сообщение об ошибке превышает максимальную длину [GH 3592]</span><span class="sxs-lookup"><span data-stu-id="a848e-170">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="a848e-171">Разрешить фсинк успешную установку файлов только для чтения в Дрвфс [GH 3556]</span><span class="sxs-lookup"><span data-stu-id="a848e-171">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="a848e-172">Перед созданием символических ссылок в [GH 3584] Убедитесь, что существуют каталоги "пере/сбин" и "%".</span><span class="sxs-lookup"><span data-stu-id="a848e-172">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="a848e-173">Добавлен механизм времени ожидания завершения экземпляра для экземпляров WSL.</span><span class="sxs-lookup"><span data-stu-id="a848e-173">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="a848e-174">В настоящее время время ожидания равно 15 секундам, то есть работа экземпляра будет прекращена через 15 секунд после завершения последнего процесса WSL.</span><span class="sxs-lookup"><span data-stu-id="a848e-174">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="a848e-175">Чтобы немедленно завершить распространение, используйте:</span><span class="sxs-lookup"><span data-stu-id="a848e-175">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="a848e-176">Сборка 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="a848e-176">Build 17763 (1809)</span></span>
<span data-ttu-id="a848e-177">Общие сведения о Windows в сборке 17763 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span><span class="sxs-lookup"><span data-stu-id="a848e-177">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-178">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-178">WSL</span></span>
* <span data-ttu-id="a848e-179">Проверка разрешений SetPriority syscall слишком ограничена для изменения того же приоритета потока [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="a848e-179">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="a848e-180">Убедитесь, что для времени загрузки используется Несмещенное время прерываний, чтобы избежать возврата отрицательных значений для clock_gettime (CLOCK_BOOTTIME) [GH 3434].</span><span class="sxs-lookup"><span data-stu-id="a848e-180">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="a848e-181">Обработать символических ссылок в интерпретаторе бинфмт WSL [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="a848e-181">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="a848e-182">Улучшенная обработка очистки дескриптора файла среадграуп.</span><span class="sxs-lookup"><span data-stu-id="a848e-182">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="a848e-183">Чтобы избежать переполнения, переключайте WSL на использование КекуеринтеррупттимепреЦисе вместо Кекуериперформанцекаунтер [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="a848e-183">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="a848e-184">Присоединение птраце может вызвать неправильное возвращаемое значение из системных вызовов [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="a848e-184">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="a848e-185">Устранение нескольких проблем, связанных с AF_UNIX [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="a848e-185">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="a848e-186">Устранение проблемы, которая может привести к сбою взаимодействия WSL, если длина текущего рабочего каталога меньше 5 символов [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="a848e-186">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="a848e-187">Предотвращение невозможности подключения замыкания на себя с несуществующими портами через одну вторую задержку (GH 3286)</span><span class="sxs-lookup"><span data-stu-id="a848e-187">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="a848e-188">Добавление файла заглушки/прок/СИС/ФС/филе-Макс [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="a848e-188">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="a848e-189">Более точные сведения об области IPV6.</span><span class="sxs-lookup"><span data-stu-id="a848e-189">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="a848e-190">Поддержка PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="a848e-190">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="a848e-191">Файловая система канала непреднамеренно очищает событие еполл, активируемое ребром [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="a848e-191">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="a848e-192">Исполняемый файл Win32, запущенный через NTFS символьную ссылку, не учитывает имя символьную ссылку [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="a848e-192">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="a848e-193">Улучшенная поддержка зомби [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="a848e-193">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="a848e-194">Добавление записей WSL. conf для управления поведением взаимодействия Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="a848e-194">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="a848e-195">Исправление для жетсоккнаме не всегда возвращает тип семейства сокетов UNIX [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="a848e-195">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="a848e-196">Добавление поддержки для ТИОКСТИ [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="a848e-196">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="a848e-197">Неблокирующие сокеты в процессе подключения должны возвращать ЕАГАИН для попыток записи [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="a848e-197">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="a848e-198">Поддержка взаимодействия на подключенных виртуальных жестких дисках [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="a848e-198">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="a848e-199">Устранение проблемы с проверкой разрешений в корневой папке [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="a848e-199">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="a848e-200">Ограниченная поддержка для клавиатуры TTY, КДГКБТИПЕ, КДГКБМОДЕ и КДСКБМОДЕ.</span><span class="sxs-lookup"><span data-stu-id="a848e-200">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="a848e-201">Приложения пользовательского интерфейса Windows должны выполняться, даже если они запущены в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="a848e-201">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="a848e-202">Add WSL-u или--User, параметр [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="a848e-202">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="a848e-203">Устранение проблем с запуском WSL при включении быстрого запуска [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="a848e-203">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="a848e-204">Сокеты Unix должны хранить отключенные одноранговые учетные данные [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="a848e-204">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="a848e-205">Неблокирующие сокеты Unix с неограниченным сбоем с ЕАГАИН [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="a848e-205">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="a848e-206">Case = Off — новый тип подключения дрвфс по умолчанию [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="a848e-206">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="a848e-207">Дополнительные сведения см. в [блоге](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) .</span><span class="sxs-lookup"><span data-stu-id="a848e-207">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="a848e-208">Добавьте вслконфиг/терминате, чтобы прерывать выполнение распределений.</span><span class="sxs-lookup"><span data-stu-id="a848e-208">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="a848e-209">Устранена проблема с записями в контекстном меню оболочки WSL, которые неправильно обработают пути с пробелами.</span><span class="sxs-lookup"><span data-stu-id="a848e-209">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="a848e-210">Предоставить учет регистра в каталоге в качестве расширенного атрибута</span><span class="sxs-lookup"><span data-stu-id="a848e-210">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="a848e-211">ARM64 Эмуляция операций обслуживания кэша.</span><span class="sxs-lookup"><span data-stu-id="a848e-211">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="a848e-212">Устраните [проблему DotNet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="a848e-212">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="a848e-213">Дрвфс: только escape-символы в закрытом диапазоне, которые соответствуют escape-символу.</span><span class="sxs-lookup"><span data-stu-id="a848e-213">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="a848e-214">Устранение ошибки при проверке длины интерпретатора анализатора ELF [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="a848e-214">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="a848e-215">WSL абсолютные таймеры с временем в прошлом не срабатывают [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="a848e-215">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="a848e-216">Убедитесь, что вновь созданные точки повторного анализа указаны в родительском каталоге.</span><span class="sxs-lookup"><span data-stu-id="a848e-216">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="a848e-217">Атомарное создание каталогов с учетом регистра в Дрвфс.</span><span class="sxs-lookup"><span data-stu-id="a848e-217">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="a848e-218">Исправлена дополнительная проблема, когда многопоточные операции могут возвращать ЕНОЕНТ, даже если файл существует.</span><span class="sxs-lookup"><span data-stu-id="a848e-218">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="a848e-219">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="a848e-219">[GH 2712]</span></span>
* <span data-ttu-id="a848e-220">Исправлена ошибка запуска WSL при включенном УМЦИ.</span><span class="sxs-lookup"><span data-stu-id="a848e-220">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="a848e-221">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="a848e-221">[GH 3020]</span></span>
* <span data-ttu-id="a848e-222">Добавьте контекстное меню обозревателя, чтобы запустить WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="a848e-222">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="a848e-223">Чтобы использовать, удерживайте клавишу Shift и щелкните правой кнопкой мыши в окне проводника.</span><span class="sxs-lookup"><span data-stu-id="a848e-223">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="a848e-224">Устранение неблокирующего поведения сокета UNIX [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="a848e-224">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="a848e-225">Исправьте команду НЕТЛИНК в соответствии с отчетом в GH 2026.</span><span class="sxs-lookup"><span data-stu-id="a848e-225">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="a848e-226">Добавлена поддержка флагов распространения подключения [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="a848e-226">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="a848e-227">Устранена проблема с усечением, которая не вызывает инотифи событий [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="a848e-227">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="a848e-228">Добавьте параметр--exec для WSL. exe, чтобы вызвать один двоичный файл без оболочки.</span><span class="sxs-lookup"><span data-stu-id="a848e-228">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="a848e-229">Добавьте параметр--Distribution для WSL. exe, чтобы выбрать конкретный дистрибутив.</span><span class="sxs-lookup"><span data-stu-id="a848e-229">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="a848e-230">Ограниченная поддержка дмесг.</span><span class="sxs-lookup"><span data-stu-id="a848e-230">Limited support for dmesg.</span></span> <span data-ttu-id="a848e-231">Теперь приложения могут входить в дмесг.</span><span class="sxs-lookup"><span data-stu-id="a848e-231">Applications can now log to dmesg.</span></span> <span data-ttu-id="a848e-232">Драйвер WSL записывает ограниченные сведения в дмесг.</span><span class="sxs-lookup"><span data-stu-id="a848e-232">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="a848e-233">В будущем это можно продлить, донести другие сведения и диагностику из драйвера.</span><span class="sxs-lookup"><span data-stu-id="a848e-233">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="a848e-234">Примечание. в настоящее время дмесг поддерживается через `/dev/kmsg` интерфейс устройства.</span><span class="sxs-lookup"><span data-stu-id="a848e-234">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="a848e-235">`syslog`интерфейс syscall пока не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a848e-235">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="a848e-236">И, таким образом, некоторые `dmesg` параметры командной строки, такие как `-S`, `-C` не работают.</span><span class="sxs-lookup"><span data-stu-id="a848e-236">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="a848e-237">Изменение значения GID и режима по умолчанию для последовательных устройств на соответствие Native [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="a848e-237">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="a848e-238">Дрвфс теперь поддерживает расширенные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="a848e-238">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="a848e-239">Примечание. Дрвфс имеет некоторые ограничения на имена расширенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="a848e-239">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="a848e-240">Некоторые символы (например, "/", ":" и\*"") не допускаются, а имена расширенных атрибутов не чувствительны к регистру в дрвфс</span><span class="sxs-lookup"><span data-stu-id="a848e-240">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="a848e-241">Сборка 18252 (прокрутка вперед)</span><span class="sxs-lookup"><span data-stu-id="a848e-241">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="a848e-242">Общие сведения о Windows в сборке 18252 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span><span class="sxs-lookup"><span data-stu-id="a848e-242">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-243">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-243">WSL</span></span>
* <span data-ttu-id="a848e-244">Перемещение двоичных файлов init и бсдтар из библиотеки DLL лксссманажер в отдельную папку Tools</span><span class="sxs-lookup"><span data-stu-id="a848e-244">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="a848e-245">Устранение состязания при закрытии дескриптора файла при использовании CLONE_FILES</span><span class="sxs-lookup"><span data-stu-id="a848e-245">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="a848e-246">Обрабатывайте необязательные поля в/прок/ПИД/маунтинфо при преобразовании путей Дрвфс</span><span class="sxs-lookup"><span data-stu-id="a848e-246">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="a848e-247">Разрешить Дрвфс мкнод выполняться без поддержки метаданных для S_IFREG</span><span class="sxs-lookup"><span data-stu-id="a848e-247">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="a848e-248">Файлы ReadOnly, созданные в Дрвфс, должны иметь набор атрибутов ReadOnly [GH 3411]</span><span class="sxs-lookup"><span data-stu-id="a848e-248">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="a848e-249">Добавление вспомогательного модуля/сбин/Маунт.дрвфс для управления подключением Дрвфс</span><span class="sxs-lookup"><span data-stu-id="a848e-249">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="a848e-250">Используйте переименование POSIX в Дрвфс.</span><span class="sxs-lookup"><span data-stu-id="a848e-250">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="a848e-251">Разрешение преобразования пути на томах без GUID тома.</span><span class="sxs-lookup"><span data-stu-id="a848e-251">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="a848e-252">Сборка 17738 (быстрая)</span><span class="sxs-lookup"><span data-stu-id="a848e-252">Build 17738 (Fast)</span></span>
<span data-ttu-id="a848e-253">Общие сведения о Windows в сборке 17738 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span><span class="sxs-lookup"><span data-stu-id="a848e-253">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-254">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-254">WSL</span></span>
* <span data-ttu-id="a848e-255">Проверка разрешений SetPriority syscall слишком ограничена для изменения того же приоритета потока [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="a848e-255">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="a848e-256">Убедитесь, что для времени загрузки используется Несмещенное время прерываний, чтобы избежать возврата отрицательных значений для clock_gettime (CLOCK_BOOTTIME) [GH 3434].</span><span class="sxs-lookup"><span data-stu-id="a848e-256">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="a848e-257">Обработать символических ссылок в интерпретаторе бинфмт WSL [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="a848e-257">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="a848e-258">Улучшенная обработка очистки дескриптора файла среадграуп.</span><span class="sxs-lookup"><span data-stu-id="a848e-258">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="a848e-259">Сборка 17728 (быстрая)</span><span class="sxs-lookup"><span data-stu-id="a848e-259">Build 17728 (Fast)</span></span>
<span data-ttu-id="a848e-260">Общие сведения о Windows в сборке 17728 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span><span class="sxs-lookup"><span data-stu-id="a848e-260">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-261">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-261">WSL</span></span>
* <span data-ttu-id="a848e-262">Чтобы избежать переполнения, переключайте WSL на использование КекуеринтеррупттимепреЦисе вместо Кекуериперформанцекаунтер [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="a848e-262">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="a848e-263">Присоединение птраце может вызвать неправильное возвращаемое значение из системных вызовов [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="a848e-263">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="a848e-264">Исправление ряда проблем, связанных с AF_UNIX [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="a848e-264">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="a848e-265">Устранение проблемы, которая может привести к сбою взаимодействия WSL, если длина текущего рабочего каталога меньше 5 символов [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="a848e-265">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="a848e-266">Сборка 18204 (прокрутка вперед)</span><span class="sxs-lookup"><span data-stu-id="a848e-266">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="a848e-267">Общие сведения о Windows в сборке 18204 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="a848e-267">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-268">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-268">WSL</span></span>
* <span data-ttu-id="a848e-269">Канал FileSystem инадвертенли очистка, инициированное еполл событие [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="a848e-269">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="a848e-270">Исполняемый файл Win32, запущенный через NTFS символьную ссылку, не учитывает имя символьную ссылку [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="a848e-270">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="a848e-271">Сборка 17723 (быстрая)</span><span class="sxs-lookup"><span data-stu-id="a848e-271">Build 17723 (Fast)</span></span>
<span data-ttu-id="a848e-272">Общие сведения о Windows в сборке 17723 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="a848e-272">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-273">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-273">WSL</span></span>
* <span data-ttu-id="a848e-274">Предотвращение невозможности подключения замыкания на себя с несуществующими портами через одну вторую задержку (GH 3286)</span><span class="sxs-lookup"><span data-stu-id="a848e-274">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="a848e-275">Добавление файла заглушки/прок/СИС/ФС/филе-Макс [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="a848e-275">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="a848e-276">Более точные сведения об области IPV6.</span><span class="sxs-lookup"><span data-stu-id="a848e-276">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="a848e-277">Поддержка PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="a848e-277">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="a848e-278">Канал FileSystem инадвертенли очистка, инициированное еполл событие [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="a848e-278">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="a848e-279">Исполняемый файл Win32, запущенный через NTFS символьную ссылку, не учитывает имя символьную ссылку [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="a848e-279">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="a848e-280">Сборка 17713</span><span class="sxs-lookup"><span data-stu-id="a848e-280">Build 17713</span></span>
<span data-ttu-id="a848e-281">Общие сведения о Windows в сборке 17713 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span><span class="sxs-lookup"><span data-stu-id="a848e-281">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-282">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-282">WSL</span></span>
* <span data-ttu-id="a848e-283">Улучшенная поддержка зомби [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="a848e-283">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="a848e-284">Добавление записей WSL. conf для управления поведением взаимодействия Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="a848e-284">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="a848e-285">Исправление для жетсоккнаме не всегда возвращает тип семейства сокетов UNIX [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="a848e-285">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="a848e-286">Добавление поддержки для ТИОКСТИ [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="a848e-286">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="a848e-287">Неблокирующие сокеты в процессе подключения должны возвращать ЕАГАИН для попыток записи [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="a848e-287">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="a848e-288">Поддержка взаимодействия на подключенных виртуальных жестких дисках [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="a848e-288">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="a848e-289">Устранение проблемы с проверкой разрешений в корневой папке [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="a848e-289">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="a848e-290">Ограниченная поддержка для клавиатуры TTY, КДГКБТИПЕ, КДГКБМОДЕ и КДСКБМОДЕ.</span><span class="sxs-lookup"><span data-stu-id="a848e-290">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="a848e-291">Приложения пользовательского интерфейса Windows должны выполняться, даже если они запущены в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="a848e-291">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="a848e-292">Сборка 17704</span><span class="sxs-lookup"><span data-stu-id="a848e-292">Build 17704</span></span>
<span data-ttu-id="a848e-293">Общие сведения о Windows в сборке 17704 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span><span class="sxs-lookup"><span data-stu-id="a848e-293">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-294">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-294">WSL</span></span>
* <span data-ttu-id="a848e-295">Add WSL-u или--User, параметр [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="a848e-295">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="a848e-296">Устранение проблем с запуском WSL при включении быстрого запуска [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="a848e-296">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="a848e-297">Сокеты Unix должны хранить отключенные одноранговые учетные данные [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="a848e-297">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="a848e-298">Неблокирующие сокеты Unix с неограниченным сбоем с ЕАГАИН [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="a848e-298">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="a848e-299">Case = Off — новый тип подключения дрвфс по умолчанию [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="a848e-299">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="a848e-300">Дополнительные сведения см. в [блоге](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) .</span><span class="sxs-lookup"><span data-stu-id="a848e-300">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="a848e-301">Добавьте вслконфиг/терминате, чтобы прерывать выполнение распределений.</span><span class="sxs-lookup"><span data-stu-id="a848e-301">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="a848e-302">Сборка 17692</span><span class="sxs-lookup"><span data-stu-id="a848e-302">Build 17692</span></span>
<span data-ttu-id="a848e-303">Общие сведения о Windows в сборке 17692 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span><span class="sxs-lookup"><span data-stu-id="a848e-303">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-304">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-304">WSL</span></span>
* <span data-ttu-id="a848e-305">Устранена проблема с записями в контекстном меню оболочки WSL, которые неправильно обработают пути с пробелами.</span><span class="sxs-lookup"><span data-stu-id="a848e-305">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="a848e-306">Предоставить учет регистра в каталоге в качестве расширенного атрибута</span><span class="sxs-lookup"><span data-stu-id="a848e-306">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="a848e-307">ARM64 Эмуляция операций обслуживания кэша.</span><span class="sxs-lookup"><span data-stu-id="a848e-307">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="a848e-308">Устраните [проблему DotNet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="a848e-308">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="a848e-309">Дрвфс: только escape-символы в закрытом диапазоне, которые соответствуют escape-символу.</span><span class="sxs-lookup"><span data-stu-id="a848e-309">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="a848e-310">Сборка 17686</span><span class="sxs-lookup"><span data-stu-id="a848e-310">Build 17686</span></span>
<span data-ttu-id="a848e-311">Общие сведения о Windows в сборке 17686 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span><span class="sxs-lookup"><span data-stu-id="a848e-311">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-312">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-312">WSL</span></span>
* <span data-ttu-id="a848e-313">Устранение ошибки при проверке длины интерпретатора анализатора ELF [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="a848e-313">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="a848e-314">WSL абсолютные таймеры с временем в прошлом не срабатывают [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="a848e-314">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="a848e-315">Убедитесь, что вновь созданные точки повторного анализа указаны в родительском каталоге.</span><span class="sxs-lookup"><span data-stu-id="a848e-315">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="a848e-316">Атомарное создание каталогов с учетом регистра в Дрвфс.</span><span class="sxs-lookup"><span data-stu-id="a848e-316">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="a848e-317">Сборка 17677</span><span class="sxs-lookup"><span data-stu-id="a848e-317">Build 17677</span></span>
<span data-ttu-id="a848e-318">Общие сведения о Windows в сборке 17677 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span><span class="sxs-lookup"><span data-stu-id="a848e-318">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-319">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-319">WSL</span></span>
* <span data-ttu-id="a848e-320">Исправлена дополнительная проблема, когда многопоточные операции могут возвращать ЕНОЕНТ, даже если файл существует.</span><span class="sxs-lookup"><span data-stu-id="a848e-320">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="a848e-321">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="a848e-321">[GH 2712]</span></span>
* <span data-ttu-id="a848e-322">Исправлена ошибка запуска WSL при включенном УМЦИ.</span><span class="sxs-lookup"><span data-stu-id="a848e-322">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="a848e-323">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="a848e-323">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="a848e-324">Сборка 17666</span><span class="sxs-lookup"><span data-stu-id="a848e-324">Build 17666</span></span>
<span data-ttu-id="a848e-325">Общие сведения о Windows в сборке 17666 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span><span class="sxs-lookup"><span data-stu-id="a848e-325">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-326">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-326">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="a848e-327">ПРЕДУПРЕЖДЕНИЕ! Существует ошибка, препятствующая запуску WSL на некоторых наборах микросхем AMD [GH 3134].</span><span class="sxs-lookup"><span data-stu-id="a848e-327">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="a848e-328">Исправление готово и делает его переход к ветви Insider Build.</span><span class="sxs-lookup"><span data-stu-id="a848e-328">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="a848e-329">Добавьте контекстное меню обозревателя, чтобы запустить WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="a848e-329">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="a848e-330">Для использования удерживайте клавишу Shift и щелкните правой кнопкой мыши в окне проводника.</span><span class="sxs-lookup"><span data-stu-id="a848e-330">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="a848e-331">Устранение неблокирующего поведения сокета UNIX [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="a848e-331">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="a848e-332">Исправьте команду НЕТЛИНК в соответствии с отчетом в GH 2026.</span><span class="sxs-lookup"><span data-stu-id="a848e-332">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="a848e-333">Добавлена поддержка флагов распространения подключения [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="a848e-333">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="a848e-334">Устранена проблема с усечением, которая не вызывает инотифи событий [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="a848e-334">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="a848e-335">Добавьте параметр--exec для WSL. exe, чтобы вызвать один двоичный файл без оболочки.</span><span class="sxs-lookup"><span data-stu-id="a848e-335">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="a848e-336">Добавьте параметр--Distribution для WSL. exe, чтобы выбрать конкретный дистрибутив.</span><span class="sxs-lookup"><span data-stu-id="a848e-336">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="a848e-337">Сборка 17655 (прокрутка вперед)</span><span class="sxs-lookup"><span data-stu-id="a848e-337">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="a848e-338">Общие сведения о Windows в сборке 17655 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="a848e-338">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-339">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-339">WSL</span></span>
* <span data-ttu-id="a848e-340">Ограниченная поддержка дмесг.</span><span class="sxs-lookup"><span data-stu-id="a848e-340">Limited support for dmesg.</span></span> <span data-ttu-id="a848e-341">Теперь приложения могут входить в дмесг.</span><span class="sxs-lookup"><span data-stu-id="a848e-341">Applications can now log to dmesg.</span></span> <span data-ttu-id="a848e-342">Драйвер WSL записывает ограниченные сведения в дмесг.</span><span class="sxs-lookup"><span data-stu-id="a848e-342">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="a848e-343">В будущем это можно продлить, донести другие сведения и диагностику из драйвера.</span><span class="sxs-lookup"><span data-stu-id="a848e-343">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="a848e-344">Примечание. в настоящее время дмесг поддерживается через `/dev/kmsg` интерфейс устройства.</span><span class="sxs-lookup"><span data-stu-id="a848e-344">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="a848e-345">`syslog`интерфейс сикалл пока не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a848e-345">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="a848e-346">И, таким образом, некоторые `dmesg` параметры командной строки, такие как `-S`, `-C` не работают.</span><span class="sxs-lookup"><span data-stu-id="a848e-346">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="a848e-347">Исправлена проблема, когда многопоточные операции могут возвращать ЕНОЕНТ, даже если файл существует.</span><span class="sxs-lookup"><span data-stu-id="a848e-347">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="a848e-348">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="a848e-348">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="a848e-349">Сборка 17639 (прокрутка вперед)</span><span class="sxs-lookup"><span data-stu-id="a848e-349">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="a848e-350">Общие сведения о Windows в сборке 17639 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="a848e-350">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-351">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-351">WSL</span></span>
* <span data-ttu-id="a848e-352">Изменение значения GID и режима по умолчанию для последовательных устройств на соответствие Native [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="a848e-352">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="a848e-353">Дрвфс теперь поддерживает расширенные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="a848e-353">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="a848e-354">Примечание. Дрвфс имеет некоторые ограничения на имена расширенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="a848e-354">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="a848e-355">В частности, некоторые символы (например, "/", ":" и\*"") не допускаются, а имена расширенных атрибутов не чувствительны к регистру в дрвфс</span><span class="sxs-lookup"><span data-stu-id="a848e-355">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="a848e-356">Сборка 17133 (быстрая)</span><span class="sxs-lookup"><span data-stu-id="a848e-356">Build 17133 (Fast)</span></span>
<span data-ttu-id="a848e-357">Общие сведения о Windows в сборке 17133 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="a848e-357">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-358">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-358">WSL</span></span>
* <span data-ttu-id="a848e-359">Исправление для зависания в WSL.</span><span class="sxs-lookup"><span data-stu-id="a848e-359">Fix for hang in WSL.</span></span> <span data-ttu-id="a848e-360">[GH 3039, 3034]</span><span class="sxs-lookup"><span data-stu-id="a848e-360">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="a848e-361">Сборка 17128 (быстрая)</span><span class="sxs-lookup"><span data-stu-id="a848e-361">Build 17128 (Fast)</span></span>
<span data-ttu-id="a848e-362">Общие сведения о Windows в сборке 17128 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="a848e-362">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-363">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-363">WSL</span></span>
* <span data-ttu-id="a848e-364">Нет</span><span class="sxs-lookup"><span data-stu-id="a848e-364">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="a848e-365">Сборка 17627 (прокрутка вперед)</span><span class="sxs-lookup"><span data-stu-id="a848e-365">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="a848e-366">Общие сведения о Windows в сборке 17627 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="a848e-366">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-367">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-367">WSL</span></span>
* <span data-ttu-id="a848e-368">Добавлена поддержка операций с поддержкой футекс PI.</span><span class="sxs-lookup"><span data-stu-id="a848e-368">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="a848e-369">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="a848e-369">[GH 1006]</span></span>
    * <span data-ttu-id="a848e-370">Обратите внимание, что приоритеты в настоящее время не поддерживают функцию WSL, так что существуют ограничения, но стандартное использование должно быть разблокировано.</span><span class="sxs-lookup"><span data-stu-id="a848e-370">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="a848e-371">Поддержка брандмауэра Windows для процессов WSL.</span><span class="sxs-lookup"><span data-stu-id="a848e-371">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="a848e-372">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="a848e-372">[GH 1852]</span></span>
    * <span data-ttu-id="a848e-373">Например, чтобы разрешить процессу Python WSL прослушивание любого порта, используйте команду Windows cmd с повышенными привилегиями:```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="a848e-373">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="a848e-374">Дополнительные сведения о добавлении правил брандмауэра см. в разделе [ссылка](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh) .</span><span class="sxs-lookup"><span data-stu-id="a848e-374">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="a848e-375">Использовать оболочку по умолчанию для пользователя при использовании WSL. exe.</span><span class="sxs-lookup"><span data-stu-id="a848e-375">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="a848e-376">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="a848e-376">[GH 2372]</span></span>
* <span data-ttu-id="a848e-377">Сообщать обо всех сетевых интерфейсах как Ethernet.</span><span class="sxs-lookup"><span data-stu-id="a848e-377">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="a848e-378">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="a848e-378">[GH 2996]</span></span>
* <span data-ttu-id="a848e-379">Улучшенная обработка поврежденного файла/etc/passwd.</span><span class="sxs-lookup"><span data-stu-id="a848e-379">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="a848e-380">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="a848e-380">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="a848e-381">Консоль</span><span class="sxs-lookup"><span data-stu-id="a848e-381">Console</span></span>
* <span data-ttu-id="a848e-382">Нет исправлений.</span><span class="sxs-lookup"><span data-stu-id="a848e-382">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-383">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-383">LTP Results:</span></span>
<span data-ttu-id="a848e-384">Выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="a848e-384">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="a848e-385">Сборка 17618 (прокрутка вперед)</span><span class="sxs-lookup"><span data-stu-id="a848e-385">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="a848e-386">Общие сведения о Windows в сборке 17618 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="a848e-386">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-387">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-387">WSL</span></span>
* <span data-ttu-id="a848e-388">Введение функций псеудоконсоле для взаимодействия NT [GH 988, 1366, 1433, 1542, 2370, 2406].</span><span class="sxs-lookup"><span data-stu-id="a848e-388">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="a848e-389">Устаревший механизм установки (лксрун. exe) является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="a848e-389">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="a848e-390">Для установки дистрибутивов поддерживается механизм Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="a848e-390">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="a848e-391">Консоль</span><span class="sxs-lookup"><span data-stu-id="a848e-391">Console</span></span>
* <span data-ttu-id="a848e-392">Нет исправлений.</span><span class="sxs-lookup"><span data-stu-id="a848e-392">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-393">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-393">LTP Results:</span></span>
<span data-ttu-id="a848e-394">Выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="a848e-394">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="a848e-395">Сборка 17110</span><span class="sxs-lookup"><span data-stu-id="a848e-395">Build 17110</span></span>
<span data-ttu-id="a848e-396">Общие сведения о Windows в сборке 17110 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span><span class="sxs-lookup"><span data-stu-id="a848e-396">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-397">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-397">WSL</span></span>
* <span data-ttu-id="a848e-398">Разрешить прекращение/ИНИТ из Windows [GH 2928].</span><span class="sxs-lookup"><span data-stu-id="a848e-398">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="a848e-399">Дрвфс теперь использует учет регистра в каталоге по умолчанию (аналогично параметру подключения "Case = Dir").</span><span class="sxs-lookup"><span data-stu-id="a848e-399">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="a848e-400">При использовании варианта "Case = Force" (прежнее поведение) требуется задать раздел реестра.</span><span class="sxs-lookup"><span data-stu-id="a848e-400">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="a848e-401">Выполните следующую команду, чтобы включить "Case = Force", если необходимо использовать ее: reg Add Хклм\систем\куррентконтролсет\сервицес\лкссс/v Дрвфсалловфорцекасесенситивити/t REG_DWORD/d 1</span><span class="sxs-lookup"><span data-stu-id="a848e-401">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="a848e-402">Если у вас есть каталоги, созданные с помощью WSL в более ранней версии Windows, которые должны быть чувствительны к регистру, используйте fsutil. exe, чтобы пометить их как учет <path> регистра: fsutil. exe file сеткасесенситивеинфо Enable</span><span class="sxs-lookup"><span data-stu-id="a848e-402">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="a848e-403">Строки завершения со значением NULL, возвращаемые из uname syscall.</span><span class="sxs-lookup"><span data-stu-id="a848e-403">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="a848e-404">Консоль</span><span class="sxs-lookup"><span data-stu-id="a848e-404">Console</span></span>
* <span data-ttu-id="a848e-405">Нет исправлений.</span><span class="sxs-lookup"><span data-stu-id="a848e-405">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-406">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-406">LTP Results:</span></span>
<span data-ttu-id="a848e-407">Выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="a848e-407">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="a848e-408">Сборка 17107</span><span class="sxs-lookup"><span data-stu-id="a848e-408">Build 17107</span></span>
<span data-ttu-id="a848e-409">Общие сведения о Windows в сборке 17107 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span><span class="sxs-lookup"><span data-stu-id="a848e-409">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-410">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-410">WSL</span></span>
* <span data-ttu-id="a848e-411">Поддержка ТКСЕТСФ и ТКСЕТСВ в конечных точках главного PTY [GH 2552].</span><span class="sxs-lookup"><span data-stu-id="a848e-411">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="a848e-412">Запуск одновременных процессов взаимодействия может привести к ЕИНВАЛ [GH 2813].</span><span class="sxs-lookup"><span data-stu-id="a848e-412">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="a848e-413">Исправление PTRACE_ATTACH для отображения правильного состояния трассировки в/прок/ПИД/статус.</span><span class="sxs-lookup"><span data-stu-id="a848e-413">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="a848e-414">Устранение состязания, когда кратковременные процессы, клонированные с помощью флагов КЛЕАРТИД и СЕТТИД, могут выйти без очистки адреса TID.</span><span class="sxs-lookup"><span data-stu-id="a848e-414">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="a848e-415">Отображать сообщение при обновлении каталогов файловой системы Linux при переходе с сборки до 17093.</span><span class="sxs-lookup"><span data-stu-id="a848e-415">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="a848e-416">Дополнительные сведения об изменениях в файловой системе 17093 см. в заметках о выпуске [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span><span class="sxs-lookup"><span data-stu-id="a848e-416">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="a848e-417">Консоль</span><span class="sxs-lookup"><span data-stu-id="a848e-417">Console</span></span>
* <span data-ttu-id="a848e-418">Нет исправлений.</span><span class="sxs-lookup"><span data-stu-id="a848e-418">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-419">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-419">LTP Results:</span></span>
<span data-ttu-id="a848e-420">Выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="a848e-420">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="a848e-421">Сборка 17101</span><span class="sxs-lookup"><span data-stu-id="a848e-421">Build 17101</span></span>
<span data-ttu-id="a848e-422">Общие сведения о Windows в сборке 17101 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="a848e-422">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-423">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-423">WSL</span></span>
* <span data-ttu-id="a848e-424">Поддержка сигналфд.</span><span class="sxs-lookup"><span data-stu-id="a848e-424">Support for signalfd.</span></span> <span data-ttu-id="a848e-425">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="a848e-425">[GH 129]</span></span>
* <span data-ttu-id="a848e-426">Поддерживает имена файлов, содержащие недопустимые символы NTFS, путем их кодирования в виде закрытых символов Юникода.</span><span class="sxs-lookup"><span data-stu-id="a848e-426">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="a848e-427">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="a848e-427">[GH 1514]</span></span>
* <span data-ttu-id="a848e-428">Функция автоматического подключения будет доступна только для чтения, если запись не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a848e-428">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="a848e-429">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="a848e-429">[GH 2603]</span></span>
* <span data-ttu-id="a848e-430">Разрешить вставлять суррогатные пары Юникода (например, символы эмодзи).</span><span class="sxs-lookup"><span data-stu-id="a848e-430">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="a848e-431">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="a848e-431">[GH 2765]</span></span>
* <span data-ttu-id="a848e-432">Псевдо-файлы в/proc и/sys должны возвращать чтение и запись, готовые к использованию SELECT, poll, еполл, et al. [GH 2838]</span><span class="sxs-lookup"><span data-stu-id="a848e-432">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="a848e-433">Устранена проблема, из-за которой служба может переходить в бесконечный цикл, когда реестр был изменен или поврежден.</span><span class="sxs-lookup"><span data-stu-id="a848e-433">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="a848e-434">Исправьте сообщения нетлинк для работы с более новой (вышестоящей 4,14) версией iproute2.</span><span class="sxs-lookup"><span data-stu-id="a848e-434">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="a848e-435">Консоль</span><span class="sxs-lookup"><span data-stu-id="a848e-435">Console</span></span>
* <span data-ttu-id="a848e-436">Нет исправлений.</span><span class="sxs-lookup"><span data-stu-id="a848e-436">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-437">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-437">LTP Results:</span></span>
<span data-ttu-id="a848e-438">Выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="a848e-438">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="a848e-439">Сборка 17093</span><span class="sxs-lookup"><span data-stu-id="a848e-439">Build 17093</span></span>
<span data-ttu-id="a848e-440">Общие сведения о Windows в сборке 17093 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span><span class="sxs-lookup"><span data-stu-id="a848e-440">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="a848e-441">Внимание!</span><span class="sxs-lookup"><span data-stu-id="a848e-441">Important:</span></span>
<span data-ttu-id="a848e-442">При запуске WSL в первый раз после обновления до этой сборки необходимо выполнить некоторые действия по обновлению каталогов файловой системы Linux.</span><span class="sxs-lookup"><span data-stu-id="a848e-442">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="a848e-443">Это может занять несколько минут, поэтому WSL может показаться медленно запущенным.</span><span class="sxs-lookup"><span data-stu-id="a848e-443">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="a848e-444">Это должно происходить только один раз для каждого дистрибутива, установленного из магазина.</span><span class="sxs-lookup"><span data-stu-id="a848e-444">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="a848e-445">Улучшена поддержка чувствительности к регистру в Дрвфс.</span><span class="sxs-lookup"><span data-stu-id="a848e-445">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="a848e-446">Дрвфс теперь поддерживает учет регистра в каталоге.</span><span class="sxs-lookup"><span data-stu-id="a848e-446">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="a848e-447">Это новый флаг, который можно задать для каталогов, чтобы указать, что все операции в этих каталогах должны обрабатываться с учетом регистра, что позволяет даже приложениям Windows правильно открывать файлы, отличающиеся только регистром.</span><span class="sxs-lookup"><span data-stu-id="a848e-447">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="a848e-448">В Дрвфс есть новые варианты подключения, контролирующие чувствительность к учету регистра для каждого каталога.</span><span class="sxs-lookup"><span data-stu-id="a848e-448">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="a848e-449">вариант = Force: все каталоги обрабатываются с учетом регистра (за исключением корневого диска).</span><span class="sxs-lookup"><span data-stu-id="a848e-449">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="a848e-450">Новые каталоги, созданные с помощью WSL, помечаются с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="a848e-450">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="a848e-451">Это поведение прежних версий, за исключением пометки новых каталогов с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="a848e-451">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="a848e-452">Case = Dir: только каталоги с флагом учета регистра для каждого каталога обрабатываются с учетом регистра; другие каталоги не чувствительны к регистру.</span><span class="sxs-lookup"><span data-stu-id="a848e-452">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="a848e-453">Новые каталоги, созданные с помощью WSL, помечаются с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="a848e-453">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="a848e-454">Case = Off: только каталоги с флагом учета регистра для каждого каталога обрабатываются с учетом регистра; другие каталоги не чувствительны к регистру.</span><span class="sxs-lookup"><span data-stu-id="a848e-454">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="a848e-455">Новые каталоги, созданные с помощью WSL, помечаются как нечувствительные к регистру.</span><span class="sxs-lookup"><span data-stu-id="a848e-455">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="a848e-456">Примечание. каталоги, созданные WSL в предыдущих выпусках, не имеют установленного флага, поэтому не будут обрабатываться с учетом регистра, если используется параметр "Case = Dir".</span><span class="sxs-lookup"><span data-stu-id="a848e-456">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="a848e-457">Можно установить этот флаг в существующие каталоги в ближайшее время.</span><span class="sxs-lookup"><span data-stu-id="a848e-457">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="a848e-458">Пример подключения с этими параметрами (для существующих дисков необходимо сначала отключиться, прежде чем можно будет подключиться с разными параметрами): Sudo Mount-t дрвфс C:/МНТ/к-o Case = dir</span><span class="sxs-lookup"><span data-stu-id="a848e-458">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="a848e-459">Пока что параметр Case = Force по умолчанию все еще используется.</span><span class="sxs-lookup"><span data-stu-id="a848e-459">For now, case=force is still the default option.</span></span> <span data-ttu-id="a848e-460">В будущем это будет изменено на case = dir.</span><span class="sxs-lookup"><span data-stu-id="a848e-460">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="a848e-461">Теперь вы можете использовать косую черту в путях Windows при подключении Дрвфс, например Sudo Mount-t дрвфс//сервер/шаре/МНТ/шаре</span><span class="sxs-lookup"><span data-stu-id="a848e-461">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="a848e-462">WSL теперь обрабатывает файл/etc/fstab во время запуска экземпляра [GH 2636].</span><span class="sxs-lookup"><span data-stu-id="a848e-462">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="a848e-463">Это делается до автоматического подключения дисков Дрвфс. все диски, которые уже подключены fstab, не будут автоматически подключены, что позволит вам изменить точку подключения для конкретных дисков.</span><span class="sxs-lookup"><span data-stu-id="a848e-463">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="a848e-464">Это поведение можно отключить с помощью WSL. conf.</span><span class="sxs-lookup"><span data-stu-id="a848e-464">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="a848e-465">Файлы Mount, маунтинфо и маунтстатс в/proc должны быть специально экранированными специальными символами, такими как символы обратной косой черты и пробелы [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="a848e-465">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="a848e-466">Специальные файлы, созданные с помощью Дрвфс, такие как WSL символьные ссылки или FIFO, а также сокеты, если метаданные включены, теперь можно копировать и перемещать из Windows.</span><span class="sxs-lookup"><span data-stu-id="a848e-466">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="a848e-467">WSL можно настроить с помощью WSL. conf.</span><span class="sxs-lookup"><span data-stu-id="a848e-467">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="a848e-468">Мы добавили метод для автоматической настройки определенных функций в WSL, которые будут применяться при каждом запуске подсистемы.</span><span class="sxs-lookup"><span data-stu-id="a848e-468">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="a848e-469">Сюда входят параметры автоподключения и конфигурация сети.</span><span class="sxs-lookup"><span data-stu-id="a848e-469">This includes automount options and network configuration.</span></span> <span data-ttu-id="a848e-470">Дополнительные сведения см. в нашей записи в блоге по адресу: https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="a848e-470">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="a848e-471">AF_UNIX разрешает подключения через сокет между процессами Linux в собственных процессах WSL и Windows</span><span class="sxs-lookup"><span data-stu-id="a848e-471">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="a848e-472">Приложения WSL и Windows теперь могут взаимодействовать друг с другом через сокеты Unix.</span><span class="sxs-lookup"><span data-stu-id="a848e-472">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="a848e-473">Представьте, что вы хотите запустить службу в Windows и сделать ее доступной для приложений Windows и WSL.</span><span class="sxs-lookup"><span data-stu-id="a848e-473">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="a848e-474">Теперь это возможно благодаря сокетам UNIX.</span><span class="sxs-lookup"><span data-stu-id="a848e-474">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="a848e-475">Дополнительные сведения см. в публикации в блоге по адресу https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="a848e-475">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-476">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-476">WSL</span></span>
* <span data-ttu-id="a848e-477">Поддержка mmap () с MAP_NORESERVE [GH 121, 2784]</span><span class="sxs-lookup"><span data-stu-id="a848e-477">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="a848e-478">Поддержка CLONE_PTRACE и CLONE_UNTRACED [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="a848e-478">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="a848e-479">Обработайте сигнал завершения без СИГЧЛД в клоне [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="a848e-479">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="a848e-480">Заглушки/proc/sys/fs/inotify/max_user_instances и/proc/sys/fs/inotify/max_user_watches [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="a848e-480">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="a848e-481">Произошла ошибка при загрузке двоичных файлов ELF, содержащих заголовки загрузки с ненулевыми смещениями [GH 1884]</span><span class="sxs-lookup"><span data-stu-id="a848e-481">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="a848e-482">Обнуление конечных страниц в байтах при загрузке изображений.</span><span class="sxs-lookup"><span data-stu-id="a848e-482">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="a848e-483">Сокращение случаев, когда ексекве автоматически завершает процесс</span><span class="sxs-lookup"><span data-stu-id="a848e-483">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="a848e-484">Консоль</span><span class="sxs-lookup"><span data-stu-id="a848e-484">Console</span></span>
* <span data-ttu-id="a848e-485">Нет исправлений.</span><span class="sxs-lookup"><span data-stu-id="a848e-485">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-486">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-486">LTP Results:</span></span>
<span data-ttu-id="a848e-487">Выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="a848e-487">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="a848e-488">Сборка 17083</span><span class="sxs-lookup"><span data-stu-id="a848e-488">Build 17083</span></span>
<span data-ttu-id="a848e-489">Общие сведения о Windows в сборке 17083 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="a848e-489">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-490">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-490">WSL</span></span>
* <span data-ttu-id="a848e-491">Исправлена критическая проблема, связанная с еполл [GH 2798, 2801, 2857]</span><span class="sxs-lookup"><span data-stu-id="a848e-491">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="a848e-492">Исправлены зависания при отключении ASLR [GH 1185, 2870]</span><span class="sxs-lookup"><span data-stu-id="a848e-492">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="a848e-493">Убедитесь, что операции mmap отображаются как атомарные [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="a848e-493">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="a848e-494">Консоль</span><span class="sxs-lookup"><span data-stu-id="a848e-494">Console</span></span>
* <span data-ttu-id="a848e-495">Нет исправлений.</span><span class="sxs-lookup"><span data-stu-id="a848e-495">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-496">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-496">LTP Results:</span></span>
<span data-ttu-id="a848e-497">Выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="a848e-497">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="a848e-498">Сборка 17074</span><span class="sxs-lookup"><span data-stu-id="a848e-498">Build 17074</span></span>
<span data-ttu-id="a848e-499">Общие сведения о Windows в сборке 17074 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span><span class="sxs-lookup"><span data-stu-id="a848e-499">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-500">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-500">WSL</span></span>
* <span data-ttu-id="a848e-501">Фиксированный формат хранения метаданных Дрвфс [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="a848e-501">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="a848e-502">**Важно!** Метаданные Дрвфс, созданные до этой сборки, будут отображаться неправильно или вообще.</span><span class="sxs-lookup"><span data-stu-id="a848e-502">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="a848e-503">Чтобы исправить затронутые файлы, используйте chmod и човн для повторного применения метаданных.</span><span class="sxs-lookup"><span data-stu-id="a848e-503">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="a848e-504">Исправлена проблема с несколькими сигналами и перезапуском syscall.</span><span class="sxs-lookup"><span data-stu-id="a848e-504">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="a848e-505">Консоль</span><span class="sxs-lookup"><span data-stu-id="a848e-505">Console</span></span>
* <span data-ttu-id="a848e-506">Нет исправлений.</span><span class="sxs-lookup"><span data-stu-id="a848e-506">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-507">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-507">LTP Results:</span></span>
<span data-ttu-id="a848e-508">Выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="a848e-508">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="a848e-509">Сборка 17063</span><span class="sxs-lookup"><span data-stu-id="a848e-509">Build 17063</span></span>
<span data-ttu-id="a848e-510">Общие сведения о Windows в сборке 17063 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span><span class="sxs-lookup"><span data-stu-id="a848e-510">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="a848e-511">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-511">WSL</span></span>
* <span data-ttu-id="a848e-512">Дрвфс поддерживает дополнительные метаданные Linux.</span><span class="sxs-lookup"><span data-stu-id="a848e-512">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="a848e-513">Это позволяет задать владельца и режим файлов с помощью команды chmod/човн, а также создать специальные файлы, такие как FIFO, сокеты Unix и файлы устройств.</span><span class="sxs-lookup"><span data-stu-id="a848e-513">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="a848e-514">По умолчанию этот параметр отключен, так как он по-прежнему эксперименталь.</span><span class="sxs-lookup"><span data-stu-id="a848e-514">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="a848e-515">**Примечание.**  Исправлена ошибка в формате метаданных, используемом Дрвфс.</span><span class="sxs-lookup"><span data-stu-id="a848e-515">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="a848e-516">Хотя метаданные работают в этой сборке для эксперимента, будущие сборки не будут правильно считывать метаданные, созданные этой сборкой.</span><span class="sxs-lookup"><span data-stu-id="a848e-516">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="a848e-517">Возможно, потребуется вручную обновить владельца измененных файлов, и устройства с пользовательским ИДЕНТИФИКАТОРом устройства потребуется создать заново.</span><span class="sxs-lookup"><span data-stu-id="a848e-517">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="a848e-518">Чтобы включить, подключите Дрвфс с параметром Metadata (чтобы включить его на существующем подключении, необходимо сначала отключить его):</span><span class="sxs-lookup"><span data-stu-id="a848e-518">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="a848e-519">Разрешения Linux добавляются в файл в качестве дополнительных метаданных; они не влияют на разрешения Windows.</span><span class="sxs-lookup"><span data-stu-id="a848e-519">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="a848e-520">Помните, что изменение файла с помощью редактора Windows может привести к удалению метаданных.</span><span class="sxs-lookup"><span data-stu-id="a848e-520">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="a848e-521">В этом случае файл вернется к разрешениям по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a848e-521">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="a848e-522">Добавлены параметры подключения к Дрвфс для управления файлами без метаданных.</span><span class="sxs-lookup"><span data-stu-id="a848e-522">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="a848e-523">UID: идентификатор пользователя, используемый для владельца всех файлов.</span><span class="sxs-lookup"><span data-stu-id="a848e-523">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="a848e-524">GID: идентификатор группы, используемый для владельца всех файлов.</span><span class="sxs-lookup"><span data-stu-id="a848e-524">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="a848e-525">umask: восьмеричная Маска разрешений, исключаемых из всех файлов и каталогов.</span><span class="sxs-lookup"><span data-stu-id="a848e-525">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="a848e-526">фмаск: восьмеричная Маска разрешений, исключаемых из обычных файлов.</span><span class="sxs-lookup"><span data-stu-id="a848e-526">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="a848e-527">дмаск: восьмеричная Маска разрешений, исключаемых из всех каталогов.</span><span class="sxs-lookup"><span data-stu-id="a848e-527">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="a848e-528">Пример:</span><span class="sxs-lookup"><span data-stu-id="a848e-528">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="a848e-529">Объедините с параметром Metadata, чтобы указать разрешения по умолчанию для файлов без метаданных.</span><span class="sxs-lookup"><span data-stu-id="a848e-529">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="a848e-530">Появилась новая переменная среды, `WSLENV`, чтобы настроить поток переменных среды между WSL и Win32.</span><span class="sxs-lookup"><span data-stu-id="a848e-530">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="a848e-531">Пример:</span><span class="sxs-lookup"><span data-stu-id="a848e-531">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="a848e-532">`WSLENV`Разделенный двоеточием список переменных среды, которые могут быть добавлены при запуске процессов WSL из процессов Win32 или Win32 из WSL.</span><span class="sxs-lookup"><span data-stu-id="a848e-532">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="a848e-533">Каждая переменная может иметь суффикс с косой чертой, за которой следуют флаги для указания способа преобразования.</span><span class="sxs-lookup"><span data-stu-id="a848e-533">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="a848e-534">ш Значение — это путь, который должен быть преобразован между WSL путями и путями Win32.</span><span class="sxs-lookup"><span data-stu-id="a848e-534">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="a848e-535">н Значение представляет собой список путей.</span><span class="sxs-lookup"><span data-stu-id="a848e-535">l: The value is a list of paths.</span></span> <span data-ttu-id="a848e-536">В WSL это список, разделенный двоеточием.</span><span class="sxs-lookup"><span data-stu-id="a848e-536">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="a848e-537">В Win32 это список, разделенный точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="a848e-537">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="a848e-538">ть Значение должно включаться только при вызове WSL из Win32</span><span class="sxs-lookup"><span data-stu-id="a848e-538">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="a848e-539">Белая Значение должно включаться только при вызове Win32 из WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-539">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="a848e-540">Вы можете задать `WSLENV` в bashrc или в пользовательской среде Windows для пользователя.</span><span class="sxs-lookup"><span data-stu-id="a848e-540">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="a848e-541">дрвфс подключения правильно сохраняет метки времени с tar, CP-p (GH 1939).</span><span class="sxs-lookup"><span data-stu-id="a848e-541">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="a848e-542">дрвфс символических ссылок сообщить правильный размер (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="a848e-542">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="a848e-543">чтение и запись работают для очень больших размеров ввода-вывода (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="a848e-543">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="a848e-544">ваитпид работает с идентификаторами групп процессов (GH 2534)</span><span class="sxs-lookup"><span data-stu-id="a848e-544">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="a848e-545">значительно улучшена производительность mmap для больших резервных регионов. повышение производительности ГХК (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="a848e-545">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="a848e-546">индивидуальность поддерживается для READ_IMPLIES_EXEC; исправления прыжка и клисп (GH 1185)</span><span class="sxs-lookup"><span data-stu-id="a848e-546">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="a848e-547">мпротект поддерживает PROT_GROWSDOWN; исправления клисп (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="a848e-547">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="a848e-548">исправления ошибок страниц в режиме перефиксации; исправления сбкл (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="a848e-548">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="a848e-549">Clone поддерживает несколько сочетаний флагов</span><span class="sxs-lookup"><span data-stu-id="a848e-549">clone supports more flags combinations</span></span>
* <span data-ttu-id="a848e-550">Поддержка SELECT/еполл файлов еполл (ранее — без операций).</span><span class="sxs-lookup"><span data-stu-id="a848e-550">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="a848e-551">Уведомлять птраце о нереализованном syscall.</span><span class="sxs-lookup"><span data-stu-id="a848e-551">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="a848e-552">Игнорировать интерфейсы, не используемые при создании resolv. conf серверах имен [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="a848e-552">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="a848e-553">Перечисление сетевых интерфейсов без физического адреса.</span><span class="sxs-lookup"><span data-stu-id="a848e-553">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="a848e-554">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="a848e-554">[GH 2685]</span></span>
* <span data-ttu-id="a848e-555">Исправления и улучшения для дополнительных ошибок.</span><span class="sxs-lookup"><span data-stu-id="a848e-555">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="a848e-556">Средства Linux, доступные для разработчиков в Windows</span><span class="sxs-lookup"><span data-stu-id="a848e-556">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="a848e-557">Командная строка Windows цепочки инструментов включает бсдтар (tar) и фигурные скобки.</span><span class="sxs-lookup"><span data-stu-id="a848e-557">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="a848e-558">Ознакомьтесь с [этим блогом](https://aka.ms/tarcurlwindows) , чтобы узнать больше о добавлении этих двух новых средств и о том, как они позволяют разработчикам работать в Windows.</span><span class="sxs-lookup"><span data-stu-id="a848e-558">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="a848e-559">`AF_UNIX`доступен в пакете SDK для предварительной оценки Windows (17061 +).</span><span class="sxs-lookup"><span data-stu-id="a848e-559">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="a848e-560">Ознакомьтесь с [этим блогом](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) , чтобы `AF_UNIX` узнать больше о том, как разработчики могут его использовать в Windows.</span><span class="sxs-lookup"><span data-stu-id="a848e-560">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="a848e-561">Консоль</span><span class="sxs-lookup"><span data-stu-id="a848e-561">Console</span></span>
* <span data-ttu-id="a848e-562">Нет исправлений.</span><span class="sxs-lookup"><span data-stu-id="a848e-562">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-563">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-563">LTP Results:</span></span>
<span data-ttu-id="a848e-564">Выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="a848e-564">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="a848e-565">Сборка 17046</span><span class="sxs-lookup"><span data-stu-id="a848e-565">Build 17046</span></span>

<span data-ttu-id="a848e-566">Общие сведения о Windows в сборке 17046 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span><span class="sxs-lookup"><span data-stu-id="a848e-566">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="a848e-567">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-567">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="a848e-568">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-568">WSL</span></span>
- <span data-ttu-id="a848e-569">Разрешить выполнение процессов без активного терминала.</span><span class="sxs-lookup"><span data-stu-id="a848e-569">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="a848e-570">[GH 709, 1007, 1511, 2252, 2391, et al.]</span><span class="sxs-lookup"><span data-stu-id="a848e-570">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="a848e-571">Улучшенная поддержка CLONE_VFORK и CLONE_VM.</span><span class="sxs-lookup"><span data-stu-id="a848e-571">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="a848e-572">[GH 1878, 2615]</span><span class="sxs-lookup"><span data-stu-id="a848e-572">[GH 1878, 2615]</span></span>
- <span data-ttu-id="a848e-573">Пропуск драйверов фильтра TDI для сетевых операций WSL.</span><span class="sxs-lookup"><span data-stu-id="a848e-573">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="a848e-574">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="a848e-574">[GH 1554]</span></span>
- <span data-ttu-id="a848e-575">Дрвфс создает символических ссылок NT при выполнении определенных условий.</span><span class="sxs-lookup"><span data-stu-id="a848e-575">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="a848e-576">[GH 353, 1475, 2602]</span><span class="sxs-lookup"><span data-stu-id="a848e-576">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="a848e-577">Целевой объект ссылки должен быть относительным, не должен пересекать точки подключения или символических ссылок и должен существовать.</span><span class="sxs-lookup"><span data-stu-id="a848e-577">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="a848e-578">Пользователь должен иметь SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (обычно для этого требуется запустить WSL. exe с повышенными правами), если режим разработчика не включен.</span><span class="sxs-lookup"><span data-stu-id="a848e-578">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="a848e-579">Во всех остальных случаях Дрвфс по-прежнему создает WSL символических ссылок.</span><span class="sxs-lookup"><span data-stu-id="a848e-579">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="a848e-580">Разрешить одновременное выполнение экземпляров WSL с повышенными привилегиями и без повышенных привилегий.</span><span class="sxs-lookup"><span data-stu-id="a848e-580">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="a848e-581">Поддержка/proc/sys/kernel/yama/ptrace_scope</span><span class="sxs-lookup"><span data-stu-id="a848e-581">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="a848e-582">Добавьте вслпас в WSL <-> преобразования пути Windows.</span><span class="sxs-lookup"><span data-stu-id="a848e-582">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="a848e-583">[GH 522, 1243, 1834, 2327, et al.]</span><span class="sxs-lookup"><span data-stu-id="a848e-583">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="a848e-584">Консоль</span><span class="sxs-lookup"><span data-stu-id="a848e-584">Console</span></span>
- <span data-ttu-id="a848e-585">Нет исправлений.</span><span class="sxs-lookup"><span data-stu-id="a848e-585">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-586">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-586">LTP Results:</span></span>
<span data-ttu-id="a848e-587">Выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="a848e-587">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="a848e-588">Сборка 17040</span><span class="sxs-lookup"><span data-stu-id="a848e-588">Build 17040</span></span>

<span data-ttu-id="a848e-589">Общие сведения о Windows в сборке 17040 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span><span class="sxs-lookup"><span data-stu-id="a848e-589">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-590">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-590">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="a848e-591">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-591">WSL</span></span>
- <span data-ttu-id="a848e-592">Нет исправлений с 17035.</span><span class="sxs-lookup"><span data-stu-id="a848e-592">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="a848e-593">Консоль</span><span class="sxs-lookup"><span data-stu-id="a848e-593">Console</span></span>
- <span data-ttu-id="a848e-594">Нет исправлений с 17035.</span><span class="sxs-lookup"><span data-stu-id="a848e-594">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-595">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-595">LTP Results:</span></span>
<span data-ttu-id="a848e-596">Выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="a848e-596">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="a848e-597">Сборка 17035</span><span class="sxs-lookup"><span data-stu-id="a848e-597">Build 17035</span></span>

<span data-ttu-id="a848e-598">Общие сведения о Windows в сборке 17035 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span><span class="sxs-lookup"><span data-stu-id="a848e-598">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-599">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-599">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="a848e-600">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-600">WSL</span></span>
- <span data-ttu-id="a848e-601">Иногда не удается получить доступ к файлам в Дрвфс с помощью ЕИНВАЛ.</span><span class="sxs-lookup"><span data-stu-id="a848e-601">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="a848e-602">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="a848e-602">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="a848e-603">Консоль</span><span class="sxs-lookup"><span data-stu-id="a848e-603">Console</span></span>
- <span data-ttu-id="a848e-604">Некоторые потери цвета при вставке или удалении строк в режиме VT.</span><span class="sxs-lookup"><span data-stu-id="a848e-604">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-605">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-605">LTP Results:</span></span>
<span data-ttu-id="a848e-606">Выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="a848e-606">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="a848e-607">Сборка 17025</span><span class="sxs-lookup"><span data-stu-id="a848e-607">Build 17025</span></span>

<span data-ttu-id="a848e-608">Общие сведения о Windows в сборке 17025 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span><span class="sxs-lookup"><span data-stu-id="a848e-608">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-609">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-609">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="a848e-610">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-610">WSL</span></span>
- <span data-ttu-id="a848e-611">Запуск начальных процессов в новой группе процессов переднего плана [GH 1653, 2510].</span><span class="sxs-lookup"><span data-stu-id="a848e-611">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="a848e-612">Исправления СИГХУП доставки [GH 2496].</span><span class="sxs-lookup"><span data-stu-id="a848e-612">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="a848e-613">Создать имя виртуального моста по умолчанию, если оно не указано [GH 2497].</span><span class="sxs-lookup"><span data-stu-id="a848e-613">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="a848e-614">Реализуйте/proc/sys/kernel/Random/boot_id [GH 2518].</span><span class="sxs-lookup"><span data-stu-id="a848e-614">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="a848e-615">Дополнительные исправления взаимодействия stdout/stderr pipe.</span><span class="sxs-lookup"><span data-stu-id="a848e-615">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="a848e-616">Заглушка системного вызова синкфс.</span><span class="sxs-lookup"><span data-stu-id="a848e-616">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="a848e-617">Консоль</span><span class="sxs-lookup"><span data-stu-id="a848e-617">Console</span></span>
- <span data-ttu-id="a848e-618">Исправление входного перевода VT для консолей сторонних разработчиков [GH 111]</span><span class="sxs-lookup"><span data-stu-id="a848e-618">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-619">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-619">LTP Results:</span></span>
<span data-ttu-id="a848e-620">Выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="a848e-620">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="a848e-621">Сборка 17017</span><span class="sxs-lookup"><span data-stu-id="a848e-621">Build 17017</span></span>

<span data-ttu-id="a848e-622">Общие сведения о Windows в сборке 17017 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span><span class="sxs-lookup"><span data-stu-id="a848e-622">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-623">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-623">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="a848e-624">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-624">WSL</span></span>
- <span data-ttu-id="a848e-625">Пропуск пустых заголовков программы ELF [GH 330].</span><span class="sxs-lookup"><span data-stu-id="a848e-625">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="a848e-626">Разрешить Лксссманажер создавать экземпляры WSL для неинтерактивных пользователей (поддержка SSH и запланированных задач) [GH 777, 1602].</span><span class="sxs-lookup"><span data-stu-id="a848e-626">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="a848e-627">Поддержка сценариев WSL-> Win32-> WSL ("порождение") [GH 1228].</span><span class="sxs-lookup"><span data-stu-id="a848e-627">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="a848e-628">Ограниченная поддержка завершения работы консольных приложений, вызванных через взаимодействие [GH 1614].</span><span class="sxs-lookup"><span data-stu-id="a848e-628">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="a848e-629">Поддержка параметров подключения для девптс [GH 1948].</span><span class="sxs-lookup"><span data-stu-id="a848e-629">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="a848e-630">Птраце, блокирующий дочерний запуск [GH 2333].</span><span class="sxs-lookup"><span data-stu-id="a848e-630">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="a848e-631">В ЕПОЛЛЕТ отсутствуют некоторые события [GH 2462].</span><span class="sxs-lookup"><span data-stu-id="a848e-631">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="a848e-632">Возвращайте дополнительные данные для PTRACE_GETSIGINFO.</span><span class="sxs-lookup"><span data-stu-id="a848e-632">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="a848e-633">Повышение уровня с помощью лсик дает неверные результаты.</span><span class="sxs-lookup"><span data-stu-id="a848e-633">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="a848e-634">Устранение некоторых зависаний приложения Win32 Interop, ожидание входных данных в канале, который больше не содержит данные.</span><span class="sxs-lookup"><span data-stu-id="a848e-634">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="a848e-635">Поддержка O_ASYNC для файлов TTY/Pty.</span><span class="sxs-lookup"><span data-stu-id="a848e-635">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="a848e-636">Дополнительные улучшения и исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="a848e-636">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="a848e-637">Консоль</span><span class="sxs-lookup"><span data-stu-id="a848e-637">Console</span></span>
- <span data-ttu-id="a848e-638">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="a848e-638">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-639">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-639">LTP Results:</span></span>
<span data-ttu-id="a848e-640">Выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="a848e-640">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="a848e-641">Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="a848e-641">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="a848e-642">Сборка 16288</span><span class="sxs-lookup"><span data-stu-id="a848e-642">Build 16288</span></span>

<span data-ttu-id="a848e-643">Общие сведения о Windows в сборке 16288 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span><span class="sxs-lookup"><span data-stu-id="a848e-643">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-644">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-644">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="a848e-645">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-645">WSL</span></span>
- <span data-ttu-id="a848e-646">Правильная инициализация и создание отчетов о UID, GID и режиме для дескрипторов файлов сокетов [GH 2490]</span><span class="sxs-lookup"><span data-stu-id="a848e-646">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="a848e-647">Дополнительные улучшения и исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="a848e-647">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="a848e-648">Консоль</span><span class="sxs-lookup"><span data-stu-id="a848e-648">Console</span></span>
- <span data-ttu-id="a848e-649">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="a848e-649">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-650">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-650">LTP Results:</span></span>
<span data-ttu-id="a848e-651">Без изменений с 16273</span><span class="sxs-lookup"><span data-stu-id="a848e-651">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="a848e-652">Сборка 16278</span><span class="sxs-lookup"><span data-stu-id="a848e-652">Build 16278</span></span>

<span data-ttu-id="a848e-653">Общие сведения о Windows в сборке 162738 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span><span class="sxs-lookup"><span data-stu-id="a848e-653">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-654">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-654">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="a848e-655">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-655">WSL</span></span>
- <span data-ttu-id="a848e-656">Явное отмена сопоставления сопоставленных представлений разделов с файлами при разрыве состояния LX MM [GH 2415]</span><span class="sxs-lookup"><span data-stu-id="a848e-656">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="a848e-657">Дополнительные улучшения и исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="a848e-657">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="a848e-658">Консоль</span><span class="sxs-lookup"><span data-stu-id="a848e-658">Console</span></span>
- <span data-ttu-id="a848e-659">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="a848e-659">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-660">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-660">LTP Results:</span></span>
<span data-ttu-id="a848e-661">Без изменений с 16273</span><span class="sxs-lookup"><span data-stu-id="a848e-661">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="a848e-662">Сборка 16275</span><span class="sxs-lookup"><span data-stu-id="a848e-662">Build 16275</span></span>

<span data-ttu-id="a848e-663">Общие сведения о Windows в сборке 162735 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span><span class="sxs-lookup"><span data-stu-id="a848e-663">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-664">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-664">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="a848e-665">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-665">WSL</span></span>
- <span data-ttu-id="a848e-666">Нет изменений, связанных с WSL в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="a848e-666">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="a848e-667">Консоль</span><span class="sxs-lookup"><span data-stu-id="a848e-667">Console</span></span>
- <span data-ttu-id="a848e-668">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="a848e-668">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-669">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-669">LTP Results:</span></span>
<span data-ttu-id="a848e-670">Без изменений с 16273</span><span class="sxs-lookup"><span data-stu-id="a848e-670">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="a848e-671">Сборка 16273</span><span class="sxs-lookup"><span data-stu-id="a848e-671">Build 16273</span></span>

<span data-ttu-id="a848e-672">Общие сведения о Windows в сборке 16273 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span><span class="sxs-lookup"><span data-stu-id="a848e-672">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-673">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-673">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="a848e-674">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-674">WSL</span></span>
- <span data-ttu-id="a848e-675">Исправлена проблема, при которой Дрвфс иногда сообщает о неправильном типе файлов для каталогов [GH 2392]</span><span class="sxs-lookup"><span data-stu-id="a848e-675">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="a848e-676">Разрешить создание сокетов NETLINK_KOBJECT_UEVENT для разблокирования программ, использующих уевент [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span><span class="sxs-lookup"><span data-stu-id="a848e-676">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="a848e-677">Добавлена поддержка неблокирующего подключения [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span><span class="sxs-lookup"><span data-stu-id="a848e-677">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="a848e-678">Реализация флага вызова системы клонирования CLONE_FS [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="a848e-678">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="a848e-679">Устранение проблем, связанных с неправильной обработкой вкладок или кавычек в Interop в NT [GH 1625, 2164]</span><span class="sxs-lookup"><span data-stu-id="a848e-679">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="a848e-680">Устранение ошибки отказа в доступе при попытке повторного запуска экземпляров WSL [GH 651, 2095]</span><span class="sxs-lookup"><span data-stu-id="a848e-680">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="a848e-681">Реализация операций футекс FUTEX_REQUEUE и FUTEX_CMP_REQUEUE [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="a848e-681">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="a848e-682">Исправление разрешений для различных файлов сисфс [GH 2214]</span><span class="sxs-lookup"><span data-stu-id="a848e-682">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="a848e-683">Исправление стека Haskell для зависания во время установки [GH 2290]</span><span class="sxs-lookup"><span data-stu-id="a848e-683">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="a848e-684">Реализуйте binfmt_misc "O" и "P" с флагами [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="a848e-684">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="a848e-685">Add/прок/СИС/Кернел/шммакс/шммни &/среадс-Макс [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="a848e-685">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="a848e-686">Добавление частичной поддержки для системного вызова ioprio_set [GH 498]</span><span class="sxs-lookup"><span data-stu-id="a848e-686">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="a848e-687">Заглушка SO_REUSEPORT & Добавление поддержки SO_PASSCRED для сокетов нетлинк [GH 69]</span><span class="sxs-lookup"><span data-stu-id="a848e-687">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="a848e-688">Возвращайте различные коды ошибок из Регистердистрибуитон, если дистрибутив в данный момент устанавливается или удаляется.</span><span class="sxs-lookup"><span data-stu-id="a848e-688">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="a848e-689">Разрешить отмену регистрации частично установленных дистрибутивов WSL через вслконфиг. exe</span><span class="sxs-lookup"><span data-stu-id="a848e-689">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="a848e-690">Устранение ошибки проверки сокета Python с UDP:: MSG_PEEK</span><span class="sxs-lookup"><span data-stu-id="a848e-690">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="a848e-691">Дополнительные улучшения и исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="a848e-691">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="a848e-692">Консоль</span><span class="sxs-lookup"><span data-stu-id="a848e-692">Console</span></span>
- <span data-ttu-id="a848e-693">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="a848e-693">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-694">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-694">LTP Results:</span></span>
<span data-ttu-id="a848e-695">Всего тестов: 1904</span><span class="sxs-lookup"><span data-stu-id="a848e-695">Total Tests: 1904</span></span><br/>
<span data-ttu-id="a848e-696">Всего пропущенных тестов: 209</span><span class="sxs-lookup"><span data-stu-id="a848e-696">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="a848e-697">Всего сбоев: 229</span><span class="sxs-lookup"><span data-stu-id="a848e-697">Total Failures: 229</span></span><br/>
[<span data-ttu-id="a848e-698">Журналы тестового запуска ЛТП</span><span class="sxs-lookup"><span data-stu-id="a848e-698">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="a848e-699">Сборка 16257</span><span class="sxs-lookup"><span data-stu-id="a848e-699">Build 16257</span></span>

<span data-ttu-id="a848e-700">Общие сведения о Windows в сборке 16257 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span><span class="sxs-lookup"><span data-stu-id="a848e-700">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-701">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-701">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="a848e-702">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-702">WSL</span></span>
- <span data-ttu-id="a848e-703">Реализация системного вызова prlimit64</span><span class="sxs-lookup"><span data-stu-id="a848e-703">Implement prlimit64 system call</span></span>
- <span data-ttu-id="a848e-704">Добавлена поддержка него команду ulimit-n (сетрлимит RLIMIT_NOFILE) [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="a848e-704">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="a848e-705">Заглушка MSG_MORE для TCP-сокетов [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="a848e-705">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="a848e-706">Исправление недопустимого вспомогательного векторного поведения AT_EXECFN [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="a848e-706">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="a848e-707">Исправьте поведение копирования и вставки для Console/TTY и добавьте более полную обработку буфера [GH 2204, 2131]</span><span class="sxs-lookup"><span data-stu-id="a848e-707">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="a848e-708">Установка AT_SECURE в дополнительном векторе для программ Set-User-ID и Set-Group-ID [GH 2031]</span><span class="sxs-lookup"><span data-stu-id="a848e-708">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="a848e-709">Псуедо — Главная конечная точка терминала не обрабатывает ТИОКПГРП [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="a848e-709">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="a848e-710">Исправление лсик для перемотки каталогов в Лксфс [GH 2310]</span><span class="sxs-lookup"><span data-stu-id="a848e-710">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="a848e-711">/Дев/птмкс блокируется после интенсивного использования [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="a848e-711">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="a848e-712">Дополнительные улучшения и исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="a848e-712">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="a848e-713">Консоль</span><span class="sxs-lookup"><span data-stu-id="a848e-713">Console</span></span>
- <span data-ttu-id="a848e-714">Исправление для горизонтальных строк и подчеркивания везде [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="a848e-714">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="a848e-715">Исправление порядка процессов изменилось, NPM закрыть [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="a848e-715">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="a848e-716">Добавлена новая цветовая схема: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="a848e-716">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-717">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-717">LTP Results:</span></span>
<span data-ttu-id="a848e-718">Без изменений с 16251</span><span class="sxs-lookup"><span data-stu-id="a848e-718">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="a848e-719">Поддержка syscall</span><span class="sxs-lookup"><span data-stu-id="a848e-719">Syscall Support</span></span>
<span data-ttu-id="a848e-720">Ниже приведен список новых или улучшенных syscall, которые имеют некоторую реализацию в WSL.</span><span class="sxs-lookup"><span data-stu-id="a848e-720">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="a848e-721">Syscall в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="a848e-721">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="a848e-722">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="a848e-722">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[<span data-ttu-id="a848e-723">Ошибка GitHub 2392: Папки Windows, не распознаваемые WSL...</span><span class="sxs-lookup"><span data-stu-id="a848e-723">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="a848e-724">В сборке 16257 при перечислении файлов и папок Windows через `/mnt/c/...`возникли проблемы с WSL.</span><span class="sxs-lookup"><span data-stu-id="a848e-724">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="a848e-725">Эта проблема исправлена и должна быть выпущена в процессе предварительной оценки в течение недели началом 8/14/2017.</span><span class="sxs-lookup"><span data-stu-id="a848e-725">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="a848e-726">Сборка 16251</span><span class="sxs-lookup"><span data-stu-id="a848e-726">Build 16251</span></span>

<span data-ttu-id="a848e-727">Общие сведения о Windows в сборке 16251 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span><span class="sxs-lookup"><span data-stu-id="a848e-727">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-728">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-728">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="a848e-729">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-729">WSL</span></span>
- <span data-ttu-id="a848e-730">Удаление тега бета-версии из дополнительного компонента WSL. Дополнительные сведения см. в [записи блога](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) .</span><span class="sxs-lookup"><span data-stu-id="a848e-730">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="a848e-731">Правильно инициализировать сохраненные-Set UID и GID для двоичных файлов Set-User-ID и Set-Group-ID в Exec [GH 962, 1415, 2072]</span><span class="sxs-lookup"><span data-stu-id="a848e-731">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="a848e-732">Добавлена поддержка птраце PTRACE_O_TRACEEXIT [GH 555].</span><span class="sxs-lookup"><span data-stu-id="a848e-732">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="a848e-733">Добавлена поддержка птраце PTRACE_GETFPREGS и PTRACE_GETREGSET с NT_FPREGSET [GH 555].</span><span class="sxs-lookup"><span data-stu-id="a848e-733">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="a848e-734">Исправлена птраце для отмены пропущенных сигналов</span><span class="sxs-lookup"><span data-stu-id="a848e-734">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="a848e-735">Дополнительные улучшения и исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="a848e-735">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="a848e-736">Консоль</span><span class="sxs-lookup"><span data-stu-id="a848e-736">Console</span></span>
- <span data-ttu-id="a848e-737">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="a848e-737">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-738">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-738">LTP Results:</span></span>
<span data-ttu-id="a848e-739">Число тестов передачи: 768</span><span class="sxs-lookup"><span data-stu-id="a848e-739">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="a848e-740">Число неудачных тестов: 244</span><span class="sxs-lookup"><span data-stu-id="a848e-740">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="a848e-741">Число пропущенных тестов: 96</span><span class="sxs-lookup"><span data-stu-id="a848e-741">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="a848e-742">Журналы тестового запуска ЛТП</span><span class="sxs-lookup"><span data-stu-id="a848e-742">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="a848e-743">Сборка 16241</span><span class="sxs-lookup"><span data-stu-id="a848e-743">Build 16241</span></span>

<span data-ttu-id="a848e-744">Общие сведения о Windows в сборке 16241 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span><span class="sxs-lookup"><span data-stu-id="a848e-744">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-745">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-745">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="a848e-746">WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-746">WSL</span></span>
- <span data-ttu-id="a848e-747">Нет изменений, связанных с WSL в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="a848e-747">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="a848e-748">Консоль</span><span class="sxs-lookup"><span data-stu-id="a848e-748">Console</span></span>
- <span data-ttu-id="a848e-749">Исправление для вывода неправильного символа для пересечением DEC, первоначально сообщаемым [здесь](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span><span class="sxs-lookup"><span data-stu-id="a848e-749">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="a848e-750">Исправление отсутствия отображаемого текста в кодовой странице 65001 (UTF8)</span><span class="sxs-lookup"><span data-stu-id="a848e-750">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="a848e-751">Не переносите изменения, внесенные в значения RGB одного цвета, в другие части палитры при изменении выбора.</span><span class="sxs-lookup"><span data-stu-id="a848e-751">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="a848e-752">Это сделает страницу свойств консоли гораздо более простой в использовании.</span><span class="sxs-lookup"><span data-stu-id="a848e-752">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="a848e-753">Ctrl + S не работает правильно</span><span class="sxs-lookup"><span data-stu-id="a848e-753">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="a848e-754">Нежирный/-Dim полностью отсутствует в кодах Escape-кодов ANSI [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="a848e-754">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="a848e-755">Консоль не поддерживает правильную поддержку цветовых тем vim [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="a848e-755">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="a848e-756">Не удается вставить определенные символы [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="a848e-756">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="a848e-757">Изменение размера перекомпоновки ведет к необычному взаимодействии с изменением размера окна bash, когда оно находится в строке редактирования или командной строки [GH Конему 1123]</span><span class="sxs-lookup"><span data-stu-id="a848e-757">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="a848e-758">Ctrl-L оставляет экран грязным [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="a848e-758">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="a848e-759">Ошибка отрисовки консоли при отображении VT on HDPI [GH 1907]</span><span class="sxs-lookup"><span data-stu-id="a848e-759">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="a848e-760">Жапансесе символы выглядят странно с символом Юникода U + 30FB [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="a848e-760">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="a848e-761">Дополнительные улучшения и исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="a848e-761">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="a848e-762">Сборка 16237</span><span class="sxs-lookup"><span data-stu-id="a848e-762">Build 16237</span></span>

<span data-ttu-id="a848e-763">Общие сведения о Windows в сборке 16237 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span><span class="sxs-lookup"><span data-stu-id="a848e-763">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-764">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-764">Fixed</span></span>
- <span data-ttu-id="a848e-765">Использовать атрибуты по умолчанию для файлов без EAs в лксфс (корневая папка, корневая папка, 0000)</span><span class="sxs-lookup"><span data-stu-id="a848e-765">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="a848e-766">Добавлена поддержка распределений, использующих расширенные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="a848e-766">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="a848e-767">Исправлять заполнение для записей, возвращаемых уровнями и getdents64</span><span class="sxs-lookup"><span data-stu-id="a848e-767">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="a848e-768">Устранение ошибки проверки разрешений для системного вызова шмктл SHM_STAT [GH 2068]</span><span class="sxs-lookup"><span data-stu-id="a848e-768">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="a848e-769">Исправлено неправильное начальное состояние еполл для телетайпы [GH 2231]</span><span class="sxs-lookup"><span data-stu-id="a848e-769">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="a848e-770">Исправление Дрвфс реаддир не возвращает все записи [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="a848e-770">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="a848e-771">Исправление Лксфс реаддир при разрыве связи с файлами [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="a848e-771">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="a848e-772">Разрешить повторное открытие несвязанных файлов дрвфс через прокфс</span><span class="sxs-lookup"><span data-stu-id="a848e-772">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="a848e-773">Добавлено глобальное переопределение ключа реестра для отключения функций WSL (монтирование взаимодействия и диска)</span><span class="sxs-lookup"><span data-stu-id="a848e-773">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="a848e-774">Исправление неправильного счетчика блокировок в "stat" для Дрвфс (и Лксфс) [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="a848e-774">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="a848e-775">Дополнительные улучшения и исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="a848e-775">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="a848e-776">Сборка 16232</span><span class="sxs-lookup"><span data-stu-id="a848e-776">Build 16232</span></span>

<span data-ttu-id="a848e-777">Общие сведения о Windows в сборке 16232 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span><span class="sxs-lookup"><span data-stu-id="a848e-777">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-778">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-778">Fixed</span></span>
- <span data-ttu-id="a848e-779">Нет изменений, связанных с WSL в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="a848e-779">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="a848e-780">Сборка 16226</span><span class="sxs-lookup"><span data-stu-id="a848e-780">Build 16226</span></span>

<span data-ttu-id="a848e-781">Общие сведения о Windows в сборке 16226 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span><span class="sxs-lookup"><span data-stu-id="a848e-781">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-782">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-782">Fixed</span></span>
- <span data-ttu-id="a848e-783">Поддержка ксаттр, связанная с syscall (жетксаттр, сетксаттр, листксаттр, ремовексаттр).</span><span class="sxs-lookup"><span data-stu-id="a848e-783">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="a848e-784">Security. капаблити ксаттр support.</span><span class="sxs-lookup"><span data-stu-id="a848e-784">security.capablity xattr support.</span></span>
- <span data-ttu-id="a848e-785">Улучшенная совместимость с некоторыми файловыми системами и фильтрами, включая серверы SMB, отличные от MS.</span><span class="sxs-lookup"><span data-stu-id="a848e-785">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="a848e-786">[GH #1952]</span><span class="sxs-lookup"><span data-stu-id="a848e-786">[GH #1952]</span></span>
- <span data-ttu-id="a848e-787">Улучшенная поддержка заполнителей OneDrive, заполнители GVFS и сжатия сжатых файлов ОС.</span><span class="sxs-lookup"><span data-stu-id="a848e-787">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="a848e-788">Дополнительные улучшения и исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="a848e-788">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="a848e-789">Сборка 16215</span><span class="sxs-lookup"><span data-stu-id="a848e-789">Build 16215</span></span>

<span data-ttu-id="a848e-790">Общие сведения о Windows в сборке 16215 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span><span class="sxs-lookup"><span data-stu-id="a848e-790">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-791">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-791">Fixed</span></span>
- <span data-ttu-id="a848e-792">Для WSL больше не требуется режим разработчика.</span><span class="sxs-lookup"><span data-stu-id="a848e-792">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="a848e-793">Поддержка соединений каталогов в дрвфс.</span><span class="sxs-lookup"><span data-stu-id="a848e-793">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="a848e-794">Обрабатывает удаление пакетов appx WSL Distribution.</span><span class="sxs-lookup"><span data-stu-id="a848e-794">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="a848e-795">Обновите прокфс, чтобы отобразить частные и общие сопоставления.</span><span class="sxs-lookup"><span data-stu-id="a848e-795">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="a848e-796">Добавьте возможность для вслконфиг. exe, чтобы очистить частично установленные или удаляемые дистрибутивы.</span><span class="sxs-lookup"><span data-stu-id="a848e-796">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="a848e-797">Добавлена поддержка IP_MTU_DISCOVER для сокетов TCP.</span><span class="sxs-lookup"><span data-stu-id="a848e-797">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="a848e-798">[GH 1639, 2115, 2205]</span><span class="sxs-lookup"><span data-stu-id="a848e-798">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="a848e-799">Вывести семейство протоколов для маршрутов к AF_INADDR.</span><span class="sxs-lookup"><span data-stu-id="a848e-799">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="a848e-800">Улучшения последовательного устройства [GH 1929].</span><span class="sxs-lookup"><span data-stu-id="a848e-800">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="a848e-801">Сборка 16199</span><span class="sxs-lookup"><span data-stu-id="a848e-801">Build 16199</span></span>

<span data-ttu-id="a848e-802">Общие сведения о Windows в сборке 16199 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span><span class="sxs-lookup"><span data-stu-id="a848e-802">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-803">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-803">Fixed</span></span>
- <span data-ttu-id="a848e-804">Нет WSL, связанных с изменениями в этих выпусках.</span><span class="sxs-lookup"><span data-stu-id="a848e-804">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="a848e-805">Сборка 16193</span><span class="sxs-lookup"><span data-stu-id="a848e-805">Build 16193</span></span>

<span data-ttu-id="a848e-806">Общие сведения о Windows в сборке 16193 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span><span class="sxs-lookup"><span data-stu-id="a848e-806">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-807">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-807">Fixed</span></span>
- <span data-ttu-id="a848e-808">Состояние гонки между отправкой СИГКОНТ и среадграуп (GH 1973])</span><span class="sxs-lookup"><span data-stu-id="a848e-808">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="a848e-809">Замените устройства tty и PTY на Report FILE_DEVICE_NAMED_PIPE вместо FILE_DEVICE_CONSOLE [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="a848e-809">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="a848e-810">Исправление SSH для IP_OPTIONS</span><span class="sxs-lookup"><span data-stu-id="a848e-810">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="a848e-811">Перемещено подключение Дрвфс к управляющей программе init [GH 1862, 1968, 1767, 1933]</span><span class="sxs-lookup"><span data-stu-id="a848e-811">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="a848e-812">Добавлена поддержка в Дрвфс для следующих символических ссылок NT.</span><span class="sxs-lookup"><span data-stu-id="a848e-812">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="a848e-813">Сборка 16184</span><span class="sxs-lookup"><span data-stu-id="a848e-813">Build 16184</span></span>

<span data-ttu-id="a848e-814">Общие сведения о Windows в сборке 16184 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span><span class="sxs-lookup"><span data-stu-id="a848e-814">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-815">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-815">Fixed</span></span>
- <span data-ttu-id="a848e-816">Удалена задача обслуживания пакета apt (лксрун. exe/Update)</span><span class="sxs-lookup"><span data-stu-id="a848e-816">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="a848e-817">Фиксированные выходные данные не отображаются в процессах Windows в Node. js [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="a848e-817">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="a848e-818">Смягчить требования к выравниванию в лкскоре [GH 1794]</span><span class="sxs-lookup"><span data-stu-id="a848e-818">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="a848e-819">Исправлена обработка флага AT_EMPTY_PATH в число ключей системных вызовов.</span><span class="sxs-lookup"><span data-stu-id="a848e-819">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="a848e-820">Исправлена проблема, когда удаление файлов Дрвфс с открытыми дескрипторами приведет к неопределенному поведению файла [GH 544, 966, 1357, 1535, 1615]</span><span class="sxs-lookup"><span data-stu-id="a848e-820">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="a848e-821">Теперь/etc/hosts будет наследовать записи из файла узлов Windows (%windir%\System32\Drivers\Etc\hosts) [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="a848e-821">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="a848e-822">Сборка 16179</span><span class="sxs-lookup"><span data-stu-id="a848e-822">Build 16179</span></span>

<span data-ttu-id="a848e-823">Общие сведения о Windows в сборке 16179 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span><span class="sxs-lookup"><span data-stu-id="a848e-823">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-824">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-824">Fixed</span></span>
- <span data-ttu-id="a848e-825">В этой неделе нет изменений WSL.</span><span class="sxs-lookup"><span data-stu-id="a848e-825">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="a848e-826">Сборка 16176</span><span class="sxs-lookup"><span data-stu-id="a848e-826">Build 16176</span></span>

<span data-ttu-id="a848e-827">Общие сведения о Windows в сборке 16176 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span><span class="sxs-lookup"><span data-stu-id="a848e-827">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-828">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-828">Fixed</span></span>

- [<span data-ttu-id="a848e-829">Включенная поддержка последовательного порта</span><span class="sxs-lookup"><span data-stu-id="a848e-829">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="a848e-830">Добавлен параметр IP-сокета IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="a848e-830">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="a848e-831">Реализованная функция пвритев (при передаче файла в nginx/PHP-FPM) [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="a848e-831">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="a848e-832">Добавлены параметры IP-сокета IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990].</span><span class="sxs-lookup"><span data-stu-id="a848e-832">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="a848e-833">Поддержка параметра сокета IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="a848e-833">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="a848e-834">Добавлен параметр сокета _MTU IP (V6) для узла приложений, Traceroute, изучение, nslookup, узел</span><span class="sxs-lookup"><span data-stu-id="a848e-834">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="a848e-835">Добавлен параметр IP-сокета IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="a848e-835">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="a848e-836">Улучшения файловой системы</span><span class="sxs-lookup"><span data-stu-id="a848e-836">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="a848e-837">Разрешить подключение UNC-путей</span><span class="sxs-lookup"><span data-stu-id="a848e-837">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="a848e-838">Включение поддержки CDFS в дрвфс</span><span class="sxs-lookup"><span data-stu-id="a848e-838">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="a848e-839">Правильная работа разрешений для сетевых файловых систем в дрвфс</span><span class="sxs-lookup"><span data-stu-id="a848e-839">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="a848e-840">Добавлена поддержка удаленных дисков для дрвфс.</span><span class="sxs-lookup"><span data-stu-id="a848e-840">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="a848e-841">Включение поддержки файловой системы FAT в дрвфс</span><span class="sxs-lookup"><span data-stu-id="a848e-841">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="a848e-842">Дополнительные исправления и улучшения</span><span class="sxs-lookup"><span data-stu-id="a848e-842">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-843">Результаты ЛТП</span><span class="sxs-lookup"><span data-stu-id="a848e-843">LTP Results</span></span>
<span data-ttu-id="a848e-844">Нет изменений с 15042</span><span class="sxs-lookup"><span data-stu-id="a848e-844">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="a848e-845">Сборка 16170</span><span class="sxs-lookup"><span data-stu-id="a848e-845">Build 16170</span></span>

<span data-ttu-id="a848e-846">Общие сведения о Windows в сборке 16170 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span><span class="sxs-lookup"><span data-stu-id="a848e-846">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="a848e-847">Мы выпустили новую [запись блога](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) , в которой обсуждаются наши усилия по тестированию WSL.</span><span class="sxs-lookup"><span data-stu-id="a848e-847">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="a848e-848">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-848">Fixed</span></span>

- <span data-ttu-id="a848e-849">Поддержка параметра сокета IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="a848e-849">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="a848e-850">Добавлена поддержка PTRACE_OLDSETOPTIONS.</span><span class="sxs-lookup"><span data-stu-id="a848e-850">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="a848e-851">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="a848e-851">[GH 1692]</span></span>
- <span data-ttu-id="a848e-852">Дополнительные исправления и улучшения</span><span class="sxs-lookup"><span data-stu-id="a848e-852">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-853">Результаты ЛТП</span><span class="sxs-lookup"><span data-stu-id="a848e-853">LTP Results</span></span>
<span data-ttu-id="a848e-854">Нет изменений с 15042</span><span class="sxs-lookup"><span data-stu-id="a848e-854">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="a848e-855">Сборка 15046 в Windows 10 Creators Update</span><span class="sxs-lookup"><span data-stu-id="a848e-855">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="a848e-856">В Windows 10 больше не WSL исправлений или компонентов, запланированных для включения в обновление авторов.</span><span class="sxs-lookup"><span data-stu-id="a848e-856">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="a848e-857">Заметки о выпуске WSL будут возобновлены в ближайшие недели для дополнений, предназначенных для следующих основных Центр обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="a848e-857">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="a848e-858">Общие сведения о Windows, посвященные сборке 15046 и будущим выпускам Insider, см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span><span class="sxs-lookup"><span data-stu-id="a848e-858">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="a848e-859">Сборка 15042</span><span class="sxs-lookup"><span data-stu-id="a848e-859">Build 15042</span></span>

<span data-ttu-id="a848e-860">Общие сведения о Windows в сборке 15042 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span><span class="sxs-lookup"><span data-stu-id="a848e-860">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-861">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-861">Fixed</span></span>

- <span data-ttu-id="a848e-862">Устранение взаимоблокировки при удалении пути, завершающего ".."</span><span class="sxs-lookup"><span data-stu-id="a848e-862">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="a848e-863">Исправлена проблема, при которой ФИОНБИО не вернул 0 при успешном выполнении [GH 1683]</span><span class="sxs-lookup"><span data-stu-id="a848e-863">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="a848e-864">Исправлена проблема с чтением inetных сокетов датаграмм нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="a848e-864">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="a848e-865">Исправление возможной взаимоблокировки из-за состояния гонки в дрвфс иноде Lookup [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="a848e-865">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="a848e-866">Расширенная поддержка вспомогательных данных сокетов UNIX; SCM_CREDENTIALS и SCM_RIGHTS [GH 514, 613, 1326]</span><span class="sxs-lookup"><span data-stu-id="a848e-866">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="a848e-867">Дополнительные исправления и улучшения</span><span class="sxs-lookup"><span data-stu-id="a848e-867">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-868">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-868">LTP Results:</span></span>
<span data-ttu-id="a848e-869">Число пройденных тестов: 737</span><span class="sxs-lookup"><span data-stu-id="a848e-869">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="a848e-870">Число непройденных (неудачных, пропущенных и т. д.): 255</span><span class="sxs-lookup"><span data-stu-id="a848e-870">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="a848e-871">Сборка 15031</span><span class="sxs-lookup"><span data-stu-id="a848e-871">Build 15031</span></span>

<span data-ttu-id="a848e-872">Общие сведения о Windows в сборке 15031 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span><span class="sxs-lookup"><span data-stu-id="a848e-872">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-873">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-873">Fixed</span></span>

- <span data-ttu-id="a848e-874">Исправлена ошибка, в которой время (2) будет ошибочно отличаться.</span><span class="sxs-lookup"><span data-stu-id="a848e-874">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="a848e-875">Исправлена и проблема, когда \* СИГПРОКМАСК syscall может повредить сигнальную маску.</span><span class="sxs-lookup"><span data-stu-id="a848e-875">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="a848e-876">Теперь верните полную длину командной строки в уведомлении о создании процесса WSL.</span><span class="sxs-lookup"><span data-stu-id="a848e-876">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="a848e-877">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="a848e-877">[GH 1632]</span></span>
- <span data-ttu-id="a848e-878">WSL теперь сообщает о выходе потока через птраце для GDB зависаний.</span><span class="sxs-lookup"><span data-stu-id="a848e-878">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="a848e-879">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="a848e-879">[GH 1196]</span></span>
- <span data-ttu-id="a848e-880">Исправлена ошибка, при которой ПТИС зависает после интенсивного ввода-вывода тмукс.</span><span class="sxs-lookup"><span data-stu-id="a848e-880">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="a848e-881">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="a848e-881">[GH 1358]</span></span>
- <span data-ttu-id="a848e-882">Фиксированная Проверка времени ожидания во многих системных вызовах (футекс, семтимедоп, пполл, сигтимедваит, итимер, timer_create)</span><span class="sxs-lookup"><span data-stu-id="a848e-882">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="a848e-883">Добавлена поддержка евентфд EFD_SEMAPHORE [GH 452].</span><span class="sxs-lookup"><span data-stu-id="a848e-883">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="a848e-884">Дополнительные исправления и улучшения</span><span class="sxs-lookup"><span data-stu-id="a848e-884">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-885">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-885">LTP Results:</span></span>
<span data-ttu-id="a848e-886">Число пройденных тестов: 737</span><span class="sxs-lookup"><span data-stu-id="a848e-886">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="a848e-887">Число непройденных (неудачных, пропущенных и т. д.): 255</span><span class="sxs-lookup"><span data-stu-id="a848e-887">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="a848e-888">Журналы тестового запуска ЛТП</span><span class="sxs-lookup"><span data-stu-id="a848e-888">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="a848e-889">Сборка 15025</span><span class="sxs-lookup"><span data-stu-id="a848e-889">Build 15025</span></span>

<span data-ttu-id="a848e-890">Общие сведения о Windows в сборке 15025 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span><span class="sxs-lookup"><span data-stu-id="a848e-890">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-891">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-891">Fixed</span></span>

- <span data-ttu-id="a848e-892">Исправление ошибки, которая нарушила grep 2,27 [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="a848e-892">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="a848e-893">Реализован флаг EFD_SEMAPHORE для eventfd2 syscall [GH 452]</span><span class="sxs-lookup"><span data-stu-id="a848e-893">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="a848e-894">Реализован/прок/[PID]/NET/ipv6_route [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="a848e-894">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="a848e-895">Поддержка управляемых сигналами операций ввода-вывода для сокетов потоков UNIX [GH 393, 68]</span><span class="sxs-lookup"><span data-stu-id="a848e-895">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="a848e-896">Поддержка F_GETPIPE_SZ и F_SETPIPE_SZ [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="a848e-896">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="a848e-897">Реализация реквммсг () syscall [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="a848e-897">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="a848e-898">Исправлена ошибка, при которой epoll_wait () не ожидал [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="a848e-898">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="a848e-899">Реализация/proc/version_signature</span><span class="sxs-lookup"><span data-stu-id="a848e-899">Implement /proc/version_signature</span></span>
- <span data-ttu-id="a848e-900">Tee syscall теперь возвращает ошибку, если оба дескриптора файлов ссылаются на один и тот же канал</span><span class="sxs-lookup"><span data-stu-id="a848e-900">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="a848e-901">Реализовано правильное поведение для SO_PEERCRED для сокетов UNIX</span><span class="sxs-lookup"><span data-stu-id="a848e-901">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="a848e-902">Исправлена ткилл syscall недопустимая обработка параметров</span><span class="sxs-lookup"><span data-stu-id="a848e-902">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="a848e-903">Изменения для увеличения преформаце дрвфс</span><span class="sxs-lookup"><span data-stu-id="a848e-903">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="a848e-904">Незначительное исправление для блокировки ввода-вывода Ruby</span><span class="sxs-lookup"><span data-stu-id="a848e-904">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="a848e-905">Исправлена реквмсг (), возвращающая ЕИНВАЛ для флага MSG_DONTWAIT для сокетов inet [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="a848e-905">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="a848e-906">Дополнительные исправления и улучшения</span><span class="sxs-lookup"><span data-stu-id="a848e-906">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-907">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-907">LTP Results:</span></span>
<span data-ttu-id="a848e-908">Число пройденных тестов: 732</span><span class="sxs-lookup"><span data-stu-id="a848e-908">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="a848e-909">Число непройденных (неудачных, пропущенных и т. д.): 255</span><span class="sxs-lookup"><span data-stu-id="a848e-909">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="a848e-910">Журналы тестового запуска ЛТП</span><span class="sxs-lookup"><span data-stu-id="a848e-910">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="a848e-911">Сборка 15019</span><span class="sxs-lookup"><span data-stu-id="a848e-911">Build 15019</span></span>

<span data-ttu-id="a848e-912">Общие сведения о Windows в сборке 15019 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span><span class="sxs-lookup"><span data-stu-id="a848e-912">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-913">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-913">Fixed</span></span>

- <span data-ttu-id="a848e-914">Исправлена ошибка, сообщающая о неправильном использовании ЦП в прокфс для таких средств, как Htop (GH 823, 945, 971).</span><span class="sxs-lookup"><span data-stu-id="a848e-914">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="a848e-915">При вызове Open () с O_TRUNC для существующего файла инотифи теперь создает IN_MODIFY перед IN_OPEN</span><span class="sxs-lookup"><span data-stu-id="a848e-915">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="a848e-916">Исправления в UNIX Socket жетсоккопт SO_ERROR для включения постгресс [GH 61, 1354]</span><span class="sxs-lookup"><span data-stu-id="a848e-916">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="a848e-917">Реализация/прок/СИС/нет/коре/сомаксконн для языка GO</span><span class="sxs-lookup"><span data-stu-id="a848e-917">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="a848e-918">APT — фоновая задача обновления пакета теперь запускается из представления в скрытом режиме</span><span class="sxs-lookup"><span data-stu-id="a848e-918">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="a848e-919">Очистите область для IPv6-адреса localhost (сбой пружины-Framework (Java)).</span><span class="sxs-lookup"><span data-stu-id="a848e-919">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="a848e-920">Дополнительные исправления и улучшения</span><span class="sxs-lookup"><span data-stu-id="a848e-920">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-921">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-921">LTP Results:</span></span>
<span data-ttu-id="a848e-922">Число пройденных тестов: 714</span><span class="sxs-lookup"><span data-stu-id="a848e-922">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="a848e-923">Число непройденных (неудачных, пропущенных и т. д.): 249</span><span class="sxs-lookup"><span data-stu-id="a848e-923">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="a848e-924">Журналы тестового запуска ЛТП</span><span class="sxs-lookup"><span data-stu-id="a848e-924">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="a848e-925">Сборка 15014</span><span class="sxs-lookup"><span data-stu-id="a848e-925">Build 15014</span></span>

<span data-ttu-id="a848e-926">Общие сведения о Windows в сборке 15014 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="a848e-926">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-927">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-927">Fixed</span></span>

- <span data-ttu-id="a848e-928">Ctrl + C теперь работает как задуманное</span><span class="sxs-lookup"><span data-stu-id="a848e-928">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="a848e-929">Htop и PS ауксв теперь показывают правильное использование ресурсов (GH #516)</span><span class="sxs-lookup"><span data-stu-id="a848e-929">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="a848e-930">Базовый перевод исключений NT в сигналы.</span><span class="sxs-lookup"><span data-stu-id="a848e-930">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="a848e-931">(GH #513)</span><span class="sxs-lookup"><span data-stu-id="a848e-931">(GH #513)</span></span>
- <span data-ttu-id="a848e-932">фаллокате теперь завершается с ошибкой ЕНОСПК при нехватке пространства вместо ЕИНВАЛ (GH #1571)</span><span class="sxs-lookup"><span data-stu-id="a848e-932">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="a848e-933">Добавлен/прок/СИС/Кернел/сем.</span><span class="sxs-lookup"><span data-stu-id="a848e-933">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="a848e-934">Реализованные системные вызовы семоп и семтимедоп</span><span class="sxs-lookup"><span data-stu-id="a848e-934">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="a848e-935">Исправлены ошибки nslookup с параметром сокета IP_RECVTOS & IPV6_RECVTCLASS (GH 69)</span><span class="sxs-lookup"><span data-stu-id="a848e-935">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="a848e-936">Поддержка параметров сокета IP_RECVTTL и IPV6_RECVHOPLIMIT</span><span class="sxs-lookup"><span data-stu-id="a848e-936">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="a848e-937">Дополнительные исправления и улучшения</span><span class="sxs-lookup"><span data-stu-id="a848e-937">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-938">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-938">LTP Results:</span></span>
<span data-ttu-id="a848e-939">Число пройденных тестов: 709</span><span class="sxs-lookup"><span data-stu-id="a848e-939">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="a848e-940">Число непройденных (неудачных, пропущенных и т. д.): 255</span><span class="sxs-lookup"><span data-stu-id="a848e-940">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="a848e-941">Журналы тестового запуска ЛТП</span><span class="sxs-lookup"><span data-stu-id="a848e-941">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="a848e-942">Сводка syscall</span><span class="sxs-lookup"><span data-stu-id="a848e-942">Syscall Summary</span></span>
<span data-ttu-id="a848e-943">Всего syscall: 384</span><span class="sxs-lookup"><span data-stu-id="a848e-943">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="a848e-944">Всего реализовано: 235</span><span class="sxs-lookup"><span data-stu-id="a848e-944">Total Implemented: 235</span></span> </br>
<span data-ttu-id="a848e-945">Всего создана: 22</span><span class="sxs-lookup"><span data-stu-id="a848e-945">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="a848e-946">Всего нереализованных: 127</span><span class="sxs-lookup"><span data-stu-id="a848e-946">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="a848e-947">Подробное разбиение</span><span class="sxs-lookup"><span data-stu-id="a848e-947">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="a848e-948">Сборка 15007</span><span class="sxs-lookup"><span data-stu-id="a848e-948">Build 15007</span></span>

<span data-ttu-id="a848e-949">Общие сведения о Windows в сборке 15007 см. в [блоге Windows]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span><span class="sxs-lookup"><span data-stu-id="a848e-949">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="a848e-950">Известная ошибка</span><span class="sxs-lookup"><span data-stu-id="a848e-950">Known Issue</span></span>

- <span data-ttu-id="a848e-951">Существует известная ошибка, из-за которой консоль не распознает некоторые <key> сочетания клавиш CTRL + ВВОД.</span><span class="sxs-lookup"><span data-stu-id="a848e-951">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="a848e-952">Сюда входит команда Ctrl-c, которая будет действовать как нормальное нажатие клавиши "c".</span><span class="sxs-lookup"><span data-stu-id="a848e-952">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="a848e-953">Возможное решение. Сопоставьте альтернативный ключ с CTRL + C.</span><span class="sxs-lookup"><span data-stu-id="a848e-953">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="a848e-954">Например, чтобы преобразовать сочетание клавиш CTRL + K в Ctrl + C, `stty intr \^k`сделайте следующее:.</span><span class="sxs-lookup"><span data-stu-id="a848e-954">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="a848e-955">Это сопоставление устанавливается на терминал и должно выполняться при *каждом* запуске bash.</span><span class="sxs-lookup"><span data-stu-id="a848e-955">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="a848e-956">Пользователи могут просмотреть этот параметр, чтобы включить его в`.bashrc`</span><span class="sxs-lookup"><span data-stu-id="a848e-956">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="a848e-957">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-957">Fixed</span></span>

- <span data-ttu-id="a848e-958">Исправлена ошибка, при которой работа WSL будет потреблять 100% ядра ЦП.</span><span class="sxs-lookup"><span data-stu-id="a848e-958">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="a848e-959">Параметр сокета IP_PKTINFO, IPV6_RECVPKTINFO теперь поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a848e-959">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="a848e-960">(GH #851, 987)</span><span class="sxs-lookup"><span data-stu-id="a848e-960">(GH #851, 987)</span></span>
- <span data-ttu-id="a848e-961">Усечение физического адреса сетевого интерфейса до 16 байт в лкскоре (GH #1452, 1414, 1343, 468, 308)</span><span class="sxs-lookup"><span data-stu-id="a848e-961">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="a848e-962">Дополнительные исправления и улучшения</span><span class="sxs-lookup"><span data-stu-id="a848e-962">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-963">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-963">LTP Results:</span></span>
<span data-ttu-id="a848e-964">Число пройденных тестов: 709</span><span class="sxs-lookup"><span data-stu-id="a848e-964">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="a848e-965">Число непройденных (неудачных, пропущенных и т. д.): 255</span><span class="sxs-lookup"><span data-stu-id="a848e-965">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="a848e-966">Журналы тестового запуска ЛТП</span><span class="sxs-lookup"><span data-stu-id="a848e-966">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="a848e-967">Сборка 15002</span><span class="sxs-lookup"><span data-stu-id="a848e-967">Build 15002</span></span>

<span data-ttu-id="a848e-968">Общие сведения о Windows в сборке 15002 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span><span class="sxs-lookup"><span data-stu-id="a848e-968">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="a848e-969">Известная ошибка</span><span class="sxs-lookup"><span data-stu-id="a848e-969">Known Issue</span></span>

<span data-ttu-id="a848e-970">Две известные проблемы:</span><span class="sxs-lookup"><span data-stu-id="a848e-970">Two known issues:</span></span>
- <span data-ttu-id="a848e-971">Существует известная ошибка, из-за которой консоль не распознает некоторые <key> сочетания клавиш CTRL + ВВОД.</span><span class="sxs-lookup"><span data-stu-id="a848e-971">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="a848e-972">Сюда входит команда Ctrl-c, которая будет действовать как нормальное нажатие клавиши "c".</span><span class="sxs-lookup"><span data-stu-id="a848e-972">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="a848e-973">Возможное решение. Сопоставьте альтернативный ключ с CTRL + C.</span><span class="sxs-lookup"><span data-stu-id="a848e-973">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="a848e-974">Например, чтобы преобразовать сочетание клавиш CTRL + K в Ctrl + C, `stty intr \^k`сделайте следующее:.</span><span class="sxs-lookup"><span data-stu-id="a848e-974">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="a848e-975">Это сопоставление устанавливается на терминал и должно выполняться при *каждом* запуске bash.</span><span class="sxs-lookup"><span data-stu-id="a848e-975">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="a848e-976">Пользователи могут просмотреть этот параметр, чтобы включить его в`.bashrc`</span><span class="sxs-lookup"><span data-stu-id="a848e-976">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="a848e-977">Во время выполнения WSL системный поток будет потреблять 100% ядер ЦП.</span><span class="sxs-lookup"><span data-stu-id="a848e-977">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="a848e-978">Основная причина устранена и исправлена внутренним образом.</span><span class="sxs-lookup"><span data-stu-id="a848e-978">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="a848e-979">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-979">Fixed</span></span>

- <span data-ttu-id="a848e-980">Все сеансы Bash теперь должны создаваться на одном уровне разрешений.</span><span class="sxs-lookup"><span data-stu-id="a848e-980">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="a848e-981">Попытка запустить сеанс на другом уровне будет заблокирована.</span><span class="sxs-lookup"><span data-stu-id="a848e-981">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="a848e-982">Это означает, что администраторы и консоли, не являющиеся администраторами, не могут работать одновременно.</span><span class="sxs-lookup"><span data-stu-id="a848e-982">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="a848e-983">(GH #626)</span><span class="sxs-lookup"><span data-stu-id="a848e-983">(GH #626)</span></span>
<br/>
- <span data-ttu-id="a848e-984">Реализует следующие сообщения NETLINK_ROUTE (требуется администратор Windows)</span><span class="sxs-lookup"><span data-stu-id="a848e-984">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="a848e-985">RTM_NEWADDR (поддерживает `ip addr add`)</span><span class="sxs-lookup"><span data-stu-id="a848e-985">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="a848e-986">RTM_NEWROUTE (поддерживает `ip route add`)</span><span class="sxs-lookup"><span data-stu-id="a848e-986">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="a848e-987">RTM_DELADDR (поддерживает `ip addr del`)</span><span class="sxs-lookup"><span data-stu-id="a848e-987">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="a848e-988">RTM_DELROUTE (поддерживает `ip route del`)</span><span class="sxs-lookup"><span data-stu-id="a848e-988">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="a848e-989">Запланированная проверка задач для пакетов, которые необходимо обновить, больше не будет выполняться для лимитного подключения (GH #1371)</span><span class="sxs-lookup"><span data-stu-id="a848e-989">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="a848e-990">Исправлена ошибка, из-за которой потрубка зависает, т. е. с "ls-alR/" | Bash-c "Cat" (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="a848e-990">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="a848e-991">Реализован параметр сокета TCP_KEEPCNT (GH #843)</span><span class="sxs-lookup"><span data-stu-id="a848e-991">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="a848e-992">Реализован параметр сокета IP_MTU_DISCOVER INET (GH #720, 717, 170, 69)</span><span class="sxs-lookup"><span data-stu-id="a848e-992">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="a848e-993">Удалены устаревшие функции для запуска двоичных файлов NT из init с помощью поиска по пути NT.</span><span class="sxs-lookup"><span data-stu-id="a848e-993">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="a848e-994">(GH #1325)</span><span class="sxs-lookup"><span data-stu-id="a848e-994">(GH #1325)</span></span>
- <span data-ttu-id="a848e-995">Исправление режима/Дев/КМСГ для разрешения групповой/другого доступа на чтение (0644) (GH #1321)</span><span class="sxs-lookup"><span data-stu-id="a848e-995">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="a848e-996">Реализованные/прок/СИС/Кернел/рандом/ууид (GH #1092)</span><span class="sxs-lookup"><span data-stu-id="a848e-996">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="a848e-997">Исправлена ошибка, когда время начала процесса было показано как год 2432 (GH #974)</span><span class="sxs-lookup"><span data-stu-id="a848e-997">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="a848e-998">Переменная среды TERM по умолчанию переключена на кстерм-256color (GH #1446)</span><span class="sxs-lookup"><span data-stu-id="a848e-998">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="a848e-999">Изменен способ вычисления фиксации процесса во время ветвления процесса.</span><span class="sxs-lookup"><span data-stu-id="a848e-999">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="a848e-1000">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="a848e-1000">(GH #1286)</span></span>
- <span data-ttu-id="a848e-1001">Реализованные/proc/sys/VM/overcommit_memory.</span><span class="sxs-lookup"><span data-stu-id="a848e-1001">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="a848e-1002">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="a848e-1002">(GH #1286)</span></span>
- <span data-ttu-id="a848e-1003">Реализованный/прок/нет/рауте-файл (GH #69)</span><span class="sxs-lookup"><span data-stu-id="a848e-1003">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="a848e-1004">Исправлена ошибка, при которой имя ярлыка было неправильно локализовано (GH #696)</span><span class="sxs-lookup"><span data-stu-id="a848e-1004">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="a848e-1005">Исправлена логика синтаксического анализа ELF, которая неправильно проверяет заголовки программы, должна быть меньше (или равна) PATH_MAX.</span><span class="sxs-lookup"><span data-stu-id="a848e-1005">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="a848e-1006">(GH #1048)</span><span class="sxs-lookup"><span data-stu-id="a848e-1006">(GH #1048)</span></span>
- <span data-ttu-id="a848e-1007">Реализован обратный вызов статфс для прокфс, сисфс, кграупфс и бинфмтфс (GH #1378)</span><span class="sxs-lookup"><span data-stu-id="a848e-1007">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="a848e-1008">Исправлены Аптпаккажеиндексупдате окна, которые не закрываются (GH #1184, также обсуждаются в GH #1193).</span><span class="sxs-lookup"><span data-stu-id="a848e-1008">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="a848e-1009">Добавлена поддержка ASLR ADDR_NO_RANDOMIZE.</span><span class="sxs-lookup"><span data-stu-id="a848e-1009">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="a848e-1010">(GH #1148, 1128)</span><span class="sxs-lookup"><span data-stu-id="a848e-1010">(GH #1148, 1128)</span></span>
- <span data-ttu-id="a848e-1011">Улучшенный PTRACE_GETSIGINFO, СИГСЕГВ для правильных трассировок стека gdb во время AV (GH #875)</span><span class="sxs-lookup"><span data-stu-id="a848e-1011">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="a848e-1012">Синтаксический анализ ELF больше не завершается ошибкой для двоичных файлов патчелф.</span><span class="sxs-lookup"><span data-stu-id="a848e-1012">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="a848e-1013">(GH #471)</span><span class="sxs-lookup"><span data-stu-id="a848e-1013">(GH #471)</span></span>
- <span data-ttu-id="a848e-1014">VPN-DNS, распространенная на/etc/resolv.conf (GH #416, 1350)</span><span class="sxs-lookup"><span data-stu-id="a848e-1014">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="a848e-1015">Улучшения в протоколе TCP Close для более надежной пересылки данных.</span><span class="sxs-lookup"><span data-stu-id="a848e-1015">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="a848e-1016">(GH #610, 616, 1025, 1335)</span><span class="sxs-lookup"><span data-stu-id="a848e-1016">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="a848e-1017">Теперь возвращает правильный код ошибки при открытии слишком большого числа файлов (ЕМФИЛЕ).</span><span class="sxs-lookup"><span data-stu-id="a848e-1017">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="a848e-1018">(GH #1126, 2090)</span><span class="sxs-lookup"><span data-stu-id="a848e-1018">(GH #1126, 2090)</span></span>
- <span data-ttu-id="a848e-1019">Журнал аудита Windows теперь сообщает имя образа в процессе создания аудита.</span><span class="sxs-lookup"><span data-stu-id="a848e-1019">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="a848e-1020">Теперь корректно завершается ошибкой при запуске bash. exe из окна bash</span><span class="sxs-lookup"><span data-stu-id="a848e-1020">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="a848e-1021">Добавлено сообщение об ошибке, когда взаимодействие не может получить доступ к рабочему каталогу в Лксфс (например, Notepad. exe. bashrc)</span><span class="sxs-lookup"><span data-stu-id="a848e-1021">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="a848e-1022">Исправлена проблема, при которой путь Windows был усечен в WSL</span><span class="sxs-lookup"><span data-stu-id="a848e-1022">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="a848e-1023">Дополнительные исправления и улучшения</span><span class="sxs-lookup"><span data-stu-id="a848e-1023">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-1024">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-1024">LTP Results:</span></span>
<span data-ttu-id="a848e-1025">Число пройденных тестов: 690</span><span class="sxs-lookup"><span data-stu-id="a848e-1025">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="a848e-1026">Число непройденных (неудачных, пропущенных и т. д.): 274</span><span class="sxs-lookup"><span data-stu-id="a848e-1026">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="a848e-1027">Журналы тестового запуска ЛТП</span><span class="sxs-lookup"><span data-stu-id="a848e-1027">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="a848e-1028">Поддержка syscall</span><span class="sxs-lookup"><span data-stu-id="a848e-1028">Syscall Support</span></span>
<span data-ttu-id="a848e-1029">Ниже приведен список новых или улучшенных syscall, которые имеют некоторую реализацию в WSL.</span><span class="sxs-lookup"><span data-stu-id="a848e-1029">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="a848e-1030">Syscall в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="a848e-1030">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="a848e-1031">Сборка 14986</span><span class="sxs-lookup"><span data-stu-id="a848e-1031">Build 14986</span></span>

<span data-ttu-id="a848e-1032">Общие сведения о Windows в сборке 14986 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span><span class="sxs-lookup"><span data-stu-id="a848e-1032">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-1033">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-1033">Fixed</span></span>

- <span data-ttu-id="a848e-1034">Исправлены бугчеккс с Нетлинк и PTY IOCTL</span><span class="sxs-lookup"><span data-stu-id="a848e-1034">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="a848e-1035">Версия ядра теперь сообщает 4.4.0-43 о согласованности с Xenial</span><span class="sxs-lookup"><span data-stu-id="a848e-1035">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="a848e-1036">Bash. exe теперь запускается, когда входные данные направляются в "NUL:" (GH #1259)</span><span class="sxs-lookup"><span data-stu-id="a848e-1036">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="a848e-1037">Идентификаторы потоков теперь отображаются правильно в прокфс (GH #967)</span><span class="sxs-lookup"><span data-stu-id="a848e-1037">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="a848e-1038">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | Флаги IN_ISDIR теперь поддерживаются в inotify_add_watch () (GH #1280)</span><span class="sxs-lookup"><span data-stu-id="a848e-1038">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="a848e-1039">Реализуйте timer_create и связанные системные вызовы.</span><span class="sxs-lookup"><span data-stu-id="a848e-1039">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="a848e-1040">Это обеспечивает поддержку ГХК (GH #307)</span><span class="sxs-lookup"><span data-stu-id="a848e-1040">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="a848e-1041">Исправлена проблема, из-за которой проверка связи возвращала время 0.000 MS (GH #1296).</span><span class="sxs-lookup"><span data-stu-id="a848e-1041">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="a848e-1042">Если открыто слишком много файлов, возвращается правильный код ошибки.</span><span class="sxs-lookup"><span data-stu-id="a848e-1042">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="a848e-1043">Исправлена проблема в WSL, при которой запрос Нетлинк для данных сетевого интерфейса завершится ошибкой с ЕИНВАЛ, если аппаратный адрес интерфейса — 32-байт (например, интерфейс Teredo).</span><span class="sxs-lookup"><span data-stu-id="a848e-1043">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="a848e-1044">Обратите внимание, что служебная программа Linux "IP" содержит ошибку, в которой произойдет сбой, если WSL сообщает 32-байтовый адрес оборудования.</span><span class="sxs-lookup"><span data-stu-id="a848e-1044">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="a848e-1045">Это ошибка в "IP", а не WSL.</span><span class="sxs-lookup"><span data-stu-id="a848e-1045">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="a848e-1046">Жестко код служебной программы "IP" имеет длину строкового буфера, используемого для печати аппаратного адреса, и этот буфер слишком мал для печати 32-байтного аппаратного адреса.</span><span class="sxs-lookup"><span data-stu-id="a848e-1046">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="a848e-1047">Дополнительные исправления и улучшения</span><span class="sxs-lookup"><span data-stu-id="a848e-1047">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-1048">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-1048">LTP Results:</span></span>
<span data-ttu-id="a848e-1049">Число пройденных тестов: 669</span><span class="sxs-lookup"><span data-stu-id="a848e-1049">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="a848e-1050">Число непройденных (неудачных, пропущенных и т. д.): 258</span><span class="sxs-lookup"><span data-stu-id="a848e-1050">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="a848e-1051">Журналы тестового запуска ЛТП</span><span class="sxs-lookup"><span data-stu-id="a848e-1051">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="a848e-1052">Поддержка syscall</span><span class="sxs-lookup"><span data-stu-id="a848e-1052">Syscall Support</span></span>
<span data-ttu-id="a848e-1053">Ниже приведен список новых или улучшенных syscall, которые имеют некоторую реализацию в WSL.</span><span class="sxs-lookup"><span data-stu-id="a848e-1053">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="a848e-1054">Syscall в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="a848e-1054">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="a848e-1055">Сборка 14971</span><span class="sxs-lookup"><span data-stu-id="a848e-1055">Build 14971</span></span>

<span data-ttu-id="a848e-1056">Общие сведения о Windows в сборке 14971 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="a848e-1056">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-1057">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-1057">Fixed</span></span>

 - <span data-ttu-id="a848e-1058">Из-за обстоятельств, которые выходят за рамки нашего управления, в этой сборке не будет обновлений для подсистемы Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="a848e-1058">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="a848e-1059">Регулярно запланированные обновления будут возобновлены в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="a848e-1059">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-1060">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-1060">LTP Results:</span></span>
<span data-ttu-id="a848e-1061">Без изменений с 14965</span><span class="sxs-lookup"><span data-stu-id="a848e-1061">Unchanged from 14965</span></span> </br>
<span data-ttu-id="a848e-1062">Число пройденных тестов: 664</span><span class="sxs-lookup"><span data-stu-id="a848e-1062">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="a848e-1063">Число непройденных (неудачных, пропущенных и т. д.): 263</span><span class="sxs-lookup"><span data-stu-id="a848e-1063">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="a848e-1064">Журналы тестового запуска ЛТП</span><span class="sxs-lookup"><span data-stu-id="a848e-1064">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="a848e-1065">Сборка 14965</span><span class="sxs-lookup"><span data-stu-id="a848e-1065">Build 14965</span></span>

<span data-ttu-id="a848e-1066">Общие сведения о Windows в сборке 14965 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="a848e-1066">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-1067">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-1067">Fixed</span></span>

- <span data-ttu-id="a848e-1068">Поддержка протоколов RTM_GETLINK и RTM_GETADDR Нетлинк Sockets NETLINK_ROUTE (GH #468)</span><span class="sxs-lookup"><span data-stu-id="a848e-1068">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="a848e-1069">Включает команды ifconfig и IP для перечисления сетей.</span><span class="sxs-lookup"><span data-stu-id="a848e-1069">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="a848e-1070">Дополнительные сведения можно найти в записи [блога WSL Networking](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span><span class="sxs-lookup"><span data-stu-id="a848e-1070">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="a848e-1071">/сбин теперь находится в пути пользователя по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a848e-1071">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="a848e-1072">Путь пользователя NT теперь по умолчанию добавляется к пути WSL (т. е. Теперь можно ввести Notepad. exe без добавления system32 в путь Linux).</span><span class="sxs-lookup"><span data-stu-id="a848e-1072">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="a848e-1073">Добавлена поддержка/proc/sys/kernel/cap_last_cap.</span><span class="sxs-lookup"><span data-stu-id="a848e-1073">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="a848e-1074">Двоичные файлы NT теперь можно запускать из WSL, если текущий рабочий каталог содержит символы, отличные от ANSI (GH #1254).</span><span class="sxs-lookup"><span data-stu-id="a848e-1074">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="a848e-1075">Разрешить завершение работы в отключенном сокете потока UNIX.</span><span class="sxs-lookup"><span data-stu-id="a848e-1075">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="a848e-1076">Добавлена поддержка PR_GET_PDEATHSIG.</span><span class="sxs-lookup"><span data-stu-id="a848e-1076">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="a848e-1077">Добавлена поддержка CLONE_PARENT.</span><span class="sxs-lookup"><span data-stu-id="a848e-1077">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="a848e-1078">Исправлена ошибка, из-за которой потрубка зависает, т. е. с "ls-alR/" | Bash-c "Cat" (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="a848e-1078">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="a848e-1079">Обрабатывает запросы для подключения к текущему терминалу.</span><span class="sxs-lookup"><span data-stu-id="a848e-1079">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="a848e-1080">Пометьте<pid>/прок//oom_score_adj как доступный для записи.</span><span class="sxs-lookup"><span data-stu-id="a848e-1080">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="a848e-1081">Добавьте папку/СИС/ФС/кграуп.</span><span class="sxs-lookup"><span data-stu-id="a848e-1081">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="a848e-1082">sched_setaffinity должен возвращать число масок сходства</span><span class="sxs-lookup"><span data-stu-id="a848e-1082">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="a848e-1083">Исправьте логику проверки ELF, которая неправильно предполагает, что пути интерпретатора должны иметь длину менее 64 символов.</span><span class="sxs-lookup"><span data-stu-id="a848e-1083">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="a848e-1084">(GH #743)</span><span class="sxs-lookup"><span data-stu-id="a848e-1084">(GH #743)</span></span>
- <span data-ttu-id="a848e-1085">Открытые дескрипторы файлов могут оставаться открытыми в окне консоли (GH #1187)</span><span class="sxs-lookup"><span data-stu-id="a848e-1085">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="a848e-1086">Фиксид Error, где сбой Rename () с завершающей косой чертой в имени целевого объекта (GH #1008)</span><span class="sxs-lookup"><span data-stu-id="a848e-1086">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="a848e-1087">Реализация файла/прок/нет/Дев</span><span class="sxs-lookup"><span data-stu-id="a848e-1087">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="a848e-1088">Исправлена 0.000 MS ping из-за разрешения таймера.</span><span class="sxs-lookup"><span data-stu-id="a848e-1088">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="a848e-1089">Реализованные/прок/Селф/енвирон (GH #730)</span><span class="sxs-lookup"><span data-stu-id="a848e-1089">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="a848e-1090">Дополнительные исправлений и усовершенствования</span><span class="sxs-lookup"><span data-stu-id="a848e-1090">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-1091">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-1091">LTP Results:</span></span>
<span data-ttu-id="a848e-1092">Число пройденных тестов: 664</span><span class="sxs-lookup"><span data-stu-id="a848e-1092">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="a848e-1093">Число непройденных (неудачных, пропущенных и т. д.): 263</span><span class="sxs-lookup"><span data-stu-id="a848e-1093">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="a848e-1094">Журналы тестового запуска ЛТП</span><span class="sxs-lookup"><span data-stu-id="a848e-1094">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="a848e-1095">Сборка 14959</span><span class="sxs-lookup"><span data-stu-id="a848e-1095">Build 14959</span></span>

<span data-ttu-id="a848e-1096">Общие сведения о Windows в сборке 14959 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span><span class="sxs-lookup"><span data-stu-id="a848e-1096">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-1097">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-1097">Fixed</span></span>

- <span data-ttu-id="a848e-1098">Улучшенное уведомление о процессе Pico для Windows.</span><span class="sxs-lookup"><span data-stu-id="a848e-1098">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="a848e-1099">Дополнительные сведения содержатся в [блоге WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span><span class="sxs-lookup"><span data-stu-id="a848e-1099">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="a848e-1100">Улучшенная стабильность благодаря взаимодействию Windows</span><span class="sxs-lookup"><span data-stu-id="a848e-1100">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="a848e-1101">Исправлена ошибка 0x80070057 при запуске bash. exe при включенной защите корпоративных данных (EDP)</span><span class="sxs-lookup"><span data-stu-id="a848e-1101">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="a848e-1102">Дополнительные исправлений и усовершенствования</span><span class="sxs-lookup"><span data-stu-id="a848e-1102">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-1103">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-1103">LTP Results:</span></span>
<span data-ttu-id="a848e-1104">Число пройденных тестов: 665</span><span class="sxs-lookup"><span data-stu-id="a848e-1104">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="a848e-1105">Число непройденных (неудачных, пропущенных и т. д.): 263</span><span class="sxs-lookup"><span data-stu-id="a848e-1105">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="a848e-1106">Журналы тестового запуска ЛТП</span><span class="sxs-lookup"><span data-stu-id="a848e-1106">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="a848e-1107">Сборка 14955</span><span class="sxs-lookup"><span data-stu-id="a848e-1107">Build 14955</span></span>

<span data-ttu-id="a848e-1108">Общие сведения о Windows в сборке 14955 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span><span class="sxs-lookup"><span data-stu-id="a848e-1108">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-1109">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-1109">Fixed</span></span>

 - <span data-ttu-id="a848e-1110">Из-за обстоятельств, которые выходят за рамки нашего управления, в этой сборке не будет обновлений для подсистемы Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="a848e-1110">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="a848e-1111">Регулярно запланированные обновления будут возобновлены в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="a848e-1111">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-1112">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-1112">LTP Results:</span></span>
<span data-ttu-id="a848e-1113">Число пройденных тестов: 665</span><span class="sxs-lookup"><span data-stu-id="a848e-1113">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="a848e-1114">Число непройденных (неудачных, пропущенных и т. д.): 263</span><span class="sxs-lookup"><span data-stu-id="a848e-1114">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="a848e-1115">Журналы тестового запуска ЛТП</span><span class="sxs-lookup"><span data-stu-id="a848e-1115">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="a848e-1116">Сборка 14951</span><span class="sxs-lookup"><span data-stu-id="a848e-1116">Build 14951</span></span>

<span data-ttu-id="a848e-1117">Общие сведения о Windows в сборке 14951 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="a848e-1117">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="a848e-1118">Новая функция: Взаимодействие Windows и Ubuntu</span><span class="sxs-lookup"><span data-stu-id="a848e-1118">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="a848e-1119">Теперь двоичные файлы Windows можно вызывать непосредственно из командной строки WSL.</span><span class="sxs-lookup"><span data-stu-id="a848e-1119">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="a848e-1120">Это дает пользователям возможность взаимодействовать со средой Windows и системой способом, который не был бы возможным.</span><span class="sxs-lookup"><span data-stu-id="a848e-1120">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="a848e-1121">В качестве краткого примера, теперь пользователи могут выполнять следующие команды:</span><span class="sxs-lookup"><span data-stu-id="a848e-1121">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="a848e-1122">Дополнительные сведения можно найти по адресу:</span><span class="sxs-lookup"><span data-stu-id="a848e-1122">More information can be found at:</span></span>

- [<span data-ttu-id="a848e-1123">Блог команды WSL для взаимодействия</span><span class="sxs-lookup"><span data-stu-id="a848e-1123">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="a848e-1124">Документация по взаимодействию MSDN</span><span class="sxs-lookup"><span data-stu-id="a848e-1124">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="a848e-1125">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-1125">Fixed</span></span>

- <span data-ttu-id="a848e-1126">Ubuntu 16,04 (Xenial) теперь устанавливается для всех новых экземпляров WSL.</span><span class="sxs-lookup"><span data-stu-id="a848e-1126">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="a848e-1127">Пользователи с существующими экземплярами 14,04 (Trusted) не будут обновляться автоматически.</span><span class="sxs-lookup"><span data-stu-id="a848e-1127">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="a848e-1128">Языковой стандарт, установленный во время установки, теперь отображается</span><span class="sxs-lookup"><span data-stu-id="a848e-1128">Locale set during install is now displayed</span></span>
- <span data-ttu-id="a848e-1129">Улучшения в терминале, включая ошибку, когда перенаправление процесса WSL в файл не всегда работает</span><span class="sxs-lookup"><span data-stu-id="a848e-1129">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="a848e-1130">Время существования консоли должно быть связано с временем существования bash. exe</span><span class="sxs-lookup"><span data-stu-id="a848e-1130">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="a848e-1131">Размер окна консоли должен иметь видимый размер, а не размер буфера</span><span class="sxs-lookup"><span data-stu-id="a848e-1131">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="a848e-1132">Дополнительные исправлений и усовершенствования</span><span class="sxs-lookup"><span data-stu-id="a848e-1132">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-1133">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-1133">LTP Results:</span></span>
<span data-ttu-id="a848e-1134">Число пройденных тестов: 665</span><span class="sxs-lookup"><span data-stu-id="a848e-1134">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="a848e-1135">Число непройденных (неудачных, пропущенных и т. д.): 263</span><span class="sxs-lookup"><span data-stu-id="a848e-1135">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="a848e-1136">Журналы тестового запуска ЛТП</span><span class="sxs-lookup"><span data-stu-id="a848e-1136">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="a848e-1137">Сборка 14946</span><span class="sxs-lookup"><span data-stu-id="a848e-1137">Build 14946</span></span>

<span data-ttu-id="a848e-1138">Общие сведения о Windows в сборке 14946 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span><span class="sxs-lookup"><span data-stu-id="a848e-1138">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-1139">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-1139">Fixed</span></span>

- <span data-ttu-id="a848e-1140">Исправлена проблема, которая не позволила создать учетные записи пользователей WSL для пользователей с именами пользователей NT, содержащими пробелы или кавычки.</span><span class="sxs-lookup"><span data-stu-id="a848e-1140">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="a848e-1141">Измените Волфс и Дрвфс, чтобы возвращалось значение 0 для счетчика ссылок каталога в stat</span><span class="sxs-lookup"><span data-stu-id="a848e-1141">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="a848e-1142">Поддержка параметра сокета IPV6_MULTICAST_HOPS.</span><span class="sxs-lookup"><span data-stu-id="a848e-1142">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="a848e-1143">Ограничивается одним циклом ввода-вывода консоли на TTY.</span><span class="sxs-lookup"><span data-stu-id="a848e-1143">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="a848e-1144">Пример. возможна следующая команда:</span><span class="sxs-lookup"><span data-stu-id="a848e-1144">Example: the following command is possible:</span></span>
  - <span data-ttu-id="a848e-1145">Bash-c "Echo Data" | Bash-c "SSH user@example.com " Cat > foo. txt ""</span><span class="sxs-lookup"><span data-stu-id="a848e-1145">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="a848e-1146">Замена пробелов символами табуляции в/прок/кпуинфо (GH #1115)</span><span class="sxs-lookup"><span data-stu-id="a848e-1146">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="a848e-1147">Дрвфс теперь отображается в маунтинфо с именем, совпадающим с подключенным томом Windows.</span><span class="sxs-lookup"><span data-stu-id="a848e-1147">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="a848e-1148">/Home и/root теперь отображаются в маунтинфо с правильными именами</span><span class="sxs-lookup"><span data-stu-id="a848e-1148">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="a848e-1149">Дополнительные исправлений и усовершенствования</span><span class="sxs-lookup"><span data-stu-id="a848e-1149">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-1150">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-1150">LTP Results:</span></span>
<span data-ttu-id="a848e-1151">Число пройденных тестов: 665</span><span class="sxs-lookup"><span data-stu-id="a848e-1151">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="a848e-1152">Число непройденных (неудачных, пропущенных и т. д.): 263</span><span class="sxs-lookup"><span data-stu-id="a848e-1152">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="a848e-1153">Журналы тестового запуска ЛТП</span><span class="sxs-lookup"><span data-stu-id="a848e-1153">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="a848e-1154">Сборка 14942</span><span class="sxs-lookup"><span data-stu-id="a848e-1154">Build 14942</span></span>

<span data-ttu-id="a848e-1155">Общие сведения о Windows в сборке 14942 см. в [блоге Windows](https://aka.ms/onefourninefourtwoooooo).</span><span class="sxs-lookup"><span data-stu-id="a848e-1155">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-1156">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-1156">Fixed</span></span>

- <span data-ttu-id="a848e-1157">Ряд бугчеккс, в том числе "попытки выполнения нехватки памяти", которые блокируют SSH</span><span class="sxs-lookup"><span data-stu-id="a848e-1157">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="a848e-1158">Поддержка инотифий для уведомлений, созданных из приложений Windows на Дрвфс, теперь находится в</span><span class="sxs-lookup"><span data-stu-id="a848e-1158">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="a848e-1159">Реализуйте TCP_KEEPIDLE и TCP_KEEPINTVL для mongod.</span><span class="sxs-lookup"><span data-stu-id="a848e-1159">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="a848e-1160">(GH #695)</span><span class="sxs-lookup"><span data-stu-id="a848e-1160">(GH #695)</span></span>
- <span data-ttu-id="a848e-1161">Реализация системного вызова pivot_root</span><span class="sxs-lookup"><span data-stu-id="a848e-1161">Implement the pivot_root system call</span></span>
- <span data-ttu-id="a848e-1162">Реализация параметра сокета для SO_DONTROUTE</span><span class="sxs-lookup"><span data-stu-id="a848e-1162">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="a848e-1163">Дополнительные исправлений и усовершенствования</span><span class="sxs-lookup"><span data-stu-id="a848e-1163">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="a848e-1164">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-1164">LTP Results:</span></span>
<span data-ttu-id="a848e-1165">Число пройденных тестов: 665</span><span class="sxs-lookup"><span data-stu-id="a848e-1165">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="a848e-1166">Число непройденных (неудачных, пропущенных и т. д.): 263</span><span class="sxs-lookup"><span data-stu-id="a848e-1166">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="a848e-1167">Журналы тестового запуска ЛТП</span><span class="sxs-lookup"><span data-stu-id="a848e-1167">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="a848e-1168">Поддержка syscall</span><span class="sxs-lookup"><span data-stu-id="a848e-1168">Syscall Support</span></span>
<span data-ttu-id="a848e-1169">Ниже приведен список новых или улучшенных syscall, которые имеют некоторую реализацию в WSL.</span><span class="sxs-lookup"><span data-stu-id="a848e-1169">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="a848e-1170">Syscall в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="a848e-1170">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="a848e-1171">Сборка 14936</span><span class="sxs-lookup"><span data-stu-id="a848e-1171">Build 14936</span></span>

<span data-ttu-id="a848e-1172">Общие сведения о Windows в сборке 14936 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="a848e-1172">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="a848e-1173">Примечание. WSL установит версию Ubuntu 16,04 (Xenial) вместо Ubuntu 14,04 (Trusted) в предстоящем выпуске.</span><span class="sxs-lookup"><span data-stu-id="a848e-1173">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="a848e-1174">Это изменение будет применено к участникам программы установки новых экземпляров (лксрун. exe/install или первый запуск bash. exe).</span><span class="sxs-lookup"><span data-stu-id="a848e-1174">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="a848e-1175">Существующие экземпляры с доверием не будут обновляться автоматически.</span><span class="sxs-lookup"><span data-stu-id="a848e-1175">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="a848e-1176">Пользователи могут обновить свой образ доверия до Xenial с помощью команды Do-Release-Upgrade.</span><span class="sxs-lookup"><span data-stu-id="a848e-1176">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="a848e-1177">Известная ошибка</span><span class="sxs-lookup"><span data-stu-id="a848e-1177">Known Issue</span></span>
<span data-ttu-id="a848e-1178">В WSL возникла проблема с некоторыми реализациями сокетов.</span><span class="sxs-lookup"><span data-stu-id="a848e-1178">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="a848e-1179">При возникновении ошибки "попыток выполнения невыполненной памяти" происходит ошибка в манифесте.</span><span class="sxs-lookup"><span data-stu-id="a848e-1179">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="a848e-1180">Наиболее распространенной обработкой этой проблемы является сбой при использовании SSH.</span><span class="sxs-lookup"><span data-stu-id="a848e-1180">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="a848e-1181">Основная причина исправлена во внутренних сборках и будет отправлена участникам программы предварительной оценки по самой ранней возможности.</span><span class="sxs-lookup"><span data-stu-id="a848e-1181">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="a848e-1182">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-1182">Fixed</span></span>

- <span data-ttu-id="a848e-1183">Реализуется системный вызов чрут</span><span class="sxs-lookup"><span data-stu-id="a848e-1183">Implemented the chroot system call</span></span>
- <span data-ttu-id="a848e-1184">Улучшения в инотифи, ~~включая поддержку уведомлений, созданных из приложений Windows на дрвфс~~</span><span class="sxs-lookup"><span data-stu-id="a848e-1184">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="a848e-1185">Предлагаем Поддержка инотифи изменений, исходящих из приложений Windows, в настоящее время недоступна.</span><span class="sxs-lookup"><span data-stu-id="a848e-1185">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="a848e-1186">Привязка сокета к IPv6:<port n> : теперь поддерживает IPV6_V6ONLY (GH #68, #157, #393, #460, #674, #740, #982, #996)</span><span class="sxs-lookup"><span data-stu-id="a848e-1186">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="a848e-1187">Поведение ВНОВАИТ для реализации ваитид системкалл (GH #638)</span><span class="sxs-lookup"><span data-stu-id="a848e-1187">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="a848e-1188">Поддержка параметров сокетов IP-адресов IP_HDRINCL и IP_TTL</span><span class="sxs-lookup"><span data-stu-id="a848e-1188">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="a848e-1189">Чтение нулевой длины () должно возвращаться немедленно (GH #975)</span><span class="sxs-lookup"><span data-stu-id="a848e-1189">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="a848e-1190">Правильно обработайте имена файлов и префиксов имен файлов, которые не содержат Терминатор NULL в tar-файле.</span><span class="sxs-lookup"><span data-stu-id="a848e-1190">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="a848e-1191">Поддержка еполл для/Дев/Нулл</span><span class="sxs-lookup"><span data-stu-id="a848e-1191">epoll support for /dev/null</span></span>
- <span data-ttu-id="a848e-1192">Исправление источника времени/дев/аларм</span><span class="sxs-lookup"><span data-stu-id="a848e-1192">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="a848e-1193">Bash-c теперь может выполнять перенаправление в файл</span><span class="sxs-lookup"><span data-stu-id="a848e-1193">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="a848e-1194">Дополнительные исправлений и усовершенствования</span><span class="sxs-lookup"><span data-stu-id="a848e-1194">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-1195">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-1195">LTP Results:</span></span>
<span data-ttu-id="a848e-1196">Число пройденных тестов: 664</span><span class="sxs-lookup"><span data-stu-id="a848e-1196">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="a848e-1197">Число непройденных (неудачных, пропущенных и т. д.): 264</span><span class="sxs-lookup"><span data-stu-id="a848e-1197">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="a848e-1198">Журналы тестового запуска ЛТП</span><span class="sxs-lookup"><span data-stu-id="a848e-1198">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="a848e-1199">Поддержка syscall</span><span class="sxs-lookup"><span data-stu-id="a848e-1199">Syscall Support</span></span>
<span data-ttu-id="a848e-1200">Ниже приведен список новых или улучшенных syscall, которые имеют некоторую реализацию в WSL.</span><span class="sxs-lookup"><span data-stu-id="a848e-1200">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="a848e-1201">Syscall в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="a848e-1201">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="a848e-1202">Сборка 14931</span><span class="sxs-lookup"><span data-stu-id="a848e-1202">Build 14931</span></span>

<span data-ttu-id="a848e-1203">Общие сведения о Windows в сборке 14931 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="a848e-1203">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-1204">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-1204">Fixed</span></span>

 - <span data-ttu-id="a848e-1205">Из-за обстоятельств, которые выходят за рамки нашего управления, в этой сборке не будет обновлений для подсистемы Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="a848e-1205">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="a848e-1206">Регулярно запланированные обновления будут возобновлены в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="a848e-1206">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="a848e-1207">Сборка 14926</span><span class="sxs-lookup"><span data-stu-id="a848e-1207">Build 14926</span></span>

<span data-ttu-id="a848e-1208">Общие сведения о Windows в сборке 14926 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="a848e-1208">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-1209">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-1209">Fixed</span></span>

- <span data-ttu-id="a848e-1210">Команда ping теперь работает в консолях, которые не имеют прав администратора</span><span class="sxs-lookup"><span data-stu-id="a848e-1210">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="a848e-1211">Теперь поддерживается ping6, но без прав администратора</span><span class="sxs-lookup"><span data-stu-id="a848e-1211">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="a848e-1212">Поддержка инотифи для файлов, измененных через WSL.</span><span class="sxs-lookup"><span data-stu-id="a848e-1212">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="a848e-1213">(GH #216)</span><span class="sxs-lookup"><span data-stu-id="a848e-1213">(GH #216)</span></span>
  - <span data-ttu-id="a848e-1214">Поддерживаемые флаги:</span><span class="sxs-lookup"><span data-stu-id="a848e-1214">Flags supported:</span></span>
    - <span data-ttu-id="a848e-1215">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="a848e-1215">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="a848e-1216">события inotify_add_watch: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="a848e-1216">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="a848e-1217">inotify_add_watch атрибуты: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="a848e-1217">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="a848e-1218">чтение выходных данных: LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="a848e-1218">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="a848e-1219">Известная ошибка: Изменение файлов из приложений Windows не приводит к созданию событий</span><span class="sxs-lookup"><span data-stu-id="a848e-1219">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="a848e-1220">Сокет UNIX теперь поддерживает SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="a848e-1220">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="a848e-1221">ЛТП результаты:</span><span class="sxs-lookup"><span data-stu-id="a848e-1221">LTP Results:</span></span>
<span data-ttu-id="a848e-1222">Число пройденных тестов: 651</span><span class="sxs-lookup"><span data-stu-id="a848e-1222">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="a848e-1223">Число непройденных (неудачных, пропущенных и т. д.): 258</span><span class="sxs-lookup"><span data-stu-id="a848e-1223">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="a848e-1224">Журналы тестового запуска ЛТП</span><span class="sxs-lookup"><span data-stu-id="a848e-1224">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="a848e-1225">Сборка 14915</span><span class="sxs-lookup"><span data-stu-id="a848e-1225">Build 14915</span></span>

<span data-ttu-id="a848e-1226">Общие сведения о Windows в сборке 14915 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="a848e-1226">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-1227">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-1227">Fixed</span></span>
-  <span data-ttu-id="a848e-1228">Соккетпаир для сокетов датаграмм UNIX (GH #262)</span><span class="sxs-lookup"><span data-stu-id="a848e-1228">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="a848e-1229">Поддержка сокетов UNIX для SO_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="a848e-1229">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="a848e-1230">Поддержка сокетов UNIX для SO_BROADCAST (GH #568)</span><span class="sxs-lookup"><span data-stu-id="a848e-1230">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="a848e-1231">Поддержка сокетов UNIX для SOCK_SEQPACKET (GH #758, #546)</span><span class="sxs-lookup"><span data-stu-id="a848e-1231">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="a848e-1232">Добавление поддержки для Send, recv и завершения работы сокета датаграмм UNIX</span><span class="sxs-lookup"><span data-stu-id="a848e-1232">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="a848e-1233">Устранена критическая ошибка из-за неправильной проверки параметра mmap для нефиксированных адресов.</span><span class="sxs-lookup"><span data-stu-id="a848e-1233">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="a848e-1234">(GH #847)</span><span class="sxs-lookup"><span data-stu-id="a848e-1234">(GH #847)</span></span>
- <span data-ttu-id="a848e-1235">Поддержка приостановки и возобновления состояний терминала</span><span class="sxs-lookup"><span data-stu-id="a848e-1235">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="a848e-1236">Поддержка ТИОКПКТ IOCTL для разблокировки экранной программы (GH #774)</span><span class="sxs-lookup"><span data-stu-id="a848e-1236">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="a848e-1237">Известная ошибка: Неработоспособные ключи функций</span><span class="sxs-lookup"><span data-stu-id="a848e-1237">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="a848e-1238">Исправлено состязание в Тимерфд, которое может привести к доступу к освобожденному члену Реадерреади с помощью Лксптимерфдворкерраутине (GH #814)</span><span class="sxs-lookup"><span data-stu-id="a848e-1238">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="a848e-1239">Включить перезапускаемую поддержку системных вызовов для футекс, опроса и clock_nanosleep</span><span class="sxs-lookup"><span data-stu-id="a848e-1239">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="a848e-1240">Добавлена поддержка монтирования привязки.</span><span class="sxs-lookup"><span data-stu-id="a848e-1240">Added bind mount support</span></span>
- <span data-ttu-id="a848e-1241">отменить общий доступ для поддержки пространства имен подключения</span><span class="sxs-lookup"><span data-stu-id="a848e-1241">unshare for mount namespace support</span></span>
    - <span data-ttu-id="a848e-1242">Известная ошибка: При создании нового пространства имен Mount с `unshare(CLONE_NEWNS)` текущим рабочим каталогом будет по-прежнему указывать на старое пространство имен</span><span class="sxs-lookup"><span data-stu-id="a848e-1242">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="a848e-1243">Дополнительные улучшения и исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="a848e-1243">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="a848e-1244">Сборка 14905</span><span class="sxs-lookup"><span data-stu-id="a848e-1244">Build 14905</span></span>

<span data-ttu-id="a848e-1245">Общие сведения о Windows в сборке 14905 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span><span class="sxs-lookup"><span data-stu-id="a848e-1245">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-1246">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-1246">Fixed</span></span>
- <span data-ttu-id="a848e-1247">Теперь поддерживаются Перезапускаемые системные вызовы (GH #349, GH #520)</span><span class="sxs-lookup"><span data-stu-id="a848e-1247">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="a848e-1248">Символических ссылок к каталогам, которые заканчиваются на текущий момент (GH #650)</span><span class="sxs-lookup"><span data-stu-id="a848e-1248">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="a848e-1249">Реализован РНДЖЕТЕНТКНТ IOCTL для/dev/random</span><span class="sxs-lookup"><span data-stu-id="a848e-1249">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="a848e-1250">Реализованы файлы/прок/[PID]/Маунтс,/прок/[PID]/маунтинфо и/прок/[PID]/маунтстатс</span><span class="sxs-lookup"><span data-stu-id="a848e-1250">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="a848e-1251">Дополнительные исправлений и усовершенствования</span><span class="sxs-lookup"><span data-stu-id="a848e-1251">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="a848e-1252">Сборка 14901</span><span class="sxs-lookup"><span data-stu-id="a848e-1252">Build 14901</span></span>
<span data-ttu-id="a848e-1253">Первая сборка Insider Preview для выпуска обновления Windows 10 годовщина.</span><span class="sxs-lookup"><span data-stu-id="a848e-1253">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="a848e-1254">Общие сведения о Windows в сборке 14901 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="a848e-1254">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-1255">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-1255">Fixed</span></span>
- <span data-ttu-id="a848e-1256">Исправлена проблема завершающей косой черты</span><span class="sxs-lookup"><span data-stu-id="a848e-1256">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="a848e-1257">Команды, такие `$ mv a/c/ a/b/` как Now</span><span class="sxs-lookup"><span data-stu-id="a848e-1257">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="a848e-1258">Теперь при установке запрашиваются параметры языкового стандарта Ubuntu в Windows.</span><span class="sxs-lookup"><span data-stu-id="a848e-1258">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="a848e-1259">Поддержка прокфс для папки NS</span><span class="sxs-lookup"><span data-stu-id="a848e-1259">Procfs support for ns folder</span></span>
- <span data-ttu-id="a848e-1260">Добавлены подключение и отключение для файловых систем тмпфс, прокфс и сисфс.</span><span class="sxs-lookup"><span data-stu-id="a848e-1260">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="a848e-1261">Исправление мкнод [at] 32-разрядная подпись ABI</span><span class="sxs-lookup"><span data-stu-id="a848e-1261">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="a848e-1262">Сокеты Unix, перемещенные в модель диспетчеризации</span><span class="sxs-lookup"><span data-stu-id="a848e-1262">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="a848e-1263">Размер буфера получения сокета INET, заданный с помощью сетсоккопт, должен быть оплачен</span><span class="sxs-lookup"><span data-stu-id="a848e-1263">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="a848e-1264">Применить флаг сообщения о получении сокета MSG_CMSG_CLOEXEC UNIX</span><span class="sxs-lookup"><span data-stu-id="a848e-1264">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="a848e-1265">Перенаправление канала stdin/stdout процесса Linux (GH #2)</span><span class="sxs-lookup"><span data-stu-id="a848e-1265">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="a848e-1266">Разрешает конвейер команд Bash-c в CMD.</span><span class="sxs-lookup"><span data-stu-id="a848e-1266">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="a848e-1267">Пример: > dir | Bash-c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="a848e-1267">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="a848e-1268">Bash теперь можно установить в системах с несколькими файлов подкачки (GH #538, #358)</span><span class="sxs-lookup"><span data-stu-id="a848e-1268">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="a848e-1269">Размер буфера сокета INET по умолчанию должен совпадать с размером программы установки Ubuntu по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a848e-1269">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="a848e-1270">Выровняйте ксаттр syscall до листксаттр</span><span class="sxs-lookup"><span data-stu-id="a848e-1270">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="a848e-1271">Возвращать только интерфейсы с допустимым IPv4-адресом из СИОКГИФКОНФ</span><span class="sxs-lookup"><span data-stu-id="a848e-1271">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="a848e-1272">Исправлять действие по умолчанию сигнала при внедрении с помощью птраце</span><span class="sxs-lookup"><span data-stu-id="a848e-1272">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="a848e-1273">Реализация/proc/sys/VM/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="a848e-1273">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="a848e-1274">Использовать значения реестра контекста компьютера при восстановлении контекста в сигретурн</span><span class="sxs-lookup"><span data-stu-id="a848e-1274">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="a848e-1275">Это решает проблему, когда Java и жавак были зависанием для некоторых пользователей</span><span class="sxs-lookup"><span data-stu-id="a848e-1275">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="a848e-1276">Реализация/прок/СИС/Кернел/хостнаме</span><span class="sxs-lookup"><span data-stu-id="a848e-1276">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="a848e-1277">Поддержка syscall</span><span class="sxs-lookup"><span data-stu-id="a848e-1277">Syscall Support</span></span>
<span data-ttu-id="a848e-1278">Ниже приведен список новых или улучшенных syscall, которые имеют некоторую реализацию в WSL.</span><span class="sxs-lookup"><span data-stu-id="a848e-1278">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="a848e-1279">Syscall в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="a848e-1279">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="a848e-1280">Создание годовщины с 14388 по Windows 10</span><span class="sxs-lookup"><span data-stu-id="a848e-1280">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="a848e-1281">Общие сведения о Windows в сборке 14388 см. в [блоге Windows](https://aka.ms/14388wip).</span><span class="sxs-lookup"><span data-stu-id="a848e-1281">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="a848e-1282">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-1282">Fixed</span></span>
- <span data-ttu-id="a848e-1283">Исправления для подготовки к обновлению годовщины Windows 10 на 8/2</span><span class="sxs-lookup"><span data-stu-id="a848e-1283">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="a848e-1284">Дополнительные сведения о WSL в обновлении годовщины можно найти в нашем [блоге](https://blogs.msdn.microsoft.com/wsl/) .</span><span class="sxs-lookup"><span data-stu-id="a848e-1284">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="a848e-1285">Сборка 14376</span><span class="sxs-lookup"><span data-stu-id="a848e-1285">Build 14376</span></span>
<span data-ttu-id="a848e-1286">Общие сведения о Windows в сборке 14376 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="a848e-1286">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="a848e-1287">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-1287">Fixed</span></span>
- <span data-ttu-id="a848e-1288">Удалены некоторые экземпляры, где APT — получение зависает (GH #493)</span><span class="sxs-lookup"><span data-stu-id="a848e-1288">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="a848e-1289">Исправлена проблема, из – за которой не были правильно обработаны пустые подключения</span><span class="sxs-lookup"><span data-stu-id="a848e-1289">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="a848e-1290">Исправлена проблема, при которой не удалось правильно подключить Ramdisk</span><span class="sxs-lookup"><span data-stu-id="a848e-1290">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="a848e-1291">Изменение флагов Accept для сокета UNIX на поддержку (частичные GH #451)</span><span class="sxs-lookup"><span data-stu-id="a848e-1291">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="a848e-1292">Исправлена общая блуескрин, связанная с сетью</span><span class="sxs-lookup"><span data-stu-id="a848e-1292">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="a848e-1293">Исправлена блуескрин при доступе к/прок/[PID]/Task (GH #523)</span><span class="sxs-lookup"><span data-stu-id="a848e-1293">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="a848e-1294">Исправлена высокая загрузка ЦП для некоторых сценариев PTY (GH #488, #504)</span><span class="sxs-lookup"><span data-stu-id="a848e-1294">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="a848e-1295">Дополнительные исправлений и усовершенствования</span><span class="sxs-lookup"><span data-stu-id="a848e-1295">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="a848e-1296">Сборка 14371</span><span class="sxs-lookup"><span data-stu-id="a848e-1296">Build 14371</span></span>
<span data-ttu-id="a848e-1297">Общие сведения о Windows в сборке 14371 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="a848e-1297">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="a848e-1298">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-1298">Fixed</span></span>
- <span data-ttu-id="a848e-1299">Исправлено состязание за синхронизацию с СИГЧЛД и Wait () при использовании птраце</span><span class="sxs-lookup"><span data-stu-id="a848e-1299">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="a848e-1300">Исправлено поведение, когда пути завершаются (GH #432)</span><span class="sxs-lookup"><span data-stu-id="a848e-1300">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="a848e-1301">Исправлена ошибка при сбое переименования или разрыва связи из-за открытых дескрипторов дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="a848e-1301">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="a848e-1302">Дополнительные исправлений и усовершенствования</span><span class="sxs-lookup"><span data-stu-id="a848e-1302">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="a848e-1303">Сборка 14366</span><span class="sxs-lookup"><span data-stu-id="a848e-1303">Build 14366</span></span>
<span data-ttu-id="a848e-1304">Общие сведения о Windows в сборке 14366 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span><span class="sxs-lookup"><span data-stu-id="a848e-1304">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="a848e-1305">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-1305">Fixed</span></span>
- <span data-ttu-id="a848e-1306">Исправление в процессе создания файла с помощью символических ссылок</span><span class="sxs-lookup"><span data-stu-id="a848e-1306">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="a848e-1307">Добавлен листксаттр для Python (GH 385).</span><span class="sxs-lookup"><span data-stu-id="a848e-1307">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="a848e-1308">Дополнительные исправлений и усовершенствования</span><span class="sxs-lookup"><span data-stu-id="a848e-1308">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="a848e-1309">Поддержка syscall</span><span class="sxs-lookup"><span data-stu-id="a848e-1309">Syscall Support</span></span>
-   <span data-ttu-id="a848e-1310">Ниже приведен список новых или улучшенных syscall, которые имеют некоторую реализацию в WSL.</span><span class="sxs-lookup"><span data-stu-id="a848e-1310">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="a848e-1311">Syscall в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="a848e-1311">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="a848e-1312">Сборка 14361</span><span class="sxs-lookup"><span data-stu-id="a848e-1312">Build 14361</span></span>
<span data-ttu-id="a848e-1313">Общие сведения о Windows в сборке 14361 см. в [блоге Windows](https://aka.ms/wip14361).</span><span class="sxs-lookup"><span data-stu-id="a848e-1313">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="a848e-1314">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-1314">Fixed</span></span>
- <span data-ttu-id="a848e-1315">Теперь Дрвфс учитывает регистр при выполнении в Bash в системе Ubuntu в Windows.</span><span class="sxs-lookup"><span data-stu-id="a848e-1315">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="a848e-1316">Пользователи могут иметь в своем регистре. txt и CASE. TXT на дисках/МНТ/к</span><span class="sxs-lookup"><span data-stu-id="a848e-1316">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="a848e-1317">Чувствительность к регистру поддерживается только в Bash на Ubuntu в Windows.</span><span class="sxs-lookup"><span data-stu-id="a848e-1317">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="a848e-1318">Если за пределами Bash NTFS будет сообщать о файлах правильно, но может возникнуть непредвиденное поведение при взаимодействии с файлами из Windows.</span><span class="sxs-lookup"><span data-stu-id="a848e-1318">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="a848e-1319">Корень каждого тома (т. е./МНТ/к) не учитывает регистр</span><span class="sxs-lookup"><span data-stu-id="a848e-1319">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="a848e-1320">Дополнительные сведения об обработке этих файлов в Windows можно найти [здесь](https://support.microsoft.com/en-us/kb/100625).</span><span class="sxs-lookup"><span data-stu-id="a848e-1320">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="a848e-1321">Значительно улучшенная поддержка PTY/TTY.</span><span class="sxs-lookup"><span data-stu-id="a848e-1321">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="a848e-1322">Теперь поддерживаются такие приложения, как ТМУКС (GH #40)</span><span class="sxs-lookup"><span data-stu-id="a848e-1322">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="a848e-1323">Исправлена проблема с установкой, при которой учетные записи пользователей не создавались</span><span class="sxs-lookup"><span data-stu-id="a848e-1323">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="a848e-1324">Оптимизированная структура аргумента командной строки, которая позволяет получить очень длинный список аргументов.</span><span class="sxs-lookup"><span data-stu-id="a848e-1324">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="a848e-1325">(GH #153)</span><span class="sxs-lookup"><span data-stu-id="a848e-1325">(GH #153)</span></span>
- <span data-ttu-id="a848e-1326">Теперь возможность удаления и chmod файлов READ_ONLY из Дрвфс</span><span class="sxs-lookup"><span data-stu-id="a848e-1326">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="a848e-1327">Исправлены некоторые экземпляры, в которых терминал зависает при отключении (GH #43)</span><span class="sxs-lookup"><span data-stu-id="a848e-1327">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="a848e-1328">Теперь на устройствах tty работает chmod и човн</span><span class="sxs-lookup"><span data-stu-id="a848e-1328">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="a848e-1329">Разрешить подключение к 0.0.0.0 и:: AS localhost (GH #388)</span><span class="sxs-lookup"><span data-stu-id="a848e-1329">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="a848e-1330">Сендмсг/реквмсг теперь обрабатывает длину вектора ввода-вывода > 1 (частичный GH #376)</span><span class="sxs-lookup"><span data-stu-id="a848e-1330">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="a848e-1331">Теперь пользователи могут отказаться от автоматически создаваемого файла hosts (GH #398)</span><span class="sxs-lookup"><span data-stu-id="a848e-1331">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="a848e-1332">Автоматически сопоставлять языковой стандарт Linux с языковым стандартом NT во время установки (GH #11)</span><span class="sxs-lookup"><span data-stu-id="a848e-1332">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="a848e-1333">Добавлен файл/прок/СИС/ВМ/сваппинесс (GH #306)</span><span class="sxs-lookup"><span data-stu-id="a848e-1333">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="a848e-1334">страце теперь правильно завершает работу</span><span class="sxs-lookup"><span data-stu-id="a848e-1334">strace now exits correctly</span></span>
- <span data-ttu-id="a848e-1335">Разрешить повторное открытие каналов через/прок/Селф/ФД (GH #222)</span><span class="sxs-lookup"><span data-stu-id="a848e-1335">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="a848e-1336">Скрытие каталогов в разделе%Локалаппдата%\лкссс from Дрвфс (GH #270)</span><span class="sxs-lookup"><span data-stu-id="a848e-1336">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="a848e-1337">Улучшенная обработка bash. exe ~.</span><span class="sxs-lookup"><span data-stu-id="a848e-1337">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="a848e-1338">Теперь поддерживаются такие команды, как "Bash ~-c ls" (GH #467)</span><span class="sxs-lookup"><span data-stu-id="a848e-1338">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="a848e-1339">Сокеты теперь уведомляют еполл Read доступным во время завершения работы (GH #271)</span><span class="sxs-lookup"><span data-stu-id="a848e-1339">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="a848e-1340">лксрун/uninstall улучшает задачу удаления файлов и папок.</span><span class="sxs-lookup"><span data-stu-id="a848e-1340">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="a848e-1341">Исправлено PS-f (GH #246)</span><span class="sxs-lookup"><span data-stu-id="a848e-1341">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="a848e-1342">Улучшенная поддержка приложений X11, таких как Ксемакс (GH #481)</span><span class="sxs-lookup"><span data-stu-id="a848e-1342">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="a848e-1343">Обновленный начальный размер стека потока в соответствии с параметром Ubuntu по умолчанию и правильно сообщает о размере в get_rlimit syscall (GH #172, #258)</span><span class="sxs-lookup"><span data-stu-id="a848e-1343">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="a848e-1344">Улучшена отчетность по именам образов процессов Pico (например, для аудита).</span><span class="sxs-lookup"><span data-stu-id="a848e-1344">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="a848e-1345">Реализована/прок/маунтинфо для команды df</span><span class="sxs-lookup"><span data-stu-id="a848e-1345">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="a848e-1346">Исправлен код ошибки символьную ссылку для дочернего имени.</span><span class="sxs-lookup"><span data-stu-id="a848e-1346">Fixed symlink error code for child name .</span></span> <span data-ttu-id="a848e-1347">и..</span><span class="sxs-lookup"><span data-stu-id="a848e-1347">and ..</span></span>
- <span data-ttu-id="a848e-1348">Дополнительные улучшения исправлений и улучшения</span><span class="sxs-lookup"><span data-stu-id="a848e-1348">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="a848e-1349">Поддержка syscall</span><span class="sxs-lookup"><span data-stu-id="a848e-1349">Syscall Support</span></span>
<span data-ttu-id="a848e-1350">Ниже приведен список новых или улучшенных syscall, которые имеют некоторую реализацию в WSL.</span><span class="sxs-lookup"><span data-stu-id="a848e-1350">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="a848e-1351">Syscall в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="a848e-1351">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="a848e-1352">Сборка 14352</span><span class="sxs-lookup"><span data-stu-id="a848e-1352">Build 14352</span></span>
<span data-ttu-id="a848e-1353">Общие сведения о Windows в сборке 14352 см. в [блоге Windows](https://aka.ms/wip14352).</span><span class="sxs-lookup"><span data-stu-id="a848e-1353">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="a848e-1354">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-1354">Fixed</span></span>
- <span data-ttu-id="a848e-1355">Исправлена проблема, из-за которой большие файлы не были правильно загружены или созданы.</span><span class="sxs-lookup"><span data-stu-id="a848e-1355">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="a848e-1356">Это должно разблокировать NPM и другие сценарии (GH #3, GH #313)</span><span class="sxs-lookup"><span data-stu-id="a848e-1356">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="a848e-1357">Удалены некоторые экземпляры, в которых сокеты зависы</span><span class="sxs-lookup"><span data-stu-id="a848e-1357">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="a848e-1358">Исправлены некоторые ошибки птраце</span><span class="sxs-lookup"><span data-stu-id="a848e-1358">Corrected some ptrace errors</span></span>
- <span data-ttu-id="a848e-1359">Исправлена проблема с WSL, разрешающая имена файлов длиннее 255 символов.</span><span class="sxs-lookup"><span data-stu-id="a848e-1359">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="a848e-1360">Улучшенная поддержка символов, отличных от английского</span><span class="sxs-lookup"><span data-stu-id="a848e-1360">Improved support for non-English characters</span></span>
- <span data-ttu-id="a848e-1361">Добавить текущие данные о часовом поясе Windows и назначить их по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a848e-1361">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="a848e-1362">Уникальный идентификатор устройства для каждой точки подключения (исправление JRE — GH #49)</span><span class="sxs-lookup"><span data-stu-id="a848e-1362">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="a848e-1363">Устранена ошибка с путями, содержащими "."</span><span class="sxs-lookup"><span data-stu-id="a848e-1363">Correct issue with paths containing “.”</span></span> <span data-ttu-id="a848e-1364">и ".."</span><span class="sxs-lookup"><span data-stu-id="a848e-1364">and “..”</span></span>
- <span data-ttu-id="a848e-1365">Добавлена поддержка FIFO (GH #71)</span><span class="sxs-lookup"><span data-stu-id="a848e-1365">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="a848e-1366">Обновлен формат resolv. conf в соответствии с собственным форматом Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="a848e-1366">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="a848e-1367">Некоторые прокфс очистки</span><span class="sxs-lookup"><span data-stu-id="a848e-1367">Some procfs cleanup</span></span>
- <span data-ttu-id="a848e-1368">Включенная проверка связи для консолей администрирования (GH #18)</span><span class="sxs-lookup"><span data-stu-id="a848e-1368">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="a848e-1369">Поддержка syscall</span><span class="sxs-lookup"><span data-stu-id="a848e-1369">Syscall Support</span></span>
<span data-ttu-id="a848e-1370">Ниже приведен список новых или улучшенных syscall, которые имеют некоторую реализацию в WSL.</span><span class="sxs-lookup"><span data-stu-id="a848e-1370">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="a848e-1371">Syscall в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="a848e-1371">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="a848e-1372">Сборка 14342</span><span class="sxs-lookup"><span data-stu-id="a848e-1372">Build 14342</span></span>
<span data-ttu-id="a848e-1373">Общие сведения о Windows для сборки 14342 в [блоге Windows](https://aka.ms/wip14342).</span><span class="sxs-lookup"><span data-stu-id="a848e-1373">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="a848e-1374">Сведения о Волфс и Дривефс можно найти в [блоге WSL](https://blogs.msdn.microsoft.com/wsl).</span><span class="sxs-lookup"><span data-stu-id="a848e-1374">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="a848e-1375">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-1375">Fixed</span></span>
- <span data-ttu-id="a848e-1376">Исправлена проблема с установкой, когда пользователь Windows в имени пользователя содержит символы Юникода</span><span class="sxs-lookup"><span data-stu-id="a848e-1376">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="a848e-1377">Решение apt-get update udev в разделе часто задаваемых вопросов теперь предоставляется по умолчанию при первом запуске</span><span class="sxs-lookup"><span data-stu-id="a848e-1377">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="a848e-1378">Включенные символических ссылок в каталогах<drive>дривефс (/МНТ/)</span><span class="sxs-lookup"><span data-stu-id="a848e-1378">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="a848e-1379">Символических ссылок теперь работает между Дривефс и Волфс</span><span class="sxs-lookup"><span data-stu-id="a848e-1379">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="a848e-1380">Устранена ошибка при анализе пути верхнего уровня: Ls.//теперь будет работать должным образом</span><span class="sxs-lookup"><span data-stu-id="a848e-1380">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="a848e-1381">NPM Install on Дривефс и параметры-g теперь работают</span><span class="sxs-lookup"><span data-stu-id="a848e-1381">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="a848e-1382">Исправлена проблема, препятствующая запуску сервера PHP</span><span class="sxs-lookup"><span data-stu-id="a848e-1382">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="a848e-1383">Обновленные значения среды по умолчанию, такие как $PATH, близко соответствуют машинному стандарту Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="a848e-1383">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="a848e-1384">Добавлена еженедельная задача обслуживания в Windows для обновления кэша пакетов apt.</span><span class="sxs-lookup"><span data-stu-id="a848e-1384">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="a848e-1385">Исправлена проблема с проверкой заголовка ELF, WSL теперь поддерживает все параметры Мелкор</span><span class="sxs-lookup"><span data-stu-id="a848e-1385">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="a848e-1386">Оболочка ЗШ работает</span><span class="sxs-lookup"><span data-stu-id="a848e-1386">Zsh shell is functional</span></span>
- <span data-ttu-id="a848e-1387">Теперь поддерживаются предварительно скомпилированные двоичные файлы Go</span><span class="sxs-lookup"><span data-stu-id="a848e-1387">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="a848e-1388">Запрос первого запуска bash. exe теперь локализован правильно</span><span class="sxs-lookup"><span data-stu-id="a848e-1388">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="a848e-1389">/прок/меминфо теперь возвращает правильные сведения</span><span class="sxs-lookup"><span data-stu-id="a848e-1389">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="a848e-1390">Сокеты теперь поддерживаются в VFS</span><span class="sxs-lookup"><span data-stu-id="a848e-1390">Sockets now supported in VFS</span></span>
- <span data-ttu-id="a848e-1391">/Дев теперь подключен как темпфс</span><span class="sxs-lookup"><span data-stu-id="a848e-1391">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="a848e-1392">FIFO теперь поддерживается</span><span class="sxs-lookup"><span data-stu-id="a848e-1392">Fifo now supported</span></span>
- <span data-ttu-id="a848e-1393">Многоядерные системы теперь правильно отображаются в/прок/кпуинфо</span><span class="sxs-lookup"><span data-stu-id="a848e-1393">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="a848e-1394">Дополнительные улучшения и сообщения об ошибках, загружаемые во время первого запуска</span><span class="sxs-lookup"><span data-stu-id="a848e-1394">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="a848e-1395">Усовершенствования syscall и исправлений.</span><span class="sxs-lookup"><span data-stu-id="a848e-1395">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="a848e-1396">Поддерживаемый список syscall ниже.</span><span class="sxs-lookup"><span data-stu-id="a848e-1396">Supported syscall list below.</span></span>
- <span data-ttu-id="a848e-1397">Дополнительные исправлений и усовершенствования</span><span class="sxs-lookup"><span data-stu-id="a848e-1397">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="a848e-1398">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="a848e-1398">Known Issues</span></span>
- <span data-ttu-id="a848e-1399">Не разрешается ".."</span><span class="sxs-lookup"><span data-stu-id="a848e-1399">Not resolving ‘..’</span></span> <span data-ttu-id="a848e-1400">правильно в Дривефс в некоторых случаях</span><span class="sxs-lookup"><span data-stu-id="a848e-1400">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="a848e-1401">Поддержка syscall</span><span class="sxs-lookup"><span data-stu-id="a848e-1401">Syscall Support</span></span>
<span data-ttu-id="a848e-1402">Ниже приведен список новых или улучшенных syscall, которые имеют некоторую реализацию в WSL.</span><span class="sxs-lookup"><span data-stu-id="a848e-1402">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="a848e-1403">Syscall в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="a848e-1403">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FCHOWNAT`<br/>
`GETEUID`<br/>
`GETGID`<br/>
`GETRESUID`<br/>
`GETXATTR`<br/>
`PTRACE`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETXATTR`<br/>
<br/>

## <a name="build-14332"></a><span data-ttu-id="a848e-1404">Сборка 14332</span><span class="sxs-lookup"><span data-stu-id="a848e-1404">Build 14332</span></span>

<span data-ttu-id="a848e-1405">Общие сведения о Windows в сборке 14332 см. в [блоге Windows](https://aka.ms/wip14332).</span><span class="sxs-lookup"><span data-stu-id="a848e-1405">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="a848e-1406">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-1406">Fixed</span></span>
- <span data-ttu-id="a848e-1407">Улучшенное создание resolv. conf, включая определение приоритета записей DNS</span><span class="sxs-lookup"><span data-stu-id="a848e-1407">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="a848e-1408">Проблемы с перемещением файлов и каталогов между/mnt и/mnt дисками</span><span class="sxs-lookup"><span data-stu-id="a848e-1408">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="a848e-1409">Теперь можно создавать tar файлы с помощью символических ссылок</span><span class="sxs-lookup"><span data-stu-id="a848e-1409">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="a848e-1410">Добавлен каталог/рун/Локк по умолчанию при создании экземпляра</span><span class="sxs-lookup"><span data-stu-id="a848e-1410">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="a848e-1411">Обновление/Дев/Нулл для возврата правильных сведений о stat</span><span class="sxs-lookup"><span data-stu-id="a848e-1411">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="a848e-1412">Дополнительные ошибки при загрузке во время первого запуска</span><span class="sxs-lookup"><span data-stu-id="a848e-1412">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="a848e-1413">Усовершенствования syscall и исправлений.</span><span class="sxs-lookup"><span data-stu-id="a848e-1413">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="a848e-1414">Поддерживаемый список syscall ниже.</span><span class="sxs-lookup"><span data-stu-id="a848e-1414">Supported syscall list below.</span></span>
- <span data-ttu-id="a848e-1415">Дополнительные улучшения исправлений и улучшения</span><span class="sxs-lookup"><span data-stu-id="a848e-1415">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="a848e-1416">Поддержка syscall</span><span class="sxs-lookup"><span data-stu-id="a848e-1416">Syscall Support</span></span>
<span data-ttu-id="a848e-1417">Ниже приведен новый объект syscall, имеющий некоторую реализацию в WSL.</span><span class="sxs-lookup"><span data-stu-id="a848e-1417">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="a848e-1418">Объект syscall в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут поддерживаться не все параметры.</span><span class="sxs-lookup"><span data-stu-id="a848e-1418">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="a848e-1419">Сборка 14328</span><span class="sxs-lookup"><span data-stu-id="a848e-1419">Build 14328</span></span>

<span data-ttu-id="a848e-1420">Общие сведения о Windows в сборке 14332 см. в [блоге Windows](https://aka.ms/wip14328).</span><span class="sxs-lookup"><span data-stu-id="a848e-1420">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="a848e-1421">Новые возможности</span><span class="sxs-lookup"><span data-stu-id="a848e-1421">New Features</span></span>
* <span data-ttu-id="a848e-1422">Теперь поддерживаются пользователи Linux.</span><span class="sxs-lookup"><span data-stu-id="a848e-1422">Now support Linux users.</span></span>  <span data-ttu-id="a848e-1423">При установке Bash в Ubuntu в Windows будет предложено создать пользователя Linux.</span><span class="sxs-lookup"><span data-stu-id="a848e-1423">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="a848e-1424">Дополнительные сведения см. на странице https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="a848e-1424">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="a848e-1425">Для имени узла теперь задано имя компьютера Windows, больше нет@localhost</span><span class="sxs-lookup"><span data-stu-id="a848e-1425">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="a848e-1426">Дополнительные сведения о сборке 14328 см. по адресу: https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="a848e-1426">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="a848e-1427">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="a848e-1427">Fixed</span></span>
* <span data-ttu-id="a848e-1428">Усовершенствования символьную ссылку для файлов,<drive> отличных от/МНТ/</span><span class="sxs-lookup"><span data-stu-id="a848e-1428">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="a848e-1429">Установка NPM теперь работает</span><span class="sxs-lookup"><span data-stu-id="a848e-1429">npm install now works</span></span>
    * <span data-ttu-id="a848e-1430">JDK/JRE теперь можно установить с помощью инструкций, приведенных [здесь](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span><span class="sxs-lookup"><span data-stu-id="a848e-1430">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="a848e-1431">известная ошибка: символических ссылок не работает для подключений Windows.</span><span class="sxs-lookup"><span data-stu-id="a848e-1431">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="a848e-1432">Функции будут доступны в последующей сборке</span><span class="sxs-lookup"><span data-stu-id="a848e-1432">Functionality will be available in a later build</span></span>
* <span data-ttu-id="a848e-1433">экраны Top и Htop Now</span><span class="sxs-lookup"><span data-stu-id="a848e-1433">top and htop now display</span></span>
* <span data-ttu-id="a848e-1434">Дополнительные сообщения об ошибках для некоторых сбоев установки</span><span class="sxs-lookup"><span data-stu-id="a848e-1434">Additional error messages for some install failures</span></span>
* <span data-ttu-id="a848e-1435">Усовершенствования syscall и исправлений.</span><span class="sxs-lookup"><span data-stu-id="a848e-1435">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="a848e-1436">Поддерживаемый список syscall ниже.</span><span class="sxs-lookup"><span data-stu-id="a848e-1436">Supported syscall list below.</span></span>
* <span data-ttu-id="a848e-1437">Дополнительные улучшения исправлений и улучшения</span><span class="sxs-lookup"><span data-stu-id="a848e-1437">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="a848e-1438">Поддержка syscall</span><span class="sxs-lookup"><span data-stu-id="a848e-1438">Syscall Support</span></span>
<span data-ttu-id="a848e-1439">Ниже приведен список syscall, имеющих некоторую реализацию в WSL.</span><span class="sxs-lookup"><span data-stu-id="a848e-1439">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="a848e-1440">Syscall в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="a848e-1440">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`ACCEPT`<br/>
`ACCEPT4`<br/>
`ACCESS`<br/>
`ALARM`<br/>
`ARCH_PRCTL`<br/>
`BIND`<br/>
`BRK`<br/>
`CAPGET`<br/>
`CAPSET`<br/>
`CHDIR`<br/>
`CHMOD`<br/>
`CHOWN`<br/>
`CLOCK_GETRES`<br/>
`CLOCK_GETTIME`<br/>
`CLOCK_NANOSLEEP`<br/>
`CLONE`<br/>
`CLOSE`<br/>
`CONNECT`<br/>
`CREAT`<br/>
`DUP`<br/>
`DUP2`<br/>
`DUP3`<br/>
`EPOLL_CREATE`<br/>
`EPOLL_CREATE1`<br/>
`EPOLL_CTL`<br/>
`EPOLL_WAIT`<br/>
`EVENTFD`<br/>
`EVENTFD2`<br/>
`EXECVE`<br/>
`EXIT`<br/>
`EXIT_GROUP`<br/>
`FACCESSAT`<br/>
`FADVISE64`<br/>
`FCHDIR`<br/>
`FCHMOD`<br/>
`FCHMODAT`<br/>
`FCHOWN`<br/>
`FCHOWNAT`<br/>
`FCNTL64`<br/>
`FDATASYNC`<br/>
`FLOCK`<br/>
`FORK`<br/>
`FSETXATTR`<br/>
`FSTAT64`<br/>
`FSTATAT64`<br/>
`FSTATFS64`<br/>
`FSYNC`<br/>
`FTRUNCATE`<br/>
`FTRUNCATE64`<br/>
`FUTEX`<br/>
`GETCPU`<br/>
`GETCWD`<br/>
`GETDENTS`<br/>
`GETDENTS64`<br/>
`GETEGID`<br/>
`GETEGID16`<br/>
`GETEUID`<br/>
`GETEUID16`<br/>
`GETGID`<br/>
`GETGID16`<br/>
`GETGROUPS`<br/>
`GETPEERNAME`<br/>
`GETPGID`<br/>
`GETPGRP`<br/>
`GETPID`<br/>
`GETPPID`<br/>
`GETPRIORITY`<br/>
`GETRESGID`<br/>
`GETRESGID16`<br/>
`GETRESUID`<br/>
`GETRESUID16`<br/>
`GETRLIMIT`<br/>
`GETRUSAGE`<br/>
`GETSID`<br/>
`GETSOCKNAME`<br/>
`GETSOCKOPT`<br/>
`GETTID`<br/>
`GETTIMEOFDAY`<br/>
`GETUID`<br/>
`GETUID16`<br/>
`GETXATTR`<br/>
`GET_ROBUST_LIST`<br/>
`GET_THREAD_AREA`<br/>
`INOTIFY_ADD_WATCH`<br/>
`INOTIFY_INIT`<br/>
`INOTIFY_RM_WATCH`<br/>
`IOCTL`<br/>
`IOPRIO_GET`<br/>
`IOPRIO_SET`<br/>
`KEYCTL`<br/>
`KILL`<br/>
`LCHOWN`<br/>
`LINK`<br/>
`LINKAT`<br/>
`LISTEN`<br/>
`LLSEEK`<br/>
`LSEEK`<br/>
`LSTAT64`<br/>
`MADVISE`<br/>
`MKDIR`<br/>
`MKDIRAT`<br/>
`MKNOD`<br/>
`MLOCK`<br/>
`MMAP`<br/>
`MMAP2`<br/>
`MOUNT`<br/>
`MPROTECT`<br/>
`MREMAP`<br/>
`MSYNC`<br/>
`MUNLOCK`<br/>
`MUNMAP`<br/>
`NANOSLEEP`<br/>
`NEWUNAME`<br/>
`OPEN`<br/>
`OPENAT`<br/>
`PAUSE`<br/>
`PERF_EVENT_OPEN`<br/>
`PERSONALITY`<br/>
`PIPE`<br/>
`PIPE2`<br/>
`POLL`<br/>
`PPOLL`<br/>
`PRCTL`<br/>
`PREAD64`<br/>
`PROCESS_VM_READV`<br/>
`PROCESS_VM_WRITEV`<br/>
`PSELECT6`<br/>
`PTRACE`<br/>
`PWRITE64`<br/>
`READ`<br/>
`READLINK`<br/>
`READV`<br/>
`REBOOT`<br/>
`RECV`<br/>
`RECVFROM`<br/>
`RECVMSG`<br/>
`RENAME`<br/>
`RMDIR`<br/>
`RT_SIGACTION`<br/>
`RT_SIGPENDING`<br/>
`RT_SIGPROCMASK`<br/>
`RT_SIGRETURN`<br/>
`RT_SIGSUSPEND`<br/>
`RT_SIGTIMEDWAIT`<br/>
`SCHED_GETAFFINITY`<br/>
`SCHED_GETPARAM`<br/>
`SCHED_GETSCHEDULER`<br/>
`SCHED_GET_PRIORITY_MAX`<br/>
`SCHED_GET_PRIORITY_MIN`<br/>
`SCHED_SETAFFINITY`<br/>
`SCHED_SETPARAM`<br/>
`SCHED_SETSCHEDULER`<br/>
`SCHED_YIELD`<br/>
`SELECT`<br/>
`SEND`<br/>
`SENDMMSG`<br/>
`SENDMSG`<br/>
`SENDTO`<br/>
`SETDOMAINNAME`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETITIMER`<br/>
`SETPGID`<br/>
`SETPRIORITY`<br/>
`SETREGID`<br/>
`SETRESGID`<br/>
`SETRESUID`<br/>
`SETREUID`<br/>
`SETRLIMIT`<br/>
`SETSID`<br/>
`SETSOCKOPT`<br/>
`SETTIMEOFDAY`<br/>
`SETUID`<br/>
`SETXATTR`<br/>
`SET_ROBUST_LIST`<br/>
`SET_THREAD_AREA`<br/>
`SET_TID_ADDRESS`<br/>
`SHUTDOWN`<br/>
`SIGACTION`<br/>
`SIGALTSTACK`<br/>
`SIGPENDING`<br/>
`SIGPROCMASK`<br/>
`SIGRETURN`<br/>
`SIGSUSPEND`<br/>
`SOCKET`<br/>
`SOCKETCALL`<br/>
`SOCKETPAIR`<br/>
`SPLICE`<br/>
`STAT64`<br/>
`STATFS64`<br/>
`SYMLINK`<br/>
`SYMLINKAT`<br/>
`SYNC`<br/>
`SYSINFO`<br/>
`TEE`<br/>
`TGKILL`<br/>
`TIME`<br/>
`TIMERFD_CREATE`<br/>
`TIMERFD_GETTIME`<br/>
`TIMERFD_SETTIME`<br/>
`TIMES`<br/>
`TKILL`<br/>
`TRUNCATE`<br/>
`TRUNCATE64`<br/>
`UMASK`<br/>
`UMOUNT`<br/>
`UMOUNT2`<br/>
`UNLINK`<br/>
`UNLINKAT`<br/>
`UNSHARE`<br/>
`UTIME`<br/>
`UTIMENSAT`<br/>
`UTIMES`<br/>
`VFORK`<br/>
`WAIT4`<br/>
`WAITPID`<br/>
`WRITE`<br/>
`WRITEV`<br/>
