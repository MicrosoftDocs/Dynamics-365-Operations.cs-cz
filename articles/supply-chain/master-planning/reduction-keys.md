---
title: Redukční klíče
description: Tento článek obsahuje příklady nastavení redukčního klíče. Obsahuje informace týkající se různého nastavení redukčního klíče a výsledky každého z nich. Redukční klíč slouží k definování způsobu snížení požadavků prognózy.
author: roxanadiaconu
manager: AnnBe
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7457aca4ca4d5188bafb497d3052276cfc154ad1
ms.sourcegitcommit: 704d273485dcdc25c97a222bc0ef0695aad334d2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/28/2019
ms.locfileid: "770909"
---
# <a name="reduction-keys"></a><span data-ttu-id="d60f9-105">Redukční klíče</span><span class="sxs-lookup"><span data-stu-id="d60f9-105">Reduction keys</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d60f9-106">Tento článek obsahuje příklady nastavení redukčního klíče.</span><span class="sxs-lookup"><span data-stu-id="d60f9-106">This articles provides examples that show how to set up a reduction key.</span></span> <span data-ttu-id="d60f9-107">Obsahuje informace týkající se různého nastavení redukčního klíče a výsledky každého z nich.</span><span class="sxs-lookup"><span data-stu-id="d60f9-107">It includes information about the various reduction key settings and the results of each.</span></span> <span data-ttu-id="d60f9-108">Redukční klíč slouží k definování způsobu snížení požadavků prognózy.</span><span class="sxs-lookup"><span data-stu-id="d60f9-108">You can use a reduction key to define how to reduce forecast requirements.</span></span>

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a><span data-ttu-id="d60f9-109">Příklad 1: Procento – princip redukce prognózy redukčního klíče</span><span class="sxs-lookup"><span data-stu-id="d60f9-109">Example 1: Percent - reduction key forecast reduction principle</span></span>
---------------------------------------------------------------

<span data-ttu-id="d60f9-110">Tento příklad ukazuje, jak redukční klíč snižuje požadavky na prognózu podle procent a období, které jsou definovány podle redukčního klíče.</span><span class="sxs-lookup"><span data-stu-id="d60f9-110">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

1. <span data-ttu-id="d60f9-111">Na stránce **Redukční klíče** nastavte následující řádky.</span><span class="sxs-lookup"><span data-stu-id="d60f9-111">On the **Reduction keys** page, set up the following lines.</span></span>

   | <span data-ttu-id="d60f9-112">Vrácená hotovost</span><span class="sxs-lookup"><span data-stu-id="d60f9-112">Change</span></span> | <span data-ttu-id="d60f9-113">Jednotka</span><span class="sxs-lookup"><span data-stu-id="d60f9-113">Unit</span></span>  | <span data-ttu-id="d60f9-114">Procento</span><span class="sxs-lookup"><span data-stu-id="d60f9-114">Percent</span></span> |
   |--------|-------|---------|
   |   <span data-ttu-id="d60f9-115">1</span><span class="sxs-lookup"><span data-stu-id="d60f9-115">1</span></span>    | <span data-ttu-id="d60f9-116">Měsíc</span><span class="sxs-lookup"><span data-stu-id="d60f9-116">Month</span></span> |   <span data-ttu-id="d60f9-117">100</span><span class="sxs-lookup"><span data-stu-id="d60f9-117">100</span></span>   |
   |   <span data-ttu-id="d60f9-118">2</span><span class="sxs-lookup"><span data-stu-id="d60f9-118">2</span></span>    | <span data-ttu-id="d60f9-119">Měsíc</span><span class="sxs-lookup"><span data-stu-id="d60f9-119">Month</span></span> |   <span data-ttu-id="d60f9-120">75</span><span class="sxs-lookup"><span data-stu-id="d60f9-120">75</span></span>    |
   |   <span data-ttu-id="d60f9-121">3</span><span class="sxs-lookup"><span data-stu-id="d60f9-121">3</span></span>    | <span data-ttu-id="d60f9-122">Měsíc</span><span class="sxs-lookup"><span data-stu-id="d60f9-122">Month</span></span> |   <span data-ttu-id="d60f9-123">50</span><span class="sxs-lookup"><span data-stu-id="d60f9-123">50</span></span>    |
   |   <span data-ttu-id="d60f9-124">4</span><span class="sxs-lookup"><span data-stu-id="d60f9-124">4</span></span>    | <span data-ttu-id="d60f9-125">Měsíc</span><span class="sxs-lookup"><span data-stu-id="d60f9-125">Month</span></span> |   <span data-ttu-id="d60f9-126">25</span><span class="sxs-lookup"><span data-stu-id="d60f9-126">25</span></span>    |


