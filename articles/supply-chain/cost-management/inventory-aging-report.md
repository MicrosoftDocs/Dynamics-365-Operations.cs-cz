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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: a6e708e4dc818f20fc8d835053da75c2fe9c98f6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423794"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="5b86e-103">Příklady a logika sestavy stárnutí zásob</span><span class="sxs-lookup"><span data-stu-id="5b86e-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b86e-104">Toto téma uvádí několik příkladů, které ukazují, jak interpretovat výsledky sestavy **stárnutí zásob**.</span><span class="sxs-lookup"><span data-stu-id="5b86e-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="5b86e-105">Tato sestava kategorizuje hodnoty množství na skladě a zásob pro vybranou položku nebo skupinu položek do několika intervalů období.</span><span class="sxs-lookup"><span data-stu-id="5b86e-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="5b86e-106">Toto téma také ukazuje vnitřní logiku sestavy.</span><span class="sxs-lookup"><span data-stu-id="5b86e-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="5b86e-107">Příklady v tomto tématu ukazují výsledky, které jsou prezentovány ve standardní sestavě **Stárnutí zásob**.</span><span class="sxs-lookup"><span data-stu-id="5b86e-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="5b86e-108">Obecně však doporučujeme použít verzi [úložiště sestavy stárnutí zásob](inventory-aging-report-storage.md) této sestavy, zejména pokud máte mnoho položek a skladů, které je třeba zpracovat.</span><span class="sxs-lookup"><span data-stu-id="5b86e-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="5b86e-109">Úložiště sestavy stárnutí zásob ukládá každý vygenerovaný přehled, zobrazuje výsledky jako interaktivní stránku a graf a umožňuje exportovat všechny uložené sestavy.</span><span class="sxs-lookup"><span data-stu-id="5b86e-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="5b86e-110">Ukázková data použitá v těchto příkladech</span><span class="sxs-lookup"><span data-stu-id="5b86e-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="5b86e-111">Příklady v tomto tématu jsou založeny na ukázkových datech skladových transakcí, které jsou popsány v této části.</span><span class="sxs-lookup"><span data-stu-id="5b86e-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="5b86e-112">Nastavení dimenze úložiště</span><span class="sxs-lookup"><span data-stu-id="5b86e-112">Storage dimension setup</span></span>

<span data-ttu-id="5b86e-113">Příklad systému obsahuje následující nastavení dimenzí úložiště.</span><span class="sxs-lookup"><span data-stu-id="5b86e-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="5b86e-114">Jméno</span><span class="sxs-lookup"><span data-stu-id="5b86e-114">Name</span></span>      | <span data-ttu-id="5b86e-115">Aktivní</span><span class="sxs-lookup"><span data-stu-id="5b86e-115">Active</span></span> | <span data-ttu-id="5b86e-116">Fyzické zásoby</span><span class="sxs-lookup"><span data-stu-id="5b86e-116">Physical inventory</span></span> | <span data-ttu-id="5b86e-117">Finanční zásoby</span><span class="sxs-lookup"><span data-stu-id="5b86e-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="5b86e-118">Lokalita</span><span class="sxs-lookup"><span data-stu-id="5b86e-118">Site</span></span>      | <span data-ttu-id="5b86e-119">Ano</span><span class="sxs-lookup"><span data-stu-id="5b86e-119">Yes</span></span>    | <span data-ttu-id="5b86e-120">Ano</span><span class="sxs-lookup"><span data-stu-id="5b86e-120">Yes</span></span>                | <span data-ttu-id="5b86e-121">Ano</span><span class="sxs-lookup"><span data-stu-id="5b86e-121">Yes</span></span>                 |
| <span data-ttu-id="5b86e-122">Sklad</span><span class="sxs-lookup"><span data-stu-id="5b86e-122">Warehouse</span></span> | <span data-ttu-id="5b86e-123">Ano</span><span class="sxs-lookup"><span data-stu-id="5b86e-123">Yes</span></span>    | <span data-ttu-id="5b86e-124">Ano</span><span class="sxs-lookup"><span data-stu-id="5b86e-124">Yes</span></span>                | <span data-ttu-id="5b86e-125">Žádný</span><span class="sxs-lookup"><span data-stu-id="5b86e-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="5b86e-126">Model zásob</span><span class="sxs-lookup"><span data-stu-id="5b86e-126">Inventory model</span></span>

<span data-ttu-id="5b86e-127">Skladový model vydaných produktů je v příkladu systému *FIFO* a nastavení **nákladové ceny** pro skladový model je *Zahrnout fyzickou hodnotu*.</span><span class="sxs-lookup"><span data-stu-id="5b86e-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="5b86e-128">Transakce zásob</span><span class="sxs-lookup"><span data-stu-id="5b86e-128">Inventory transactions</span></span>

