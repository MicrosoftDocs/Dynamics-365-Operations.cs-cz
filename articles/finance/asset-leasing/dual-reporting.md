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
ms.openlocfilehash: d6daa43178625316a40427728e7e4186691cc13c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229543"
---
# <a name="dual-reporting"></a><span data-ttu-id="139de-103">Duální vykazování</span><span class="sxs-lookup"><span data-stu-id="139de-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="139de-104">Toto téma vás provede příkladem, který ukazuje, jak můžete splnit požadavky jak pro vykazování podle Mezinárodního standardu finančního výkaznictví (IFRS), tak pro statutární vykazování v leasingu majetku.</span><span class="sxs-lookup"><span data-stu-id="139de-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="139de-105">Znalost účtovacích vrstev v Microsoft Dynamics 365 Finance je nutná a příklad bude lépe srozumitelný.</span><span class="sxs-lookup"><span data-stu-id="139de-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="139de-106">Příklad</span><span class="sxs-lookup"><span data-stu-id="139de-106">Example</span></span>

<span data-ttu-id="139de-107">Následující příklad provádí účtování pro leasing podle italského statutárního výkaznictví pomocí metody hotovostního základu i metod vykazování podle IFRS.</span><span class="sxs-lookup"><span data-stu-id="139de-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="139de-108">Společnost musí založit tři účetní knihy, které zohlední jak italské zákonné požadavky, tak požadavky IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="139de-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="139de-109">Jedna kniha je vyžadována pro IFRS 16, jedna kniha je vyžadována pro zákonné požadavky a jedna kniha je vyžadována k automatickému stornování statutárních účtování.</span><span class="sxs-lookup"><span data-stu-id="139de-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="139de-110">Knihy jsou vytvořeny tak, jak je uvedeno v následujících tabulkách.</span><span class="sxs-lookup"><span data-stu-id="139de-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="139de-111">**Kniha IFRS 16**</span><span class="sxs-lookup"><span data-stu-id="139de-111">**IFRS 16 book**</span></span>

<span data-ttu-id="139de-112">Kniha IFRS 16 je vytvořena v souladu s účetním standardem IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="139de-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="139de-113">Všechny položky, které jsou zaúčtovány v této knize, budou zaúčtovány do vlastní vrstvy.</span><span class="sxs-lookup"><span data-stu-id="139de-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="139de-114">Jméno</span><span class="sxs-lookup"><span data-stu-id="139de-114">Name</span></span>                                    | <span data-ttu-id="139de-115">popis</span><span class="sxs-lookup"><span data-stu-id="139de-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="139de-116">Typ knihy</span><span class="sxs-lookup"><span data-stu-id="139de-116">Book type</span></span>                               | <span data-ttu-id="139de-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="139de-117">IFRS 16</span></span>        |
| <span data-ttu-id="139de-118">Popis knihy</span><span class="sxs-lookup"><span data-stu-id="139de-118">Book description</span></span>                        | <span data-ttu-id="139de-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="139de-119">IFRS 16</span></span>        |
| <span data-ttu-id="139de-120">Účtovací vrstva</span><span class="sxs-lookup"><span data-stu-id="139de-120">Posting Layer</span></span>                           | <span data-ttu-id="139de-121">Vlastní vrstva 1</span><span class="sxs-lookup"><span data-stu-id="139de-121">Custom layer 1</span></span> |
| <span data-ttu-id="139de-122">Typ leasingu</span><span class="sxs-lookup"><span data-stu-id="139de-122">Lease Type</span></span>                              | <span data-ttu-id="139de-123">Finance</span><span class="sxs-lookup"><span data-stu-id="139de-123">Finance</span></span>        |
| <span data-ttu-id="139de-124">Rámec účetnictví</span><span class="sxs-lookup"><span data-stu-id="139de-124">Accounting Framework</span></span>                    | <span data-ttu-id="139de-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="139de-125">IFRS 16</span></span>        |
| <span data-ttu-id="139de-126">Nastavení doby trvání leasingu / očekávané doby použitelnosti</span><span class="sxs-lookup"><span data-stu-id="139de-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="139de-127">0,00</span><span class="sxs-lookup"><span data-stu-id="139de-127">0.00</span></span>           |
| <span data-ttu-id="139de-128">Nastavení současné hodnoty / reálné hodnoty majetku</span><span class="sxs-lookup"><span data-stu-id="139de-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="139de-129">0,00</span><span class="sxs-lookup"><span data-stu-id="139de-129">0.00</span></span>           |
| <span data-ttu-id="139de-130">Krátkodobá prahová hodnota</span><span class="sxs-lookup"><span data-stu-id="139de-130">Short-term threshold</span></span>                    | <span data-ttu-id="139de-131">12</span><span class="sxs-lookup"><span data-stu-id="139de-131">12</span></span>             |
| <span data-ttu-id="139de-132">Nízká prahová hodnota</span><span class="sxs-lookup"><span data-stu-id="139de-132">Low Value Threshold</span></span>                     | <span data-ttu-id="139de-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="139de-133">5,000.00</span></span>       |
| <span data-ttu-id="139de-134">Platba dodavateli</span><span class="sxs-lookup"><span data-stu-id="139de-134">Pay to Vendor</span></span>                           | <span data-ttu-id="139de-135">Žádný</span><span class="sxs-lookup"><span data-stu-id="139de-135">No</span></span>             |

<span data-ttu-id="139de-136">**Statutární kniha**</span><span class="sxs-lookup"><span data-stu-id="139de-136">**Statutory book**</span></span>

<span data-ttu-id="139de-137">Statutární kniha je hotovostní kniha, kde společnost bude účtovat výdaje na leasing jako částku hotovosti, která se každý měsíc platí za nájem.</span><span class="sxs-lookup"><span data-stu-id="139de-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="139de-138">Tato kniha nevytvoří používaný majetek ani leasingový závazek.</span><span class="sxs-lookup"><span data-stu-id="139de-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="139de-139">Jméno</span><span class="sxs-lookup"><span data-stu-id="139de-139">Name</span></span>                                    | <span data-ttu-id="139de-140">popis</span><span class="sxs-lookup"><span data-stu-id="139de-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="139de-141">Typ knihy</span><span class="sxs-lookup"><span data-stu-id="139de-141">Book type</span></span>                               | <span data-ttu-id="139de-142">Statutární</span><span class="sxs-lookup"><span data-stu-id="139de-142">Statutory</span></span>   |
| <span data-ttu-id="139de-143">Popis knihy</span><span class="sxs-lookup"><span data-stu-id="139de-143">Book description</span></span>                        | <span data-ttu-id="139de-144">Místní GAAP</span><span class="sxs-lookup"><span data-stu-id="139de-144">Local GAAP</span></span>  |
| <span data-ttu-id="139de-145">Účtovací vrstva</span><span class="sxs-lookup"><span data-stu-id="139de-145">Posting Layer</span></span>                           | <span data-ttu-id="139de-146">Aktuální</span><span class="sxs-lookup"><span data-stu-id="139de-146">Current</span></span>     |
| <span data-ttu-id="139de-147">Typ leasingu</span><span class="sxs-lookup"><span data-stu-id="139de-147">Lease Type</span></span>                              | <span data-ttu-id="139de-148">Automatické</span><span class="sxs-lookup"><span data-stu-id="139de-148">Automatic</span></span>   |
| <span data-ttu-id="139de-149">Rámec účetnictví</span><span class="sxs-lookup"><span data-stu-id="139de-149">Accounting Framework</span></span>                    | <span data-ttu-id="139de-150">Hotovostní základ</span><span class="sxs-lookup"><span data-stu-id="139de-150">Cash basis</span></span>  |
| <span data-ttu-id="139de-151">Nastavení doby trvání leasingu / očekávané doby použitelnosti</span><span class="sxs-lookup"><span data-stu-id="139de-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="139de-152">0,00</span><span class="sxs-lookup"><span data-stu-id="139de-152">0.00</span></span>        |
| <span data-ttu-id="139de-153">Nastavení současné hodnoty / reálné hodnoty majetku</span><span class="sxs-lookup"><span data-stu-id="139de-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="139de-154">0,00</span><span class="sxs-lookup"><span data-stu-id="139de-154">0.00</span></span>        |
| <span data-ttu-id="139de-155">Krátkodobá prahová hodnota</span><span class="sxs-lookup"><span data-stu-id="139de-155">Short-term threshold</span></span>                    | <span data-ttu-id="139de-156">0</span><span class="sxs-lookup"><span data-stu-id="139de-156">0</span></span>           |
| <span data-ttu-id="139de-157">Nízká prahová hodnota</span><span class="sxs-lookup"><span data-stu-id="139de-157">Low Value Threshold</span></span>                     | <span data-ttu-id="139de-158">0</span><span class="sxs-lookup"><span data-stu-id="139de-158">0</span></span>           |
| <span data-ttu-id="139de-159">Platba dodavateli</span><span class="sxs-lookup"><span data-stu-id="139de-159">Pay to Vendor</span></span>                           | <span data-ttu-id="139de-160">Žádný</span><span class="sxs-lookup"><span data-stu-id="139de-160">No</span></span>          |

