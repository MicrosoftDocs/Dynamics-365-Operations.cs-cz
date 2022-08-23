---
title: Funkce el. výkaznictví LEN
description: Tento článek obsahuje obecné informace o použití funkce LEN elektronického výkaznictví.
author: kfend
ms.date: 12/11/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 5a8e672e0308a58dca28c73ce01c7307abec60ed
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280118"
---
# <a name="len-er-function"></a>Funkce el. výkaznictví LEN

[!include [banner](../includes/banner.md)]

Funkce `LEN` vrátí počet znaků v zadaném řetězci jako *celočíselnou* hodnotu.

## <a name="syntax"></a>Syntaxe

```vb
LEN (text)
```

## <a name="arguments"></a>Argumenty

`text`: *řetězec*

Hodnota typu *řetězec*, která představuje samotný text.

## <a name="return-values"></a>Vrácené hodnoty

*Celé číslo*

Výsledná číselná hodnota.

## <a name="example"></a>Příklad

`LEN ("Sample")` vrátí **6**.

## <a name="additional-resources"></a>Další zdroje

[Textové funkce](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
