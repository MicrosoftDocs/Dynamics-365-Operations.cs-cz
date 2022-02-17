---
title: Co je nového nebo co se změnilo v aplikaci Dynamics 365 Supply Chain Management 10.0.21 (říjen 2021)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Supply Chain Management 10.0.21.
author: kamaybac
ms.date: 10/28/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: ec7fcb97bd46551846ccee13b369a1b02a589688
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075292"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10021-october-2021"></a>Co je nového nebo co se změnilo v aplikaci Dynamics 365 Supply Chain Management 10.0.21 (říjen 2021)

[!include [banner](../includes/banner.md)]

Tohle téma uvádí funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Supply Chain Management verze 10.0.21. Tato verze má číslo sestavení 10.0.960 a je k dispozici následujícím způsobem:

- **Preview verze:** Srpen 2021
- **Obecně dostupné vydání (automatická aktualizace):** Září 2021
- **Obecně dostupné vydání (automatická aktualizace):** Říjen 2021

## <a name="features-included-in-this-release"></a>Funkce zahrnuté do této verze

V následující tabulce je uveden seznam funkcí této verze. Sloupec *Funkce* poskytuje odkazy na [plán vydání](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features), kde můžete vidět oficiální datumy vydání jednotlivých funkcí. Sloupec *Další informace* obsahuje další podrobnosti a/nebo odkazy na související dokumentaci.

Většinu těchto funkcí je nutné povolit pomocí [Správy funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), než je budete moci použít.

