---
title: Funkce el. výkaznictví TABLENAME2ID
description: Toto téma obsahuje obecné informace o použití funkce TABLENAME2ID elektronického výkaznictví.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 0f94d00d9d40830d895e906ffbaa2a236f1efc43
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746548"
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