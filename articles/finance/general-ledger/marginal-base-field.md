---
title: Sazby DPH na základě polí Základ marže a Metody výpočtu
description: Toto téma vysvětluje, jak hodnoty v poli Základ marže a Metoda výpočtu určují sazby daně v prodejních a nákupních transakcích.
author: ShylaThompson
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad4ec9f016b78425a2661d8df643ea67efc51fc9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838806"
---
# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a><span data-ttu-id="99b51-103">Sazby DPH na základě polí Základ marže a Metody výpočtu</span><span class="sxs-lookup"><span data-stu-id="99b51-103">Sales tax rates based on the Marginal base and Calculation methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99b51-104">Toto téma vysvětluje, jak hodnoty v poli Základ marže a Metoda výpočtu určují sazby daně v prodejních a nákupních transakcích.</span><span class="sxs-lookup"><span data-stu-id="99b51-104">This topic explains how the values in the fields Marginal base and Calculation method determine the tax rate(s) in sales and purchase transactions.</span></span>

<span data-ttu-id="99b51-105">Základ marže na pevné záložce Výpočet na stránce Kódy DPH určuje částku, která je použita k výběru odpovídající sazby daně ze sazeb na stránce Hodnoty kódu DPH.</span><span class="sxs-lookup"><span data-stu-id="99b51-105">The Marginal base on the Calculation FastTab on the Sales tax codes page determines which amount is used to pick the appropriate tax rate(s) from the rates in the Sales tax code values page.</span></span> <span data-ttu-id="99b51-106">Typ částky v poli Základ marže v kombinaci s metodu v poli Metoda výpočtu určuje logiku, podle které je hledána správná sazba daně pro transakci.</span><span class="sxs-lookup"><span data-stu-id="99b51-106">The amount type in the Marginal base field in combination with the method in the Calculation method field determines the logic to find the correct tax rate(s) for a transaction.</span></span> 

<span data-ttu-id="99b51-107">Různé kombinace hodnot v těchto polích poskytují velmi rozdílné výpočty DPH, jak je uvedeno v následujících příkladech.</span><span class="sxs-lookup"><span data-stu-id="99b51-107">Various combinations of values in these fields produce very different sales tax calculations, as shown by the following examples.</span></span> <span data-ttu-id="99b51-108">V příkladech jsou použity stejné hodnoty daňového období, jaké se nastavují pro každý kód DPH na stránce Hodnoty kódů DPH.</span><span class="sxs-lookup"><span data-stu-id="99b51-108">The examples use the same tax interval values, which are set up for each tax code in the Sales tax codes values page.</span></span> <span data-ttu-id="99b51-109">Tuto stránku otevřete kliknutím na možnosti Kód prodejní daně &gt; Hodnoty na stránce Kódy DPH.</span><span class="sxs-lookup"><span data-stu-id="99b51-109">To open this page, click Sales tax code &gt; Values in the Sales tax codes page.</span></span>

> [!Important]                                                                                                                  
> <span data-ttu-id="99b51-110">Je-li základ marže některého kódu DPH založen na částkách nebo jednotkách řádku, je nutné v poli Metoda výpočtu na stránce Parametry hlavní knihy nastavit hodnotu Řádek.</span><span class="sxs-lookup"><span data-stu-id="99b51-110">If the Marginal base on one or more of your sales tax codes is based on line amounts or units, the value of the Calculation method field in the General ledger parameters page must be set to Line.</span></span> |

## <a name="net-amount-per-line"></a><span data-ttu-id="99b51-111"> Čistá částka za řádek</span><span class="sxs-lookup"><span data-stu-id="99b51-111">Net amount per line</span></span>
<span data-ttu-id="99b51-112">Tuto možnost vyberte k určení sazeb DPH na základě čisté částky na řádcích faktury bez jakýchkoliv jiných daní.</span><span class="sxs-lookup"><span data-stu-id="99b51-112">Select this option to determine sales tax rates based on the net amount for the invoice lines, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="99b51-113">Příklad</span><span class="sxs-lookup"><span data-stu-id="99b51-113">Example</span></span>

