---
title: Příklady a logika sestavy stárnutí zásob
description: Toto téma uvádí několik příkladů, které ukazují, jak interpretovat výsledky sestavy stárnutí zásob.
author: RichardLuan
manager: tfehr
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1d9c70a7931c009cd53fbd28a3f4c768d04964a4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214411"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="ceece-103">Příklady a logika sestavy stárnutí zásob</span><span class="sxs-lookup"><span data-stu-id="ceece-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ceece-104">Toto téma uvádí několik příkladů, které ukazují, jak interpretovat výsledky sestavy **stárnutí zásob**.</span><span class="sxs-lookup"><span data-stu-id="ceece-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="ceece-105">Tato sestava kategorizuje hodnoty množství na skladě a zásob pro vybranou položku nebo skupinu položek do několika intervalů období.</span><span class="sxs-lookup"><span data-stu-id="ceece-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="ceece-106">Toto téma také ukazuje vnitřní logiku sestavy.</span><span class="sxs-lookup"><span data-stu-id="ceece-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="ceece-107">Příklady v tomto tématu ukazují výsledky, které jsou prezentovány ve standardní sestavě **Stárnutí zásob**.</span><span class="sxs-lookup"><span data-stu-id="ceece-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="ceece-108">Obecně však doporučujeme použít verzi [úložiště sestavy stárnutí zásob](inventory-aging-report-storage.md) této sestavy, zejména pokud máte mnoho položek a skladů, které je třeba zpracovat.</span><span class="sxs-lookup"><span data-stu-id="ceece-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="ceece-109">Úložiště sestavy stárnutí zásob ukládá každý vygenerovaný přehled, zobrazuje výsledky jako interaktivní stránku a graf a umožňuje exportovat všechny uložené sestavy.</span><span class="sxs-lookup"><span data-stu-id="ceece-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="ceece-110">Ukázková data použitá v těchto příkladech</span><span class="sxs-lookup"><span data-stu-id="ceece-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="ceece-111">Příklady v tomto tématu jsou založeny na ukázkových datech skladových transakcí, které jsou popsány v této části.</span><span class="sxs-lookup"><span data-stu-id="ceece-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="ceece-112">Nastavení dimenze úložiště</span><span class="sxs-lookup"><span data-stu-id="ceece-112">Storage dimension setup</span></span>

<span data-ttu-id="ceece-113">Příklad systému obsahuje následující nastavení dimenzí úložiště.</span><span class="sxs-lookup"><span data-stu-id="ceece-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="ceece-114">Jméno</span><span class="sxs-lookup"><span data-stu-id="ceece-114">Name</span></span>      | <span data-ttu-id="ceece-115">Aktivní</span><span class="sxs-lookup"><span data-stu-id="ceece-115">Active</span></span> | <span data-ttu-id="ceece-116">Fyzické zásoby</span><span class="sxs-lookup"><span data-stu-id="ceece-116">Physical inventory</span></span> | <span data-ttu-id="ceece-117">Finanční zásoby</span><span class="sxs-lookup"><span data-stu-id="ceece-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="ceece-118">Lokalita</span><span class="sxs-lookup"><span data-stu-id="ceece-118">Site</span></span>      | <span data-ttu-id="ceece-119">Ano</span><span class="sxs-lookup"><span data-stu-id="ceece-119">Yes</span></span>    | <span data-ttu-id="ceece-120">Ano</span><span class="sxs-lookup"><span data-stu-id="ceece-120">Yes</span></span>                | <span data-ttu-id="ceece-121">Ano</span><span class="sxs-lookup"><span data-stu-id="ceece-121">Yes</span></span>                 |
| <span data-ttu-id="ceece-122">Sklad</span><span class="sxs-lookup"><span data-stu-id="ceece-122">Warehouse</span></span> | <span data-ttu-id="ceece-123">Ano</span><span class="sxs-lookup"><span data-stu-id="ceece-123">Yes</span></span>    | <span data-ttu-id="ceece-124">Ano</span><span class="sxs-lookup"><span data-stu-id="ceece-124">Yes</span></span>                | <span data-ttu-id="ceece-125">Žádný</span><span class="sxs-lookup"><span data-stu-id="ceece-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="ceece-126">Model zásob</span><span class="sxs-lookup"><span data-stu-id="ceece-126">Inventory model</span></span>

<span data-ttu-id="ceece-127">Skladový model vydaných produktů je v příkladu systému *FIFO* a nastavení **nákladové ceny** pro skladový model je *Zahrnout fyzickou hodnotu*.</span><span class="sxs-lookup"><span data-stu-id="ceece-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="ceece-128">Transakce zásob</span><span class="sxs-lookup"><span data-stu-id="ceece-128">Inventory transactions</span></span>

