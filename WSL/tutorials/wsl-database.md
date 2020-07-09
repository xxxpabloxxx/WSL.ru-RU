---
title: Приступая к работе с MySQL MongoDB, PostgreSQL, SQLite, Microsoft SQL Server или Redis, чтобы настроить базу данных в подсистеме Windows для Linux
description: Узнайте, как настроить MySQL MongoDB, PostgreSQL, SQLite, Microsoft SQL Server или Redis в подсистеме Windows для Linux.
keywords: WSL, Windows, виндовссубсистем, MySQL MongoDB, PostgreSQL, SQLite, Microsoft SQL Server, Redis, Windows 10
ms.date: 07/07/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: 8ffd40ef21e8fb8ece529157852ba5d8bb676076
ms.sourcegitcommit: 16ffb1a096a4a7fbb77c58f92258051930cc82da
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2020
ms.locfileid: "86160229"
---
# <a name="get-started-with-databases-on-windows-subsystem-for-linux"></a><span data-ttu-id="0b178-104">Начало работы с базами данных в подсистеме Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="0b178-104">Get started with databases on Windows Subsystem for Linux</span></span>

<span data-ttu-id="0b178-105">Это пошаговое руководство поможет приступить к подключению проекта в WSL к базе данных.</span><span class="sxs-lookup"><span data-stu-id="0b178-105">This step-by-step guide will help you get started connecting your project in WSL to a database.</span></span> <span data-ttu-id="0b178-106">Приступая к работе с MySQL, PostgreSQL, MongoDB, Redis, Microsoft SQL Server или SQLite.</span><span class="sxs-lookup"><span data-stu-id="0b178-106">Get started with MySQL, PostgreSQL, MongoDB, Redis, Microsoft SQL Server, or SQLite.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0b178-107">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="0b178-107">Prerequisites</span></span>

