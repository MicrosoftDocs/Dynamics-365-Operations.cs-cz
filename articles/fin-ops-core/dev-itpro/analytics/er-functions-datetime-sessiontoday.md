---
title: Funkce elektronického výkaznictví SESSIONTODAY
description: Toto téma obsahuje obecné informace o použití funkce SESSIONTODAY elektronického výkaznictví.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: caadfbe9d82c967b84abd362211a2ecec1bdd0481c7f3907816b7aec23883175
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756470"
---
# <a name="sessiontoday-er-function"></a>Funkce elektronického výkaznictví SESSIONTODAY

[!include [banner](../includes/banner.md)]

Funkce `SESSIONTODAY` vrátí hodnotu typu *datum*, která představuje aktuální datum relace aplikace.

## <a name="syntax"></a>Syntaxe

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a>Vrácené hodnoty

*Datum*

Výsledná hodnota data.

## <a name="example"></a>Příklad

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` vrátí aktuální datum relace aplikace, 24. prosince 2015, jako řetězec **"24-12-2015"** na základě vybrané německé jazykové verze a zadaného formátu.

## <a name="additional-resources"></a>Další zdroje

[Funkce data a času](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]