---
title: Duální vykazování
description: Toto téma vás provede příkladem, který ukazuje, jak můžete splnit požadavky jak pro vykazování podle Mezinárodního standardu finančního výkaznictví (IFRS), tak pro statutární vykazování v leasingu majetku.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a7d9b3ea3d4f1d48b8a7326bd5a01d3119310c62
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003174"
---
# <a name="dual-reporting"></a><span data-ttu-id="f2578-103">Duální vykazování</span><span class="sxs-lookup"><span data-stu-id="f2578-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2578-104">Toto téma vás provede příkladem, který ukazuje, jak můžete splnit požadavky jak pro vykazování podle Mezinárodního standardu finančního výkaznictví (IFRS), tak pro statutární vykazování v leasingu majetku.</span><span class="sxs-lookup"><span data-stu-id="f2578-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="f2578-105">Znalost účtovacích vrstev v Microsoft Dynamics 365 Finance je nutná a příklad bude lépe srozumitelný.</span><span class="sxs-lookup"><span data-stu-id="f2578-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="f2578-106">Příklad</span><span class="sxs-lookup"><span data-stu-id="f2578-106">Example</span></span>

<span data-ttu-id="f2578-107">Následující příklad provádí účtování pro leasing podle italského statutárního výkaznictví pomocí metody hotovostního základu i metod vykazování podle IFRS.</span><span class="sxs-lookup"><span data-stu-id="f2578-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="f2578-108">Společnost musí založit tři účetní knihy, které zohlední jak italské zákonné požadavky, tak požadavky IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="f2578-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="f2578-109">Jedna kniha je vyžadována pro IFRS 16, jedna kniha je vyžadována pro zákonné požadavky a jedna kniha je vyžadována k automatickému stornování statutárních účtování.</span><span class="sxs-lookup"><span data-stu-id="f2578-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="f2578-110">Knihy jsou vytvořeny tak, jak je uvedeno v následujících tabulkách.</span><span class="sxs-lookup"><span data-stu-id="f2578-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="f2578-111">**Kniha IFRS 16**</span><span class="sxs-lookup"><span data-stu-id="f2578-111">**IFRS 16 book**</span></span>

<span data-ttu-id="f2578-112">Kniha IFRS 16 je vytvořena v souladu s účetním standardem IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="f2578-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="f2578-113">Všechny položky, které jsou zaúčtovány v této knize, budou zaúčtovány do vlastní vrstvy.</span><span class="sxs-lookup"><span data-stu-id="f2578-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="f2578-114">Jméno</span><span class="sxs-lookup"><span data-stu-id="f2578-114">Name</span></span>                                    | <span data-ttu-id="f2578-115">popis</span><span class="sxs-lookup"><span data-stu-id="f2578-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="f2578-116">Typ knihy</span><span class="sxs-lookup"><span data-stu-id="f2578-116">Book type</span></span>                               | <span data-ttu-id="f2578-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="f2578-117">IFRS 16</span></span>        |
| <span data-ttu-id="f2578-118">Popis knihy</span><span class="sxs-lookup"><span data-stu-id="f2578-118">Book description</span></span>                        | <span data-ttu-id="f2578-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="f2578-119">IFRS 16</span></span>        |
| <span data-ttu-id="f2578-120">Účtovací vrstva</span><span class="sxs-lookup"><span data-stu-id="f2578-120">Posting Layer</span></span>                           | <span data-ttu-id="f2578-121">Vlastní vrstva 1</span><span class="sxs-lookup"><span data-stu-id="f2578-121">Custom layer 1</span></span> |
| <span data-ttu-id="f2578-122">Typ leasingu</span><span class="sxs-lookup"><span data-stu-id="f2578-122">Lease Type</span></span>                              | <span data-ttu-id="f2578-123">Finance</span><span class="sxs-lookup"><span data-stu-id="f2578-123">Finance</span></span>        |
| <span data-ttu-id="f2578-124">Rámec účetnictví</span><span class="sxs-lookup"><span data-stu-id="f2578-124">Accounting Framework</span></span>                    | <span data-ttu-id="f2578-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="f2578-125">IFRS 16</span></span>        |
| <span data-ttu-id="f2578-126">Nastavení doby trvání leasingu / očekávané doby použitelnosti</span><span class="sxs-lookup"><span data-stu-id="f2578-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="f2578-127">0,00</span><span class="sxs-lookup"><span data-stu-id="f2578-127">0.00</span></span>           |
| <span data-ttu-id="f2578-128">Nastavení současné hodnoty / reálné hodnoty majetku</span><span class="sxs-lookup"><span data-stu-id="f2578-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="f2578-129">0,00</span><span class="sxs-lookup"><span data-stu-id="f2578-129">0.00</span></span>           |
| <span data-ttu-id="f2578-130">Krátkodobá prahová hodnota</span><span class="sxs-lookup"><span data-stu-id="f2578-130">Short-term threshold</span></span>                    | <span data-ttu-id="f2578-131">12</span><span class="sxs-lookup"><span data-stu-id="f2578-131">12</span></span>             |
| <span data-ttu-id="f2578-132">Nízká prahová hodnota</span><span class="sxs-lookup"><span data-stu-id="f2578-132">Low Value Threshold</span></span>                     | <span data-ttu-id="f2578-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="f2578-133">5,000.00</span></span>       |
| <span data-ttu-id="f2578-134">Platba dodavateli</span><span class="sxs-lookup"><span data-stu-id="f2578-134">Pay to Vendor</span></span>                           | <span data-ttu-id="f2578-135">Žádný</span><span class="sxs-lookup"><span data-stu-id="f2578-135">No</span></span>             |

<span data-ttu-id="f2578-136">**Statutární kniha**</span><span class="sxs-lookup"><span data-stu-id="f2578-136">**Statutory book**</span></span>

<span data-ttu-id="f2578-137">Statutární kniha je hotovostní kniha, kde společnost bude účtovat výdaje na leasing jako částku hotovosti, která se každý měsíc platí za nájem.</span><span class="sxs-lookup"><span data-stu-id="f2578-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="f2578-138">Tato kniha nevytvoří používaný majetek ani leasingový závazek.</span><span class="sxs-lookup"><span data-stu-id="f2578-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="f2578-139">Jméno</span><span class="sxs-lookup"><span data-stu-id="f2578-139">Name</span></span>                                    | <span data-ttu-id="f2578-140">popis</span><span class="sxs-lookup"><span data-stu-id="f2578-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="f2578-141">Typ knihy</span><span class="sxs-lookup"><span data-stu-id="f2578-141">Book type</span></span>                               | <span data-ttu-id="f2578-142">Statutární</span><span class="sxs-lookup"><span data-stu-id="f2578-142">Statutory</span></span>   |
| <span data-ttu-id="f2578-143">Popis knihy</span><span class="sxs-lookup"><span data-stu-id="f2578-143">Book description</span></span>                        | <span data-ttu-id="f2578-144">Místní GAAP</span><span class="sxs-lookup"><span data-stu-id="f2578-144">Local GAAP</span></span>  |
| <span data-ttu-id="f2578-145">Účtovací vrstva</span><span class="sxs-lookup"><span data-stu-id="f2578-145">Posting Layer</span></span>                           | <span data-ttu-id="f2578-146">Aktuální</span><span class="sxs-lookup"><span data-stu-id="f2578-146">Current</span></span>     |
| <span data-ttu-id="f2578-147">Typ leasingu</span><span class="sxs-lookup"><span data-stu-id="f2578-147">Lease Type</span></span>                              | <span data-ttu-id="f2578-148">Automatické</span><span class="sxs-lookup"><span data-stu-id="f2578-148">Automatic</span></span>   |
| <span data-ttu-id="f2578-149">Rámec účetnictví</span><span class="sxs-lookup"><span data-stu-id="f2578-149">Accounting Framework</span></span>                    | <span data-ttu-id="f2578-150">Hotovostní základ</span><span class="sxs-lookup"><span data-stu-id="f2578-150">Cash basis</span></span>  |
| <span data-ttu-id="f2578-151">Nastavení doby trvání leasingu / očekávané doby použitelnosti</span><span class="sxs-lookup"><span data-stu-id="f2578-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="f2578-152">0,00</span><span class="sxs-lookup"><span data-stu-id="f2578-152">0.00</span></span>        |
| <span data-ttu-id="f2578-153">Nastavení současné hodnoty / reálné hodnoty majetku</span><span class="sxs-lookup"><span data-stu-id="f2578-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="f2578-154">0,00</span><span class="sxs-lookup"><span data-stu-id="f2578-154">0.00</span></span>        |
| <span data-ttu-id="f2578-155">Krátkodobá prahová hodnota</span><span class="sxs-lookup"><span data-stu-id="f2578-155">Short-term threshold</span></span>                    | <span data-ttu-id="f2578-156">0</span><span class="sxs-lookup"><span data-stu-id="f2578-156">0</span></span>           |
| <span data-ttu-id="f2578-157">Nízká prahová hodnota</span><span class="sxs-lookup"><span data-stu-id="f2578-157">Low Value Threshold</span></span>                     | <span data-ttu-id="f2578-158">0</span><span class="sxs-lookup"><span data-stu-id="f2578-158">0</span></span>           |
| <span data-ttu-id="f2578-159">Platba dodavateli</span><span class="sxs-lookup"><span data-stu-id="f2578-159">Pay to Vendor</span></span>                           | <span data-ttu-id="f2578-160">Žádný</span><span class="sxs-lookup"><span data-stu-id="f2578-160">No</span></span>          |

