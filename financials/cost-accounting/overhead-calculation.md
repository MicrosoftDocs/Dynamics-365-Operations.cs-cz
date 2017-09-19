---
title: "Výpočet režijních nákladů"
description: "Toto téma popisuje typické procesy pro výpočet a přidělení režijních nákladů."
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: 9e13fc9fa7e51a1299ca8698f581de979b680a7b
ms.openlocfilehash: a8c867ba49b95af2816fe8294059307e974c0a81
ms.contentlocale: cs-cz
ms.lasthandoff: 09/18/2017

---

# <a name="overhead-calculation"></a><span data-ttu-id="4775d-103">Výpočet režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4775d-104">Toto téma popisuje typické procesy pro výpočet a přidělení režijních nákladů.</span><span class="sxs-lookup"><span data-stu-id="4775d-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="4775d-105">Definice termínu</span><span class="sxs-lookup"><span data-stu-id="4775d-105">Term definition</span></span>
---------------

<span data-ttu-id="4775d-106">Režijní náklady jsou náklady, které nutně vznikají při chodu podnikání, ale nelze je připsat přímo k žádné konkrétní podnikatelské aktivitě, produktu nebo službě.</span><span class="sxs-lookup"><span data-stu-id="4775d-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="4775d-107">Režijní náklady poskytují důležitou podporu pro generování aktivity přinášejících zisk.</span><span class="sxs-lookup"><span data-stu-id="4775d-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="4775d-108">Následuje několik příkladů režijních nákladů:</span><span class="sxs-lookup"><span data-stu-id="4775d-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="4775d-109">Renta</span><span class="sxs-lookup"><span data-stu-id="4775d-109">Rent</span></span>
-   <span data-ttu-id="4775d-110">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-110">Electricity</span></span>
-   <span data-ttu-id="4775d-111">Administrativní mzdy</span><span class="sxs-lookup"><span data-stu-id="4775d-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="4775d-112">Přehled výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-112">Overhead calculation overview</span></span>
<span data-ttu-id="4775d-113">Výpočet režijních nákladů spustí zásady účtování nákladů ve správném pořadí.</span><span class="sxs-lookup"><span data-stu-id="4775d-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="4775d-114">Výpočet režijních nákladů můžete pro stejné fiskální období spustit mnohokrát, pokud došlo ke změně zásad účtování nákladů nebo zjištění konkrétních chyb.</span><span class="sxs-lookup"><span data-stu-id="4775d-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="4775d-115">Každé spuštění výpočtu režijních nákladů se ukládá a přijímá ID jedinečné verze, které vám umožní porovnávat výpočty v různých verzích.</span><span class="sxs-lookup"><span data-stu-id="4775d-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="4775d-116">Položky nákladů, které generuje výpočet režijních nákladů, přijímá datum účtování.</span><span class="sxs-lookup"><span data-stu-id="4775d-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="4775d-117">Toto datum účtován se shoduje s konvovým datem fiskálního období, které se použije ve výpočtu.</span><span class="sxs-lookup"><span data-stu-id="4775d-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="4775d-118">ID jedinečné verze se skládá z následujících prvků:</span><span class="sxs-lookup"><span data-stu-id="4775d-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="4775d-119">Typ verze</span><span class="sxs-lookup"><span data-stu-id="4775d-119">Version type</span></span>
-   <span data-ttu-id="4775d-120">Datum a čas</span><span class="sxs-lookup"><span data-stu-id="4775d-120">Date and time</span></span>
-   <span data-ttu-id="4775d-121">Hlavní kniha nákladového účetnictví</span><span class="sxs-lookup"><span data-stu-id="4775d-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="4775d-122">Fiskální rok</span><span class="sxs-lookup"><span data-stu-id="4775d-122">Fiscal year</span></span>
-   <span data-ttu-id="4775d-123">Fiskální období</span><span class="sxs-lookup"><span data-stu-id="4775d-123">Fiscal period</span></span>

