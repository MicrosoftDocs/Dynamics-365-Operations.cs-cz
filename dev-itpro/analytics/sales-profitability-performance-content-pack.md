---
title: "Obsah výkonu prodeje a ziskovosti Power BI"
description: "Toto téma popisuje, co je součástí aplikace Dynamics 365 for Operations - Sales a balíčku obsahu výkonnosti pro Microsoft Power BI. Popisuje, jak získat přístup k sestavám, které jsou obsaženy v balíčku obsahu, a uvádí informace o datovém modelu a entitách, které se používají k vytváření balíčku obsahu."
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

# <a name="sales-and-profitability-performance-power-bi-content"></a>Obsah výkonu prodeje a ziskovosti Power BI

Toto téma popisuje, co je součástí aplikace Dynamics 365 for Operations - Sales a balíčku obsahu výkonnosti pro Microsoft Power BI. Popisuje, jak získat přístup k sestavám, které jsou obsaženy v balíčku obsahu, a uvádí informace o datovém modelu a entitách, které se používají k vytváření balíčku obsahu.

<a name="overview"></a>Přehled
--------

Tento balíček obsahu byl vytvořen pro prodejní manažery ke sledování klíčových metrik pro výnosy, hrubý zisk a zisková rozpětí. Používá prodejní transakční data z Microsoft Dynamics 365 for Operations a poskytuje agregované zobrazení nákupní celopodnikových údajů a rozpis výkonu prodeje podle odběratelů a produktů. Zvýrazněním změn v růstu výnosů a zisku v čase lze sestavy používat k upozornění správců na pozitivní a negativní trendy pro jednotlivé odběratele a produkty. Manažeři kategorií a regionální manažeři budou považovat za užitečné vlastnictví grafů, které porovnávají výnosy a ziskovost různých produktových kategorií a skupin zákazníků s jednoduchými opozdilci a vůdci. Souhrnná sestava, která vykresluje výnos jednotlivého odběratele oproti ziskovému rozpětí, nabízí account manažerům základ na základě dat pro vyladění prodejních a marketingových snah pro příslušný profil jednotlivých zákazníků. Balíček obsahu pro Prodej a ziskovost umožňuje prodejním manažerům analyzovat prodejní výsledky podle:

-   Výnosy, od konce roku (podle skupiny zákazníků a jednotlivých zákazníků, prodejních kategorií a jednotlivých produktů a zeměpisných míst)
-   Změna výnosu, rok od roku (regionů a kategorie prodeje zákazníka)

Ziskovost může být analyzována podle:

-   Hrubý zisk a zisková marže (podle skupin zákazníků a prodejních kategorií produktů)
-   Změna hrubého zisku, rok od roku
-   Ziskovost zákazníků (podle výnosů versus hrubá marže)

## <a name="accessing-the-content-pack"></a>Přístup k balíčku obsahu
Balíček obsahu Power BI výkonu prodeje a ziskovosti je publikován jako implementační aktivum v Microsoft Dynamics Lifecycle Services (LCS) a je přístupný z Microsoft Dynamics 365 for Operations. Další informace o přístupu k otevřeným sestavám Power BI a jejich spouštění, viz [Obsahu Power BI od společnosti Microsoft a partnerů v LCS](power-bi-content-microsoft-partners.md).

## <a name="metrics-included-in-the-content-pack"></a>Metriky zahrnuté v balíčku obsahu
Balíček obsahu analýzy zahrnuje sestavu, která sestává ze sady metrik vizualizovaných jako grafy, dlaždice a tabulky. Následující tabulka poskytuje přehled vizualizací v balíčku obsahu.

|                        |                                            |                                                         |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| **Stránka sestavy**        | **Grafy**                                 | **Dlaždice**                                               |
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
Data aplikace Dynamics 365 for Operations se používají k naplnění sestavy v balíčku obsahu prodejů a ziskovosti. To je vyjádřeno jako měrné systémy agregace, které jsou rozfázovány v úložišti entit, což je databáze Microsoft SQL optimalizovaná pro analýzy. Více si o tom můžete přečíst v blogu [Integrace Power BI s úložištěm entit v Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Souhrnná opatření v tomto balíčku obsahu jsou podmnožinou celkových opatření, která byla k dispozici v prodejní datové krychli v Dynamics AX 2012 a AX 2012 R3. Příprava fází agregovaných opatření v úložišti entit vyžaduje, aby bylo možné je nasadit. Další informace získáte v postupu fázování agregovaných opatření v úložišti entity v příspěvku v blogu [Integrace Power BI s úložištěm entit v aplikaci Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Následující klíčová agregovaná opatření jsou k dispozici přímo z entity řádky faktury a slouží jako základ balíčku obsahu.

|               |                                              |                                                 |                                              |                                          |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|------------------------------------------|
| **Entita**    | **Klíčová opatření agregace**               | **Zdroj dat pro aplikaci Dynamics 365 for Operations** | **Pole**                                    | **Popis**                          |
| Řádky faktury | Výnosy                                      | CustInvoiceTrans                                | SUM(LineAmountMST)                           | Částka v zúčtovací měně            |
|               | Náklady prodaného zboží                           | InventTrans                                     | SUMA(CostAmountPosted + CostAmountAdjustment) | Částka nákladů + úprava                 |
|               | Částka řádku provize – zúčtovací měna | CustInvoiceTrans                                | SUMA(CommissAmountMST)                        | Částka řádku provize v zúčtovací měně |

Následující tabulka zobrazuje, jak se používají klíčová agregovaná opatření v entitě řádku faktury k vytvoření několika vypočtených hodnot v souboru dat obsahu.

|                   |                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------|
| **Opatření**       | **Vypočítáno podle**                                                                                |
| Hrubý zisk      | SUM(Výnos – COGS – Provize – (DPH (zahrnutá v částce na řádku faktury dodavatele))          |
| Hrubá marže      | SUMA(Hrubý zisk / (Výnos – (DPH (zahrnutá v částce na řádku faktury dodavatele)))             |
| Výnosy z minulého roku | Výnos za minulý rok = CALCULATE(SUM('Invoice lines'\[Revenue\]), SAMEPERIODLASTYEAR(Dates\[Date\])) |

Následující klíčové dimenze v **prodejní krychli** se používají jako filtry k řezu měrných systémů agregace pro dosažení většího rozlišení a poskytnutí hlubších analytických poznatků.

|                  |                                                      |
|------------------|------------------------------------------------------|
| **Entita**       | **Příklady atributů**                           |
| Zákazníci        | Skupiny odběratelů, oblasti zákazníka, adresa, průmysl |
| Produkty         | Číslo produktu, název produktu, název skupiny zboží       |
| Kategorie prodeje | Názvy kategorie prodeje                                 |
| Právnické osoby   | Jména právnické osoby                                   |
| Data            | Data                                                |

Ve výchozím nastavení balíček obsahu zobrazuje data pro aktuální kalendářní rok, ale můžete otevřít oddíl filtrů sestavy a změnit filtr dat. Můžete také změnit filtr společnosti.

## <a name="additional-resources"></a>Další prostředky
Zde uvádíme některé užitečné odkazy související s entitami a vytvářením obsahu v aplikaci Power BI:

-   [Datové entity](..\data-entities\data-entities.md)
-   [Vytvoření organizačního balíčku obsahu](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Modelování dat pomocí aplikace Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Přidání dlaždic Power BI do pracovních prostorů](configure-power-bi-integration.md)



