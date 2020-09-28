---
title: Funkce el. výkaznictví TEXT
description: Toto téma obsahuje obecné informace o použití funkce TEXT elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 20313133ce29b8d5048814ff78ce4ea4f5c54d4a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743681"
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
