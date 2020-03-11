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
ms.openlocfilehash: 7fcb8a617507801d82d16175e9e86c9193091a12
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042681"
---
# <span data-ttu-id="98648-103"><a name="INT64VALUE">Funkce INT64VALUE ER</a></span><span class="sxs-lookup"><span data-stu-id="98648-103"><a name="INT64VALUE">INT64VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98648-104">Funkce `INT64VALUE` vrátí hodnotu *Int64*, která představuje zadaný řetězec.</span><span class="sxs-lookup"><span data-stu-id="98648-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="98648-105">Syntaxe 1</span><span class="sxs-lookup"><span data-stu-id="98648-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="98648-106">Syntaxe 2</span><span class="sxs-lookup"><span data-stu-id="98648-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="98648-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="98648-107">Arguments</span></span>

<span data-ttu-id="98648-108">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="98648-108">`text`: *String*</span></span>

<span data-ttu-id="98648-109">Textová hodnota, která musí být převedena na číslo *Int64*.</span><span class="sxs-lookup"><span data-stu-id="98648-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="98648-110">`number`: *reálné číslo* nebo *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="98648-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="98648-111">Číselná hodnota *Reálné* nebo *Celé číslo*, která musí být převedena na číslo *Int64*.</span><span class="sxs-lookup"><span data-stu-id="98648-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="98648-112">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="98648-112">Return values</span></span>

<span data-ttu-id="98648-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="98648-113">*Int64*</span></span>

<span data-ttu-id="98648-114">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="98648-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="98648-115">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="98648-115">Usage notes</span></span>

<span data-ttu-id="98648-116">Desetinná místa jsou oříznuta.</span><span class="sxs-lookup"><span data-stu-id="98648-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="98648-117">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="98648-117">Example 1</span></span>

<span data-ttu-id="98648-118">`INT64VALUE ("22565422744")` vrátí hodnotu *Int64* **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="98648-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="98648-119">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="98648-119">Example 2</span></span>

<span data-ttu-id="98648-120">`INT64VALUE ( VALUE("22565422744.77"))` vrátí hodnotu *Int64* **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="98648-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="98648-121">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="98648-121">Additional resources</span></span>

[<span data-ttu-id="98648-122">Funkce převodu typu</span><span class="sxs-lookup"><span data-stu-id="98648-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
