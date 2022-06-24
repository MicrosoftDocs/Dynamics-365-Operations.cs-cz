---
title: Funkce elektronického výkaznictví SESSIONNOW
description: Tento článek obsahuje obecné informace o použití funkce SESSIONNOW elektronického výkaznictví.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 586d49a1fbbbcab7b0cd41c31daf0f50598754c2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884192"
---
# <a name="sessionnow-er-function"></a>Funkce elektronického výkaznictví SESSIONNOW

[!include [banner](../includes/banner.md)]

Funkce `SESSIONNOW` vrátí hodnotu typu *datum a čas*, která představuje aktuální datum a čas relace aplikace.

## <a name="syntax"></a>Syntaxe

```vb
SESSIONNOW ()
```

## <a name="return-values"></a>Vrácené hodnoty

*Datum a čas*

Výsledná hodnota data a času.

## <a name="example"></a>Příklad

`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` vrátí aktuální datum a čas relace aplikace, 24. prosince 2015, jako **"24.12.2015"** na základě vybrané německé jazykové verze a zadaného formátu.

## <a name="additional-resources"></a>Další zdroje

[Funkce data a času](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]