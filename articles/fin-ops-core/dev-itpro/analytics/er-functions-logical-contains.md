---
title: Funkce ER CONTAINS
description: Toto téma obsahuje obecné informace o použití funkce CONTAINS elektronického výkaznictví.
author: NickSelin
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: a31d89f036a6e821bea2b6733c0c646145d2a47c
ms.sourcegitcommit: 17cee26b03f7b5afe8a089a0a9b2380e8d377d70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2021
ms.locfileid: "6048863"
---
# <a name="contains-er-function"></a>Funkce ER CONTAINS

[!include [banner](../includes/banner.md)]

Funkce `CONTAINS` určuje, zda zadaný vstup obsahuje zadaný text. Vrací *logickou* hodnotu **TRUE**, pokud zadaný vstup obsahuje zadaný text. V opačném případě výraz vrátí *logickou hodnotu* **FALSE**.

## <a name="syntax"></a>Syntaxe

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a>Argumenty

`input`: *řetězec*

Platná cesta k položce zdroje dat z typu *Řetězec* nebo řetězcová konstanta, jejíž hodnota může obsahovat druhý argument.

`search text`: *řetězec*

Platná cesta k zdroje dat z typu dat *Řetězec* nebo řetězcová konstanta, jejíž hodnota může být obsažena v prvním argumentu.

## <a name="return-values"></a>Vrácené hodnoty

*Logická*

Výsledná *logická hodnota*.

## <a name="usage-notes"></a>Poznámky k použití

Tuto funkci lze použít k určení podmínkového výrazu funkce [FILTER](er-functions-list-filter.md) pouze v případě, že je příslušné mapování nakonfigurováno v [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) pro přístup k [Microsoft Dataverse](/power-platform/admin/data-integrator). Jinak je v době návrhu vyvolána výjimka. Zpráva, kterou obdržíte, doporučuje použít funkci [WHERE](er-functions-list-where.md) namísto funkce `FILTER`.

## <a name="example-1"></a>Příklad 1

Výraz `CONTAINS ("abc", "d")` vrací **FALSE**, zatímco výraz `CONTAINS ("abc", "C")` vrací **TRUE**.

## <a name="example-2"></a>Příklad 2

Výraz `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` vrací **TRUE** pokud hodnota pole **Address** zdroje **modelových** dat obsahuje řetězec **DEU**. V opačném případě vrátí hodnotu **FALSE**.

## <a name="additional-resources"></a>Další prostředky

[Logické funkce](er-functions-category-logical.md)