<span data-ttu-id="99b51-114">Sazby DPH jsou nastaveny v následujících intervalech.</span><span class="sxs-lookup"><span data-stu-id="99b51-114">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="99b51-115">Intervaly pro částky</span><span class="sxs-lookup"><span data-stu-id="99b51-115">Amount interval</span></span>    | <span data-ttu-id="99b51-116">Daňová sazba</span><span class="sxs-lookup"><span data-stu-id="99b51-116">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="99b51-117">0–50</span><span class="sxs-lookup"><span data-stu-id="99b51-117">0 - 50</span></span>             | <span data-ttu-id="99b51-118">30 %</span><span class="sxs-lookup"><span data-stu-id="99b51-118">30%</span></span>      |
| <span data-ttu-id="99b51-119">50–100</span><span class="sxs-lookup"><span data-stu-id="99b51-119">50 - 100</span></span>           | <span data-ttu-id="99b51-120">20 %</span><span class="sxs-lookup"><span data-stu-id="99b51-120">20%</span></span>      |
| <span data-ttu-id="99b51-121">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="99b51-121">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="99b51-122">10 %</span><span class="sxs-lookup"><span data-stu-id="99b51-122">10%</span></span>      |

> [!NOTE]                                                                                                             
> <span data-ttu-id="99b51-123">Horní limit 0 v posledním intervalu značí zahrnutí všech částek větších než 100 do intervalu.</span><span class="sxs-lookup"><span data-stu-id="99b51-123">The upper limit of zero (0) in the last interval means that all amounts that exceed 100 are included in the interval.</span></span>

<span data-ttu-id="99b51-124">Základ marže: **Čistá částka podle řádku**</span><span class="sxs-lookup"><span data-stu-id="99b51-124">Marginal base: **Net amount per line**</span></span> 

<span data-ttu-id="99b51-125">Způsob výpočtu: **Interval**</span><span class="sxs-lookup"><span data-stu-id="99b51-125">Calculation method: **Interval**</span></span> 

<span data-ttu-id="99b51-126">Koupíte 8 lamp po 25,00 za kus.</span><span class="sxs-lookup"><span data-stu-id="99b51-126">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="99b51-127">Čistá částka řádku faktury je 200,00.</span><span class="sxs-lookup"><span data-stu-id="99b51-127">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="99b51-128">Daň se vypočítá následovně:</span><span class="sxs-lookup"><span data-stu-id="99b51-128">The tax is calculated as follows:</span></span> 

<span data-ttu-id="99b51-129">Celková DPH = 50 x 30 % + 50 x 20 % + 100 x 10 % = 15 + 10 + 10 = 35,00</span><span class="sxs-lookup"><span data-stu-id="99b51-129">Total sales tax = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = 35.00</span></span> 

<span data-ttu-id="99b51-130">Celková fakturovaná částka = 200,00 + 35,00 = 235,00</span><span class="sxs-lookup"><span data-stu-id="99b51-130">Total invoice amount = 200.00 + 35.00 = 235.00</span></span> 

<span data-ttu-id="99b51-131">**Odchylka**</span><span class="sxs-lookup"><span data-stu-id="99b51-131">**Variation**</span></span> 

<span data-ttu-id="99b51-132">Pokud má faktura dva řádky se čtyřmi položkami na každém řádku, čistá částka na každém řádku je 100 a DPH se vypočítá následovně:</span><span class="sxs-lookup"><span data-stu-id="99b51-132">If the invoice has two lines with four items on each line, the net amount on each line is 100.00 and the sales tax is calculated as follows:</span></span> 

<span data-ttu-id="99b51-133">DPH – řádek 1 = 50 x 30 % + 50 x 20 % = 15 + 10 = 25,00</span><span class="sxs-lookup"><span data-stu-id="99b51-133">Sales tax line 1 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="99b51-134">DPH - řádek 2 = 50 x 30 % + 50 x 20 % = 15 + 10 = 25,00</span><span class="sxs-lookup"><span data-stu-id="99b51-134">Sales tax line 2 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="99b51-135">Celková DPH = 25,00 + 25,00 = 50,00</span><span class="sxs-lookup"><span data-stu-id="99b51-135">Total sales tax = 25.00 + 25.00 = 50.00</span></span> 