2. <span data-ttu-id="d60f9-127">Propojte redukční klíč se skupinou disponibility položky.</span><span class="sxs-lookup"><span data-stu-id="d60f9-127">Link the reduction key to the item's coverage group.</span></span>
3. <span data-ttu-id="d60f9-128">Na stránce **Hlavní plány**v poli **Metoda redukce** vyberte **Procento – redukční klíč**.</span><span class="sxs-lookup"><span data-stu-id="d60f9-128">On the **Master plans** page, in the **Reduction principle** field, select **Percent - reduction key**.</span></span>
4. <span data-ttu-id="d60f9-129">Vytvořte prognózu poptávky pro 1000 kusů za měsíc.</span><span class="sxs-lookup"><span data-stu-id="d60f9-129">Create a demand forecast of 1,000 pieces per month.</span></span>

<span data-ttu-id="d60f9-130">Pokud spustíte plánování prognózy 1. ledna, požadavky prognózy poptávky se spotřebují podle procentuálních hodnot, které se nastavují na stránce **Redukční klíče**.</span><span class="sxs-lookup"><span data-stu-id="d60f9-130">If you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="d60f9-131">Do hlavního plánu se přenesou následující požadované objemy.</span><span class="sxs-lookup"><span data-stu-id="d60f9-131">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="d60f9-132">Měsíc</span><span class="sxs-lookup"><span data-stu-id="d60f9-132">Month</span></span>                | <span data-ttu-id="d60f9-133">Počet požadovaných kusů</span><span class="sxs-lookup"><span data-stu-id="d60f9-133">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="d60f9-134">Leden</span><span class="sxs-lookup"><span data-stu-id="d60f9-134">January</span></span>              | <span data-ttu-id="d60f9-135">0</span><span class="sxs-lookup"><span data-stu-id="d60f9-135">0</span></span>                         |
| <span data-ttu-id="d60f9-136">Únor</span><span class="sxs-lookup"><span data-stu-id="d60f9-136">February</span></span>             | <span data-ttu-id="d60f9-137">250</span><span class="sxs-lookup"><span data-stu-id="d60f9-137">250</span></span>                       |
| <span data-ttu-id="d60f9-138">Březen</span><span class="sxs-lookup"><span data-stu-id="d60f9-138">March</span></span>                | <span data-ttu-id="d60f9-139">500</span><span class="sxs-lookup"><span data-stu-id="d60f9-139">500</span></span>                       |
| <span data-ttu-id="d60f9-140">Duben</span><span class="sxs-lookup"><span data-stu-id="d60f9-140">April</span></span>                | <span data-ttu-id="d60f9-141">750</span><span class="sxs-lookup"><span data-stu-id="d60f9-141">750</span></span>                       |
| <span data-ttu-id="d60f9-142">Květen až prosinec</span><span class="sxs-lookup"><span data-stu-id="d60f9-142">May through December</span></span> | <span data-ttu-id="d60f9-143">1 000</span><span class="sxs-lookup"><span data-stu-id="d60f9-143">1,000</span></span>                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a><span data-ttu-id="d60f9-144">Příklad 2: Transakce – princip redukce prognózy redukčního klíče</span><span class="sxs-lookup"><span data-stu-id="d60f9-144">Example 2: Transactions  reduction key forecast reduction principle</span></span>
<span data-ttu-id="d60f9-145">Tento příklad ukazuje, jak jsou skutečné objednávky prováděné v období definovány podle redukčního klíče pro snížení požadavků prognózy poptávky.</span><span class="sxs-lookup"><span data-stu-id="d60f9-145">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

-   <span data-ttu-id="d60f9-146">Na stránce **Hlavní plány**v poli **Metoda redukce** vyberte **Transakce – redukční klíč**.</span><span class="sxs-lookup"><span data-stu-id="d60f9-146">On the **Master plans** page, in the **Reduction principle** field, select **Transactions - reduction key**.</span></span>

