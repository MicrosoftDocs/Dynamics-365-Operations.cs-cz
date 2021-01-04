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
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 96e1d4d460aef2f74422d5e4bd4fc68255466455
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4441343"
---
# <a name="dual-reporting"></a><span data-ttu-id="d46bd-103">Duální vykazování</span><span class="sxs-lookup"><span data-stu-id="d46bd-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d46bd-104">Toto téma vás provede příkladem, který ukazuje, jak můžete splnit požadavky jak pro vykazování podle Mezinárodního standardu finančního výkaznictví (IFRS), tak pro statutární vykazování v leasingu majetku.</span><span class="sxs-lookup"><span data-stu-id="d46bd-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="d46bd-105">Znalost účtovacích vrstev v Microsoft Dynamics 365 Finance je nutná a příklad bude lépe srozumitelný.</span><span class="sxs-lookup"><span data-stu-id="d46bd-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="d46bd-106">Příklad</span><span class="sxs-lookup"><span data-stu-id="d46bd-106">Example</span></span>

<span data-ttu-id="d46bd-107">Následující příklad provádí účtování pro leasing podle italského statutárního výkaznictví pomocí metody hotovostního základu i metod vykazování podle IFRS.</span><span class="sxs-lookup"><span data-stu-id="d46bd-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="d46bd-108">Společnost musí založit tři účetní knihy, které zohlední jak italské zákonné požadavky, tak požadavky IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="d46bd-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="d46bd-109">Jedna kniha je vyžadována pro IFRS 16, jedna kniha je vyžadována pro zákonné požadavky a jedna kniha je vyžadována k automatickému stornování statutárních účtování.</span><span class="sxs-lookup"><span data-stu-id="d46bd-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="d46bd-110">Knihy jsou vytvořeny tak, jak je uvedeno v následujících tabulkách.</span><span class="sxs-lookup"><span data-stu-id="d46bd-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="d46bd-111">**Kniha IFRS 16**</span><span class="sxs-lookup"><span data-stu-id="d46bd-111">**IFRS 16 book**</span></span>

<span data-ttu-id="d46bd-112">Kniha IFRS 16 je vytvořena v souladu s účetním standardem IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="d46bd-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="d46bd-113">Všechny položky, které jsou zaúčtovány v této knize, budou zaúčtovány do vlastní vrstvy.</span><span class="sxs-lookup"><span data-stu-id="d46bd-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="d46bd-114">Jméno</span><span class="sxs-lookup"><span data-stu-id="d46bd-114">Name</span></span>                                    | <span data-ttu-id="d46bd-115">popis</span><span class="sxs-lookup"><span data-stu-id="d46bd-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="d46bd-116">Typ knihy</span><span class="sxs-lookup"><span data-stu-id="d46bd-116">Book type</span></span>                               | <span data-ttu-id="d46bd-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="d46bd-117">IFRS 16</span></span>        |
| <span data-ttu-id="d46bd-118">Popis knihy</span><span class="sxs-lookup"><span data-stu-id="d46bd-118">Book description</span></span>                        | <span data-ttu-id="d46bd-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="d46bd-119">IFRS 16</span></span>        |
| <span data-ttu-id="d46bd-120">Účtovací vrstva</span><span class="sxs-lookup"><span data-stu-id="d46bd-120">Posting Layer</span></span>                           | <span data-ttu-id="d46bd-121">Vlastní vrstva 1</span><span class="sxs-lookup"><span data-stu-id="d46bd-121">Custom layer 1</span></span> |
| <span data-ttu-id="d46bd-122">Typ leasingu</span><span class="sxs-lookup"><span data-stu-id="d46bd-122">Lease Type</span></span>                              | <span data-ttu-id="d46bd-123">Finance</span><span class="sxs-lookup"><span data-stu-id="d46bd-123">Finance</span></span>        |
| <span data-ttu-id="d46bd-124">Rámec účetnictví</span><span class="sxs-lookup"><span data-stu-id="d46bd-124">Accounting Framework</span></span>                    | <span data-ttu-id="d46bd-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="d46bd-125">IFRS 16</span></span>        |
| <span data-ttu-id="d46bd-126">Nastavení doby trvání leasingu / očekávané doby použitelnosti</span><span class="sxs-lookup"><span data-stu-id="d46bd-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="d46bd-127">0,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-127">0.00</span></span>           |
| <span data-ttu-id="d46bd-128">Nastavení současné hodnoty / reálné hodnoty majetku</span><span class="sxs-lookup"><span data-stu-id="d46bd-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="d46bd-129">0,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-129">0.00</span></span>           |
| <span data-ttu-id="d46bd-130">Krátkodobá prahová hodnota</span><span class="sxs-lookup"><span data-stu-id="d46bd-130">Short-term threshold</span></span>                    | <span data-ttu-id="d46bd-131">12</span><span class="sxs-lookup"><span data-stu-id="d46bd-131">12</span></span>             |
| <span data-ttu-id="d46bd-132">Nízká prahová hodnota</span><span class="sxs-lookup"><span data-stu-id="d46bd-132">Low Value Threshold</span></span>                     | <span data-ttu-id="d46bd-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-133">5,000.00</span></span>       |
| <span data-ttu-id="d46bd-134">Platba dodavateli</span><span class="sxs-lookup"><span data-stu-id="d46bd-134">Pay to Vendor</span></span>                           | <span data-ttu-id="d46bd-135">Žádný</span><span class="sxs-lookup"><span data-stu-id="d46bd-135">No</span></span>             |

<span data-ttu-id="d46bd-136">**Statutární kniha**</span><span class="sxs-lookup"><span data-stu-id="d46bd-136">**Statutory book**</span></span>

<span data-ttu-id="d46bd-137">Statutární kniha je hotovostní kniha, kde společnost bude účtovat výdaje na leasing jako částku hotovosti, která se každý měsíc platí za nájem.</span><span class="sxs-lookup"><span data-stu-id="d46bd-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="d46bd-138">Tato kniha nevytvoří používaný majetek ani leasingový závazek.</span><span class="sxs-lookup"><span data-stu-id="d46bd-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="d46bd-139">Jméno</span><span class="sxs-lookup"><span data-stu-id="d46bd-139">Name</span></span>                                    | <span data-ttu-id="d46bd-140">popis</span><span class="sxs-lookup"><span data-stu-id="d46bd-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="d46bd-141">Typ knihy</span><span class="sxs-lookup"><span data-stu-id="d46bd-141">Book type</span></span>                               | <span data-ttu-id="d46bd-142">Statutární</span><span class="sxs-lookup"><span data-stu-id="d46bd-142">Statutory</span></span>   |
| <span data-ttu-id="d46bd-143">Popis knihy</span><span class="sxs-lookup"><span data-stu-id="d46bd-143">Book description</span></span>                        | <span data-ttu-id="d46bd-144">Místní GAAP</span><span class="sxs-lookup"><span data-stu-id="d46bd-144">Local GAAP</span></span>  |
| <span data-ttu-id="d46bd-145">Účtovací vrstva</span><span class="sxs-lookup"><span data-stu-id="d46bd-145">Posting Layer</span></span>                           | <span data-ttu-id="d46bd-146">Aktuální</span><span class="sxs-lookup"><span data-stu-id="d46bd-146">Current</span></span>     |
| <span data-ttu-id="d46bd-147">Typ leasingu</span><span class="sxs-lookup"><span data-stu-id="d46bd-147">Lease Type</span></span>                              | <span data-ttu-id="d46bd-148">Automatické</span><span class="sxs-lookup"><span data-stu-id="d46bd-148">Automatic</span></span>   |
| <span data-ttu-id="d46bd-149">Rámec účetnictví</span><span class="sxs-lookup"><span data-stu-id="d46bd-149">Accounting Framework</span></span>                    | <span data-ttu-id="d46bd-150">Hotovostní základ</span><span class="sxs-lookup"><span data-stu-id="d46bd-150">Cash basis</span></span>  |
| <span data-ttu-id="d46bd-151">Nastavení doby trvání leasingu / očekávané doby použitelnosti</span><span class="sxs-lookup"><span data-stu-id="d46bd-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="d46bd-152">0,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-152">0.00</span></span>        |
| <span data-ttu-id="d46bd-153">Nastavení současné hodnoty / reálné hodnoty majetku</span><span class="sxs-lookup"><span data-stu-id="d46bd-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="d46bd-154">0,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-154">0.00</span></span>        |
| <span data-ttu-id="d46bd-155">Krátkodobá prahová hodnota</span><span class="sxs-lookup"><span data-stu-id="d46bd-155">Short-term threshold</span></span>                    | <span data-ttu-id="d46bd-156">0</span><span class="sxs-lookup"><span data-stu-id="d46bd-156">0</span></span>           |
| <span data-ttu-id="d46bd-157">Nízká prahová hodnota</span><span class="sxs-lookup"><span data-stu-id="d46bd-157">Low Value Threshold</span></span>                     | <span data-ttu-id="d46bd-158">0</span><span class="sxs-lookup"><span data-stu-id="d46bd-158">0</span></span>           |
| <span data-ttu-id="d46bd-159">Platba dodavateli</span><span class="sxs-lookup"><span data-stu-id="d46bd-159">Pay to Vendor</span></span>                           | <span data-ttu-id="d46bd-160">Žádný</span><span class="sxs-lookup"><span data-stu-id="d46bd-160">No</span></span>          |

