---
title: Funkce elektronického výkaznictví ISOCREDREF
description: Toto téma obsahuje obecné informace o použití funkce ISOCREDREF elektronického výkaznictví.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 51adc6392b07ba4061a475f3072fb35452f15ad2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748310"
---
# <a name="isocredref-er-function"></a>Funkce elektronického výkaznictví ISOCREDREF

[!include [banner](../includes/banner.md)]

Funkce `ISOCREDREF` vrátí hodnotu typu *řetězec*, která představuje ISO údaj věřitele na základě číslic a abecedních symbolů zadaného čísla faktury.

## <a name="syntax"></a>Syntaxe

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a>Argumenty

`invoice number digits`: *řetězec*

Textová hodnota, která představuje číslice čísla faktury.

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná textová hodnota.

## <a name="usage-notes"></a>Poznámky k použití

> [!NOTE] 
> Chcete-li vyloučit z abecedy symboly, které nejsou v souladu se standardem ISO, argument `invoice number digits` musí být přeložen před jeho předáním této funkci.

## <a name="example"></a>Příklad

`ISOCredRef ("VEND-200002")` vrátí **"RF23VEND-200002"**.

## <a name="additional-resources"></a>Další zdroje

[Další funkce (konkrétní pro obchodní domény)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]