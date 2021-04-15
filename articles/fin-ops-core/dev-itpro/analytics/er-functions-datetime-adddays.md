---
title: Funkce el. výkaznictví ADDDAYS
description: Toto téma obsahuje obecné informace o použití funkce ADDDAYS elektronického výkaznictví.
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: 0c420daa04b8e22504d25d317c75826f1d1914b7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747052"
---
# <a name="adddays-er-function"></a>Funkce el. výkaznictví ADDDAYS

[!include [banner](../includes/banner.md)]

Funkce `ADDDAYS` vypočítá hodnotu *datum a čas*, která představuje zadaný počet dní před nebo po zadaném počátečním datu.

## <a name="syntax"></a>Syntaxe

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a>Argumenty

`datetime`: *datum a čas*

Hodnota data a času, která představuje počáteční datum.

`days`: *celé číslo*

Počet dnů před nebo po `datetime`.

## <a name="return-values"></a>Vrácené hodnoty

*Datum a čas*

Výsledná hodnota data a času.

## <a name="usage-notes"></a>Poznámky k použití

Kladná hodnota pro `days` znamená datum v budoucnosti. Záporná hodnota znamená datum v minulosti.

## <a name="example-1"></a>Příklad 1

`ADDDAYS (NOW(), 7)` vrátí datum a čas sedm dní v budoucnosti.

## <a name="example-2"></a>Příklad 2

`ADDDAYS (NOW(), -3)` vrátí datum a čas tři dny v minulosti.

## <a name="additional-resources"></a>Další zdroje

[Funkce data a času](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]