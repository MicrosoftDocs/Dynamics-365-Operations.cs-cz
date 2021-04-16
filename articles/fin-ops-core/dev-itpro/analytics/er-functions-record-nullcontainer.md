---
title: Funkce elektronického výkaznictví NULLCONTAINER
description: Toto téma obsahuje obecné informace o použití funkce NULLCONTAINER elektronického výkaznictví.
author: NickSelin
ms.date: 12/12/2019
ms.topic: article
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
ms.openlocfilehash: af6651ef3c62bd8d1285fa8179ac923d3c333ce7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746500"
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