---
title: Funkce INTVALUE ER
description: Toto téma obsahuje obecné informace o použití funkce INTVALUE elektronického výkaznictví.
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
ms.openlocfilehash: 64f43ad29d59ade1e124b6800734b003f6ca07df
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561463"
---
# <a name="intvalue-er-function"></a><span data-ttu-id="913f4-103">Funkce INTVALUE ER</span><span class="sxs-lookup"><span data-stu-id="913f4-103">INTVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="913f4-104">Funkce `INTVALUE` vrátí hodnotu *Int*, která představuje zadaný řetězec.</span><span class="sxs-lookup"><span data-stu-id="913f4-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="913f4-105">Syntaxe 1</span><span class="sxs-lookup"><span data-stu-id="913f4-105">Syntax 1</span></span>

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="913f4-106">Syntaxe 2</span><span class="sxs-lookup"><span data-stu-id="913f4-106">Syntax 2</span></span>

```vb
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="913f4-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="913f4-107">Arguments</span></span>

<span data-ttu-id="913f4-108">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="913f4-108">`text`: *String*</span></span>

<span data-ttu-id="913f4-109">Textová hodnota, která musí být převedena na číslo *Int*.</span><span class="sxs-lookup"><span data-stu-id="913f4-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="913f4-110">`number`: *reálné číslo* nebo *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="913f4-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="913f4-111">Číselná hodnota *Reálné* nebo *Celé číslo*, která musí být převedena na číslo *Int*.</span><span class="sxs-lookup"><span data-stu-id="913f4-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="913f4-112">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="913f4-112">Return values</span></span>

<span data-ttu-id="913f4-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="913f4-113">*Int*</span></span>

<span data-ttu-id="913f4-114">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="913f4-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="913f4-115">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="913f4-115">Usage notes</span></span>

<span data-ttu-id="913f4-116">Desetinná místa jsou oříznuta.</span><span class="sxs-lookup"><span data-stu-id="913f4-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="913f4-117">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="913f4-117">Example 1</span></span>

<span data-ttu-id="913f4-118">`INTVALUE ("100.77")` vrátí hodnotu *Int* **100**.</span><span class="sxs-lookup"><span data-stu-id="913f4-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="913f4-119">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="913f4-119">Example 2</span></span>

<span data-ttu-id="913f4-120">`INTVALUE (-100.77)` vrátí hodnotu *Int* **-100**.</span><span class="sxs-lookup"><span data-stu-id="913f4-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="913f4-121">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="913f4-121">Additional resources</span></span>

[<span data-ttu-id="913f4-122">Funkce převodu typu</span><span class="sxs-lookup"><span data-stu-id="913f4-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]