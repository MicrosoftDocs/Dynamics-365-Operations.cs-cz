---
title: Obsah správy nákladů v Power BI
description: Toto téma popisuje, co je součástí obsahu správy nákladů v Power BI.
author: ShylaThompson
manager: AnnBe
ms.date: 03/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6bd76fc771c370d8d769a97d3b33003f632717f2
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174183"
---
# <a name="cost-management-power-bi-content"></a>Obsah správy nákladů v Power BI

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Přehled

Obsah **Řízení nákladů** v Microsoft Power BI je určen pro skladové účetní nebo osoby v rámci organizace, které zodpovídají za nebo se zabývají stavem zásob nebo nedokončenou výrobu (NV) nebo které jsou zodpovědné za nebo se zabývají analýzou odchylek standardních nákladů.

> [!NOTE]
> Obsah **Řízení nákladů** v Power BI popsaný v tomto tématu se vztahuje na Dynamics 365 Finance and Operations 8.0.
> 
> Sada obsahu **Řízení nákladů**v Power BI, dostupná na webu AppSource se již nepoužívá. Další informace o tomto odepsání uvádí [Sady obsahu Power BI dostupné na AppSource](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource).

Tento obsah Power BI obsahuje kategorizovaný formát, který pomáhá sledovat výkon zásob a vizualizovat, jak jimi protékají náklady. Můžete získat manažerské informace, jako je například ukazatel obratu, počet dní, po který jsou zásoby na skladě, přesnost a "ABC-klasifikace" na preferované agregované úrovni (společnost, položka, skupina položek nebo webové stránky). Zpřístupněné informace lze použít také jako podrobný doplněk k finančnímu výkazu.

Obsah Power BI je vystavěn na souhrnném měření **CostObjectStatementCacheMonthly**, které má jako primární datový zdroj tabulku **CostObjectStatementCache**. Tato tabulka je spravována rozhraním mezipaměti sady dat. Ve výchozím nastavení je tabulka aktualizována každých 24 hodin, ale můžete změnit četnost aktualizací nebo povolit ruční aktualizace v konfiguraci mezipaměti datové sady. Ruční aktualizace lze spustit v pracovním prostoru **Správa nákladů** nebo **Analýza nákladů**.

Po každé aktualizaci tabulky **CostObjectStatementCache** je nutné aktualizovat souhrnné měření **CostObjectStatementCacheMonthly**, než bude možné aktualizovat data ve vizualizacích Power BI.

## <a name="accessing-the-power-bi-content"></a>Přístup k obsahu Power BI

Obsah **Řízení nákladů** v Power BI se zobrazí v pracovním prostoru **Správa nákladů** a **Analýza nákladů**.

Pracovní prostor **Správa nákladů** obsahuje následující karty:

- **Přehled** – na této kartě se zobrazují data aplikace.
- **Stav účetnictví zásob** – na této kartě se zobrazuje obsah Power BI.
- **Stav účetnictví pro výrobu** – na této kartě se zobrazuje obsah Power BI.

Pracovní prostor **Analýza nákladů** obsahuje následující karty:

- **Přehled** – na této kartě se zobrazují data aplikace.
- **Analýza účetnictví zásob** – na této kartě se zobrazuje obsah Power BI.
- **Analýza účetnictví pro výrobu** – na této kartě se zobrazuje obsah Power BI.
- **Analýza odchylky st. nákladů** – na této kartě se zobrazuje obsah Power BI.

## <a name="report-pages-that-are-included-in-the-power-bi-content"></a>Stránky sestav, které jsou součástí obsahu Power BI

Obsah **Správa nákladů** v Power BI obsahuje sadu stránek sestavy, které sestávají ze sady metrik. Tyto metriky jsou zobrazována jako grafy, dlaždice a tabulky. 

Následující tabulky poskytují přehled vizualizace v obsahu **správy nákladů** v Power BI.

### <a name="inventory-accounting-status"></a>Stav skladového účetnictví

