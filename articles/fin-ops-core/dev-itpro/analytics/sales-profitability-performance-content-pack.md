---
title: Obsah výkonu prodeje a ziskovosti Power BI
description: Toto téma popisuje, co je součástí obsahu Power BI Prodej a ziskovost. Vysvětluje přístup k sestavám Power BI a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu.
author: ShylaThompson
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SalesProfitabilityPerformancePowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f7929aeed9a1f1e334d8c75ef941b601d8c6b664
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769917"
---
# <a name="sales-and-profitability-performance-power-bi-content"></a>Obsah výkonu prodeje a ziskovosti Power BI

[!include [banner](../includes/banner.md)]

Toto téma popisuje, co je součástí obsahu **Prodej a ziskovost** v Microsoft Power BI. Vysvětluje přístup k sestavám Power BI a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu.

## <a name="overview"></a>Přehled

Obsah **Výkon prodeje a ziskovosti** Power BI byl vytvořen tak, aby manažeři prodeje mohli monitorovat prodejní klíčové metriky příjmů, hrubého zisku a ziskové marže. Používá prodejní transakční data a poskytuje agregované zobrazení nákupní celopodnikových údajů a rozpis výkonu prodeje podle odběratelů a produktů.

Sestavy zvýrazňují změny v nárůstu výnosů a zisků v průběhu času. Proto lze sestavy používat k upozornění manažerů na pozitivní a negativní trendy výdajů u jednotlivých zákazníků a výrobků. Kromě toho grafy porovnávají výnosy a ziskovost různých produktových kategorií a skupiny zákazníků. Z toho vyplývá, že manažeři pro kategorie a regionální manažeři mohou určovat silné a slabé stránky. Nakonec komplexní sestava vykreslí výnosy jednotlivých zákazníků vs. marže ze zisku. Account manažeři tak mají podložený datový základ, který mohou používat k vyladění prodejních a marketingových snah pro jednotlivé profily zákazníků.

Obsah **Výkon prodejů a ziskovosti** (Výkon prodejů a ziskovosti) prodejním manažerům umožňuje analyzovat prodejní výsledky následovně:

- Výnosy, od konce roku (podle skupiny zákazníků a jednotlivých zákazníků, prodejních kategorií a jednotlivých produktů a zeměpisných míst)
- Změna výnosu, rok od roku (regionů a kategorie prodeje zákazníka)

Ziskovost lze analyzovat následujícími způsoby:

- Hrubý zisk a zisková marže (podle skupin zákazníků a prodejních kategorií produktů)
- Změna hrubého zisku, rok od roku
- Ziskovost zákazníků (podle výnosů versus hrubá marže)

## <a name="accessing-the-power-bi-content"></a>Přístup k obsahu Power BI
Obsah **Výkon prodeje a ziskovosti** Power BI se zobrazí na stránce **Výkon prodeje a ziskovosti** (**Prodej a marketing** \> **Dotazy a sestavy** \> **Analýza prodejních výsledků** \> **Výkon prodeje a ziskovosti**).

## <a name="metricsthat-are-included-in-the-power-bi-content"></a>Metriky, které jsou součástí obsahu Power BI
Obsah **Výkon prodeje** a ziskovosti Power BI obsahuje sestavu, která obsahuje sadu metrik. Tyto metriky jsou zobrazována jako grafy, dlaždice a tabulky. Následující tabulka poskytuje přehled vizualizací v obsahu.

| Stránka sestavy            | Grafy                                     | Dlaždice                                                   |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| Výnos podle odběratele    | Top 10 odběratelů podle výnosu                | Celkový výnos                                           |
|                        | Celkové výnosy podle skupin zákazníků            | Meziroční růst výnosů                                      |
|                        | Průměrný výnos zákazníka podle skupiny odběratelů | Hrubá marže                                            |
|                        | Výnosy a hrubý zisk podle skupiny zákazníků   |                                                         |
| Výnos podle produktu     | Výnos a hrubý zisk podle kategorie prodeje   | Celkový \# produktů                                    |
|                        | Top 10 produktů podle výnosu                 | Celkový počet aktivních produktů a procento z celkového počtu produktů |
|                        | Celkové výnosy podle kategorie prodeje            | Počet účtování produktů pro 80 % výnosů           |
| Výnos podle období\*    | Výnos podle měsíce                           | Meziroční růst výnosů                                      |
|                        | Koncová odchylka výnosu, meziroční             | Meziroční růst výnosů v %                                    |
|                        | Celková odchylka prodeje podle oblasti zákazníka    |                                                         |
| Výnos podle skladového místa    | Výnosy z prodeje podle města                      |                                                         |
|                        | Meziroční růst výnosů v %                       |                                                         |
|                        | Výnosy z prodeje podle oblasti                    |                                                         |
| Ziskovost zákazníků | Hrubá marže vs. výnos podle zákazníka   | Hrubý zisk, hrubá marže, meziroční růst výnosů          |
| Analýza ziskovosti | Výnosy a hrubý zisk podle měsíce          |                                                         |
|                        | Top 15 zákazníků podle hrubé marže           |                                                         |
|                        | Hrubý zisk za měsíc, meziroční                 |                                                         |

