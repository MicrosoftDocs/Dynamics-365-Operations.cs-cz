---
title: Funkce el. výkaznictví DATETIMEVALUE
description: Toto téma obsahuje obecné informace o použití funkce DATETIMEVALUE elektronického výkaznictví.
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: db5b2c56f0c6dcc019419801821d7a6eae8a0e91
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891274"
---
# <a name="datetimevalue-er-function"></a>Funkce el. výkaznictví DATETIMEVALUE

[!include [banner](../includes/banner.md)]

Funkce `DATETIMEVALUE` vrátí hodnotu typu *datum a čas*, která je převedena ze zadané textové hodnoty v určeném formátu a ve volitelně zadané [jazykové verzi](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Informace o podporovaných formátech: [standardní](/dotnet/standard/base-types/standard-date-and-time-format-strings) a [vlastní](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Syntaxe 1

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a>Syntaxe 2

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a>Argumenty

`text`: *řetězec*

Text, který představuje hodnotu pro zformátování.

`format`: *řetězec*

Formát zadaného textu.

`culture`: *řetězec*

Jazyková verze, která se používá pro formátování zadaného textu.

## <a name="return-values"></a>Vrácené hodnoty

*Datum a čas*

Výsledná hodnota data a času.

## <a name="usage-notes"></a>Poznámky k použití

Pokud není jazyková verze definována jako argument volané funkce, hodnota `culture` je definovaná kontextem volání. Například, pokud je funkce `DATETIMEVALUE` volána pomocí syntaxe 1 ve formátu elektronického výkaznictví (ER) pro prvek **FILE**, který je konfigurován pro použití německé jazykové verze, převod se provede pomocí německé jazykové verze. Výchozí hodnota `culture` je **EN-US**.

## <a name="example-1"></a>Příklad 1

`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` vrátí **2:55:00 AM on December 21, 2016** na základě zadaného vlastního formátu a výchozí jazykové verze **EN-US** aplikace.

## <a name="example-2"></a>Příklad 2

`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` vrátí **2:55:00, 21. ledna 2016** (italsky) na základě zadaného vlastního formátu a jazykové verze.

Nicméně `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` zobrazí výjimku informující uživatele, že zadaný řetězec nebyl rozpoznán jako platná hodnota data/času pro zadanou jazykovou verzi.

## <a name="additional-resources"></a>Další zdroje

[Funkce data a času](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]