<span data-ttu-id="139de-161">**Statutární stornovací kniha**</span><span class="sxs-lookup"><span data-stu-id="139de-161">**Statutory reversal book**</span></span>

<span data-ttu-id="139de-162">Statutární stornovací kniha je sestavena stejným způsobem jako statutární kniha.</span><span class="sxs-lookup"><span data-stu-id="139de-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="139de-163">Jméno</span><span class="sxs-lookup"><span data-stu-id="139de-163">Name</span></span>                                    | <span data-ttu-id="139de-164">popis</span><span class="sxs-lookup"><span data-stu-id="139de-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="139de-165">Typ knihy</span><span class="sxs-lookup"><span data-stu-id="139de-165">Book type</span></span>                               | <span data-ttu-id="139de-166">Statutární – storno</span><span class="sxs-lookup"><span data-stu-id="139de-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="139de-167">Popis knihy</span><span class="sxs-lookup"><span data-stu-id="139de-167">Book description</span></span>                        | <span data-ttu-id="139de-168">Kniha pro stornování statutární knihy</span><span class="sxs-lookup"><span data-stu-id="139de-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="139de-169">Účtovací vrstva</span><span class="sxs-lookup"><span data-stu-id="139de-169">Posting Layer</span></span>                           | <span data-ttu-id="139de-170">Vlastní vrstva 1</span><span class="sxs-lookup"><span data-stu-id="139de-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="139de-171">Typ leasingu</span><span class="sxs-lookup"><span data-stu-id="139de-171">Lease Type</span></span>                              | <span data-ttu-id="139de-172">Automatické</span><span class="sxs-lookup"><span data-stu-id="139de-172">Automatic</span></span>                      |
| <span data-ttu-id="139de-173">Rámec účetnictví</span><span class="sxs-lookup"><span data-stu-id="139de-173">Accounting Framework</span></span>                    | <span data-ttu-id="139de-174">Hotovostní základ</span><span class="sxs-lookup"><span data-stu-id="139de-174">Cash basis</span></span>                     |
| <span data-ttu-id="139de-175">Nastavení doby trvání leasingu / očekávané doby použitelnosti</span><span class="sxs-lookup"><span data-stu-id="139de-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="139de-176">0,00</span><span class="sxs-lookup"><span data-stu-id="139de-176">0.00</span></span>                           |
| <span data-ttu-id="139de-177">Nastavení současné hodnoty / reálné hodnoty majetku</span><span class="sxs-lookup"><span data-stu-id="139de-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="139de-178">0,00</span><span class="sxs-lookup"><span data-stu-id="139de-178">0.00</span></span>                           |
| <span data-ttu-id="139de-179">Krátkodobá prahová hodnota</span><span class="sxs-lookup"><span data-stu-id="139de-179">Short-term threshold</span></span>                    | <span data-ttu-id="139de-180">0</span><span class="sxs-lookup"><span data-stu-id="139de-180">0</span></span>                              |
| <span data-ttu-id="139de-181">Nízká prahová hodnota</span><span class="sxs-lookup"><span data-stu-id="139de-181">Low Value Threshold</span></span>                     | <span data-ttu-id="139de-182">0</span><span class="sxs-lookup"><span data-stu-id="139de-182">0</span></span>                              |
| <span data-ttu-id="139de-183">Platba dodavateli</span><span class="sxs-lookup"><span data-stu-id="139de-183">Pay to Vendor</span></span>                           | <span data-ttu-id="139de-184">Žádný</span><span class="sxs-lookup"><span data-stu-id="139de-184">No</span></span>                             |

<span data-ttu-id="139de-185">V tomto příkladu byl vytvořen leasing, který má následující nastavení na kartách **Obecné** a **Řádky platebního kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="139de-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="139de-186">**Karta Obecné**</span><span class="sxs-lookup"><span data-stu-id="139de-186">**General tab**</span></span>

| <span data-ttu-id="139de-187">Pole</span><span class="sxs-lookup"><span data-stu-id="139de-187">Field</span></span>                      | <span data-ttu-id="139de-188">Hodnota</span><span class="sxs-lookup"><span data-stu-id="139de-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="139de-189">Přírůstková výpůjční úroková sazba</span><span class="sxs-lookup"><span data-stu-id="139de-189">Incremental borrowing rate</span></span> | <span data-ttu-id="139de-190">5 %</span><span class="sxs-lookup"><span data-stu-id="139de-190">5%</span></span>               |
| <span data-ttu-id="139de-191">Datum zahájení</span><span class="sxs-lookup"><span data-stu-id="139de-191">Commencement date</span></span>          | <span data-ttu-id="139de-192">1. 1. 2020</span><span class="sxs-lookup"><span data-stu-id="139de-192">1/1/2020</span></span>         |
| <span data-ttu-id="139de-193">Skupina leasingu</span><span class="sxs-lookup"><span data-stu-id="139de-193">Lease group</span></span>                | <span data-ttu-id="139de-194">Budovy</span><span class="sxs-lookup"><span data-stu-id="139de-194">Buildings</span></span>        |
| <span data-ttu-id="139de-195">Dodavatel</span><span class="sxs-lookup"><span data-stu-id="139de-195">Vendor</span></span>                     | <span data-ttu-id="139de-196">1001</span><span class="sxs-lookup"><span data-stu-id="139de-196">1001</span></span>             |
| <span data-ttu-id="139de-197">Reálná hodnota majetku</span><span class="sxs-lookup"><span data-stu-id="139de-197">Fair value of the asset</span></span>    | <span data-ttu-id="139de-198">245,000</span><span class="sxs-lookup"><span data-stu-id="139de-198">245,000</span></span>          |
| <span data-ttu-id="139de-199">Očekávaná doba použitelnosti majetku</span><span class="sxs-lookup"><span data-stu-id="139de-199">Asset useful life</span></span>          | <span data-ttu-id="139de-200">120</span><span class="sxs-lookup"><span data-stu-id="139de-200">120</span></span>              |
| <span data-ttu-id="139de-201">Typ anuity</span><span class="sxs-lookup"><span data-stu-id="139de-201">Annuity type</span></span>               | <span data-ttu-id="139de-202">Běžná anuita</span><span class="sxs-lookup"><span data-stu-id="139de-202">Ordinary annuity</span></span> |
| <span data-ttu-id="139de-203">Interval úročení</span><span class="sxs-lookup"><span data-stu-id="139de-203">Compounding interval</span></span>       | <span data-ttu-id="139de-204">Měsíčně</span><span class="sxs-lookup"><span data-stu-id="139de-204">Monthly</span></span>          |

