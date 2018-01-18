---
title: "Obsah výkonosti výroby v Power BI"
description: "Toto téma popisuje, co je součástí obsahu výkonosti výroby v Power BI. Vysvětluje přístup k sestavám Power BI a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu."
author: AndersGirke
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: cb43245afe578341251b140383a3b03ba2abd962
ms.openlocfilehash: 592514e9ef8b0ec1e3bacda0f26d5991da88449e
ms.contentlocale: cs-cz
ms.lasthandoff: 12/19/2017

---

# <a name="production-performance-power-bi-content"></a>Obsah výkonosti výroby v Power BI

[!include[banner](../includes/banner.md)]

Toto téma popisuje, co je součástí obsahu **výkonnosti výroby** v Microsoft Power BI. Vysvětluje přístup k sestavám Power BI a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu.

## <a name="overview"></a>Přehled

Obsah **Výkonnost výroby** pro Power BI je určený pro výrobní manažery nebo osoby v rámci organizace, které odpovídají za kontrolu výroby.

Sestavy, které jsou zahrnuty, umožňují používat Power BI spotřeby ke sledování výkonu výrobních operací z hlediska včasné realizace, kvality a nákladů. Sestavy používají transakční data z výrobních zakázek a dávkových objednávek a poskytují agregované zobrazení metrik výroby na úrovni celé společnosti a rozúčtování metrik podle produktu a zdroje.

Obsah Power BI zvýrazňuje schopnost organizace dokončit výrobu včas a v plném rozsahu. Budoucí výkon je plánovaný na základě plánů výroby. Komplexní sestavy zajišťují komplexní přehled o vadách produktů, které vznikly během výroby, míry závad pro prostředky a operace.

Tento obsah Power BI také lze analyzuje výrobní odchylky. Výrobní odchylky se vypočítávají jako rozdíl mezi odhadovanými a realizovanými náklady. Výrobní odchylky se vypočítají, když výrobní zakázky nebo dávkové objednávky dosáhnou stavu **Ukončeno**.

Obsah **Výkonnost výroby** v Power BI zahrnuje data, která pocházejí z výrobních zakázek a dávkových objednávek. Sestavy neobsahují data, která souvisí s kanbanovými výrobami.

