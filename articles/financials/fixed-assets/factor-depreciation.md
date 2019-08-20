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
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840522"
---
# <a name="factor-depreciation"></a><span data-ttu-id="f7991-103">Odpis koeficientem</span><span class="sxs-lookup"><span data-stu-id="f7991-103">Factor depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7991-104">Tento článek poskytuje přehled o metodě odpisu koeficientem.</span><span class="sxs-lookup"><span data-stu-id="f7991-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="f7991-105">Koeficienty jsou procenta, která se používají při odpisování majetku.</span><span class="sxs-lookup"><span data-stu-id="f7991-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="f7991-106">Když nastavíte odpisový plán dlouhodobého majetku a v poli **Metoda** na stránce **Odpisové profily** vyberete hodnotu **Koeficient**, můžete nastavit progresivní, degresivní nebo lineární metodu odepisování:</span><span class="sxs-lookup"><span data-stu-id="f7991-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="f7991-107">Jestliže vyberete progresivní metodu odepisování, částka odpisu se v každém období odpisu zvýší.</span><span class="sxs-lookup"><span data-stu-id="f7991-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="f7991-108">Jestliže vyberete degresivní metodu odepisování, částka odpisu za dané období se bude v průběhu let snižovat.</span><span class="sxs-lookup"><span data-stu-id="f7991-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="f7991-109">Jestliže vyberete lineární metodu odepisování, odpis bude v každém období stejný.</span><span class="sxs-lookup"><span data-stu-id="f7991-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="f7991-110">Níže uvedená pravidla a příklady ukazují, jak lze nastavit koeficienty pro jednotlivé typy odpisů.</span><span class="sxs-lookup"><span data-stu-id="f7991-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="f7991-111">Když vyberete možnost **Faktor** v poli **Metoda**, zobrazí se pole **Faktor** a pole **Interval**.</span><span class="sxs-lookup"><span data-stu-id="f7991-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="f7991-112">Progresivní metoda odepisování</span><span class="sxs-lookup"><span data-stu-id="f7991-112">Progressive depreciation</span></span>
<span data-ttu-id="f7991-113">Hodnota v poli **Koeficient** je větší než **50**.</span><span class="sxs-lookup"><span data-stu-id="f7991-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="f7991-114">Příklad</span><span class="sxs-lookup"><span data-stu-id="f7991-114">Example</span></span>

