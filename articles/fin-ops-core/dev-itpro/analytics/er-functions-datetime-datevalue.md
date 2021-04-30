---
title: Funkce el. výkaznictví DATEVALUE
description: Toto téma obsahuje obecné informace o použití funkce DATEVALUE elektronického výkaznictví.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: cfaf183c61d3663442cbc244239b872b9e1957bb
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891226"
---
# <a name="datevalue-er-function"></a>Funkce el. výkaznictví DATEVALUE

[!include [banner](../includes/banner.md)]

Funkce `DATEVALUE` vrátí hodnotu typu *datum*, která je převedena ze zadané textové hodnoty v určeném formátu a ve volitelně zadané [jazykové verzi](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Informace o podporovaných formátech: [standardní](/dotnet/standard/base-types/standard-date-and-time-format-strings) a [vlastní](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Syntaxe 1

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a>Syntaxe 2

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a>Argumenty

`text`: *řetězec*

Text, který představuje hodnotu pro zformátování.

`format`: *řetězec*

Formát zadaného textu.

`culture`: *řetězec*

Jazyková verze, která se používá pro formátování zadaného textu.

## <a name="return-values"></a>Vrácené hodnoty

*Datum*

Výsledná hodnota data.

## <a name="usage-notes"></a>Poznámky k použití

Pokud není jazyková verze definována jako argument volané funkce, hodnota `culture` je definovaná kontextem volání. Například, pokud je funkce `DATEVALUE` volána pomocí syntaxe 1 ve formátu elektronického výkaznictví (ER) pro prvek **FILE**, který je konfigurován pro použití německé jazykové verze, převod se provede pomocí německé jazykové verze. Výchozí hodnota `culture` je **EN-US**.

## <a name="example-1"></a>Příklad 1

`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` vrátí hodnotu data **December 21, 2016** na základě zadaného vlastního formátu a výchozí jazykové verze **EN-US** aplikace.

## <a name="example-2"></a>Příklad 2

`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` vrátí hodnotu **21. ledna, 2016** (italsky) na základě zadaného vlastního formátu a jazykové verze.

Nicméně `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` zobrazí výjimku informující uživatele, že zadaný řetězec nebyl rozpoznán jako platná hodnota data pro zadanou jazykovou verzi.

## <a name="additional-resources"></a>Další zdroje

[Funkce data a času](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]