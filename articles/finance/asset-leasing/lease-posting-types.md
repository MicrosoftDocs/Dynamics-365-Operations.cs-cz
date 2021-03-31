---
title: Typy zaúčtování leasingu
description: Toto téma popisuje typy účtování, které se používají pro transakce leasingu aktiv.
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
ms.openlocfilehash: 9b7d8c545c1addaa570d54855bbad6c576783007
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229495"
---
# <a name="lease-posting-types"></a><span data-ttu-id="a3d32-103">Typy zaúčtování leasingu</span><span class="sxs-lookup"><span data-stu-id="a3d32-103">Lease posting types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3d32-104">Toto téma popisuje typy účtování, které se používají pro transakce leasingu aktiv.</span><span class="sxs-lookup"><span data-stu-id="a3d32-104">This topic describes the posting types that are used for asset leasing transactions.</span></span>

## <a name="lease-asset"></a><span data-ttu-id="a3d32-105">Aktivum leasingu</span><span class="sxs-lookup"><span data-stu-id="a3d32-105">Lease asset</span></span>

<span data-ttu-id="a3d32-106">Účet je přidružen k používanému majetku (ROU).</span><span class="sxs-lookup"><span data-stu-id="a3d32-106">The account is associated with the right-of-use (ROU) asset.</span></span> <span data-ttu-id="a3d32-107">Z tohoto účtu je odečtena částka, když je leasing původně uznán podle nových účetních standardů leasingu, tématu Kodifikace účetních standardů 842 (ASC 842) a Mezinárodního standardu účetního výkaznictví 16 (IFRS 16).</span><span class="sxs-lookup"><span data-stu-id="a3d32-107">This account is debited when a lease is initially recognized under the new lease accounting standards, Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16).</span></span> <span data-ttu-id="a3d32-108">U upraveného leasingu může být z tohoto účtu odečtena nebo připsána částka v závislosti na tom, zda úprava zvyšuje nebo snižuje závazek z leasingu.</span><span class="sxs-lookup"><span data-stu-id="a3d32-108">For a modified lease, this account might be either debited or credited, depending on whether the modification increases or decreases the lease liability.</span></span>

<span data-ttu-id="a3d32-109">**Příklad záznamů v deníku:** Počáteční uznání</span><span class="sxs-lookup"><span data-stu-id="a3d32-109">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="a3d32-110">**Debet:** leasign majetku XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-110">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="a3d32-111">**Kredit:** leasingový závazek XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-111">**Credit:** Lease liability XXX</span></span>

## <a name="lease-liability"></a><span data-ttu-id="a3d32-112">Leasingový závazek</span><span class="sxs-lookup"><span data-stu-id="a3d32-112">Lease liability</span></span>

<span data-ttu-id="a3d32-113">Účet je spojen s leasingovým závazkem, ke kterému dochází, když jsou platby diskontovány podle nových standardů IFRS 16 a ASC 842.</span><span class="sxs-lookup"><span data-stu-id="a3d32-113">The account is associated with the lease liability that occurs when payments are discounted under the new IFRS 16 and ASC 842 standards.</span></span> <span data-ttu-id="a3d32-114">Tento účet je kreditován, když je leasing od počátku uznán podle nových standardů.</span><span class="sxs-lookup"><span data-stu-id="a3d32-114">This account is credited when a lease is initially recognized under the new standards.</span></span> <span data-ttu-id="a3d32-115">Je debetován leasingovými splátkami a kreditován úroky.</span><span class="sxs-lookup"><span data-stu-id="a3d32-115">It's debited for lease payments and credited for interest accruals.</span></span>