<span data-ttu-id="d60f9-147">Následující prodejní objednávky existují k 1. lednu.</span><span class="sxs-lookup"><span data-stu-id="d60f9-147">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="d60f9-148">Měsíc</span><span class="sxs-lookup"><span data-stu-id="d60f9-148">Month</span></span>    | <span data-ttu-id="d60f9-149">Počet objednaných kusů</span><span class="sxs-lookup"><span data-stu-id="d60f9-149">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="d60f9-150">Leden</span><span class="sxs-lookup"><span data-stu-id="d60f9-150">January</span></span>  | <span data-ttu-id="d60f9-151">956</span><span class="sxs-lookup"><span data-stu-id="d60f9-151">956</span></span>                      |
| <span data-ttu-id="d60f9-152">Únor</span><span class="sxs-lookup"><span data-stu-id="d60f9-152">February</span></span> | <span data-ttu-id="d60f9-153">1 176</span><span class="sxs-lookup"><span data-stu-id="d60f9-153">1,176</span></span>                    |
| <span data-ttu-id="d60f9-154">Březen</span><span class="sxs-lookup"><span data-stu-id="d60f9-154">March</span></span>    | <span data-ttu-id="d60f9-155">451</span><span class="sxs-lookup"><span data-stu-id="d60f9-155">451</span></span>                      |
| <span data-ttu-id="d60f9-156">Duben</span><span class="sxs-lookup"><span data-stu-id="d60f9-156">April</span></span>    | <span data-ttu-id="d60f9-157">119</span><span class="sxs-lookup"><span data-stu-id="d60f9-157">119</span></span>                      |

<span data-ttu-id="d60f9-158">Pokud použijete stejnou prognózu poptávky pro 1000 kusů za měsíc, následující požadované objemy se přenesou do hlavního plánu.</span><span class="sxs-lookup"><span data-stu-id="d60f9-158">If you use the same demand forecast of 1,000 pieces per month, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="d60f9-159">Měsíc</span><span class="sxs-lookup"><span data-stu-id="d60f9-159">Month</span></span>                | <span data-ttu-id="d60f9-160">Počet požadovaných kusů</span><span class="sxs-lookup"><span data-stu-id="d60f9-160">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="d60f9-161">Leden</span><span class="sxs-lookup"><span data-stu-id="d60f9-161">January</span></span>              | <span data-ttu-id="d60f9-162">44</span><span class="sxs-lookup"><span data-stu-id="d60f9-162">44</span></span>                        |
| <span data-ttu-id="d60f9-163">Únor</span><span class="sxs-lookup"><span data-stu-id="d60f9-163">February</span></span>             | <span data-ttu-id="d60f9-164">0</span><span class="sxs-lookup"><span data-stu-id="d60f9-164">0</span></span>                         |
| <span data-ttu-id="d60f9-165">Březen</span><span class="sxs-lookup"><span data-stu-id="d60f9-165">March</span></span>                | <span data-ttu-id="d60f9-166">549</span><span class="sxs-lookup"><span data-stu-id="d60f9-166">549</span></span>                       |
| <span data-ttu-id="d60f9-167">Duben</span><span class="sxs-lookup"><span data-stu-id="d60f9-167">April</span></span>                | <span data-ttu-id="d60f9-168">881</span><span class="sxs-lookup"><span data-stu-id="d60f9-168">881</span></span>                       |
| <span data-ttu-id="d60f9-169">Květen až prosinec</span><span class="sxs-lookup"><span data-stu-id="d60f9-169">May through December</span></span> | <span data-ttu-id="d60f9-170">1 000</span><span class="sxs-lookup"><span data-stu-id="d60f9-170">1,000</span></span>                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a><span data-ttu-id="d60f9-171">Příklad 3: Transakce – princip redukce prognózy dynamického období</span><span class="sxs-lookup"><span data-stu-id="d60f9-171">Example 3: Transactions  dynamic period forecast reduction principle</span></span>
<span data-ttu-id="d60f9-172">Ve většině případů jsou systémy nastaveny tak, aby transakce snižovaly prognózu poptávky v rámci konkrétních obdobích prognózy: týdny, měsíce a tak dále.</span><span class="sxs-lookup"><span data-stu-id="d60f9-172">In most cases, systems are set up so that transactions reduce demand forecast within specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="d60f9-173">Tato období jsou definována v redukčním klíči.</span><span class="sxs-lookup"><span data-stu-id="d60f9-173">These periods are defined in the reduction key.</span></span> <span data-ttu-id="d60f9-174">Čas mezi dvěma řádky však prognózy poptávky může také *vyjadřovat* období.</span><span class="sxs-lookup"><span data-stu-id="d60f9-174">However, the time between two demand forecast lines can also *imply* a period.</span></span>