<span data-ttu-id="f7991-115">Pořizovací cena je 100 000, koeficient je 70, doba životnosti je 10 let a odepisování začíná 1. ledna.</span><span class="sxs-lookup"><span data-stu-id="f7991-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="f7991-116">Částky odpisů a zůstatkové účetní hodnoty jsou zobrazeny pouze pro prvních šest let životnosti.</span><span class="sxs-lookup"><span data-stu-id="f7991-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="f7991-117">Rok</span><span class="sxs-lookup"><span data-stu-id="f7991-117">Year</span></span> | <span data-ttu-id="f7991-118">Období</span><span class="sxs-lookup"><span data-stu-id="f7991-118">Period</span></span>      | <span data-ttu-id="f7991-119">Odpisovaná částka</span><span class="sxs-lookup"><span data-stu-id="f7991-119">Depreciation amount</span></span> | <span data-ttu-id="f7991-120">Zůstatková účetní hodnota</span><span class="sxs-lookup"><span data-stu-id="f7991-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="f7991-121">1</span><span class="sxs-lookup"><span data-stu-id="f7991-121">1</span></span>    | <span data-ttu-id="f7991-122">31. prosince</span><span class="sxs-lookup"><span data-stu-id="f7991-122">December 31</span></span> | <span data-ttu-id="f7991-123">307,69</span><span class="sxs-lookup"><span data-stu-id="f7991-123">307.69</span></span>              | <span data-ttu-id="f7991-124">99 692,31</span><span class="sxs-lookup"><span data-stu-id="f7991-124">99,692.31</span></span>             |
| <span data-ttu-id="f7991-125">2</span><span class="sxs-lookup"><span data-stu-id="f7991-125">2</span></span>    | <span data-ttu-id="f7991-126">31. prosince</span><span class="sxs-lookup"><span data-stu-id="f7991-126">December 31</span></span> | <span data-ttu-id="f7991-127">1 447,21</span><span class="sxs-lookup"><span data-stu-id="f7991-127">1,447.21</span></span>            | <span data-ttu-id="f7991-128">98 245,10</span><span class="sxs-lookup"><span data-stu-id="f7991-128">98,245.10</span></span>             |
| <span data-ttu-id="f7991-129">3</span><span class="sxs-lookup"><span data-stu-id="f7991-129">3</span></span>    | <span data-ttu-id="f7991-130">31. prosince</span><span class="sxs-lookup"><span data-stu-id="f7991-130">December 31</span></span> | <span data-ttu-id="f7991-131">3 104,50</span><span class="sxs-lookup"><span data-stu-id="f7991-131">3,104.50</span></span>            | <span data-ttu-id="f7991-132">95 140,60</span><span class="sxs-lookup"><span data-stu-id="f7991-132">95,140.60</span></span>             |
| <span data-ttu-id="f7991-133">4</span><span class="sxs-lookup"><span data-stu-id="f7991-133">4</span></span>    | <span data-ttu-id="f7991-134">31. prosince</span><span class="sxs-lookup"><span data-stu-id="f7991-134">December 31</span></span> | <span data-ttu-id="f7991-135">5 150,21</span><span class="sxs-lookup"><span data-stu-id="f7991-135">5,150.21</span></span>            | <span data-ttu-id="f7991-136">89 990,39</span><span class="sxs-lookup"><span data-stu-id="f7991-136">89,990.39</span></span>             |
| <span data-ttu-id="f7991-137">5</span><span class="sxs-lookup"><span data-stu-id="f7991-137">5</span></span>    | <span data-ttu-id="f7991-138">31. prosince</span><span class="sxs-lookup"><span data-stu-id="f7991-138">December 31</span></span> | <span data-ttu-id="f7991-139">7 522,95</span><span class="sxs-lookup"><span data-stu-id="f7991-139">7,522.95</span></span>            | <span data-ttu-id="f7991-140">82 467,44</span><span class="sxs-lookup"><span data-stu-id="f7991-140">82,467.44</span></span>             |
| <span data-ttu-id="f7991-141">6</span><span class="sxs-lookup"><span data-stu-id="f7991-141">6</span></span>    | <span data-ttu-id="f7991-142">31. prosince</span><span class="sxs-lookup"><span data-stu-id="f7991-142">December 31</span></span> | <span data-ttu-id="f7991-143">10 184,06</span><span class="sxs-lookup"><span data-stu-id="f7991-143">10,184.06</span></span>           | <span data-ttu-id="f7991-144">72 283,38</span><span class="sxs-lookup"><span data-stu-id="f7991-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="f7991-145">Degresivní metoda odepisování</span><span class="sxs-lookup"><span data-stu-id="f7991-145">Digressive depreciation</span></span>
<span data-ttu-id="f7991-146">Hodnota v poli **Koeficient** je menší než **50**.</span><span class="sxs-lookup"><span data-stu-id="f7991-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="f7991-147">Příklad</span><span class="sxs-lookup"><span data-stu-id="f7991-147">Example</span></span>

