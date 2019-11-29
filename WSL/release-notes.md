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
ms.openlocfilehash: 2e1b8a2ae37568af273ac311572881daa8b55d4b
ms.sourcegitcommit: 3be576f946611cf36e27745bdb7c4c52af1b9928
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "74200230"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="fc0fe-105">Заметки о выпуске подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="fc0fe-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-19028"></a><span data-ttu-id="fc0fe-106">Сборка 19028</span><span class="sxs-lookup"><span data-stu-id="fc0fe-106">Build 19028</span></span>
<span data-ttu-id="fc0fe-107">Общие сведения о сборке Windows 19028 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/11/19/announcing-windows-10-insider-preview-build-19028/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-107">For general Windows information on build 19028 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/11/19/announcing-windows-10-insider-preview-build-19028/).</span></span>

* <span data-ttu-id="fc0fe-108">[WSL2] Ядро Linux обновлено до версии 4.19.81</span><span class="sxs-lookup"><span data-stu-id="fc0fe-108">[WSL2] Update Linux kernel to 4.19.81</span></span>
* <span data-ttu-id="fc0fe-109">[WSL2] Разрешение по умолчанию /dev/net/tun изменено на 0666 [GH 4629]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-109">[WSL2] Change the default permission of /dev/net/tun to 0666 [GH 4629]</span></span>
* <span data-ttu-id="fc0fe-110">[WSL2] Объем памяти, назначенный виртуальной машине Linux по умолчанию, оптимизирован до 80 % памяти узла</span><span class="sxs-lookup"><span data-stu-id="fc0fe-110">[WSL2] Tweak default amount of memory assigned to Linux VM to be 80% of host memory</span></span>
* <span data-ttu-id="fc0fe-111">[WSL2] Внесены исправления в работу сервера взаимодействия для обработки запросов со временем ожидания, чтобы сервер не перестал отвечать на запросы из-за неправильных вызовов</span><span class="sxs-lookup"><span data-stu-id="fc0fe-111">[WSL2] fix interop server to handle requests with a timeout so bad callers cannot hang the server</span></span>

## <a name="build-19018"></a><span data-ttu-id="fc0fe-112">Сборка 19018</span><span class="sxs-lookup"><span data-stu-id="fc0fe-112">Build 19018</span></span>
<span data-ttu-id="fc0fe-113">Общие сведения о сборке Windows 19018 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/11/05/announcing-windows-10-insider-preview-build-19018/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-113">For general Windows information on build 19018 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/11/05/announcing-windows-10-insider-preview-build-19018/).</span></span>

* <span data-ttu-id="fc0fe-114">[WSL2] Для исправления неполадок с приложениями .NET по умолчанию используется параметр cache=mmap для подключения ресурсов 9p.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-114">[WSL2] Use cache=mmap as the default for 9p mounts to fix dotnet apps</span></span>
* <span data-ttu-id="fc0fe-115">[WSL2] Исправления для ретранслятора localhost [GH 4340].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-115">[WSL2] Fixes for localhost relay [GH 4340]</span></span>
* <span data-ttu-id="fc0fe-116">[WSL2] Добавлен подключаемый общедоступный ресурс tmpfs для передачи состояний между дистрибутивами.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-116">[WSL2] Introduce a cross-distro shared tmpfs mount for sharing state between distros</span></span>
* <span data-ttu-id="fc0fe-117">Исправлено восстановление постоянного сетевого диска для \\\\wsl$.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-117">Fix restoring persistent network drive for \\\\wsl$</span></span>

## <a name="build-19013"></a><span data-ttu-id="fc0fe-118">Сборка 19013</span><span class="sxs-lookup"><span data-stu-id="fc0fe-118">Build 19013</span></span>
<span data-ttu-id="fc0fe-119">Общие сведения о сборке Windows 19013 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/10/29/announcing-windows-10-insider-preview-build-19013/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-119">For general Windows information on build 19013 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/29/announcing-windows-10-insider-preview-build-19013/).</span></span>

* <span data-ttu-id="fc0fe-120">[WSL2] Повышение производительности памяти служебной виртуальной машины WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-120">[WSL2] Improve memory performance of WSL utility VM.</span></span> <span data-ttu-id="fc0fe-121">Память, которая больше не используется, будет освобождена для узла.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-121">Memory that is no longer in use will be freed back to the host.</span></span>
* <span data-ttu-id="fc0fe-122">[WSL2] Ядро обновлено до версии 4.19.79.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-122">[WSL2] Update kernel version to 4.19.79.</span></span> <span data-ttu-id="fc0fe-123">(Добавлены модули CONFIG_HIGH_RES_TIMERS, CONFIG_TASK_XACCT, CONFIG_TASK_IO_ACCOUNTING, CONFIG_SCHED_HRTICK и CONFIG_BRIDGE_VLAN_FILTERING.)</span><span class="sxs-lookup"><span data-stu-id="fc0fe-123">(add CONFIG_HIGH_RES_TIMERS, CONFIG_TASK_XACCT, CONFIG_TASK_IO_ACCOUNTING, CONFIG_SCHED_HRTICK, and CONFIG_BRIDGE_VLAN_FILTERING).</span></span>
* <span data-ttu-id="fc0fe-124">[WSL2] Исправлен ретранслятор ввода для обработки ситуаций, когда STDIN является незакрытым обработчиком канала [GH 4424].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-124">[WSL2] Fix input relay to handle cases where stdin is a pipe handle that is not closed [GH 4424]</span></span>
* <span data-ttu-id="fc0fe-125">При проверке наличия \\\\wsl$ не учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-125">Make the check for \\\\wsl$ case-insensitive.</span></span>
```
[wsl2]
pageReporting = <bool>    # Enable or disable the free memory page reporting feature (default true).
idleThreshold = <integer> # Set the idle threshold for memory compaction, 0 disables the feature (default 1).
```

## <a name="build-19002"></a><span data-ttu-id="fc0fe-126">Сборка 19002</span><span class="sxs-lookup"><span data-stu-id="fc0fe-126">Build 19002</span></span>
<span data-ttu-id="fc0fe-127">Общие сведения о сборке Windows 19002 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-127">For general Windows information on build 19002 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/).</span></span>

* <span data-ttu-id="fc0fe-128">[WSL] Устранена проблема с обработкой некоторых знаков Юникода: https://github.com/microsoft/terminal/issues/2770</span><span class="sxs-lookup"><span data-stu-id="fc0fe-128">[WSL] Fix issue with handling of some Unicode characters: https://github.com/microsoft/terminal/issues/2770</span></span>
* <span data-ttu-id="fc0fe-129">[WSL] Исправлена редко возникавшая проблема, приводившая к отмене регистрации дистрибутива, если он запускался сразу после обновления сборки новой сборкой.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-129">[WSL] Fix rare cases where distros could be unregistered if launched immediately after a build-to-build upgrade.</span></span>
* <span data-ttu-id="fc0fe-130">[WSL] Устранена незначительная проблема с wsl.exe --shutdown, из-за которой таймеры бездействия экземпляра не отменялись.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-130">[WSL] Fix minor issue with wsl.exe --shutdown where instance idle timers were not cancelled.</span></span>

## <a name="build-18995"></a><span data-ttu-id="fc0fe-131">Сборка 18995</span><span class="sxs-lookup"><span data-stu-id="fc0fe-131">Build 18995</span></span>
<span data-ttu-id="fc0fe-132">Общие сведения о сборке Windows 18995 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-132">For general Windows information on build 18995 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).</span></span>

* <span data-ttu-id="fc0fe-133">[WSL2] Устранена проблема, из-за которой подключения DrvFs прекращали работать после прерывания операции (например, нажатия клавиш CTRL+C) [GH 4377].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-133">[WSL2] Fix an issue where DrvFs mounts stopped working after an operation was interrupted (e.g. ctrl-c) [GH 4377]</span></span>
* <span data-ttu-id="fc0fe-134">[WSL2] Исправлена обработка очень больших сообщений hvsocket [GH 4105].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-134">[WSL2] Fix handling of very large hvsocket messages [GH 4105]</span></span>
* <span data-ttu-id="fc0fe-135">[WSL2] Устранена проблема с взаимодействием, возникавшая, если в качестве stdin использовался файл [GH 4475].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-135">[WSL2] Fix issue with interop when stdin is a file [GH 4475]</span></span>
* <span data-ttu-id="fc0fe-136">[WSL2] Устранено аварийное завершение службы при обнаружении непредвиденного состояния сети [GH 4474].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-136">[WSL2] Fix service crash when unexpected network state is encountered [GH 4474]</span></span>
* <span data-ttu-id="fc0fe-137">[WSL2] Запрос имени дистрибутива с сервера взаимодействия, если текущий процесс не имеет переменной среды.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-137">[WSL2] Query the distro name from the interop server if the current process does not have the environment variable</span></span>
* <span data-ttu-id="fc0fe-138">[WSL2] Устранена проблема с взаимодействием, возникавшая, если в качестве stdin использовался файл.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-138">[WSL2] Fix issue with interop whe stdin is a file</span></span>
* <span data-ttu-id="fc0fe-139">[WSL2] Ядро Linux обновлено до версии 4.19.72.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-139">[WSL2] Update Linux kernel version to 4.19.72</span></span>
* <span data-ttu-id="fc0fe-140">[WSL2] Добавлена возможность указать дополнительные параметры командной строки ядра с помощью wslconfig.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-140">[WSL2] Add ability to specify additional kernel command line parameters via .wslconfig</span></span>
```
[wsl2]
kernelCommandLine = <string> # Additional kernel command line arguments
```

## <a name="build-18990"></a><span data-ttu-id="fc0fe-141">Сборка 18990</span><span class="sxs-lookup"><span data-stu-id="fc0fe-141">Build 18990</span></span>
<span data-ttu-id="fc0fe-142">Общие сведения о сборке Windows 18990 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-142">For general Windows information on build 18990 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).</span></span>

* <span data-ttu-id="fc0fe-143">Ускорен вывод списка каталогов в \\\\wsl$.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-143">Improve the performance for directory listings in \\\\wsl$</span></span>
* <span data-ttu-id="fc0fe-144">[WSL2] Внедрена дополнительная энтропия загрузки [GH 4416].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-144">[WSL2] Inject additional boot entropy [GH 4416]</span></span>
* <span data-ttu-id="fc0fe-145">[WSL2] Исправлено взаимодействие с Windows при использовании su или sudo [GH 4465].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-145">[WSL2] Fix for Windows interop when using su / sudo [GH 4465]</span></span>

## <a name="build-18980"></a><span data-ttu-id="fc0fe-146">Сборка 18980</span><span class="sxs-lookup"><span data-stu-id="fc0fe-146">Build 18980</span></span>
<span data-ttu-id="fc0fe-147">Общие сведения о сборке Windows 18980 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-147">For general Windows information on build 18980 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span></span>

* <span data-ttu-id="fc0fe-148">Исправлено чтение символических ссылок, которые запрещают FILE_READ_DATA.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-148">Fix reading symlinks that deny FILE_READ_DATA.</span></span> <span data-ttu-id="fc0fe-149">Сюда входят все символические ссылки Windows, создаваемые для обеспечения обратной совместимости, такие как "C:\Document and Settings", а также множество символических ссылок в каталоге профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-149">This includes all the symlinks Windows creates for backwards compatibility such as "C:\Document and Settings" and a bunch of symlinks in the user profile directory</span></span>
* <span data-ttu-id="fc0fe-150">Непредвиденное состояние файловой системы перестало быть неустранимым [GH 4334, 4305].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-150">Make unexpected filesystem state non-fatal [GH 4334, 4305]</span></span>
* <span data-ttu-id="fc0fe-151">[WSL2] Добавлена поддержка arm64, если ЦП или встроенное ПО поддерживает виртуализацию.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-151">[WSL2] Add support for arm64 if your CPU / firmware supports virtualization</span></span>
* <span data-ttu-id="fc0fe-152">[WSL2] Непривилегированным пользователям разрешено просматривать журнал ядра.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-152">[WSL2] Allow unprivileged users to view kernel log</span></span>
* <span data-ttu-id="fc0fe-153">[WSL2] Исправлена ретрансляция вывода при закрытии сокетов stdout и stderr [GH 4375].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-153">[WSL2] Fix output relay when stdout / stderr sockets have been closed [GH 4375]</span></span>
* <span data-ttu-id="fc0fe-154">[WSL2] Поддержка сквозного режима батареи и адаптера питания.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-154">[WSL2] Support battery and AC adapter passthrough</span></span>
* <span data-ttu-id="fc0fe-155">[WSL2] Ядро Linux обновлено до версии 4.19.67.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-155">[WSL2] Update Linux kernel to 4.19.67</span></span>
* <span data-ttu-id="fc0fe-156">Добавлена возможность задать имя пользователя по умолчанию в /etc/wsl.conf:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-156">Add the ability to set default username in /etc/wsl.conf:</span></span>
```
[user]
default=<string>
```

## <a name="build-18975"></a><span data-ttu-id="fc0fe-157">Сборка 18975</span><span class="sxs-lookup"><span data-stu-id="fc0fe-157">Build 18975</span></span>
<span data-ttu-id="fc0fe-158">Общие сведения о сборке Windows 18975 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-158">For general Windows information on build 18975 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span></span>

* <span data-ttu-id="fc0fe-159">[WSL2] Исправлен ряд проблем с надежностью localhost [GH 4340].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-159">[WSL2] Fixed a number of localhost reliability issues [GH 4340]</span></span>

## <a name="build-18970"></a><span data-ttu-id="fc0fe-160">Сборка 18970</span><span class="sxs-lookup"><span data-stu-id="fc0fe-160">Build 18970</span></span>
<span data-ttu-id="fc0fe-161">Общие сведения о сборке Windows 18970 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-161">For general Windows information on build 18970 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span></span>

* <span data-ttu-id="fc0fe-162">[WSL2] Синхронизация времени с временем узла при выходе системы из спящего режима [GH 4245].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-162">[WSL2] Sync time with host time when system resumes from sleep state [GH 4245]</span></span>
* <span data-ttu-id="fc0fe-163">[WSL2] Создание символических ссылок NT на тома Windows, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-163">[WSL2] Create NT symlinks on the Windows volumes when possible.</span></span>
* <span data-ttu-id="fc0fe-164">[WSL2] Создание дистрибутивов в пространствах имен UTS, IPC, PID и Mount.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-164">[WSL2] Create distros in UTS, IPC, PID, and Mount namespaces.</span></span>
* <span data-ttu-id="fc0fe-165">[WSL2] Исправлена ретрансляция портов localhost при привязке сервера к localhost напрямую [GH 4353].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-165">[WSL2] Fix localhost port relay when server binds to localhost directly [GH 4353]</span></span>
* <span data-ttu-id="fc0fe-166">[WSL2] Исправлено взаимодействие при перенаправлении вывода [GH 4337].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-166">[WSL2] Fix interop when output is redirected [GH 4337]</span></span>
* <span data-ttu-id="fc0fe-167">[WSL2] Поддержка преобразования абсолютных символических ссылок NT.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-167">[WSL2] Support translating absolute NT symlinks.</span></span>
* <span data-ttu-id="fc0fe-168">[WSL2] Ядро обновлено до версии 4.19.59.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-168">[WSL2] Update kernel to 4.19.59</span></span>
* <span data-ttu-id="fc0fe-169">[WSL2] Правильное задание маски подсети для eth0.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-169">[WSL2] Properly set subnet mask for eth0.</span></span>
* <span data-ttu-id="fc0fe-170">[WSL2] Изменение логики для выхода из циклов консольного рабочего процесса при получении сигнала о событии выхода.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-170">[WSL2] Change logic to break out of console worker loop when exit event is signaled.</span></span>
* <span data-ttu-id="fc0fe-171">[WSL2] Если дистрибутив не работает, то его VHD-файл можно извлечь.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-171">[WSL2] Eject distribution vhd when the distro is not running.</span></span>
* <span data-ttu-id="fc0fe-172">[WSL2] Исправлена библиотека анализа конфигурации, чтобы правильно обрабатывать пустые значения.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-172">[WSL2] Fix config parsing library to correctly handle empty values.</span></span>
* <span data-ttu-id="fc0fe-173">[WSL2] Поддержка рабочего стола Docker путем создания подключений между дистрибутивами.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-173">[WSL2] Support Docker Desktop by creating cross distro mounts.</span></span> <span data-ttu-id="fc0fe-174">Дистрибутив можно настроить для такого режима, добавив следующую строку в файл /etc/wsl.conf:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-174">A distro can opt-in to this behavior by adding the following line to the /etc/wsl.conf file:</span></span>
```
[automount]
crossDistro = true
```

## <a name="build-18945"></a><span data-ttu-id="fc0fe-175">Сборка 18945</span><span class="sxs-lookup"><span data-stu-id="fc0fe-175">Build 18945</span></span>
<span data-ttu-id="fc0fe-176">Общие сведения о сборке Windows 18945 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-176">For general Windows information on build 18945 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-177">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-177">WSL</span></span>
* <span data-ttu-id="fc0fe-178">[WSL2] Разрешен доступ к ожидающим передачи данных TCP-сокетам в WSL2 с узла по адресу localhost:<порт>.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-178">[WSL2] Allow listening tcp sockets in WSL2 to be accessible from the host by using localhost:port</span></span>
* <span data-ttu-id="fc0fe-179">[WSL2] Устранены сбои при установке и преобразовании. Добавлена дополнительная диагностика для отслеживания будущих проблем [GH 4105].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-179">[WSL2] Fixes for install / conversion failures and additional diagnostics to track down future issues [GH 4105]</span></span> 
* <span data-ttu-id="fc0fe-180">[WSL2] Улучшена диагностируемость проблем с сетью WSL2.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-180">[WSL2] Improve diagnosability of WSL2 network issues</span></span>
* <span data-ttu-id="fc0fe-181">[WSL2] Ядро обновлено до версии 4.19.55.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-181">[WSL2] Update kernel version to 4.19.55</span></span>
* <span data-ttu-id="fc0fe-182">[WSL2] Ядро обновлено с помощью параметров конфигурации, необходимых для Docker [GH 4165].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-182">[WSL2] Update kernel with config options required for docker [GH 4165]</span></span>
* <span data-ttu-id="fc0fe-183">[WSL2] Увеличено число ЦП, назначаемых упрощенной служебной виртуальной машине, чтобы оно совпадало с числом ЦП узла (ранее это значение было ограничено 8 ЦП с помощью параметра CONFIG_NR_CPUS в конфигурации ядра) [GH 4137].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-183">[WSL2] Increase the number of CPUs assigned to the lightweight utility VM to be the same as the host (was previously capped at 8 by CONFIG_NR_CPUS in the kernel config) [GH 4137]</span></span>
* <span data-ttu-id="fc0fe-184">[WSL2] Создание файла подкачки для упрощенной виртуальной машины WSL2.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-184">[WSL2] Create a swap file for the WSL2 lightweight VM</span></span>
* <span data-ttu-id="fc0fe-185">[WSL2] Разрешено отображение подключений пользователей в \\\\wsl$\\<имя_дистрибутива> (например, sshfs) [GH 4172].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-185">[WSL2] Allow user mounts to be visible via \\\\wsl$\\distro (for example sshfs) [GH 4172]</span></span>
* <span data-ttu-id="fc0fe-186">[WSL2] Повышена производительность файловой системы 9p.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-186">[WSL2] Improve 9p filesystem performance</span></span>
* <span data-ttu-id="fc0fe-187">[WSL2] Предотвращение неограниченного роста списка ACL виртуального жесткого диска [GH 4126].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-187">[WSL2] Ensure vhd ACL does not grow unbounded [GH 4126]</span></span>
* <span data-ttu-id="fc0fe-188">[WSL2] Обновлена конфигурации ядра для поддержки squashfs и xt_conntrack [GH 4107, 4123].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-188">[WSL2] Update kernel config to support squashfs and xt_conntrack [GH 4107, 4123]</span></span>
* <span data-ttu-id="fc0fe-189">[WSL2] Исправлен параметр interop.enabled в /etc/wsl.conf [GH 4140].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-189">[WSL2] Fix for interop.enabled /etc/wsl.conf option [GH 4140]</span></span>
* <span data-ttu-id="fc0fe-190">[WSL2] Если файловая система не поддерживает EA, возвращается ENOTSUP.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-190">[WSL2] Return ENOTSUP if the file system does not support EAs</span></span>
* <span data-ttu-id="fc0fe-191">[WSL2] CopyFile больше не прекращает отвечать на запросы при работе с \\\\wsl$.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-191">[WSL2] Fix CopyFile hang with \\\\wsl$</span></span>
* <span data-ttu-id="fc0fe-192">Параметр umask по умолчанию переключен на значение 0022, и добавлен параметр filesystem.umask в /etc/wsl.conf.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-192">Switch default umask to 0022 and add filesystem.umask setting to /etc/wsl.conf</span></span>
* <span data-ttu-id="fc0fe-193">Исправлен wslpath, чтобы правильно разрешать символические ссылки, что повторно происходило в 19h1 [GH 4078].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-193">Fix wslpath to properly resolve symlinks, this was regressed in 19h1 [GH 4078]</span></span>
* <span data-ttu-id="fc0fe-194">Введен файл %UserProfile%\\.wslconfig для настройки параметров WSL2.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-194">Introduce %UserProfile%\\.wslconfig file for tweaking WSL2 settings</span></span>
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

