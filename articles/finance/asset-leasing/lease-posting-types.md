---
title: Typy zaúčtování leasingu
description: Toto téma popisuje typy účtování, které se používají pro transakce leasingu aktiv.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ddc229f3ab8e048390f27503e2c6c26bd1a6f24f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841134"
---
# <a name="lease-posting-types"></a><span data-ttu-id="f4514-103">Typy zaúčtování leasingu</span><span class="sxs-lookup"><span data-stu-id="f4514-103">Lease posting types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4514-104">Toto téma popisuje typy účtování, které se používají pro transakce leasingu aktiv.</span><span class="sxs-lookup"><span data-stu-id="f4514-104">This topic describes the posting types that are used for asset leasing transactions.</span></span>

## <a name="lease-asset"></a><span data-ttu-id="f4514-105">Aktivum leasingu</span><span class="sxs-lookup"><span data-stu-id="f4514-105">Lease asset</span></span>

<span data-ttu-id="f4514-106">Účet je přidružen k používanému majetku (ROU).</span><span class="sxs-lookup"><span data-stu-id="f4514-106">The account is associated with the right-of-use (ROU) asset.</span></span> <span data-ttu-id="f4514-107">Z tohoto účtu je odečtena částka, když je leasing původně uznán podle nových účetních standardů leasingu, tématu Kodifikace účetních standardů 842 (ASC 842) a Mezinárodního standardu účetního výkaznictví 16 (IFRS 16).</span><span class="sxs-lookup"><span data-stu-id="f4514-107">This account is debited when a lease is initially recognized under the new lease accounting standards, Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16).</span></span> <span data-ttu-id="f4514-108">U upraveného leasingu může být z tohoto účtu odečtena nebo připsána částka v závislosti na tom, zda úprava zvyšuje nebo snižuje závazek z leasingu.</span><span class="sxs-lookup"><span data-stu-id="f4514-108">For a modified lease, this account might be either debited or credited, depending on whether the modification increases or decreases the lease liability.</span></span>

<span data-ttu-id="f4514-109">**Příklad záznamů v deníku:** Počáteční uznání</span><span class="sxs-lookup"><span data-stu-id="f4514-109">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="f4514-110">**Debet:** leasign majetku XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-110">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="f4514-111">**Kredit:** leasingový závazek XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-111">**Credit:** Lease liability XXX</span></span>

## <a name="lease-liability"></a><span data-ttu-id="f4514-112">Leasingový závazek</span><span class="sxs-lookup"><span data-stu-id="f4514-112">Lease liability</span></span>

<span data-ttu-id="f4514-113">Účet je spojen s leasingovým závazkem, ke kterému dochází, když jsou platby diskontovány podle nových standardů IFRS 16 a ASC 842.</span><span class="sxs-lookup"><span data-stu-id="f4514-113">The account is associated with the lease liability that occurs when payments are discounted under the new IFRS 16 and ASC 842 standards.</span></span> <span data-ttu-id="f4514-114">Tento účet je kreditován, když je leasing od počátku uznán podle nových standardů.</span><span class="sxs-lookup"><span data-stu-id="f4514-114">This account is credited when a lease is initially recognized under the new standards.</span></span> <span data-ttu-id="f4514-115">Je debetován leasingovými splátkami a kreditován úroky.</span><span class="sxs-lookup"><span data-stu-id="f4514-115">It's debited for lease payments and credited for interest accruals.</span></span>

<span data-ttu-id="f4514-116">**Příklad záznamů v deníku:** Počáteční uznání</span><span class="sxs-lookup"><span data-stu-id="f4514-116">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="f4514-117">**Debet:** leasign majetku XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-117">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="f4514-118">**Kredit:** leasingový závazek XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-118">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="f4514-119">**Příklad záznamů v deníku:** Časové rozlišení úroků</span><span class="sxs-lookup"><span data-stu-id="f4514-119">**Example journal entries:** Interest accrual</span></span><br>
<span data-ttu-id="f4514-120">**Debet:** úrokové náklady XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-120">**Debit:** Interest expense XXX</span></span><br>
<span data-ttu-id="f4514-121">**Kredit:** leasingový závazek XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-121">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="f4514-122">**Příklad záznamů v deníku:** Leasingová splátka</span><span class="sxs-lookup"><span data-stu-id="f4514-122">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="f4514-123">**Debet:** leasingový závazek XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-123">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="f4514-124">**Kredit:** závazek dodavatele / leasingová splátka XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-124">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="short-term-lease-liability"></a><span data-ttu-id="f4514-125">Krátkodobý leasingový závazek</span><span class="sxs-lookup"><span data-stu-id="f4514-125">Short-term lease liability</span></span>

