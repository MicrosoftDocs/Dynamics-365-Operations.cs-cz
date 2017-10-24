---
title: "Syntax pokročilého filtrování a dotazů"
description: "Tento článek popisuje možnosti filtrování a dotazů, které jsou k dispozici při použití operátoru \"shody\" v dialogovém okně Rozšířený filtr či řazení."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 616366009ce7bf7135704e980becc331617cf5af
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="advanced-filtering-and-query-syntax"></a>Syntax pokročilého filtrování a dotazů

[!include[banner](../includes/banner.md)]


Tento článek popisuje možnosti filtrování a dotazů, které jsou k dispozici při použití operátoru "shody" v dialogovém okně Rozšířený filtr či řazení.

<a name="advanced-query-syntax"></a>Syntax pokročilých dotazů
---------------------

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Syntaxe</th>
<th>Popis znaku</th>
<th>popis</th>
<th>Příklad</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>hodnota</em></td>
<td>Rovno zadané hodnotě</td>
<td>Zadejte hodnotu, kterou chcete vyhledat.</td>
<td><strong>Smith</strong> vyhledá &quot;Smith&quot;.</td>
</tr>
<tr class="even">
<td>!<em>hodnota</em> (vykřičník)</td>
<td>Není rovno zadané hodnotě</td>
<td>Před hodnotu, kterou chcete vyloučit, zadejte vykřičník.</td>
<td><strong>!Smith</strong> vyhledá všechny hodnoty kromě hodnoty &quot;Smith&quot;.</td>
</tr>
<tr class="odd">
<td><em>hodnota od</em>..<em>hodnota do</em> (dvojí období)</td>
<td>Mezi dvěma zadanými hodnotami oddělenými dvěma tečkami</td>
<td>Zadejte hodnotu Od, pak dvě tečky a nakonec hodnotu Do.</td>
<td><strong>1..10</strong> vyhledá všechny hodnoty od 1 do 10. V poli řetězce však zadání hodnot <strong>A..C</strong> vyhledá všechny hodnoty, které začínají písmeny &quot;A&quot; a &quot;B&quot; a hodnoty, které se přesně rovnají &quot;C&quot;. Tento dotaz nebude hledat například &quot;Ca&quot;. Chcete-li vyhledat všechny hodnoty od &quot;A*&quot; do &quot;C*&quot;, <strong>A..D</strong>.</td>
</tr>
<tr class="even">
<td>..<em>hodnota</em> (dvojí období)</td>
<td>Méně nebo rovno zadané hodnotě</td>
<td>Zadejte dvě tečky a pak hodnotu.</td>
<td><strong>..1000</strong> vyhledá libovolné číslo menší nebo rovné hodnotě 1000: například &quot;100&quot;, &quot;999.95&quot;, and &quot;1,000&quot;.</td>
</tr>
<tr class="odd">
<td><em>hodnota</em>.. (dvě tečky)</td>
<td>Větší nebo rovno zadané hodnotě</td>
<td>Zadejte hodnotu a poté dvě tečky.</td>
<td><strong>1000..</strong> vyhledá libovolné číslo větší nebo rovné hodnotě 1000: například &quot;1,000&quot;, &quot;1,000.01&quot;, and &quot;1,000,000&quot;.</td>
</tr>
<tr class="even">
<td>&gt;<em>hodnota</em> (znaménko větší než)</td>
<td>Větší než zadaná hodnota</td>
<td>Zadejte znaménko „větší než“ (<strong>&gt;</strong>) a pak hodnotu.</td>
<td><strong>&gt;1000</strong> vyhledá libovolné číslo větší než hodnota 1000: &quot;1000.01&quot;, &quot;20,000&quot;, and &quot;1,000,000&quot;.</td>
</tr>
<tr class="odd">
<td>&lt;<em>hodnota</em> (znaménko menší než)</td>
<td>Menší než zadaná hodnota</td>
<td>Zadejte znaménko „menší než“ (<strong>&lt;</strong>) a pak hodnotu.</td>
<td><strong>&lt;1000</strong> vyhledá libovolné číslo menší než hodnota 1000: například &quot;999.99&quot;, &quot;1&quot;, and &quot;-200&quot;.</td>
</tr>
<tr class="even">
<td><em>hodnota</em>* (hvězdička)</td>
<td>Začínající od zadané hodnoty</td>
<td>Zadejte počáteční hodnotu a pak hvězdičku (<strong>*</strong>).</td>
<td><strong>S*</strong>nalezne libovolný řetězec začínající na &quot;S&quot;, jako například &quot;Stockholm&quot;, &quot;Sydney&quot;, a &quot;San Francisco&quot;.</td>
</tr>
<tr class="odd">
<td>*<em>hodnota</em> (hvězdička)</td>
<td>Končí zadanou hodnotou</td>
<td>Zadejte hvězdičku a pak konečnou hodnotu.</td>
<td><strong>*east</strong>nalezne řetězec končící na &quot;východ&quot;, jako například &quot;severovýchod&quot; nebo &quot;jihovýchod&quot;.</td>
</tr>
<tr class="even">
<td>*<em>hodnota</em>* (hvězdička)</td>
<td>Obsahující zadanou hodnotu</td>
<td>Zadejte hvězdičku, pak hodnotu, a nakonec opět hvězdičku.</td>
<td><strong>*th*</strong> nalezne libovolný řetězec obsahující &quot;ch&quot;, jako například &quot;severovýchod&quot; nebo &quot;jihovýchod&quot;.</td>
</tr>
<tr class="odd">
<td>? (otazník)</td>
<td>Obsahující jeden nebo více neznámých znaků</td>
<td>V pozici neznámého znaku v hodnotě můžete zadat otazník.</td>
<td><strong>Sm?th</strong> nalezne &quot;Smith&quot; a &quot;Smyth&quot;.</td>
</tr>
<tr class="even">
<td><em>hodnota</em>,<em>hodnota</em> (čárka)</td>
<td>Shoduje se s hodnotami oddělenými čárkou</td>
<td>Zadejte veškerá vaše kritéria a oddělte je čárkami.</td>
<td><strong>A, D, F, G</strong> vyhledá přesně &quot;A&quot;, &quot;D&quot;, &quot;F&quot; a &quot;G&quot;. <strong>10, 20, 30, 100</strong> vyhledá přesně &quot;10, 20, 30, 100&quot;.</td>
</tr>
<tr class="odd">
<td>(<span class="code">příkaz SQL</span>) (příkaz SQL v uvozovkách)</td>
<td>Nalezení definovaného dotazu</td>
<td>Zadejte dotaz ve formě příkazu SQL v uvozovkách.</td>
<td><strong><span class="code">(datový zdroj.Název pole != &quot;A&quot;)</span></strong></td>
</tr>
<tr class="even">
<td>bil.</td>
<td>Dnešní datum</td>
<td>Zadejte <strong>T</strong>.</td>
<td><strong>T</strong> odpovídá dnešnímu datu.</td>
</tr>
<tr class="odd">
<td>(methodName(parameters)) (metoda <strong>SysQueryRangeUtil</strong> v uvozovkách)</td>
<td>Párování hodnoty nebo rozsahu hodnot zadaných za pomoci parametrů metody <strong>SysQueryRangeUtil</strong></td>
<td>Zadejte parametry metody <strong>SysQueryRangeUtil</strong> Párování pro určení hodnoty nebo rozsahu hodnot.</td>
<td><ol>
<li>Klikněte na <strong>Pohledávky</strong> &gt; <strong>Faktury</strong> &gt; <strong>Otevřené faktury odběratele</strong>.</li>
<li>Stisknutím kombinace kláves Ctrl + Shift + F3 otevřete stránku <strong>Dotaz</strong>.</li>
<li>Na kartě <strong>Rozsah</strong> klepněte na možnost <strong>Přidat</strong>.</li>
<li>V poli <strong>Tabulka</strong> vyberte <strong>Otevřít transakce odběratelů</strong>.</li>
<li>V poli <strong>Pole</strong> vyberte <strong>Datum splatnosti</strong>.</li>
<li>V poli <strong>Kritéria</strong> zadejte <strong>(yearRange(-2,0))</strong>.</li>
<li>Klepněte na tlačítko <strong>OK</strong>. Stránka seznamu se aktualizuje a bude obsahovat seznam faktur, které odpovídají zadaným kritériím. V tomto případě budou uvedeny faktury, které byly splatné v předchozích dvou letech.</li>
</ol>
Další podrobnosti o metodách pro data <strong>SysQueryRangeUtil</strong> a několik příkladů naleznete v tabulce v další části.</td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a>Upřesnění datových dotazů, které používají metody SysQueryRangeUtil
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Metoda</th>
<th>Popis</th>
<th>Příklad</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Den (_relativeDays=0)</td>
<td>Vyhledání data vzhledem k datu relace. Kladné hodnoty naznačují budoucí data a záporné hodnoty dřívější data.</td>
<td><ul>
<li><strong>Zítra</strong> – zadejte <strong>(Day(1))</strong>.</li>
<li><strong>Dnes</strong> – zadejte <strong>(Day(0))</strong>.</li>
<li><strong>Včera</strong> – zadejte <strong>(Day(-1))</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</td>
<td>Vyhledání rozsahu vzhledem k datu relace. Kladné hodnoty naznačují budoucí data a záporné hodnoty dřívější data.</td>
<td><ul>
<li><strong>Posledních 30 dnů</strong> – zadejte <strong>(DayRange(-30,0))</strong>.</li>
<li><strong>Posledních 30 dnů a budoucích 30 dnů</strong> – zadejte <strong>(DayRange(-30,30))</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</td>
<td>Vyhledání všech dat po určeném relativním datu.</td>
<td><ul>
<li><strong>Více než 30 dnů ode dneška</strong> – zadejte <strong>(GreaterThanDate(30))</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>GreaterThanUtcNow ()</td>
<td>Vyhledání všech záznamů data/času po aktuálním času.</td>
<td><ul>
<li><strong>Všechna budoucí data a časy</strong> – zadejte <strong>(GreaterThanUtcNow())</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</td>
<td>Vyhledání všech dat před určeném relativním datem.</td>
<td><ul>
<li><strong>Méně než sedm dní ode dneška</strong> – zadejte <strong>(LessThanDate(7))</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>LessThanUtcNow ()</td>
<td>Vyhledání všech záznamů data/času před aktuálním časem.</td>
<td><ul>
<li><strong>Všechna minulá data/časy</strong> – zadejte <strong>(LessThanUtcNow())</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>MonthRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Vyhledání rozsahu dat na základě měsíců vzhledem k aktuálnímu měsíci.</td>
<td><ul>
<li><strong>Předchozí dva měsíce</strong> – zadejte <strong>(MonthRange(-2,0))</strong>.</li>
<li><strong>Následující tři měsíce</strong> – zadejte <strong>(MonthRange(0,3))</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>YearRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Vyhledání rozsahu dat na základě roků vzhledem k aktuálnímu roku.</td>
<td><ul>
<li><strong>Příští rok</strong> – zadejte <strong>(YearRange(0, 1))</strong>.</li>
<li><strong>Předchozí rok</strong> – zadejte <strong>(YearRange(-1,0))</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>






