---
title: "Upgrade přechodového testování"
description: "Toto téma vysvětluje, jak testovat úlohy prováděné po vypnutí aplikace AX 2012, ale před zapnutím aplikace Dynamics 365 for Finance and Operations, Enterprise edition."
author: tariqbell
manager: AnnBe
ms.date: 05/29/2017
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
ms.openlocfilehash: 711ad5cc3aafacf209704349effb4e08019205ac
ms.contentlocale: cs-cz
ms.lasthandoff: 06/15/2017

---

# <a name="upgrade-cutover-testing"></a>Upgrade přechodového testování

[!include[banner](../includes/banner.md)]

[!include[upgrade banner](../includes/upgrade-banner.md)]

*Přechodové* je pojem, který používáme pro konečný proces oživení nového systému. Tento proces sestává z úloh, které nastanou po vypnutí aplikace Microsoft Dynamics AX 2012, ale před zapnutím aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. Účelem přechodového testování upgradu je procvičit proces přechodu na pomoc se zaručením plynulé zkušenosti pro každého, kdo je zapojený do skutečného procesu přechodu.

Během přechodu jsou k dispozici dva hlavní proudy práce:

- **Technický proud práce** – Tento proud práce zahrnuje proces provedení upgradu dat. Vaše společnost vynutí limit povoleného množství prostojů. Během tohoto výpadku nebude k dispozici aplikace AX 2012 ani Finance and Operations. Tento proud práce bude nejspíš muset vyladit postupu upgradování dat, aby byl splněn limit prostojů firmy.
- **Funkční proud práce** – tento proud práce zahrnuje konfigurační úkoly prováděné po dokončení upgradu dat. Všechny tyto úlohy musí být zdokumentované a kvantifikované a musí být přiřazen prostředek, protože funkční tok práce a technický tok práce musí zapadat do limitu prostojů společnosti.

Následující obrázek znázorňuje celkový proces přechodu do praxe tak, jak bude probíhat v produkčním prostředí.

![Proces přechodu](./media/cutover_1.png)

Tento proces přechodu se liší od upgradu základních dat v prostředí sandbox následujícími způsoby:

- Databáze AX 2012 není zkopírována, ale pouze zálohována a následně dojde k úpravě původní databáze. Tento postup je rychlejší a záloha poskytuje vrácení zpět, pokud je vyžadováno.
- Vzhledem k tomu, že výrobní prostředí aplikace Finance and Operations má omezený přístup, úkoly, které již byly provedeny v instanci prostředí sandbox aplikačního serveru objektů (AOS) nyní provádí tým Microsoft DSE. Tyto úkoly zahrnují stažení a import souboru bacpac a spuštění balíčku MajorversionDataUpgrade.zip.
- Přidali jsme následující úkoly:

    - Proveďte kouřový test.
    - Dokončete úkoly nastavení aplikace. Tento krok může být velký, v závislosti na funkcích, které se používají. Při tomto kroku funkční týmu konfiguruje novou funkčnost aplikace tak, že je připravena k použití v upgradovaném systému.
    - Povolte uživatelům návrat zpět. Upozorněte svou uživatelskou bázi, že je upgrade dokončen a mohou znovu používat systém.

## <a name="technical-workstream"></a>Technický proud práce

Technické proud práce zahrnuje různé členy technického týmu: správce databáze (DBA), správce systému AX 2012, správci serveru a vývojáři, kteří jsou obeznámeni s aplikací AX 2012 a Finance and Operations. Toto téma vysvětluje, které úkoly zahrnují které role.

Při testování přechodu se technický tým zaměřuje na výkon a testování spolehlivosti procesu upgradu dat pro ověření, zda odpovídá limitu prostojů ve firmě. V tomto procesu je zahrnuto mnoho prvků hardwaru a softwaru. Některé z těchto prvků jsou místní, zatímco ostatní patří do cloudu společnosti Microsoft. Dále je zde zahrnuta spousta prvků vlastního aplikačního a standardního kódu. Výsledek testování by měl mít jistotu v procesu přechodu pro prostředí.

### <a name="turn-off-the-ax-2012-aos-instances"></a>Vypnutí instancí AX 2012 AOS