<span data-ttu-id="139de-205">**Karta Řádky platebního kalendáře**</span><span class="sxs-lookup"><span data-stu-id="139de-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="139de-206">Pole</span><span class="sxs-lookup"><span data-stu-id="139de-206">Field</span></span>             | <span data-ttu-id="139de-207">Hodnota</span><span class="sxs-lookup"><span data-stu-id="139de-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="139de-208">Počáteční datum</span><span class="sxs-lookup"><span data-stu-id="139de-208">Start date</span></span>        | <span data-ttu-id="139de-209">1. 1. 2020</span><span class="sxs-lookup"><span data-stu-id="139de-209">1/1/2020</span></span>   |
| <span data-ttu-id="139de-210">Interval období</span><span class="sxs-lookup"><span data-stu-id="139de-210">Period interval</span></span>   | <span data-ttu-id="139de-211">Měsíce</span><span class="sxs-lookup"><span data-stu-id="139de-211">Months</span></span>     |
| <span data-ttu-id="139de-212">Období</span><span class="sxs-lookup"><span data-stu-id="139de-212">Periods</span></span>           | <span data-ttu-id="139de-213">24</span><span class="sxs-lookup"><span data-stu-id="139de-213">24</span></span>         |
| <span data-ttu-id="139de-214">Koncové datum</span><span class="sxs-lookup"><span data-stu-id="139de-214">End date</span></span>          | <span data-ttu-id="139de-215">31. 12. 2020</span><span class="sxs-lookup"><span data-stu-id="139de-215">12/31/2020</span></span> |
| <span data-ttu-id="139de-216">Četnost plateb</span><span class="sxs-lookup"><span data-stu-id="139de-216">Payment frequency</span></span> | <span data-ttu-id="139de-217">Měsíčně</span><span class="sxs-lookup"><span data-stu-id="139de-217">Monthly</span></span>    |
| <span data-ttu-id="139de-218">Částka platby</span><span class="sxs-lookup"><span data-stu-id="139de-218">Payment amount</span></span>    | <span data-ttu-id="139de-219">1 000</span><span class="sxs-lookup"><span data-stu-id="139de-219">1,000</span></span>      |

