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
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 923e6e38a664e17ec3349d839c4b77ec903c5dc2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441267"
---
# <a name="overhead-calculation"></a><span data-ttu-id="6a4dc-103">Výpočet režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a4dc-104">Toto téma popisuje typické procesy pro výpočet a přidělení režijních nákladů.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="6a4dc-105">Definice termínu</span><span class="sxs-lookup"><span data-stu-id="6a4dc-105">Term definition</span></span>
---------------

<span data-ttu-id="6a4dc-106">Režijní náklady jsou náklady, které nutně vznikají při chodu podnikání, ale nelze je připsat přímo k žádné konkrétní podnikatelské aktivitě, produktu nebo službě.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="6a4dc-107">Režijní náklady poskytují důležitou podporu pro generování aktivity přinášejících zisk.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="6a4dc-108">Následuje několik příkladů režijních nákladů:</span><span class="sxs-lookup"><span data-stu-id="6a4dc-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="6a4dc-109">Renta</span><span class="sxs-lookup"><span data-stu-id="6a4dc-109">Rent</span></span>
-   <span data-ttu-id="6a4dc-110">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-110">Electricity</span></span>
-   <span data-ttu-id="6a4dc-111">Administrativní mzdy</span><span class="sxs-lookup"><span data-stu-id="6a4dc-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="6a4dc-112">Přehled výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-112">Overhead calculation overview</span></span>
<span data-ttu-id="6a4dc-113">Výpočet režijních nákladů spustí zásady účtování nákladů ve správném pořadí.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="6a4dc-114">Výpočet režijních nákladů můžete pro stejné fiskální období spustit mnohokrát, pokud došlo ke změně zásad účtování nákladů nebo zjištění konkrétních chyb.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="6a4dc-115">Každé spuštění výpočtu režijních nákladů se ukládá a přijímá ID jedinečné verze, které vám umožní porovnávat výpočty v různých verzích.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="6a4dc-116">Položky nákladů, které generuje výpočet režijních nákladů, přijímá datum účtování.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="6a4dc-117">Toto datum účtován se shoduje s konvovým datem fiskálního období, které se použije ve výpočtu.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="6a4dc-118">ID jedinečné verze se skládá z následujících prvků:</span><span class="sxs-lookup"><span data-stu-id="6a4dc-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="6a4dc-119">Typ verze</span><span class="sxs-lookup"><span data-stu-id="6a4dc-119">Version type</span></span>
-   <span data-ttu-id="6a4dc-120">Datum a čas</span><span class="sxs-lookup"><span data-stu-id="6a4dc-120">Date and time</span></span>
-   <span data-ttu-id="6a4dc-121">Hlavní kniha nákladového účetnictví</span><span class="sxs-lookup"><span data-stu-id="6a4dc-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="6a4dc-122">Fiskální rok</span><span class="sxs-lookup"><span data-stu-id="6a4dc-122">Fiscal year</span></span>
-   <span data-ttu-id="6a4dc-123">Fiskální období</span><span class="sxs-lookup"><span data-stu-id="6a4dc-123">Fiscal period</span></span>

