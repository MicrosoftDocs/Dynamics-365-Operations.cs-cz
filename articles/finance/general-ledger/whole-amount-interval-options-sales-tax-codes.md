---
title: Možnost Celková částka a Interval výpočtu pro kódy DPH
description: Tento článek vysvětluje možnosti pro pole Metoda výpočtu pro kódy DPH, a postup výpočtu DPH v rámci intervalů a celých částek.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3e18eac934eb109e8f3f509b2bd78f76dd5f74d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2020
ms.locfileid: "3980907"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="4bf5f-103">Možnost Celková částka a Interval výpočtu pro kódy DPH</span><span class="sxs-lookup"><span data-stu-id="4bf5f-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4bf5f-104">Tento článek vysvětluje možnosti pro pole Metoda výpočtu pro kódy DPH, a postup výpočtu DPH v rámci intervalů a celých částek.</span><span class="sxs-lookup"><span data-stu-id="4bf5f-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="4bf5f-105">Můžete nastavit kód DPH, aby byl vypočten na základě celé částky nebo částky intervalu.</span><span class="sxs-lookup"><span data-stu-id="4bf5f-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="4bf5f-106">Na stránce Kódy DPH pomocí pole Metoda výpočtu na pevné záložce Výpočet vyberte způsob výpočtu kódu DPH.</span><span class="sxs-lookup"><span data-stu-id="4bf5f-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
- <span data-ttu-id="4bf5f-107">Celá částka – Sazba daně se použije na celou zdanitelnou částku.</span><span class="sxs-lookup"><span data-stu-id="4bf5f-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
- <span data-ttu-id="4bf5f-108">Interval – základ daně je rozdělen do částí, kde každá část spadá do rozsahu, který má konkrétní kurz DPH.</span><span class="sxs-lookup"><span data-stu-id="4bf5f-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="4bf5f-109">Část částky, která spadá do příslušného intervalu, je zdaněna podle sazby daně pro tento interval.</span><span class="sxs-lookup"><span data-stu-id="4bf5f-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="4bf5f-110">Prodejní daň je součtem částek daně, které byly vypočteny pro každou částku intervalu.</span><span class="sxs-lookup"><span data-stu-id="4bf5f-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
  > [!NOTE]                                                                                                                              
  > <span data-ttu-id="4bf5f-111">Možnost Interval je k dispozici pouze při výběru řádku v poli Metoda výpočtu v oblasti DPH na stránce Parametry hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="4bf5f-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="4bf5f-112">Intervaly jsou nastaveny na stránce Hodnoty kódu DPH zadáním minimálního a maximálního limitu částky pro jednotlivé daňové sazby.</span><span class="sxs-lookup"><span data-stu-id="4bf5f-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="4bf5f-113">U daní, které se počítají z jakéhokoli základu, musejí být u intervalů dodržena následující pravidla (bez ohledu na vybranou metodu výpočtu):</span><span class="sxs-lookup"><span data-stu-id="4bf5f-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="4bf5f-114">První interval má dolní mez rovnou 0.</span><span class="sxs-lookup"><span data-stu-id="4bf5f-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="4bf5f-115">Poslední interval má maximální limit 0, což znamená nekonečno.</span><span class="sxs-lookup"><span data-stu-id="4bf5f-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="4bf5f-116">Maximální limit u intervalu musí být minimálním limitem následujícího intervalu.</span><span class="sxs-lookup"><span data-stu-id="4bf5f-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="4bf5f-117">Pokud částka odpovídá horní mezi předchozím intervalem a zároveň dolní mezi dalšího intervalu, použije se pro částku sazby DPH prvního intervalu.</span><span class="sxs-lookup"><span data-stu-id="4bf5f-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="4bf5f-118">Jestliže částka nenáleží do žádného intervalu, které jsou definované dolní a horní mezí, použije se nulová sazba DPH.</span><span class="sxs-lookup"><span data-stu-id="4bf5f-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="4bf5f-119">Příklad: výpočet metodou celkové částky</span><span class="sxs-lookup"><span data-stu-id="4bf5f-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="4bf5f-120">Na stránce Hodnoty kódu DPH jsou sazby DPH nastaveny v následujících intervalech:</span><span class="sxs-lookup"><span data-stu-id="4bf5f-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="4bf5f-121">**Minimální limit**</span><span class="sxs-lookup"><span data-stu-id="4bf5f-121">**Minimum limit**</span></span> | <span data-ttu-id="4bf5f-122">**Maximální limit**</span><span class="sxs-lookup"><span data-stu-id="4bf5f-122">**Maximum limit**</span></span> | <span data-ttu-id="4bf5f-123">**Sazba daně**</span><span class="sxs-lookup"><span data-stu-id="4bf5f-123">**Tax rate**</span></span> |