<span data-ttu-id="139de-220">Chcete-li tento leasing započítat do dvou rámců, použijete aktuální účtovací vrstvu a vlastní účtovací vrstvu.</span><span class="sxs-lookup"><span data-stu-id="139de-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="139de-221">Následující tabulka ukazuje příklad každé položky deníku, která je potřeba pro věrné zobrazení financí podle každého standardu výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="139de-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="139de-222">Podrobný popis každé položky deníku pro první měsíc leasingu je poskytnut později.</span><span class="sxs-lookup"><span data-stu-id="139de-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="139de-223">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="139de-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="139de-224">popis</span><span class="sxs-lookup"><span data-stu-id="139de-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="139de-225">Statutární kniha (aktuální vrstva)</span><span class="sxs-lookup"><span data-stu-id="139de-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="139de-226">Celková aktuální vrstva</span><span class="sxs-lookup"><span data-stu-id="139de-226">Current layer total</span></span></th>
<th><span data-ttu-id="139de-227">Stornovací kniha (vlastní vrstva)</span><span class="sxs-lookup"><span data-stu-id="139de-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="139de-228">Kniha IFRS 16 (vlastní vrstva)</span><span class="sxs-lookup"><span data-stu-id="139de-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="139de-229">Aktuální vrstva + vlastní vrstva celkem</span><span class="sxs-lookup"><span data-stu-id="139de-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="139de-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="139de-230">JE-100</span></span></th>
<th><span data-ttu-id="139de-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="139de-231">JE-110</span></span></th>
<th><span data-ttu-id="139de-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="139de-232">JE-120</span></span></th>
<th><span data-ttu-id="139de-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="139de-233">JE-130</span></span></th>
<th><span data-ttu-id="139de-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="139de-234">JE-140</span></span></th>
<th><span data-ttu-id="139de-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="139de-235">JE-150</span></span></th>
<th><span data-ttu-id="139de-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="139de-236">JE-160</span></span></th>
<th><span data-ttu-id="139de-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="139de-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="139de-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="139de-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="139de-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="139de-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="139de-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="139de-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="139de-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="139de-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="139de-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="139de-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="139de-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="139de-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="139de-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="139de-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="139de-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="139de-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="139de-246">1</span><span class="sxs-lookup"><span data-stu-id="139de-246">1</span></span></td>
<td><span data-ttu-id="139de-247">Výdaje leasingu</span><span class="sxs-lookup"><span data-stu-id="139de-247">Lease expense</span></span></td>
<td><span data-ttu-id="139de-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="139de-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="139de-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="139de-249">1,000.00</span></span></td>
<td><span data-ttu-id="139de-250">−1 000,00</span><span class="sxs-lookup"><span data-stu-id="139de-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="139de-251">0,00</span><span class="sxs-lookup"><span data-stu-id="139de-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="139de-252">2</span><span class="sxs-lookup"><span data-stu-id="139de-252">2</span></span></td>
<td><span data-ttu-id="139de-253">Bankovní poplatek</span><span class="sxs-lookup"><span data-stu-id="139de-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="139de-254">3.00</span><span class="sxs-lookup"><span data-stu-id="139de-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="139de-255">3.00</span><span class="sxs-lookup"><span data-stu-id="139de-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="139de-256">3.00</span><span class="sxs-lookup"><span data-stu-id="139de-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="139de-257">3</span><span class="sxs-lookup"><span data-stu-id="139de-257">3</span></span></td>
<td><span data-ttu-id="139de-258">Výdaje DPH</span><span class="sxs-lookup"><span data-stu-id="139de-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="139de-259">5.00</span><span class="sxs-lookup"><span data-stu-id="139de-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="139de-260">5.00</span><span class="sxs-lookup"><span data-stu-id="139de-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="139de-261">5.00</span><span class="sxs-lookup"><span data-stu-id="139de-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="139de-262">4</span><span class="sxs-lookup"><span data-stu-id="139de-262">4</span></span></td>
<td><span data-ttu-id="139de-263">Clearingový účet</span><span class="sxs-lookup"><span data-stu-id="139de-263">Clearing account</span></span></td>
<td><span data-ttu-id="139de-264">−1 000,00</span><span class="sxs-lookup"><span data-stu-id="139de-264">-1,000.00</span></span></td>
<td><span data-ttu-id="139de-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="139de-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="139de-266">0,00</span><span class="sxs-lookup"><span data-stu-id="139de-266">0.00</span></span></td>
<td><span data-ttu-id="139de-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="139de-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="139de-268">−1 000,00</span><span class="sxs-lookup"><span data-stu-id="139de-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="139de-269">0,00</span><span class="sxs-lookup"><span data-stu-id="139de-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="139de-270">5</span><span class="sxs-lookup"><span data-stu-id="139de-270">5</span></span></td>
<td><span data-ttu-id="139de-271">Závazky</span><span class="sxs-lookup"><span data-stu-id="139de-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="139de-272">-1008,00</span><span class="sxs-lookup"><span data-stu-id="139de-272">-1,008.00</span></span></td>
<td><span data-ttu-id="139de-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="139de-273">1,008.00</span></span></td>
<td><span data-ttu-id="139de-274">0,00</span><span class="sxs-lookup"><span data-stu-id="139de-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="139de-275">0,00</span><span class="sxs-lookup"><span data-stu-id="139de-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="139de-276">6</span><span class="sxs-lookup"><span data-stu-id="139de-276">6</span></span></td>
<td><span data-ttu-id="139de-277">Používaný majetek</span><span class="sxs-lookup"><span data-stu-id="139de-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="139de-278">0,00</span><span class="sxs-lookup"><span data-stu-id="139de-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="139de-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="139de-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="139de-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="139de-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="139de-281">7</span><span class="sxs-lookup"><span data-stu-id="139de-281">7</span></span></td>
<td><span data-ttu-id="139de-282">Povinnost finančního leasingu</span><span class="sxs-lookup"><span data-stu-id="139de-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="139de-283">0,00</span><span class="sxs-lookup"><span data-stu-id="139de-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="139de-284">-22 794,00</span><span class="sxs-lookup"><span data-stu-id="139de-284">-22,794.00</span></span></td>
<td><span data-ttu-id="139de-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="139de-285">1,000.00</span></span></td>
<td><span data-ttu-id="139de-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="139de-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="139de-287">-21 888,87</span><span class="sxs-lookup"><span data-stu-id="139de-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="139de-288">8</span><span class="sxs-lookup"><span data-stu-id="139de-288">8</span></span></td>
<td><span data-ttu-id="139de-289">Výdaje na úroky</span><span class="sxs-lookup"><span data-stu-id="139de-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="139de-290">0,00</span><span class="sxs-lookup"><span data-stu-id="139de-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="139de-291">94.97</span><span class="sxs-lookup"><span data-stu-id="139de-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="139de-292">94.97</span><span class="sxs-lookup"><span data-stu-id="139de-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="139de-293">9</span><span class="sxs-lookup"><span data-stu-id="139de-293">9</span></span></td>
<td><span data-ttu-id="139de-294">Hotovost</span><span class="sxs-lookup"><span data-stu-id="139de-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="139de-295">-1008,00</span><span class="sxs-lookup"><span data-stu-id="139de-295">-1,008.00</span></span></td>
<td><span data-ttu-id="139de-296">-1008,00</span><span class="sxs-lookup"><span data-stu-id="139de-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="139de-297">-1008,00</span><span class="sxs-lookup"><span data-stu-id="139de-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="139de-298">10</span><span class="sxs-lookup"><span data-stu-id="139de-298">10</span></span></td>
<td><span data-ttu-id="139de-299">Odpisové výdaje</span><span class="sxs-lookup"><span data-stu-id="139de-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="139de-300">0,00</span><span class="sxs-lookup"><span data-stu-id="139de-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="139de-301">949.75</span><span class="sxs-lookup"><span data-stu-id="139de-301">949.75</span></span></td>
<td><span data-ttu-id="139de-302">949.75</span><span class="sxs-lookup"><span data-stu-id="139de-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="139de-303">11</span><span class="sxs-lookup"><span data-stu-id="139de-303">11</span></span></td>
<td><span data-ttu-id="139de-304">Akumulovaný odpis</span><span class="sxs-lookup"><span data-stu-id="139de-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="139de-305">0,00</span><span class="sxs-lookup"><span data-stu-id="139de-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="139de-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="139de-306">-949.75</span></span></td>
<td><span data-ttu-id="139de-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="139de-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="139de-308">Jak ukazuje předchozí tabulka, jsou potřeba tři knihy pro vykazování v rámci statutárního výkaznictví i výkaznictví podle IFRS.</span><span class="sxs-lookup"><span data-stu-id="139de-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="139de-309">Statutární kniha zaznamenává leasingové splátky podle pravidel pro hotovostní účetnictví v aktuální vrstvě.</span><span class="sxs-lookup"><span data-stu-id="139de-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="139de-310">Statutární stornovací kniha stornuje položky statutárního deníku.</span><span class="sxs-lookup"><span data-stu-id="139de-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="139de-311">Kniha IFRS 16 vytváří položky deníku, které jsou vyžadovány podle IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="139de-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="139de-312">Leasing musíte zadat pouze jednou.</span><span class="sxs-lookup"><span data-stu-id="139de-312">You must enter a lease only one time.</span></span> <span data-ttu-id="139de-313">Poté můžete otevřít stránku **Knihy**, kde jsou všechny knihy, které jsou přidruženy k leasingu.</span><span class="sxs-lookup"><span data-stu-id="139de-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="139de-314">Když vytvoříte knihy, všechny tři musí být přidruženy ke stejnému záznamu leasingu.</span><span class="sxs-lookup"><span data-stu-id="139de-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="139de-315">První položka deníku zaznamenává výdaje na leasing podle statutární knihy.</span><span class="sxs-lookup"><span data-stu-id="139de-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="139de-316">Platby můžete vytvářet v dávce nebo výběrem platebního kalendáře ve statutární knize.</span><span class="sxs-lookup"><span data-stu-id="139de-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="139de-317">V tomto příkladu se pro statutární knihu z platebního kalendáře vytvoří následující položka deníku.</span><span class="sxs-lookup"><span data-stu-id="139de-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="139de-318">Leasingová splátka – 31. 1. 2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="139de-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="139de-319">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="139de-319">Account type</span></span> | <span data-ttu-id="139de-320">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="139de-320">Account number</span></span> | <span data-ttu-id="139de-321">Vrstva</span><span class="sxs-lookup"><span data-stu-id="139de-321">Layer</span></span>   | <span data-ttu-id="139de-322">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="139de-322">Account description</span></span> | <span data-ttu-id="139de-323">Debet</span><span class="sxs-lookup"><span data-stu-id="139de-323">Debit</span></span>    | <span data-ttu-id="139de-324">Kredit</span><span class="sxs-lookup"><span data-stu-id="139de-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="139de-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="139de-325">Ledger</span></span>       | <span data-ttu-id="139de-326">1</span><span class="sxs-lookup"><span data-stu-id="139de-326">1</span></span>              | <span data-ttu-id="139de-327">Aktuální</span><span class="sxs-lookup"><span data-stu-id="139de-327">Current</span></span> | <span data-ttu-id="139de-328">Výdaje leasingu</span><span class="sxs-lookup"><span data-stu-id="139de-328">Lease expense</span></span>       | <span data-ttu-id="139de-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="139de-329">1,000.00</span></span> |          |
| <span data-ttu-id="139de-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="139de-330">Ledger</span></span>       | <span data-ttu-id="139de-331">4</span><span class="sxs-lookup"><span data-stu-id="139de-331">4</span></span>              | <span data-ttu-id="139de-332">Aktuální</span><span class="sxs-lookup"><span data-stu-id="139de-332">Current</span></span> | <span data-ttu-id="139de-333">Clearingový účet</span><span class="sxs-lookup"><span data-stu-id="139de-333">Clearing account</span></span>    |          | <span data-ttu-id="139de-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="139de-334">1,000.00</span></span> |

