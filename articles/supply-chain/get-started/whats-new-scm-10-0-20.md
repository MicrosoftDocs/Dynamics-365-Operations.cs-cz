---
title: Náhled verze Dynamics 365 Supply Chain Management 10.0.20 (srpen 2021)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Supply Chain Management 10.0.20.
author: kamaybac
ms.date: 05/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a782416bdb12a8ac7f1ba807452ca54072af3ab5
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301739"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10020-august-2021"></a>Náhled verze Dynamics 365 Supply Chain Management 10.0.20 (srpen 2021)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tohle téma uvádí funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Supply Chain Management verze Preview 10.0.20. Tato verze má číslo sestavení 10.0.886 a je k dispozici následujícím způsobem:

- **Náhled verze:** květen 2021
- **Obecně dostupné vydání (automatická aktualizace):** červenec 2021
- **Obecně dostupné vydání (automatická aktualizace):** srpen 2021


## <a name="features-included-in-this-release"></a>Funkce zahrnuté do této verze

V následující tabulce je uveden seznam funkcí této verze. Sloupec *Funkce* poskytuje odkazy na [plán vydání](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features), kde můžete vidět oficiální datumy vydání jednotlivých funkcí. Sloupec *Další informace* obsahuje další podrobnosti a/nebo odkazy na související dokumentaci.

Většinu těchto funkcí je nutné povolit pomocí [Správy funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), než je budete moci použít. Některé z uvedených funkcí jsou stále ve verzi Preview, zatímco jiné již mohou být obecně dostupné.

