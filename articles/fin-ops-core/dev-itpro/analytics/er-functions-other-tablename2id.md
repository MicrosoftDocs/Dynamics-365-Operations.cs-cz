---
title: Funkce el. výkaznictví TABLENAME2ID
description: Tento článek obsahuje obecné informace o použití funkce TABLENAME2ID elektronického výkaznictví.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: b5deea69d5c43be599ccf02c0344ba8d662a6e0f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886842"
---
# <a name="tablename2id-er-function"></a>Funkce el. výkaznictví TABLENAME2ID

[!include [banner](../includes/banner.md)]

Funkce `TABLENAME2ID` vrátí číselnou reprezentaci ID tabulky pro zadaný název tabulky jako *celočíselnou* hodnotu.

## <a name="syntax"></a>Syntaxe

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a>Argumenty

`text`: *řetězec*

Textová hodnota, která představuje platný název tabulky.

## <a name="return-values"></a>Vrácené hodnoty

*Celé číslo*

Výsledná číselná hodnota.

## <a name="usage-notes"></a>Poznámky k použití

Spuštění této funkce může mít různé výsledky v různých instancích aplikace Microsoft Dynamics 365 Finance, i když je použit stejný název společnosti.

## <a name="example"></a>Příklad

`TABLENAME2ID ("Intrastat")` vrátí **1510**.

## <a name="additional-resources"></a>Další zdroje

[Další funkce (konkrétní pro obchodní domény)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]