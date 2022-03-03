---
title: Náhled Dynamics 365 Supply Chain Management 10.0.25 (duben 2022)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Supply Chain Management 10.0.25.
author: kamaybac
ms.date: 02/01/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 8a9b873b7b4bba43b7b3e6e83c389ac35b4e223e
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/09/2022
ms.locfileid: "8102989"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10025-april-2022"></a>Náhled Dynamics 365 Supply Chain Management 10.0.25 (duben 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tohle téma uvádí funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Supply Chain Management verze Preview 10.0.25. Tato verze má číslo sestavení 10.0.1149 a je k dispozici následujícím způsobem:

- **Náhled vydané verze:** únor 2022
- **Obecně dostupné vydání (automatická aktualizace):** březen 2022
- **Obecně dostupné vydání (automatická aktualizace):** duben 2022

## <a name="features-included-in-this-release"></a>Funkce zahrnuté do této verze

V následující tabulce je uveden seznam funkcí této verze. Tohle téma můžeme aktualizovat, aby obsahovalo funkce, které se dostaly do sestavení poté, co bylo toto téma původně publikováno.

| Oblast funkce | Funkce | Další informace | Povolil/a   |
|---|---|---|---|
| Zásoby&nbsp;a&nbsp;logistika | Vylepšení nebezpečných materiálů | Tato vylepšení vycházejí ze stávající funkčnosti nebezpečných materiálů a pomáhají společnostem lépe dodržovat místní předpisy při přepravě nebezpečných materiálů v různých geografických oblastech. <!-- KFM: Update to 2022w1 link when published -->| Správa funkcí:<br>*Vylepšení nebezpečných materiálů* |
| Zásoby&nbsp;a&nbsp;logistika | Práce balení pro balicí stanice | Tato funkce výrazně zlepšuje flexibilitu a agilitu vašich balicích a přepravních operací. Během procesu balení mohou nyní skladníci balit a odesílat jednotlivé balíky, které se týkají stejné dodávky a nákladu. Řádky objednávek, které jsou součástí stejné dodávky, nemusejí být nutně odeslány společně, pokud jsou některé položky připraveny k odeslání ihned. Jedna objednávka může být zabalena a odeslána ve více dodávkách v různých dodacích lhůtách, čímž se zkrátí čekací doby a zvýší se agilita.<!-- KFM: Update to 2022w1 link when published --> | Správa funkcí:<br>*Práce balení pro balicí stanice* |
| Zásoby&nbsp;a&nbsp;logistika | [Skenování čárových kódů ve skladu pomocí standardů formátu GS1](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) <!-- KFM: Update to 2022w1 link when published --> | [QR kódy a čárové kódy GS1](../warehousing/gs1-barcodes.md) | Správa funkcí:<br>*Naskenovat čárové kódy GS1* |
| Výroba | [Spotřeba materiálu a rezervace v rozhraní pro provádění výrobního provozu](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/material-consumption-reservations-production-floor-execution-interface) | [Jak pracovníci používají rozhraní pro provádění výrobního provozu](../production-control/production-floor-execution-use.md) | Správa funkcí:<br>*(Preview) Registrace spotřeby materiálu na rozhraní pro provádění výrobního provozu (s povoleným WMS)* |
| Výroba | [Registrovat spotřebu materiálu v jednotce škálování](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/register-material-consumption-scale-units) | [Pracovní zátěž spouštění výroby pro jednotky škálování cloudu a hraniční sítě](../cloud-edge/cloud-edge-workload-manufacturing.md) | Správa funkcí:<br>*Registrovat spotřebu materiálu v mobilní aplikaci na jednotce škálování* |
| Plánování | [Návrhy optimalizace plánování pro optimalizaci stávající nabídky](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-suggestions-optimize-existing-supply) | [Zprávy akce](../master-planning/action-messages.md) | Ve výchozím nastavení povoleno |
| Plánování | Zjednodušené plánované objednávky | [Zjednodušené plánované objednávky](../master-planning/planning-optimization/planned-orders-simplified.md ) | Správa funkcí:<br>*Zjednodušené plánované objednávky* |

## <a name="feature-enhancements-included-in-this-release"></a>Vylepšení funkcí zahrnutých do této verze

