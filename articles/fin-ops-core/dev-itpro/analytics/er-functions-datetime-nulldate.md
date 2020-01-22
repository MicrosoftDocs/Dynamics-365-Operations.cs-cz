---
title: Funkce el. výkaznictví NULLDATE
description: Toto téma obsahuje obecné informace o použití funkce NULLDATE elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7761342c6759c11591e06fc7c32f0ddd8bef407a
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916308"
---
# <a name="NULLDATE">Funkce el. výkaznictví NULLDATE</a>

[!include [banner](../includes/banner.md)]

Funkce `NULLDATE` vrátí hodnotu typu *datum* představující hodnotu **null** data (1. leden 1900).

## <a name="syntax"></a>Syntaxe

```
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