1. <span data-ttu-id="d60f9-175">Vytvořte prognózu poptávky pro následující data a množství.</span><span class="sxs-lookup"><span data-stu-id="d60f9-175">Create a demand forecast for the following dates and quantities.</span></span>

   | <span data-ttu-id="d60f9-176">Datum</span><span class="sxs-lookup"><span data-stu-id="d60f9-176">Date</span></span>       | <span data-ttu-id="d60f9-177">Prognóza poptávky</span><span class="sxs-lookup"><span data-stu-id="d60f9-177">Demand forecast</span></span> |
   |------------|-----------------|
   | <span data-ttu-id="d60f9-178">1. leden</span><span class="sxs-lookup"><span data-stu-id="d60f9-178">January 1</span></span>  | <span data-ttu-id="d60f9-179">1 000</span><span class="sxs-lookup"><span data-stu-id="d60f9-179">1,000</span></span>           |
   | <span data-ttu-id="d60f9-180">5. leden</span><span class="sxs-lookup"><span data-stu-id="d60f9-180">January 5</span></span>  | <span data-ttu-id="d60f9-181">500</span><span class="sxs-lookup"><span data-stu-id="d60f9-181">500</span></span>             |
   | <span data-ttu-id="d60f9-182">12. leden</span><span class="sxs-lookup"><span data-stu-id="d60f9-182">January 12</span></span> | <span data-ttu-id="d60f9-183">1 000</span><span class="sxs-lookup"><span data-stu-id="d60f9-183">1,000</span></span>           |

   <span data-ttu-id="d60f9-184">V této prognóze není jasné období mezi daty prognózy: mezi 1. a 2. daty existuje 4denní rozpětí a mezi 2. a 3. daty je 7denní rozpětí.</span><span class="sxs-lookup"><span data-stu-id="d60f9-184">In this forecast, there isn't a clear period between the forecast dates: between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="d60f9-185">Tato různá rozpětí jsou dynamická období.</span><span class="sxs-lookup"><span data-stu-id="d60f9-185">These various spans are the dynamic periods.</span></span>
2. <span data-ttu-id="d60f9-186">Vytvořte řádky prodejní objednávky následovně.</span><span class="sxs-lookup"><span data-stu-id="d60f9-186">Create sales order lines as follows.</span></span>

   | <span data-ttu-id="d60f9-187">Datum</span><span class="sxs-lookup"><span data-stu-id="d60f9-187">Date</span></span>                             | <span data-ttu-id="d60f9-188">Množství prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="d60f9-188">Sales order quantity</span></span> |
   |----------------------------------|----------------------|
   | <span data-ttu-id="d60f9-189">15. prosince v minulém roce</span><span class="sxs-lookup"><span data-stu-id="d60f9-189">December 15 in the previous year</span></span> | <span data-ttu-id="d60f9-190">500</span><span class="sxs-lookup"><span data-stu-id="d60f9-190">500</span></span>                  |
   | <span data-ttu-id="d60f9-191">3. leden</span><span class="sxs-lookup"><span data-stu-id="d60f9-191">January 3</span></span>                        | <span data-ttu-id="d60f9-192">100</span><span class="sxs-lookup"><span data-stu-id="d60f9-192">100</span></span>                  |
   | <span data-ttu-id="d60f9-193">10. leden</span><span class="sxs-lookup"><span data-stu-id="d60f9-193">January 10</span></span>                       | <span data-ttu-id="d60f9-194">200</span><span class="sxs-lookup"><span data-stu-id="d60f9-194">200</span></span>                  |

<span data-ttu-id="d60f9-195">Prognóza bude snížena následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="d60f9-195">The forecast will be reduced as follows:</span></span>

-   <span data-ttu-id="d60f9-196">První prodejní objednávka není v rámci žádného období, takže nesníží žádnou prognózu.</span><span class="sxs-lookup"><span data-stu-id="d60f9-196">The first sales order isn't within any period, so it won't reduce any forecast.</span></span>
-   <span data-ttu-id="d60f9-197">Druhá prodejní objednávka je mezi 1. lednem a 5. lednem, takže sníží prognózu pro 1. leden o hodnotu 100.</span><span class="sxs-lookup"><span data-stu-id="d60f9-197">The second sales order is between January 1 and January 5, so it will reduce the forecast for January 1 by 100.</span></span>
-   <span data-ttu-id="d60f9-198">Třetí prodejní objednávka je mezi 5. lednem a 12. lednem, takže sníží prognózu pro 5. leden o hodnotu 200.</span><span class="sxs-lookup"><span data-stu-id="d60f9-198">The third sales order is between January 5 and January 12, so it will reduce the forecast for January 5 by 200.</span></span>

