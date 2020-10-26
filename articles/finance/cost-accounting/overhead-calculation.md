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
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976468"
---
# <a name="overhead-calculation"></a><span data-ttu-id="d9892-103">Výpočet režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9892-104">Toto téma popisuje typické procesy pro výpočet a přidělení režijních nákladů.</span><span class="sxs-lookup"><span data-stu-id="d9892-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="d9892-105">Definice termínu</span><span class="sxs-lookup"><span data-stu-id="d9892-105">Term definition</span></span>
---------------

<span data-ttu-id="d9892-106">Režijní náklady jsou náklady, které nutně vznikají při chodu podnikání, ale nelze je připsat přímo k žádné konkrétní podnikatelské aktivitě, produktu nebo službě.</span><span class="sxs-lookup"><span data-stu-id="d9892-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="d9892-107">Režijní náklady poskytují důležitou podporu pro generování aktivity přinášejících zisk.</span><span class="sxs-lookup"><span data-stu-id="d9892-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="d9892-108">Následuje několik příkladů režijních nákladů:</span><span class="sxs-lookup"><span data-stu-id="d9892-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="d9892-109">Renta</span><span class="sxs-lookup"><span data-stu-id="d9892-109">Rent</span></span>
-   <span data-ttu-id="d9892-110">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-110">Electricity</span></span>
-   <span data-ttu-id="d9892-111">Administrativní mzdy</span><span class="sxs-lookup"><span data-stu-id="d9892-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="d9892-112">Přehled výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-112">Overhead calculation overview</span></span>
<span data-ttu-id="d9892-113">Výpočet režijních nákladů spustí zásady účtování nákladů ve správném pořadí.</span><span class="sxs-lookup"><span data-stu-id="d9892-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="d9892-114">Výpočet režijních nákladů můžete pro stejné fiskální období spustit mnohokrát, pokud došlo ke změně zásad účtování nákladů nebo zjištění konkrétních chyb.</span><span class="sxs-lookup"><span data-stu-id="d9892-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="d9892-115">Každé spuštění výpočtu režijních nákladů se ukládá a přijímá ID jedinečné verze, které vám umožní porovnávat výpočty v různých verzích.</span><span class="sxs-lookup"><span data-stu-id="d9892-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="d9892-116">Položky nákladů, které generuje výpočet režijních nákladů, přijímá datum účtování.</span><span class="sxs-lookup"><span data-stu-id="d9892-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="d9892-117">Toto datum účtován se shoduje s konvovým datem fiskálního období, které se použije ve výpočtu.</span><span class="sxs-lookup"><span data-stu-id="d9892-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="d9892-118">ID jedinečné verze se skládá z následujících prvků:</span><span class="sxs-lookup"><span data-stu-id="d9892-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="d9892-119">Typ verze</span><span class="sxs-lookup"><span data-stu-id="d9892-119">Version type</span></span>
-   <span data-ttu-id="d9892-120">Datum a čas</span><span class="sxs-lookup"><span data-stu-id="d9892-120">Date and time</span></span>
-   <span data-ttu-id="d9892-121">Hlavní kniha nákladového účetnictví</span><span class="sxs-lookup"><span data-stu-id="d9892-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="d9892-122">Fiskální rok</span><span class="sxs-lookup"><span data-stu-id="d9892-122">Fiscal year</span></span>
-   <span data-ttu-id="d9892-123">Fiskální období</span><span class="sxs-lookup"><span data-stu-id="d9892-123">Fiscal period</span></span>

<span data-ttu-id="d9892-124">Výpočet režijních nákladů se spustí bez ohledu na verzi.</span><span class="sxs-lookup"><span data-stu-id="d9892-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="d9892-125">Proto lze vypočítat rozpočtovou verzi před skutečnou verzí.</span><span class="sxs-lookup"><span data-stu-id="d9892-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="d9892-126">Výpočet režijních nákladů se skládá ze čtyř kroků uvedených na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="d9892-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="d9892-127">V každé fázi je vytvořeno záhlaví deníku, které obsahuje položky deníku.</span><span class="sxs-lookup"><span data-stu-id="d9892-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="d9892-128">Toto záhlaví deníku zachovává vstupní data pro každý krok výpočtu.</span><span class="sxs-lookup"><span data-stu-id="d9892-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="d9892-129">Zásady a pravidla se použijí na každý řádek deníku a položky nákladů jsou generovány jako výstup.</span><span class="sxs-lookup"><span data-stu-id="d9892-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="d9892-130">Máte tedy vždy plnou sledovatelnost.</span><span class="sxs-lookup"><span data-stu-id="d9892-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="d9892-131">[![Výpočet režijních nákladů](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="d9892-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="d9892-132">Výpočet a přidělení režijních nákladů za elektřinu</span><span class="sxs-lookup"><span data-stu-id="d9892-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="d9892-133">Ve finančním účetnictví se některé náklady, jako je například elektřina, registrují jako paušální.</span><span class="sxs-lookup"><span data-stu-id="d9892-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="d9892-134">Podrobný přehled pro vedoucí není tedy pro nákladové účetnictví k dispozici.</span><span class="sxs-lookup"><span data-stu-id="d9892-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="d9892-135">V nákladovém účetnictví musí náklady procházet organizačními jednotkami, aby byl získán správný přehled pro vedoucí napříč všemi jednotkami a úrovněmi organizace.</span><span class="sxs-lookup"><span data-stu-id="d9892-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="d9892-136">Tento tok musí být založen buď na přesném záznamu spotřeby nebo na objektivním hodnocení.</span><span class="sxs-lookup"><span data-stu-id="d9892-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="d9892-137">V hlavní knize mohou být zaúčtovány náklady na elektřinu způsobem znázorněným v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="d9892-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d9892-138">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="d9892-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="d9892-139">Nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="d9892-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="d9892-140">Hlavní účet</span><span class="sxs-lookup"><span data-stu-id="d9892-140">Main account</span></span></th>
<th><span data-ttu-id="d9892-141">Částka v zúčtovací měně</span><span class="sxs-lookup"><span data-stu-id="d9892-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9892-142">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="d9892-143">CC099</span><span class="sxs-lookup"><span data-stu-id="d9892-143">CC099</span></span></td>
<td><span data-ttu-id="d9892-144">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="d9892-144">Default cost center</span></span></td>
<td><span data-ttu-id="d9892-145">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-145">10001</span></span></td>
<td><span data-ttu-id="d9892-146">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-146">Electricity</span></span></td>
<td><span data-ttu-id="d9892-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="d9892-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="d9892-148">Krok 1: Zpracování výpočtu chování nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="d9892-149">Ve výchozím nastavení dostanou při importu položek nákladů z datového zdroje tyto položky v nákladovém účetnictví klasifikaci **Neklasifikované** .</span><span class="sxs-lookup"><span data-stu-id="d9892-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="d9892-150">Použitím pravidla zásad chování nákladů lze reklasifikovat položky nákladů jako **Pevné náklady** nebo **Variabilní náklady** .</span><span class="sxs-lookup"><span data-stu-id="d9892-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost** .</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="d9892-151">Definice pravidel chování nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-151">Define the cost behavior rule</span></span>

<span data-ttu-id="d9892-152">V některých případech je část nákladů s pevným poplatkem a zbývající náklady jsou založeny na spotřebě.</span><span class="sxs-lookup"><span data-stu-id="d9892-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="d9892-153">Účty za elektřinu často odpovídají této definici.</span><span class="sxs-lookup"><span data-stu-id="d9892-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="d9892-154">Po platbě konkrétního pevného poplatku platíte spotřebu za kilowatthodinu (kWh).</span><span class="sxs-lookup"><span data-stu-id="d9892-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="d9892-155">Pokud je například poplatek pevných nákladů 1 000,00, definuje se pravidlo chování nákladů takto:</span><span class="sxs-lookup"><span data-stu-id="d9892-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="d9892-156">Pevná částka 1 000,00</span><span class="sxs-lookup"><span data-stu-id="d9892-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="d9892-157">0 &lt;= 1 000,00 = Pevná</span><span class="sxs-lookup"><span data-stu-id="d9892-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="d9892-158">1 000,01 &lt; N = Variabilní</span><span class="sxs-lookup"><span data-stu-id="d9892-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="d9892-159">Deník</span><span class="sxs-lookup"><span data-stu-id="d9892-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d9892-160">Deník</span><span class="sxs-lookup"><span data-stu-id="d9892-160">Journal</span></span></th>
<th><span data-ttu-id="d9892-161">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="d9892-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="d9892-162">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="d9892-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="d9892-163">Verze</span><span class="sxs-lookup"><span data-stu-id="d9892-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9892-164">00001</span><span class="sxs-lookup"><span data-stu-id="d9892-164">00001</span></span></td>
<td><span data-ttu-id="d9892-165">Deník výpočtu chování nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="d9892-166">Fiskální</span><span class="sxs-lookup"><span data-stu-id="d9892-166">Fiscal</span></span></td>
<td><span data-ttu-id="d9892-167">2017</span><span class="sxs-lookup"><span data-stu-id="d9892-167">2017</span></span></td>
<td><span data-ttu-id="d9892-168">Období 1</span><span class="sxs-lookup"><span data-stu-id="d9892-168">Period 1</span></span></td>
<td><span data-ttu-id="d9892-169">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="d9892-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="d9892-170">Položky deníku (Položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="d9892-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d9892-171">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="d9892-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="d9892-172">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d9892-173">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-173">Cost element</span></span></th>
<th><span data-ttu-id="d9892-174">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-174">Cost behavior</span></span></th>
<th><span data-ttu-id="d9892-175">Částka</span><span class="sxs-lookup"><span data-stu-id="d9892-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9892-176">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="d9892-177">CC099</span><span class="sxs-lookup"><span data-stu-id="d9892-177">CC099</span></span></td>
<td><span data-ttu-id="d9892-178">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="d9892-178">Default cost center</span></span></td>
<td><span data-ttu-id="d9892-179">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-179">10001</span></span></td>
<td><span data-ttu-id="d9892-180">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-180">Electricity</span></span></td>
<td><span data-ttu-id="d9892-181">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="d9892-181">Unclassified</span></span></td>
<td><span data-ttu-id="d9892-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="d9892-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="d9892-183">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d9892-184">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d9892-185">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-185">Cost element</span></span></th>
<th><span data-ttu-id="d9892-186">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-186">Cost behavior</span></span></th>
<th><span data-ttu-id="d9892-187">Částka</span><span class="sxs-lookup"><span data-stu-id="d9892-187">Amount</span></span></th>
<th><span data-ttu-id="d9892-188">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="d9892-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9892-189">CC099</span><span class="sxs-lookup"><span data-stu-id="d9892-189">CC099</span></span></td>
<td><span data-ttu-id="d9892-190">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="d9892-190">Default cost center</span></span></td>
<td><span data-ttu-id="d9892-191">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-191">10001</span></span></td>
<td><span data-ttu-id="d9892-192">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-192">Electricity</span></span></td>
<td><span data-ttu-id="d9892-193">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="d9892-193">Unclassified</span></span></td>
<td><span data-ttu-id="d9892-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="d9892-194">10,000.00</span></span></td>
<td><span data-ttu-id="d9892-195">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-196">CC099</span><span class="sxs-lookup"><span data-stu-id="d9892-196">CC099</span></span></td>
<td><span data-ttu-id="d9892-197">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="d9892-197">Default cost center</span></span></td>
<td><span data-ttu-id="d9892-198">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-198">10001</span></span></td>
<td><span data-ttu-id="d9892-199">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-199">Electricity</span></span></td>
<td><span data-ttu-id="d9892-200">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="d9892-200">Unclassified</span></span></td>
<td><span data-ttu-id="d9892-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="d9892-201">-10,000.00</span></span></td>
<td><span data-ttu-id="d9892-202">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-203">CC099</span><span class="sxs-lookup"><span data-stu-id="d9892-203">CC099</span></span></td>
<td><span data-ttu-id="d9892-204">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="d9892-204">Default cost center</span></span></td>
<td><span data-ttu-id="d9892-205">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-205">10001</span></span></td>
<td><span data-ttu-id="d9892-206">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-206">Electricity</span></span></td>
<td><span data-ttu-id="d9892-207">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-207">Fixed cost</span></span></td>
<td><span data-ttu-id="d9892-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="d9892-208">1,000.00</span></span></td>
<td><span data-ttu-id="d9892-209">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-210">CC099</span><span class="sxs-lookup"><span data-stu-id="d9892-210">CC099</span></span></td>
<td><span data-ttu-id="d9892-211">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="d9892-211">Default cost center</span></span></td>
<td><span data-ttu-id="d9892-212">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-212">10001</span></span></td>
<td><span data-ttu-id="d9892-213">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-213">Electricity</span></span></td>
<td><span data-ttu-id="d9892-214">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-214">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="d9892-215">9,000.00</span></span></td>
<td><span data-ttu-id="d9892-216">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d9892-217">Více informací naleznete v tématu [Vytvoření a přiřazení zásad chování nákladů k jednotce řízení nákladů](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="d9892-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="d9892-218">Krok 2: Zpracování výpočtu distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="d9892-219">Distribuce nákladů se používá k rozdělení nákladů z jednoho objektu nákladů na jeden nebo více dalších objektů nákladů použitím příslušného základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="d9892-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="d9892-220">Distribuce nákladů a přidělení nákladů se liší v tom, že k distribuci nákladů dochází vždy na úrovni primárního prvku nákladů původních nákladů.</span><span class="sxs-lookup"><span data-stu-id="d9892-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="d9892-221">Definice pravidel distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-221">Define the cost distribution rule</span></span>

