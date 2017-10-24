---
title: "Obnovení datového tržiště finančního vykazování po obnovení databáze"
description: "Toto téma popisuje, jak obnovit datový trh finančního výkaznictví po obnovení databázeMicrosoft Dynamics 365 for Finance and Operations."
author: ShylaThompson
manager: AnnBe
ms.date: 08/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261824
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 200b1a03a0ea95ec2d75850f9a8aebda966e38d6
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>Obnovení datového tržiště finančního vykazování po obnovení databáze

[!include[banner](../includes/banner.md)]


Toto téma popisuje, jak obnovit datový trh finančního výkaznictví po obnovení databázeMicrosoft Dynamics 365 for Finance and Operations.

Pokud někdy obnovíte databázi Finance and Operations ze zálohy nebo zkopírujete databázi z jiného prostředí, musíte postupovat podle kroků v tomto tématu, chcete-li zajistit, aby datové tržiště finančního vykazování správně používalo obnovenou databázi aplikace Finance and Operations. 
> [!Note] 
> Kroky v tomto procesu jsou podporovány pro vydání aplikace Dynamics 365 for Operations z května 2016 release (sestavení aplikace 7.0.1265.23014 a sestavení finančního výkaznictví 7.0.10000.4) a novější verze. Pokud máte dřívější verzi aplikace Finance and Operations, obraťte se na náš tým podpory pro pomoc.

## <a name="export-report-definitions"></a>Export definicí sestav
Nejprve exportujte návrhy sestavy z Návrháře sestav pomocí následujících kroků:

1.  V Návrháři sestav přejděte na **Společnost** &gt; **Skupiny stavebních bloků**.
2.  Vyberte skupinu stavebních bloků k exportu a klepněte na tlačítko **Export**. 

    > [!Note] 
    > V modulu Finance and Operations je podporována pouze jedna skupina stavebních bloků, **výchozí**.
    
3.  Vyberte definice sestavy k exportu:
    -   Pokud chcete exportovat všechny definice sestavy a přidružené stavební bloky, klikněte na tlačítko **Vybrat vše**.
    -   Pokud chcete exportovat konkrétní sestavy, řádky, sloupce, stromy či sady dimenzí, klikněte na příslušnou kartu a vyberte položky k exportu. Stisknutím a podržením klávesy Ctrl vyberte více položek na kartě. Při výběru sestav, které chcete exportovat, jsou vybrány přidružené řádky, sloupce, stromy a sady dimenzí.

4.  Klikněte na **Exportovat**.
5.  Zadejte název souboru a vyberte bezpečné místo, kam chcete uložit exportované definice sestavy.
6.  Klikněte na možnost **Uložit**.

Soubor lze zkopírovat nebo nahrát do bezpečného umístění, odkud ho lze později importovat do jiného prostředí. Informace o použití účtu úložiště Microsoft Azure naleznete v části [Přenos dat pomocí nástroje příkazového řádku AzCopy](/azure/storage/storage-use-azcopy). 
> [!NOTE]
> Microsoft neposkytuje úložiště účtu v rámci vaší smlouvy na aplikaci Finance and Operations. Musíte zakoupit účet úložiště nebo použít účet úložiště ze samostatného předplatného Azure. 
> [!WARNING]
> Musíte znát chování jednotky D na Azure Virtual Machines. Nenechávejte zde exportované stavební skupiny trvale. Další informace o dočasných jednotkách viz [Principy dočasné jednotky na Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>Ukončení služeb
Pomocí připojení ke vzdálené ploše se připojte ke všem počítačům v prostředí a zastavte následující služby systému Windows pomocí services.msc:

-   World wide web publishing service (na všech počítačích AOS)
-   Microsoft Dynamics 365 for Finance and Operations Batch Management Service (pouze na nesoukromých počítačích AOS)
-   Management Reporter 2012 Process Service (pouze v počítačích BI)

Tyto služby mají otevřené připojení k databázi Dynamics 365 for Finance and Operations.

## <a name="reset"></a>Resetovat
### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a>Vyhledejte a stáhněte nejnovější balíček MinorVersionDataUpgrade.zip

Vyhledejte nejnovější balíček MinorVersionDataUpgrade.zip pomocí pokynů v části [Stažení nejnovějšího nasaditelného balíčku pro upgrade dat](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages). Pokyny vysvětlují, jak najít a stáhnout správnou verzi balíčku pro upgradování dat. Upgrade ke stažení balíčku MinorVersionDataUpgrade.zip není vyžadován. Je zapotřebí dokončit kroky v části "Stažení nejnovějšího nasaditelného balíčku pro upgrade dat" bez provedení jakýchkoliv dalších kroků v článku pro načtení kopie balíčku MinorVersionDataUpgrade.zip.

### <a name="execute-scripts-against-finance-and-operations-database"></a>Spuštění skriptů proti databázi Finance and Operations

Spusťte následující skripty proti databázi Finance and Operations (nikoli proti databázi finančního výkaznictví).

-   DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Tyto skripty zkontrolujte správnost uživatelů, rolí a nastavení sledování změn.

### <a name="execute-powershell-command-to-reset-database"></a>Chcete-li obnovit databázi, spusťte příkaz prostředí PowerShell

V počítači AOS spusťte následující příkazy v nástroji PowerShell jako správce pro obnovení integrace mezi aplikací Finance and Operations a finančním výkaznictvím.

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail “<my reason for resetting>”

```
> [!NOTE]
> Po vykonání příkazu se zobrazí výzva k zadání Y pro potvrzení.

Vysvětlení parametrů:

-   Platné hodnoty parametru  -Reason jsou: SERVIS, CHYBNÁ DATA, JINÉ
-   Parametr -ReasonDetail je textový.
-   Parametry reason a reasonDetail budou zaznamenány ve sledování telemetrie/prostředí.

## <a name="start-services"></a>Spuštění služeb
Pomocí services.msc restartujte dříve zastavené služby:

-   World wide web publishing service (na všech počítačích AOS)
-   Microsoft Dynamics 365 for Finance and Operations Batch Management Service (pouze na nesoukromých počítačích AOS)
-   Management Reporter 2012 Process Service (pouze v počítačích BI)

## <a name="import-report-definitions"></a>Import definicí sestav
Importujte návrhy sestavy z Návrháře sestav pomocí souboru vytvořeného během exportu:

1.  V Návrháři sestav přejděte na **Společnost** &gt; **Skupiny stavebních bloků**.
2.  Vyberte skupinu stavebních bloků k exportu a klepněte na tlačítko **Export**. 

    > [!NOTE]
    > V modulu Finance and Operations je podporována pouze jedna skupina stavebních bloků, **výchozí**.
    
3.  Vyberte stavební blok **Výchozí** a klikněte na **Import**.
4.  Vyberte soubor obsahující definice exportované sestavy a klepněte na tlačítko **Otevřít**.
5.  V dialogovém okně Import vyberte definice sestavy k importu:
    -   Pokud chcete importovat všechny definice sestavy a podpůrné stavební bloky, klikněte na tlačítko **Vybrat vše**.
    -   Chcete-li importovat konkrétní sestavy, řádky, sloupce, stromy či sady dimenzí, vyberte sestavy, řádky, sloupce, stromy a sady dimenzí k importu.

6.  Klepněte na tlačítko **Import**.





