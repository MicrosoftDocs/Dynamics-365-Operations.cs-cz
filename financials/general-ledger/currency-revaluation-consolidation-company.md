---
title: "Přecenění měny v konsolidované společnosti"
description: 
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 643af8d771685fe8fd652b353d41f2679e0bef8b
ms.contentlocale: cs-cz
ms.lasthandoff: 07/18/2017

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="5c57d-102">Přecenění měny v konsolidované společnosti</span><span class="sxs-lookup"><span data-stu-id="5c57d-102">Currency revaluation in a consolidation company</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="5c57d-103">Při konsolidaci dat z jedné zúčtovací měny na jinou musíte spustit přecenění měny, pokud dojde ke změně směnných kurzů, aby byly správně přehodnoceny zůstatky účtů.</span><span class="sxs-lookup"><span data-stu-id="5c57d-103">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="5c57d-104">Při původní konsolidaci data použijte kartu **Převod měny** k výběru počátečních směnných kurzů pro převod při procesu konsolidace.</span><span class="sxs-lookup"><span data-stu-id="5c57d-104">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="5c57d-105">Po zadání nového směnného kurzu (např. v dalším měsíci) je nutné přecenění zůstatků účtů.</span><span class="sxs-lookup"><span data-stu-id="5c57d-105">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="5c57d-106">Nerealizované zisky nebo ztráty jsou pak odpovídajícím způsobem aktualizovány na základě nového směnného kurzu a data.</span><span class="sxs-lookup"><span data-stu-id="5c57d-106">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="5c57d-107">Následující příklad znázorňuje účetní položky, které jsou vytvořeny během tohoto procesu.</span><span class="sxs-lookup"><span data-stu-id="5c57d-107">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="5c57d-108">Nastavení společnosti</span><span class="sxs-lookup"><span data-stu-id="5c57d-108">Company setup</span></span>
-   <span data-ttu-id="5c57d-109">**Zdrojová/provozní společnost (USMF)** – americké dolary (USD) se používají jako zúčtovací a vykazovací měna.</span><span class="sxs-lookup"><span data-stu-id="5c57d-109">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="5c57d-110">**Konsolidovaná společnost (CON)** – euro (EUR) se používá jako zúčtovací a vykazovací měna.</span><span class="sxs-lookup"><span data-stu-id="5c57d-110">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="5c57d-111">**Realizovaný zisk **– účet hlavní knihy 801500</span><span class="sxs-lookup"><span data-stu-id="5c57d-111">**Realized gain **– Ledger account 801500</span></span>
    -   <span data-ttu-id="5c57d-112">**Realizovaná ztráta** – účet hlavní knihy 801600</span><span class="sxs-lookup"><span data-stu-id="5c57d-112">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="5c57d-113">**Nerealizovaný zisk** – účet hlavní knihy 801600</span><span class="sxs-lookup"><span data-stu-id="5c57d-113">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="5c57d-114">**Nerealizovaná ztráta** – účet hlavní knihy 801400</span><span class="sxs-lookup"><span data-stu-id="5c57d-114">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="5c57d-115">Původní transakce</span><span class="sxs-lookup"><span data-stu-id="5c57d-115">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="5c57d-116">Transakce příjmů v hotovosti v USMF</span><span class="sxs-lookup"><span data-stu-id="5c57d-116">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="5c57d-117">Datum</span><span class="sxs-lookup"><span data-stu-id="5c57d-117">Date</span></span>       | <span data-ttu-id="5c57d-118">Účet hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="5c57d-118">Ledger account</span></span>               | <span data-ttu-id="5c57d-119">Měna</span><span class="sxs-lookup"><span data-stu-id="5c57d-119">Currency</span></span> | <span data-ttu-id="5c57d-120">Částka</span><span class="sxs-lookup"><span data-stu-id="5c57d-120">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="5c57d-121">11. 10. 2015</span><span class="sxs-lookup"><span data-stu-id="5c57d-121">10/11/2015</span></span> | <span data-ttu-id="5c57d-122">110110 – Hotovost</span><span class="sxs-lookup"><span data-stu-id="5c57d-122">110110 – Cash</span></span>                | <span data-ttu-id="5c57d-123">USD</span><span class="sxs-lookup"><span data-stu-id="5c57d-123">USD</span></span>      | <span data-ttu-id="5c57d-124">500</span><span class="sxs-lookup"><span data-stu-id="5c57d-124">500</span></span>    |