<span data-ttu-id="f4514-126">Účet je spojen s krátkodobým závazkem z leasingu, když je zaúčtován zápis do deníku reklasifikace závazků z krátkodobého pronájmu.</span><span class="sxs-lookup"><span data-stu-id="f4514-126">The account is associated with the short-term lease liability when the short-term lease liability reclass journal entry is posted.</span></span> <span data-ttu-id="f4514-127">Na tento účet se připisuje krátkodobý závazek z amortizačního plánu poslední den v měsíci.</span><span class="sxs-lookup"><span data-stu-id="f4514-127">This account is credited for the short-term liability from the amortization schedule on the last day of the month.</span></span> <span data-ttu-id="f4514-128">Stejná částka je však odečtena první den následujícího měsíce.</span><span class="sxs-lookup"><span data-stu-id="f4514-128">However, the same amount is debited on the first day of the next month.</span></span>

<span data-ttu-id="f4514-129">**Příklad záznamů v deníku:** reklasifikace krátkodobých leasingových závazků</span><span class="sxs-lookup"><span data-stu-id="f4514-129">**Example journal entries:** Short-term lease liability reclass</span></span><br>
<span data-ttu-id="f4514-130">**Debet:** leasingový závazek XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-130">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="f4514-131">**Kredit:** krátkodobý leasingový závazek XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-131">**Credit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="f4514-132">**Debit:** krátkodobý leasingový závazek XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-132">**Debit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="f4514-133">**Kredit:** leasingový závazek XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-133">**Credit:** Lease liability XXX</span></span>

## <a name="depreciation-expense"></a><span data-ttu-id="f4514-134">Odpisové výdaje</span><span class="sxs-lookup"><span data-stu-id="f4514-134">Depreciation expense</span></span>

<span data-ttu-id="f4514-135">Účet je spojen s výdajem, který souvisí s odpisy aktiva ROU podle IFRS 16, ASC 842 a finančního leasingu podle IAS 17 a ASC 840.</span><span class="sxs-lookup"><span data-stu-id="f4514-135">The account is associated with the expense that is related to the depreciation of the ROU asset under IFRS 16, ASC 842, and finance leases under IAS 17 and ASC 840.</span></span> <span data-ttu-id="f4514-136">Tento účet je debetován, když je každý měsíc odepisován používaný majetek.</span><span class="sxs-lookup"><span data-stu-id="f4514-136">This account is debited when an ROU asset is depreciated each month.</span></span>

<span data-ttu-id="f4514-137">**Příklad záznamů v deníku:** Časové rozlišení odpisů</span><span class="sxs-lookup"><span data-stu-id="f4514-137">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="f4514-138">**Debet:** výdej za odpis XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-138">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="f4514-139">**Kredit:** Akumulovaný odpis XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-139">**Credit:** Accumulated Depreciation XXX</span></span>

## <a name="gainloss-on-lease-modification"></a><span data-ttu-id="f4514-140">Zisk/ztráta při upravení leasingu</span><span class="sxs-lookup"><span data-stu-id="f4514-140">Gain/loss on lease modification</span></span>

<span data-ttu-id="f4514-141">Účet je spojen s jakýmikoli zisky nebo ztrátami, které vzniknou úpravami leasingu.</span><span class="sxs-lookup"><span data-stu-id="f4514-141">The account is associated with any gains or losses that arise from lease modifications.</span></span> <span data-ttu-id="f4514-142">Zisk může vzniknout během úpravy leasingu, pokud tato úprava sníží závazek z leasingu o částku, která přesahuje účetní hodnotu aktiva ROU.</span><span class="sxs-lookup"><span data-stu-id="f4514-142">A gain might arise during a lease modification if the modification decreases the lease liability by an amount that exceeds the carrying value of the ROU asset.</span></span>