<span data-ttu-id="d46bd-161">**Statutární stornovací kniha**</span><span class="sxs-lookup"><span data-stu-id="d46bd-161">**Statutory reversal book**</span></span>

<span data-ttu-id="d46bd-162">Statutární stornovací kniha je sestavena stejným způsobem jako statutární kniha.</span><span class="sxs-lookup"><span data-stu-id="d46bd-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="d46bd-163">Jméno</span><span class="sxs-lookup"><span data-stu-id="d46bd-163">Name</span></span>                                    | <span data-ttu-id="d46bd-164">popis</span><span class="sxs-lookup"><span data-stu-id="d46bd-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="d46bd-165">Typ knihy</span><span class="sxs-lookup"><span data-stu-id="d46bd-165">Book type</span></span>                               | <span data-ttu-id="d46bd-166">Statutární – storno</span><span class="sxs-lookup"><span data-stu-id="d46bd-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="d46bd-167">Popis knihy</span><span class="sxs-lookup"><span data-stu-id="d46bd-167">Book description</span></span>                        | <span data-ttu-id="d46bd-168">Kniha pro stornování statutární knihy</span><span class="sxs-lookup"><span data-stu-id="d46bd-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="d46bd-169">Účtovací vrstva</span><span class="sxs-lookup"><span data-stu-id="d46bd-169">Posting Layer</span></span>                           | <span data-ttu-id="d46bd-170">Vlastní vrstva 1</span><span class="sxs-lookup"><span data-stu-id="d46bd-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="d46bd-171">Typ leasingu</span><span class="sxs-lookup"><span data-stu-id="d46bd-171">Lease Type</span></span>                              | <span data-ttu-id="d46bd-172">Automatické</span><span class="sxs-lookup"><span data-stu-id="d46bd-172">Automatic</span></span>                      |
| <span data-ttu-id="d46bd-173">Rámec účetnictví</span><span class="sxs-lookup"><span data-stu-id="d46bd-173">Accounting Framework</span></span>                    | <span data-ttu-id="d46bd-174">Hotovostní základ</span><span class="sxs-lookup"><span data-stu-id="d46bd-174">Cash basis</span></span>                     |
| <span data-ttu-id="d46bd-175">Nastavení doby trvání leasingu / očekávané doby použitelnosti</span><span class="sxs-lookup"><span data-stu-id="d46bd-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="d46bd-176">0,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-176">0.00</span></span>                           |
| <span data-ttu-id="d46bd-177">Nastavení současné hodnoty / reálné hodnoty majetku</span><span class="sxs-lookup"><span data-stu-id="d46bd-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="d46bd-178">0,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-178">0.00</span></span>                           |
| <span data-ttu-id="d46bd-179">Krátkodobá prahová hodnota</span><span class="sxs-lookup"><span data-stu-id="d46bd-179">Short-term threshold</span></span>                    | <span data-ttu-id="d46bd-180">0</span><span class="sxs-lookup"><span data-stu-id="d46bd-180">0</span></span>                              |
| <span data-ttu-id="d46bd-181">Nízká prahová hodnota</span><span class="sxs-lookup"><span data-stu-id="d46bd-181">Low Value Threshold</span></span>                     | <span data-ttu-id="d46bd-182">0</span><span class="sxs-lookup"><span data-stu-id="d46bd-182">0</span></span>                              |
| <span data-ttu-id="d46bd-183">Platba dodavateli</span><span class="sxs-lookup"><span data-stu-id="d46bd-183">Pay to Vendor</span></span>                           | <span data-ttu-id="d46bd-184">Žádný</span><span class="sxs-lookup"><span data-stu-id="d46bd-184">No</span></span>                             |

<span data-ttu-id="d46bd-185">V tomto příkladu byl vytvořen leasing, který má následující nastavení na kartách **Obecné** a **Řádky platebního kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="d46bd-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="d46bd-186">**Karta Obecné**</span><span class="sxs-lookup"><span data-stu-id="d46bd-186">**General tab**</span></span>

| <span data-ttu-id="d46bd-187">Pole</span><span class="sxs-lookup"><span data-stu-id="d46bd-187">Field</span></span>                      | <span data-ttu-id="d46bd-188">Hodnota</span><span class="sxs-lookup"><span data-stu-id="d46bd-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="d46bd-189">Přírůstková výpůjční úroková sazba</span><span class="sxs-lookup"><span data-stu-id="d46bd-189">Incremental borrowing rate</span></span> | <span data-ttu-id="d46bd-190">5 %</span><span class="sxs-lookup"><span data-stu-id="d46bd-190">5%</span></span>               |
| <span data-ttu-id="d46bd-191">Datum zahájení</span><span class="sxs-lookup"><span data-stu-id="d46bd-191">Commencement date</span></span>          | <span data-ttu-id="d46bd-192">1. 1. 2020</span><span class="sxs-lookup"><span data-stu-id="d46bd-192">1/1/2020</span></span>         |
| <span data-ttu-id="d46bd-193">Skupina leasingu</span><span class="sxs-lookup"><span data-stu-id="d46bd-193">Lease group</span></span>                | <span data-ttu-id="d46bd-194">Budovy</span><span class="sxs-lookup"><span data-stu-id="d46bd-194">Buildings</span></span>        |
| <span data-ttu-id="d46bd-195">Dodavatel</span><span class="sxs-lookup"><span data-stu-id="d46bd-195">Vendor</span></span>                     | <span data-ttu-id="d46bd-196">1001</span><span class="sxs-lookup"><span data-stu-id="d46bd-196">1001</span></span>             |
| <span data-ttu-id="d46bd-197">Reálná hodnota majetku</span><span class="sxs-lookup"><span data-stu-id="d46bd-197">Fair value of the asset</span></span>    | <span data-ttu-id="d46bd-198">245,000</span><span class="sxs-lookup"><span data-stu-id="d46bd-198">245,000</span></span>          |
| <span data-ttu-id="d46bd-199">Očekávaná doba použitelnosti majetku</span><span class="sxs-lookup"><span data-stu-id="d46bd-199">Asset useful life</span></span>          | <span data-ttu-id="d46bd-200">120</span><span class="sxs-lookup"><span data-stu-id="d46bd-200">120</span></span>              |
| <span data-ttu-id="d46bd-201">Typ anuity</span><span class="sxs-lookup"><span data-stu-id="d46bd-201">Annuity type</span></span>               | <span data-ttu-id="d46bd-202">Běžná anuita</span><span class="sxs-lookup"><span data-stu-id="d46bd-202">Ordinary annuity</span></span> |
| <span data-ttu-id="d46bd-203">Interval úročení</span><span class="sxs-lookup"><span data-stu-id="d46bd-203">Compounding interval</span></span>       | <span data-ttu-id="d46bd-204">Měsíčně</span><span class="sxs-lookup"><span data-stu-id="d46bd-204">Monthly</span></span>          |

