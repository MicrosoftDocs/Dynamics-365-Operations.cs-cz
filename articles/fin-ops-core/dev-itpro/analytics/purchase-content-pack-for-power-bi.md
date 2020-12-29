---
title: Analýza obsahu výdajů na nákup v Power BI
description: Toto téma popisuje, co je součástí obsahu analýzy nákupu a výdajů v Power BI. Popisuje, jak získat přístup k sestavám, které jsou obsaženy v obsahu, a uvádí informace o datovém modelu a entitách, které se používají k vytváření obsahu.
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3f556cf2e506c57e465c2a86485d2cdd4cf8b65e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680607"
---
# <a name="purchase-spend-analysis-power-bi-content"></a>Analýza obsahu výdajů na nákup v Power BI

[!include [banner](../includes/banner.md)]

Toto téma popisuje, co je součástí obsahu **analýzy nákupu a výdajů** v Microsoft Power BI. Vysvětluje přístup k sestavám Power BI a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu.

## <a name="overview"></a>Přehled

Obsah **Analýza nákupních výdajů** v Power BI byl vytvořen, aby pomohl nákupním manažerům a vedoucím pracovníkům, kteří odpovídají za rozpočty, sledovat nákupní výdaje. Manažeři mohou analyzovat nákupní výdaje následujícím způsobem:

- Nákup k datu v daném roce (podle skupiny dodavatelů a jednotlivých dodavatelů, kategorie zásobování a jednotlivých produktů a umístění dodavatele)
- Rok přes rok nákupu změna (podle skupiny a zadávání zakázek kategorií dodavatele)

Obsah používá nákupní transakční data a poskytuje agregované zobrazení nákupní celopodnikových údajů a rozpis nákupních výdajů podle dodavatelů a produktů. V sestavách jsou zvýrazněny změny nákupních výdajů v průběhu času. Proto lze sestavy používat k upozornění manažerů na pozitivní a negativní trendy výdajů u jednotlivých dodavatelů a výrobků. Grafy dále zobrazují nákupní výdaje pro zásobování různých kategorií a skupin dodavatelů. Proto manažeři pro kategorie a regionální manažeři mohou tyto grafy používat k identifikaci změn v chování při výdajích.