<span data-ttu-id="d9892-222">Ve finančním účetnictví se náklady na elektřinu často registrují jako paušální.</span><span class="sxs-lookup"><span data-stu-id="d9892-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="d9892-223">V nákladovém účetnictví není tento přístup dostatečně podrobný.</span><span class="sxs-lookup"><span data-stu-id="d9892-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="d9892-224">Variabilní náklady by měly být distribuovány k jednotlivým objektům nákladů na solidním základě.</span><span class="sxs-lookup"><span data-stu-id="d9892-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="d9892-225">Nejlogičtější základ přidělení je spotřeba elektřiny (kWh).</span><span class="sxs-lookup"><span data-stu-id="d9892-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="d9892-226">Vytvoří se člen statistické dimenzi s názvem Elektřina a zaznamená se elektrické spotřeba.</span><span class="sxs-lookup"><span data-stu-id="d9892-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="d9892-227">Ve výchozím nastavení se všechny členy statistické dimenze stanou dostupnými zpřístupněny jako základy přidělení.</span><span class="sxs-lookup"><span data-stu-id="d9892-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d9892-228">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-228">Cost object</span></span></th>
<th><span data-ttu-id="d9892-229">kWh</span><span class="sxs-lookup"><span data-stu-id="d9892-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9892-230">CC001</span><span class="sxs-lookup"><span data-stu-id="d9892-230">CC001</span></span></td>
<td><span data-ttu-id="d9892-231">HR</span><span class="sxs-lookup"><span data-stu-id="d9892-231">HR</span></span></td>
<td><span data-ttu-id="d9892-232">1 000</span><span class="sxs-lookup"><span data-stu-id="d9892-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-233">CC002</span><span class="sxs-lookup"><span data-stu-id="d9892-233">CC002</span></span></td>
<td><span data-ttu-id="d9892-234">Finance</span><span class="sxs-lookup"><span data-stu-id="d9892-234">Finance</span></span></td>
<td><span data-ttu-id="d9892-235">6,000</span><span class="sxs-lookup"><span data-stu-id="d9892-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-236">CC003</span><span class="sxs-lookup"><span data-stu-id="d9892-236">CC003</span></span></td>
<td><span data-ttu-id="d9892-237">Sestavení</span><span class="sxs-lookup"><span data-stu-id="d9892-237">Assembly</span></span></td>
<td><span data-ttu-id="d9892-238">0</span><span class="sxs-lookup"><span data-stu-id="d9892-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d9892-239">Následující tabulka zobrazuje výsledek při použití elektrické spotřeby jako základu přidělení pro variabilní náklady.</span><span class="sxs-lookup"><span data-stu-id="d9892-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d9892-240">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-240">Cost object</span></span></th>
<th><span data-ttu-id="d9892-241">Hodnota</span><span class="sxs-lookup"><span data-stu-id="d9892-241">Magnitude</span></span></th>
<th><span data-ttu-id="d9892-242">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="d9892-242">Allocation factor</span></span></th>
<th><span data-ttu-id="d9892-243">Částka</span><span class="sxs-lookup"><span data-stu-id="d9892-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9892-244">CC001</span><span class="sxs-lookup"><span data-stu-id="d9892-244">CC001</span></span></td>
<td><span data-ttu-id="d9892-245">HR</span><span class="sxs-lookup"><span data-stu-id="d9892-245">HR</span></span></td>
<td><span data-ttu-id="d9892-246">1 000</span><span class="sxs-lookup"><span data-stu-id="d9892-246">1,000</span></span></td>
<td><span data-ttu-id="d9892-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="d9892-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="d9892-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="d9892-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-249">CC002</span><span class="sxs-lookup"><span data-stu-id="d9892-249">CC002</span></span></td>
<td><span data-ttu-id="d9892-250">Finance</span><span class="sxs-lookup"><span data-stu-id="d9892-250">Finance</span></span></td>
<td><span data-ttu-id="d9892-251">6,000</span><span class="sxs-lookup"><span data-stu-id="d9892-251">6,000</span></span></td>
<td><span data-ttu-id="d9892-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="d9892-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="d9892-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="d9892-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-254">CC003</span><span class="sxs-lookup"><span data-stu-id="d9892-254">CC003</span></span></td>
<td><span data-ttu-id="d9892-255">Sestavení</span><span class="sxs-lookup"><span data-stu-id="d9892-255">Assembly</span></span></td>
<td><span data-ttu-id="d9892-256">0</span><span class="sxs-lookup"><span data-stu-id="d9892-256">0</span></span></td>
<td><span data-ttu-id="d9892-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="d9892-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="d9892-258">0,00</span><span class="sxs-lookup"><span data-stu-id="d9892-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d9892-259">Pevné náklady musí být distribuovány rovnoměrně k jednotlivých objektům nákladů, které spotřebovávaly elektřinu.</span><span class="sxs-lookup"><span data-stu-id="d9892-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="d9892-260">Tohoto výsledku můžete dosáhnout pomocí členu statistické dimenze Elektřina v základu přidělení vzorce: (Elektřina &gt; 0,00) Následující tabulka zobrazuje výsledek při použití elektrické spotřeby jako základu přidělení pro variabilní náklady.</span><span class="sxs-lookup"><span data-stu-id="d9892-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d9892-261">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-261">Cost object</span></span></th>
<th><span data-ttu-id="d9892-262">Vzorec</span><span class="sxs-lookup"><span data-stu-id="d9892-262">Formula</span></span></th>
<th><span data-ttu-id="d9892-263">Hodnota</span><span class="sxs-lookup"><span data-stu-id="d9892-263">Magnitude</span></span></th>
<th><span data-ttu-id="d9892-264">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="d9892-264">Allocation factor</span></span></th>
<th><span data-ttu-id="d9892-265">Částka</span><span class="sxs-lookup"><span data-stu-id="d9892-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9892-266">CC001</span><span class="sxs-lookup"><span data-stu-id="d9892-266">CC001</span></span></td>
<td><span data-ttu-id="d9892-267">HR</span><span class="sxs-lookup"><span data-stu-id="d9892-267">HR</span></span></td>
<td><span data-ttu-id="d9892-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="d9892-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="d9892-269">1</span><span class="sxs-lookup"><span data-stu-id="d9892-269">1</span></span></td>
<td><span data-ttu-id="d9892-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="d9892-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="d9892-271">500.00</span><span class="sxs-lookup"><span data-stu-id="d9892-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-272">CC002</span><span class="sxs-lookup"><span data-stu-id="d9892-272">CC002</span></span></td>
<td><span data-ttu-id="d9892-273">Finance</span><span class="sxs-lookup"><span data-stu-id="d9892-273">Finance</span></span></td>
<td><span data-ttu-id="d9892-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="d9892-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="d9892-275">1</span><span class="sxs-lookup"><span data-stu-id="d9892-275">1</span></span></td>
<td><span data-ttu-id="d9892-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="d9892-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="d9892-277">500.00</span><span class="sxs-lookup"><span data-stu-id="d9892-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-278">CC003</span><span class="sxs-lookup"><span data-stu-id="d9892-278">CC003</span></span></td>
<td><span data-ttu-id="d9892-279">Sestavení</span><span class="sxs-lookup"><span data-stu-id="d9892-279">Assembly</span></span></td>
<td><span data-ttu-id="d9892-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="d9892-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="d9892-281">0</span><span class="sxs-lookup"><span data-stu-id="d9892-281">0</span></span></td>
<td><span data-ttu-id="d9892-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="d9892-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="d9892-283">0,00</span><span class="sxs-lookup"><span data-stu-id="d9892-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="d9892-284">Deník</span><span class="sxs-lookup"><span data-stu-id="d9892-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d9892-285">Deník</span><span class="sxs-lookup"><span data-stu-id="d9892-285">Journal</span></span></th>
<th><span data-ttu-id="d9892-286">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="d9892-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="d9892-287">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="d9892-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="d9892-288">Verze</span><span class="sxs-lookup"><span data-stu-id="d9892-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9892-289">00002</span><span class="sxs-lookup"><span data-stu-id="d9892-289">00002</span></span></td>
<td><span data-ttu-id="d9892-290">Deník výpočtu distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="d9892-291">Fiskální</span><span class="sxs-lookup"><span data-stu-id="d9892-291">Fiscal</span></span></td>
<td><span data-ttu-id="d9892-292">2017</span><span class="sxs-lookup"><span data-stu-id="d9892-292">2017</span></span></td>
<td><span data-ttu-id="d9892-293">Období 1</span><span class="sxs-lookup"><span data-stu-id="d9892-293">Period 1</span></span></td>
<td><span data-ttu-id="d9892-294">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="d9892-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="d9892-295">Položky deníku (Položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="d9892-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d9892-296">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="d9892-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="d9892-297">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d9892-298">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-298">Cost element</span></span></th>
<th><span data-ttu-id="d9892-299">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-299">Cost behavior</span></span></th>
<th><span data-ttu-id="d9892-300">Částka</span><span class="sxs-lookup"><span data-stu-id="d9892-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9892-301">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="d9892-302">CC099</span><span class="sxs-lookup"><span data-stu-id="d9892-302">CC099</span></span></td>
<td><span data-ttu-id="d9892-303">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="d9892-303">Default cost center</span></span></td>
<td><span data-ttu-id="d9892-304">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-304">10001</span></span></td>
<td><span data-ttu-id="d9892-305">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-305">Electricity</span></span></td>
<td><span data-ttu-id="d9892-306">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-306">Fixed cost</span></span></td>
<td><span data-ttu-id="d9892-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="d9892-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-308">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="d9892-309">CC099</span><span class="sxs-lookup"><span data-stu-id="d9892-309">CC099</span></span></td>
<td><span data-ttu-id="d9892-310">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="d9892-310">Default cost center</span></span></td>
<td><span data-ttu-id="d9892-311">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-311">10001</span></span></td>
<td><span data-ttu-id="d9892-312">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-312">Electricity</span></span></td>
<td><span data-ttu-id="d9892-313">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-313">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="d9892-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="d9892-315">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d9892-316">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d9892-317">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-317">Cost element</span></span></th>
<th><span data-ttu-id="d9892-318">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-318">Cost behavior</span></span></th>
<th><span data-ttu-id="d9892-319">Částka</span><span class="sxs-lookup"><span data-stu-id="d9892-319">Amount</span></span></th>
<th><span data-ttu-id="d9892-320">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="d9892-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9892-321">CC099</span><span class="sxs-lookup"><span data-stu-id="d9892-321">CC099</span></span></td>
<td><span data-ttu-id="d9892-322">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="d9892-322">Default cost center</span></span></td>
<td><span data-ttu-id="d9892-323">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-323">10001</span></span></td>
<td><span data-ttu-id="d9892-324">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-324">Electricity</span></span></td>
<td><span data-ttu-id="d9892-325">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-325">Fixed cost</span></span></td>
<td><span data-ttu-id="d9892-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="d9892-326">-1,000.00</span></span></td>
<td><span data-ttu-id="d9892-327">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-328">CC001</span><span class="sxs-lookup"><span data-stu-id="d9892-328">CC001</span></span></td>
<td><span data-ttu-id="d9892-329">HR</span><span class="sxs-lookup"><span data-stu-id="d9892-329">HR</span></span></td>
<td><span data-ttu-id="d9892-330">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-330">10001</span></span></td>
<td><span data-ttu-id="d9892-331">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-331">Electricity</span></span></td>
<td><span data-ttu-id="d9892-332">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-332">Fixed cost</span></span></td>
<td><span data-ttu-id="d9892-333">500.00</span><span class="sxs-lookup"><span data-stu-id="d9892-333">500.00</span></span></td>
<td><span data-ttu-id="d9892-334">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-335">CC002</span><span class="sxs-lookup"><span data-stu-id="d9892-335">CC002</span></span></td>
<td><span data-ttu-id="d9892-336">Finance</span><span class="sxs-lookup"><span data-stu-id="d9892-336">Finance</span></span></td>
<td><span data-ttu-id="d9892-337">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-337">10001</span></span></td>
<td><span data-ttu-id="d9892-338">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-338">Electricity</span></span></td>
<td><span data-ttu-id="d9892-339">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-339">Fixed cost</span></span></td>
<td><span data-ttu-id="d9892-340">500.00</span><span class="sxs-lookup"><span data-stu-id="d9892-340">500.00</span></span></td>
<td><span data-ttu-id="d9892-341">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-342">CC099</span><span class="sxs-lookup"><span data-stu-id="d9892-342">CC099</span></span></td>
<td><span data-ttu-id="d9892-343">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="d9892-343">Default cost center</span></span></td>
<td><span data-ttu-id="d9892-344">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-344">10001</span></span></td>
<td><span data-ttu-id="d9892-345">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-345">Electricity</span></span></td>
<td><span data-ttu-id="d9892-346">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-346">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-347">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="d9892-347">-9,000.00</span></span></td>
<td><span data-ttu-id="d9892-348">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-349">CC001</span><span class="sxs-lookup"><span data-stu-id="d9892-349">CC001</span></span></td>
<td><span data-ttu-id="d9892-350">HR</span><span class="sxs-lookup"><span data-stu-id="d9892-350">HR</span></span></td>
<td><span data-ttu-id="d9892-351">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-351">10001</span></span></td>
<td><span data-ttu-id="d9892-352">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-352">Electricity</span></span></td>
<td><span data-ttu-id="d9892-353">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-353">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="d9892-354">1,285.71</span></span></td>
<td><span data-ttu-id="d9892-355">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-356">CC002</span><span class="sxs-lookup"><span data-stu-id="d9892-356">CC002</span></span></td>
<td><span data-ttu-id="d9892-357">Finance</span><span class="sxs-lookup"><span data-stu-id="d9892-357">Finance</span></span></td>
<td><span data-ttu-id="d9892-358">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-358">10001</span></span></td>
<td><span data-ttu-id="d9892-359">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-359">Electricity</span></span></td>
<td><span data-ttu-id="d9892-360">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-360">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="d9892-361">7,714.29</span></span></td>
<td><span data-ttu-id="d9892-362">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d9892-363">Více informací naleznete v tématu [Vytvoření a přiřazení zásad distribuce nákladů k jednotce řízení nákladů](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="d9892-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="d9892-364">Krok 3: Zpracování výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="d9892-365">Režijní náklady se používají k účtování jednoho nebo více konkrétních objektů nákladů.</span><span class="sxs-lookup"><span data-stu-id="d9892-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="d9892-366">Účtování je založeno na předem určené nákladové sazbě a množství z přiřazeného základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="d9892-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="d9892-367">Definice sazby režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-367">Define the overhead rate</span></span>

