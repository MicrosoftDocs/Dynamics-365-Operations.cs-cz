---
title: Funkce elektronického výkaznictví RIGHT
description: Toto téma obsahuje obecné informace o použití funkce RIGHT elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 7169d9d3d2cdfb9f36bb77c1688922549e79ff32
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040864"
---
# <a name="RIGHT">Funkce elektronického výkaznictví RIGHT</a>

[!include [banner](../includes/banner.md)]

Funkce `RIGHT` vrací hodnotu typu *řetězec*, která představuje zadaný počet znaků od konce zadaného řetězce.

## <a name="syntax"></a>Syntaxe

```vb
RIGHT (text, number)
```

## <a name="arguments"></a>Argumenty

`text`: *řetězec*

Hodnota typu *řetězec*, která představuje původní text.

`number`: *celé číslo*

Počet znaků, které mají být vráceny od konce původního textu.

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná textová hodnota.

## <a name="example"></a>Příklad

`RIGHT ("Sample", 3)` vrátí **"ple"**.

## <a name="additional-resources"></a>Další zdroje

[Textové funkce](er-functions-category-text.md)