V následující tabulce je uveden seznam vylepšených funkcí této verze. Každé z těchto vylepšení poskytuje přírůstkové vylepšení stávající funkce. Protože se jedná pouze o vylepšení, nejsou uvedeny v seznamu [plán vydání](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Aby se však zajistilo, že tato vylepšení nebudou v rozporu s vašimi stávajícími přizpůsobeními nebo předvolbami, je každé z nich ve výchozím nastavení vypnuto (pokud není uvedeno jinak).

Pokud chcete zapnout nebo vypnout některou z těchto funkcí, musíte to udělat ve [správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Název funkce ve správě funkcí | Další informace |
|---|---|---|
| Řízení zásob a skladu | (Polsko) Umožnit propojení několika faktur SAD na jeden řádek nákupní objednávky v jednom SAD | Tato funkce umožňuje rozdělit řádky nákupní objednávky a propojit je s jedním administrativním dokladem (SAD), pokud byly tyto řádky nákupní objednávky zaúčtovány pro několik různých faktur (například pro různé dodávky). |
| Zásobování a zdroje | Konsolidovat více nákupních žádanek do jedné nákupní objednávky podle účetního data | Tato funkce umožňuje sloučit více nákupních žádanek do jedné nákupní objednávky, pokud mají nákupní žádanky různá účetní data. Pravidla nákupní politiky pro vytváření nákupních objednávek a konsolidaci poptávky lze nastavit tak, aby bylo automatizováno rozhodování o seskupování řádků žádanky podle účetního data na úrovni nákupní objednávky. Konsolidace nákupních objednávek podle účetního data není podporována, pokud je povoleno řízení rozpočtu, protože účetní datum se používá pro rozpočtové rezervace a břemeno. Proto by mělo být uchováno během přechodu z nákupní žádanky na nákupní objednávku. |
| Zásobování a zdroje | Zobrazit starší výchozí nastavení pole odpovědi na RFQ | Tato funkce znovu zavádí starší výchozí pole odpovědi na požadavku na nabídku (RFQ), která byla dříve z uživatelského rozhraní odstraněna. Tato nastavení neposkytují žádné funkce implicitně, ale lze je upravit podle potřeby. Povolte tuto funkci, pokud vaše organizace již přidala funkce pro výchozí nastavení polí odpovědi na RFQ nebo to plánuje. Když je tato funkce povolena, můžete přistupovat k nastavení přechodem na stránku **Parametry modulu Zásobování a zdroje**, kde otevřete kartu **Žádost o cenovou nabídku** a zvolíte **Výchozí pole odpovědí v požadavku na nabídku**. |
| Zásobování a zdroje | Sloučit finanční dimenze dodavatele s finanční dimenzí aktivního propojení dimenzí na nákupní objednávce | Tato funkce umožňuje sloučit finanční dimenze od dodavatelů s aktivními finančními dimenzemi propojení dimenze po schválení nákupní žádanky, pokud nastavíte propojení mezi finanční dimenzí a dimenzí skladových zásob. Pravidla nákupní politiky pro vytváření nákupních objednávek a konsolidaci poptávky lze nastavit tak, aby řídila rozhodnutí o sloučení finančních dimenzí od dodavatelů s aktivní finanční dimenzí propojení dimenzí na úrovni hlavičky nákupní objednávky. |
| Řízení výroby | (Rusko) Povolit nastavení výchozího umístění pro výrobní receptury nebo kusovník a automatickou rezervaci GTD nebo spotřebu ve výrobě | Tato funkce umožňuje další možnosti výroby z importovaných surovin (pouze ruská lokalizace):<ul><li>Možnost nastavit automatické výchozí umístění pro výrobní receptury a kusovníky ve skupinách zdrojů i ve skladech.</li><li>Automatická rezervace surovin podle dimenze *Číslo GTD* dimenze ve skladech s aktivovaným WMS podle rezervačního algoritmu, který není WMS. To platí v případech, kdy existuje zásada práce pro *Výdej suroviny* s **Metodou tvorby práce** nastavenou na *Nikdy*, jejíž nastavení skladu, umístění a čísla položky odpovídá inventárním transakcím výrobní zakázky (dávky).</li><li>Automatická spotřeba surovin podle dimenze *Číslo GTD* při zaúčtování výdejky, podle výše popsané pořízené rezervace.</li></ul> |
| Řízení skladu | (Náhled) Podpora jednotky škálování pro příchozí a odchozí objednávky skladu | Tato funkce způsobí, že systém vytvoří odchozí skladové objednávky během procesu uvolnění do skladu a vytvoří příchozí skladové objednávky, když jsou převodní příkazy zaúčtovány jako odeslané. Systém pak synchronizuje každou příchozí nebo odchozí skladovou objednávku s jednotkou škálování odpovědnou za odeslání nebo přijetí objednávky. Všimněte si, že po povolení této funkce je nutné upgradovat vaše prováděcí úlohy skladu. Další informace naleznete v části [Pracovní zatížení pro jednotky škálování cloudu a hraniční sítě](../cloud-edge/cloud-edge-workload-warehousing.md).<br><br>Tato funkce vyžaduje funkci *Odpojit odloženou práci od ASN* a umožní možnost přijímat převodní příkazy pomocí procesu příjmu registrační značky v mobilní aplikaci Warehouse Management. |

## <a name="feature-state-changes-in-this-release"></a>Změny stavu funkcí v této verzi

V následující tabulce je uveden seznam funkcí, které jsou počínaje vydáním 10.0.25 povinné nebo ve výchozím nastavení zapnuté. Všechny tyto funkce se pro váš systém automaticky zapnou, jakmile provedete aktualizaci na verzi 10.0.25. Povinné funkce nelze vypnout, ale funkce, které jsou ve výchozím nastavení zapnuté, lze stále vypnout ve [Správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Tabulka také uvádí funkce, které byly dříve ve veřejném preview, ale změnily se tak, aby byly obecně dostupné ve vydání 10.0.25, což znamená, že jsou nyní doporučeny k použití v produkčních prostředích. Tyto funkce jsou ve výchozím nastavení vypnuty, pokud není uvedeno jinak, takže je musíte ve [Správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) povolit, abyste je m,ohli používat.

| Modul | Název funkce | Stav funkce |
| --- | --- | --- |
| Správa majetku | [Použít pravidla pro seskupování pracovních příkazů při provádění plánu údržby](../asset-management/preventive-and-reactive-maintenance/creating-work-orders.md) | Obecně dostupné |
| Správa majetku | [Vylepšení údržby na základě čítače](../asset-management/preventive-and-reactive-maintenance/maintenance-plans.md) | Obecně dostupné |
| Správa nákladů | [Úroveň výpočtu nákladů](../cost-management/cost-calculation-level.md) | Obecně dostupné |
| Správa nákladů | Povolit nastavení čísla dávky definované uživatelem pro storno uzávěrky zásob | Obecně dostupné |
| Správa nákladů | [Podrobnosti o průběhu uzávěrky zásob](whats-new-scm-10-0-21.md) | Obecně dostupné |
| Správa nákladů | [Možnosti výchozích finančních dimenzí pro přecenění standardních nákladů na zásoby](../cost-management/manage-standard-cost-updates.md) | Obecně dostupné |
| Správa nákladů | Vyčištění dat výkazu hodnoty zásob | Zapnuto ve výchozím nastavení |
| Správa nákladů | [Úložiště sestavy hodnot zásob](../cost-management/inventory-value-report-storage.md) | Zapnuto ve výchozím nastavení |
| Správa nákladů | Zobrazit protokol uzávěrky zásob v mřížce | Zapnuto ve výchozím nastavení |
| Správa technických změn | [Povolení správy změn u stávajících produktů](../engineering-change-management/change-management-existing-products.md) | Zapnuto ve výchozím nastavení |
| Správa technických změn | [Správa technických změn](../engineering-change-management/product-engineering-overview.md) | Zapnuto ve výchozím nastavení |
| Správa technických změn | [Technická oznámení pro výrobu](../engineering-change-management/engineering-change-management.md) | Zapnuto ve výchozím nastavení |
| Správa technických změn | [Vylepšená dědičnost atributů pro Řízení technických změn](../engineering-change-management/engineering-attributes-and-search.md) | Zapnuto ve výchozím nastavení |
| Správa technických změn | [Spravujte změny v recepturách a jejich látkách](../engineering-change-management/manage-formula-changes.md) | Zapnuto ve výchozím nastavení |
| Správa technických změn | [Kontroly připravenosti produktu](../engineering-change-management/product-readiness.md) | Zapnuto ve výchozím nastavení |
| Správa technických změn | [Generování varianty pro technické produkty](../engineering-change-management/engineering-variants.md) | Zapnuto ve výchozím nastavení |
| Řízení zásob a skladu | Navigace do verze kusovníku z řádků kusovníku | Povinné |
| Hlavní plánování | [Dávkové potvrzení a konsolidace pro plánované hromadné a balíkové dávkové objednávky](whats-new-scm-10-0-20.md) | Obecně dostupné |
| Hlavní plánování | Plánování zdrojů s údržbou | Obecně dostupné |
| Hlavní plánování | Povolení funkcí průvodce nastavení hlavního plánu | Povinné |
| Hlavní plánování | [Výběr modelu prognózy v podrobnostech prognózy poptávky](../master-planning/manual-adjustments-baseline-forecast.md) | Povinné |
| Hlavní plánování | [Znázornění průběhu hlavního plánování](../master-planning/tasks/monitor-master-planning-run.md) | Povinné |
| Hlavní plánování | [Paralelní potvrzování plánovaných objednávek](../master-planning/planning-optimization/planned-order-firming.md) | Povinné |
| Hlavní plánování | [Potvrzení plánované objednávky s filtrováním](../master-planning/planning-optimization/planned-order-firming.md) | Zapnuto ve výchozím nastavení |
| Hlavní plánování | [Uložená zobrazení pro plánované objednávky](saved-views-scm.md) | Zapnuto ve výchozím nastavení |
| Zásobování a zdroje | Zakázat tlačítko resetování distribuce nákupní žádanky | Obecně dostupné |
| Zásobování a zdroje | [Povolit resetování pracovních postupů souvisejících se zásobováním](whats-new-scm-10-0-20.md) | Obecně dostupné |
| Zásobování a zdroje | Možnost dávkového potvrzení přijatých nákupních objednávek z dodavatelské spolupráce | Povinné |
| Zásobování a zdroje | Uzavřený stav nákupní smlouvy | Povinné |
| Zásobování a zdroje | Přidat řádky k fakturám nákupních objednávek přidruženým k nákupní smlouvě | Zapnuto ve výchozím nastavení |
| Zásobování a zdroje | Přidat pole Objednané množství na stránku Zaúčtování příjemky produktu | Zapnuto ve výchozím nastavení |
| Zásobování a zdroje | [Umožnit dodavatelům žádat o kategorie zásobování prostřednictvím spolupráce s dodavateli](../procurement/category-requests-from-vendors.md) | Zapnuto ve výchozím nastavení |
| Zásobování a zdroje | Částky poplatků od a do na nákupních objednávkách | Zapnuto ve výchozím nastavení |
| Zásobování a zdroje | Nastavení poplatků s pracovištěm a skladem | Zapnuto ve výchozím nastavení |
| Zásobování a zdroje | Povolit výpočet dovozního cla na základě ročního tarifu | Zapnuto ve výchozím nastavení |
| Zásobování a zdroje | [Odpovědná strana nákupní smlouvy](../procurement/purchase-agreements.md) | Zapnuto ve výchozím nastavení |
| Zásobování a zdroje | [Uložená zobrazení pro nákupní objednávky](saved-views-scm.md) | Zapnuto ve výchozím nastavení |
| Správa informací o produktech | [Striktní ověření výchozího množství objednávky](../production-control/default-order-settings.md) | Povinné |
| Správa informací o produktech | Kusovník předzpracovává sestavy, aby nedošlo k vypršení časového limitu | Zapnuto ve výchozím nastavení |
| Správa informací o produktech | Výchozí finanční dimenze samostatně při použití šablon položek | Zapnuto ve výchozím nastavení |
| Správa informací o produktech | Povolit skupiny dimenzí produktů pro šablony položek | Zapnuto ve výchozím nastavení |
| Správa informací o produktech | Opětovně vygenerovat názvy variant produktů na základě názvosloví | Zapnuto ve výchozím nastavení |
| Správa informací o produktech | [Vylepšení stránky návrhů variant](../pim/tasks/create-predefined-product-variants.md) | Zapnuto ve výchozím nastavení |
| Řízení výroby | Vylepšený výdej množství skutečné hmotnosti produkce | Obecně dostupné |
| Řízení výroby | Na stránku terminálu úkolových lístků bylo přidáno nové tlačítko Ukončit přestávku | Povinné |
| Řízení výroby | [Povolit automatické generování čísla registrační značky při vykazování jako dokončeno v zařízení úkolového lístku](../production-control/production-floor-execution-configure.md) | Povinné |
| Řízení výroby | Povolení částečného příjmu subdodavatelských položek a oprava problému s výpočtem odpadu pro řádky kusovníku typu dodavatele | Povinné |
| Řízení výroby | [Funkce pro uzamčení zařízení úkolového lístku a terminálu úkolových lístků za účelem dezinfekce](../production-control/production-floor-execution-configure.md) | Povinné |
| Řízení výroby | Vylepšení dialogových oken Úlohy schválení a Úlohy převodu | Povinné |
| Řízení výroby | [Registrační značka pro vykazování jako dokončené přidána do zařízení úkolového lístku](../production-control/production-floor-execution-configure.md) | Povinné |
| Řízení výroby | [Vytisknout štítek ze zařízení úkolového lístku](../production-control/production-floor-execution-configure.md) | Povinné |
| Řízení výroby | [Provádění výrobního provozu](../production-control/production-floor-execution-configure.md) | Povinné |
| Řízení výroby | [Funkce správy majetku pro rozhraní provádění výrobního provozu](../production-control/production-floor-execution-configure.md) | Zapnuto ve výchozím nastavení |
| Řízení výroby | [Vyhledávání práce pro rozhraní ke spuštění výrobního provozu](../production-control/production-floor-execution-configure.md) | Zapnuto ve výchozím nastavení |
| Řízení výroby | [Přepsat výchozí rezervaci výroby](../production-control/override-default-reservation-principle.md) | Zapnuto ve výchozím nastavení |
| Řízení výroby | [Zobrazit celé sériové číslo, číslo dávky a registrační značku v rozhraní provádění výrobního provozu](whats-new-scm-10-0-21.md) | Zapnuto ve výchozím nastavení |
| Prodej a marketing | [Vylepšení výkonu podrobností prodejní objednávky](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-details-performance-enhancement) | Obecně dostupné |
| Prodej a marketing | Vylepšení výkonu podrobností prodejní nabídky | Obecně dostupné |
| Prodej a marketing | Zásady exportu dat odkazující na prodejní objednávku | Povinné |
| Prodej a marketing | [Zásady odstranění řádku prodejní objednávky propojeného s řádkem nákupní objednávky](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-purchase-order-line-deletion-policy) | Povinné |
| Prodej a marketing | [Zásady exportu dat odkazující na prodejní nabídku](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy)| Povinné |
| Prodej a marketing | [Optimalizace exportu datové entity kontaktní osoby](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization) | Zapnuto ve výchozím nastavení |
| Prodej a marketing | Povolit vyhledávání polí úvodu a závěru dokumentu prodejní nabídky | Zapnuto ve výchozím nastavení |
| Prodej a marketing | [Zlepšit výkonnost sestavy „Prvních 100“ zákazníků](whats-new-scm-10-0-23.md) | Zapnuto ve výchozím nastavení |
| Prodej a marketing | Přepočítat odhadovaný zůstatek zákazníka | Zapnuto ve výchozím nastavení |
| Prodej a marketing | [Registrace řádků vratky prodeje s desetinnou přesností se skutečnou hmotností a bez ní](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight) | Zapnuto ve výchozím nastavení |
| Prodej a marketing | [Uložená zobrazení pro prodej a marketing](saved-views-scm.md) | Zapnuto ve výchozím nastavení |
| Prodej a marketing | Potvrzení prodejní objednávky jediným kliknutím | Zapnuto ve výchozím nastavení |
| Řízení skladu | [Šablony cross dockingu se směrnicemi skladového místa](../warehousing/planned-cross-docking.md) | Obecně dostupné |
| Řízení skladu | [Zakázat očekávané příjmy z objednávek kvality, které slouží pro pořízení vzorku blokovaných zásob](../inventory/inventory-blocking.md) | Obecně dostupné |
| Řízení skladu | Historie přijetí registrační značky | Obecně dostupné |
| Řízení skladu | [Rozhraní vybavení manipulace s materiálem](../warehousing/mhax.md) | Obecně dostupné |
| Řízení skladu | [Zaokrouhlit množství dolů na nejbližší prodejní jednotku při uvolnění do skladu](whats-new-scm-10-0-19.md) | Obecně dostupné |
| Řízení skladu | Podpora jednotek škálování pro seznamy prací skladové aplikace | Obecně dostupné |
| Řízení skladu | Podrobnosti štítku vlny dodávky | Obecně dostupné |
| Řízení skladu | [Použijte rychlejší rozhraní API pro zavírání/opětovné otevírání kontejnerů na balicí stanici](whats-new-scm-10-0-21.md) | Obecně dostupné |
| Řízení skladu | [Ověřit šablony vybrané pro práci doplnění](whats-new-scm-10-0-20.md) | Obecně dostupné |
| Řízení skladu | Povolit šabloně doplnění použít existující práci okamžitého doplnění (napříč jednotkami) | Povinné |
| Řízení skladu | Automatické přiřazení GUID při vytváření uživatelů WHS | Povinné |
| Řízení skladu | Zaznamenat varianty produktu a sledovací dimenze ve skladové aplikaci při příjmu položky vytížení | Povinné |
| Řízení skladu | [Změnit stav zásob položek kontrolovaných sledovacími dimenzemi](../inventory/inventory-statuses.md) | Povinné |
| Řízení skladu | [Změnit fond práce u práce](../warehousing/change-work-pool-on-work.md) | Povinné |
| Řízení skladu | [Plná pozice seskupení](../warehousing/cluster-position-full.md) | Povinné |
| Řízení skladu | [Funkce odložení seskupení](../warehousing/putaway-clusters.md) | Povinné |
| Řízení skladu | [Potvrdit a převést](../warehousing/confirm-and-transfer.md) | Povinné |
| Řízení skladu | [Potvrdit odchozí dodávky z dávkových úloh](../warehousing/confirm-outbound-shipments-from-batch-jobs.md) | Povinné |
| Řízení skladu | [Určit zda se má na mobilních zařízeních zobrazit stránka se souhrnem příjmu](../warehousing/warehousing-mobile-device-app-license-plate-receiving.md) | Povinné |
| Řízení skladu | [Odložené zpracování ruční operace přesunu zásob](../warehousing/deferred-processing-manual-inventory-movement.md) | Povinné |
| Řízení skladu | Nepovolujte vytváření nákladů, které nesplňují požadavky šablony sestavení vytížení vlny | Povinné |
| Řízení skladu | [Vylepšené rozvržení popisků registračních značek](../warehousing/document-routing-layout-for-license-plates.md) | Povinné |
| Řízení skladu | [Vyhodnocení všech akcí pro směrnice umístění více SKU](../troubleshooting/warehousing/evaluate-multiple-location-directive-actions.md) | Povinné |
| Řízení skladu | Skrýt pole Celková hodnota na stránkách Všechny náklady a Podrobnosti o nákladu | Povinné |
| Řízení skladu | Konfigurace sestavení popisků registračních značek | Povinné |
| Řízení skladu | Ruční oprava řádku vytížení pro správce nebo podobné důvěryhodné uživatele | Povinné |
| Řízení skladu | [Umístění registrační značky místa](../warehousing/location-license-plate-positioning.md) | Povinné |
| Řízení skladu | [Směšování dimenzí produktu na skladovém místě](../warehousing/location-product-dimension-mixing.md) | Povinné |
| Řízení skladu | Udělat pole stavu zásob pohybu zásob mobilního zařízení upravitelným | Povinné |
| Řízení skladu | Služba ručního výdeje řádku prodeje pro správce nebo podobné důvěryhodné uživatele | Povinné |
| Řízení skladu | [Zabránit použití registračních značek odeslaných převodním příkazem na jiných skladech než je cílový sklad](../warehousing/warehousing-mobile-device-app-license-plate-receiving.md) | Povinné |
| Řízení skladu | Vyzvat k vyřešení nejednoznačných názvů 'Loc / LP' | Povinné |
| Řízení skladu | [Kontrola kvality](../warehousing/quality-check.md) | Povinné |
| Řízení skladu | [Uživatelská nastavení, ikony a názvy kroků pro novou skladovou aplikaci](../warehousing/install-configure-warehouse-management-app.md) | Povinné |
| Řízení skladu | [Další zóna skladového místa](../warehousing/additional-location-zones.md) | Zapnuto ve výchozím nastavení |
| Řízení skladu | [Vytvářet a zpracovat převodní příkazy z aplikace skladu](../warehousing/create-transfer-order-from-warehouse-app.md) | Zapnuto ve výchozím nastavení |
| Řízení skladu | Povolit rychlé ověření pro mobilních zařízení ve skladu | Zapnuto ve výchozím nastavení |
| Řízení skladu | [Maximální doba provedení pro úlohu čištění položek zásob na skladě v řízení skladu](../warehousing/onhand-cleanup.md) | Zapnuto ve výchozím nastavení |
| Řízení skladu | [Vizualizace odchozí úlohy](../warehousing/outbound-workload-visualization.md) | Zapnuto ve výchozím nastavení |
| Řízení skladu | [Zpracovat události aplikace skladu](../warehousing/warehouse-app-events.md) | Zapnuto ve výchozím nastavení |
| Řízení skladu | [Uložené zobrazení pro pracovní plochu plánování vytížení](saved-views-scm.md) | Zapnuto ve výchozím nastavení |
| Řízení skladu | [Uložené zobrazení stránky s podrobnostmi o práci](saved-views-scm.md) | Zapnuto ve výchozím nastavení |
| Řízení skladu | [Uložené zobrazení pro zpracování vlny](saved-views-scm.md) | Zapnuto ve výchozím nastavení |
| Řízení skladu | [Uložená zobrazení pro zpracování vytížení](saved-views-scm.md) | Zapnuto ve výchozím nastavení |
| Řízení skladu | [Uložená zobrazení pro zpracování dodávky](saved-views-scm.md) | Zapnuto ve výchozím nastavení |
| Řízení skladu | [Podrobnosti dávkové úlohy vlny](../warehousing/wave-processing.md) | Zapnuto ve výchozím nastavení |
| Řízení skladu | [Oznámení o provedení vlny](../warehousing/wave-execution-notifications.md) | Zapnuto ve výchozím nastavení |

## <a name="additional-resources"></a>Další prostředky

### <a name="platform-updates-for-finance-and-operations-apps"></a>Aktualizace platformy pro finanční a provozní aplikace

Microsoft Dynamics 365 Supply Chain Management 10.0.25 zahrnuje aktualizace platformy. Další informace naleznete v tématu [Aktualizace platformy pro verze 10.0.25 finančních a provozních aplikací (duben 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-25.md).

### <a name="bug-fixes"></a>Opravy chyb

Sháníte-li informace o opravách chyb zahrnutých v jednotlivých aktualizacích, které jsou součástí verze 10.0.25, přihlaste se ke službám Lifecycle Services (LCS) a přečtěte si [článek znalostní báze](https://fix.lcs.dynamics.com/Issue/Details?bugId=654580&dbType=3&qc=3799fa965b008dd980d27cf740e4582e6384ec6601ae8a35b7eaec6f1287a868).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 a průmyslová cloudová řešení: Plán vlny 1 vydání 2022

Zajímáte se o nadcházející a nedávno uvedené funkce jakékoliv z našich obchodních aplikací nebo platforem?

Přečtěte si [Dynamics 365 a průmyslová cloudová řešení: Plán vlny 1 vydání 2022](/dynamics365-release-plan/2022wave1/). Popsali jsme všechny podrobnosti, od A až do Z, v jednom dokumentu, který můžete používat pro plánování.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Odebrané a zastaralé funkce Supply Chain Management

Téma [Odebrané nebo zastaralé funkce v Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) popisuje funkce Supply Chain Management, které byly nebo jsou naplánovány k odebrání nebo které zastaraly.

- *Odstraněná* funkce již není k dispozici v produktu.
- *Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Před odebráním jakékoli funkce produktu bude oznámeno její zastarání v tématu [Odebrané nebo zastaralé funkce v Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 měsíců před odebráním.

U změn způsobujícíh chyby, které ovlivní pouze dobu kompilace, ale jsou v binárním formátu kompatibilní s prostředím sandbox a produkčními prostředími, bude doba zastarání kratší než 12 měsíců. Obvykle se jedná o funkční aktualizace, které je třeba provést v kompilátoru.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