## <a name="accessing-the-power-bi-content"></a>Přístup k obsahu Power BI
Obsah Power BI **Výkonnost výroby** se zobrazí na stránce **Výkonnost výroby** (**Řízení výroby** > **Dotazy a sestavy** > **Analýza výkonnosti výroby** > **Výkonnost výroby**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metriky, které jsou součástí obsahu Power BI

Obsah **Výkonnost výroby** v Power BI zahrnuje sadu stránek sestavy. Každá stránka obsahuje sadu metrik, které jsou zobrazovány jako grafy, dlaždice a tabulky.

Následující tabulka poskytuje přehled zahrnutých vizualizací.

| Stránka sestavy                                | Grafy                                               | Dlaždice |
|--------------------------------------------|------------------------------------------------------|-------|
| Výkon výroby                     | <ul><li>Množství výroby podle data</li><li>Množství výroby podle produktu a skupiny položek</li><li>Množství plánované výroby podle data</li><li>Dolních 10 produktů podle včasného a plného dodání</li></ul> | <ul><li>Celkem objednávek</li><li>Včas a v plném rozsahu %</li><li>Neúplné v %</li><li>Včasné v %</li><li>Zpožděné v %</li></ul> |
| Vady podle produktu                         | <ul><li>Míra vad (ppm) dle data</li><li>Míra chyb (ppm) podle produktu a skupiny položek</li><li>Dosud vyrobené množství</li><li>10 hlavních produktů podle platné sazby</li></ul> | <ul><li>Míra vad (ppm)</li><li>Chybné množství</li><li>Celkové množství</li></ul> |
| Trend vad podle produktu                   | Míra vad (ppm) podle vyrobeného množství | Míra vad (ppm) |
| Vady podle zdrojů                        | <ul><li>Míra vad (ppm) podle data</li><li>Míra vad (ppm) podle zdroje a pracoviště</li><li>Míra vad (ppm) podle operace</li><li>Hlavních 10 zdrojů podle míry vad</li></ul> | Chybné množství |
| Trendy vad podle zdroje                  | Míra vad (ppm) podle zpracovaného množství | |
| Výrobní odchylky pro výpočet nákladů na pořadí úloh | <ul><li>Výrobní odchylka podle data a typu nákladové skupiny</li><li>Výrobní odchylka podle pracoviště a typu nákladové skupiny</li><li>10 hlavních produktů s nepříznivou výrobní odchylkou</li><li>10 hlavních produktů s nepříznivou výrobní odchylkou podle zdroje</li></ul> | <ul><li>Realizované náklady</li><li>Výrobní odchylka</li><li>Výrobní odchylka v %</li></ul> |


## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách

Tyto údaje se používají pro stránky sestavy v obsahu **Výkonnost výroby** v Power BI. Tato data jsou vyjádřena jako agregační měření, která jsou rozfázována v úložišti entit. Úložiště entit je databáze Microsoft SQL Server, která je optimalizována pro analýzu. Další informace o úložišti entit získáte v článku [Integrace Power BI s úložištěm entit](power-bi-integration-entity-store.md).

Následující tabulka uvádí klíčová agregovaná opatření, která se používají jako základ obsahu Power BI.

| Celek                   | Klíčová opatření agregace  | Datový zdroj pro Finance and Operations | Pole              |
|--------------------------|-----------------------------|----------------------------------------|--------------------|
| CostCalculation          | CostAmount                  | ProdCalcTransExpanded                  | CostAmount         |
| CostCalculation          | CostMarkup                  | ProdCalcTransExpanded                  | CostMarkup         |
| CostCalculation          | ActualCostAmount            | ProdCalcTransExpanded                  | RealCostAmount     |
| CostCalculation          | RealCostAdjustment          | ProdCalcTransExpanded                  | RealCostAdjustment |
| RouteTransactions        | ErrorQuantity               | ProdRouteTransExpanded                 | QtyError           |
| RouteTransactions        | GoodQuantity                | ProdRouteTransExpanded                 | QtyGood            |
| ProductionOrder          | DaysDelayed                 | ProdTableExpanded                      | DaysDelayed        |
| ProductionOrder          | LeadTime                    | ProdTableExpanded                      | LeadTime           |
| ProductionOrder          | PlannedLeadTime             | ProdTableExpanded                      | PlannedLeadTime    |
| ProductionOrder          | ProductionOrderCount        | ProdTableExpanded                      |                    |
| CoproductCostCalculation | CoproductCostAmount         | PmfCoByProdCalcTransExpanded           | CostAmount         |
| CoproductCostCalculation | CoproductCostMarkup         | PmfCoByProdCalcTransExpanded           | CostMarkup         |
| CoproductCostCalculation | CoproductRealCostAdjustment | PmfCoByProdCalcTransExpanded           | RealCostAdjustment |
| CoproductCostCalculation | CoproductActualCostAmount   | PmfCoByProdCalcTransExpanded           | RealCostAmount     |

Následující tabulka zobrazuje, jak se používají klíčové měrné systémy agregace k vytvoření několika vypočtených hodnot v souboru dat obsahu.

| Výměra                  | Jak vypočítat míru |
|--------------------------|-------------------------------|
| Výrobní odchylka, v %   | SUMA('Výrobní odchylka'[Výrobní odchylka]) / SUMA('Výrobní odchylka'[Odhadované náklady]) |
| Všechny plánované objednávky       | COUNTROWS('Plánovaná výrobní zakázka') |
| Včasné                    | COUNTROWS(FILTER('Plánovaná výrobní zakázka', Plánovaná výrobní zakázka'[Plánované koncové datum] \< 'Plánovaná výrobní zakázka'[Datum požadavku])) |
| Zpožděné                     | COUNTROWS(FILTER('Plánovaná výrobní zakázka', Plánovaná výrobní zakázka'[Plánované koncové datum] \> 'Plánovaná výrobní zakázka'[Datum požadavku])) |
| Včas                  | COUNTROWS(FILTER('Plánovaná výrobní zakázka', Plánovaná výrobní zakázka'[Plánované koncové datum]= ' 'Plánovaná výrobní zakázka'[Datum požadavku])) |
| Včas %                | IF ( 'Plánovaná výrobní zakázka'[Včas] \<\> 0, 'Plánovaná výrobní zakázka'[Včas], IF ('Plánovaná výrobní zakázka'[Všechny plánované zakázky] \<\> 0, 0, BLANK()) ) / 'Plánovaná výrobní zakázka'[Všechny plánované zakázky] |
| Dokončené                | COUNTROWS(FILTER('Výrobní zakázka', 'Výrobní zakázka'[Je s RAF] = TRUE)) |
| Míra vad (ppm)     | IF( 'Výrobní zakázka'[Celkové množství] = 0, BLANK(), (SUM('Výrobní zakázka'[Vadné množství]) / 'Výrobní zakázka'[Celkové množství]) \* 1000000) |
| Zpožděné plnění termínů výroby  | 'Výrobní zakázka'[Pozdě \#] / 'Výrobní zakázka'[Dokončená] |
| Včas a v plném rozsahu          | COUNTROWS(FILTER('Výrobní zakázka', 'Výrobní zakázka'[Je v plném rozsahu] = TRUE && 'Výrobní zakázka'[Je včas] = TRUE)) |
| Včas \#                 | COUNTROWS(FILTER('Výrobní zakázka', 'Výrobní zakázka'[Je včas] = TRUE)) |
| Včasné v %                  | IFERROR( IF('Výrobní zakázka'[Včas \#] \<\> 0, 'Výrobní zakázka'[Včas \#], IF('Výrobní zakázka'[Celkem zakázek] = 0, BLANK(), 0)) / 'Výrobní zakázka'[Celkem zakázek], BLANK()) |
| Neúplné               | COUNTROWS(FILTER('Výrobní zakázka', 'Výrobní zakázka'[Je v plném rozsahu] = FALSE && 'Výrobní zakázka'[Je s RAF] = TRUE)) |
| Neúplné v %             | IFERROR( IF('Výrobní zakázka'[Neúplné] \<\> 0, 'Výrobní zakázka'[Neúplné], IF('Výrobní zakázka'[Celkem zakázek] = 0, BLANK(), 0)) / 'Výrobní zakázka'[Celkem zakázek], BLANK()) |
| Je zpožděno               | 'Výrobní zakázka'[Je s RAF] = TRUE && 'Výrobní zakázka'[Hodnota Zpoždění] = 1 |
| Je včas                 | 'Výrobní zakázka'[Je s RAF] = TRUE && 'Výrobní zakázka'[Dny zpoždění] \< 0 |
| Je v plném rozsahu               | 'Výrobní zakázka'[Dobré množství] \>= 'Výrobní zakázka'[Plánované množství] |
| Je s RAF                | 'Výrobní zakázka'[Hodnota Stav výroby] = 5 \|\| 'Výrobní zakázka'[Hodnota Stav výroby] = 7 |
| Zpoždění a v plném rozsahu           | COUNTROWS(FILTER('Výrobní zakázka', 'Výrobní zakázka'[Je v plném rozsahu] = TRUE && 'Výrobní zakázka'[Je zpožděna] = TRUE)) |
| Zpožděné \#                  | COUNTROWS(FILTER('Výrobní zakázka', 'Výrobní zakázka'[Je zpožděná] = TRUE)) |
| Zpožděné v %                   | IFERROR( IF('Výrobní zakázka'[Pozdě \#] \<\> 0, 'Výrobní zakázka'[Pozdě \#], IF('Výrobní zakázka'[Celkem zakázek] = 0, BLANK(), 0)) / 'Výrobní zakázka'[Celkem zakázek], BLANK()) |
| Včas a v plném rozsahu        | COUNTROWS(FILTER('Výrobní zakázka', 'Výrobní zakázka'[Je plně realizovaná] = TRUE && 'Výrobní zakázka'[Je zpožděná] = FALSE && 'Výrobní zakázka'[Je včas] = FALSE)) |
| Včas a v plném rozsahu %      | IFERROR( IF('Výrobní zakázka'[Včas a úplná] \<\> 0, 'Výrobní zakázka'[Včas a úplná], IF('Výrobní zakázka'[Dokončeno] = 0, BLANK(), 0)) / 'Výrobní zakázka'[Dokončeno], BLANK()) |
| Celkem objednávek             | COUNTROWS('Výrobní zakázka') |
| Celkové množství           | SUM('Výrobní zakázka'[Dobré množství]) + SUM(Výrobní zakázka'[Vadné množství]) |
| Míra vad (ppm)        | IF( 'Transakce směrování'[Zpracované množství] = 0, BLANK(), (SUM('Transakce směrování'[Vadné množství]) / 'Transakce směrování'[Zpracované množství]) \* 1000000) |
| Smíšený poměr závad (ppm) | IF( 'Transakce směrování'[Celkem kombinované množství] = 0, BLANK(), (SUM('Transakce směrování'[Vadné množství]) / 'Transakce směrování'[Celkem kombinované množství]) \* 1000000) |
| Zpracované množství       | SUM('Transakce směrování'[Dobré množství]) + SUM('Transakce směrování'[Vadné množství]) |
| Celkové kombinované množství     | SUM('Výrobní zakázka'[Dobré množství]) + SUM('Transakce směrování'[Vadné množství]) |

Následující tabulka uvádí klíčové dimenze, které se používají jako filtry k rozdělení agregovaných měření, aby bylo možné dosáhnout většího odstupňování a získat hlubší analytický přehled.

| Celek                    | Příklady atributů                                        |
|---------------------------|---------------------------------------------------------------|
| Datum vykázání dokončeného množství | Datum, měsíc a rok dokončení (RAF)                 |
| Datum ukončení                | Ukončeno posunutí měsíce a měsíc                                  |
| Datum požadavku          | Posunutí měsíce data požadavku a datum požadavku            |
| Datum transakce postupu    | Posunutí a datum měsíce transakce technologického postupu                       |
| Pracoviště                     | ID pracovišť, název pracoviště, stát a město                          |
| Entity                  | ID a jméno                                                   |
| Zdroje                 | ID prostředku, název prostředku, typ prostředku a skupiny prostředků |
| Produkty                  | Číslo produktu, název produktu, ID položky a skupina položek         |



