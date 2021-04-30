---
title: Duální vykazování
description: Toto téma vás provede příkladem, který ukazuje, jak můžete splnit požadavky jak pro vykazování podle Mezinárodního standardu finančního výkaznictví (IFRS), tak pro statutární vykazování v leasingu majetku.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseBookMaster
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 86f42f8db707f3b8c62b9ec4c39ad6464f080748
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881149"
---
# <a name="dual-reporting"></a><span data-ttu-id="69770-103">Duální vykazování</span><span class="sxs-lookup"><span data-stu-id="69770-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="69770-104">Toto téma vás provede příkladem, který ukazuje, jak můžete splnit požadavky jak pro vykazování podle Mezinárodního standardu finančního výkaznictví (IFRS), tak pro statutární vykazování v leasingu majetku.</span><span class="sxs-lookup"><span data-stu-id="69770-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="69770-105">Znalost účtovacích vrstev v Microsoft Dynamics 365 Finance je nutná a příklad bude lépe srozumitelný.</span><span class="sxs-lookup"><span data-stu-id="69770-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="69770-106">Příklad</span><span class="sxs-lookup"><span data-stu-id="69770-106">Example</span></span>

<span data-ttu-id="69770-107">Následující příklad provádí účtování pro leasing podle italského statutárního výkaznictví pomocí metody hotovostního základu i metod vykazování podle IFRS.</span><span class="sxs-lookup"><span data-stu-id="69770-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="69770-108">Společnost musí založit tři účetní knihy, které zohlední jak italské zákonné požadavky, tak požadavky IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="69770-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="69770-109">Jedna kniha je vyžadována pro IFRS 16, jedna kniha je vyžadována pro zákonné požadavky a jedna kniha je vyžadována k automatickému stornování statutárních účtování.</span><span class="sxs-lookup"><span data-stu-id="69770-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="69770-110">Knihy jsou vytvořeny tak, jak je uvedeno v následujících tabulkách.</span><span class="sxs-lookup"><span data-stu-id="69770-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="69770-111">**Kniha IFRS 16**</span><span class="sxs-lookup"><span data-stu-id="69770-111">**IFRS 16 book**</span></span>

<span data-ttu-id="69770-112">Kniha IFRS 16 je vytvořena v souladu s účetním standardem IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="69770-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="69770-113">Všechny položky, které jsou zaúčtovány v této knize, budou zaúčtovány do vlastní vrstvy.</span><span class="sxs-lookup"><span data-stu-id="69770-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="69770-114">Jméno</span><span class="sxs-lookup"><span data-stu-id="69770-114">Name</span></span>                                    | <span data-ttu-id="69770-115">popis</span><span class="sxs-lookup"><span data-stu-id="69770-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="69770-116">Typ knihy</span><span class="sxs-lookup"><span data-stu-id="69770-116">Book type</span></span>                               | <span data-ttu-id="69770-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="69770-117">IFRS 16</span></span>        |
| <span data-ttu-id="69770-118">Popis knihy</span><span class="sxs-lookup"><span data-stu-id="69770-118">Book description</span></span>                        | <span data-ttu-id="69770-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="69770-119">IFRS 16</span></span>        |
| <span data-ttu-id="69770-120">Účtovací vrstva</span><span class="sxs-lookup"><span data-stu-id="69770-120">Posting Layer</span></span>                           | <span data-ttu-id="69770-121">Vlastní vrstva 1</span><span class="sxs-lookup"><span data-stu-id="69770-121">Custom layer 1</span></span> |
| <span data-ttu-id="69770-122">Typ leasingu</span><span class="sxs-lookup"><span data-stu-id="69770-122">Lease Type</span></span>                              | <span data-ttu-id="69770-123">Finance</span><span class="sxs-lookup"><span data-stu-id="69770-123">Finance</span></span>        |
| <span data-ttu-id="69770-124">Rámec účetnictví</span><span class="sxs-lookup"><span data-stu-id="69770-124">Accounting Framework</span></span>                    | <span data-ttu-id="69770-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="69770-125">IFRS 16</span></span>        |
| <span data-ttu-id="69770-126">Nastavení doby trvání leasingu / očekávané doby použitelnosti</span><span class="sxs-lookup"><span data-stu-id="69770-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="69770-127">0,00</span><span class="sxs-lookup"><span data-stu-id="69770-127">0.00</span></span>           |
| <span data-ttu-id="69770-128">Nastavení současné hodnoty / reálné hodnoty majetku</span><span class="sxs-lookup"><span data-stu-id="69770-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="69770-129">0,00</span><span class="sxs-lookup"><span data-stu-id="69770-129">0.00</span></span>           |
| <span data-ttu-id="69770-130">Krátkodobá prahová hodnota</span><span class="sxs-lookup"><span data-stu-id="69770-130">Short-term threshold</span></span>                    | <span data-ttu-id="69770-131">12</span><span class="sxs-lookup"><span data-stu-id="69770-131">12</span></span>             |
| <span data-ttu-id="69770-132">Nízká prahová hodnota</span><span class="sxs-lookup"><span data-stu-id="69770-132">Low Value Threshold</span></span>                     | <span data-ttu-id="69770-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="69770-133">5,000.00</span></span>       |
| <span data-ttu-id="69770-134">Platba dodavateli</span><span class="sxs-lookup"><span data-stu-id="69770-134">Pay to Vendor</span></span>                           | <span data-ttu-id="69770-135">Žádný</span><span class="sxs-lookup"><span data-stu-id="69770-135">No</span></span>             |

<span data-ttu-id="69770-136">**Statutární kniha**</span><span class="sxs-lookup"><span data-stu-id="69770-136">**Statutory book**</span></span>

<span data-ttu-id="69770-137">Statutární kniha je hotovostní kniha, kde společnost bude účtovat výdaje na leasing jako částku hotovosti, která se každý měsíc platí za nájem.</span><span class="sxs-lookup"><span data-stu-id="69770-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="69770-138">Tato kniha nevytvoří používaný majetek ani leasingový závazek.</span><span class="sxs-lookup"><span data-stu-id="69770-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="69770-139">Jméno</span><span class="sxs-lookup"><span data-stu-id="69770-139">Name</span></span>                                    | <span data-ttu-id="69770-140">popis</span><span class="sxs-lookup"><span data-stu-id="69770-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="69770-141">Typ knihy</span><span class="sxs-lookup"><span data-stu-id="69770-141">Book type</span></span>                               | <span data-ttu-id="69770-142">Statutární</span><span class="sxs-lookup"><span data-stu-id="69770-142">Statutory</span></span>   |
| <span data-ttu-id="69770-143">Popis knihy</span><span class="sxs-lookup"><span data-stu-id="69770-143">Book description</span></span>                        | <span data-ttu-id="69770-144">Místní GAAP</span><span class="sxs-lookup"><span data-stu-id="69770-144">Local GAAP</span></span>  |
| <span data-ttu-id="69770-145">Účtovací vrstva</span><span class="sxs-lookup"><span data-stu-id="69770-145">Posting Layer</span></span>                           | <span data-ttu-id="69770-146">Aktuální</span><span class="sxs-lookup"><span data-stu-id="69770-146">Current</span></span>     |
| <span data-ttu-id="69770-147">Typ leasingu</span><span class="sxs-lookup"><span data-stu-id="69770-147">Lease Type</span></span>                              | <span data-ttu-id="69770-148">Automatické</span><span class="sxs-lookup"><span data-stu-id="69770-148">Automatic</span></span>   |
| <span data-ttu-id="69770-149">Rámec účetnictví</span><span class="sxs-lookup"><span data-stu-id="69770-149">Accounting Framework</span></span>                    | <span data-ttu-id="69770-150">Hotovostní základ</span><span class="sxs-lookup"><span data-stu-id="69770-150">Cash basis</span></span>  |
| <span data-ttu-id="69770-151">Nastavení doby trvání leasingu / očekávané doby použitelnosti</span><span class="sxs-lookup"><span data-stu-id="69770-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="69770-152">0,00</span><span class="sxs-lookup"><span data-stu-id="69770-152">0.00</span></span>        |
| <span data-ttu-id="69770-153">Nastavení současné hodnoty / reálné hodnoty majetku</span><span class="sxs-lookup"><span data-stu-id="69770-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="69770-154">0,00</span><span class="sxs-lookup"><span data-stu-id="69770-154">0.00</span></span>        |
| <span data-ttu-id="69770-155">Krátkodobá prahová hodnota</span><span class="sxs-lookup"><span data-stu-id="69770-155">Short-term threshold</span></span>                    | <span data-ttu-id="69770-156">0</span><span class="sxs-lookup"><span data-stu-id="69770-156">0</span></span>           |
| <span data-ttu-id="69770-157">Nízká prahová hodnota</span><span class="sxs-lookup"><span data-stu-id="69770-157">Low Value Threshold</span></span>                     | <span data-ttu-id="69770-158">0</span><span class="sxs-lookup"><span data-stu-id="69770-158">0</span></span>           |
| <span data-ttu-id="69770-159">Platba dodavateli</span><span class="sxs-lookup"><span data-stu-id="69770-159">Pay to Vendor</span></span>                           | <span data-ttu-id="69770-160">Žádný</span><span class="sxs-lookup"><span data-stu-id="69770-160">No</span></span>          |

