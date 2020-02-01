---
title: Funkce INT64VALUE ER
description: Toto téma obsahuje obecné informace o použití funkce INT64VALUE elektronického výkaznictví.
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
ms.openlocfilehash: 75df802b75454baeea75a8ceb32d5d045a77a3a0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916538"
---
# <span data-ttu-id="134ba-103"><a name="INT64VALUE">Funkce INT64VALUE ER</a></span><span class="sxs-lookup"><span data-stu-id="134ba-103"><a name="INT64VALUE">INT64VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="134ba-104">Funkce `INT64VALUE` vrátí hodnotu *Int64*, která představuje zadaný řetězec.</span><span class="sxs-lookup"><span data-stu-id="134ba-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="134ba-105">Syntaxe 1</span><span class="sxs-lookup"><span data-stu-id="134ba-105">Syntax 1</span></span>

```
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="134ba-106">Syntaxe 2</span><span class="sxs-lookup"><span data-stu-id="134ba-106">Syntax 2</span></span>

```
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="134ba-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="134ba-107">Arguments</span></span>

<span data-ttu-id="134ba-108">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="134ba-108">`text`: *String*</span></span>

<span data-ttu-id="134ba-109">Textová hodnota, která musí být převedena na číslo *Int64*.</span><span class="sxs-lookup"><span data-stu-id="134ba-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="134ba-110">`number`: *reálné číslo* nebo *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="134ba-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="134ba-111">Číselná hodnota *Reálné* nebo *Celé číslo*, která musí být převedena na číslo *Int64*.</span><span class="sxs-lookup"><span data-stu-id="134ba-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="134ba-112">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="134ba-112">Return values</span></span>

<span data-ttu-id="134ba-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="134ba-113">*Int64*</span></span>

<span data-ttu-id="134ba-114">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="134ba-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="134ba-115">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="134ba-115">Usage notes</span></span>

<span data-ttu-id="134ba-116">Desetinná místa jsou oříznuta.</span><span class="sxs-lookup"><span data-stu-id="134ba-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="134ba-117">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="134ba-117">Example 1</span></span>

<span data-ttu-id="134ba-118">`INT64VALUE ("22565422744")` vrátí hodnotu *Int64* **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="134ba-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="134ba-119">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="134ba-119">Example 2</span></span>

<span data-ttu-id="134ba-120">`INT64VALUE ( VALUE("22565422744.77"))` vrátí hodnotu *Int64* **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="134ba-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="134ba-121">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="134ba-121">Additional resources</span></span>

[<span data-ttu-id="134ba-122">Funkce převodu typu</span><span class="sxs-lookup"><span data-stu-id="134ba-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)