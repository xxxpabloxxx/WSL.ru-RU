---
title: Разрешения для файла
description: Общие сведения о том, как WSL определяет разрешения для файлов в Windows
keywords: Башонвиндовс, bash, WSL, wsl2, Windows, подсистема Windows для Linux, виндовссубсистем, Ubuntu, Debian, SUSE, Windows 10, файл, разрешения
ms.date: 01/14/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 4566fc86cf14df986bde80cf3a6cfb9267b23308
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520863"
---
# <a name="file-permissions-for-wsl"></a><span data-ttu-id="2352a-104">Разрешения файла для WSL</span><span class="sxs-lookup"><span data-stu-id="2352a-104">File Permissions for WSL</span></span>

<span data-ttu-id="2352a-105">На этой странице подробно описана интерпретация разрешений файлов Linux в подсистеме Windows для Linux, особенно при доступе к ресурсам в Windows в файловой системе NT.</span><span class="sxs-lookup"><span data-stu-id="2352a-105">This page details how Linux file permissions are interpreted across the Windows Subsystem for Linux, especially when accessing resources inside of Windows on the NT file system.</span></span> <span data-ttu-id="2352a-106">В этой документации предполагается, что основные сведения о [структуре разрешений файловой системы Linux](https://wiki.archlinux.org/index.php/File_permissions_and_attributes)</span><span class="sxs-lookup"><span data-stu-id="2352a-106">This documentation assumes a basic understanding of the [Linux file system permissions structure](https://wiki.archlinux.org/index.php/File_permissions_and_attributes)</span></span> <!--TODO: Double check that it's okay to add these links--> <span data-ttu-id="2352a-107">и [команда umask](https://en.wikipedia.org/wiki/Umask).</span><span class="sxs-lookup"><span data-stu-id="2352a-107">and the [umask command](https://en.wikipedia.org/wiki/Umask).</span></span>

<span data-ttu-id="2352a-108">При доступе к файлам Windows из WSL разрешения на файлы либо рассчитываются из разрешений Windows, либо считываются из метаданных, которые были добавлены в файл WSL.</span><span class="sxs-lookup"><span data-stu-id="2352a-108">When accessing Windows files from WSL the file permissions are either calculated from Windows permissions, or are read from metadata that has been added to the file by WSL.</span></span> <span data-ttu-id="2352a-109">По умолчанию эти метаданные не включены.</span><span class="sxs-lookup"><span data-stu-id="2352a-109">This metadata is not enabled by default.</span></span> 

## <a name="wsl-metadata-on-windows-files"></a><span data-ttu-id="2352a-110">Метаданные WSL в файлах Windows</span><span class="sxs-lookup"><span data-stu-id="2352a-110">WSL metadata on Windows files</span></span>

<span data-ttu-id="2352a-111">Если метаданные включены в качестве параметра подключения в WSL, можно добавить и интерпретировать расширенные атрибуты в файлах Windows NT, чтобы предоставить разрешения файловой системы Linux.</span><span class="sxs-lookup"><span data-stu-id="2352a-111">When metadata is enabled as a mount option in WSL, extended attributes on Windows NT files can be added and interpreted to supply Linux file system permissions.</span></span> 

<span data-ttu-id="2352a-112">WSL может добавлять четыре расширенных атрибута NTFS:</span><span class="sxs-lookup"><span data-stu-id="2352a-112">WSL can add four NTFS extended attributes:</span></span>

| <span data-ttu-id="2352a-113">Имя атрибута</span><span class="sxs-lookup"><span data-stu-id="2352a-113">Attribute Name</span></span> | <span data-ttu-id="2352a-114">Описание</span><span class="sxs-lookup"><span data-stu-id="2352a-114">Description</span></span> |
| --- | --- |
| <span data-ttu-id="2352a-115">$LXUID</span><span class="sxs-lookup"><span data-stu-id="2352a-115">$LXUID</span></span> | <span data-ttu-id="2352a-116">Идентификатор владельца пользователя</span><span class="sxs-lookup"><span data-stu-id="2352a-116">User Owner ID</span></span> |
| <span data-ttu-id="2352a-117">$LXGID</span><span class="sxs-lookup"><span data-stu-id="2352a-117">$LXGID</span></span> | <span data-ttu-id="2352a-118">Идентификатор владельца группы</span><span class="sxs-lookup"><span data-stu-id="2352a-118">Group Owner ID</span></span> |
| <span data-ttu-id="2352a-119">$LXMOD</span><span class="sxs-lookup"><span data-stu-id="2352a-119">$LXMOD</span></span> | <span data-ttu-id="2352a-120">Файловый режим (восьмеричные разрешения и тип разрешений файловой системы, например: 0777)</span><span class="sxs-lookup"><span data-stu-id="2352a-120">File mode (File systems permission octals and type, e.g: 0777)</span></span> |
| <span data-ttu-id="2352a-121">$LXDEV</span><span class="sxs-lookup"><span data-stu-id="2352a-121">$LXDEV</span></span> | <span data-ttu-id="2352a-122">Устройство, если это файл устройства</span><span class="sxs-lookup"><span data-stu-id="2352a-122">Device, if it is a device file</span></span> |

<span data-ttu-id="2352a-123">Кроме того, любой файл, который не является обычным файлом или каталогом (например, символических ссылок, ФИФО, блочные устройства, сокеты Unix и символьные устройства), также имеет [точку повторного анализа](https://docs.microsoft.com/en-us/windows/win32/fileio/reparse-points)NTFS.</span><span class="sxs-lookup"><span data-stu-id="2352a-123">Additionally, any file that is not a regular file or directory (e.g: symlinks, FIFOs, block devices, unix sockets, and character devices) also have an NTFS [reparse point](https://docs.microsoft.com/en-us/windows/win32/fileio/reparse-points).</span></span> <span data-ttu-id="2352a-124">Это значительно ускоряет определение типа файла в определенном каталоге без запроса его расширенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="2352a-124">This makes it much faster to determine the kind of file in a given directory without having to query its extended attributes.</span></span> 
<!-- TODO: For the blog include ONeDrive detail -->

## <a name="file-access-scenarios"></a><span data-ttu-id="2352a-125">Сценарии доступа к файлам</span><span class="sxs-lookup"><span data-stu-id="2352a-125">File Access Scenarios</span></span>

<span data-ttu-id="2352a-126">Ниже приведено описание того, как определяются разрешения при доступе к файлам различными способами с помощью подсистемы Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="2352a-126">Below is a description of how permissions are determined when accessing files in different ways using the Windows Subsystem for Linux.</span></span>

### <a name="accessing-files-in-the-windows-drive-file-system-drvfs-from-linux"></a><span data-ttu-id="2352a-127">Доступ к файлам в файловой системе Windows Drive (Дрвфс) из Linux</span><span class="sxs-lookup"><span data-stu-id="2352a-127">Accessing Files in the Windows drive file system (DrvFS) from Linux</span></span>

<span data-ttu-id="2352a-128">Эти сценарии возникают при доступе к файлам Windows из WSL, скорее всего, с помощью `/mnt/c`.</span><span class="sxs-lookup"><span data-stu-id="2352a-128">These scenarios occur when you are accessing your Windows files from WSL, most likely via `/mnt/c`.</span></span> 

#### <a name="reading-file-permissions-from-an-existing-windows-file"></a><span data-ttu-id="2352a-129">Чтение разрешений файла из существующего файла Windows</span><span class="sxs-lookup"><span data-stu-id="2352a-129">Reading file permissions from an existing Windows file</span></span>

<span data-ttu-id="2352a-130">Результат зависит от того, есть ли у файла уже существующие метаданные.</span><span class="sxs-lookup"><span data-stu-id="2352a-130">The result depends on if the file already has existing metadata.</span></span>

##### <a name="the-file-does-not-have-metadata-default"></a><span data-ttu-id="2352a-131">**Файл не имеет метаданных (по умолчанию)**</span><span class="sxs-lookup"><span data-stu-id="2352a-131">**The file does not have metadata (default)**</span></span>

<span data-ttu-id="2352a-132">Если с файлом не связаны метаданные, мы преобразуем действующие разрешения пользователя Windows на чтение, запись и выполнение BITS и присвоить этому файлу такое же значение для пользователя, группы и других.</span><span class="sxs-lookup"><span data-stu-id="2352a-132">If the file has no metadata associated with it then we translate the effective permissions of the Windows user to read/write/execute bits and set them to the this as the same value for user, group, and other.</span></span> <span data-ttu-id="2352a-133">Например, если учетная запись пользователя Windows имеет доступ на чтение и выполнение, но не имеет доступа на запись к файлу, то он будет отображаться как `r-x` для пользователя, группы и других.</span><span class="sxs-lookup"><span data-stu-id="2352a-133">For example, if your Windows user account has read and execute access but not write access to the file then this will be shown as `r-x` for user, group and other.</span></span> <span data-ttu-id="2352a-134">Если для файла в Windows установлен атрибут "только для чтения", доступ на запись в Linux не предоставляется.</span><span class="sxs-lookup"><span data-stu-id="2352a-134">If the file has the 'Read Only' attribute set in Windows then we do not grant write access in Linux.</span></span>

##### <a name="the-file-has-metadata"></a><span data-ttu-id="2352a-135">Файл содержит метаданные</span><span class="sxs-lookup"><span data-stu-id="2352a-135">The file has metadata</span></span>

<span data-ttu-id="2352a-136">Если в файле есть метаданные, мы просто используем эти значения метаданных вместо перевода действующих разрешений пользователя Windows.</span><span class="sxs-lookup"><span data-stu-id="2352a-136">If the file has metadata present, we simply use those metadata values instead of translating effective permissions of the Windows user.</span></span>

#### <a name="changing-file-permissions-on-an-existing-windows-file-using-chmod"></a><span data-ttu-id="2352a-137">Изменение разрешений для файла в существующем файле Windows с помощью команды chmod</span><span class="sxs-lookup"><span data-stu-id="2352a-137">Changing file permissions on an existing Windows file using chmod</span></span>

<span data-ttu-id="2352a-138">Результат зависит от того, есть ли у файла уже существующие метаданные.</span><span class="sxs-lookup"><span data-stu-id="2352a-138">The result depends on if the file already has existing metadata.</span></span>

##### <a name="the-file-does-not-have-metadata-default"></a><span data-ttu-id="2352a-139">**Файл не имеет метаданных (по умолчанию)**</span><span class="sxs-lookup"><span data-stu-id="2352a-139">**The file does not have metadata (default)**</span></span>

<span data-ttu-id="2352a-140">Chmod будет иметь только один результат. Если удалить все атрибуты записи файла, то будет установлен атрибут "только для чтения" в файле Windows, так как это то же поведение, что и CIFS (Общая файловая система Интернета), которая является клиентом SMB (серверный блок сообщений) в Linux.</span><span class="sxs-lookup"><span data-stu-id="2352a-140">Chmod will only have one effect, if you remove all the write attributes of a file then the 'read only' attribute on the Windows file will be set, since this is the same behaviour as CIFS (Common Internet File System) which is the SMB (Server Message Block) client in Linux.</span></span>

##### <a name="the-file-has-metadata"></a><span data-ttu-id="2352a-141">Файл содержит метаданные</span><span class="sxs-lookup"><span data-stu-id="2352a-141">The file has metadata</span></span>

<span data-ttu-id="2352a-142">Параметр chmod изменит или добавит метаданные в зависимости от уже существующих метаданных файла.</span><span class="sxs-lookup"><span data-stu-id="2352a-142">Chmod will change or add metadata depending on the file's already existing metadata.</span></span> 

<span data-ttu-id="2352a-143">Имейте в виду, что вы не можете предоставить вам больше доступа, чем у вас в Windows, даже если в метаданных указано, что это так.</span><span class="sxs-lookup"><span data-stu-id="2352a-143">Please keep in mind that you cannot give yourself more access than what you have on Windows, even if the metadata says that is the case.</span></span> <span data-ttu-id="2352a-144">Например, можно задать для метаданных отображение разрешений на запись в файл с помощью `chmod 777`, но если вы попытались получить доступ к этому файлу, запись в него будет невозможна.</span><span class="sxs-lookup"><span data-stu-id="2352a-144">For example, you could set the metadata to display that you have write permissions to a file using `chmod 777`, but if you tried to access that file you would still not be able to write to it.</span></span> <span data-ttu-id="2352a-145">Это спасибо за взаимодействие, так как любые команды чтения или записи для файлов Windows направляются через разрешения пользователя Windows.</span><span class="sxs-lookup"><span data-stu-id="2352a-145">This is thanks to interopability, as any read or write commands to Windows files are routed through your Windows user permissions.</span></span>

#### <a name="creating-a-file-in-drivefs"></a><span data-ttu-id="2352a-146">Создание файла в Дривефс</span><span class="sxs-lookup"><span data-stu-id="2352a-146">Creating a file in DriveFS</span></span>

<span data-ttu-id="2352a-147">Результат зависит от того, включены ли метаданные.</span><span class="sxs-lookup"><span data-stu-id="2352a-147">The result depends on if metadata is enabled.</span></span>

##### <a name="metadata-is-not-enabled-default"></a><span data-ttu-id="2352a-148">Метаданные не включены (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2352a-148">Metadata is not enabled (default)</span></span>

<span data-ttu-id="2352a-149">Разрешения Windows для вновь созданного файла будут такими же, как если бы вы создали файл в Windows без определенного дескриптора безопасности, он наследует разрешения родителя.</span><span class="sxs-lookup"><span data-stu-id="2352a-149">The Windows permissions of the newly created file will be the same as if you created the file in Windows without a specific security descriptor, it will inherit the parent's permissions.</span></span> 

##### <a name="metadata-is-enabled"></a><span data-ttu-id="2352a-150">Метаданные включены</span><span class="sxs-lookup"><span data-stu-id="2352a-150">Metadata is enabled</span></span>

<span data-ttu-id="2352a-151">Биты разрешений файла задаются в соответствии с umask Linux, и файл будет сохранен вместе с метаданными.</span><span class="sxs-lookup"><span data-stu-id="2352a-151">The file's permission bits are set to follow the Linux umask, and the file will be saved with metadata.</span></span>

#### <a name="which-linux-user-and-linux-group-owns-the-file"></a><span data-ttu-id="2352a-152">Какой пользователь Linux и группа Linux владеет файлом?</span><span class="sxs-lookup"><span data-stu-id="2352a-152">Which Linux user and Linux group owns the file?</span></span> 

<span data-ttu-id="2352a-153">Результат зависит от того, есть ли у файла уже существующие метаданные.</span><span class="sxs-lookup"><span data-stu-id="2352a-153">The result depends on if the file already has existing metadata.</span></span>

##### <a name="the-file-does-not-have-metadata-default"></a><span data-ttu-id="2352a-154">**Файл не имеет метаданных (по умолчанию)**</span><span class="sxs-lookup"><span data-stu-id="2352a-154">**The file does not have metadata (default)**</span></span>
<span data-ttu-id="2352a-155">В сценарии по умолчанию при автомонтировании дисков Windows мы указываем, что ИДЕНТИФИКАТОРу пользователя (UID) для любого файла присваивается идентификатор пользователя WSL, а ИДЕНТИФИКАТОРу группы (GID) присваивается идентификатор группы участников пользователя WSL.</span><span class="sxs-lookup"><span data-stu-id="2352a-155">In the default scenario, when automounting Windows drives, we specify that the user ID (UID) for any file is set to the user ID of your WSL user and the group ID (GID) is set to the principal group ID of your WSL user.</span></span> 

##### <a name="the-file-has-metadata"></a><span data-ttu-id="2352a-156">Файл содержит метаданные</span><span class="sxs-lookup"><span data-stu-id="2352a-156">The file has metadata</span></span>

<span data-ttu-id="2352a-157">Идентификаторы UID и GID, указанные в метаданных, применяются как владелец пользователя и владелец группы файла.</span><span class="sxs-lookup"><span data-stu-id="2352a-157">The UID and GID specified in the metadata is applied as the user owner and group owner of the file.</span></span> 

### <a name="accessing-linux-files-from-windows-using-wsl"></a><span data-ttu-id="2352a-158">Доступ к файлам Linux из Windows с помощью `\\wsl$`</span><span class="sxs-lookup"><span data-stu-id="2352a-158">Accessing Linux files from Windows using `\\wsl$`</span></span>

<span data-ttu-id="2352a-159">Для доступа к файлам Linux с помощью `\\wsl$` будет использоваться пользователь по умолчанию WSL дистрибутив.</span><span class="sxs-lookup"><span data-stu-id="2352a-159">Accessing Linux files via `\\wsl$` will use the default user of your WSL distro.</span></span> <span data-ttu-id="2352a-160">Таким образом, все приложения Windows, обращающиеся к файлам Linux, будут иметь те же разрешения, что и пользователь по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2352a-160">Therefore any Windows app accessing Linux files will have the same permissions as the default user.</span></span>

#### <a name="creating-a-new-file"></a><span data-ttu-id="2352a-161">Создание нового файла</span><span class="sxs-lookup"><span data-stu-id="2352a-161">Creating a new file</span></span>

<span data-ttu-id="2352a-162">Umask по умолчанию применяется при создании нового файла в WSL дистрибутив из Windows.</span><span class="sxs-lookup"><span data-stu-id="2352a-162">The default umask is applied when creating a new file inside of a WSL distro from Windows.</span></span> <span data-ttu-id="2352a-163">Значение по умолчанию umask `022`или другими словами, оно позволяет использовать все разрешения, кроме разрешения на запись в группы и другие.</span><span class="sxs-lookup"><span data-stu-id="2352a-163">The default umask is `022`, or in other words it allows all permissions except write permissions to groups and others.</span></span> 

### <a name="accessing-files-in-the-linux-root-file-system-from-linux"></a><span data-ttu-id="2352a-164">Доступ к файлам в корневой файловой системе Linux из Linux</span><span class="sxs-lookup"><span data-stu-id="2352a-164">Accessing files in the Linux root file system from Linux</span></span>

<span data-ttu-id="2352a-165">Все файлы, созданные, измененные или доступные в корневой файловой системе Linux, следуют стандартным соглашениям Linux, таким как применение umask к только что созданному файлу.</span><span class="sxs-lookup"><span data-stu-id="2352a-165">Any files created, modified, or accessed in the Linux root file system follow standard Linux conventions, such as applying the umask to a newly created file.</span></span>

## <a name="configuring-file-permissions"></a><span data-ttu-id="2352a-166">Настройка разрешений для файла</span><span class="sxs-lookup"><span data-stu-id="2352a-166">Configuring file permissions</span></span>

<span data-ttu-id="2352a-167">Вы можете настроить разрешения для файлов в дисках Windows с помощью параметров подключения в WSL. conf.</span><span class="sxs-lookup"><span data-stu-id="2352a-167">You can configure your file permissions inside of your Windows drives using the mount options in wsl.conf.</span></span> <span data-ttu-id="2352a-168">Параметры подключения позволяют задать маски разрешений `umask`, `dmask` и `fmask`.</span><span class="sxs-lookup"><span data-stu-id="2352a-168">The mount options allow you to set `umask`, `dmask` and `fmask` permissions masks.</span></span> <span data-ttu-id="2352a-169">`umask` применяется ко всем файлам, `dmask` применяется только к каталогам, а `fmask` применяется только к файлам.</span><span class="sxs-lookup"><span data-stu-id="2352a-169">The `umask` is applied to all files, the `dmask` is applied just to directories and the `fmask` is applied just to files.</span></span> <span data-ttu-id="2352a-170">Эти маски разрешений затем помещаются в логическую операцию или при применении к файлам, например, если имеется `umask` значение `023` и `fmask` значение `022` то результирующая Маска разрешений для файлов будет `023`.</span><span class="sxs-lookup"><span data-stu-id="2352a-170">These permission masks are then put through a logical OR operation when being applied to files, e.g: If you have a `umask` value of `023` and an `fmask` value of `022` then the resulting permissions mask for files will be `023`.</span></span> 

<span data-ttu-id="2352a-171">Инструкции о том, как это сделать, см. на странице документа ["Управление дистрибутивами Linux"](./wsl-config.md) .</span><span class="sxs-lookup"><span data-stu-id="2352a-171">Please see the ['Manage Linux Distributions'](./wsl-config.md) document page for instructions on how to do this.</span></span>
<!-- TODO: Add # to the link-->

