---
title: Co je nového nebo se změnilo v aplikaci Dynamics 365 Supply Chain Management verze 10.0.19 (červen 2021)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Supply Chain Management 10.0.19.
author: kamaybac
ms.date: 04/23/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-23
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c1930a47bc133c411a0e6054aa766322a261064a06ac4cec8dcdd12c126dc7cd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773530"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-version-10019-june-2021"></a>Co je nového nebo se změnilo v aplikaci Dynamics 365 Supply Chain Management verze 10.0.19 (červen 2021)

[!include [banner](../includes/banner.md)]

Tohle téma uvádí funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Supply Chain Management verze 10.0.19. Tato verze má číslo sestavení 10.0.837 a je k dispozici následujícím způsobem:

- **Verze Preview:** duben 2021
- **Obecně dostupné vydání (vlastní aktualizace):** červen 2021
- **Obecně dostupné vydání (automatická aktualizace):** červen 2021

## <a name="features-included-in-this-release"></a>Funkce zahrnuté do této verze

V následující tabulce je uveden seznam funkcí této verze. Sloupec *Funkce* poskytuje odkazy na [plán vydání](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features), kde můžete vidět oficiální datumy vydání jednotlivých funkcí. Sloupec *Další informace* obsahuje další podrobnosti a/nebo odkazy na související dokumentaci.

Většinu těchto funkcí je nutné povolit pomocí [Správy funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), než je budete moci použít.

