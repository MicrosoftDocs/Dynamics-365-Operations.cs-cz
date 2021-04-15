---
title: Jazyk receptur v elektronickém výkaznictví
description: Toto téma obsahuje obecné informace o použití jazyka receptury v elektronickém výkaznictví (ER).
author: NickSelin
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2015405f3c7f89ba36f811ca125f3a73bc13c38
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753257"
---
# <a name="electronic-reporting-formula-language"></a>Jazyk receptur v elektronickém výkaznictví

[!include [banner](../includes/banner.md)]

Elektronické výkaznictví (ER) poskytuje výkonné možnosti transformace dat. Jazyk používaný k vyjádření potřebných manipulací s daty v [Návrháři vzorců ER](general-electronic-reporting-formula-designer.md) se podobá jazyku vzorců v aplikaci Microsoft Excel.

## <a name="basic-syntax"></a>Základní syntaxe

Výrazy elektronické výkaznictví mohou obsahovat jakékoli nebo všechny následující prvky:

- [Konstanty](#Constants)
- [Operátory](#Operators)
- [Odkazy](#References)
- [Cesty](#Paths)
- [Funkce](#Functions)

## <a name=""></a><a name="Constants">Konstanty</a>

Při návrhu výrazů lze použít text a numerické konstanty (hodnoty, které nejsou vypočteny). Například výraz `VALUE ("100") + 20` používá číselnou konstantu **20** a řetězcovou konstantu **"100"** a vrátí číselnou hodnotu **120**.

Návrhář receptur elektronického výkaznictví podporuje řídicí sekvence. Můžete tedy určit řetězec výrazu, se kterým má být zacházeno jinak. Výraz `"Leo Tolstoy ""War and Peace"" Volume 1"` například vrátí textový řetězec **Leo Tolstoy "War and Peace" Volume 1**.

## <a name=""></a><a name="Operators">Operátory</a>

Následující tabulka ukazuje aritmetické operátory, které lze používat k provádění základních matematických operací, například sčítání, odčítání, dělení a násobení.

| Operátor | Význam               | Příklad     |
|----------|-----------------------|-------------|
| +        | Dodatek              | `1+2`       |
| -        | Odečítání, negace | `5-2`, `-1` |
| \*       | Násobení        | `7\*8`      |
| /        | Divize              | `9/3`       |

Následující tabulka ukazuje operátory porovnávání, které jsou podporovány. Tyto operátory slouží k porovnání dvou hodnot.

| Operátor | Význam                  | Příklad      |
|----------|--------------------------|--------------|
| =        | Rovno                    | `X=Y`        |
| &gt;     | Je větší než             | `X>Y`        |
| &lt;     | Je menší než                | `X<Y`        |
| &gt;=    | Větší než nebo rovno | `X>=Y`       |
| &lt;=    | Menší než nebo rovno    | `X<=Y`       |
| &lt;&gt; | Není rovno             | `X<>Y`       |

Kromě toho můžete použít znak & jako operátor ke zřetězení textu. Tímto způsobem můžete spojit nebo zřetězit jeden nebo více řetězců do jednoho textu.

| Operátor | Význam     | Příklad                                               |
|----------|-------------|-------------------------------------------------------|
| &        | Sloučit | `"Nothing to print:" & " " & "no records found"`      |

### <a name="operator-precedence"></a>Priorita operátorů

Pořadí, v jakém jsou části složeného výrazu vyhodnoceny, je důležité. Například výsledek výrazu `1 + 4 / 2` se liší v závislosti na tom, zda se provádí nejprve sčítání nebo dělení. Pomocí závorek lze explicitně definovat způsob vyhodnocení výrazu. Chcete-li například uvést, že se sčítání musí provést jako první, můžete upravit předchozí výraz na `(1 + 4) / 2`. Pokud pořadí operací ve výrazu, není explicitně definováno, pořadí vychází z výchozí priority přiřazené k podporovaným operátorům. V následující tabulce je priorita, která je přiřazena ke každému operátoru. Operátory, které mají vyšší prioritu (například 7), jsou vyhodnoceny dříve než operátory s nižší prioritou (například 1).

| Priorita | Operátory      | Syntaxe                                                                  |
|------------|----------------|-------------------------------------------------------------------------|
| 7          | Seskupení       | ( … )                                                                   |
| 6          | Přístup členů  | … . …                                                                   |
| 5          | Volání funkce  | … ( … )                                                                 |
| 4          | Multiplikativní | … \* …<br>… / …                                                         |
| 3          | Přídavné       | … + …<br>… - …                                                          |
| 2          | Porovnání     | … &lt; …<br>… &lt;= …<br>… =&gt; …<br>… &gt; …<br>… = …<br>… &lt;&gt; … |
| 1          | Dělení     | … , …                                                                   |

Pokud výraz obsahuje několik po sobě jdoucích operátorů, které mají stejnou prioritu, vyhodnocují se tyto operátory zleva doprava. Například výraz `1 + 6 / 2 \* 3 > 5` vrátí hodnotu **pravda**. Doporučujeme vám pomocí závorek explicitně určit požadované pořadí operátorů ve výrazech, usnadní se tím čtení a správa výrazů.

## <a name=""></a><a name="References">Odkazy</a>

Všechny zdroje dat aktuální součásti elektronického výkaznictví, které jsou k dispozici během návrhu výrazu, lze použít jako pojmenované odkazy. Aktuální komponenta ER může být buď mapování modelu, nebo formát. Aktuální datový model elektronického výkaznictví například obsahuje zdroj dat **ReportingDate**, který vrací hodnotu datového typu *DateTime*. Abyste tuto hodnotu v generování dokumentu správně zformátovali, můžete odkazovat na zdroj dat ve výrazu, jako je `DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy")`.

Všechny znaky v názvu referenčního datového zdroje, které nepředstavují písmeno abecedy, musí předcházet jednoduchá uvozovka ('). Pokud název odkazujícího zdroje dat obsahuje alespoň jeden znak, který nepředstavuje písmeno abecedy, musí být název v jednoduchých uvozovkách. Těmito nealfabetickými symboly mohou být například interpunkční znaménka nebo jiné psané symboly. Několik příkladů:

- Datový zdroj **Dnešní datum a čas** je nutné odkazovat ve výrazu elektronického výkaznictví jako `'Today''s date & time'`.
- Na metodu **name()** zdroje dat **Odběratelé** musí být odkazováno ve výrazu elektronického výkaznictví jako `Customers.'name()'`.

Pokud mají metody aplikace datové zdroje s parametry, používá se pro volání těchto metod následující syntaxe:

- Pokud má metoda **isLanguageRTL** datového zdroje **Systém** parametr **EN-US** datového typu *Řetězec*, musí být odkazována ve výrazu elektronického výkaznictví jako `System.isLanguageRTL("EN-US")`.
- Pokud název metody obsahuje pouze alfanumerické znaky, nejsou uvozovky vyžadovány. U metod tabulky, jejichž název obsahuje závorky, jsou však povinné.

Při přidání datového zdroje **Systém** do mapování elektronického výkaznictví, které odkazuje na třídu aplikace **Globální**, výraz `System.isLanguageRTL("EN-US ")` vrátí *logickou hodnotu* **FALSE**. Upravený výraz `System.isLanguageRTL("AR")` vrátí *logickou* hodnotu **TRUE**.

Je možné omezit způsob, jakým jsou hodnoty předány do parametrů tohoto typu metody:

- Lze předat pouze konstanty do metod tohoto typu. Hodnoty konstant jsou definovány v době návrhu.
- Podporovány jsou pouze jednoduché (základní) datové typy pro parametry tohoto typu. Jednoduché datové typy jsou *celé číslo*, *reálné*, *logická hodnota* a *řetězec*.

## <a name=""></a><a name="Paths">Cesty</a>

Pokud výraz odkazuje na strukturovaný zdroj dat, můžete použít definici cesty k volbě určitého primitivního prvku daného zdroje dat. Znak tečky (.) se používá k oddělení jednotlivých prvků strukturovaného zdroje dat. Například aktuální model mapování elektronického výkaznictví obsahuje zdroj dat **InvoiceTransactions** a ten vrátí seznam záznamů. Struktura záznamu **InvoiceTransactions** obsahuje pole **AmountDebit** a **AmountCredit** a obě tato pole vrací číselné hodnoty. Proto můžete pro výpočet fakturované částky navrhnout následující výraz: `InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit`. Konstrukce `InvoiceTransactions.AmountDebit` v tomto výrazu je cesta, která se používá pro přístup k poli **AmountDebit** zdroje dat **InvoiceTransactions** typu *Seznam záznamů*.

### <a name="relative-path"></a>Relativní cesta

Pokud cesta strukturovaného zdroje dat začíná znakem "zavináče" (@), jedná se o relativní cestu. Místo zbývající části absolutní cesty k hierarchické stromové struktuře, která je použita, se zobrazí znaménko zavináče. Následující obrázek znázorňuje příklad. Absolutní cesta `Ledger.'accountingCurrency()'` zde označuje, že hodnota účetní měny ze zdroje dat **hlavní knihy** je zadána do pole **AccountingCurrency** datového modelu.

![Příklad absolutní cesty na stránce návrháře mapování modelu ER](./media/ER-FormulaLanguage-AbsolutePath.png)

Příklad na následujícím obrázku znázorňuje, jak je použita relativní cesta. Relativní cesta `@.AccountNum` označuje, že pole **AccountNum** zdroje dat **Intrastat** (které se zobrazuje o jednu úroveň nad polem **AccountNum** v hierarchickém stromu datového modelu) se používá k zadání čísla účtu odběratele nebo dodavatele v poli **AccountNum** datového modelu.

![Příklad relativní cesty na stránce návrháře mapování modelu ER](./media/ER-FormulaLanguage-RelativePath1.png)

Zbývající část absolutní cesty je také zobrazena v [editoru vzorců ER](general-electronic-reporting-formula-designer.md).

![Zbývající část absolutní cesty na stránce návrháře vzorců ER](./media/ER-FormulaLanguage-RelativePath2.png)

Další informace získáte v části [Použití relativní cesty v datových vazbách modelů a formátů elektronického výkaznictví](relative-path-data-bindings-er-models-format.md).

## <a name=""></a><a name="Functions">Funkce</a>

Vestavěné funkce ER lze používat ve výrazech ER. Všechny zdroje dat kontextu výrazu (tj. aktuální mapování modelu nebo formát elektronického výkaznictví) mohou sloužit jako parametry funkcí volání, v souladu se seznamem argumentů pro funkce volání. Konstanty lze také použít jako parametry funkcí volání. Například aktuální model mapování elektronického výkaznictví obsahuje zdroj dat **InvoiceTransactions** a ten vrátí seznam záznamů. Struktura záznamu **InvoiceTransactions** obsahuje pole **AmountDebit** a **AmountCredit** a obě tato pole vrací číselné hodnoty. Takže pokud chcete vypočítat fakturovanou částku, můžete navrhnout následující výraz využívající integrovanou funkci zaokrouhlování pro použití v elektronickém výkaznictví: `ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)`.

Při navrhování mapování modelu ER a sestav ER můžete použít funkce elektronického výkaznictví z následujících kategorií:

- [Funkce data a času](er-functions-category-datetime.md)
- [Funkce seznamu](er-functions-category-list.md)
- [Logické funkce](er-functions-category-logical.md)
- [Matematické funkce](er-functions-category-mathematical.md)
- [Funkce záznamu](er-functions-category-record.md)
- [Textové funkce](er-functions-category-text.md)
- [Funkce shromažďování dat](er-functions-category-data-collection.md)
- [Další funkce (konkrétní pro obchodní domény)](er-functions-category-other.md)
- [Funkce převodu typu](er-functions-category-type-conversion.md)

## <a name="functions-list-extension"></a>Rozšíření seznamu funkcí

Elektronické výkaznictví umožňuje rozšířit seznam funkcí, které se používají ve výrazech elektronického výkaznictví. Je však vyžadováno určité technické úsilí. Další informace naleznete v tématu [Rozšíření seznamu funkcí elektronického výkaznictví](general-electronic-reporting-formulas-list-extension.md).

## <a name="compound-expressions"></a>Složené výrazy

Můžete vytvořit složené výrazy, které používají funkce z různých kategorií za předpokladu, že se datové typy shodují. Pokud funkce používáte společně, porovnejte datový typ výstupu z jedné funkce do vstupního datového typu, který je vyžadován jinou funkcí. Chcete-li například předejít možné chybě "seznam-je-prázdný" ve vazbě pole na prvek formátu ER, zkombinujte funkce z [kategorie seznamu](er-functions-category-list.md) s funkcí z kategorie [logické](er-functions-category-logical.md), jak ukazuje následující příklad. Zde vzorec používá funkci [IF](er-functions-logical-if.md) k testování, zda je seznam **IntrastatTotals** prázdný předtím, než vrátí hodnotu požadované agregace z tohoto seznamu. Pokud je seznam **IntrastatTotals** prázdný, vrátí vzorec hodnotu **0** (nula).

```vb
IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded') 
```

## <a name="multiple-solutions"></a>Více řešení

Často lze stejný výsledek transformace dat získat několika způsoby, použitím funkcí z různých kategorií nebo různých funkcí ze stejné kategorie. Předchozí výraz lze například také nakonfigurovat pomocí funkce [COUNT](er-functions-list-count.md) z kategorie [List](er-functions-category-list.md).

```vb
IF(COUNT (IntrastatTotals)=0, 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded') 
```

## <a name="additional-resources"></a>Další zdroje

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Návrhář receptur v elektronickém výkaznictví](general-electronic-reporting-formula-designer.md)

[Rozšíření seznamu funkcí elektronického výkaznictví](general-electronic-reporting-formulas-list-extension.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]