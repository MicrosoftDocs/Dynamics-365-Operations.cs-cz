---
title: Výpočet režijních nákladů
description: Toto téma popisuje typické procesy pro výpočet a přidělení režijních nákladů.
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: cc6ad48ef80aa01739129b59cc1133d0a1930f24
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759465"
---
# <a name="overhead-calculation"></a><span data-ttu-id="73cf6-103">Výpočet režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73cf6-104">Toto téma popisuje typické procesy pro výpočet a přidělení režijních nákladů.</span><span class="sxs-lookup"><span data-stu-id="73cf6-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="73cf6-105">Definice termínu</span><span class="sxs-lookup"><span data-stu-id="73cf6-105">Term definition</span></span>
---------------

<span data-ttu-id="73cf6-106">Režijní náklady jsou náklady, které nutně vznikají při chodu podnikání, ale nelze je připsat přímo k žádné konkrétní podnikatelské aktivitě, produktu nebo službě.</span><span class="sxs-lookup"><span data-stu-id="73cf6-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="73cf6-107">Režijní náklady poskytují důležitou podporu pro generování aktivity přinášejících zisk.</span><span class="sxs-lookup"><span data-stu-id="73cf6-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="73cf6-108">Následuje několik příkladů režijních nákladů:</span><span class="sxs-lookup"><span data-stu-id="73cf6-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="73cf6-109">Renta</span><span class="sxs-lookup"><span data-stu-id="73cf6-109">Rent</span></span>
-   <span data-ttu-id="73cf6-110">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-110">Electricity</span></span>
-   <span data-ttu-id="73cf6-111">Administrativní mzdy</span><span class="sxs-lookup"><span data-stu-id="73cf6-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="73cf6-112">Přehled výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-112">Overhead calculation overview</span></span>
<span data-ttu-id="73cf6-113">Výpočet režijních nákladů spustí zásady účtování nákladů ve správném pořadí.</span><span class="sxs-lookup"><span data-stu-id="73cf6-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="73cf6-114">Výpočet režijních nákladů můžete pro stejné fiskální období spustit mnohokrát, pokud došlo ke změně zásad účtování nákladů nebo zjištění konkrétních chyb.</span><span class="sxs-lookup"><span data-stu-id="73cf6-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="73cf6-115">Každé spuštění výpočtu režijních nákladů se ukládá a přijímá ID jedinečné verze, které vám umožní porovnávat výpočty v různých verzích.</span><span class="sxs-lookup"><span data-stu-id="73cf6-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="73cf6-116">Položky nákladů, které generuje výpočet režijních nákladů, přijímá datum účtování.</span><span class="sxs-lookup"><span data-stu-id="73cf6-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="73cf6-117">Toto datum účtován se shoduje s konvovým datem fiskálního období, které se použije ve výpočtu.</span><span class="sxs-lookup"><span data-stu-id="73cf6-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="73cf6-118">ID jedinečné verze se skládá z následujících prvků:</span><span class="sxs-lookup"><span data-stu-id="73cf6-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="73cf6-119">Typ verze</span><span class="sxs-lookup"><span data-stu-id="73cf6-119">Version type</span></span>
-   <span data-ttu-id="73cf6-120">Datum a čas</span><span class="sxs-lookup"><span data-stu-id="73cf6-120">Date and time</span></span>
-   <span data-ttu-id="73cf6-121">Hlavní kniha nákladového účetnictví</span><span class="sxs-lookup"><span data-stu-id="73cf6-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="73cf6-122">Fiskální rok</span><span class="sxs-lookup"><span data-stu-id="73cf6-122">Fiscal year</span></span>
-   <span data-ttu-id="73cf6-123">Fiskální období</span><span class="sxs-lookup"><span data-stu-id="73cf6-123">Fiscal period</span></span>

<span data-ttu-id="73cf6-124">Výpočet režijních nákladů se spustí bez ohledu na verzi.</span><span class="sxs-lookup"><span data-stu-id="73cf6-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="73cf6-125">Proto lze vypočítat rozpočtovou verzi před skutečnou verzí.</span><span class="sxs-lookup"><span data-stu-id="73cf6-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="73cf6-126">Výpočet režijních nákladů se skládá ze čtyř kroků uvedených na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="73cf6-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="73cf6-127">V každé fázi je vytvořeno záhlaví deníku, které obsahuje položky deníku.</span><span class="sxs-lookup"><span data-stu-id="73cf6-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="73cf6-128">Toto záhlaví deníku zachovává vstupní data pro každý krok výpočtu.</span><span class="sxs-lookup"><span data-stu-id="73cf6-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="73cf6-129">Zásady a pravidla se použijí na každý řádek deníku a položky nákladů jsou generovány jako výstup.</span><span class="sxs-lookup"><span data-stu-id="73cf6-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="73cf6-130">Máte tedy vždy plnou sledovatelnost.</span><span class="sxs-lookup"><span data-stu-id="73cf6-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="73cf6-131">[![Výpočet režijních nákladů](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="73cf6-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="73cf6-132">Výpočet a přidělení režijních nákladů za elektřinu</span><span class="sxs-lookup"><span data-stu-id="73cf6-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="73cf6-133">Ve finančním účetnictví se některé náklady, jako je například elektřina, registrují jako paušální.</span><span class="sxs-lookup"><span data-stu-id="73cf6-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="73cf6-134">Podrobný přehled pro vedoucí není tedy pro nákladové účetnictví k dispozici.</span><span class="sxs-lookup"><span data-stu-id="73cf6-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="73cf6-135">V nákladovém účetnictví musí náklady procházet organizačními jednotkami, aby byl získán správný přehled pro vedoucí napříč všemi jednotkami a úrovněmi organizace.</span><span class="sxs-lookup"><span data-stu-id="73cf6-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="73cf6-136">Tento tok musí být založen buď na přesném záznamu spotřeby nebo na objektivním hodnocení.</span><span class="sxs-lookup"><span data-stu-id="73cf6-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="73cf6-137">V hlavní knize mohou být zaúčtovány náklady na elektřinu způsobem znázorněným v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="73cf6-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="73cf6-138">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="73cf6-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="73cf6-139">Nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="73cf6-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="73cf6-140">Hlavní účet</span><span class="sxs-lookup"><span data-stu-id="73cf6-140">Main account</span></span></th>
<th><span data-ttu-id="73cf6-141">Částka v zúčtovací měně</span><span class="sxs-lookup"><span data-stu-id="73cf6-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73cf6-142">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="73cf6-143">CC099</span><span class="sxs-lookup"><span data-stu-id="73cf6-143">CC099</span></span></td>
<td><span data-ttu-id="73cf6-144">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="73cf6-144">Default cost center</span></span></td>
<td><span data-ttu-id="73cf6-145">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-145">10001</span></span></td>
<td><span data-ttu-id="73cf6-146">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-146">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="73cf6-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="73cf6-148">Krok 1: Zpracování výpočtu chování nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="73cf6-149">Ve výchozím nastavení dostanou při importu položek nákladů z datového zdroje tyto položky v nákladovém účetnictví klasifikaci **Neklasifikované**.</span><span class="sxs-lookup"><span data-stu-id="73cf6-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="73cf6-150">Použitím pravidla zásad chování nákladů lze reklasifikovat položky nákladů jako **Pevné náklady** nebo **Variabilní náklady**.</span><span class="sxs-lookup"><span data-stu-id="73cf6-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="73cf6-151">Definice pravidel chování nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-151">Define the cost behavior rule</span></span>

