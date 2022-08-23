---
title: Funkce el. výkaznictví ABS
description: Tento článek obsahuje obecné informace o použití funkce ABS elektronického výkaznictví.
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: a8d0fe68232d9dd27d9ba0cc6b81c7708d22711e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272551"
---
# <a name="abs-er-function"></a>Funkce el. výkaznictví ABS

[!include [banner](../includes/banner.md)]

Funkce `ABS` vrací absolutní hodnotu (modul) zadaného čísla jako hodnotu typu *reálné číslo*. Jinými slovy, vrací číslo bez znaménka.

## <a name="syntax"></a>Syntaxe

```vb
ABS (number)
```

## <a name="arguments"></a>Argumenty

`number`: *reálné číslo*

Číselná hodnota, ze které chceme získat modul.

## <a name="return-values"></a>Vrácené hodnoty

*Reálný*

Výsledná číselná hodnota.

## <a name="example"></a>Příklad

`ABS (-1)` vrátí **1**.

## <a name="additional-resources"></a>Další zdroje

[Matematické funkce](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
