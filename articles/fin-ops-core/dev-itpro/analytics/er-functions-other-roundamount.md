---
title: Funkce elektronického výkaznictví ROUNDAMOUNT
description: Tento článek obsahuje obecné informace o použití funkce ROUNDAMOUNT elektronického výkaznictví.
author: kfend
ms.date: 12/17/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 0e4de43f865ca21822ab2c0c345026d2e9113ca2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286022"
---
# <a name="roundamount-er-function"></a>Funkce elektronického výkaznictví ROUNDAMOUNT

[!include [banner](../includes/banner.md)]

Funkce `ROUNDAMOUNT` vrátí hodnotu typu *reálné číslo* jako výsledek zaokrouhlení zadaného čísla na nejbližší násobek jiného čísla podle zadaného pravidla zaokrouhlení.

## <a name="syntax"></a>Syntaxe

```vb
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a>Argumenty

`number`: *celé číslo* nebo *reálné číslo*

Číselná hodnota, která má být zaokrouhlena.

`decimals`: *celé číslo* nebo *reálné číslo*

Číslo, na jehož násobek má být zaokrouhlena hodnota parametru `number`.

`round rule`: *hodnota výčtu*

Výčtová hodnota výčtu **RoundOffType**, která definuje pravidlo zaokrouhlení. Tento výčet nabízí následující hodnoty:

- Normální (Ordinary)
- Zaokrouhlení dolů (RoundDown)
- Zaokrouhlení nahoru (RoundUp)

## <a name="return-values"></a>Vrácené hodnoty

*Reálný*

Výsledná číselná hodnota je násobkem hodnoty určené parametrem `decimals` a je nejblíže hodnotě určené parametrem `number`.

## <a name="usage-notes"></a>Poznámky k použití

Pokud je parametr `number` nulový, vrátí funkce vždy nulu.

Pokud je parametr `decimals` nulový, zaokrouhlí tato funkce na výchozí hodnotu zaokrouhlení. Pokud je parametr `round rule` nastaven na **RoundOffType.Ordinary**, výchozí hodnota zaokrouhlení bude **0,01**. V opačném případě je výchozí hodnota zaokrouhlení **1,0**.

Pokud je parametr `round rule` nastaven na hodnotu **RoundOffType.Ordinary**, tato funkce jej zaokrouhlí na nejbližší zaokrouhlenou částku.

Pokud je parametr `round rule` nastaven na hodnotu **RoundOffType.RoundDown**, tato funkce zaokrouhlí směrem k nule na nejbližší zaokrouhlenou částku.

Pokud je parametr `round rule` nastaven na hodnotu **RoundOffType.RoundUp**, tato funkce zaokrouhlí směrem od nuly na nejbližší zaokrouhlenou částku.

Pokud je parametr `round rule` nastaven na **RoundOffType.Ordinary**, tato funkce se zachová podobně jako funkce aplikace Excel [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) a X++ [Round](../dev-ref/xpp-math-run-time-functions.md#round).

## <a name="remarks"></a>Poznámky

Chcete-li zaokrouhlit číselnou hodnotu na zadaný počet desetinných míst, použijte funkci [ROUND](er-functions-mathematical-round.md).

## <a name="example"></a>Příklad

Pokud je parametr **model.RoundOff** nastaven na **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` vrátí 7,35. 

Pokud je parametr **model.RoundOff** nastaven na **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` vrátí 7,35. 

Pokud je parametr **model.RoundOff** nastaven na **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` vrátí 8,4.

## <a name="additional-resources"></a>Další zdroje

[Další funkce (konkrétní pro obchodní domény)](er-functions-category-other.md)

[Matematické funkce](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