<span data-ttu-id="69770-161">**Statutární stornovací kniha**</span><span class="sxs-lookup"><span data-stu-id="69770-161">**Statutory reversal book**</span></span>

<span data-ttu-id="69770-162">Statutární stornovací kniha je sestavena stejným způsobem jako statutární kniha.</span><span class="sxs-lookup"><span data-stu-id="69770-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="69770-163">Jméno</span><span class="sxs-lookup"><span data-stu-id="69770-163">Name</span></span>                                    | <span data-ttu-id="69770-164">popis</span><span class="sxs-lookup"><span data-stu-id="69770-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="69770-165">Typ knihy</span><span class="sxs-lookup"><span data-stu-id="69770-165">Book type</span></span>                               | <span data-ttu-id="69770-166">Statutární – storno</span><span class="sxs-lookup"><span data-stu-id="69770-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="69770-167">Popis knihy</span><span class="sxs-lookup"><span data-stu-id="69770-167">Book description</span></span>                        | <span data-ttu-id="69770-168">Kniha pro stornování statutární knihy</span><span class="sxs-lookup"><span data-stu-id="69770-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="69770-169">Účtovací vrstva</span><span class="sxs-lookup"><span data-stu-id="69770-169">Posting Layer</span></span>                           | <span data-ttu-id="69770-170">Vlastní vrstva 1</span><span class="sxs-lookup"><span data-stu-id="69770-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="69770-171">Typ leasingu</span><span class="sxs-lookup"><span data-stu-id="69770-171">Lease Type</span></span>                              | <span data-ttu-id="69770-172">Automatické</span><span class="sxs-lookup"><span data-stu-id="69770-172">Automatic</span></span>                      |
| <span data-ttu-id="69770-173">Rámec účetnictví</span><span class="sxs-lookup"><span data-stu-id="69770-173">Accounting Framework</span></span>                    | <span data-ttu-id="69770-174">Hotovostní základ</span><span class="sxs-lookup"><span data-stu-id="69770-174">Cash basis</span></span>                     |
| <span data-ttu-id="69770-175">Nastavení doby trvání leasingu / očekávané doby použitelnosti</span><span class="sxs-lookup"><span data-stu-id="69770-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="69770-176">0,00</span><span class="sxs-lookup"><span data-stu-id="69770-176">0.00</span></span>                           |
| <span data-ttu-id="69770-177">Nastavení současné hodnoty / reálné hodnoty majetku</span><span class="sxs-lookup"><span data-stu-id="69770-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="69770-178">0,00</span><span class="sxs-lookup"><span data-stu-id="69770-178">0.00</span></span>                           |
| <span data-ttu-id="69770-179">Krátkodobá prahová hodnota</span><span class="sxs-lookup"><span data-stu-id="69770-179">Short-term threshold</span></span>                    | <span data-ttu-id="69770-180">0</span><span class="sxs-lookup"><span data-stu-id="69770-180">0</span></span>                              |
| <span data-ttu-id="69770-181">Nízká prahová hodnota</span><span class="sxs-lookup"><span data-stu-id="69770-181">Low Value Threshold</span></span>                     | <span data-ttu-id="69770-182">0</span><span class="sxs-lookup"><span data-stu-id="69770-182">0</span></span>                              |
| <span data-ttu-id="69770-183">Platba dodavateli</span><span class="sxs-lookup"><span data-stu-id="69770-183">Pay to Vendor</span></span>                           | <span data-ttu-id="69770-184">Žádný</span><span class="sxs-lookup"><span data-stu-id="69770-184">No</span></span>                             |

<span data-ttu-id="69770-185">V tomto příkladu byl vytvořen leasing, který má následující nastavení na kartách **Obecné** a **Řádky platebního kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="69770-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="69770-186">**Karta Obecné**</span><span class="sxs-lookup"><span data-stu-id="69770-186">**General tab**</span></span>

| <span data-ttu-id="69770-187">Pole</span><span class="sxs-lookup"><span data-stu-id="69770-187">Field</span></span>                      | <span data-ttu-id="69770-188">Hodnota</span><span class="sxs-lookup"><span data-stu-id="69770-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="69770-189">Přírůstková výpůjční úroková sazba</span><span class="sxs-lookup"><span data-stu-id="69770-189">Incremental borrowing rate</span></span> | <span data-ttu-id="69770-190">5 %</span><span class="sxs-lookup"><span data-stu-id="69770-190">5%</span></span>               |
| <span data-ttu-id="69770-191">Datum zahájení</span><span class="sxs-lookup"><span data-stu-id="69770-191">Commencement date</span></span>          | <span data-ttu-id="69770-192">1. 1. 2020</span><span class="sxs-lookup"><span data-stu-id="69770-192">1/1/2020</span></span>         |
| <span data-ttu-id="69770-193">Skupina leasingu</span><span class="sxs-lookup"><span data-stu-id="69770-193">Lease group</span></span>                | <span data-ttu-id="69770-194">Budovy</span><span class="sxs-lookup"><span data-stu-id="69770-194">Buildings</span></span>        |
| <span data-ttu-id="69770-195">Dodavatel</span><span class="sxs-lookup"><span data-stu-id="69770-195">Vendor</span></span>                     | <span data-ttu-id="69770-196">1001</span><span class="sxs-lookup"><span data-stu-id="69770-196">1001</span></span>             |
| <span data-ttu-id="69770-197">Reálná hodnota majetku</span><span class="sxs-lookup"><span data-stu-id="69770-197">Fair value of the asset</span></span>    | <span data-ttu-id="69770-198">245,000</span><span class="sxs-lookup"><span data-stu-id="69770-198">245,000</span></span>          |
| <span data-ttu-id="69770-199">Očekávaná doba použitelnosti majetku</span><span class="sxs-lookup"><span data-stu-id="69770-199">Asset useful life</span></span>          | <span data-ttu-id="69770-200">120</span><span class="sxs-lookup"><span data-stu-id="69770-200">120</span></span>              |
| <span data-ttu-id="69770-201">Typ anuity</span><span class="sxs-lookup"><span data-stu-id="69770-201">Annuity type</span></span>               | <span data-ttu-id="69770-202">Běžná anuita</span><span class="sxs-lookup"><span data-stu-id="69770-202">Ordinary annuity</span></span> |
| <span data-ttu-id="69770-203">Interval úročení</span><span class="sxs-lookup"><span data-stu-id="69770-203">Compounding interval</span></span>       | <span data-ttu-id="69770-204">Měsíčně</span><span class="sxs-lookup"><span data-stu-id="69770-204">Monthly</span></span>          |