<span data-ttu-id="a3d32-116">**Příklad záznamů v deníku:** Počáteční uznání</span><span class="sxs-lookup"><span data-stu-id="a3d32-116">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="a3d32-117">**Debet:** leasign majetku XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-117">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="a3d32-118">**Kredit:** leasingový závazek XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-118">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="a3d32-119">**Příklad záznamů v deníku:** Časové rozlišení úroků</span><span class="sxs-lookup"><span data-stu-id="a3d32-119">**Example journal entries:** Interest accrual</span></span><br>
<span data-ttu-id="a3d32-120">**Debet:** úrokové náklady XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-120">**Debit:** Interest expense XXX</span></span><br>
<span data-ttu-id="a3d32-121">**Kredit:** leasingový závazek XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-121">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="a3d32-122">**Příklad záznamů v deníku:** Leasingová splátka</span><span class="sxs-lookup"><span data-stu-id="a3d32-122">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="a3d32-123">**Debet:** leasingový závazek XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-123">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="a3d32-124">**Kredit:** závazek dodavatele / leasingová splátka XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-124">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="short-term-lease-liability"></a><span data-ttu-id="a3d32-125">Krátkodobý leasingový závazek</span><span class="sxs-lookup"><span data-stu-id="a3d32-125">Short-term lease liability</span></span>

<span data-ttu-id="a3d32-126">Účet je spojen s krátkodobým závazkem z leasingu, když je zaúčtován zápis do deníku reklasifikace závazků z krátkodobého pronájmu.</span><span class="sxs-lookup"><span data-stu-id="a3d32-126">The account is associated with the short-term lease liability when the short-term lease liability reclass journal entry is posted.</span></span> <span data-ttu-id="a3d32-127">Na tento účet se připisuje krátkodobý závazek z amortizačního plánu poslední den v měsíci.</span><span class="sxs-lookup"><span data-stu-id="a3d32-127">This account is credited for the short-term liability from the amortization schedule on the last day of the month.</span></span> <span data-ttu-id="a3d32-128">Stejná částka je však odečtena první den následujícího měsíce.</span><span class="sxs-lookup"><span data-stu-id="a3d32-128">However, the same amount is debited on the first day of the next month.</span></span>

<span data-ttu-id="a3d32-129">**Příklad záznamů v deníku:** reklasifikace krátkodobých leasingových závazků</span><span class="sxs-lookup"><span data-stu-id="a3d32-129">**Example journal entries:** Short-term lease liability reclass</span></span><br>
<span data-ttu-id="a3d32-130">**Debet:** leasingový závazek XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-130">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="a3d32-131">**Kredit:** krátkodobý leasingový závazek XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-131">**Credit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="a3d32-132">**Debit:** krátkodobý leasingový závazek XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-132">**Debit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="a3d32-133">**Kredit:** leasingový závazek XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-133">**Credit:** Lease liability XXX</span></span>

## <a name="depreciation-expense"></a><span data-ttu-id="a3d32-134">Odpisové výdaje</span><span class="sxs-lookup"><span data-stu-id="a3d32-134">Depreciation expense</span></span>

<span data-ttu-id="a3d32-135">Účet je spojen s výdajem, který souvisí s odpisy aktiva ROU podle IFRS 16, ASC 842 a finančního leasingu podle IAS 17 a ASC 840.</span><span class="sxs-lookup"><span data-stu-id="a3d32-135">The account is associated with the expense that is related to the depreciation of the ROU asset under IFRS 16, ASC 842, and finance leases under IAS 17 and ASC 840.</span></span> <span data-ttu-id="a3d32-136">Tento účet je debetován, když je každý měsíc odepisován používaný majetek.</span><span class="sxs-lookup"><span data-stu-id="a3d32-136">This account is debited when an ROU asset is depreciated each month.</span></span>

<span data-ttu-id="a3d32-137">**Příklad záznamů v deníku:** Časové rozlišení odpisů</span><span class="sxs-lookup"><span data-stu-id="a3d32-137">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="a3d32-138">**Debet:** výdej za odpis XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-138">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="a3d32-139">**Kredit:** Akumulovaný odpis XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-139">**Credit:** Accumulated Depreciation XXX</span></span>

## <a name="gainloss-on-lease-modification"></a><span data-ttu-id="a3d32-140">Zisk/ztráta při upravení leasingu</span><span class="sxs-lookup"><span data-stu-id="a3d32-140">Gain/loss on lease modification</span></span>