Tato úloha zahrnuje správce systému AX 2012 a správce serveru.

Je vhodné ověřit následující oblasti:

- **Dávkové úlohy, které jsou spuštěny v době přechodu** – dlouhotrvající dávková úloha, která již byla zahájena, zabrání ukončení systému. Plánujte předem, abyste mohli v požadovanou dobu ukončit instance AOS. Může být nutné naplánovat dávky tak, aby byly dokončeny nějakou dobu před vypnutím AX 2012.
- **Integrované systémy** – Můžete používat další systémy, které jsou integrovány s prostředím AX 2012. Tyto systémy musíte zahrnout do plánu vypnutí AX 2012. Například může být nutné vypnout integrované systémy nějakou dobu před vypnutím AX 2012, tak aby bylo možné dokončit jakékoli zbývající vlastní transakce. Požadavky na integrované systémy se v jednotlivých firmách značně odlišují. Proto váš tým odborníků musí plánovat tento scénář samostatně.

### <a name="create-a-backup-of-the-ax-2012-database"></a>Vytvoření zálohy databáze AX 2012

Tato úloha zahrnuje DBA. Záloha se použije, pokud je vyžadováno vrácení zpět. Také se použije jako referenční bod, který se uchová po dané období a zobrazí stav systému v daném okamžiku.

Je vhodné ověřit následující oblasti:

- Získejte konkrétní načasování procesu zálohování.
- Upravte používané možnosti zálohování používané (například kompresi versus bez komprese), k zajištění nejrychlejšího možného zálohování.

### <a name="export-the-database-to-bacpac"></a>Export databáze do souboru bacpac

Tato úloha zahrnuje DBA. Výstup tohoto úkolu je soubor exportu, který bude nahrán do systému Microsoft Azure pro nový systém.

Je vhodné ověřit následující oblasti:

- Získejte konkrétní načasování procesu zálohování.
- Optimalizujte proces exportu k zajištění nejrychlejšího průběhu. Optimalizace může vyžadovat následující úkoly:

    - Během exportu měřte systémové prostředky, jako je procesor, V/V disku a paměť.
    - Pokud naleznete omezení prostředků, vytvořte plán pro jejich omezení. Obvykle budete tato omezení zmírňovat přiřazením více požadovaného prostředku.

### <a name="upload-the-bacpac-file-to-azure-storage"></a>Nahrání souboru bacpac do úložiště Azure

Tato úloha zahrnuje správce databáze nebo serveru. Během tohoto úkolu se soubor bacpac přemístí do Azure.

Je vhodné ověřit následující oblasti:

- Vyberte počítač, který bude použit pro odesílání, a ujistěte se, že je nakonfigurovaný nástroj Průzkumník úložiště Azure a je připraven k použití.
- Získání konkrétních načasování procesu odesílání vyžaduje několik měření. Doby nahrávání jsou různé v závislosti na rychlosti vašeho internetového připojení a geografického umístění datového centra Azure ve vztahu k umístění.

### <a name="download-and-import-the-bacpac-file-to-the-azure-sql-database"></a>Stažení a import souboru bacpac do databáze Azure SQL

Když tato úloha bude probíhat při uvedení do praxe, bude ji realizovat tým DSE společnosti Microsoft. Při testování přechodu však zahrnuje váš obchodní název společnosti. Výstupem tohoto úkolu je soubor exportu, který bude nahrán do systému Azure pro nový systém.

Je vhodné ověřit následující oblasti:

- Získejte konkrétní načasování procesu importu.
- Optimalizujte proces exportu k zajištění nejrychlejšího průběhu. Optimalizace může vyžadovat následující úkoly:

    - Změřte systémové prostředky při exportu. Několik příkladů:

        - **V počítači AOS:** procesor, disk v/v a paměť
        - **V instanci databáze SQL Azure:** propustnost databáze SQL (DTU). Azure SQL DTU z aplikace Microsoft SQL Server Management Studio můžete monitorovat na počítači AOS ověřením zobrazení sys.dm_resource_stats.

    - Pokud naleznete omezení prostředků, vytvořte plán pro jejich omezení. Obvykle budete tato omezení zmírňovat přiřazením více požadovaného prostředku. Vzhledem k tomu, že tento počítač je hostovaný společností Microsoft, musíte odeslat požadavek společnosti Microsoft na navýšení zdrojů, pokud zjistíte, že představují překážku.