<span data-ttu-id="5b86e-129">Příklad systému obsahuje následující transakce zásob vydaného produktu, který má číslo položky *1000*.</span><span class="sxs-lookup"><span data-stu-id="5b86e-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="5b86e-130">Odkaz</span><span class="sxs-lookup"><span data-stu-id="5b86e-130">Reference</span></span>      | <span data-ttu-id="5b86e-131">Lokalita</span><span class="sxs-lookup"><span data-stu-id="5b86e-131">Site</span></span> | <span data-ttu-id="5b86e-132">Sklad</span><span class="sxs-lookup"><span data-stu-id="5b86e-132">Warehouse</span></span> | <span data-ttu-id="5b86e-133">Příjem</span><span class="sxs-lookup"><span data-stu-id="5b86e-133">Receipt</span></span>   | <span data-ttu-id="5b86e-134">Výdej</span><span class="sxs-lookup"><span data-stu-id="5b86e-134">Issue</span></span> | <span data-ttu-id="5b86e-135">Fyzické datum</span><span class="sxs-lookup"><span data-stu-id="5b86e-135">Physical date</span></span> | <span data-ttu-id="5b86e-136">Finanční datum</span><span class="sxs-lookup"><span data-stu-id="5b86e-136">Financial date</span></span> | <span data-ttu-id="5b86e-137">Množství</span><span class="sxs-lookup"><span data-stu-id="5b86e-137">Quantity</span></span> | <span data-ttu-id="5b86e-138">Částka nákladů</span><span class="sxs-lookup"><span data-stu-id="5b86e-138">Cost amount</span></span> | <span data-ttu-id="5b86e-139">Fyzická částka nákladů</span><span class="sxs-lookup"><span data-stu-id="5b86e-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="5b86e-140">Nákupní objednávka</span><span class="sxs-lookup"><span data-stu-id="5b86e-140">Purchase order</span></span> | <span data-ttu-id="5b86e-141">1</span><span class="sxs-lookup"><span data-stu-id="5b86e-141">1</span></span>    | <span data-ttu-id="5b86e-142">11</span><span class="sxs-lookup"><span data-stu-id="5b86e-142">11</span></span>        | <span data-ttu-id="5b86e-143">Koupeno</span><span class="sxs-lookup"><span data-stu-id="5b86e-143">Purchased</span></span> |       | <span data-ttu-id="5b86e-144">15. březen</span><span class="sxs-lookup"><span data-stu-id="5b86e-144">March 15</span></span>      | <span data-ttu-id="5b86e-145">15. březen</span><span class="sxs-lookup"><span data-stu-id="5b86e-145">March 15</span></span>       | <span data-ttu-id="5b86e-146">10</span><span class="sxs-lookup"><span data-stu-id="5b86e-146">10</span></span>       | <span data-ttu-id="5b86e-147">1 000</span><span class="sxs-lookup"><span data-stu-id="5b86e-147">1,000</span></span>       | <span data-ttu-id="5b86e-148">1 000</span><span class="sxs-lookup"><span data-stu-id="5b86e-148">1,000</span></span>                |
| <span data-ttu-id="5b86e-149">Nákupní objednávka</span><span class="sxs-lookup"><span data-stu-id="5b86e-149">Purchase order</span></span> | <span data-ttu-id="5b86e-150">2</span><span class="sxs-lookup"><span data-stu-id="5b86e-150">2</span></span>    | <span data-ttu-id="5b86e-151">21</span><span class="sxs-lookup"><span data-stu-id="5b86e-151">21</span></span>        | <span data-ttu-id="5b86e-152">Koupeno</span><span class="sxs-lookup"><span data-stu-id="5b86e-152">Purchased</span></span> |       | <span data-ttu-id="5b86e-153">15. březen</span><span class="sxs-lookup"><span data-stu-id="5b86e-153">March 15</span></span>      | <span data-ttu-id="5b86e-154">15. březen</span><span class="sxs-lookup"><span data-stu-id="5b86e-154">March 15</span></span>       | <span data-ttu-id="5b86e-155">10</span><span class="sxs-lookup"><span data-stu-id="5b86e-155">10</span></span>       | <span data-ttu-id="5b86e-156">2,000</span><span class="sxs-lookup"><span data-stu-id="5b86e-156">2,000</span></span>       | <span data-ttu-id="5b86e-157">2,000</span><span class="sxs-lookup"><span data-stu-id="5b86e-157">2,000</span></span>                |
| <span data-ttu-id="5b86e-158">Nákupní objednávka</span><span class="sxs-lookup"><span data-stu-id="5b86e-158">Purchase order</span></span> | <span data-ttu-id="5b86e-159">1</span><span class="sxs-lookup"><span data-stu-id="5b86e-159">1</span></span>    | <span data-ttu-id="5b86e-160">11</span><span class="sxs-lookup"><span data-stu-id="5b86e-160">11</span></span>        | <span data-ttu-id="5b86e-161">Přijato</span><span class="sxs-lookup"><span data-stu-id="5b86e-161">Received</span></span>  |       | <span data-ttu-id="5b86e-162">15. duben</span><span class="sxs-lookup"><span data-stu-id="5b86e-162">April 15</span></span>      |                | <span data-ttu-id="5b86e-163">5</span><span class="sxs-lookup"><span data-stu-id="5b86e-163">5</span></span>        |             | <span data-ttu-id="5b86e-164">375</span><span class="sxs-lookup"><span data-stu-id="5b86e-164">375</span></span>                  |
| <span data-ttu-id="5b86e-165">Objednávka převozu</span><span class="sxs-lookup"><span data-stu-id="5b86e-165">Transfer order</span></span> | <span data-ttu-id="5b86e-166">1</span><span class="sxs-lookup"><span data-stu-id="5b86e-166">1</span></span>    | <span data-ttu-id="5b86e-167">11</span><span class="sxs-lookup"><span data-stu-id="5b86e-167">11</span></span>        |           | <span data-ttu-id="5b86e-168">Prodáno</span><span class="sxs-lookup"><span data-stu-id="5b86e-168">Sold</span></span>  | <span data-ttu-id="5b86e-169">2. květen</span><span class="sxs-lookup"><span data-stu-id="5b86e-169">May 2</span></span>         | <span data-ttu-id="5b86e-170">2. květen</span><span class="sxs-lookup"><span data-stu-id="5b86e-170">May 2</span></span>          | <span data-ttu-id="5b86e-171">-5</span><span class="sxs-lookup"><span data-stu-id="5b86e-171">-5</span></span>       | <span data-ttu-id="5b86e-172">-458,33</span><span class="sxs-lookup"><span data-stu-id="5b86e-172">-458.33</span></span>     | <span data-ttu-id="5b86e-173">-458,33</span><span class="sxs-lookup"><span data-stu-id="5b86e-173">-458.33</span></span>              |
| <span data-ttu-id="5b86e-174">Objednávka převozu</span><span class="sxs-lookup"><span data-stu-id="5b86e-174">Transfer order</span></span> | <span data-ttu-id="5b86e-175">1</span><span class="sxs-lookup"><span data-stu-id="5b86e-175">1</span></span>    | <span data-ttu-id="5b86e-176">12</span><span class="sxs-lookup"><span data-stu-id="5b86e-176">12</span></span>        | <span data-ttu-id="5b86e-177">Koupeno</span><span class="sxs-lookup"><span data-stu-id="5b86e-177">Purchased</span></span> |       | <span data-ttu-id="5b86e-178">2. květen</span><span class="sxs-lookup"><span data-stu-id="5b86e-178">May 2</span></span>         | <span data-ttu-id="5b86e-179">2. květen</span><span class="sxs-lookup"><span data-stu-id="5b86e-179">May 2</span></span>          | <span data-ttu-id="5b86e-180">5</span><span class="sxs-lookup"><span data-stu-id="5b86e-180">5</span></span>        | <span data-ttu-id="5b86e-181">458.33</span><span class="sxs-lookup"><span data-stu-id="5b86e-181">458.33</span></span>      | <span data-ttu-id="5b86e-182">458.33</span><span class="sxs-lookup"><span data-stu-id="5b86e-182">458.33</span></span>               |
| <span data-ttu-id="5b86e-183">Prodejní objednávka</span><span class="sxs-lookup"><span data-stu-id="5b86e-183">Sales order</span></span>    | <span data-ttu-id="5b86e-184">1</span><span class="sxs-lookup"><span data-stu-id="5b86e-184">1</span></span>    | <span data-ttu-id="5b86e-185">12</span><span class="sxs-lookup"><span data-stu-id="5b86e-185">12</span></span>        |           | <span data-ttu-id="5b86e-186">Prodáno</span><span class="sxs-lookup"><span data-stu-id="5b86e-186">Sold</span></span>  | <span data-ttu-id="5b86e-187">3. květen</span><span class="sxs-lookup"><span data-stu-id="5b86e-187">May 3</span></span>         | <span data-ttu-id="5b86e-188">3. květen</span><span class="sxs-lookup"><span data-stu-id="5b86e-188">May 3</span></span>          | <span data-ttu-id="5b86e-189">-1</span><span class="sxs-lookup"><span data-stu-id="5b86e-189">-1</span></span>       | <span data-ttu-id="5b86e-190">-91,67</span><span class="sxs-lookup"><span data-stu-id="5b86e-190">-91.67</span></span>      | <span data-ttu-id="5b86e-191">-91,67</span><span class="sxs-lookup"><span data-stu-id="5b86e-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="5b86e-192">Jak se vypočítává množství a částky v jednotlivých intervalech období</span><span class="sxs-lookup"><span data-stu-id="5b86e-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="5b86e-193">Pomocí ukázkových dat, která jsou popsána v předchozích částech, můžete spustit sestavu **Stárnutí zásob**, která má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="5b86e-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="5b86e-194">**K datu:** *9. května 2020*</span><span class="sxs-lookup"><span data-stu-id="5b86e-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="5b86e-195">**Pracoviště:** *Zobrazit*</span><span class="sxs-lookup"><span data-stu-id="5b86e-195">**Site:** *View*</span></span>
- <span data-ttu-id="5b86e-196">**Sklad:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="5b86e-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="5b86e-197">**Číslo položky:** *Součet*</span><span class="sxs-lookup"><span data-stu-id="5b86e-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="5b86e-198">**Doba stárnutí:** Toto pole nastavte tak, aby generovalo měsíční intervaly.</span><span class="sxs-lookup"><span data-stu-id="5b86e-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="5b86e-199">V takovém případě bude obsah vygenerované sestavy vypadat jako v následujícím příkladu.</span><span class="sxs-lookup"><span data-stu-id="5b86e-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="5b86e-200">Č. položky</span><span class="sxs-lookup"><span data-stu-id="5b86e-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="5b86e-201">Lokalita</span><span class="sxs-lookup"><span data-stu-id="5b86e-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="5b86e-202">Množství na skladě</span><span class="sxs-lookup"><span data-stu-id="5b86e-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="5b86e-203">Hodnota položek na skladě</span><span class="sxs-lookup"><span data-stu-id="5b86e-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="5b86e-204">Hodnota/množství skladových zásob</span><span class="sxs-lookup"><span data-stu-id="5b86e-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="5b86e-205">Hodnota zásob</span><span class="sxs-lookup"><span data-stu-id="5b86e-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="5b86e-206">Průměrné náklady na jednotku</span><span class="sxs-lookup"><span data-stu-id="5b86e-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="5b86e-207">5/8/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="5b86e-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="5b86e-208">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="5b86e-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="5b86e-209">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="5b86e-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="5b86e-210">P1:Množství</span><span class="sxs-lookup"><span data-stu-id="5b86e-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="5b86e-211">P1:Částka</span><span class="sxs-lookup"><span data-stu-id="5b86e-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="5b86e-212">P2:Množství</span><span class="sxs-lookup"><span data-stu-id="5b86e-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="5b86e-213">P2:Částka</span><span class="sxs-lookup"><span data-stu-id="5b86e-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="5b86e-214">P3:Množství</span><span class="sxs-lookup"><span data-stu-id="5b86e-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="5b86e-215">P3:Částka</span><span class="sxs-lookup"><span data-stu-id="5b86e-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="5b86e-216">1 000</span><span class="sxs-lookup"><span data-stu-id="5b86e-216">1000</span></span></td>
    <td><span data-ttu-id="5b86e-217">1</span><span class="sxs-lookup"><span data-stu-id="5b86e-217">1</span></span></td>
    <td><span data-ttu-id="5b86e-218">14</span><span class="sxs-lookup"><span data-stu-id="5b86e-218">14</span></span></td>
    <td><span data-ttu-id="5b86e-219">1,283.33</span><span class="sxs-lookup"><span data-stu-id="5b86e-219">1,283.33</span></span></td>
    <td><span data-ttu-id="5b86e-220">14</span><span class="sxs-lookup"><span data-stu-id="5b86e-220">14</span></span></td>
    <td><span data-ttu-id="5b86e-221">1,283.33</span><span class="sxs-lookup"><span data-stu-id="5b86e-221">1,283.33</span></span></td>
    <td><span data-ttu-id="5b86e-222">91.67</span><span class="sxs-lookup"><span data-stu-id="5b86e-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="5b86e-223">5.00</span><span class="sxs-lookup"><span data-stu-id="5b86e-223">5.00</span></span></td>
    <td><span data-ttu-id="5b86e-224">458.33</span><span class="sxs-lookup"><span data-stu-id="5b86e-224">458.33</span></span></td>
    <td><span data-ttu-id="5b86e-225">9.00</span><span class="sxs-lookup"><span data-stu-id="5b86e-225">9.00</span></span></td>
    <td><span data-ttu-id="5b86e-226">825.00</span><span class="sxs-lookup"><span data-stu-id="5b86e-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="5b86e-227">1 000</span><span class="sxs-lookup"><span data-stu-id="5b86e-227">1000</span></span></td>
    <td><span data-ttu-id="5b86e-228">2</span><span class="sxs-lookup"><span data-stu-id="5b86e-228">2</span></span></td>
    <td><span data-ttu-id="5b86e-229">10</span><span class="sxs-lookup"><span data-stu-id="5b86e-229">10</span></span></td>
    <td><span data-ttu-id="5b86e-230">2,000.00</span><span class="sxs-lookup"><span data-stu-id="5b86e-230">2,000.00</span></span></td>
    <td><span data-ttu-id="5b86e-231">10</span><span class="sxs-lookup"><span data-stu-id="5b86e-231">10</span></span></td>
    <td><span data-ttu-id="5b86e-232">2,000.00</span><span class="sxs-lookup"><span data-stu-id="5b86e-232">2,000.00</span></span></td>
    <td><span data-ttu-id="5b86e-233">200.00</span><span class="sxs-lookup"><span data-stu-id="5b86e-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="5b86e-234">10.00</span><span class="sxs-lookup"><span data-stu-id="5b86e-234">10.00</span></span></td>
    <td><span data-ttu-id="5b86e-235">2,000.00</span><span class="sxs-lookup"><span data-stu-id="5b86e-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="5b86e-236"><strong>Celkem 1000</strong></span><span class="sxs-lookup"><span data-stu-id="5b86e-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="5b86e-237"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="5b86e-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="5b86e-238"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="5b86e-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="5b86e-239"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="5b86e-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="5b86e-240"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="5b86e-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="5b86e-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="5b86e-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="5b86e-242"><strong>2,825.00</strong></span><span class="sxs-lookup"><span data-stu-id="5b86e-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="5b86e-243">V této ukázkové sestavě si všimněte následujících podrobností:</span><span class="sxs-lookup"><span data-stu-id="5b86e-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="5b86e-244">Hodnoty **Množství hodnoty zásob**, **Hodnota zásob** a **Průměrná jednotková cena** uvedené v sestavě jsou hodnoty dimenze finančních zásob (v tomto případě **Pracoviště**).</span><span class="sxs-lookup"><span data-stu-id="5b86e-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="5b86e-245">Například pro pracoviště 1 obsahuje sestava následující informace:</span><span class="sxs-lookup"><span data-stu-id="5b86e-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="5b86e-246">Hodnota **Množství hodnoty zásob** je *14* (= 10 + 5 - 5 + 5 - 1).</span><span class="sxs-lookup"><span data-stu-id="5b86e-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="5b86e-247">Hodnota **Hodnota zásob** je *1,283.33* (= 1,000 + 375 - 458.33 + 458.33 - 91.67).</span><span class="sxs-lookup"><span data-stu-id="5b86e-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="5b86e-248">Hodnota **Průměrné náklady na jednotku** je *91,67*.</span><span class="sxs-lookup"><span data-stu-id="5b86e-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="5b86e-249">Hodnota **Hodnota na skladě** a hodnota **Částka** v jednotlivých intervalech období se vypočítává pomocí hodnoty **Průměrná jednotková cena**.</span><span class="sxs-lookup"><span data-stu-id="5b86e-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="5b86e-250">Sestava určuje množství na skladě pro každý interval období sečtením celkového přijatého skladového množství pro každý interval období.</span><span class="sxs-lookup"><span data-stu-id="5b86e-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="5b86e-251">Následně použije princip FIFO (první dovnitř, první ven) k odečtení celkového vydaného množství bez ohledu na model zásob, který položky používají.</span><span class="sxs-lookup"><span data-stu-id="5b86e-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="5b86e-252">Pokud stejnou sestavu spustíte znovu, ale tentokrát nastavíte pole **Pracoviště** i **Sklad** na *Zobrazení*, bude nová sestava vypadat jako v následujícím příkladu.</span><span class="sxs-lookup"><span data-stu-id="5b86e-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="5b86e-253">Č. položky</span><span class="sxs-lookup"><span data-stu-id="5b86e-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="5b86e-254">Lokalita</span><span class="sxs-lookup"><span data-stu-id="5b86e-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="5b86e-255">Sklad</span><span class="sxs-lookup"><span data-stu-id="5b86e-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="5b86e-256">Množství na skladě</span><span class="sxs-lookup"><span data-stu-id="5b86e-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="5b86e-257">Hodnota položek na skladě</span><span class="sxs-lookup"><span data-stu-id="5b86e-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="5b86e-258">Hodnota/množství skladových zásob</span><span class="sxs-lookup"><span data-stu-id="5b86e-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="5b86e-259">Hodnota zásob</span><span class="sxs-lookup"><span data-stu-id="5b86e-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="5b86e-260">Průměrné náklady na jednotku</span><span class="sxs-lookup"><span data-stu-id="5b86e-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="5b86e-261">5/8/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="5b86e-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="5b86e-262">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="5b86e-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="5b86e-263">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="5b86e-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="5b86e-264">P1:Množství</span><span class="sxs-lookup"><span data-stu-id="5b86e-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="5b86e-265">P1:Částka</span><span class="sxs-lookup"><span data-stu-id="5b86e-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="5b86e-266">P2:Množství</span><span class="sxs-lookup"><span data-stu-id="5b86e-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="5b86e-267">P2:Částka</span><span class="sxs-lookup"><span data-stu-id="5b86e-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="5b86e-268">P3:Množství</span><span class="sxs-lookup"><span data-stu-id="5b86e-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="5b86e-269">P3:Částka</span><span class="sxs-lookup"><span data-stu-id="5b86e-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="5b86e-270">1 000</span><span class="sxs-lookup"><span data-stu-id="5b86e-270">1000</span></span></td>
    <td><span data-ttu-id="5b86e-271">1</span><span class="sxs-lookup"><span data-stu-id="5b86e-271">1</span></span></td>
    <td><span data-ttu-id="5b86e-272">11</span><span class="sxs-lookup"><span data-stu-id="5b86e-272">11</span></span></td>
    <td><span data-ttu-id="5b86e-273">10</span><span class="sxs-lookup"><span data-stu-id="5b86e-273">10</span></span></td>
    <td><span data-ttu-id="5b86e-274">916.67</span><span class="sxs-lookup"><span data-stu-id="5b86e-274">916.67</span></span></td>
    <td><span data-ttu-id="5b86e-275">14</span><span class="sxs-lookup"><span data-stu-id="5b86e-275">14</span></span></td>
    <td><span data-ttu-id="5b86e-276">1,283.33</span><span class="sxs-lookup"><span data-stu-id="5b86e-276">1,283.33</span></span></td>
    <td><span data-ttu-id="5b86e-277">91.67</span><span class="sxs-lookup"><span data-stu-id="5b86e-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="5b86e-278">5.00</span><span class="sxs-lookup"><span data-stu-id="5b86e-278">5.00</span></span></td>
    <td><span data-ttu-id="5b86e-279">458.33</span><span class="sxs-lookup"><span data-stu-id="5b86e-279">458.33</span></span></td>
    <td><span data-ttu-id="5b86e-280">5.00</span><span class="sxs-lookup"><span data-stu-id="5b86e-280">5.00</span></span></td>
    <td><span data-ttu-id="5b86e-281">458.33</span><span class="sxs-lookup"><span data-stu-id="5b86e-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="5b86e-282">1 000</span><span class="sxs-lookup"><span data-stu-id="5b86e-282">1000</span></span></td>
    <td><span data-ttu-id="5b86e-283">1</span><span class="sxs-lookup"><span data-stu-id="5b86e-283">1</span></span></td>
    <td><span data-ttu-id="5b86e-284">12</span><span class="sxs-lookup"><span data-stu-id="5b86e-284">12</span></span></td>
    <td><span data-ttu-id="5b86e-285">4</span><span class="sxs-lookup"><span data-stu-id="5b86e-285">4</span></span></td>
    <td><span data-ttu-id="5b86e-286">366.67</span><span class="sxs-lookup"><span data-stu-id="5b86e-286">366.67</span></span></td>
    <td><span data-ttu-id="5b86e-287">14</span><span class="sxs-lookup"><span data-stu-id="5b86e-287">14</span></span></td>
    <td><span data-ttu-id="5b86e-288">1,283.33</span><span class="sxs-lookup"><span data-stu-id="5b86e-288">1,283.33</span></span></td>
    <td><span data-ttu-id="5b86e-289">91.67</span><span class="sxs-lookup"><span data-stu-id="5b86e-289">91.67</span></span></td>
    <td><span data-ttu-id="5b86e-290">4.00</span><span class="sxs-lookup"><span data-stu-id="5b86e-290">4.00</span></span></td>
    <td><span data-ttu-id="5b86e-291">366.67</span><span class="sxs-lookup"><span data-stu-id="5b86e-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="5b86e-292">1 000</span><span class="sxs-lookup"><span data-stu-id="5b86e-292">1000</span></span></td>
    <td><span data-ttu-id="5b86e-293">2</span><span class="sxs-lookup"><span data-stu-id="5b86e-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="5b86e-294">10</span><span class="sxs-lookup"><span data-stu-id="5b86e-294">10</span></span></td>
    <td><span data-ttu-id="5b86e-295">2,000.00</span><span class="sxs-lookup"><span data-stu-id="5b86e-295">2,000.00</span></span></td>
    <td><span data-ttu-id="5b86e-296">10</span><span class="sxs-lookup"><span data-stu-id="5b86e-296">10</span></span></td>
    <td><span data-ttu-id="5b86e-297">2,000.00</span><span class="sxs-lookup"><span data-stu-id="5b86e-297">2,000.00</span></span></td>
    <td><span data-ttu-id="5b86e-298">200.00</span><span class="sxs-lookup"><span data-stu-id="5b86e-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="5b86e-299">10.00</span><span class="sxs-lookup"><span data-stu-id="5b86e-299">10.00</span></span></td>
    <td><span data-ttu-id="5b86e-300">2,000.00</span><span class="sxs-lookup"><span data-stu-id="5b86e-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="5b86e-301"><strong>Celkem 1000</strong></span><span class="sxs-lookup"><span data-stu-id="5b86e-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="5b86e-302"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="5b86e-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="5b86e-303"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="5b86e-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="5b86e-304"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="5b86e-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="5b86e-305"><strong>366.67</strong></span><span class="sxs-lookup"><span data-stu-id="5b86e-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="5b86e-306"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="5b86e-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="5b86e-307"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="5b86e-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="5b86e-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="5b86e-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="5b86e-309"><strong>2,458.33</strong></span><span class="sxs-lookup"><span data-stu-id="5b86e-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="5b86e-310">Tentokrát je pracoviště 1 rozděleno na dva řádky, jeden pro sklad 11 a jeden pro sklad 12.</span><span class="sxs-lookup"><span data-stu-id="5b86e-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="5b86e-311">Hodnoty **Množství hodnoty zásob**, **Hodnota zásob** a **Průměrná jednotková cena** uvedené v sestavě jsou však stejné, protože **Sklad** není dimenze finančních zásob.</span><span class="sxs-lookup"><span data-stu-id="5b86e-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="5b86e-312">Dále si všimněte, že distribuce množství na pracovišti 1 je odlišná.</span><span class="sxs-lookup"><span data-stu-id="5b86e-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="5b86e-313">V první sestavě, kterou jste spustili, systém ignoroval příkaz k převodu, ke kterému došlo na stejném pracovišti, a odečetl množství prodejní faktury z intervalu období **31. 3. 2020 - 3. 1. 2020** na pracovišti 1.</span><span class="sxs-lookup"><span data-stu-id="5b86e-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="5b86e-314">V nové sestavě však systém odečte z prodejní faktury množství z intervalu období **5. 5. 2012 - 5. 1. 2012** ve skladu 12.</span><span class="sxs-lookup"><span data-stu-id="5b86e-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="5b86e-315">Dopady uzávěrky skladu</span><span class="sxs-lookup"><span data-stu-id="5b86e-315">Effects of inventory closing</span></span>