<span data-ttu-id="a3d32-141">Účet je spojen s jakýmikoli zisky nebo ztrátami, které vzniknou úpravami leasingu.</span><span class="sxs-lookup"><span data-stu-id="a3d32-141">The account is associated with any gains or losses that arise from lease modifications.</span></span> <span data-ttu-id="a3d32-142">Zisk může vzniknout během úpravy leasingu, pokud tato úprava sníží závazek z leasingu o částku, která přesahuje účetní hodnotu aktiva ROU.</span><span class="sxs-lookup"><span data-stu-id="a3d32-142">A gain might arise during a lease modification if the modification decreases the lease liability by an amount that exceeds the carrying value of the ROU asset.</span></span>

<span data-ttu-id="a3d32-143">Například leasing má aktuální účetní hodnotu závazku z leasingu ve výši $150 000 a účetní hodnotu aktiva ROU ve výši $100 000.</span><span class="sxs-lookup"><span data-stu-id="a3d32-143">For example, a lease has a current carrying value of the lease liability of $150,000 and a carrying value of the ROU asset of $100,000.</span></span> <span data-ttu-id="a3d32-144">Leasing je upraven a tato úprava vytváří novou současnou hodnotu budoucích minimálních leasingových plateb (PVFMLP) ve výši $ 40 000.</span><span class="sxs-lookup"><span data-stu-id="a3d32-144">The lease is modified, and this modification produces a new present value of the future minimum lease payments (PVFMLP) of $40,000.</span></span> <span data-ttu-id="a3d32-145">Proto bude odpovědnost za leasing stržena společností $110 000 (150 000 $ - $40 000).</span><span class="sxs-lookup"><span data-stu-id="a3d32-145">Therefore, the lease liability will be debited by $110,000 ($150,000 – $40,000).</span></span> <span data-ttu-id="a3d32-146">Protože používaný majetek je pouze $100 000, snížení $110 000 sníží aktivum za 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="a3d32-146">Because the ROU asset is only $100,000, the decrease of $110,000 will decrease the asset past 0 (zero).</span></span> <span data-ttu-id="a3d32-147">Účetní pokyny proto stanoví, že zbytek by měl být zaúčtován na účet zisků.</span><span class="sxs-lookup"><span data-stu-id="a3d32-147">Therefore, the accounting guidance states that the remainder should be booked to a gain account.</span></span> <span data-ttu-id="a3d32-148">V tomto případě bude konečným zápisem do deníku debit z leasingové odpovědnosti za $110 000, kredit z leasingového aktiva za $100 000 a kredit na účtu zisku $10 000.</span><span class="sxs-lookup"><span data-stu-id="a3d32-148">In this case, the final journal entry will be a debit to the lease liability for $110,000, a credit to the lease asset for $100,000, and a credit to the gain account for $10,000.</span></span>

<span data-ttu-id="a3d32-149">**Příklad záznamů v deníku:** Leasingová úprava</span><span class="sxs-lookup"><span data-stu-id="a3d32-149">**Example journal entries:** Lease modification</span></span><br>
<span data-ttu-id="a3d32-150">**Debet:** leasingový závazek XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-150">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="a3d32-151">**Kredit** leasing majetku XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-151">**Credit:** Lease Asset XXX</span></span><br>
<span data-ttu-id="a3d32-152">**Kredit:** Zisk XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-152">**Credit:** Gain XXX</span></span>

## <a name="accumulated-depreciation"></a><span data-ttu-id="a3d32-153">Akumulovaný odpis</span><span class="sxs-lookup"><span data-stu-id="a3d32-153">Accumulated depreciation</span></span>

<span data-ttu-id="a3d32-154">Účet je přidružen k protiúčtu majetku používaného majetku.</span><span class="sxs-lookup"><span data-stu-id="a3d32-154">The account is associated with the contra-asset account of the ROU asset.</span></span> <span data-ttu-id="a3d32-155">Účet je kreditován při zaúčtování výdaje odpisu.</span><span class="sxs-lookup"><span data-stu-id="a3d32-155">This account is credited when a depreciation expense is posted.</span></span>