<span data-ttu-id="d46bd-205">**Karta Řádky platebního kalendáře**</span><span class="sxs-lookup"><span data-stu-id="d46bd-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="d46bd-206">Pole</span><span class="sxs-lookup"><span data-stu-id="d46bd-206">Field</span></span>             | <span data-ttu-id="d46bd-207">Hodnota</span><span class="sxs-lookup"><span data-stu-id="d46bd-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="d46bd-208">Počáteční datum</span><span class="sxs-lookup"><span data-stu-id="d46bd-208">Start date</span></span>        | <span data-ttu-id="d46bd-209">1. 1. 2020</span><span class="sxs-lookup"><span data-stu-id="d46bd-209">1/1/2020</span></span>   |
| <span data-ttu-id="d46bd-210">Interval období</span><span class="sxs-lookup"><span data-stu-id="d46bd-210">Period interval</span></span>   | <span data-ttu-id="d46bd-211">Měsíce</span><span class="sxs-lookup"><span data-stu-id="d46bd-211">Months</span></span>     |
| <span data-ttu-id="d46bd-212">Období</span><span class="sxs-lookup"><span data-stu-id="d46bd-212">Periods</span></span>           | <span data-ttu-id="d46bd-213">24</span><span class="sxs-lookup"><span data-stu-id="d46bd-213">24</span></span>         |
| <span data-ttu-id="d46bd-214">Koncové datum</span><span class="sxs-lookup"><span data-stu-id="d46bd-214">End date</span></span>          | <span data-ttu-id="d46bd-215">31. 12. 2020</span><span class="sxs-lookup"><span data-stu-id="d46bd-215">12/31/2020</span></span> |
| <span data-ttu-id="d46bd-216">Četnost plateb</span><span class="sxs-lookup"><span data-stu-id="d46bd-216">Payment frequency</span></span> | <span data-ttu-id="d46bd-217">Měsíčně</span><span class="sxs-lookup"><span data-stu-id="d46bd-217">Monthly</span></span>    |
| <span data-ttu-id="d46bd-218">Částka platby</span><span class="sxs-lookup"><span data-stu-id="d46bd-218">Payment amount</span></span>    | <span data-ttu-id="d46bd-219">1 000</span><span class="sxs-lookup"><span data-stu-id="d46bd-219">1,000</span></span>      |