<span data-ttu-id="f7991-148">Pořizovací cena je 100 000, koeficient je 20, doba životnosti je 10 let a odepisování začíná 1. ledna.</span><span class="sxs-lookup"><span data-stu-id="f7991-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="f7991-149">Částky odpisů a zůstatkové účetní hodnoty jsou zobrazeny pouze pro prvních šest let životnosti.</span><span class="sxs-lookup"><span data-stu-id="f7991-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="f7991-150">Rok</span><span class="sxs-lookup"><span data-stu-id="f7991-150">Year</span></span> | <span data-ttu-id="f7991-151">Období</span><span class="sxs-lookup"><span data-stu-id="f7991-151">Period</span></span>      | <span data-ttu-id="f7991-152">Odpisovaná částka</span><span class="sxs-lookup"><span data-stu-id="f7991-152">Depreciation amount</span></span> | <span data-ttu-id="f7991-153">Zůstatková účetní hodnota</span><span class="sxs-lookup"><span data-stu-id="f7991-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="f7991-154">1</span><span class="sxs-lookup"><span data-stu-id="f7991-154">1</span></span>    | <span data-ttu-id="f7991-155">31. prosince</span><span class="sxs-lookup"><span data-stu-id="f7991-155">December 31</span></span> | <span data-ttu-id="f7991-156">56 080,43</span><span class="sxs-lookup"><span data-stu-id="f7991-156">56,080.43</span></span>           | <span data-ttu-id="f7991-157">43 919,57</span><span class="sxs-lookup"><span data-stu-id="f7991-157">43,919.57</span></span>             |
| <span data-ttu-id="f7991-158">2</span><span class="sxs-lookup"><span data-stu-id="f7991-158">2</span></span>    | <span data-ttu-id="f7991-159">31. prosince</span><span class="sxs-lookup"><span data-stu-id="f7991-159">December 31</span></span> | <span data-ttu-id="f7991-160">10 665,70</span><span class="sxs-lookup"><span data-stu-id="f7991-160">10,665.70</span></span>           | <span data-ttu-id="f7991-161">33 253,87</span><span class="sxs-lookup"><span data-stu-id="f7991-161">33,253.87</span></span>             |
| <span data-ttu-id="f7991-162">3</span><span class="sxs-lookup"><span data-stu-id="f7991-162">3</span></span>    | <span data-ttu-id="f7991-163">31. prosince</span><span class="sxs-lookup"><span data-stu-id="f7991-163">December 31</span></span> | <span data-ttu-id="f7991-164">7 156,22</span><span class="sxs-lookup"><span data-stu-id="f7991-164">7,156.22</span></span>            | <span data-ttu-id="f7991-165">26 097,65</span><span class="sxs-lookup"><span data-stu-id="f7991-165">26,097.65</span></span>             |
| <span data-ttu-id="f7991-166">4</span><span class="sxs-lookup"><span data-stu-id="f7991-166">4</span></span>    | <span data-ttu-id="f7991-167">31. prosince</span><span class="sxs-lookup"><span data-stu-id="f7991-167">December 31</span></span> | <span data-ttu-id="f7991-168">5 538,06</span><span class="sxs-lookup"><span data-stu-id="f7991-168">5,538.06</span></span>            | <span data-ttu-id="f7991-169">20 559,59</span><span class="sxs-lookup"><span data-stu-id="f7991-169">20,559.59</span></span>             |
| <span data-ttu-id="f7991-170">5</span><span class="sxs-lookup"><span data-stu-id="f7991-170">5</span></span>    | <span data-ttu-id="f7991-171">31. prosince</span><span class="sxs-lookup"><span data-stu-id="f7991-171">December 31</span></span> | <span data-ttu-id="f7991-172">4 579,89</span><span class="sxs-lookup"><span data-stu-id="f7991-172">4,579.89</span></span>            | <span data-ttu-id="f7991-173">15 979,70</span><span class="sxs-lookup"><span data-stu-id="f7991-173">15,979.70</span></span>             |
| <span data-ttu-id="f7991-174">6</span><span class="sxs-lookup"><span data-stu-id="f7991-174">6</span></span>    | <span data-ttu-id="f7991-175">31. prosince</span><span class="sxs-lookup"><span data-stu-id="f7991-175">December 31</span></span> | <span data-ttu-id="f7991-176">3 937,36</span><span class="sxs-lookup"><span data-stu-id="f7991-176">3,937.36</span></span>            | <span data-ttu-id="f7991-177">12 042,34</span><span class="sxs-lookup"><span data-stu-id="f7991-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="f7991-178">Lineární metoda odepisování</span><span class="sxs-lookup"><span data-stu-id="f7991-178">Straight line depreciation</span></span>
<span data-ttu-id="f7991-179">Hodnota v poli **Koeficient** je rovna **50**.</span><span class="sxs-lookup"><span data-stu-id="f7991-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="f7991-180">V tomto případě bude odpis stejný v každém období a je třeba zvážit vliv vámi vybraných hodnot na ostatní pole tak, jak je to popsáno v tématu [Lineární odpisování](straight-line-service-life-depreciation.md).</span><span class="sxs-lookup"><span data-stu-id="f7991-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>