<span data-ttu-id="99b51-136">Celková fakturovaná částka = 200,00 + 50,00 = 250,00</span><span class="sxs-lookup"><span data-stu-id="99b51-136">Total invoice amount = 200.00 + 50.00 = 250.00</span></span>

## <a name="net-amount-per-unit"></a><span data-ttu-id="99b51-137"> Čistá částka za jednotku</span><span class="sxs-lookup"><span data-stu-id="99b51-137">Net amount per unit</span></span>
<span data-ttu-id="99b51-138">Tuto možnost vyberte k určení sazeb DPH na základě hodnoty jednotlivých jednotek bez jakýchkoliv jiných daní.</span><span class="sxs-lookup"><span data-stu-id="99b51-138">Select this option to determine sales tax rates based on the value of each unit, excluding any other taxes.</span></span> <span data-ttu-id="99b51-139">Je-li vybrán základ marže vycházející z jednotek, je nutné určit jednotku také pro kód DPH.</span><span class="sxs-lookup"><span data-stu-id="99b51-139">When a unit based Marginal base is selected then also a Unit has to be specified for the Sales tax code.</span></span>

### <a name="example"></a><span data-ttu-id="99b51-140">Příklad</span><span class="sxs-lookup"><span data-stu-id="99b51-140">Example</span></span>

<span data-ttu-id="99b51-141">Sazby DPH jsou nastaveny v následujících intervalech.</span><span class="sxs-lookup"><span data-stu-id="99b51-141">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="99b51-142">Částka</span><span class="sxs-lookup"><span data-stu-id="99b51-142">Amount</span></span>             | <span data-ttu-id="99b51-143">Daňová sazba</span><span class="sxs-lookup"><span data-stu-id="99b51-143">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="99b51-144">0–50</span><span class="sxs-lookup"><span data-stu-id="99b51-144">0 - 50</span></span>             | <span data-ttu-id="99b51-145">30 %</span><span class="sxs-lookup"><span data-stu-id="99b51-145">30%</span></span>      |
| <span data-ttu-id="99b51-146">50–100</span><span class="sxs-lookup"><span data-stu-id="99b51-146">50 - 100</span></span>           | <span data-ttu-id="99b51-147">20 %</span><span class="sxs-lookup"><span data-stu-id="99b51-147">20%</span></span>      |
| <span data-ttu-id="99b51-148">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="99b51-148">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="99b51-149">10 %</span><span class="sxs-lookup"><span data-stu-id="99b51-149">10%</span></span>      |

<span data-ttu-id="99b51-150">Základ marže: **Čistá částka podle jednotky**</span><span class="sxs-lookup"><span data-stu-id="99b51-150">Marginal base: **Net amount per unit**</span></span> 

<span data-ttu-id="99b51-151">Metoda výpočtu: **Celková částka**</span><span class="sxs-lookup"><span data-stu-id="99b51-151">Calculation method: **Whole amount**</span></span> 

<span data-ttu-id="99b51-152">Koupíte 8 lamp po 25,00 za kus.</span><span class="sxs-lookup"><span data-stu-id="99b51-152">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="99b51-153">Čistá částka řádku faktury je 200,00.</span><span class="sxs-lookup"><span data-stu-id="99b51-153">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="99b51-154">Daň se vypočítá takto: DPH za jednotku = 25,00 x 30 % = 7,50 Celková DPH = 7,50 x 8 jednotek = 60,00 Celková fakturovaná částka = 200,00 + 60,00 = 260,00</span><span class="sxs-lookup"><span data-stu-id="99b51-154">The tax is calculated as follows: Sales tax per unit = 25.00 x 30% = 7.50 Total sales tax = 7.50 x 8 units = 60.00 Total invoice amount = 200.00 + 60.00 = 260.00</span></span>