<span data-ttu-id="4775d-124">Výpočet režijních nákladů se spustí bez ohledu na verzi.</span><span class="sxs-lookup"><span data-stu-id="4775d-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="4775d-125">Proto lze vypočítat rozpočtovou verzi před skutečnou verzí.</span><span class="sxs-lookup"><span data-stu-id="4775d-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="4775d-126">Výpočet režijních nákladů se skládá ze čtyř kroků uvedených na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="4775d-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="4775d-127">V každé fázi je vytvořeno záhlaví deníku, které obsahuje položky deníku.</span><span class="sxs-lookup"><span data-stu-id="4775d-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="4775d-128">Toto záhlaví deníku zachovává vstupní data pro každý krok výpočtu.</span><span class="sxs-lookup"><span data-stu-id="4775d-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="4775d-129">Zásady a pravidla se použijí na každý řádek deníku a položky nákladů jsou generovány jako výstup.</span><span class="sxs-lookup"><span data-stu-id="4775d-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="4775d-130">Máte tedy vždy plnou sledovatelnost.</span><span class="sxs-lookup"><span data-stu-id="4775d-130">Therefore, you always have full traceability.</span></span> 
<span data-ttu-id="4775d-131">[![Výpočet režijních nákladů](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="4775d-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="4775d-132">Výpočet a přidělení režijních nákladů za elektřinu</span><span class="sxs-lookup"><span data-stu-id="4775d-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="4775d-133">Ve finančním účetnictví se některé náklady, jako je například elektřina, registrují jako paušální.</span><span class="sxs-lookup"><span data-stu-id="4775d-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="4775d-134">Podrobný přehled pro vedoucí není tedy pro nákladové účetnictví k dispozici.</span><span class="sxs-lookup"><span data-stu-id="4775d-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="4775d-135">V nákladovém účetnictví musí náklady procházet organizačními jednotkami, aby byl získán správný přehled pro vedoucí napříč všemi jednotkami a úrovněmi organizace.</span><span class="sxs-lookup"><span data-stu-id="4775d-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="4775d-136">Tento tok musí být založen buď na přesném záznamu spotřeby nebo na objektivním hodnocení.</span><span class="sxs-lookup"><span data-stu-id="4775d-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="4775d-137">V hlavní knize mohou být zaúčtovány náklady na elektřinu způsobem znázorněným v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="4775d-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4775d-138">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="4775d-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4775d-139">Nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="4775d-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="4775d-140">Hlavní účet</span><span class="sxs-lookup"><span data-stu-id="4775d-140">Main account</span></span></th>
<th><span data-ttu-id="4775d-141">Částka v zúčtovací měně</span><span class="sxs-lookup"><span data-stu-id="4775d-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4775d-142">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="4775d-143">CC099</span><span class="sxs-lookup"><span data-stu-id="4775d-143">CC099</span></span></td>
<td><span data-ttu-id="4775d-144">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="4775d-144">Default cost center</span></span></td>
<td><span data-ttu-id="4775d-145">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-145">10001</span></span></td>
<td><span data-ttu-id="4775d-146">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-146">Electricity</span></span></td>
<td><span data-ttu-id="4775d-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="4775d-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="4775d-148">Krok 1: Zpracování výpočtu chování nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="4775d-149">Ve výchozím nastavení dostanou při importu položek nákladů z datového zdroje tyto položky v nákladovém účetnictví klasifikaci **Neklasifikované**.</span><span class="sxs-lookup"><span data-stu-id="4775d-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="4775d-150">Použitím pravidla zásad chování nákladů lze reklasifikovat položky nákladů jako **Pevné náklady** nebo **Variabilní náklady**.</span><span class="sxs-lookup"><span data-stu-id="4775d-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="4775d-151">Definice pravidel chování nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-151">Define the cost behavior rule</span></span>

<span data-ttu-id="4775d-152">V některých případech je část nákladů s pevným poplatkem a zbývající náklady jsou založeny na spotřebě.</span><span class="sxs-lookup"><span data-stu-id="4775d-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="4775d-153">Účty za elektřinu často odpovídají této definici.</span><span class="sxs-lookup"><span data-stu-id="4775d-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="4775d-154">Po platbě konkrétního pevného poplatku platíte spotřebu za kilowatthodinu (kWh).</span><span class="sxs-lookup"><span data-stu-id="4775d-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="4775d-155">Pokud je například poplatek pevných nákladů 1 000,00, definuje se pravidlo chování nákladů takto:</span><span class="sxs-lookup"><span data-stu-id="4775d-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="4775d-156">Pevná částka 1 000,00</span><span class="sxs-lookup"><span data-stu-id="4775d-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="4775d-157">0 &lt;= 1 000,00 = Pevná</span><span class="sxs-lookup"><span data-stu-id="4775d-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="4775d-158">1 000,01 &lt; N = Variabilní</span><span class="sxs-lookup"><span data-stu-id="4775d-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="4775d-159">Deník</span><span class="sxs-lookup"><span data-stu-id="4775d-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4775d-160">Deník</span><span class="sxs-lookup"><span data-stu-id="4775d-160">Journal</span></span></th>
<th><span data-ttu-id="4775d-161">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="4775d-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4775d-162">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="4775d-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4775d-163">Verze</span><span class="sxs-lookup"><span data-stu-id="4775d-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4775d-164">00001</span><span class="sxs-lookup"><span data-stu-id="4775d-164">00001</span></span></td>
<td><span data-ttu-id="4775d-165">Deník výpočtu chování nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="4775d-166">Fiskální</span><span class="sxs-lookup"><span data-stu-id="4775d-166">Fiscal</span></span></td>
<td><span data-ttu-id="4775d-167">2017</span><span class="sxs-lookup"><span data-stu-id="4775d-167">2017</span></span></td>
<td><span data-ttu-id="4775d-168">Období 1</span><span class="sxs-lookup"><span data-stu-id="4775d-168">Period 1</span></span></td>
<td><span data-ttu-id="4775d-169">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="4775d-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4775d-170">Položky deníku (Položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="4775d-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4775d-171">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="4775d-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4775d-172">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4775d-173">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-173">Cost element</span></span></th>
<th><span data-ttu-id="4775d-174">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-174">Cost behavior</span></span></th>
<th><span data-ttu-id="4775d-175">Částka</span><span class="sxs-lookup"><span data-stu-id="4775d-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4775d-176">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="4775d-177">CC099</span><span class="sxs-lookup"><span data-stu-id="4775d-177">CC099</span></span></td>
<td><span data-ttu-id="4775d-178">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="4775d-178">Default cost center</span></span></td>
<td><span data-ttu-id="4775d-179">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-179">10001</span></span></td>
<td><span data-ttu-id="4775d-180">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-180">Electricity</span></span></td>
<td><span data-ttu-id="4775d-181">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="4775d-181">Unclassified</span></span></td>
<td><span data-ttu-id="4775d-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="4775d-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4775d-183">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4775d-184">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4775d-185">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-185">Cost element</span></span></th>
<th><span data-ttu-id="4775d-186">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-186">Cost behavior</span></span></th>
<th><span data-ttu-id="4775d-187">Částka</span><span class="sxs-lookup"><span data-stu-id="4775d-187">Amount</span></span></th>
<th><span data-ttu-id="4775d-188">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="4775d-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4775d-189">CC099</span><span class="sxs-lookup"><span data-stu-id="4775d-189">CC099</span></span></td>
<td><span data-ttu-id="4775d-190">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="4775d-190">Default cost center</span></span></td>
<td><span data-ttu-id="4775d-191">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-191">10001</span></span></td>
<td><span data-ttu-id="4775d-192">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-192">Electricity</span></span></td>
<td><span data-ttu-id="4775d-193">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="4775d-193">Unclassified</span></span></td>
<td><span data-ttu-id="4775d-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="4775d-194">10,000.00</span></span></td>
<td><span data-ttu-id="4775d-195">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-196">CC099</span><span class="sxs-lookup"><span data-stu-id="4775d-196">CC099</span></span></td>
<td><span data-ttu-id="4775d-197">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="4775d-197">Default cost center</span></span></td>
<td><span data-ttu-id="4775d-198">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-198">10001</span></span></td>
<td><span data-ttu-id="4775d-199">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-199">Electricity</span></span></td>
<td><span data-ttu-id="4775d-200">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="4775d-200">Unclassified</span></span></td>
<td><span data-ttu-id="4775d-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="4775d-201">-10,000.00</span></span></td>
<td><span data-ttu-id="4775d-202">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-203">CC099</span><span class="sxs-lookup"><span data-stu-id="4775d-203">CC099</span></span></td>
<td><span data-ttu-id="4775d-204">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="4775d-204">Default cost center</span></span></td>
<td><span data-ttu-id="4775d-205">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-205">10001</span></span></td>
<td><span data-ttu-id="4775d-206">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-206">Electricity</span></span></td>
<td><span data-ttu-id="4775d-207">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-207">Fixed cost</span></span></td>
<td><span data-ttu-id="4775d-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="4775d-208">1,000.00</span></span></td>
<td><span data-ttu-id="4775d-209">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-210">CC099</span><span class="sxs-lookup"><span data-stu-id="4775d-210">CC099</span></span></td>
<td><span data-ttu-id="4775d-211">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="4775d-211">Default cost center</span></span></td>
<td><span data-ttu-id="4775d-212">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-212">10001</span></span></td>
<td><span data-ttu-id="4775d-213">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-213">Electricity</span></span></td>
<td><span data-ttu-id="4775d-214">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-214">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="4775d-215">9,000.00</span></span></td>
<td><span data-ttu-id="4775d-216">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4775d-217">Ohledně podrobných informací o chování nákladů nahlédněte do zásad chování nákladů.</span><span class="sxs-lookup"><span data-stu-id="4775d-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="4775d-218">(Všimněte si, že toto téma ještě není dokončené, ale bud k dispozici již brzy.)</span><span class="sxs-lookup"><span data-stu-id="4775d-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="4775d-219">Krok 2: Zpracování výpočtu distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="4775d-220">Distribuce nákladů se používá k rozdělení nákladů z jednoho objektu nákladů na jeden nebo více dalších objektů nákladů použitím příslušného základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="4775d-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="4775d-221">Distribuce nákladů a přidělení nákladů se liší v tom, že k distribuci nákladů dochází vždy na úrovni primárního prvku nákladů původních nákladů.</span><span class="sxs-lookup"><span data-stu-id="4775d-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="4775d-222">Definice pravidel distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-222">Define the cost distribution rule</span></span>

<span data-ttu-id="4775d-223">Ve finančním účetnictví se náklady na elektřinu často registrují jako paušální.</span><span class="sxs-lookup"><span data-stu-id="4775d-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="4775d-224">V nákladovém účetnictví není tento přístup dostatečně podrobný.</span><span class="sxs-lookup"><span data-stu-id="4775d-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="4775d-225">Variabilní náklady by měly být distribuovány k jednotlivým objektům nákladů na solidním základě.</span><span class="sxs-lookup"><span data-stu-id="4775d-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="4775d-226">Nejlogičtější základ přidělení je spotřeba elektřiny (kWh).</span><span class="sxs-lookup"><span data-stu-id="4775d-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="4775d-227">Vytvoří se člen statistické dimenzi s názvem Elektřina a zaznamená se elektrické spotřeba.</span><span class="sxs-lookup"><span data-stu-id="4775d-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="4775d-228">Ve výchozím nastavení se všechny členy statistické dimenze stanou dostupnými zpřístupněny jako základy přidělení.</span><span class="sxs-lookup"><span data-stu-id="4775d-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4775d-229">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-229">Cost object</span></span></th>
<th><span data-ttu-id="4775d-230">kWh</span><span class="sxs-lookup"><span data-stu-id="4775d-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4775d-231">CC001</span><span class="sxs-lookup"><span data-stu-id="4775d-231">CC001</span></span></td>
<td><span data-ttu-id="4775d-232">HR</span><span class="sxs-lookup"><span data-stu-id="4775d-232">HR</span></span></td>
<td><span data-ttu-id="4775d-233">1 000</span><span class="sxs-lookup"><span data-stu-id="4775d-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-234">CC002</span><span class="sxs-lookup"><span data-stu-id="4775d-234">CC002</span></span></td>
<td><span data-ttu-id="4775d-235">Finance</span><span class="sxs-lookup"><span data-stu-id="4775d-235">Finance</span></span></td>
<td><span data-ttu-id="4775d-236">6,000</span><span class="sxs-lookup"><span data-stu-id="4775d-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-237">CC003</span><span class="sxs-lookup"><span data-stu-id="4775d-237">CC003</span></span></td>
<td><span data-ttu-id="4775d-238">Sestavení</span><span class="sxs-lookup"><span data-stu-id="4775d-238">Assembly</span></span></td>
<td><span data-ttu-id="4775d-239">0</span><span class="sxs-lookup"><span data-stu-id="4775d-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4775d-240">Následující tabulka zobrazuje výsledek při použití elektrické spotřeby jako základu přidělení pro variabilní náklady.</span><span class="sxs-lookup"><span data-stu-id="4775d-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4775d-241">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-241">Cost object</span></span></th>
<th><span data-ttu-id="4775d-242">Hodnota</span><span class="sxs-lookup"><span data-stu-id="4775d-242">Magnitude</span></span></th>
<th><span data-ttu-id="4775d-243">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="4775d-243">Allocation factor</span></span></th>
<th><span data-ttu-id="4775d-244">Částka</span><span class="sxs-lookup"><span data-stu-id="4775d-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4775d-245">CC001</span><span class="sxs-lookup"><span data-stu-id="4775d-245">CC001</span></span></td>
<td><span data-ttu-id="4775d-246">HR</span><span class="sxs-lookup"><span data-stu-id="4775d-246">HR</span></span></td>
<td><span data-ttu-id="4775d-247">1 000</span><span class="sxs-lookup"><span data-stu-id="4775d-247">1,000</span></span></td>
<td><span data-ttu-id="4775d-248">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="4775d-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4775d-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="4775d-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-250">CC002</span><span class="sxs-lookup"><span data-stu-id="4775d-250">CC002</span></span></td>
<td><span data-ttu-id="4775d-251">Finance</span><span class="sxs-lookup"><span data-stu-id="4775d-251">Finance</span></span></td>
<td><span data-ttu-id="4775d-252">6,000</span><span class="sxs-lookup"><span data-stu-id="4775d-252">6,000</span></span></td>
<td><span data-ttu-id="4775d-253">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="4775d-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4775d-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="4775d-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-255">CC003</span><span class="sxs-lookup"><span data-stu-id="4775d-255">CC003</span></span></td>
<td><span data-ttu-id="4775d-256">Sestavení</span><span class="sxs-lookup"><span data-stu-id="4775d-256">Assembly</span></span></td>
<td><span data-ttu-id="4775d-257">0</span><span class="sxs-lookup"><span data-stu-id="4775d-257">0</span></span></td>
<td><span data-ttu-id="4775d-258">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="4775d-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4775d-259">0,00</span><span class="sxs-lookup"><span data-stu-id="4775d-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4775d-260">Pevné náklady musí být distribuovány rovnoměrně k jednotlivých objektům nákladů, které spotřebovávaly elektřinu.</span><span class="sxs-lookup"><span data-stu-id="4775d-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="4775d-261">Tohoto výsledku můžete dosáhnout pomocí členu statistické dimenze Elektřina v základu přidělení vzorce: (Elektřina &gt; 0,00) Následující tabulka zobrazuje výsledek při použití elektrické spotřeby jako základu přidělení pro variabilní náklady.</span><span class="sxs-lookup"><span data-stu-id="4775d-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4775d-262">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-262">Cost object</span></span></th>
<th><span data-ttu-id="4775d-263">Vzorec</span><span class="sxs-lookup"><span data-stu-id="4775d-263">Formula</span></span></th>
<th><span data-ttu-id="4775d-264">Hodnota</span><span class="sxs-lookup"><span data-stu-id="4775d-264">Magnitude</span></span></th>
<th><span data-ttu-id="4775d-265">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="4775d-265">Allocation factor</span></span></th>
<th><span data-ttu-id="4775d-266">Částka</span><span class="sxs-lookup"><span data-stu-id="4775d-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4775d-267">CC001</span><span class="sxs-lookup"><span data-stu-id="4775d-267">CC001</span></span></td>
<td><span data-ttu-id="4775d-268">HR</span><span class="sxs-lookup"><span data-stu-id="4775d-268">HR</span></span></td>
<td><span data-ttu-id="4775d-269">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="4775d-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4775d-270">1</span><span class="sxs-lookup"><span data-stu-id="4775d-270">1</span></span></td>
<td><span data-ttu-id="4775d-271">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="4775d-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4775d-272">500.00</span><span class="sxs-lookup"><span data-stu-id="4775d-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-273">CC002</span><span class="sxs-lookup"><span data-stu-id="4775d-273">CC002</span></span></td>
<td><span data-ttu-id="4775d-274">Finance</span><span class="sxs-lookup"><span data-stu-id="4775d-274">Finance</span></span></td>
<td><span data-ttu-id="4775d-275">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="4775d-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4775d-276">1</span><span class="sxs-lookup"><span data-stu-id="4775d-276">1</span></span></td>
<td><span data-ttu-id="4775d-277">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="4775d-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4775d-278">500.00</span><span class="sxs-lookup"><span data-stu-id="4775d-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-279">CC003</span><span class="sxs-lookup"><span data-stu-id="4775d-279">CC003</span></span></td>
<td><span data-ttu-id="4775d-280">Sestavení</span><span class="sxs-lookup"><span data-stu-id="4775d-280">Assembly</span></span></td>
<td><span data-ttu-id="4775d-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="4775d-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4775d-282">0</span><span class="sxs-lookup"><span data-stu-id="4775d-282">0</span></span></td>
<td><span data-ttu-id="4775d-283">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="4775d-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4775d-284">0,00</span><span class="sxs-lookup"><span data-stu-id="4775d-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="4775d-285">Deník</span><span class="sxs-lookup"><span data-stu-id="4775d-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4775d-286">Deník</span><span class="sxs-lookup"><span data-stu-id="4775d-286">Journal</span></span></th>
<th><span data-ttu-id="4775d-287">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="4775d-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4775d-288">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="4775d-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4775d-289">Verze</span><span class="sxs-lookup"><span data-stu-id="4775d-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4775d-290">00002</span><span class="sxs-lookup"><span data-stu-id="4775d-290">00002</span></span></td>
<td><span data-ttu-id="4775d-291">Deník výpočtu distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="4775d-292">Fiskální</span><span class="sxs-lookup"><span data-stu-id="4775d-292">Fiscal</span></span></td>
<td><span data-ttu-id="4775d-293">2017</span><span class="sxs-lookup"><span data-stu-id="4775d-293">2017</span></span></td>
<td><span data-ttu-id="4775d-294">Období 1</span><span class="sxs-lookup"><span data-stu-id="4775d-294">Period 1</span></span></td>
<td><span data-ttu-id="4775d-295">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="4775d-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4775d-296">Položky deníku (Položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="4775d-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4775d-297">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="4775d-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4775d-298">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4775d-299">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-299">Cost element</span></span></th>
<th><span data-ttu-id="4775d-300">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-300">Cost behavior</span></span></th>
<th><span data-ttu-id="4775d-301">Částka</span><span class="sxs-lookup"><span data-stu-id="4775d-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4775d-302">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="4775d-303">CC099</span><span class="sxs-lookup"><span data-stu-id="4775d-303">CC099</span></span></td>
<td><span data-ttu-id="4775d-304">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="4775d-304">Default cost center</span></span></td>
<td><span data-ttu-id="4775d-305">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-305">10001</span></span></td>
<td><span data-ttu-id="4775d-306">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-306">Electricity</span></span></td>
<td><span data-ttu-id="4775d-307">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-307">Fixed cost</span></span></td>
<td><span data-ttu-id="4775d-308">1 000,00</span><span class="sxs-lookup"><span data-stu-id="4775d-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-309">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="4775d-310">CC099</span><span class="sxs-lookup"><span data-stu-id="4775d-310">CC099</span></span></td>
<td><span data-ttu-id="4775d-311">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="4775d-311">Default cost center</span></span></td>
<td><span data-ttu-id="4775d-312">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-312">10001</span></span></td>
<td><span data-ttu-id="4775d-313">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-313">Electricity</span></span></td>
<td><span data-ttu-id="4775d-314">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-314">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="4775d-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4775d-316">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4775d-317">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4775d-318">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-318">Cost element</span></span></th>
<th><span data-ttu-id="4775d-319">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-319">Cost behavior</span></span></th>
<th><span data-ttu-id="4775d-320">Částka</span><span class="sxs-lookup"><span data-stu-id="4775d-320">Amount</span></span></th>
<th><span data-ttu-id="4775d-321">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="4775d-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4775d-322">CC099</span><span class="sxs-lookup"><span data-stu-id="4775d-322">CC099</span></span></td>
<td><span data-ttu-id="4775d-323">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="4775d-323">Default cost center</span></span></td>
<td><span data-ttu-id="4775d-324">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-324">10001</span></span></td>
<td><span data-ttu-id="4775d-325">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-325">Electricity</span></span></td>
<td><span data-ttu-id="4775d-326">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-326">Fixed cost</span></span></td>
<td><span data-ttu-id="4775d-327">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="4775d-327">-1,000.00</span></span></td>
<td><span data-ttu-id="4775d-328">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-329">CC001</span><span class="sxs-lookup"><span data-stu-id="4775d-329">CC001</span></span></td>
<td><span data-ttu-id="4775d-330">HR</span><span class="sxs-lookup"><span data-stu-id="4775d-330">HR</span></span></td>
<td><span data-ttu-id="4775d-331">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-331">10001</span></span></td>
<td><span data-ttu-id="4775d-332">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-332">Electricity</span></span></td>
<td><span data-ttu-id="4775d-333">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-333">Fixed cost</span></span></td>
<td><span data-ttu-id="4775d-334">500.00</span><span class="sxs-lookup"><span data-stu-id="4775d-334">500.00</span></span></td>
<td><span data-ttu-id="4775d-335">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-336">CC002</span><span class="sxs-lookup"><span data-stu-id="4775d-336">CC002</span></span></td>
<td><span data-ttu-id="4775d-337">Finance</span><span class="sxs-lookup"><span data-stu-id="4775d-337">Finance</span></span></td>
<td><span data-ttu-id="4775d-338">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-338">10001</span></span></td>
<td><span data-ttu-id="4775d-339">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-339">Electricity</span></span></td>
<td><span data-ttu-id="4775d-340">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-340">Fixed cost</span></span></td>
<td><span data-ttu-id="4775d-341">500.00</span><span class="sxs-lookup"><span data-stu-id="4775d-341">500.00</span></span></td>
<td><span data-ttu-id="4775d-342">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-343">CC099</span><span class="sxs-lookup"><span data-stu-id="4775d-343">CC099</span></span></td>
<td><span data-ttu-id="4775d-344">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="4775d-344">Default cost center</span></span></td>
<td><span data-ttu-id="4775d-345">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-345">10001</span></span></td>
<td><span data-ttu-id="4775d-346">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-346">Electricity</span></span></td>
<td><span data-ttu-id="4775d-347">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-347">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-348">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="4775d-348">-9,000.00</span></span></td>
<td><span data-ttu-id="4775d-349">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-350">CC001</span><span class="sxs-lookup"><span data-stu-id="4775d-350">CC001</span></span></td>
<td><span data-ttu-id="4775d-351">HR</span><span class="sxs-lookup"><span data-stu-id="4775d-351">HR</span></span></td>
<td><span data-ttu-id="4775d-352">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-352">10001</span></span></td>
<td><span data-ttu-id="4775d-353">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-353">Electricity</span></span></td>
<td><span data-ttu-id="4775d-354">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-354">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="4775d-355">1,285.71</span></span></td>
<td><span data-ttu-id="4775d-356">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-357">CC002</span><span class="sxs-lookup"><span data-stu-id="4775d-357">CC002</span></span></td>
<td><span data-ttu-id="4775d-358">Finance</span><span class="sxs-lookup"><span data-stu-id="4775d-358">Finance</span></span></td>
<td><span data-ttu-id="4775d-359">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-359">10001</span></span></td>
<td><span data-ttu-id="4775d-360">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-360">Electricity</span></span></td>
<td><span data-ttu-id="4775d-361">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-361">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="4775d-362">7,714.29</span></span></td>
<td><span data-ttu-id="4775d-363">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4775d-364">Podrobné informace o základech distribuce a přidělení nákladů získáte v tématech Zásady distribuce nákladů a Základy přidělení.</span><span class="sxs-lookup"><span data-stu-id="4775d-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="4775d-365">(Všimněte si, že toto téma ještě není dokončené, ale bud k dispozici již brzy.)</span><span class="sxs-lookup"><span data-stu-id="4775d-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="4775d-366">Krok 3: Zpracování výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="4775d-367">Režijní náklady se používají k účtování jednoho nebo více konkrétních objektů nákladů.</span><span class="sxs-lookup"><span data-stu-id="4775d-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="4775d-368">Účtování je založeno na předem určené nákladové sazbě a množství z přiřazeného základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="4775d-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="4775d-369">Definice sazby režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-369">Define the overhead rate</span></span>

<span data-ttu-id="4775d-370">Objekt nákladů CC001 HR přispívá k sadě interních projektů.</span><span class="sxs-lookup"><span data-stu-id="4775d-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="4775d-371">Vytvoří se člen statistické dimenzi s názvem projekty lidských zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="4775d-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4775d-372">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-372">Cost object</span></span></th>
<th><span data-ttu-id="4775d-373">Pracovní doba</span><span class="sxs-lookup"><span data-stu-id="4775d-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4775d-374">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4775d-374">Proj 1</span></span></td>
<td><span data-ttu-id="4775d-375">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="4775d-375">Project 1</span></span></td>
<td><span data-ttu-id="4775d-376">3</span><span class="sxs-lookup"><span data-stu-id="4775d-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-377">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4775d-377">Proj 2</span></span></td>
<td><span data-ttu-id="4775d-378">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="4775d-378">Project 2</span></span></td>
<td><span data-ttu-id="4775d-379">1</span><span class="sxs-lookup"><span data-stu-id="4775d-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4775d-380">Byla definována předem určená nákladová sazba pro příspěvky k nákladovým projektům.</span><span class="sxs-lookup"><span data-stu-id="4775d-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4775d-381">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-381">Cost object</span></span></th>
<th><span data-ttu-id="4775d-382">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-382">Cost element</span></span></th>
<th><span data-ttu-id="4775d-383">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-383">Cost behavior</span></span></th>
<th><span data-ttu-id="4775d-384">Jednotky</span><span class="sxs-lookup"><span data-stu-id="4775d-384">Units</span></span></th>
<th><span data-ttu-id="4775d-385">Kurz</span><span class="sxs-lookup"><span data-stu-id="4775d-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4775d-386">CC001</span><span class="sxs-lookup"><span data-stu-id="4775d-386">CC001</span></span></td>
<td><span data-ttu-id="4775d-387">HR</span><span class="sxs-lookup"><span data-stu-id="4775d-387">HR</span></span></td>
<td><span data-ttu-id="4775d-388">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-388">10001</span></span></td>
<td><span data-ttu-id="4775d-389">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-389">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-390">1</span><span class="sxs-lookup"><span data-stu-id="4775d-390">1</span></span></td>
<td><span data-ttu-id="4775d-391">10</span><span class="sxs-lookup"><span data-stu-id="4775d-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4775d-392">Následující tabulka zobrazuje výsledek při použití projektů lidských zdrojů jako základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="4775d-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4775d-393">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-393">Cost object</span></span></th>
<th><span data-ttu-id="4775d-394">Hodnota</span><span class="sxs-lookup"><span data-stu-id="4775d-394">Magnitude</span></span></th>
<th><span data-ttu-id="4775d-395">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-395">Cost element</span></span></th>
<th><span data-ttu-id="4775d-396">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="4775d-396">Allocation factor</span></span></th>
<th><span data-ttu-id="4775d-397">Částka</span><span class="sxs-lookup"><span data-stu-id="4775d-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4775d-398">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4775d-398">Proj 1</span></span></td>
<td><span data-ttu-id="4775d-399">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="4775d-399">Project 1</span></span></td>
<td><span data-ttu-id="4775d-400">3</span><span class="sxs-lookup"><span data-stu-id="4775d-400">3</span></span></td>
<td><span data-ttu-id="4775d-401">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-401">10001</span></span></td>
<td><span data-ttu-id="4775d-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="4775d-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="4775d-403">30.00</span><span class="sxs-lookup"><span data-stu-id="4775d-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-404">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4775d-404">Proj 2</span></span></td>
<td><span data-ttu-id="4775d-405">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="4775d-405">Project 2</span></span></td>
<td><span data-ttu-id="4775d-406">1</span><span class="sxs-lookup"><span data-stu-id="4775d-406">1</span></span></td>
<td><span data-ttu-id="4775d-407">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-407">10001</span></span></td>
<td><span data-ttu-id="4775d-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="4775d-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="4775d-409">10,00</span><span class="sxs-lookup"><span data-stu-id="4775d-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="4775d-410">Deník</span><span class="sxs-lookup"><span data-stu-id="4775d-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4775d-411">Deník</span><span class="sxs-lookup"><span data-stu-id="4775d-411">Journal</span></span></th>
<th><span data-ttu-id="4775d-412">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="4775d-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4775d-413">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="4775d-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4775d-414">Verze</span><span class="sxs-lookup"><span data-stu-id="4775d-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4775d-415">00003</span><span class="sxs-lookup"><span data-stu-id="4775d-415">00003</span></span></td>
<td><span data-ttu-id="4775d-416">Deník výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="4775d-417">Fiskální</span><span class="sxs-lookup"><span data-stu-id="4775d-417">Fiscal</span></span></td>
<td><span data-ttu-id="4775d-418">2017</span><span class="sxs-lookup"><span data-stu-id="4775d-418">2017</span></span></td>
<td><span data-ttu-id="4775d-419">Období 1</span><span class="sxs-lookup"><span data-stu-id="4775d-419">Period 1</span></span></td>
<td><span data-ttu-id="4775d-420">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="4775d-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="4775d-421">Položky deníku (položky deníku pro výpočet sazby režijních nákladů)</span><span class="sxs-lookup"><span data-stu-id="4775d-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4775d-422">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="4775d-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4775d-423">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-423">Cost object</span></span></th>
<th><span data-ttu-id="4775d-424">Hodnota</span><span class="sxs-lookup"><span data-stu-id="4775d-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4775d-425">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="4775d-426">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4775d-426">Proj 1</span></span></td>
<td><span data-ttu-id="4775d-427">Interní projekt 1</span><span class="sxs-lookup"><span data-stu-id="4775d-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="4775d-428">3,00</span><span class="sxs-lookup"><span data-stu-id="4775d-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-429">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="4775d-430">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4775d-430">Proj 2</span></span></td>
<td><span data-ttu-id="4775d-431">Interní projekt 2</span><span class="sxs-lookup"><span data-stu-id="4775d-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="4775d-432">1.00</span><span class="sxs-lookup"><span data-stu-id="4775d-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4775d-433">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4775d-434">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4775d-435">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-435">Cost element</span></span></th>
<th><span data-ttu-id="4775d-436">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-436">Cost behavior</span></span></th>
<th><span data-ttu-id="4775d-437">Částka</span><span class="sxs-lookup"><span data-stu-id="4775d-437">Amount</span></span></th>
<th><span data-ttu-id="4775d-438">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="4775d-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4775d-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="4775d-439">CC0001</span></span></td>
<td><span data-ttu-id="4775d-440">HR</span><span class="sxs-lookup"><span data-stu-id="4775d-440">HR</span></span></td>
<td><span data-ttu-id="4775d-441">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-441">10001</span></span></td>
<td><span data-ttu-id="4775d-442">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-442">Electricity</span></span></td>
<td><span data-ttu-id="4775d-443">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-443">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-444">-30,00</span><span class="sxs-lookup"><span data-stu-id="4775d-444">-30.00</span></span></td>
<td><span data-ttu-id="4775d-445">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-446">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4775d-446">Proj 1</span></span></td>
<td><span data-ttu-id="4775d-447">Interní projekt 1</span><span class="sxs-lookup"><span data-stu-id="4775d-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="4775d-448">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-448">10001</span></span></td>
<td><span data-ttu-id="4775d-449">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-449">Electricity</span></span></td>
<td><span data-ttu-id="4775d-450">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-450">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-451">30.00</span><span class="sxs-lookup"><span data-stu-id="4775d-451">30.00</span></span></td>
<td><span data-ttu-id="4775d-452">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-453">CC001</span><span class="sxs-lookup"><span data-stu-id="4775d-453">CC001</span></span></td>
<td><span data-ttu-id="4775d-454">HR</span><span class="sxs-lookup"><span data-stu-id="4775d-454">HR</span></span></td>
<td><span data-ttu-id="4775d-455">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-455">10001</span></span></td>
<td><span data-ttu-id="4775d-456">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-456">Electricity</span></span></td>
<td><span data-ttu-id="4775d-457">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-457">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-458">-10,00</span><span class="sxs-lookup"><span data-stu-id="4775d-458">-10.00</span></span></td>
<td><span data-ttu-id="4775d-459">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-460">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4775d-460">Proj 2</span></span></td>
<td><span data-ttu-id="4775d-461">Interní projekt 2</span><span class="sxs-lookup"><span data-stu-id="4775d-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="4775d-462">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-462">10001</span></span></td>
<td><span data-ttu-id="4775d-463">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-463">Electricity</span></span></td>
<td><span data-ttu-id="4775d-464">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-464">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-465">10,00</span><span class="sxs-lookup"><span data-stu-id="4775d-465">10.00</span></span></td>
<td><span data-ttu-id="4775d-466">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4775d-467">Podrobné informace o zásadách sazby režijních nákladů najdete v tématech Zásady sazby režijních nákladů a Základy přidělení.</span><span class="sxs-lookup"><span data-stu-id="4775d-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="4775d-468">(Všimněte si, že toto téma ještě není dokončené, ale bud k dispozici již brzy.)</span><span class="sxs-lookup"><span data-stu-id="4775d-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="4775d-469">Krok 4: Zpracování výpočtu přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="4775d-470">Přidělení se používá k přidělení zůstatku objektu nákladů do jiných objektů nákladů použitím základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="4775d-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="4775d-471">Aplikace Finance and Operations podporuje reciproční metodu přidělování.</span><span class="sxs-lookup"><span data-stu-id="4775d-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="4775d-472">V metodě vzájemného přidělení jsou plně rozpoznány vzájemné služby, které si vyměňují pomocné objekty nákladů.</span><span class="sxs-lookup"><span data-stu-id="4775d-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="4775d-473">Systém automaticky určí provádění přidělení ve správném pořadí.</span><span class="sxs-lookup"><span data-stu-id="4775d-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="4775d-474">Zůstatek objektu nákladů je přidělen jedním základem přidělení.</span><span class="sxs-lookup"><span data-stu-id="4775d-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="4775d-475">Je podporováno přidělování napříč dimenzemi objektů nákladů a jejich příslušných členů.</span><span class="sxs-lookup"><span data-stu-id="4775d-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="4775d-476">Pořadí přidělení je řízeno jednotkou řízení nákladů.</span><span class="sxs-lookup"><span data-stu-id="4775d-476">The allocation order is controlled by the cost control unit.</span></span> <span data-ttu-id="4775d-477">[![Reciproční metoda](./media/reciprocal-method.png)]</span><span class="sxs-lookup"><span data-stu-id="4775d-477">[![Reciprocal method](./media/reciprocal-method.png)]</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="4775d-478">Definice přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-478">Define the cost allocation</span></span>

<span data-ttu-id="4775d-479">Toto je jednoduchý příklad, který vysvětluje, jakým způsobem lze sledovat tok nákladů.</span><span class="sxs-lookup"><span data-stu-id="4775d-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="4775d-480">Objekt nákladů objektu CC001 HR přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="4775d-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="4775d-481">Vytvoří se člen statistické dimenzi s názvem služby lidských zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="4775d-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4775d-482">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-482">Cost object</span></span></th>
<th><span data-ttu-id="4775d-483">Služby HR</span><span class="sxs-lookup"><span data-stu-id="4775d-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4775d-484">CC002</span><span class="sxs-lookup"><span data-stu-id="4775d-484">CC002</span></span></td>
<td><span data-ttu-id="4775d-485">Finance</span><span class="sxs-lookup"><span data-stu-id="4775d-485">Finance</span></span></td>
<td><span data-ttu-id="4775d-486">35</span><span class="sxs-lookup"><span data-stu-id="4775d-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-487">CC003</span><span class="sxs-lookup"><span data-stu-id="4775d-487">CC003</span></span></td>
<td><span data-ttu-id="4775d-488">Sestavení</span><span class="sxs-lookup"><span data-stu-id="4775d-488">Assembly</span></span></td>
<td><span data-ttu-id="4775d-489">55</span><span class="sxs-lookup"><span data-stu-id="4775d-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-490">CC004</span><span class="sxs-lookup"><span data-stu-id="4775d-490">CC004</span></span></td>
<td><span data-ttu-id="4775d-491">Balení</span><span class="sxs-lookup"><span data-stu-id="4775d-491">Packaging</span></span></td>
<td><span data-ttu-id="4775d-492">10</span><span class="sxs-lookup"><span data-stu-id="4775d-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4775d-493">Objekt nákladů objektu CC002 Finance přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="4775d-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="4775d-494">Vytvoří se člen statistické dimenzi s názvem Finanční služby k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="4775d-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4775d-495">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-495">Cost object</span></span></th>
<th><span data-ttu-id="4775d-496">Finanční služby</span><span class="sxs-lookup"><span data-stu-id="4775d-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4775d-497">CC003</span><span class="sxs-lookup"><span data-stu-id="4775d-497">CC003</span></span></td>
<td><span data-ttu-id="4775d-498">Sestavení</span><span class="sxs-lookup"><span data-stu-id="4775d-498">Assembly</span></span></td>
<td><span data-ttu-id="4775d-499">65</span><span class="sxs-lookup"><span data-stu-id="4775d-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-500">CC004</span><span class="sxs-lookup"><span data-stu-id="4775d-500">CC004</span></span></td>
<td><span data-ttu-id="4775d-501">Balení</span><span class="sxs-lookup"><span data-stu-id="4775d-501">Packaging</span></span></td>
<td><span data-ttu-id="4775d-502">35</span><span class="sxs-lookup"><span data-stu-id="4775d-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4775d-503">Objekt nákladů objektu CC003 Sestavení přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="4775d-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="4775d-504">Vytvoří se člen statistické dimenzi s názvem Služby sestavení zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="4775d-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4775d-505">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-505">Cost object</span></span></th>
<th><span data-ttu-id="4775d-506">Služby sestavení (v hodinách)</span><span class="sxs-lookup"><span data-stu-id="4775d-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4775d-507">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4775d-507">Prod 1</span></span></td>
<td><span data-ttu-id="4775d-508">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4775d-508">Product 1</span></span></td>
<td><span data-ttu-id="4775d-509">60</span><span class="sxs-lookup"><span data-stu-id="4775d-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-510">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4775d-510">Prod 2</span></span></td>
<td><span data-ttu-id="4775d-511">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="4775d-511">Product 2</span></span></td>
<td><span data-ttu-id="4775d-512">20</span><span class="sxs-lookup"><span data-stu-id="4775d-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4775d-513">Objekt nákladů objektu CC004 Balení přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="4775d-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="4775d-514">Vytvoří se člen statistické dimenzi s názvem Služby balení k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="4775d-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4775d-515">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-515">Cost object</span></span></th>
<th><span data-ttu-id="4775d-516">Služby balení (v hodinách)</span><span class="sxs-lookup"><span data-stu-id="4775d-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4775d-517">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4775d-517">Prod 1</span></span></td>
<td><span data-ttu-id="4775d-518">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4775d-518">Product 1</span></span></td>
<td><span data-ttu-id="4775d-519">80</span><span class="sxs-lookup"><span data-stu-id="4775d-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-520">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4775d-520">Prod 2</span></span></td>
<td><span data-ttu-id="4775d-521">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="4775d-521">Product 2</span></span></td>
<td><span data-ttu-id="4775d-522">září</span><span class="sxs-lookup"><span data-stu-id="4775d-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4775d-523">**Poznámka:** V aplikaci Finance and Operations lze odvodit statistická měření, jako je například výrobní doba spotřebovaná produktem, z datového zdroje.</span><span class="sxs-lookup"><span data-stu-id="4775d-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="4775d-524">Podrobnější informace o poskytovatelích statistických měření získáte v tématu Šablony poskytovatelů statistického měření.</span><span class="sxs-lookup"><span data-stu-id="4775d-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="4775d-525">(Všimněte si, že toto téma ještě není dokončeno, ale bude k dispozici brzy.) V následující tabulce jsou uvedeny výsledky použití HR služeb HR jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="4775d-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4775d-526">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-526">Cost object</span></span></th>
<th><span data-ttu-id="4775d-527">Hodnota</span><span class="sxs-lookup"><span data-stu-id="4775d-527">Magnitude</span></span></th>
<th><span data-ttu-id="4775d-528">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="4775d-528">Allocation factor</span></span></th>
<th><span data-ttu-id="4775d-529">Částka</span><span class="sxs-lookup"><span data-stu-id="4775d-529">Amount</span></span></th>
<th><span data-ttu-id="4775d-530">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4775d-531">CC002</span><span class="sxs-lookup"><span data-stu-id="4775d-531">CC002</span></span></td>
<td><span data-ttu-id="4775d-532">Finance</span><span class="sxs-lookup"><span data-stu-id="4775d-532">Finance</span></span></td>
<td><span data-ttu-id="4775d-533">35</span><span class="sxs-lookup"><span data-stu-id="4775d-533">35</span></span></td>
<td><span data-ttu-id="4775d-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="4775d-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4775d-535">175.00</span><span class="sxs-lookup"><span data-stu-id="4775d-535">175.00</span></span></td>
<td><span data-ttu-id="4775d-536">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-537">CC003</span><span class="sxs-lookup"><span data-stu-id="4775d-537">CC003</span></span></td>
<td><span data-ttu-id="4775d-538">Sestavení</span><span class="sxs-lookup"><span data-stu-id="4775d-538">Assembly</span></span></td>
<td><span data-ttu-id="4775d-539">55</span><span class="sxs-lookup"><span data-stu-id="4775d-539">55</span></span></td>
<td><span data-ttu-id="4775d-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="4775d-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4775d-541">275.00</span><span class="sxs-lookup"><span data-stu-id="4775d-541">275.00</span></span></td>
<td><span data-ttu-id="4775d-542">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-543">CC004</span><span class="sxs-lookup"><span data-stu-id="4775d-543">CC004</span></span></td>
<td><span data-ttu-id="4775d-544">Balení</span><span class="sxs-lookup"><span data-stu-id="4775d-544">Packaging</span></span></td>
<td><span data-ttu-id="4775d-545">10</span><span class="sxs-lookup"><span data-stu-id="4775d-545">10</span></span></td>
<td><span data-ttu-id="4775d-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="4775d-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4775d-547">50,00</span><span class="sxs-lookup"><span data-stu-id="4775d-547">50.00</span></span></td>
<td><span data-ttu-id="4775d-548">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-549">CC002</span><span class="sxs-lookup"><span data-stu-id="4775d-549">CC002</span></span></td>
<td><span data-ttu-id="4775d-550">Finance</span><span class="sxs-lookup"><span data-stu-id="4775d-550">Finance</span></span></td>
<td><span data-ttu-id="4775d-551">35</span><span class="sxs-lookup"><span data-stu-id="4775d-551">35</span></span></td>
<td><span data-ttu-id="4775d-552">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="4775d-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4775d-553">436.00</span><span class="sxs-lookup"><span data-stu-id="4775d-553">436.00</span></span></td>
<td><span data-ttu-id="4775d-554">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-555">CC003</span><span class="sxs-lookup"><span data-stu-id="4775d-555">CC003</span></span></td>
<td><span data-ttu-id="4775d-556">Sestavení</span><span class="sxs-lookup"><span data-stu-id="4775d-556">Assembly</span></span></td>
<td><span data-ttu-id="4775d-557">55</span><span class="sxs-lookup"><span data-stu-id="4775d-557">55</span></span></td>
<td><span data-ttu-id="4775d-558">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="4775d-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4775d-559">685.14</span><span class="sxs-lookup"><span data-stu-id="4775d-559">685.14</span></span></td>
<td><span data-ttu-id="4775d-560">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-561">CC004</span><span class="sxs-lookup"><span data-stu-id="4775d-561">CC004</span></span></td>
<td><span data-ttu-id="4775d-562">Balení</span><span class="sxs-lookup"><span data-stu-id="4775d-562">Packaging</span></span></td>
<td><span data-ttu-id="4775d-563">10</span><span class="sxs-lookup"><span data-stu-id="4775d-563">10</span></span></td>
<td><span data-ttu-id="4775d-564">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="4775d-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4775d-565">124.57</span><span class="sxs-lookup"><span data-stu-id="4775d-565">124.57</span></span></td>
<td><span data-ttu-id="4775d-566">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4775d-567">V následující tabulce je uveden výsledek při použití Finančních služeb Finance jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="4775d-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4775d-568">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-568">Cost object</span></span></th>
<th><span data-ttu-id="4775d-569">Hodnota</span><span class="sxs-lookup"><span data-stu-id="4775d-569">Magnitude</span></span></th>
<th><span data-ttu-id="4775d-570">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="4775d-570">Allocation factor</span></span></th>
<th><span data-ttu-id="4775d-571">Částka</span><span class="sxs-lookup"><span data-stu-id="4775d-571">Amount</span></span></th>
<th><span data-ttu-id="4775d-572">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4775d-573">CC003</span><span class="sxs-lookup"><span data-stu-id="4775d-573">CC003</span></span></td>
<td><span data-ttu-id="4775d-574">Sestavení</span><span class="sxs-lookup"><span data-stu-id="4775d-574">Assembly</span></span></td>
<td><span data-ttu-id="4775d-575">65</span><span class="sxs-lookup"><span data-stu-id="4775d-575">65</span></span></td>
<td><span data-ttu-id="4775d-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="4775d-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="4775d-577">438.75</span><span class="sxs-lookup"><span data-stu-id="4775d-577">438.75</span></span></td>
<td><span data-ttu-id="4775d-578">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-579">CC004</span><span class="sxs-lookup"><span data-stu-id="4775d-579">CC004</span></span></td>
<td><span data-ttu-id="4775d-580">Balení</span><span class="sxs-lookup"><span data-stu-id="4775d-580">Packaging</span></span></td>
<td><span data-ttu-id="4775d-581">35</span><span class="sxs-lookup"><span data-stu-id="4775d-581">35</span></span></td>
<td><span data-ttu-id="4775d-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="4775d-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="4775d-583">236.25</span><span class="sxs-lookup"><span data-stu-id="4775d-583">236.25</span></span></td>
<td><span data-ttu-id="4775d-584">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-585">CC003</span><span class="sxs-lookup"><span data-stu-id="4775d-585">CC003</span></span></td>
<td><span data-ttu-id="4775d-586">Sestavení</span><span class="sxs-lookup"><span data-stu-id="4775d-586">Assembly</span></span></td>
<td><span data-ttu-id="4775d-587">65</span><span class="sxs-lookup"><span data-stu-id="4775d-587">65</span></span></td>
<td><span data-ttu-id="4775d-588">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="4775d-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="4775d-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="4775d-589">5,297.69</span></span></td>
<td><span data-ttu-id="4775d-590">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-591">CC004</span><span class="sxs-lookup"><span data-stu-id="4775d-591">CC004</span></span></td>
<td><span data-ttu-id="4775d-592">Balení</span><span class="sxs-lookup"><span data-stu-id="4775d-592">Packaging</span></span></td>
<td><span data-ttu-id="4775d-593">35</span><span class="sxs-lookup"><span data-stu-id="4775d-593">35</span></span></td>
<td><span data-ttu-id="4775d-594">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="4775d-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="4775d-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="4775d-595">2,852.60</span></span></td>
<td><span data-ttu-id="4775d-596">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4775d-597">V následující tabulce je uveden výsledek při použití Služeb sestavení jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="4775d-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4775d-598">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-598">Cost object</span></span></th>
<th><span data-ttu-id="4775d-599">Hodnota</span><span class="sxs-lookup"><span data-stu-id="4775d-599">Magnitude</span></span></th>
<th><span data-ttu-id="4775d-600">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="4775d-600">Allocation factor</span></span></th>
<th><span data-ttu-id="4775d-601">Částka</span><span class="sxs-lookup"><span data-stu-id="4775d-601">Amount</span></span></th>
<th><span data-ttu-id="4775d-602">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4775d-603">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4775d-603">Prod 1</span></span></td>
<td><span data-ttu-id="4775d-604">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4775d-604">Product 1</span></span></td>
<td><span data-ttu-id="4775d-605">60</span><span class="sxs-lookup"><span data-stu-id="4775d-605">60</span></span></td>
<td><span data-ttu-id="4775d-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="4775d-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="4775d-607">535.31</span><span class="sxs-lookup"><span data-stu-id="4775d-607">535.31</span></span></td>
<td><span data-ttu-id="4775d-608">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-609">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4775d-609">Prod 2</span></span></td>
<td><span data-ttu-id="4775d-610">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="4775d-610">Product 2</span></span></td>
<td><span data-ttu-id="4775d-611">20</span><span class="sxs-lookup"><span data-stu-id="4775d-611">20</span></span></td>
<td><span data-ttu-id="4775d-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="4775d-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="4775d-613">178.44</span><span class="sxs-lookup"><span data-stu-id="4775d-613">178.44</span></span></td>
<td><span data-ttu-id="4775d-614">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-615">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4775d-615">Prod 1</span></span></td>
<td><span data-ttu-id="4775d-616">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4775d-616">Product 1</span></span></td>
<td><span data-ttu-id="4775d-617">60</span><span class="sxs-lookup"><span data-stu-id="4775d-617">60</span></span></td>
<td><span data-ttu-id="4775d-618">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="4775d-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="4775d-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="4775d-619">4,487.12</span></span></td>
<td><span data-ttu-id="4775d-620">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-621">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4775d-621">Prod 2</span></span></td>
<td><span data-ttu-id="4775d-622">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="4775d-622">Product 2</span></span></td>
<td><span data-ttu-id="4775d-623">20</span><span class="sxs-lookup"><span data-stu-id="4775d-623">20</span></span></td>
<td><span data-ttu-id="4775d-624">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="4775d-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="4775d-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="4775d-625">1,495.71</span></span></td>
<td><span data-ttu-id="4775d-626">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4775d-627">V následující tabulce je uveden výsledek při použití Služeb balení jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="4775d-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4775d-628">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-628">Cost object</span></span></th>
<th><span data-ttu-id="4775d-629">Hodnota</span><span class="sxs-lookup"><span data-stu-id="4775d-629">Magnitude</span></span></th>
<th><span data-ttu-id="4775d-630">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="4775d-630">Allocation factor</span></span></th>
<th><span data-ttu-id="4775d-631">Částka</span><span class="sxs-lookup"><span data-stu-id="4775d-631">Amount</span></span></th>
<th><span data-ttu-id="4775d-632">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4775d-633">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4775d-633">Prod 1</span></span></td>
<td><span data-ttu-id="4775d-634">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4775d-634">Product 1</span></span></td>
<td><span data-ttu-id="4775d-635">80</span><span class="sxs-lookup"><span data-stu-id="4775d-635">80</span></span></td>
<td><span data-ttu-id="4775d-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="4775d-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="4775d-637">241.05</span><span class="sxs-lookup"><span data-stu-id="4775d-637">241.05</span></span></td>
<td><span data-ttu-id="4775d-638">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-639">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4775d-639">Prod 2</span></span></td>
<td><span data-ttu-id="4775d-640">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="4775d-640">Product 2</span></span></td>
<td><span data-ttu-id="4775d-641">15</span><span class="sxs-lookup"><span data-stu-id="4775d-641">15</span></span></td>
<td><span data-ttu-id="4775d-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="4775d-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="4775d-643">45.20</span><span class="sxs-lookup"><span data-stu-id="4775d-643">45.20</span></span></td>
<td><span data-ttu-id="4775d-644">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-645">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4775d-645">Prod 1</span></span></td>
<td><span data-ttu-id="4775d-646">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4775d-646">Product 1</span></span></td>
<td><span data-ttu-id="4775d-647">80</span><span class="sxs-lookup"><span data-stu-id="4775d-647">80</span></span></td>
<td><span data-ttu-id="4775d-648">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="4775d-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="4775d-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="4775d-649">2,507.09</span></span></td>
<td><span data-ttu-id="4775d-650">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-651">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4775d-651">Prod 2</span></span></td>
<td><span data-ttu-id="4775d-652">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="4775d-652">Product 2</span></span></td>
<td><span data-ttu-id="4775d-653">15</span><span class="sxs-lookup"><span data-stu-id="4775d-653">15</span></span></td>
<td><span data-ttu-id="4775d-654">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="4775d-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="4775d-655">470.08</span><span class="sxs-lookup"><span data-stu-id="4775d-655">470.08</span></span></td>
<td><span data-ttu-id="4775d-656">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4775d-657">Položky deníku (položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="4775d-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4775d-658">Deník</span><span class="sxs-lookup"><span data-stu-id="4775d-658">Journal</span></span></th>
<th><span data-ttu-id="4775d-659">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="4775d-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4775d-660">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="4775d-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4775d-661">Verze</span><span class="sxs-lookup"><span data-stu-id="4775d-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4775d-662">00004</span><span class="sxs-lookup"><span data-stu-id="4775d-662">00004</span></span></td>
<td><span data-ttu-id="4775d-663">Deník přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="4775d-664">Fiskální</span><span class="sxs-lookup"><span data-stu-id="4775d-664">Fiscal</span></span></td>
<td><span data-ttu-id="4775d-665">2017</span><span class="sxs-lookup"><span data-stu-id="4775d-665">2017</span></span></td>
<td><span data-ttu-id="4775d-666">Období 1</span><span class="sxs-lookup"><span data-stu-id="4775d-666">Period 1</span></span></td>
<td><span data-ttu-id="4775d-667">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="4775d-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="4775d-668">Řádky deníku</span><span class="sxs-lookup"><span data-stu-id="4775d-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4775d-669">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="4775d-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4775d-670">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4775d-671">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-671">Cost element</span></span></th>
<th><span data-ttu-id="4775d-672">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-672">Cost behavior</span></span></th>
<th><span data-ttu-id="4775d-673">Částka</span><span class="sxs-lookup"><span data-stu-id="4775d-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4775d-674">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="4775d-675">CC001</span><span class="sxs-lookup"><span data-stu-id="4775d-675">CC001</span></span></td>
<td><span data-ttu-id="4775d-676">HR</span><span class="sxs-lookup"><span data-stu-id="4775d-676">HR</span></span></td>
<td><span data-ttu-id="4775d-677">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-677">10001</span></span></td>
<td><span data-ttu-id="4775d-678">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-678">Electricity</span></span></td>
<td><span data-ttu-id="4775d-679">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-679">Fixed cost</span></span></td>
<td><span data-ttu-id="4775d-680">500.00</span><span class="sxs-lookup"><span data-stu-id="4775d-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-681">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="4775d-682">CC001</span><span class="sxs-lookup"><span data-stu-id="4775d-682">CC001</span></span></td>
<td><span data-ttu-id="4775d-683">HR</span><span class="sxs-lookup"><span data-stu-id="4775d-683">HR</span></span></td>
<td><span data-ttu-id="4775d-684">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-684">10001</span></span></td>
<td><span data-ttu-id="4775d-685">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-685">Electricity</span></span></td>
<td><span data-ttu-id="4775d-686">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-686">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="4775d-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-688">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="4775d-689">CC002</span><span class="sxs-lookup"><span data-stu-id="4775d-689">CC002</span></span></td>
<td><span data-ttu-id="4775d-690">Finance</span><span class="sxs-lookup"><span data-stu-id="4775d-690">Finance</span></span></td>
<td><span data-ttu-id="4775d-691">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-691">10001</span></span></td>
<td><span data-ttu-id="4775d-692">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-692">Electricity</span></span></td>
<td><span data-ttu-id="4775d-693">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-693">Fixed cost</span></span></td>
<td><span data-ttu-id="4775d-694">675.00</span><span class="sxs-lookup"><span data-stu-id="4775d-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-695">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="4775d-696">CC002</span><span class="sxs-lookup"><span data-stu-id="4775d-696">CC002</span></span></td>
<td><span data-ttu-id="4775d-697">Finance</span><span class="sxs-lookup"><span data-stu-id="4775d-697">Finance</span></span></td>
<td><span data-ttu-id="4775d-698">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-698">10001</span></span></td>
<td><span data-ttu-id="4775d-699">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-699">Electricity</span></span></td>
<td><span data-ttu-id="4775d-700">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-700">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="4775d-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-702">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="4775d-703">CC003</span><span class="sxs-lookup"><span data-stu-id="4775d-703">CC003</span></span></td>
<td><span data-ttu-id="4775d-704">Sestavení</span><span class="sxs-lookup"><span data-stu-id="4775d-704">Assembly</span></span></td>
<td><span data-ttu-id="4775d-705">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-705">10001</span></span></td>
<td><span data-ttu-id="4775d-706">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-706">Electricity</span></span></td>
<td><span data-ttu-id="4775d-707">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-707">Fixed cost</span></span></td>
<td><span data-ttu-id="4775d-708">713.75</span><span class="sxs-lookup"><span data-stu-id="4775d-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-709">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="4775d-710">CC003</span><span class="sxs-lookup"><span data-stu-id="4775d-710">CC003</span></span></td>
<td><span data-ttu-id="4775d-711">Sestavení</span><span class="sxs-lookup"><span data-stu-id="4775d-711">Assembly</span></span></td>
<td><span data-ttu-id="4775d-712">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-712">10001</span></span></td>
<td><span data-ttu-id="4775d-713">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-713">Electricity</span></span></td>
<td><span data-ttu-id="4775d-714">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-714">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="4775d-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-716">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="4775d-717">CC003</span><span class="sxs-lookup"><span data-stu-id="4775d-717">CC003</span></span></td>
<td><span data-ttu-id="4775d-718">Balení</span><span class="sxs-lookup"><span data-stu-id="4775d-718">Packaging</span></span></td>
<td><span data-ttu-id="4775d-719">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-719">10001</span></span></td>
<td><span data-ttu-id="4775d-720">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-720">Electricity</span></span></td>
<td><span data-ttu-id="4775d-721">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-721">Fixed cost</span></span></td>
<td><span data-ttu-id="4775d-722">286.25</span><span class="sxs-lookup"><span data-stu-id="4775d-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-723">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="4775d-724">CC003</span><span class="sxs-lookup"><span data-stu-id="4775d-724">CC003</span></span></td>
<td><span data-ttu-id="4775d-725">Balení</span><span class="sxs-lookup"><span data-stu-id="4775d-725">Packaging</span></span></td>
<td><span data-ttu-id="4775d-726">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-726">10001</span></span></td>
<td><span data-ttu-id="4775d-727">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-727">Electricity</span></span></td>
<td><span data-ttu-id="4775d-728">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-728">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="4775d-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-730">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="4775d-731">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4775d-731">Prod 1</span></span></td>
<td><span data-ttu-id="4775d-732">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4775d-732">Product 1</span></span></td>
<td><span data-ttu-id="4775d-733">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-733">10001</span></span></td>
<td><span data-ttu-id="4775d-734">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-734">Electricity</span></span></td>
<td><span data-ttu-id="4775d-735">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-735">Fixed cost</span></span></td>
<td><span data-ttu-id="4775d-736">776.36</span><span class="sxs-lookup"><span data-stu-id="4775d-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-737">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="4775d-738">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4775d-738">Prod 1</span></span></td>
<td><span data-ttu-id="4775d-739">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4775d-739">Product 1</span></span></td>
<td><span data-ttu-id="4775d-740">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-740">10001</span></span></td>
<td><span data-ttu-id="4775d-741">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-741">Electricity</span></span></td>
<td><span data-ttu-id="4775d-742">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-742">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="4775d-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-744">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="4775d-745">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4775d-745">Prod 2</span></span></td>
<td><span data-ttu-id="4775d-746">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4775d-746">Product 1</span></span></td>
<td><span data-ttu-id="4775d-747">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-747">10001</span></span></td>
<td><span data-ttu-id="4775d-748">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-748">Electricity</span></span></td>
<td><span data-ttu-id="4775d-749">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-749">Fixed cost</span></span></td>
<td><span data-ttu-id="4775d-750">223.64</span><span class="sxs-lookup"><span data-stu-id="4775d-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-751">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="4775d-752">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4775d-752">Prod 2</span></span></td>
<td><span data-ttu-id="4775d-753">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4775d-753">Product 1</span></span></td>
<td><span data-ttu-id="4775d-754">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-754">10001</span></span></td>
<td><span data-ttu-id="4775d-755">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-755">Electricity</span></span></td>
<td><span data-ttu-id="4775d-756">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-756">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="4775d-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4775d-758">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4775d-759">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4775d-760">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-760">Cost element</span></span></th>
<th><span data-ttu-id="4775d-761">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-761">Cost behavior</span></span></th>
<th><span data-ttu-id="4775d-762">Částka</span><span class="sxs-lookup"><span data-stu-id="4775d-762">Amount</span></span></th>
<th><span data-ttu-id="4775d-763">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="4775d-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4775d-764">CC001</span><span class="sxs-lookup"><span data-stu-id="4775d-764">CC001</span></span></td>
<td><span data-ttu-id="4775d-765">HR</span><span class="sxs-lookup"><span data-stu-id="4775d-765">HR</span></span></td>
<td><span data-ttu-id="4775d-766">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-766">10001</span></span></td>
<td><span data-ttu-id="4775d-767">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-767">Electricity</span></span></td>
<td><span data-ttu-id="4775d-768">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-768">Fixed cost</span></span></td>
<td><span data-ttu-id="4775d-769">-500,00</span><span class="sxs-lookup"><span data-stu-id="4775d-769">-500.00</span></span></td>
<td><span data-ttu-id="4775d-770">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-771">CC002</span><span class="sxs-lookup"><span data-stu-id="4775d-771">CC002</span></span></td>
<td><span data-ttu-id="4775d-772">Finance</span><span class="sxs-lookup"><span data-stu-id="4775d-772">Finance</span></span></td>
<td><span data-ttu-id="4775d-773">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-773">10001</span></span></td>
<td><span data-ttu-id="4775d-774">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-774">Electricity</span></span></td>
<td><span data-ttu-id="4775d-775">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-775">Fixed cost</span></span></td>
<td><span data-ttu-id="4775d-776">175.00</span><span class="sxs-lookup"><span data-stu-id="4775d-776">175.00</span></span></td>
<td><span data-ttu-id="4775d-777">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-778">CC003</span><span class="sxs-lookup"><span data-stu-id="4775d-778">CC003</span></span></td>
<td><span data-ttu-id="4775d-779">Sestavení</span><span class="sxs-lookup"><span data-stu-id="4775d-779">Assembly</span></span></td>
<td><span data-ttu-id="4775d-780">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-780">10001</span></span></td>
<td><span data-ttu-id="4775d-781">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-781">Electricity</span></span></td>
<td><span data-ttu-id="4775d-782">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-782">Fixed cost</span></span></td>
<td><span data-ttu-id="4775d-783">275.00</span><span class="sxs-lookup"><span data-stu-id="4775d-783">275.00</span></span></td>
<td><span data-ttu-id="4775d-784">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-785">CC004</span><span class="sxs-lookup"><span data-stu-id="4775d-785">CC004</span></span></td>
<td><span data-ttu-id="4775d-786">Balení</span><span class="sxs-lookup"><span data-stu-id="4775d-786">Packaging</span></span></td>
<td><span data-ttu-id="4775d-787">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-787">10001</span></span></td>
<td><span data-ttu-id="4775d-788">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-788">Electricity</span></span></td>
<td><span data-ttu-id="4775d-789">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-789">Fixed cost</span></span></td>
<td><span data-ttu-id="4775d-790">50,00</span><span class="sxs-lookup"><span data-stu-id="4775d-790">50,00</span></span></td>
<td><span data-ttu-id="4775d-791">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-792">CC001</span><span class="sxs-lookup"><span data-stu-id="4775d-792">CC001</span></span></td>
<td><span data-ttu-id="4775d-793">HR</span><span class="sxs-lookup"><span data-stu-id="4775d-793">HR</span></span></td>
<td><span data-ttu-id="4775d-794">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-794">10001</span></span></td>
<td><span data-ttu-id="4775d-795">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-795">Electricity</span></span></td>
<td><span data-ttu-id="4775d-796">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-796">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-797">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="4775d-797">-1,245.71</span></span></td>
<td><span data-ttu-id="4775d-798">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-799">CC002</span><span class="sxs-lookup"><span data-stu-id="4775d-799">CC002</span></span></td>
<td><span data-ttu-id="4775d-800">Finance</span><span class="sxs-lookup"><span data-stu-id="4775d-800">Finance</span></span></td>
<td><span data-ttu-id="4775d-801">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-801">10001</span></span></td>
<td><span data-ttu-id="4775d-802">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-802">Electricity</span></span></td>
<td><span data-ttu-id="4775d-803">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-803">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-804">436.00</span><span class="sxs-lookup"><span data-stu-id="4775d-804">436.00</span></span></td>
<td><span data-ttu-id="4775d-805">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-806">CC003</span><span class="sxs-lookup"><span data-stu-id="4775d-806">CC003</span></span></td>
<td><span data-ttu-id="4775d-807">Sestavení</span><span class="sxs-lookup"><span data-stu-id="4775d-807">Assembly</span></span></td>
<td><span data-ttu-id="4775d-808">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-808">10001</span></span></td>
<td><span data-ttu-id="4775d-809">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-809">Electricity</span></span></td>
<td><span data-ttu-id="4775d-810">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-810">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-811">685.14</span><span class="sxs-lookup"><span data-stu-id="4775d-811">685.14</span></span></td>
<td><span data-ttu-id="4775d-812">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-813">CC004</span><span class="sxs-lookup"><span data-stu-id="4775d-813">CC004</span></span></td>
<td><span data-ttu-id="4775d-814">Balení</span><span class="sxs-lookup"><span data-stu-id="4775d-814">Packaging</span></span></td>
<td><span data-ttu-id="4775d-815">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-815">10001</span></span></td>
<td><span data-ttu-id="4775d-816">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-816">Electricity</span></span></td>
<td><span data-ttu-id="4775d-817">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-817">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-818">124.57</span><span class="sxs-lookup"><span data-stu-id="4775d-818">124.57</span></span></td>
<td><span data-ttu-id="4775d-819">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-820">CC002</span><span class="sxs-lookup"><span data-stu-id="4775d-820">CC002</span></span></td>
<td><span data-ttu-id="4775d-821">Finance</span><span class="sxs-lookup"><span data-stu-id="4775d-821">Finance</span></span></td>
<td><span data-ttu-id="4775d-822">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-822">10001</span></span></td>
<td><span data-ttu-id="4775d-823">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-823">Electricity</span></span></td>
<td><span data-ttu-id="4775d-824">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-824">Fixed cost</span></span></td>
<td><span data-ttu-id="4775d-825">-675,00</span><span class="sxs-lookup"><span data-stu-id="4775d-825">-675.00</span></span></td>
<td><span data-ttu-id="4775d-826">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-827">CC003</span><span class="sxs-lookup"><span data-stu-id="4775d-827">CC003</span></span></td>
<td><span data-ttu-id="4775d-828">Sestavení</span><span class="sxs-lookup"><span data-stu-id="4775d-828">Assembly</span></span></td>
<td><span data-ttu-id="4775d-829">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-829">10001</span></span></td>
<td><span data-ttu-id="4775d-830">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-830">Electricity</span></span></td>
<td><span data-ttu-id="4775d-831">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-831">Fixed cost</span></span></td>
<td><span data-ttu-id="4775d-832">438.75</span><span class="sxs-lookup"><span data-stu-id="4775d-832">438.75</span></span></td>
<td><span data-ttu-id="4775d-833">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-834">CC004</span><span class="sxs-lookup"><span data-stu-id="4775d-834">CC004</span></span></td>
<td><span data-ttu-id="4775d-835">Balení</span><span class="sxs-lookup"><span data-stu-id="4775d-835">Packaging</span></span></td>
<td><span data-ttu-id="4775d-836">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-836">10001</span></span></td>
<td><span data-ttu-id="4775d-837">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-837">Electricity</span></span></td>
<td><span data-ttu-id="4775d-838">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-838">Fixed cost</span></span></td>
<td><span data-ttu-id="4775d-839">236.25</span><span class="sxs-lookup"><span data-stu-id="4775d-839">236.25</span></span></td>
<td><span data-ttu-id="4775d-840">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-841">CC002</span><span class="sxs-lookup"><span data-stu-id="4775d-841">CC002</span></span></td>
<td><span data-ttu-id="4775d-842">Finance</span><span class="sxs-lookup"><span data-stu-id="4775d-842">Finance</span></span></td>
<td><span data-ttu-id="4775d-843">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-843">10001</span></span></td>
<td><span data-ttu-id="4775d-844">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-844">Electricity</span></span></td>
<td><span data-ttu-id="4775d-845">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-845">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-846">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="4775d-846">-8,150.29</span></span></td>
<td><span data-ttu-id="4775d-847">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-848">CC003</span><span class="sxs-lookup"><span data-stu-id="4775d-848">CC003</span></span></td>
<td><span data-ttu-id="4775d-849">Sestavení</span><span class="sxs-lookup"><span data-stu-id="4775d-849">Assembly</span></span></td>
<td><span data-ttu-id="4775d-850">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-850">10001</span></span></td>
<td><span data-ttu-id="4775d-851">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-851">Electricity</span></span></td>
<td><span data-ttu-id="4775d-852">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-852">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="4775d-853">5,297.69</span></span></td>
<td><span data-ttu-id="4775d-854">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-855">CC004</span><span class="sxs-lookup"><span data-stu-id="4775d-855">CC004</span></span></td>
<td><span data-ttu-id="4775d-856">Balení</span><span class="sxs-lookup"><span data-stu-id="4775d-856">Packaging</span></span></td>
<td><span data-ttu-id="4775d-857">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-857">10001</span></span></td>
<td><span data-ttu-id="4775d-858">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-858">Electricity</span></span></td>
<td><span data-ttu-id="4775d-859">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-859">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="4775d-860">2,852.60</span></span></td>
<td><span data-ttu-id="4775d-861">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-862">CC003</span><span class="sxs-lookup"><span data-stu-id="4775d-862">CC003</span></span></td>
<td><span data-ttu-id="4775d-863">Sestavení</span><span class="sxs-lookup"><span data-stu-id="4775d-863">Assembly</span></span></td>
<td><span data-ttu-id="4775d-864">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-864">10001</span></span></td>
<td><span data-ttu-id="4775d-865">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-865">Electricity</span></span></td>
<td><span data-ttu-id="4775d-866">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-866">Fixed cost</span></span></td>
<td><span data-ttu-id="4775d-867">-713,75</span><span class="sxs-lookup"><span data-stu-id="4775d-867">-713.75</span></span></td>
<td><span data-ttu-id="4775d-868">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-869">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4775d-869">Prod 1</span></span></td>
<td><span data-ttu-id="4775d-870">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4775d-870">Product 1</span></span></td>
<td><span data-ttu-id="4775d-871">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-871">10001</span></span></td>
<td><span data-ttu-id="4775d-872">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-872">Electricity</span></span></td>
<td><span data-ttu-id="4775d-873">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-873">Fixed cost</span></span></td>
<td><span data-ttu-id="4775d-874">535.31</span><span class="sxs-lookup"><span data-stu-id="4775d-874">535.31</span></span></td>
<td><span data-ttu-id="4775d-875">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-876">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4775d-876">Prod 2</span></span></td>
<td><span data-ttu-id="4775d-877">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="4775d-877">Product 2</span></span></td>
<td><span data-ttu-id="4775d-878">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-878">10001</span></span></td>
<td><span data-ttu-id="4775d-879">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-879">Electricity</span></span></td>
<td><span data-ttu-id="4775d-880">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-880">Fixed cost</span></span></td>
<td><span data-ttu-id="4775d-881">178.44</span><span class="sxs-lookup"><span data-stu-id="4775d-881">178.44</span></span></td>
<td><span data-ttu-id="4775d-882">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-883">CC003</span><span class="sxs-lookup"><span data-stu-id="4775d-883">CC003</span></span></td>
<td><span data-ttu-id="4775d-884">Sestavení</span><span class="sxs-lookup"><span data-stu-id="4775d-884">Assembly</span></span></td>
<td><span data-ttu-id="4775d-885">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-885">10001</span></span></td>
<td><span data-ttu-id="4775d-886">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-886">Electricity</span></span></td>
<td><span data-ttu-id="4775d-887">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-887">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-888">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="4775d-888">-5,982.83</span></span></td>
<td><span data-ttu-id="4775d-889">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-890">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4775d-890">Prod 1</span></span></td>
<td><span data-ttu-id="4775d-891">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4775d-891">Product 1</span></span></td>
<td><span data-ttu-id="4775d-892">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-892">10001</span></span></td>
<td><span data-ttu-id="4775d-893">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-893">Electricity</span></span></td>
<td><span data-ttu-id="4775d-894">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-894">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="4775d-895">4,487.12</span></span></td>
<td><span data-ttu-id="4775d-896">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-897">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4775d-897">Prod 2</span></span></td>
<td><span data-ttu-id="4775d-898">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="4775d-898">Product 2</span></span></td>
<td><span data-ttu-id="4775d-899">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-899">10001</span></span></td>
<td><span data-ttu-id="4775d-900">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-900">Electricity</span></span></td>
<td><span data-ttu-id="4775d-901">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-901">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="4775d-902">1,495.71</span></span></td>
<td><span data-ttu-id="4775d-903">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-904">CC003</span><span class="sxs-lookup"><span data-stu-id="4775d-904">CC003</span></span></td>
<td><span data-ttu-id="4775d-905">Sestavení</span><span class="sxs-lookup"><span data-stu-id="4775d-905">Assembly</span></span></td>
<td><span data-ttu-id="4775d-906">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-906">10001</span></span></td>
<td><span data-ttu-id="4775d-907">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-907">Electricity</span></span></td>
<td><span data-ttu-id="4775d-908">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-908">Fixed cost</span></span></td>
<td><span data-ttu-id="4775d-909">-286,25</span><span class="sxs-lookup"><span data-stu-id="4775d-909">-286.25</span></span></td>
<td><span data-ttu-id="4775d-910">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-911">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4775d-911">Prod 1</span></span></td>
<td><span data-ttu-id="4775d-912">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4775d-912">Product 1</span></span></td>
<td><span data-ttu-id="4775d-913">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-913">10001</span></span></td>
<td><span data-ttu-id="4775d-914">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-914">Electricity</span></span></td>
<td><span data-ttu-id="4775d-915">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-915">Fixed cost</span></span></td>
<td><span data-ttu-id="4775d-916">241.05</span><span class="sxs-lookup"><span data-stu-id="4775d-916">241.05</span></span></td>
<td><span data-ttu-id="4775d-917">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-918">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4775d-918">Prod 2</span></span></td>
<td><span data-ttu-id="4775d-919">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="4775d-919">Product 2</span></span></td>
<td><span data-ttu-id="4775d-920">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-920">10001</span></span></td>
<td><span data-ttu-id="4775d-921">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-921">Electricity</span></span></td>
<td><span data-ttu-id="4775d-922">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-922">Fixed cost</span></span></td>
<td><span data-ttu-id="4775d-923">45.20</span><span class="sxs-lookup"><span data-stu-id="4775d-923">45.20</span></span></td>
<td><span data-ttu-id="4775d-924">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-925">CC003</span><span class="sxs-lookup"><span data-stu-id="4775d-925">CC003</span></span></td>
<td><span data-ttu-id="4775d-926">Sestavení</span><span class="sxs-lookup"><span data-stu-id="4775d-926">Assembly</span></span></td>
<td><span data-ttu-id="4775d-927">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-927">10001</span></span></td>
<td><span data-ttu-id="4775d-928">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-928">Electricity</span></span></td>
<td><span data-ttu-id="4775d-929">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-929">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-930">-2977,17</span><span class="sxs-lookup"><span data-stu-id="4775d-930">-2,977.17</span></span></td>
<td><span data-ttu-id="4775d-931">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-932">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4775d-932">Prod 1</span></span></td>
<td><span data-ttu-id="4775d-933">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="4775d-933">Product 1</span></span></td>
<td><span data-ttu-id="4775d-934">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-934">10001</span></span></td>
<td><span data-ttu-id="4775d-935">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-935">Electricity</span></span></td>
<td><span data-ttu-id="4775d-936">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-936">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="4775d-937">2,507.09</span></span></td>
<td><span data-ttu-id="4775d-938">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4775d-939">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4775d-939">Prod 2</span></span></td>
<td><span data-ttu-id="4775d-940">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="4775d-940">Product 2</span></span></td>
<td><span data-ttu-id="4775d-941">10001</span><span class="sxs-lookup"><span data-stu-id="4775d-941">10001</span></span></td>
<td><span data-ttu-id="4775d-942">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="4775d-942">Electricity</span></span></td>
<td><span data-ttu-id="4775d-943">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-943">Variable cost</span></span></td>
<td><span data-ttu-id="4775d-944">470.08</span><span class="sxs-lookup"><span data-stu-id="4775d-944">470.08</span></span></td>
<td><span data-ttu-id="4775d-945">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="4775d-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="4775d-946">Závěr</span><span class="sxs-lookup"><span data-stu-id="4775d-946">Conclusion</span></span>
<span data-ttu-id="4775d-947">Ve finančním účtování se náklady za elektřinu ve výši 10 000 zaúčtují na ID fiktivního nákladového střediska.</span><span class="sxs-lookup"><span data-stu-id="4775d-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="4775d-948">Účetní tak budou vědět, že tento náklad musí být přidělen.</span><span class="sxs-lookup"><span data-stu-id="4775d-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="4775d-949">V nákladovém účetnictví náklady procházejí napříč organizačními jednotkami a úrovněmi, na základě použitých zásad a pravidel.</span><span class="sxs-lookup"><span data-stu-id="4775d-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="4775d-950">Každý náklad byl přidružen k základu přidělení, který poskytuje nejlepší hodnocení pro přidělení nákladů.</span><span class="sxs-lookup"><span data-stu-id="4775d-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="4775d-951">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="4775d-952">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="4775d-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="4775d-953">Celkem</span><span class="sxs-lookup"><span data-stu-id="4775d-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4775d-954">CC099</span><span class="sxs-lookup"><span data-stu-id="4775d-954">CC099</span></span></th>
<th><span data-ttu-id="4775d-955">CC001</span><span class="sxs-lookup"><span data-stu-id="4775d-955">CC001</span></span></th>
<th><span data-ttu-id="4775d-956">CC002</span><span class="sxs-lookup"><span data-stu-id="4775d-956">CC002</span></span></th>
<th><span data-ttu-id="4775d-957">CC003</span><span class="sxs-lookup"><span data-stu-id="4775d-957">CC003</span></span></th>
<th><span data-ttu-id="4775d-958">CC004</span><span class="sxs-lookup"><span data-stu-id="4775d-958">CC004</span></span></th>
<th><span data-ttu-id="4775d-959">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4775d-959">Proj 1</span></span></th>
<th><span data-ttu-id="4775d-960">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4775d-960">Proj 2</span></span></th>
<th><span data-ttu-id="4775d-961">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4775d-961">Prod 1</span></span></th>
<th><span data-ttu-id="4775d-962">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4775d-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="4775d-963">10001 Elektřina</span><span class="sxs-lookup"><span data-stu-id="4775d-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4775d-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="4775d-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4775d-965"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="4775d-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4775d-966"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="4775d-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4775d-967"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="4775d-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="4775d-968"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="4775d-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4775d-969"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="4775d-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4775d-970"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="4775d-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4775d-971"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="4775d-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4775d-972"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="4775d-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="4775d-973">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="4775d-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4775d-974">0,00</span><span class="sxs-lookup"><span data-stu-id="4775d-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="4775d-975">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4775d-976">0,00</span><span class="sxs-lookup"><span data-stu-id="4775d-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4775d-977">0,00</span><span class="sxs-lookup"><span data-stu-id="4775d-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4775d-978">0,00</span><span class="sxs-lookup"><span data-stu-id="4775d-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4775d-979">0,00</span><span class="sxs-lookup"><span data-stu-id="4775d-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4775d-980">0,00</span><span class="sxs-lookup"><span data-stu-id="4775d-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="4775d-981">776.36</span><span class="sxs-lookup"><span data-stu-id="4775d-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4775d-982">223.64</span><span class="sxs-lookup"><span data-stu-id="4775d-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4775d-983"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="4775d-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="4775d-984">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="4775d-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4775d-985">000</span><span class="sxs-lookup"><span data-stu-id="4775d-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4775d-986">0,00</span><span class="sxs-lookup"><span data-stu-id="4775d-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4775d-987">0,00</span><span class="sxs-lookup"><span data-stu-id="4775d-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4775d-988">0,00</span><span class="sxs-lookup"><span data-stu-id="4775d-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4775d-989">0,00</span><span class="sxs-lookup"><span data-stu-id="4775d-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4775d-990">30.00</span><span class="sxs-lookup"><span data-stu-id="4775d-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4775d-991">10,00</span><span class="sxs-lookup"><span data-stu-id="4775d-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4775d-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="4775d-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4775d-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="4775d-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4775d-994"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="4775d-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="4775d-995">Toto téma popisuje, jak primární prvek nákladů, 10001 Elektřina, prochází přes objekty nákladů.</span><span class="sxs-lookup"><span data-stu-id="4775d-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="4775d-996">Tyto režijní náklady tedy budou přiděleny na nejnižší úroveň v organizaci.</span><span class="sxs-lookup"><span data-stu-id="4775d-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="4775d-997">Jinak řečeno, objekty nákladů na nejnižší úrovni ponesou náklady.</span><span class="sxs-lookup"><span data-stu-id="4775d-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="4775d-998">Chcete-li vizuální tok nákladů mezi objekty nákladů, můžete použít pravidla zásad shrnutí nákladů pro vizualizaci jejich toků.</span><span class="sxs-lookup"><span data-stu-id="4775d-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="4775d-999">Podrobnější informace naleznete v tématu Zásady shrnutí nákladů.</span><span class="sxs-lookup"><span data-stu-id="4775d-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="4775d-1000">(Všimněte si, že toto téma ještě není dokončené, ale bud k dispozici již brzy.)</span><span class="sxs-lookup"><span data-stu-id="4775d-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




