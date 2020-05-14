---
title: Разрешения файлов
description: Общие сведения об определении разрешений файлов в Windows с помощью WSL
keywords: bashonwindows, bash, wsl, wsl2, windows, подсистема windows для linux, windowssubsystem, ubuntu, debian, suse, windows 10, файл, разрешения
ms.date: 01/14/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.localizationpriority: high
ms.openlocfilehash: 66cded36fb7182a54a05e7794250808665bd4cf1
ms.sourcegitcommit: 3fb40fd65b34a5eb26b213a0df6a3b2746b7a9b4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2020
ms.locfileid: "83235853"
---
# <a name="file-permissions-for-wsl"></a><span data-ttu-id="dfc78-104">Разрешения файлов для WSL</span><span class="sxs-lookup"><span data-stu-id="dfc78-104">File Permissions for WSL</span></span>

<span data-ttu-id="dfc78-105">На этой странице представлены сведения об интерпретации разрешений файлов Linux в подсистеме Windows для Linux, особенно при получении доступа к ресурсам в файловой системе NT под управлением Windows.</span><span class="sxs-lookup"><span data-stu-id="dfc78-105">This page details how Linux file permissions are interpreted across the Windows Subsystem for Linux, especially when accessing resources inside of Windows on the NT file system.</span></span> <span data-ttu-id="dfc78-106">В этой документации предполагается, что вы имеете базовое представление о [структуре разрешений файловой системы Linux](https://wiki.archlinux.org/index.php/File_permissions_and_attributes) и [командах umask](https://en.wikipedia.org/wiki/Umask).</span><span class="sxs-lookup"><span data-stu-id="dfc78-106">This documentation assumes a basic understanding of the [Linux file system permissions structure](https://wiki.archlinux.org/index.php/File_permissions_and_attributes) and the [umask command](https://en.wikipedia.org/wiki/Umask).</span></span>

<span data-ttu-id="dfc78-107">При доступе к файлам Windows из WSL разрешения файлов вычисляются на основе разрешений Windows, либо считываются из метаданных, которые были добавлены в файл с помощью WSL.</span><span class="sxs-lookup"><span data-stu-id="dfc78-107">When accessing Windows files from WSL the file permissions are either calculated from Windows permissions, or are read from metadata that has been added to the file by WSL.</span></span> <span data-ttu-id="dfc78-108">По умолчанию эти метаданные не включены.</span><span class="sxs-lookup"><span data-stu-id="dfc78-108">This metadata is not enabled by default.</span></span>

## <a name="wsl-metadata-on-windows-files"></a><span data-ttu-id="dfc78-109">Метаданные WSL в файлах Windows</span><span class="sxs-lookup"><span data-stu-id="dfc78-109">WSL metadata on Windows files</span></span>

<span data-ttu-id="dfc78-110">Если метаданные включены в качестве параметра подключения в WSL, вы можете добавить и интерпретировать расширенные атрибуты в файлах Windows NT, чтобы предоставить разрешения файловой системы Linux.</span><span class="sxs-lookup"><span data-stu-id="dfc78-110">When metadata is enabled as a mount option in WSL, extended attributes on Windows NT files can be added and interpreted to supply Linux file system permissions.</span></span>

<span data-ttu-id="dfc78-111">WSL может добавлять четыре расширенных атрибута NTFS:</span><span class="sxs-lookup"><span data-stu-id="dfc78-111">WSL can add four NTFS extended attributes:</span></span>

| <span data-ttu-id="dfc78-112">Имя атрибута</span><span class="sxs-lookup"><span data-stu-id="dfc78-112">Attribute Name</span></span> | <span data-ttu-id="dfc78-113">Описание</span><span class="sxs-lookup"><span data-stu-id="dfc78-113">Description</span></span> |
| --- | --- |
| <span data-ttu-id="dfc78-114">$LXUID</span><span class="sxs-lookup"><span data-stu-id="dfc78-114">$LXUID</span></span> | <span data-ttu-id="dfc78-115">Идентификатор пользователя владельца</span><span class="sxs-lookup"><span data-stu-id="dfc78-115">User Owner ID</span></span> |
| <span data-ttu-id="dfc78-116">$LXGID</span><span class="sxs-lookup"><span data-stu-id="dfc78-116">$LXGID</span></span> | <span data-ttu-id="dfc78-117">Идентификатор владельца группы</span><span class="sxs-lookup"><span data-stu-id="dfc78-117">Group Owner ID</span></span> |
| <span data-ttu-id="dfc78-118">$LXMOD</span><span class="sxs-lookup"><span data-stu-id="dfc78-118">$LXMOD</span></span> | <span data-ttu-id="dfc78-119">Файловый режим (восьмеричная система и типы разрешений файловой системы, например: 0777)</span><span class="sxs-lookup"><span data-stu-id="dfc78-119">File mode (File systems permission octals and type, e.g: 0777)</span></span> |
| <span data-ttu-id="dfc78-120">$LXDEV</span><span class="sxs-lookup"><span data-stu-id="dfc78-120">$LXDEV</span></span> | <span data-ttu-id="dfc78-121">Устройство (если это файл устройства)</span><span class="sxs-lookup"><span data-stu-id="dfc78-121">Device, if it is a device file</span></span> |

<span data-ttu-id="dfc78-122">Кроме того, любой файл, который не является обычным файлом или каталогом (например, символические ссылки, файлы FIFO, блочные устройства, сокеты Unix и символьные устройства) также имеет точку повторного анализа [NTFS](https://docs.microsoft.com/windows/win32/fileio/reparse-points).</span><span class="sxs-lookup"><span data-stu-id="dfc78-122">Additionally, any file that is not a regular file or directory (e.g: symlinks, FIFOs, block devices, unix sockets, and character devices) also have an NTFS [reparse point](https://docs.microsoft.com/windows/win32/fileio/reparse-points).</span></span> <span data-ttu-id="dfc78-123">Это позволяет быстрее определить тип файла в определенном каталоге, не запрашивая его расширенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="dfc78-123">This makes it much faster to determine the kind of file in a given directory without having to query its extended attributes.</span></span>

## <a name="file-access-scenarios"></a><span data-ttu-id="dfc78-124">Сценарии доступа к файлам</span><span class="sxs-lookup"><span data-stu-id="dfc78-124">File Access Scenarios</span></span>

<span data-ttu-id="dfc78-125">Ниже приведено описание того, как определяются разрешения при получении доступа к файлам с помощью подсистемы Windows для Linux различными способами.</span><span class="sxs-lookup"><span data-stu-id="dfc78-125">Below is a description of how permissions are determined when accessing files in different ways using the Windows Subsystem for Linux.</span></span>

### <a name="accessing-files-in-the-windows-drive-file-system-drvfs-from-linux"></a><span data-ttu-id="dfc78-126">Получение доступа к файлам в файловой системе диска Windows (DrvFS) из Linux</span><span class="sxs-lookup"><span data-stu-id="dfc78-126">Accessing Files in the Windows drive file system (DrvFS) from Linux</span></span>

<span data-ttu-id="dfc78-127">Эти сценарии возникают при получении доступа к файлам Windows из WSL, скорее всего с помощью `/mnt/c`.</span><span class="sxs-lookup"><span data-stu-id="dfc78-127">These scenarios occur when you are accessing your Windows files from WSL, most likely via `/mnt/c`.</span></span>

#### <a name="reading-file-permissions-from-an-existing-windows-file"></a><span data-ttu-id="dfc78-128">Чтение разрешений файлов из существующего файла Windows</span><span class="sxs-lookup"><span data-stu-id="dfc78-128">Reading file permissions from an existing Windows file</span></span>

<span data-ttu-id="dfc78-129">Результат будет зависеть от того, содержит ли файл уже существующие метаданные.</span><span class="sxs-lookup"><span data-stu-id="dfc78-129">The result depends on if the file already has existing metadata.</span></span>

##### <a name="drvfs-file-does-not-have-metadata-default"></a><span data-ttu-id="dfc78-130">Файл DrvFS не имеет метаданных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dfc78-130">DrvFS file does not have metadata (default)</span></span>

<span data-ttu-id="dfc78-131">Если файл не имеет связанных метаданных, мы преобразовываем действующие разрешения пользователя Windows в биты чтения, записи или выполнения и назначаем их этому файлу в качестве того же значения для пользователя, группы и других элементов.</span><span class="sxs-lookup"><span data-stu-id="dfc78-131">If the file has no metadata associated with it then we translate the effective permissions of the Windows user to read/write/execute bits and set them to the this as the same value for user, group, and other.</span></span> <span data-ttu-id="dfc78-132">Например, если учетная запись пользователя Windows имеет доступ на чтение и выполнение, но не имеет доступа на запись в файл, для пользователя, группы и других элементов она будет отображаться как `r-x`.</span><span class="sxs-lookup"><span data-stu-id="dfc78-132">For example, if your Windows user account has read and execute access but not write access to the file then this will be shown as `r-x` for user, group and other.</span></span> <span data-ttu-id="dfc78-133">Если для файла в Windows задан атрибут "только для чтения", доступ на запись в Linux не предоставляется.</span><span class="sxs-lookup"><span data-stu-id="dfc78-133">If the file has the 'Read Only' attribute set in Windows then we do not grant write access in Linux.</span></span>

##### <a name="the-file-has-metadata"></a><span data-ttu-id="dfc78-134">Файл содержит метаданные</span><span class="sxs-lookup"><span data-stu-id="dfc78-134">The file has metadata</span></span>

<span data-ttu-id="dfc78-135">Если файл содержит метаданные, мы будем использовать их значения вместо преобразованных действующих разрешений пользователя Windows.</span><span class="sxs-lookup"><span data-stu-id="dfc78-135">If the file has metadata present, we simply use those metadata values instead of translating effective permissions of the Windows user.</span></span>

#### <a name="changing-file-permissions-on-an-existing-windows-file-using-chmod"></a><span data-ttu-id="dfc78-136">Изменение разрешений файла в существующем файле Windows с помощью команды chmod</span><span class="sxs-lookup"><span data-stu-id="dfc78-136">Changing file permissions on an existing Windows file using chmod</span></span>

<span data-ttu-id="dfc78-137">Результат будет зависеть от того, содержит ли файл уже существующие метаданные.</span><span class="sxs-lookup"><span data-stu-id="dfc78-137">The result depends on if the file already has existing metadata.</span></span>

##### <a name="chmod-file-does-not-have-metadata-default"></a><span data-ttu-id="dfc78-138">Файл chmod не имеет метаданных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dfc78-138">chmod file does not have metadata (default)</span></span>

<span data-ttu-id="dfc78-139">Файл chmod может иметь только один эффект. Если вы удалите все атрибуты записи файла, в файле Windows будет задан атрибут "только для чтения", так как это то же поведение, что и в общей файловой системе Интернета (CIFS), которая является клиентом SMB в Linux.</span><span class="sxs-lookup"><span data-stu-id="dfc78-139">Chmod will only have one effect, if you remove all the write attributes of a file then the 'read only' attribute on the Windows file will be set, since this is the same behaviour as CIFS (Common Internet File System) which is the SMB (Server Message Block) client in Linux.</span></span>

##### <a name="chmod-file-has-metadata"></a><span data-ttu-id="dfc78-140">Файл chmod содержит метаданные</span><span class="sxs-lookup"><span data-stu-id="dfc78-140">chmod file has metadata</span></span>

<span data-ttu-id="dfc78-141">В зависимости от уже существующих метаданных файла, файл chmod будет изменен или будут добавлены метаданные.</span><span class="sxs-lookup"><span data-stu-id="dfc78-141">Chmod will change or add metadata depending on the file's already existing metadata.</span></span> 

<span data-ttu-id="dfc78-142">Помните, что вы не можете предоставить себе больше прав доступа, чем вы имели в Windows, даже если в метаданных указано, что это возможно.</span><span class="sxs-lookup"><span data-stu-id="dfc78-142">Please keep in mind that you cannot give yourself more access than what you have on Windows, even if the metadata says that is the case.</span></span> <span data-ttu-id="dfc78-143">Например, можно задать, чтобы в метаданных отображалось, что у вас есть разрешения на запись в файл с помощью `chmod 777`, но если вы попытаетесь получить доступ к этому файлу, запись будет невозможна.</span><span class="sxs-lookup"><span data-stu-id="dfc78-143">For example, you could set the metadata to display that you have write permissions to a file using `chmod 777`, but if you tried to access that file you would still not be able to write to it.</span></span> <span data-ttu-id="dfc78-144">Это происходит благодаря взаимодействию, так как любые команды чтения или записи в файлы Windows направляются через разрешения пользователя Windows.</span><span class="sxs-lookup"><span data-stu-id="dfc78-144">This is thanks to interopability, as any read or write commands to Windows files are routed through your Windows user permissions.</span></span>

#### <a name="creating-a-file-in-drivefs"></a><span data-ttu-id="dfc78-145">Создание файла в DriveFS</span><span class="sxs-lookup"><span data-stu-id="dfc78-145">Creating a file in DriveFS</span></span>

<span data-ttu-id="dfc78-146">Результат зависит от того, включены метаданные или нет.</span><span class="sxs-lookup"><span data-stu-id="dfc78-146">The result depends on if metadata is enabled.</span></span>

##### <a name="metadata-is-not-enabled-default"></a><span data-ttu-id="dfc78-147">Метаданные не включены (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dfc78-147">Metadata is not enabled (default)</span></span>

<span data-ttu-id="dfc78-148">Разрешения Windows для созданного файла будут такими же, как если бы вы создали файл в Windows без конкретного дескриптора безопасности. Он наследует родительские разрешения.</span><span class="sxs-lookup"><span data-stu-id="dfc78-148">The Windows permissions of the newly created file will be the same as if you created the file in Windows without a specific security descriptor, it will inherit the parent's permissions.</span></span>

##### <a name="metadata-is-enabled"></a><span data-ttu-id="dfc78-149">Метаданные включены</span><span class="sxs-lookup"><span data-stu-id="dfc78-149">Metadata is enabled</span></span>

<span data-ttu-id="dfc78-150">Биты разрешений файла задаются в соответствии с командой umask в Linux, и файл будет сохранен с метаданными.</span><span class="sxs-lookup"><span data-stu-id="dfc78-150">The file's permission bits are set to follow the Linux umask, and the file will be saved with metadata.</span></span>

#### <a name="which-linux-user-and-linux-group-owns-the-file"></a><span data-ttu-id="dfc78-151">Какому пользователю или группе Linux принадлежит файл?</span><span class="sxs-lookup"><span data-stu-id="dfc78-151">Which Linux user and Linux group owns the file?</span></span> 

<span data-ttu-id="dfc78-152">Результат будет зависеть от того, содержит ли файл уже существующие метаданные.</span><span class="sxs-lookup"><span data-stu-id="dfc78-152">The result depends on if the file already has existing metadata.</span></span>

##### <a name="user-file-does-not-have-metadata-default"></a><span data-ttu-id="dfc78-153">Файл пользователя не имеет метаданных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dfc78-153">User file does not have metadata (default)</span></span>

<span data-ttu-id="dfc78-154">В сценарии по умолчанию при автоподключении дисков Windows мы указываем, что идентификатору пользователя (UID) любого файла присваивается идентификатор пользователя WSL, а идентификатору группы (GID) — идентификатор главной группы пользователя WSL.</span><span class="sxs-lookup"><span data-stu-id="dfc78-154">In the default scenario, when automounting Windows drives, we specify that the user ID (UID) for any file is set to the user ID of your WSL user and the group ID (GID) is set to the principal group ID of your WSL user.</span></span>

##### <a name="user-file-has-metadata"></a><span data-ttu-id="dfc78-155">Файл пользователя содержит метаданные</span><span class="sxs-lookup"><span data-stu-id="dfc78-155">User file has metadata</span></span>

<span data-ttu-id="dfc78-156">Идентификаторы пользователя и группы, указанные в метаданных, применяются в качестве пользователя владельца и владельца группы файла.</span><span class="sxs-lookup"><span data-stu-id="dfc78-156">The UID and GID specified in the metadata is applied as the user owner and group owner of the file.</span></span>

### <a name="accessing-linux-files-from-windows-using-wsl"></a><span data-ttu-id="dfc78-157">Получение доступа к файлам Linux из Windows с помощью `\\wsl$`</span><span class="sxs-lookup"><span data-stu-id="dfc78-157">Accessing Linux files from Windows using `\\wsl$`</span></span>

<span data-ttu-id="dfc78-158">Для получения доступа к файлам Linux с помощью `\\wsl$` будет использоваться пользователь по умолчанию дистрибутива WSL.</span><span class="sxs-lookup"><span data-stu-id="dfc78-158">Accessing Linux files via `\\wsl$` will use the default user of your WSL distribution.</span></span> <span data-ttu-id="dfc78-159">Таким образом, все приложения Windows, обращающиеся к файлам Linux, будут иметь те же разрешения, что и пользователь по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dfc78-159">Therefore any Windows app accessing Linux files will have the same permissions as the default user.</span></span>

#### <a name="creating-a-new-file"></a><span data-ttu-id="dfc78-160">Создание поля</span><span class="sxs-lookup"><span data-stu-id="dfc78-160">Creating a new file</span></span>

<span data-ttu-id="dfc78-161">Параметр umask по умолчанию применяется при создании файла в дистрибутиве WSL из Windows.</span><span class="sxs-lookup"><span data-stu-id="dfc78-161">The default umask is applied when creating a new file inside of a WSL distribution from Windows.</span></span> <span data-ttu-id="dfc78-162">По умолчанию параметр umask имеет значение `022`. Или другими словами он позволяет использовать все разрешения, кроме разрешения на запись, в группах и других элементах.</span><span class="sxs-lookup"><span data-stu-id="dfc78-162">The default umask is `022`, or in other words it allows all permissions except write permissions to groups and others.</span></span> 

### <a name="accessing-files-in-the-linux-root-file-system-from-linux"></a><span data-ttu-id="dfc78-163">Доступ к файлам в корневой файловой системе Linux из Linux</span><span class="sxs-lookup"><span data-stu-id="dfc78-163">Accessing files in the Linux root file system from Linux</span></span>

<span data-ttu-id="dfc78-164">Во всех файлах, созданных, измененных или доступ к которым осуществлялся с помощью корневой файловой системы Linux, используются стандартные соглашения Linux. Например, к только что созданному файлу применяется команда umask.</span><span class="sxs-lookup"><span data-stu-id="dfc78-164">Any files created, modified, or accessed in the Linux root file system follow standard Linux conventions, such as applying the umask to a newly created file.</span></span>

## <a name="configuring-file-permissions"></a><span data-ttu-id="dfc78-165">Настройка разрешений файлов</span><span class="sxs-lookup"><span data-stu-id="dfc78-165">Configuring file permissions</span></span>

<span data-ttu-id="dfc78-166">Вы можете настроить разрешения файлов в дисках Windows с помощью параметров подключения в wsl.conf.</span><span class="sxs-lookup"><span data-stu-id="dfc78-166">You can configure your file permissions inside of your Windows drives using the mount options in wsl.conf.</span></span> <span data-ttu-id="dfc78-167">Параметры подключения позволяют задать маски разрешений `umask`, `dmask` и `fmask`.</span><span class="sxs-lookup"><span data-stu-id="dfc78-167">The mount options allow you to set `umask`, `dmask` and `fmask` permissions masks.</span></span> <span data-ttu-id="dfc78-168">`umask` применяется ко всем файлам, `dmask` — только к каталогам, а `fmask` — только к файлам.</span><span class="sxs-lookup"><span data-stu-id="dfc78-168">The `umask` is applied to all files, the `dmask` is applied just to directories and the `fmask` is applied just to files.</span></span> <span data-ttu-id="dfc78-169">Затем эти маски разрешений подвергаются логической операции ИЛИ во время применения к файлам, например: Если у вас есть значение `umask` для `023` и значение `fmask` для `022`, то полученная маска разрешений для файлов будет `023`.</span><span class="sxs-lookup"><span data-stu-id="dfc78-169">These permission masks are then put through a logical OR operation when being applied to files, e.g: If you have a `umask` value of `023` and an `fmask` value of `022` then the resulting permissions mask for files will be `023`.</span></span>

<span data-ttu-id="dfc78-170">Дополнительные инструкции см. в разделе [Настройка параметров запуска с помощью wslconf](./wsl-config.md#configure-launch-settings-with-wslconf).</span><span class="sxs-lookup"><span data-stu-id="dfc78-170">Please see the [Configure launch settings with wslconf](./wsl-config.md#configure-launch-settings-with-wslconf) article for instructions on how to do this.</span></span>