<span data-ttu-id="f2578-161">**Statutární stornovací kniha**</span><span class="sxs-lookup"><span data-stu-id="f2578-161">**Statutory reversal book**</span></span>

<span data-ttu-id="f2578-162">Statutární stornovací kniha je sestavena stejným způsobem jako statutární kniha.</span><span class="sxs-lookup"><span data-stu-id="f2578-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="f2578-163">Jméno</span><span class="sxs-lookup"><span data-stu-id="f2578-163">Name</span></span>                                    | <span data-ttu-id="f2578-164">popis</span><span class="sxs-lookup"><span data-stu-id="f2578-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="f2578-165">Typ knihy</span><span class="sxs-lookup"><span data-stu-id="f2578-165">Book type</span></span>                               | <span data-ttu-id="f2578-166">Statutární – storno</span><span class="sxs-lookup"><span data-stu-id="f2578-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="f2578-167">Popis knihy</span><span class="sxs-lookup"><span data-stu-id="f2578-167">Book description</span></span>                        | <span data-ttu-id="f2578-168">Kniha pro stornování statutární knihy</span><span class="sxs-lookup"><span data-stu-id="f2578-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="f2578-169">Účtovací vrstva</span><span class="sxs-lookup"><span data-stu-id="f2578-169">Posting Layer</span></span>                           | <span data-ttu-id="f2578-170">Vlastní vrstva 1</span><span class="sxs-lookup"><span data-stu-id="f2578-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="f2578-171">Typ leasingu</span><span class="sxs-lookup"><span data-stu-id="f2578-171">Lease Type</span></span>                              | <span data-ttu-id="f2578-172">Automatické</span><span class="sxs-lookup"><span data-stu-id="f2578-172">Automatic</span></span>                      |
| <span data-ttu-id="f2578-173">Rámec účetnictví</span><span class="sxs-lookup"><span data-stu-id="f2578-173">Accounting Framework</span></span>                    | <span data-ttu-id="f2578-174">Hotovostní základ</span><span class="sxs-lookup"><span data-stu-id="f2578-174">Cash basis</span></span>                     |
| <span data-ttu-id="f2578-175">Nastavení doby trvání leasingu / očekávané doby použitelnosti</span><span class="sxs-lookup"><span data-stu-id="f2578-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="f2578-176">0,00</span><span class="sxs-lookup"><span data-stu-id="f2578-176">0.00</span></span>                           |
| <span data-ttu-id="f2578-177">Nastavení současné hodnoty / reálné hodnoty majetku</span><span class="sxs-lookup"><span data-stu-id="f2578-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="f2578-178">0,00</span><span class="sxs-lookup"><span data-stu-id="f2578-178">0.00</span></span>                           |
| <span data-ttu-id="f2578-179">Krátkodobá prahová hodnota</span><span class="sxs-lookup"><span data-stu-id="f2578-179">Short-term threshold</span></span>                    | <span data-ttu-id="f2578-180">0</span><span class="sxs-lookup"><span data-stu-id="f2578-180">0</span></span>                              |
| <span data-ttu-id="f2578-181">Nízká prahová hodnota</span><span class="sxs-lookup"><span data-stu-id="f2578-181">Low Value Threshold</span></span>                     | <span data-ttu-id="f2578-182">0</span><span class="sxs-lookup"><span data-stu-id="f2578-182">0</span></span>                              |
| <span data-ttu-id="f2578-183">Platba dodavateli</span><span class="sxs-lookup"><span data-stu-id="f2578-183">Pay to Vendor</span></span>                           | <span data-ttu-id="f2578-184">Žádný</span><span class="sxs-lookup"><span data-stu-id="f2578-184">No</span></span>                             |

<span data-ttu-id="f2578-185">V tomto příkladu byl vytvořen leasing, který má následující nastavení na kartách **Obecné** a **Řádky platebního kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="f2578-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="f2578-186">**Karta Obecné**</span><span class="sxs-lookup"><span data-stu-id="f2578-186">**General tab**</span></span>

| <span data-ttu-id="f2578-187">Pole</span><span class="sxs-lookup"><span data-stu-id="f2578-187">Field</span></span>                      | <span data-ttu-id="f2578-188">Hodnota</span><span class="sxs-lookup"><span data-stu-id="f2578-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="f2578-189">Přírůstková výpůjční úroková sazba</span><span class="sxs-lookup"><span data-stu-id="f2578-189">Incremental borrowing rate</span></span> | <span data-ttu-id="f2578-190">5 %</span><span class="sxs-lookup"><span data-stu-id="f2578-190">5%</span></span>               |
| <span data-ttu-id="f2578-191">Datum zahájení</span><span class="sxs-lookup"><span data-stu-id="f2578-191">Commencement date</span></span>          | <span data-ttu-id="f2578-192">1. 1. 2020</span><span class="sxs-lookup"><span data-stu-id="f2578-192">1/1/2020</span></span>         |
| <span data-ttu-id="f2578-193">Skupina leasingu</span><span class="sxs-lookup"><span data-stu-id="f2578-193">Lease group</span></span>                | <span data-ttu-id="f2578-194">Budovy</span><span class="sxs-lookup"><span data-stu-id="f2578-194">Buildings</span></span>        |
| <span data-ttu-id="f2578-195">Dodavatel</span><span class="sxs-lookup"><span data-stu-id="f2578-195">Vendor</span></span>                     | <span data-ttu-id="f2578-196">1001</span><span class="sxs-lookup"><span data-stu-id="f2578-196">1001</span></span>             |
| <span data-ttu-id="f2578-197">Reálná hodnota majetku</span><span class="sxs-lookup"><span data-stu-id="f2578-197">Fair value of the asset</span></span>    | <span data-ttu-id="f2578-198">245,000</span><span class="sxs-lookup"><span data-stu-id="f2578-198">245,000</span></span>          |
| <span data-ttu-id="f2578-199">Očekávaná doba použitelnosti majetku</span><span class="sxs-lookup"><span data-stu-id="f2578-199">Asset useful life</span></span>          | <span data-ttu-id="f2578-200">120</span><span class="sxs-lookup"><span data-stu-id="f2578-200">120</span></span>              |
| <span data-ttu-id="f2578-201">Typ anuity</span><span class="sxs-lookup"><span data-stu-id="f2578-201">Annuity type</span></span>               | <span data-ttu-id="f2578-202">Běžná anuita</span><span class="sxs-lookup"><span data-stu-id="f2578-202">Ordinary annuity</span></span> |
| <span data-ttu-id="f2578-203">Interval úročení</span><span class="sxs-lookup"><span data-stu-id="f2578-203">Compounding interval</span></span>       | <span data-ttu-id="f2578-204">Měsíčně</span><span class="sxs-lookup"><span data-stu-id="f2578-204">Monthly</span></span>          |

