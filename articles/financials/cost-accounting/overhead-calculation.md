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
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 0ea6f7428cd5c7618d2d69f1fb66fd9539ad1073
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="overhead-calculation"></a><span data-ttu-id="72735-103">Výpočet režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="72735-104">Toto téma popisuje typické procesy pro výpočet a přidělení režijních nákladů.</span><span class="sxs-lookup"><span data-stu-id="72735-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="72735-105">Definice termínu</span><span class="sxs-lookup"><span data-stu-id="72735-105">Term definition</span></span>
---------------

<span data-ttu-id="72735-106">Režijní náklady jsou náklady, které nutně vznikají při chodu podnikání, ale nelze je připsat přímo k žádné konkrétní podnikatelské aktivitě, produktu nebo službě.</span><span class="sxs-lookup"><span data-stu-id="72735-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="72735-107">Režijní náklady poskytují důležitou podporu pro generování aktivity přinášejících zisk.</span><span class="sxs-lookup"><span data-stu-id="72735-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="72735-108">Následuje několik příkladů režijních nákladů:</span><span class="sxs-lookup"><span data-stu-id="72735-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="72735-109">Renta</span><span class="sxs-lookup"><span data-stu-id="72735-109">Rent</span></span>
-   <span data-ttu-id="72735-110">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-110">Electricity</span></span>
-   <span data-ttu-id="72735-111">Administrativní mzdy</span><span class="sxs-lookup"><span data-stu-id="72735-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="72735-112">Přehled výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-112">Overhead calculation overview</span></span>
<span data-ttu-id="72735-113">Výpočet režijních nákladů spustí zásady účtování nákladů ve správném pořadí.</span><span class="sxs-lookup"><span data-stu-id="72735-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="72735-114">Výpočet režijních nákladů můžete pro stejné fiskální období spustit mnohokrát, pokud došlo ke změně zásad účtování nákladů nebo zjištění konkrétních chyb.</span><span class="sxs-lookup"><span data-stu-id="72735-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="72735-115">Každé spuštění výpočtu režijních nákladů se ukládá a přijímá ID jedinečné verze, které vám umožní porovnávat výpočty v různých verzích.</span><span class="sxs-lookup"><span data-stu-id="72735-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="72735-116">Položky nákladů, které generuje výpočet režijních nákladů, přijímá datum účtování.</span><span class="sxs-lookup"><span data-stu-id="72735-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="72735-117">Toto datum účtován se shoduje s konvovým datem fiskálního období, které se použije ve výpočtu.</span><span class="sxs-lookup"><span data-stu-id="72735-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="72735-118">ID jedinečné verze se skládá z následujících prvků:</span><span class="sxs-lookup"><span data-stu-id="72735-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="72735-119">Typ verze</span><span class="sxs-lookup"><span data-stu-id="72735-119">Version type</span></span>
-   <span data-ttu-id="72735-120">Datum a čas</span><span class="sxs-lookup"><span data-stu-id="72735-120">Date and time</span></span>
-   <span data-ttu-id="72735-121">Hlavní kniha nákladového účetnictví</span><span class="sxs-lookup"><span data-stu-id="72735-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="72735-122">Fiskální rok</span><span class="sxs-lookup"><span data-stu-id="72735-122">Fiscal year</span></span>
-   <span data-ttu-id="72735-123">Fiskální období</span><span class="sxs-lookup"><span data-stu-id="72735-123">Fiscal period</span></span>

<span data-ttu-id="72735-124">Výpočet režijních nákladů se spustí bez ohledu na verzi.</span><span class="sxs-lookup"><span data-stu-id="72735-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="72735-125">Proto lze vypočítat rozpočtovou verzi před skutečnou verzí.</span><span class="sxs-lookup"><span data-stu-id="72735-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="72735-126">Výpočet režijních nákladů se skládá ze čtyř kroků uvedených na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="72735-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="72735-127">V každé fázi je vytvořeno záhlaví deníku, které obsahuje položky deníku.</span><span class="sxs-lookup"><span data-stu-id="72735-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="72735-128">Toto záhlaví deníku zachovává vstupní data pro každý krok výpočtu.</span><span class="sxs-lookup"><span data-stu-id="72735-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="72735-129">Zásady a pravidla se použijí na každý řádek deníku a položky nákladů jsou generovány jako výstup.</span><span class="sxs-lookup"><span data-stu-id="72735-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="72735-130">Máte tedy vždy plnou sledovatelnost.</span><span class="sxs-lookup"><span data-stu-id="72735-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="72735-131">[![Výpočet režijních nákladů](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="72735-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="72735-132">Výpočet a přidělení režijních nákladů za elektřinu</span><span class="sxs-lookup"><span data-stu-id="72735-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="72735-133">Ve finančním účetnictví se některé náklady, jako je například elektřina, registrují jako paušální.</span><span class="sxs-lookup"><span data-stu-id="72735-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="72735-134">Podrobný přehled pro vedoucí není tedy pro nákladové účetnictví k dispozici.</span><span class="sxs-lookup"><span data-stu-id="72735-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="72735-135">V nákladovém účetnictví musí náklady procházet organizačními jednotkami, aby byl získán správný přehled pro vedoucí napříč všemi jednotkami a úrovněmi organizace.</span><span class="sxs-lookup"><span data-stu-id="72735-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="72735-136">Tento tok musí být založen buď na přesném záznamu spotřeby nebo na objektivním hodnocení.</span><span class="sxs-lookup"><span data-stu-id="72735-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="72735-137">V hlavní knize mohou být zaúčtovány náklady na elektřinu způsobem znázorněným v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="72735-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="72735-138">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="72735-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="72735-139">Nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="72735-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="72735-140">Hlavní účet</span><span class="sxs-lookup"><span data-stu-id="72735-140">Main account</span></span></th>
<th><span data-ttu-id="72735-141">Částka v zúčtovací měně</span><span class="sxs-lookup"><span data-stu-id="72735-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="72735-142">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="72735-143">CC099</span><span class="sxs-lookup"><span data-stu-id="72735-143">CC099</span></span></td>
<td><span data-ttu-id="72735-144">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="72735-144">Default cost center</span></span></td>
<td><span data-ttu-id="72735-145">10001</span><span class="sxs-lookup"><span data-stu-id="72735-145">10001</span></span></td>
<td><span data-ttu-id="72735-146">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-146">Electricity</span></span></td>
<td><span data-ttu-id="72735-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="72735-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="72735-148">Krok 1: Zpracování výpočtu chování nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="72735-149">Ve výchozím nastavení dostanou při importu položek nákladů z datového zdroje tyto položky v nákladovém účetnictví klasifikaci **Neklasifikované**.</span><span class="sxs-lookup"><span data-stu-id="72735-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="72735-150">Použitím pravidla zásad chování nákladů lze reklasifikovat položky nákladů jako **Pevné náklady** nebo **Variabilní náklady**.</span><span class="sxs-lookup"><span data-stu-id="72735-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="72735-151">Definice pravidel chování nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-151">Define the cost behavior rule</span></span>

<span data-ttu-id="72735-152">V některých případech je část nákladů s pevným poplatkem a zbývající náklady jsou založeny na spotřebě.</span><span class="sxs-lookup"><span data-stu-id="72735-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="72735-153">Účty za elektřinu často odpovídají této definici.</span><span class="sxs-lookup"><span data-stu-id="72735-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="72735-154">Po platbě konkrétního pevného poplatku platíte spotřebu za kilowatthodinu (kWh).</span><span class="sxs-lookup"><span data-stu-id="72735-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="72735-155">Pokud je například poplatek pevných nákladů 1 000,00, definuje se pravidlo chování nákladů takto:</span><span class="sxs-lookup"><span data-stu-id="72735-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="72735-156">Pevná částka 1 000,00</span><span class="sxs-lookup"><span data-stu-id="72735-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="72735-157">0 &lt;= 1 000,00 = Pevná</span><span class="sxs-lookup"><span data-stu-id="72735-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="72735-158">1 000,01 &lt; N = Variabilní</span><span class="sxs-lookup"><span data-stu-id="72735-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="72735-159">Deník</span><span class="sxs-lookup"><span data-stu-id="72735-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="72735-160">Deník</span><span class="sxs-lookup"><span data-stu-id="72735-160">Journal</span></span></th>
<th><span data-ttu-id="72735-161">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="72735-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="72735-162">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="72735-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="72735-163">Verze</span><span class="sxs-lookup"><span data-stu-id="72735-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="72735-164">00001</span><span class="sxs-lookup"><span data-stu-id="72735-164">00001</span></span></td>
<td><span data-ttu-id="72735-165">Deník výpočtu chování nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="72735-166">Fiskální</span><span class="sxs-lookup"><span data-stu-id="72735-166">Fiscal</span></span></td>
<td><span data-ttu-id="72735-167">2017</span><span class="sxs-lookup"><span data-stu-id="72735-167">2017</span></span></td>
<td><span data-ttu-id="72735-168">Období 1</span><span class="sxs-lookup"><span data-stu-id="72735-168">Period 1</span></span></td>
<td><span data-ttu-id="72735-169">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="72735-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="72735-170">Položky deníku (Položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="72735-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="72735-171">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="72735-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="72735-172">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="72735-173">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-173">Cost element</span></span></th>
<th><span data-ttu-id="72735-174">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-174">Cost behavior</span></span></th>
<th><span data-ttu-id="72735-175">Částka</span><span class="sxs-lookup"><span data-stu-id="72735-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="72735-176">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="72735-177">CC099</span><span class="sxs-lookup"><span data-stu-id="72735-177">CC099</span></span></td>
<td><span data-ttu-id="72735-178">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="72735-178">Default cost center</span></span></td>
<td><span data-ttu-id="72735-179">10001</span><span class="sxs-lookup"><span data-stu-id="72735-179">10001</span></span></td>
<td><span data-ttu-id="72735-180">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-180">Electricity</span></span></td>
<td><span data-ttu-id="72735-181">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="72735-181">Unclassified</span></span></td>
<td><span data-ttu-id="72735-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="72735-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="72735-183">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="72735-184">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="72735-185">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-185">Cost element</span></span></th>
<th><span data-ttu-id="72735-186">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-186">Cost behavior</span></span></th>
<th><span data-ttu-id="72735-187">Částka</span><span class="sxs-lookup"><span data-stu-id="72735-187">Amount</span></span></th>
<th><span data-ttu-id="72735-188">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="72735-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="72735-189">CC099</span><span class="sxs-lookup"><span data-stu-id="72735-189">CC099</span></span></td>
<td><span data-ttu-id="72735-190">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="72735-190">Default cost center</span></span></td>
<td><span data-ttu-id="72735-191">10001</span><span class="sxs-lookup"><span data-stu-id="72735-191">10001</span></span></td>
<td><span data-ttu-id="72735-192">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-192">Electricity</span></span></td>
<td><span data-ttu-id="72735-193">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="72735-193">Unclassified</span></span></td>
<td><span data-ttu-id="72735-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="72735-194">10,000.00</span></span></td>
<td><span data-ttu-id="72735-195">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-196">CC099</span><span class="sxs-lookup"><span data-stu-id="72735-196">CC099</span></span></td>
<td><span data-ttu-id="72735-197">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="72735-197">Default cost center</span></span></td>
<td><span data-ttu-id="72735-198">10001</span><span class="sxs-lookup"><span data-stu-id="72735-198">10001</span></span></td>
<td><span data-ttu-id="72735-199">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-199">Electricity</span></span></td>
<td><span data-ttu-id="72735-200">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="72735-200">Unclassified</span></span></td>
<td><span data-ttu-id="72735-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="72735-201">-10,000.00</span></span></td>
<td><span data-ttu-id="72735-202">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-203">CC099</span><span class="sxs-lookup"><span data-stu-id="72735-203">CC099</span></span></td>
<td><span data-ttu-id="72735-204">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="72735-204">Default cost center</span></span></td>
<td><span data-ttu-id="72735-205">10001</span><span class="sxs-lookup"><span data-stu-id="72735-205">10001</span></span></td>
<td><span data-ttu-id="72735-206">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-206">Electricity</span></span></td>
<td><span data-ttu-id="72735-207">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-207">Fixed cost</span></span></td>
<td><span data-ttu-id="72735-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="72735-208">1,000.00</span></span></td>
<td><span data-ttu-id="72735-209">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-210">CC099</span><span class="sxs-lookup"><span data-stu-id="72735-210">CC099</span></span></td>
<td><span data-ttu-id="72735-211">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="72735-211">Default cost center</span></span></td>
<td><span data-ttu-id="72735-212">10001</span><span class="sxs-lookup"><span data-stu-id="72735-212">10001</span></span></td>
<td><span data-ttu-id="72735-213">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-213">Electricity</span></span></td>
<td><span data-ttu-id="72735-214">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-214">Variable cost</span></span></td>
<td><span data-ttu-id="72735-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="72735-215">9,000.00</span></span></td>
<td><span data-ttu-id="72735-216">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="72735-217">Ohledně podrobných informací o chování nákladů nahlédněte do zásad chování nákladů.</span><span class="sxs-lookup"><span data-stu-id="72735-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="72735-218">(Všimněte si, že toto téma ještě není dokončené, ale bud k dispozici již brzy.)</span><span class="sxs-lookup"><span data-stu-id="72735-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="72735-219">Krok 2: Zpracování výpočtu distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="72735-220">Distribuce nákladů se používá k rozdělení nákladů z jednoho objektu nákladů na jeden nebo více dalších objektů nákladů použitím příslušného základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="72735-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="72735-221">Distribuce nákladů a přidělení nákladů se liší v tom, že k distribuci nákladů dochází vždy na úrovni primárního prvku nákladů původních nákladů.</span><span class="sxs-lookup"><span data-stu-id="72735-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="72735-222">Definice pravidel distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-222">Define the cost distribution rule</span></span>

