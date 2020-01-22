---
title: Funkce el. výkaznictví ADDDAYS
description: Toto téma obsahuje obecné informace o použití funkce ADDDAYS elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: dd1290538c506cd0db6eb21a304ff9812c808f17
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916446"
---
# <span data-ttu-id="16052-103"><a name="ADDDAYS">Funkce el. výkaznictví ADDDAYS</a></span><span class="sxs-lookup"><span data-stu-id="16052-103"><a name="ADDDAYS">ADDDAYS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16052-104">Funkce `ADDDAYS` vypočítá hodnotu *datum a čas*, která představuje zadaný počet dní před nebo po zadaném počátečním datu.</span><span class="sxs-lookup"><span data-stu-id="16052-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="16052-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16052-105">Syntax</span></span>

```
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="16052-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="16052-106">Arguments</span></span>

<span data-ttu-id="16052-107">`datetime`: *datum a čas*</span><span class="sxs-lookup"><span data-stu-id="16052-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="16052-108">Hodnota data a času, která představuje počáteční datum.</span><span class="sxs-lookup"><span data-stu-id="16052-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="16052-109">`days`: *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="16052-109">`days`: *Integer*</span></span>

<span data-ttu-id="16052-110">Počet dnů před nebo po `datetime`.</span><span class="sxs-lookup"><span data-stu-id="16052-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="16052-111">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="16052-111">Return values</span></span>

<span data-ttu-id="16052-112">*Datum a čas*</span><span class="sxs-lookup"><span data-stu-id="16052-112">*DateTime*</span></span>

<span data-ttu-id="16052-113">Výsledná hodnota data a času.</span><span class="sxs-lookup"><span data-stu-id="16052-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="16052-114">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="16052-114">Usage notes</span></span>

<span data-ttu-id="16052-115">Kladná hodnota pro `days` znamená datum v budoucnosti.</span><span class="sxs-lookup"><span data-stu-id="16052-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="16052-116">Záporná hodnota znamená datum v minulosti.</span><span class="sxs-lookup"><span data-stu-id="16052-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="16052-117">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="16052-117">Example 1</span></span>

<span data-ttu-id="16052-118">`ADDDAYS (NOW(), 7)` vrátí datum a čas sedm dní v budoucnosti.</span><span class="sxs-lookup"><span data-stu-id="16052-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="16052-119">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="16052-119">Example 2</span></span>

<span data-ttu-id="16052-120">`ADDDAYS (NOW(), -3)` vrátí datum a čas tři dny v minulosti.</span><span class="sxs-lookup"><span data-stu-id="16052-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="16052-121">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="16052-121">Additional resources</span></span>

[<span data-ttu-id="16052-122">Funkce data a času</span><span class="sxs-lookup"><span data-stu-id="16052-122">Date and time functions</span></span>](er-functions-category-datetime.md)
