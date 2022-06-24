---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Supply Chain Management 10.0.23 (leden 2022)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Supply Chain Management 10.0.23.
author: kamaybac
ms.date: 10/15/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: acffe97cf1844f16a70c716a7f2078b1e9a072d1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849467"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10023-january-2022"></a>Co je nového nebo změněného v aplikaci Dynamics 365 Supply Chain Management 10.0.23 (leden 2022)

[!include [banner](../includes/banner.md)]

Tento článek uvádí funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Supply Chain Management verze 10.0.23. Tato verze má číslo sestavení 10.0.1037 a je k dispozici následujícím způsobem:

- **Verze Preview:** Říjen 2021
- **Obecně dostupné vydání (automatická aktualizace):** Prosinec 2021
- **Obecně dostupné vydání (automatická aktualizace):** Leden 2022

## <a name="features-included-in-this-release"></a>Funkce zahrnuté do této verze

V následující tabulce je uveden seznam funkcí této verze. Sloupec *Funkce* poskytuje odkazy na [plán vydání](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features), kde můžete vidět oficiální datumy vydání jednotlivých funkcí. Sloupec *Další informace* obsahuje další podrobnosti a/nebo odkazy na související dokumentaci. Chcete -li zjistit, jak zapnout funkci, podívejte se na sloupec *Povoleno uživatelem*. Další informace o tom, jak používat správu funkcí, naleznete v tématu [Přehled správy funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Tento článek můžeme aktualizovat, aby obsahovalo funkce, které se dostaly do sestavení poté, co byl tento článek původně publikován.

| Oblast funkce | Funkce | Další informace | Povolil/a   |
|---|---|---|---|
| Globální adresář | Definujte výchozí stát/provincii pro každou zemi/oblast v nastavení adresy | Nyní můžete definovat výchozí stát/provincii pro každou zemi/oblast v nastavení adresy pro globální adresář. Když je nastaven výchozí stát/provincie, bude to výchozí hodnota zadaná do polí pro stát/provincii, když vytvoříte nový záznam okresu nebo města pro danou zemi/oblast. Viz také [Nastavení adresy](../../fin-ops-core/fin-ops/organization-administration/global-address-book-address-setup.md?toc=/dynamics365/supply-chain/toc.json) | Ve výchozím nastavení povoleno. |
| Zásoby&nbsp;a&nbsp;logistika | [Pozastavení úloh v mobilní aplikaci Warehouse Management](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/park-tasks-warehouse-management-mobile-app) | [Konfigurace náhradního procesu pro kroky v položkách nabídky mobilního zařízení](../warehousing/warehouse-app-detours.md) | Správa funkce (*Obcházení aplikace Warehouse Management*) |
| Zásoby&nbsp;a&nbsp;logistika | [Propagovaná pole aplikace skladu](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [Konfigurace propagovaných polí pro kroky v mobilním zařízení](../warehousing/warehouse-app-promoted-fields.md)| Správa funkcí (*Propagovaná pole aplikace Warehouse*) |
| Výroba | [Integrace výrobních informačních systémů](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-systems-integration) | [Integrace s výrobními informačními systémy třetích stran](../production-control/mes-integration.md) | Správa funkcí (*Integrace výrobního informačního systému*) |
| Výroba | [Zpráva o vedlejších a souběžných produktech z rozhraní pro provádění výrobního provozu](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-process-manufacturing) | [Jak pracovníci používají rozhraní pro provádění výrobního provozu](../production-control/production-floor-execution-use.md) | Správa funkcí (*Zpráva o vedlejších a souběžných produktech z rozhraní pro provádění výrobního provozu*) |
| Plánování | [Podpora optimalizace plánování u plánování na základě priority](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-priority-based-planning) | [Plánování na základě priority](../master-planning/planning-optimization/priority-based-planning.md) | Správa funkcí (*Podpora MRP řízená prioritou pro Optimalizaci plánování*) |

## <a name="feature-enhancements-included-in-this-release"></a>Vylepšení funkcí zahrnutých do této verze

V následující tabulce je uveden seznam nových funkcí této verze. Každé z těchto vylepšení poskytuje přírůstkové vylepšení stávající funkce. Protože se jedná pouze o vylepšení, nejsou uvedeny v seznamu [plán vydání](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Aby se však zajistilo, že tato vylepšení nebudou v rozporu s vašimi stávajícími přizpůsobeními nebo předvolbami, je každé z nich ve výchozím nastavení vypnuto (pokud není uvedeno jinak).

Pokud chcete některou z těchto funkcí zapnout nebo vypnout, musíte tak učinit v části [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), kde jsou uvedeny pomocí jmen uvedených ve sloupci *Název funkce ve správě funkcí* následující tabulky.

| Modul | Název funkce ve správě funkcí | Další informace |
|---|---|---|
| Správa majetku | Ofsetové účty výdajů v denících pracovních příkazů | Tato funkce umožňuje zadat kompenzační účet pro každý výdaj uvedený v deníku pracovních příkazů. Obvykle můžete ke každému výdaji přiřadit účet dodavatele, ale jsou podporovány i jiné typy účtů. Přidává dva nové sloupce (**Typ offsetového účtu** a **Offsetový účet**) k pevné záložce **Výdaj** na stránce **Deník pracovních příkazů**.|
| Správa nákladů | Vytvořit související doklady pro přecenění zaokrouhlování standardních nákladů | <p>Když je provedeno finanční zaúčtování zásob (například faktura prodejní objednávky nebo transakce zásob), tato funkce způsobí, že systém vytvoří samostatný doklad pro jakékoli související přecenění zaokrouhlování standardních nákladů a připojí jej k dokladu o finančním účtování jako související doklad.</p><p>Bez této funkce systém zaznamenává standardní přecenění zaokrouhlení nákladů na stejné zaúčtování poukázky. Toto chování může někdy způsobit konfliktní informace o datu, protože přecenění používají relaci nebo systémové datum, zatímco finanční účtování používá datum účtování.</p> |
| Řízení zásob a skladu | \[Rusko\] Zaúčtovat transakce stornování finančních zásob podle opravného příznaku ve finančním dokladu pro prodejní objednávky | Tato funkce má vliv na funkci oprav dobropisů pro Rusko. Umožňuje zaúčtování inventurních transakcí pro prodejní faktury v souladu s možností opravy v hlavní knize. Když je tato funkce povolena, již nejsou žádné nesrovnalosti mezi příznakem **Oprava** na finanční doklad transakce zásob a příznakem **Storno** na skladových transakcích. |
| Řízení zásob a skladu | (Rusko) Spustit hromadný výpočet sestavy obratu salda zásob | V ruských lokalizacích Supply Chain Management tato funkce umožňuje hromadně spouštět sestavu *obratu salda zásob*, uložit ji a prohlížet zprávy vygenerované dříve. |
| Řízení zásob a skladu | (Rusko) Použít překlady do místního jazyka v primárních formulářích specifických pro danou zemi nebo oblast v řízení zásob | V ruských lokalizacích Supply Chain Management tato funkce umožňuje použití ruských překladů pro názvy produktů či položek a měrných jednotek v následujících výtiscích zásob specifických pro Rusko:Inventurní seznam (INV-3),Inventurní seznam (INV-5),Inventurní seznam (INV-6). |
| Hlavní plánování | Služba Azure Machine Learning Service pro prognózy poptávky | Tato funkce umožňuje službě Azure Machine Learning Service generovat prognózy poptávky na základě historických dat. Další informace viz [Nastavení prognózy poptávky](../master-planning/demand-forecasting-setup.md). |
| Zásobování a zdroje | Vyčistit historii aktualizace nákupní objednávky | Tato funkce vám umožňuje vyčistit dočasné historické záznamy související s aktualizacemi nákupních objednávek. Přidává nové tlačítko s názvem **Vyčistit historii aktualizací nákupů** do podokna akcí na stránce **Všechny nákupní objednávky**. Tato funkce je povolena ve výchozím nastavení. |
| Řízení výroby | (Preview) Automatické vyskladňování materiálů s povoleným skladem pro automaticky účtované výdejky | Tato funkce vám umožňuje automaticky vydávat a řešit dimenze zásob pro automaticky zaúčtované, odvozené a zpětně účtované deníky výdejek. |
| Řízení výroby | Potvrdit expiraci surovin oproti plánovanému datu spotřeby | Tato funkce mění způsob, jakým se ověřují data expirace šarže při rezervaci šarže suroviny, která má být použita během výroby. Když je tato funkce povolena, datum vypršení šarže se ověřuje proti datu plánované spotřeby (datum suroviny), jak je stanoveno na řádku výrobního kusovníku nebo řádku vzorce dávkové objednávky. Když je tato funkce zakázána, je datum vypršení šarže ověřeno oproti plánovanému datu dodání výrobní nebo dávkové zakázky (jako dříve). |
| Prodej a marketing | Vyčistění historie aktualizace prodejů na základě stáří | Tato funkce umožňuje nastavit maximální stáří záznamů, které se mají uchovávat při spuštění periodické úlohy **Vyčištění historie aktualizace prodeje**. Starší záznamy budou smazány. To je užitečné, když nastavíte pravidelné spouštění úlohy, protože stáří se vždy počítá vzhledem k datu spuštění úlohy. Bez této funkce můžete nastavit pouze konkrétní datum pro uchování nejstarších záznamů. Další informace viz [Vymazání historických dat plánu prodeje](../sales-marketing/sales-update-history-cleanup-performance-improvements.md). |
| Prodej a marketing | Zlepšit výkonnost sestavy „Prvních 100“ zákazníků | Tato funkce zlepšuje výkon sestavy zákazníků **Top 100** tím, že se sestava vždy spouští u všech zákazníků (což je její zamýšlené použití) místo umožnění vlastních dotazů. Když je tato funkce povolena, všechna nastavení **Záznamy k zahrnutí** jsou zakázána v dialogovém okně sestavy **Top 100**. |
| Řízení skladu | Podpora jednoty škálování pro uvolnění odchozích objednávek do skladu | Když je tato funkce povolena, mohou být odchozí objednávky uvolněny z centra přímo na jednotku měřítka, odkud budou objednávky splněny. |

## <a name="new-and-updated-documentation-resources"></a>Nové a aktualizované zdroje dokumentace

Nedávno jsme přidali nebo významně aktualizovali následující články nápovědy. Tento článek nemusí nutně souviset s novými funkcemi, které byly přidány pro toto vydání, jak je uvedeno v předchozí části. Mohou vám však pomoci lépe využít stávající funkce.

| Oblast funkce | Nové nebo aktualizované články |
|---|---|
| Správa technických změn | [Technické atributy a vyhledávání technických atributů](../engineering-change-management/engineering-attributes-and-search.md) nyní popisuje, jak funguje dědění technického atributu. |
| Hlavní plánování | [Hlavní plánování s prognózami poptávky](../master-planning/planning-optimization/demand-forecast.md) a [Redukční klíče prognózy](../master-planning/reduction-keys.md) nyní poskytuje více informací o tom, jak pracovat s redukčními klíči. |
| Hlavní plánování | [Bezpečnostní plnění zásob pro položky](../master-planning/safety-stock-replenishment.md) nyní poskytuje více informací o používání klíčů minimum/maximum. |
| Hlavní plánování | [Prognózy zásob](../master-planning/inventory-forecast.md) nyní poskytuje více informací o přidělování prognóz. |
| Hlavní plánování | [Plán dodávek](../master-planning/supply-schedule.md) |
| Řízení skladu | [Globální parametry mobilního zařízení](../warehousing/mobile-device-parameters.md) |
| Řízení skladu | [Ukotvení](../warehousing/anchoring.md) |
| Prodej a marketing | Mezipodnikový obchod je nyní podrobně popsán, počínaje [Nastavení mezipodnikového obchodu](../sales-marketing/intercompany-trade-set-up.md) a s tím souvisejících článcích. |
| Prodej a marketing | [Vylepšení výkonu čištění historie prodeje](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) |
| Řízení zásob | Dokumentace viditelnosti zásob byla rozšířena a aktualizována počínaje [Přehled doplňku Viditelnost zásob](../inventory/inventory-visibility.md) a s tím souvisejícími články. |
| Řízení skladu | [Uživatelské účty mobilního zařízení](../warehousing/mobile-device-work-users.md) |

## <a name="additional-resources"></a>Další prostředky

### <a name="platform-updates-for-finance-and-operations-apps"></a>Aktualizace platformy pro finanční a provozní aplikace

Microsoft Dynamics 365 Supply Chain Management 10.0.23 zahrnuje aktualizace platformy. Další informace naleznete v tématu [Aktualizace platformy pro verze 10.0.23 aplikací Finance a Operace (listopad 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-23.md).

### <a name="bug-fixes"></a>Opravy chyb

Sháníte-li informace o opravách chyb zahrnutých v jednotlivých aktualizacích, které jsou součástí verze 10.0.23, přihlaste se ke službám Lifecycle Services (LCS) a přečtěte si [článek znalostní báze](https://fix.lcs.dynamics.com/Issue/Details?bugId=627874&dbType=3&qc=9b7e01944eb8b43f9c3aac4be26811c27be205847d6d2a240424f34f7e722910).

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 a průmyslová cloudová řešení: Plán vlny 2 vydání 2021

Zajímáte se o nadcházející a nedávno uvedené funkce jakékoliv z našich obchodních aplikací nebo platforem?

Přečtěte si [Dynamics 365 a průmyslová cloudová řešení: Plán vlny 2 vydání 2021](/dynamics365-release-plan/2021wave2/). Popsali jsme všechny podrobnosti, od A až do Z, v jednom dokumentu, který můžete používat pro plánování.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Odebrané a zastaralé funkce Supply Chain Management

Článek [Odebrané nebo zastaralé funkce v Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) popisuje funkce Supply Chain Management, které byly nebo jsou naplánovány k odebrání nebo které zastaraly.

- *Odstraněná* funkce již není k dispozici v produktu.
- *Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Před odebráním jakékoli funkce produktu bude oznámeno její zastarání v článku [Odebrané nebo zastaralé funkce v Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 měsíců před odebráním.

U změn způsobujícíh chyby, které ovlivní pouze dobu kompilace, ale jsou v binárním formátu kompatibilní s prostředím sandbox a produkčními prostředími, bude doba zastarání kratší než 12 měsíců. Obvykle se jedná o funkční aktualizace, které je třeba provést v kompilátoru.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