| <span data-ttu-id="4bf5f-124">0,00</span><span class="sxs-lookup"><span data-stu-id="4bf5f-124">0.00</span></span>              | <span data-ttu-id="4bf5f-125">50,00</span><span class="sxs-lookup"><span data-stu-id="4bf5f-125">50.00</span></span>             | <span data-ttu-id="4bf5f-126">30 %</span><span class="sxs-lookup"><span data-stu-id="4bf5f-126">30%</span></span>          |
| <span data-ttu-id="4bf5f-127">50,00</span><span class="sxs-lookup"><span data-stu-id="4bf5f-127">50.00</span></span>             | <span data-ttu-id="4bf5f-128">100,00</span><span class="sxs-lookup"><span data-stu-id="4bf5f-128">100.00</span></span>            | <span data-ttu-id="4bf5f-129">20 %</span><span class="sxs-lookup"><span data-stu-id="4bf5f-129">20%</span></span>          |
| <span data-ttu-id="4bf5f-130">100,00</span><span class="sxs-lookup"><span data-stu-id="4bf5f-130">100.00</span></span>            | <span data-ttu-id="4bf5f-131">0,00</span><span class="sxs-lookup"><span data-stu-id="4bf5f-131">0.00</span></span>              | <span data-ttu-id="4bf5f-132">10 %</span><span class="sxs-lookup"><span data-stu-id="4bf5f-132">10%</span></span>          |

<span data-ttu-id="4bf5f-133">Prodejní daň bude vypočtena ve výši celé zdanitelné částky.</span><span class="sxs-lookup"><span data-stu-id="4bf5f-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="4bf5f-134">Zdanitelná částka (cena)</span><span class="sxs-lookup"><span data-stu-id="4bf5f-134">Taxable amount (price)</span></span> | <span data-ttu-id="4bf5f-135">Výpočet</span><span class="sxs-lookup"><span data-stu-id="4bf5f-135">Calculation</span></span>    | <span data-ttu-id="4bf5f-136">DPH</span><span class="sxs-lookup"><span data-stu-id="4bf5f-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="4bf5f-137">35,00</span><span class="sxs-lookup"><span data-stu-id="4bf5f-137">35.00</span></span>                  | <span data-ttu-id="4bf5f-138">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="4bf5f-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="4bf5f-139">10.50</span><span class="sxs-lookup"><span data-stu-id="4bf5f-139">10.50</span></span>     |
| <span data-ttu-id="4bf5f-140">50,00</span><span class="sxs-lookup"><span data-stu-id="4bf5f-140">50.00</span></span>                  | <span data-ttu-id="4bf5f-141">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="4bf5f-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="4bf5f-142">15:00</span><span class="sxs-lookup"><span data-stu-id="4bf5f-142">15.00</span></span>     |
| <span data-ttu-id="4bf5f-143">85,00</span><span class="sxs-lookup"><span data-stu-id="4bf5f-143">85.00</span></span>                  | <span data-ttu-id="4bf5f-144">85,00 \* 0,20</span><span class="sxs-lookup"><span data-stu-id="4bf5f-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="4bf5f-145">17,00</span><span class="sxs-lookup"><span data-stu-id="4bf5f-145">17.00</span></span>     |
| <span data-ttu-id="4bf5f-146">305,00</span><span class="sxs-lookup"><span data-stu-id="4bf5f-146">305.00</span></span>                 | <span data-ttu-id="4bf5f-147">305,00 \* 0,10</span><span class="sxs-lookup"><span data-stu-id="4bf5f-147">305.00 \* 0.10</span></span> | <span data-ttu-id="4bf5f-148">30,50</span><span class="sxs-lookup"><span data-stu-id="4bf5f-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="4bf5f-149"> Příklad: výpočet metodou intervalu</span><span class="sxs-lookup"><span data-stu-id="4bf5f-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="4bf5f-150">Na stránce Hodnoty jsou sazby DPH nastaveny v následujících intervalech:</span><span class="sxs-lookup"><span data-stu-id="4bf5f-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="4bf5f-151">**Minimální limit**</span><span class="sxs-lookup"><span data-stu-id="4bf5f-151">**Minimum limit**</span></span> | <span data-ttu-id="4bf5f-152">**Maximální limit**</span><span class="sxs-lookup"><span data-stu-id="4bf5f-152">**Maximum limit**</span></span> | <span data-ttu-id="4bf5f-153">**Sazba daně**</span><span class="sxs-lookup"><span data-stu-id="4bf5f-153">**Tax rate**</span></span> |
| <span data-ttu-id="4bf5f-154">0,00</span><span class="sxs-lookup"><span data-stu-id="4bf5f-154">0.00</span></span>              | <span data-ttu-id="4bf5f-155">50,00</span><span class="sxs-lookup"><span data-stu-id="4bf5f-155">50.00</span></span>             | <span data-ttu-id="4bf5f-156">30 %</span><span class="sxs-lookup"><span data-stu-id="4bf5f-156">30%</span></span>          |
| <span data-ttu-id="4bf5f-157">50,00</span><span class="sxs-lookup"><span data-stu-id="4bf5f-157">50.00</span></span>             | <span data-ttu-id="4bf5f-158">100,00</span><span class="sxs-lookup"><span data-stu-id="4bf5f-158">100.00</span></span>            | <span data-ttu-id="4bf5f-159">20 %</span><span class="sxs-lookup"><span data-stu-id="4bf5f-159">20%</span></span>          |
| <span data-ttu-id="4bf5f-160">100,00</span><span class="sxs-lookup"><span data-stu-id="4bf5f-160">100.00</span></span>            | <span data-ttu-id="4bf5f-161">0,00</span><span class="sxs-lookup"><span data-stu-id="4bf5f-161">0.00</span></span>              | <span data-ttu-id="4bf5f-162">10 %</span><span class="sxs-lookup"><span data-stu-id="4bf5f-162">10%</span></span>          |

