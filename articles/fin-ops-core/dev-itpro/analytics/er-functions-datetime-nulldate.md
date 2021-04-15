---
title: Funkce el. výkaznictví NULLDATE
description: Toto téma obsahuje obecné informace o použití funkce NULLDATE elektronického výkaznictví.
author: NickSelin
ms.date: 12/04/2019
ms.topic: article
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
ms.openlocfilehash: 6ac8da3f18c7793512685d52dd64a9bd55bfb8fc
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746836"
---
# <a name="nulldate-er-function"></a>Funkce el. výkaznictví NULLDATE

[!include [banner](../includes/banner.md)]

Funkce `NULLDATE` vrátí hodnotu typu *datum* představující hodnotu **null** data (1. leden 1900).

## <a name="syntax"></a>Syntaxe

```vb
NULLDATE () as 
```

## <a name="return-values"></a>Vrácené hodnoty

*Datum*

Výsledná hodnota data.

## <a name="example-1"></a>Příklad 1

`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` vrátí hodnotu **null** data, 1 leden 1900, jako **"1900-01-01"** na základě zadaného vlastního formátu.

## <a name="example-2"></a>Příklad 2

Výraz `IF( Invoice.DocumentDate = NULLDATE(), true, false)` vrátí hodnotu **True**, pokud se hodnota pole **DocumentDate** shoduje s hodnotou **null** data. V tomto příkladu **Invoice** představuje zdroj dat elektronického výkaznictví typu **záznamy Finance/Table** a odkazuje na tabulku CustInvoiceJour.

## <a name="additional-resources"></a>Další zdroje

[Funkce data a času](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]