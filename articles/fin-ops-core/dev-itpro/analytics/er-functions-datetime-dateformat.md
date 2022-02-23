---
title: Funkce el. výkaznictví DATEFORMAT
description: Toto téma obsahuje obecné informace o použití funkce DATEFORMAT elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: cdc1671f818bc2c4d8a78d0a35337298e83c5060
ms.sourcegitcommit: 7cfe8931dd454e811a691f5118a4ecae7ba4b478
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/04/2021
ms.locfileid: "4826004"
---
# <a name="dateformat-er-function"></a>Funkce el. výkaznictví DATEFORMAT

[!include [banner](../includes/banner.md)]

Funkce `DATEFORMAT` vrátí hodnotu typu *řetězec*, která představuje zadanou hodnotu data jako text v určeném formátu a ve volitelně zadané [jazykové verzi](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Informace o podporovaných formátech: [standardní](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) a [vlastní](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).

## <a name="syntax-1"></a>Syntaxe 1

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a>Syntaxe 2

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a>Argumenty

`date`: *datum*

Hodnota data, která představuje datum pro zformátování.

`format`: *řetězec*

Formát výstupního řetězce.

> [!NOTE]
> Ve formátu řetězce se rozlišují velká a malá písmena, pokud používáte standardní formát nebo vlastní formát. Například [standardní](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) specifikátor formátu „d“ vrací datum pomocí vzoru krátkého data, zatímco standardní specifikátor formátu „D“ vrací datum pomocí vzoru dlouhého data. Navíc [vlastní](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) specifikátor formátu „M“ vrací měsíc od 1 do 12, zatímco specifikátor formátu „m“ vrací minutu od 0 do 59.

`culture`: *řetězec*

Jazyková verze, která má být použita pro formátování.

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná hodnota řetězce.

## <a name="usage-notes"></a>Poznámky k použití

Pokud není jazyková verze definována jako argument volané funkce, hodnota `culture` je definovaná kontextem volání. Například, pokud je funkce `DATEFORMAT` volána pomocí syntaxe 1 ve formátu elektronického výkaznictví (ER) pro prvek **FILE**, který je konfigurován pro použití německé jazykové verze, převod se provede pomocí německé jazykové verze. Výchozí hodnota `culture` je **EN-US**.

## <a name="example-1"></a>Příklad 1

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` vrátí aktuální datum aplikačního serveru, například 24. prosince 2015, jako řetězec **"24-12-2015"** na základě zadaného vlastního formátu.

## <a name="example-2"></a>Příklad 2

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` vrátí aktuální datum relace aplikace, 24. prosince 2015, jako řetězec **"24-12-2015"** na základě vybrané německé jazykové verze a zadaného formátu.

## <a name="additional-resources"></a>Další zdroje

[Funkce data a času](er-functions-category-datetime.md)
