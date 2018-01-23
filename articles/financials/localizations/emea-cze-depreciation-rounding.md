---
title: " Zaokrouhlení odpisu"
description: "Toto téma vysvětluje, jak můžete zaokrouhlit částky odpisu dlouhodobého majetku nahoru nebo dolů na nejbližší celé číslo."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265204
ms.search.region: Czech Republic
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a523ff097eedf9a4a2cb0341b3be9d05abfa09fa
ms.openlocfilehash: 794d917c19661ee2b54263e26561933968d631b7
ms.contentlocale: cs-cz
ms.lasthandoff: 01/23/2018

---

# <a name="depreciation-rounding"></a><span data-ttu-id="e968d-103"> Zaokrouhlení odpisu</span><span class="sxs-lookup"><span data-stu-id="e968d-103">Depreciation rounding</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e968d-104">Toto téma vysvětluje, jak můžete zaokrouhlit částky odpisu dlouhodobého majetku nahoru nebo dolů na nejbližší celé číslo.</span><span class="sxs-lookup"><span data-stu-id="e968d-104">This topic explains how you can round fixed asset depreciation amounts up or down to the nearest whole number.</span></span> 

<span data-ttu-id="e968d-105">Částky odpisu jsou zaokrouhleny nahoru nebo dolů, na základě hodnoty zadané v poli **Zaokrouhlit odpis** a metody zaokrouhlení, která je určena v poli **Metoda zaokrouhlení** na stránce **Knihy odpisů**.</span><span class="sxs-lookup"><span data-stu-id="e968d-105">Depreciation amounts are rounded up or down, based on the value that is entered in the **Round off depreciation** field and the rounding method that is specified in the **Rounding method** field on the **Depreciation books** page.</span></span> <span data-ttu-id="e968d-106">Částka odpisu (x) s hodnotou **Zaokrouhlování odpisu** (y), se částka odpisu (z) vypočítá jako x ÷ y.</span><span class="sxs-lookup"><span data-stu-id="e968d-106">For a depreciation amount (x) that has a **Round off depreciation** value (y), the depreciation amount (z) is calculated as x ÷ y.</span></span> <span data-ttu-id="e968d-107">Částka odpisu zaokrouhlená nahoru nebo dolů se počítá jako z × y.</span><span class="sxs-lookup"><span data-stu-id="e968d-107">The rounded-up or rounded-down depreciation amount is calculated as z × y.</span></span> <span data-ttu-id="e968d-108">Například pro částku odpisu CZK 1 111.11 a hodnotu **Zaokrouhlování odpisu** **1** se částka odpisu vypočte jako CZK 1 111.11 ÷ 1 nebo CZK 1 111.11.</span><span class="sxs-lookup"><span data-stu-id="e968d-108">For example, for the depreciation amount CZK 1,111.11 and a **Round off depreciation** value of **1**, the depreciation amount is calculated as CZK 1,111.11 ÷ 1, or CZK 1,111.11.</span></span> <span data-ttu-id="e968d-109">Částka odpisu zaokrouhlená nahoru se počítá jako CZK 1 112 × 1 nebo CZK 1 112.</span><span class="sxs-lookup"><span data-stu-id="e968d-109">The rounded-up depreciation amount is calculated as CZK 1,112 × 1, or CZK 1,112.</span></span> <span data-ttu-id="e968d-110">Částka odpisu zaokrouhlená dolů se počítá jako CZK 1 111 × 1 nebo CZK 1 111.</span><span class="sxs-lookup"><span data-stu-id="e968d-110">The rounded-down depreciation amount is calculated as CZK 1,111 × 1, or CZK 1,111.</span></span> <span data-ttu-id="e968d-111">Následující tabulka uvádí částky odpisů zaokrouhlené nahoru a dolů pro různé částky odpisu a hodnoty **Zaokrouhlení odpisu**.</span><span class="sxs-lookup"><span data-stu-id="e968d-111">The following table shows rounded-up and rounded-down depreciation amounts for various depreciation amounts and **Round off depreciation** values.</span></span>

