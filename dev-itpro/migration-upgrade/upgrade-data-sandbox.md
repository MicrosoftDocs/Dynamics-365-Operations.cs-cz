---
title: "Upgrade dat v prostředí sandbox"
description: "Toto téma vysvětluje, jak provést upgrade dat aplikace AX 2012 na Dynamics 365 for Finance and Operations v prostředí sandbox."
author: tariqbell
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations, UnifiedOperations, Platform
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: Human Translation
ms.sourcegitcommit: 6816e3820ab77c71bbf9bde4a068375448331671
ms.openlocfilehash: 7140bf740f37a5eb970a5103750a7095d12a33cc
ms.contentlocale: cs-cz
ms.lasthandoff: 06/15/2017

---

# <a name="data-upgrade-in-a-sandbox-environment"></a>Upgrade dat v prostředí sandbox

[!include[banner](../includes/banner.md)]

[!include[upgrade banner](../includes/upgrade-banner.md)]

Výstup tohoto úkolu je upgradovaná databáze, kterou můžete používat v prostředí sandbox. Prostředí sandbox je takové prostředí, kde podnikoví uživatelé a členové funkčního týmu mohou ověřovat funkce aplikace. Mezi tyto funkce patří vlastní nastavení a data, která byla převedena z aplikace Microsoft Dynamics AX 2012.

Důrazně doporučujeme spustit proces upgradu dat ve vývojovém prostředí před spuštěním ve sdíleném prostředí sandbox, protože vám tento přístup pomůže zredukovat celkový čas potřebný pro úspěšný upgrade dat. Další informace získáte v části [Upgrade dat ve vývojovém prostředí](prepare-data-upgrade.md).

## <a name="overview-of-the-sandbox-data-upgrade-process"></a>Přehled upgradu dat v prostředí sandbox

Před zahájením upgradu dat v prostředí sandbox budete již mít upgradovaná data ve vývojovém prostředí, jak je popsáno v části [Upgrade dat ve vývojovém prostředí](prepare-data-upgrade.md). Tyto dva procesy jsou si velmi podobné. Hlavní rozdíl je, že prostředí sandbox používá k ukládání dat databázi Microsoft Azure SQL, zatímco vývojové prostředí používá Microsoft SQL Server. Tento technický rozdíl ve vrstvě databáze vyžaduje mírnou úpravu postupu upgradu dat v prostředí sandbox, protože zálohu z instance databáze aplikace AX 2012 nelze pouze obnovit do databáze SQL.

![Proces upgradu dat prostředí sandbox](./media/data-upgrade-sandbox.png)

Zde jsou hlavní kroky v procesu upgradu.

1. Vytvořte kopii d databáze AX 2012. Důrazně doporučujeme používat kopii, protože musíte odstranit některé objekty v kopii, které budou exportovány.
2. Exportujte zkopírovanou databázi do souboru bacpac souboru pomocí bezplatného nástroje SQL Serveru nazvaného SQLPackage.exe. Tento nástroj poskytuje zvláštní typ zálohy databáze, kterou lze importovat do databáze SQL.
3. Nahrajte soubor bacpac do úložiště Azure.
4. Stáhněte soubor bacpac do počítače aplikačního objektového serveru (AOS) v prostředí sandbox a poté ho importujte pomocí balíčku SQLPackage.exe. Potom je nutné spustit skript v importované databázi a resetovat tak uživatele databáze SQL.
5. Spusťte balíček MajorVersionDataUpgrade.zip ke spuštění upgradu dat proti importované databázi.

## <a name="create-a-copy-of-the-ax-2012-database"></a>Vytvoření kopie databáze AX 2012

Vzhledem k tomu, že je nutné odstranit některé objektů z databáze, musíte vytvořit kopii databáze AX 2012, kterou upgradujete. Tyto objekty zahrnují všechny uživatele ověřování systému Windows. Tyto změny způsobí, že změněnou databázi nebude možné v aplikaci AX 2012 použít. Při tomto kroku vytvoříte kopii databáze a tyto objekty odstraníte.

Tento krok musí provést správce databáze (DBA) nebo osoba, která má podobné znalosti a zkušenosti.

Chcete-li vytvořit kopii databáze, vytvořte zálohu původní databáze a obnovte ji s novým názvem. Zkontrolujte, zda je pro obě databáze k dispozici dostatek místa. Můžete vytvořit kopii na jiném serveru. Verze instanci serveru SQL Server, který je spuštěn v databázi, není důležitá.

Následuje příklad kódu, který vytváří kopii databáze. V tomto příkladu je nutné provést změnu, aby odrážela konkrétní názvy databáze.

    BACKUP DATABASE [AxDB] TO  DISK = N'D:\Backups\axdb_copyForUpgrade.bak' WITH NOFORMAT, NOINIT,  
    NAME = N'AxDB_copyForUpgrade-Full Database Backup', SKIP, NOREWIND, NOUNLOAD, COMPRESSION,  STATS = 10
    GO

    RESTORE DATABASE [AxDB_copyForUpgrade] FROM  DISK = N'D:\Backups\axdb_copyForUpgrade.bak'   WITH  FILE = 1,  
    MOVE N'AXDBBuild_Data' TO N'F:\MSSQL_DATA\AxDB_copyForUpgrade.mdf',  
    MOVE N'AXDBBuild_Log' TO N'G:\MSSQL_LOGS\AxDB_CopyForUpgrade.ldf',  
    NOUNLOAD,  STATS = 5

Po vytvoření kopie spusťte následující skript Transact-SQL (T-SQL).
ÚKOL 

### <a name="export-the-copied-database-to-a-bacpac-file"></a>Export zkopírované databáze do souboru bacpac

