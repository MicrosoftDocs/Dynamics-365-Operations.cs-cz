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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b7f0a18910cbaed382971e47eb688c075e7e6a5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176751"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="1125f-103">Přecenění měny v konsolidační společnosti</span><span class="sxs-lookup"><span data-stu-id="1125f-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1125f-104">Při konsolidaci dat z jedné zúčtovací měny na jinou musíte spustit přecenění měny, pokud dojde ke změně směnných kurzů, aby byly správně přehodnoceny zůstatky účtů.</span><span class="sxs-lookup"><span data-stu-id="1125f-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="1125f-105">Při původní konsolidaci data použijte kartu **Převod měny** k výběru počátečních směnných kurzů pro převod při procesu konsolidace.</span><span class="sxs-lookup"><span data-stu-id="1125f-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="1125f-106">Po zadání nového směnného kurzu (např. v dalším měsíci) je nutné přecenění zůstatků účtů.</span><span class="sxs-lookup"><span data-stu-id="1125f-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="1125f-107">Nerealizované zisky nebo ztráty jsou pak odpovídajícím způsobem aktualizovány na základě nového směnného kurzu a data.</span><span class="sxs-lookup"><span data-stu-id="1125f-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="1125f-108">Následující příklad znázorňuje účetní položky, které jsou vytvořeny během tohoto procesu.</span><span class="sxs-lookup"><span data-stu-id="1125f-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="1125f-109">Nastavení společnosti</span><span class="sxs-lookup"><span data-stu-id="1125f-109">Company setup</span></span>
-   <span data-ttu-id="1125f-110">**Zdrojová/provozní společnost (USMF)** – americké dolary (USD) se používají jako zúčtovací a vykazovací měna.</span><span class="sxs-lookup"><span data-stu-id="1125f-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="1125f-111">**Konsolidovaná společnost (CON)** – euro (EUR) se používá jako zúčtovací a vykazovací měna.</span><span class="sxs-lookup"><span data-stu-id="1125f-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="1125f-112">**Realizovaný zisk** – účet hlavní knihy 801500</span><span class="sxs-lookup"><span data-stu-id="1125f-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="1125f-113">**Realizovaná ztráta** – účet hlavní knihy 801600</span><span class="sxs-lookup"><span data-stu-id="1125f-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="1125f-114">**Nerealizovaný zisk** – účet hlavní knihy 801600</span><span class="sxs-lookup"><span data-stu-id="1125f-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="1125f-115">**Nerealizovaná ztráta** – účet hlavní knihy 801400</span><span class="sxs-lookup"><span data-stu-id="1125f-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="1125f-116">Původní transakce</span><span class="sxs-lookup"><span data-stu-id="1125f-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="1125f-117">Transakce příjmů v hotovosti v USMF</span><span class="sxs-lookup"><span data-stu-id="1125f-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="1125f-118">Datum</span><span class="sxs-lookup"><span data-stu-id="1125f-118">Date</span></span>       | <span data-ttu-id="1125f-119">Účet hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="1125f-119">Ledger account</span></span>               | <span data-ttu-id="1125f-120">Měna</span><span class="sxs-lookup"><span data-stu-id="1125f-120">Currency</span></span> | <span data-ttu-id="1125f-121">Částka</span><span class="sxs-lookup"><span data-stu-id="1125f-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="1125f-122">11. 10. 2015</span><span class="sxs-lookup"><span data-stu-id="1125f-122">10/11/2015</span></span> | <span data-ttu-id="1125f-123">110110 – Hotovost</span><span class="sxs-lookup"><span data-stu-id="1125f-123">110110 – Cash</span></span>                | <span data-ttu-id="1125f-124">USD</span><span class="sxs-lookup"><span data-stu-id="1125f-124">USD</span></span>      | <span data-ttu-id="1125f-125">500</span><span class="sxs-lookup"><span data-stu-id="1125f-125">500</span></span>    |
| <span data-ttu-id="1125f-126">11. 10. 2015</span><span class="sxs-lookup"><span data-stu-id="1125f-126">10/11/2015</span></span> | <span data-ttu-id="1125f-127">130100 – Pohledávky</span><span class="sxs-lookup"><span data-stu-id="1125f-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="1125f-128">USD</span><span class="sxs-lookup"><span data-stu-id="1125f-128">USD</span></span>      | <span data-ttu-id="1125f-129">-500</span><span class="sxs-lookup"><span data-stu-id="1125f-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="1125f-130">Směnné kurzy</span><span class="sxs-lookup"><span data-stu-id="1125f-130">Exchange rates</span></span>

