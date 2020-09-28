---
title: Funkce elektronického výkaznictví ISOCREDREF
description: Toto téma obsahuje obecné informace o použití funkce ISOCREDREF elektronického výkaznictví.
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
ms.openlocfilehash: d6e5d025e7de15c27b19711ea5b597d75bdf3d41
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744088"
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