Exportujte zkopírovanou databázi do souboru bacpac souboru pomocí nástroje SQLPackage.exe. Tento krok by měl provést správce databáze nebo člen týmu, který má stejné znalosti.

Je velmi důležité instalovat nejnovější verzi systému SQL Server Management Studio před zahájením tohoto kroku. I když je v předchozích verzích aplikace Management Studio k dispozici SQLPackage, nebude fungovat správně v tomto kroku, pokud nenainstalujete nejnovější verzi.

Tento krok je důležitý, protože export bude nutné provést znovu během výpadku před uvedením do provozu. Několik tipů:

- Proces bacpac velmi zatěžuje vstupně/výstupní operace a procesor. Export proto spouštějte v počítači s vysokým výkonem.
- SQLPackage by měl být spuštěn lokálně v počítači, který je hostitelem databáze. Nespouštějte SQLPackage v místním laptopu připojeném k databázovému stroji, protože tento proces je také náročný na síťový provoz.

Dále otevřete okno **příkazového řádku** jako správce a spusťte následující příkazy.

    cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

    SqlPackage.exe /a:export /ssn:localhost /sdn:<database to export> /tf:D:\Exportedbacpac\my.bacpac /p:CommandTimeout=1200 /p:VerifyFullTextDocumentTypesSupported=false

Následuje vysvětlení parametrů:

- **ssn** (Název zdrojového serveru) – název serveru SQL Server, ze které chcete exportovat. Tento parametr by měl pro účely našeho procesu být vždy nastaven na hodnotu **localhost**.
- **sdn** (název zdrojové databáze) – název databáze pro export.
- **tf** (cílový soubor) –Cesta a název souboru pro export. Složka by měla již existovat, ale soubor bude vytvořen procesem.
- **/p:CommandTimeout** – hodnota časového limitu pro dotaz. Tento parametr umožňuje export větších tabulek bez dosažení časového limitu.

### <a name="upload-the-bacpac-file-to-azure-storage"></a>Nahrání souboru bacpac do úložiště Azure

Nahrajte soubor bacpac do úložiště Azure. Viz ÚKOL UsingStorageExplorer.docx

### <a name="import-the-bacpac-file-into-sql-database"></a>Import souboru bacpac do databáze SQL

Při tomto kroku budete importovat exportovaný soubor bacpac do instance databáze SQL, kterou používá prostředí sandbox. Do počítače s prostředím AOS sandbox nejprve nainstalujte nejnovější verzi aplikace Management Studio. Pomocí nástroje SQLPackage.exe pak naimportuje soubor.

Vzhledem k tomu, že existují pravidla brány firewall, která omezují přístup k instanci databáze SQL, budete tyto úkoly provádět přímo v počítači AOS ve vašem konkrétním prostředí sandbox. Přístup však můžete získat pomocí počítače AOS.

Stejně jako u kroku exportu musíte mít nejnovější verzi aplikace Management Studio před zahájením importu. Tento krok nebude fungovat v případě, že máte starší verzi.

Z důvodu výkonu doporučujeme, abyste vložili soubor bacpac soubor na disk D v počítači AOS. Jednotka D na virtuálních počítačích (VM) Azure je fyzický disk, který má zpravidla vyšší výkon než ostatní dostupné disky.

Otevřete okno **příkazového řádku** jako správce a spusťte následující příkazy.

    cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

    SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:<azure sql database server name>.database.windows.net /tu:sqladmin /tp:<password from LCS> /tdn:<New database name> /p:CommandTimeout=1200 /p:DatabaseEdition=Premium /p:DatabaseServiceObjective=P1

Následuje vysvětlení parametrů:

- **tsn** (název cílového serveru) – název serveru SQL Azure pro import. Název je uveden v LCS. Jako příponu uveďte **.database.windows.net**.
- **tdn** (název cílové databáze) – název databáze pro import. Databáze by neměla již existovat. Proces importu ji vytvoří.
- **sf** (zdrojový soubor) – cesta a název zdrojového souboru pro import.
- **tp** (cílové heslo) – heslo SQL pro instanci cílové databáze SQL.
- **tu** (cílový uživatel) – uživatelské jméno SQL pro instanci cílové databáze SQL. Doporučujeme používat **sqladmin**. Heslo pro tohoto uživatele můžete načíst z projektu LCS.
- **/p:CommandTimeout** – hodnota časového limitu pro dotaz. Tento parametr umožňuje export větších tabulek bez dosažení časového limitu.
- **/p:DatabaseServiceObjective** – úroveň vrstvy služeb databáze, která je vytvořena. Můžete zkontrolovat hodnotu existující databáze pomocí aplikace Management Studio. Klikněte pravým tlačítkem na databázi a poté vyberte možnost **Vlastnosti**.

Po spuštění příkazů se zobrazí následující upozornění. Můžete je bezpečně ignorovat.

![Chyba prostředí sandbox](./media/sandbox-2.png)
 
### <a name="run-the-majorversiondataupgradezip-package"></a>Spusťte balíček MajorVersionDataUpgrade.zip

Spusťte nasaditelný balíček upgradu podle pokynů v tématu [Upgrade dat ve vývojovém prostředí, prostředí ukázky nebo prostředí sandbox](upgrade-data-to-latest-update.md).

### <a name="upgrade-a-copy-of-the-database-in-a-development-environment"></a>Upgrade kopie databáze ve vývojovém prostředí

Je užitečné upgradovat stejnou databázi ve vývojovém prostředí. Pokud máte k dispozici kopii databáze pro vývojová prostředí, bude mnohem jednodušší zkoumat chyby, které se nacházejí v upgradovaném prostředí sandbox.

