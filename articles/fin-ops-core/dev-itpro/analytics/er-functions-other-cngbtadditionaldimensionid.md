---
title: Funkce el. výkaznictví CN_GBT_ADDITIONALDIMENSIONID
description: Toto téma obsahuje obecné informace o použití funkce CN_GBT_ADDITIONALDIMENSIONID elektronického výkaznictví.
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
ms.openlocfilehash: 9217b70076a369c18a94f820f19ca371c2d8aca61ab72b6be762592f39fa1160
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731538"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a>Funkce el. výkaznictví CN_GBT_ADDITIONALDIMENSIONID

[!include [banner](../includes/banner.md)]

Funkce `CN_GBT_ADDITIONALDIMENSIONID` vrací hodnotu typu *řetězec*, která představuje jedno ID dimenze financí, které je převzato ze zadaného řetězce. Zadaný řetězec představuje všechny dimenze jako seznam ID oddělených čárkami.

## <a name="syntax"></a>Syntaxe

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a>Argumenty

`text`: *řetězec*

Hodnota typu *řetězec*, která představuje všechny dimenze jako seznam ID oddělených čárkami.

`number`: celé číslo

Hodnota typu *celé číslo* definující kód sekvence požadované dimenze v zadaném řetězci.

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná textová hodnota.

## <a name="example"></a>Příklad

`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` vrátí **"CC"**.

## <a name="additional-resources"></a>Další zdroje

[Další funkce (konkrétní pro obchodní domény)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]