---
title: Funkce el. výkaznictví AND
description: Toto téma obsahuje obecné informace o použití funkce AND elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 8ccb7feb1d0f6836e7e8001870034900f6a1f598
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687067"
---
# <a name="and-er-function"></a><span data-ttu-id="7dd3c-103">Funkce el. výkaznictví AND</span><span class="sxs-lookup"><span data-stu-id="7dd3c-103">AND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7dd3c-104">Funce `AND` vrátí *logickou hodnotu* **TRUE**, jsou-li splněny všechny zadané podmínky.</span><span class="sxs-lookup"><span data-stu-id="7dd3c-104">The `AND` function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="7dd3c-105">V opačném případě výraz vrátí *logickou hodnotu* **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="7dd3c-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dd3c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7dd3c-106">Syntax</span></span>

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="7dd3c-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="7dd3c-107">Arguments</span></span>

<span data-ttu-id="7dd3c-108">`condition 1`: *logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="7dd3c-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="7dd3c-109">Platný podmíněný výraz, který má být testován.</span><span class="sxs-lookup"><span data-stu-id="7dd3c-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="7dd3c-110">Tento argument je povinný.</span><span class="sxs-lookup"><span data-stu-id="7dd3c-110">This argument is required.</span></span>

<span data-ttu-id="7dd3c-111">`condition N`: *logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="7dd3c-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="7dd3c-112">Platný podmíněný výraz, který má být testován.</span><span class="sxs-lookup"><span data-stu-id="7dd3c-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="7dd3c-113">Tyto další argumenty jsou nepovinné.</span><span class="sxs-lookup"><span data-stu-id="7dd3c-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="7dd3c-114">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="7dd3c-114">Return values</span></span>

<span data-ttu-id="7dd3c-115">*Logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="7dd3c-115">*Boolean*</span></span>

<span data-ttu-id="7dd3c-116">Výsledná *logická hodnota*.</span><span class="sxs-lookup"><span data-stu-id="7dd3c-116">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7dd3c-117">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="7dd3c-117">Usage notes</span></span>

<span data-ttu-id="7dd3c-118">V argumentech logických funkcí můžete použít odkazy na zdroje dat, číselné a textové hodnoty, logické hodnoty, relační operátory a jiné funkce elektronického výkaznictví (ER).</span><span class="sxs-lookup"><span data-stu-id="7dd3c-118">In the arguments of logical functions, you can use data source references, numeric and text values, Boolean values, comparison operators, and other Electronic reporting (ER) functions.</span></span> <span data-ttu-id="7dd3c-119">Všechny argumenty je však nutné vyhodnotit na *logickou hodnotu* **TRUE** nebo **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="7dd3c-119">However, all the arguments must be evaluated to a *Boolean* value of **TRUE** or **FALSE**.</span></span>

## <a name="example"></a><span data-ttu-id="7dd3c-120">Příklad</span><span class="sxs-lookup"><span data-stu-id="7dd3c-120">Example</span></span>

<span data-ttu-id="7dd3c-121">`AND (1=1, "a"="a")` vrátí **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="7dd3c-121">`AND (1=1, "a"="a")` returns **TRUE**.</span></span>

<span data-ttu-id="7dd3c-122">`AND (1=2, "a"="a")` vrátí **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="7dd3c-122">`AND (1=2, "a"="a")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7dd3c-123">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="7dd3c-123">Additional resources</span></span>

[<span data-ttu-id="7dd3c-124">Logické funkce</span><span class="sxs-lookup"><span data-stu-id="7dd3c-124">Logical functions</span></span>](er-functions-category-logical.md)
