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
ms.openlocfilehash: 77d889f75f38b3c07855a96bf65f1456ac2f42e2
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915802"
---
# <a name="TABLENAME2ID">Funkce el. výkaznictví TABLENAME2ID</a>

[!include [banner](../includes/banner.md)]

Funkce `TABLENAME2ID` vrátí číselnou reprezentaci ID tabulky pro zadaný název tabulky jako *celočíselnou* hodnotu.

## <a name="syntax"></a>Syntaxe

```
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