<span data-ttu-id="d9892-368">Objekt nákladů CC001 HR přispívá k sadě interních projektů.</span><span class="sxs-lookup"><span data-stu-id="d9892-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="d9892-369">Vytvoří se člen statistické dimenzi s názvem projekty lidských zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="d9892-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d9892-370">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-370">Cost object</span></span></th>
<th><span data-ttu-id="d9892-371">Pracovní doba</span><span class="sxs-lookup"><span data-stu-id="d9892-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9892-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="d9892-372">Proj 1</span></span></td>
<td><span data-ttu-id="d9892-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="d9892-373">Project 1</span></span></td>
<td><span data-ttu-id="d9892-374">3</span><span class="sxs-lookup"><span data-stu-id="d9892-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="d9892-375">Proj 2</span></span></td>
<td><span data-ttu-id="d9892-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="d9892-376">Project 2</span></span></td>
<td><span data-ttu-id="d9892-377">1</span><span class="sxs-lookup"><span data-stu-id="d9892-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d9892-378">Byla definována předem určená nákladová sazba pro příspěvky k nákladovým projektům.</span><span class="sxs-lookup"><span data-stu-id="d9892-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d9892-379">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-379">Cost object</span></span></th>
<th><span data-ttu-id="d9892-380">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-380">Cost element</span></span></th>
<th><span data-ttu-id="d9892-381">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-381">Cost behavior</span></span></th>
<th><span data-ttu-id="d9892-382">Jednotky</span><span class="sxs-lookup"><span data-stu-id="d9892-382">Units</span></span></th>
<th><span data-ttu-id="d9892-383">Kurz</span><span class="sxs-lookup"><span data-stu-id="d9892-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9892-384">CC001</span><span class="sxs-lookup"><span data-stu-id="d9892-384">CC001</span></span></td>
<td><span data-ttu-id="d9892-385">HR</span><span class="sxs-lookup"><span data-stu-id="d9892-385">HR</span></span></td>
<td><span data-ttu-id="d9892-386">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-386">10001</span></span></td>
<td><span data-ttu-id="d9892-387">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-387">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-388">1</span><span class="sxs-lookup"><span data-stu-id="d9892-388">1</span></span></td>
<td><span data-ttu-id="d9892-389">10</span><span class="sxs-lookup"><span data-stu-id="d9892-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d9892-390">Následující tabulka zobrazuje výsledek při použití projektů lidských zdrojů jako základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="d9892-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d9892-391">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-391">Cost object</span></span></th>
<th><span data-ttu-id="d9892-392">Hodnota</span><span class="sxs-lookup"><span data-stu-id="d9892-392">Magnitude</span></span></th>
<th><span data-ttu-id="d9892-393">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-393">Cost element</span></span></th>
<th><span data-ttu-id="d9892-394">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="d9892-394">Allocation factor</span></span></th>
<th><span data-ttu-id="d9892-395">Částka</span><span class="sxs-lookup"><span data-stu-id="d9892-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9892-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="d9892-396">Proj 1</span></span></td>
<td><span data-ttu-id="d9892-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="d9892-397">Project 1</span></span></td>
<td><span data-ttu-id="d9892-398">3</span><span class="sxs-lookup"><span data-stu-id="d9892-398">3</span></span></td>
<td><span data-ttu-id="d9892-399">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-399">10001</span></span></td>
<td><span data-ttu-id="d9892-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="d9892-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="d9892-401">30.00</span><span class="sxs-lookup"><span data-stu-id="d9892-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="d9892-402">Proj 2</span></span></td>
<td><span data-ttu-id="d9892-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="d9892-403">Project 2</span></span></td>
<td><span data-ttu-id="d9892-404">1</span><span class="sxs-lookup"><span data-stu-id="d9892-404">1</span></span></td>
<td><span data-ttu-id="d9892-405">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-405">10001</span></span></td>
<td><span data-ttu-id="d9892-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="d9892-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="d9892-407">10,00</span><span class="sxs-lookup"><span data-stu-id="d9892-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="d9892-408">Deník</span><span class="sxs-lookup"><span data-stu-id="d9892-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d9892-409">Deník</span><span class="sxs-lookup"><span data-stu-id="d9892-409">Journal</span></span></th>
<th><span data-ttu-id="d9892-410">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="d9892-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="d9892-411">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="d9892-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="d9892-412">Verze</span><span class="sxs-lookup"><span data-stu-id="d9892-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9892-413">00003</span><span class="sxs-lookup"><span data-stu-id="d9892-413">00003</span></span></td>
<td><span data-ttu-id="d9892-414">Deník výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="d9892-415">Fiskální</span><span class="sxs-lookup"><span data-stu-id="d9892-415">Fiscal</span></span></td>
<td><span data-ttu-id="d9892-416">2017</span><span class="sxs-lookup"><span data-stu-id="d9892-416">2017</span></span></td>
<td><span data-ttu-id="d9892-417">Období 1</span><span class="sxs-lookup"><span data-stu-id="d9892-417">Period 1</span></span></td>
<td><span data-ttu-id="d9892-418">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="d9892-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="d9892-419">Položky deníku (položky deníku pro výpočet sazby režijních nákladů)</span><span class="sxs-lookup"><span data-stu-id="d9892-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d9892-420">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="d9892-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="d9892-421">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-421">Cost object</span></span></th>
<th><span data-ttu-id="d9892-422">Hodnota</span><span class="sxs-lookup"><span data-stu-id="d9892-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9892-423">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="d9892-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="d9892-424">Proj 1</span></span></td>
<td><span data-ttu-id="d9892-425">Interní projekt 1</span><span class="sxs-lookup"><span data-stu-id="d9892-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="d9892-426">3,00</span><span class="sxs-lookup"><span data-stu-id="d9892-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-427">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="d9892-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="d9892-428">Proj 2</span></span></td>
<td><span data-ttu-id="d9892-429">Interní projekt 2</span><span class="sxs-lookup"><span data-stu-id="d9892-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="d9892-430">1.00</span><span class="sxs-lookup"><span data-stu-id="d9892-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="d9892-431">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d9892-432">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d9892-433">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-433">Cost element</span></span></th>
<th><span data-ttu-id="d9892-434">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-434">Cost behavior</span></span></th>
<th><span data-ttu-id="d9892-435">Částka</span><span class="sxs-lookup"><span data-stu-id="d9892-435">Amount</span></span></th>
<th><span data-ttu-id="d9892-436">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="d9892-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9892-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="d9892-437">CC0001</span></span></td>
<td><span data-ttu-id="d9892-438">HR</span><span class="sxs-lookup"><span data-stu-id="d9892-438">HR</span></span></td>
<td><span data-ttu-id="d9892-439">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-439">10001</span></span></td>
<td><span data-ttu-id="d9892-440">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-440">Electricity</span></span></td>
<td><span data-ttu-id="d9892-441">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-441">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="d9892-442">-30.00</span></span></td>
<td><span data-ttu-id="d9892-443">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="d9892-444">Proj 1</span></span></td>
<td><span data-ttu-id="d9892-445">Interní projekt 1</span><span class="sxs-lookup"><span data-stu-id="d9892-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="d9892-446">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-446">10001</span></span></td>
<td><span data-ttu-id="d9892-447">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-447">Electricity</span></span></td>
<td><span data-ttu-id="d9892-448">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-448">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-449">30.00</span><span class="sxs-lookup"><span data-stu-id="d9892-449">30.00</span></span></td>
<td><span data-ttu-id="d9892-450">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-451">CC001</span><span class="sxs-lookup"><span data-stu-id="d9892-451">CC001</span></span></td>
<td><span data-ttu-id="d9892-452">HR</span><span class="sxs-lookup"><span data-stu-id="d9892-452">HR</span></span></td>
<td><span data-ttu-id="d9892-453">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-453">10001</span></span></td>
<td><span data-ttu-id="d9892-454">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-454">Electricity</span></span></td>
<td><span data-ttu-id="d9892-455">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-455">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="d9892-456">-10.00</span></span></td>
<td><span data-ttu-id="d9892-457">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="d9892-458">Proj 2</span></span></td>
<td><span data-ttu-id="d9892-459">Interní projekt 2</span><span class="sxs-lookup"><span data-stu-id="d9892-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="d9892-460">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-460">10001</span></span></td>
<td><span data-ttu-id="d9892-461">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-461">Electricity</span></span></td>
<td><span data-ttu-id="d9892-462">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-462">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-463">10.00</span><span class="sxs-lookup"><span data-stu-id="d9892-463">10.00</span></span></td>
<td><span data-ttu-id="d9892-464">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d9892-465">Další informace naleznete v tématu [Provedení výpočtu režijních nákladů](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="d9892-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="d9892-466">Krok 4: Zpracování výpočtu přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="d9892-467">Přidělení se používá k přidělení zůstatku objektu nákladů do jiných objektů nákladů použitím základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="d9892-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="d9892-468">Aplikace Finance podporuje reciproční metodu přidělování.</span><span class="sxs-lookup"><span data-stu-id="d9892-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="d9892-469">V metodě vzájemného přidělení jsou plně rozpoznány vzájemné služby, které si vyměňují pomocné objekty nákladů.</span><span class="sxs-lookup"><span data-stu-id="d9892-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="d9892-470">Systém automaticky určí provádění přidělení ve správném pořadí.</span><span class="sxs-lookup"><span data-stu-id="d9892-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="d9892-471">Zůstatek objektu nákladů je přidělen jedním základem přidělení.</span><span class="sxs-lookup"><span data-stu-id="d9892-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="d9892-472">Je podporováno přidělování napříč dimenzemi objektů nákladů a jejich příslušných členů.</span><span class="sxs-lookup"><span data-stu-id="d9892-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="d9892-473">Pořadí přidělení je řízeno jednotkou řízení nákladů.</span><span class="sxs-lookup"><span data-stu-id="d9892-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="d9892-474">[![Reciproční metoda](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="d9892-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="d9892-475">Definice přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-475">Define the cost allocation</span></span>

