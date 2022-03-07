---
title: Funkce elektronického výkaznictví ROUNDAMOUNT
description: Toto téma obsahuje obecné informace o použití funkce ROUNDAMOUNT elektronického výkaznictví.
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
ms.openlocfilehash: 1b05c6024d9eeecfe74022df10d793055a026d5a159e9c011f37708f6a4e6e0d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770854"
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