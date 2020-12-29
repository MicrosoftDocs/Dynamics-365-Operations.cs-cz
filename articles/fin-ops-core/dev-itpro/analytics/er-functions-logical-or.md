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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 107241dbf9a5127d61343fc1cf42c3bab577adb3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686971"
---
# <a name="or-er-function"></a><span data-ttu-id="057a5-103">Funkce el. výkaznictví OR</span><span class="sxs-lookup"><span data-stu-id="057a5-103">OR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="057a5-104">Funkce `OR` vrátí *logickou hodnotu* **FALSE**, pokud nejsou splněny všechny zadané podmínky.</span><span class="sxs-lookup"><span data-stu-id="057a5-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="057a5-105">Tato funkce vrátí *logickou* hodnotu **PRAVDA**, pokud je splněna libovolná uvedená podmínka.</span><span class="sxs-lookup"><span data-stu-id="057a5-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="057a5-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="057a5-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="057a5-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="057a5-107">Arguments</span></span>

<span data-ttu-id="057a5-108">`condition 1`: *logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="057a5-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="057a5-109">Platný podmíněný výraz, který má být testován.</span><span class="sxs-lookup"><span data-stu-id="057a5-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="057a5-110">Tento argument je povinný.</span><span class="sxs-lookup"><span data-stu-id="057a5-110">This argument is required.</span></span>

<span data-ttu-id="057a5-111">`condition N`: *logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="057a5-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="057a5-112">Platný podmíněný výraz, který má být testován.</span><span class="sxs-lookup"><span data-stu-id="057a5-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="057a5-113">Tyto další argumenty jsou nepovinné.</span><span class="sxs-lookup"><span data-stu-id="057a5-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="057a5-114">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="057a5-114">Return values</span></span>

<span data-ttu-id="057a5-115">*Logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="057a5-115">*Boolean*</span></span>

<span data-ttu-id="057a5-116">Výsledná *logická hodnota*.</span><span class="sxs-lookup"><span data-stu-id="057a5-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="057a5-117">Příklad</span><span class="sxs-lookup"><span data-stu-id="057a5-117">Example</span></span>

<span data-ttu-id="057a5-118">`OR (1=2, "a"="a")` vrátí **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="057a5-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="057a5-119">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="057a5-119">Additional resources</span></span>

[<span data-ttu-id="057a5-120">Logické funkce</span><span class="sxs-lookup"><span data-stu-id="057a5-120">Logical functions</span></span>](er-functions-category-logical.md)