<span data-ttu-id="139de-335">Úředník pro závazky používá standardní funkce Dynamics 365 k vytvoření fakturu pro zaplacení leasingu mimo leasing majetku.</span><span class="sxs-lookup"><span data-stu-id="139de-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="139de-336">Nicméně místo výběru **Výdaje na leasing** jako debetního účtu vybere clearingový účet pro vygenerování následující položky.</span><span class="sxs-lookup"><span data-stu-id="139de-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="139de-337">Proces AP – 31. 1. 2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="139de-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="139de-338">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="139de-338">Account type</span></span> | <span data-ttu-id="139de-339">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="139de-339">Account number</span></span> | <span data-ttu-id="139de-340">Vrstva</span><span class="sxs-lookup"><span data-stu-id="139de-340">Layer</span></span>   | <span data-ttu-id="139de-341">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="139de-341">Account description</span></span> | <span data-ttu-id="139de-342">Debet</span><span class="sxs-lookup"><span data-stu-id="139de-342">Debit</span></span>    | <span data-ttu-id="139de-343">Kredit</span><span class="sxs-lookup"><span data-stu-id="139de-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="139de-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="139de-344">Ledger</span></span>       | <span data-ttu-id="139de-345">4</span><span class="sxs-lookup"><span data-stu-id="139de-345">4</span></span>              | <span data-ttu-id="139de-346">Aktuální</span><span class="sxs-lookup"><span data-stu-id="139de-346">Current</span></span> | <span data-ttu-id="139de-347">Clearingový účet</span><span class="sxs-lookup"><span data-stu-id="139de-347">Clearing account</span></span>    | <span data-ttu-id="139de-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="139de-348">1,000.00</span></span> |          |
| <span data-ttu-id="139de-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="139de-349">Ledger</span></span>       | <span data-ttu-id="139de-350">2</span><span class="sxs-lookup"><span data-stu-id="139de-350">2</span></span>              | <span data-ttu-id="139de-351">Aktuální</span><span class="sxs-lookup"><span data-stu-id="139de-351">Current</span></span> | <span data-ttu-id="139de-352">Bankovní poplatek</span><span class="sxs-lookup"><span data-stu-id="139de-352">Bank fee</span></span>            | <span data-ttu-id="139de-353">3.00</span><span class="sxs-lookup"><span data-stu-id="139de-353">3.00</span></span>     |          |
| <span data-ttu-id="139de-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="139de-354">Ledger</span></span>       | <span data-ttu-id="139de-355">3</span><span class="sxs-lookup"><span data-stu-id="139de-355">3</span></span>              | <span data-ttu-id="139de-356">Aktuální</span><span class="sxs-lookup"><span data-stu-id="139de-356">Current</span></span> | <span data-ttu-id="139de-357">Výdaje DPH</span><span class="sxs-lookup"><span data-stu-id="139de-357">VAT expense</span></span>         | <span data-ttu-id="139de-358">5.00</span><span class="sxs-lookup"><span data-stu-id="139de-358">5.00</span></span>     |          |
| <span data-ttu-id="139de-359">Dodavatel</span><span class="sxs-lookup"><span data-stu-id="139de-359">Vendor</span></span>       | <span data-ttu-id="139de-360">5</span><span class="sxs-lookup"><span data-stu-id="139de-360">5</span></span>              | <span data-ttu-id="139de-361">Aktuální</span><span class="sxs-lookup"><span data-stu-id="139de-361">Current</span></span> | <span data-ttu-id="139de-362">Závazky</span><span class="sxs-lookup"><span data-stu-id="139de-362">Accounts payable</span></span>    |          | <span data-ttu-id="139de-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="139de-363">1,008.00</span></span> |

<span data-ttu-id="139de-364">Když je prodejci vystaven výpis, postupujete podle pravidelného platebního procesu.</span><span class="sxs-lookup"><span data-stu-id="139de-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="139de-365">Během tohoto procesu je vygenerována následující položka deníku.</span><span class="sxs-lookup"><span data-stu-id="139de-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="139de-366">Platba v hotovosti – 31. 1. 2020 – 120</span><span class="sxs-lookup"><span data-stu-id="139de-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="139de-367">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="139de-367">Account type</span></span> | <span data-ttu-id="139de-368">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="139de-368">Account number</span></span> | <span data-ttu-id="139de-369">Vrstva</span><span class="sxs-lookup"><span data-stu-id="139de-369">Layer</span></span>   | <span data-ttu-id="139de-370">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="139de-370">Account description</span></span> | <span data-ttu-id="139de-371">Debet</span><span class="sxs-lookup"><span data-stu-id="139de-371">Debit</span></span>    | <span data-ttu-id="139de-372">Kredit</span><span class="sxs-lookup"><span data-stu-id="139de-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="139de-373">Dodavatel</span><span class="sxs-lookup"><span data-stu-id="139de-373">Vendor</span></span>       | <span data-ttu-id="139de-374">5</span><span class="sxs-lookup"><span data-stu-id="139de-374">5</span></span>              | <span data-ttu-id="139de-375">Aktuální</span><span class="sxs-lookup"><span data-stu-id="139de-375">Current</span></span> | <span data-ttu-id="139de-376">Závazky</span><span class="sxs-lookup"><span data-stu-id="139de-376">Accounts Payable</span></span>    | <span data-ttu-id="139de-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="139de-377">1,008.00</span></span> |          |
| <span data-ttu-id="139de-378">Banka</span><span class="sxs-lookup"><span data-stu-id="139de-378">Bank</span></span>         | <span data-ttu-id="139de-379">9</span><span class="sxs-lookup"><span data-stu-id="139de-379">9</span></span>              | <span data-ttu-id="139de-380">Aktuální</span><span class="sxs-lookup"><span data-stu-id="139de-380">Current</span></span> | <span data-ttu-id="139de-381">Hotovost</span><span class="sxs-lookup"><span data-stu-id="139de-381">Cash</span></span>                |          | <span data-ttu-id="139de-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="139de-382">1,008.00</span></span> |