| Oblast funkce | Funkce | Další informace |
|---|---|---|
| Zásoby&nbsp;a&nbsp;logistika | [Vylepšení výkonu podrobností prodejní objednávky](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-details-performance-enhancement) | Tato funkce umožňuje reagovat na uživatelské rozhraní při otevírání prodejních objednávek, zejména objednávek, které obsahují mnoho řádků. |
| Výroba | [Vyvolání toků automatizace procesů k vytvoření objednávek kvality](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/invoke-process-automation-flows-create-quality-orders) | [Vyvolání toků automatizace procesů k vytvoření objednávek kvality](../production-control/process-automation-quality-orders.md ) |
| Výroba | [Vylepšené uživatelské rozhraní pro provádění výrobního provozu](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-manufacturing) | [Konfigurace rozhraní pro provádění výrobního provozu](../production-control/production-floor-execution-configure.md) |
| Řízení informací o produktech | [Spravujte změny v recepturách a jejich látkách](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/engineering-change-management-support-process-manufacturing) | [Spravujte změny v recepturách a jejich látkách](../engineering-change-management/manage-formula-changes.md) |
| Řízení informací o produktech | [Kontroly připravenosti produktu](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/product-readiness-checks) | [Připravenost produktu](../engineering-change-management/product-readiness.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Vylepšení funkcí zahrnutých do této verze

V následující tabulce je uveden seznam vylepšených funkcí této verze. Každý z nich poskytuje přírůstkové vylepšení stávající funkce. Protože se jedná pouze o vylepšení, nejsou uvedeny v seznamu [plán vydání](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Aby se však zajistilo, že tato vylepšení nebudou v rozporu s vašimi stávajícími přizpůsobeními nebo předvolbami, je každé z nich ve výchozím nastavení vypnuto (pokud není uvedeno jinak). Pokud chcete použít některou z těchto funkcí, musíte ji výslovně povolit ve [Správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Oblast funkce | Vlastnosti&nbsp;název&nbsp;ve funkci&nbsp;řízení | Další informace |
|---|---|---|
| Hlavní plánování | Dny zpoždění pro Optimalizaci plánování | Tato funkce náhledu umožňuje optimalizaci plánování zohlednit toleranci zpoždění na základě parametru **Negativní dny** definovaného ve skupinách pokrytí. |
| Hlavní plánování | Paralelní autorizace upravené prognózy poptávky | Tato funkce umožňuje paralelní autorizaci upravené prognózy poptávky ze stránky **Upravená předpověď poptávky**. Záměrem této funkce je zvýšit výkon při autorizaci vysokého počtu prognóz. Při autorizaci může uživatel zadat **Počet vláken** v autorizačním dialogu. |
| Hlavní plánování | (Preview) Dávkové potvrzení a konsolidace pro plánované hromadné a balíkové dávkové objednávky | Tato funkce umožňuje používat dávkové úlohy k potvrzení a konsolidaci plánovaných hromadných a balíkových objednávek. |
| Řízení výroby | Zkopírujte obecné postupy | Tato funkce vylepšuje funkci kopírování trasy a umožňuje uživatelům kopírovat trasy, které nejsou specifické pro jednotlivé položky. Umožňuje systému aktualizovat všechny relevantní informace (například web, skupinu tras, požadavky na zdroje a různé časy) poté, co byla funkce kopírování trasy použita k přepsání trasy, která ještě není přiřazena k položce. |
| Řízení výroby | Aktualizovat související požadavky na zdroje při změně operace postupu | Tato funkce umožňuje systému aktualizovat související požadavky na zdroje po změně operace existujícího kroku postupu uživatelem. |
| Řízení informací o produktech | Kusovník předzpracovává zprávu, aby se zabránilo vypršení časového limitu | Tato funkce způsobí, že zpráva o kusovníku bude předběžně zpracována. Tím se vyhnete problémům s časovým limitem při velkém načtení dat pro sestavu. |
| Zásobování a zdroje | Povolit resetování pracovních postupů souvisejících se zásobováním | Tato funkce náhledu umožňuje obnovit následující pracovní postupy do stavu konceptu: Objednávka, Změna dodavatele a Požadavky na objednávku. |
| Správa přepravy | Povolit vytvoření deníku faktury dodavatele při vyřazování účtu dopravného | Když je tato funkce povolena, odpovídající deník faktur dodavatele bude vytvořen pouze z důvodů odsouhlasení, když používáte možnost dodavatele plateb. Jinak bude deník faktur vždy vytvořen. |
| Řízení skladu | Ověřit šablony vybrané pro práci doplnění | Tato funkce pomáhá zajistit, aby uživatelé při nastavování úlohy doplňování vybrali platné šablony doplňování. Zabraňuje uživatelům ve vytváření úlohy doplňování bez šablony a ve výběru šablon typu *Vlnová poptávka*, který nevytvoří žádné doplňovací práce a jeho zpracování může trvat dlouho. |

## <a name="new-and-updated-documentation-resources"></a>Nové a aktualizované zdroje dokumentace

Nedávno jsme přidali nebo významně aktualizovali následující témata nápovědy. Nemusí nutně souviset s novými funkcemi přidanými pro toto vydání, jak je uvedeno v předchozí části, ale mohou vám pomoci lépe využít stávající funkce.

| Oblast funkce | Nová nebo aktualizovaná témata |
|---|---|
| Správa technických změn | [Stavy životního cyklu produktu a transakce](../engineering-change-management/product-lifecycle-state-transactions.md) |
| Řízení zásob | [Doplněk viditelnosti zásob](../inventory/inventory-visibility.md)<br><br>[Přehled řízení kvality a neshod](../inventory/quality-management-processes.md) (plus všechna související témata řízení kvality) |
| Zásobování a zdroje | [Udržování certifikace dodavatele](../../finance/public-sector/manage-vendor-certification.md) |
| Řízení výroby | [Styl rozhraní pro provádění výrobního provozu](../production-control/production-floor-execution-styles.md) |
| Řízení skladu | [Přiřaďte ikony kroků a názvy pro mobilní aplikaci Warehouse Management](../warehousing/step-icons-titles.md)<br><br>[Odložené zpracování ručního pohybu zásob](../warehousing/deferred-processing-manual-inventory-movement.md) |

## <a name="additional-resources"></a>Další prostředky

### <a name="platform-updates-for-finance-and-operations-apps"></a>Aktualizace platformy pro aplikace Finance and Operations

Microsoft Dynamics 365 Supply Chain Management 10.0.20 zahrnuje aktualizace platformy. Další informace naleznete v tématu [Aktualizace platformy pro verze 10.0.20 aplikací Finance and Operations (červenec 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20.md). <!-- KFM: Confirm link -->

### <a name="bug-fixes"></a>Opravy chyb

Sháníte-li informace o opravách chyb zahrnutých v jednotlivých aktualizacích, které jsou součástí verze 10.0.20, přihlaste se ke službám Lifecycle Services (LCS) a přečtěte si [článek znalostní báze](https://fix.lcs.dynamics.com/Issue/Details?bugId=586707&dbType=3&qc=d0dad8eee2af234e8c288e2a7df14c579004518673d014be511f900cfed008f8). 

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
