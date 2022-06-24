---
title: Funkce el. výkaznictví MOD_97
description: Tento článek obsahuje obecné informace o použití funkce MOD_97 elektronického výkaznictví.
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
ms.openlocfilehash: f57b55a9c4182b411e098ebce2f36b78ef03b6f8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898426"
---
# <a name="mod_97-er-function"></a>Funkce el. výkaznictví MOD_97

[!include [banner](../includes/banner.md)]

Funkce `MOD_97` vrátí hodnotu typu *řetězec*, která představuje referenční údaj věřitele jako výraz MOD97 na základě číslic zadaného čísla faktury.

## <a name="syntax"></a>Syntaxe

```vb
MOD_97 (invoice number digits)
```

## <a name="arguments"></a>Argumenty

`invoice number digits`: *řetězec*

Textová hodnota, která představuje číslice čísla faktury.

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná textová hodnota.

## <a name="example"></a>Příklad

`MOD_97 ("VEND-200002")` vrátí **"20000285"**.

## <a name="additional-resources"></a>Další zdroje

[Další funkce (konkrétní pro obchodní domény)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]