---
title: Funkce elektronického výkaznictví POWER
description: Toto téma obsahuje obecné informace o použití funkce POWER elektronického výkaznictví.
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
ms.openlocfilehash: ce1f4c735f815c46003ded35156bb47febf177a3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750149"
---
# <a name="power-er-function"></a><span data-ttu-id="ff13e-103">Funkce elektronického výkaznictví POWER</span><span class="sxs-lookup"><span data-stu-id="ff13e-103">POWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff13e-104">Funkce `POWER` vrací hodnotu typu *reálné číslo*, která představuje výsledek umocnění zadaného kladného čísla dle zadané mocniny.</span><span class="sxs-lookup"><span data-stu-id="ff13e-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff13e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff13e-105">Syntax</span></span>

```vb
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="ff13e-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="ff13e-106">Arguments</span></span>

<span data-ttu-id="ff13e-107">`number`: *reálné číslo* nebo *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="ff13e-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="ff13e-108">Číselná hodnota, která musí být umoceněna dle zadané mocniny.</span><span class="sxs-lookup"><span data-stu-id="ff13e-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="ff13e-109">`power`: *reálné číslo* nebo *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="ff13e-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="ff13e-110">Číselná hodnota, která představuje zadanou mocninu.</span><span class="sxs-lookup"><span data-stu-id="ff13e-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="ff13e-111">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="ff13e-111">Return values</span></span>

<span data-ttu-id="ff13e-112">*Reálný*</span><span class="sxs-lookup"><span data-stu-id="ff13e-112">*Real*</span></span>

<span data-ttu-id="ff13e-113">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="ff13e-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="ff13e-114">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="ff13e-114">Example 1</span></span>

<span data-ttu-id="ff13e-115">`POWER (10, 2)` vrátí **100**.</span><span class="sxs-lookup"><span data-stu-id="ff13e-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="ff13e-116">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="ff13e-116">Example 2</span></span>

<span data-ttu-id="ff13e-117">`POWER (4, 0.5)` vrátí **2**.</span><span class="sxs-lookup"><span data-stu-id="ff13e-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ff13e-118">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="ff13e-118">Additional resources</span></span>

[<span data-ttu-id="ff13e-119">Matematické funkce</span><span class="sxs-lookup"><span data-stu-id="ff13e-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]