<span data-ttu-id="d46bd-220">Chcete-li tento leasing započítat do dvou rámců, použijete aktuální účtovací vrstvu a vlastní účtovací vrstvu.</span><span class="sxs-lookup"><span data-stu-id="d46bd-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="d46bd-221">Následující tabulka ukazuje příklad každé položky deníku, která je potřeba pro věrné zobrazení financí podle každého standardu výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="d46bd-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="d46bd-222">Podrobný popis každé položky deníku pro první měsíc leasingu je poskytnut později.</span><span class="sxs-lookup"><span data-stu-id="d46bd-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="d46bd-223">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="d46bd-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="d46bd-224">popis</span><span class="sxs-lookup"><span data-stu-id="d46bd-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="d46bd-225">Statutární kniha (aktuální vrstva)</span><span class="sxs-lookup"><span data-stu-id="d46bd-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="d46bd-226">Celková aktuální vrstva</span><span class="sxs-lookup"><span data-stu-id="d46bd-226">Current layer total</span></span></th>
<th><span data-ttu-id="d46bd-227">Stornovací kniha (vlastní vrstva)</span><span class="sxs-lookup"><span data-stu-id="d46bd-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="d46bd-228">Kniha IFRS 16 (vlastní vrstva)</span><span class="sxs-lookup"><span data-stu-id="d46bd-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="d46bd-229">Aktuální vrstva + vlastní vrstva celkem</span><span class="sxs-lookup"><span data-stu-id="d46bd-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d46bd-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="d46bd-230">JE-100</span></span></th>
<th><span data-ttu-id="d46bd-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="d46bd-231">JE-110</span></span></th>
<th><span data-ttu-id="d46bd-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="d46bd-232">JE-120</span></span></th>
<th><span data-ttu-id="d46bd-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="d46bd-233">JE-130</span></span></th>
<th><span data-ttu-id="d46bd-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="d46bd-234">JE-140</span></span></th>
<th><span data-ttu-id="d46bd-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="d46bd-235">JE-150</span></span></th>
<th><span data-ttu-id="d46bd-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="d46bd-236">JE-160</span></span></th>
<th><span data-ttu-id="d46bd-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="d46bd-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d46bd-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="d46bd-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="d46bd-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="d46bd-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="d46bd-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="d46bd-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="d46bd-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="d46bd-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="d46bd-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="d46bd-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="d46bd-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="d46bd-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="d46bd-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="d46bd-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="d46bd-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="d46bd-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d46bd-246">1</span><span class="sxs-lookup"><span data-stu-id="d46bd-246">1</span></span></td>
<td><span data-ttu-id="d46bd-247">Výdaje leasingu</span><span class="sxs-lookup"><span data-stu-id="d46bd-247">Lease expense</span></span></td>
<td><span data-ttu-id="d46bd-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="d46bd-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-249">1,000.00</span></span></td>
<td><span data-ttu-id="d46bd-250">−1 000,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d46bd-251">0,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d46bd-252">2</span><span class="sxs-lookup"><span data-stu-id="d46bd-252">2</span></span></td>
<td><span data-ttu-id="d46bd-253">Bankovní poplatek</span><span class="sxs-lookup"><span data-stu-id="d46bd-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="d46bd-254">3.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="d46bd-255">3.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d46bd-256">3.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d46bd-257">3</span><span class="sxs-lookup"><span data-stu-id="d46bd-257">3</span></span></td>
<td><span data-ttu-id="d46bd-258">Výdaje DPH</span><span class="sxs-lookup"><span data-stu-id="d46bd-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="d46bd-259">5.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="d46bd-260">5.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d46bd-261">5.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d46bd-262">4</span><span class="sxs-lookup"><span data-stu-id="d46bd-262">4</span></span></td>
<td><span data-ttu-id="d46bd-263">Clearingový účet</span><span class="sxs-lookup"><span data-stu-id="d46bd-263">Clearing account</span></span></td>
<td><span data-ttu-id="d46bd-264">−1 000,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-264">-1,000.00</span></span></td>
<td><span data-ttu-id="d46bd-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="d46bd-266">0,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-266">0.00</span></span></td>
<td><span data-ttu-id="d46bd-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="d46bd-268">−1 000,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="d46bd-269">0,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d46bd-270">5</span><span class="sxs-lookup"><span data-stu-id="d46bd-270">5</span></span></td>
<td><span data-ttu-id="d46bd-271">Závazky</span><span class="sxs-lookup"><span data-stu-id="d46bd-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="d46bd-272">-1008,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-272">-1,008.00</span></span></td>
<td><span data-ttu-id="d46bd-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-273">1,008.00</span></span></td>
<td><span data-ttu-id="d46bd-274">0,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d46bd-275">0,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d46bd-276">6</span><span class="sxs-lookup"><span data-stu-id="d46bd-276">6</span></span></td>
<td><span data-ttu-id="d46bd-277">Používaný majetek</span><span class="sxs-lookup"><span data-stu-id="d46bd-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d46bd-278">0,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="d46bd-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d46bd-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="d46bd-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d46bd-281">7</span><span class="sxs-lookup"><span data-stu-id="d46bd-281">7</span></span></td>
<td><span data-ttu-id="d46bd-282">Povinnost finančního leasingu</span><span class="sxs-lookup"><span data-stu-id="d46bd-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d46bd-283">0,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="d46bd-284">-22 794,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-284">-22,794.00</span></span></td>
<td><span data-ttu-id="d46bd-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-285">1,000.00</span></span></td>
<td><span data-ttu-id="d46bd-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="d46bd-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="d46bd-287">-21 888,87</span><span class="sxs-lookup"><span data-stu-id="d46bd-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d46bd-288">8</span><span class="sxs-lookup"><span data-stu-id="d46bd-288">8</span></span></td>
<td><span data-ttu-id="d46bd-289">Výdaje na úroky</span><span class="sxs-lookup"><span data-stu-id="d46bd-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d46bd-290">0,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d46bd-291">94.97</span><span class="sxs-lookup"><span data-stu-id="d46bd-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="d46bd-292">94.97</span><span class="sxs-lookup"><span data-stu-id="d46bd-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d46bd-293">9</span><span class="sxs-lookup"><span data-stu-id="d46bd-293">9</span></span></td>
<td><span data-ttu-id="d46bd-294">Hotovost</span><span class="sxs-lookup"><span data-stu-id="d46bd-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="d46bd-295">-1008,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-295">-1,008.00</span></span></td>
<td><span data-ttu-id="d46bd-296">-1008,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d46bd-297">-1008,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d46bd-298">10</span><span class="sxs-lookup"><span data-stu-id="d46bd-298">10</span></span></td>
<td><span data-ttu-id="d46bd-299">Odpisové výdaje</span><span class="sxs-lookup"><span data-stu-id="d46bd-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d46bd-300">0,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d46bd-301">949.75</span><span class="sxs-lookup"><span data-stu-id="d46bd-301">949.75</span></span></td>
<td><span data-ttu-id="d46bd-302">949.75</span><span class="sxs-lookup"><span data-stu-id="d46bd-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d46bd-303">11</span><span class="sxs-lookup"><span data-stu-id="d46bd-303">11</span></span></td>
<td><span data-ttu-id="d46bd-304">Akumulovaný odpis</span><span class="sxs-lookup"><span data-stu-id="d46bd-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d46bd-305">0,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d46bd-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="d46bd-306">-949.75</span></span></td>
<td><span data-ttu-id="d46bd-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="d46bd-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d46bd-308">Jak ukazuje předchozí tabulka, jsou potřeba tři knihy pro vykazování v rámci statutárního výkaznictví i výkaznictví podle IFRS.</span><span class="sxs-lookup"><span data-stu-id="d46bd-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="d46bd-309">Statutární kniha zaznamenává leasingové splátky podle pravidel pro hotovostní účetnictví v aktuální vrstvě.</span><span class="sxs-lookup"><span data-stu-id="d46bd-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="d46bd-310">Statutární stornovací kniha stornuje položky statutárního deníku.</span><span class="sxs-lookup"><span data-stu-id="d46bd-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="d46bd-311">Kniha IFRS 16 vytváří položky deníku, které jsou vyžadovány podle IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="d46bd-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="d46bd-312">Leasing musíte zadat pouze jednou.</span><span class="sxs-lookup"><span data-stu-id="d46bd-312">You must enter a lease only one time.</span></span> <span data-ttu-id="d46bd-313">Poté můžete otevřít stránku **Knihy**, kde jsou všechny knihy, které jsou přidruženy k leasingu.</span><span class="sxs-lookup"><span data-stu-id="d46bd-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="d46bd-314">Když vytvoříte knihy, všechny tři musí být přidruženy ke stejnému záznamu leasingu.</span><span class="sxs-lookup"><span data-stu-id="d46bd-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="d46bd-315">První položka deníku zaznamenává výdaje na leasing podle statutární knihy.</span><span class="sxs-lookup"><span data-stu-id="d46bd-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="d46bd-316">Platby můžete vytvářet v dávce nebo výběrem platebního kalendáře ve statutární knize.</span><span class="sxs-lookup"><span data-stu-id="d46bd-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="d46bd-317">V tomto příkladu se pro statutární knihu z platebního kalendáře vytvoří následující položka deníku.</span><span class="sxs-lookup"><span data-stu-id="d46bd-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="d46bd-318">Leasingová splátka – 31. 1. 2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="d46bd-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="d46bd-319">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="d46bd-319">Account type</span></span> | <span data-ttu-id="d46bd-320">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="d46bd-320">Account number</span></span> | <span data-ttu-id="d46bd-321">Vrstva</span><span class="sxs-lookup"><span data-stu-id="d46bd-321">Layer</span></span>   | <span data-ttu-id="d46bd-322">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="d46bd-322">Account description</span></span> | <span data-ttu-id="d46bd-323">Debet</span><span class="sxs-lookup"><span data-stu-id="d46bd-323">Debit</span></span>    | <span data-ttu-id="d46bd-324">Kredit</span><span class="sxs-lookup"><span data-stu-id="d46bd-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="d46bd-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="d46bd-325">Ledger</span></span>       | <span data-ttu-id="d46bd-326">1</span><span class="sxs-lookup"><span data-stu-id="d46bd-326">1</span></span>              | <span data-ttu-id="d46bd-327">Aktuální</span><span class="sxs-lookup"><span data-stu-id="d46bd-327">Current</span></span> | <span data-ttu-id="d46bd-328">Výdaje leasingu</span><span class="sxs-lookup"><span data-stu-id="d46bd-328">Lease expense</span></span>       | <span data-ttu-id="d46bd-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-329">1,000.00</span></span> |          |
| <span data-ttu-id="d46bd-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="d46bd-330">Ledger</span></span>       | <span data-ttu-id="d46bd-331">4</span><span class="sxs-lookup"><span data-stu-id="d46bd-331">4</span></span>              | <span data-ttu-id="d46bd-332">Aktuální</span><span class="sxs-lookup"><span data-stu-id="d46bd-332">Current</span></span> | <span data-ttu-id="d46bd-333">Clearingový účet</span><span class="sxs-lookup"><span data-stu-id="d46bd-333">Clearing account</span></span>    |          | <span data-ttu-id="d46bd-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-334">1,000.00</span></span> |

