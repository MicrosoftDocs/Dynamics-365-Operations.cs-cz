---
title: "Analýza obsahu Power BI výdajů na nákup"
description: "Toto téma popisuje, co je součástí obsahu analýzy výdajů na nákup v Power BI. Popisuje, jak získat přístup k sestavám, které jsou obsaženy v balíčku obsahu, a uvádí informace o datovém modelu a entitách, které se používají k vytváření balíčku obsahu."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: ad0ee95113d05710cccc1a5e9d215b38244c2047
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="purchase-spend-analysis-power-bi-content"></a>Analýza obsahu Power BI výdajů na nákup

[!include[banner](../includes/banner.md)]


Toto téma popisuje, co je součástí obsahu analýzy výdajů na nákup v Power BI. Popisuje, jak získat přístup k sestavám, které jsou obsaženy v balíčku obsahu, a uvádí informace o datovém modelu a entitách, které se používají k vytváření balíčku obsahu.

<a name="overview"></a>Přehled
--------

Obsah balíčku analýzy výdajů na nákup pro Microsoft Power BI byla vytvořena pro nákupní manažery a manažery, kteří jsou zodpovědní za rozpočty. Je navržen tak, aby jim pomáhal kontrolovat výdaje na nákup. Používá nákupní transakční data z Microsoft Dynamics 365 for Operations a poskytuje agregované zobrazení nákupní celopodnikových údajů a rozpis nákupních výdajů podle dodavatelů a produktů. V sestavách jsou zvýrazněny změny nákupních výdajů v průběhu času. Proto je lze používat k upozornění manažerů na pozitivní a negativní trendy výdajů u jednotlivých dodavatelů a výrobků. Grafy zobrazují nákupní výdaje pro zásobování různých kategorií a skupin dodavatelů. Manažeři pro kategorie a regionální manažeři mohou shledat jako užitečné použít tyto grafy k identifikaci změn v chování při výdajích. Balíček obsahu umožňuje nákupním manažerům a manažerům, kteří jsou zodpovědní za rozpočty, analyzovat nákupní výdaje následujícími způsoby:

-   Nákup k datu v daném roce (podle skupiny dodavatelů a jednotlivých dodavatelů, kategorie zásobování a jednotlivých produktů a umístění dodavatele)
-   Rok přes rok nákupu změna (podle skupiny a zadávání zakázek kategorií dodavatele)

## <a name="accessing-the-content-pack"></a>Přístup k balíčku obsahu
Balíček obsahu analýzy je publikován jako implementační aktivum v Microsoft Dynamics Lifecycle Services (LCS) a je přístupný z Microsoft Dynamics 365 for Operations. Další informace o přístupu k otevřeným sestavám Power BI, viz [Obsahu Power BI od společnosti Microsoft a partnerů v LCS](power-bi-content-microsoft-partners.md).
Poznámka: Předpokladem pro obsah Power BI je KB4011327. Po přihlášení ke službě Lifecycle Services můžete přejít k článku znalostní báze zde: https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.

## <a name="metrics-that-are-included-in-the-content-pack"></a>Metriky, které jsou součástí balíčku obsahu
Balíček obsahu analýzy investic do nákupu obsahuje sestavu, která obsahuje sadu metrik. Tyto metriky jsou zobrazována jako grafy, dlaždice a tabulky. Následující tabulka poskytuje přehled vizualizací v balíčku obsahu.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Stránka sestavy</th>
<th>Grafy</th>
<th>Dlaždice</th>
</tr>
</thead>
<tbody>
<tr class="odd">
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
<tr class="even">
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
<tr class="odd">
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
<tr class="even">
<td>Nákup podle místa dodavatele</td>
<td><ul>
<li>Nákup podle města</li>
<li>Meziroční růst nákupů v %</li>
<li>Nákup podle země</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td>Analýza výdajů při nákupu podle času</td>
<td><ul>
<li>Aktální rok nákupu podle měsíců / den (spojnicový graf)</li>
<li>Nákup za aktuální a předchozí rok (řádkový a sloupcový graf)</li>
</ul></td>
<td></td>
</tr>
<tr class="even">
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
Data Dynamics 365 for Operations se používají pro sestavu balíčku obsahu investic do nákupu. Tato data jsou reprezentována jako měrné systémy agregace, které jsou rozfázovány v úložišti entit, což je databáze Microsoft SQL optimalizována pro analýzy. Další informace o úložišti Entity naleznete v příspěvku v blogu [Integrace Power BI s úložištěm entit v aplikaci Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Souhrnná opatření v tomto balíčku obsahu jsou podmnožinou celkových opatření, která byla k dispozici v nákupní datové krychli v aplikaci Microsoft Dynamics AX 2012 a AX 2012 R3. Příprava fází agregovaných opatření v úložišti Entity vyžaduje, aby bylo možné je nasadit. Další informace získáte v postupu nastavování agregovaných opatření v úložišti entity v příspěvku v blogu [Integrace Power BI s úložištěm entit v aplikaci Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Následující klíčová agregovaná opatření jsou k dispozici přímo z entity řádky faktury a slouží jako základ balíčku obsahu.

| Celek        | Klíčová opatření agregace | Zdroj dat pro aplikaci Dynamics 365 for Operations | Pole              | popis                           |
|---------------|----------------------------|---------------------------------------------|--------------------|---------------------------------------|
| Řádky faktury | Nákup                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Částka v zúčtovací měně |

V následující tabulce jsou uvedena klíčová opatření, která jsou vypočtena v balíčku obsahu z entity řádky faktury.

| Měřítko               | Výpočet                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Aktuální rok nákupu | Aktuální rok nákupu = SUM (Řádky faktury\[Nákup\])                                            |
| Minulý nákupní rok    | Minulý nákupní rok = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\])) |
| Meziroční růst nákupů   | Meziroční růst nákup = \[Aktuální nákupní rok\] – \[Minulý nákupní rok\]                            |

Následující klíčové dimenze v balíčku obsahu se používají jako filtry k rozdělení agregovaných opatření, aby bylo možné dosažení většího rozlišení a poskytnutí hlubších analytických poznatků.

| Celek                 | Příklady atributů                                |
|------------------------|-------------------------------------------------------|
| Dodavatelé                | Skupiny dodavatelů, země nebo oblast dodavatele nebo název dodavatele |
| Produkty               | Číslo produktu, název produktu, název skupiny zboží        |
| Kategorie zásobování | Kategorie zásobování, názvy kategorií zásobování      |
| Právnické osoby         | Jméno právnické osoby                                     |
| Data                  | Data, Posun o rok                                    |

Ve výchozím nastavení balíček obsahu zobrazuje data pro aktuální kalendářní rok. Můžete však změnit filtr dat v části filtrů sestavy. Můžete také změnit filtr společnosti.

## <a name="additional-resources"></a>Další prostředky
Zde uvádíme některé užitečné odkazy související s entitami a vytvářením obsahu v aplikaci Power BI:

-   [Datové entity](..\data-entities\data-entities.md)
-   [Vytvoření organizačního balíčku obsahu](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Modelování dat pomocí aplikace Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Přidání dlaždic Power BI do pracovních prostorů](configure-power-bi-integration.md)





