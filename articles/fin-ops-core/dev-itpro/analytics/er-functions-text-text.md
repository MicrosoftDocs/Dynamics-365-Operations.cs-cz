---
title: Funkce el. výkaznictví TEXT
description: Tento článek obsahuje obecné informace o použití funkce TEXT elektronického výkaznictví.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: bf9049463ca905952cab512884afad380b7b3d52
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900157"
---
# <a name="text-er-function"></a>Funkce el. výkaznictví TEXT

[!include [banner](../includes/banner.md)]

Funkce `TEXT` vrátí zadané číslo jako hodnotu typu *řetězec* poté, co bylo převedeno na textový řetězec naformátovaný podle nastavení národního prostředí jazyka stávající instance aplikace.

## <a name="syntax"></a>Syntaxe

```vb
TEXT (number)
```

## <a name="arguments"></a>Argumenty

`number`: *celé číslo* nebo *reálné číslo*

Číslo, které mí být převedeno na textový řetězec.

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná textová hodnota.

## <a name="usage-notes"></a>Poznámky k použití

Co se týká hodnot typu *reálné číslo*, převod řetězce je omezen na dvě desetinná místa.

## <a name="example"></a>Příklad

Jestliže je národní prostředí instance Microsoft Dynamics 365 Finance definováno jako **EN-US**, `TEXT (NOW ())` vrátí aktuální datum relace Finance, December 17, 2015, jako textový řetězec **"12/17/2015 07:59:23 AM"**. `TEXT (1/3)` vrátí **"0.33"**.

## <a name="additional-resources"></a>Další zdroje

[Textové funkce](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]