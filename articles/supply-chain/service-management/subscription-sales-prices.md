---
title: Prodejní cena předplatného
description: Při vytváření předplatného je prodejní cena odvozena od nastavení prodejní ceny vytvořené ve formuláři Prodejní cena (předplatné).
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d6c59c90d49a4dcf3df4672c5f40d52ed639760c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206604"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="1a5e3-103">Prodejní cena předplatného</span><span class="sxs-lookup"><span data-stu-id="1a5e3-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="1a5e3-104">Při vytváření předplatného je prodejní cena odvozena od nastavení prodejní ceny vytvořené ve formuláři **Prodejní cena (předplatné)**.</span><span class="sxs-lookup"><span data-stu-id="1a5e3-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="1a5e3-105">Ve formuláři **Prodejní cena (předplatné)** můžete vytvořit prodejní ceny pro konkrétní předplatné nebo můžete vytvořit obecněji platné prodejní ceny.</span><span class="sxs-lookup"><span data-stu-id="1a5e3-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="1a5e3-106">Aby byla prodejní cena u předplatného použita, musí být kód období a měna předplatného a prodejní stejný jako kód období a měna prodejní ceny.</span><span class="sxs-lookup"><span data-stu-id="1a5e3-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="1a5e3-107">Jestliže jsou kód období a měna pro předplatné i pro prodejní cenu identické, jsou prodejní ceny předplatného vybírány na základě priorit uvedených v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="1a5e3-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="1a5e3-108">Prázdná buňka v tabulce označuje prázdné pole a X označuje, že je hodnota rovna hodnotě předplatného, ze které je transakce generována.</span><span class="sxs-lookup"><span data-stu-id="1a5e3-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

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
<th><p><span data-ttu-id="1a5e3-109">Priorita </span><span class="sxs-lookup"><span data-stu-id="1a5e3-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-110"><strong>Kategorie</strong></span><span class="sxs-lookup"><span data-stu-id="1a5e3-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="1a5e3-111"><strong>ID projektu</strong></span><span class="sxs-lookup"><span data-stu-id="1a5e3-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="1a5e3-112"><strong>Předplatné</strong></span><span class="sxs-lookup"><span data-stu-id="1a5e3-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="1a5e3-113"><strong>Měna prodeje</strong></span><span class="sxs-lookup"><span data-stu-id="1a5e3-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="1a5e3-114"><strong>Kód období</strong></span><span class="sxs-lookup"><span data-stu-id="1a5e3-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a5e3-115">1</span><span class="sxs-lookup"><span data-stu-id="1a5e3-115">1</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-116">X</span><span class="sxs-lookup"><span data-stu-id="1a5e3-116">X</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-117">X</span><span class="sxs-lookup"><span data-stu-id="1a5e3-117">X</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-118">X</span><span class="sxs-lookup"><span data-stu-id="1a5e3-118">X</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-119">X</span><span class="sxs-lookup"><span data-stu-id="1a5e3-119">X</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-120">X</span><span class="sxs-lookup"><span data-stu-id="1a5e3-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a5e3-121">2</span><span class="sxs-lookup"><span data-stu-id="1a5e3-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="1a5e3-122">X</span><span class="sxs-lookup"><span data-stu-id="1a5e3-122">X</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-123">X</span><span class="sxs-lookup"><span data-stu-id="1a5e3-123">X</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-124">X</span><span class="sxs-lookup"><span data-stu-id="1a5e3-124">X</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-125">X</span><span class="sxs-lookup"><span data-stu-id="1a5e3-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a5e3-126">3</span><span class="sxs-lookup"><span data-stu-id="1a5e3-126">3</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-127">X</span><span class="sxs-lookup"><span data-stu-id="1a5e3-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="1a5e3-128">X</span><span class="sxs-lookup"><span data-stu-id="1a5e3-128">X</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-129">X</span><span class="sxs-lookup"><span data-stu-id="1a5e3-129">X</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-130">X</span><span class="sxs-lookup"><span data-stu-id="1a5e3-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a5e3-131">4</span><span class="sxs-lookup"><span data-stu-id="1a5e3-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="1a5e3-132">X</span><span class="sxs-lookup"><span data-stu-id="1a5e3-132">X</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-133">X</span><span class="sxs-lookup"><span data-stu-id="1a5e3-133">X</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-134">X</span><span class="sxs-lookup"><span data-stu-id="1a5e3-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a5e3-135">5</span><span class="sxs-lookup"><span data-stu-id="1a5e3-135">5</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-136">X</span><span class="sxs-lookup"><span data-stu-id="1a5e3-136">X</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-137">X</span><span class="sxs-lookup"><span data-stu-id="1a5e3-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="1a5e3-138">X</span><span class="sxs-lookup"><span data-stu-id="1a5e3-138">X</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-139">X</span><span class="sxs-lookup"><span data-stu-id="1a5e3-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a5e3-140">6</span><span class="sxs-lookup"><span data-stu-id="1a5e3-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="1a5e3-141">X</span><span class="sxs-lookup"><span data-stu-id="1a5e3-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="1a5e3-142">X</span><span class="sxs-lookup"><span data-stu-id="1a5e3-142">X</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-143">X</span><span class="sxs-lookup"><span data-stu-id="1a5e3-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a5e3-144">7</span><span class="sxs-lookup"><span data-stu-id="1a5e3-144">7</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-145">X</span><span class="sxs-lookup"><span data-stu-id="1a5e3-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="1a5e3-146">X</span><span class="sxs-lookup"><span data-stu-id="1a5e3-146">X</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-147">X</span><span class="sxs-lookup"><span data-stu-id="1a5e3-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a5e3-148">8</span><span class="sxs-lookup"><span data-stu-id="1a5e3-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="1a5e3-149">X</span><span class="sxs-lookup"><span data-stu-id="1a5e3-149">X</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-150">X</span><span class="sxs-lookup"><span data-stu-id="1a5e3-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1a5e3-151">Pokud je vytvořen poplatek předplatného, je jako prodejní cena předplatného vybrána prodejní cena s nejvyšší úrovní podrobností, jak je uvedeno v předchozí tabulce.</span><span class="sxs-lookup"><span data-stu-id="1a5e3-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="1a5e3-152">Aktualizace a indexování prodejních cen předplatného</span><span class="sxs-lookup"><span data-stu-id="1a5e3-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="1a5e3-153">Prodejní cenu předplatného můžete aktualizovat aktualizováním základní ceny nebo indexu.</span><span class="sxs-lookup"><span data-stu-id="1a5e3-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="1a5e3-154">Aktualizovat lze o procentuální hodnotu nebo na novou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1a5e3-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="1a5e3-155">Prodejní ceny poplatků předplatného</span><span class="sxs-lookup"><span data-stu-id="1a5e3-155">Subscription fee sales prices</span></span>

