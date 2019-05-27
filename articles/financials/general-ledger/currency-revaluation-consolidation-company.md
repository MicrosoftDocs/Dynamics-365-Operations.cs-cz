---
title: Přecenění měny v konsolidační společnosti
description: Toto téma popisuje, jak přecenit měnu v konsolidační společnosti.
author: ShylaThompson
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76290564037ab6f5c7a1cd4508a819bd603e8148
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567276"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="27f40-103">Přecenění měny v konsolidační společnosti</span><span class="sxs-lookup"><span data-stu-id="27f40-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27f40-104">Při konsolidaci dat z jedné zúčtovací měny na jinou musíte spustit přecenění měny, pokud dojde ke změně směnných kurzů, aby byly správně přehodnoceny zůstatky účtů.</span><span class="sxs-lookup"><span data-stu-id="27f40-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="27f40-105">Při původní konsolidaci data použijte kartu **Převod měny** k výběru počátečních směnných kurzů pro převod při procesu konsolidace.</span><span class="sxs-lookup"><span data-stu-id="27f40-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="27f40-106">Po zadání nového směnného kurzu (např. v dalším měsíci) je nutné přecenění zůstatků účtů.</span><span class="sxs-lookup"><span data-stu-id="27f40-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="27f40-107">Nerealizované zisky nebo ztráty jsou pak odpovídajícím způsobem aktualizovány na základě nového směnného kurzu a data.</span><span class="sxs-lookup"><span data-stu-id="27f40-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="27f40-108">Následující příklad znázorňuje účetní položky, které jsou vytvořeny během tohoto procesu.</span><span class="sxs-lookup"><span data-stu-id="27f40-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="27f40-109">Nastavení společnosti</span><span class="sxs-lookup"><span data-stu-id="27f40-109">Company setup</span></span>
-   <span data-ttu-id="27f40-110">**Zdrojová/provozní společnost (USMF)** – americké dolary (USD) se používají jako zúčtovací a vykazovací měna.</span><span class="sxs-lookup"><span data-stu-id="27f40-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="27f40-111">**Konsolidovaná společnost (CON)** – euro (EUR) se používá jako zúčtovací a vykazovací měna.</span><span class="sxs-lookup"><span data-stu-id="27f40-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="27f40-112">**Realizovaný zisk** – účet hlavní knihy 801500</span><span class="sxs-lookup"><span data-stu-id="27f40-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="27f40-113">**Realizovaná ztráta** – účet hlavní knihy 801600</span><span class="sxs-lookup"><span data-stu-id="27f40-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="27f40-114">**Nerealizovaný zisk** – účet hlavní knihy 801600</span><span class="sxs-lookup"><span data-stu-id="27f40-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="27f40-115">**Nerealizovaná ztráta** – účet hlavní knihy 801400</span><span class="sxs-lookup"><span data-stu-id="27f40-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="27f40-116">Původní transakce</span><span class="sxs-lookup"><span data-stu-id="27f40-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="27f40-117">Transakce příjmů v hotovosti v USMF</span><span class="sxs-lookup"><span data-stu-id="27f40-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="27f40-118">Datum</span><span class="sxs-lookup"><span data-stu-id="27f40-118">Date</span></span>       | <span data-ttu-id="27f40-119">Účet hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="27f40-119">Ledger account</span></span>               | <span data-ttu-id="27f40-120">Měna</span><span class="sxs-lookup"><span data-stu-id="27f40-120">Currency</span></span> | <span data-ttu-id="27f40-121">Částka</span><span class="sxs-lookup"><span data-stu-id="27f40-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="27f40-122">11. 10. 2015</span><span class="sxs-lookup"><span data-stu-id="27f40-122">10/11/2015</span></span> | <span data-ttu-id="27f40-123">110110 – Hotovost</span><span class="sxs-lookup"><span data-stu-id="27f40-123">110110 – Cash</span></span>                | <span data-ttu-id="27f40-124">USD</span><span class="sxs-lookup"><span data-stu-id="27f40-124">USD</span></span>      | <span data-ttu-id="27f40-125">500</span><span class="sxs-lookup"><span data-stu-id="27f40-125">500</span></span>    |
| <span data-ttu-id="27f40-126">11. 10. 2015</span><span class="sxs-lookup"><span data-stu-id="27f40-126">10/11/2015</span></span> | <span data-ttu-id="27f40-127">130100 – Pohledávky</span><span class="sxs-lookup"><span data-stu-id="27f40-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="27f40-128">USD</span><span class="sxs-lookup"><span data-stu-id="27f40-128">USD</span></span>      | <span data-ttu-id="27f40-129">-500</span><span class="sxs-lookup"><span data-stu-id="27f40-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="27f40-130">Směnné kurzy</span><span class="sxs-lookup"><span data-stu-id="27f40-130">Exchange rates</span></span>