| <span data-ttu-id="5c57d-125">11. 10. 2015</span><span class="sxs-lookup"><span data-stu-id="5c57d-125">10/11/2015</span></span> | <span data-ttu-id="5c57d-126">130100 – Pohledávky</span><span class="sxs-lookup"><span data-stu-id="5c57d-126">130100 – Accounts Receivable</span></span> | <span data-ttu-id="5c57d-127">USD</span><span class="sxs-lookup"><span data-stu-id="5c57d-127">USD</span></span>      | <span data-ttu-id="5c57d-128">-500</span><span class="sxs-lookup"><span data-stu-id="5c57d-128">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="5c57d-129">Směnné kurzy</span><span class="sxs-lookup"><span data-stu-id="5c57d-129">Exchange rates</span></span>
| <span data-ttu-id="5c57d-130">Z měny</span><span class="sxs-lookup"><span data-stu-id="5c57d-130">From currency</span></span> | <span data-ttu-id="5c57d-131">Do měny</span><span class="sxs-lookup"><span data-stu-id="5c57d-131">To currency</span></span> | <span data-ttu-id="5c57d-132">Počáteční datum</span><span class="sxs-lookup"><span data-stu-id="5c57d-132">Start date</span></span> | <span data-ttu-id="5c57d-133">Směnný kurz</span><span class="sxs-lookup"><span data-stu-id="5c57d-133">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="5c57d-134">EUR</span><span class="sxs-lookup"><span data-stu-id="5c57d-134">EUR</span></span>           | <span data-ttu-id="5c57d-135">USD</span><span class="sxs-lookup"><span data-stu-id="5c57d-135">USD</span></span>         | <span data-ttu-id="5c57d-136">1. 10. 2015</span><span class="sxs-lookup"><span data-stu-id="5c57d-136">10/1/2015</span></span>  | <span data-ttu-id="5c57d-137">200</span><span class="sxs-lookup"><span data-stu-id="5c57d-137">200</span></span>           |
| <span data-ttu-id="5c57d-138">EUR</span><span class="sxs-lookup"><span data-stu-id="5c57d-138">EUR</span></span>           | <span data-ttu-id="5c57d-139">USD</span><span class="sxs-lookup"><span data-stu-id="5c57d-139">USD</span></span>         | <span data-ttu-id="5c57d-140">1. 11. 2015</span><span class="sxs-lookup"><span data-stu-id="5c57d-140">11/1/2015</span></span>  | <span data-ttu-id="5c57d-141">150</span><span class="sxs-lookup"><span data-stu-id="5c57d-141">150</span></span>           |
| <span data-ttu-id="5c57d-142">EUR</span><span class="sxs-lookup"><span data-stu-id="5c57d-142">EUR</span></span>           | <span data-ttu-id="5c57d-143">USD</span><span class="sxs-lookup"><span data-stu-id="5c57d-143">USD</span></span>         | <span data-ttu-id="5c57d-144">1. 12. 2012</span><span class="sxs-lookup"><span data-stu-id="5c57d-144">12/1/2012</span></span>  | <span data-ttu-id="5c57d-145">100</span><span class="sxs-lookup"><span data-stu-id="5c57d-145">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="5c57d-146">Provedení konsolidace pro říjen roku 2015</span><span class="sxs-lookup"><span data-stu-id="5c57d-146">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="5c57d-147">Zůstatky v konsolidované společnosti</span><span class="sxs-lookup"><span data-stu-id="5c57d-147">Balances in the consolidation company</span></span>