|<span data-ttu-id="e968d-112">Odpisovaná částka (x)</span><span class="sxs-lookup"><span data-stu-id="e968d-112">Depreciation amount (x)</span></span>|<span data-ttu-id="e968d-113">Zaokrouhlení odpisu (y)</span><span class="sxs-lookup"><span data-stu-id="e968d-113">Round off depreciation (y)</span></span>|<span data-ttu-id="e968d-114">Částka odpisu (z = x ÷ y)</span><span class="sxs-lookup"><span data-stu-id="e968d-114">Depreciation amount (z = x ÷ y)</span></span>|<span data-ttu-id="e968d-115">Normální metoda zaokrouhlování</span><span class="sxs-lookup"><span data-stu-id="e968d-115">Normal rounding method</span></span>| <span data-ttu-id="e968d-116">Metoda zaokrouhlování dolů</span><span class="sxs-lookup"><span data-stu-id="e968d-116">Downward rounding method</span></span>|<span data-ttu-id="e968d-117">Metoda zaokrouhlování nahoru</span><span class="sxs-lookup"><span data-stu-id="e968d-117">Rounding-up rounding method</span></span>|
|-----------------------|-----------------------|-----------------------|-----------------------|-----------------------|-----------------------|
|<span data-ttu-id="e968d-118">1 111,11 Kč</span><span class="sxs-lookup"><span data-stu-id="e968d-118">CZK 1,111.11</span></span>|<span data-ttu-id="e968d-119">1</span><span class="sxs-lookup"><span data-stu-id="e968d-119">1</span></span>|<span data-ttu-id="e968d-120">CZK 1 111.11 ÷ 1 = CZK 1 111.11</span><span class="sxs-lookup"><span data-stu-id="e968d-120">CZK 1,111.11 ÷ 1 = CZK 1,111.11</span></span>|<span data-ttu-id="e968d-121">1 111,1 Kč</span><span class="sxs-lookup"><span data-stu-id="e968d-121">CZK 1,111.1</span></span>|<span data-ttu-id="e968d-122">1 111,11 Kč je zaokrouhleno nahoru na 1 112 Kč.</span><span class="sxs-lookup"><span data-stu-id="e968d-122">CZK 1,111.11 is rounded up to CZK 1,112.</span></span> <span data-ttu-id="e968d-123">Výsledná částka odpisu: CZK 1 112 × 1 = CZK 1 112</span><span class="sxs-lookup"><span data-stu-id="e968d-123">Final depreciation amount: CZK 1,112 × 1 = CZK 1,112</span></span>|<span data-ttu-id="e968d-124">1 111,11 Kč je zaokrouhleno dolů na 1 111 Kč.</span><span class="sxs-lookup"><span data-stu-id="e968d-124">CZK 1,111.11 is rounded down to CZK 1,111.</span></span> <span data-ttu-id="e968d-125">Výsledná částka odpisu: CZK 1 111 × 1 = CZK 1 111</span><span class="sxs-lookup"><span data-stu-id="e968d-125">Final depreciation amount: CZK 1,111 × 1 = CZK 1,111</span></span>|
|<span data-ttu-id="e968d-126">1 234,5 Kč</span><span class="sxs-lookup"><span data-stu-id="e968d-126">CZK 1,234.5</span></span>|<span data-ttu-id="e968d-127">10</span><span class="sxs-lookup"><span data-stu-id="e968d-127">10</span></span>|<span data-ttu-id="e968d-128">CZK 1 234.5 ÷ 10 = CZK 123,45</span><span class="sxs-lookup"><span data-stu-id="e968d-128">CZK 1,234.5 ÷ 10 = CZK 123.45</span></span>|<span data-ttu-id="e968d-129">1 235 Kč</span><span class="sxs-lookup"><span data-stu-id="e968d-129">CZK 1,235</span></span>|<span data-ttu-id="e968d-130">123,45 Kč je zaokrouhleno nahoru na 124 Kč.</span><span class="sxs-lookup"><span data-stu-id="e968d-130">CZK 123.45 is rounded up to CZK 124.</span></span> <span data-ttu-id="e968d-131">Výsledná částka odpisu: CZK 124 × 10 = CZK 1 240</span><span class="sxs-lookup"><span data-stu-id="e968d-131">Final depreciation amount: CZK 124 × 10 = CZK 1,240</span></span>|<span data-ttu-id="e968d-132">123,45 Kč je zaokrouhleno dolů na 123 Kč.</span><span class="sxs-lookup"><span data-stu-id="e968d-132">CZK 123.45 is rounded down to CZK 123.</span></span> <span data-ttu-id="e968d-133">Výsledná částka odpisu: CZK 123 × 10 = CZK 1 230</span><span class="sxs-lookup"><span data-stu-id="e968d-133">Final depreciation amount: CZK 123 × 10 = CZK 1,230</span></span>|




