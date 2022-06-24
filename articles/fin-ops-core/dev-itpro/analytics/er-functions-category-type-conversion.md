---
title: Seznam funkcí ER v kategorii převodu typu
description: Tento článek obsahuje informace o funkcích převodu, které jsou podporovány v elektronickém výkaznictví (ER).
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 37516ced402e0204ebd09d5b175ff56b040b9043
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889307"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a>Seznam funkcí ER v kategorii převodu typu

[!include [banner](../includes/banner.md)]

K převodu hodnot mezi typy lze použít funkce pro převod typů elektronického výkaznictví (ER). Tento článek obsahuje souhrn těchto funkcí.

## <a name="type-conversion-functions"></a>Funkce převodu typu

| Funkce | Popis |
|----------|-------------|
| [Int64Value](er-functions-conversion-int64value.md)   | Tato funkce vrací hodnotu *Int64*, která představuje zadaný řetězec. |
| [IntValue](er-functions-conversion-intvalue.md)       | Tato funkce vrací hodnotu *Int*, která představuje zadaný řetězec. |
| [NumberValue](er-functions-conversion-numbervalue.md) | Tato funkce vrací hodnotu typu *reálné číslo*, která je převedena ze zadané hodnoty typu *Řetězec*. Během převodu se uvažují určené oddělovače skupin desetinných míst a číslic. |
| [Hodnota](er-functions-conversion-value.md)             | Tato funkce vrací hodnotu typu *reálné číslo*, která je převedena ze zadané hodnoty typu *Řetězec*. |

## <a name="type-conversion-functions-in-the-container-category"></a>Funkce převodu typu v kategorii kontejneru

V následující tabulce jsou popsány funkce pro převod typů v kategorii [kontejner](er-functions-category-container.md).

| Funkce | popis |
|----------|-------------|
| [Base64StringToContainer](er-functions-container-base64stringtocontainer.md) | Tato funkce převede zadaný vstup datového typu *String* na datovou položku datového typu *Kontejner*. |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a>Funkce převodu typu v kategorii datum a čas

V následující tabulce jsou popsány funkce pro převod typů v [kategorii datum a čas](er-functions-category-datetime.md).

| Funkce | Popis |
|----------|-------------|
| [DateTimeValue](er-functions-datetime-datetimevalue.md)   | Tato funkce vrací hodnotu *DateTime*, která je převedena ze zadané hodnoty typu *řetězec* v určeném formátu a ve volitelně zadané jazykové verzi. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | Tato funkce vrací hodnotu *DateTime*, která je převedena ze zadané hodnoty *datum* na hodnotu data a času v koordinovaném světovém čase (Greenwich Mean Time \[GMT\]). |
| [DateValue](er-functions-datetime-datevalue.md)           | Tato funkce vrací hodnotu *Datum*, která je převedena ze zadané hodnoty typu *řetězec* v určeném formátu a ve volitelně zadané jazykové verzi. |

## <a name="type-conversion-functions-in-the-list-category"></a>Funkce převodu typu v kategorii seznamu

V následující tabulce jsou popsány funkce pro převod typů v [kategorii seznamu](er-functions-category-list.md).

| Funkce | Popis |
|----------|-------------|
| [Seznam](er-functions-list-list.md)                 | Tato funkce vrací hodnotu *seznam záznamů*, která je vytvořena ze specifikovaných argumentů typu *Kontejner (záznam)*. |
| [ListOfFields](er-functions-list-listoffields.md) | Tato funkce vrací hodnotu typu *seznam záznamů*, která je vytvořena na základě struktury daného argumentu typu *výčet* nebo *kontejner (záznam)*. |
| [Rozdělit](er-functions-list-split.md)               | Tato funkce rozdělí zadanou hodnotu *řetězec* do podřetězců a vrátí výsledek jako novou hodnotu typu *seznam záznamů*. |
| [StringJoin](er-functions-list-stringjoin.md)     | Tato funkce vrací hodnotu typu *řetězec*, která se skládá ze zřetězených hodnot zadaného pole ze zadané hodnoty *Seznam záznamů*. Hodnoty mohou být odděleny určeným oddělovačem. |

## <a name="type-conversion-functions-in-the-text-category"></a>Funkce převodu typu v textové kategorii

V následující tabulce jsou popsány funkce pro převod typů v [kategorii textu](er-functions-category-text.md).

| Funkce | Popis |
|----------|-------------|
| [Char](er-functions-text-char.md)                 | Tato funkce vrací hodnotu typu *řetězec*, která představuje jeden znak odkazovaný zadaným číslem Unicode. |
| [GuidValue](er-functions-text-guidvalue.md)       | Tato funkce převede zadaný vstup datového typu *String* na datovou položku datového typu *GUID*. |
| [NumberFormat](er-functions-text-numberformat.md) | Tato funkce vrací hodnotu typu *řetězec*, která představuje zadané číslo jako text v určeném formátu a ve volitelně zadané jazykové verzi. |
| [QrCode](er-functions-text-qrcode.md)             | Tato funkce vrací hodnotu *kontejner*, která zobrazuje kód rychlé odpovědi (QR kód) pro zadaný řetězec v binárním formátu. |
| [Text](er-functions-text-text.md)                 | Tato funkce vrací hodnotu *řetězec*, která představuje zadané číslo poté, co bylo převedeno na textový řetězec formátovaný podle nastavení národního prostředí jazyka stávající instance aplikace. |

## <a name="additional-resources"></a>Další zdroje

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Návrhář receptur v elektronickém výkaznictví](general-electronic-reporting-formula-designer.md)

[Jazyk receptur v elektronickém výkaznictví](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]