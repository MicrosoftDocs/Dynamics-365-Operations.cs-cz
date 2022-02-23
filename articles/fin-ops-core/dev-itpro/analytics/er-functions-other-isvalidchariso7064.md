---
title: Funkce el. výkaznictví ISVALIDCHARACTERISO7064
description: Toto téma obsahuje obecné informace o použití funkce ISVALIDCHARACTERISO7064 elektronického výkaznictví.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3bceb15bbe1dc65abc88c1229459707a6166482
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680655"
---
# <a name="isvalidcharacteriso7064-er-function"></a>Funkce el. výkaznictví ISVALIDCHARACTERISO7064

[!include [banner](../includes/banner.md)]

Funkce `ISVALIDCHARACTERISO7064` vrátí *logickou hodnotu* **TRUE**, pokud zadaný řetězec představuje platné mezinárodní číslo bankovního účtu (IBAN). V opačném případě výraz vrátí *logickou hodnotu* **FALSE**.

## <a name="syntax"></a>Syntaxe

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a>Argumenty

`text`: *řetězec*

Textová hodnota, která představuje IBAN.

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná textová hodnota.

## <a name="example"></a>Příklad

`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` vrátí **TRUE**. 

`ISVALIDCHARACTERISO7064 ("AT61")` vrátí **FALSE**.

## <a name="additional-resources"></a>Další zdroje

[Další funkce (konkrétní pro obchodní domény)](er-functions-category-other.md)