<span data-ttu-id="f4514-143">Například leasing má aktuální účetní hodnotu závazku z leasingu ve výši $150 000 a účetní hodnotu aktiva ROU ve výši $100 000.</span><span class="sxs-lookup"><span data-stu-id="f4514-143">For example, a lease has a current carrying value of the lease liability of $150,000 and a carrying value of the ROU asset of $100,000.</span></span> <span data-ttu-id="f4514-144">Leasing je upraven a tato úprava vytváří novou současnou hodnotu budoucích minimálních leasingových plateb (PVFMLP) ve výši $ 40 000.</span><span class="sxs-lookup"><span data-stu-id="f4514-144">The lease is modified, and this modification produces a new present value of the future minimum lease payments (PVFMLP) of $40,000.</span></span> <span data-ttu-id="f4514-145">Proto bude odpovědnost za leasing stržena společností $110 000 (150 000 $ - $40 000).</span><span class="sxs-lookup"><span data-stu-id="f4514-145">Therefore, the lease liability will be debited by $110,000 ($150,000 – $40,000).</span></span> <span data-ttu-id="f4514-146">Protože používaný majetek je pouze $100 000, snížení $110 000 sníží aktivum za 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="f4514-146">Because the ROU asset is only $100,000, the decrease of $110,000 will decrease the asset past 0 (zero).</span></span> <span data-ttu-id="f4514-147">Účetní pokyny proto stanoví, že zbytek by měl být zaúčtován na účet zisků.</span><span class="sxs-lookup"><span data-stu-id="f4514-147">Therefore, the accounting guidance states that the remainder should be booked to a gain account.</span></span> <span data-ttu-id="f4514-148">V tomto případě bude konečným zápisem do deníku debit z leasingové odpovědnosti za $110 000, kredit z leasingového aktiva za $100 000 a kredit na účtu zisku $10 000.</span><span class="sxs-lookup"><span data-stu-id="f4514-148">In this case, the final journal entry will be a debit to the lease liability for $110,000, a credit to the lease asset for $100,000, and a credit to the gain account for $10,000.</span></span>

<span data-ttu-id="f4514-149">**Příklad záznamů v deníku:** Leasingová úprava</span><span class="sxs-lookup"><span data-stu-id="f4514-149">**Example journal entries:** Lease modification</span></span><br>
<span data-ttu-id="f4514-150">**Debet:** leasingový závazek XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-150">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="f4514-151">**Kredit** leasing majetku XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-151">**Credit:** Lease Asset XXX</span></span><br>
<span data-ttu-id="f4514-152">**Kredit:** Zisk XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-152">**Credit:** Gain XXX</span></span>

## <a name="accumulated-depreciation"></a><span data-ttu-id="f4514-153">Akumulovaný odpis</span><span class="sxs-lookup"><span data-stu-id="f4514-153">Accumulated depreciation</span></span>

<span data-ttu-id="f4514-154">Účet je přidružen k protiúčtu majetku používaného majetku.</span><span class="sxs-lookup"><span data-stu-id="f4514-154">The account is associated with the contra-asset account of the ROU asset.</span></span> <span data-ttu-id="f4514-155">Účet je kreditován při zaúčtování výdaje odpisu.</span><span class="sxs-lookup"><span data-stu-id="f4514-155">This account is credited when a depreciation expense is posted.</span></span>

<span data-ttu-id="f4514-156">**Příklad záznamů v deníku:** Časové rozlišení odpisů</span><span class="sxs-lookup"><span data-stu-id="f4514-156">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="f4514-157">**Debet:** výdej za odpis XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-157">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="f4514-158">**Kredit:** Akumulovaný odpis XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-158">**Credit:** Accumulated depreciation XXX</span></span>

## <a name="variable-payment"></a><span data-ttu-id="f4514-159">Variabilní splátka</span><span class="sxs-lookup"><span data-stu-id="f4514-159">Variable payment</span></span>

