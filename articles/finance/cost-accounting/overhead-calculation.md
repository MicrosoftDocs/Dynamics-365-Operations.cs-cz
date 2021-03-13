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
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: d60248f2bd6774b2e9afdb3632b6eb31d67349ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009511"
---
# <a name="overhead-calculation"></a><span data-ttu-id="f8cb8-103">Výpočet režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8cb8-104">Toto téma popisuje typické procesy pro výpočet a přidělení režijních nákladů.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="f8cb8-105">Definice termínu</span><span class="sxs-lookup"><span data-stu-id="f8cb8-105">Term definition</span></span>
---------------

<span data-ttu-id="f8cb8-106">Režijní náklady jsou náklady, které nutně vznikají při chodu podnikání, ale nelze je připsat přímo k žádné konkrétní podnikatelské aktivitě, produktu nebo službě.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="f8cb8-107">Režijní náklady poskytují důležitou podporu pro generování aktivity přinášejících zisk.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="f8cb8-108">Následuje několik příkladů režijních nákladů:</span><span class="sxs-lookup"><span data-stu-id="f8cb8-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="f8cb8-109">Renta</span><span class="sxs-lookup"><span data-stu-id="f8cb8-109">Rent</span></span>
-   <span data-ttu-id="f8cb8-110">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-110">Electricity</span></span>
-   <span data-ttu-id="f8cb8-111">Administrativní mzdy</span><span class="sxs-lookup"><span data-stu-id="f8cb8-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="f8cb8-112">Přehled výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-112">Overhead calculation overview</span></span>
<span data-ttu-id="f8cb8-113">Výpočet režijních nákladů spustí zásady účtování nákladů ve správném pořadí.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="f8cb8-114">Výpočet režijních nákladů můžete pro stejné fiskální období spustit mnohokrát, pokud došlo ke změně zásad účtování nákladů nebo zjištění konkrétních chyb.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="f8cb8-115">Každé spuštění výpočtu režijních nákladů se ukládá a přijímá ID jedinečné verze, které vám umožní porovnávat výpočty v různých verzích.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="f8cb8-116">Položky nákladů, které generuje výpočet režijních nákladů, přijímá datum účtování.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="f8cb8-117">Toto datum účtován se shoduje s konvovým datem fiskálního období, které se použije ve výpočtu.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="f8cb8-118">ID jedinečné verze se skládá z následujících prvků:</span><span class="sxs-lookup"><span data-stu-id="f8cb8-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="f8cb8-119">Typ verze</span><span class="sxs-lookup"><span data-stu-id="f8cb8-119">Version type</span></span>
-   <span data-ttu-id="f8cb8-120">Datum a čas</span><span class="sxs-lookup"><span data-stu-id="f8cb8-120">Date and time</span></span>
-   <span data-ttu-id="f8cb8-121">Hlavní kniha nákladového účetnictví</span><span class="sxs-lookup"><span data-stu-id="f8cb8-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="f8cb8-122">Fiskální rok</span><span class="sxs-lookup"><span data-stu-id="f8cb8-122">Fiscal year</span></span>
-   <span data-ttu-id="f8cb8-123">Fiskální období</span><span class="sxs-lookup"><span data-stu-id="f8cb8-123">Fiscal period</span></span>