<span data-ttu-id="69770-205">**Karta Řádky platebního kalendáře**</span><span class="sxs-lookup"><span data-stu-id="69770-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="69770-206">Pole</span><span class="sxs-lookup"><span data-stu-id="69770-206">Field</span></span>             | <span data-ttu-id="69770-207">Hodnota</span><span class="sxs-lookup"><span data-stu-id="69770-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="69770-208">Počáteční datum</span><span class="sxs-lookup"><span data-stu-id="69770-208">Start date</span></span>        | <span data-ttu-id="69770-209">1. 1. 2020</span><span class="sxs-lookup"><span data-stu-id="69770-209">1/1/2020</span></span>   |
| <span data-ttu-id="69770-210">Interval období</span><span class="sxs-lookup"><span data-stu-id="69770-210">Period interval</span></span>   | <span data-ttu-id="69770-211">Měsíce</span><span class="sxs-lookup"><span data-stu-id="69770-211">Months</span></span>     |
| <span data-ttu-id="69770-212">Období</span><span class="sxs-lookup"><span data-stu-id="69770-212">Periods</span></span>           | <span data-ttu-id="69770-213">24</span><span class="sxs-lookup"><span data-stu-id="69770-213">24</span></span>         |
| <span data-ttu-id="69770-214">Koncové datum</span><span class="sxs-lookup"><span data-stu-id="69770-214">End date</span></span>          | <span data-ttu-id="69770-215">31. 12. 2020</span><span class="sxs-lookup"><span data-stu-id="69770-215">12/31/2020</span></span> |
| <span data-ttu-id="69770-216">Četnost plateb</span><span class="sxs-lookup"><span data-stu-id="69770-216">Payment frequency</span></span> | <span data-ttu-id="69770-217">Měsíčně</span><span class="sxs-lookup"><span data-stu-id="69770-217">Monthly</span></span>    |
| <span data-ttu-id="69770-218">Částka platby</span><span class="sxs-lookup"><span data-stu-id="69770-218">Payment amount</span></span>    | <span data-ttu-id="69770-219">1 000</span><span class="sxs-lookup"><span data-stu-id="69770-219">1,000</span></span>      |

