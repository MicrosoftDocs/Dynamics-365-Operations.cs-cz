---
title: Odpis koeficientem
description: Tento článek poskytuje přehled o metodě odpisu koeficientem.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5c36441e926cd5a82c802a350adf6b2ed6d6387
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176770"
---
# <a name="factor-depreciation"></a><span data-ttu-id="67e43-103">Odpis koeficientem</span><span class="sxs-lookup"><span data-stu-id="67e43-103">Factor depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67e43-104">Tento článek poskytuje přehled o metodě odpisu koeficientem.</span><span class="sxs-lookup"><span data-stu-id="67e43-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="67e43-105">Koeficienty jsou procenta, která se používají při odpisování majetku.</span><span class="sxs-lookup"><span data-stu-id="67e43-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="67e43-106">Když nastavíte odpisový plán dlouhodobého majetku a v poli **Metoda** na stránce **Odpisové profily** vyberete hodnotu **Koeficient**, můžete nastavit progresivní, degresivní nebo lineární metodu odepisování:</span><span class="sxs-lookup"><span data-stu-id="67e43-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="67e43-107">Jestliže vyberete progresivní metodu odepisování, částka odpisu se v každém období odpisu zvýší.</span><span class="sxs-lookup"><span data-stu-id="67e43-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="67e43-108">Jestliže vyberete degresivní metodu odepisování, částka odpisu za dané období se bude v průběhu let snižovat.</span><span class="sxs-lookup"><span data-stu-id="67e43-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="67e43-109">Jestliže vyberete lineární metodu odepisování, odpis bude v každém období stejný.</span><span class="sxs-lookup"><span data-stu-id="67e43-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="67e43-110">Níže uvedená pravidla a příklady ukazují, jak lze nastavit koeficienty pro jednotlivé typy odpisů.</span><span class="sxs-lookup"><span data-stu-id="67e43-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="67e43-111">Když vyberete možnost **Faktor** v poli **Metoda**, zobrazí se pole **Faktor** a pole **Interval**.</span><span class="sxs-lookup"><span data-stu-id="67e43-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="67e43-112">Progresivní metoda odepisování</span><span class="sxs-lookup"><span data-stu-id="67e43-112">Progressive depreciation</span></span>
<span data-ttu-id="67e43-113">Hodnota v poli **Koeficient** je větší než **50**.</span><span class="sxs-lookup"><span data-stu-id="67e43-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="67e43-114">Příklad</span><span class="sxs-lookup"><span data-stu-id="67e43-114">Example</span></span>

