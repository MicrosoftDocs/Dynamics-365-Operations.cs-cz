---
title: "Prodej a ziskovost výkonu obsahu Power BI"
description: "Toto téma popisuje, co je součástí Dynamics 365 pro operace - prodej a ziskovost výkonu obsahu pack pro Microsoft Power BI. Popisuje, jak přístup k sestavám součástí obsahu pack a obsahuje informace o datovém modelu a entit, které se používají k vytváření obsahu pack."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 3e6b48768bb8e69d46f1555d9300f3b878b01ff1
ms.lasthandoff: 03/31/2017


---

# <a name="sales-and-profitability-performance-power-bi-content"></a>Prodej a ziskovost výkonu obsahu Power BI

Toto téma popisuje, co je součástí Dynamics 365 pro operace - prodej a ziskovost výkonu obsahu pack pro Microsoft Power BI. Popisuje, jak přístup k sestavám součástí obsahu pack a obsahuje informace o datovém modelu a entit, které se používají k vytváření obsahu pack.

<a name="overview"></a>Přehled
--------

Tohoto obsahu pack byla vytvořena pro prodejní manažery ke sledování klíčových metrik prodejní výnosy, hrubý zisk a zisková rozpětí. Transakční údaje o prodeji z Dynamics 365 používá pro operace a poskytuje agregované zobrazení hodnoty prodeje celé společnosti i poruchy výkonnosti prodeje pro odběratele a produkty. Zvýrazněním změn v růstu výnosů a zisku v čase lze sestav správcům oznámení o pozitivní a negativní trendy pro jednotlivé odběratele a produkty. Kategorie a regionálními manažery bude užitečné mít grafy, které porovnávají výnosy a ziskovost různých kategorií produktu a skupiny zákazníků navzájem vybrat laggards a vedoucí. Souhrnnou zprávu, která vykresluje jednotlivé odběratele výnos oproti ziskové rozpětí nabídky manažeři zálohovaná data základ pro každého zákazníka příslušného profilu aplikace attune své prodejní a marketingové úsilí. Prodej a ziskovost výkonu obsahu pack umožňuje správcům prodej analyzovat prodejní výsledky podle:

-   Výnosy-na rok (ve skupině zákazníků a jednotlivých zákazníků, prodejních kategorií a jednotlivých produktů a zeměpisných)
-   Výnosu, přes rok rok (podle kategorií regionů a prodeje zákazníka)

Ziskovost může být analyzována podle:

-   Hrubý zisk a marže (podle skupin zákazníků a prodejních kategorií produktů)
-   Změna hrubého zisku, přes roky
-   Ziskovost zákazníků (podle výnosů versus hrubá marže)

## <a name="accessing-the-content-pack"></a>Přístup k obsahu pack
Prodej a ziskovost výkonu Power BI obsahu pack je publikován jako aktivum implementace služby životního cyklu (LCS) a je přístupný z 365 Dynamics pro operace. Další informace o tom, jak získat přístup a spuštění sestav Power BI, viz [obsahu Power BI od společnosti Microsoft a partnerů LCS](power-bi-content-microsoft-partners.md).

## <a name="metrics-included-in-the-content-pack"></a>Metriky, které jsou součástí obsahu pack
Obsahu pack obsahuje sestavu, která obsahuje sadu metriky zobrazována jako grafy, kameny a tabulky. Následující tabulka obsahuje přehled visualisations v obsahu pack.

|                        |                                            |                                                         |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| **Stránky sestavy**        | **Charts**                                 | **Vedle sebe**                                               |
| Výnosy podle zákazníka    | Nejlepších 10 odběratelů podle výnosů                | Celkový výnos                                           |
|                        | Celkové výnosy podle skupin zákazníků            | Po letech růstu výnosů                                      |
|                        | Průměrného zákazníka výnosy podle skupiny odběratelů | Hrubá marže                                            |
|                        | Příjmy a hrubý zisk ve skupině zákazníků   |                                                         |
| Výnosy podle produktu     | Příjmy a hrubý zisk podle kategorie prodeje   | Celkem \#produktů                                    |
|                        | Nejlepších 10 produktů podle výnosů                 | Celkový počet aktivních produktů a procento z celku |
|                        | Celkové výnosy podle kategorie prodeje            | Počet produktů účtování výnosů 80 %           |
| Výnosy podle období\*    | Výnosy podle měsíce                           | Po letech růstu výnosů                                      |
|                        | Koncové odchylky výnosů, po letech             | % Růstu výnosů po letech                                    |
|                        | Celková odchylka prodeje podle oblasti zákazníka    |                                                         |
| Výnosy podle umístění    | Výnosy z prodeje podle města                      |                                                         |
|                        | % Růstu výnosů po letech                       |                                                         |
|                        | Výnosy z prodeje podle oblastí                    |                                                         |
| Ziskovost zákazníků | Hrubá marže versus příjmy podle zákazníků   | Hrubá marže hrubého zisku, po letech růstu výnosů          |
| Analýza ziskovosti | Příjmy a hrubý zisk za měsíc          |                                                         |
|                        | TOP 15 zákazníci podle hrubé marže           |                                                         |
|                        | Hrubý zisk za měsíc, po letech                 |                                                         |

