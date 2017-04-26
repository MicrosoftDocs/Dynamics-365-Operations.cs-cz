---
title: "Náklady na správu obsahu Power BI"
description: "Toto téma popisuje, co je součástí nákladů řízení obsahu Power BI. Popisuje, jak přístup k sestavám Power BI a obsahuje informace o datovém modelu a entit, které jsou použity k sestavení obsahu."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: e4de011e6eeac58643b828b65e24b874d981d5e7
ms.lasthandoff: 03/31/2017


---

# <a name="cost-management-power-bi-content"></a>Náklady na správu obsahu Power BI

[!include[banner](../includes/banner.md)]


Toto téma popisuje, co je součástí nákladů řízení obsahu Power BI. Popisuje, jak přístup k sestavám Power BI a obsahuje informace o datovém modelu a entit, které jsou použity k sestavení obsahu.

# <a name="overview"></a>Přehled

**Nákladů řízení** obsah Microsoft Power BI je určena pro účetní zásob nebo osobám v organizaci odpovědné za zásoby. **Nákladů řízení** obsahu Power BI poskytuje vedoucím skladu a zásob rozpracované výroby (NV) a jak náklady prochází je podle kategorie v průběhu času. Informace lze použít také jako doplněk podrobné finanční výkaz.

## <a name="key-measures"></a>Klíčové opatření

+ Počáteční zůstatek
+ Konečný zůstatek
+ Čistá změna
+ Pohyb v %
+ Sledování splatnosti

## <a name="key-performance-indicators"></a>Klíčové ukazatele výkonnosti
+ Obrat zásob
+ Přesnost zásob

