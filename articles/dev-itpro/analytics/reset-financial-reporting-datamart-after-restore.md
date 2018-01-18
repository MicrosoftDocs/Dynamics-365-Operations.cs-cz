---
title: "Resetování datového tržiště finančního výkaznictví"
description: "Toto téma popisuje postup resetování datového tržiště finančního výkaznictví."
author: aolson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 5b956dcc5a4a93033396ae0ffcf8b7aeba2cf3f2
ms.openlocfilehash: a07e8b5bae2c4f71e9212cd2f8080d2481769818
ms.contentlocale: cs-cz
ms.lasthandoff: 12/14/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a>Resetování datového tržiště finančního výkaznictví

[!include[banner](../includes/banner.md)]

Toto téma vysvětluje resetování datového tržiště finančního výkaznictví pro následující verze:

- Aplikace Microsoft Dynamics 365 for Finance and Operations: Finanční výkaznictví
- Microsoft Dynamics 365 for Finance and Operations: Finanční výkaznictví, vydání 7.0.10000.4 a vyšší
- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (místní)

Abyste získali Finance and Operations: Finanční výkaznictví, vydání 7.2.6.0, můžete stáhnout článek znalostní báze KB 4052514 z <https://fix.lcs.dynamics.com/Issue/Resolved?kb=4052514>.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a>Resetování datového tržiště finančního výkaznictví pro Finance and Operations, Finanční výkaznictví, vydání 7.2.6.0 a vyšší

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a>Resetování datového tržiště finančního výkaznictví z Návrháře sestav

> [!NOTE]
> Kroky v tomto procesu jsou podporovány pro Finance and Operations, Finanční výkaznictví, vydání 7.2.6.0 a vyšší. Pokud máte dřívější vydání, obraťte se na tým podpory.

V určitých situacích je nutné resetovat datové tržiště pro Finanční výkaznictví Tento úkol můžete dokončit v klientovi návrháře sestav. Zde je několik scénářů, kdy je třeba resetovat datové tržiště:

- Databáze aplikace Finance and Operations byla obnovena, ale nebyla obnovena databáze datového tržiště.
- Za určité období máte nesprávná data.
- Podpora vás může vyzvat k resetování datového tržiště jako součást kroku při řešení potíží.

Resetování datového tržiště má být provedeno pouze během situace, kdy je se na databázi zpracovává malé množství dat. Finanční výkaznictví není k dispozici během procesu resetování.

#### <a name="reset-the-data-mart"></a>Resetování datového tržiště

Chcete-li resetovat datového tržiště, v návrháři sestav v nabídce **Nástroje** zvolte **Resetovat datové tržiště**. Zobrazené dialogové okno má dvě části: **Statistiky** a **Resetování**.

[![Dialogové okno resetování datového tržiště](./media/Reset-72.jpg)](./media/Reset-72.jpg)

##### <a name="integration-attempts"></a>Pokusy o integraci

Mřížka **Integrace pokusí** ukazuje, kolikrát se systém pokusil integrovat transakce. Systém pokračuje v pokusu o integraci dat několik dnů, pokud několik prvních pokusů není úspěšných. Uvidíte, že datové tržiště je třeba resetovat, pokud je počet pokusů 8 a více a pokud existuje mnoho kombinací dimenzí nebo záznamů transakcí. V tomto případě nebudou data vyreportována.

##### <a name="data-status"></a>Stav dat

Mřížka **Stav dat** poskytuje snímek transakcí, směnných kurzů a hodnoty dimenzí v datovém tržišti. Velký počet zastaralých záznamů označuje, že došlo k četným aktualizacím záznamům. Taková situace může způsobit pomalejší čas generování sestav.

##### <a name="misaligned-main-account-categories"></a>Nezarovnané kategorie hlavního účtu

Používáte-li verzi, která je starší než Microsoft Dynamics 365 for Finance and Operations: Finanční výkaznictví, vydání 7.2.1, může být zapotřebí resetovat datové tržiště, pokud přejmenujete účty nebo přesunete účty mezi kategoriemi účtů. Tyto akce mohou způsobit, že hlavní kategorie účtů budou nesprávně zarovnány. Pole **Nezarovnané kategorie hlavního účtu** ukazuje, zda dochází k daného problému.

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a>Resetování datového tržiště Finance and Operations: Finanční výkaznictví, vydání 7.2.6.0

Chcete-li resetovat datové tržiště v aplikaci Finance and Operations: Finanční výkaznictví, vydání 7.2.6.0 a dřívější, v dialogovém okně **Resetovat datové tržiště** zvolte zaškrtávací políčko **Resetovat datové tržiště** a poté vyberte **OK**. Resetování datového tržiště musí být prováděno pouze během plánované odstávky.

[![Zaškrtávací políčko resetování datového tržiště](./media/Reset-72.jpg)](./media/Reset-72.jpg)

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a>Resetování datového tržiště a volba důvodu v aplikaci Microsoft Dynamics 365 for Finance and Operations: Finanční výkaznictví, vydání 7.3.0

Pokud určíte, že je nutné resetovat datové tržiště, zvolte zaškrtávací políčko **Resetovat datové tržiště** a poté vyberte příčinu v poli **Důvod**. Existují tyto možnosti:

- **Chybějící nebo nesprávná data** – Na základě statistik jste určili, že mohou chybět data. Než budete pokračovat, doporučujeme, abyste kontaktovali podporu a pokusili se určit hlavní příčinu.
- **Obnovit databázi** – Databáze aplikace Finance and Operations byla obnovena, ale nebyla obnovena databáze datového tržiště finančního výkaznictví.
- **Ostatní** – Resetujete datové tržiště z jiného důvodu. Pokud se obáváte problému, kontaktujte podporu, která ho identifikuje.

[![Resetovat datové tržiště](./media/Integration.png)](./media/Integration.png)

> [!NOTE]
> Před zahájením resetu ověřte, zda všechny úlohy resetu datového tržiště dokončily počáteční vytížení. To můžete potvrdit vyhledáním hodnoty ve sloupci Čas posledního spuštění výběrem položek **Nástroje** &gt; **Stav integrace**.

#### <a name="clear-users-and-companies"></a>Vymazat uživatele a společnosti

Vyberte zaškrtávací políčko **Vymazat uživatele a společnosti**, pokud jste obnovili databázi, ale poté jste provedli změny uživatelů nebo společností. Toto políčko budete muset zaškrtávat zřídka.

Jakmile jste připraveni zahájit proces resetování, zvolte **OK**. Budete vyzváni k potvrzení, že jste připraveni zahájit proces. Všimněte si, že finanční výkaznictví nebude k dispozici během resetování a během počáteční integrace dat, ke které dochází později.

Pokud chcete ověřit stav integrace, vyberte **Nástroje** &gt; **Stav integrace** a zobrazí se poslední čas, kdy byla integrace naposledy spuštěna, a její stav.

[![Zobrazení stavu integrace](./media/New-integration.PNG)](./media/New-integration.PNG)

> [!NOTE]
> Reset je dokončen, když všechna mapování zobrazují stav RanToCompletion a okno stavu integrace okno v levém dolním rohu říká Integrace dokončena.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a>Resetování datového tržiště finančního výkaznictví pro Finance and Operations, Finanční výkaznictví, vydání 7.0.10000.4 a vyšší

Pokud někdy obnovíte databázi aplikace Finance and Operations ze zálohy nebo zkopírujete databázi z jiného prostředí, musíte postupovat podle kroků v této části, chcete-li zajistit, aby datové tržiště finančního výkaznictví správně používalo obnovenou databázi aplikace Finance and Operations.

> [!NOTE]
> Kroky v tomto procesu jsou podporovány aplikací Microsoft Dynamics AX, verze 7.0.1 (květen 2016) (sestavení aplikace 7.0.1265.23014 a sestavení finančního výkaznictví 7.0.10000.4) a vyšší. Pokud máte dřívější verzi aplikace Finance and Operations, obraťte se na náš tým podpory pro pomoc.

### <a name="export-report-definitions"></a>Export definicí sestav

Nejdříve postupujte podle těchto kroků pro exportování návrhů sestav z návrháře sestav.

1. V návrháři sestav zvolte **Společnost** &gt; **Skupiny stavebních bloků**.
2. Vyberte skupinu stavebních bloků k exportu a poté zvolte **Export**.

    > [!NOTE]
    > V modulu Finance and Operations je podporována pouze jedna skupina stavebních bloků, **výchozí**.

3. Vyberte definice sestavy k exportu:

    - Pokud chcete vyexportovat všechny definice sestav a přidružené stavební bloky, zvolte **Vybrat vše**.
    - Pokud chcete exportovat konkrétní sestavy, řádky, sloupce, stromy či sady dimenzí, zvolte příslušnou kartu a vyberte položky k exportu. Stisknutím a podržením klávesy Ctrl vyberte více položek na kartě. Při výběru sestav, které chcete exportovat, jsou vybrány přidružené řádky, sloupce, stromy a sady dimenzí.

4. Vyberte **Export**.
5. Zadejte název souboru a vyberte bezpečné místo, kam chcete uložit exportované definice sestavy.
6. Zvolte **Uložit**.

Můžete kopírovat nebo odeslat tento soubor do bezpečného umístění. Tímto způsobem lze soubor importovat do jiného prostředí později. Informace o použití účtu úložiště Microsoft Azure naleznete v části [Přenos dat pomocí nástroje příkazového řádku AzCopy](/azure/storage/storage-use-azcopy).

> [!NOTE]
> Microsoft neposkytuje úložiště účtu v rámci vaší smlouvy na aplikaci Finance and Operations. Musíte zakoupit účet úložiště nebo použít účet úložiště ze samostatného předplatného Azure.

