---
title: Funkce ER ENDSWITH
description: Tento článek obsahuje obecné informace o použití funkce ENDSWITH elektronického výkaznictví (ER).
author: kfend
ms.date: 02/11/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 2608593238e5b2f738b452fb042837238f17e44e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271606"
---
# <a name="endswith-er-function"></a>Funkce ER ENDSWITH

[!include [banner](../includes/banner.md)]

Funkce `ENDSWITH` určuje, zda zadaný vstup končí zadaným textem. Vrací *logickou* hodnotu **TRUE**, pokud zadaný vstup končí zadaným textem. V opačném případě výraz vrátí *logickou hodnotu* **FALSE**.

## <a name="syntax"></a>Syntaxe

```vb
ENDSWITH (input, end text)
```

## <a name="arguments"></a>Argumenty

`input`: *řetězec*

Platná cesta k položce zdroje dat z typu *Řetězec* nebo řetězcová konstanta, jejíž hodnota může končit druhým argumentem.

`start text`: *řetězec*

Platná cesta k zdroje dat z typu dat *Řetězec* nebo řetězcová konstanta, jejíž hodnota může být na konci prvního argumentu.

## <a name="return-values"></a>Vrácené hodnoty

*Logická*

Výsledná *logická hodnota*.

## <a name="usage-notes"></a>Poznámky k použití

Tuto funkci lze použít k určení podmínkového výrazu funkce [FILTER](er-functions-list-filter.md) pouze v případě, že je příslušné mapování nakonfigurováno v [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) pro přístup k [Microsoft Dataverse](/power-platform/admin/data-integrator). Jinak je v době návrhu vyvolána výjimka. Zpráva, kterou obdržíte, doporučuje použít funkci [WHERE](er-functions-list-where.md) namísto funkce `FILTER`.

## <a name="example-1"></a>Příklad 1

Výraz `ENDSWITH ("abc", "d")` vrací **FALSE**, zatímco výraz `ENDSWITH ("abc", "C")` vrací **TRUE**.

## <a name="example-2"></a>Příklad 2

Výraz `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` vrací **TRUE** pokud hodnota pole **Address** zdroje **modelových** dat končí řetězcem **USA**. V opačném případě vrátí hodnotu **FALSE**.

## <a name="additional-resources"></a>Další prostředky

[Logické funkce](er-functions-category-logical.md)
