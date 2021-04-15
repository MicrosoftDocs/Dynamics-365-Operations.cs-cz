---
title: Funkce INT64VALUE ER
description: Toto téma obsahuje obecné informace o použití funkce INT64VALUE elektronického výkaznictví.
author: NickSelin
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
ms.openlocfilehash: 89a26e867579bcb34a9bae33fa0b98e1ecfe9995
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755389"
---
# <a name="int64value-er-function"></a><span data-ttu-id="2f2f2-103">Funkce INT64VALUE ER</span><span class="sxs-lookup"><span data-stu-id="2f2f2-103">INT64VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f2f2-104">Funkce `INT64VALUE` vrátí hodnotu *Int64*, která představuje zadaný řetězec.</span><span class="sxs-lookup"><span data-stu-id="2f2f2-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="2f2f2-105">Syntaxe 1</span><span class="sxs-lookup"><span data-stu-id="2f2f2-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="2f2f2-106">Syntaxe 2</span><span class="sxs-lookup"><span data-stu-id="2f2f2-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="2f2f2-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="2f2f2-107">Arguments</span></span>

<span data-ttu-id="2f2f2-108">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="2f2f2-108">`text`: *String*</span></span>

<span data-ttu-id="2f2f2-109">Textová hodnota, která musí být převedena na číslo *Int64*.</span><span class="sxs-lookup"><span data-stu-id="2f2f2-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="2f2f2-110">`number`: *reálné číslo* nebo *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="2f2f2-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="2f2f2-111">Číselná hodnota *Reálné* nebo *Celé číslo*, která musí být převedena na číslo *Int64*.</span><span class="sxs-lookup"><span data-stu-id="2f2f2-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="2f2f2-112">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="2f2f2-112">Return values</span></span>

<span data-ttu-id="2f2f2-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="2f2f2-113">*Int64*</span></span>

<span data-ttu-id="2f2f2-114">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="2f2f2-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2f2f2-115">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="2f2f2-115">Usage notes</span></span>

<span data-ttu-id="2f2f2-116">Desetinná místa jsou oříznuta.</span><span class="sxs-lookup"><span data-stu-id="2f2f2-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="2f2f2-117">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="2f2f2-117">Example 1</span></span>

<span data-ttu-id="2f2f2-118">`INT64VALUE ("22565422744")` vrátí hodnotu *Int64* **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="2f2f2-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="2f2f2-119">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="2f2f2-119">Example 2</span></span>

<span data-ttu-id="2f2f2-120">`INT64VALUE ( VALUE("22565422744.77"))` vrátí hodnotu *Int64* **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="2f2f2-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2f2f2-121">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="2f2f2-121">Additional resources</span></span>

[<span data-ttu-id="2f2f2-122">Funkce převodu typu</span><span class="sxs-lookup"><span data-stu-id="2f2f2-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]