<span data-ttu-id="f2578-205">**Karta Řádky platebního kalendáře**</span><span class="sxs-lookup"><span data-stu-id="f2578-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="f2578-206">Pole</span><span class="sxs-lookup"><span data-stu-id="f2578-206">Field</span></span>             | <span data-ttu-id="f2578-207">Hodnota</span><span class="sxs-lookup"><span data-stu-id="f2578-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="f2578-208">Počáteční datum</span><span class="sxs-lookup"><span data-stu-id="f2578-208">Start date</span></span>        | <span data-ttu-id="f2578-209">1. 1. 2020</span><span class="sxs-lookup"><span data-stu-id="f2578-209">1/1/2020</span></span>   |
| <span data-ttu-id="f2578-210">Interval období</span><span class="sxs-lookup"><span data-stu-id="f2578-210">Period interval</span></span>   | <span data-ttu-id="f2578-211">Měsíce</span><span class="sxs-lookup"><span data-stu-id="f2578-211">Months</span></span>     |
| <span data-ttu-id="f2578-212">Období</span><span class="sxs-lookup"><span data-stu-id="f2578-212">Periods</span></span>           | <span data-ttu-id="f2578-213">24</span><span class="sxs-lookup"><span data-stu-id="f2578-213">24</span></span>         |
| <span data-ttu-id="f2578-214">Koncové datum</span><span class="sxs-lookup"><span data-stu-id="f2578-214">End date</span></span>          | <span data-ttu-id="f2578-215">31. 12. 2020</span><span class="sxs-lookup"><span data-stu-id="f2578-215">12/31/2020</span></span> |
| <span data-ttu-id="f2578-216">Četnost plateb</span><span class="sxs-lookup"><span data-stu-id="f2578-216">Payment frequency</span></span> | <span data-ttu-id="f2578-217">Měsíčně</span><span class="sxs-lookup"><span data-stu-id="f2578-217">Monthly</span></span>    |
| <span data-ttu-id="f2578-218">Částka platby</span><span class="sxs-lookup"><span data-stu-id="f2578-218">Payment amount</span></span>    | <span data-ttu-id="f2578-219">1 000</span><span class="sxs-lookup"><span data-stu-id="f2578-219">1,000</span></span>      |

