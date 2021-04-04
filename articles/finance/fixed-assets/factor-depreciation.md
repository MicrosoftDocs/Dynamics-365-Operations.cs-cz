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
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87cca8b3472f572cd1c4ba3d894269f7ba0f248a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241067"
---
# <a name="factor-depreciation"></a><span data-ttu-id="bf004-103">Odpis koeficientem</span><span class="sxs-lookup"><span data-stu-id="bf004-103">Factor depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf004-104">Tento článek poskytuje přehled o metodě odpisu koeficientem.</span><span class="sxs-lookup"><span data-stu-id="bf004-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="bf004-105">Koeficienty jsou procenta, která se používají při odpisování majetku.</span><span class="sxs-lookup"><span data-stu-id="bf004-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="bf004-106">Když nastavíte odpisový plán dlouhodobého majetku a v poli **Metoda** na stránce **Odpisové profily** vyberete hodnotu **Koeficient**, můžete nastavit progresivní, degresivní nebo lineární metodu odepisování:</span><span class="sxs-lookup"><span data-stu-id="bf004-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="bf004-107">Jestliže vyberete progresivní metodu odepisování, částka odpisu se v každém období odpisu zvýší.</span><span class="sxs-lookup"><span data-stu-id="bf004-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="bf004-108">Jestliže vyberete degresivní metodu odepisování, částka odpisu za dané období se bude v průběhu let snižovat.</span><span class="sxs-lookup"><span data-stu-id="bf004-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="bf004-109">Jestliže vyberete lineární metodu odepisování, odpis bude v každém období stejný.</span><span class="sxs-lookup"><span data-stu-id="bf004-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="bf004-110">Níže uvedená pravidla a příklady ukazují, jak lze nastavit koeficienty pro jednotlivé typy odpisů.</span><span class="sxs-lookup"><span data-stu-id="bf004-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="bf004-111">Když vyberete možnost **Faktor** v poli **Metoda**, zobrazí se pole **Faktor** a pole **Interval**.</span><span class="sxs-lookup"><span data-stu-id="bf004-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="bf004-112">Progresivní metoda odepisování</span><span class="sxs-lookup"><span data-stu-id="bf004-112">Progressive depreciation</span></span>
<span data-ttu-id="bf004-113">Hodnota v poli **Koeficient** je větší než **50**.</span><span class="sxs-lookup"><span data-stu-id="bf004-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="bf004-114">Příklad</span><span class="sxs-lookup"><span data-stu-id="bf004-114">Example</span></span>

