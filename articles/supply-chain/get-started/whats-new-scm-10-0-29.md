---
title: Preview verze Dynamics 365 Supply Chain Management 10.0.29 (říjen 2022)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Supply Chain Management 10.0.29.
author: kamaybac
ms.date: 08/12/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 62e06f2348ca3524beaaef5d8879c199db56696f
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689276"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10029-october-2022"></a>Co je nového nebo co se změnilo v aplikaci Dynamics 365 Supply Chain Management 10.0.29 (říjen 2022)

[!include [banner](../includes/banner.md)]

Tento článek uvádí funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Supply Chain Management verze 10.0.29. Tato verze má číslo sestavení 10.0.1326 a je k dispozici podle následujícího plánu:

- **Preview verze:** Srpen 2022
- **Obecně dostupné vydání (automatická aktualizace):** Září 2022
- **Obecně dostupné vydání (automatická aktualizace):** Říjen 2022

## <a name="features-included-in-this-release"></a>Funkce zahrnuté do této verze

V následující tabulce je uveden seznam funkcí této verze. Tento článek můžeme aktualizovat, aby obsahoval funkce, které se dostaly do sestavení poté, co byl tento článek původně publikován.

| Oblast funkce | Funkce | Další informace | Povolil/a |
|---|---|---|---|
| Zásoby a logistika | [Přidělení a rezervace položek WMS ve viditelnosti zásob](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/allocate-reserve-whs-items-inventory-visibility) | Již brzy | Ve výchozím nastavení povoleno |
| Zásoby a logistika | [Přednačtení přehlednější v seznamech zásob na skladě](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/query-inventory-visibility-summary-entity) | [Použití aplikace Inventory Visibility](../inventory/inventory-visibility-power-platform.md) | Aktivováno konfigurací služeb |
| Automatizace dodávek na zakázku | [Automatizace dodávek na zakázku](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-to-order-supply-automation) | [Automatizace dodávek na zakázku](../master-planning/make-to-order-supply-automation.md) | Správa funkcí:<br>*Automatizace dodávek na zakázku* |
| Plánování | [Zobrazení a použití podrobných přehledů pro DDMRP](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/view-apply-detailed-insights-ddmrp) | [Plánování materiálových požadavků řízené poptávkou – přehled](../master-planning/planning-optimization/ddmrp-overview.md) | Správa funkcí:<br>*(Preview) DDMRP pro optimalizaci plánování* |
| Řízení výroby | [Zpřístupnění hotového zboží fyzicky před odesláním do deníků](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-finished-goods-physically-before-posting) | [Zpřístupnění hotového zboží fyzicky před odesláním do deníků](../production-control/deferred-posting.md) | Správa funkcí:<br>*(Preview) Před odesláním do deníků zpřístupněte hotové výrobky fyzicky* |
| Řízení skladu | [Vyhledání relevantních dat v Warehouse mobile app](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/look-up-relevant-data-within-warehouse-mobile-app) | [Dotazování na data pomocí obcházení mobilní aplikace Warehouse Management](../warehousing/warehouse-app-data-inquiry.md) | Správa funkcí:<br>*Tok zjištění dat aplikace Warehouse Management* |

## <a name="feature-enhancements-included-in-this-release"></a>Vylepšení funkcí zahrnutých do této verze