<span data-ttu-id="a3d32-156">**Příklad záznamů v deníku:** Časové rozlišení odpisů</span><span class="sxs-lookup"><span data-stu-id="a3d32-156">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="a3d32-157">**Debet:** výdej za odpis XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-157">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="a3d32-158">**Kredit:** Akumulovaný odpis XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-158">**Credit:** Accumulated depreciation XXX</span></span>

## <a name="retained-earnings"></a><span data-ttu-id="a3d32-159">Pozdržené příjmy</span><span class="sxs-lookup"><span data-stu-id="a3d32-159">Retained earnings</span></span>

<span data-ttu-id="a3d32-160">Účet přidružený k pozdrženým příjmům.</span><span class="sxs-lookup"><span data-stu-id="a3d32-160">The account is associated with retained earnings.</span></span> <span data-ttu-id="a3d32-161">Tento účet může být debitován nebo kreditován v položce deníku vyrovnání přechodu pomocí úplné retrospektivní metody nebo metody A kumulativní možnosti oprav.</span><span class="sxs-lookup"><span data-stu-id="a3d32-161">This account might be either debited or credited in a transition adjustment journal entry by using the full retrospective method or the cumulative catch-up option A method.</span></span> <span data-ttu-id="a3d32-162">Rozdíl mezi počátečním používaného majetku a leasingovým závazkem se zaúčtuje do pozdržených příjmů.</span><span class="sxs-lookup"><span data-stu-id="a3d32-162">The difference between the initial ROU asset and lease liability is booked to retained earnings.</span></span> <span data-ttu-id="a3d32-163">Ve vzácných případech může dojít k ovlivnění pozdržených příjmů během úpravy leasingu, pokud se klasifikace leasingu změní z finanční na operativní tak, aby se hodnota používaného majetku zvyšovala nebo snižovala tak, aby se rovnala leasingovému závazku.</span><span class="sxs-lookup"><span data-stu-id="a3d32-163">In rare cases, the retained earnings might also be affected during lease modification, if the classification of a lease is changed from finance to operating to write the ROU asset up or down so that it equals the lease liability.</span></span>

<span data-ttu-id="a3d32-164">**Příklad záznamů v deníku:** Přechodové vyrovnání (metoda s možností A plně retrospektivní nebo kumulativní opravy)</span><span class="sxs-lookup"><span data-stu-id="a3d32-164">**Example journal entries:** Transition adjustment (full retrospective or cumulative catch-up option A method)</span></span><br>
<span data-ttu-id="a3d32-165">**Debet:** leasingový závazek XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-165">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="a3d32-166">**Kredit** leasing majetku XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-166">**Credit:** Lease asset XXX</span></span><br>
<span data-ttu-id="a3d32-167">**Kredit:** pozdržené příjmy XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-167">**Credit:** Retained earnings XXX</span></span>

## <a name="variable-payment"></a><span data-ttu-id="a3d32-168">Variabilní splátka</span><span class="sxs-lookup"><span data-stu-id="a3d32-168">Variable payment</span></span>

<span data-ttu-id="a3d32-169">Účet je spojen s variabilními leasingovými splátkami, které vznikají přeceněním indexu podle leasingů dle ASC 842, ASC 840 a IAS 17.</span><span class="sxs-lookup"><span data-stu-id="a3d32-169">The account is associated with variable lease payments that are produced by an index revaluation under ASC 842, ASC 840, and IAS 17 leases.</span></span> <span data-ttu-id="a3d32-170">V harmonogramu splátek leasingu jsou variabilní splátky zahrnuty ve sloupci **Variabilní splátka**.</span><span class="sxs-lookup"><span data-stu-id="a3d32-170">In the lease payment schedule, variable payments are included in the **Variable payment** column.</span></span> <span data-ttu-id="a3d32-171">Z tohoto účtu je odečtena částka, když je faktura vytvořena na řádku plánu splátek, který obsahuje variabilní splátku.</span><span class="sxs-lookup"><span data-stu-id="a3d32-171">This account is debited when an invoice is created against a payment schedule line that contains a variable payment.</span></span>

