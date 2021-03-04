---
title: Funkce el. výkaznictví GUIDVALUE
description: Toto téma obsahuje obecné informace o použití funkce GUIDVALUE elektronického výkaznictví.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eb6f301cf7a39208aa23337401a9684fb5b3a73d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685947"
---
# <a name="guidvalue-er-function"></a>Funkce el. výkaznictví GUIDVALUE

[!include [banner](../includes/banner.md)]

Funkce `GUIDVALUE` převede zadaný vstup datového typu *řetězec* na datovou položku datového typu *GUID*.

## <a name="syntax"></a>Syntaxe

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a>Argumenty

`input`: *řetězec*

Platná cesta ke zdroji dat typu *řetězec*.

## <a name="return-values"></a>Vrácené hodnoty

*GUID*

Výsledná hodnota globálně jedinečného identifikátoru (GUID).

## <a name="usage-notes"></a>Poznámky k použití

Pro převod opačným směrem (to znamená převod zadaného vstupu datového typu *GUID* na datovou položku datového typu *řetězec*) lze použít funkci [TEXT](er-functions-text-text.md).

## <a name="example"></a>Příklad

Definujte v mapování modelu následující zdroje dat:

- Zdroj dat **myID** typu *vypočítané pole*, který obsahuje výraz `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`
- Zdroj dat **Users** typu *záznamy tabulky*, který odkazuje na tabulku UserInfo

Potom můžete použít výraz jako `FILTER (Users, Users.objectId = myID)` pro filtrování tabulky UserInfo podle pole **objectId** datového typu *GUID*.

## <a name="additional-resources"></a>Další zdroje

[Textové funkce](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]