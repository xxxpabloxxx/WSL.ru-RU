---
title: Заметки о выпуске подсистемы Windows для Linux
description: Заметки о выпуске подсистемы Windows для Linux.  Обновляются еженедельно.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 9dfd4704eee537c053d874d6fcee47b70efbc33c
ms.sourcegitcommit: 212d3e0092dbc584a8422de47599a4ce46f0f016
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/11/2019
ms.locfileid: "70902416"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="b3232-105">Заметки о выпуске подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="b3232-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-18980"></a><span data-ttu-id="b3232-106">Сборка 18980</span><span class="sxs-lookup"><span data-stu-id="b3232-106">Build 18980</span></span>
<span data-ttu-id="b3232-107">Общие сведения о сборке Windows 18980 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span><span class="sxs-lookup"><span data-stu-id="b3232-107">For general Windows information on build 18980 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span></span>

* <span data-ttu-id="b3232-108">Исправлено чтение символических ссылок, которые запрещают FILE_READ_DATA.</span><span class="sxs-lookup"><span data-stu-id="b3232-108">Fix reading symlinks that deny FILE_READ_DATA.</span></span> <span data-ttu-id="b3232-109">Сюда входят все символические ссылки Windows, создаваемые для обеспечения обратной совместимости, такие как "C:\Document and Settings", а также множество символических ссылок в каталоге профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="b3232-109">This includes all the symlinks Windows creates for backwards compatibility such as "C:\Document and Settings" and a bunch of symlinks in the user profile directory</span></span>
* <span data-ttu-id="b3232-110">Непредвиденное состояние файловой системы перестало быть неустранимым [GH 4334, 4305].</span><span class="sxs-lookup"><span data-stu-id="b3232-110">Make unexpected filesystem state non-fatal [GH 4334, 4305]</span></span>
* <span data-ttu-id="b3232-111">[WSL2] Добавлена поддержка arm64, если ЦП или встроенное ПО поддерживает виртуализацию.</span><span class="sxs-lookup"><span data-stu-id="b3232-111">[WSL2] Add support for arm64 if your CPU / firmware supports virtualization</span></span>
* <span data-ttu-id="b3232-112">[WSL2] Непривилегированным пользователям разрешено просматривать журнал ядра.</span><span class="sxs-lookup"><span data-stu-id="b3232-112">[WSL2] Allow unprivileged users to view kernel log</span></span>
* <span data-ttu-id="b3232-113">[WSL2] Исправлена ретрансляция вывода при закрытии сокетов stdout и stderr [GH 4375].</span><span class="sxs-lookup"><span data-stu-id="b3232-113">[WSL2] Fix output relay when stdout / stderr sockets have been closed [GH 4375]</span></span>
* <span data-ttu-id="b3232-114">[WSL2] Поддержка сквозного режима батареи и адаптера питания.</span><span class="sxs-lookup"><span data-stu-id="b3232-114">[WSL2] Support battery and AC adapter passthrough</span></span>
* <span data-ttu-id="b3232-115">[WSL2] Ядро Linux обновлено до версии 4.19.67.</span><span class="sxs-lookup"><span data-stu-id="b3232-115">[WSL2] Update Linux kernel to 4.19.67</span></span>
* <span data-ttu-id="b3232-116">Добавлена возможность задать имя пользователя по умолчанию в /etc/wsl.conf:</span><span class="sxs-lookup"><span data-stu-id="b3232-116">Add the ability to set default username in /etc/wsl.conf:</span></span>
```
[user]
default=root
```

## <a name="build-18975"></a><span data-ttu-id="b3232-117">Сборка 18975</span><span class="sxs-lookup"><span data-stu-id="b3232-117">Build 18975</span></span>
<span data-ttu-id="b3232-118">Общие сведения о сборке Windows 18975 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span><span class="sxs-lookup"><span data-stu-id="b3232-118">For general Windows information on build 18975 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span></span>

* <span data-ttu-id="b3232-119">[WSL2] Исправлен ряд проблем с надежностью localhost [GH 4340].</span><span class="sxs-lookup"><span data-stu-id="b3232-119">[WSL2] Fixed a number of localhost reliability issues [GH 4340]</span></span>

## <a name="build-18970"></a><span data-ttu-id="b3232-120">Сборка 18970</span><span class="sxs-lookup"><span data-stu-id="b3232-120">Build 18970</span></span>
<span data-ttu-id="b3232-121">Общие сведения о сборке Windows 18970 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span><span class="sxs-lookup"><span data-stu-id="b3232-121">For general Windows information on build 18970 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span></span>

* <span data-ttu-id="b3232-122">[WSL2] Синхронизация времени с временем узла при выходе системы из спящего режима [GH 4245].</span><span class="sxs-lookup"><span data-stu-id="b3232-122">[WSL2] Sync time with host time when system resumes from sleep state [GH 4245]</span></span>
* <span data-ttu-id="b3232-123">[WSL2] Создание символических ссылок NT на тома Windows, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="b3232-123">[WSL2] Create NT symlinks on the Windows volumes when possible.</span></span>
* <span data-ttu-id="b3232-124">[WSL2] Создание дистрибутивов в пространствах имен UTS, IPC, PID и Mount.</span><span class="sxs-lookup"><span data-stu-id="b3232-124">[WSL2] Create distros in UTS, IPC, PID, and Mount namespaces.</span></span>
* <span data-ttu-id="b3232-125">[WSL2] Исправлена ретрансляция портов localhost при привязке сервера к localhost напрямую [GH 4353].</span><span class="sxs-lookup"><span data-stu-id="b3232-125">[WSL2] Fix localhost port relay when server binds to localhost directly [GH 4353]</span></span>
* <span data-ttu-id="b3232-126">[WSL2] Исправлено взаимодействие при перенаправлении вывода [GH 4337].</span><span class="sxs-lookup"><span data-stu-id="b3232-126">[WSL2] Fix interop when output is redirected [GH 4337]</span></span>
* <span data-ttu-id="b3232-127">[WSL2] Поддержка преобразования абсолютных символических ссылок NT.</span><span class="sxs-lookup"><span data-stu-id="b3232-127">[WSL2] Support translating absolute NT symlinks.</span></span>
* <span data-ttu-id="b3232-128">[WSL2] Ядро обновлено до версии 4.19.59.</span><span class="sxs-lookup"><span data-stu-id="b3232-128">[WSL2] Update kernel to 4.19.59</span></span>
* <span data-ttu-id="b3232-129">[WSL2] Правильное задание маски подсети для eth0.</span><span class="sxs-lookup"><span data-stu-id="b3232-129">[WSL2] Properly set subnet mask for eth0.</span></span>
* <span data-ttu-id="b3232-130">[WSL2] Изменение логики для выхода из циклов консольного рабочего процесса при получении сигнала о событии выхода.</span><span class="sxs-lookup"><span data-stu-id="b3232-130">[WSL2] Change logic to break out of console worker loop when exit event is signaled.</span></span>
* <span data-ttu-id="b3232-131">[WSL2] Если дистрибутив не работает, то его VHD-файл можно извлечь.</span><span class="sxs-lookup"><span data-stu-id="b3232-131">[WSL2] Eject distribution vhd when the distro is not running.</span></span>
* <span data-ttu-id="b3232-132">[WSL2] Исправлена библиотека анализа конфигурации, чтобы правильно обрабатывать пустые значения.</span><span class="sxs-lookup"><span data-stu-id="b3232-132">[WSL2] Fix config parsing library to correctly handle empty values.</span></span>
* <span data-ttu-id="b3232-133">[WSL2] Поддержка рабочего стола Docker путем создания подключений между дистрибутивами.</span><span class="sxs-lookup"><span data-stu-id="b3232-133">[WSL2] Support Docker Desktop by creating cross distro mounts.</span></span> <span data-ttu-id="b3232-134">Дистрибутив можно настроить для такого режима, добавив следующую строку в файл /etc/wsl.conf:</span><span class="sxs-lookup"><span data-stu-id="b3232-134">A distro can opt-in to this behavior by adding the following line to the /etc/wsl.conf file:</span></span>
```
[automount]
crossDistro = true
```

## <a name="build-18945"></a><span data-ttu-id="b3232-135">Сборка 18945</span><span class="sxs-lookup"><span data-stu-id="b3232-135">Build 18945</span></span>
<span data-ttu-id="b3232-136">Общие сведения о сборке Windows 18945 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span><span class="sxs-lookup"><span data-stu-id="b3232-136">For general Windows information on build 18945 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-137">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-137">WSL</span></span>
* <span data-ttu-id="b3232-138">[WSL2] Разрешен доступ к ожидающим передачи данных TCP-сокетам в WSL2 с узла по адресу localhost:<порт>.</span><span class="sxs-lookup"><span data-stu-id="b3232-138">[WSL2] Allow listening tcp sockets in WSL2 to be accessible from the host by using localhost:port</span></span>
* <span data-ttu-id="b3232-139">[WSL2] Устранены сбои при установке и преобразовании. Добавлена дополнительная диагностика для отслеживания будущих проблем [GH 4105].</span><span class="sxs-lookup"><span data-stu-id="b3232-139">[WSL2] Fixes for install / conversion failures and additional diagnostics to track down future issues [GH 4105]</span></span> 
* <span data-ttu-id="b3232-140">[WSL2] Улучшена диагностируемость проблем с сетью WSL2.</span><span class="sxs-lookup"><span data-stu-id="b3232-140">[WSL2] Improve diagnosability of WSL2 network issues</span></span>
* <span data-ttu-id="b3232-141">[WSL2] Ядро обновлено до версии 4.19.55.</span><span class="sxs-lookup"><span data-stu-id="b3232-141">[WSL2] Update kernel version to 4.19.55</span></span>
* <span data-ttu-id="b3232-142">[WSL2] Ядро обновлено с помощью параметров конфигурации, необходимых для Docker [GH 4165].</span><span class="sxs-lookup"><span data-stu-id="b3232-142">[WSL2] Update kernel with config options required for docker [GH 4165]</span></span>
* <span data-ttu-id="b3232-143">[WSL2] Увеличено число ЦП, назначаемых упрощенной служебной виртуальной машине, чтобы оно совпадало с числом ЦП узла (ранее это значение было ограничено 8 ЦП с помощью параметра CONFIG_NR_CPUS в конфигурации ядра) [GH 4137].</span><span class="sxs-lookup"><span data-stu-id="b3232-143">[WSL2] Increase the number of CPUs assigned to the lightweight utility VM to be the same as the host (was previously capped at 8 by CONFIG_NR_CPUS in the kernel config) [GH 4137]</span></span>
* <span data-ttu-id="b3232-144">[WSL2] Создание файла подкачки для упрощенной виртуальной машины WSL2.</span><span class="sxs-lookup"><span data-stu-id="b3232-144">[WSL2] Create a swap file for the WSL2 lightweight VM</span></span>
* <span data-ttu-id="b3232-145">[WSL2] Разрешено отображение подключений пользователей в \\\\wsl$\\<имя_дистрибутива> (например, sshfs) [GH 4172].</span><span class="sxs-lookup"><span data-stu-id="b3232-145">[WSL2] Allow user mounts to be visible via \\\\wsl$\\distro (for example sshfs) [GH 4172]</span></span>
* <span data-ttu-id="b3232-146">[WSL2] Повышена производительность файловой системы 9p.</span><span class="sxs-lookup"><span data-stu-id="b3232-146">[WSL2] Improve 9p filesystem performance</span></span>
* <span data-ttu-id="b3232-147">[WSL2] Предотвращение неограниченного роста списка ACL виртуального жесткого диска [GH 4126].</span><span class="sxs-lookup"><span data-stu-id="b3232-147">[WSL2] Ensure vhd ACL does not grow unbounded [GH 4126]</span></span>
* <span data-ttu-id="b3232-148">[WSL2] Обновлена конфигурации ядра для поддержки squashfs и xt_conntrack [GH 4107, 4123].</span><span class="sxs-lookup"><span data-stu-id="b3232-148">[WSL2] Update kernel config to support squashfs and xt_conntrack [GH 4107, 4123]</span></span>
* <span data-ttu-id="b3232-149">[WSL2] Исправлен параметр interop.enabled в /etc/wsl.conf [GH 4140].</span><span class="sxs-lookup"><span data-stu-id="b3232-149">[WSL2] Fix for interop.enabled /etc/wsl.conf option [GH 4140]</span></span>
* <span data-ttu-id="b3232-150">[WSL2] Если файловая система не поддерживает EA, возвращается ENOTSUP.</span><span class="sxs-lookup"><span data-stu-id="b3232-150">[WSL2] Return ENOTSUP if the file system does not support EAs</span></span>
* <span data-ttu-id="b3232-151">[WSL2] CopyFile больше не прекращает отвечать на запросы при работе с \\\\wsl$.</span><span class="sxs-lookup"><span data-stu-id="b3232-151">[WSL2] Fix CopyFile hang with \\\\wsl$</span></span>
* <span data-ttu-id="b3232-152">Параметр umask по умолчанию переключен на значение 0022, и добавлен параметр filesystem.umask в /etc/wsl.conf.</span><span class="sxs-lookup"><span data-stu-id="b3232-152">Switch default umask to 0022 and add filesystem.umask setting to /etc/wsl.conf</span></span>
* <span data-ttu-id="b3232-153">Исправлен wslpath, чтобы правильно разрешать символические ссылки, что повторно происходило в 19h1 [GH 4078].</span><span class="sxs-lookup"><span data-stu-id="b3232-153">Fix wslpath to properly resolve symlinks, this was regressed in 19h1 [GH 4078]</span></span>
* <span data-ttu-id="b3232-154">Введен файл %UserProfile%\\.wslconfig для настройки параметров WSL2.</span><span class="sxs-lookup"><span data-stu-id="b3232-154">Introduce %UserProfile%\\.wslconfig file for tweaking WSL2 settings</span></span>
```
[wsl2]
kernel=<path>              # An absolute Windows path to a custom Linux kernel.
memory=<size>              # How much memory to assign to the WSL2 VM.
processors=<number>        # How many processors to assign to the WSL2 VM.
swap=<size>                # How much swap space to add to the WSL2 VM. 0 for no swap file.
swapFile=<path>            # An absolute Windows path to the swap vhd.
localhostForwarding=<bool> # Boolean specifying if ports bound to wildcard or localhost in the WSL2 VM should be connectable from the host via localhost:port (default true).

# <path> entries must be absolute Windows paths with escaped backslashes, for example C:\\Users\\Ben\\kernel
# <size> entries must be size followed by unit, for example 8GB or 512MB
```

## <a name="build-18917"></a><span data-ttu-id="b3232-155">Сборка 18917</span><span class="sxs-lookup"><span data-stu-id="b3232-155">Build 18917</span></span>
<span data-ttu-id="b3232-156">Общие сведения о сборке Windows 18917 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span><span class="sxs-lookup"><span data-stu-id="b3232-156">For general Windows information on build 18917 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-157">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-157">WSL</span></span>
* <span data-ttu-id="b3232-158">Уже доступна версия WSL 2!</span><span class="sxs-lookup"><span data-stu-id="b3232-158">WSL 2 is now available!</span></span> <span data-ttu-id="b3232-159">Дополнительные сведения см. в [блоге](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/).</span><span class="sxs-lookup"><span data-stu-id="b3232-159">Please see [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) for more details.</span></span>
* <span data-ttu-id="b3232-160">Устранена регрессия, из-за которой запуск процессов Windows через символические ссылки выполнялся некорректно [GH 3999].</span><span class="sxs-lookup"><span data-stu-id="b3232-160">Fix a regression where launching Windows processes via symlinks did not work correctly [GH 3999]</span></span>
* <span data-ttu-id="b3232-161">Добавлены следующие параметры wsl.exe: wsl.exe --list --verbose, wsl.exe --list --quiet и wsl.exe --import --version.</span><span class="sxs-lookup"><span data-stu-id="b3232-161">Add wsl.exe --list --verbose, wsl.exe --list --quiet, and wsl.exe --import --version options to wsl.exe</span></span>
* <span data-ttu-id="b3232-162">Добавлен параметр wsl.exe --shutdown.</span><span class="sxs-lookup"><span data-stu-id="b3232-162">Add wsl.exe --shutdown option</span></span>
* <span data-ttu-id="b3232-163">Plan 9: для успешной работы разрешено открытие каталога для записи.</span><span class="sxs-lookup"><span data-stu-id="b3232-163">Plan 9: Allow opening a directory for write to succeed</span></span>

## <a name="build-18890"></a><span data-ttu-id="b3232-164">Сборка 18890</span><span class="sxs-lookup"><span data-stu-id="b3232-164">Build 18890</span></span>
<span data-ttu-id="b3232-165">Общие сведения о сборке Windows 18890 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span><span class="sxs-lookup"><span data-stu-id="b3232-165">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-166">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-166">WSL</span></span>
* <span data-ttu-id="b3232-167">Утечка сокетов не блокирует работу [GH 2913].</span><span class="sxs-lookup"><span data-stu-id="b3232-167">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="b3232-168">Ввод EOF в терминал может заблокировать последующие операции чтения [GH 3421].</span><span class="sxs-lookup"><span data-stu-id="b3232-168">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="b3232-169">В заголовок resolv.conf добавлена ссылка на wsl.conf [рассмотрено в GH 3928].</span><span class="sxs-lookup"><span data-stu-id="b3232-169">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="b3232-170">Взаимоблокировка в коде epoll delete [GH 3922].</span><span class="sxs-lookup"><span data-stu-id="b3232-170">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="b3232-171">Обработка пробелов в аргументах параметров --import и --export [GH 3932].</span><span class="sxs-lookup"><span data-stu-id="b3232-171">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="b3232-172">Расширение файлов, обработанных mmap, не работает должным образом [GH 3939].</span><span class="sxs-lookup"><span data-stu-id="b3232-172">Extending mmap’d files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="b3232-173">Устранена проблема с доступом ARM64 к \\wsl$.</span><span class="sxs-lookup"><span data-stu-id="b3232-173">Fix issue with ARM64 \\wsl$ access not working properly</span></span>
* <span data-ttu-id="b3232-174">Улучшен значок по умолчанию для wsl.exe.</span><span class="sxs-lookup"><span data-stu-id="b3232-174">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="b3232-175">Сборка 18342</span><span class="sxs-lookup"><span data-stu-id="b3232-175">Build 18342</span></span>
<span data-ttu-id="b3232-176">Общие сведения о сборке Windows 18342 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span><span class="sxs-lookup"><span data-stu-id="b3232-176">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-177">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-177">WSL</span></span>
* <span data-ttu-id="b3232-178">Мы добавили возможность доступа пользователей к файлам Linux в дистрибутиве WSL из Windows.</span><span class="sxs-lookup"><span data-stu-id="b3232-178">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="b3232-179">Доступ к этим файлам можно получить с помощью командной строки. Кроме того, такие приложения для Windows, как проводник, VSCode и т. д., могут взаимодействовать с этими файлами.</span><span class="sxs-lookup"><span data-stu-id="b3232-179">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="b3232-180">Чтобы получить доступ к файлам, перейдите в папку \\\\wsl$\\<имя_дистрибутива>, или просмотрите список выполняющихся дистрибутивов, перейдя в \\\\wsl$.</span><span class="sxs-lookup"><span data-stu-id="b3232-180">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="b3232-181">Добавлены дополнительные теги сведений о ЦП и исправлены значения Cpus_allowed[_list] [GH 2234].</span><span class="sxs-lookup"><span data-stu-id="b3232-181">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="b3232-182">Поддержка выполнения из ведомого потока [GH 3800].</span><span class="sxs-lookup"><span data-stu-id="b3232-182">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="b3232-183">Ошибки обновления конфигурации не считаются критическими [GH 3785].</span><span class="sxs-lookup"><span data-stu-id="b3232-183">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="b3232-184">Подсистема binfmt обновлена для правильной обработки смещений [GH 3768].</span><span class="sxs-lookup"><span data-stu-id="b3232-184">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="b3232-185">Включено сопоставление сетевых дисков для Plan 9 [GH 3854].</span><span class="sxs-lookup"><span data-stu-id="b3232-185">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="b3232-186">Поддержка преобразования путей Windows в Linux и наоборот для подключения привязок.</span><span class="sxs-lookup"><span data-stu-id="b3232-186">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="b3232-187">Создание разделов только для чтения для сопоставлений файлов, открытых только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b3232-187">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="b3232-188">Сборка 18334</span><span class="sxs-lookup"><span data-stu-id="b3232-188">Build 18334</span></span>
<span data-ttu-id="b3232-189">Общие сведения о сборке Windows 18334 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span><span class="sxs-lookup"><span data-stu-id="b3232-189">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-190">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-190">WSL</span></span>
* <span data-ttu-id="b3232-191">Перепроектирован способ сопоставления часового пояса Windows с часовым поясом Linux [GH 3747].</span><span class="sxs-lookup"><span data-stu-id="b3232-191">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="b3232-192">Устранены утечки памяти и добавлены новые функции преобразования строк [GH 3746].</span><span class="sxs-lookup"><span data-stu-id="b3232-192">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="b3232-193">Выполнение SIGCONT для группы потоков без потоков является холостой командой [GH 3741].</span><span class="sxs-lookup"><span data-stu-id="b3232-193">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="b3232-194">Правильное отображение дескрипторов файлов socket и epoll в /proc/self/fd.</span><span class="sxs-lookup"><span data-stu-id="b3232-194">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="b3232-195">Сборка 18305</span><span class="sxs-lookup"><span data-stu-id="b3232-195">Build 18305</span></span>
<span data-ttu-id="b3232-196">Общие сведения о сборке Windows 18305 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span><span class="sxs-lookup"><span data-stu-id="b3232-196">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-197">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-197">WSL</span></span>
* <span data-ttu-id="b3232-198">Когда основной поток завершает работу, pthreads утрачивает доступ к файлам [GH 3589].</span><span class="sxs-lookup"><span data-stu-id="b3232-198">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="b3232-199">Команда TIOCSCTTY должна игнорировать параметр force, если он не является обязательным [GH 3652].</span><span class="sxs-lookup"><span data-stu-id="b3232-199">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="b3232-200">Усовершенствована командная строка wsl.exe и добавлены функции импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="b3232-200">wsl.exe command line improvements and addition of import / export functionality.</span></span>
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