V následující tabulce je uveden seznam vylepšených funkcí této verze. Každé z těchto vylepšení poskytuje přírůstkové vylepšení stávající funkce. Protože se jedná pouze o vylepšení, nejsou uvedeny v seznamu [plán vydání](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Aby se však zajistilo, že tato vylepšení nebudou v rozporu s vašimi stávajícími přizpůsobeními nebo předvolbami, je každé z nich ve výchozím nastavení vypnuto (pokud není uvedeno jinak).

Pokud chcete zapnout nebo vypnout některou z těchto funkcí, musíte to udělat ve [správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Název funkce ve správě funkcí | Další informace |
|---|---|---|
| Správa nákladů | Optimalizace cenové kalkulace vedlejších produktů čekajících na vyřízení | Tato funkce opravuje konflikt, který může někdy nastat při výpočtu cen vedlejších produktů pomocí více vláken. Způsobí to, že systém zajistí, aby se každá cena vedlejšího produktu vypočítávala pouze jednou. Výsledek tohoto výpočtu se pak použije jako vstup pro všechny ostatní výpočty. Pokud již čekající cena existuje, použije se tato cena. |
| Hlavní plánování | Seskupit transakce v optimalizaci plánování | Tato funkce může pomoci snížit počet plánovaných objednávek, které se generují pro dodání jednoho řádku prodejní objednávky, když používáte optimalizaci plánování. Když je tato funkce zapnutá, optimalizace plánování seskupí všechny transakce zásob pro řádek objednávky do jediného požadavku na celé množství. (Toto chování odpovídá chování integrovaného plánovacího nástroje.) Nabídka a poptávka jsou seskupeny samostatně. Funkce proto pomáhá snížit objem transakcí, když máte rozdělené transakce a když používáte dimenze (jako jsou čísla šarží nebo sériová čísla), které nejsou dimenzemi pokrytí. |
| Zásobování a zdroje | Zablokování dodavatele pro nákupní objednávky | Tato funkce vám umožňuje pozastavit dodavatele pro nákupní objednávky. Přidává nový typ pozastavení *Nákupní objednávka*, který označí dodavatele jako pozastaveného pro nákupní objednávky. Nebudete moci vytvářet nové nákupní objednávky pro dodavatele, kteří jsou kvůli objednávkám pozastaveni, ale stále budete moci pokračovat se všemi otevřenými fakturami nebo platbami pro tyto dodavatele. |
| Prodej a marketing | Vypočítat čistou částku řádku při importu | Tato funkce vám umožňuje řídit, zda má systém přepočítat součty řádků, když importujete data přes entitu *Řádky prodejní objednávky*, *Řádky prodejní nabídky* nebo *Řádky objednávky vrácení* používající OData nebo duální zápis. Má to účinek pouze tehdy, když máte také zavedeny zásady hodnocení obchodních smluv, které omezují změny na pole **Čistá částka** pro řádky prodejní objednávky, řádky prodejní nabídky a řádky návratové objednávky. Přidává nastavení s názvem **Vypočítat čistou částku řádku** na stránku **Pohledávky > Nastavení > Parametry pohledávek**. Když je toto nastavení nastaveno na *Ano*, systém v případě potřeby vždy přepočítá částky řádku (a ignoruje tak jakoukoli politiku hodnocení obchodních dohod pro čistou částku řádku). Když je nastavení nastaveno na *Ne*, systém nikdy automaticky nevypočítá čistou částku řádku, i když by příchozí změny ceny řádku, množství nebo slevy znamenaly, že by se měla čistá částka řádku přepočítat. Tato funkce je ve výchozím nastavení aktivní a nastavuje **Vypočítat čistou částku řádku** na *Ano*. Nastavení *Ne* odpovídá chování systému před verzí 10.0.23 a je poskytováno především pro podporu starších scénářů integrace.<br><br>Více informací viz [Přepočítat čisté částky řádku při importu prodejních objednávek, nabídek a vratek](../sales-marketing/calc-line-net-amounts-import.md). |
| Prodej a marketing | Vypočítat celkové prodeje pomocí více vláken | Tato funkce pomáhá zlepšit výkon tím, že umožňuje systému používat paralelní zpracování při výpočtu celkových prodejů v dávce. Funkce přidává nové pole **Počet vláken** k dialogovému oknu **Vypočítat součty prodeje**. Pokud se rozhodnete spustit výpočet v dávce, můžete toto pole použít k nastavení maximálního počtu vláken. Pokud nastavíte hodnotu na *0* (nula) nebo *1*, bude použito jediné vlákno. Hodnoty nad 1 umožňují vícevláknové zpracování. |
| Prodej a marketing | Aktualizovat ceny a slevy zadané ručně pro mezipodnikové objednávky | Tato funkce přidává podporu pro zásady ruční změny pro mezipodnikové objednávky. Zahrnuje podporu pro přenos zásad manuální změny mezi mezipodnikovými prodejními a nákupními objednávkami. Dříve byly zásady ruční změny podporovány pouze u objednávek mimo společnost. Když je tato funkce povolena, systém vám dá možnost aktualizovat ceny a slevy po uložení změn v mezipodnikové objednávce. Tato možnost vám umožňuje vybrat, zda chcete na vnitropodnikovou objednávku použít nové údaje o cenách a slevách, nebo objednávku ponechat beze změny. |

## <a name="new-and-updated-documentation-resources"></a>Nové a aktualizované zdroje dokumentace

Nedávno jsme přidali nebo významně aktualizovali následující články nápovědy. Tento článek nemusí nutně souviset s novými funkcemi, které byly přidány pro toto vydání, jak je uvedeno v předchozích částech. Mohou vám však pomoci lépe využít stávající funkce.

| Oblast funkce | Nové nebo aktualizované články |
|---|---|
| Hlavní plánování, CTP | [Výpočet dat dodání prodejní objednávky pomocí CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md) |
| Hlavní plánování, DDMRP | [Plánování materiálových požadavků řízené poptávkou – přehled](../master-planning/planning-optimization/ddmrp-overview.md)<br>[Zapnutí funkce DDMRP ve vašem systému](../master-planning/planning-optimization/ddmrp-enable.md)<br>[Umístění zásob](../master-planning/planning-optimization/ddmrp-inventory-positioning.md)<br>[Profil a úrovně vyrovnávacích zásob](../master-planning/planning-optimization/ddmrp-buffer-profile-and-levels.md)<br>[Plánování řízené poptávkou](../master-planning/planning-optimization/ddmrp-planning.md)<br>[Vizuální a společné provádění](../master-planning/planning-optimization/ddmrp-visual-and-collaborative-execution.md) |
| Řízení skladu | [Balení kontejnerů pro dodávku](../warehousing/packing-containers.md)<br>[Balicí práce pro balení odchozích kontejnerů a zpracování zásilek](../warehousing/packing-work.md) |

## <a name="feature-state-changes-in-this-release"></a>Změny stavu funkcí v této verzi

V následující tabulce je uveden seznam funkcí, které jsou počínaje verze 10.0.29 povinné nebo ve výchozím nastavení zapnuté. Všechny tyto funkce se pro váš systém automaticky zapnou, jakmile provedete aktualizaci na verzi 10.0.29. Povinné funkce nelze vypnout, ale funkce, které jsou ve výchozím nastavení zapnuté, lze stále vypnout ve [Správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Tabulka také uvádí funkce, které byly dříve v Public Preview, ale změnily se tak, aby byly obecně dostupné ve verzi 10.0.29. Tato změna znamená, že funkce jsou nyní doporučeny pro použití v produkčních prostředích. Tyto funkce jsou ve výchozím nastavení vypnuté, pokud není uvedeno jinak. Pokud je chcete použít, musíte je výslovně povolit ve [Správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Název funkce | Nový stav funkce |
| --- | --- | --- |
| Správa majetku | [Funkce správy majetku pro rozhraní provádění výrobního provozu](../production-control/production-floor-execution-configure.md) | Povinné |
| Správa nákladů | [Změnit popisek zrušení v uzávěrce a úpravě pro stornování](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/change-terminology-inventory-closing-cancellation-inventory-closing-reverse) | Povinné |
| Správa nákladů | Vyčistění údajů výpočtu kusovníku ve verzích výpočtu nákladů | Povinné |
| Správa nákladů | [Úložiště porovnání cen zboží](../cost-management/compare-item-price.md) | Povinné |
| Správa nákladů | [Úroveň výpočtu nákladů](../cost-management/cost-calculation-level.md) | Zapnuto ve výchozím nastavení |
| Správa nákladů | Povolit nastavení čísla dávky definované uživatelem pro storno uzávěrky zásob | Zapnuto ve výchozím nastavení |
| Správa nákladů | [Podrobnosti o průběhu uzávěrky zásob](whats-new-scm-10-0-21.md) | Zapnuto ve výchozím nastavení |
| Správa nákladů | [Úložiště sestavy hodnot zásob](../cost-management/inventory-value-report-storage.md) | Povinné |
| Správa nákladů | Vyčištění dat výkazu hodnoty zásob | Povinné |
| Správa nákladů | Klouzavý průměr, posloupnost záložních nákladů | Povinné |
| Správa nákladů | Zobrazit protokol uzávěrky zásob v mřížce | Povinné |
| Správa nákladů | Zobrazit položky s neúplně vyrovnanými transakcemi v souhrnném formátu | Povinné |
| Řízení zásob a skladu | Povolit prázdné hodnoty atributů dávky | Povinné |
| Řízení zásob a skladu | Automatické navyšování čísel řádků převodních příkazů zásob | Povinné |
| Řízení zásob a skladu | Vytvořit převodní příkaz z řádku prodeje | Povinné |
| Řízení zásob a skladu | Deaktivace pole řádku deníku zásob v pracovním postupu | Povinné |
| Řízení zásob a skladu | Povolit funkci upozornění na parametry správy kvality zásob | Povinné |
| Řízení zásob a skladu | (Čína) Vyloučit fyzický příjem a náklady na výdej z průměrných měsíčních nákladů | Zapnuto ve výchozím nastavení |
| Řízení zásob a skladu | [Workflow schválení deníku zásob](../inventory/inventory-journal-workflow.md) | Povinné |
| Řízení zásob a skladu | [Úložiště sestavy zásob na skladě](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/inventory-on-hand-report-storage) | Povinné |
| Řízení zásob a skladu | [Uložená zobrazení pro řízení zásob](saved-views-scm.md) | Povinné |
| Řízení zásob a skladu | Zrušení převodního příkazu | Povinné |
| Řízení zásob a skladu | Použití měrné jednotky a jednotkového množství v denících zásob | Povinné |
| Řízení zásob a skladu | Odemčení deníku zásob | Povinné |
| Výroba | [Automatické vyskladňování materiálů s povoleným skladem pro automaticky účtované výdejky](whats-new-scm-10-0-23.md) | Obecně dostupné |
| Výroba | Povolit zobrazování dimenzí zásob v seznamu materiálů pro operace výrobního postupu | Povinné |
| Výroba | [Umožňuje zadávat čísla dávky a sériová čísla při vykazování za dokončené v zařízení úkolového lístku](../production-control/report-finished-job-device.md) | Zapnuto ve výchozím nastavení |
| Výroba | Vylepšený výdej množství skutečné hmotnosti produkce | Zapnuto ve výchozím nastavení |
| Výroba | [Vyhledávání práce pro rozhraní ke spuštění výrobního provozu](../production-control/production-floor-execution-configure.md) | Povinné |
| Výroba | [Integrace se systémem realizace výroby](../production-control/mes-integration.md) | Zapnuto ve výchozím nastavení |
| Výroba | [Zobrazení Můj den pro rozhraní pro provádění výrobního provozu](../production-control/production-floor-execution-configure.md) | Zapnuto ve výchozím nastavení |
| Výroba | [Kontrola dostupnosti materiálu na vyžádání pro výrobní zakázky](whats-new-scm-10-0-24.md) | Zapnuto ve výchozím nastavení |
| Výroba | [Přepsat výchozí rezervaci výroby](../production-control/override-default-reservation-principle.md) | Povinné |
| Výroba | [Registrace spotřeby materiálu na rozhraní pro provádění výrobního provozu (mimo WMS)](../production-control/production-floor-execution-configure.md) | Obecně dostupné |
| Výroba | [Sestava položek skutečné hmotnosti z rozhraní provádění výrobního provozu](../production-control/production-floor-execution-configure.md) | Obecně dostupné |
| Výroba | [Zpráva o vedlejších a souběžných produktech z rozhraní pro provádění výrobního provozu](../production-control/production-floor-execution-configure.md) | Zapnuto ve výchozím nastavení |
| Výroba | [Vykazování položek plánování v rozhraní pro provádění výrobního provozu](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-process-manufacturing) | Zapnuto ve výchozím nastavení |
| Výroba | [Uložená zobrazení pro řízení výroby](saved-views-scm.md) | Povinné |
| Výroba | [Zobrazit celé sériové číslo, číslo dávky a registrační značku v rozhraní provádění výrobního provozu](../production-control/production-floor-execution-configure.md) | Povinné |
| Výroba | [Potvrdit expiraci surovin oproti plánovanému datu spotřeby](whats-new-scm-10-0-23.md) | Zapnuto ve výchozím nastavení |
| Hlavní plánování | [Automatické potvrzování pro optimalizaci plánování](../master-planning/planning-optimization/planned-order-firming.md) | Povinné |
| Hlavní plánování | [Dávkové potvrzení a konsolidace pro plánované hromadné a balíkové dávkové objednávky](whats-new-scm-10-0-20.md) | Zapnuto ve výchozím nastavení |
| Hlavní plánování | [Zahrnout položky se zásobami na skladě, když jsou povoleny filtry pro předběžné zpracování](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/master-planning-include-items-on-hand-when-pre-processing-filters-are-enabled) | Zapnuto ve výchozím nastavení |
| Hlavní plánování | [Plánování nekonečné kapacity pro optimalizaci plánování](../master-planning/planning-optimization/infinite-capacity-planning.md) | Zapnuto ve výchozím nastavení |
| Hlavní plánování | [Marže pro optimalizaci plánování](../master-planning/planning-optimization/safety-margins.md) | Povinné |
| Hlavní plánování | [Dny zpoždění pro Optimalizaci plánování](../master-planning/planning-optimization/delay-tolerance.md) | Povinné |
| Hlavní plánování | [Paralelní autorizace upravené prognózy poptávky](whats-new-scm-10-0-20.md) | Povinné |
| Hlavní plánování | [Potvrzení plánované objednávky s filtrováním](../master-planning/planning-optimization/planned-order-firming.md) | Povinné |
| Hlavní plánování | [Plánované výrobní zakázky pro optimalizaci plánování](../master-planning/planning-optimization/production-planning.md) | Povinné |
| Hlavní plánování | [Obchodní nákupní smlouvy pro optimalizaci plánování](../master-planning/planning-optimization/purchase-trade-agreement.md) | Povinné |
| Hlavní plánování | [Uložená zobrazení pro plánované objednávky](saved-views-scm.md) | Povinné |
| Zásobování a zdroje | Částky poplatků od a do na nákupních objednávkách | Povinné |
| Zásobování a zdroje | Deaktivace tlačítka resetování distribuce nákupní žádanky | Zapnuto ve výchozím nastavení |
| Zásobování a zdroje | [Povolit resetování pracovních postupů souvisejících se zásobováním](whats-new-scm-10-0-20.md) | Zapnuto ve výchozím nastavení |
| Zásobování a zdroje | [Omezit počet řádků nákupní objednávky na dávkovou úlohu](whats-new-scm-10-0-27.md) | Zapnuto ve výchozím nastavení |
| Zásobování a zdroje | [Sloučit finanční dimenze dodavatele s finanční dimenzí aktivního propojení dimenzí na nákupní objednávce](whats-new-scm-10-0-25.md) | Povinné |
| Zásobování a zdroje | [Účtujte registrovaná množství produktů na skladě a zbytky neskladových produktů pro účtenky a faktury dodavatele](whats-new-scm-10-0-26.md) | Obecně dostupné |
| Zásobování a zdroje | [Zabránit nadměrné spotřebě rezervací účelových položek rozpočtu, když je v pracovním postupu více nákupních žádanek](whats-new-scm-10-0-21.md) | Zapnuto ve výchozím nastavení |
| Zásobování a zdroje | [Odpovědná strana nákupní smlouvy](../procurement/purchase-agreements.md) | Povinné |
| Zásobování a zdroje | [Uložená zobrazení pro nákupní objednávky](saved-views-scm.md) | Povinné |
| Správa informací o produktech | Kusovník předzpracovává sestavy, aby nedošlo k vypršení časového limitu | Povinné |
| Správa informací o produktech | Výchozí finanční dimenze samostatně při použití šablon položek | Povinné |
| Správa informací o produktech | Povolit skupiny dimenzí produktů pro šablony položek | Povinné |
| Správa informací o produktech | Vylepšení entity položka - čárový kód | Povinné |
| Správa informací o produktech | Opětovně vygenerovat názvy variant produktů na základě názvosloví | Povinné |
| Správa informací o produktech | [Uložená zobrazení pro uvolněné produkty](saved-views-scm.md) | Povinné |
| Správa informací o produktech | [Vylepšení stránky návrhů variant](../pim/tasks/create-predefined-product-variants.md) | Povinné |
| Prodej a marketing | [Přidělení poplatků na prodejní objednávce](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/miscellaneous-charges-enhancements) | Povinné |
| Prodej a marketing | Vyčistit historii aktualizace prodejní objednávky | Povinné |
| Prodej a marketing | [Vyčistění historie aktualizace prodejů na základě stáří](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) | Povinné |
| Prodej a marketing | [Optimalizace exportu datové entity kontaktní osoby](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization) | Povinné |
| Prodej a marketing | Zkopírovat skupinu celkových slev pro prodejní dobropis | Povinné |
| Prodej a marketing | [Povolit vyhledávání polí úvodu a závěru dokumentu prodejní nabídky](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | Povinné |
| Prodej a marketing | [Zlepšit výkonnost sestavy „Prvních 100“ zákazníků](whats-new-scm-10-0-23.md) | Povinné |
| Prodej a marketing | Zahrnout čekající záznamy do úloh čištění historie | Povinné |
| Prodej a marketing | Omezit počet řádků prodejní objednávky na dávkovou úlohu | Zapnuto ve výchozím nastavení |
| Prodej a marketing | [Omezit počet prodejních objednávek, které lze vybrat k zaúčtování](whats-new-scm-10-0-21.md) | Povinné |
| Prodej a marketing | Přepočítat odhadovaný zůstatek zákazníka | Povinné |
| Prodej a marketing | [Registrace řádků vratky prodeje s desetinnou přesností se skutečnou hmotností a bez ní](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight) | Povinné |
| Prodej a marketing | [Uložená zobrazení pro prodej a marketing](saved-views-scm.md) | Povinné |
| Prodej a marketing | [Potvrzení prodejní objednávky jediným kliknutím](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/single-click-sales-order-confirmation) | Povinné |
| Správa přepravy | Povolit zrušení spárování účtů dopravného z řádků faktury za přepravu bez zaúčtovaného deníku faktur dodavatele | Zapnuto ve výchozím nastavení |
| Správa přepravy | [Povolit vytvoření deníku faktury dodavatele při vyřazování účtu dopravného](whats-new-scm-10-0-20.md) | Zapnuto ve výchozím nastavení |
| Správa přepravy | [Expedice malých balíků](../warehousing/small-parcel-shipping.md) | Povinné |
| Správa přepravy | [Dokument s certifikátem o původu USMCA](../transportation/usmca-certification-of-origin.md) | Zapnuto ve výchozím nastavení |
| Řízení skladu | [Další zóna skladového místa](../warehousing/additional-location-zones.md) | Povinné |
| Řízení skladu | [Zrušit práci](../warehousing/cancel-warehouse-work.md) | Povinné |
| Řízení skladu | [Konsolidovat dodávku](../warehousing/configure-shipment-consolidation-policies.md) | Povinné |
| Řízení skladu | [Vytvářet a zpracovat převodní příkazy z aplikace skladu](../warehousing/create-transfer-order-from-warehouse-app.md) | Povinné |
| Řízení skladu | Šablony cross dockingu se směrnicemi skladového místa | Zapnuto ve výchozím nastavení |
| Řízení skladu | [Odpojit odloženou práci od ASN](whats-new-scm-10-0-21.md) | Povinné |
| Řízení skladu | [Odložené operace Put](../warehousing/deferred-processing-manual-inventory-movement.md) | Povinné |
| Řízení skladu | Odložený příjem - kontejner | Zapnuto ve výchozím nastavení |
| Řízení skladu | Zpracování odloženého příjmu - povolit funkci šablony auditu s aktivační událostí nastavenou na Předchozí | Povinné |
| Řízení skladu | [Zakázat očekávané příjmy z objednávek kvality, které slouží pro pořízení vzorku blokovaných zásob](../inventory/inventory-blocking.md) | Zapnuto ve výchozím nastavení |
| Řízení skladu | Povolit rychlé ověření pro mobilních zařízení ve skladu | Povinné |
| Řízení skladu | [Vylepšený analyzátor pro čárové kódy GS1](../warehousing/gs1-barcodes.md) | Obecně dostupné |
| Řízení skladu | [Flexibilní rezervace registrační značky potvrzená objednávkou](../warehousing/flexible-warehouse-level-dimension-reservation.md) | Povinné |
| Řízení skladu | [Pružná rezervace dimenze na úrovni skladu](../warehousing/flexible-warehouse-level-dimension-reservation.md) | Povinné |
| Řízení skladu | [Využití skladového místa pro konsolidaci zboží](../warehousing/item-consolidation-location-utilization.md) | Zapnuto ve výchozím nastavení |
| Řízení skladu | Historie přijetí registrační značky | Zapnuto ve výchozím nastavení |
| Řízení skladu | [Ruční konsolidace dodávky](../warehousing/consolidate-shipments-manual-workbench.md) | Zapnuto ve výchozím nastavení |
| Řízení skladu | [Služba ručního výdeje řádku převodu pro správce nebo podobné důvěryhodné uživatele](whats-new-scm-10-0-28.md) | Obecně dostupné |
| Řízení skladu | [Rozhraní vybavení manipulace s materiálem](../warehousing/mhax.md) | Povinné |
| Řízení skladu | [Nové stránky pracovní plochy plánování vytížení](whats-new-scm-10-0-24.md) | Obecně dostupné |
| Řízení skladu | [Vizualizace odchozí úlohy](../warehousing/outbound-workload-visualization.md) | Povinné |
| Řízení skladu | [Plánovaný cross docking](../warehousing/planned-cross-docking.md) | Povinné |
| Řízení skladu | [Zpracovat události aplikace skladu](../warehousing/warehouse-app-events.md) | Povinné |
| Řízení skladu | Vylepšení dotazu pro šablonu práce vyskladnění souběžného a vedlejšího produktu | Povinné |
| Řízení skladu | [Zaokrouhlit množství dolů na nejbližší prodejní jednotku při uvolnění do skladu](whats-new-scm-10-0-19.md) | Povinné |
| Řízení skladu | [Uložené zobrazení pro pracovní plochu plánování vytížení](saved-views-scm.md) | Povinné |
| Řízení skladu | [Uložené zobrazení stránky s podrobnostmi o práci](saved-views-scm.md) | Povinné |
| Řízení skladu | [Uložené zobrazení pro zpracování vlny](saved-views-scm.md) | Povinné |
| Řízení skladu | [Uložená zobrazení pro zpracování vytížení](saved-views-scm.md) | Povinné |
| Řízení skladu | [Uložená zobrazení pro zpracování dodávky](saved-views-scm.md) | Povinné |
| Řízení skladu | [Naskenovat čárové kódy GS1](../warehousing/gs1-barcodes.md) | Obecně dostupné |
| Řízení skladu | Podrobnosti štítku vlny dodávky | Povinné |
| Řízení skladu | [Umístit smíšené jednotky do slotu](whats-new-scm-10-0-21.md) | Povinné |
| Řízení skladu | [Použijte rychlejší rozhraní API pro zavírání/opětovné otevírání kontejnerů na balicí stanici](whats-new-scm-10-0-21.md) | Zapnuto ve výchozím nastavení |
| Řízení skladu | [Ověřit šablony vybrané pro práci doplnění](whats-new-scm-10-0-20.md) | Zapnuto ve výchozím nastavení |
| Řízení skladu | [Propagovaná pole aplikace skladu](../warehousing/warehouse-app-promoted-fields.md) | Povinné |
| Řízení skladu | [Pokyny ke kroku aplikace skladu](../warehousing/mobile-app-titles-instructions.md) | Povinné |
| Řízení skladu | [Stav skladového místa](../warehousing/warehouse-location-status.md) | Povinné |
| Řízení skladu | [Obcházení aplikace Warehouse Management](../warehousing/warehouse-app-detours.md) | Zapnuto ve výchozím nastavení |
| Řízení skladu | [Podrobnosti dávkové úlohy vlny](../warehousing/wave-processing.md) | Povinné |
| Řízení skladu | [Oznámení o provedení vlny](../warehousing/wave-execution-notifications.md) | Povinné |

## <a name="additional-resources"></a>Další prostředky

### <a name="platform-updates-for-finance-and-operations-apps"></a>Aktualizace platformy pro finanční a provozní aplikace

Microsoft Dynamics 365 Supply Chain Management 10.0.29 zahrnuje aktualizace platformy. Další informace naleznete v tématu [Aktualizace platformy pro verze 10.0.29 finančních a provozních aplikací (říjen 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-29.md).

### <a name="bug-fixes"></a>Opravy chyb

Sháníte-li informace o opravách chyb zahrnutých v jednotlivých aktualizacích, které jsou součástí verze 10.0.29, přihlaste se ke službám Lifecycle Services (LCS) a přečtěte si [článek znalostní báze](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 a průmyslová cloudová řešení: Plán vlny 1 vydání 2022

Zajímáte se o nadcházející a nedávno uvedené funkce jakékoliv z našich obchodních aplikací nebo platforem?

Přečtěte si [Dynamics 365 a průmyslová cloudová řešení: Plán vlny 2 vydání 2022](/dynamics365-release-plan/2022wave2/). Popsali jsme všechny podrobnosti, od A až do Z, v jednom dokumentu, který můžete používat pro plánování.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Odebrané a zastaralé funkce Supply Chain Management

Článek [Odebrané nebo zastaralé funkce v Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) popisuje funkce Supply Chain Management, které byly nebo jsou naplánovány k odebrání nebo které zastaraly.

- *Odstraněná* funkce již není k dispozici v produktu.
- *Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Před odebráním jakékoli funkce produktu bude oznámeno její zastarání v článku [Odebrané nebo zastaralé funkce v Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 měsíců před odebráním.

U změn způsobujícíh chyby, které ovlivní pouze dobu kompilace, ale jsou v binárním formátu kompatibilní s prostředím sandbox a produkčními prostředími, bude doba zastarání kratší než 12 měsíců. Obvykle se jedná o funkční aktualizace, které je třeba provést v kompilátoru.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
