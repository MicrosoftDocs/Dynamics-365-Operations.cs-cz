---
title: Funkce el. výkaznictví CONCATENATE
description: Toto téma obsahuje obecné informace o použití funkce CONCATENATE elektronického výkaznictví.
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
ms.openlocfilehash: 1507e1b8a31ed45e7c540e4e2ff31b79e8de3b866ffbace9de17d7b3e169e877
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762493"
---
# <a name="concatenate-er-function"></a>Funkce el. výkaznictví CONCATENATE

[!include [banner](../includes/banner.md)]

Funkce `CONCATENATE` vrátí všechny zadané textové řetězce jako hodnotu typu *řetězec* poté, co byly spojeny do jednoho řetězce.

## <a name="syntax"></a>Syntaxe

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a>Argumenty

`text 1`: *řetězec*

Odkaz na zdroj dat datového typu *řetězec*. Tento argument je povinný.

`text N`: *řetězec*

Odkaz na zdroj dat datového typu *řetězec*. Tyto další argumenty jsou nepovinné.

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná textová hodnota.

## <a name="example"></a>Příklad

`CONCATENATE ("abc", "def")` vrátí **"abcdef"**.

## <a name="usage-notes"></a>Poznámky k použití

Výraz `"abc" & "def"` vrátí též **"abcdef"**.

## <a name="additional-resources"></a>Další zdroje

[Textové funkce](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]