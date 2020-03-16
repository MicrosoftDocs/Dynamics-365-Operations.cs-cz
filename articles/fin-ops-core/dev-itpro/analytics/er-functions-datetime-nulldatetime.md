---
title: Funkce el. výkaznictví NULLDATETIME
description: Toto téma obsahuje obecné informace o použití funkce NULLDATETIME elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 3cd4c152d4e220a2f6315265ed5e44d148134279
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042245"
---
# <a name="NULLDATETIME">Funkce el. výkaznictví NULLDATETIME</a>

[!include [banner](../includes/banner.md)]

Funkce `NULLDATETIME` vrátí hodnotu typu *datum a čas*, která představuje hodnotu **null** data a času (1. leden 1900) v koordinovaném světovém čase (Greenwich Mean Time \[GMT\]).

## <a name="syntax"></a>Syntaxe

```vb
NULLDATETIME ()
```

## <a name="return-values"></a>Vrácené hodnoty

*Datum a čas*

Výsledná hodnota data a času.

## <a name="example"></a>Příklad

Funkce `DATETIMEFORMAT( NULLDATETIME(), "O")` vrátí řetězcovou hodnotu **1900-01-01T00:00:00.0000000+00:00**, pokud je volána během procesu, který byl iniciován uživatelem aplikace, který má hodnotu časového pásma **(GMT) Koordinovaný světový čas** v sekci **Předvolby jazyka a země/oblasti**.

## <a name="additional-resources"></a>Další zdroje

[Funkce data a času](er-functions-category-datetime.md)
