---
title: Funkce el. výkaznictví CONVERTCURRENCY
description: Toto téma obsahuje obecné informace o použití funkce CONVERTCURRENCY elektronického výkaznictví.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a27fd30236a61576ab9063010ea6bc38d9cf7a1e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686779"
---
# <a name="convertcurrency-er-function"></a>Funkce el. výkaznictví CONVERTCURRENCY

[!include [banner](../includes/banner.md)]

Funkce `CONVERTCURRENCY` vrátí hodnotu typu *reálné číslo*, které představuje výsledek pro převedení zadané peněžní částky ze zadané zdrojové měny na zadanou cílovou měnu za použití nastavení zadané společnosti k zadanému datu.

## <a name="syntax"></a>Syntaxe

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a>Argumenty

`amount`: *celé číslo* nebo *reálné číslo*

Číselná hodnota, která představuje peněžní částku, která má být převedena.

`source currency`: *řetězec*

Kód zdrojové měny.

`target currency`: *řetězec*

Kód cílové měny.

`date`: *datum*

Hodnota typu *datum*, která představuje datum, které slouží k určení směnného kursu pro převod.

`company`: *řetězec*

Hodnota typu *řetězec* představující kód společnosti, která poskytuje nastavení použitá pro převod.

## <a name="return-values"></a>Vrácené hodnoty

*Reálný*

Výsledná číselná hodnota.

## <a name="example"></a>Příklad

`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` vrátí ekvivalent jednoho eura v amerických dolarech v aktuální den relace podle nastavení společnosti **DEMF**.

## <a name="additional-resources"></a>Další zdroje

[Další funkce (konkrétní pro obchodní domény)](er-functions-category-other.md)
