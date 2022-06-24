---
title: Funkce el. výkaznictví OR
description: Tento článek obsahuje obecné informace o použití funkce OR elektronického výkaznictví.
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
ms.openlocfilehash: d2783b5aff34e6ab4b5bde5dfe39e92d20892634
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892944"
---
# <a name="or-er-function"></a>Funkce el. výkaznictví OR

[!include [banner](../includes/banner.md)]

Funkce `OR` vrátí *logickou hodnotu* **FALSE**, pokud nejsou splněny všechny zadané podmínky. Tato funkce vrátí *logickou* hodnotu **PRAVDA**, pokud je splněna libovolná uvedená podmínka.

## <a name="syntax"></a>Syntaxe

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>Argumenty

`condition 1`: *logická hodnota*

Platný podmíněný výraz, který má být testován. Tento argument je povinný.

`condition N`: *logická hodnota*

Platný podmíněný výraz, který má být testován. Tyto další argumenty jsou nepovinné.

## <a name="return-values"></a>Vrácené hodnoty

*Logická hodnota*

Výsledná *logická hodnota*.

## <a name="example"></a>Příklad

`OR (1=2, "a"="a")` vrátí **TRUE**.

## <a name="additional-resources"></a>Další zdroje

[Logické funkce](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]