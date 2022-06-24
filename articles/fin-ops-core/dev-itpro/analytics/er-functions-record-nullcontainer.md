---
title: Funkce elektronického výkaznictví NULLCONTAINER
description: Tento článek obsahuje obecné informace o použití funkce NULLCONTAINER elektronického výkaznictví.
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
ms.openlocfilehash: 8da2a30cf2839adabf7b5ea4916f44999aa05758
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850951"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]