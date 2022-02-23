---
title: Omezení výrazu a omezení tabulky v modelech konfigurace produktu
description: Toto téma popisuje použití omezení výrazu a omezení tabulky. Omezení řídí hodnoty atributů, které jsou k dispozici při konfiguraci produktů pro prodejní nabídku, nákupní objednávku nebo výrobní zakázku. Můžete použít omezení výrazu nebo omezení tabulky v závislosti na tom, jak chcete vytvářet omezení.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be9d9ae48d21db077928ba7bd5615fea47ea5181
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424011"
---
# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a>Omezení výrazu a omezení tabulky v modelech konfigurace produktu

[!include [banner](../includes/banner.md)]

Toto téma popisuje použití omezení výrazu a omezení tabulky. Omezení řídí hodnoty atributů, které jsou k dispozici při konfiguraci produktů pro prodejní nabídku, nákupní objednávku nebo výrobní zakázku. Můžete použít omezení výrazu nebo omezení tabulky v závislosti na tom, jak chcete vytvářet omezení. 

Omezení slouží k řízení hodnot atributů, které můžete vybrat při konfiguraci produktů pro prodejní nabídku, nákupní objednávku nebo výrobní zakázku. Můžete použít omezení výrazu nebo omezení tabulky v závislosti na tom, jak chcete vytvářet omezení.

## <a name="what-are-expression-constraints"></a>Co jsou omezení výrazu?
Omezení výrazu se vyznačují výrazem, který používá aritmetické a logické operátory a funkce. Omezení výrazu zapisuje pro určitou komponentu v modelu konfigurace produktu. Nelze ji znovu použít nebo sdílet s jinou součástí. Omezení výrazů pro komponentu se však může odkazovat na atributy dílčích komponent dané komponenty.

## <a name="what-are-table-constraints"></a>Co jsou omezení tabulky?
Omezení tabulky jsou seznam kombinací hodnoty, které jsou povoleny pro atributy při konfiguraci produktu. Definice omezení tabulky lze používat genericky. Při vytváření omezení tabulky pro komponentu v modelu konfigurace produktu je třeba vybrat definici omezení tabulky. Chcete-li vytvořit kombinace, které jsou povoleny, přidáváte atributy specifických typů ke komponentám. Každý typ atributu má konkrétní hodnotu.

### <a name="example-of-a-table-constraint"></a>Příklad omezení tabulky

Tento příklad ukazuje, jak můžete omezit konfiguraci reproduktoru na konkrétní povrchové úpravy skříně a přední kryty. První tabulka obsahuje povrchové úpravy skříně a přední kryty, které jsou obecně dostupné pro konfiguraci. Hodnoty jsou definovány pro typy atributů **Povrch skříňky** a **Přední mřížka**.

| Typ atributu | Hodnoty                      |
|----------------|-----------------------------|
| Povrch skříňky | Černá, dub, palisandr, bílá |
| Přední mřížka    | Černá, kov, bílá         |

Následující tabulka zobrazuje kombinace, které jsou definovány omezením tabulky **Barva a povrch**. Pomocí tohoto omezení tabulky lze konfigurovat reproduktor, který má dubový povrch a černou mřížku, palisandrový povrch a bílou mřížku a tak dále.

| Dokončit         | Mřížka                       |
|----------------|-----------------------------|
| Dub            | Černá                       |
| Palisandr       | Bílá                       |
| Bílá          | Černá                       |
| Bílá          | Bílá                       |
| Černá          | Černá                       |
| Černá          | Kov                       | 

Můžete vytvořit omezení tabulek definovaná uživatelem nebo systémem. Další informace naleznete v tématu [Omezení tabulek definovaná uživatelem nebo systémem](system-defined-user-defined-table-constraints.md).

## <a name="what-syntax-should-be-used-to-write-constraints"></a>Jaká syntax se používá pro řešení omezení psaní?
Když píšete omezení, musíte použít syntaxi jazyka OML (Optimization Modeling Language). Systém používá k řešení omezení produkt Microsoft Solver Foundation.

