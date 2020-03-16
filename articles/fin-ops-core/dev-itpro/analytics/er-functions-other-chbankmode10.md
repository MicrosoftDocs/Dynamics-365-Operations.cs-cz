---
title: Funkce el. výkaznictví CH_BANK_MOD_10
description: Toto téma obsahuje obecné informace o použití funkce CH_BANK_MOD_10 elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 808e328bfcc35c96091da9a69850429b82a71070
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070568"
---
# <a name="CH_BANK_MOD_10">Funkce el. výkaznictví CH_BANK_MOD_10</a>

[!include [banner](../includes/banner.md)]

Funkce `CH_BANK_MOD_10` vrátí hodnotu typu *řetězec*, která představuje referenční údaj věřitele jako výraz MOD10 na základě číslic zadaného čísla faktury.

## <a name="syntax"></a>Syntaxe

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a>Argumenty

`invoice number digits`: *řetězec*

Textová hodnota, která představuje číslice čísla faktury.

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná textová hodnota.

## <a name="example"></a>Příklad

`CH_BANK_MOD_10 ("VEND-200002")` vrátí **3**.

## <a name="additional-resources"></a>Další zdroje

[Další funkce (konkrétní pro obchodní domény)](er-functions-category-other.md)