<span data-ttu-id="ceece-129">Příklad systému obsahuje následující transakce zásob vydaného produktu, který má číslo položky *1000*.</span><span class="sxs-lookup"><span data-stu-id="ceece-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="ceece-130">Odkaz</span><span class="sxs-lookup"><span data-stu-id="ceece-130">Reference</span></span>      | <span data-ttu-id="ceece-131">Lokalita</span><span class="sxs-lookup"><span data-stu-id="ceece-131">Site</span></span> | <span data-ttu-id="ceece-132">Sklad</span><span class="sxs-lookup"><span data-stu-id="ceece-132">Warehouse</span></span> | <span data-ttu-id="ceece-133">Příjem</span><span class="sxs-lookup"><span data-stu-id="ceece-133">Receipt</span></span>   | <span data-ttu-id="ceece-134">Výdej</span><span class="sxs-lookup"><span data-stu-id="ceece-134">Issue</span></span> | <span data-ttu-id="ceece-135">Fyzické datum</span><span class="sxs-lookup"><span data-stu-id="ceece-135">Physical date</span></span> | <span data-ttu-id="ceece-136">Finanční datum</span><span class="sxs-lookup"><span data-stu-id="ceece-136">Financial date</span></span> | <span data-ttu-id="ceece-137">Množství</span><span class="sxs-lookup"><span data-stu-id="ceece-137">Quantity</span></span> | <span data-ttu-id="ceece-138">Částka nákladů</span><span class="sxs-lookup"><span data-stu-id="ceece-138">Cost amount</span></span> | <span data-ttu-id="ceece-139">Fyzická částka nákladů</span><span class="sxs-lookup"><span data-stu-id="ceece-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="ceece-140">Nákupní objednávka</span><span class="sxs-lookup"><span data-stu-id="ceece-140">Purchase order</span></span> | <span data-ttu-id="ceece-141">1</span><span class="sxs-lookup"><span data-stu-id="ceece-141">1</span></span>    | <span data-ttu-id="ceece-142">11</span><span class="sxs-lookup"><span data-stu-id="ceece-142">11</span></span>        | <span data-ttu-id="ceece-143">Koupeno</span><span class="sxs-lookup"><span data-stu-id="ceece-143">Purchased</span></span> |       | <span data-ttu-id="ceece-144">15. březen</span><span class="sxs-lookup"><span data-stu-id="ceece-144">March 15</span></span>      | <span data-ttu-id="ceece-145">15. březen</span><span class="sxs-lookup"><span data-stu-id="ceece-145">March 15</span></span>       | <span data-ttu-id="ceece-146">10</span><span class="sxs-lookup"><span data-stu-id="ceece-146">10</span></span>       | <span data-ttu-id="ceece-147">1 000</span><span class="sxs-lookup"><span data-stu-id="ceece-147">1,000</span></span>       | <span data-ttu-id="ceece-148">1 000</span><span class="sxs-lookup"><span data-stu-id="ceece-148">1,000</span></span>                |
| <span data-ttu-id="ceece-149">Nákupní objednávka</span><span class="sxs-lookup"><span data-stu-id="ceece-149">Purchase order</span></span> | <span data-ttu-id="ceece-150">2</span><span class="sxs-lookup"><span data-stu-id="ceece-150">2</span></span>    | <span data-ttu-id="ceece-151">21</span><span class="sxs-lookup"><span data-stu-id="ceece-151">21</span></span>        | <span data-ttu-id="ceece-152">Koupeno</span><span class="sxs-lookup"><span data-stu-id="ceece-152">Purchased</span></span> |       | <span data-ttu-id="ceece-153">15. březen</span><span class="sxs-lookup"><span data-stu-id="ceece-153">March 15</span></span>      | <span data-ttu-id="ceece-154">15. březen</span><span class="sxs-lookup"><span data-stu-id="ceece-154">March 15</span></span>       | <span data-ttu-id="ceece-155">10</span><span class="sxs-lookup"><span data-stu-id="ceece-155">10</span></span>       | <span data-ttu-id="ceece-156">2,000</span><span class="sxs-lookup"><span data-stu-id="ceece-156">2,000</span></span>       | <span data-ttu-id="ceece-157">2,000</span><span class="sxs-lookup"><span data-stu-id="ceece-157">2,000</span></span>                |
| <span data-ttu-id="ceece-158">Nákupní objednávka</span><span class="sxs-lookup"><span data-stu-id="ceece-158">Purchase order</span></span> | <span data-ttu-id="ceece-159">1</span><span class="sxs-lookup"><span data-stu-id="ceece-159">1</span></span>    | <span data-ttu-id="ceece-160">11</span><span class="sxs-lookup"><span data-stu-id="ceece-160">11</span></span>        | <span data-ttu-id="ceece-161">Přijato</span><span class="sxs-lookup"><span data-stu-id="ceece-161">Received</span></span>  |       | <span data-ttu-id="ceece-162">15. duben</span><span class="sxs-lookup"><span data-stu-id="ceece-162">April 15</span></span>      |                | <span data-ttu-id="ceece-163">5</span><span class="sxs-lookup"><span data-stu-id="ceece-163">5</span></span>        |             | <span data-ttu-id="ceece-164">375</span><span class="sxs-lookup"><span data-stu-id="ceece-164">375</span></span>                  |
| <span data-ttu-id="ceece-165">Objednávka převozu</span><span class="sxs-lookup"><span data-stu-id="ceece-165">Transfer order</span></span> | <span data-ttu-id="ceece-166">1</span><span class="sxs-lookup"><span data-stu-id="ceece-166">1</span></span>    | <span data-ttu-id="ceece-167">11</span><span class="sxs-lookup"><span data-stu-id="ceece-167">11</span></span>        |           | <span data-ttu-id="ceece-168">Prodáno</span><span class="sxs-lookup"><span data-stu-id="ceece-168">Sold</span></span>  | <span data-ttu-id="ceece-169">2. květen</span><span class="sxs-lookup"><span data-stu-id="ceece-169">May 2</span></span>         | <span data-ttu-id="ceece-170">2. květen</span><span class="sxs-lookup"><span data-stu-id="ceece-170">May 2</span></span>          | <span data-ttu-id="ceece-171">-5</span><span class="sxs-lookup"><span data-stu-id="ceece-171">-5</span></span>       | <span data-ttu-id="ceece-172">-458,33</span><span class="sxs-lookup"><span data-stu-id="ceece-172">-458.33</span></span>     | <span data-ttu-id="ceece-173">-458,33</span><span class="sxs-lookup"><span data-stu-id="ceece-173">-458.33</span></span>              |
| <span data-ttu-id="ceece-174">Objednávka převozu</span><span class="sxs-lookup"><span data-stu-id="ceece-174">Transfer order</span></span> | <span data-ttu-id="ceece-175">1</span><span class="sxs-lookup"><span data-stu-id="ceece-175">1</span></span>    | <span data-ttu-id="ceece-176">12</span><span class="sxs-lookup"><span data-stu-id="ceece-176">12</span></span>        | <span data-ttu-id="ceece-177">Koupeno</span><span class="sxs-lookup"><span data-stu-id="ceece-177">Purchased</span></span> |       | <span data-ttu-id="ceece-178">2. květen</span><span class="sxs-lookup"><span data-stu-id="ceece-178">May 2</span></span>         | <span data-ttu-id="ceece-179">2. květen</span><span class="sxs-lookup"><span data-stu-id="ceece-179">May 2</span></span>          | <span data-ttu-id="ceece-180">5</span><span class="sxs-lookup"><span data-stu-id="ceece-180">5</span></span>        | <span data-ttu-id="ceece-181">458.33</span><span class="sxs-lookup"><span data-stu-id="ceece-181">458.33</span></span>      | <span data-ttu-id="ceece-182">458.33</span><span class="sxs-lookup"><span data-stu-id="ceece-182">458.33</span></span>               |
| <span data-ttu-id="ceece-183">Prodejní objednávka</span><span class="sxs-lookup"><span data-stu-id="ceece-183">Sales order</span></span>    | <span data-ttu-id="ceece-184">1</span><span class="sxs-lookup"><span data-stu-id="ceece-184">1</span></span>    | <span data-ttu-id="ceece-185">12</span><span class="sxs-lookup"><span data-stu-id="ceece-185">12</span></span>        |           | <span data-ttu-id="ceece-186">Prodáno</span><span class="sxs-lookup"><span data-stu-id="ceece-186">Sold</span></span>  | <span data-ttu-id="ceece-187">3. květen</span><span class="sxs-lookup"><span data-stu-id="ceece-187">May 3</span></span>         | <span data-ttu-id="ceece-188">3. květen</span><span class="sxs-lookup"><span data-stu-id="ceece-188">May 3</span></span>          | <span data-ttu-id="ceece-189">-1</span><span class="sxs-lookup"><span data-stu-id="ceece-189">-1</span></span>       | <span data-ttu-id="ceece-190">-91,67</span><span class="sxs-lookup"><span data-stu-id="ceece-190">-91.67</span></span>      | <span data-ttu-id="ceece-191">-91,67</span><span class="sxs-lookup"><span data-stu-id="ceece-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="ceece-192">Jak se vypočítává množství a částky v jednotlivých intervalech období</span><span class="sxs-lookup"><span data-stu-id="ceece-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="ceece-193">Pomocí ukázkových dat, která jsou popsána v předchozích částech, můžete spustit sestavu **Stárnutí zásob**, která má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ceece-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="ceece-194">**K datu:** *9. května 2020*</span><span class="sxs-lookup"><span data-stu-id="ceece-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="ceece-195">**Pracoviště:** *Zobrazit*</span><span class="sxs-lookup"><span data-stu-id="ceece-195">**Site:** *View*</span></span>
- <span data-ttu-id="ceece-196">**Sklad:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="ceece-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="ceece-197">**Číslo položky:** *Součet*</span><span class="sxs-lookup"><span data-stu-id="ceece-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="ceece-198">**Doba stárnutí:** Toto pole nastavte tak, aby generovalo měsíční intervaly.</span><span class="sxs-lookup"><span data-stu-id="ceece-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="ceece-199">V takovém případě bude obsah vygenerované sestavy vypadat jako v následujícím příkladu.</span><span class="sxs-lookup"><span data-stu-id="ceece-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="ceece-200">Č. položky</span><span class="sxs-lookup"><span data-stu-id="ceece-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="ceece-201">Lokalita</span><span class="sxs-lookup"><span data-stu-id="ceece-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="ceece-202">Množství na skladě</span><span class="sxs-lookup"><span data-stu-id="ceece-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="ceece-203">Hodnota položek na skladě</span><span class="sxs-lookup"><span data-stu-id="ceece-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="ceece-204">Hodnota/množství skladových zásob</span><span class="sxs-lookup"><span data-stu-id="ceece-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="ceece-205">Hodnota zásob</span><span class="sxs-lookup"><span data-stu-id="ceece-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="ceece-206">Průměrné náklady na jednotku</span><span class="sxs-lookup"><span data-stu-id="ceece-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="ceece-207">5/8/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="ceece-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="ceece-208">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="ceece-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="ceece-209">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="ceece-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="ceece-210">P1:Množství</span><span class="sxs-lookup"><span data-stu-id="ceece-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="ceece-211">P1:Částka</span><span class="sxs-lookup"><span data-stu-id="ceece-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="ceece-212">P2:Množství</span><span class="sxs-lookup"><span data-stu-id="ceece-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="ceece-213">P2:Částka</span><span class="sxs-lookup"><span data-stu-id="ceece-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="ceece-214">P3:Množství</span><span class="sxs-lookup"><span data-stu-id="ceece-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="ceece-215">P3:Částka</span><span class="sxs-lookup"><span data-stu-id="ceece-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="ceece-216">1 000</span><span class="sxs-lookup"><span data-stu-id="ceece-216">1000</span></span></td>
    <td><span data-ttu-id="ceece-217">1</span><span class="sxs-lookup"><span data-stu-id="ceece-217">1</span></span></td>
    <td><span data-ttu-id="ceece-218">14</span><span class="sxs-lookup"><span data-stu-id="ceece-218">14</span></span></td>
    <td><span data-ttu-id="ceece-219">1,283.33</span><span class="sxs-lookup"><span data-stu-id="ceece-219">1,283.33</span></span></td>
    <td><span data-ttu-id="ceece-220">14</span><span class="sxs-lookup"><span data-stu-id="ceece-220">14</span></span></td>
    <td><span data-ttu-id="ceece-221">1,283.33</span><span class="sxs-lookup"><span data-stu-id="ceece-221">1,283.33</span></span></td>
    <td><span data-ttu-id="ceece-222">91.67</span><span class="sxs-lookup"><span data-stu-id="ceece-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="ceece-223">5.00</span><span class="sxs-lookup"><span data-stu-id="ceece-223">5.00</span></span></td>
    <td><span data-ttu-id="ceece-224">458.33</span><span class="sxs-lookup"><span data-stu-id="ceece-224">458.33</span></span></td>
    <td><span data-ttu-id="ceece-225">9.00</span><span class="sxs-lookup"><span data-stu-id="ceece-225">9.00</span></span></td>
    <td><span data-ttu-id="ceece-226">825.00</span><span class="sxs-lookup"><span data-stu-id="ceece-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="ceece-227">1 000</span><span class="sxs-lookup"><span data-stu-id="ceece-227">1000</span></span></td>
    <td><span data-ttu-id="ceece-228">2</span><span class="sxs-lookup"><span data-stu-id="ceece-228">2</span></span></td>
    <td><span data-ttu-id="ceece-229">10</span><span class="sxs-lookup"><span data-stu-id="ceece-229">10</span></span></td>
    <td><span data-ttu-id="ceece-230">2,000.00</span><span class="sxs-lookup"><span data-stu-id="ceece-230">2,000.00</span></span></td>
    <td><span data-ttu-id="ceece-231">10</span><span class="sxs-lookup"><span data-stu-id="ceece-231">10</span></span></td>
    <td><span data-ttu-id="ceece-232">2,000.00</span><span class="sxs-lookup"><span data-stu-id="ceece-232">2,000.00</span></span></td>
    <td><span data-ttu-id="ceece-233">200.00</span><span class="sxs-lookup"><span data-stu-id="ceece-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="ceece-234">10.00</span><span class="sxs-lookup"><span data-stu-id="ceece-234">10.00</span></span></td>
    <td><span data-ttu-id="ceece-235">2,000.00</span><span class="sxs-lookup"><span data-stu-id="ceece-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="ceece-236"><strong>Celkem 1000</strong></span><span class="sxs-lookup"><span data-stu-id="ceece-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="ceece-237"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="ceece-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="ceece-238"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="ceece-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="ceece-239"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="ceece-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="ceece-240"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="ceece-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="ceece-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="ceece-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="ceece-242"><strong>2,825.00</strong></span><span class="sxs-lookup"><span data-stu-id="ceece-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="ceece-243">V této ukázkové sestavě si všimněte následujících podrobností:</span><span class="sxs-lookup"><span data-stu-id="ceece-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="ceece-244">Hodnoty **Množství hodnoty zásob**, **Hodnota zásob** a **Průměrná jednotková cena** uvedené v sestavě jsou hodnoty dimenze finančních zásob (v tomto případě **Pracoviště**).</span><span class="sxs-lookup"><span data-stu-id="ceece-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="ceece-245">Například pro pracoviště 1 obsahuje sestava následující informace:</span><span class="sxs-lookup"><span data-stu-id="ceece-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="ceece-246">Hodnota **Množství hodnoty zásob** je *14* (= 10 + 5 - 5 + 5 - 1).</span><span class="sxs-lookup"><span data-stu-id="ceece-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="ceece-247">Hodnota **Hodnota zásob** je *1,283.33* (= 1,000 + 375 - 458.33 + 458.33 - 91.67).</span><span class="sxs-lookup"><span data-stu-id="ceece-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="ceece-248">Hodnota **Průměrné náklady na jednotku** je *91,67*.</span><span class="sxs-lookup"><span data-stu-id="ceece-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="ceece-249">Hodnota **Hodnota na skladě** a hodnota **Částka** v jednotlivých intervalech období se vypočítává pomocí hodnoty **Průměrná jednotková cena**.</span><span class="sxs-lookup"><span data-stu-id="ceece-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="ceece-250">Sestava určuje množství na skladě pro každý interval období sečtením celkového přijatého skladového množství pro každý interval období.</span><span class="sxs-lookup"><span data-stu-id="ceece-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="ceece-251">Následně použije princip FIFO (první dovnitř, první ven) k odečtení celkového vydaného množství bez ohledu na model zásob, který položky používají.</span><span class="sxs-lookup"><span data-stu-id="ceece-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="ceece-252">Pokud stejnou sestavu spustíte znovu, ale tentokrát nastavíte pole **Pracoviště** i **Sklad** na *Zobrazení*, bude nová sestava vypadat jako v následujícím příkladu.</span><span class="sxs-lookup"><span data-stu-id="ceece-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="ceece-253">Č. položky</span><span class="sxs-lookup"><span data-stu-id="ceece-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="ceece-254">Lokalita</span><span class="sxs-lookup"><span data-stu-id="ceece-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="ceece-255">Sklad</span><span class="sxs-lookup"><span data-stu-id="ceece-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="ceece-256">Množství na skladě</span><span class="sxs-lookup"><span data-stu-id="ceece-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="ceece-257">Hodnota položek na skladě</span><span class="sxs-lookup"><span data-stu-id="ceece-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="ceece-258">Hodnota/množství skladových zásob</span><span class="sxs-lookup"><span data-stu-id="ceece-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="ceece-259">Hodnota zásob</span><span class="sxs-lookup"><span data-stu-id="ceece-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="ceece-260">Průměrné náklady na jednotku</span><span class="sxs-lookup"><span data-stu-id="ceece-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="ceece-261">5/8/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="ceece-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="ceece-262">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="ceece-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="ceece-263">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="ceece-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="ceece-264">P1:Množství</span><span class="sxs-lookup"><span data-stu-id="ceece-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="ceece-265">P1:Částka</span><span class="sxs-lookup"><span data-stu-id="ceece-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="ceece-266">P2:Množství</span><span class="sxs-lookup"><span data-stu-id="ceece-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="ceece-267">P2:Částka</span><span class="sxs-lookup"><span data-stu-id="ceece-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="ceece-268">P3:Množství</span><span class="sxs-lookup"><span data-stu-id="ceece-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="ceece-269">P3:Částka</span><span class="sxs-lookup"><span data-stu-id="ceece-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="ceece-270">1 000</span><span class="sxs-lookup"><span data-stu-id="ceece-270">1000</span></span></td>
    <td><span data-ttu-id="ceece-271">1</span><span class="sxs-lookup"><span data-stu-id="ceece-271">1</span></span></td>
    <td><span data-ttu-id="ceece-272">11</span><span class="sxs-lookup"><span data-stu-id="ceece-272">11</span></span></td>
    <td><span data-ttu-id="ceece-273">10</span><span class="sxs-lookup"><span data-stu-id="ceece-273">10</span></span></td>
    <td><span data-ttu-id="ceece-274">916.67</span><span class="sxs-lookup"><span data-stu-id="ceece-274">916.67</span></span></td>
    <td><span data-ttu-id="ceece-275">14</span><span class="sxs-lookup"><span data-stu-id="ceece-275">14</span></span></td>
    <td><span data-ttu-id="ceece-276">1,283.33</span><span class="sxs-lookup"><span data-stu-id="ceece-276">1,283.33</span></span></td>
    <td><span data-ttu-id="ceece-277">91.67</span><span class="sxs-lookup"><span data-stu-id="ceece-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="ceece-278">5.00</span><span class="sxs-lookup"><span data-stu-id="ceece-278">5.00</span></span></td>
    <td><span data-ttu-id="ceece-279">458.33</span><span class="sxs-lookup"><span data-stu-id="ceece-279">458.33</span></span></td>
    <td><span data-ttu-id="ceece-280">5.00</span><span class="sxs-lookup"><span data-stu-id="ceece-280">5.00</span></span></td>
    <td><span data-ttu-id="ceece-281">458.33</span><span class="sxs-lookup"><span data-stu-id="ceece-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="ceece-282">1 000</span><span class="sxs-lookup"><span data-stu-id="ceece-282">1000</span></span></td>
    <td><span data-ttu-id="ceece-283">1</span><span class="sxs-lookup"><span data-stu-id="ceece-283">1</span></span></td>
    <td><span data-ttu-id="ceece-284">12</span><span class="sxs-lookup"><span data-stu-id="ceece-284">12</span></span></td>
    <td><span data-ttu-id="ceece-285">4</span><span class="sxs-lookup"><span data-stu-id="ceece-285">4</span></span></td>
    <td><span data-ttu-id="ceece-286">366.67</span><span class="sxs-lookup"><span data-stu-id="ceece-286">366.67</span></span></td>
    <td><span data-ttu-id="ceece-287">14</span><span class="sxs-lookup"><span data-stu-id="ceece-287">14</span></span></td>
    <td><span data-ttu-id="ceece-288">1,283.33</span><span class="sxs-lookup"><span data-stu-id="ceece-288">1,283.33</span></span></td>
    <td><span data-ttu-id="ceece-289">91.67</span><span class="sxs-lookup"><span data-stu-id="ceece-289">91.67</span></span></td>
    <td><span data-ttu-id="ceece-290">4.00</span><span class="sxs-lookup"><span data-stu-id="ceece-290">4.00</span></span></td>
    <td><span data-ttu-id="ceece-291">366.67</span><span class="sxs-lookup"><span data-stu-id="ceece-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="ceece-292">1 000</span><span class="sxs-lookup"><span data-stu-id="ceece-292">1000</span></span></td>
    <td><span data-ttu-id="ceece-293">2</span><span class="sxs-lookup"><span data-stu-id="ceece-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="ceece-294">10</span><span class="sxs-lookup"><span data-stu-id="ceece-294">10</span></span></td>
    <td><span data-ttu-id="ceece-295">2,000.00</span><span class="sxs-lookup"><span data-stu-id="ceece-295">2,000.00</span></span></td>
    <td><span data-ttu-id="ceece-296">10</span><span class="sxs-lookup"><span data-stu-id="ceece-296">10</span></span></td>
    <td><span data-ttu-id="ceece-297">2,000.00</span><span class="sxs-lookup"><span data-stu-id="ceece-297">2,000.00</span></span></td>
    <td><span data-ttu-id="ceece-298">200.00</span><span class="sxs-lookup"><span data-stu-id="ceece-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="ceece-299">10.00</span><span class="sxs-lookup"><span data-stu-id="ceece-299">10.00</span></span></td>
    <td><span data-ttu-id="ceece-300">2,000.00</span><span class="sxs-lookup"><span data-stu-id="ceece-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="ceece-301"><strong>Celkem 1000</strong></span><span class="sxs-lookup"><span data-stu-id="ceece-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="ceece-302"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="ceece-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="ceece-303"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="ceece-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="ceece-304"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="ceece-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="ceece-305"><strong>366.67</strong></span><span class="sxs-lookup"><span data-stu-id="ceece-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="ceece-306"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="ceece-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="ceece-307"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="ceece-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="ceece-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="ceece-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="ceece-309"><strong>2,458.33</strong></span><span class="sxs-lookup"><span data-stu-id="ceece-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="ceece-310">Tentokrát je pracoviště 1 rozděleno na dva řádky, jeden pro sklad 11 a jeden pro sklad 12.</span><span class="sxs-lookup"><span data-stu-id="ceece-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="ceece-311">Hodnoty **Množství hodnoty zásob**, **Hodnota zásob** a **Průměrná jednotková cena** uvedené v sestavě jsou však stejné, protože **Sklad** není dimenze finančních zásob.</span><span class="sxs-lookup"><span data-stu-id="ceece-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="ceece-312">Dále si všimněte, že distribuce množství na pracovišti 1 je odlišná.</span><span class="sxs-lookup"><span data-stu-id="ceece-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="ceece-313">V první sestavě, kterou jste spustili, systém ignoroval příkaz k převodu, ke kterému došlo na stejném pracovišti, a odečetl množství prodejní faktury z intervalu období **31. 3. 2020 - 3. 1. 2020** na pracovišti 1.</span><span class="sxs-lookup"><span data-stu-id="ceece-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="ceece-314">V nové sestavě však systém odečte z prodejní faktury množství z intervalu období **5. 5. 2012 - 5. 1. 2012** ve skladu 12.</span><span class="sxs-lookup"><span data-stu-id="ceece-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="ceece-315">Dopady uzávěrky skladu</span><span class="sxs-lookup"><span data-stu-id="ceece-315">Effects of inventory closing</span></span>