<span data-ttu-id="69770-220">Chcete-li tento leasing započítat do dvou rámců, použijete aktuální účtovací vrstvu a vlastní účtovací vrstvu.</span><span class="sxs-lookup"><span data-stu-id="69770-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="69770-221">Následující tabulka ukazuje příklad každé položky deníku, která je potřeba pro věrné zobrazení financí podle každého standardu výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="69770-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="69770-222">Podrobný popis každé položky deníku pro první měsíc leasingu je poskytnut později.</span><span class="sxs-lookup"><span data-stu-id="69770-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="69770-223">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="69770-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="69770-224">popis</span><span class="sxs-lookup"><span data-stu-id="69770-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="69770-225">Statutární kniha (aktuální vrstva)</span><span class="sxs-lookup"><span data-stu-id="69770-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="69770-226">Celková aktuální vrstva</span><span class="sxs-lookup"><span data-stu-id="69770-226">Current layer total</span></span></th>
<th><span data-ttu-id="69770-227">Stornovací kniha (vlastní vrstva)</span><span class="sxs-lookup"><span data-stu-id="69770-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="69770-228">Kniha IFRS 16 (vlastní vrstva)</span><span class="sxs-lookup"><span data-stu-id="69770-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="69770-229">Aktuální vrstva + vlastní vrstva celkem</span><span class="sxs-lookup"><span data-stu-id="69770-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="69770-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="69770-230">JE-100</span></span></th>
<th><span data-ttu-id="69770-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="69770-231">JE-110</span></span></th>
<th><span data-ttu-id="69770-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="69770-232">JE-120</span></span></th>
<th><span data-ttu-id="69770-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="69770-233">JE-130</span></span></th>
<th><span data-ttu-id="69770-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="69770-234">JE-140</span></span></th>
<th><span data-ttu-id="69770-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="69770-235">JE-150</span></span></th>
<th><span data-ttu-id="69770-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="69770-236">JE-160</span></span></th>
<th><span data-ttu-id="69770-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="69770-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="69770-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="69770-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="69770-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="69770-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="69770-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="69770-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="69770-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="69770-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="69770-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="69770-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="69770-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="69770-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="69770-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="69770-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="69770-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="69770-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69770-246">1</span><span class="sxs-lookup"><span data-stu-id="69770-246">1</span></span></td>
<td><span data-ttu-id="69770-247">Výdaje leasingu</span><span class="sxs-lookup"><span data-stu-id="69770-247">Lease expense</span></span></td>
<td><span data-ttu-id="69770-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="69770-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="69770-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="69770-249">1,000.00</span></span></td>
<td><span data-ttu-id="69770-250">−1 000,00</span><span class="sxs-lookup"><span data-stu-id="69770-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="69770-251">0,00</span><span class="sxs-lookup"><span data-stu-id="69770-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69770-252">2</span><span class="sxs-lookup"><span data-stu-id="69770-252">2</span></span></td>
<td><span data-ttu-id="69770-253">Bankovní poplatek</span><span class="sxs-lookup"><span data-stu-id="69770-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="69770-254">3.00</span><span class="sxs-lookup"><span data-stu-id="69770-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="69770-255">3.00</span><span class="sxs-lookup"><span data-stu-id="69770-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="69770-256">3.00</span><span class="sxs-lookup"><span data-stu-id="69770-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69770-257">3</span><span class="sxs-lookup"><span data-stu-id="69770-257">3</span></span></td>
<td><span data-ttu-id="69770-258">Výdaje DPH</span><span class="sxs-lookup"><span data-stu-id="69770-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="69770-259">5.00</span><span class="sxs-lookup"><span data-stu-id="69770-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="69770-260">5.00</span><span class="sxs-lookup"><span data-stu-id="69770-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="69770-261">5.00</span><span class="sxs-lookup"><span data-stu-id="69770-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69770-262">4</span><span class="sxs-lookup"><span data-stu-id="69770-262">4</span></span></td>
<td><span data-ttu-id="69770-263">Clearingový účet</span><span class="sxs-lookup"><span data-stu-id="69770-263">Clearing account</span></span></td>
<td><span data-ttu-id="69770-264">−1 000,00</span><span class="sxs-lookup"><span data-stu-id="69770-264">-1,000.00</span></span></td>
<td><span data-ttu-id="69770-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="69770-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="69770-266">0,00</span><span class="sxs-lookup"><span data-stu-id="69770-266">0.00</span></span></td>
<td><span data-ttu-id="69770-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="69770-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="69770-268">−1 000,00</span><span class="sxs-lookup"><span data-stu-id="69770-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="69770-269">0,00</span><span class="sxs-lookup"><span data-stu-id="69770-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69770-270">5</span><span class="sxs-lookup"><span data-stu-id="69770-270">5</span></span></td>
<td><span data-ttu-id="69770-271">Závazky</span><span class="sxs-lookup"><span data-stu-id="69770-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="69770-272">-1008,00</span><span class="sxs-lookup"><span data-stu-id="69770-272">-1,008.00</span></span></td>
<td><span data-ttu-id="69770-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="69770-273">1,008.00</span></span></td>
<td><span data-ttu-id="69770-274">0,00</span><span class="sxs-lookup"><span data-stu-id="69770-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="69770-275">0,00</span><span class="sxs-lookup"><span data-stu-id="69770-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69770-276">6</span><span class="sxs-lookup"><span data-stu-id="69770-276">6</span></span></td>
<td><span data-ttu-id="69770-277">Používaný majetek</span><span class="sxs-lookup"><span data-stu-id="69770-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="69770-278">0,00</span><span class="sxs-lookup"><span data-stu-id="69770-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="69770-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="69770-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="69770-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="69770-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69770-281">7</span><span class="sxs-lookup"><span data-stu-id="69770-281">7</span></span></td>
<td><span data-ttu-id="69770-282">Povinnost finančního leasingu</span><span class="sxs-lookup"><span data-stu-id="69770-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="69770-283">0,00</span><span class="sxs-lookup"><span data-stu-id="69770-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="69770-284">-22 794,00</span><span class="sxs-lookup"><span data-stu-id="69770-284">-22,794.00</span></span></td>
<td><span data-ttu-id="69770-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="69770-285">1,000.00</span></span></td>
<td><span data-ttu-id="69770-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="69770-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="69770-287">-21 888,87</span><span class="sxs-lookup"><span data-stu-id="69770-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69770-288">8</span><span class="sxs-lookup"><span data-stu-id="69770-288">8</span></span></td>
<td><span data-ttu-id="69770-289">Výdaje na úroky</span><span class="sxs-lookup"><span data-stu-id="69770-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="69770-290">0,00</span><span class="sxs-lookup"><span data-stu-id="69770-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="69770-291">94.97</span><span class="sxs-lookup"><span data-stu-id="69770-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="69770-292">94.97</span><span class="sxs-lookup"><span data-stu-id="69770-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69770-293">9</span><span class="sxs-lookup"><span data-stu-id="69770-293">9</span></span></td>
<td><span data-ttu-id="69770-294">Hotovost</span><span class="sxs-lookup"><span data-stu-id="69770-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="69770-295">-1008,00</span><span class="sxs-lookup"><span data-stu-id="69770-295">-1,008.00</span></span></td>
<td><span data-ttu-id="69770-296">-1008,00</span><span class="sxs-lookup"><span data-stu-id="69770-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="69770-297">-1008,00</span><span class="sxs-lookup"><span data-stu-id="69770-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69770-298">10</span><span class="sxs-lookup"><span data-stu-id="69770-298">10</span></span></td>
<td><span data-ttu-id="69770-299">Odpisové výdaje</span><span class="sxs-lookup"><span data-stu-id="69770-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="69770-300">0,00</span><span class="sxs-lookup"><span data-stu-id="69770-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="69770-301">949.75</span><span class="sxs-lookup"><span data-stu-id="69770-301">949.75</span></span></td>
<td><span data-ttu-id="69770-302">949.75</span><span class="sxs-lookup"><span data-stu-id="69770-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69770-303">11</span><span class="sxs-lookup"><span data-stu-id="69770-303">11</span></span></td>
<td><span data-ttu-id="69770-304">Akumulovaný odpis</span><span class="sxs-lookup"><span data-stu-id="69770-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="69770-305">0,00</span><span class="sxs-lookup"><span data-stu-id="69770-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="69770-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="69770-306">-949.75</span></span></td>
<td><span data-ttu-id="69770-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="69770-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="69770-308">Jak ukazuje předchozí tabulka, jsou potřeba tři knihy pro vykazování v rámci statutárního výkaznictví i výkaznictví podle IFRS.</span><span class="sxs-lookup"><span data-stu-id="69770-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="69770-309">Statutární kniha zaznamenává leasingové splátky podle pravidel pro hotovostní účetnictví v aktuální vrstvě.</span><span class="sxs-lookup"><span data-stu-id="69770-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="69770-310">Statutární stornovací kniha stornuje položky statutárního deníku.</span><span class="sxs-lookup"><span data-stu-id="69770-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="69770-311">Kniha IFRS 16 vytváří položky deníku, které jsou vyžadovány podle IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="69770-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="69770-312">Leasing musíte zadat pouze jednou.</span><span class="sxs-lookup"><span data-stu-id="69770-312">You must enter a lease only one time.</span></span> <span data-ttu-id="69770-313">Poté můžete otevřít stránku **Knihy**, kde jsou všechny knihy, které jsou přidruženy k leasingu.</span><span class="sxs-lookup"><span data-stu-id="69770-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="69770-314">Když vytvoříte knihy, všechny tři musí být přidruženy ke stejnému záznamu leasingu.</span><span class="sxs-lookup"><span data-stu-id="69770-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="69770-315">První položka deníku zaznamenává výdaje na leasing podle statutární knihy.</span><span class="sxs-lookup"><span data-stu-id="69770-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="69770-316">Platby můžete vytvářet v dávce nebo výběrem platebního kalendáře ve statutární knize.</span><span class="sxs-lookup"><span data-stu-id="69770-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="69770-317">V tomto příkladu se pro statutární knihu z platebního kalendáře vytvoří následující položka deníku.</span><span class="sxs-lookup"><span data-stu-id="69770-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="69770-318">Leasingová splátka – 31. 1. 2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="69770-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="69770-319">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="69770-319">Account type</span></span> | <span data-ttu-id="69770-320">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="69770-320">Account number</span></span> | <span data-ttu-id="69770-321">Vrstva</span><span class="sxs-lookup"><span data-stu-id="69770-321">Layer</span></span>   | <span data-ttu-id="69770-322">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="69770-322">Account description</span></span> | <span data-ttu-id="69770-323">Debet</span><span class="sxs-lookup"><span data-stu-id="69770-323">Debit</span></span>    | <span data-ttu-id="69770-324">Kredit</span><span class="sxs-lookup"><span data-stu-id="69770-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="69770-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="69770-325">Ledger</span></span>       | <span data-ttu-id="69770-326">1</span><span class="sxs-lookup"><span data-stu-id="69770-326">1</span></span>              | <span data-ttu-id="69770-327">Aktuální</span><span class="sxs-lookup"><span data-stu-id="69770-327">Current</span></span> | <span data-ttu-id="69770-328">Výdaje leasingu</span><span class="sxs-lookup"><span data-stu-id="69770-328">Lease expense</span></span>       | <span data-ttu-id="69770-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="69770-329">1,000.00</span></span> |          |
| <span data-ttu-id="69770-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="69770-330">Ledger</span></span>       | <span data-ttu-id="69770-331">4</span><span class="sxs-lookup"><span data-stu-id="69770-331">4</span></span>              | <span data-ttu-id="69770-332">Aktuální</span><span class="sxs-lookup"><span data-stu-id="69770-332">Current</span></span> | <span data-ttu-id="69770-333">Clearingový účet</span><span class="sxs-lookup"><span data-stu-id="69770-333">Clearing account</span></span>    |          | <span data-ttu-id="69770-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="69770-334">1,000.00</span></span> |