- <span data-ttu-id="0b178-108">Использовать Windows 10 с [обновлением до версии 2004](ms-settings:windowsupdate), **сборкой 19041** или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="0b178-108">Running Windows 10, [updated to version 2004](ms-settings:windowsupdate), **Build 19041** or higher.</span></span>
- <span data-ttu-id="0b178-109">[WSL включен и установлен и обновлен до WSL 2](https://docs.microsoft.com/windows/wsl/install-win10).</span><span class="sxs-lookup"><span data-stu-id="0b178-109">[WSL enabled and installed, and updated to WSL 2](https://docs.microsoft.com/windows/wsl/install-win10).</span></span>
- <span data-ttu-id="0b178-110">[Дистрибутив Linux установлен](https://docs.microsoft.com/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (Ubuntu 18,04 для наших примеров).</span><span class="sxs-lookup"><span data-stu-id="0b178-110">[Linux distribution installed](https://docs.microsoft.com/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (Ubuntu 18.04 for our examples).</span></span>
- <span data-ttu-id="0b178-111">Убедитесь, что дистрибутив Ubuntu 18,04 [работает в режиме WSL 2](https://docs.microsoft.com/windows/wsl/install-win10#set-your-distribution-version-to-wsl-1-or-wsl-2).</span><span class="sxs-lookup"><span data-stu-id="0b178-111">Ensure your Ubuntu 18.04 distribution is [running in WSL 2 mode](https://docs.microsoft.com/windows/wsl/install-win10#set-your-distribution-version-to-wsl-1-or-wsl-2).</span></span> <span data-ttu-id="0b178-112">(WSL может запускать дистрибутивы в режиме v1 или v2.) Это можно проверить, открыв PowerShell и введя следующее:`wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="0b178-112">(WSL can run distributions in both v1 or v2 mode.) You can check this by opening PowerShell and entering: `wsl -l -v`</span></span>

## <a name="differences-between-database-systems"></a><span data-ttu-id="0b178-113">Различия между системами баз данных</span><span class="sxs-lookup"><span data-stu-id="0b178-113">Differences between database systems</span></span>

<span data-ttu-id="0b178-114">Наиболее [популярными вариантами](https://insights.stackoverflow.com/survey/2019#technology-_-databases) для системы базы данных являются:</span><span class="sxs-lookup"><span data-stu-id="0b178-114">The most [popular choices](https://insights.stackoverflow.com/survey/2019#technology-_-databases) for a database system include:</span></span>

- <span data-ttu-id="0b178-115">[MySQL](https://www.mysql.com/why-mysql/) (SQL)</span><span class="sxs-lookup"><span data-stu-id="0b178-115">[MySQL](https://www.mysql.com/why-mysql/) (SQL)</span></span>
- <span data-ttu-id="0b178-116">[PostgreSQL](https://www.postgresql.org/about/) (SQL)</span><span class="sxs-lookup"><span data-stu-id="0b178-116">[PostgreSQL](https://www.postgresql.org/about/) (SQL)</span></span>
- <span data-ttu-id="0b178-117">[Microsoft SQL Server](https://docs.microsoft.com/sql/?view=sql-server-ver15) (SQL)</span><span class="sxs-lookup"><span data-stu-id="0b178-117">[Microsoft SQL Server](https://docs.microsoft.com/sql/?view=sql-server-ver15) (SQL)</span></span>
- <span data-ttu-id="0b178-118">[SQLite](https://www.sqlite.org/about.html) (SQL)</span><span class="sxs-lookup"><span data-stu-id="0b178-118">[SQLite](https://www.sqlite.org/about.html) (SQL)</span></span>
- <span data-ttu-id="0b178-119">[MongoDB](https://www.mongodb.com/what-is-mongodb) (NoSQL)</span><span class="sxs-lookup"><span data-stu-id="0b178-119">[MongoDB](https://www.mongodb.com/what-is-mongodb) (NoSQL)</span></span>
- <span data-ttu-id="0b178-120">[Redis](https://redis.io/topics/introduction) (NoSQL)</span><span class="sxs-lookup"><span data-stu-id="0b178-120">[Redis](https://redis.io/topics/introduction) (NoSQL)</span></span>

<span data-ttu-id="0b178-121">**MySQL** — это реляционная база данных SQL с открытым исходным кодом, которая организует данные в одну или несколько таблиц, в которых типы данных могут быть связаны друг с другом.</span><span class="sxs-lookup"><span data-stu-id="0b178-121">**MySQL** is an open-source SQL relational database, organizing data into one or more tables in which data types may be related to each other.</span></span> <span data-ttu-id="0b178-122">Он вертикально масштабируемый. Это означает, что один конечный компьютер выполняет свою работу.</span><span class="sxs-lookup"><span data-stu-id="0b178-122">It is vertically scalable, which means one ultimate machine will do the work for you.</span></span> <span data-ttu-id="0b178-123">В настоящее время это наиболее широкое использование четырех систем баз данных.</span><span class="sxs-lookup"><span data-stu-id="0b178-123">It is currently the most widely used of the four database systems.</span></span>

<span data-ttu-id="0b178-124">**PostgreSQL** (иногда называется postgres) — это также реляционная база данных SQL с открытым исходным кодом, в которой особое внимание уделяется расширению и соответствию стандартам.</span><span class="sxs-lookup"><span data-stu-id="0b178-124">**PostgreSQL** (sometimes referred to as Postgres) is also an open-source SQL relational database with an emphasis on extensibility and standards compliance.</span></span> <span data-ttu-id="0b178-125">Теперь она также может обрабатывать JSON, однако обычно лучше подходит для структурированных данных, вертикального масштабирования и требований ACID, таких как электронная коммерция и финансовые транзакции.</span><span class="sxs-lookup"><span data-stu-id="0b178-125">It can handle JSON now too, but it is generally better for structured data, vertical scaling, and ACID-compliant needs like eCommerce and financial transactions.</span></span>

<span data-ttu-id="0b178-126">**Microsoft SQL Server** включает SQL Server в Windows, SQL Server на Linux и SQL в Azure.</span><span class="sxs-lookup"><span data-stu-id="0b178-126">**Microsoft SQL Server** includes SQL Server on Windows, SQL Server on Linux, and SQL on Azure.</span></span> <span data-ttu-id="0b178-127">Это также системы управления реляционными базами данных, настроенные на серверах с основной функцией хранения и извлечения данных в соответствии с запросом программных приложений.</span><span class="sxs-lookup"><span data-stu-id="0b178-127">These are also relational database management systems set up on servers with primary function of storing and retrieving data as requested by software applications.</span></span>

<span data-ttu-id="0b178-128">**SQLite** — это автономно автономная, основанная на файлах база данных с открытым исходным кодом, которая обеспечивает переносимость, надежность и высокую производительность даже в средах с нехваткой памяти.</span><span class="sxs-lookup"><span data-stu-id="0b178-128">**SQLite** is an open-source self-contained, file-based, “serverless” database, known for its portability, reliability, and good performance even in low-memory environments.</span></span>

<span data-ttu-id="0b178-129">**MongoDB** — это база данных документов NoSQL с открытым исходным кодом, предназначенная для работы с JSON и хранения данных без схемы.</span><span class="sxs-lookup"><span data-stu-id="0b178-129">**MongoDB** is an open-source NoSQL document database designed to work with JSON and store schema-free data.</span></span> <span data-ttu-id="0b178-130">Это горизонтально масштабируемый. Это означает, что несколько небольших компьютеров будут выполнять свою работу.</span><span class="sxs-lookup"><span data-stu-id="0b178-130">It is horizontally scalable, which means multiple smaller machines will do the work for you.</span></span> <span data-ttu-id="0b178-131">Это хорошо подходит для гибкости и неструктурированных данных, а также для кэширования аналитики в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="0b178-131">It's good for flexibility and unstructured data, and caching real-time analytics.</span></span>

<span data-ttu-id="0b178-132">**Redis** — это хранилище структуры данных NoSQL в памяти с открытым исходным кодом.</span><span class="sxs-lookup"><span data-stu-id="0b178-132">**Redis** is is an open-source NoSQL in-memory data structure store.</span></span> <span data-ttu-id="0b178-133">Вместо документов используются пары "ключ-значение" для хранения.</span><span class="sxs-lookup"><span data-stu-id="0b178-133">It uses key-value pairs for storage instead of documents.</span></span> <span data-ttu-id="0b178-134">Redis известен как гибкость, производительность и широкая поддержка языка.</span><span class="sxs-lookup"><span data-stu-id="0b178-134">Redis is known for its flexibility, performance, and wide language support.</span></span> <span data-ttu-id="0b178-135">Он достаточно гибок для использования в качестве кэша или брокера сообщений и может использовать такие структуры данных, как списки, наборы и хэши.</span><span class="sxs-lookup"><span data-stu-id="0b178-135">It’s flexible enough to be used as a cache or message broker and can use data structures like lists, sets, and hashes.</span></span>

<span data-ttu-id="0b178-136">Выбор базы данных должен зависеть от типа приложения, с которым вы будете использовать базу данных.</span><span class="sxs-lookup"><span data-stu-id="0b178-136">The sort of database you choose should depend on the type of application you will be using the database with.</span></span> <span data-ttu-id="0b178-137">Мы рекомендуем вам изучить преимущества и недостатки структурированных и неструктурированных баз данных и сделать выбор в зависимости от конкретного случая использования.</span><span class="sxs-lookup"><span data-stu-id="0b178-137">We recommend that you look up the advantages and disadvantages of structured and unstructured databases and choose based on your use case.</span></span>

## <a name="install-mysql"></a><span data-ttu-id="0b178-138">Установка MySQL</span><span class="sxs-lookup"><span data-stu-id="0b178-138">Install MySQL</span></span>

<span data-ttu-id="0b178-139">Установка MySQL в WSL (Ubuntu 18,04):</span><span class="sxs-lookup"><span data-stu-id="0b178-139">To install MySQL on WSL (Ubuntu 18.04):</span></span>

1. <span data-ttu-id="0b178-140">Откройте терминал WSL (например, Ubuntu 18.04).</span><span class="sxs-lookup"><span data-stu-id="0b178-140">Open your WSL terminal (ie. Ubuntu 18.04).</span></span>
2. <span data-ttu-id="0b178-141">Обновите пакеты Ubuntu: `sudo apt update`</span><span class="sxs-lookup"><span data-stu-id="0b178-141">Update your Ubuntu packages: `sudo apt update`</span></span>
3. <span data-ttu-id="0b178-142">После обновления пакетов установите MySQL с помощью:`sudo apt install mysql-server`</span><span class="sxs-lookup"><span data-stu-id="0b178-142">Once the packages have updated, install MySQL with: `sudo apt install mysql-server`</span></span>
4. <span data-ttu-id="0b178-143">Подтвердите установку и получите номер версии: `mysql --version`</span><span class="sxs-lookup"><span data-stu-id="0b178-143">Confirm installation and get the version number: `mysql --version`</span></span>

<span data-ttu-id="0b178-144">Также может потребоваться запустить прилагаемый сценарий безопасности.</span><span class="sxs-lookup"><span data-stu-id="0b178-144">You may also want to run the included security script.</span></span> <span data-ttu-id="0b178-145">Это изменяет некоторые менее безопасные параметры по умолчанию для таких вещей, как удаленные корневые имена входа и примеры пользователей.</span><span class="sxs-lookup"><span data-stu-id="0b178-145">This changes some of the less secure default options for things like remote root logins and sample users.</span></span> <span data-ttu-id="0b178-146">Чтобы запустить сценарий безопасности, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0b178-146">To run the security script:</span></span>

1. <span data-ttu-id="0b178-147">Запустите сервер MySQL.`sudo /etc/init.d/mysql start`</span><span class="sxs-lookup"><span data-stu-id="0b178-147">Start a MySQL server: `sudo /etc/init.d/mysql start`</span></span>
2. <span data-ttu-id="0b178-148">Запустите запрос сценария безопасности:`sudo mysql_secure_installation`</span><span class="sxs-lookup"><span data-stu-id="0b178-148">Start the security script prompts: `sudo mysql_secure_installation`</span></span>
3. <span data-ttu-id="0b178-149">В первом запросе будет указано, хотите ли вы настроить подключаемый модуль проверки пароля, который можно использовать для проверки надежности пароля MySQL.</span><span class="sxs-lookup"><span data-stu-id="0b178-149">The first prompt will ask whether you’d like to set up the Validate Password Plugin, which can be used to test the strength of your MySQL password.</span></span> <span data-ttu-id="0b178-150">Затем вы установите пароль для привилегированного пользователя MySQL, решите, следует ли удалять анонимных пользователей, решите, следует ли разрешить вход привилегированного пользователя как локально, так и удаленно, решить, следует ли удалить тестовую базу данных, и, наконец, решить, нужно ли повторно загружать таблицы прав.</span><span class="sxs-lookup"><span data-stu-id="0b178-150">You will then set a password for the MySQL root user, decide whether or not to remove anonymous users, decide whether to allow the root user to login both locally and remotely, decide whether to remove the test database, and, lastly, decide whether to reload the privilege tables immediately.</span></span>

<span data-ttu-id="0b178-151">Чтобы открыть запрос MySQL, введите:`sudo mysql`</span><span class="sxs-lookup"><span data-stu-id="0b178-151">To open the MySQL prompt, enter: `sudo mysql`</span></span>

<span data-ttu-id="0b178-152">Чтобы узнать, какие базы данных доступны, в командной строке MySQL введите:`SHOW DATABASES;`</span><span class="sxs-lookup"><span data-stu-id="0b178-152">To see what databases you have available, in the MySQL prompt, enter: `SHOW DATABASES;`</span></span>

<span data-ttu-id="0b178-153">Чтобы создать новую базу данных, введите:`CREATE DATABASE database_name;`</span><span class="sxs-lookup"><span data-stu-id="0b178-153">To create a new database, enter: `CREATE DATABASE database_name;`</span></span>

<span data-ttu-id="0b178-154">Чтобы удалить базу данных, введите:` DROP DATABASE database_name;`</span><span class="sxs-lookup"><span data-stu-id="0b178-154">To delete a database, enter: ` DROP DATABASE database_name;`</span></span>

<span data-ttu-id="0b178-155">Дополнительные сведения о работе с базами данных MySQL см. в документации по [MySQL](https://dev.mysql.com/doc/mysql-getting-started/en/).</span><span class="sxs-lookup"><span data-stu-id="0b178-155">For more about working with MySQL databases, see the [MySQL docs](https://dev.mysql.com/doc/mysql-getting-started/en/).</span></span>

<span data-ttu-id="0b178-156">Для работы с базами данных MySQL в VS Code попробуйте [расширение MySQL](https://marketplace.visualstudio.com/items?itemName=cweijan.vscode-mysql-client2).</span><span class="sxs-lookup"><span data-stu-id="0b178-156">To work with with MySQL databases in VS Code, try the [MySQL extension](https://marketplace.visualstudio.com/items?itemName=cweijan.vscode-mysql-client2).</span></span>

## <a name="install-postgresql"></a><span data-ttu-id="0b178-157">Установка PostgreSQL</span><span class="sxs-lookup"><span data-stu-id="0b178-157">Install PostgreSQL</span></span>

<span data-ttu-id="0b178-158">Чтобы установить PostgreSQL на WSL (Ubuntu 18,04), сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="0b178-158">To install PostgreSQL on WSL (Ubuntu 18.04):</span></span>

1. <span data-ttu-id="0b178-159">Откройте терминал WSL (например, Ubuntu 18.04).</span><span class="sxs-lookup"><span data-stu-id="0b178-159">Open your WSL terminal (ie. Ubuntu 18.04).</span></span>
2. <span data-ttu-id="0b178-160">Обновите пакеты Ubuntu: `sudo apt update`</span><span class="sxs-lookup"><span data-stu-id="0b178-160">Update your Ubuntu packages: `sudo apt update`</span></span>
3. <span data-ttu-id="0b178-161">После обновления пакетов установите PostgreSQL (и пакет -contrib с некоторыми полезными служебными программами) с помощью команды `sudo apt install postgresql postgresql-contrib`.</span><span class="sxs-lookup"><span data-stu-id="0b178-161">Once the packages have updated, install PostgreSQL (and the -contrib package which has some helpful utilities) with: `sudo apt install postgresql postgresql-contrib`</span></span>
4. <span data-ttu-id="0b178-162">Подтвердите установку и получите номер версии: `psql --version`</span><span class="sxs-lookup"><span data-stu-id="0b178-162">Confirm installation and get the version number: `psql --version`</span></span>

<span data-ttu-id="0b178-163">Есть 3 команды, о которых необходимо знать после установки PostgreSQL:</span><span class="sxs-lookup"><span data-stu-id="0b178-163">There are 3 commands you need to know once PostgreSQL is installed:</span></span>

- <span data-ttu-id="0b178-164">`sudo service postgresql status` позволяет проверить состояние базы данных.</span><span class="sxs-lookup"><span data-stu-id="0b178-164">`sudo service postgresql status` for checking the status of your database.</span></span>
- <span data-ttu-id="0b178-165">`sudo service postgresql start` позволяет запустить базу данных.</span><span class="sxs-lookup"><span data-stu-id="0b178-165">`sudo service postgresql start`  to start running your database.</span></span>
- <span data-ttu-id="0b178-166">`sudo service postgresql stop` позволяет завершить работу с базой данных.</span><span class="sxs-lookup"><span data-stu-id="0b178-166">`sudo service postgresql stop` to stop running your database.</span></span>

<span data-ttu-id="0b178-167">Администратору по умолчанию `postgres` требуется назначать пароль для подключения к базе данных.</span><span class="sxs-lookup"><span data-stu-id="0b178-167">The default admin user, `postgres`, needs a password assigned in order to connect to a database.</span></span> <span data-ttu-id="0b178-168">Чтобы задать пароль, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="0b178-168">To set a password:</span></span>

1. <span data-ttu-id="0b178-169">Введите команду: `sudo passwd postgres`.</span><span class="sxs-lookup"><span data-stu-id="0b178-169">Enter the command: `sudo passwd postgres`</span></span>
2. <span data-ttu-id="0b178-170">Появится запрос на ввод нового пароля.</span><span class="sxs-lookup"><span data-stu-id="0b178-170">You will get a prompt to enter your new password.</span></span>
3. <span data-ttu-id="0b178-171">Закройте и снова откройте терминал.</span><span class="sxs-lookup"><span data-stu-id="0b178-171">Close and reopen your terminal.</span></span>

<span data-ttu-id="0b178-172">Чтобы запустить PostgreSQL с помощью оболочки [psql](https://www.postgresql.org/docs/10/app-psql.html) , выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0b178-172">To run PostgreSQL with [psql](https://www.postgresql.org/docs/10/app-psql.html) shell:</span></span>

1. <span data-ttu-id="0b178-173">Запустите службу postgres: `sudo service postgresql start`</span><span class="sxs-lookup"><span data-stu-id="0b178-173">Start your postgres service: `sudo service postgresql start`</span></span>
2. <span data-ttu-id="0b178-174">Подключитесь к службе postgres и откройте оболочку psql: `sudo -u postgres psql`</span><span class="sxs-lookup"><span data-stu-id="0b178-174">Connect to the postgres service and open the psql shell: `sudo -u postgres psql`</span></span>

<span data-ttu-id="0b178-175">После успешного входа в оболочку psql вы увидите, что ваша командная строка будет выглядеть следующим образом: `postgres=#`</span><span class="sxs-lookup"><span data-stu-id="0b178-175">Once you have successfully entered the psql shell, you will see your command line change to look like this: `postgres=#`</span></span>

> [!NOTE]
> <span data-ttu-id="0b178-176">Кроме того, вы можете открыть оболочку psql, перейдя к пользователю postgres с помощью команды `su - postgres`, а затем введя команду `psql`.</span><span class="sxs-lookup"><span data-stu-id="0b178-176">Alternatively, you can open the psql shell by switching to the postgres user with: `su - postgres` and then entering the command: `psql`.</span></span>

<span data-ttu-id="0b178-177">Чтобы выйти из postgres = # ввод: `\q` или используйте сочетание клавиш, нажмите клавиши CTRL + D.</span><span class="sxs-lookup"><span data-stu-id="0b178-177">To exit postgres=# enter: `\q` or use the shortcut key: Ctrl+D</span></span>

<span data-ttu-id="0b178-178">Чтобы узнать, какие учетные записи пользователей были созданы в установке PostgreSQL, в терминале WSL введите `psql -c "\du"` или просто `\du`, если оболочка psql открыта.</span><span class="sxs-lookup"><span data-stu-id="0b178-178">To see what user accounts have been created on your PostgreSQL installation, use from your WSL terminal: `psql -c "\du"` ...or just `\du` if you have the psql shell open.</span></span> <span data-ttu-id="0b178-179">Эта команда будет отображать столбцы: имя пользователя учетной записи, список атрибутов ролей и член групп ролей.</span><span class="sxs-lookup"><span data-stu-id="0b178-179">This command will display columns: Account User Name, List of Roles Attributes, and Member of role group(s).</span></span> <span data-ttu-id="0b178-180">Чтобы вернуться в командную строку, введите: `q`.</span><span class="sxs-lookup"><span data-stu-id="0b178-180">To exit back to the command line, enter: `q`.</span></span>

<span data-ttu-id="0b178-181">Дополнительные сведения о работе с базами данных PostgreSQL см. в документации по [PostgreSQL](https://www.postgresql.org/docs/13/tutorial-createdb.html).</span><span class="sxs-lookup"><span data-stu-id="0b178-181">For more about working with PostgreSQL databases, see the [PostgreSQL docs](https://www.postgresql.org/docs/13/tutorial-createdb.html).</span></span>

<span data-ttu-id="0b178-182">Для работы с базами данных PostgreSQL в VS Code попробуйте использовать [расширение PostgreSQL](https://marketplace.visualstudio.com/items?itemName=ms-ossdata.vscode-postgresql).</span><span class="sxs-lookup"><span data-stu-id="0b178-182">To work with with PostgreSQL databases in VS Code, try the [PostgreSQL extension](https://marketplace.visualstudio.com/items?itemName=ms-ossdata.vscode-postgresql).</span></span>

## <a name="install-mongodb"></a><span data-ttu-id="0b178-183">Установка MongoDB</span><span class="sxs-lookup"><span data-stu-id="0b178-183">Install MongoDB</span></span>

<span data-ttu-id="0b178-184">Чтобы установить MongoDB на WSL (Ubuntu 18,04), сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="0b178-184">To install MongoDB on WSL (Ubuntu 18.04):</span></span>

1. <span data-ttu-id="0b178-185">Откройте терминал WSL (например, Ubuntu 18.04).</span><span class="sxs-lookup"><span data-stu-id="0b178-185">Open your WSL terminal (ie. Ubuntu 18.04).</span></span>
2. <span data-ttu-id="0b178-186">Обновите пакеты Ubuntu: `sudo apt update`</span><span class="sxs-lookup"><span data-stu-id="0b178-186">Update your Ubuntu packages: `sudo apt update`</span></span>
3. <span data-ttu-id="0b178-187">После обновления пакетов установите MongoDB с помощью: `sudo apt-get install mongodb`</span><span class="sxs-lookup"><span data-stu-id="0b178-187">Once the packages have updated, install MongoDB with: `sudo apt-get install mongodb`</span></span>
4. <span data-ttu-id="0b178-188">Подтвердите установку и получите номер версии: `mongod --version`</span><span class="sxs-lookup"><span data-stu-id="0b178-188">Confirm installation and get the version number: `mongod --version`</span></span>

<span data-ttu-id="0b178-189">После установки MongoDB следует знать 3 команды:</span><span class="sxs-lookup"><span data-stu-id="0b178-189">There are 3 commands you need to know once MongoDB is installed:</span></span>

- <span data-ttu-id="0b178-190">`sudo service mongodb status` позволяет проверить состояние базы данных.</span><span class="sxs-lookup"><span data-stu-id="0b178-190">`sudo service mongodb status` for checking the status of your database.</span></span>
- <span data-ttu-id="0b178-191">`sudo service mongodb start` позволяет запустить базу данных.</span><span class="sxs-lookup"><span data-stu-id="0b178-191">`sudo service mongodb start`  to start running your database.</span></span>
- <span data-ttu-id="0b178-192">`sudo service mongodb stop` позволяет завершить работу с базой данных.</span><span class="sxs-lookup"><span data-stu-id="0b178-192">`sudo service mongodb stop` to stop running your database.</span></span>

> [!NOTE]
> <span data-ttu-id="0b178-193">Вы можете увидеть команду `sudo systemctl status mongodb`, используемую в учебниках или статьях.</span><span class="sxs-lookup"><span data-stu-id="0b178-193">You might see the command `sudo systemctl status mongodb` used in tutorials or articles.</span></span> <span data-ttu-id="0b178-194">Чтобы остаться облегченным, WSL не включает `systemd` (система управления службами в Linux).</span><span class="sxs-lookup"><span data-stu-id="0b178-194">In order to remain lightweight, WSL does not include `systemd` (a service management system in Linux).</span></span> <span data-ttu-id="0b178-195">Вместо этого он использует SysVinit для запуска служб на компьютере.</span><span class="sxs-lookup"><span data-stu-id="0b178-195">Instead, it uses SysVinit to start services on your machine.</span></span> <span data-ttu-id="0b178-196">Вы не должны заметить разницы, но если учебник рекомендует использовать `sudo systemctl`, используйте: `sudo /etc/init.d/`.</span><span class="sxs-lookup"><span data-stu-id="0b178-196">You shouldn't notice a difference, but if a tutorial recommends using `sudo systemctl`, instead use: `sudo /etc/init.d/`.</span></span> <span data-ttu-id="0b178-197">Например, `sudo systemctl status mongodb`для WSL будет `sudo /etc/inid.d/mongodb status`... или вы также можете использовать `sudo service mongodb status`.</span><span class="sxs-lookup"><span data-stu-id="0b178-197">For example, `sudo systemctl status mongodb`, for WSL would be `sudo /etc/inid.d/mongodb status` ...or you can also use `sudo service mongodb status`.</span></span>

<span data-ttu-id="0b178-198">Чтобы запустить базу данных Mongo на локальном сервере, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0b178-198">To run your Mongo database in a local server:</span></span>

1. <span data-ttu-id="0b178-199">Проверьте состояние базы данных: `sudo service mongodb status` вы должны увидеть ответ [Fail], если вы еще не начали работу с базой данных.</span><span class="sxs-lookup"><span data-stu-id="0b178-199">Check the status of your database: `sudo service mongodb status` You should see a [Fail] response, unless you've already started your database.</span></span>

2. <span data-ttu-id="0b178-200">Запустите базу данных. `sudo service mongodb start` теперь должен отобразиться ответ [ОК].</span><span class="sxs-lookup"><span data-stu-id="0b178-200">Start your database: `sudo service mongodb start` You should now see an [OK] response.</span></span>

3. <span data-ttu-id="0b178-201">Проверьте, подключившись к серверу базы данных и выполнив команду диагностики: `mongo --eval 'db.runCommand({ connectionStatus: 1 })'` в результате будет выведена Текущая версия базы данных, адрес и порт сервера, а также выходные данные команды Status.</span><span class="sxs-lookup"><span data-stu-id="0b178-201">Verify by connecting to the database server and running a diagnostic command: `mongo --eval 'db.runCommand({ connectionStatus: 1 })'` This will output the current database version, the server address and port, and the output of the status command.</span></span> <span data-ttu-id="0b178-202">Значение `1` в поле "ОК" в ответе указывает на то, что сервер работает.</span><span class="sxs-lookup"><span data-stu-id="0b178-202">A value of `1` for the "ok" field in the response indicates that the server is working.</span></span>

4. <span data-ttu-id="0b178-203">Чтобы предотвратить запуск службы MongoDB, введите: `sudo service mongodb stop`</span><span class="sxs-lookup"><span data-stu-id="0b178-203">To stop your MongoDB service from running, enter: `sudo service mongodb stop`</span></span>

> [!NOTE]
> <span data-ttu-id="0b178-204">MongoDB имеет несколько параметров по умолчанию, включая хранение данных в /data/db и выполнение на порте 27017.</span><span class="sxs-lookup"><span data-stu-id="0b178-204">MongoDB has several default parameters, including storing data in /data/db and running on port 27017.</span></span> <span data-ttu-id="0b178-205">Кроме того, `mongod` является управляющей программой (хост-процессом для базы данных), а `mongo` — оболочкой командной строки, которая подключается к конкретному экземпляру `mongod`.</span><span class="sxs-lookup"><span data-stu-id="0b178-205">Also, `mongod` is the daemon (host process for the database) and `mongo` is the command-line shell that connects to a specific instance of `mongod`.</span></span>

<span data-ttu-id="0b178-206">VS Code поддерживает работу с базами данных MongoDB с помощью [расширения Azure CosmosDB](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-cosmosdb), вы можете создавать, управлять базами данных MongoDB и выполнять запросы из них в VS Code.</span><span class="sxs-lookup"><span data-stu-id="0b178-206">VS Code supports working with MongoDB databases via the [Azure CosmosDB extension](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-cosmosdb), you can create, manage and query MongoDB databases from within VS Code.</span></span> <span data-ttu-id="0b178-207">Дополнительные сведения см. в VS Code документах: [Работа с MongoDB](https://code.visualstudio.com/docs/azure/mongodb).</span><span class="sxs-lookup"><span data-stu-id="0b178-207">To learn more, visit the VS Code docs: [Working with MongoDB](https://code.visualstudio.com/docs/azure/mongodb).</span></span>

<span data-ttu-id="0b178-208">Дополнительные сведения см. в документах MongoDB:</span><span class="sxs-lookup"><span data-stu-id="0b178-208">Learn more in the MongoDB docs:</span></span>

- [<span data-ttu-id="0b178-209">Общие сведения об использовании MongoDB</span><span class="sxs-lookup"><span data-stu-id="0b178-209">Introduction to using MongoDB</span></span>](https://docs.mongodb.com/manual/introduction/)
- [<span data-ttu-id="0b178-210">Создание пользователей</span><span class="sxs-lookup"><span data-stu-id="0b178-210">Create users</span></span>](https://docs.mongodb.com/manual/tutorial/create-users/)
- [<span data-ttu-id="0b178-211">Подключение к экземпляру MongoDB на удаленном узле</span><span class="sxs-lookup"><span data-stu-id="0b178-211">Connect to a MongoDB instance on a remote host</span></span>](https://docs.mongodb.com/manual/mongo/#mongodb-instance-on-a-remote-host)
- [<span data-ttu-id="0b178-212">CRUD: создание, чтение, обновление, удаление</span><span class="sxs-lookup"><span data-stu-id="0b178-212">CRUD: Create, Read, Update, Delete</span></span>](https://docs.mongodb.com/manual/crud/)
- [<span data-ttu-id="0b178-213">Справочные документы</span><span class="sxs-lookup"><span data-stu-id="0b178-213">Reference Docs</span></span>](https://docs.mongodb.com/manual/reference/)

## <a name="install-microsoft-sql-server"></a><span data-ttu-id="0b178-214">Установка Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="0b178-214">Install Microsoft SQL Server</span></span>

<span data-ttu-id="0b178-215">Чтобы установить SQL Server на WSL (Ubuntu 18,04), следуйте указаниям в этом кратком руководстве: [установка SQL Server и создание базы данных на Ubuntu](https://docs.microsoft.com/sql/linux/quickstart-install-connect-ubuntu?view=sql-server-ver15).</span><span class="sxs-lookup"><span data-stu-id="0b178-215">To install SQL Server on WSL (Ubuntu 18.04), follow this quickstart: [Install SQL Server and create a database on Ubuntu](https://docs.microsoft.com/sql/linux/quickstart-install-connect-ubuntu?view=sql-server-ver15).</span></span>

<span data-ttu-id="0b178-216">Для работы с Microsoft SQL Server базами данных в VS Code используйте [расширение MSSQL](https://marketplace.visualstudio.com/items?itemName=ms-mssql.mssql).</span><span class="sxs-lookup"><span data-stu-id="0b178-216">To work with Microsoft SQL Server databases in VS Code, try the [MSSQL extension](https://marketplace.visualstudio.com/items?itemName=ms-mssql.mssql).</span></span>

## <a name="install-sqlite"></a><span data-ttu-id="0b178-217">Установка SQLite</span><span class="sxs-lookup"><span data-stu-id="0b178-217">Install SQLite</span></span>

<span data-ttu-id="0b178-218">Установка SQLite в WSL (Ubuntu 18,04):</span><span class="sxs-lookup"><span data-stu-id="0b178-218">To install SQLite on WSL (Ubuntu 18.04):</span></span>

1. <span data-ttu-id="0b178-219">Откройте терминал WSL (например, Ubuntu 18.04).</span><span class="sxs-lookup"><span data-stu-id="0b178-219">Open your WSL terminal (ie. Ubuntu 18.04).</span></span>
2. <span data-ttu-id="0b178-220">Обновите пакеты Ubuntu: `sudo apt update`</span><span class="sxs-lookup"><span data-stu-id="0b178-220">Update your Ubuntu packages: `sudo apt update`</span></span>
3. <span data-ttu-id="0b178-221">После обновления пакетов установите SQLite3 с помощью:`sudo apt install sqlite3`</span><span class="sxs-lookup"><span data-stu-id="0b178-221">Once the packages have updated, install SQLite3 with: `sudo apt install sqlite3`</span></span>
4. <span data-ttu-id="0b178-222">Подтвердите установку и получите номер версии: `sqlite3 --version`</span><span class="sxs-lookup"><span data-stu-id="0b178-222">Confirm installation and get the version number: `sqlite3 --version`</span></span>

<span data-ttu-id="0b178-223">Чтобы создать тестовую базу данных с именем example. DB, введите:`sqlite3 example.db`</span><span class="sxs-lookup"><span data-stu-id="0b178-223">To create a test database, called "example.db", enter: `sqlite3 example.db`</span></span>

<span data-ttu-id="0b178-224">Чтобы просмотреть список баз данных SQLite, введите:`.databases`</span><span class="sxs-lookup"><span data-stu-id="0b178-224">To see a list of your SQLite databases, enter: `.databases`</span></span>

<span data-ttu-id="0b178-225">Чтобы просмотреть состояние базы данных, введите:`.dbinfo ?DB?`</span><span class="sxs-lookup"><span data-stu-id="0b178-225">To see the status of your database, enter: `.dbinfo ?DB?`</span></span>

<span data-ttu-id="0b178-226">Чтобы выйти из командной строки SQLite, введите:`.exit`</span><span class="sxs-lookup"><span data-stu-id="0b178-226">To exit the SQLite prompt, enter: `.exit`</span></span>

<span data-ttu-id="0b178-227">Дополнительные сведения о работе с базой данных SQLite см. в документации по [SQLite](https://www.sqlite.org/quickstart.html).</span><span class="sxs-lookup"><span data-stu-id="0b178-227">For more information about working with a SQLite database, see the [SQLite docs](https://www.sqlite.org/quickstart.html).</span></span>

<span data-ttu-id="0b178-228">Для работы с базами данных SQLite в VS Code попробуйте [расширение SQLite](https://marketplace.visualstudio.com/items?itemName=mtxr.sqltools).</span><span class="sxs-lookup"><span data-stu-id="0b178-228">To work with SQLite databases in VS Code, try the [SQLite extension](https://marketplace.visualstudio.com/items?itemName=mtxr.sqltools).</span></span>

## <a name="install-redis"></a><span data-ttu-id="0b178-229">Установка Redis</span><span class="sxs-lookup"><span data-stu-id="0b178-229">Install Redis</span></span>

<span data-ttu-id="0b178-230">Чтобы установить Redis на WSL (Ubuntu 18,04), сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="0b178-230">To install Redis on WSL (Ubuntu 18.04):</span></span>

1. <span data-ttu-id="0b178-231">Откройте терминал WSL (например, Ubuntu 18.04).</span><span class="sxs-lookup"><span data-stu-id="0b178-231">Open your WSL terminal (ie. Ubuntu 18.04).</span></span>
2. <span data-ttu-id="0b178-232">Обновите пакеты Ubuntu: `sudo apt update`</span><span class="sxs-lookup"><span data-stu-id="0b178-232">Update your Ubuntu packages: `sudo apt update`</span></span>
3. <span data-ttu-id="0b178-233">После обновления пакетов установите Redis с помощью:`sudo apt install redis-server`</span><span class="sxs-lookup"><span data-stu-id="0b178-233">Once the packages have updated, install Redis with: `sudo apt install redis-server`</span></span>
4. <span data-ttu-id="0b178-234">Подтвердите установку и получите номер версии: `redis-server --version`</span><span class="sxs-lookup"><span data-stu-id="0b178-234">Confirm installation and get the version number: `redis-server --version`</span></span>

<span data-ttu-id="0b178-235">Чтобы начать работу с сервером Redis, выполните следующие действия.`sudo service redis-server start`</span><span class="sxs-lookup"><span data-stu-id="0b178-235">To start running your Redis server: `sudo service redis-server start`</span></span>

<span data-ttu-id="0b178-236">Проверьте, работает ли Redis (Redis-CLI — служебная программа командной строки для взаимодействия с Redis): `redis-cli ping` это должно вернуть ответ "теннис".</span><span class="sxs-lookup"><span data-stu-id="0b178-236">Check to see if redis is working (redis-cli is the command line interface utility to talk with Redis): `redis-cli ping` this should return a reply of "PONG".</span></span>

<span data-ttu-id="0b178-237">Чтобы прерывать работу сервера Redis, выполните следующие действия.`sudo service redis-server stop`</span><span class="sxs-lookup"><span data-stu-id="0b178-237">To stop running your Redis server: `sudo service redis-server stop`</span></span>

<span data-ttu-id="0b178-238">Дополнительные сведения о работе с базой данных Redis см. в документации по [Redis](https://redis.io/topics/quickstart).</span><span class="sxs-lookup"><span data-stu-id="0b178-238">For more information about working with a Redis database, see the [Redis docs](https://redis.io/topics/quickstart).</span></span>

<span data-ttu-id="0b178-239">Для работы с базами данных Redis в VS Code попробуйте использовать [расширение Redis](https://marketplace.visualstudio.com/items?itemName=cweijan.vscode-redis-client).</span><span class="sxs-lookup"><span data-stu-id="0b178-239">To work with Redis databases in VS Code, try the [Redis extension](https://marketplace.visualstudio.com/items?itemName=cweijan.vscode-redis-client).</span></span>

## <a name="see-services-running-and-set-up-profile-aliases"></a><span data-ttu-id="0b178-240">См. раздел службы запуск и настройка псевдонимов профилей.</span><span class="sxs-lookup"><span data-stu-id="0b178-240">See services running and set up profile aliases</span></span>

<span data-ttu-id="0b178-241">Чтобы просмотреть службы, которые в настоящее время выполняются в дистрибутиве WSL, введите:`service --status-all`</span><span class="sxs-lookup"><span data-stu-id="0b178-241">To see the services that you currently have running on your WSL distribution, enter: `service --status-all`</span></span>

<span data-ttu-id="0b178-242">Вводить `sudo service mongodb start` или `sudo service postgres start` и `sudo -u postgrest psql` может быть утомительно.</span><span class="sxs-lookup"><span data-stu-id="0b178-242">Typing out `sudo service mongodb start` or `sudo service postgres start` and `sudo -u postgrest psql` can get tedious.</span></span>  <span data-ttu-id="0b178-243">Однако, вы можете рассмотреть возможность установки псевдонимов в файле `.profile` на WSL, чтобы сделать эти команды более быстрыми в использовании и легкими в запоминании.</span><span class="sxs-lookup"><span data-stu-id="0b178-243">However, you could consider setting up aliases in your `.profile` file on WSL to make these commands quicker to use and easier to remember.</span></span>

<span data-ttu-id="0b178-244">Настройка собственного пользовательского псевдонима или ярлыка для выполнения этих команд:</span><span class="sxs-lookup"><span data-stu-id="0b178-244">To set up your own custom alias, or shortcut, for executing these commands:</span></span>

1. <span data-ttu-id="0b178-245">Откройте терминал WSL и введите `cd ~`, чтобы убедиться, что вы находитесь в корневом каталоге.</span><span class="sxs-lookup"><span data-stu-id="0b178-245">Open your WSL terminal and enter `cd ~` to be sure you're in the root directory.</span></span>
2. <span data-ttu-id="0b178-246">Откройте файл `.profile`, управляющий настройками терминала, в текстовом редакторе терминала Nano: `sudo nano .profile`.</span><span class="sxs-lookup"><span data-stu-id="0b178-246">Open the `.profile` file, which controls the settings for your terminal, with the terminal text editor, Nano: `sudo nano .profile`</span></span>
3. <span data-ttu-id="0b178-247">В нижней части файла (не меняйте настройки `# set PATH`) добавьте следующее:</span><span class="sxs-lookup"><span data-stu-id="0b178-247">At the bottom of the file (don't change the `# set PATH` settings), add the following:</span></span>

    ```bash
    # My Aliases
    alias start-pg='sudo service postgresql start'
    alias run-pg='sudo -u postgres psql'
    ```

    <span data-ttu-id="0b178-248">Это позволит вам ввести `start-pg` для запуска службы postgresql и `run-pg` — для открытия оболочки psql.</span><span class="sxs-lookup"><span data-stu-id="0b178-248">This will allow you to enter `start-pg` to start running the postgresql service and `run-pg` to open the psql shell.</span></span> <span data-ttu-id="0b178-249">Вы можете изменить `start-pg` и `run-pg` на любые имена, просто следите за тем, чтобы не перезаписать команду, которую postgres уже использует!</span><span class="sxs-lookup"><span data-stu-id="0b178-249">You can change `start-pg` and `run-pg` to whatever names you want, just be careful not to overwrite a command that postgres already uses!</span></span>

4. <span data-ttu-id="0b178-250">После добавления новых псевдонимов выйдите из текстового редактора Nano, используя **Ctrl+X** — выберите `Y` (Да) при запросе сохранения и Enter (имя файла останется `.profile`).</span><span class="sxs-lookup"><span data-stu-id="0b178-250">Once you've added your new aliases, exit the Nano text editor using **Ctrl+X** -- select `Y` (Yes) when prompted to save and Enter (leaving the file name as `.profile`).</span></span>
5. <span data-ttu-id="0b178-251">Закройте и снова откройте терминал WSL, а затем попробуйте использовать свои новые команды ввода псевдонима.</span><span class="sxs-lookup"><span data-stu-id="0b178-251">Close and re-open your WSL terminal, then try your new alias commands.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0b178-252">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0b178-252">Additional resources</span></span>

- [<span data-ttu-id="0b178-253">Настройка среды разработки в Windows 10</span><span class="sxs-lookup"><span data-stu-id="0b178-253">Setting up your development environment on Windows 10</span></span>](https://docs.microsoft.com/windows/dev-environment/)
