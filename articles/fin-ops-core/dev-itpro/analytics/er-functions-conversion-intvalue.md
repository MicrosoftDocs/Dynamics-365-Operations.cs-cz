---
title: Funkce INTVALUE ER
description: Toto téma obsahuje obecné informace o použití funkce INTVALUE elektronického výkaznictví.
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
ms.openlocfilehash: 2b279de39cf91c3919145735518034fc60cd3341
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917711"
---
# <span data-ttu-id="ef2b4-103"><a name="INTVALUE">Funkce INTVALUE ER</a></span><span class="sxs-lookup"><span data-stu-id="ef2b4-103"><a name="INTVALUE">INTVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef2b4-104">Funkce `INTVALUE` vrátí hodnotu *Int*, která představuje zadaný řetězec.</span><span class="sxs-lookup"><span data-stu-id="ef2b4-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="ef2b4-105">Syntaxe 1</span><span class="sxs-lookup"><span data-stu-id="ef2b4-105">Syntax 1</span></span>

```
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="ef2b4-106">Syntaxe 2</span><span class="sxs-lookup"><span data-stu-id="ef2b4-106">Syntax 2</span></span>

```
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="ef2b4-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="ef2b4-107">Arguments</span></span>

<span data-ttu-id="ef2b4-108">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="ef2b4-108">`text`: *String*</span></span>

<span data-ttu-id="ef2b4-109">Textová hodnota, která musí být převedena na číslo *Int*.</span><span class="sxs-lookup"><span data-stu-id="ef2b4-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="ef2b4-110">`number`: *reálné číslo* nebo *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="ef2b4-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="ef2b4-111">Číselná hodnota *Reálné* nebo *Celé číslo*, která musí být převedena na číslo *Int*.</span><span class="sxs-lookup"><span data-stu-id="ef2b4-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="ef2b4-112">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="ef2b4-112">Return values</span></span>

<span data-ttu-id="ef2b4-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="ef2b4-113">*Int*</span></span>

<span data-ttu-id="ef2b4-114">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="ef2b4-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ef2b4-115">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="ef2b4-115">Usage notes</span></span>

<span data-ttu-id="ef2b4-116">Desetinná místa jsou oříznuta.</span><span class="sxs-lookup"><span data-stu-id="ef2b4-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="ef2b4-117">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="ef2b4-117">Example 1</span></span>

<span data-ttu-id="ef2b4-118">`INTVALUE ("100.77")` vrátí hodnotu *Int* **100**.</span><span class="sxs-lookup"><span data-stu-id="ef2b4-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="ef2b4-119">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="ef2b4-119">Example 2</span></span>

<span data-ttu-id="ef2b4-120">`INTVALUE (-100.77)` vrátí hodnotu *Int* **-100**.</span><span class="sxs-lookup"><span data-stu-id="ef2b4-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ef2b4-121">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="ef2b4-121">Additional resources</span></span>

[<span data-ttu-id="ef2b4-122">Funkce převodu typu</span><span class="sxs-lookup"><span data-stu-id="ef2b4-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