<span data-ttu-id="69770-335">Úředník pro závazky používá standardní funkce Dynamics 365 k vytvoření fakturu pro zaplacení leasingu mimo leasing majetku.</span><span class="sxs-lookup"><span data-stu-id="69770-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="69770-336">Nicméně místo výběru **Výdaje na leasing** jako debetního účtu vybere clearingový účet pro vygenerování následující položky.</span><span class="sxs-lookup"><span data-stu-id="69770-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="69770-337">Proces AP – 31. 1. 2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="69770-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="69770-338">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="69770-338">Account type</span></span> | <span data-ttu-id="69770-339">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="69770-339">Account number</span></span> | <span data-ttu-id="69770-340">Vrstva</span><span class="sxs-lookup"><span data-stu-id="69770-340">Layer</span></span>   | <span data-ttu-id="69770-341">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="69770-341">Account description</span></span> | <span data-ttu-id="69770-342">Debet</span><span class="sxs-lookup"><span data-stu-id="69770-342">Debit</span></span>    | <span data-ttu-id="69770-343">Kredit</span><span class="sxs-lookup"><span data-stu-id="69770-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="69770-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="69770-344">Ledger</span></span>       | <span data-ttu-id="69770-345">4</span><span class="sxs-lookup"><span data-stu-id="69770-345">4</span></span>              | <span data-ttu-id="69770-346">Aktuální</span><span class="sxs-lookup"><span data-stu-id="69770-346">Current</span></span> | <span data-ttu-id="69770-347">Clearingový účet</span><span class="sxs-lookup"><span data-stu-id="69770-347">Clearing account</span></span>    | <span data-ttu-id="69770-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="69770-348">1,000.00</span></span> |          |
| <span data-ttu-id="69770-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="69770-349">Ledger</span></span>       | <span data-ttu-id="69770-350">2</span><span class="sxs-lookup"><span data-stu-id="69770-350">2</span></span>              | <span data-ttu-id="69770-351">Aktuální</span><span class="sxs-lookup"><span data-stu-id="69770-351">Current</span></span> | <span data-ttu-id="69770-352">Bankovní poplatek</span><span class="sxs-lookup"><span data-stu-id="69770-352">Bank fee</span></span>            | <span data-ttu-id="69770-353">3.00</span><span class="sxs-lookup"><span data-stu-id="69770-353">3.00</span></span>     |          |
| <span data-ttu-id="69770-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="69770-354">Ledger</span></span>       | <span data-ttu-id="69770-355">3</span><span class="sxs-lookup"><span data-stu-id="69770-355">3</span></span>              | <span data-ttu-id="69770-356">Aktuální</span><span class="sxs-lookup"><span data-stu-id="69770-356">Current</span></span> | <span data-ttu-id="69770-357">Výdaje DPH</span><span class="sxs-lookup"><span data-stu-id="69770-357">VAT expense</span></span>         | <span data-ttu-id="69770-358">5.00</span><span class="sxs-lookup"><span data-stu-id="69770-358">5.00</span></span>     |          |
| <span data-ttu-id="69770-359">Dodavatel</span><span class="sxs-lookup"><span data-stu-id="69770-359">Vendor</span></span>       | <span data-ttu-id="69770-360">5</span><span class="sxs-lookup"><span data-stu-id="69770-360">5</span></span>              | <span data-ttu-id="69770-361">Aktuální</span><span class="sxs-lookup"><span data-stu-id="69770-361">Current</span></span> | <span data-ttu-id="69770-362">Závazky</span><span class="sxs-lookup"><span data-stu-id="69770-362">Accounts payable</span></span>    |          | <span data-ttu-id="69770-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="69770-363">1,008.00</span></span> |

<span data-ttu-id="69770-364">Když je prodejci vystaven výpis, postupujete podle pravidelného platebního procesu.</span><span class="sxs-lookup"><span data-stu-id="69770-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="69770-365">Během tohoto procesu je vygenerována následující položka deníku.</span><span class="sxs-lookup"><span data-stu-id="69770-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="69770-366">Platba v hotovosti – 31. 1. 2020 – 120</span><span class="sxs-lookup"><span data-stu-id="69770-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="69770-367">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="69770-367">Account type</span></span> | <span data-ttu-id="69770-368">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="69770-368">Account number</span></span> | <span data-ttu-id="69770-369">Vrstva</span><span class="sxs-lookup"><span data-stu-id="69770-369">Layer</span></span>   | <span data-ttu-id="69770-370">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="69770-370">Account description</span></span> | <span data-ttu-id="69770-371">Debet</span><span class="sxs-lookup"><span data-stu-id="69770-371">Debit</span></span>    | <span data-ttu-id="69770-372">Kredit</span><span class="sxs-lookup"><span data-stu-id="69770-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="69770-373">Dodavatel</span><span class="sxs-lookup"><span data-stu-id="69770-373">Vendor</span></span>       | <span data-ttu-id="69770-374">5</span><span class="sxs-lookup"><span data-stu-id="69770-374">5</span></span>              | <span data-ttu-id="69770-375">Aktuální</span><span class="sxs-lookup"><span data-stu-id="69770-375">Current</span></span> | <span data-ttu-id="69770-376">Závazky</span><span class="sxs-lookup"><span data-stu-id="69770-376">Accounts Payable</span></span>    | <span data-ttu-id="69770-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="69770-377">1,008.00</span></span> |          |
| <span data-ttu-id="69770-378">Banka</span><span class="sxs-lookup"><span data-stu-id="69770-378">Bank</span></span>         | <span data-ttu-id="69770-379">9</span><span class="sxs-lookup"><span data-stu-id="69770-379">9</span></span>              | <span data-ttu-id="69770-380">Aktuální</span><span class="sxs-lookup"><span data-stu-id="69770-380">Current</span></span> | <span data-ttu-id="69770-381">Hotovost</span><span class="sxs-lookup"><span data-stu-id="69770-381">Cash</span></span>                |          | <span data-ttu-id="69770-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="69770-382">1,008.00</span></span> |