<span data-ttu-id="f2578-220">Chcete-li tento leasing započítat do dvou rámců, použijete aktuální účtovací vrstvu a vlastní účtovací vrstvu.</span><span class="sxs-lookup"><span data-stu-id="f2578-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="f2578-221">Následující tabulka ukazuje příklad každé položky deníku, která je potřeba pro věrné zobrazení financí podle každého standardu výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="f2578-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="f2578-222">Podrobný popis každé položky deníku pro první měsíc leasingu je poskytnut později.</span><span class="sxs-lookup"><span data-stu-id="f2578-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="f2578-223">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="f2578-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="f2578-224">popis</span><span class="sxs-lookup"><span data-stu-id="f2578-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="f2578-225">Statutární kniha (aktuální vrstva)</span><span class="sxs-lookup"><span data-stu-id="f2578-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="f2578-226">Celková aktuální vrstva</span><span class="sxs-lookup"><span data-stu-id="f2578-226">Current layer total</span></span></th>
<th><span data-ttu-id="f2578-227">Stornovací kniha (vlastní vrstva)</span><span class="sxs-lookup"><span data-stu-id="f2578-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="f2578-228">Kniha IFRS 16 (vlastní vrstva)</span><span class="sxs-lookup"><span data-stu-id="f2578-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="f2578-229">Aktuální vrstva + vlastní vrstva celkem</span><span class="sxs-lookup"><span data-stu-id="f2578-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f2578-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="f2578-230">JE-100</span></span></th>
<th><span data-ttu-id="f2578-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="f2578-231">JE-110</span></span></th>
<th><span data-ttu-id="f2578-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="f2578-232">JE-120</span></span></th>
<th><span data-ttu-id="f2578-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="f2578-233">JE-130</span></span></th>
<th><span data-ttu-id="f2578-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="f2578-234">JE-140</span></span></th>
<th><span data-ttu-id="f2578-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="f2578-235">JE-150</span></span></th>
<th><span data-ttu-id="f2578-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="f2578-236">JE-160</span></span></th>
<th><span data-ttu-id="f2578-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="f2578-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f2578-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="f2578-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="f2578-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="f2578-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="f2578-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="f2578-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="f2578-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="f2578-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="f2578-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="f2578-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="f2578-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="f2578-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="f2578-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="f2578-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="f2578-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="f2578-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f2578-246">1</span><span class="sxs-lookup"><span data-stu-id="f2578-246">1</span></span></td>
<td><span data-ttu-id="f2578-247">Výdaje leasingu</span><span class="sxs-lookup"><span data-stu-id="f2578-247">Lease expense</span></span></td>
<td><span data-ttu-id="f2578-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="f2578-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="f2578-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="f2578-249">1,000.00</span></span></td>
<td><span data-ttu-id="f2578-250">−1 000,00</span><span class="sxs-lookup"><span data-stu-id="f2578-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f2578-251">0,00</span><span class="sxs-lookup"><span data-stu-id="f2578-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2578-252">2</span><span class="sxs-lookup"><span data-stu-id="f2578-252">2</span></span></td>
<td><span data-ttu-id="f2578-253">Bankovní poplatek</span><span class="sxs-lookup"><span data-stu-id="f2578-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="f2578-254">3.00</span><span class="sxs-lookup"><span data-stu-id="f2578-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="f2578-255">3.00</span><span class="sxs-lookup"><span data-stu-id="f2578-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f2578-256">3.00</span><span class="sxs-lookup"><span data-stu-id="f2578-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2578-257">3</span><span class="sxs-lookup"><span data-stu-id="f2578-257">3</span></span></td>
<td><span data-ttu-id="f2578-258">Výdaje DPH</span><span class="sxs-lookup"><span data-stu-id="f2578-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="f2578-259">5.00</span><span class="sxs-lookup"><span data-stu-id="f2578-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="f2578-260">5.00</span><span class="sxs-lookup"><span data-stu-id="f2578-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f2578-261">5.00</span><span class="sxs-lookup"><span data-stu-id="f2578-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2578-262">4</span><span class="sxs-lookup"><span data-stu-id="f2578-262">4</span></span></td>
<td><span data-ttu-id="f2578-263">Clearingový účet</span><span class="sxs-lookup"><span data-stu-id="f2578-263">Clearing account</span></span></td>
<td><span data-ttu-id="f2578-264">−1 000,00</span><span class="sxs-lookup"><span data-stu-id="f2578-264">-1,000.00</span></span></td>
<td><span data-ttu-id="f2578-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="f2578-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="f2578-266">0,00</span><span class="sxs-lookup"><span data-stu-id="f2578-266">0.00</span></span></td>
<td><span data-ttu-id="f2578-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="f2578-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="f2578-268">−1 000,00</span><span class="sxs-lookup"><span data-stu-id="f2578-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="f2578-269">0,00</span><span class="sxs-lookup"><span data-stu-id="f2578-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2578-270">5</span><span class="sxs-lookup"><span data-stu-id="f2578-270">5</span></span></td>
<td><span data-ttu-id="f2578-271">Závazky</span><span class="sxs-lookup"><span data-stu-id="f2578-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="f2578-272">-1008,00</span><span class="sxs-lookup"><span data-stu-id="f2578-272">-1,008.00</span></span></td>
<td><span data-ttu-id="f2578-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="f2578-273">1,008.00</span></span></td>
<td><span data-ttu-id="f2578-274">0,00</span><span class="sxs-lookup"><span data-stu-id="f2578-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f2578-275">0,00</span><span class="sxs-lookup"><span data-stu-id="f2578-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2578-276">6</span><span class="sxs-lookup"><span data-stu-id="f2578-276">6</span></span></td>
<td><span data-ttu-id="f2578-277">Používaný majetek</span><span class="sxs-lookup"><span data-stu-id="f2578-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f2578-278">0,00</span><span class="sxs-lookup"><span data-stu-id="f2578-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="f2578-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="f2578-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f2578-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="f2578-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2578-281">7</span><span class="sxs-lookup"><span data-stu-id="f2578-281">7</span></span></td>
<td><span data-ttu-id="f2578-282">Povinnost finančního leasingu</span><span class="sxs-lookup"><span data-stu-id="f2578-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f2578-283">0,00</span><span class="sxs-lookup"><span data-stu-id="f2578-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="f2578-284">-22 794,00</span><span class="sxs-lookup"><span data-stu-id="f2578-284">-22,794.00</span></span></td>
<td><span data-ttu-id="f2578-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="f2578-285">1,000.00</span></span></td>
<td><span data-ttu-id="f2578-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="f2578-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="f2578-287">-21 888,87</span><span class="sxs-lookup"><span data-stu-id="f2578-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2578-288">8</span><span class="sxs-lookup"><span data-stu-id="f2578-288">8</span></span></td>
<td><span data-ttu-id="f2578-289">Výdaje na úroky</span><span class="sxs-lookup"><span data-stu-id="f2578-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f2578-290">0,00</span><span class="sxs-lookup"><span data-stu-id="f2578-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f2578-291">94.97</span><span class="sxs-lookup"><span data-stu-id="f2578-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="f2578-292">94.97</span><span class="sxs-lookup"><span data-stu-id="f2578-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2578-293">9</span><span class="sxs-lookup"><span data-stu-id="f2578-293">9</span></span></td>
<td><span data-ttu-id="f2578-294">Hotovost</span><span class="sxs-lookup"><span data-stu-id="f2578-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="f2578-295">-1008,00</span><span class="sxs-lookup"><span data-stu-id="f2578-295">-1,008.00</span></span></td>
<td><span data-ttu-id="f2578-296">-1008,00</span><span class="sxs-lookup"><span data-stu-id="f2578-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f2578-297">-1008,00</span><span class="sxs-lookup"><span data-stu-id="f2578-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2578-298">10</span><span class="sxs-lookup"><span data-stu-id="f2578-298">10</span></span></td>
<td><span data-ttu-id="f2578-299">Odpisové výdaje</span><span class="sxs-lookup"><span data-stu-id="f2578-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f2578-300">0,00</span><span class="sxs-lookup"><span data-stu-id="f2578-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f2578-301">949.75</span><span class="sxs-lookup"><span data-stu-id="f2578-301">949.75</span></span></td>
<td><span data-ttu-id="f2578-302">949.75</span><span class="sxs-lookup"><span data-stu-id="f2578-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2578-303">11</span><span class="sxs-lookup"><span data-stu-id="f2578-303">11</span></span></td>
<td><span data-ttu-id="f2578-304">Akumulovaný odpis</span><span class="sxs-lookup"><span data-stu-id="f2578-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f2578-305">0,00</span><span class="sxs-lookup"><span data-stu-id="f2578-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f2578-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="f2578-306">-949.75</span></span></td>
<td><span data-ttu-id="f2578-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="f2578-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f2578-308">Jak ukazuje předchozí tabulka, jsou potřeba tři knihy pro vykazování v rámci statutárního výkaznictví i výkaznictví podle IFRS.</span><span class="sxs-lookup"><span data-stu-id="f2578-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="f2578-309">Statutární kniha zaznamenává leasingové splátky podle pravidel pro hotovostní účetnictví v aktuální vrstvě.</span><span class="sxs-lookup"><span data-stu-id="f2578-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="f2578-310">Statutární stornovací kniha stornuje položky statutárního deníku.</span><span class="sxs-lookup"><span data-stu-id="f2578-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="f2578-311">Kniha IFRS 16 vytváří položky deníku, které jsou vyžadovány podle IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="f2578-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="f2578-312">Leasing musíte zadat pouze jednou.</span><span class="sxs-lookup"><span data-stu-id="f2578-312">You must enter a lease only one time.</span></span> <span data-ttu-id="f2578-313">Poté můžete otevřít stránku **Knihy**, kde jsou všechny knihy, které jsou přidruženy k leasingu.</span><span class="sxs-lookup"><span data-stu-id="f2578-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="f2578-314">Když vytvoříte knihy, všechny tři musí být přidruženy ke stejnému záznamu leasingu.</span><span class="sxs-lookup"><span data-stu-id="f2578-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="f2578-315">První položka deníku zaznamenává výdaje na leasing podle statutární knihy.</span><span class="sxs-lookup"><span data-stu-id="f2578-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="f2578-316">Platby můžete vytvářet v dávce nebo výběrem platebního kalendáře ve statutární knize.</span><span class="sxs-lookup"><span data-stu-id="f2578-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="f2578-317">V tomto příkladu se pro statutární knihu z platebního kalendáře vytvoří následující položka deníku.</span><span class="sxs-lookup"><span data-stu-id="f2578-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="f2578-318">Leasingová splátka – 31. 1. 2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="f2578-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="f2578-319">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="f2578-319">Account type</span></span> | <span data-ttu-id="f2578-320">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="f2578-320">Account number</span></span> | <span data-ttu-id="f2578-321">Vrstva</span><span class="sxs-lookup"><span data-stu-id="f2578-321">Layer</span></span>   | <span data-ttu-id="f2578-322">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="f2578-322">Account description</span></span> | <span data-ttu-id="f2578-323">Debet</span><span class="sxs-lookup"><span data-stu-id="f2578-323">Debit</span></span>    | <span data-ttu-id="f2578-324">Kredit</span><span class="sxs-lookup"><span data-stu-id="f2578-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="f2578-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="f2578-325">Ledger</span></span>       | <span data-ttu-id="f2578-326">1</span><span class="sxs-lookup"><span data-stu-id="f2578-326">1</span></span>              | <span data-ttu-id="f2578-327">Aktuální</span><span class="sxs-lookup"><span data-stu-id="f2578-327">Current</span></span> | <span data-ttu-id="f2578-328">Výdaje leasingu</span><span class="sxs-lookup"><span data-stu-id="f2578-328">Lease expense</span></span>       | <span data-ttu-id="f2578-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="f2578-329">1,000.00</span></span> |          |
| <span data-ttu-id="f2578-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="f2578-330">Ledger</span></span>       | <span data-ttu-id="f2578-331">4</span><span class="sxs-lookup"><span data-stu-id="f2578-331">4</span></span>              | <span data-ttu-id="f2578-332">Aktuální</span><span class="sxs-lookup"><span data-stu-id="f2578-332">Current</span></span> | <span data-ttu-id="f2578-333">Clearingový účet</span><span class="sxs-lookup"><span data-stu-id="f2578-333">Clearing account</span></span>    |          | <span data-ttu-id="f2578-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="f2578-334">1,000.00</span></span> |

