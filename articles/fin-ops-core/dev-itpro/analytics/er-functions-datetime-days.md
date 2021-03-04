---
title: Funkce el. výkaznictví DAYS
description: Toto téma obsahuje obecné informace o použití funkce DAYS elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 66398e624e4b9d69d4dc3ccf3ee8f97758f4f861
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682334"
---
# <a name="days-er-function"></a>Funkce el. výkaznictví DAYS

[!include [banner](../includes/banner.md)]

Funkce `DAYS` vrátí hodnotu typu *celé číslo*, které představuje počet dní mezi jedním a druhým zadaným datem.

## <a name="syntax"></a>Syntaxe

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a>Argumenty

`date 1`: *datum*

Hodnota kalendářního data, která představuje počáteční datum pro výpočet počtu dní.

`date 2`: *datum*

Hodnota kalendářního data, která představuje koncové datum pro výpočet počtu dní.

## <a name="return-values"></a>Vrácené hodnoty

*Celé číslo*

Výsledná číselná hodnota.

## <a name="usage-notes"></a>Poznámky k použití

Funkce `DAYS` vrátí kladnou hodnotu, pokud je první datum pozdější než druhé datum, vrátí **0** (nulu), když se první datum shoduje s druhým datem, nebo vrátí zápornou hodnotu, když je první datum dřívější než druhé.

## <a name="example"></a>Příklad

`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` vrací **-1**.

## <a name="additional-resources"></a>Další zdroje

[Funkce data a času](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]