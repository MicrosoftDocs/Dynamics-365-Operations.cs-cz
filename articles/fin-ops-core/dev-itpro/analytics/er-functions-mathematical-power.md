---
title: Funkce elektronického výkaznictví POWER
description: Toto téma obsahuje obecné informace o použití funkce POWER elektronického výkaznictví.
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
ms.openlocfilehash: c57222d7fcc133faa679bab43431272c984c9d8b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041623"
---
# <a name="POWER">Funkce elektronického výkaznictví POWER</a>

[!include [banner](../includes/banner.md)]

Funkce `POWER` vrací hodnotu typu *reálné číslo*, která představuje výsledek umocnění zadaného kladného čísla dle zadané mocniny.

## <a name="syntax"></a>Syntaxe

```vb
POWER (number, power)
```

## <a name="arguments"></a>Argumenty

`number`: *reálné číslo* nebo *celé číslo*

Číselná hodnota, která musí být umoceněna dle zadané mocniny.

`power`: *reálné číslo* nebo *celé číslo*

Číselná hodnota, která představuje zadanou mocninu.

## <a name="return-values"></a>Vrácené hodnoty

*Reálný*

Výsledná číselná hodnota.

## <a name="example-1"></a>Příklad 1

`POWER (10, 2)` vrátí **100**.

## <a name="example-2"></a>Příklad 2

`POWER (4, 0.5)` vrátí **2**.

## <a name="additional-resources"></a>Další zdroje

[Matematické funkce](er-functions-category-mathematical.md)
