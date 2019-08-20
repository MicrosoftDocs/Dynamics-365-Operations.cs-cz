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
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb737e6600b1812c44d6101814fc858ac27013e9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834626"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="c010f-103">Možnost Celková částka a Interval výpočtu pro kódy DPH</span><span class="sxs-lookup"><span data-stu-id="c010f-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="c010f-104">Tento článek vysvětluje možnosti pro pole Metoda výpočtu pro kódy DPH, a postup výpočtu DPH v rámci intervalů a celých částek.</span><span class="sxs-lookup"><span data-stu-id="c010f-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="c010f-105">Můžete nastavit kód DPH, aby byl vypočten na základě celé částky nebo částky intervalu.</span><span class="sxs-lookup"><span data-stu-id="c010f-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="c010f-106">Na stránce Kódy DPH pomocí pole Metoda výpočtu na pevné záložce Výpočet vyberte způsob výpočtu kódu DPH.</span><span class="sxs-lookup"><span data-stu-id="c010f-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
- <span data-ttu-id="c010f-107">Celá částka – Sazba daně se použije na celou zdanitelnou částku.</span><span class="sxs-lookup"><span data-stu-id="c010f-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
- <span data-ttu-id="c010f-108">Interval – základ daně je rozdělen do částí, kde každá část spadá do rozsahu, který má konkrétní kurz DPH.</span><span class="sxs-lookup"><span data-stu-id="c010f-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="c010f-109">Část částky, která spadá do příslušného intervalu, je zdaněna podle sazby daně pro tento interval.</span><span class="sxs-lookup"><span data-stu-id="c010f-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="c010f-110">Prodejní daň je součtem částek daně, které byly vypočteny pro každou částku intervalu.</span><span class="sxs-lookup"><span data-stu-id="c010f-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
  > [!NOTE]                                                                                                                              
  > <span data-ttu-id="c010f-111">Možnost Interval je k dispozici pouze při výběru řádku v poli Metoda výpočtu v oblasti DPH na stránce Parametry hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="c010f-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="c010f-112">Intervaly jsou nastaveny na stránce Hodnoty kódu DPH zadáním minimálního a maximálního limitu částky pro jednotlivé daňové sazby.</span><span class="sxs-lookup"><span data-stu-id="c010f-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="c010f-113">U daní, které se počítají z jakéhokoli základu, musejí být u intervalů dodržena následující pravidla (bez ohledu na vybranou metodu výpočtu):</span><span class="sxs-lookup"><span data-stu-id="c010f-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="c010f-114">První interval má dolní mez rovnou 0.</span><span class="sxs-lookup"><span data-stu-id="c010f-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="c010f-115">Poslední interval má maximální limit 0, což znamená nekonečno.</span><span class="sxs-lookup"><span data-stu-id="c010f-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="c010f-116">Maximální limit u intervalu musí být minimálním limitem následujícího intervalu.</span><span class="sxs-lookup"><span data-stu-id="c010f-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="c010f-117">Pokud částka odpovídá horní mezi předchozím intervalem a zároveň dolní mezi dalšího intervalu, použije se pro částku sazby DPH prvního intervalu.</span><span class="sxs-lookup"><span data-stu-id="c010f-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="c010f-118">Jestliže částka nenáleží do žádného intervalu, které jsou definované dolní a horní mezí, použije se nulová sazba DPH.</span><span class="sxs-lookup"><span data-stu-id="c010f-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="c010f-119">Příklad: výpočet metodou celkové částky</span><span class="sxs-lookup"><span data-stu-id="c010f-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="c010f-120">Na stránce Hodnoty kódu DPH jsou sazby DPH nastaveny v následujících intervalech:</span><span class="sxs-lookup"><span data-stu-id="c010f-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="c010f-121">**Minimální limit**</span><span class="sxs-lookup"><span data-stu-id="c010f-121">**Minimum limit**</span></span> | <span data-ttu-id="c010f-122">**Maximální limit**</span><span class="sxs-lookup"><span data-stu-id="c010f-122">**Maximum limit**</span></span> | <span data-ttu-id="c010f-123">**Sazba daně**</span><span class="sxs-lookup"><span data-stu-id="c010f-123">**Tax rate**</span></span> |