<span data-ttu-id="bf004-115">Pořizovací cena je 100 000, koeficient je 70, doba životnosti je 10 let a odepisování začíná 1. ledna.</span><span class="sxs-lookup"><span data-stu-id="bf004-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="bf004-116">Částky odpisů a zůstatkové účetní hodnoty jsou zobrazeny pouze pro prvních šest let životnosti.</span><span class="sxs-lookup"><span data-stu-id="bf004-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="bf004-117">Rok</span><span class="sxs-lookup"><span data-stu-id="bf004-117">Year</span></span> | <span data-ttu-id="bf004-118">Období</span><span class="sxs-lookup"><span data-stu-id="bf004-118">Period</span></span>      | <span data-ttu-id="bf004-119">Odpisovaná částka</span><span class="sxs-lookup"><span data-stu-id="bf004-119">Depreciation amount</span></span> | <span data-ttu-id="bf004-120">Zůstatková účetní hodnota</span><span class="sxs-lookup"><span data-stu-id="bf004-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="bf004-121">1</span><span class="sxs-lookup"><span data-stu-id="bf004-121">1</span></span>    | <span data-ttu-id="bf004-122">31. prosince</span><span class="sxs-lookup"><span data-stu-id="bf004-122">December 31</span></span> | <span data-ttu-id="bf004-123">307,69</span><span class="sxs-lookup"><span data-stu-id="bf004-123">307.69</span></span>              | <span data-ttu-id="bf004-124">99 692,31</span><span class="sxs-lookup"><span data-stu-id="bf004-124">99,692.31</span></span>             |
| <span data-ttu-id="bf004-125">2</span><span class="sxs-lookup"><span data-stu-id="bf004-125">2</span></span>    | <span data-ttu-id="bf004-126">31. prosince</span><span class="sxs-lookup"><span data-stu-id="bf004-126">December 31</span></span> | <span data-ttu-id="bf004-127">1 447,21</span><span class="sxs-lookup"><span data-stu-id="bf004-127">1,447.21</span></span>            | <span data-ttu-id="bf004-128">98 245,10</span><span class="sxs-lookup"><span data-stu-id="bf004-128">98,245.10</span></span>             |
| <span data-ttu-id="bf004-129">3</span><span class="sxs-lookup"><span data-stu-id="bf004-129">3</span></span>    | <span data-ttu-id="bf004-130">31. prosince</span><span class="sxs-lookup"><span data-stu-id="bf004-130">December 31</span></span> | <span data-ttu-id="bf004-131">3 104,50</span><span class="sxs-lookup"><span data-stu-id="bf004-131">3,104.50</span></span>            | <span data-ttu-id="bf004-132">95 140,60</span><span class="sxs-lookup"><span data-stu-id="bf004-132">95,140.60</span></span>             |
| <span data-ttu-id="bf004-133">4</span><span class="sxs-lookup"><span data-stu-id="bf004-133">4</span></span>    | <span data-ttu-id="bf004-134">31. prosince</span><span class="sxs-lookup"><span data-stu-id="bf004-134">December 31</span></span> | <span data-ttu-id="bf004-135">5 150,21</span><span class="sxs-lookup"><span data-stu-id="bf004-135">5,150.21</span></span>            | <span data-ttu-id="bf004-136">89 990,39</span><span class="sxs-lookup"><span data-stu-id="bf004-136">89,990.39</span></span>             |
| <span data-ttu-id="bf004-137">5</span><span class="sxs-lookup"><span data-stu-id="bf004-137">5</span></span>    | <span data-ttu-id="bf004-138">31. prosince</span><span class="sxs-lookup"><span data-stu-id="bf004-138">December 31</span></span> | <span data-ttu-id="bf004-139">7 522,95</span><span class="sxs-lookup"><span data-stu-id="bf004-139">7,522.95</span></span>            | <span data-ttu-id="bf004-140">82 467,44</span><span class="sxs-lookup"><span data-stu-id="bf004-140">82,467.44</span></span>             |
| <span data-ttu-id="bf004-141">6</span><span class="sxs-lookup"><span data-stu-id="bf004-141">6</span></span>    | <span data-ttu-id="bf004-142">31. prosince</span><span class="sxs-lookup"><span data-stu-id="bf004-142">December 31</span></span> | <span data-ttu-id="bf004-143">10 184,06</span><span class="sxs-lookup"><span data-stu-id="bf004-143">10,184.06</span></span>           | <span data-ttu-id="bf004-144">72 283,38</span><span class="sxs-lookup"><span data-stu-id="bf004-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="bf004-145">Degresivní metoda odepisování</span><span class="sxs-lookup"><span data-stu-id="bf004-145">Digressive depreciation</span></span>
<span data-ttu-id="bf004-146">Hodnota v poli **Koeficient** je menší než **50**.</span><span class="sxs-lookup"><span data-stu-id="bf004-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="bf004-147">Příklad</span><span class="sxs-lookup"><span data-stu-id="bf004-147">Example</span></span>