| <span data-ttu-id="1125f-131">Z měny</span><span class="sxs-lookup"><span data-stu-id="1125f-131">From currency</span></span> | <span data-ttu-id="1125f-132">Do měny</span><span class="sxs-lookup"><span data-stu-id="1125f-132">To currency</span></span> | <span data-ttu-id="1125f-133">Počáteční datum</span><span class="sxs-lookup"><span data-stu-id="1125f-133">Start date</span></span> | <span data-ttu-id="1125f-134">Směnný kurz</span><span class="sxs-lookup"><span data-stu-id="1125f-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="1125f-135">EUR</span><span class="sxs-lookup"><span data-stu-id="1125f-135">EUR</span></span>           | <span data-ttu-id="1125f-136">USD</span><span class="sxs-lookup"><span data-stu-id="1125f-136">USD</span></span>         | <span data-ttu-id="1125f-137">1. 10. 2015</span><span class="sxs-lookup"><span data-stu-id="1125f-137">10/1/2015</span></span>  | <span data-ttu-id="1125f-138">200</span><span class="sxs-lookup"><span data-stu-id="1125f-138">200</span></span>           |
| <span data-ttu-id="1125f-139">EUR</span><span class="sxs-lookup"><span data-stu-id="1125f-139">EUR</span></span>           | <span data-ttu-id="1125f-140">USD</span><span class="sxs-lookup"><span data-stu-id="1125f-140">USD</span></span>         | <span data-ttu-id="1125f-141">1. 11. 2015</span><span class="sxs-lookup"><span data-stu-id="1125f-141">11/1/2015</span></span>  | <span data-ttu-id="1125f-142">150</span><span class="sxs-lookup"><span data-stu-id="1125f-142">150</span></span>           |
| <span data-ttu-id="1125f-143">EUR</span><span class="sxs-lookup"><span data-stu-id="1125f-143">EUR</span></span>           | <span data-ttu-id="1125f-144">USD</span><span class="sxs-lookup"><span data-stu-id="1125f-144">USD</span></span>         | <span data-ttu-id="1125f-145">1. 12. 2012</span><span class="sxs-lookup"><span data-stu-id="1125f-145">12/1/2012</span></span>  | <span data-ttu-id="1125f-146">100</span><span class="sxs-lookup"><span data-stu-id="1125f-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="1125f-147">Provedení konsolidace pro říjen roku 2015</span><span class="sxs-lookup"><span data-stu-id="1125f-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="1125f-148">Zůstatky v konsolidované společnosti</span><span class="sxs-lookup"><span data-stu-id="1125f-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="1125f-149">Účet hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="1125f-149">Ledger account</span></span> | <span data-ttu-id="1125f-150">Měna</span><span class="sxs-lookup"><span data-stu-id="1125f-150">Currency</span></span> | <span data-ttu-id="1125f-151">Částka</span><span class="sxs-lookup"><span data-stu-id="1125f-151">Amount</span></span> | <span data-ttu-id="1125f-152">Výpočet</span><span class="sxs-lookup"><span data-stu-id="1125f-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="1125f-153">110110</span><span class="sxs-lookup"><span data-stu-id="1125f-153">110110</span></span>         | <span data-ttu-id="1125f-154">EUR</span><span class="sxs-lookup"><span data-stu-id="1125f-154">EUR</span></span>      | <span data-ttu-id="1125f-155">250</span><span class="sxs-lookup"><span data-stu-id="1125f-155">250</span></span>    | <span data-ttu-id="1125f-156">500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="1125f-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="1125f-157">130100</span><span class="sxs-lookup"><span data-stu-id="1125f-157">130100</span></span>         | <span data-ttu-id="1125f-158">EUR</span><span class="sxs-lookup"><span data-stu-id="1125f-158">EUR</span></span>      | <span data-ttu-id="1125f-159">-250</span><span class="sxs-lookup"><span data-stu-id="1125f-159">-250</span></span>   | <span data-ttu-id="1125f-160">-500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="1125f-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="1125f-161">Provedení přecenění měny pro účty od 1. října 2015 do 30. listopadu 2015</span><span class="sxs-lookup"><span data-stu-id="1125f-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="1125f-162">Zůstatky v konsolidované společnosti</span><span class="sxs-lookup"><span data-stu-id="1125f-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="1125f-163">Účet hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="1125f-163">Ledger account</span></span> | <span data-ttu-id="1125f-164">Měna</span><span class="sxs-lookup"><span data-stu-id="1125f-164">Currency</span></span> | <span data-ttu-id="1125f-165">Částka</span><span class="sxs-lookup"><span data-stu-id="1125f-165">Amount</span></span>  | <span data-ttu-id="1125f-166">Výpočet</span><span class="sxs-lookup"><span data-stu-id="1125f-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="1125f-167">110110</span><span class="sxs-lookup"><span data-stu-id="1125f-167">110110</span></span>         | <span data-ttu-id="1125f-168">EUR</span><span class="sxs-lookup"><span data-stu-id="1125f-168">EUR</span></span>      | <span data-ttu-id="1125f-169">333,33</span><span class="sxs-lookup"><span data-stu-id="1125f-169">333.33</span></span>  | <span data-ttu-id="1125f-170">Původní částka 500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="1125f-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="1125f-171">130100</span><span class="sxs-lookup"><span data-stu-id="1125f-171">130100</span></span>         | <span data-ttu-id="1125f-172">EUR</span><span class="sxs-lookup"><span data-stu-id="1125f-172">EUR</span></span>      | <span data-ttu-id="1125f-173">-333,33</span><span class="sxs-lookup"><span data-stu-id="1125f-173">-333.33</span></span> | <span data-ttu-id="1125f-174">Původní částka -500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="1125f-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="1125f-175">801400</span><span class="sxs-lookup"><span data-stu-id="1125f-175">801400</span></span>         | <span data-ttu-id="1125f-176">EUR</span><span class="sxs-lookup"><span data-stu-id="1125f-176">EUR</span></span>      | <span data-ttu-id="1125f-177">83,33</span><span class="sxs-lookup"><span data-stu-id="1125f-177">83.33</span></span>   | <span data-ttu-id="1125f-178">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="1125f-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="1125f-179">801600</span><span class="sxs-lookup"><span data-stu-id="1125f-179">801600</span></span>         | <span data-ttu-id="1125f-180">EUR</span><span class="sxs-lookup"><span data-stu-id="1125f-180">EUR</span></span>      | <span data-ttu-id="1125f-181">-83,33</span><span class="sxs-lookup"><span data-stu-id="1125f-181">-83.33</span></span>  | <span data-ttu-id="1125f-182">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="1125f-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="1125f-183">Zobrazí se další transakce pro částky v měně vykazování.</span><span class="sxs-lookup"><span data-stu-id="1125f-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="1125f-184">Provedení přecenění měny pro účty od 1. října 2015 do 31. prosince 2015</span><span class="sxs-lookup"><span data-stu-id="1125f-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="1125f-185">Zůstatky v konsolidované společnosti</span><span class="sxs-lookup"><span data-stu-id="1125f-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="1125f-186">Účet hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="1125f-186">Ledger account</span></span> | <span data-ttu-id="1125f-187">Měna</span><span class="sxs-lookup"><span data-stu-id="1125f-187">Currency</span></span> | <span data-ttu-id="1125f-188">Částka</span><span class="sxs-lookup"><span data-stu-id="1125f-188">Amount</span></span>  | <span data-ttu-id="1125f-189">Výpočet</span><span class="sxs-lookup"><span data-stu-id="1125f-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="1125f-190">110110</span><span class="sxs-lookup"><span data-stu-id="1125f-190">110110</span></span>         | <span data-ttu-id="1125f-191">EUR</span><span class="sxs-lookup"><span data-stu-id="1125f-191">EUR</span></span>      | <span data-ttu-id="1125f-192">500,00</span><span class="sxs-lookup"><span data-stu-id="1125f-192">500.00</span></span>  | <span data-ttu-id="1125f-193">Původní částka 500 × 1</span><span class="sxs-lookup"><span data-stu-id="1125f-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="1125f-194">130100</span><span class="sxs-lookup"><span data-stu-id="1125f-194">130100</span></span>         | <span data-ttu-id="1125f-195">EUR</span><span class="sxs-lookup"><span data-stu-id="1125f-195">EUR</span></span>      | <span data-ttu-id="1125f-196">-500,00</span><span class="sxs-lookup"><span data-stu-id="1125f-196">-500.00</span></span> | <span data-ttu-id="1125f-197">Původní částka -500 × 1</span><span class="sxs-lookup"><span data-stu-id="1125f-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="1125f-198">801400</span><span class="sxs-lookup"><span data-stu-id="1125f-198">801400</span></span>         | <span data-ttu-id="1125f-199">EUR</span><span class="sxs-lookup"><span data-stu-id="1125f-199">EUR</span></span>      | <span data-ttu-id="1125f-200">250</span><span class="sxs-lookup"><span data-stu-id="1125f-200">250</span></span>     | <span data-ttu-id="1125f-201">500 – 333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="1125f-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="1125f-202">801600</span><span class="sxs-lookup"><span data-stu-id="1125f-202">801600</span></span>         | <span data-ttu-id="1125f-203">EUR</span><span class="sxs-lookup"><span data-stu-id="1125f-203">EUR</span></span>      | <span data-ttu-id="1125f-204">-250</span><span class="sxs-lookup"><span data-stu-id="1125f-204">-250</span></span>    | <span data-ttu-id="1125f-205">-500 – (-333,33) = -166,67 -166,67 + (-83,33) = -250</span><span class="sxs-lookup"><span data-stu-id="1125f-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |





