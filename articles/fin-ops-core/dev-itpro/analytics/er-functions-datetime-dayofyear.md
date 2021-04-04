---
title: Funkce el. výkaznictví DAYOFYEAR
description: Toto téma obsahuje obecné informace o použití funkce DAYOFYEAR elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: ba63c96355a6a7a1eccaddf39e47a3edb2d1e651
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563527"
---
# <a name="dayofyear-er-function"></a><span data-ttu-id="298e4-103">Funkce el. výkaznictví DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="298e4-103">DAYOFYEAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="298e4-104">Funkce `DAYOFYEAR` vrátí hodnotu typu *celé číslo*, které představuje počet dní mezi 1. lednem a zadaným datem.</span><span class="sxs-lookup"><span data-stu-id="298e4-104">The `DAYOFYEAR` function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="298e4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="298e4-105">Syntax</span></span>

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a><span data-ttu-id="298e4-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="298e4-106">Arguments</span></span>

<span data-ttu-id="298e4-107">`date`: *datum*</span><span class="sxs-lookup"><span data-stu-id="298e4-107">`date`: *Date*</span></span>

<span data-ttu-id="298e4-108">Hodnota kalendářního data, která představuje datum, které má být použito pro výpočet počtu dní.</span><span class="sxs-lookup"><span data-stu-id="298e4-108">A date value that represents the date to use for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="298e4-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="298e4-109">Return values</span></span>

<span data-ttu-id="298e4-110">*Celé číslo*</span><span class="sxs-lookup"><span data-stu-id="298e4-110">*Integer*</span></span>

<span data-ttu-id="298e4-111">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="298e4-111">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="298e4-112">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="298e4-112">Example 1</span></span>

<span data-ttu-id="298e4-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` vrací **61**.</span><span class="sxs-lookup"><span data-stu-id="298e4-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returns **61**.</span></span>

## <a name="example-2"></a><span data-ttu-id="298e4-114">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="298e4-114">Example 2</span></span>

<span data-ttu-id="298e4-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` vrací **1**.</span><span class="sxs-lookup"><span data-stu-id="298e4-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="298e4-116">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="298e4-116">Additional resources</span></span>

[<span data-ttu-id="298e4-117">Funkce data a času</span><span class="sxs-lookup"><span data-stu-id="298e4-117">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]