---
title: Efekty odpisů se storny
description: Tento článek popisuje potenciální důsledky stornování transakcí dlouhodobého majetku.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd4c4a9e7e89b34b1311b38310877b45e4d95b22
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840594"
---
# <a name="depreciation-effects-with-reversals"></a><span data-ttu-id="72c32-103">Efekty odpisů se storny</span><span class="sxs-lookup"><span data-stu-id="72c32-103">Depreciation effects with reversals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72c32-104">Tento článek popisuje potenciální důsledky stornování transakcí dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="72c32-104">This article discusses potential implications of reversing a fixed asset transaction.</span></span> 

<span data-ttu-id="72c32-105">Transakce dlouhodobého majetku a transakce související s dlouhodobým majetkem můžete stornovat.</span><span class="sxs-lookup"><span data-stu-id="72c32-105">You can reverse fixed asset transactions, and the transactions that are associated with a fixed asset.</span></span> <span data-ttu-id="72c32-106">Dále můžete stornovanou transakci odvolat.</span><span class="sxs-lookup"><span data-stu-id="72c32-106">You can also revoke a reversed transaction.</span></span> 

<span data-ttu-id="72c32-107">Můžete stornovat nebo odvolat transakci, která nebyla poslední transakcí zaúčtovanou do knihy pro majetek.</span><span class="sxs-lookup"><span data-stu-id="72c32-107">You can reverse or revoke a transaction that was not the most recent transaction posted to the book for the asset.</span></span> <span data-ttu-id="72c32-108">Nejprve určete, zda byly po transakci, kterou stornujete, zaúčtovány nějaké transakce odpisů.</span><span class="sxs-lookup"><span data-stu-id="72c32-108">You should first determine whether any depreciation transactions were posted after the transaction that you are reversing.</span></span> <span data-ttu-id="72c32-109">Důvodem je skutečnost, že odpisy nejsou při stornování transakce přepočítány.</span><span class="sxs-lookup"><span data-stu-id="72c32-109">This is because depreciation is not recalculated when you reverse a transaction.</span></span> <span data-ttu-id="72c32-110">Proto jsou odpisy často nadhodnoceny nebo podhodnoceny po stornování, jak je uvedeno v příkladech.</span><span class="sxs-lookup"><span data-stu-id="72c32-110">Therefore, depreciation often is overstated or understated after the reversal, as shown in the examples.</span></span> 

<span data-ttu-id="72c32-111">Chcete-li zajistit správnost odpisů při stornování transakce, nepokračujte ve stornování v případě, že během stornování obdržíte zprávu s vysvětlením, že odpisy nebudou přepočítány.</span><span class="sxs-lookup"><span data-stu-id="72c32-111">To make sure that depreciation is correct when you reverse a transaction, do not continue with the reversal if you receive a message that states that depreciation will not be recalculated.</span></span> <span data-ttu-id="72c32-112">Namísto toho nejprve stornujte odpisovou transakci, která byla zaúčtována po transakci, kterou chcete stornovat, a poté pokračujte ve stornování.</span><span class="sxs-lookup"><span data-stu-id="72c32-112">Instead, first reverse the depreciation transaction that was posted after the transaction you tried to reverse, and then continue with the reversal.</span></span> <span data-ttu-id="72c32-113">Nezobrazí se varování o přepočítání odpisů a můžete pokračovat ve stornování.</span><span class="sxs-lookup"><span data-stu-id="72c32-113">You will not be warned about depreciation recalculations, and you can continue with the reversal.</span></span> 

<span data-ttu-id="72c32-114">Následující příklady zobrazují kalkulace, ke kterým dochází při pokračování i přes varovnou zprávu namísto prvního stornování odpisových transakcí.</span><span class="sxs-lookup"><span data-stu-id="72c32-114">The following examples show the calculations that occur if you continue beyond the message without first reversing the depreciation transactions.</span></span>

## <a name="example-1-depreciation-is-overstated"></a><span data-ttu-id="72c32-115"> Příklad 1: Odpisy jsou nadhodnocené</span><span class="sxs-lookup"><span data-stu-id="72c32-115">Example 1: Depreciation is overstated</span></span>
<span data-ttu-id="72c32-116">Pro majetek je nastavena doba životnosti 5 let a lineární metoda odepisování (60 období odepisování).</span><span class="sxs-lookup"><span data-stu-id="72c32-116">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="72c32-117">V tomto příkladu jsou odpisy nadhodnoceny.</span><span class="sxs-lookup"><span data-stu-id="72c32-117">In this example, depreciation is overstated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="72c32-118">Historie transakcí majetku</span><span class="sxs-lookup"><span data-stu-id="72c32-118">Asset transaction history</span></span>

| <span data-ttu-id="72c32-119">Datum</span><span class="sxs-lookup"><span data-stu-id="72c32-119">Date</span></span>       | <span data-ttu-id="72c32-120">Typ transakce</span><span class="sxs-lookup"><span data-stu-id="72c32-120">Transaction type</span></span>                                                          | <span data-ttu-id="72c32-121">Částka</span><span class="sxs-lookup"><span data-stu-id="72c32-121">Amount</span></span>                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="72c32-122">1. leden</span><span class="sxs-lookup"><span data-stu-id="72c32-122">January 1</span></span>  | <span data-ttu-id="72c32-123">Pořizovací cena</span><span class="sxs-lookup"><span data-stu-id="72c32-123">Acquisition</span></span>                                                               | <span data-ttu-id="72c32-124">59 000,00</span><span class="sxs-lookup"><span data-stu-id="72c32-124">59,000.00</span></span>                                 |
| <span data-ttu-id="72c32-125">1. leden</span><span class="sxs-lookup"><span data-stu-id="72c32-125">January 1</span></span>  | <span data-ttu-id="72c32-126">Oprava pořizovací ceny</span><span class="sxs-lookup"><span data-stu-id="72c32-126">Acquisition adjustment</span></span>                                                    | <span data-ttu-id="72c32-127">1 000,00</span><span class="sxs-lookup"><span data-stu-id="72c32-127">1,000.00</span></span>                                  |
| <span data-ttu-id="72c32-128">31. leden</span><span class="sxs-lookup"><span data-stu-id="72c32-128">January 31</span></span> | <span data-ttu-id="72c32-129">Odpisy (vytvořeno pomocí návrhu pro jedno odpisové období)</span><span class="sxs-lookup"><span data-stu-id="72c32-129">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="72c32-130">Kalkulace 1 000,00: Účetní hodnota (59 000 + 1 000) / Počet zbývajících odpisových období (60)</span><span class="sxs-lookup"><span data-stu-id="72c32-130">1,000.00Calculation: Book value (59,000 + 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="72c32-131">Akce Storno</span><span class="sxs-lookup"><span data-stu-id="72c32-131">Reversal action</span></span>

| <span data-ttu-id="72c32-132">Datum</span><span class="sxs-lookup"><span data-stu-id="72c32-132">Date</span></span>      | <span data-ttu-id="72c32-133">Typ transakce</span><span class="sxs-lookup"><span data-stu-id="72c32-133">Transaction type</span></span>                | <span data-ttu-id="72c32-134">Částka</span><span class="sxs-lookup"><span data-stu-id="72c32-134">Amount</span></span>    |
|-----------|---------------------------------|-----------|
| <span data-ttu-id="72c32-135">1. leden</span><span class="sxs-lookup"><span data-stu-id="72c32-135">January 1</span></span> | <span data-ttu-id="72c32-136">Storno opravy pořizovací ceny</span><span class="sxs-lookup"><span data-stu-id="72c32-136">Acquisition adjustment reversal</span></span> | <span data-ttu-id="72c32-137">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="72c32-137">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="72c32-138">Efekt odpisů</span><span class="sxs-lookup"><span data-stu-id="72c32-138">Depreciation effect</span></span>

| <span data-ttu-id="72c32-139">Datum</span><span class="sxs-lookup"><span data-stu-id="72c32-139">Date</span></span>        | <span data-ttu-id="72c32-140">Typ transakce</span><span class="sxs-lookup"><span data-stu-id="72c32-140">Transaction type</span></span>        | <span data-ttu-id="72c32-141">Částka</span><span class="sxs-lookup"><span data-stu-id="72c32-141">Amount</span></span>                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="72c32-142">28. únor</span><span class="sxs-lookup"><span data-stu-id="72c32-142">February 28</span></span> | <span data-ttu-id="72c32-143">Odpis (návrh)</span><span class="sxs-lookup"><span data-stu-id="72c32-143">Depreciation (proposal)</span></span> | <span data-ttu-id="72c32-144">Kalkulace 983,05: Účetní hodnota (59 000 -1 000 odpisy) / Počet zbývajících odpisových období (59)</span><span class="sxs-lookup"><span data-stu-id="72c32-144">983.05Calculation: Book value (59,000 - 1,000 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="72c32-145">Odpisy jsou nadhodnoceny o 16,95 (1 000 - 983,05).</span><span class="sxs-lookup"><span data-stu-id="72c32-145">Depreciation is overstated by 16.95 (1,000 - 983.05).</span></span>

## <a name="example-2-depreciation-is-understated"></a><span data-ttu-id="72c32-146"> Příklad 2: Odpisy jsou podhodnocené</span><span class="sxs-lookup"><span data-stu-id="72c32-146">Example 2: Depreciation is understated</span></span>
<span data-ttu-id="72c32-147">Pro majetek je nastavena doba životnosti 5 let a lineární metoda odepisování (60 období odepisování).</span><span class="sxs-lookup"><span data-stu-id="72c32-147">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="72c32-148">V tomto příkladu jsou odpisy podhodnoceny.</span><span class="sxs-lookup"><span data-stu-id="72c32-148">In this example, depreciation is understated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="72c32-149">Historie transakcí majetku</span><span class="sxs-lookup"><span data-stu-id="72c32-149">Asset transaction history</span></span>

| <span data-ttu-id="72c32-150">Datum</span><span class="sxs-lookup"><span data-stu-id="72c32-150">Date</span></span>       | <span data-ttu-id="72c32-151">Typ transakce</span><span class="sxs-lookup"><span data-stu-id="72c32-151">Transaction type</span></span>                                                          | <span data-ttu-id="72c32-152">Částka</span><span class="sxs-lookup"><span data-stu-id="72c32-152">Amount</span></span>                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="72c32-153">1. leden</span><span class="sxs-lookup"><span data-stu-id="72c32-153">January 1</span></span>  | <span data-ttu-id="72c32-154">Pořizovací cena</span><span class="sxs-lookup"><span data-stu-id="72c32-154">Acquisition</span></span>                                                               | <span data-ttu-id="72c32-155">59 000,00</span><span class="sxs-lookup"><span data-stu-id="72c32-155">59,000.00</span></span>                                   |
| <span data-ttu-id="72c32-156">1. leden</span><span class="sxs-lookup"><span data-stu-id="72c32-156">January 1</span></span>  | <span data-ttu-id="72c32-157">Snížení odpisu</span><span class="sxs-lookup"><span data-stu-id="72c32-157">Write-down adjustment</span></span>                                                     | <span data-ttu-id="72c32-158">1 000,00</span><span class="sxs-lookup"><span data-stu-id="72c32-158">1,000.00</span></span>                                    |
| <span data-ttu-id="72c32-159">31. leden</span><span class="sxs-lookup"><span data-stu-id="72c32-159">January 31</span></span> | <span data-ttu-id="72c32-160">Odpisy (vytvořeno pomocí návrhu pro jedno odpisové období)</span><span class="sxs-lookup"><span data-stu-id="72c32-160">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="72c32-161">Kalkulace 966,67: Účetní hodnota (59 000 - 1 000) / Počet zbývajících odpisových období (60)</span><span class="sxs-lookup"><span data-stu-id="72c32-161">966.67Calculation: Book value (59,000 - 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="72c32-162">Akce Storno</span><span class="sxs-lookup"><span data-stu-id="72c32-162">Reversal action</span></span>

| <span data-ttu-id="72c32-163">Datum</span><span class="sxs-lookup"><span data-stu-id="72c32-163">Date</span></span>      | <span data-ttu-id="72c32-164">Typ transakce</span><span class="sxs-lookup"><span data-stu-id="72c32-164">Transaction type</span></span>               | <span data-ttu-id="72c32-165">Částka</span><span class="sxs-lookup"><span data-stu-id="72c32-165">Amount</span></span>    |
|-----------|--------------------------------|-----------|
| <span data-ttu-id="72c32-166">1. leden</span><span class="sxs-lookup"><span data-stu-id="72c32-166">January 1</span></span> | <span data-ttu-id="72c32-167">Storno snížení odpisu</span><span class="sxs-lookup"><span data-stu-id="72c32-167">Write-down adjustment reversal</span></span> | <span data-ttu-id="72c32-168">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="72c32-168">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="72c32-169">Efekt odpisů</span><span class="sxs-lookup"><span data-stu-id="72c32-169">Depreciation effect</span></span>

| <span data-ttu-id="72c32-170">Datum</span><span class="sxs-lookup"><span data-stu-id="72c32-170">Date</span></span>        | <span data-ttu-id="72c32-171">Typ transakce</span><span class="sxs-lookup"><span data-stu-id="72c32-171">Transaction type</span></span>        | <span data-ttu-id="72c32-172">Částka</span><span class="sxs-lookup"><span data-stu-id="72c32-172">Amount</span></span>                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="72c32-173">28. únor</span><span class="sxs-lookup"><span data-stu-id="72c32-173">February 28</span></span> | <span data-ttu-id="72c32-174">Odpis (návrh)</span><span class="sxs-lookup"><span data-stu-id="72c32-174">Depreciation (proposal)</span></span> | <span data-ttu-id="72c32-175">Kalkulace 983,62: Účetní hodnota (59 000 - 966,67 odpisy) / Počet zbývajících odpisových období (59)</span><span class="sxs-lookup"><span data-stu-id="72c32-175">983.62Calculation: Book value (59,000 - 966.67 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="72c32-176">Odpisy jsou podhodnoceny o 16,95 (983,62 - 966,67).</span><span class="sxs-lookup"><span data-stu-id="72c32-176">Depreciation is understated by 16.95 (983.62 - 966.67).</span></span>



<a name="additional-resources"></a><span data-ttu-id="72c32-177">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="72c32-177">Additional resources</span></span>
--------

[<span data-ttu-id="72c32-178">Odpisy dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="72c32-178">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)



