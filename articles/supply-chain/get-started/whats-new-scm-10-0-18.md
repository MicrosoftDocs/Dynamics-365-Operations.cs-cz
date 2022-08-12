---
title: Co je nového nebo změněného v softwaru Dynamics 365 Supply Chain Management verze 10.0.18 (květen 2021)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Supply Chain Management 10.0.18.
author: kamaybac
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2aa5d40d6263f9f91fc3ebfcb37558a5ba71d2ab
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2022
ms.locfileid: "9123831"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-version-10018-may-2021"></a>Co je nového nebo změněného v softwaru Dynamics 365 Supply Chain Management verze 10.0.18 (květen 2021)

[!include [banner](../includes/banner.md)]

Tento článek uvádí funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Supply Chain Management 10.0.18. Tato verze má číslo sestavení 10.0.793 a je k dispozici následujícím způsobem:

- **Náhled verze:** březen 2021
- **Obecně dostupné vydání (vlastní aktualizace):** duben 2021
- **Obecně dostupné vydání (automatická aktualizace):** květen 2021

## <a name="features-included-in-this-release"></a>Funkce zahrnuté do této verze

Tato verze obsahuje následující funkce. Postupujte podle odkazů v [plánu vydání](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) pro zobrazení oficiálních dat vydání pro každou funkci.

- Automatické vydávání objednávek (vylepšení pro [Realizace skladu s jednotkami škálování v cloudu](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-scale-units-cloud))<br> - Další informace naleznete v části [Pracovní zatížení pro jednotky škálování cloudu a hraniční sítě](../cloud-edge/cloud-edge-workload-warehousing.md).

- [Vytváření a zobrazení certifikací v rozhraní pro spolupráci dodavatele](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/create-view-certifications-vendor-collaboration-interface)<br> - Další informace viz [Udržování certifikace dodavatele](../../finance/public-sector/manage-vendor-certification.md).

- [Vylepšení výkonu a archivace v podnikovém měřítku](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/enterprise-scale-inventory-performance-improvements-archiving)<br> - Další informace viz [Archivace skladových transakcí](../inventory/archive-inventory-transactions.md).

- [Správa rabatu](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/rebate-management)<br> - Další informace naleznete v tématu [Přehled modulu Správa rabatu](../rebate-management/rebate-management-overview.md).

- [Zásady nastavení exportu datové entity prodeje](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-data-entity-export-setup-policy)

- [Registrace řádků vratky prodeje s desetinnou přesností se skutečnou hmotností a bez ní](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight)

- [Potvrzení prodejní objednávky jediným kliknutím](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/single-click-sales-order-confirmation)

- [Zásady odstranění řádku prodejní objednávky propojeného s řádkem nákupní objednávky](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-purchase-order-line-deletion-policy)

- Zjednodušené rozhraní pouze pro označení příchodu do práce a odchodu z práce (vylepšení pro [Vylepšené rozhraní pro provádění výrobního provozu pro výrobu](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-manufacturing))<br> - Další informace viz [Konfigurace rozhraní pro provádění výrobního provozu](../production-control/production-floor-execution-configure.md).

Většinu těchto funkcí je nutné povolit pomocí [Správy funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), než je budete moci použít.

## <a name="new-and-updated-documentation-resources"></a>Nové a aktualizované zdroje dokumentace

Nedávno jsme přidali nebo významně aktualizovali následující články nápovědy. Nemusí nutně souviset s novými funkcemi přidanými pro toto vydání, jak je uvedeno v předchozí části, ale mohou vám pomoci lépe využít stávající funkce.

- [Doplněk viditelnosti zásob](../inventory/inventory-visibility.md)
- [Modul Náklady za doručení](../landed-cost/landed-cost-overview.md)
- [Rozhraní vybavení manipulace s materiálem (MHAX)](../warehousing/mhax.md)
- [Analýza přizpůsobení pro optimalizaci plánování](../master-planning/planning-optimization/planning-optimization-fit-analysis.md)

## <a name="additional-resources"></a>Další prostředky

### <a name="platform-updates-for-finance-and-operations-apps"></a>Aktualizace platformy pro finanční a provozní aplikace

Microsoft Dynamics 365 Supply Chain Management 10.0.18 zahrnuje aktualizace platformy. Další informace naleznete v tématu [Aktualizace platformy pro verze 10.0.18 finančních a provozních aplikací (květen 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18.md).

### <a name="bug-fixes"></a>Opravy chyb

Sháníte-li informace o opravách chyb zahrnutých v jednotlivých aktualizacích, které jsou součástí verze 10.0.18, přihlaste se ke službám Lifecycle Services (LCS) a přečtěte si [článek znalostní báze](https://fix.lcs.dynamics.com/Issue/Details?bugId=561679&dbType=3&qc=13bb1641c1be430ead8b21ae3d4e0f800d5b81c39b3a56e890db1de7ede59e46).

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: plán 1. vlny vydání v r. 2021

Zajímáte se o nadcházející a nedávno uvedené funkce jakékoliv z našich obchodních aplikací nebo platforem?

Přečtěte si téma [Dynamics 365: plán 1. vlny vydání v r. 2021](/dynamics365-release-plan/2021wave1/). Popsali jsme všechny podrobnosti, od A až do Z, v jednom dokumentu, který můžete používat pro plánování.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Odebrané a zastaralé funkce Supply Chain Management

Článek [Odebrané nebo zastaralé funkce v Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) popisuje funkce Supply Chain Management, které byly nebo jsou naplánovány k odebrání nebo které zastaraly.

- *Odstraněná* funkce již není k dispozici v produktu.
- *Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Před odebráním jakékoli funkce produktu bude oznámeno její zastarání v článku [Odebrané nebo zastaralé funkce v Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 měsíců před odebráním.

U změn způsobujícíh chyby, které ovlivní pouze dobu kompilace, ale jsou v binárním formátu kompatibilní s prostředím sandbox a produkčními prostředími, bude doba zastarání kratší než 12 měsíců. Obvykle se jedná o funkční aktualizace, které je třeba provést v kompilátoru.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

