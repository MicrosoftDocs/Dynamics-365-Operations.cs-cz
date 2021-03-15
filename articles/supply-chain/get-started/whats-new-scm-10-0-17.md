---
title: Náhled Dynamics 365 Supply Chain Management 10.0.17 (duben 2021)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Supply Chain Management 10.0.17.
author: kamaybac
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-11-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: bfa6e04f8d7ae192d0acd88fb3f1d7e2ce6cc576
ms.sourcegitcommit: b9c6ad79d05feb858f818b37ce5c344f90cc6eb7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/08/2021
ms.locfileid: "5137921"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10017-april-2021"></a>Náhled Dynamics 365 Supply Chain Management 10.0.17 (duben 2021)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tohle téma uvádí funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Supply Chain Management verze Preview 10.0.17. Tato verze má číslo sestavení 10.0.761 a je k dispozici následujícím způsobem:

- **Náhled vydané verze:** únor 2021
- **Obecně dostupné vydání (automatická aktualizace):** březen 2021
- **Obecně dostupné vydání (automatická aktualizace):** duben 2021

## <a name="features-included-in-this-release"></a>Funkce zahrnuté do této verze

Tato verze obsahuje následující funkce. Některé z uvedených funkcí jsou stále ve verzi Preview, zatímco jiné již mohou být obecně dostupné. Postupujte podle odkazů v [plánu vydání](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) pro zobrazení oficiálních dat vydání pro každou funkci.

- [Použití pravidel pro seskupování pracovních příkazů při provádění plánu údržby](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/apply-rules-grouping-work-orders-while-running-maintenance-plan)<br> - Další informace naleznete v tématu [Vytvoření pracovních příkazů](../asset-management/preventive-and-reactive-maintenance/creating-work-orders.md).

<!-- KFM: Blocked for now. Dana will followup.
- [Approve and save vendor-submitted bank details](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/approve-save-vendor-submitted-bank-details) 
-->

- Funkce správy majetku v rozhraní pro spuštění výrobního provozu<br> - Další informace viz [Jak pracovníci používají rozhraní pro provádění výrobního provozu](../production-control/production-floor-execution-use.md).  <!-- KFM: Not yet published on release plan, but is ready. Should be in the next publish. -->

- [Fakturace zákazníků za údržbářské práce](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/bill-customers-maintenance-work)<br> - Další informace viz [Účet za údržbu na majetku ve vlastnictví zákazníka](../asset-management/integration-to-project-management-and-accounting/customer-billing.md).

- [Podpora ochranné lhůty pro optimalizaci plánování](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/coverage-time-fence-support-planning-optimization)<br> - Další informace viz [Ochranná lhůta pokrytí](../master-planning/planning-optimization/coverage-time-fence.md).

- [Povolit správu změn u stávajících produktů](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/enable-change-management-existing-products)

<!-- KFM: Add this when the feature appears in release plan at next update:
- Enterprise-scale inventory performance improvements and archiving  -->

- [Náklady za doručení](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/landed-cost)

- [Provádění výroby s jednotkami škálování v cloudu](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-scale-units-cloud)<br> - Další informace naleznete v části [Pracovní zatížení provádění výroby a jednotky okrajového škálování](../cloud-edge/cloud-edge-workload-manufacturing.md).

- [Manipulace s materiálem / automatizace skladu](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/material-handlingwarehouse-automation) <!-- KFM: Update RP link when the new one goes live -->

- [Dimenze balení a uskladnění](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/packing-vs.-storage-dimensions)<br> - Další informace viz [Nastavení různých rozměrů pro balení a skladování](../warehousing/packing-vs-storage-dimensions.md)

- Přepis výchozího principu rezervace pro materiály ve výrobě<br> - Další informace získáte v části [Přepis výchozího principu rezervace pro materiály ve výrobě](../production-control/override-default-reservation-principle.md). <!-- KFM: Not yet published on release plan, but is ready. Should be in the next publish. -->

- [Plánovaná údržba na základě kumulovaných hodnot počitadel majetku](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/plan-maintenance-based-accumulated-asset-counter-values)<br> - Další informace naleznete v tématu [Plány údržby](../asset-management/preventive-and-reactive-maintenance/maintenance-plans.md).

- [Podpora nákupních žádanek pro optimalizaci plánování](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/purchase-requisition-support-planning-optimization)<br> - Další informace naleznete v tématu [Nákupní žádanky](../master-planning/planning-optimization/purchase-requisitions.md)

- [Uložená zobrazení pro inventář a logistiku](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/saved-views-inventory-logistics)<br> - Další informace viz [Standardní uložená zobrazení pro Supply Chain Management](saved-views-scm.md).

- [Uložená zobrazení pro plánované objednávky](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/saved-views-planned-orders)<br> - Další informace viz [Standardní uložená zobrazení pro Supply Chain Management](saved-views-scm.md).

- [Uložená zobrazení pro řízení výroby](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/saved-views-production-control)<br> - Další informace viz [Standardní uložená zobrazení pro Supply Chain Management](saved-views-scm.md).