<span data-ttu-id="139de-383">V tomto okamžiku jste plně zaúčtovali tento leasing podle zákonných požadavků na výkaznictví a můžete vygenerovat předvahu pomocí aktuální vrstvy.</span><span class="sxs-lookup"><span data-stu-id="139de-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="139de-384">Systém vrátí předvahu s následujícími čísly.</span><span class="sxs-lookup"><span data-stu-id="139de-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="139de-385">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="139de-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="139de-386">popis</span><span class="sxs-lookup"><span data-stu-id="139de-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="139de-387">Statutární kniha (aktuální vrstva)</span><span class="sxs-lookup"><span data-stu-id="139de-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="139de-388">Celková aktuální vrstva</span><span class="sxs-lookup"><span data-stu-id="139de-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="139de-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="139de-389">JE-100</span></span></th>
<th><span data-ttu-id="139de-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="139de-390">JE-110</span></span></th>
<th><span data-ttu-id="139de-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="139de-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="139de-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="139de-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="139de-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="139de-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="139de-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="139de-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="139de-395">1</span><span class="sxs-lookup"><span data-stu-id="139de-395">1</span></span></td>
<td><span data-ttu-id="139de-396">Výdaje leasingu</span><span class="sxs-lookup"><span data-stu-id="139de-396">Lease expense</span></span></td>
<td><span data-ttu-id="139de-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="139de-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="139de-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="139de-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="139de-399">2</span><span class="sxs-lookup"><span data-stu-id="139de-399">2</span></span></td>
<td><span data-ttu-id="139de-400">Bankovní poplatek</span><span class="sxs-lookup"><span data-stu-id="139de-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="139de-401">3.00</span><span class="sxs-lookup"><span data-stu-id="139de-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="139de-402">3.00</span><span class="sxs-lookup"><span data-stu-id="139de-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="139de-403">3</span><span class="sxs-lookup"><span data-stu-id="139de-403">3</span></span></td>
<td><span data-ttu-id="139de-404">Výdaje DPH</span><span class="sxs-lookup"><span data-stu-id="139de-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="139de-405">5.00</span><span class="sxs-lookup"><span data-stu-id="139de-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="139de-406">5.00</span><span class="sxs-lookup"><span data-stu-id="139de-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="139de-407">4</span><span class="sxs-lookup"><span data-stu-id="139de-407">4</span></span></td>
<td><span data-ttu-id="139de-408">Clearingový účet</span><span class="sxs-lookup"><span data-stu-id="139de-408">Clearing account</span></span></td>
<td><span data-ttu-id="139de-409">−1 000,00</span><span class="sxs-lookup"><span data-stu-id="139de-409">-1,000.00</span></span></td>
<td><span data-ttu-id="139de-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="139de-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="139de-411">0,00</span><span class="sxs-lookup"><span data-stu-id="139de-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="139de-412">5</span><span class="sxs-lookup"><span data-stu-id="139de-412">5</span></span></td>
<td><span data-ttu-id="139de-413">Závazky</span><span class="sxs-lookup"><span data-stu-id="139de-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="139de-414">-1008,00</span><span class="sxs-lookup"><span data-stu-id="139de-414">-1,008.00</span></span></td>
<td><span data-ttu-id="139de-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="139de-415">1,008.00</span></span></td>
<td><span data-ttu-id="139de-416">0,00</span><span class="sxs-lookup"><span data-stu-id="139de-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="139de-417">6</span><span class="sxs-lookup"><span data-stu-id="139de-417">6</span></span></td>
<td><span data-ttu-id="139de-418">Používaný majetek</span><span class="sxs-lookup"><span data-stu-id="139de-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="139de-419">0,00</span><span class="sxs-lookup"><span data-stu-id="139de-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="139de-420">7</span><span class="sxs-lookup"><span data-stu-id="139de-420">7</span></span></td>
<td><span data-ttu-id="139de-421">Povinnost finančního leasingu</span><span class="sxs-lookup"><span data-stu-id="139de-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="139de-422">0,00</span><span class="sxs-lookup"><span data-stu-id="139de-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="139de-423">8</span><span class="sxs-lookup"><span data-stu-id="139de-423">8</span></span></td>
<td><span data-ttu-id="139de-424">Výdaje na úroky</span><span class="sxs-lookup"><span data-stu-id="139de-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="139de-425">0,00</span><span class="sxs-lookup"><span data-stu-id="139de-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="139de-426">9</span><span class="sxs-lookup"><span data-stu-id="139de-426">9</span></span></td>
<td><span data-ttu-id="139de-427">Hotovost</span><span class="sxs-lookup"><span data-stu-id="139de-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="139de-428">-1008,00</span><span class="sxs-lookup"><span data-stu-id="139de-428">-1,008.00</span></span></td>
<td><span data-ttu-id="139de-429">-1008,00</span><span class="sxs-lookup"><span data-stu-id="139de-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="139de-430">10</span><span class="sxs-lookup"><span data-stu-id="139de-430">10</span></span></td>
<td><span data-ttu-id="139de-431">Odpisové výdaje</span><span class="sxs-lookup"><span data-stu-id="139de-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="139de-432">0,00</span><span class="sxs-lookup"><span data-stu-id="139de-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="139de-433">11</span><span class="sxs-lookup"><span data-stu-id="139de-433">11</span></span></td>
<td><span data-ttu-id="139de-434">Akumulovaný odpis</span><span class="sxs-lookup"><span data-stu-id="139de-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="139de-435">0,00</span><span class="sxs-lookup"><span data-stu-id="139de-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="139de-436">Pokud chcete použít čísla IFRS 16 ke spuštění stejné předvahy, musí být položky deníku statutárního účtování stornovány a položky deníku IFRS 16 musí být zaúčtovány.</span><span class="sxs-lookup"><span data-stu-id="139de-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="139de-437">Chcete-li stornovat položky statutárního deníku, tento příklad obsahuje statutární stornovací knihu, která má stejné nastavení jako statutární kniha, ale má opačný profil účtování.</span><span class="sxs-lookup"><span data-stu-id="139de-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="139de-438">Například statutární kniha *debetovala* účet výdaje na leasing, ale stornovací kniha bude tento účet *kreditovat*.</span><span class="sxs-lookup"><span data-stu-id="139de-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="139de-439">Tyto vztahy lze snadno definovat v účtech pro zaúčtování leasingu majetku na stránce **Parametry leasingu majetku** (**Leasing majetku \> Nastavení \> Parametry leasingu majetku**).</span><span class="sxs-lookup"><span data-stu-id="139de-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="139de-440">Když se pro stornovací knihu použije stejný proces, který byl použit pro statutární knihu, vytvoří se následující položka deníku.</span><span class="sxs-lookup"><span data-stu-id="139de-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="139de-441">Rozdíl je v tom, že stornovací kniha rezervuje stornované položky ze statutární knihy.</span><span class="sxs-lookup"><span data-stu-id="139de-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="139de-442">Stornování položek se provede také ve vlastní vrstvě.</span><span class="sxs-lookup"><span data-stu-id="139de-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="139de-443">Když je na aktuální vrstvě spuštěna předvaha, stornované položky deníku nejsou zahrnuty.</span><span class="sxs-lookup"><span data-stu-id="139de-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="139de-444">Leasingová splátka – 31. 1. 2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="139de-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="139de-445">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="139de-445">Account type</span></span> | <span data-ttu-id="139de-446">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="139de-446">Account number</span></span> | <span data-ttu-id="139de-447">Vrstva</span><span class="sxs-lookup"><span data-stu-id="139de-447">Layer</span></span>  | <span data-ttu-id="139de-448">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="139de-448">Account description</span></span> | <span data-ttu-id="139de-449">Debet</span><span class="sxs-lookup"><span data-stu-id="139de-449">Debit</span></span>    | <span data-ttu-id="139de-450">Kredit</span><span class="sxs-lookup"><span data-stu-id="139de-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="139de-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="139de-451">Ledger</span></span>       | <span data-ttu-id="139de-452">4</span><span class="sxs-lookup"><span data-stu-id="139de-452">4</span></span>              | <span data-ttu-id="139de-453">Vlastní</span><span class="sxs-lookup"><span data-stu-id="139de-453">Custom</span></span> | <span data-ttu-id="139de-454">Clearingový účet</span><span class="sxs-lookup"><span data-stu-id="139de-454">Clearing account</span></span>    | <span data-ttu-id="139de-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="139de-455">1,000.00</span></span> |          |
| <span data-ttu-id="139de-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="139de-456">Ledger</span></span>       | <span data-ttu-id="139de-457">1</span><span class="sxs-lookup"><span data-stu-id="139de-457">1</span></span>              | <span data-ttu-id="139de-458">Vlastní</span><span class="sxs-lookup"><span data-stu-id="139de-458">Custom</span></span> | <span data-ttu-id="139de-459">Výdaje leasingu</span><span class="sxs-lookup"><span data-stu-id="139de-459">Lease expense</span></span>       |          | <span data-ttu-id="139de-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="139de-460">1,000.00</span></span> |