<span data-ttu-id="d9892-476">Toto je jednoduchý příklad, který vysvětluje, jakým způsobem lze sledovat tok nákladů.</span><span class="sxs-lookup"><span data-stu-id="d9892-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="d9892-477">Objekt nákladů objektu CC001 HR přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="d9892-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="d9892-478">Vytvoří se člen statistické dimenzi s názvem služby lidských zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="d9892-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d9892-479">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-479">Cost object</span></span></th>
<th><span data-ttu-id="d9892-480">Služby HR</span><span class="sxs-lookup"><span data-stu-id="d9892-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9892-481">CC002</span><span class="sxs-lookup"><span data-stu-id="d9892-481">CC002</span></span></td>
<td><span data-ttu-id="d9892-482">Finance</span><span class="sxs-lookup"><span data-stu-id="d9892-482">Finance</span></span></td>
<td><span data-ttu-id="d9892-483">35</span><span class="sxs-lookup"><span data-stu-id="d9892-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-484">CC003</span><span class="sxs-lookup"><span data-stu-id="d9892-484">CC003</span></span></td>
<td><span data-ttu-id="d9892-485">Sestavení</span><span class="sxs-lookup"><span data-stu-id="d9892-485">Assembly</span></span></td>
<td><span data-ttu-id="d9892-486">55</span><span class="sxs-lookup"><span data-stu-id="d9892-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-487">CC004</span><span class="sxs-lookup"><span data-stu-id="d9892-487">CC004</span></span></td>
<td><span data-ttu-id="d9892-488">Balení</span><span class="sxs-lookup"><span data-stu-id="d9892-488">Packaging</span></span></td>
<td><span data-ttu-id="d9892-489">10</span><span class="sxs-lookup"><span data-stu-id="d9892-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d9892-490">Objekt nákladů objektu CC002 Finance přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="d9892-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="d9892-491">Vytvoří se člen statistické dimenzi s názvem Finanční služby k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="d9892-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d9892-492">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-492">Cost object</span></span></th>
<th><span data-ttu-id="d9892-493">Finanční služby</span><span class="sxs-lookup"><span data-stu-id="d9892-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9892-494">CC003</span><span class="sxs-lookup"><span data-stu-id="d9892-494">CC003</span></span></td>
<td><span data-ttu-id="d9892-495">Sestavení</span><span class="sxs-lookup"><span data-stu-id="d9892-495">Assembly</span></span></td>
<td><span data-ttu-id="d9892-496">65</span><span class="sxs-lookup"><span data-stu-id="d9892-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-497">CC004</span><span class="sxs-lookup"><span data-stu-id="d9892-497">CC004</span></span></td>
<td><span data-ttu-id="d9892-498">Balení</span><span class="sxs-lookup"><span data-stu-id="d9892-498">Packaging</span></span></td>
<td><span data-ttu-id="d9892-499">35</span><span class="sxs-lookup"><span data-stu-id="d9892-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d9892-500">Objekt nákladů objektu CC003 Sestavení přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="d9892-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="d9892-501">Vytvoří se člen statistické dimenzi s názvem Služby sestavení zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="d9892-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d9892-502">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-502">Cost object</span></span></th>
<th><span data-ttu-id="d9892-503">Služby sestavení (v hodinách)</span><span class="sxs-lookup"><span data-stu-id="d9892-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9892-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d9892-504">Prod 1</span></span></td>
<td><span data-ttu-id="d9892-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="d9892-505">Product 1</span></span></td>
<td><span data-ttu-id="d9892-506">60</span><span class="sxs-lookup"><span data-stu-id="d9892-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d9892-507">Prod 2</span></span></td>
<td><span data-ttu-id="d9892-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="d9892-508">Product 2</span></span></td>
<td><span data-ttu-id="d9892-509">20</span><span class="sxs-lookup"><span data-stu-id="d9892-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d9892-510">Objekt nákladů objektu CC004 Balení přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="d9892-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="d9892-511">Vytvoří se člen statistické dimenzi s názvem Služby balení k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="d9892-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d9892-512">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-512">Cost object</span></span></th>
<th><span data-ttu-id="d9892-513">Služby balení (v hodinách)</span><span class="sxs-lookup"><span data-stu-id="d9892-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9892-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d9892-514">Prod 1</span></span></td>
<td><span data-ttu-id="d9892-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="d9892-515">Product 1</span></span></td>
<td><span data-ttu-id="d9892-516">80</span><span class="sxs-lookup"><span data-stu-id="d9892-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d9892-517">Prod 2</span></span></td>
<td><span data-ttu-id="d9892-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="d9892-518">Product 2</span></span></td>
<td><span data-ttu-id="d9892-519">15</span><span class="sxs-lookup"><span data-stu-id="d9892-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="d9892-520">Statistická měření, jako je například výrobní doba spotřebovaná produktem, lze odvodit z datového zdroje.</span><span class="sxs-lookup"><span data-stu-id="d9892-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="d9892-521">Více informací naleznete v části [Šablona poskytovatele statistického měření](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="d9892-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="d9892-522">V následující tabulce je uveden výsledek při použití služeb HR jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="d9892-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d9892-523">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-523">Cost object</span></span></th>
<th><span data-ttu-id="d9892-524">Hodnota</span><span class="sxs-lookup"><span data-stu-id="d9892-524">Magnitude</span></span></th>
<th><span data-ttu-id="d9892-525">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="d9892-525">Allocation factor</span></span></th>
<th><span data-ttu-id="d9892-526">Částka</span><span class="sxs-lookup"><span data-stu-id="d9892-526">Amount</span></span></th>
<th><span data-ttu-id="d9892-527">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9892-528">CC002</span><span class="sxs-lookup"><span data-stu-id="d9892-528">CC002</span></span></td>
<td><span data-ttu-id="d9892-529">Finance</span><span class="sxs-lookup"><span data-stu-id="d9892-529">Finance</span></span></td>
<td><span data-ttu-id="d9892-530">35</span><span class="sxs-lookup"><span data-stu-id="d9892-530">35</span></span></td>
<td><span data-ttu-id="d9892-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="d9892-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="d9892-532">175.00</span><span class="sxs-lookup"><span data-stu-id="d9892-532">175.00</span></span></td>
<td><span data-ttu-id="d9892-533">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-534">CC003</span><span class="sxs-lookup"><span data-stu-id="d9892-534">CC003</span></span></td>
<td><span data-ttu-id="d9892-535">Sestavení</span><span class="sxs-lookup"><span data-stu-id="d9892-535">Assembly</span></span></td>
<td><span data-ttu-id="d9892-536">55</span><span class="sxs-lookup"><span data-stu-id="d9892-536">55</span></span></td>
<td><span data-ttu-id="d9892-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="d9892-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="d9892-538">275.00</span><span class="sxs-lookup"><span data-stu-id="d9892-538">275.00</span></span></td>
<td><span data-ttu-id="d9892-539">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-540">CC004</span><span class="sxs-lookup"><span data-stu-id="d9892-540">CC004</span></span></td>
<td><span data-ttu-id="d9892-541">Balení</span><span class="sxs-lookup"><span data-stu-id="d9892-541">Packaging</span></span></td>
<td><span data-ttu-id="d9892-542">10</span><span class="sxs-lookup"><span data-stu-id="d9892-542">10</span></span></td>
<td><span data-ttu-id="d9892-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="d9892-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="d9892-544">50,00</span><span class="sxs-lookup"><span data-stu-id="d9892-544">50.00</span></span></td>
<td><span data-ttu-id="d9892-545">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-546">CC002</span><span class="sxs-lookup"><span data-stu-id="d9892-546">CC002</span></span></td>
<td><span data-ttu-id="d9892-547">Finance</span><span class="sxs-lookup"><span data-stu-id="d9892-547">Finance</span></span></td>
<td><span data-ttu-id="d9892-548">35</span><span class="sxs-lookup"><span data-stu-id="d9892-548">35</span></span></td>
<td><span data-ttu-id="d9892-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="d9892-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="d9892-550">436.00</span><span class="sxs-lookup"><span data-stu-id="d9892-550">436.00</span></span></td>
<td><span data-ttu-id="d9892-551">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-552">CC003</span><span class="sxs-lookup"><span data-stu-id="d9892-552">CC003</span></span></td>
<td><span data-ttu-id="d9892-553">Sestavení</span><span class="sxs-lookup"><span data-stu-id="d9892-553">Assembly</span></span></td>
<td><span data-ttu-id="d9892-554">55</span><span class="sxs-lookup"><span data-stu-id="d9892-554">55</span></span></td>
<td><span data-ttu-id="d9892-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="d9892-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="d9892-556">685.14</span><span class="sxs-lookup"><span data-stu-id="d9892-556">685.14</span></span></td>
<td><span data-ttu-id="d9892-557">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-558">CC004</span><span class="sxs-lookup"><span data-stu-id="d9892-558">CC004</span></span></td>
<td><span data-ttu-id="d9892-559">Balení</span><span class="sxs-lookup"><span data-stu-id="d9892-559">Packaging</span></span></td>
<td><span data-ttu-id="d9892-560">10</span><span class="sxs-lookup"><span data-stu-id="d9892-560">10</span></span></td>
<td><span data-ttu-id="d9892-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="d9892-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="d9892-562">124.57</span><span class="sxs-lookup"><span data-stu-id="d9892-562">124.57</span></span></td>
<td><span data-ttu-id="d9892-563">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d9892-564">V následující tabulce je uveden výsledek při použití Finančních služeb Finance jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="d9892-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d9892-565">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-565">Cost object</span></span></th>
<th><span data-ttu-id="d9892-566">Hodnota</span><span class="sxs-lookup"><span data-stu-id="d9892-566">Magnitude</span></span></th>
<th><span data-ttu-id="d9892-567">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="d9892-567">Allocation factor</span></span></th>
<th><span data-ttu-id="d9892-568">Částka</span><span class="sxs-lookup"><span data-stu-id="d9892-568">Amount</span></span></th>
<th><span data-ttu-id="d9892-569">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9892-570">CC003</span><span class="sxs-lookup"><span data-stu-id="d9892-570">CC003</span></span></td>
<td><span data-ttu-id="d9892-571">Sestavení</span><span class="sxs-lookup"><span data-stu-id="d9892-571">Assembly</span></span></td>
<td><span data-ttu-id="d9892-572">65</span><span class="sxs-lookup"><span data-stu-id="d9892-572">65</span></span></td>
<td><span data-ttu-id="d9892-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="d9892-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="d9892-574">438.75</span><span class="sxs-lookup"><span data-stu-id="d9892-574">438.75</span></span></td>
<td><span data-ttu-id="d9892-575">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-576">CC004</span><span class="sxs-lookup"><span data-stu-id="d9892-576">CC004</span></span></td>
<td><span data-ttu-id="d9892-577">Balení</span><span class="sxs-lookup"><span data-stu-id="d9892-577">Packaging</span></span></td>
<td><span data-ttu-id="d9892-578">35</span><span class="sxs-lookup"><span data-stu-id="d9892-578">35</span></span></td>
<td><span data-ttu-id="d9892-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="d9892-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="d9892-580">236.25</span><span class="sxs-lookup"><span data-stu-id="d9892-580">236.25</span></span></td>
<td><span data-ttu-id="d9892-581">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-582">CC003</span><span class="sxs-lookup"><span data-stu-id="d9892-582">CC003</span></span></td>
<td><span data-ttu-id="d9892-583">Sestavení</span><span class="sxs-lookup"><span data-stu-id="d9892-583">Assembly</span></span></td>
<td><span data-ttu-id="d9892-584">65</span><span class="sxs-lookup"><span data-stu-id="d9892-584">65</span></span></td>
<td><span data-ttu-id="d9892-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="d9892-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="d9892-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="d9892-586">5,297.69</span></span></td>
<td><span data-ttu-id="d9892-587">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-588">CC004</span><span class="sxs-lookup"><span data-stu-id="d9892-588">CC004</span></span></td>
<td><span data-ttu-id="d9892-589">Balení</span><span class="sxs-lookup"><span data-stu-id="d9892-589">Packaging</span></span></td>
<td><span data-ttu-id="d9892-590">35</span><span class="sxs-lookup"><span data-stu-id="d9892-590">35</span></span></td>
<td><span data-ttu-id="d9892-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="d9892-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="d9892-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="d9892-592">2,852.60</span></span></td>
<td><span data-ttu-id="d9892-593">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d9892-594">V následující tabulce je uveden výsledek při použití Služeb sestavení jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="d9892-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d9892-595">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-595">Cost object</span></span></th>
<th><span data-ttu-id="d9892-596">Hodnota</span><span class="sxs-lookup"><span data-stu-id="d9892-596">Magnitude</span></span></th>
<th><span data-ttu-id="d9892-597">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="d9892-597">Allocation factor</span></span></th>
<th><span data-ttu-id="d9892-598">Částka</span><span class="sxs-lookup"><span data-stu-id="d9892-598">Amount</span></span></th>
<th><span data-ttu-id="d9892-599">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9892-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d9892-600">Prod 1</span></span></td>
<td><span data-ttu-id="d9892-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="d9892-601">Product 1</span></span></td>
<td><span data-ttu-id="d9892-602">60</span><span class="sxs-lookup"><span data-stu-id="d9892-602">60</span></span></td>
<td><span data-ttu-id="d9892-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="d9892-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="d9892-604">535.31</span><span class="sxs-lookup"><span data-stu-id="d9892-604">535.31</span></span></td>
<td><span data-ttu-id="d9892-605">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d9892-606">Prod 2</span></span></td>
<td><span data-ttu-id="d9892-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="d9892-607">Product 2</span></span></td>
<td><span data-ttu-id="d9892-608">20</span><span class="sxs-lookup"><span data-stu-id="d9892-608">20</span></span></td>
<td><span data-ttu-id="d9892-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="d9892-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="d9892-610">178.44</span><span class="sxs-lookup"><span data-stu-id="d9892-610">178.44</span></span></td>
<td><span data-ttu-id="d9892-611">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d9892-612">Prod 1</span></span></td>
<td><span data-ttu-id="d9892-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="d9892-613">Product 1</span></span></td>
<td><span data-ttu-id="d9892-614">60</span><span class="sxs-lookup"><span data-stu-id="d9892-614">60</span></span></td>
<td><span data-ttu-id="d9892-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="d9892-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="d9892-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="d9892-616">4,487.12</span></span></td>
<td><span data-ttu-id="d9892-617">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d9892-618">Prod 2</span></span></td>
<td><span data-ttu-id="d9892-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="d9892-619">Product 2</span></span></td>
<td><span data-ttu-id="d9892-620">20</span><span class="sxs-lookup"><span data-stu-id="d9892-620">20</span></span></td>
<td><span data-ttu-id="d9892-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="d9892-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="d9892-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="d9892-622">1,495.71</span></span></td>
<td><span data-ttu-id="d9892-623">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d9892-624">V následující tabulce je uveden výsledek při použití Služeb balení jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="d9892-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d9892-625">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-625">Cost object</span></span></th>
<th><span data-ttu-id="d9892-626">Hodnota</span><span class="sxs-lookup"><span data-stu-id="d9892-626">Magnitude</span></span></th>
<th><span data-ttu-id="d9892-627">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="d9892-627">Allocation factor</span></span></th>
<th><span data-ttu-id="d9892-628">Částka</span><span class="sxs-lookup"><span data-stu-id="d9892-628">Amount</span></span></th>
<th><span data-ttu-id="d9892-629">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9892-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d9892-630">Prod 1</span></span></td>
<td><span data-ttu-id="d9892-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="d9892-631">Product 1</span></span></td>
<td><span data-ttu-id="d9892-632">80</span><span class="sxs-lookup"><span data-stu-id="d9892-632">80</span></span></td>
<td><span data-ttu-id="d9892-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="d9892-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="d9892-634">241.05</span><span class="sxs-lookup"><span data-stu-id="d9892-634">241.05</span></span></td>
<td><span data-ttu-id="d9892-635">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d9892-636">Prod 2</span></span></td>
<td><span data-ttu-id="d9892-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="d9892-637">Product 2</span></span></td>
<td><span data-ttu-id="d9892-638">15</span><span class="sxs-lookup"><span data-stu-id="d9892-638">15</span></span></td>
<td><span data-ttu-id="d9892-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="d9892-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="d9892-640">45.20</span><span class="sxs-lookup"><span data-stu-id="d9892-640">45.20</span></span></td>
<td><span data-ttu-id="d9892-641">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d9892-642">Prod 1</span></span></td>
<td><span data-ttu-id="d9892-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="d9892-643">Product 1</span></span></td>
<td><span data-ttu-id="d9892-644">80</span><span class="sxs-lookup"><span data-stu-id="d9892-644">80</span></span></td>
<td><span data-ttu-id="d9892-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="d9892-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="d9892-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="d9892-646">2,507.09</span></span></td>
<td><span data-ttu-id="d9892-647">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d9892-648">Prod 2</span></span></td>
<td><span data-ttu-id="d9892-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="d9892-649">Product 2</span></span></td>
<td><span data-ttu-id="d9892-650">15</span><span class="sxs-lookup"><span data-stu-id="d9892-650">15</span></span></td>
<td><span data-ttu-id="d9892-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="d9892-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="d9892-652">470.08</span><span class="sxs-lookup"><span data-stu-id="d9892-652">470.08</span></span></td>
<td><span data-ttu-id="d9892-653">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="d9892-654">Položky deníku (položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="d9892-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d9892-655">Deník</span><span class="sxs-lookup"><span data-stu-id="d9892-655">Journal</span></span></th>
<th><span data-ttu-id="d9892-656">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="d9892-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="d9892-657">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="d9892-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="d9892-658">Verze</span><span class="sxs-lookup"><span data-stu-id="d9892-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9892-659">00004</span><span class="sxs-lookup"><span data-stu-id="d9892-659">00004</span></span></td>
<td><span data-ttu-id="d9892-660">Deník přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="d9892-661">Fiskální</span><span class="sxs-lookup"><span data-stu-id="d9892-661">Fiscal</span></span></td>
<td><span data-ttu-id="d9892-662">2017</span><span class="sxs-lookup"><span data-stu-id="d9892-662">2017</span></span></td>
<td><span data-ttu-id="d9892-663">Období 1</span><span class="sxs-lookup"><span data-stu-id="d9892-663">Period 1</span></span></td>
<td><span data-ttu-id="d9892-664">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="d9892-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="d9892-665">Řádky deníku</span><span class="sxs-lookup"><span data-stu-id="d9892-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d9892-666">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="d9892-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="d9892-667">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d9892-668">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-668">Cost element</span></span></th>
<th><span data-ttu-id="d9892-669">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-669">Cost behavior</span></span></th>
<th><span data-ttu-id="d9892-670">Částka</span><span class="sxs-lookup"><span data-stu-id="d9892-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9892-671">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="d9892-672">CC001</span><span class="sxs-lookup"><span data-stu-id="d9892-672">CC001</span></span></td>
<td><span data-ttu-id="d9892-673">HR</span><span class="sxs-lookup"><span data-stu-id="d9892-673">HR</span></span></td>
<td><span data-ttu-id="d9892-674">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-674">10001</span></span></td>
<td><span data-ttu-id="d9892-675">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-675">Electricity</span></span></td>
<td><span data-ttu-id="d9892-676">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-676">Fixed cost</span></span></td>
<td><span data-ttu-id="d9892-677">500.00</span><span class="sxs-lookup"><span data-stu-id="d9892-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-678">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="d9892-679">CC001</span><span class="sxs-lookup"><span data-stu-id="d9892-679">CC001</span></span></td>
<td><span data-ttu-id="d9892-680">HR</span><span class="sxs-lookup"><span data-stu-id="d9892-680">HR</span></span></td>
<td><span data-ttu-id="d9892-681">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-681">10001</span></span></td>
<td><span data-ttu-id="d9892-682">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-682">Electricity</span></span></td>
<td><span data-ttu-id="d9892-683">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-683">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="d9892-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-685">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="d9892-686">CC002</span><span class="sxs-lookup"><span data-stu-id="d9892-686">CC002</span></span></td>
<td><span data-ttu-id="d9892-687">Finance</span><span class="sxs-lookup"><span data-stu-id="d9892-687">Finance</span></span></td>
<td><span data-ttu-id="d9892-688">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-688">10001</span></span></td>
<td><span data-ttu-id="d9892-689">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-689">Electricity</span></span></td>
<td><span data-ttu-id="d9892-690">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-690">Fixed cost</span></span></td>
<td><span data-ttu-id="d9892-691">675.00</span><span class="sxs-lookup"><span data-stu-id="d9892-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-692">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="d9892-693">CC002</span><span class="sxs-lookup"><span data-stu-id="d9892-693">CC002</span></span></td>
<td><span data-ttu-id="d9892-694">Finance</span><span class="sxs-lookup"><span data-stu-id="d9892-694">Finance</span></span></td>
<td><span data-ttu-id="d9892-695">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-695">10001</span></span></td>
<td><span data-ttu-id="d9892-696">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-696">Electricity</span></span></td>
<td><span data-ttu-id="d9892-697">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-697">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="d9892-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-699">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="d9892-700">CC003</span><span class="sxs-lookup"><span data-stu-id="d9892-700">CC003</span></span></td>
<td><span data-ttu-id="d9892-701">Sestavení</span><span class="sxs-lookup"><span data-stu-id="d9892-701">Assembly</span></span></td>
<td><span data-ttu-id="d9892-702">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-702">10001</span></span></td>
<td><span data-ttu-id="d9892-703">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-703">Electricity</span></span></td>
<td><span data-ttu-id="d9892-704">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-704">Fixed cost</span></span></td>
<td><span data-ttu-id="d9892-705">713.75</span><span class="sxs-lookup"><span data-stu-id="d9892-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-706">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="d9892-707">CC003</span><span class="sxs-lookup"><span data-stu-id="d9892-707">CC003</span></span></td>
<td><span data-ttu-id="d9892-708">Sestavení</span><span class="sxs-lookup"><span data-stu-id="d9892-708">Assembly</span></span></td>
<td><span data-ttu-id="d9892-709">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-709">10001</span></span></td>
<td><span data-ttu-id="d9892-710">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-710">Electricity</span></span></td>
<td><span data-ttu-id="d9892-711">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-711">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="d9892-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-713">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="d9892-714">CC003</span><span class="sxs-lookup"><span data-stu-id="d9892-714">CC003</span></span></td>
<td><span data-ttu-id="d9892-715">Balení</span><span class="sxs-lookup"><span data-stu-id="d9892-715">Packaging</span></span></td>
<td><span data-ttu-id="d9892-716">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-716">10001</span></span></td>
<td><span data-ttu-id="d9892-717">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-717">Electricity</span></span></td>
<td><span data-ttu-id="d9892-718">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-718">Fixed cost</span></span></td>
<td><span data-ttu-id="d9892-719">286.25</span><span class="sxs-lookup"><span data-stu-id="d9892-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-720">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="d9892-721">CC003</span><span class="sxs-lookup"><span data-stu-id="d9892-721">CC003</span></span></td>
<td><span data-ttu-id="d9892-722">Balení</span><span class="sxs-lookup"><span data-stu-id="d9892-722">Packaging</span></span></td>
<td><span data-ttu-id="d9892-723">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-723">10001</span></span></td>
<td><span data-ttu-id="d9892-724">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-724">Electricity</span></span></td>
<td><span data-ttu-id="d9892-725">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-725">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="d9892-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-727">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="d9892-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d9892-728">Prod 1</span></span></td>
<td><span data-ttu-id="d9892-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="d9892-729">Product 1</span></span></td>
<td><span data-ttu-id="d9892-730">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-730">10001</span></span></td>
<td><span data-ttu-id="d9892-731">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-731">Electricity</span></span></td>
<td><span data-ttu-id="d9892-732">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-732">Fixed cost</span></span></td>
<td><span data-ttu-id="d9892-733">776.36</span><span class="sxs-lookup"><span data-stu-id="d9892-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-734">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="d9892-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d9892-735">Prod 1</span></span></td>
<td><span data-ttu-id="d9892-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="d9892-736">Product 1</span></span></td>
<td><span data-ttu-id="d9892-737">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-737">10001</span></span></td>
<td><span data-ttu-id="d9892-738">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-738">Electricity</span></span></td>
<td><span data-ttu-id="d9892-739">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-739">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="d9892-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-741">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="d9892-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d9892-742">Prod 2</span></span></td>
<td><span data-ttu-id="d9892-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="d9892-743">Product 1</span></span></td>
<td><span data-ttu-id="d9892-744">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-744">10001</span></span></td>
<td><span data-ttu-id="d9892-745">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-745">Electricity</span></span></td>
<td><span data-ttu-id="d9892-746">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-746">Fixed cost</span></span></td>
<td><span data-ttu-id="d9892-747">223.64</span><span class="sxs-lookup"><span data-stu-id="d9892-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-748">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="d9892-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d9892-749">Prod 2</span></span></td>
<td><span data-ttu-id="d9892-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="d9892-750">Product 1</span></span></td>
<td><span data-ttu-id="d9892-751">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-751">10001</span></span></td>
<td><span data-ttu-id="d9892-752">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-752">Electricity</span></span></td>
<td><span data-ttu-id="d9892-753">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-753">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="d9892-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="d9892-755">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d9892-756">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d9892-757">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-757">Cost element</span></span></th>
<th><span data-ttu-id="d9892-758">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-758">Cost behavior</span></span></th>
<th><span data-ttu-id="d9892-759">Částka</span><span class="sxs-lookup"><span data-stu-id="d9892-759">Amount</span></span></th>
<th><span data-ttu-id="d9892-760">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="d9892-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d9892-761">CC001</span><span class="sxs-lookup"><span data-stu-id="d9892-761">CC001</span></span></td>
<td><span data-ttu-id="d9892-762">HR</span><span class="sxs-lookup"><span data-stu-id="d9892-762">HR</span></span></td>
<td><span data-ttu-id="d9892-763">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-763">10001</span></span></td>
<td><span data-ttu-id="d9892-764">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-764">Electricity</span></span></td>
<td><span data-ttu-id="d9892-765">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-765">Fixed cost</span></span></td>
<td><span data-ttu-id="d9892-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="d9892-766">-500.00</span></span></td>
<td><span data-ttu-id="d9892-767">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-768">CC002</span><span class="sxs-lookup"><span data-stu-id="d9892-768">CC002</span></span></td>
<td><span data-ttu-id="d9892-769">Finance</span><span class="sxs-lookup"><span data-stu-id="d9892-769">Finance</span></span></td>
<td><span data-ttu-id="d9892-770">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-770">10001</span></span></td>
<td><span data-ttu-id="d9892-771">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-771">Electricity</span></span></td>
<td><span data-ttu-id="d9892-772">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-772">Fixed cost</span></span></td>
<td><span data-ttu-id="d9892-773">175.00</span><span class="sxs-lookup"><span data-stu-id="d9892-773">175.00</span></span></td>
<td><span data-ttu-id="d9892-774">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-775">CC003</span><span class="sxs-lookup"><span data-stu-id="d9892-775">CC003</span></span></td>
<td><span data-ttu-id="d9892-776">Sestavení</span><span class="sxs-lookup"><span data-stu-id="d9892-776">Assembly</span></span></td>
<td><span data-ttu-id="d9892-777">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-777">10001</span></span></td>
<td><span data-ttu-id="d9892-778">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-778">Electricity</span></span></td>
<td><span data-ttu-id="d9892-779">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-779">Fixed cost</span></span></td>
<td><span data-ttu-id="d9892-780">275.00</span><span class="sxs-lookup"><span data-stu-id="d9892-780">275.00</span></span></td>
<td><span data-ttu-id="d9892-781">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-782">CC004</span><span class="sxs-lookup"><span data-stu-id="d9892-782">CC004</span></span></td>
<td><span data-ttu-id="d9892-783">Balení</span><span class="sxs-lookup"><span data-stu-id="d9892-783">Packaging</span></span></td>
<td><span data-ttu-id="d9892-784">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-784">10001</span></span></td>
<td><span data-ttu-id="d9892-785">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-785">Electricity</span></span></td>
<td><span data-ttu-id="d9892-786">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-786">Fixed cost</span></span></td>
<td><span data-ttu-id="d9892-787">50,00</span><span class="sxs-lookup"><span data-stu-id="d9892-787">50,00</span></span></td>
<td><span data-ttu-id="d9892-788">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-789">CC001</span><span class="sxs-lookup"><span data-stu-id="d9892-789">CC001</span></span></td>
<td><span data-ttu-id="d9892-790">HR</span><span class="sxs-lookup"><span data-stu-id="d9892-790">HR</span></span></td>
<td><span data-ttu-id="d9892-791">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-791">10001</span></span></td>
<td><span data-ttu-id="d9892-792">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-792">Electricity</span></span></td>
<td><span data-ttu-id="d9892-793">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-793">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-794">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="d9892-794">-1,245.71</span></span></td>
<td><span data-ttu-id="d9892-795">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-796">CC002</span><span class="sxs-lookup"><span data-stu-id="d9892-796">CC002</span></span></td>
<td><span data-ttu-id="d9892-797">Finance</span><span class="sxs-lookup"><span data-stu-id="d9892-797">Finance</span></span></td>
<td><span data-ttu-id="d9892-798">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-798">10001</span></span></td>
<td><span data-ttu-id="d9892-799">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-799">Electricity</span></span></td>
<td><span data-ttu-id="d9892-800">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-800">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-801">436.00</span><span class="sxs-lookup"><span data-stu-id="d9892-801">436.00</span></span></td>
<td><span data-ttu-id="d9892-802">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-803">CC003</span><span class="sxs-lookup"><span data-stu-id="d9892-803">CC003</span></span></td>
<td><span data-ttu-id="d9892-804">Sestavení</span><span class="sxs-lookup"><span data-stu-id="d9892-804">Assembly</span></span></td>
<td><span data-ttu-id="d9892-805">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-805">10001</span></span></td>
<td><span data-ttu-id="d9892-806">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-806">Electricity</span></span></td>
<td><span data-ttu-id="d9892-807">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-807">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-808">685.14</span><span class="sxs-lookup"><span data-stu-id="d9892-808">685.14</span></span></td>
<td><span data-ttu-id="d9892-809">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-810">CC004</span><span class="sxs-lookup"><span data-stu-id="d9892-810">CC004</span></span></td>
<td><span data-ttu-id="d9892-811">Balení</span><span class="sxs-lookup"><span data-stu-id="d9892-811">Packaging</span></span></td>
<td><span data-ttu-id="d9892-812">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-812">10001</span></span></td>
<td><span data-ttu-id="d9892-813">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-813">Electricity</span></span></td>
<td><span data-ttu-id="d9892-814">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-814">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-815">124.57</span><span class="sxs-lookup"><span data-stu-id="d9892-815">124.57</span></span></td>
<td><span data-ttu-id="d9892-816">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-817">CC002</span><span class="sxs-lookup"><span data-stu-id="d9892-817">CC002</span></span></td>
<td><span data-ttu-id="d9892-818">Finance</span><span class="sxs-lookup"><span data-stu-id="d9892-818">Finance</span></span></td>
<td><span data-ttu-id="d9892-819">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-819">10001</span></span></td>
<td><span data-ttu-id="d9892-820">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-820">Electricity</span></span></td>
<td><span data-ttu-id="d9892-821">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-821">Fixed cost</span></span></td>
<td><span data-ttu-id="d9892-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="d9892-822">-675.00</span></span></td>
<td><span data-ttu-id="d9892-823">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-824">CC003</span><span class="sxs-lookup"><span data-stu-id="d9892-824">CC003</span></span></td>
<td><span data-ttu-id="d9892-825">Sestavení</span><span class="sxs-lookup"><span data-stu-id="d9892-825">Assembly</span></span></td>
<td><span data-ttu-id="d9892-826">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-826">10001</span></span></td>
<td><span data-ttu-id="d9892-827">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-827">Electricity</span></span></td>
<td><span data-ttu-id="d9892-828">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-828">Fixed cost</span></span></td>
<td><span data-ttu-id="d9892-829">438.75</span><span class="sxs-lookup"><span data-stu-id="d9892-829">438.75</span></span></td>
<td><span data-ttu-id="d9892-830">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-831">CC004</span><span class="sxs-lookup"><span data-stu-id="d9892-831">CC004</span></span></td>
<td><span data-ttu-id="d9892-832">Balení</span><span class="sxs-lookup"><span data-stu-id="d9892-832">Packaging</span></span></td>
<td><span data-ttu-id="d9892-833">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-833">10001</span></span></td>
<td><span data-ttu-id="d9892-834">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-834">Electricity</span></span></td>
<td><span data-ttu-id="d9892-835">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-835">Fixed cost</span></span></td>
<td><span data-ttu-id="d9892-836">236.25</span><span class="sxs-lookup"><span data-stu-id="d9892-836">236.25</span></span></td>
<td><span data-ttu-id="d9892-837">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-838">CC002</span><span class="sxs-lookup"><span data-stu-id="d9892-838">CC002</span></span></td>
<td><span data-ttu-id="d9892-839">Finance</span><span class="sxs-lookup"><span data-stu-id="d9892-839">Finance</span></span></td>
<td><span data-ttu-id="d9892-840">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-840">10001</span></span></td>
<td><span data-ttu-id="d9892-841">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-841">Electricity</span></span></td>
<td><span data-ttu-id="d9892-842">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-842">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-843">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="d9892-843">-8,150.29</span></span></td>
<td><span data-ttu-id="d9892-844">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-845">CC003</span><span class="sxs-lookup"><span data-stu-id="d9892-845">CC003</span></span></td>
<td><span data-ttu-id="d9892-846">Sestavení</span><span class="sxs-lookup"><span data-stu-id="d9892-846">Assembly</span></span></td>
<td><span data-ttu-id="d9892-847">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-847">10001</span></span></td>
<td><span data-ttu-id="d9892-848">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-848">Electricity</span></span></td>
<td><span data-ttu-id="d9892-849">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-849">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="d9892-850">5,297.69</span></span></td>
<td><span data-ttu-id="d9892-851">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-852">CC004</span><span class="sxs-lookup"><span data-stu-id="d9892-852">CC004</span></span></td>
<td><span data-ttu-id="d9892-853">Balení</span><span class="sxs-lookup"><span data-stu-id="d9892-853">Packaging</span></span></td>
<td><span data-ttu-id="d9892-854">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-854">10001</span></span></td>
<td><span data-ttu-id="d9892-855">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-855">Electricity</span></span></td>
<td><span data-ttu-id="d9892-856">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-856">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="d9892-857">2,852.60</span></span></td>
<td><span data-ttu-id="d9892-858">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-859">CC003</span><span class="sxs-lookup"><span data-stu-id="d9892-859">CC003</span></span></td>
<td><span data-ttu-id="d9892-860">Sestavení</span><span class="sxs-lookup"><span data-stu-id="d9892-860">Assembly</span></span></td>
<td><span data-ttu-id="d9892-861">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-861">10001</span></span></td>
<td><span data-ttu-id="d9892-862">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-862">Electricity</span></span></td>
<td><span data-ttu-id="d9892-863">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-863">Fixed cost</span></span></td>
<td><span data-ttu-id="d9892-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="d9892-864">-713.75</span></span></td>
<td><span data-ttu-id="d9892-865">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d9892-866">Prod 1</span></span></td>
<td><span data-ttu-id="d9892-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="d9892-867">Product 1</span></span></td>
<td><span data-ttu-id="d9892-868">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-868">10001</span></span></td>
<td><span data-ttu-id="d9892-869">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-869">Electricity</span></span></td>
<td><span data-ttu-id="d9892-870">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-870">Fixed cost</span></span></td>
<td><span data-ttu-id="d9892-871">535.31</span><span class="sxs-lookup"><span data-stu-id="d9892-871">535.31</span></span></td>
<td><span data-ttu-id="d9892-872">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d9892-873">Prod 2</span></span></td>
<td><span data-ttu-id="d9892-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="d9892-874">Product 2</span></span></td>
<td><span data-ttu-id="d9892-875">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-875">10001</span></span></td>
<td><span data-ttu-id="d9892-876">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-876">Electricity</span></span></td>
<td><span data-ttu-id="d9892-877">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-877">Fixed cost</span></span></td>
<td><span data-ttu-id="d9892-878">178.44</span><span class="sxs-lookup"><span data-stu-id="d9892-878">178.44</span></span></td>
<td><span data-ttu-id="d9892-879">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-880">CC003</span><span class="sxs-lookup"><span data-stu-id="d9892-880">CC003</span></span></td>
<td><span data-ttu-id="d9892-881">Sestavení</span><span class="sxs-lookup"><span data-stu-id="d9892-881">Assembly</span></span></td>
<td><span data-ttu-id="d9892-882">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-882">10001</span></span></td>
<td><span data-ttu-id="d9892-883">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-883">Electricity</span></span></td>
<td><span data-ttu-id="d9892-884">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-884">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-885">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="d9892-885">-5,982.83</span></span></td>
<td><span data-ttu-id="d9892-886">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d9892-887">Prod 1</span></span></td>
<td><span data-ttu-id="d9892-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="d9892-888">Product 1</span></span></td>
<td><span data-ttu-id="d9892-889">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-889">10001</span></span></td>
<td><span data-ttu-id="d9892-890">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-890">Electricity</span></span></td>
<td><span data-ttu-id="d9892-891">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-891">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="d9892-892">4,487.12</span></span></td>
<td><span data-ttu-id="d9892-893">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d9892-894">Prod 2</span></span></td>
<td><span data-ttu-id="d9892-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="d9892-895">Product 2</span></span></td>
<td><span data-ttu-id="d9892-896">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-896">10001</span></span></td>
<td><span data-ttu-id="d9892-897">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-897">Electricity</span></span></td>
<td><span data-ttu-id="d9892-898">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-898">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="d9892-899">1,495.71</span></span></td>
<td><span data-ttu-id="d9892-900">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-901">CC003</span><span class="sxs-lookup"><span data-stu-id="d9892-901">CC003</span></span></td>
<td><span data-ttu-id="d9892-902">Sestavení</span><span class="sxs-lookup"><span data-stu-id="d9892-902">Assembly</span></span></td>
<td><span data-ttu-id="d9892-903">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-903">10001</span></span></td>
<td><span data-ttu-id="d9892-904">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-904">Electricity</span></span></td>
<td><span data-ttu-id="d9892-905">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-905">Fixed cost</span></span></td>
<td><span data-ttu-id="d9892-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="d9892-906">-286.25</span></span></td>
<td><span data-ttu-id="d9892-907">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d9892-908">Prod 1</span></span></td>
<td><span data-ttu-id="d9892-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="d9892-909">Product 1</span></span></td>
<td><span data-ttu-id="d9892-910">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-910">10001</span></span></td>
<td><span data-ttu-id="d9892-911">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-911">Electricity</span></span></td>
<td><span data-ttu-id="d9892-912">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-912">Fixed cost</span></span></td>
<td><span data-ttu-id="d9892-913">241.05</span><span class="sxs-lookup"><span data-stu-id="d9892-913">241.05</span></span></td>
<td><span data-ttu-id="d9892-914">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d9892-915">Prod 2</span></span></td>
<td><span data-ttu-id="d9892-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="d9892-916">Product 2</span></span></td>
<td><span data-ttu-id="d9892-917">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-917">10001</span></span></td>
<td><span data-ttu-id="d9892-918">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-918">Electricity</span></span></td>
<td><span data-ttu-id="d9892-919">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-919">Fixed cost</span></span></td>
<td><span data-ttu-id="d9892-920">45.20</span><span class="sxs-lookup"><span data-stu-id="d9892-920">45.20</span></span></td>
<td><span data-ttu-id="d9892-921">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-922">CC003</span><span class="sxs-lookup"><span data-stu-id="d9892-922">CC003</span></span></td>
<td><span data-ttu-id="d9892-923">Sestavení</span><span class="sxs-lookup"><span data-stu-id="d9892-923">Assembly</span></span></td>
<td><span data-ttu-id="d9892-924">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-924">10001</span></span></td>
<td><span data-ttu-id="d9892-925">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-925">Electricity</span></span></td>
<td><span data-ttu-id="d9892-926">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-926">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="d9892-927">-2,977.17</span></span></td>
<td><span data-ttu-id="d9892-928">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d9892-929">Prod 1</span></span></td>
<td><span data-ttu-id="d9892-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="d9892-930">Product 1</span></span></td>
<td><span data-ttu-id="d9892-931">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-931">10001</span></span></td>
<td><span data-ttu-id="d9892-932">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-932">Electricity</span></span></td>
<td><span data-ttu-id="d9892-933">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-933">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="d9892-934">2,507.09</span></span></td>
<td><span data-ttu-id="d9892-935">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d9892-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d9892-936">Prod 2</span></span></td>
<td><span data-ttu-id="d9892-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="d9892-937">Product 2</span></span></td>
<td><span data-ttu-id="d9892-938">10001</span><span class="sxs-lookup"><span data-stu-id="d9892-938">10001</span></span></td>
<td><span data-ttu-id="d9892-939">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="d9892-939">Electricity</span></span></td>
<td><span data-ttu-id="d9892-940">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-940">Variable cost</span></span></td>
<td><span data-ttu-id="d9892-941">470.08</span><span class="sxs-lookup"><span data-stu-id="d9892-941">470.08</span></span></td>
<td><span data-ttu-id="d9892-942">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="d9892-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="d9892-943">Závěr</span><span class="sxs-lookup"><span data-stu-id="d9892-943">Conclusion</span></span>
<span data-ttu-id="d9892-944">Ve finančním účtování se náklady za elektřinu ve výši 10 000 zaúčtují na ID fiktivního nákladového střediska.</span><span class="sxs-lookup"><span data-stu-id="d9892-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="d9892-945">Účetní tak budou vědět, že tento náklad musí být přidělen.</span><span class="sxs-lookup"><span data-stu-id="d9892-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="d9892-946">V nákladovém účetnictví náklady procházejí napříč organizačními jednotkami a úrovněmi, na základě použitých zásad a pravidel.</span><span class="sxs-lookup"><span data-stu-id="d9892-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="d9892-947">Každý náklad byl přidružen k základu přidělení, který poskytuje nejlepší hodnocení pro přidělení nákladů.</span><span class="sxs-lookup"><span data-stu-id="d9892-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="d9892-948">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="d9892-949">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="d9892-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="d9892-950">Celkem</span><span class="sxs-lookup"><span data-stu-id="d9892-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d9892-951">CC099</span><span class="sxs-lookup"><span data-stu-id="d9892-951">CC099</span></span></th>
<th><span data-ttu-id="d9892-952">CC001</span><span class="sxs-lookup"><span data-stu-id="d9892-952">CC001</span></span></th>
<th><span data-ttu-id="d9892-953">CC002</span><span class="sxs-lookup"><span data-stu-id="d9892-953">CC002</span></span></th>
<th><span data-ttu-id="d9892-954">CC003</span><span class="sxs-lookup"><span data-stu-id="d9892-954">CC003</span></span></th>
<th><span data-ttu-id="d9892-955">CC004</span><span class="sxs-lookup"><span data-stu-id="d9892-955">CC004</span></span></th>
<th><span data-ttu-id="d9892-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="d9892-956">Proj 1</span></span></th>
<th><span data-ttu-id="d9892-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="d9892-957">Proj 2</span></span></th>
<th><span data-ttu-id="d9892-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d9892-958">Prod 1</span></span></th>
<th><span data-ttu-id="d9892-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d9892-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="d9892-960">10001 Elektřina</span><span class="sxs-lookup"><span data-stu-id="d9892-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d9892-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="d9892-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d9892-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="d9892-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d9892-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="d9892-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d9892-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="d9892-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="d9892-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="d9892-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d9892-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="d9892-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d9892-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="d9892-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d9892-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="d9892-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d9892-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="d9892-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="d9892-970">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="d9892-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d9892-971">0,00</span><span class="sxs-lookup"><span data-stu-id="d9892-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="d9892-972">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d9892-973">0,00</span><span class="sxs-lookup"><span data-stu-id="d9892-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d9892-974">0,00</span><span class="sxs-lookup"><span data-stu-id="d9892-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d9892-975">0,00</span><span class="sxs-lookup"><span data-stu-id="d9892-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d9892-976">0,00</span><span class="sxs-lookup"><span data-stu-id="d9892-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d9892-977">0,00</span><span class="sxs-lookup"><span data-stu-id="d9892-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="d9892-978">776.36</span><span class="sxs-lookup"><span data-stu-id="d9892-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d9892-979">223.64</span><span class="sxs-lookup"><span data-stu-id="d9892-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d9892-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="d9892-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="d9892-981">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="d9892-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d9892-982">000</span><span class="sxs-lookup"><span data-stu-id="d9892-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d9892-983">0,00</span><span class="sxs-lookup"><span data-stu-id="d9892-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d9892-984">0,00</span><span class="sxs-lookup"><span data-stu-id="d9892-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d9892-985">0,00</span><span class="sxs-lookup"><span data-stu-id="d9892-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d9892-986">0,00</span><span class="sxs-lookup"><span data-stu-id="d9892-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d9892-987">30.00</span><span class="sxs-lookup"><span data-stu-id="d9892-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d9892-988">10,00</span><span class="sxs-lookup"><span data-stu-id="d9892-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d9892-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="d9892-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d9892-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="d9892-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d9892-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="d9892-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="d9892-992">Toto téma popisuje, jak primární prvek nákladů, 10001 Elektřina, prochází přes objekty nákladů.</span><span class="sxs-lookup"><span data-stu-id="d9892-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="d9892-993">Tyto režijní náklady tedy budou přiděleny na nejnižší úroveň v organizaci.</span><span class="sxs-lookup"><span data-stu-id="d9892-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="d9892-994">Jinak řečeno, objekty nákladů na nejnižší úrovni ponesou náklady.</span><span class="sxs-lookup"><span data-stu-id="d9892-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="d9892-995">Chcete-li vizuální tok nákladů mezi objekty nákladů, můžete použít pravidla zásad shrnutí nákladů pro vizualizaci jejich toků.</span><span class="sxs-lookup"><span data-stu-id="d9892-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="d9892-996">Další informace naleznete v tématu [Zásady shrnutí nákladů a výpočet režijních nákladů](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="d9892-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