### <a name="run-the-majorversiondataupgradezip-package"></a>Spusťte balíček MajorVersiondataUpgrade.zip

Když tato úloha bude probíhat při uvedení do praxe, bude ji realizovat tým DSE společnosti Microsoft. Při testování přechodu však vyžaduje zapojení vývojářů. Během tohoto úkolu je stará databázová struktura transformována do struktury nového systému.

Proces synchronizace databáze běží jako součást této úlohy. Synchronizace databáze může v některých situacích trvat dlouhou dobu, například, když se změní clusterovaný index v tabulce, protože tato operace je nákladná operace SQL.

Důrazně doporučujeme nejprve provést analýzu a ladění ve vývojovém prostředí. V prostředí sandbox jsou možnosti ladění a analýzy omezenější. Cílem je mít několik málo nebo žádné problémy, které je nutné vyřešit při testování přechodu.

Je vhodné ověřit následující oblasti:

- Získejte konkrétní načasování procesu importu.
- Optimalizujte proces k zajištění nejrychlejšího průběhu. Optimalizace může vyžadovat následující úkoly:

    - Sledujte výkon jednotlivých skriptů upgradu prostřednictvím tabulky ReleaseUpdateScriptsExecution.
    - Upravte skripty k optimalizaci výkonu. Tento úkol může vyžadovat přizpůsobení kódu skriptu X ++ k optimalizaci pro datovou sadu.
    - Monitorujte Azure SQL DTU pomocí monitorování aplikace Microsoft Dynamics Lifecycle Services (LCS) nebo zobrazení sys.dm_resources_stats v aplikaci Management Studio. Pokud jsou prostředky zcela vyčerpány, můžete si vyžádat vyšší úroveň databáze od týmu Microsoft DSE.

### <a name="roll-back-to-ax-2012"></a>Návrat do aplikace AX 2012

Cílem tohoto úkolu je obnovit databázi pomocí zálohy vytvořené při vypnutí aplikace AX 2012 a jejím následném zapnutí. Stav integrovaných systémů může být rovněž třeba obnovit. Protože se však integrované systémy liší mezi jednotlivými firmami, je nutné naplánovat tento scénář nezávisle, podle okolností. Ačkoli je nepravděpodobné, že se budete muset vrátit zpět, je velmi důležité, abyste měli otestovaný proces pro případ, že to je nezbytné.

## <a name="functional-workstream"></a>Funkční tok práce

Po upgradu dat bude v novém prostředí požadováno několik úloh konfigurace. Cílem tohoto toku práce je zdokumentovat a kvantifikovat všechny konfigurační úlohy a přiřadit prostředek k jednotlivým úlohám pro zajištění, aby tyto úlohy bylo možné provádět spolu s technickým tokem práce během prostojů.

Funkční úkoly obvykle zahrnují změnu hodnot konkrétních parametrů systému nebo jiných konfiguračních dat. Tyto úkoly jsou identifikovány prostřednictvím plně funkčních úspěšných testů, což je aktivita nezávislá na testování přechodu. Když je identifikován úkol tohoto typu, měl by být zkontrolován společně s funkčním prostředkem a vývojářem.

Větší změny mohou vyžadovat, aby byl zapsán vlastní skript upgradu pro aktualizaci dat během procesu upgradu dat. Funkční prostředky však mohou ručně spouštět menší změny prostřednictvím nového systému po upgradu dat.

Musí být testovány větší změny, které mají nové skripty pro upgrade dat. Proto bude nutné spustit jednu nebo více dalších iterací balíčku MajorVersionDataUpgrade.zip. Je důležité zvážit náklady na opětovné spuštění balíčku oproti nákladům na ruční zadávání dat.

U každé ruční změny musí být přidán úkol k dokumentu plánu přechodu. Tato úloha musí zobrazovat následující informace:

-   Co je úkol a co je třeba provést?
-   Kdo to musí provést?
-   Jak dlouho to bude trvat?