<span data-ttu-id="72735-223">Ve finančním účetnictví se náklady na elektřinu často registrují jako paušální.</span><span class="sxs-lookup"><span data-stu-id="72735-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="72735-224">V nákladovém účetnictví není tento přístup dostatečně podrobný.</span><span class="sxs-lookup"><span data-stu-id="72735-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="72735-225">Variabilní náklady by měly být distribuovány k jednotlivým objektům nákladů na solidním základě.</span><span class="sxs-lookup"><span data-stu-id="72735-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="72735-226">Nejlogičtější základ přidělení je spotřeba elektřiny (kWh).</span><span class="sxs-lookup"><span data-stu-id="72735-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="72735-227">Vytvoří se člen statistické dimenzi s názvem Elektřina a zaznamená se elektrické spotřeba.</span><span class="sxs-lookup"><span data-stu-id="72735-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="72735-228">Ve výchozím nastavení se všechny členy statistické dimenze stanou dostupnými zpřístupněny jako základy přidělení.</span><span class="sxs-lookup"><span data-stu-id="72735-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="72735-229">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-229">Cost object</span></span></th>
<th><span data-ttu-id="72735-230">kWh</span><span class="sxs-lookup"><span data-stu-id="72735-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="72735-231">CC001</span><span class="sxs-lookup"><span data-stu-id="72735-231">CC001</span></span></td>
<td><span data-ttu-id="72735-232">HR</span><span class="sxs-lookup"><span data-stu-id="72735-232">HR</span></span></td>
<td><span data-ttu-id="72735-233">1 000</span><span class="sxs-lookup"><span data-stu-id="72735-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-234">CC002</span><span class="sxs-lookup"><span data-stu-id="72735-234">CC002</span></span></td>
<td><span data-ttu-id="72735-235">Finance</span><span class="sxs-lookup"><span data-stu-id="72735-235">Finance</span></span></td>
<td><span data-ttu-id="72735-236">6,000</span><span class="sxs-lookup"><span data-stu-id="72735-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-237">CC003</span><span class="sxs-lookup"><span data-stu-id="72735-237">CC003</span></span></td>
<td><span data-ttu-id="72735-238">Sestavení</span><span class="sxs-lookup"><span data-stu-id="72735-238">Assembly</span></span></td>
<td><span data-ttu-id="72735-239">0</span><span class="sxs-lookup"><span data-stu-id="72735-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="72735-240">Následující tabulka zobrazuje výsledek při použití elektrické spotřeby jako základu přidělení pro variabilní náklady.</span><span class="sxs-lookup"><span data-stu-id="72735-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="72735-241">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-241">Cost object</span></span></th>
<th><span data-ttu-id="72735-242">Hodnota</span><span class="sxs-lookup"><span data-stu-id="72735-242">Magnitude</span></span></th>
<th><span data-ttu-id="72735-243">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="72735-243">Allocation factor</span></span></th>
<th><span data-ttu-id="72735-244">Částka</span><span class="sxs-lookup"><span data-stu-id="72735-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="72735-245">CC001</span><span class="sxs-lookup"><span data-stu-id="72735-245">CC001</span></span></td>
<td><span data-ttu-id="72735-246">HR</span><span class="sxs-lookup"><span data-stu-id="72735-246">HR</span></span></td>
<td><span data-ttu-id="72735-247">1 000</span><span class="sxs-lookup"><span data-stu-id="72735-247">1,000</span></span></td>
<td><span data-ttu-id="72735-248">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="72735-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="72735-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="72735-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-250">CC002</span><span class="sxs-lookup"><span data-stu-id="72735-250">CC002</span></span></td>
<td><span data-ttu-id="72735-251">Finance</span><span class="sxs-lookup"><span data-stu-id="72735-251">Finance</span></span></td>
<td><span data-ttu-id="72735-252">6,000</span><span class="sxs-lookup"><span data-stu-id="72735-252">6,000</span></span></td>
<td><span data-ttu-id="72735-253">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="72735-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="72735-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="72735-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-255">CC003</span><span class="sxs-lookup"><span data-stu-id="72735-255">CC003</span></span></td>
<td><span data-ttu-id="72735-256">Sestavení</span><span class="sxs-lookup"><span data-stu-id="72735-256">Assembly</span></span></td>
<td><span data-ttu-id="72735-257">0</span><span class="sxs-lookup"><span data-stu-id="72735-257">0</span></span></td>
<td><span data-ttu-id="72735-258">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="72735-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="72735-259">0,00</span><span class="sxs-lookup"><span data-stu-id="72735-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="72735-260">Pevné náklady musí být distribuovány rovnoměrně k jednotlivých objektům nákladů, které spotřebovávaly elektřinu.</span><span class="sxs-lookup"><span data-stu-id="72735-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="72735-261">Tohoto výsledku můžete dosáhnout pomocí členu statistické dimenze Elektřina v základu přidělení vzorce: (Elektřina &gt; 0,00) Následující tabulka zobrazuje výsledek při použití elektrické spotřeby jako základu přidělení pro variabilní náklady.</span><span class="sxs-lookup"><span data-stu-id="72735-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="72735-262">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-262">Cost object</span></span></th>
<th><span data-ttu-id="72735-263">Vzorec</span><span class="sxs-lookup"><span data-stu-id="72735-263">Formula</span></span></th>
<th><span data-ttu-id="72735-264">Hodnota</span><span class="sxs-lookup"><span data-stu-id="72735-264">Magnitude</span></span></th>
<th><span data-ttu-id="72735-265">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="72735-265">Allocation factor</span></span></th>
<th><span data-ttu-id="72735-266">Částka</span><span class="sxs-lookup"><span data-stu-id="72735-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="72735-267">CC001</span><span class="sxs-lookup"><span data-stu-id="72735-267">CC001</span></span></td>
<td><span data-ttu-id="72735-268">HR</span><span class="sxs-lookup"><span data-stu-id="72735-268">HR</span></span></td>
<td><span data-ttu-id="72735-269">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="72735-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="72735-270">1</span><span class="sxs-lookup"><span data-stu-id="72735-270">1</span></span></td>
<td><span data-ttu-id="72735-271">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="72735-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="72735-272">500.00</span><span class="sxs-lookup"><span data-stu-id="72735-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-273">CC002</span><span class="sxs-lookup"><span data-stu-id="72735-273">CC002</span></span></td>
<td><span data-ttu-id="72735-274">Finance</span><span class="sxs-lookup"><span data-stu-id="72735-274">Finance</span></span></td>
<td><span data-ttu-id="72735-275">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="72735-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="72735-276">1</span><span class="sxs-lookup"><span data-stu-id="72735-276">1</span></span></td>
<td><span data-ttu-id="72735-277">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="72735-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="72735-278">500.00</span><span class="sxs-lookup"><span data-stu-id="72735-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-279">CC003</span><span class="sxs-lookup"><span data-stu-id="72735-279">CC003</span></span></td>
<td><span data-ttu-id="72735-280">Sestavení</span><span class="sxs-lookup"><span data-stu-id="72735-280">Assembly</span></span></td>
<td><span data-ttu-id="72735-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="72735-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="72735-282">0</span><span class="sxs-lookup"><span data-stu-id="72735-282">0</span></span></td>
<td><span data-ttu-id="72735-283">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="72735-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="72735-284">0,00</span><span class="sxs-lookup"><span data-stu-id="72735-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="72735-285">Deník</span><span class="sxs-lookup"><span data-stu-id="72735-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="72735-286">Deník</span><span class="sxs-lookup"><span data-stu-id="72735-286">Journal</span></span></th>
<th><span data-ttu-id="72735-287">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="72735-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="72735-288">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="72735-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="72735-289">Verze</span><span class="sxs-lookup"><span data-stu-id="72735-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="72735-290">00002</span><span class="sxs-lookup"><span data-stu-id="72735-290">00002</span></span></td>
<td><span data-ttu-id="72735-291">Deník výpočtu distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="72735-292">Fiskální</span><span class="sxs-lookup"><span data-stu-id="72735-292">Fiscal</span></span></td>
<td><span data-ttu-id="72735-293">2017</span><span class="sxs-lookup"><span data-stu-id="72735-293">2017</span></span></td>
<td><span data-ttu-id="72735-294">Období 1</span><span class="sxs-lookup"><span data-stu-id="72735-294">Period 1</span></span></td>
<td><span data-ttu-id="72735-295">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="72735-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="72735-296">Položky deníku (Položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="72735-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="72735-297">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="72735-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="72735-298">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="72735-299">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-299">Cost element</span></span></th>
<th><span data-ttu-id="72735-300">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-300">Cost behavior</span></span></th>
<th><span data-ttu-id="72735-301">Částka</span><span class="sxs-lookup"><span data-stu-id="72735-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="72735-302">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="72735-303">CC099</span><span class="sxs-lookup"><span data-stu-id="72735-303">CC099</span></span></td>
<td><span data-ttu-id="72735-304">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="72735-304">Default cost center</span></span></td>
<td><span data-ttu-id="72735-305">10001</span><span class="sxs-lookup"><span data-stu-id="72735-305">10001</span></span></td>
<td><span data-ttu-id="72735-306">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-306">Electricity</span></span></td>
<td><span data-ttu-id="72735-307">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-307">Fixed cost</span></span></td>
<td><span data-ttu-id="72735-308">1 000,00</span><span class="sxs-lookup"><span data-stu-id="72735-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-309">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="72735-310">CC099</span><span class="sxs-lookup"><span data-stu-id="72735-310">CC099</span></span></td>
<td><span data-ttu-id="72735-311">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="72735-311">Default cost center</span></span></td>
<td><span data-ttu-id="72735-312">10001</span><span class="sxs-lookup"><span data-stu-id="72735-312">10001</span></span></td>
<td><span data-ttu-id="72735-313">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-313">Electricity</span></span></td>
<td><span data-ttu-id="72735-314">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-314">Variable cost</span></span></td>
<td><span data-ttu-id="72735-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="72735-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="72735-316">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="72735-317">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="72735-318">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-318">Cost element</span></span></th>
<th><span data-ttu-id="72735-319">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-319">Cost behavior</span></span></th>
<th><span data-ttu-id="72735-320">Částka</span><span class="sxs-lookup"><span data-stu-id="72735-320">Amount</span></span></th>
<th><span data-ttu-id="72735-321">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="72735-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="72735-322">CC099</span><span class="sxs-lookup"><span data-stu-id="72735-322">CC099</span></span></td>
<td><span data-ttu-id="72735-323">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="72735-323">Default cost center</span></span></td>
<td><span data-ttu-id="72735-324">10001</span><span class="sxs-lookup"><span data-stu-id="72735-324">10001</span></span></td>
<td><span data-ttu-id="72735-325">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-325">Electricity</span></span></td>
<td><span data-ttu-id="72735-326">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-326">Fixed cost</span></span></td>
<td><span data-ttu-id="72735-327">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="72735-327">-1,000.00</span></span></td>
<td><span data-ttu-id="72735-328">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-329">CC001</span><span class="sxs-lookup"><span data-stu-id="72735-329">CC001</span></span></td>
<td><span data-ttu-id="72735-330">HR</span><span class="sxs-lookup"><span data-stu-id="72735-330">HR</span></span></td>
<td><span data-ttu-id="72735-331">10001</span><span class="sxs-lookup"><span data-stu-id="72735-331">10001</span></span></td>
<td><span data-ttu-id="72735-332">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-332">Electricity</span></span></td>
<td><span data-ttu-id="72735-333">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-333">Fixed cost</span></span></td>
<td><span data-ttu-id="72735-334">500.00</span><span class="sxs-lookup"><span data-stu-id="72735-334">500.00</span></span></td>
<td><span data-ttu-id="72735-335">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-336">CC002</span><span class="sxs-lookup"><span data-stu-id="72735-336">CC002</span></span></td>
<td><span data-ttu-id="72735-337">Finance</span><span class="sxs-lookup"><span data-stu-id="72735-337">Finance</span></span></td>
<td><span data-ttu-id="72735-338">10001</span><span class="sxs-lookup"><span data-stu-id="72735-338">10001</span></span></td>
<td><span data-ttu-id="72735-339">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-339">Electricity</span></span></td>
<td><span data-ttu-id="72735-340">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-340">Fixed cost</span></span></td>
<td><span data-ttu-id="72735-341">500.00</span><span class="sxs-lookup"><span data-stu-id="72735-341">500.00</span></span></td>
<td><span data-ttu-id="72735-342">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-343">CC099</span><span class="sxs-lookup"><span data-stu-id="72735-343">CC099</span></span></td>
<td><span data-ttu-id="72735-344">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="72735-344">Default cost center</span></span></td>
<td><span data-ttu-id="72735-345">10001</span><span class="sxs-lookup"><span data-stu-id="72735-345">10001</span></span></td>
<td><span data-ttu-id="72735-346">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-346">Electricity</span></span></td>
<td><span data-ttu-id="72735-347">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-347">Variable cost</span></span></td>
<td><span data-ttu-id="72735-348">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="72735-348">-9,000.00</span></span></td>
<td><span data-ttu-id="72735-349">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-350">CC001</span><span class="sxs-lookup"><span data-stu-id="72735-350">CC001</span></span></td>
<td><span data-ttu-id="72735-351">HR</span><span class="sxs-lookup"><span data-stu-id="72735-351">HR</span></span></td>
<td><span data-ttu-id="72735-352">10001</span><span class="sxs-lookup"><span data-stu-id="72735-352">10001</span></span></td>
<td><span data-ttu-id="72735-353">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-353">Electricity</span></span></td>
<td><span data-ttu-id="72735-354">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-354">Variable cost</span></span></td>
<td><span data-ttu-id="72735-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="72735-355">1,285.71</span></span></td>
<td><span data-ttu-id="72735-356">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-357">CC002</span><span class="sxs-lookup"><span data-stu-id="72735-357">CC002</span></span></td>
<td><span data-ttu-id="72735-358">Finance</span><span class="sxs-lookup"><span data-stu-id="72735-358">Finance</span></span></td>
<td><span data-ttu-id="72735-359">10001</span><span class="sxs-lookup"><span data-stu-id="72735-359">10001</span></span></td>
<td><span data-ttu-id="72735-360">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-360">Electricity</span></span></td>
<td><span data-ttu-id="72735-361">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-361">Variable cost</span></span></td>
<td><span data-ttu-id="72735-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="72735-362">7,714.29</span></span></td>
<td><span data-ttu-id="72735-363">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="72735-364">Podrobné informace o základech distribuce a přidělení nákladů získáte v tématech Zásady distribuce nákladů a Základy přidělení.</span><span class="sxs-lookup"><span data-stu-id="72735-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="72735-365">(Všimněte si, že toto téma ještě není dokončené, ale bud k dispozici již brzy.)</span><span class="sxs-lookup"><span data-stu-id="72735-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="72735-366">Krok 3: Zpracování výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="72735-367">Režijní náklady se používají k účtování jednoho nebo více konkrétních objektů nákladů.</span><span class="sxs-lookup"><span data-stu-id="72735-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="72735-368">Účtování je založeno na předem určené nákladové sazbě a množství z přiřazeného základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="72735-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="72735-369">Definice sazby režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-369">Define the overhead rate</span></span>

