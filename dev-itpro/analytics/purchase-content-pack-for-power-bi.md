---
title: "Analýza obsahu Power BI výdajů na nákup"
description: "Toto téma popisuje, co je zahrnuta v nákupu věnovat analýze obsahu pack pro Microsoft Power BI. Popisuje, jak přístup k sestavám, které jsou součástí obsahu pack a obsahuje informace o datovém modelu a entit, které se používají k vytváření obsahu pack."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-12-30 09 - 40 - 51
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 8cb928cbf1316e63a8c7de833587168cd36a455c
ms.lasthandoff: 03/29/2017


---

# <a name="purchase-spend-analysis-power-bi-content"></a>Analýza obsahu Power BI výdajů na nákup

Toto téma popisuje, co je zahrnuta v nákupu věnovat analýze obsahu pack pro Microsoft Power BI. Popisuje, jak přístup k sestavám, které jsou součástí obsahu pack a obsahuje informace o datovém modelu a entit, které se používají k vytváření obsahu pack.

<a name="overview"></a>Přehled
--------

Nákup strávit analýzy obsahu pack pro Microsoft Power BI byla vytvořena pro nákup, manažeři a vedoucí, kteří jsou zodpovědní za rozpočty. Je navržen tak, aby jejich kontrola výdajů na nákup. Nákupní transakční data z Microsoft Dynamics 365 používá pro operace a poskytuje agregované zobrazení nákupní celopodnikové údaje i rozdělení nákupní výdaje podle dodavatelů a produktů. Zprávy zvýraznit změny v nákupní výdaje v průběhu času. Proto jsou slouží správcům oznámení o pozitivní a negativní vývoj výdajů u jednotlivých dodavatelů a výrobků. Grafy zobrazují nákupní výdaje pro zásobování různých kategorií a skupin dodavatelů. Kategorie a regionálními manažery může být užitečné k identifikaci změn v chování výdaje pomocí těchto grafů. Obsahu pack nyní nákupní manažeři a vedoucí, kteří jsou zodpovědní za rozpočty analyzovat nákupní výdaje následujícími způsoby:

-   -Na rok nákupu (ze skupiny dodavatelů a jednotlivým dodavatelům, kategorie zásobování a jednotlivé produkty a umístění dodavatele)
-   Rok přes rok nákupu změna (podle skupiny a zadávání zakázek kategorií dodavatele)

## <a name="accessing-the-content-pack"></a>Přístup k obsahu pack
Nákupu věnovat obsahu pack je publikován jako aktivum implementace v Microsoft Dynamics Lifecycle Services (LCS) a je přístupný z 365 Microsoft Dynamics pro operace analýzy. Další informace o přístupu a otevřených sestav Power BI, viz [obsahu Power BI od společnosti Microsoft a partnerů LCS](power-bi-content-microsoft-partners.md).

## <a name="metrics-that-are-included-in-the-content-pack"></a>Metriky, které jsou součástí obsahu pack
Nákupu věnovat rozboru obsahu pack obsahuje sestavu, která obsahuje sadu metriky. Tyto metriky jsou zobrazována jako grafy, kameny a tabulky. Následující tabulka obsahuje přehled vizualizace v obsahu pack.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Stránky sestavy</th>
<th>Grafy</th>
<th>Vedle sebe</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Nákup od dodavatele</td>
<td><ul>
<li>Prvních 10 dodavatelů podle nákupu (skládaný sloupcový graf)</li>
<li>Celkový nákup od dodavatele skupiny / země / name (výsečový graf)</li>
<li>Nákupy podle dodavatele skupiny / země / name (sloupcový graf)</li>
<li>Průměrná nákupní dodavatelem skupiny / země / name (sloupcový graf)</li>
</ul></td>
<td><ul>
<li>Celkový nákup</li>
<li>Po letech růstu nákupu</li>
<li>Celkový počet dodavatelů</li>
<li>Celkový počet aktivních dodavatelů</li>
</ul></td>
</tr>
<tr class="even">
<td>Nákup produktu</td>
<td><ul>
<li>Nákup podle kategorie zásobování / product name (sloupcový graf)</li>
<li>Celkový nákup podle kategorie zásobování / product name (výsečový graf)</li>
<li>Nejlepších 10 produktů nákupem (skládaný sloupcový graf)</li>
</ul></td>
<td><ul>
<li>Celkový počet produktů</li>
<li>Celkový počet aktivních produktů procento celkový počet produktů</li>
<li>Počet produktů účtování nákupu 80 %</li>
</ul></td>
</tr>
<tr class="odd">
<td>Nákup v období *</td>
<td><ul>
<li>Nákup za měsíc / den (sloupcový graf)</li>
<li>Kumulativní nákupní odchylka po letech (graf vodopádu)</li>
<li>Po letech růstu celkového nákupu (sloupcový graf)</li>
<li>Prohlášení o zadávání veřejných zakázek (matice)</li>
</ul></td>
<td><ul>
<li>Po letech růstu nákupu</li>
<li>% Nárůst nákupu po letech</li>
</ul></td>
</tr>
<tr class="even">
<td>Nákup podle umístění dodavatele</td>
<td><ul>
<li>Nákup podle města</li>
<li>Nákup po letech růstu %</li>
<li>Nákup podle země</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td>Analýza nákupních výdajů podle času</td>
<td><ul>
<li>Nákup běžného roku za měsíc / den (spojnicový graf)</li>
<li>Nákupní aktuálního a předchozího roku (řádek a sloupec grafu)</li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td>Analýza podle dodavatele nákupní výdajů</td>
<td><ul>
<li>TOP 10 % nákupu dodavatele nákupní (nálevky)</li>
<li>Prvních 10 dodavatelů s zvýšení výdajů po letech</li>
<li>Prvních 10 dodavatelů se po letech poklesu výdajů</li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