<span data-ttu-id="4bf5f-163">Prodejní daň je součtem částek daně, které byly vypočteny pro každou částku intervalu.</span><span class="sxs-lookup"><span data-stu-id="4bf5f-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="4bf5f-164">Zdanitelná částka (cena)</span><span class="sxs-lookup"><span data-stu-id="4bf5f-164">Taxable amount (price)</span></span> | <span data-ttu-id="4bf5f-165">Výpočet</span><span class="sxs-lookup"><span data-stu-id="4bf5f-165">Calculation</span></span>                                                               | <span data-ttu-id="4bf5f-166">DPH</span><span class="sxs-lookup"><span data-stu-id="4bf5f-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="4bf5f-167">35,00</span><span class="sxs-lookup"><span data-stu-id="4bf5f-167">35.00</span></span>                  | <span data-ttu-id="4bf5f-168">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="4bf5f-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="4bf5f-169">10.50</span><span class="sxs-lookup"><span data-stu-id="4bf5f-169">10.50</span></span>     |
| <span data-ttu-id="4bf5f-170">50,00</span><span class="sxs-lookup"><span data-stu-id="4bf5f-170">50.00</span></span>                  | <span data-ttu-id="4bf5f-171">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="4bf5f-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="4bf5f-172">15:00</span><span class="sxs-lookup"><span data-stu-id="4bf5f-172">15.00</span></span>     |
| <span data-ttu-id="4bf5f-173">85,00</span><span class="sxs-lookup"><span data-stu-id="4bf5f-173">85.00</span></span>                  | <span data-ttu-id="4bf5f-174">(50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)</span><span class="sxs-lookup"><span data-stu-id="4bf5f-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="4bf5f-175">22,00</span><span class="sxs-lookup"><span data-stu-id="4bf5f-175">22.00</span></span>     |
| <span data-ttu-id="4bf5f-176">305,00</span><span class="sxs-lookup"><span data-stu-id="4bf5f-176">305.00</span></span>                 | <span data-ttu-id="4bf5f-177">(50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50)</span><span class="sxs-lookup"><span data-stu-id="4bf5f-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="4bf5f-178">45.50</span><span class="sxs-lookup"><span data-stu-id="4bf5f-178">45.50</span></span>     |



<span data-ttu-id="4bf5f-179">Více informací najdete v části [Sazby DPH na základě polí Základ marže a Metody výpočtu](marginal-base-field.md).</span><span class="sxs-lookup"><span data-stu-id="4bf5f-179">For more information, see [Sales tax rates based on the Marginal base and Calculation methods](marginal-base-field.md).</span></span>