## <a name="net-amount-of-invoice-balance"></a><span data-ttu-id="99b51-155"> Čistá částka zůstatku faktury</span><span class="sxs-lookup"><span data-stu-id="99b51-155">Net amount of invoice balance</span></span>

<span data-ttu-id="99b51-156">Tuto možnost vyberte k určení sazeb DPH na základě celkové hodnoty faktury bez jakýchkoliv jiných daní.</span><span class="sxs-lookup"><span data-stu-id="99b51-156">Select this option to determine sales tax rates based on the total value for the invoice, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="99b51-157">Příklad</span><span class="sxs-lookup"><span data-stu-id="99b51-157">Example</span></span>

<span data-ttu-id="99b51-158">Sazby DPH jsou nastaveny v následujících intervalech.</span><span class="sxs-lookup"><span data-stu-id="99b51-158">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="99b51-159">Částka</span><span class="sxs-lookup"><span data-stu-id="99b51-159">Amount</span></span>            | <span data-ttu-id="99b51-160">Daňová sazba</span><span class="sxs-lookup"><span data-stu-id="99b51-160">Tax rate</span></span> |
|-------------------|----------|
| <span data-ttu-id="99b51-161">0–50</span><span class="sxs-lookup"><span data-stu-id="99b51-161">0 - 50</span></span>            | <span data-ttu-id="99b51-162">30 %</span><span class="sxs-lookup"><span data-stu-id="99b51-162">30%</span></span>      |
| <span data-ttu-id="99b51-163">50–100</span><span class="sxs-lookup"><span data-stu-id="99b51-163">50 - 100</span></span>          | <span data-ttu-id="99b51-164">20 %</span><span class="sxs-lookup"><span data-stu-id="99b51-164">20%</span></span>      |
| <span data-ttu-id="99b51-165">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="99b51-165">100 -0 (&gt; 100)</span></span> | <span data-ttu-id="99b51-166">10 %</span><span class="sxs-lookup"><span data-stu-id="99b51-166">10%</span></span>      |

<span data-ttu-id="99b51-167">Základ marže: **Čistá částka zůstatku faktury**</span><span class="sxs-lookup"><span data-stu-id="99b51-167">Marginal base: **Net amount of invoice balance**</span></span> 

<span data-ttu-id="99b51-168">Metoda výpočtu: **Interval** Prodejní faktura obsahuje 2 řádky se 4 zářivkami na jednotlivých řádkách pro 25,00 ks.</span><span class="sxs-lookup"><span data-stu-id="99b51-168">Calculation method: **Interval** A sales invoice has 2 lines with 4 lamps on each lines for 25.00 each.</span></span> <span data-ttu-id="99b51-169">Čistá částka zůstatku faktury je 4 x 25,00 + 4 x 25,00 = 200,00.</span><span class="sxs-lookup"><span data-stu-id="99b51-169">The net amount of invoice balance is 4 x 25.00 + 4 x 25.00 = 200.00.</span></span> <span data-ttu-id="99b51-170">Daň se vypočítá takto: Celková DPH = 50 x 0,30 + 50 x 0,20 + 100 x 0,10 = 15 + 10 + 10 = 35,00 Celková fakturovaná částka = 200,00 + 35,00 = 235,00</span><span class="sxs-lookup"><span data-stu-id="99b51-170">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 100 x 0.10 = 15 + 10 + 10 = 35.00 Total invoice amount = 200.00 + 35.00 = 235.00</span></span>

## <a name="gross-amount-per-line"></a><span data-ttu-id="99b51-171"> Hrubá částka za řádek</span><span class="sxs-lookup"><span data-stu-id="99b51-171">Gross amount per line</span></span>

<span data-ttu-id="99b51-172">Tuto možnost vyberte k určení sazeb DPH na základě hodnoty řádku včetně jakýchkoliv jiných daní pro daný řádek.</span><span class="sxs-lookup"><span data-stu-id="99b51-172">Select this option to determine sales tax rates based on the value of the line including all other taxes for that line.</span></span>

