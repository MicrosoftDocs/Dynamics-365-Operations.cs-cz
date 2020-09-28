---
title: Funkce el. výkaznictví TABLENAME2ID
description: Toto téma obsahuje obecné informace o použití funkce TABLENAME2ID elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: d9f9e38f46df8a93b5cb16b8d0d5e5afbff8558a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743992"
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
