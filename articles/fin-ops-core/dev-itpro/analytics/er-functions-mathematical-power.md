---
title: Funkce elektronického výkaznictví POWER
description: Toto téma obsahuje obecné informace o použití funkce POWER elektronického výkaznictví.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 6955d2787b2a9be6d38fe10165a9d5ef8310b108e3a9772709d9d1ff51712424
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767137"
---
# <a name="power-er-function"></a>Funkce elektronického výkaznictví POWER

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]