> [!NOTE]
> <span data-ttu-id="99b51-173">Ve skupině DPH může být s touto hodnotou v poli Základ marže uveden pouze jeden kód DPH.</span><span class="sxs-lookup"><span data-stu-id="99b51-173">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="99b51-174">Příklad</span><span class="sxs-lookup"><span data-stu-id="99b51-174">Example</span></span>

<span data-ttu-id="99b51-175">Sazby DPH jsou nastaveny v následujících intervalech.</span><span class="sxs-lookup"><span data-stu-id="99b51-175">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="99b51-176">Částka</span><span class="sxs-lookup"><span data-stu-id="99b51-176">Amount</span></span>             | <span data-ttu-id="99b51-177">Daňová sazba</span><span class="sxs-lookup"><span data-stu-id="99b51-177">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="99b51-178">0–50</span><span class="sxs-lookup"><span data-stu-id="99b51-178">0 - 50</span></span>             | <span data-ttu-id="99b51-179">30 %</span><span class="sxs-lookup"><span data-stu-id="99b51-179">30%</span></span>      |
| <span data-ttu-id="99b51-180">50–100</span><span class="sxs-lookup"><span data-stu-id="99b51-180">50 - 100</span></span>           | <span data-ttu-id="99b51-181">20 %</span><span class="sxs-lookup"><span data-stu-id="99b51-181">20%</span></span>      |
| <span data-ttu-id="99b51-182">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="99b51-182">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="99b51-183">10 %</span><span class="sxs-lookup"><span data-stu-id="99b51-183">10%</span></span>      |

<span data-ttu-id="99b51-184">Základ marže: **Hrubá částka za řádek** Metoda výpočtu: **Interval** Dále je zde vypočítán jiný kód daně pro zvláštní clo 5,00 na každou lampu.</span><span class="sxs-lookup"><span data-stu-id="99b51-184">Marginal base: **Gross amount per line** Calculation method: **Interval** Additionally there is another tax code calculated for a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="99b51-185">Toto clo je k čisté částce přidáno před výpočtem DPH.</span><span class="sxs-lookup"><span data-stu-id="99b51-185">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="99b51-186">Koupíte 8 lamp po 25,00 za kus.</span><span class="sxs-lookup"><span data-stu-id="99b51-186">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="99b51-187">Čistá částka řádku faktury je 200,00.</span><span class="sxs-lookup"><span data-stu-id="99b51-187">The net amount for the invoice line is 200.00.</span></span> <span data-ttu-id="99b51-188">Hrubá částka řádku faktury je 8 x 25,00 + 8 x 5,00 = 240,00.</span><span class="sxs-lookup"><span data-stu-id="99b51-188">The gross amount for the invoice line is 8 x 25.00 + 8 x 5.00 = 240.00.</span></span> <span data-ttu-id="99b51-189">Daň se vypočítá takto: Celková DPH = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 20 + 14 = 39,00 Celkové clo = 5,00 x 8 = 40,00 Celková fakturovaná částka = 200,00 + 39,00 + 40,00 = 279,00</span><span class="sxs-lookup"><span data-stu-id="99b51-189">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 20 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="99b51-190">**Odchylka**</span><span class="sxs-lookup"><span data-stu-id="99b51-190">**Variation**</span></span> 

<span data-ttu-id="99b51-191">Pokud dojde k vytvoření faktury pomocí dvou řádků se čtyřmi položkami na každém řádku, čistá částka na řádek je 100,00.</span><span class="sxs-lookup"><span data-stu-id="99b51-191">If the invoice is created by using 2 invoice lines with 4 items on each line, the net amount per invoice line is 100.00.</span></span> <span data-ttu-id="99b51-192">Hrubá částka (včetně cla 4 x 5,00) na každém řádku faktury by byla 120,00 a DPH se vypočte následujícím způsobem: DPH pro řádek faktury 1 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 DPH pro řádek faktury 2 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Celková DPH = 27,00 + 27,00 = 54,00 Celkové clo = 5,00 x 8 = 40,00 Celková fakturovaná částka = 200,00 + 54,00 + 40,00 = 294,00</span><span class="sxs-lookup"><span data-stu-id="99b51-192">The gross amount (including the duty of 4 x 5.00) per invoice line would be 120.00, and the sales tax is created as follows: Sales tax invoice line 1 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Sales tax invoice line 2 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Total sales tax = 27.00 + 27.00 = 54.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 54.00 + 40.00 = 294.00</span></span>