## <a name="build-18917"></a><span data-ttu-id="fc0fe-195">Сборка 18917</span><span class="sxs-lookup"><span data-stu-id="fc0fe-195">Build 18917</span></span>
<span data-ttu-id="fc0fe-196">Общие сведения о сборке Windows 18917 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-196">For general Windows information on build 18917 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-197">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-197">WSL</span></span>
* <span data-ttu-id="fc0fe-198">Уже доступна версия WSL 2!</span><span class="sxs-lookup"><span data-stu-id="fc0fe-198">WSL 2 is now available!</span></span> <span data-ttu-id="fc0fe-199">Дополнительные сведения см. в [блоге](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-199">Please see [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) for more details.</span></span>
* <span data-ttu-id="fc0fe-200">Устранена регрессия, из-за которой запуск процессов Windows через символические ссылки выполнялся некорректно [GH 3999].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-200">Fix a regression where launching Windows processes via symlinks did not work correctly [GH 3999]</span></span>
* <span data-ttu-id="fc0fe-201">Добавлены следующие параметры wsl.exe: wsl.exe --list --verbose, wsl.exe --list --quiet и wsl.exe --import --version.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-201">Add wsl.exe --list --verbose, wsl.exe --list --quiet, and wsl.exe --import --version options to wsl.exe</span></span>
* <span data-ttu-id="fc0fe-202">Добавлен параметр wsl.exe --shutdown.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-202">Add wsl.exe --shutdown option</span></span>
* <span data-ttu-id="fc0fe-203">Plan 9: для успешной работы разрешено открытие каталога для записи.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-203">Plan 9: Allow opening a directory for write to succeed</span></span>

## <a name="build-18890"></a><span data-ttu-id="fc0fe-204">Сборка 18890</span><span class="sxs-lookup"><span data-stu-id="fc0fe-204">Build 18890</span></span>
<span data-ttu-id="fc0fe-205">Общие сведения о сборке Windows 18890 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-205">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-206">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-206">WSL</span></span>
* <span data-ttu-id="fc0fe-207">Утечка сокетов не блокирует работу [GH 2913].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-207">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="fc0fe-208">Ввод EOF в терминал может заблокировать последующие операции чтения [GH 3421].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-208">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="fc0fe-209">В заголовок resolv.conf добавлена ссылка на wsl.conf [рассмотрено в GH 3928].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-209">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="fc0fe-210">Взаимоблокировка в коде epoll delete [GH 3922].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-210">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="fc0fe-211">Обработка пробелов в аргументах параметров --import и --export [GH 3932].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-211">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="fc0fe-212">Расширение файлов, обработанных mmap, не работает должным образом [GH 3939].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-212">Extending mmap’d files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="fc0fe-213">Устранена проблема с доступом ARM64 к \\\\wsl$.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-213">Fix issue with ARM64 \\\\wsl$ access not working properly</span></span>
* <span data-ttu-id="fc0fe-214">Улучшен значок по умолчанию для wsl.exe.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-214">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="fc0fe-215">Сборка 18342</span><span class="sxs-lookup"><span data-stu-id="fc0fe-215">Build 18342</span></span>
<span data-ttu-id="fc0fe-216">Общие сведения о сборке Windows 18342 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-216">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-217">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-217">WSL</span></span>
* <span data-ttu-id="fc0fe-218">Мы добавили возможность доступа пользователей к файлам Linux в дистрибутиве WSL из Windows.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-218">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="fc0fe-219">Доступ к этим файлам можно получить с помощью командной строки. Кроме того, такие приложения для Windows, как проводник, VSCode и т. д., могут взаимодействовать с этими файлами.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-219">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="fc0fe-220">Чтобы получить доступ к файлам, перейдите в папку \\\\wsl$\\<имя_дистрибутива>, или просмотрите список выполняющихся дистрибутивов, перейдя в \\\\wsl$.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-220">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="fc0fe-221">Добавлены дополнительные теги сведений о ЦП и исправлены значения Cpus_allowed[_list] [GH 2234].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-221">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="fc0fe-222">Поддержка выполнения из ведомого потока [GH 3800].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-222">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="fc0fe-223">Ошибки обновления конфигурации не считаются критическими [GH 3785].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-223">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="fc0fe-224">Подсистема binfmt обновлена для правильной обработки смещений [GH 3768].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-224">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="fc0fe-225">Включено сопоставление сетевых дисков для Plan 9 [GH 3854].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-225">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="fc0fe-226">Поддержка преобразования путей Windows в Linux и наоборот для подключения привязок.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-226">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="fc0fe-227">Создание разделов только для чтения для сопоставлений файлов, открытых только для чтения.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-227">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="fc0fe-228">Сборка 18334</span><span class="sxs-lookup"><span data-stu-id="fc0fe-228">Build 18334</span></span>
<span data-ttu-id="fc0fe-229">Общие сведения о сборке Windows 18334 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-229">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-230">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-230">WSL</span></span>
* <span data-ttu-id="fc0fe-231">Перепроектирован способ сопоставления часового пояса Windows с часовым поясом Linux [GH 3747].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-231">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="fc0fe-232">Устранены утечки памяти и добавлены новые функции преобразования строк [GH 3746].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-232">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="fc0fe-233">Выполнение SIGCONT для группы потоков без потоков является холостой командой [GH 3741].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-233">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="fc0fe-234">Правильное отображение дескрипторов файлов socket и epoll в /proc/self/fd.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-234">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="fc0fe-235">Сборка 18305</span><span class="sxs-lookup"><span data-stu-id="fc0fe-235">Build 18305</span></span>
<span data-ttu-id="fc0fe-236">Общие сведения о сборке Windows 18305 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-236">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-237">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-237">WSL</span></span>
* <span data-ttu-id="fc0fe-238">Когда основной поток завершает работу, pthreads утрачивает доступ к файлам [GH 3589].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-238">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="fc0fe-239">Команда TIOCSCTTY должна игнорировать параметр force, если он не является обязательным [GH 3652].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-239">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="fc0fe-240">Усовершенствована командная строка wsl.exe и добавлены функции импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-240">wsl.exe command line improvements and addition of import / export functionality.</span></span>
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

## <a name="build-18277"></a><span data-ttu-id="fc0fe-241">Сборка 18277</span><span class="sxs-lookup"><span data-stu-id="fc0fe-241">Build 18277</span></span>
<span data-ttu-id="fc0fe-242">Общие сведения о сборке Windows 18277 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-242">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-243">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-243">WSL</span></span>
* <span data-ttu-id="fc0fe-244">Устранена ошибка "Интерфейс не поддерживается" в сборке 18272 [GH 3645].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-244">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="fc0fe-245">Игнорируется флаг MNT_FORCE для umount syscall [GH 3605].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-245">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="fc0fe-246">Переключено взаимодействие WSL для использования официального API CreatePseudoConsole.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-246">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="fc0fe-247">При перезапуске FUTEX_WAIT значение времени ожидания не сохраняется.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-247">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="fc0fe-248">Сборка 18272</span><span class="sxs-lookup"><span data-stu-id="fc0fe-248">Build 18272</span></span>
<span data-ttu-id="fc0fe-249">Общие сведения о сборке Windows 18272 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-249">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-250">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-250">WSL</span></span>
* <span data-ttu-id="fc0fe-251">**Предупреждение**. В этой сборке есть проблема, делающая компонент WSL неработоспособным.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-251">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="fc0fe-252">При попытке запустить дистрибутив появится сообщение об ошибке "Интерфейс не поддерживается".</span><span class="sxs-lookup"><span data-stu-id="fc0fe-252">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="fc0fe-253">Эта проблема устранена, и соответствующее исправление будет добавлено в сборку для предварительной оценки с ранним доступом, выпускаемую на следующей неделе.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-253">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="fc0fe-254">Если вы установили эту сборку, то вы можете вернуться к предыдущей сборке Windows, выбрав "Параметры > Обновление и безопасность > Восстановление" и щелкнув "Вернуться к предыдущей версии Windows 10".</span><span class="sxs-lookup"><span data-stu-id="fc0fe-254">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="fc0fe-255">Сборка 18267</span><span class="sxs-lookup"><span data-stu-id="fc0fe-255">Build 18267</span></span>
<span data-ttu-id="fc0fe-256">Общие сведения о сборке Windows 18267 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-256">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-257">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-257">WSL</span></span>
* <span data-ttu-id="fc0fe-258">Устранена проблема, из-за которой зомби-процесс мог быть не удален и существовал неограниченное время.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-258">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="fc0fe-259">WslRegisterDistribution переставал отвечать на запросы, если сообщение об ошибке превышало максимальную длину [GH 3592].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-259">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="fc0fe-260">Разрешено использование fsync с файлами только для чтения в DrvFs [GH 3556].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-260">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="fc0fe-261">Перед созданием символических ссылок в каталогах /bin и /sbin убедитесь, что эти каталоги существуют [GH 3584].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-261">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="fc0fe-262">Добавлен механизм времени ожидания завершения экземпляра для экземпляров WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-262">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="fc0fe-263">Сейчас время ожидания равно 15 секундам, то есть работа экземпляра завершается через 15 секунд после завершения последнего процесса WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-263">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="fc0fe-264">Чтобы немедленно завершить дистрибутив, используйте следующую команду.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-264">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="fc0fe-265">Сборка 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="fc0fe-265">Build 17763 (1809)</span></span>
<span data-ttu-id="fc0fe-266">Общие сведения о сборке Windows 17763 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-266">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-267">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-267">WSL</span></span>
* <span data-ttu-id="fc0fe-268">Проверка разрешения SetPriority для syscall была слишком строгая для изменения приоритета того же потока [GH 1838].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-268">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="fc0fe-269">Убедитесь, что для времени загрузки используется несмещенное время прерывания, чтобы избежать возврата отрицательных значений clock_gettime (CLOCK_BOOTTIME) [GH 3434].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-269">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="fc0fe-270">Обработка символических ссылок в интерпретаторе binfmt для WSL [GH 3424].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-270">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="fc0fe-271">Улучшена обработка очистки дескриптора файла ведущего потока группы потоков.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-271">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="fc0fe-272">Чтобы избежать переполнения, переключите WSL на использование KeQueryInterruptTimePrecise вместо KeQueryPerformanceCounter [GH 3252].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-272">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="fc0fe-273">Подключение Ptrace могло вызывать неправильное возвращаемое значение из системных вызовов [GH 1731].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-273">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="fc0fe-274">Устранено несколько проблем, связанных с AF_UNIX [GH 3371].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-274">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="fc0fe-275">Устранена проблема, которая могла привести к сбою взаимодействия WSL, если длина текущего рабочего каталога была меньше 5 знаков [GH 3379].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-275">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="fc0fe-276">Предотвращена задержка в 1 секунду при сбое замыкания на себя подключений к несуществующим портам (GH 3286).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-276">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="fc0fe-277">Добавлен файл заглушки /proc/sys/fs/file-max [GH 2893].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-277">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="fc0fe-278">Уточнены сведения об области действия IPv6.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-278">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="fc0fe-279">Поддержка PR_SET_PTRACER [GH 3053].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-279">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="fc0fe-280">Канальная файловая система необоснованно очищала событие epoll, активируемое переходом [GH 3276].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-280">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="fc0fe-281">Исполняемый файл Win32, запущенный с помощью символической ссылки NTFS, не учитывал имя символической ссылки [GH 2909].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-281">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="fc0fe-282">Улучшена поддержка зомби [GH 1353].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-282">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="fc0fe-283">Добавлены записи wsl.conf для управления поведением взаимодействия с Windows [GH 1493].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-283">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="fc0fe-284">Устранена проблема, из-за которой команда getsockname не всегда возвращала тип семейства сокетов UNIX [GH 1774].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-284">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="fc0fe-285">Добавлена поддержка TIOCSTI [GH 1863].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-285">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="fc0fe-286">Неблокирующие сокеты в процессе подключения должны возвращать EAGAIN для попыток записи [GH 2846].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-286">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="fc0fe-287">Поддержка взаимодействия с подключенными виртуальными жесткими дисками [GH 3246, 3291].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-287">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="fc0fe-288">Устранена проблема с проверкой разрешений для корневой папки [GH 3304].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-288">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="fc0fe-289">Ограниченная поддержка вызовов ioctl с аргументами KDGKBTYPE, KDGKBMODE и KDSKBMODE для клавиатуры tty.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-289">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="fc0fe-290">Приложения пользовательского интерфейса Windows должны выполняться, даже если они запущены в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-290">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="fc0fe-291">Добавлен параметр wsl --u или --user [GH 1203].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-291">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="fc0fe-292">Устранены проблемы с запуском WSL, когда включен быстрый запуск [GH 2576].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-292">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="fc0fe-293">Сокеты UNIX должны хранить учетные данные отключенных одноранговых узлов [GH 3183].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-293">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="fc0fe-294">Работа неблокирующих сокетов UNIX неограниченное время завершалась сбоем и возвращалось значение EAGAIN [GH 3191].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-294">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="fc0fe-295">Новый тип подключения drvfs по умолчанию case=off [GH 2937, 3212, 3328].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-295">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="fc0fe-296">Дополнительные сведения см. в [этом блоге](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-296">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="fc0fe-297">Добавлен параметр wslconfig /terminate для остановки выполнения дистрибутивов.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-297">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="fc0fe-298">Устранена проблема с пунктами в контекстном меню оболочки WSL, из-за которой неправильно обрабатывались пути с пробелами.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-298">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="fc0fe-299">Учет регистра в именах каталогов реализован в качестве расширенного атрибута.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-299">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="fc0fe-300">ARM64: имитация операций обслуживания кэша.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-300">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="fc0fe-301">Устранена [проблема с dotnet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-301">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="fc0fe-302">DrvFs: в частном диапазоне допускаются только неэкранированные знаки, которые соответствуют экранированному знаку.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-302">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="fc0fe-303">Устранена ошибка завышения или занижения на единицу при проверке длины интерпретатором анализатора ELF [GH 3154].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-303">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="fc0fe-304">Абсолютные таймеры WSL со временем в прошлом не срабатывали [GH 3091].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-304">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="fc0fe-305">Убедитесь, что вновь созданные точки повторного анализа указаны как таковые в родительском каталоге.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-305">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="fc0fe-306">Атомарное создание каталогов с учетом регистра в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-306">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="fc0fe-307">Устранена дополнительная проблема, из-за которой многопоточные операции могли возвращать ENOENT, даже если файл существовал.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-307">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="fc0fe-308">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-308">[GH 2712]</span></span>
* <span data-ttu-id="fc0fe-309">Устранена ошибка запуска WSL при включенном режиме UMCI.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-309">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="fc0fe-310">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-310">[GH 3020]</span></span>
* <span data-ttu-id="fc0fe-311">Добавлено контекстное меню обозревателя для запуска WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-311">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="fc0fe-312">Чтобы открыть его, нажмите и удерживайте клавишу SHIFT и щелкните правой кнопкой мыши в окне проводника.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-312">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="fc0fe-313">Устранено неблокирующее поведение сокетов UNIX [GH 2822, 3100].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-313">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="fc0fe-314">Устранена проблема, из-за которой команда NETLINK переставала отвечать на запросы, как было сообщено в GH 2026.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-314">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="fc0fe-315">Добавлена поддержка флагов распространения подключения [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-315">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="fc0fe-316">Устранена проблема, из-за которой усечение не вызывало события inotify [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-316">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="fc0fe-317">Добавлен параметр --exec для wsl.exe, позволяющий вызвать отдельный двоичный файл без оболочки.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-317">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="fc0fe-318">Добавлен параметр --distribution для wsl.exe, позволяющий выбрать конкретный дистрибутив.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-318">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="fc0fe-319">Ограниченная поддержка dmesg.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-319">Limited support for dmesg.</span></span> <span data-ttu-id="fc0fe-320">Теперь приложения могут входить в dmesg.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-320">Applications can now log to dmesg.</span></span> <span data-ttu-id="fc0fe-321">Драйвер WSL записывает ограниченные сведения в dmesg.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-321">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="fc0fe-322">В будущем эти возможности можно будет расширить, чтобы записывать другие сведения и данные диагностики из драйвера.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-322">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="fc0fe-323">Примечание. Сейчас dmesg поддерживается через интерфейс устройства `/dev/kmsg`.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-323">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="fc0fe-324">Интерфейс syscall `syslog` пока не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-324">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="fc0fe-325">Поэтому некоторые параметры командной строки `dmesg`, такие как `-S` и `-C`, не работают.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-325">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="fc0fe-326">Изменены GID и режим по умолчанию для последовательных устройств, чтобы обеспечить соответствие собственному режиму [GH 3042].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-326">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="fc0fe-327">Теперь DrvFs поддерживает расширенные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-327">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="fc0fe-328">Примечание. В DrvFs были некоторые ограничения для имен расширенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-328">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="fc0fe-329">Некоторые знаки (например, "/", ":" и "\*") не допускаются, а в именах расширенных атрибутов в DrvFs не учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-329">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="fc0fe-330">Сборка 18252 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="fc0fe-330">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="fc0fe-331">Общие сведения о сборке Windows 18252 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-331">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-332">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-332">WSL</span></span>
* <span data-ttu-id="fc0fe-333">Двоичные файлы init и bsdtar перемещены из библиотеки DLL lxssmanager в отдельную папку tools.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-333">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="fc0fe-334">Устранено состязание при закрытии дескриптора файла в случае использования CLONE_FILES.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-334">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="fc0fe-335">Обработка необязательных полей в /proc/pid/mountinfo при преобразовании путей DrvFs.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-335">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="fc0fe-336">Допускается успешное выполнение mknod DrvFs без поддержки метаданных для S_IFREG.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-336">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="fc0fe-337">Файлы только для чтения, созданные в DrvFs, должны иметь атрибут readonly [GH 3411].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-337">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="fc0fe-338">Добавлено вспомогательное приложение /sbin/mount.drvfs для управления подключением DrvFs.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-338">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="fc0fe-339">Использование переименования POSIX в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-339">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="fc0fe-340">Разрешено преобразование путей в томах без GUID тома.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-340">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="fc0fe-341">Сборка 17738 (Fast)</span><span class="sxs-lookup"><span data-stu-id="fc0fe-341">Build 17738 (Fast)</span></span>
<span data-ttu-id="fc0fe-342">Общие сведения о сборке Windows 17738 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-342">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-343">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-343">WSL</span></span>
* <span data-ttu-id="fc0fe-344">Проверка разрешения SetPriority для syscall была слишком строгая для изменения приоритета того же потока [GH 1838].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-344">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="fc0fe-345">Убедитесь, что для времени загрузки используется несмещенное время прерывания, чтобы избежать возврата отрицательных значений clock_gettime (CLOCK_BOOTTIME) [GH 3434].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-345">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="fc0fe-346">Обработка символических ссылок в интерпретаторе binfmt для WSL [GH 3424].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-346">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="fc0fe-347">Улучшена обработка очистки дескриптора файла ведущего потока группы потоков.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-347">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="fc0fe-348">Сборка 17728 (Fast)</span><span class="sxs-lookup"><span data-stu-id="fc0fe-348">Build 17728 (Fast)</span></span>
<span data-ttu-id="fc0fe-349">Общие сведения о сборке Windows 17728 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-349">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-350">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-350">WSL</span></span>
* <span data-ttu-id="fc0fe-351">Чтобы избежать переполнения, переключите WSL на использование KeQueryInterruptTimePrecise вместо KeQueryPerformanceCounter [GH 3252].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-351">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="fc0fe-352">Подключение Ptrace могло вызывать неправильное возвращаемое значение из системных вызовов [GH 1731].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-352">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="fc0fe-353">Устранен ряд проблем, связанных с AF_UNIX [GH 3371].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-353">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="fc0fe-354">Устранена проблема, которая могла привести к сбою взаимодействия WSL, если длина текущего рабочего каталога была меньше 5 знаков [GH 3379].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-354">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="fc0fe-355">Сборка 18204 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="fc0fe-355">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="fc0fe-356">Общие сведения о сборке Windows 18204 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-356">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-357">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-357">WSL</span></span>
* <span data-ttu-id="fc0fe-358">Канальная файловая система необоснованно очищала событие epoll, активируемое переходом [GH 3276].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-358">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="fc0fe-359">Исполняемый файл Win32, запущенный с помощью символической ссылки NTFS, не учитывал имя символической ссылки [GH 2909].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-359">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="fc0fe-360">Сборка 17723 (Fast)</span><span class="sxs-lookup"><span data-stu-id="fc0fe-360">Build 17723 (Fast)</span></span>
<span data-ttu-id="fc0fe-361">Общие сведения о сборке Windows 17723 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-361">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-362">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-362">WSL</span></span>
* <span data-ttu-id="fc0fe-363">Предотвращена задержка в 1 секунду при сбое замыкания на себя подключений к несуществующим портам (GH 3286).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-363">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="fc0fe-364">Добавлен файл заглушки /proc/sys/fs/file-max [GH 2893].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-364">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="fc0fe-365">Уточнены сведения об области действия IPv6.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-365">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="fc0fe-366">Поддержка PR_SET_PTRACER [GH 3053].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-366">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="fc0fe-367">Канальная файловая система необоснованно очищала событие epoll, активируемое переходом [GH 3276].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-367">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="fc0fe-368">Исполняемый файл Win32, запущенный с помощью символической ссылки NTFS, не учитывал имя символической ссылки [GH 2909].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-368">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="fc0fe-369">Сборка 17713</span><span class="sxs-lookup"><span data-stu-id="fc0fe-369">Build 17713</span></span>
<span data-ttu-id="fc0fe-370">Общие сведения о сборке Windows 17713 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-370">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-371">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-371">WSL</span></span>
* <span data-ttu-id="fc0fe-372">Улучшена поддержка зомби [GH 1353].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-372">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="fc0fe-373">Добавлены записи wsl.conf для управления поведением взаимодействия с Windows [GH 1493].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-373">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="fc0fe-374">Устранена проблема, из-за которой команда getsockname не всегда возвращала тип семейства сокетов UNIX [GH 1774].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-374">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="fc0fe-375">Добавлена поддержка TIOCSTI [GH 1863].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-375">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="fc0fe-376">Неблокирующие сокеты в процессе подключения должны возвращать EAGAIN для попыток записи [GH 2846].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-376">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="fc0fe-377">Поддержка взаимодействия с подключенными виртуальными жесткими дисками [GH 3246, 3291].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-377">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="fc0fe-378">Устранена проблема с проверкой разрешений для корневой папки [GH 3304].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-378">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="fc0fe-379">Ограниченная поддержка вызовов ioctl с аргументами KDGKBTYPE, KDGKBMODE и KDSKBMODE для клавиатуры tty.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-379">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="fc0fe-380">Приложения пользовательского интерфейса Windows должны выполняться, даже если они запущены в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-380">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="fc0fe-381">Сборка 17704</span><span class="sxs-lookup"><span data-stu-id="fc0fe-381">Build 17704</span></span>
<span data-ttu-id="fc0fe-382">Общие сведения о сборке Windows 17704 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-382">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-383">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-383">WSL</span></span>
* <span data-ttu-id="fc0fe-384">Добавлен параметр wsl --u или --user [GH 1203].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-384">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="fc0fe-385">Устранены проблемы с запуском WSL, когда включен быстрый запуск [GH 2576].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-385">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="fc0fe-386">Сокеты UNIX должны хранить учетные данные отключенных одноранговых узлов [GH 3183].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-386">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="fc0fe-387">Работа неблокирующих сокетов UNIX неограниченное время завершалась сбоем и возвращалось значение EAGAIN [GH 3191].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-387">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="fc0fe-388">Новый тип подключения drvfs по умолчанию case=off [GH 2937, 3212, 3328].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-388">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="fc0fe-389">Дополнительные сведения см. в [этом блоге](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-389">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="fc0fe-390">Добавлен параметр wslconfig /terminate для остановки выполнения дистрибутивов.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-390">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="fc0fe-391">Сборка 17692</span><span class="sxs-lookup"><span data-stu-id="fc0fe-391">Build 17692</span></span>
<span data-ttu-id="fc0fe-392">Общие сведения о сборке Windows 17692 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-392">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-393">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-393">WSL</span></span>
* <span data-ttu-id="fc0fe-394">Устранена проблема с пунктами в контекстном меню оболочки WSL, из-за которой неправильно обрабатывались пути с пробелами.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-394">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="fc0fe-395">Учет регистра в именах каталогов реализован в качестве расширенного атрибута.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-395">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="fc0fe-396">ARM64: имитация операций обслуживания кэша.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-396">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="fc0fe-397">Устранена [проблема с dotnet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-397">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="fc0fe-398">DrvFs: в частном диапазоне допускаются только неэкранированные знаки, которые соответствуют экранированному знаку.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-398">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="fc0fe-399">Сборка 17686</span><span class="sxs-lookup"><span data-stu-id="fc0fe-399">Build 17686</span></span>
<span data-ttu-id="fc0fe-400">Общие сведения о сборке Windows 17686 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-400">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-401">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-401">WSL</span></span>
* <span data-ttu-id="fc0fe-402">Устранена ошибка завышения или занижения на единицу при проверке длины интерпретатором анализатора ELF [GH 3154].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-402">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="fc0fe-403">Абсолютные таймеры WSL со временем в прошлом не срабатывали [GH 3091].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-403">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="fc0fe-404">Убедитесь, что вновь созданные точки повторного анализа указаны как таковые в родительском каталоге.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-404">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="fc0fe-405">Атомарное создание каталогов с учетом регистра в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-405">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="fc0fe-406">Сборка 17677</span><span class="sxs-lookup"><span data-stu-id="fc0fe-406">Build 17677</span></span>
<span data-ttu-id="fc0fe-407">Общие сведения о сборке Windows 17677 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-407">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-408">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-408">WSL</span></span>
* <span data-ttu-id="fc0fe-409">Устранена дополнительная проблема, из-за которой многопоточные операции могли возвращать ENOENT, даже если файл существовал.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-409">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="fc0fe-410">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-410">[GH 2712]</span></span>
* <span data-ttu-id="fc0fe-411">Устранена ошибка запуска WSL при включенном режиме UMCI.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-411">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="fc0fe-412">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-412">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="fc0fe-413">Сборка 17666</span><span class="sxs-lookup"><span data-stu-id="fc0fe-413">Build 17666</span></span>
<span data-ttu-id="fc0fe-414">Общие сведения о сборке Windows 17666 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-414">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-415">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-415">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="fc0fe-416">ПРЕДУПРЕЖДЕНИЕ! Существует проблема, препятствующая запуску WSL на некоторых наборах микросхем AMD [GH 3134].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-416">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="fc0fe-417">Исправление готово и находится в процессе добавления в ветвь сборок для программы предварительной оценки Windows.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-417">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="fc0fe-418">Добавлено контекстное меню обозревателя для запуска WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-418">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="fc0fe-419">Чтобы открыть его, нажмите и удерживайте клавишу SHIFT и щелкните правой кнопкой мыши в окне проводника.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-419">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="fc0fe-420">Устранено неблокирующее поведение сокетов UNIX [GH 2822, 3100].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-420">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="fc0fe-421">Устранена проблема, из-за которой команда NETLINK переставала отвечать на запросы, как было сообщено в GH 2026.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-421">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="fc0fe-422">Добавлена поддержка флагов распространения подключения [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-422">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="fc0fe-423">Устранена проблема, из-за которой усечение не вызывало события inotify [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-423">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="fc0fe-424">Добавлен параметр --exec для wsl.exe, позволяющий вызвать отдельный двоичный файл без оболочки.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-424">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="fc0fe-425">Добавлен параметр --distribution для wsl.exe, позволяющий выбрать конкретный дистрибутив.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-425">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="fc0fe-426">Сборка 17655 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="fc0fe-426">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="fc0fe-427">Общие сведения о сборке Windows 17655 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-427">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-428">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-428">WSL</span></span>
* <span data-ttu-id="fc0fe-429">Ограниченная поддержка dmesg.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-429">Limited support for dmesg.</span></span> <span data-ttu-id="fc0fe-430">Теперь приложения могут входить в dmesg.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-430">Applications can now log to dmesg.</span></span> <span data-ttu-id="fc0fe-431">Драйвер WSL записывает ограниченные сведения в dmesg.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-431">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="fc0fe-432">В будущем эти возможности можно будет расширить, чтобы записывать другие сведения и данные диагностики из драйвера.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-432">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="fc0fe-433">Примечание. Сейчас dmesg поддерживается через интерфейс устройства `/dev/kmsg`.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-433">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="fc0fe-434">Интерфейс sycall `syslog` еще не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-434">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="fc0fe-435">Поэтому некоторые параметры командной строки `dmesg`, такие как `-S` и `-C`, не работают.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-435">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="fc0fe-436">Устранена проблема, из-за которой многопоточные операции могли возвращать ENOENT, даже если файл существовал.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-436">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="fc0fe-437">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-437">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="fc0fe-438">Сборка 17639 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="fc0fe-438">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="fc0fe-439">Общие сведения о сборке Windows 17639 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-439">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-440">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-440">WSL</span></span>
* <span data-ttu-id="fc0fe-441">Изменены GID и режим по умолчанию для последовательных устройств, чтобы обеспечить соответствие собственному режиму [GH 3042].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-441">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="fc0fe-442">Теперь DrvFs поддерживает расширенные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-442">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="fc0fe-443">Примечание. В DrvFs были некоторые ограничения для имен расширенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-443">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="fc0fe-444">В частности, некоторые знаки (например, "/", ":" и "\*") не допускаются, а в именах расширенных атрибутов в DrvFs не учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-444">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="fc0fe-445">Сборка 17133 (Fast)</span><span class="sxs-lookup"><span data-stu-id="fc0fe-445">Build 17133 (Fast)</span></span>
<span data-ttu-id="fc0fe-446">Общие сведения о сборке Windows 17133 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-446">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-447">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-447">WSL</span></span>
* <span data-ttu-id="fc0fe-448">Устранено прекращение ответа на запросы в WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-448">Fix for hang in WSL.</span></span> <span data-ttu-id="fc0fe-449">[GH 3039, 3034]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-449">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="fc0fe-450">Сборка 17128 (Fast)</span><span class="sxs-lookup"><span data-stu-id="fc0fe-450">Build 17128 (Fast)</span></span>
<span data-ttu-id="fc0fe-451">Общие сведения о сборке Windows 17128 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-451">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-452">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-452">WSL</span></span>
* <span data-ttu-id="fc0fe-453">Нет</span><span class="sxs-lookup"><span data-stu-id="fc0fe-453">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="fc0fe-454">Сборка 17627 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="fc0fe-454">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="fc0fe-455">Общие сведения о сборке Windows 17627 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-455">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-456">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-456">WSL</span></span>
* <span data-ttu-id="fc0fe-457">Добавлена поддержка фьютексных операций с поддержкой числа пи.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-457">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="fc0fe-458">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-458">[GH 1006]</span></span>
    * <span data-ttu-id="fc0fe-459">Обратите внимание на то, что приоритеты в настоящее время не поддерживаются компонентом WSL, так что существуют ограничения, но стандартное использование должно быть доступно.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-459">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="fc0fe-460">Поддержка брандмауэра Windows для процессов WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-460">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="fc0fe-461">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-461">[GH 1852]</span></span>
    * <span data-ttu-id="fc0fe-462">Например, чтобы разрешить процессу Python в WSL ожидать передачи данных через какой-либо порт, используйте командную строку Windows с повышенными привилегиями: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="fc0fe-462">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="fc0fe-463">Дополнительные сведения о добавлении правил брандмауэра доступны по [этой ссылке](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-463">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="fc0fe-464">При использовании wsl.exe учитывается оболочка по умолчанию пользователя.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-464">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="fc0fe-465">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-465">[GH 2372]</span></span>
* <span data-ttu-id="fc0fe-466">Все сетевые интерфейсы отображаются как Ethernet.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-466">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="fc0fe-467">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-467">[GH 2996]</span></span>
* <span data-ttu-id="fc0fe-468">Улучшена обработка поврежденного файла /etc/passwd.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-468">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="fc0fe-469">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-469">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="fc0fe-470">Консоль</span><span class="sxs-lookup"><span data-stu-id="fc0fe-470">Console</span></span>
* <span data-ttu-id="fc0fe-471">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-471">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-472">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-472">LTP Results:</span></span>
<span data-ttu-id="fc0fe-473">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-473">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="fc0fe-474">Сборка 17618 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="fc0fe-474">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="fc0fe-475">Общие сведения о сборке Windows 17618 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-475">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-476">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-476">WSL</span></span>
* <span data-ttu-id="fc0fe-477">Введена функция псевдоконсоли для взаимодействия с NT [GH 988, 1366, 1433, 1542, 2370, 2406].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-477">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="fc0fe-478">Устаревший механизм установки (lxrun.exe) является нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-478">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="fc0fe-479">Для установки дистрибутивов используется Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-479">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="fc0fe-480">Консоль</span><span class="sxs-lookup"><span data-stu-id="fc0fe-480">Console</span></span>
* <span data-ttu-id="fc0fe-481">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-481">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-482">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-482">LTP Results:</span></span>
<span data-ttu-id="fc0fe-483">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-483">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="fc0fe-484">Сборка 17110</span><span class="sxs-lookup"><span data-stu-id="fc0fe-484">Build 17110</span></span>
<span data-ttu-id="fc0fe-485">Общие сведения о сборке Windows 17110 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-485">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-486">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-486">WSL</span></span>
* <span data-ttu-id="fc0fe-487">Разрешено завершение /init из Windows [GH 2928].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-487">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="fc0fe-488">Теперь DrvFs по умолчанию учитывает регистр в имени отдельно для каждого каталога (аналогично параметру подключения "case=dir").</span><span class="sxs-lookup"><span data-stu-id="fc0fe-488">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="fc0fe-489">Для использования параметра "case=force" (прежнее поведение) требуется задать раздел реестра.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-489">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="fc0fe-490">Выполните следующую команду, чтобы включить режим "case=force", если необходимо его использовать: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span><span class="sxs-lookup"><span data-stu-id="fc0fe-490">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="fc0fe-491">Если у вас есть каталоги, созданные с помощью WSL в более ранней версии Windows, в которых должен учитываться регистр, используйте fsutil.exe, чтобы пометить их как каталоги с учетом регистра: fsutil.exe file setcasesensitiveinfo <path> enable</span><span class="sxs-lookup"><span data-stu-id="fc0fe-491">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="fc0fe-492">Строки, возвращаемые из uname syscall, завершаются значением NULL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-492">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="fc0fe-493">Консоль</span><span class="sxs-lookup"><span data-stu-id="fc0fe-493">Console</span></span>
* <span data-ttu-id="fc0fe-494">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-494">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-495">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-495">LTP Results:</span></span>
<span data-ttu-id="fc0fe-496">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-496">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="fc0fe-497">Сборка 17107</span><span class="sxs-lookup"><span data-stu-id="fc0fe-497">Build 17107</span></span>
<span data-ttu-id="fc0fe-498">Общие сведения о сборке Windows 17107 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-498">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-499">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-499">WSL</span></span>
* <span data-ttu-id="fc0fe-500">Поддержка TCSETSF и TCSETSW на главных конечных точках PTY [GH 2552].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-500">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="fc0fe-501">Запуск одновременных процессов взаимодействия мог привести к возвращению EINVAL [GH 2813].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-501">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="fc0fe-502">Устранена проблема с PTRACE_ATTACH для отображения правильного состояния трассировки в /proc/pid/status.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-502">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="fc0fe-503">Устранено состязание, когда кратковременные процессы, клонированные с флагами CLEARTID и SETTID, могли завершиться без очистки адреса TID.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-503">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="fc0fe-504">Отображается сообщение, если при переходе со сборки, предшествующей сборке 17093, выполняется обновление каталогов файловой системы Linux.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-504">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="fc0fe-505">Дополнительные сведения об изменениях в файловой системе в сборке 17093 доступны в заметках о выпуске [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-505">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="fc0fe-506">Консоль</span><span class="sxs-lookup"><span data-stu-id="fc0fe-506">Console</span></span>
* <span data-ttu-id="fc0fe-507">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-507">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-508">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-508">LTP Results:</span></span>
<span data-ttu-id="fc0fe-509">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-509">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="fc0fe-510">Сборка 17101</span><span class="sxs-lookup"><span data-stu-id="fc0fe-510">Build 17101</span></span>
<span data-ttu-id="fc0fe-511">Общие сведения о сборке Windows 17101 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-511">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-512">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-512">WSL</span></span>
* <span data-ttu-id="fc0fe-513">Поддержка signalfd.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-513">Support for signalfd.</span></span> <span data-ttu-id="fc0fe-514">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-514">[GH 129]</span></span>
* <span data-ttu-id="fc0fe-515">Поддержка имен файлов, содержащих недопустимые знаки NTFS, благодаря их кодированию в виде частных знаков Юникода.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-515">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="fc0fe-516">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-516">[GH 1514]</span></span>
* <span data-ttu-id="fc0fe-517">Функция автоматического подключения будет переключаться в режим только для чтения, если запись не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-517">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="fc0fe-518">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-518">[GH 2603]</span></span>
* <span data-ttu-id="fc0fe-519">Допускается вставка суррогатных пар Юникода (например, знаков эмодзи).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-519">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="fc0fe-520">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-520">[GH 2765]</span></span>
* <span data-ttu-id="fc0fe-521">Псевдофайлы в /proc и /sys должны возвращаться готовыми для чтения и записи после выполнения команд select, poll, epoll и т. д. [GH 2838].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-521">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="fc0fe-522">Устранена проблема, из-за которой служба могла уйти в бесконечный цикл, если реестр был незаконно изменен или поврежден.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-522">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="fc0fe-523">Сообщения NETLINK исправлены для работы с более новой версией iproute2 (начиная с версии 4.14).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-523">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="fc0fe-524">Консоль</span><span class="sxs-lookup"><span data-stu-id="fc0fe-524">Console</span></span>
* <span data-ttu-id="fc0fe-525">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-525">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-526">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-526">LTP Results:</span></span>
<span data-ttu-id="fc0fe-527">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-527">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="fc0fe-528">Сборка 17093</span><span class="sxs-lookup"><span data-stu-id="fc0fe-528">Build 17093</span></span>
<span data-ttu-id="fc0fe-529">Общие сведения о сборке Windows 17093 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-529">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="fc0fe-530">Внимание!</span><span class="sxs-lookup"><span data-stu-id="fc0fe-530">Important:</span></span>
<span data-ttu-id="fc0fe-531">При запуске WSL в первый раз после обновления до этой сборки необходимо выполнить некоторые действия, чтобы обновить каталоги файловой системы Linux.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-531">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="fc0fe-532">Это может занять несколько минут, поэтому может показаться, что WSL медленно запускается.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-532">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="fc0fe-533">Это должно произойти только один раз для каждого дистрибутива, установленного из Store.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-533">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="fc0fe-534">Улучшена поддержка учета регистра в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-534">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="fc0fe-535">Теперь DrvFs поддерживает учет регистра отдельно для каждого каталога.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-535">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="fc0fe-536">Это новый флаг, который можно задать для каталогов, чтобы указать, что все операции в этих каталогах должны выполняться с учетом регистра, что позволит даже приложениям для Windows правильно открывать файлы, отличающиеся только регистром в именах.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-536">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="fc0fe-537">В DrvFs есть новые параметры подключения, управляющие учетом регистра для каждого каталога:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-537">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="fc0fe-538">case=force: для всех каталогов учитывается регистр (за исключением корневого диска).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-538">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="fc0fe-539">Новые каталоги, созданные с помощью WSL, помечаются как каталоги с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-539">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="fc0fe-540">Это устаревшее поведение, за исключением пометки новых каталогов как каталогов с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-540">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="fc0fe-541">case=dir: регистр учитывается только для каталогов с флагом учета регистра; для других каталогов регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-541">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="fc0fe-542">Новые каталоги, созданные с помощью WSL, помечаются как каталоги с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-542">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="fc0fe-543">case=off: регистр учитывается только для каталогов с флагом учета регистра; для других каталогов регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-543">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="fc0fe-544">Новые каталоги, созданные с помощью WSL, помечаются как каталоги без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-544">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="fc0fe-545">Примечание. Каталоги, созданные WSL в предыдущих выпусках, не имеют этого флага, поэтому для них регистр не будет учитываться, если задан параметр "case=dir".</span><span class="sxs-lookup"><span data-stu-id="fc0fe-545">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="fc0fe-546">Способ задания этого флага для существующих каталогов будет реализован в ближайшее время.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-546">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="fc0fe-547">Пример подключения с этими параметрами (существующие диски необходимо сначала отключить, чтобы подключить их с другими параметрами): sudo mount -t drvfs C: /mnt/c -o case=dir</span><span class="sxs-lookup"><span data-stu-id="fc0fe-547">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="fc0fe-548">Пока что параметр "case=force" все еще используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-548">For now, case=force is still the default option.</span></span> <span data-ttu-id="fc0fe-549">В будущем по умолчанию будет использоваться параметр case=dir.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-549">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="fc0fe-550">Теперь вы можете использовать косую черту в путях Windows при подключении DrvFs, например: sudo mount -t drvfs //server/share /mnt/share</span><span class="sxs-lookup"><span data-stu-id="fc0fe-550">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="fc0fe-551">WSL теперь обрабатывает файл /etc/fstab во время запуска экземпляра [GH 2636].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-551">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="fc0fe-552">Это делается до автоматического подключения дисков DrvFs. Все диски, которые уже были подключены fstab, не будут автоматически подключаться. Это позволит вам изменить точку подключения для конкретных дисков.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-552">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="fc0fe-553">Это поведение можно отключить с помощью wsl.conf.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-553">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="fc0fe-554">Файлы mount, mountinfo и mountstats в /proc правильно экранируют специальные знаки, такие как символы обратной косой черты и пробелы [GH 2799].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-554">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="fc0fe-555">Теперь можно копировать и перемещать из Windows специальные файлы, созданные с помощью DrvFs, такие как символьные ссылки WSL, или файлы FIFO и сокеты, если метаданные включены.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-555">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="fc0fe-556">Можно настроить больше параметров WSL с помощью wsl.conf.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-556">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="fc0fe-557">Мы добавили метод для автоматической настройки определенных функций в WSL, которые будут применяться при каждом запуске подсистемы.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-557">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="fc0fe-558">Сюда входят параметры автоподключения и конфигурация сети.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-558">This includes automount options and network configuration.</span></span> <span data-ttu-id="fc0fe-559">Дополнительные сведения об этом можно получить из нашей записи блога: https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="fc0fe-559">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="af_unix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="fc0fe-560">AF_UNIX позволяет устанавливать подключения через сокет между процессами Linux в собственных процессах WSL и Windows.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-560">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="fc0fe-561">Теперь приложения WSL и приложения для Windows могут взаимодействовать друг с другом через сокеты UNIX.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-561">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="fc0fe-562">Представьте, что вы хотите запустить службу в Windows и сделать ее доступной для приложений для Windows и приложений WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-562">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="fc0fe-563">Теперь это возможно благодаря сокетам UNIX.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-563">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="fc0fe-564">Узнайте больше в записи блога https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="fc0fe-564">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-565">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-565">WSL</span></span>
* <span data-ttu-id="fc0fe-566">Поддержка mmap() с MAP_NORESERVE [GH 121, 2784].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-566">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="fc0fe-567">Поддержка CLONE_PTRACE и CLONE_UNTRACED [GH 121, 2781].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-567">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="fc0fe-568">Обработка сигнала завершения без SIGCHLD в клоне [GH 121, 2781].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-568">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="fc0fe-569">Добавлены заглушки /proc/sys/fs/inotify/max_user_instances и /proc/sys/fs/inotify/max_user_watches [GH 1705].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-569">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="fc0fe-570">Устранена ошибка при загрузке двоичных файлов ELF, содержащих заголовки загрузки с ненулевыми смещениями [GH 1884].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-570">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="fc0fe-571">Заполнение нулями конечных байтов страниц при загрузке образов.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-571">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="fc0fe-572">Сокращены случаи, когда execve автоматически завершает процесс.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-572">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="fc0fe-573">Консоль</span><span class="sxs-lookup"><span data-stu-id="fc0fe-573">Console</span></span>
* <span data-ttu-id="fc0fe-574">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-574">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-575">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-575">LTP Results:</span></span>
<span data-ttu-id="fc0fe-576">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-576">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="fc0fe-577">Сборка 17083</span><span class="sxs-lookup"><span data-stu-id="fc0fe-577">Build 17083</span></span>
<span data-ttu-id="fc0fe-578">Общие сведения о сборке Windows 17083 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-578">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-579">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-579">WSL</span></span>
* <span data-ttu-id="fc0fe-580">Исправлена критическая ошибка, связанная с epoll [GH 2798, 2801, 2857].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-580">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="fc0fe-581">Исправлено прекращение реагирования на запросы при отключении ASLR [GH 1185, 2870].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-581">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="fc0fe-582">Обеспечена атомарность операций mmap [GH 2732].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-582">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="fc0fe-583">Консоль</span><span class="sxs-lookup"><span data-stu-id="fc0fe-583">Console</span></span>
* <span data-ttu-id="fc0fe-584">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-584">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-585">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-585">LTP Results:</span></span>
<span data-ttu-id="fc0fe-586">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-586">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="fc0fe-587">Сборка 17074</span><span class="sxs-lookup"><span data-stu-id="fc0fe-587">Build 17074</span></span>
<span data-ttu-id="fc0fe-588">Общие сведения о сборке Windows 17074 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-588">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-589">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-589">WSL</span></span>
* <span data-ttu-id="fc0fe-590">Исправлен формат хранения метаданных DrvFs [GH 2777].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-590">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="fc0fe-591">**Важно!** Метаданные DrvFs, созданные до выпуска этой сборки, будут отображаться неправильно или вообще не будут отображаться.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-591">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="fc0fe-592">Чтобы исправить затронутые файлы, используйте chmod и chown для повторного применения метаданных.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-592">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="fc0fe-593">Устранена проблема с несколькими сигналами и перезапускаемыми вызовами syscall.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-593">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="fc0fe-594">Консоль</span><span class="sxs-lookup"><span data-stu-id="fc0fe-594">Console</span></span>
* <span data-ttu-id="fc0fe-595">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-595">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-596">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-596">LTP Results:</span></span>
<span data-ttu-id="fc0fe-597">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-597">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="fc0fe-598">Сборка 17063</span><span class="sxs-lookup"><span data-stu-id="fc0fe-598">Build 17063</span></span>
<span data-ttu-id="fc0fe-599">Общие сведения о сборке Windows 17063 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-599">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc0fe-600">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-600">WSL</span></span>
* <span data-ttu-id="fc0fe-601">DrvFs поддерживает дополнительные метаданные Linux.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-601">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="fc0fe-602">Это позволяет задать владельца и режим файлов с помощью chmod или chown, а также создать специальные файлы, такие как FIFO, сокеты UNIX и файлы устройств.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-602">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="fc0fe-603">Сейчас эта функция отключена по умолчанию, так как еще является экспериментальной.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-603">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="fc0fe-604">**Примечание.**  Исправлена ошибка в формате метаданных, используемом DrvFs.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-604">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="fc0fe-605">Хотя метаданные используются в этой сборке в качестве эксперимента, будущие сборки не будут правильно считывать метаданные, созданные этой сборкой.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-605">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="fc0fe-606">Возможно, потребуется вручную обновить владельца измененных файлов, а устройства с пользовательским идентификатором устройства потребуется создать заново.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-606">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="fc0fe-607">Чтобы включить эту функцию, подключите DrvFs с параметром metadata (чтобы включить эту функцию для существующего подключения, его необходимо сначала отключить):</span><span class="sxs-lookup"><span data-stu-id="fc0fe-607">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="fc0fe-608">Разрешения Linux добавляются в файл в качестве дополнительных метаданных; они не влияют на разрешения Windows.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-608">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="fc0fe-609">Помните, что изменение файла с помощью редактора Windows может привести к удалению метаданных.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-609">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="fc0fe-610">В этом случае будут восстановлены разрешения этого файла по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-610">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="fc0fe-611">Добавлены параметры подключения к DrvFs для управления файлами без метаданных.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-611">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="fc0fe-612">uid: идентификатор пользователя, используемый для владельца всех файлов.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-612">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="fc0fe-613">gid: идентификатор группы, используемый для владельца всех файлов.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-613">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="fc0fe-614">umask: восьмеричная маска разрешений, исключаемых для всех файлов и каталогов.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-614">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="fc0fe-615">fmask: восьмеричная маска разрешений, исключаемых для всех обычных файлов.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-615">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="fc0fe-616">dmask: восьмеричная маска разрешений, исключаемых для всех каталогов.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-616">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="fc0fe-617">Например:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-617">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="fc0fe-618">Используйте вместе с параметром metadata, чтобы указать разрешения по умолчанию для файлов без метаданных.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-618">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="fc0fe-619">Появилась новая переменная среды, `WSLENV`, позволяющая настроить поток переменных среды между WSL и Win32.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-619">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="fc0fe-620">Например:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-620">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="fc0fe-621">`WSLENV` — разделенный двоеточиями список переменных среды, которые могут быть добавлены при запуске процессов WSL из Win32 или при запуске процессов Win32 из WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-621">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="fc0fe-622">Каждая переменная может иметь суффикс с косой чертой, за которой следуют флаги для указания способа преобразования.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-622">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="fc0fe-623">p: значение — это путь, который должен быть преобразован между WSL и Win32.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-623">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="fc0fe-624">l: значение — это список путей.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-624">l: The value is a list of paths.</span></span> <span data-ttu-id="fc0fe-625">В WSL это список, разделенный двоеточиями.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-625">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="fc0fe-626">В Win32 это список, разделенный точками с запятой.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-626">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="fc0fe-627">u: это значение должно добавляться только при вызове WSL из Win32.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-627">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="fc0fe-628">w: это значение должно добавляться только при вызове Win32 из WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-628">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="fc0fe-629">Вы можете задать `WSLENV` в bashrc или в пользовательской среде Windows для пользователя.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-629">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="fc0fe-630">Подключения DrvFs правильно сохраняют метки времени из tar, cp -p (GH 1939).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-630">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="fc0fe-631">Символические ссылки DrvFs сообщают правильный размер (GH 2641).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-631">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="fc0fe-632">Операции чтения и записи могут обрабатывать очень большие объемы ввода-вывода (GH 2653).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-632">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="fc0fe-633">Функция waitpid работает с идентификаторами групп процессов (GH 2534).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-633">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="fc0fe-634">Значительно улучшена производительность mmap для больших резервных регионов. Повышена производительность ghc (GH 1671).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-634">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="fc0fe-635">Personality поддерживает READ_IMPLIES_EXEC; реализованы исправления для maxima и clisp (GH 1185).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-635">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="fc0fe-636">Mprotect поддерживает PROT_GROWSDOWN; реализованы исправления для clisp (GH 1128).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-636">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="fc0fe-637">Устранены сбои страниц в режиме перегрузки; реализованы исправления для sbcl (GH 1128).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-637">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="fc0fe-638">Функция clone поддерживает больше сочетаний флагов.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-638">clone supports more flags combinations</span></span>
* <span data-ttu-id="fc0fe-639">Поддержка select/epoll для файлов epoll (ранее это считалось холостой командой).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-639">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="fc0fe-640">Уведомление ptrace о нереализованных вызовах syscall.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-640">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="fc0fe-641">Игнорирование интерфейсов, которые не выполняются, при создании серверов имен resolv.conf [GH 2694].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-641">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="fc0fe-642">Перечисление сетевых интерфейсов без физического адреса.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-642">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="fc0fe-643">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-643">[GH 2685]</span></span>
* <span data-ttu-id="fc0fe-644">Дополнительные исправления ошибок и улучшения.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-644">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="fc0fe-645">Инструменты Linux, доступные для разработчиков в Windows</span><span class="sxs-lookup"><span data-stu-id="fc0fe-645">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="fc0fe-646">Цепочка инструментов командной строки Windows включает в себя bsdtar (tar) и curl.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-646">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="fc0fe-647">Ознакомьтесь с [этим блогом](https://aka.ms/tarcurlwindows), чтобы узнать больше о добавлении этих двух новых инструментов и о том, как они изменяют разработку в Windows.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-647">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="fc0fe-648">`AF_UNIX` доступен в пакете SDK для программы предварительной оценки Windows (начиная со сборки 17061).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-648">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="fc0fe-649">Ознакомьтесь с [этим блогом](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/), чтобы узнать больше о `AF_UNIX` и способах его использования разработчиками в Windows.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-649">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="fc0fe-650">Консоль</span><span class="sxs-lookup"><span data-stu-id="fc0fe-650">Console</span></span>
* <span data-ttu-id="fc0fe-651">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-651">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-652">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-652">LTP Results:</span></span>
<span data-ttu-id="fc0fe-653">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-653">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="fc0fe-654">Сборка 17046</span><span class="sxs-lookup"><span data-stu-id="fc0fe-654">Build 17046</span></span>

<span data-ttu-id="fc0fe-655">Общие сведения о сборке Windows 17046 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-655">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="fc0fe-656">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-656">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="fc0fe-657">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-657">WSL</span></span>
- <span data-ttu-id="fc0fe-658">Разрешено выполнение процессов без активного терминала.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-658">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="fc0fe-659">[GH 709, 1007, 1511, 2252, 2391 и т. д.]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-659">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="fc0fe-660">Улучшена поддержка CLONE_VFORK и CLONE_VM.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-660">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="fc0fe-661">[GH 1878, 2615]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-661">[GH 1878, 2615]</span></span>
- <span data-ttu-id="fc0fe-662">Пропуск драйверов фильтра TDI для сетевых операций WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-662">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="fc0fe-663">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-663">[GH 1554]</span></span>
- <span data-ttu-id="fc0fe-664">DrvFs создает символические ссылки NT при выполнении определенных условий.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-664">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="fc0fe-665">[GH 353, 1475, 2602]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-665">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="fc0fe-666">Цель ссылки должна быть относительной, не должна пересекать точки подключения или символические ссылки и должна существовать.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-666">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="fc0fe-667">Пользователь должен иметь разрешение SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (обычно для этого требуется запустить wsl.exe с повышенными привилегиями), если режим разработчика не включен.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-667">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="fc0fe-668">Во всех остальных случаях DrvFs по-прежнему создает символические ссылки WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-668">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="fc0fe-669">Разрешено одновременное выполнение экземпляров WSL с повышенными привилегиями и без повышенных привилегий.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-669">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="fc0fe-670">Поддержка /proc/sys/kernel/yama/ptrace_scope.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-670">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="fc0fe-671">Добавлена функция wslpath для преобразования путей WSL в пути Windows и наоборот.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-671">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="fc0fe-672">[GH 522, 1243, 1834, 2327 и т. д.]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-672">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="fc0fe-673">Консоль</span><span class="sxs-lookup"><span data-stu-id="fc0fe-673">Console</span></span>
- <span data-ttu-id="fc0fe-674">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-674">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-675">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-675">LTP Results:</span></span>
<span data-ttu-id="fc0fe-676">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-676">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="fc0fe-677">Сборка 17040</span><span class="sxs-lookup"><span data-stu-id="fc0fe-677">Build 17040</span></span>

<span data-ttu-id="fc0fe-678">Общие сведения о сборке Windows 17040 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-678">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-679">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-679">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="fc0fe-680">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-680">WSL</span></span>
- <span data-ttu-id="fc0fe-681">Исправления с момента выпуска сборки 17035 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-681">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="fc0fe-682">Консоль</span><span class="sxs-lookup"><span data-stu-id="fc0fe-682">Console</span></span>
- <span data-ttu-id="fc0fe-683">Исправления с момента выпуска сборки 17035 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-683">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-684">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-684">LTP Results:</span></span>
<span data-ttu-id="fc0fe-685">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-685">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="fc0fe-686">Сборка 17035</span><span class="sxs-lookup"><span data-stu-id="fc0fe-686">Build 17035</span></span>

<span data-ttu-id="fc0fe-687">Общие сведения о сборке Windows 17035 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-687">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-688">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-688">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="fc0fe-689">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-689">WSL</span></span>
- <span data-ttu-id="fc0fe-690">Иногда не удавалось получить доступ к файлам в DrvFs с ошибкой EINVAL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-690">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="fc0fe-691">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-691">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="fc0fe-692">Консоль</span><span class="sxs-lookup"><span data-stu-id="fc0fe-692">Console</span></span>
- <span data-ttu-id="fc0fe-693">Устранена небольшая потеря цветов при вставке или удалении строк в режиме VT.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-693">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-694">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-694">LTP Results:</span></span>
<span data-ttu-id="fc0fe-695">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-695">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="fc0fe-696">Сборка 17025</span><span class="sxs-lookup"><span data-stu-id="fc0fe-696">Build 17025</span></span>

<span data-ttu-id="fc0fe-697">Общие сведения о сборке Windows 17025 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-697">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-698">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-698">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="fc0fe-699">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-699">WSL</span></span>
- <span data-ttu-id="fc0fe-700">Запуск начальных процессов в новой группе процессов переднего плана [GH 1653, 2510].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-700">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="fc0fe-701">Исправления доставки SIGHUP [GH 2496].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-701">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="fc0fe-702">Создание имени виртуального моста по умолчанию, если оно не указано [GH 2497].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-702">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="fc0fe-703">Реализовано /proc/sys/kernel/Random/boot_id [GH 2518].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-703">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="fc0fe-704">Дополнительные исправления взаимодействия с каналом stdout/stderr.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-704">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="fc0fe-705">Заглушка системного вызова syncfs.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-705">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="fc0fe-706">Консоль</span><span class="sxs-lookup"><span data-stu-id="fc0fe-706">Console</span></span>
- <span data-ttu-id="fc0fe-707">Исправление входного преобразования VT для консолей сторонних разработчиков [GH 111].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-707">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-708">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-708">LTP Results:</span></span>
<span data-ttu-id="fc0fe-709">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-709">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="fc0fe-710">Сборка 17017</span><span class="sxs-lookup"><span data-stu-id="fc0fe-710">Build 17017</span></span>

<span data-ttu-id="fc0fe-711">Общие сведения о сборке Windows 17017 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-711">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-712">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-712">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="fc0fe-713">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-713">WSL</span></span>
- <span data-ttu-id="fc0fe-714">Пропуск пустых заголовков программы ELF [GH 330].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-714">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="fc0fe-715">LxssManager разрешено создавать экземпляры WSL для неинтерактивных пользователей (поддержка SSH и запланированных задач) [GH 777, 1602].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-715">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="fc0fe-716">Поддержка сценариев WSL > Win32 > WSL ("порождение") [GH 1228].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-716">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="fc0fe-717">Ограниченная поддержка завершения работы консольных приложений, вызванных посредством взаимодействия [GH 1614].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-717">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="fc0fe-718">Поддержка параметров подключения для devpts [GH 1948].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-718">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="fc0fe-719">Устранена блокировка Ptrace запуска дочерних процессов [GH 2333].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-719">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="fc0fe-720">В EPOLLET отсутствовали некоторые события [GH 2462].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-720">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="fc0fe-721">PTRACE_GETSIGINFO возвращает больше данных.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-721">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="fc0fe-722">Функция getdents с lseek выдавала неправильные результаты.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-722">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="fc0fe-723">Устранены некоторые сценарии, в которых взаимодействующее приложение Win32 переставало отвечать на запросы, ожидая входных данных в канале, который больше не содержал данные.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-723">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="fc0fe-724">Поддержка O_ASYNC для файлов tty и pty.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-724">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="fc0fe-725">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-725">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="fc0fe-726">Консоль</span><span class="sxs-lookup"><span data-stu-id="fc0fe-726">Console</span></span>
- <span data-ttu-id="fc0fe-727">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-727">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-728">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-728">LTP Results:</span></span>
<span data-ttu-id="fc0fe-729">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-729">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="fc0fe-730">Обновление Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="fc0fe-730">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="fc0fe-731">Сборка 16288</span><span class="sxs-lookup"><span data-stu-id="fc0fe-731">Build 16288</span></span>

<span data-ttu-id="fc0fe-732">Общие сведения о сборке Windows 16288 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-732">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-733">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-733">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="fc0fe-734">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-734">WSL</span></span>
- <span data-ttu-id="fc0fe-735">Правильная инициализация и отображение UID, GID и режима для дескрипторов файлов сокетов [GH 2490].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-735">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="fc0fe-736">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-736">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="fc0fe-737">Консоль</span><span class="sxs-lookup"><span data-stu-id="fc0fe-737">Console</span></span>
- <span data-ttu-id="fc0fe-738">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-738">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-739">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-739">LTP Results:</span></span>
<span data-ttu-id="fc0fe-740">Изменения с момента выпуска сборки 16273 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-740">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="fc0fe-741">Сборка 16278</span><span class="sxs-lookup"><span data-stu-id="fc0fe-741">Build 16278</span></span>

<span data-ttu-id="fc0fe-742">Общие сведения о сборке Windows 162738 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-742">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-743">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-743">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="fc0fe-744">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-744">WSL</span></span>
- <span data-ttu-id="fc0fe-745">Явная отмена сопоставления сопоставленных представлений разделов с файлами при завершении состояния LX MM [GH 2415].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-745">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="fc0fe-746">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-746">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="fc0fe-747">Консоль</span><span class="sxs-lookup"><span data-stu-id="fc0fe-747">Console</span></span>
- <span data-ttu-id="fc0fe-748">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-748">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-749">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-749">LTP Results:</span></span>
<span data-ttu-id="fc0fe-750">Изменения с момента выпуска сборки 16273 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-750">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="fc0fe-751">Сборка 16275</span><span class="sxs-lookup"><span data-stu-id="fc0fe-751">Build 16275</span></span>

<span data-ttu-id="fc0fe-752">Общие сведения о сборке Windows 162735 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-752">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-753">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-753">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="fc0fe-754">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-754">WSL</span></span>
- <span data-ttu-id="fc0fe-755">В этом выпуске нет изменений, связанных с WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-755">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="fc0fe-756">Консоль</span><span class="sxs-lookup"><span data-stu-id="fc0fe-756">Console</span></span>
- <span data-ttu-id="fc0fe-757">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-757">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-758">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-758">LTP Results:</span></span>
<span data-ttu-id="fc0fe-759">Изменения с момента выпуска сборки 16273 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-759">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="fc0fe-760">Сборка 16273</span><span class="sxs-lookup"><span data-stu-id="fc0fe-760">Build 16273</span></span>

<span data-ttu-id="fc0fe-761">Общие сведения о сборке Windows 16273 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-761">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-762">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-762">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="fc0fe-763">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-763">WSL</span></span>
- <span data-ttu-id="fc0fe-764">Исправлена проблема, из-за которой DrvFs иногда сообщал о неправильном типе файла для каталогов [GH 2392].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-764">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="fc0fe-765">Разрешено создание сокетов NETLINK_KOBJECT_UEVENT для разблокирования программ, использующих uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-765">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="fc0fe-766">Добавлена поддержка неблокирующего подключения [GH 903, 1391, 1584, 1585, 1829, 2290, 2314].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-766">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="fc0fe-767">Реализован флаг системного вызова клонирования CLONE_FS [GH 2242].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-767">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="fc0fe-768">Устранены проблемы, связанные с неправильной обработкой знаков табуляции или кавычек при взаимодействии с NT [GH 1625, 2164].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-768">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="fc0fe-769">Устранена ошибка отказа в доступе при попытке повторного запуска экземпляров WSL [GH 651, 2095].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-769">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="fc0fe-770">Реализованы фьютексные операции FUTEX_REQUEUE и FUTEX_CMP_REQUEUE [GH 2242].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-770">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="fc0fe-771">Исправлены разрешения для различных файлов SysFs [GH 2214].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-771">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="fc0fe-772">Устранена проблема, из-за которой стек Haskell переставал отвечать на запросы во время установки [GH 2290].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-772">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="fc0fe-773">Реализованы флаги binfmt_misc "C", "O" и "P" [GH 2103].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-773">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="fc0fe-774">Добавлены /proc/sys/kernel, /shmmax, /shmmni и /threads-max [GH 1753].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-774">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="fc0fe-775">Добавлена частичная поддержка системного вызова ioprio_set [GH 498].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-775">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="fc0fe-776">Реализована заглушка SO_REUSEPORT и добавлена поддержка SO_PASSCRED для сокетов NETLINK [GH 69].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-776">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="fc0fe-777">Возвращение разных кодов ошибок из RegisterDistribuiton, если дистрибутив в данный момент устанавливается или удаляется.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-777">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="fc0fe-778">Обеспечена отмена регистрации частично установленных дистрибутивов WSL с помощью wslconfig.exe.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-778">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="fc0fe-779">Устранена ошибка, из-за которой сокет Python переставал отвечать на запросы при выполнении udp::msg_peek.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-779">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="fc0fe-780">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-780">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="fc0fe-781">Консоль</span><span class="sxs-lookup"><span data-stu-id="fc0fe-781">Console</span></span>
- <span data-ttu-id="fc0fe-782">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-782">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-783">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-783">LTP Results:</span></span>
<span data-ttu-id="fc0fe-784">Всего тестов: 1904.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-784">Total Tests: 1904</span></span><br/>
<span data-ttu-id="fc0fe-785">Всего пропущенных тестов: 209.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-785">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="fc0fe-786">Всего сбоев: 229.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-786">Total Failures: 229</span></span><br/>
[<span data-ttu-id="fc0fe-787">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="fc0fe-787">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="fc0fe-788">Сборка 16257</span><span class="sxs-lookup"><span data-stu-id="fc0fe-788">Build 16257</span></span>

<span data-ttu-id="fc0fe-789">Общие сведения о сборке Windows 16257 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-789">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-790">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-790">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="fc0fe-791">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-791">WSL</span></span>
- <span data-ttu-id="fc0fe-792">Реализован системный вызов prlimit64.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-792">Implement prlimit64 system call</span></span>
- <span data-ttu-id="fc0fe-793">Добавлена поддержка ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-793">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="fc0fe-794">Заглушка MSG_MORE для TCP-сокетов [GH 2351].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-794">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="fc0fe-795">Исправлено недопустимое поведение вспомогательного вектора AT_EXECFN [GH 2133].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-795">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="fc0fe-796">Исправлено поведение копирования и вставки для консоли и tty и добавлена улучшенная обработка полного буфера [GH 2204, 2131].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-796">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="fc0fe-797">Установка AT_SECURE в дополнительном векторе для программ set-user-ID и set-group-ID [GH 2031].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-797">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="fc0fe-798">Главная конечная точка псевдотерминала не обрабатывала TIOCPGRP [GH 1063].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-798">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="fc0fe-799">Исправлена проблема lseek с перемоткой каталогов в LxFs [GH 2310].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-799">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="fc0fe-800">Исправлена блокировка /dev/ptmx после интенсивного использования [GH 1882].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-800">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="fc0fe-801">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-801">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="fc0fe-802">Консоль</span><span class="sxs-lookup"><span data-stu-id="fc0fe-802">Console</span></span>
- <span data-ttu-id="fc0fe-803">Исправлено отображение горизонтальных линий и знаков подчеркивания везде [GH 2168].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-803">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="fc0fe-804">Исправлено изменение порядка процессов, усложнявшее закрытие NPM [GH 2170].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-804">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="fc0fe-805">Добавлена новая цветовая схема: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-805">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-806">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-806">LTP Results:</span></span>
<span data-ttu-id="fc0fe-807">Изменения с момента выпуска сборки 16251 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-807">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="fc0fe-808">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="fc0fe-808">Syscall Support</span></span>
<span data-ttu-id="fc0fe-809">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-809">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="fc0fe-810">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-810">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="fc0fe-811">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="fc0fe-811">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[<span data-ttu-id="fc0fe-812">Проблема GitHub 2392: WSL не распознает папки Windows…</span><span class="sxs-lookup"><span data-stu-id="fc0fe-812">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="fc0fe-813">В сборке 16257 в WSL возникли проблемы при перечислении файлов и папок Windows с помощью `/mnt/c/...`.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-813">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="fc0fe-814">Эта проблема устранена, и исправление будет выпущено в сборке для программы предварительной оценки в течение недели после 14 августа 2017 года.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-814">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="fc0fe-815">Сборка 16251</span><span class="sxs-lookup"><span data-stu-id="fc0fe-815">Build 16251</span></span>

<span data-ttu-id="fc0fe-816">Общие сведения о сборке Windows 16251 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-816">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-817">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-817">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="fc0fe-818">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-818">WSL</span></span>
- <span data-ttu-id="fc0fe-819">Удален тег бета-версии из дополнительного компонента WSL. Дополнительные сведения см. в этой [записи блога](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-819">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="fc0fe-820">Правильная инициализация сохраненных заданных UID и GID для двоичных файлов set-user-ID и set-group-ID при выполнении [GH 962, 1415, 2072].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-820">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="fc0fe-821">Добавлена поддержка PTRACE_O_TRACEEXIT в ptrace [GH 555].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-821">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="fc0fe-822">В ptrace добавлена поддержка PTRACE_GETFPREGS и PTRACE_GETREGSET с NT_FPREGSET [GH 555].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-822">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="fc0fe-823">Исправлена проблема, из-за которой выполнение ptrace останавливалось на пропущенных сигналах.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-823">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="fc0fe-824">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-824">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="fc0fe-825">Консоль</span><span class="sxs-lookup"><span data-stu-id="fc0fe-825">Console</span></span>
- <span data-ttu-id="fc0fe-826">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-826">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-827">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-827">LTP Results:</span></span>
<span data-ttu-id="fc0fe-828">Число пройденных тестов: 768</span><span class="sxs-lookup"><span data-stu-id="fc0fe-828">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="fc0fe-829">Число непройденных тестов: 244.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-829">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="fc0fe-830">Число пропущенных тестов: 96</span><span class="sxs-lookup"><span data-stu-id="fc0fe-830">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="fc0fe-831">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="fc0fe-831">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="fc0fe-832">Сборка 16241</span><span class="sxs-lookup"><span data-stu-id="fc0fe-832">Build 16241</span></span>

<span data-ttu-id="fc0fe-833">Общие сведения о сборке Windows 16241 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-833">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-834">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-834">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="fc0fe-835">WSL</span><span class="sxs-lookup"><span data-stu-id="fc0fe-835">WSL</span></span>
- <span data-ttu-id="fc0fe-836">В этом выпуске нет изменений, связанных с WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-836">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="fc0fe-837">Консоль</span><span class="sxs-lookup"><span data-stu-id="fc0fe-837">Console</span></span>
- <span data-ttu-id="fc0fe-838">Исправлено вывода неправильного знака для пересечения линий DEC, о котором первоначально было сообщено [здесь](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-838">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="fc0fe-839">Исправлено отсутствие вывода текста в кодовой странице 65001 (UTF8).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-839">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="fc0fe-840">Изменения, внесенные в значения RGB одного цвета, не переносятся в другие части палитры при изменении выбора.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-840">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="fc0fe-841">Это заметно облегчит использование страницы свойств консоли.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-841">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="fc0fe-842">Нажатие клавиш Ctrl+S не работало правильно.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-842">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="fc0fe-843">Un-Bold и -Dim полностью отсутствуют в escape-кодах ANSI [GH 2174].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-843">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="fc0fe-844">Консоль неправильно поддерживала цветовые темы Vim [GH 1706].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-844">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="fc0fe-845">Не удавалось вставить определенные знаки [GH 2149].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-845">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="fc0fe-846">Изменение размера расплавления приводило к необычному изменению размера окна Bash, когда что-то было введено в строке редактирования или командной строке [GH ConEmu 1123].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-846">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="fc0fe-847">Нажатие клавиш CTRL+L не очищало экран [GH 1978].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-847">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="fc0fe-848">Устранена ошибка отрисовки консоли при отображении VT в HDPI [GH 1907].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-848">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="fc0fe-849">Японские знаки выглядели необычно со знаком Юникода U+30FB [GH 2146].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-849">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="fc0fe-850">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-850">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="fc0fe-851">Сборка 16237</span><span class="sxs-lookup"><span data-stu-id="fc0fe-851">Build 16237</span></span>

<span data-ttu-id="fc0fe-852">Общие сведения о сборке Windows 16237 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-852">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-853">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-853">Fixed</span></span>
- <span data-ttu-id="fc0fe-854">Использование атрибутов по умолчанию для файлов без EA в lxfs (root, root, 0000).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-854">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="fc0fe-855">Добавлена поддержка дистрибутивов, использующих расширенные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-855">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="fc0fe-856">Исправлено заполнение записей, возвращаемых getdents и getdents64.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-856">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="fc0fe-857">Исправлена проверка разрешений для системного вызова shmctl SHM_STAT [GH 2068].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-857">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="fc0fe-858">Исправлено неправильное начальное состояние epoll для tty [GH 2231].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-858">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="fc0fe-859">Устранена проблема в DrvFs, из-за которой команда readdir не возвращала все записи [GH 2077].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-859">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="fc0fe-860">Исправлена операция LxFs readdir с несвязанными файлами [GH 2077].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-860">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="fc0fe-861">Допускается повторное открытие несвязанных файлов DrvFs с помощью procfs.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-861">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="fc0fe-862">Добавлено переопределение глобального раздела реестра для отключения функций WSL (взаимодействие и монтирование дисков).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-862">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="fc0fe-863">Исправлено неправильное число блокировок в "stat" для DrvFs (и LxFs) [GH 1894].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-863">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="fc0fe-864">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-864">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="fc0fe-865">Сборка 16232</span><span class="sxs-lookup"><span data-stu-id="fc0fe-865">Build 16232</span></span>

<span data-ttu-id="fc0fe-866">Общие сведения о сборке Windows 16232 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-866">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-867">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-867">Fixed</span></span>
- <span data-ttu-id="fc0fe-868">В этом выпуске нет изменений, связанных с WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-868">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="fc0fe-869">Сборка 16226</span><span class="sxs-lookup"><span data-stu-id="fc0fe-869">Build 16226</span></span>

<span data-ttu-id="fc0fe-870">Общие сведения о сборке Windows 16226 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-870">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-871">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-871">Fixed</span></span>
- <span data-ttu-id="fc0fe-872">Поддержка системных вызовов, связанных с xattr (getxattr, setxattr, listxattr, removexattr).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-872">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="fc0fe-873">Поддержка security.capablity xattr.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-873">security.capablity xattr support.</span></span>
- <span data-ttu-id="fc0fe-874">Улучшена совместимость с некоторыми файловыми системами и фильтрами, включая серверы SMB сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-874">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="fc0fe-875">[GH 1952]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-875">[GH #1952]</span></span>
- <span data-ttu-id="fc0fe-876">Улучшена поддержка заполнителей OneDrive, заполнителей GVFS и сжатых файлов Compact OS.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-876">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="fc0fe-877">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-877">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="fc0fe-878">Сборка 16215</span><span class="sxs-lookup"><span data-stu-id="fc0fe-878">Build 16215</span></span>

<span data-ttu-id="fc0fe-879">Общие сведения о сборке Windows 16215 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-879">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-880">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-880">Fixed</span></span>
- <span data-ttu-id="fc0fe-881">Для WSL больше не требуется режим разработчика.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-881">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="fc0fe-882">Поддержка соединений каталогов в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-882">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="fc0fe-883">Обработка удаления пакетов appx дистрибутивов WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-883">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="fc0fe-884">Обновление procfs для отображения частных и общих сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-884">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="fc0fe-885">В wslconfig.exe добавлена возможность очистки частично установленных или частично удаленных дистрибутивов.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-885">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="fc0fe-886">Добавлена поддержка IP_MTU_DISCOVER для TCP-сокетов.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-886">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="fc0fe-887">[GH 1639, 2115, 2205]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-887">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="fc0fe-888">Вывод семейства протоколов для маршрутов к AF_INADDR.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-888">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="fc0fe-889">Улучшения для последовательных устройств [GH 1929].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-889">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="fc0fe-890">Сборка 16199</span><span class="sxs-lookup"><span data-stu-id="fc0fe-890">Build 16199</span></span>

<span data-ttu-id="fc0fe-891">Общие сведения о сборке Windows 16199 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-891">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-892">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-892">Fixed</span></span>
- <span data-ttu-id="fc0fe-893">В этих выпусках нет изменений, связанных с WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-893">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="fc0fe-894">Сборка 16193</span><span class="sxs-lookup"><span data-stu-id="fc0fe-894">Build 16193</span></span>

<span data-ttu-id="fc0fe-895">Общие сведения о сборке Windows 16193 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-895">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-896">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-896">Fixed</span></span>
- <span data-ttu-id="fc0fe-897">Исправлено состояние состязания между отправкой SIGCONT и завершением группы потоков [GH 1973].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-897">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="fc0fe-898">Устройства tty и pty изменены для передачи FILE_DEVICE_NAMED_PIPE вместо FILE_DEVICE_CONSOLE [GH 1840].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-898">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="fc0fe-899">Исправление SSH для IP_OPTIONS.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-899">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="fc0fe-900">Подключение DrvFs перемещено в управляющую программу инициализации [GH 1862, 1968, 1767, 1933].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-900">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="fc0fe-901">Добавлена поддержка в DrvFs приведенных ниже символических ссылок NT.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-901">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="fc0fe-902">Сборка 16184</span><span class="sxs-lookup"><span data-stu-id="fc0fe-902">Build 16184</span></span>

<span data-ttu-id="fc0fe-903">Общие сведения о сборке Windows 16184 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-903">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-904">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-904">Fixed</span></span>
- <span data-ttu-id="fc0fe-905">Удалена задача обслуживания пакета apt (lxrun.exe /update).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-905">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="fc0fe-906">Исправлено отсутствие выходных данных из процессов Windows в Node.js [GH 1840].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-906">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="fc0fe-907">Смягчены требования к соответствию в lxcore [GH 1794].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-907">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="fc0fe-908">Исправлена обработка флага AT_EMPTY_PATH в ряде системных вызовов.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-908">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="fc0fe-909">Исправлена проблема, из-за которой удаление файлов DrvFs с открытыми дескрипторами приводило к неопределенному поведению файла [GH 544, 966, 1357, 1535, 1615].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-909">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="fc0fe-910">Теперь /etc/hosts будет наследовать записи из файла hosts Windows (%windir%\System32\Drivers\Etc\hosts) [GH 1495].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-910">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="fc0fe-911">Сборка 16179</span><span class="sxs-lookup"><span data-stu-id="fc0fe-911">Build 16179</span></span>

<span data-ttu-id="fc0fe-912">Общие сведения о сборке Windows 16179 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-912">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-913">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-913">Fixed</span></span>
- <span data-ttu-id="fc0fe-914">На этой неделе изменения в WSL отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-914">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="fc0fe-915">Сборка 16176</span><span class="sxs-lookup"><span data-stu-id="fc0fe-915">Build 16176</span></span>

<span data-ttu-id="fc0fe-916">Общие сведения о сборке Windows 16176 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-916">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-917">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-917">Fixed</span></span>

- <span data-ttu-id="fc0fe-918">[Включена поддержка последовательных устройств](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-918">[Enabled serial support](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)</span></span>
- <span data-ttu-id="fc0fe-919">Добавлен параметр IP-сокета IP_OPTIONS [GH 1116].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-919">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="fc0fe-920">Реализована функция pwritev (при передаче файла в nginx/PHP-FPM) [GH 1506].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-920">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="fc0fe-921">Добавлены параметры IP-сокета IP_MULTICAST_IF и IPV6_MULTICAST_IF [GH 990].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-921">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="fc0fe-922">Поддержка параметров сокета IP_MULTICAST_LOOP и IPV6_MULTICAST_LOOP [GH 1678].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-922">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="fc0fe-923">Добавлен параметр сокета IP(V6)_MTU для приложений node, traceroute, dig, nslookup, host.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-923">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="fc0fe-924">Добавлен параметр IP-сокета IPV6_UNICAST_HOPS.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-924">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- <span data-ttu-id="fc0fe-925">[Улучшения файловой системы](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-925">[Filesystem Improvements](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)</span></span>
    * <span data-ttu-id="fc0fe-926">Разрешено подключение путей UNC.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-926">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="fc0fe-927">Включена поддержка CDFS в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-927">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="fc0fe-928">Правильная обработка разрешений для сетевых файловых систем в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-928">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="fc0fe-929">Добавлена поддержка удаленных дисков в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-929">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="fc0fe-930">Включена поддержка файловой системы FAT в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-930">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="fc0fe-931">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-931">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-932">Результаты LTP</span><span class="sxs-lookup"><span data-stu-id="fc0fe-932">LTP Results</span></span>
<span data-ttu-id="fc0fe-933">Изменения с момента выпуска сборки 15042 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-933">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="fc0fe-934">Сборка 16170</span><span class="sxs-lookup"><span data-stu-id="fc0fe-934">Build 16170</span></span>

<span data-ttu-id="fc0fe-935">Общие сведения о сборке Windows 16170 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-935">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="fc0fe-936">Мы опубликовали новую[запись блога](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/), в которой обсуждаем наши усилия по тестированию WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-936">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="fc0fe-937">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-937">Fixed</span></span>

- <span data-ttu-id="fc0fe-938">Поддержка параметров сокета IP_ADD_MEMBERSHIP и IPV6_ADD_MEMBERSHIP [GH 1678].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-938">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="fc0fe-939">Добавлена поддержка PTRACE_OLDSETOPTIONS.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-939">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="fc0fe-940">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-940">[GH 1692]</span></span>
- <span data-ttu-id="fc0fe-941">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-941">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-942">Результаты LTP</span><span class="sxs-lookup"><span data-stu-id="fc0fe-942">LTP Results</span></span>
<span data-ttu-id="fc0fe-943">Изменения с момента выпуска сборки 15042 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-943">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="fc0fe-944">Сборка 15046 для Windows 10 Creators Update</span><span class="sxs-lookup"><span data-stu-id="fc0fe-944">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="fc0fe-945">В обновление Creators Update для Windows 10 больше не планируется добавлять какие-либо исправления или функции WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-945">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="fc0fe-946">Публикация заметок о выпуске WSL будет возобновлена в ближайшие недели, чтобы охватить дополнения, запланированные в следующих основных версиях в Центре обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-946">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="fc0fe-947">Общие сведения о сборке Windows 15046 и будущих выпусках для программы предварительной оценки доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-947">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="fc0fe-948">Сборка 15042</span><span class="sxs-lookup"><span data-stu-id="fc0fe-948">Build 15042</span></span>

<span data-ttu-id="fc0fe-949">Общие сведения о сборке Windows 15042 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-949">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-950">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-950">Fixed</span></span>

- <span data-ttu-id="fc0fe-951">Устранена взаимоблокировка при удалении пути, завершающегося "..".</span><span class="sxs-lookup"><span data-stu-id="fc0fe-951">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="fc0fe-952">Устранена проблема, из-за которой функция FIONBIO не возвращала 0 при успешном выполнении [GH 1683].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-952">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="fc0fe-953">Устранена проблема с чтением сокетов датаграмм INET нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-953">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="fc0fe-954">Устранена возможная взаимоблокировка из-за состояния состязания при поиске DrvFs в DrvFs [GH 1675].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-954">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="fc0fe-955">Расширена поддержка вспомогательных данных сокетов UNIX, SCM_CREDENTIALS и SCM_RIGHTS [GH 514, 613, 1326].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-955">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="fc0fe-956">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-956">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-957">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-957">LTP Results:</span></span>
<span data-ttu-id="fc0fe-958">Число пройденных тестов: 737.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-958">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="fc0fe-959">Число непройденных тестов (неудачных, пропущенных и т. д.): 255.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-959">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="fc0fe-960">Сборка 15031</span><span class="sxs-lookup"><span data-stu-id="fc0fe-960">Build 15031</span></span>

<span data-ttu-id="fc0fe-961">Общие сведения о сборке Windows 15031 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-961">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-962">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-962">Fixed</span></span>

- <span data-ttu-id="fc0fe-963">Исправлена ошибка, из-за которой поведение time(2) иногда было неправильным.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-963">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="fc0fe-964">Исправлена проблема, из-за которой системный вызов \*SIGPROCMASK мог повредить маску сигнала.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-964">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="fc0fe-965">Теперь в уведомлении о создании процесса WSL возвращается полная длина командной строки.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-965">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="fc0fe-966">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-966">[GH 1632]</span></span>
- <span data-ttu-id="fc0fe-967">Теперь WSL сообщает о выходе из потока посредством ptrace, если GDB перестает отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-967">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="fc0fe-968">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-968">[GH 1196]</span></span>
- <span data-ttu-id="fc0fe-969">Исправлена ошибка, из-за которой устройства pty переставали отвечать на запросы после интенсивного ввода-вывода tmux.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-969">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="fc0fe-970">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-970">[GH 1358]</span></span>
- <span data-ttu-id="fc0fe-971">Исправлена проверка времени ожидания во многих системных вызовах (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-971">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="fc0fe-972">Добавлена поддержка eventfd EFD_SEMAPHORE [GH 452].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-972">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="fc0fe-973">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-973">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-974">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-974">LTP Results:</span></span>
<span data-ttu-id="fc0fe-975">Число пройденных тестов: 737.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-975">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="fc0fe-976">Число непройденных тестов (неудачных, пропущенных и т. д.): 255.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-976">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="fc0fe-977">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="fc0fe-977">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="fc0fe-978">Сборка 15025</span><span class="sxs-lookup"><span data-stu-id="fc0fe-978">Build 15025</span></span>

<span data-ttu-id="fc0fe-979">Общие сведения о сборке Windows 15025 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-979">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-980">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-980">Fixed</span></span>

- <span data-ttu-id="fc0fe-981">Исправлена ошибка, которая нарушала работу grep 2.27 [GH 1578].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-981">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="fc0fe-982">Реализован флаг EFD_SEMAPHORE для системного вызова eventfd2 [GH 452].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-982">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="fc0fe-983">Реализован файл /proc/[pid]/net/ipv6_route [GH 1608].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-983">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="fc0fe-984">Поддержка управляемого сигналами ввода-вывода для сокетов потоков UNIX [GH 393, 68].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-984">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="fc0fe-985">Поддержка F_GETPIPE_SZ и F_SETPIPE_SZ [GH 1012].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-985">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="fc0fe-986">Реализация системного вызова recvmmsg() [GH 1531].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-986">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="fc0fe-987">Исправлена ошибка, из-за которой функция epoll_wait() не ожидала выполнения [GH 1609].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-987">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="fc0fe-988">Реализация /proc/version_signature.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-988">Implement /proc/version_signature</span></span>
- <span data-ttu-id="fc0fe-989">Теперь системный вызов Tee возвращает ошибку, если оба дескриптора файла ссылаются на один и тот же канал.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-989">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="fc0fe-990">Реализовано правильное поведение SO_PEERCRED для сокетов UNIX.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-990">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="fc0fe-991">Исправлена недопустимая обработка параметров системного вызова tkill.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-991">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="fc0fe-992">Внесены изменения для увеличения производительности DrvFs.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-992">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="fc0fe-993">Незначительное исправление блокировки ввода-вывода Ruby.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-993">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="fc0fe-994">Исправлена проблема, из-за которой функция recvmsg() возвращала EINVAL для флага MSG_DONTWAIT для сокетов INET [GH 1296].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-994">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="fc0fe-995">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-995">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-996">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-996">LTP Results:</span></span>
<span data-ttu-id="fc0fe-997">Число пройденных тестов: 732.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-997">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="fc0fe-998">Число непройденных тестов (неудачных, пропущенных и т. д.): 255.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-998">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="fc0fe-999">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="fc0fe-999">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="fc0fe-1000">Сборка 15019</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1000">Build 15019</span></span>

<span data-ttu-id="fc0fe-1001">Общие сведения о сборке Windows 15019 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1001">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-1002">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1002">Fixed</span></span>

- <span data-ttu-id="fc0fe-1003">Исправлена ошибка, из-за которой отображались неправильные данные об использовании ЦП в procfs для таких инструментов, как htop [GH 823, 945, 971].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1003">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="fc0fe-1004">Теперь при вызове Open() с O_TRUNC для существующего файла inotify теперь создает IN_MODIFY до IN_OPEN.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1004">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="fc0fe-1005">Исправление getsockopt SO_ERROR в сокетах UNIX для включения возможностей postgress [GH 61, 1354].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1005">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="fc0fe-1006">Реализация /proc/sys/net/core/somaxconn для языка GO.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1006">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="fc0fe-1007">Теперь фоновая задача обновления пакета apt-get запускается из представления в скрытом режиме.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1007">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="fc0fe-1008">Очищена область для IPv6-адреса localhost (сбой (Spring-Framework(Java)).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1008">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="fc0fe-1009">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1009">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-1010">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1010">LTP Results:</span></span>
<span data-ttu-id="fc0fe-1011">Число пройденных тестов: 714.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1011">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="fc0fe-1012">Число непройденных тестов (неудачных, пропущенных и т. д.): 249.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1012">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="fc0fe-1013">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1013">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="fc0fe-1014">Сборка 15014</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1014">Build 15014</span></span>

<span data-ttu-id="fc0fe-1015">Общие сведения о сборке Windows 15014 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1015">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-1016">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1016">Fixed</span></span>

- <span data-ttu-id="fc0fe-1017">Нажатие клавиш CTRL+C теперь работает ожидаемым образом.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1017">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="fc0fe-1018">Теперь htop и ps auxw показывают правильные данные об использовании ресурсов (GH 516).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1018">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="fc0fe-1019">Простое преобразование исключений NT в сигналы.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1019">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="fc0fe-1020">(GH 513)</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1020">(GH #513)</span></span>
- <span data-ttu-id="fc0fe-1021">Теперь при нехватке пространства fallocate завершается ошибкой ENOSPC вместо EINVAL (GH 1571).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1021">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="fc0fe-1022">Добавлен /proc/sys/kernel/sem.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1022">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="fc0fe-1023">Реализованы системные вызовы semop и semtimedop.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1023">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="fc0fe-1024">Устранены ошибки nslookup, связанные с параметрами сокета IP_RECVTOS и IPV6_RECVTCLASS (GH 69).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1024">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="fc0fe-1025">Поддержка параметров сокета IP_RECVTTL и IPV6_RECVHOPLIMIT.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1025">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="fc0fe-1026">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1026">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-1027">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1027">LTP Results:</span></span>
<span data-ttu-id="fc0fe-1028">Число пройденных тестов: 709.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1028">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="fc0fe-1029">Число непройденных тестов (неудачных, пропущенных и т. д.): 255.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1029">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="fc0fe-1030">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1030">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="fc0fe-1031">Сводка по системным вызовам</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1031">Syscall Summary</span></span>
<span data-ttu-id="fc0fe-1032">Всего системных вызовов: 384</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1032">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="fc0fe-1033">Всего реализовано: 235.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1033">Total Implemented: 235</span></span> </br>
<span data-ttu-id="fc0fe-1034">Всего заглушено: 22</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1034">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="fc0fe-1035">Всего не реализовано: 127</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1035">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="fc0fe-1036">Подробная разбивка</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1036">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="fc0fe-1037">Сборка 15007</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1037">Build 15007</span></span>

<span data-ttu-id="fc0fe-1038">Общие сведения о сборке Windows 15007 доступны в [блоге о Windows]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1038">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="fc0fe-1039">Известная проблема</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1039">Known Issue</span></span>

- <span data-ttu-id="fc0fe-1040">Существует известная ошибка, из-за которой консоль не распознает некоторые клавиши CTRL+<key>.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1040">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="fc0fe-1041">Сюда входит команда CTRL+C, которая будет функционировать как обычное нажатие клавиши C.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1041">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="fc0fe-1042">Возможное решение. Сопоставьте альтернативную клавишу с клавишами CTRL+C.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1042">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="fc0fe-1043">Например, чтобы сопоставить клавиши CTRL+K с CTRL+C, выполните следующее: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1043">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="fc0fe-1044">Это сопоставление действует в пределах терминала и должно выполняться *при каждом* запуске Bash.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1044">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="fc0fe-1045">Пользователи могут изучить этот параметр, чтобы включить его в `.bashrc`.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1045">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="fc0fe-1046">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1046">Fixed</span></span>

- <span data-ttu-id="fc0fe-1047">Исправлена ошибка, из-за которой подсистема WSL потребляла 100 % ресурсов ядра ЦП.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1047">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="fc0fe-1048">Теперь поддерживаются параметры сокета IP_PKTINFO и IPV6_RECVPKTINFO.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1048">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="fc0fe-1049">(GH 851, 987)</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1049">(GH #851, 987)</span></span>
- <span data-ttu-id="fc0fe-1050">Усечение физического адреса сетевого интерфейса до 16 байтов в lxcore (GH #1452, 1414, 1343, 468, 308).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1050">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="fc0fe-1051">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1051">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-1052">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1052">LTP Results:</span></span>
<span data-ttu-id="fc0fe-1053">Число пройденных тестов: 709.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1053">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="fc0fe-1054">Число непройденных тестов (неудачных, пропущенных и т. д.): 255.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1054">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="fc0fe-1055">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1055">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="fc0fe-1056">Сборка 15002</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1056">Build 15002</span></span>

<span data-ttu-id="fc0fe-1057">Общие сведения о сборке Windows 15002 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1057">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="fc0fe-1058">Известная проблема</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1058">Known Issue</span></span>

<span data-ttu-id="fc0fe-1059">Две известные проблемы:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1059">Two known issues:</span></span>
- <span data-ttu-id="fc0fe-1060">Существует известная ошибка, из-за которой консоль не распознает некоторые клавиши CTRL+<key>.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1060">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="fc0fe-1061">Сюда входит команда CTRL+C, которая будет функционировать как обычное нажатие клавиши C.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1061">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="fc0fe-1062">Возможное решение. Сопоставьте альтернативную клавишу с клавишами CTRL+C.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1062">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="fc0fe-1063">Например, чтобы сопоставить клавиши CTRL+K с CTRL+C, выполните следующее: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1063">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="fc0fe-1064">Это сопоставление действует в пределах терминала и должно выполняться *при каждом* запуске Bash.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1064">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="fc0fe-1065">Пользователи могут изучить этот параметр, чтобы включить его в `.bashrc`.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1065">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="fc0fe-1066">Во время выполнения WSL системный поток потребляет 100 % ресурсов ядра ЦП.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1066">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="fc0fe-1067">Первопричина устранена и исправлена внутри компонента.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1067">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="fc0fe-1068">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1068">Fixed</span></span>

- <span data-ttu-id="fc0fe-1069">Все сеансы Bash теперь должны создаваться на одном уровне разрешений.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1069">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="fc0fe-1070">Попытка запустить сеанс на другом уровне будет заблокирована.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1070">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="fc0fe-1071">Это означает, что консоль администратора и консоль пользователя, не являющегося администратором, не могут работать одновременно.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1071">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="fc0fe-1072">(GH 626)</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1072">(GH #626)</span></span>
<br/>
- <span data-ttu-id="fc0fe-1073">Реализованы следующие сообщения NETLINK_ROUTE (требуются права администратора Windows):</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1073">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="fc0fe-1074">RTM_NEWADDR (поддерживает `ip addr add`);</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1074">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="fc0fe-1075">RTM_NEWROUTE (поддерживает `ip route add`);</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1075">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="fc0fe-1076">RTM_DELADDR (поддерживает `ip addr del`);</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1076">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="fc0fe-1077">RTM_DELROUTE (поддерживает `ip route del`).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1077">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="fc0fe-1078">Проверка запланированных задач для пакетов, которые необходимо обновить, больше не будет выполняться при лимитном подключении (GH 1371).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1078">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="fc0fe-1079">Исправлена ошибка, из-за которой канал переставал отвечать на запросы, например bash -c "ls -alR /" | bash -c "cat" (GH 1214).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1079">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="fc0fe-1080">Реализован параметр сокета TCP_KEEPCNT (GH 843).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1080">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="fc0fe-1081">Реализован параметр сокета INET IP_MTU_DISCOVER (GH 720, 717, 170, 69).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1081">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="fc0fe-1082">Удалены устаревшие функции для запуска двоичных файлов NT из init с помощью поиска по пути NT.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1082">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="fc0fe-1083">(GH 1325)</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1083">(GH #1325)</span></span>
- <span data-ttu-id="fc0fe-1084">Исправлен режим /dev/kmsg для разрешения группового и другого доступа на чтение (0644) (GH 1321).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1084">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="fc0fe-1085">Реализован файл /proc/sys/kernel/random/uuid [GH 1092].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1085">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="fc0fe-1086">Исправлена ошибка, из-за которой время начала процесса отображалось как 2432 год (GH 974).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1086">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="fc0fe-1087">Переменная среды TERM по умолчанию заменена xterm-256color (GH 1446).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1087">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="fc0fe-1088">Изменен способ вычисления фиксации процесса во время ветвления процесса.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1088">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="fc0fe-1089">(GH 1286)</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1089">(GH #1286)</span></span>
- <span data-ttu-id="fc0fe-1090">Реализован файл /proc/sys/VM/overcommit_memory.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1090">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="fc0fe-1091">(GH 1286)</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1091">(GH #1286)</span></span>
- <span data-ttu-id="fc0fe-1092">Реализован файл /proc/net/route (GH 69).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1092">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="fc0fe-1093">Исправлена ошибка, из-за которой имя ярлыка было неправильно локализовано (GH 696).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1093">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="fc0fe-1094">Исправлена логика анализа ELF, которая неправильно проверяла заголовки программ, которые должны быть меньше или равны PATH_MAX.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1094">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="fc0fe-1095">(GH 1048)</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1095">(GH #1048)</span></span>
- <span data-ttu-id="fc0fe-1096">Реализован обратный вызов statfs для procfs, sysfs, cgroupfs и binfmtf (GH 1378).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1096">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="fc0fe-1097">Исправлены окна AptPackageIndexUpdate, которые не закрывались (GH 1184, также обсуждается в GH 1193).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1097">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="fc0fe-1098">Добавлена поддержка ADDR_NO_RANDOMIZE в ASLR personality.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1098">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="fc0fe-1099">[GH 1148, 1128]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1099">(GH #1148, 1128)</span></span>
- <span data-ttu-id="fc0fe-1100">Улучшена функция PTRACE_GETSIGINFO для SIGSEGV для обеспечения правильных трассировок стека GDB во время операций AV (GH 875).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1100">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="fc0fe-1101">Анализ ELF больше не завершается ошибкой для двоичных файлов patchelf.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1101">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="fc0fe-1102">(GH 471)</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1102">(GH #471)</span></span>
- <span data-ttu-id="fc0fe-1103">DNS-сервер VPN добавлен в /etc/resolv.conf (GH 416, 1350).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1103">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="fc0fe-1104">Улучшено закрытие TCP-подключений для более надежной передачи данных.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1104">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="fc0fe-1105">(GH 610, 616, 1025, 1335)</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1105">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="fc0fe-1106">Теперь возвращается правильный код ошибки при открытии слишком большого числа файлов (EMFILE).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1106">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="fc0fe-1107">[GH 1126, 2090]</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1107">(GH #1126, 2090)</span></span>
- <span data-ttu-id="fc0fe-1108">Журнал аудита Windows теперь отображает имя образа при аудите процесса создания.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1108">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="fc0fe-1109">Теперь запуск bash.exe из окна Bash корректно завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1109">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="fc0fe-1110">Добавлено сообщение об ошибке, когда служба взаимодействия не может получить доступ к рабочему каталогу в LxFs (например, notepad.exe. bashrc).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1110">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="fc0fe-1111">Исправлена проблема, из-за которой путь Windows в WSL был усеченным.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1111">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="fc0fe-1112">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1112">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-1113">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1113">LTP Results:</span></span>
<span data-ttu-id="fc0fe-1114">Число пройденных тестов: 690.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1114">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="fc0fe-1115">Число непройденных тестов (неудачных, пропущенных и т. д.): 274.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1115">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="fc0fe-1116">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1116">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="fc0fe-1117">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1117">Syscall Support</span></span>
<span data-ttu-id="fc0fe-1118">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1118">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="fc0fe-1119">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1119">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="fc0fe-1120">Сборка 14986</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1120">Build 14986</span></span>

<span data-ttu-id="fc0fe-1121">Общие сведения о сборке Windows 14986 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1121">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-1122">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1122">Fixed</span></span>

- <span data-ttu-id="fc0fe-1123">Исправлены ошибки NETLINK и PTY IOCTL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1123">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="fc0fe-1124">Теперь отображается версия ядра 4.4.0-43 для обеспечения согласованности с Xenial.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1124">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="fc0fe-1125">Теперь Bash.exe запускается, когда ввод направляется в "nul:" (GH 1259).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1125">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="fc0fe-1126">Теперь идентификаторы потоков отображаются правильно в procfs (GH 967).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1126">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="fc0fe-1127">Теперь в inotify_add_watch() поддерживаются флаги IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR (GH 1280).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1127">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="fc0fe-1128">Реализован timer_create и связанные системные вызовы.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1128">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="fc0fe-1129">Это обеспечивает поддержку GHC (GH 307).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1129">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="fc0fe-1130">Исправлена проблема, из-за которой проверка связи возвращала время 0,000 мс (GH 1296).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1130">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="fc0fe-1131">Возвращается правильный код ошибки при открытии слишком большого числа файлов.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1131">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="fc0fe-1132">Исправлена проблема в WSL, из-за которой запрос NETLINK на данные сетевого интерфейса завершался ошибкой EINVAL, если аппаратный адрес интерфейса был 32-байтовым (например, интерфейс Teredo).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1132">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="fc0fe-1133">Обратите внимание на то, что служебная программа Linux "ip" содержит ошибку, из-за которой произойдет сбой, если WSL сообщит 32-байтовый адрес оборудования.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1133">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="fc0fe-1134">Это ошибка в "ip", а не в WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1134">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="fc0fe-1135">В служебной программе "ip" жестко запрограммирована длина строкового буфера, используемого для вывода адреса оборудования, и этот буфер слишком мал для вывода 32-байтового адреса оборудования.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1135">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="fc0fe-1136">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1136">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-1137">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1137">LTP Results:</span></span>
<span data-ttu-id="fc0fe-1138">Число пройденных тестов: 669.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1138">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="fc0fe-1139">Число непройденных тестов (неудачных, пропущенных и т. д.): 258</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1139">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="fc0fe-1140">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1140">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="fc0fe-1141">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1141">Syscall Support</span></span>
<span data-ttu-id="fc0fe-1142">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1142">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="fc0fe-1143">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1143">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="fc0fe-1144">Сборка 14971</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1144">Build 14971</span></span>

<span data-ttu-id="fc0fe-1145">Общие сведения о сборке Windows 14971 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1145">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-1146">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1146">Fixed</span></span>

 - <span data-ttu-id="fc0fe-1147">Из-за независящих от нас обстоятельств в этой сборке не будет обновлений для подсистемы Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1147">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="fc0fe-1148">Регулярный выпуск плановых обновлений будет возобновлен в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1148">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-1149">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1149">LTP Results:</span></span>
<span data-ttu-id="fc0fe-1150">без изменений с момента выпуска сборки 14965.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1150">Unchanged from 14965</span></span> </br>
<span data-ttu-id="fc0fe-1151">Число пройденных тестов: 664</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1151">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="fc0fe-1152">Число непройденных тестов (неудачных, пропущенных и т. д.): 263.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1152">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="fc0fe-1153">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1153">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="fc0fe-1154">Сборка 14965</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1154">Build 14965</span></span>

<span data-ttu-id="fc0fe-1155">Общие сведения о сборке Windows 14965 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1155">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-1156">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1156">Fixed</span></span>

- <span data-ttu-id="fc0fe-1157">Поддержка RTM_GETLINK и RTM_GETADDR для NETLINK_ROUTE в сокетах NETLINK (GH 468).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1157">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="fc0fe-1158">Применение команд ifconfig и ip для перечисления сетей.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1158">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="fc0fe-1159">Дополнительные сведения см. в нашей [записи блога о сетях WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1159">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="fc0fe-1160">Теперь /sbin добавляется в путь пользователя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1160">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="fc0fe-1161">Теперь путь пользователя NT по умолчанию добавляется к пути WSL (т. е. теперь можно ввести notepad.exe, не добавляя System32 в путь Linux).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1161">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="fc0fe-1162">Добавлена поддержка /proc/sys/kernel/cap_last_cap.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1162">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="fc0fe-1163">Теперь двоичные файлы NT можно запускать из WSL, если текущий рабочий каталог содержит знаки, отличные от ANSI (GH 1254).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1163">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="fc0fe-1164">Разрешено завершение работы при отключении сокета потока UNIX.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1164">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="fc0fe-1165">Добавлена поддержка PR_GET_PDEATHSIG.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1165">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="fc0fe-1166">Добавлена поддержка CLONE_PARENT.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1166">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="fc0fe-1167">Исправлена ошибка, из-за которой канал переставал отвечать на запросы, например bash -c "ls -alR /" | bash -c "cat" (GH 1214).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1167">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="fc0fe-1168">Обработка запросов на подключение к текущему терминалу.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1168">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="fc0fe-1169">Файл /proc/<pid>/oom_score_adj помечен как записываемый.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1169">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="fc0fe-1170">Добавлена папку /sys/fs/cgroup.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1170">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="fc0fe-1171">Функция sched_setaffinity должна возвращать значение маски битов сходства.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1171">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="fc0fe-1172">Исправлена логика проверки ELF, которая неправильно предполагала, что пути интерпретатора должны содержать менее 64 знаков.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1172">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="fc0fe-1173">(GH 743)</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1173">(GH #743)</span></span>
- <span data-ttu-id="fc0fe-1174">Открытые дескрипторы файлов могут оставаться открытыми в окне консоли (GH 1187).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1174">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="fc0fe-1175">Устранена ошибка, из-за которой происходил сбой rename(), если имя цели содержало конечную косую черту (GH 1008).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1175">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="fc0fe-1176">Реализован файл /proc/net/dev.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1176">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="fc0fe-1177">Исправлена ошибка, из-за которой при проверке связи возвращалось значение 0,000 мс из-за разрешения таймера.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1177">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="fc0fe-1178">Реализован файл /proc/self/environ (GH 730).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1178">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="fc0fe-1179">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1179">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-1180">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1180">LTP Results:</span></span>
<span data-ttu-id="fc0fe-1181">Число пройденных тестов: 664</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1181">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="fc0fe-1182">Число непройденных тестов (неудачных, пропущенных и т. д.): 263.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1182">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="fc0fe-1183">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1183">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="fc0fe-1184">Сборка 14959</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1184">Build 14959</span></span>

<span data-ttu-id="fc0fe-1185">Общие сведения о сборке Windows 14959 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1185">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-1186">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1186">Fixed</span></span>

- <span data-ttu-id="fc0fe-1187">Улучшены уведомления о процессе Pico для Windows.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1187">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="fc0fe-1188">Дополнительные сведения см. в [блоге о WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1188">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="fc0fe-1189">Повышена стабильность взаимодействия с Windows.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1189">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="fc0fe-1190">Устранена ошибка 0x80070057, возникавшая при запуске bash.exe при включенной защите корпоративных данных (EDP).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1190">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="fc0fe-1191">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1191">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-1192">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1192">LTP Results:</span></span>
<span data-ttu-id="fc0fe-1193">Число пройденных тестов: 665</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1193">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="fc0fe-1194">Число непройденных тестов (неудачных, пропущенных и т. д.): 263.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1194">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="fc0fe-1195">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1195">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="fc0fe-1196">Сборка 14955</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1196">Build 14955</span></span>

<span data-ttu-id="fc0fe-1197">Общие сведения о сборке Windows 14955 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1197">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-1198">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1198">Fixed</span></span>

 - <span data-ttu-id="fc0fe-1199">Из-за независящих от нас обстоятельств в этой сборке не будет обновлений для подсистемы Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1199">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="fc0fe-1200">Регулярный выпуск плановых обновлений будет возобновлен в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1200">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-1201">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1201">LTP Results:</span></span>
<span data-ttu-id="fc0fe-1202">Число пройденных тестов: 665</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1202">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="fc0fe-1203">Число непройденных тестов (неудачных, пропущенных и т. д.): 263.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1203">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="fc0fe-1204">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1204">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="fc0fe-1205">Сборка 14951</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1205">Build 14951</span></span>

<span data-ttu-id="fc0fe-1206">Общие сведения о сборке Windows 14951 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1206">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="fc0fe-1207">Новая функция: взаимодействие Ubuntu и Windows</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1207">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="fc0fe-1208">Теперь двоичные файлы Windows можно вызывать непосредственно из командной строки WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1208">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="fc0fe-1209">Это дает пользователям возможность взаимодействовать со средой и системой Windows способом, который ранее был невозможен.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1209">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="fc0fe-1210">Например, теперь пользователи могут выполнять следующие команды.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1210">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="fc0fe-1211">Дополнительные сведения:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1211">More information can be found at:</span></span>

- [<span data-ttu-id="fc0fe-1212">Блог команды WSL по взаимодействию</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1212">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="fc0fe-1213">Документация по взаимодействию на сайте MSDN</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1213">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="fc0fe-1214">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1214">Fixed</span></span>

- <span data-ttu-id="fc0fe-1215">Ubuntu 16.04 (Xenial) теперь устанавливается для всех новых экземпляров WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1215">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="fc0fe-1216">Существующие у пользователей экземпляры Ubuntu 14.04 (Trusty) не будут обновляться автоматически.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1216">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="fc0fe-1217">Теперь отображается языковой стандарт, установленный во время установки.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1217">Locale set during install is now displayed</span></span>
- <span data-ttu-id="fc0fe-1218">Улучшения в терминале, включая устранение ошибки, из-за которой перенаправление процесса WSL в файл не всегда работало.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1218">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="fc0fe-1219">Время существования консоли должно быть связано со временем существования bash.exe.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1219">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="fc0fe-1220">Размер окна консоли должен быть основан на видимом размере, а не размере буфера.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1220">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="fc0fe-1221">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1221">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-1222">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1222">LTP Results:</span></span>
<span data-ttu-id="fc0fe-1223">Число пройденных тестов: 665</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1223">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="fc0fe-1224">Число непройденных тестов (неудачных, пропущенных и т. д.): 263.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1224">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="fc0fe-1225">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1225">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="fc0fe-1226">Сборка 14946</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1226">Build 14946</span></span>

<span data-ttu-id="fc0fe-1227">Общие сведения о сборке Windows 14946 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1227">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-1228">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1228">Fixed</span></span>

- <span data-ttu-id="fc0fe-1229">Устранена проблема, которая не позволила создавать учетные записи WSL для пользователей с именами пользователей NT, содержащими пробелы или кавычки.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1229">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="fc0fe-1230">Внесены изменения в VolFs и DrvFs, чтобы возвращалось значение 0 для количества ссылок каталога в stat.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1230">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="fc0fe-1231">Поддержка параметра сокета IPV6_MULTICAST_HOPS.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1231">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="fc0fe-1232">Ограничение в один цикл ввода-вывода консоли на tty.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1232">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="fc0fe-1233">Например, можно выполнить следующую команду:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1233">Example: the following command is possible:</span></span>
  - <span data-ttu-id="fc0fe-1234">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1234">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="fc0fe-1235">Пробелы в /proc/cpuinfo заменены символами табуляции (GH 1115).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1235">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="fc0fe-1236">DrvFs теперь отображается в mountinfo с именем, совпадающим с подключенным томом Windows.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1236">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="fc0fe-1237">Теперь /home и /root отображаются в mountinfo с правильными именами.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1237">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="fc0fe-1238">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1238">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-1239">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1239">LTP Results:</span></span>
<span data-ttu-id="fc0fe-1240">Число пройденных тестов: 665</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1240">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="fc0fe-1241">Число непройденных тестов (неудачных, пропущенных и т. д.): 263.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1241">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="fc0fe-1242">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1242">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="fc0fe-1243">Сборка 14942</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1243">Build 14942</span></span>

<span data-ttu-id="fc0fe-1244">Общие сведения о сборке Windows 14942 доступны в [блоге о Windows](https://aka.ms/onefourninefourtwoooooo).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1244">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-1245">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1245">Fixed</span></span>

- <span data-ttu-id="fc0fe-1246">Исправлен ряд ошибок, в том числе сбой сети "ATTEMPTED EXECUTE OF NOEXECUTE MEMORY" (Попытка выполнения в недоступной памяти), которые блокируют SSH.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1246">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="fc0fe-1247">Добавлена поддержка inotifiy для уведомлений, созданных в приложениях для Windows в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1247">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="fc0fe-1248">Реализованы параметры TCP_KEEPIDLE и TCP_KEEPINTVL для mongod.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1248">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="fc0fe-1249">(GH 695)</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1249">(GH #695)</span></span>
- <span data-ttu-id="fc0fe-1250">Реализован системный вызов pivot_root.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1250">Implement the pivot_root system call</span></span>
- <span data-ttu-id="fc0fe-1251">Реализован параметр сокета для SO_DONTROUTE.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1251">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="fc0fe-1252">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1252">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="fc0fe-1253">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1253">LTP Results:</span></span>
<span data-ttu-id="fc0fe-1254">Число пройденных тестов: 665</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1254">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="fc0fe-1255">Число непройденных тестов (неудачных, пропущенных и т. д.): 263.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1255">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="fc0fe-1256">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1256">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="fc0fe-1257">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1257">Syscall Support</span></span>
<span data-ttu-id="fc0fe-1258">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1258">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="fc0fe-1259">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1259">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="fc0fe-1260">Сборка 14936</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1260">Build 14936</span></span>

<span data-ttu-id="fc0fe-1261">Общие сведения о сборке Windows 14936 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1261">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="fc0fe-1262">Примечание. В предстоящем выпуске WSL будет устанавливать версию Ubuntu 16.04 (Xenial) вместо Ubuntu 14.04 (Trusty).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1262">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="fc0fe-1263">Это изменение будет применено к участникам программы предварительной оценки, которые устанавливают новые экземпляры (lxrun.exe /install или первый запуск bash.exe).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1263">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="fc0fe-1264">Существующие экземпляры с версией Trusty не будут обновлены автоматически.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1264">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="fc0fe-1265">Пользователи могут обновить свой образ Trusty до версии Xenial с помощью команды do-release-upgrade.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1265">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="fc0fe-1266">Известная проблема</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1266">Known Issue</span></span>
<span data-ttu-id="fc0fe-1267">В WSL существует проблема с реализацией некоторых сокетов.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1267">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="fc0fe-1268">Ошибка проявляется как сбой "ATTEMPTED EXECUTE OF NOEXECUTE MEMORY" (Попытка выполнения в недоступной памяти).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1268">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="fc0fe-1269">Чаще всего этот сбой происходит при использовании SSH.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1269">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="fc0fe-1270">Первопричина исправлена во внутренних сборках, и исправление будет добавлено в сборки для программы предварительной оценки при первой возможности.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1270">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="fc0fe-1271">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1271">Fixed</span></span>

- <span data-ttu-id="fc0fe-1272">Реализован системный вызов chroot.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1272">Implemented the chroot system call</span></span>
- <span data-ttu-id="fc0fe-1273">Улучшения в inotify, ~~включая поддержку уведомлений, созданных в приложениях для Windows в DrvFs~~.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1273">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="fc0fe-1274">Исправление: В настоящее время недоступна поддержка в inotify изменений, исходящих из приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1274">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="fc0fe-1275">Привязка сокета к IPV6::<port n> теперь поддерживает IPV6_V6ONLY (GH 68, 157, 393, 460, 674, 740, 982, 996).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1275">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="fc0fe-1276">Реализовано поведение WNOWAIT для системного вызова waitid (GH 638).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1276">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="fc0fe-1277">Поддержка параметров IP-сокета IP_HDRINCL и IP_TTL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1277">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="fc0fe-1278">Результат read() нулевой длины должен возвращаться немедленно (GH 975).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1278">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="fc0fe-1279">Правильная обработка имен файлов и префиксов имен файлов, которые не содержат терминатор NULL в TAR-файле.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1279">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="fc0fe-1280">Поддержка epoll для /dev/null.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1280">epoll support for /dev/null</span></span>
- <span data-ttu-id="fc0fe-1281">Исправлен источник времени /dev/alarm.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1281">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="fc0fe-1282">Теперь команда bash -c может выполнять перенаправление в файл.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1282">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="fc0fe-1283">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1283">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-1284">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1284">LTP Results:</span></span>
<span data-ttu-id="fc0fe-1285">Число пройденных тестов: 664</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1285">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="fc0fe-1286">Число непройденных тестов (неудачных, пропущенных и т. д.): 264.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1286">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="fc0fe-1287">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1287">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="fc0fe-1288">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1288">Syscall Support</span></span>
<span data-ttu-id="fc0fe-1289">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1289">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="fc0fe-1290">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1290">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="fc0fe-1291">Сборка 14931</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1291">Build 14931</span></span>

<span data-ttu-id="fc0fe-1292">Общие сведения о сборке Windows 14931 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1292">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-1293">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1293">Fixed</span></span>

 - <span data-ttu-id="fc0fe-1294">Из-за независящих от нас обстоятельств в этой сборке не будет обновлений для подсистемы Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1294">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="fc0fe-1295">Регулярный выпуск плановых обновлений будет возобновлен в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1295">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="fc0fe-1296">Сборка 14926</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1296">Build 14926</span></span>

<span data-ttu-id="fc0fe-1297">Общие сведения о сборке Windows 14926 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1297">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-1298">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1298">Fixed</span></span>

- <span data-ttu-id="fc0fe-1299">Проверка связи теперь работает в консолях без привилегий администратора.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1299">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="fc0fe-1300">Теперь поддерживается ping6, также без привилегий администратора.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1300">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="fc0fe-1301">Поддержка в inotify файлов, измененных посредством WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1301">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="fc0fe-1302">(GH 216)</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1302">(GH #216)</span></span>
  - <span data-ttu-id="fc0fe-1303">Поддерживаемые флаги:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1303">Flags supported:</span></span>
    - <span data-ttu-id="fc0fe-1304">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1304">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="fc0fe-1305">События inotify_add_watch: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1305">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="fc0fe-1306">Атрибуты inotify_add_watch: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1306">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="fc0fe-1307">Выходные данные чтения: LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1307">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="fc0fe-1308">Известная проблема: Изменение файлов из приложений Windows не приводит к созданию событий.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1308">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="fc0fe-1309">Сокет UNIX теперь поддерживает SCM_CREDENTIALS.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1309">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc0fe-1310">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1310">LTP Results:</span></span>
<span data-ttu-id="fc0fe-1311">Число пройденных тестов: 651</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1311">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="fc0fe-1312">Число непройденных тестов (неудачных, пропущенных и т. д.): 258</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1312">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="fc0fe-1313">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1313">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="fc0fe-1314">Сборка 14915</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1314">Build 14915</span></span>

<span data-ttu-id="fc0fe-1315">Общие сведения о сборке Windows 14915 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1315">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-1316">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1316">Fixed</span></span>
-  <span data-ttu-id="fc0fe-1317">Socketpair для сокетов датаграмм UNIX (GH 262).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1317">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="fc0fe-1318">Поддержка сокетов UNIX для SO_REUSEADDR.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1318">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="fc0fe-1319">Поддержка сокетов UNIX для SO_BROADCAST (GH 568).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1319">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="fc0fe-1320">Поддержка сокетов UNIX для SOCK_SEQPACKET (GH 758, 546).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1320">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="fc0fe-1321">Добавлена поддержка send, recv и shutdown для сокетов датаграмм UNIX.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1321">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="fc0fe-1322">Устранена ошибка из-за неправильной проверки параметров mmap для нефиксированных адресов.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1322">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="fc0fe-1323">(GH 847)</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1323">(GH #847)</span></span>
- <span data-ttu-id="fc0fe-1324">Поддержка приостановки и возобновления состояний терминала.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1324">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="fc0fe-1325">Поддержка TIOCPKT ioctl для разблокировки служебной программы Screen (GH 774).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1325">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="fc0fe-1326">Известная проблема: Не работают функциональные клавиши.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1326">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="fc0fe-1327">Исправлено состязание в TimerFd, которое могло привести к обращению LxpTimerFdWorkerRoutine к освобожденному элементу ReaderReady (GH 814).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1327">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="fc0fe-1328">Включена поддержка перезапускаемых системных вызовов для futex, poll и clock_nanosleep.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1328">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="fc0fe-1329">Добавлена поддержка подключения привязки.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1329">Added bind mount support</span></span>
- <span data-ttu-id="fc0fe-1330">Поддержка отмены общего доступа для пространства имен подключения.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1330">unshare for mount namespace support</span></span>
    - <span data-ttu-id="fc0fe-1331">Известная проблема: При создании пространства имен подключения посредством `unshare(CLONE_NEWNS)` текущий рабочий каталог будет по-прежнему указывать на старое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1331">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="fc0fe-1332">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1332">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="fc0fe-1333">Сборка 14905</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1333">Build 14905</span></span>

<span data-ttu-id="fc0fe-1334">Общие сведения о сборке Windows 14905 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1334">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-1335">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1335">Fixed</span></span>
- <span data-ttu-id="fc0fe-1336">Теперь поддерживаются перезапускаемые системные вызовы (GH 349, GH 520).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1336">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="fc0fe-1337">Теперь функционируют символические ссылки на каталоги, которые заканчиваются косой чертой "/" (GH 650).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1337">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="fc0fe-1338">Реализован параметр RNDGETENTCNT ioctl для /dev/random.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1338">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="fc0fe-1339">Реализованы файлы /proc/[pid]/mounts, /proc/[pid]/mountinfo и /proc/[pid]/mountstats.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1339">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="fc0fe-1340">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1340">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="fc0fe-1341">Сборка 14901</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1341">Build 14901</span></span>
<span data-ttu-id="fc0fe-1342">Первая сборка для программы предварительной оценки для выпуска после юбилейного обновления Windows 10.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1342">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="fc0fe-1343">Общие сведения о сборке Windows 14901 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1343">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-1344">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1344">Fixed</span></span>
- <span data-ttu-id="fc0fe-1345">Исправлена проблема конечной косой черты.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1345">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="fc0fe-1346">Теперь работают такие команды, как `$ mv a/c/ a/b/`.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1346">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="fc0fe-1347">Теперь при установке отображается запрос, позволяющий установить языковый стандарт Ubuntu, совпадающий с языковым стандартом Windows.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1347">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="fc0fe-1348">Поддержка procfs для папки ns.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1348">Procfs support for ns folder</span></span>
- <span data-ttu-id="fc0fe-1349">Добавлены функции подключения и отключения для файловых систем tmpfs, procfs и sysfs.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1349">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="fc0fe-1350">Исправлена 32-разрядная подпись ABI для mknod[at].</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1350">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="fc0fe-1351">Сокеты UNIX переведены на модель диспетчеризации.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1351">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="fc0fe-1352">Размер буфера recv сокета INET, заданный с помощью setsockopt, должен учитываться.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1352">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="fc0fe-1353">Реализован флаг получения сообщения MSG_CMSG_CLOEXEC для сокетов UNIX.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1353">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="fc0fe-1354">Перенаправление канала stdin/stdout процесса Linux (GH 2).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1354">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="fc0fe-1355">Разрешена конвейерная передача команд bash -c в командную строку.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1355">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="fc0fe-1356">Пример:  >dir | bash -c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1356">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="fc0fe-1357">Теперь Bash можно установить в системах с несколькими файлами подкачки (GH 538, 358).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1357">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="fc0fe-1358">Размер буфера сокета INET по умолчанию должен соответствовать установке Ubuntu по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1358">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="fc0fe-1359">Системные вызовы xattr согласованы с listxattr.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1359">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="fc0fe-1360">SIOCGIFCONF возвращает только интерфейсы с допустимым IPv4-адресом.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1360">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="fc0fe-1361">Исправлено действие по умолчанию для сигнала при внедрении с помощью ptrace.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1361">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="fc0fe-1362">Реализован файл /proc/sys/vm/min_free_kbytes.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1362">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="fc0fe-1363">Использование значений реестра для контекста компьютера при восстановлении контекста в sigreturn.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1363">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="fc0fe-1364">Это устраняет проблему, из-за которой у некоторых пользователей java и javac переставали отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1364">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="fc0fe-1365">Реализован файл /proc/sys/kernel/hostname.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1365">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="fc0fe-1366">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1366">Syscall Support</span></span>
<span data-ttu-id="fc0fe-1367">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1367">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="fc0fe-1368">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1368">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="fc0fe-1369">Сборка 14388 для юбилейного обновления Windows 10</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1369">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="fc0fe-1370">Общие сведения о сборке Windows 14388 доступны в [блоге о Windows](https://aka.ms/14388wip).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1370">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="fc0fe-1371">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1371">Fixed</span></span>
- <span data-ttu-id="fc0fe-1372">Исправления для подготовки к выпуску юбилейного обновления Windows 10 2-го августа.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1372">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="fc0fe-1373">Дополнительные сведения о компоненте WSL в юбилейном обновлении можно найти на нашем [блоге](https://blogs.msdn.microsoft.com/wsl/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1373">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="fc0fe-1374">Сборка 14376</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1374">Build 14376</span></span>
<span data-ttu-id="fc0fe-1375">Общие сведения о сборке Windows 14376 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1375">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="fc0fe-1376">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1376">Fixed</span></span>
- <span data-ttu-id="fc0fe-1377">Удалены некоторые экземпляры, в которых функция apt-get переставала отвечать на запросы (GH 493).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1377">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="fc0fe-1378">Исправлена проблема, из-за которой неправильно обрабатывались пустые подключения.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1378">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="fc0fe-1379">Исправлена проблема, из-за которой неправильно подключались диски ramdisk.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1379">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="fc0fe-1380">Изменена процедура принятия сокетов UNIX для поддержки флагов (частично GH 451).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1380">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="fc0fe-1381">Исправлена распространенная проблема с сетью, вызывавшая ошибку "синий экран".</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1381">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="fc0fe-1382">Устранена ошибка "синий экран" при доступе к /proc/[pid]/task (GH 523).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1382">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="fc0fe-1383">Исправлена высокая загрузка ЦП для некоторых сценариев использования pty (GH 488, 504).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1383">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="fc0fe-1384">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1384">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="fc0fe-1385">Сборка 14371</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1385">Build 14371</span></span>
<span data-ttu-id="fc0fe-1386">Общие сведения о сборке Windows 14371 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1386">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="fc0fe-1387">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1387">Fixed</span></span>
- <span data-ttu-id="fc0fe-1388">Исправлено состязание за синхронизацию SIGCHLD и wait() при использовании ptrace.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1388">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="fc0fe-1389">Исправлена обработка путей, которые завершаются косой чертой "/" (GH 432).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1389">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="fc0fe-1390">Устранен сбой при переименовании или отмене связи из-за открытых дескрипторов дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1390">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="fc0fe-1391">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1391">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="fc0fe-1392">Сборка 14366</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1392">Build 14366</span></span>
<span data-ttu-id="fc0fe-1393">Общие сведения о сборке Windows 14366 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1393">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="fc0fe-1394">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1394">Fixed</span></span>
- <span data-ttu-id="fc0fe-1395">Исправлено создание файла с помощью символических ссылок.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1395">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="fc0fe-1396">Добавлена функция listxattr для Python (GH 385).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1396">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="fc0fe-1397">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1397">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="fc0fe-1398">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1398">Syscall Support</span></span>
-   <span data-ttu-id="fc0fe-1399">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1399">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="fc0fe-1400">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1400">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="fc0fe-1401">Сборка 14361</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1401">Build 14361</span></span>
<span data-ttu-id="fc0fe-1402">Общие сведения о сборке Windows 14361 доступны в [блоге о Windows](https://aka.ms/wip14361).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1402">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="fc0fe-1403">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1403">Fixed</span></span>
- <span data-ttu-id="fc0fe-1404">Теперь в DrvFs учитывается регистр при выполнении в Bash для Ubuntu в Windows.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1404">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="fc0fe-1405">Пользователи могут хранить на дисках в /mnt/c и файл case.txt, и файл CASE.TXT.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1405">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="fc0fe-1406">Учет регистра поддерживается только в Bash для Ubuntu в Windows.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1406">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="fc0fe-1407">За пределами Bash NTFS будет отображать сведения о файлах правильно, но при взаимодействии с этими файлами из Windows может наблюдаться непредвиденное поведение.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1407">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="fc0fe-1408">Корень каждого тома (т. е. /mnt/c) не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1408">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="fc0fe-1409">Дополнительные сведения об обработке этих файлов в Windows можно найти [здесь](https://support.microsoft.com/en-us/kb/100625).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1409">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="fc0fe-1410">Значительно улучшена поддержка pty и tty.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1410">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="fc0fe-1411">Теперь поддерживаются такие приложения, как tmux (GH 40).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1411">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="fc0fe-1412">Исправлена проблема с установкой, из-за которой учетные записи пользователей создавались не всегда.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1412">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="fc0fe-1413">Оптимизирована структура аргументов командной строки, которая позволяет получить очень длинный список аргументов.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1413">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="fc0fe-1414">(GH 153)</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1414">(GH #153)</span></span>
- <span data-ttu-id="fc0fe-1415">Теперь можно выполнять операции delete и chmod с файлами только для чтения в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1415">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="fc0fe-1416">Исправлены некоторые экземпляры, в которых терминал при отключении переставал отвечать на запросы (GH 43).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1416">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="fc0fe-1417">Теперь на устройствах tty работает chmod и chown.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1417">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="fc0fe-1418">Разрешено подключение к 0.0.0.0 и :: как localhost (GH 388).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1418">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="fc0fe-1419">Теперь sendmsg и recvmsg обрабатывают векторы ввода-вывода длиной больше 1 (частично GH 376).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1419">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="fc0fe-1420">Теперь пользователи могут отказаться от автоматически создаваемого файла hosts (GH 398).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1420">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="fc0fe-1421">Автоматическое сопоставление языкового стандарта Linux с языковым стандартом NT во время установки (GH 11).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1421">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="fc0fe-1422">Добавлен файл /proc/sys/vm/swappiness (GH #306).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1422">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="fc0fe-1423">Теперь strace завершается правильно.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1423">strace now exits correctly</span></span>
- <span data-ttu-id="fc0fe-1424">Разрешено повторное открытие каналов через /proc/self/fd (GH 222).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1424">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="fc0fe-1425">Скрытие каталогов в %LOCALAPPDATA%\lxss из DrvFs (GH 270).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1425">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="fc0fe-1426">Улучшена обработка bash.exe ~.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1426">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="fc0fe-1427">Теперь поддерживаются такие команды, как "bash ~ -c ls" (GH 467).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1427">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="fc0fe-1428">Сокеты теперь уведомляют epoll о доступе на чтение во время завершения (GH 271).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1428">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="fc0fe-1429">Команда lxrun /uninstall лучше удаляет файлы и папки.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1429">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="fc0fe-1430">Исправлена команда ps -f (GH 246).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1430">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="fc0fe-1431">Улучшена поддержка приложений x11, таких как xEmacs (GH 481).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1431">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="fc0fe-1432">Обновлен начальный размер стека потока в соответствии с параметром Ubuntu по умолчанию. Теперь при системном вызове get_rlimit размер отображается правильно (GH 172, 258).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1432">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="fc0fe-1433">Улучшено отображение имен образов процессов Pico (например, для аудита).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1433">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="fc0fe-1434">Реализован файл /proc/mountinfo для команды df.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1434">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="fc0fe-1435">Исправлен код ошибки символической ссылки для дочернего имени.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1435">Fixed symlink error code for child name .</span></span> <span data-ttu-id="fc0fe-1436">И еще:</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1436">and ..</span></span>
- <span data-ttu-id="fc0fe-1437">Дополнительные улучшения исправлений ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1437">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="fc0fe-1438">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1438">Syscall Support</span></span>
<span data-ttu-id="fc0fe-1439">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1439">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="fc0fe-1440">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1440">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="fc0fe-1441">Сборка 14352</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1441">Build 14352</span></span>
<span data-ttu-id="fc0fe-1442">Общие сведения о сборке Windows 14352 доступны в [блоге о Windows](https://aka.ms/wip14352).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1442">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-1443">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1443">Fixed</span></span>
- <span data-ttu-id="fc0fe-1444">Исправлена проблема, из-за которой большие файлы скачивались и создавались неправильно.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1444">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="fc0fe-1445">Это должно позволить использовать npm и реализовать другие сценарии (GH 3, GH 313).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1445">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="fc0fe-1446">Удалены некоторые экземпляры, в которых сокеты переставали отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1446">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="fc0fe-1447">Исправлены некоторые ошибки ptrace.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1447">Corrected some ptrace errors</span></span>
- <span data-ttu-id="fc0fe-1448">Исправлена проблема с WSL, и теперь можно использовать имена файлов длиннее 255 знаков.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1448">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="fc0fe-1449">Улучшена поддержка знаков языков, отличных от английского.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1449">Improved support for non-English characters</span></span>
- <span data-ttu-id="fc0fe-1450">Добавление данных о текущем часовом поясе Windows и назначение его используемым по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1450">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="fc0fe-1451">Уникальный идентификатор устройства для каждой точки подключения (исправление JRE — GH 49).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1451">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="fc0fe-1452">Устранена ошибка из-за путей, содержащих "."</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1452">Correct issue with paths containing “.”</span></span> <span data-ttu-id="fc0fe-1453">и ".."</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1453">and “..”</span></span>
- <span data-ttu-id="fc0fe-1454">Добавлена поддержка FIFO (GH 71).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1454">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="fc0fe-1455">Обновлен формат resolv.conf в соответствии с собственным форматом Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1455">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="fc0fe-1456">Некоторая очистка procfs.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1456">Some procfs cleanup</span></span>
- <span data-ttu-id="fc0fe-1457">Включена проверка связи для консолей администратора (GH 18).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1457">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="fc0fe-1458">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1458">Syscall Support</span></span>
<span data-ttu-id="fc0fe-1459">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1459">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="fc0fe-1460">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1460">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="fc0fe-1461">Сборка 14342</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1461">Build 14342</span></span>
<span data-ttu-id="fc0fe-1462">Общие сведения о сборке Windows 14342 доступны в [блоге о Windows](https://aka.ms/wip14342).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1462">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="fc0fe-1463">Сведения о VolFs и DriveFs можно найти в [блоге о WSL](https://blogs.msdn.microsoft.com/wsl).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1463">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="fc0fe-1464">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1464">Fixed</span></span>
- <span data-ttu-id="fc0fe-1465">Исправлена проблема с установкой, возникавшая, когда в имени пользователя Windows присутствовали знаки Юникода.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1465">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="fc0fe-1466">Теперь обходное решение для обновления apt-get с помощью udev, приведенное в разделе часто задаваемых вопросов, предоставляется по умолчанию при первом запуске.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1466">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="fc0fe-1467">Включены символические ссылки в каталогах DriveFs (/mnt/<drive>).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1467">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="fc0fe-1468">Теперь работают символические ссылки между DriveFs и VolFs.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1468">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="fc0fe-1469">Устранена проблема с анализом путей верхнего уровня. Теперь ls .// будет работать должным образом.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1469">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="fc0fe-1470">Теперь работает установка npm в DriveFs и параметры -g.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1470">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="fc0fe-1471">Исправлена проблема, препятствующая запуску сервера PHP.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1471">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="fc0fe-1472">Обновлены значения среды по умолчанию, такие как $PATH, чтобы они больше соответствовали собственным переменным Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1472">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="fc0fe-1473">Добавлена еженедельная задача обслуживания в Windows для обновления кэша пакетов apt.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1473">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="fc0fe-1474">Исправлена проблема с проверкой заголовков ELF. Теперь WSL поддерживает все параметры Melkor.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1474">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="fc0fe-1475">Оболочка Zsh работает.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1475">Zsh shell is functional</span></span>
- <span data-ttu-id="fc0fe-1476">Теперь поддерживаются предварительно скомпилированные двоичные файлы Go.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1476">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="fc0fe-1477">Теперь запросы при первом запуске bash.exe локализованы правильно.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1477">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="fc0fe-1478">Теперь /proc/meminfo возвращает правильные сведения.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1478">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="fc0fe-1479">Сокеты теперь поддерживаются в VFS.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1479">Sockets now supported in VFS</span></span>
- <span data-ttu-id="fc0fe-1480">Теперь /dev подключен как tempfs.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1480">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="fc0fe-1481">FIFO теперь поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1481">Fifo now supported</span></span>
- <span data-ttu-id="fc0fe-1482">Многоядерные системы теперь правильно отображаются в /proc/cpuinfo.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1482">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="fc0fe-1483">Дополнительные улучшения и сообщения об ошибках при скачивании во время первого запуска.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1483">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="fc0fe-1484">Усовершенствования и исправления системных вызовов.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1484">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="fc0fe-1485">Список поддерживаемых системных вызовов приведен ниже.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1485">Supported syscall list below.</span></span>
- <span data-ttu-id="fc0fe-1486">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1486">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="fc0fe-1487">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1487">Known Issues</span></span>
- <span data-ttu-id="fc0fe-1488">Неправильное разрешение ".."</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1488">Not resolving ‘..’</span></span> <span data-ttu-id="fc0fe-1489">в DriveFs в некоторых случаях.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1489">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="fc0fe-1490">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1490">Syscall Support</span></span>
<span data-ttu-id="fc0fe-1491">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1491">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="fc0fe-1492">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1492">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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

## <a name="build-14332"></a><span data-ttu-id="fc0fe-1493">Сборка 14332</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1493">Build 14332</span></span>

<span data-ttu-id="fc0fe-1494">Общие сведения о сборке Windows 14332 доступны в [блоге о Windows](https://aka.ms/wip14332).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1494">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="fc0fe-1495">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1495">Fixed</span></span>
- <span data-ttu-id="fc0fe-1496">Улучшенное создание resolv.conf, включая определение приоритета записей DNS.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1496">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="fc0fe-1497">Проблема с перемещением файлов и каталогов между дисками в /mnt и прочими дисками.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1497">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="fc0fe-1498">Теперь можно создавать TAR-файлы с помощью символических ссылок.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1498">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="fc0fe-1499">Добавлен каталог /run/lock по умолчанию, создаваемый при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1499">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="fc0fe-1500">Обновлен файл /dev/null для возврата правильных сведений stat.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1500">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="fc0fe-1501">Дополнительные ошибки при скачивании во время первого запуска.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1501">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="fc0fe-1502">Усовершенствования и исправления системных вызовов.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1502">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="fc0fe-1503">Список поддерживаемых системных вызовов приведен ниже.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1503">Supported syscall list below.</span></span>
- <span data-ttu-id="fc0fe-1504">Дополнительные улучшения исправлений ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1504">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="fc0fe-1505">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1505">Syscall Support</span></span>
<span data-ttu-id="fc0fe-1506">Ниже приведен новый системный вызов, реализованный в WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1506">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="fc0fe-1507">Системный вызов в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут поддерживаться не все параметры.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1507">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="fc0fe-1508">Сборка 14328</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1508">Build 14328</span></span>

<span data-ttu-id="fc0fe-1509">Общие сведения о сборке Windows 14332 доступны в [блоге о Windows](https://aka.ms/wip14328).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1509">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="fc0fe-1510">Новые возможности</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1510">New Features</span></span>
* <span data-ttu-id="fc0fe-1511">Теперь поддерживаются пользователи Linux.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1511">Now support Linux users.</span></span>  <span data-ttu-id="fc0fe-1512">При установке Bash для Ubuntu в Windows будет предложено создать пользователя Linux.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1512">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="fc0fe-1513">Дополнительные сведения: https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1513">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="fc0fe-1514">В качестве имени узла теперь указывается имя компьютера Windows, а не @localhost.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1514">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="fc0fe-1515">Дополнительные сведения о сборке 14328: https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1515">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="fc0fe-1516">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1516">Fixed</span></span>
* <span data-ttu-id="fc0fe-1517">Улучшения символьных ссылок для файлов вне каталога /mnt/<drive>.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1517">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="fc0fe-1518">Теперь установка npm работает.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1518">npm install now works</span></span>
    * <span data-ttu-id="fc0fe-1519">Теперь можно установить JDK или JRE с помощью [этих инструкций](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1519">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="fc0fe-1520">Известная ошибка: символические ссылки не работали для подключений Windows.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1520">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="fc0fe-1521">Эта функция будет доступна в последующей сборке.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1521">Functionality will be available in a later build</span></span>
* <span data-ttu-id="fc0fe-1522">Теперь отображаются top и htop.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1522">top and htop now display</span></span>
* <span data-ttu-id="fc0fe-1523">Дополнительные сообщения об ошибке для некоторых сбоев при установке.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1523">Additional error messages for some install failures</span></span>
* <span data-ttu-id="fc0fe-1524">Усовершенствования и исправления системных вызовов.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1524">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="fc0fe-1525">Список поддерживаемых системных вызовов приведен ниже.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1525">Supported syscall list below.</span></span>
* <span data-ttu-id="fc0fe-1526">Дополнительные улучшения исправлений ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1526">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="fc0fe-1527">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1527">Syscall Support</span></span>
<span data-ttu-id="fc0fe-1528">Ниже приведен список системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1528">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="fc0fe-1529">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="fc0fe-1529">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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