<span data-ttu-id="73cf6-152">V některých případech je část nákladů s pevným poplatkem a zbývající náklady jsou založeny na spotřebě.</span><span class="sxs-lookup"><span data-stu-id="73cf6-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="73cf6-153">Účty za elektřinu často odpovídají této definici.</span><span class="sxs-lookup"><span data-stu-id="73cf6-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="73cf6-154">Po platbě konkrétního pevného poplatku platíte spotřebu za kilowatthodinu (kWh).</span><span class="sxs-lookup"><span data-stu-id="73cf6-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="73cf6-155">Pokud je například poplatek pevných nákladů 1 000,00, definuje se pravidlo chování nákladů takto:</span><span class="sxs-lookup"><span data-stu-id="73cf6-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="73cf6-156">Pevná částka 1 000,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="73cf6-157">0 &lt;= 1 000,00 = Pevná</span><span class="sxs-lookup"><span data-stu-id="73cf6-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="73cf6-158">1 000,01 &lt; N = Variabilní</span><span class="sxs-lookup"><span data-stu-id="73cf6-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="73cf6-159">Deník</span><span class="sxs-lookup"><span data-stu-id="73cf6-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="73cf6-160">Deník</span><span class="sxs-lookup"><span data-stu-id="73cf6-160">Journal</span></span></th>
<th><span data-ttu-id="73cf6-161">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="73cf6-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="73cf6-162">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="73cf6-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="73cf6-163">Verze</span><span class="sxs-lookup"><span data-stu-id="73cf6-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73cf6-164">00001</span><span class="sxs-lookup"><span data-stu-id="73cf6-164">00001</span></span></td>
<td><span data-ttu-id="73cf6-165">Deník výpočtu chování nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="73cf6-166">Fiskální</span><span class="sxs-lookup"><span data-stu-id="73cf6-166">Fiscal</span></span></td>
<td><span data-ttu-id="73cf6-167">2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-167">2017</span></span></td>
<td><span data-ttu-id="73cf6-168">Období 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-168">Period 1</span></span></td>
<td><span data-ttu-id="73cf6-169">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="73cf6-170">Položky deníku (Položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="73cf6-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="73cf6-171">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="73cf6-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="73cf6-172">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="73cf6-173">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-173">Cost element</span></span></th>
<th><span data-ttu-id="73cf6-174">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-174">Cost behavior</span></span></th>
<th><span data-ttu-id="73cf6-175">Částka</span><span class="sxs-lookup"><span data-stu-id="73cf6-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73cf6-176">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="73cf6-177">CC099</span><span class="sxs-lookup"><span data-stu-id="73cf6-177">CC099</span></span></td>
<td><span data-ttu-id="73cf6-178">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="73cf6-178">Default cost center</span></span></td>
<td><span data-ttu-id="73cf6-179">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-179">10001</span></span></td>
<td><span data-ttu-id="73cf6-180">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-180">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-181">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="73cf6-181">Unclassified</span></span></td>
<td><span data-ttu-id="73cf6-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="73cf6-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="73cf6-183">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73cf6-184">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="73cf6-185">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-185">Cost element</span></span></th>
<th><span data-ttu-id="73cf6-186">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-186">Cost behavior</span></span></th>
<th><span data-ttu-id="73cf6-187">Částka</span><span class="sxs-lookup"><span data-stu-id="73cf6-187">Amount</span></span></th>
<th><span data-ttu-id="73cf6-188">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="73cf6-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73cf6-189">CC099</span><span class="sxs-lookup"><span data-stu-id="73cf6-189">CC099</span></span></td>
<td><span data-ttu-id="73cf6-190">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="73cf6-190">Default cost center</span></span></td>
<td><span data-ttu-id="73cf6-191">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-191">10001</span></span></td>
<td><span data-ttu-id="73cf6-192">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-192">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-193">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="73cf6-193">Unclassified</span></span></td>
<td><span data-ttu-id="73cf6-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="73cf6-194">10,000.00</span></span></td>
<td><span data-ttu-id="73cf6-195">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-196">CC099</span><span class="sxs-lookup"><span data-stu-id="73cf6-196">CC099</span></span></td>
<td><span data-ttu-id="73cf6-197">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="73cf6-197">Default cost center</span></span></td>
<td><span data-ttu-id="73cf6-198">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-198">10001</span></span></td>
<td><span data-ttu-id="73cf6-199">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-199">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-200">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="73cf6-200">Unclassified</span></span></td>
<td><span data-ttu-id="73cf6-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-201">-10,000.00</span></span></td>
<td><span data-ttu-id="73cf6-202">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-203">CC099</span><span class="sxs-lookup"><span data-stu-id="73cf6-203">CC099</span></span></td>
<td><span data-ttu-id="73cf6-204">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="73cf6-204">Default cost center</span></span></td>
<td><span data-ttu-id="73cf6-205">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-205">10001</span></span></td>
<td><span data-ttu-id="73cf6-206">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-206">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-207">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-207">Fixed cost</span></span></td>
<td><span data-ttu-id="73cf6-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-208">1,000.00</span></span></td>
<td><span data-ttu-id="73cf6-209">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-210">CC099</span><span class="sxs-lookup"><span data-stu-id="73cf6-210">CC099</span></span></td>
<td><span data-ttu-id="73cf6-211">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="73cf6-211">Default cost center</span></span></td>
<td><span data-ttu-id="73cf6-212">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-212">10001</span></span></td>
<td><span data-ttu-id="73cf6-213">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-213">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-214">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-214">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="73cf6-215">9,000.00</span></span></td>
<td><span data-ttu-id="73cf6-216">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="73cf6-217">Více informací naleznete v tématu [Vytvoření a přiřazení zásad chování nákladů k jednotce řízení nákladů](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="73cf6-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="73cf6-218">Krok 2: Zpracování výpočtu distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="73cf6-219">Distribuce nákladů se používá k rozdělení nákladů z jednoho objektu nákladů na jeden nebo více dalších objektů nákladů použitím příslušného základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="73cf6-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="73cf6-220">Distribuce nákladů a přidělení nákladů se liší v tom, že k distribuci nákladů dochází vždy na úrovni primárního prvku nákladů původních nákladů.</span><span class="sxs-lookup"><span data-stu-id="73cf6-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="73cf6-221">Definice pravidel distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-221">Define the cost distribution rule</span></span>

<span data-ttu-id="73cf6-222">Ve finančním účetnictví se náklady na elektřinu často registrují jako paušální.</span><span class="sxs-lookup"><span data-stu-id="73cf6-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="73cf6-223">V nákladovém účetnictví není tento přístup dostatečně podrobný.</span><span class="sxs-lookup"><span data-stu-id="73cf6-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="73cf6-224">Variabilní náklady by měly být distribuovány k jednotlivým objektům nákladů na solidním základě.</span><span class="sxs-lookup"><span data-stu-id="73cf6-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="73cf6-225">Nejlogičtější základ přidělení je spotřeba elektřiny (kWh).</span><span class="sxs-lookup"><span data-stu-id="73cf6-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="73cf6-226">Vytvoří se člen statistické dimenzi s názvem Elektřina a zaznamená se elektrické spotřeba.</span><span class="sxs-lookup"><span data-stu-id="73cf6-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="73cf6-227">Ve výchozím nastavení se všechny členy statistické dimenze stanou dostupnými zpřístupněny jako základy přidělení.</span><span class="sxs-lookup"><span data-stu-id="73cf6-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73cf6-228">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-228">Cost object</span></span></th>
<th><span data-ttu-id="73cf6-229">kWh</span><span class="sxs-lookup"><span data-stu-id="73cf6-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73cf6-230">CC001</span><span class="sxs-lookup"><span data-stu-id="73cf6-230">CC001</span></span></td>
<td><span data-ttu-id="73cf6-231">HR</span><span class="sxs-lookup"><span data-stu-id="73cf6-231">HR</span></span></td>
<td><span data-ttu-id="73cf6-232">1 000</span><span class="sxs-lookup"><span data-stu-id="73cf6-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-233">CC002</span><span class="sxs-lookup"><span data-stu-id="73cf6-233">CC002</span></span></td>
<td><span data-ttu-id="73cf6-234">Finance</span><span class="sxs-lookup"><span data-stu-id="73cf6-234">Finance</span></span></td>
<td><span data-ttu-id="73cf6-235">6,000</span><span class="sxs-lookup"><span data-stu-id="73cf6-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-236">CC003</span><span class="sxs-lookup"><span data-stu-id="73cf6-236">CC003</span></span></td>
<td><span data-ttu-id="73cf6-237">Sestavení</span><span class="sxs-lookup"><span data-stu-id="73cf6-237">Assembly</span></span></td>
<td><span data-ttu-id="73cf6-238">0</span><span class="sxs-lookup"><span data-stu-id="73cf6-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="73cf6-239">Následující tabulka zobrazuje výsledek při použití elektrické spotřeby jako základu přidělení pro variabilní náklady.</span><span class="sxs-lookup"><span data-stu-id="73cf6-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73cf6-240">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-240">Cost object</span></span></th>
<th><span data-ttu-id="73cf6-241">Hodnota</span><span class="sxs-lookup"><span data-stu-id="73cf6-241">Magnitude</span></span></th>
<th><span data-ttu-id="73cf6-242">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="73cf6-242">Allocation factor</span></span></th>
<th><span data-ttu-id="73cf6-243">Částka</span><span class="sxs-lookup"><span data-stu-id="73cf6-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73cf6-244">CC001</span><span class="sxs-lookup"><span data-stu-id="73cf6-244">CC001</span></span></td>
<td><span data-ttu-id="73cf6-245">HR</span><span class="sxs-lookup"><span data-stu-id="73cf6-245">HR</span></span></td>
<td><span data-ttu-id="73cf6-246">1 000</span><span class="sxs-lookup"><span data-stu-id="73cf6-246">1,000</span></span></td>
<td><span data-ttu-id="73cf6-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="73cf6-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="73cf6-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-249">CC002</span><span class="sxs-lookup"><span data-stu-id="73cf6-249">CC002</span></span></td>
<td><span data-ttu-id="73cf6-250">Finance</span><span class="sxs-lookup"><span data-stu-id="73cf6-250">Finance</span></span></td>
<td><span data-ttu-id="73cf6-251">6,000</span><span class="sxs-lookup"><span data-stu-id="73cf6-251">6,000</span></span></td>
<td><span data-ttu-id="73cf6-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="73cf6-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="73cf6-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-254">CC003</span><span class="sxs-lookup"><span data-stu-id="73cf6-254">CC003</span></span></td>
<td><span data-ttu-id="73cf6-255">Sestavení</span><span class="sxs-lookup"><span data-stu-id="73cf6-255">Assembly</span></span></td>
<td><span data-ttu-id="73cf6-256">0</span><span class="sxs-lookup"><span data-stu-id="73cf6-256">0</span></span></td>
<td><span data-ttu-id="73cf6-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="73cf6-258">0,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="73cf6-259">Pevné náklady musí být distribuovány rovnoměrně k jednotlivých objektům nákladů, které spotřebovávaly elektřinu.</span><span class="sxs-lookup"><span data-stu-id="73cf6-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="73cf6-260">Tohoto výsledku můžete dosáhnout pomocí členu statistické dimenze Elektřina v základu přidělení vzorce: (Elektřina &gt; 0,00) Následující tabulka zobrazuje výsledek při použití elektrické spotřeby jako základu přidělení pro variabilní náklady.</span><span class="sxs-lookup"><span data-stu-id="73cf6-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73cf6-261">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-261">Cost object</span></span></th>
<th><span data-ttu-id="73cf6-262">Vzorec</span><span class="sxs-lookup"><span data-stu-id="73cf6-262">Formula</span></span></th>
<th><span data-ttu-id="73cf6-263">Hodnota</span><span class="sxs-lookup"><span data-stu-id="73cf6-263">Magnitude</span></span></th>
<th><span data-ttu-id="73cf6-264">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="73cf6-264">Allocation factor</span></span></th>
<th><span data-ttu-id="73cf6-265">Částka</span><span class="sxs-lookup"><span data-stu-id="73cf6-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73cf6-266">CC001</span><span class="sxs-lookup"><span data-stu-id="73cf6-266">CC001</span></span></td>
<td><span data-ttu-id="73cf6-267">HR</span><span class="sxs-lookup"><span data-stu-id="73cf6-267">HR</span></span></td>
<td><span data-ttu-id="73cf6-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="73cf6-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="73cf6-269">1</span><span class="sxs-lookup"><span data-stu-id="73cf6-269">1</span></span></td>
<td><span data-ttu-id="73cf6-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="73cf6-271">500.00</span><span class="sxs-lookup"><span data-stu-id="73cf6-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-272">CC002</span><span class="sxs-lookup"><span data-stu-id="73cf6-272">CC002</span></span></td>
<td><span data-ttu-id="73cf6-273">Finance</span><span class="sxs-lookup"><span data-stu-id="73cf6-273">Finance</span></span></td>
<td><span data-ttu-id="73cf6-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="73cf6-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="73cf6-275">1</span><span class="sxs-lookup"><span data-stu-id="73cf6-275">1</span></span></td>
<td><span data-ttu-id="73cf6-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="73cf6-277">500.00</span><span class="sxs-lookup"><span data-stu-id="73cf6-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-278">CC003</span><span class="sxs-lookup"><span data-stu-id="73cf6-278">CC003</span></span></td>
<td><span data-ttu-id="73cf6-279">Sestavení</span><span class="sxs-lookup"><span data-stu-id="73cf6-279">Assembly</span></span></td>
<td><span data-ttu-id="73cf6-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="73cf6-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="73cf6-281">0</span><span class="sxs-lookup"><span data-stu-id="73cf6-281">0</span></span></td>
<td><span data-ttu-id="73cf6-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="73cf6-283">0,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="73cf6-284">Deník</span><span class="sxs-lookup"><span data-stu-id="73cf6-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="73cf6-285">Deník</span><span class="sxs-lookup"><span data-stu-id="73cf6-285">Journal</span></span></th>
<th><span data-ttu-id="73cf6-286">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="73cf6-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="73cf6-287">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="73cf6-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="73cf6-288">Verze</span><span class="sxs-lookup"><span data-stu-id="73cf6-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73cf6-289">00002</span><span class="sxs-lookup"><span data-stu-id="73cf6-289">00002</span></span></td>
<td><span data-ttu-id="73cf6-290">Deník výpočtu distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="73cf6-291">Fiskální</span><span class="sxs-lookup"><span data-stu-id="73cf6-291">Fiscal</span></span></td>
<td><span data-ttu-id="73cf6-292">2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-292">2017</span></span></td>
<td><span data-ttu-id="73cf6-293">Období 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-293">Period 1</span></span></td>
<td><span data-ttu-id="73cf6-294">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="73cf6-295">Položky deníku (Položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="73cf6-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="73cf6-296">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="73cf6-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="73cf6-297">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="73cf6-298">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-298">Cost element</span></span></th>
<th><span data-ttu-id="73cf6-299">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-299">Cost behavior</span></span></th>
<th><span data-ttu-id="73cf6-300">Částka</span><span class="sxs-lookup"><span data-stu-id="73cf6-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73cf6-301">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="73cf6-302">CC099</span><span class="sxs-lookup"><span data-stu-id="73cf6-302">CC099</span></span></td>
<td><span data-ttu-id="73cf6-303">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="73cf6-303">Default cost center</span></span></td>
<td><span data-ttu-id="73cf6-304">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-304">10001</span></span></td>
<td><span data-ttu-id="73cf6-305">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-305">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-306">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-306">Fixed cost</span></span></td>
<td><span data-ttu-id="73cf6-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-308">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="73cf6-309">CC099</span><span class="sxs-lookup"><span data-stu-id="73cf6-309">CC099</span></span></td>
<td><span data-ttu-id="73cf6-310">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="73cf6-310">Default cost center</span></span></td>
<td><span data-ttu-id="73cf6-311">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-311">10001</span></span></td>
<td><span data-ttu-id="73cf6-312">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-312">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-313">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-313">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="73cf6-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="73cf6-315">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73cf6-316">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="73cf6-317">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-317">Cost element</span></span></th>
<th><span data-ttu-id="73cf6-318">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-318">Cost behavior</span></span></th>
<th><span data-ttu-id="73cf6-319">Částka</span><span class="sxs-lookup"><span data-stu-id="73cf6-319">Amount</span></span></th>
<th><span data-ttu-id="73cf6-320">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="73cf6-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73cf6-321">CC099</span><span class="sxs-lookup"><span data-stu-id="73cf6-321">CC099</span></span></td>
<td><span data-ttu-id="73cf6-322">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="73cf6-322">Default cost center</span></span></td>
<td><span data-ttu-id="73cf6-323">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-323">10001</span></span></td>
<td><span data-ttu-id="73cf6-324">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-324">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-325">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-325">Fixed cost</span></span></td>
<td><span data-ttu-id="73cf6-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-326">-1,000.00</span></span></td>
<td><span data-ttu-id="73cf6-327">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-328">CC001</span><span class="sxs-lookup"><span data-stu-id="73cf6-328">CC001</span></span></td>
<td><span data-ttu-id="73cf6-329">HR</span><span class="sxs-lookup"><span data-stu-id="73cf6-329">HR</span></span></td>
<td><span data-ttu-id="73cf6-330">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-330">10001</span></span></td>
<td><span data-ttu-id="73cf6-331">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-331">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-332">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-332">Fixed cost</span></span></td>
<td><span data-ttu-id="73cf6-333">500.00</span><span class="sxs-lookup"><span data-stu-id="73cf6-333">500.00</span></span></td>
<td><span data-ttu-id="73cf6-334">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-335">CC002</span><span class="sxs-lookup"><span data-stu-id="73cf6-335">CC002</span></span></td>
<td><span data-ttu-id="73cf6-336">Finance</span><span class="sxs-lookup"><span data-stu-id="73cf6-336">Finance</span></span></td>
<td><span data-ttu-id="73cf6-337">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-337">10001</span></span></td>
<td><span data-ttu-id="73cf6-338">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-338">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-339">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-339">Fixed cost</span></span></td>
<td><span data-ttu-id="73cf6-340">500.00</span><span class="sxs-lookup"><span data-stu-id="73cf6-340">500.00</span></span></td>
<td><span data-ttu-id="73cf6-341">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-342">CC099</span><span class="sxs-lookup"><span data-stu-id="73cf6-342">CC099</span></span></td>
<td><span data-ttu-id="73cf6-343">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="73cf6-343">Default cost center</span></span></td>
<td><span data-ttu-id="73cf6-344">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-344">10001</span></span></td>
<td><span data-ttu-id="73cf6-345">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-345">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-346">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-346">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-347">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-347">-9,000.00</span></span></td>
<td><span data-ttu-id="73cf6-348">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-349">CC001</span><span class="sxs-lookup"><span data-stu-id="73cf6-349">CC001</span></span></td>
<td><span data-ttu-id="73cf6-350">HR</span><span class="sxs-lookup"><span data-stu-id="73cf6-350">HR</span></span></td>
<td><span data-ttu-id="73cf6-351">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-351">10001</span></span></td>
<td><span data-ttu-id="73cf6-352">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-352">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-353">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-353">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="73cf6-354">1,285.71</span></span></td>
<td><span data-ttu-id="73cf6-355">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-356">CC002</span><span class="sxs-lookup"><span data-stu-id="73cf6-356">CC002</span></span></td>
<td><span data-ttu-id="73cf6-357">Finance</span><span class="sxs-lookup"><span data-stu-id="73cf6-357">Finance</span></span></td>
<td><span data-ttu-id="73cf6-358">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-358">10001</span></span></td>
<td><span data-ttu-id="73cf6-359">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-359">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-360">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-360">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="73cf6-361">7,714.29</span></span></td>
<td><span data-ttu-id="73cf6-362">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="73cf6-363">Více informací naleznete v tématu [Vytvoření a přiřazení zásad distribuce nákladů k jednotce řízení nákladů](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="73cf6-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="73cf6-364">Krok 3: Zpracování výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="73cf6-365">Režijní náklady se používají k účtování jednoho nebo více konkrétních objektů nákladů.</span><span class="sxs-lookup"><span data-stu-id="73cf6-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="73cf6-366">Účtování je založeno na předem určené nákladové sazbě a množství z přiřazeného základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="73cf6-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="73cf6-367">Definice sazby režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-367">Define the overhead rate</span></span>

<span data-ttu-id="73cf6-368">Objekt nákladů CC001 HR přispívá k sadě interních projektů.</span><span class="sxs-lookup"><span data-stu-id="73cf6-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="73cf6-369">Vytvoří se člen statistické dimenzi s názvem projekty lidských zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="73cf6-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73cf6-370">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-370">Cost object</span></span></th>
<th><span data-ttu-id="73cf6-371">Pracovní doba</span><span class="sxs-lookup"><span data-stu-id="73cf6-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73cf6-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-372">Proj 1</span></span></td>
<td><span data-ttu-id="73cf6-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-373">Project 1</span></span></td>
<td><span data-ttu-id="73cf6-374">3</span><span class="sxs-lookup"><span data-stu-id="73cf6-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-375">Proj 2</span></span></td>
<td><span data-ttu-id="73cf6-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-376">Project 2</span></span></td>
<td><span data-ttu-id="73cf6-377">1</span><span class="sxs-lookup"><span data-stu-id="73cf6-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="73cf6-378">Byla definována předem určená nákladová sazba pro příspěvky k nákladovým projektům.</span><span class="sxs-lookup"><span data-stu-id="73cf6-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73cf6-379">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-379">Cost object</span></span></th>
<th><span data-ttu-id="73cf6-380">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-380">Cost element</span></span></th>
<th><span data-ttu-id="73cf6-381">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-381">Cost behavior</span></span></th>
<th><span data-ttu-id="73cf6-382">Jednotky</span><span class="sxs-lookup"><span data-stu-id="73cf6-382">Units</span></span></th>
<th><span data-ttu-id="73cf6-383">Kurz</span><span class="sxs-lookup"><span data-stu-id="73cf6-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73cf6-384">CC001</span><span class="sxs-lookup"><span data-stu-id="73cf6-384">CC001</span></span></td>
<td><span data-ttu-id="73cf6-385">HR</span><span class="sxs-lookup"><span data-stu-id="73cf6-385">HR</span></span></td>
<td><span data-ttu-id="73cf6-386">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-386">10001</span></span></td>
<td><span data-ttu-id="73cf6-387">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-387">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-388">1</span><span class="sxs-lookup"><span data-stu-id="73cf6-388">1</span></span></td>
<td><span data-ttu-id="73cf6-389">10</span><span class="sxs-lookup"><span data-stu-id="73cf6-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="73cf6-390">Následující tabulka zobrazuje výsledek při použití projektů lidských zdrojů jako základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="73cf6-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73cf6-391">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-391">Cost object</span></span></th>
<th><span data-ttu-id="73cf6-392">Hodnota</span><span class="sxs-lookup"><span data-stu-id="73cf6-392">Magnitude</span></span></th>
<th><span data-ttu-id="73cf6-393">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-393">Cost element</span></span></th>
<th><span data-ttu-id="73cf6-394">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="73cf6-394">Allocation factor</span></span></th>
<th><span data-ttu-id="73cf6-395">Částka</span><span class="sxs-lookup"><span data-stu-id="73cf6-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73cf6-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-396">Proj 1</span></span></td>
<td><span data-ttu-id="73cf6-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-397">Project 1</span></span></td>
<td><span data-ttu-id="73cf6-398">3</span><span class="sxs-lookup"><span data-stu-id="73cf6-398">3</span></span></td>
<td><span data-ttu-id="73cf6-399">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-399">10001</span></span></td>
<td><span data-ttu-id="73cf6-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="73cf6-401">30.00</span><span class="sxs-lookup"><span data-stu-id="73cf6-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-402">Proj 2</span></span></td>
<td><span data-ttu-id="73cf6-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-403">Project 2</span></span></td>
<td><span data-ttu-id="73cf6-404">1</span><span class="sxs-lookup"><span data-stu-id="73cf6-404">1</span></span></td>
<td><span data-ttu-id="73cf6-405">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-405">10001</span></span></td>
<td><span data-ttu-id="73cf6-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="73cf6-407">10,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="73cf6-408">Deník</span><span class="sxs-lookup"><span data-stu-id="73cf6-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="73cf6-409">Deník</span><span class="sxs-lookup"><span data-stu-id="73cf6-409">Journal</span></span></th>
<th><span data-ttu-id="73cf6-410">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="73cf6-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="73cf6-411">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="73cf6-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="73cf6-412">Verze</span><span class="sxs-lookup"><span data-stu-id="73cf6-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73cf6-413">00003</span><span class="sxs-lookup"><span data-stu-id="73cf6-413">00003</span></span></td>
<td><span data-ttu-id="73cf6-414">Deník výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="73cf6-415">Fiskální</span><span class="sxs-lookup"><span data-stu-id="73cf6-415">Fiscal</span></span></td>
<td><span data-ttu-id="73cf6-416">2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-416">2017</span></span></td>
<td><span data-ttu-id="73cf6-417">Období 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-417">Period 1</span></span></td>
<td><span data-ttu-id="73cf6-418">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="73cf6-419">Položky deníku (položky deníku pro výpočet sazby režijních nákladů)</span><span class="sxs-lookup"><span data-stu-id="73cf6-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="73cf6-420">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="73cf6-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="73cf6-421">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-421">Cost object</span></span></th>
<th><span data-ttu-id="73cf6-422">Hodnota</span><span class="sxs-lookup"><span data-stu-id="73cf6-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73cf6-423">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="73cf6-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-424">Proj 1</span></span></td>
<td><span data-ttu-id="73cf6-425">Interní projekt 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="73cf6-426">3,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-427">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="73cf6-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-428">Proj 2</span></span></td>
<td><span data-ttu-id="73cf6-429">Interní projekt 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="73cf6-430">1.00</span><span class="sxs-lookup"><span data-stu-id="73cf6-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="73cf6-431">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73cf6-432">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="73cf6-433">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-433">Cost element</span></span></th>
<th><span data-ttu-id="73cf6-434">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-434">Cost behavior</span></span></th>
<th><span data-ttu-id="73cf6-435">Částka</span><span class="sxs-lookup"><span data-stu-id="73cf6-435">Amount</span></span></th>
<th><span data-ttu-id="73cf6-436">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="73cf6-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73cf6-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="73cf6-437">CC0001</span></span></td>
<td><span data-ttu-id="73cf6-438">HR</span><span class="sxs-lookup"><span data-stu-id="73cf6-438">HR</span></span></td>
<td><span data-ttu-id="73cf6-439">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-439">10001</span></span></td>
<td><span data-ttu-id="73cf6-440">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-440">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-441">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-441">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-442">-30.00</span></span></td>
<td><span data-ttu-id="73cf6-443">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-444">Proj 1</span></span></td>
<td><span data-ttu-id="73cf6-445">Interní projekt 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="73cf6-446">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-446">10001</span></span></td>
<td><span data-ttu-id="73cf6-447">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-447">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-448">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-448">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-449">30.00</span><span class="sxs-lookup"><span data-stu-id="73cf6-449">30.00</span></span></td>
<td><span data-ttu-id="73cf6-450">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-451">CC001</span><span class="sxs-lookup"><span data-stu-id="73cf6-451">CC001</span></span></td>
<td><span data-ttu-id="73cf6-452">HR</span><span class="sxs-lookup"><span data-stu-id="73cf6-452">HR</span></span></td>
<td><span data-ttu-id="73cf6-453">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-453">10001</span></span></td>
<td><span data-ttu-id="73cf6-454">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-454">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-455">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-455">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-456">-10.00</span></span></td>
<td><span data-ttu-id="73cf6-457">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-458">Proj 2</span></span></td>
<td><span data-ttu-id="73cf6-459">Interní projekt 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="73cf6-460">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-460">10001</span></span></td>
<td><span data-ttu-id="73cf6-461">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-461">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-462">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-462">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-463">10.00</span><span class="sxs-lookup"><span data-stu-id="73cf6-463">10.00</span></span></td>
<td><span data-ttu-id="73cf6-464">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="73cf6-465">Další informace naleznete v tématu [Provedení výpočtu režijních nákladů](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="73cf6-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="73cf6-466">Krok 4: Zpracování výpočtu přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="73cf6-467">Přidělení se používá k přidělení zůstatku objektu nákladů do jiných objektů nákladů použitím základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="73cf6-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="73cf6-468">Aplikace Finance podporuje reciproční metodu přidělování.</span><span class="sxs-lookup"><span data-stu-id="73cf6-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="73cf6-469">V metodě vzájemného přidělení jsou plně rozpoznány vzájemné služby, které si vyměňují pomocné objekty nákladů.</span><span class="sxs-lookup"><span data-stu-id="73cf6-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="73cf6-470">Systém automaticky určí provádění přidělení ve správném pořadí.</span><span class="sxs-lookup"><span data-stu-id="73cf6-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="73cf6-471">Zůstatek objektu nákladů je přidělen jedním základem přidělení.</span><span class="sxs-lookup"><span data-stu-id="73cf6-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="73cf6-472">Je podporováno přidělování napříč dimenzemi objektů nákladů a jejich příslušných členů.</span><span class="sxs-lookup"><span data-stu-id="73cf6-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="73cf6-473">Pořadí přidělení je řízeno jednotkou řízení nákladů.</span><span class="sxs-lookup"><span data-stu-id="73cf6-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="73cf6-474">[![Reciproční metoda](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="73cf6-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="73cf6-475">Definice přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-475">Define the cost allocation</span></span>

<span data-ttu-id="73cf6-476">Toto je jednoduchý příklad, který vysvětluje, jakým způsobem lze sledovat tok nákladů.</span><span class="sxs-lookup"><span data-stu-id="73cf6-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="73cf6-477">Objekt nákladů objektu CC001 HR přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="73cf6-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="73cf6-478">Vytvoří se člen statistické dimenzi s názvem služby lidských zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="73cf6-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73cf6-479">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-479">Cost object</span></span></th>
<th><span data-ttu-id="73cf6-480">Služby HR</span><span class="sxs-lookup"><span data-stu-id="73cf6-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73cf6-481">CC002</span><span class="sxs-lookup"><span data-stu-id="73cf6-481">CC002</span></span></td>
<td><span data-ttu-id="73cf6-482">Finance</span><span class="sxs-lookup"><span data-stu-id="73cf6-482">Finance</span></span></td>
<td><span data-ttu-id="73cf6-483">35</span><span class="sxs-lookup"><span data-stu-id="73cf6-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-484">CC003</span><span class="sxs-lookup"><span data-stu-id="73cf6-484">CC003</span></span></td>
<td><span data-ttu-id="73cf6-485">Sestavení</span><span class="sxs-lookup"><span data-stu-id="73cf6-485">Assembly</span></span></td>
<td><span data-ttu-id="73cf6-486">55</span><span class="sxs-lookup"><span data-stu-id="73cf6-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-487">CC004</span><span class="sxs-lookup"><span data-stu-id="73cf6-487">CC004</span></span></td>
<td><span data-ttu-id="73cf6-488">Balení</span><span class="sxs-lookup"><span data-stu-id="73cf6-488">Packaging</span></span></td>
<td><span data-ttu-id="73cf6-489">10</span><span class="sxs-lookup"><span data-stu-id="73cf6-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="73cf6-490">Objekt nákladů objektu CC002 Finance přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="73cf6-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="73cf6-491">Vytvoří se člen statistické dimenzi s názvem Finanční služby k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="73cf6-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73cf6-492">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-492">Cost object</span></span></th>
<th><span data-ttu-id="73cf6-493">Finanční služby</span><span class="sxs-lookup"><span data-stu-id="73cf6-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73cf6-494">CC003</span><span class="sxs-lookup"><span data-stu-id="73cf6-494">CC003</span></span></td>
<td><span data-ttu-id="73cf6-495">Sestavení</span><span class="sxs-lookup"><span data-stu-id="73cf6-495">Assembly</span></span></td>
<td><span data-ttu-id="73cf6-496">65</span><span class="sxs-lookup"><span data-stu-id="73cf6-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-497">CC004</span><span class="sxs-lookup"><span data-stu-id="73cf6-497">CC004</span></span></td>
<td><span data-ttu-id="73cf6-498">Balení</span><span class="sxs-lookup"><span data-stu-id="73cf6-498">Packaging</span></span></td>
<td><span data-ttu-id="73cf6-499">35</span><span class="sxs-lookup"><span data-stu-id="73cf6-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="73cf6-500">Objekt nákladů objektu CC003 Sestavení přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="73cf6-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="73cf6-501">Vytvoří se člen statistické dimenzi s názvem Služby sestavení zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="73cf6-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73cf6-502">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-502">Cost object</span></span></th>
<th><span data-ttu-id="73cf6-503">Služby sestavení (v hodinách)</span><span class="sxs-lookup"><span data-stu-id="73cf6-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73cf6-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-504">Prod 1</span></span></td>
<td><span data-ttu-id="73cf6-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-505">Product 1</span></span></td>
<td><span data-ttu-id="73cf6-506">60</span><span class="sxs-lookup"><span data-stu-id="73cf6-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-507">Prod 2</span></span></td>
<td><span data-ttu-id="73cf6-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-508">Product 2</span></span></td>
<td><span data-ttu-id="73cf6-509">20</span><span class="sxs-lookup"><span data-stu-id="73cf6-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="73cf6-510">Objekt nákladů objektu CC004 Balení přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="73cf6-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="73cf6-511">Vytvoří se člen statistické dimenzi s názvem Služby balení k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="73cf6-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73cf6-512">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-512">Cost object</span></span></th>
<th><span data-ttu-id="73cf6-513">Služby balení (v hodinách)</span><span class="sxs-lookup"><span data-stu-id="73cf6-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73cf6-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-514">Prod 1</span></span></td>
<td><span data-ttu-id="73cf6-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-515">Product 1</span></span></td>
<td><span data-ttu-id="73cf6-516">80</span><span class="sxs-lookup"><span data-stu-id="73cf6-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-517">Prod 2</span></span></td>
<td><span data-ttu-id="73cf6-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-518">Product 2</span></span></td>
<td><span data-ttu-id="73cf6-519">15</span><span class="sxs-lookup"><span data-stu-id="73cf6-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="73cf6-520">Statistická měření, jako je například výrobní doba spotřebovaná produktem, lze odvodit z datového zdroje.</span><span class="sxs-lookup"><span data-stu-id="73cf6-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="73cf6-521">Více informací naleznete v části [Šablona poskytovatele statistického měření](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="73cf6-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="73cf6-522">V následující tabulce je uveden výsledek při použití služeb HR jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="73cf6-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73cf6-523">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-523">Cost object</span></span></th>
<th><span data-ttu-id="73cf6-524">Hodnota</span><span class="sxs-lookup"><span data-stu-id="73cf6-524">Magnitude</span></span></th>
<th><span data-ttu-id="73cf6-525">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="73cf6-525">Allocation factor</span></span></th>
<th><span data-ttu-id="73cf6-526">Částka</span><span class="sxs-lookup"><span data-stu-id="73cf6-526">Amount</span></span></th>
<th><span data-ttu-id="73cf6-527">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73cf6-528">CC002</span><span class="sxs-lookup"><span data-stu-id="73cf6-528">CC002</span></span></td>
<td><span data-ttu-id="73cf6-529">Finance</span><span class="sxs-lookup"><span data-stu-id="73cf6-529">Finance</span></span></td>
<td><span data-ttu-id="73cf6-530">35</span><span class="sxs-lookup"><span data-stu-id="73cf6-530">35</span></span></td>
<td><span data-ttu-id="73cf6-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="73cf6-532">175.00</span><span class="sxs-lookup"><span data-stu-id="73cf6-532">175.00</span></span></td>
<td><span data-ttu-id="73cf6-533">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-534">CC003</span><span class="sxs-lookup"><span data-stu-id="73cf6-534">CC003</span></span></td>
<td><span data-ttu-id="73cf6-535">Sestavení</span><span class="sxs-lookup"><span data-stu-id="73cf6-535">Assembly</span></span></td>
<td><span data-ttu-id="73cf6-536">55</span><span class="sxs-lookup"><span data-stu-id="73cf6-536">55</span></span></td>
<td><span data-ttu-id="73cf6-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="73cf6-538">275.00</span><span class="sxs-lookup"><span data-stu-id="73cf6-538">275.00</span></span></td>
<td><span data-ttu-id="73cf6-539">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-540">CC004</span><span class="sxs-lookup"><span data-stu-id="73cf6-540">CC004</span></span></td>
<td><span data-ttu-id="73cf6-541">Balení</span><span class="sxs-lookup"><span data-stu-id="73cf6-541">Packaging</span></span></td>
<td><span data-ttu-id="73cf6-542">10</span><span class="sxs-lookup"><span data-stu-id="73cf6-542">10</span></span></td>
<td><span data-ttu-id="73cf6-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="73cf6-544">50,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-544">50.00</span></span></td>
<td><span data-ttu-id="73cf6-545">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-546">CC002</span><span class="sxs-lookup"><span data-stu-id="73cf6-546">CC002</span></span></td>
<td><span data-ttu-id="73cf6-547">Finance</span><span class="sxs-lookup"><span data-stu-id="73cf6-547">Finance</span></span></td>
<td><span data-ttu-id="73cf6-548">35</span><span class="sxs-lookup"><span data-stu-id="73cf6-548">35</span></span></td>
<td><span data-ttu-id="73cf6-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="73cf6-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="73cf6-550">436.00</span><span class="sxs-lookup"><span data-stu-id="73cf6-550">436.00</span></span></td>
<td><span data-ttu-id="73cf6-551">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-552">CC003</span><span class="sxs-lookup"><span data-stu-id="73cf6-552">CC003</span></span></td>
<td><span data-ttu-id="73cf6-553">Sestavení</span><span class="sxs-lookup"><span data-stu-id="73cf6-553">Assembly</span></span></td>
<td><span data-ttu-id="73cf6-554">55</span><span class="sxs-lookup"><span data-stu-id="73cf6-554">55</span></span></td>
<td><span data-ttu-id="73cf6-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="73cf6-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="73cf6-556">685.14</span><span class="sxs-lookup"><span data-stu-id="73cf6-556">685.14</span></span></td>
<td><span data-ttu-id="73cf6-557">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-558">CC004</span><span class="sxs-lookup"><span data-stu-id="73cf6-558">CC004</span></span></td>
<td><span data-ttu-id="73cf6-559">Balení</span><span class="sxs-lookup"><span data-stu-id="73cf6-559">Packaging</span></span></td>
<td><span data-ttu-id="73cf6-560">10</span><span class="sxs-lookup"><span data-stu-id="73cf6-560">10</span></span></td>
<td><span data-ttu-id="73cf6-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="73cf6-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="73cf6-562">124.57</span><span class="sxs-lookup"><span data-stu-id="73cf6-562">124.57</span></span></td>
<td><span data-ttu-id="73cf6-563">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="73cf6-564">V následující tabulce je uveden výsledek při použití Finančních služeb Finance jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="73cf6-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73cf6-565">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-565">Cost object</span></span></th>
<th><span data-ttu-id="73cf6-566">Hodnota</span><span class="sxs-lookup"><span data-stu-id="73cf6-566">Magnitude</span></span></th>
<th><span data-ttu-id="73cf6-567">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="73cf6-567">Allocation factor</span></span></th>
<th><span data-ttu-id="73cf6-568">Částka</span><span class="sxs-lookup"><span data-stu-id="73cf6-568">Amount</span></span></th>
<th><span data-ttu-id="73cf6-569">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73cf6-570">CC003</span><span class="sxs-lookup"><span data-stu-id="73cf6-570">CC003</span></span></td>
<td><span data-ttu-id="73cf6-571">Sestavení</span><span class="sxs-lookup"><span data-stu-id="73cf6-571">Assembly</span></span></td>
<td><span data-ttu-id="73cf6-572">65</span><span class="sxs-lookup"><span data-stu-id="73cf6-572">65</span></span></td>
<td><span data-ttu-id="73cf6-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="73cf6-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="73cf6-574">438.75</span><span class="sxs-lookup"><span data-stu-id="73cf6-574">438.75</span></span></td>
<td><span data-ttu-id="73cf6-575">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-576">CC004</span><span class="sxs-lookup"><span data-stu-id="73cf6-576">CC004</span></span></td>
<td><span data-ttu-id="73cf6-577">Balení</span><span class="sxs-lookup"><span data-stu-id="73cf6-577">Packaging</span></span></td>
<td><span data-ttu-id="73cf6-578">35</span><span class="sxs-lookup"><span data-stu-id="73cf6-578">35</span></span></td>
<td><span data-ttu-id="73cf6-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="73cf6-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="73cf6-580">236.25</span><span class="sxs-lookup"><span data-stu-id="73cf6-580">236.25</span></span></td>
<td><span data-ttu-id="73cf6-581">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-582">CC003</span><span class="sxs-lookup"><span data-stu-id="73cf6-582">CC003</span></span></td>
<td><span data-ttu-id="73cf6-583">Sestavení</span><span class="sxs-lookup"><span data-stu-id="73cf6-583">Assembly</span></span></td>
<td><span data-ttu-id="73cf6-584">65</span><span class="sxs-lookup"><span data-stu-id="73cf6-584">65</span></span></td>
<td><span data-ttu-id="73cf6-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="73cf6-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="73cf6-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="73cf6-586">5,297.69</span></span></td>
<td><span data-ttu-id="73cf6-587">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-588">CC004</span><span class="sxs-lookup"><span data-stu-id="73cf6-588">CC004</span></span></td>
<td><span data-ttu-id="73cf6-589">Balení</span><span class="sxs-lookup"><span data-stu-id="73cf6-589">Packaging</span></span></td>
<td><span data-ttu-id="73cf6-590">35</span><span class="sxs-lookup"><span data-stu-id="73cf6-590">35</span></span></td>
<td><span data-ttu-id="73cf6-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="73cf6-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="73cf6-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="73cf6-592">2,852.60</span></span></td>
<td><span data-ttu-id="73cf6-593">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="73cf6-594">V následující tabulce je uveden výsledek při použití Služeb sestavení jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="73cf6-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73cf6-595">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-595">Cost object</span></span></th>
<th><span data-ttu-id="73cf6-596">Hodnota</span><span class="sxs-lookup"><span data-stu-id="73cf6-596">Magnitude</span></span></th>
<th><span data-ttu-id="73cf6-597">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="73cf6-597">Allocation factor</span></span></th>
<th><span data-ttu-id="73cf6-598">Částka</span><span class="sxs-lookup"><span data-stu-id="73cf6-598">Amount</span></span></th>
<th><span data-ttu-id="73cf6-599">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73cf6-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-600">Prod 1</span></span></td>
<td><span data-ttu-id="73cf6-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-601">Product 1</span></span></td>
<td><span data-ttu-id="73cf6-602">60</span><span class="sxs-lookup"><span data-stu-id="73cf6-602">60</span></span></td>
<td><span data-ttu-id="73cf6-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="73cf6-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="73cf6-604">535.31</span><span class="sxs-lookup"><span data-stu-id="73cf6-604">535.31</span></span></td>
<td><span data-ttu-id="73cf6-605">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-606">Prod 2</span></span></td>
<td><span data-ttu-id="73cf6-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-607">Product 2</span></span></td>
<td><span data-ttu-id="73cf6-608">20</span><span class="sxs-lookup"><span data-stu-id="73cf6-608">20</span></span></td>
<td><span data-ttu-id="73cf6-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="73cf6-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="73cf6-610">178.44</span><span class="sxs-lookup"><span data-stu-id="73cf6-610">178.44</span></span></td>
<td><span data-ttu-id="73cf6-611">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-612">Prod 1</span></span></td>
<td><span data-ttu-id="73cf6-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-613">Product 1</span></span></td>
<td><span data-ttu-id="73cf6-614">60</span><span class="sxs-lookup"><span data-stu-id="73cf6-614">60</span></span></td>
<td><span data-ttu-id="73cf6-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="73cf6-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="73cf6-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="73cf6-616">4,487.12</span></span></td>
<td><span data-ttu-id="73cf6-617">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-618">Prod 2</span></span></td>
<td><span data-ttu-id="73cf6-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-619">Product 2</span></span></td>
<td><span data-ttu-id="73cf6-620">20</span><span class="sxs-lookup"><span data-stu-id="73cf6-620">20</span></span></td>
<td><span data-ttu-id="73cf6-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="73cf6-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="73cf6-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="73cf6-622">1,495.71</span></span></td>
<td><span data-ttu-id="73cf6-623">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="73cf6-624">V následující tabulce je uveden výsledek při použití Služeb balení jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="73cf6-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73cf6-625">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-625">Cost object</span></span></th>
<th><span data-ttu-id="73cf6-626">Hodnota</span><span class="sxs-lookup"><span data-stu-id="73cf6-626">Magnitude</span></span></th>
<th><span data-ttu-id="73cf6-627">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="73cf6-627">Allocation factor</span></span></th>
<th><span data-ttu-id="73cf6-628">Částka</span><span class="sxs-lookup"><span data-stu-id="73cf6-628">Amount</span></span></th>
<th><span data-ttu-id="73cf6-629">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73cf6-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-630">Prod 1</span></span></td>
<td><span data-ttu-id="73cf6-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-631">Product 1</span></span></td>
<td><span data-ttu-id="73cf6-632">80</span><span class="sxs-lookup"><span data-stu-id="73cf6-632">80</span></span></td>
<td><span data-ttu-id="73cf6-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="73cf6-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="73cf6-634">241.05</span><span class="sxs-lookup"><span data-stu-id="73cf6-634">241.05</span></span></td>
<td><span data-ttu-id="73cf6-635">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-636">Prod 2</span></span></td>
<td><span data-ttu-id="73cf6-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-637">Product 2</span></span></td>
<td><span data-ttu-id="73cf6-638">15</span><span class="sxs-lookup"><span data-stu-id="73cf6-638">15</span></span></td>
<td><span data-ttu-id="73cf6-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="73cf6-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="73cf6-640">45.20</span><span class="sxs-lookup"><span data-stu-id="73cf6-640">45.20</span></span></td>
<td><span data-ttu-id="73cf6-641">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-642">Prod 1</span></span></td>
<td><span data-ttu-id="73cf6-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-643">Product 1</span></span></td>
<td><span data-ttu-id="73cf6-644">80</span><span class="sxs-lookup"><span data-stu-id="73cf6-644">80</span></span></td>
<td><span data-ttu-id="73cf6-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="73cf6-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="73cf6-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="73cf6-646">2,507.09</span></span></td>
<td><span data-ttu-id="73cf6-647">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-648">Prod 2</span></span></td>
<td><span data-ttu-id="73cf6-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-649">Product 2</span></span></td>
<td><span data-ttu-id="73cf6-650">15</span><span class="sxs-lookup"><span data-stu-id="73cf6-650">15</span></span></td>
<td><span data-ttu-id="73cf6-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="73cf6-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="73cf6-652">470.08</span><span class="sxs-lookup"><span data-stu-id="73cf6-652">470.08</span></span></td>
<td><span data-ttu-id="73cf6-653">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="73cf6-654">Položky deníku (položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="73cf6-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="73cf6-655">Deník</span><span class="sxs-lookup"><span data-stu-id="73cf6-655">Journal</span></span></th>
<th><span data-ttu-id="73cf6-656">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="73cf6-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="73cf6-657">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="73cf6-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="73cf6-658">Verze</span><span class="sxs-lookup"><span data-stu-id="73cf6-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73cf6-659">00004</span><span class="sxs-lookup"><span data-stu-id="73cf6-659">00004</span></span></td>
<td><span data-ttu-id="73cf6-660">Deník přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="73cf6-661">Fiskální</span><span class="sxs-lookup"><span data-stu-id="73cf6-661">Fiscal</span></span></td>
<td><span data-ttu-id="73cf6-662">2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-662">2017</span></span></td>
<td><span data-ttu-id="73cf6-663">Období 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-663">Period 1</span></span></td>
<td><span data-ttu-id="73cf6-664">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="73cf6-665">Řádky deníku</span><span class="sxs-lookup"><span data-stu-id="73cf6-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="73cf6-666">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="73cf6-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="73cf6-667">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="73cf6-668">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-668">Cost element</span></span></th>
<th><span data-ttu-id="73cf6-669">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-669">Cost behavior</span></span></th>
<th><span data-ttu-id="73cf6-670">Částka</span><span class="sxs-lookup"><span data-stu-id="73cf6-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73cf6-671">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="73cf6-672">CC001</span><span class="sxs-lookup"><span data-stu-id="73cf6-672">CC001</span></span></td>
<td><span data-ttu-id="73cf6-673">HR</span><span class="sxs-lookup"><span data-stu-id="73cf6-673">HR</span></span></td>
<td><span data-ttu-id="73cf6-674">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-674">10001</span></span></td>
<td><span data-ttu-id="73cf6-675">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-675">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-676">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-676">Fixed cost</span></span></td>
<td><span data-ttu-id="73cf6-677">500.00</span><span class="sxs-lookup"><span data-stu-id="73cf6-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-678">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="73cf6-679">CC001</span><span class="sxs-lookup"><span data-stu-id="73cf6-679">CC001</span></span></td>
<td><span data-ttu-id="73cf6-680">HR</span><span class="sxs-lookup"><span data-stu-id="73cf6-680">HR</span></span></td>
<td><span data-ttu-id="73cf6-681">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-681">10001</span></span></td>
<td><span data-ttu-id="73cf6-682">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-682">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-683">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-683">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="73cf6-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-685">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="73cf6-686">CC002</span><span class="sxs-lookup"><span data-stu-id="73cf6-686">CC002</span></span></td>
<td><span data-ttu-id="73cf6-687">Finance</span><span class="sxs-lookup"><span data-stu-id="73cf6-687">Finance</span></span></td>
<td><span data-ttu-id="73cf6-688">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-688">10001</span></span></td>
<td><span data-ttu-id="73cf6-689">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-689">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-690">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-690">Fixed cost</span></span></td>
<td><span data-ttu-id="73cf6-691">675.00</span><span class="sxs-lookup"><span data-stu-id="73cf6-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-692">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="73cf6-693">CC002</span><span class="sxs-lookup"><span data-stu-id="73cf6-693">CC002</span></span></td>
<td><span data-ttu-id="73cf6-694">Finance</span><span class="sxs-lookup"><span data-stu-id="73cf6-694">Finance</span></span></td>
<td><span data-ttu-id="73cf6-695">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-695">10001</span></span></td>
<td><span data-ttu-id="73cf6-696">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-696">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-697">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-697">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="73cf6-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-699">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="73cf6-700">CC003</span><span class="sxs-lookup"><span data-stu-id="73cf6-700">CC003</span></span></td>
<td><span data-ttu-id="73cf6-701">Sestavení</span><span class="sxs-lookup"><span data-stu-id="73cf6-701">Assembly</span></span></td>
<td><span data-ttu-id="73cf6-702">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-702">10001</span></span></td>
<td><span data-ttu-id="73cf6-703">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-703">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-704">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-704">Fixed cost</span></span></td>
<td><span data-ttu-id="73cf6-705">713.75</span><span class="sxs-lookup"><span data-stu-id="73cf6-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-706">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="73cf6-707">CC003</span><span class="sxs-lookup"><span data-stu-id="73cf6-707">CC003</span></span></td>
<td><span data-ttu-id="73cf6-708">Sestavení</span><span class="sxs-lookup"><span data-stu-id="73cf6-708">Assembly</span></span></td>
<td><span data-ttu-id="73cf6-709">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-709">10001</span></span></td>
<td><span data-ttu-id="73cf6-710">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-710">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-711">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-711">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="73cf6-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-713">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="73cf6-714">CC003</span><span class="sxs-lookup"><span data-stu-id="73cf6-714">CC003</span></span></td>
<td><span data-ttu-id="73cf6-715">Balení</span><span class="sxs-lookup"><span data-stu-id="73cf6-715">Packaging</span></span></td>
<td><span data-ttu-id="73cf6-716">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-716">10001</span></span></td>
<td><span data-ttu-id="73cf6-717">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-717">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-718">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-718">Fixed cost</span></span></td>
<td><span data-ttu-id="73cf6-719">286.25</span><span class="sxs-lookup"><span data-stu-id="73cf6-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-720">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="73cf6-721">CC003</span><span class="sxs-lookup"><span data-stu-id="73cf6-721">CC003</span></span></td>
<td><span data-ttu-id="73cf6-722">Balení</span><span class="sxs-lookup"><span data-stu-id="73cf6-722">Packaging</span></span></td>
<td><span data-ttu-id="73cf6-723">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-723">10001</span></span></td>
<td><span data-ttu-id="73cf6-724">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-724">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-725">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-725">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="73cf6-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-727">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="73cf6-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-728">Prod 1</span></span></td>
<td><span data-ttu-id="73cf6-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-729">Product 1</span></span></td>
<td><span data-ttu-id="73cf6-730">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-730">10001</span></span></td>
<td><span data-ttu-id="73cf6-731">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-731">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-732">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-732">Fixed cost</span></span></td>
<td><span data-ttu-id="73cf6-733">776.36</span><span class="sxs-lookup"><span data-stu-id="73cf6-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-734">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="73cf6-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-735">Prod 1</span></span></td>
<td><span data-ttu-id="73cf6-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-736">Product 1</span></span></td>
<td><span data-ttu-id="73cf6-737">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-737">10001</span></span></td>
<td><span data-ttu-id="73cf6-738">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-738">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-739">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-739">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="73cf6-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-741">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="73cf6-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-742">Prod 2</span></span></td>
<td><span data-ttu-id="73cf6-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-743">Product 1</span></span></td>
<td><span data-ttu-id="73cf6-744">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-744">10001</span></span></td>
<td><span data-ttu-id="73cf6-745">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-745">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-746">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-746">Fixed cost</span></span></td>
<td><span data-ttu-id="73cf6-747">223.64</span><span class="sxs-lookup"><span data-stu-id="73cf6-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-748">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="73cf6-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-749">Prod 2</span></span></td>
<td><span data-ttu-id="73cf6-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-750">Product 1</span></span></td>
<td><span data-ttu-id="73cf6-751">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-751">10001</span></span></td>
<td><span data-ttu-id="73cf6-752">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-752">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-753">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-753">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="73cf6-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="73cf6-755">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73cf6-756">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="73cf6-757">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-757">Cost element</span></span></th>
<th><span data-ttu-id="73cf6-758">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-758">Cost behavior</span></span></th>
<th><span data-ttu-id="73cf6-759">Částka</span><span class="sxs-lookup"><span data-stu-id="73cf6-759">Amount</span></span></th>
<th><span data-ttu-id="73cf6-760">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="73cf6-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73cf6-761">CC001</span><span class="sxs-lookup"><span data-stu-id="73cf6-761">CC001</span></span></td>
<td><span data-ttu-id="73cf6-762">HR</span><span class="sxs-lookup"><span data-stu-id="73cf6-762">HR</span></span></td>
<td><span data-ttu-id="73cf6-763">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-763">10001</span></span></td>
<td><span data-ttu-id="73cf6-764">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-764">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-765">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-765">Fixed cost</span></span></td>
<td><span data-ttu-id="73cf6-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-766">-500.00</span></span></td>
<td><span data-ttu-id="73cf6-767">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-768">CC002</span><span class="sxs-lookup"><span data-stu-id="73cf6-768">CC002</span></span></td>
<td><span data-ttu-id="73cf6-769">Finance</span><span class="sxs-lookup"><span data-stu-id="73cf6-769">Finance</span></span></td>
<td><span data-ttu-id="73cf6-770">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-770">10001</span></span></td>
<td><span data-ttu-id="73cf6-771">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-771">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-772">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-772">Fixed cost</span></span></td>
<td><span data-ttu-id="73cf6-773">175.00</span><span class="sxs-lookup"><span data-stu-id="73cf6-773">175.00</span></span></td>
<td><span data-ttu-id="73cf6-774">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-775">CC003</span><span class="sxs-lookup"><span data-stu-id="73cf6-775">CC003</span></span></td>
<td><span data-ttu-id="73cf6-776">Sestavení</span><span class="sxs-lookup"><span data-stu-id="73cf6-776">Assembly</span></span></td>
<td><span data-ttu-id="73cf6-777">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-777">10001</span></span></td>
<td><span data-ttu-id="73cf6-778">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-778">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-779">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-779">Fixed cost</span></span></td>
<td><span data-ttu-id="73cf6-780">275.00</span><span class="sxs-lookup"><span data-stu-id="73cf6-780">275.00</span></span></td>
<td><span data-ttu-id="73cf6-781">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-782">CC004</span><span class="sxs-lookup"><span data-stu-id="73cf6-782">CC004</span></span></td>
<td><span data-ttu-id="73cf6-783">Balení</span><span class="sxs-lookup"><span data-stu-id="73cf6-783">Packaging</span></span></td>
<td><span data-ttu-id="73cf6-784">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-784">10001</span></span></td>
<td><span data-ttu-id="73cf6-785">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-785">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-786">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-786">Fixed cost</span></span></td>
<td><span data-ttu-id="73cf6-787">50,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-787">50,00</span></span></td>
<td><span data-ttu-id="73cf6-788">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-789">CC001</span><span class="sxs-lookup"><span data-stu-id="73cf6-789">CC001</span></span></td>
<td><span data-ttu-id="73cf6-790">HR</span><span class="sxs-lookup"><span data-stu-id="73cf6-790">HR</span></span></td>
<td><span data-ttu-id="73cf6-791">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-791">10001</span></span></td>
<td><span data-ttu-id="73cf6-792">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-792">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-793">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-793">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-794">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="73cf6-794">-1,245.71</span></span></td>
<td><span data-ttu-id="73cf6-795">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-796">CC002</span><span class="sxs-lookup"><span data-stu-id="73cf6-796">CC002</span></span></td>
<td><span data-ttu-id="73cf6-797">Finance</span><span class="sxs-lookup"><span data-stu-id="73cf6-797">Finance</span></span></td>
<td><span data-ttu-id="73cf6-798">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-798">10001</span></span></td>
<td><span data-ttu-id="73cf6-799">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-799">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-800">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-800">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-801">436.00</span><span class="sxs-lookup"><span data-stu-id="73cf6-801">436.00</span></span></td>
<td><span data-ttu-id="73cf6-802">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-803">CC003</span><span class="sxs-lookup"><span data-stu-id="73cf6-803">CC003</span></span></td>
<td><span data-ttu-id="73cf6-804">Sestavení</span><span class="sxs-lookup"><span data-stu-id="73cf6-804">Assembly</span></span></td>
<td><span data-ttu-id="73cf6-805">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-805">10001</span></span></td>
<td><span data-ttu-id="73cf6-806">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-806">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-807">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-807">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-808">685.14</span><span class="sxs-lookup"><span data-stu-id="73cf6-808">685.14</span></span></td>
<td><span data-ttu-id="73cf6-809">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-810">CC004</span><span class="sxs-lookup"><span data-stu-id="73cf6-810">CC004</span></span></td>
<td><span data-ttu-id="73cf6-811">Balení</span><span class="sxs-lookup"><span data-stu-id="73cf6-811">Packaging</span></span></td>
<td><span data-ttu-id="73cf6-812">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-812">10001</span></span></td>
<td><span data-ttu-id="73cf6-813">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-813">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-814">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-814">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-815">124.57</span><span class="sxs-lookup"><span data-stu-id="73cf6-815">124.57</span></span></td>
<td><span data-ttu-id="73cf6-816">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-817">CC002</span><span class="sxs-lookup"><span data-stu-id="73cf6-817">CC002</span></span></td>
<td><span data-ttu-id="73cf6-818">Finance</span><span class="sxs-lookup"><span data-stu-id="73cf6-818">Finance</span></span></td>
<td><span data-ttu-id="73cf6-819">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-819">10001</span></span></td>
<td><span data-ttu-id="73cf6-820">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-820">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-821">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-821">Fixed cost</span></span></td>
<td><span data-ttu-id="73cf6-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-822">-675.00</span></span></td>
<td><span data-ttu-id="73cf6-823">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-824">CC003</span><span class="sxs-lookup"><span data-stu-id="73cf6-824">CC003</span></span></td>
<td><span data-ttu-id="73cf6-825">Sestavení</span><span class="sxs-lookup"><span data-stu-id="73cf6-825">Assembly</span></span></td>
<td><span data-ttu-id="73cf6-826">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-826">10001</span></span></td>
<td><span data-ttu-id="73cf6-827">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-827">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-828">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-828">Fixed cost</span></span></td>
<td><span data-ttu-id="73cf6-829">438.75</span><span class="sxs-lookup"><span data-stu-id="73cf6-829">438.75</span></span></td>
<td><span data-ttu-id="73cf6-830">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-831">CC004</span><span class="sxs-lookup"><span data-stu-id="73cf6-831">CC004</span></span></td>
<td><span data-ttu-id="73cf6-832">Balení</span><span class="sxs-lookup"><span data-stu-id="73cf6-832">Packaging</span></span></td>
<td><span data-ttu-id="73cf6-833">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-833">10001</span></span></td>
<td><span data-ttu-id="73cf6-834">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-834">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-835">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-835">Fixed cost</span></span></td>
<td><span data-ttu-id="73cf6-836">236.25</span><span class="sxs-lookup"><span data-stu-id="73cf6-836">236.25</span></span></td>
<td><span data-ttu-id="73cf6-837">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-838">CC002</span><span class="sxs-lookup"><span data-stu-id="73cf6-838">CC002</span></span></td>
<td><span data-ttu-id="73cf6-839">Finance</span><span class="sxs-lookup"><span data-stu-id="73cf6-839">Finance</span></span></td>
<td><span data-ttu-id="73cf6-840">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-840">10001</span></span></td>
<td><span data-ttu-id="73cf6-841">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-841">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-842">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-842">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-843">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="73cf6-843">-8,150.29</span></span></td>
<td><span data-ttu-id="73cf6-844">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-845">CC003</span><span class="sxs-lookup"><span data-stu-id="73cf6-845">CC003</span></span></td>
<td><span data-ttu-id="73cf6-846">Sestavení</span><span class="sxs-lookup"><span data-stu-id="73cf6-846">Assembly</span></span></td>
<td><span data-ttu-id="73cf6-847">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-847">10001</span></span></td>
<td><span data-ttu-id="73cf6-848">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-848">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-849">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-849">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="73cf6-850">5,297.69</span></span></td>
<td><span data-ttu-id="73cf6-851">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-852">CC004</span><span class="sxs-lookup"><span data-stu-id="73cf6-852">CC004</span></span></td>
<td><span data-ttu-id="73cf6-853">Balení</span><span class="sxs-lookup"><span data-stu-id="73cf6-853">Packaging</span></span></td>
<td><span data-ttu-id="73cf6-854">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-854">10001</span></span></td>
<td><span data-ttu-id="73cf6-855">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-855">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-856">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-856">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="73cf6-857">2,852.60</span></span></td>
<td><span data-ttu-id="73cf6-858">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-859">CC003</span><span class="sxs-lookup"><span data-stu-id="73cf6-859">CC003</span></span></td>
<td><span data-ttu-id="73cf6-860">Sestavení</span><span class="sxs-lookup"><span data-stu-id="73cf6-860">Assembly</span></span></td>
<td><span data-ttu-id="73cf6-861">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-861">10001</span></span></td>
<td><span data-ttu-id="73cf6-862">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-862">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-863">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-863">Fixed cost</span></span></td>
<td><span data-ttu-id="73cf6-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="73cf6-864">-713.75</span></span></td>
<td><span data-ttu-id="73cf6-865">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-866">Prod 1</span></span></td>
<td><span data-ttu-id="73cf6-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-867">Product 1</span></span></td>
<td><span data-ttu-id="73cf6-868">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-868">10001</span></span></td>
<td><span data-ttu-id="73cf6-869">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-869">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-870">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-870">Fixed cost</span></span></td>
<td><span data-ttu-id="73cf6-871">535.31</span><span class="sxs-lookup"><span data-stu-id="73cf6-871">535.31</span></span></td>
<td><span data-ttu-id="73cf6-872">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-873">Prod 2</span></span></td>
<td><span data-ttu-id="73cf6-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-874">Product 2</span></span></td>
<td><span data-ttu-id="73cf6-875">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-875">10001</span></span></td>
<td><span data-ttu-id="73cf6-876">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-876">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-877">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-877">Fixed cost</span></span></td>
<td><span data-ttu-id="73cf6-878">178.44</span><span class="sxs-lookup"><span data-stu-id="73cf6-878">178.44</span></span></td>
<td><span data-ttu-id="73cf6-879">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-880">CC003</span><span class="sxs-lookup"><span data-stu-id="73cf6-880">CC003</span></span></td>
<td><span data-ttu-id="73cf6-881">Sestavení</span><span class="sxs-lookup"><span data-stu-id="73cf6-881">Assembly</span></span></td>
<td><span data-ttu-id="73cf6-882">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-882">10001</span></span></td>
<td><span data-ttu-id="73cf6-883">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-883">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-884">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-884">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-885">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="73cf6-885">-5,982.83</span></span></td>
<td><span data-ttu-id="73cf6-886">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-887">Prod 1</span></span></td>
<td><span data-ttu-id="73cf6-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-888">Product 1</span></span></td>
<td><span data-ttu-id="73cf6-889">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-889">10001</span></span></td>
<td><span data-ttu-id="73cf6-890">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-890">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-891">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-891">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="73cf6-892">4,487.12</span></span></td>
<td><span data-ttu-id="73cf6-893">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-894">Prod 2</span></span></td>
<td><span data-ttu-id="73cf6-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-895">Product 2</span></span></td>
<td><span data-ttu-id="73cf6-896">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-896">10001</span></span></td>
<td><span data-ttu-id="73cf6-897">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-897">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-898">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-898">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="73cf6-899">1,495.71</span></span></td>
<td><span data-ttu-id="73cf6-900">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-901">CC003</span><span class="sxs-lookup"><span data-stu-id="73cf6-901">CC003</span></span></td>
<td><span data-ttu-id="73cf6-902">Sestavení</span><span class="sxs-lookup"><span data-stu-id="73cf6-902">Assembly</span></span></td>
<td><span data-ttu-id="73cf6-903">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-903">10001</span></span></td>
<td><span data-ttu-id="73cf6-904">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-904">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-905">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-905">Fixed cost</span></span></td>
<td><span data-ttu-id="73cf6-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="73cf6-906">-286.25</span></span></td>
<td><span data-ttu-id="73cf6-907">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-908">Prod 1</span></span></td>
<td><span data-ttu-id="73cf6-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-909">Product 1</span></span></td>
<td><span data-ttu-id="73cf6-910">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-910">10001</span></span></td>
<td><span data-ttu-id="73cf6-911">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-911">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-912">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-912">Fixed cost</span></span></td>
<td><span data-ttu-id="73cf6-913">241.05</span><span class="sxs-lookup"><span data-stu-id="73cf6-913">241.05</span></span></td>
<td><span data-ttu-id="73cf6-914">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-915">Prod 2</span></span></td>
<td><span data-ttu-id="73cf6-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-916">Product 2</span></span></td>
<td><span data-ttu-id="73cf6-917">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-917">10001</span></span></td>
<td><span data-ttu-id="73cf6-918">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-918">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-919">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-919">Fixed cost</span></span></td>
<td><span data-ttu-id="73cf6-920">45.20</span><span class="sxs-lookup"><span data-stu-id="73cf6-920">45.20</span></span></td>
<td><span data-ttu-id="73cf6-921">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-922">CC003</span><span class="sxs-lookup"><span data-stu-id="73cf6-922">CC003</span></span></td>
<td><span data-ttu-id="73cf6-923">Sestavení</span><span class="sxs-lookup"><span data-stu-id="73cf6-923">Assembly</span></span></td>
<td><span data-ttu-id="73cf6-924">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-924">10001</span></span></td>
<td><span data-ttu-id="73cf6-925">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-925">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-926">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-926">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="73cf6-927">-2,977.17</span></span></td>
<td><span data-ttu-id="73cf6-928">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-929">Prod 1</span></span></td>
<td><span data-ttu-id="73cf6-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-930">Product 1</span></span></td>
<td><span data-ttu-id="73cf6-931">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-931">10001</span></span></td>
<td><span data-ttu-id="73cf6-932">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-932">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-933">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-933">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="73cf6-934">2,507.09</span></span></td>
<td><span data-ttu-id="73cf6-935">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73cf6-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-936">Prod 2</span></span></td>
<td><span data-ttu-id="73cf6-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-937">Product 2</span></span></td>
<td><span data-ttu-id="73cf6-938">10001</span><span class="sxs-lookup"><span data-stu-id="73cf6-938">10001</span></span></td>
<td><span data-ttu-id="73cf6-939">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="73cf6-939">Electricity</span></span></td>
<td><span data-ttu-id="73cf6-940">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-940">Variable cost</span></span></td>
<td><span data-ttu-id="73cf6-941">470.08</span><span class="sxs-lookup"><span data-stu-id="73cf6-941">470.08</span></span></td>
<td><span data-ttu-id="73cf6-942">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="73cf6-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="73cf6-943">Závěr</span><span class="sxs-lookup"><span data-stu-id="73cf6-943">Conclusion</span></span>
<span data-ttu-id="73cf6-944">Ve finančním účtování se náklady za elektřinu ve výši 10 000 zaúčtují na ID fiktivního nákladového střediska.</span><span class="sxs-lookup"><span data-stu-id="73cf6-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="73cf6-945">Účetní tak budou vědět, že tento náklad musí být přidělen.</span><span class="sxs-lookup"><span data-stu-id="73cf6-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="73cf6-946">V nákladovém účetnictví náklady procházejí napříč organizačními jednotkami a úrovněmi, na základě použitých zásad a pravidel.</span><span class="sxs-lookup"><span data-stu-id="73cf6-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="73cf6-947">Každý náklad byl přidružen k základu přidělení, který poskytuje nejlepší hodnocení pro přidělení nákladů.</span><span class="sxs-lookup"><span data-stu-id="73cf6-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="73cf6-948">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="73cf6-949">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="73cf6-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="73cf6-950">Celkem</span><span class="sxs-lookup"><span data-stu-id="73cf6-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="73cf6-951">CC099</span><span class="sxs-lookup"><span data-stu-id="73cf6-951">CC099</span></span></th>
<th><span data-ttu-id="73cf6-952">CC001</span><span class="sxs-lookup"><span data-stu-id="73cf6-952">CC001</span></span></th>
<th><span data-ttu-id="73cf6-953">CC002</span><span class="sxs-lookup"><span data-stu-id="73cf6-953">CC002</span></span></th>
<th><span data-ttu-id="73cf6-954">CC003</span><span class="sxs-lookup"><span data-stu-id="73cf6-954">CC003</span></span></th>
<th><span data-ttu-id="73cf6-955">CC004</span><span class="sxs-lookup"><span data-stu-id="73cf6-955">CC004</span></span></th>
<th><span data-ttu-id="73cf6-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-956">Proj 1</span></span></th>
<th><span data-ttu-id="73cf6-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-957">Proj 2</span></span></th>
<th><span data-ttu-id="73cf6-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="73cf6-958">Prod 1</span></span></th>
<th><span data-ttu-id="73cf6-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="73cf6-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="73cf6-960">10001 Elektřina</span><span class="sxs-lookup"><span data-stu-id="73cf6-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73cf6-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="73cf6-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="73cf6-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="73cf6-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="73cf6-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="73cf6-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="73cf6-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="73cf6-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="73cf6-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="73cf6-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="73cf6-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="73cf6-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="73cf6-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="73cf6-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="73cf6-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="73cf6-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="73cf6-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="73cf6-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="73cf6-970">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="73cf6-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73cf6-971">0,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-971">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="73cf6-972">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73cf6-973">0,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73cf6-974">0,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73cf6-975">0,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73cf6-976">0,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73cf6-977">0,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="73cf6-978">776.36</span><span class="sxs-lookup"><span data-stu-id="73cf6-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73cf6-979">223.64</span><span class="sxs-lookup"><span data-stu-id="73cf6-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73cf6-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="73cf6-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="73cf6-981">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="73cf6-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73cf6-982">000</span><span class="sxs-lookup"><span data-stu-id="73cf6-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73cf6-983">0,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73cf6-984">0,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73cf6-985">0,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73cf6-986">0,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73cf6-987">30.00</span><span class="sxs-lookup"><span data-stu-id="73cf6-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73cf6-988">10,00</span><span class="sxs-lookup"><span data-stu-id="73cf6-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73cf6-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="73cf6-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73cf6-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="73cf6-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73cf6-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="73cf6-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="73cf6-992">Toto téma popisuje, jak primární prvek nákladů, 10001 Elektřina, prochází přes objekty nákladů.</span><span class="sxs-lookup"><span data-stu-id="73cf6-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="73cf6-993">Tyto režijní náklady tedy budou přiděleny na nejnižší úroveň v organizaci.</span><span class="sxs-lookup"><span data-stu-id="73cf6-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="73cf6-994">Jinak řečeno, objekty nákladů na nejnižší úrovni ponesou náklady.</span><span class="sxs-lookup"><span data-stu-id="73cf6-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="73cf6-995">Chcete-li vizuální tok nákladů mezi objekty nákladů, můžete použít pravidla zásad shrnutí nákladů pro vizualizaci jejich toků.</span><span class="sxs-lookup"><span data-stu-id="73cf6-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="73cf6-996">Další informace naleznete v tématu [Zásady shrnutí nákladů a výpočet režijních nákladů](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="73cf6-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