## <a name="should-i-use-table-constraints-or-expression-constraints"></a>Mám použít omezení tabulky nebo omezení výrazu?
Můžete použít omezení výrazu nebo omezení tabulky v závislosti na tom, jak chcete vytvářet omezení. Omezení tabulky vytváříte jako matici, zatímco omezení výrazu je jednotlivý výraz. Při konfiguraci produktu nezáleží na omezení, jaký druh omezení se použije. V následujícím příkladu je znázorněn rozdíl v těchto dvou metodách.  

Při konfiguraci produktu pomocí následujícího nastavení omezení jsou povoleny tyto kombinace:

-   Černá barva produktu a velikost 30 nebo 50
-   Červená barva produktu a velikost 20

### <a name="table-constraint-setup"></a>Nastavení omezení tabulky

| Barva | Velikost |
|-------|------|
| Černá | 30   |
| Černá | 50   |
| Červená   | 20   |

### <a name="expression-constraint-setup"></a>Nastavení omezení výrazu

(Barva == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a>Mám používat operátory nebo infixový zápis při psaní omezení výrazu?
Můžete napsat omezení výrazu buď pomocí dostupných prefixových operátorů, nebo pomocí infixového zápisu. U operátorů **Min**, **Max** a **Abs** nelze použít infixový zápis. Tyto operátory jsou k dispozici jako standardní operátory ve většině programovacích jazyků.

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a>Které operátory a infixový zápis můžu používat při psaní omezení výrazu?
V následujících tabulkách jsou uvedeny operátory a infixový zápis, které lze použít při zápisu omezení výrazu pro komponentu v modelu konfigurace produktu. V příkladech v první tabulce můžete vidět způsob zápisu výrazu pomocí infixového zápisu nebo operátorů.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Operátor</th>
<th>Popis</th>
<th>Syntaxe</th>
<th>Příklad</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Implikace</td>
<td>To platí v případě, že první podmínka není splněna, druhá podmínka je pravda, nebo obojí.</td>
<td>Implies[a, b], infix: a -: b</td>
<td><ul>
<li><strong>Operátor:</strong> Implies[x != 0, y &gt;= 0]</li>
<li><strong>Infixový zápis:</strong> x != 0 -: y &gt;= 0</li>
</ul></td>
</tr>
<tr class="even">
<td>A</td>
<td>To platí pouze v případě, že jsou splněny všechny podmínky. Pokud je počet podmínek 0 (nula), výsledkem je <strong>pravda</strong>.</td>
<td>And[args], infix: a &amp; b &amp; ... &amp; z</td>
<td><ul>
<li><strong>Operátor:</strong> And[x == 2, y &lt;= 2]</li>
<li><strong>Infixový zápis:</strong> x == 2 &amp; y &lt;= 2</li>
</ul></td>
</tr>
<tr class="odd">
<td>nebo</td>
<td>To platí při splnění libovolné podmínky. Pokud je počet podmínek 0 (nula), výsledkem je <strong>nepravda</strong>.</td>
<td>Or[args], infix: a | b | ... | z</td>
<td><ul>
<li><strong>Operátor:</strong> Or[x == 2, y &lt;= 2]</li>
<li><strong>Infixový zápis:</strong> x == 2 | y &lt;= 2</li>
</ul></td>
</tr>
<tr class="even">
<td>Plus</td>
<td>Sečte podmínky. Pokud je počet podmínek 0 (nula), výsledkem je <strong>0</strong>.</td>
<td>Plus[args], infix: a + b + ... + z</td>
<td><ul>
<li><strong>Operátor:</strong> Plus[x, y, 2] == z</li>
<li><strong>Infixový zápis:</strong> x + y + 2 == z</li>
</ul></td>
</tr>
<tr class="odd">
<td>Minus</td>
<td>Argumenty se negují. Musí mít právě jednu podmínku.</td>
<td>Minus[expr], infix: -expr</td>
<td><ul>
<li><strong>Operátor:</strong> Minus[x] == y</li>
<li><strong>Infixový zápis:</strong> -x == y</li>
</ul></td>
</tr>
<tr class="even">
<td>Abs</td>
<td>Vezme absolutní hodnotu podmínky. Musí mít právě jednu podmínku.</td>
<td>Abs[expr]</td>
<td><strong>Operátor:</strong> Abs[x]</td>
</tr>
<tr class="odd">
<td>Časy</td>
<td>Vezme násobek podmínek. Pokud je počet podmínek 0 (nula), výsledkem je <strong>1</strong>.</td>
<td>Times[args], infix: a * b * ... * z</td>
<td><ul>
<li><strong>Operátor:</strong> Times[x, y, 2] == z</li>
<li><strong>Infixový zápis:</strong> x * y * 2 == z</li>
</ul></td>
</tr>
<tr class="even">
<td>Výkon</td>
<td>Vezme mocninu. Umocňuje se zprava doleva. (Jinými slovy je zprava asociativní.) Proto je <strong>Power[a, b, c]</strong> ekvivalentní k <strong>Power[a, Power[b, c]]</strong>. <strong>Výkon</strong> lze použít pouze s exponentem jako kladnou konstantou.</td>
<td>Power[args], infix: a ^ b ^ ... ^ z</td>
<td><ul>
<li><strong>Operátor:</strong> Power[x, 2] == y</li>
<li><strong>Infixový zápis:</strong> x ^ 2 == y</li>
</ul></td>
</tr>
<tr class="odd">
<td>Maximum</td>
<td>Výsledkem je největší podmínka. Pokud je počet podmínek 0 (nula), výsledkem je <strong>nekonečno</strong>.</td>
<td>Max[args]</td>
<td><strong>Operátor:</strong> Max[x, y, 2] == z</td>
</tr>
<tr class="even">
<td>Minimum</td>
<td>Výsledkem je nejmenší podmínka. Pokud je počet podmínek 0 (nula), výsledkem je <strong>nekonečno</strong>.</td>
<td>Min[args]</td>
<td><strong>Operátor:</strong> Min[x, y, 2] == z</td>
</tr>
<tr class="odd">
<td>Ne</td>
<td>Výsledkem logický opak podmínky. Musí mít právě jednu podmínku.</td>
<td>Not[expr], infix: !expr</td>
<td><ul>
<li><strong>Operátor:</strong> Not[x] &amp; Not[y == 3]</li>
<li><strong>Infixový zápis:</strong> !x!(y == 3)</li>
</ul></td>
</tr>
</tbody>
</table>

V následující tabulce jsou uvedeny příklady, jak zapsat infixový zápis.


|  Infixový zápis   |                                          popis                                          |
|-------------------|-----------------------------------------------------------------------------------------------|
|     x + y + z     |                                           Dodatek                                            |
|    x \* y \* z    |                                        Násobení                                         |
|       x - y       | Binární odčítání je převedeno stejně jako binární součet, kde je negovaná druhá podmínka. |
|     x ^ y ^ z     |                          Umocňování s pravou asociativitou                          |
|        !x         |                                          Logické ne                                          |
|      x -: y       |                                      Logická implikace                                      |
|         x         |                                               y                                               |
|     x & y & z     |                                          Logické a                                          |
|    x == y == z    |                                           Rovnost                                            |
|    x != y != z    |                                           Různé                                            |
|  x &lt; y &lt; z  |                                           Je menší než                                           |
|  x &gt; y &gt; z  |                                         Je větší než                                          |
| x &lt;= y &lt;= z |                                     Menší než nebo rovno                                     |
| x &gt;= y &gt;= z |                                   Větší než nebo rovno                                    |
|        (x)        |                           Závorky ruší výchozí priority.                            |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a>Proč nejsou má omezení výrazu vyhodnocena správně?
Rezervovaná slovo nelze použít jako řešitelské názvy atributů, komponentů nebo dílčích komponentů v modelu konfigurace produktu.Následující seznam obsahuje rezervovaná klíčová slova, která nelze použít:

-   Horní mez
-   Prvek
-   Rovno
-   Podlaží
-   Jestliže
-   Menší
-   Větší
-   Implikace
-   Protokol
-   Maximum
-   Minimum
-   Záporný
-   Kladný
-   Výkon
-   Časy
-   Úsek
-   Model
-   Rozhodnutí
-   Cíl


<a name="additional-resources"></a>Další zdroje
--------

[Vytvoření omezení výrazu](tasks/add-expression-constraint-product-configuration-model.md)

[Přidání výpočtu do modelu konfigurace produktu](tasks/add-calculation-product-configuration-model.md)