<span data-ttu-id="69770-383">V tomto okamžiku jste plně zaúčtovali tento leasing podle zákonných požadavků na výkaznictví a můžete vygenerovat předvahu pomocí aktuální vrstvy.</span><span class="sxs-lookup"><span data-stu-id="69770-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="69770-384">Systém vrátí předvahu s následujícími čísly.</span><span class="sxs-lookup"><span data-stu-id="69770-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="69770-385">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="69770-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="69770-386">popis</span><span class="sxs-lookup"><span data-stu-id="69770-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="69770-387">Statutární kniha (aktuální vrstva)</span><span class="sxs-lookup"><span data-stu-id="69770-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="69770-388">Celková aktuální vrstva</span><span class="sxs-lookup"><span data-stu-id="69770-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="69770-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="69770-389">JE-100</span></span></th>
<th><span data-ttu-id="69770-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="69770-390">JE-110</span></span></th>
<th><span data-ttu-id="69770-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="69770-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="69770-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="69770-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="69770-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="69770-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="69770-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="69770-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="69770-395">1</span><span class="sxs-lookup"><span data-stu-id="69770-395">1</span></span></td>
<td><span data-ttu-id="69770-396">Výdaje leasingu</span><span class="sxs-lookup"><span data-stu-id="69770-396">Lease expense</span></span></td>
<td><span data-ttu-id="69770-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="69770-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="69770-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="69770-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69770-399">2</span><span class="sxs-lookup"><span data-stu-id="69770-399">2</span></span></td>
<td><span data-ttu-id="69770-400">Bankovní poplatek</span><span class="sxs-lookup"><span data-stu-id="69770-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="69770-401">3.00</span><span class="sxs-lookup"><span data-stu-id="69770-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="69770-402">3.00</span><span class="sxs-lookup"><span data-stu-id="69770-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69770-403">3</span><span class="sxs-lookup"><span data-stu-id="69770-403">3</span></span></td>
<td><span data-ttu-id="69770-404">Výdaje DPH</span><span class="sxs-lookup"><span data-stu-id="69770-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="69770-405">5.00</span><span class="sxs-lookup"><span data-stu-id="69770-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="69770-406">5.00</span><span class="sxs-lookup"><span data-stu-id="69770-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69770-407">4</span><span class="sxs-lookup"><span data-stu-id="69770-407">4</span></span></td>
<td><span data-ttu-id="69770-408">Clearingový účet</span><span class="sxs-lookup"><span data-stu-id="69770-408">Clearing account</span></span></td>
<td><span data-ttu-id="69770-409">−1 000,00</span><span class="sxs-lookup"><span data-stu-id="69770-409">-1,000.00</span></span></td>
<td><span data-ttu-id="69770-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="69770-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="69770-411">0,00</span><span class="sxs-lookup"><span data-stu-id="69770-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69770-412">5</span><span class="sxs-lookup"><span data-stu-id="69770-412">5</span></span></td>
<td><span data-ttu-id="69770-413">Závazky</span><span class="sxs-lookup"><span data-stu-id="69770-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="69770-414">-1008,00</span><span class="sxs-lookup"><span data-stu-id="69770-414">-1,008.00</span></span></td>
<td><span data-ttu-id="69770-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="69770-415">1,008.00</span></span></td>
<td><span data-ttu-id="69770-416">0,00</span><span class="sxs-lookup"><span data-stu-id="69770-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69770-417">6</span><span class="sxs-lookup"><span data-stu-id="69770-417">6</span></span></td>
<td><span data-ttu-id="69770-418">Používaný majetek</span><span class="sxs-lookup"><span data-stu-id="69770-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="69770-419">0,00</span><span class="sxs-lookup"><span data-stu-id="69770-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69770-420">7</span><span class="sxs-lookup"><span data-stu-id="69770-420">7</span></span></td>
<td><span data-ttu-id="69770-421">Povinnost finančního leasingu</span><span class="sxs-lookup"><span data-stu-id="69770-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="69770-422">0,00</span><span class="sxs-lookup"><span data-stu-id="69770-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69770-423">8</span><span class="sxs-lookup"><span data-stu-id="69770-423">8</span></span></td>
<td><span data-ttu-id="69770-424">Výdaje na úroky</span><span class="sxs-lookup"><span data-stu-id="69770-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="69770-425">0,00</span><span class="sxs-lookup"><span data-stu-id="69770-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69770-426">9</span><span class="sxs-lookup"><span data-stu-id="69770-426">9</span></span></td>
<td><span data-ttu-id="69770-427">Hotovost</span><span class="sxs-lookup"><span data-stu-id="69770-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="69770-428">-1008,00</span><span class="sxs-lookup"><span data-stu-id="69770-428">-1,008.00</span></span></td>
<td><span data-ttu-id="69770-429">-1008,00</span><span class="sxs-lookup"><span data-stu-id="69770-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69770-430">10</span><span class="sxs-lookup"><span data-stu-id="69770-430">10</span></span></td>
<td><span data-ttu-id="69770-431">Odpisové výdaje</span><span class="sxs-lookup"><span data-stu-id="69770-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="69770-432">0,00</span><span class="sxs-lookup"><span data-stu-id="69770-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="69770-433">11</span><span class="sxs-lookup"><span data-stu-id="69770-433">11</span></span></td>
<td><span data-ttu-id="69770-434">Akumulovaný odpis</span><span class="sxs-lookup"><span data-stu-id="69770-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="69770-435">0,00</span><span class="sxs-lookup"><span data-stu-id="69770-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="69770-436">Pokud chcete použít čísla IFRS 16 ke spuštění stejné předvahy, musí být položky deníku statutárního účtování stornovány a položky deníku IFRS 16 musí být zaúčtovány.</span><span class="sxs-lookup"><span data-stu-id="69770-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="69770-437">Chcete-li stornovat položky statutárního deníku, tento příklad obsahuje statutární stornovací knihu, která má stejné nastavení jako statutární kniha, ale má opačný profil účtování.</span><span class="sxs-lookup"><span data-stu-id="69770-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="69770-438">Například statutární kniha *debetovala* účet výdaje na leasing, ale stornovací kniha bude tento účet *kreditovat*.</span><span class="sxs-lookup"><span data-stu-id="69770-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="69770-439">Tyto vztahy lze snadno definovat v účtech pro zaúčtování leasingu majetku na stránce **Parametry leasingu majetku** (**Leasing majetku \> Nastavení \> Parametry leasingu majetku**).</span><span class="sxs-lookup"><span data-stu-id="69770-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="69770-440">Když se pro stornovací knihu použije stejný proces, který byl použit pro statutární knihu, vytvoří se následující položka deníku.</span><span class="sxs-lookup"><span data-stu-id="69770-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="69770-441">Rozdíl je v tom, že stornovací kniha rezervuje stornované položky ze statutární knihy.</span><span class="sxs-lookup"><span data-stu-id="69770-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="69770-442">Stornování položek se provede také ve vlastní vrstvě.</span><span class="sxs-lookup"><span data-stu-id="69770-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="69770-443">Když je na aktuální vrstvě spuštěna předvaha, stornované položky deníku nejsou zahrnuty.</span><span class="sxs-lookup"><span data-stu-id="69770-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="69770-444">Leasingová splátka – 31. 1. 2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="69770-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="69770-445">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="69770-445">Account type</span></span> | <span data-ttu-id="69770-446">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="69770-446">Account number</span></span> | <span data-ttu-id="69770-447">Vrstva</span><span class="sxs-lookup"><span data-stu-id="69770-447">Layer</span></span>  | <span data-ttu-id="69770-448">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="69770-448">Account description</span></span> | <span data-ttu-id="69770-449">Debet</span><span class="sxs-lookup"><span data-stu-id="69770-449">Debit</span></span>    | <span data-ttu-id="69770-450">Kredit</span><span class="sxs-lookup"><span data-stu-id="69770-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="69770-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="69770-451">Ledger</span></span>       | <span data-ttu-id="69770-452">4</span><span class="sxs-lookup"><span data-stu-id="69770-452">4</span></span>              | <span data-ttu-id="69770-453">Vlastní</span><span class="sxs-lookup"><span data-stu-id="69770-453">Custom</span></span> | <span data-ttu-id="69770-454">Clearingový účet</span><span class="sxs-lookup"><span data-stu-id="69770-454">Clearing account</span></span>    | <span data-ttu-id="69770-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="69770-455">1,000.00</span></span> |          |
| <span data-ttu-id="69770-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="69770-456">Ledger</span></span>       | <span data-ttu-id="69770-457">1</span><span class="sxs-lookup"><span data-stu-id="69770-457">1</span></span>              | <span data-ttu-id="69770-458">Vlastní</span><span class="sxs-lookup"><span data-stu-id="69770-458">Custom</span></span> | <span data-ttu-id="69770-459">Výdaje leasingu</span><span class="sxs-lookup"><span data-stu-id="69770-459">Lease expense</span></span>       |          | <span data-ttu-id="69770-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="69770-460">1,000.00</span></span> |