## <a name="build-18277"></a><span data-ttu-id="b3232-201">Сборка 18277</span><span class="sxs-lookup"><span data-stu-id="b3232-201">Build 18277</span></span>
<span data-ttu-id="b3232-202">Общие сведения о сборке Windows 18277 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span><span class="sxs-lookup"><span data-stu-id="b3232-202">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-203">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-203">WSL</span></span>
* <span data-ttu-id="b3232-204">Устранена ошибка "Интерфейс не поддерживается" в сборке 18272 [GH 3645].</span><span class="sxs-lookup"><span data-stu-id="b3232-204">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="b3232-205">Игнорируется флаг MNT_FORCE для umount syscall [GH 3605].</span><span class="sxs-lookup"><span data-stu-id="b3232-205">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="b3232-206">Переключено взаимодействие WSL для использования официального API CreatePseudoConsole.</span><span class="sxs-lookup"><span data-stu-id="b3232-206">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="b3232-207">При перезапуске FUTEX_WAIT значение времени ожидания не сохраняется.</span><span class="sxs-lookup"><span data-stu-id="b3232-207">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="b3232-208">Сборка 18272</span><span class="sxs-lookup"><span data-stu-id="b3232-208">Build 18272</span></span>
<span data-ttu-id="b3232-209">Общие сведения о сборке Windows 18272 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span><span class="sxs-lookup"><span data-stu-id="b3232-209">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-210">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-210">WSL</span></span>
* <span data-ttu-id="b3232-211">**Предупреждение**. В этой сборке есть проблема, делающая компонент WSL неработоспособным.</span><span class="sxs-lookup"><span data-stu-id="b3232-211">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="b3232-212">При попытке запустить дистрибутив появится сообщение об ошибке "Интерфейс не поддерживается".</span><span class="sxs-lookup"><span data-stu-id="b3232-212">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="b3232-213">Эта проблема устранена, и соответствующее исправление будет добавлено в сборку для предварительной оценки с ранним доступом, выпускаемую на следующей неделе.</span><span class="sxs-lookup"><span data-stu-id="b3232-213">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="b3232-214">Если вы установили эту сборку, то вы можете вернуться к предыдущей сборке Windows, выбрав "Параметры > Обновление и безопасность > Восстановление" и щелкнув "Вернуться к предыдущей версии Windows 10".</span><span class="sxs-lookup"><span data-stu-id="b3232-214">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="b3232-215">Сборка 18267</span><span class="sxs-lookup"><span data-stu-id="b3232-215">Build 18267</span></span>
<span data-ttu-id="b3232-216">Общие сведения о сборке Windows 18267 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span><span class="sxs-lookup"><span data-stu-id="b3232-216">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-217">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-217">WSL</span></span>
* <span data-ttu-id="b3232-218">Устранена проблема, из-за которой зомби-процесс мог быть не удален и существовал неограниченное время.</span><span class="sxs-lookup"><span data-stu-id="b3232-218">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="b3232-219">WslRegisterDistribution переставал отвечать на запросы, если сообщение об ошибке превышало максимальную длину [GH 3592].</span><span class="sxs-lookup"><span data-stu-id="b3232-219">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="b3232-220">Разрешено использование fsync с файлами только для чтения в DrvFs [GH 3556].</span><span class="sxs-lookup"><span data-stu-id="b3232-220">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="b3232-221">Перед созданием символических ссылок в каталогах /bin и /sbin убедитесь, что эти каталоги существуют [GH 3584].</span><span class="sxs-lookup"><span data-stu-id="b3232-221">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="b3232-222">Добавлен механизм времени ожидания завершения экземпляра для экземпляров WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-222">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="b3232-223">Сейчас время ожидания равно 15 секундам, то есть работа экземпляра завершается через 15 секунд после завершения последнего процесса WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-223">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="b3232-224">Чтобы немедленно завершить дистрибутив, используйте следующую команду.</span><span class="sxs-lookup"><span data-stu-id="b3232-224">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="b3232-225">Сборка 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="b3232-225">Build 17763 (1809)</span></span>
<span data-ttu-id="b3232-226">Общие сведения о сборке Windows 17763 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span><span class="sxs-lookup"><span data-stu-id="b3232-226">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-227">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-227">WSL</span></span>
* <span data-ttu-id="b3232-228">Проверка разрешения SetPriority для syscall была слишком строгая для изменения приоритета того же потока [GH 1838].</span><span class="sxs-lookup"><span data-stu-id="b3232-228">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="b3232-229">Убедитесь, что для времени загрузки используется несмещенное время прерывания, чтобы избежать возврата отрицательных значений clock_gettime (CLOCK_BOOTTIME) [GH 3434].</span><span class="sxs-lookup"><span data-stu-id="b3232-229">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="b3232-230">Обработка символических ссылок в интерпретаторе binfmt для WSL [GH 3424].</span><span class="sxs-lookup"><span data-stu-id="b3232-230">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="b3232-231">Улучшена обработка очистки дескриптора файла ведущего потока группы потоков.</span><span class="sxs-lookup"><span data-stu-id="b3232-231">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="b3232-232">Чтобы избежать переполнения, переключите WSL на использование KeQueryInterruptTimePrecise вместо KeQueryPerformanceCounter [GH 3252].</span><span class="sxs-lookup"><span data-stu-id="b3232-232">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="b3232-233">Подключение Ptrace могло вызывать неправильное возвращаемое значение из системных вызовов [GH 1731].</span><span class="sxs-lookup"><span data-stu-id="b3232-233">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="b3232-234">Устранено несколько проблем, связанных с AF_UNIX [GH 3371].</span><span class="sxs-lookup"><span data-stu-id="b3232-234">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="b3232-235">Устранена проблема, которая могла привести к сбою взаимодействия WSL, если длина текущего рабочего каталога была меньше 5 знаков [GH 3379].</span><span class="sxs-lookup"><span data-stu-id="b3232-235">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="b3232-236">Предотвращена задержка в 1 секунду при сбое замыкания на себя подключений к несуществующим портам (GH 3286).</span><span class="sxs-lookup"><span data-stu-id="b3232-236">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="b3232-237">Добавлен файл заглушки /proc/sys/fs/file-max [GH 2893].</span><span class="sxs-lookup"><span data-stu-id="b3232-237">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="b3232-238">Уточнены сведения об области действия IPv6.</span><span class="sxs-lookup"><span data-stu-id="b3232-238">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="b3232-239">Поддержка PR_SET_PTRACER [GH 3053].</span><span class="sxs-lookup"><span data-stu-id="b3232-239">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="b3232-240">Канальная файловая система необоснованно очищала событие epoll, активируемое переходом [GH 3276].</span><span class="sxs-lookup"><span data-stu-id="b3232-240">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="b3232-241">Исполняемый файл Win32, запущенный с помощью символической ссылки NTFS, не учитывал имя символической ссылки [GH 2909].</span><span class="sxs-lookup"><span data-stu-id="b3232-241">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="b3232-242">Улучшена поддержка зомби [GH 1353].</span><span class="sxs-lookup"><span data-stu-id="b3232-242">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="b3232-243">Добавлены записи wsl.conf для управления поведением взаимодействия с Windows [GH 1493].</span><span class="sxs-lookup"><span data-stu-id="b3232-243">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="b3232-244">Устранена проблема, из-за которой команда getsockname не всегда возвращала тип семейства сокетов UNIX [GH 1774].</span><span class="sxs-lookup"><span data-stu-id="b3232-244">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="b3232-245">Добавлена поддержка TIOCSTI [GH 1863].</span><span class="sxs-lookup"><span data-stu-id="b3232-245">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="b3232-246">Неблокирующие сокеты в процессе подключения должны возвращать EAGAIN для попыток записи [GH 2846].</span><span class="sxs-lookup"><span data-stu-id="b3232-246">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="b3232-247">Поддержка взаимодействия с подключенными виртуальными жесткими дисками [GH 3246, 3291].</span><span class="sxs-lookup"><span data-stu-id="b3232-247">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="b3232-248">Устранена проблема с проверкой разрешений для корневой папки [GH 3304].</span><span class="sxs-lookup"><span data-stu-id="b3232-248">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="b3232-249">Ограниченная поддержка вызовов ioctl с аргументами KDGKBTYPE, KDGKBMODE и KDSKBMODE для клавиатуры tty.</span><span class="sxs-lookup"><span data-stu-id="b3232-249">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="b3232-250">Приложения пользовательского интерфейса Windows должны выполняться, даже если они запущены в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="b3232-250">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="b3232-251">Добавлен параметр wsl --u или --user [GH 1203].</span><span class="sxs-lookup"><span data-stu-id="b3232-251">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="b3232-252">Устранены проблемы с запуском WSL, когда включен быстрый запуск [GH 2576].</span><span class="sxs-lookup"><span data-stu-id="b3232-252">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="b3232-253">Сокеты UNIX должны хранить учетные данные отключенных одноранговых узлов [GH 3183].</span><span class="sxs-lookup"><span data-stu-id="b3232-253">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="b3232-254">Работа неблокирующих сокетов UNIX неограниченное время завершалась сбоем и возвращалось значение EAGAIN [GH 3191].</span><span class="sxs-lookup"><span data-stu-id="b3232-254">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="b3232-255">Новый тип подключения drvfs по умолчанию case=off [GH 2937, 3212, 3328].</span><span class="sxs-lookup"><span data-stu-id="b3232-255">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="b3232-256">Дополнительные сведения см. в [этом блоге](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/).</span><span class="sxs-lookup"><span data-stu-id="b3232-256">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="b3232-257">Добавлен параметр wslconfig /terminate для остановки выполнения дистрибутивов.</span><span class="sxs-lookup"><span data-stu-id="b3232-257">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="b3232-258">Устранена проблема с пунктами в контекстном меню оболочки WSL, из-за которой неправильно обрабатывались пути с пробелами.</span><span class="sxs-lookup"><span data-stu-id="b3232-258">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="b3232-259">Учет регистра в именах каталогов реализован в качестве расширенного атрибута.</span><span class="sxs-lookup"><span data-stu-id="b3232-259">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="b3232-260">ARM64: имитация операций обслуживания кэша.</span><span class="sxs-lookup"><span data-stu-id="b3232-260">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="b3232-261">Устранена [проблема с dotnet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="b3232-261">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="b3232-262">DrvFs: в частном диапазоне допускаются только неэкранированные знаки, которые соответствуют экранированному знаку.</span><span class="sxs-lookup"><span data-stu-id="b3232-262">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="b3232-263">Устранена ошибка завышения или занижения на единицу при проверке длины интерпретатором анализатора ELF [GH 3154].</span><span class="sxs-lookup"><span data-stu-id="b3232-263">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="b3232-264">Абсолютные таймеры WSL со временем в прошлом не срабатывали [GH 3091].</span><span class="sxs-lookup"><span data-stu-id="b3232-264">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="b3232-265">Убедитесь, что вновь созданные точки повторного анализа указаны как таковые в родительском каталоге.</span><span class="sxs-lookup"><span data-stu-id="b3232-265">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="b3232-266">Атомарное создание каталогов с учетом регистра в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="b3232-266">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="b3232-267">Устранена дополнительная проблема, из-за которой многопоточные операции могли возвращать ENOENT, даже если файл существовал.</span><span class="sxs-lookup"><span data-stu-id="b3232-267">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="b3232-268">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="b3232-268">[GH 2712]</span></span>
* <span data-ttu-id="b3232-269">Устранена ошибка запуска WSL при включенном режиме UMCI.</span><span class="sxs-lookup"><span data-stu-id="b3232-269">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="b3232-270">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="b3232-270">[GH 3020]</span></span>
* <span data-ttu-id="b3232-271">Добавлено контекстное меню обозревателя для запуска WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="b3232-271">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="b3232-272">Чтобы открыть его, нажмите и удерживайте клавишу SHIFT и щелкните правой кнопкой мыши в окне проводника.</span><span class="sxs-lookup"><span data-stu-id="b3232-272">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="b3232-273">Устранено неблокирующее поведение сокетов UNIX [GH 2822, 3100].</span><span class="sxs-lookup"><span data-stu-id="b3232-273">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="b3232-274">Устранена проблема, из-за которой команда NETLINK переставала отвечать на запросы, как было сообщено в GH 2026.</span><span class="sxs-lookup"><span data-stu-id="b3232-274">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="b3232-275">Добавлена поддержка флагов распространения подключения [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="b3232-275">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="b3232-276">Устранена проблема, из-за которой усечение не вызывало события inotify [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="b3232-276">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="b3232-277">Добавлен параметр --exec для wsl.exe, позволяющий вызвать отдельный двоичный файл без оболочки.</span><span class="sxs-lookup"><span data-stu-id="b3232-277">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="b3232-278">Добавлен параметр --distribution для wsl.exe, позволяющий выбрать конкретный дистрибутив.</span><span class="sxs-lookup"><span data-stu-id="b3232-278">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="b3232-279">Ограниченная поддержка dmesg.</span><span class="sxs-lookup"><span data-stu-id="b3232-279">Limited support for dmesg.</span></span> <span data-ttu-id="b3232-280">Теперь приложения могут входить в dmesg.</span><span class="sxs-lookup"><span data-stu-id="b3232-280">Applications can now log to dmesg.</span></span> <span data-ttu-id="b3232-281">Драйвер WSL записывает ограниченные сведения в dmesg.</span><span class="sxs-lookup"><span data-stu-id="b3232-281">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="b3232-282">В будущем эти возможности можно будет расширить, чтобы записывать другие сведения и данные диагностики из драйвера.</span><span class="sxs-lookup"><span data-stu-id="b3232-282">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="b3232-283">Примечание. Сейчас dmesg поддерживается через интерфейс устройства `/dev/kmsg`.</span><span class="sxs-lookup"><span data-stu-id="b3232-283">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="b3232-284">Интерфейс syscall `syslog` пока не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b3232-284">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="b3232-285">Поэтому некоторые параметры командной строки `dmesg`, такие как `-S` и `-C`, не работают.</span><span class="sxs-lookup"><span data-stu-id="b3232-285">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="b3232-286">Изменены GID и режим по умолчанию для последовательных устройств, чтобы обеспечить соответствие собственному режиму [GH 3042].</span><span class="sxs-lookup"><span data-stu-id="b3232-286">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="b3232-287">Теперь DrvFs поддерживает расширенные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="b3232-287">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="b3232-288">Примечание. В DrvFs были некоторые ограничения для имен расширенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="b3232-288">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="b3232-289">Некоторые знаки (например, "/", ":" и "\*") не допускаются, а в именах расширенных атрибутов в DrvFs не учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="b3232-289">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="b3232-290">Сборка 18252 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="b3232-290">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="b3232-291">Общие сведения о сборке Windows 18252 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span><span class="sxs-lookup"><span data-stu-id="b3232-291">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-292">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-292">WSL</span></span>
* <span data-ttu-id="b3232-293">Двоичные файлы init и bsdtar перемещены из библиотеки DLL lxssmanager в отдельную папку tools.</span><span class="sxs-lookup"><span data-stu-id="b3232-293">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="b3232-294">Устранено состязание при закрытии дескриптора файла в случае использования CLONE_FILES.</span><span class="sxs-lookup"><span data-stu-id="b3232-294">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="b3232-295">Обработка необязательных полей в /proc/pid/mountinfo при преобразовании путей DrvFs.</span><span class="sxs-lookup"><span data-stu-id="b3232-295">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="b3232-296">Допускается успешное выполнение mknod DrvFs без поддержки метаданных для S_IFREG.</span><span class="sxs-lookup"><span data-stu-id="b3232-296">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="b3232-297">Файлы только для чтения, созданные в DrvFs, должны иметь атрибут readonly [GH 3411].</span><span class="sxs-lookup"><span data-stu-id="b3232-297">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="b3232-298">Добавлено вспомогательное приложение /sbin/mount.drvfs для управления подключением DrvFs.</span><span class="sxs-lookup"><span data-stu-id="b3232-298">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="b3232-299">Использование переименования POSIX в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="b3232-299">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="b3232-300">Разрешено преобразование путей в томах без GUID тома.</span><span class="sxs-lookup"><span data-stu-id="b3232-300">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="b3232-301">Сборка 17738 (Fast)</span><span class="sxs-lookup"><span data-stu-id="b3232-301">Build 17738 (Fast)</span></span>
<span data-ttu-id="b3232-302">Общие сведения о сборке Windows 17738 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span><span class="sxs-lookup"><span data-stu-id="b3232-302">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-303">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-303">WSL</span></span>
* <span data-ttu-id="b3232-304">Проверка разрешения SetPriority для syscall была слишком строгая для изменения приоритета того же потока [GH 1838].</span><span class="sxs-lookup"><span data-stu-id="b3232-304">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="b3232-305">Убедитесь, что для времени загрузки используется несмещенное время прерывания, чтобы избежать возврата отрицательных значений clock_gettime (CLOCK_BOOTTIME) [GH 3434].</span><span class="sxs-lookup"><span data-stu-id="b3232-305">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="b3232-306">Обработка символических ссылок в интерпретаторе binfmt для WSL [GH 3424].</span><span class="sxs-lookup"><span data-stu-id="b3232-306">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="b3232-307">Улучшена обработка очистки дескриптора файла ведущего потока группы потоков.</span><span class="sxs-lookup"><span data-stu-id="b3232-307">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="b3232-308">Сборка 17728 (Fast)</span><span class="sxs-lookup"><span data-stu-id="b3232-308">Build 17728 (Fast)</span></span>
<span data-ttu-id="b3232-309">Общие сведения о сборке Windows 17728 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span><span class="sxs-lookup"><span data-stu-id="b3232-309">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-310">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-310">WSL</span></span>
* <span data-ttu-id="b3232-311">Чтобы избежать переполнения, переключите WSL на использование KeQueryInterruptTimePrecise вместо KeQueryPerformanceCounter [GH 3252].</span><span class="sxs-lookup"><span data-stu-id="b3232-311">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="b3232-312">Подключение Ptrace могло вызывать неправильное возвращаемое значение из системных вызовов [GH 1731].</span><span class="sxs-lookup"><span data-stu-id="b3232-312">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="b3232-313">Устранен ряд проблем, связанных с AF_UNIX [GH 3371].</span><span class="sxs-lookup"><span data-stu-id="b3232-313">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="b3232-314">Устранена проблема, которая могла привести к сбою взаимодействия WSL, если длина текущего рабочего каталога была меньше 5 знаков [GH 3379].</span><span class="sxs-lookup"><span data-stu-id="b3232-314">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="b3232-315">Сборка 18204 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="b3232-315">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="b3232-316">Общие сведения о сборке Windows 18204 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="b3232-316">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-317">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-317">WSL</span></span>
* <span data-ttu-id="b3232-318">Канальная файловая система необоснованно очищала событие epoll, активируемое переходом [GH 3276].</span><span class="sxs-lookup"><span data-stu-id="b3232-318">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="b3232-319">Исполняемый файл Win32, запущенный с помощью символической ссылки NTFS, не учитывал имя символической ссылки [GH 2909].</span><span class="sxs-lookup"><span data-stu-id="b3232-319">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="b3232-320">Сборка 17723 (Fast)</span><span class="sxs-lookup"><span data-stu-id="b3232-320">Build 17723 (Fast)</span></span>
<span data-ttu-id="b3232-321">Общие сведения о сборке Windows 17723 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="b3232-321">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-322">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-322">WSL</span></span>
* <span data-ttu-id="b3232-323">Предотвращена задержка в 1 секунду при сбое замыкания на себя подключений к несуществующим портам (GH 3286).</span><span class="sxs-lookup"><span data-stu-id="b3232-323">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="b3232-324">Добавлен файл заглушки /proc/sys/fs/file-max [GH 2893].</span><span class="sxs-lookup"><span data-stu-id="b3232-324">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="b3232-325">Уточнены сведения об области действия IPv6.</span><span class="sxs-lookup"><span data-stu-id="b3232-325">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="b3232-326">Поддержка PR_SET_PTRACER [GH 3053].</span><span class="sxs-lookup"><span data-stu-id="b3232-326">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="b3232-327">Канальная файловая система необоснованно очищала событие epoll, активируемое переходом [GH 3276].</span><span class="sxs-lookup"><span data-stu-id="b3232-327">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="b3232-328">Исполняемый файл Win32, запущенный с помощью символической ссылки NTFS, не учитывал имя символической ссылки [GH 2909].</span><span class="sxs-lookup"><span data-stu-id="b3232-328">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="b3232-329">Сборка 17713</span><span class="sxs-lookup"><span data-stu-id="b3232-329">Build 17713</span></span>
<span data-ttu-id="b3232-330">Общие сведения о сборке Windows 17713 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span><span class="sxs-lookup"><span data-stu-id="b3232-330">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-331">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-331">WSL</span></span>
* <span data-ttu-id="b3232-332">Улучшена поддержка зомби [GH 1353].</span><span class="sxs-lookup"><span data-stu-id="b3232-332">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="b3232-333">Добавлены записи wsl.conf для управления поведением взаимодействия с Windows [GH 1493].</span><span class="sxs-lookup"><span data-stu-id="b3232-333">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="b3232-334">Устранена проблема, из-за которой команда getsockname не всегда возвращала тип семейства сокетов UNIX [GH 1774].</span><span class="sxs-lookup"><span data-stu-id="b3232-334">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="b3232-335">Добавлена поддержка TIOCSTI [GH 1863].</span><span class="sxs-lookup"><span data-stu-id="b3232-335">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="b3232-336">Неблокирующие сокеты в процессе подключения должны возвращать EAGAIN для попыток записи [GH 2846].</span><span class="sxs-lookup"><span data-stu-id="b3232-336">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="b3232-337">Поддержка взаимодействия с подключенными виртуальными жесткими дисками [GH 3246, 3291].</span><span class="sxs-lookup"><span data-stu-id="b3232-337">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="b3232-338">Устранена проблема с проверкой разрешений для корневой папки [GH 3304].</span><span class="sxs-lookup"><span data-stu-id="b3232-338">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="b3232-339">Ограниченная поддержка вызовов ioctl с аргументами KDGKBTYPE, KDGKBMODE и KDSKBMODE для клавиатуры tty.</span><span class="sxs-lookup"><span data-stu-id="b3232-339">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="b3232-340">Приложения пользовательского интерфейса Windows должны выполняться, даже если они запущены в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="b3232-340">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="b3232-341">Сборка 17704</span><span class="sxs-lookup"><span data-stu-id="b3232-341">Build 17704</span></span>
<span data-ttu-id="b3232-342">Общие сведения о сборке Windows 17704 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span><span class="sxs-lookup"><span data-stu-id="b3232-342">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-343">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-343">WSL</span></span>
* <span data-ttu-id="b3232-344">Добавлен параметр wsl --u или --user [GH 1203].</span><span class="sxs-lookup"><span data-stu-id="b3232-344">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="b3232-345">Устранены проблемы с запуском WSL, когда включен быстрый запуск [GH 2576].</span><span class="sxs-lookup"><span data-stu-id="b3232-345">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="b3232-346">Сокеты UNIX должны хранить учетные данные отключенных одноранговых узлов [GH 3183].</span><span class="sxs-lookup"><span data-stu-id="b3232-346">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="b3232-347">Работа неблокирующих сокетов UNIX неограниченное время завершалась сбоем и возвращалось значение EAGAIN [GH 3191].</span><span class="sxs-lookup"><span data-stu-id="b3232-347">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="b3232-348">Новый тип подключения drvfs по умолчанию case=off [GH 2937, 3212, 3328].</span><span class="sxs-lookup"><span data-stu-id="b3232-348">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="b3232-349">Дополнительные сведения см. в [этом блоге](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/).</span><span class="sxs-lookup"><span data-stu-id="b3232-349">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="b3232-350">Добавлен параметр wslconfig /terminate для остановки выполнения дистрибутивов.</span><span class="sxs-lookup"><span data-stu-id="b3232-350">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="b3232-351">Сборка 17692</span><span class="sxs-lookup"><span data-stu-id="b3232-351">Build 17692</span></span>
<span data-ttu-id="b3232-352">Общие сведения о сборке Windows 17692 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span><span class="sxs-lookup"><span data-stu-id="b3232-352">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-353">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-353">WSL</span></span>
* <span data-ttu-id="b3232-354">Устранена проблема с пунктами в контекстном меню оболочки WSL, из-за которой неправильно обрабатывались пути с пробелами.</span><span class="sxs-lookup"><span data-stu-id="b3232-354">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="b3232-355">Учет регистра в именах каталогов реализован в качестве расширенного атрибута.</span><span class="sxs-lookup"><span data-stu-id="b3232-355">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="b3232-356">ARM64: имитация операций обслуживания кэша.</span><span class="sxs-lookup"><span data-stu-id="b3232-356">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="b3232-357">Устранена [проблема с dotnet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="b3232-357">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="b3232-358">DrvFs: в частном диапазоне допускаются только неэкранированные знаки, которые соответствуют экранированному знаку.</span><span class="sxs-lookup"><span data-stu-id="b3232-358">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="b3232-359">Сборка 17686</span><span class="sxs-lookup"><span data-stu-id="b3232-359">Build 17686</span></span>
<span data-ttu-id="b3232-360">Общие сведения о сборке Windows 17686 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span><span class="sxs-lookup"><span data-stu-id="b3232-360">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-361">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-361">WSL</span></span>
* <span data-ttu-id="b3232-362">Устранена ошибка завышения или занижения на единицу при проверке длины интерпретатором анализатора ELF [GH 3154].</span><span class="sxs-lookup"><span data-stu-id="b3232-362">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="b3232-363">Абсолютные таймеры WSL со временем в прошлом не срабатывали [GH 3091].</span><span class="sxs-lookup"><span data-stu-id="b3232-363">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="b3232-364">Убедитесь, что вновь созданные точки повторного анализа указаны как таковые в родительском каталоге.</span><span class="sxs-lookup"><span data-stu-id="b3232-364">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="b3232-365">Атомарное создание каталогов с учетом регистра в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="b3232-365">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="b3232-366">Сборка 17677</span><span class="sxs-lookup"><span data-stu-id="b3232-366">Build 17677</span></span>
<span data-ttu-id="b3232-367">Общие сведения о сборке Windows 17677 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span><span class="sxs-lookup"><span data-stu-id="b3232-367">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-368">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-368">WSL</span></span>
* <span data-ttu-id="b3232-369">Устранена дополнительная проблема, из-за которой многопоточные операции могли возвращать ENOENT, даже если файл существовал.</span><span class="sxs-lookup"><span data-stu-id="b3232-369">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="b3232-370">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="b3232-370">[GH 2712]</span></span>
* <span data-ttu-id="b3232-371">Устранена ошибка запуска WSL при включенном режиме UMCI.</span><span class="sxs-lookup"><span data-stu-id="b3232-371">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="b3232-372">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="b3232-372">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="b3232-373">Сборка 17666</span><span class="sxs-lookup"><span data-stu-id="b3232-373">Build 17666</span></span>
<span data-ttu-id="b3232-374">Общие сведения о сборке Windows 17666 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span><span class="sxs-lookup"><span data-stu-id="b3232-374">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-375">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-375">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="b3232-376">ПРЕДУПРЕЖДЕНИЕ! Существует проблема, препятствующая запуску WSL на некоторых наборах микросхем AMD [GH 3134].</span><span class="sxs-lookup"><span data-stu-id="b3232-376">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="b3232-377">Исправление готово и находится в процессе добавления в ветвь сборок для программы предварительной оценки Windows.</span><span class="sxs-lookup"><span data-stu-id="b3232-377">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="b3232-378">Добавлено контекстное меню обозревателя для запуска WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="b3232-378">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="b3232-379">Чтобы открыть его, нажмите и удерживайте клавишу SHIFT и щелкните правой кнопкой мыши в окне проводника.</span><span class="sxs-lookup"><span data-stu-id="b3232-379">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="b3232-380">Устранено неблокирующее поведение сокетов UNIX [GH 2822, 3100].</span><span class="sxs-lookup"><span data-stu-id="b3232-380">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="b3232-381">Устранена проблема, из-за которой команда NETLINK переставала отвечать на запросы, как было сообщено в GH 2026.</span><span class="sxs-lookup"><span data-stu-id="b3232-381">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="b3232-382">Добавлена поддержка флагов распространения подключения [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="b3232-382">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="b3232-383">Устранена проблема, из-за которой усечение не вызывало события inotify [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="b3232-383">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="b3232-384">Добавлен параметр --exec для wsl.exe, позволяющий вызвать отдельный двоичный файл без оболочки.</span><span class="sxs-lookup"><span data-stu-id="b3232-384">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="b3232-385">Добавлен параметр --distribution для wsl.exe, позволяющий выбрать конкретный дистрибутив.</span><span class="sxs-lookup"><span data-stu-id="b3232-385">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="b3232-386">Сборка 17655 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="b3232-386">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="b3232-387">Общие сведения о сборке Windows 17655 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="b3232-387">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-388">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-388">WSL</span></span>
* <span data-ttu-id="b3232-389">Ограниченная поддержка dmesg.</span><span class="sxs-lookup"><span data-stu-id="b3232-389">Limited support for dmesg.</span></span> <span data-ttu-id="b3232-390">Теперь приложения могут входить в dmesg.</span><span class="sxs-lookup"><span data-stu-id="b3232-390">Applications can now log to dmesg.</span></span> <span data-ttu-id="b3232-391">Драйвер WSL записывает ограниченные сведения в dmesg.</span><span class="sxs-lookup"><span data-stu-id="b3232-391">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="b3232-392">В будущем эти возможности можно будет расширить, чтобы записывать другие сведения и данные диагностики из драйвера.</span><span class="sxs-lookup"><span data-stu-id="b3232-392">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="b3232-393">Примечание. Сейчас dmesg поддерживается через интерфейс устройства `/dev/kmsg`.</span><span class="sxs-lookup"><span data-stu-id="b3232-393">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="b3232-394">Интерфейс sycall `syslog` еще не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b3232-394">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="b3232-395">Поэтому некоторые параметры командной строки `dmesg`, такие как `-S` и `-C`, не работают.</span><span class="sxs-lookup"><span data-stu-id="b3232-395">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="b3232-396">Устранена проблема, из-за которой многопоточные операции могли возвращать ENOENT, даже если файл существовал.</span><span class="sxs-lookup"><span data-stu-id="b3232-396">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="b3232-397">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="b3232-397">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="b3232-398">Сборка 17639 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="b3232-398">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="b3232-399">Общие сведения о сборке Windows 17639 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="b3232-399">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-400">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-400">WSL</span></span>
* <span data-ttu-id="b3232-401">Изменены GID и режим по умолчанию для последовательных устройств, чтобы обеспечить соответствие собственному режиму [GH 3042].</span><span class="sxs-lookup"><span data-stu-id="b3232-401">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="b3232-402">Теперь DrvFs поддерживает расширенные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="b3232-402">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="b3232-403">Примечание. В DrvFs были некоторые ограничения для имен расширенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="b3232-403">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="b3232-404">В частности, некоторые знаки (например, "/", ":" и "\*") не допускаются, а в именах расширенных атрибутов в DrvFs не учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="b3232-404">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="b3232-405">Сборка 17133 (Fast)</span><span class="sxs-lookup"><span data-stu-id="b3232-405">Build 17133 (Fast)</span></span>
<span data-ttu-id="b3232-406">Общие сведения о сборке Windows 17133 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="b3232-406">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-407">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-407">WSL</span></span>
* <span data-ttu-id="b3232-408">Устранено прекращение ответа на запросы в WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-408">Fix for hang in WSL.</span></span> <span data-ttu-id="b3232-409">[GH 3039, 3034]</span><span class="sxs-lookup"><span data-stu-id="b3232-409">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="b3232-410">Сборка 17128 (Fast)</span><span class="sxs-lookup"><span data-stu-id="b3232-410">Build 17128 (Fast)</span></span>
<span data-ttu-id="b3232-411">Общие сведения о сборке Windows 17128 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="b3232-411">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-412">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-412">WSL</span></span>
* <span data-ttu-id="b3232-413">Нет</span><span class="sxs-lookup"><span data-stu-id="b3232-413">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="b3232-414">Сборка 17627 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="b3232-414">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="b3232-415">Общие сведения о сборке Windows 17627 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="b3232-415">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-416">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-416">WSL</span></span>
* <span data-ttu-id="b3232-417">Добавлена поддержка фьютексных операций с поддержкой числа пи.</span><span class="sxs-lookup"><span data-stu-id="b3232-417">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="b3232-418">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="b3232-418">[GH 1006]</span></span>
    * <span data-ttu-id="b3232-419">Обратите внимание на то, что приоритеты в настоящее время не поддерживаются компонентом WSL, так что существуют ограничения, но стандартное использование должно быть доступно.</span><span class="sxs-lookup"><span data-stu-id="b3232-419">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="b3232-420">Поддержка брандмауэра Windows для процессов WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-420">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="b3232-421">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="b3232-421">[GH 1852]</span></span>
    * <span data-ttu-id="b3232-422">Например, чтобы разрешить процессу Python в WSL ожидать передачи данных через какой-либо порт, используйте командную строку Windows с повышенными привилегиями: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="b3232-422">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="b3232-423">Дополнительные сведения о добавлении правил брандмауэра доступны по [этой ссылке](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh).</span><span class="sxs-lookup"><span data-stu-id="b3232-423">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="b3232-424">При использовании wsl.exe учитывается оболочка по умолчанию пользователя.</span><span class="sxs-lookup"><span data-stu-id="b3232-424">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="b3232-425">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="b3232-425">[GH 2372]</span></span>
* <span data-ttu-id="b3232-426">Все сетевые интерфейсы отображаются как Ethernet.</span><span class="sxs-lookup"><span data-stu-id="b3232-426">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="b3232-427">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="b3232-427">[GH 2996]</span></span>
* <span data-ttu-id="b3232-428">Улучшена обработка поврежденного файла /etc/passwd.</span><span class="sxs-lookup"><span data-stu-id="b3232-428">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="b3232-429">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="b3232-429">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="b3232-430">Консоль</span><span class="sxs-lookup"><span data-stu-id="b3232-430">Console</span></span>
* <span data-ttu-id="b3232-431">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="b3232-431">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-432">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-432">LTP Results:</span></span>
<span data-ttu-id="b3232-433">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="b3232-433">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="b3232-434">Сборка 17618 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="b3232-434">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="b3232-435">Общие сведения о сборке Windows 17618 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="b3232-435">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-436">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-436">WSL</span></span>
* <span data-ttu-id="b3232-437">Введена функция псевдоконсоли для взаимодействия с NT [GH 988, 1366, 1433, 1542, 2370, 2406].</span><span class="sxs-lookup"><span data-stu-id="b3232-437">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="b3232-438">Устаревший механизм установки (lxrun.exe) является нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="b3232-438">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="b3232-439">Для установки дистрибутивов используется Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="b3232-439">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="b3232-440">Консоль</span><span class="sxs-lookup"><span data-stu-id="b3232-440">Console</span></span>
* <span data-ttu-id="b3232-441">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="b3232-441">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-442">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-442">LTP Results:</span></span>
<span data-ttu-id="b3232-443">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="b3232-443">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="b3232-444">Сборка 17110</span><span class="sxs-lookup"><span data-stu-id="b3232-444">Build 17110</span></span>
<span data-ttu-id="b3232-445">Общие сведения о сборке Windows 17110 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span><span class="sxs-lookup"><span data-stu-id="b3232-445">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-446">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-446">WSL</span></span>
* <span data-ttu-id="b3232-447">Разрешено завершение /init из Windows [GH 2928].</span><span class="sxs-lookup"><span data-stu-id="b3232-447">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="b3232-448">Теперь DrvFs по умолчанию учитывает регистр в имени отдельно для каждого каталога (аналогично параметру подключения "case=dir").</span><span class="sxs-lookup"><span data-stu-id="b3232-448">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="b3232-449">Для использования параметра "case=force" (прежнее поведение) требуется задать раздел реестра.</span><span class="sxs-lookup"><span data-stu-id="b3232-449">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="b3232-450">Выполните следующую команду, чтобы включить режим "case=force", если необходимо его использовать: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span><span class="sxs-lookup"><span data-stu-id="b3232-450">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="b3232-451">Если у вас есть каталоги, созданные с помощью WSL в более ранней версии Windows, в которых должен учитываться регистр, используйте fsutil.exe, чтобы пометить их как каталоги с учетом регистра: fsutil.exe file setcasesensitiveinfo <path> enable</span><span class="sxs-lookup"><span data-stu-id="b3232-451">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="b3232-452">Строки, возвращаемые из uname syscall, завершаются значением NULL.</span><span class="sxs-lookup"><span data-stu-id="b3232-452">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="b3232-453">Консоль</span><span class="sxs-lookup"><span data-stu-id="b3232-453">Console</span></span>
* <span data-ttu-id="b3232-454">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="b3232-454">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-455">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-455">LTP Results:</span></span>
<span data-ttu-id="b3232-456">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="b3232-456">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="b3232-457">Сборка 17107</span><span class="sxs-lookup"><span data-stu-id="b3232-457">Build 17107</span></span>
<span data-ttu-id="b3232-458">Общие сведения о сборке Windows 17107 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span><span class="sxs-lookup"><span data-stu-id="b3232-458">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-459">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-459">WSL</span></span>
* <span data-ttu-id="b3232-460">Поддержка TCSETSF и TCSETSW на главных конечных точках PTY [GH 2552].</span><span class="sxs-lookup"><span data-stu-id="b3232-460">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="b3232-461">Запуск одновременных процессов взаимодействия мог привести к возвращению EINVAL [GH 2813].</span><span class="sxs-lookup"><span data-stu-id="b3232-461">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="b3232-462">Устранена проблема с PTRACE_ATTACH для отображения правильного состояния трассировки в /proc/pid/status.</span><span class="sxs-lookup"><span data-stu-id="b3232-462">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="b3232-463">Устранено состязание, когда кратковременные процессы, клонированные с флагами CLEARTID и SETTID, могли завершиться без очистки адреса TID.</span><span class="sxs-lookup"><span data-stu-id="b3232-463">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="b3232-464">Отображается сообщение, если при переходе со сборки, предшествующей сборке 17093, выполняется обновление каталогов файловой системы Linux.</span><span class="sxs-lookup"><span data-stu-id="b3232-464">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="b3232-465">Дополнительные сведения об изменениях в файловой системе в сборке 17093 доступны в заметках о выпуске [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span><span class="sxs-lookup"><span data-stu-id="b3232-465">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="b3232-466">Консоль</span><span class="sxs-lookup"><span data-stu-id="b3232-466">Console</span></span>
* <span data-ttu-id="b3232-467">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="b3232-467">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-468">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-468">LTP Results:</span></span>
<span data-ttu-id="b3232-469">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="b3232-469">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="b3232-470">Сборка 17101</span><span class="sxs-lookup"><span data-stu-id="b3232-470">Build 17101</span></span>
<span data-ttu-id="b3232-471">Общие сведения о сборке Windows 17101 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="b3232-471">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-472">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-472">WSL</span></span>
* <span data-ttu-id="b3232-473">Поддержка signalfd.</span><span class="sxs-lookup"><span data-stu-id="b3232-473">Support for signalfd.</span></span> <span data-ttu-id="b3232-474">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="b3232-474">[GH 129]</span></span>
* <span data-ttu-id="b3232-475">Поддержка имен файлов, содержащих недопустимые знаки NTFS, благодаря их кодированию в виде частных знаков Юникода.</span><span class="sxs-lookup"><span data-stu-id="b3232-475">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="b3232-476">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="b3232-476">[GH 1514]</span></span>
* <span data-ttu-id="b3232-477">Функция автоматического подключения будет переключаться в режим только для чтения, если запись не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b3232-477">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="b3232-478">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="b3232-478">[GH 2603]</span></span>
* <span data-ttu-id="b3232-479">Допускается вставка суррогатных пар Юникода (например, знаков эмодзи).</span><span class="sxs-lookup"><span data-stu-id="b3232-479">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="b3232-480">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="b3232-480">[GH 2765]</span></span>
* <span data-ttu-id="b3232-481">Псевдофайлы в /proc и /sys должны возвращаться готовыми для чтения и записи после выполнения команд select, poll, epoll и т. д. [GH 2838].</span><span class="sxs-lookup"><span data-stu-id="b3232-481">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="b3232-482">Устранена проблема, из-за которой служба могла уйти в бесконечный цикл, если реестр был незаконно изменен или поврежден.</span><span class="sxs-lookup"><span data-stu-id="b3232-482">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="b3232-483">Сообщения NETLINK исправлены для работы с более новой версией iproute2 (начиная с версии 4.14).</span><span class="sxs-lookup"><span data-stu-id="b3232-483">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="b3232-484">Консоль</span><span class="sxs-lookup"><span data-stu-id="b3232-484">Console</span></span>
* <span data-ttu-id="b3232-485">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="b3232-485">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-486">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-486">LTP Results:</span></span>
<span data-ttu-id="b3232-487">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="b3232-487">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="b3232-488">Сборка 17093</span><span class="sxs-lookup"><span data-stu-id="b3232-488">Build 17093</span></span>
<span data-ttu-id="b3232-489">Общие сведения о сборке Windows 17093 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span><span class="sxs-lookup"><span data-stu-id="b3232-489">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="b3232-490">Внимание!</span><span class="sxs-lookup"><span data-stu-id="b3232-490">Important:</span></span>
<span data-ttu-id="b3232-491">При запуске WSL в первый раз после обновления до этой сборки необходимо выполнить некоторые действия, чтобы обновить каталоги файловой системы Linux.</span><span class="sxs-lookup"><span data-stu-id="b3232-491">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="b3232-492">Это может занять несколько минут, поэтому может показаться, что WSL медленно запускается.</span><span class="sxs-lookup"><span data-stu-id="b3232-492">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="b3232-493">Это должно произойти только один раз для каждого дистрибутива, установленного из Store.</span><span class="sxs-lookup"><span data-stu-id="b3232-493">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="b3232-494">Улучшена поддержка учета регистра в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="b3232-494">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="b3232-495">Теперь DrvFs поддерживает учет регистра отдельно для каждого каталога.</span><span class="sxs-lookup"><span data-stu-id="b3232-495">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="b3232-496">Это новый флаг, который можно задать для каталогов, чтобы указать, что все операции в этих каталогах должны выполняться с учетом регистра, что позволит даже приложениям для Windows правильно открывать файлы, отличающиеся только регистром в именах.</span><span class="sxs-lookup"><span data-stu-id="b3232-496">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="b3232-497">В DrvFs есть новые параметры подключения, управляющие учетом регистра для каждого каталога:</span><span class="sxs-lookup"><span data-stu-id="b3232-497">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="b3232-498">case=force: для всех каталогов учитывается регистр (за исключением корневого диска).</span><span class="sxs-lookup"><span data-stu-id="b3232-498">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="b3232-499">Новые каталоги, созданные с помощью WSL, помечаются как каталоги с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="b3232-499">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="b3232-500">Это устаревшее поведение, за исключением пометки новых каталогов как каталогов с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="b3232-500">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="b3232-501">case=dir: регистр учитывается только для каталогов с флагом учета регистра; для других каталогов регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="b3232-501">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="b3232-502">Новые каталоги, созданные с помощью WSL, помечаются как каталоги с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="b3232-502">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="b3232-503">case=off: регистр учитывается только для каталогов с флагом учета регистра; для других каталогов регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="b3232-503">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="b3232-504">Новые каталоги, созданные с помощью WSL, помечаются как каталоги без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="b3232-504">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="b3232-505">Примечание. Каталоги, созданные WSL в предыдущих выпусках, не имеют этого флага, поэтому для них регистр не будет учитываться, если задан параметр "case=dir".</span><span class="sxs-lookup"><span data-stu-id="b3232-505">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="b3232-506">Способ задания этого флага для существующих каталогов будет реализован в ближайшее время.</span><span class="sxs-lookup"><span data-stu-id="b3232-506">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="b3232-507">Пример подключения с этими параметрами (существующие диски необходимо сначала отключить, чтобы подключить их с другими параметрами): sudo mount -t drvfs C: /mnt/c -o case=dir</span><span class="sxs-lookup"><span data-stu-id="b3232-507">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="b3232-508">Пока что параметр "case=force" все еще используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b3232-508">For now, case=force is still the default option.</span></span> <span data-ttu-id="b3232-509">В будущем по умолчанию будет использоваться параметр case=dir.</span><span class="sxs-lookup"><span data-stu-id="b3232-509">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="b3232-510">Теперь вы можете использовать косую черту в путях Windows при подключении DrvFs, например: sudo mount -t drvfs //server/share /mnt/share</span><span class="sxs-lookup"><span data-stu-id="b3232-510">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="b3232-511">WSL теперь обрабатывает файл /etc/fstab во время запуска экземпляра [GH 2636].</span><span class="sxs-lookup"><span data-stu-id="b3232-511">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="b3232-512">Это делается до автоматического подключения дисков DrvFs. Все диски, которые уже были подключены fstab, не будут автоматически подключаться. Это позволит вам изменить точку подключения для конкретных дисков.</span><span class="sxs-lookup"><span data-stu-id="b3232-512">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="b3232-513">Это поведение можно отключить с помощью wsl.conf.</span><span class="sxs-lookup"><span data-stu-id="b3232-513">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="b3232-514">Файлы mount, mountinfo и mountstats в /proc правильно экранируют специальные знаки, такие как символы обратной косой черты и пробелы [GH 2799].</span><span class="sxs-lookup"><span data-stu-id="b3232-514">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="b3232-515">Теперь можно копировать и перемещать из Windows специальные файлы, созданные с помощью DrvFs, такие как символьные ссылки WSL, или файлы FIFO и сокеты, если метаданные включены.</span><span class="sxs-lookup"><span data-stu-id="b3232-515">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="b3232-516">Можно настроить больше параметров WSL с помощью wsl.conf.</span><span class="sxs-lookup"><span data-stu-id="b3232-516">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="b3232-517">Мы добавили метод для автоматической настройки определенных функций в WSL, которые будут применяться при каждом запуске подсистемы.</span><span class="sxs-lookup"><span data-stu-id="b3232-517">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="b3232-518">Сюда входят параметры автоподключения и конфигурация сети.</span><span class="sxs-lookup"><span data-stu-id="b3232-518">This includes automount options and network configuration.</span></span> <span data-ttu-id="b3232-519">Дополнительные сведения об этом можно получить из нашей записи блога: https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="b3232-519">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="af_unix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="b3232-520">AF_UNIX позволяет устанавливать подключения через сокет между процессами Linux в собственных процессах WSL и Windows.</span><span class="sxs-lookup"><span data-stu-id="b3232-520">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="b3232-521">Теперь приложения WSL и приложения для Windows могут взаимодействовать друг с другом через сокеты UNIX.</span><span class="sxs-lookup"><span data-stu-id="b3232-521">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="b3232-522">Представьте, что вы хотите запустить службу в Windows и сделать ее доступной для приложений для Windows и приложений WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-522">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="b3232-523">Теперь это возможно благодаря сокетам UNIX.</span><span class="sxs-lookup"><span data-stu-id="b3232-523">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="b3232-524">Узнайте больше в записи блога https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="b3232-524">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-525">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-525">WSL</span></span>
* <span data-ttu-id="b3232-526">Поддержка mmap() с MAP_NORESERVE [GH 121, 2784].</span><span class="sxs-lookup"><span data-stu-id="b3232-526">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="b3232-527">Поддержка CLONE_PTRACE и CLONE_UNTRACED [GH 121, 2781].</span><span class="sxs-lookup"><span data-stu-id="b3232-527">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="b3232-528">Обработка сигнала завершения без SIGCHLD в клоне [GH 121, 2781].</span><span class="sxs-lookup"><span data-stu-id="b3232-528">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="b3232-529">Добавлены заглушки /proc/sys/fs/inotify/max_user_instances и /proc/sys/fs/inotify/max_user_watches [GH 1705].</span><span class="sxs-lookup"><span data-stu-id="b3232-529">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="b3232-530">Устранена ошибка при загрузке двоичных файлов ELF, содержащих заголовки загрузки с ненулевыми смещениями [GH 1884].</span><span class="sxs-lookup"><span data-stu-id="b3232-530">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="b3232-531">Заполнение нулями конечных байтов страниц при загрузке образов.</span><span class="sxs-lookup"><span data-stu-id="b3232-531">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="b3232-532">Сокращены случаи, когда execve автоматически завершает процесс.</span><span class="sxs-lookup"><span data-stu-id="b3232-532">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="b3232-533">Консоль</span><span class="sxs-lookup"><span data-stu-id="b3232-533">Console</span></span>
* <span data-ttu-id="b3232-534">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="b3232-534">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-535">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-535">LTP Results:</span></span>
<span data-ttu-id="b3232-536">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="b3232-536">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="b3232-537">Сборка 17083</span><span class="sxs-lookup"><span data-stu-id="b3232-537">Build 17083</span></span>
<span data-ttu-id="b3232-538">Общие сведения о сборке Windows 17083 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="b3232-538">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-539">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-539">WSL</span></span>
* <span data-ttu-id="b3232-540">Исправлена критическая ошибка, связанная с epoll [GH 2798, 2801, 2857].</span><span class="sxs-lookup"><span data-stu-id="b3232-540">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="b3232-541">Исправлено прекращение реагирования на запросы при отключении ASLR [GH 1185, 2870].</span><span class="sxs-lookup"><span data-stu-id="b3232-541">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="b3232-542">Обеспечена атомарность операций mmap [GH 2732].</span><span class="sxs-lookup"><span data-stu-id="b3232-542">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="b3232-543">Консоль</span><span class="sxs-lookup"><span data-stu-id="b3232-543">Console</span></span>
* <span data-ttu-id="b3232-544">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="b3232-544">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-545">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-545">LTP Results:</span></span>
<span data-ttu-id="b3232-546">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="b3232-546">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="b3232-547">Сборка 17074</span><span class="sxs-lookup"><span data-stu-id="b3232-547">Build 17074</span></span>
<span data-ttu-id="b3232-548">Общие сведения о сборке Windows 17074 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span><span class="sxs-lookup"><span data-stu-id="b3232-548">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-549">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-549">WSL</span></span>
* <span data-ttu-id="b3232-550">Исправлен формат хранения метаданных DrvFs [GH 2777].</span><span class="sxs-lookup"><span data-stu-id="b3232-550">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="b3232-551">**Важно!** Метаданные DrvFs, созданные до выпуска этой сборки, будут отображаться неправильно или вообще не будут отображаться.</span><span class="sxs-lookup"><span data-stu-id="b3232-551">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="b3232-552">Чтобы исправить затронутые файлы, используйте chmod и chown для повторного применения метаданных.</span><span class="sxs-lookup"><span data-stu-id="b3232-552">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="b3232-553">Устранена проблема с несколькими сигналами и перезапускаемыми вызовами syscall.</span><span class="sxs-lookup"><span data-stu-id="b3232-553">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="b3232-554">Консоль</span><span class="sxs-lookup"><span data-stu-id="b3232-554">Console</span></span>
* <span data-ttu-id="b3232-555">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="b3232-555">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-556">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-556">LTP Results:</span></span>
<span data-ttu-id="b3232-557">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="b3232-557">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="b3232-558">Сборка 17063</span><span class="sxs-lookup"><span data-stu-id="b3232-558">Build 17063</span></span>
<span data-ttu-id="b3232-559">Общие сведения о сборке Windows 17063 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span><span class="sxs-lookup"><span data-stu-id="b3232-559">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b3232-560">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-560">WSL</span></span>
* <span data-ttu-id="b3232-561">DrvFs поддерживает дополнительные метаданные Linux.</span><span class="sxs-lookup"><span data-stu-id="b3232-561">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="b3232-562">Это позволяет задать владельца и режим файлов с помощью chmod или chown, а также создать специальные файлы, такие как FIFO, сокеты UNIX и файлы устройств.</span><span class="sxs-lookup"><span data-stu-id="b3232-562">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="b3232-563">Сейчас эта функция отключена по умолчанию, так как еще является экспериментальной.</span><span class="sxs-lookup"><span data-stu-id="b3232-563">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="b3232-564">**Примечание.**  Исправлена ошибка в формате метаданных, используемом DrvFs.</span><span class="sxs-lookup"><span data-stu-id="b3232-564">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="b3232-565">Хотя метаданные используются в этой сборке в качестве эксперимента, будущие сборки не будут правильно считывать метаданные, созданные этой сборкой.</span><span class="sxs-lookup"><span data-stu-id="b3232-565">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="b3232-566">Возможно, потребуется вручную обновить владельца измененных файлов, а устройства с пользовательским идентификатором устройства потребуется создать заново.</span><span class="sxs-lookup"><span data-stu-id="b3232-566">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="b3232-567">Чтобы включить эту функцию, подключите DrvFs с параметром metadata (чтобы включить эту функцию для существующего подключения, его необходимо сначала отключить):</span><span class="sxs-lookup"><span data-stu-id="b3232-567">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="b3232-568">Разрешения Linux добавляются в файл в качестве дополнительных метаданных; они не влияют на разрешения Windows.</span><span class="sxs-lookup"><span data-stu-id="b3232-568">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="b3232-569">Помните, что изменение файла с помощью редактора Windows может привести к удалению метаданных.</span><span class="sxs-lookup"><span data-stu-id="b3232-569">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="b3232-570">В этом случае будут восстановлены разрешения этого файла по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b3232-570">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="b3232-571">Добавлены параметры подключения к DrvFs для управления файлами без метаданных.</span><span class="sxs-lookup"><span data-stu-id="b3232-571">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="b3232-572">uid: идентификатор пользователя, используемый для владельца всех файлов.</span><span class="sxs-lookup"><span data-stu-id="b3232-572">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="b3232-573">gid: идентификатор группы, используемый для владельца всех файлов.</span><span class="sxs-lookup"><span data-stu-id="b3232-573">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="b3232-574">umask: восьмеричная маска разрешений, исключаемых для всех файлов и каталогов.</span><span class="sxs-lookup"><span data-stu-id="b3232-574">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="b3232-575">fmask: восьмеричная маска разрешений, исключаемых для всех обычных файлов.</span><span class="sxs-lookup"><span data-stu-id="b3232-575">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="b3232-576">dmask: восьмеричная маска разрешений, исключаемых для всех каталогов.</span><span class="sxs-lookup"><span data-stu-id="b3232-576">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="b3232-577">Например:</span><span class="sxs-lookup"><span data-stu-id="b3232-577">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="b3232-578">Используйте вместе с параметром metadata, чтобы указать разрешения по умолчанию для файлов без метаданных.</span><span class="sxs-lookup"><span data-stu-id="b3232-578">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="b3232-579">Появилась новая переменная среды, `WSLENV`, позволяющая настроить поток переменных среды между WSL и Win32.</span><span class="sxs-lookup"><span data-stu-id="b3232-579">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="b3232-580">Например:</span><span class="sxs-lookup"><span data-stu-id="b3232-580">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="b3232-581">`WSLENV` — разделенный двоеточиями список переменных среды, которые могут быть добавлены при запуске процессов WSL из Win32 или при запуске процессов Win32 из WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-581">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="b3232-582">Каждая переменная может иметь суффикс с косой чертой, за которой следуют флаги для указания способа преобразования.</span><span class="sxs-lookup"><span data-stu-id="b3232-582">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="b3232-583">p: значение — это путь, который должен быть преобразован между WSL и Win32.</span><span class="sxs-lookup"><span data-stu-id="b3232-583">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="b3232-584">l: значение — это список путей.</span><span class="sxs-lookup"><span data-stu-id="b3232-584">l: The value is a list of paths.</span></span> <span data-ttu-id="b3232-585">В WSL это список, разделенный двоеточиями.</span><span class="sxs-lookup"><span data-stu-id="b3232-585">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="b3232-586">В Win32 это список, разделенный точками с запятой.</span><span class="sxs-lookup"><span data-stu-id="b3232-586">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="b3232-587">u: это значение должно добавляться только при вызове WSL из Win32.</span><span class="sxs-lookup"><span data-stu-id="b3232-587">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="b3232-588">w: это значение должно добавляться только при вызове Win32 из WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-588">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="b3232-589">Вы можете задать `WSLENV` в bashrc или в пользовательской среде Windows для пользователя.</span><span class="sxs-lookup"><span data-stu-id="b3232-589">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="b3232-590">Подключения DrvFs правильно сохраняют метки времени из tar, cp -p (GH 1939).</span><span class="sxs-lookup"><span data-stu-id="b3232-590">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="b3232-591">Символические ссылки DrvFs сообщают правильный размер (GH 2641).</span><span class="sxs-lookup"><span data-stu-id="b3232-591">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="b3232-592">Операции чтения и записи могут обрабатывать очень большие объемы ввода-вывода (GH 2653).</span><span class="sxs-lookup"><span data-stu-id="b3232-592">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="b3232-593">Функция waitpid работает с идентификаторами групп процессов (GH 2534).</span><span class="sxs-lookup"><span data-stu-id="b3232-593">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="b3232-594">Значительно улучшена производительность mmap для больших резервных регионов. Повышена производительность ghc (GH 1671).</span><span class="sxs-lookup"><span data-stu-id="b3232-594">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="b3232-595">Personality поддерживает READ_IMPLIES_EXEC; реализованы исправления для maxima и clisp (GH 1185).</span><span class="sxs-lookup"><span data-stu-id="b3232-595">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="b3232-596">Mprotect поддерживает PROT_GROWSDOWN; реализованы исправления для clisp (GH 1128).</span><span class="sxs-lookup"><span data-stu-id="b3232-596">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="b3232-597">Устранены сбои страниц в режиме перегрузки; реализованы исправления для sbcl (GH 1128).</span><span class="sxs-lookup"><span data-stu-id="b3232-597">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="b3232-598">Функция clone поддерживает больше сочетаний флагов.</span><span class="sxs-lookup"><span data-stu-id="b3232-598">clone supports more flags combinations</span></span>
* <span data-ttu-id="b3232-599">Поддержка select/epoll для файлов epoll (ранее это считалось холостой командой).</span><span class="sxs-lookup"><span data-stu-id="b3232-599">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="b3232-600">Уведомление ptrace о нереализованных вызовах syscall.</span><span class="sxs-lookup"><span data-stu-id="b3232-600">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="b3232-601">Игнорирование интерфейсов, которые не выполняются, при создании серверов имен resolv.conf [GH 2694].</span><span class="sxs-lookup"><span data-stu-id="b3232-601">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="b3232-602">Перечисление сетевых интерфейсов без физического адреса.</span><span class="sxs-lookup"><span data-stu-id="b3232-602">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="b3232-603">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="b3232-603">[GH 2685]</span></span>
* <span data-ttu-id="b3232-604">Дополнительные исправления ошибок и улучшения.</span><span class="sxs-lookup"><span data-stu-id="b3232-604">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="b3232-605">Инструменты Linux, доступные для разработчиков в Windows</span><span class="sxs-lookup"><span data-stu-id="b3232-605">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="b3232-606">Цепочка инструментов командной строки Windows включает в себя bsdtar (tar) и curl.</span><span class="sxs-lookup"><span data-stu-id="b3232-606">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="b3232-607">Ознакомьтесь с [этим блогом](https://aka.ms/tarcurlwindows), чтобы узнать больше о добавлении этих двух новых инструментов и о том, как они изменяют разработку в Windows.</span><span class="sxs-lookup"><span data-stu-id="b3232-607">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="b3232-608">`AF_UNIX` доступен в пакете SDK для программы предварительной оценки Windows (начиная со сборки 17061).</span><span class="sxs-lookup"><span data-stu-id="b3232-608">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="b3232-609">Ознакомьтесь с [этим блогом](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/), чтобы узнать больше о `AF_UNIX` и способах его использования разработчиками в Windows.</span><span class="sxs-lookup"><span data-stu-id="b3232-609">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="b3232-610">Консоль</span><span class="sxs-lookup"><span data-stu-id="b3232-610">Console</span></span>
* <span data-ttu-id="b3232-611">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="b3232-611">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-612">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-612">LTP Results:</span></span>
<span data-ttu-id="b3232-613">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="b3232-613">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="b3232-614">Сборка 17046</span><span class="sxs-lookup"><span data-stu-id="b3232-614">Build 17046</span></span>

<span data-ttu-id="b3232-615">Общие сведения о сборке Windows 17046 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span><span class="sxs-lookup"><span data-stu-id="b3232-615">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="b3232-616">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-616">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b3232-617">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-617">WSL</span></span>
- <span data-ttu-id="b3232-618">Разрешено выполнение процессов без активного терминала.</span><span class="sxs-lookup"><span data-stu-id="b3232-618">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="b3232-619">[GH 709, 1007, 1511, 2252, 2391 и т. д.]</span><span class="sxs-lookup"><span data-stu-id="b3232-619">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="b3232-620">Улучшена поддержка CLONE_VFORK и CLONE_VM.</span><span class="sxs-lookup"><span data-stu-id="b3232-620">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="b3232-621">[GH 1878, 2615]</span><span class="sxs-lookup"><span data-stu-id="b3232-621">[GH 1878, 2615]</span></span>
- <span data-ttu-id="b3232-622">Пропуск драйверов фильтра TDI для сетевых операций WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-622">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="b3232-623">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="b3232-623">[GH 1554]</span></span>
- <span data-ttu-id="b3232-624">DrvFs создает символические ссылки NT при выполнении определенных условий.</span><span class="sxs-lookup"><span data-stu-id="b3232-624">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="b3232-625">[GH 353, 1475, 2602]</span><span class="sxs-lookup"><span data-stu-id="b3232-625">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="b3232-626">Цель ссылки должна быть относительной, не должна пересекать точки подключения или символические ссылки и должна существовать.</span><span class="sxs-lookup"><span data-stu-id="b3232-626">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="b3232-627">Пользователь должен иметь разрешение SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (обычно для этого требуется запустить wsl.exe с повышенными привилегиями), если режим разработчика не включен.</span><span class="sxs-lookup"><span data-stu-id="b3232-627">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="b3232-628">Во всех остальных случаях DrvFs по-прежнему создает символические ссылки WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-628">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="b3232-629">Разрешено одновременное выполнение экземпляров WSL с повышенными привилегиями и без повышенных привилегий.</span><span class="sxs-lookup"><span data-stu-id="b3232-629">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="b3232-630">Поддержка /proc/sys/kernel/yama/ptrace_scope.</span><span class="sxs-lookup"><span data-stu-id="b3232-630">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="b3232-631">Добавлена функция wslpath для преобразования путей WSL в пути Windows и наоборот.</span><span class="sxs-lookup"><span data-stu-id="b3232-631">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="b3232-632">[GH 522, 1243, 1834, 2327 и т. д.]</span><span class="sxs-lookup"><span data-stu-id="b3232-632">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="b3232-633">Консоль</span><span class="sxs-lookup"><span data-stu-id="b3232-633">Console</span></span>
- <span data-ttu-id="b3232-634">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="b3232-634">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-635">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-635">LTP Results:</span></span>
<span data-ttu-id="b3232-636">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="b3232-636">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="b3232-637">Сборка 17040</span><span class="sxs-lookup"><span data-stu-id="b3232-637">Build 17040</span></span>

<span data-ttu-id="b3232-638">Общие сведения о сборке Windows 17040 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span><span class="sxs-lookup"><span data-stu-id="b3232-638">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-639">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-639">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b3232-640">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-640">WSL</span></span>
- <span data-ttu-id="b3232-641">Исправления с момента выпуска сборки 17035 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="b3232-641">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="b3232-642">Консоль</span><span class="sxs-lookup"><span data-stu-id="b3232-642">Console</span></span>
- <span data-ttu-id="b3232-643">Исправления с момента выпуска сборки 17035 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="b3232-643">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-644">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-644">LTP Results:</span></span>
<span data-ttu-id="b3232-645">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="b3232-645">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="b3232-646">Сборка 17035</span><span class="sxs-lookup"><span data-stu-id="b3232-646">Build 17035</span></span>

<span data-ttu-id="b3232-647">Общие сведения о сборке Windows 17035 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span><span class="sxs-lookup"><span data-stu-id="b3232-647">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-648">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-648">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b3232-649">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-649">WSL</span></span>
- <span data-ttu-id="b3232-650">Иногда не удавалось получить доступ к файлам в DrvFs с ошибкой EINVAL.</span><span class="sxs-lookup"><span data-stu-id="b3232-650">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="b3232-651">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="b3232-651">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="b3232-652">Консоль</span><span class="sxs-lookup"><span data-stu-id="b3232-652">Console</span></span>
- <span data-ttu-id="b3232-653">Устранена небольшая потеря цветов при вставке или удалении строк в режиме VT.</span><span class="sxs-lookup"><span data-stu-id="b3232-653">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-654">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-654">LTP Results:</span></span>
<span data-ttu-id="b3232-655">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="b3232-655">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="b3232-656">Сборка 17025</span><span class="sxs-lookup"><span data-stu-id="b3232-656">Build 17025</span></span>

<span data-ttu-id="b3232-657">Общие сведения о сборке Windows 17025 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span><span class="sxs-lookup"><span data-stu-id="b3232-657">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-658">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-658">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b3232-659">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-659">WSL</span></span>
- <span data-ttu-id="b3232-660">Запуск начальных процессов в новой группе процессов переднего плана [GH 1653, 2510].</span><span class="sxs-lookup"><span data-stu-id="b3232-660">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="b3232-661">Исправления доставки SIGHUP [GH 2496].</span><span class="sxs-lookup"><span data-stu-id="b3232-661">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="b3232-662">Создание имени виртуального моста по умолчанию, если оно не указано [GH 2497].</span><span class="sxs-lookup"><span data-stu-id="b3232-662">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="b3232-663">Реализовано /proc/sys/kernel/Random/boot_id [GH 2518].</span><span class="sxs-lookup"><span data-stu-id="b3232-663">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="b3232-664">Дополнительные исправления взаимодействия с каналом stdout/stderr.</span><span class="sxs-lookup"><span data-stu-id="b3232-664">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="b3232-665">Заглушка системного вызова syncfs.</span><span class="sxs-lookup"><span data-stu-id="b3232-665">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="b3232-666">Консоль</span><span class="sxs-lookup"><span data-stu-id="b3232-666">Console</span></span>
- <span data-ttu-id="b3232-667">Исправление входного преобразования VT для консолей сторонних разработчиков [GH 111].</span><span class="sxs-lookup"><span data-stu-id="b3232-667">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-668">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-668">LTP Results:</span></span>
<span data-ttu-id="b3232-669">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="b3232-669">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="b3232-670">Сборка 17017</span><span class="sxs-lookup"><span data-stu-id="b3232-670">Build 17017</span></span>

<span data-ttu-id="b3232-671">Общие сведения о сборке Windows 17017 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span><span class="sxs-lookup"><span data-stu-id="b3232-671">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-672">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-672">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b3232-673">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-673">WSL</span></span>
- <span data-ttu-id="b3232-674">Пропуск пустых заголовков программы ELF [GH 330].</span><span class="sxs-lookup"><span data-stu-id="b3232-674">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="b3232-675">LxssManager разрешено создавать экземпляры WSL для неинтерактивных пользователей (поддержка SSH и запланированных задач) [GH 777, 1602].</span><span class="sxs-lookup"><span data-stu-id="b3232-675">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="b3232-676">Поддержка сценариев WSL > Win32 > WSL ("порождение") [GH 1228].</span><span class="sxs-lookup"><span data-stu-id="b3232-676">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="b3232-677">Ограниченная поддержка завершения работы консольных приложений, вызванных посредством взаимодействия [GH 1614].</span><span class="sxs-lookup"><span data-stu-id="b3232-677">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="b3232-678">Поддержка параметров подключения для devpts [GH 1948].</span><span class="sxs-lookup"><span data-stu-id="b3232-678">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="b3232-679">Устранена блокировка Ptrace запуска дочерних процессов [GH 2333].</span><span class="sxs-lookup"><span data-stu-id="b3232-679">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="b3232-680">В EPOLLET отсутствовали некоторые события [GH 2462].</span><span class="sxs-lookup"><span data-stu-id="b3232-680">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="b3232-681">PTRACE_GETSIGINFO возвращает больше данных.</span><span class="sxs-lookup"><span data-stu-id="b3232-681">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="b3232-682">Функция getdents с lseek выдавала неправильные результаты.</span><span class="sxs-lookup"><span data-stu-id="b3232-682">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="b3232-683">Устранены некоторые сценарии, в которых взаимодействующее приложение Win32 переставало отвечать на запросы, ожидая входных данных в канале, который больше не содержал данные.</span><span class="sxs-lookup"><span data-stu-id="b3232-683">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="b3232-684">Поддержка O_ASYNC для файлов tty и pty.</span><span class="sxs-lookup"><span data-stu-id="b3232-684">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="b3232-685">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="b3232-685">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="b3232-686">Консоль</span><span class="sxs-lookup"><span data-stu-id="b3232-686">Console</span></span>
- <span data-ttu-id="b3232-687">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="b3232-687">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-688">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-688">LTP Results:</span></span>
<span data-ttu-id="b3232-689">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="b3232-689">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="b3232-690">Обновление Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="b3232-690">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="b3232-691">Сборка 16288</span><span class="sxs-lookup"><span data-stu-id="b3232-691">Build 16288</span></span>

<span data-ttu-id="b3232-692">Общие сведения о сборке Windows 16288 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span><span class="sxs-lookup"><span data-stu-id="b3232-692">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-693">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-693">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b3232-694">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-694">WSL</span></span>
- <span data-ttu-id="b3232-695">Правильная инициализация и отображение UID, GID и режима для дескрипторов файлов сокетов [GH 2490].</span><span class="sxs-lookup"><span data-stu-id="b3232-695">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="b3232-696">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="b3232-696">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="b3232-697">Консоль</span><span class="sxs-lookup"><span data-stu-id="b3232-697">Console</span></span>
- <span data-ttu-id="b3232-698">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="b3232-698">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-699">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-699">LTP Results:</span></span>
<span data-ttu-id="b3232-700">Изменения с момента выпуска сборки 16273 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="b3232-700">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="b3232-701">Сборка 16278</span><span class="sxs-lookup"><span data-stu-id="b3232-701">Build 16278</span></span>

<span data-ttu-id="b3232-702">Общие сведения о сборке Windows 162738 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span><span class="sxs-lookup"><span data-stu-id="b3232-702">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-703">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-703">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b3232-704">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-704">WSL</span></span>
- <span data-ttu-id="b3232-705">Явная отмена сопоставления сопоставленных представлений разделов с файлами при завершении состояния LX MM [GH 2415].</span><span class="sxs-lookup"><span data-stu-id="b3232-705">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="b3232-706">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="b3232-706">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="b3232-707">Консоль</span><span class="sxs-lookup"><span data-stu-id="b3232-707">Console</span></span>
- <span data-ttu-id="b3232-708">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="b3232-708">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-709">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-709">LTP Results:</span></span>
<span data-ttu-id="b3232-710">Изменения с момента выпуска сборки 16273 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="b3232-710">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="b3232-711">Сборка 16275</span><span class="sxs-lookup"><span data-stu-id="b3232-711">Build 16275</span></span>

<span data-ttu-id="b3232-712">Общие сведения о сборке Windows 162735 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span><span class="sxs-lookup"><span data-stu-id="b3232-712">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-713">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-713">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b3232-714">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-714">WSL</span></span>
- <span data-ttu-id="b3232-715">В этом выпуске нет изменений, связанных с WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-715">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="b3232-716">Консоль</span><span class="sxs-lookup"><span data-stu-id="b3232-716">Console</span></span>
- <span data-ttu-id="b3232-717">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="b3232-717">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-718">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-718">LTP Results:</span></span>
<span data-ttu-id="b3232-719">Изменения с момента выпуска сборки 16273 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="b3232-719">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="b3232-720">Сборка 16273</span><span class="sxs-lookup"><span data-stu-id="b3232-720">Build 16273</span></span>

<span data-ttu-id="b3232-721">Общие сведения о сборке Windows 16273 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span><span class="sxs-lookup"><span data-stu-id="b3232-721">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-722">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-722">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b3232-723">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-723">WSL</span></span>
- <span data-ttu-id="b3232-724">Исправлена проблема, из-за которой DrvFs иногда сообщал о неправильном типе файла для каталогов [GH 2392].</span><span class="sxs-lookup"><span data-stu-id="b3232-724">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="b3232-725">Разрешено создание сокетов NETLINK_KOBJECT_UEVENT для разблокирования программ, использующих uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637].</span><span class="sxs-lookup"><span data-stu-id="b3232-725">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="b3232-726">Добавлена поддержка неблокирующего подключения [GH 903, 1391, 1584, 1585, 1829, 2290, 2314].</span><span class="sxs-lookup"><span data-stu-id="b3232-726">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="b3232-727">Реализован флаг системного вызова клонирования CLONE_FS [GH 2242].</span><span class="sxs-lookup"><span data-stu-id="b3232-727">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="b3232-728">Устранены проблемы, связанные с неправильной обработкой знаков табуляции или кавычек при взаимодействии с NT [GH 1625, 2164].</span><span class="sxs-lookup"><span data-stu-id="b3232-728">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="b3232-729">Устранена ошибка отказа в доступе при попытке повторного запуска экземпляров WSL [GH 651, 2095].</span><span class="sxs-lookup"><span data-stu-id="b3232-729">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="b3232-730">Реализованы фьютексные операции FUTEX_REQUEUE и FUTEX_CMP_REQUEUE [GH 2242].</span><span class="sxs-lookup"><span data-stu-id="b3232-730">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="b3232-731">Исправлены разрешения для различных файлов SysFs [GH 2214].</span><span class="sxs-lookup"><span data-stu-id="b3232-731">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="b3232-732">Устранена проблема, из-за которой стек Haskell переставал отвечать на запросы во время установки [GH 2290].</span><span class="sxs-lookup"><span data-stu-id="b3232-732">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="b3232-733">Реализованы флаги binfmt_misc "C", "O" и "P" [GH 2103].</span><span class="sxs-lookup"><span data-stu-id="b3232-733">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="b3232-734">Добавлены /proc/sys/kernel, /shmmax, /shmmni и /threads-max [GH 1753].</span><span class="sxs-lookup"><span data-stu-id="b3232-734">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="b3232-735">Добавлена частичная поддержка системного вызова ioprio_set [GH 498].</span><span class="sxs-lookup"><span data-stu-id="b3232-735">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="b3232-736">Реализована заглушка SO_REUSEPORT и добавлена поддержка SO_PASSCRED для сокетов NETLINK [GH 69].</span><span class="sxs-lookup"><span data-stu-id="b3232-736">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="b3232-737">Возвращение разных кодов ошибок из RegisterDistribuiton, если дистрибутив в данный момент устанавливается или удаляется.</span><span class="sxs-lookup"><span data-stu-id="b3232-737">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="b3232-738">Обеспечена отмена регистрации частично установленных дистрибутивов WSL с помощью wslconfig.exe.</span><span class="sxs-lookup"><span data-stu-id="b3232-738">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="b3232-739">Устранена ошибка, из-за которой сокет Python переставал отвечать на запросы при выполнении udp::msg_peek.</span><span class="sxs-lookup"><span data-stu-id="b3232-739">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="b3232-740">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="b3232-740">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="b3232-741">Консоль</span><span class="sxs-lookup"><span data-stu-id="b3232-741">Console</span></span>
- <span data-ttu-id="b3232-742">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="b3232-742">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-743">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-743">LTP Results:</span></span>
<span data-ttu-id="b3232-744">Всего тестов: 1904.</span><span class="sxs-lookup"><span data-stu-id="b3232-744">Total Tests: 1904</span></span><br/>
<span data-ttu-id="b3232-745">Всего пропущенных тестов: 209.</span><span class="sxs-lookup"><span data-stu-id="b3232-745">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="b3232-746">Всего сбоев: 229.</span><span class="sxs-lookup"><span data-stu-id="b3232-746">Total Failures: 229</span></span><br/>
[<span data-ttu-id="b3232-747">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="b3232-747">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="b3232-748">Сборка 16257</span><span class="sxs-lookup"><span data-stu-id="b3232-748">Build 16257</span></span>

<span data-ttu-id="b3232-749">Общие сведения о сборке Windows 16257 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span><span class="sxs-lookup"><span data-stu-id="b3232-749">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-750">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-750">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b3232-751">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-751">WSL</span></span>
- <span data-ttu-id="b3232-752">Реализован системный вызов prlimit64.</span><span class="sxs-lookup"><span data-stu-id="b3232-752">Implement prlimit64 system call</span></span>
- <span data-ttu-id="b3232-753">Добавлена поддержка ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688].</span><span class="sxs-lookup"><span data-stu-id="b3232-753">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="b3232-754">Заглушка MSG_MORE для TCP-сокетов [GH 2351].</span><span class="sxs-lookup"><span data-stu-id="b3232-754">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="b3232-755">Исправлено недопустимое поведение вспомогательного вектора AT_EXECFN [GH 2133].</span><span class="sxs-lookup"><span data-stu-id="b3232-755">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="b3232-756">Исправлено поведение копирования и вставки для консоли и tty и добавлена улучшенная обработка полного буфера [GH 2204, 2131].</span><span class="sxs-lookup"><span data-stu-id="b3232-756">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="b3232-757">Установка AT_SECURE в дополнительном векторе для программ set-user-ID и set-group-ID [GH 2031].</span><span class="sxs-lookup"><span data-stu-id="b3232-757">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="b3232-758">Главная конечная точка псевдотерминала не обрабатывала TIOCPGRP [GH 1063].</span><span class="sxs-lookup"><span data-stu-id="b3232-758">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="b3232-759">Исправлена проблема lseek с перемоткой каталогов в LxFs [GH 2310].</span><span class="sxs-lookup"><span data-stu-id="b3232-759">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="b3232-760">Исправлена блокировка /dev/ptmx после интенсивного использования [GH 1882].</span><span class="sxs-lookup"><span data-stu-id="b3232-760">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="b3232-761">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="b3232-761">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="b3232-762">Консоль</span><span class="sxs-lookup"><span data-stu-id="b3232-762">Console</span></span>
- <span data-ttu-id="b3232-763">Исправлено отображение горизонтальных линий и знаков подчеркивания везде [GH 2168].</span><span class="sxs-lookup"><span data-stu-id="b3232-763">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="b3232-764">Исправлено изменение порядка процессов, усложнявшее закрытие NPM [GH 2170].</span><span class="sxs-lookup"><span data-stu-id="b3232-764">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="b3232-765">Добавлена новая цветовая схема: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/.</span><span class="sxs-lookup"><span data-stu-id="b3232-765">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-766">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-766">LTP Results:</span></span>
<span data-ttu-id="b3232-767">Изменения с момента выпуска сборки 16251 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="b3232-767">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b3232-768">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="b3232-768">Syscall Support</span></span>
<span data-ttu-id="b3232-769">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-769">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b3232-770">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="b3232-770">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="b3232-771">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="b3232-771">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[<span data-ttu-id="b3232-772">Проблема GitHub 2392: WSL не распознает папки Windows…</span><span class="sxs-lookup"><span data-stu-id="b3232-772">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="b3232-773">В сборке 16257 в WSL возникли проблемы при перечислении файлов и папок Windows с помощью `/mnt/c/...`.</span><span class="sxs-lookup"><span data-stu-id="b3232-773">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="b3232-774">Эта проблема устранена, и исправление будет выпущено в сборке для программы предварительной оценки в течение недели после 14 августа 2017 года.</span><span class="sxs-lookup"><span data-stu-id="b3232-774">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="b3232-775">Сборка 16251</span><span class="sxs-lookup"><span data-stu-id="b3232-775">Build 16251</span></span>

<span data-ttu-id="b3232-776">Общие сведения о сборке Windows 16251 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span><span class="sxs-lookup"><span data-stu-id="b3232-776">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-777">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-777">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b3232-778">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-778">WSL</span></span>
- <span data-ttu-id="b3232-779">Удален тег бета-версии из дополнительного компонента WSL. Дополнительные сведения см. в этой [записи блога](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/).</span><span class="sxs-lookup"><span data-stu-id="b3232-779">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="b3232-780">Правильная инициализация сохраненных заданных UID и GID для двоичных файлов set-user-ID и set-group-ID при выполнении [GH 962, 1415, 2072].</span><span class="sxs-lookup"><span data-stu-id="b3232-780">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="b3232-781">Добавлена поддержка PTRACE_O_TRACEEXIT в ptrace [GH 555].</span><span class="sxs-lookup"><span data-stu-id="b3232-781">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="b3232-782">В ptrace добавлена поддержка PTRACE_GETFPREGS и PTRACE_GETREGSET с NT_FPREGSET [GH 555].</span><span class="sxs-lookup"><span data-stu-id="b3232-782">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="b3232-783">Исправлена проблема, из-за которой выполнение ptrace останавливалось на пропущенных сигналах.</span><span class="sxs-lookup"><span data-stu-id="b3232-783">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="b3232-784">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="b3232-784">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="b3232-785">Консоль</span><span class="sxs-lookup"><span data-stu-id="b3232-785">Console</span></span>
- <span data-ttu-id="b3232-786">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="b3232-786">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-787">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-787">LTP Results:</span></span>
<span data-ttu-id="b3232-788">Число пройденных тестов: 768</span><span class="sxs-lookup"><span data-stu-id="b3232-788">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="b3232-789">Число непройденных тестов: 244.</span><span class="sxs-lookup"><span data-stu-id="b3232-789">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="b3232-790">Число пропущенных тестов: 96</span><span class="sxs-lookup"><span data-stu-id="b3232-790">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="b3232-791">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="b3232-791">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="b3232-792">Сборка 16241</span><span class="sxs-lookup"><span data-stu-id="b3232-792">Build 16241</span></span>

<span data-ttu-id="b3232-793">Общие сведения о сборке Windows 16241 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span><span class="sxs-lookup"><span data-stu-id="b3232-793">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-794">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-794">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b3232-795">WSL</span><span class="sxs-lookup"><span data-stu-id="b3232-795">WSL</span></span>
- <span data-ttu-id="b3232-796">В этом выпуске нет изменений, связанных с WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-796">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="b3232-797">Консоль</span><span class="sxs-lookup"><span data-stu-id="b3232-797">Console</span></span>
- <span data-ttu-id="b3232-798">Исправлено вывода неправильного знака для пересечения линий DEC, о котором первоначально было сообщено [здесь](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/).</span><span class="sxs-lookup"><span data-stu-id="b3232-798">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="b3232-799">Исправлено отсутствие вывода текста в кодовой странице 65001 (UTF8).</span><span class="sxs-lookup"><span data-stu-id="b3232-799">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="b3232-800">Изменения, внесенные в значения RGB одного цвета, не переносятся в другие части палитры при изменении выбора.</span><span class="sxs-lookup"><span data-stu-id="b3232-800">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="b3232-801">Это заметно облегчит использование страницы свойств консоли.</span><span class="sxs-lookup"><span data-stu-id="b3232-801">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="b3232-802">Нажатие клавиш Ctrl+S не работало правильно.</span><span class="sxs-lookup"><span data-stu-id="b3232-802">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="b3232-803">Un-Bold и -Dim полностью отсутствуют в escape-кодах ANSI [GH 2174].</span><span class="sxs-lookup"><span data-stu-id="b3232-803">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="b3232-804">Консоль неправильно поддерживала цветовые темы Vim [GH 1706].</span><span class="sxs-lookup"><span data-stu-id="b3232-804">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="b3232-805">Не удавалось вставить определенные знаки [GH 2149].</span><span class="sxs-lookup"><span data-stu-id="b3232-805">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="b3232-806">Изменение размера расплавления приводило к необычному изменению размера окна Bash, когда что-то было введено в строке редактирования или командной строке [GH ConEmu 1123].</span><span class="sxs-lookup"><span data-stu-id="b3232-806">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="b3232-807">Нажатие клавиш CTRL+L не очищало экран [GH 1978].</span><span class="sxs-lookup"><span data-stu-id="b3232-807">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="b3232-808">Устранена ошибка отрисовки консоли при отображении VT в HDPI [GH 1907].</span><span class="sxs-lookup"><span data-stu-id="b3232-808">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="b3232-809">Японские знаки выглядели необычно со знаком Юникода U+30FB [GH 2146].</span><span class="sxs-lookup"><span data-stu-id="b3232-809">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="b3232-810">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="b3232-810">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="b3232-811">Сборка 16237</span><span class="sxs-lookup"><span data-stu-id="b3232-811">Build 16237</span></span>

<span data-ttu-id="b3232-812">Общие сведения о сборке Windows 16237 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span><span class="sxs-lookup"><span data-stu-id="b3232-812">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-813">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-813">Fixed</span></span>
- <span data-ttu-id="b3232-814">Использование атрибутов по умолчанию для файлов без EA в lxfs (root, root, 0000).</span><span class="sxs-lookup"><span data-stu-id="b3232-814">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="b3232-815">Добавлена поддержка дистрибутивов, использующих расширенные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="b3232-815">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="b3232-816">Исправлено заполнение записей, возвращаемых getdents и getdents64.</span><span class="sxs-lookup"><span data-stu-id="b3232-816">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="b3232-817">Исправлена проверка разрешений для системного вызова shmctl SHM_STAT [GH 2068].</span><span class="sxs-lookup"><span data-stu-id="b3232-817">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="b3232-818">Исправлено неправильное начальное состояние epoll для tty [GH 2231].</span><span class="sxs-lookup"><span data-stu-id="b3232-818">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="b3232-819">Устранена проблема в DrvFs, из-за которой команда readdir не возвращала все записи [GH 2077].</span><span class="sxs-lookup"><span data-stu-id="b3232-819">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="b3232-820">Исправлена операция LxFs readdir с несвязанными файлами [GH 2077].</span><span class="sxs-lookup"><span data-stu-id="b3232-820">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="b3232-821">Допускается повторное открытие несвязанных файлов DrvFs с помощью procfs.</span><span class="sxs-lookup"><span data-stu-id="b3232-821">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="b3232-822">Добавлено переопределение глобального раздела реестра для отключения функций WSL (взаимодействие и монтирование дисков).</span><span class="sxs-lookup"><span data-stu-id="b3232-822">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="b3232-823">Исправлено неправильное число блокировок в "stat" для DrvFs (и LxFs) [GH 1894].</span><span class="sxs-lookup"><span data-stu-id="b3232-823">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="b3232-824">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="b3232-824">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="b3232-825">Сборка 16232</span><span class="sxs-lookup"><span data-stu-id="b3232-825">Build 16232</span></span>

<span data-ttu-id="b3232-826">Общие сведения о сборке Windows 16232 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span><span class="sxs-lookup"><span data-stu-id="b3232-826">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-827">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-827">Fixed</span></span>
- <span data-ttu-id="b3232-828">В этом выпуске нет изменений, связанных с WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-828">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="b3232-829">Сборка 16226</span><span class="sxs-lookup"><span data-stu-id="b3232-829">Build 16226</span></span>

<span data-ttu-id="b3232-830">Общие сведения о сборке Windows 16226 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span><span class="sxs-lookup"><span data-stu-id="b3232-830">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-831">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-831">Fixed</span></span>
- <span data-ttu-id="b3232-832">Поддержка системных вызовов, связанных с xattr (getxattr, setxattr, listxattr, removexattr).</span><span class="sxs-lookup"><span data-stu-id="b3232-832">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="b3232-833">Поддержка security.capablity xattr.</span><span class="sxs-lookup"><span data-stu-id="b3232-833">security.capablity xattr support.</span></span>
- <span data-ttu-id="b3232-834">Улучшена совместимость с некоторыми файловыми системами и фильтрами, включая серверы SMB сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="b3232-834">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="b3232-835">[GH 1952]</span><span class="sxs-lookup"><span data-stu-id="b3232-835">[GH #1952]</span></span>
- <span data-ttu-id="b3232-836">Улучшена поддержка заполнителей OneDrive, заполнителей GVFS и сжатых файлов Compact OS.</span><span class="sxs-lookup"><span data-stu-id="b3232-836">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="b3232-837">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="b3232-837">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="b3232-838">Сборка 16215</span><span class="sxs-lookup"><span data-stu-id="b3232-838">Build 16215</span></span>

<span data-ttu-id="b3232-839">Общие сведения о сборке Windows 16215 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span><span class="sxs-lookup"><span data-stu-id="b3232-839">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-840">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-840">Fixed</span></span>
- <span data-ttu-id="b3232-841">Для WSL больше не требуется режим разработчика.</span><span class="sxs-lookup"><span data-stu-id="b3232-841">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="b3232-842">Поддержка соединений каталогов в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="b3232-842">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="b3232-843">Обработка удаления пакетов appx дистрибутивов WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-843">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="b3232-844">Обновление procfs для отображения частных и общих сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="b3232-844">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="b3232-845">В wslconfig.exe добавлена возможность очистки частично установленных или частично удаленных дистрибутивов.</span><span class="sxs-lookup"><span data-stu-id="b3232-845">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="b3232-846">Добавлена поддержка IP_MTU_DISCOVER для TCP-сокетов.</span><span class="sxs-lookup"><span data-stu-id="b3232-846">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="b3232-847">[GH 1639, 2115, 2205]</span><span class="sxs-lookup"><span data-stu-id="b3232-847">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="b3232-848">Вывод семейства протоколов для маршрутов к AF_INADDR.</span><span class="sxs-lookup"><span data-stu-id="b3232-848">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="b3232-849">Улучшения для последовательных устройств [GH 1929].</span><span class="sxs-lookup"><span data-stu-id="b3232-849">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="b3232-850">Сборка 16199</span><span class="sxs-lookup"><span data-stu-id="b3232-850">Build 16199</span></span>

<span data-ttu-id="b3232-851">Общие сведения о сборке Windows 16199 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span><span class="sxs-lookup"><span data-stu-id="b3232-851">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-852">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-852">Fixed</span></span>
- <span data-ttu-id="b3232-853">В этих выпусках нет изменений, связанных с WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-853">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="b3232-854">Сборка 16193</span><span class="sxs-lookup"><span data-stu-id="b3232-854">Build 16193</span></span>

<span data-ttu-id="b3232-855">Общие сведения о сборке Windows 16193 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span><span class="sxs-lookup"><span data-stu-id="b3232-855">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-856">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-856">Fixed</span></span>
- <span data-ttu-id="b3232-857">Исправлено состояние состязания между отправкой SIGCONT и завершением группы потоков [GH 1973].</span><span class="sxs-lookup"><span data-stu-id="b3232-857">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="b3232-858">Устройства tty и pty изменены для передачи FILE_DEVICE_NAMED_PIPE вместо FILE_DEVICE_CONSOLE [GH 1840].</span><span class="sxs-lookup"><span data-stu-id="b3232-858">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="b3232-859">Исправление SSH для IP_OPTIONS.</span><span class="sxs-lookup"><span data-stu-id="b3232-859">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="b3232-860">Подключение DrvFs перемещено в управляющую программу инициализации [GH 1862, 1968, 1767, 1933].</span><span class="sxs-lookup"><span data-stu-id="b3232-860">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="b3232-861">Добавлена поддержка в DrvFs приведенных ниже символических ссылок NT.</span><span class="sxs-lookup"><span data-stu-id="b3232-861">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="b3232-862">Сборка 16184</span><span class="sxs-lookup"><span data-stu-id="b3232-862">Build 16184</span></span>

<span data-ttu-id="b3232-863">Общие сведения о сборке Windows 16184 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span><span class="sxs-lookup"><span data-stu-id="b3232-863">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-864">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-864">Fixed</span></span>
- <span data-ttu-id="b3232-865">Удалена задача обслуживания пакета apt (lxrun.exe /update).</span><span class="sxs-lookup"><span data-stu-id="b3232-865">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="b3232-866">Исправлено отсутствие выходных данных из процессов Windows в Node.js [GH 1840].</span><span class="sxs-lookup"><span data-stu-id="b3232-866">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="b3232-867">Смягчены требования к соответствию в lxcore [GH 1794].</span><span class="sxs-lookup"><span data-stu-id="b3232-867">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="b3232-868">Исправлена обработка флага AT_EMPTY_PATH в ряде системных вызовов.</span><span class="sxs-lookup"><span data-stu-id="b3232-868">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="b3232-869">Исправлена проблема, из-за которой удаление файлов DrvFs с открытыми дескрипторами приводило к неопределенному поведению файла [GH 544, 966, 1357, 1535, 1615].</span><span class="sxs-lookup"><span data-stu-id="b3232-869">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="b3232-870">Теперь /etc/hosts будет наследовать записи из файла hosts Windows (%windir%\System32\Drivers\Etc\hosts) [GH 1495].</span><span class="sxs-lookup"><span data-stu-id="b3232-870">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="b3232-871">Сборка 16179</span><span class="sxs-lookup"><span data-stu-id="b3232-871">Build 16179</span></span>

<span data-ttu-id="b3232-872">Общие сведения о сборке Windows 16179 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span><span class="sxs-lookup"><span data-stu-id="b3232-872">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-873">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-873">Fixed</span></span>
- <span data-ttu-id="b3232-874">На этой неделе изменения в WSL отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="b3232-874">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="b3232-875">Сборка 16176</span><span class="sxs-lookup"><span data-stu-id="b3232-875">Build 16176</span></span>

<span data-ttu-id="b3232-876">Общие сведения о сборке Windows 16176 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span><span class="sxs-lookup"><span data-stu-id="b3232-876">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-877">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-877">Fixed</span></span>

- <span data-ttu-id="b3232-878">[Включена поддержка последовательных устройств](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/).</span><span class="sxs-lookup"><span data-stu-id="b3232-878">[Enabled serial support](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)</span></span>
- <span data-ttu-id="b3232-879">Добавлен параметр IP-сокета IP_OPTIONS [GH 1116].</span><span class="sxs-lookup"><span data-stu-id="b3232-879">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="b3232-880">Реализована функция pwritev (при передаче файла в nginx/PHP-FPM) [GH 1506].</span><span class="sxs-lookup"><span data-stu-id="b3232-880">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="b3232-881">Добавлены параметры IP-сокета IP_MULTICAST_IF и IPV6_MULTICAST_IF [GH 990].</span><span class="sxs-lookup"><span data-stu-id="b3232-881">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="b3232-882">Поддержка параметров сокета IP_MULTICAST_LOOP и IPV6_MULTICAST_LOOP [GH 1678].</span><span class="sxs-lookup"><span data-stu-id="b3232-882">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="b3232-883">Добавлен параметр сокета IP(V6)_MTU для приложений node, traceroute, dig, nslookup, host.</span><span class="sxs-lookup"><span data-stu-id="b3232-883">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="b3232-884">Добавлен параметр IP-сокета IPV6_UNICAST_HOPS.</span><span class="sxs-lookup"><span data-stu-id="b3232-884">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- <span data-ttu-id="b3232-885">[Улучшения файловой системы](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/).</span><span class="sxs-lookup"><span data-stu-id="b3232-885">[Filesystem Improvements](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)</span></span>
    * <span data-ttu-id="b3232-886">Разрешено подключение путей UNC.</span><span class="sxs-lookup"><span data-stu-id="b3232-886">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="b3232-887">Включена поддержка CDFS в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="b3232-887">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="b3232-888">Правильная обработка разрешений для сетевых файловых систем в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="b3232-888">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="b3232-889">Добавлена поддержка удаленных дисков в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="b3232-889">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="b3232-890">Включена поддержка файловой системы FAT в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="b3232-890">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="b3232-891">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="b3232-891">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-892">Результаты LTP</span><span class="sxs-lookup"><span data-stu-id="b3232-892">LTP Results</span></span>
<span data-ttu-id="b3232-893">Изменения с момента выпуска сборки 15042 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="b3232-893">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="b3232-894">Сборка 16170</span><span class="sxs-lookup"><span data-stu-id="b3232-894">Build 16170</span></span>

<span data-ttu-id="b3232-895">Общие сведения о сборке Windows 16170 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span><span class="sxs-lookup"><span data-stu-id="b3232-895">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="b3232-896">Мы опубликовали новую[запись блога](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/), в которой обсуждаем наши усилия по тестированию WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-896">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="b3232-897">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-897">Fixed</span></span>

- <span data-ttu-id="b3232-898">Поддержка параметров сокета IP_ADD_MEMBERSHIP и IPV6_ADD_MEMBERSHIP [GH 1678].</span><span class="sxs-lookup"><span data-stu-id="b3232-898">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="b3232-899">Добавлена поддержка PTRACE_OLDSETOPTIONS.</span><span class="sxs-lookup"><span data-stu-id="b3232-899">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="b3232-900">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="b3232-900">[GH 1692]</span></span>
- <span data-ttu-id="b3232-901">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="b3232-901">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-902">Результаты LTP</span><span class="sxs-lookup"><span data-stu-id="b3232-902">LTP Results</span></span>
<span data-ttu-id="b3232-903">Изменения с момента выпуска сборки 15042 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="b3232-903">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="b3232-904">Сборка 15046 для Windows 10 Creators Update</span><span class="sxs-lookup"><span data-stu-id="b3232-904">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="b3232-905">В обновление Creators Update для Windows 10 больше не планируется добавлять какие-либо исправления или функции WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-905">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="b3232-906">Публикация заметок о выпуске WSL будет возобновлена в ближайшие недели, чтобы охватить дополнения, запланированные в следующих основных версиях в Центре обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="b3232-906">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="b3232-907">Общие сведения о сборке Windows 15046 и будущих выпусках для программы предварительной оценки доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span><span class="sxs-lookup"><span data-stu-id="b3232-907">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="b3232-908">Сборка 15042</span><span class="sxs-lookup"><span data-stu-id="b3232-908">Build 15042</span></span>

<span data-ttu-id="b3232-909">Общие сведения о сборке Windows 15042 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span><span class="sxs-lookup"><span data-stu-id="b3232-909">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-910">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-910">Fixed</span></span>

- <span data-ttu-id="b3232-911">Устранена взаимоблокировка при удалении пути, завершающегося "..".</span><span class="sxs-lookup"><span data-stu-id="b3232-911">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="b3232-912">Устранена проблема, из-за которой функция FIONBIO не возвращала 0 при успешном выполнении [GH 1683].</span><span class="sxs-lookup"><span data-stu-id="b3232-912">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="b3232-913">Устранена проблема с чтением сокетов датаграмм INET нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="b3232-913">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="b3232-914">Устранена возможная взаимоблокировка из-за состояния состязания при поиске DrvFs в DrvFs [GH 1675].</span><span class="sxs-lookup"><span data-stu-id="b3232-914">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="b3232-915">Расширена поддержка вспомогательных данных сокетов UNIX, SCM_CREDENTIALS и SCM_RIGHTS [GH 514, 613, 1326].</span><span class="sxs-lookup"><span data-stu-id="b3232-915">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="b3232-916">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="b3232-916">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-917">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-917">LTP Results:</span></span>
<span data-ttu-id="b3232-918">Число пройденных тестов: 737.</span><span class="sxs-lookup"><span data-stu-id="b3232-918">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="b3232-919">Число непройденных тестов (неудачных, пропущенных и т. д.): 255.</span><span class="sxs-lookup"><span data-stu-id="b3232-919">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="b3232-920">Сборка 15031</span><span class="sxs-lookup"><span data-stu-id="b3232-920">Build 15031</span></span>

<span data-ttu-id="b3232-921">Общие сведения о сборке Windows 15031 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span><span class="sxs-lookup"><span data-stu-id="b3232-921">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-922">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-922">Fixed</span></span>

- <span data-ttu-id="b3232-923">Исправлена ошибка, из-за которой поведение time(2) иногда было неправильным.</span><span class="sxs-lookup"><span data-stu-id="b3232-923">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="b3232-924">Исправлена проблема, из-за которой системный вызов \*SIGPROCMASK мог повредить маску сигнала.</span><span class="sxs-lookup"><span data-stu-id="b3232-924">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="b3232-925">Теперь в уведомлении о создании процесса WSL возвращается полная длина командной строки.</span><span class="sxs-lookup"><span data-stu-id="b3232-925">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="b3232-926">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="b3232-926">[GH 1632]</span></span>
- <span data-ttu-id="b3232-927">Теперь WSL сообщает о выходе из потока посредством ptrace, если GDB перестает отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="b3232-927">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="b3232-928">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="b3232-928">[GH 1196]</span></span>
- <span data-ttu-id="b3232-929">Исправлена ошибка, из-за которой устройства pty переставали отвечать на запросы после интенсивного ввода-вывода tmux.</span><span class="sxs-lookup"><span data-stu-id="b3232-929">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="b3232-930">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="b3232-930">[GH 1358]</span></span>
- <span data-ttu-id="b3232-931">Исправлена проверка времени ожидания во многих системных вызовах (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create).</span><span class="sxs-lookup"><span data-stu-id="b3232-931">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="b3232-932">Добавлена поддержка eventfd EFD_SEMAPHORE [GH 452].</span><span class="sxs-lookup"><span data-stu-id="b3232-932">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="b3232-933">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="b3232-933">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-934">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-934">LTP Results:</span></span>
<span data-ttu-id="b3232-935">Число пройденных тестов: 737.</span><span class="sxs-lookup"><span data-stu-id="b3232-935">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="b3232-936">Число непройденных тестов (неудачных, пропущенных и т. д.): 255.</span><span class="sxs-lookup"><span data-stu-id="b3232-936">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="b3232-937">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="b3232-937">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="b3232-938">Сборка 15025</span><span class="sxs-lookup"><span data-stu-id="b3232-938">Build 15025</span></span>

<span data-ttu-id="b3232-939">Общие сведения о сборке Windows 15025 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span><span class="sxs-lookup"><span data-stu-id="b3232-939">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-940">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-940">Fixed</span></span>

- <span data-ttu-id="b3232-941">Исправлена ошибка, которая нарушала работу grep 2.27 [GH 1578].</span><span class="sxs-lookup"><span data-stu-id="b3232-941">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="b3232-942">Реализован флаг EFD_SEMAPHORE для системного вызова eventfd2 [GH 452].</span><span class="sxs-lookup"><span data-stu-id="b3232-942">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="b3232-943">Реализован файл /proc/[pid]/net/ipv6_route [GH 1608].</span><span class="sxs-lookup"><span data-stu-id="b3232-943">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="b3232-944">Поддержка управляемого сигналами ввода-вывода для сокетов потоков UNIX [GH 393, 68].</span><span class="sxs-lookup"><span data-stu-id="b3232-944">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="b3232-945">Поддержка F_GETPIPE_SZ и F_SETPIPE_SZ [GH 1012].</span><span class="sxs-lookup"><span data-stu-id="b3232-945">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="b3232-946">Реализация системного вызова recvmmsg() [GH 1531].</span><span class="sxs-lookup"><span data-stu-id="b3232-946">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="b3232-947">Исправлена ошибка, из-за которой функция epoll_wait() не ожидала выполнения [GH 1609].</span><span class="sxs-lookup"><span data-stu-id="b3232-947">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="b3232-948">Реализация /proc/version_signature.</span><span class="sxs-lookup"><span data-stu-id="b3232-948">Implement /proc/version_signature</span></span>
- <span data-ttu-id="b3232-949">Теперь системный вызов Tee возвращает ошибку, если оба дескриптора файла ссылаются на один и тот же канал.</span><span class="sxs-lookup"><span data-stu-id="b3232-949">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="b3232-950">Реализовано правильное поведение SO_PEERCRED для сокетов UNIX.</span><span class="sxs-lookup"><span data-stu-id="b3232-950">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="b3232-951">Исправлена недопустимая обработка параметров системного вызова tkill.</span><span class="sxs-lookup"><span data-stu-id="b3232-951">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="b3232-952">Внесены изменения для увеличения производительности DrvFs.</span><span class="sxs-lookup"><span data-stu-id="b3232-952">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="b3232-953">Незначительное исправление блокировки ввода-вывода Ruby.</span><span class="sxs-lookup"><span data-stu-id="b3232-953">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="b3232-954">Исправлена проблема, из-за которой функция recvmsg() возвращала EINVAL для флага MSG_DONTWAIT для сокетов INET [GH 1296].</span><span class="sxs-lookup"><span data-stu-id="b3232-954">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="b3232-955">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="b3232-955">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-956">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-956">LTP Results:</span></span>
<span data-ttu-id="b3232-957">Число пройденных тестов: 732.</span><span class="sxs-lookup"><span data-stu-id="b3232-957">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="b3232-958">Число непройденных тестов (неудачных, пропущенных и т. д.): 255.</span><span class="sxs-lookup"><span data-stu-id="b3232-958">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="b3232-959">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="b3232-959">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="b3232-960">Сборка 15019</span><span class="sxs-lookup"><span data-stu-id="b3232-960">Build 15019</span></span>

<span data-ttu-id="b3232-961">Общие сведения о сборке Windows 15019 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span><span class="sxs-lookup"><span data-stu-id="b3232-961">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-962">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-962">Fixed</span></span>

- <span data-ttu-id="b3232-963">Исправлена ошибка, из-за которой отображались неправильные данные об использовании ЦП в procfs для таких инструментов, как htop [GH 823, 945, 971].</span><span class="sxs-lookup"><span data-stu-id="b3232-963">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="b3232-964">Теперь при вызове Open() с O_TRUNC для существующего файла inotify теперь создает IN_MODIFY до IN_OPEN.</span><span class="sxs-lookup"><span data-stu-id="b3232-964">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="b3232-965">Исправление getsockopt SO_ERROR в сокетах UNIX для включения возможностей postgress [GH 61, 1354].</span><span class="sxs-lookup"><span data-stu-id="b3232-965">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="b3232-966">Реализация /proc/sys/net/core/somaxconn для языка GO.</span><span class="sxs-lookup"><span data-stu-id="b3232-966">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="b3232-967">Теперь фоновая задача обновления пакета apt-get запускается из представления в скрытом режиме.</span><span class="sxs-lookup"><span data-stu-id="b3232-967">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="b3232-968">Очищена область для IPv6-адреса localhost (сбой (Spring-Framework(Java)).</span><span class="sxs-lookup"><span data-stu-id="b3232-968">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="b3232-969">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="b3232-969">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-970">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-970">LTP Results:</span></span>
<span data-ttu-id="b3232-971">Число пройденных тестов: 714.</span><span class="sxs-lookup"><span data-stu-id="b3232-971">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="b3232-972">Число непройденных тестов (неудачных, пропущенных и т. д.): 249.</span><span class="sxs-lookup"><span data-stu-id="b3232-972">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="b3232-973">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="b3232-973">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="b3232-974">Сборка 15014</span><span class="sxs-lookup"><span data-stu-id="b3232-974">Build 15014</span></span>

<span data-ttu-id="b3232-975">Общие сведения о сборке Windows 15014 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="b3232-975">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-976">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-976">Fixed</span></span>

- <span data-ttu-id="b3232-977">Нажатие клавиш CTRL+C теперь работает ожидаемым образом.</span><span class="sxs-lookup"><span data-stu-id="b3232-977">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="b3232-978">Теперь htop и ps auxw показывают правильные данные об использовании ресурсов (GH 516).</span><span class="sxs-lookup"><span data-stu-id="b3232-978">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="b3232-979">Простое преобразование исключений NT в сигналы.</span><span class="sxs-lookup"><span data-stu-id="b3232-979">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="b3232-980">(GH 513)</span><span class="sxs-lookup"><span data-stu-id="b3232-980">(GH #513)</span></span>
- <span data-ttu-id="b3232-981">Теперь при нехватке пространства fallocate завершается ошибкой ENOSPC вместо EINVAL (GH 1571).</span><span class="sxs-lookup"><span data-stu-id="b3232-981">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="b3232-982">Добавлен /proc/sys/kernel/sem.</span><span class="sxs-lookup"><span data-stu-id="b3232-982">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="b3232-983">Реализованы системные вызовы semop и semtimedop.</span><span class="sxs-lookup"><span data-stu-id="b3232-983">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="b3232-984">Устранены ошибки nslookup, связанные с параметрами сокета IP_RECVTOS и IPV6_RECVTCLASS (GH 69).</span><span class="sxs-lookup"><span data-stu-id="b3232-984">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="b3232-985">Поддержка параметров сокета IP_RECVTTL и IPV6_RECVHOPLIMIT.</span><span class="sxs-lookup"><span data-stu-id="b3232-985">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="b3232-986">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="b3232-986">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-987">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-987">LTP Results:</span></span>
<span data-ttu-id="b3232-988">Число пройденных тестов: 709.</span><span class="sxs-lookup"><span data-stu-id="b3232-988">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="b3232-989">Число непройденных тестов (неудачных, пропущенных и т. д.): 255.</span><span class="sxs-lookup"><span data-stu-id="b3232-989">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="b3232-990">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="b3232-990">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="b3232-991">Сводка по системным вызовам</span><span class="sxs-lookup"><span data-stu-id="b3232-991">Syscall Summary</span></span>
<span data-ttu-id="b3232-992">Всего системных вызовов: 384</span><span class="sxs-lookup"><span data-stu-id="b3232-992">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="b3232-993">Всего реализовано: 235.</span><span class="sxs-lookup"><span data-stu-id="b3232-993">Total Implemented: 235</span></span> </br>
<span data-ttu-id="b3232-994">Всего заглушено: 22</span><span class="sxs-lookup"><span data-stu-id="b3232-994">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="b3232-995">Всего не реализовано: 127</span><span class="sxs-lookup"><span data-stu-id="b3232-995">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="b3232-996">Подробная разбивка</span><span class="sxs-lookup"><span data-stu-id="b3232-996">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="b3232-997">Сборка 15007</span><span class="sxs-lookup"><span data-stu-id="b3232-997">Build 15007</span></span>

<span data-ttu-id="b3232-998">Общие сведения о сборке Windows 15007 доступны в [блоге о Windows]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span><span class="sxs-lookup"><span data-stu-id="b3232-998">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="b3232-999">Известная проблема</span><span class="sxs-lookup"><span data-stu-id="b3232-999">Known Issue</span></span>

- <span data-ttu-id="b3232-1000">Существует известная ошибка, из-за которой консоль не распознает некоторые клавиши CTRL+<key>.</span><span class="sxs-lookup"><span data-stu-id="b3232-1000">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="b3232-1001">Сюда входит команда CTRL+C, которая будет функционировать как обычное нажатие клавиши C.</span><span class="sxs-lookup"><span data-stu-id="b3232-1001">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="b3232-1002">Возможное решение. Сопоставьте альтернативную клавишу с клавишами CTRL+C.</span><span class="sxs-lookup"><span data-stu-id="b3232-1002">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="b3232-1003">Например, чтобы сопоставить клавиши CTRL+K с CTRL+C, выполните следующее: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="b3232-1003">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="b3232-1004">Это сопоставление действует в пределах терминала и должно выполняться *при каждом* запуске Bash.</span><span class="sxs-lookup"><span data-stu-id="b3232-1004">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="b3232-1005">Пользователи могут изучить этот параметр, чтобы включить его в `.bashrc`.</span><span class="sxs-lookup"><span data-stu-id="b3232-1005">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="b3232-1006">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-1006">Fixed</span></span>

- <span data-ttu-id="b3232-1007">Исправлена ошибка, из-за которой подсистема WSL потребляла 100 % ресурсов ядра ЦП.</span><span class="sxs-lookup"><span data-stu-id="b3232-1007">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="b3232-1008">Теперь поддерживаются параметры сокета IP_PKTINFO и IPV6_RECVPKTINFO.</span><span class="sxs-lookup"><span data-stu-id="b3232-1008">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="b3232-1009">(GH 851, 987)</span><span class="sxs-lookup"><span data-stu-id="b3232-1009">(GH #851, 987)</span></span>
- <span data-ttu-id="b3232-1010">Усечение физического адреса сетевого интерфейса до 16 байтов в lxcore (GH #1452, 1414, 1343, 468, 308).</span><span class="sxs-lookup"><span data-stu-id="b3232-1010">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="b3232-1011">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="b3232-1011">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-1012">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-1012">LTP Results:</span></span>
<span data-ttu-id="b3232-1013">Число пройденных тестов: 709.</span><span class="sxs-lookup"><span data-stu-id="b3232-1013">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="b3232-1014">Число непройденных тестов (неудачных, пропущенных и т. д.): 255.</span><span class="sxs-lookup"><span data-stu-id="b3232-1014">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="b3232-1015">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="b3232-1015">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="b3232-1016">Сборка 15002</span><span class="sxs-lookup"><span data-stu-id="b3232-1016">Build 15002</span></span>

<span data-ttu-id="b3232-1017">Общие сведения о сборке Windows 15002 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span><span class="sxs-lookup"><span data-stu-id="b3232-1017">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="b3232-1018">Известная проблема</span><span class="sxs-lookup"><span data-stu-id="b3232-1018">Known Issue</span></span>

<span data-ttu-id="b3232-1019">Две известные проблемы:</span><span class="sxs-lookup"><span data-stu-id="b3232-1019">Two known issues:</span></span>
- <span data-ttu-id="b3232-1020">Существует известная ошибка, из-за которой консоль не распознает некоторые клавиши CTRL+<key>.</span><span class="sxs-lookup"><span data-stu-id="b3232-1020">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="b3232-1021">Сюда входит команда CTRL+C, которая будет функционировать как обычное нажатие клавиши C.</span><span class="sxs-lookup"><span data-stu-id="b3232-1021">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="b3232-1022">Возможное решение. Сопоставьте альтернативную клавишу с клавишами CTRL+C.</span><span class="sxs-lookup"><span data-stu-id="b3232-1022">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="b3232-1023">Например, чтобы сопоставить клавиши CTRL+K с CTRL+C, выполните следующее: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="b3232-1023">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="b3232-1024">Это сопоставление действует в пределах терминала и должно выполняться *при каждом* запуске Bash.</span><span class="sxs-lookup"><span data-stu-id="b3232-1024">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="b3232-1025">Пользователи могут изучить этот параметр, чтобы включить его в `.bashrc`.</span><span class="sxs-lookup"><span data-stu-id="b3232-1025">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="b3232-1026">Во время выполнения WSL системный поток потребляет 100 % ресурсов ядра ЦП.</span><span class="sxs-lookup"><span data-stu-id="b3232-1026">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="b3232-1027">Первопричина устранена и исправлена внутри компонента.</span><span class="sxs-lookup"><span data-stu-id="b3232-1027">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="b3232-1028">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-1028">Fixed</span></span>

- <span data-ttu-id="b3232-1029">Все сеансы Bash теперь должны создаваться на одном уровне разрешений.</span><span class="sxs-lookup"><span data-stu-id="b3232-1029">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="b3232-1030">Попытка запустить сеанс на другом уровне будет заблокирована.</span><span class="sxs-lookup"><span data-stu-id="b3232-1030">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="b3232-1031">Это означает, что консоль администратора и консоль пользователя, не являющегося администратором, не могут работать одновременно.</span><span class="sxs-lookup"><span data-stu-id="b3232-1031">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="b3232-1032">(GH 626)</span><span class="sxs-lookup"><span data-stu-id="b3232-1032">(GH #626)</span></span>
<br/>
- <span data-ttu-id="b3232-1033">Реализованы следующие сообщения NETLINK_ROUTE (требуются права администратора Windows):</span><span class="sxs-lookup"><span data-stu-id="b3232-1033">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="b3232-1034">RTM_NEWADDR (поддерживает `ip addr add`);</span><span class="sxs-lookup"><span data-stu-id="b3232-1034">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="b3232-1035">RTM_NEWROUTE (поддерживает `ip route add`);</span><span class="sxs-lookup"><span data-stu-id="b3232-1035">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="b3232-1036">RTM_DELADDR (поддерживает `ip addr del`);</span><span class="sxs-lookup"><span data-stu-id="b3232-1036">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="b3232-1037">RTM_DELROUTE (поддерживает `ip route del`).</span><span class="sxs-lookup"><span data-stu-id="b3232-1037">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="b3232-1038">Проверка запланированных задач для пакетов, которые необходимо обновить, больше не будет выполняться при лимитном подключении (GH 1371).</span><span class="sxs-lookup"><span data-stu-id="b3232-1038">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="b3232-1039">Исправлена ошибка, из-за которой канал переставал отвечать на запросы, например bash -c "ls -alR /" | bash -c "cat" (GH 1214).</span><span class="sxs-lookup"><span data-stu-id="b3232-1039">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="b3232-1040">Реализован параметр сокета TCP_KEEPCNT (GH 843).</span><span class="sxs-lookup"><span data-stu-id="b3232-1040">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="b3232-1041">Реализован параметр сокета INET IP_MTU_DISCOVER (GH 720, 717, 170, 69).</span><span class="sxs-lookup"><span data-stu-id="b3232-1041">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="b3232-1042">Удалены устаревшие функции для запуска двоичных файлов NT из init с помощью поиска по пути NT.</span><span class="sxs-lookup"><span data-stu-id="b3232-1042">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="b3232-1043">(GH 1325)</span><span class="sxs-lookup"><span data-stu-id="b3232-1043">(GH #1325)</span></span>
- <span data-ttu-id="b3232-1044">Исправлен режим /dev/kmsg для разрешения группового и другого доступа на чтение (0644) (GH 1321).</span><span class="sxs-lookup"><span data-stu-id="b3232-1044">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="b3232-1045">Реализован файл /proc/sys/kernel/random/uuid [GH 1092].</span><span class="sxs-lookup"><span data-stu-id="b3232-1045">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="b3232-1046">Исправлена ошибка, из-за которой время начала процесса отображалось как 2432 год (GH 974).</span><span class="sxs-lookup"><span data-stu-id="b3232-1046">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="b3232-1047">Переменная среды TERM по умолчанию заменена xterm-256color (GH 1446).</span><span class="sxs-lookup"><span data-stu-id="b3232-1047">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="b3232-1048">Изменен способ вычисления фиксации процесса во время ветвления процесса.</span><span class="sxs-lookup"><span data-stu-id="b3232-1048">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="b3232-1049">(GH 1286)</span><span class="sxs-lookup"><span data-stu-id="b3232-1049">(GH #1286)</span></span>
- <span data-ttu-id="b3232-1050">Реализован файл /proc/sys/VM/overcommit_memory.</span><span class="sxs-lookup"><span data-stu-id="b3232-1050">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="b3232-1051">(GH 1286)</span><span class="sxs-lookup"><span data-stu-id="b3232-1051">(GH #1286)</span></span>
- <span data-ttu-id="b3232-1052">Реализован файл /proc/net/route (GH 69).</span><span class="sxs-lookup"><span data-stu-id="b3232-1052">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="b3232-1053">Исправлена ошибка, из-за которой имя ярлыка было неправильно локализовано (GH 696).</span><span class="sxs-lookup"><span data-stu-id="b3232-1053">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="b3232-1054">Исправлена логика анализа ELF, которая неправильно проверяла заголовки программ, которые должны быть меньше или равны PATH_MAX.</span><span class="sxs-lookup"><span data-stu-id="b3232-1054">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="b3232-1055">(GH 1048)</span><span class="sxs-lookup"><span data-stu-id="b3232-1055">(GH #1048)</span></span>
- <span data-ttu-id="b3232-1056">Реализован обратный вызов statfs для procfs, sysfs, cgroupfs и binfmtf (GH 1378).</span><span class="sxs-lookup"><span data-stu-id="b3232-1056">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="b3232-1057">Исправлены окна AptPackageIndexUpdate, которые не закрывались (GH 1184, также обсуждается в GH 1193).</span><span class="sxs-lookup"><span data-stu-id="b3232-1057">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="b3232-1058">Добавлена поддержка ADDR_NO_RANDOMIZE в ASLR personality.</span><span class="sxs-lookup"><span data-stu-id="b3232-1058">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="b3232-1059">[GH 1148, 1128]</span><span class="sxs-lookup"><span data-stu-id="b3232-1059">(GH #1148, 1128)</span></span>
- <span data-ttu-id="b3232-1060">Улучшена функция PTRACE_GETSIGINFO для SIGSEGV для обеспечения правильных трассировок стека GDB во время операций AV (GH 875).</span><span class="sxs-lookup"><span data-stu-id="b3232-1060">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="b3232-1061">Анализ ELF больше не завершается ошибкой для двоичных файлов patchelf.</span><span class="sxs-lookup"><span data-stu-id="b3232-1061">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="b3232-1062">(GH 471)</span><span class="sxs-lookup"><span data-stu-id="b3232-1062">(GH #471)</span></span>
- <span data-ttu-id="b3232-1063">DNS-сервер VPN добавлен в /etc/resolv.conf (GH 416, 1350).</span><span class="sxs-lookup"><span data-stu-id="b3232-1063">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="b3232-1064">Улучшено закрытие TCP-подключений для более надежной передачи данных.</span><span class="sxs-lookup"><span data-stu-id="b3232-1064">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="b3232-1065">(GH 610, 616, 1025, 1335)</span><span class="sxs-lookup"><span data-stu-id="b3232-1065">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="b3232-1066">Теперь возвращается правильный код ошибки при открытии слишком большого числа файлов (EMFILE).</span><span class="sxs-lookup"><span data-stu-id="b3232-1066">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="b3232-1067">[GH 1126, 2090]</span><span class="sxs-lookup"><span data-stu-id="b3232-1067">(GH #1126, 2090)</span></span>
- <span data-ttu-id="b3232-1068">Журнал аудита Windows теперь отображает имя образа при аудите процесса создания.</span><span class="sxs-lookup"><span data-stu-id="b3232-1068">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="b3232-1069">Теперь запуск bash.exe из окна Bash корректно завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="b3232-1069">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="b3232-1070">Добавлено сообщение об ошибке, когда служба взаимодействия не может получить доступ к рабочему каталогу в LxFs (например, notepad.exe. bashrc).</span><span class="sxs-lookup"><span data-stu-id="b3232-1070">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="b3232-1071">Исправлена проблема, из-за которой путь Windows в WSL был усеченным.</span><span class="sxs-lookup"><span data-stu-id="b3232-1071">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="b3232-1072">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="b3232-1072">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-1073">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-1073">LTP Results:</span></span>
<span data-ttu-id="b3232-1074">Число пройденных тестов: 690.</span><span class="sxs-lookup"><span data-stu-id="b3232-1074">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="b3232-1075">Число непройденных тестов (неудачных, пропущенных и т. д.): 274.</span><span class="sxs-lookup"><span data-stu-id="b3232-1075">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="b3232-1076">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="b3232-1076">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="b3232-1077">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="b3232-1077">Syscall Support</span></span>
<span data-ttu-id="b3232-1078">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-1078">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b3232-1079">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="b3232-1079">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="b3232-1080">Сборка 14986</span><span class="sxs-lookup"><span data-stu-id="b3232-1080">Build 14986</span></span>

<span data-ttu-id="b3232-1081">Общие сведения о сборке Windows 14986 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span><span class="sxs-lookup"><span data-stu-id="b3232-1081">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-1082">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-1082">Fixed</span></span>

- <span data-ttu-id="b3232-1083">Исправлены ошибки NETLINK и PTY IOCTL.</span><span class="sxs-lookup"><span data-stu-id="b3232-1083">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="b3232-1084">Теперь отображается версия ядра 4.4.0-43 для обеспечения согласованности с Xenial.</span><span class="sxs-lookup"><span data-stu-id="b3232-1084">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="b3232-1085">Теперь Bash.exe запускается, когда ввод направляется в "nul:" (GH 1259).</span><span class="sxs-lookup"><span data-stu-id="b3232-1085">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="b3232-1086">Теперь идентификаторы потоков отображаются правильно в procfs (GH 967).</span><span class="sxs-lookup"><span data-stu-id="b3232-1086">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="b3232-1087">Теперь в inotify_add_watch() поддерживаются флаги IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR (GH 1280).</span><span class="sxs-lookup"><span data-stu-id="b3232-1087">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="b3232-1088">Реализован timer_create и связанные системные вызовы.</span><span class="sxs-lookup"><span data-stu-id="b3232-1088">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="b3232-1089">Это обеспечивает поддержку GHC (GH 307).</span><span class="sxs-lookup"><span data-stu-id="b3232-1089">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="b3232-1090">Исправлена проблема, из-за которой проверка связи возвращала время 0,000 мс (GH 1296).</span><span class="sxs-lookup"><span data-stu-id="b3232-1090">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="b3232-1091">Возвращается правильный код ошибки при открытии слишком большого числа файлов.</span><span class="sxs-lookup"><span data-stu-id="b3232-1091">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="b3232-1092">Исправлена проблема в WSL, из-за которой запрос NETLINK на данные сетевого интерфейса завершался ошибкой EINVAL, если аппаратный адрес интерфейса был 32-байтовым (например, интерфейс Teredo).</span><span class="sxs-lookup"><span data-stu-id="b3232-1092">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="b3232-1093">Обратите внимание на то, что служебная программа Linux "ip" содержит ошибку, из-за которой произойдет сбой, если WSL сообщит 32-байтовый адрес оборудования.</span><span class="sxs-lookup"><span data-stu-id="b3232-1093">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="b3232-1094">Это ошибка в "ip", а не в WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-1094">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="b3232-1095">В служебной программе "ip" жестко запрограммирована длина строкового буфера, используемого для вывода адреса оборудования, и этот буфер слишком мал для вывода 32-байтового адреса оборудования.</span><span class="sxs-lookup"><span data-stu-id="b3232-1095">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="b3232-1096">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="b3232-1096">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-1097">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-1097">LTP Results:</span></span>
<span data-ttu-id="b3232-1098">Число пройденных тестов: 669.</span><span class="sxs-lookup"><span data-stu-id="b3232-1098">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="b3232-1099">Число непройденных тестов (неудачных, пропущенных и т. д.): 258</span><span class="sxs-lookup"><span data-stu-id="b3232-1099">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="b3232-1100">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="b3232-1100">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="b3232-1101">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="b3232-1101">Syscall Support</span></span>
<span data-ttu-id="b3232-1102">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-1102">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b3232-1103">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="b3232-1103">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="b3232-1104">Сборка 14971</span><span class="sxs-lookup"><span data-stu-id="b3232-1104">Build 14971</span></span>

<span data-ttu-id="b3232-1105">Общие сведения о сборке Windows 14971 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="b3232-1105">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-1106">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-1106">Fixed</span></span>

 - <span data-ttu-id="b3232-1107">Из-за независящих от нас обстоятельств в этой сборке не будет обновлений для подсистемы Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="b3232-1107">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="b3232-1108">Регулярный выпуск плановых обновлений будет возобновлен в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="b3232-1108">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-1109">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-1109">LTP Results:</span></span>
<span data-ttu-id="b3232-1110">без изменений с момента выпуска сборки 14965.</span><span class="sxs-lookup"><span data-stu-id="b3232-1110">Unchanged from 14965</span></span> </br>
<span data-ttu-id="b3232-1111">Число пройденных тестов: 664</span><span class="sxs-lookup"><span data-stu-id="b3232-1111">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="b3232-1112">Число непройденных тестов (неудачных, пропущенных и т. д.): 263.</span><span class="sxs-lookup"><span data-stu-id="b3232-1112">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="b3232-1113">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="b3232-1113">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="b3232-1114">Сборка 14965</span><span class="sxs-lookup"><span data-stu-id="b3232-1114">Build 14965</span></span>

<span data-ttu-id="b3232-1115">Общие сведения о сборке Windows 14965 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="b3232-1115">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-1116">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-1116">Fixed</span></span>

- <span data-ttu-id="b3232-1117">Поддержка RTM_GETLINK и RTM_GETADDR для NETLINK_ROUTE в сокетах NETLINK (GH 468).</span><span class="sxs-lookup"><span data-stu-id="b3232-1117">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="b3232-1118">Применение команд ifconfig и ip для перечисления сетей.</span><span class="sxs-lookup"><span data-stu-id="b3232-1118">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="b3232-1119">Дополнительные сведения см. в нашей [записи блога о сетях WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span><span class="sxs-lookup"><span data-stu-id="b3232-1119">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="b3232-1120">Теперь /sbin добавляется в путь пользователя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b3232-1120">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="b3232-1121">Теперь путь пользователя NT по умолчанию добавляется к пути WSL (т. е. теперь можно ввести notepad.exe, не добавляя System32 в путь Linux).</span><span class="sxs-lookup"><span data-stu-id="b3232-1121">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="b3232-1122">Добавлена поддержка /proc/sys/kernel/cap_last_cap.</span><span class="sxs-lookup"><span data-stu-id="b3232-1122">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="b3232-1123">Теперь двоичные файлы NT можно запускать из WSL, если текущий рабочий каталог содержит знаки, отличные от ANSI (GH 1254).</span><span class="sxs-lookup"><span data-stu-id="b3232-1123">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="b3232-1124">Разрешено завершение работы при отключении сокета потока UNIX.</span><span class="sxs-lookup"><span data-stu-id="b3232-1124">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="b3232-1125">Добавлена поддержка PR_GET_PDEATHSIG.</span><span class="sxs-lookup"><span data-stu-id="b3232-1125">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="b3232-1126">Добавлена поддержка CLONE_PARENT.</span><span class="sxs-lookup"><span data-stu-id="b3232-1126">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="b3232-1127">Исправлена ошибка, из-за которой канал переставал отвечать на запросы, например bash -c "ls -alR /" | bash -c "cat" (GH 1214).</span><span class="sxs-lookup"><span data-stu-id="b3232-1127">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="b3232-1128">Обработка запросов на подключение к текущему терминалу.</span><span class="sxs-lookup"><span data-stu-id="b3232-1128">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="b3232-1129">Файл /proc/<pid>/oom_score_adj помечен как записываемый.</span><span class="sxs-lookup"><span data-stu-id="b3232-1129">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="b3232-1130">Добавлена папку /sys/fs/cgroup.</span><span class="sxs-lookup"><span data-stu-id="b3232-1130">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="b3232-1131">Функция sched_setaffinity должна возвращать значение маски битов сходства.</span><span class="sxs-lookup"><span data-stu-id="b3232-1131">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="b3232-1132">Исправлена логика проверки ELF, которая неправильно предполагала, что пути интерпретатора должны содержать менее 64 знаков.</span><span class="sxs-lookup"><span data-stu-id="b3232-1132">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="b3232-1133">(GH 743)</span><span class="sxs-lookup"><span data-stu-id="b3232-1133">(GH #743)</span></span>
- <span data-ttu-id="b3232-1134">Открытые дескрипторы файлов могут оставаться открытыми в окне консоли (GH 1187).</span><span class="sxs-lookup"><span data-stu-id="b3232-1134">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="b3232-1135">Устранена ошибка, из-за которой происходил сбой rename(), если имя цели содержало конечную косую черту (GH 1008).</span><span class="sxs-lookup"><span data-stu-id="b3232-1135">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="b3232-1136">Реализован файл /proc/net/dev.</span><span class="sxs-lookup"><span data-stu-id="b3232-1136">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="b3232-1137">Исправлена ошибка, из-за которой при проверке связи возвращалось значение 0,000 мс из-за разрешения таймера.</span><span class="sxs-lookup"><span data-stu-id="b3232-1137">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="b3232-1138">Реализован файл /proc/self/environ (GH 730).</span><span class="sxs-lookup"><span data-stu-id="b3232-1138">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="b3232-1139">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="b3232-1139">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-1140">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-1140">LTP Results:</span></span>
<span data-ttu-id="b3232-1141">Число пройденных тестов: 664</span><span class="sxs-lookup"><span data-stu-id="b3232-1141">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="b3232-1142">Число непройденных тестов (неудачных, пропущенных и т. д.): 263.</span><span class="sxs-lookup"><span data-stu-id="b3232-1142">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="b3232-1143">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="b3232-1143">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="b3232-1144">Сборка 14959</span><span class="sxs-lookup"><span data-stu-id="b3232-1144">Build 14959</span></span>

<span data-ttu-id="b3232-1145">Общие сведения о сборке Windows 14959 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span><span class="sxs-lookup"><span data-stu-id="b3232-1145">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-1146">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-1146">Fixed</span></span>

- <span data-ttu-id="b3232-1147">Улучшены уведомления о процессе Pico для Windows.</span><span class="sxs-lookup"><span data-stu-id="b3232-1147">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="b3232-1148">Дополнительные сведения см. в [блоге о WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span><span class="sxs-lookup"><span data-stu-id="b3232-1148">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="b3232-1149">Повышена стабильность взаимодействия с Windows.</span><span class="sxs-lookup"><span data-stu-id="b3232-1149">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="b3232-1150">Устранена ошибка 0x80070057, возникавшая при запуске bash.exe при включенной защите корпоративных данных (EDP).</span><span class="sxs-lookup"><span data-stu-id="b3232-1150">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="b3232-1151">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="b3232-1151">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-1152">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-1152">LTP Results:</span></span>
<span data-ttu-id="b3232-1153">Число пройденных тестов: 665</span><span class="sxs-lookup"><span data-stu-id="b3232-1153">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="b3232-1154">Число непройденных тестов (неудачных, пропущенных и т. д.): 263.</span><span class="sxs-lookup"><span data-stu-id="b3232-1154">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="b3232-1155">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="b3232-1155">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="b3232-1156">Сборка 14955</span><span class="sxs-lookup"><span data-stu-id="b3232-1156">Build 14955</span></span>

<span data-ttu-id="b3232-1157">Общие сведения о сборке Windows 14955 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span><span class="sxs-lookup"><span data-stu-id="b3232-1157">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-1158">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-1158">Fixed</span></span>

 - <span data-ttu-id="b3232-1159">Из-за независящих от нас обстоятельств в этой сборке не будет обновлений для подсистемы Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="b3232-1159">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="b3232-1160">Регулярный выпуск плановых обновлений будет возобновлен в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="b3232-1160">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-1161">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-1161">LTP Results:</span></span>
<span data-ttu-id="b3232-1162">Число пройденных тестов: 665</span><span class="sxs-lookup"><span data-stu-id="b3232-1162">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="b3232-1163">Число непройденных тестов (неудачных, пропущенных и т. д.): 263.</span><span class="sxs-lookup"><span data-stu-id="b3232-1163">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="b3232-1164">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="b3232-1164">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="b3232-1165">Сборка 14951</span><span class="sxs-lookup"><span data-stu-id="b3232-1165">Build 14951</span></span>

<span data-ttu-id="b3232-1166">Общие сведения о сборке Windows 14951 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="b3232-1166">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="b3232-1167">Новая функция: взаимодействие Ubuntu и Windows</span><span class="sxs-lookup"><span data-stu-id="b3232-1167">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="b3232-1168">Теперь двоичные файлы Windows можно вызывать непосредственно из командной строки WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-1168">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="b3232-1169">Это дает пользователям возможность взаимодействовать со средой и системой Windows способом, который ранее был невозможен.</span><span class="sxs-lookup"><span data-stu-id="b3232-1169">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="b3232-1170">Например, теперь пользователи могут выполнять следующие команды.</span><span class="sxs-lookup"><span data-stu-id="b3232-1170">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="b3232-1171">Дополнительные сведения:</span><span class="sxs-lookup"><span data-stu-id="b3232-1171">More information can be found at:</span></span>

- [<span data-ttu-id="b3232-1172">Блог команды WSL по взаимодействию</span><span class="sxs-lookup"><span data-stu-id="b3232-1172">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="b3232-1173">Документация по взаимодействию на сайте MSDN</span><span class="sxs-lookup"><span data-stu-id="b3232-1173">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="b3232-1174">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-1174">Fixed</span></span>

- <span data-ttu-id="b3232-1175">Ubuntu 16.04 (Xenial) теперь устанавливается для всех новых экземпляров WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-1175">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="b3232-1176">Существующие у пользователей экземпляры Ubuntu 14.04 (Trusty) не будут обновляться автоматически.</span><span class="sxs-lookup"><span data-stu-id="b3232-1176">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="b3232-1177">Теперь отображается языковой стандарт, установленный во время установки.</span><span class="sxs-lookup"><span data-stu-id="b3232-1177">Locale set during install is now displayed</span></span>
- <span data-ttu-id="b3232-1178">Улучшения в терминале, включая устранение ошибки, из-за которой перенаправление процесса WSL в файл не всегда работало.</span><span class="sxs-lookup"><span data-stu-id="b3232-1178">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="b3232-1179">Время существования консоли должно быть связано со временем существования bash.exe.</span><span class="sxs-lookup"><span data-stu-id="b3232-1179">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="b3232-1180">Размер окна консоли должен быть основан на видимом размере, а не размере буфера.</span><span class="sxs-lookup"><span data-stu-id="b3232-1180">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="b3232-1181">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="b3232-1181">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-1182">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-1182">LTP Results:</span></span>
<span data-ttu-id="b3232-1183">Число пройденных тестов: 665</span><span class="sxs-lookup"><span data-stu-id="b3232-1183">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="b3232-1184">Число непройденных тестов (неудачных, пропущенных и т. д.): 263.</span><span class="sxs-lookup"><span data-stu-id="b3232-1184">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="b3232-1185">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="b3232-1185">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="b3232-1186">Сборка 14946</span><span class="sxs-lookup"><span data-stu-id="b3232-1186">Build 14946</span></span>

<span data-ttu-id="b3232-1187">Общие сведения о сборке Windows 14946 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span><span class="sxs-lookup"><span data-stu-id="b3232-1187">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-1188">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-1188">Fixed</span></span>

- <span data-ttu-id="b3232-1189">Устранена проблема, которая не позволила создавать учетные записи WSL для пользователей с именами пользователей NT, содержащими пробелы или кавычки.</span><span class="sxs-lookup"><span data-stu-id="b3232-1189">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="b3232-1190">Внесены изменения в VolFs и DrvFs, чтобы возвращалось значение 0 для количества ссылок каталога в stat.</span><span class="sxs-lookup"><span data-stu-id="b3232-1190">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="b3232-1191">Поддержка параметра сокета IPV6_MULTICAST_HOPS.</span><span class="sxs-lookup"><span data-stu-id="b3232-1191">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="b3232-1192">Ограничение в один цикл ввода-вывода консоли на tty.</span><span class="sxs-lookup"><span data-stu-id="b3232-1192">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="b3232-1193">Например, можно выполнить следующую команду:</span><span class="sxs-lookup"><span data-stu-id="b3232-1193">Example: the following command is possible:</span></span>
  - <span data-ttu-id="b3232-1194">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span><span class="sxs-lookup"><span data-stu-id="b3232-1194">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="b3232-1195">Пробелы в /proc/cpuinfo заменены символами табуляции (GH 1115).</span><span class="sxs-lookup"><span data-stu-id="b3232-1195">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="b3232-1196">DrvFs теперь отображается в mountinfo с именем, совпадающим с подключенным томом Windows.</span><span class="sxs-lookup"><span data-stu-id="b3232-1196">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="b3232-1197">Теперь /home и /root отображаются в mountinfo с правильными именами.</span><span class="sxs-lookup"><span data-stu-id="b3232-1197">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="b3232-1198">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="b3232-1198">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-1199">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-1199">LTP Results:</span></span>
<span data-ttu-id="b3232-1200">Число пройденных тестов: 665</span><span class="sxs-lookup"><span data-stu-id="b3232-1200">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="b3232-1201">Число непройденных тестов (неудачных, пропущенных и т. д.): 263.</span><span class="sxs-lookup"><span data-stu-id="b3232-1201">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="b3232-1202">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="b3232-1202">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="b3232-1203">Сборка 14942</span><span class="sxs-lookup"><span data-stu-id="b3232-1203">Build 14942</span></span>

<span data-ttu-id="b3232-1204">Общие сведения о сборке Windows 14942 доступны в [блоге о Windows](https://aka.ms/onefourninefourtwoooooo).</span><span class="sxs-lookup"><span data-stu-id="b3232-1204">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-1205">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-1205">Fixed</span></span>

- <span data-ttu-id="b3232-1206">Исправлен ряд ошибок, в том числе сбой сети "ATTEMPTED EXECUTE OF NOEXECUTE MEMORY" (Попытка выполнения в недоступной памяти), которые блокируют SSH.</span><span class="sxs-lookup"><span data-stu-id="b3232-1206">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="b3232-1207">Добавлена поддержка inotifiy для уведомлений, созданных в приложениях для Windows в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="b3232-1207">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="b3232-1208">Реализованы параметры TCP_KEEPIDLE и TCP_KEEPINTVL для mongod.</span><span class="sxs-lookup"><span data-stu-id="b3232-1208">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="b3232-1209">(GH 695)</span><span class="sxs-lookup"><span data-stu-id="b3232-1209">(GH #695)</span></span>
- <span data-ttu-id="b3232-1210">Реализован системный вызов pivot_root.</span><span class="sxs-lookup"><span data-stu-id="b3232-1210">Implement the pivot_root system call</span></span>
- <span data-ttu-id="b3232-1211">Реализован параметр сокета для SO_DONTROUTE.</span><span class="sxs-lookup"><span data-stu-id="b3232-1211">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="b3232-1212">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="b3232-1212">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="b3232-1213">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-1213">LTP Results:</span></span>
<span data-ttu-id="b3232-1214">Число пройденных тестов: 665</span><span class="sxs-lookup"><span data-stu-id="b3232-1214">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="b3232-1215">Число непройденных тестов (неудачных, пропущенных и т. д.): 263.</span><span class="sxs-lookup"><span data-stu-id="b3232-1215">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="b3232-1216">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="b3232-1216">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="b3232-1217">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="b3232-1217">Syscall Support</span></span>
<span data-ttu-id="b3232-1218">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-1218">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b3232-1219">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="b3232-1219">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="b3232-1220">Сборка 14936</span><span class="sxs-lookup"><span data-stu-id="b3232-1220">Build 14936</span></span>

<span data-ttu-id="b3232-1221">Общие сведения о сборке Windows 14936 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="b3232-1221">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="b3232-1222">Примечание. В предстоящем выпуске WSL будет устанавливать версию Ubuntu 16.04 (Xenial) вместо Ubuntu 14.04 (Trusty).</span><span class="sxs-lookup"><span data-stu-id="b3232-1222">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="b3232-1223">Это изменение будет применено к участникам программы предварительной оценки, которые устанавливают новые экземпляры (lxrun.exe /install или первый запуск bash.exe).</span><span class="sxs-lookup"><span data-stu-id="b3232-1223">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="b3232-1224">Существующие экземпляры с версией Trusty не будут обновлены автоматически.</span><span class="sxs-lookup"><span data-stu-id="b3232-1224">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="b3232-1225">Пользователи могут обновить свой образ Trusty до версии Xenial с помощью команды do-release-upgrade.</span><span class="sxs-lookup"><span data-stu-id="b3232-1225">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="b3232-1226">Известная проблема</span><span class="sxs-lookup"><span data-stu-id="b3232-1226">Known Issue</span></span>
<span data-ttu-id="b3232-1227">В WSL существует проблема с реализацией некоторых сокетов.</span><span class="sxs-lookup"><span data-stu-id="b3232-1227">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="b3232-1228">Ошибка проявляется как сбой "ATTEMPTED EXECUTE OF NOEXECUTE MEMORY" (Попытка выполнения в недоступной памяти).</span><span class="sxs-lookup"><span data-stu-id="b3232-1228">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="b3232-1229">Чаще всего этот сбой происходит при использовании SSH.</span><span class="sxs-lookup"><span data-stu-id="b3232-1229">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="b3232-1230">Первопричина исправлена во внутренних сборках, и исправление будет добавлено в сборки для программы предварительной оценки при первой возможности.</span><span class="sxs-lookup"><span data-stu-id="b3232-1230">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="b3232-1231">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-1231">Fixed</span></span>

- <span data-ttu-id="b3232-1232">Реализован системный вызов chroot.</span><span class="sxs-lookup"><span data-stu-id="b3232-1232">Implemented the chroot system call</span></span>
- <span data-ttu-id="b3232-1233">Улучшения в inotify, ~~включая поддержку уведомлений, созданных в приложениях для Windows в DrvFs~~.</span><span class="sxs-lookup"><span data-stu-id="b3232-1233">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="b3232-1234">Исправление: В настоящее время недоступна поддержка в inotify изменений, исходящих из приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="b3232-1234">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="b3232-1235">Привязка сокета к IPV6::<port n> теперь поддерживает IPV6_V6ONLY (GH 68, 157, 393, 460, 674, 740, 982, 996).</span><span class="sxs-lookup"><span data-stu-id="b3232-1235">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="b3232-1236">Реализовано поведение WNOWAIT для системного вызова waitid (GH 638).</span><span class="sxs-lookup"><span data-stu-id="b3232-1236">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="b3232-1237">Поддержка параметров IP-сокета IP_HDRINCL и IP_TTL.</span><span class="sxs-lookup"><span data-stu-id="b3232-1237">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="b3232-1238">Результат read() нулевой длины должен возвращаться немедленно (GH 975).</span><span class="sxs-lookup"><span data-stu-id="b3232-1238">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="b3232-1239">Правильная обработка имен файлов и префиксов имен файлов, которые не содержат терминатор NULL в TAR-файле.</span><span class="sxs-lookup"><span data-stu-id="b3232-1239">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="b3232-1240">Поддержка epoll для /dev/null.</span><span class="sxs-lookup"><span data-stu-id="b3232-1240">epoll support for /dev/null</span></span>
- <span data-ttu-id="b3232-1241">Исправлен источник времени /dev/alarm.</span><span class="sxs-lookup"><span data-stu-id="b3232-1241">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="b3232-1242">Теперь команда bash -c может выполнять перенаправление в файл.</span><span class="sxs-lookup"><span data-stu-id="b3232-1242">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="b3232-1243">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="b3232-1243">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-1244">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-1244">LTP Results:</span></span>
<span data-ttu-id="b3232-1245">Число пройденных тестов: 664</span><span class="sxs-lookup"><span data-stu-id="b3232-1245">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="b3232-1246">Число непройденных тестов (неудачных, пропущенных и т. д.): 264.</span><span class="sxs-lookup"><span data-stu-id="b3232-1246">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="b3232-1247">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="b3232-1247">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="b3232-1248">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="b3232-1248">Syscall Support</span></span>
<span data-ttu-id="b3232-1249">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-1249">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b3232-1250">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="b3232-1250">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="b3232-1251">Сборка 14931</span><span class="sxs-lookup"><span data-stu-id="b3232-1251">Build 14931</span></span>

<span data-ttu-id="b3232-1252">Общие сведения о сборке Windows 14931 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="b3232-1252">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-1253">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-1253">Fixed</span></span>

 - <span data-ttu-id="b3232-1254">Из-за независящих от нас обстоятельств в этой сборке не будет обновлений для подсистемы Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="b3232-1254">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="b3232-1255">Регулярный выпуск плановых обновлений будет возобновлен в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="b3232-1255">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="b3232-1256">Сборка 14926</span><span class="sxs-lookup"><span data-stu-id="b3232-1256">Build 14926</span></span>

<span data-ttu-id="b3232-1257">Общие сведения о сборке Windows 14926 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="b3232-1257">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-1258">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-1258">Fixed</span></span>

- <span data-ttu-id="b3232-1259">Проверка связи теперь работает в консолях без привилегий администратора.</span><span class="sxs-lookup"><span data-stu-id="b3232-1259">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="b3232-1260">Теперь поддерживается ping6, также без привилегий администратора.</span><span class="sxs-lookup"><span data-stu-id="b3232-1260">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="b3232-1261">Поддержка в inotify файлов, измененных посредством WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-1261">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="b3232-1262">(GH 216)</span><span class="sxs-lookup"><span data-stu-id="b3232-1262">(GH #216)</span></span>
  - <span data-ttu-id="b3232-1263">Поддерживаемые флаги:</span><span class="sxs-lookup"><span data-stu-id="b3232-1263">Flags supported:</span></span>
    - <span data-ttu-id="b3232-1264">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="b3232-1264">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="b3232-1265">События inotify_add_watch: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="b3232-1265">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="b3232-1266">Атрибуты inotify_add_watch: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="b3232-1266">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="b3232-1267">Выходные данные чтения: LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="b3232-1267">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="b3232-1268">Известная проблема: Изменение файлов из приложений Windows не приводит к созданию событий.</span><span class="sxs-lookup"><span data-stu-id="b3232-1268">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="b3232-1269">Сокет UNIX теперь поддерживает SCM_CREDENTIALS.</span><span class="sxs-lookup"><span data-stu-id="b3232-1269">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b3232-1270">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="b3232-1270">LTP Results:</span></span>
<span data-ttu-id="b3232-1271">Число пройденных тестов: 651</span><span class="sxs-lookup"><span data-stu-id="b3232-1271">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="b3232-1272">Число непройденных тестов (неудачных, пропущенных и т. д.): 258</span><span class="sxs-lookup"><span data-stu-id="b3232-1272">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="b3232-1273">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="b3232-1273">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="b3232-1274">Сборка 14915</span><span class="sxs-lookup"><span data-stu-id="b3232-1274">Build 14915</span></span>

<span data-ttu-id="b3232-1275">Общие сведения о сборке Windows 14915 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="b3232-1275">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-1276">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-1276">Fixed</span></span>
-  <span data-ttu-id="b3232-1277">Socketpair для сокетов датаграмм UNIX (GH 262).</span><span class="sxs-lookup"><span data-stu-id="b3232-1277">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="b3232-1278">Поддержка сокетов UNIX для SO_REUSEADDR.</span><span class="sxs-lookup"><span data-stu-id="b3232-1278">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="b3232-1279">Поддержка сокетов UNIX для SO_BROADCAST (GH 568).</span><span class="sxs-lookup"><span data-stu-id="b3232-1279">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="b3232-1280">Поддержка сокетов UNIX для SOCK_SEQPACKET (GH 758, 546).</span><span class="sxs-lookup"><span data-stu-id="b3232-1280">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="b3232-1281">Добавлена поддержка send, recv и shutdown для сокетов датаграмм UNIX.</span><span class="sxs-lookup"><span data-stu-id="b3232-1281">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="b3232-1282">Устранена ошибка из-за неправильной проверки параметров mmap для нефиксированных адресов.</span><span class="sxs-lookup"><span data-stu-id="b3232-1282">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="b3232-1283">(GH 847)</span><span class="sxs-lookup"><span data-stu-id="b3232-1283">(GH #847)</span></span>
- <span data-ttu-id="b3232-1284">Поддержка приостановки и возобновления состояний терминала.</span><span class="sxs-lookup"><span data-stu-id="b3232-1284">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="b3232-1285">Поддержка TIOCPKT ioctl для разблокировки служебной программы Screen (GH 774).</span><span class="sxs-lookup"><span data-stu-id="b3232-1285">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="b3232-1286">Известная проблема: Не работают функциональные клавиши.</span><span class="sxs-lookup"><span data-stu-id="b3232-1286">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="b3232-1287">Исправлено состязание в TimerFd, которое могло привести к обращению LxpTimerFdWorkerRoutine к освобожденному элементу ReaderReady (GH 814).</span><span class="sxs-lookup"><span data-stu-id="b3232-1287">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="b3232-1288">Включена поддержка перезапускаемых системных вызовов для futex, poll и clock_nanosleep.</span><span class="sxs-lookup"><span data-stu-id="b3232-1288">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="b3232-1289">Добавлена поддержка подключения привязки.</span><span class="sxs-lookup"><span data-stu-id="b3232-1289">Added bind mount support</span></span>
- <span data-ttu-id="b3232-1290">Поддержка отмены общего доступа для пространства имен подключения.</span><span class="sxs-lookup"><span data-stu-id="b3232-1290">unshare for mount namespace support</span></span>
    - <span data-ttu-id="b3232-1291">Известная проблема: При создании пространства имен подключения посредством `unshare(CLONE_NEWNS)` текущий рабочий каталог будет по-прежнему указывать на старое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="b3232-1291">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="b3232-1292">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="b3232-1292">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="b3232-1293">Сборка 14905</span><span class="sxs-lookup"><span data-stu-id="b3232-1293">Build 14905</span></span>

<span data-ttu-id="b3232-1294">Общие сведения о сборке Windows 14905 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span><span class="sxs-lookup"><span data-stu-id="b3232-1294">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-1295">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-1295">Fixed</span></span>
- <span data-ttu-id="b3232-1296">Теперь поддерживаются перезапускаемые системные вызовы (GH 349, GH 520).</span><span class="sxs-lookup"><span data-stu-id="b3232-1296">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="b3232-1297">Теперь функционируют символические ссылки на каталоги, которые заканчиваются косой чертой "/" (GH 650).</span><span class="sxs-lookup"><span data-stu-id="b3232-1297">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="b3232-1298">Реализован параметр RNDGETENTCNT ioctl для /dev/random.</span><span class="sxs-lookup"><span data-stu-id="b3232-1298">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="b3232-1299">Реализованы файлы /proc/[pid]/mounts, /proc/[pid]/mountinfo и /proc/[pid]/mountstats.</span><span class="sxs-lookup"><span data-stu-id="b3232-1299">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="b3232-1300">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="b3232-1300">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="b3232-1301">Сборка 14901</span><span class="sxs-lookup"><span data-stu-id="b3232-1301">Build 14901</span></span>
<span data-ttu-id="b3232-1302">Первая сборка для программы предварительной оценки для выпуска после юбилейного обновления Windows 10.</span><span class="sxs-lookup"><span data-stu-id="b3232-1302">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="b3232-1303">Общие сведения о сборке Windows 14901 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="b3232-1303">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-1304">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-1304">Fixed</span></span>
- <span data-ttu-id="b3232-1305">Исправлена проблема конечной косой черты.</span><span class="sxs-lookup"><span data-stu-id="b3232-1305">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="b3232-1306">Теперь работают такие команды, как `$ mv a/c/ a/b/`.</span><span class="sxs-lookup"><span data-stu-id="b3232-1306">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="b3232-1307">Теперь при установке отображается запрос, позволяющий установить языковый стандарт Ubuntu, совпадающий с языковым стандартом Windows.</span><span class="sxs-lookup"><span data-stu-id="b3232-1307">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="b3232-1308">Поддержка procfs для папки ns.</span><span class="sxs-lookup"><span data-stu-id="b3232-1308">Procfs support for ns folder</span></span>
- <span data-ttu-id="b3232-1309">Добавлены функции подключения и отключения для файловых систем tmpfs, procfs и sysfs.</span><span class="sxs-lookup"><span data-stu-id="b3232-1309">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="b3232-1310">Исправлена 32-разрядная подпись ABI для mknod[at].</span><span class="sxs-lookup"><span data-stu-id="b3232-1310">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="b3232-1311">Сокеты UNIX переведены на модель диспетчеризации.</span><span class="sxs-lookup"><span data-stu-id="b3232-1311">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="b3232-1312">Размер буфера recv сокета INET, заданный с помощью setsockopt, должен учитываться.</span><span class="sxs-lookup"><span data-stu-id="b3232-1312">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="b3232-1313">Реализован флаг получения сообщения MSG_CMSG_CLOEXEC для сокетов UNIX.</span><span class="sxs-lookup"><span data-stu-id="b3232-1313">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="b3232-1314">Перенаправление канала stdin/stdout процесса Linux (GH 2).</span><span class="sxs-lookup"><span data-stu-id="b3232-1314">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="b3232-1315">Разрешена конвейерная передача команд bash -c в командную строку.</span><span class="sxs-lookup"><span data-stu-id="b3232-1315">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="b3232-1316">Пример:  >dir | bash -c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="b3232-1316">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="b3232-1317">Теперь Bash можно установить в системах с несколькими файлами подкачки (GH 538, 358).</span><span class="sxs-lookup"><span data-stu-id="b3232-1317">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="b3232-1318">Размер буфера сокета INET по умолчанию должен соответствовать установке Ubuntu по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b3232-1318">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="b3232-1319">Системные вызовы xattr согласованы с listxattr.</span><span class="sxs-lookup"><span data-stu-id="b3232-1319">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="b3232-1320">SIOCGIFCONF возвращает только интерфейсы с допустимым IPv4-адресом.</span><span class="sxs-lookup"><span data-stu-id="b3232-1320">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="b3232-1321">Исправлено действие по умолчанию для сигнала при внедрении с помощью ptrace.</span><span class="sxs-lookup"><span data-stu-id="b3232-1321">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="b3232-1322">Реализован файл /proc/sys/vm/min_free_kbytes.</span><span class="sxs-lookup"><span data-stu-id="b3232-1322">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="b3232-1323">Использование значений реестра для контекста компьютера при восстановлении контекста в sigreturn.</span><span class="sxs-lookup"><span data-stu-id="b3232-1323">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="b3232-1324">Это устраняет проблему, из-за которой у некоторых пользователей java и javac переставали отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="b3232-1324">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="b3232-1325">Реализован файл /proc/sys/kernel/hostname.</span><span class="sxs-lookup"><span data-stu-id="b3232-1325">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b3232-1326">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="b3232-1326">Syscall Support</span></span>
<span data-ttu-id="b3232-1327">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-1327">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b3232-1328">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="b3232-1328">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="b3232-1329">Сборка 14388 для юбилейного обновления Windows 10</span><span class="sxs-lookup"><span data-stu-id="b3232-1329">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="b3232-1330">Общие сведения о сборке Windows 14388 доступны в [блоге о Windows](https://aka.ms/14388wip).</span><span class="sxs-lookup"><span data-stu-id="b3232-1330">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="b3232-1331">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-1331">Fixed</span></span>
- <span data-ttu-id="b3232-1332">Исправления для подготовки к выпуску юбилейного обновления Windows 10 2-го августа.</span><span class="sxs-lookup"><span data-stu-id="b3232-1332">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="b3232-1333">Дополнительные сведения о компоненте WSL в юбилейном обновлении можно найти на нашем [блоге](https://blogs.msdn.microsoft.com/wsl/).</span><span class="sxs-lookup"><span data-stu-id="b3232-1333">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="b3232-1334">Сборка 14376</span><span class="sxs-lookup"><span data-stu-id="b3232-1334">Build 14376</span></span>
<span data-ttu-id="b3232-1335">Общие сведения о сборке Windows 14376 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="b3232-1335">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="b3232-1336">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-1336">Fixed</span></span>
- <span data-ttu-id="b3232-1337">Удалены некоторые экземпляры, в которых функция apt-get переставала отвечать на запросы (GH 493).</span><span class="sxs-lookup"><span data-stu-id="b3232-1337">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="b3232-1338">Исправлена проблема, из-за которой неправильно обрабатывались пустые подключения.</span><span class="sxs-lookup"><span data-stu-id="b3232-1338">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="b3232-1339">Исправлена проблема, из-за которой неправильно подключались диски ramdisk.</span><span class="sxs-lookup"><span data-stu-id="b3232-1339">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="b3232-1340">Изменена процедура принятия сокетов UNIX для поддержки флагов (частично GH 451).</span><span class="sxs-lookup"><span data-stu-id="b3232-1340">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="b3232-1341">Исправлена распространенная проблема с сетью, вызывавшая ошибку "синий экран".</span><span class="sxs-lookup"><span data-stu-id="b3232-1341">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="b3232-1342">Устранена ошибка "синий экран" при доступе к /proc/[pid]/task (GH 523).</span><span class="sxs-lookup"><span data-stu-id="b3232-1342">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="b3232-1343">Исправлена высокая загрузка ЦП для некоторых сценариев использования pty (GH 488, 504).</span><span class="sxs-lookup"><span data-stu-id="b3232-1343">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="b3232-1344">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="b3232-1344">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="b3232-1345">Сборка 14371</span><span class="sxs-lookup"><span data-stu-id="b3232-1345">Build 14371</span></span>
<span data-ttu-id="b3232-1346">Общие сведения о сборке Windows 14371 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="b3232-1346">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="b3232-1347">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-1347">Fixed</span></span>
- <span data-ttu-id="b3232-1348">Исправлено состязание за синхронизацию SIGCHLD и wait() при использовании ptrace.</span><span class="sxs-lookup"><span data-stu-id="b3232-1348">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="b3232-1349">Исправлена обработка путей, которые завершаются косой чертой "/" (GH 432).</span><span class="sxs-lookup"><span data-stu-id="b3232-1349">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="b3232-1350">Устранен сбой при переименовании или отмене связи из-за открытых дескрипторов дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="b3232-1350">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="b3232-1351">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="b3232-1351">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="b3232-1352">Сборка 14366</span><span class="sxs-lookup"><span data-stu-id="b3232-1352">Build 14366</span></span>
<span data-ttu-id="b3232-1353">Общие сведения о сборке Windows 14366 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span><span class="sxs-lookup"><span data-stu-id="b3232-1353">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="b3232-1354">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-1354">Fixed</span></span>
- <span data-ttu-id="b3232-1355">Исправлено создание файла с помощью символических ссылок.</span><span class="sxs-lookup"><span data-stu-id="b3232-1355">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="b3232-1356">Добавлена функция listxattr для Python (GH 385).</span><span class="sxs-lookup"><span data-stu-id="b3232-1356">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="b3232-1357">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="b3232-1357">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b3232-1358">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="b3232-1358">Syscall Support</span></span>
-   <span data-ttu-id="b3232-1359">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-1359">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b3232-1360">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="b3232-1360">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="b3232-1361">Сборка 14361</span><span class="sxs-lookup"><span data-stu-id="b3232-1361">Build 14361</span></span>
<span data-ttu-id="b3232-1362">Общие сведения о сборке Windows 14361 доступны в [блоге о Windows](https://aka.ms/wip14361).</span><span class="sxs-lookup"><span data-stu-id="b3232-1362">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="b3232-1363">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-1363">Fixed</span></span>
- <span data-ttu-id="b3232-1364">Теперь в DrvFs учитывается регистр при выполнении в Bash для Ubuntu в Windows.</span><span class="sxs-lookup"><span data-stu-id="b3232-1364">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="b3232-1365">Пользователи могут хранить на дисках в /mnt/c и файл case.txt, и файл CASE.TXT.</span><span class="sxs-lookup"><span data-stu-id="b3232-1365">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="b3232-1366">Учет регистра поддерживается только в Bash для Ubuntu в Windows.</span><span class="sxs-lookup"><span data-stu-id="b3232-1366">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="b3232-1367">За пределами Bash NTFS будет отображать сведения о файлах правильно, но при взаимодействии с этими файлами из Windows может наблюдаться непредвиденное поведение.</span><span class="sxs-lookup"><span data-stu-id="b3232-1367">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="b3232-1368">Корень каждого тома (т. е. /mnt/c) не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="b3232-1368">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="b3232-1369">Дополнительные сведения об обработке этих файлов в Windows можно найти [здесь](https://support.microsoft.com/en-us/kb/100625).</span><span class="sxs-lookup"><span data-stu-id="b3232-1369">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="b3232-1370">Значительно улучшена поддержка pty и tty.</span><span class="sxs-lookup"><span data-stu-id="b3232-1370">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="b3232-1371">Теперь поддерживаются такие приложения, как tmux (GH 40).</span><span class="sxs-lookup"><span data-stu-id="b3232-1371">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="b3232-1372">Исправлена проблема с установкой, из-за которой учетные записи пользователей создавались не всегда.</span><span class="sxs-lookup"><span data-stu-id="b3232-1372">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="b3232-1373">Оптимизирована структура аргументов командной строки, которая позволяет получить очень длинный список аргументов.</span><span class="sxs-lookup"><span data-stu-id="b3232-1373">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="b3232-1374">(GH 153)</span><span class="sxs-lookup"><span data-stu-id="b3232-1374">(GH #153)</span></span>
- <span data-ttu-id="b3232-1375">Теперь можно выполнять операции delete и chmod с файлами только для чтения в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="b3232-1375">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="b3232-1376">Исправлены некоторые экземпляры, в которых терминал при отключении переставал отвечать на запросы (GH 43).</span><span class="sxs-lookup"><span data-stu-id="b3232-1376">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="b3232-1377">Теперь на устройствах tty работает chmod и chown.</span><span class="sxs-lookup"><span data-stu-id="b3232-1377">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="b3232-1378">Разрешено подключение к 0.0.0.0 и :: как localhost (GH 388).</span><span class="sxs-lookup"><span data-stu-id="b3232-1378">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="b3232-1379">Теперь sendmsg и recvmsg обрабатывают векторы ввода-вывода длиной больше 1 (частично GH 376).</span><span class="sxs-lookup"><span data-stu-id="b3232-1379">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="b3232-1380">Теперь пользователи могут отказаться от автоматически создаваемого файла hosts (GH 398).</span><span class="sxs-lookup"><span data-stu-id="b3232-1380">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="b3232-1381">Автоматическое сопоставление языкового стандарта Linux с языковым стандартом NT во время установки (GH 11).</span><span class="sxs-lookup"><span data-stu-id="b3232-1381">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="b3232-1382">Добавлен файл /proc/sys/vm/swappiness (GH #306).</span><span class="sxs-lookup"><span data-stu-id="b3232-1382">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="b3232-1383">Теперь strace завершается правильно.</span><span class="sxs-lookup"><span data-stu-id="b3232-1383">strace now exits correctly</span></span>
- <span data-ttu-id="b3232-1384">Разрешено повторное открытие каналов через /proc/self/fd (GH 222).</span><span class="sxs-lookup"><span data-stu-id="b3232-1384">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="b3232-1385">Скрытие каталогов в %LOCALAPPDATA%\lxss из DrvFs (GH 270).</span><span class="sxs-lookup"><span data-stu-id="b3232-1385">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="b3232-1386">Улучшена обработка bash.exe ~.</span><span class="sxs-lookup"><span data-stu-id="b3232-1386">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="b3232-1387">Теперь поддерживаются такие команды, как "bash ~ -c ls" (GH 467).</span><span class="sxs-lookup"><span data-stu-id="b3232-1387">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="b3232-1388">Сокеты теперь уведомляют epoll о доступе на чтение во время завершения (GH 271).</span><span class="sxs-lookup"><span data-stu-id="b3232-1388">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="b3232-1389">Команда lxrun /uninstall лучше удаляет файлы и папки.</span><span class="sxs-lookup"><span data-stu-id="b3232-1389">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="b3232-1390">Исправлена команда ps -f (GH 246).</span><span class="sxs-lookup"><span data-stu-id="b3232-1390">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="b3232-1391">Улучшена поддержка приложений x11, таких как xEmacs (GH 481).</span><span class="sxs-lookup"><span data-stu-id="b3232-1391">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="b3232-1392">Обновлен начальный размер стека потока в соответствии с параметром Ubuntu по умолчанию. Теперь при системном вызове get_rlimit размер отображается правильно (GH 172, 258).</span><span class="sxs-lookup"><span data-stu-id="b3232-1392">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="b3232-1393">Улучшено отображение имен образов процессов Pico (например, для аудита).</span><span class="sxs-lookup"><span data-stu-id="b3232-1393">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="b3232-1394">Реализован файл /proc/mountinfo для команды df.</span><span class="sxs-lookup"><span data-stu-id="b3232-1394">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="b3232-1395">Исправлен код ошибки символической ссылки для дочернего имени.</span><span class="sxs-lookup"><span data-stu-id="b3232-1395">Fixed symlink error code for child name .</span></span> <span data-ttu-id="b3232-1396"> </span><span class="sxs-lookup"><span data-stu-id="b3232-1396">and ..</span></span>
- <span data-ttu-id="b3232-1397">Дополнительные улучшения исправлений ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="b3232-1397">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b3232-1398">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="b3232-1398">Syscall Support</span></span>
<span data-ttu-id="b3232-1399">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-1399">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b3232-1400">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="b3232-1400">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="b3232-1401">Сборка 14352</span><span class="sxs-lookup"><span data-stu-id="b3232-1401">Build 14352</span></span>
<span data-ttu-id="b3232-1402">Общие сведения о сборке Windows 14352 доступны в [блоге о Windows](https://aka.ms/wip14352).</span><span class="sxs-lookup"><span data-stu-id="b3232-1402">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b3232-1403">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-1403">Fixed</span></span>
- <span data-ttu-id="b3232-1404">Исправлена проблема, из-за которой большие файлы скачивались и создавались неправильно.</span><span class="sxs-lookup"><span data-stu-id="b3232-1404">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="b3232-1405">Это должно позволить использовать npm и реализовать другие сценарии (GH 3, GH 313).</span><span class="sxs-lookup"><span data-stu-id="b3232-1405">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="b3232-1406">Удалены некоторые экземпляры, в которых сокеты переставали отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="b3232-1406">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="b3232-1407">Исправлены некоторые ошибки ptrace.</span><span class="sxs-lookup"><span data-stu-id="b3232-1407">Corrected some ptrace errors</span></span>
- <span data-ttu-id="b3232-1408">Исправлена проблема с WSL, и теперь можно использовать имена файлов длиннее 255 знаков.</span><span class="sxs-lookup"><span data-stu-id="b3232-1408">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="b3232-1409">Улучшена поддержка знаков языков, отличных от английского.</span><span class="sxs-lookup"><span data-stu-id="b3232-1409">Improved support for non-English characters</span></span>
- <span data-ttu-id="b3232-1410">Добавление данных о текущем часовом поясе Windows и назначение его используемым по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b3232-1410">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="b3232-1411">Уникальный идентификатор устройства для каждой точки подключения (исправление JRE — GH 49).</span><span class="sxs-lookup"><span data-stu-id="b3232-1411">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="b3232-1412">Устранена ошибка из-за путей, содержащих "."</span><span class="sxs-lookup"><span data-stu-id="b3232-1412">Correct issue with paths containing “.”</span></span> <span data-ttu-id="b3232-1413">и ".."</span><span class="sxs-lookup"><span data-stu-id="b3232-1413">and “..”</span></span>
- <span data-ttu-id="b3232-1414">Добавлена поддержка FIFO (GH 71).</span><span class="sxs-lookup"><span data-stu-id="b3232-1414">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="b3232-1415">Обновлен формат resolv.conf в соответствии с собственным форматом Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="b3232-1415">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="b3232-1416">Некоторая очистка procfs.</span><span class="sxs-lookup"><span data-stu-id="b3232-1416">Some procfs cleanup</span></span>
- <span data-ttu-id="b3232-1417">Включена проверка связи для консолей администратора (GH 18).</span><span class="sxs-lookup"><span data-stu-id="b3232-1417">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b3232-1418">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="b3232-1418">Syscall Support</span></span>
<span data-ttu-id="b3232-1419">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-1419">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b3232-1420">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="b3232-1420">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="b3232-1421">Сборка 14342</span><span class="sxs-lookup"><span data-stu-id="b3232-1421">Build 14342</span></span>
<span data-ttu-id="b3232-1422">Общие сведения о сборке Windows 14342 доступны в [блоге о Windows](https://aka.ms/wip14342).</span><span class="sxs-lookup"><span data-stu-id="b3232-1422">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="b3232-1423">Сведения о VolFs и DriveFs можно найти в [блоге о WSL](https://blogs.msdn.microsoft.com/wsl).</span><span class="sxs-lookup"><span data-stu-id="b3232-1423">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="b3232-1424">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-1424">Fixed</span></span>
- <span data-ttu-id="b3232-1425">Исправлена проблема с установкой, возникавшая, когда в имени пользователя Windows присутствовали знаки Юникода.</span><span class="sxs-lookup"><span data-stu-id="b3232-1425">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="b3232-1426">Теперь обходное решение для обновления apt-get с помощью udev, приведенное в разделе часто задаваемых вопросов, предоставляется по умолчанию при первом запуске.</span><span class="sxs-lookup"><span data-stu-id="b3232-1426">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="b3232-1427">Включены символические ссылки в каталогах DriveFs (/mnt/<drive>).</span><span class="sxs-lookup"><span data-stu-id="b3232-1427">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="b3232-1428">Теперь работают символические ссылки между DriveFs и VolFs.</span><span class="sxs-lookup"><span data-stu-id="b3232-1428">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="b3232-1429">Устранена проблема с анализом путей верхнего уровня. Теперь ls .// будет работать должным образом.</span><span class="sxs-lookup"><span data-stu-id="b3232-1429">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="b3232-1430">Теперь работает установка npm в DriveFs и параметры -g.</span><span class="sxs-lookup"><span data-stu-id="b3232-1430">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="b3232-1431">Исправлена проблема, препятствующая запуску сервера PHP.</span><span class="sxs-lookup"><span data-stu-id="b3232-1431">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="b3232-1432">Обновлены значения среды по умолчанию, такие как $PATH, чтобы они больше соответствовали собственным переменным Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="b3232-1432">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="b3232-1433">Добавлена еженедельная задача обслуживания в Windows для обновления кэша пакетов apt.</span><span class="sxs-lookup"><span data-stu-id="b3232-1433">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="b3232-1434">Исправлена проблема с проверкой заголовков ELF. Теперь WSL поддерживает все параметры Melkor.</span><span class="sxs-lookup"><span data-stu-id="b3232-1434">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="b3232-1435">Оболочка Zsh работает.</span><span class="sxs-lookup"><span data-stu-id="b3232-1435">Zsh shell is functional</span></span>
- <span data-ttu-id="b3232-1436">Теперь поддерживаются предварительно скомпилированные двоичные файлы Go.</span><span class="sxs-lookup"><span data-stu-id="b3232-1436">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="b3232-1437">Теперь запросы при первом запуске bash.exe локализованы правильно.</span><span class="sxs-lookup"><span data-stu-id="b3232-1437">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="b3232-1438">Теперь /proc/meminfo возвращает правильные сведения.</span><span class="sxs-lookup"><span data-stu-id="b3232-1438">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="b3232-1439">Сокеты теперь поддерживаются в VFS.</span><span class="sxs-lookup"><span data-stu-id="b3232-1439">Sockets now supported in VFS</span></span>
- <span data-ttu-id="b3232-1440">Теперь /dev подключен как tempfs.</span><span class="sxs-lookup"><span data-stu-id="b3232-1440">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="b3232-1441">FIFO теперь поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b3232-1441">Fifo now supported</span></span>
- <span data-ttu-id="b3232-1442">Многоядерные системы теперь правильно отображаются в /proc/cpuinfo.</span><span class="sxs-lookup"><span data-stu-id="b3232-1442">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="b3232-1443">Дополнительные улучшения и сообщения об ошибках при скачивании во время первого запуска.</span><span class="sxs-lookup"><span data-stu-id="b3232-1443">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="b3232-1444">Усовершенствования и исправления системных вызовов.</span><span class="sxs-lookup"><span data-stu-id="b3232-1444">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="b3232-1445">Список поддерживаемых системных вызовов приведен ниже.</span><span class="sxs-lookup"><span data-stu-id="b3232-1445">Supported syscall list below.</span></span>
- <span data-ttu-id="b3232-1446">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="b3232-1446">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="b3232-1447">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="b3232-1447">Known Issues</span></span>
- <span data-ttu-id="b3232-1448">Неправильное разрешение ".."</span><span class="sxs-lookup"><span data-stu-id="b3232-1448">Not resolving ‘..’</span></span> <span data-ttu-id="b3232-1449">в DriveFs в некоторых случаях.</span><span class="sxs-lookup"><span data-stu-id="b3232-1449">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b3232-1450">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="b3232-1450">Syscall Support</span></span>
<span data-ttu-id="b3232-1451">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-1451">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b3232-1452">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="b3232-1452">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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

## <a name="build-14332"></a><span data-ttu-id="b3232-1453">Сборка 14332</span><span class="sxs-lookup"><span data-stu-id="b3232-1453">Build 14332</span></span>

<span data-ttu-id="b3232-1454">Общие сведения о сборке Windows 14332 доступны в [блоге о Windows](https://aka.ms/wip14332).</span><span class="sxs-lookup"><span data-stu-id="b3232-1454">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="b3232-1455">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-1455">Fixed</span></span>
- <span data-ttu-id="b3232-1456">Улучшенное создание resolv.conf, включая определение приоритета записей DNS.</span><span class="sxs-lookup"><span data-stu-id="b3232-1456">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="b3232-1457">Проблема с перемещением файлов и каталогов между дисками в /mnt и прочими дисками.</span><span class="sxs-lookup"><span data-stu-id="b3232-1457">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="b3232-1458">Теперь можно создавать TAR-файлы с помощью символических ссылок.</span><span class="sxs-lookup"><span data-stu-id="b3232-1458">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="b3232-1459">Добавлен каталог /run/lock по умолчанию, создаваемый при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b3232-1459">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="b3232-1460">Обновлен файл /dev/null для возврата правильных сведений stat.</span><span class="sxs-lookup"><span data-stu-id="b3232-1460">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="b3232-1461">Дополнительные ошибки при скачивании во время первого запуска.</span><span class="sxs-lookup"><span data-stu-id="b3232-1461">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="b3232-1462">Усовершенствования и исправления системных вызовов.</span><span class="sxs-lookup"><span data-stu-id="b3232-1462">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="b3232-1463">Список поддерживаемых системных вызовов приведен ниже.</span><span class="sxs-lookup"><span data-stu-id="b3232-1463">Supported syscall list below.</span></span>
- <span data-ttu-id="b3232-1464">Дополнительные улучшения исправлений ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="b3232-1464">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b3232-1465">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="b3232-1465">Syscall Support</span></span>
<span data-ttu-id="b3232-1466">Ниже приведен новый системный вызов, реализованный в WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-1466">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="b3232-1467">Системный вызов в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут поддерживаться не все параметры.</span><span class="sxs-lookup"><span data-stu-id="b3232-1467">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="b3232-1468">Сборка 14328</span><span class="sxs-lookup"><span data-stu-id="b3232-1468">Build 14328</span></span>

<span data-ttu-id="b3232-1469">Общие сведения о сборке Windows 14332 доступны в [блоге о Windows](https://aka.ms/wip14328).</span><span class="sxs-lookup"><span data-stu-id="b3232-1469">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="b3232-1470">Новые возможности</span><span class="sxs-lookup"><span data-stu-id="b3232-1470">New Features</span></span>
* <span data-ttu-id="b3232-1471">Теперь поддерживаются пользователи Linux.</span><span class="sxs-lookup"><span data-stu-id="b3232-1471">Now support Linux users.</span></span>  <span data-ttu-id="b3232-1472">При установке Bash для Ubuntu в Windows будет предложено создать пользователя Linux.</span><span class="sxs-lookup"><span data-stu-id="b3232-1472">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="b3232-1473">Дополнительные сведения: https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="b3232-1473">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="b3232-1474">В качестве имени узла теперь указывается имя компьютера Windows, а не @localhost.</span><span class="sxs-lookup"><span data-stu-id="b3232-1474">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="b3232-1475">Дополнительные сведения о сборке 14328: https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="b3232-1475">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="b3232-1476">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="b3232-1476">Fixed</span></span>
* <span data-ttu-id="b3232-1477">Улучшения символьных ссылок для файлов вне каталога /mnt/<drive>.</span><span class="sxs-lookup"><span data-stu-id="b3232-1477">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="b3232-1478">Теперь установка npm работает.</span><span class="sxs-lookup"><span data-stu-id="b3232-1478">npm install now works</span></span>
    * <span data-ttu-id="b3232-1479">Теперь можно установить JDK или JRE с помощью [этих инструкций](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span><span class="sxs-lookup"><span data-stu-id="b3232-1479">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="b3232-1480">Известная ошибка: символические ссылки не работали для подключений Windows.</span><span class="sxs-lookup"><span data-stu-id="b3232-1480">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="b3232-1481">Эта функция будет доступна в последующей сборке.</span><span class="sxs-lookup"><span data-stu-id="b3232-1481">Functionality will be available in a later build</span></span>
* <span data-ttu-id="b3232-1482">Теперь отображаются top и htop.</span><span class="sxs-lookup"><span data-stu-id="b3232-1482">top and htop now display</span></span>
* <span data-ttu-id="b3232-1483">Дополнительные сообщения об ошибке для некоторых сбоев при установке.</span><span class="sxs-lookup"><span data-stu-id="b3232-1483">Additional error messages for some install failures</span></span>
* <span data-ttu-id="b3232-1484">Усовершенствования и исправления системных вызовов.</span><span class="sxs-lookup"><span data-stu-id="b3232-1484">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="b3232-1485">Список поддерживаемых системных вызовов приведен ниже.</span><span class="sxs-lookup"><span data-stu-id="b3232-1485">Supported syscall list below.</span></span>
* <span data-ttu-id="b3232-1486">Дополнительные улучшения исправлений ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="b3232-1486">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b3232-1487">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="b3232-1487">Syscall Support</span></span>
<span data-ttu-id="b3232-1488">Ниже приведен список системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="b3232-1488">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="b3232-1489">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="b3232-1489">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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
