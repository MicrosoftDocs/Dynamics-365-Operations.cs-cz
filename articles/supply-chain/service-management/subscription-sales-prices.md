---
title: "Prodejní cena předplatného"
description: "Při vytváření předplatného je prodejní cena odvozena od nastavení prodejní ceny vytvořené ve formuláři Prodejní cena (předplatné)."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 5e18690f7e9b790ecbd0ac0de1955fc95ab1f082
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---

# <a name="subscription-sales-prices"></a><span data-ttu-id="ef935-103">Prodejní cena předplatného</span><span class="sxs-lookup"><span data-stu-id="ef935-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="ef935-104">Při vytváření předplatného je prodejní cena odvozena od nastavení prodejní ceny vytvořené ve formuláři **Prodejní cena (předplatné)**.</span><span class="sxs-lookup"><span data-stu-id="ef935-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="ef935-105">Ve formuláři **Prodejní cena (předplatné)** můžete vytvořit prodejní ceny pro konkrétní předplatné nebo můžete vytvořit obecněji platné prodejní ceny.</span><span class="sxs-lookup"><span data-stu-id="ef935-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="ef935-106">Aby byla prodejní cena u předplatného použita, musí být kód období a měna předplatného a prodejní stejný jako kód období a měna prodejní ceny.</span><span class="sxs-lookup"><span data-stu-id="ef935-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="ef935-107">Jestliže jsou kód období a měna pro předplatné i pro prodejní cenu identické, jsou prodejní ceny předplatného vybírány na základě priorit uvedených v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="ef935-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="ef935-108">Prázdná buňka v tabulce označuje prázdné pole a X označuje, že je hodnota rovna hodnotě předplatného, ze které je transakce generována.</span><span class="sxs-lookup"><span data-stu-id="ef935-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ef935-109">Priorita </span><span class="sxs-lookup"><span data-stu-id="ef935-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="ef935-110"><strong>Kategorie</strong></span><span class="sxs-lookup"><span data-stu-id="ef935-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="ef935-111"><strong>ID projektu</strong></span><span class="sxs-lookup"><span data-stu-id="ef935-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="ef935-112"><strong>Předplatné</strong></span><span class="sxs-lookup"><span data-stu-id="ef935-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="ef935-113"><strong>Měna prodeje</strong></span><span class="sxs-lookup"><span data-stu-id="ef935-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="ef935-114"><strong>Kód období</strong></span><span class="sxs-lookup"><span data-stu-id="ef935-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef935-115">1</span><span class="sxs-lookup"><span data-stu-id="ef935-115">1</span></span></p></td>
<td><p><span data-ttu-id="ef935-116">X</span><span class="sxs-lookup"><span data-stu-id="ef935-116">X</span></span></p></td>
<td><p><span data-ttu-id="ef935-117">X</span><span class="sxs-lookup"><span data-stu-id="ef935-117">X</span></span></p></td>
<td><p><span data-ttu-id="ef935-118">X</span><span class="sxs-lookup"><span data-stu-id="ef935-118">X</span></span></p></td>
<td><p><span data-ttu-id="ef935-119">X</span><span class="sxs-lookup"><span data-stu-id="ef935-119">X</span></span></p></td>
<td><p><span data-ttu-id="ef935-120">X</span><span class="sxs-lookup"><span data-stu-id="ef935-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef935-121">2</span><span class="sxs-lookup"><span data-stu-id="ef935-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="ef935-122">X</span><span class="sxs-lookup"><span data-stu-id="ef935-122">X</span></span></p></td>
<td><p><span data-ttu-id="ef935-123">X</span><span class="sxs-lookup"><span data-stu-id="ef935-123">X</span></span></p></td>
<td><p><span data-ttu-id="ef935-124">X</span><span class="sxs-lookup"><span data-stu-id="ef935-124">X</span></span></p></td>
<td><p><span data-ttu-id="ef935-125">X</span><span class="sxs-lookup"><span data-stu-id="ef935-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef935-126">3</span><span class="sxs-lookup"><span data-stu-id="ef935-126">3</span></span></p></td>
<td><p><span data-ttu-id="ef935-127">X</span><span class="sxs-lookup"><span data-stu-id="ef935-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="ef935-128">X</span><span class="sxs-lookup"><span data-stu-id="ef935-128">X</span></span></p></td>
<td><p><span data-ttu-id="ef935-129">X</span><span class="sxs-lookup"><span data-stu-id="ef935-129">X</span></span></p></td>
<td><p><span data-ttu-id="ef935-130">X</span><span class="sxs-lookup"><span data-stu-id="ef935-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef935-131">4</span><span class="sxs-lookup"><span data-stu-id="ef935-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="ef935-132">X</span><span class="sxs-lookup"><span data-stu-id="ef935-132">X</span></span></p></td>
<td><p><span data-ttu-id="ef935-133">X</span><span class="sxs-lookup"><span data-stu-id="ef935-133">X</span></span></p></td>
<td><p><span data-ttu-id="ef935-134">X</span><span class="sxs-lookup"><span data-stu-id="ef935-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef935-135">5</span><span class="sxs-lookup"><span data-stu-id="ef935-135">5</span></span></p></td>
<td><p><span data-ttu-id="ef935-136">X</span><span class="sxs-lookup"><span data-stu-id="ef935-136">X</span></span></p></td>
<td><p><span data-ttu-id="ef935-137">X</span><span class="sxs-lookup"><span data-stu-id="ef935-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="ef935-138">X</span><span class="sxs-lookup"><span data-stu-id="ef935-138">X</span></span></p></td>
<td><p><span data-ttu-id="ef935-139">X</span><span class="sxs-lookup"><span data-stu-id="ef935-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef935-140">6</span><span class="sxs-lookup"><span data-stu-id="ef935-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="ef935-141">X</span><span class="sxs-lookup"><span data-stu-id="ef935-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="ef935-142">X</span><span class="sxs-lookup"><span data-stu-id="ef935-142">X</span></span></p></td>
<td><p><span data-ttu-id="ef935-143">X</span><span class="sxs-lookup"><span data-stu-id="ef935-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef935-144">7</span><span class="sxs-lookup"><span data-stu-id="ef935-144">7</span></span></p></td>
<td><p><span data-ttu-id="ef935-145">X</span><span class="sxs-lookup"><span data-stu-id="ef935-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="ef935-146">X</span><span class="sxs-lookup"><span data-stu-id="ef935-146">X</span></span></p></td>
<td><p><span data-ttu-id="ef935-147">X</span><span class="sxs-lookup"><span data-stu-id="ef935-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef935-148">8</span><span class="sxs-lookup"><span data-stu-id="ef935-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="ef935-149">X</span><span class="sxs-lookup"><span data-stu-id="ef935-149">X</span></span></p></td>
<td><p><span data-ttu-id="ef935-150">X</span><span class="sxs-lookup"><span data-stu-id="ef935-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef935-151">Pokud je vytvořen poplatek předplatného, je jako prodejní cena předplatného vybrána prodejní cena s nejvyšší úrovní podrobností, jak je uvedeno v předchozí tabulce.</span><span class="sxs-lookup"><span data-stu-id="ef935-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="ef935-152">Aktualizace a indexování prodejních cen předplatného</span><span class="sxs-lookup"><span data-stu-id="ef935-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="ef935-153">Prodejní cenu předplatného můžete aktualizovat aktualizováním základní ceny nebo indexu.</span><span class="sxs-lookup"><span data-stu-id="ef935-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="ef935-154">Aktualizovat lze o procentuální hodnotu nebo na novou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ef935-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="ef935-155">Prodejní ceny poplatků předplatného</span><span class="sxs-lookup"><span data-stu-id="ef935-155">Subscription fee sales prices</span></span>

