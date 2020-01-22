---
title: Funkce el. výkaznictví AND
description: Toto téma obsahuje obecné informace o použití funkce AND elektronického výkaznictví.
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
ms.openlocfilehash: dd9c0ed0238009f70ad7a9bf5a5e19ebfb95cccc
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917159"
---
# <a name="AND">Funkce el. výkaznictví AND</a>

[!include [banner](../includes/banner.md)]

Funce `AND` vrátí *logickou hodnotu* **TRUE**, jsou-li splněny všechny zadané podmínky. V opačném případě výraz vrátí *logickou hodnotu* **FALSE**.

## <a name="syntax"></a>Syntaxe

```
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>Argumenty

`condition 1`: *logická hodnota*

Platný podmíněný výraz, který má být testován. Tento argument je povinný.

`condition N`: *logická hodnota*

Platný podmíněný výraz, který má být testován. Tyto další argumenty jsou nepovinné.

## <a name="return-values"></a>Vrácené hodnoty

*Logická hodnota*

Výsledná *logická hodnota*.

## <a name="usage-notes"></a>Poznámky k použití

V argumentech logických funkcí můžete použít odkazy na zdroje dat, číselné a textové hodnoty, logické hodnoty, relační operátory a jiné funkce elektronického výkaznictví (ER). Všechny argumenty je však nutné vyhodnotit na *logickou hodnotu* **TRUE** nebo **FALSE**.

## <a name="example"></a>Příklad

`AND (1=1, "a"="a")` vrátí **TRUE**.

`AND (1=2, "a"="a")` vrátí **FALSE**.

## <a name="additional-resources"></a>Další zdroje

[Logické funkce](er-functions-category-logical.md)
