---
title: Funkce elektronického výkaznictví NULLCONTAINER
description: Toto téma obsahuje obecné informace o použití funkce NULLCONTAINER elektronického výkaznictví.
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
ms.openlocfilehash: dac6283ec35d3d03f586ca157048bd3ecc4bfa8a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743920"
---
# <a name="nullcontainer-er-function"></a>Funkce elektronického výkaznictví NULLCONTAINER

[!include [banner](../includes/banner.md)]

Funkce `NULLCONTAINER` vrací prázdnou hodnotu typu *kontejner (záznam)*, která má stejnou strukturu jako zadaný seznam záznamů nebo záznam.

## <a name="syntax"></a>Syntaxe

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a>Argumenty

`list`: *seznam záznamů* nebo *kontejner (záznam)*

Platná cesta ke zdroji dat buď typu *seznam záznamů* nebo *kontejner (záznam)*.

## <a name="return-values"></a>Vrácené hodnoty

*Kontejner (záznam)*

Výsledná hodnota atributu.

## <a name="usage-notes"></a>Poznámky k použití

> [!NOTE] 
> Tato funkce je zastaralá. Místo toho použijte funkci `EMPTYRECORD`. Další informace naleznete v tématu [EMPTYRECORD](er-functions-record-emptyrecord.md).

## <a name="example"></a>Příklad

`NULLCONTAINER (SPLIT ("abc", 1))` vrátí nový prázdný záznam, který má stejnou strukturu jako seznam vrácený funkcí `SPLIT`. Další informace naleznete v tématu [SPLIT](er-functions-list-split.md)

## <a name="additional-resources"></a>Další zdroje

[Funkce záznamu](er-functions-category-record.md)
