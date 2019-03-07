---
title: Analýza obsahu výdajů na nákup v Power BI
description: Toto téma popisuje, co je součástí obsahu analýzy nákupu a výdajů v Power BI. Popisuje, jak získat přístup k sestavám, které jsou obsaženy v obsahu, a uvádí informace o datovém modelu a entitách, které se používají k vytváření obsahu.
author: FrankDahl
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 069c4dc21959ab603ba6ca3da0ac68ef20325265
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "313835"
---
# <a name="purchase-spend-analysis-power-bi-content"></a>Analýza obsahu výdajů na nákup v Power BI

[!include [banner](../includes/banner.md)]

Toto téma popisuje, co je součástí obsahu **analýzy nákupu a výdajů** v Microsoft Power BI. Vysvětluje přístup k sestavám Power BI a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu.

## <a name="overview"></a>Přehled

Obsah **Analýza nákupních výdajů** v Power BI byl vytvořen na pomoc nákupním manažerům a vedoucím pracovníkům, kteří odpovídají za rozpočty, prohlížet nákupní výdaje. Manažeři mohou analyzovat nákupní výdaje následujícím způsobem:

- Nákup k datu v daném roce (podle skupiny dodavatelů a jednotlivých dodavatelů, kategorie zásobování a jednotlivých produktů a umístění dodavatele)
- Rok přes rok nákupu změna (podle skupiny a zadávání zakázek kategorií dodavatele)

Obsah používá nákupní transakční data a poskytuje agregované zobrazení nákupní celopodnikových údajů a rozpis nákupních výdajů podle dodavatelů a produktů. V sestavách jsou zvýrazněny změny nákupních výdajů v průběhu času. Proto lze sestavy používat k upozornění manažerů na pozitivní a negativní trendy výdajů u jednotlivých dodavatelů a výrobků. Grafy dále zobrazují nákupní výdaje pro zásobování různých kategorií a skupin dodavatelů. Proto manažeři pro kategorie a regionální manažeři mohou tyto grafy používat k identifikaci změn v chování při výdajích.

## <a name="accessing-the-power-bi-content"></a>Přístup k obsahu Power BI
Obsah **Analýza nákupu a výdajů** v Power BI se zobrazí na stránce **Analýza nákupu a výdajů** (**Zásobování a zdroje** \> **Dotazy a sestavy** \> **Analýza výkonu nákupu** \> **Analýza nákupu a výdajů**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metriky, které jsou součástí obsahu Power BI
**Balíček obsahu analýzy investic** Power BI do nákupu obsahuje sestavu, která obsahuje sadu metrik. Tyto metriky jsou zobrazována jako grafy, dlaždice a tabulky. Následující tabulka poskytuje přehled vizualizací.

<table>
<thead>
<tr>
<th>Stránka sestavy</th>
<th>Grafy</th>
<th>Dlaždice</th>
</tr>
</thead>
<tbody>
<tr>
<td>Nákup podle dodavatele</td>
<td><ul>
<li>Prvních 10 dodavatelů podle nákupu (skládaný sloupcový graf)</li>
<li>Celkový nákup podle skupiny dodavatelů / země / name (výsečový graf)</li>
<li>Nákup podle skupiny dodavatelů / země / název (sloupcový graf)</li>
<li>Průměrný nákup podle skupiny dodavatelů / země / název (sloupcový graf)</li>
</ul></td>
<td><ul>
<li>Celkový nákup</li>
<li>Meziroční růst nákupů</li>
<li>Celkový počet dodavatelů</li>
<li>Celkový počet aktivních dodavatelů</li>
</ul></td>
</tr>
<tr>
<td>Nákup podle produktu</td>
<td><ul>
<li>Nákup podle kategorie zásobování / název produktu (sloupcový graf)</li>
<li>Celkový nákup podle kategorie zásobování / název produktu (výsečový graf)</li>
<li>Prvních 10 produktů podle nákupu (skládaný sloupcový graf)</li>
</ul></td>
<td><ul>
<li>Celkový počet produktů</li>
<li>Celkové procento aktivních produktů z celkového počtu produktů</li>
<li>Počet účtování produktů pro 80 % nákupů</li>
</ul></td>
</tr>
<tr>
<td>Nákup podle období*</td>
<td><ul>
<li>Nákup za měsíc / den (sloupcový graf)</li>
<li>Kumulativní mezirodčí nákupní odchylka (vodopádový graf)</li>
<li>Meziroční růst celkového nákupu (sloupcový graf)</li>
<li>Prohlášení o zadávání veřejných zakázek (matice)</li>
</ul></td>
<td><ul>
<li>Meziroční růst nákupů</li>
<li>Meziroční růst nákupů v %</li>
</ul></td>
</tr>
<tr>
<td>Nákup podle místa dodavatele</td>
<td><ul>
<li>Nákup podle města</li>
<li>Meziroční růst nákupů v %</li>
<li>Nákup podle země</li>
</ul></td>
<td></td>
</tr>
<tr>
<td>Analýza výdajů při nákupu podle času</td>
<td><ul>
<li>Aktální rok nákupu podle měsíců / den (spojnicový graf)</li>
<li>Nákup za aktuální a předchozí rok (řádkový a sloupcový graf)</li>
</ul></td>
<td></td>
</tr>
<tr>
<td>Analýza výdajů při nákupu podle dodavatele</td>
<td><ul>
<li>TOP 10 % nákupů dodavatele nákupní (trychtýřový graf)</li>
<li>Top 10 dodavatelů se zvýšenými investicemi meziročně</li>
<li>Top 10 dodavatelů se sníženými investicemi meziročně</li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

\* Nákup v tomto a minulém roce a růst podle kategorie zásobování

## <a name="data-model-and-entities"></a>Datový model a entity
Následující data se používají k naplnění stránek sestavy v obsahu **Analýza nákupu a výdajů** v Power BI. Tato data jsou vyjádřena jako agregační měření, která jsou rozfázována v úložišti entit. Úložiště entit je databáze Microsoft SQL Server, která je optimalizována pro analýzu. Další informace naleznete v tématu [Přehled integrace Power BI s úložištěm entit](power-bi-integration-entity-store.md).

Souhrnná opatření v tomto balíčku obsahu jsou podmnožinou celkových opatření, která byla k dispozici v nákupní datové krychli v Microsoft Dynamics AX 2012 a Microsoft Dynamics AX 2012 R3. Příprava fází agregovaných opatření krychle v úložišti Entity vyžaduje, aby bylo možné je nasadit. Další informace získáte v postupu nastavování agregovaných opatření v úložišti entity v příspěvku v blogu [Přehled integrace Power BI s úložištěm entit](power-bi-integration-entity-store.md). Následující klíčová agregovaná opatření jsou k dispozici přímo z entity řádky faktury a slouží jako základ obsahu.

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