<span data-ttu-id="bf004-148">Pořizovací cena je 100 000, koeficient je 20, doba životnosti je 10 let a odepisování začíná 1. ledna.</span><span class="sxs-lookup"><span data-stu-id="bf004-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="bf004-149">Částky odpisů a zůstatkové účetní hodnoty jsou zobrazeny pouze pro prvních šest let životnosti.</span><span class="sxs-lookup"><span data-stu-id="bf004-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="bf004-150">Rok</span><span class="sxs-lookup"><span data-stu-id="bf004-150">Year</span></span> | <span data-ttu-id="bf004-151">Období</span><span class="sxs-lookup"><span data-stu-id="bf004-151">Period</span></span>      | <span data-ttu-id="bf004-152">Odpisovaná částka</span><span class="sxs-lookup"><span data-stu-id="bf004-152">Depreciation amount</span></span> | <span data-ttu-id="bf004-153">Zůstatková účetní hodnota</span><span class="sxs-lookup"><span data-stu-id="bf004-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="bf004-154">1</span><span class="sxs-lookup"><span data-stu-id="bf004-154">1</span></span>    | <span data-ttu-id="bf004-155">31. prosince</span><span class="sxs-lookup"><span data-stu-id="bf004-155">December 31</span></span> | <span data-ttu-id="bf004-156">56 080,43</span><span class="sxs-lookup"><span data-stu-id="bf004-156">56,080.43</span></span>           | <span data-ttu-id="bf004-157">43 919,57</span><span class="sxs-lookup"><span data-stu-id="bf004-157">43,919.57</span></span>             |
| <span data-ttu-id="bf004-158">2</span><span class="sxs-lookup"><span data-stu-id="bf004-158">2</span></span>    | <span data-ttu-id="bf004-159">31. prosince</span><span class="sxs-lookup"><span data-stu-id="bf004-159">December 31</span></span> | <span data-ttu-id="bf004-160">10 665,70</span><span class="sxs-lookup"><span data-stu-id="bf004-160">10,665.70</span></span>           | <span data-ttu-id="bf004-161">33 253,87</span><span class="sxs-lookup"><span data-stu-id="bf004-161">33,253.87</span></span>             |
| <span data-ttu-id="bf004-162">3</span><span class="sxs-lookup"><span data-stu-id="bf004-162">3</span></span>    | <span data-ttu-id="bf004-163">31. prosince</span><span class="sxs-lookup"><span data-stu-id="bf004-163">December 31</span></span> | <span data-ttu-id="bf004-164">7 156,22</span><span class="sxs-lookup"><span data-stu-id="bf004-164">7,156.22</span></span>            | <span data-ttu-id="bf004-165">26 097,65</span><span class="sxs-lookup"><span data-stu-id="bf004-165">26,097.65</span></span>             |
| <span data-ttu-id="bf004-166">4</span><span class="sxs-lookup"><span data-stu-id="bf004-166">4</span></span>    | <span data-ttu-id="bf004-167">31. prosince</span><span class="sxs-lookup"><span data-stu-id="bf004-167">December 31</span></span> | <span data-ttu-id="bf004-168">5 538,06</span><span class="sxs-lookup"><span data-stu-id="bf004-168">5,538.06</span></span>            | <span data-ttu-id="bf004-169">20 559,59</span><span class="sxs-lookup"><span data-stu-id="bf004-169">20,559.59</span></span>             |
| <span data-ttu-id="bf004-170">5</span><span class="sxs-lookup"><span data-stu-id="bf004-170">5</span></span>    | <span data-ttu-id="bf004-171">31. prosince</span><span class="sxs-lookup"><span data-stu-id="bf004-171">December 31</span></span> | <span data-ttu-id="bf004-172">4 579,89</span><span class="sxs-lookup"><span data-stu-id="bf004-172">4,579.89</span></span>            | <span data-ttu-id="bf004-173">15 979,70</span><span class="sxs-lookup"><span data-stu-id="bf004-173">15,979.70</span></span>             |
| <span data-ttu-id="bf004-174">6</span><span class="sxs-lookup"><span data-stu-id="bf004-174">6</span></span>    | <span data-ttu-id="bf004-175">31. prosince</span><span class="sxs-lookup"><span data-stu-id="bf004-175">December 31</span></span> | <span data-ttu-id="bf004-176">3 937,36</span><span class="sxs-lookup"><span data-stu-id="bf004-176">3,937.36</span></span>            | <span data-ttu-id="bf004-177">12 042,34</span><span class="sxs-lookup"><span data-stu-id="bf004-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="bf004-178">Lineární metoda odepisování</span><span class="sxs-lookup"><span data-stu-id="bf004-178">Straight line depreciation</span></span>
<span data-ttu-id="bf004-179">Hodnota v poli **Koeficient** je rovna **50**.</span><span class="sxs-lookup"><span data-stu-id="bf004-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="bf004-180">V tomto případě bude odpis stejný v každém období a je třeba zvážit vliv vámi vybraných hodnot na ostatní pole tak, jak je to popsáno v tématu [Lineární odpisování](straight-line-service-life-depreciation.md).</span><span class="sxs-lookup"><span data-stu-id="bf004-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]