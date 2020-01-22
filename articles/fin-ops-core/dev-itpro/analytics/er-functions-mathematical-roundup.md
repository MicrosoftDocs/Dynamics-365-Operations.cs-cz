---
title: Funkce elektronického výkaznictví ROUNDUP
description: Toto téma obsahuje obecné informace o použití funkce ROUNDUP elektronického výkaznictví.
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
ms.openlocfilehash: 84a62639b49db17fef1abcda75bc5ad7f08d1005
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917044"
---
# <span data-ttu-id="575ef-103"><a name="ROUNDUP">Funkce elektronického výkaznictví ROUNDUP</a></span><span class="sxs-lookup"><span data-stu-id="575ef-103"><a name="ROUNDUP">ROUNDUP ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="575ef-104">Funkce `ROUNDUP` vrátí zadané číslo, poté, co je zaokrouhleno na hodnotu typu *reálné číslo* po zaokrouhlení nahoru na zadaný počet desetinných míst.</span><span class="sxs-lookup"><span data-stu-id="575ef-104">The `ROUNDUP` function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="575ef-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="575ef-105">Syntax</span></span>

```
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="575ef-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="575ef-106">Arguments</span></span>

<span data-ttu-id="575ef-107">`number`: *reálné číslo*</span><span class="sxs-lookup"><span data-stu-id="575ef-107">`number`: *Real*</span></span>

<span data-ttu-id="575ef-108">Číselná hodnota, která má být zaokrouhlena nahoru.</span><span class="sxs-lookup"><span data-stu-id="575ef-108">A numeric value that must be rounded up.</span></span>

<span data-ttu-id="575ef-109">`decimals`: *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="575ef-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="575ef-110">Číselná hodnota, která představuje počet desetinných míst.</span><span class="sxs-lookup"><span data-stu-id="575ef-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="575ef-111">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="575ef-111">Return values</span></span>

<span data-ttu-id="575ef-112">*Reálný*</span><span class="sxs-lookup"><span data-stu-id="575ef-112">*Real*</span></span>

<span data-ttu-id="575ef-113">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="575ef-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="575ef-114">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="575ef-114">Usage notes</span></span>

<span data-ttu-id="575ef-115">Tato funkce se chová jako [ROUND](er-functions-mathematical-round.md), ale vždy zaokrouhluje zadané číslo směrem nahoru (směrem od nuly).</span><span class="sxs-lookup"><span data-stu-id="575ef-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number up (away from zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="575ef-116">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="575ef-116">Example 1</span></span>

<span data-ttu-id="575ef-117">`ROUNDUP (1200.763, 2)` zaokrouhlí směrem nahoru na dvě desetinná místa a vrátí hodnotu **1200.77**.</span><span class="sxs-lookup"><span data-stu-id="575ef-117">`ROUNDUP (1200.763, 2)` rounds up to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="575ef-118">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="575ef-118">Example 2</span></span>

<span data-ttu-id="575ef-119">`ROUNDUP (1200.767, -3)` zaokrouhlí směrem nahoru na nejbližší násobek 1 000 a vrátí hodnotu **2000**.</span><span class="sxs-lookup"><span data-stu-id="575ef-119">`ROUNDUP (1200.767, -3)` rounds up to the nearest multiple of 1,000 and returns **2000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="575ef-120">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="575ef-120">Additional resources</span></span>

[<span data-ttu-id="575ef-121">Matematické funkce</span><span class="sxs-lookup"><span data-stu-id="575ef-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