<span data-ttu-id="69770-461">Nyní, když jste vyloučili položky statutárního deníku, zarezervujete všechny položky deníku, které vyžadují IFRS 16 v knize IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="69770-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="69770-462">Mezi tyto položky patří počáteční uznání používaného majetku a záznam úroků a odpisů.</span><span class="sxs-lookup"><span data-stu-id="69770-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="69770-463">Počáteční uznání – 1. 1. 2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="69770-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="69770-464">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="69770-464">Account type</span></span> | <span data-ttu-id="69770-465">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="69770-465">Account number</span></span> | <span data-ttu-id="69770-466">Vrstva</span><span class="sxs-lookup"><span data-stu-id="69770-466">Layer</span></span>  | <span data-ttu-id="69770-467">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="69770-467">Account description</span></span>      | <span data-ttu-id="69770-468">Debet</span><span class="sxs-lookup"><span data-stu-id="69770-468">Debit</span></span>     | <span data-ttu-id="69770-469">Kredit</span><span class="sxs-lookup"><span data-stu-id="69770-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="69770-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="69770-470">Ledger</span></span>       | <span data-ttu-id="69770-471">6</span><span class="sxs-lookup"><span data-stu-id="69770-471">6</span></span>              | <span data-ttu-id="69770-472">Vlastní</span><span class="sxs-lookup"><span data-stu-id="69770-472">Custom</span></span> | <span data-ttu-id="69770-473">Používaný majetek</span><span class="sxs-lookup"><span data-stu-id="69770-473">ROU Asset</span></span>                | <span data-ttu-id="69770-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="69770-474">22,793.90</span></span> |           |
| <span data-ttu-id="69770-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="69770-475">Ledger</span></span>       | <span data-ttu-id="69770-476">7</span><span class="sxs-lookup"><span data-stu-id="69770-476">7</span></span>              | <span data-ttu-id="69770-477">Vlastní</span><span class="sxs-lookup"><span data-stu-id="69770-477">Custom</span></span> | <span data-ttu-id="69770-478">Povinnost finančního leasingu</span><span class="sxs-lookup"><span data-stu-id="69770-478">Finance lease obligation</span></span> |           | <span data-ttu-id="69770-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="69770-479">22,793.90</span></span> |

<span data-ttu-id="69770-480">Leasingová splátka je zaúčtována jako ostatní leasingové splátky.</span><span class="sxs-lookup"><span data-stu-id="69770-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="69770-481">Důvodem pro použití clearingového účtu je zajistit, aby byla hotovost připsána pouze jednou.</span><span class="sxs-lookup"><span data-stu-id="69770-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="69770-482">Leasingová splátka – 31. 1. 2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="69770-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="69770-483">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="69770-483">Account type</span></span> | <span data-ttu-id="69770-484">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="69770-484">Account number</span></span> | <span data-ttu-id="69770-485">Vrstva</span><span class="sxs-lookup"><span data-stu-id="69770-485">Layer</span></span>  | <span data-ttu-id="69770-486">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="69770-486">Account description</span></span>      | <span data-ttu-id="69770-487">Debet</span><span class="sxs-lookup"><span data-stu-id="69770-487">Debit</span></span>    | <span data-ttu-id="69770-488">Kredit</span><span class="sxs-lookup"><span data-stu-id="69770-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="69770-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="69770-489">Ledger</span></span>       | <span data-ttu-id="69770-490">7</span><span class="sxs-lookup"><span data-stu-id="69770-490">7</span></span>              | <span data-ttu-id="69770-491">Vlastní</span><span class="sxs-lookup"><span data-stu-id="69770-491">Custom</span></span> | <span data-ttu-id="69770-492">Povinnost finančního leasingu</span><span class="sxs-lookup"><span data-stu-id="69770-492">Finance lease obligation</span></span> | <span data-ttu-id="69770-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="69770-493">1,000.00</span></span> |          |
| <span data-ttu-id="69770-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="69770-494">Ledger</span></span>       | <span data-ttu-id="69770-495">4</span><span class="sxs-lookup"><span data-stu-id="69770-495">4</span></span>              | <span data-ttu-id="69770-496">Vlastní</span><span class="sxs-lookup"><span data-stu-id="69770-496">Custom</span></span> | <span data-ttu-id="69770-497">Clearingový účet</span><span class="sxs-lookup"><span data-stu-id="69770-497">Clearing account</span></span>         |          | <span data-ttu-id="69770-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="69770-498">1,000.00</span></span> |

<span data-ttu-id="69770-499">Položka deníku úrokových nákladů je generována z plánu amortizace závazků.</span><span class="sxs-lookup"><span data-stu-id="69770-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="69770-500">Úrokové náklady – 31. 1. 2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="69770-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="69770-501">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="69770-501">Account type</span></span> | <span data-ttu-id="69770-502">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="69770-502">Account number</span></span> | <span data-ttu-id="69770-503">Vrstva</span><span class="sxs-lookup"><span data-stu-id="69770-503">Layer</span></span>  | <span data-ttu-id="69770-504">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="69770-504">Account description</span></span>      | <span data-ttu-id="69770-505">Debet</span><span class="sxs-lookup"><span data-stu-id="69770-505">Debit</span></span> | <span data-ttu-id="69770-506">Kredit</span><span class="sxs-lookup"><span data-stu-id="69770-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="69770-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="69770-507">Ledger</span></span>       | <span data-ttu-id="69770-508">8</span><span class="sxs-lookup"><span data-stu-id="69770-508">8</span></span>              | <span data-ttu-id="69770-509">Vlastní</span><span class="sxs-lookup"><span data-stu-id="69770-509">Custom</span></span> | <span data-ttu-id="69770-510">Výdaje na úroky</span><span class="sxs-lookup"><span data-stu-id="69770-510">Interest expense</span></span>         | <span data-ttu-id="69770-511">94.97</span><span class="sxs-lookup"><span data-stu-id="69770-511">94.97</span></span> |        |
| <span data-ttu-id="69770-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="69770-512">Ledger</span></span>       | <span data-ttu-id="69770-513">7</span><span class="sxs-lookup"><span data-stu-id="69770-513">7</span></span>              | <span data-ttu-id="69770-514">Vlastní</span><span class="sxs-lookup"><span data-stu-id="69770-514">Custom</span></span> | <span data-ttu-id="69770-515">Povinnost finančního leasingu</span><span class="sxs-lookup"><span data-stu-id="69770-515">Finance lease obligation</span></span> |       | <span data-ttu-id="69770-516">94.97</span><span class="sxs-lookup"><span data-stu-id="69770-516">94.97</span></span>  |

<span data-ttu-id="69770-517">Položka deníku odpisových výdajů je generována z plánu odpisu majetku.</span><span class="sxs-lookup"><span data-stu-id="69770-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="69770-518">Odpisové výdaje – 31. 1. 2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="69770-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="69770-519">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="69770-519">Account type</span></span> | <span data-ttu-id="69770-520">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="69770-520">Account number</span></span> | <span data-ttu-id="69770-521">Vrstva</span><span class="sxs-lookup"><span data-stu-id="69770-521">Layer</span></span>  | <span data-ttu-id="69770-522">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="69770-522">Account description</span></span>      | <span data-ttu-id="69770-523">Debet</span><span class="sxs-lookup"><span data-stu-id="69770-523">Debit</span></span>  | <span data-ttu-id="69770-524">Kredit</span><span class="sxs-lookup"><span data-stu-id="69770-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="69770-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="69770-525">Ledger</span></span>       | <span data-ttu-id="69770-526">10</span><span class="sxs-lookup"><span data-stu-id="69770-526">10</span></span>             | <span data-ttu-id="69770-527">Vlastní</span><span class="sxs-lookup"><span data-stu-id="69770-527">Custom</span></span> | <span data-ttu-id="69770-528">Odpisové výdaje</span><span class="sxs-lookup"><span data-stu-id="69770-528">Depreciation expense</span></span>     | <span data-ttu-id="69770-529">949.75</span><span class="sxs-lookup"><span data-stu-id="69770-529">949.75</span></span> |        |
| <span data-ttu-id="69770-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="69770-530">Ledger</span></span>       | <span data-ttu-id="69770-531">11</span><span class="sxs-lookup"><span data-stu-id="69770-531">11</span></span>             | <span data-ttu-id="69770-532">Vlastní</span><span class="sxs-lookup"><span data-stu-id="69770-532">Custom</span></span> | <span data-ttu-id="69770-533">Akumulovaný odpis</span><span class="sxs-lookup"><span data-stu-id="69770-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="69770-534">949.75</span><span class="sxs-lookup"><span data-stu-id="69770-534">949.75</span></span> |