CostStatementCache tabulka je primární datový zdroj pro CostAggregatedCostStatementEntryEntity. Tato tabulka je spravován mezipaměti rámcem datové sady. Ve výchozím nastavení tabulka je aktualizován každých 24 hodin, ale můžete povolit ruční aktualizace konfigurace mezipaměti data. Pak můžete provést ruční aktualizaci **nákladů řízení** nebo **analýza nákladů** prostoru. Po spuštění aktualizace CostStatementCache je nutné aktualizovat OData připojení na napájení BI.com Chcete-li zobrazit aktualizovaná data na webu. Odchylka (nákup, výroba) opatření v tomto obsahu Power BI se vztahují pouze na položky, které jsou valuated pevnou pořizovací cenu zásob metodou. Výrobní odchylka se vypočítá jako rozdíl mezi aktivní a realizované náklady. Výrobní odchylka se vypočítá, když výrobní zakázka má stav **ukončeno**. Další informace o typy výroby odchylky a způsob výpočtu jednotlivých typů naleznete v tématu [analýza odchylek pro dokončenou výrobní zakázku](https://technet.microsoft.com/en-us/library/gg242850.aspx).

## <a name="accessing-the-power-bi-content"></a>Přístup k obsahu Power BI
**Nákladů řízení** obsahu Power BI je k dispozici na PowerBI.com. Další informace o tom, jak připojit a načíst vaše 365 Microsoft Dynamics pro datové operace, viz [obsahu Power BI přístup z PowerBI.com](power-bi-home-page.md).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metriky, které jsou součástí obsahu Power BI
Obsah zahrnuje sadu stránky sestavy. Každá stránka obsahuje sadu metriky, které jsou zobrazována jako grafy, kameny a tabulky. Následující tabulka obsahuje přehled vizualizace v **nákladů řízení** obsahu Power BI.

| Stránky sestavy | Grafy | Pozice |
|---|---|---|
|Celkové zásoby (výchozí nastavení v aktuálním období) |Přesnost |Opatření zásob:<br>Konečný zůstatek zásob<br>Pohyb zásob<br>% Pohyb zásob<br>|
| |Obrat zásob | |
| |Konečné saldo podle skupiny zdrojů zásob | |
| |Pohyb zásob úroveň název kategorie 1 a kategorie název úrovně 2| |
| |Nákupní odchylky podle skupiny zdrojů a úroveň název kategorie 3 | |
|Zásoby dle serveru (výchozí nastavení v aktuálním období) |Konečné saldo podle názvu webu a skupiny zdrojů zásob | |
| |Obratu zásob podle názvu webu a skupiny zdrojů | |
| |Konečné saldo podle města a zdrojů skupiny zásob | |
|Zásoby dle skupiny zdrojů (výchozí nastavení v aktuálním období) |Opatření zásob | |
| |Přesnost zásob podle částky podle skupiny zdrojů | |
| |Obratu zásob podle částky podle skupiny zdrojů | |
|Zásoby po letech (výchozí aktuální rok vs předchozího roku) |Opatření zásob | |
| |Klíčové ukazatele výkonu zásob:<br>Obrat zásob<br>Přesnost zásob | |
| |Konečné saldo podle roku a zdrojů skupiny zásob | |
| |Nákupní odchylky podle roku a kategorie název úrovně 3 | |
|Prodlení zásob (výchozí aktuální rok) |Prodlení zásob podle čtvrtletí a zdrojů skupiny | |
| |Prodlení zásob podle názvu webu a čtvrtletí | |
|NV-celková (výchozí nastavení v aktuálním období) |Net NV změnit úroveň název kategorie 1 a kategorie název úrovně 2 |Nedokončená výroba NV opatření:<br>Konečný zůstatek NV<br>Čistá změna NV<br>Pohyb % NV<br> |
| |Výrobní odchylky podle skupiny zdrojů a kategorie název úroveň 3 | |
| |Čistá změna NV podle skupiny zdrojů | |
|Nedokončené výroby podle pracoviště (výchozí nastavení v aktuálním období) |Nedokončená výroba NV opatření | |
| |Net NV změnit název webu a název úroveň kategorie 2 | |
| |Výrobní odchylky podle názvu serveru a úroveň název kategorie 3 | |

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách
Dynamics 365 pro datové operace se používá k naplnění stránky sestavy **nákladů řízení** obsahu Power BI. Tato data jsou reprezentována jako agregační hodnoty, které jsou připraveny v úložišti Entity, což je databáze Microsoft SQL, která je optimalizována pro analytics. Další informace naleznete v tématu [BI napájení Přehled integrace s úložištěm Entity](power-bi-integration-entity-store.md). Následující klíče souhrnné měření slouží jako základ pro obsah.

| Celek            | Agregované míry klíče | Zdroj dat pro Dynamics 365 pro operace | Pole             | popis                       |
|-------------------|---------------------------|---------------------------------------------|-------------------|-----------------------------------|
| Výpis položek | Čistá změna                | CostAggregatedCostStatementEntryEntity      | Součet (\[částka\])   | Částka v zúčtovací měně |
| Výpis položek | Čistá změna množství       | CostAggregatedCostStatementEntryEntity      | Součet (\[množství\]) |                                   |

Následující tabulka zobrazuje, jak agregační klíčové měření slouží k vytvoření několika vypočtené rozměry v obsahu dataset.

| Měřítko                                 | Jak vypočítat rozměr                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Počáteční zůstatek                       | \[Konečný zůstatek\]-\[pohyb\]                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Počáteční zůstatek množství              | \[Koncové množství zůstatek\]-\[množství pohybu.\]                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Konečný zůstatek                          | VYPOČÍTAT (součet (\[částka\]), filtr (ALLEXCEPT ('Fiskální kalendáře', 'Fiskální kalendáře'\[LedgerRecId\], "subjekty"\[ID\], "entity"\[název\], "Knih"\[měny\], "Knih"\[popis\], "Knih"\[název\]), 'Fiskální kalendáře'\[datum\]&lt;= MAX ('Fiskální kalendáře'\[datum\])))                                                                                                                                                                                           |
| Koncové množství zůstatek                 | VYPOČÍTAT (součet (\[množství\]), filtr (ALLEXCEPT ('Fiskální kalendáře', 'Fiskální kalendáře'\[LedgerRecId\], "entity"\[ID\], "subjekty"\[název\], "Knih"\[měny\], "Knih"\[popis\], "Knih"\[název\]), 'Fiskální kalendáře'\[datum\]&lt;= MAX ('Fiskální kalendáře'\[datum\])))                                                                                                                                                                                         |
| Počáteční zůstatek zásob             | Výpočet (\[počáteční zůstatek\], 'Výpis položek'\[typ příkazu\] = "Zásoby")                                                                                                                                                                                                                                                                                                                                                                                      |
| Konečný zůstatek zásob                | Výpočet (\[konečný zůstatek\], 'Výpis položek'\[typ příkazu\] = "Zásob")                                                                                                                                                                                                                                                                                                                                                                                         |
| Pohyb zásob                    | Výpočet (\[pohyb\], 'Výpis položek'\[typ příkazu\] = "Zásoby")                                                                                                                                                                                                                                                                                                                                                                                             |
| Čistá změna množství zásob           | Výpočet (\[pohyb, množství\], 'Výpis položek'\[typ příkazu\] = "Zásob")                                                                                                                                                                                                                                                                                                                                                                                    |
| % Pohyb zásob                  | IF (\[konečný zůstatek zásob\] = 0, 0, \[pohyb zásob\] / \[konečný zůstatek zásob\])                                                                                                                                                                                                                                                                                                                                                                           |
| Částka obratu zásob                | Pokud (OR (\[Průměrný zůstatek zásob\]&lt;= 0, \[zásob prodané nebo spotřebované problémy\]&gt;= 0), 0, ABS (\[zásob prodané nebo spotřebované problémy\]) /\[Průměrný zůstatek zásob\])                                                                                                                                                                                                                                                                                                  |
| Průměrný zůstatek zásob               | (\[Konečný zůstatek zásob\] + \[počáteční zůstatek zásob\]) / 2                                                                                                                                                                                                                                                                                                                                                                                                       |
| Zásoby prodané nebo spotřebované problémy       | \[Prodaný inventář\] + \[zásoby spotřebované náklady na materiál\]                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Zásoby spotřebované náklady na materiál        | Výpočet (\[pohyb zásob\], 'Výpis položek'\[název kategorie - úroveň 2\_\] = "ConsumedMaterialsCost")                                                                                                                                                                                                                                                                                                                                                            |
| Prodaný inventář                          | Výpočet (\[pohyb zásob\], 'Výpis položek'\[název kategorie - úroveň 2\_\] = "Prodáno")                                                                                                                                                                                                                                                                                                                                                                             |
| Přesnost zásob podle částky            | IF (\[konečný zůstatek zásob\]&lt;= 0, pokud (nebo (\[zásob Spočtená částka\]&lt;&gt; 0, \[konečný zůstatek zásob\]&lt; 0), 0, 1), MAX (0, (\[konečný zůstatek zásob\] -ABS (\[zásob Spočtená částka\])) /\[konečný zůstatek zásob\]))                                                                                                                                                                                                                              |
| Spočtená částka zásob                | Výpočet (\[pohyb zásob\], 'Výpis položek'\[název kategorie - úroveň 3\_\] = "Inventury")                                                                                                                                                                                                                                                                                                                                                                         |
| Prodlení zásob                         | Pokud (zjistit (max ('Fiskální kalendáře'\[datum\])), blank(), MAX (0, MIN (\[množství příjmů zásob stárnutí\], \[zásob stárnutí konečné bilance množství\] - \[stárnutí skladové příjmy v budoucnu množství\]))) \*\[zásob průměrné náklady na jednotku\]                                                                                                                                                                                                                                |
| Skladové množství příjemky stárnutí       | IF (\[minDate\] = \[minDateAllSelected\], VYPOČÍTAT (\[pohyb množství zásob\], "Výpis položek"\[množství\]&gt; 0, filtr (ALLEXCEPT ('Fiskální kalendáře', "Fiskální kalendáře"\[LedgerRecId\], "subjekty"\[ID\], "subjekty"\[název\], "Knih"\[měny\], "Knih"\[popis\], "Knih"\[název\]), "Fiskální kalendáře"\[datum\]&lt;= MAX ("Fiskální kalendáře"\[datum\]))), VYPOČÍTAT (\[pohyb množství zásob\], "Výpis položek"\[množství\]&gt; 0)) |
| Koncové množství zůstatek stárnutí zásob | \[Koncové množství zůstatku zásob\] + výpočet (\[pohyb množství zásob\], filtr (ALLEXCEPT ('Fiskální kalendáře', 'Fiskální kalendáře'\[LedgerRecId\], "subjekty"\[ID\], "subjekty"\[název\], "Knih"\[měny\], "Knih"\[popis\], "Knih"\[název\]), 'Fiskální kalendáře'\[datum\]&gt; max ('Fiskální kalendáře'\[datum\])))                                                                                                                                 |
| Příjmy na sklad stárnutí v budoucnosti  | VYPOČÍTAT (\[pohyb zásob\], "Výpis položek"\[částka\]&gt; 0, filtr (ALLEXCEPT ('Fiskální kalendáře', 'Fiskální kalendáře'\[LedgerRecId\], "subjekty"\[ID\], "subjekty"\[název\], "Knih"\[měny\], "Knih"\[popis\], "Knih"\[název\]), 'Fiskální kalendáře'\[datum\]&gt; MAX ("Fiskální kalendáře"\[datum\])))                                                                                                                                             |
| Průměrné náklady na jednotku zásob                 | Výpočet (\[konečný zůstatek zásob\] / \[konečné bilance množství zásob\], ALLEXCEPT ('Fiskální kalendáře', 'Fiskální kalendáře'\[LedgerRecId\], "subjekty"\[ID\], "subjekty"\[název\], 'Knihy'\[měny\], "Knih"\[popis\], "Knih"\[název\]))                                                                                                                                                                                                                 |
| Nákupní odchylky                      | Výpočet (součet (\[částka\]), "Výpis položek"\[název kategorie - úroveň 2\_\] = "Procured", "Příkaz položky"\[typ příkazu\] = "Rozptyl")                                                                                                                                                                                                                                                                                                                              |
| Počáteční zůstatek NV                   | Výpočet (\[počáteční zůstatek\], 'Výpis položek'\[typ příkazu\] = "NV")                                                                                                                                                                                                                                                                                                                                                                                            |
| Konečný zůstatek NV                      | Výpočet (\[konečný zůstatek\], 'Výpis položek'\[typ příkazu\] = "NV")                                                                                                                                                                                                                                                                                                                                                                                               |
| Čistá změna NV                          | Výpočet (\[pohyb\], 'Výpis položek'\[typ příkazu\] = "NV")                                                                                                                                                                                                                                                                                                                                                                                                   |
| Pohyb % NV                        | IF (\[NV, koncový zůstatek\] = 0, 0, \[pohyb NV\] / \[NV, koncový zůstatek\])                                                                                                                                                                                                                                                                                                                                                                                             |
| Výrobní odchylky                    | Výpočet (součet (\[částka\]), "Výpis položek"\[název kategorie - úroveň 2\_\] = "ManufacturedCost", "Příkaz položky"\[typ příkazu\] = "Rozptyl")                                                                                                                                                                                                                                                                                                                      |
| Název kategorie - úroveň 1                 | Přepnout (\[název kategorie - úroveň 1\_\], "None", "None", "NetSourcing", "Čistý původ", "NetUsage", "Čisté využití", "NetConversionCost", "Čistý převod nákladů", "NetCostOfGoodsManufactured", "Čisté náklady vyrobeného zboží", "BeginningBalance", "Počáteční zůstatek")                                                                                                                                                                                                         |
| Název kategorie - úroveň 2                 | Přepnout (\[název kategorie - úroveň 2\_\], "None", "None", "Procured", "Procured", "Disposed", "Disposed", "Transfer", "Transfer", "Prodáno", "Prodáno", "ConsumedMaterialsCost", "Spotřebované náklady na materiál", "ConsumedManufacturingCost", "Spotřebovaných nákladů výroby", "ConsumedOutsourcingCost", "Spotřebované náklady outsourcing", "ConsumedIndirectCost", "Spotřebováno nepřímé náklady", "ManufacturedCost", "Náklady výrobce", "Odchylky", "Odchylky")                            |
| Název kategorie - úroveň 3                 | Přepnout (\[název kategorie - úroveň 3\_\], "None", "None", "Počítání", "None", "ProductionPriceVariance", "Výrobní ceny", "QuantityVariance", "Množství", "SubstitutionVariance", "Náhradní", "ScrapVariance", "Odpad", "LotSizeVariance", "Velikost dávky", "RevaluationVariance", "Přecenění", "PurchasePriceVariance", "Nákupní cena", "CostChangeVariance", "Změnu ceny", "RoundingVariance", "Odchylka zaokrouhlení")                                                   |

Následující klíče dimenze slouží jako filtry k řezu agregovaných měr dosáhnout větší rozlišovací schopnost a poskytují hlubší analytické poznatky.

| Celek           | Příklady atributů                       |
|------------------|----------------------------------------------|
| Entity         | ID názvu                                     |
| Fiskální kalendáře | Kalendáře, období, čtvrtletí, měsíc rok       |
| Cíle ukazatele KPI        | Obratu zásob skladu přesnost cíl, cíl |
| Hlavní knihy          | Měna, název, popis                  |
| Pracoviště            | ID, jméno, země, Město                      |

## <a name="additional-resources"></a>Další prostředky
Zde uvádíme některé užitečné odkazy související s entitami a vytvářením obsahu v aplikaci Power BI:

-   [Datové entity](..\data-entities\data-entities.md)
-   [Vytvoření organizačního balíčku obsahu](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Modelování dat pomocí aplikace Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Přidání dlaždic Power BI do pracovních prostorů](configure-power-bi-integration.md)





