---
title: Funkce el. výkaznictví JSONVALUE
description: Toto téma obsahuje obecné informace o použití funkce JSONVALUE elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 11f9ac680ea00622367ea56106fd22508628d85d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685900"
---
# <a name="jsonvalue-er-function"></a>Funkce el. výkaznictví JSONVALUE

[!include [banner](../includes/banner.md)]

Funkce `JSONVALUE` analyzuje data ve formátu notace objektu JavaScript (JSON), který je dostupný v zadané cestě, a extrahuje skalární hodnotu se zadaným ID. Poté vrátí extrahovanou skalární hodnotu jako *řetězcovou* hodnotu.

## <a name="syntax"></a>Syntaxe

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a>Argumenty

`input`: *řetězec*

Platná cesta ke zdroji dat typu *řetězec* obsahujícímu data JSON.

`path`: *řetězec*

Identifikátor skalární hodnoty dat JSON.

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná textová hodnota.

## <a name="example"></a>Příklad

Zdroj dat **JsonField** obsahuje následující data ve formátu JSON: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**. V tomto případě výraz `JSONVALUE (JsonField, "BuildNumber")` vrátí následující hodnotu datového typu *řetězec*: **"7.3.1234.1"**.

## <a name="additional-resources"></a>Další zdroje

[Textové funkce](er-functions-category-text.md)
