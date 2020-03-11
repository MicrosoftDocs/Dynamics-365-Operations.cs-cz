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
ms.openlocfilehash: 5e06236bf1d158a4cf579b8b89cc0a5f7d815c38
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042638"
---
# <span data-ttu-id="305dd-103"><a name="INTVALUE">Funkce INTVALUE ER</a></span><span class="sxs-lookup"><span data-stu-id="305dd-103"><a name="INTVALUE">INTVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="305dd-104">Funkce `INTVALUE` vrátí hodnotu *Int*, která představuje zadaný řetězec.</span><span class="sxs-lookup"><span data-stu-id="305dd-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="305dd-105">Syntaxe 1</span><span class="sxs-lookup"><span data-stu-id="305dd-105">Syntax 1</span></span>

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="305dd-106">Syntaxe 2</span><span class="sxs-lookup"><span data-stu-id="305dd-106">Syntax 2</span></span>

```vb
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="305dd-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="305dd-107">Arguments</span></span>

<span data-ttu-id="305dd-108">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="305dd-108">`text`: *String*</span></span>

<span data-ttu-id="305dd-109">Textová hodnota, která musí být převedena na číslo *Int*.</span><span class="sxs-lookup"><span data-stu-id="305dd-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="305dd-110">`number`: *reálné číslo* nebo *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="305dd-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="305dd-111">Číselná hodnota *Reálné* nebo *Celé číslo*, která musí být převedena na číslo *Int*.</span><span class="sxs-lookup"><span data-stu-id="305dd-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="305dd-112">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="305dd-112">Return values</span></span>

<span data-ttu-id="305dd-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="305dd-113">*Int*</span></span>

<span data-ttu-id="305dd-114">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="305dd-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="305dd-115">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="305dd-115">Usage notes</span></span>

<span data-ttu-id="305dd-116">Desetinná místa jsou oříznuta.</span><span class="sxs-lookup"><span data-stu-id="305dd-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="305dd-117">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="305dd-117">Example 1</span></span>

<span data-ttu-id="305dd-118">`INTVALUE ("100.77")` vrátí hodnotu *Int* **100**.</span><span class="sxs-lookup"><span data-stu-id="305dd-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="305dd-119">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="305dd-119">Example 2</span></span>

<span data-ttu-id="305dd-120">`INTVALUE (-100.77)` vrátí hodnotu *Int* **-100**.</span><span class="sxs-lookup"><span data-stu-id="305dd-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="305dd-121">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="305dd-121">Additional resources</span></span>

[<span data-ttu-id="305dd-122">Funkce převodu typu</span><span class="sxs-lookup"><span data-stu-id="305dd-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