<span data-ttu-id="139de-461">Nyní, když jste vyloučili položky statutárního deníku, zarezervujete všechny položky deníku, které vyžadují IFRS 16 v knize IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="139de-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="139de-462">Mezi tyto položky patří počáteční uznání používaného majetku a záznam úroků a odpisů.</span><span class="sxs-lookup"><span data-stu-id="139de-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="139de-463">Počáteční uznání – 1. 1. 2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="139de-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="139de-464">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="139de-464">Account type</span></span> | <span data-ttu-id="139de-465">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="139de-465">Account number</span></span> | <span data-ttu-id="139de-466">Vrstva</span><span class="sxs-lookup"><span data-stu-id="139de-466">Layer</span></span>  | <span data-ttu-id="139de-467">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="139de-467">Account description</span></span>      | <span data-ttu-id="139de-468">Debet</span><span class="sxs-lookup"><span data-stu-id="139de-468">Debit</span></span>     | <span data-ttu-id="139de-469">Kredit</span><span class="sxs-lookup"><span data-stu-id="139de-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="139de-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="139de-470">Ledger</span></span>       | <span data-ttu-id="139de-471">6</span><span class="sxs-lookup"><span data-stu-id="139de-471">6</span></span>              | <span data-ttu-id="139de-472">Vlastní</span><span class="sxs-lookup"><span data-stu-id="139de-472">Custom</span></span> | <span data-ttu-id="139de-473">Používaný majetek</span><span class="sxs-lookup"><span data-stu-id="139de-473">ROU Asset</span></span>                | <span data-ttu-id="139de-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="139de-474">22,793.90</span></span> |           |
| <span data-ttu-id="139de-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="139de-475">Ledger</span></span>       | <span data-ttu-id="139de-476">7</span><span class="sxs-lookup"><span data-stu-id="139de-476">7</span></span>              | <span data-ttu-id="139de-477">Vlastní</span><span class="sxs-lookup"><span data-stu-id="139de-477">Custom</span></span> | <span data-ttu-id="139de-478">Povinnost finančního leasingu</span><span class="sxs-lookup"><span data-stu-id="139de-478">Finance lease obligation</span></span> |           | <span data-ttu-id="139de-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="139de-479">22,793.90</span></span> |

<span data-ttu-id="139de-480">Leasingová splátka je zaúčtována jako ostatní leasingové splátky.</span><span class="sxs-lookup"><span data-stu-id="139de-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="139de-481">Důvodem pro použití clearingového účtu je zajistit, aby byla hotovost připsána pouze jednou.</span><span class="sxs-lookup"><span data-stu-id="139de-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="139de-482">Leasingová splátka – 31. 1. 2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="139de-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="139de-483">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="139de-483">Account type</span></span> | <span data-ttu-id="139de-484">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="139de-484">Account number</span></span> | <span data-ttu-id="139de-485">Vrstva</span><span class="sxs-lookup"><span data-stu-id="139de-485">Layer</span></span>  | <span data-ttu-id="139de-486">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="139de-486">Account description</span></span>      | <span data-ttu-id="139de-487">Debet</span><span class="sxs-lookup"><span data-stu-id="139de-487">Debit</span></span>    | <span data-ttu-id="139de-488">Kredit</span><span class="sxs-lookup"><span data-stu-id="139de-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="139de-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="139de-489">Ledger</span></span>       | <span data-ttu-id="139de-490">7</span><span class="sxs-lookup"><span data-stu-id="139de-490">7</span></span>              | <span data-ttu-id="139de-491">Vlastní</span><span class="sxs-lookup"><span data-stu-id="139de-491">Custom</span></span> | <span data-ttu-id="139de-492">Povinnost finančního leasingu</span><span class="sxs-lookup"><span data-stu-id="139de-492">Finance lease obligation</span></span> | <span data-ttu-id="139de-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="139de-493">1,000.00</span></span> |          |
| <span data-ttu-id="139de-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="139de-494">Ledger</span></span>       | <span data-ttu-id="139de-495">4</span><span class="sxs-lookup"><span data-stu-id="139de-495">4</span></span>              | <span data-ttu-id="139de-496">Vlastní</span><span class="sxs-lookup"><span data-stu-id="139de-496">Custom</span></span> | <span data-ttu-id="139de-497">Clearingový účet</span><span class="sxs-lookup"><span data-stu-id="139de-497">Clearing account</span></span>         |          | <span data-ttu-id="139de-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="139de-498">1,000.00</span></span> |

<span data-ttu-id="139de-499">Položka deníku úrokových nákladů je generována z plánu amortizace závazků.</span><span class="sxs-lookup"><span data-stu-id="139de-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="139de-500">Úrokové náklady – 31. 1. 2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="139de-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="139de-501">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="139de-501">Account type</span></span> | <span data-ttu-id="139de-502">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="139de-502">Account number</span></span> | <span data-ttu-id="139de-503">Vrstva</span><span class="sxs-lookup"><span data-stu-id="139de-503">Layer</span></span>  | <span data-ttu-id="139de-504">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="139de-504">Account description</span></span>      | <span data-ttu-id="139de-505">Debet</span><span class="sxs-lookup"><span data-stu-id="139de-505">Debit</span></span> | <span data-ttu-id="139de-506">Kredit</span><span class="sxs-lookup"><span data-stu-id="139de-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="139de-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="139de-507">Ledger</span></span>       | <span data-ttu-id="139de-508">8</span><span class="sxs-lookup"><span data-stu-id="139de-508">8</span></span>              | <span data-ttu-id="139de-509">Vlastní</span><span class="sxs-lookup"><span data-stu-id="139de-509">Custom</span></span> | <span data-ttu-id="139de-510">Výdaje na úroky</span><span class="sxs-lookup"><span data-stu-id="139de-510">Interest expense</span></span>         | <span data-ttu-id="139de-511">94.97</span><span class="sxs-lookup"><span data-stu-id="139de-511">94.97</span></span> |        |
| <span data-ttu-id="139de-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="139de-512">Ledger</span></span>       | <span data-ttu-id="139de-513">7</span><span class="sxs-lookup"><span data-stu-id="139de-513">7</span></span>              | <span data-ttu-id="139de-514">Vlastní</span><span class="sxs-lookup"><span data-stu-id="139de-514">Custom</span></span> | <span data-ttu-id="139de-515">Povinnost finančního leasingu</span><span class="sxs-lookup"><span data-stu-id="139de-515">Finance lease obligation</span></span> |       | <span data-ttu-id="139de-516">94.97</span><span class="sxs-lookup"><span data-stu-id="139de-516">94.97</span></span>  |

<span data-ttu-id="139de-517">Položka deníku odpisových výdajů je generována z plánu odpisu majetku.</span><span class="sxs-lookup"><span data-stu-id="139de-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="139de-518">Odpisové výdaje – 31. 1. 2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="139de-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="139de-519">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="139de-519">Account type</span></span> | <span data-ttu-id="139de-520">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="139de-520">Account number</span></span> | <span data-ttu-id="139de-521">Vrstva</span><span class="sxs-lookup"><span data-stu-id="139de-521">Layer</span></span>  | <span data-ttu-id="139de-522">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="139de-522">Account description</span></span>      | <span data-ttu-id="139de-523">Debet</span><span class="sxs-lookup"><span data-stu-id="139de-523">Debit</span></span>  | <span data-ttu-id="139de-524">Kredit</span><span class="sxs-lookup"><span data-stu-id="139de-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="139de-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="139de-525">Ledger</span></span>       | <span data-ttu-id="139de-526">10</span><span class="sxs-lookup"><span data-stu-id="139de-526">10</span></span>             | <span data-ttu-id="139de-527">Vlastní</span><span class="sxs-lookup"><span data-stu-id="139de-527">Custom</span></span> | <span data-ttu-id="139de-528">Odpisové výdaje</span><span class="sxs-lookup"><span data-stu-id="139de-528">Depreciation expense</span></span>     | <span data-ttu-id="139de-529">949.75</span><span class="sxs-lookup"><span data-stu-id="139de-529">949.75</span></span> |        |
| <span data-ttu-id="139de-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="139de-530">Ledger</span></span>       | <span data-ttu-id="139de-531">11</span><span class="sxs-lookup"><span data-stu-id="139de-531">11</span></span>             | <span data-ttu-id="139de-532">Vlastní</span><span class="sxs-lookup"><span data-stu-id="139de-532">Custom</span></span> | <span data-ttu-id="139de-533">Akumulovaný odpis</span><span class="sxs-lookup"><span data-stu-id="139de-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="139de-534">949.75</span><span class="sxs-lookup"><span data-stu-id="139de-534">949.75</span></span> |