<span data-ttu-id="67e43-115">Pořizovací cena je 100 000, koeficient je 70, doba životnosti je 10 let a odepisování začíná 1. ledna.</span><span class="sxs-lookup"><span data-stu-id="67e43-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="67e43-116">Částky odpisů a zůstatkové účetní hodnoty jsou zobrazeny pouze pro prvních šest let životnosti.</span><span class="sxs-lookup"><span data-stu-id="67e43-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="67e43-117">Rok</span><span class="sxs-lookup"><span data-stu-id="67e43-117">Year</span></span> | <span data-ttu-id="67e43-118">Období</span><span class="sxs-lookup"><span data-stu-id="67e43-118">Period</span></span>      | <span data-ttu-id="67e43-119">Odpisovaná částka</span><span class="sxs-lookup"><span data-stu-id="67e43-119">Depreciation amount</span></span> | <span data-ttu-id="67e43-120">Zůstatková účetní hodnota</span><span class="sxs-lookup"><span data-stu-id="67e43-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="67e43-121">1</span><span class="sxs-lookup"><span data-stu-id="67e43-121">1</span></span>    | <span data-ttu-id="67e43-122">31. prosince</span><span class="sxs-lookup"><span data-stu-id="67e43-122">December 31</span></span> | <span data-ttu-id="67e43-123">307,69</span><span class="sxs-lookup"><span data-stu-id="67e43-123">307.69</span></span>              | <span data-ttu-id="67e43-124">99 692,31</span><span class="sxs-lookup"><span data-stu-id="67e43-124">99,692.31</span></span>             |
| <span data-ttu-id="67e43-125">2</span><span class="sxs-lookup"><span data-stu-id="67e43-125">2</span></span>    | <span data-ttu-id="67e43-126">31. prosince</span><span class="sxs-lookup"><span data-stu-id="67e43-126">December 31</span></span> | <span data-ttu-id="67e43-127">1 447,21</span><span class="sxs-lookup"><span data-stu-id="67e43-127">1,447.21</span></span>            | <span data-ttu-id="67e43-128">98 245,10</span><span class="sxs-lookup"><span data-stu-id="67e43-128">98,245.10</span></span>             |
| <span data-ttu-id="67e43-129">3</span><span class="sxs-lookup"><span data-stu-id="67e43-129">3</span></span>    | <span data-ttu-id="67e43-130">31. prosince</span><span class="sxs-lookup"><span data-stu-id="67e43-130">December 31</span></span> | <span data-ttu-id="67e43-131">3 104,50</span><span class="sxs-lookup"><span data-stu-id="67e43-131">3,104.50</span></span>            | <span data-ttu-id="67e43-132">95 140,60</span><span class="sxs-lookup"><span data-stu-id="67e43-132">95,140.60</span></span>             |
| <span data-ttu-id="67e43-133">4</span><span class="sxs-lookup"><span data-stu-id="67e43-133">4</span></span>    | <span data-ttu-id="67e43-134">31. prosince</span><span class="sxs-lookup"><span data-stu-id="67e43-134">December 31</span></span> | <span data-ttu-id="67e43-135">5 150,21</span><span class="sxs-lookup"><span data-stu-id="67e43-135">5,150.21</span></span>            | <span data-ttu-id="67e43-136">89 990,39</span><span class="sxs-lookup"><span data-stu-id="67e43-136">89,990.39</span></span>             |
| <span data-ttu-id="67e43-137">5</span><span class="sxs-lookup"><span data-stu-id="67e43-137">5</span></span>    | <span data-ttu-id="67e43-138">31. prosince</span><span class="sxs-lookup"><span data-stu-id="67e43-138">December 31</span></span> | <span data-ttu-id="67e43-139">7 522,95</span><span class="sxs-lookup"><span data-stu-id="67e43-139">7,522.95</span></span>            | <span data-ttu-id="67e43-140">82 467,44</span><span class="sxs-lookup"><span data-stu-id="67e43-140">82,467.44</span></span>             |
| <span data-ttu-id="67e43-141">6</span><span class="sxs-lookup"><span data-stu-id="67e43-141">6</span></span>    | <span data-ttu-id="67e43-142">31. prosince</span><span class="sxs-lookup"><span data-stu-id="67e43-142">December 31</span></span> | <span data-ttu-id="67e43-143">10 184,06</span><span class="sxs-lookup"><span data-stu-id="67e43-143">10,184.06</span></span>           | <span data-ttu-id="67e43-144">72 283,38</span><span class="sxs-lookup"><span data-stu-id="67e43-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="67e43-145">Degresivní metoda odepisování</span><span class="sxs-lookup"><span data-stu-id="67e43-145">Digressive depreciation</span></span>
<span data-ttu-id="67e43-146">Hodnota v poli **Koeficient** je menší než **50**.</span><span class="sxs-lookup"><span data-stu-id="67e43-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="67e43-147">Příklad</span><span class="sxs-lookup"><span data-stu-id="67e43-147">Example</span></span>

