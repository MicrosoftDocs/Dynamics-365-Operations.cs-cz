---
title: Funkce elektronického výkaznictví SESSIONTODAY
description: Toto téma obsahuje obecné informace o použití funkce SESSIONTODAY elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: bcfb36d6e3fb8475546f7cfb420c4aca848ac896
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917458"
---
# <a name="SESSIONTODAY">Funkce elektronického výkaznictví SESSIONTODAY</a>

[!include [banner](../includes/banner.md)]

Funkce `SESSIONTODAY` vrátí hodnotu typu *datum*, která představuje aktuální datum relace aplikace.

## <a name="syntax"></a>Syntaxe

```
SESSIONTODAY ()
```

## <a name="return-values"></a>Vrácené hodnoty

*Datum*

Výsledná hodnota data.

## <a name="example"></a>Příklad

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` vrátí aktuální datum relace aplikace, 24. prosince 2015, jako řetězec **"24-12-2015"** na základě vybrané německé jazykové verze a zadaného formátu.

## <a name="additional-resources"></a>Další zdroje

[Funkce data a času](er-functions-category-datetime.md)
