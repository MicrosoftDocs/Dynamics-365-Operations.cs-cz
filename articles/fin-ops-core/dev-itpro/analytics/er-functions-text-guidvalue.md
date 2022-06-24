---
title: Funkce el. výkaznictví GUIDVALUE
description: Tento článek obsahuje obecné informace o použití funkce GUIDVALUE elektronického výkaznictví.
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
ms.openlocfilehash: f3899d983f7c790ff2e3dc74dd91c44fc54e44d3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898733"
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