| Stránka sestavy                               | Vizualizace                                   |
|-------------------------------------------|-------------------------------------------------|
| Přehled zásob                        | Počáteční zůstatek                               |
|                                           | Změna netto                                      |
|                                           | Čistá změna v %                                    |
|                                           | Konečný zůstatek                                  |
|                                           | Přesnost zásob                              |
|                                           | Ukazatel obratu zásob                        |
|                                           | Dny zásob na skladě                          |
|                                           | Aktivní produkt za období                        |
|                                           | Aktivní objekty nákladů v období                   |
|                                           | Zůstatek podle skupiny položek                           |
|                                           | Zůstatek podle pracoviště                                 |
|                                           | Výpis podle kategorie                           |
|                                           | Čistá změna podle čtvrtletí                           |
| Přehled zásob podle skupiny pracoviště a položky | Přesnost zásob podle pracoviště                      |
|                                           | Ukazatel obratu zásob podle pracoviště                |
|                                           | Konečný zůstatek zásob podle pracoviště                |
|                                           | Přesnost zásob podle skupin zboží                |
|                                           | Ukazatel obratu zásob podle skupiny položek          |
|                                           | Konečný zůstatek zásob podle pracoviště a skupiny položek |
| Výkaz inventury                       | Výkaz inventury                             |
| Výpis zásob podle pracoviště               | Výpis zásob podle pracoviště                     |
| Výkaz zásob podle hierarchie produktů  | Výkaz inventury                             |
| Výkaz zásob podle hierarchie produktů  | Výpis zásob podle pracoviště                     |

### <a name="manufacturing-accounting-status"></a>Stav účetnictví pro výrobu

| Stránka sestavy                | Vizualizace                       |
|----------------------------|-------------------------------------|
| Přehled NV do konce roku           | Počáteční zůstatek                   |
|                            | Změna netto                          |
|                            | Čistá změna v %                        |
|                            | Konečný zůstatek                      |
|                            | Ukazatel obratu NP                  |
|                            | Denní pokladní hotovost NV                    |
|                            | Aktivní objekt nákladů v období        |
|                            | Čistá změna podle skupiny prostředků        |
|                            | Zůstatek podle pracoviště                     |
|                            | Výpis podle kategorie               |
|                            | Čistá změna podle čtvrtletí               |
| výkaz nedokončené výroby              | Počáteční zůstatek                   |
|                            | Konečný zůstatek                      |
|                            | Výpis NV podle kategorie           |
| Výpis zásob NV podle pracoviště      | Počáteční zůstatek                   |
|                            | Konečný zůstatek                      |
|                            | Výpis NV podle kategorie a pracoviště  |
| Výpis NV podle hierarchie | Počáteční zůstatek                   |
|                            | Konečný zůstatek                      |
|                            | Výpis NV podle kategorie a hierarchie |

### <a name="inventory-accounting-analysis"></a>Analýza skladového účetnictví

| Stránka sestavy        | Vizualizace                                                                |
|--------------------|------------------------------------------------------------------------------|
| Podrobnosti skladu  | Prvních 10 prostředků podle konečného zůstatku                                           |
|                    | Hlavních 10 zdrojů podle čistého navýšení změny                                      |
|                    | Hlavních 10 zdrojů podle čistého snížení změny                                      |
|                    | Hlavních 10 zdrojů podle ukazatele obratu zásob                                 |
|                    | Zdroje podle nízkého ukazatele obratu a konečného zůstatku nad prahovou hodnotou |
|                    | Hlavních 10 zdrojů podle nízké přesnosti                                             |
| Klasifikace ABC | Konečný zůstatek zásob                                                     |
|                    | Spotřebovaný materiál                                                            |
|                    | Prodáno (COGS)                                                                  |
| Trendy zásob   | Konečný zůstatek zásob                                                     |
|                    | Čistá změna zásob                                                         |
|                    | Ukazatel obratu zásob                                                     |
|                    | Přesnost zásob                                                           |

### <a name="manufacturing-accounting-analysis"></a>Analýza účetnictví pro výrobu

| Stránka sestavy | Vizualizace      |
|-------------|--------------------|
| Trendy NV  | Konečný zůstatek NV |
|             | Čistá změna NV     |
|             | Ukazatel obratu NP |

### <a name="std-cost-variance-analysis"></a>Analýza standardní odchylky nákladů

| Stránka sestavy                             | Vizualizace                                        |
|-----------------------------------------|------------------------------------------------------|
| Odchylka nákupní ceny (standardní náklady) od začátku roku | Zůstatek z nákupu                                     |
|                                         | Odchylka nákupní ceny                              |
|                                         | Poměr odchylky nákupní ceny                        |
|                                         | Odchylka podle skupiny položek                               |
|                                         | Odchylka podle pracoviště                                     |
|                                         | Nákupní cena podle čtvrtletí                            |
|                                         | Nákupní cena podle čtvrtletí a skupiny položek             |
|                                         | Hlavních 10 zdrojů podle poměru nepříznivé nákupní ceny |
|                                         | Hlavních 10 zdrojů podle poměru příznivé nákupní ceny   |
| Výrobní odchylka (st. náklady) od začátku roku     | Výrobní náklady                                    |
|                                         | Výrobní odchylka                                  |
|                                         | Poměr výrobní odchylky                            |
|                                         | Odchylka podle skupiny položek                               |
|                                         | Odchylka podle pracoviště                                     |
|                                         | Výrobní odchylka množství podle čtvrtletí                       |
|                                         | Výrobní odchylka podle čtvrtletí a typu odchylky     |
|                                         | 10 hlavních zdrojů s nepříznivou výrobní odchylkou  |
|                                         | 10 hlavních zdrojů s příznivou výrobní odchylkou    |

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách

