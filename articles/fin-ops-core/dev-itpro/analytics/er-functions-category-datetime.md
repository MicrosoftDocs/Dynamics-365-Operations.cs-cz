---
title: Seznam funkcí ER v kategorii Datum a čas
description: Toto téma obsahuje informace o funkcích data a času, které jsou podporovány v elektronickém výkaznictví (ER).
author: NickSelin
ms.date: 09/09/2021
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
ms.openlocfilehash: 706331eaadf602aba46463fdcfc0d38f1fc94e08
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647256"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a>Seznam funkcí ER v kategorii Datum a čas

[!include [banner](../includes/banner.md)]

Funkce data a času elektronického výkaznictví lze používat k extrahování informací z hodnot data a času a k provádění operací s těmito hodnotami. Toto téma obsahuje souhrn těchto funkcí.

## <a name="list-of-supported-functions"></a>Seznam podporovaných funkcí

| Funkce | Popis |
|----------|-------------|
| [AddDays](er-functions-datetime-adddays.md) | Tato funkce vrací hodnotu *[DateTime](er-formula-supported-data-types-primitive.md#datetime)*, která představuje zadaný počet dní před nebo po zadaném počátečním datu. |
| [ChangeTimeZone](er-functions-datetime-changetimezone.md) | Tato funkce vrací hodnotu *DateTime*, která je převedena ze zadané hodnoty kalendářního data/času v jednom časovém pásmu na hodnotu data a času v jiném časovém pásmu. |
| [DateFormat](er-functions-datetime-dateformat.md) | Tato funkce vrací hodnotu typu *[řetězec](er-formula-supported-data-types-primitive.md#string)*, která představuje zadanou hodnotu data jako text v určeném formátu a ve volitelně zadané jazykové verzi. |
| [DateTimeFormat](er-functions-datetime-datetimeformat.md) | Tato funkce vrací hodnotu typu *řetězec*, která představuje zadanou hodnotu data/času jako text v určeném formátu a ve volitelně zadané jazykové verzi. |
| [DateTimeValue](er-functions-datetime-datetimevalue.md) | Tato funkce vrací hodnotu *DateTime*, která je převedena ze zadané textové hodnoty v určeném formátu a ve volitelně zadané jazykové verzi. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | Tato funkce vrací hodnotu *DateTime*, která je převedena ze zadané hodnoty kalendářního data na hodnotu data a času v koordinovaném světovém čase (Greenwich Mean Time \[GMT\]). |
| [DateValue](er-functions-datetime-datevalue.md) | Tato funkce vrací hodnotu typu *Datum*, která je převedena ze zadané textové hodnoty v určeném formátu a ve volitelně zadané jazykové verzi. |
| [DayOfYear](er-functions-datetime-dayofyear.md) | Tato funkce vrací hodnotu typu *celé číslo*, která představuje počet dní mezi 1. lednem a zadaným datem. |
| [Dny](er-functions-datetime-days.md) | Tato funkce vrací hodnotu typu *celé číslo*, která představuje počet dní mezi jedním a druhým zadaným datem. |
| [Now](er-functions-datetime-now.md) | Tato funkce vrací hodnotu *DateTime*, která představuje aktuální datum a čas aplikačního serveru. |
| [NullDate](er-functions-datetime-nulldate.md) | Tato funkce vrací hodnotu typu *datum*, která představuje datum typu **null** (1. leden 1900). |
| [NullDateTime](er-functions-datetime-nulldatetime.md) | Tato funkce vrací hodnotu *DateTime*, která představuje hodnotu **null** data a času (1. leden 1900) v koordinovaném univerzálním čase (Coordinated Universal Time). |
| [SessionNow](er-functions-datetime-sessionnow.md) | Tato funkce vrací hodnotu *DateTime*, která představuje aktuální datum a čas relace aplikace. |
| [SessionToday](er-functions-datetime-sessiontoday.md) | Tato funkce vrací hodnotu typu *datum*, která představuje aktuální datum relace aplikace. |
| [Dnes](er-functions-datetime-today.md) | Tato funkce vrací hodnotu typu *datum*, která představuje aktuální datum aplikačního serveru. |

## <a name="additional-resources"></a>Další zdroje

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Návrhář receptur v elektronickém výkaznictví](general-electronic-reporting-formula-designer.md)

[Jazyk receptur v elektronickém výkaznictví](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