| <span data-ttu-id="c010f-124">0,00</span><span class="sxs-lookup"><span data-stu-id="c010f-124">0.00</span></span>              | <span data-ttu-id="c010f-125">50,00</span><span class="sxs-lookup"><span data-stu-id="c010f-125">50.00</span></span>             | <span data-ttu-id="c010f-126">30 %</span><span class="sxs-lookup"><span data-stu-id="c010f-126">30%</span></span>          |
| <span data-ttu-id="c010f-127">50,00</span><span class="sxs-lookup"><span data-stu-id="c010f-127">50.00</span></span>             | <span data-ttu-id="c010f-128">100,00</span><span class="sxs-lookup"><span data-stu-id="c010f-128">100.00</span></span>            | <span data-ttu-id="c010f-129">20 %</span><span class="sxs-lookup"><span data-stu-id="c010f-129">20%</span></span>          |
| <span data-ttu-id="c010f-130">100,00</span><span class="sxs-lookup"><span data-stu-id="c010f-130">100.00</span></span>            | <span data-ttu-id="c010f-131">0,00</span><span class="sxs-lookup"><span data-stu-id="c010f-131">0.00</span></span>              | <span data-ttu-id="c010f-132">10 %</span><span class="sxs-lookup"><span data-stu-id="c010f-132">10%</span></span>          |

<span data-ttu-id="c010f-133">Prodejní daň bude vypočtena ve výši celé zdanitelné částky.</span><span class="sxs-lookup"><span data-stu-id="c010f-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="c010f-134">Zdanitelná částka (cena)</span><span class="sxs-lookup"><span data-stu-id="c010f-134">Taxable amount (price)</span></span> | <span data-ttu-id="c010f-135">Výpočet</span><span class="sxs-lookup"><span data-stu-id="c010f-135">Calculation</span></span>    | <span data-ttu-id="c010f-136">DPH</span><span class="sxs-lookup"><span data-stu-id="c010f-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="c010f-137">35,00</span><span class="sxs-lookup"><span data-stu-id="c010f-137">35.00</span></span>                  | <span data-ttu-id="c010f-138">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="c010f-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="c010f-139">10.50</span><span class="sxs-lookup"><span data-stu-id="c010f-139">10.50</span></span>     |
| <span data-ttu-id="c010f-140">50,00</span><span class="sxs-lookup"><span data-stu-id="c010f-140">50.00</span></span>                  | <span data-ttu-id="c010f-141">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="c010f-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="c010f-142">15:00</span><span class="sxs-lookup"><span data-stu-id="c010f-142">15.00</span></span>     |
| <span data-ttu-id="c010f-143">85,00</span><span class="sxs-lookup"><span data-stu-id="c010f-143">85.00</span></span>                  | <span data-ttu-id="c010f-144">85,00 \* 0,20</span><span class="sxs-lookup"><span data-stu-id="c010f-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="c010f-145">17,00</span><span class="sxs-lookup"><span data-stu-id="c010f-145">17.00</span></span>     |
| <span data-ttu-id="c010f-146">305,00</span><span class="sxs-lookup"><span data-stu-id="c010f-146">305.00</span></span>                 | <span data-ttu-id="c010f-147">305,00 \* 0,10</span><span class="sxs-lookup"><span data-stu-id="c010f-147">305.00 \* 0.10</span></span> | <span data-ttu-id="c010f-148">30,50</span><span class="sxs-lookup"><span data-stu-id="c010f-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="c010f-149"> Příklad: výpočet metodou intervalu</span><span class="sxs-lookup"><span data-stu-id="c010f-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="c010f-150">Na stránce Hodnoty jsou sazby DPH nastaveny v následujících intervalech:</span><span class="sxs-lookup"><span data-stu-id="c010f-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="c010f-151">**Minimální limit**</span><span class="sxs-lookup"><span data-stu-id="c010f-151">**Minimum limit**</span></span> | <span data-ttu-id="c010f-152">**Maximální limit**</span><span class="sxs-lookup"><span data-stu-id="c010f-152">**Maximum limit**</span></span> | <span data-ttu-id="c010f-153">**Sazba daně**</span><span class="sxs-lookup"><span data-stu-id="c010f-153">**Tax rate**</span></span> |
| <span data-ttu-id="c010f-154">0,00</span><span class="sxs-lookup"><span data-stu-id="c010f-154">0.00</span></span>              | <span data-ttu-id="c010f-155">50,00</span><span class="sxs-lookup"><span data-stu-id="c010f-155">50.00</span></span>             | <span data-ttu-id="c010f-156">30 %</span><span class="sxs-lookup"><span data-stu-id="c010f-156">30%</span></span>          |
| <span data-ttu-id="c010f-157">50,00</span><span class="sxs-lookup"><span data-stu-id="c010f-157">50.00</span></span>             | <span data-ttu-id="c010f-158">100,00</span><span class="sxs-lookup"><span data-stu-id="c010f-158">100.00</span></span>            | <span data-ttu-id="c010f-159">20 %</span><span class="sxs-lookup"><span data-stu-id="c010f-159">20%</span></span>          |
| <span data-ttu-id="c010f-160">100,00</span><span class="sxs-lookup"><span data-stu-id="c010f-160">100.00</span></span>            | <span data-ttu-id="c010f-161">0,00</span><span class="sxs-lookup"><span data-stu-id="c010f-161">0.00</span></span>              | <span data-ttu-id="c010f-162">10 %</span><span class="sxs-lookup"><span data-stu-id="c010f-162">10%</span></span>          |