<span data-ttu-id="f8cb8-124">Výpočet režijních nákladů se spustí bez ohledu na verzi.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="f8cb8-125">Proto lze vypočítat rozpočtovou verzi před skutečnou verzí.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="f8cb8-126">Výpočet režijních nákladů se skládá ze čtyř kroků uvedených na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="f8cb8-127">V každé fázi je vytvořeno záhlaví deníku, které obsahuje položky deníku.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="f8cb8-128">Toto záhlaví deníku zachovává vstupní data pro každý krok výpočtu.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="f8cb8-129">Zásady a pravidla se použijí na každý řádek deníku a položky nákladů jsou generovány jako výstup.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="f8cb8-130">Máte tedy vždy plnou sledovatelnost.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="f8cb8-131">[![Výpočet režijních nákladů](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="f8cb8-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="f8cb8-132">Výpočet a přidělení režijních nákladů za elektřinu</span><span class="sxs-lookup"><span data-stu-id="f8cb8-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="f8cb8-133">Ve finančním účetnictví se některé náklady, jako je například elektřina, registrují jako paušální.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="f8cb8-134">Podrobný přehled pro vedoucí není tedy pro nákladové účetnictví k dispozici.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="f8cb8-135">V nákladovém účetnictví musí náklady procházet organizačními jednotkami, aby byl získán správný přehled pro vedoucí napříč všemi jednotkami a úrovněmi organizace.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="f8cb8-136">Tento tok musí být založen buď na přesném záznamu spotřeby nebo na objektivním hodnocení.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="f8cb8-137">V hlavní knize mohou být zaúčtovány náklady na elektřinu způsobem znázorněným v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f8cb8-138">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="f8cb8-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="f8cb8-139">Nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="f8cb8-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="f8cb8-140">Hlavní účet</span><span class="sxs-lookup"><span data-stu-id="f8cb8-140">Main account</span></span></th>
<th><span data-ttu-id="f8cb8-141">Částka v zúčtovací měně</span><span class="sxs-lookup"><span data-stu-id="f8cb8-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8cb8-142">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="f8cb8-143">CC099</span><span class="sxs-lookup"><span data-stu-id="f8cb8-143">CC099</span></span></td>
<td><span data-ttu-id="f8cb8-144">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="f8cb8-144">Default cost center</span></span></td>
<td><span data-ttu-id="f8cb8-145">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-145">10001</span></span></td>
<td><span data-ttu-id="f8cb8-146">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-146">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="f8cb8-148">Krok 1: Zpracování výpočtu chování nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="f8cb8-149">Ve výchozím nastavení dostanou při importu položek nákladů z datového zdroje tyto položky v nákladovém účetnictví klasifikaci **Neklasifikované**.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="f8cb8-150">Použitím pravidla zásad chování nákladů lze reklasifikovat položky nákladů jako **Pevné náklady** nebo **Variabilní náklady**.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="f8cb8-151">Definice pravidel chování nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-151">Define the cost behavior rule</span></span>

<span data-ttu-id="f8cb8-152">V některých případech je část nákladů s pevným poplatkem a zbývající náklady jsou založeny na spotřebě.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="f8cb8-153">Účty za elektřinu často odpovídají této definici.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="f8cb8-154">Po platbě konkrétního pevného poplatku platíte spotřebu za kilowatthodinu (kWh).</span><span class="sxs-lookup"><span data-stu-id="f8cb8-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="f8cb8-155">Pokud je například poplatek pevných nákladů 1 000,00, definuje se pravidlo chování nákladů takto:</span><span class="sxs-lookup"><span data-stu-id="f8cb8-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="f8cb8-156">Pevná částka 1 000,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="f8cb8-157">0 &lt;= 1 000,00 = Pevná</span><span class="sxs-lookup"><span data-stu-id="f8cb8-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="f8cb8-158">1 000,01 &lt; N = Variabilní</span><span class="sxs-lookup"><span data-stu-id="f8cb8-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="f8cb8-159">Deník</span><span class="sxs-lookup"><span data-stu-id="f8cb8-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f8cb8-160">Deník</span><span class="sxs-lookup"><span data-stu-id="f8cb8-160">Journal</span></span></th>
<th><span data-ttu-id="f8cb8-161">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="f8cb8-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="f8cb8-162">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="f8cb8-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="f8cb8-163">Verze</span><span class="sxs-lookup"><span data-stu-id="f8cb8-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8cb8-164">00001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-164">00001</span></span></td>
<td><span data-ttu-id="f8cb8-165">Deník výpočtu chování nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="f8cb8-166">Fiskální</span><span class="sxs-lookup"><span data-stu-id="f8cb8-166">Fiscal</span></span></td>
<td><span data-ttu-id="f8cb8-167">2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-167">2017</span></span></td>
<td><span data-ttu-id="f8cb8-168">Období 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-168">Period 1</span></span></td>
<td><span data-ttu-id="f8cb8-169">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="f8cb8-170">Položky deníku (Položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="f8cb8-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f8cb8-171">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="f8cb8-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="f8cb8-172">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f8cb8-173">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-173">Cost element</span></span></th>
<th><span data-ttu-id="f8cb8-174">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-174">Cost behavior</span></span></th>
<th><span data-ttu-id="f8cb8-175">Částka</span><span class="sxs-lookup"><span data-stu-id="f8cb8-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8cb8-176">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="f8cb8-177">CC099</span><span class="sxs-lookup"><span data-stu-id="f8cb8-177">CC099</span></span></td>
<td><span data-ttu-id="f8cb8-178">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="f8cb8-178">Default cost center</span></span></td>
<td><span data-ttu-id="f8cb8-179">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-179">10001</span></span></td>
<td><span data-ttu-id="f8cb8-180">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-180">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-181">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="f8cb8-181">Unclassified</span></span></td>
<td><span data-ttu-id="f8cb8-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="f8cb8-183">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f8cb8-184">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f8cb8-185">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-185">Cost element</span></span></th>
<th><span data-ttu-id="f8cb8-186">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-186">Cost behavior</span></span></th>
<th><span data-ttu-id="f8cb8-187">Částka</span><span class="sxs-lookup"><span data-stu-id="f8cb8-187">Amount</span></span></th>
<th><span data-ttu-id="f8cb8-188">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="f8cb8-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8cb8-189">CC099</span><span class="sxs-lookup"><span data-stu-id="f8cb8-189">CC099</span></span></td>
<td><span data-ttu-id="f8cb8-190">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="f8cb8-190">Default cost center</span></span></td>
<td><span data-ttu-id="f8cb8-191">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-191">10001</span></span></td>
<td><span data-ttu-id="f8cb8-192">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-192">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-193">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="f8cb8-193">Unclassified</span></span></td>
<td><span data-ttu-id="f8cb8-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-194">10,000.00</span></span></td>
<td><span data-ttu-id="f8cb8-195">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-196">CC099</span><span class="sxs-lookup"><span data-stu-id="f8cb8-196">CC099</span></span></td>
<td><span data-ttu-id="f8cb8-197">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="f8cb8-197">Default cost center</span></span></td>
<td><span data-ttu-id="f8cb8-198">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-198">10001</span></span></td>
<td><span data-ttu-id="f8cb8-199">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-199">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-200">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="f8cb8-200">Unclassified</span></span></td>
<td><span data-ttu-id="f8cb8-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-201">-10,000.00</span></span></td>
<td><span data-ttu-id="f8cb8-202">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-203">CC099</span><span class="sxs-lookup"><span data-stu-id="f8cb8-203">CC099</span></span></td>
<td><span data-ttu-id="f8cb8-204">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="f8cb8-204">Default cost center</span></span></td>
<td><span data-ttu-id="f8cb8-205">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-205">10001</span></span></td>
<td><span data-ttu-id="f8cb8-206">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-206">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-207">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-207">Fixed cost</span></span></td>
<td><span data-ttu-id="f8cb8-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-208">1,000.00</span></span></td>
<td><span data-ttu-id="f8cb8-209">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-210">CC099</span><span class="sxs-lookup"><span data-stu-id="f8cb8-210">CC099</span></span></td>
<td><span data-ttu-id="f8cb8-211">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="f8cb8-211">Default cost center</span></span></td>
<td><span data-ttu-id="f8cb8-212">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-212">10001</span></span></td>
<td><span data-ttu-id="f8cb8-213">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-213">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-214">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-214">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-215">9,000.00</span></span></td>
<td><span data-ttu-id="f8cb8-216">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f8cb8-217">Více informací naleznete v tématu [Vytvoření a přiřazení zásad chování nákladů k jednotce řízení nákladů](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="f8cb8-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="f8cb8-218">Krok 2: Zpracování výpočtu distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="f8cb8-219">Distribuce nákladů se používá k rozdělení nákladů z jednoho objektu nákladů na jeden nebo více dalších objektů nákladů použitím příslušného základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="f8cb8-220">Distribuce nákladů a přidělení nákladů se liší v tom, že k distribuci nákladů dochází vždy na úrovni primárního prvku nákladů původních nákladů.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="f8cb8-221">Definice pravidel distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-221">Define the cost distribution rule</span></span>

<span data-ttu-id="f8cb8-222">Ve finančním účetnictví se náklady na elektřinu často registrují jako paušální.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="f8cb8-223">V nákladovém účetnictví není tento přístup dostatečně podrobný.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="f8cb8-224">Variabilní náklady by měly být distribuovány k jednotlivým objektům nákladů na solidním základě.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="f8cb8-225">Nejlogičtější základ přidělení je spotřeba elektřiny (kWh).</span><span class="sxs-lookup"><span data-stu-id="f8cb8-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="f8cb8-226">Vytvoří se člen statistické dimenzi s názvem Elektřina a zaznamená se elektrické spotřeba.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="f8cb8-227">Ve výchozím nastavení se všechny členy statistické dimenze stanou dostupnými zpřístupněny jako základy přidělení.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f8cb8-228">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-228">Cost object</span></span></th>
<th><span data-ttu-id="f8cb8-229">kWh</span><span class="sxs-lookup"><span data-stu-id="f8cb8-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8cb8-230">CC001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-230">CC001</span></span></td>
<td><span data-ttu-id="f8cb8-231">HR</span><span class="sxs-lookup"><span data-stu-id="f8cb8-231">HR</span></span></td>
<td><span data-ttu-id="f8cb8-232">1 000</span><span class="sxs-lookup"><span data-stu-id="f8cb8-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-233">CC002</span><span class="sxs-lookup"><span data-stu-id="f8cb8-233">CC002</span></span></td>
<td><span data-ttu-id="f8cb8-234">Finance</span><span class="sxs-lookup"><span data-stu-id="f8cb8-234">Finance</span></span></td>
<td><span data-ttu-id="f8cb8-235">6,000</span><span class="sxs-lookup"><span data-stu-id="f8cb8-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-236">CC003</span><span class="sxs-lookup"><span data-stu-id="f8cb8-236">CC003</span></span></td>
<td><span data-ttu-id="f8cb8-237">Sestavení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-237">Assembly</span></span></td>
<td><span data-ttu-id="f8cb8-238">0</span><span class="sxs-lookup"><span data-stu-id="f8cb8-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f8cb8-239">Následující tabulka zobrazuje výsledek při použití elektrické spotřeby jako základu přidělení pro variabilní náklady.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f8cb8-240">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-240">Cost object</span></span></th>
<th><span data-ttu-id="f8cb8-241">Hodnota</span><span class="sxs-lookup"><span data-stu-id="f8cb8-241">Magnitude</span></span></th>
<th><span data-ttu-id="f8cb8-242">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-242">Allocation factor</span></span></th>
<th><span data-ttu-id="f8cb8-243">Částka</span><span class="sxs-lookup"><span data-stu-id="f8cb8-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8cb8-244">CC001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-244">CC001</span></span></td>
<td><span data-ttu-id="f8cb8-245">HR</span><span class="sxs-lookup"><span data-stu-id="f8cb8-245">HR</span></span></td>
<td><span data-ttu-id="f8cb8-246">1 000</span><span class="sxs-lookup"><span data-stu-id="f8cb8-246">1,000</span></span></td>
<td><span data-ttu-id="f8cb8-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="f8cb8-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="f8cb8-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-249">CC002</span><span class="sxs-lookup"><span data-stu-id="f8cb8-249">CC002</span></span></td>
<td><span data-ttu-id="f8cb8-250">Finance</span><span class="sxs-lookup"><span data-stu-id="f8cb8-250">Finance</span></span></td>
<td><span data-ttu-id="f8cb8-251">6,000</span><span class="sxs-lookup"><span data-stu-id="f8cb8-251">6,000</span></span></td>
<td><span data-ttu-id="f8cb8-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="f8cb8-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="f8cb8-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-254">CC003</span><span class="sxs-lookup"><span data-stu-id="f8cb8-254">CC003</span></span></td>
<td><span data-ttu-id="f8cb8-255">Sestavení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-255">Assembly</span></span></td>
<td><span data-ttu-id="f8cb8-256">0</span><span class="sxs-lookup"><span data-stu-id="f8cb8-256">0</span></span></td>
<td><span data-ttu-id="f8cb8-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="f8cb8-258">0,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f8cb8-259">Pevné náklady musí být distribuovány rovnoměrně k jednotlivých objektům nákladů, které spotřebovávaly elektřinu.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="f8cb8-260">Tohoto výsledku můžete dosáhnout pomocí členu statistické dimenze Elektřina v základu přidělení vzorce: (Elektřina &gt; 0,00) Následující tabulka zobrazuje výsledek při použití elektrické spotřeby jako základu přidělení pro variabilní náklady.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f8cb8-261">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-261">Cost object</span></span></th>
<th><span data-ttu-id="f8cb8-262">Vzorec</span><span class="sxs-lookup"><span data-stu-id="f8cb8-262">Formula</span></span></th>
<th><span data-ttu-id="f8cb8-263">Hodnota</span><span class="sxs-lookup"><span data-stu-id="f8cb8-263">Magnitude</span></span></th>
<th><span data-ttu-id="f8cb8-264">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-264">Allocation factor</span></span></th>
<th><span data-ttu-id="f8cb8-265">Částka</span><span class="sxs-lookup"><span data-stu-id="f8cb8-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8cb8-266">CC001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-266">CC001</span></span></td>
<td><span data-ttu-id="f8cb8-267">HR</span><span class="sxs-lookup"><span data-stu-id="f8cb8-267">HR</span></span></td>
<td><span data-ttu-id="f8cb8-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="f8cb8-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="f8cb8-269">1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-269">1</span></span></td>
<td><span data-ttu-id="f8cb8-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="f8cb8-271">500.00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-272">CC002</span><span class="sxs-lookup"><span data-stu-id="f8cb8-272">CC002</span></span></td>
<td><span data-ttu-id="f8cb8-273">Finance</span><span class="sxs-lookup"><span data-stu-id="f8cb8-273">Finance</span></span></td>
<td><span data-ttu-id="f8cb8-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="f8cb8-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="f8cb8-275">1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-275">1</span></span></td>
<td><span data-ttu-id="f8cb8-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="f8cb8-277">500.00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-278">CC003</span><span class="sxs-lookup"><span data-stu-id="f8cb8-278">CC003</span></span></td>
<td><span data-ttu-id="f8cb8-279">Sestavení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-279">Assembly</span></span></td>
<td><span data-ttu-id="f8cb8-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="f8cb8-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="f8cb8-281">0</span><span class="sxs-lookup"><span data-stu-id="f8cb8-281">0</span></span></td>
<td><span data-ttu-id="f8cb8-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="f8cb8-283">0,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="f8cb8-284">Deník</span><span class="sxs-lookup"><span data-stu-id="f8cb8-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f8cb8-285">Deník</span><span class="sxs-lookup"><span data-stu-id="f8cb8-285">Journal</span></span></th>
<th><span data-ttu-id="f8cb8-286">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="f8cb8-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="f8cb8-287">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="f8cb8-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="f8cb8-288">Verze</span><span class="sxs-lookup"><span data-stu-id="f8cb8-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8cb8-289">00002</span><span class="sxs-lookup"><span data-stu-id="f8cb8-289">00002</span></span></td>
<td><span data-ttu-id="f8cb8-290">Deník výpočtu distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="f8cb8-291">Fiskální</span><span class="sxs-lookup"><span data-stu-id="f8cb8-291">Fiscal</span></span></td>
<td><span data-ttu-id="f8cb8-292">2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-292">2017</span></span></td>
<td><span data-ttu-id="f8cb8-293">Období 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-293">Period 1</span></span></td>
<td><span data-ttu-id="f8cb8-294">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="f8cb8-295">Položky deníku (Položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="f8cb8-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f8cb8-296">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="f8cb8-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="f8cb8-297">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f8cb8-298">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-298">Cost element</span></span></th>
<th><span data-ttu-id="f8cb8-299">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-299">Cost behavior</span></span></th>
<th><span data-ttu-id="f8cb8-300">Částka</span><span class="sxs-lookup"><span data-stu-id="f8cb8-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8cb8-301">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="f8cb8-302">CC099</span><span class="sxs-lookup"><span data-stu-id="f8cb8-302">CC099</span></span></td>
<td><span data-ttu-id="f8cb8-303">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="f8cb8-303">Default cost center</span></span></td>
<td><span data-ttu-id="f8cb8-304">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-304">10001</span></span></td>
<td><span data-ttu-id="f8cb8-305">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-305">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-306">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-306">Fixed cost</span></span></td>
<td><span data-ttu-id="f8cb8-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-308">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="f8cb8-309">CC099</span><span class="sxs-lookup"><span data-stu-id="f8cb8-309">CC099</span></span></td>
<td><span data-ttu-id="f8cb8-310">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="f8cb8-310">Default cost center</span></span></td>
<td><span data-ttu-id="f8cb8-311">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-311">10001</span></span></td>
<td><span data-ttu-id="f8cb8-312">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-312">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-313">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-313">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="f8cb8-315">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f8cb8-316">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f8cb8-317">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-317">Cost element</span></span></th>
<th><span data-ttu-id="f8cb8-318">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-318">Cost behavior</span></span></th>
<th><span data-ttu-id="f8cb8-319">Částka</span><span class="sxs-lookup"><span data-stu-id="f8cb8-319">Amount</span></span></th>
<th><span data-ttu-id="f8cb8-320">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="f8cb8-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8cb8-321">CC099</span><span class="sxs-lookup"><span data-stu-id="f8cb8-321">CC099</span></span></td>
<td><span data-ttu-id="f8cb8-322">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="f8cb8-322">Default cost center</span></span></td>
<td><span data-ttu-id="f8cb8-323">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-323">10001</span></span></td>
<td><span data-ttu-id="f8cb8-324">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-324">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-325">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-325">Fixed cost</span></span></td>
<td><span data-ttu-id="f8cb8-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-326">-1,000.00</span></span></td>
<td><span data-ttu-id="f8cb8-327">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-328">CC001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-328">CC001</span></span></td>
<td><span data-ttu-id="f8cb8-329">HR</span><span class="sxs-lookup"><span data-stu-id="f8cb8-329">HR</span></span></td>
<td><span data-ttu-id="f8cb8-330">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-330">10001</span></span></td>
<td><span data-ttu-id="f8cb8-331">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-331">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-332">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-332">Fixed cost</span></span></td>
<td><span data-ttu-id="f8cb8-333">500.00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-333">500.00</span></span></td>
<td><span data-ttu-id="f8cb8-334">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-335">CC002</span><span class="sxs-lookup"><span data-stu-id="f8cb8-335">CC002</span></span></td>
<td><span data-ttu-id="f8cb8-336">Finance</span><span class="sxs-lookup"><span data-stu-id="f8cb8-336">Finance</span></span></td>
<td><span data-ttu-id="f8cb8-337">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-337">10001</span></span></td>
<td><span data-ttu-id="f8cb8-338">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-338">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-339">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-339">Fixed cost</span></span></td>
<td><span data-ttu-id="f8cb8-340">500.00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-340">500.00</span></span></td>
<td><span data-ttu-id="f8cb8-341">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-342">CC099</span><span class="sxs-lookup"><span data-stu-id="f8cb8-342">CC099</span></span></td>
<td><span data-ttu-id="f8cb8-343">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="f8cb8-343">Default cost center</span></span></td>
<td><span data-ttu-id="f8cb8-344">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-344">10001</span></span></td>
<td><span data-ttu-id="f8cb8-345">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-345">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-346">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-346">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-347">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-347">-9,000.00</span></span></td>
<td><span data-ttu-id="f8cb8-348">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-349">CC001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-349">CC001</span></span></td>
<td><span data-ttu-id="f8cb8-350">HR</span><span class="sxs-lookup"><span data-stu-id="f8cb8-350">HR</span></span></td>
<td><span data-ttu-id="f8cb8-351">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-351">10001</span></span></td>
<td><span data-ttu-id="f8cb8-352">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-352">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-353">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-353">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="f8cb8-354">1,285.71</span></span></td>
<td><span data-ttu-id="f8cb8-355">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-356">CC002</span><span class="sxs-lookup"><span data-stu-id="f8cb8-356">CC002</span></span></td>
<td><span data-ttu-id="f8cb8-357">Finance</span><span class="sxs-lookup"><span data-stu-id="f8cb8-357">Finance</span></span></td>
<td><span data-ttu-id="f8cb8-358">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-358">10001</span></span></td>
<td><span data-ttu-id="f8cb8-359">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-359">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-360">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-360">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="f8cb8-361">7,714.29</span></span></td>
<td><span data-ttu-id="f8cb8-362">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f8cb8-363">Více informací naleznete v tématu [Vytvoření a přiřazení zásad distribuce nákladů k jednotce řízení nákladů](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="f8cb8-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="f8cb8-364">Krok 3: Zpracování výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="f8cb8-365">Režijní náklady se používají k účtování jednoho nebo více konkrétních objektů nákladů.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="f8cb8-366">Účtování je založeno na předem určené nákladové sazbě a množství z přiřazeného základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="f8cb8-367">Definice sazby režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-367">Define the overhead rate</span></span>

<span data-ttu-id="f8cb8-368">Objekt nákladů CC001 HR přispívá k sadě interních projektů.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="f8cb8-369">Vytvoří se člen statistické dimenzi s názvem projekty lidských zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f8cb8-370">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-370">Cost object</span></span></th>
<th><span data-ttu-id="f8cb8-371">Pracovní doba</span><span class="sxs-lookup"><span data-stu-id="f8cb8-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8cb8-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-372">Proj 1</span></span></td>
<td><span data-ttu-id="f8cb8-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-373">Project 1</span></span></td>
<td><span data-ttu-id="f8cb8-374">3</span><span class="sxs-lookup"><span data-stu-id="f8cb8-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-375">Proj 2</span></span></td>
<td><span data-ttu-id="f8cb8-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-376">Project 2</span></span></td>
<td><span data-ttu-id="f8cb8-377">1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f8cb8-378">Byla definována předem určená nákladová sazba pro příspěvky k nákladovým projektům.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f8cb8-379">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-379">Cost object</span></span></th>
<th><span data-ttu-id="f8cb8-380">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-380">Cost element</span></span></th>
<th><span data-ttu-id="f8cb8-381">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-381">Cost behavior</span></span></th>
<th><span data-ttu-id="f8cb8-382">Jednotky</span><span class="sxs-lookup"><span data-stu-id="f8cb8-382">Units</span></span></th>
<th><span data-ttu-id="f8cb8-383">Kurz</span><span class="sxs-lookup"><span data-stu-id="f8cb8-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8cb8-384">CC001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-384">CC001</span></span></td>
<td><span data-ttu-id="f8cb8-385">HR</span><span class="sxs-lookup"><span data-stu-id="f8cb8-385">HR</span></span></td>
<td><span data-ttu-id="f8cb8-386">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-386">10001</span></span></td>
<td><span data-ttu-id="f8cb8-387">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-387">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-388">1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-388">1</span></span></td>
<td><span data-ttu-id="f8cb8-389">10</span><span class="sxs-lookup"><span data-stu-id="f8cb8-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f8cb8-390">Následující tabulka zobrazuje výsledek při použití projektů lidských zdrojů jako základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f8cb8-391">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-391">Cost object</span></span></th>
<th><span data-ttu-id="f8cb8-392">Hodnota</span><span class="sxs-lookup"><span data-stu-id="f8cb8-392">Magnitude</span></span></th>
<th><span data-ttu-id="f8cb8-393">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-393">Cost element</span></span></th>
<th><span data-ttu-id="f8cb8-394">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-394">Allocation factor</span></span></th>
<th><span data-ttu-id="f8cb8-395">Částka</span><span class="sxs-lookup"><span data-stu-id="f8cb8-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8cb8-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-396">Proj 1</span></span></td>
<td><span data-ttu-id="f8cb8-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-397">Project 1</span></span></td>
<td><span data-ttu-id="f8cb8-398">3</span><span class="sxs-lookup"><span data-stu-id="f8cb8-398">3</span></span></td>
<td><span data-ttu-id="f8cb8-399">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-399">10001</span></span></td>
<td><span data-ttu-id="f8cb8-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="f8cb8-401">30.00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-402">Proj 2</span></span></td>
<td><span data-ttu-id="f8cb8-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-403">Project 2</span></span></td>
<td><span data-ttu-id="f8cb8-404">1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-404">1</span></span></td>
<td><span data-ttu-id="f8cb8-405">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-405">10001</span></span></td>
<td><span data-ttu-id="f8cb8-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="f8cb8-407">10,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="f8cb8-408">Deník</span><span class="sxs-lookup"><span data-stu-id="f8cb8-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f8cb8-409">Deník</span><span class="sxs-lookup"><span data-stu-id="f8cb8-409">Journal</span></span></th>
<th><span data-ttu-id="f8cb8-410">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="f8cb8-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="f8cb8-411">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="f8cb8-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="f8cb8-412">Verze</span><span class="sxs-lookup"><span data-stu-id="f8cb8-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8cb8-413">00003</span><span class="sxs-lookup"><span data-stu-id="f8cb8-413">00003</span></span></td>
<td><span data-ttu-id="f8cb8-414">Deník výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="f8cb8-415">Fiskální</span><span class="sxs-lookup"><span data-stu-id="f8cb8-415">Fiscal</span></span></td>
<td><span data-ttu-id="f8cb8-416">2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-416">2017</span></span></td>
<td><span data-ttu-id="f8cb8-417">Období 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-417">Period 1</span></span></td>
<td><span data-ttu-id="f8cb8-418">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="f8cb8-419">Položky deníku (položky deníku pro výpočet sazby režijních nákladů)</span><span class="sxs-lookup"><span data-stu-id="f8cb8-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f8cb8-420">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="f8cb8-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="f8cb8-421">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-421">Cost object</span></span></th>
<th><span data-ttu-id="f8cb8-422">Hodnota</span><span class="sxs-lookup"><span data-stu-id="f8cb8-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8cb8-423">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="f8cb8-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-424">Proj 1</span></span></td>
<td><span data-ttu-id="f8cb8-425">Interní projekt 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="f8cb8-426">3,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-427">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="f8cb8-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-428">Proj 2</span></span></td>
<td><span data-ttu-id="f8cb8-429">Interní projekt 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="f8cb8-430">1.00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="f8cb8-431">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f8cb8-432">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f8cb8-433">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-433">Cost element</span></span></th>
<th><span data-ttu-id="f8cb8-434">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-434">Cost behavior</span></span></th>
<th><span data-ttu-id="f8cb8-435">Částka</span><span class="sxs-lookup"><span data-stu-id="f8cb8-435">Amount</span></span></th>
<th><span data-ttu-id="f8cb8-436">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="f8cb8-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8cb8-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-437">CC0001</span></span></td>
<td><span data-ttu-id="f8cb8-438">HR</span><span class="sxs-lookup"><span data-stu-id="f8cb8-438">HR</span></span></td>
<td><span data-ttu-id="f8cb8-439">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-439">10001</span></span></td>
<td><span data-ttu-id="f8cb8-440">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-440">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-441">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-441">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-442">-30.00</span></span></td>
<td><span data-ttu-id="f8cb8-443">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-444">Proj 1</span></span></td>
<td><span data-ttu-id="f8cb8-445">Interní projekt 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="f8cb8-446">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-446">10001</span></span></td>
<td><span data-ttu-id="f8cb8-447">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-447">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-448">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-448">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-449">30.00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-449">30.00</span></span></td>
<td><span data-ttu-id="f8cb8-450">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-451">CC001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-451">CC001</span></span></td>
<td><span data-ttu-id="f8cb8-452">HR</span><span class="sxs-lookup"><span data-stu-id="f8cb8-452">HR</span></span></td>
<td><span data-ttu-id="f8cb8-453">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-453">10001</span></span></td>
<td><span data-ttu-id="f8cb8-454">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-454">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-455">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-455">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-456">-10.00</span></span></td>
<td><span data-ttu-id="f8cb8-457">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-458">Proj 2</span></span></td>
<td><span data-ttu-id="f8cb8-459">Interní projekt 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="f8cb8-460">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-460">10001</span></span></td>
<td><span data-ttu-id="f8cb8-461">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-461">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-462">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-462">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-463">10.00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-463">10.00</span></span></td>
<td><span data-ttu-id="f8cb8-464">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f8cb8-465">Další informace naleznete v tématu [Provedení výpočtu režijních nákladů](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="f8cb8-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="f8cb8-466">Krok 4: Zpracování výpočtu přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="f8cb8-467">Přidělení se používá k přidělení zůstatku objektu nákladů do jiných objektů nákladů použitím základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="f8cb8-468">Aplikace Finance podporuje reciproční metodu přidělování.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="f8cb8-469">V metodě vzájemného přidělení jsou plně rozpoznány vzájemné služby, které si vyměňují pomocné objekty nákladů.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="f8cb8-470">Systém automaticky určí provádění přidělení ve správném pořadí.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="f8cb8-471">Zůstatek objektu nákladů je přidělen jedním základem přidělení.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="f8cb8-472">Je podporováno přidělování napříč dimenzemi objektů nákladů a jejich příslušných členů.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="f8cb8-473">Pořadí přidělení je řízeno jednotkou řízení nákladů.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="f8cb8-474">[![Reciproční metoda](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="f8cb8-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="f8cb8-475">Definice přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-475">Define the cost allocation</span></span>

<span data-ttu-id="f8cb8-476">Toto je jednoduchý příklad, který vysvětluje, jakým způsobem lze sledovat tok nákladů.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="f8cb8-477">Objekt nákladů objektu CC001 HR přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="f8cb8-478">Vytvoří se člen statistické dimenzi s názvem služby lidských zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f8cb8-479">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-479">Cost object</span></span></th>
<th><span data-ttu-id="f8cb8-480">Služby HR</span><span class="sxs-lookup"><span data-stu-id="f8cb8-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8cb8-481">CC002</span><span class="sxs-lookup"><span data-stu-id="f8cb8-481">CC002</span></span></td>
<td><span data-ttu-id="f8cb8-482">Finance</span><span class="sxs-lookup"><span data-stu-id="f8cb8-482">Finance</span></span></td>
<td><span data-ttu-id="f8cb8-483">35</span><span class="sxs-lookup"><span data-stu-id="f8cb8-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-484">CC003</span><span class="sxs-lookup"><span data-stu-id="f8cb8-484">CC003</span></span></td>
<td><span data-ttu-id="f8cb8-485">Sestavení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-485">Assembly</span></span></td>
<td><span data-ttu-id="f8cb8-486">55</span><span class="sxs-lookup"><span data-stu-id="f8cb8-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-487">CC004</span><span class="sxs-lookup"><span data-stu-id="f8cb8-487">CC004</span></span></td>
<td><span data-ttu-id="f8cb8-488">Balení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-488">Packaging</span></span></td>
<td><span data-ttu-id="f8cb8-489">10</span><span class="sxs-lookup"><span data-stu-id="f8cb8-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f8cb8-490">Objekt nákladů objektu CC002 Finance přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="f8cb8-491">Vytvoří se člen statistické dimenzi s názvem Finanční služby k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f8cb8-492">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-492">Cost object</span></span></th>
<th><span data-ttu-id="f8cb8-493">Finanční služby</span><span class="sxs-lookup"><span data-stu-id="f8cb8-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8cb8-494">CC003</span><span class="sxs-lookup"><span data-stu-id="f8cb8-494">CC003</span></span></td>
<td><span data-ttu-id="f8cb8-495">Sestavení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-495">Assembly</span></span></td>
<td><span data-ttu-id="f8cb8-496">65</span><span class="sxs-lookup"><span data-stu-id="f8cb8-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-497">CC004</span><span class="sxs-lookup"><span data-stu-id="f8cb8-497">CC004</span></span></td>
<td><span data-ttu-id="f8cb8-498">Balení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-498">Packaging</span></span></td>
<td><span data-ttu-id="f8cb8-499">35</span><span class="sxs-lookup"><span data-stu-id="f8cb8-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f8cb8-500">Objekt nákladů objektu CC003 Sestavení přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="f8cb8-501">Vytvoří se člen statistické dimenzi s názvem Služby sestavení zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f8cb8-502">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-502">Cost object</span></span></th>
<th><span data-ttu-id="f8cb8-503">Služby sestavení (v hodinách)</span><span class="sxs-lookup"><span data-stu-id="f8cb8-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8cb8-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-504">Prod 1</span></span></td>
<td><span data-ttu-id="f8cb8-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-505">Product 1</span></span></td>
<td><span data-ttu-id="f8cb8-506">60</span><span class="sxs-lookup"><span data-stu-id="f8cb8-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-507">Prod 2</span></span></td>
<td><span data-ttu-id="f8cb8-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-508">Product 2</span></span></td>
<td><span data-ttu-id="f8cb8-509">20</span><span class="sxs-lookup"><span data-stu-id="f8cb8-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f8cb8-510">Objekt nákladů objektu CC004 Balení přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="f8cb8-511">Vytvoří se člen statistické dimenzi s názvem Služby balení k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f8cb8-512">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-512">Cost object</span></span></th>
<th><span data-ttu-id="f8cb8-513">Služby balení (v hodinách)</span><span class="sxs-lookup"><span data-stu-id="f8cb8-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8cb8-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-514">Prod 1</span></span></td>
<td><span data-ttu-id="f8cb8-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-515">Product 1</span></span></td>
<td><span data-ttu-id="f8cb8-516">80</span><span class="sxs-lookup"><span data-stu-id="f8cb8-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-517">Prod 2</span></span></td>
<td><span data-ttu-id="f8cb8-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-518">Product 2</span></span></td>
<td><span data-ttu-id="f8cb8-519">15</span><span class="sxs-lookup"><span data-stu-id="f8cb8-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="f8cb8-520">Statistická měření, jako je například výrobní doba spotřebovaná produktem, lze odvodit z datového zdroje.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="f8cb8-521">Více informací naleznete v části [Šablona poskytovatele statistického měření](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="f8cb8-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="f8cb8-522">V následující tabulce je uveden výsledek při použití služeb HR jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="f8cb8-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f8cb8-523">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-523">Cost object</span></span></th>
<th><span data-ttu-id="f8cb8-524">Hodnota</span><span class="sxs-lookup"><span data-stu-id="f8cb8-524">Magnitude</span></span></th>
<th><span data-ttu-id="f8cb8-525">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-525">Allocation factor</span></span></th>
<th><span data-ttu-id="f8cb8-526">Částka</span><span class="sxs-lookup"><span data-stu-id="f8cb8-526">Amount</span></span></th>
<th><span data-ttu-id="f8cb8-527">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8cb8-528">CC002</span><span class="sxs-lookup"><span data-stu-id="f8cb8-528">CC002</span></span></td>
<td><span data-ttu-id="f8cb8-529">Finance</span><span class="sxs-lookup"><span data-stu-id="f8cb8-529">Finance</span></span></td>
<td><span data-ttu-id="f8cb8-530">35</span><span class="sxs-lookup"><span data-stu-id="f8cb8-530">35</span></span></td>
<td><span data-ttu-id="f8cb8-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="f8cb8-532">175.00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-532">175.00</span></span></td>
<td><span data-ttu-id="f8cb8-533">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-534">CC003</span><span class="sxs-lookup"><span data-stu-id="f8cb8-534">CC003</span></span></td>
<td><span data-ttu-id="f8cb8-535">Sestavení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-535">Assembly</span></span></td>
<td><span data-ttu-id="f8cb8-536">55</span><span class="sxs-lookup"><span data-stu-id="f8cb8-536">55</span></span></td>
<td><span data-ttu-id="f8cb8-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="f8cb8-538">275.00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-538">275.00</span></span></td>
<td><span data-ttu-id="f8cb8-539">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-540">CC004</span><span class="sxs-lookup"><span data-stu-id="f8cb8-540">CC004</span></span></td>
<td><span data-ttu-id="f8cb8-541">Balení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-541">Packaging</span></span></td>
<td><span data-ttu-id="f8cb8-542">10</span><span class="sxs-lookup"><span data-stu-id="f8cb8-542">10</span></span></td>
<td><span data-ttu-id="f8cb8-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="f8cb8-544">50,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-544">50.00</span></span></td>
<td><span data-ttu-id="f8cb8-545">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-546">CC002</span><span class="sxs-lookup"><span data-stu-id="f8cb8-546">CC002</span></span></td>
<td><span data-ttu-id="f8cb8-547">Finance</span><span class="sxs-lookup"><span data-stu-id="f8cb8-547">Finance</span></span></td>
<td><span data-ttu-id="f8cb8-548">35</span><span class="sxs-lookup"><span data-stu-id="f8cb8-548">35</span></span></td>
<td><span data-ttu-id="f8cb8-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="f8cb8-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="f8cb8-550">436.00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-550">436.00</span></span></td>
<td><span data-ttu-id="f8cb8-551">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-552">CC003</span><span class="sxs-lookup"><span data-stu-id="f8cb8-552">CC003</span></span></td>
<td><span data-ttu-id="f8cb8-553">Sestavení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-553">Assembly</span></span></td>
<td><span data-ttu-id="f8cb8-554">55</span><span class="sxs-lookup"><span data-stu-id="f8cb8-554">55</span></span></td>
<td><span data-ttu-id="f8cb8-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="f8cb8-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="f8cb8-556">685.14</span><span class="sxs-lookup"><span data-stu-id="f8cb8-556">685.14</span></span></td>
<td><span data-ttu-id="f8cb8-557">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-558">CC004</span><span class="sxs-lookup"><span data-stu-id="f8cb8-558">CC004</span></span></td>
<td><span data-ttu-id="f8cb8-559">Balení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-559">Packaging</span></span></td>
<td><span data-ttu-id="f8cb8-560">10</span><span class="sxs-lookup"><span data-stu-id="f8cb8-560">10</span></span></td>
<td><span data-ttu-id="f8cb8-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="f8cb8-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="f8cb8-562">124.57</span><span class="sxs-lookup"><span data-stu-id="f8cb8-562">124.57</span></span></td>
<td><span data-ttu-id="f8cb8-563">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f8cb8-564">V následující tabulce je uveden výsledek při použití Finančních služeb Finance jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="f8cb8-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f8cb8-565">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-565">Cost object</span></span></th>
<th><span data-ttu-id="f8cb8-566">Hodnota</span><span class="sxs-lookup"><span data-stu-id="f8cb8-566">Magnitude</span></span></th>
<th><span data-ttu-id="f8cb8-567">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-567">Allocation factor</span></span></th>
<th><span data-ttu-id="f8cb8-568">Částka</span><span class="sxs-lookup"><span data-stu-id="f8cb8-568">Amount</span></span></th>
<th><span data-ttu-id="f8cb8-569">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8cb8-570">CC003</span><span class="sxs-lookup"><span data-stu-id="f8cb8-570">CC003</span></span></td>
<td><span data-ttu-id="f8cb8-571">Sestavení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-571">Assembly</span></span></td>
<td><span data-ttu-id="f8cb8-572">65</span><span class="sxs-lookup"><span data-stu-id="f8cb8-572">65</span></span></td>
<td><span data-ttu-id="f8cb8-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="f8cb8-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="f8cb8-574">438.75</span><span class="sxs-lookup"><span data-stu-id="f8cb8-574">438.75</span></span></td>
<td><span data-ttu-id="f8cb8-575">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-576">CC004</span><span class="sxs-lookup"><span data-stu-id="f8cb8-576">CC004</span></span></td>
<td><span data-ttu-id="f8cb8-577">Balení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-577">Packaging</span></span></td>
<td><span data-ttu-id="f8cb8-578">35</span><span class="sxs-lookup"><span data-stu-id="f8cb8-578">35</span></span></td>
<td><span data-ttu-id="f8cb8-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="f8cb8-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="f8cb8-580">236.25</span><span class="sxs-lookup"><span data-stu-id="f8cb8-580">236.25</span></span></td>
<td><span data-ttu-id="f8cb8-581">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-582">CC003</span><span class="sxs-lookup"><span data-stu-id="f8cb8-582">CC003</span></span></td>
<td><span data-ttu-id="f8cb8-583">Sestavení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-583">Assembly</span></span></td>
<td><span data-ttu-id="f8cb8-584">65</span><span class="sxs-lookup"><span data-stu-id="f8cb8-584">65</span></span></td>
<td><span data-ttu-id="f8cb8-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="f8cb8-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="f8cb8-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="f8cb8-586">5,297.69</span></span></td>
<td><span data-ttu-id="f8cb8-587">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-588">CC004</span><span class="sxs-lookup"><span data-stu-id="f8cb8-588">CC004</span></span></td>
<td><span data-ttu-id="f8cb8-589">Balení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-589">Packaging</span></span></td>
<td><span data-ttu-id="f8cb8-590">35</span><span class="sxs-lookup"><span data-stu-id="f8cb8-590">35</span></span></td>
<td><span data-ttu-id="f8cb8-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="f8cb8-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="f8cb8-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="f8cb8-592">2,852.60</span></span></td>
<td><span data-ttu-id="f8cb8-593">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f8cb8-594">V následující tabulce je uveden výsledek při použití Služeb sestavení jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="f8cb8-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f8cb8-595">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-595">Cost object</span></span></th>
<th><span data-ttu-id="f8cb8-596">Hodnota</span><span class="sxs-lookup"><span data-stu-id="f8cb8-596">Magnitude</span></span></th>
<th><span data-ttu-id="f8cb8-597">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-597">Allocation factor</span></span></th>
<th><span data-ttu-id="f8cb8-598">Částka</span><span class="sxs-lookup"><span data-stu-id="f8cb8-598">Amount</span></span></th>
<th><span data-ttu-id="f8cb8-599">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8cb8-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-600">Prod 1</span></span></td>
<td><span data-ttu-id="f8cb8-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-601">Product 1</span></span></td>
<td><span data-ttu-id="f8cb8-602">60</span><span class="sxs-lookup"><span data-stu-id="f8cb8-602">60</span></span></td>
<td><span data-ttu-id="f8cb8-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="f8cb8-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="f8cb8-604">535.31</span><span class="sxs-lookup"><span data-stu-id="f8cb8-604">535.31</span></span></td>
<td><span data-ttu-id="f8cb8-605">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-606">Prod 2</span></span></td>
<td><span data-ttu-id="f8cb8-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-607">Product 2</span></span></td>
<td><span data-ttu-id="f8cb8-608">20</span><span class="sxs-lookup"><span data-stu-id="f8cb8-608">20</span></span></td>
<td><span data-ttu-id="f8cb8-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="f8cb8-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="f8cb8-610">178.44</span><span class="sxs-lookup"><span data-stu-id="f8cb8-610">178.44</span></span></td>
<td><span data-ttu-id="f8cb8-611">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-612">Prod 1</span></span></td>
<td><span data-ttu-id="f8cb8-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-613">Product 1</span></span></td>
<td><span data-ttu-id="f8cb8-614">60</span><span class="sxs-lookup"><span data-stu-id="f8cb8-614">60</span></span></td>
<td><span data-ttu-id="f8cb8-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="f8cb8-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="f8cb8-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="f8cb8-616">4,487.12</span></span></td>
<td><span data-ttu-id="f8cb8-617">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-618">Prod 2</span></span></td>
<td><span data-ttu-id="f8cb8-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-619">Product 2</span></span></td>
<td><span data-ttu-id="f8cb8-620">20</span><span class="sxs-lookup"><span data-stu-id="f8cb8-620">20</span></span></td>
<td><span data-ttu-id="f8cb8-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="f8cb8-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="f8cb8-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="f8cb8-622">1,495.71</span></span></td>
<td><span data-ttu-id="f8cb8-623">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f8cb8-624">V následující tabulce je uveden výsledek při použití Služeb balení jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="f8cb8-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f8cb8-625">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-625">Cost object</span></span></th>
<th><span data-ttu-id="f8cb8-626">Hodnota</span><span class="sxs-lookup"><span data-stu-id="f8cb8-626">Magnitude</span></span></th>
<th><span data-ttu-id="f8cb8-627">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-627">Allocation factor</span></span></th>
<th><span data-ttu-id="f8cb8-628">Částka</span><span class="sxs-lookup"><span data-stu-id="f8cb8-628">Amount</span></span></th>
<th><span data-ttu-id="f8cb8-629">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8cb8-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-630">Prod 1</span></span></td>
<td><span data-ttu-id="f8cb8-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-631">Product 1</span></span></td>
<td><span data-ttu-id="f8cb8-632">80</span><span class="sxs-lookup"><span data-stu-id="f8cb8-632">80</span></span></td>
<td><span data-ttu-id="f8cb8-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="f8cb8-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="f8cb8-634">241.05</span><span class="sxs-lookup"><span data-stu-id="f8cb8-634">241.05</span></span></td>
<td><span data-ttu-id="f8cb8-635">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-636">Prod 2</span></span></td>
<td><span data-ttu-id="f8cb8-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-637">Product 2</span></span></td>
<td><span data-ttu-id="f8cb8-638">15</span><span class="sxs-lookup"><span data-stu-id="f8cb8-638">15</span></span></td>
<td><span data-ttu-id="f8cb8-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="f8cb8-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="f8cb8-640">45.20</span><span class="sxs-lookup"><span data-stu-id="f8cb8-640">45.20</span></span></td>
<td><span data-ttu-id="f8cb8-641">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-642">Prod 1</span></span></td>
<td><span data-ttu-id="f8cb8-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-643">Product 1</span></span></td>
<td><span data-ttu-id="f8cb8-644">80</span><span class="sxs-lookup"><span data-stu-id="f8cb8-644">80</span></span></td>
<td><span data-ttu-id="f8cb8-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="f8cb8-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="f8cb8-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="f8cb8-646">2,507.09</span></span></td>
<td><span data-ttu-id="f8cb8-647">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-648">Prod 2</span></span></td>
<td><span data-ttu-id="f8cb8-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-649">Product 2</span></span></td>
<td><span data-ttu-id="f8cb8-650">15</span><span class="sxs-lookup"><span data-stu-id="f8cb8-650">15</span></span></td>
<td><span data-ttu-id="f8cb8-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="f8cb8-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="f8cb8-652">470.08</span><span class="sxs-lookup"><span data-stu-id="f8cb8-652">470.08</span></span></td>
<td><span data-ttu-id="f8cb8-653">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="f8cb8-654">Položky deníku (položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="f8cb8-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f8cb8-655">Deník</span><span class="sxs-lookup"><span data-stu-id="f8cb8-655">Journal</span></span></th>
<th><span data-ttu-id="f8cb8-656">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="f8cb8-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="f8cb8-657">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="f8cb8-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="f8cb8-658">Verze</span><span class="sxs-lookup"><span data-stu-id="f8cb8-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8cb8-659">00004</span><span class="sxs-lookup"><span data-stu-id="f8cb8-659">00004</span></span></td>
<td><span data-ttu-id="f8cb8-660">Deník přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="f8cb8-661">Fiskální</span><span class="sxs-lookup"><span data-stu-id="f8cb8-661">Fiscal</span></span></td>
<td><span data-ttu-id="f8cb8-662">2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-662">2017</span></span></td>
<td><span data-ttu-id="f8cb8-663">Období 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-663">Period 1</span></span></td>
<td><span data-ttu-id="f8cb8-664">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="f8cb8-665">Řádky deníku</span><span class="sxs-lookup"><span data-stu-id="f8cb8-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f8cb8-666">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="f8cb8-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="f8cb8-667">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f8cb8-668">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-668">Cost element</span></span></th>
<th><span data-ttu-id="f8cb8-669">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-669">Cost behavior</span></span></th>
<th><span data-ttu-id="f8cb8-670">Částka</span><span class="sxs-lookup"><span data-stu-id="f8cb8-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8cb8-671">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="f8cb8-672">CC001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-672">CC001</span></span></td>
<td><span data-ttu-id="f8cb8-673">HR</span><span class="sxs-lookup"><span data-stu-id="f8cb8-673">HR</span></span></td>
<td><span data-ttu-id="f8cb8-674">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-674">10001</span></span></td>
<td><span data-ttu-id="f8cb8-675">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-675">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-676">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-676">Fixed cost</span></span></td>
<td><span data-ttu-id="f8cb8-677">500.00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-678">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="f8cb8-679">CC001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-679">CC001</span></span></td>
<td><span data-ttu-id="f8cb8-680">HR</span><span class="sxs-lookup"><span data-stu-id="f8cb8-680">HR</span></span></td>
<td><span data-ttu-id="f8cb8-681">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-681">10001</span></span></td>
<td><span data-ttu-id="f8cb8-682">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-682">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-683">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-683">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="f8cb8-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-685">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="f8cb8-686">CC002</span><span class="sxs-lookup"><span data-stu-id="f8cb8-686">CC002</span></span></td>
<td><span data-ttu-id="f8cb8-687">Finance</span><span class="sxs-lookup"><span data-stu-id="f8cb8-687">Finance</span></span></td>
<td><span data-ttu-id="f8cb8-688">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-688">10001</span></span></td>
<td><span data-ttu-id="f8cb8-689">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-689">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-690">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-690">Fixed cost</span></span></td>
<td><span data-ttu-id="f8cb8-691">675.00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-692">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="f8cb8-693">CC002</span><span class="sxs-lookup"><span data-stu-id="f8cb8-693">CC002</span></span></td>
<td><span data-ttu-id="f8cb8-694">Finance</span><span class="sxs-lookup"><span data-stu-id="f8cb8-694">Finance</span></span></td>
<td><span data-ttu-id="f8cb8-695">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-695">10001</span></span></td>
<td><span data-ttu-id="f8cb8-696">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-696">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-697">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-697">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="f8cb8-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-699">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="f8cb8-700">CC003</span><span class="sxs-lookup"><span data-stu-id="f8cb8-700">CC003</span></span></td>
<td><span data-ttu-id="f8cb8-701">Sestavení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-701">Assembly</span></span></td>
<td><span data-ttu-id="f8cb8-702">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-702">10001</span></span></td>
<td><span data-ttu-id="f8cb8-703">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-703">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-704">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-704">Fixed cost</span></span></td>
<td><span data-ttu-id="f8cb8-705">713.75</span><span class="sxs-lookup"><span data-stu-id="f8cb8-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-706">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="f8cb8-707">CC003</span><span class="sxs-lookup"><span data-stu-id="f8cb8-707">CC003</span></span></td>
<td><span data-ttu-id="f8cb8-708">Sestavení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-708">Assembly</span></span></td>
<td><span data-ttu-id="f8cb8-709">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-709">10001</span></span></td>
<td><span data-ttu-id="f8cb8-710">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-710">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-711">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-711">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="f8cb8-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-713">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="f8cb8-714">CC003</span><span class="sxs-lookup"><span data-stu-id="f8cb8-714">CC003</span></span></td>
<td><span data-ttu-id="f8cb8-715">Balení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-715">Packaging</span></span></td>
<td><span data-ttu-id="f8cb8-716">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-716">10001</span></span></td>
<td><span data-ttu-id="f8cb8-717">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-717">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-718">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-718">Fixed cost</span></span></td>
<td><span data-ttu-id="f8cb8-719">286.25</span><span class="sxs-lookup"><span data-stu-id="f8cb8-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-720">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="f8cb8-721">CC003</span><span class="sxs-lookup"><span data-stu-id="f8cb8-721">CC003</span></span></td>
<td><span data-ttu-id="f8cb8-722">Balení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-722">Packaging</span></span></td>
<td><span data-ttu-id="f8cb8-723">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-723">10001</span></span></td>
<td><span data-ttu-id="f8cb8-724">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-724">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-725">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-725">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="f8cb8-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-727">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="f8cb8-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-728">Prod 1</span></span></td>
<td><span data-ttu-id="f8cb8-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-729">Product 1</span></span></td>
<td><span data-ttu-id="f8cb8-730">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-730">10001</span></span></td>
<td><span data-ttu-id="f8cb8-731">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-731">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-732">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-732">Fixed cost</span></span></td>
<td><span data-ttu-id="f8cb8-733">776.36</span><span class="sxs-lookup"><span data-stu-id="f8cb8-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-734">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="f8cb8-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-735">Prod 1</span></span></td>
<td><span data-ttu-id="f8cb8-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-736">Product 1</span></span></td>
<td><span data-ttu-id="f8cb8-737">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-737">10001</span></span></td>
<td><span data-ttu-id="f8cb8-738">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-738">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-739">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-739">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="f8cb8-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-741">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="f8cb8-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-742">Prod 2</span></span></td>
<td><span data-ttu-id="f8cb8-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-743">Product 1</span></span></td>
<td><span data-ttu-id="f8cb8-744">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-744">10001</span></span></td>
<td><span data-ttu-id="f8cb8-745">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-745">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-746">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-746">Fixed cost</span></span></td>
<td><span data-ttu-id="f8cb8-747">223.64</span><span class="sxs-lookup"><span data-stu-id="f8cb8-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-748">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="f8cb8-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-749">Prod 2</span></span></td>
<td><span data-ttu-id="f8cb8-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-750">Product 1</span></span></td>
<td><span data-ttu-id="f8cb8-751">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-751">10001</span></span></td>
<td><span data-ttu-id="f8cb8-752">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-752">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-753">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-753">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="f8cb8-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="f8cb8-755">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f8cb8-756">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f8cb8-757">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-757">Cost element</span></span></th>
<th><span data-ttu-id="f8cb8-758">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-758">Cost behavior</span></span></th>
<th><span data-ttu-id="f8cb8-759">Částka</span><span class="sxs-lookup"><span data-stu-id="f8cb8-759">Amount</span></span></th>
<th><span data-ttu-id="f8cb8-760">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="f8cb8-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8cb8-761">CC001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-761">CC001</span></span></td>
<td><span data-ttu-id="f8cb8-762">HR</span><span class="sxs-lookup"><span data-stu-id="f8cb8-762">HR</span></span></td>
<td><span data-ttu-id="f8cb8-763">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-763">10001</span></span></td>
<td><span data-ttu-id="f8cb8-764">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-764">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-765">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-765">Fixed cost</span></span></td>
<td><span data-ttu-id="f8cb8-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-766">-500.00</span></span></td>
<td><span data-ttu-id="f8cb8-767">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-768">CC002</span><span class="sxs-lookup"><span data-stu-id="f8cb8-768">CC002</span></span></td>
<td><span data-ttu-id="f8cb8-769">Finance</span><span class="sxs-lookup"><span data-stu-id="f8cb8-769">Finance</span></span></td>
<td><span data-ttu-id="f8cb8-770">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-770">10001</span></span></td>
<td><span data-ttu-id="f8cb8-771">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-771">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-772">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-772">Fixed cost</span></span></td>
<td><span data-ttu-id="f8cb8-773">175.00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-773">175.00</span></span></td>
<td><span data-ttu-id="f8cb8-774">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-775">CC003</span><span class="sxs-lookup"><span data-stu-id="f8cb8-775">CC003</span></span></td>
<td><span data-ttu-id="f8cb8-776">Sestavení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-776">Assembly</span></span></td>
<td><span data-ttu-id="f8cb8-777">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-777">10001</span></span></td>
<td><span data-ttu-id="f8cb8-778">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-778">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-779">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-779">Fixed cost</span></span></td>
<td><span data-ttu-id="f8cb8-780">275.00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-780">275.00</span></span></td>
<td><span data-ttu-id="f8cb8-781">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-782">CC004</span><span class="sxs-lookup"><span data-stu-id="f8cb8-782">CC004</span></span></td>
<td><span data-ttu-id="f8cb8-783">Balení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-783">Packaging</span></span></td>
<td><span data-ttu-id="f8cb8-784">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-784">10001</span></span></td>
<td><span data-ttu-id="f8cb8-785">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-785">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-786">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-786">Fixed cost</span></span></td>
<td><span data-ttu-id="f8cb8-787">50,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-787">50,00</span></span></td>
<td><span data-ttu-id="f8cb8-788">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-789">CC001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-789">CC001</span></span></td>
<td><span data-ttu-id="f8cb8-790">HR</span><span class="sxs-lookup"><span data-stu-id="f8cb8-790">HR</span></span></td>
<td><span data-ttu-id="f8cb8-791">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-791">10001</span></span></td>
<td><span data-ttu-id="f8cb8-792">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-792">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-793">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-793">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-794">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="f8cb8-794">-1,245.71</span></span></td>
<td><span data-ttu-id="f8cb8-795">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-796">CC002</span><span class="sxs-lookup"><span data-stu-id="f8cb8-796">CC002</span></span></td>
<td><span data-ttu-id="f8cb8-797">Finance</span><span class="sxs-lookup"><span data-stu-id="f8cb8-797">Finance</span></span></td>
<td><span data-ttu-id="f8cb8-798">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-798">10001</span></span></td>
<td><span data-ttu-id="f8cb8-799">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-799">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-800">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-800">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-801">436.00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-801">436.00</span></span></td>
<td><span data-ttu-id="f8cb8-802">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-803">CC003</span><span class="sxs-lookup"><span data-stu-id="f8cb8-803">CC003</span></span></td>
<td><span data-ttu-id="f8cb8-804">Sestavení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-804">Assembly</span></span></td>
<td><span data-ttu-id="f8cb8-805">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-805">10001</span></span></td>
<td><span data-ttu-id="f8cb8-806">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-806">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-807">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-807">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-808">685.14</span><span class="sxs-lookup"><span data-stu-id="f8cb8-808">685.14</span></span></td>
<td><span data-ttu-id="f8cb8-809">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-810">CC004</span><span class="sxs-lookup"><span data-stu-id="f8cb8-810">CC004</span></span></td>
<td><span data-ttu-id="f8cb8-811">Balení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-811">Packaging</span></span></td>
<td><span data-ttu-id="f8cb8-812">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-812">10001</span></span></td>
<td><span data-ttu-id="f8cb8-813">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-813">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-814">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-814">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-815">124.57</span><span class="sxs-lookup"><span data-stu-id="f8cb8-815">124.57</span></span></td>
<td><span data-ttu-id="f8cb8-816">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-817">CC002</span><span class="sxs-lookup"><span data-stu-id="f8cb8-817">CC002</span></span></td>
<td><span data-ttu-id="f8cb8-818">Finance</span><span class="sxs-lookup"><span data-stu-id="f8cb8-818">Finance</span></span></td>
<td><span data-ttu-id="f8cb8-819">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-819">10001</span></span></td>
<td><span data-ttu-id="f8cb8-820">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-820">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-821">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-821">Fixed cost</span></span></td>
<td><span data-ttu-id="f8cb8-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-822">-675.00</span></span></td>
<td><span data-ttu-id="f8cb8-823">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-824">CC003</span><span class="sxs-lookup"><span data-stu-id="f8cb8-824">CC003</span></span></td>
<td><span data-ttu-id="f8cb8-825">Sestavení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-825">Assembly</span></span></td>
<td><span data-ttu-id="f8cb8-826">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-826">10001</span></span></td>
<td><span data-ttu-id="f8cb8-827">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-827">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-828">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-828">Fixed cost</span></span></td>
<td><span data-ttu-id="f8cb8-829">438.75</span><span class="sxs-lookup"><span data-stu-id="f8cb8-829">438.75</span></span></td>
<td><span data-ttu-id="f8cb8-830">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-831">CC004</span><span class="sxs-lookup"><span data-stu-id="f8cb8-831">CC004</span></span></td>
<td><span data-ttu-id="f8cb8-832">Balení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-832">Packaging</span></span></td>
<td><span data-ttu-id="f8cb8-833">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-833">10001</span></span></td>
<td><span data-ttu-id="f8cb8-834">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-834">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-835">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-835">Fixed cost</span></span></td>
<td><span data-ttu-id="f8cb8-836">236.25</span><span class="sxs-lookup"><span data-stu-id="f8cb8-836">236.25</span></span></td>
<td><span data-ttu-id="f8cb8-837">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-838">CC002</span><span class="sxs-lookup"><span data-stu-id="f8cb8-838">CC002</span></span></td>
<td><span data-ttu-id="f8cb8-839">Finance</span><span class="sxs-lookup"><span data-stu-id="f8cb8-839">Finance</span></span></td>
<td><span data-ttu-id="f8cb8-840">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-840">10001</span></span></td>
<td><span data-ttu-id="f8cb8-841">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-841">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-842">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-842">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-843">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="f8cb8-843">-8,150.29</span></span></td>
<td><span data-ttu-id="f8cb8-844">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-845">CC003</span><span class="sxs-lookup"><span data-stu-id="f8cb8-845">CC003</span></span></td>
<td><span data-ttu-id="f8cb8-846">Sestavení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-846">Assembly</span></span></td>
<td><span data-ttu-id="f8cb8-847">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-847">10001</span></span></td>
<td><span data-ttu-id="f8cb8-848">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-848">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-849">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-849">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="f8cb8-850">5,297.69</span></span></td>
<td><span data-ttu-id="f8cb8-851">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-852">CC004</span><span class="sxs-lookup"><span data-stu-id="f8cb8-852">CC004</span></span></td>
<td><span data-ttu-id="f8cb8-853">Balení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-853">Packaging</span></span></td>
<td><span data-ttu-id="f8cb8-854">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-854">10001</span></span></td>
<td><span data-ttu-id="f8cb8-855">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-855">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-856">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-856">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="f8cb8-857">2,852.60</span></span></td>
<td><span data-ttu-id="f8cb8-858">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-859">CC003</span><span class="sxs-lookup"><span data-stu-id="f8cb8-859">CC003</span></span></td>
<td><span data-ttu-id="f8cb8-860">Sestavení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-860">Assembly</span></span></td>
<td><span data-ttu-id="f8cb8-861">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-861">10001</span></span></td>
<td><span data-ttu-id="f8cb8-862">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-862">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-863">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-863">Fixed cost</span></span></td>
<td><span data-ttu-id="f8cb8-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="f8cb8-864">-713.75</span></span></td>
<td><span data-ttu-id="f8cb8-865">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-866">Prod 1</span></span></td>
<td><span data-ttu-id="f8cb8-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-867">Product 1</span></span></td>
<td><span data-ttu-id="f8cb8-868">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-868">10001</span></span></td>
<td><span data-ttu-id="f8cb8-869">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-869">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-870">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-870">Fixed cost</span></span></td>
<td><span data-ttu-id="f8cb8-871">535.31</span><span class="sxs-lookup"><span data-stu-id="f8cb8-871">535.31</span></span></td>
<td><span data-ttu-id="f8cb8-872">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-873">Prod 2</span></span></td>
<td><span data-ttu-id="f8cb8-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-874">Product 2</span></span></td>
<td><span data-ttu-id="f8cb8-875">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-875">10001</span></span></td>
<td><span data-ttu-id="f8cb8-876">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-876">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-877">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-877">Fixed cost</span></span></td>
<td><span data-ttu-id="f8cb8-878">178.44</span><span class="sxs-lookup"><span data-stu-id="f8cb8-878">178.44</span></span></td>
<td><span data-ttu-id="f8cb8-879">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-880">CC003</span><span class="sxs-lookup"><span data-stu-id="f8cb8-880">CC003</span></span></td>
<td><span data-ttu-id="f8cb8-881">Sestavení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-881">Assembly</span></span></td>
<td><span data-ttu-id="f8cb8-882">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-882">10001</span></span></td>
<td><span data-ttu-id="f8cb8-883">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-883">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-884">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-884">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-885">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="f8cb8-885">-5,982.83</span></span></td>
<td><span data-ttu-id="f8cb8-886">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-887">Prod 1</span></span></td>
<td><span data-ttu-id="f8cb8-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-888">Product 1</span></span></td>
<td><span data-ttu-id="f8cb8-889">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-889">10001</span></span></td>
<td><span data-ttu-id="f8cb8-890">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-890">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-891">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-891">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="f8cb8-892">4,487.12</span></span></td>
<td><span data-ttu-id="f8cb8-893">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-894">Prod 2</span></span></td>
<td><span data-ttu-id="f8cb8-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-895">Product 2</span></span></td>
<td><span data-ttu-id="f8cb8-896">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-896">10001</span></span></td>
<td><span data-ttu-id="f8cb8-897">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-897">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-898">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-898">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="f8cb8-899">1,495.71</span></span></td>
<td><span data-ttu-id="f8cb8-900">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-901">CC003</span><span class="sxs-lookup"><span data-stu-id="f8cb8-901">CC003</span></span></td>
<td><span data-ttu-id="f8cb8-902">Sestavení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-902">Assembly</span></span></td>
<td><span data-ttu-id="f8cb8-903">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-903">10001</span></span></td>
<td><span data-ttu-id="f8cb8-904">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-904">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-905">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-905">Fixed cost</span></span></td>
<td><span data-ttu-id="f8cb8-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="f8cb8-906">-286.25</span></span></td>
<td><span data-ttu-id="f8cb8-907">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-908">Prod 1</span></span></td>
<td><span data-ttu-id="f8cb8-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-909">Product 1</span></span></td>
<td><span data-ttu-id="f8cb8-910">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-910">10001</span></span></td>
<td><span data-ttu-id="f8cb8-911">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-911">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-912">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-912">Fixed cost</span></span></td>
<td><span data-ttu-id="f8cb8-913">241.05</span><span class="sxs-lookup"><span data-stu-id="f8cb8-913">241.05</span></span></td>
<td><span data-ttu-id="f8cb8-914">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-915">Prod 2</span></span></td>
<td><span data-ttu-id="f8cb8-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-916">Product 2</span></span></td>
<td><span data-ttu-id="f8cb8-917">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-917">10001</span></span></td>
<td><span data-ttu-id="f8cb8-918">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-918">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-919">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-919">Fixed cost</span></span></td>
<td><span data-ttu-id="f8cb8-920">45.20</span><span class="sxs-lookup"><span data-stu-id="f8cb8-920">45.20</span></span></td>
<td><span data-ttu-id="f8cb8-921">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-922">CC003</span><span class="sxs-lookup"><span data-stu-id="f8cb8-922">CC003</span></span></td>
<td><span data-ttu-id="f8cb8-923">Sestavení</span><span class="sxs-lookup"><span data-stu-id="f8cb8-923">Assembly</span></span></td>
<td><span data-ttu-id="f8cb8-924">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-924">10001</span></span></td>
<td><span data-ttu-id="f8cb8-925">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-925">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-926">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-926">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="f8cb8-927">-2,977.17</span></span></td>
<td><span data-ttu-id="f8cb8-928">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-929">Prod 1</span></span></td>
<td><span data-ttu-id="f8cb8-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-930">Product 1</span></span></td>
<td><span data-ttu-id="f8cb8-931">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-931">10001</span></span></td>
<td><span data-ttu-id="f8cb8-932">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-932">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-933">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-933">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="f8cb8-934">2,507.09</span></span></td>
<td><span data-ttu-id="f8cb8-935">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8cb8-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-936">Prod 2</span></span></td>
<td><span data-ttu-id="f8cb8-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-937">Product 2</span></span></td>
<td><span data-ttu-id="f8cb8-938">10001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-938">10001</span></span></td>
<td><span data-ttu-id="f8cb8-939">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="f8cb8-939">Electricity</span></span></td>
<td><span data-ttu-id="f8cb8-940">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-940">Variable cost</span></span></td>
<td><span data-ttu-id="f8cb8-941">470.08</span><span class="sxs-lookup"><span data-stu-id="f8cb8-941">470.08</span></span></td>
<td><span data-ttu-id="f8cb8-942">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="f8cb8-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="f8cb8-943">Závěr</span><span class="sxs-lookup"><span data-stu-id="f8cb8-943">Conclusion</span></span>
<span data-ttu-id="f8cb8-944">Ve finančním účtování se náklady za elektřinu ve výši 10 000 zaúčtují na ID fiktivního nákladového střediska.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="f8cb8-945">Účetní tak budou vědět, že tento náklad musí být přidělen.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="f8cb8-946">V nákladovém účetnictví náklady procházejí napříč organizačními jednotkami a úrovněmi, na základě použitých zásad a pravidel.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="f8cb8-947">Každý náklad byl přidružen k základu přidělení, který poskytuje nejlepší hodnocení pro přidělení nákladů.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="f8cb8-948">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="f8cb8-949">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="f8cb8-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="f8cb8-950">Celkem</span><span class="sxs-lookup"><span data-stu-id="f8cb8-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f8cb8-951">CC099</span><span class="sxs-lookup"><span data-stu-id="f8cb8-951">CC099</span></span></th>
<th><span data-ttu-id="f8cb8-952">CC001</span><span class="sxs-lookup"><span data-stu-id="f8cb8-952">CC001</span></span></th>
<th><span data-ttu-id="f8cb8-953">CC002</span><span class="sxs-lookup"><span data-stu-id="f8cb8-953">CC002</span></span></th>
<th><span data-ttu-id="f8cb8-954">CC003</span><span class="sxs-lookup"><span data-stu-id="f8cb8-954">CC003</span></span></th>
<th><span data-ttu-id="f8cb8-955">CC004</span><span class="sxs-lookup"><span data-stu-id="f8cb8-955">CC004</span></span></th>
<th><span data-ttu-id="f8cb8-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-956">Proj 1</span></span></th>
<th><span data-ttu-id="f8cb8-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-957">Proj 2</span></span></th>
<th><span data-ttu-id="f8cb8-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="f8cb8-958">Prod 1</span></span></th>
<th><span data-ttu-id="f8cb8-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="f8cb8-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="f8cb8-960">10001 Elektřina</span><span class="sxs-lookup"><span data-stu-id="f8cb8-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f8cb8-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="f8cb8-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f8cb8-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="f8cb8-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f8cb8-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="f8cb8-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f8cb8-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="f8cb8-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="f8cb8-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="f8cb8-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f8cb8-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="f8cb8-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f8cb8-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="f8cb8-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f8cb8-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="f8cb8-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f8cb8-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="f8cb8-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="f8cb8-970">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="f8cb8-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f8cb8-971">0,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="f8cb8-972">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f8cb8-973">0,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f8cb8-974">0,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f8cb8-975">0,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f8cb8-976">0,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f8cb8-977">0,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="f8cb8-978">776.36</span><span class="sxs-lookup"><span data-stu-id="f8cb8-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f8cb8-979">223.64</span><span class="sxs-lookup"><span data-stu-id="f8cb8-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f8cb8-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="f8cb8-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="f8cb8-981">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="f8cb8-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f8cb8-982">000</span><span class="sxs-lookup"><span data-stu-id="f8cb8-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f8cb8-983">0,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f8cb8-984">0,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f8cb8-985">0,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f8cb8-986">0,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f8cb8-987">30.00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f8cb8-988">10,00</span><span class="sxs-lookup"><span data-stu-id="f8cb8-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f8cb8-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="f8cb8-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f8cb8-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="f8cb8-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f8cb8-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="f8cb8-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="f8cb8-992">Toto téma popisuje, jak primární prvek nákladů, 10001 Elektřina, prochází přes objekty nákladů.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="f8cb8-993">Tyto režijní náklady tedy budou přiděleny na nejnižší úroveň v organizaci.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="f8cb8-994">Jinak řečeno, objekty nákladů na nejnižší úrovni ponesou náklady.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="f8cb8-995">Chcete-li vizuální tok nákladů mezi objekty nákladů, můžete použít pravidla zásad shrnutí nákladů pro vizualizaci jejich toků.</span><span class="sxs-lookup"><span data-stu-id="f8cb8-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="f8cb8-996">Další informace naleznete v tématu [Zásady shrnutí nákladů a výpočet režijních nákladů](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="f8cb8-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



