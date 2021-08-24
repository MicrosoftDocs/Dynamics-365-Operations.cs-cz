---
title: Funkce el. výkaznictví NULLDATETIME
description: Toto téma obsahuje obecné informace o použití funkce NULLDATETIME elektronického výkaznictví.
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
ms.openlocfilehash: 79bdcaa90ce4002d92a4a0d959c9b94d8c47d7c7c855584d49818fb713bda4b7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745227"
---
# <a name="nulldatetime-er-function"></a>Funkce el. výkaznictví NULLDATETIME

[!include [banner](../includes/banner.md)]

Funkce `NULLDATETIME` vrátí hodnotu typu *datum a čas*, která představuje hodnotu **null** data a času (1. leden 1900) v koordinovaném světovém čase (Greenwich Mean Time \[GMT\]).

## <a name="syntax"></a>Syntaxe

```vb
NULLDATETIME ()
```

## <a name="return-values"></a>Vrácené hodnoty

*Datum a čas*

Výsledná hodnota data a času.

## <a name="example"></a>Příklad

Funkce `DATETIMEFORMAT( NULLDATETIME(), "O")` vrátí řetězcovou hodnotu **1900-01-01T00:00:00.0000000+00:00**, pokud je volána během procesu, který byl iniciován uživatelem aplikace, který má hodnotu časového pásma **(GMT) Koordinovaný světový čas** v sekci **Předvolby jazyka a země/oblasti**.

## <a name="additional-resources"></a>Další zdroje

[Funkce data a času](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]