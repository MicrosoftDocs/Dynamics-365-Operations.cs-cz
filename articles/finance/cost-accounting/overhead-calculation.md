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
ms.openlocfilehash: 2dddc22128621dc148a253cd568430587f294544
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822896"
---
# <a name="overhead-calculation"></a><span data-ttu-id="8f7de-103">Výpočet režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8f7de-104">Toto téma popisuje typické procesy pro výpočet a přidělení režijních nákladů.</span><span class="sxs-lookup"><span data-stu-id="8f7de-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="8f7de-105">Definice termínu</span><span class="sxs-lookup"><span data-stu-id="8f7de-105">Term definition</span></span>
---------------

<span data-ttu-id="8f7de-106">Režijní náklady jsou náklady, které nutně vznikají při chodu podnikání, ale nelze je připsat přímo k žádné konkrétní podnikatelské aktivitě, produktu nebo službě.</span><span class="sxs-lookup"><span data-stu-id="8f7de-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="8f7de-107">Režijní náklady poskytují důležitou podporu pro generování aktivity přinášejících zisk.</span><span class="sxs-lookup"><span data-stu-id="8f7de-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="8f7de-108">Následuje několik příkladů režijních nákladů:</span><span class="sxs-lookup"><span data-stu-id="8f7de-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="8f7de-109">Renta</span><span class="sxs-lookup"><span data-stu-id="8f7de-109">Rent</span></span>
-   <span data-ttu-id="8f7de-110">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-110">Electricity</span></span>
-   <span data-ttu-id="8f7de-111">Administrativní mzdy</span><span class="sxs-lookup"><span data-stu-id="8f7de-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="8f7de-112">Přehled výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-112">Overhead calculation overview</span></span>
<span data-ttu-id="8f7de-113">Výpočet režijních nákladů spustí zásady účtování nákladů ve správném pořadí.</span><span class="sxs-lookup"><span data-stu-id="8f7de-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="8f7de-114">Výpočet režijních nákladů můžete pro stejné fiskální období spustit mnohokrát, pokud došlo ke změně zásad účtování nákladů nebo zjištění konkrétních chyb.</span><span class="sxs-lookup"><span data-stu-id="8f7de-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="8f7de-115">Každé spuštění výpočtu režijních nákladů se ukládá a přijímá ID jedinečné verze, které vám umožní porovnávat výpočty v různých verzích.</span><span class="sxs-lookup"><span data-stu-id="8f7de-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="8f7de-116">Položky nákladů, které generuje výpočet režijních nákladů, přijímá datum účtování.</span><span class="sxs-lookup"><span data-stu-id="8f7de-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="8f7de-117">Toto datum účtován se shoduje s konvovým datem fiskálního období, které se použije ve výpočtu.</span><span class="sxs-lookup"><span data-stu-id="8f7de-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="8f7de-118">ID jedinečné verze se skládá z následujících prvků:</span><span class="sxs-lookup"><span data-stu-id="8f7de-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="8f7de-119">Typ verze</span><span class="sxs-lookup"><span data-stu-id="8f7de-119">Version type</span></span>
-   <span data-ttu-id="8f7de-120">Datum a čas</span><span class="sxs-lookup"><span data-stu-id="8f7de-120">Date and time</span></span>
-   <span data-ttu-id="8f7de-121">Hlavní kniha nákladového účetnictví</span><span class="sxs-lookup"><span data-stu-id="8f7de-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="8f7de-122">Fiskální rok</span><span class="sxs-lookup"><span data-stu-id="8f7de-122">Fiscal year</span></span>
-   <span data-ttu-id="8f7de-123">Fiskální období</span><span class="sxs-lookup"><span data-stu-id="8f7de-123">Fiscal period</span></span>

<span data-ttu-id="8f7de-124">Výpočet režijních nákladů se spustí bez ohledu na verzi.</span><span class="sxs-lookup"><span data-stu-id="8f7de-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="8f7de-125">Proto lze vypočítat rozpočtovou verzi před skutečnou verzí.</span><span class="sxs-lookup"><span data-stu-id="8f7de-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="8f7de-126">Výpočet režijních nákladů se skládá ze čtyř kroků uvedených na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="8f7de-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="8f7de-127">V každé fázi je vytvořeno záhlaví deníku, které obsahuje položky deníku.</span><span class="sxs-lookup"><span data-stu-id="8f7de-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="8f7de-128">Toto záhlaví deníku zachovává vstupní data pro každý krok výpočtu.</span><span class="sxs-lookup"><span data-stu-id="8f7de-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="8f7de-129">Zásady a pravidla se použijí na každý řádek deníku a položky nákladů jsou generovány jako výstup.</span><span class="sxs-lookup"><span data-stu-id="8f7de-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="8f7de-130">Máte tedy vždy plnou sledovatelnost.</span><span class="sxs-lookup"><span data-stu-id="8f7de-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="8f7de-131">[![Výpočet režijních nákladů](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="8f7de-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="8f7de-132">Výpočet a přidělení režijních nákladů za elektřinu</span><span class="sxs-lookup"><span data-stu-id="8f7de-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="8f7de-133">Ve finančním účetnictví se některé náklady, jako je například elektřina, registrují jako paušální.</span><span class="sxs-lookup"><span data-stu-id="8f7de-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="8f7de-134">Podrobný přehled pro vedoucí není tedy pro nákladové účetnictví k dispozici.</span><span class="sxs-lookup"><span data-stu-id="8f7de-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="8f7de-135">V nákladovém účetnictví musí náklady procházet organizačními jednotkami, aby byl získán správný přehled pro vedoucí napříč všemi jednotkami a úrovněmi organizace.</span><span class="sxs-lookup"><span data-stu-id="8f7de-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="8f7de-136">Tento tok musí být založen buď na přesném záznamu spotřeby nebo na objektivním hodnocení.</span><span class="sxs-lookup"><span data-stu-id="8f7de-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="8f7de-137">V hlavní knize mohou být zaúčtovány náklady na elektřinu způsobem znázorněným v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="8f7de-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8f7de-138">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="8f7de-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8f7de-139">Nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="8f7de-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="8f7de-140">Hlavní účet</span><span class="sxs-lookup"><span data-stu-id="8f7de-140">Main account</span></span></th>
<th><span data-ttu-id="8f7de-141">Částka v zúčtovací měně</span><span class="sxs-lookup"><span data-stu-id="8f7de-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8f7de-142">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="8f7de-143">CC099</span><span class="sxs-lookup"><span data-stu-id="8f7de-143">CC099</span></span></td>
<td><span data-ttu-id="8f7de-144">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="8f7de-144">Default cost center</span></span></td>
<td><span data-ttu-id="8f7de-145">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-145">10001</span></span></td>
<td><span data-ttu-id="8f7de-146">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-146">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="8f7de-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="8f7de-148">Krok 1: Zpracování výpočtu chování nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="8f7de-149">Ve výchozím nastavení dostanou při importu položek nákladů z datového zdroje tyto položky v nákladovém účetnictví klasifikaci **Neklasifikované**.</span><span class="sxs-lookup"><span data-stu-id="8f7de-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="8f7de-150">Použitím pravidla zásad chování nákladů lze reklasifikovat položky nákladů jako **Pevné náklady** nebo **Variabilní náklady**.</span><span class="sxs-lookup"><span data-stu-id="8f7de-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="8f7de-151">Definice pravidel chování nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-151">Define the cost behavior rule</span></span>

