---
title: Verze Preview aplikace Dynamics 365 Supply Chain Management 10.0.24 (únor 2022)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Supply Chain Management 10.0.24.
author: kamaybac
ms.date: 12/03/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 1b5742ddf7e5e2c5c32c446a0bde08f4964d6b95
ms.sourcegitcommit: 96515ddbe2f65905140b16088ba62e9b258863fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/04/2021
ms.locfileid: "7891872"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10024-february-2022"></a>Verze Preview aplikace Dynamics 365 Supply Chain Management 10.0.24 (únor 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tohle téma uvádí funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Supply Chain Management verze Preview 10.0.24. Tato verze má číslo sestavení 10.0.1084 a je k dispozici následujícím způsobem:

- **Vydání verze Preview:** prosinec 2021
- **Obecně dostupné vydání (automatická aktualizace):** Leden 2022
- **Obecně dostupné vydání (automatická aktualizace):** Únor 2022

## <a name="features-included-in-this-release"></a>Funkce zahrnuté do této verze

V následující tabulce je uveden seznam funkcí této verze. Tohle téma můžeme aktualizovat, aby obsahovalo funkce, které se dostaly do sestavení poté, co bylo toto téma původně publikováno.

| Oblast funkce | Funkce | Další informace | Povolil/a   |
|---|---|---|---|
| Distribuovaná hybridní topologie | [Vylepšení prováděcích úloh skladu na jednotkách škálování](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-warehouse-execution-workloads-scale-units) | [Pracovní zátěže správy skladu pro jednotky škálování cloudu a hraniční sítě](../cloud-edge/cloud-edge-workload-warehousing.md) | Ve výchozím nastavení povoleno. |
| Plánování | [Podpora optimalizace plánování pro rezervu a rezervu výdeje](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-reorder-margin-issue-margin) | [Pojistné doby](../master-planning/planning-optimization/safety-margins.md) | Ve výchozím nastavení povoleno. |

## <a name="feature-enhancements-included-in-this-release"></a>Vylepšení funkcí zahrnutých do této verze

