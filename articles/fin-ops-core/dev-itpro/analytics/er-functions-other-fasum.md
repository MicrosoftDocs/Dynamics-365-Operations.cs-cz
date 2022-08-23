---
title: Funkce el. výkaznictví FA_SUM
description: Tento článek obsahuje obecné informace o použití funkce FA_SUM elektronického výkaznictví.
author: kfend
ms.date: 12/17/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: bcedbc3df835b219b8df6d05f1db6b331f1e9254
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278910"
---
# <a name="fa_sum-er-function"></a>Funkce el. výkaznictví FA_SUM

[!include [banner](../includes/banner.md)]

Funkce `FA_SUM` vrátí hodnotu typu *kontejneru (záznam)*, která se skládá z dat pro částky dlouhodobého majetku pro zadanou položku dlouhodobého majetku, kód oceňovacího modelu a rozsah kalendářních dat.

## <a name="syntax"></a>Syntaxe

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a>Argumenty

`fixed asset code`: *řetězec*

Hodnota typu *řetězec* představující kód položky dlouhodobého majetku, pro kterou se počítá zůstatek.

`value model code`: *řetězec*

Hodnota typu *řetězec* představující kód oceňovacího modelu, pro který se počítá zůstatek.

`start date`: *datum*

Hodnota typu *datum* představuje počáteční datum období, pro které jsou vypočteny částky dlouhodobého majetku.

`end date`: *datum*

Hodnota typu *datum* představuje koncové datum období, pro které jsou vypočteny částky dlouhodobého majetku.

## <a name="return-values"></a>Vrácené hodnoty

*Kontejner (záznam)*

Výsledná hodnota atributu.

## <a name="example"></a>Příklad

`FA_SUM ("COMP-000001", "Current", Date1, Date2)` vrátí kontejner dat pro dlouhodobý majetek **COMP-000001**, který byl připraven pro **aktuální** (Current) oceňovací model a pro období od **Date1** (datum1) do **Date2** (datum2).

## <a name="additional-resources"></a>Další zdroje

[Další funkce (konkrétní pro obchodní domény)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