<span data-ttu-id="ceece-316">Pokud spustíte uzávěrku zásob na květen a poté znovu spustíte předchozí sestavu, ale nastavíte hodnotu v poli **K datu** na *31. května 2020*, všimnete si následujících výsledků:</span><span class="sxs-lookup"><span data-stu-id="ceece-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="ceece-317">Hodnoty **Hodnota zásob** a **Průměrné jednotkové náklady** se aktualizují.</span><span class="sxs-lookup"><span data-stu-id="ceece-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="ceece-318">Hodnota **Hodnota na skladě** a všechny hodnoty **Částka** v každém intervalu období se aktualizují odpovídajícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="ceece-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="ceece-319">Nová sestava bude vypadat podobně jako v následujícím příkladu.</span><span class="sxs-lookup"><span data-stu-id="ceece-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="ceece-320">Č. položky</span><span class="sxs-lookup"><span data-stu-id="ceece-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="ceece-321">Lokalita</span><span class="sxs-lookup"><span data-stu-id="ceece-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="ceece-322">Sklad</span><span class="sxs-lookup"><span data-stu-id="ceece-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="ceece-323">Množství na skladě</span><span class="sxs-lookup"><span data-stu-id="ceece-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="ceece-324">Hodnota položek na skladě</span><span class="sxs-lookup"><span data-stu-id="ceece-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="ceece-325">Hodnota/množství skladových zásob</span><span class="sxs-lookup"><span data-stu-id="ceece-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="ceece-326">Hodnota zásob</span><span class="sxs-lookup"><span data-stu-id="ceece-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="ceece-327">Průměrné náklady na jednotku</span><span class="sxs-lookup"><span data-stu-id="ceece-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="ceece-328">5/31/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="ceece-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="ceece-329">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="ceece-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="ceece-330">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="ceece-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="ceece-331">P1:Množství</span><span class="sxs-lookup"><span data-stu-id="ceece-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="ceece-332">P1:Částka</span><span class="sxs-lookup"><span data-stu-id="ceece-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="ceece-333">P2:Množství</span><span class="sxs-lookup"><span data-stu-id="ceece-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="ceece-334">P2:Částka</span><span class="sxs-lookup"><span data-stu-id="ceece-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="ceece-335">P3:Množství</span><span class="sxs-lookup"><span data-stu-id="ceece-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="ceece-336">P3:Částka</span><span class="sxs-lookup"><span data-stu-id="ceece-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="ceece-337">1 000</span><span class="sxs-lookup"><span data-stu-id="ceece-337">1000</span></span></td>
    <td><span data-ttu-id="ceece-338">1</span><span class="sxs-lookup"><span data-stu-id="ceece-338">1</span></span></td>
    <td><span data-ttu-id="ceece-339">11</span><span class="sxs-lookup"><span data-stu-id="ceece-339">11</span></span></td>
    <td><span data-ttu-id="ceece-340">10</span><span class="sxs-lookup"><span data-stu-id="ceece-340">10</span></span></td>
    <td><span data-ttu-id="ceece-341">910.70</span><span class="sxs-lookup"><span data-stu-id="ceece-341">910.70</span></span></td>
    <td><span data-ttu-id="ceece-342">14</span><span class="sxs-lookup"><span data-stu-id="ceece-342">14</span></span></td>
    <td><span data-ttu-id="ceece-343">1,275.00</span><span class="sxs-lookup"><span data-stu-id="ceece-343">1,275.00</span></span></td>
    <td><span data-ttu-id="ceece-344">91.07</span><span class="sxs-lookup"><span data-stu-id="ceece-344">91.07</span></span></td>
    <td><span data-ttu-id="ceece-345">0,00</span><span class="sxs-lookup"><span data-stu-id="ceece-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="ceece-346">5.00</span><span class="sxs-lookup"><span data-stu-id="ceece-346">5.00</span></span></td>
    <td><span data-ttu-id="ceece-347">455.36</span><span class="sxs-lookup"><span data-stu-id="ceece-347">455.36</span></span></td>
    <td><span data-ttu-id="ceece-348">5.00</span><span class="sxs-lookup"><span data-stu-id="ceece-348">5.00</span></span></td>
    <td><span data-ttu-id="ceece-349">455.36</span><span class="sxs-lookup"><span data-stu-id="ceece-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="ceece-350">1 000</span><span class="sxs-lookup"><span data-stu-id="ceece-350">1000</span></span></td>
    <td><span data-ttu-id="ceece-351">1</span><span class="sxs-lookup"><span data-stu-id="ceece-351">1</span></span></td>
    <td><span data-ttu-id="ceece-352">12</span><span class="sxs-lookup"><span data-stu-id="ceece-352">12</span></span></td>
    <td><span data-ttu-id="ceece-353">4</span><span class="sxs-lookup"><span data-stu-id="ceece-353">4</span></span></td>
    <td><span data-ttu-id="ceece-354">364.29</span><span class="sxs-lookup"><span data-stu-id="ceece-354">364.29</span></span></td>
    <td><span data-ttu-id="ceece-355">14</span><span class="sxs-lookup"><span data-stu-id="ceece-355">14</span></span></td>
    <td><span data-ttu-id="ceece-356">1,275.00</span><span class="sxs-lookup"><span data-stu-id="ceece-356">1,275.00</span></span></td>
    <td><span data-ttu-id="ceece-357">91.07</span><span class="sxs-lookup"><span data-stu-id="ceece-357">91.07</span></span></td>
    <td><span data-ttu-id="ceece-358">4.00</span><span class="sxs-lookup"><span data-stu-id="ceece-358">4.00</span></span></td>
    <td><span data-ttu-id="ceece-359">364.29</span><span class="sxs-lookup"><span data-stu-id="ceece-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="ceece-360">1 000</span><span class="sxs-lookup"><span data-stu-id="ceece-360">1000</span></span></td>
    <td><span data-ttu-id="ceece-361">2</span><span class="sxs-lookup"><span data-stu-id="ceece-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="ceece-362">10</span><span class="sxs-lookup"><span data-stu-id="ceece-362">10</span></span></td>
    <td><span data-ttu-id="ceece-363">2,000.00</span><span class="sxs-lookup"><span data-stu-id="ceece-363">2,000.00</span></span></td>
    <td><span data-ttu-id="ceece-364">10</span><span class="sxs-lookup"><span data-stu-id="ceece-364">10</span></span></td>
    <td><span data-ttu-id="ceece-365">2,000.00</span><span class="sxs-lookup"><span data-stu-id="ceece-365">2,000.00</span></span></td>
    <td><span data-ttu-id="ceece-366">200.00</span><span class="sxs-lookup"><span data-stu-id="ceece-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="ceece-367">10.00</span><span class="sxs-lookup"><span data-stu-id="ceece-367">10.00</span></span></td>
    <td><span data-ttu-id="ceece-368">2,000.00</span><span class="sxs-lookup"><span data-stu-id="ceece-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="ceece-369"><strong>Celkem 1000</strong></span><span class="sxs-lookup"><span data-stu-id="ceece-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="ceece-370"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="ceece-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="ceece-371"><strong>3,275.00</strong></span><span class="sxs-lookup"><span data-stu-id="ceece-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="ceece-372"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="ceece-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="ceece-373"><strong>364.29</strong></span><span class="sxs-lookup"><span data-stu-id="ceece-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="ceece-374"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="ceece-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="ceece-375"><strong>455.36</strong></span><span class="sxs-lookup"><span data-stu-id="ceece-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="ceece-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="ceece-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="ceece-377"><strong>2,455.36</strong></span><span class="sxs-lookup"><span data-stu-id="ceece-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]