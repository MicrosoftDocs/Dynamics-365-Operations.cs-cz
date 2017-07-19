---
title: "Analýza obsahu Power BI výdajů na nákup"
description: "Toto téma popisuje, co je součástí obsahu analýzy nákupu a výdajů v Power BI. Popisuje, jak získat přístup k sestavám, které jsou obsaženy v obsahu, a uvádí informace o datovém modelu a entitách, které se používají k vytváření obsahu."
author: FrankDahl
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: daba17aed7e6cc475a16d6100c5c99ee747ca048
ms.contentlocale: cs-cz
ms.lasthandoff: 06/13/2017

---

# <a name="purchase-spend-analysis-power-bi-content"></a>Analýza obsahu Power BI výdajů na nákup

[!include[banner](../includes/banner.md)]

Toto téma popisuje, co je součástí obsahu analýzy **nákupu a výdajů** v Power BI. Vysvětluje přístup k sestavám Power BI a poskytuje informace o datovém modelu a entitách, které jsou použity k sestavení obsahu.

## <a name="overview"></a>Přehled

Obsah Power BI **Analýza nákupních výdajů** byl vytvořen na pomoc nákupním manažerům a vedoucím pracovníkům, kteří odpovídají za rozpočty, prohlížet nákupní výdaje. Manažeři mohou analyzovat nákupní výdaje následujícím způsobem:

-   Nákup k datu v daném roce (podle skupiny dodavatelů a jednotlivých dodavatelů, kategorie zásobování a jednotlivých produktů a umístění dodavatele)
-   Rok přes rok nákupu změna (podle skupiny a zadávání zakázek kategorií dodavatele)

Obsah používá nákupní transakční data a poskytuje agregované zobrazení nákupní celopodnikových údajů a rozpis nákupních výdajů podle dodavatelů a produktů. V sestavách jsou zvýrazněny změny nákupních výdajů v průběhu času. Proto lze sestavy používat k upozornění manažerů na pozitivní a negativní trendy výdajů u jednotlivých dodavatelů a výrobků. Grafy dále zobrazují nákupní výdaje pro zásobování různých kategorií a skupin dodavatelů. Proto manažeři pro kategorie a regionální manažeři mohou tyto grafy používat k identifikaci změn v chování při výdajích.

## <a name="accessing-the-power-bi-content"></a>Přístup k obsahu Power BI
Pokud používáte aktualizaci Microsoft Dynamics 365 for Finance and Operations, Enterprise edition z července 2017, obsah Power BI **Analýza nákupu a výdajů** se zobrazí na stránce **Analýza nákupu a výdajů** (**Nákup a zdroje** > **Dotazy a sestavy** > **Analýza výkonu nákupu** > **Analýza nákupu a investic**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metriky, které jsou součástí obsahu Power BI
Obsahu Power BI **Analýza nákupu a výdajů** obsahuje sestavu, která obsahuje sadu metrik. Tyto metriky jsou zobrazována jako grafy, dlaždice a tabulky. Následující tabulka poskytuje přehled vizualizací.

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

## <a name="extending-the-power-bi-content"></a>Rozšíření obsahu v Power BI
Pomocí balíčků obsahu, které jsou k dispozici ve službě Microsoft Dynamics Lifecycle Services (LCS) můžete poskytovat skvělou analýzu osobám, které nejsou přihlášeny k aplikaci Microsoft Dynamics 365. Tyto balíčky obsahu můžete upravit tak, aby zahrnovaly jiné sestavy nebo vizuály, a potom publikovat balíčky obsahu na svého klienta Power BI.com pro analýzu. 

Obsah Power BI **Analýza nákupu a výdajů** naleznete v knihovně sdíleného majetku ve službě LCS. Další informace o stažení obsahu a jeho implementaci ve vaší organizaci naleznete v tématu [Obsah Power BI v LCS od společnosti Microsoft a vašich partnerů](power-bi-content-microsoft-partners.md). Pokud se chcete podívat na ukázku, jak implementovat obsah Power BI, najdete informace v tématu [Obsah Power BI od společnosti Microsoft a partnerů ve službě Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) pro Office Mix.

Nezapomeňte si stáhnout obsah **Analýza nákupu a výdajů**, který se vztahuje k vámi používané verzi aplikace Dynamics 365.

> [!NOTE]
> Pokud používáte verzi Microsoft Dynamics 365 for Operations 1611, je předpokladem pro tento obsah Power BI článek znalostní báze KB 4011327. Po přihlášení ke službě LCS můžete přejít k článku znalostní báze zde: https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.

## <a name="data-model-and-entities"></a>Datový model a entity
Následující data se používají k naplnění stránek sestavy v obsahu **Analýza nákupu a výdajů** v Power BI. Tato data jsou vyjádřena jako agregační měření, která jsou rozfázována v úložišti entit. Úložiště entit je databáze Microsoft SQL Server, která je optimalizována pro analýzu. Další informace naleznete v tématu [Přehled integrace Power BI úložištěm entit](power-bi-integration-entity-store.md).

Souhrnná opatření v tomto obsahu jsou podmnožinou celkových opatření, která byla k dispozici v nákupní datové krychli v aplikaci Microsoft Dynamics AX 2012 a AX 2012 R3. Příprava fází agregovaných opatření v úložišti Entity vyžaduje, aby bylo možné je nasadit. Další informace získáte v postupu nastavování agregovaných opatření v úložišti entity v příspěvku v blogu [Přehled integrace Power BI s úložištěm entit](power-bi-integration-entity-store.md). Následující klíčová agregovaná opatření jsou k dispozici přímo z entity řádky faktury a slouží jako základ obsahu.

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