<span data-ttu-id="1a5e3-156">Při vytváření poplatku odběru je prodejní cena založena na nastavení prodejní ceny předplatného.</span><span class="sxs-lookup"><span data-stu-id="1a5e3-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="1a5e3-157">Můžete buď použít základní cenu z nastavení ceny předplatného, nebo vytvořit indexované prodejní ceny.</span><span class="sxs-lookup"><span data-stu-id="1a5e3-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="1a5e3-158">Příklad</span><span class="sxs-lookup"><span data-stu-id="1a5e3-158">Example</span></span>

<span data-ttu-id="1a5e3-159">Chcete nastavit prodejní ceny předplatného na 500 EUR pro nový projekt 9030.</span><span class="sxs-lookup"><span data-stu-id="1a5e3-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="1a5e3-160">Ve formuláři **prodejní cena (předplatné)** vytvoříte řádek prodejní ceny předplatného podle návodu v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="1a5e3-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

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
<th><p><span data-ttu-id="1a5e3-161">Platné od</span><span class="sxs-lookup"><span data-stu-id="1a5e3-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-162">Kategorie</span><span class="sxs-lookup"><span data-stu-id="1a5e3-162">Category</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-163">Project</span><span class="sxs-lookup"><span data-stu-id="1a5e3-163">Project</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-164">Předplatné</span><span class="sxs-lookup"><span data-stu-id="1a5e3-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-165">Kód období</span><span class="sxs-lookup"><span data-stu-id="1a5e3-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-166">Prodejní měna</span><span class="sxs-lookup"><span data-stu-id="1a5e3-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-167">Prodejní cena</span><span class="sxs-lookup"><span data-stu-id="1a5e3-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a5e3-168">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="1a5e3-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1a5e3-169">9030</span><span class="sxs-lookup"><span data-stu-id="1a5e3-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1a5e3-170">Měsíc</span><span class="sxs-lookup"><span data-stu-id="1a5e3-170">Month</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-171">EUR</span><span class="sxs-lookup"><span data-stu-id="1a5e3-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-172">500</span><span class="sxs-lookup"><span data-stu-id="1a5e3-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1a5e3-173">Pole **Kategorie** a **Předplatné** jsou prázdná.</span><span class="sxs-lookup"><span data-stu-id="1a5e3-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="1a5e3-174">Potom vytvoříte následující předplatná.</span><span class="sxs-lookup"><span data-stu-id="1a5e3-174">You then create the following subscriptions.</span></span>

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
<th><p><span data-ttu-id="1a5e3-175">Předplatné servisu</span><span class="sxs-lookup"><span data-stu-id="1a5e3-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-176">Project</span><span class="sxs-lookup"><span data-stu-id="1a5e3-176">Project</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-177">Skupina předplatného</span><span class="sxs-lookup"><span data-stu-id="1a5e3-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-178">Kategorie</span><span class="sxs-lookup"><span data-stu-id="1a5e3-178">Category</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-179">Měna</span><span class="sxs-lookup"><span data-stu-id="1a5e3-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-180">Kód období</span><span class="sxs-lookup"><span data-stu-id="1a5e3-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a5e3-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="1a5e3-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-182">9030</span><span class="sxs-lookup"><span data-stu-id="1a5e3-182">9030</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-183">Předpl.1</span><span class="sxs-lookup"><span data-stu-id="1a5e3-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-184">Kateg.předpl.1</span><span class="sxs-lookup"><span data-stu-id="1a5e3-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-185">EUR</span><span class="sxs-lookup"><span data-stu-id="1a5e3-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-186">Měsíčně</span><span class="sxs-lookup"><span data-stu-id="1a5e3-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a5e3-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="1a5e3-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-188">9030</span><span class="sxs-lookup"><span data-stu-id="1a5e3-188">9030</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-189">Předpl.1</span><span class="sxs-lookup"><span data-stu-id="1a5e3-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-190">Kateg.předpl.2</span><span class="sxs-lookup"><span data-stu-id="1a5e3-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-191">EUR</span><span class="sxs-lookup"><span data-stu-id="1a5e3-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-192">Měsíčně</span><span class="sxs-lookup"><span data-stu-id="1a5e3-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1a5e3-193">Nyní vytvoříte poplatky předplatného pro obě předplatné ve skupině předplatného Předpl.1:</span><span class="sxs-lookup"><span data-stu-id="1a5e3-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="1a5e3-194">Klikněte na uzel **Řízení služeb** \> **Nastavení** \> **Servisní zakázky** \> **Skupiny předplatného**.</span><span class="sxs-lookup"><span data-stu-id="1a5e3-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="1a5e3-195">Ve formuláři **skupiny předplatného** klepněte na možnost **funkce** \> **Vytvořit poplatek předplatného**.</span><span class="sxs-lookup"><span data-stu-id="1a5e3-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="1a5e3-196">Ve formuláři **Vytvořit poplatek za předplatné** zadejte příslušné informace do polí.</span><span class="sxs-lookup"><span data-stu-id="1a5e3-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="1a5e3-197">Další informace o transakcích poplatků naleznete v tématu [Vytvoření transakcí poplatku za předplatné](create-subscription-fee-transactions.md)..</span><span class="sxs-lookup"><span data-stu-id="1a5e3-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="1a5e3-198">Pro obě předplatná jsou vytvořeny poplatky předplatného s prodejní cenou 500 EUR, jak je uvedeno v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="1a5e3-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="1a5e3-199">Datum projektu</span><span class="sxs-lookup"><span data-stu-id="1a5e3-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-200">Předplatné servisu</span><span class="sxs-lookup"><span data-stu-id="1a5e3-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-201">Project</span><span class="sxs-lookup"><span data-stu-id="1a5e3-201">Project</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-202">Kategorie</span><span class="sxs-lookup"><span data-stu-id="1a5e3-202">Category</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-203">Datum zahájení</span><span class="sxs-lookup"><span data-stu-id="1a5e3-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-204">Koncové datum</span><span class="sxs-lookup"><span data-stu-id="1a5e3-204">End date</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-205">Prodejní měna</span><span class="sxs-lookup"><span data-stu-id="1a5e3-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-206">Prodejní cena</span><span class="sxs-lookup"><span data-stu-id="1a5e3-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a5e3-207">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="1a5e3-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="1a5e3-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-209">9030</span><span class="sxs-lookup"><span data-stu-id="1a5e3-209">9030</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-210">Kateg.předpl.1</span><span class="sxs-lookup"><span data-stu-id="1a5e3-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-211">1. 1. 2007</span><span class="sxs-lookup"><span data-stu-id="1a5e3-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-212">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="1a5e3-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-213">EUR</span><span class="sxs-lookup"><span data-stu-id="1a5e3-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-214">500</span><span class="sxs-lookup"><span data-stu-id="1a5e3-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a5e3-215">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="1a5e3-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="1a5e3-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-217">9030</span><span class="sxs-lookup"><span data-stu-id="1a5e3-217">9030</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-218">Kateg.předpl.2</span><span class="sxs-lookup"><span data-stu-id="1a5e3-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-219">1. 1. 2007</span><span class="sxs-lookup"><span data-stu-id="1a5e3-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-220">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="1a5e3-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-221">EUR</span><span class="sxs-lookup"><span data-stu-id="1a5e3-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-222">500</span><span class="sxs-lookup"><span data-stu-id="1a5e3-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1a5e3-223">Později se rozhodnete, že budete chtít zadat prodejní ceny pro kategorii Kateg.předpl.1 pro projekt 9030.</span><span class="sxs-lookup"><span data-stu-id="1a5e3-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="1a5e3-224">Proto vytvoříte nový řádek prodejní ceny s prodejní cenou 550 EUR pro kombinaci projektu 9030 a kategorie poplatků Kateg.předpl.1.</span><span class="sxs-lookup"><span data-stu-id="1a5e3-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="1a5e3-225">Pro projekt 9030 nyní existují dva řádky prodejní ceny předplatného, jak ukazuje následující tabulka.</span><span class="sxs-lookup"><span data-stu-id="1a5e3-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="1a5e3-226">Platné od</span><span class="sxs-lookup"><span data-stu-id="1a5e3-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-227">Kategorie</span><span class="sxs-lookup"><span data-stu-id="1a5e3-227">Category</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-228">Project</span><span class="sxs-lookup"><span data-stu-id="1a5e3-228">Project</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-229">Předplatné</span><span class="sxs-lookup"><span data-stu-id="1a5e3-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-230">Kód období</span><span class="sxs-lookup"><span data-stu-id="1a5e3-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-231">Měna</span><span class="sxs-lookup"><span data-stu-id="1a5e3-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-232">Prodejní cena</span><span class="sxs-lookup"><span data-stu-id="1a5e3-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a5e3-233">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="1a5e3-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1a5e3-234">9030</span><span class="sxs-lookup"><span data-stu-id="1a5e3-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1a5e3-235">Měsíc</span><span class="sxs-lookup"><span data-stu-id="1a5e3-235">Month</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-236">EUR</span><span class="sxs-lookup"><span data-stu-id="1a5e3-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-237">500</span><span class="sxs-lookup"><span data-stu-id="1a5e3-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a5e3-238">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="1a5e3-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-239">Kateg.předpl.1</span><span class="sxs-lookup"><span data-stu-id="1a5e3-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-240">9030</span><span class="sxs-lookup"><span data-stu-id="1a5e3-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1a5e3-241">Měsíc</span><span class="sxs-lookup"><span data-stu-id="1a5e3-241">Month</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-242">EUR</span><span class="sxs-lookup"><span data-stu-id="1a5e3-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-243">550</span><span class="sxs-lookup"><span data-stu-id="1a5e3-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1a5e3-244">Opakováním výše uvedeného postupu vytvoříte poplatky předplatného pro obě předplatné ve skupině předplatného Předpl.1.</span><span class="sxs-lookup"><span data-stu-id="1a5e3-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="1a5e3-245">Následující tabulka ukazuje transakce, které jsou vytvořeny pro každé předplatné připojené ke skupině předplatného:</span><span class="sxs-lookup"><span data-stu-id="1a5e3-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

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
<th><p><span data-ttu-id="1a5e3-246">Datum projektu</span><span class="sxs-lookup"><span data-stu-id="1a5e3-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-247">Předplatné</span><span class="sxs-lookup"><span data-stu-id="1a5e3-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-248">Project</span><span class="sxs-lookup"><span data-stu-id="1a5e3-248">Project</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-249">Kategorie</span><span class="sxs-lookup"><span data-stu-id="1a5e3-249">Category</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-250">Datum zahájení</span><span class="sxs-lookup"><span data-stu-id="1a5e3-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-251">Datum ukončení</span><span class="sxs-lookup"><span data-stu-id="1a5e3-251">End date</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-252">Prodejní měna</span><span class="sxs-lookup"><span data-stu-id="1a5e3-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="1a5e3-253">Prodejní cena</span><span class="sxs-lookup"><span data-stu-id="1a5e3-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a5e3-254">28-07-2007</span><span class="sxs-lookup"><span data-stu-id="1a5e3-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="1a5e3-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-256">9030</span><span class="sxs-lookup"><span data-stu-id="1a5e3-256">9030</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-257">Kateg.předpl.1</span><span class="sxs-lookup"><span data-stu-id="1a5e3-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-258">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="1a5e3-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-259">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="1a5e3-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-260">EUR</span><span class="sxs-lookup"><span data-stu-id="1a5e3-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-261">550</span><span class="sxs-lookup"><span data-stu-id="1a5e3-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a5e3-262">28-07-2008</span><span class="sxs-lookup"><span data-stu-id="1a5e3-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="1a5e3-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-264">9030</span><span class="sxs-lookup"><span data-stu-id="1a5e3-264">9030</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-265">Kateg.předpl.2</span><span class="sxs-lookup"><span data-stu-id="1a5e3-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-266">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="1a5e3-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-267">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="1a5e3-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-268">EUR</span><span class="sxs-lookup"><span data-stu-id="1a5e3-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="1a5e3-269">500</span><span class="sxs-lookup"><span data-stu-id="1a5e3-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1a5e3-270">V první transakci pro předplatné 00020\_13 je prodejní cena 550 EUR odvozena od prodejní ceny předplatného nastavené pro kombinaci konkrétního projektu a kategorie.</span><span class="sxs-lookup"><span data-stu-id="1a5e3-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="1a5e3-271">Ve druhé transakci pro předplatné 00021\_135 se jako prodejní cena předplatného projektu používá prodejní cena 500 EUR, protože není nastavena cena pro kombinaci projektu 9030 a kategorie Kateg.předpl.2.</span><span class="sxs-lookup"><span data-stu-id="1a5e3-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a5e3-272">Viz také</span><span class="sxs-lookup"><span data-stu-id="1a5e3-272">See also</span></span>

[<span data-ttu-id="1a5e3-273">Aktualizace a indexování prodejních cen předplatného</span><span class="sxs-lookup"><span data-stu-id="1a5e3-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  