## <a name="accessing-the-power-bi-content"></a>Přístup k obsahu Power BI
Obsah **Analýza nákupu a výdajů** v Power BI se zobrazí na stránce **Analýza nákupu a výdajů** (**Zásobování a zdroje** \> **Dotazy a sestavy** \> **Analýza výkonu nákupu** \> **Analýza nákupu a výdajů**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metriky, které jsou součástí obsahu Power BI
**Balíček obsahu analýzy investic** Power BI do nákupu obsahuje sestavu, která obsahuje sadu metrik. Tyto metriky jsou zobrazována jako grafy, dlaždice a tabulky. 

Následující sekce poskytují přehled vizualizací.

### <a name="purchase-by-vendor-report-page"></a>Stránka sestavy nákupu podle dodavatele
**Grafy**
- Prvních 10 dodavatelů podle nákupu (skládaný sloupcový graf)
- Celkový nákup podle skupiny dodavatelů / země / name (výsečový graf)
- Nákup podle skupiny dodavatelů / země / název (sloupcový graf)
- Průměrný nákup podle skupiny dodavatelů / země / název (sloupcový graf)

**Dlaždice**
- Celkový nákup
- Meziroční růst nákupů
- Celkový počet dodavatelů
- Celkový počet aktivních dodavatelů

**Příklad**
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a>Stránka sestavy nákupu podle produktu

**Grafy**
- Nákup podle kategorie zásobování / název produktu (sloupcový graf)
- Celkový nákup podle kategorie zásobování / název produktu (výsečový graf)
- Prvních 10 produktů podle nákupu (skládaný sloupcový graf)

**Dlaždice**
- Celkový počet produktů</li>
- Celkové procento aktivních produktů z celkového počtu produktů
- Počet účtování produktů pro 80 % nákupů

**Příklad**


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a>Stránka sestavy nákupu podle období
Tato stránka zobrazuje nákupy v tomto a minulém roce a růst podle kategorie zásobování.

**Grafy** 
- Nákup za měsíc / den (sloupcový graf)
- Kumulativní mezirodčí nákupní odchylka (vodopádový graf)
- Meziroční růst celkového nákupu (sloupcový graf)
- Prohlášení o zadávání veřejných zakázek (matice)

**Dlaždice**
- Meziroční růst nákupů
- Meziroční růst nákupů v %

**Příklad**
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a>Stránka sestavy nákupu podle místa dodavatele

**Grafy**
- Nákup podle města
- Meziroční růst nákupů v %
- Nákup podle země

**Příklad**
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a>Stránka sestavy analýzy výdajů při nákupu podle času

**Grafy** 
- Aktální rok nákupu podle měsíců / den (spojnicový graf)
- Nákup za aktuální a předchozí rok (řádkový a sloupcový graf)

**Příklad**
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a>Stránka sestavy analýzy výdajů při nákupu podle dodavatele

**Grafy** 
- TOP 10 % nákupů dodavatele nákupní (trychtýřový graf)
- Top 10 dodavatelů se zvýšenými investicemi meziročně
- Top 10 dodavatelů se sníženými investicemi meziročně

**Příklad** 
<img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a>Datový model a entity
Následující data se používají k naplnění stránek sestavy v obsahu **Analýza nákupu a výdajů** v Power BI. Tato data jsou vyjádřena jako agregační měření, která jsou rozfázována v úložišti entit. Úložiště entit je databáze Microsoft SQL Server, která je optimalizována pro analýzu. Další informace naleznete v tématu [Integrace Power BI s úložištěm entit](power-bi-integration-entity-store.md).

Souhrnná opatření v tomto balíčku obsahu jsou podmnožinou celkových opatření, která byla k dispozici v nákupní datové krychli v Microsoft Dynamics AX 2012 a Microsoft Dynamics AX 2012 R3. Příprava fází agregovaných opatření krychle v úložišti Entity vyžaduje, aby bylo možné je nasadit. Další informace získáte v postupu nastavování agregovaných opatření v úložišti entity v příspěvku v blogu [Integrace Power BI s úložištěm entity](power-bi-integration-entity-store.md). Následující klíčová agregovaná opatření jsou k dispozici přímo z entity řádky faktury a slouží jako základ obsahu.

| Celek        | Klíčová opatření agregace | Zdroj dat                                 | Pole              | popis                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| Řádky faktury | Nákup                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Částka v zúčtovací měně. |

V následující tabulce jsou uvedena klíčová opatření, která jsou vypočtena z entity řádky faktury.

| Výměra               | Výpočet                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Aktuální rok nákupu | Aktuální rok nákupu = SUM (Řádky faktury\[Nákup\])                                            |
| Minulý nákupní rok    | Minulý nákupní rok = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\])) |
| Meziroční růst nákupů   | Meziroční růst nákup = \[Aktuální nákupní rok\] – \[Minulý nákupní rok\]                            |

Následující klíčové dimenze v obsahu se používají jako filtry k rozdělení agregovaných opatření, aby bylo možné dosažení většího rozlišení a získání hlubších analytických poznatků.

| Celek                 | Příklady atributů                                |
|------------------------|-------------------------------------------------------|
| Dodavatelé                | Skupiny dodavatelů, země nebo oblast dodavatele nebo název dodavatele |
| Produkty               | Číslo produktu, název produktu, název skupiny zboží        |
| Kategorie zásobování | Kategorie zásobování, názvy kategorií zásobování      |
| Právnické osoby         | Jméno právnické osoby                                     |
| Data                  | Data, Posun o rok                                    |

Ve výchozím nastavení obsah zobrazuje data pro aktuální kalendářní rok. Můžete však změnit filtr dat v části filtrů sestavy. Můžete také změnit filtr společnosti.