<span data-ttu-id="f2578-335">Úředník pro závazky používá standardní funkce Dynamics 365 k vytvoření fakturu pro zaplacení leasingu mimo leasing majetku.</span><span class="sxs-lookup"><span data-stu-id="f2578-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="f2578-336">Nicméně místo výběru **Výdaje na leasing** jako debetního účtu vybere clearingový účet pro vygenerování následující položky.</span><span class="sxs-lookup"><span data-stu-id="f2578-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="f2578-337">Proces AP – 31. 1. 2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="f2578-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="f2578-338">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="f2578-338">Account type</span></span> | <span data-ttu-id="f2578-339">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="f2578-339">Account number</span></span> | <span data-ttu-id="f2578-340">Vrstva</span><span class="sxs-lookup"><span data-stu-id="f2578-340">Layer</span></span>   | <span data-ttu-id="f2578-341">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="f2578-341">Account description</span></span> | <span data-ttu-id="f2578-342">Debet</span><span class="sxs-lookup"><span data-stu-id="f2578-342">Debit</span></span>    | <span data-ttu-id="f2578-343">Kredit</span><span class="sxs-lookup"><span data-stu-id="f2578-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="f2578-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="f2578-344">Ledger</span></span>       | <span data-ttu-id="f2578-345">4</span><span class="sxs-lookup"><span data-stu-id="f2578-345">4</span></span>              | <span data-ttu-id="f2578-346">Aktuální</span><span class="sxs-lookup"><span data-stu-id="f2578-346">Current</span></span> | <span data-ttu-id="f2578-347">Clearingový účet</span><span class="sxs-lookup"><span data-stu-id="f2578-347">Clearing account</span></span>    | <span data-ttu-id="f2578-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="f2578-348">1,000.00</span></span> |          |
| <span data-ttu-id="f2578-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="f2578-349">Ledger</span></span>       | <span data-ttu-id="f2578-350">2</span><span class="sxs-lookup"><span data-stu-id="f2578-350">2</span></span>              | <span data-ttu-id="f2578-351">Aktuální</span><span class="sxs-lookup"><span data-stu-id="f2578-351">Current</span></span> | <span data-ttu-id="f2578-352">Bankovní poplatek</span><span class="sxs-lookup"><span data-stu-id="f2578-352">Bank fee</span></span>            | <span data-ttu-id="f2578-353">3.00</span><span class="sxs-lookup"><span data-stu-id="f2578-353">3.00</span></span>     |          |
| <span data-ttu-id="f2578-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="f2578-354">Ledger</span></span>       | <span data-ttu-id="f2578-355">3</span><span class="sxs-lookup"><span data-stu-id="f2578-355">3</span></span>              | <span data-ttu-id="f2578-356">Aktuální</span><span class="sxs-lookup"><span data-stu-id="f2578-356">Current</span></span> | <span data-ttu-id="f2578-357">Výdaje DPH</span><span class="sxs-lookup"><span data-stu-id="f2578-357">VAT expense</span></span>         | <span data-ttu-id="f2578-358">5.00</span><span class="sxs-lookup"><span data-stu-id="f2578-358">5.00</span></span>     |          |
| <span data-ttu-id="f2578-359">Dodavatel</span><span class="sxs-lookup"><span data-stu-id="f2578-359">Vendor</span></span>       | <span data-ttu-id="f2578-360">5</span><span class="sxs-lookup"><span data-stu-id="f2578-360">5</span></span>              | <span data-ttu-id="f2578-361">Aktuální</span><span class="sxs-lookup"><span data-stu-id="f2578-361">Current</span></span> | <span data-ttu-id="f2578-362">Závazky</span><span class="sxs-lookup"><span data-stu-id="f2578-362">Accounts payable</span></span>    |          | <span data-ttu-id="f2578-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="f2578-363">1,008.00</span></span> |

<span data-ttu-id="f2578-364">Když je prodejci vystaven výpis, postupujete podle pravidelného platebního procesu.</span><span class="sxs-lookup"><span data-stu-id="f2578-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="f2578-365">Během tohoto procesu je vygenerována následující položka deníku.</span><span class="sxs-lookup"><span data-stu-id="f2578-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="f2578-366">Platba v hotovosti – 31. 1. 2020 – 120</span><span class="sxs-lookup"><span data-stu-id="f2578-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="f2578-367">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="f2578-367">Account type</span></span> | <span data-ttu-id="f2578-368">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="f2578-368">Account number</span></span> | <span data-ttu-id="f2578-369">Vrstva</span><span class="sxs-lookup"><span data-stu-id="f2578-369">Layer</span></span>   | <span data-ttu-id="f2578-370">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="f2578-370">Account description</span></span> | <span data-ttu-id="f2578-371">Debet</span><span class="sxs-lookup"><span data-stu-id="f2578-371">Debit</span></span>    | <span data-ttu-id="f2578-372">Kredit</span><span class="sxs-lookup"><span data-stu-id="f2578-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="f2578-373">Dodavatel</span><span class="sxs-lookup"><span data-stu-id="f2578-373">Vendor</span></span>       | <span data-ttu-id="f2578-374">5</span><span class="sxs-lookup"><span data-stu-id="f2578-374">5</span></span>              | <span data-ttu-id="f2578-375">Aktuální</span><span class="sxs-lookup"><span data-stu-id="f2578-375">Current</span></span> | <span data-ttu-id="f2578-376">Závazky</span><span class="sxs-lookup"><span data-stu-id="f2578-376">Accounts Payable</span></span>    | <span data-ttu-id="f2578-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="f2578-377">1,008.00</span></span> |          |
| <span data-ttu-id="f2578-378">Banka</span><span class="sxs-lookup"><span data-stu-id="f2578-378">Bank</span></span>         | <span data-ttu-id="f2578-379">9</span><span class="sxs-lookup"><span data-stu-id="f2578-379">9</span></span>              | <span data-ttu-id="f2578-380">Aktuální</span><span class="sxs-lookup"><span data-stu-id="f2578-380">Current</span></span> | <span data-ttu-id="f2578-381">Hotovost</span><span class="sxs-lookup"><span data-stu-id="f2578-381">Cash</span></span>                |          | <span data-ttu-id="f2578-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="f2578-382">1,008.00</span></span> |