<span data-ttu-id="f4514-160">Účet je spojen s variabilními leasingovými splátkami, které vznikají přeceněním indexu podle leasingů dle ASC 842, ASC 840 a IAS 17.</span><span class="sxs-lookup"><span data-stu-id="f4514-160">The account is associated with variable lease payments that are produced by an index revaluation under ASC 842, ASC 840, and IAS 17 leases.</span></span> <span data-ttu-id="f4514-161">V harmonogramu splátek leasingu jsou variabilní splátky zahrnuty ve sloupci **Variabilní splátka**.</span><span class="sxs-lookup"><span data-stu-id="f4514-161">In the lease payment schedule, variable payments are included in the **Variable payment** column.</span></span> <span data-ttu-id="f4514-162">Z tohoto účtu je odečtena částka, když je faktura vytvořena na řádku plánu splátek, který obsahuje variabilní splátku.</span><span class="sxs-lookup"><span data-stu-id="f4514-162">This account is debited when an invoice is created against a payment schedule line that contains a variable payment.</span></span>

<span data-ttu-id="f4514-163">**Příklad záznamů v deníku:** Leasingová splátka</span><span class="sxs-lookup"><span data-stu-id="f4514-163">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="f4514-164">**Debet:** leasingový závazek XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-164">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="f4514-165">**Debet:** Variabilní splátka XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-165">**Debit:** Variable payment XXX</span></span><br>
<span data-ttu-id="f4514-166">**Kredit:** závazek dodavatele / leasingová splátka XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-166">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="deferred-rent-asset-liability"></a><span data-ttu-id="f4514-167">Aktivum (pasivum) odložené splátky</span><span class="sxs-lookup"><span data-stu-id="f4514-167">Deferred rent asset (liability)</span></span>

<span data-ttu-id="f4514-168">Účet je spojen s aktivem nebo pasivem odložené splátky, který je vytvořen odložením splátky leasingu.</span><span class="sxs-lookup"><span data-stu-id="f4514-168">The account is associated with the deferred rent asset or liability that is produced by a deferred rent treatment lease.</span></span> <span data-ttu-id="f4514-169">Z tohoto účtu je odečtena částka, když je faktura zaúčtována proti odložené splátce leasingu, pokud je částka leasingové splátky vyšší než lineární výdaje leasingu za dané období.</span><span class="sxs-lookup"><span data-stu-id="f4514-169">This account is debited when an invoice is posted against a deferred rent treatment lease, if the lease payment amount is more than the period's straight-line rent expense.</span></span> <span data-ttu-id="f4514-170">Je kreditován, pokud je leasingová splátka nižší než lineární výdaje leasingu v daném období.</span><span class="sxs-lookup"><span data-stu-id="f4514-170">It's credited if the lease payment is less than the period's straight-line rent expense.</span></span>

<span data-ttu-id="f4514-171">**Příklad záznamů v deníku:** Leasingová splátka (leasing s odloženými splátkami)</span><span class="sxs-lookup"><span data-stu-id="f4514-171">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="f4514-172">**Debet:** leasingový výdaj XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-172">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="f4514-173">**Kredit:** pasivum odložené splátky XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-173">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="f4514-174">**Kredit:** závazek dodavatele / leasingová splátka XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-174">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="lease-expense"></a><span data-ttu-id="f4514-175">Výdaje leasingu</span><span class="sxs-lookup"><span data-stu-id="f4514-175">Lease expense</span></span>

<span data-ttu-id="f4514-176">Účet je spojen s náklady na leasing, pokud je leasing klasifikován jako leasing s opožděnými splátkami.</span><span class="sxs-lookup"><span data-stu-id="f4514-176">The account is associated with the lease expense if the lease is classified as a deferred rent treatment lease.</span></span> <span data-ttu-id="f4514-177">Z tohoto účtu je odečtena částka, když je faktura zaúčtována na základě odložené splátky.</span><span class="sxs-lookup"><span data-stu-id="f4514-177">This account is debited when an invoice is posted against a deferred rent treatment lease.</span></span>

<span data-ttu-id="f4514-178">**Příklad záznamů v deníku:** Leasingová splátka (leasing s odloženými splátkami)</span><span class="sxs-lookup"><span data-stu-id="f4514-178">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="f4514-179">**Debet:** leasingový výdaj XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-179">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="f4514-180">**Kredit:** pasivum odložené splátky XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-180">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="f4514-181">**Kredit:** závazek dodavatele / leasingová splátka XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-181">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="impairment-expense"></a><span data-ttu-id="f4514-182">Výdaje snížení hodnoty</span><span class="sxs-lookup"><span data-stu-id="f4514-182">Impairment expense</span></span>

