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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65e9ef92dc30e46c297d93e262bad8878df47a0c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682286"
---
# <a name="nulldatetime-er-function"></a><span data-ttu-id="ecf85-103">Funkce el. výkaznictví NULLDATETIME</span><span class="sxs-lookup"><span data-stu-id="ecf85-103">NULLDATETIME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ecf85-104">Funkce `NULLDATETIME` vrátí hodnotu typu *datum a čas*, která představuje hodnotu **null** data a času (1. leden 1900) v koordinovaném světovém čase (Greenwich Mean Time \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="ecf85-104">The `NULLDATETIME` function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="ecf85-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ecf85-105">Syntax</span></span>

```vb
NULLDATETIME ()
```

## <a name="return-values"></a><span data-ttu-id="ecf85-106">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="ecf85-106">Return values</span></span>

<span data-ttu-id="ecf85-107">*Datum a čas*</span><span class="sxs-lookup"><span data-stu-id="ecf85-107">*DateTime*</span></span>

<span data-ttu-id="ecf85-108">Výsledná hodnota data a času.</span><span class="sxs-lookup"><span data-stu-id="ecf85-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="ecf85-109">Příklad</span><span class="sxs-lookup"><span data-stu-id="ecf85-109">Example</span></span>

<span data-ttu-id="ecf85-110">Funkce `DATETIMEFORMAT( NULLDATETIME(), "O")` vrátí řetězcovou hodnotu **1900-01-01T00:00:00.0000000+00:00**, pokud je volána během procesu, který byl iniciován uživatelem aplikace, který má hodnotu časového pásma **(GMT) Koordinovaný světový čas** v sekci **Předvolby jazyka a země/oblasti**.</span><span class="sxs-lookup"><span data-stu-id="ecf85-110">`DATETIMEFORMAT( NULLDATETIME(), "O")` returns the string value **1900-01-01T00:00:00.0000000+00:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT) Coordinated Universal Time** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ecf85-111">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="ecf85-111">Additional resources</span></span>

[<span data-ttu-id="ecf85-112">Funkce data a času</span><span class="sxs-lookup"><span data-stu-id="ecf85-112">Date and time functions</span></span>](er-functions-category-datetime.md)