<span data-ttu-id="d60f9-199">Následující plánovaná objednávka bude vytvořena ke splnění prognózy.</span><span class="sxs-lookup"><span data-stu-id="d60f9-199">The following planned order will be created to fulfill the forecast.</span></span>

| <span data-ttu-id="d60f9-200">Datum prognózy poptávky</span><span class="sxs-lookup"><span data-stu-id="d60f9-200">Demand forecast date</span></span> | <span data-ttu-id="d60f9-201">Snížené množství</span><span class="sxs-lookup"><span data-stu-id="d60f9-201">Reduced quantity</span></span> |
|----------------------|------------------|
| <span data-ttu-id="d60f9-202">1. leden</span><span class="sxs-lookup"><span data-stu-id="d60f9-202">January 1</span></span>            | <span data-ttu-id="d60f9-203">900</span><span class="sxs-lookup"><span data-stu-id="d60f9-203">900</span></span>              |
| <span data-ttu-id="d60f9-204">5. leden</span><span class="sxs-lookup"><span data-stu-id="d60f9-204">January 5</span></span>            | <span data-ttu-id="d60f9-205">300</span><span class="sxs-lookup"><span data-stu-id="d60f9-205">300</span></span>              |
| <span data-ttu-id="d60f9-206">12. leden</span><span class="sxs-lookup"><span data-stu-id="d60f9-206">January 12</span></span>           | <span data-ttu-id="d60f9-207">1 000</span><span class="sxs-lookup"><span data-stu-id="d60f9-207">1,000</span></span>            |

<span data-ttu-id="d60f9-208">Zde je souhrn snížení **Transakce – dynamické období**:</span><span class="sxs-lookup"><span data-stu-id="d60f9-208">Here is a summary of **Transactions - dynamic period** reduction:</span></span>

-   <span data-ttu-id="d60f9-209">Požadavky prognózy jsou sníženy podle skutečných transakcích objednávky, ke kterým došlo během dynamické doby.</span><span class="sxs-lookup"><span data-stu-id="d60f9-209">Forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="d60f9-210">Dynamické období pokrývá aktuální data prognózy a končí na začátku další prognózy.</span><span class="sxs-lookup"><span data-stu-id="d60f9-210">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span>
-   <span data-ttu-id="d60f9-211">Tato metoda nepoužívá ani nevyžaduje redukční klíč.</span><span class="sxs-lookup"><span data-stu-id="d60f9-211">This method doesn't use or require a reduction key.</span></span>
-   <span data-ttu-id="d60f9-212">Použití této možnosti způsobí následující jevy:</span><span class="sxs-lookup"><span data-stu-id="d60f9-212">When this option is used, the following behavior occurs:</span></span>
    -   <span data-ttu-id="d60f9-213">Pokud je prognóza snížena úplně, požadavky prognózy pro aktuální prognózu budou 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="d60f9-213">If the forecast is reduced completely, the forecast requirements for the current forecast become 0 (zero).</span></span>
    -   <span data-ttu-id="d60f9-214">Pokud neexistuje žádná budoucí prognóza, požadavky prognózy z poslední zadané prognózy budou sníženy.</span><span class="sxs-lookup"><span data-stu-id="d60f9-214">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
    -   <span data-ttu-id="d60f9-215">Ochranná doba je zahrnuta do výpočtu snížení prognózy.</span><span class="sxs-lookup"><span data-stu-id="d60f9-215">Time fences are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="d60f9-216">Kladné dny jsou zahrnuty do výpočtu snížení prognózy.</span><span class="sxs-lookup"><span data-stu-id="d60f9-216">Positive days are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="d60f9-217">Překračuje-li skutečná transakce objednávky požadavky prognózy, zbývající transakce nejsou předávány do dalšího období prognózy.</span><span class="sxs-lookup"><span data-stu-id="d60f9-217">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>


<a name="additional-resources"></a><span data-ttu-id="d60f9-218">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="d60f9-218">Additional resources</span></span>
--------

[<span data-ttu-id="d60f9-219">Hlavní plány</span><span class="sxs-lookup"><span data-stu-id="d60f9-219">Master plans</span></span>](master-plans.md)