<span data-ttu-id="72735-370">Objekt nákladů CC001 HR přispívá k sadě interních projektů.</span><span class="sxs-lookup"><span data-stu-id="72735-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="72735-371">Vytvoří se člen statistické dimenzi s názvem projekty lidských zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="72735-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="72735-372">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-372">Cost object</span></span></th>
<th><span data-ttu-id="72735-373">Pracovní doba</span><span class="sxs-lookup"><span data-stu-id="72735-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="72735-374">Proj 1</span><span class="sxs-lookup"><span data-stu-id="72735-374">Proj 1</span></span></td>
<td><span data-ttu-id="72735-375">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="72735-375">Project 1</span></span></td>
<td><span data-ttu-id="72735-376">3</span><span class="sxs-lookup"><span data-stu-id="72735-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-377">Proj 2</span><span class="sxs-lookup"><span data-stu-id="72735-377">Proj 2</span></span></td>
<td><span data-ttu-id="72735-378">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="72735-378">Project 2</span></span></td>
<td><span data-ttu-id="72735-379">1</span><span class="sxs-lookup"><span data-stu-id="72735-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="72735-380">Byla definována předem určená nákladová sazba pro příspěvky k nákladovým projektům.</span><span class="sxs-lookup"><span data-stu-id="72735-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="72735-381">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-381">Cost object</span></span></th>
<th><span data-ttu-id="72735-382">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-382">Cost element</span></span></th>
<th><span data-ttu-id="72735-383">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-383">Cost behavior</span></span></th>
<th><span data-ttu-id="72735-384">Jednotky</span><span class="sxs-lookup"><span data-stu-id="72735-384">Units</span></span></th>
<th><span data-ttu-id="72735-385">Kurz</span><span class="sxs-lookup"><span data-stu-id="72735-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="72735-386">CC001</span><span class="sxs-lookup"><span data-stu-id="72735-386">CC001</span></span></td>
<td><span data-ttu-id="72735-387">HR</span><span class="sxs-lookup"><span data-stu-id="72735-387">HR</span></span></td>
<td><span data-ttu-id="72735-388">10001</span><span class="sxs-lookup"><span data-stu-id="72735-388">10001</span></span></td>
<td><span data-ttu-id="72735-389">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-389">Variable cost</span></span></td>
<td><span data-ttu-id="72735-390">1</span><span class="sxs-lookup"><span data-stu-id="72735-390">1</span></span></td>
<td><span data-ttu-id="72735-391">10</span><span class="sxs-lookup"><span data-stu-id="72735-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="72735-392">Následující tabulka zobrazuje výsledek při použití projektů lidských zdrojů jako základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="72735-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="72735-393">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-393">Cost object</span></span></th>
<th><span data-ttu-id="72735-394">Hodnota</span><span class="sxs-lookup"><span data-stu-id="72735-394">Magnitude</span></span></th>
<th><span data-ttu-id="72735-395">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-395">Cost element</span></span></th>
<th><span data-ttu-id="72735-396">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="72735-396">Allocation factor</span></span></th>
<th><span data-ttu-id="72735-397">Částka</span><span class="sxs-lookup"><span data-stu-id="72735-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="72735-398">Proj 1</span><span class="sxs-lookup"><span data-stu-id="72735-398">Proj 1</span></span></td>
<td><span data-ttu-id="72735-399">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="72735-399">Project 1</span></span></td>
<td><span data-ttu-id="72735-400">3</span><span class="sxs-lookup"><span data-stu-id="72735-400">3</span></span></td>
<td><span data-ttu-id="72735-401">10001</span><span class="sxs-lookup"><span data-stu-id="72735-401">10001</span></span></td>
<td><span data-ttu-id="72735-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="72735-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="72735-403">30.00</span><span class="sxs-lookup"><span data-stu-id="72735-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-404">Proj 2</span><span class="sxs-lookup"><span data-stu-id="72735-404">Proj 2</span></span></td>
<td><span data-ttu-id="72735-405">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="72735-405">Project 2</span></span></td>
<td><span data-ttu-id="72735-406">1</span><span class="sxs-lookup"><span data-stu-id="72735-406">1</span></span></td>
<td><span data-ttu-id="72735-407">10001</span><span class="sxs-lookup"><span data-stu-id="72735-407">10001</span></span></td>
<td><span data-ttu-id="72735-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="72735-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="72735-409">10,00</span><span class="sxs-lookup"><span data-stu-id="72735-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="72735-410">Deník</span><span class="sxs-lookup"><span data-stu-id="72735-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="72735-411">Deník</span><span class="sxs-lookup"><span data-stu-id="72735-411">Journal</span></span></th>
<th><span data-ttu-id="72735-412">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="72735-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="72735-413">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="72735-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="72735-414">Verze</span><span class="sxs-lookup"><span data-stu-id="72735-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="72735-415">00003</span><span class="sxs-lookup"><span data-stu-id="72735-415">00003</span></span></td>
<td><span data-ttu-id="72735-416">Deník výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="72735-417">Fiskální</span><span class="sxs-lookup"><span data-stu-id="72735-417">Fiscal</span></span></td>
<td><span data-ttu-id="72735-418">2017</span><span class="sxs-lookup"><span data-stu-id="72735-418">2017</span></span></td>
<td><span data-ttu-id="72735-419">Období 1</span><span class="sxs-lookup"><span data-stu-id="72735-419">Period 1</span></span></td>
<td><span data-ttu-id="72735-420">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="72735-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="72735-421">Položky deníku (položky deníku pro výpočet sazby režijních nákladů)</span><span class="sxs-lookup"><span data-stu-id="72735-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="72735-422">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="72735-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="72735-423">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-423">Cost object</span></span></th>
<th><span data-ttu-id="72735-424">Hodnota</span><span class="sxs-lookup"><span data-stu-id="72735-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="72735-425">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="72735-426">Proj 1</span><span class="sxs-lookup"><span data-stu-id="72735-426">Proj 1</span></span></td>
<td><span data-ttu-id="72735-427">Interní projekt 1</span><span class="sxs-lookup"><span data-stu-id="72735-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="72735-428">3,00</span><span class="sxs-lookup"><span data-stu-id="72735-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-429">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="72735-430">Proj 2</span><span class="sxs-lookup"><span data-stu-id="72735-430">Proj 2</span></span></td>
<td><span data-ttu-id="72735-431">Interní projekt 2</span><span class="sxs-lookup"><span data-stu-id="72735-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="72735-432">1.00</span><span class="sxs-lookup"><span data-stu-id="72735-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="72735-433">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="72735-434">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="72735-435">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-435">Cost element</span></span></th>
<th><span data-ttu-id="72735-436">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-436">Cost behavior</span></span></th>
<th><span data-ttu-id="72735-437">Částka</span><span class="sxs-lookup"><span data-stu-id="72735-437">Amount</span></span></th>
<th><span data-ttu-id="72735-438">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="72735-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="72735-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="72735-439">CC0001</span></span></td>
<td><span data-ttu-id="72735-440">HR</span><span class="sxs-lookup"><span data-stu-id="72735-440">HR</span></span></td>
<td><span data-ttu-id="72735-441">10001</span><span class="sxs-lookup"><span data-stu-id="72735-441">10001</span></span></td>
<td><span data-ttu-id="72735-442">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-442">Electricity</span></span></td>
<td><span data-ttu-id="72735-443">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-443">Variable cost</span></span></td>
<td><span data-ttu-id="72735-444">-30,00</span><span class="sxs-lookup"><span data-stu-id="72735-444">-30.00</span></span></td>
<td><span data-ttu-id="72735-445">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-446">Proj 1</span><span class="sxs-lookup"><span data-stu-id="72735-446">Proj 1</span></span></td>
<td><span data-ttu-id="72735-447">Interní projekt 1</span><span class="sxs-lookup"><span data-stu-id="72735-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="72735-448">10001</span><span class="sxs-lookup"><span data-stu-id="72735-448">10001</span></span></td>
<td><span data-ttu-id="72735-449">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-449">Electricity</span></span></td>
<td><span data-ttu-id="72735-450">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-450">Variable cost</span></span></td>
<td><span data-ttu-id="72735-451">30.00</span><span class="sxs-lookup"><span data-stu-id="72735-451">30.00</span></span></td>
<td><span data-ttu-id="72735-452">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-453">CC001</span><span class="sxs-lookup"><span data-stu-id="72735-453">CC001</span></span></td>
<td><span data-ttu-id="72735-454">HR</span><span class="sxs-lookup"><span data-stu-id="72735-454">HR</span></span></td>
<td><span data-ttu-id="72735-455">10001</span><span class="sxs-lookup"><span data-stu-id="72735-455">10001</span></span></td>
<td><span data-ttu-id="72735-456">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-456">Electricity</span></span></td>
<td><span data-ttu-id="72735-457">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-457">Variable cost</span></span></td>
<td><span data-ttu-id="72735-458">-10,00</span><span class="sxs-lookup"><span data-stu-id="72735-458">-10.00</span></span></td>
<td><span data-ttu-id="72735-459">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-460">Proj 2</span><span class="sxs-lookup"><span data-stu-id="72735-460">Proj 2</span></span></td>
<td><span data-ttu-id="72735-461">Interní projekt 2</span><span class="sxs-lookup"><span data-stu-id="72735-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="72735-462">10001</span><span class="sxs-lookup"><span data-stu-id="72735-462">10001</span></span></td>
<td><span data-ttu-id="72735-463">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-463">Electricity</span></span></td>
<td><span data-ttu-id="72735-464">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-464">Variable cost</span></span></td>
<td><span data-ttu-id="72735-465">10,00</span><span class="sxs-lookup"><span data-stu-id="72735-465">10.00</span></span></td>
<td><span data-ttu-id="72735-466">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="72735-467">Podrobné informace o zásadách sazby režijních nákladů najdete v tématech Zásady sazby režijních nákladů a Základy přidělení.</span><span class="sxs-lookup"><span data-stu-id="72735-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="72735-468">(Všimněte si, že toto téma ještě není dokončené, ale bud k dispozici již brzy.)</span><span class="sxs-lookup"><span data-stu-id="72735-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="72735-469">Krok 4: Zpracování výpočtu přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="72735-470">Přidělení se používá k přidělení zůstatku objektu nákladů do jiných objektů nákladů použitím základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="72735-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="72735-471">Aplikace Finance and Operations podporuje reciproční metodu přidělování.</span><span class="sxs-lookup"><span data-stu-id="72735-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="72735-472">V metodě vzájemného přidělení jsou plně rozpoznány vzájemné služby, které si vyměňují pomocné objekty nákladů.</span><span class="sxs-lookup"><span data-stu-id="72735-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="72735-473">Systém automaticky určí provádění přidělení ve správném pořadí.</span><span class="sxs-lookup"><span data-stu-id="72735-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="72735-474">Zůstatek objektu nákladů je přidělen jedním základem přidělení.</span><span class="sxs-lookup"><span data-stu-id="72735-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="72735-475">Je podporováno přidělování napříč dimenzemi objektů nákladů a jejich příslušných členů.</span><span class="sxs-lookup"><span data-stu-id="72735-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="72735-476">Pořadí přidělení je řízeno jednotkou řízení nákladů.</span><span class="sxs-lookup"><span data-stu-id="72735-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="72735-477">[![Reciproční metoda](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="72735-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="72735-478">Definice přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-478">Define the cost allocation</span></span>

