---
title: Funkce el. výkaznictví WEEKNUM
description: Toto téma obsahuje obecné informace o použití funkce WEEKNUM elektronického výkaznictví.
author: NickSelin
ms.date: 01/15/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: 37e62b32896e2030b3322a89ac4acdd6c18d5e3c
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982170"
---
# <a name="weeknum-er-function"></a>Funkce el. výkaznictví WEEKNUM

[!include [banner](../includes/banner.md)]

Funkce `WEEKNUM` vrátí hodnotu typu *[celé číslo](er-formula-supported-data-types-primitive.md#integer)*, která představuje týden v roce a zahrnuje zadanou hodnotu *[Datum](er-formula-supported-data-types-primitive.md#date)*. Výpočet je založen na pravidlech závislých na jazykové verzi, která definují kalendářní týden a první den v týdnu.

## <a name="syntax"></a>Syntaxe

```vb
WEEKNUM (date, culture) as Integer
```

## <a name=""></a><a name="arguments">Argumenty</a>

`date`: *datum*

Hodnota kalendářního data, která představuje datum, které má být použito pro výpočet týdne v roce.

`culture`: *[Řetězec](er-formula-supported-data-types-primitive.md#string)*

Jazyková verze, která má být použita pro výpočet. Můžete použít kódy jazykové verze, které jsou podporovány v souladu se [standardy](/dotnet/api/system.globalization.cultureinfo.getcultures?view=net-5.0) .NET.

## <a name="return-values"></a>Vrácené hodnoty

*Celé číslo*

Výsledná číselná hodnota.

## <a name="usage-notes"></a>Poznámky k použití

Týden v roce se vypočítá na základě standardu [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html), pokud byl tento standard přijat zemí nebo oblastí, pro které je národní prostředí poskytováno za běhu. Jinak je výpočet založen na národních standardech specifických pro zemi/oblast.

Pokud je při běhu jako argument funkce `WEEKNUM` zadán nepodporovaný kód [jazykové verze](#arguments), je vyvolána výjimka. Pokud je jako kód kultury zadán prázdný řetězec, použije se k výpočtu čísla týdne anglický kalendář, který je neutrální pro danou zemi.

## <a name="examples"></a>Příklad

`WEEKNUM (DATEVALUE ("01-01-2020", "de"))` vrací **1**.

`WEEKNUM (DATEVALUE ("01-01-2021", "de"))` vrací **53**.

`WEEKNUM (DATEVALUE ("01-01-2022", "de"))` vrací **52**.

`WEEKNUM (DATEVALUE ("01-01-2022", "ar"))` vrací **21**.

## <a name="additional-resources"></a>Další prostředky

[Funkce data a času](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
