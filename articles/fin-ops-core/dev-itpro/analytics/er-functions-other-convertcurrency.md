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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d0c168e07252f7c423271bc808f3fca3834077f
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041508"
---
# <a name="CONVERTCURRENCY">Funkce el. výkaznictví CONVERTCURRENCY</a>

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
