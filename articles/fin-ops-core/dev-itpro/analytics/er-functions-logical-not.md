---
title: Funkce el. výkaznictví NOT
description: Tento článek obsahuje obecné informace o použití funkce NOT elektronického výkaznictví.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: da30e9a0092f594da7cef7b425e2b89af7bda491
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890478"
---
# <a name="not-er-function"></a>Funkce el. výkaznictví NOT

[!include [banner](../includes/banner.md)]

Funkce `NOT` vrací stornovanou logickou hodnotu zadané podmínky jako *logickou hodnotu*.

## <a name="syntax"></a>Syntaxe

```vb
NOT (condition)
```

## <a name="arguments"></a>Argumenty

`condition`: *logická hodnota*

Platný podmíněný výraz, který má být stornován.

## <a name="return-values"></a>Vrácené hodnoty

*Logická hodnota*

Výsledná *logická hodnota*.

## <a name="example"></a>Příklad

`NOT (TRUE)` vrátí **FALSE**.

## <a name="additional-resources"></a>Další zdroje

[Logické funkce](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]