| <span data-ttu-id="27f40-131">Z měny</span><span class="sxs-lookup"><span data-stu-id="27f40-131">From currency</span></span> | <span data-ttu-id="27f40-132">Do měny</span><span class="sxs-lookup"><span data-stu-id="27f40-132">To currency</span></span> | <span data-ttu-id="27f40-133">Počáteční datum</span><span class="sxs-lookup"><span data-stu-id="27f40-133">Start date</span></span> | <span data-ttu-id="27f40-134">Směnný kurz</span><span class="sxs-lookup"><span data-stu-id="27f40-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="27f40-135">EUR</span><span class="sxs-lookup"><span data-stu-id="27f40-135">EUR</span></span>           | <span data-ttu-id="27f40-136">USD</span><span class="sxs-lookup"><span data-stu-id="27f40-136">USD</span></span>         | <span data-ttu-id="27f40-137">1. 10. 2015</span><span class="sxs-lookup"><span data-stu-id="27f40-137">10/1/2015</span></span>  | <span data-ttu-id="27f40-138">200</span><span class="sxs-lookup"><span data-stu-id="27f40-138">200</span></span>           |
| <span data-ttu-id="27f40-139">EUR</span><span class="sxs-lookup"><span data-stu-id="27f40-139">EUR</span></span>           | <span data-ttu-id="27f40-140">USD</span><span class="sxs-lookup"><span data-stu-id="27f40-140">USD</span></span>         | <span data-ttu-id="27f40-141">1. 11. 2015</span><span class="sxs-lookup"><span data-stu-id="27f40-141">11/1/2015</span></span>  | <span data-ttu-id="27f40-142">150</span><span class="sxs-lookup"><span data-stu-id="27f40-142">150</span></span>           |
| <span data-ttu-id="27f40-143">EUR</span><span class="sxs-lookup"><span data-stu-id="27f40-143">EUR</span></span>           | <span data-ttu-id="27f40-144">USD</span><span class="sxs-lookup"><span data-stu-id="27f40-144">USD</span></span>         | <span data-ttu-id="27f40-145">1. 12. 2012</span><span class="sxs-lookup"><span data-stu-id="27f40-145">12/1/2012</span></span>  | <span data-ttu-id="27f40-146">100</span><span class="sxs-lookup"><span data-stu-id="27f40-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="27f40-147">Provedení konsolidace pro říjen roku 2015</span><span class="sxs-lookup"><span data-stu-id="27f40-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="27f40-148">Zůstatky v konsolidované společnosti</span><span class="sxs-lookup"><span data-stu-id="27f40-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="27f40-149">Účet hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="27f40-149">Ledger account</span></span> | <span data-ttu-id="27f40-150">Měna</span><span class="sxs-lookup"><span data-stu-id="27f40-150">Currency</span></span> | <span data-ttu-id="27f40-151">Částka</span><span class="sxs-lookup"><span data-stu-id="27f40-151">Amount</span></span> | <span data-ttu-id="27f40-152">Výpočet</span><span class="sxs-lookup"><span data-stu-id="27f40-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="27f40-153">110110</span><span class="sxs-lookup"><span data-stu-id="27f40-153">110110</span></span>         | <span data-ttu-id="27f40-154">EUR</span><span class="sxs-lookup"><span data-stu-id="27f40-154">EUR</span></span>      | <span data-ttu-id="27f40-155">250</span><span class="sxs-lookup"><span data-stu-id="27f40-155">250</span></span>    | <span data-ttu-id="27f40-156">500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="27f40-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="27f40-157">130100</span><span class="sxs-lookup"><span data-stu-id="27f40-157">130100</span></span>         | <span data-ttu-id="27f40-158">EUR</span><span class="sxs-lookup"><span data-stu-id="27f40-158">EUR</span></span>      | <span data-ttu-id="27f40-159">-250</span><span class="sxs-lookup"><span data-stu-id="27f40-159">-250</span></span>   | <span data-ttu-id="27f40-160">-500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="27f40-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="27f40-161">Provedení přecenění měny pro účty od 1. října 2015 do 30. listopadu 2015</span><span class="sxs-lookup"><span data-stu-id="27f40-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="27f40-162">Zůstatky v konsolidované společnosti</span><span class="sxs-lookup"><span data-stu-id="27f40-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="27f40-163">Účet hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="27f40-163">Ledger account</span></span> | <span data-ttu-id="27f40-164">Měna</span><span class="sxs-lookup"><span data-stu-id="27f40-164">Currency</span></span> | <span data-ttu-id="27f40-165">Částka</span><span class="sxs-lookup"><span data-stu-id="27f40-165">Amount</span></span>  | <span data-ttu-id="27f40-166">Výpočet</span><span class="sxs-lookup"><span data-stu-id="27f40-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="27f40-167">110110</span><span class="sxs-lookup"><span data-stu-id="27f40-167">110110</span></span>         | <span data-ttu-id="27f40-168">EUR</span><span class="sxs-lookup"><span data-stu-id="27f40-168">EUR</span></span>      | <span data-ttu-id="27f40-169">333,33</span><span class="sxs-lookup"><span data-stu-id="27f40-169">333.33</span></span>  | <span data-ttu-id="27f40-170">Původní částka 500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="27f40-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="27f40-171">130100</span><span class="sxs-lookup"><span data-stu-id="27f40-171">130100</span></span>         | <span data-ttu-id="27f40-172">EUR</span><span class="sxs-lookup"><span data-stu-id="27f40-172">EUR</span></span>      | <span data-ttu-id="27f40-173">-333,33</span><span class="sxs-lookup"><span data-stu-id="27f40-173">-333.33</span></span> | <span data-ttu-id="27f40-174">Původní částka -500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="27f40-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="27f40-175">801400</span><span class="sxs-lookup"><span data-stu-id="27f40-175">801400</span></span>         | <span data-ttu-id="27f40-176">EUR</span><span class="sxs-lookup"><span data-stu-id="27f40-176">EUR</span></span>      | <span data-ttu-id="27f40-177">83,33</span><span class="sxs-lookup"><span data-stu-id="27f40-177">83.33</span></span>   | <span data-ttu-id="27f40-178">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="27f40-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="27f40-179">801600</span><span class="sxs-lookup"><span data-stu-id="27f40-179">801600</span></span>         | <span data-ttu-id="27f40-180">EUR</span><span class="sxs-lookup"><span data-stu-id="27f40-180">EUR</span></span>      | <span data-ttu-id="27f40-181">-83,33</span><span class="sxs-lookup"><span data-stu-id="27f40-181">-83.33</span></span>  | <span data-ttu-id="27f40-182">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="27f40-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="27f40-183">Zobrazí se další transakce pro částky v měně vykazování.</span><span class="sxs-lookup"><span data-stu-id="27f40-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="27f40-184">Provedení přecenění měny pro účty od 1. října 2015 do 31. prosince 2015</span><span class="sxs-lookup"><span data-stu-id="27f40-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="27f40-185">Zůstatky v konsolidované společnosti</span><span class="sxs-lookup"><span data-stu-id="27f40-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="27f40-186">Účet hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="27f40-186">Ledger account</span></span> | <span data-ttu-id="27f40-187">Měna</span><span class="sxs-lookup"><span data-stu-id="27f40-187">Currency</span></span> | <span data-ttu-id="27f40-188">Částka</span><span class="sxs-lookup"><span data-stu-id="27f40-188">Amount</span></span>  | <span data-ttu-id="27f40-189">Výpočet</span><span class="sxs-lookup"><span data-stu-id="27f40-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="27f40-190">110110</span><span class="sxs-lookup"><span data-stu-id="27f40-190">110110</span></span>         | <span data-ttu-id="27f40-191">EUR</span><span class="sxs-lookup"><span data-stu-id="27f40-191">EUR</span></span>      | <span data-ttu-id="27f40-192">500,00</span><span class="sxs-lookup"><span data-stu-id="27f40-192">500.00</span></span>  | <span data-ttu-id="27f40-193">Původní částka 500 × 1</span><span class="sxs-lookup"><span data-stu-id="27f40-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="27f40-194">130100</span><span class="sxs-lookup"><span data-stu-id="27f40-194">130100</span></span>         | <span data-ttu-id="27f40-195">EUR</span><span class="sxs-lookup"><span data-stu-id="27f40-195">EUR</span></span>      | <span data-ttu-id="27f40-196">-500,00</span><span class="sxs-lookup"><span data-stu-id="27f40-196">-500.00</span></span> | <span data-ttu-id="27f40-197">Původní částka -500 × 1</span><span class="sxs-lookup"><span data-stu-id="27f40-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="27f40-198">801400</span><span class="sxs-lookup"><span data-stu-id="27f40-198">801400</span></span>         | <span data-ttu-id="27f40-199">EUR</span><span class="sxs-lookup"><span data-stu-id="27f40-199">EUR</span></span>      | <span data-ttu-id="27f40-200">250</span><span class="sxs-lookup"><span data-stu-id="27f40-200">250</span></span>     | <span data-ttu-id="27f40-201">500 – 333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="27f40-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="27f40-202">801600</span><span class="sxs-lookup"><span data-stu-id="27f40-202">801600</span></span>         | <span data-ttu-id="27f40-203">EUR</span><span class="sxs-lookup"><span data-stu-id="27f40-203">EUR</span></span>      | <span data-ttu-id="27f40-204">-250</span><span class="sxs-lookup"><span data-stu-id="27f40-204">-250</span></span>    | <span data-ttu-id="27f40-205">-500 – (-333,33) = -166,67 -166,67 + (-83,33) = -250</span><span class="sxs-lookup"><span data-stu-id="27f40-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |





