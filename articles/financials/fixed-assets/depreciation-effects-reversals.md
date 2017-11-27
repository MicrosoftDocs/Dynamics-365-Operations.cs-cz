---
title: "Efekty odpisů se storny"
description: "Tento článek popisuje potenciální důsledky stornování transakcí dlouhodobého majetku."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6672047cb3234e4432190d3afb20f46827ad5ef4
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="depreciation-effects-with-reversals"></a><span data-ttu-id="baea9-103">Efekty odpisů se storny</span><span class="sxs-lookup"><span data-stu-id="baea9-103">Depreciation effects with reversals</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="baea9-104">Tento článek popisuje potenciální důsledky stornování transakcí dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="baea9-104">This article discusses potential implications of reversing a fixed asset transaction.</span></span> 

<span data-ttu-id="baea9-105">Transakce dlouhodobého majetku a transakce související s dlouhodobým majetkem můžete stornovat.</span><span class="sxs-lookup"><span data-stu-id="baea9-105">You can reverse fixed asset transactions, and the transactions that are associated with a fixed asset.</span></span> <span data-ttu-id="baea9-106">Dále můžete stornovanou transakci odvolat.</span><span class="sxs-lookup"><span data-stu-id="baea9-106">You can also revoke a reversed transaction.</span></span> 

<span data-ttu-id="baea9-107">Můžete stornovat nebo odvolat transakci, která nebyla poslední transakcí zaúčtovanou do knihy pro majetek.</span><span class="sxs-lookup"><span data-stu-id="baea9-107">You can reverse or revoke a transaction that was not the most recent transaction posted to the book for the asset.</span></span> <span data-ttu-id="baea9-108">Nejprve určete, zda byly po transakci, kterou stornujete, zaúčtovány nějaké transakce odpisů.</span><span class="sxs-lookup"><span data-stu-id="baea9-108">You should first determine whether any depreciation transactions were posted after the transaction that you are reversing.</span></span> <span data-ttu-id="baea9-109">Důvodem je skutečnost, že odpisy nejsou při stornování transakce přepočítány.</span><span class="sxs-lookup"><span data-stu-id="baea9-109">This is because depreciation is not recalculated when you reverse a transaction.</span></span> <span data-ttu-id="baea9-110">Proto jsou odpisy často nadhodnoceny nebo podhodnoceny po stornování, jak je uvedeno v příkladech.</span><span class="sxs-lookup"><span data-stu-id="baea9-110">Therefore, depreciation often is overstated or understated after the reversal, as shown in the examples.</span></span> 

<span data-ttu-id="baea9-111">Chcete-li zajistit správnost odpisů při stornování transakce, nepokračujte ve stornování v případě, že během stornování obdržíte zprávu s vysvětlením, že odpisy nebudou přepočítány.</span><span class="sxs-lookup"><span data-stu-id="baea9-111">To make sure that depreciation is correct when you reverse a transaction, do not continue with the reversal if you receive a message that states that depreciation will not be recalculated.</span></span> <span data-ttu-id="baea9-112">Namísto toho nejprve stornujte odpisovou transakci, která byla zaúčtována po transakci, kterou chcete stornovat, a poté pokračujte ve stornování.</span><span class="sxs-lookup"><span data-stu-id="baea9-112">Instead, first reverse the depreciation transaction that was posted after the transaction you tried to reverse, and then continue with the reversal.</span></span> <span data-ttu-id="baea9-113">Nezobrazí se varování o přepočítání odpisů a můžete pokračovat ve stornování.</span><span class="sxs-lookup"><span data-stu-id="baea9-113">You will not be warned about depreciation recalculations, and you can continue with the reversal.</span></span> 

<span data-ttu-id="baea9-114">Následující příklady zobrazují kalkulace, ke kterým dochází při pokračování i přes varovnou zprávu namísto prvního stornování odpisových transakcí.</span><span class="sxs-lookup"><span data-stu-id="baea9-114">The following examples show the calculations that occur if you continue beyond the message without first reversing the depreciation transactions.</span></span>

## <a name="example-1-depreciation-is-overstated"></a><span data-ttu-id="baea9-115"> Příklad 1: Odpisy jsou nadhodnocené</span><span class="sxs-lookup"><span data-stu-id="baea9-115">Example 1: Depreciation is overstated</span></span>
<span data-ttu-id="baea9-116">Pro majetek je nastavena doba životnosti 5 let a lineární metoda odepisování (60 období odepisování).</span><span class="sxs-lookup"><span data-stu-id="baea9-116">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="baea9-117">V tomto příkladu jsou odpisy nadhodnoceny.</span><span class="sxs-lookup"><span data-stu-id="baea9-117">In this example, depreciation is overstated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="baea9-118">Historie transakcí majetku</span><span class="sxs-lookup"><span data-stu-id="baea9-118">Asset transaction history</span></span>

