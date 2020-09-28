---
title: Funkce el. výkaznictví ADDDAYS
description: Toto téma obsahuje obecné informace o použití funkce ADDDAYS elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 998cf2c0dac67040814d4a32e433b465ec51f88c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743368"
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
