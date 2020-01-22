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
ms.openlocfilehash: dd1290538c506cd0db6eb21a304ff9812c808f17
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916446"
---
# <a name="ADDDAYS">Funkce el. výkaznictví ADDDAYS</a>

[!include [banner](../includes/banner.md)]

Funkce `ADDDAYS` vypočítá hodnotu *datum a čas*, která představuje zadaný počet dní před nebo po zadaném počátečním datu.

## <a name="syntax"></a>Syntaxe

```
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
