---
title: Funkce elektronického výkaznictví ROUND
description: Toto téma obsahuje obecné informace o použití funkce ROUND elektronického výkaznictví.
author: NickSelin
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ce0f50cd5e544455626862e44b774dba39cf6e57
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744480"
---
# <a name="round-er-function"></a><span data-ttu-id="5a060-103">Funkce elektronického výkaznictví ROUND</span><span class="sxs-lookup"><span data-stu-id="5a060-103">ROUND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a060-104">Funkce `ROUND` vrátí zadané číslo, poté, co je zaokrouhleno na hodnotu typu *reálné číslo* po zaokrouhlení na zadaný počet desetinných míst.</span><span class="sxs-lookup"><span data-stu-id="5a060-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a060-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a060-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="5a060-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="5a060-106">Arguments</span></span>

<span data-ttu-id="5a060-107">`number`: *reálné číslo*</span><span class="sxs-lookup"><span data-stu-id="5a060-107">`number`: *Real*</span></span>

<span data-ttu-id="5a060-108">Číselná hodnota, která má být zaokrouhlena.</span><span class="sxs-lookup"><span data-stu-id="5a060-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="5a060-109">`decimals`: *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="5a060-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="5a060-110">Číselná hodnota, která představuje počet desetinných míst.</span><span class="sxs-lookup"><span data-stu-id="5a060-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="5a060-111">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="5a060-111">Return values</span></span>

<span data-ttu-id="5a060-112">*Reálný*</span><span class="sxs-lookup"><span data-stu-id="5a060-112">*Real*</span></span>

<span data-ttu-id="5a060-113">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="5a060-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5a060-114">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="5a060-114">Usage notes</span></span>

<span data-ttu-id="5a060-115">Pokud je hodnota argumentu `decimals` vyšší než 0 (nula), zadané číslo je zaokrouhleno na tento počet desetinných míst.</span><span class="sxs-lookup"><span data-stu-id="5a060-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="5a060-116">Pokud má argument `decimals` hodnotu **0** (nula), zadané číslo je zaokrouhleno na nejbližší sudé celé číslo.</span><span class="sxs-lookup"><span data-stu-id="5a060-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest even integer.</span></span>

<span data-ttu-id="5a060-117">Pokud je hodnota argumentu `decimals` nižší než 0 (nula), zadané číslo je zaokrouhleno vlevo od oddělovače desetinných míst.</span><span class="sxs-lookup"><span data-stu-id="5a060-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="5a060-118">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="5a060-118">Example 1</span></span>

<span data-ttu-id="5a060-119">`ROUND (1200.767, 2)` zaokrouhlí na dvě desetinná místa a vrátí hodnotu **1200.77**.</span><span class="sxs-lookup"><span data-stu-id="5a060-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="5a060-120">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="5a060-120">Example 2</span></span>

<span data-ttu-id="5a060-121">`ROUND (1200.767, -3)` zaokrouhlí na nejbližší násobek 1 000 a vrátí hodnotu **1000**.</span><span class="sxs-lookup"><span data-stu-id="5a060-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="example-3"></a><span data-ttu-id="5a060-122">Příklad 3</span><span class="sxs-lookup"><span data-stu-id="5a060-122">Example 3</span></span>

<span data-ttu-id="5a060-123">`ROUND (1200.5, 0)` zaokrouhlí na nejbližší sudé celé číslo a vrátí **1200**, zatímco `ROUND (1201.5, 0)` udělá totéž a vrátí **1202**.</span><span class="sxs-lookup"><span data-stu-id="5a060-123">`ROUND (1200.5, 0)` rounds to the nearest even integer and returns **1200**, while `ROUND (1201.5, 0)` does the same and returns **1202**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5a060-124">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="5a060-124">Additional resources</span></span>

[<span data-ttu-id="5a060-125">Matematické funkce</span><span class="sxs-lookup"><span data-stu-id="5a060-125">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]