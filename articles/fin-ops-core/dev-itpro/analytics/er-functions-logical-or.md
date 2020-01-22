---
title: Funkce el. výkaznictví OR
description: Toto téma obsahuje obecné informace o použití funkce OR elektronického výkaznictví.
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
ms.openlocfilehash: 81a596f5206b23001feea553adcdf6c904572775
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917113"
---
# <span data-ttu-id="d4def-103"><a name="OR">Funkce el. výkaznictví OR</a></span><span class="sxs-lookup"><span data-stu-id="d4def-103"><a name="OR">OR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4def-104">Funkce `OR` vrátí *logickou hodnotu* **FALSE**, pokud nejsou splněny všechny zadané podmínky.</span><span class="sxs-lookup"><span data-stu-id="d4def-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="d4def-105">Tato funkce vrátí *logickou* hodnotu **PRAVDA**, pokud je splněna libovolná uvedená podmínka.</span><span class="sxs-lookup"><span data-stu-id="d4def-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4def-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4def-106">Syntax</span></span>

```
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="d4def-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="d4def-107">Arguments</span></span>

<span data-ttu-id="d4def-108">`condition 1`: *logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="d4def-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="d4def-109">Platný podmíněný výraz, který má být testován.</span><span class="sxs-lookup"><span data-stu-id="d4def-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="d4def-110">Tento argument je povinný.</span><span class="sxs-lookup"><span data-stu-id="d4def-110">This argument is required.</span></span>

<span data-ttu-id="d4def-111">`condition N`: *logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="d4def-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="d4def-112">Platný podmíněný výraz, který má být testován.</span><span class="sxs-lookup"><span data-stu-id="d4def-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="d4def-113">Tyto další argumenty jsou nepovinné.</span><span class="sxs-lookup"><span data-stu-id="d4def-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="d4def-114">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="d4def-114">Return values</span></span>

<span data-ttu-id="d4def-115">*Logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="d4def-115">*Boolean*</span></span>

<span data-ttu-id="d4def-116">Výsledná *logická hodnota*.</span><span class="sxs-lookup"><span data-stu-id="d4def-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="d4def-117">Příklad</span><span class="sxs-lookup"><span data-stu-id="d4def-117">Example</span></span>

<span data-ttu-id="d4def-118">`OR (1=2, "a"="a")` vrátí **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="d4def-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d4def-119">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="d4def-119">Additional resources</span></span>

[<span data-ttu-id="d4def-120">Logické funkce</span><span class="sxs-lookup"><span data-stu-id="d4def-120">Logical functions</span></span>](er-functions-category-logical.md)
