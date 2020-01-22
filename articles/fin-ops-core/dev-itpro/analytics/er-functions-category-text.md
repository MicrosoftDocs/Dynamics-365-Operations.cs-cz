---
title: Seznam funkcí elektronického výkaznictví textové kategorie
description: Toto téma obsahuje informace o textových funkcích, které jsou podporovány v elektronickém výkaznictví (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f519d242fe74196b0d12bdc9df4f1b4b0e585752
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916607"
---
# <a name="list-of-er-functions-of-the-text-category"></a>Seznam funkcí elektronického výkaznictví textové kategorie

[!include [banner](../includes/banner.md)]

Textové funkce elektronického výkaznictví (ER) lze použít k provádění operací se zdroji dat datového typu *řetězec*. Toto téma obsahuje souhrn těchto funkcí.

## <a name="list-of-supported-functions"></a>Seznam podporovaných funkcí

| Funkce | Popis |
|----------|-------------|
| [Char](er-functions-text-char.md) | Tato funkce vrací hodnotu typu *řetězec*, která představuje jeden znak odkazovaný zadaným číslem Unicode. |
| [Sloučit](er-functions-text-concatenate.md) | Tato funkce vrací všechny zadané textové řetězce jako hodnotu typu *řetězec* poté, co byly spojeny do jednoho řetězce. |
| [Formát](er-functions-text-format.md) | Tato funkce vrací zadaný řetězec jako hodnotu typu *řetězec* po zformátování nahrazením všech výskytů hodnoty **%N** argumentem *N*tý. |
| [GetEnumValueByName](er-functions-text-getenumvaluebyname.md) | Tato funkce vyhledá určitou hodnotu typu *výčet* v zadaném zdroji dat výčtu pomocí názvu výčtu, který je zadán jako hodnota typu *řetězec*. Pokud je nalezena hodnota *výčet*, funkce ji vrátí. |
| [GuidValue](er-functions-text-guidvalue.md) | Tato funkce převede zadaný vstup datového typu *String* na datovou položku datového typu *GUID*. |
| [JsonValue](er-functions-text-jsonvalue.md) | Tato funkce analyzuje data ve formátu notace objektu JavaScript (JSON), který je přístupný ze zadané cesty, a extrahuje skalární hodnotu založenou na zadaném ID. Poté vrátí extrahovanou skalární hodnotu jako *řetězcovou* hodnotu. |
| [Vlevo](er-functions-text-left.md) | Tato funkce vrací hodnotu typu *řetězec*, která představuje zadaný počet znaků od počátku zadaného řetězce. |
| [Len](er-functions-text-len.md) | Tato funkce vrací hodnotu *Celé číslo*, která představuje počet znaků v zadaném řetězci. |
| [Lower](er-functions-text-lower.md) | Tato funkce vrací zadaný textový řetězec jako hodnotu *řetězec* poté, co byl převeden na malá písmena. |
| [Mid](er-functions-text-mid.md) | Tato funkce vrací hodnotu typu *řetězec*, která představuje zadaný počet znaků ze zadaného řetězce počínaje zadanou pozicí. |
| [NumberFormat](er-functions-text-numberformat.md) | Tato funkce vrací hodnotu typu *řetězec*, která představuje zadané číslo jako text v určeném formátu a ve volitelně zadané jazykové verzi. |
| [NumeralsToText](er-functions-text-numeralstotext.md) | Tato funkce vrací zadané číslo jako hodnotu typu *řetězec* poté, co byla napsána (tedy převedena na textové řetězce) v zadaném jazyce. |
| [PadLeft](er-functions-text-padleft.md) | Tato funkce vrací hodnotu typu *řetězec* určené délky, ve kterém je začátek určeného řetězce odsazen jednou nebo více instancemi zadaných znaků. |
| [QrCode](er-functions-text-qrcode.md) | Tato funkce vrací hodnotu *kontejner*, která zobrazuje kód rychlé odpovědi (QR kód) pro zadaný řetězec v binárním formátu. |
| [Nahradit](er-functions-text-replace.md) | Tato funkce vrací zadaný textový řetězec jako hodnotu typu *řetězec* po nahrazení celého řetězce nebo jeho části jiným řetězcem. |
| [Vpravo](er-functions-text-right.md) | Tato funkce vrací hodnotu typu *řetězec*, která představuje zadaný počet znaků od konce zadaného řetězce. |
| [Text](er-functions-text-text.md) | Tato funkce vrací zadané číslo jako hodnotu *řetězec* poté, co bylo převedeno na textový řetězec naformátovaný podle nastavení národního prostředí jazyka stávající instance aplikace. |
| [Přeložit](er-functions-text-translate.md) | Tato funkce vrací zadaný textový řetězec jako hodnotu typu *řetězec* po nahrazení celého řetězce nebo jeho části jiným řetězcem. |
| [Trim](er-functions-text-trim.md) | Tato funkce vrací určený textový řetězec jako hodnotu typu *řetězec* poté, co byly zkráceny úvodní a koncové mezery a odebráno více mezer mezi slovy. |
| [Upper](er-functions-text-upper.md) | Tato funkce vrací zadaný textový řetězec jako hodnotu *řetězec* poté, co byl převeden na velká písmena. |

## <a name="additional-resources"></a>Další zdroje

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Návrhář receptur v elektronickém výkaznictví](general-electronic-reporting-formula-designer.md)

[Jazyk receptur v elektronickém výkaznictví](er-formula-language.md)
