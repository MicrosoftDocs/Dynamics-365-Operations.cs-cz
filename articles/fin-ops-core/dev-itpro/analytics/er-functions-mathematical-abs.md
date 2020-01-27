---
title: Funkce el. výkaznictví ABS
description: Toto téma obsahuje obecné informace o použití funkce ABS elektronického výkaznictví.
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
ms.openlocfilehash: 9b32c5e8a413be3583177f565e2d4909330ad1e0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917090"
---
# <a name="ABS">Funkce el. výkaznictví ABS</a>

[!include [banner](../includes/banner.md)]

Funkce `ABS` vrací absolutní hodnotu (modul) zadaného čísla jako hodnotu typu *reálné číslo*. Jinými slovy, vrací číslo bez znaménka.

## <a name="syntax"></a>Syntaxe

```
ABS (number)
```

## <a name="arguments"></a>Argumenty

`number`: *reálné číslo*

Číselná hodnota, ze které chceme získat modul.

## <a name="return-values"></a>Vrácené hodnoty

*Reálný*

Výsledná číselná hodnota.

## <a name="example"></a>Příklad

`ABS (-1)` vrátí **1**.

## <a name="additional-resources"></a>Další zdroje

[Matematické funkce](er-functions-category-mathematical.md)
