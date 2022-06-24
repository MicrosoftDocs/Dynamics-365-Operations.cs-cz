---
title: Funkce el. výkaznictví ISVALIDCHARACTERISO7064
description: Tento článek obsahuje obecné informace o použití funkce ISVALIDCHARACTERISO7064 elektronického výkaznictví.
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
ms.openlocfilehash: 43da66e79bd8fbeecf5a04283574077600552a05
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908467"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]