<span data-ttu-id="f2578-383">V tomto okamžiku jste plně zaúčtovali tento leasing podle zákonných požadavků na výkaznictví a můžete vygenerovat předvahu pomocí aktuální vrstvy.</span><span class="sxs-lookup"><span data-stu-id="f2578-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="f2578-384">Systém vrátí předvahu s následujícími čísly.</span><span class="sxs-lookup"><span data-stu-id="f2578-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="f2578-385">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="f2578-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="f2578-386">popis</span><span class="sxs-lookup"><span data-stu-id="f2578-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="f2578-387">Statutární kniha (aktuální vrstva)</span><span class="sxs-lookup"><span data-stu-id="f2578-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="f2578-388">Celková aktuální vrstva</span><span class="sxs-lookup"><span data-stu-id="f2578-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f2578-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="f2578-389">JE-100</span></span></th>
<th><span data-ttu-id="f2578-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="f2578-390">JE-110</span></span></th>
<th><span data-ttu-id="f2578-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="f2578-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f2578-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="f2578-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="f2578-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="f2578-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="f2578-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="f2578-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f2578-395">1</span><span class="sxs-lookup"><span data-stu-id="f2578-395">1</span></span></td>
<td><span data-ttu-id="f2578-396">Výdaje leasingu</span><span class="sxs-lookup"><span data-stu-id="f2578-396">Lease expense</span></span></td>
<td><span data-ttu-id="f2578-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="f2578-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="f2578-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="f2578-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2578-399">2</span><span class="sxs-lookup"><span data-stu-id="f2578-399">2</span></span></td>
<td><span data-ttu-id="f2578-400">Bankovní poplatek</span><span class="sxs-lookup"><span data-stu-id="f2578-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="f2578-401">3.00</span><span class="sxs-lookup"><span data-stu-id="f2578-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="f2578-402">3.00</span><span class="sxs-lookup"><span data-stu-id="f2578-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2578-403">3</span><span class="sxs-lookup"><span data-stu-id="f2578-403">3</span></span></td>
<td><span data-ttu-id="f2578-404">Výdaje DPH</span><span class="sxs-lookup"><span data-stu-id="f2578-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="f2578-405">5.00</span><span class="sxs-lookup"><span data-stu-id="f2578-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="f2578-406">5.00</span><span class="sxs-lookup"><span data-stu-id="f2578-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2578-407">4</span><span class="sxs-lookup"><span data-stu-id="f2578-407">4</span></span></td>
<td><span data-ttu-id="f2578-408">Clearingový účet</span><span class="sxs-lookup"><span data-stu-id="f2578-408">Clearing account</span></span></td>
<td><span data-ttu-id="f2578-409">−1 000,00</span><span class="sxs-lookup"><span data-stu-id="f2578-409">-1,000.00</span></span></td>
<td><span data-ttu-id="f2578-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="f2578-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="f2578-411">0,00</span><span class="sxs-lookup"><span data-stu-id="f2578-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2578-412">5</span><span class="sxs-lookup"><span data-stu-id="f2578-412">5</span></span></td>
<td><span data-ttu-id="f2578-413">Závazky</span><span class="sxs-lookup"><span data-stu-id="f2578-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="f2578-414">-1008,00</span><span class="sxs-lookup"><span data-stu-id="f2578-414">-1,008.00</span></span></td>
<td><span data-ttu-id="f2578-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="f2578-415">1,008.00</span></span></td>
<td><span data-ttu-id="f2578-416">0,00</span><span class="sxs-lookup"><span data-stu-id="f2578-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2578-417">6</span><span class="sxs-lookup"><span data-stu-id="f2578-417">6</span></span></td>
<td><span data-ttu-id="f2578-418">Používaný majetek</span><span class="sxs-lookup"><span data-stu-id="f2578-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f2578-419">0,00</span><span class="sxs-lookup"><span data-stu-id="f2578-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2578-420">7</span><span class="sxs-lookup"><span data-stu-id="f2578-420">7</span></span></td>
<td><span data-ttu-id="f2578-421">Povinnost finančního leasingu</span><span class="sxs-lookup"><span data-stu-id="f2578-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f2578-422">0,00</span><span class="sxs-lookup"><span data-stu-id="f2578-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2578-423">8</span><span class="sxs-lookup"><span data-stu-id="f2578-423">8</span></span></td>
<td><span data-ttu-id="f2578-424">Výdaje na úroky</span><span class="sxs-lookup"><span data-stu-id="f2578-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f2578-425">0,00</span><span class="sxs-lookup"><span data-stu-id="f2578-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2578-426">9</span><span class="sxs-lookup"><span data-stu-id="f2578-426">9</span></span></td>
<td><span data-ttu-id="f2578-427">Hotovost</span><span class="sxs-lookup"><span data-stu-id="f2578-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="f2578-428">-1008,00</span><span class="sxs-lookup"><span data-stu-id="f2578-428">-1,008.00</span></span></td>
<td><span data-ttu-id="f2578-429">-1008,00</span><span class="sxs-lookup"><span data-stu-id="f2578-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2578-430">10</span><span class="sxs-lookup"><span data-stu-id="f2578-430">10</span></span></td>
<td><span data-ttu-id="f2578-431">Odpisové výdaje</span><span class="sxs-lookup"><span data-stu-id="f2578-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f2578-432">0,00</span><span class="sxs-lookup"><span data-stu-id="f2578-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f2578-433">11</span><span class="sxs-lookup"><span data-stu-id="f2578-433">11</span></span></td>
<td><span data-ttu-id="f2578-434">Akumulovaný odpis</span><span class="sxs-lookup"><span data-stu-id="f2578-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="f2578-435">0,00</span><span class="sxs-lookup"><span data-stu-id="f2578-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f2578-436">Pokud chcete použít čísla IFRS 16 ke spuštění stejné předvahy, musí být položky deníku statutárního účtování stornovány a položky deníku IFRS 16 musí být zaúčtovány.</span><span class="sxs-lookup"><span data-stu-id="f2578-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="f2578-437">Chcete-li stornovat položky statutárního deníku, tento příklad obsahuje statutární stornovací knihu, která má stejné nastavení jako statutární kniha, ale má opačný profil účtování.</span><span class="sxs-lookup"><span data-stu-id="f2578-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="f2578-438">Například statutární kniha *debetovala* účet výdaje na leasing, ale stornovací kniha bude tento účet *kreditovat*.</span><span class="sxs-lookup"><span data-stu-id="f2578-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="f2578-439">Tyto vztahy lze snadno definovat v účtech pro zaúčtování leasingu majetku na stránce **Parametry leasingu majetku** (**Leasing majetku \> Nastavení \> Parametry leasingu majetku**).</span><span class="sxs-lookup"><span data-stu-id="f2578-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="f2578-440">Když se pro stornovací knihu použije stejný proces, který byl použit pro statutární knihu, vytvoří se následující položka deníku.</span><span class="sxs-lookup"><span data-stu-id="f2578-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="f2578-441">Rozdíl je v tom, že stornovací kniha rezervuje stornované položky ze statutární knihy.</span><span class="sxs-lookup"><span data-stu-id="f2578-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="f2578-442">Stornování položek se provede také ve vlastní vrstvě.</span><span class="sxs-lookup"><span data-stu-id="f2578-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="f2578-443">Když je na aktuální vrstvě spuštěna předvaha, stornované položky deníku nejsou zahrnuty.</span><span class="sxs-lookup"><span data-stu-id="f2578-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="f2578-444">Leasingová splátka – 31. 1. 2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="f2578-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="f2578-445">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="f2578-445">Account type</span></span> | <span data-ttu-id="f2578-446">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="f2578-446">Account number</span></span> | <span data-ttu-id="f2578-447">Vrstva</span><span class="sxs-lookup"><span data-stu-id="f2578-447">Layer</span></span>  | <span data-ttu-id="f2578-448">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="f2578-448">Account description</span></span> | <span data-ttu-id="f2578-449">Debet</span><span class="sxs-lookup"><span data-stu-id="f2578-449">Debit</span></span>    | <span data-ttu-id="f2578-450">Kredit</span><span class="sxs-lookup"><span data-stu-id="f2578-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="f2578-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="f2578-451">Ledger</span></span>       | <span data-ttu-id="f2578-452">4</span><span class="sxs-lookup"><span data-stu-id="f2578-452">4</span></span>              | <span data-ttu-id="f2578-453">Vlastní</span><span class="sxs-lookup"><span data-stu-id="f2578-453">Custom</span></span> | <span data-ttu-id="f2578-454">Clearingový účet</span><span class="sxs-lookup"><span data-stu-id="f2578-454">Clearing account</span></span>    | <span data-ttu-id="f2578-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="f2578-455">1,000.00</span></span> |          |
| <span data-ttu-id="f2578-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="f2578-456">Ledger</span></span>       | <span data-ttu-id="f2578-457">1</span><span class="sxs-lookup"><span data-stu-id="f2578-457">1</span></span>              | <span data-ttu-id="f2578-458">Vlastní</span><span class="sxs-lookup"><span data-stu-id="f2578-458">Custom</span></span> | <span data-ttu-id="f2578-459">Výdaje leasingu</span><span class="sxs-lookup"><span data-stu-id="f2578-459">Lease expense</span></span>       |          | <span data-ttu-id="f2578-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="f2578-460">1,000.00</span></span> |

