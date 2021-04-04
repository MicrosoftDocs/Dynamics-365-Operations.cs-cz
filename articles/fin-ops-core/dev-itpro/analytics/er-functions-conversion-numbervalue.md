---
title: Funkce NUMBERVALUE ER
description: Toto téma obsahuje obecné informace o použití funkce NUMBERVALUE elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: f542621c4bcc29e03d8c92b0c700e2c80c9846f6
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561415"
---
# <a name="numbervalue-er-function"></a><span data-ttu-id="40b2f-103">Funkce NUMBERVALUE ER</span><span class="sxs-lookup"><span data-stu-id="40b2f-103">NUMBERVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40b2f-104">Funkce `NUMBERVALUE` vrací hodnotu *reálné číslo*, která je převedena ze zadané hodnoty *Řetězec*.</span><span class="sxs-lookup"><span data-stu-id="40b2f-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="40b2f-105">Během převodu se uvažují určené oddělovače skupin desetinných míst a číslic.</span><span class="sxs-lookup"><span data-stu-id="40b2f-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="40b2f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40b2f-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="40b2f-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="40b2f-107">Arguments</span></span>

<span data-ttu-id="40b2f-108">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="40b2f-108">`text`: *String*</span></span>

<span data-ttu-id="40b2f-109">Textová hodnota, která musí být převedena na *reálné* číslo.</span><span class="sxs-lookup"><span data-stu-id="40b2f-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="40b2f-110">`decimal separator`: řetězec</span><span class="sxs-lookup"><span data-stu-id="40b2f-110">`decimal separator`: String</span></span>

<span data-ttu-id="40b2f-111">Desetinný oddělovač.</span><span class="sxs-lookup"><span data-stu-id="40b2f-111">A decimal separator.</span></span> <span data-ttu-id="40b2f-112">Používá se k oddělení celého čísla a zlomkových částí desetinného čísla.</span><span class="sxs-lookup"><span data-stu-id="40b2f-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="40b2f-113">`digit grouping separator`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="40b2f-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="40b2f-114">Oddělovač skupin číslic.</span><span class="sxs-lookup"><span data-stu-id="40b2f-114">A digit grouping separator.</span></span> <span data-ttu-id="40b2f-115">Používá se jako oddělovač tisíců.</span><span class="sxs-lookup"><span data-stu-id="40b2f-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="40b2f-116">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="40b2f-116">Return values</span></span>

<span data-ttu-id="40b2f-117">*Reálný*</span><span class="sxs-lookup"><span data-stu-id="40b2f-117">*Real*</span></span>

<span data-ttu-id="40b2f-118">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="40b2f-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="40b2f-119">Příklad</span><span class="sxs-lookup"><span data-stu-id="40b2f-119">Example</span></span>

<span data-ttu-id="40b2f-120">`NUMBERVALUE( "1 234,56", ",", " ")` vrací **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="40b2f-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="40b2f-121">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="40b2f-121">Additional resources</span></span>

[<span data-ttu-id="40b2f-122">Funkce převodu typu</span><span class="sxs-lookup"><span data-stu-id="40b2f-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]