<span data-ttu-id="d46bd-335">Úředník pro závazky používá standardní funkce Dynamics 365 k vytvoření fakturu pro zaplacení leasingu mimo leasing majetku.</span><span class="sxs-lookup"><span data-stu-id="d46bd-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="d46bd-336">Nicméně místo výběru **Výdaje na leasing** jako debetního účtu vybere clearingový účet pro vygenerování následující položky.</span><span class="sxs-lookup"><span data-stu-id="d46bd-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="d46bd-337">Proces AP – 31. 1. 2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="d46bd-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="d46bd-338">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="d46bd-338">Account type</span></span> | <span data-ttu-id="d46bd-339">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="d46bd-339">Account number</span></span> | <span data-ttu-id="d46bd-340">Vrstva</span><span class="sxs-lookup"><span data-stu-id="d46bd-340">Layer</span></span>   | <span data-ttu-id="d46bd-341">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="d46bd-341">Account description</span></span> | <span data-ttu-id="d46bd-342">Debet</span><span class="sxs-lookup"><span data-stu-id="d46bd-342">Debit</span></span>    | <span data-ttu-id="d46bd-343">Kredit</span><span class="sxs-lookup"><span data-stu-id="d46bd-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="d46bd-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="d46bd-344">Ledger</span></span>       | <span data-ttu-id="d46bd-345">4</span><span class="sxs-lookup"><span data-stu-id="d46bd-345">4</span></span>              | <span data-ttu-id="d46bd-346">Aktuální</span><span class="sxs-lookup"><span data-stu-id="d46bd-346">Current</span></span> | <span data-ttu-id="d46bd-347">Clearingový účet</span><span class="sxs-lookup"><span data-stu-id="d46bd-347">Clearing account</span></span>    | <span data-ttu-id="d46bd-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-348">1,000.00</span></span> |          |
| <span data-ttu-id="d46bd-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="d46bd-349">Ledger</span></span>       | <span data-ttu-id="d46bd-350">2</span><span class="sxs-lookup"><span data-stu-id="d46bd-350">2</span></span>              | <span data-ttu-id="d46bd-351">Aktuální</span><span class="sxs-lookup"><span data-stu-id="d46bd-351">Current</span></span> | <span data-ttu-id="d46bd-352">Bankovní poplatek</span><span class="sxs-lookup"><span data-stu-id="d46bd-352">Bank fee</span></span>            | <span data-ttu-id="d46bd-353">3.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-353">3.00</span></span>     |          |
| <span data-ttu-id="d46bd-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="d46bd-354">Ledger</span></span>       | <span data-ttu-id="d46bd-355">3</span><span class="sxs-lookup"><span data-stu-id="d46bd-355">3</span></span>              | <span data-ttu-id="d46bd-356">Aktuální</span><span class="sxs-lookup"><span data-stu-id="d46bd-356">Current</span></span> | <span data-ttu-id="d46bd-357">Výdaje DPH</span><span class="sxs-lookup"><span data-stu-id="d46bd-357">VAT expense</span></span>         | <span data-ttu-id="d46bd-358">5.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-358">5.00</span></span>     |          |
| <span data-ttu-id="d46bd-359">Dodavatel</span><span class="sxs-lookup"><span data-stu-id="d46bd-359">Vendor</span></span>       | <span data-ttu-id="d46bd-360">5</span><span class="sxs-lookup"><span data-stu-id="d46bd-360">5</span></span>              | <span data-ttu-id="d46bd-361">Aktuální</span><span class="sxs-lookup"><span data-stu-id="d46bd-361">Current</span></span> | <span data-ttu-id="d46bd-362">Závazky</span><span class="sxs-lookup"><span data-stu-id="d46bd-362">Accounts payable</span></span>    |          | <span data-ttu-id="d46bd-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-363">1,008.00</span></span> |

<span data-ttu-id="d46bd-364">Když je prodejci vystaven výpis, postupujete podle pravidelného platebního procesu.</span><span class="sxs-lookup"><span data-stu-id="d46bd-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="d46bd-365">Během tohoto procesu je vygenerována následující položka deníku.</span><span class="sxs-lookup"><span data-stu-id="d46bd-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="d46bd-366">Platba v hotovosti – 31. 1. 2020 – 120</span><span class="sxs-lookup"><span data-stu-id="d46bd-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="d46bd-367">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="d46bd-367">Account type</span></span> | <span data-ttu-id="d46bd-368">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="d46bd-368">Account number</span></span> | <span data-ttu-id="d46bd-369">Vrstva</span><span class="sxs-lookup"><span data-stu-id="d46bd-369">Layer</span></span>   | <span data-ttu-id="d46bd-370">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="d46bd-370">Account description</span></span> | <span data-ttu-id="d46bd-371">Debet</span><span class="sxs-lookup"><span data-stu-id="d46bd-371">Debit</span></span>    | <span data-ttu-id="d46bd-372">Kredit</span><span class="sxs-lookup"><span data-stu-id="d46bd-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="d46bd-373">Dodavatel</span><span class="sxs-lookup"><span data-stu-id="d46bd-373">Vendor</span></span>       | <span data-ttu-id="d46bd-374">5</span><span class="sxs-lookup"><span data-stu-id="d46bd-374">5</span></span>              | <span data-ttu-id="d46bd-375">Aktuální</span><span class="sxs-lookup"><span data-stu-id="d46bd-375">Current</span></span> | <span data-ttu-id="d46bd-376">Závazky</span><span class="sxs-lookup"><span data-stu-id="d46bd-376">Accounts Payable</span></span>    | <span data-ttu-id="d46bd-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-377">1,008.00</span></span> |          |
| <span data-ttu-id="d46bd-378">Banka</span><span class="sxs-lookup"><span data-stu-id="d46bd-378">Bank</span></span>         | <span data-ttu-id="d46bd-379">9</span><span class="sxs-lookup"><span data-stu-id="d46bd-379">9</span></span>              | <span data-ttu-id="d46bd-380">Aktuální</span><span class="sxs-lookup"><span data-stu-id="d46bd-380">Current</span></span> | <span data-ttu-id="d46bd-381">Hotovost</span><span class="sxs-lookup"><span data-stu-id="d46bd-381">Cash</span></span>                |          | <span data-ttu-id="d46bd-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-382">1,008.00</span></span> |

