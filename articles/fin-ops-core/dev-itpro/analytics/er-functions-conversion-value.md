---
title: Funkce VALUE ER
description: Toto téma obsahuje obecné informace o použití funkce VALUE elektronického výkaznictví.
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
ms.openlocfilehash: 04d3320276bc1e23436bd9baa7a84da36314d6c3bf7f84694aa2e01e31230a0b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713935"
---
# <a name="value-er-function"></a>Funkce VALUE ER

[!include [banner](../includes/banner.md)]

Funkce `VALUE` vrací hodnotu *reálné číslo*, která je převedena ze zadaného řetězce.

## <a name="syntax"></a>Syntaxe

```vb
VALUE (text)
```

## <a name="arguments"></a>Argumenty

`text`: *řetězec*

Hodnota řetězce, která musí být převedena na číselnou hodnotu.

## <a name="return-values"></a>Vrácené hodnoty

*Reálný*

Výsledná číselná hodnota.

## <a name="usage-notes"></a>Poznámky k použití

Čárky a tečky (.) jsou považovány za oddělovače desetinných míst a úvodní spojovník (-) se používá jako záporné znaménko. Pokud jsou v zadaném řetězci obsaženy jiné než číselné znaky, je vyvolána výjimka v době běhu.

## <a name="example-1"></a>Příklad 1

`VALUE ("1 234,56")` zahodí výjimku.

## <a name="example-2"></a>Příklad 2

`VALUE ("1234,56")` vrací **1234.56**.

## <a name="additional-resources"></a>Další zdroje

[Funkce převodu typu](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]