| Oblast funkce | Funkce | Další informace |
|---|---|---|
| Zásoby&nbsp;a&nbsp;logistika | [Doplněk Globální účetnictví zásob pro Dynamics 365 Supply Chain Management](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/global-inventory-accounting-add-in-dynamics-365-supply-chain-management) | [Domovská stránka globálního skladového účetnictví](../global-inventory-accounting/global-inventory-accounting-home.md) |
| Zásoby&nbsp;a&nbsp;logistika | [Zaúčtovat úpravy množství na skladě pomocí konfigurovatelných kódů důvodu připojených k protiúčtům](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/post-on-hand-adjustments-using-configurable-reason-codes-connected-offset-accounts) | [Kódy důvodů pro inventury zásob](../warehousing/reason-codes-for-counting-journals.md) |
| Zásoby&nbsp;a&nbsp;logistika | [Zásady exportu dat odkazující na prodejní nabídku](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy) | Určete, zda změny dat odkazovaných v nabídkách způsobí zahrnutí těchto nabídek (nebo řádků) do dalšího přírůstkového exportu. Pokud se rozhodnete nezahrnout tyto nabídky nebo řádky, vaše přírůstkové exporty poběží rychleji.<br><br>Tato funkce přidává nastavení s názvem **Vynechat data odkazovaná v prodejních nabídkách při sledování změn** do stránky **Parametry pohledávek**. |
| Zásoby&nbsp;a&nbsp;logistika | [Zapečetěné nabídky](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sealed-bidding) | [Zapečetěné nabídky pro požadavky na nabídku](../procurement/sealed-bidding.md) |
| Zásoby&nbsp;a&nbsp;logistika | [Předběžná rezervace pro doplněk Viditelnost zásob](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/soft-reservation-inventory-visibility-add-in) | [Rezervace viditelnosti zásob](../inventory/inventory-visibility-reservations.md) |
| Zásoby&nbsp;a&nbsp;logistika | [Vylepšení odpočtů a skutečné hmotnosti ve správě rabatu](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/deduction-catch-weight-enhancements-rebate-management) | [Správa odpočtů pomocí pracovní plochy odpočtu](../rebate-management/deduction-workbench.md )<br><br>[Zpracování, kontrola a zaúčtování rabatu](../rebate-management/process-review-post.md)<br><br>[Obchody správy rabatu](../rebate-management/rebate-management-deals.md) |
| Zásoby&nbsp;a&nbsp;logistika | [Pokyny ke kroku aplikace skladu](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [Přizpůsobení názvů kroků a pokyny pro mobilní aplikaci Warehouse Management](../warehousing/mobile-app-titles-instructions.md) |
| Zásoby&nbsp;a&nbsp;logistika | [Pracovní přestávky a sledování aktualizací u nákladů za doručení](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/work-breaks-tracking-updates-landed-cost) | [Aktualizovat sledování pro odložení](../landed-cost/update-tracking-putaway.md )<br><br>[Zpracování přepravovaného zboží](../landed-cost/in-transit-processing.md) |
| Hlavní plánování | [Dny zpoždění pro Optimalizaci plánování](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/negative-days-support-planning-optimization) | [Tolerance zpoždění (záporné dny)](../master-planning/planning-optimization/delay-tolerance.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Vylepšení funkcí zahrnutých do této verze

V následující tabulce je uveden seznam vylepšených funkcí této verze. Každý z nich poskytuje přírůstkové vylepšení stávající funkce. Protože se jedná pouze o vylepšení, nejsou uvedeny v seznamu [plán vydání](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Aby se však zajistilo, že tato vylepšení nebudou v rozporu s vašimi stávajícími přizpůsobeními nebo předvolbami, je každé z nich ve výchozím nastavení vypnuto (pokud není uvedeno jinak). Pokud chcete použít některou z těchto funkcí, musíte ji výslovně povolit ve [Správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Vlastnosti&nbsp;název&nbsp;ve funkci&nbsp;řízení | Další informace |
|---|---|---|
| Správa nákladů | Podrobnosti o průběhu uzávěrky zásob | Tato funkce preview umožňuje detailní zobrazení průběhu uzávěrky zásob. |
| Zásobování a zdroje | Zabránit nadměrné spotřebě rezervací účelových položek rozpočtu, když je v pracovním postupu více nákupních žádanek | Tato funkce preview vylepšuje kontrolu chyb, když uživatelé odesílají a schvalují nákupní žádanky, které překračují zbývající zůstatek řádku rezervace účelových položek rozpočtu. To pomáhá předcházet nadměrné spotřebě rezervace účelových položek rozpočtu, když je v pracovním postupu více nákupních žádanek. |
| Řízení výroby | Zobrazit celé sériové číslo, číslo dávky a registrační značku v rozhraní provádění výrobního provozu | Tato funkce poskytuje vylepšené prostředí k prohlížení seznamů sériových, dávkových a registračních čísel v rozhraní pro provádění výrobního provozu. Zobrazení se změní ze zobrazení karty s omezeným počtem znaků na zobrazení seznamu, ve kterém je dostatek prostoru pro zobrazení celých hodnot. Seznam také poskytuje možnost vyhledávat konkrétní čísla. |
| Prodej a marketing | Omezit počet prodejních objednávek, které lze vybrat k zaúčtování | Tato funkce vám umožňuje definovat maximální počet prodejních objednávek, které lze vybrat při odesílání potvrzení, výdejek, dodacích listů a faktur ze stránky seznamu prodejních objednávek. Je povoleno automaticky. Funkce přidává nastavení s názvem **Max. počet prodejních objednávek k zaúčtování** na stránku **Parametry pohledávek**. Nové nastavení má výchozí hodnotu *100*. Tato funkce pomáhá zlepšit výkon stránky seznamu prodejních objednávek, když je vybrán značný počet prodejních objednávek. Nemá to žádný vliv na počet prodejních objednávek, které lze zpracovat periodickým úkolem. |
| Řízení skladu | Odpojit odloženou práci od ASN | Tato funkce je vyžadována k odesílání a přijímání rozšířených oznámení expedice (ASN), když spouštíte úlohu správy skladu na jednotce škálování (jako součást distribuované hybridní topologie). Přidává novou databázovou tabulku určenou k ukládání informací o práci vyskladnění. Dříve byly tyto informace uloženy v tabulkách používaných také pro ASN. |
| Řízení skladu | Umístit smíšené jednotky do slotu | Umožňuje systému vkládat položky na místa, která obsahují smíšené jednotky (například krabice a pouzdra). U každého řádky šablony slotingu vám tato funkce umožňuje zvolit, zda má řádek vkládat položky do umístění se smíšenou jednotkou nebo jednou jednotkou. |
| Řízení skladu | Použijte rychlejší rozhraní API pro zavírání/opětovné otevírání kontejnerů na balicí stanici | Když je tato funkce preview povolena, transakce zásob související s kontejnery se vytvářejí pomocí nového zjednodušeného procesu, který zlepšuje výkon zavírání nebo opětovného otevírání kontejnerů během ručního zpracování ve stanici balení. |

## <a name="features-turned-on-by-default-in-this-release"></a>Funkce v této verzi zapnuté ve výchozím nastavení

V následující tabulce je uveden seznam funkcí, které jsou ve verzi 10.0.21 ve výchozím nastavení zapnuté. Většinu funkcí, které byly automaticky zapnuty, lze vypnout v části [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Název funkce | Povolit datum | Funkce přidána | Stav funkce | Modul |
| :--- | :--- | :--- | :--- | :--- |
| Úložiště sestavy zásob na skladě | 1. 9. 2021 | 1. 4. 2020 | Zapnuto ve výchozím nastavení | Řízení zásob a skladu |
| Zrušení převodního příkazu | 1. 9. 2021 | 13. 7. 2020 | Zapnuto ve výchozím nastavení | Řízení zásob a skladu |
| Odemknout deník zásob | 1. 9. 2021 | 17. 8. 2020 | Zapnuto ve výchozím nastavení | Řízení zásob a skladu |
| Uložená zobrazení pro řízení zásob | 1. 9. 2021 | 30. 9. 2020 | Zapnuto ve výchozím nastavení | Řízení zásob a skladu |
| Navigace do verze kusovníku z řádků kusovníku | 1. 9. 2021 | 11. 11. 2019 | Zapnuto ve výchozím nastavení | Řízení zásob a skladu |
| Použití měrné jednotky a jednotkového množství v denících zásob | 1. 9. 2021 | 11. 11. 2019 | Zapnuto ve výchozím nastavení | Řízení zásob a skladu |
| Povolit prázdné hodnoty atributů dávky | 1. 9. 2021 | 11. 11. 2019 | Zapnuto ve výchozím nastavení | Řízení zásob a skladu |
| Automatické navyšování čísel řádků převodních příkazů zásob | 1. 9. 2021 | 11. 10. 2019 | Zapnuto ve výchozím nastavení | Řízení zásob a skladu |
| Workflow schválení deníku zásob | 1. 9. 2021 | 6. 1. 2020 | Zapnuto ve výchozím nastavení | Řízení zásob a skladu |
| Povolit funkci upozornění na parametry správy kvality zásob | 1. 9. 2021 | 7. 10. 2019 | Zapnuto ve výchozím nastavení | Řízení zásob a skladu |
| Vytvořit převodní příkaz z řádku prodeje | 1. 9. 2021 | 31. 8. 2019 | Zapnuto ve výchozím nastavení | Řízení zásob a skladu |
| Výběr modelu prognózy v podrobnostech prognózy poptávky | 1. 9. 2021 | 11. 10. 2019 | Zapnuto ve výchozím nastavení | Hlavní plánování |
| Znázornění průběhu hlavního plánování | 1. 9. 2021 | 7. 10. 2019 | Zapnuto ve výchozím nastavení | Hlavní plánování |
| Automatické potvrzování pro optimalizaci plánování | 1. 9. 2021 | 11. 10. 2019 | Zapnuto ve výchozím nastavení | Hlavní plánování |
| Paralelní potvrzování plánovaných objednávek | 1. 9. 2021 | 31. 8. 2019 | Zapnuto ve výchozím nastavení | Hlavní plánování |
| Zpráva o úspěšném odeslání nabídky | 1. 9. 2021 | 15. 5. 2019 | Zapnuto ve výchozím nastavení | Zásobování a zdroje |
| Referenční odkaz požadavku na nabídku byl přidán do NO | 1. 9. 2021 | 31. 8. 2019 | Zapnuto ve výchozím nastavení | Zásobování a zdroje |
| Možnost dávkového potvrzení přijatých nákupních objednávek z dodavatelské spolupráce | 1. 9. 2021 | 10. 9. 2019 | Zapnuto ve výchozím nastavení | Zásobování a zdroje |
| cXML vylepšení nákupu | 1. 9. 2021 | 11. 11. 2019 | Zapnuto ve výchozím nastavení | Zásobování a zdroje |
| Zobrazte odkaz „Otevřít publikované žádosti o nabídku“ jako dlaždici | 1. 9. 2021 | 30. 9. 2020 | Zapnuto ve výchozím nastavení | Zásobování a zdroje |
| Otázky a odpovědi v RFQ | 1. 9. 2021 | 19. 2. 2020 | Zapnuto ve výchozím nastavení | Zásobování a zdroje |
| Informace o produktu nebezpečných materiálů a přepravní dokumentace | 1. 9. 2021 | 14. 6. 2020 | Zapnuto ve výchozím nastavení | Správa informací o produktech |
| Striktní ověření výchozího množství objednávky | 1. 9. 2021 | 24. 6. 2020 | Zapnuto ve výchozím nastavení | Správa informací o produktech |
| Funkce správy země původu | 1. 9. 2021 | 13. 7. 2020 | Zapnuto ve výchozím nastavení | Správa informací o produktech |
| Uložená zobrazení pro uvolněné produkty | 1. 9. 2021 | 30. 9. 2020 | Zapnuto ve výchozím nastavení | Správa informací o produktech |
| Vylepšení dialogových oken Úlohy schválení a Úlohy převodu | 1. 9. 2021 | 11. 10. 2019 | Zapnuto ve výchozím nastavení | Řízení výroby |
| Registrační značka pro vykazování jako dokončené přidána do zařízení úkolového lístku | 1. 9. 2021 | 31. 8. 2019 | Zapnuto ve výchozím nastavení | Řízení výroby |
| Na stránku terminálu úkolových lístků bylo přidáno nové tlačítko Ukončit přestávku | 1. 9. 2021 | 19. 2. 2020 | Zapnuto ve výchozím nastavení | Řízení výroby |
| Povolte částečný příjem subdodavatelských položek a opravte problém s výpočtem odpadu pro řádky kusovníku typu dodavatele. | 1. 9. 2021 | 11. 11. 2019 | Zapnuto ve výchozím nastavení | Řízení výroby |
| Uložená zobrazení pro řízení výroby | 1. 9. 2021 | 17. 8. 2020 | Zapnuto ve výchozím nastavení | Řízení výroby |
| Dynamics 365 Guides pro výrobu | 1. 9. 2021 | 13. 7. 2020 | Zapnuto ve výchozím nastavení | Řízení výroby |
| Provádění výrobního provozu | 1. 9. 2021 | 30. 9. 2020 | Zapnuto ve výchozím nastavení | Řízení výroby |
| Funkce pro uzamčení zařízení úkolového lístku a terminálu úkolových lístků za účelem dezinfekce | 1. 9. 2021 | 10. 5. 2020 | Zapnuto ve výchozím nastavení | Řízení výroby |
| Přidělení poplatků na prodejní objednávce | 1. 9. 2021 | 30. 9. 2020 | Zapnuto ve výchozím nastavení | Prodej a marketing |
| Omezit počet prodejních objednávek, které lze vybrat k zaúčtování | 1. 9. 2021 | 1. 9. 2021 | Zapnuto ve výchozím nastavení | Prodej a marketing |
| Vyčistit historii aktualizace prodejní objednávky | 1. 9. 2021 | 1. 9. 2021 | Zapnuto ve výchozím nastavení | Prodej a marketing |
| Změnit číselnou řadu pro práci cyklické inventury | 1. 9. 2021 | 7. 10. 2019 | Zapnuto ve výchozím nastavení | Řízení skladu |
| Doplnění vlny poptávky na základě úkolu | 1. 9. 2021 | 7. 10. 2019 | Povinné | Řízení skladu |
| Skrýt pole Celková hodnota na stránkách „Všechny náklady“ a „Podrobnosti o nákladu“ | 1. 9. 2021 | 7. 10. 2019 | Zapnuto ve výchozím nastavení | Řízení skladu |
| Tisk štítků vlny | 1. 9. 2021 | 19. 2. 2020 | Povinné | Řízení skladu |
| Přiřadit transakce zásob nákupní objednávky k vytížení | 1. 9. 2021 | 6. 1. 2020 | Povinné | Řízení skladu |
| Vylepšené rozvržení popisků registračních značek | 1. 9. 2021 | 19. 2. 2020 | Zapnuto ve výchozím nastavení | Řízení skladu |
| Blokování práce pro celou organizaci | 1. 9. 2021 | 19. 2. 2020 | Povinné | Řízení skladu |
| Podrobnosti řádku práce | 1. 9. 2021 | 11. 10. 2019 | Zapnuto ve výchozím nastavení | Řízení skladu |
| Udělat pole stavu zásob pohybu zásob mobilního zařízení upravitelným | 1. 9. 2021 | 16. 10. 2019 | Zapnuto ve výchozím nastavení | Řízení skladu |
| Potvrdit odchozí dodávky z dávkových úloh | 1. 9. 2021 | 13. 7. 2020 | Zapnuto ve výchozím nastavení | Řízení skladu |
| Určit zda se má na mobilních zařízeních zobrazit stránka se souhrnem příjmu | 1. 9. 2021 | 1. 4. 2020 | Zapnuto ve výchozím nastavení | Řízení skladu |
| Vyzvat k vyřešení nejednoznačných názvů &#39;Loc / LP&#39; | 1. 9. 2021 | 1. 4. 2020 | Zapnuto ve výchozím nastavení | Řízení skladu |
| Zaznamenat varianty produktu a sledovací dimenze ve skladové aplikaci při příjmu položky vytížení | 1. 9. 2021 | 10. 5. 2020 | Zapnuto ve výchozím nastavení | Řízení skladu |
| Nepovolujte vytváření nákladů, které nesplňují požadavky šablony sestavení vytížení vlny. | 1. 9. 2021 | 17. 8. 2020 | Zapnuto ve výchozím nastavení | Řízení skladu |
| Vyhodnocení všech akcí pro směrnice umístění více SKU | 1. 9. 2021 | 30. 9. 2020 | Zapnuto ve výchozím nastavení | Řízení skladu |

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

### <a name="platform-updates-for-finance-and-operations-apps"></a>Aktualizace platformy pro finanční a provozní aplikace

Microsoft Dynamics 365 Supply Chain Management 10.0.21 zahrnuje aktualizace platformy. Další informace naleznete v tématu [Aktualizace platformy pro verze 10.0.21 finančních a provozních aplikací (říjen 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21.md).

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
