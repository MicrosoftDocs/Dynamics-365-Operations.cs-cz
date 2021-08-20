---
title: Preview verze Dynamics 365 Supply Chain Management 10.0.21 (říjen 2021)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Supply Chain Management 10.0.21.
author: kamaybac
ms.date: 08/02/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 517411512760374f1d1fd3b8ea3615563c47202c2e847569d00cb17a94657630
ms.sourcegitcommit: fa5ff2a0822aac16b518a2aea0d3389f79793390
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/07/2021
ms.locfileid: "7012030"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10021-october-2021"></a>Preview verze Dynamics 365 Supply Chain Management 10.0.21 (říjen 2021)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tohle téma uvádí funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Supply Chain Management verze Preview 10.0.21. Tato verze má číslo sestavení 10.0.960 a je k dispozici následujícím způsobem:

- **Preview verze:** Srpen 2021
- **Obecně dostupné vydání (automatická aktualizace):** Září 2021
- **Obecně dostupné vydání (automatická aktualizace):** Říjen 2021

## <a name="known-deployment-issue"></a>Známý problém s nasazením
Při nasazení verze 10.0.21 na IaaS můžete obdržet následující upozornění nasazení:

**Kód upozornění:** 95017

**Zpráva s upozorněním:** Neúspěšné spuštění skriptu [SetupDiagnostics] proti VM

Nasazení bude fungovat i přes toto upozornění, ale ve službě Lifecycle Services (LCS) mohou nastat následující známé problémy:

-   Na stránce **Sledování prostředí** se nezobrazí odkaz **Zobrazit podrobné informace o verzi**, takže neuvidíte konkrétní verze modulů nainstalovaných ve vašem prostředí. Bez těchto dat by následné opravy hotfix mohly selhat, protože proces, který používá opravy hotfix, používá tato data k ověření, že jsou splněny požadavky na verzi modulu. Protože sestavení PEAP/Preview není možné použít ve výrobě nebo v něm použít opravy hotfix, měl by být dopad minimální.
-   Karty **Měření výkonu** a **Analýza indexu** ve stránce **Sledování prostředí** nezobrazí v části SQL Insights žádná data. Všechny ostatní funkce **Sledování prostředí** budou fungovat podle očekávání.
-   Stránka **plná diagnostika systému** nebude přístupná. Přidružená data o stavu nočních běhů kolektorů dat a problémech zjištěných jeho pravidly se také nezobrazí.

## <a name="features-included-in-this-release"></a>Funkce zahrnuté do této verze

V následující tabulce je uveden seznam funkcí této verze. Sloupec *Funkce* poskytuje odkazy na [plán vydání](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features), kde můžete vidět oficiální datumy vydání jednotlivých funkcí. Sloupec *Další informace* obsahuje další podrobnosti a/nebo odkazy na související dokumentaci.

Většinu těchto funkcí je nutné povolit pomocí [Správy funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), než je budete moci použít. Některé z uvedených funkcí jsou stále ve verzi Preview, zatímco jiné již mohou být obecně dostupné.

