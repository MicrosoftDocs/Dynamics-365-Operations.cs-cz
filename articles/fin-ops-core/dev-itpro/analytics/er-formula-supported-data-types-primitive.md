---
title: Podporované typy jednoduchých dat pro vzorce elektronického výkaznictví
description: Tento článek obsahuje informace o typech jednoduchých dat, které jsou podporovány ve vzorcích elektronického výkaznictví (ER).
author: kfend
ms.date: 06/02/2021
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 26c166744e1705baa9dcce6b93c76f110524b7d7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284567"
---
# <a name="supported-primitive-data-types-for-electronic-reporting-formulas"></a>Podporované typy jednoduchých dat pro vzorce elektronického výkaznictví

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace o typech jednoduchých dat, které jsou podporovány ve výrazech [elektronického výkaznictví (ER)](general-electronic-reporting.md). Zde je uveden seznam typů jednoduchýcg dat:

- [logická hodnota](#boolean)
- [datum](#date)
- [datetime](#datetime)
- [výčet](#enumeration)
- [guid](#guid)
- [integer](#integer)
- [int64](#int64)
- [real](#real)
- [řetězec](#string)

## <a name="boolean"></a><a name="boolean"></a>Logická

*Logický* typ jednoduchých dat obsahuje hodnotu, která je vyhodnocena jako *true* nebo *false*. Můžete použít vyhrazená doslovná klíčová slova **True** a **False**, kdekoli se očekává *logický* výraz. Výchozí hodnota je *false*.

Interní reprezentace a *logického* typu je *integer*. Hodnota *integer* 0 (nula) je vyhodnocena jako *false* a všechny ostatní hodnoty *integer* jsou vyhodnoceny jako *true*. Pokud jste [ověřili](general-electronic-reporting-formula-designer.md#TestFormula) nakonfigurovaný výraz, který vrací *logickou* hodnotu v [návrháři vzorců ER](er-advanced-formula-editor.md), podokno výsledků testu zobrazí *0* (nula), když výraz vrátí *false*. Jinak se podokno výsledků testu zobrazí *1*.

*Logický* typ nemá žádné implicitní převody. Můžete však použít funkci [TEXT](er-functions-text-text.md) k výslovnému převodu *logického* typu na *řetězec*:

- Hodnota *false* se převede na textový řetězec **False**.
- Hodnota *true* se převede na textový řetězec **True**.

> [!NOTE]
> Tato konverze nezávisí na zadaném jazyce a [kontextu](er-design-multilingual-reports.md) jazykové verze.

[Operátory](er-formula-language.md#Operators) srovnání jsou jediným typem operátoru, který lze použít s *logickým* datovým typem. K porovnání dvou *logických* hodnot lze použít následující operátory: \<\> and =.

## <a name="date"></a><a name="date"></a>Datum

Jednoduchý datový typ *date* obsahuje údaje o dnu, měsíci a roce. Data lze spustit pomocí následujících funkcí:

- [DATEVALUE](er-functions-datetime-datevalue.md)
- [NULLDATE](er-functions-datetime-nulldate.md)
- [SESSIONTODAY](er-functions-datetime-sessiontoday.md)
- [TODAY](er-functions-datetime-today.md)

Datový typ *datum* může obsahovat data mezi 1. lednem 1900 a 31. prosincem 2154. Výchozí hodnota je **null** a interní reprezentace je datum 1. ledna 1900.

*Datum* nemá žádné implicitní převody. Můžete však použít následující explicitní funkce převodu:

- [DATEFORMAT](er-functions-datetime-dateformat.md)
- [DATETODATETIME](er-functions-datetime-datetodatetime.md)
- [TEXT](er-functions-text-text.md)

Funkce [ADDDAYS](er-functions-datetime-adddays.md) umožňuje sčítat a odečítat dny od dat. Tímto způsobem můžete datum přesunout o určitý počet dní do budoucnosti a minulosti. Funkce [DAYS](er-functions-datetime-days.md) umožňuje odečíst data od sebe navzájem a vypočítat rozdíl ve dnech. Další informace o transformaci hodnot *datum* viz [Seznam funkcí ER v kategorii Datum a čas](er-functions-category-datetime.md).

[Operátory](er-formula-language.md#Operators) srovnání jsou jediným typem operátoru, který lze použít s datovým typem *datum*. K porovnání dvou hodnot *datum* lze použít následující operátory: \<\>, \<, \<=, =, \> a \>=.

## <a name="datetime"></a><a name="datetime"></a>Datum a čas

Typ jednoduchých dat *datetime* kombinuje typ *datum* a hodnotu, která představuje čas, který uplynul od půlnoci. Čas je vyjádřen v hodinách, minutách, sekundách a zlomcích sekundy. Hodnota *datetime* také obsahuje informace o časovém pásmu.

Datový typ *datetime* může obsahovat data mezi 1. lednem 1900 (1900-01-01T00:00:00.0000000+00:00 ve [formátu](/dotnet/standard/base-types/standard-date-and-time-format-strings)) opakované cesty a 31. prosince 2154 (2154/12/31T11:59:59.9999999+00:00 ve formátu opakované cesty). Nejmenší jednotka času v *datetime* je desetimiliontina sekundy.

> [!NOTE]
> Pokud se použije **hh** [specifikátor](/dotnet/standard/base-types/standard-date-and-time-format-strings) pro hodiny, časové hodnoty nad 12:59:59:9999999 nelze interpretovat jako platné časy.
>
> Pokud se použije **HH** specifikátor pro hodiny, časové hodnoty nad 23:59:59:9999999 nelze interpretovat jako platné časy.

Výchozí hodnota je **nul** a interní reprezentace je datum 1. ledna 1900 (1900-01-01T00:00:00.0000000+00:00 ve formátu opakované cesty).

Datetime lze spustit pomocí následujících funkcí:

- [DATETIMEVALUE](er-functions-datetime-datetimevalue.md)
- [NULNULLDATETIMELDATE](er-functions-datetime-nulldatetime.md)
- [SESSIONNOW](er-functions-datetime-sessionnow.md)
- [NOW](er-functions-datetime-now.md)

*Datetime* nemá žádné implicitní převody. Můžete však použít následující explicitní funkce převodu:

- [DATETIMEFORMAT](er-functions-datetime-datetimeformat.md)
- [TEXT](er-functions-text-text.md)

Další informace o transformaci hodnot *datetime* viz [Seznam funkcí ER v kategorii Datum a čas](er-functions-category-datetime.md).

[Operátory](er-formula-language.md#Operators) srovnání jsou jediným typem operátoru, který lze použít s datovým typem *datetime*. K porovnání dvou hodnot *datetime* lze použít následující operátory: \<\>, \<, \<=, =, \> a \>=.

## <a name="enumeration"></a><a name="enumeration"></a>Výčet

Typ jednoduchých dat *výčet* je seznam znaků. Můžete použít výčty, které jsou definovány v aplikaci [zdrojový kód](../dev-ref/xpp-data-primitive.md#enum). Můžete také představit své vlastní výčty v datovém modelu ER a komponentách formátu ER.

Aplikace *výčet* lze použít ve výrazech libovolného mapování modelu ER a formátu ER.

Následující obrázek ukazuje, jak můžete přidat výčet modelu **CustVendCorrectiveReasonCode** do upravitelného datového modelu ER.

[![Konfigurace výčtu modelu v návrháři datového modelu ER.](./media/er-formula-supported-data-types-primitive-enum1.gif)](./media/er-formula-supported-data-types-primitive-enum1.gif)

*Výčet* modelu lze použít ve výrazech libovolného mapování modelu ER a formátu ER, které byly vytvořeny pod datovým modelem, kde byl *výčet* představen.

Následující obrázek ukazuje, jak můžete přidat výčet formátu **Seznam podkategorií stornovacích poplatků Natura** do upravitelného formátu ER.

[![Konfigurace výčtu formátu v návrháři formátu ER.](./media/er-formula-supported-data-types-primitive-enum2.gif)](./media/er-formula-supported-data-types-primitive-enum2.gif)

*Výčet* formátu lze použít pouze ve výrazech formátu ER, kde byl *výčet* představen.

Musíte použít vhodný typ zdrojů dat ER k přenesení konkrétního výčtu do nakonfigurované komponenty ER jako konstanty nebo jako hodnotu, kterou uživatel, který spouští řešení ER, definoval v dialogovém okně za běhu.

- K výčtu aplikací lze přistupovat pomocín zdrojů dat **Dynamics 365 for Operations \ Výčet** a **Obecné \ Uživatelské vstupní parametry**. Následující obrázek ukazuje, jak můžete přidat do upravitelného formátu ER datové zdroje **appenumNoAno** a **uipNoYes**, které odkazují na výčet aplikací **NoYes**.

    [![Přidání zdrojů dat výčtu aplikace v návrháři formátu ER.](./media/er-formula-supported-data-types-primitive-enum3a.gif)](./media/er-formula-supported-data-types-primitive-enum3a.gif)

- K výčtům datového modelu lze přistupovat pomocí zdrojů dat  **Datový model \ Výčet** a **Datový model \ Vstupní parametry uživatele výčtu**. Následující obrázek ukazuje, jak můžete přidat do upravitelného formátu ER datové zdroje **CustVendCorrectiveReasonCode**, které odkazují na datový model **CustVendCorrectiveReasonCode**.

    [![Přidání zdrojů dat výčtu modelu v návrháři formátu ER.](./media/er-formula-supported-data-types-primitive-enum3b.gif)](./media/er-formula-supported-data-types-primitive-enum3b.gif)

- K výčtům formátů lze přistupovat pomocí zdrojů dat **Formát \ Výčet** a **Formát \ Vstupní parametry uživatele výčtu** Následující obrázek ukazuje, jak můžete přidat do upravitelného formátu ER datové zdroje **NaturaReverseCharge**, které odkazují na výčet formátu **Podkategorie stornovacích poplatků Natura**.

    [![Přidání zdrojů dat výčtu formátu v návrháři formátu ER.](./media/er-formula-supported-data-types-primitive-enum3c.gif)](./media/er-formula-supported-data-types-primitive-enum3c.gif)

*Výčet* nemá žádné implicitní převody. Můžete však použít převodní funkci [TEXT](er-functions-text-text.md) pro převod *výčtu* na textový řetězec. Tato konverze není závislá na jazyce. Chcete-li se dozvědět, jak můžete přidružit hodnotu *výčet* s příslušnými popisky specifickými pro daný jazyk, viz příklady použití pro funkce [LISTOFFIELDS](er-functions-list-listoffields.md) a [GETENUMVALUEBYNAME](er-functions-text-getenumvaluebyname.md).

[Operátory](er-formula-language.md#Operators) srovnání jsou jediným typem operátoru, který lze použít s datovým typem *výčet*. K porovnání dvou hodno *výčtu* lze použít následující operátory: \<\> and =.

## <a name="guid"></a><a name="guid"></a>Guid

Typ jednoduchých dat *giud* obsahuje hodnotu globálně jedinečného identifikátoru (GUID). Identifikátor GUID je hodnota, kterou lze použít ve všech počítačích a sítích, kdekoli je vyžadován jedinečný identifikátor. Je nepravděpodobné, že číslo bude duplikováno. Platný identifikátor GUID splňuje všechny následující specifikace:

- Musí existovat 32 hexadecimálních číslic.
- Kromě toho musí být na následujících místech vloženy čtyři pomlčkové znaky: 8-4-4-4-12.
- Navíc volitelná lomítka \{\} lze přidat na začátek a konec řetězce. Například **\{2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212\}** a **2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212** jsou platné řetězce GUID.
- Proto musí existovat celkem 36 nebo 38 znaků, v závislosti na tom, zda jsou přidány složené závorky.
- Písmena, která se používají jako hexadecimální číslice, mohou být velká (A – F), malá písmena (a – f) nebo smíšená.

Můžete použít následující explicitní funkce převodu:

- [GUIDVALUE](er-functions-text-guidvalue.md)
- [TEXT](er-functions-text-text.md)

[Operátory](er-formula-language.md#Operators) srovnání jsou jediným typem operátoru, který lze použít s datovým typem *guid*. K porovnání dvou hodnot *guid* hodnot lze použít následující operátory: \<\> a =.

## <a name="integer"></a><a name="integer"></a>Celé číslo

Typ jednoduchých dat *integer* představuje číslo, které nemá desetinná místa. Integery se používají jako kontrolní proměnné v opakujících se příkazech nebo jako indexy v seznamech záznamů.

Literál *integer* je celé číslo, protože je zadáno přímo do [výrazu](general-electronic-reporting-formula-designer.md#formula-designer-overview) ER (vzorec), jako je **12345**. *Integer* má 32 bitů. Výchozí hodnota je **0** a interní reprezentace je dlouhé číslo. *Integer* se automaticky převede na *real*.

Můžete také použít následující explicitní funkce převodu:

- [INTVALUE](er-functions-conversion-intvalue.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)

Rozsah funkce *integer* je \[-2 147 483 647 : 2 147 483 647\]. Všechny integery tohoto rozsahu lze použít jako literály.

Všechny srovnání a matematické [operátory](er-formula-language.md#Operators) lze použít s datovým typem *integer*.

## <a name="int64"></a><a name="int64"></a>Int64

Typ jednoduchých dat *int64* představuje číslo, které nemá desetinná místa. Hodnoty *Int64* se používají jako kontrolní proměnné v opakujících se příkazech nebo jako indentifikátory záznamů.

*Int64* má 64 bitů. Výchozí hodnota je **0** a interní reprezentace je dlouhé číslo. *Int64* se automaticky převede na *real*.

Můžete také použít následující explicitní funkce převodu:

- [INT64VALUE](er-functions-conversion-int64value.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)

Rozsah funkce *int64* je \[-9 223 372 036 854 775 807 : 9 223 372 036 854 775 807\].

Všechny srovnání a matematické [operátory](er-formula-language.md#Operators) lze použít s datovým typem *int64*.

## <a name="real"></a><a name="real"></a>Reálný

Typ jednoduchých dat *real* může kromě celých čísel obsahovat desetinná místa. Desetinné literály můžete použít kdekoli, kde se očekává *real*. Desetinný literál je desetinné číslo, protože je zadáno přímo v kódu, například **2,19**.

> [!NOTE]
> Ve výrazech ER se jako oddělovač desetinných míst vždy používá tečka (.).

Funkci real lze použít ve všech výrazech a lze ji použít s operátory porovnání i aritmetiky. *Real* má přesnost 16 platných číslic. Výchozí hodnota pro *real* je **0,0** a interní reprezentace je binárně kódované digitální číslo (BCD). Kódování BCD umožňuje přesnou reprezentaci hodnot, které jsou násobky 0,1. Rozsah proměnné *real* je -(10)<sup>127</sup> až (10)<sup>127</sup>. Všechny hodnoty real v tomto rozsahu lze použít jako literály ve výrazech ER.

*Real* nemá žádné implicitní převody. Následující funkce však můžete použít k explicitnímu převodu hodnoty *real* do jiných datových typů a dalších datových typů do hodnoty *real*:

- [INTVALUE](er-functions-conversion-intvalue.md)
- [INT64VALUE](er-functions-conversion-int64value.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)
- [VALUE](er-functions-conversion-value.md)

Všechny srovnávací a matematické [operátory](er-formula-language.md#Operators) lze použít s datovým typem *real*.

## <a name="string"></a><a name="string"></a>Řetězec

Typ jednoduchých dat *řetězec* představuje posloupnost znaků, které se používají jako texty, čísla účtů, adresy a telefonní čísla.

Literály typu *řetězec* jsou znaky, které jsou uzavřeny v uvozovkách (""). Literály typu *řetězec* lze použít kdekoli, kde se očekávají hodnoty *řetězec* ve výrazech ER. Řetězce můžete použít v logických výrazech, jako jsou například srovnání. Můžete také zřetězit hodnoty *řetězec* pomocí operátoru **\&** nebo funkce [CONCATENATE](er-functions-text-concatenate.md).

> [!NOTE]
> Pokud spojíte dvě hodnboty *řetězec* a chcete, aby výsledný *řetězec* překlenul více než jeden řádek, použijte mezi hodnotami oddělovač konce řádku. Pro výstup TEXT může být tímto oddělovačem znak, který je generován pomocí výrazu [CHAR](er-functions-text-char.md)(10) nebo CHAR (13). U HTML to může být značka **\<br\>**.

Výchozí hodnota pro *řetězec* je prázdný textový řetězec, který nemá žádné znaky, a interní reprezentací je seznam znaků.

Pro řetězce neexistují žádné automatické převody. Lze však použít následující explicitní funkce převodu:

- [CHAR](er-functions-text-char.md)
- [FORMAT](er-functions-text-format.md)
- [LEFT](er-functions-text-left.md)
- [LEN](er-functions-text-len.md)
- [MID](er-functions-text-mid.md)
- [PADLEFT](er-functions-text-padleft.md)
- [REPLACE](er-functions-text-replace.md)
- [RIGHT](er-functions-text-right.md)
- [TEXT](er-functions-text-text.md)
- [TRANSLATE](er-functions-text-translate.md)
- [TRIM](er-functions-text-trim.md)
- [UPPER](er-functions-text-upper.md)

Další informace o transformaci hodnot *řetězec* viz [Seznam funkcí ER v kategorii text](er-functions-category-text.md).

*Řetězec* může obsahovat neomezený počet znaků.

Všechny srovnávací [operátory](er-formula-language.md#Operators) lze použít s datovým typem *rětězec*.

## <a name="additional-resources"></a>Další prostředky

- [Přehled elektronického výkaznictví](general-electronic-reporting.md)
- [Jazyk receptur v elektronickém výkaznictví](er-formula-language.md)
- [Podporované typy složených dat](er-formula-supported-data-types-composite.md)