| <span data-ttu-id="baea9-119">Datum</span><span class="sxs-lookup"><span data-stu-id="baea9-119">Date</span></span>       | <span data-ttu-id="baea9-120">Typ transakce</span><span class="sxs-lookup"><span data-stu-id="baea9-120">Transaction type</span></span>                                                          | <span data-ttu-id="baea9-121">Částka</span><span class="sxs-lookup"><span data-stu-id="baea9-121">Amount</span></span>                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="baea9-122">1. leden</span><span class="sxs-lookup"><span data-stu-id="baea9-122">January 1</span></span>  | <span data-ttu-id="baea9-123">Pořizovací cena</span><span class="sxs-lookup"><span data-stu-id="baea9-123">Acquisition</span></span>                                                               | <span data-ttu-id="baea9-124">59 000,00</span><span class="sxs-lookup"><span data-stu-id="baea9-124">59,000.00</span></span>                                 |
| <span data-ttu-id="baea9-125">1. leden</span><span class="sxs-lookup"><span data-stu-id="baea9-125">January 1</span></span>  | <span data-ttu-id="baea9-126">Oprava pořizovací ceny</span><span class="sxs-lookup"><span data-stu-id="baea9-126">Acquisition adjustment</span></span>                                                    | <span data-ttu-id="baea9-127">1 000,00</span><span class="sxs-lookup"><span data-stu-id="baea9-127">1,000.00</span></span>                                  |
| <span data-ttu-id="baea9-128">31. leden</span><span class="sxs-lookup"><span data-stu-id="baea9-128">January 31</span></span> | <span data-ttu-id="baea9-129">Odpisy (vytvořeno pomocí návrhu pro jedno odpisové období)</span><span class="sxs-lookup"><span data-stu-id="baea9-129">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="baea9-130">Kalkulace 1 000,00: Účetní hodnota (59 000 + 1 000) / Počet zbývajících odpisových období (60)</span><span class="sxs-lookup"><span data-stu-id="baea9-130">1,000.00Calculation: Book value (59,000 + 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="baea9-131">Akce Storno</span><span class="sxs-lookup"><span data-stu-id="baea9-131">Reversal action</span></span>

| <span data-ttu-id="baea9-132">Datum</span><span class="sxs-lookup"><span data-stu-id="baea9-132">Date</span></span>      | <span data-ttu-id="baea9-133">Typ transakce</span><span class="sxs-lookup"><span data-stu-id="baea9-133">Transaction type</span></span>                | <span data-ttu-id="baea9-134">Částka</span><span class="sxs-lookup"><span data-stu-id="baea9-134">Amount</span></span>    |
|-----------|---------------------------------|-----------|
| <span data-ttu-id="baea9-135">1. leden</span><span class="sxs-lookup"><span data-stu-id="baea9-135">January 1</span></span> | <span data-ttu-id="baea9-136">Storno opravy pořizovací ceny</span><span class="sxs-lookup"><span data-stu-id="baea9-136">Acquisition adjustment reversal</span></span> | <span data-ttu-id="baea9-137">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="baea9-137">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="baea9-138">Efekt odpisů</span><span class="sxs-lookup"><span data-stu-id="baea9-138">Depreciation effect</span></span>

| <span data-ttu-id="baea9-139">Datum</span><span class="sxs-lookup"><span data-stu-id="baea9-139">Date</span></span>        | <span data-ttu-id="baea9-140">Typ transakce</span><span class="sxs-lookup"><span data-stu-id="baea9-140">Transaction type</span></span>        | <span data-ttu-id="baea9-141">Částka</span><span class="sxs-lookup"><span data-stu-id="baea9-141">Amount</span></span>                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="baea9-142">28. únor</span><span class="sxs-lookup"><span data-stu-id="baea9-142">February 28</span></span> | <span data-ttu-id="baea9-143">Odpis (návrh)</span><span class="sxs-lookup"><span data-stu-id="baea9-143">Depreciation (proposal)</span></span> | <span data-ttu-id="baea9-144">Kalkulace 983,05: Účetní hodnota (59 000 -1 000 odpisy) / Počet zbývajících odpisových období (59)</span><span class="sxs-lookup"><span data-stu-id="baea9-144">983.05Calculation: Book value (59,000 - 1,000 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="baea9-145">Odpisy jsou nadhodnoceny o 16,95 (1 000 - 983,05).</span><span class="sxs-lookup"><span data-stu-id="baea9-145">Depreciation is overstated by 16.95 (1,000 - 983.05).</span></span>

## <a name="example-2-depreciation-is-understated"></a><span data-ttu-id="baea9-146"> Příklad 2: Odpisy jsou podhodnocené</span><span class="sxs-lookup"><span data-stu-id="baea9-146">Example 2: Depreciation is understated</span></span>
<span data-ttu-id="baea9-147">Pro majetek je nastavena doba životnosti 5 let a lineární metoda odepisování (60 období odepisování).</span><span class="sxs-lookup"><span data-stu-id="baea9-147">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="baea9-148">V tomto příkladu jsou odpisy podhodnoceny.</span><span class="sxs-lookup"><span data-stu-id="baea9-148">In this example, depreciation is understated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="baea9-149">Historie transakcí majetku</span><span class="sxs-lookup"><span data-stu-id="baea9-149">Asset transaction history</span></span>

| <span data-ttu-id="baea9-150">Datum</span><span class="sxs-lookup"><span data-stu-id="baea9-150">Date</span></span>       | <span data-ttu-id="baea9-151">Typ transakce</span><span class="sxs-lookup"><span data-stu-id="baea9-151">Transaction type</span></span>                                                          | <span data-ttu-id="baea9-152">Částka</span><span class="sxs-lookup"><span data-stu-id="baea9-152">Amount</span></span>                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="baea9-153">1. leden</span><span class="sxs-lookup"><span data-stu-id="baea9-153">January 1</span></span>  | <span data-ttu-id="baea9-154">Pořizovací cena</span><span class="sxs-lookup"><span data-stu-id="baea9-154">Acquisition</span></span>                                                               | <span data-ttu-id="baea9-155">59 000,00</span><span class="sxs-lookup"><span data-stu-id="baea9-155">59,000.00</span></span>                                   |
| <span data-ttu-id="baea9-156">1. leden</span><span class="sxs-lookup"><span data-stu-id="baea9-156">January 1</span></span>  | <span data-ttu-id="baea9-157">Snížení odpisu</span><span class="sxs-lookup"><span data-stu-id="baea9-157">Write-down adjustment</span></span>                                                     | <span data-ttu-id="baea9-158">1 000,00</span><span class="sxs-lookup"><span data-stu-id="baea9-158">1,000.00</span></span>                                    |
| <span data-ttu-id="baea9-159">31. leden</span><span class="sxs-lookup"><span data-stu-id="baea9-159">January 31</span></span> | <span data-ttu-id="baea9-160">Odpisy (vytvořeno pomocí návrhu pro jedno odpisové období)</span><span class="sxs-lookup"><span data-stu-id="baea9-160">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="baea9-161">Kalkulace 966,67: Účetní hodnota (59 000 - 1 000) / Počet zbývajících odpisových období (60)</span><span class="sxs-lookup"><span data-stu-id="baea9-161">966.67Calculation: Book value (59,000 - 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="baea9-162">Akce Storno</span><span class="sxs-lookup"><span data-stu-id="baea9-162">Reversal action</span></span>

| <span data-ttu-id="baea9-163">Datum</span><span class="sxs-lookup"><span data-stu-id="baea9-163">Date</span></span>      | <span data-ttu-id="baea9-164">Typ transakce</span><span class="sxs-lookup"><span data-stu-id="baea9-164">Transaction type</span></span>               | <span data-ttu-id="baea9-165">Částka</span><span class="sxs-lookup"><span data-stu-id="baea9-165">Amount</span></span>    |
|-----------|--------------------------------|-----------|
| <span data-ttu-id="baea9-166">1. leden</span><span class="sxs-lookup"><span data-stu-id="baea9-166">January 1</span></span> | <span data-ttu-id="baea9-167">Storno snížení odpisu</span><span class="sxs-lookup"><span data-stu-id="baea9-167">Write-down adjustment reversal</span></span> | <span data-ttu-id="baea9-168">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="baea9-168">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="baea9-169">Efekt odpisů</span><span class="sxs-lookup"><span data-stu-id="baea9-169">Depreciation effect</span></span>

| <span data-ttu-id="baea9-170">Datum</span><span class="sxs-lookup"><span data-stu-id="baea9-170">Date</span></span>        | <span data-ttu-id="baea9-171">Typ transakce</span><span class="sxs-lookup"><span data-stu-id="baea9-171">Transaction type</span></span>        | <span data-ttu-id="baea9-172">Částka</span><span class="sxs-lookup"><span data-stu-id="baea9-172">Amount</span></span>                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="baea9-173">28. únor</span><span class="sxs-lookup"><span data-stu-id="baea9-173">February 28</span></span> | <span data-ttu-id="baea9-174">Odpis (návrh)</span><span class="sxs-lookup"><span data-stu-id="baea9-174">Depreciation (proposal)</span></span> | <span data-ttu-id="baea9-175">Kalkulace 983,62: Účetní hodnota (59 000 - 966,67 odpisy) / Počet zbývajících odpisových období (59)</span><span class="sxs-lookup"><span data-stu-id="baea9-175">983.62Calculation: Book value (59,000 - 966.67 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="baea9-176">Odpisy jsou podhodnoceny o 16,95 (983,62 - 966,67).</span><span class="sxs-lookup"><span data-stu-id="baea9-176">Depreciation is understated by 16.95 (983.62 - 966.67).</span></span>



<a name="see-also"></a><span data-ttu-id="baea9-177">Viz také</span><span class="sxs-lookup"><span data-stu-id="baea9-177">See also</span></span>
--------

[<span data-ttu-id="baea9-178">Odpisy dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="baea9-178">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)