<span data-ttu-id="72735-479">Toto je jednoduchý příklad, který vysvětluje, jakým způsobem lze sledovat tok nákladů.</span><span class="sxs-lookup"><span data-stu-id="72735-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="72735-480">Objekt nákladů objektu CC001 HR přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="72735-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="72735-481">Vytvoří se člen statistické dimenzi s názvem služby lidských zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="72735-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="72735-482">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-482">Cost object</span></span></th>
<th><span data-ttu-id="72735-483">Služby HR</span><span class="sxs-lookup"><span data-stu-id="72735-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="72735-484">CC002</span><span class="sxs-lookup"><span data-stu-id="72735-484">CC002</span></span></td>
<td><span data-ttu-id="72735-485">Finance</span><span class="sxs-lookup"><span data-stu-id="72735-485">Finance</span></span></td>
<td><span data-ttu-id="72735-486">35</span><span class="sxs-lookup"><span data-stu-id="72735-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-487">CC003</span><span class="sxs-lookup"><span data-stu-id="72735-487">CC003</span></span></td>
<td><span data-ttu-id="72735-488">Sestavení</span><span class="sxs-lookup"><span data-stu-id="72735-488">Assembly</span></span></td>
<td><span data-ttu-id="72735-489">55</span><span class="sxs-lookup"><span data-stu-id="72735-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-490">CC004</span><span class="sxs-lookup"><span data-stu-id="72735-490">CC004</span></span></td>
<td><span data-ttu-id="72735-491">Balení</span><span class="sxs-lookup"><span data-stu-id="72735-491">Packaging</span></span></td>
<td><span data-ttu-id="72735-492">10</span><span class="sxs-lookup"><span data-stu-id="72735-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="72735-493">Objekt nákladů objektu CC002 Finance přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="72735-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="72735-494">Vytvoří se člen statistické dimenzi s názvem Finanční služby k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="72735-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="72735-495">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-495">Cost object</span></span></th>
<th><span data-ttu-id="72735-496">Finanční služby</span><span class="sxs-lookup"><span data-stu-id="72735-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="72735-497">CC003</span><span class="sxs-lookup"><span data-stu-id="72735-497">CC003</span></span></td>
<td><span data-ttu-id="72735-498">Sestavení</span><span class="sxs-lookup"><span data-stu-id="72735-498">Assembly</span></span></td>
<td><span data-ttu-id="72735-499">65</span><span class="sxs-lookup"><span data-stu-id="72735-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-500">CC004</span><span class="sxs-lookup"><span data-stu-id="72735-500">CC004</span></span></td>
<td><span data-ttu-id="72735-501">Balení</span><span class="sxs-lookup"><span data-stu-id="72735-501">Packaging</span></span></td>
<td><span data-ttu-id="72735-502">35</span><span class="sxs-lookup"><span data-stu-id="72735-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="72735-503">Objekt nákladů objektu CC003 Sestavení přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="72735-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="72735-504">Vytvoří se člen statistické dimenzi s názvem Služby sestavení zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="72735-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="72735-505">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-505">Cost object</span></span></th>
<th><span data-ttu-id="72735-506">Služby sestavení (v hodinách)</span><span class="sxs-lookup"><span data-stu-id="72735-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="72735-507">Prod 1</span><span class="sxs-lookup"><span data-stu-id="72735-507">Prod 1</span></span></td>
<td><span data-ttu-id="72735-508">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="72735-508">Product 1</span></span></td>
<td><span data-ttu-id="72735-509">60</span><span class="sxs-lookup"><span data-stu-id="72735-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-510">Prod 2</span><span class="sxs-lookup"><span data-stu-id="72735-510">Prod 2</span></span></td>
<td><span data-ttu-id="72735-511">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="72735-511">Product 2</span></span></td>
<td><span data-ttu-id="72735-512">20</span><span class="sxs-lookup"><span data-stu-id="72735-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="72735-513">Objekt nákladů objektu CC004 Balení přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="72735-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="72735-514">Vytvoří se člen statistické dimenzi s názvem Služby balení k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="72735-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="72735-515">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-515">Cost object</span></span></th>
<th><span data-ttu-id="72735-516">Služby balení (v hodinách)</span><span class="sxs-lookup"><span data-stu-id="72735-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="72735-517">Prod 1</span><span class="sxs-lookup"><span data-stu-id="72735-517">Prod 1</span></span></td>
<td><span data-ttu-id="72735-518">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="72735-518">Product 1</span></span></td>
<td><span data-ttu-id="72735-519">80</span><span class="sxs-lookup"><span data-stu-id="72735-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-520">Prod 2</span><span class="sxs-lookup"><span data-stu-id="72735-520">Prod 2</span></span></td>
<td><span data-ttu-id="72735-521">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="72735-521">Product 2</span></span></td>
<td><span data-ttu-id="72735-522">září</span><span class="sxs-lookup"><span data-stu-id="72735-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="72735-523">**Poznámka:** V aplikaci Finance and Operations lze odvodit statistická měření, jako je například výrobní doba spotřebovaná produktem, z datového zdroje.</span><span class="sxs-lookup"><span data-stu-id="72735-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="72735-524">Podrobnější informace o poskytovatelích statistických měření získáte v tématu Šablony poskytovatelů statistického měření.</span><span class="sxs-lookup"><span data-stu-id="72735-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="72735-525">(Všimněte si, že toto téma ještě není dokončeno, ale bude k dispozici brzy.) V následující tabulce jsou uvedeny výsledky použití HR služeb HR jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="72735-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="72735-526">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-526">Cost object</span></span></th>
<th><span data-ttu-id="72735-527">Hodnota</span><span class="sxs-lookup"><span data-stu-id="72735-527">Magnitude</span></span></th>
<th><span data-ttu-id="72735-528">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="72735-528">Allocation factor</span></span></th>
<th><span data-ttu-id="72735-529">Částka</span><span class="sxs-lookup"><span data-stu-id="72735-529">Amount</span></span></th>
<th><span data-ttu-id="72735-530">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="72735-531">CC002</span><span class="sxs-lookup"><span data-stu-id="72735-531">CC002</span></span></td>
<td><span data-ttu-id="72735-532">Finance</span><span class="sxs-lookup"><span data-stu-id="72735-532">Finance</span></span></td>
<td><span data-ttu-id="72735-533">35</span><span class="sxs-lookup"><span data-stu-id="72735-533">35</span></span></td>
<td><span data-ttu-id="72735-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="72735-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="72735-535">175.00</span><span class="sxs-lookup"><span data-stu-id="72735-535">175.00</span></span></td>
<td><span data-ttu-id="72735-536">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-537">CC003</span><span class="sxs-lookup"><span data-stu-id="72735-537">CC003</span></span></td>
<td><span data-ttu-id="72735-538">Sestavení</span><span class="sxs-lookup"><span data-stu-id="72735-538">Assembly</span></span></td>
<td><span data-ttu-id="72735-539">55</span><span class="sxs-lookup"><span data-stu-id="72735-539">55</span></span></td>
<td><span data-ttu-id="72735-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="72735-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="72735-541">275.00</span><span class="sxs-lookup"><span data-stu-id="72735-541">275.00</span></span></td>
<td><span data-ttu-id="72735-542">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-543">CC004</span><span class="sxs-lookup"><span data-stu-id="72735-543">CC004</span></span></td>
<td><span data-ttu-id="72735-544">Balení</span><span class="sxs-lookup"><span data-stu-id="72735-544">Packaging</span></span></td>
<td><span data-ttu-id="72735-545">10</span><span class="sxs-lookup"><span data-stu-id="72735-545">10</span></span></td>
<td><span data-ttu-id="72735-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="72735-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="72735-547">50,00</span><span class="sxs-lookup"><span data-stu-id="72735-547">50.00</span></span></td>
<td><span data-ttu-id="72735-548">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-549">CC002</span><span class="sxs-lookup"><span data-stu-id="72735-549">CC002</span></span></td>
<td><span data-ttu-id="72735-550">Finance</span><span class="sxs-lookup"><span data-stu-id="72735-550">Finance</span></span></td>
<td><span data-ttu-id="72735-551">35</span><span class="sxs-lookup"><span data-stu-id="72735-551">35</span></span></td>
<td><span data-ttu-id="72735-552">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="72735-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="72735-553">436.00</span><span class="sxs-lookup"><span data-stu-id="72735-553">436.00</span></span></td>
<td><span data-ttu-id="72735-554">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-555">CC003</span><span class="sxs-lookup"><span data-stu-id="72735-555">CC003</span></span></td>
<td><span data-ttu-id="72735-556">Sestavení</span><span class="sxs-lookup"><span data-stu-id="72735-556">Assembly</span></span></td>
<td><span data-ttu-id="72735-557">55</span><span class="sxs-lookup"><span data-stu-id="72735-557">55</span></span></td>
<td><span data-ttu-id="72735-558">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="72735-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="72735-559">685.14</span><span class="sxs-lookup"><span data-stu-id="72735-559">685.14</span></span></td>
<td><span data-ttu-id="72735-560">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-561">CC004</span><span class="sxs-lookup"><span data-stu-id="72735-561">CC004</span></span></td>
<td><span data-ttu-id="72735-562">Balení</span><span class="sxs-lookup"><span data-stu-id="72735-562">Packaging</span></span></td>
<td><span data-ttu-id="72735-563">10</span><span class="sxs-lookup"><span data-stu-id="72735-563">10</span></span></td>
<td><span data-ttu-id="72735-564">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="72735-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="72735-565">124.57</span><span class="sxs-lookup"><span data-stu-id="72735-565">124.57</span></span></td>
<td><span data-ttu-id="72735-566">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="72735-567">V následující tabulce je uveden výsledek při použití Finančních služeb Finance jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="72735-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="72735-568">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-568">Cost object</span></span></th>
<th><span data-ttu-id="72735-569">Hodnota</span><span class="sxs-lookup"><span data-stu-id="72735-569">Magnitude</span></span></th>
<th><span data-ttu-id="72735-570">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="72735-570">Allocation factor</span></span></th>
<th><span data-ttu-id="72735-571">Částka</span><span class="sxs-lookup"><span data-stu-id="72735-571">Amount</span></span></th>
<th><span data-ttu-id="72735-572">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="72735-573">CC003</span><span class="sxs-lookup"><span data-stu-id="72735-573">CC003</span></span></td>
<td><span data-ttu-id="72735-574">Sestavení</span><span class="sxs-lookup"><span data-stu-id="72735-574">Assembly</span></span></td>
<td><span data-ttu-id="72735-575">65</span><span class="sxs-lookup"><span data-stu-id="72735-575">65</span></span></td>
<td><span data-ttu-id="72735-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="72735-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="72735-577">438.75</span><span class="sxs-lookup"><span data-stu-id="72735-577">438.75</span></span></td>
<td><span data-ttu-id="72735-578">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-579">CC004</span><span class="sxs-lookup"><span data-stu-id="72735-579">CC004</span></span></td>
<td><span data-ttu-id="72735-580">Balení</span><span class="sxs-lookup"><span data-stu-id="72735-580">Packaging</span></span></td>
<td><span data-ttu-id="72735-581">35</span><span class="sxs-lookup"><span data-stu-id="72735-581">35</span></span></td>
<td><span data-ttu-id="72735-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="72735-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="72735-583">236.25</span><span class="sxs-lookup"><span data-stu-id="72735-583">236.25</span></span></td>
<td><span data-ttu-id="72735-584">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-585">CC003</span><span class="sxs-lookup"><span data-stu-id="72735-585">CC003</span></span></td>
<td><span data-ttu-id="72735-586">Sestavení</span><span class="sxs-lookup"><span data-stu-id="72735-586">Assembly</span></span></td>
<td><span data-ttu-id="72735-587">65</span><span class="sxs-lookup"><span data-stu-id="72735-587">65</span></span></td>
<td><span data-ttu-id="72735-588">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="72735-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="72735-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="72735-589">5,297.69</span></span></td>
<td><span data-ttu-id="72735-590">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-591">CC004</span><span class="sxs-lookup"><span data-stu-id="72735-591">CC004</span></span></td>
<td><span data-ttu-id="72735-592">Balení</span><span class="sxs-lookup"><span data-stu-id="72735-592">Packaging</span></span></td>
<td><span data-ttu-id="72735-593">35</span><span class="sxs-lookup"><span data-stu-id="72735-593">35</span></span></td>
<td><span data-ttu-id="72735-594">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="72735-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="72735-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="72735-595">2,852.60</span></span></td>
<td><span data-ttu-id="72735-596">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="72735-597">V následující tabulce je uveden výsledek při použití Služeb sestavení jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="72735-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="72735-598">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-598">Cost object</span></span></th>
<th><span data-ttu-id="72735-599">Hodnota</span><span class="sxs-lookup"><span data-stu-id="72735-599">Magnitude</span></span></th>
<th><span data-ttu-id="72735-600">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="72735-600">Allocation factor</span></span></th>
<th><span data-ttu-id="72735-601">Částka</span><span class="sxs-lookup"><span data-stu-id="72735-601">Amount</span></span></th>
<th><span data-ttu-id="72735-602">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="72735-603">Prod 1</span><span class="sxs-lookup"><span data-stu-id="72735-603">Prod 1</span></span></td>
<td><span data-ttu-id="72735-604">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="72735-604">Product 1</span></span></td>
<td><span data-ttu-id="72735-605">60</span><span class="sxs-lookup"><span data-stu-id="72735-605">60</span></span></td>
<td><span data-ttu-id="72735-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="72735-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="72735-607">535.31</span><span class="sxs-lookup"><span data-stu-id="72735-607">535.31</span></span></td>
<td><span data-ttu-id="72735-608">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-609">Prod 2</span><span class="sxs-lookup"><span data-stu-id="72735-609">Prod 2</span></span></td>
<td><span data-ttu-id="72735-610">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="72735-610">Product 2</span></span></td>
<td><span data-ttu-id="72735-611">20</span><span class="sxs-lookup"><span data-stu-id="72735-611">20</span></span></td>
<td><span data-ttu-id="72735-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="72735-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="72735-613">178.44</span><span class="sxs-lookup"><span data-stu-id="72735-613">178.44</span></span></td>
<td><span data-ttu-id="72735-614">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-615">Prod 1</span><span class="sxs-lookup"><span data-stu-id="72735-615">Prod 1</span></span></td>
<td><span data-ttu-id="72735-616">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="72735-616">Product 1</span></span></td>
<td><span data-ttu-id="72735-617">60</span><span class="sxs-lookup"><span data-stu-id="72735-617">60</span></span></td>
<td><span data-ttu-id="72735-618">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="72735-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="72735-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="72735-619">4,487.12</span></span></td>
<td><span data-ttu-id="72735-620">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-621">Prod 2</span><span class="sxs-lookup"><span data-stu-id="72735-621">Prod 2</span></span></td>
<td><span data-ttu-id="72735-622">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="72735-622">Product 2</span></span></td>
<td><span data-ttu-id="72735-623">20</span><span class="sxs-lookup"><span data-stu-id="72735-623">20</span></span></td>
<td><span data-ttu-id="72735-624">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="72735-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="72735-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="72735-625">1,495.71</span></span></td>
<td><span data-ttu-id="72735-626">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="72735-627">V následující tabulce je uveden výsledek při použití Služeb balení jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="72735-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="72735-628">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-628">Cost object</span></span></th>
<th><span data-ttu-id="72735-629">Hodnota</span><span class="sxs-lookup"><span data-stu-id="72735-629">Magnitude</span></span></th>
<th><span data-ttu-id="72735-630">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="72735-630">Allocation factor</span></span></th>
<th><span data-ttu-id="72735-631">Částka</span><span class="sxs-lookup"><span data-stu-id="72735-631">Amount</span></span></th>
<th><span data-ttu-id="72735-632">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="72735-633">Prod 1</span><span class="sxs-lookup"><span data-stu-id="72735-633">Prod 1</span></span></td>
<td><span data-ttu-id="72735-634">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="72735-634">Product 1</span></span></td>
<td><span data-ttu-id="72735-635">80</span><span class="sxs-lookup"><span data-stu-id="72735-635">80</span></span></td>
<td><span data-ttu-id="72735-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="72735-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="72735-637">241.05</span><span class="sxs-lookup"><span data-stu-id="72735-637">241.05</span></span></td>
<td><span data-ttu-id="72735-638">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-639">Prod 2</span><span class="sxs-lookup"><span data-stu-id="72735-639">Prod 2</span></span></td>
<td><span data-ttu-id="72735-640">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="72735-640">Product 2</span></span></td>
<td><span data-ttu-id="72735-641">15</span><span class="sxs-lookup"><span data-stu-id="72735-641">15</span></span></td>
<td><span data-ttu-id="72735-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="72735-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="72735-643">45.20</span><span class="sxs-lookup"><span data-stu-id="72735-643">45.20</span></span></td>
<td><span data-ttu-id="72735-644">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-645">Prod 1</span><span class="sxs-lookup"><span data-stu-id="72735-645">Prod 1</span></span></td>
<td><span data-ttu-id="72735-646">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="72735-646">Product 1</span></span></td>
<td><span data-ttu-id="72735-647">80</span><span class="sxs-lookup"><span data-stu-id="72735-647">80</span></span></td>
<td><span data-ttu-id="72735-648">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="72735-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="72735-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="72735-649">2,507.09</span></span></td>
<td><span data-ttu-id="72735-650">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-651">Prod 2</span><span class="sxs-lookup"><span data-stu-id="72735-651">Prod 2</span></span></td>
<td><span data-ttu-id="72735-652">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="72735-652">Product 2</span></span></td>
<td><span data-ttu-id="72735-653">15</span><span class="sxs-lookup"><span data-stu-id="72735-653">15</span></span></td>
<td><span data-ttu-id="72735-654">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="72735-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="72735-655">470.08</span><span class="sxs-lookup"><span data-stu-id="72735-655">470.08</span></span></td>
<td><span data-ttu-id="72735-656">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="72735-657">Položky deníku (položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="72735-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="72735-658">Deník</span><span class="sxs-lookup"><span data-stu-id="72735-658">Journal</span></span></th>
<th><span data-ttu-id="72735-659">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="72735-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="72735-660">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="72735-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="72735-661">Verze</span><span class="sxs-lookup"><span data-stu-id="72735-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="72735-662">00004</span><span class="sxs-lookup"><span data-stu-id="72735-662">00004</span></span></td>
<td><span data-ttu-id="72735-663">Deník přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="72735-664">Fiskální</span><span class="sxs-lookup"><span data-stu-id="72735-664">Fiscal</span></span></td>
<td><span data-ttu-id="72735-665">2017</span><span class="sxs-lookup"><span data-stu-id="72735-665">2017</span></span></td>
<td><span data-ttu-id="72735-666">Období 1</span><span class="sxs-lookup"><span data-stu-id="72735-666">Period 1</span></span></td>
<td><span data-ttu-id="72735-667">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="72735-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="72735-668">Řádky deníku</span><span class="sxs-lookup"><span data-stu-id="72735-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="72735-669">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="72735-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="72735-670">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="72735-671">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-671">Cost element</span></span></th>
<th><span data-ttu-id="72735-672">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-672">Cost behavior</span></span></th>
<th><span data-ttu-id="72735-673">Částka</span><span class="sxs-lookup"><span data-stu-id="72735-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="72735-674">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="72735-675">CC001</span><span class="sxs-lookup"><span data-stu-id="72735-675">CC001</span></span></td>
<td><span data-ttu-id="72735-676">HR</span><span class="sxs-lookup"><span data-stu-id="72735-676">HR</span></span></td>
<td><span data-ttu-id="72735-677">10001</span><span class="sxs-lookup"><span data-stu-id="72735-677">10001</span></span></td>
<td><span data-ttu-id="72735-678">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-678">Electricity</span></span></td>
<td><span data-ttu-id="72735-679">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-679">Fixed cost</span></span></td>
<td><span data-ttu-id="72735-680">500.00</span><span class="sxs-lookup"><span data-stu-id="72735-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-681">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="72735-682">CC001</span><span class="sxs-lookup"><span data-stu-id="72735-682">CC001</span></span></td>
<td><span data-ttu-id="72735-683">HR</span><span class="sxs-lookup"><span data-stu-id="72735-683">HR</span></span></td>
<td><span data-ttu-id="72735-684">10001</span><span class="sxs-lookup"><span data-stu-id="72735-684">10001</span></span></td>
<td><span data-ttu-id="72735-685">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-685">Electricity</span></span></td>
<td><span data-ttu-id="72735-686">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-686">Variable cost</span></span></td>
<td><span data-ttu-id="72735-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="72735-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-688">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="72735-689">CC002</span><span class="sxs-lookup"><span data-stu-id="72735-689">CC002</span></span></td>
<td><span data-ttu-id="72735-690">Finance</span><span class="sxs-lookup"><span data-stu-id="72735-690">Finance</span></span></td>
<td><span data-ttu-id="72735-691">10001</span><span class="sxs-lookup"><span data-stu-id="72735-691">10001</span></span></td>
<td><span data-ttu-id="72735-692">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-692">Electricity</span></span></td>
<td><span data-ttu-id="72735-693">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-693">Fixed cost</span></span></td>
<td><span data-ttu-id="72735-694">675.00</span><span class="sxs-lookup"><span data-stu-id="72735-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-695">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="72735-696">CC002</span><span class="sxs-lookup"><span data-stu-id="72735-696">CC002</span></span></td>
<td><span data-ttu-id="72735-697">Finance</span><span class="sxs-lookup"><span data-stu-id="72735-697">Finance</span></span></td>
<td><span data-ttu-id="72735-698">10001</span><span class="sxs-lookup"><span data-stu-id="72735-698">10001</span></span></td>
<td><span data-ttu-id="72735-699">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-699">Electricity</span></span></td>
<td><span data-ttu-id="72735-700">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-700">Variable cost</span></span></td>
<td><span data-ttu-id="72735-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="72735-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-702">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="72735-703">CC003</span><span class="sxs-lookup"><span data-stu-id="72735-703">CC003</span></span></td>
<td><span data-ttu-id="72735-704">Sestavení</span><span class="sxs-lookup"><span data-stu-id="72735-704">Assembly</span></span></td>
<td><span data-ttu-id="72735-705">10001</span><span class="sxs-lookup"><span data-stu-id="72735-705">10001</span></span></td>
<td><span data-ttu-id="72735-706">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-706">Electricity</span></span></td>
<td><span data-ttu-id="72735-707">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-707">Fixed cost</span></span></td>
<td><span data-ttu-id="72735-708">713.75</span><span class="sxs-lookup"><span data-stu-id="72735-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-709">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="72735-710">CC003</span><span class="sxs-lookup"><span data-stu-id="72735-710">CC003</span></span></td>
<td><span data-ttu-id="72735-711">Sestavení</span><span class="sxs-lookup"><span data-stu-id="72735-711">Assembly</span></span></td>
<td><span data-ttu-id="72735-712">10001</span><span class="sxs-lookup"><span data-stu-id="72735-712">10001</span></span></td>
<td><span data-ttu-id="72735-713">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-713">Electricity</span></span></td>
<td><span data-ttu-id="72735-714">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-714">Variable cost</span></span></td>
<td><span data-ttu-id="72735-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="72735-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-716">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="72735-717">CC003</span><span class="sxs-lookup"><span data-stu-id="72735-717">CC003</span></span></td>
<td><span data-ttu-id="72735-718">Balení</span><span class="sxs-lookup"><span data-stu-id="72735-718">Packaging</span></span></td>
<td><span data-ttu-id="72735-719">10001</span><span class="sxs-lookup"><span data-stu-id="72735-719">10001</span></span></td>
<td><span data-ttu-id="72735-720">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-720">Electricity</span></span></td>
<td><span data-ttu-id="72735-721">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-721">Fixed cost</span></span></td>
<td><span data-ttu-id="72735-722">286.25</span><span class="sxs-lookup"><span data-stu-id="72735-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-723">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="72735-724">CC003</span><span class="sxs-lookup"><span data-stu-id="72735-724">CC003</span></span></td>
<td><span data-ttu-id="72735-725">Balení</span><span class="sxs-lookup"><span data-stu-id="72735-725">Packaging</span></span></td>
<td><span data-ttu-id="72735-726">10001</span><span class="sxs-lookup"><span data-stu-id="72735-726">10001</span></span></td>
<td><span data-ttu-id="72735-727">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-727">Electricity</span></span></td>
<td><span data-ttu-id="72735-728">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-728">Variable cost</span></span></td>
<td><span data-ttu-id="72735-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="72735-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-730">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="72735-731">Prod 1</span><span class="sxs-lookup"><span data-stu-id="72735-731">Prod 1</span></span></td>
<td><span data-ttu-id="72735-732">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="72735-732">Product 1</span></span></td>
<td><span data-ttu-id="72735-733">10001</span><span class="sxs-lookup"><span data-stu-id="72735-733">10001</span></span></td>
<td><span data-ttu-id="72735-734">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-734">Electricity</span></span></td>
<td><span data-ttu-id="72735-735">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-735">Fixed cost</span></span></td>
<td><span data-ttu-id="72735-736">776.36</span><span class="sxs-lookup"><span data-stu-id="72735-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-737">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="72735-738">Prod 1</span><span class="sxs-lookup"><span data-stu-id="72735-738">Prod 1</span></span></td>
<td><span data-ttu-id="72735-739">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="72735-739">Product 1</span></span></td>
<td><span data-ttu-id="72735-740">10001</span><span class="sxs-lookup"><span data-stu-id="72735-740">10001</span></span></td>
<td><span data-ttu-id="72735-741">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-741">Electricity</span></span></td>
<td><span data-ttu-id="72735-742">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-742">Variable cost</span></span></td>
<td><span data-ttu-id="72735-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="72735-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-744">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="72735-745">Prod 2</span><span class="sxs-lookup"><span data-stu-id="72735-745">Prod 2</span></span></td>
<td><span data-ttu-id="72735-746">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="72735-746">Product 1</span></span></td>
<td><span data-ttu-id="72735-747">10001</span><span class="sxs-lookup"><span data-stu-id="72735-747">10001</span></span></td>
<td><span data-ttu-id="72735-748">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-748">Electricity</span></span></td>
<td><span data-ttu-id="72735-749">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-749">Fixed cost</span></span></td>
<td><span data-ttu-id="72735-750">223.64</span><span class="sxs-lookup"><span data-stu-id="72735-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-751">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="72735-752">Prod 2</span><span class="sxs-lookup"><span data-stu-id="72735-752">Prod 2</span></span></td>
<td><span data-ttu-id="72735-753">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="72735-753">Product 1</span></span></td>
<td><span data-ttu-id="72735-754">10001</span><span class="sxs-lookup"><span data-stu-id="72735-754">10001</span></span></td>
<td><span data-ttu-id="72735-755">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-755">Electricity</span></span></td>
<td><span data-ttu-id="72735-756">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-756">Variable cost</span></span></td>
<td><span data-ttu-id="72735-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="72735-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="72735-758">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="72735-759">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="72735-760">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-760">Cost element</span></span></th>
<th><span data-ttu-id="72735-761">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-761">Cost behavior</span></span></th>
<th><span data-ttu-id="72735-762">Částka</span><span class="sxs-lookup"><span data-stu-id="72735-762">Amount</span></span></th>
<th><span data-ttu-id="72735-763">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="72735-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="72735-764">CC001</span><span class="sxs-lookup"><span data-stu-id="72735-764">CC001</span></span></td>
<td><span data-ttu-id="72735-765">HR</span><span class="sxs-lookup"><span data-stu-id="72735-765">HR</span></span></td>
<td><span data-ttu-id="72735-766">10001</span><span class="sxs-lookup"><span data-stu-id="72735-766">10001</span></span></td>
<td><span data-ttu-id="72735-767">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-767">Electricity</span></span></td>
<td><span data-ttu-id="72735-768">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-768">Fixed cost</span></span></td>
<td><span data-ttu-id="72735-769">-500,00</span><span class="sxs-lookup"><span data-stu-id="72735-769">-500.00</span></span></td>
<td><span data-ttu-id="72735-770">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-771">CC002</span><span class="sxs-lookup"><span data-stu-id="72735-771">CC002</span></span></td>
<td><span data-ttu-id="72735-772">Finance</span><span class="sxs-lookup"><span data-stu-id="72735-772">Finance</span></span></td>
<td><span data-ttu-id="72735-773">10001</span><span class="sxs-lookup"><span data-stu-id="72735-773">10001</span></span></td>
<td><span data-ttu-id="72735-774">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-774">Electricity</span></span></td>
<td><span data-ttu-id="72735-775">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-775">Fixed cost</span></span></td>
<td><span data-ttu-id="72735-776">175.00</span><span class="sxs-lookup"><span data-stu-id="72735-776">175.00</span></span></td>
<td><span data-ttu-id="72735-777">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-778">CC003</span><span class="sxs-lookup"><span data-stu-id="72735-778">CC003</span></span></td>
<td><span data-ttu-id="72735-779">Sestavení</span><span class="sxs-lookup"><span data-stu-id="72735-779">Assembly</span></span></td>
<td><span data-ttu-id="72735-780">10001</span><span class="sxs-lookup"><span data-stu-id="72735-780">10001</span></span></td>
<td><span data-ttu-id="72735-781">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-781">Electricity</span></span></td>
<td><span data-ttu-id="72735-782">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-782">Fixed cost</span></span></td>
<td><span data-ttu-id="72735-783">275.00</span><span class="sxs-lookup"><span data-stu-id="72735-783">275.00</span></span></td>
<td><span data-ttu-id="72735-784">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-785">CC004</span><span class="sxs-lookup"><span data-stu-id="72735-785">CC004</span></span></td>
<td><span data-ttu-id="72735-786">Balení</span><span class="sxs-lookup"><span data-stu-id="72735-786">Packaging</span></span></td>
<td><span data-ttu-id="72735-787">10001</span><span class="sxs-lookup"><span data-stu-id="72735-787">10001</span></span></td>
<td><span data-ttu-id="72735-788">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-788">Electricity</span></span></td>
<td><span data-ttu-id="72735-789">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-789">Fixed cost</span></span></td>
<td><span data-ttu-id="72735-790">50,00</span><span class="sxs-lookup"><span data-stu-id="72735-790">50,00</span></span></td>
<td><span data-ttu-id="72735-791">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-792">CC001</span><span class="sxs-lookup"><span data-stu-id="72735-792">CC001</span></span></td>
<td><span data-ttu-id="72735-793">HR</span><span class="sxs-lookup"><span data-stu-id="72735-793">HR</span></span></td>
<td><span data-ttu-id="72735-794">10001</span><span class="sxs-lookup"><span data-stu-id="72735-794">10001</span></span></td>
<td><span data-ttu-id="72735-795">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-795">Electricity</span></span></td>
<td><span data-ttu-id="72735-796">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-796">Variable cost</span></span></td>
<td><span data-ttu-id="72735-797">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="72735-797">-1,245.71</span></span></td>
<td><span data-ttu-id="72735-798">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-799">CC002</span><span class="sxs-lookup"><span data-stu-id="72735-799">CC002</span></span></td>
<td><span data-ttu-id="72735-800">Finance</span><span class="sxs-lookup"><span data-stu-id="72735-800">Finance</span></span></td>
<td><span data-ttu-id="72735-801">10001</span><span class="sxs-lookup"><span data-stu-id="72735-801">10001</span></span></td>
<td><span data-ttu-id="72735-802">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-802">Electricity</span></span></td>
<td><span data-ttu-id="72735-803">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-803">Variable cost</span></span></td>
<td><span data-ttu-id="72735-804">436.00</span><span class="sxs-lookup"><span data-stu-id="72735-804">436.00</span></span></td>
<td><span data-ttu-id="72735-805">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-806">CC003</span><span class="sxs-lookup"><span data-stu-id="72735-806">CC003</span></span></td>
<td><span data-ttu-id="72735-807">Sestavení</span><span class="sxs-lookup"><span data-stu-id="72735-807">Assembly</span></span></td>
<td><span data-ttu-id="72735-808">10001</span><span class="sxs-lookup"><span data-stu-id="72735-808">10001</span></span></td>
<td><span data-ttu-id="72735-809">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-809">Electricity</span></span></td>
<td><span data-ttu-id="72735-810">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-810">Variable cost</span></span></td>
<td><span data-ttu-id="72735-811">685.14</span><span class="sxs-lookup"><span data-stu-id="72735-811">685.14</span></span></td>
<td><span data-ttu-id="72735-812">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-813">CC004</span><span class="sxs-lookup"><span data-stu-id="72735-813">CC004</span></span></td>
<td><span data-ttu-id="72735-814">Balení</span><span class="sxs-lookup"><span data-stu-id="72735-814">Packaging</span></span></td>
<td><span data-ttu-id="72735-815">10001</span><span class="sxs-lookup"><span data-stu-id="72735-815">10001</span></span></td>
<td><span data-ttu-id="72735-816">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-816">Electricity</span></span></td>
<td><span data-ttu-id="72735-817">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-817">Variable cost</span></span></td>
<td><span data-ttu-id="72735-818">124.57</span><span class="sxs-lookup"><span data-stu-id="72735-818">124.57</span></span></td>
<td><span data-ttu-id="72735-819">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-820">CC002</span><span class="sxs-lookup"><span data-stu-id="72735-820">CC002</span></span></td>
<td><span data-ttu-id="72735-821">Finance</span><span class="sxs-lookup"><span data-stu-id="72735-821">Finance</span></span></td>
<td><span data-ttu-id="72735-822">10001</span><span class="sxs-lookup"><span data-stu-id="72735-822">10001</span></span></td>
<td><span data-ttu-id="72735-823">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-823">Electricity</span></span></td>
<td><span data-ttu-id="72735-824">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-824">Fixed cost</span></span></td>
<td><span data-ttu-id="72735-825">-675,00</span><span class="sxs-lookup"><span data-stu-id="72735-825">-675.00</span></span></td>
<td><span data-ttu-id="72735-826">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-827">CC003</span><span class="sxs-lookup"><span data-stu-id="72735-827">CC003</span></span></td>
<td><span data-ttu-id="72735-828">Sestavení</span><span class="sxs-lookup"><span data-stu-id="72735-828">Assembly</span></span></td>
<td><span data-ttu-id="72735-829">10001</span><span class="sxs-lookup"><span data-stu-id="72735-829">10001</span></span></td>
<td><span data-ttu-id="72735-830">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-830">Electricity</span></span></td>
<td><span data-ttu-id="72735-831">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-831">Fixed cost</span></span></td>
<td><span data-ttu-id="72735-832">438.75</span><span class="sxs-lookup"><span data-stu-id="72735-832">438.75</span></span></td>
<td><span data-ttu-id="72735-833">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-834">CC004</span><span class="sxs-lookup"><span data-stu-id="72735-834">CC004</span></span></td>
<td><span data-ttu-id="72735-835">Balení</span><span class="sxs-lookup"><span data-stu-id="72735-835">Packaging</span></span></td>
<td><span data-ttu-id="72735-836">10001</span><span class="sxs-lookup"><span data-stu-id="72735-836">10001</span></span></td>
<td><span data-ttu-id="72735-837">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-837">Electricity</span></span></td>
<td><span data-ttu-id="72735-838">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-838">Fixed cost</span></span></td>
<td><span data-ttu-id="72735-839">236.25</span><span class="sxs-lookup"><span data-stu-id="72735-839">236.25</span></span></td>
<td><span data-ttu-id="72735-840">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-841">CC002</span><span class="sxs-lookup"><span data-stu-id="72735-841">CC002</span></span></td>
<td><span data-ttu-id="72735-842">Finance</span><span class="sxs-lookup"><span data-stu-id="72735-842">Finance</span></span></td>
<td><span data-ttu-id="72735-843">10001</span><span class="sxs-lookup"><span data-stu-id="72735-843">10001</span></span></td>
<td><span data-ttu-id="72735-844">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-844">Electricity</span></span></td>
<td><span data-ttu-id="72735-845">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-845">Variable cost</span></span></td>
<td><span data-ttu-id="72735-846">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="72735-846">-8,150.29</span></span></td>
<td><span data-ttu-id="72735-847">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-848">CC003</span><span class="sxs-lookup"><span data-stu-id="72735-848">CC003</span></span></td>
<td><span data-ttu-id="72735-849">Sestavení</span><span class="sxs-lookup"><span data-stu-id="72735-849">Assembly</span></span></td>
<td><span data-ttu-id="72735-850">10001</span><span class="sxs-lookup"><span data-stu-id="72735-850">10001</span></span></td>
<td><span data-ttu-id="72735-851">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-851">Electricity</span></span></td>
<td><span data-ttu-id="72735-852">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-852">Variable cost</span></span></td>
<td><span data-ttu-id="72735-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="72735-853">5,297.69</span></span></td>
<td><span data-ttu-id="72735-854">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-855">CC004</span><span class="sxs-lookup"><span data-stu-id="72735-855">CC004</span></span></td>
<td><span data-ttu-id="72735-856">Balení</span><span class="sxs-lookup"><span data-stu-id="72735-856">Packaging</span></span></td>
<td><span data-ttu-id="72735-857">10001</span><span class="sxs-lookup"><span data-stu-id="72735-857">10001</span></span></td>
<td><span data-ttu-id="72735-858">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-858">Electricity</span></span></td>
<td><span data-ttu-id="72735-859">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-859">Variable cost</span></span></td>
<td><span data-ttu-id="72735-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="72735-860">2,852.60</span></span></td>
<td><span data-ttu-id="72735-861">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-862">CC003</span><span class="sxs-lookup"><span data-stu-id="72735-862">CC003</span></span></td>
<td><span data-ttu-id="72735-863">Sestavení</span><span class="sxs-lookup"><span data-stu-id="72735-863">Assembly</span></span></td>
<td><span data-ttu-id="72735-864">10001</span><span class="sxs-lookup"><span data-stu-id="72735-864">10001</span></span></td>
<td><span data-ttu-id="72735-865">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-865">Electricity</span></span></td>
<td><span data-ttu-id="72735-866">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-866">Fixed cost</span></span></td>
<td><span data-ttu-id="72735-867">-713,75</span><span class="sxs-lookup"><span data-stu-id="72735-867">-713.75</span></span></td>
<td><span data-ttu-id="72735-868">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-869">Prod 1</span><span class="sxs-lookup"><span data-stu-id="72735-869">Prod 1</span></span></td>
<td><span data-ttu-id="72735-870">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="72735-870">Product 1</span></span></td>
<td><span data-ttu-id="72735-871">10001</span><span class="sxs-lookup"><span data-stu-id="72735-871">10001</span></span></td>
<td><span data-ttu-id="72735-872">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-872">Electricity</span></span></td>
<td><span data-ttu-id="72735-873">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-873">Fixed cost</span></span></td>
<td><span data-ttu-id="72735-874">535.31</span><span class="sxs-lookup"><span data-stu-id="72735-874">535.31</span></span></td>
<td><span data-ttu-id="72735-875">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-876">Prod 2</span><span class="sxs-lookup"><span data-stu-id="72735-876">Prod 2</span></span></td>
<td><span data-ttu-id="72735-877">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="72735-877">Product 2</span></span></td>
<td><span data-ttu-id="72735-878">10001</span><span class="sxs-lookup"><span data-stu-id="72735-878">10001</span></span></td>
<td><span data-ttu-id="72735-879">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-879">Electricity</span></span></td>
<td><span data-ttu-id="72735-880">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-880">Fixed cost</span></span></td>
<td><span data-ttu-id="72735-881">178.44</span><span class="sxs-lookup"><span data-stu-id="72735-881">178.44</span></span></td>
<td><span data-ttu-id="72735-882">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-883">CC003</span><span class="sxs-lookup"><span data-stu-id="72735-883">CC003</span></span></td>
<td><span data-ttu-id="72735-884">Sestavení</span><span class="sxs-lookup"><span data-stu-id="72735-884">Assembly</span></span></td>
<td><span data-ttu-id="72735-885">10001</span><span class="sxs-lookup"><span data-stu-id="72735-885">10001</span></span></td>
<td><span data-ttu-id="72735-886">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-886">Electricity</span></span></td>
<td><span data-ttu-id="72735-887">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-887">Variable cost</span></span></td>
<td><span data-ttu-id="72735-888">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="72735-888">-5,982.83</span></span></td>
<td><span data-ttu-id="72735-889">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-890">Prod 1</span><span class="sxs-lookup"><span data-stu-id="72735-890">Prod 1</span></span></td>
<td><span data-ttu-id="72735-891">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="72735-891">Product 1</span></span></td>
<td><span data-ttu-id="72735-892">10001</span><span class="sxs-lookup"><span data-stu-id="72735-892">10001</span></span></td>
<td><span data-ttu-id="72735-893">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-893">Electricity</span></span></td>
<td><span data-ttu-id="72735-894">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-894">Variable cost</span></span></td>
<td><span data-ttu-id="72735-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="72735-895">4,487.12</span></span></td>
<td><span data-ttu-id="72735-896">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-897">Prod 2</span><span class="sxs-lookup"><span data-stu-id="72735-897">Prod 2</span></span></td>
<td><span data-ttu-id="72735-898">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="72735-898">Product 2</span></span></td>
<td><span data-ttu-id="72735-899">10001</span><span class="sxs-lookup"><span data-stu-id="72735-899">10001</span></span></td>
<td><span data-ttu-id="72735-900">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-900">Electricity</span></span></td>
<td><span data-ttu-id="72735-901">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-901">Variable cost</span></span></td>
<td><span data-ttu-id="72735-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="72735-902">1,495.71</span></span></td>
<td><span data-ttu-id="72735-903">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-904">CC003</span><span class="sxs-lookup"><span data-stu-id="72735-904">CC003</span></span></td>
<td><span data-ttu-id="72735-905">Sestavení</span><span class="sxs-lookup"><span data-stu-id="72735-905">Assembly</span></span></td>
<td><span data-ttu-id="72735-906">10001</span><span class="sxs-lookup"><span data-stu-id="72735-906">10001</span></span></td>
<td><span data-ttu-id="72735-907">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-907">Electricity</span></span></td>
<td><span data-ttu-id="72735-908">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-908">Fixed cost</span></span></td>
<td><span data-ttu-id="72735-909">-286,25</span><span class="sxs-lookup"><span data-stu-id="72735-909">-286.25</span></span></td>
<td><span data-ttu-id="72735-910">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-911">Prod 1</span><span class="sxs-lookup"><span data-stu-id="72735-911">Prod 1</span></span></td>
<td><span data-ttu-id="72735-912">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="72735-912">Product 1</span></span></td>
<td><span data-ttu-id="72735-913">10001</span><span class="sxs-lookup"><span data-stu-id="72735-913">10001</span></span></td>
<td><span data-ttu-id="72735-914">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-914">Electricity</span></span></td>
<td><span data-ttu-id="72735-915">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-915">Fixed cost</span></span></td>
<td><span data-ttu-id="72735-916">241.05</span><span class="sxs-lookup"><span data-stu-id="72735-916">241.05</span></span></td>
<td><span data-ttu-id="72735-917">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-918">Prod 2</span><span class="sxs-lookup"><span data-stu-id="72735-918">Prod 2</span></span></td>
<td><span data-ttu-id="72735-919">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="72735-919">Product 2</span></span></td>
<td><span data-ttu-id="72735-920">10001</span><span class="sxs-lookup"><span data-stu-id="72735-920">10001</span></span></td>
<td><span data-ttu-id="72735-921">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-921">Electricity</span></span></td>
<td><span data-ttu-id="72735-922">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-922">Fixed cost</span></span></td>
<td><span data-ttu-id="72735-923">45.20</span><span class="sxs-lookup"><span data-stu-id="72735-923">45.20</span></span></td>
<td><span data-ttu-id="72735-924">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-925">CC003</span><span class="sxs-lookup"><span data-stu-id="72735-925">CC003</span></span></td>
<td><span data-ttu-id="72735-926">Sestavení</span><span class="sxs-lookup"><span data-stu-id="72735-926">Assembly</span></span></td>
<td><span data-ttu-id="72735-927">10001</span><span class="sxs-lookup"><span data-stu-id="72735-927">10001</span></span></td>
<td><span data-ttu-id="72735-928">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-928">Electricity</span></span></td>
<td><span data-ttu-id="72735-929">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-929">Variable cost</span></span></td>
<td><span data-ttu-id="72735-930">-2977,17</span><span class="sxs-lookup"><span data-stu-id="72735-930">-2,977.17</span></span></td>
<td><span data-ttu-id="72735-931">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-932">Prod 1</span><span class="sxs-lookup"><span data-stu-id="72735-932">Prod 1</span></span></td>
<td><span data-ttu-id="72735-933">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="72735-933">Product 1</span></span></td>
<td><span data-ttu-id="72735-934">10001</span><span class="sxs-lookup"><span data-stu-id="72735-934">10001</span></span></td>
<td><span data-ttu-id="72735-935">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-935">Electricity</span></span></td>
<td><span data-ttu-id="72735-936">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-936">Variable cost</span></span></td>
<td><span data-ttu-id="72735-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="72735-937">2,507.09</span></span></td>
<td><span data-ttu-id="72735-938">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="72735-939">Prod 2</span><span class="sxs-lookup"><span data-stu-id="72735-939">Prod 2</span></span></td>
<td><span data-ttu-id="72735-940">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="72735-940">Product 2</span></span></td>
<td><span data-ttu-id="72735-941">10001</span><span class="sxs-lookup"><span data-stu-id="72735-941">10001</span></span></td>
<td><span data-ttu-id="72735-942">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="72735-942">Electricity</span></span></td>
<td><span data-ttu-id="72735-943">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-943">Variable cost</span></span></td>
<td><span data-ttu-id="72735-944">470.08</span><span class="sxs-lookup"><span data-stu-id="72735-944">470.08</span></span></td>
<td><span data-ttu-id="72735-945">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="72735-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="72735-946">Závěr</span><span class="sxs-lookup"><span data-stu-id="72735-946">Conclusion</span></span>
<span data-ttu-id="72735-947">Ve finančním účtování se náklady za elektřinu ve výši 10 000 zaúčtují na ID fiktivního nákladového střediska.</span><span class="sxs-lookup"><span data-stu-id="72735-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="72735-948">Účetní tak budou vědět, že tento náklad musí být přidělen.</span><span class="sxs-lookup"><span data-stu-id="72735-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="72735-949">V nákladovém účetnictví náklady procházejí napříč organizačními jednotkami a úrovněmi, na základě použitých zásad a pravidel.</span><span class="sxs-lookup"><span data-stu-id="72735-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="72735-950">Každý náklad byl přidružen k základu přidělení, který poskytuje nejlepší hodnocení pro přidělení nákladů.</span><span class="sxs-lookup"><span data-stu-id="72735-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="72735-951">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="72735-952">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="72735-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="72735-953">Celkem</span><span class="sxs-lookup"><span data-stu-id="72735-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="72735-954">CC099</span><span class="sxs-lookup"><span data-stu-id="72735-954">CC099</span></span></th>
<th><span data-ttu-id="72735-955">CC001</span><span class="sxs-lookup"><span data-stu-id="72735-955">CC001</span></span></th>
<th><span data-ttu-id="72735-956">CC002</span><span class="sxs-lookup"><span data-stu-id="72735-956">CC002</span></span></th>
<th><span data-ttu-id="72735-957">CC003</span><span class="sxs-lookup"><span data-stu-id="72735-957">CC003</span></span></th>
<th><span data-ttu-id="72735-958">CC004</span><span class="sxs-lookup"><span data-stu-id="72735-958">CC004</span></span></th>
<th><span data-ttu-id="72735-959">Proj 1</span><span class="sxs-lookup"><span data-stu-id="72735-959">Proj 1</span></span></th>
<th><span data-ttu-id="72735-960">Proj 2</span><span class="sxs-lookup"><span data-stu-id="72735-960">Proj 2</span></span></th>
<th><span data-ttu-id="72735-961">Prod 1</span><span class="sxs-lookup"><span data-stu-id="72735-961">Prod 1</span></span></th>
<th><span data-ttu-id="72735-962">Prod 2</span><span class="sxs-lookup"><span data-stu-id="72735-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="72735-963">10001 Elektřina</span><span class="sxs-lookup"><span data-stu-id="72735-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="72735-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="72735-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="72735-965"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="72735-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="72735-966"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="72735-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="72735-967"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="72735-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="72735-968"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="72735-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="72735-969"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="72735-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="72735-970"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="72735-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="72735-971"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="72735-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="72735-972"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="72735-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="72735-973">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="72735-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="72735-974">0,00</span><span class="sxs-lookup"><span data-stu-id="72735-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="72735-975">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="72735-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="72735-976">0,00</span><span class="sxs-lookup"><span data-stu-id="72735-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="72735-977">0,00</span><span class="sxs-lookup"><span data-stu-id="72735-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="72735-978">0,00</span><span class="sxs-lookup"><span data-stu-id="72735-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="72735-979">0,00</span><span class="sxs-lookup"><span data-stu-id="72735-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="72735-980">0,00</span><span class="sxs-lookup"><span data-stu-id="72735-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="72735-981">776.36</span><span class="sxs-lookup"><span data-stu-id="72735-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="72735-982">223.64</span><span class="sxs-lookup"><span data-stu-id="72735-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="72735-983"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="72735-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="72735-984">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="72735-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="72735-985">000</span><span class="sxs-lookup"><span data-stu-id="72735-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="72735-986">0,00</span><span class="sxs-lookup"><span data-stu-id="72735-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="72735-987">0,00</span><span class="sxs-lookup"><span data-stu-id="72735-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="72735-988">0,00</span><span class="sxs-lookup"><span data-stu-id="72735-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="72735-989">0,00</span><span class="sxs-lookup"><span data-stu-id="72735-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="72735-990">30.00</span><span class="sxs-lookup"><span data-stu-id="72735-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="72735-991">10,00</span><span class="sxs-lookup"><span data-stu-id="72735-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="72735-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="72735-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="72735-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="72735-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="72735-994"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="72735-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="72735-995">Toto téma popisuje, jak primární prvek nákladů, 10001 Elektřina, prochází přes objekty nákladů.</span><span class="sxs-lookup"><span data-stu-id="72735-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="72735-996">Tyto režijní náklady tedy budou přiděleny na nejnižší úroveň v organizaci.</span><span class="sxs-lookup"><span data-stu-id="72735-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="72735-997">Jinak řečeno, objekty nákladů na nejnižší úrovni ponesou náklady.</span><span class="sxs-lookup"><span data-stu-id="72735-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="72735-998">Chcete-li vizuální tok nákladů mezi objekty nákladů, můžete použít pravidla zásad shrnutí nákladů pro vizualizaci jejich toků.</span><span class="sxs-lookup"><span data-stu-id="72735-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="72735-999">Podrobnější informace naleznete v tématu Zásady shrnutí nákladů.</span><span class="sxs-lookup"><span data-stu-id="72735-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="72735-1000">(Všimněte si, že toto téma ještě není dokončené, ale bud k dispozici již brzy.)</span><span class="sxs-lookup"><span data-stu-id="72735-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




