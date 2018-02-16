---
title: "Obsah správy nákladů v Power BI"
description: "Toto téma popisuje, co je součástí obsahu správy nákladů v Power BI."
author: YuyuScheller
manager: AnnBe
ms.date: 02/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: b167d7577823bbc88d8e64952333110f9a652b64
ms.openlocfilehash: 1f552e1ee0286326e3a2a8bb6a7bfb84df53b45d
ms.contentlocale: cs-cz
ms.lasthandoff: 02/02/2018

---

# <a name="cost-management-power-bi-content"></a>Obsah správy nákladů v Power BI

[!include[banner](../includes/banner.md)]

> [Poznámka] Tento balíček obsahu je zastaralý, jak je uvedeno v části [Balíčky obsahu Power BI publikované na PowerBI.com](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features#power-bi-content-packs-published-to-powerbicom).


Toto téma popisuje, co je součástí obsahu správy nákladů v Power BI. 

Obsah **Správy nákladů** sady nástrojů Microsoft Power BI je určen pro skladové účetní zásob nebo pro osoby v organizaci, které jsou odpovědné za zásoby. Obsah **Správy nákladů** v Power BI poskytuje manažerský přehled o zásobách a rozpracované výrobě (NV), a způsobu, jakým jimi náklady procházejí podle kategorie v průběhu času. Informace lze použít také jako podrobný doplněk k finančnímu výkazu.

## <a name="key-measures"></a>Klíčová měřítka

+ Počáteční zůstatek
+ Konečný zůstatek
+ Čistá změna
+ Čistá změna v %
+ Sledování splatnosti

## <a name="key-performance-indicators"></a>Klíčové ukazatele výkonnosti
+ Obrat zásob
+ Přesnost zásob

Primárním datovým zdrojem pro CostAggregatedCostStatementEntryEntity je tabulka CostStatementCache. Tato tabulka je spravována rozhraním mezipaměti sady dat. Ve výchozím nastavení je tabulka aktualizována každých 24 hodin, ale můžete povolit ruční aktualizace v konfiguraci mezipaměti dat. Pak můžete provést ruční aktualizaci v pracovním prostoru **Správa nákladů** nebo **Analýza nákladů**. Po spuštění aktualizace CostStatementCache je nutné aktualizovat OData připojení na Power BI.com, pokud chcete zobrazit aktualizovaná data na webu. Měření odchylky (nákup, výroba) v tomto obsahu Power BI se vztahují pouze na položky, které jsou ohodnoceny skladovou metodou standardních nákladů. Výrobní odchylka se vypočítá jako rozdíl mezi aktivními a realizovanými náklady. Výrobní odchylka se vypočítá, když má výrobní zakázka stav **Ukončeno**. Další informace o typech výrobní odchylky a způsobu výpočtu jednotlivých typů naleznete v tématu [Analýza odchylek pro dokončenou výrobní zakázku](https://technet.microsoft.com/en-us/library/gg242850.aspx).


## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metriky, které jsou součástí obsahu Power BI
Obsah zahrnuje sadu stránek sestav. Každá stránka obsahuje sadu metrik, které jsou zobrazovány jako grafy, dlaždice a tabulky. Následující tabulka poskytuje přehled vizualizace v obsahu **správy nákladů** v Power BI.

| Stránka sestavy | Grafy | Pozice |
|---|---|---|
|Celkové zásoby (výchozí nastavení podle aktuálního období) |Přesnost |Měření zásob:<br>Konečný zůstatek zásob<br>Čistá změna zásob<br>Čistá změna zásob %<br>|
| |Obrat zásob | |
| |Konečný zůstatek zásob podle skupiny prostředků | |
| |Čistá změna zásob podle úrovně názvu kategorie 1 a úrovně názvu kategorie 2| |
| |Nákupní odchylky podle skupiny prostředků a úrovně názvu kategorie 3 | |
|Zásoby podle pracoviště (výchozí nastavení podle aktuálního období) |Konečný zůstatek zásob podle názvu pracoviště a skupiny prostředků | |
| |Obrat zásob podle názvu pracoviště a skupiny prostředků | |
| |Konečný zůstatek zásob podle města a skupiny prostředků | |
|Zásoby podle skupiny prostředků (výchozí nastavení podle aktuálního období) |Měření zásob | |
| |Přesnost zásob podle částky podle skupiny prostředků | |
| |Obrat zásob podle částky podle skupiny prostředků | |
|Zásoby po letech (výchozí aktuální rok oproti předchozímu roku) |Měření zásob | |
| |Ukazatelé KPI zásob:<br>Obrat zásob<br>Přesnost zásob | |
| |Konečný zůstatek zásob podle roku a skupiny prostředků | |
| |Nákupní odchylky podle roku a úrovně názvu kategorie 3 | |
|Prodlení zásob (výchozí nastavení podle aktuálního roku) |Prodlení zásob podle čtvrtletí a skupiny prostředků | |
| |Prodlení zásob podle čtvrtletí a názvu pracoviště | |
|Celková NV (výchozí nastavení podle aktuálního období) |Čistá změna NV podle úrovně názvu kategorie 1 a úrovně názvu kategorie 2 |Měření nedokončené výroby:<br>Konečný zůstatek NV<br>Čistá změna NV<br>Čistá změna NV %<br> |
| |Výrobní odchylky podle skupiny prostředků a úrovně názvu kategorie 3 | |
| |Čistá změna NV podle skupiny prostředků | |
|NV podle pracoviště (výchozí nastavení podle aktuálního období) |Měření nedokončené výroby | |
| |Čistá změna NV podle názvu pracoviště a úrovně názvu kategorie 2 | |
| |Výrobní odchylky podle názvu pracoviště a úrovně názvu kategorie 3 | |

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách
Data aplikace Finance and Operations se používají k naplnění stránek sestavy v obsahu **Správa nákladů** v Power BI. Tato data jsou reprezentována jako měrné systémy agregace, které jsou rozfázovány v úložišti entit, což je databáze Microsoft SQL optimalizována pro analýzy. Další informace naleznete v tématu [Přehled integrace Power BI úložištěm entit](power-bi-integration-entity-store.md). Následujících klíčové měrné systémy agregace byly použity jako základ obsahu.

| Celek            | Klíčové měření agregace | Datový zdroj pro Finance and Operations | Pole             | popis                       |
|-------------------|---------------------------|---------------------------------------------|-------------------|-----------------------------------|
| Záznamy výpisu | Čistá změna                | CostAggregatedCostStatementEntryEntity      | součet (\[Částka\])   | Částka v zúčtovací měně |
| Záznamy výpisu | Množství čisté změny       | CostAggregatedCostStatementEntryEntity      | součet\[Množství\] |                                   |

Následující tabulka zobrazuje, jak se používají klíčové měrné systémy agregace k vytvoření několika vypočtených hodnot v souboru dat obsahu.

| Měřítko                                 | Jak vypočítat míru                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Počáteční zůstatek                       | \[Konečný zůstatek\]-\[Čistá změna\]                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Množství počátečního zůstatku              | \[Množství koncového zůstatku\]-\[Množství čisté změny\]                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Konečný zůstatek                          | CALCULATE(SUM(\[Částka\]), FILTER(ALLEXCEPT('Fiskální kalendáře', 'Fiskální kalendáře'\[LedgerRecId\], 'entity'\[ID\], 'entity'\[Název\], 'Hlavní knihy'\[Měna\], 'Hlavní knihy'\[Popis\], 'Hlavní knihy'\[Název\]), 'Fiskální kalendáře'\[Datum\] &lt;= MAX('Fiskální kalendáře'\[Datum\])))                                                                                                                                                                                           |
| Množství konečného zůstatku                 | CALCULATE(SUM(\[Množství\]), FILTER(ALLEXCEPT('Fiskální kalendáře', 'Fiskální kalendáře'\[LedgerRecId\], 'entity'\[ID\], 'entity'\[Název\], 'Hlavní knihy'\[Měna\], 'Hlavní knihy'\[Popis\], 'Hlavní knihy'\[Název\]), 'Fiskální kalendáře'\[Datum\] &lt;= MAX('Fiskální kalendáře'\[Datum\])))                                                                                                                                                                                         |
| Počáteční zůstatek zásob             | CALCULATE(\[Počáteční zůstatek\], 'Záznamy výpisu'\[Typ výpisu\] = "Zásoby")                                                                                                                                                                                                                                                                                                                                                                                      |
| Konečný zůstatek zásob                | CALCULATE(\[Konečný zůstatek\], 'Záznamy výpisu'\[Typ výpisu\] = "Zásoby")                                                                                                                                                                                                                                                                                                                                                                                         |
| Čistá změna zásob                    | CALCULATE(\[Čistá změna\], 'Záznamy výpisu'\[Typ výpisu\] = "Zásoby")                                                                                                                                                                                                                                                                                                                                                                                             |
| Množství čisté změny zásob           | CALCULATE(\[Množství čisté změny\], 'Záznamy výpisu'\[Typ výpisu\] = "Zásoby")                                                                                                                                                                                                                                                                                                                                                                                    |
| Čistá změna zásob %                  | IF (\[Konečný zůstatek zásob\] = 0, 0, \[Čistá změna zásob\] / \[Konečný zůstatek zásob\])                                                                                                                                                                                                                                                                                                                                                                           |
| Obrat zásob podle částky                | if(OR (\[Průměrný zůstatek zásob\] &lt;= 0, \[Prodané zásoby nebo spotřebované výdeje\] &gt;= 0), 0, ABS (\[Prodané zásoby nebo spotřebované výdeje\]) /\[Průměrný zůstatek zásob\])                                                                                                                                                                                                                                                                                                  |
| Průměrný zůstatek zásob               | (\[Konečný zůstatek zásob\] + \[Počáteční zůstatek zásob\]) / 2                                                                                                                                                                                                                                                                                                                                                                                                       |
| Prodané zásoby nebo spotřebované výdeje       | \[Prodané zásoby\] + \[Náklady na spotřebovaný materiál zásob\]                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Náklady na spotřebovaný materiál zásob        | CALCULATE(\[Čistá změna zásob\], 'Záznamy výpisu'\[Název kategorie - úroveň 2\_\] = "ConsumedMaterialsCost")                                                                                                                                                                                                                                                                                                                                                            |
| Prodané zásoby                          | CALCULATE(\[Čistá změna zásob\], 'Záznamy výpisu'\[Název kategorie - úroveň 2\_\] = "Prodáno")                                                                                                                                                                                                                                                                                                                                                                             |
| Přesnost zásob podle částky            | IF(\[Konečný zůstatek zásob\] &lt;= 0, IF(OR(\[Spočtená částka zásob\] &lt;&gt; 0, \[Konečný zůstatek zásob\] &lt; 0), 0, 1), MAX (0, (\[Konečný zůstatek zásob\] -ABS (\[Spočtená částka zásob\])) /\[Konečný zůstatek zásob\]))                                                                                                                                                                                                                              |
| Spočtená částka zásob                | CALCULATE(\[Čistá změna zásob\], 'Záznamy výpisu'\[Název kategorie - úroveň 3\_\] = "Inventura")                                                                                                                                                                                                                                                                                                                                                                         |
| Prodlení zásob                         | if(ISBLANK(max('Fiskální kalendáře'\[Datum\])), blank(), MAX(0, MIN(\[Množství příjemek prodlení zásob\], \[Množství konečného zůstatku prodlení zásob\] - \[Množství příjemek prodlení zásob v budoucnosti\]))) \* \[Průměrné náklady na jednotku zásob\]                                                                                                                                                                                                                                |
| Množství příjemek prodlení zásob       | IF(\[minDate\] = \[minDateAllSelected\], CALCULATE (\[Množství čisté změny zásob\], 'Záznamy výpisu'\[Množství\] &gt; 0, FILTER(ALLEXCEPT ('Fiskální kalendáře', 'Fiskální kalendáře'\[LedgerRecId\], 'entity'\[ID\], 'entity'\[název\], 'Hlavní knihy'\[Měna\], 'Hlavní knihy'\[Popis\], 'Hlavní knihy'\[Název\]), 'Fiskální kalendáře'\[Datum\] &lt;= MAX ('Fiskální kalendáře'\[datum\]))), CALCULATE(\[Množství čisté změny zásob\], 'Výpis položek'\[Množství\] &gt; 0)) |
| Množství koncového zůstatku prodlení zásob | \[Množství konečného zůstatku zásob\] + CALCULATE(\[Množství čisté změny zásob\], FILTER(ALLEXCEPT('Fiskální kalendáře', 'Fiskální kalendáře'\[LedgerRecId\], 'entitiy'\[ID\], 'entitiy'\[Název\], 'Hlavní knihy'\[Měna\], 'Hlavní knihy'\[Popis\], 'Hlavní knihy'\[Název\]), 'Fiskální kalendáře'\[Datum\] &gt; max('Fiskální kalendáře'\[Datum\]) ))                                                                                                                                 |
| Příjemky prodlení zásob v budoucnosti  | CALCULATE(\[Čistá změna zásob\], 'Záznamy výpisu'\[Částka\] &gt; 0, FILTER(ALLEXCEPT('Fiskální kalendáře', 'Fiskální kalendáře'\[LedgerRecId\], 'entity'\[ID\], 'entity'\[Název\], 'Hlavní knihy'\[Měna\], 'Hlavní knihy'\[Popis\], 'Hlavní knihy'\[Název\]), 'Fiskální kalendáře'\[Datum\] &gt; MAX('Fiskální kalendáře'\[Datum\])))                                                                                                                                             |
| Průměrné náklady na jednotku zásob                 | CALCULATE(\[Konečný zůstatek zásob\] / \[Množství konečného zůstatku zásob\],ALLEXCEPT('Fiskální kalendáře', 'Fiskální kalendáře'\[LedgerRecId\], 'entity'\[ID\], 'entity'\[Název\], 'Hlavní knihy'\[Měna\], 'Hlavní knihy'\[Popis\], 'Hlavní knihy'\[Název\]))                                                                                                                                                                                                                 |
| Nákupní odchylky                      | CALCULATE(SUM(\[Částka\]), 'Záznamy výpisu'\[Název kategorie - úroveň 2\_\] = "Pořízeno", 'Záznamy výpisu'\[Typ výpisu\] = "Odchylka")                                                                                                                                                                                                                                                                                                                              |
| Počáteční zůstatek NV                   | CALCULATE(\[Počáteční zůstatek\], 'Záznamy výpisu'\[Typ výpisu\] = "NV")                                                                                                                                                                                                                                                                                                                                                                                            |
| Konečný zůstatek NV                      | CALCULATE(\[Konečný zůstatek\], 'Záznamy výpisu'\[Typ výpisu\] = "NV")                                                                                                                                                                                                                                                                                                                                                                                               |
| Čistá změna NV                          | CALCULATE(\[Čistá změna\], 'Záznamy výpisu'\[Typ výpisu\] = "NV")                                                                                                                                                                                                                                                                                                                                                                                                   |
| Čistá změna NV %                        | IF(\[Koncový zůstatek NV\] = 0, 0, \[Čistá změna NV\] / \[Koncový zůstatek NV\])                                                                                                                                                                                                                                                                                                                                                                                             |
| Výrobní odchylky                    | CALCULATE(SUM(\[Částka\]), 'Záznamy výpisu'\[Název kategorie - úroveň 2\_\] = "ManufacturedCost", 'Záznamy výpisu'\[Typ výpisu\] = "Odchylka")                                                                                                                                                                                                                                                                                                                      |
| Název kategorie - úroveň 1                 | switch(\[Název kategorie - úroveň 1\_\], "None", "Žádný", "NetSourcing", "Čisté zdroje", "NetUsage", "Čisté použití", "NetConversionCost", "Čisté náklady převodu", "NetCostOfGoodsManufactured", "Čisté náklady vyrobeného zboží", "BeginningBalance", "Počáteční zůstatek")                                                                                                                                                                                                         |
| Název kategorie - úroveň 2                 | switch(\[Název kategorie - úroveň 2\_\], "None", "Žádný", "Procured", "Pořízeno", "Disposed", "Vyřazeno", "Transferred", "Převedeno", "Sold", "Prodáno", "ConsumedMaterialsCost", "Spotřebované náklady na materiál", "ConsumedManufacturingCost", "Spotřebované výrobní náklady", "ConsumedOutsourcingCost", "Spotřebované náklady na outsourcing", "ConsumedIndirectCost", "Spotřebované nepřímé náklady", "ManufacturedCost", "Výrobní náklady", "Variances", "Odchylky")                            |
| Název kategorie - úroveň 3                 | switch(\[Název kategorie - úroveň 3\_\], "None", "Žádný", "Counting", "Žádný", "ProductionPriceVariance", "Výrobní cena", "QuantityVariance", "Množství", "SubstitutionVariance", "Náhrada", "ScrapVariance", "Odpad", "LotSizeVariance", "Velikost šarže", "RevaluationVariance", "Přecenění", "PurchasePriceVariance", "Nákupní cena", "CostChangeVariance", "Změna nákladů", "RoundingVariance", "Odchylka zaokrouhlení")                                                   |

Následující klíčové dimenze se používají jako filtry k řezu měrných systémů agregace pro dosažení většího rozlišení a poskytnutí hlubších analytických poznatků.

| Celek           | Příklady atributů                       |
|------------------|----------------------------------------------|
| Entity         | ID, název                                     |
| Fiskální kalendáře | Kalendář, měsíc, období, čtvrtletí, rok       |
| Cíle ukazatele KPI        | Cíl přesnosti zásob, cíl obratu zásob |
| Hlavní knihy          | Měna, Název, Popis                  |
| Pracoviště            | ID, Název, Země, Město                      |






