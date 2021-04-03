---
title: Funkce elektronického výkaznictví POWER
description: Toto téma obsahuje obecné informace o použití funkce POWER elektronického výkaznictví.
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
ms.openlocfilehash: 9c45e7f9b47a3f0ff4445b1dd160def0ada3a56e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570415"
---
# <a name="power-er-function"></a><span data-ttu-id="b1f1f-103">Funkce elektronického výkaznictví POWER</span><span class="sxs-lookup"><span data-stu-id="b1f1f-103">POWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1f1f-104">Funkce `POWER` vrací hodnotu typu *reálné číslo*, která představuje výsledek umocnění zadaného kladného čísla dle zadané mocniny.</span><span class="sxs-lookup"><span data-stu-id="b1f1f-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1f1f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1f1f-105">Syntax</span></span>

```vb
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="b1f1f-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="b1f1f-106">Arguments</span></span>

<span data-ttu-id="b1f1f-107">`number`: *reálné číslo* nebo *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="b1f1f-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="b1f1f-108">Číselná hodnota, která musí být umoceněna dle zadané mocniny.</span><span class="sxs-lookup"><span data-stu-id="b1f1f-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="b1f1f-109">`power`: *reálné číslo* nebo *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="b1f1f-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="b1f1f-110">Číselná hodnota, která představuje zadanou mocninu.</span><span class="sxs-lookup"><span data-stu-id="b1f1f-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="b1f1f-111">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="b1f1f-111">Return values</span></span>

<span data-ttu-id="b1f1f-112">*Reálný*</span><span class="sxs-lookup"><span data-stu-id="b1f1f-112">*Real*</span></span>

<span data-ttu-id="b1f1f-113">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="b1f1f-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="b1f1f-114">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="b1f1f-114">Example 1</span></span>

<span data-ttu-id="b1f1f-115">`POWER (10, 2)` vrátí **100**.</span><span class="sxs-lookup"><span data-stu-id="b1f1f-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="b1f1f-116">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="b1f1f-116">Example 2</span></span>

<span data-ttu-id="b1f1f-117">`POWER (4, 0.5)` vrátí **2**.</span><span class="sxs-lookup"><span data-stu-id="b1f1f-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1f1f-118">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="b1f1f-118">Additional resources</span></span>

[<span data-ttu-id="b1f1f-119">Matematické funkce</span><span class="sxs-lookup"><span data-stu-id="b1f1f-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]