- [Plánování vytvoření skladové práce](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/schedule-warehouse-work-creation)<br> - Další informace viz [Plánování vytváření práce během vlny](../warehousing/configure-wave-schedule-work-creation.md).

- [Nastavení výchozích finančních dimenzí pro poukázky na přecenění standardních nákladů na zásoby](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/set-default-financial-dimensions-inventory-standard-cost-revaluation-vouchers)<br> - Další informace viz [Správa aktualizací standardních nákladů](../cost-management/manage-standard-cost-updates.md).

- [Expedice malých balíků (SPS)](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/small-package-shipping-sps)<br> - Další informace viz [Expedice malých balíků](../warehousing/small-parcel-shipping.md). <!-- KFM: Update RP link when the new one goes live -->

- [Provádění skladů s jednotkami škálování v cloudu](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-scale-units-cloud)<br> - Další informace získáte v části [Pracovní zatížení řízení skladu pro cloudové a okrajové jednotky škálování](../cloud-edge/cloud-edge-workload-warehousing.md) a [Skladové objednávky pro cloudové a okrajové jednotky škálování](../cloud-edge/cloud-edge-warehouse-order.md).

- [Mobilní aplikace pro správu skladu](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application)<br> - Další informace naleznete v části [Instalace a připojení aplikace řízení skladu](../warehousing/install-configure-warehouse-management-app.md).

Většinu těchto funkcí je nutné povolit pomocí [Správy funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), než je budete moci použít.

## <a name="new-and-updated-documentation-resources"></a>Nové a aktualizované zdroje dokumentace

Nedávno jsme přidali nebo významně aktualizovali následující témata nápovědy. Nemusí nutně souviset s novými funkcemi přidanými pro toto vydání, jak je uvedeno v předchozí části, ale mohou vám pomoci lépe využít stávající funkce.

- [Konfigurace produktových filtrů pro skladové transakce](../warehousing/filters-and-filter-codes.md)

- [Návrh rozhraní pro provádění výrobního provozu](../production-control/production-floor-execution-tabs.md)

- [Mezipodnikové plánování](../master-planning/planning-optimization/Intercompany-planning.md)

- [Značení zásob s optimalizací plánování](../master-planning/planning-optimization/marking.md)

- [Hlavní plánování s prognózami poptávky](../master-planning/planning-optimization/demand-forecast.md)

- [Částečná cyklická inventura místa](../warehousing/partial-location-cycle-counting.md)

- [Seskupování řádků vyskladnění](../warehousing/pick-line-grouping.md)

- [Plánování výroby](../master-planning/planning-optimization/production-planning.md) <!--KFM: Remember to add YouTube link to this topic -->

- [Požadavky na nákup v hlavním plánování](../master-planning/planning-optimization/purchase-requisitions.md)

- [Nastavení mobilního pracovního prostoru správy majetku](../asset-management/set-up-asset-management-mobile.md)

- [Řešení potíží se správou nákladů](../cost-management/troubleshoot-costmanagement.md)

- [Řešení potíží s operacemi inventáře](../inventory/troubleshoot-inventory-operations.md)

- [Skladový slotting](../warehousing/warehouse-slotting.md)

## <a name="additional-resources"></a>Další prostředky

### <a name="platform-updates-for-finance-and-operations-apps"></a>Aktualizace platformy pro aplikace Finance and Operations

Microsoft Dynamics 365 Supply Chain Management 10.0.17 zahrnuje aktualizace platformy. Další informace naleznete v tématu [Aktualizace platformy pro verze 10.0.17 aplikací Finance and Operations (duben 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md).

### <a name="bug-fixes"></a>Opravy chyb

Sháníte-li informace o opravách chyb zahrnutých v jednotlivých aktualizacích, které jsou součástí verze 10.0.17, přihlaste se ke službám Lifecycle Services (LCS) a přečtěte si [článek znalostní báze](https://fix.lcs.dynamics.com/Issue/Details?bugId=551039&dbType=3&qc=91219e7c3fc585acb17b810c915c3cbea499403538520c40e54de43a53aea6a8).

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: plán 1. vlny vydání v r. 2021

Zajímáte se o nadcházející a nedávno uvedené funkce jakékoliv z našich obchodních aplikací nebo platforem?

Přečtěte si téma [Dynamics 365: plán 1. vlny vydání v r. 2021](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/). Popsali jsme všechny podrobnosti, od A až do Z, v jednom dokumentu, který můžete používat pro plánování.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Odebrané a zastaralé funkce Supply Chain Management

Téma [Odebrané nebo zastaralé funkce v Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) popisuje funkce Supply Chain Management, které byly nebo jsou naplánovány k odebrání nebo které zastaraly.

- *Odstraněná* funkce již není k dispozici v produktu.
- *Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Před odebráním jakékoli funkce produktu bude oznámeno její zastarání v tématu [Odebrané nebo zastaralé funkce v Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 měsíců před odebráním.

U změn způsobujícíh chyby, které ovlivní pouze dobu kompilace, ale jsou v binárním formátu kompatibilní s prostředím sandbox a produkčními prostředími, bude doba zastarání kratší než 12 měsíců. Obvykle se jedná o funkční aktualizace, které je třeba provést v kompilátoru.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]