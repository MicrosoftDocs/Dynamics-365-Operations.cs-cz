---
title: Funkce FA_BALANCE
description: Toto téma obsahuje obecné informace o použití funkce FA_BALANCE elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 76a087157ae53e2c571654ade7383d7bd7a005c3
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041439"
---
# <a name="FA_BALANCE">Funkce FA_BALANCE</a>

[!include [banner](../includes/banner.md)]

Funkce `FA_BALANCE` vrátí hodnotu typu *kontejner (záznam)*, která se skládá z dat pro zůstatek dlouhodobého majetku pro zadanou položku dlouhodobého majetku, vykazovaný rok a datum vykazování.

## <a name="syntax"></a>Syntaxe

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a>Argumenty

`fixed asset code`: *řetězec*

Hodnota typu *řetězec* představující kód položky dlouhodobého majetku, pro kterou se počítá zůstatek.

`value model code`: *řetězec*

Hodnota typu *řetězec* představující kód oceňovacího modelu, pro který se počítá zůstatek.

`reporting year`: *výčtová hodnota*

Výčtová hodnota pro výčet aplikace **AssetYear** (rok majetku), která definuje období pro výpočet zůstatku.

`reporting date`: *datum*

Hodnota typu *datum* definující datum výpočtu zůstatku.

## <a name="return-values"></a>Vrácené hodnoty

*Kontejner (záznam)*

Výsledná hodnota atributu.

## <a name="example"></a>Příklad

`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` vrátí kontejner dat zůstatků pro dlouhodobý majetek **COMP-000001** připravený pro **Current** (aktuální) oceňovací model k aktuálnímu datu relace aplikace.

## <a name="additional-resources"></a>Další zdroje

[Další funkce (konkrétní pro obchodní domény)](er-functions-category-other.md)