<span data-ttu-id="d46bd-383">V tomto okamžiku jste plně zaúčtovali tento leasing podle zákonných požadavků na výkaznictví a můžete vygenerovat předvahu pomocí aktuální vrstvy.</span><span class="sxs-lookup"><span data-stu-id="d46bd-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="d46bd-384">Systém vrátí předvahu s následujícími čísly.</span><span class="sxs-lookup"><span data-stu-id="d46bd-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="d46bd-385">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="d46bd-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="d46bd-386">popis</span><span class="sxs-lookup"><span data-stu-id="d46bd-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="d46bd-387">Statutární kniha (aktuální vrstva)</span><span class="sxs-lookup"><span data-stu-id="d46bd-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="d46bd-388">Celková aktuální vrstva</span><span class="sxs-lookup"><span data-stu-id="d46bd-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d46bd-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="d46bd-389">JE-100</span></span></th>
<th><span data-ttu-id="d46bd-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="d46bd-390">JE-110</span></span></th>
<th><span data-ttu-id="d46bd-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="d46bd-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d46bd-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="d46bd-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="d46bd-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="d46bd-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="d46bd-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="d46bd-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d46bd-395">1</span><span class="sxs-lookup"><span data-stu-id="d46bd-395">1</span></span></td>
<td><span data-ttu-id="d46bd-396">Výdaje leasingu</span><span class="sxs-lookup"><span data-stu-id="d46bd-396">Lease expense</span></span></td>
<td><span data-ttu-id="d46bd-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="d46bd-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d46bd-399">2</span><span class="sxs-lookup"><span data-stu-id="d46bd-399">2</span></span></td>
<td><span data-ttu-id="d46bd-400">Bankovní poplatek</span><span class="sxs-lookup"><span data-stu-id="d46bd-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="d46bd-401">3.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="d46bd-402">3.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d46bd-403">3</span><span class="sxs-lookup"><span data-stu-id="d46bd-403">3</span></span></td>
<td><span data-ttu-id="d46bd-404">Výdaje DPH</span><span class="sxs-lookup"><span data-stu-id="d46bd-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="d46bd-405">5.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="d46bd-406">5.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d46bd-407">4</span><span class="sxs-lookup"><span data-stu-id="d46bd-407">4</span></span></td>
<td><span data-ttu-id="d46bd-408">Clearingový účet</span><span class="sxs-lookup"><span data-stu-id="d46bd-408">Clearing account</span></span></td>
<td><span data-ttu-id="d46bd-409">−1 000,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-409">-1,000.00</span></span></td>
<td><span data-ttu-id="d46bd-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="d46bd-411">0,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d46bd-412">5</span><span class="sxs-lookup"><span data-stu-id="d46bd-412">5</span></span></td>
<td><span data-ttu-id="d46bd-413">Závazky</span><span class="sxs-lookup"><span data-stu-id="d46bd-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="d46bd-414">-1008,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-414">-1,008.00</span></span></td>
<td><span data-ttu-id="d46bd-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-415">1,008.00</span></span></td>
<td><span data-ttu-id="d46bd-416">0,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d46bd-417">6</span><span class="sxs-lookup"><span data-stu-id="d46bd-417">6</span></span></td>
<td><span data-ttu-id="d46bd-418">Používaný majetek</span><span class="sxs-lookup"><span data-stu-id="d46bd-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d46bd-419">0,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d46bd-420">7</span><span class="sxs-lookup"><span data-stu-id="d46bd-420">7</span></span></td>
<td><span data-ttu-id="d46bd-421">Povinnost finančního leasingu</span><span class="sxs-lookup"><span data-stu-id="d46bd-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d46bd-422">0,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d46bd-423">8</span><span class="sxs-lookup"><span data-stu-id="d46bd-423">8</span></span></td>
<td><span data-ttu-id="d46bd-424">Výdaje na úroky</span><span class="sxs-lookup"><span data-stu-id="d46bd-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d46bd-425">0,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d46bd-426">9</span><span class="sxs-lookup"><span data-stu-id="d46bd-426">9</span></span></td>
<td><span data-ttu-id="d46bd-427">Hotovost</span><span class="sxs-lookup"><span data-stu-id="d46bd-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="d46bd-428">-1008,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-428">-1,008.00</span></span></td>
<td><span data-ttu-id="d46bd-429">-1008,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d46bd-430">10</span><span class="sxs-lookup"><span data-stu-id="d46bd-430">10</span></span></td>
<td><span data-ttu-id="d46bd-431">Odpisové výdaje</span><span class="sxs-lookup"><span data-stu-id="d46bd-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d46bd-432">0,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d46bd-433">11</span><span class="sxs-lookup"><span data-stu-id="d46bd-433">11</span></span></td>
<td><span data-ttu-id="d46bd-434">Akumulovaný odpis</span><span class="sxs-lookup"><span data-stu-id="d46bd-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="d46bd-435">0,00</span><span class="sxs-lookup"><span data-stu-id="d46bd-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d46bd-436">Pokud chcete použít čísla IFRS 16 ke spuštění stejné předvahy, musí být položky deníku statutárního účtování stornovány a položky deníku IFRS 16 musí být zaúčtovány.</span><span class="sxs-lookup"><span data-stu-id="d46bd-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="d46bd-437">Chcete-li stornovat položky statutárního deníku, tento příklad obsahuje statutární stornovací knihu, která má stejné nastavení jako statutární kniha, ale má opačný profil účtování.</span><span class="sxs-lookup"><span data-stu-id="d46bd-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="d46bd-438">Například statutární kniha *debetovala* účet výdaje na leasing, ale stornovací kniha bude tento účet *kreditovat*.</span><span class="sxs-lookup"><span data-stu-id="d46bd-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="d46bd-439">Tyto vztahy lze snadno definovat v účtech pro zaúčtování leasingu majetku na stránce **Parametry leasingu majetku** (**Leasing majetku \> Nastavení \> Parametry leasingu majetku**).</span><span class="sxs-lookup"><span data-stu-id="d46bd-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="d46bd-440">Když se pro stornovací knihu použije stejný proces, který byl použit pro statutární knihu, vytvoří se následující položka deníku.</span><span class="sxs-lookup"><span data-stu-id="d46bd-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="d46bd-441">Rozdíl je v tom, že stornovací kniha rezervuje stornované položky ze statutární knihy.</span><span class="sxs-lookup"><span data-stu-id="d46bd-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="d46bd-442">Stornování položek se provede také ve vlastní vrstvě.</span><span class="sxs-lookup"><span data-stu-id="d46bd-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="d46bd-443">Když je na aktuální vrstvě spuštěna předvaha, stornované položky deníku nejsou zahrnuty.</span><span class="sxs-lookup"><span data-stu-id="d46bd-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="d46bd-444">Leasingová splátka – 31. 1. 2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="d46bd-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="d46bd-445">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="d46bd-445">Account type</span></span> | <span data-ttu-id="d46bd-446">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="d46bd-446">Account number</span></span> | <span data-ttu-id="d46bd-447">Vrstva</span><span class="sxs-lookup"><span data-stu-id="d46bd-447">Layer</span></span>  | <span data-ttu-id="d46bd-448">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="d46bd-448">Account description</span></span> | <span data-ttu-id="d46bd-449">Debet</span><span class="sxs-lookup"><span data-stu-id="d46bd-449">Debit</span></span>    | <span data-ttu-id="d46bd-450">Kredit</span><span class="sxs-lookup"><span data-stu-id="d46bd-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="d46bd-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="d46bd-451">Ledger</span></span>       | <span data-ttu-id="d46bd-452">4</span><span class="sxs-lookup"><span data-stu-id="d46bd-452">4</span></span>              | <span data-ttu-id="d46bd-453">Vlastní</span><span class="sxs-lookup"><span data-stu-id="d46bd-453">Custom</span></span> | <span data-ttu-id="d46bd-454">Clearingový účet</span><span class="sxs-lookup"><span data-stu-id="d46bd-454">Clearing account</span></span>    | <span data-ttu-id="d46bd-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-455">1,000.00</span></span> |          |
| <span data-ttu-id="d46bd-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="d46bd-456">Ledger</span></span>       | <span data-ttu-id="d46bd-457">1</span><span class="sxs-lookup"><span data-stu-id="d46bd-457">1</span></span>              | <span data-ttu-id="d46bd-458">Vlastní</span><span class="sxs-lookup"><span data-stu-id="d46bd-458">Custom</span></span> | <span data-ttu-id="d46bd-459">Výdaje leasingu</span><span class="sxs-lookup"><span data-stu-id="d46bd-459">Lease expense</span></span>       |          | <span data-ttu-id="d46bd-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-460">1,000.00</span></span> |

<span data-ttu-id="d46bd-461">Nyní, když jste vyloučili položky statutárního deníku, zarezervujete všechny položky deníku, které vyžadují IFRS 16 v knize IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="d46bd-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="d46bd-462">Mezi tyto položky patří počáteční uznání používaného majetku a záznam úroků a odpisů.</span><span class="sxs-lookup"><span data-stu-id="d46bd-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="d46bd-463">Počáteční uznání – 1. 1. 2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="d46bd-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="d46bd-464">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="d46bd-464">Account type</span></span> | <span data-ttu-id="d46bd-465">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="d46bd-465">Account number</span></span> | <span data-ttu-id="d46bd-466">Vrstva</span><span class="sxs-lookup"><span data-stu-id="d46bd-466">Layer</span></span>  | <span data-ttu-id="d46bd-467">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="d46bd-467">Account description</span></span>      | <span data-ttu-id="d46bd-468">Debet</span><span class="sxs-lookup"><span data-stu-id="d46bd-468">Debit</span></span>     | <span data-ttu-id="d46bd-469">Kredit</span><span class="sxs-lookup"><span data-stu-id="d46bd-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="d46bd-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="d46bd-470">Ledger</span></span>       | <span data-ttu-id="d46bd-471">6</span><span class="sxs-lookup"><span data-stu-id="d46bd-471">6</span></span>              | <span data-ttu-id="d46bd-472">Vlastní</span><span class="sxs-lookup"><span data-stu-id="d46bd-472">Custom</span></span> | <span data-ttu-id="d46bd-473">Používaný majetek</span><span class="sxs-lookup"><span data-stu-id="d46bd-473">ROU Asset</span></span>                | <span data-ttu-id="d46bd-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="d46bd-474">22,793.90</span></span> |           |
| <span data-ttu-id="d46bd-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="d46bd-475">Ledger</span></span>       | <span data-ttu-id="d46bd-476">7</span><span class="sxs-lookup"><span data-stu-id="d46bd-476">7</span></span>              | <span data-ttu-id="d46bd-477">Vlastní</span><span class="sxs-lookup"><span data-stu-id="d46bd-477">Custom</span></span> | <span data-ttu-id="d46bd-478">Povinnost finančního leasingu</span><span class="sxs-lookup"><span data-stu-id="d46bd-478">Finance lease obligation</span></span> |           | <span data-ttu-id="d46bd-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="d46bd-479">22,793.90</span></span> |

