---
title: Funkce elektronického výkaznictví ISEMPTY
description: Tento článek obsahuje obecné informace o použití funkce ISEMPTY elektronického výkaznictví.
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
ms.openlocfilehash: 1d8c9a2195afbc76bc00f31778d087268b98279f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845511"
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