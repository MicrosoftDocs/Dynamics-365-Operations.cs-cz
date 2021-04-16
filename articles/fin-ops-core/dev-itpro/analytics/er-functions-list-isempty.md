---
title: Funkce elektronického výkaznictví ISEMPTY
description: Toto téma obsahuje obecné informace o použití funkce ISEMPTY elektronického výkaznictví.
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
ms.openlocfilehash: 9c33e8b613bf5bf5bc17a42a7668d4cc4ee58e53
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750429"
---
# <a name="isempty-er-function"></a>Funkce elektronického výkaznictví ISEMPTY

[!include [banner](../includes/banner.md)]

Funce `ISEMPTY` vrátí *logickou hodnotu* **TRUE**, pokud zadaný seznam neobsahuje žádné záznamy. V opačném případě výraz vrátí *logickou hodnotu* **FALSE**.

## <a name="syntax"></a>Syntaxe

```vb
ISEMPTY (list)
```

## <a name="arguments"></a>Argumenty

`list`: *seznam záznamů*

Platná cesta ke zdroji dat typu *seznam záznamů*.

## <a name="return-values"></a>Vrácené hodnoty

*Logická hodnota*

Výsledná *logická hodnota*.

## <a name="example-1"></a>Příklad 1

Pokud zadáte zdroj dat **DS** typu *vypočítané pole* a ten obsahuje výraz `SPLIT ("A|B|C", "|")`, výraz `ISEMPTY(DS)` vrátí hodnotu **"FALSE"**.

## <a name="example-2"></a>Příklad 2

Výraz `ISEMPTY (SPLIT ("",1))` vrátí hodnotu **TRUE**.

## <a name="additional-resources"></a>Další zdroje

[Funkce seznamu](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]