<span data-ttu-id="5b86e-316">Pokud spustíte uzávěrku zásob na květen a poté znovu spustíte předchozí sestavu, ale nastavíte hodnotu v poli **K datu** na *31. května 2020*, všimnete si následujících výsledků:</span><span class="sxs-lookup"><span data-stu-id="5b86e-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="5b86e-317">Hodnoty **Hodnota zásob** a **Průměrné jednotkové náklady** se aktualizují.</span><span class="sxs-lookup"><span data-stu-id="5b86e-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="5b86e-318">Hodnota **Hodnota na skladě** a všechny hodnoty **Částka** v každém intervalu období se aktualizují odpovídajícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="5b86e-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="5b86e-319">Nová sestava bude vypadat podobně jako v následujícím příkladu.</span><span class="sxs-lookup"><span data-stu-id="5b86e-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="5b86e-320">Č. položky</span><span class="sxs-lookup"><span data-stu-id="5b86e-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="5b86e-321">Lokalita</span><span class="sxs-lookup"><span data-stu-id="5b86e-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="5b86e-322">Sklad</span><span class="sxs-lookup"><span data-stu-id="5b86e-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="5b86e-323">Množství na skladě</span><span class="sxs-lookup"><span data-stu-id="5b86e-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="5b86e-324">Hodnota položek na skladě</span><span class="sxs-lookup"><span data-stu-id="5b86e-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="5b86e-325">Hodnota/množství skladových zásob</span><span class="sxs-lookup"><span data-stu-id="5b86e-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="5b86e-326">Hodnota zásob</span><span class="sxs-lookup"><span data-stu-id="5b86e-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="5b86e-327">Průměrné náklady na jednotku</span><span class="sxs-lookup"><span data-stu-id="5b86e-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="5b86e-328">5/31/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="5b86e-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="5b86e-329">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="5b86e-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="5b86e-330">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="5b86e-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="5b86e-331">P1:Množství</span><span class="sxs-lookup"><span data-stu-id="5b86e-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="5b86e-332">P1:Částka</span><span class="sxs-lookup"><span data-stu-id="5b86e-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="5b86e-333">P2:Množství</span><span class="sxs-lookup"><span data-stu-id="5b86e-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="5b86e-334">P2:Částka</span><span class="sxs-lookup"><span data-stu-id="5b86e-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="5b86e-335">P3:Množství</span><span class="sxs-lookup"><span data-stu-id="5b86e-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="5b86e-336">P3:Částka</span><span class="sxs-lookup"><span data-stu-id="5b86e-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="5b86e-337">1 000</span><span class="sxs-lookup"><span data-stu-id="5b86e-337">1000</span></span></td>
    <td><span data-ttu-id="5b86e-338">1</span><span class="sxs-lookup"><span data-stu-id="5b86e-338">1</span></span></td>
    <td><span data-ttu-id="5b86e-339">11</span><span class="sxs-lookup"><span data-stu-id="5b86e-339">11</span></span></td>
    <td><span data-ttu-id="5b86e-340">10</span><span class="sxs-lookup"><span data-stu-id="5b86e-340">10</span></span></td>
    <td><span data-ttu-id="5b86e-341">910.70</span><span class="sxs-lookup"><span data-stu-id="5b86e-341">910.70</span></span></td>
    <td><span data-ttu-id="5b86e-342">14</span><span class="sxs-lookup"><span data-stu-id="5b86e-342">14</span></span></td>
    <td><span data-ttu-id="5b86e-343">1,275.00</span><span class="sxs-lookup"><span data-stu-id="5b86e-343">1,275.00</span></span></td>
    <td><span data-ttu-id="5b86e-344">91.07</span><span class="sxs-lookup"><span data-stu-id="5b86e-344">91.07</span></span></td>
    <td><span data-ttu-id="5b86e-345">0,00</span><span class="sxs-lookup"><span data-stu-id="5b86e-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="5b86e-346">5.00</span><span class="sxs-lookup"><span data-stu-id="5b86e-346">5.00</span></span></td>
    <td><span data-ttu-id="5b86e-347">455.36</span><span class="sxs-lookup"><span data-stu-id="5b86e-347">455.36</span></span></td>
    <td><span data-ttu-id="5b86e-348">5.00</span><span class="sxs-lookup"><span data-stu-id="5b86e-348">5.00</span></span></td>
    <td><span data-ttu-id="5b86e-349">455.36</span><span class="sxs-lookup"><span data-stu-id="5b86e-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="5b86e-350">1 000</span><span class="sxs-lookup"><span data-stu-id="5b86e-350">1000</span></span></td>
    <td><span data-ttu-id="5b86e-351">1</span><span class="sxs-lookup"><span data-stu-id="5b86e-351">1</span></span></td>
    <td><span data-ttu-id="5b86e-352">12</span><span class="sxs-lookup"><span data-stu-id="5b86e-352">12</span></span></td>
    <td><span data-ttu-id="5b86e-353">4</span><span class="sxs-lookup"><span data-stu-id="5b86e-353">4</span></span></td>
    <td><span data-ttu-id="5b86e-354">364.29</span><span class="sxs-lookup"><span data-stu-id="5b86e-354">364.29</span></span></td>
    <td><span data-ttu-id="5b86e-355">14</span><span class="sxs-lookup"><span data-stu-id="5b86e-355">14</span></span></td>
    <td><span data-ttu-id="5b86e-356">1,275.00</span><span class="sxs-lookup"><span data-stu-id="5b86e-356">1,275.00</span></span></td>
    <td><span data-ttu-id="5b86e-357">91.07</span><span class="sxs-lookup"><span data-stu-id="5b86e-357">91.07</span></span></td>
    <td><span data-ttu-id="5b86e-358">4.00</span><span class="sxs-lookup"><span data-stu-id="5b86e-358">4.00</span></span></td>
    <td><span data-ttu-id="5b86e-359">364.29</span><span class="sxs-lookup"><span data-stu-id="5b86e-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="5b86e-360">1 000</span><span class="sxs-lookup"><span data-stu-id="5b86e-360">1000</span></span></td>
    <td><span data-ttu-id="5b86e-361">2</span><span class="sxs-lookup"><span data-stu-id="5b86e-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="5b86e-362">10</span><span class="sxs-lookup"><span data-stu-id="5b86e-362">10</span></span></td>
    <td><span data-ttu-id="5b86e-363">2,000.00</span><span class="sxs-lookup"><span data-stu-id="5b86e-363">2,000.00</span></span></td>
    <td><span data-ttu-id="5b86e-364">10</span><span class="sxs-lookup"><span data-stu-id="5b86e-364">10</span></span></td>
    <td><span data-ttu-id="5b86e-365">2,000.00</span><span class="sxs-lookup"><span data-stu-id="5b86e-365">2,000.00</span></span></td>
    <td><span data-ttu-id="5b86e-366">200.00</span><span class="sxs-lookup"><span data-stu-id="5b86e-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="5b86e-367">10.00</span><span class="sxs-lookup"><span data-stu-id="5b86e-367">10.00</span></span></td>
    <td><span data-ttu-id="5b86e-368">2,000.00</span><span class="sxs-lookup"><span data-stu-id="5b86e-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="5b86e-369"><strong>Celkem 1000</strong></span><span class="sxs-lookup"><span data-stu-id="5b86e-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="5b86e-370"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="5b86e-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="5b86e-371"><strong>3,275.00</strong></span><span class="sxs-lookup"><span data-stu-id="5b86e-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="5b86e-372"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="5b86e-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="5b86e-373"><strong>364.29</strong></span><span class="sxs-lookup"><span data-stu-id="5b86e-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="5b86e-374"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="5b86e-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="5b86e-375"><strong>455.36</strong></span><span class="sxs-lookup"><span data-stu-id="5b86e-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="5b86e-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="5b86e-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="5b86e-377"><strong>2,455.36</strong></span><span class="sxs-lookup"><span data-stu-id="5b86e-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>