\* Výnosy v tomto a minulém roce a růst podle kategorie prodeje.

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách
Následující data se používají k naplnění stránek sestavy v obsahu **Výkon prodeje a ziskovosti** v Power BI. Tato data jsou vyjádřena jako agregační měření, která jsou rozfázována v úložišti entit. Úložiště entit je databáze Microsoft SQL Server, která je optimalizována pro analýzu. Další informace naleznete v tématu [Integrace Power BI s úložištěm entit](power-bi-integration-entity-store.md).

Souhrnná opatření v tomto balíčku obsahu jsou podmnožinou celkových opatření, která byla k dispozici v prodejní datové krychli v Microsoft Dynamics AX 2012 a Microsoft Dynamics AX 2012 R3. Příprava fází agregovaných opatření krychle v úložišti Entity vyžaduje, aby bylo možné je nasadit. Další informace získáte v postupu nastavování agregovaných opatření v úložišti entity v příspěvku v blogu [Integrace Power BI s úložištěm entit v aplikaci Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) 

Následující klíčová agregovaná opatření jsou k dispozici přímo z entity řádky faktury a slouží jako základ obsahu.

| Celek        | Klíčová opatření agregace                   | Zdroj dat pro Dynamics 365. | Pole                                        | popis                                       |
|---------------|----------------------------------------------|------------------------------|----------------------------------------------|---------------------------------------------------|
| Řádky faktury | Výnosy                                      | CustInvoiceTrans             | SUM(LineAmountMST)                           | Částka v zúčtovací měně.            |
|               | Náklady prodaného zboží                           | InventTrans                  | SUMA(CostAmountPosted + CostAmountAdjustment) | Součet částky nákladů a oprava.    |
|               | Částka řádku provize – zúčtovací měna | CustInvoiceTrans             | SUMA(CommissAmountMST)                        | Částka provize v zúčtovací měně. |

Následující tabulka zobrazuje, jak se používají klíčová agregovaná opatření v entitě řádku Faktury k vytvoření několika vypočtených hodnot v souboru dat obsahu.

| Výměra           | Výpočet                                                                                      |
|-------------------|--------------------------------------------------------------------------------------------------|
| Hrubý zisk      | SUM(Výnos – COGS – Provize – (DPH (zahrnutá v částce na řádku faktury dodavatele))          |
| Hrubá marže      | SUMA(Hrubý zisk / (Výnos – (DPH (zahrnutá v částce na řádku faktury dodavatele)))             |
| Výnosy z minulého roku | Výnos za minulý rok = CALCULATE(SUM('Invoice lines'\[Revenue\]), SAMEPERIODLASTYEAR(Dates\[Date\])) |

Následující tabulka uvádí klíčové dimenze v prodejní krychli, které se používají jako filtry k rozdělení agregovaných měření, aby bylo možné dosáhnout většího odstupňování a získat hlubší analytický přehled.

| Celek           | Příklady atributů                               |
|------------------|------------------------------------------------------|
| Zákazníci        | Skupiny odběratelů, oblasti zákazníka, adresa, průmysl |
| Produkty         | Číslo produktu, název produktu, název skupiny zboží       |
| Kategorie prodeje | Názvy kategorie prodeje                                 |
| Právnické osoby   | Jména právnické osoby                                   |
| Data            | Data                                                |

Ve výchozím nastavení obsah zobrazuje data pro aktuální kalendářní rok. Můžete však změnit filtr dat v části filtrů sestavy. Můžete také změnit filtr společnosti.
