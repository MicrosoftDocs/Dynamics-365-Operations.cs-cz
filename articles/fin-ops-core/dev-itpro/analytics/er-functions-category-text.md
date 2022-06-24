---
title: Seznam funkcí elektronického výkaznictví textové kategorie
description: Tento článek obsahuje informace o textových funkcích, které jsou podporovány v elektronickém výkaznictví (ER).
author: NickSelin
ms.date: 02/28/2022
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
ms.openlocfilehash: 502a68d51705114adc096a1cd2217210f4e925bb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885536"
---
# <a name="list-of-er-functions-of-the-text-category"></a>Seznam funkcí elektronického výkaznictví textové kategorie

[!include [banner](../includes/banner.md)]

Textové funkce elektronického výkaznictví (ER) lze použít k provádění operací se zdroji dat datového typu *řetězec*. Tento článek obsahuje souhrn těchto funkcí.

## <a name="list-of-supported-functions"></a>Seznam podporovaných funkcí

| Funkce | Popis |
|----------|-------------|
| [Char](er-functions-text-char.md) | Tato funkce vrací hodnotu typu *řetězec*, která představuje jeden znak odkazovaný zadaným číslem Unicode. |
| [Sloučit](er-functions-text-concatenate.md) | Tato funkce vrací všechny zadané textové řetězce jako hodnotu typu *řetězec* poté, co byly spojeny do jednoho řetězce. |
| [Formát](er-functions-text-format.md) | Tato funkce vrací zadaný řetězec jako hodnotu typu *řetězec* po zformátování nahrazením všech výskytů hodnoty **%N** argumentem *N* tý. |
| [GetEnumValueByName](er-functions-text-getenumvaluebyname.md) | Tato funkce vyhledá určitou hodnotu typu *výčet* v zadaném zdroji dat výčtu pomocí názvu výčtu, který je zadán jako hodnota typu *řetězec*. Pokud je nalezena hodnota *výčet*, funkce ji vrátí. |
| [GetLabelText](er-functions-text-getlabeltext.md) | Tato funkce hledá konkrétní štítek, aby vrátila a hodnotu *[Řetězec](er-formula-supported-data-types-primitive.md#string)*, která představuje překlad zadaného štítku do zadaného jazyka. |
| [GuidValue](er-functions-text-guidvalue.md) | Tato funkce převede zadaný vstup datového typu *String* na datovou položku datového typu *GUID*. |
| [JsonValue](er-functions-text-jsonvalue.md) | Tato funkce analyzuje data ve formátu notace objektu JavaScript (JSON), který je přístupný ze zadané cesty, a extrahuje skalární hodnotu založenou na zadaném ID. Poté vrátí extrahovanou skalární hodnotu jako *řetězcovou* hodnotu. |
| [Vlevo](er-functions-text-left.md) | Tato funkce vrací hodnotu typu *řetězec*, která představuje zadaný počet znaků od počátku zadaného řetězce. |
| [Len](er-functions-text-len.md) | Tato funkce vrací hodnotu *Celé číslo*, která představuje počet znaků v zadaném řetězci. |
| [Lower](er-functions-text-lower.md) | Tato funkce vrací zadaný textový řetězec jako hodnotu *řetězec* poté, co byl převeden na malá písmena. |
| [Mid](er-functions-text-mid.md) | Tato funkce vrací hodnotu typu *[řetězec](er-formula-supported-data-types-primitive.md#string)*, která představuje zadaný počet znaků ze zadaného řetězce počínaje zadanou pozicí. |
| [NewGUID](er-functions-text-newguid.md) | Tato funkce vrací nově vygenerovaná hodnota *[GUID](er-formula-supported-data-types-primitive.md#guid)*. |
| [NumberFormat](er-functions-text-numberformat.md) | Tato funkce vrací hodnotu typu *řetězec*, která představuje zadané číslo jako text v určeném formátu a ve volitelně zadané jazykové verzi. |
| [NumeralsToText](er-functions-text-numeralstotext.md) | Tato funkce vrací zadané číslo jako hodnotu typu *řetězec* poté, co byla napsána (tedy převedena na textové řetězce) v zadaném jazyce. |
| [PadLeft](er-functions-text-padleft.md) | Tato funkce vrací hodnotu typu *řetězec* určené délky, ve kterém je začátek určeného řetězce odsazen jednou nebo více instancemi zadaných znaků. |
| [QrCode](er-functions-text-qrcode.md) | Tato funkce vrací hodnotu *kontejner*, která zobrazuje kód rychlé odpovědi (QR kód) pro zadaný řetězec v binárním formátu. |
| [Nahradit](er-functions-text-replace.md) | Tato funkce vrací zadaný textový řetězec jako hodnotu typu *řetězec* po nahrazení celého řetězce nebo jeho části jiným řetězcem. |
| [Vpravo](er-functions-text-right.md) | Tato funkce vrací hodnotu typu *řetězec*, která představuje zadaný počet znaků od konce zadaného řetězce. |
| [Text](er-functions-text-text.md) | Tato funkce vrací zadané číslo jako hodnotu *řetězec* poté, co bylo převedeno na textový řetězec naformátovaný podle nastavení národního prostředí jazyka stávající instance aplikace. |
| [Přeložit](er-functions-text-translate.md) | Tato funkce vrací *řetězcovou* hodnotu, která obsahuje výsledek nahrazení zadaného textu znaky pro jinou zadanou sadu znaků. |
| [Trim](er-functions-text-trim.md) | Tato funkce vrátí zadaný textový řetězec jako hodnotu *Řetězec* poté, co tabulátor, návrat vozíku, posun řádku a posun formuláře byly nahrazeny jednou mezerou, po zkrácení úvodní a koncové mezery a po odstranění více mezer mezi slovy. |
| [Upper](er-functions-text-upper.md) | Tato funkce vrací zadaný textový řetězec jako hodnotu *řetězec* poté, co byl převeden na velká písmena. |

## <a name="additional-resources"></a>Další zdroje

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Návrhář receptur v elektronickém výkaznictví](general-electronic-reporting-formula-designer.md)

[Jazyk receptur v elektronickém výkaznictví](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