<span data-ttu-id="69770-535">Po vytvoření a zaúčtování všech těchto položek deníku se zobrazí následující hodnoty „vlastní vrstvy 1“.</span><span class="sxs-lookup"><span data-stu-id="69770-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="69770-536">Všimněte si, že poslední sloupec obsahuje bankovní poplatek, výdaj na daň z přidané hodnoty (DPH) a snížení hotovosti z předchozí vrstvy, ale nezahrnuje položky deníku pro statutární vykazování.</span><span class="sxs-lookup"><span data-stu-id="69770-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="69770-537">Proto dosáhnete skutečného využití možností duálního hlášení.</span><span class="sxs-lookup"><span data-stu-id="69770-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="69770-538">V tomto okamžiku musí společnost spustit předvahu a zkombinovat aktuální a vlastní vrstvu, aby vytvořila předvahu podle IFRS.</span><span class="sxs-lookup"><span data-stu-id="69770-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="69770-539">Č. účtu</span><span class="sxs-lookup"><span data-stu-id="69770-539">Account No</span></span> | <span data-ttu-id="69770-540">popis</span><span class="sxs-lookup"><span data-stu-id="69770-540">Description</span></span>              | <span data-ttu-id="69770-541">Statutární kniha\-Aktuální vrstva\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="69770-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="69770-542">Statutární kniha\-Aktuální vrstva\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="69770-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="69770-543">Statutární kniha\-Aktuální vrstva\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="69770-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="69770-544">Aktuální vrstva \- Celkem</span><span class="sxs-lookup"><span data-stu-id="69770-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="69770-545">Stornovací kniha\-Vlastní vrstva\-JE\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="69770-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="69770-546">Kniha IFRS 16\-Vlastní vrstva\-JE\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="69770-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="69770-547">Kniha IFRS 16\-Vlastní vrstva\-JE\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="69770-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="69770-548">Kniha IFRS 16\-Vlastní vrstva\-JE\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="69770-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="69770-549">Kniha IFRS 16\-Vlastní vrstva\-JE\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="69770-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="69770-550">Vlastní vrstva \+ Vlastní vrstva \- Celkem</span><span class="sxs-lookup"><span data-stu-id="69770-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="69770-551">1</span><span class="sxs-lookup"><span data-stu-id="69770-551">1</span></span>          | <span data-ttu-id="69770-552">Výdaje leasingu</span><span class="sxs-lookup"><span data-stu-id="69770-552">Lease expense</span></span>            | <span data-ttu-id="69770-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="69770-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="69770-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="69770-554">1,000\.00</span></span>               |   | <span data-ttu-id="69770-555">\-1000</span><span class="sxs-lookup"><span data-stu-id="69770-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="69770-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="69770-556">0\.00</span></span>                                   |
| <span data-ttu-id="69770-557">2</span><span class="sxs-lookup"><span data-stu-id="69770-557">2</span></span>          | <span data-ttu-id="69770-558">Bankovní poplatek</span><span class="sxs-lookup"><span data-stu-id="69770-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="69770-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="69770-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="69770-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="69770-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="69770-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="69770-561">3\.00</span></span>                                   |
| <span data-ttu-id="69770-562">3</span><span class="sxs-lookup"><span data-stu-id="69770-562">3</span></span>          | <span data-ttu-id="69770-563">Výdaje DPH</span><span class="sxs-lookup"><span data-stu-id="69770-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="69770-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="69770-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="69770-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="69770-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="69770-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="69770-566">5\.00</span></span>                                   |
| <span data-ttu-id="69770-567">4</span><span class="sxs-lookup"><span data-stu-id="69770-567">4</span></span>          | <span data-ttu-id="69770-568">Clearingový účet</span><span class="sxs-lookup"><span data-stu-id="69770-568">Clearing account</span></span>         | <span data-ttu-id="69770-569">\-1000\.00</span><span class="sxs-lookup"><span data-stu-id="69770-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="69770-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="69770-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="69770-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="69770-571">0\.00</span></span>                   |   | <span data-ttu-id="69770-572">1 000</span><span class="sxs-lookup"><span data-stu-id="69770-572">1,000</span></span>                                           |                                                | <span data-ttu-id="69770-573">\-1000</span><span class="sxs-lookup"><span data-stu-id="69770-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="69770-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="69770-574">0\.00</span></span>                                   |
| <span data-ttu-id="69770-575">5</span><span class="sxs-lookup"><span data-stu-id="69770-575">5</span></span>          | <span data-ttu-id="69770-576">Závazky</span><span class="sxs-lookup"><span data-stu-id="69770-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="69770-577">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="69770-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="69770-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="69770-578">1,008\.00</span></span>                                         | <span data-ttu-id="69770-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="69770-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="69770-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="69770-580">0\.00</span></span>                                   |
| <span data-ttu-id="69770-581">6</span><span class="sxs-lookup"><span data-stu-id="69770-581">6</span></span>          | <span data-ttu-id="69770-582">Používaný majetek</span><span class="sxs-lookup"><span data-stu-id="69770-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="69770-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="69770-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="69770-584">22,794</span><span class="sxs-lookup"><span data-stu-id="69770-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="69770-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="69770-585">22,793\.90</span></span>                              |
| <span data-ttu-id="69770-586">7</span><span class="sxs-lookup"><span data-stu-id="69770-586">7</span></span>          | <span data-ttu-id="69770-587">Povinnost finančního leasingu</span><span class="sxs-lookup"><span data-stu-id="69770-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="69770-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="69770-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="69770-589">\-22 794</span><span class="sxs-lookup"><span data-stu-id="69770-589">\-22,794</span></span>                                       | <span data-ttu-id="69770-590">1 000</span><span class="sxs-lookup"><span data-stu-id="69770-590">1,000</span></span>                                          | <span data-ttu-id="69770-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="69770-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="69770-592">\-21 888\.87</span><span class="sxs-lookup"><span data-stu-id="69770-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="69770-593">8</span><span class="sxs-lookup"><span data-stu-id="69770-593">8</span></span>          | <span data-ttu-id="69770-594">Výdaje na úroky</span><span class="sxs-lookup"><span data-stu-id="69770-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="69770-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="69770-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="69770-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="69770-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="69770-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="69770-597">94\.97</span></span>                                  |
| <span data-ttu-id="69770-598">9</span><span class="sxs-lookup"><span data-stu-id="69770-598">9</span></span>          | <span data-ttu-id="69770-599">Hotovost</span><span class="sxs-lookup"><span data-stu-id="69770-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="69770-600">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="69770-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="69770-601">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="69770-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="69770-602">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="69770-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="69770-603">10</span><span class="sxs-lookup"><span data-stu-id="69770-603">10</span></span>         | <span data-ttu-id="69770-604">Odpisové výdaje</span><span class="sxs-lookup"><span data-stu-id="69770-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="69770-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="69770-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="69770-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="69770-606">949\.75</span></span>                                        | <span data-ttu-id="69770-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="69770-607">949\.75</span></span>                                 |
| <span data-ttu-id="69770-608">11</span><span class="sxs-lookup"><span data-stu-id="69770-608">11</span></span>         | <span data-ttu-id="69770-609">Akumulovaný odpis</span><span class="sxs-lookup"><span data-stu-id="69770-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="69770-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="69770-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="69770-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="69770-611">\-949\.75</span></span>                                      | <span data-ttu-id="69770-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="69770-612">\-949\.75</span></span>                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
