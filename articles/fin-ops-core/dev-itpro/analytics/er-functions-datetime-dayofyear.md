---
title: Funkce el. výkaznictví DAYOFYEAR
description: Toto téma obsahuje obecné informace o použití funkce DAYOFYEAR elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: d24aabb582151b0b357b64a988cc932a9c9f3cea
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070660"
---
# <span data-ttu-id="62eea-103"><a name="DAYOFYEAR">Funkce el. výkaznictví DAYOFYEAR</a></span><span class="sxs-lookup"><span data-stu-id="62eea-103"><a name="DAYOFYEAR">DAYOFYEAR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62eea-104">Funkce `DAYOFYEAR` vrátí hodnotu typu *celé číslo*, které představuje počet dní mezi 1. lednem a zadaným datem.</span><span class="sxs-lookup"><span data-stu-id="62eea-104">The `DAYOFYEAR` function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="62eea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62eea-105">Syntax</span></span>

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a><span data-ttu-id="62eea-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="62eea-106">Arguments</span></span>

<span data-ttu-id="62eea-107">`date`: *datum*</span><span class="sxs-lookup"><span data-stu-id="62eea-107">`date`: *Date*</span></span>

<span data-ttu-id="62eea-108">Hodnota kalendářního data, která představuje datum, které má být použito pro výpočet počtu dní.</span><span class="sxs-lookup"><span data-stu-id="62eea-108">A date value that represents the date to use for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="62eea-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="62eea-109">Return values</span></span>

<span data-ttu-id="62eea-110">*Celé číslo*</span><span class="sxs-lookup"><span data-stu-id="62eea-110">*Integer*</span></span>

<span data-ttu-id="62eea-111">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="62eea-111">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="62eea-112">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="62eea-112">Example 1</span></span>

<span data-ttu-id="62eea-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` vrací **61**.</span><span class="sxs-lookup"><span data-stu-id="62eea-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returns **61**.</span></span>

## <a name="example-2"></a><span data-ttu-id="62eea-114">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="62eea-114">Example 2</span></span>

<span data-ttu-id="62eea-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` vrací **1**.</span><span class="sxs-lookup"><span data-stu-id="62eea-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="62eea-116">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="62eea-116">Additional resources</span></span>

[<span data-ttu-id="62eea-117">Funkce data a času</span><span class="sxs-lookup"><span data-stu-id="62eea-117">Date and time functions</span></span>](er-functions-category-datetime.md)