\*Příjmy to a poslední rok a růst podle kategorie prodeje.

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách
Dynamics 365 pro datové operace se používá k naplnění sestavy v okně Prodej a ziskovost výkonu obsahu pack. Prostředí je reprezentováno jako agregační hodnoty, které jsou připraveny v úložišti Entity, která je optimalizována pro analýzu databáze Microsoft SQL. Další informace o to v blogu [BI napájení integrace s úložištěm entit v aplikaci Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Souhrnné měření v tomto obsahu pack jsou podmnožiny celkové měření, která byla k dispozici v krychli prodeje v Dynamics AX 2012 a AX 2012 R3. Příprava agregovaných měr datové krychli v úložišti Entity musíte je nasadit. Další informace naleznete v tématu Postup jak připravit Souhrnné měření do úložiště entita v blogu [BI napájení integrace s úložištěm entit v aplikaci Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Jako základ obsahu pack se používají následující klíče agregovaných měr entity řádky faktury.

|               |                                              |                                                 |                                              |                                          |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|------------------------------------------|
| **Entity**    | **Klíče agregovaných měr**               | **Zdroj dat pro Dynamics 365 pro operace** | **Field**                                    | **Description**                          |
| Řádky faktury | Výnosy                                      | CustInvoiceTrans                                | SUM(LineAmountMST)                           | Částka v zúčtovací měně            |
|               | Náklady prodaného zboží                           | InventTrans                                     | SOUČET (CostAmountPosted + CostAmountAdjustment) | Částka nákladů + úprava                 |
|               | Částka řádku Komise – zúčtovací měna | CustInvoiceTrans                                | SUM(CommissAmountMST)                        | Částka provize v zúčtovací měně |

Následující tabulce jsou uvedeny klíče agregační měření entity faktury řádky použité k vytvoření několika vypočtené rozměry v obsahu pack dataset.

|                   |                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------|
| **Measure**       | **Počítá jako**                                                                                |
| Hrubý zisk      | SOUČET (výnosy – náklady na prodané zboží – Komise – DPH (zahrnuto v částce řádku faktury odběratele))          |
| Hrubá marže      | SOUČET (hrubý zisk / (výnosy - prodejní daň (zahrnutá v částce řádku faktury odběratele)))             |
| Výnosy minulého roku | Výnosy Loni = výpočet (součet (řádky faktur\[výnosů\]), SAMEPERIODLASTYEAR (data\[datum\]) |

Následující klíčové dimenze v **krychle Sales** jsou používány jako filtry k řezu agregovaných měr pro dosažení větší univerzálnost a hlubší analytické poznatky.

|                  |                                                      |
|------------------|------------------------------------------------------|
| **Entity**       | **Příklady atributů**                           |
| Zákazníci        | Skupiny odběratelů, oblasti zákazníka, adresa, průmysl |
| Produkty         | Číslo produktu, název produktu, název skupiny zboží       |
| Kategorie prodeje | Názvy kategorií prodeje                                 |
| Právnické osoby   | Jména právnické osoby                                   |
| Data            | Data                                                |

Ve výchozím obsahu pack zobrazuje data pro aktuální kalendářní rok, ale můžete otevřít oddíl filtry sestavy a změnit filtr data. Můžete také změnit filtr společnosti.

## <a name="additional-resources"></a>Další prostředky
Zde uvádíme některé užitečné odkazy související s entitami a vytvářením obsahu v aplikaci Power BI:

-   [Datové entity](..\data-entities\data-entities.md)
-   [Vytvoření organizačního balíčku obsahu](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Modelování dat pomocí aplikace Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Přidání dlaždic Power BI do pracovních prostorů](configure-power-bi-integration.md)



