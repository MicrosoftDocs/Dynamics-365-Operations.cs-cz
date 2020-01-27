---
title: Funkce VALUE ER
description: Toto téma obsahuje obecné informace o použití funkce VALUE elektronického výkaznictví.
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
ms.openlocfilehash: 160dd81baa43702b2deea1e3eea20080fca122ca
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917619"
---
# <a name="VALUE">Funkce VALUE ER</a>

[!include [banner](../includes/banner.md)]

Funkce `VALUE` vrací hodnotu *reálné číslo*, která je převedena ze zadaného řetězce.

## <a name="syntax"></a>Syntaxe

```
VALUE (text)
```

## <a name="arguments"></a>Argumenty

`text`: *řetězec*

Hodnota řetězce, která musí být převedena na číselnou hodnotu.

## <a name="return-values"></a>Vrácené hodnoty

*Reálný*

Výsledná číselná hodnota.

## <a name="usage-notes"></a>Poznámky k použití

Čárky a tečky (.) jsou považovány za oddělovače desetinných míst a úvodní spojovník (-) se používá jako záporné znaménko. Pokud jsou v zadaném řetězci obsaženy jiné než číselné znaky, je vyvolána výjimka v době běhu.

## <a name="example-1"></a>Příklad 1

`VALUE ("1 234,56")` zahodí výjimku.

## <a name="example-2"></a>Příklad 2

`VALUE ("1234,56")` vrací **1234.56**.

## <a name="additional-resources"></a>Další zdroje

[Funkce převodu typu](er-functions-category-type-conversion.md)