## <a name="gross-amount-per-unit"></a><span data-ttu-id="99b51-193"> Hrubá částka za jednotku</span><span class="sxs-lookup"><span data-stu-id="99b51-193">Gross amount per unit</span></span>

<span data-ttu-id="99b51-194">Tuto možnost vyberte k určení sazeb DPH na základě hodnoty jednotky včetně jakýchkoliv jiných daní.</span><span class="sxs-lookup"><span data-stu-id="99b51-194">Select this option to determine sales tax rates based on the value of the unit including any other taxes.</span></span>

> [!NOTE]
> <span data-ttu-id="99b51-195">Ve skupině DPH může být s touto hodnotou v poli Základ marže uveden pouze jeden kód DPH.</span><span class="sxs-lookup"><span data-stu-id="99b51-195">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="99b51-196">Příklad</span><span class="sxs-lookup"><span data-stu-id="99b51-196">Example</span></span>

<span data-ttu-id="99b51-197">Sazby DPH jsou nastaveny v následujících intervalech.</span><span class="sxs-lookup"><span data-stu-id="99b51-197">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="99b51-198">Částka</span><span class="sxs-lookup"><span data-stu-id="99b51-198">Amount</span></span>             | <span data-ttu-id="99b51-199">Daňová sazba</span><span class="sxs-lookup"><span data-stu-id="99b51-199">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="99b51-200">0–50</span><span class="sxs-lookup"><span data-stu-id="99b51-200">0 - 50</span></span>             | <span data-ttu-id="99b51-201">30 %</span><span class="sxs-lookup"><span data-stu-id="99b51-201">30%</span></span>      |
| <span data-ttu-id="99b51-202">50–100</span><span class="sxs-lookup"><span data-stu-id="99b51-202">50 - 100</span></span>           | <span data-ttu-id="99b51-203">20 %</span><span class="sxs-lookup"><span data-stu-id="99b51-203">20%</span></span>      |
| <span data-ttu-id="99b51-204">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="99b51-204">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="99b51-205">10 %</span><span class="sxs-lookup"><span data-stu-id="99b51-205">10%</span></span>      |

<span data-ttu-id="99b51-206">Základ marže: **Hrubá částka za jednotku** Je uloženo zvláštní clo 5,00 na každou lampu.</span><span class="sxs-lookup"><span data-stu-id="99b51-206">Marginal base: **Gross amount per unit** There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="99b51-207">Toto clo je k čisté částce přidáno před výpočtem DPH.</span><span class="sxs-lookup"><span data-stu-id="99b51-207">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="99b51-208">Koupíte 8 lamp po 25,00 za kus.</span><span class="sxs-lookup"><span data-stu-id="99b51-208">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="99b51-209">Hrubá částka na jednotku je 30,00.</span><span class="sxs-lookup"><span data-stu-id="99b51-209">The gross amount per unit is 30.00.</span></span> <span data-ttu-id="99b51-210">Daň se vypočítá takto: DPH za jednotku = 30 x 30 % = 9,00 Celková DPH = 9,00 x 8 = 72,00 Celkové clo= 5,00 x 8 = 40,00 Celková fakturovaná částka = 200,00 + 72,00 + 40,00 = 312,00</span><span class="sxs-lookup"><span data-stu-id="99b51-210">The tax is calculated as follows: Sales tax per unit = 30 x 30% = 9.00 Total sales tax = 9.00 x 8 = 72.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 72.00 + 40.00 = 312.00</span></span>

## <a name="invoice-total-incl-other-sales-tax-amounts"></a><span data-ttu-id="99b51-211"> Celková fakturovaná částka, včetně částek DPH</span><span class="sxs-lookup"><span data-stu-id="99b51-211">Invoice total incl. other sales tax amounts</span></span>