| Oblast funkce | Funkce | Další informace |
|---|---|---|
| Zásoby&nbsp;a&nbsp;logistika | [Schválení a uložení bankovních údajů odeslaných dodavatelem](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/approve-save-vendor-submitted-bank-details) | [Udržování informací o bankovním účtu dodavatele](../../finance/accounts-payable/maintain-vendor-bank-info.md) |
| Zásoby a logistika | [Optimalizace exportu datové entity kontaktní osoby](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization)  | Je-li tato funkce povolena, změny odkazovaných dat nezpůsobí zahrnutí souvisejících kontaktů do dalšího přírůstkového exportu. Je-li tato funkce zakázána, změny odkazovaných dat způsobí zahrnutí souvisejících kontaktů do dalšího přírůstkového exportu. |
| Zásoby a logistika | [Přírůstková vylepšení možností provádění skladu s jednotkami škálování](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/incremental-enhancements-warehouse-execution-capabilities-scale-units) |[Zprávy procesoru zpráv](../cloud-edge/cloud-edge-message-processor-messages.md)<br><br>[Úprava skladových zásob](../cloud-edge/cloud-edge-warehouse-inventory-adjustment.md)<br><br>[Pracovní zátěže správy skladu pro jednotky škálování cloudu a hraniční sítě](../cloud-edge/cloud-edge-workload-warehousing.md) |
| Zásoby a logistika | [Funkce vyhledávání pro pole Úvod do dokumentu a Závěr dokumentu na stránce Prodejní nabídka](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | Funkce přidá funkci vyhledávání pro pole **Úvod do dokumentu** a **Závěr dokumentu** na stránce **Prodejní nabídka**.<br><br>Tato funkce je povolena ve výchozím nastavení. |
| Zásoby a logistika | [Provádění skladu s jednotkami škálování hraniční sítě na vašem vlastním hardwaru](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-edge-scale-units-custom-hardware) | [Nasazení jednotek škálování hraniční sítě na vlastní hardware pomocí LBD](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Výroba | [Provádění výroby s jednotkami škálování hraniční sítě na vašem vlastním hardwaru](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-edge-scale-units-custom-hardware) | [Nasazení jednotek škálování hraničního zařízení na vlastní hardware pomocí LBD](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Plánování | [Plánování nekonečné kapacity pro optimalizaci plánování](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/schedule-infinite-capacity-support-planning-optimization) | Tato funkce umožňuje plánování kapacity s nekonečnou kapacitou pro optimalizaci plánování. Bez této funkce plánované výrobní zakázky získají svůj dodací čas z dodaného času inventáře vydaných produktů bez ohledu na časový rozvrh plánování. |
| Plánování | Plánované potvrzení objednávek založené na dotazech | [Potvrdit plánované objednávky](../master-planning/planning-optimization/planned-order-firming.md) |
| Řízení informací o produktech | [Vylepšení stránky návrhů variant](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/variant-suggestions-page-improvements) | [Vytváření předdefinovaných variant produktů](../pim/tasks/create-predefined-product-variants.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Vylepšení funkcí zahrnutých do této verze

V následující tabulce je uveden seznam vylepšených funkcí této verze. Každý z nich poskytuje přírůstkové vylepšení stávající funkce. Protože se jedná pouze o vylepšení, nejsou uvedeny v seznamu [plán vydání](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Aby se však zajistilo, že tato vylepšení nebudou v rozporu s vašimi stávajícími přizpůsobeními nebo předvolbami, je každé z nich ve výchozím nastavení vypnuto (pokud není uvedeno jinak). Pokud chcete použít některou z těchto funkcí, musíte ji výslovně povolit ve [Správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Oblast funkce | Vlastnosti&nbsp;název&nbsp;ve funkci&nbsp;řízení | Další informace |
|---|---|---|
| Prodej a marketing | Vylepšení výkonu čištění historie prodeje | Vyčištění historie prodeje může trvat dlouho, pokud se zřídka spouští v prostředích s velkým objemem aktualizací prodeje. Chcete-li zkrátit dobu trvání a zlepšit spolehlivost, tato funkce rozděluje vyčištění na dávky, které běží po omezenou dobu. Kde je to možné, využijí se možnosti databáze, aby se minimalizovalo zamykání a zabránilo se spojování transakčních tabulek během čištění. |
| Prodej a marketing | Aktualizovat požadované datum přijetí o datum potvrzení pro mezipodnikové objednávky | Tato funkce vám umožňuje řídit, co se stane s hodnotami pole data prodeje a nákupu při použití mezipodnikového přímého doručení. Můžete si vybrat, zda bude systém požadovaná data aktualizovat, nebo jejich aktualizaci přeskočit. Pokud aktualizaci přeskočíte, budou požadovaná data představovat to, co zákazník požadoval. Pokud povolíte aktualizaci, požadovaná data (při použití kontroly data dodání) představují pouze zpočátku to, co zákazník požadoval. Kontrola data dodání, pokud se liší od *Žádný*, zruší to, co bylo původně požadováno. Tuto možnost můžete nastavit pomocí nového nastavení **Aktualizovat požadované datum přijetí o potvrzené datum** mezipodnikového dodavatele nebo nastavení zákazníka.<br><br>Pokud je funkce deaktivována, systém přepíše požadované datum přijetí u původních prodejních objednávek na základě pravidla kontroly data dodání, ale požadované datum odeslání zůstane tak, jak je. |
| Řízení skladu | Zaokrouhlit množství dolů na nejbližší prodejní jednotku při uvolnění do skladu | Tato funkce přidává možnost, která může omezit množství objednávek při propuštění do skladu. Pokud je tato možnost povolena, množství objednávek bude zaokrouhleno dolů na nejbližší celou prodejní jednotku a objednávky obsahující množství pro méně než jednu prodejní jednotku budou pro vydání odmítnuty. |
| Řízení skladu | Metoda vlny „plánované vytvoření práce“ v celé organizaci | Po povolení této funkce bude metoda vlny *Plánování vytvoření práce* přidána a nakonfigurována pro paralelní běh napříč všemi právnickými osobami. Bude také ovlivněno několik dalších nastavení. Úplné informace viz [Plánování vytváření práce během vlny](../warehousing/configure-wave-schedule-work-creation.md). |

## <a name="new-and-updated-documentation-resources"></a>Nové a aktualizované zdroje dokumentace

Nedávno jsme přidali nebo významně aktualizovali následující témata nápovědy. Nemusí nutně souviset s novými funkcemi přidanými pro toto vydání, jak je uvedeno v předchozí části, ale mohou vám pomoci lépe využít stávající funkce.

| Oblast funkce | Nová nebo aktualizovaná témata |
|---|---|
| Správa technických změn | [Správa technických změn – často kladené otázky](../engineering-change-management/change-management-faq.md) |
| Zásobování a zdroje | [Požadavky kategorií od dodavatelů](../procurement/category-requests-from-vendors.md) |
| Řízení informací o produktech | [Správa měrných jednotek](../pim/tasks/manage-unit-measure.md)<br><br>[Výpočty modelu konfigurace produktu](../pim/config-model-calculations.md) |
| Řízení výroby | [Sjednocená číselná řady pro ID úloh](../production-control/unified-job-ids.md) |
| Správa přepravy | [Třídy LTL](../transportation/ltl-class.md)<br><br>[Kódy NMFC](../transportation/nmfc-codes.md) |
| Řízení skladu | [Odstraňování problémů s hierarchiemi dávkových a sériových rezervací skladu](../warehousing/troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md) |
| Řízení skladu, tvorba a zpracování vln | [Tvorba a zpracování vln](../warehousing/wave-processing.md)<br><br>[Parametry skladu pro zpracování vln](../warehousing/wave-warehouse-parameters.md)<br><br>[Šablony vlny](../warehousing/wave-templates.md)<br><br>[Přidělení vlny](../warehousing/wave-allocation-method.md)<br><br>[Plánování vytváření práce během vlny](../warehousing/configure-wave-schedule-work-creation.md)<br><br>[Vytváření kontejnerů](../warehousing/wave-containerization.md)<br><br>[Oznámení o provedení vlny](../warehousing/wave-execution-notifications.md) |

## <a name="additional-resources"></a>Další prostředky

### <a name="platform-updates-for-finance-and-operations-apps"></a>Aktualizace platformy pro aplikace Finance and Operations

Microsoft Dynamics 365 Supply Chain Management 10.0.19 zahrnuje aktualizace platformy. Další informace naleznete v tématu [Aktualizace platformy pro verze 10.0.19 aplikací Finance and Operations (červen 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19.md).

### <a name="bug-fixes"></a>Opravy chyb

Sháníte-li informace o opravách chyb zahrnutých v jednotlivých aktualizacích, které jsou součástí verze 10.0.19, přihlaste se ke službám Lifecycle Services (LCS) a přečtěte si [článek znalostní báze](https://fix.lcs.dynamics.com/Issue/Details?bugId=575415).

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: plán 1. vlny vydání v r. 2021

Zajímáte se o nadcházející a nedávno uvedené funkce jakékoliv z našich obchodních aplikací nebo platforem?

Přečtěte si téma [Dynamics 365: plán 1. vlny vydání v r. 2021](/dynamics365-release-plan/2021wave1/). Popsali jsme všechny podrobnosti, od A až do Z, v jednom dokumentu, který můžete používat pro plánování.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Odebrané a zastaralé funkce Supply Chain Management

Téma [Odebrané nebo zastaralé funkce v Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) popisuje funkce Supply Chain Management, které byly nebo jsou naplánovány k odebrání nebo které zastaraly.

- *Odstraněná* funkce již není k dispozici v produktu.
- *Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Před odebráním jakékoli funkce produktu bude oznámeno její zastarání v tématu [Odebrané nebo zastaralé funkce v Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 měsíců před odebráním.

U změn způsobujícíh chyby, které ovlivní pouze dobu kompilace, ale jsou v binárním formátu kompatibilní s prostředím sandbox a produkčními prostředími, bude doba zastarání kratší než 12 měsíců. Obvykle se jedná o funkční aktualizace, které je třeba provést v kompilátoru.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
