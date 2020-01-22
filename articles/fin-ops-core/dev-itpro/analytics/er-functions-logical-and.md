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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd9c0ed0238009f70ad7a9bf5a5e19ebfb95cccc
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917159"
---
# <span data-ttu-id="9007f-103"><a name="AND">Funkce el. výkaznictví AND</a></span><span class="sxs-lookup"><span data-stu-id="9007f-103"><a name="AND">AND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9007f-104">Funce `AND` vrátí *logickou hodnotu* **TRUE**, jsou-li splněny všechny zadané podmínky.</span><span class="sxs-lookup"><span data-stu-id="9007f-104">The `AND` function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="9007f-105">V opačném případě výraz vrátí *logickou hodnotu* **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="9007f-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9007f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9007f-106">Syntax</span></span>

```
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="9007f-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="9007f-107">Arguments</span></span>

<span data-ttu-id="9007f-108">`condition 1`: *logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="9007f-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="9007f-109">Platný podmíněný výraz, který má být testován.</span><span class="sxs-lookup"><span data-stu-id="9007f-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="9007f-110">Tento argument je povinný.</span><span class="sxs-lookup"><span data-stu-id="9007f-110">This argument is required.</span></span>

<span data-ttu-id="9007f-111">`condition N`: *logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="9007f-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="9007f-112">Platný podmíněný výraz, který má být testován.</span><span class="sxs-lookup"><span data-stu-id="9007f-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="9007f-113">Tyto další argumenty jsou nepovinné.</span><span class="sxs-lookup"><span data-stu-id="9007f-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="9007f-114">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="9007f-114">Return values</span></span>

<span data-ttu-id="9007f-115">*Logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="9007f-115">*Boolean*</span></span>

<span data-ttu-id="9007f-116">Výsledná *logická hodnota*.</span><span class="sxs-lookup"><span data-stu-id="9007f-116">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9007f-117">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="9007f-117">Usage notes</span></span>

<span data-ttu-id="9007f-118">V argumentech logických funkcí můžete použít odkazy na zdroje dat, číselné a textové hodnoty, logické hodnoty, relační operátory a jiné funkce elektronického výkaznictví (ER).</span><span class="sxs-lookup"><span data-stu-id="9007f-118">In the arguments of logical functions, you can use data source references, numeric and text values, Boolean values, comparison operators, and other Electronic reporting (ER) functions.</span></span> <span data-ttu-id="9007f-119">Všechny argumenty je však nutné vyhodnotit na *logickou hodnotu* **TRUE** nebo **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="9007f-119">However, all the arguments must be evaluated to a *Boolean* value of **TRUE** or **FALSE**.</span></span>

## <a name="example"></a><span data-ttu-id="9007f-120">Příklad</span><span class="sxs-lookup"><span data-stu-id="9007f-120">Example</span></span>

<span data-ttu-id="9007f-121">`AND (1=1, "a"="a")` vrátí **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="9007f-121">`AND (1=1, "a"="a")` returns **TRUE**.</span></span>

<span data-ttu-id="9007f-122">`AND (1=2, "a"="a")` vrátí **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="9007f-122">`AND (1=2, "a"="a")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9007f-123">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="9007f-123">Additional resources</span></span>

[<span data-ttu-id="9007f-124">Logické funkce</span><span class="sxs-lookup"><span data-stu-id="9007f-124">Logical functions</span></span>](er-functions-category-logical.md)