> [!WARNING]
> Musíte znát chování jednotky D na virtuálních počítačích Azure. Neukládejte trvale své exportované skupiny stavebních bloků na jednotce D. Více informací o dočasných discích naleznete v části [Princip dočasné jednotky na virtuálních počítačích Windows Azure](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

### <a name="stop-services"></a>Ukončení služeb

Následující služby systému Microsoft Windows budou mít otevřená připojení k databázi Finance and Operations. Proto musíte použít vzdálenou plochu Microsoft pro připojení ke všem počítačům v prostředí a zastavit tyto služby pomocí services.msc.

- World wide web publishing service (na všech počítačích AOS)
- Microsoft Dynamics 365 for Finance and Operations Batch Management Service (pouze na nesoukromých počítačích AOS)
- Management Reporter 2012 Process Service (pouze v počítačích BI)

### <a name="reset"></a>Resetovat

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a>Stažení nejnovějšího balíčku MinorVersionDataUpgrade.zip

Stáhněte nejnovější balíček MinorVersionDataUpgrade.zip. Pokyny k vyhledání a stažení správné verze balíčku upgradu dat lze najít v části [Stažení nejnovějšího nasaditelného balíčku pro upgrade dat](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package). 

Upgrade ke stažení balíčku MinorVersionDataUpgrade.zip není vyžadován. Proto stačí postupovat podle kroků v části "Stažení nejnovějšího nasaditelného balíčku pro upgrade dat" tohoto tématu. Je možné přeskočit všechny ostatní kroky v tomto tématu.

#### <a name="run-scripts-against-the-finance-and-operations-database"></a>Spuštění skriptů proti databázi Finance and Operations

Spusťte následující skripty proti databázi Finance and Operations (nikoli proti databázi finančního výkaznictví):

- DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
- DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Tyto skripty pomáhají zaručit správnost uživatelů, rolí a nastavení sledování změn.

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a>Spuštění příkazu Windows PowerShell pro resetování databáze

V počítači AOS spusťte Microsoft Windows PowerShell jako správce a pro resetování integrace mezi aplikací Finance and Operations a finančním výkaznictvím spusťte následující příkazy.

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

Zde uvádíme vysvětlení parametrů v příkazu **Reset-DatamartIntegration**:

- Platné hodnoty parametru **-Reason** jsou **SERVICING**, **BADDATA** a **OTHER**.
- Parametr **-ReasonDetail** je textový.
- Parametry reason a reason detail budou zaznamenány ve sledování telemetrie/prostředí.

> [!NOTE]
> Po spuštění příkazů se zobrazí výzva k zadání **Y** pro potvrzení, že chcete resetovat databázi.

#### <a name="restart-services"></a>Restartování služeb

Pomocí services.msc restartujte dříve zastavené služby:

- World wide web publishing service (na všech počítačích AOS)
- Microsoft Dynamics 365 for Finance and Operations Batch Management Service (pouze na nesoukromých počítačích AOS)
- Management Reporter 2012 Process Service (pouze v počítačích BI)

#### <a name="import-report-definitions"></a>Import definicí sestav

Importujte návrhy sestavy z Návrháře sestav pomocí souboru vytvořeného během exportu.

1. V návrháři sestav zvolte **Společnost** &gt; **Skupiny stavebních bloků**.
2. Vyberte skupinu stavebních bloků k exportu a poté zvolte **Export**.

    > [!NOTE]
    > V modulu Finance and Operations je podporována pouze jedna skupina stavebních bloků, **výchozí**.

3. Vyberte stavební blok **Výchozí** a zvolte **Import**.
4. Vyberte soubor obsahující definice exportované sestavy a zvolte **Otevřít**.
5. V dialogovém okně **Import** vyberte definice sestav, které chcete naimportovat:

    - Pokud chcete importovat všechny definice sestav a přidružené stavební bloky, zvolte **Vybrat vše**.
    - Chcete-li naimportovat konkrétní sestavy, řádky, sloupce, stromy nebo sady dimenzí, vyberte konkrétní sestavy, řádky, sloupce, stromy nebo sady dimenzí, které chcete naimportovat.

6. Vyberte **Import**.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a>Resetování datového tržiště finančního výkaznictví pro Finance and Operations (místní)

1. Požádejte všechny uživatele, aby ukončili návrháře sestav a oblast finančního výkaznictví aplikace Finance and Operations.
2. Spusťte následující skript proti databázi finančního vykazování (MRDB).

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. Zkraťte nebo odstraňte všechny záznamy z tabulky FINANCIALREPORTS v databázi aplikace Finance and Operations.
4. Zkraťte nebo odstraňte všechny záznamy z tabulky FINANCIALREPORTVERSION, pokud tato databáze v aplikaci Finance and Operations existuje. Pokud tabulka neexistuje v databázi aplikace Finance and Operations, vynechte tento krok.
5. Spusťte skript **ResetDatamart.sql** proti databázi finančního vykazování. Tento skript zakáže integraci datového tržiště, odstraní všechna data datového tržiště potom znovu povolí integraci datového tržiště.

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. Po resetování můžete znovu ověřit ručně načtení dat spuštěním následujícího dotazu proti databázi finančního výkaznictví.

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    Potvrďte, že všechny řádky mají hodnotu **LastRunTime** a že **StateType** je nastaven na **5**. Hodnota **5** pro **StateType** označuje, že data byla úspěšně znovu načtena. Hodnota **7** označuje chybový stav. V některých případech mapa organizační hierarchie má tento stav při prvním spuštění. Chybový stav by však měl být automaticky vyřešen.