Data z aplikace se používají k naplnění stránek sestav v obsahu **Správa nákladů** v Power BI. Tato data jsou reprezentována jako měrné systémy agregace, které jsou rozfázovány v úložišti entit, což je databáze Microsoft SQL Server optimalizována pro analýzy. Další informace naleznete v tématu [Integrace Power BI s úložištěm entit](power-bi-integration-entity-store.md).

Klíčová agregovaná opatření následujících objektů se používají jako základ obsahu Power BI.

| Objekt                          | Klíčová opatření agregace | Datový zdroj pro Finance and Operations | Pole               |
|---------------------------------|----------------------------|----------------------------------------|---------------------|
| CostObjectStatementCacheMonthly | Množství                     | CostObjectStatementCache               | Množství              |
| CostObjectStatementCacheMonthly | Množství                   | CostObjectStatementCache               | Množství                 |
| CostInventoryAccountingKPIGoal  | AnnualInventoryTurn        | CostInventoryAccountingKPIGoal         | AnnualInventoryTurn |
| CostInventoryAccountingKPIGoal  | InventoryAccuracy          | CostInventoryAccountingKPIGoal         | InventoryAccuracy   |

Následující tabulka zobrazuje klíčová vypočítaná měření v obsahu Power BI.

| Vyhodnocení                            | Výpočet |
|------------------------------------|-------------|
| Počáteční zůstatek                  | Počáteční zůstatek = \[Koncový zůstatek\]-\[Čistá změna\] |
| Množství počátečního zůstatku             | Množství Počáteční zůstatek = \[Množství Koncový zůstatek\]-\[Množství Čistá změna\] |
| Konečný zůstatek                     | Konečný zůstatek = (CALCULATE(SUM(\[Amount\]), FILTER(ALL(FiscalCalendar) ,FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\])))) |
| Množství Konečný zůstatek                | Množství koncového zůstatku = CALCULATE(SUM(\[QTY\]), FILTER(ALL(FiscalCalendar),FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\]))) |
| Změna netto                         | Čistá změna = SUM(\[AMOUNT\]) |
| Změna čistého množství                    | Množství čisté změny = SUM(\[QTY\]) |
| Ukazatel obratu zásob podle částky | Ukazatel obratu zásob podle částky = if(OR(\[Průměrný zůstatek zásob\] \<= 0, \[Prodané zásoby nebo spotřebované zboží\] \>= 0), 0, ABS(\[Prodané zásoby nebo spotřebované zboží\])/\[Průměrný zůstatek zásob\]) |
| Průměrný zůstatek zásob          | Průměrný zůstatek zásob = ((\[konečný zůstatek\] + \[počáteční zůstatek\]) / 2) |
| Dny zásob na skladě             | Denní zásoby množství na skladě = 365 / CostObjectStatementEntries\[Ukazatel obratu zásob podle částky\] |
| Přesnost zásob                 | Přesnost zásob podle částky = IF(\[Konečný zůstatek\] \<= 0, IF(OR(\[Spočítaná částka zásob\] \<\> 0, \[Konečný zůstatek\] \< 0), 0, 1), MAX(0, (\[Konečný zůstatek\] - ABS(\[Spočítaná částka zásob\]))/\[Konečný zůstatek\])) |

Následující tabulka uvádí klíčové dimenze, které se používají jako filtry k rozdělení agregovaných měření, aby bylo možné dosáhnout většího odstupňování a získat hlubší analytický přehled.


| Celek                                                  | Příklady atributů                          |
|---------------------------------------------------------|-------------------------------------------------|
| Produkty                                                | Číslo produktu, název produktu, jednotka, skupiny zboží |
| Hierarchie kategorií (přiřazeno role Řízení nákladů) | Hierarchie kategorií, úroveň kategorie              |
| Právnické osoby                                          | Jména právnické osoby                              |
| Fiskální kalendáře                                        | Fiskální kalendář, rok, čtvrtletí, období, měsíc   |
| Pracoviště                                                    | ID, název, adresa, stát, země               |