<span data-ttu-id="f2578-461">Nyní, když jste vyloučili položky statutárního deníku, zarezervujete všechny položky deníku, které vyžadují IFRS 16 v knize IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="f2578-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="f2578-462">Mezi tyto položky patří počáteční uznání používaného majetku a záznam úroků a odpisů.</span><span class="sxs-lookup"><span data-stu-id="f2578-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="f2578-463">Počáteční uznání – 1. 1. 2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="f2578-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="f2578-464">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="f2578-464">Account type</span></span> | <span data-ttu-id="f2578-465">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="f2578-465">Account number</span></span> | <span data-ttu-id="f2578-466">Vrstva</span><span class="sxs-lookup"><span data-stu-id="f2578-466">Layer</span></span>  | <span data-ttu-id="f2578-467">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="f2578-467">Account description</span></span>      | <span data-ttu-id="f2578-468">Debet</span><span class="sxs-lookup"><span data-stu-id="f2578-468">Debit</span></span>     | <span data-ttu-id="f2578-469">Kredit</span><span class="sxs-lookup"><span data-stu-id="f2578-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="f2578-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="f2578-470">Ledger</span></span>       | <span data-ttu-id="f2578-471">6</span><span class="sxs-lookup"><span data-stu-id="f2578-471">6</span></span>              | <span data-ttu-id="f2578-472">Vlastní</span><span class="sxs-lookup"><span data-stu-id="f2578-472">Custom</span></span> | <span data-ttu-id="f2578-473">Používaný majetek</span><span class="sxs-lookup"><span data-stu-id="f2578-473">ROU Asset</span></span>                | <span data-ttu-id="f2578-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="f2578-474">22,793.90</span></span> |           |
| <span data-ttu-id="f2578-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="f2578-475">Ledger</span></span>       | <span data-ttu-id="f2578-476">7</span><span class="sxs-lookup"><span data-stu-id="f2578-476">7</span></span>              | <span data-ttu-id="f2578-477">Vlastní</span><span class="sxs-lookup"><span data-stu-id="f2578-477">Custom</span></span> | <span data-ttu-id="f2578-478">Povinnost finančního leasingu</span><span class="sxs-lookup"><span data-stu-id="f2578-478">Finance lease obligation</span></span> |           | <span data-ttu-id="f2578-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="f2578-479">22,793.90</span></span> |

<span data-ttu-id="f2578-480">Leasingová splátka je zaúčtována jako ostatní leasingové splátky.</span><span class="sxs-lookup"><span data-stu-id="f2578-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="f2578-481">Důvodem pro použití clearingového účtu je zajistit, aby byla hotovost připsána pouze jednou.</span><span class="sxs-lookup"><span data-stu-id="f2578-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="f2578-482">Leasingová splátka – 31. 1. 2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="f2578-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="f2578-483">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="f2578-483">Account type</span></span> | <span data-ttu-id="f2578-484">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="f2578-484">Account number</span></span> | <span data-ttu-id="f2578-485">Vrstva</span><span class="sxs-lookup"><span data-stu-id="f2578-485">Layer</span></span>  | <span data-ttu-id="f2578-486">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="f2578-486">Account description</span></span>      | <span data-ttu-id="f2578-487">Debet</span><span class="sxs-lookup"><span data-stu-id="f2578-487">Debit</span></span>    | <span data-ttu-id="f2578-488">Kredit</span><span class="sxs-lookup"><span data-stu-id="f2578-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="f2578-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="f2578-489">Ledger</span></span>       | <span data-ttu-id="f2578-490">7</span><span class="sxs-lookup"><span data-stu-id="f2578-490">7</span></span>              | <span data-ttu-id="f2578-491">Vlastní</span><span class="sxs-lookup"><span data-stu-id="f2578-491">Custom</span></span> | <span data-ttu-id="f2578-492">Povinnost finančního leasingu</span><span class="sxs-lookup"><span data-stu-id="f2578-492">Finance lease obligation</span></span> | <span data-ttu-id="f2578-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="f2578-493">1,000.00</span></span> |          |
| <span data-ttu-id="f2578-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="f2578-494">Ledger</span></span>       | <span data-ttu-id="f2578-495">4</span><span class="sxs-lookup"><span data-stu-id="f2578-495">4</span></span>              | <span data-ttu-id="f2578-496">Vlastní</span><span class="sxs-lookup"><span data-stu-id="f2578-496">Custom</span></span> | <span data-ttu-id="f2578-497">Clearingový účet</span><span class="sxs-lookup"><span data-stu-id="f2578-497">Clearing account</span></span>         |          | <span data-ttu-id="f2578-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="f2578-498">1,000.00</span></span> |

<span data-ttu-id="f2578-499">Položka deníku úrokových nákladů je generována z plánu amortizace závazků.</span><span class="sxs-lookup"><span data-stu-id="f2578-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="f2578-500">Úrokové náklady – 31. 1. 2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="f2578-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="f2578-501">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="f2578-501">Account type</span></span> | <span data-ttu-id="f2578-502">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="f2578-502">Account number</span></span> | <span data-ttu-id="f2578-503">Vrstva</span><span class="sxs-lookup"><span data-stu-id="f2578-503">Layer</span></span>  | <span data-ttu-id="f2578-504">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="f2578-504">Account description</span></span>      | <span data-ttu-id="f2578-505">Debet</span><span class="sxs-lookup"><span data-stu-id="f2578-505">Debit</span></span> | <span data-ttu-id="f2578-506">Kredit</span><span class="sxs-lookup"><span data-stu-id="f2578-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="f2578-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="f2578-507">Ledger</span></span>       | <span data-ttu-id="f2578-508">8</span><span class="sxs-lookup"><span data-stu-id="f2578-508">8</span></span>              | <span data-ttu-id="f2578-509">Vlastní</span><span class="sxs-lookup"><span data-stu-id="f2578-509">Custom</span></span> | <span data-ttu-id="f2578-510">Výdaje na úroky</span><span class="sxs-lookup"><span data-stu-id="f2578-510">Interest expense</span></span>         | <span data-ttu-id="f2578-511">94.97</span><span class="sxs-lookup"><span data-stu-id="f2578-511">94.97</span></span> |        |
| <span data-ttu-id="f2578-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="f2578-512">Ledger</span></span>       | <span data-ttu-id="f2578-513">7</span><span class="sxs-lookup"><span data-stu-id="f2578-513">7</span></span>              | <span data-ttu-id="f2578-514">Vlastní</span><span class="sxs-lookup"><span data-stu-id="f2578-514">Custom</span></span> | <span data-ttu-id="f2578-515">Povinnost finančního leasingu</span><span class="sxs-lookup"><span data-stu-id="f2578-515">Finance lease obligation</span></span> |       | <span data-ttu-id="f2578-516">94.97</span><span class="sxs-lookup"><span data-stu-id="f2578-516">94.97</span></span>  |

<span data-ttu-id="f2578-517">Položka deníku odpisových výdajů je generována z plánu odpisu majetku.</span><span class="sxs-lookup"><span data-stu-id="f2578-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="f2578-518">Odpisové výdaje – 31. 1. 2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="f2578-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="f2578-519">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="f2578-519">Account type</span></span> | <span data-ttu-id="f2578-520">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="f2578-520">Account number</span></span> | <span data-ttu-id="f2578-521">Vrstva</span><span class="sxs-lookup"><span data-stu-id="f2578-521">Layer</span></span>  | <span data-ttu-id="f2578-522">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="f2578-522">Account description</span></span>      | <span data-ttu-id="f2578-523">Debet</span><span class="sxs-lookup"><span data-stu-id="f2578-523">Debit</span></span>  | <span data-ttu-id="f2578-524">Kredit</span><span class="sxs-lookup"><span data-stu-id="f2578-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="f2578-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="f2578-525">Ledger</span></span>       | <span data-ttu-id="f2578-526">10</span><span class="sxs-lookup"><span data-stu-id="f2578-526">10</span></span>             | <span data-ttu-id="f2578-527">Vlastní</span><span class="sxs-lookup"><span data-stu-id="f2578-527">Custom</span></span> | <span data-ttu-id="f2578-528">Odpisové výdaje</span><span class="sxs-lookup"><span data-stu-id="f2578-528">Depreciation expense</span></span>     | <span data-ttu-id="f2578-529">949.75</span><span class="sxs-lookup"><span data-stu-id="f2578-529">949.75</span></span> |        |
| <span data-ttu-id="f2578-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="f2578-530">Ledger</span></span>       | <span data-ttu-id="f2578-531">11</span><span class="sxs-lookup"><span data-stu-id="f2578-531">11</span></span>             | <span data-ttu-id="f2578-532">Vlastní</span><span class="sxs-lookup"><span data-stu-id="f2578-532">Custom</span></span> | <span data-ttu-id="f2578-533">Akumulovaný odpis</span><span class="sxs-lookup"><span data-stu-id="f2578-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="f2578-534">949.75</span><span class="sxs-lookup"><span data-stu-id="f2578-534">949.75</span></span> |