<span data-ttu-id="99b51-212">Tuto možnost vyberte k určení sazeb DPH na základě celkové hodnoty faktury včetně jakýchkoliv jiných daní.</span><span class="sxs-lookup"><span data-stu-id="99b51-212">Select this option to determine sales tax rates based on the total value for the invoice including any other taxes.</span></span>
> [!NOTE]
> <span data-ttu-id="99b51-213">Ve skupině DPH může být s touto hodnotou v poli Základ marže uveden pouze jeden kód DPH.</span><span class="sxs-lookup"><span data-stu-id="99b51-213">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field</span></span>

### <a name="example"></a><span data-ttu-id="99b51-214">Příklad</span><span class="sxs-lookup"><span data-stu-id="99b51-214">Example</span></span>

<span data-ttu-id="99b51-215">Sazby DPH jsou nastaveny v následujících intervalech.</span><span class="sxs-lookup"><span data-stu-id="99b51-215">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="99b51-216">Částka</span><span class="sxs-lookup"><span data-stu-id="99b51-216">Amount</span></span>             | <span data-ttu-id="99b51-217">Daňová sazba</span><span class="sxs-lookup"><span data-stu-id="99b51-217">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="99b51-218">0–50</span><span class="sxs-lookup"><span data-stu-id="99b51-218">0 - 50</span></span>             | <span data-ttu-id="99b51-219">30 %</span><span class="sxs-lookup"><span data-stu-id="99b51-219">30%</span></span>      |
| <span data-ttu-id="99b51-220">50–100</span><span class="sxs-lookup"><span data-stu-id="99b51-220">50 - 100</span></span>           | <span data-ttu-id="99b51-221">20 %</span><span class="sxs-lookup"><span data-stu-id="99b51-221">20%</span></span>      |
| <span data-ttu-id="99b51-222">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="99b51-222">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="99b51-223">10 %</span><span class="sxs-lookup"><span data-stu-id="99b51-223">10%</span></span>      |

<span data-ttu-id="99b51-224">Základ marže: **Faktura celkem včetně částek DPH** metoda výpočtu: **Interval** </span><span class="sxs-lookup"><span data-stu-id="99b51-224">Marginal base: **Invoice total incl. other sales tax amounts** Calculation method: **Interval** </span></span>  
<span data-ttu-id="99b51-225">Pro každou lampu existuje speciální clo ve výši 5,00 eur.</span><span class="sxs-lookup"><span data-stu-id="99b51-225">There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="99b51-226">Toto clo je k čisté částce přidáno před výpočtem DPH.</span><span class="sxs-lookup"><span data-stu-id="99b51-226">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="99b51-227">Koupíte 8 lamp po 25,00 za kus.</span><span class="sxs-lookup"><span data-stu-id="99b51-227">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="99b51-228">Čistá částka faktury je 200,00.</span><span class="sxs-lookup"><span data-stu-id="99b51-228">The net amount for the invoice is 200.00.</span></span> <span data-ttu-id="99b51-229">Hrubá částka faktury je 200,00 + (8 x 5,00) = 240,00.</span><span class="sxs-lookup"><span data-stu-id="99b51-229">The gross amount for the invoice is 200.00 + (8 x 5.00) = 240.00.</span></span> <span data-ttu-id="99b51-230">Daň se vypočítá takto: Celková DPH = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 10 + 14 = 39,00 Celkové clo = 5,00 x 8 = 40,00 Celková fakturovaná částka = 200,00 + 39,00 + 40,00 = 279,00</span><span class="sxs-lookup"><span data-stu-id="99b51-230">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 10 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="99b51-231">Další informace viz [Možnost Celková částka a Interval výpočtu pro kódy DPH](whole-amount-interval-options-sales-tax-codes.md) a [Metody výpočtu DPH v poli Zdroj](sales-tax-calculation-methods-origin-field.md).</span><span class="sxs-lookup"><span data-stu-id="99b51-231">For more information, see [Whole amount and Interval calculation options for sales tax codes](whole-amount-interval-options-sales-tax-codes.md) and [Sales tax calculation methods in the Origin field](sales-tax-calculation-methods-origin-field.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]