V následující tabulce je uveden seznam vylepšených funkcí této verze. Každé z těchto vylepšení poskytuje přírůstkové vylepšení stávající funkce. Protože se jedná pouze o vylepšení, nejsou uvedeny v seznamu [plán vydání](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Aby se však zajistilo, že tato vylepšení nebudou v rozporu s vašimi stávajícími přizpůsobeními nebo předvolbami, je každé z nich ve výchozím nastavení vypnuto (pokud není uvedeno jinak).

Pokud chcete zapnout nebo vypnout některou z těchto funkcí, musíte to udělat ve [správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Název funkce ve správě funkcí | Další informace |
|---|---|---|
| Řízení výroby | Kontrola dostupnosti materiálu na vyžádání pro výrobní zakázky | Tato funkce umožňuje rychlejší otevření stránky **Výrobní zakázky pro uvolnění**, která je dostupná v pracovním prostoru **Správa výrobního provozu**. Bez této funkce systém automaticky zkontroluje, zda jsou dostupné materiály pro všechny uvedené výrobní zakázky, jakmile stránku otevřete, což může trvat velice dlouho, pokud máte velký počet zakázek. Pokud je tato funkce povolena, systém místo toho poskytuje tlačítko na panelu nástrojů, které můžete použít ke spuštění kontroly materiálu pouze u vybraných zakázek a v případě potřeby. |
| Řízení výroby | (Preview) Registrace spotřeby materiálu na rozhraní pro provádění výrobního provozu (mimo WMS) | Tato funkce umožňuje pracovníkům používat rozhraní k provádění výrobního provozu k registraci spotřeby materiálu, čísel šarží a sériových čísel. Tato funkce podporuje pouze položky, které nemají povoleno používat pokročilé skladové procesy (WMS). Podpora pro položky s podporou WMS je naplánována na budoucí vydání.<p>Někteří výrobci, zejména výrobci ve zpracovatelském průmyslu, potřebují explicitně registrovat množství spotřebovaného materiálu pro každou dávku nebo výrobní zakázku. Pracovníci mohou například používat váhu k vážení množství spotřebovaného materiálu při práci. Aby byla zajištěna úplná sledovatelnost materiálu, musí tyto organizace také registrovat, která čísla šarží byla spotřebována při výrobě každého produktu. |
| Řízení výroby | Vykázání jako dokončeno v úlohách správy skladu pro jednotky škálování cloudu a hraniční sítě | Tato funkce umožňuje pracovníkům používat mobilní aplikaci Warehouse Management k nahlášení výrobní nebo dávkové zakázky jako dokončené, když aplikace běží spolu s úlohou pro správu skladu v jednotce škálování cloudu a hraniční sítě. Další informace viz [Vykázání jako dokončené a odložené na jednotce škálování](../cloud-edge/cloud-edge-workload-manufacturing.md#RAF). |
| Řízení výroby | Zahájení výrobní zakázky v úlohách správy skladu pro jednotky škálování cloudu a hraniční sítě | Tato funkce umožňuje pracovníkům používat mobilní aplikaci Warehouse Management k zahájení výrobní nebo dávkové zakázky, když aplikace běží spolu s úlohou pro správu skladu v jednotce škálování cloudu a hraniční sítě. |
| Řízení skladu | Nové stránky pracovní plochy plánování vytížení | Aktivuje dvě nové stránky pracovní plochy pro plánování vytížení: **Pracovní plocha pro plánování příchozího vytížení** a **Pracovní plocha pro plánování odchozího vytížení**. |

## <a name="new-and-updated-documentation-resources"></a>Nové a aktualizované zdroje dokumentace

Nedávno jsme přidali nebo významně aktualizovali následující témata nápovědy. Tato témata nemusí nutně souviset s novými funkcemi, které byly přidány pro toto vydání, jak je uvedeno v předchozí části. Mohou vám však pomoci lépe využít stávající funkce.

| Oblast funkce | Nová nebo aktualizovaná témata |
|---|---|
| Správa nákladů | [Sestavy hodnot zásob](../cost-management/inventory-value-report-storage.md) |
| Správa nákladů | [Příklady a logika sestavy hodnoty zásob](../cost-management/inventory-value-report-examples.md) |
| Hlavní plánování | [Parametry data a času používané optimalizací plánování](../master-planning/planning-optimization/date-time-used.md) |
| Hlavní plánování | [Nastavení prognózy poptávky](../master-planning/demand-forecasting-setup.md) |
| Hlavní plánování | [Použití deníku pojistných zásob pro aktualizaci minimální disponibility položek](../master-planning/safety-stock-journal.md) |
| Řízení výroby | [Přizpůsobení rozhraní pro provádění výrobního provozu](../production-control/production-floor-execution-customize.md) |
| Řízení výroby | [Styl rozhraní pro provádění výrobního provozu](../production-control/production-floor-execution-styles.md) |
| Prodej a marketing | [Vylepšení výkonu čištění historie prodeje](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) |
| Řízení skladu | [Uživatelské účty mobilního zařízení](../warehousing/mobile-device-work-users.md) |

## <a name="additional-resources"></a>Další prostředky

### <a name="platform-updates-for-finance-and-operations-apps"></a>Aktualizace platformy pro aplikace Finance and Operations

Microsoft Dynamics 365 Supply Chain Management 10.0.24 zahrnuje aktualizace platformy. Další informace naleznete v tématu [Aktualizace platformy pro verze 10.0.24 aplikací Finance and Operations (listopad 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-24.md).

### <a name="bug-fixes"></a>Opravy chyb

Sháníte-li informace o opravách chyb zahrnutých v jednotlivých aktualizacích, které jsou součástí verze 10.0.24, přihlaste se ke službám Lifecycle Services (LCS) a přečtěte si [článek znalostní báze](https://fix.lcs.dynamics.com/Issue/Details?bugId=641306&dbType=3&qc=5b1d5e49c96b8a5cfb5601889a413e6f3773ba6500f9bc47310dcc5c54fff42f).

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 a průmyslová cloudová řešení: Plán vlny 2 vydání 2021

Zajímáte se o nadcházející a nedávno uvedené funkce jakékoliv z našich obchodních aplikací nebo platforem?

Přečtěte si [Dynamics 365 a průmyslová cloudová řešení: Plán vlny 2 vydání 2021](/dynamics365-release-plan/2021wave2/). Popsali jsme všechny podrobnosti, od A až do Z, v jednom dokumentu, který můžete používat pro plánování.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Odebrané a zastaralé funkce Supply Chain Management

Téma [Odebrané nebo zastaralé funkce v Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) popisuje funkce Supply Chain Management, které byly nebo jsou naplánovány k odebrání nebo které zastaraly.

- *Odstraněná* funkce již není k dispozici v produktu.
- *Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Před odebráním jakékoli funkce produktu bude oznámeno její zastarání v tématu [Odebrané nebo zastaralé funkce v Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 měsíců před odebráním.

U změn způsobujícíh chyby, které ovlivní pouze dobu kompilace, ale jsou v binárním formátu kompatibilní s prostředím sandbox a produkčními prostředími, bude doba zastarání kratší než 12 měsíců. Obvykle se jedná o funkční aktualizace, které je třeba provést v kompilátoru.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
