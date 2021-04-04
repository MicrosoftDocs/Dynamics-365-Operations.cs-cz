---
title: Funkce elektronického výkaznictví ROUNDDOWN
description: Toto téma obsahuje obecné informace o použití funkce ROUNDDOWN elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: f199d662eb31f184b6f978b3d251e64907254584
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567133"
---
# <a name="rounddown-er-function"></a><span data-ttu-id="0d790-103">Funkce elektronického výkaznictví ROUNDDOWN</span><span class="sxs-lookup"><span data-stu-id="0d790-103">ROUNDDOWN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d790-104">Funkce `ROUNDDOWN` vrátí zadané číslo poté, co je zaokrouhleno dolů na hodnotu typu *reálné číslo* na zadaný počet desetinných míst.</span><span class="sxs-lookup"><span data-stu-id="0d790-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d790-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d790-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="0d790-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="0d790-106">Arguments</span></span>

<span data-ttu-id="0d790-107">`number`: *reálné číslo*</span><span class="sxs-lookup"><span data-stu-id="0d790-107">`number`: *Real*</span></span>

<span data-ttu-id="0d790-108">Číselná hodnota, která má být zaokrouhlena dolů.</span><span class="sxs-lookup"><span data-stu-id="0d790-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="0d790-109">`decimals`: *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="0d790-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="0d790-110">Číselná hodnota, která představuje počet desetinných míst.</span><span class="sxs-lookup"><span data-stu-id="0d790-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="0d790-111">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="0d790-111">Return values</span></span>

<span data-ttu-id="0d790-112">*Reálný*</span><span class="sxs-lookup"><span data-stu-id="0d790-112">*Real*</span></span>

<span data-ttu-id="0d790-113">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="0d790-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0d790-114">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="0d790-114">Usage notes</span></span>

<span data-ttu-id="0d790-115">Tato funkce se chová jako [ROUND](er-functions-mathematical-round.md), ale vždy zaokrouhluje zadané číslo směrem dolů (směrem k nule).</span><span class="sxs-lookup"><span data-stu-id="0d790-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="0d790-116">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="0d790-116">Example 1</span></span>

<span data-ttu-id="0d790-117">`ROUNDDOWN (1200.767, 2)` zaokrouhlí směrem dolů na dvě desetinná místa a vrátí hodnotu **1200.76**.</span><span class="sxs-lookup"><span data-stu-id="0d790-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="0d790-118">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="0d790-118">Example 2</span></span>

<span data-ttu-id="0d790-119">`ROUNDDOWN (1700.767, -3)` zaokrouhlí směrem dolů na nejbližší násobek 1 000 a vrátí hodnotu **1000**.</span><span class="sxs-lookup"><span data-stu-id="0d790-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0d790-120">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="0d790-120">Additional resources</span></span>

[<span data-ttu-id="0d790-121">Matematické funkce</span><span class="sxs-lookup"><span data-stu-id="0d790-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]