<span data-ttu-id="67e43-148">Pořizovací cena je 100 000, koeficient je 20, doba životnosti je 10 let a odepisování začíná 1. ledna.</span><span class="sxs-lookup"><span data-stu-id="67e43-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="67e43-149">Částky odpisů a zůstatkové účetní hodnoty jsou zobrazeny pouze pro prvních šest let životnosti.</span><span class="sxs-lookup"><span data-stu-id="67e43-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="67e43-150">Rok</span><span class="sxs-lookup"><span data-stu-id="67e43-150">Year</span></span> | <span data-ttu-id="67e43-151">Období</span><span class="sxs-lookup"><span data-stu-id="67e43-151">Period</span></span>      | <span data-ttu-id="67e43-152">Odpisovaná částka</span><span class="sxs-lookup"><span data-stu-id="67e43-152">Depreciation amount</span></span> | <span data-ttu-id="67e43-153">Zůstatková účetní hodnota</span><span class="sxs-lookup"><span data-stu-id="67e43-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="67e43-154">1</span><span class="sxs-lookup"><span data-stu-id="67e43-154">1</span></span>    | <span data-ttu-id="67e43-155">31. prosince</span><span class="sxs-lookup"><span data-stu-id="67e43-155">December 31</span></span> | <span data-ttu-id="67e43-156">56 080,43</span><span class="sxs-lookup"><span data-stu-id="67e43-156">56,080.43</span></span>           | <span data-ttu-id="67e43-157">43 919,57</span><span class="sxs-lookup"><span data-stu-id="67e43-157">43,919.57</span></span>             |
| <span data-ttu-id="67e43-158">2</span><span class="sxs-lookup"><span data-stu-id="67e43-158">2</span></span>    | <span data-ttu-id="67e43-159">31. prosince</span><span class="sxs-lookup"><span data-stu-id="67e43-159">December 31</span></span> | <span data-ttu-id="67e43-160">10 665,70</span><span class="sxs-lookup"><span data-stu-id="67e43-160">10,665.70</span></span>           | <span data-ttu-id="67e43-161">33 253,87</span><span class="sxs-lookup"><span data-stu-id="67e43-161">33,253.87</span></span>             |
| <span data-ttu-id="67e43-162">3</span><span class="sxs-lookup"><span data-stu-id="67e43-162">3</span></span>    | <span data-ttu-id="67e43-163">31. prosince</span><span class="sxs-lookup"><span data-stu-id="67e43-163">December 31</span></span> | <span data-ttu-id="67e43-164">7 156,22</span><span class="sxs-lookup"><span data-stu-id="67e43-164">7,156.22</span></span>            | <span data-ttu-id="67e43-165">26 097,65</span><span class="sxs-lookup"><span data-stu-id="67e43-165">26,097.65</span></span>             |
| <span data-ttu-id="67e43-166">4</span><span class="sxs-lookup"><span data-stu-id="67e43-166">4</span></span>    | <span data-ttu-id="67e43-167">31. prosince</span><span class="sxs-lookup"><span data-stu-id="67e43-167">December 31</span></span> | <span data-ttu-id="67e43-168">5 538,06</span><span class="sxs-lookup"><span data-stu-id="67e43-168">5,538.06</span></span>            | <span data-ttu-id="67e43-169">20 559,59</span><span class="sxs-lookup"><span data-stu-id="67e43-169">20,559.59</span></span>             |
| <span data-ttu-id="67e43-170">5</span><span class="sxs-lookup"><span data-stu-id="67e43-170">5</span></span>    | <span data-ttu-id="67e43-171">31. prosince</span><span class="sxs-lookup"><span data-stu-id="67e43-171">December 31</span></span> | <span data-ttu-id="67e43-172">4 579,89</span><span class="sxs-lookup"><span data-stu-id="67e43-172">4,579.89</span></span>            | <span data-ttu-id="67e43-173">15 979,70</span><span class="sxs-lookup"><span data-stu-id="67e43-173">15,979.70</span></span>             |
| <span data-ttu-id="67e43-174">6</span><span class="sxs-lookup"><span data-stu-id="67e43-174">6</span></span>    | <span data-ttu-id="67e43-175">31. prosince</span><span class="sxs-lookup"><span data-stu-id="67e43-175">December 31</span></span> | <span data-ttu-id="67e43-176">3 937,36</span><span class="sxs-lookup"><span data-stu-id="67e43-176">3,937.36</span></span>            | <span data-ttu-id="67e43-177">12 042,34</span><span class="sxs-lookup"><span data-stu-id="67e43-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="67e43-178">Lineární metoda odepisování</span><span class="sxs-lookup"><span data-stu-id="67e43-178">Straight line depreciation</span></span>
<span data-ttu-id="67e43-179">Hodnota v poli **Koeficient** je rovna **50**.</span><span class="sxs-lookup"><span data-stu-id="67e43-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="67e43-180">V tomto případě bude odpis stejný v každém období a je třeba zvážit vliv vámi vybraných hodnot na ostatní pole tak, jak je to popsáno v tématu [Lineární odpisování](straight-line-service-life-depreciation.md).</span><span class="sxs-lookup"><span data-stu-id="67e43-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>