<span data-ttu-id="6a4dc-124">Výpočet režijních nákladů se spustí bez ohledu na verzi.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="6a4dc-125">Proto lze vypočítat rozpočtovou verzi před skutečnou verzí.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="6a4dc-126">Výpočet režijních nákladů se skládá ze čtyř kroků uvedených na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="6a4dc-127">V každé fázi je vytvořeno záhlaví deníku, které obsahuje položky deníku.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="6a4dc-128">Toto záhlaví deníku zachovává vstupní data pro každý krok výpočtu.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="6a4dc-129">Zásady a pravidla se použijí na každý řádek deníku a položky nákladů jsou generovány jako výstup.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="6a4dc-130">Máte tedy vždy plnou sledovatelnost.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="6a4dc-131">[![Výpočet režijních nákladů](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="6a4dc-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="6a4dc-132">Výpočet a přidělení režijních nákladů za elektřinu</span><span class="sxs-lookup"><span data-stu-id="6a4dc-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="6a4dc-133">Ve finančním účetnictví se některé náklady, jako je například elektřina, registrují jako paušální.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="6a4dc-134">Podrobný přehled pro vedoucí není tedy pro nákladové účetnictví k dispozici.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="6a4dc-135">V nákladovém účetnictví musí náklady procházet organizačními jednotkami, aby byl získán správný přehled pro vedoucí napříč všemi jednotkami a úrovněmi organizace.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="6a4dc-136">Tento tok musí být založen buď na přesném záznamu spotřeby nebo na objektivním hodnocení.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="6a4dc-137">V hlavní knize mohou být zaúčtovány náklady na elektřinu způsobem znázorněným v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6a4dc-138">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="6a4dc-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6a4dc-139">Nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="6a4dc-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="6a4dc-140">Hlavní účet</span><span class="sxs-lookup"><span data-stu-id="6a4dc-140">Main account</span></span></th>
<th><span data-ttu-id="6a4dc-141">Částka v zúčtovací měně</span><span class="sxs-lookup"><span data-stu-id="6a4dc-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a4dc-142">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="6a4dc-143">CC099</span><span class="sxs-lookup"><span data-stu-id="6a4dc-143">CC099</span></span></td>
<td><span data-ttu-id="6a4dc-144">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="6a4dc-144">Default cost center</span></span></td>
<td><span data-ttu-id="6a4dc-145">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-145">10001</span></span></td>
<td><span data-ttu-id="6a4dc-146">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-146">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="6a4dc-148">Krok 1: Zpracování výpočtu chování nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="6a4dc-149">Ve výchozím nastavení dostanou při importu položek nákladů z datového zdroje tyto položky v nákladovém účetnictví klasifikaci **Neklasifikované**.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="6a4dc-150">Použitím pravidla zásad chování nákladů lze reklasifikovat položky nákladů jako **Pevné náklady** nebo **Variabilní náklady**.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="6a4dc-151">Definice pravidel chování nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-151">Define the cost behavior rule</span></span>

<span data-ttu-id="6a4dc-152">V některých případech je část nákladů s pevným poplatkem a zbývající náklady jsou založeny na spotřebě.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="6a4dc-153">Účty za elektřinu často odpovídají této definici.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="6a4dc-154">Po platbě konkrétního pevného poplatku platíte spotřebu za kilowatthodinu (kWh).</span><span class="sxs-lookup"><span data-stu-id="6a4dc-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="6a4dc-155">Pokud je například poplatek pevných nákladů 1 000,00, definuje se pravidlo chování nákladů takto:</span><span class="sxs-lookup"><span data-stu-id="6a4dc-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="6a4dc-156">Pevná částka 1 000,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="6a4dc-157">0 &lt;= 1 000,00 = Pevná</span><span class="sxs-lookup"><span data-stu-id="6a4dc-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="6a4dc-158">1 000,01 &lt; N = Variabilní</span><span class="sxs-lookup"><span data-stu-id="6a4dc-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="6a4dc-159">Deník</span><span class="sxs-lookup"><span data-stu-id="6a4dc-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6a4dc-160">Deník</span><span class="sxs-lookup"><span data-stu-id="6a4dc-160">Journal</span></span></th>
<th><span data-ttu-id="6a4dc-161">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="6a4dc-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6a4dc-162">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="6a4dc-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6a4dc-163">Verze</span><span class="sxs-lookup"><span data-stu-id="6a4dc-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a4dc-164">00001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-164">00001</span></span></td>
<td><span data-ttu-id="6a4dc-165">Deník výpočtu chování nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="6a4dc-166">Fiskální</span><span class="sxs-lookup"><span data-stu-id="6a4dc-166">Fiscal</span></span></td>
<td><span data-ttu-id="6a4dc-167">2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-167">2017</span></span></td>
<td><span data-ttu-id="6a4dc-168">Období 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-168">Period 1</span></span></td>
<td><span data-ttu-id="6a4dc-169">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="6a4dc-170">Položky deníku (Položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="6a4dc-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6a4dc-171">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="6a4dc-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6a4dc-172">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6a4dc-173">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-173">Cost element</span></span></th>
<th><span data-ttu-id="6a4dc-174">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-174">Cost behavior</span></span></th>
<th><span data-ttu-id="6a4dc-175">Částka</span><span class="sxs-lookup"><span data-stu-id="6a4dc-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a4dc-176">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="6a4dc-177">CC099</span><span class="sxs-lookup"><span data-stu-id="6a4dc-177">CC099</span></span></td>
<td><span data-ttu-id="6a4dc-178">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="6a4dc-178">Default cost center</span></span></td>
<td><span data-ttu-id="6a4dc-179">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-179">10001</span></span></td>
<td><span data-ttu-id="6a4dc-180">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-180">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-181">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="6a4dc-181">Unclassified</span></span></td>
<td><span data-ttu-id="6a4dc-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6a4dc-183">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6a4dc-184">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6a4dc-185">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-185">Cost element</span></span></th>
<th><span data-ttu-id="6a4dc-186">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-186">Cost behavior</span></span></th>
<th><span data-ttu-id="6a4dc-187">Částka</span><span class="sxs-lookup"><span data-stu-id="6a4dc-187">Amount</span></span></th>
<th><span data-ttu-id="6a4dc-188">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="6a4dc-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a4dc-189">CC099</span><span class="sxs-lookup"><span data-stu-id="6a4dc-189">CC099</span></span></td>
<td><span data-ttu-id="6a4dc-190">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="6a4dc-190">Default cost center</span></span></td>
<td><span data-ttu-id="6a4dc-191">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-191">10001</span></span></td>
<td><span data-ttu-id="6a4dc-192">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-192">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-193">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="6a4dc-193">Unclassified</span></span></td>
<td><span data-ttu-id="6a4dc-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-194">10,000.00</span></span></td>
<td><span data-ttu-id="6a4dc-195">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-196">CC099</span><span class="sxs-lookup"><span data-stu-id="6a4dc-196">CC099</span></span></td>
<td><span data-ttu-id="6a4dc-197">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="6a4dc-197">Default cost center</span></span></td>
<td><span data-ttu-id="6a4dc-198">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-198">10001</span></span></td>
<td><span data-ttu-id="6a4dc-199">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-199">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-200">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="6a4dc-200">Unclassified</span></span></td>
<td><span data-ttu-id="6a4dc-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-201">-10,000.00</span></span></td>
<td><span data-ttu-id="6a4dc-202">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-203">CC099</span><span class="sxs-lookup"><span data-stu-id="6a4dc-203">CC099</span></span></td>
<td><span data-ttu-id="6a4dc-204">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="6a4dc-204">Default cost center</span></span></td>
<td><span data-ttu-id="6a4dc-205">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-205">10001</span></span></td>
<td><span data-ttu-id="6a4dc-206">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-206">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-207">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-207">Fixed cost</span></span></td>
<td><span data-ttu-id="6a4dc-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-208">1,000.00</span></span></td>
<td><span data-ttu-id="6a4dc-209">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-210">CC099</span><span class="sxs-lookup"><span data-stu-id="6a4dc-210">CC099</span></span></td>
<td><span data-ttu-id="6a4dc-211">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="6a4dc-211">Default cost center</span></span></td>
<td><span data-ttu-id="6a4dc-212">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-212">10001</span></span></td>
<td><span data-ttu-id="6a4dc-213">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-213">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-214">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-214">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-215">9,000.00</span></span></td>
<td><span data-ttu-id="6a4dc-216">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6a4dc-217">Více informací naleznete v tématu [Vytvoření a přiřazení zásad chování nákladů k jednotce řízení nákladů](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="6a4dc-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="6a4dc-218">Krok 2: Zpracování výpočtu distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="6a4dc-219">Distribuce nákladů se používá k rozdělení nákladů z jednoho objektu nákladů na jeden nebo více dalších objektů nákladů použitím příslušného základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="6a4dc-220">Distribuce nákladů a přidělení nákladů se liší v tom, že k distribuci nákladů dochází vždy na úrovni primárního prvku nákladů původních nákladů.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="6a4dc-221">Definice pravidel distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-221">Define the cost distribution rule</span></span>

<span data-ttu-id="6a4dc-222">Ve finančním účetnictví se náklady na elektřinu často registrují jako paušální.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="6a4dc-223">V nákladovém účetnictví není tento přístup dostatečně podrobný.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="6a4dc-224">Variabilní náklady by měly být distribuovány k jednotlivým objektům nákladů na solidním základě.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="6a4dc-225">Nejlogičtější základ přidělení je spotřeba elektřiny (kWh).</span><span class="sxs-lookup"><span data-stu-id="6a4dc-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="6a4dc-226">Vytvoří se člen statistické dimenzi s názvem Elektřina a zaznamená se elektrické spotřeba.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="6a4dc-227">Ve výchozím nastavení se všechny členy statistické dimenze stanou dostupnými zpřístupněny jako základy přidělení.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6a4dc-228">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-228">Cost object</span></span></th>
<th><span data-ttu-id="6a4dc-229">kWh</span><span class="sxs-lookup"><span data-stu-id="6a4dc-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a4dc-230">CC001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-230">CC001</span></span></td>
<td><span data-ttu-id="6a4dc-231">HR</span><span class="sxs-lookup"><span data-stu-id="6a4dc-231">HR</span></span></td>
<td><span data-ttu-id="6a4dc-232">1 000</span><span class="sxs-lookup"><span data-stu-id="6a4dc-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-233">CC002</span><span class="sxs-lookup"><span data-stu-id="6a4dc-233">CC002</span></span></td>
<td><span data-ttu-id="6a4dc-234">Finance</span><span class="sxs-lookup"><span data-stu-id="6a4dc-234">Finance</span></span></td>
<td><span data-ttu-id="6a4dc-235">6,000</span><span class="sxs-lookup"><span data-stu-id="6a4dc-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-236">CC003</span><span class="sxs-lookup"><span data-stu-id="6a4dc-236">CC003</span></span></td>
<td><span data-ttu-id="6a4dc-237">Sestavení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-237">Assembly</span></span></td>
<td><span data-ttu-id="6a4dc-238">0</span><span class="sxs-lookup"><span data-stu-id="6a4dc-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6a4dc-239">Následující tabulka zobrazuje výsledek při použití elektrické spotřeby jako základu přidělení pro variabilní náklady.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6a4dc-240">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-240">Cost object</span></span></th>
<th><span data-ttu-id="6a4dc-241">Hodnota</span><span class="sxs-lookup"><span data-stu-id="6a4dc-241">Magnitude</span></span></th>
<th><span data-ttu-id="6a4dc-242">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-242">Allocation factor</span></span></th>
<th><span data-ttu-id="6a4dc-243">Částka</span><span class="sxs-lookup"><span data-stu-id="6a4dc-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a4dc-244">CC001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-244">CC001</span></span></td>
<td><span data-ttu-id="6a4dc-245">HR</span><span class="sxs-lookup"><span data-stu-id="6a4dc-245">HR</span></span></td>
<td><span data-ttu-id="6a4dc-246">1 000</span><span class="sxs-lookup"><span data-stu-id="6a4dc-246">1,000</span></span></td>
<td><span data-ttu-id="6a4dc-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="6a4dc-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="6a4dc-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-249">CC002</span><span class="sxs-lookup"><span data-stu-id="6a4dc-249">CC002</span></span></td>
<td><span data-ttu-id="6a4dc-250">Finance</span><span class="sxs-lookup"><span data-stu-id="6a4dc-250">Finance</span></span></td>
<td><span data-ttu-id="6a4dc-251">6,000</span><span class="sxs-lookup"><span data-stu-id="6a4dc-251">6,000</span></span></td>
<td><span data-ttu-id="6a4dc-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="6a4dc-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="6a4dc-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-254">CC003</span><span class="sxs-lookup"><span data-stu-id="6a4dc-254">CC003</span></span></td>
<td><span data-ttu-id="6a4dc-255">Sestavení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-255">Assembly</span></span></td>
<td><span data-ttu-id="6a4dc-256">0</span><span class="sxs-lookup"><span data-stu-id="6a4dc-256">0</span></span></td>
<td><span data-ttu-id="6a4dc-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="6a4dc-258">0,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6a4dc-259">Pevné náklady musí být distribuovány rovnoměrně k jednotlivých objektům nákladů, které spotřebovávaly elektřinu.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="6a4dc-260">Tohoto výsledku můžete dosáhnout pomocí členu statistické dimenze Elektřina v základu přidělení vzorce: (Elektřina &gt; 0,00) Následující tabulka zobrazuje výsledek při použití elektrické spotřeby jako základu přidělení pro variabilní náklady.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6a4dc-261">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-261">Cost object</span></span></th>
<th><span data-ttu-id="6a4dc-262">Vzorec</span><span class="sxs-lookup"><span data-stu-id="6a4dc-262">Formula</span></span></th>
<th><span data-ttu-id="6a4dc-263">Hodnota</span><span class="sxs-lookup"><span data-stu-id="6a4dc-263">Magnitude</span></span></th>
<th><span data-ttu-id="6a4dc-264">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-264">Allocation factor</span></span></th>
<th><span data-ttu-id="6a4dc-265">Částka</span><span class="sxs-lookup"><span data-stu-id="6a4dc-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a4dc-266">CC001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-266">CC001</span></span></td>
<td><span data-ttu-id="6a4dc-267">HR</span><span class="sxs-lookup"><span data-stu-id="6a4dc-267">HR</span></span></td>
<td><span data-ttu-id="6a4dc-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="6a4dc-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="6a4dc-269">1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-269">1</span></span></td>
<td><span data-ttu-id="6a4dc-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="6a4dc-271">500.00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-272">CC002</span><span class="sxs-lookup"><span data-stu-id="6a4dc-272">CC002</span></span></td>
<td><span data-ttu-id="6a4dc-273">Finance</span><span class="sxs-lookup"><span data-stu-id="6a4dc-273">Finance</span></span></td>
<td><span data-ttu-id="6a4dc-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="6a4dc-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="6a4dc-275">1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-275">1</span></span></td>
<td><span data-ttu-id="6a4dc-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="6a4dc-277">500.00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-278">CC003</span><span class="sxs-lookup"><span data-stu-id="6a4dc-278">CC003</span></span></td>
<td><span data-ttu-id="6a4dc-279">Sestavení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-279">Assembly</span></span></td>
<td><span data-ttu-id="6a4dc-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="6a4dc-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="6a4dc-281">0</span><span class="sxs-lookup"><span data-stu-id="6a4dc-281">0</span></span></td>
<td><span data-ttu-id="6a4dc-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="6a4dc-283">0,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="6a4dc-284">Deník</span><span class="sxs-lookup"><span data-stu-id="6a4dc-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6a4dc-285">Deník</span><span class="sxs-lookup"><span data-stu-id="6a4dc-285">Journal</span></span></th>
<th><span data-ttu-id="6a4dc-286">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="6a4dc-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6a4dc-287">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="6a4dc-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6a4dc-288">Verze</span><span class="sxs-lookup"><span data-stu-id="6a4dc-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a4dc-289">00002</span><span class="sxs-lookup"><span data-stu-id="6a4dc-289">00002</span></span></td>
<td><span data-ttu-id="6a4dc-290">Deník výpočtu distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="6a4dc-291">Fiskální</span><span class="sxs-lookup"><span data-stu-id="6a4dc-291">Fiscal</span></span></td>
<td><span data-ttu-id="6a4dc-292">2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-292">2017</span></span></td>
<td><span data-ttu-id="6a4dc-293">Období 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-293">Period 1</span></span></td>
<td><span data-ttu-id="6a4dc-294">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="6a4dc-295">Položky deníku (Položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="6a4dc-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6a4dc-296">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="6a4dc-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6a4dc-297">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6a4dc-298">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-298">Cost element</span></span></th>
<th><span data-ttu-id="6a4dc-299">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-299">Cost behavior</span></span></th>
<th><span data-ttu-id="6a4dc-300">Částka</span><span class="sxs-lookup"><span data-stu-id="6a4dc-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a4dc-301">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="6a4dc-302">CC099</span><span class="sxs-lookup"><span data-stu-id="6a4dc-302">CC099</span></span></td>
<td><span data-ttu-id="6a4dc-303">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="6a4dc-303">Default cost center</span></span></td>
<td><span data-ttu-id="6a4dc-304">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-304">10001</span></span></td>
<td><span data-ttu-id="6a4dc-305">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-305">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-306">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-306">Fixed cost</span></span></td>
<td><span data-ttu-id="6a4dc-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-308">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="6a4dc-309">CC099</span><span class="sxs-lookup"><span data-stu-id="6a4dc-309">CC099</span></span></td>
<td><span data-ttu-id="6a4dc-310">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="6a4dc-310">Default cost center</span></span></td>
<td><span data-ttu-id="6a4dc-311">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-311">10001</span></span></td>
<td><span data-ttu-id="6a4dc-312">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-312">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-313">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-313">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6a4dc-315">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6a4dc-316">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6a4dc-317">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-317">Cost element</span></span></th>
<th><span data-ttu-id="6a4dc-318">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-318">Cost behavior</span></span></th>
<th><span data-ttu-id="6a4dc-319">Částka</span><span class="sxs-lookup"><span data-stu-id="6a4dc-319">Amount</span></span></th>
<th><span data-ttu-id="6a4dc-320">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="6a4dc-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a4dc-321">CC099</span><span class="sxs-lookup"><span data-stu-id="6a4dc-321">CC099</span></span></td>
<td><span data-ttu-id="6a4dc-322">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="6a4dc-322">Default cost center</span></span></td>
<td><span data-ttu-id="6a4dc-323">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-323">10001</span></span></td>
<td><span data-ttu-id="6a4dc-324">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-324">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-325">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-325">Fixed cost</span></span></td>
<td><span data-ttu-id="6a4dc-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-326">-1,000.00</span></span></td>
<td><span data-ttu-id="6a4dc-327">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-328">CC001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-328">CC001</span></span></td>
<td><span data-ttu-id="6a4dc-329">HR</span><span class="sxs-lookup"><span data-stu-id="6a4dc-329">HR</span></span></td>
<td><span data-ttu-id="6a4dc-330">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-330">10001</span></span></td>
<td><span data-ttu-id="6a4dc-331">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-331">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-332">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-332">Fixed cost</span></span></td>
<td><span data-ttu-id="6a4dc-333">500.00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-333">500.00</span></span></td>
<td><span data-ttu-id="6a4dc-334">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-335">CC002</span><span class="sxs-lookup"><span data-stu-id="6a4dc-335">CC002</span></span></td>
<td><span data-ttu-id="6a4dc-336">Finance</span><span class="sxs-lookup"><span data-stu-id="6a4dc-336">Finance</span></span></td>
<td><span data-ttu-id="6a4dc-337">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-337">10001</span></span></td>
<td><span data-ttu-id="6a4dc-338">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-338">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-339">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-339">Fixed cost</span></span></td>
<td><span data-ttu-id="6a4dc-340">500.00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-340">500.00</span></span></td>
<td><span data-ttu-id="6a4dc-341">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-342">CC099</span><span class="sxs-lookup"><span data-stu-id="6a4dc-342">CC099</span></span></td>
<td><span data-ttu-id="6a4dc-343">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="6a4dc-343">Default cost center</span></span></td>
<td><span data-ttu-id="6a4dc-344">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-344">10001</span></span></td>
<td><span data-ttu-id="6a4dc-345">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-345">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-346">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-346">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-347">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-347">-9,000.00</span></span></td>
<td><span data-ttu-id="6a4dc-348">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-349">CC001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-349">CC001</span></span></td>
<td><span data-ttu-id="6a4dc-350">HR</span><span class="sxs-lookup"><span data-stu-id="6a4dc-350">HR</span></span></td>
<td><span data-ttu-id="6a4dc-351">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-351">10001</span></span></td>
<td><span data-ttu-id="6a4dc-352">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-352">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-353">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-353">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="6a4dc-354">1,285.71</span></span></td>
<td><span data-ttu-id="6a4dc-355">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-356">CC002</span><span class="sxs-lookup"><span data-stu-id="6a4dc-356">CC002</span></span></td>
<td><span data-ttu-id="6a4dc-357">Finance</span><span class="sxs-lookup"><span data-stu-id="6a4dc-357">Finance</span></span></td>
<td><span data-ttu-id="6a4dc-358">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-358">10001</span></span></td>
<td><span data-ttu-id="6a4dc-359">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-359">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-360">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-360">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="6a4dc-361">7,714.29</span></span></td>
<td><span data-ttu-id="6a4dc-362">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6a4dc-363">Více informací naleznete v tématu [Vytvoření a přiřazení zásad distribuce nákladů k jednotce řízení nákladů](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="6a4dc-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="6a4dc-364">Krok 3: Zpracování výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="6a4dc-365">Režijní náklady se používají k účtování jednoho nebo více konkrétních objektů nákladů.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="6a4dc-366">Účtování je založeno na předem určené nákladové sazbě a množství z přiřazeného základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="6a4dc-367">Definice sazby režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-367">Define the overhead rate</span></span>

<span data-ttu-id="6a4dc-368">Objekt nákladů CC001 HR přispívá k sadě interních projektů.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="6a4dc-369">Vytvoří se člen statistické dimenzi s názvem projekty lidských zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6a4dc-370">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-370">Cost object</span></span></th>
<th><span data-ttu-id="6a4dc-371">Pracovní doba</span><span class="sxs-lookup"><span data-stu-id="6a4dc-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a4dc-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-372">Proj 1</span></span></td>
<td><span data-ttu-id="6a4dc-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-373">Project 1</span></span></td>
<td><span data-ttu-id="6a4dc-374">3</span><span class="sxs-lookup"><span data-stu-id="6a4dc-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-375">Proj 2</span></span></td>
<td><span data-ttu-id="6a4dc-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-376">Project 2</span></span></td>
<td><span data-ttu-id="6a4dc-377">1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6a4dc-378">Byla definována předem určená nákladová sazba pro příspěvky k nákladovým projektům.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6a4dc-379">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-379">Cost object</span></span></th>
<th><span data-ttu-id="6a4dc-380">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-380">Cost element</span></span></th>
<th><span data-ttu-id="6a4dc-381">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-381">Cost behavior</span></span></th>
<th><span data-ttu-id="6a4dc-382">Jednotky</span><span class="sxs-lookup"><span data-stu-id="6a4dc-382">Units</span></span></th>
<th><span data-ttu-id="6a4dc-383">Kurz</span><span class="sxs-lookup"><span data-stu-id="6a4dc-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a4dc-384">CC001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-384">CC001</span></span></td>
<td><span data-ttu-id="6a4dc-385">HR</span><span class="sxs-lookup"><span data-stu-id="6a4dc-385">HR</span></span></td>
<td><span data-ttu-id="6a4dc-386">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-386">10001</span></span></td>
<td><span data-ttu-id="6a4dc-387">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-387">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-388">1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-388">1</span></span></td>
<td><span data-ttu-id="6a4dc-389">10</span><span class="sxs-lookup"><span data-stu-id="6a4dc-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6a4dc-390">Následující tabulka zobrazuje výsledek při použití projektů lidských zdrojů jako základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6a4dc-391">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-391">Cost object</span></span></th>
<th><span data-ttu-id="6a4dc-392">Hodnota</span><span class="sxs-lookup"><span data-stu-id="6a4dc-392">Magnitude</span></span></th>
<th><span data-ttu-id="6a4dc-393">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-393">Cost element</span></span></th>
<th><span data-ttu-id="6a4dc-394">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-394">Allocation factor</span></span></th>
<th><span data-ttu-id="6a4dc-395">Částka</span><span class="sxs-lookup"><span data-stu-id="6a4dc-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a4dc-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-396">Proj 1</span></span></td>
<td><span data-ttu-id="6a4dc-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-397">Project 1</span></span></td>
<td><span data-ttu-id="6a4dc-398">3</span><span class="sxs-lookup"><span data-stu-id="6a4dc-398">3</span></span></td>
<td><span data-ttu-id="6a4dc-399">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-399">10001</span></span></td>
<td><span data-ttu-id="6a4dc-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="6a4dc-401">30.00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-402">Proj 2</span></span></td>
<td><span data-ttu-id="6a4dc-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-403">Project 2</span></span></td>
<td><span data-ttu-id="6a4dc-404">1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-404">1</span></span></td>
<td><span data-ttu-id="6a4dc-405">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-405">10001</span></span></td>
<td><span data-ttu-id="6a4dc-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="6a4dc-407">10,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="6a4dc-408">Deník</span><span class="sxs-lookup"><span data-stu-id="6a4dc-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6a4dc-409">Deník</span><span class="sxs-lookup"><span data-stu-id="6a4dc-409">Journal</span></span></th>
<th><span data-ttu-id="6a4dc-410">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="6a4dc-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6a4dc-411">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="6a4dc-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6a4dc-412">Verze</span><span class="sxs-lookup"><span data-stu-id="6a4dc-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a4dc-413">00003</span><span class="sxs-lookup"><span data-stu-id="6a4dc-413">00003</span></span></td>
<td><span data-ttu-id="6a4dc-414">Deník výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="6a4dc-415">Fiskální</span><span class="sxs-lookup"><span data-stu-id="6a4dc-415">Fiscal</span></span></td>
<td><span data-ttu-id="6a4dc-416">2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-416">2017</span></span></td>
<td><span data-ttu-id="6a4dc-417">Období 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-417">Period 1</span></span></td>
<td><span data-ttu-id="6a4dc-418">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="6a4dc-419">Položky deníku (položky deníku pro výpočet sazby režijních nákladů)</span><span class="sxs-lookup"><span data-stu-id="6a4dc-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6a4dc-420">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="6a4dc-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6a4dc-421">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-421">Cost object</span></span></th>
<th><span data-ttu-id="6a4dc-422">Hodnota</span><span class="sxs-lookup"><span data-stu-id="6a4dc-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a4dc-423">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="6a4dc-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-424">Proj 1</span></span></td>
<td><span data-ttu-id="6a4dc-425">Interní projekt 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="6a4dc-426">3,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-427">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="6a4dc-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-428">Proj 2</span></span></td>
<td><span data-ttu-id="6a4dc-429">Interní projekt 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="6a4dc-430">1.00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6a4dc-431">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6a4dc-432">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6a4dc-433">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-433">Cost element</span></span></th>
<th><span data-ttu-id="6a4dc-434">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-434">Cost behavior</span></span></th>
<th><span data-ttu-id="6a4dc-435">Částka</span><span class="sxs-lookup"><span data-stu-id="6a4dc-435">Amount</span></span></th>
<th><span data-ttu-id="6a4dc-436">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="6a4dc-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a4dc-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-437">CC0001</span></span></td>
<td><span data-ttu-id="6a4dc-438">HR</span><span class="sxs-lookup"><span data-stu-id="6a4dc-438">HR</span></span></td>
<td><span data-ttu-id="6a4dc-439">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-439">10001</span></span></td>
<td><span data-ttu-id="6a4dc-440">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-440">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-441">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-441">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-442">-30.00</span></span></td>
<td><span data-ttu-id="6a4dc-443">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-444">Proj 1</span></span></td>
<td><span data-ttu-id="6a4dc-445">Interní projekt 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="6a4dc-446">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-446">10001</span></span></td>
<td><span data-ttu-id="6a4dc-447">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-447">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-448">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-448">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-449">30.00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-449">30.00</span></span></td>
<td><span data-ttu-id="6a4dc-450">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-451">CC001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-451">CC001</span></span></td>
<td><span data-ttu-id="6a4dc-452">HR</span><span class="sxs-lookup"><span data-stu-id="6a4dc-452">HR</span></span></td>
<td><span data-ttu-id="6a4dc-453">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-453">10001</span></span></td>
<td><span data-ttu-id="6a4dc-454">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-454">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-455">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-455">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-456">-10.00</span></span></td>
<td><span data-ttu-id="6a4dc-457">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-458">Proj 2</span></span></td>
<td><span data-ttu-id="6a4dc-459">Interní projekt 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="6a4dc-460">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-460">10001</span></span></td>
<td><span data-ttu-id="6a4dc-461">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-461">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-462">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-462">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-463">10.00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-463">10.00</span></span></td>
<td><span data-ttu-id="6a4dc-464">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6a4dc-465">Další informace naleznete v tématu [Provedení výpočtu režijních nákladů](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="6a4dc-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="6a4dc-466">Krok 4: Zpracování výpočtu přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="6a4dc-467">Přidělení se používá k přidělení zůstatku objektu nákladů do jiných objektů nákladů použitím základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="6a4dc-468">Aplikace Finance podporuje reciproční metodu přidělování.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="6a4dc-469">V metodě vzájemného přidělení jsou plně rozpoznány vzájemné služby, které si vyměňují pomocné objekty nákladů.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="6a4dc-470">Systém automaticky určí provádění přidělení ve správném pořadí.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="6a4dc-471">Zůstatek objektu nákladů je přidělen jedním základem přidělení.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="6a4dc-472">Je podporováno přidělování napříč dimenzemi objektů nákladů a jejich příslušných členů.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="6a4dc-473">Pořadí přidělení je řízeno jednotkou řízení nákladů.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="6a4dc-474">[![Reciproční metoda](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="6a4dc-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="6a4dc-475">Definice přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-475">Define the cost allocation</span></span>

<span data-ttu-id="6a4dc-476">Toto je jednoduchý příklad, který vysvětluje, jakým způsobem lze sledovat tok nákladů.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="6a4dc-477">Objekt nákladů objektu CC001 HR přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="6a4dc-478">Vytvoří se člen statistické dimenzi s názvem služby lidských zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6a4dc-479">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-479">Cost object</span></span></th>
<th><span data-ttu-id="6a4dc-480">Služby HR</span><span class="sxs-lookup"><span data-stu-id="6a4dc-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a4dc-481">CC002</span><span class="sxs-lookup"><span data-stu-id="6a4dc-481">CC002</span></span></td>
<td><span data-ttu-id="6a4dc-482">Finance</span><span class="sxs-lookup"><span data-stu-id="6a4dc-482">Finance</span></span></td>
<td><span data-ttu-id="6a4dc-483">35</span><span class="sxs-lookup"><span data-stu-id="6a4dc-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-484">CC003</span><span class="sxs-lookup"><span data-stu-id="6a4dc-484">CC003</span></span></td>
<td><span data-ttu-id="6a4dc-485">Sestavení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-485">Assembly</span></span></td>
<td><span data-ttu-id="6a4dc-486">55</span><span class="sxs-lookup"><span data-stu-id="6a4dc-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-487">CC004</span><span class="sxs-lookup"><span data-stu-id="6a4dc-487">CC004</span></span></td>
<td><span data-ttu-id="6a4dc-488">Balení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-488">Packaging</span></span></td>
<td><span data-ttu-id="6a4dc-489">10</span><span class="sxs-lookup"><span data-stu-id="6a4dc-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6a4dc-490">Objekt nákladů objektu CC002 Finance přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="6a4dc-491">Vytvoří se člen statistické dimenzi s názvem Finanční služby k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6a4dc-492">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-492">Cost object</span></span></th>
<th><span data-ttu-id="6a4dc-493">Finanční služby</span><span class="sxs-lookup"><span data-stu-id="6a4dc-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a4dc-494">CC003</span><span class="sxs-lookup"><span data-stu-id="6a4dc-494">CC003</span></span></td>
<td><span data-ttu-id="6a4dc-495">Sestavení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-495">Assembly</span></span></td>
<td><span data-ttu-id="6a4dc-496">65</span><span class="sxs-lookup"><span data-stu-id="6a4dc-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-497">CC004</span><span class="sxs-lookup"><span data-stu-id="6a4dc-497">CC004</span></span></td>
<td><span data-ttu-id="6a4dc-498">Balení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-498">Packaging</span></span></td>
<td><span data-ttu-id="6a4dc-499">35</span><span class="sxs-lookup"><span data-stu-id="6a4dc-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6a4dc-500">Objekt nákladů objektu CC003 Sestavení přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="6a4dc-501">Vytvoří se člen statistické dimenzi s názvem Služby sestavení zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6a4dc-502">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-502">Cost object</span></span></th>
<th><span data-ttu-id="6a4dc-503">Služby sestavení (v hodinách)</span><span class="sxs-lookup"><span data-stu-id="6a4dc-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a4dc-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-504">Prod 1</span></span></td>
<td><span data-ttu-id="6a4dc-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-505">Product 1</span></span></td>
<td><span data-ttu-id="6a4dc-506">60</span><span class="sxs-lookup"><span data-stu-id="6a4dc-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-507">Prod 2</span></span></td>
<td><span data-ttu-id="6a4dc-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-508">Product 2</span></span></td>
<td><span data-ttu-id="6a4dc-509">20</span><span class="sxs-lookup"><span data-stu-id="6a4dc-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6a4dc-510">Objekt nákladů objektu CC004 Balení přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="6a4dc-511">Vytvoří se člen statistické dimenzi s názvem Služby balení k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6a4dc-512">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-512">Cost object</span></span></th>
<th><span data-ttu-id="6a4dc-513">Služby balení (v hodinách)</span><span class="sxs-lookup"><span data-stu-id="6a4dc-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a4dc-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-514">Prod 1</span></span></td>
<td><span data-ttu-id="6a4dc-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-515">Product 1</span></span></td>
<td><span data-ttu-id="6a4dc-516">80</span><span class="sxs-lookup"><span data-stu-id="6a4dc-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-517">Prod 2</span></span></td>
<td><span data-ttu-id="6a4dc-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-518">Product 2</span></span></td>
<td><span data-ttu-id="6a4dc-519">15</span><span class="sxs-lookup"><span data-stu-id="6a4dc-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="6a4dc-520">Statistická měření, jako je například výrobní doba spotřebovaná produktem, lze odvodit z datového zdroje.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="6a4dc-521">Více informací naleznete v části [Šablona poskytovatele statistického měření](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="6a4dc-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="6a4dc-522">V následující tabulce je uveden výsledek při použití služeb HR jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="6a4dc-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6a4dc-523">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-523">Cost object</span></span></th>
<th><span data-ttu-id="6a4dc-524">Hodnota</span><span class="sxs-lookup"><span data-stu-id="6a4dc-524">Magnitude</span></span></th>
<th><span data-ttu-id="6a4dc-525">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-525">Allocation factor</span></span></th>
<th><span data-ttu-id="6a4dc-526">Částka</span><span class="sxs-lookup"><span data-stu-id="6a4dc-526">Amount</span></span></th>
<th><span data-ttu-id="6a4dc-527">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a4dc-528">CC002</span><span class="sxs-lookup"><span data-stu-id="6a4dc-528">CC002</span></span></td>
<td><span data-ttu-id="6a4dc-529">Finance</span><span class="sxs-lookup"><span data-stu-id="6a4dc-529">Finance</span></span></td>
<td><span data-ttu-id="6a4dc-530">35</span><span class="sxs-lookup"><span data-stu-id="6a4dc-530">35</span></span></td>
<td><span data-ttu-id="6a4dc-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="6a4dc-532">175.00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-532">175.00</span></span></td>
<td><span data-ttu-id="6a4dc-533">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-534">CC003</span><span class="sxs-lookup"><span data-stu-id="6a4dc-534">CC003</span></span></td>
<td><span data-ttu-id="6a4dc-535">Sestavení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-535">Assembly</span></span></td>
<td><span data-ttu-id="6a4dc-536">55</span><span class="sxs-lookup"><span data-stu-id="6a4dc-536">55</span></span></td>
<td><span data-ttu-id="6a4dc-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="6a4dc-538">275.00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-538">275.00</span></span></td>
<td><span data-ttu-id="6a4dc-539">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-540">CC004</span><span class="sxs-lookup"><span data-stu-id="6a4dc-540">CC004</span></span></td>
<td><span data-ttu-id="6a4dc-541">Balení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-541">Packaging</span></span></td>
<td><span data-ttu-id="6a4dc-542">10</span><span class="sxs-lookup"><span data-stu-id="6a4dc-542">10</span></span></td>
<td><span data-ttu-id="6a4dc-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="6a4dc-544">50,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-544">50.00</span></span></td>
<td><span data-ttu-id="6a4dc-545">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-546">CC002</span><span class="sxs-lookup"><span data-stu-id="6a4dc-546">CC002</span></span></td>
<td><span data-ttu-id="6a4dc-547">Finance</span><span class="sxs-lookup"><span data-stu-id="6a4dc-547">Finance</span></span></td>
<td><span data-ttu-id="6a4dc-548">35</span><span class="sxs-lookup"><span data-stu-id="6a4dc-548">35</span></span></td>
<td><span data-ttu-id="6a4dc-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="6a4dc-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="6a4dc-550">436.00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-550">436.00</span></span></td>
<td><span data-ttu-id="6a4dc-551">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-552">CC003</span><span class="sxs-lookup"><span data-stu-id="6a4dc-552">CC003</span></span></td>
<td><span data-ttu-id="6a4dc-553">Sestavení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-553">Assembly</span></span></td>
<td><span data-ttu-id="6a4dc-554">55</span><span class="sxs-lookup"><span data-stu-id="6a4dc-554">55</span></span></td>
<td><span data-ttu-id="6a4dc-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="6a4dc-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="6a4dc-556">685.14</span><span class="sxs-lookup"><span data-stu-id="6a4dc-556">685.14</span></span></td>
<td><span data-ttu-id="6a4dc-557">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-558">CC004</span><span class="sxs-lookup"><span data-stu-id="6a4dc-558">CC004</span></span></td>
<td><span data-ttu-id="6a4dc-559">Balení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-559">Packaging</span></span></td>
<td><span data-ttu-id="6a4dc-560">10</span><span class="sxs-lookup"><span data-stu-id="6a4dc-560">10</span></span></td>
<td><span data-ttu-id="6a4dc-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="6a4dc-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="6a4dc-562">124.57</span><span class="sxs-lookup"><span data-stu-id="6a4dc-562">124.57</span></span></td>
<td><span data-ttu-id="6a4dc-563">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6a4dc-564">V následující tabulce je uveden výsledek při použití Finančních služeb Finance jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="6a4dc-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6a4dc-565">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-565">Cost object</span></span></th>
<th><span data-ttu-id="6a4dc-566">Hodnota</span><span class="sxs-lookup"><span data-stu-id="6a4dc-566">Magnitude</span></span></th>
<th><span data-ttu-id="6a4dc-567">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-567">Allocation factor</span></span></th>
<th><span data-ttu-id="6a4dc-568">Částka</span><span class="sxs-lookup"><span data-stu-id="6a4dc-568">Amount</span></span></th>
<th><span data-ttu-id="6a4dc-569">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a4dc-570">CC003</span><span class="sxs-lookup"><span data-stu-id="6a4dc-570">CC003</span></span></td>
<td><span data-ttu-id="6a4dc-571">Sestavení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-571">Assembly</span></span></td>
<td><span data-ttu-id="6a4dc-572">65</span><span class="sxs-lookup"><span data-stu-id="6a4dc-572">65</span></span></td>
<td><span data-ttu-id="6a4dc-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="6a4dc-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="6a4dc-574">438.75</span><span class="sxs-lookup"><span data-stu-id="6a4dc-574">438.75</span></span></td>
<td><span data-ttu-id="6a4dc-575">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-576">CC004</span><span class="sxs-lookup"><span data-stu-id="6a4dc-576">CC004</span></span></td>
<td><span data-ttu-id="6a4dc-577">Balení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-577">Packaging</span></span></td>
<td><span data-ttu-id="6a4dc-578">35</span><span class="sxs-lookup"><span data-stu-id="6a4dc-578">35</span></span></td>
<td><span data-ttu-id="6a4dc-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="6a4dc-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="6a4dc-580">236.25</span><span class="sxs-lookup"><span data-stu-id="6a4dc-580">236.25</span></span></td>
<td><span data-ttu-id="6a4dc-581">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-582">CC003</span><span class="sxs-lookup"><span data-stu-id="6a4dc-582">CC003</span></span></td>
<td><span data-ttu-id="6a4dc-583">Sestavení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-583">Assembly</span></span></td>
<td><span data-ttu-id="6a4dc-584">65</span><span class="sxs-lookup"><span data-stu-id="6a4dc-584">65</span></span></td>
<td><span data-ttu-id="6a4dc-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="6a4dc-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="6a4dc-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="6a4dc-586">5,297.69</span></span></td>
<td><span data-ttu-id="6a4dc-587">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-588">CC004</span><span class="sxs-lookup"><span data-stu-id="6a4dc-588">CC004</span></span></td>
<td><span data-ttu-id="6a4dc-589">Balení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-589">Packaging</span></span></td>
<td><span data-ttu-id="6a4dc-590">35</span><span class="sxs-lookup"><span data-stu-id="6a4dc-590">35</span></span></td>
<td><span data-ttu-id="6a4dc-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="6a4dc-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="6a4dc-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="6a4dc-592">2,852.60</span></span></td>
<td><span data-ttu-id="6a4dc-593">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6a4dc-594">V následující tabulce je uveden výsledek při použití Služeb sestavení jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="6a4dc-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6a4dc-595">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-595">Cost object</span></span></th>
<th><span data-ttu-id="6a4dc-596">Hodnota</span><span class="sxs-lookup"><span data-stu-id="6a4dc-596">Magnitude</span></span></th>
<th><span data-ttu-id="6a4dc-597">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-597">Allocation factor</span></span></th>
<th><span data-ttu-id="6a4dc-598">Částka</span><span class="sxs-lookup"><span data-stu-id="6a4dc-598">Amount</span></span></th>
<th><span data-ttu-id="6a4dc-599">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a4dc-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-600">Prod 1</span></span></td>
<td><span data-ttu-id="6a4dc-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-601">Product 1</span></span></td>
<td><span data-ttu-id="6a4dc-602">60</span><span class="sxs-lookup"><span data-stu-id="6a4dc-602">60</span></span></td>
<td><span data-ttu-id="6a4dc-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="6a4dc-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="6a4dc-604">535.31</span><span class="sxs-lookup"><span data-stu-id="6a4dc-604">535.31</span></span></td>
<td><span data-ttu-id="6a4dc-605">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-606">Prod 2</span></span></td>
<td><span data-ttu-id="6a4dc-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-607">Product 2</span></span></td>
<td><span data-ttu-id="6a4dc-608">20</span><span class="sxs-lookup"><span data-stu-id="6a4dc-608">20</span></span></td>
<td><span data-ttu-id="6a4dc-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="6a4dc-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="6a4dc-610">178.44</span><span class="sxs-lookup"><span data-stu-id="6a4dc-610">178.44</span></span></td>
<td><span data-ttu-id="6a4dc-611">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-612">Prod 1</span></span></td>
<td><span data-ttu-id="6a4dc-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-613">Product 1</span></span></td>
<td><span data-ttu-id="6a4dc-614">60</span><span class="sxs-lookup"><span data-stu-id="6a4dc-614">60</span></span></td>
<td><span data-ttu-id="6a4dc-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="6a4dc-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="6a4dc-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="6a4dc-616">4,487.12</span></span></td>
<td><span data-ttu-id="6a4dc-617">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-618">Prod 2</span></span></td>
<td><span data-ttu-id="6a4dc-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-619">Product 2</span></span></td>
<td><span data-ttu-id="6a4dc-620">20</span><span class="sxs-lookup"><span data-stu-id="6a4dc-620">20</span></span></td>
<td><span data-ttu-id="6a4dc-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="6a4dc-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="6a4dc-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="6a4dc-622">1,495.71</span></span></td>
<td><span data-ttu-id="6a4dc-623">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6a4dc-624">V následující tabulce je uveden výsledek při použití Služeb balení jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="6a4dc-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6a4dc-625">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-625">Cost object</span></span></th>
<th><span data-ttu-id="6a4dc-626">Hodnota</span><span class="sxs-lookup"><span data-stu-id="6a4dc-626">Magnitude</span></span></th>
<th><span data-ttu-id="6a4dc-627">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-627">Allocation factor</span></span></th>
<th><span data-ttu-id="6a4dc-628">Částka</span><span class="sxs-lookup"><span data-stu-id="6a4dc-628">Amount</span></span></th>
<th><span data-ttu-id="6a4dc-629">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a4dc-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-630">Prod 1</span></span></td>
<td><span data-ttu-id="6a4dc-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-631">Product 1</span></span></td>
<td><span data-ttu-id="6a4dc-632">80</span><span class="sxs-lookup"><span data-stu-id="6a4dc-632">80</span></span></td>
<td><span data-ttu-id="6a4dc-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="6a4dc-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="6a4dc-634">241.05</span><span class="sxs-lookup"><span data-stu-id="6a4dc-634">241.05</span></span></td>
<td><span data-ttu-id="6a4dc-635">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-636">Prod 2</span></span></td>
<td><span data-ttu-id="6a4dc-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-637">Product 2</span></span></td>
<td><span data-ttu-id="6a4dc-638">15</span><span class="sxs-lookup"><span data-stu-id="6a4dc-638">15</span></span></td>
<td><span data-ttu-id="6a4dc-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="6a4dc-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="6a4dc-640">45.20</span><span class="sxs-lookup"><span data-stu-id="6a4dc-640">45.20</span></span></td>
<td><span data-ttu-id="6a4dc-641">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-642">Prod 1</span></span></td>
<td><span data-ttu-id="6a4dc-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-643">Product 1</span></span></td>
<td><span data-ttu-id="6a4dc-644">80</span><span class="sxs-lookup"><span data-stu-id="6a4dc-644">80</span></span></td>
<td><span data-ttu-id="6a4dc-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="6a4dc-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="6a4dc-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="6a4dc-646">2,507.09</span></span></td>
<td><span data-ttu-id="6a4dc-647">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-648">Prod 2</span></span></td>
<td><span data-ttu-id="6a4dc-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-649">Product 2</span></span></td>
<td><span data-ttu-id="6a4dc-650">15</span><span class="sxs-lookup"><span data-stu-id="6a4dc-650">15</span></span></td>
<td><span data-ttu-id="6a4dc-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="6a4dc-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="6a4dc-652">470.08</span><span class="sxs-lookup"><span data-stu-id="6a4dc-652">470.08</span></span></td>
<td><span data-ttu-id="6a4dc-653">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="6a4dc-654">Položky deníku (položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="6a4dc-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6a4dc-655">Deník</span><span class="sxs-lookup"><span data-stu-id="6a4dc-655">Journal</span></span></th>
<th><span data-ttu-id="6a4dc-656">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="6a4dc-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6a4dc-657">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="6a4dc-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6a4dc-658">Verze</span><span class="sxs-lookup"><span data-stu-id="6a4dc-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a4dc-659">00004</span><span class="sxs-lookup"><span data-stu-id="6a4dc-659">00004</span></span></td>
<td><span data-ttu-id="6a4dc-660">Deník přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="6a4dc-661">Fiskální</span><span class="sxs-lookup"><span data-stu-id="6a4dc-661">Fiscal</span></span></td>
<td><span data-ttu-id="6a4dc-662">2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-662">2017</span></span></td>
<td><span data-ttu-id="6a4dc-663">Období 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-663">Period 1</span></span></td>
<td><span data-ttu-id="6a4dc-664">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="6a4dc-665">Řádky deníku</span><span class="sxs-lookup"><span data-stu-id="6a4dc-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6a4dc-666">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="6a4dc-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6a4dc-667">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6a4dc-668">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-668">Cost element</span></span></th>
<th><span data-ttu-id="6a4dc-669">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-669">Cost behavior</span></span></th>
<th><span data-ttu-id="6a4dc-670">Částka</span><span class="sxs-lookup"><span data-stu-id="6a4dc-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a4dc-671">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="6a4dc-672">CC001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-672">CC001</span></span></td>
<td><span data-ttu-id="6a4dc-673">HR</span><span class="sxs-lookup"><span data-stu-id="6a4dc-673">HR</span></span></td>
<td><span data-ttu-id="6a4dc-674">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-674">10001</span></span></td>
<td><span data-ttu-id="6a4dc-675">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-675">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-676">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-676">Fixed cost</span></span></td>
<td><span data-ttu-id="6a4dc-677">500.00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-678">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="6a4dc-679">CC001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-679">CC001</span></span></td>
<td><span data-ttu-id="6a4dc-680">HR</span><span class="sxs-lookup"><span data-stu-id="6a4dc-680">HR</span></span></td>
<td><span data-ttu-id="6a4dc-681">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-681">10001</span></span></td>
<td><span data-ttu-id="6a4dc-682">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-682">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-683">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-683">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="6a4dc-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-685">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="6a4dc-686">CC002</span><span class="sxs-lookup"><span data-stu-id="6a4dc-686">CC002</span></span></td>
<td><span data-ttu-id="6a4dc-687">Finance</span><span class="sxs-lookup"><span data-stu-id="6a4dc-687">Finance</span></span></td>
<td><span data-ttu-id="6a4dc-688">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-688">10001</span></span></td>
<td><span data-ttu-id="6a4dc-689">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-689">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-690">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-690">Fixed cost</span></span></td>
<td><span data-ttu-id="6a4dc-691">675.00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-692">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="6a4dc-693">CC002</span><span class="sxs-lookup"><span data-stu-id="6a4dc-693">CC002</span></span></td>
<td><span data-ttu-id="6a4dc-694">Finance</span><span class="sxs-lookup"><span data-stu-id="6a4dc-694">Finance</span></span></td>
<td><span data-ttu-id="6a4dc-695">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-695">10001</span></span></td>
<td><span data-ttu-id="6a4dc-696">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-696">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-697">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-697">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="6a4dc-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-699">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="6a4dc-700">CC003</span><span class="sxs-lookup"><span data-stu-id="6a4dc-700">CC003</span></span></td>
<td><span data-ttu-id="6a4dc-701">Sestavení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-701">Assembly</span></span></td>
<td><span data-ttu-id="6a4dc-702">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-702">10001</span></span></td>
<td><span data-ttu-id="6a4dc-703">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-703">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-704">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-704">Fixed cost</span></span></td>
<td><span data-ttu-id="6a4dc-705">713.75</span><span class="sxs-lookup"><span data-stu-id="6a4dc-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-706">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="6a4dc-707">CC003</span><span class="sxs-lookup"><span data-stu-id="6a4dc-707">CC003</span></span></td>
<td><span data-ttu-id="6a4dc-708">Sestavení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-708">Assembly</span></span></td>
<td><span data-ttu-id="6a4dc-709">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-709">10001</span></span></td>
<td><span data-ttu-id="6a4dc-710">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-710">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-711">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-711">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="6a4dc-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-713">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="6a4dc-714">CC003</span><span class="sxs-lookup"><span data-stu-id="6a4dc-714">CC003</span></span></td>
<td><span data-ttu-id="6a4dc-715">Balení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-715">Packaging</span></span></td>
<td><span data-ttu-id="6a4dc-716">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-716">10001</span></span></td>
<td><span data-ttu-id="6a4dc-717">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-717">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-718">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-718">Fixed cost</span></span></td>
<td><span data-ttu-id="6a4dc-719">286.25</span><span class="sxs-lookup"><span data-stu-id="6a4dc-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-720">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="6a4dc-721">CC003</span><span class="sxs-lookup"><span data-stu-id="6a4dc-721">CC003</span></span></td>
<td><span data-ttu-id="6a4dc-722">Balení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-722">Packaging</span></span></td>
<td><span data-ttu-id="6a4dc-723">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-723">10001</span></span></td>
<td><span data-ttu-id="6a4dc-724">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-724">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-725">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-725">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="6a4dc-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-727">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="6a4dc-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-728">Prod 1</span></span></td>
<td><span data-ttu-id="6a4dc-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-729">Product 1</span></span></td>
<td><span data-ttu-id="6a4dc-730">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-730">10001</span></span></td>
<td><span data-ttu-id="6a4dc-731">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-731">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-732">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-732">Fixed cost</span></span></td>
<td><span data-ttu-id="6a4dc-733">776.36</span><span class="sxs-lookup"><span data-stu-id="6a4dc-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-734">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="6a4dc-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-735">Prod 1</span></span></td>
<td><span data-ttu-id="6a4dc-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-736">Product 1</span></span></td>
<td><span data-ttu-id="6a4dc-737">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-737">10001</span></span></td>
<td><span data-ttu-id="6a4dc-738">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-738">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-739">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-739">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="6a4dc-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-741">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="6a4dc-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-742">Prod 2</span></span></td>
<td><span data-ttu-id="6a4dc-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-743">Product 1</span></span></td>
<td><span data-ttu-id="6a4dc-744">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-744">10001</span></span></td>
<td><span data-ttu-id="6a4dc-745">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-745">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-746">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-746">Fixed cost</span></span></td>
<td><span data-ttu-id="6a4dc-747">223.64</span><span class="sxs-lookup"><span data-stu-id="6a4dc-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-748">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="6a4dc-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-749">Prod 2</span></span></td>
<td><span data-ttu-id="6a4dc-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-750">Product 1</span></span></td>
<td><span data-ttu-id="6a4dc-751">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-751">10001</span></span></td>
<td><span data-ttu-id="6a4dc-752">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-752">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-753">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-753">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="6a4dc-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6a4dc-755">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6a4dc-756">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6a4dc-757">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-757">Cost element</span></span></th>
<th><span data-ttu-id="6a4dc-758">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-758">Cost behavior</span></span></th>
<th><span data-ttu-id="6a4dc-759">Částka</span><span class="sxs-lookup"><span data-stu-id="6a4dc-759">Amount</span></span></th>
<th><span data-ttu-id="6a4dc-760">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="6a4dc-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6a4dc-761">CC001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-761">CC001</span></span></td>
<td><span data-ttu-id="6a4dc-762">HR</span><span class="sxs-lookup"><span data-stu-id="6a4dc-762">HR</span></span></td>
<td><span data-ttu-id="6a4dc-763">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-763">10001</span></span></td>
<td><span data-ttu-id="6a4dc-764">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-764">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-765">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-765">Fixed cost</span></span></td>
<td><span data-ttu-id="6a4dc-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-766">-500.00</span></span></td>
<td><span data-ttu-id="6a4dc-767">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-768">CC002</span><span class="sxs-lookup"><span data-stu-id="6a4dc-768">CC002</span></span></td>
<td><span data-ttu-id="6a4dc-769">Finance</span><span class="sxs-lookup"><span data-stu-id="6a4dc-769">Finance</span></span></td>
<td><span data-ttu-id="6a4dc-770">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-770">10001</span></span></td>
<td><span data-ttu-id="6a4dc-771">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-771">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-772">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-772">Fixed cost</span></span></td>
<td><span data-ttu-id="6a4dc-773">175.00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-773">175.00</span></span></td>
<td><span data-ttu-id="6a4dc-774">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-775">CC003</span><span class="sxs-lookup"><span data-stu-id="6a4dc-775">CC003</span></span></td>
<td><span data-ttu-id="6a4dc-776">Sestavení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-776">Assembly</span></span></td>
<td><span data-ttu-id="6a4dc-777">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-777">10001</span></span></td>
<td><span data-ttu-id="6a4dc-778">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-778">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-779">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-779">Fixed cost</span></span></td>
<td><span data-ttu-id="6a4dc-780">275.00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-780">275.00</span></span></td>
<td><span data-ttu-id="6a4dc-781">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-782">CC004</span><span class="sxs-lookup"><span data-stu-id="6a4dc-782">CC004</span></span></td>
<td><span data-ttu-id="6a4dc-783">Balení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-783">Packaging</span></span></td>
<td><span data-ttu-id="6a4dc-784">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-784">10001</span></span></td>
<td><span data-ttu-id="6a4dc-785">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-785">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-786">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-786">Fixed cost</span></span></td>
<td><span data-ttu-id="6a4dc-787">50,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-787">50,00</span></span></td>
<td><span data-ttu-id="6a4dc-788">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-789">CC001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-789">CC001</span></span></td>
<td><span data-ttu-id="6a4dc-790">HR</span><span class="sxs-lookup"><span data-stu-id="6a4dc-790">HR</span></span></td>
<td><span data-ttu-id="6a4dc-791">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-791">10001</span></span></td>
<td><span data-ttu-id="6a4dc-792">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-792">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-793">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-793">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-794">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="6a4dc-794">-1,245.71</span></span></td>
<td><span data-ttu-id="6a4dc-795">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-796">CC002</span><span class="sxs-lookup"><span data-stu-id="6a4dc-796">CC002</span></span></td>
<td><span data-ttu-id="6a4dc-797">Finance</span><span class="sxs-lookup"><span data-stu-id="6a4dc-797">Finance</span></span></td>
<td><span data-ttu-id="6a4dc-798">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-798">10001</span></span></td>
<td><span data-ttu-id="6a4dc-799">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-799">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-800">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-800">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-801">436.00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-801">436.00</span></span></td>
<td><span data-ttu-id="6a4dc-802">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-803">CC003</span><span class="sxs-lookup"><span data-stu-id="6a4dc-803">CC003</span></span></td>
<td><span data-ttu-id="6a4dc-804">Sestavení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-804">Assembly</span></span></td>
<td><span data-ttu-id="6a4dc-805">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-805">10001</span></span></td>
<td><span data-ttu-id="6a4dc-806">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-806">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-807">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-807">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-808">685.14</span><span class="sxs-lookup"><span data-stu-id="6a4dc-808">685.14</span></span></td>
<td><span data-ttu-id="6a4dc-809">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-810">CC004</span><span class="sxs-lookup"><span data-stu-id="6a4dc-810">CC004</span></span></td>
<td><span data-ttu-id="6a4dc-811">Balení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-811">Packaging</span></span></td>
<td><span data-ttu-id="6a4dc-812">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-812">10001</span></span></td>
<td><span data-ttu-id="6a4dc-813">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-813">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-814">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-814">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-815">124.57</span><span class="sxs-lookup"><span data-stu-id="6a4dc-815">124.57</span></span></td>
<td><span data-ttu-id="6a4dc-816">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-817">CC002</span><span class="sxs-lookup"><span data-stu-id="6a4dc-817">CC002</span></span></td>
<td><span data-ttu-id="6a4dc-818">Finance</span><span class="sxs-lookup"><span data-stu-id="6a4dc-818">Finance</span></span></td>
<td><span data-ttu-id="6a4dc-819">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-819">10001</span></span></td>
<td><span data-ttu-id="6a4dc-820">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-820">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-821">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-821">Fixed cost</span></span></td>
<td><span data-ttu-id="6a4dc-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-822">-675.00</span></span></td>
<td><span data-ttu-id="6a4dc-823">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-824">CC003</span><span class="sxs-lookup"><span data-stu-id="6a4dc-824">CC003</span></span></td>
<td><span data-ttu-id="6a4dc-825">Sestavení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-825">Assembly</span></span></td>
<td><span data-ttu-id="6a4dc-826">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-826">10001</span></span></td>
<td><span data-ttu-id="6a4dc-827">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-827">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-828">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-828">Fixed cost</span></span></td>
<td><span data-ttu-id="6a4dc-829">438.75</span><span class="sxs-lookup"><span data-stu-id="6a4dc-829">438.75</span></span></td>
<td><span data-ttu-id="6a4dc-830">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-831">CC004</span><span class="sxs-lookup"><span data-stu-id="6a4dc-831">CC004</span></span></td>
<td><span data-ttu-id="6a4dc-832">Balení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-832">Packaging</span></span></td>
<td><span data-ttu-id="6a4dc-833">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-833">10001</span></span></td>
<td><span data-ttu-id="6a4dc-834">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-834">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-835">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-835">Fixed cost</span></span></td>
<td><span data-ttu-id="6a4dc-836">236.25</span><span class="sxs-lookup"><span data-stu-id="6a4dc-836">236.25</span></span></td>
<td><span data-ttu-id="6a4dc-837">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-838">CC002</span><span class="sxs-lookup"><span data-stu-id="6a4dc-838">CC002</span></span></td>
<td><span data-ttu-id="6a4dc-839">Finance</span><span class="sxs-lookup"><span data-stu-id="6a4dc-839">Finance</span></span></td>
<td><span data-ttu-id="6a4dc-840">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-840">10001</span></span></td>
<td><span data-ttu-id="6a4dc-841">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-841">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-842">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-842">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-843">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="6a4dc-843">-8,150.29</span></span></td>
<td><span data-ttu-id="6a4dc-844">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-845">CC003</span><span class="sxs-lookup"><span data-stu-id="6a4dc-845">CC003</span></span></td>
<td><span data-ttu-id="6a4dc-846">Sestavení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-846">Assembly</span></span></td>
<td><span data-ttu-id="6a4dc-847">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-847">10001</span></span></td>
<td><span data-ttu-id="6a4dc-848">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-848">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-849">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-849">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="6a4dc-850">5,297.69</span></span></td>
<td><span data-ttu-id="6a4dc-851">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-852">CC004</span><span class="sxs-lookup"><span data-stu-id="6a4dc-852">CC004</span></span></td>
<td><span data-ttu-id="6a4dc-853">Balení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-853">Packaging</span></span></td>
<td><span data-ttu-id="6a4dc-854">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-854">10001</span></span></td>
<td><span data-ttu-id="6a4dc-855">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-855">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-856">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-856">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="6a4dc-857">2,852.60</span></span></td>
<td><span data-ttu-id="6a4dc-858">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-859">CC003</span><span class="sxs-lookup"><span data-stu-id="6a4dc-859">CC003</span></span></td>
<td><span data-ttu-id="6a4dc-860">Sestavení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-860">Assembly</span></span></td>
<td><span data-ttu-id="6a4dc-861">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-861">10001</span></span></td>
<td><span data-ttu-id="6a4dc-862">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-862">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-863">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-863">Fixed cost</span></span></td>
<td><span data-ttu-id="6a4dc-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="6a4dc-864">-713.75</span></span></td>
<td><span data-ttu-id="6a4dc-865">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-866">Prod 1</span></span></td>
<td><span data-ttu-id="6a4dc-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-867">Product 1</span></span></td>
<td><span data-ttu-id="6a4dc-868">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-868">10001</span></span></td>
<td><span data-ttu-id="6a4dc-869">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-869">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-870">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-870">Fixed cost</span></span></td>
<td><span data-ttu-id="6a4dc-871">535.31</span><span class="sxs-lookup"><span data-stu-id="6a4dc-871">535.31</span></span></td>
<td><span data-ttu-id="6a4dc-872">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-873">Prod 2</span></span></td>
<td><span data-ttu-id="6a4dc-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-874">Product 2</span></span></td>
<td><span data-ttu-id="6a4dc-875">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-875">10001</span></span></td>
<td><span data-ttu-id="6a4dc-876">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-876">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-877">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-877">Fixed cost</span></span></td>
<td><span data-ttu-id="6a4dc-878">178.44</span><span class="sxs-lookup"><span data-stu-id="6a4dc-878">178.44</span></span></td>
<td><span data-ttu-id="6a4dc-879">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-880">CC003</span><span class="sxs-lookup"><span data-stu-id="6a4dc-880">CC003</span></span></td>
<td><span data-ttu-id="6a4dc-881">Sestavení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-881">Assembly</span></span></td>
<td><span data-ttu-id="6a4dc-882">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-882">10001</span></span></td>
<td><span data-ttu-id="6a4dc-883">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-883">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-884">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-884">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-885">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="6a4dc-885">-5,982.83</span></span></td>
<td><span data-ttu-id="6a4dc-886">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-887">Prod 1</span></span></td>
<td><span data-ttu-id="6a4dc-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-888">Product 1</span></span></td>
<td><span data-ttu-id="6a4dc-889">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-889">10001</span></span></td>
<td><span data-ttu-id="6a4dc-890">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-890">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-891">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-891">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="6a4dc-892">4,487.12</span></span></td>
<td><span data-ttu-id="6a4dc-893">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-894">Prod 2</span></span></td>
<td><span data-ttu-id="6a4dc-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-895">Product 2</span></span></td>
<td><span data-ttu-id="6a4dc-896">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-896">10001</span></span></td>
<td><span data-ttu-id="6a4dc-897">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-897">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-898">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-898">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="6a4dc-899">1,495.71</span></span></td>
<td><span data-ttu-id="6a4dc-900">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-901">CC003</span><span class="sxs-lookup"><span data-stu-id="6a4dc-901">CC003</span></span></td>
<td><span data-ttu-id="6a4dc-902">Sestavení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-902">Assembly</span></span></td>
<td><span data-ttu-id="6a4dc-903">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-903">10001</span></span></td>
<td><span data-ttu-id="6a4dc-904">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-904">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-905">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-905">Fixed cost</span></span></td>
<td><span data-ttu-id="6a4dc-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="6a4dc-906">-286.25</span></span></td>
<td><span data-ttu-id="6a4dc-907">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-908">Prod 1</span></span></td>
<td><span data-ttu-id="6a4dc-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-909">Product 1</span></span></td>
<td><span data-ttu-id="6a4dc-910">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-910">10001</span></span></td>
<td><span data-ttu-id="6a4dc-911">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-911">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-912">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-912">Fixed cost</span></span></td>
<td><span data-ttu-id="6a4dc-913">241.05</span><span class="sxs-lookup"><span data-stu-id="6a4dc-913">241.05</span></span></td>
<td><span data-ttu-id="6a4dc-914">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-915">Prod 2</span></span></td>
<td><span data-ttu-id="6a4dc-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-916">Product 2</span></span></td>
<td><span data-ttu-id="6a4dc-917">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-917">10001</span></span></td>
<td><span data-ttu-id="6a4dc-918">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-918">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-919">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-919">Fixed cost</span></span></td>
<td><span data-ttu-id="6a4dc-920">45.20</span><span class="sxs-lookup"><span data-stu-id="6a4dc-920">45.20</span></span></td>
<td><span data-ttu-id="6a4dc-921">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-922">CC003</span><span class="sxs-lookup"><span data-stu-id="6a4dc-922">CC003</span></span></td>
<td><span data-ttu-id="6a4dc-923">Sestavení</span><span class="sxs-lookup"><span data-stu-id="6a4dc-923">Assembly</span></span></td>
<td><span data-ttu-id="6a4dc-924">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-924">10001</span></span></td>
<td><span data-ttu-id="6a4dc-925">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-925">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-926">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-926">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="6a4dc-927">-2,977.17</span></span></td>
<td><span data-ttu-id="6a4dc-928">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-929">Prod 1</span></span></td>
<td><span data-ttu-id="6a4dc-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-930">Product 1</span></span></td>
<td><span data-ttu-id="6a4dc-931">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-931">10001</span></span></td>
<td><span data-ttu-id="6a4dc-932">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-932">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-933">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-933">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="6a4dc-934">2,507.09</span></span></td>
<td><span data-ttu-id="6a4dc-935">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6a4dc-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-936">Prod 2</span></span></td>
<td><span data-ttu-id="6a4dc-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-937">Product 2</span></span></td>
<td><span data-ttu-id="6a4dc-938">10001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-938">10001</span></span></td>
<td><span data-ttu-id="6a4dc-939">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="6a4dc-939">Electricity</span></span></td>
<td><span data-ttu-id="6a4dc-940">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-940">Variable cost</span></span></td>
<td><span data-ttu-id="6a4dc-941">470.08</span><span class="sxs-lookup"><span data-stu-id="6a4dc-941">470.08</span></span></td>
<td><span data-ttu-id="6a4dc-942">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="6a4dc-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="6a4dc-943">Závěr</span><span class="sxs-lookup"><span data-stu-id="6a4dc-943">Conclusion</span></span>
<span data-ttu-id="6a4dc-944">Ve finančním účtování se náklady za elektřinu ve výši 10 000 zaúčtují na ID fiktivního nákladového střediska.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="6a4dc-945">Účetní tak budou vědět, že tento náklad musí být přidělen.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="6a4dc-946">V nákladovém účetnictví náklady procházejí napříč organizačními jednotkami a úrovněmi, na základě použitých zásad a pravidel.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="6a4dc-947">Každý náklad byl přidružen k základu přidělení, který poskytuje nejlepší hodnocení pro přidělení nákladů.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="6a4dc-948">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="6a4dc-949">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="6a4dc-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="6a4dc-950">Celkem</span><span class="sxs-lookup"><span data-stu-id="6a4dc-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="6a4dc-951">CC099</span><span class="sxs-lookup"><span data-stu-id="6a4dc-951">CC099</span></span></th>
<th><span data-ttu-id="6a4dc-952">CC001</span><span class="sxs-lookup"><span data-stu-id="6a4dc-952">CC001</span></span></th>
<th><span data-ttu-id="6a4dc-953">CC002</span><span class="sxs-lookup"><span data-stu-id="6a4dc-953">CC002</span></span></th>
<th><span data-ttu-id="6a4dc-954">CC003</span><span class="sxs-lookup"><span data-stu-id="6a4dc-954">CC003</span></span></th>
<th><span data-ttu-id="6a4dc-955">CC004</span><span class="sxs-lookup"><span data-stu-id="6a4dc-955">CC004</span></span></th>
<th><span data-ttu-id="6a4dc-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-956">Proj 1</span></span></th>
<th><span data-ttu-id="6a4dc-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-957">Proj 2</span></span></th>
<th><span data-ttu-id="6a4dc-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6a4dc-958">Prod 1</span></span></th>
<th><span data-ttu-id="6a4dc-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6a4dc-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="6a4dc-960">10001 Elektřina</span><span class="sxs-lookup"><span data-stu-id="6a4dc-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6a4dc-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="6a4dc-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6a4dc-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="6a4dc-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6a4dc-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="6a4dc-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6a4dc-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="6a4dc-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="6a4dc-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="6a4dc-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6a4dc-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="6a4dc-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6a4dc-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="6a4dc-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6a4dc-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="6a4dc-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6a4dc-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="6a4dc-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="6a4dc-970">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="6a4dc-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6a4dc-971">0,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="6a4dc-972">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6a4dc-973">0,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6a4dc-974">0,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6a4dc-975">0,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6a4dc-976">0,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6a4dc-977">0,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="6a4dc-978">776.36</span><span class="sxs-lookup"><span data-stu-id="6a4dc-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6a4dc-979">223.64</span><span class="sxs-lookup"><span data-stu-id="6a4dc-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6a4dc-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="6a4dc-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="6a4dc-981">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="6a4dc-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6a4dc-982">000</span><span class="sxs-lookup"><span data-stu-id="6a4dc-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6a4dc-983">0,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6a4dc-984">0,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6a4dc-985">0,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6a4dc-986">0,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6a4dc-987">30.00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6a4dc-988">10,00</span><span class="sxs-lookup"><span data-stu-id="6a4dc-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6a4dc-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="6a4dc-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6a4dc-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="6a4dc-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6a4dc-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="6a4dc-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="6a4dc-992">Toto téma popisuje, jak primární prvek nákladů, 10001 Elektřina, prochází přes objekty nákladů.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="6a4dc-993">Tyto režijní náklady tedy budou přiděleny na nejnižší úroveň v organizaci.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="6a4dc-994">Jinak řečeno, objekty nákladů na nejnižší úrovni ponesou náklady.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="6a4dc-995">Chcete-li vizuální tok nákladů mezi objekty nákladů, můžete použít pravidla zásad shrnutí nákladů pro vizualizaci jejich toků.</span><span class="sxs-lookup"><span data-stu-id="6a4dc-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="6a4dc-996">Další informace naleznete v tématu [Zásady shrnutí nákladů a výpočet režijních nákladů](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="6a4dc-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



