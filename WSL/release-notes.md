---
title: Заметки о выпуске для подсистемы Windows для Linux
description: Заметки о выпуске для подсистемы Windows для Linux.  Обновляется еженедельно.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: 3eee7ff6d1f8302e98cde84fccabf5d9113c83f2
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063632"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="d707b-105">Заметки о выпуске для подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="d707b-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-18342"></a><span data-ttu-id="d707b-106">Сборки 18342</span><span class="sxs-lookup"><span data-stu-id="d707b-106">Build 18342</span></span>
<span data-ttu-id="d707b-107">Windows, общие сведения о сборке 18342 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span><span class="sxs-lookup"><span data-stu-id="d707b-107">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-108">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-108">WSL</span></span>
* <span data-ttu-id="d707b-109">Мы добавили возможность для пользователей для доступа к файлам Linux в дистрибутив WSL из Windows.</span><span class="sxs-lookup"><span data-stu-id="d707b-109">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="d707b-110">Эти файлы можно получить с помощью командной строки, а также приложения Windows, такие как проводник, VSCode, и т.д. можно взаимодействовать с этими файлами.</span><span class="sxs-lookup"><span data-stu-id="d707b-110">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="d707b-111">Доступ к файлам, перейдя по адресу \\ \\wsl$\\< distro_name >, или просмотреть список запуска выпусков, перейдя по адресу \\ \\wsl$</span><span class="sxs-lookup"><span data-stu-id="d707b-111">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="d707b-112">Добавление дополнительных тегов информации о ЦП и исправить значения Cpus_allowed [_list] [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="d707b-112">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="d707b-113">Поддерживает exec из потока без лидера [GH 3800]</span><span class="sxs-lookup"><span data-stu-id="d707b-113">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="d707b-114">Считать ошибок при обновлении конфигурации, не являющиеся неустранимыми [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="d707b-114">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="d707b-115">Обновить binfmt для правильной обработки смещения [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="d707b-115">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="d707b-116">Включение сопоставления сетевых дисков для планирования 9 [GH 3854]</span><span class="sxs-lookup"><span data-stu-id="d707b-116">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="d707b-117">Поддержка Windows -> Linux и Linux "->" преобразование пути Windows для подключений привязки</span><span class="sxs-lookup"><span data-stu-id="d707b-117">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="d707b-118">Создать разделы, доступные только для чтения для сопоставления на файлы, открытые только для чтения</span><span class="sxs-lookup"><span data-stu-id="d707b-118">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="d707b-119">Сборки 18334</span><span class="sxs-lookup"><span data-stu-id="d707b-119">Build 18334</span></span>
<span data-ttu-id="d707b-120">Windows, общие сведения о сборке 18334 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span><span class="sxs-lookup"><span data-stu-id="d707b-120">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-121">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-121">WSL</span></span>
* <span data-ttu-id="d707b-122">Изменение способа является сопоставления Windows часового пояса в часовой пояс Linux [GH 3747]</span><span class="sxs-lookup"><span data-stu-id="d707b-122">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="d707b-123">Устранить утечки памяти и добавьте новые строковые функции преобразования [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="d707b-123">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="d707b-124">SIGCONT на threadgroup с потоками, не является холостой [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="d707b-124">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="d707b-125">Правильно отображать сокета и epoll дескрипторов файлов в /proc/self/fd</span><span class="sxs-lookup"><span data-stu-id="d707b-125">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="d707b-126">Сборки 18305</span><span class="sxs-lookup"><span data-stu-id="d707b-126">Build 18305</span></span>
<span data-ttu-id="d707b-127">Windows, общие сведения о сборке 18305 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span><span class="sxs-lookup"><span data-stu-id="d707b-127">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-128">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-128">WSL</span></span>
* <span data-ttu-id="d707b-129">потоки потерять доступ к файлам, когда основной поток выходит из [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="d707b-129">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="d707b-130">TIOCSCTTY должен игнорировать параметром «force», если он не требуется [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="d707b-130">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="d707b-131">Усовершенствования командной строки wsl.exe и добавление импорта или экспорта функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="d707b-131">wsl.exe command line improvements and addition of import / export functionality.</span></span>
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

## <a name="build-18277"></a><span data-ttu-id="d707b-132">Сборки 18277</span><span class="sxs-lookup"><span data-stu-id="d707b-132">Build 18277</span></span>
<span data-ttu-id="d707b-133">Windows, общие сведения о сборке 18277 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span><span class="sxs-lookup"><span data-stu-id="d707b-133">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-134">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-134">WSL</span></span>
* <span data-ttu-id="d707b-135">Устранить ошибку «интерфейс не поддерживается», представленные в сборке 18272 [GH 3645]</span><span class="sxs-lookup"><span data-stu-id="d707b-135">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="d707b-136">Игнорировать флаг MNT_FORCE umount syscall [GH 3605]</span><span class="sxs-lookup"><span data-stu-id="d707b-136">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="d707b-137">Переключение WSL взаимодействия использовать официальный интерфейс API CreatePseudoConsole</span><span class="sxs-lookup"><span data-stu-id="d707b-137">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="d707b-138">Ведение отсутствие времени ожидания при перезапуске FUTEX_WAIT</span><span class="sxs-lookup"><span data-stu-id="d707b-138">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="d707b-139">Сборки 18272</span><span class="sxs-lookup"><span data-stu-id="d707b-139">Build 18272</span></span>
<span data-ttu-id="d707b-140">Windows, общие сведения о сборке 18272 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span><span class="sxs-lookup"><span data-stu-id="d707b-140">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-141">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-141">WSL</span></span>
* <span data-ttu-id="d707b-142">**ПРЕДУПРЕЖДЕНИЕ:** Имеется проблема в этой сборке, который делает WSL вышел из строя.</span><span class="sxs-lookup"><span data-stu-id="d707b-142">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="d707b-143">При попытке запуска вашего дистрибутива вы увидите сообщение об ошибке «Интерфейс не поддерживается».</span><span class="sxs-lookup"><span data-stu-id="d707b-143">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="d707b-144">Проблема была устранена и будет находиться в следующей неделе Insider быстрого построения.</span><span class="sxs-lookup"><span data-stu-id="d707b-144">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="d707b-145">Если вы уже установили этой сборки, которые можно выполнить откат к предыдущей сборки Windows, с помощью «Вернитесь к предыдущей версии Windows 10» в параметрах "->" обновления и безопасности -> восстановления.</span><span class="sxs-lookup"><span data-stu-id="d707b-145">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="d707b-146">Сборки 18267</span><span class="sxs-lookup"><span data-stu-id="d707b-146">Build 18267</span></span>
<span data-ttu-id="d707b-147">Windows, общие сведения о сборке 18267 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span><span class="sxs-lookup"><span data-stu-id="d707b-147">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-148">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-148">WSL</span></span>
* <span data-ttu-id="d707b-149">Устранить проблему, где может не быть компании появились следующие зомби процесс и будут храниться неограниченно долго.</span><span class="sxs-lookup"><span data-stu-id="d707b-149">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="d707b-150">WslRegisterDistribution зависает, если сообщение об ошибке превышает максимальную длину [GH 3592]</span><span class="sxs-lookup"><span data-stu-id="d707b-150">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="d707b-151">Разрешить fsync для успешного выполнения только для чтения файлов на DrvFs [GH 3556]</span><span class="sxs-lookup"><span data-stu-id="d707b-151">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="d707b-152">Убедитесь, что каталоги/Bin и/sbin существуют перед созданием символических ссылок внутри [GH 3584]</span><span class="sxs-lookup"><span data-stu-id="d707b-152">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="d707b-153">Добавлен механизм времени ожидания завершения экземпляра для экземпляров WSL.</span><span class="sxs-lookup"><span data-stu-id="d707b-153">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="d707b-154">В настоящее время, время ожидания составляет 15 секунд, это означает, что экземпляр будет завершена 15 секунд, после выхода из системы последнего WSL процесса.</span><span class="sxs-lookup"><span data-stu-id="d707b-154">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="d707b-155">К немедленному завершению дистрибутив, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d707b-155">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="d707b-156">Построение 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="d707b-156">Build 17763 (1809)</span></span>
<span data-ttu-id="d707b-157">Windows, общие сведения о сборке 17763 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span><span class="sxs-lookup"><span data-stu-id="d707b-157">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-158">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-158">WSL</span></span>
* <span data-ttu-id="d707b-159">Проверка разрешений SetPriority syscall слишком строгие для изменения одинаковый приоритет потока [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="d707b-159">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="d707b-160">Убедитесь, что время прерываний несмещенной используется для время загрузки, чтобы избежать возвращения отрицательные значения для clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="d707b-160">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="d707b-161">Обработка символических ссылок в интерпретаторе binfmt WSL [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="d707b-161">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="d707b-162">Более эффективная обработка очистки дескриптора файла лидером threadgroup.</span><span class="sxs-lookup"><span data-stu-id="d707b-162">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="d707b-163">Переключение WSL для использования вместо KeQueryPerformanceCounter KeQueryInterruptTimePrecise, чтобы избежать переполнения [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="d707b-163">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="d707b-164">Ptrace присоединение может привести к плохой возвращаемого значения из системных вызовов [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="d707b-164">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="d707b-165">Исправления, связанные с несколько AF_UNIX выдает [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="d707b-165">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="d707b-166">Устранить проблему, которая могла привести к WSL взаимодействия с ошибкой, если текущий рабочий каталог не меньше 5 символов [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="d707b-166">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="d707b-167">Избежать сбоя замыкания соединений к несуществующему порты [GH 3286] один секунда</span><span class="sxs-lookup"><span data-stu-id="d707b-167">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="d707b-168">Добавьте файл-заглушку /proc/sys/fs/file-max [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="d707b-168">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="d707b-169">Более точные сведения об области IPV6.</span><span class="sxs-lookup"><span data-stu-id="d707b-169">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="d707b-170">Поддержка PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="d707b-170">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="d707b-171">Передать файловой системы, случайно очистки событий активации edge epoll [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="d707b-171">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="d707b-172">Запущено через символическую ссылку NTFS исполняемого файла Win32 не учитывает имя символьную ссылку [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="d707b-172">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="d707b-173">Улучшенная поддержка зомби [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="d707b-173">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="d707b-174">Добавьте записи wsl.conf для управления поведением взаимодействия Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="d707b-174">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="d707b-175">Исправление ошибки, не всегда возвращает тип семейства UNIX сокета [GH 1774] getsockname</span><span class="sxs-lookup"><span data-stu-id="d707b-175">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="d707b-176">Добавлена поддержка TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="d707b-176">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="d707b-177">Сокеты, без блокировки, в процессе подключения должен возвращать EAGAIN попытки записи [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="d707b-177">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="d707b-178">Поддержка взаимодействия на виртуальными жесткими дисками [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="d707b-178">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="d707b-179">Исправьте проблему на корневую папку [GH 3304] проверки разрешений</span><span class="sxs-lookup"><span data-stu-id="d707b-179">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="d707b-180">Ограниченная поддержка запросы IOCTL клавиатуры TTY KDGKBTYPE, KDGKBMODE и KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="d707b-180">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="d707b-181">Приложения пользовательского интерфейса Windows должен выполняться, даже в том случае, когда запускается в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="d707b-181">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="d707b-182">Добавление wsl -u или--пользователя параметр [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="d707b-182">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="d707b-183">Устранение проблем запуска WSL в том случае, если включена быстрая загрузка [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="d707b-183">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="d707b-184">Сокеты UNIX необходимо сохранить учетные данные отключенных однорангового узла [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="d707b-184">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="d707b-185">Сокеты Unix неблокирующие бессрочно завершились с EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="d707b-185">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="d707b-186">случай = off — тип [GH 2937, 3212, 3328] подключить новый drvfs по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d707b-186">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="d707b-187">См. в разделе [блог](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) Дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="d707b-187">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="d707b-188">Добавьте wslconfig / завершения остановки выполнения распределения.</span><span class="sxs-lookup"><span data-stu-id="d707b-188">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="d707b-189">Устранена проблема с контекст оболочки WSL пунктов меню, которые не обрабатывают правильно путей с пробелами.</span><span class="sxs-lookup"><span data-stu-id="d707b-189">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="d707b-190">Предоставлять чувствительность к регистру-directory как расширенный атрибут</span><span class="sxs-lookup"><span data-stu-id="d707b-190">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="d707b-191">ARM64: Эмулировать операций обслуживания кэша.</span><span class="sxs-lookup"><span data-stu-id="d707b-191">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="d707b-192">Разрешить [проблема dotnet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="d707b-192">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="d707b-193">DrvFs: только unescape символов в диапазоне частных, которые соответствуют в escape-символ.</span><span class="sxs-lookup"><span data-stu-id="d707b-193">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="d707b-194">Исправление ошибки из за другой в проверка длины интерпретатор средство синтаксического анализа ELF [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="d707b-194">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="d707b-195">WSL абсолютный таймеров с помощью времени в прошлом не срабатывают [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="d707b-195">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="d707b-196">Убедитесь, вновь точки повторного анализа созданный таким образом, перечислены в родительском каталоге.</span><span class="sxs-lookup"><span data-stu-id="d707b-196">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="d707b-197">Атомарным образом создайте каталоги с учетом регистра DrvFs.</span><span class="sxs-lookup"><span data-stu-id="d707b-197">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="d707b-198">Исправлена проблема, дополнительный, где многопоточные операции может вернуть ENOENT, несмотря на то, что файл существует.</span><span class="sxs-lookup"><span data-stu-id="d707b-198">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="d707b-199">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="d707b-199">[GH 2712]</span></span>
* <span data-ttu-id="d707b-200">Фиксированный WSL запустите сбой при включении UMCI.</span><span class="sxs-lookup"><span data-stu-id="d707b-200">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="d707b-201">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="d707b-201">[GH 3020]</span></span>
* <span data-ttu-id="d707b-202">Добавление контекстного меню обозревателя для запуска WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="d707b-202">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="d707b-203">Чтобы использовать этот параметр, удерживайте клавишу shift и щелкните правой кнопкой мыши в окне проводника.</span><span class="sxs-lookup"><span data-stu-id="d707b-203">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="d707b-204">Исправить сокет Unix неблокирующее поведение [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="d707b-204">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="d707b-205">Исправление, выступающие NETLINK команды в GH 2026.</span><span class="sxs-lookup"><span data-stu-id="d707b-205">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="d707b-206">Добавлена поддержка Флаги распространения подключения [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="d707b-206">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="d707b-207">Устранена проблема с усечения не вызывает события inotify [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="d707b-207">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="d707b-208">Добавлен параметр--exec параметр для wsl.exe для вызова единого двоичного файла без оболочки.</span><span class="sxs-lookup"><span data-stu-id="d707b-208">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="d707b-209">Добавлен параметр--параметр распределения для wsl.exe для выбора конкретного дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="d707b-209">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="d707b-210">Ограниченная поддержка dmesg.</span><span class="sxs-lookup"><span data-stu-id="d707b-210">Limited support for dmesg.</span></span> <span data-ttu-id="d707b-211">Теперь приложения могут входить dmesg.</span><span class="sxs-lookup"><span data-stu-id="d707b-211">Applications can now log to dmesg.</span></span> <span data-ttu-id="d707b-212">Драйвер WSL входит команда dmesg ограниченные сведения.</span><span class="sxs-lookup"><span data-stu-id="d707b-212">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="d707b-213">В будущем это может быть расширен для выполнения другие сведения или диагностики от драйвера.</span><span class="sxs-lookup"><span data-stu-id="d707b-213">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="d707b-214">Примечание: команда dmesg в настоящее время поддерживается через `/dev/kmsg` интерфейс устройства.</span><span class="sxs-lookup"><span data-stu-id="d707b-214">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> `syslog` <span data-ttu-id="d707b-215">интерфейс syscall еще не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d707b-215">syscall interface is not yet supported.</span></span> <span data-ttu-id="d707b-216">И, таким образом, некоторые `dmesg` параметры командной строки, такие как `-S`, `-C` не работают.</span><span class="sxs-lookup"><span data-stu-id="d707b-216">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="d707b-217">Изменение по умолчанию gid и режима последовательной устройств в соответствии с машинный код [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="d707b-217">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="d707b-218">DrvFs теперь поддерживает дополнительные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="d707b-218">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="d707b-219">Примечание. DrvFs имеет некоторые ограничения на основе имени изменяемого дополнительные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="d707b-219">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="d707b-220">Некоторые символы (например «/», ":" и "\*") не разрешено и расширенные имена атрибутов не учитывается регистр на DrvFs</span><span class="sxs-lookup"><span data-stu-id="d707b-220">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="d707b-221">Сборки 18252 (пропустить вперед)</span><span class="sxs-lookup"><span data-stu-id="d707b-221">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="d707b-222">Windows, общие сведения о сборке 18252 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span><span class="sxs-lookup"><span data-stu-id="d707b-222">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-223">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-223">WSL</span></span>
* <span data-ttu-id="d707b-224">Переместить двоичные файлы init и bsdtar из библиотеки dll lxssmanager и поместить в папку выполняемых рядом отдельных инструментов</span><span class="sxs-lookup"><span data-stu-id="d707b-224">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="d707b-225">Устранить конфликт вокруг закрытие дескриптора файла, при использовании CLONE_FILES</span><span class="sxs-lookup"><span data-stu-id="d707b-225">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="d707b-226">Обрабатывать необязательных полях в /proc/pid/mountinfo при переводе DrvFs пути</span><span class="sxs-lookup"><span data-stu-id="d707b-226">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="d707b-227">Разрешить mknod DrvFs небезопасная поддержки метаданных для S_IFREG</span><span class="sxs-lookup"><span data-stu-id="d707b-227">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="d707b-228">Только для чтения файлов, создаваемых на DrvFs должны иметь атрибут только для чтения [GH 3411]</span><span class="sxs-lookup"><span data-stu-id="d707b-228">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="d707b-229">Добавить /sbin/mount.drvfs вспомогательную функцию для обработки DrvFs подключения</span><span class="sxs-lookup"><span data-stu-id="d707b-229">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="d707b-230">Используйте DrvFs переименования в POSIX.</span><span class="sxs-lookup"><span data-stu-id="d707b-230">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="d707b-231">Разрешить трансляцию путь на томах без идентификатора GUID тома.</span><span class="sxs-lookup"><span data-stu-id="d707b-231">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="d707b-232">Построение 17738 (Fast)</span><span class="sxs-lookup"><span data-stu-id="d707b-232">Build 17738 (Fast)</span></span>
<span data-ttu-id="d707b-233">Windows, общие сведения о сборке 17738 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span><span class="sxs-lookup"><span data-stu-id="d707b-233">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-234">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-234">WSL</span></span>
* <span data-ttu-id="d707b-235">Проверка разрешений SetPriority syscall слишком строгие для изменения одинаковый приоритет потока [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="d707b-235">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="d707b-236">Убедитесь, что время прерываний несмещенной используется для время загрузки, чтобы избежать возвращения отрицательные значения для clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="d707b-236">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="d707b-237">Обработка символических ссылок в интерпретаторе binfmt WSL [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="d707b-237">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="d707b-238">Более эффективная обработка очистки дескриптора файла лидером threadgroup.</span><span class="sxs-lookup"><span data-stu-id="d707b-238">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="d707b-239">Построение 17728 (Fast)</span><span class="sxs-lookup"><span data-stu-id="d707b-239">Build 17728 (Fast)</span></span>
<span data-ttu-id="d707b-240">Windows, общие сведения о сборке 17728 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span><span class="sxs-lookup"><span data-stu-id="d707b-240">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-241">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-241">WSL</span></span>
* <span data-ttu-id="d707b-242">Переключение WSL для использования вместо KeQueryPerformanceCounter KeQueryInterruptTimePrecise, чтобы избежать переполнения [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="d707b-242">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="d707b-243">Ptrace присоединение может привести к плохой возвращаемого значения из системных вызовов [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="d707b-243">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="d707b-244">Исправьте указанные ряд AF_UNIX связанных выдает [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="d707b-244">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="d707b-245">Устранить проблему, которая могла привести к WSL взаимодействия с ошибкой, если текущий рабочий каталог не меньше 5 символов [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="d707b-245">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="d707b-246">Сборки 18204 (пропустить вперед)</span><span class="sxs-lookup"><span data-stu-id="d707b-246">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="d707b-247">Windows, общие сведения о сборке 18204 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="d707b-247">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-248">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-248">WSL</span></span>
* <span data-ttu-id="d707b-249">Канал очистки событий активации edge epoll [GH 3276] inadvertenly файловой системы</span><span class="sxs-lookup"><span data-stu-id="d707b-249">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="d707b-250">Запущено через символическую ссылку NTFS исполняемого файла Win32 не учитывает имя символьную ссылку [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="d707b-250">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="d707b-251">Построение 17723 (Fast)</span><span class="sxs-lookup"><span data-stu-id="d707b-251">Build 17723 (Fast)</span></span>
<span data-ttu-id="d707b-252">Windows, общие сведения о сборке 17723 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="d707b-252">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-253">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-253">WSL</span></span>
* <span data-ttu-id="d707b-254">Избежать сбоя замыкания соединений к несуществующему порты [GH 3286] один секунда</span><span class="sxs-lookup"><span data-stu-id="d707b-254">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="d707b-255">Добавьте файл-заглушку /proc/sys/fs/file-max [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="d707b-255">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="d707b-256">Более точные сведения об области IPV6.</span><span class="sxs-lookup"><span data-stu-id="d707b-256">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="d707b-257">Поддержка PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="d707b-257">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="d707b-258">Канал очистки событий активации edge epoll [GH 3276] inadvertenly файловой системы</span><span class="sxs-lookup"><span data-stu-id="d707b-258">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="d707b-259">Запущено через символическую ссылку NTFS исполняемого файла Win32 не учитывает имя символьную ссылку [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="d707b-259">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="d707b-260">Сборки 17713</span><span class="sxs-lookup"><span data-stu-id="d707b-260">Build 17713</span></span>
<span data-ttu-id="d707b-261">Windows, общие сведения о сборке 17713 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span><span class="sxs-lookup"><span data-stu-id="d707b-261">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-262">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-262">WSL</span></span>
* <span data-ttu-id="d707b-263">Улучшенная поддержка зомби [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="d707b-263">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="d707b-264">Добавьте записи wsl.conf для управления поведением взаимодействия Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="d707b-264">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="d707b-265">Исправление ошибки, не всегда возвращает тип семейства UNIX сокета [GH 1774] getsockname</span><span class="sxs-lookup"><span data-stu-id="d707b-265">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="d707b-266">Добавлена поддержка TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="d707b-266">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="d707b-267">Сокеты, без блокировки, в процессе подключения должен возвращать EAGAIN попытки записи [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="d707b-267">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="d707b-268">Поддержка взаимодействия на виртуальными жесткими дисками [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="d707b-268">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="d707b-269">Исправьте проблему на корневую папку [GH 3304] проверки разрешений</span><span class="sxs-lookup"><span data-stu-id="d707b-269">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="d707b-270">Ограниченная поддержка запросы IOCTL клавиатуры TTY KDGKBTYPE, KDGKBMODE и KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="d707b-270">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="d707b-271">Приложения пользовательского интерфейса Windows должен выполняться, даже в том случае, когда запускается в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="d707b-271">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="d707b-272">Сборки 17704</span><span class="sxs-lookup"><span data-stu-id="d707b-272">Build 17704</span></span>
<span data-ttu-id="d707b-273">Windows, общие сведения о сборке 17704 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span><span class="sxs-lookup"><span data-stu-id="d707b-273">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-274">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-274">WSL</span></span>
* <span data-ttu-id="d707b-275">Добавление wsl -u или--пользователя параметр [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="d707b-275">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="d707b-276">Устранение проблем запуска WSL в том случае, если включена быстрая загрузка [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="d707b-276">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="d707b-277">Сокеты UNIX необходимо сохранить учетные данные отключенных однорангового узла [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="d707b-277">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="d707b-278">Сокеты Unix неблокирующие бессрочно завершились с EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="d707b-278">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="d707b-279">случай = off — тип [GH 2937, 3212, 3328] подключить новый drvfs по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d707b-279">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="d707b-280">См. в разделе [блог](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) Дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="d707b-280">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="d707b-281">Добавьте wslconfig / завершения остановки выполнения распределения.</span><span class="sxs-lookup"><span data-stu-id="d707b-281">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="d707b-282">Сборки 17692</span><span class="sxs-lookup"><span data-stu-id="d707b-282">Build 17692</span></span>
<span data-ttu-id="d707b-283">Windows, общие сведения о сборке 17692 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span><span class="sxs-lookup"><span data-stu-id="d707b-283">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-284">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-284">WSL</span></span>
* <span data-ttu-id="d707b-285">Устранена проблема с контекст оболочки WSL пунктов меню, которые не обрабатывают правильно путей с пробелами.</span><span class="sxs-lookup"><span data-stu-id="d707b-285">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="d707b-286">Предоставлять чувствительность к регистру-directory как расширенный атрибут</span><span class="sxs-lookup"><span data-stu-id="d707b-286">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="d707b-287">ARM64: Эмулировать операций обслуживания кэша.</span><span class="sxs-lookup"><span data-stu-id="d707b-287">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="d707b-288">Разрешить [проблема dotnet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="d707b-288">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="d707b-289">DrvFs: только unescape символов в диапазоне частных, которые соответствуют в escape-символ.</span><span class="sxs-lookup"><span data-stu-id="d707b-289">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="d707b-290">Сборки 17686</span><span class="sxs-lookup"><span data-stu-id="d707b-290">Build 17686</span></span>
<span data-ttu-id="d707b-291">Windows, общие сведения о сборке 17686 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span><span class="sxs-lookup"><span data-stu-id="d707b-291">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-292">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-292">WSL</span></span>
* <span data-ttu-id="d707b-293">Исправление ошибки из за другой в проверка длины интерпретатор средство синтаксического анализа ELF [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="d707b-293">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="d707b-294">WSL абсолютный таймеров с помощью времени в прошлом не срабатывают [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="d707b-294">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="d707b-295">Убедитесь, вновь точки повторного анализа созданный таким образом, перечислены в родительском каталоге.</span><span class="sxs-lookup"><span data-stu-id="d707b-295">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="d707b-296">Атомарным образом создайте каталоги с учетом регистра DrvFs.</span><span class="sxs-lookup"><span data-stu-id="d707b-296">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="d707b-297">Сборки 17677</span><span class="sxs-lookup"><span data-stu-id="d707b-297">Build 17677</span></span>
<span data-ttu-id="d707b-298">Windows, общие сведения о сборке 17677 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span><span class="sxs-lookup"><span data-stu-id="d707b-298">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-299">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-299">WSL</span></span>
* <span data-ttu-id="d707b-300">Исправлена проблема, дополнительный, где многопоточные операции может вернуть ENOENT, несмотря на то, что файл существует.</span><span class="sxs-lookup"><span data-stu-id="d707b-300">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="d707b-301">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="d707b-301">[GH 2712]</span></span>
* <span data-ttu-id="d707b-302">Фиксированный WSL запустите сбой при включении UMCI.</span><span class="sxs-lookup"><span data-stu-id="d707b-302">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="d707b-303">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="d707b-303">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="d707b-304">Сборки 17666</span><span class="sxs-lookup"><span data-stu-id="d707b-304">Build 17666</span></span>
<span data-ttu-id="d707b-305">Windows, общие сведения о сборке 17666 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span><span class="sxs-lookup"><span data-stu-id="d707b-305">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-306">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-306">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="d707b-307">ПРЕДУПРЕЖДЕНИЕ! Имеется проблема препятствует запуску на некоторые наборы микросхем AMD [GH 3134] WSL.</span><span class="sxs-lookup"><span data-stu-id="d707b-307">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="d707b-308">Исправление — Готово к работе и внесения его способ ветви сборка программы предварительной оценки.</span><span class="sxs-lookup"><span data-stu-id="d707b-308">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="d707b-309">Добавление контекстного меню обозревателя для запуска WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="d707b-309">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="d707b-310">Для использования, удерживайте клавишу shift и щелкните правой кнопкой мыши в окне проводника.</span><span class="sxs-lookup"><span data-stu-id="d707b-310">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="d707b-311">Исправить сокет unix неблокирующее поведение [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="d707b-311">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="d707b-312">Исправление, выступающие NETLINK команды в GH 2026.</span><span class="sxs-lookup"><span data-stu-id="d707b-312">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="d707b-313">Добавлена поддержка Флаги распространения подключения [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="d707b-313">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="d707b-314">Устранена проблема с усечения не вызывает события inotify [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="d707b-314">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="d707b-315">Добавлен параметр--exec параметр для wsl.exe для вызова единого двоичного файла без оболочки.</span><span class="sxs-lookup"><span data-stu-id="d707b-315">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="d707b-316">Добавлен параметр--параметр распределения для wsl.exe для выбора конкретного дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="d707b-316">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="d707b-317">Сборки 17655 (пропустить вперед)</span><span class="sxs-lookup"><span data-stu-id="d707b-317">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="d707b-318">Windows, общие сведения о сборке 17655 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="d707b-318">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-319">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-319">WSL</span></span>
* <span data-ttu-id="d707b-320">Ограниченная поддержка dmesg.</span><span class="sxs-lookup"><span data-stu-id="d707b-320">Limited support for dmesg.</span></span> <span data-ttu-id="d707b-321">Теперь приложения могут входить dmesg.</span><span class="sxs-lookup"><span data-stu-id="d707b-321">Applications can now log to dmesg.</span></span> <span data-ttu-id="d707b-322">Драйвер WSL входит команда dmesg ограниченные сведения.</span><span class="sxs-lookup"><span data-stu-id="d707b-322">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="d707b-323">В будущем это может быть расширен для выполнения другие сведения или диагностики от драйвера.</span><span class="sxs-lookup"><span data-stu-id="d707b-323">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="d707b-324">Примечание: команда dmesg в настоящее время поддерживается через `/dev/kmsg` интерфейс устройства.</span><span class="sxs-lookup"><span data-stu-id="d707b-324">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> `syslog` <span data-ttu-id="d707b-325">интерфейс sycall еще не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d707b-325">sycall interface is not yet supported.</span></span> <span data-ttu-id="d707b-326">И, таким образом, некоторые `dmesg` параметры командной строки, такие как `-S`, `-C` не работают.</span><span class="sxs-lookup"><span data-stu-id="d707b-326">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="d707b-327">Устранена проблема, где многопоточные операции может вернуть ENOENT, несмотря на то, что файл существует.</span><span class="sxs-lookup"><span data-stu-id="d707b-327">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="d707b-328">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="d707b-328">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="d707b-329">Сборки 17639 (пропустить вперед)</span><span class="sxs-lookup"><span data-stu-id="d707b-329">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="d707b-330">Windows, общие сведения о сборке 17639 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="d707b-330">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-331">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-331">WSL</span></span>
* <span data-ttu-id="d707b-332">Изменение по умолчанию gid и режима последовательной устройств в соответствии с машинный код [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="d707b-332">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="d707b-333">DrvFs теперь поддерживает дополнительные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="d707b-333">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="d707b-334">Примечание. DrvFs имеет некоторые ограничения на основе имени изменяемого дополнительные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="d707b-334">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="d707b-335">В частности, некоторые символы (например «/», ":" и "\*") не разрешено и расширенные имена атрибутов не учитывается регистр на DrvFs</span><span class="sxs-lookup"><span data-stu-id="d707b-335">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="d707b-336">Построение 17133 (Fast)</span><span class="sxs-lookup"><span data-stu-id="d707b-336">Build 17133 (Fast)</span></span>
<span data-ttu-id="d707b-337">Windows, общие сведения о сборке 17133 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="d707b-337">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-338">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-338">WSL</span></span>
* <span data-ttu-id="d707b-339">Исправление для ответа на запросы в WSL.</span><span class="sxs-lookup"><span data-stu-id="d707b-339">Fix for hang in WSL.</span></span> <span data-ttu-id="d707b-340">[GH 3039, 3034]</span><span class="sxs-lookup"><span data-stu-id="d707b-340">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="d707b-341">Построение 17128 (Fast)</span><span class="sxs-lookup"><span data-stu-id="d707b-341">Build 17128 (Fast)</span></span>
<span data-ttu-id="d707b-342">Windows, общие сведения о сборке 17128 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="d707b-342">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-343">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-343">WSL</span></span>
* <span data-ttu-id="d707b-344">Нет</span><span class="sxs-lookup"><span data-stu-id="d707b-344">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="d707b-345">Сборки 17627 (пропустить вперед)</span><span class="sxs-lookup"><span data-stu-id="d707b-345">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="d707b-346">Windows, общие сведения о сборке 17627 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="d707b-346">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-347">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-347">WSL</span></span>
* <span data-ttu-id="d707b-348">Добавлена поддержка futex pi с поддержкой операций.</span><span class="sxs-lookup"><span data-stu-id="d707b-348">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="d707b-349">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="d707b-349">[GH 1006]</span></span>
    * <span data-ttu-id="d707b-350">Обратите внимание на то, что приоритеты настоящее время не поддерживаемой функцией WSL существуют ограничения, но стандартного использования должны быть разблокированы.</span><span class="sxs-lookup"><span data-stu-id="d707b-350">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="d707b-351">Поддержка брандмауэра Windows для WSL процессов.</span><span class="sxs-lookup"><span data-stu-id="d707b-351">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="d707b-352">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="d707b-352">[GH 1852]</span></span>
    * <span data-ttu-id="d707b-353">Например чтобы разрешить WSL python обработки прослушивание любого порта, используйте cmd Windows с повышенными правами:</span><span class="sxs-lookup"><span data-stu-id="d707b-353">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd:</span></span>
```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```
    * <span data-ttu-id="d707b-354">Дополнительные сведения о добавлении правил брандмауэра см. в разделе [ссылку](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span><span class="sxs-lookup"><span data-stu-id="d707b-354">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="d707b-355">Использовать оболочку пользователя по умолчанию, при использовании wsl.exe.</span><span class="sxs-lookup"><span data-stu-id="d707b-355">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="d707b-356">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="d707b-356">[GH 2372]</span></span>
* <span data-ttu-id="d707b-357">О всех сетевых интерфейсов, как ethernet.</span><span class="sxs-lookup"><span data-stu-id="d707b-357">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="d707b-358">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="d707b-358">[GH 2996]</span></span>
* <span data-ttu-id="d707b-359">Более эффективная обработка файла/etc/passwd поврежден.</span><span class="sxs-lookup"><span data-stu-id="d707b-359">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="d707b-360">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="d707b-360">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="d707b-361">Консоль</span><span class="sxs-lookup"><span data-stu-id="d707b-361">Console</span></span>
* <span data-ttu-id="d707b-362">Нет исправления.</span><span class="sxs-lookup"><span data-stu-id="d707b-362">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-363">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-363">LTP Results:</span></span>
<span data-ttu-id="d707b-364">Проверка выполняется.</span><span class="sxs-lookup"><span data-stu-id="d707b-364">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="d707b-365">Сборки 17618 (пропустить вперед)</span><span class="sxs-lookup"><span data-stu-id="d707b-365">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="d707b-366">Windows, общие сведения о сборке 17618 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="d707b-366">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-367">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-367">WSL</span></span>
* <span data-ttu-id="d707b-368">Добавления функциональных возможностей pseudoconsole для NT взаимодействия [988 GH, 1366, 1433, 1542, 2370, 2406].</span><span class="sxs-lookup"><span data-stu-id="d707b-368">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="d707b-369">Механизм установки предыдущих версий (lxrun.exe) является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="d707b-369">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="d707b-370">Поддерживаемые механизм для установки дистрибутивов осуществляется через Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="d707b-370">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="d707b-371">Консоль</span><span class="sxs-lookup"><span data-stu-id="d707b-371">Console</span></span>
* <span data-ttu-id="d707b-372">Нет исправления.</span><span class="sxs-lookup"><span data-stu-id="d707b-372">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-373">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-373">LTP Results:</span></span>
<span data-ttu-id="d707b-374">Проверка выполняется.</span><span class="sxs-lookup"><span data-stu-id="d707b-374">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="d707b-375">Сборки 17110</span><span class="sxs-lookup"><span data-stu-id="d707b-375">Build 17110</span></span>
<span data-ttu-id="d707b-376">Windows, общие сведения о сборке 17110 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span><span class="sxs-lookup"><span data-stu-id="d707b-376">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-377">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-377">WSL</span></span>
* <span data-ttu-id="d707b-378">Разрешить /init прекращение из Windows [GH 2928].</span><span class="sxs-lookup"><span data-stu-id="d707b-378">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="d707b-379">DrvFs теперь использует учет регистра в каталог по умолчанию (эквивалентно «случай = dir» режим подключения).</span><span class="sxs-lookup"><span data-stu-id="d707b-379">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="d707b-380">С помощью «случай = force» (старое поведение) необходимо задать раздел реестра.</span><span class="sxs-lookup"><span data-stu-id="d707b-380">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="d707b-381">Выполните следующую команду, чтобы включить «случай = force» Если вам нужно использовать его: reg добавить HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span><span class="sxs-lookup"><span data-stu-id="d707b-381">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="d707b-382">Если у вас есть существующие каталоги, созданные с помощью WSL в более старой версии Windows, которые нужно учитывать регистр, использовать fsutil.exe, чтобы пометить их регистр: setcasesensitiveinfo файл fsutil.exe <path> включить</span><span class="sxs-lookup"><span data-stu-id="d707b-382">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="d707b-383">Строки, возвращаемые из uname syscall с НУЛЕВЫМ завершением.</span><span class="sxs-lookup"><span data-stu-id="d707b-383">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="d707b-384">Консоль</span><span class="sxs-lookup"><span data-stu-id="d707b-384">Console</span></span>
* <span data-ttu-id="d707b-385">Нет исправления.</span><span class="sxs-lookup"><span data-stu-id="d707b-385">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-386">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-386">LTP Results:</span></span>
<span data-ttu-id="d707b-387">Проверка выполняется.</span><span class="sxs-lookup"><span data-stu-id="d707b-387">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="d707b-388">Сборки 17107</span><span class="sxs-lookup"><span data-stu-id="d707b-388">Build 17107</span></span>
<span data-ttu-id="d707b-389">Windows, общие сведения о сборке 17107 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span><span class="sxs-lookup"><span data-stu-id="d707b-389">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-390">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-390">WSL</span></span>
* <span data-ttu-id="d707b-391">Поддерживает TCSETSF и TCSETSW на конечных точках master pty [GH 2552].</span><span class="sxs-lookup"><span data-stu-id="d707b-391">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="d707b-392">Запуск одновременных взаимодействия процессов может привести к появлению EINVAL [GH 2813].</span><span class="sxs-lookup"><span data-stu-id="d707b-392">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="d707b-393">Исправьте PTRACE_ATTACH для отображения состояния правильной трассировки в /proc/pid/status.</span><span class="sxs-lookup"><span data-stu-id="d707b-393">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="d707b-394">Исправление конкуренции, которому кратковременные клонирован с флагами CLEARTID и SETTID может выйти из без очистки адрес TID.</span><span class="sxs-lookup"><span data-stu-id="d707b-394">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="d707b-395">Отображать сообщение при обновлении системные каталоги файлов Linux, при перемещении из сборки предварительно 17093.</span><span class="sxs-lookup"><span data-stu-id="d707b-395">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="d707b-396">Дополнительные сведения о изменений 17093 файловой системы, см. в разделе заметки о выпуске [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span><span class="sxs-lookup"><span data-stu-id="d707b-396">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="d707b-397">Консоль</span><span class="sxs-lookup"><span data-stu-id="d707b-397">Console</span></span>
* <span data-ttu-id="d707b-398">Нет исправления.</span><span class="sxs-lookup"><span data-stu-id="d707b-398">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-399">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-399">LTP Results:</span></span>
<span data-ttu-id="d707b-400">Проверка выполняется.</span><span class="sxs-lookup"><span data-stu-id="d707b-400">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="d707b-401">Сборки 17101</span><span class="sxs-lookup"><span data-stu-id="d707b-401">Build 17101</span></span>
<span data-ttu-id="d707b-402">Windows, общие сведения о сборке 17101 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="d707b-402">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-403">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-403">WSL</span></span>
* <span data-ttu-id="d707b-404">Поддержка signalfd.</span><span class="sxs-lookup"><span data-stu-id="d707b-404">Support for signalfd.</span></span> <span data-ttu-id="d707b-405">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="d707b-405">[GH 129]</span></span>
* <span data-ttu-id="d707b-406">Поддерживает имена файлов, содержащие недопустимые символы NTFS, кодировать их в виде частных символов Юникода.</span><span class="sxs-lookup"><span data-stu-id="d707b-406">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="d707b-407">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="d707b-407">[GH 1514]</span></span>
* <span data-ttu-id="d707b-408">Автоподключение будут переведены только для чтения, если запись не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d707b-408">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="d707b-409">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="d707b-409">[GH 2603]</span></span>
* <span data-ttu-id="d707b-410">Разрешить вставки суррогатных пар Юникода (например, эмодзи символов).</span><span class="sxs-lookup"><span data-stu-id="d707b-410">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="d707b-411">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="d707b-411">[GH 2765]</span></span>
* <span data-ttu-id="d707b-412">Псевдо файлы в/proc и/PF должен возвращать чтения и записи ready select, опроса, epoll, т. д. [GH 2838]</span><span class="sxs-lookup"><span data-stu-id="d707b-412">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="d707b-413">Устранена проблема, может стать причиной службы перейти в бесконечный цикл при реестра было изменено или повреждено.</span><span class="sxs-lookup"><span data-stu-id="d707b-413">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="d707b-414">Исправьте netlink сообщений для работы с более новой версии iproute2 (upstream 4.14).</span><span class="sxs-lookup"><span data-stu-id="d707b-414">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="d707b-415">Консоль</span><span class="sxs-lookup"><span data-stu-id="d707b-415">Console</span></span>
* <span data-ttu-id="d707b-416">Нет исправления.</span><span class="sxs-lookup"><span data-stu-id="d707b-416">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-417">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-417">LTP Results:</span></span>
<span data-ttu-id="d707b-418">Проверка выполняется.</span><span class="sxs-lookup"><span data-stu-id="d707b-418">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="d707b-419">Сборки 17093</span><span class="sxs-lookup"><span data-stu-id="d707b-419">Build 17093</span></span>
<span data-ttu-id="d707b-420">Windows, общие сведения о сборке 17093 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span><span class="sxs-lookup"><span data-stu-id="d707b-420">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="d707b-421">Внимание!</span><span class="sxs-lookup"><span data-stu-id="d707b-421">Important:</span></span>
<span data-ttu-id="d707b-422">Когда вы запускаете WSL в первый раз после обновления до этой сборки, ему необходимо выполнить определенные действия, обновление системные каталоги файлов Linux.</span><span class="sxs-lookup"><span data-stu-id="d707b-422">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="d707b-423">Это может занять несколько минут, поэтому может показаться WSL работает медленно.</span><span class="sxs-lookup"><span data-stu-id="d707b-423">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="d707b-424">Это должно произойти, только один раз для каждого распределения установленная в магазине.</span><span class="sxs-lookup"><span data-stu-id="d707b-424">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="d707b-425">Улучшенная поддержка учет регистра в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="d707b-425">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="d707b-426">DrvFs теперь поддерживает учет регистра в каталоге.</span><span class="sxs-lookup"><span data-stu-id="d707b-426">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="d707b-427">Это новый флаг, можно задать каталоги, чтобы указать, что все операции в этих папках должны рассматриваться как регистр, который позволяет даже приложениям Windows, чтобы правильно открыть файлы, которые отличаются только регистром.</span><span class="sxs-lookup"><span data-stu-id="d707b-427">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="d707b-428">DrvFs имеет новые параметры подключения, управляющие учет регистра на основе-directory</span><span class="sxs-lookup"><span data-stu-id="d707b-428">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="d707b-429">случай = force: все каталоги обрабатываются с учетом регистра (за исключением корневого диска).</span><span class="sxs-lookup"><span data-stu-id="d707b-429">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="d707b-430">Новые каталоги, созданные с помощью WSL, помечаются как с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="d707b-430">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="d707b-431">Это устаревшее поведение, за исключением пометки новые каталоги с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="d707b-431">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="d707b-432">случай = dir: только каталоги с флагом-directory учет регистра обрабатываются с учетом регистра; другие каталоги зависят от регистра символов.</span><span class="sxs-lookup"><span data-stu-id="d707b-432">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="d707b-433">Новые каталоги, созданные с помощью WSL, помечаются как с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="d707b-433">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="d707b-434">случай = off: только каталоги с флагом-directory учет регистра обрабатываются с учетом регистра; другие каталоги зависят от регистра символов.</span><span class="sxs-lookup"><span data-stu-id="d707b-434">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="d707b-435">Новые каталоги, созданные с помощью WSL, помечаются как без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="d707b-435">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="d707b-436">Примечание: каталоги, созданные WSL в предыдущих выпусках не имеют этот флаг установлен, поэтому не следует обрабатывать как регистр при использовании «случай = dir» параметр.</span><span class="sxs-lookup"><span data-stu-id="d707b-436">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="d707b-437">Можно задать этот флаг в существующих каталогах ожидается в ближайшее время.</span><span class="sxs-lookup"><span data-stu-id="d707b-437">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="d707b-438">Пример присоединения с помощью этих параметров (для существующих дисков, необходимо сначала отключить перед подключением с различными параметрами): sudo mount -t drvfs C:/mnt/c -o случай = dir</span><span class="sxs-lookup"><span data-stu-id="d707b-438">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="d707b-439">Сейчас, измените прописные = force по-прежнему является параметром по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d707b-439">For now, case=force is still the default option.</span></span> <span data-ttu-id="d707b-440">Это будет изменено на случай = dir в будущем.</span><span class="sxs-lookup"><span data-stu-id="d707b-440">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="d707b-441">Теперь можно использовать символы косой черты в путях Windows, при подключении DrvFs, например: sudo подключить /mnt/share //server/share drvfs -t</span><span class="sxs-lookup"><span data-stu-id="d707b-441">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="d707b-442">WSL сейчас обрабатывает файл/etc/fstab во время запуска экземпляра [GH 2636].</span><span class="sxs-lookup"><span data-stu-id="d707b-442">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="d707b-443">Для этого перед автоматическое подключение DrvFs дисков; все диски, которые уже были подключены с fstab будет не быть автоматическое повторное подключение, вы можете изменить точку монтирования для дисков.</span><span class="sxs-lookup"><span data-stu-id="d707b-443">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="d707b-444">Это поведение можно отключить с помощью wsl.conf.</span><span class="sxs-lookup"><span data-stu-id="d707b-444">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="d707b-445">Файлы подключения, mountinfo и mountstats в/proc правильным образом экранировать специальные символы, такие как обратные косые черты и пробелы [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="d707b-445">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="d707b-446">Теперь специальные файлы, созданные DrvFs как WSL символические ссылки, или fifos и сокеты при включения метаданных можно копировать и перемещать из Windows.</span><span class="sxs-lookup"><span data-stu-id="d707b-446">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="d707b-447">WSL более настраивается с помощью wsl.conf</span><span class="sxs-lookup"><span data-stu-id="d707b-447">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="d707b-448">Мы добавили метод позволяют автоматически настраивать определенные функции в WSL, которая будет применяться каждый раз при запуске подсистемы.</span><span class="sxs-lookup"><span data-stu-id="d707b-448">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="d707b-449">Сюда входят автоподключения параметры и конфигурации сети.</span><span class="sxs-lookup"><span data-stu-id="d707b-449">This includes automount options and network configuration.</span></span> <span data-ttu-id="d707b-450">Дополнительные сведения о нем в записи блога в: https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="d707b-450">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="d707b-451">AF_UNIX позволяет подключениями между процессами Linux на WSL и собственные процессы Windows</span><span class="sxs-lookup"><span data-stu-id="d707b-451">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="d707b-452">Приложения, WSL и Windows теперь может взаимодействовать друг с другом через сокеты Unix.</span><span class="sxs-lookup"><span data-stu-id="d707b-452">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="d707b-453">Представьте, что вы хотите запустить службу в Windows и сделает его доступным для приложений Windows и WSL.</span><span class="sxs-lookup"><span data-stu-id="d707b-453">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="d707b-454">Теперь это возможно с помощью сокетов Unix.</span><span class="sxs-lookup"><span data-stu-id="d707b-454">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="d707b-455">Чтение блога см. в нашем блоге https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="d707b-455">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-456">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-456">WSL</span></span>
* <span data-ttu-id="d707b-457">Поддержка mmap() с MAP_NORESERVE [GH 121, 2784]</span><span class="sxs-lookup"><span data-stu-id="d707b-457">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="d707b-458">Поддерживает CLONE_PTRACE и CLONE_UNTRACED [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="d707b-458">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="d707b-459">Сигнал завершения не SIGCHLD дескриптор в клоне [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="d707b-459">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="d707b-460">Заглушки /proc/sys/fs/inotify/max_user_instances и /proc/sys/fs/inotify/max_user_watches [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="d707b-460">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="d707b-461">Произошла ошибка при загрузке ELF двоичные файлы, содержащие заголовки нагрузки со смещениями ненулевое значение [GH 1884]</span><span class="sxs-lookup"><span data-stu-id="d707b-461">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="d707b-462">Обнуляется конечные байты, страницы, при загрузке изображений.</span><span class="sxs-lookup"><span data-stu-id="d707b-462">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="d707b-463">Снизить число случаев, где execve автоматически завершает процесс</span><span class="sxs-lookup"><span data-stu-id="d707b-463">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="d707b-464">Консоль</span><span class="sxs-lookup"><span data-stu-id="d707b-464">Console</span></span>
* <span data-ttu-id="d707b-465">Нет исправления.</span><span class="sxs-lookup"><span data-stu-id="d707b-465">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-466">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-466">LTP Results:</span></span>
<span data-ttu-id="d707b-467">Проверка выполняется.</span><span class="sxs-lookup"><span data-stu-id="d707b-467">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="d707b-468">Сборки 17083</span><span class="sxs-lookup"><span data-stu-id="d707b-468">Build 17083</span></span>
<span data-ttu-id="d707b-469">Windows, общие сведения о сборке 17083 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="d707b-469">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-470">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-470">WSL</span></span>
* <span data-ttu-id="d707b-471">Фиксированный критической ошибки, связанные с epoll [GH 2798, 2801, 2857]</span><span class="sxs-lookup"><span data-stu-id="d707b-471">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="d707b-472">Фиксированный зависает при отключении ASLR [GH 1185, 2870]</span><span class="sxs-lookup"><span data-stu-id="d707b-472">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="d707b-473">Убедитесь, что операции mmap отображаются atomic [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="d707b-473">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="d707b-474">Консоль</span><span class="sxs-lookup"><span data-stu-id="d707b-474">Console</span></span>
* <span data-ttu-id="d707b-475">Нет исправления.</span><span class="sxs-lookup"><span data-stu-id="d707b-475">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-476">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-476">LTP Results:</span></span>
<span data-ttu-id="d707b-477">Проверка выполняется.</span><span class="sxs-lookup"><span data-stu-id="d707b-477">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="d707b-478">Сборки 17074</span><span class="sxs-lookup"><span data-stu-id="d707b-478">Build 17074</span></span>
<span data-ttu-id="d707b-479">Windows, общие сведения о сборке 17074 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span><span class="sxs-lookup"><span data-stu-id="d707b-479">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-480">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-480">WSL</span></span>
* <span data-ttu-id="d707b-481">Формат хранения фиксированного DrvFs метаданных [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="d707b-481">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="d707b-482">**Важно!** DrvFs метаданные, созданные до этой сборки будут отображаться неправильно или вообще не.</span><span class="sxs-lookup"><span data-stu-id="d707b-482">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="d707b-483">Чтобы устранить затронутых файлов, используйте chmod и сменить повторно применить метаданные.</span><span class="sxs-lookup"><span data-stu-id="d707b-483">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="d707b-484">Устранена проблема с несколькими сигналы и перезапускаемые syscalls.</span><span class="sxs-lookup"><span data-stu-id="d707b-484">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="d707b-485">Консоль</span><span class="sxs-lookup"><span data-stu-id="d707b-485">Console</span></span>
* <span data-ttu-id="d707b-486">Нет исправления.</span><span class="sxs-lookup"><span data-stu-id="d707b-486">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-487">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-487">LTP Results:</span></span>
<span data-ttu-id="d707b-488">Проверка выполняется.</span><span class="sxs-lookup"><span data-stu-id="d707b-488">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="d707b-489">Сборки 17063</span><span class="sxs-lookup"><span data-stu-id="d707b-489">Build 17063</span></span>
<span data-ttu-id="d707b-490">Windows, общие сведения о сборке 17063 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span><span class="sxs-lookup"><span data-stu-id="d707b-490">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d707b-491">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-491">WSL</span></span>
* <span data-ttu-id="d707b-492">DrvFs поддерживает дополнительные метаданные для Linux.</span><span class="sxs-lookup"><span data-stu-id="d707b-492">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="d707b-493">Это позволяет задать владельца и режима файлов с помощью chmod/сменить, а также создание специальных файлов, таких как fifos, сокеты unix и файлы устройства.</span><span class="sxs-lookup"><span data-stu-id="d707b-493">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="d707b-494">Эта функция отключена по умолчанию сейчас так как это по-прежнему экспериментальных.</span><span class="sxs-lookup"><span data-stu-id="d707b-494">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="d707b-495">**Примечание.**  Мы исправили ошибку, в формат метаданных, используемый DrvFs.</span><span class="sxs-lookup"><span data-stu-id="d707b-495">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="d707b-496">Метаданные работает на эту сборку для службы "Экспериментирование", последующих сборках не будет правильно считывать метаданные, созданные в этой сборке.</span><span class="sxs-lookup"><span data-stu-id="d707b-496">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="d707b-497">Может потребоваться вручную обновить владельца для измененных файлов и устройств с Идентификатором пользовательского устройства придется создать заново.</span><span class="sxs-lookup"><span data-stu-id="d707b-497">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="d707b-498">Чтобы включить подключения DrvFs с параметром метаданных (Чтобы включить его на точку существующие подключения, необходимо сначала отключить его):</span><span class="sxs-lookup"><span data-stu-id="d707b-498">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="d707b-499">Linux разрешения добавляются как дополнительные метаданные в файл; они не влияют на разрешения Windows.</span><span class="sxs-lookup"><span data-stu-id="d707b-499">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="d707b-500">Помните, что изменения в файл с помощью редактора Windows может удалить метаданные.</span><span class="sxs-lookup"><span data-stu-id="d707b-500">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="d707b-501">В этом случае файл вернется к его разрешения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d707b-501">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="d707b-502">Добавлена подключения параметры DrvFs для управляющих файлов без метаданных.</span><span class="sxs-lookup"><span data-stu-id="d707b-502">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="d707b-503">UID: идентификатор пользователя, используемый для владельца всех файлов.</span><span class="sxs-lookup"><span data-stu-id="d707b-503">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="d707b-504">GID: идентификатор группы, используемый для владельца всех файлов.</span><span class="sxs-lookup"><span data-stu-id="d707b-504">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="d707b-505">umask: маски восьмеричные разрешений, чтобы исключить для всех файлов и каталогов.</span><span class="sxs-lookup"><span data-stu-id="d707b-505">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="d707b-506">fmask: маски восьмеричные разрешений, чтобы исключить все обычные файлы.</span><span class="sxs-lookup"><span data-stu-id="d707b-506">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="d707b-507">dmask: маски восьмеричные разрешений, чтобы исключить для всех каталогов.</span><span class="sxs-lookup"><span data-stu-id="d707b-507">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="d707b-508">Пример:</span><span class="sxs-lookup"><span data-stu-id="d707b-508">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="d707b-509">Совместного использования с параметром метаданных задание разрешений по умолчанию для файлов без метаданных.</span><span class="sxs-lookup"><span data-stu-id="d707b-509">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="d707b-510">Появилась новая переменная среды `WSLENV`, чтобы настроить как переменные среды передавать между WSL и Win32.</span><span class="sxs-lookup"><span data-stu-id="d707b-510">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="d707b-511">Пример:</span><span class="sxs-lookup"><span data-stu-id="d707b-511">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  `WSLENV` <span data-ttu-id="d707b-512">приведен список переменных среды, которые могут быть включены при запуске WSL из Win32 или процессах Win32 из WSL после двоеточия.</span><span class="sxs-lookup"><span data-stu-id="d707b-512">is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="d707b-513">Каждая переменная может заканчиваться косой чертой, означает следуют флаг для определения того, как он преобразуется.</span><span class="sxs-lookup"><span data-stu-id="d707b-513">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="d707b-514">p: Значение — это путь, который следует преобразовать между WSL пути и пути Win32.</span><span class="sxs-lookup"><span data-stu-id="d707b-514">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="d707b-515">L: Значение — это список путей.</span><span class="sxs-lookup"><span data-stu-id="d707b-515">l: The value is a list of paths.</span></span> <span data-ttu-id="d707b-516">В WSL это список разделенных запятой.</span><span class="sxs-lookup"><span data-stu-id="d707b-516">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="d707b-517">В Win32 это список разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="d707b-517">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="d707b-518">u: Значения должны быть включены только при вызове WSL из Win32</span><span class="sxs-lookup"><span data-stu-id="d707b-518">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="d707b-519">запись: Значения должны быть включены только при вызове Win32 из WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-519">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="d707b-520">Можно задать `WSLENV` в .bashrc или в настраиваемой среды Windows для пользователя.</span><span class="sxs-lookup"><span data-stu-id="d707b-520">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="d707b-521">подключение drvfs правильно сохраняет отметки времени из tar-файл, cp -p (GH 1939)</span><span class="sxs-lookup"><span data-stu-id="d707b-521">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="d707b-522">сообщить о символических ссылок drvfs верного размера (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="d707b-522">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="d707b-523">чтение и запись работает для очень большие объемы ввода-ВЫВОДА (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="d707b-523">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="d707b-524">waitpid работает с группой процессов идентификаторы (GH 2534)</span><span class="sxs-lookup"><span data-stu-id="d707b-524">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="d707b-525">значительно улучшенная mmap производительности для больших резерва регионов; повышает производительность ghc (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="d707b-525">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="d707b-526">поддерживает индивидуальные для READ_IMPLIES_EXEC; исправления maxima и clisp (GH 1185)</span><span class="sxs-lookup"><span data-stu-id="d707b-526">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="d707b-527">mprotect поддерживает PROT_GROWSDOWN; исправления clisp (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="d707b-527">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="d707b-528">исправления ошибок страницы в перегруженности режиме; исправления sbcl (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="d707b-528">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="d707b-529">клон поддерживает дополнительные сочетания флагов</span><span class="sxs-lookup"><span data-stu-id="d707b-529">clone supports more flags combinations</span></span>
* <span data-ttu-id="d707b-530">Поддерживает select/epoll epoll файлов (ранее no-op).</span><span class="sxs-lookup"><span data-stu-id="d707b-530">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="d707b-531">Уведомите ptrace из Нереализованная syscalls.</span><span class="sxs-lookup"><span data-stu-id="d707b-531">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="d707b-532">Игнорировать интерфейсы, которые не являются вверх при создании серверах имен resolv.conf [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="d707b-532">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="d707b-533">Перечислить интерфейсы сети без физического адреса.</span><span class="sxs-lookup"><span data-stu-id="d707b-533">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="d707b-534">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="d707b-534">[GH 2685]</span></span>
* <span data-ttu-id="d707b-535">Дополнительные исправления ошибок и улучшения.</span><span class="sxs-lookup"><span data-stu-id="d707b-535">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="d707b-536">Средства Linux, доступные для разработчиков Windows</span><span class="sxs-lookup"><span data-stu-id="d707b-536">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="d707b-537">Windows Командная строка цепочки инструментов содержит bsdtar (tar-файл) и curl.</span><span class="sxs-lookup"><span data-stu-id="d707b-537">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="d707b-538">Чтение [этот блог](https://aka.ms/tarcurlwindows) Дополнительные сведения о добавлении этих двух новых средств и см. в разделе, как формирование опыт разработки на Windows.</span><span class="sxs-lookup"><span data-stu-id="d707b-538">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   `AF_UNIX` <span data-ttu-id="d707b-539">доступна в пакете SDK для предварительной оценки Windows (17061 +).</span><span class="sxs-lookup"><span data-stu-id="d707b-539">is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="d707b-540">Чтение [этот блог](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) Дополнительные сведения о `AF_UNIX` и как разработчики на Windows могут использовать его.</span><span class="sxs-lookup"><span data-stu-id="d707b-540">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="d707b-541">Консоль</span><span class="sxs-lookup"><span data-stu-id="d707b-541">Console</span></span>
* <span data-ttu-id="d707b-542">Нет исправления.</span><span class="sxs-lookup"><span data-stu-id="d707b-542">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-543">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-543">LTP Results:</span></span>
<span data-ttu-id="d707b-544">Проверка выполняется.</span><span class="sxs-lookup"><span data-stu-id="d707b-544">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="d707b-545">Сборки 17046</span><span class="sxs-lookup"><span data-stu-id="d707b-545">Build 17046</span></span>

<span data-ttu-id="d707b-546">Windows, общие сведения о сборке 17046 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span><span class="sxs-lookup"><span data-stu-id="d707b-546">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="d707b-547">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-547">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="d707b-548">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-548">WSL</span></span>
- <span data-ttu-id="d707b-549">Разрешить выполнение без active терминалов процессов.</span><span class="sxs-lookup"><span data-stu-id="d707b-549">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="d707b-550">[GH-709, 1007, 1511, 2252, 2391, т. п.]</span><span class="sxs-lookup"><span data-stu-id="d707b-550">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="d707b-551">Улучшенная поддержка CLONE_VFORK и CLONE_VM.</span><span class="sxs-lookup"><span data-stu-id="d707b-551">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="d707b-552">[GH 1878, 2615]</span><span class="sxs-lookup"><span data-stu-id="d707b-552">[GH 1878, 2615]</span></span>
- <span data-ttu-id="d707b-553">Пропустите драйвер-фильтры TDI WSL, сетевыми операциями.</span><span class="sxs-lookup"><span data-stu-id="d707b-553">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="d707b-554">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="d707b-554">[GH 1554]</span></span>
- <span data-ttu-id="d707b-555">DrvFs создает NT символических ссылок при соблюдении определенных условий.</span><span class="sxs-lookup"><span data-stu-id="d707b-555">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="d707b-556">[GH 353, 1475, 2602]</span><span class="sxs-lookup"><span data-stu-id="d707b-556">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="d707b-557">Цель ссылки должен быть относительным, не должен быть больше любого точек подключения или символических ссылок и должна существовать.</span><span class="sxs-lookup"><span data-stu-id="d707b-557">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="d707b-558">Пользователь должен иметь SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (это обычно требует запуска с повышенными правами wsl.exe), если не включен режим разработчика.</span><span class="sxs-lookup"><span data-stu-id="d707b-558">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="d707b-559">В других случаях DrvFs по-прежнему создает WSL символических ссылок.</span><span class="sxs-lookup"><span data-stu-id="d707b-559">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="d707b-560">Разрешить, одновременно работающих экземпляров WSL с повышенными правами и без повышенных привилегий.</span><span class="sxs-lookup"><span data-stu-id="d707b-560">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="d707b-561">Поддержка /proc/sys/kernel/yama/ptrace_scope</span><span class="sxs-lookup"><span data-stu-id="d707b-561">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="d707b-562">Добавьте wslpath сделать WSL <> – Windows путь преобразования.</span><span class="sxs-lookup"><span data-stu-id="d707b-562">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="d707b-563">[GH 522 1243, 1834, 2327, т. п.]</span><span class="sxs-lookup"><span data-stu-id="d707b-563">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="d707b-564">Консоль</span><span class="sxs-lookup"><span data-stu-id="d707b-564">Console</span></span>
- <span data-ttu-id="d707b-565">Нет исправления.</span><span class="sxs-lookup"><span data-stu-id="d707b-565">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-566">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-566">LTP Results:</span></span>
<span data-ttu-id="d707b-567">Проверка выполняется.</span><span class="sxs-lookup"><span data-stu-id="d707b-567">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="d707b-568">Сборки 17040</span><span class="sxs-lookup"><span data-stu-id="d707b-568">Build 17040</span></span>

<span data-ttu-id="d707b-569">Windows, общие сведения о сборке 17040 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span><span class="sxs-lookup"><span data-stu-id="d707b-569">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-570">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-570">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="d707b-571">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-571">WSL</span></span>
- <span data-ttu-id="d707b-572">Нет исправления с момента 17035.</span><span class="sxs-lookup"><span data-stu-id="d707b-572">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="d707b-573">Консоль</span><span class="sxs-lookup"><span data-stu-id="d707b-573">Console</span></span>
- <span data-ttu-id="d707b-574">Нет исправления с момента 17035.</span><span class="sxs-lookup"><span data-stu-id="d707b-574">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-575">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-575">LTP Results:</span></span>
<span data-ttu-id="d707b-576">Проверка выполняется.</span><span class="sxs-lookup"><span data-stu-id="d707b-576">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="d707b-577">Сборки 17035</span><span class="sxs-lookup"><span data-stu-id="d707b-577">Build 17035</span></span>

<span data-ttu-id="d707b-578">Windows, общие сведения о сборке 17035 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span><span class="sxs-lookup"><span data-stu-id="d707b-578">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-579">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-579">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="d707b-580">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-580">WSL</span></span>
- <span data-ttu-id="d707b-581">Доступ к файлам на DrvFs может периодически давать сбой с EINVAL.</span><span class="sxs-lookup"><span data-stu-id="d707b-581">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="d707b-582">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="d707b-582">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="d707b-583">Консоль</span><span class="sxs-lookup"><span data-stu-id="d707b-583">Console</span></span>
- <span data-ttu-id="d707b-584">Потеря цвет при вставке или удалении строк в режиме VT.</span><span class="sxs-lookup"><span data-stu-id="d707b-584">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-585">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-585">LTP Results:</span></span>
<span data-ttu-id="d707b-586">Проверка выполняется.</span><span class="sxs-lookup"><span data-stu-id="d707b-586">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="d707b-587">Сборки 17025</span><span class="sxs-lookup"><span data-stu-id="d707b-587">Build 17025</span></span>

<span data-ttu-id="d707b-588">Для Windows, общие сведения о сборки 17025 посетите [блог Windows](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span><span class="sxs-lookup"><span data-stu-id="d707b-588">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-589">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-589">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="d707b-590">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-590">WSL</span></span>
- <span data-ttu-id="d707b-591">Запуск начальной процессов в новой основной группы [GH 1653, 2510].</span><span class="sxs-lookup"><span data-stu-id="d707b-591">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="d707b-592">Доставка SIGHUP исправления [GH 2496].</span><span class="sxs-lookup"><span data-stu-id="d707b-592">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="d707b-593">Создать виртуальный мост имя по умолчанию, если не указан [GH 2497].</span><span class="sxs-lookup"><span data-stu-id="d707b-593">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="d707b-594">Реализуйте /proc/sys/kernel/random/boot_id [GH 2518].</span><span class="sxs-lookup"><span data-stu-id="d707b-594">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="d707b-595">Исправления более взаимодействия канал stdout и stderr.</span><span class="sxs-lookup"><span data-stu-id="d707b-595">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="d707b-596">Заглушки syncfs системного вызова.</span><span class="sxs-lookup"><span data-stu-id="d707b-596">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="d707b-597">Консоль</span><span class="sxs-lookup"><span data-stu-id="d707b-597">Console</span></span>
- <span data-ttu-id="d707b-598">Исправьте входные VT перевода для сторонних консолей [GH 111]</span><span class="sxs-lookup"><span data-stu-id="d707b-598">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-599">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-599">LTP Results:</span></span>
<span data-ttu-id="d707b-600">Проверка выполняется.</span><span class="sxs-lookup"><span data-stu-id="d707b-600">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="d707b-601">Сборки 17017</span><span class="sxs-lookup"><span data-stu-id="d707b-601">Build 17017</span></span>

<span data-ttu-id="d707b-602">Windows, общие сведения о сборке 17017 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span><span class="sxs-lookup"><span data-stu-id="d707b-602">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-603">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-603">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="d707b-604">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-604">WSL</span></span>
- <span data-ttu-id="d707b-605">Игнорируйте пустые заголовки программы ELF [GH 330].</span><span class="sxs-lookup"><span data-stu-id="d707b-605">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="d707b-606">Разрешить LxssManager для создания экземпляров WSL для неинтерактивной пользователей (ssh и запланированных задач поддержки) [GH 777, 1602].</span><span class="sxs-lookup"><span data-stu-id="d707b-606">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="d707b-607">Поддержка WSL "->" Win32 "->" сценарии WSL («начало») [GH 1228].</span><span class="sxs-lookup"><span data-stu-id="d707b-607">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="d707b-608">Ограниченная поддержка завершения вызывается через взаимодействие [GH 1614] консольных приложений.</span><span class="sxs-lookup"><span data-stu-id="d707b-608">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="d707b-609">Варианты поддержки подключения для devpts [GH 1948].</span><span class="sxs-lookup"><span data-stu-id="d707b-609">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="d707b-610">Ptrace блокировка запуска дочерних [GH 2333].</span><span class="sxs-lookup"><span data-stu-id="d707b-610">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="d707b-611">EPOLLET отсутствуют некоторые события [GH 2462].</span><span class="sxs-lookup"><span data-stu-id="d707b-611">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="d707b-612">Возвращаются дополнительные данные для PTRACE_GETSIGINFO.</span><span class="sxs-lookup"><span data-stu-id="d707b-612">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="d707b-613">Getdents с lseek дает неверные результаты.</span><span class="sxs-lookup"><span data-stu-id="d707b-613">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="d707b-614">Устраните некоторые зависаний взаимодействия приложений Win32, ожидание входных данных для канала, который не содержит дополнительные данные.</span><span class="sxs-lookup"><span data-stu-id="d707b-614">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="d707b-615">Поддержка O_ASYNC tty/pty файлов.</span><span class="sxs-lookup"><span data-stu-id="d707b-615">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="d707b-616">Дополнительные улучшения и исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="d707b-616">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="d707b-617">Консоль</span><span class="sxs-lookup"><span data-stu-id="d707b-617">Console</span></span>
- <span data-ttu-id="d707b-618">Консоль, связанные с ними изменения в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="d707b-618">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-619">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-619">LTP Results:</span></span>
<span data-ttu-id="d707b-620">Проверка выполняется.</span><span class="sxs-lookup"><span data-stu-id="d707b-620">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="d707b-621">Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="d707b-621">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="d707b-622">Сборки 16288</span><span class="sxs-lookup"><span data-stu-id="d707b-622">Build 16288</span></span>

<span data-ttu-id="d707b-623">Windows, общие сведения о сборке 16288 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span><span class="sxs-lookup"><span data-stu-id="d707b-623">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-624">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-624">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="d707b-625">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-625">WSL</span></span>
- <span data-ttu-id="d707b-626">Правильно инициализировать и отчетов uid, gid и режим для дескрипторов сокетов файл [2 490 GH]</span><span class="sxs-lookup"><span data-stu-id="d707b-626">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="d707b-627">Дополнительные улучшения и исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="d707b-627">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="d707b-628">Консоль</span><span class="sxs-lookup"><span data-stu-id="d707b-628">Console</span></span>
- <span data-ttu-id="d707b-629">Консоль, связанные с ними изменения в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="d707b-629">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-630">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-630">LTP Results:</span></span>
<span data-ttu-id="d707b-631">Без изменений с момента 16273</span><span class="sxs-lookup"><span data-stu-id="d707b-631">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="d707b-632">Сборки 16278</span><span class="sxs-lookup"><span data-stu-id="d707b-632">Build 16278</span></span>

<span data-ttu-id="d707b-633">Windows, общие сведения о сборке 162738 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span><span class="sxs-lookup"><span data-stu-id="d707b-633">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-634">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-634">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="d707b-635">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-635">WSL</span></span>
- <span data-ttu-id="d707b-636">Явно отменить сопоставление сопоставленных представлений из разделов в резервном файле, при закрытие мм LX состояние [GH 2415]</span><span class="sxs-lookup"><span data-stu-id="d707b-636">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="d707b-637">Дополнительные улучшения и исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="d707b-637">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="d707b-638">Консоль</span><span class="sxs-lookup"><span data-stu-id="d707b-638">Console</span></span>
- <span data-ttu-id="d707b-639">Консоль, связанные с ними изменения в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="d707b-639">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-640">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-640">LTP Results:</span></span>
<span data-ttu-id="d707b-641">Без изменений с момента 16273</span><span class="sxs-lookup"><span data-stu-id="d707b-641">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="d707b-642">Сборки 16275</span><span class="sxs-lookup"><span data-stu-id="d707b-642">Build 16275</span></span>

<span data-ttu-id="d707b-643">Windows, общие сведения о сборке 162735 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span><span class="sxs-lookup"><span data-stu-id="d707b-643">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-644">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-644">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="d707b-645">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-645">WSL</span></span>
- <span data-ttu-id="d707b-646">Нет WSL связанные изменения в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="d707b-646">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="d707b-647">Консоль</span><span class="sxs-lookup"><span data-stu-id="d707b-647">Console</span></span>
- <span data-ttu-id="d707b-648">Консоль, связанные с ними изменения в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="d707b-648">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-649">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-649">LTP Results:</span></span>
<span data-ttu-id="d707b-650">Без изменений с момента 16273</span><span class="sxs-lookup"><span data-stu-id="d707b-650">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="d707b-651">Сборки 16273</span><span class="sxs-lookup"><span data-stu-id="d707b-651">Build 16273</span></span>

<span data-ttu-id="d707b-652">Windows, общие сведения о сборке 16273 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span><span class="sxs-lookup"><span data-stu-id="d707b-652">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-653">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-653">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="d707b-654">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-654">WSL</span></span>
- <span data-ttu-id="d707b-655">Исправлена проблема, при котором иногда DrvFs сообщили свой тип неверный файл для каталогов [GH 2392]</span><span class="sxs-lookup"><span data-stu-id="d707b-655">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="d707b-656">Разрешить создание сокетов NETLINK_KOBJECT_UEVENT разблокировать программы, используйте uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span><span class="sxs-lookup"><span data-stu-id="d707b-656">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="d707b-657">Добавить поддержку без блокировки подключение [903 GH, 1391, 1584, 1585, 1829, 2290, 2314]</span><span class="sxs-lookup"><span data-stu-id="d707b-657">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="d707b-658">Реализуйте CLONE_FS клонировать флаг вызова системы [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="d707b-658">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="d707b-659">Исправить проблемы, связанные с не обрабатывает символы табуляции или кавычки в NT взаимодействия [GH 1625, 2164]</span><span class="sxs-lookup"><span data-stu-id="d707b-659">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="d707b-660">Разрешить доступ запрещен, произошла ошибка при попытке повторного запуска WSL экземпляров [GH 651, 2095]</span><span class="sxs-lookup"><span data-stu-id="d707b-660">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="d707b-661">Реализация futex FUTEX_REQUEUE и FUTEX_CMP_REQUEUE операций [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="d707b-661">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="d707b-662">Исправьте разрешения для разных файлов SysFs [GH 2214]</span><span class="sxs-lookup"><span data-stu-id="d707b-662">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="d707b-663">Исправьте зависания Haskell стека во время установки [GH 2290]</span><span class="sxs-lookup"><span data-stu-id="d707b-663">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="d707b-664">Реализовать binfmt_misc 'C' "о и флаги «P» [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="d707b-664">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="d707b-665">Добавить /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753 г.]</span><span class="sxs-lookup"><span data-stu-id="d707b-665">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="d707b-666">Добавление частичная поддержка ioprio_set системный вызов [GH 498]</span><span class="sxs-lookup"><span data-stu-id="d707b-666">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="d707b-667">Заглушки SO_REUSEPORT & добавлена поддержка SO_PASSCRED для сокетов netlink [GH 69]</span><span class="sxs-lookup"><span data-stu-id="d707b-667">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="d707b-668">Возвращать различных кодов ошибок из RegisterDistribuiton, если распределение в настоящее время находится в процессе установки или удаления.</span><span class="sxs-lookup"><span data-stu-id="d707b-668">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="d707b-669">Разрешить отмену регистрации частично установленный распределений WSL через wslconfig.exe</span><span class="sxs-lookup"><span data-stu-id="d707b-669">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="d707b-670">Исправьте зависания теста сокета python из udp::msg_peek</span><span class="sxs-lookup"><span data-stu-id="d707b-670">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="d707b-671">Дополнительные улучшения и исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="d707b-671">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="d707b-672">Консоль</span><span class="sxs-lookup"><span data-stu-id="d707b-672">Console</span></span>
- <span data-ttu-id="d707b-673">Консоль, связанные с ними изменения в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="d707b-673">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-674">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-674">LTP Results:</span></span>
<span data-ttu-id="d707b-675">Всего тестов: 1904</span><span class="sxs-lookup"><span data-stu-id="d707b-675">Total Tests: 1904</span></span><br/>
<span data-ttu-id="d707b-676">Всего пропущено тестов: 209</span><span class="sxs-lookup"><span data-stu-id="d707b-676">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="d707b-677">Общее количество ошибок: 229</span><span class="sxs-lookup"><span data-stu-id="d707b-677">Total Failures: 229</span></span><br/>
[<span data-ttu-id="d707b-678">LTP тестовый запуск журналы</span><span class="sxs-lookup"><span data-stu-id="d707b-678">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="d707b-679">Сборки 16257</span><span class="sxs-lookup"><span data-stu-id="d707b-679">Build 16257</span></span>

<span data-ttu-id="d707b-680">Windows, общие сведения о сборке 16257 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span><span class="sxs-lookup"><span data-stu-id="d707b-680">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-681">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-681">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="d707b-682">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-682">WSL</span></span>
- <span data-ttu-id="d707b-683">Реализуйте prlimit64 системный вызов</span><span class="sxs-lookup"><span data-stu-id="d707b-683">Implement prlimit64 system call</span></span>
- <span data-ttu-id="d707b-684">Добавлена поддержка ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="d707b-684">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="d707b-685">Заглушки MSG_MORE подключении через сокеты TCP [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="d707b-685">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="d707b-686">Исправление вспомогательных вектор поведение недопустимый AT_EXECFN [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="d707b-686">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="d707b-687">Исправления поведения копирования и вставки для консоли/tty и добавить более полный буфер, обработка [GH 2204, 2131]</span><span class="sxs-lookup"><span data-stu-id="d707b-687">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="d707b-688">Задайте AT_SECURE в векторе вспомогательных программ, set-user-ID и set-group-ID [GH 2031]</span><span class="sxs-lookup"><span data-stu-id="d707b-688">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="d707b-689">Psuedo терминалов конечной точки мастера не обрабатывает TIOCPGRP [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="d707b-689">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="d707b-690">Lseek исправление не rewind каталогов в LxFs [GH 2310]</span><span class="sxs-lookup"><span data-stu-id="d707b-690">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="d707b-691">Блокировка /dev/ptmx после интенсивного использования [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="d707b-691">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="d707b-692">Дополнительные улучшения и исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="d707b-692">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="d707b-693">Консоль</span><span class="sxs-lookup"><span data-stu-id="d707b-693">Console</span></span>
- <span data-ttu-id="d707b-694">Исправление для горизонтальной линии и символы подчеркивания Everywhere [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="d707b-694">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="d707b-695">Исправлена изменен порядок процесс внесения NPM труднее закрыть [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="d707b-695">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="d707b-696">Добавлены нашей новой цветовой схемы: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="d707b-696">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-697">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-697">LTP Results:</span></span>
<span data-ttu-id="d707b-698">Без изменений с момента 16251</span><span class="sxs-lookup"><span data-stu-id="d707b-698">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="d707b-699">Поддержка syscall</span><span class="sxs-lookup"><span data-stu-id="d707b-699">Syscall Support</span></span>
<span data-ttu-id="d707b-700">Ниже приведен список новых или улучшенных syscalls, которая содержит некоторые реализации в WSL.</span><span class="sxs-lookup"><span data-stu-id="d707b-700">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="d707b-701">В сценарии по крайней мере один поддерживаются syscalls в этом списке, но может не иметь все параметры, поддерживаемые в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="d707b-701">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="d707b-702">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="d707b-702">Known Issues</span></span>
#### [<a name="github-issue-2392-windows-folders-not-recognized-by-wsl-"></a><span data-ttu-id="d707b-703">GitHub Issue 2392: Папки Windows, не распознается средой WSL...</span><span class="sxs-lookup"><span data-stu-id="d707b-703">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="d707b-704">В построении 16257 WSL имеет проблемы при перечислении файлов и папок Windows с помощью `/mnt/c/...`.</span><span class="sxs-lookup"><span data-stu-id="d707b-704">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="d707b-705">Эта проблема была устранена и должен быть выпущен в течение недели, начинающейся 8/14/2017 сборка программы предварительной оценки.</span><span class="sxs-lookup"><span data-stu-id="d707b-705">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="d707b-706">Сборки 16251</span><span class="sxs-lookup"><span data-stu-id="d707b-706">Build 16251</span></span>

<span data-ttu-id="d707b-707">Windows, общие сведения о сборке 16251 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span><span class="sxs-lookup"><span data-stu-id="d707b-707">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-708">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-708">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="d707b-709">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-709">WSL</span></span>
- <span data-ttu-id="d707b-710">Удалить тег бета-версии из WSL дополнительный компонент, см. в разделе [блога](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="d707b-710">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="d707b-711">Правильно инициализируйте сохранен набор uid и gid для set-user-ID и set-group-ID двоичных файлов на exec [GH 962, 1415, 2072]</span><span class="sxs-lookup"><span data-stu-id="d707b-711">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="d707b-712">Добавлена поддержка ptrace PTRACE_O_TRACEEXIT [GH 555]</span><span class="sxs-lookup"><span data-stu-id="d707b-712">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="d707b-713">Добавлена поддержка ptrace PTRACE_GETFPREGS и PTRACE_GETREGSET с NT_FPREGSET [GH 555]</span><span class="sxs-lookup"><span data-stu-id="d707b-713">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="d707b-714">Исправлена ptrace для остановки на игнорировать сигналы</span><span class="sxs-lookup"><span data-stu-id="d707b-714">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="d707b-715">Дополнительные улучшения и исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="d707b-715">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="d707b-716">Консоль</span><span class="sxs-lookup"><span data-stu-id="d707b-716">Console</span></span>
- <span data-ttu-id="d707b-717">Консоль, связанные с ними изменения в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="d707b-717">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-718">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-718">LTP Results:</span></span>
<span data-ttu-id="d707b-719">Число тестов передачи: 768</span><span class="sxs-lookup"><span data-stu-id="d707b-719">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="d707b-720">Число тестов: 244</span><span class="sxs-lookup"><span data-stu-id="d707b-720">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="d707b-721">Число пропущенных тестов: 96</span><span class="sxs-lookup"><span data-stu-id="d707b-721">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="d707b-722">LTP тестовый запуск журналы</span><span class="sxs-lookup"><span data-stu-id="d707b-722">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="d707b-723">Сборки 16241</span><span class="sxs-lookup"><span data-stu-id="d707b-723">Build 16241</span></span>

<span data-ttu-id="d707b-724">Windows, общие сведения о сборке 16241 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span><span class="sxs-lookup"><span data-stu-id="d707b-724">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-725">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-725">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="d707b-726">WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-726">WSL</span></span>
- <span data-ttu-id="d707b-727">Нет WSL связанные изменения в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="d707b-727">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="d707b-728">Консоль</span><span class="sxs-lookup"><span data-stu-id="d707b-728">Console</span></span>
- <span data-ttu-id="d707b-729">Исправление для вывода недопустимый символ для DEC пересечения линии, сообщила, изначально [здесь](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span><span class="sxs-lookup"><span data-stu-id="d707b-729">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="d707b-730">Исправление для выходной текст не будет отображаться на кодовая страница 65001 (utf8)</span><span class="sxs-lookup"><span data-stu-id="d707b-730">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="d707b-731">Не обменивайтесь изменения, внесенные в значения одного цвета RGB в другие части палитры при изменении выделения.</span><span class="sxs-lookup"><span data-stu-id="d707b-731">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="d707b-732">Это сделает страницы свойств консоли гораздо проще использовать.</span><span class="sxs-lookup"><span data-stu-id="d707b-732">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="d707b-733">CTRL + S не отображается для правильной работы</span><span class="sxs-lookup"><span data-stu-id="d707b-733">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="d707b-734">Отмена полужирный / измерение полностью отсутствовать из ANSI escape-кодов [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="d707b-734">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="d707b-735">Консоль не поддерживает правильно Vim цветовые темы [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="d707b-735">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="d707b-736">Невозможно вставить определенных знаков [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="d707b-736">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="d707b-737">Перекомпоновка изменения размера, как это ни странно взаимодействует с изменение размеров окна bash при stuff редактирования в командной строке [GH ConEmu 1123]</span><span class="sxs-lookup"><span data-stu-id="d707b-737">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="d707b-738">Сочетание клавиш CTRL-L оставляет экрана "грязных" [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="d707b-738">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="d707b-739">Ошибки отрисовки консоли при отображении VT на HDPI [GH 1907]</span><span class="sxs-lookup"><span data-stu-id="d707b-739">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="d707b-740">Символы Japansese выглядеть странно, с помощью символа Юникода U + 30FB [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="d707b-740">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="d707b-741">Дополнительные улучшения и исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="d707b-741">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="d707b-742">Сборка 16237</span><span class="sxs-lookup"><span data-stu-id="d707b-742">Build 16237</span></span>

<span data-ttu-id="d707b-743">Windows, общие сведения о сборке 16237 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span><span class="sxs-lookup"><span data-stu-id="d707b-743">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-744">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-744">Fixed</span></span>
- <span data-ttu-id="d707b-745">Используйте атрибуты по умолчанию для файлов без EAs в lxfs (корень, корень, 0000)</span><span class="sxs-lookup"><span data-stu-id="d707b-745">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="d707b-746">Добавлена поддержка для дистрибутивов, использующие расширенные атрибуты</span><span class="sxs-lookup"><span data-stu-id="d707b-746">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="d707b-747">Исправить внутренние поля для записи, возвращенные getdents и getdents64</span><span class="sxs-lookup"><span data-stu-id="d707b-747">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="d707b-748">Исправить проверку разрешений для вызова системы SHM_STAT shmctl [GH 2068]</span><span class="sxs-lookup"><span data-stu-id="d707b-748">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="d707b-749">Состояние основных неверные начальной epoll телетайпы [GH 2231]</span><span class="sxs-lookup"><span data-stu-id="d707b-749">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="d707b-750">Исправить readdir DrvFs, не возвращающий все записи [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="d707b-750">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="d707b-751">Исправить LxFs readdir, когда файлы будут несвязанные [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="d707b-751">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="d707b-752">Разрешить файлы несвязанные drvfs быть открыт через procfs</span><span class="sxs-lookup"><span data-stu-id="d707b-752">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="d707b-753">Добавить переопределение ключа глобального реестра для отключения функций WSL (взаимодействия / диска подключение)</span><span class="sxs-lookup"><span data-stu-id="d707b-753">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="d707b-754">Исправить неверный блок счетчика в «stat» для DrvFs (и LxFs) [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="d707b-754">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="d707b-755">Дополнительные улучшения и исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="d707b-755">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="d707b-756">Сборки 16232</span><span class="sxs-lookup"><span data-stu-id="d707b-756">Build 16232</span></span>

<span data-ttu-id="d707b-757">Windows, общие сведения о сборке 16232 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span><span class="sxs-lookup"><span data-stu-id="d707b-757">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-758">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-758">Fixed</span></span>
- <span data-ttu-id="d707b-759">Нет WSL связанные изменения в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="d707b-759">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="d707b-760">Сборки 16226</span><span class="sxs-lookup"><span data-stu-id="d707b-760">Build 16226</span></span>

<span data-ttu-id="d707b-761">Windows, общие сведения о сборке 16226 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span><span class="sxs-lookup"><span data-stu-id="d707b-761">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-762">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-762">Fixed</span></span>
- <span data-ttu-id="d707b-763">xattr, связанные с поддержкой syscalls (getxattr, setxattr, listxattr, removexattr).</span><span class="sxs-lookup"><span data-stu-id="d707b-763">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="d707b-764">Поддержка xattr Security.capablity.</span><span class="sxs-lookup"><span data-stu-id="d707b-764">security.capablity xattr support.</span></span>
- <span data-ttu-id="d707b-765">Улучшенная совместимость с определенными файловые системы и фильтров, включая серверы SMB, отличных от MS.</span><span class="sxs-lookup"><span data-stu-id="d707b-765">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="d707b-766">[GH #1952]</span><span class="sxs-lookup"><span data-stu-id="d707b-766">[GH #1952]</span></span>
- <span data-ttu-id="d707b-767">Улучшенная поддержка OneDrive заполнители, заполнители GVFS и Compact ОС сжатые файлы.</span><span class="sxs-lookup"><span data-stu-id="d707b-767">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="d707b-768">Дополнительные улучшения и исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="d707b-768">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="d707b-769">Сборки 16215</span><span class="sxs-lookup"><span data-stu-id="d707b-769">Build 16215</span></span>

<span data-ttu-id="d707b-770">Windows, общие сведения о сборке 16215 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span><span class="sxs-lookup"><span data-stu-id="d707b-770">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-771">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-771">Fixed</span></span>
- <span data-ttu-id="d707b-772">WSL больше не требуется режим разработчика.</span><span class="sxs-lookup"><span data-stu-id="d707b-772">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="d707b-773">Поддерживает соединения каталогов в drvfs.</span><span class="sxs-lookup"><span data-stu-id="d707b-773">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="d707b-774">Дескриптор, при удалении пакетов appx WSL распространения.</span><span class="sxs-lookup"><span data-stu-id="d707b-774">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="d707b-775">Обновление procfs Показать частных и общих сопоставления.</span><span class="sxs-lookup"><span data-stu-id="d707b-775">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="d707b-776">Добавление возможности для wslconfig.exe для очистки дистрибутивов, которые частично установлено или удалено.</span><span class="sxs-lookup"><span data-stu-id="d707b-776">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="d707b-777">Добавлена поддержка для IP_MTU_DISCOVER сокетами TCP.</span><span class="sxs-lookup"><span data-stu-id="d707b-777">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="d707b-778">[GH 1639, 2115, 2205]</span><span class="sxs-lookup"><span data-stu-id="d707b-778">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="d707b-779">Получить семейства протоколов для маршрутов, чтобы AF_INADDR.</span><span class="sxs-lookup"><span data-stu-id="d707b-779">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="d707b-780">Усовершенствования устройству для последовательного порта [1929 годами GH].</span><span class="sxs-lookup"><span data-stu-id="d707b-780">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="d707b-781">Сборки 16199</span><span class="sxs-lookup"><span data-stu-id="d707b-781">Build 16199</span></span>

<span data-ttu-id="d707b-782">Windows, общие сведения о сборке 16199 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span><span class="sxs-lookup"><span data-stu-id="d707b-782">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-783">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-783">Fixed</span></span>
- <span data-ttu-id="d707b-784">Нет WSL связанные изменения в этих выпусков.</span><span class="sxs-lookup"><span data-stu-id="d707b-784">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="d707b-785">Сборки 16193</span><span class="sxs-lookup"><span data-stu-id="d707b-785">Build 16193</span></span>

<span data-ttu-id="d707b-786">Windows, общие сведения о сборке 16193 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span><span class="sxs-lookup"><span data-stu-id="d707b-786">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-787">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-787">Fixed</span></span>
- <span data-ttu-id="d707b-788">Условие состязания между отправкой SIGCONT и threadgroup, завершение [GH 1973 г.]</span><span class="sxs-lookup"><span data-stu-id="d707b-788">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="d707b-789">Изменение устройства tty и pty отчет FILE_DEVICE_NAMED_PIPE вместо FILE_DEVICE_CONSOLE [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="d707b-789">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="d707b-790">Исправление IP_OPTIONS SSH</span><span class="sxs-lookup"><span data-stu-id="d707b-790">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="d707b-791">Переместить подключение DrvFs init управляющей программы [1862 GH, 1968 году 1767, 1933]</span><span class="sxs-lookup"><span data-stu-id="d707b-791">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="d707b-792">Добавлена поддержка в DrvFs следуя NT символических ссылок.</span><span class="sxs-lookup"><span data-stu-id="d707b-792">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="d707b-793">Сборки 16184</span><span class="sxs-lookup"><span data-stu-id="d707b-793">Build 16184</span></span>

<span data-ttu-id="d707b-794">Windows, общие сведения о сборке 16184 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span><span class="sxs-lookup"><span data-stu-id="d707b-794">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-795">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-795">Fixed</span></span>
- <span data-ttu-id="d707b-796">Задача обслуживания удаленных пакетов apt (lxrun.exe/Update)</span><span class="sxs-lookup"><span data-stu-id="d707b-796">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="d707b-797">Исправлены выходные данные не отображаются в Windows процессов в node.js [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="d707b-797">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="d707b-798">Смягчать требования к выравниванию в lxcore [GH 1794]</span><span class="sxs-lookup"><span data-stu-id="d707b-798">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="d707b-799">Исправлена обработка AT_EMPTY_PATH флага в число системных вызовов.</span><span class="sxs-lookup"><span data-stu-id="d707b-799">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="d707b-800">Исправлена проблема, где удаление DrvFs файлы с открытыми дескрипторами создаст файл неопределенное поведение [GH 544,966,1357,1535,1615]</span><span class="sxs-lookup"><span data-stu-id="d707b-800">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="d707b-801">/ etc/hosts унаследует записей из файла hosts Windows (% windir%\system32\drivers\etc\hosts) [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="d707b-801">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="d707b-802">Сборки 16179</span><span class="sxs-lookup"><span data-stu-id="d707b-802">Build 16179</span></span>

<span data-ttu-id="d707b-803">Windows, общие сведения о сборке 16179 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span><span class="sxs-lookup"><span data-stu-id="d707b-803">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-804">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-804">Fixed</span></span>
- <span data-ttu-id="d707b-805">Нет WSL изменений на этой неделе.</span><span class="sxs-lookup"><span data-stu-id="d707b-805">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="d707b-806">Сборки 16176</span><span class="sxs-lookup"><span data-stu-id="d707b-806">Build 16176</span></span>

<span data-ttu-id="d707b-807">Windows, общие сведения о сборке 16176 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span><span class="sxs-lookup"><span data-stu-id="d707b-807">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-808">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-808">Fixed</span></span>

- [<span data-ttu-id="d707b-809">Включена поддержка последовательного порта</span><span class="sxs-lookup"><span data-stu-id="d707b-809">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="d707b-810">Добавлен параметр сокета IP-адрес IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="d707b-810">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="d707b-811">Реализована функция pwritev (при отправке файла в nginx, PHP-FPM) [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="d707b-811">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="d707b-812">Добавлены параметры сокета IP-адрес IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span><span class="sxs-lookup"><span data-stu-id="d707b-812">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="d707b-813">Поддержка параметр сокета IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="d707b-813">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="d707b-814">Добавлен параметр сокета _MTU IP-адрес (V6) для узла приложения, Трассировка маршрута, узнайте, nslookup, узла</span><span class="sxs-lookup"><span data-stu-id="d707b-814">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="d707b-815">Добавлен параметр сокета IP-адрес IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="d707b-815">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="d707b-816">Усовершенствования файловой системы</span><span class="sxs-lookup"><span data-stu-id="d707b-816">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="d707b-817">Разрешить подключение UNC-пути</span><span class="sxs-lookup"><span data-stu-id="d707b-817">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="d707b-818">Включить поддержку CDFS в drvfs</span><span class="sxs-lookup"><span data-stu-id="d707b-818">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="d707b-819">Правильно обрабатывать разрешения для сети файловых систем в drvfs</span><span class="sxs-lookup"><span data-stu-id="d707b-819">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="d707b-820">Добавьте поддержку удаленные диски drvfs</span><span class="sxs-lookup"><span data-stu-id="d707b-820">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="d707b-821">Включить FAT поддержки в drvfs</span><span class="sxs-lookup"><span data-stu-id="d707b-821">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="d707b-822">Дополнительные исправления и улучшения</span><span class="sxs-lookup"><span data-stu-id="d707b-822">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-823">Результаты LTP</span><span class="sxs-lookup"><span data-stu-id="d707b-823">LTP Results</span></span>
<span data-ttu-id="d707b-824">Нет изменений с момента 15042</span><span class="sxs-lookup"><span data-stu-id="d707b-824">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="d707b-825">Сборки 16170</span><span class="sxs-lookup"><span data-stu-id="d707b-825">Build 16170</span></span>

<span data-ttu-id="d707b-826">Windows, общие сведения о сборке 16170 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span><span class="sxs-lookup"><span data-stu-id="d707b-826">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="d707b-827">Мы выпустили новый [блога](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) обсуждения свои усилия на тестирование WSL.</span><span class="sxs-lookup"><span data-stu-id="d707b-827">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="d707b-828">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-828">Fixed</span></span>

- <span data-ttu-id="d707b-829">Поддержка сокета параметр IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="d707b-829">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="d707b-830">Добавлена поддержка PTRACE_OLDSETOPTIONS.</span><span class="sxs-lookup"><span data-stu-id="d707b-830">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="d707b-831">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="d707b-831">[GH 1692]</span></span>
- <span data-ttu-id="d707b-832">Дополнительные исправления и улучшения</span><span class="sxs-lookup"><span data-stu-id="d707b-832">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-833">Результаты LTP</span><span class="sxs-lookup"><span data-stu-id="d707b-833">LTP Results</span></span>
<span data-ttu-id="d707b-834">Нет изменений с момента 15042</span><span class="sxs-lookup"><span data-stu-id="d707b-834">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="d707b-835">Построение 15046 для Windows 10 Creators Update</span><span class="sxs-lookup"><span data-stu-id="d707b-835">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="d707b-836">Существует больше не WSL исправления или функций, запланированных для включения в обновлении до Windows 10 для дизайнеров.</span><span class="sxs-lookup"><span data-stu-id="d707b-836">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="d707b-837">Заметки о выпуске для WSL будет возобновлена в ближайшие недели для дополнения, предназначенных для значительным обновлением Windows.</span><span class="sxs-lookup"><span data-stu-id="d707b-837">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="d707b-838">Для Windows, общие сведения о сборке 15046 и будущих Insider выпусков посещение [блог Windows](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span><span class="sxs-lookup"><span data-stu-id="d707b-838">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="d707b-839">Сборки 15042</span><span class="sxs-lookup"><span data-stu-id="d707b-839">Build 15042</span></span>

<span data-ttu-id="d707b-840">Windows, общие сведения о сборке 15042 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span><span class="sxs-lookup"><span data-stu-id="d707b-840">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-841">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-841">Fixed</span></span>

- <span data-ttu-id="d707b-842">Исправлена взаимоблокировка при удалении пути, заканчивающиеся на «..»</span><span class="sxs-lookup"><span data-stu-id="d707b-842">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="d707b-843">Исправлена проблема, при котором fionbio СПЕЦИФИКАЦИИ, не возвращает 0 в случае успешного выполнения [GH 1683]</span><span class="sxs-lookup"><span data-stu-id="d707b-843">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="d707b-844">Устранена проблема с нулевой длины считывание inet. сокеты датаграмм</span><span class="sxs-lookup"><span data-stu-id="d707b-844">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="d707b-845">Устранения возможных взаимоблокировок из-за условия конкуренции в уточняющем запросе inode drvfs [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="d707b-845">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="d707b-846">Расширенная поддержка для данных вспомогательные сокет unix; SCM_CREDENTIALS и SCM_RIGHTS [GH 514, 613, 1326]</span><span class="sxs-lookup"><span data-stu-id="d707b-846">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="d707b-847">Дополнительные исправления и улучшения</span><span class="sxs-lookup"><span data-stu-id="d707b-847">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-848">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-848">LTP Results:</span></span>
<span data-ttu-id="d707b-849">Число пройденный тест: 737</span><span class="sxs-lookup"><span data-stu-id="d707b-849">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="d707b-850">Число с отрицательным (сбой, пропущенных и т. д...): 255</span><span class="sxs-lookup"><span data-stu-id="d707b-850">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="d707b-851">Сборки 15031</span><span class="sxs-lookup"><span data-stu-id="d707b-851">Build 15031</span></span>

<span data-ttu-id="d707b-852">Windows, общие сведения о сборке 15031 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span><span class="sxs-lookup"><span data-stu-id="d707b-852">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-853">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-853">Fixed</span></span>

- <span data-ttu-id="d707b-854">Исправлена ошибка, где бы нерегулярно проблемное time(2).</span><span class="sxs-lookup"><span data-stu-id="d707b-854">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="d707b-855">Исправлена и выдавать where \* SIGPROCMASK syscalls может повредить маска сигнала.</span><span class="sxs-lookup"><span data-stu-id="d707b-855">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="d707b-856">Теперь возвращают длину полную командную строку в WSL уведомление о создании процесса.</span><span class="sxs-lookup"><span data-stu-id="d707b-856">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="d707b-857">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="d707b-857">[GH 1632]</span></span>
- <span data-ttu-id="d707b-858">WSL теперь сообщает о выходе из потока через ptrace для зависаний GDB.</span><span class="sxs-lookup"><span data-stu-id="d707b-858">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="d707b-859">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="d707b-859">[GH 1196]</span></span>
- <span data-ttu-id="d707b-860">Исправлена ошибка, где ptys зависала после большой tmux операций ввода-ВЫВОДА.</span><span class="sxs-lookup"><span data-stu-id="d707b-860">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="d707b-861">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="d707b-861">[GH 1358]</span></span>
- <span data-ttu-id="d707b-862">Фиксированный время ожидания проверки в многих системных вызовов (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span><span class="sxs-lookup"><span data-stu-id="d707b-862">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="d707b-863">Поддержка EFD_SEMAPHORE добавлена eventfd [GH 452]</span><span class="sxs-lookup"><span data-stu-id="d707b-863">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="d707b-864">Дополнительные исправления и улучшения</span><span class="sxs-lookup"><span data-stu-id="d707b-864">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-865">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-865">LTP Results:</span></span>
<span data-ttu-id="d707b-866">Число пройденный тест: 737</span><span class="sxs-lookup"><span data-stu-id="d707b-866">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="d707b-867">Число с отрицательным (сбой, пропущенных и т. д...): 255</span><span class="sxs-lookup"><span data-stu-id="d707b-867">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="d707b-868">LTP тестовый запуск журналы</span><span class="sxs-lookup"><span data-stu-id="d707b-868">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="d707b-869">Сборки 15025</span><span class="sxs-lookup"><span data-stu-id="d707b-869">Build 15025</span></span>

<span data-ttu-id="d707b-870">Windows, общие сведения о сборке 15025 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span><span class="sxs-lookup"><span data-stu-id="d707b-870">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-871">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-871">Fixed</span></span>

- <span data-ttu-id="d707b-872">Исправление ошибки, продолжили grep 2.27 [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="d707b-872">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="d707b-873">Реализованный EFD_SEMAPHORE флаг для eventfd2 syscall [GH 452]</span><span class="sxs-lookup"><span data-stu-id="d707b-873">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="d707b-874">Реализации /proc/ [pid] / net/ipv6_route [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="d707b-874">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="d707b-875">Сигнал, поддержки операций ввода-ВЫВОДА для сокетов потока unix [GH 393 68]</span><span class="sxs-lookup"><span data-stu-id="d707b-875">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="d707b-876">Поддерживает F_GETPIPE_SZ и F_SETPIPE_SZ [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="d707b-876">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="d707b-877">Реализовать recvmmsg() syscall [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="d707b-877">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="d707b-878">Исправлена ошибка, где epoll_wait() не было ожидания [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="d707b-878">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="d707b-879">Реализовать /proc/version_signature</span><span class="sxs-lookup"><span data-stu-id="d707b-879">Implement /proc/version_signature</span></span>
- <span data-ttu-id="d707b-880">TEE syscall теперь возвращает сбой, если оба дескрипторов файлов см. в том же канал</span><span class="sxs-lookup"><span data-stu-id="d707b-880">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="d707b-881">Реализованный корректность поведения для SO_PEERCRED сокеты Unix</span><span class="sxs-lookup"><span data-stu-id="d707b-881">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="d707b-882">Обработка недопустимых параметров основных tkill syscall</span><span class="sxs-lookup"><span data-stu-id="d707b-882">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="d707b-883">Изменения, чтобы увеличить preformace drvfs</span><span class="sxs-lookup"><span data-stu-id="d707b-883">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="d707b-884">Внесены незначительные исправления для блокирующих операций ввода-ВЫВОДА для Ruby</span><span class="sxs-lookup"><span data-stu-id="d707b-884">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="d707b-885">Фиксированный recvmsg(), возвращая EINVAL MSG_DONTWAIT флага для сокетов inet [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="d707b-885">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="d707b-886">Дополнительные исправления и улучшения</span><span class="sxs-lookup"><span data-stu-id="d707b-886">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-887">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-887">LTP Results:</span></span>
<span data-ttu-id="d707b-888">Число пройденный тест: 732</span><span class="sxs-lookup"><span data-stu-id="d707b-888">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="d707b-889">Число с отрицательным (сбой, пропущенных и т. д...): 255</span><span class="sxs-lookup"><span data-stu-id="d707b-889">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="d707b-890">LTP тестовый запуск журналы</span><span class="sxs-lookup"><span data-stu-id="d707b-890">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="d707b-891">Сборки 15019</span><span class="sxs-lookup"><span data-stu-id="d707b-891">Build 15019</span></span>

<span data-ttu-id="d707b-892">Windows, общие сведения о сборке 15019 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span><span class="sxs-lookup"><span data-stu-id="d707b-892">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-893">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-893">Fixed</span></span>

- <span data-ttu-id="d707b-894">Исправлена ошибка, которая неверно определяется ЦП в procfs для средств, таких как htop (GH 823, 945, 971)</span><span class="sxs-lookup"><span data-stu-id="d707b-894">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="d707b-895">При вызове open() с O_TRUNC в существующем файле inotify теперь создает IN_MODIFY перед IN_OPEN</span><span class="sxs-lookup"><span data-stu-id="d707b-895">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="d707b-896">Исправления для getsockopt сокет unix SO_ERROR для включения postgress [GH-61, 1354]</span><span class="sxs-lookup"><span data-stu-id="d707b-896">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="d707b-897">Реализовать /proc/sys/net/core/somaxconn язык GO</span><span class="sxs-lookup"><span data-stu-id="d707b-897">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="d707b-898">Фоновая задача apt-get пакета обновления теперь запускается в скрытом из представления</span><span class="sxs-lookup"><span data-stu-id="d707b-898">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="d707b-899">Очистить область для ipv6 localhost (неуспешное завершение Spring-Framework(Java)).</span><span class="sxs-lookup"><span data-stu-id="d707b-899">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="d707b-900">Дополнительные исправления и улучшения</span><span class="sxs-lookup"><span data-stu-id="d707b-900">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-901">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-901">LTP Results:</span></span>
<span data-ttu-id="d707b-902">Число пройденный тест: 714</span><span class="sxs-lookup"><span data-stu-id="d707b-902">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="d707b-903">Число с отрицательным (сбой, пропущенных и т. д...): 249</span><span class="sxs-lookup"><span data-stu-id="d707b-903">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="d707b-904">LTP тестовый запуск журналы</span><span class="sxs-lookup"><span data-stu-id="d707b-904">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="d707b-905">Сборки 15014</span><span class="sxs-lookup"><span data-stu-id="d707b-905">Build 15014</span></span>

<span data-ttu-id="d707b-906">Windows, общие сведения о сборке 15014 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="d707b-906">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-907">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-907">Fixed</span></span>

- <span data-ttu-id="d707b-908">CTRL + C теперь работает должным образом</span><span class="sxs-lookup"><span data-stu-id="d707b-908">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="d707b-909">htop и ps auxw теперь Показать правильное использование ресурсов (GH #516)</span><span class="sxs-lookup"><span data-stu-id="d707b-909">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="d707b-910">Перевода сигналов исключения NT.</span><span class="sxs-lookup"><span data-stu-id="d707b-910">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="d707b-911">(GH #513)</span><span class="sxs-lookup"><span data-stu-id="d707b-911">(GH #513)</span></span>
- <span data-ttu-id="d707b-912">fallocate теперь завершается сбоем с ENOSPC когда заканчивается свободное место, а не EINVAL (GH #1571)</span><span class="sxs-lookup"><span data-stu-id="d707b-912">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="d707b-913">Добавлена /proc/sys/kernel/sem.</span><span class="sxs-lookup"><span data-stu-id="d707b-913">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="d707b-914">Реализованный semop и semtimedop системные вызовы</span><span class="sxs-lookup"><span data-stu-id="d707b-914">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="d707b-915">Фиксированный nslookup ошибки, связанные с IP_RECVTOS & IPV6_RECVTCLASS параметр сокета (GH 69)</span><span class="sxs-lookup"><span data-stu-id="d707b-915">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="d707b-916">Поддержка параметров сокета IP_RECVTTL и IPV6_RECVHOPLIMIT</span><span class="sxs-lookup"><span data-stu-id="d707b-916">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="d707b-917">Дополнительные исправления и улучшения</span><span class="sxs-lookup"><span data-stu-id="d707b-917">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-918">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-918">LTP Results:</span></span>
<span data-ttu-id="d707b-919">Число пройденный тест: 709</span><span class="sxs-lookup"><span data-stu-id="d707b-919">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="d707b-920">Число с отрицательным (сбой, пропущенных и т. д...): 255</span><span class="sxs-lookup"><span data-stu-id="d707b-920">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="d707b-921">LTP тестовый запуск журналы</span><span class="sxs-lookup"><span data-stu-id="d707b-921">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="d707b-922">Сводка по syscall</span><span class="sxs-lookup"><span data-stu-id="d707b-922">Syscall Summary</span></span>
<span data-ttu-id="d707b-923">Общее Syscalls: 384</span><span class="sxs-lookup"><span data-stu-id="d707b-923">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="d707b-924">Всего реализации: 235</span><span class="sxs-lookup"><span data-stu-id="d707b-924">Total Implemented: 235</span></span> </br>
<span data-ttu-id="d707b-925">Всего заглушка: 22</span><span class="sxs-lookup"><span data-stu-id="d707b-925">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="d707b-926">Если не реализовано, всего: 127</span><span class="sxs-lookup"><span data-stu-id="d707b-926">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="d707b-927">Подробный разбор</span><span class="sxs-lookup"><span data-stu-id="d707b-927">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="d707b-928">Сборки 15007</span><span class="sxs-lookup"><span data-stu-id="d707b-928">Build 15007</span></span>

<span data-ttu-id="d707b-929">Windows, общие сведения о сборке 15007 см. в статье [блог Windows]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span><span class="sxs-lookup"><span data-stu-id="d707b-929">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="d707b-930">Известная проблема</span><span class="sxs-lookup"><span data-stu-id="d707b-930">Known Issue</span></span>

- <span data-ttu-id="d707b-931">Есть известная ошибка, где консоль не распознает некоторые Ctrl + <key> ввода.</span><span class="sxs-lookup"><span data-stu-id="d707b-931">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="d707b-932">Это включает в себя команду ctrl-c, которая будет выступать в качестве обычных 'c' keypress.</span><span class="sxs-lookup"><span data-stu-id="d707b-932">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="d707b-933">Возможное решение. Сопоставьте альтернативного ключа Ctrl + C.</span><span class="sxs-lookup"><span data-stu-id="d707b-933">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="d707b-934">Например, сделать Ctrl + K, чтобы сочетание клавиш Ctrl + C для сопоставления: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="d707b-934">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="d707b-935">Это сопоставление в терминалов и придется сделать *каждые* запускается время bash.</span><span class="sxs-lookup"><span data-stu-id="d707b-935">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="d707b-936">Пользователи могут анализировать параметр для включения в их</span><span class="sxs-lookup"><span data-stu-id="d707b-936">Users can explore the option to include this in their</span></span> `.bashrc`

### <a name="fixed"></a><span data-ttu-id="d707b-937">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-937">Fixed</span></span>

- <span data-ttu-id="d707b-938">Исправлена проблема, где под управлением WSL займут 100% ядра ЦП</span><span class="sxs-lookup"><span data-stu-id="d707b-938">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="d707b-939">Параметром IP_PKTINFO, теперь поддерживается IPV6_RECVPKTINFO сокета.</span><span class="sxs-lookup"><span data-stu-id="d707b-939">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="d707b-940">(GH #851 987)</span><span class="sxs-lookup"><span data-stu-id="d707b-940">(GH #851, 987)</span></span>
- <span data-ttu-id="d707b-941">Усечение физический адрес сетевого интерфейса на 16 байт в lxcore (1452 # GH, 1414, 1343, 468, 308)</span><span class="sxs-lookup"><span data-stu-id="d707b-941">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="d707b-942">Дополнительные исправления и улучшения</span><span class="sxs-lookup"><span data-stu-id="d707b-942">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-943">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-943">LTP Results:</span></span>
<span data-ttu-id="d707b-944">Число пройденный тест: 709</span><span class="sxs-lookup"><span data-stu-id="d707b-944">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="d707b-945">Число с отрицательным (сбой, пропущенных и т. д...): 255</span><span class="sxs-lookup"><span data-stu-id="d707b-945">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="d707b-946">LTP тестовый запуск журналы</span><span class="sxs-lookup"><span data-stu-id="d707b-946">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="d707b-947">15002 сборки</span><span class="sxs-lookup"><span data-stu-id="d707b-947">Build 15002</span></span>

<span data-ttu-id="d707b-948">Windows, общие сведения о сборке 15002 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span><span class="sxs-lookup"><span data-stu-id="d707b-948">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="d707b-949">Известная проблема</span><span class="sxs-lookup"><span data-stu-id="d707b-949">Known Issue</span></span>

<span data-ttu-id="d707b-950">Известны две проблемы:</span><span class="sxs-lookup"><span data-stu-id="d707b-950">Two known issues:</span></span>
- <span data-ttu-id="d707b-951">Есть известная ошибка, где консоль не распознает некоторые Ctrl + <key> ввода.</span><span class="sxs-lookup"><span data-stu-id="d707b-951">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="d707b-952">Это включает в себя команду ctrl-c, которая будет выступать в качестве обычных 'c' keypress.</span><span class="sxs-lookup"><span data-stu-id="d707b-952">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="d707b-953">Возможное решение. Сопоставьте альтернативного ключа Ctrl + C.</span><span class="sxs-lookup"><span data-stu-id="d707b-953">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="d707b-954">Например, сделать Ctrl + K, чтобы сочетание клавиш Ctrl + C для сопоставления: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="d707b-954">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="d707b-955">Это сопоставление в терминалов и придется сделать *каждые* запускается время bash.</span><span class="sxs-lookup"><span data-stu-id="d707b-955">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="d707b-956">Пользователи могут анализировать параметр для включения в их</span><span class="sxs-lookup"><span data-stu-id="d707b-956">Users can explore the option to include this in their</span></span> `.bashrc`

- <span data-ttu-id="d707b-957">Во время работы WSL в потоке операционной системы будет составлять 100% ядра ЦП.</span><span class="sxs-lookup"><span data-stu-id="d707b-957">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="d707b-958">Основной причиной адрес и исправлена внутренним образом.</span><span class="sxs-lookup"><span data-stu-id="d707b-958">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="d707b-959">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-959">Fixed</span></span>

- <span data-ttu-id="d707b-960">Все сеансы bash теперь должны создаваться с тем же уровнем разрешений.</span><span class="sxs-lookup"><span data-stu-id="d707b-960">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="d707b-961">Попытка запустить сеанс на другом уровне будет блокироваться.</span><span class="sxs-lookup"><span data-stu-id="d707b-961">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="d707b-962">Это означает, что нельзя запустить консолей администрирования и без прав администратора, в то же время.</span><span class="sxs-lookup"><span data-stu-id="d707b-962">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="d707b-963">(GH #626)</span><span class="sxs-lookup"><span data-stu-id="d707b-963">(GH #626)</span></span>
<br/>
- <span data-ttu-id="d707b-964">Реализованы следующие сообщения NETLINK_ROUTE (требуются права администратора Windows)</span><span class="sxs-lookup"><span data-stu-id="d707b-964">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="d707b-965">RTM_NEWADDR (поддерживает `ip addr add`)</span><span class="sxs-lookup"><span data-stu-id="d707b-965">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="d707b-966">RTM_NEWROUTE (поддерживает `ip route add`)</span><span class="sxs-lookup"><span data-stu-id="d707b-966">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="d707b-967">RTM_DELADDR (поддерживает `ip addr del`)</span><span class="sxs-lookup"><span data-stu-id="d707b-967">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="d707b-968">RTM_DELROUTE (поддерживает `ip route del`)</span><span class="sxs-lookup"><span data-stu-id="d707b-968">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="d707b-969">Запланированная задача, проверка пакеты для обновления больше не будут работать, использующим лимитное подключение (GH #1371)</span><span class="sxs-lookup"><span data-stu-id="d707b-969">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="d707b-970">Исправлена ошибка, где по конвейеру получает заблокирована т. е. bash - c «ls - alR /» | bash -c «cat» (приложением 1214 # GH)</span><span class="sxs-lookup"><span data-stu-id="d707b-970">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="d707b-971">Параметр сокета реализованного TCP_KEEPCNT (GH #843)</span><span class="sxs-lookup"><span data-stu-id="d707b-971">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="d707b-972">Параметр сокета реализованного IP_MTU_DISCOVER INET (GH #720, 717, 170, 69)</span><span class="sxs-lookup"><span data-stu-id="d707b-972">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="d707b-973">Удалены устаревшие функциональные возможности запускать исполняемые файлы NT из init с NT пути поиска.</span><span class="sxs-lookup"><span data-stu-id="d707b-973">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="d707b-974">(GH #1325)</span><span class="sxs-lookup"><span data-stu-id="d707b-974">(GH #1325)</span></span>
- <span data-ttu-id="d707b-975">Исправление режима для/dev/kmsg, чтобы разрешить группа или доступ на чтение (0644) (GH #1321)</span><span class="sxs-lookup"><span data-stu-id="d707b-975">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="d707b-976">Реализованный /proc/sys/kernel/random/uuid (GH #1092)</span><span class="sxs-lookup"><span data-stu-id="d707b-976">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="d707b-977">Исправлена ошибка, где время запуска процесса отображалось как год 2432 (GH #974)</span><span class="sxs-lookup"><span data-stu-id="d707b-977">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="d707b-978">Переменной среды по умолчанию коммутируемой ТЕРМИН xterm-256color (GH #1446)</span><span class="sxs-lookup"><span data-stu-id="d707b-978">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="d707b-979">Измененный так, что процесс фиксации вычисляется во время процесса вилки.</span><span class="sxs-lookup"><span data-stu-id="d707b-979">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="d707b-980">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="d707b-980">(GH #1286)</span></span>
- <span data-ttu-id="d707b-981">Реализованный /proc/sys/vm/overcommit_memory.</span><span class="sxs-lookup"><span data-stu-id="d707b-981">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="d707b-982">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="d707b-982">(GH #1286)</span></span>
- <span data-ttu-id="d707b-983">Файл реализованного /proc/net/route (GH #69)</span><span class="sxs-lookup"><span data-stu-id="d707b-983">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="d707b-984">Исправлена ошибка, где имя ярлыка был неправильно локализованные (GH #696)</span><span class="sxs-lookup"><span data-stu-id="d707b-984">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="d707b-985">Фиксированный elf, синтаксический анализ логику, которая неправильно проверяет заголовки программы должно быть меньше (или равным) PATH_MAX.</span><span class="sxs-lookup"><span data-stu-id="d707b-985">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="d707b-986">(GH #1048)</span><span class="sxs-lookup"><span data-stu-id="d707b-986">(GH #1048)</span></span>
- <span data-ttu-id="d707b-987">Реализованный statfs обратный вызов для procfs sysfs cgroupfs и binfmtfs (GH #1378)</span><span class="sxs-lookup"><span data-stu-id="d707b-987">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="d707b-988">Фиксированные AptPackageIndexUpdate окна, которые не будет закрыто (GH #1184, также представлены в GH 1193)</span><span class="sxs-lookup"><span data-stu-id="d707b-988">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="d707b-989">Добавлена ASLR индивидуальность ADDR_NO_RANDOMIZE поддержки.</span><span class="sxs-lookup"><span data-stu-id="d707b-989">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="d707b-990">(GH #1148 1128)</span><span class="sxs-lookup"><span data-stu-id="d707b-990">(GH #1148, 1128)</span></span>
- <span data-ttu-id="d707b-991">Улучшенная PTRACE_GETSIGINFO, SIGSEGV, для правильной gdb трассировок стека во время AV (GH #875)</span><span class="sxs-lookup"><span data-stu-id="d707b-991">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="d707b-992">Elf, синтаксический анализ больше не завершается ошибкой для patchelf двоичных файлов.</span><span class="sxs-lookup"><span data-stu-id="d707b-992">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="d707b-993">(GH #471)</span><span class="sxs-lookup"><span data-stu-id="d707b-993">(GH #471)</span></span>
- <span data-ttu-id="d707b-994">VPN DNS передаются /etc/resolv.conf (GH #416, 1350)</span><span class="sxs-lookup"><span data-stu-id="d707b-994">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="d707b-995">Усовершенствования TCP закройте для более надежной передачи данных.</span><span class="sxs-lookup"><span data-stu-id="d707b-995">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="d707b-996">(GH #610 616, 1025, 1335)</span><span class="sxs-lookup"><span data-stu-id="d707b-996">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="d707b-997">Теперь возвращают правильный код ошибки при слишком много файлов открыто (EMFILE).</span><span class="sxs-lookup"><span data-stu-id="d707b-997">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="d707b-998">(GH #1126 2090)</span><span class="sxs-lookup"><span data-stu-id="d707b-998">(GH #1126, 2090)</span></span>
- <span data-ttu-id="d707b-999">Аудит Windows теперь отчеты по журналу имя изображения в процессе создания аудита.</span><span class="sxs-lookup"><span data-stu-id="d707b-999">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="d707b-1000">Теперь корректно ошибкой при запуске bash.exe из в окне bash</span><span class="sxs-lookup"><span data-stu-id="d707b-1000">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="d707b-1001">Добавлено сообщение об ошибке при взаимодействия не имеет доступа к в рабочий каталог, в разделе LxFs (т. е. .bashrc notepad.exe)</span><span class="sxs-lookup"><span data-stu-id="d707b-1001">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="d707b-1002">Исправлена проблема, где путь Windows был усечен в WSL</span><span class="sxs-lookup"><span data-stu-id="d707b-1002">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="d707b-1003">Дополнительные исправления и улучшения</span><span class="sxs-lookup"><span data-stu-id="d707b-1003">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-1004">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-1004">LTP Results:</span></span>
<span data-ttu-id="d707b-1005">Число пройденный тест: 690</span><span class="sxs-lookup"><span data-stu-id="d707b-1005">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="d707b-1006">Число с отрицательным (сбой, пропущенных и т. д...): 274</span><span class="sxs-lookup"><span data-stu-id="d707b-1006">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="d707b-1007">LTP тестовый запуск журналы</span><span class="sxs-lookup"><span data-stu-id="d707b-1007">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="d707b-1008">Поддержка syscall</span><span class="sxs-lookup"><span data-stu-id="d707b-1008">Syscall Support</span></span>
<span data-ttu-id="d707b-1009">Ниже приведен список новых или улучшенных syscalls, которая содержит некоторые реализации в WSL.</span><span class="sxs-lookup"><span data-stu-id="d707b-1009">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="d707b-1010">В сценарии по крайней мере один поддерживаются syscalls в этом списке, но может не иметь все параметры, поддерживаемые в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="d707b-1010">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="d707b-1011">Сборки 14986</span><span class="sxs-lookup"><span data-stu-id="d707b-1011">Build 14986</span></span>

<span data-ttu-id="d707b-1012">Windows, общие сведения о сборке 14986 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span><span class="sxs-lookup"><span data-stu-id="d707b-1012">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-1013">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-1013">Fixed</span></span>

- <span data-ttu-id="d707b-1014">Основные проверки ошибок с Netlink и IOCTL Pty</span><span class="sxs-lookup"><span data-stu-id="d707b-1014">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="d707b-1015">Версия ядра теперь сообщает 4.4.0-43 для обеспечения согласованности с Xenial</span><span class="sxs-lookup"><span data-stu-id="d707b-1015">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="d707b-1016">Bash.exe теперь запускается при направлении ввода в "nul:" (GH #1259)</span><span class="sxs-lookup"><span data-stu-id="d707b-1016">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="d707b-1017">Идентификаторы теперь искажены в procfs (GH #967)</span><span class="sxs-lookup"><span data-stu-id="d707b-1017">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="d707b-1018">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | Флаги IN_ISDIR, теперь поддерживается в inotify_add_watch() (GH #1280)</span><span class="sxs-lookup"><span data-stu-id="d707b-1018">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="d707b-1019">Реализуйте timer_create и связанные системные вызовы.</span><span class="sxs-lookup"><span data-stu-id="d707b-1019">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="d707b-1020">Это обеспечивает поддержку GHC (GH #307)</span><span class="sxs-lookup"><span data-stu-id="d707b-1020">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="d707b-1021">Исправлена проблема, когда ping, возвращенный время 0.000ms (GH #1296)</span><span class="sxs-lookup"><span data-stu-id="d707b-1021">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="d707b-1022">Возвращает правильный код ошибки, если открыто слишком много файлов.</span><span class="sxs-lookup"><span data-stu-id="d707b-1022">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="d707b-1023">Устранена проблема в WSL, где Netlink для сетевого интерфейса данных вернет ошибку EINVAL Если адрес интерфейса оборудования является 32-байтовое (например, интерфейс Teredo)</span><span class="sxs-lookup"><span data-stu-id="d707b-1023">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="d707b-1024">Обратите внимание на то, что программа Linux «IP-адрес» содержит ошибку, где он аварийно, если WSL сообщает адрес 32-разрядного оборудования.</span><span class="sxs-lookup"><span data-stu-id="d707b-1024">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="d707b-1025">Это ошибка в «IP-адрес», не WSL.</span><span class="sxs-lookup"><span data-stu-id="d707b-1025">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="d707b-1026">«IP-адрес» служебная программа жестко длину буфера строки используется для печати аппаратный адрес, и этот буфер слишком мал, чтобы отображать адрес 32-разрядного оборудования.</span><span class="sxs-lookup"><span data-stu-id="d707b-1026">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="d707b-1027">Дополнительные исправления и улучшения</span><span class="sxs-lookup"><span data-stu-id="d707b-1027">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-1028">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-1028">LTP Results:</span></span>
<span data-ttu-id="d707b-1029">Число пройденный тест: 669</span><span class="sxs-lookup"><span data-stu-id="d707b-1029">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="d707b-1030">Число с отрицательным (сбой, пропущенных и т. д...): 258</span><span class="sxs-lookup"><span data-stu-id="d707b-1030">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="d707b-1031">LTP тестовый запуск журналы</span><span class="sxs-lookup"><span data-stu-id="d707b-1031">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="d707b-1032">Поддержка syscall</span><span class="sxs-lookup"><span data-stu-id="d707b-1032">Syscall Support</span></span>
<span data-ttu-id="d707b-1033">Ниже приведен список новых или улучшенных syscalls, которая содержит некоторые реализации в WSL.</span><span class="sxs-lookup"><span data-stu-id="d707b-1033">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="d707b-1034">В сценарии по крайней мере один поддерживаются syscalls в этом списке, но может не иметь все параметры, поддерживаемые в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="d707b-1034">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="d707b-1035">Сборки 14971</span><span class="sxs-lookup"><span data-stu-id="d707b-1035">Build 14971</span></span>

<span data-ttu-id="d707b-1036">Windows, общие сведения о сборке 14971 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="d707b-1036">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-1037">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-1037">Fixed</span></span>

 - <span data-ttu-id="d707b-1038">Из-за обстоятельств, помимо наш элемент управления нет обновлений, в этой сборке для подсистемы Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="d707b-1038">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="d707b-1039">В следующем выпуске будет возобновлена регулярно запланированных обновлений.</span><span class="sxs-lookup"><span data-stu-id="d707b-1039">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-1040">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-1040">LTP Results:</span></span>
<span data-ttu-id="d707b-1041">Изменились по сравнению с 14965</span><span class="sxs-lookup"><span data-stu-id="d707b-1041">Unchanged from 14965</span></span> </br>
<span data-ttu-id="d707b-1042">Число пройденный тест: 664</span><span class="sxs-lookup"><span data-stu-id="d707b-1042">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="d707b-1043">Число с отрицательным (сбой, пропущенных и т. д...): 263</span><span class="sxs-lookup"><span data-stu-id="d707b-1043">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="d707b-1044">LTP тестовый запуск журналы</span><span class="sxs-lookup"><span data-stu-id="d707b-1044">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="d707b-1045">Сборки 14965</span><span class="sxs-lookup"><span data-stu-id="d707b-1045">Build 14965</span></span>

<span data-ttu-id="d707b-1046">Windows, общие сведения о сборке 14965 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="d707b-1046">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-1047">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-1047">Fixed</span></span>

- <span data-ttu-id="d707b-1048">Поддержка Netlink сокеты протокола NETLINK_ROUTE RTM_GETLINK и RTM_GETADDR (GH #468)</span><span class="sxs-lookup"><span data-stu-id="d707b-1048">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="d707b-1049">Включает команды ifconfig и IP-адрес для сети перечисления</span><span class="sxs-lookup"><span data-stu-id="d707b-1049">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="d707b-1050">Дополнительные сведения можно найти в нашей [WSL сети блога](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span><span class="sxs-lookup"><span data-stu-id="d707b-1050">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="d707b-1051">/ sbin теперь находится в пути пользователя по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d707b-1051">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="d707b-1052">Путь пользователя NT, теперь добавить к пути WSL по умолчанию (т. е. можно ввести notepad.exe без добавления System32 в пути Linux)</span><span class="sxs-lookup"><span data-stu-id="d707b-1052">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="d707b-1053">Добавлена поддержка /proc/sys/kernel/cap_last_cap</span><span class="sxs-lookup"><span data-stu-id="d707b-1053">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="d707b-1054">Двоичные файлы NT теперь могут запускаться из WSL, если текущий рабочий каталог содержит символы не удовлетворяющую стандарту ansi (GH #1254)</span><span class="sxs-lookup"><span data-stu-id="d707b-1054">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="d707b-1055">Разрешить завершение работы на отключенных сокет unix потока.</span><span class="sxs-lookup"><span data-stu-id="d707b-1055">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="d707b-1056">Добавлена поддержка PR_GET_PDEATHSIG.</span><span class="sxs-lookup"><span data-stu-id="d707b-1056">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="d707b-1057">Добавлена поддержка CLONE_PARENT</span><span class="sxs-lookup"><span data-stu-id="d707b-1057">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="d707b-1058">Исправлена ошибка, где по конвейеру получает заблокирована т. е. bash - c «ls - alR /» | bash -c «cat» (приложением 1214 # GH)</span><span class="sxs-lookup"><span data-stu-id="d707b-1058">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="d707b-1059">Дескриптор запросы на подключение к текущего терминала.</span><span class="sxs-lookup"><span data-stu-id="d707b-1059">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="d707b-1060">Пометить /proc/<pid>/oom_score_adj как доступный для записи.</span><span class="sxs-lookup"><span data-stu-id="d707b-1060">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="d707b-1061">Добавьте папку /sys/fs/cgroup.</span><span class="sxs-lookup"><span data-stu-id="d707b-1061">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="d707b-1062">sched_setaffinity должен возвращать число битов маски схожести</span><span class="sxs-lookup"><span data-stu-id="d707b-1062">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="d707b-1063">Исправьте ELF логику проверки, который неправильно предполагается, что интерпретатор пути должны быть короче 64 символов.</span><span class="sxs-lookup"><span data-stu-id="d707b-1063">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="d707b-1064">(GH #743)</span><span class="sxs-lookup"><span data-stu-id="d707b-1064">(GH #743)</span></span>
- <span data-ttu-id="d707b-1065">Дескрипторов открытых файлов может поддерживать консоли окно открытым (GH #1187)</span><span class="sxs-lookup"><span data-stu-id="d707b-1065">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="d707b-1066">Ошибка Fixeed, где не удалось rename() с завершающей косой чертой на имя целевого объекта (GH #1008)</span><span class="sxs-lookup"><span data-stu-id="d707b-1066">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="d707b-1067">Реализации /proc/net/dev файла</span><span class="sxs-lookup"><span data-stu-id="d707b-1067">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="d707b-1068">Проверка связи с предопределенной 0.000ms из-за разрешения таймера.</span><span class="sxs-lookup"><span data-stu-id="d707b-1068">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="d707b-1069">Реализованный /proc/self/environ (GH #730)</span><span class="sxs-lookup"><span data-stu-id="d707b-1069">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="d707b-1070">Дополнительных исправлений и улучшений</span><span class="sxs-lookup"><span data-stu-id="d707b-1070">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-1071">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-1071">LTP Results:</span></span>
<span data-ttu-id="d707b-1072">Число пройденный тест: 664</span><span class="sxs-lookup"><span data-stu-id="d707b-1072">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="d707b-1073">Число с отрицательным (сбой, пропущенных и т. д...): 263</span><span class="sxs-lookup"><span data-stu-id="d707b-1073">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="d707b-1074">LTP тестовый запуск журналы</span><span class="sxs-lookup"><span data-stu-id="d707b-1074">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="d707b-1075">Сборки 14959</span><span class="sxs-lookup"><span data-stu-id="d707b-1075">Build 14959</span></span>

<span data-ttu-id="d707b-1076">Windows, общие сведения о сборке 14959 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span><span class="sxs-lookup"><span data-stu-id="d707b-1076">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-1077">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-1077">Fixed</span></span>

- <span data-ttu-id="d707b-1078">Улучшенная функция уведомления использованием процесс для Windows.</span><span class="sxs-lookup"><span data-stu-id="d707b-1078">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="d707b-1079">Дополнительные сведения см. на [WSL блог](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span><span class="sxs-lookup"><span data-stu-id="d707b-1079">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="d707b-1080">Улучшенная стабильность с Windows взаимодействия</span><span class="sxs-lookup"><span data-stu-id="d707b-1080">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="d707b-1081">Исправлена ошибка 0x80070057 при запуске bash.exe при включении защиты данных предприятия (EDP)</span><span class="sxs-lookup"><span data-stu-id="d707b-1081">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="d707b-1082">Дополнительных исправлений и улучшений</span><span class="sxs-lookup"><span data-stu-id="d707b-1082">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-1083">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-1083">LTP Results:</span></span>
<span data-ttu-id="d707b-1084">Число пройденный тест: 665</span><span class="sxs-lookup"><span data-stu-id="d707b-1084">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="d707b-1085">Число с отрицательным (сбой, пропущенных и т. д...): 263</span><span class="sxs-lookup"><span data-stu-id="d707b-1085">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="d707b-1086">LTP тестовый запуск журналы</span><span class="sxs-lookup"><span data-stu-id="d707b-1086">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="d707b-1087">Сборки 14955</span><span class="sxs-lookup"><span data-stu-id="d707b-1087">Build 14955</span></span>

<span data-ttu-id="d707b-1088">Windows, общие сведения о сборке 14955 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span><span class="sxs-lookup"><span data-stu-id="d707b-1088">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-1089">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-1089">Fixed</span></span>

 - <span data-ttu-id="d707b-1090">Из-за обстоятельств, помимо наш элемент управления нет обновлений, в этой сборке для подсистемы Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="d707b-1090">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="d707b-1091">В следующем выпуске будет возобновлена регулярно запланированных обновлений.</span><span class="sxs-lookup"><span data-stu-id="d707b-1091">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-1092">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-1092">LTP Results:</span></span>
<span data-ttu-id="d707b-1093">Число пройденный тест: 665</span><span class="sxs-lookup"><span data-stu-id="d707b-1093">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="d707b-1094">Число с отрицательным (сбой, пропущенных и т. д...): 263</span><span class="sxs-lookup"><span data-stu-id="d707b-1094">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="d707b-1095">LTP тестовый запуск журналы</span><span class="sxs-lookup"><span data-stu-id="d707b-1095">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="d707b-1096">Сборки 14951</span><span class="sxs-lookup"><span data-stu-id="d707b-1096">Build 14951</span></span>

<span data-ttu-id="d707b-1097">Windows, общие сведения о сборке 14951 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="d707b-1097">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="d707b-1098">Новые возможности: Windows или Ubuntu взаимодействия</span><span class="sxs-lookup"><span data-stu-id="d707b-1098">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="d707b-1099">Двоичные файлы Windows теперь могут вызываться непосредственно из командной строки WSL.</span><span class="sxs-lookup"><span data-stu-id="d707b-1099">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="d707b-1100">Это дает пользователям возможность взаимодействовать с их среды Windows и системы таким образом, не было возможно.</span><span class="sxs-lookup"><span data-stu-id="d707b-1100">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="d707b-1101">Как краткий пример теперь стало возможным для пользователей, выполните следующие команды:</span><span class="sxs-lookup"><span data-stu-id="d707b-1101">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="d707b-1102">Дополнительные сведения можно найти в:</span><span class="sxs-lookup"><span data-stu-id="d707b-1102">More information can be found at:</span></span>

- [<span data-ttu-id="d707b-1103">Блог группы WSL для взаимодействия</span><span class="sxs-lookup"><span data-stu-id="d707b-1103">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="d707b-1104">Взаимодействия документации MSDN</span><span class="sxs-lookup"><span data-stu-id="d707b-1104">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="d707b-1105">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-1105">Fixed</span></span>

- <span data-ttu-id="d707b-1106">Ubuntu 16.04 (Xenial) теперь устанавливается для всех новых экземпляров WSL.</span><span class="sxs-lookup"><span data-stu-id="d707b-1106">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="d707b-1107">Пользователи с существующими экземплярами 14.04 (надежных) не обновляются автоматически.</span><span class="sxs-lookup"><span data-stu-id="d707b-1107">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="d707b-1108">Теперь отображается языкового стандарта, установленного во время установки</span><span class="sxs-lookup"><span data-stu-id="d707b-1108">Locale set during install is now displayed</span></span>
- <span data-ttu-id="d707b-1109">Терминалов улучшений, включая ошибки, где перенаправление WSL процесса в файл не всегда работать</span><span class="sxs-lookup"><span data-stu-id="d707b-1109">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="d707b-1110">Время существования консоли должны привязываться к времени существования bash.exe</span><span class="sxs-lookup"><span data-stu-id="d707b-1110">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="d707b-1111">Размер окна консоли следует использовать видимым размер, а не размер буфера</span><span class="sxs-lookup"><span data-stu-id="d707b-1111">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="d707b-1112">Дополнительных исправлений и улучшений</span><span class="sxs-lookup"><span data-stu-id="d707b-1112">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-1113">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-1113">LTP Results:</span></span>
<span data-ttu-id="d707b-1114">Число пройденный тест: 665</span><span class="sxs-lookup"><span data-stu-id="d707b-1114">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="d707b-1115">Число с отрицательным (сбой, пропущенных и т. д...): 263</span><span class="sxs-lookup"><span data-stu-id="d707b-1115">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="d707b-1116">LTP тестовый запуск журналы</span><span class="sxs-lookup"><span data-stu-id="d707b-1116">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="d707b-1117">Сборки 14946</span><span class="sxs-lookup"><span data-stu-id="d707b-1117">Build 14946</span></span>

<span data-ttu-id="d707b-1118">Windows, общие сведения о сборке 14946 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span><span class="sxs-lookup"><span data-stu-id="d707b-1118">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-1119">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-1119">Fixed</span></span>

- <span data-ttu-id="d707b-1120">Устранена проблема, которая препятствовала созданию WSL учетными записями пользователей с помощью имен пользователей NT, которые содержат пробелы или кавычки.</span><span class="sxs-lookup"><span data-stu-id="d707b-1120">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="d707b-1121">Изменить VolFs и DrvFs возвращает значение 0 для каталога подсчет ссылок в stat</span><span class="sxs-lookup"><span data-stu-id="d707b-1121">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="d707b-1122">Поддерживает параметр сокета IPV6_MULTICAST_HOPS.</span><span class="sxs-lookup"><span data-stu-id="d707b-1122">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="d707b-1123">Только для одной консоли цикл ввода/вывода на tty.</span><span class="sxs-lookup"><span data-stu-id="d707b-1123">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="d707b-1124">Пример: возможна следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d707b-1124">Example: the following command is possible:</span></span>
  - <span data-ttu-id="d707b-1125">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span><span class="sxs-lookup"><span data-stu-id="d707b-1125">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="d707b-1126">Замените пробелы с вкладками в /proc/cpuinfo (GH #1115)</span><span class="sxs-lookup"><span data-stu-id="d707b-1126">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="d707b-1127">DrvFs теперь отображается в mountinfo с именем, соответствующим подключенного тома Windows</span><span class="sxs-lookup"><span data-stu-id="d707b-1127">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="d707b-1128">/ Home и/root, теперь отображаются в mountinfo с правильные имена</span><span class="sxs-lookup"><span data-stu-id="d707b-1128">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="d707b-1129">Дополнительных исправлений и улучшений</span><span class="sxs-lookup"><span data-stu-id="d707b-1129">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-1130">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-1130">LTP Results:</span></span>
<span data-ttu-id="d707b-1131">Число пройденный тест: 665</span><span class="sxs-lookup"><span data-stu-id="d707b-1131">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="d707b-1132">Число с отрицательным (сбой, пропущенных и т. д...): 263</span><span class="sxs-lookup"><span data-stu-id="d707b-1132">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="d707b-1133">LTP тестовый запуск журналы</span><span class="sxs-lookup"><span data-stu-id="d707b-1133">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="d707b-1134">Сборки 14942</span><span class="sxs-lookup"><span data-stu-id="d707b-1134">Build 14942</span></span>

<span data-ttu-id="d707b-1135">Windows, общие сведения о сборке 14942 см. в статье [блог Windows](https://aka.ms/onefourninefourtwoooooo).</span><span class="sxs-lookup"><span data-stu-id="d707b-1135">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-1136">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-1136">Fixed</span></span>

- <span data-ttu-id="d707b-1137">Количество ошибок решает, включая «ПОПЫТКИ ВЫПОЛНЕНИЯ NOEXECUTE памяти» сети аварийного завершения, который блокирует SSH</span><span class="sxs-lookup"><span data-stu-id="d707b-1137">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="d707b-1138">Поддержка inotifiy для уведомления, создаваемые из приложений Windows на DrvFs теперь доступна в</span><span class="sxs-lookup"><span data-stu-id="d707b-1138">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="d707b-1139">Реализуйте TCP_KEEPIDLE и TCP_KEEPINTVL mongod.</span><span class="sxs-lookup"><span data-stu-id="d707b-1139">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="d707b-1140">(GH #695)</span><span class="sxs-lookup"><span data-stu-id="d707b-1140">(GH #695)</span></span>
- <span data-ttu-id="d707b-1141">Реализуйте pivot_root системный вызов</span><span class="sxs-lookup"><span data-stu-id="d707b-1141">Implement the pivot_root system call</span></span>
- <span data-ttu-id="d707b-1142">Реализовать параметр сокета для SO_DONTROUTE</span><span class="sxs-lookup"><span data-stu-id="d707b-1142">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="d707b-1143">Дополнительных исправлений и улучшений</span><span class="sxs-lookup"><span data-stu-id="d707b-1143">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="d707b-1144">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-1144">LTP Results:</span></span>
<span data-ttu-id="d707b-1145">Число пройденный тест: 665</span><span class="sxs-lookup"><span data-stu-id="d707b-1145">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="d707b-1146">Число с отрицательным (сбой, пропущенных и т. д...): 263</span><span class="sxs-lookup"><span data-stu-id="d707b-1146">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="d707b-1147">LTP тестовый запуск журналы</span><span class="sxs-lookup"><span data-stu-id="d707b-1147">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="d707b-1148">Поддержка syscall</span><span class="sxs-lookup"><span data-stu-id="d707b-1148">Syscall Support</span></span>
<span data-ttu-id="d707b-1149">Ниже приведен список новых или улучшенных syscalls, которая содержит некоторые реализации в WSL.</span><span class="sxs-lookup"><span data-stu-id="d707b-1149">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="d707b-1150">В сценарии по крайней мере один поддерживаются syscalls в этом списке, но может не иметь все параметры, поддерживаемые в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="d707b-1150">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="d707b-1151">Сборки 14936</span><span class="sxs-lookup"><span data-stu-id="d707b-1151">Build 14936</span></span>

<span data-ttu-id="d707b-1152">Windows, общие сведения о сборке 14936 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="d707b-1152">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="d707b-1153">Примечание. WSL установит Ubuntu версии 16.04 (Xenial) вместо Ubuntu 14.04 (верный) в следующих выпусках.</span><span class="sxs-lookup"><span data-stu-id="d707b-1153">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="d707b-1154">Это изменение будет применено участникам программы предварительной оценки, установки новых экземпляров (/ Install / lxrun.exe или первом запуске bash.exe).</span><span class="sxs-lookup"><span data-stu-id="d707b-1154">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="d707b-1155">Существующие экземпляры с верный не обновляется автоматически.</span><span class="sxs-lookup"><span data-stu-id="d707b-1155">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="d707b-1156">Пользователи могут обновить их надежных образа до Xenial, с помощью команды — выпуск обновление.</span><span class="sxs-lookup"><span data-stu-id="d707b-1156">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="d707b-1157">Известная проблема</span><span class="sxs-lookup"><span data-stu-id="d707b-1157">Known Issue</span></span>
<span data-ttu-id="d707b-1158">WSL возникла проблема с некоторые реализации сокета.</span><span class="sxs-lookup"><span data-stu-id="d707b-1158">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="d707b-1159">Отладка проявляется как сбой с ошибкой «ПОПЫТКА ВЫПОЛНЕНИЯ NOEXECUTE памяти».</span><span class="sxs-lookup"><span data-stu-id="d707b-1159">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="d707b-1160">Наиболее распространенной реализацией этой проблемы при сбое с помощью ssh.</span><span class="sxs-lookup"><span data-stu-id="d707b-1160">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="d707b-1161">Основной причиной фиксируется на внутренние сборки и будут отправляться при первой возможности участникам программы предварительной оценки.</span><span class="sxs-lookup"><span data-stu-id="d707b-1161">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="d707b-1162">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-1162">Fixed</span></span>

- <span data-ttu-id="d707b-1163">Реализации chroot системный вызов</span><span class="sxs-lookup"><span data-stu-id="d707b-1163">Implemented the chroot system call</span></span>
- <span data-ttu-id="d707b-1164">Улучшения в inotify ~~включая поддержку уведомлений, созданных из приложений Windows на DrvFs~~</span><span class="sxs-lookup"><span data-stu-id="d707b-1164">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="d707b-1165">Исправление: Для изменения, полученные из приложений Windows, не доступных в настоящее время поддерживает Inotify.</span><span class="sxs-lookup"><span data-stu-id="d707b-1165">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="d707b-1166">Сокета привязки на IPV6::<port n> теперь поддерживает IPV6_V6ONLY (GH #68, #157, #393, #460, #674, #740, #982, #996)</span><span class="sxs-lookup"><span data-stu-id="d707b-1166">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="d707b-1167">Поведение WNOWAIT для waitid systemcall реализуется (GH #638)</span><span class="sxs-lookup"><span data-stu-id="d707b-1167">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="d707b-1168">Поддержка параметров IP-адрес сокета IP_HDRINCL и IP_TTL</span><span class="sxs-lookup"><span data-stu-id="d707b-1168">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="d707b-1169">Немедленный возврат read() нулевой длины (GH #975)</span><span class="sxs-lookup"><span data-stu-id="d707b-1169">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="d707b-1170">Правильно обрабатывать имена файлов и имя файла префиксы, которые не содержат завершающий нуль-символ в tar-файл.</span><span class="sxs-lookup"><span data-stu-id="d707b-1170">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="d707b-1171">Поддержка epoll для/dev/NULL</span><span class="sxs-lookup"><span data-stu-id="d707b-1171">epoll support for /dev/null</span></span>
- <span data-ttu-id="d707b-1172">Исправьте источник времени /dev/alarm</span><span class="sxs-lookup"><span data-stu-id="d707b-1172">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="d707b-1173">Bash -c, теперь могут перенаправить в файл</span><span class="sxs-lookup"><span data-stu-id="d707b-1173">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="d707b-1174">Дополнительных исправлений и улучшений</span><span class="sxs-lookup"><span data-stu-id="d707b-1174">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-1175">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-1175">LTP Results:</span></span>
<span data-ttu-id="d707b-1176">Число пройденный тест: 664</span><span class="sxs-lookup"><span data-stu-id="d707b-1176">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="d707b-1177">Число с отрицательным (сбой, пропущенных и т. д...): 264</span><span class="sxs-lookup"><span data-stu-id="d707b-1177">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="d707b-1178">LTP тестовый запуск журналы</span><span class="sxs-lookup"><span data-stu-id="d707b-1178">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="d707b-1179">Поддержка syscall</span><span class="sxs-lookup"><span data-stu-id="d707b-1179">Syscall Support</span></span>
<span data-ttu-id="d707b-1180">Ниже приведен список новых или улучшенных syscalls, которая содержит некоторые реализации в WSL.</span><span class="sxs-lookup"><span data-stu-id="d707b-1180">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="d707b-1181">В сценарии по крайней мере один поддерживаются syscalls в этом списке, но может не иметь все параметры, поддерживаемые в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="d707b-1181">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="d707b-1182">Сборки 14931</span><span class="sxs-lookup"><span data-stu-id="d707b-1182">Build 14931</span></span>

<span data-ttu-id="d707b-1183">Windows, общие сведения о сборке 14931 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="d707b-1183">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-1184">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-1184">Fixed</span></span>

 - <span data-ttu-id="d707b-1185">Из-за обстоятельств, помимо наш элемент управления нет обновлений, в этой сборке для подсистемы Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="d707b-1185">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="d707b-1186">В следующем выпуске будет возобновлена регулярно запланированных обновлений.</span><span class="sxs-lookup"><span data-stu-id="d707b-1186">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="d707b-1187">Сборки 14926</span><span class="sxs-lookup"><span data-stu-id="d707b-1187">Build 14926</span></span>

<span data-ttu-id="d707b-1188">Windows, общие сведения о сборке 14926 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="d707b-1188">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-1189">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-1189">Fixed</span></span>

- <span data-ttu-id="d707b-1190">Проверка связи, теперь работает в консоли, которые не имеют права администратора</span><span class="sxs-lookup"><span data-stu-id="d707b-1190">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="d707b-1191">Ping6, теперь поддерживается, также без прав администратора</span><span class="sxs-lookup"><span data-stu-id="d707b-1191">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="d707b-1192">Поддержка Inotify файлы изменены с помощью WSL.</span><span class="sxs-lookup"><span data-stu-id="d707b-1192">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="d707b-1193">(GH #216)</span><span class="sxs-lookup"><span data-stu-id="d707b-1193">(GH #216)</span></span>
  - <span data-ttu-id="d707b-1194">Флаги, которые поддерживаются:</span><span class="sxs-lookup"><span data-stu-id="d707b-1194">Flags supported:</span></span>
    - <span data-ttu-id="d707b-1195">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="d707b-1195">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="d707b-1196">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="d707b-1196">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="d707b-1197">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="d707b-1197">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="d707b-1198">Прочитайте выходные данные: LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="d707b-1198">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="d707b-1199">Известные проблемы: Изменение файлов из приложений Windows создает события</span><span class="sxs-lookup"><span data-stu-id="d707b-1199">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="d707b-1200">Сокет UNIX теперь поддерживает SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="d707b-1200">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d707b-1201">LTP результаты:</span><span class="sxs-lookup"><span data-stu-id="d707b-1201">LTP Results:</span></span>
<span data-ttu-id="d707b-1202">Число пройденный тест: 651</span><span class="sxs-lookup"><span data-stu-id="d707b-1202">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="d707b-1203">Число с отрицательным (сбой, пропущенных и т. д...): 258</span><span class="sxs-lookup"><span data-stu-id="d707b-1203">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="d707b-1204">LTP тестовый запуск журналы</span><span class="sxs-lookup"><span data-stu-id="d707b-1204">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="d707b-1205">Сборки 14915</span><span class="sxs-lookup"><span data-stu-id="d707b-1205">Build 14915</span></span>

<span data-ttu-id="d707b-1206">Windows, общие сведения о сборке 14915 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="d707b-1206">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-1207">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-1207">Fixed</span></span>
-  <span data-ttu-id="d707b-1208">Socketpair для unix. сокеты датаграмм (GH #262)</span><span class="sxs-lookup"><span data-stu-id="d707b-1208">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="d707b-1209">Поддержка SO_REUSEADDR сокет UNIX</span><span class="sxs-lookup"><span data-stu-id="d707b-1209">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="d707b-1210">Поддержка сокет UNIX для SO_BROADCAST (GH #568)</span><span class="sxs-lookup"><span data-stu-id="d707b-1210">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="d707b-1211">Поддержка сокет UNIX для SOCK_SEQPACKET (GH #758, #546)</span><span class="sxs-lookup"><span data-stu-id="d707b-1211">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="d707b-1212">Добавление поддержки для сокета датаграмм unix при отправке, получаемого сообщения и завершение работы</span><span class="sxs-lookup"><span data-stu-id="d707b-1212">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="d707b-1213">Устранения критической ошибки из-за недопустимый mmap проверка параметров для съемном адресов.</span><span class="sxs-lookup"><span data-stu-id="d707b-1213">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="d707b-1214">(GH #847)</span><span class="sxs-lookup"><span data-stu-id="d707b-1214">(GH #847)</span></span>
- <span data-ttu-id="d707b-1215">Поддержка suspend / resume терминалов состояний</span><span class="sxs-lookup"><span data-stu-id="d707b-1215">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="d707b-1216">Поддержка ioctl TIOCPKT разблокировать экран программы (GH #774)</span><span class="sxs-lookup"><span data-stu-id="d707b-1216">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="d707b-1217">Известные проблемы: Функциональные клавиши не работает</span><span class="sxs-lookup"><span data-stu-id="d707b-1217">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="d707b-1218">Исправлено состояние гонки при TimerFd, которая могла привести к освобожденные член «ReaderReady», к которым осуществляется LxpTimerFdWorkerRoutine (GH #814)</span><span class="sxs-lookup"><span data-stu-id="d707b-1218">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="d707b-1219">Включить поддержку вызова перезапуска системы для futex опроса и clock_nanosleep</span><span class="sxs-lookup"><span data-stu-id="d707b-1219">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="d707b-1220">Добавлены привязки поддержкой подключения</span><span class="sxs-lookup"><span data-stu-id="d707b-1220">Added bind mount support</span></span>
- <span data-ttu-id="d707b-1221">Отмена общего доступа для поддержки подключения пространства имен</span><span class="sxs-lookup"><span data-stu-id="d707b-1221">unshare for mount namespace support</span></span>
    - <span data-ttu-id="d707b-1222">Известные проблемы: При создании нового пространства имен подключения с `unshare(CLONE_NEWNS)` текущий рабочий каталог будут по-прежнему указывать старого пространства имен</span><span class="sxs-lookup"><span data-stu-id="d707b-1222">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="d707b-1223">Дополнительные улучшения и исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="d707b-1223">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="d707b-1224">Сборки 14905</span><span class="sxs-lookup"><span data-stu-id="d707b-1224">Build 14905</span></span>

<span data-ttu-id="d707b-1225">Windows, общие сведения о сборке 14905 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span><span class="sxs-lookup"><span data-stu-id="d707b-1225">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-1226">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-1226">Fixed</span></span>
- <span data-ttu-id="d707b-1227">Возможность перезапуска системы, которую вызывает стали поддерживается (GH #349, GH #520)</span><span class="sxs-lookup"><span data-stu-id="d707b-1227">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="d707b-1228">Символических ссылок для конца в / теперь рабочие каталоги (GH #650)</span><span class="sxs-lookup"><span data-stu-id="d707b-1228">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="d707b-1229">Реализованный RNDGETENTCNT ioctl для/dev/Random</span><span class="sxs-lookup"><span data-stu-id="d707b-1229">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="d707b-1230">Реализации /proc/ [pid] / Подключает /proc/ [pid] / mountinfo и /proc/ [pid] / mountstats файлов</span><span class="sxs-lookup"><span data-stu-id="d707b-1230">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="d707b-1231">Дополнительных исправлений и улучшений</span><span class="sxs-lookup"><span data-stu-id="d707b-1231">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="d707b-1232">Сборки 14901</span><span class="sxs-lookup"><span data-stu-id="d707b-1232">Build 14901</span></span>
<span data-ttu-id="d707b-1233">Первый Insider сборку для post выпуска Windows 10 Anniversary Update.</span><span class="sxs-lookup"><span data-stu-id="d707b-1233">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="d707b-1234">Windows, общие сведения о сборке 14901 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="d707b-1234">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-1235">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-1235">Fixed</span></span>
- <span data-ttu-id="d707b-1236">Исправлена проблема конечные косой черты</span><span class="sxs-lookup"><span data-stu-id="d707b-1236">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="d707b-1237">Команды, такие как `$ mv a/c/ a/b/` теперь работать</span><span class="sxs-lookup"><span data-stu-id="d707b-1237">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="d707b-1238">Установка теперь запрашивает, если языковой стандарт Ubuntu должно быть присвоено языковой стандарт Windows</span><span class="sxs-lookup"><span data-stu-id="d707b-1238">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="d707b-1239">Procfs поддержка папку ns</span><span class="sxs-lookup"><span data-stu-id="d707b-1239">Procfs support for ns folder</span></span>
- <span data-ttu-id="d707b-1240">Добавлены подключения и отключения tmpfs, procfs и sysfs файловых систем</span><span class="sxs-lookup"><span data-stu-id="d707b-1240">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="d707b-1241">Исправить mknod [32-разрядных ABI подписи at]</span><span class="sxs-lookup"><span data-stu-id="d707b-1241">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="d707b-1242">Переместить сокеты UNIX для отправки модели</span><span class="sxs-lookup"><span data-stu-id="d707b-1242">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="d707b-1243">Следует учитывать размер INET сокета recv буфера, на наборе с помощью setsockopt</span><span class="sxs-lookup"><span data-stu-id="d707b-1243">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="d707b-1244">Сокет MSG_CMSG_CLOEXEC unix реализуйте получать сообщения флаг</span><span class="sxs-lookup"><span data-stu-id="d707b-1244">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="d707b-1245">Перенаправление stdin и stdout канала процесс Linux (GH #2)</span><span class="sxs-lookup"><span data-stu-id="d707b-1245">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="d707b-1246">Позволяет конвейерная передача - c команд bash в CMD.</span><span class="sxs-lookup"><span data-stu-id="d707b-1246">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="d707b-1247">Пример: > dir | bash -c «grep foo»</span><span class="sxs-lookup"><span data-stu-id="d707b-1247">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="d707b-1248">Bash теперь можно устанавливать в системах с нескольких файлов подкачки (GH #538, #358)</span><span class="sxs-lookup"><span data-stu-id="d707b-1248">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="d707b-1249">Размер буфера по умолчанию INET сокета должно совпадать с таковым Ubuntu установки по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d707b-1249">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="d707b-1250">Выровнять syscalls xattr для listxattr</span><span class="sxs-lookup"><span data-stu-id="d707b-1250">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="d707b-1251">Возвращать только интерфейсы с допустимым IPv4-адресом из SIOCGIFCONF</span><span class="sxs-lookup"><span data-stu-id="d707b-1251">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="d707b-1252">Исправить действие по умолчанию сигнала при введенному ptrace</span><span class="sxs-lookup"><span data-stu-id="d707b-1252">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="d707b-1253">implement /proc/sys/vm/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="d707b-1253">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="d707b-1254">Используйте значения регистра контекста машины при восстановлении контекста в sigreturn</span><span class="sxs-lookup"><span data-stu-id="d707b-1254">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="d707b-1255">Это устраняет проблему, где висячей java и javac для некоторых пользователей</span><span class="sxs-lookup"><span data-stu-id="d707b-1255">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="d707b-1256">Реализовать /proc/sys/kernel/hostname</span><span class="sxs-lookup"><span data-stu-id="d707b-1256">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="d707b-1257">Поддержка syscall</span><span class="sxs-lookup"><span data-stu-id="d707b-1257">Syscall Support</span></span>
<span data-ttu-id="d707b-1258">Ниже приведен список новых или улучшенных syscalls, которая содержит некоторые реализации в WSL.</span><span class="sxs-lookup"><span data-stu-id="d707b-1258">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="d707b-1259">В сценарии по крайней мере один поддерживаются syscalls в этом списке, но может не иметь все параметры, поддерживаемые в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="d707b-1259">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="d707b-1260">Построение 14388 до Юбилейного обновления Windows 10</span><span class="sxs-lookup"><span data-stu-id="d707b-1260">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="d707b-1261">Windows, общие сведения о сборке 14388 см. в статье [блог Windows](https://aka.ms/14388wip).</span><span class="sxs-lookup"><span data-stu-id="d707b-1261">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="d707b-1262">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-1262">Fixed</span></span>
- <span data-ttu-id="d707b-1263">Исправления для подготовки к Юбилейное обновление Windows 10 на 8/2</span><span class="sxs-lookup"><span data-stu-id="d707b-1263">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="d707b-1264">Дополнительные сведения о WSL в юбилейном обновлении можно найти на нашем [блог](https://blogs.msdn.microsoft.com/wsl/)</span><span class="sxs-lookup"><span data-stu-id="d707b-1264">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="d707b-1265">Сборки 14376</span><span class="sxs-lookup"><span data-stu-id="d707b-1265">Build 14376</span></span>
<span data-ttu-id="d707b-1266">Windows, общие сведения о сборке 14376 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="d707b-1266">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="d707b-1267">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-1267">Fixed</span></span>
- <span data-ttu-id="d707b-1268">Удалены некоторые экземпляры, где apt-get перестает отвечать на запросы (GH #493)</span><span class="sxs-lookup"><span data-stu-id="d707b-1268">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="d707b-1269">Устранена проблема, где пустой подключение не обрабатывались правильно</span><span class="sxs-lookup"><span data-stu-id="d707b-1269">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="d707b-1270">Исправлена проблема, при котором ramdisks не подключены правильно</span><span class="sxs-lookup"><span data-stu-id="d707b-1270">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="d707b-1271">Принятие сокета unix изменения для поддержки флаги (частичное 451 GH #)</span><span class="sxs-lookup"><span data-stu-id="d707b-1271">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="d707b-1272">Синий экран, связанные с предопределенной общей сети</span><span class="sxs-lookup"><span data-stu-id="d707b-1272">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="d707b-1273">Исправлена синий экран при доступе к /proc/ [pid] / task (GH #523)</span><span class="sxs-lookup"><span data-stu-id="d707b-1273">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="d707b-1274">Фиксированный высокая загрузка ЦП для некоторых сценариев pty (GH #488, #504)</span><span class="sxs-lookup"><span data-stu-id="d707b-1274">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="d707b-1275">Дополнительных исправлений и улучшений</span><span class="sxs-lookup"><span data-stu-id="d707b-1275">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="d707b-1276">Сборки 14371</span><span class="sxs-lookup"><span data-stu-id="d707b-1276">Build 14371</span></span>
<span data-ttu-id="d707b-1277">Windows, общие сведения о сборке 14371 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="d707b-1277">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="d707b-1278">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-1278">Fixed</span></span>
- <span data-ttu-id="d707b-1279">Исправлен конфликт синхронизации с SIGCHLD и wait() при использовании ptrace</span><span class="sxs-lookup"><span data-stu-id="d707b-1279">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="d707b-1280">Исправлены некоторые поведения при пути содержится знак / (GH #432)</span><span class="sxs-lookup"><span data-stu-id="d707b-1280">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="d707b-1281">Устранена проблема с переименования/удаления связи сбой из-за открытых дескрипторов к дочерним элементам</span><span class="sxs-lookup"><span data-stu-id="d707b-1281">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="d707b-1282">Дополнительных исправлений и улучшений</span><span class="sxs-lookup"><span data-stu-id="d707b-1282">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="d707b-1283">Сборки 14366</span><span class="sxs-lookup"><span data-stu-id="d707b-1283">Build 14366</span></span>
<span data-ttu-id="d707b-1284">Windows, общие сведения о сборке 14366 см. в статье [блог Windows](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span><span class="sxs-lookup"><span data-stu-id="d707b-1284">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="d707b-1285">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-1285">Fixed</span></span>
- <span data-ttu-id="d707b-1286">Исправление в создания файла через символических ссылок</span><span class="sxs-lookup"><span data-stu-id="d707b-1286">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="d707b-1287">Добавлена listxattr для Python (GH 385)</span><span class="sxs-lookup"><span data-stu-id="d707b-1287">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="d707b-1288">Дополнительных исправлений и улучшений</span><span class="sxs-lookup"><span data-stu-id="d707b-1288">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="d707b-1289">Поддержка syscall</span><span class="sxs-lookup"><span data-stu-id="d707b-1289">Syscall Support</span></span>
-   <span data-ttu-id="d707b-1290">Ниже приведен список новых или улучшенных syscalls, которая содержит некоторые реализации в WSL.</span><span class="sxs-lookup"><span data-stu-id="d707b-1290">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="d707b-1291">В сценарии по крайней мере один поддерживаются syscalls в этом списке, но может не иметь все параметры, поддерживаемые в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="d707b-1291">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="d707b-1292">Сборки 14361</span><span class="sxs-lookup"><span data-stu-id="d707b-1292">Build 14361</span></span>
<span data-ttu-id="d707b-1293">Для Windows, общие сведения о сборке 14361, при посетите [блог Windows](https://aka.ms/wip14361).</span><span class="sxs-lookup"><span data-stu-id="d707b-1293">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="d707b-1294">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-1294">Fixed</span></span>
- <span data-ttu-id="d707b-1295">DrvFs теперь учитывается регистр символов, при выполнении в Bash на Ubuntu в Windows.</span><span class="sxs-lookup"><span data-stu-id="d707b-1295">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="d707b-1296">Пользователи case.txt мая и регистр. Диски типа TXT на их/mnt/c</span><span class="sxs-lookup"><span data-stu-id="d707b-1296">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="d707b-1297">Чувствительность к регистру поддерживается только в пределах Bash на Ubuntu в Windows.</span><span class="sxs-lookup"><span data-stu-id="d707b-1297">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="d707b-1298">При внешней Bash NTFS сообщит файлы правильно, но может наблюдаться неожиданное поведение, взаимодействия с файлами Windows.</span><span class="sxs-lookup"><span data-stu-id="d707b-1298">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="d707b-1299">Корневой каталог каждого тома (т. е. /mnt/c) выполняется без учета регистра</span><span class="sxs-lookup"><span data-stu-id="d707b-1299">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="d707b-1300">Дополнительные сведения об обработке этих файлов в Windows можно найти [здесь](https://support.microsoft.com/en-us/kb/100625).</span><span class="sxs-lookup"><span data-stu-id="d707b-1300">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="d707b-1301">Значительно улучшено pty / tty поддержки.</span><span class="sxs-lookup"><span data-stu-id="d707b-1301">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="d707b-1302">Приложений, таких как TMUX теперь поддерживается (GH #40)</span><span class="sxs-lookup"><span data-stu-id="d707b-1302">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="d707b-1303">Установка основных проблемы, где не всегда создать учетные записи пользователей</span><span class="sxs-lookup"><span data-stu-id="d707b-1303">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="d707b-1304">Оптимизировать структуру arg командной строки, позволяя список аргументов слишком длинный.</span><span class="sxs-lookup"><span data-stu-id="d707b-1304">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="d707b-1305">(GH #153)</span><span class="sxs-lookup"><span data-stu-id="d707b-1305">(GH #153)</span></span>
- <span data-ttu-id="d707b-1306">Теперь возможность удаления и chmod read_only файлов из DrvFs</span><span class="sxs-lookup"><span data-stu-id="d707b-1306">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="d707b-1307">Исправлены некоторые экземпляры, где терминалов зависает на отключение (GH #43)</span><span class="sxs-lookup"><span data-stu-id="d707b-1307">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="d707b-1308">chmod и сменить теперь работать на устройствах tty</span><span class="sxs-lookup"><span data-stu-id="d707b-1308">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="d707b-1309">Разрешить подключение к 0.0.0.0 и:: как localhost (GH № 388)</span><span class="sxs-lookup"><span data-stu-id="d707b-1309">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="d707b-1310">Длина вектора операций ввода-ВЫВОДА обрабатывают Sendmsg/recvmsg > 1 (частичное 376 GH #)</span><span class="sxs-lookup"><span data-stu-id="d707b-1310">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="d707b-1311">Пользователи могут теперь отказаться от узлов автоматически созданный файл (GH #398)</span><span class="sxs-lookup"><span data-stu-id="d707b-1311">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="d707b-1312">Автоматический подбор Linux языкового стандарта, языковой стандарт NT во время установки (GH 11)</span><span class="sxs-lookup"><span data-stu-id="d707b-1312">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="d707b-1313">Добавлен файл /proc/sys/vm/swappiness (GH #306)</span><span class="sxs-lookup"><span data-stu-id="d707b-1313">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="d707b-1314">помощью strace теперь обеспечивает правильное завершение</span><span class="sxs-lookup"><span data-stu-id="d707b-1314">strace now exits correctly</span></span>
- <span data-ttu-id="d707b-1315">Разрешить каналы открыть повторно через /proc/self/fd (GH #222)</span><span class="sxs-lookup"><span data-stu-id="d707b-1315">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="d707b-1316">Скрыть каталогов в папке %LOCALAPPDATA%\lxss из DrvFs (GH #270)</span><span class="sxs-lookup"><span data-stu-id="d707b-1316">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="d707b-1317">Более эффективная обработка bash.exe ~.</span><span class="sxs-lookup"><span data-stu-id="d707b-1317">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="d707b-1318">Команды, такие как «bash ~ ls - c» теперь поддерживается (467 указано # GH)</span><span class="sxs-lookup"><span data-stu-id="d707b-1318">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="d707b-1319">Сокеты теперь уведомлять epoll чтения, доступные во время завершения работы (GH #271)</span><span class="sxs-lookup"><span data-stu-id="d707b-1319">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="d707b-1320">lxrun / uninstall лучше справляется удаления файлов и папок</span><span class="sxs-lookup"><span data-stu-id="d707b-1320">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="d707b-1321">Исправленный ps -f (# GH 246)</span><span class="sxs-lookup"><span data-stu-id="d707b-1321">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="d707b-1322">Улучшенная поддержка x11 приложениями, такими как xEmacs (GH № 481)</span><span class="sxs-lookup"><span data-stu-id="d707b-1322">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="d707b-1323">Обновить исходный поток размер стека для сопоставления по умолчанию Ubuntu и неправильно сообщает размер syscall get_rlimit (GH #172, #258)</span><span class="sxs-lookup"><span data-stu-id="d707b-1323">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="d707b-1324">Сведения об имена образов использованием процесса (например, для аудита)</span><span class="sxs-lookup"><span data-stu-id="d707b-1324">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="d707b-1325">Реализованный /proc/mountinfo для команды df</span><span class="sxs-lookup"><span data-stu-id="d707b-1325">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="d707b-1326">Код ошибки фиксированной символьной ссылки имени дочернего.</span><span class="sxs-lookup"><span data-stu-id="d707b-1326">Fixed symlink error code for child name .</span></span> <span data-ttu-id="d707b-1327">и...</span><span class="sxs-lookup"><span data-stu-id="d707b-1327">and ..</span></span>
- <span data-ttu-id="d707b-1328">Дополнительные улучшения исправлений и улучшений</span><span class="sxs-lookup"><span data-stu-id="d707b-1328">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="d707b-1329">Поддержка syscall</span><span class="sxs-lookup"><span data-stu-id="d707b-1329">Syscall Support</span></span>
<span data-ttu-id="d707b-1330">Ниже приведен список новых или улучшенных syscalls, которая содержит некоторые реализации в WSL.</span><span class="sxs-lookup"><span data-stu-id="d707b-1330">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="d707b-1331">В сценарии по крайней мере один поддерживаются syscalls в этом списке, но может не иметь все параметры, поддерживаемые в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="d707b-1331">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="d707b-1332">Начиная со сборки 14352</span><span class="sxs-lookup"><span data-stu-id="d707b-1332">Build 14352</span></span>
<span data-ttu-id="d707b-1333">Для Windows, общие сведения о сборки 14352 посетите [блог Windows](https://aka.ms/wip14352).</span><span class="sxs-lookup"><span data-stu-id="d707b-1333">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d707b-1334">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-1334">Fixed</span></span>
- <span data-ttu-id="d707b-1335">Устранена проблема, где большие файлы не были загружены / создан правильно.</span><span class="sxs-lookup"><span data-stu-id="d707b-1335">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="d707b-1336">Это следует разблокировать npm и других сценариев, (GH 3, GH #313)</span><span class="sxs-lookup"><span data-stu-id="d707b-1336">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="d707b-1337">Удалены некоторые экземпляры, где зависания сокетов</span><span class="sxs-lookup"><span data-stu-id="d707b-1337">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="d707b-1338">Исправлены некоторые ошибки ptrace</span><span class="sxs-lookup"><span data-stu-id="d707b-1338">Corrected some ptrace errors</span></span>
- <span data-ttu-id="d707b-1339">Устранена проблема с WSL, позволяя длиннее 255 символов в именах файлов</span><span class="sxs-lookup"><span data-stu-id="d707b-1339">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="d707b-1340">Улучшенная поддержка символы национальных алфавитов</span><span class="sxs-lookup"><span data-stu-id="d707b-1340">Improved support for non-English characters</span></span>
- <span data-ttu-id="d707b-1341">Добавьте текущие данные часового пояса Windows и по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d707b-1341">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="d707b-1342">Уникальный идентификатор для каждой точки подключения (исправлено jre-GH № 49)</span><span class="sxs-lookup"><span data-stu-id="d707b-1342">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="d707b-1343">Исправьте проблему с пути, содержащие «.»</span><span class="sxs-lookup"><span data-stu-id="d707b-1343">Correct issue with paths containing “.”</span></span> <span data-ttu-id="d707b-1344">и «..»</span><span class="sxs-lookup"><span data-stu-id="d707b-1344">and “..”</span></span>
- <span data-ttu-id="d707b-1345">Добавлена поддержка Fifo (GH #71)</span><span class="sxs-lookup"><span data-stu-id="d707b-1345">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="d707b-1346">Обновленный формат resolv.conf в соответствии с собственного формата Ubuntu</span><span class="sxs-lookup"><span data-stu-id="d707b-1346">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="d707b-1347">Очистка некоторых procfs</span><span class="sxs-lookup"><span data-stu-id="d707b-1347">Some procfs cleanup</span></span>
- <span data-ttu-id="d707b-1348">Включена проверка связи для консолей администрирования (GH 18)</span><span class="sxs-lookup"><span data-stu-id="d707b-1348">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="d707b-1349">Поддержка syscall</span><span class="sxs-lookup"><span data-stu-id="d707b-1349">Syscall Support</span></span>
<span data-ttu-id="d707b-1350">Ниже приведен список новых или улучшенных syscalls, которая содержит некоторые реализации в WSL.</span><span class="sxs-lookup"><span data-stu-id="d707b-1350">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="d707b-1351">В сценарии по крайней мере один поддерживаются syscalls в этом списке, но может не иметь все параметры, поддерживаемые в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="d707b-1351">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="d707b-1352">Сборки 14342</span><span class="sxs-lookup"><span data-stu-id="d707b-1352">Build 14342</span></span>
<span data-ttu-id="d707b-1353">Для Windows, общие сведения о сборки 14342 [блог Windows](https://aka.ms/wip14342).</span><span class="sxs-lookup"><span data-stu-id="d707b-1353">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="d707b-1354">Сведения о VolFs и DriveFs можно найти на [WSL блог](https://blogs.msdn.microsoft.com/wsl).</span><span class="sxs-lookup"><span data-stu-id="d707b-1354">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="d707b-1355">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-1355">Fixed</span></span>
- <span data-ttu-id="d707b-1356">Исправлена проблема с установкой, когда пользователь Windows имеет символов Юникода в имени пользователя</span><span class="sxs-lookup"><span data-stu-id="d707b-1356">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="d707b-1357">Инструкции по решению udev обновления apt-get в часто задаваемых вопросов теперь предоставляется по умолчанию при первом запуске</span><span class="sxs-lookup"><span data-stu-id="d707b-1357">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="d707b-1358">Включить символических ссылок в DriveFs (/mnt/<drive>) каталоги</span><span class="sxs-lookup"><span data-stu-id="d707b-1358">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="d707b-1359">Теперь работать символических ссылок между DriveFs и VolFs</span><span class="sxs-lookup"><span data-stu-id="d707b-1359">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="d707b-1360">Известные проблемы верхнего уровня пути, проблемы с синтаксическим: ls. / / Теперь будет работать должным образом</span><span class="sxs-lookup"><span data-stu-id="d707b-1360">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="d707b-1361">параметры -g теперь работу и установите npm на DriveFs</span><span class="sxs-lookup"><span data-stu-id="d707b-1361">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="d707b-1362">Исправлена проблема, предотвращая запуск сервера PHP</span><span class="sxs-lookup"><span data-stu-id="d707b-1362">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="d707b-1363">Параметры среды по умолчанию обновлен, например $PATH ближе сопоставляемое собственного Ubuntu</span><span class="sxs-lookup"><span data-stu-id="d707b-1363">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="d707b-1364">Добавлены еженедельные задачи обслуживания в Windows, чтобы обновить кэш пакетов apt</span><span class="sxs-lookup"><span data-stu-id="d707b-1364">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="d707b-1365">Исправлена проблема с проверкой заголовка ELF, WSL теперь поддерживает все параметры Melkor</span><span class="sxs-lookup"><span data-stu-id="d707b-1365">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="d707b-1366">Оболочка Zsh работает</span><span class="sxs-lookup"><span data-stu-id="d707b-1366">Zsh shell is functional</span></span>
- <span data-ttu-id="d707b-1367">Теперь поддерживаются предкомпилированные двоичные файлы Go</span><span class="sxs-lookup"><span data-stu-id="d707b-1367">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="d707b-1368">Подсказки для первого запуска Bash.exe теперь локализован правильно</span><span class="sxs-lookup"><span data-stu-id="d707b-1368">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="d707b-1369">/proc/meminfo теперь возвращает правильные сведения</span><span class="sxs-lookup"><span data-stu-id="d707b-1369">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="d707b-1370">Сокеты, теперь поддерживается в VFS</span><span class="sxs-lookup"><span data-stu-id="d707b-1370">Sockets now supported in VFS</span></span>
- <span data-ttu-id="d707b-1371">/ dev. теперь подключен как tempfs</span><span class="sxs-lookup"><span data-stu-id="d707b-1371">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="d707b-1372">Теперь поддерживается FIFO</span><span class="sxs-lookup"><span data-stu-id="d707b-1372">Fifo now supported</span></span>
- <span data-ttu-id="d707b-1373">Теперь отображается правильно в параметр cpuinfo/proc/многоядерных системах</span><span class="sxs-lookup"><span data-stu-id="d707b-1373">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="d707b-1374">Дополнительные улучшения и сообщения об ошибках, загрузки во время первого запуска</span><span class="sxs-lookup"><span data-stu-id="d707b-1374">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="d707b-1375">Syscall улучшений и исправлений.</span><span class="sxs-lookup"><span data-stu-id="d707b-1375">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="d707b-1376">Список поддерживаемых syscall ниже.</span><span class="sxs-lookup"><span data-stu-id="d707b-1376">Supported syscall list below.</span></span>
- <span data-ttu-id="d707b-1377">Дополнительных исправлений и улучшений</span><span class="sxs-lookup"><span data-stu-id="d707b-1377">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="d707b-1378">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="d707b-1378">Known Issues</span></span>
- <span data-ttu-id="d707b-1379">Не удается разрешить ".."</span><span class="sxs-lookup"><span data-stu-id="d707b-1379">Not resolving ‘..’</span></span> <span data-ttu-id="d707b-1380">неправильно на DriveFs в некоторых случаях</span><span class="sxs-lookup"><span data-stu-id="d707b-1380">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="d707b-1381">Поддержка syscall</span><span class="sxs-lookup"><span data-stu-id="d707b-1381">Syscall Support</span></span>
<span data-ttu-id="d707b-1382">Ниже приведен список новых или улучшенных syscalls, которая содержит некоторые реализации в WSL.</span><span class="sxs-lookup"><span data-stu-id="d707b-1382">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="d707b-1383">В сценарии по крайней мере один поддерживаются syscalls в этом списке, но может не иметь все параметры, поддерживаемые в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="d707b-1383">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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

## <a name="build-14332"></a><span data-ttu-id="d707b-1384">Сборки 14332</span><span class="sxs-lookup"><span data-stu-id="d707b-1384">Build 14332</span></span>

<span data-ttu-id="d707b-1385">Windows, общие сведения о сборке 14332 см. в статье [блог Windows](https://aka.ms/wip14332).</span><span class="sxs-lookup"><span data-stu-id="d707b-1385">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="d707b-1386">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-1386">Fixed</span></span>
- <span data-ttu-id="d707b-1387">Более эффективное создание resolv.conf, включая назначение приоритетов DNS-записей</span><span class="sxs-lookup"><span data-stu-id="d707b-1387">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="d707b-1388">Проблема с перемещение файлов и каталогов между/mnt и не- / mnt дисков</span><span class="sxs-lookup"><span data-stu-id="d707b-1388">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="d707b-1389">TAR-файлы теперь можно создать с помощью символических ссылок</span><span class="sxs-lookup"><span data-stu-id="d707b-1389">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="d707b-1390">Добавлено стандартное /run/lock каталог на создание экземпляра</span><span class="sxs-lookup"><span data-stu-id="d707b-1390">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="d707b-1391">Обновить/dev/NULL для возврата правильного stat info</span><span class="sxs-lookup"><span data-stu-id="d707b-1391">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="d707b-1392">Дополнительные ошибки при загрузке во время первого запуска</span><span class="sxs-lookup"><span data-stu-id="d707b-1392">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="d707b-1393">Syscall улучшений и исправлений.</span><span class="sxs-lookup"><span data-stu-id="d707b-1393">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="d707b-1394">Список поддерживаемых syscall ниже.</span><span class="sxs-lookup"><span data-stu-id="d707b-1394">Supported syscall list below.</span></span>
- <span data-ttu-id="d707b-1395">Дополнительные улучшения исправлений и улучшений</span><span class="sxs-lookup"><span data-stu-id="d707b-1395">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="d707b-1396">Поддержка syscall</span><span class="sxs-lookup"><span data-stu-id="d707b-1396">Syscall Support</span></span>
<span data-ttu-id="d707b-1397">Ниже приведен новый syscall, с некоторой реализации в WSL.</span><span class="sxs-lookup"><span data-stu-id="d707b-1397">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="d707b-1398">В по крайней мере один из сценариев поддерживается syscall в этом списке, но может не иметь все параметры, поддерживаемые в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="d707b-1398">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="d707b-1399">Сборка 14328</span><span class="sxs-lookup"><span data-stu-id="d707b-1399">Build 14328</span></span>

<span data-ttu-id="d707b-1400">Windows, общие сведения о сборке 14332 см. в статье [блог Windows](https://aka.ms/wip14328).</span><span class="sxs-lookup"><span data-stu-id="d707b-1400">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="d707b-1401">Новые возможности</span><span class="sxs-lookup"><span data-stu-id="d707b-1401">New Features</span></span>
* <span data-ttu-id="d707b-1402">Теперь поддерживают пользователей Linux.</span><span class="sxs-lookup"><span data-stu-id="d707b-1402">Now support Linux users.</span></span>  <span data-ttu-id="d707b-1403">Установка Bash на Ubuntu в Windows выдаст запрос на создание пользователей Linux.</span><span class="sxs-lookup"><span data-stu-id="d707b-1403">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="d707b-1404">Дополнительные сведения см. в статье https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="d707b-1404">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="d707b-1405">Имя узла теперь присваивается имя компьютера Windows, не более @localhost</span><span class="sxs-lookup"><span data-stu-id="d707b-1405">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="d707b-1406">Дополнительные сведения о создания 14328, посетите: https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="d707b-1406">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="d707b-1407">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="d707b-1407">Fixed</span></span>
* <span data-ttu-id="d707b-1408">Усовершенствования символьную ссылку для не /mnt/<drive> файлов</span><span class="sxs-lookup"><span data-stu-id="d707b-1408">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="d707b-1409">npm Установка теперь работает</span><span class="sxs-lookup"><span data-stu-id="d707b-1409">npm install now works</span></span>
    * <span data-ttu-id="d707b-1410">JDK / jre теперь устанавливаемые с помощью инструкций, приведенных [здесь](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span><span class="sxs-lookup"><span data-stu-id="d707b-1410">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="d707b-1411">Известная проблема: символических ссылок не работают для подключает Windows.</span><span class="sxs-lookup"><span data-stu-id="d707b-1411">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="d707b-1412">Функциональные возможности будут доступны при последующей сборке</span><span class="sxs-lookup"><span data-stu-id="d707b-1412">Functionality will be available in a later build</span></span>
* <span data-ttu-id="d707b-1413">Теперь отображается вверху и htop</span><span class="sxs-lookup"><span data-stu-id="d707b-1413">top and htop now display</span></span>
* <span data-ttu-id="d707b-1414">Сбои установки дополнительных сообщений об ошибках для некоторых</span><span class="sxs-lookup"><span data-stu-id="d707b-1414">Additional error messages for some install failures</span></span>
* <span data-ttu-id="d707b-1415">Syscall улучшений и исправлений.</span><span class="sxs-lookup"><span data-stu-id="d707b-1415">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="d707b-1416">Список поддерживаемых syscall ниже.</span><span class="sxs-lookup"><span data-stu-id="d707b-1416">Supported syscall list below.</span></span>
* <span data-ttu-id="d707b-1417">Дополнительные улучшения исправлений и улучшений</span><span class="sxs-lookup"><span data-stu-id="d707b-1417">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="d707b-1418">Поддержка syscall</span><span class="sxs-lookup"><span data-stu-id="d707b-1418">Syscall Support</span></span>
<span data-ttu-id="d707b-1419">Ниже приведен список syscalls, которая содержит некоторые реализации в WSL.</span><span class="sxs-lookup"><span data-stu-id="d707b-1419">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="d707b-1420">В сценарии по крайней мере один поддерживаются syscalls в этом списке, но может не иметь все параметры, поддерживаемые в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="d707b-1420">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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