<span data-ttu-id="a3d32-172">**Příklad záznamů v deníku:** Leasingová splátka</span><span class="sxs-lookup"><span data-stu-id="a3d32-172">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="a3d32-173">**Debet:** leasingový závazek XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-173">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="a3d32-174">**Debet:** Variabilní splátka XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-174">**Debit:** Variable payment XXX</span></span><br>
<span data-ttu-id="a3d32-175">**Kredit:** závazek dodavatele / leasingová splátka XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-175">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="deferred-rent-asset-liability"></a><span data-ttu-id="a3d32-176">Aktivum (pasivum) odložené splátky</span><span class="sxs-lookup"><span data-stu-id="a3d32-176">Deferred rent asset (liability)</span></span>

<span data-ttu-id="a3d32-177">Účet je spojen s aktivem nebo pasivem odložené splátky, který je vytvořen odložením splátky leasingu.</span><span class="sxs-lookup"><span data-stu-id="a3d32-177">The account is associated with the deferred rent asset or liability that is produced by a deferred rent treatment lease.</span></span> <span data-ttu-id="a3d32-178">Z tohoto účtu je odečtena částka, když je faktura zaúčtována proti odložené splátce leasingu, pokud je částka leasingové splátky vyšší než lineární výdaje leasingu za dané období.</span><span class="sxs-lookup"><span data-stu-id="a3d32-178">This account is debited when an invoice is posted against a deferred rent treatment lease, if the lease payment amount is more than the period's straight-line rent expense.</span></span> <span data-ttu-id="a3d32-179">Je kreditován, pokud je leasingová splátka nižší než lineární výdaje leasingu v daném období.</span><span class="sxs-lookup"><span data-stu-id="a3d32-179">It's credited if the lease payment is less than the period's straight-line rent expense.</span></span>

<span data-ttu-id="a3d32-180">**Příklad záznamů v deníku:** Leasingová splátka (leasing s odloženými splátkami)</span><span class="sxs-lookup"><span data-stu-id="a3d32-180">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="a3d32-181">**Debet:** leasingový výdaj XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-181">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="a3d32-182">**Kredit:** pasivum odložené splátky XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-182">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="a3d32-183">**Kredit:** závazek dodavatele / leasingová splátka XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-183">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="lease-expense"></a><span data-ttu-id="a3d32-184">Výdaje leasingu</span><span class="sxs-lookup"><span data-stu-id="a3d32-184">Lease expense</span></span>

<span data-ttu-id="a3d32-185">Účet je spojen s náklady na leasing, pokud je leasing klasifikován jako leasing s opožděnými splátkami.</span><span class="sxs-lookup"><span data-stu-id="a3d32-185">The account is associated with the lease expense if the lease is classified as a deferred rent treatment lease.</span></span> <span data-ttu-id="a3d32-186">Z tohoto účtu je odečtena částka, když je faktura zaúčtována na základě odložené splátky.</span><span class="sxs-lookup"><span data-stu-id="a3d32-186">This account is debited when an invoice is posted against a deferred rent treatment lease.</span></span>

<span data-ttu-id="a3d32-187">**Příklad záznamů v deníku:** Leasingová splátka (leasing s odloženými splátkami)</span><span class="sxs-lookup"><span data-stu-id="a3d32-187">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="a3d32-188">**Debet:** leasingový výdaj XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-188">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="a3d32-189">**Kredit:** pasivum odložené splátky XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-189">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="a3d32-190">**Kredit:** závazek dodavatele / leasingová splátka XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-190">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="impairment-expense"></a><span data-ttu-id="a3d32-191">Výdaje snížení hodnoty</span><span class="sxs-lookup"><span data-stu-id="a3d32-191">Impairment expense</span></span>

