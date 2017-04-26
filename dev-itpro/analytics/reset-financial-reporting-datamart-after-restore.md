---
title: "Po obnovení databáze obnovit finanční vykazování datového tržiště"
description: "Toto téma popisuje, jak obnovit po obnovení služeb Microsoft Dynamics 365 pro operace databáze datového tržiště finanční vykazování."
author: twheeloc
manager: AnnBe
ms.date: 2016-12-08 16 - 20 - 13
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 3967cbb869fbb23d5d7716f619e4c22b4a273921
ms.lasthandoff: 03/29/2017


---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>Po obnovení databáze obnovit finanční vykazování datového tržiště

Toto téma popisuje, jak obnovit po obnovení služeb Microsoft Dynamics 365 pro operace databáze datového tržiště finanční vykazování. 

Existuje několik scénářů, kde pravděpodobně nutné obnovit vaše 365 Dynamics pro operace databáze ze zálohy nebo kopírování databáze z jiného prostředí. V takovém případě musíte také dodržovat vhodná opatření s cílem zajistit, aby finanční zpravodajské datového tržiště je správně používali obnovené 365 Dynamics pro operace databáze. Pokud máte otázky týkající se obnovení finanční vykazování datového tržiště z důvodu mimo Dynamics 365 pro databázové operace obnovení, naleznete [obnovení datového tržiště Management Reporter](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) Další informace. Všimněte si, že kroky v tomto procesu jsou podporovány pro Dynamics 365 pro operaci vydání květen 2016 (App 7.0.1265.23014 a finanční vykazování sestavení 7.0.10000.4) a novější verze. Pokud máte dřívější verzi Dynamics 365 pro operace, obraťte se na náš tým podpory pro pomoc.

## <a name="export-report-definitions"></a>Export definice sestav
Nejprve exportujte návrhů sestavy v Návrhář sestav, pomocí následujících kroků:

1.  V Návrhář sestav, přejděte na **společnost**&gt;**stavební skupiny**.
2.  Vyberte skupinu stavební blok exportovat, a klepněte na tlačítko **Export**. **Poznámka:** pro Dynamics 365 pro operace, je podporován pouze jeden stavební skupiny, **výchozí**.
3.  Vyberte definici sestavy exportovat:
    -   Pokud chcete exportovat všechny definice sestavy a přidružené stavební bloky, klikněte na tlačítko **Vybrat vše**.
    -   Pokud chcete exportovat konkrétní sestavy, řádky, sloupce, stromy či sady dimenzí, klikněte na příslušnou kartu a vyberte položky k exportu. Když stisknete a podržíte klávesu Ctrl, můžete vybrat na kartě více položek. Při výběru sestavy exportovat související řádky, sloupce, stromy a sad dimenzí jsou vybrány.

4.  Klepněte na tlačítko **Export**.
5.  Zadejte název souboru a vyberte bezpečné místo, kam chcete uložit exportovaná sestava definice.
6.  Click **Save**.

Soubor lze zkopírovat nebo uložit na bezpečném místě, což ho později importovat do jiného prostředí. Informace o použití účtu Microsoft Azure úložiště naleznete v [přenos dat pomocí nástroje příkazového řádku AzCopy](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy). **Poznámka:** Microsoft neposkytuje účtu úložiště v rámci aplikace Dynamics 365 operace smlouvy. Musíte zakoupit účet úložiště nebo ze samostatné předplatné Azure účet úložiště. **Důležité:** znát chování jednotky D na Azure virtuálních počítačů. Trvale vést vaše exportované stavební skupiny. Další informace o dočasné jednotky, viz [Principy dočasnou jednotku na virtuálních počítačích Windows Azure](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>Zastavení služeb
Pomocí připojení ke vzdálené ploše připojit k ostatním počítačům v prostředí a zastaví následující služby systému Windows pomocí services.msc:

-   (Ve všech počítačích serveru AOS) služby publikování na webu
-   Microsoft Dynamics 365 služby Řízení dávkové operace (pouze v počítačích jiných soukromých AOS)
-   Služba proces Management Reporter 2012 (pouze v počítačích BI)

Tyto služby mají otevřené připojení k 365 Dynamics pro operace databáze.

## <a name="reset"></a>Resetovat
#### <a name="locate-the-latest-dataupgradezip-package"></a>Vyhledejte nejnovější balíček DataUpgrade.zip

Vyhledejte nejnovější balíček DataUpgrade.zip pomocí pokynů v [stažení skriptu DataUpgrade.zip](..\migration-upgrade\upgrade-data-to-latest-update.md). Pokyny vysvětlují, jak najít správnou verzi dat inovační balíček pro vaše prostředí.

#### <a name="execute-scripts-against-dynamics-365-for-operations-database"></a>Spuštění skriptů pro operace databáze Dynamics 365

Spusťte následující skripty 365 Dynamics pro operace databáze (nikoli proti finanční vykazování databáze).

-   DataUpgrade.zip\\AosService\\skripty\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\skripty\\GrantAzViewChangeTracking.sql

Tyto skripty zkontrolujte správnost uživatelů, rolí a nastavení sledování změn.

#### <a name="execute-powershell-command-to-reset-database"></a>Chcete-li obnovit databázi spustit příkaz prostředí PowerShell

Přímo v počítači serveru AOS, obnovíte integrace mezi Dynamics 365 pro operace a finanční hlášení spusťte následující příkaz:

1.  Otevřete prostředí Windows PowerShell jako správce.
2.  Provedení: F:
3.  Provedení: cd F:\\MRApplicationService\\MRInstallDirectory
4.  Provedení: Import-Module. \\Server\\MRDeploy\\MRDeploy.psd1
5.  Provedení: Reset DatamartIntegration-jiný důvod - ReasonDetail "&lt;Můj důvod pro obnovení&gt;"
    -   Zobrazí se výzva zadejte "Y" pro potvrzení.

Vysvětlení parametrů:

-   Platné hodnoty parametru - příčiny jsou: pro OBSLUHU, BADDATA, jiné.
-   Parametr - ReasonDetail je volné.
-   Důvod a reasonDetail budou zaznamenány ve sledování telemetrické a životní prostředí.

## <a name="start-services"></a>Spuštění služeb
Restartujte služby, které jste zastavili dříve pomocí services.msc:

-   (Ve všech počítačích serveru AOS) služby publikování na webu
-   Microsoft Dynamics 365 služby Řízení dávkové operace (pouze v počítačích jiných soukromých AOS)
-   Služba proces Management Reporter 2012 (pouze v počítačích BI)

## <a name="import-report-definitions"></a>Import definice sestav
Importujte návrhů sestavy z Návrháře sestav pomocí souboru vytvořeného během exportu:

1.  V Návrhář sestav, přejděte na **společnost**&gt;**stavební skupiny**.
2.  Vyberte skupinu stavební blok exportovat, a klepněte na tlačítko **Export**. **Poznámka:** pro Dynamics 365 pro operace, je podporován pouze jeden stavební skupiny, **výchozí**.
3.  Vyberte **výchozí** stavební blok a klepněte na tlačítko **Import**.
4.  Vyberte soubor obsahující definice exportovanou sestavu a klepněte na tlačítko **Open**.
5.  V dialogovém okně Import vyberte definice sestavy k importu:
    -   Pokud chcete importovat všechny definice sestavy a podpůrné stavební bloky, klikněte na tlačítko **Vybrat vše**.
    -   Chcete-li importovat konkrétní sestavy, řádky, sloupce, stromy či sady dimenzí, vyberte sestavy, řádky, sloupce, stromy a sady dimenzí k importu.

6.  Click **Import**.