<span data-ttu-id="ef935-156">Při vytváření poplatku odběru je prodejní cena založena na nastavení prodejní ceny předplatného.</span><span class="sxs-lookup"><span data-stu-id="ef935-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="ef935-157">Můžete buď použít základní cenu z nastavení ceny předplatného, nebo vytvořit indexované prodejní ceny.</span><span class="sxs-lookup"><span data-stu-id="ef935-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="ef935-158">Příklad</span><span class="sxs-lookup"><span data-stu-id="ef935-158">Example</span></span>

<span data-ttu-id="ef935-159">Chcete nastavit prodejní ceny předplatného na 500 EUR pro nový projekt 9030.</span><span class="sxs-lookup"><span data-stu-id="ef935-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="ef935-160">Ve formuláři **prodejní cena (předplatné)** vytvoříte řádek prodejní ceny předplatného podle návodu v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="ef935-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ef935-161">Platné od</span><span class="sxs-lookup"><span data-stu-id="ef935-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="ef935-162">Kategorie</span><span class="sxs-lookup"><span data-stu-id="ef935-162">Category</span></span></p></th>
<th><p><span data-ttu-id="ef935-163">Project</span><span class="sxs-lookup"><span data-stu-id="ef935-163">Project</span></span></p></th>
<th><p><span data-ttu-id="ef935-164">Předplatné</span><span class="sxs-lookup"><span data-stu-id="ef935-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="ef935-165">Kód období</span><span class="sxs-lookup"><span data-stu-id="ef935-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="ef935-166">Prodejní měna</span><span class="sxs-lookup"><span data-stu-id="ef935-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="ef935-167">Prodejní cena</span><span class="sxs-lookup"><span data-stu-id="ef935-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef935-168">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="ef935-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef935-169">9030</span><span class="sxs-lookup"><span data-stu-id="ef935-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef935-170">Měsíc</span><span class="sxs-lookup"><span data-stu-id="ef935-170">Month</span></span></p></td>
<td><p><span data-ttu-id="ef935-171">EUR</span><span class="sxs-lookup"><span data-stu-id="ef935-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="ef935-172">500</span><span class="sxs-lookup"><span data-stu-id="ef935-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef935-173">Pole **Kategorie** a **Předplatné** jsou prázdná.</span><span class="sxs-lookup"><span data-stu-id="ef935-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="ef935-174">Potom vytvoříte následující předplatná.</span><span class="sxs-lookup"><span data-stu-id="ef935-174">You then create the following subscriptions.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ef935-175">Předplatné servisu</span><span class="sxs-lookup"><span data-stu-id="ef935-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="ef935-176">Project</span><span class="sxs-lookup"><span data-stu-id="ef935-176">Project</span></span></p></th>
<th><p><span data-ttu-id="ef935-177">Skupina předplatného</span><span class="sxs-lookup"><span data-stu-id="ef935-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="ef935-178">Kategorie</span><span class="sxs-lookup"><span data-stu-id="ef935-178">Category</span></span></p></th>
<th><p><span data-ttu-id="ef935-179">Měna</span><span class="sxs-lookup"><span data-stu-id="ef935-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="ef935-180">Kód období</span><span class="sxs-lookup"><span data-stu-id="ef935-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef935-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="ef935-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="ef935-182">9030</span><span class="sxs-lookup"><span data-stu-id="ef935-182">9030</span></span></p></td>
<td><p><span data-ttu-id="ef935-183">Předpl.1</span><span class="sxs-lookup"><span data-stu-id="ef935-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="ef935-184">Kateg.předpl.1</span><span class="sxs-lookup"><span data-stu-id="ef935-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="ef935-185">EUR</span><span class="sxs-lookup"><span data-stu-id="ef935-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="ef935-186">Měsíčně</span><span class="sxs-lookup"><span data-stu-id="ef935-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef935-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="ef935-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="ef935-188">9030</span><span class="sxs-lookup"><span data-stu-id="ef935-188">9030</span></span></p></td>
<td><p><span data-ttu-id="ef935-189">Předpl.1</span><span class="sxs-lookup"><span data-stu-id="ef935-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="ef935-190">Kateg.předpl.2</span><span class="sxs-lookup"><span data-stu-id="ef935-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="ef935-191">EUR</span><span class="sxs-lookup"><span data-stu-id="ef935-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="ef935-192">Měsíčně</span><span class="sxs-lookup"><span data-stu-id="ef935-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef935-193">Nyní vytvoříte poplatky předplatného pro obě předplatné ve skupině předplatného Předpl.1:</span><span class="sxs-lookup"><span data-stu-id="ef935-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="ef935-194">Klikněte na uzel **Řízení služeb** \> **Nastavení** \> **Servisní zakázky** \> **Skupiny předplatného**.</span><span class="sxs-lookup"><span data-stu-id="ef935-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="ef935-195">Ve formuláři **skupiny předplatného** klepněte na možnost **funkce** \> **Vytvořit poplatek předplatného**.</span><span class="sxs-lookup"><span data-stu-id="ef935-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="ef935-196">Ve formuláři **Vytvořit poplatek za předplatné** zadejte příslušné informace do polí.</span><span class="sxs-lookup"><span data-stu-id="ef935-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="ef935-197">Další informace o transakcích poplatků naleznete v tématu [Vytvoření transakcí poplatku za předplatné](create-subscription-fee-transactions.md)..</span><span class="sxs-lookup"><span data-stu-id="ef935-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="ef935-198">Pro obě předplatná jsou vytvořeny poplatky předplatného s prodejní cenou 500 EUR, jak je uvedeno v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="ef935-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ef935-199">Datum projektu</span><span class="sxs-lookup"><span data-stu-id="ef935-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="ef935-200">Předplatné servisu</span><span class="sxs-lookup"><span data-stu-id="ef935-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="ef935-201">Project</span><span class="sxs-lookup"><span data-stu-id="ef935-201">Project</span></span></p></th>
<th><p><span data-ttu-id="ef935-202">Kategorie</span><span class="sxs-lookup"><span data-stu-id="ef935-202">Category</span></span></p></th>
<th><p><span data-ttu-id="ef935-203">Datum zahájení</span><span class="sxs-lookup"><span data-stu-id="ef935-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="ef935-204">Koncové datum</span><span class="sxs-lookup"><span data-stu-id="ef935-204">End date</span></span></p></th>
<th><p><span data-ttu-id="ef935-205">Prodejní měna</span><span class="sxs-lookup"><span data-stu-id="ef935-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="ef935-206">Prodejní cena</span><span class="sxs-lookup"><span data-stu-id="ef935-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef935-207">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="ef935-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="ef935-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="ef935-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="ef935-209">9030</span><span class="sxs-lookup"><span data-stu-id="ef935-209">9030</span></span></p></td>
<td><p><span data-ttu-id="ef935-210">Kateg.předpl.1</span><span class="sxs-lookup"><span data-stu-id="ef935-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="ef935-211">1. 1. 2007</span><span class="sxs-lookup"><span data-stu-id="ef935-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="ef935-212">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="ef935-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="ef935-213">EUR</span><span class="sxs-lookup"><span data-stu-id="ef935-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="ef935-214">500</span><span class="sxs-lookup"><span data-stu-id="ef935-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef935-215">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="ef935-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="ef935-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="ef935-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="ef935-217">9030</span><span class="sxs-lookup"><span data-stu-id="ef935-217">9030</span></span></p></td>
<td><p><span data-ttu-id="ef935-218">Kateg.předpl.2</span><span class="sxs-lookup"><span data-stu-id="ef935-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="ef935-219">1. 1. 2007</span><span class="sxs-lookup"><span data-stu-id="ef935-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="ef935-220">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="ef935-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="ef935-221">EUR</span><span class="sxs-lookup"><span data-stu-id="ef935-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="ef935-222">500</span><span class="sxs-lookup"><span data-stu-id="ef935-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef935-223">Později se rozhodnete, že budete chtít zadat prodejní ceny pro kategorii Kateg.předpl.1 pro projekt 9030.</span><span class="sxs-lookup"><span data-stu-id="ef935-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="ef935-224">Proto vytvoříte nový řádek prodejní ceny s prodejní cenou 550 EUR pro kombinaci projektu 9030 a kategorie poplatků Kateg.předpl.1.</span><span class="sxs-lookup"><span data-stu-id="ef935-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="ef935-225">Pro projekt 9030 nyní existují dva řádky prodejní ceny předplatného, jak ukazuje následující tabulka.</span><span class="sxs-lookup"><span data-stu-id="ef935-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ef935-226">Platné od</span><span class="sxs-lookup"><span data-stu-id="ef935-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="ef935-227">Kategorie</span><span class="sxs-lookup"><span data-stu-id="ef935-227">Category</span></span></p></th>
<th><p><span data-ttu-id="ef935-228">Project</span><span class="sxs-lookup"><span data-stu-id="ef935-228">Project</span></span></p></th>
<th><p><span data-ttu-id="ef935-229">Předplatné</span><span class="sxs-lookup"><span data-stu-id="ef935-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="ef935-230">Kód období</span><span class="sxs-lookup"><span data-stu-id="ef935-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="ef935-231">Měna</span><span class="sxs-lookup"><span data-stu-id="ef935-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="ef935-232">Prodejní cena</span><span class="sxs-lookup"><span data-stu-id="ef935-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef935-233">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="ef935-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef935-234">9030</span><span class="sxs-lookup"><span data-stu-id="ef935-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef935-235">Měsíc</span><span class="sxs-lookup"><span data-stu-id="ef935-235">Month</span></span></p></td>
<td><p><span data-ttu-id="ef935-236">EUR</span><span class="sxs-lookup"><span data-stu-id="ef935-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="ef935-237">500</span><span class="sxs-lookup"><span data-stu-id="ef935-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef935-238">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="ef935-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="ef935-239">Kateg.předpl.1</span><span class="sxs-lookup"><span data-stu-id="ef935-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="ef935-240">9030</span><span class="sxs-lookup"><span data-stu-id="ef935-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="ef935-241">Měsíc</span><span class="sxs-lookup"><span data-stu-id="ef935-241">Month</span></span></p></td>
<td><p><span data-ttu-id="ef935-242">EUR</span><span class="sxs-lookup"><span data-stu-id="ef935-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="ef935-243">550</span><span class="sxs-lookup"><span data-stu-id="ef935-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef935-244">Opakováním výše uvedeného postupu vytvoříte poplatky předplatného pro obě předplatné ve skupině předplatného Předpl.1.</span><span class="sxs-lookup"><span data-stu-id="ef935-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="ef935-245">Následující tabulka ukazuje transakce, které jsou vytvořeny pro každé předplatné připojené ke skupině předplatného:</span><span class="sxs-lookup"><span data-stu-id="ef935-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ef935-246">Datum projektu</span><span class="sxs-lookup"><span data-stu-id="ef935-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="ef935-247">Předplatné</span><span class="sxs-lookup"><span data-stu-id="ef935-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="ef935-248">Project</span><span class="sxs-lookup"><span data-stu-id="ef935-248">Project</span></span></p></th>
<th><p><span data-ttu-id="ef935-249">Kategorie</span><span class="sxs-lookup"><span data-stu-id="ef935-249">Category</span></span></p></th>
<th><p><span data-ttu-id="ef935-250">Datum zahájení</span><span class="sxs-lookup"><span data-stu-id="ef935-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="ef935-251">Datum ukončení</span><span class="sxs-lookup"><span data-stu-id="ef935-251">End date</span></span></p></th>
<th><p><span data-ttu-id="ef935-252">Prodejní měna</span><span class="sxs-lookup"><span data-stu-id="ef935-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="ef935-253">Prodejní cena</span><span class="sxs-lookup"><span data-stu-id="ef935-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef935-254">28-07-2007</span><span class="sxs-lookup"><span data-stu-id="ef935-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="ef935-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="ef935-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="ef935-256">9030</span><span class="sxs-lookup"><span data-stu-id="ef935-256">9030</span></span></p></td>
<td><p><span data-ttu-id="ef935-257">Kateg.předpl.1</span><span class="sxs-lookup"><span data-stu-id="ef935-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="ef935-258">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="ef935-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="ef935-259">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="ef935-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="ef935-260">EUR</span><span class="sxs-lookup"><span data-stu-id="ef935-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="ef935-261">550</span><span class="sxs-lookup"><span data-stu-id="ef935-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef935-262">28-07-2008</span><span class="sxs-lookup"><span data-stu-id="ef935-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="ef935-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="ef935-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="ef935-264">9030</span><span class="sxs-lookup"><span data-stu-id="ef935-264">9030</span></span></p></td>
<td><p><span data-ttu-id="ef935-265">Kateg.předpl.2</span><span class="sxs-lookup"><span data-stu-id="ef935-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="ef935-266">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="ef935-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="ef935-267">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="ef935-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="ef935-268">EUR</span><span class="sxs-lookup"><span data-stu-id="ef935-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="ef935-269">500</span><span class="sxs-lookup"><span data-stu-id="ef935-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef935-270">V první transakci pro předplatné 00020\_13 je prodejní cena 550 EUR odvozena od prodejní ceny předplatného nastavené pro kombinaci konkrétního projektu a kategorie.</span><span class="sxs-lookup"><span data-stu-id="ef935-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="ef935-271">Ve druhé transakci pro předplatné 00021\_135 se jako prodejní cena předplatného projektu používá prodejní cena 500 EUR, protože není nastavena cena pro kombinaci projektu 9030 a kategorie Kateg.předpl.2.</span><span class="sxs-lookup"><span data-stu-id="ef935-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="ef935-272">Viz také</span><span class="sxs-lookup"><span data-stu-id="ef935-272">See also</span></span>

[<span data-ttu-id="ef935-273">Aktualizace a indexování prodejních cen předplatného</span><span class="sxs-lookup"><span data-stu-id="ef935-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  