<span data-ttu-id="139de-535">Po vytvoření a zaúčtování všech těchto položek deníku se zobrazí následující hodnoty „vlastní vrstvy 1“.</span><span class="sxs-lookup"><span data-stu-id="139de-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="139de-536">Všimněte si, že poslední sloupec obsahuje bankovní poplatek, výdaj na daň z přidané hodnoty (DPH) a snížení hotovosti z předchozí vrstvy, ale nezahrnuje položky deníku pro statutární vykazování.</span><span class="sxs-lookup"><span data-stu-id="139de-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="139de-537">Proto dosáhnete skutečného využití možností duálního hlášení.</span><span class="sxs-lookup"><span data-stu-id="139de-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="139de-538">V tomto okamžiku musí společnost spustit předvahu a zkombinovat aktuální a vlastní vrstvu, aby vytvořila předvahu podle IFRS.</span><span class="sxs-lookup"><span data-stu-id="139de-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="139de-539">Č. účtu</span><span class="sxs-lookup"><span data-stu-id="139de-539">Account No</span></span> | <span data-ttu-id="139de-540">popis</span><span class="sxs-lookup"><span data-stu-id="139de-540">Description</span></span>              | <span data-ttu-id="139de-541">Statutární kniha\-Aktuální vrstva\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="139de-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="139de-542">Statutární kniha\-Aktuální vrstva\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="139de-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="139de-543">Statutární kniha\-Aktuální vrstva\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="139de-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="139de-544">Aktuální vrstva \- Celkem</span><span class="sxs-lookup"><span data-stu-id="139de-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="139de-545">Stornovací kniha\-Vlastní vrstva\-JE\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="139de-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="139de-546">Kniha IFRS 16\-Vlastní vrstva\-JE\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="139de-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="139de-547">Kniha IFRS 16\-Vlastní vrstva\-JE\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="139de-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="139de-548">Kniha IFRS 16\-Vlastní vrstva\-JE\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="139de-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="139de-549">Kniha IFRS 16\-Vlastní vrstva\-JE\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="139de-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="139de-550">Vlastní vrstva \+ Vlastní vrstva \- Celkem</span><span class="sxs-lookup"><span data-stu-id="139de-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="139de-551">1</span><span class="sxs-lookup"><span data-stu-id="139de-551">1</span></span>          | <span data-ttu-id="139de-552">Výdaje leasingu</span><span class="sxs-lookup"><span data-stu-id="139de-552">Lease expense</span></span>            | <span data-ttu-id="139de-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="139de-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="139de-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="139de-554">1,000\.00</span></span>               |   | <span data-ttu-id="139de-555">\-1000</span><span class="sxs-lookup"><span data-stu-id="139de-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="139de-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="139de-556">0\.00</span></span>                                   |
| <span data-ttu-id="139de-557">2</span><span class="sxs-lookup"><span data-stu-id="139de-557">2</span></span>          | <span data-ttu-id="139de-558">Bankovní poplatek</span><span class="sxs-lookup"><span data-stu-id="139de-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="139de-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="139de-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="139de-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="139de-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="139de-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="139de-561">3\.00</span></span>                                   |
| <span data-ttu-id="139de-562">3</span><span class="sxs-lookup"><span data-stu-id="139de-562">3</span></span>          | <span data-ttu-id="139de-563">Výdaje DPH</span><span class="sxs-lookup"><span data-stu-id="139de-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="139de-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="139de-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="139de-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="139de-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="139de-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="139de-566">5\.00</span></span>                                   |
| <span data-ttu-id="139de-567">4</span><span class="sxs-lookup"><span data-stu-id="139de-567">4</span></span>          | <span data-ttu-id="139de-568">Clearingový účet</span><span class="sxs-lookup"><span data-stu-id="139de-568">Clearing account</span></span>         | <span data-ttu-id="139de-569">\-1000\.00</span><span class="sxs-lookup"><span data-stu-id="139de-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="139de-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="139de-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="139de-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="139de-571">0\.00</span></span>                   |   | <span data-ttu-id="139de-572">1 000</span><span class="sxs-lookup"><span data-stu-id="139de-572">1,000</span></span>                                           |                                                | <span data-ttu-id="139de-573">\-1000</span><span class="sxs-lookup"><span data-stu-id="139de-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="139de-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="139de-574">0\.00</span></span>                                   |
| <span data-ttu-id="139de-575">5</span><span class="sxs-lookup"><span data-stu-id="139de-575">5</span></span>          | <span data-ttu-id="139de-576">Závazky</span><span class="sxs-lookup"><span data-stu-id="139de-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="139de-577">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="139de-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="139de-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="139de-578">1,008\.00</span></span>                                         | <span data-ttu-id="139de-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="139de-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="139de-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="139de-580">0\.00</span></span>                                   |
| <span data-ttu-id="139de-581">6</span><span class="sxs-lookup"><span data-stu-id="139de-581">6</span></span>          | <span data-ttu-id="139de-582">Používaný majetek</span><span class="sxs-lookup"><span data-stu-id="139de-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="139de-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="139de-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="139de-584">22,794</span><span class="sxs-lookup"><span data-stu-id="139de-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="139de-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="139de-585">22,793\.90</span></span>                              |
| <span data-ttu-id="139de-586">7</span><span class="sxs-lookup"><span data-stu-id="139de-586">7</span></span>          | <span data-ttu-id="139de-587">Povinnost finančního leasingu</span><span class="sxs-lookup"><span data-stu-id="139de-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="139de-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="139de-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="139de-589">\-22 794</span><span class="sxs-lookup"><span data-stu-id="139de-589">\-22,794</span></span>                                       | <span data-ttu-id="139de-590">1 000</span><span class="sxs-lookup"><span data-stu-id="139de-590">1,000</span></span>                                          | <span data-ttu-id="139de-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="139de-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="139de-592">\-21 888\.87</span><span class="sxs-lookup"><span data-stu-id="139de-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="139de-593">8</span><span class="sxs-lookup"><span data-stu-id="139de-593">8</span></span>          | <span data-ttu-id="139de-594">Výdaje na úroky</span><span class="sxs-lookup"><span data-stu-id="139de-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="139de-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="139de-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="139de-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="139de-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="139de-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="139de-597">94\.97</span></span>                                  |
| <span data-ttu-id="139de-598">9</span><span class="sxs-lookup"><span data-stu-id="139de-598">9</span></span>          | <span data-ttu-id="139de-599">Hotovost</span><span class="sxs-lookup"><span data-stu-id="139de-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="139de-600">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="139de-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="139de-601">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="139de-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="139de-602">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="139de-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="139de-603">10</span><span class="sxs-lookup"><span data-stu-id="139de-603">10</span></span>         | <span data-ttu-id="139de-604">Odpisové výdaje</span><span class="sxs-lookup"><span data-stu-id="139de-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="139de-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="139de-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="139de-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="139de-606">949\.75</span></span>                                        | <span data-ttu-id="139de-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="139de-607">949\.75</span></span>                                 |
| <span data-ttu-id="139de-608">11</span><span class="sxs-lookup"><span data-stu-id="139de-608">11</span></span>         | <span data-ttu-id="139de-609">Akumulovaný odpis</span><span class="sxs-lookup"><span data-stu-id="139de-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="139de-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="139de-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="139de-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="139de-611">\-949\.75</span></span>                                      | <span data-ttu-id="139de-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="139de-612">\-949\.75</span></span>                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]