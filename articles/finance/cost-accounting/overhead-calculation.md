---
title: Výpočet režijních nákladů
description: Toto téma popisuje typické procesy pro výpočet a přidělení režijních nákladů.
author: AndersGirke
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 8dc312e66dc666ac6c23bac6b705ffc7893fd06b
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187990"
---
# <a name="overhead-calculation"></a><span data-ttu-id="173e1-103">Výpočet režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="173e1-104">Toto téma popisuje typické procesy pro výpočet a přidělení režijních nákladů.</span><span class="sxs-lookup"><span data-stu-id="173e1-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

## <a name="term-definition"></a><span data-ttu-id="173e1-105">Definice termínu</span><span class="sxs-lookup"><span data-stu-id="173e1-105">Term definition</span></span>

<span data-ttu-id="173e1-106">Režijní náklady jsou náklady, které nutně vznikají při chodu podnikání, ale nelze je připsat přímo k žádné konkrétní podnikatelské aktivitě, produktu nebo službě.</span><span class="sxs-lookup"><span data-stu-id="173e1-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="173e1-107">Režijní náklady poskytují důležitou podporu pro generování aktivity přinášejících zisk.</span><span class="sxs-lookup"><span data-stu-id="173e1-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="173e1-108">Následuje několik příkladů režijních nákladů:</span><span class="sxs-lookup"><span data-stu-id="173e1-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="173e1-109">Renta</span><span class="sxs-lookup"><span data-stu-id="173e1-109">Rent</span></span>
-   <span data-ttu-id="173e1-110">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-110">Electricity</span></span>
-   <span data-ttu-id="173e1-111">Administrativní mzdy</span><span class="sxs-lookup"><span data-stu-id="173e1-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="173e1-112">Přehled výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-112">Overhead calculation overview</span></span>
<span data-ttu-id="173e1-113">Výpočet režijních nákladů spustí zásady účtování nákladů ve správném pořadí.</span><span class="sxs-lookup"><span data-stu-id="173e1-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="173e1-114">Výpočet režijních nákladů můžete pro stejné fiskální období spustit mnohokrát, pokud došlo ke změně zásad účtování nákladů nebo zjištění konkrétních chyb.</span><span class="sxs-lookup"><span data-stu-id="173e1-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="173e1-115">Každé spuštění výpočtu režijních nákladů se ukládá a přijímá ID jedinečné verze, které vám umožní porovnávat výpočty v různých verzích.</span><span class="sxs-lookup"><span data-stu-id="173e1-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="173e1-116">Položky nákladů, které generuje výpočet režijních nákladů, přijímá datum účtování.</span><span class="sxs-lookup"><span data-stu-id="173e1-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="173e1-117">Toto datum účtován se shoduje s konvovým datem fiskálního období, které se použije ve výpočtu.</span><span class="sxs-lookup"><span data-stu-id="173e1-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="173e1-118">ID jedinečné verze se skládá z následujících prvků:</span><span class="sxs-lookup"><span data-stu-id="173e1-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="173e1-119">Typ verze</span><span class="sxs-lookup"><span data-stu-id="173e1-119">Version type</span></span>
-   <span data-ttu-id="173e1-120">Datum a čas</span><span class="sxs-lookup"><span data-stu-id="173e1-120">Date and time</span></span>
-   <span data-ttu-id="173e1-121">Hlavní kniha nákladového účetnictví</span><span class="sxs-lookup"><span data-stu-id="173e1-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="173e1-122">Fiskální rok</span><span class="sxs-lookup"><span data-stu-id="173e1-122">Fiscal year</span></span>
-   <span data-ttu-id="173e1-123">Fiskální období</span><span class="sxs-lookup"><span data-stu-id="173e1-123">Fiscal period</span></span>

<span data-ttu-id="173e1-124">Výpočet režijních nákladů se spustí bez ohledu na verzi.</span><span class="sxs-lookup"><span data-stu-id="173e1-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="173e1-125">Proto lze vypočítat rozpočtovou verzi před skutečnou verzí.</span><span class="sxs-lookup"><span data-stu-id="173e1-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="173e1-126">Výpočet režijních nákladů se skládá ze čtyř kroků uvedených na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="173e1-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="173e1-127">V každé fázi je vytvořeno záhlaví deníku, které obsahuje položky deníku.</span><span class="sxs-lookup"><span data-stu-id="173e1-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="173e1-128">Toto záhlaví deníku zachovává vstupní data pro každý krok výpočtu.</span><span class="sxs-lookup"><span data-stu-id="173e1-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="173e1-129">Zásady a pravidla se použijí na každý řádek deníku a položky nákladů jsou generovány jako výstup.</span><span class="sxs-lookup"><span data-stu-id="173e1-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="173e1-130">Máte tedy vždy plnou sledovatelnost.</span><span class="sxs-lookup"><span data-stu-id="173e1-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="173e1-131">[![Výpočet režijních nákladů](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="173e1-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="173e1-132">Výpočet a přidělení režijních nákladů za elektřinu</span><span class="sxs-lookup"><span data-stu-id="173e1-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="173e1-133">Ve finančním účetnictví se některé náklady, jako je například elektřina, registrují jako paušální.</span><span class="sxs-lookup"><span data-stu-id="173e1-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="173e1-134">Podrobný přehled pro vedoucí není tedy pro nákladové účetnictví k dispozici.</span><span class="sxs-lookup"><span data-stu-id="173e1-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="173e1-135">V nákladovém účetnictví musí náklady procházet organizačními jednotkami, aby byl získán správný přehled pro vedoucí napříč všemi jednotkami a úrovněmi organizace.</span><span class="sxs-lookup"><span data-stu-id="173e1-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="173e1-136">Tento tok musí být založen buď na přesném záznamu spotřeby nebo na objektivním hodnocení.</span><span class="sxs-lookup"><span data-stu-id="173e1-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="173e1-137">V hlavní knize mohou být zaúčtovány náklady na elektřinu způsobem znázorněným v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="173e1-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="173e1-138">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="173e1-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="173e1-139">Nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="173e1-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="173e1-140">Hlavní účet</span><span class="sxs-lookup"><span data-stu-id="173e1-140">Main account</span></span></th>
<th><span data-ttu-id="173e1-141">Částka v zúčtovací měně</span><span class="sxs-lookup"><span data-stu-id="173e1-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="173e1-142">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="173e1-143">CC099</span><span class="sxs-lookup"><span data-stu-id="173e1-143">CC099</span></span></td>
<td><span data-ttu-id="173e1-144">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="173e1-144">Default cost center</span></span></td>
<td><span data-ttu-id="173e1-145">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-145">10001</span></span></td>
<td><span data-ttu-id="173e1-146">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-146">Electricity</span></span></td>
<td><span data-ttu-id="173e1-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="173e1-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="173e1-148">Krok 1: Zpracování výpočtu chování nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="173e1-149">Ve výchozím nastavení dostanou při importu položek nákladů z datového zdroje tyto položky v nákladovém účetnictví klasifikaci **Neklasifikované**.</span><span class="sxs-lookup"><span data-stu-id="173e1-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="173e1-150">Použitím pravidla zásad chování nákladů lze reklasifikovat položky nákladů jako **Pevné náklady** nebo **Variabilní náklady**.</span><span class="sxs-lookup"><span data-stu-id="173e1-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="173e1-151">Definice pravidel chování nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-151">Define the cost behavior rule</span></span>

<span data-ttu-id="173e1-152">V některých případech je část nákladů s pevným poplatkem a zbývající náklady jsou založeny na spotřebě.</span><span class="sxs-lookup"><span data-stu-id="173e1-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="173e1-153">Účty za elektřinu často odpovídají této definici.</span><span class="sxs-lookup"><span data-stu-id="173e1-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="173e1-154">Po platbě konkrétního pevného poplatku platíte spotřebu za kilowatthodinu (kWh).</span><span class="sxs-lookup"><span data-stu-id="173e1-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="173e1-155">Pokud je například poplatek pevných nákladů 1 000,00, definuje se pravidlo chování nákladů takto:</span><span class="sxs-lookup"><span data-stu-id="173e1-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="173e1-156">Pevná částka 1 000,00</span><span class="sxs-lookup"><span data-stu-id="173e1-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="173e1-157">0 &lt;= 1 000,00 = Pevná</span><span class="sxs-lookup"><span data-stu-id="173e1-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="173e1-158">1 000,01 &lt; N = Variabilní</span><span class="sxs-lookup"><span data-stu-id="173e1-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="173e1-159">Deník</span><span class="sxs-lookup"><span data-stu-id="173e1-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="173e1-160">Deník</span><span class="sxs-lookup"><span data-stu-id="173e1-160">Journal</span></span></th>
<th><span data-ttu-id="173e1-161">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="173e1-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="173e1-162">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="173e1-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="173e1-163">Verze</span><span class="sxs-lookup"><span data-stu-id="173e1-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="173e1-164">00001</span><span class="sxs-lookup"><span data-stu-id="173e1-164">00001</span></span></td>
<td><span data-ttu-id="173e1-165">Deník výpočtu chování nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="173e1-166">Fiskální</span><span class="sxs-lookup"><span data-stu-id="173e1-166">Fiscal</span></span></td>
<td><span data-ttu-id="173e1-167">2017</span><span class="sxs-lookup"><span data-stu-id="173e1-167">2017</span></span></td>
<td><span data-ttu-id="173e1-168">Období 1</span><span class="sxs-lookup"><span data-stu-id="173e1-168">Period 1</span></span></td>
<td><span data-ttu-id="173e1-169">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="173e1-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="173e1-170">Položky deníku (Položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="173e1-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="173e1-171">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="173e1-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="173e1-172">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="173e1-173">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-173">Cost element</span></span></th>
<th><span data-ttu-id="173e1-174">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-174">Cost behavior</span></span></th>
<th><span data-ttu-id="173e1-175">Částka</span><span class="sxs-lookup"><span data-stu-id="173e1-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="173e1-176">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="173e1-177">CC099</span><span class="sxs-lookup"><span data-stu-id="173e1-177">CC099</span></span></td>
<td><span data-ttu-id="173e1-178">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="173e1-178">Default cost center</span></span></td>
<td><span data-ttu-id="173e1-179">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-179">10001</span></span></td>
<td><span data-ttu-id="173e1-180">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-180">Electricity</span></span></td>
<td><span data-ttu-id="173e1-181">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="173e1-181">Unclassified</span></span></td>
<td><span data-ttu-id="173e1-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="173e1-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="173e1-183">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="173e1-184">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="173e1-185">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-185">Cost element</span></span></th>
<th><span data-ttu-id="173e1-186">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-186">Cost behavior</span></span></th>
<th><span data-ttu-id="173e1-187">Částka</span><span class="sxs-lookup"><span data-stu-id="173e1-187">Amount</span></span></th>
<th><span data-ttu-id="173e1-188">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="173e1-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="173e1-189">CC099</span><span class="sxs-lookup"><span data-stu-id="173e1-189">CC099</span></span></td>
<td><span data-ttu-id="173e1-190">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="173e1-190">Default cost center</span></span></td>
<td><span data-ttu-id="173e1-191">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-191">10001</span></span></td>
<td><span data-ttu-id="173e1-192">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-192">Electricity</span></span></td>
<td><span data-ttu-id="173e1-193">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="173e1-193">Unclassified</span></span></td>
<td><span data-ttu-id="173e1-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="173e1-194">10,000.00</span></span></td>
<td><span data-ttu-id="173e1-195">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-196">CC099</span><span class="sxs-lookup"><span data-stu-id="173e1-196">CC099</span></span></td>
<td><span data-ttu-id="173e1-197">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="173e1-197">Default cost center</span></span></td>
<td><span data-ttu-id="173e1-198">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-198">10001</span></span></td>
<td><span data-ttu-id="173e1-199">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-199">Electricity</span></span></td>
<td><span data-ttu-id="173e1-200">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="173e1-200">Unclassified</span></span></td>
<td><span data-ttu-id="173e1-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="173e1-201">-10,000.00</span></span></td>
<td><span data-ttu-id="173e1-202">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-203">CC099</span><span class="sxs-lookup"><span data-stu-id="173e1-203">CC099</span></span></td>
<td><span data-ttu-id="173e1-204">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="173e1-204">Default cost center</span></span></td>
<td><span data-ttu-id="173e1-205">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-205">10001</span></span></td>
<td><span data-ttu-id="173e1-206">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-206">Electricity</span></span></td>
<td><span data-ttu-id="173e1-207">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-207">Fixed cost</span></span></td>
<td><span data-ttu-id="173e1-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="173e1-208">1,000.00</span></span></td>
<td><span data-ttu-id="173e1-209">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-210">CC099</span><span class="sxs-lookup"><span data-stu-id="173e1-210">CC099</span></span></td>
<td><span data-ttu-id="173e1-211">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="173e1-211">Default cost center</span></span></td>
<td><span data-ttu-id="173e1-212">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-212">10001</span></span></td>
<td><span data-ttu-id="173e1-213">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-213">Electricity</span></span></td>
<td><span data-ttu-id="173e1-214">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-214">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="173e1-215">9,000.00</span></span></td>
<td><span data-ttu-id="173e1-216">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="173e1-217">Více informací naleznete v tématu [Vytvoření a přiřazení zásad chování nákladů k jednotce řízení nákladů](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="173e1-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="173e1-218">Krok 2: Zpracování výpočtu distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="173e1-219">Distribuce nákladů se používá k rozdělení nákladů z jednoho objektu nákladů na jeden nebo více dalších objektů nákladů použitím příslušného základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="173e1-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="173e1-220">Distribuce nákladů a přidělení nákladů se liší v tom, že k distribuci nákladů dochází vždy na úrovni primárního prvku nákladů původních nákladů.</span><span class="sxs-lookup"><span data-stu-id="173e1-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="173e1-221">Definice pravidel distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-221">Define the cost distribution rule</span></span>

<span data-ttu-id="173e1-222">Ve finančním účetnictví se náklady na elektřinu často registrují jako paušální.</span><span class="sxs-lookup"><span data-stu-id="173e1-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="173e1-223">V nákladovém účetnictví není tento přístup dostatečně podrobný.</span><span class="sxs-lookup"><span data-stu-id="173e1-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="173e1-224">Variabilní náklady by měly být distribuovány k jednotlivým objektům nákladů na solidním základě.</span><span class="sxs-lookup"><span data-stu-id="173e1-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="173e1-225">Nejlogičtější základ přidělení je spotřeba elektřiny (kWh).</span><span class="sxs-lookup"><span data-stu-id="173e1-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="173e1-226">Vytvoří se člen statistické dimenzi s názvem Elektřina a zaznamená se elektrické spotřeba.</span><span class="sxs-lookup"><span data-stu-id="173e1-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="173e1-227">Ve výchozím nastavení se všechny členy statistické dimenze stanou dostupnými zpřístupněny jako základy přidělení.</span><span class="sxs-lookup"><span data-stu-id="173e1-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="173e1-228">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-228">Cost object</span></span></th>
<th><span data-ttu-id="173e1-229">kWh</span><span class="sxs-lookup"><span data-stu-id="173e1-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="173e1-230">CC001</span><span class="sxs-lookup"><span data-stu-id="173e1-230">CC001</span></span></td>
<td><span data-ttu-id="173e1-231">HR</span><span class="sxs-lookup"><span data-stu-id="173e1-231">HR</span></span></td>
<td><span data-ttu-id="173e1-232">1 000</span><span class="sxs-lookup"><span data-stu-id="173e1-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-233">CC002</span><span class="sxs-lookup"><span data-stu-id="173e1-233">CC002</span></span></td>
<td><span data-ttu-id="173e1-234">Finance</span><span class="sxs-lookup"><span data-stu-id="173e1-234">Finance</span></span></td>
<td><span data-ttu-id="173e1-235">6,000</span><span class="sxs-lookup"><span data-stu-id="173e1-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-236">CC003</span><span class="sxs-lookup"><span data-stu-id="173e1-236">CC003</span></span></td>
<td><span data-ttu-id="173e1-237">Sestavení</span><span class="sxs-lookup"><span data-stu-id="173e1-237">Assembly</span></span></td>
<td><span data-ttu-id="173e1-238">0</span><span class="sxs-lookup"><span data-stu-id="173e1-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="173e1-239">Následující tabulka zobrazuje výsledek při použití elektrické spotřeby jako základu přidělení pro variabilní náklady.</span><span class="sxs-lookup"><span data-stu-id="173e1-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="173e1-240">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-240">Cost object</span></span></th>
<th><span data-ttu-id="173e1-241">Hodnota</span><span class="sxs-lookup"><span data-stu-id="173e1-241">Magnitude</span></span></th>
<th><span data-ttu-id="173e1-242">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="173e1-242">Allocation factor</span></span></th>
<th><span data-ttu-id="173e1-243">Částka</span><span class="sxs-lookup"><span data-stu-id="173e1-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="173e1-244">CC001</span><span class="sxs-lookup"><span data-stu-id="173e1-244">CC001</span></span></td>
<td><span data-ttu-id="173e1-245">HR</span><span class="sxs-lookup"><span data-stu-id="173e1-245">HR</span></span></td>
<td><span data-ttu-id="173e1-246">1 000</span><span class="sxs-lookup"><span data-stu-id="173e1-246">1,000</span></span></td>
<td><span data-ttu-id="173e1-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="173e1-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="173e1-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="173e1-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-249">CC002</span><span class="sxs-lookup"><span data-stu-id="173e1-249">CC002</span></span></td>
<td><span data-ttu-id="173e1-250">Finance</span><span class="sxs-lookup"><span data-stu-id="173e1-250">Finance</span></span></td>
<td><span data-ttu-id="173e1-251">6,000</span><span class="sxs-lookup"><span data-stu-id="173e1-251">6,000</span></span></td>
<td><span data-ttu-id="173e1-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="173e1-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="173e1-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="173e1-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-254">CC003</span><span class="sxs-lookup"><span data-stu-id="173e1-254">CC003</span></span></td>
<td><span data-ttu-id="173e1-255">Sestavení</span><span class="sxs-lookup"><span data-stu-id="173e1-255">Assembly</span></span></td>
<td><span data-ttu-id="173e1-256">0</span><span class="sxs-lookup"><span data-stu-id="173e1-256">0</span></span></td>
<td><span data-ttu-id="173e1-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="173e1-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="173e1-258">0,00</span><span class="sxs-lookup"><span data-stu-id="173e1-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="173e1-259">Pevné náklady musí být distribuovány rovnoměrně k jednotlivých objektům nákladů, které spotřebovávaly elektřinu.</span><span class="sxs-lookup"><span data-stu-id="173e1-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="173e1-260">Tohoto výsledku můžete dosáhnout pomocí členu statistické dimenze Elektřina v základu přidělení vzorce: (Elektřina &gt; 0,00) Následující tabulka zobrazuje výsledek při použití elektrické spotřeby jako základu přidělení pro variabilní náklady.</span><span class="sxs-lookup"><span data-stu-id="173e1-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="173e1-261">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-261">Cost object</span></span></th>
<th><span data-ttu-id="173e1-262">Vzorec</span><span class="sxs-lookup"><span data-stu-id="173e1-262">Formula</span></span></th>
<th><span data-ttu-id="173e1-263">Hodnota</span><span class="sxs-lookup"><span data-stu-id="173e1-263">Magnitude</span></span></th>
<th><span data-ttu-id="173e1-264">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="173e1-264">Allocation factor</span></span></th>
<th><span data-ttu-id="173e1-265">Částka</span><span class="sxs-lookup"><span data-stu-id="173e1-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="173e1-266">CC001</span><span class="sxs-lookup"><span data-stu-id="173e1-266">CC001</span></span></td>
<td><span data-ttu-id="173e1-267">HR</span><span class="sxs-lookup"><span data-stu-id="173e1-267">HR</span></span></td>
<td><span data-ttu-id="173e1-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="173e1-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="173e1-269">1</span><span class="sxs-lookup"><span data-stu-id="173e1-269">1</span></span></td>
<td><span data-ttu-id="173e1-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="173e1-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="173e1-271">500.00</span><span class="sxs-lookup"><span data-stu-id="173e1-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-272">CC002</span><span class="sxs-lookup"><span data-stu-id="173e1-272">CC002</span></span></td>
<td><span data-ttu-id="173e1-273">Finance</span><span class="sxs-lookup"><span data-stu-id="173e1-273">Finance</span></span></td>
<td><span data-ttu-id="173e1-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="173e1-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="173e1-275">1</span><span class="sxs-lookup"><span data-stu-id="173e1-275">1</span></span></td>
<td><span data-ttu-id="173e1-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="173e1-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="173e1-277">500.00</span><span class="sxs-lookup"><span data-stu-id="173e1-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-278">CC003</span><span class="sxs-lookup"><span data-stu-id="173e1-278">CC003</span></span></td>
<td><span data-ttu-id="173e1-279">Sestavení</span><span class="sxs-lookup"><span data-stu-id="173e1-279">Assembly</span></span></td>
<td><span data-ttu-id="173e1-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="173e1-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="173e1-281">0</span><span class="sxs-lookup"><span data-stu-id="173e1-281">0</span></span></td>
<td><span data-ttu-id="173e1-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="173e1-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="173e1-283">0,00</span><span class="sxs-lookup"><span data-stu-id="173e1-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="173e1-284">Deník</span><span class="sxs-lookup"><span data-stu-id="173e1-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="173e1-285">Deník</span><span class="sxs-lookup"><span data-stu-id="173e1-285">Journal</span></span></th>
<th><span data-ttu-id="173e1-286">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="173e1-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="173e1-287">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="173e1-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="173e1-288">Verze</span><span class="sxs-lookup"><span data-stu-id="173e1-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="173e1-289">00002</span><span class="sxs-lookup"><span data-stu-id="173e1-289">00002</span></span></td>
<td><span data-ttu-id="173e1-290">Deník výpočtu distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="173e1-291">Fiskální</span><span class="sxs-lookup"><span data-stu-id="173e1-291">Fiscal</span></span></td>
<td><span data-ttu-id="173e1-292">2017</span><span class="sxs-lookup"><span data-stu-id="173e1-292">2017</span></span></td>
<td><span data-ttu-id="173e1-293">Období 1</span><span class="sxs-lookup"><span data-stu-id="173e1-293">Period 1</span></span></td>
<td><span data-ttu-id="173e1-294">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="173e1-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="173e1-295">Položky deníku (Položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="173e1-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="173e1-296">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="173e1-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="173e1-297">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="173e1-298">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-298">Cost element</span></span></th>
<th><span data-ttu-id="173e1-299">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-299">Cost behavior</span></span></th>
<th><span data-ttu-id="173e1-300">Částka</span><span class="sxs-lookup"><span data-stu-id="173e1-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="173e1-301">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="173e1-302">CC099</span><span class="sxs-lookup"><span data-stu-id="173e1-302">CC099</span></span></td>
<td><span data-ttu-id="173e1-303">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="173e1-303">Default cost center</span></span></td>
<td><span data-ttu-id="173e1-304">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-304">10001</span></span></td>
<td><span data-ttu-id="173e1-305">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-305">Electricity</span></span></td>
<td><span data-ttu-id="173e1-306">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-306">Fixed cost</span></span></td>
<td><span data-ttu-id="173e1-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="173e1-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-308">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="173e1-309">CC099</span><span class="sxs-lookup"><span data-stu-id="173e1-309">CC099</span></span></td>
<td><span data-ttu-id="173e1-310">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="173e1-310">Default cost center</span></span></td>
<td><span data-ttu-id="173e1-311">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-311">10001</span></span></td>
<td><span data-ttu-id="173e1-312">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-312">Electricity</span></span></td>
<td><span data-ttu-id="173e1-313">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-313">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="173e1-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="173e1-315">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="173e1-316">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="173e1-317">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-317">Cost element</span></span></th>
<th><span data-ttu-id="173e1-318">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-318">Cost behavior</span></span></th>
<th><span data-ttu-id="173e1-319">Částka</span><span class="sxs-lookup"><span data-stu-id="173e1-319">Amount</span></span></th>
<th><span data-ttu-id="173e1-320">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="173e1-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="173e1-321">CC099</span><span class="sxs-lookup"><span data-stu-id="173e1-321">CC099</span></span></td>
<td><span data-ttu-id="173e1-322">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="173e1-322">Default cost center</span></span></td>
<td><span data-ttu-id="173e1-323">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-323">10001</span></span></td>
<td><span data-ttu-id="173e1-324">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-324">Electricity</span></span></td>
<td><span data-ttu-id="173e1-325">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-325">Fixed cost</span></span></td>
<td><span data-ttu-id="173e1-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="173e1-326">-1,000.00</span></span></td>
<td><span data-ttu-id="173e1-327">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-328">CC001</span><span class="sxs-lookup"><span data-stu-id="173e1-328">CC001</span></span></td>
<td><span data-ttu-id="173e1-329">HR</span><span class="sxs-lookup"><span data-stu-id="173e1-329">HR</span></span></td>
<td><span data-ttu-id="173e1-330">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-330">10001</span></span></td>
<td><span data-ttu-id="173e1-331">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-331">Electricity</span></span></td>
<td><span data-ttu-id="173e1-332">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-332">Fixed cost</span></span></td>
<td><span data-ttu-id="173e1-333">500.00</span><span class="sxs-lookup"><span data-stu-id="173e1-333">500.00</span></span></td>
<td><span data-ttu-id="173e1-334">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-335">CC002</span><span class="sxs-lookup"><span data-stu-id="173e1-335">CC002</span></span></td>
<td><span data-ttu-id="173e1-336">Finance</span><span class="sxs-lookup"><span data-stu-id="173e1-336">Finance</span></span></td>
<td><span data-ttu-id="173e1-337">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-337">10001</span></span></td>
<td><span data-ttu-id="173e1-338">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-338">Electricity</span></span></td>
<td><span data-ttu-id="173e1-339">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-339">Fixed cost</span></span></td>
<td><span data-ttu-id="173e1-340">500.00</span><span class="sxs-lookup"><span data-stu-id="173e1-340">500.00</span></span></td>
<td><span data-ttu-id="173e1-341">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-342">CC099</span><span class="sxs-lookup"><span data-stu-id="173e1-342">CC099</span></span></td>
<td><span data-ttu-id="173e1-343">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="173e1-343">Default cost center</span></span></td>
<td><span data-ttu-id="173e1-344">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-344">10001</span></span></td>
<td><span data-ttu-id="173e1-345">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-345">Electricity</span></span></td>
<td><span data-ttu-id="173e1-346">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-346">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-347">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="173e1-347">-9,000.00</span></span></td>
<td><span data-ttu-id="173e1-348">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-349">CC001</span><span class="sxs-lookup"><span data-stu-id="173e1-349">CC001</span></span></td>
<td><span data-ttu-id="173e1-350">HR</span><span class="sxs-lookup"><span data-stu-id="173e1-350">HR</span></span></td>
<td><span data-ttu-id="173e1-351">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-351">10001</span></span></td>
<td><span data-ttu-id="173e1-352">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-352">Electricity</span></span></td>
<td><span data-ttu-id="173e1-353">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-353">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="173e1-354">1,285.71</span></span></td>
<td><span data-ttu-id="173e1-355">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-356">CC002</span><span class="sxs-lookup"><span data-stu-id="173e1-356">CC002</span></span></td>
<td><span data-ttu-id="173e1-357">Finance</span><span class="sxs-lookup"><span data-stu-id="173e1-357">Finance</span></span></td>
<td><span data-ttu-id="173e1-358">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-358">10001</span></span></td>
<td><span data-ttu-id="173e1-359">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-359">Electricity</span></span></td>
<td><span data-ttu-id="173e1-360">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-360">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="173e1-361">7,714.29</span></span></td>
<td><span data-ttu-id="173e1-362">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="173e1-363">Více informací naleznete v tématu [Vytvoření a přiřazení zásad distribuce nákladů k jednotce řízení nákladů](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="173e1-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="173e1-364">Krok 3: Zpracování výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="173e1-365">Režijní náklady se používají k účtování jednoho nebo více konkrétních objektů nákladů.</span><span class="sxs-lookup"><span data-stu-id="173e1-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="173e1-366">Účtování je založeno na předem určené nákladové sazbě a množství z přiřazeného základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="173e1-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="173e1-367">Definice sazby režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-367">Define the overhead rate</span></span>

<span data-ttu-id="173e1-368">Objekt nákladů CC001 HR přispívá k sadě interních projektů.</span><span class="sxs-lookup"><span data-stu-id="173e1-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="173e1-369">Vytvoří se člen statistické dimenzi s názvem projekty lidských zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="173e1-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="173e1-370">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-370">Cost object</span></span></th>
<th><span data-ttu-id="173e1-371">Pracovní doba</span><span class="sxs-lookup"><span data-stu-id="173e1-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="173e1-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="173e1-372">Proj 1</span></span></td>
<td><span data-ttu-id="173e1-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="173e1-373">Project 1</span></span></td>
<td><span data-ttu-id="173e1-374">3</span><span class="sxs-lookup"><span data-stu-id="173e1-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="173e1-375">Proj 2</span></span></td>
<td><span data-ttu-id="173e1-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="173e1-376">Project 2</span></span></td>
<td><span data-ttu-id="173e1-377">1</span><span class="sxs-lookup"><span data-stu-id="173e1-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="173e1-378">Byla definována předem určená nákladová sazba pro příspěvky k nákladovým projektům.</span><span class="sxs-lookup"><span data-stu-id="173e1-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="173e1-379">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-379">Cost object</span></span></th>
<th><span data-ttu-id="173e1-380">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-380">Cost element</span></span></th>
<th><span data-ttu-id="173e1-381">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-381">Cost behavior</span></span></th>
<th><span data-ttu-id="173e1-382">Jednotky</span><span class="sxs-lookup"><span data-stu-id="173e1-382">Units</span></span></th>
<th><span data-ttu-id="173e1-383">Kurz</span><span class="sxs-lookup"><span data-stu-id="173e1-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="173e1-384">CC001</span><span class="sxs-lookup"><span data-stu-id="173e1-384">CC001</span></span></td>
<td><span data-ttu-id="173e1-385">HR</span><span class="sxs-lookup"><span data-stu-id="173e1-385">HR</span></span></td>
<td><span data-ttu-id="173e1-386">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-386">10001</span></span></td>
<td><span data-ttu-id="173e1-387">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-387">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-388">1</span><span class="sxs-lookup"><span data-stu-id="173e1-388">1</span></span></td>
<td><span data-ttu-id="173e1-389">10</span><span class="sxs-lookup"><span data-stu-id="173e1-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="173e1-390">Následující tabulka zobrazuje výsledek při použití projektů lidských zdrojů jako základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="173e1-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="173e1-391">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-391">Cost object</span></span></th>
<th><span data-ttu-id="173e1-392">Hodnota</span><span class="sxs-lookup"><span data-stu-id="173e1-392">Magnitude</span></span></th>
<th><span data-ttu-id="173e1-393">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-393">Cost element</span></span></th>
<th><span data-ttu-id="173e1-394">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="173e1-394">Allocation factor</span></span></th>
<th><span data-ttu-id="173e1-395">Částka</span><span class="sxs-lookup"><span data-stu-id="173e1-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="173e1-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="173e1-396">Proj 1</span></span></td>
<td><span data-ttu-id="173e1-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="173e1-397">Project 1</span></span></td>
<td><span data-ttu-id="173e1-398">3</span><span class="sxs-lookup"><span data-stu-id="173e1-398">3</span></span></td>
<td><span data-ttu-id="173e1-399">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-399">10001</span></span></td>
<td><span data-ttu-id="173e1-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="173e1-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="173e1-401">30.00</span><span class="sxs-lookup"><span data-stu-id="173e1-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="173e1-402">Proj 2</span></span></td>
<td><span data-ttu-id="173e1-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="173e1-403">Project 2</span></span></td>
<td><span data-ttu-id="173e1-404">1</span><span class="sxs-lookup"><span data-stu-id="173e1-404">1</span></span></td>
<td><span data-ttu-id="173e1-405">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-405">10001</span></span></td>
<td><span data-ttu-id="173e1-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="173e1-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="173e1-407">10,00</span><span class="sxs-lookup"><span data-stu-id="173e1-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="173e1-408">Deník</span><span class="sxs-lookup"><span data-stu-id="173e1-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="173e1-409">Deník</span><span class="sxs-lookup"><span data-stu-id="173e1-409">Journal</span></span></th>
<th><span data-ttu-id="173e1-410">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="173e1-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="173e1-411">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="173e1-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="173e1-412">Verze</span><span class="sxs-lookup"><span data-stu-id="173e1-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="173e1-413">00003</span><span class="sxs-lookup"><span data-stu-id="173e1-413">00003</span></span></td>
<td><span data-ttu-id="173e1-414">Deník výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="173e1-415">Fiskální</span><span class="sxs-lookup"><span data-stu-id="173e1-415">Fiscal</span></span></td>
<td><span data-ttu-id="173e1-416">2017</span><span class="sxs-lookup"><span data-stu-id="173e1-416">2017</span></span></td>
<td><span data-ttu-id="173e1-417">Období 1</span><span class="sxs-lookup"><span data-stu-id="173e1-417">Period 1</span></span></td>
<td><span data-ttu-id="173e1-418">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="173e1-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="173e1-419">Položky deníku (položky deníku pro výpočet sazby režijních nákladů)</span><span class="sxs-lookup"><span data-stu-id="173e1-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="173e1-420">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="173e1-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="173e1-421">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-421">Cost object</span></span></th>
<th><span data-ttu-id="173e1-422">Hodnota</span><span class="sxs-lookup"><span data-stu-id="173e1-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="173e1-423">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="173e1-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="173e1-424">Proj 1</span></span></td>
<td><span data-ttu-id="173e1-425">Interní projekt 1</span><span class="sxs-lookup"><span data-stu-id="173e1-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="173e1-426">3,00</span><span class="sxs-lookup"><span data-stu-id="173e1-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-427">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="173e1-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="173e1-428">Proj 2</span></span></td>
<td><span data-ttu-id="173e1-429">Interní projekt 2</span><span class="sxs-lookup"><span data-stu-id="173e1-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="173e1-430">1.00</span><span class="sxs-lookup"><span data-stu-id="173e1-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="173e1-431">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="173e1-432">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="173e1-433">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-433">Cost element</span></span></th>
<th><span data-ttu-id="173e1-434">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-434">Cost behavior</span></span></th>
<th><span data-ttu-id="173e1-435">Částka</span><span class="sxs-lookup"><span data-stu-id="173e1-435">Amount</span></span></th>
<th><span data-ttu-id="173e1-436">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="173e1-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="173e1-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="173e1-437">CC0001</span></span></td>
<td><span data-ttu-id="173e1-438">HR</span><span class="sxs-lookup"><span data-stu-id="173e1-438">HR</span></span></td>
<td><span data-ttu-id="173e1-439">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-439">10001</span></span></td>
<td><span data-ttu-id="173e1-440">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-440">Electricity</span></span></td>
<td><span data-ttu-id="173e1-441">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-441">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="173e1-442">-30.00</span></span></td>
<td><span data-ttu-id="173e1-443">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="173e1-444">Proj 1</span></span></td>
<td><span data-ttu-id="173e1-445">Interní projekt 1</span><span class="sxs-lookup"><span data-stu-id="173e1-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="173e1-446">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-446">10001</span></span></td>
<td><span data-ttu-id="173e1-447">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-447">Electricity</span></span></td>
<td><span data-ttu-id="173e1-448">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-448">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-449">30.00</span><span class="sxs-lookup"><span data-stu-id="173e1-449">30.00</span></span></td>
<td><span data-ttu-id="173e1-450">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-451">CC001</span><span class="sxs-lookup"><span data-stu-id="173e1-451">CC001</span></span></td>
<td><span data-ttu-id="173e1-452">HR</span><span class="sxs-lookup"><span data-stu-id="173e1-452">HR</span></span></td>
<td><span data-ttu-id="173e1-453">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-453">10001</span></span></td>
<td><span data-ttu-id="173e1-454">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-454">Electricity</span></span></td>
<td><span data-ttu-id="173e1-455">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-455">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="173e1-456">-10.00</span></span></td>
<td><span data-ttu-id="173e1-457">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="173e1-458">Proj 2</span></span></td>
<td><span data-ttu-id="173e1-459">Interní projekt 2</span><span class="sxs-lookup"><span data-stu-id="173e1-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="173e1-460">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-460">10001</span></span></td>
<td><span data-ttu-id="173e1-461">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-461">Electricity</span></span></td>
<td><span data-ttu-id="173e1-462">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-462">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-463">10.00</span><span class="sxs-lookup"><span data-stu-id="173e1-463">10.00</span></span></td>
<td><span data-ttu-id="173e1-464">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="173e1-465">Další informace naleznete v tématu [Provedení výpočtu režijních nákladů](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="173e1-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="173e1-466">Krok 4: Zpracování výpočtu přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="173e1-467">Přidělení se používá k přidělení zůstatku objektu nákladů do jiných objektů nákladů použitím základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="173e1-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="173e1-468">Aplikace Finance podporuje reciproční metodu přidělování.</span><span class="sxs-lookup"><span data-stu-id="173e1-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="173e1-469">V metodě vzájemného přidělení jsou plně rozpoznány vzájemné služby, které si vyměňují pomocné objekty nákladů.</span><span class="sxs-lookup"><span data-stu-id="173e1-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="173e1-470">Systém automaticky určí provádění přidělení ve správném pořadí.</span><span class="sxs-lookup"><span data-stu-id="173e1-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="173e1-471">Zůstatek objektu nákladů je přidělen jedním základem přidělení.</span><span class="sxs-lookup"><span data-stu-id="173e1-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="173e1-472">Je podporováno přidělování napříč dimenzemi objektů nákladů a jejich příslušných členů.</span><span class="sxs-lookup"><span data-stu-id="173e1-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="173e1-473">Pořadí přidělení je řízeno jednotkou řízení nákladů.</span><span class="sxs-lookup"><span data-stu-id="173e1-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="173e1-474">[![Reciproční metoda](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="173e1-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="173e1-475">Definice přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-475">Define the cost allocation</span></span>

<span data-ttu-id="173e1-476">Toto je jednoduchý příklad, který vysvětluje, jakým způsobem lze sledovat tok nákladů.</span><span class="sxs-lookup"><span data-stu-id="173e1-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="173e1-477">Objekt nákladů objektu CC001 HR přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="173e1-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="173e1-478">Vytvoří se člen statistické dimenzi s názvem služby lidských zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="173e1-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="173e1-479">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-479">Cost object</span></span></th>
<th><span data-ttu-id="173e1-480">Služby HR</span><span class="sxs-lookup"><span data-stu-id="173e1-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="173e1-481">CC002</span><span class="sxs-lookup"><span data-stu-id="173e1-481">CC002</span></span></td>
<td><span data-ttu-id="173e1-482">Finance</span><span class="sxs-lookup"><span data-stu-id="173e1-482">Finance</span></span></td>
<td><span data-ttu-id="173e1-483">35</span><span class="sxs-lookup"><span data-stu-id="173e1-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-484">CC003</span><span class="sxs-lookup"><span data-stu-id="173e1-484">CC003</span></span></td>
<td><span data-ttu-id="173e1-485">Sestavení</span><span class="sxs-lookup"><span data-stu-id="173e1-485">Assembly</span></span></td>
<td><span data-ttu-id="173e1-486">55</span><span class="sxs-lookup"><span data-stu-id="173e1-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-487">CC004</span><span class="sxs-lookup"><span data-stu-id="173e1-487">CC004</span></span></td>
<td><span data-ttu-id="173e1-488">Balení</span><span class="sxs-lookup"><span data-stu-id="173e1-488">Packaging</span></span></td>
<td><span data-ttu-id="173e1-489">10</span><span class="sxs-lookup"><span data-stu-id="173e1-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="173e1-490">Objekt nákladů objektu CC002 Finance přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="173e1-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="173e1-491">Vytvoří se člen statistické dimenzi s názvem Finanční služby k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="173e1-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="173e1-492">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-492">Cost object</span></span></th>
<th><span data-ttu-id="173e1-493">Finanční služby</span><span class="sxs-lookup"><span data-stu-id="173e1-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="173e1-494">CC003</span><span class="sxs-lookup"><span data-stu-id="173e1-494">CC003</span></span></td>
<td><span data-ttu-id="173e1-495">Sestavení</span><span class="sxs-lookup"><span data-stu-id="173e1-495">Assembly</span></span></td>
<td><span data-ttu-id="173e1-496">65</span><span class="sxs-lookup"><span data-stu-id="173e1-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-497">CC004</span><span class="sxs-lookup"><span data-stu-id="173e1-497">CC004</span></span></td>
<td><span data-ttu-id="173e1-498">Balení</span><span class="sxs-lookup"><span data-stu-id="173e1-498">Packaging</span></span></td>
<td><span data-ttu-id="173e1-499">35</span><span class="sxs-lookup"><span data-stu-id="173e1-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="173e1-500">Objekt nákladů objektu CC003 Sestavení přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="173e1-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="173e1-501">Vytvoří se člen statistické dimenzi s názvem Služby sestavení zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="173e1-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="173e1-502">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-502">Cost object</span></span></th>
<th><span data-ttu-id="173e1-503">Služby sestavení (v hodinách)</span><span class="sxs-lookup"><span data-stu-id="173e1-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="173e1-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="173e1-504">Prod 1</span></span></td>
<td><span data-ttu-id="173e1-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="173e1-505">Product 1</span></span></td>
<td><span data-ttu-id="173e1-506">60</span><span class="sxs-lookup"><span data-stu-id="173e1-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="173e1-507">Prod 2</span></span></td>
<td><span data-ttu-id="173e1-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="173e1-508">Product 2</span></span></td>
<td><span data-ttu-id="173e1-509">20</span><span class="sxs-lookup"><span data-stu-id="173e1-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="173e1-510">Objekt nákladů objektu CC004 Balení přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="173e1-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="173e1-511">Vytvoří se člen statistické dimenzi s názvem Služby balení k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="173e1-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="173e1-512">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-512">Cost object</span></span></th>
<th><span data-ttu-id="173e1-513">Služby balení (v hodinách)</span><span class="sxs-lookup"><span data-stu-id="173e1-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="173e1-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="173e1-514">Prod 1</span></span></td>
<td><span data-ttu-id="173e1-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="173e1-515">Product 1</span></span></td>
<td><span data-ttu-id="173e1-516">80</span><span class="sxs-lookup"><span data-stu-id="173e1-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="173e1-517">Prod 2</span></span></td>
<td><span data-ttu-id="173e1-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="173e1-518">Product 2</span></span></td>
<td><span data-ttu-id="173e1-519">15</span><span class="sxs-lookup"><span data-stu-id="173e1-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="173e1-520">Statistická měření, jako je například výrobní doba spotřebovaná produktem, lze odvodit z datového zdroje.</span><span class="sxs-lookup"><span data-stu-id="173e1-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="173e1-521">Více informací naleznete v části [Šablona poskytovatele statistického měření](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="173e1-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="173e1-522">V následující tabulce je uveden výsledek při použití služeb HR jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="173e1-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="173e1-523">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-523">Cost object</span></span></th>
<th><span data-ttu-id="173e1-524">Hodnota</span><span class="sxs-lookup"><span data-stu-id="173e1-524">Magnitude</span></span></th>
<th><span data-ttu-id="173e1-525">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="173e1-525">Allocation factor</span></span></th>
<th><span data-ttu-id="173e1-526">Částka</span><span class="sxs-lookup"><span data-stu-id="173e1-526">Amount</span></span></th>
<th><span data-ttu-id="173e1-527">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="173e1-528">CC002</span><span class="sxs-lookup"><span data-stu-id="173e1-528">CC002</span></span></td>
<td><span data-ttu-id="173e1-529">Finance</span><span class="sxs-lookup"><span data-stu-id="173e1-529">Finance</span></span></td>
<td><span data-ttu-id="173e1-530">35</span><span class="sxs-lookup"><span data-stu-id="173e1-530">35</span></span></td>
<td><span data-ttu-id="173e1-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="173e1-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="173e1-532">175.00</span><span class="sxs-lookup"><span data-stu-id="173e1-532">175.00</span></span></td>
<td><span data-ttu-id="173e1-533">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-534">CC003</span><span class="sxs-lookup"><span data-stu-id="173e1-534">CC003</span></span></td>
<td><span data-ttu-id="173e1-535">Sestavení</span><span class="sxs-lookup"><span data-stu-id="173e1-535">Assembly</span></span></td>
<td><span data-ttu-id="173e1-536">55</span><span class="sxs-lookup"><span data-stu-id="173e1-536">55</span></span></td>
<td><span data-ttu-id="173e1-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="173e1-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="173e1-538">275.00</span><span class="sxs-lookup"><span data-stu-id="173e1-538">275.00</span></span></td>
<td><span data-ttu-id="173e1-539">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-540">CC004</span><span class="sxs-lookup"><span data-stu-id="173e1-540">CC004</span></span></td>
<td><span data-ttu-id="173e1-541">Balení</span><span class="sxs-lookup"><span data-stu-id="173e1-541">Packaging</span></span></td>
<td><span data-ttu-id="173e1-542">10</span><span class="sxs-lookup"><span data-stu-id="173e1-542">10</span></span></td>
<td><span data-ttu-id="173e1-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="173e1-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="173e1-544">50,00</span><span class="sxs-lookup"><span data-stu-id="173e1-544">50.00</span></span></td>
<td><span data-ttu-id="173e1-545">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-546">CC002</span><span class="sxs-lookup"><span data-stu-id="173e1-546">CC002</span></span></td>
<td><span data-ttu-id="173e1-547">Finance</span><span class="sxs-lookup"><span data-stu-id="173e1-547">Finance</span></span></td>
<td><span data-ttu-id="173e1-548">35</span><span class="sxs-lookup"><span data-stu-id="173e1-548">35</span></span></td>
<td><span data-ttu-id="173e1-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="173e1-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="173e1-550">436.00</span><span class="sxs-lookup"><span data-stu-id="173e1-550">436.00</span></span></td>
<td><span data-ttu-id="173e1-551">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-552">CC003</span><span class="sxs-lookup"><span data-stu-id="173e1-552">CC003</span></span></td>
<td><span data-ttu-id="173e1-553">Sestavení</span><span class="sxs-lookup"><span data-stu-id="173e1-553">Assembly</span></span></td>
<td><span data-ttu-id="173e1-554">55</span><span class="sxs-lookup"><span data-stu-id="173e1-554">55</span></span></td>
<td><span data-ttu-id="173e1-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="173e1-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="173e1-556">685.14</span><span class="sxs-lookup"><span data-stu-id="173e1-556">685.14</span></span></td>
<td><span data-ttu-id="173e1-557">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-558">CC004</span><span class="sxs-lookup"><span data-stu-id="173e1-558">CC004</span></span></td>
<td><span data-ttu-id="173e1-559">Balení</span><span class="sxs-lookup"><span data-stu-id="173e1-559">Packaging</span></span></td>
<td><span data-ttu-id="173e1-560">10</span><span class="sxs-lookup"><span data-stu-id="173e1-560">10</span></span></td>
<td><span data-ttu-id="173e1-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="173e1-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="173e1-562">124.57</span><span class="sxs-lookup"><span data-stu-id="173e1-562">124.57</span></span></td>
<td><span data-ttu-id="173e1-563">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="173e1-564">V následující tabulce je uveden výsledek při použití Finančních služeb Finance jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="173e1-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="173e1-565">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-565">Cost object</span></span></th>
<th><span data-ttu-id="173e1-566">Hodnota</span><span class="sxs-lookup"><span data-stu-id="173e1-566">Magnitude</span></span></th>
<th><span data-ttu-id="173e1-567">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="173e1-567">Allocation factor</span></span></th>
<th><span data-ttu-id="173e1-568">Částka</span><span class="sxs-lookup"><span data-stu-id="173e1-568">Amount</span></span></th>
<th><span data-ttu-id="173e1-569">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="173e1-570">CC003</span><span class="sxs-lookup"><span data-stu-id="173e1-570">CC003</span></span></td>
<td><span data-ttu-id="173e1-571">Sestavení</span><span class="sxs-lookup"><span data-stu-id="173e1-571">Assembly</span></span></td>
<td><span data-ttu-id="173e1-572">65</span><span class="sxs-lookup"><span data-stu-id="173e1-572">65</span></span></td>
<td><span data-ttu-id="173e1-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="173e1-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="173e1-574">438.75</span><span class="sxs-lookup"><span data-stu-id="173e1-574">438.75</span></span></td>
<td><span data-ttu-id="173e1-575">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-576">CC004</span><span class="sxs-lookup"><span data-stu-id="173e1-576">CC004</span></span></td>
<td><span data-ttu-id="173e1-577">Balení</span><span class="sxs-lookup"><span data-stu-id="173e1-577">Packaging</span></span></td>
<td><span data-ttu-id="173e1-578">35</span><span class="sxs-lookup"><span data-stu-id="173e1-578">35</span></span></td>
<td><span data-ttu-id="173e1-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="173e1-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="173e1-580">236.25</span><span class="sxs-lookup"><span data-stu-id="173e1-580">236.25</span></span></td>
<td><span data-ttu-id="173e1-581">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-582">CC003</span><span class="sxs-lookup"><span data-stu-id="173e1-582">CC003</span></span></td>
<td><span data-ttu-id="173e1-583">Sestavení</span><span class="sxs-lookup"><span data-stu-id="173e1-583">Assembly</span></span></td>
<td><span data-ttu-id="173e1-584">65</span><span class="sxs-lookup"><span data-stu-id="173e1-584">65</span></span></td>
<td><span data-ttu-id="173e1-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="173e1-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="173e1-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="173e1-586">5,297.69</span></span></td>
<td><span data-ttu-id="173e1-587">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-588">CC004</span><span class="sxs-lookup"><span data-stu-id="173e1-588">CC004</span></span></td>
<td><span data-ttu-id="173e1-589">Balení</span><span class="sxs-lookup"><span data-stu-id="173e1-589">Packaging</span></span></td>
<td><span data-ttu-id="173e1-590">35</span><span class="sxs-lookup"><span data-stu-id="173e1-590">35</span></span></td>
<td><span data-ttu-id="173e1-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="173e1-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="173e1-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="173e1-592">2,852.60</span></span></td>
<td><span data-ttu-id="173e1-593">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="173e1-594">V následující tabulce je uveden výsledek při použití Služeb sestavení jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="173e1-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="173e1-595">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-595">Cost object</span></span></th>
<th><span data-ttu-id="173e1-596">Hodnota</span><span class="sxs-lookup"><span data-stu-id="173e1-596">Magnitude</span></span></th>
<th><span data-ttu-id="173e1-597">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="173e1-597">Allocation factor</span></span></th>
<th><span data-ttu-id="173e1-598">Částka</span><span class="sxs-lookup"><span data-stu-id="173e1-598">Amount</span></span></th>
<th><span data-ttu-id="173e1-599">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="173e1-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="173e1-600">Prod 1</span></span></td>
<td><span data-ttu-id="173e1-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="173e1-601">Product 1</span></span></td>
<td><span data-ttu-id="173e1-602">60</span><span class="sxs-lookup"><span data-stu-id="173e1-602">60</span></span></td>
<td><span data-ttu-id="173e1-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="173e1-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="173e1-604">535.31</span><span class="sxs-lookup"><span data-stu-id="173e1-604">535.31</span></span></td>
<td><span data-ttu-id="173e1-605">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="173e1-606">Prod 2</span></span></td>
<td><span data-ttu-id="173e1-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="173e1-607">Product 2</span></span></td>
<td><span data-ttu-id="173e1-608">20</span><span class="sxs-lookup"><span data-stu-id="173e1-608">20</span></span></td>
<td><span data-ttu-id="173e1-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="173e1-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="173e1-610">178.44</span><span class="sxs-lookup"><span data-stu-id="173e1-610">178.44</span></span></td>
<td><span data-ttu-id="173e1-611">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="173e1-612">Prod 1</span></span></td>
<td><span data-ttu-id="173e1-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="173e1-613">Product 1</span></span></td>
<td><span data-ttu-id="173e1-614">60</span><span class="sxs-lookup"><span data-stu-id="173e1-614">60</span></span></td>
<td><span data-ttu-id="173e1-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="173e1-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="173e1-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="173e1-616">4,487.12</span></span></td>
<td><span data-ttu-id="173e1-617">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="173e1-618">Prod 2</span></span></td>
<td><span data-ttu-id="173e1-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="173e1-619">Product 2</span></span></td>
<td><span data-ttu-id="173e1-620">20</span><span class="sxs-lookup"><span data-stu-id="173e1-620">20</span></span></td>
<td><span data-ttu-id="173e1-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="173e1-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="173e1-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="173e1-622">1,495.71</span></span></td>
<td><span data-ttu-id="173e1-623">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="173e1-624">V následující tabulce je uveden výsledek při použití Služeb balení jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="173e1-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="173e1-625">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-625">Cost object</span></span></th>
<th><span data-ttu-id="173e1-626">Hodnota</span><span class="sxs-lookup"><span data-stu-id="173e1-626">Magnitude</span></span></th>
<th><span data-ttu-id="173e1-627">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="173e1-627">Allocation factor</span></span></th>
<th><span data-ttu-id="173e1-628">Částka</span><span class="sxs-lookup"><span data-stu-id="173e1-628">Amount</span></span></th>
<th><span data-ttu-id="173e1-629">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="173e1-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="173e1-630">Prod 1</span></span></td>
<td><span data-ttu-id="173e1-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="173e1-631">Product 1</span></span></td>
<td><span data-ttu-id="173e1-632">80</span><span class="sxs-lookup"><span data-stu-id="173e1-632">80</span></span></td>
<td><span data-ttu-id="173e1-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="173e1-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="173e1-634">241.05</span><span class="sxs-lookup"><span data-stu-id="173e1-634">241.05</span></span></td>
<td><span data-ttu-id="173e1-635">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="173e1-636">Prod 2</span></span></td>
<td><span data-ttu-id="173e1-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="173e1-637">Product 2</span></span></td>
<td><span data-ttu-id="173e1-638">15</span><span class="sxs-lookup"><span data-stu-id="173e1-638">15</span></span></td>
<td><span data-ttu-id="173e1-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="173e1-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="173e1-640">45.20</span><span class="sxs-lookup"><span data-stu-id="173e1-640">45.20</span></span></td>
<td><span data-ttu-id="173e1-641">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="173e1-642">Prod 1</span></span></td>
<td><span data-ttu-id="173e1-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="173e1-643">Product 1</span></span></td>
<td><span data-ttu-id="173e1-644">80</span><span class="sxs-lookup"><span data-stu-id="173e1-644">80</span></span></td>
<td><span data-ttu-id="173e1-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="173e1-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="173e1-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="173e1-646">2,507.09</span></span></td>
<td><span data-ttu-id="173e1-647">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="173e1-648">Prod 2</span></span></td>
<td><span data-ttu-id="173e1-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="173e1-649">Product 2</span></span></td>
<td><span data-ttu-id="173e1-650">15</span><span class="sxs-lookup"><span data-stu-id="173e1-650">15</span></span></td>
<td><span data-ttu-id="173e1-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="173e1-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="173e1-652">470.08</span><span class="sxs-lookup"><span data-stu-id="173e1-652">470.08</span></span></td>
<td><span data-ttu-id="173e1-653">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="173e1-654">Položky deníku (položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="173e1-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="173e1-655">Deník</span><span class="sxs-lookup"><span data-stu-id="173e1-655">Journal</span></span></th>
<th><span data-ttu-id="173e1-656">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="173e1-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="173e1-657">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="173e1-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="173e1-658">Verze</span><span class="sxs-lookup"><span data-stu-id="173e1-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="173e1-659">00004</span><span class="sxs-lookup"><span data-stu-id="173e1-659">00004</span></span></td>
<td><span data-ttu-id="173e1-660">Deník přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="173e1-661">Fiskální</span><span class="sxs-lookup"><span data-stu-id="173e1-661">Fiscal</span></span></td>
<td><span data-ttu-id="173e1-662">2017</span><span class="sxs-lookup"><span data-stu-id="173e1-662">2017</span></span></td>
<td><span data-ttu-id="173e1-663">Období 1</span><span class="sxs-lookup"><span data-stu-id="173e1-663">Period 1</span></span></td>
<td><span data-ttu-id="173e1-664">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="173e1-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="173e1-665">Řádky deníku</span><span class="sxs-lookup"><span data-stu-id="173e1-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="173e1-666">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="173e1-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="173e1-667">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="173e1-668">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-668">Cost element</span></span></th>
<th><span data-ttu-id="173e1-669">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-669">Cost behavior</span></span></th>
<th><span data-ttu-id="173e1-670">Částka</span><span class="sxs-lookup"><span data-stu-id="173e1-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="173e1-671">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="173e1-672">CC001</span><span class="sxs-lookup"><span data-stu-id="173e1-672">CC001</span></span></td>
<td><span data-ttu-id="173e1-673">HR</span><span class="sxs-lookup"><span data-stu-id="173e1-673">HR</span></span></td>
<td><span data-ttu-id="173e1-674">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-674">10001</span></span></td>
<td><span data-ttu-id="173e1-675">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-675">Electricity</span></span></td>
<td><span data-ttu-id="173e1-676">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-676">Fixed cost</span></span></td>
<td><span data-ttu-id="173e1-677">500.00</span><span class="sxs-lookup"><span data-stu-id="173e1-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-678">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="173e1-679">CC001</span><span class="sxs-lookup"><span data-stu-id="173e1-679">CC001</span></span></td>
<td><span data-ttu-id="173e1-680">HR</span><span class="sxs-lookup"><span data-stu-id="173e1-680">HR</span></span></td>
<td><span data-ttu-id="173e1-681">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-681">10001</span></span></td>
<td><span data-ttu-id="173e1-682">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-682">Electricity</span></span></td>
<td><span data-ttu-id="173e1-683">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-683">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="173e1-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-685">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="173e1-686">CC002</span><span class="sxs-lookup"><span data-stu-id="173e1-686">CC002</span></span></td>
<td><span data-ttu-id="173e1-687">Finance</span><span class="sxs-lookup"><span data-stu-id="173e1-687">Finance</span></span></td>
<td><span data-ttu-id="173e1-688">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-688">10001</span></span></td>
<td><span data-ttu-id="173e1-689">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-689">Electricity</span></span></td>
<td><span data-ttu-id="173e1-690">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-690">Fixed cost</span></span></td>
<td><span data-ttu-id="173e1-691">675.00</span><span class="sxs-lookup"><span data-stu-id="173e1-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-692">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="173e1-693">CC002</span><span class="sxs-lookup"><span data-stu-id="173e1-693">CC002</span></span></td>
<td><span data-ttu-id="173e1-694">Finance</span><span class="sxs-lookup"><span data-stu-id="173e1-694">Finance</span></span></td>
<td><span data-ttu-id="173e1-695">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-695">10001</span></span></td>
<td><span data-ttu-id="173e1-696">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-696">Electricity</span></span></td>
<td><span data-ttu-id="173e1-697">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-697">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="173e1-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-699">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="173e1-700">CC003</span><span class="sxs-lookup"><span data-stu-id="173e1-700">CC003</span></span></td>
<td><span data-ttu-id="173e1-701">Sestavení</span><span class="sxs-lookup"><span data-stu-id="173e1-701">Assembly</span></span></td>
<td><span data-ttu-id="173e1-702">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-702">10001</span></span></td>
<td><span data-ttu-id="173e1-703">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-703">Electricity</span></span></td>
<td><span data-ttu-id="173e1-704">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-704">Fixed cost</span></span></td>
<td><span data-ttu-id="173e1-705">713.75</span><span class="sxs-lookup"><span data-stu-id="173e1-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-706">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="173e1-707">CC003</span><span class="sxs-lookup"><span data-stu-id="173e1-707">CC003</span></span></td>
<td><span data-ttu-id="173e1-708">Sestavení</span><span class="sxs-lookup"><span data-stu-id="173e1-708">Assembly</span></span></td>
<td><span data-ttu-id="173e1-709">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-709">10001</span></span></td>
<td><span data-ttu-id="173e1-710">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-710">Electricity</span></span></td>
<td><span data-ttu-id="173e1-711">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-711">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="173e1-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-713">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="173e1-714">CC003</span><span class="sxs-lookup"><span data-stu-id="173e1-714">CC003</span></span></td>
<td><span data-ttu-id="173e1-715">Balení</span><span class="sxs-lookup"><span data-stu-id="173e1-715">Packaging</span></span></td>
<td><span data-ttu-id="173e1-716">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-716">10001</span></span></td>
<td><span data-ttu-id="173e1-717">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-717">Electricity</span></span></td>
<td><span data-ttu-id="173e1-718">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-718">Fixed cost</span></span></td>
<td><span data-ttu-id="173e1-719">286.25</span><span class="sxs-lookup"><span data-stu-id="173e1-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-720">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="173e1-721">CC003</span><span class="sxs-lookup"><span data-stu-id="173e1-721">CC003</span></span></td>
<td><span data-ttu-id="173e1-722">Balení</span><span class="sxs-lookup"><span data-stu-id="173e1-722">Packaging</span></span></td>
<td><span data-ttu-id="173e1-723">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-723">10001</span></span></td>
<td><span data-ttu-id="173e1-724">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-724">Electricity</span></span></td>
<td><span data-ttu-id="173e1-725">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-725">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="173e1-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-727">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="173e1-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="173e1-728">Prod 1</span></span></td>
<td><span data-ttu-id="173e1-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="173e1-729">Product 1</span></span></td>
<td><span data-ttu-id="173e1-730">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-730">10001</span></span></td>
<td><span data-ttu-id="173e1-731">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-731">Electricity</span></span></td>
<td><span data-ttu-id="173e1-732">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-732">Fixed cost</span></span></td>
<td><span data-ttu-id="173e1-733">776.36</span><span class="sxs-lookup"><span data-stu-id="173e1-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-734">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="173e1-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="173e1-735">Prod 1</span></span></td>
<td><span data-ttu-id="173e1-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="173e1-736">Product 1</span></span></td>
<td><span data-ttu-id="173e1-737">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-737">10001</span></span></td>
<td><span data-ttu-id="173e1-738">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-738">Electricity</span></span></td>
<td><span data-ttu-id="173e1-739">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-739">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="173e1-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-741">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="173e1-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="173e1-742">Prod 2</span></span></td>
<td><span data-ttu-id="173e1-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="173e1-743">Product 1</span></span></td>
<td><span data-ttu-id="173e1-744">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-744">10001</span></span></td>
<td><span data-ttu-id="173e1-745">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-745">Electricity</span></span></td>
<td><span data-ttu-id="173e1-746">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-746">Fixed cost</span></span></td>
<td><span data-ttu-id="173e1-747">223.64</span><span class="sxs-lookup"><span data-stu-id="173e1-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-748">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="173e1-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="173e1-749">Prod 2</span></span></td>
<td><span data-ttu-id="173e1-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="173e1-750">Product 1</span></span></td>
<td><span data-ttu-id="173e1-751">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-751">10001</span></span></td>
<td><span data-ttu-id="173e1-752">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-752">Electricity</span></span></td>
<td><span data-ttu-id="173e1-753">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-753">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="173e1-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="173e1-755">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="173e1-756">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="173e1-757">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-757">Cost element</span></span></th>
<th><span data-ttu-id="173e1-758">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-758">Cost behavior</span></span></th>
<th><span data-ttu-id="173e1-759">Částka</span><span class="sxs-lookup"><span data-stu-id="173e1-759">Amount</span></span></th>
<th><span data-ttu-id="173e1-760">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="173e1-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="173e1-761">CC001</span><span class="sxs-lookup"><span data-stu-id="173e1-761">CC001</span></span></td>
<td><span data-ttu-id="173e1-762">HR</span><span class="sxs-lookup"><span data-stu-id="173e1-762">HR</span></span></td>
<td><span data-ttu-id="173e1-763">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-763">10001</span></span></td>
<td><span data-ttu-id="173e1-764">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-764">Electricity</span></span></td>
<td><span data-ttu-id="173e1-765">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-765">Fixed cost</span></span></td>
<td><span data-ttu-id="173e1-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="173e1-766">-500.00</span></span></td>
<td><span data-ttu-id="173e1-767">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-768">CC002</span><span class="sxs-lookup"><span data-stu-id="173e1-768">CC002</span></span></td>
<td><span data-ttu-id="173e1-769">Finance</span><span class="sxs-lookup"><span data-stu-id="173e1-769">Finance</span></span></td>
<td><span data-ttu-id="173e1-770">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-770">10001</span></span></td>
<td><span data-ttu-id="173e1-771">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-771">Electricity</span></span></td>
<td><span data-ttu-id="173e1-772">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-772">Fixed cost</span></span></td>
<td><span data-ttu-id="173e1-773">175.00</span><span class="sxs-lookup"><span data-stu-id="173e1-773">175.00</span></span></td>
<td><span data-ttu-id="173e1-774">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-775">CC003</span><span class="sxs-lookup"><span data-stu-id="173e1-775">CC003</span></span></td>
<td><span data-ttu-id="173e1-776">Sestavení</span><span class="sxs-lookup"><span data-stu-id="173e1-776">Assembly</span></span></td>
<td><span data-ttu-id="173e1-777">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-777">10001</span></span></td>
<td><span data-ttu-id="173e1-778">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-778">Electricity</span></span></td>
<td><span data-ttu-id="173e1-779">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-779">Fixed cost</span></span></td>
<td><span data-ttu-id="173e1-780">275.00</span><span class="sxs-lookup"><span data-stu-id="173e1-780">275.00</span></span></td>
<td><span data-ttu-id="173e1-781">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-782">CC004</span><span class="sxs-lookup"><span data-stu-id="173e1-782">CC004</span></span></td>
<td><span data-ttu-id="173e1-783">Balení</span><span class="sxs-lookup"><span data-stu-id="173e1-783">Packaging</span></span></td>
<td><span data-ttu-id="173e1-784">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-784">10001</span></span></td>
<td><span data-ttu-id="173e1-785">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-785">Electricity</span></span></td>
<td><span data-ttu-id="173e1-786">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-786">Fixed cost</span></span></td>
<td><span data-ttu-id="173e1-787">50,00</span><span class="sxs-lookup"><span data-stu-id="173e1-787">50,00</span></span></td>
<td><span data-ttu-id="173e1-788">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-789">CC001</span><span class="sxs-lookup"><span data-stu-id="173e1-789">CC001</span></span></td>
<td><span data-ttu-id="173e1-790">HR</span><span class="sxs-lookup"><span data-stu-id="173e1-790">HR</span></span></td>
<td><span data-ttu-id="173e1-791">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-791">10001</span></span></td>
<td><span data-ttu-id="173e1-792">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-792">Electricity</span></span></td>
<td><span data-ttu-id="173e1-793">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-793">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-794">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="173e1-794">-1,245.71</span></span></td>
<td><span data-ttu-id="173e1-795">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-796">CC002</span><span class="sxs-lookup"><span data-stu-id="173e1-796">CC002</span></span></td>
<td><span data-ttu-id="173e1-797">Finance</span><span class="sxs-lookup"><span data-stu-id="173e1-797">Finance</span></span></td>
<td><span data-ttu-id="173e1-798">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-798">10001</span></span></td>
<td><span data-ttu-id="173e1-799">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-799">Electricity</span></span></td>
<td><span data-ttu-id="173e1-800">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-800">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-801">436.00</span><span class="sxs-lookup"><span data-stu-id="173e1-801">436.00</span></span></td>
<td><span data-ttu-id="173e1-802">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-803">CC003</span><span class="sxs-lookup"><span data-stu-id="173e1-803">CC003</span></span></td>
<td><span data-ttu-id="173e1-804">Sestavení</span><span class="sxs-lookup"><span data-stu-id="173e1-804">Assembly</span></span></td>
<td><span data-ttu-id="173e1-805">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-805">10001</span></span></td>
<td><span data-ttu-id="173e1-806">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-806">Electricity</span></span></td>
<td><span data-ttu-id="173e1-807">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-807">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-808">685.14</span><span class="sxs-lookup"><span data-stu-id="173e1-808">685.14</span></span></td>
<td><span data-ttu-id="173e1-809">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-810">CC004</span><span class="sxs-lookup"><span data-stu-id="173e1-810">CC004</span></span></td>
<td><span data-ttu-id="173e1-811">Balení</span><span class="sxs-lookup"><span data-stu-id="173e1-811">Packaging</span></span></td>
<td><span data-ttu-id="173e1-812">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-812">10001</span></span></td>
<td><span data-ttu-id="173e1-813">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-813">Electricity</span></span></td>
<td><span data-ttu-id="173e1-814">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-814">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-815">124.57</span><span class="sxs-lookup"><span data-stu-id="173e1-815">124.57</span></span></td>
<td><span data-ttu-id="173e1-816">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-817">CC002</span><span class="sxs-lookup"><span data-stu-id="173e1-817">CC002</span></span></td>
<td><span data-ttu-id="173e1-818">Finance</span><span class="sxs-lookup"><span data-stu-id="173e1-818">Finance</span></span></td>
<td><span data-ttu-id="173e1-819">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-819">10001</span></span></td>
<td><span data-ttu-id="173e1-820">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-820">Electricity</span></span></td>
<td><span data-ttu-id="173e1-821">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-821">Fixed cost</span></span></td>
<td><span data-ttu-id="173e1-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="173e1-822">-675.00</span></span></td>
<td><span data-ttu-id="173e1-823">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-824">CC003</span><span class="sxs-lookup"><span data-stu-id="173e1-824">CC003</span></span></td>
<td><span data-ttu-id="173e1-825">Sestavení</span><span class="sxs-lookup"><span data-stu-id="173e1-825">Assembly</span></span></td>
<td><span data-ttu-id="173e1-826">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-826">10001</span></span></td>
<td><span data-ttu-id="173e1-827">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-827">Electricity</span></span></td>
<td><span data-ttu-id="173e1-828">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-828">Fixed cost</span></span></td>
<td><span data-ttu-id="173e1-829">438.75</span><span class="sxs-lookup"><span data-stu-id="173e1-829">438.75</span></span></td>
<td><span data-ttu-id="173e1-830">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-831">CC004</span><span class="sxs-lookup"><span data-stu-id="173e1-831">CC004</span></span></td>
<td><span data-ttu-id="173e1-832">Balení</span><span class="sxs-lookup"><span data-stu-id="173e1-832">Packaging</span></span></td>
<td><span data-ttu-id="173e1-833">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-833">10001</span></span></td>
<td><span data-ttu-id="173e1-834">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-834">Electricity</span></span></td>
<td><span data-ttu-id="173e1-835">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-835">Fixed cost</span></span></td>
<td><span data-ttu-id="173e1-836">236.25</span><span class="sxs-lookup"><span data-stu-id="173e1-836">236.25</span></span></td>
<td><span data-ttu-id="173e1-837">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-838">CC002</span><span class="sxs-lookup"><span data-stu-id="173e1-838">CC002</span></span></td>
<td><span data-ttu-id="173e1-839">Finance</span><span class="sxs-lookup"><span data-stu-id="173e1-839">Finance</span></span></td>
<td><span data-ttu-id="173e1-840">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-840">10001</span></span></td>
<td><span data-ttu-id="173e1-841">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-841">Electricity</span></span></td>
<td><span data-ttu-id="173e1-842">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-842">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-843">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="173e1-843">-8,150.29</span></span></td>
<td><span data-ttu-id="173e1-844">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-845">CC003</span><span class="sxs-lookup"><span data-stu-id="173e1-845">CC003</span></span></td>
<td><span data-ttu-id="173e1-846">Sestavení</span><span class="sxs-lookup"><span data-stu-id="173e1-846">Assembly</span></span></td>
<td><span data-ttu-id="173e1-847">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-847">10001</span></span></td>
<td><span data-ttu-id="173e1-848">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-848">Electricity</span></span></td>
<td><span data-ttu-id="173e1-849">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-849">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="173e1-850">5,297.69</span></span></td>
<td><span data-ttu-id="173e1-851">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-852">CC004</span><span class="sxs-lookup"><span data-stu-id="173e1-852">CC004</span></span></td>
<td><span data-ttu-id="173e1-853">Balení</span><span class="sxs-lookup"><span data-stu-id="173e1-853">Packaging</span></span></td>
<td><span data-ttu-id="173e1-854">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-854">10001</span></span></td>
<td><span data-ttu-id="173e1-855">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-855">Electricity</span></span></td>
<td><span data-ttu-id="173e1-856">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-856">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="173e1-857">2,852.60</span></span></td>
<td><span data-ttu-id="173e1-858">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-859">CC003</span><span class="sxs-lookup"><span data-stu-id="173e1-859">CC003</span></span></td>
<td><span data-ttu-id="173e1-860">Sestavení</span><span class="sxs-lookup"><span data-stu-id="173e1-860">Assembly</span></span></td>
<td><span data-ttu-id="173e1-861">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-861">10001</span></span></td>
<td><span data-ttu-id="173e1-862">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-862">Electricity</span></span></td>
<td><span data-ttu-id="173e1-863">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-863">Fixed cost</span></span></td>
<td><span data-ttu-id="173e1-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="173e1-864">-713.75</span></span></td>
<td><span data-ttu-id="173e1-865">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="173e1-866">Prod 1</span></span></td>
<td><span data-ttu-id="173e1-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="173e1-867">Product 1</span></span></td>
<td><span data-ttu-id="173e1-868">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-868">10001</span></span></td>
<td><span data-ttu-id="173e1-869">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-869">Electricity</span></span></td>
<td><span data-ttu-id="173e1-870">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-870">Fixed cost</span></span></td>
<td><span data-ttu-id="173e1-871">535.31</span><span class="sxs-lookup"><span data-stu-id="173e1-871">535.31</span></span></td>
<td><span data-ttu-id="173e1-872">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="173e1-873">Prod 2</span></span></td>
<td><span data-ttu-id="173e1-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="173e1-874">Product 2</span></span></td>
<td><span data-ttu-id="173e1-875">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-875">10001</span></span></td>
<td><span data-ttu-id="173e1-876">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-876">Electricity</span></span></td>
<td><span data-ttu-id="173e1-877">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-877">Fixed cost</span></span></td>
<td><span data-ttu-id="173e1-878">178.44</span><span class="sxs-lookup"><span data-stu-id="173e1-878">178.44</span></span></td>
<td><span data-ttu-id="173e1-879">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-880">CC003</span><span class="sxs-lookup"><span data-stu-id="173e1-880">CC003</span></span></td>
<td><span data-ttu-id="173e1-881">Sestavení</span><span class="sxs-lookup"><span data-stu-id="173e1-881">Assembly</span></span></td>
<td><span data-ttu-id="173e1-882">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-882">10001</span></span></td>
<td><span data-ttu-id="173e1-883">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-883">Electricity</span></span></td>
<td><span data-ttu-id="173e1-884">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-884">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-885">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="173e1-885">-5,982.83</span></span></td>
<td><span data-ttu-id="173e1-886">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="173e1-887">Prod 1</span></span></td>
<td><span data-ttu-id="173e1-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="173e1-888">Product 1</span></span></td>
<td><span data-ttu-id="173e1-889">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-889">10001</span></span></td>
<td><span data-ttu-id="173e1-890">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-890">Electricity</span></span></td>
<td><span data-ttu-id="173e1-891">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-891">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="173e1-892">4,487.12</span></span></td>
<td><span data-ttu-id="173e1-893">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="173e1-894">Prod 2</span></span></td>
<td><span data-ttu-id="173e1-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="173e1-895">Product 2</span></span></td>
<td><span data-ttu-id="173e1-896">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-896">10001</span></span></td>
<td><span data-ttu-id="173e1-897">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-897">Electricity</span></span></td>
<td><span data-ttu-id="173e1-898">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-898">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="173e1-899">1,495.71</span></span></td>
<td><span data-ttu-id="173e1-900">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-901">CC003</span><span class="sxs-lookup"><span data-stu-id="173e1-901">CC003</span></span></td>
<td><span data-ttu-id="173e1-902">Sestavení</span><span class="sxs-lookup"><span data-stu-id="173e1-902">Assembly</span></span></td>
<td><span data-ttu-id="173e1-903">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-903">10001</span></span></td>
<td><span data-ttu-id="173e1-904">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-904">Electricity</span></span></td>
<td><span data-ttu-id="173e1-905">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-905">Fixed cost</span></span></td>
<td><span data-ttu-id="173e1-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="173e1-906">-286.25</span></span></td>
<td><span data-ttu-id="173e1-907">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="173e1-908">Prod 1</span></span></td>
<td><span data-ttu-id="173e1-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="173e1-909">Product 1</span></span></td>
<td><span data-ttu-id="173e1-910">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-910">10001</span></span></td>
<td><span data-ttu-id="173e1-911">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-911">Electricity</span></span></td>
<td><span data-ttu-id="173e1-912">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-912">Fixed cost</span></span></td>
<td><span data-ttu-id="173e1-913">241.05</span><span class="sxs-lookup"><span data-stu-id="173e1-913">241.05</span></span></td>
<td><span data-ttu-id="173e1-914">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="173e1-915">Prod 2</span></span></td>
<td><span data-ttu-id="173e1-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="173e1-916">Product 2</span></span></td>
<td><span data-ttu-id="173e1-917">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-917">10001</span></span></td>
<td><span data-ttu-id="173e1-918">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-918">Electricity</span></span></td>
<td><span data-ttu-id="173e1-919">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-919">Fixed cost</span></span></td>
<td><span data-ttu-id="173e1-920">45.20</span><span class="sxs-lookup"><span data-stu-id="173e1-920">45.20</span></span></td>
<td><span data-ttu-id="173e1-921">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-922">CC003</span><span class="sxs-lookup"><span data-stu-id="173e1-922">CC003</span></span></td>
<td><span data-ttu-id="173e1-923">Sestavení</span><span class="sxs-lookup"><span data-stu-id="173e1-923">Assembly</span></span></td>
<td><span data-ttu-id="173e1-924">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-924">10001</span></span></td>
<td><span data-ttu-id="173e1-925">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-925">Electricity</span></span></td>
<td><span data-ttu-id="173e1-926">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-926">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="173e1-927">-2,977.17</span></span></td>
<td><span data-ttu-id="173e1-928">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="173e1-929">Prod 1</span></span></td>
<td><span data-ttu-id="173e1-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="173e1-930">Product 1</span></span></td>
<td><span data-ttu-id="173e1-931">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-931">10001</span></span></td>
<td><span data-ttu-id="173e1-932">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-932">Electricity</span></span></td>
<td><span data-ttu-id="173e1-933">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-933">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="173e1-934">2,507.09</span></span></td>
<td><span data-ttu-id="173e1-935">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="173e1-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="173e1-936">Prod 2</span></span></td>
<td><span data-ttu-id="173e1-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="173e1-937">Product 2</span></span></td>
<td><span data-ttu-id="173e1-938">10001</span><span class="sxs-lookup"><span data-stu-id="173e1-938">10001</span></span></td>
<td><span data-ttu-id="173e1-939">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="173e1-939">Electricity</span></span></td>
<td><span data-ttu-id="173e1-940">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-940">Variable cost</span></span></td>
<td><span data-ttu-id="173e1-941">470.08</span><span class="sxs-lookup"><span data-stu-id="173e1-941">470.08</span></span></td>
<td><span data-ttu-id="173e1-942">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="173e1-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="173e1-943">Závěr</span><span class="sxs-lookup"><span data-stu-id="173e1-943">Conclusion</span></span>
<span data-ttu-id="173e1-944">Ve finančním účtování se náklady za elektřinu ve výši 10 000 zaúčtují na ID fiktivního nákladového střediska.</span><span class="sxs-lookup"><span data-stu-id="173e1-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="173e1-945">Účetní tak budou vědět, že tento náklad musí být přidělen.</span><span class="sxs-lookup"><span data-stu-id="173e1-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="173e1-946">V nákladovém účetnictví náklady procházejí napříč organizačními jednotkami a úrovněmi, na základě použitých zásad a pravidel.</span><span class="sxs-lookup"><span data-stu-id="173e1-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="173e1-947">Každý náklad byl přidružen k základu přidělení, který poskytuje nejlepší hodnocení pro přidělení nákladů.</span><span class="sxs-lookup"><span data-stu-id="173e1-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="173e1-948">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="173e1-949">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="173e1-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="173e1-950">Celkem</span><span class="sxs-lookup"><span data-stu-id="173e1-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="173e1-951">CC099</span><span class="sxs-lookup"><span data-stu-id="173e1-951">CC099</span></span></th>
<th><span data-ttu-id="173e1-952">CC001</span><span class="sxs-lookup"><span data-stu-id="173e1-952">CC001</span></span></th>
<th><span data-ttu-id="173e1-953">CC002</span><span class="sxs-lookup"><span data-stu-id="173e1-953">CC002</span></span></th>
<th><span data-ttu-id="173e1-954">CC003</span><span class="sxs-lookup"><span data-stu-id="173e1-954">CC003</span></span></th>
<th><span data-ttu-id="173e1-955">CC004</span><span class="sxs-lookup"><span data-stu-id="173e1-955">CC004</span></span></th>
<th><span data-ttu-id="173e1-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="173e1-956">Proj 1</span></span></th>
<th><span data-ttu-id="173e1-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="173e1-957">Proj 2</span></span></th>
<th><span data-ttu-id="173e1-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="173e1-958">Prod 1</span></span></th>
<th><span data-ttu-id="173e1-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="173e1-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="173e1-960">10001 Elektřina</span><span class="sxs-lookup"><span data-stu-id="173e1-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="173e1-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="173e1-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="173e1-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="173e1-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="173e1-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="173e1-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="173e1-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="173e1-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="173e1-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="173e1-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="173e1-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="173e1-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="173e1-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="173e1-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="173e1-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="173e1-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="173e1-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="173e1-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="173e1-970">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="173e1-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="173e1-971">0,00</span><span class="sxs-lookup"><span data-stu-id="173e1-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="173e1-972">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="173e1-973">0,00</span><span class="sxs-lookup"><span data-stu-id="173e1-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="173e1-974">0,00</span><span class="sxs-lookup"><span data-stu-id="173e1-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="173e1-975">0,00</span><span class="sxs-lookup"><span data-stu-id="173e1-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="173e1-976">0,00</span><span class="sxs-lookup"><span data-stu-id="173e1-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="173e1-977">0,00</span><span class="sxs-lookup"><span data-stu-id="173e1-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="173e1-978">776.36</span><span class="sxs-lookup"><span data-stu-id="173e1-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="173e1-979">223.64</span><span class="sxs-lookup"><span data-stu-id="173e1-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="173e1-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="173e1-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="173e1-981">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="173e1-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="173e1-982">000</span><span class="sxs-lookup"><span data-stu-id="173e1-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="173e1-983">0,00</span><span class="sxs-lookup"><span data-stu-id="173e1-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="173e1-984">0,00</span><span class="sxs-lookup"><span data-stu-id="173e1-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="173e1-985">0,00</span><span class="sxs-lookup"><span data-stu-id="173e1-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="173e1-986">0,00</span><span class="sxs-lookup"><span data-stu-id="173e1-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="173e1-987">30.00</span><span class="sxs-lookup"><span data-stu-id="173e1-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="173e1-988">10,00</span><span class="sxs-lookup"><span data-stu-id="173e1-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="173e1-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="173e1-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="173e1-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="173e1-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="173e1-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="173e1-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="173e1-992">Toto téma popisuje, jak primární prvek nákladů, 10001 Elektřina, prochází přes objekty nákladů.</span><span class="sxs-lookup"><span data-stu-id="173e1-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="173e1-993">Tyto režijní náklady tedy budou přiděleny na nejnižší úroveň v organizaci.</span><span class="sxs-lookup"><span data-stu-id="173e1-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="173e1-994">Jinak řečeno, objekty nákladů na nejnižší úrovni ponesou náklady.</span><span class="sxs-lookup"><span data-stu-id="173e1-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="173e1-995">Chcete-li vizuální tok nákladů mezi objekty nákladů, můžete použít pravidla zásad shrnutí nákladů pro vizualizaci jejich toků.</span><span class="sxs-lookup"><span data-stu-id="173e1-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="173e1-996">Další informace naleznete v tématu [Zásady shrnutí nákladů a výpočet režijních nákladů](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="173e1-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]