<span data-ttu-id="8f7de-152">V některých případech je část nákladů s pevným poplatkem a zbývající náklady jsou založeny na spotřebě.</span><span class="sxs-lookup"><span data-stu-id="8f7de-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="8f7de-153">Účty za elektřinu často odpovídají této definici.</span><span class="sxs-lookup"><span data-stu-id="8f7de-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="8f7de-154">Po platbě konkrétního pevného poplatku platíte spotřebu za kilowatthodinu (kWh).</span><span class="sxs-lookup"><span data-stu-id="8f7de-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="8f7de-155">Pokud je například poplatek pevných nákladů 1 000,00, definuje se pravidlo chování nákladů takto:</span><span class="sxs-lookup"><span data-stu-id="8f7de-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="8f7de-156">Pevná částka 1 000,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="8f7de-157">0 &lt;= 1 000,00 = Pevná</span><span class="sxs-lookup"><span data-stu-id="8f7de-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="8f7de-158">1 000,01 &lt; N = Variabilní</span><span class="sxs-lookup"><span data-stu-id="8f7de-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="8f7de-159">Deník</span><span class="sxs-lookup"><span data-stu-id="8f7de-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8f7de-160">Deník</span><span class="sxs-lookup"><span data-stu-id="8f7de-160">Journal</span></span></th>
<th><span data-ttu-id="8f7de-161">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="8f7de-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8f7de-162">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="8f7de-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8f7de-163">Verze</span><span class="sxs-lookup"><span data-stu-id="8f7de-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8f7de-164">00001</span><span class="sxs-lookup"><span data-stu-id="8f7de-164">00001</span></span></td>
<td><span data-ttu-id="8f7de-165">Deník výpočtu chování nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="8f7de-166">Fiskální</span><span class="sxs-lookup"><span data-stu-id="8f7de-166">Fiscal</span></span></td>
<td><span data-ttu-id="8f7de-167">2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-167">2017</span></span></td>
<td><span data-ttu-id="8f7de-168">Období 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-168">Period 1</span></span></td>
<td><span data-ttu-id="8f7de-169">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="8f7de-170">Položky deníku (Položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="8f7de-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8f7de-171">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="8f7de-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8f7de-172">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8f7de-173">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-173">Cost element</span></span></th>
<th><span data-ttu-id="8f7de-174">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-174">Cost behavior</span></span></th>
<th><span data-ttu-id="8f7de-175">Částka</span><span class="sxs-lookup"><span data-stu-id="8f7de-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8f7de-176">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="8f7de-177">CC099</span><span class="sxs-lookup"><span data-stu-id="8f7de-177">CC099</span></span></td>
<td><span data-ttu-id="8f7de-178">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="8f7de-178">Default cost center</span></span></td>
<td><span data-ttu-id="8f7de-179">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-179">10001</span></span></td>
<td><span data-ttu-id="8f7de-180">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-180">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-181">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="8f7de-181">Unclassified</span></span></td>
<td><span data-ttu-id="8f7de-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="8f7de-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8f7de-183">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8f7de-184">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8f7de-185">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-185">Cost element</span></span></th>
<th><span data-ttu-id="8f7de-186">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-186">Cost behavior</span></span></th>
<th><span data-ttu-id="8f7de-187">Částka</span><span class="sxs-lookup"><span data-stu-id="8f7de-187">Amount</span></span></th>
<th><span data-ttu-id="8f7de-188">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="8f7de-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8f7de-189">CC099</span><span class="sxs-lookup"><span data-stu-id="8f7de-189">CC099</span></span></td>
<td><span data-ttu-id="8f7de-190">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="8f7de-190">Default cost center</span></span></td>
<td><span data-ttu-id="8f7de-191">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-191">10001</span></span></td>
<td><span data-ttu-id="8f7de-192">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-192">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-193">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="8f7de-193">Unclassified</span></span></td>
<td><span data-ttu-id="8f7de-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="8f7de-194">10,000.00</span></span></td>
<td><span data-ttu-id="8f7de-195">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-196">CC099</span><span class="sxs-lookup"><span data-stu-id="8f7de-196">CC099</span></span></td>
<td><span data-ttu-id="8f7de-197">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="8f7de-197">Default cost center</span></span></td>
<td><span data-ttu-id="8f7de-198">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-198">10001</span></span></td>
<td><span data-ttu-id="8f7de-199">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-199">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-200">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="8f7de-200">Unclassified</span></span></td>
<td><span data-ttu-id="8f7de-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-201">-10,000.00</span></span></td>
<td><span data-ttu-id="8f7de-202">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-203">CC099</span><span class="sxs-lookup"><span data-stu-id="8f7de-203">CC099</span></span></td>
<td><span data-ttu-id="8f7de-204">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="8f7de-204">Default cost center</span></span></td>
<td><span data-ttu-id="8f7de-205">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-205">10001</span></span></td>
<td><span data-ttu-id="8f7de-206">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-206">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-207">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-207">Fixed cost</span></span></td>
<td><span data-ttu-id="8f7de-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-208">1,000.00</span></span></td>
<td><span data-ttu-id="8f7de-209">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-210">CC099</span><span class="sxs-lookup"><span data-stu-id="8f7de-210">CC099</span></span></td>
<td><span data-ttu-id="8f7de-211">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="8f7de-211">Default cost center</span></span></td>
<td><span data-ttu-id="8f7de-212">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-212">10001</span></span></td>
<td><span data-ttu-id="8f7de-213">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-213">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-214">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-214">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="8f7de-215">9,000.00</span></span></td>
<td><span data-ttu-id="8f7de-216">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8f7de-217">Více informací naleznete v tématu [Vytvoření a přiřazení zásad chování nákladů k jednotce řízení nákladů](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="8f7de-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="8f7de-218">Krok 2: Zpracování výpočtu distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="8f7de-219">Distribuce nákladů se používá k rozdělení nákladů z jednoho objektu nákladů na jeden nebo více dalších objektů nákladů použitím příslušného základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="8f7de-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="8f7de-220">Distribuce nákladů a přidělení nákladů se liší v tom, že k distribuci nákladů dochází vždy na úrovni primárního prvku nákladů původních nákladů.</span><span class="sxs-lookup"><span data-stu-id="8f7de-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="8f7de-221">Definice pravidel distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-221">Define the cost distribution rule</span></span>

<span data-ttu-id="8f7de-222">Ve finančním účetnictví se náklady na elektřinu často registrují jako paušální.</span><span class="sxs-lookup"><span data-stu-id="8f7de-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="8f7de-223">V nákladovém účetnictví není tento přístup dostatečně podrobný.</span><span class="sxs-lookup"><span data-stu-id="8f7de-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="8f7de-224">Variabilní náklady by měly být distribuovány k jednotlivým objektům nákladů na solidním základě.</span><span class="sxs-lookup"><span data-stu-id="8f7de-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="8f7de-225">Nejlogičtější základ přidělení je spotřeba elektřiny (kWh).</span><span class="sxs-lookup"><span data-stu-id="8f7de-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="8f7de-226">Vytvoří se člen statistické dimenzi s názvem Elektřina a zaznamená se elektrické spotřeba.</span><span class="sxs-lookup"><span data-stu-id="8f7de-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="8f7de-227">Ve výchozím nastavení se všechny členy statistické dimenze stanou dostupnými zpřístupněny jako základy přidělení.</span><span class="sxs-lookup"><span data-stu-id="8f7de-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8f7de-228">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-228">Cost object</span></span></th>
<th><span data-ttu-id="8f7de-229">kWh</span><span class="sxs-lookup"><span data-stu-id="8f7de-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8f7de-230">CC001</span><span class="sxs-lookup"><span data-stu-id="8f7de-230">CC001</span></span></td>
<td><span data-ttu-id="8f7de-231">HR</span><span class="sxs-lookup"><span data-stu-id="8f7de-231">HR</span></span></td>
<td><span data-ttu-id="8f7de-232">1 000</span><span class="sxs-lookup"><span data-stu-id="8f7de-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-233">CC002</span><span class="sxs-lookup"><span data-stu-id="8f7de-233">CC002</span></span></td>
<td><span data-ttu-id="8f7de-234">Finance</span><span class="sxs-lookup"><span data-stu-id="8f7de-234">Finance</span></span></td>
<td><span data-ttu-id="8f7de-235">6,000</span><span class="sxs-lookup"><span data-stu-id="8f7de-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-236">CC003</span><span class="sxs-lookup"><span data-stu-id="8f7de-236">CC003</span></span></td>
<td><span data-ttu-id="8f7de-237">Sestavení</span><span class="sxs-lookup"><span data-stu-id="8f7de-237">Assembly</span></span></td>
<td><span data-ttu-id="8f7de-238">0</span><span class="sxs-lookup"><span data-stu-id="8f7de-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8f7de-239">Následující tabulka zobrazuje výsledek při použití elektrické spotřeby jako základu přidělení pro variabilní náklady.</span><span class="sxs-lookup"><span data-stu-id="8f7de-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8f7de-240">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-240">Cost object</span></span></th>
<th><span data-ttu-id="8f7de-241">Hodnota</span><span class="sxs-lookup"><span data-stu-id="8f7de-241">Magnitude</span></span></th>
<th><span data-ttu-id="8f7de-242">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="8f7de-242">Allocation factor</span></span></th>
<th><span data-ttu-id="8f7de-243">Částka</span><span class="sxs-lookup"><span data-stu-id="8f7de-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8f7de-244">CC001</span><span class="sxs-lookup"><span data-stu-id="8f7de-244">CC001</span></span></td>
<td><span data-ttu-id="8f7de-245">HR</span><span class="sxs-lookup"><span data-stu-id="8f7de-245">HR</span></span></td>
<td><span data-ttu-id="8f7de-246">1 000</span><span class="sxs-lookup"><span data-stu-id="8f7de-246">1,000</span></span></td>
<td><span data-ttu-id="8f7de-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="8f7de-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="8f7de-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-249">CC002</span><span class="sxs-lookup"><span data-stu-id="8f7de-249">CC002</span></span></td>
<td><span data-ttu-id="8f7de-250">Finance</span><span class="sxs-lookup"><span data-stu-id="8f7de-250">Finance</span></span></td>
<td><span data-ttu-id="8f7de-251">6,000</span><span class="sxs-lookup"><span data-stu-id="8f7de-251">6,000</span></span></td>
<td><span data-ttu-id="8f7de-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="8f7de-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="8f7de-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-254">CC003</span><span class="sxs-lookup"><span data-stu-id="8f7de-254">CC003</span></span></td>
<td><span data-ttu-id="8f7de-255">Sestavení</span><span class="sxs-lookup"><span data-stu-id="8f7de-255">Assembly</span></span></td>
<td><span data-ttu-id="8f7de-256">0</span><span class="sxs-lookup"><span data-stu-id="8f7de-256">0</span></span></td>
<td><span data-ttu-id="8f7de-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="8f7de-258">0,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8f7de-259">Pevné náklady musí být distribuovány rovnoměrně k jednotlivých objektům nákladů, které spotřebovávaly elektřinu.</span><span class="sxs-lookup"><span data-stu-id="8f7de-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="8f7de-260">Tohoto výsledku můžete dosáhnout pomocí členu statistické dimenze Elektřina v základu přidělení vzorce: (Elektřina &gt; 0,00) Následující tabulka zobrazuje výsledek při použití elektrické spotřeby jako základu přidělení pro variabilní náklady.</span><span class="sxs-lookup"><span data-stu-id="8f7de-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8f7de-261">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-261">Cost object</span></span></th>
<th><span data-ttu-id="8f7de-262">Vzorec</span><span class="sxs-lookup"><span data-stu-id="8f7de-262">Formula</span></span></th>
<th><span data-ttu-id="8f7de-263">Hodnota</span><span class="sxs-lookup"><span data-stu-id="8f7de-263">Magnitude</span></span></th>
<th><span data-ttu-id="8f7de-264">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="8f7de-264">Allocation factor</span></span></th>
<th><span data-ttu-id="8f7de-265">Částka</span><span class="sxs-lookup"><span data-stu-id="8f7de-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8f7de-266">CC001</span><span class="sxs-lookup"><span data-stu-id="8f7de-266">CC001</span></span></td>
<td><span data-ttu-id="8f7de-267">HR</span><span class="sxs-lookup"><span data-stu-id="8f7de-267">HR</span></span></td>
<td><span data-ttu-id="8f7de-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="8f7de-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="8f7de-269">1</span><span class="sxs-lookup"><span data-stu-id="8f7de-269">1</span></span></td>
<td><span data-ttu-id="8f7de-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="8f7de-271">500.00</span><span class="sxs-lookup"><span data-stu-id="8f7de-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-272">CC002</span><span class="sxs-lookup"><span data-stu-id="8f7de-272">CC002</span></span></td>
<td><span data-ttu-id="8f7de-273">Finance</span><span class="sxs-lookup"><span data-stu-id="8f7de-273">Finance</span></span></td>
<td><span data-ttu-id="8f7de-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="8f7de-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="8f7de-275">1</span><span class="sxs-lookup"><span data-stu-id="8f7de-275">1</span></span></td>
<td><span data-ttu-id="8f7de-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="8f7de-277">500.00</span><span class="sxs-lookup"><span data-stu-id="8f7de-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-278">CC003</span><span class="sxs-lookup"><span data-stu-id="8f7de-278">CC003</span></span></td>
<td><span data-ttu-id="8f7de-279">Sestavení</span><span class="sxs-lookup"><span data-stu-id="8f7de-279">Assembly</span></span></td>
<td><span data-ttu-id="8f7de-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="8f7de-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="8f7de-281">0</span><span class="sxs-lookup"><span data-stu-id="8f7de-281">0</span></span></td>
<td><span data-ttu-id="8f7de-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="8f7de-283">0,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="8f7de-284">Deník</span><span class="sxs-lookup"><span data-stu-id="8f7de-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8f7de-285">Deník</span><span class="sxs-lookup"><span data-stu-id="8f7de-285">Journal</span></span></th>
<th><span data-ttu-id="8f7de-286">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="8f7de-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8f7de-287">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="8f7de-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8f7de-288">Verze</span><span class="sxs-lookup"><span data-stu-id="8f7de-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8f7de-289">00002</span><span class="sxs-lookup"><span data-stu-id="8f7de-289">00002</span></span></td>
<td><span data-ttu-id="8f7de-290">Deník výpočtu distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="8f7de-291">Fiskální</span><span class="sxs-lookup"><span data-stu-id="8f7de-291">Fiscal</span></span></td>
<td><span data-ttu-id="8f7de-292">2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-292">2017</span></span></td>
<td><span data-ttu-id="8f7de-293">Období 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-293">Period 1</span></span></td>
<td><span data-ttu-id="8f7de-294">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="8f7de-295">Položky deníku (Položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="8f7de-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8f7de-296">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="8f7de-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8f7de-297">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8f7de-298">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-298">Cost element</span></span></th>
<th><span data-ttu-id="8f7de-299">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-299">Cost behavior</span></span></th>
<th><span data-ttu-id="8f7de-300">Částka</span><span class="sxs-lookup"><span data-stu-id="8f7de-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8f7de-301">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="8f7de-302">CC099</span><span class="sxs-lookup"><span data-stu-id="8f7de-302">CC099</span></span></td>
<td><span data-ttu-id="8f7de-303">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="8f7de-303">Default cost center</span></span></td>
<td><span data-ttu-id="8f7de-304">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-304">10001</span></span></td>
<td><span data-ttu-id="8f7de-305">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-305">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-306">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-306">Fixed cost</span></span></td>
<td><span data-ttu-id="8f7de-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-308">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="8f7de-309">CC099</span><span class="sxs-lookup"><span data-stu-id="8f7de-309">CC099</span></span></td>
<td><span data-ttu-id="8f7de-310">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="8f7de-310">Default cost center</span></span></td>
<td><span data-ttu-id="8f7de-311">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-311">10001</span></span></td>
<td><span data-ttu-id="8f7de-312">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-312">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-313">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-313">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="8f7de-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8f7de-315">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8f7de-316">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8f7de-317">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-317">Cost element</span></span></th>
<th><span data-ttu-id="8f7de-318">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-318">Cost behavior</span></span></th>
<th><span data-ttu-id="8f7de-319">Částka</span><span class="sxs-lookup"><span data-stu-id="8f7de-319">Amount</span></span></th>
<th><span data-ttu-id="8f7de-320">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="8f7de-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8f7de-321">CC099</span><span class="sxs-lookup"><span data-stu-id="8f7de-321">CC099</span></span></td>
<td><span data-ttu-id="8f7de-322">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="8f7de-322">Default cost center</span></span></td>
<td><span data-ttu-id="8f7de-323">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-323">10001</span></span></td>
<td><span data-ttu-id="8f7de-324">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-324">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-325">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-325">Fixed cost</span></span></td>
<td><span data-ttu-id="8f7de-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-326">-1,000.00</span></span></td>
<td><span data-ttu-id="8f7de-327">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-328">CC001</span><span class="sxs-lookup"><span data-stu-id="8f7de-328">CC001</span></span></td>
<td><span data-ttu-id="8f7de-329">HR</span><span class="sxs-lookup"><span data-stu-id="8f7de-329">HR</span></span></td>
<td><span data-ttu-id="8f7de-330">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-330">10001</span></span></td>
<td><span data-ttu-id="8f7de-331">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-331">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-332">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-332">Fixed cost</span></span></td>
<td><span data-ttu-id="8f7de-333">500.00</span><span class="sxs-lookup"><span data-stu-id="8f7de-333">500.00</span></span></td>
<td><span data-ttu-id="8f7de-334">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-335">CC002</span><span class="sxs-lookup"><span data-stu-id="8f7de-335">CC002</span></span></td>
<td><span data-ttu-id="8f7de-336">Finance</span><span class="sxs-lookup"><span data-stu-id="8f7de-336">Finance</span></span></td>
<td><span data-ttu-id="8f7de-337">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-337">10001</span></span></td>
<td><span data-ttu-id="8f7de-338">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-338">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-339">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-339">Fixed cost</span></span></td>
<td><span data-ttu-id="8f7de-340">500.00</span><span class="sxs-lookup"><span data-stu-id="8f7de-340">500.00</span></span></td>
<td><span data-ttu-id="8f7de-341">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-342">CC099</span><span class="sxs-lookup"><span data-stu-id="8f7de-342">CC099</span></span></td>
<td><span data-ttu-id="8f7de-343">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="8f7de-343">Default cost center</span></span></td>
<td><span data-ttu-id="8f7de-344">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-344">10001</span></span></td>
<td><span data-ttu-id="8f7de-345">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-345">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-346">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-346">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-347">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-347">-9,000.00</span></span></td>
<td><span data-ttu-id="8f7de-348">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-349">CC001</span><span class="sxs-lookup"><span data-stu-id="8f7de-349">CC001</span></span></td>
<td><span data-ttu-id="8f7de-350">HR</span><span class="sxs-lookup"><span data-stu-id="8f7de-350">HR</span></span></td>
<td><span data-ttu-id="8f7de-351">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-351">10001</span></span></td>
<td><span data-ttu-id="8f7de-352">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-352">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-353">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-353">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="8f7de-354">1,285.71</span></span></td>
<td><span data-ttu-id="8f7de-355">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-356">CC002</span><span class="sxs-lookup"><span data-stu-id="8f7de-356">CC002</span></span></td>
<td><span data-ttu-id="8f7de-357">Finance</span><span class="sxs-lookup"><span data-stu-id="8f7de-357">Finance</span></span></td>
<td><span data-ttu-id="8f7de-358">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-358">10001</span></span></td>
<td><span data-ttu-id="8f7de-359">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-359">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-360">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-360">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="8f7de-361">7,714.29</span></span></td>
<td><span data-ttu-id="8f7de-362">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8f7de-363">Více informací naleznete v tématu [Vytvoření a přiřazení zásad distribuce nákladů k jednotce řízení nákladů](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="8f7de-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="8f7de-364">Krok 3: Zpracování výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="8f7de-365">Režijní náklady se používají k účtování jednoho nebo více konkrétních objektů nákladů.</span><span class="sxs-lookup"><span data-stu-id="8f7de-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="8f7de-366">Účtování je založeno na předem určené nákladové sazbě a množství z přiřazeného základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="8f7de-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="8f7de-367">Definice sazby režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-367">Define the overhead rate</span></span>

<span data-ttu-id="8f7de-368">Objekt nákladů CC001 HR přispívá k sadě interních projektů.</span><span class="sxs-lookup"><span data-stu-id="8f7de-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="8f7de-369">Vytvoří se člen statistické dimenzi s názvem projekty lidských zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="8f7de-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8f7de-370">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-370">Cost object</span></span></th>
<th><span data-ttu-id="8f7de-371">Pracovní doba</span><span class="sxs-lookup"><span data-stu-id="8f7de-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8f7de-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-372">Proj 1</span></span></td>
<td><span data-ttu-id="8f7de-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-373">Project 1</span></span></td>
<td><span data-ttu-id="8f7de-374">3</span><span class="sxs-lookup"><span data-stu-id="8f7de-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-375">Proj 2</span></span></td>
<td><span data-ttu-id="8f7de-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-376">Project 2</span></span></td>
<td><span data-ttu-id="8f7de-377">1</span><span class="sxs-lookup"><span data-stu-id="8f7de-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8f7de-378">Byla definována předem určená nákladová sazba pro příspěvky k nákladovým projektům.</span><span class="sxs-lookup"><span data-stu-id="8f7de-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8f7de-379">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-379">Cost object</span></span></th>
<th><span data-ttu-id="8f7de-380">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-380">Cost element</span></span></th>
<th><span data-ttu-id="8f7de-381">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-381">Cost behavior</span></span></th>
<th><span data-ttu-id="8f7de-382">Jednotky</span><span class="sxs-lookup"><span data-stu-id="8f7de-382">Units</span></span></th>
<th><span data-ttu-id="8f7de-383">Kurz</span><span class="sxs-lookup"><span data-stu-id="8f7de-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8f7de-384">CC001</span><span class="sxs-lookup"><span data-stu-id="8f7de-384">CC001</span></span></td>
<td><span data-ttu-id="8f7de-385">HR</span><span class="sxs-lookup"><span data-stu-id="8f7de-385">HR</span></span></td>
<td><span data-ttu-id="8f7de-386">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-386">10001</span></span></td>
<td><span data-ttu-id="8f7de-387">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-387">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-388">1</span><span class="sxs-lookup"><span data-stu-id="8f7de-388">1</span></span></td>
<td><span data-ttu-id="8f7de-389">10</span><span class="sxs-lookup"><span data-stu-id="8f7de-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8f7de-390">Následující tabulka zobrazuje výsledek při použití projektů lidských zdrojů jako základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="8f7de-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8f7de-391">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-391">Cost object</span></span></th>
<th><span data-ttu-id="8f7de-392">Hodnota</span><span class="sxs-lookup"><span data-stu-id="8f7de-392">Magnitude</span></span></th>
<th><span data-ttu-id="8f7de-393">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-393">Cost element</span></span></th>
<th><span data-ttu-id="8f7de-394">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="8f7de-394">Allocation factor</span></span></th>
<th><span data-ttu-id="8f7de-395">Částka</span><span class="sxs-lookup"><span data-stu-id="8f7de-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8f7de-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-396">Proj 1</span></span></td>
<td><span data-ttu-id="8f7de-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-397">Project 1</span></span></td>
<td><span data-ttu-id="8f7de-398">3</span><span class="sxs-lookup"><span data-stu-id="8f7de-398">3</span></span></td>
<td><span data-ttu-id="8f7de-399">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-399">10001</span></span></td>
<td><span data-ttu-id="8f7de-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="8f7de-401">30.00</span><span class="sxs-lookup"><span data-stu-id="8f7de-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-402">Proj 2</span></span></td>
<td><span data-ttu-id="8f7de-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-403">Project 2</span></span></td>
<td><span data-ttu-id="8f7de-404">1</span><span class="sxs-lookup"><span data-stu-id="8f7de-404">1</span></span></td>
<td><span data-ttu-id="8f7de-405">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-405">10001</span></span></td>
<td><span data-ttu-id="8f7de-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="8f7de-407">10,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="8f7de-408">Deník</span><span class="sxs-lookup"><span data-stu-id="8f7de-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8f7de-409">Deník</span><span class="sxs-lookup"><span data-stu-id="8f7de-409">Journal</span></span></th>
<th><span data-ttu-id="8f7de-410">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="8f7de-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8f7de-411">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="8f7de-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8f7de-412">Verze</span><span class="sxs-lookup"><span data-stu-id="8f7de-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8f7de-413">00003</span><span class="sxs-lookup"><span data-stu-id="8f7de-413">00003</span></span></td>
<td><span data-ttu-id="8f7de-414">Deník výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="8f7de-415">Fiskální</span><span class="sxs-lookup"><span data-stu-id="8f7de-415">Fiscal</span></span></td>
<td><span data-ttu-id="8f7de-416">2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-416">2017</span></span></td>
<td><span data-ttu-id="8f7de-417">Období 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-417">Period 1</span></span></td>
<td><span data-ttu-id="8f7de-418">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="8f7de-419">Položky deníku (položky deníku pro výpočet sazby režijních nákladů)</span><span class="sxs-lookup"><span data-stu-id="8f7de-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8f7de-420">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="8f7de-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8f7de-421">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-421">Cost object</span></span></th>
<th><span data-ttu-id="8f7de-422">Hodnota</span><span class="sxs-lookup"><span data-stu-id="8f7de-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8f7de-423">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="8f7de-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-424">Proj 1</span></span></td>
<td><span data-ttu-id="8f7de-425">Interní projekt 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="8f7de-426">3,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-427">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="8f7de-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-428">Proj 2</span></span></td>
<td><span data-ttu-id="8f7de-429">Interní projekt 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="8f7de-430">1.00</span><span class="sxs-lookup"><span data-stu-id="8f7de-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8f7de-431">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8f7de-432">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8f7de-433">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-433">Cost element</span></span></th>
<th><span data-ttu-id="8f7de-434">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-434">Cost behavior</span></span></th>
<th><span data-ttu-id="8f7de-435">Částka</span><span class="sxs-lookup"><span data-stu-id="8f7de-435">Amount</span></span></th>
<th><span data-ttu-id="8f7de-436">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="8f7de-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8f7de-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="8f7de-437">CC0001</span></span></td>
<td><span data-ttu-id="8f7de-438">HR</span><span class="sxs-lookup"><span data-stu-id="8f7de-438">HR</span></span></td>
<td><span data-ttu-id="8f7de-439">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-439">10001</span></span></td>
<td><span data-ttu-id="8f7de-440">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-440">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-441">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-441">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-442">-30.00</span></span></td>
<td><span data-ttu-id="8f7de-443">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-444">Proj 1</span></span></td>
<td><span data-ttu-id="8f7de-445">Interní projekt 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="8f7de-446">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-446">10001</span></span></td>
<td><span data-ttu-id="8f7de-447">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-447">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-448">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-448">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-449">30.00</span><span class="sxs-lookup"><span data-stu-id="8f7de-449">30.00</span></span></td>
<td><span data-ttu-id="8f7de-450">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-451">CC001</span><span class="sxs-lookup"><span data-stu-id="8f7de-451">CC001</span></span></td>
<td><span data-ttu-id="8f7de-452">HR</span><span class="sxs-lookup"><span data-stu-id="8f7de-452">HR</span></span></td>
<td><span data-ttu-id="8f7de-453">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-453">10001</span></span></td>
<td><span data-ttu-id="8f7de-454">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-454">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-455">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-455">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-456">-10.00</span></span></td>
<td><span data-ttu-id="8f7de-457">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-458">Proj 2</span></span></td>
<td><span data-ttu-id="8f7de-459">Interní projekt 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="8f7de-460">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-460">10001</span></span></td>
<td><span data-ttu-id="8f7de-461">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-461">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-462">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-462">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-463">10.00</span><span class="sxs-lookup"><span data-stu-id="8f7de-463">10.00</span></span></td>
<td><span data-ttu-id="8f7de-464">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8f7de-465">Další informace naleznete v tématu [Provedení výpočtu režijních nákladů](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="8f7de-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="8f7de-466">Krok 4: Zpracování výpočtu přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="8f7de-467">Přidělení se používá k přidělení zůstatku objektu nákladů do jiných objektů nákladů použitím základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="8f7de-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="8f7de-468">Aplikace Finance podporuje reciproční metodu přidělování.</span><span class="sxs-lookup"><span data-stu-id="8f7de-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="8f7de-469">V metodě vzájemného přidělení jsou plně rozpoznány vzájemné služby, které si vyměňují pomocné objekty nákladů.</span><span class="sxs-lookup"><span data-stu-id="8f7de-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="8f7de-470">Systém automaticky určí provádění přidělení ve správném pořadí.</span><span class="sxs-lookup"><span data-stu-id="8f7de-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="8f7de-471">Zůstatek objektu nákladů je přidělen jedním základem přidělení.</span><span class="sxs-lookup"><span data-stu-id="8f7de-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="8f7de-472">Je podporováno přidělování napříč dimenzemi objektů nákladů a jejich příslušných členů.</span><span class="sxs-lookup"><span data-stu-id="8f7de-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="8f7de-473">Pořadí přidělení je řízeno jednotkou řízení nákladů.</span><span class="sxs-lookup"><span data-stu-id="8f7de-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="8f7de-474">[![Reciproční metoda](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="8f7de-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="8f7de-475">Definice přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-475">Define the cost allocation</span></span>

<span data-ttu-id="8f7de-476">Toto je jednoduchý příklad, který vysvětluje, jakým způsobem lze sledovat tok nákladů.</span><span class="sxs-lookup"><span data-stu-id="8f7de-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="8f7de-477">Objekt nákladů objektu CC001 HR přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="8f7de-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="8f7de-478">Vytvoří se člen statistické dimenzi s názvem služby lidských zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="8f7de-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8f7de-479">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-479">Cost object</span></span></th>
<th><span data-ttu-id="8f7de-480">Služby HR</span><span class="sxs-lookup"><span data-stu-id="8f7de-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8f7de-481">CC002</span><span class="sxs-lookup"><span data-stu-id="8f7de-481">CC002</span></span></td>
<td><span data-ttu-id="8f7de-482">Finance</span><span class="sxs-lookup"><span data-stu-id="8f7de-482">Finance</span></span></td>
<td><span data-ttu-id="8f7de-483">35</span><span class="sxs-lookup"><span data-stu-id="8f7de-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-484">CC003</span><span class="sxs-lookup"><span data-stu-id="8f7de-484">CC003</span></span></td>
<td><span data-ttu-id="8f7de-485">Sestavení</span><span class="sxs-lookup"><span data-stu-id="8f7de-485">Assembly</span></span></td>
<td><span data-ttu-id="8f7de-486">55</span><span class="sxs-lookup"><span data-stu-id="8f7de-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-487">CC004</span><span class="sxs-lookup"><span data-stu-id="8f7de-487">CC004</span></span></td>
<td><span data-ttu-id="8f7de-488">Balení</span><span class="sxs-lookup"><span data-stu-id="8f7de-488">Packaging</span></span></td>
<td><span data-ttu-id="8f7de-489">10</span><span class="sxs-lookup"><span data-stu-id="8f7de-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8f7de-490">Objekt nákladů objektu CC002 Finance přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="8f7de-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="8f7de-491">Vytvoří se člen statistické dimenzi s názvem Finanční služby k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="8f7de-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8f7de-492">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-492">Cost object</span></span></th>
<th><span data-ttu-id="8f7de-493">Finanční služby</span><span class="sxs-lookup"><span data-stu-id="8f7de-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8f7de-494">CC003</span><span class="sxs-lookup"><span data-stu-id="8f7de-494">CC003</span></span></td>
<td><span data-ttu-id="8f7de-495">Sestavení</span><span class="sxs-lookup"><span data-stu-id="8f7de-495">Assembly</span></span></td>
<td><span data-ttu-id="8f7de-496">65</span><span class="sxs-lookup"><span data-stu-id="8f7de-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-497">CC004</span><span class="sxs-lookup"><span data-stu-id="8f7de-497">CC004</span></span></td>
<td><span data-ttu-id="8f7de-498">Balení</span><span class="sxs-lookup"><span data-stu-id="8f7de-498">Packaging</span></span></td>
<td><span data-ttu-id="8f7de-499">35</span><span class="sxs-lookup"><span data-stu-id="8f7de-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8f7de-500">Objekt nákladů objektu CC003 Sestavení přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="8f7de-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="8f7de-501">Vytvoří se člen statistické dimenzi s názvem Služby sestavení zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="8f7de-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8f7de-502">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-502">Cost object</span></span></th>
<th><span data-ttu-id="8f7de-503">Služby sestavení (v hodinách)</span><span class="sxs-lookup"><span data-stu-id="8f7de-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8f7de-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-504">Prod 1</span></span></td>
<td><span data-ttu-id="8f7de-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-505">Product 1</span></span></td>
<td><span data-ttu-id="8f7de-506">60</span><span class="sxs-lookup"><span data-stu-id="8f7de-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-507">Prod 2</span></span></td>
<td><span data-ttu-id="8f7de-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-508">Product 2</span></span></td>
<td><span data-ttu-id="8f7de-509">20</span><span class="sxs-lookup"><span data-stu-id="8f7de-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8f7de-510">Objekt nákladů objektu CC004 Balení přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="8f7de-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="8f7de-511">Vytvoří se člen statistické dimenzi s názvem Služby balení k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="8f7de-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8f7de-512">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-512">Cost object</span></span></th>
<th><span data-ttu-id="8f7de-513">Služby balení (v hodinách)</span><span class="sxs-lookup"><span data-stu-id="8f7de-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8f7de-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-514">Prod 1</span></span></td>
<td><span data-ttu-id="8f7de-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-515">Product 1</span></span></td>
<td><span data-ttu-id="8f7de-516">80</span><span class="sxs-lookup"><span data-stu-id="8f7de-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-517">Prod 2</span></span></td>
<td><span data-ttu-id="8f7de-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-518">Product 2</span></span></td>
<td><span data-ttu-id="8f7de-519">15</span><span class="sxs-lookup"><span data-stu-id="8f7de-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="8f7de-520">Statistická měření, jako je například výrobní doba spotřebovaná produktem, lze odvodit z datového zdroje.</span><span class="sxs-lookup"><span data-stu-id="8f7de-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="8f7de-521">Více informací naleznete v části [Šablona poskytovatele statistického měření](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="8f7de-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="8f7de-522">V následující tabulce je uveden výsledek při použití služeb HR jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="8f7de-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8f7de-523">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-523">Cost object</span></span></th>
<th><span data-ttu-id="8f7de-524">Hodnota</span><span class="sxs-lookup"><span data-stu-id="8f7de-524">Magnitude</span></span></th>
<th><span data-ttu-id="8f7de-525">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="8f7de-525">Allocation factor</span></span></th>
<th><span data-ttu-id="8f7de-526">Částka</span><span class="sxs-lookup"><span data-stu-id="8f7de-526">Amount</span></span></th>
<th><span data-ttu-id="8f7de-527">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8f7de-528">CC002</span><span class="sxs-lookup"><span data-stu-id="8f7de-528">CC002</span></span></td>
<td><span data-ttu-id="8f7de-529">Finance</span><span class="sxs-lookup"><span data-stu-id="8f7de-529">Finance</span></span></td>
<td><span data-ttu-id="8f7de-530">35</span><span class="sxs-lookup"><span data-stu-id="8f7de-530">35</span></span></td>
<td><span data-ttu-id="8f7de-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="8f7de-532">175.00</span><span class="sxs-lookup"><span data-stu-id="8f7de-532">175.00</span></span></td>
<td><span data-ttu-id="8f7de-533">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-534">CC003</span><span class="sxs-lookup"><span data-stu-id="8f7de-534">CC003</span></span></td>
<td><span data-ttu-id="8f7de-535">Sestavení</span><span class="sxs-lookup"><span data-stu-id="8f7de-535">Assembly</span></span></td>
<td><span data-ttu-id="8f7de-536">55</span><span class="sxs-lookup"><span data-stu-id="8f7de-536">55</span></span></td>
<td><span data-ttu-id="8f7de-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="8f7de-538">275.00</span><span class="sxs-lookup"><span data-stu-id="8f7de-538">275.00</span></span></td>
<td><span data-ttu-id="8f7de-539">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-540">CC004</span><span class="sxs-lookup"><span data-stu-id="8f7de-540">CC004</span></span></td>
<td><span data-ttu-id="8f7de-541">Balení</span><span class="sxs-lookup"><span data-stu-id="8f7de-541">Packaging</span></span></td>
<td><span data-ttu-id="8f7de-542">10</span><span class="sxs-lookup"><span data-stu-id="8f7de-542">10</span></span></td>
<td><span data-ttu-id="8f7de-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="8f7de-544">50,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-544">50.00</span></span></td>
<td><span data-ttu-id="8f7de-545">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-546">CC002</span><span class="sxs-lookup"><span data-stu-id="8f7de-546">CC002</span></span></td>
<td><span data-ttu-id="8f7de-547">Finance</span><span class="sxs-lookup"><span data-stu-id="8f7de-547">Finance</span></span></td>
<td><span data-ttu-id="8f7de-548">35</span><span class="sxs-lookup"><span data-stu-id="8f7de-548">35</span></span></td>
<td><span data-ttu-id="8f7de-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="8f7de-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="8f7de-550">436.00</span><span class="sxs-lookup"><span data-stu-id="8f7de-550">436.00</span></span></td>
<td><span data-ttu-id="8f7de-551">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-552">CC003</span><span class="sxs-lookup"><span data-stu-id="8f7de-552">CC003</span></span></td>
<td><span data-ttu-id="8f7de-553">Sestavení</span><span class="sxs-lookup"><span data-stu-id="8f7de-553">Assembly</span></span></td>
<td><span data-ttu-id="8f7de-554">55</span><span class="sxs-lookup"><span data-stu-id="8f7de-554">55</span></span></td>
<td><span data-ttu-id="8f7de-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="8f7de-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="8f7de-556">685.14</span><span class="sxs-lookup"><span data-stu-id="8f7de-556">685.14</span></span></td>
<td><span data-ttu-id="8f7de-557">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-558">CC004</span><span class="sxs-lookup"><span data-stu-id="8f7de-558">CC004</span></span></td>
<td><span data-ttu-id="8f7de-559">Balení</span><span class="sxs-lookup"><span data-stu-id="8f7de-559">Packaging</span></span></td>
<td><span data-ttu-id="8f7de-560">10</span><span class="sxs-lookup"><span data-stu-id="8f7de-560">10</span></span></td>
<td><span data-ttu-id="8f7de-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="8f7de-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="8f7de-562">124.57</span><span class="sxs-lookup"><span data-stu-id="8f7de-562">124.57</span></span></td>
<td><span data-ttu-id="8f7de-563">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8f7de-564">V následující tabulce je uveden výsledek při použití Finančních služeb Finance jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="8f7de-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8f7de-565">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-565">Cost object</span></span></th>
<th><span data-ttu-id="8f7de-566">Hodnota</span><span class="sxs-lookup"><span data-stu-id="8f7de-566">Magnitude</span></span></th>
<th><span data-ttu-id="8f7de-567">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="8f7de-567">Allocation factor</span></span></th>
<th><span data-ttu-id="8f7de-568">Částka</span><span class="sxs-lookup"><span data-stu-id="8f7de-568">Amount</span></span></th>
<th><span data-ttu-id="8f7de-569">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8f7de-570">CC003</span><span class="sxs-lookup"><span data-stu-id="8f7de-570">CC003</span></span></td>
<td><span data-ttu-id="8f7de-571">Sestavení</span><span class="sxs-lookup"><span data-stu-id="8f7de-571">Assembly</span></span></td>
<td><span data-ttu-id="8f7de-572">65</span><span class="sxs-lookup"><span data-stu-id="8f7de-572">65</span></span></td>
<td><span data-ttu-id="8f7de-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="8f7de-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="8f7de-574">438.75</span><span class="sxs-lookup"><span data-stu-id="8f7de-574">438.75</span></span></td>
<td><span data-ttu-id="8f7de-575">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-576">CC004</span><span class="sxs-lookup"><span data-stu-id="8f7de-576">CC004</span></span></td>
<td><span data-ttu-id="8f7de-577">Balení</span><span class="sxs-lookup"><span data-stu-id="8f7de-577">Packaging</span></span></td>
<td><span data-ttu-id="8f7de-578">35</span><span class="sxs-lookup"><span data-stu-id="8f7de-578">35</span></span></td>
<td><span data-ttu-id="8f7de-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="8f7de-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="8f7de-580">236.25</span><span class="sxs-lookup"><span data-stu-id="8f7de-580">236.25</span></span></td>
<td><span data-ttu-id="8f7de-581">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-582">CC003</span><span class="sxs-lookup"><span data-stu-id="8f7de-582">CC003</span></span></td>
<td><span data-ttu-id="8f7de-583">Sestavení</span><span class="sxs-lookup"><span data-stu-id="8f7de-583">Assembly</span></span></td>
<td><span data-ttu-id="8f7de-584">65</span><span class="sxs-lookup"><span data-stu-id="8f7de-584">65</span></span></td>
<td><span data-ttu-id="8f7de-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="8f7de-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="8f7de-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="8f7de-586">5,297.69</span></span></td>
<td><span data-ttu-id="8f7de-587">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-588">CC004</span><span class="sxs-lookup"><span data-stu-id="8f7de-588">CC004</span></span></td>
<td><span data-ttu-id="8f7de-589">Balení</span><span class="sxs-lookup"><span data-stu-id="8f7de-589">Packaging</span></span></td>
<td><span data-ttu-id="8f7de-590">35</span><span class="sxs-lookup"><span data-stu-id="8f7de-590">35</span></span></td>
<td><span data-ttu-id="8f7de-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="8f7de-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="8f7de-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="8f7de-592">2,852.60</span></span></td>
<td><span data-ttu-id="8f7de-593">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8f7de-594">V následující tabulce je uveden výsledek při použití Služeb sestavení jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="8f7de-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8f7de-595">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-595">Cost object</span></span></th>
<th><span data-ttu-id="8f7de-596">Hodnota</span><span class="sxs-lookup"><span data-stu-id="8f7de-596">Magnitude</span></span></th>
<th><span data-ttu-id="8f7de-597">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="8f7de-597">Allocation factor</span></span></th>
<th><span data-ttu-id="8f7de-598">Částka</span><span class="sxs-lookup"><span data-stu-id="8f7de-598">Amount</span></span></th>
<th><span data-ttu-id="8f7de-599">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8f7de-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-600">Prod 1</span></span></td>
<td><span data-ttu-id="8f7de-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-601">Product 1</span></span></td>
<td><span data-ttu-id="8f7de-602">60</span><span class="sxs-lookup"><span data-stu-id="8f7de-602">60</span></span></td>
<td><span data-ttu-id="8f7de-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="8f7de-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="8f7de-604">535.31</span><span class="sxs-lookup"><span data-stu-id="8f7de-604">535.31</span></span></td>
<td><span data-ttu-id="8f7de-605">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-606">Prod 2</span></span></td>
<td><span data-ttu-id="8f7de-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-607">Product 2</span></span></td>
<td><span data-ttu-id="8f7de-608">20</span><span class="sxs-lookup"><span data-stu-id="8f7de-608">20</span></span></td>
<td><span data-ttu-id="8f7de-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="8f7de-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="8f7de-610">178.44</span><span class="sxs-lookup"><span data-stu-id="8f7de-610">178.44</span></span></td>
<td><span data-ttu-id="8f7de-611">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-612">Prod 1</span></span></td>
<td><span data-ttu-id="8f7de-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-613">Product 1</span></span></td>
<td><span data-ttu-id="8f7de-614">60</span><span class="sxs-lookup"><span data-stu-id="8f7de-614">60</span></span></td>
<td><span data-ttu-id="8f7de-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="8f7de-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="8f7de-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="8f7de-616">4,487.12</span></span></td>
<td><span data-ttu-id="8f7de-617">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-618">Prod 2</span></span></td>
<td><span data-ttu-id="8f7de-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-619">Product 2</span></span></td>
<td><span data-ttu-id="8f7de-620">20</span><span class="sxs-lookup"><span data-stu-id="8f7de-620">20</span></span></td>
<td><span data-ttu-id="8f7de-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="8f7de-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="8f7de-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="8f7de-622">1,495.71</span></span></td>
<td><span data-ttu-id="8f7de-623">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8f7de-624">V následující tabulce je uveden výsledek při použití Služeb balení jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="8f7de-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8f7de-625">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-625">Cost object</span></span></th>
<th><span data-ttu-id="8f7de-626">Hodnota</span><span class="sxs-lookup"><span data-stu-id="8f7de-626">Magnitude</span></span></th>
<th><span data-ttu-id="8f7de-627">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="8f7de-627">Allocation factor</span></span></th>
<th><span data-ttu-id="8f7de-628">Částka</span><span class="sxs-lookup"><span data-stu-id="8f7de-628">Amount</span></span></th>
<th><span data-ttu-id="8f7de-629">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8f7de-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-630">Prod 1</span></span></td>
<td><span data-ttu-id="8f7de-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-631">Product 1</span></span></td>
<td><span data-ttu-id="8f7de-632">80</span><span class="sxs-lookup"><span data-stu-id="8f7de-632">80</span></span></td>
<td><span data-ttu-id="8f7de-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="8f7de-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="8f7de-634">241.05</span><span class="sxs-lookup"><span data-stu-id="8f7de-634">241.05</span></span></td>
<td><span data-ttu-id="8f7de-635">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-636">Prod 2</span></span></td>
<td><span data-ttu-id="8f7de-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-637">Product 2</span></span></td>
<td><span data-ttu-id="8f7de-638">15</span><span class="sxs-lookup"><span data-stu-id="8f7de-638">15</span></span></td>
<td><span data-ttu-id="8f7de-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="8f7de-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="8f7de-640">45.20</span><span class="sxs-lookup"><span data-stu-id="8f7de-640">45.20</span></span></td>
<td><span data-ttu-id="8f7de-641">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-642">Prod 1</span></span></td>
<td><span data-ttu-id="8f7de-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-643">Product 1</span></span></td>
<td><span data-ttu-id="8f7de-644">80</span><span class="sxs-lookup"><span data-stu-id="8f7de-644">80</span></span></td>
<td><span data-ttu-id="8f7de-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="8f7de-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="8f7de-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="8f7de-646">2,507.09</span></span></td>
<td><span data-ttu-id="8f7de-647">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-648">Prod 2</span></span></td>
<td><span data-ttu-id="8f7de-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-649">Product 2</span></span></td>
<td><span data-ttu-id="8f7de-650">15</span><span class="sxs-lookup"><span data-stu-id="8f7de-650">15</span></span></td>
<td><span data-ttu-id="8f7de-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="8f7de-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="8f7de-652">470.08</span><span class="sxs-lookup"><span data-stu-id="8f7de-652">470.08</span></span></td>
<td><span data-ttu-id="8f7de-653">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="8f7de-654">Položky deníku (položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="8f7de-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8f7de-655">Deník</span><span class="sxs-lookup"><span data-stu-id="8f7de-655">Journal</span></span></th>
<th><span data-ttu-id="8f7de-656">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="8f7de-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="8f7de-657">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="8f7de-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="8f7de-658">Verze</span><span class="sxs-lookup"><span data-stu-id="8f7de-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8f7de-659">00004</span><span class="sxs-lookup"><span data-stu-id="8f7de-659">00004</span></span></td>
<td><span data-ttu-id="8f7de-660">Deník přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="8f7de-661">Fiskální</span><span class="sxs-lookup"><span data-stu-id="8f7de-661">Fiscal</span></span></td>
<td><span data-ttu-id="8f7de-662">2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-662">2017</span></span></td>
<td><span data-ttu-id="8f7de-663">Období 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-663">Period 1</span></span></td>
<td><span data-ttu-id="8f7de-664">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="8f7de-665">Řádky deníku</span><span class="sxs-lookup"><span data-stu-id="8f7de-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8f7de-666">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="8f7de-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="8f7de-667">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8f7de-668">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-668">Cost element</span></span></th>
<th><span data-ttu-id="8f7de-669">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-669">Cost behavior</span></span></th>
<th><span data-ttu-id="8f7de-670">Částka</span><span class="sxs-lookup"><span data-stu-id="8f7de-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8f7de-671">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="8f7de-672">CC001</span><span class="sxs-lookup"><span data-stu-id="8f7de-672">CC001</span></span></td>
<td><span data-ttu-id="8f7de-673">HR</span><span class="sxs-lookup"><span data-stu-id="8f7de-673">HR</span></span></td>
<td><span data-ttu-id="8f7de-674">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-674">10001</span></span></td>
<td><span data-ttu-id="8f7de-675">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-675">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-676">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-676">Fixed cost</span></span></td>
<td><span data-ttu-id="8f7de-677">500.00</span><span class="sxs-lookup"><span data-stu-id="8f7de-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-678">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="8f7de-679">CC001</span><span class="sxs-lookup"><span data-stu-id="8f7de-679">CC001</span></span></td>
<td><span data-ttu-id="8f7de-680">HR</span><span class="sxs-lookup"><span data-stu-id="8f7de-680">HR</span></span></td>
<td><span data-ttu-id="8f7de-681">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-681">10001</span></span></td>
<td><span data-ttu-id="8f7de-682">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-682">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-683">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-683">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="8f7de-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-685">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="8f7de-686">CC002</span><span class="sxs-lookup"><span data-stu-id="8f7de-686">CC002</span></span></td>
<td><span data-ttu-id="8f7de-687">Finance</span><span class="sxs-lookup"><span data-stu-id="8f7de-687">Finance</span></span></td>
<td><span data-ttu-id="8f7de-688">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-688">10001</span></span></td>
<td><span data-ttu-id="8f7de-689">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-689">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-690">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-690">Fixed cost</span></span></td>
<td><span data-ttu-id="8f7de-691">675.00</span><span class="sxs-lookup"><span data-stu-id="8f7de-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-692">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="8f7de-693">CC002</span><span class="sxs-lookup"><span data-stu-id="8f7de-693">CC002</span></span></td>
<td><span data-ttu-id="8f7de-694">Finance</span><span class="sxs-lookup"><span data-stu-id="8f7de-694">Finance</span></span></td>
<td><span data-ttu-id="8f7de-695">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-695">10001</span></span></td>
<td><span data-ttu-id="8f7de-696">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-696">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-697">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-697">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="8f7de-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-699">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="8f7de-700">CC003</span><span class="sxs-lookup"><span data-stu-id="8f7de-700">CC003</span></span></td>
<td><span data-ttu-id="8f7de-701">Sestavení</span><span class="sxs-lookup"><span data-stu-id="8f7de-701">Assembly</span></span></td>
<td><span data-ttu-id="8f7de-702">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-702">10001</span></span></td>
<td><span data-ttu-id="8f7de-703">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-703">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-704">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-704">Fixed cost</span></span></td>
<td><span data-ttu-id="8f7de-705">713.75</span><span class="sxs-lookup"><span data-stu-id="8f7de-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-706">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="8f7de-707">CC003</span><span class="sxs-lookup"><span data-stu-id="8f7de-707">CC003</span></span></td>
<td><span data-ttu-id="8f7de-708">Sestavení</span><span class="sxs-lookup"><span data-stu-id="8f7de-708">Assembly</span></span></td>
<td><span data-ttu-id="8f7de-709">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-709">10001</span></span></td>
<td><span data-ttu-id="8f7de-710">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-710">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-711">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-711">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="8f7de-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-713">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="8f7de-714">CC003</span><span class="sxs-lookup"><span data-stu-id="8f7de-714">CC003</span></span></td>
<td><span data-ttu-id="8f7de-715">Balení</span><span class="sxs-lookup"><span data-stu-id="8f7de-715">Packaging</span></span></td>
<td><span data-ttu-id="8f7de-716">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-716">10001</span></span></td>
<td><span data-ttu-id="8f7de-717">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-717">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-718">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-718">Fixed cost</span></span></td>
<td><span data-ttu-id="8f7de-719">286.25</span><span class="sxs-lookup"><span data-stu-id="8f7de-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-720">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="8f7de-721">CC003</span><span class="sxs-lookup"><span data-stu-id="8f7de-721">CC003</span></span></td>
<td><span data-ttu-id="8f7de-722">Balení</span><span class="sxs-lookup"><span data-stu-id="8f7de-722">Packaging</span></span></td>
<td><span data-ttu-id="8f7de-723">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-723">10001</span></span></td>
<td><span data-ttu-id="8f7de-724">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-724">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-725">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-725">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="8f7de-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-727">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="8f7de-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-728">Prod 1</span></span></td>
<td><span data-ttu-id="8f7de-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-729">Product 1</span></span></td>
<td><span data-ttu-id="8f7de-730">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-730">10001</span></span></td>
<td><span data-ttu-id="8f7de-731">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-731">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-732">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-732">Fixed cost</span></span></td>
<td><span data-ttu-id="8f7de-733">776.36</span><span class="sxs-lookup"><span data-stu-id="8f7de-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-734">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="8f7de-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-735">Prod 1</span></span></td>
<td><span data-ttu-id="8f7de-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-736">Product 1</span></span></td>
<td><span data-ttu-id="8f7de-737">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-737">10001</span></span></td>
<td><span data-ttu-id="8f7de-738">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-738">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-739">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-739">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="8f7de-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-741">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="8f7de-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-742">Prod 2</span></span></td>
<td><span data-ttu-id="8f7de-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-743">Product 1</span></span></td>
<td><span data-ttu-id="8f7de-744">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-744">10001</span></span></td>
<td><span data-ttu-id="8f7de-745">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-745">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-746">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-746">Fixed cost</span></span></td>
<td><span data-ttu-id="8f7de-747">223.64</span><span class="sxs-lookup"><span data-stu-id="8f7de-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-748">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="8f7de-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-749">Prod 2</span></span></td>
<td><span data-ttu-id="8f7de-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-750">Product 1</span></span></td>
<td><span data-ttu-id="8f7de-751">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-751">10001</span></span></td>
<td><span data-ttu-id="8f7de-752">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-752">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-753">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-753">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="8f7de-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="8f7de-755">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="8f7de-756">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="8f7de-757">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-757">Cost element</span></span></th>
<th><span data-ttu-id="8f7de-758">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-758">Cost behavior</span></span></th>
<th><span data-ttu-id="8f7de-759">Částka</span><span class="sxs-lookup"><span data-stu-id="8f7de-759">Amount</span></span></th>
<th><span data-ttu-id="8f7de-760">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="8f7de-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8f7de-761">CC001</span><span class="sxs-lookup"><span data-stu-id="8f7de-761">CC001</span></span></td>
<td><span data-ttu-id="8f7de-762">HR</span><span class="sxs-lookup"><span data-stu-id="8f7de-762">HR</span></span></td>
<td><span data-ttu-id="8f7de-763">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-763">10001</span></span></td>
<td><span data-ttu-id="8f7de-764">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-764">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-765">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-765">Fixed cost</span></span></td>
<td><span data-ttu-id="8f7de-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-766">-500.00</span></span></td>
<td><span data-ttu-id="8f7de-767">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-768">CC002</span><span class="sxs-lookup"><span data-stu-id="8f7de-768">CC002</span></span></td>
<td><span data-ttu-id="8f7de-769">Finance</span><span class="sxs-lookup"><span data-stu-id="8f7de-769">Finance</span></span></td>
<td><span data-ttu-id="8f7de-770">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-770">10001</span></span></td>
<td><span data-ttu-id="8f7de-771">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-771">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-772">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-772">Fixed cost</span></span></td>
<td><span data-ttu-id="8f7de-773">175.00</span><span class="sxs-lookup"><span data-stu-id="8f7de-773">175.00</span></span></td>
<td><span data-ttu-id="8f7de-774">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-775">CC003</span><span class="sxs-lookup"><span data-stu-id="8f7de-775">CC003</span></span></td>
<td><span data-ttu-id="8f7de-776">Sestavení</span><span class="sxs-lookup"><span data-stu-id="8f7de-776">Assembly</span></span></td>
<td><span data-ttu-id="8f7de-777">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-777">10001</span></span></td>
<td><span data-ttu-id="8f7de-778">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-778">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-779">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-779">Fixed cost</span></span></td>
<td><span data-ttu-id="8f7de-780">275.00</span><span class="sxs-lookup"><span data-stu-id="8f7de-780">275.00</span></span></td>
<td><span data-ttu-id="8f7de-781">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-782">CC004</span><span class="sxs-lookup"><span data-stu-id="8f7de-782">CC004</span></span></td>
<td><span data-ttu-id="8f7de-783">Balení</span><span class="sxs-lookup"><span data-stu-id="8f7de-783">Packaging</span></span></td>
<td><span data-ttu-id="8f7de-784">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-784">10001</span></span></td>
<td><span data-ttu-id="8f7de-785">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-785">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-786">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-786">Fixed cost</span></span></td>
<td><span data-ttu-id="8f7de-787">50,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-787">50,00</span></span></td>
<td><span data-ttu-id="8f7de-788">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-789">CC001</span><span class="sxs-lookup"><span data-stu-id="8f7de-789">CC001</span></span></td>
<td><span data-ttu-id="8f7de-790">HR</span><span class="sxs-lookup"><span data-stu-id="8f7de-790">HR</span></span></td>
<td><span data-ttu-id="8f7de-791">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-791">10001</span></span></td>
<td><span data-ttu-id="8f7de-792">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-792">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-793">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-793">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-794">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="8f7de-794">-1,245.71</span></span></td>
<td><span data-ttu-id="8f7de-795">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-796">CC002</span><span class="sxs-lookup"><span data-stu-id="8f7de-796">CC002</span></span></td>
<td><span data-ttu-id="8f7de-797">Finance</span><span class="sxs-lookup"><span data-stu-id="8f7de-797">Finance</span></span></td>
<td><span data-ttu-id="8f7de-798">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-798">10001</span></span></td>
<td><span data-ttu-id="8f7de-799">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-799">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-800">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-800">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-801">436.00</span><span class="sxs-lookup"><span data-stu-id="8f7de-801">436.00</span></span></td>
<td><span data-ttu-id="8f7de-802">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-803">CC003</span><span class="sxs-lookup"><span data-stu-id="8f7de-803">CC003</span></span></td>
<td><span data-ttu-id="8f7de-804">Sestavení</span><span class="sxs-lookup"><span data-stu-id="8f7de-804">Assembly</span></span></td>
<td><span data-ttu-id="8f7de-805">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-805">10001</span></span></td>
<td><span data-ttu-id="8f7de-806">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-806">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-807">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-807">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-808">685.14</span><span class="sxs-lookup"><span data-stu-id="8f7de-808">685.14</span></span></td>
<td><span data-ttu-id="8f7de-809">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-810">CC004</span><span class="sxs-lookup"><span data-stu-id="8f7de-810">CC004</span></span></td>
<td><span data-ttu-id="8f7de-811">Balení</span><span class="sxs-lookup"><span data-stu-id="8f7de-811">Packaging</span></span></td>
<td><span data-ttu-id="8f7de-812">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-812">10001</span></span></td>
<td><span data-ttu-id="8f7de-813">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-813">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-814">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-814">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-815">124.57</span><span class="sxs-lookup"><span data-stu-id="8f7de-815">124.57</span></span></td>
<td><span data-ttu-id="8f7de-816">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-817">CC002</span><span class="sxs-lookup"><span data-stu-id="8f7de-817">CC002</span></span></td>
<td><span data-ttu-id="8f7de-818">Finance</span><span class="sxs-lookup"><span data-stu-id="8f7de-818">Finance</span></span></td>
<td><span data-ttu-id="8f7de-819">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-819">10001</span></span></td>
<td><span data-ttu-id="8f7de-820">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-820">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-821">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-821">Fixed cost</span></span></td>
<td><span data-ttu-id="8f7de-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-822">-675.00</span></span></td>
<td><span data-ttu-id="8f7de-823">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-824">CC003</span><span class="sxs-lookup"><span data-stu-id="8f7de-824">CC003</span></span></td>
<td><span data-ttu-id="8f7de-825">Sestavení</span><span class="sxs-lookup"><span data-stu-id="8f7de-825">Assembly</span></span></td>
<td><span data-ttu-id="8f7de-826">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-826">10001</span></span></td>
<td><span data-ttu-id="8f7de-827">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-827">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-828">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-828">Fixed cost</span></span></td>
<td><span data-ttu-id="8f7de-829">438.75</span><span class="sxs-lookup"><span data-stu-id="8f7de-829">438.75</span></span></td>
<td><span data-ttu-id="8f7de-830">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-831">CC004</span><span class="sxs-lookup"><span data-stu-id="8f7de-831">CC004</span></span></td>
<td><span data-ttu-id="8f7de-832">Balení</span><span class="sxs-lookup"><span data-stu-id="8f7de-832">Packaging</span></span></td>
<td><span data-ttu-id="8f7de-833">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-833">10001</span></span></td>
<td><span data-ttu-id="8f7de-834">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-834">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-835">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-835">Fixed cost</span></span></td>
<td><span data-ttu-id="8f7de-836">236.25</span><span class="sxs-lookup"><span data-stu-id="8f7de-836">236.25</span></span></td>
<td><span data-ttu-id="8f7de-837">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-838">CC002</span><span class="sxs-lookup"><span data-stu-id="8f7de-838">CC002</span></span></td>
<td><span data-ttu-id="8f7de-839">Finance</span><span class="sxs-lookup"><span data-stu-id="8f7de-839">Finance</span></span></td>
<td><span data-ttu-id="8f7de-840">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-840">10001</span></span></td>
<td><span data-ttu-id="8f7de-841">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-841">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-842">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-842">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-843">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="8f7de-843">-8,150.29</span></span></td>
<td><span data-ttu-id="8f7de-844">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-845">CC003</span><span class="sxs-lookup"><span data-stu-id="8f7de-845">CC003</span></span></td>
<td><span data-ttu-id="8f7de-846">Sestavení</span><span class="sxs-lookup"><span data-stu-id="8f7de-846">Assembly</span></span></td>
<td><span data-ttu-id="8f7de-847">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-847">10001</span></span></td>
<td><span data-ttu-id="8f7de-848">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-848">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-849">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-849">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="8f7de-850">5,297.69</span></span></td>
<td><span data-ttu-id="8f7de-851">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-852">CC004</span><span class="sxs-lookup"><span data-stu-id="8f7de-852">CC004</span></span></td>
<td><span data-ttu-id="8f7de-853">Balení</span><span class="sxs-lookup"><span data-stu-id="8f7de-853">Packaging</span></span></td>
<td><span data-ttu-id="8f7de-854">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-854">10001</span></span></td>
<td><span data-ttu-id="8f7de-855">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-855">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-856">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-856">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="8f7de-857">2,852.60</span></span></td>
<td><span data-ttu-id="8f7de-858">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-859">CC003</span><span class="sxs-lookup"><span data-stu-id="8f7de-859">CC003</span></span></td>
<td><span data-ttu-id="8f7de-860">Sestavení</span><span class="sxs-lookup"><span data-stu-id="8f7de-860">Assembly</span></span></td>
<td><span data-ttu-id="8f7de-861">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-861">10001</span></span></td>
<td><span data-ttu-id="8f7de-862">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-862">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-863">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-863">Fixed cost</span></span></td>
<td><span data-ttu-id="8f7de-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="8f7de-864">-713.75</span></span></td>
<td><span data-ttu-id="8f7de-865">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-866">Prod 1</span></span></td>
<td><span data-ttu-id="8f7de-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-867">Product 1</span></span></td>
<td><span data-ttu-id="8f7de-868">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-868">10001</span></span></td>
<td><span data-ttu-id="8f7de-869">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-869">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-870">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-870">Fixed cost</span></span></td>
<td><span data-ttu-id="8f7de-871">535.31</span><span class="sxs-lookup"><span data-stu-id="8f7de-871">535.31</span></span></td>
<td><span data-ttu-id="8f7de-872">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-873">Prod 2</span></span></td>
<td><span data-ttu-id="8f7de-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-874">Product 2</span></span></td>
<td><span data-ttu-id="8f7de-875">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-875">10001</span></span></td>
<td><span data-ttu-id="8f7de-876">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-876">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-877">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-877">Fixed cost</span></span></td>
<td><span data-ttu-id="8f7de-878">178.44</span><span class="sxs-lookup"><span data-stu-id="8f7de-878">178.44</span></span></td>
<td><span data-ttu-id="8f7de-879">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-880">CC003</span><span class="sxs-lookup"><span data-stu-id="8f7de-880">CC003</span></span></td>
<td><span data-ttu-id="8f7de-881">Sestavení</span><span class="sxs-lookup"><span data-stu-id="8f7de-881">Assembly</span></span></td>
<td><span data-ttu-id="8f7de-882">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-882">10001</span></span></td>
<td><span data-ttu-id="8f7de-883">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-883">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-884">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-884">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-885">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="8f7de-885">-5,982.83</span></span></td>
<td><span data-ttu-id="8f7de-886">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-887">Prod 1</span></span></td>
<td><span data-ttu-id="8f7de-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-888">Product 1</span></span></td>
<td><span data-ttu-id="8f7de-889">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-889">10001</span></span></td>
<td><span data-ttu-id="8f7de-890">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-890">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-891">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-891">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="8f7de-892">4,487.12</span></span></td>
<td><span data-ttu-id="8f7de-893">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-894">Prod 2</span></span></td>
<td><span data-ttu-id="8f7de-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-895">Product 2</span></span></td>
<td><span data-ttu-id="8f7de-896">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-896">10001</span></span></td>
<td><span data-ttu-id="8f7de-897">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-897">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-898">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-898">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="8f7de-899">1,495.71</span></span></td>
<td><span data-ttu-id="8f7de-900">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-901">CC003</span><span class="sxs-lookup"><span data-stu-id="8f7de-901">CC003</span></span></td>
<td><span data-ttu-id="8f7de-902">Sestavení</span><span class="sxs-lookup"><span data-stu-id="8f7de-902">Assembly</span></span></td>
<td><span data-ttu-id="8f7de-903">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-903">10001</span></span></td>
<td><span data-ttu-id="8f7de-904">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-904">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-905">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-905">Fixed cost</span></span></td>
<td><span data-ttu-id="8f7de-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="8f7de-906">-286.25</span></span></td>
<td><span data-ttu-id="8f7de-907">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-908">Prod 1</span></span></td>
<td><span data-ttu-id="8f7de-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-909">Product 1</span></span></td>
<td><span data-ttu-id="8f7de-910">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-910">10001</span></span></td>
<td><span data-ttu-id="8f7de-911">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-911">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-912">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-912">Fixed cost</span></span></td>
<td><span data-ttu-id="8f7de-913">241.05</span><span class="sxs-lookup"><span data-stu-id="8f7de-913">241.05</span></span></td>
<td><span data-ttu-id="8f7de-914">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-915">Prod 2</span></span></td>
<td><span data-ttu-id="8f7de-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-916">Product 2</span></span></td>
<td><span data-ttu-id="8f7de-917">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-917">10001</span></span></td>
<td><span data-ttu-id="8f7de-918">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-918">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-919">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-919">Fixed cost</span></span></td>
<td><span data-ttu-id="8f7de-920">45.20</span><span class="sxs-lookup"><span data-stu-id="8f7de-920">45.20</span></span></td>
<td><span data-ttu-id="8f7de-921">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-922">CC003</span><span class="sxs-lookup"><span data-stu-id="8f7de-922">CC003</span></span></td>
<td><span data-ttu-id="8f7de-923">Sestavení</span><span class="sxs-lookup"><span data-stu-id="8f7de-923">Assembly</span></span></td>
<td><span data-ttu-id="8f7de-924">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-924">10001</span></span></td>
<td><span data-ttu-id="8f7de-925">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-925">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-926">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-926">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="8f7de-927">-2,977.17</span></span></td>
<td><span data-ttu-id="8f7de-928">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-929">Prod 1</span></span></td>
<td><span data-ttu-id="8f7de-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-930">Product 1</span></span></td>
<td><span data-ttu-id="8f7de-931">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-931">10001</span></span></td>
<td><span data-ttu-id="8f7de-932">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-932">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-933">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-933">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="8f7de-934">2,507.09</span></span></td>
<td><span data-ttu-id="8f7de-935">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8f7de-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-936">Prod 2</span></span></td>
<td><span data-ttu-id="8f7de-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-937">Product 2</span></span></td>
<td><span data-ttu-id="8f7de-938">10001</span><span class="sxs-lookup"><span data-stu-id="8f7de-938">10001</span></span></td>
<td><span data-ttu-id="8f7de-939">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="8f7de-939">Electricity</span></span></td>
<td><span data-ttu-id="8f7de-940">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-940">Variable cost</span></span></td>
<td><span data-ttu-id="8f7de-941">470.08</span><span class="sxs-lookup"><span data-stu-id="8f7de-941">470.08</span></span></td>
<td><span data-ttu-id="8f7de-942">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="8f7de-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="8f7de-943">Závěr</span><span class="sxs-lookup"><span data-stu-id="8f7de-943">Conclusion</span></span>
<span data-ttu-id="8f7de-944">Ve finančním účtování se náklady za elektřinu ve výši 10 000 zaúčtují na ID fiktivního nákladového střediska.</span><span class="sxs-lookup"><span data-stu-id="8f7de-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="8f7de-945">Účetní tak budou vědět, že tento náklad musí být přidělen.</span><span class="sxs-lookup"><span data-stu-id="8f7de-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="8f7de-946">V nákladovém účetnictví náklady procházejí napříč organizačními jednotkami a úrovněmi, na základě použitých zásad a pravidel.</span><span class="sxs-lookup"><span data-stu-id="8f7de-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="8f7de-947">Každý náklad byl přidružen k základu přidělení, který poskytuje nejlepší hodnocení pro přidělení nákladů.</span><span class="sxs-lookup"><span data-stu-id="8f7de-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="8f7de-948">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="8f7de-949">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="8f7de-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="8f7de-950">Celkem</span><span class="sxs-lookup"><span data-stu-id="8f7de-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="8f7de-951">CC099</span><span class="sxs-lookup"><span data-stu-id="8f7de-951">CC099</span></span></th>
<th><span data-ttu-id="8f7de-952">CC001</span><span class="sxs-lookup"><span data-stu-id="8f7de-952">CC001</span></span></th>
<th><span data-ttu-id="8f7de-953">CC002</span><span class="sxs-lookup"><span data-stu-id="8f7de-953">CC002</span></span></th>
<th><span data-ttu-id="8f7de-954">CC003</span><span class="sxs-lookup"><span data-stu-id="8f7de-954">CC003</span></span></th>
<th><span data-ttu-id="8f7de-955">CC004</span><span class="sxs-lookup"><span data-stu-id="8f7de-955">CC004</span></span></th>
<th><span data-ttu-id="8f7de-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-956">Proj 1</span></span></th>
<th><span data-ttu-id="8f7de-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-957">Proj 2</span></span></th>
<th><span data-ttu-id="8f7de-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="8f7de-958">Prod 1</span></span></th>
<th><span data-ttu-id="8f7de-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="8f7de-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="8f7de-960">10001 Elektřina</span><span class="sxs-lookup"><span data-stu-id="8f7de-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8f7de-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="8f7de-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8f7de-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="8f7de-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8f7de-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="8f7de-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8f7de-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="8f7de-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="8f7de-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="8f7de-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8f7de-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="8f7de-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8f7de-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="8f7de-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8f7de-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="8f7de-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="8f7de-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="8f7de-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="8f7de-970">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="8f7de-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8f7de-971">0,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="8f7de-972">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8f7de-973">0,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8f7de-974">0,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8f7de-975">0,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8f7de-976">0,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8f7de-977">0,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="8f7de-978">776.36</span><span class="sxs-lookup"><span data-stu-id="8f7de-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8f7de-979">223.64</span><span class="sxs-lookup"><span data-stu-id="8f7de-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8f7de-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="8f7de-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="8f7de-981">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="8f7de-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8f7de-982">000</span><span class="sxs-lookup"><span data-stu-id="8f7de-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8f7de-983">0,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8f7de-984">0,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8f7de-985">0,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8f7de-986">0,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8f7de-987">30.00</span><span class="sxs-lookup"><span data-stu-id="8f7de-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8f7de-988">10,00</span><span class="sxs-lookup"><span data-stu-id="8f7de-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8f7de-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="8f7de-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8f7de-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="8f7de-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="8f7de-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="8f7de-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="8f7de-992">Toto téma popisuje, jak primární prvek nákladů, 10001 Elektřina, prochází přes objekty nákladů.</span><span class="sxs-lookup"><span data-stu-id="8f7de-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="8f7de-993">Tyto režijní náklady tedy budou přiděleny na nejnižší úroveň v organizaci.</span><span class="sxs-lookup"><span data-stu-id="8f7de-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="8f7de-994">Jinak řečeno, objekty nákladů na nejnižší úrovni ponesou náklady.</span><span class="sxs-lookup"><span data-stu-id="8f7de-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="8f7de-995">Chcete-li vizuální tok nákladů mezi objekty nákladů, můžete použít pravidla zásad shrnutí nákladů pro vizualizaci jejich toků.</span><span class="sxs-lookup"><span data-stu-id="8f7de-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="8f7de-996">Další informace naleznete v tématu [Zásady shrnutí nákladů a výpočet režijních nákladů](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="8f7de-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]