<span data-ttu-id="f4514-183">Proti účtu se účtuje, když je snížena hodnota leasingu.</span><span class="sxs-lookup"><span data-stu-id="f4514-183">The account is posted against when a lease is impaired.</span></span> <span data-ttu-id="f4514-184">Tento účet je debetován, zatímco účet používaného majetku je přímo kreditován.</span><span class="sxs-lookup"><span data-stu-id="f4514-184">This account is debited, whereas the ROU asset account is directly credited.</span></span>

<span data-ttu-id="f4514-185">**Příklad záznamů v deníku:** Leasingová splátka</span><span class="sxs-lookup"><span data-stu-id="f4514-185">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="f4514-186">**Debet:** Výdaj snížení hodnoty XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-186">**Debit:** Impairment expense XXX</span></span><br>
<span data-ttu-id="f4514-187">**Kredit:** používaný majetek XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-187">**Credit:** ROU asset XXX</span></span>

## <a name="lease-payment"></a><span data-ttu-id="f4514-188">Leasingová splátka</span><span class="sxs-lookup"><span data-stu-id="f4514-188">Lease payment</span></span>

<span data-ttu-id="f4514-189">Proti účtu se provede účetní zápis, pokud je vypnutý parametr **Platba dodavateli**.</span><span class="sxs-lookup"><span data-stu-id="f4514-189">The account is posted against if the **Pay to Vendor** parameter is turned off.</span></span> <span data-ttu-id="f4514-190">Tento účet je kreditován místo závazku dodavateli, pokud je parametr vypnutý.</span><span class="sxs-lookup"><span data-stu-id="f4514-190">This account is credited instead of the vendor payable if the parameter is turned off.</span></span>

<span data-ttu-id="f4514-191">**Příklad záznamů v deníku:** Leasingová splátka</span><span class="sxs-lookup"><span data-stu-id="f4514-191">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="f4514-192">**Debet:** leasingový závazek XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-192">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="f4514-193">**Kredit:** Leasingová splátka XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-193">**Credit:** Lease payment XXX</span></span>

## <a name="expense-type-postings"></a><span data-ttu-id="f4514-194">Zaúčtování typu výdajů</span><span class="sxs-lookup"><span data-stu-id="f4514-194">Expense type postings</span></span>

<span data-ttu-id="f4514-195">Účet, který je vybrán pro každý typ výdajů, je debetován při generování platby pro daný typ výdajů.</span><span class="sxs-lookup"><span data-stu-id="f4514-195">The account that is selected for each expense type is debited when a payment for that expense type is generated.</span></span> <span data-ttu-id="f4514-196">Například účet určený prontyp výdajů **Pojištění** je debetován, kdykoli je vytvořena položka faktury nebo deníku plateb z rozvrhu zachraňovacích nákladů pro výdaje na pojištění.</span><span class="sxs-lookup"><span data-stu-id="f4514-196">For example, the account that is specified for the **Insurance** expense type is debited whenever an invoice or payment journal entry is created from the executory cost schedule for insurance expense.</span></span>

<span data-ttu-id="f4514-197">**Příklad záznamů v deníku:** platba za pojištění</span><span class="sxs-lookup"><span data-stu-id="f4514-197">**Example journal entries:** Insurance payment</span></span><br>
<span data-ttu-id="f4514-198">**Debet:** Účet typu výdajů na pojištění XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-198">**Debit:** Insurance expense type account XXX</span></span><br>
<span data-ttu-id="f4514-199">**Kredit:** Ofsetový účet XXX</span><span class="sxs-lookup"><span data-stu-id="f4514-199">**Credit:** Offset account XXX</span></span>

> [!NOTE]
> <span data-ttu-id="f4514-200">Ofsetový účet je vybrán na úrovni leasingu na řádcích pro plán plateb zachraňovacích nákladů.</span><span class="sxs-lookup"><span data-stu-id="f4514-200">The offset account is selected at the lease level on the lines for the executory cost payment schedule.</span></span> <span data-ttu-id="f4514-201">Tento offsetový účet lze přidružit k dodavateli nebo k účtu hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="f4514-201">This offset account can associated with the vendor, or with a ledger account.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
