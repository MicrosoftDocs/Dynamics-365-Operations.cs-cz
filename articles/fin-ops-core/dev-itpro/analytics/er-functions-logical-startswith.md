---
title: Funkce ER STARTSWITH
description: Tento článek obsahuje obecné informace o použití funkce STARTSWITH elektronického výkaznictví (ER).
author: NickSelin
ms.date: 02/11/2021
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
ms.openlocfilehash: a9c22154484f9e98dbe101b5de0f539b2feb9865
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883720"
---
# <a name="startswith-er-function"></a>Funkce ER STARTSWITH

[!include [banner](../includes/banner.md)]

Funkce `STARTSWITH` určuje, zda zadaný vstup začíná zadaným textem. Vrací *logickou* hodnotu **TRUE**, pokud zadaný vstup začíná zadaným textem. V opačném případě výraz vrátí *logickou hodnotu* **FALSE**.

## <a name="syntax"></a>Syntaxe

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a>Argumenty

`input`: *řetězec*

Platná cesta k položce zdroje dat z typu *Řetězec* nebo řetězcová konstanta, jejíž hodnota může začínat druhým argumentem.

`start text`: *řetězec*

Platná cesta k zdroje dat z typu dat *Řetězec* nebo řetězcová konstanta, jejíž hodnota může být na začátku prvního argumentu.

## <a name="return-values"></a>Vrácené hodnoty

*Logická*

Výsledná *logická hodnota*.

## <a name="usage-notes"></a>Poznámky k použití

Tuto funkci lze použít k určení podmínkového výrazu funkce [FILTER](er-functions-list-filter.md) pouze v případě, že je příslušné mapování nakonfigurováno v [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) pro přístup k [Microsoft Dataverse](/power-platform/admin/data-integrator). Jinak je v době návrhu vyvolána výjimka. Zpráva, kterou obdržíte, doporučuje použít funkci [WHERE](er-functions-list-where.md) namísto funkce `FILTER`.

## <a name="example-1"></a>Příklad 1

Výraz `STARTSWITH ("abc", "d")` vrací **FALSE**, zatímco výraz `STARTSWITH ("abc", "A")` vrací **TRUE**.

## <a name="example-2"></a>Příklad 2

Výraz `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` vrací **TRUE** pokud hodnota pole **Address** zdroje **modelových** dat začíná řetězcem **123 Coffee Street**. V opačném případě vrátí hodnotu **FALSE**.

## <a name="additional-resources"></a>Další prostředky

[Logické funkce](er-functions-category-logical.md)