<span data-ttu-id="d46bd-480">Leasingová splátka je zaúčtována jako ostatní leasingové splátky.</span><span class="sxs-lookup"><span data-stu-id="d46bd-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="d46bd-481">Důvodem pro použití clearingového účtu je zajistit, aby byla hotovost připsána pouze jednou.</span><span class="sxs-lookup"><span data-stu-id="d46bd-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="d46bd-482">Leasingová splátka – 31. 1. 2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="d46bd-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="d46bd-483">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="d46bd-483">Account type</span></span> | <span data-ttu-id="d46bd-484">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="d46bd-484">Account number</span></span> | <span data-ttu-id="d46bd-485">Vrstva</span><span class="sxs-lookup"><span data-stu-id="d46bd-485">Layer</span></span>  | <span data-ttu-id="d46bd-486">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="d46bd-486">Account description</span></span>      | <span data-ttu-id="d46bd-487">Debet</span><span class="sxs-lookup"><span data-stu-id="d46bd-487">Debit</span></span>    | <span data-ttu-id="d46bd-488">Kredit</span><span class="sxs-lookup"><span data-stu-id="d46bd-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="d46bd-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="d46bd-489">Ledger</span></span>       | <span data-ttu-id="d46bd-490">7</span><span class="sxs-lookup"><span data-stu-id="d46bd-490">7</span></span>              | <span data-ttu-id="d46bd-491">Vlastní</span><span class="sxs-lookup"><span data-stu-id="d46bd-491">Custom</span></span> | <span data-ttu-id="d46bd-492">Povinnost finančního leasingu</span><span class="sxs-lookup"><span data-stu-id="d46bd-492">Finance lease obligation</span></span> | <span data-ttu-id="d46bd-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-493">1,000.00</span></span> |          |
| <span data-ttu-id="d46bd-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="d46bd-494">Ledger</span></span>       | <span data-ttu-id="d46bd-495">4</span><span class="sxs-lookup"><span data-stu-id="d46bd-495">4</span></span>              | <span data-ttu-id="d46bd-496">Vlastní</span><span class="sxs-lookup"><span data-stu-id="d46bd-496">Custom</span></span> | <span data-ttu-id="d46bd-497">Clearingový účet</span><span class="sxs-lookup"><span data-stu-id="d46bd-497">Clearing account</span></span>         |          | <span data-ttu-id="d46bd-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-498">1,000.00</span></span> |

<span data-ttu-id="d46bd-499">Položka deníku úrokových nákladů je generována z plánu amortizace závazků.</span><span class="sxs-lookup"><span data-stu-id="d46bd-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="d46bd-500">Úrokové náklady – 31. 1. 2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="d46bd-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="d46bd-501">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="d46bd-501">Account type</span></span> | <span data-ttu-id="d46bd-502">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="d46bd-502">Account number</span></span> | <span data-ttu-id="d46bd-503">Vrstva</span><span class="sxs-lookup"><span data-stu-id="d46bd-503">Layer</span></span>  | <span data-ttu-id="d46bd-504">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="d46bd-504">Account description</span></span>      | <span data-ttu-id="d46bd-505">Debet</span><span class="sxs-lookup"><span data-stu-id="d46bd-505">Debit</span></span> | <span data-ttu-id="d46bd-506">Kredit</span><span class="sxs-lookup"><span data-stu-id="d46bd-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="d46bd-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="d46bd-507">Ledger</span></span>       | <span data-ttu-id="d46bd-508">8</span><span class="sxs-lookup"><span data-stu-id="d46bd-508">8</span></span>              | <span data-ttu-id="d46bd-509">Vlastní</span><span class="sxs-lookup"><span data-stu-id="d46bd-509">Custom</span></span> | <span data-ttu-id="d46bd-510">Výdaje na úroky</span><span class="sxs-lookup"><span data-stu-id="d46bd-510">Interest expense</span></span>         | <span data-ttu-id="d46bd-511">94.97</span><span class="sxs-lookup"><span data-stu-id="d46bd-511">94.97</span></span> |        |
| <span data-ttu-id="d46bd-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="d46bd-512">Ledger</span></span>       | <span data-ttu-id="d46bd-513">7</span><span class="sxs-lookup"><span data-stu-id="d46bd-513">7</span></span>              | <span data-ttu-id="d46bd-514">Vlastní</span><span class="sxs-lookup"><span data-stu-id="d46bd-514">Custom</span></span> | <span data-ttu-id="d46bd-515">Povinnost finančního leasingu</span><span class="sxs-lookup"><span data-stu-id="d46bd-515">Finance lease obligation</span></span> |       | <span data-ttu-id="d46bd-516">94.97</span><span class="sxs-lookup"><span data-stu-id="d46bd-516">94.97</span></span>  |

<span data-ttu-id="d46bd-517">Položka deníku odpisových výdajů je generována z plánu odpisu majetku.</span><span class="sxs-lookup"><span data-stu-id="d46bd-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="d46bd-518">Odpisové výdaje – 31. 1. 2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="d46bd-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="d46bd-519">Typ účtu</span><span class="sxs-lookup"><span data-stu-id="d46bd-519">Account type</span></span> | <span data-ttu-id="d46bd-520">Číslo účtu</span><span class="sxs-lookup"><span data-stu-id="d46bd-520">Account number</span></span> | <span data-ttu-id="d46bd-521">Vrstva</span><span class="sxs-lookup"><span data-stu-id="d46bd-521">Layer</span></span>  | <span data-ttu-id="d46bd-522">Popis účtu</span><span class="sxs-lookup"><span data-stu-id="d46bd-522">Account description</span></span>      | <span data-ttu-id="d46bd-523">Debet</span><span class="sxs-lookup"><span data-stu-id="d46bd-523">Debit</span></span>  | <span data-ttu-id="d46bd-524">Kredit</span><span class="sxs-lookup"><span data-stu-id="d46bd-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="d46bd-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="d46bd-525">Ledger</span></span>       | <span data-ttu-id="d46bd-526">10</span><span class="sxs-lookup"><span data-stu-id="d46bd-526">10</span></span>             | <span data-ttu-id="d46bd-527">Vlastní</span><span class="sxs-lookup"><span data-stu-id="d46bd-527">Custom</span></span> | <span data-ttu-id="d46bd-528">Odpisové výdaje</span><span class="sxs-lookup"><span data-stu-id="d46bd-528">Depreciation expense</span></span>     | <span data-ttu-id="d46bd-529">949.75</span><span class="sxs-lookup"><span data-stu-id="d46bd-529">949.75</span></span> |        |
| <span data-ttu-id="d46bd-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="d46bd-530">Ledger</span></span>       | <span data-ttu-id="d46bd-531">11</span><span class="sxs-lookup"><span data-stu-id="d46bd-531">11</span></span>             | <span data-ttu-id="d46bd-532">Vlastní</span><span class="sxs-lookup"><span data-stu-id="d46bd-532">Custom</span></span> | <span data-ttu-id="d46bd-533">Akumulovaný odpis</span><span class="sxs-lookup"><span data-stu-id="d46bd-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="d46bd-534">949.75</span><span class="sxs-lookup"><span data-stu-id="d46bd-534">949.75</span></span> |