<span data-ttu-id="c010f-163">Prodejní daň je součtem částek daně, které byly vypočteny pro každou částku intervalu.</span><span class="sxs-lookup"><span data-stu-id="c010f-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="c010f-164">Zdanitelná částka (cena)</span><span class="sxs-lookup"><span data-stu-id="c010f-164">Taxable amount (price)</span></span> | <span data-ttu-id="c010f-165">Výpočet</span><span class="sxs-lookup"><span data-stu-id="c010f-165">Calculation</span></span>                                                               | <span data-ttu-id="c010f-166">DPH</span><span class="sxs-lookup"><span data-stu-id="c010f-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="c010f-167">35,00</span><span class="sxs-lookup"><span data-stu-id="c010f-167">35.00</span></span>                  | <span data-ttu-id="c010f-168">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="c010f-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="c010f-169">10.50</span><span class="sxs-lookup"><span data-stu-id="c010f-169">10.50</span></span>     |
| <span data-ttu-id="c010f-170">50,00</span><span class="sxs-lookup"><span data-stu-id="c010f-170">50.00</span></span>                  | <span data-ttu-id="c010f-171">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="c010f-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="c010f-172">15:00</span><span class="sxs-lookup"><span data-stu-id="c010f-172">15.00</span></span>     |
| <span data-ttu-id="c010f-173">85,00</span><span class="sxs-lookup"><span data-stu-id="c010f-173">85.00</span></span>                  | <span data-ttu-id="c010f-174">(50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)</span><span class="sxs-lookup"><span data-stu-id="c010f-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="c010f-175">22,00</span><span class="sxs-lookup"><span data-stu-id="c010f-175">22.00</span></span>     |
| <span data-ttu-id="c010f-176">305,00</span><span class="sxs-lookup"><span data-stu-id="c010f-176">305.00</span></span>                 | <span data-ttu-id="c010f-177">(50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50)</span><span class="sxs-lookup"><span data-stu-id="c010f-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="c010f-178">45,50</span><span class="sxs-lookup"><span data-stu-id="c010f-178">45.50</span></span>     |



<span data-ttu-id="c010f-179">Více informací najdete v části [Určení sazby DPH na základě polí Základ marže a Metoda výpočtu](marginal-base-field.md).</span><span class="sxs-lookup"><span data-stu-id="c010f-179">For more information, see [Determining sale tax rates based on the Marginal base and Calculation method fields](marginal-base-field.md).</span></span>