<span data-ttu-id="f2578-535">Po vytvoření a zaúčtování všech těchto položek deníku se zobrazí následující hodnoty „vlastní vrstvy 1“.</span><span class="sxs-lookup"><span data-stu-id="f2578-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="f2578-536">Všimněte si, že poslední sloupec obsahuje bankovní poplatek, výdaj na daň z přidané hodnoty (DPH) a snížení hotovosti z předchozí vrstvy, ale nezahrnuje položky deníku pro statutární vykazování.</span><span class="sxs-lookup"><span data-stu-id="f2578-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="f2578-537">Proto dosáhnete skutečného využití možností duálního hlášení.</span><span class="sxs-lookup"><span data-stu-id="f2578-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="f2578-538">V tomto okamžiku musí společnost spustit předvahu a zkombinovat aktuální a vlastní vrstvu, aby vytvořila předvahu podle IFRS.</span><span class="sxs-lookup"><span data-stu-id="f2578-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="f2578-539">Č. účtu</span><span class="sxs-lookup"><span data-stu-id="f2578-539">Account No</span></span> | <span data-ttu-id="f2578-540">popis</span><span class="sxs-lookup"><span data-stu-id="f2578-540">Description</span></span>              | <span data-ttu-id="f2578-541">Statutární kniha\-Aktuální vrstva\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="f2578-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="f2578-542">Statutární kniha\-Aktuální vrstva\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="f2578-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="f2578-543">Statutární kniha\-Aktuální vrstva\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="f2578-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="f2578-544">Aktuální vrstva \- Celkem</span><span class="sxs-lookup"><span data-stu-id="f2578-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="f2578-545">Stornovací kniha\-Vlastní vrstva\-JE\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="f2578-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="f2578-546">Kniha IFRS 16\-Vlastní vrstva\-JE\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="f2578-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="f2578-547">Kniha IFRS 16\-Vlastní vrstva\-JE\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="f2578-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="f2578-548">Kniha IFRS 16\-Vlastní vrstva\-JE\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="f2578-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="f2578-549">Kniha IFRS 16\-Vlastní vrstva\-JE\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="f2578-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="f2578-550">Vlastní vrstva \+ Vlastní vrstva \- Celkem</span><span class="sxs-lookup"><span data-stu-id="f2578-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="f2578-551">1</span><span class="sxs-lookup"><span data-stu-id="f2578-551">1</span></span>          | <span data-ttu-id="f2578-552">Výdaje leasingu</span><span class="sxs-lookup"><span data-stu-id="f2578-552">Lease expense</span></span>            | <span data-ttu-id="f2578-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="f2578-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="f2578-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="f2578-554">1,000\.00</span></span>               |   | <span data-ttu-id="f2578-555">\-1000</span><span class="sxs-lookup"><span data-stu-id="f2578-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="f2578-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="f2578-556">0\.00</span></span>                                   |
| <span data-ttu-id="f2578-557">2</span><span class="sxs-lookup"><span data-stu-id="f2578-557">2</span></span>          | <span data-ttu-id="f2578-558">Bankovní poplatek</span><span class="sxs-lookup"><span data-stu-id="f2578-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="f2578-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="f2578-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="f2578-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="f2578-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="f2578-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="f2578-561">3\.00</span></span>                                   |
| <span data-ttu-id="f2578-562">3</span><span class="sxs-lookup"><span data-stu-id="f2578-562">3</span></span>          | <span data-ttu-id="f2578-563">Výdaje DPH</span><span class="sxs-lookup"><span data-stu-id="f2578-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="f2578-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="f2578-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="f2578-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="f2578-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="f2578-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="f2578-566">5\.00</span></span>                                   |
| <span data-ttu-id="f2578-567">4</span><span class="sxs-lookup"><span data-stu-id="f2578-567">4</span></span>          | <span data-ttu-id="f2578-568">Clearingový účet</span><span class="sxs-lookup"><span data-stu-id="f2578-568">Clearing account</span></span>         | <span data-ttu-id="f2578-569">\-1000\.00</span><span class="sxs-lookup"><span data-stu-id="f2578-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="f2578-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="f2578-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="f2578-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="f2578-571">0\.00</span></span>                   |   | <span data-ttu-id="f2578-572">1 000</span><span class="sxs-lookup"><span data-stu-id="f2578-572">1,000</span></span>                                           |                                                | <span data-ttu-id="f2578-573">\-1000</span><span class="sxs-lookup"><span data-stu-id="f2578-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="f2578-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="f2578-574">0\.00</span></span>                                   |
| <span data-ttu-id="f2578-575">5</span><span class="sxs-lookup"><span data-stu-id="f2578-575">5</span></span>          | <span data-ttu-id="f2578-576">Závazky</span><span class="sxs-lookup"><span data-stu-id="f2578-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="f2578-577">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="f2578-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="f2578-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="f2578-578">1,008\.00</span></span>                                         | <span data-ttu-id="f2578-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="f2578-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="f2578-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="f2578-580">0\.00</span></span>                                   |
| <span data-ttu-id="f2578-581">6</span><span class="sxs-lookup"><span data-stu-id="f2578-581">6</span></span>          | <span data-ttu-id="f2578-582">Používaný majetek</span><span class="sxs-lookup"><span data-stu-id="f2578-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="f2578-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="f2578-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="f2578-584">22,794</span><span class="sxs-lookup"><span data-stu-id="f2578-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="f2578-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="f2578-585">22,793\.90</span></span>                              |
| <span data-ttu-id="f2578-586">7</span><span class="sxs-lookup"><span data-stu-id="f2578-586">7</span></span>          | <span data-ttu-id="f2578-587">Povinnost finančního leasingu</span><span class="sxs-lookup"><span data-stu-id="f2578-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="f2578-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="f2578-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="f2578-589">\-22 794</span><span class="sxs-lookup"><span data-stu-id="f2578-589">\-22,794</span></span>                                       | <span data-ttu-id="f2578-590">1 000</span><span class="sxs-lookup"><span data-stu-id="f2578-590">1,000</span></span>                                          | <span data-ttu-id="f2578-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="f2578-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="f2578-592">\-21 888\.87</span><span class="sxs-lookup"><span data-stu-id="f2578-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="f2578-593">8</span><span class="sxs-lookup"><span data-stu-id="f2578-593">8</span></span>          | <span data-ttu-id="f2578-594">Výdaje na úroky</span><span class="sxs-lookup"><span data-stu-id="f2578-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="f2578-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="f2578-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="f2578-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="f2578-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="f2578-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="f2578-597">94\.97</span></span>                                  |
| <span data-ttu-id="f2578-598">9</span><span class="sxs-lookup"><span data-stu-id="f2578-598">9</span></span>          | <span data-ttu-id="f2578-599">Hotovost</span><span class="sxs-lookup"><span data-stu-id="f2578-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="f2578-600">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="f2578-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="f2578-601">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="f2578-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="f2578-602">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="f2578-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="f2578-603">10</span><span class="sxs-lookup"><span data-stu-id="f2578-603">10</span></span>         | <span data-ttu-id="f2578-604">Odpisové výdaje</span><span class="sxs-lookup"><span data-stu-id="f2578-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="f2578-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="f2578-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="f2578-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="f2578-606">949\.75</span></span>                                        | <span data-ttu-id="f2578-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="f2578-607">949\.75</span></span>                                 |
| <span data-ttu-id="f2578-608">11</span><span class="sxs-lookup"><span data-stu-id="f2578-608">11</span></span>         | <span data-ttu-id="f2578-609">Akumulovaný odpis</span><span class="sxs-lookup"><span data-stu-id="f2578-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="f2578-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="f2578-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="f2578-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="f2578-611">\-949\.75</span></span>                                      | <span data-ttu-id="f2578-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="f2578-612">\-949\.75</span></span>                               |


