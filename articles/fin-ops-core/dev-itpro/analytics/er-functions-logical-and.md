---
title: Funkce el. výkaznictví AND
description: Toto téma obsahuje obecné informace o použití funkce AND elektronického výkaznictví.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 9851321137b4c7744634df30f85aa3a0b1a0a588
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745466"
---
# <a name="and-er-function"></a><span data-ttu-id="962fe-103">Funkce el. výkaznictví AND</span><span class="sxs-lookup"><span data-stu-id="962fe-103">AND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="962fe-104">Funce `AND` vrátí *logickou hodnotu* **TRUE**, jsou-li splněny všechny zadané podmínky.</span><span class="sxs-lookup"><span data-stu-id="962fe-104">The `AND` function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="962fe-105">V opačném případě výraz vrátí *logickou hodnotu* **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="962fe-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="962fe-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="962fe-106">Syntax</span></span>

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="962fe-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="962fe-107">Arguments</span></span>

<span data-ttu-id="962fe-108">`condition 1`: *logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="962fe-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="962fe-109">Platný podmíněný výraz, který má být testován.</span><span class="sxs-lookup"><span data-stu-id="962fe-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="962fe-110">Tento argument je povinný.</span><span class="sxs-lookup"><span data-stu-id="962fe-110">This argument is required.</span></span>

<span data-ttu-id="962fe-111">`condition N`: *logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="962fe-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="962fe-112">Platný podmíněný výraz, který má být testován.</span><span class="sxs-lookup"><span data-stu-id="962fe-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="962fe-113">Tyto další argumenty jsou nepovinné.</span><span class="sxs-lookup"><span data-stu-id="962fe-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="962fe-114">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="962fe-114">Return values</span></span>

<span data-ttu-id="962fe-115">*Logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="962fe-115">*Boolean*</span></span>

<span data-ttu-id="962fe-116">Výsledná *logická hodnota*.</span><span class="sxs-lookup"><span data-stu-id="962fe-116">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="962fe-117">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="962fe-117">Usage notes</span></span>

<span data-ttu-id="962fe-118">V argumentech logických funkcí můžete použít odkazy na zdroje dat, číselné a textové hodnoty, logické hodnoty, relační operátory a jiné funkce elektronického výkaznictví (ER).</span><span class="sxs-lookup"><span data-stu-id="962fe-118">In the arguments of logical functions, you can use data source references, numeric and text values, Boolean values, comparison operators, and other Electronic reporting (ER) functions.</span></span> <span data-ttu-id="962fe-119">Všechny argumenty je však nutné vyhodnotit na *logickou hodnotu* **TRUE** nebo **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="962fe-119">However, all the arguments must be evaluated to a *Boolean* value of **TRUE** or **FALSE**.</span></span>

## <a name="example"></a><span data-ttu-id="962fe-120">Příklad</span><span class="sxs-lookup"><span data-stu-id="962fe-120">Example</span></span>

<span data-ttu-id="962fe-121">`AND (1=1, "a"="a")` vrátí **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="962fe-121">`AND (1=1, "a"="a")` returns **TRUE**.</span></span>

<span data-ttu-id="962fe-122">`AND (1=2, "a"="a")` vrátí **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="962fe-122">`AND (1=2, "a"="a")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="962fe-123">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="962fe-123">Additional resources</span></span>

[<span data-ttu-id="962fe-124">Logické funkce</span><span class="sxs-lookup"><span data-stu-id="962fe-124">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]