---
title: Funkce elektronického výkaznictví ROUNDDOWN
description: Toto téma obsahuje obecné informace o použití funkce ROUNDDOWN elektronického výkaznictví.
author: NickSelin
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
ms.openlocfilehash: 89fc134ec11a47506211ce68ec3aaf966d9a308b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744456"
---
# <a name="rounddown-er-function"></a><span data-ttu-id="3b216-103">Funkce elektronického výkaznictví ROUNDDOWN</span><span class="sxs-lookup"><span data-stu-id="3b216-103">ROUNDDOWN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b216-104">Funkce `ROUNDDOWN` vrátí zadané číslo poté, co je zaokrouhleno dolů na hodnotu typu *reálné číslo* na zadaný počet desetinných míst.</span><span class="sxs-lookup"><span data-stu-id="3b216-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b216-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b216-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="3b216-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="3b216-106">Arguments</span></span>

<span data-ttu-id="3b216-107">`number`: *reálné číslo*</span><span class="sxs-lookup"><span data-stu-id="3b216-107">`number`: *Real*</span></span>

<span data-ttu-id="3b216-108">Číselná hodnota, která má být zaokrouhlena dolů.</span><span class="sxs-lookup"><span data-stu-id="3b216-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="3b216-109">`decimals`: *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="3b216-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="3b216-110">Číselná hodnota, která představuje počet desetinných míst.</span><span class="sxs-lookup"><span data-stu-id="3b216-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="3b216-111">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="3b216-111">Return values</span></span>

<span data-ttu-id="3b216-112">*Reálný*</span><span class="sxs-lookup"><span data-stu-id="3b216-112">*Real*</span></span>

<span data-ttu-id="3b216-113">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="3b216-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3b216-114">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="3b216-114">Usage notes</span></span>

<span data-ttu-id="3b216-115">Tato funkce se chová jako [ROUND](er-functions-mathematical-round.md), ale vždy zaokrouhluje zadané číslo směrem dolů (směrem k nule).</span><span class="sxs-lookup"><span data-stu-id="3b216-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="3b216-116">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="3b216-116">Example 1</span></span>

<span data-ttu-id="3b216-117">`ROUNDDOWN (1200.767, 2)` zaokrouhlí směrem dolů na dvě desetinná místa a vrátí hodnotu **1200.76**.</span><span class="sxs-lookup"><span data-stu-id="3b216-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="3b216-118">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="3b216-118">Example 2</span></span>

<span data-ttu-id="3b216-119">`ROUNDDOWN (1700.767, -3)` zaokrouhlí směrem dolů na nejbližší násobek 1 000 a vrátí hodnotu **1000**.</span><span class="sxs-lookup"><span data-stu-id="3b216-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3b216-120">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="3b216-120">Additional resources</span></span>

[<span data-ttu-id="3b216-121">Matematické funkce</span><span class="sxs-lookup"><span data-stu-id="3b216-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]