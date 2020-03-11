---
title: Funkce NUMBERVALUE ER
description: Toto téma obsahuje obecné informace o použití funkce NUMBERVALUE elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 6eeb66f4206eb39141a5b2573fcb9d15428ae52a
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042640"
---
# <span data-ttu-id="2c0fa-103"><a name="NUMBERVALUE">Funkce NUMBERVALUE ER</a></span><span class="sxs-lookup"><span data-stu-id="2c0fa-103"><a name="NUMBERVALUE">NUMBERVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c0fa-104">Funkce `NUMBERVALUE` vrací hodnotu *reálné číslo*, která je převedena ze zadané hodnoty *Řetězec*.</span><span class="sxs-lookup"><span data-stu-id="2c0fa-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="2c0fa-105">Během převodu se uvažují určené oddělovače skupin desetinných míst a číslic.</span><span class="sxs-lookup"><span data-stu-id="2c0fa-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c0fa-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c0fa-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="2c0fa-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="2c0fa-107">Arguments</span></span>

<span data-ttu-id="2c0fa-108">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="2c0fa-108">`text`: *String*</span></span>

<span data-ttu-id="2c0fa-109">Textová hodnota, která musí být převedena na *reálné* číslo.</span><span class="sxs-lookup"><span data-stu-id="2c0fa-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="2c0fa-110">`decimal separator`: řetězec</span><span class="sxs-lookup"><span data-stu-id="2c0fa-110">`decimal separator`: String</span></span>

<span data-ttu-id="2c0fa-111">Desetinný oddělovač.</span><span class="sxs-lookup"><span data-stu-id="2c0fa-111">A decimal separator.</span></span> <span data-ttu-id="2c0fa-112">Používá se k oddělení celého čísla a zlomkových částí desetinného čísla.</span><span class="sxs-lookup"><span data-stu-id="2c0fa-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="2c0fa-113">`digit grouping separator`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="2c0fa-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="2c0fa-114">Oddělovač skupin číslic.</span><span class="sxs-lookup"><span data-stu-id="2c0fa-114">A digit grouping separator.</span></span> <span data-ttu-id="2c0fa-115">Používá se jako oddělovač tisíců.</span><span class="sxs-lookup"><span data-stu-id="2c0fa-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="2c0fa-116">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="2c0fa-116">Return values</span></span>

<span data-ttu-id="2c0fa-117">*Reálný*</span><span class="sxs-lookup"><span data-stu-id="2c0fa-117">*Real*</span></span>

<span data-ttu-id="2c0fa-118">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="2c0fa-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="2c0fa-119">Příklad</span><span class="sxs-lookup"><span data-stu-id="2c0fa-119">Example</span></span>

<span data-ttu-id="2c0fa-120">`NUMBERVALUE( "1 234,56", ",", " ")` vrací **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="2c0fa-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c0fa-121">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="2c0fa-121">Additional resources</span></span>

[<span data-ttu-id="2c0fa-122">Funkce převodu typu</span><span class="sxs-lookup"><span data-stu-id="2c0fa-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
