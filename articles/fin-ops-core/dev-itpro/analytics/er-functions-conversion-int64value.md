---
title: Funkce INT64VALUE ER
description: Toto téma obsahuje obecné informace o použití funkce INT64VALUE elektronického výkaznictví.
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
ms.openlocfilehash: 9db2e9abcac36a8331a494c886218bbfc82e93aa
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561487"
---
# <a name="int64value-er-function"></a><span data-ttu-id="3dd63-103">Funkce INT64VALUE ER</span><span class="sxs-lookup"><span data-stu-id="3dd63-103">INT64VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3dd63-104">Funkce `INT64VALUE` vrátí hodnotu *Int64*, která představuje zadaný řetězec.</span><span class="sxs-lookup"><span data-stu-id="3dd63-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="3dd63-105">Syntaxe 1</span><span class="sxs-lookup"><span data-stu-id="3dd63-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="3dd63-106">Syntaxe 2</span><span class="sxs-lookup"><span data-stu-id="3dd63-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="3dd63-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="3dd63-107">Arguments</span></span>

<span data-ttu-id="3dd63-108">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="3dd63-108">`text`: *String*</span></span>

<span data-ttu-id="3dd63-109">Textová hodnota, která musí být převedena na číslo *Int64*.</span><span class="sxs-lookup"><span data-stu-id="3dd63-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="3dd63-110">`number`: *reálné číslo* nebo *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="3dd63-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="3dd63-111">Číselná hodnota *Reálné* nebo *Celé číslo*, která musí být převedena na číslo *Int64*.</span><span class="sxs-lookup"><span data-stu-id="3dd63-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="3dd63-112">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="3dd63-112">Return values</span></span>

<span data-ttu-id="3dd63-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="3dd63-113">*Int64*</span></span>

<span data-ttu-id="3dd63-114">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="3dd63-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3dd63-115">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="3dd63-115">Usage notes</span></span>

<span data-ttu-id="3dd63-116">Desetinná místa jsou oříznuta.</span><span class="sxs-lookup"><span data-stu-id="3dd63-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="3dd63-117">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="3dd63-117">Example 1</span></span>

<span data-ttu-id="3dd63-118">`INT64VALUE ("22565422744")` vrátí hodnotu *Int64* **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="3dd63-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="3dd63-119">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="3dd63-119">Example 2</span></span>

<span data-ttu-id="3dd63-120">`INT64VALUE ( VALUE("22565422744.77"))` vrátí hodnotu *Int64* **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="3dd63-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3dd63-121">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="3dd63-121">Additional resources</span></span>

[<span data-ttu-id="3dd63-122">Funkce převodu typu</span><span class="sxs-lookup"><span data-stu-id="3dd63-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]