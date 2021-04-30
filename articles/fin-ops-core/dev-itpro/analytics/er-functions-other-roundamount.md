---
title: Funkce elektronického výkaznictví ROUNDAMOUNT
description: Toto téma obsahuje obecné informace o použití funkce ROUNDAMOUNT elektronického výkaznictví.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 7dfc7817eab68e9dd70ce84e68f26d14fd8cf1df
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891202"
---
# <a name="roundamount-er-function"></a><span data-ttu-id="2c844-103">Funkce elektronického výkaznictví ROUNDAMOUNT</span><span class="sxs-lookup"><span data-stu-id="2c844-103">ROUNDAMOUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c844-104">Funkce `ROUNDAMOUNT` vrátí hodnotu typu *reálné číslo* jako výsledek zaokrouhlení zadaného čísla na nejbližší násobek jiného čísla podle zadaného pravidla zaokrouhlení.</span><span class="sxs-lookup"><span data-stu-id="2c844-104">The `ROUNDAMOUNT` function returns a *Real* value as the result of the rounding of the specified number to the nearest multiple of another number according to the specified rounding rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c844-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c844-105">Syntax</span></span>

```vb
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a><span data-ttu-id="2c844-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="2c844-106">Arguments</span></span>

<span data-ttu-id="2c844-107">`number`: *celé číslo* nebo *reálné číslo*</span><span class="sxs-lookup"><span data-stu-id="2c844-107">`number`: *Int* or *Real*</span></span>

<span data-ttu-id="2c844-108">Číselná hodnota, která má být zaokrouhlena.</span><span class="sxs-lookup"><span data-stu-id="2c844-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="2c844-109">`decimals`: *celé číslo* nebo *reálné číslo*</span><span class="sxs-lookup"><span data-stu-id="2c844-109">`decimals`: *Int* or *Real*</span></span>

<span data-ttu-id="2c844-110">Číslo, na jehož násobek má být zaokrouhlena hodnota parametru `number`.</span><span class="sxs-lookup"><span data-stu-id="2c844-110">The number that the value of the `number` parameter must be rounded to a multiple of.</span></span>

<span data-ttu-id="2c844-111">`round rule`: *hodnota výčtu*</span><span class="sxs-lookup"><span data-stu-id="2c844-111">`round rule`: *Enum value*</span></span>

<span data-ttu-id="2c844-112">Výčtová hodnota výčtu **RoundOffType**, která definuje pravidlo zaokrouhlení.</span><span class="sxs-lookup"><span data-stu-id="2c844-112">An enumeration value of the **RoundOffType** enumeration that defines the rounding rule.</span></span> <span data-ttu-id="2c844-113">Tento výčet nabízí následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="2c844-113">This enumeration offers the following values:</span></span>

- <span data-ttu-id="2c844-114">Normální (Ordinary)</span><span class="sxs-lookup"><span data-stu-id="2c844-114">Normal (Ordinary)</span></span>
- <span data-ttu-id="2c844-115">Zaokrouhlení dolů (RoundDown)</span><span class="sxs-lookup"><span data-stu-id="2c844-115">Downward (RoundDown)</span></span>
- <span data-ttu-id="2c844-116">Zaokrouhlení nahoru (RoundUp)</span><span class="sxs-lookup"><span data-stu-id="2c844-116">Rounding-up (RoundUp)</span></span>

## <a name="return-values"></a><span data-ttu-id="2c844-117">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="2c844-117">Return values</span></span>

<span data-ttu-id="2c844-118">*Reálný*</span><span class="sxs-lookup"><span data-stu-id="2c844-118">*Real*</span></span>

<span data-ttu-id="2c844-119">Výsledná číselná hodnota je násobkem hodnoty určené parametrem `decimals` a je nejblíže hodnotě určené parametrem `number`.</span><span class="sxs-lookup"><span data-stu-id="2c844-119">The resulting numeric value is a multiple of the value specified by the `decimals` parameter and is closest to the value specified by the `number` parameter.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2c844-120">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="2c844-120">Usage notes</span></span>

<span data-ttu-id="2c844-121">Pokud je parametr `number` nulový, vrátí funkce vždy nulu.</span><span class="sxs-lookup"><span data-stu-id="2c844-121">When the `number` parameter is zero, this function always returns zero.</span></span>

<span data-ttu-id="2c844-122">Pokud je parametr `decimals` nulový, zaokrouhlí tato funkce na výchozí hodnotu zaokrouhlení.</span><span class="sxs-lookup"><span data-stu-id="2c844-122">When the `decimals` parameter is zero, this function rounds to the default round-off value.</span></span> <span data-ttu-id="2c844-123">Pokud je parametr `round rule` nastaven na **RoundOffType.Ordinary**, výchozí hodnota zaokrouhlení bude **0,01**.</span><span class="sxs-lookup"><span data-stu-id="2c844-123">When the `round rule` parameter is set to **RoundOffType.Ordinary**, the default round-off value is **0.01**.</span></span> <span data-ttu-id="2c844-124">V opačném případě je výchozí hodnota zaokrouhlení **1,0**.</span><span class="sxs-lookup"><span data-stu-id="2c844-124">Otherwise, the default round-off value is **1.0**.</span></span>

<span data-ttu-id="2c844-125">Pokud je parametr `round rule` nastaven na hodnotu **RoundOffType.Ordinary**, tato funkce jej zaokrouhlí na nejbližší zaokrouhlenou částku.</span><span class="sxs-lookup"><span data-stu-id="2c844-125">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function rounds to the nearest round-off amount.</span></span>

<span data-ttu-id="2c844-126">Pokud je parametr `round rule` nastaven na hodnotu **RoundOffType.RoundDown**, tato funkce zaokrouhlí směrem k nule na nejbližší zaokrouhlenou částku.</span><span class="sxs-lookup"><span data-stu-id="2c844-126">When the `round rule` parameter is set to **RoundOffType.RoundDown**, this function rounds towards zero to the nearest round-off amount.</span></span>

<span data-ttu-id="2c844-127">Pokud je parametr `round rule` nastaven na hodnotu **RoundOffType.RoundUp**, tato funkce zaokrouhlí směrem od nuly na nejbližší zaokrouhlenou částku.</span><span class="sxs-lookup"><span data-stu-id="2c844-127">When the `round rule` parameter is set to **RoundOffType.RoundUp**, this function rounds away from zero to the nearest round-off amount.</span></span>

<span data-ttu-id="2c844-128">Pokud je parametr `round rule` nastaven na **RoundOffType.Ordinary**, tato funkce se zachová podobně jako funkce aplikace Excel [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) a X++ [Round](../dev-ref/xpp-math-run-time-functions.md#round).</span><span class="sxs-lookup"><span data-stu-id="2c844-128">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function behaves like the [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel function and the [ROUND](../dev-ref/xpp-math-run-time-functions.md#round) X++ function.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c844-129">Poznámky</span><span class="sxs-lookup"><span data-stu-id="2c844-129">Remarks</span></span>

<span data-ttu-id="2c844-130">Chcete-li zaokrouhlit číselnou hodnotu na zadaný počet desetinných míst, použijte funkci [ROUND](er-functions-mathematical-round.md).</span><span class="sxs-lookup"><span data-stu-id="2c844-130">To round a numeric value to a specified number of decimal places, use the [ROUND](er-functions-mathematical-round.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="2c844-131">Příklad</span><span class="sxs-lookup"><span data-stu-id="2c844-131">Example</span></span>

<span data-ttu-id="2c844-132">Pokud je parametr **model.RoundOff** nastaven na **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` vrátí 7,35.</span><span class="sxs-lookup"><span data-stu-id="2c844-132">If the **model.RoundOff** parameter is set to **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="2c844-133">Pokud je parametr **model.RoundOff** nastaven na **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` vrátí 7,35.</span><span class="sxs-lookup"><span data-stu-id="2c844-133">If the **model.RoundOff** parameter is set to **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="2c844-134">Pokud je parametr **model.RoundOff** nastaven na **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` vrátí 8,4.</span><span class="sxs-lookup"><span data-stu-id="2c844-134">If the **model.RoundOff** parameter is set to **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 8.4.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c844-135">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="2c844-135">Additional resources</span></span>

[<span data-ttu-id="2c844-136">Další funkce (konkrétní pro obchodní domény)</span><span class="sxs-lookup"><span data-stu-id="2c844-136">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

[<span data-ttu-id="2c844-137">Matematické funkce</span><span class="sxs-lookup"><span data-stu-id="2c844-137">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]