<span data-ttu-id="d46bd-535">Po vytvoření a zaúčtování všech těchto položek deníku se zobrazí následující hodnoty „vlastní vrstvy 1“.</span><span class="sxs-lookup"><span data-stu-id="d46bd-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="d46bd-536">Všimněte si, že poslední sloupec obsahuje bankovní poplatek, výdaj na daň z přidané hodnoty (DPH) a snížení hotovosti z předchozí vrstvy, ale nezahrnuje položky deníku pro statutární vykazování.</span><span class="sxs-lookup"><span data-stu-id="d46bd-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="d46bd-537">Proto dosáhnete skutečného využití možností duálního hlášení.</span><span class="sxs-lookup"><span data-stu-id="d46bd-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="d46bd-538">V tomto okamžiku musí společnost spustit předvahu a zkombinovat aktuální a vlastní vrstvu, aby vytvořila předvahu podle IFRS.</span><span class="sxs-lookup"><span data-stu-id="d46bd-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="d46bd-539">Č. účtu</span><span class="sxs-lookup"><span data-stu-id="d46bd-539">Account No</span></span> | <span data-ttu-id="d46bd-540">popis</span><span class="sxs-lookup"><span data-stu-id="d46bd-540">Description</span></span>              | <span data-ttu-id="d46bd-541">Statutární kniha\-Aktuální vrstva\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="d46bd-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="d46bd-542">Statutární kniha\-Aktuální vrstva\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="d46bd-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="d46bd-543">Statutární kniha\-Aktuální vrstva\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="d46bd-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="d46bd-544">Aktuální vrstva \- Celkem</span><span class="sxs-lookup"><span data-stu-id="d46bd-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="d46bd-545">Stornovací kniha\-Vlastní vrstva\-JE\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="d46bd-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="d46bd-546">Kniha IFRS 16\-Vlastní vrstva\-JE\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="d46bd-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="d46bd-547">Kniha IFRS 16\-Vlastní vrstva\-JE\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="d46bd-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="d46bd-548">Kniha IFRS 16\-Vlastní vrstva\-JE\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="d46bd-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="d46bd-549">Kniha IFRS 16\-Vlastní vrstva\-JE\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="d46bd-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="d46bd-550">Vlastní vrstva \+ Vlastní vrstva \- Celkem</span><span class="sxs-lookup"><span data-stu-id="d46bd-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="d46bd-551">1</span><span class="sxs-lookup"><span data-stu-id="d46bd-551">1</span></span>          | <span data-ttu-id="d46bd-552">Výdaje leasingu</span><span class="sxs-lookup"><span data-stu-id="d46bd-552">Lease expense</span></span>            | <span data-ttu-id="d46bd-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="d46bd-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-554">1,000\.00</span></span>               |   | <span data-ttu-id="d46bd-555">\-1000</span><span class="sxs-lookup"><span data-stu-id="d46bd-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="d46bd-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-556">0\.00</span></span>                                   |
| <span data-ttu-id="d46bd-557">2</span><span class="sxs-lookup"><span data-stu-id="d46bd-557">2</span></span>          | <span data-ttu-id="d46bd-558">Bankovní poplatek</span><span class="sxs-lookup"><span data-stu-id="d46bd-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="d46bd-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="d46bd-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="d46bd-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-561">3\.00</span></span>                                   |
| <span data-ttu-id="d46bd-562">3</span><span class="sxs-lookup"><span data-stu-id="d46bd-562">3</span></span>          | <span data-ttu-id="d46bd-563">Výdaje DPH</span><span class="sxs-lookup"><span data-stu-id="d46bd-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="d46bd-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="d46bd-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="d46bd-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-566">5\.00</span></span>                                   |
| <span data-ttu-id="d46bd-567">4</span><span class="sxs-lookup"><span data-stu-id="d46bd-567">4</span></span>          | <span data-ttu-id="d46bd-568">Clearingový účet</span><span class="sxs-lookup"><span data-stu-id="d46bd-568">Clearing account</span></span>         | <span data-ttu-id="d46bd-569">\-1000\.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="d46bd-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="d46bd-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-571">0\.00</span></span>                   |   | <span data-ttu-id="d46bd-572">1 000</span><span class="sxs-lookup"><span data-stu-id="d46bd-572">1,000</span></span>                                           |                                                | <span data-ttu-id="d46bd-573">\-1000</span><span class="sxs-lookup"><span data-stu-id="d46bd-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="d46bd-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-574">0\.00</span></span>                                   |
| <span data-ttu-id="d46bd-575">5</span><span class="sxs-lookup"><span data-stu-id="d46bd-575">5</span></span>          | <span data-ttu-id="d46bd-576">Závazky</span><span class="sxs-lookup"><span data-stu-id="d46bd-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="d46bd-577">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="d46bd-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-578">1,008\.00</span></span>                                         | <span data-ttu-id="d46bd-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="d46bd-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-580">0\.00</span></span>                                   |
| <span data-ttu-id="d46bd-581">6</span><span class="sxs-lookup"><span data-stu-id="d46bd-581">6</span></span>          | <span data-ttu-id="d46bd-582">Používaný majetek</span><span class="sxs-lookup"><span data-stu-id="d46bd-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="d46bd-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="d46bd-584">22,794</span><span class="sxs-lookup"><span data-stu-id="d46bd-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="d46bd-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="d46bd-585">22,793\.90</span></span>                              |
| <span data-ttu-id="d46bd-586">7</span><span class="sxs-lookup"><span data-stu-id="d46bd-586">7</span></span>          | <span data-ttu-id="d46bd-587">Povinnost finančního leasingu</span><span class="sxs-lookup"><span data-stu-id="d46bd-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="d46bd-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="d46bd-589">\-22 794</span><span class="sxs-lookup"><span data-stu-id="d46bd-589">\-22,794</span></span>                                       | <span data-ttu-id="d46bd-590">1 000</span><span class="sxs-lookup"><span data-stu-id="d46bd-590">1,000</span></span>                                          | <span data-ttu-id="d46bd-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="d46bd-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="d46bd-592">\-21 888\.87</span><span class="sxs-lookup"><span data-stu-id="d46bd-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="d46bd-593">8</span><span class="sxs-lookup"><span data-stu-id="d46bd-593">8</span></span>          | <span data-ttu-id="d46bd-594">Výdaje na úroky</span><span class="sxs-lookup"><span data-stu-id="d46bd-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="d46bd-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="d46bd-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="d46bd-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="d46bd-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="d46bd-597">94\.97</span></span>                                  |
| <span data-ttu-id="d46bd-598">9</span><span class="sxs-lookup"><span data-stu-id="d46bd-598">9</span></span>          | <span data-ttu-id="d46bd-599">Hotovost</span><span class="sxs-lookup"><span data-stu-id="d46bd-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="d46bd-600">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="d46bd-601">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="d46bd-602">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="d46bd-603">10</span><span class="sxs-lookup"><span data-stu-id="d46bd-603">10</span></span>         | <span data-ttu-id="d46bd-604">Odpisové výdaje</span><span class="sxs-lookup"><span data-stu-id="d46bd-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="d46bd-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="d46bd-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="d46bd-606">949\.75</span></span>                                        | <span data-ttu-id="d46bd-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="d46bd-607">949\.75</span></span>                                 |
| <span data-ttu-id="d46bd-608">11</span><span class="sxs-lookup"><span data-stu-id="d46bd-608">11</span></span>         | <span data-ttu-id="d46bd-609">Akumulovaný odpis</span><span class="sxs-lookup"><span data-stu-id="d46bd-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="d46bd-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="d46bd-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="d46bd-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="d46bd-611">\-949\.75</span></span>                                      | <span data-ttu-id="d46bd-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="d46bd-612">\-949\.75</span></span>                               |


