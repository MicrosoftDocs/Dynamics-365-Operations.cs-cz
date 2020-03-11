---
title: Funkce elektronického výkaznictví ROUND
description: Toto téma obsahuje obecné informace o použití funkce ROUND elektronického výkaznictví.
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
ms.openlocfilehash: 6751c1321fc71419fa8b153145a057371e0f7af5
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041600"
---
# <span data-ttu-id="0c199-103"><a name="ROUND">Funkce elektronického výkaznictví ROUND</a></span><span class="sxs-lookup"><span data-stu-id="0c199-103"><a name="ROUND">ROUND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c199-104">Funkce `ROUND` vrátí zadané číslo, poté, co je zaokrouhleno na hodnotu typu *reálné číslo* po zaokrouhlení na zadaný počet desetinných míst.</span><span class="sxs-lookup"><span data-stu-id="0c199-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c199-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c199-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="0c199-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="0c199-106">Arguments</span></span>

<span data-ttu-id="0c199-107">`number`: *reálné číslo*</span><span class="sxs-lookup"><span data-stu-id="0c199-107">`number`: *Real*</span></span>

<span data-ttu-id="0c199-108">Číselná hodnota, která má být zaokrouhlena.</span><span class="sxs-lookup"><span data-stu-id="0c199-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="0c199-109">`decimals`: *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="0c199-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="0c199-110">Číselná hodnota, která představuje počet desetinných míst.</span><span class="sxs-lookup"><span data-stu-id="0c199-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="0c199-111">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="0c199-111">Return values</span></span>

<span data-ttu-id="0c199-112">*Reálný*</span><span class="sxs-lookup"><span data-stu-id="0c199-112">*Real*</span></span>

<span data-ttu-id="0c199-113">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="0c199-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0c199-114">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="0c199-114">Usage notes</span></span>

<span data-ttu-id="0c199-115">Pokud je hodnota argumentu `decimals` vyšší než 0 (nula), zadané číslo je zaokrouhleno na tento počet desetinných míst.</span><span class="sxs-lookup"><span data-stu-id="0c199-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="0c199-116">Pokud je hodnota argumentu `decimals` **0** (nula), zadané číslo je zaokrouhleno na nejbližší celé číslo.</span><span class="sxs-lookup"><span data-stu-id="0c199-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest integer.</span></span>

<span data-ttu-id="0c199-117">Pokud je hodnota argumentu `decimals` nižší než 0 (nula), zadané číslo je zaokrouhleno vlevo od oddělovače desetinných míst.</span><span class="sxs-lookup"><span data-stu-id="0c199-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="0c199-118">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="0c199-118">Example 1</span></span>

<span data-ttu-id="0c199-119">`ROUND (1200.767, 2)` zaokrouhlí na dvě desetinná místa a vrátí hodnotu **1200.77**.</span><span class="sxs-lookup"><span data-stu-id="0c199-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="0c199-120">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="0c199-120">Example 2</span></span>

<span data-ttu-id="0c199-121">`ROUND (1200.767, -3)` zaokrouhlí na nejbližší násobek 1 000 a vrátí hodnotu **1000**.</span><span class="sxs-lookup"><span data-stu-id="0c199-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0c199-122">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="0c199-122">Additional resources</span></span>

[<span data-ttu-id="0c199-123">Matematické funkce</span><span class="sxs-lookup"><span data-stu-id="0c199-123">Mathematical functions</span></span>](er-functions-category-mathematical.md)