| <span data-ttu-id="5c57d-148">Účet hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="5c57d-148">Ledger account</span></span> | <span data-ttu-id="5c57d-149">Měna</span><span class="sxs-lookup"><span data-stu-id="5c57d-149">Currency</span></span> | <span data-ttu-id="5c57d-150">Částka</span><span class="sxs-lookup"><span data-stu-id="5c57d-150">Amount</span></span> | <span data-ttu-id="5c57d-151">Výpočet</span><span class="sxs-lookup"><span data-stu-id="5c57d-151">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="5c57d-152">110110</span><span class="sxs-lookup"><span data-stu-id="5c57d-152">110110</span></span>         | <span data-ttu-id="5c57d-153">EUR</span><span class="sxs-lookup"><span data-stu-id="5c57d-153">EUR</span></span>      | <span data-ttu-id="5c57d-154">250</span><span class="sxs-lookup"><span data-stu-id="5c57d-154">250</span></span>    | <span data-ttu-id="5c57d-155">500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="5c57d-155">500 USD × 50%</span></span>  |
| <span data-ttu-id="5c57d-156">130100</span><span class="sxs-lookup"><span data-stu-id="5c57d-156">130100</span></span>         | <span data-ttu-id="5c57d-157">EUR</span><span class="sxs-lookup"><span data-stu-id="5c57d-157">EUR</span></span>      | <span data-ttu-id="5c57d-158">-250</span><span class="sxs-lookup"><span data-stu-id="5c57d-158">-250</span></span>   | <span data-ttu-id="5c57d-159">-500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="5c57d-159">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="5c57d-160">Provedení přecenění měny pro účty od 1. října 2015 do 30. listopadu 2015</span><span class="sxs-lookup"><span data-stu-id="5c57d-160">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="5c57d-161">Zůstatky v konsolidované společnosti</span><span class="sxs-lookup"><span data-stu-id="5c57d-161">Balances in the consolidation company</span></span>

| <span data-ttu-id="5c57d-162">Účet hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="5c57d-162">Ledger account</span></span> | <span data-ttu-id="5c57d-163">Měna</span><span class="sxs-lookup"><span data-stu-id="5c57d-163">Currency</span></span> | <span data-ttu-id="5c57d-164">Částka</span><span class="sxs-lookup"><span data-stu-id="5c57d-164">Amount</span></span>  | <span data-ttu-id="5c57d-165">Výpočet</span><span class="sxs-lookup"><span data-stu-id="5c57d-165">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="5c57d-166">110110</span><span class="sxs-lookup"><span data-stu-id="5c57d-166">110110</span></span>         | <span data-ttu-id="5c57d-167">EUR</span><span class="sxs-lookup"><span data-stu-id="5c57d-167">EUR</span></span>      | <span data-ttu-id="5c57d-168">333,33</span><span class="sxs-lookup"><span data-stu-id="5c57d-168">333.33</span></span>  | <span data-ttu-id="5c57d-169">Původní částka 500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="5c57d-169">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="5c57d-170">130100</span><span class="sxs-lookup"><span data-stu-id="5c57d-170">130100</span></span>         | <span data-ttu-id="5c57d-171">EUR</span><span class="sxs-lookup"><span data-stu-id="5c57d-171">EUR</span></span>      | <span data-ttu-id="5c57d-172">-333,33</span><span class="sxs-lookup"><span data-stu-id="5c57d-172">-333.33</span></span> | <span data-ttu-id="5c57d-173">Původní částka -500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="5c57d-173">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="5c57d-174">801400</span><span class="sxs-lookup"><span data-stu-id="5c57d-174">801400</span></span>         | <span data-ttu-id="5c57d-175">EUR</span><span class="sxs-lookup"><span data-stu-id="5c57d-175">EUR</span></span>      | <span data-ttu-id="5c57d-176">83,33</span><span class="sxs-lookup"><span data-stu-id="5c57d-176">83.33</span></span>   | <span data-ttu-id="5c57d-177">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="5c57d-177">333.33 – 250</span></span>                       |
| <span data-ttu-id="5c57d-178">801600</span><span class="sxs-lookup"><span data-stu-id="5c57d-178">801600</span></span>         | <span data-ttu-id="5c57d-179">EUR</span><span class="sxs-lookup"><span data-stu-id="5c57d-179">EUR</span></span>      | <span data-ttu-id="5c57d-180">-83,33</span><span class="sxs-lookup"><span data-stu-id="5c57d-180">-83.33</span></span>  | <span data-ttu-id="5c57d-181">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="5c57d-181">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="5c57d-182">Zobrazí se další transakce pro částky v měně vykazování.</span><span class="sxs-lookup"><span data-stu-id="5c57d-182">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="5c57d-183">Provedení přecenění měny pro účty od 1. října 2015 do 31. prosince 2015</span><span class="sxs-lookup"><span data-stu-id="5c57d-183">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="5c57d-184">Zůstatky v konsolidované společnosti</span><span class="sxs-lookup"><span data-stu-id="5c57d-184">Balances in the consolidation company</span></span>