| Oblast funkce | Funkce | Další informace |
|---|---|---|
| Zásoby&nbsp;a&nbsp;logistika | [Doplněk Globální účetnictví zásob pro Dynamics 365 Supply Chain Management](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/global-inventory-accounting-add-in-dynamics-365-supply-chain-management) | [Domovská stránka globálního skladového účetnictví](../global-inventory-accounting/global-inventory-accounting-home.md) |
| Zásoby&nbsp;a&nbsp;logistika | [Zaúčtovat úpravy množství na skladě pomocí konfigurovatelných kódů důvodu připojených k protiúčtům](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/post-on-hand-adjustments-using-configurable-reason-codes-connected-offset-accounts) | [Kódy důvodů pro inventury zásob](../warehousing/reason-codes-for-counting-journals.md) |
| Zásoby&nbsp;a&nbsp;logistika | [Zásady exportu dat odkazující na prodejní nabídku](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy) | Určete, zda změny dat odkazovaných v nabídkách způsobí zahrnutí těchto nabídek (nebo řádků) do dalšího přírůstkového exportu. Pokud se rozhodnete nezahrnout tyto nabídky nebo řádky, vaše přírůstkové exporty poběží rychleji.<br><br>Tato funkce přidává nastavení s názvem **Vynechat data odkazovaná v prodejních nabídkách při sledování změn** do stránky **Parametry pohledávek**. |
| Zásoby&nbsp;a&nbsp;logistika | [Skenování čárových kódů ve skladu pomocí standardů formátu GS1](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) | *Již brzy*<!-- KFM: Add doc link when ready. --> |
| Zásoby&nbsp;a&nbsp;logistika | Zapečetěné nabídky <!-- KFM: Add RP link when available --> | *Již brzy*<!-- KFM: Add doc link when ready. --> |
| Zásoby&nbsp;a&nbsp;logistika | [Vylepšení odpočtů a skutečné hmotnosti ve správě rabatu](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/deduction-catch-weight-enhancements-rebate-management) | [Správa odpočtů pomocí pracovní plochy odpočtu](../rebate-management/deduction-workbench.md )<br><br>[Zpracování, kontrola a zaúčtování rabatu](../rebate-management/process-review-post.md)<br><br>[Obchody správy rabatu](../rebate-management/rebate-management-deals.md) |
| Zásoby&nbsp;a&nbsp;logistika | [Pokyny ke kroku aplikace skladu](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | *Již brzy*<!-- KFM: Add doc link when ready --> |
| Zásoby&nbsp;a&nbsp;logistika | [Pracovní přestávky a sledování aktualizací u nákladů za doručení](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/work-breaks-tracking-updates-landed-cost) | [Aktualizovat sledování pro odložení](../landed-cost/update-tracking-putaway.md )<br><br>[Zpracování přepravovaného zboží](../landed-cost/in-transit-processing.md) |
| Hlavní plánování | [Dny zpoždění pro Optimalizaci plánování](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/negative-days-support-planning-optimization) | [Tolerance zpoždění (záporné dny)](../master-planning/planning-optimization/delay-tolerance.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Vylepšení funkcí zahrnutých do této verze

V následující tabulce je uveden seznam vylepšených funkcí této verze. Každý z nich poskytuje přírůstkové vylepšení stávající funkce. Protože se jedná pouze o vylepšení, nejsou uvedeny v seznamu [plán vydání](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Aby se však zajistilo, že tato vylepšení nebudou v rozporu s vašimi stávajícími přizpůsobeními nebo předvolbami, je každé z nich ve výchozím nastavení vypnuto (pokud není uvedeno jinak). Pokud chcete použít některou z těchto funkcí, musíte ji výslovně povolit ve [Správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Oblast funkce | Vlastnosti&nbsp;název&nbsp;ve funkci&nbsp;řízení | Další informace |
|---|---|---|
| Správa nákladů | Podrobnosti o průběhu uzávěrky zásob | Tato funkce preview umožňuje detailní zobrazení průběhu uzávěrky zásob. |
| Hlavní plánování | (Preview) Podpora MRP řízená prioritou pro optimalizaci plánování | Tato funkce preview Optimalizace plánování umožňuje hlavní plánování řízené prioritou plánování s bodem přiobjednání. Mezi zvýrazněné změny patří: pole **Priorita plánování** na řádcích prodejní objednávky, řádcích nákupní objednávky, prognóze poptávky a plánovaných objednávkách; nová možnost kódu disponibility; pole **Disponibilita položky** pole pro bod přiobjednání; formuláře nastavení hlavního plánování pro řízení nastavení priority plánování; a logika výpočtu Optimalizace plánování k nastavení a respektování priority plánování. |
| Zásobování a zdroje | Zabránit nadměrné spotřebě rezervací účelových položek rozpočtu, když je v pracovním postupu více nákupních žádanek | Tato funkce preview vylepšuje kontrolu chyb, když uživatelé odesílají a schvalují nákupní žádanky, které překračují zbývající zůstatek řádku rezervace účelových položek rozpočtu. To pomáhá předcházet nadměrné spotřebě rezervace účelových položek rozpočtu, když je v pracovním postupu více nákupních žádanek. |
| Řízení výroby | Zobrazit celé sériové číslo, číslo dávky a registrační značku v rozhraní provádění výrobního provozu | Tato funkce poskytuje vylepšené prostředí k prohlížení seznamů sériových, dávkových a registračních čísel v rozhraní pro provádění výrobního provozu. Zobrazení se změní ze zobrazení karty s omezeným počtem znaků na zobrazení seznamu, ve kterém je dostatek prostoru pro zobrazení celých hodnot. Seznam také poskytuje možnost vyhledávat konkrétní čísla. |
| Řízení skladu | Odpojit odloženou práci od ASN | Tato funkce je vyžadována k odesílání a přijímání rozšířených oznámení expedice (ASN), když spouštíte úlohu správy skladu na jednotce škálování (jako součást distribuované hybridní topologie). Přidává novou databázovou tabulku určenou k ukládání informací o práci vyskladnění. Dříve byly tyto informace uloženy v tabulkách používaných také pro ASN. |
| Řízení skladu | Umístit smíšené jednotky do slotu | Umožňuje systému vkládat položky na místa, která obsahují smíšené jednotky (například krabice a pouzdra). U každého řádky šablony slotingu vám tato funkce umožňuje zvolit, zda má řádek vkládat položky do umístění se smíšenou jednotkou nebo jednou jednotkou. |
| Řízení skladu | Použijte rychlejší rozhraní API pro zavírání/opětovné otevírání kontejnerů na balicí stanici | Když je tato funkce preview povolena, transakce zásob související s kontejnery se vytvářejí pomocí nového zjednodušeného procesu, který zlepšuje výkon zavírání nebo opětovného otevírání kontejnerů během ručního zpracování ve stanici balení. |

## <a name="new-and-updated-documentation-resources"></a>Nové a aktualizované zdroje dokumentace

Nedávno jsme přidali nebo významně aktualizovali následující témata nápovědy. Nemusí nutně souviset s novými funkcemi přidanými pro toto vydání, jak je uvedeno v předchozí části, ale mohou vám pomoci lépe využít stávající funkce.

| Oblast funkce | Nová nebo aktualizovaná témata |
|---|---|
| Hlavní plánování | [Prognózy zásob](../master-planning/inventory-forecast.md) |
| Hlavní plánování | [Parametry, které optimalizace plánování nepoužívá](../master-planning/planning-optimization/not-used-parameters.md) |
| Hlavní plánování | [Metody doplnění a modifikace množství](../master-planning/planning-optimization/replenishment-methods-quantity-modification.md) |
| Hlavní plánování | [Plánování s nekonečnou kapacitou](../master-planning/planning-optimization/infinite-capacity-planning.md) |
| Hlavní plánování | [Zobrazení historie pánů a plánovacích protokolů](../master-planning/planning-optimization/plan-history-logs.md) |
| Řízení skladu | [Strategie balení kontejnerů](../warehousing/container-packing-strategy-overview.md) |
| Řízení skladu | [Příkladové scénáře cyklické inventury](../warehousing/cycle-counting-scenarios.md) |
| Řízení skladu | [Import příchozích ASN prostřednictvím datové entity V2](../warehousing/import-asn-v2-data-entity.md) |
| Řízení skladu | [Nadměrné vyskladnění u prodejních objednávek a převodních příkazů](../warehousing/over-picking-for-sales-and-transfer-orders.md) |
| Řízení skladu | [Plánování tisku štítků vlny během vlny](../warehousing/configure-task-based-wave-label-printing.md) |
| Řízení skladu | [Co je nového nebo změněného v mobilní aplikaci Warehouse Management](../warehousing/whats-new-wma.md) |

## <a name="additional-resources"></a>Další prostředky

### <a name="platform-updates-for-finance-and-operations-apps"></a>Aktualizace platformy pro aplikace Finance and Operations

Microsoft Dynamics 365 Supply Chain Management 10.0.21 zahrnuje aktualizace platformy. Další informace naleznete v tématu [Aktualizace platformy pro verze 10.0.21 aplikací Finance and Operations (říjen 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21.md).

### <a name="bug-fixes"></a>Opravy chyb

Sháníte-li informace o opravách chyb zahrnutých v jednotlivých aktualizacích, které jsou součástí verze 10.0.21, přihlaste se ke službám Lifecycle Services (LCS) a přečtěte si [článek znalostní báze](https://fix.lcs.dynamics.com/Issue/Details?bugId=605166&dbType=3&qc=4b9449bf0d947113983bd0697140bf4d8727bfafd5566aa682cb38db343374de).

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