<span data-ttu-id="a3d32-192">Proti účtu se účtuje, když je snížena hodnota leasingu.</span><span class="sxs-lookup"><span data-stu-id="a3d32-192">The account is posted against when a lease is impaired.</span></span> <span data-ttu-id="a3d32-193">Tento účet je debetován, zatímco účet používaného majetku je přímo kreditován.</span><span class="sxs-lookup"><span data-stu-id="a3d32-193">This account is debited, whereas the ROU asset account is directly credited.</span></span>

<span data-ttu-id="a3d32-194">**Příklad záznamů v deníku:** Leasingová splátka</span><span class="sxs-lookup"><span data-stu-id="a3d32-194">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="a3d32-195">**Debet:** Výdaj snížení hodnoty XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-195">**Debit:** Impairment expense XXX</span></span><br>
<span data-ttu-id="a3d32-196">**Kredit:** používaný majetek XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-196">**Credit:** ROU asset XXX</span></span>

## <a name="lease-payment"></a><span data-ttu-id="a3d32-197">Leasingová splátka</span><span class="sxs-lookup"><span data-stu-id="a3d32-197">Lease payment</span></span>

<span data-ttu-id="a3d32-198">Proti účtu se provede účetní zápis, pokud je vypnutý parametr **Platba dodavateli**.</span><span class="sxs-lookup"><span data-stu-id="a3d32-198">The account is posted against if the **Pay to Vendor** parameter is turned off.</span></span> <span data-ttu-id="a3d32-199">Tento účet je kreditován místo závazku dodavateli, pokud je parametr vypnutý.</span><span class="sxs-lookup"><span data-stu-id="a3d32-199">This account is credited instead of the vendor payable if the parameter is turned off.</span></span>

<span data-ttu-id="a3d32-200">**Příklad záznamů v deníku:** Leasingová splátka</span><span class="sxs-lookup"><span data-stu-id="a3d32-200">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="a3d32-201">**Debet:** leasingový závazek XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-201">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="a3d32-202">**Kredit:** Leasingová splátka XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-202">**Credit:** Lease payment XXX</span></span>

## <a name="expense-type-postings"></a><span data-ttu-id="a3d32-203">Zaúčtování typu výdajů</span><span class="sxs-lookup"><span data-stu-id="a3d32-203">Expense type postings</span></span>

<span data-ttu-id="a3d32-204">Účet, který je vybrán pro každý typ výdajů, je debetován při generování platby pro daný typ výdajů.</span><span class="sxs-lookup"><span data-stu-id="a3d32-204">The account that is selected for each expense type is debited when a payment for that expense type is generated.</span></span> <span data-ttu-id="a3d32-205">Například účet určený prontyp výdajů **Pojištění** je debetován, kdykoli je vytvořena položka faktury nebo deníku plateb z rozvrhu zachraňovacích nákladů pro výdaje na pojištění.</span><span class="sxs-lookup"><span data-stu-id="a3d32-205">For example, the account that is specified for the **Insurance** expense type is debited whenever an invoice or payment journal entry is created from the executory cost schedule for insurance expense.</span></span>

<span data-ttu-id="a3d32-206">**Příklad záznamů v deníku:** platba za pojištění</span><span class="sxs-lookup"><span data-stu-id="a3d32-206">**Example journal entries:** Insurance payment</span></span><br>
<span data-ttu-id="a3d32-207">**Debet:** Účet typu výdajů na pojištění XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-207">**Debit:** Insurance expense type account XXX</span></span><br>
<span data-ttu-id="a3d32-208">**Kredit:** Ofsetový účet XXX</span><span class="sxs-lookup"><span data-stu-id="a3d32-208">**Credit:** Offset account XXX</span></span>

> [!NOTE]
> <span data-ttu-id="a3d32-209">Ofsetový účet je vybrán na úrovni leasingu na řádcích pro plán plateb zachraňovacích nákladů.</span><span class="sxs-lookup"><span data-stu-id="a3d32-209">The offset account is selected at the lease level on the lines for the executory cost payment schedule.</span></span> <span data-ttu-id="a3d32-210">Tento offsetový účet lze přidružit k dodavateli nebo k účtu hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="a3d32-210">This offset account can associated with the vendor, or with a ledger account.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]