| <span data-ttu-id="5c57d-185">Účet hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="5c57d-185">Ledger account</span></span> | <span data-ttu-id="5c57d-186">Měna</span><span class="sxs-lookup"><span data-stu-id="5c57d-186">Currency</span></span> | <span data-ttu-id="5c57d-187">Částka</span><span class="sxs-lookup"><span data-stu-id="5c57d-187">Amount</span></span>  | <span data-ttu-id="5c57d-188">Výpočet</span><span class="sxs-lookup"><span data-stu-id="5c57d-188">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="5c57d-189">110110</span><span class="sxs-lookup"><span data-stu-id="5c57d-189">110110</span></span>         | <span data-ttu-id="5c57d-190">EUR</span><span class="sxs-lookup"><span data-stu-id="5c57d-190">EUR</span></span>      | <span data-ttu-id="5c57d-191">500,00</span><span class="sxs-lookup"><span data-stu-id="5c57d-191">500.00</span></span>  | <span data-ttu-id="5c57d-192">Původní částka 500 × 1</span><span class="sxs-lookup"><span data-stu-id="5c57d-192">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="5c57d-193">130100</span><span class="sxs-lookup"><span data-stu-id="5c57d-193">130100</span></span>         | <span data-ttu-id="5c57d-194">EUR</span><span class="sxs-lookup"><span data-stu-id="5c57d-194">EUR</span></span>      | <span data-ttu-id="5c57d-195">-500,00</span><span class="sxs-lookup"><span data-stu-id="5c57d-195">-500.00</span></span> | <span data-ttu-id="5c57d-196">Původní částka -500 × 1</span><span class="sxs-lookup"><span data-stu-id="5c57d-196">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="5c57d-197">801400</span><span class="sxs-lookup"><span data-stu-id="5c57d-197">801400</span></span>         | <span data-ttu-id="5c57d-198">EUR</span><span class="sxs-lookup"><span data-stu-id="5c57d-198">EUR</span></span>      | <span data-ttu-id="5c57d-199">250</span><span class="sxs-lookup"><span data-stu-id="5c57d-199">250</span></span>     | <span data-ttu-id="5c57d-200">500 – 333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="5c57d-200">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="5c57d-201">801600</span><span class="sxs-lookup"><span data-stu-id="5c57d-201">801600</span></span>         | <span data-ttu-id="5c57d-202">EUR</span><span class="sxs-lookup"><span data-stu-id="5c57d-202">EUR</span></span>      | <span data-ttu-id="5c57d-203">-250</span><span class="sxs-lookup"><span data-stu-id="5c57d-203">-250</span></span>    | <span data-ttu-id="5c57d-204">-500 – (-333,33) = -166,67 -166,67 + (-83,33) = -250</span><span class="sxs-lookup"><span data-stu-id="5c57d-204">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