\*Nákup tohoto a minulého roku a růst podle kategorie zásobování

## <a name="data-model-and-entities"></a>Datový model a entity
Dynamics 365 pro operace data slouží pro sestavu v nákupu věnovat obsahu analytické nástroje. Tato data jsou reprezentována jako agregační hodnoty, které jsou připraveny v úložišti Entity, což je databáze Microsoft SQL, která je optimalizována pro analytics. Další informace o úložišti Entity naleznete [BI napájení integrace s úložištěm entit v aplikaci Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) blogu. Souhrnné měření v tomto obsahu pack jsou podmnožiny celkové měření, která byla k dispozici v nákupní datové krychle v aplikaci Microsoft Dynamics AX 2012 a Microsoft Dynamics 365 pro operace 2012 R3. Příprava agregovaných měr datové krychli v úložišti Entity, musíte je provést nasaditelné. Další informace naleznete v tématu agregační měření v úložišti Entity v pracovní postup [BI napájení integrace s úložištěm entit v aplikaci Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) blogu. Následující klíče souhrnné měření jsou k dispozici přímo z entity řádky faktury a slouží jako základ obsahu pack.

| Celek        | Klíče agregovaných měr | Zdroj dat pro Dynamics 365 pro operace | Pole              | popis                           |
|---------------|----------------------------|---------------------------------------------|--------------------|---------------------------------------|
| Řádky faktury | Nákup                   | VendInvoiceTrans.                            | SUM(LineAmountMST) | Částka v zúčtovací měně |

Následující tabulce jsou uvedeny klíče měření, které jsou vypočteny v obsahu pack z entity řádky faktury.

| Měřítko               | Výpočet                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Nákup běžného roku | Nákupní aktuální rok = SUMA (řádky faktur\[nákupní\])                                            |
| Nákupní Loni    | Nákupní Loni = výpočet (součet (řádky faktur\[nákupní\]), SAMEPERIODLASTYEAR (data\[datum\])) |
| Po letech růstu nákupu   | Po letech koupit růstu = \[nákup běžného roku\] – \[koupit Loni\]                            |

Následující klíče dimenze v obsahu pack slouží jako filtry při řezu agregovaných měr, takže můžete dosáhnout větší univerzálnost a hlubší analytické poznatky.

| Celek                 | Příklady atributů                                |
|------------------------|-------------------------------------------------------|
| Dodavatelé                | Skupiny dodavatelů, dodavatele, země nebo oblasti název dodavatele |
| Produkty               | Číslo produktu, název produktu, název skupiny zboží        |
| Kategorie zásobování | Kategorie zásobování, názvy kategorií zásobování      |
| Právnické osoby         | Jméno právnické osoby                                     |
| Data                  | Roční posun data                                    |

Ve výchozím nastavení obsahu pack zobrazuje data pro aktuální kalendářní rok. Můžete však změnit filtr data v části filtry sestavy. Můžete také změnit filtr společnosti.

## <a name="additional-resources"></a>Další prostředky
Zde uvádíme některé užitečné odkazy související s entitami a vytvářením obsahu v aplikaci Power BI:

-   [Datové entity](..\data-entities\data-entities.md)
-   [Vytvoření organizačního balíčku obsahu](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Modelování dat pomocí aplikace Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Přidání dlaždic Power BI do pracovních prostorů](configure-power-bi-integration.md)



