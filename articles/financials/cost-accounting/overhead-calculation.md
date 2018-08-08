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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: be548959985a6fcaabf482f1e5951024633283cf
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---

# <a name="overhead-calculation"></a><span data-ttu-id="822dd-103">Výpočet režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="822dd-104">Toto téma popisuje typické procesy pro výpočet a přidělení režijních nákladů.</span><span class="sxs-lookup"><span data-stu-id="822dd-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="822dd-105">Definice termínu</span><span class="sxs-lookup"><span data-stu-id="822dd-105">Term definition</span></span>
---------------

<span data-ttu-id="822dd-106">Režijní náklady jsou náklady, které nutně vznikají při chodu podnikání, ale nelze je připsat přímo k žádné konkrétní podnikatelské aktivitě, produktu nebo službě.</span><span class="sxs-lookup"><span data-stu-id="822dd-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="822dd-107">Režijní náklady poskytují důležitou podporu pro generování aktivity přinášejících zisk.</span><span class="sxs-lookup"><span data-stu-id="822dd-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="822dd-108">Následuje několik příkladů režijních nákladů:</span><span class="sxs-lookup"><span data-stu-id="822dd-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="822dd-109">Renta</span><span class="sxs-lookup"><span data-stu-id="822dd-109">Rent</span></span>
-   <span data-ttu-id="822dd-110">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-110">Electricity</span></span>
-   <span data-ttu-id="822dd-111">Administrativní mzdy</span><span class="sxs-lookup"><span data-stu-id="822dd-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="822dd-112">Přehled výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-112">Overhead calculation overview</span></span>
<span data-ttu-id="822dd-113">Výpočet režijních nákladů spustí zásady účtování nákladů ve správném pořadí.</span><span class="sxs-lookup"><span data-stu-id="822dd-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="822dd-114">Výpočet režijních nákladů můžete pro stejné fiskální období spustit mnohokrát, pokud došlo ke změně zásad účtování nákladů nebo zjištění konkrétních chyb.</span><span class="sxs-lookup"><span data-stu-id="822dd-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="822dd-115">Každé spuštění výpočtu režijních nákladů se ukládá a přijímá ID jedinečné verze, které vám umožní porovnávat výpočty v různých verzích.</span><span class="sxs-lookup"><span data-stu-id="822dd-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="822dd-116">Položky nákladů, které generuje výpočet režijních nákladů, přijímá datum účtování.</span><span class="sxs-lookup"><span data-stu-id="822dd-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="822dd-117">Toto datum účtován se shoduje s konvovým datem fiskálního období, které se použije ve výpočtu.</span><span class="sxs-lookup"><span data-stu-id="822dd-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="822dd-118">ID jedinečné verze se skládá z následujících prvků:</span><span class="sxs-lookup"><span data-stu-id="822dd-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="822dd-119">Typ verze</span><span class="sxs-lookup"><span data-stu-id="822dd-119">Version type</span></span>
-   <span data-ttu-id="822dd-120">Datum a čas</span><span class="sxs-lookup"><span data-stu-id="822dd-120">Date and time</span></span>
-   <span data-ttu-id="822dd-121">Hlavní kniha nákladového účetnictví</span><span class="sxs-lookup"><span data-stu-id="822dd-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="822dd-122">Fiskální rok</span><span class="sxs-lookup"><span data-stu-id="822dd-122">Fiscal year</span></span>
-   <span data-ttu-id="822dd-123">Fiskální období</span><span class="sxs-lookup"><span data-stu-id="822dd-123">Fiscal period</span></span>

<span data-ttu-id="822dd-124">Výpočet režijních nákladů se spustí bez ohledu na verzi.</span><span class="sxs-lookup"><span data-stu-id="822dd-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="822dd-125">Proto lze vypočítat rozpočtovou verzi před skutečnou verzí.</span><span class="sxs-lookup"><span data-stu-id="822dd-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="822dd-126">Výpočet režijních nákladů se skládá ze čtyř kroků uvedených na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="822dd-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="822dd-127">V každé fázi je vytvořeno záhlaví deníku, které obsahuje položky deníku.</span><span class="sxs-lookup"><span data-stu-id="822dd-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="822dd-128">Toto záhlaví deníku zachovává vstupní data pro každý krok výpočtu.</span><span class="sxs-lookup"><span data-stu-id="822dd-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="822dd-129">Zásady a pravidla se použijí na každý řádek deníku a položky nákladů jsou generovány jako výstup.</span><span class="sxs-lookup"><span data-stu-id="822dd-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="822dd-130">Máte tedy vždy plnou sledovatelnost.</span><span class="sxs-lookup"><span data-stu-id="822dd-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="822dd-131">[![Výpočet režijních nákladů](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="822dd-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="822dd-132">Výpočet a přidělení režijních nákladů za elektřinu</span><span class="sxs-lookup"><span data-stu-id="822dd-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="822dd-133">Ve finančním účetnictví se některé náklady, jako je například elektřina, registrují jako paušální.</span><span class="sxs-lookup"><span data-stu-id="822dd-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="822dd-134">Podrobný přehled pro vedoucí není tedy pro nákladové účetnictví k dispozici.</span><span class="sxs-lookup"><span data-stu-id="822dd-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="822dd-135">V nákladovém účetnictví musí náklady procházet organizačními jednotkami, aby byl získán správný přehled pro vedoucí napříč všemi jednotkami a úrovněmi organizace.</span><span class="sxs-lookup"><span data-stu-id="822dd-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="822dd-136">Tento tok musí být založen buď na přesném záznamu spotřeby nebo na objektivním hodnocení.</span><span class="sxs-lookup"><span data-stu-id="822dd-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="822dd-137">V hlavní knize mohou být zaúčtovány náklady na elektřinu způsobem znázorněným v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="822dd-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="822dd-138">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="822dd-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="822dd-139">Nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="822dd-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="822dd-140">Hlavní účet</span><span class="sxs-lookup"><span data-stu-id="822dd-140">Main account</span></span></th>
<th><span data-ttu-id="822dd-141">Částka v zúčtovací měně</span><span class="sxs-lookup"><span data-stu-id="822dd-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="822dd-142">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="822dd-143">CC099</span><span class="sxs-lookup"><span data-stu-id="822dd-143">CC099</span></span></td>
<td><span data-ttu-id="822dd-144">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="822dd-144">Default cost center</span></span></td>
<td><span data-ttu-id="822dd-145">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-145">10001</span></span></td>
<td><span data-ttu-id="822dd-146">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-146">Electricity</span></span></td>
<td><span data-ttu-id="822dd-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="822dd-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="822dd-148">Krok 1: Zpracování výpočtu chování nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="822dd-149">Ve výchozím nastavení dostanou při importu položek nákladů z datového zdroje tyto položky v nákladovém účetnictví klasifikaci **Neklasifikované**.</span><span class="sxs-lookup"><span data-stu-id="822dd-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="822dd-150">Použitím pravidla zásad chování nákladů lze reklasifikovat položky nákladů jako **Pevné náklady** nebo **Variabilní náklady**.</span><span class="sxs-lookup"><span data-stu-id="822dd-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="822dd-151">Definice pravidel chování nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-151">Define the cost behavior rule</span></span>

<span data-ttu-id="822dd-152">V některých případech je část nákladů s pevným poplatkem a zbývající náklady jsou založeny na spotřebě.</span><span class="sxs-lookup"><span data-stu-id="822dd-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="822dd-153">Účty za elektřinu často odpovídají této definici.</span><span class="sxs-lookup"><span data-stu-id="822dd-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="822dd-154">Po platbě konkrétního pevného poplatku platíte spotřebu za kilowatthodinu (kWh).</span><span class="sxs-lookup"><span data-stu-id="822dd-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="822dd-155">Pokud je například poplatek pevných nákladů 1 000,00, definuje se pravidlo chování nákladů takto:</span><span class="sxs-lookup"><span data-stu-id="822dd-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="822dd-156">Pevná částka 1 000,00</span><span class="sxs-lookup"><span data-stu-id="822dd-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="822dd-157">0 &lt;= 1 000,00 = Pevná</span><span class="sxs-lookup"><span data-stu-id="822dd-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="822dd-158">1 000,01 &lt; N = Variabilní</span><span class="sxs-lookup"><span data-stu-id="822dd-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="822dd-159">Deník</span><span class="sxs-lookup"><span data-stu-id="822dd-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="822dd-160">Deník</span><span class="sxs-lookup"><span data-stu-id="822dd-160">Journal</span></span></th>
<th><span data-ttu-id="822dd-161">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="822dd-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="822dd-162">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="822dd-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="822dd-163">Verze</span><span class="sxs-lookup"><span data-stu-id="822dd-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="822dd-164">00001</span><span class="sxs-lookup"><span data-stu-id="822dd-164">00001</span></span></td>
<td><span data-ttu-id="822dd-165">Deník výpočtu chování nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="822dd-166">Fiskální</span><span class="sxs-lookup"><span data-stu-id="822dd-166">Fiscal</span></span></td>
<td><span data-ttu-id="822dd-167">2017</span><span class="sxs-lookup"><span data-stu-id="822dd-167">2017</span></span></td>
<td><span data-ttu-id="822dd-168">Období 1</span><span class="sxs-lookup"><span data-stu-id="822dd-168">Period 1</span></span></td>
<td><span data-ttu-id="822dd-169">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="822dd-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="822dd-170">Položky deníku (Položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="822dd-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="822dd-171">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="822dd-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="822dd-172">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="822dd-173">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-173">Cost element</span></span></th>
<th><span data-ttu-id="822dd-174">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-174">Cost behavior</span></span></th>
<th><span data-ttu-id="822dd-175">Částka</span><span class="sxs-lookup"><span data-stu-id="822dd-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="822dd-176">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="822dd-177">CC099</span><span class="sxs-lookup"><span data-stu-id="822dd-177">CC099</span></span></td>
<td><span data-ttu-id="822dd-178">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="822dd-178">Default cost center</span></span></td>
<td><span data-ttu-id="822dd-179">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-179">10001</span></span></td>
<td><span data-ttu-id="822dd-180">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-180">Electricity</span></span></td>
<td><span data-ttu-id="822dd-181">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="822dd-181">Unclassified</span></span></td>
<td><span data-ttu-id="822dd-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="822dd-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="822dd-183">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="822dd-184">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="822dd-185">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-185">Cost element</span></span></th>
<th><span data-ttu-id="822dd-186">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-186">Cost behavior</span></span></th>
<th><span data-ttu-id="822dd-187">Částka</span><span class="sxs-lookup"><span data-stu-id="822dd-187">Amount</span></span></th>
<th><span data-ttu-id="822dd-188">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="822dd-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="822dd-189">CC099</span><span class="sxs-lookup"><span data-stu-id="822dd-189">CC099</span></span></td>
<td><span data-ttu-id="822dd-190">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="822dd-190">Default cost center</span></span></td>
<td><span data-ttu-id="822dd-191">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-191">10001</span></span></td>
<td><span data-ttu-id="822dd-192">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-192">Electricity</span></span></td>
<td><span data-ttu-id="822dd-193">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="822dd-193">Unclassified</span></span></td>
<td><span data-ttu-id="822dd-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="822dd-194">10,000.00</span></span></td>
<td><span data-ttu-id="822dd-195">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-196">CC099</span><span class="sxs-lookup"><span data-stu-id="822dd-196">CC099</span></span></td>
<td><span data-ttu-id="822dd-197">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="822dd-197">Default cost center</span></span></td>
<td><span data-ttu-id="822dd-198">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-198">10001</span></span></td>
<td><span data-ttu-id="822dd-199">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-199">Electricity</span></span></td>
<td><span data-ttu-id="822dd-200">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="822dd-200">Unclassified</span></span></td>
<td><span data-ttu-id="822dd-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="822dd-201">-10,000.00</span></span></td>
<td><span data-ttu-id="822dd-202">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-203">CC099</span><span class="sxs-lookup"><span data-stu-id="822dd-203">CC099</span></span></td>
<td><span data-ttu-id="822dd-204">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="822dd-204">Default cost center</span></span></td>
<td><span data-ttu-id="822dd-205">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-205">10001</span></span></td>
<td><span data-ttu-id="822dd-206">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-206">Electricity</span></span></td>
<td><span data-ttu-id="822dd-207">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-207">Fixed cost</span></span></td>
<td><span data-ttu-id="822dd-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="822dd-208">1,000.00</span></span></td>
<td><span data-ttu-id="822dd-209">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-210">CC099</span><span class="sxs-lookup"><span data-stu-id="822dd-210">CC099</span></span></td>
<td><span data-ttu-id="822dd-211">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="822dd-211">Default cost center</span></span></td>
<td><span data-ttu-id="822dd-212">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-212">10001</span></span></td>
<td><span data-ttu-id="822dd-213">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-213">Electricity</span></span></td>
<td><span data-ttu-id="822dd-214">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-214">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="822dd-215">9,000.00</span></span></td>
<td><span data-ttu-id="822dd-216">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="822dd-217">Ohledně podrobných informací o chování nákladů nahlédněte do zásad chování nákladů.</span><span class="sxs-lookup"><span data-stu-id="822dd-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="822dd-218">(Všimněte si, že toto téma ještě není dokončené, ale bud k dispozici již brzy.)</span><span class="sxs-lookup"><span data-stu-id="822dd-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="822dd-219">Krok 2: Zpracování výpočtu distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="822dd-220">Distribuce nákladů se používá k rozdělení nákladů z jednoho objektu nákladů na jeden nebo více dalších objektů nákladů použitím příslušného základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="822dd-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="822dd-221">Distribuce nákladů a přidělení nákladů se liší v tom, že k distribuci nákladů dochází vždy na úrovni primárního prvku nákladů původních nákladů.</span><span class="sxs-lookup"><span data-stu-id="822dd-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="822dd-222">Definice pravidel distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-222">Define the cost distribution rule</span></span>

<span data-ttu-id="822dd-223">Ve finančním účetnictví se náklady na elektřinu často registrují jako paušální.</span><span class="sxs-lookup"><span data-stu-id="822dd-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="822dd-224">V nákladovém účetnictví není tento přístup dostatečně podrobný.</span><span class="sxs-lookup"><span data-stu-id="822dd-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="822dd-225">Variabilní náklady by měly být distribuovány k jednotlivým objektům nákladů na solidním základě.</span><span class="sxs-lookup"><span data-stu-id="822dd-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="822dd-226">Nejlogičtější základ přidělení je spotřeba elektřiny (kWh).</span><span class="sxs-lookup"><span data-stu-id="822dd-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="822dd-227">Vytvoří se člen statistické dimenzi s názvem Elektřina a zaznamená se elektrické spotřeba.</span><span class="sxs-lookup"><span data-stu-id="822dd-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="822dd-228">Ve výchozím nastavení se všechny členy statistické dimenze stanou dostupnými zpřístupněny jako základy přidělení.</span><span class="sxs-lookup"><span data-stu-id="822dd-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="822dd-229">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-229">Cost object</span></span></th>
<th><span data-ttu-id="822dd-230">kWh</span><span class="sxs-lookup"><span data-stu-id="822dd-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="822dd-231">CC001</span><span class="sxs-lookup"><span data-stu-id="822dd-231">CC001</span></span></td>
<td><span data-ttu-id="822dd-232">HR</span><span class="sxs-lookup"><span data-stu-id="822dd-232">HR</span></span></td>
<td><span data-ttu-id="822dd-233">1 000</span><span class="sxs-lookup"><span data-stu-id="822dd-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-234">CC002</span><span class="sxs-lookup"><span data-stu-id="822dd-234">CC002</span></span></td>
<td><span data-ttu-id="822dd-235">Finance</span><span class="sxs-lookup"><span data-stu-id="822dd-235">Finance</span></span></td>
<td><span data-ttu-id="822dd-236">6,000</span><span class="sxs-lookup"><span data-stu-id="822dd-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-237">CC003</span><span class="sxs-lookup"><span data-stu-id="822dd-237">CC003</span></span></td>
<td><span data-ttu-id="822dd-238">Sestavení</span><span class="sxs-lookup"><span data-stu-id="822dd-238">Assembly</span></span></td>
<td><span data-ttu-id="822dd-239">0</span><span class="sxs-lookup"><span data-stu-id="822dd-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="822dd-240">Následující tabulka zobrazuje výsledek při použití elektrické spotřeby jako základu přidělení pro variabilní náklady.</span><span class="sxs-lookup"><span data-stu-id="822dd-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="822dd-241">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-241">Cost object</span></span></th>
<th><span data-ttu-id="822dd-242">Hodnota</span><span class="sxs-lookup"><span data-stu-id="822dd-242">Magnitude</span></span></th>
<th><span data-ttu-id="822dd-243">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="822dd-243">Allocation factor</span></span></th>
<th><span data-ttu-id="822dd-244">Částka</span><span class="sxs-lookup"><span data-stu-id="822dd-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="822dd-245">CC001</span><span class="sxs-lookup"><span data-stu-id="822dd-245">CC001</span></span></td>
<td><span data-ttu-id="822dd-246">HR</span><span class="sxs-lookup"><span data-stu-id="822dd-246">HR</span></span></td>
<td><span data-ttu-id="822dd-247">1 000</span><span class="sxs-lookup"><span data-stu-id="822dd-247">1,000</span></span></td>
<td><span data-ttu-id="822dd-248">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="822dd-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="822dd-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="822dd-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-250">CC002</span><span class="sxs-lookup"><span data-stu-id="822dd-250">CC002</span></span></td>
<td><span data-ttu-id="822dd-251">Finance</span><span class="sxs-lookup"><span data-stu-id="822dd-251">Finance</span></span></td>
<td><span data-ttu-id="822dd-252">6,000</span><span class="sxs-lookup"><span data-stu-id="822dd-252">6,000</span></span></td>
<td><span data-ttu-id="822dd-253">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="822dd-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="822dd-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="822dd-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-255">CC003</span><span class="sxs-lookup"><span data-stu-id="822dd-255">CC003</span></span></td>
<td><span data-ttu-id="822dd-256">Sestavení</span><span class="sxs-lookup"><span data-stu-id="822dd-256">Assembly</span></span></td>
<td><span data-ttu-id="822dd-257">0</span><span class="sxs-lookup"><span data-stu-id="822dd-257">0</span></span></td>
<td><span data-ttu-id="822dd-258">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="822dd-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="822dd-259">0,00</span><span class="sxs-lookup"><span data-stu-id="822dd-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="822dd-260">Pevné náklady musí být distribuovány rovnoměrně k jednotlivých objektům nákladů, které spotřebovávaly elektřinu.</span><span class="sxs-lookup"><span data-stu-id="822dd-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="822dd-261">Tohoto výsledku můžete dosáhnout pomocí členu statistické dimenze Elektřina v základu přidělení vzorce: (Elektřina &gt; 0,00) Následující tabulka zobrazuje výsledek při použití elektrické spotřeby jako základu přidělení pro variabilní náklady.</span><span class="sxs-lookup"><span data-stu-id="822dd-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="822dd-262">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-262">Cost object</span></span></th>
<th><span data-ttu-id="822dd-263">Vzorec</span><span class="sxs-lookup"><span data-stu-id="822dd-263">Formula</span></span></th>
<th><span data-ttu-id="822dd-264">Hodnota</span><span class="sxs-lookup"><span data-stu-id="822dd-264">Magnitude</span></span></th>
<th><span data-ttu-id="822dd-265">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="822dd-265">Allocation factor</span></span></th>
<th><span data-ttu-id="822dd-266">Částka</span><span class="sxs-lookup"><span data-stu-id="822dd-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="822dd-267">CC001</span><span class="sxs-lookup"><span data-stu-id="822dd-267">CC001</span></span></td>
<td><span data-ttu-id="822dd-268">HR</span><span class="sxs-lookup"><span data-stu-id="822dd-268">HR</span></span></td>
<td><span data-ttu-id="822dd-269">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="822dd-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="822dd-270">1</span><span class="sxs-lookup"><span data-stu-id="822dd-270">1</span></span></td>
<td><span data-ttu-id="822dd-271">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="822dd-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="822dd-272">500.00</span><span class="sxs-lookup"><span data-stu-id="822dd-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-273">CC002</span><span class="sxs-lookup"><span data-stu-id="822dd-273">CC002</span></span></td>
<td><span data-ttu-id="822dd-274">Finance</span><span class="sxs-lookup"><span data-stu-id="822dd-274">Finance</span></span></td>
<td><span data-ttu-id="822dd-275">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="822dd-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="822dd-276">1</span><span class="sxs-lookup"><span data-stu-id="822dd-276">1</span></span></td>
<td><span data-ttu-id="822dd-277">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="822dd-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="822dd-278">500.00</span><span class="sxs-lookup"><span data-stu-id="822dd-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-279">CC003</span><span class="sxs-lookup"><span data-stu-id="822dd-279">CC003</span></span></td>
<td><span data-ttu-id="822dd-280">Sestavení</span><span class="sxs-lookup"><span data-stu-id="822dd-280">Assembly</span></span></td>
<td><span data-ttu-id="822dd-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="822dd-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="822dd-282">0</span><span class="sxs-lookup"><span data-stu-id="822dd-282">0</span></span></td>
<td><span data-ttu-id="822dd-283">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="822dd-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="822dd-284">0,00</span><span class="sxs-lookup"><span data-stu-id="822dd-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="822dd-285">Deník</span><span class="sxs-lookup"><span data-stu-id="822dd-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="822dd-286">Deník</span><span class="sxs-lookup"><span data-stu-id="822dd-286">Journal</span></span></th>
<th><span data-ttu-id="822dd-287">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="822dd-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="822dd-288">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="822dd-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="822dd-289">Verze</span><span class="sxs-lookup"><span data-stu-id="822dd-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="822dd-290">00002</span><span class="sxs-lookup"><span data-stu-id="822dd-290">00002</span></span></td>
<td><span data-ttu-id="822dd-291">Deník výpočtu distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="822dd-292">Fiskální</span><span class="sxs-lookup"><span data-stu-id="822dd-292">Fiscal</span></span></td>
<td><span data-ttu-id="822dd-293">2017</span><span class="sxs-lookup"><span data-stu-id="822dd-293">2017</span></span></td>
<td><span data-ttu-id="822dd-294">Období 1</span><span class="sxs-lookup"><span data-stu-id="822dd-294">Period 1</span></span></td>
<td><span data-ttu-id="822dd-295">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="822dd-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="822dd-296">Položky deníku (Položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="822dd-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="822dd-297">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="822dd-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="822dd-298">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="822dd-299">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-299">Cost element</span></span></th>
<th><span data-ttu-id="822dd-300">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-300">Cost behavior</span></span></th>
<th><span data-ttu-id="822dd-301">Částka</span><span class="sxs-lookup"><span data-stu-id="822dd-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="822dd-302">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="822dd-303">CC099</span><span class="sxs-lookup"><span data-stu-id="822dd-303">CC099</span></span></td>
<td><span data-ttu-id="822dd-304">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="822dd-304">Default cost center</span></span></td>
<td><span data-ttu-id="822dd-305">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-305">10001</span></span></td>
<td><span data-ttu-id="822dd-306">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-306">Electricity</span></span></td>
<td><span data-ttu-id="822dd-307">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-307">Fixed cost</span></span></td>
<td><span data-ttu-id="822dd-308">1 000,00</span><span class="sxs-lookup"><span data-stu-id="822dd-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-309">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="822dd-310">CC099</span><span class="sxs-lookup"><span data-stu-id="822dd-310">CC099</span></span></td>
<td><span data-ttu-id="822dd-311">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="822dd-311">Default cost center</span></span></td>
<td><span data-ttu-id="822dd-312">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-312">10001</span></span></td>
<td><span data-ttu-id="822dd-313">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-313">Electricity</span></span></td>
<td><span data-ttu-id="822dd-314">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-314">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="822dd-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="822dd-316">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="822dd-317">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="822dd-318">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-318">Cost element</span></span></th>
<th><span data-ttu-id="822dd-319">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-319">Cost behavior</span></span></th>
<th><span data-ttu-id="822dd-320">Částka</span><span class="sxs-lookup"><span data-stu-id="822dd-320">Amount</span></span></th>
<th><span data-ttu-id="822dd-321">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="822dd-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="822dd-322">CC099</span><span class="sxs-lookup"><span data-stu-id="822dd-322">CC099</span></span></td>
<td><span data-ttu-id="822dd-323">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="822dd-323">Default cost center</span></span></td>
<td><span data-ttu-id="822dd-324">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-324">10001</span></span></td>
<td><span data-ttu-id="822dd-325">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-325">Electricity</span></span></td>
<td><span data-ttu-id="822dd-326">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-326">Fixed cost</span></span></td>
<td><span data-ttu-id="822dd-327">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="822dd-327">-1,000.00</span></span></td>
<td><span data-ttu-id="822dd-328">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-329">CC001</span><span class="sxs-lookup"><span data-stu-id="822dd-329">CC001</span></span></td>
<td><span data-ttu-id="822dd-330">HR</span><span class="sxs-lookup"><span data-stu-id="822dd-330">HR</span></span></td>
<td><span data-ttu-id="822dd-331">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-331">10001</span></span></td>
<td><span data-ttu-id="822dd-332">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-332">Electricity</span></span></td>
<td><span data-ttu-id="822dd-333">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-333">Fixed cost</span></span></td>
<td><span data-ttu-id="822dd-334">500.00</span><span class="sxs-lookup"><span data-stu-id="822dd-334">500.00</span></span></td>
<td><span data-ttu-id="822dd-335">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-336">CC002</span><span class="sxs-lookup"><span data-stu-id="822dd-336">CC002</span></span></td>
<td><span data-ttu-id="822dd-337">Finance</span><span class="sxs-lookup"><span data-stu-id="822dd-337">Finance</span></span></td>
<td><span data-ttu-id="822dd-338">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-338">10001</span></span></td>
<td><span data-ttu-id="822dd-339">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-339">Electricity</span></span></td>
<td><span data-ttu-id="822dd-340">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-340">Fixed cost</span></span></td>
<td><span data-ttu-id="822dd-341">500.00</span><span class="sxs-lookup"><span data-stu-id="822dd-341">500.00</span></span></td>
<td><span data-ttu-id="822dd-342">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-343">CC099</span><span class="sxs-lookup"><span data-stu-id="822dd-343">CC099</span></span></td>
<td><span data-ttu-id="822dd-344">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="822dd-344">Default cost center</span></span></td>
<td><span data-ttu-id="822dd-345">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-345">10001</span></span></td>
<td><span data-ttu-id="822dd-346">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-346">Electricity</span></span></td>
<td><span data-ttu-id="822dd-347">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-347">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-348">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="822dd-348">-9,000.00</span></span></td>
<td><span data-ttu-id="822dd-349">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-350">CC001</span><span class="sxs-lookup"><span data-stu-id="822dd-350">CC001</span></span></td>
<td><span data-ttu-id="822dd-351">HR</span><span class="sxs-lookup"><span data-stu-id="822dd-351">HR</span></span></td>
<td><span data-ttu-id="822dd-352">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-352">10001</span></span></td>
<td><span data-ttu-id="822dd-353">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-353">Electricity</span></span></td>
<td><span data-ttu-id="822dd-354">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-354">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="822dd-355">1,285.71</span></span></td>
<td><span data-ttu-id="822dd-356">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-357">CC002</span><span class="sxs-lookup"><span data-stu-id="822dd-357">CC002</span></span></td>
<td><span data-ttu-id="822dd-358">Finance</span><span class="sxs-lookup"><span data-stu-id="822dd-358">Finance</span></span></td>
<td><span data-ttu-id="822dd-359">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-359">10001</span></span></td>
<td><span data-ttu-id="822dd-360">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-360">Electricity</span></span></td>
<td><span data-ttu-id="822dd-361">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-361">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="822dd-362">7,714.29</span></span></td>
<td><span data-ttu-id="822dd-363">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="822dd-364">Podrobné informace o základech distribuce a přidělení nákladů získáte v tématech Zásady distribuce nákladů a Základy přidělení.</span><span class="sxs-lookup"><span data-stu-id="822dd-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="822dd-365">(Všimněte si, že toto téma ještě není dokončené, ale bud k dispozici již brzy.)</span><span class="sxs-lookup"><span data-stu-id="822dd-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="822dd-366">Krok 3: Zpracování výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="822dd-367">Režijní náklady se používají k účtování jednoho nebo více konkrétních objektů nákladů.</span><span class="sxs-lookup"><span data-stu-id="822dd-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="822dd-368">Účtování je založeno na předem určené nákladové sazbě a množství z přiřazeného základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="822dd-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="822dd-369">Definice sazby režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-369">Define the overhead rate</span></span>

<span data-ttu-id="822dd-370">Objekt nákladů CC001 HR přispívá k sadě interních projektů.</span><span class="sxs-lookup"><span data-stu-id="822dd-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="822dd-371">Vytvoří se člen statistické dimenzi s názvem projekty lidských zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="822dd-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="822dd-372">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-372">Cost object</span></span></th>
<th><span data-ttu-id="822dd-373">Pracovní doba</span><span class="sxs-lookup"><span data-stu-id="822dd-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="822dd-374">Proj 1</span><span class="sxs-lookup"><span data-stu-id="822dd-374">Proj 1</span></span></td>
<td><span data-ttu-id="822dd-375">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="822dd-375">Project 1</span></span></td>
<td><span data-ttu-id="822dd-376">3</span><span class="sxs-lookup"><span data-stu-id="822dd-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-377">Proj 2</span><span class="sxs-lookup"><span data-stu-id="822dd-377">Proj 2</span></span></td>
<td><span data-ttu-id="822dd-378">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="822dd-378">Project 2</span></span></td>
<td><span data-ttu-id="822dd-379">1</span><span class="sxs-lookup"><span data-stu-id="822dd-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="822dd-380">Byla definována předem určená nákladová sazba pro příspěvky k nákladovým projektům.</span><span class="sxs-lookup"><span data-stu-id="822dd-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="822dd-381">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-381">Cost object</span></span></th>
<th><span data-ttu-id="822dd-382">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-382">Cost element</span></span></th>
<th><span data-ttu-id="822dd-383">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-383">Cost behavior</span></span></th>
<th><span data-ttu-id="822dd-384">Jednotky</span><span class="sxs-lookup"><span data-stu-id="822dd-384">Units</span></span></th>
<th><span data-ttu-id="822dd-385">Kurz</span><span class="sxs-lookup"><span data-stu-id="822dd-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="822dd-386">CC001</span><span class="sxs-lookup"><span data-stu-id="822dd-386">CC001</span></span></td>
<td><span data-ttu-id="822dd-387">HR</span><span class="sxs-lookup"><span data-stu-id="822dd-387">HR</span></span></td>
<td><span data-ttu-id="822dd-388">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-388">10001</span></span></td>
<td><span data-ttu-id="822dd-389">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-389">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-390">1</span><span class="sxs-lookup"><span data-stu-id="822dd-390">1</span></span></td>
<td><span data-ttu-id="822dd-391">10</span><span class="sxs-lookup"><span data-stu-id="822dd-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="822dd-392">Následující tabulka zobrazuje výsledek při použití projektů lidských zdrojů jako základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="822dd-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="822dd-393">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-393">Cost object</span></span></th>
<th><span data-ttu-id="822dd-394">Hodnota</span><span class="sxs-lookup"><span data-stu-id="822dd-394">Magnitude</span></span></th>
<th><span data-ttu-id="822dd-395">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-395">Cost element</span></span></th>
<th><span data-ttu-id="822dd-396">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="822dd-396">Allocation factor</span></span></th>
<th><span data-ttu-id="822dd-397">Částka</span><span class="sxs-lookup"><span data-stu-id="822dd-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="822dd-398">Proj 1</span><span class="sxs-lookup"><span data-stu-id="822dd-398">Proj 1</span></span></td>
<td><span data-ttu-id="822dd-399">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="822dd-399">Project 1</span></span></td>
<td><span data-ttu-id="822dd-400">3</span><span class="sxs-lookup"><span data-stu-id="822dd-400">3</span></span></td>
<td><span data-ttu-id="822dd-401">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-401">10001</span></span></td>
<td><span data-ttu-id="822dd-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="822dd-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="822dd-403">30.00</span><span class="sxs-lookup"><span data-stu-id="822dd-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-404">Proj 2</span><span class="sxs-lookup"><span data-stu-id="822dd-404">Proj 2</span></span></td>
<td><span data-ttu-id="822dd-405">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="822dd-405">Project 2</span></span></td>
<td><span data-ttu-id="822dd-406">1</span><span class="sxs-lookup"><span data-stu-id="822dd-406">1</span></span></td>
<td><span data-ttu-id="822dd-407">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-407">10001</span></span></td>
<td><span data-ttu-id="822dd-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="822dd-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="822dd-409">10,00</span><span class="sxs-lookup"><span data-stu-id="822dd-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="822dd-410">Deník</span><span class="sxs-lookup"><span data-stu-id="822dd-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="822dd-411">Deník</span><span class="sxs-lookup"><span data-stu-id="822dd-411">Journal</span></span></th>
<th><span data-ttu-id="822dd-412">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="822dd-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="822dd-413">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="822dd-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="822dd-414">Verze</span><span class="sxs-lookup"><span data-stu-id="822dd-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="822dd-415">00003</span><span class="sxs-lookup"><span data-stu-id="822dd-415">00003</span></span></td>
<td><span data-ttu-id="822dd-416">Deník výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="822dd-417">Fiskální</span><span class="sxs-lookup"><span data-stu-id="822dd-417">Fiscal</span></span></td>
<td><span data-ttu-id="822dd-418">2017</span><span class="sxs-lookup"><span data-stu-id="822dd-418">2017</span></span></td>
<td><span data-ttu-id="822dd-419">Období 1</span><span class="sxs-lookup"><span data-stu-id="822dd-419">Period 1</span></span></td>
<td><span data-ttu-id="822dd-420">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="822dd-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="822dd-421">Položky deníku (položky deníku pro výpočet sazby režijních nákladů)</span><span class="sxs-lookup"><span data-stu-id="822dd-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="822dd-422">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="822dd-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="822dd-423">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-423">Cost object</span></span></th>
<th><span data-ttu-id="822dd-424">Hodnota</span><span class="sxs-lookup"><span data-stu-id="822dd-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="822dd-425">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="822dd-426">Proj 1</span><span class="sxs-lookup"><span data-stu-id="822dd-426">Proj 1</span></span></td>
<td><span data-ttu-id="822dd-427">Interní projekt 1</span><span class="sxs-lookup"><span data-stu-id="822dd-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="822dd-428">3,00</span><span class="sxs-lookup"><span data-stu-id="822dd-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-429">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="822dd-430">Proj 2</span><span class="sxs-lookup"><span data-stu-id="822dd-430">Proj 2</span></span></td>
<td><span data-ttu-id="822dd-431">Interní projekt 2</span><span class="sxs-lookup"><span data-stu-id="822dd-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="822dd-432">1.00</span><span class="sxs-lookup"><span data-stu-id="822dd-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="822dd-433">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="822dd-434">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="822dd-435">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-435">Cost element</span></span></th>
<th><span data-ttu-id="822dd-436">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-436">Cost behavior</span></span></th>
<th><span data-ttu-id="822dd-437">Částka</span><span class="sxs-lookup"><span data-stu-id="822dd-437">Amount</span></span></th>
<th><span data-ttu-id="822dd-438">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="822dd-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="822dd-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="822dd-439">CC0001</span></span></td>
<td><span data-ttu-id="822dd-440">HR</span><span class="sxs-lookup"><span data-stu-id="822dd-440">HR</span></span></td>
<td><span data-ttu-id="822dd-441">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-441">10001</span></span></td>
<td><span data-ttu-id="822dd-442">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-442">Electricity</span></span></td>
<td><span data-ttu-id="822dd-443">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-443">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-444">-30,00</span><span class="sxs-lookup"><span data-stu-id="822dd-444">-30.00</span></span></td>
<td><span data-ttu-id="822dd-445">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-446">Proj 1</span><span class="sxs-lookup"><span data-stu-id="822dd-446">Proj 1</span></span></td>
<td><span data-ttu-id="822dd-447">Interní projekt 1</span><span class="sxs-lookup"><span data-stu-id="822dd-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="822dd-448">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-448">10001</span></span></td>
<td><span data-ttu-id="822dd-449">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-449">Electricity</span></span></td>
<td><span data-ttu-id="822dd-450">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-450">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-451">30.00</span><span class="sxs-lookup"><span data-stu-id="822dd-451">30.00</span></span></td>
<td><span data-ttu-id="822dd-452">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-453">CC001</span><span class="sxs-lookup"><span data-stu-id="822dd-453">CC001</span></span></td>
<td><span data-ttu-id="822dd-454">HR</span><span class="sxs-lookup"><span data-stu-id="822dd-454">HR</span></span></td>
<td><span data-ttu-id="822dd-455">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-455">10001</span></span></td>
<td><span data-ttu-id="822dd-456">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-456">Electricity</span></span></td>
<td><span data-ttu-id="822dd-457">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-457">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-458">-10,00</span><span class="sxs-lookup"><span data-stu-id="822dd-458">-10.00</span></span></td>
<td><span data-ttu-id="822dd-459">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-460">Proj 2</span><span class="sxs-lookup"><span data-stu-id="822dd-460">Proj 2</span></span></td>
<td><span data-ttu-id="822dd-461">Interní projekt 2</span><span class="sxs-lookup"><span data-stu-id="822dd-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="822dd-462">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-462">10001</span></span></td>
<td><span data-ttu-id="822dd-463">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-463">Electricity</span></span></td>
<td><span data-ttu-id="822dd-464">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-464">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-465">10,00</span><span class="sxs-lookup"><span data-stu-id="822dd-465">10.00</span></span></td>
<td><span data-ttu-id="822dd-466">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="822dd-467">Podrobné informace o zásadách sazby režijních nákladů najdete v tématech Zásady sazby režijních nákladů a Základy přidělení.</span><span class="sxs-lookup"><span data-stu-id="822dd-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="822dd-468">(Všimněte si, že toto téma ještě není dokončené, ale bud k dispozici již brzy.)</span><span class="sxs-lookup"><span data-stu-id="822dd-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="822dd-469">Krok 4: Zpracování výpočtu přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="822dd-470">Přidělení se používá k přidělení zůstatku objektu nákladů do jiných objektů nákladů použitím základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="822dd-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="822dd-471">Aplikace Finance and Operations podporuje reciproční metodu přidělování.</span><span class="sxs-lookup"><span data-stu-id="822dd-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="822dd-472">V metodě vzájemného přidělení jsou plně rozpoznány vzájemné služby, které si vyměňují pomocné objekty nákladů.</span><span class="sxs-lookup"><span data-stu-id="822dd-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="822dd-473">Systém automaticky určí provádění přidělení ve správném pořadí.</span><span class="sxs-lookup"><span data-stu-id="822dd-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="822dd-474">Zůstatek objektu nákladů je přidělen jedním základem přidělení.</span><span class="sxs-lookup"><span data-stu-id="822dd-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="822dd-475">Je podporováno přidělování napříč dimenzemi objektů nákladů a jejich příslušných členů.</span><span class="sxs-lookup"><span data-stu-id="822dd-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="822dd-476">Pořadí přidělení je řízeno jednotkou řízení nákladů.</span><span class="sxs-lookup"><span data-stu-id="822dd-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="822dd-477">[![Reciproční metoda](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="822dd-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="822dd-478">Definice přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-478">Define the cost allocation</span></span>

<span data-ttu-id="822dd-479">Toto je jednoduchý příklad, který vysvětluje, jakým způsobem lze sledovat tok nákladů.</span><span class="sxs-lookup"><span data-stu-id="822dd-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="822dd-480">Objekt nákladů objektu CC001 HR přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="822dd-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="822dd-481">Vytvoří se člen statistické dimenzi s názvem služby lidských zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="822dd-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="822dd-482">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-482">Cost object</span></span></th>
<th><span data-ttu-id="822dd-483">Služby HR</span><span class="sxs-lookup"><span data-stu-id="822dd-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="822dd-484">CC002</span><span class="sxs-lookup"><span data-stu-id="822dd-484">CC002</span></span></td>
<td><span data-ttu-id="822dd-485">Finance</span><span class="sxs-lookup"><span data-stu-id="822dd-485">Finance</span></span></td>
<td><span data-ttu-id="822dd-486">35</span><span class="sxs-lookup"><span data-stu-id="822dd-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-487">CC003</span><span class="sxs-lookup"><span data-stu-id="822dd-487">CC003</span></span></td>
<td><span data-ttu-id="822dd-488">Sestavení</span><span class="sxs-lookup"><span data-stu-id="822dd-488">Assembly</span></span></td>
<td><span data-ttu-id="822dd-489">55</span><span class="sxs-lookup"><span data-stu-id="822dd-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-490">CC004</span><span class="sxs-lookup"><span data-stu-id="822dd-490">CC004</span></span></td>
<td><span data-ttu-id="822dd-491">Balení</span><span class="sxs-lookup"><span data-stu-id="822dd-491">Packaging</span></span></td>
<td><span data-ttu-id="822dd-492">10</span><span class="sxs-lookup"><span data-stu-id="822dd-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="822dd-493">Objekt nákladů objektu CC002 Finance přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="822dd-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="822dd-494">Vytvoří se člen statistické dimenzi s názvem Finanční služby k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="822dd-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="822dd-495">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-495">Cost object</span></span></th>
<th><span data-ttu-id="822dd-496">Finanční služby</span><span class="sxs-lookup"><span data-stu-id="822dd-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="822dd-497">CC003</span><span class="sxs-lookup"><span data-stu-id="822dd-497">CC003</span></span></td>
<td><span data-ttu-id="822dd-498">Sestavení</span><span class="sxs-lookup"><span data-stu-id="822dd-498">Assembly</span></span></td>
<td><span data-ttu-id="822dd-499">65</span><span class="sxs-lookup"><span data-stu-id="822dd-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-500">CC004</span><span class="sxs-lookup"><span data-stu-id="822dd-500">CC004</span></span></td>
<td><span data-ttu-id="822dd-501">Balení</span><span class="sxs-lookup"><span data-stu-id="822dd-501">Packaging</span></span></td>
<td><span data-ttu-id="822dd-502">35</span><span class="sxs-lookup"><span data-stu-id="822dd-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="822dd-503">Objekt nákladů objektu CC003 Sestavení přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="822dd-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="822dd-504">Vytvoří se člen statistické dimenzi s názvem Služby sestavení zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="822dd-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="822dd-505">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-505">Cost object</span></span></th>
<th><span data-ttu-id="822dd-506">Služby sestavení (v hodinách)</span><span class="sxs-lookup"><span data-stu-id="822dd-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="822dd-507">Prod 1</span><span class="sxs-lookup"><span data-stu-id="822dd-507">Prod 1</span></span></td>
<td><span data-ttu-id="822dd-508">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="822dd-508">Product 1</span></span></td>
<td><span data-ttu-id="822dd-509">60</span><span class="sxs-lookup"><span data-stu-id="822dd-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-510">Prod 2</span><span class="sxs-lookup"><span data-stu-id="822dd-510">Prod 2</span></span></td>
<td><span data-ttu-id="822dd-511">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="822dd-511">Product 2</span></span></td>
<td><span data-ttu-id="822dd-512">20</span><span class="sxs-lookup"><span data-stu-id="822dd-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="822dd-513">Objekt nákladů objektu CC004 Balení přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="822dd-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="822dd-514">Vytvoří se člen statistické dimenzi s názvem Služby balení k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="822dd-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="822dd-515">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-515">Cost object</span></span></th>
<th><span data-ttu-id="822dd-516">Služby balení (v hodinách)</span><span class="sxs-lookup"><span data-stu-id="822dd-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="822dd-517">Prod 1</span><span class="sxs-lookup"><span data-stu-id="822dd-517">Prod 1</span></span></td>
<td><span data-ttu-id="822dd-518">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="822dd-518">Product 1</span></span></td>
<td><span data-ttu-id="822dd-519">80</span><span class="sxs-lookup"><span data-stu-id="822dd-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-520">Prod 2</span><span class="sxs-lookup"><span data-stu-id="822dd-520">Prod 2</span></span></td>
<td><span data-ttu-id="822dd-521">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="822dd-521">Product 2</span></span></td>
<td><span data-ttu-id="822dd-522">15</span><span class="sxs-lookup"><span data-stu-id="822dd-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="822dd-523">**Poznámka:** V aplikaci Finance and Operations lze odvodit statistická měření, jako je například výrobní doba spotřebovaná produktem, z datového zdroje.</span><span class="sxs-lookup"><span data-stu-id="822dd-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="822dd-524">Podrobnější informace o poskytovatelích statistických měření získáte v tématu Šablony poskytovatelů statistického měření.</span><span class="sxs-lookup"><span data-stu-id="822dd-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="822dd-525">(Všimněte si, že toto téma ještě není dokončeno, ale bude k dispozici brzy.) V následující tabulce jsou uvedeny výsledky použití HR služeb HR jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="822dd-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="822dd-526">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-526">Cost object</span></span></th>
<th><span data-ttu-id="822dd-527">Hodnota</span><span class="sxs-lookup"><span data-stu-id="822dd-527">Magnitude</span></span></th>
<th><span data-ttu-id="822dd-528">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="822dd-528">Allocation factor</span></span></th>
<th><span data-ttu-id="822dd-529">Částka</span><span class="sxs-lookup"><span data-stu-id="822dd-529">Amount</span></span></th>
<th><span data-ttu-id="822dd-530">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="822dd-531">CC002</span><span class="sxs-lookup"><span data-stu-id="822dd-531">CC002</span></span></td>
<td><span data-ttu-id="822dd-532">Finance</span><span class="sxs-lookup"><span data-stu-id="822dd-532">Finance</span></span></td>
<td><span data-ttu-id="822dd-533">35</span><span class="sxs-lookup"><span data-stu-id="822dd-533">35</span></span></td>
<td><span data-ttu-id="822dd-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="822dd-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="822dd-535">175.00</span><span class="sxs-lookup"><span data-stu-id="822dd-535">175.00</span></span></td>
<td><span data-ttu-id="822dd-536">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-537">CC003</span><span class="sxs-lookup"><span data-stu-id="822dd-537">CC003</span></span></td>
<td><span data-ttu-id="822dd-538">Sestavení</span><span class="sxs-lookup"><span data-stu-id="822dd-538">Assembly</span></span></td>
<td><span data-ttu-id="822dd-539">55</span><span class="sxs-lookup"><span data-stu-id="822dd-539">55</span></span></td>
<td><span data-ttu-id="822dd-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="822dd-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="822dd-541">275.00</span><span class="sxs-lookup"><span data-stu-id="822dd-541">275.00</span></span></td>
<td><span data-ttu-id="822dd-542">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-543">CC004</span><span class="sxs-lookup"><span data-stu-id="822dd-543">CC004</span></span></td>
<td><span data-ttu-id="822dd-544">Balení</span><span class="sxs-lookup"><span data-stu-id="822dd-544">Packaging</span></span></td>
<td><span data-ttu-id="822dd-545">10</span><span class="sxs-lookup"><span data-stu-id="822dd-545">10</span></span></td>
<td><span data-ttu-id="822dd-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="822dd-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="822dd-547">50,00</span><span class="sxs-lookup"><span data-stu-id="822dd-547">50.00</span></span></td>
<td><span data-ttu-id="822dd-548">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-549">CC002</span><span class="sxs-lookup"><span data-stu-id="822dd-549">CC002</span></span></td>
<td><span data-ttu-id="822dd-550">Finance</span><span class="sxs-lookup"><span data-stu-id="822dd-550">Finance</span></span></td>
<td><span data-ttu-id="822dd-551">35</span><span class="sxs-lookup"><span data-stu-id="822dd-551">35</span></span></td>
<td><span data-ttu-id="822dd-552">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="822dd-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="822dd-553">436.00</span><span class="sxs-lookup"><span data-stu-id="822dd-553">436.00</span></span></td>
<td><span data-ttu-id="822dd-554">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-555">CC003</span><span class="sxs-lookup"><span data-stu-id="822dd-555">CC003</span></span></td>
<td><span data-ttu-id="822dd-556">Sestavení</span><span class="sxs-lookup"><span data-stu-id="822dd-556">Assembly</span></span></td>
<td><span data-ttu-id="822dd-557">55</span><span class="sxs-lookup"><span data-stu-id="822dd-557">55</span></span></td>
<td><span data-ttu-id="822dd-558">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="822dd-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="822dd-559">685.14</span><span class="sxs-lookup"><span data-stu-id="822dd-559">685.14</span></span></td>
<td><span data-ttu-id="822dd-560">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-561">CC004</span><span class="sxs-lookup"><span data-stu-id="822dd-561">CC004</span></span></td>
<td><span data-ttu-id="822dd-562">Balení</span><span class="sxs-lookup"><span data-stu-id="822dd-562">Packaging</span></span></td>
<td><span data-ttu-id="822dd-563">10</span><span class="sxs-lookup"><span data-stu-id="822dd-563">10</span></span></td>
<td><span data-ttu-id="822dd-564">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="822dd-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="822dd-565">124.57</span><span class="sxs-lookup"><span data-stu-id="822dd-565">124.57</span></span></td>
<td><span data-ttu-id="822dd-566">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="822dd-567">V následující tabulce je uveden výsledek při použití Finančních služeb Finance jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="822dd-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="822dd-568">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-568">Cost object</span></span></th>
<th><span data-ttu-id="822dd-569">Hodnota</span><span class="sxs-lookup"><span data-stu-id="822dd-569">Magnitude</span></span></th>
<th><span data-ttu-id="822dd-570">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="822dd-570">Allocation factor</span></span></th>
<th><span data-ttu-id="822dd-571">Částka</span><span class="sxs-lookup"><span data-stu-id="822dd-571">Amount</span></span></th>
<th><span data-ttu-id="822dd-572">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="822dd-573">CC003</span><span class="sxs-lookup"><span data-stu-id="822dd-573">CC003</span></span></td>
<td><span data-ttu-id="822dd-574">Sestavení</span><span class="sxs-lookup"><span data-stu-id="822dd-574">Assembly</span></span></td>
<td><span data-ttu-id="822dd-575">65</span><span class="sxs-lookup"><span data-stu-id="822dd-575">65</span></span></td>
<td><span data-ttu-id="822dd-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="822dd-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="822dd-577">438.75</span><span class="sxs-lookup"><span data-stu-id="822dd-577">438.75</span></span></td>
<td><span data-ttu-id="822dd-578">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-579">CC004</span><span class="sxs-lookup"><span data-stu-id="822dd-579">CC004</span></span></td>
<td><span data-ttu-id="822dd-580">Balení</span><span class="sxs-lookup"><span data-stu-id="822dd-580">Packaging</span></span></td>
<td><span data-ttu-id="822dd-581">35</span><span class="sxs-lookup"><span data-stu-id="822dd-581">35</span></span></td>
<td><span data-ttu-id="822dd-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="822dd-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="822dd-583">236.25</span><span class="sxs-lookup"><span data-stu-id="822dd-583">236.25</span></span></td>
<td><span data-ttu-id="822dd-584">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-585">CC003</span><span class="sxs-lookup"><span data-stu-id="822dd-585">CC003</span></span></td>
<td><span data-ttu-id="822dd-586">Sestavení</span><span class="sxs-lookup"><span data-stu-id="822dd-586">Assembly</span></span></td>
<td><span data-ttu-id="822dd-587">65</span><span class="sxs-lookup"><span data-stu-id="822dd-587">65</span></span></td>
<td><span data-ttu-id="822dd-588">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="822dd-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="822dd-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="822dd-589">5,297.69</span></span></td>
<td><span data-ttu-id="822dd-590">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-591">CC004</span><span class="sxs-lookup"><span data-stu-id="822dd-591">CC004</span></span></td>
<td><span data-ttu-id="822dd-592">Balení</span><span class="sxs-lookup"><span data-stu-id="822dd-592">Packaging</span></span></td>
<td><span data-ttu-id="822dd-593">35</span><span class="sxs-lookup"><span data-stu-id="822dd-593">35</span></span></td>
<td><span data-ttu-id="822dd-594">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="822dd-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="822dd-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="822dd-595">2,852.60</span></span></td>
<td><span data-ttu-id="822dd-596">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="822dd-597">V následující tabulce je uveden výsledek při použití Služeb sestavení jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="822dd-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="822dd-598">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-598">Cost object</span></span></th>
<th><span data-ttu-id="822dd-599">Hodnota</span><span class="sxs-lookup"><span data-stu-id="822dd-599">Magnitude</span></span></th>
<th><span data-ttu-id="822dd-600">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="822dd-600">Allocation factor</span></span></th>
<th><span data-ttu-id="822dd-601">Částka</span><span class="sxs-lookup"><span data-stu-id="822dd-601">Amount</span></span></th>
<th><span data-ttu-id="822dd-602">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="822dd-603">Prod 1</span><span class="sxs-lookup"><span data-stu-id="822dd-603">Prod 1</span></span></td>
<td><span data-ttu-id="822dd-604">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="822dd-604">Product 1</span></span></td>
<td><span data-ttu-id="822dd-605">60</span><span class="sxs-lookup"><span data-stu-id="822dd-605">60</span></span></td>
<td><span data-ttu-id="822dd-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="822dd-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="822dd-607">535.31</span><span class="sxs-lookup"><span data-stu-id="822dd-607">535.31</span></span></td>
<td><span data-ttu-id="822dd-608">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-609">Prod 2</span><span class="sxs-lookup"><span data-stu-id="822dd-609">Prod 2</span></span></td>
<td><span data-ttu-id="822dd-610">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="822dd-610">Product 2</span></span></td>
<td><span data-ttu-id="822dd-611">20</span><span class="sxs-lookup"><span data-stu-id="822dd-611">20</span></span></td>
<td><span data-ttu-id="822dd-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="822dd-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="822dd-613">178.44</span><span class="sxs-lookup"><span data-stu-id="822dd-613">178.44</span></span></td>
<td><span data-ttu-id="822dd-614">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-615">Prod 1</span><span class="sxs-lookup"><span data-stu-id="822dd-615">Prod 1</span></span></td>
<td><span data-ttu-id="822dd-616">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="822dd-616">Product 1</span></span></td>
<td><span data-ttu-id="822dd-617">60</span><span class="sxs-lookup"><span data-stu-id="822dd-617">60</span></span></td>
<td><span data-ttu-id="822dd-618">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="822dd-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="822dd-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="822dd-619">4,487.12</span></span></td>
<td><span data-ttu-id="822dd-620">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-621">Prod 2</span><span class="sxs-lookup"><span data-stu-id="822dd-621">Prod 2</span></span></td>
<td><span data-ttu-id="822dd-622">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="822dd-622">Product 2</span></span></td>
<td><span data-ttu-id="822dd-623">20</span><span class="sxs-lookup"><span data-stu-id="822dd-623">20</span></span></td>
<td><span data-ttu-id="822dd-624">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="822dd-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="822dd-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="822dd-625">1,495.71</span></span></td>
<td><span data-ttu-id="822dd-626">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="822dd-627">V následující tabulce je uveden výsledek při použití Služeb balení jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="822dd-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="822dd-628">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-628">Cost object</span></span></th>
<th><span data-ttu-id="822dd-629">Hodnota</span><span class="sxs-lookup"><span data-stu-id="822dd-629">Magnitude</span></span></th>
<th><span data-ttu-id="822dd-630">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="822dd-630">Allocation factor</span></span></th>
<th><span data-ttu-id="822dd-631">Částka</span><span class="sxs-lookup"><span data-stu-id="822dd-631">Amount</span></span></th>
<th><span data-ttu-id="822dd-632">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="822dd-633">Prod 1</span><span class="sxs-lookup"><span data-stu-id="822dd-633">Prod 1</span></span></td>
<td><span data-ttu-id="822dd-634">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="822dd-634">Product 1</span></span></td>
<td><span data-ttu-id="822dd-635">80</span><span class="sxs-lookup"><span data-stu-id="822dd-635">80</span></span></td>
<td><span data-ttu-id="822dd-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="822dd-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="822dd-637">241.05</span><span class="sxs-lookup"><span data-stu-id="822dd-637">241.05</span></span></td>
<td><span data-ttu-id="822dd-638">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-639">Prod 2</span><span class="sxs-lookup"><span data-stu-id="822dd-639">Prod 2</span></span></td>
<td><span data-ttu-id="822dd-640">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="822dd-640">Product 2</span></span></td>
<td><span data-ttu-id="822dd-641">15</span><span class="sxs-lookup"><span data-stu-id="822dd-641">15</span></span></td>
<td><span data-ttu-id="822dd-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="822dd-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="822dd-643">45.20</span><span class="sxs-lookup"><span data-stu-id="822dd-643">45.20</span></span></td>
<td><span data-ttu-id="822dd-644">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-645">Prod 1</span><span class="sxs-lookup"><span data-stu-id="822dd-645">Prod 1</span></span></td>
<td><span data-ttu-id="822dd-646">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="822dd-646">Product 1</span></span></td>
<td><span data-ttu-id="822dd-647">80</span><span class="sxs-lookup"><span data-stu-id="822dd-647">80</span></span></td>
<td><span data-ttu-id="822dd-648">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="822dd-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="822dd-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="822dd-649">2,507.09</span></span></td>
<td><span data-ttu-id="822dd-650">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-651">Prod 2</span><span class="sxs-lookup"><span data-stu-id="822dd-651">Prod 2</span></span></td>
<td><span data-ttu-id="822dd-652">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="822dd-652">Product 2</span></span></td>
<td><span data-ttu-id="822dd-653">15</span><span class="sxs-lookup"><span data-stu-id="822dd-653">15</span></span></td>
<td><span data-ttu-id="822dd-654">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="822dd-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="822dd-655">470.08</span><span class="sxs-lookup"><span data-stu-id="822dd-655">470.08</span></span></td>
<td><span data-ttu-id="822dd-656">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="822dd-657">Položky deníku (položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="822dd-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="822dd-658">Deník</span><span class="sxs-lookup"><span data-stu-id="822dd-658">Journal</span></span></th>
<th><span data-ttu-id="822dd-659">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="822dd-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="822dd-660">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="822dd-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="822dd-661">Verze</span><span class="sxs-lookup"><span data-stu-id="822dd-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="822dd-662">00004</span><span class="sxs-lookup"><span data-stu-id="822dd-662">00004</span></span></td>
<td><span data-ttu-id="822dd-663">Deník přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="822dd-664">Fiskální</span><span class="sxs-lookup"><span data-stu-id="822dd-664">Fiscal</span></span></td>
<td><span data-ttu-id="822dd-665">2017</span><span class="sxs-lookup"><span data-stu-id="822dd-665">2017</span></span></td>
<td><span data-ttu-id="822dd-666">Období 1</span><span class="sxs-lookup"><span data-stu-id="822dd-666">Period 1</span></span></td>
<td><span data-ttu-id="822dd-667">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="822dd-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="822dd-668">Řádky deníku</span><span class="sxs-lookup"><span data-stu-id="822dd-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="822dd-669">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="822dd-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="822dd-670">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="822dd-671">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-671">Cost element</span></span></th>
<th><span data-ttu-id="822dd-672">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-672">Cost behavior</span></span></th>
<th><span data-ttu-id="822dd-673">Částka</span><span class="sxs-lookup"><span data-stu-id="822dd-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="822dd-674">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="822dd-675">CC001</span><span class="sxs-lookup"><span data-stu-id="822dd-675">CC001</span></span></td>
<td><span data-ttu-id="822dd-676">HR</span><span class="sxs-lookup"><span data-stu-id="822dd-676">HR</span></span></td>
<td><span data-ttu-id="822dd-677">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-677">10001</span></span></td>
<td><span data-ttu-id="822dd-678">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-678">Electricity</span></span></td>
<td><span data-ttu-id="822dd-679">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-679">Fixed cost</span></span></td>
<td><span data-ttu-id="822dd-680">500.00</span><span class="sxs-lookup"><span data-stu-id="822dd-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-681">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="822dd-682">CC001</span><span class="sxs-lookup"><span data-stu-id="822dd-682">CC001</span></span></td>
<td><span data-ttu-id="822dd-683">HR</span><span class="sxs-lookup"><span data-stu-id="822dd-683">HR</span></span></td>
<td><span data-ttu-id="822dd-684">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-684">10001</span></span></td>
<td><span data-ttu-id="822dd-685">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-685">Electricity</span></span></td>
<td><span data-ttu-id="822dd-686">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-686">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="822dd-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-688">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="822dd-689">CC002</span><span class="sxs-lookup"><span data-stu-id="822dd-689">CC002</span></span></td>
<td><span data-ttu-id="822dd-690">Finance</span><span class="sxs-lookup"><span data-stu-id="822dd-690">Finance</span></span></td>
<td><span data-ttu-id="822dd-691">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-691">10001</span></span></td>
<td><span data-ttu-id="822dd-692">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-692">Electricity</span></span></td>
<td><span data-ttu-id="822dd-693">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-693">Fixed cost</span></span></td>
<td><span data-ttu-id="822dd-694">675.00</span><span class="sxs-lookup"><span data-stu-id="822dd-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-695">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="822dd-696">CC002</span><span class="sxs-lookup"><span data-stu-id="822dd-696">CC002</span></span></td>
<td><span data-ttu-id="822dd-697">Finance</span><span class="sxs-lookup"><span data-stu-id="822dd-697">Finance</span></span></td>
<td><span data-ttu-id="822dd-698">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-698">10001</span></span></td>
<td><span data-ttu-id="822dd-699">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-699">Electricity</span></span></td>
<td><span data-ttu-id="822dd-700">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-700">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="822dd-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-702">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="822dd-703">CC003</span><span class="sxs-lookup"><span data-stu-id="822dd-703">CC003</span></span></td>
<td><span data-ttu-id="822dd-704">Sestavení</span><span class="sxs-lookup"><span data-stu-id="822dd-704">Assembly</span></span></td>
<td><span data-ttu-id="822dd-705">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-705">10001</span></span></td>
<td><span data-ttu-id="822dd-706">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-706">Electricity</span></span></td>
<td><span data-ttu-id="822dd-707">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-707">Fixed cost</span></span></td>
<td><span data-ttu-id="822dd-708">713.75</span><span class="sxs-lookup"><span data-stu-id="822dd-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-709">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="822dd-710">CC003</span><span class="sxs-lookup"><span data-stu-id="822dd-710">CC003</span></span></td>
<td><span data-ttu-id="822dd-711">Sestavení</span><span class="sxs-lookup"><span data-stu-id="822dd-711">Assembly</span></span></td>
<td><span data-ttu-id="822dd-712">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-712">10001</span></span></td>
<td><span data-ttu-id="822dd-713">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-713">Electricity</span></span></td>
<td><span data-ttu-id="822dd-714">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-714">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="822dd-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-716">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="822dd-717">CC003</span><span class="sxs-lookup"><span data-stu-id="822dd-717">CC003</span></span></td>
<td><span data-ttu-id="822dd-718">Balení</span><span class="sxs-lookup"><span data-stu-id="822dd-718">Packaging</span></span></td>
<td><span data-ttu-id="822dd-719">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-719">10001</span></span></td>
<td><span data-ttu-id="822dd-720">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-720">Electricity</span></span></td>
<td><span data-ttu-id="822dd-721">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-721">Fixed cost</span></span></td>
<td><span data-ttu-id="822dd-722">286.25</span><span class="sxs-lookup"><span data-stu-id="822dd-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-723">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="822dd-724">CC003</span><span class="sxs-lookup"><span data-stu-id="822dd-724">CC003</span></span></td>
<td><span data-ttu-id="822dd-725">Balení</span><span class="sxs-lookup"><span data-stu-id="822dd-725">Packaging</span></span></td>
<td><span data-ttu-id="822dd-726">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-726">10001</span></span></td>
<td><span data-ttu-id="822dd-727">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-727">Electricity</span></span></td>
<td><span data-ttu-id="822dd-728">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-728">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="822dd-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-730">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="822dd-731">Prod 1</span><span class="sxs-lookup"><span data-stu-id="822dd-731">Prod 1</span></span></td>
<td><span data-ttu-id="822dd-732">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="822dd-732">Product 1</span></span></td>
<td><span data-ttu-id="822dd-733">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-733">10001</span></span></td>
<td><span data-ttu-id="822dd-734">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-734">Electricity</span></span></td>
<td><span data-ttu-id="822dd-735">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-735">Fixed cost</span></span></td>
<td><span data-ttu-id="822dd-736">776.36</span><span class="sxs-lookup"><span data-stu-id="822dd-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-737">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="822dd-738">Prod 1</span><span class="sxs-lookup"><span data-stu-id="822dd-738">Prod 1</span></span></td>
<td><span data-ttu-id="822dd-739">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="822dd-739">Product 1</span></span></td>
<td><span data-ttu-id="822dd-740">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-740">10001</span></span></td>
<td><span data-ttu-id="822dd-741">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-741">Electricity</span></span></td>
<td><span data-ttu-id="822dd-742">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-742">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="822dd-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-744">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="822dd-745">Prod 2</span><span class="sxs-lookup"><span data-stu-id="822dd-745">Prod 2</span></span></td>
<td><span data-ttu-id="822dd-746">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="822dd-746">Product 1</span></span></td>
<td><span data-ttu-id="822dd-747">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-747">10001</span></span></td>
<td><span data-ttu-id="822dd-748">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-748">Electricity</span></span></td>
<td><span data-ttu-id="822dd-749">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-749">Fixed cost</span></span></td>
<td><span data-ttu-id="822dd-750">223.64</span><span class="sxs-lookup"><span data-stu-id="822dd-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-751">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="822dd-752">Prod 2</span><span class="sxs-lookup"><span data-stu-id="822dd-752">Prod 2</span></span></td>
<td><span data-ttu-id="822dd-753">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="822dd-753">Product 1</span></span></td>
<td><span data-ttu-id="822dd-754">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-754">10001</span></span></td>
<td><span data-ttu-id="822dd-755">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-755">Electricity</span></span></td>
<td><span data-ttu-id="822dd-756">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-756">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="822dd-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="822dd-758">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="822dd-759">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="822dd-760">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-760">Cost element</span></span></th>
<th><span data-ttu-id="822dd-761">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-761">Cost behavior</span></span></th>
<th><span data-ttu-id="822dd-762">Částka</span><span class="sxs-lookup"><span data-stu-id="822dd-762">Amount</span></span></th>
<th><span data-ttu-id="822dd-763">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="822dd-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="822dd-764">CC001</span><span class="sxs-lookup"><span data-stu-id="822dd-764">CC001</span></span></td>
<td><span data-ttu-id="822dd-765">HR</span><span class="sxs-lookup"><span data-stu-id="822dd-765">HR</span></span></td>
<td><span data-ttu-id="822dd-766">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-766">10001</span></span></td>
<td><span data-ttu-id="822dd-767">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-767">Electricity</span></span></td>
<td><span data-ttu-id="822dd-768">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-768">Fixed cost</span></span></td>
<td><span data-ttu-id="822dd-769">-500,00</span><span class="sxs-lookup"><span data-stu-id="822dd-769">-500.00</span></span></td>
<td><span data-ttu-id="822dd-770">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-771">CC002</span><span class="sxs-lookup"><span data-stu-id="822dd-771">CC002</span></span></td>
<td><span data-ttu-id="822dd-772">Finance</span><span class="sxs-lookup"><span data-stu-id="822dd-772">Finance</span></span></td>
<td><span data-ttu-id="822dd-773">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-773">10001</span></span></td>
<td><span data-ttu-id="822dd-774">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-774">Electricity</span></span></td>
<td><span data-ttu-id="822dd-775">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-775">Fixed cost</span></span></td>
<td><span data-ttu-id="822dd-776">175.00</span><span class="sxs-lookup"><span data-stu-id="822dd-776">175.00</span></span></td>
<td><span data-ttu-id="822dd-777">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-778">CC003</span><span class="sxs-lookup"><span data-stu-id="822dd-778">CC003</span></span></td>
<td><span data-ttu-id="822dd-779">Sestavení</span><span class="sxs-lookup"><span data-stu-id="822dd-779">Assembly</span></span></td>
<td><span data-ttu-id="822dd-780">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-780">10001</span></span></td>
<td><span data-ttu-id="822dd-781">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-781">Electricity</span></span></td>
<td><span data-ttu-id="822dd-782">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-782">Fixed cost</span></span></td>
<td><span data-ttu-id="822dd-783">275.00</span><span class="sxs-lookup"><span data-stu-id="822dd-783">275.00</span></span></td>
<td><span data-ttu-id="822dd-784">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-785">CC004</span><span class="sxs-lookup"><span data-stu-id="822dd-785">CC004</span></span></td>
<td><span data-ttu-id="822dd-786">Balení</span><span class="sxs-lookup"><span data-stu-id="822dd-786">Packaging</span></span></td>
<td><span data-ttu-id="822dd-787">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-787">10001</span></span></td>
<td><span data-ttu-id="822dd-788">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-788">Electricity</span></span></td>
<td><span data-ttu-id="822dd-789">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-789">Fixed cost</span></span></td>
<td><span data-ttu-id="822dd-790">50,00</span><span class="sxs-lookup"><span data-stu-id="822dd-790">50,00</span></span></td>
<td><span data-ttu-id="822dd-791">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-792">CC001</span><span class="sxs-lookup"><span data-stu-id="822dd-792">CC001</span></span></td>
<td><span data-ttu-id="822dd-793">HR</span><span class="sxs-lookup"><span data-stu-id="822dd-793">HR</span></span></td>
<td><span data-ttu-id="822dd-794">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-794">10001</span></span></td>
<td><span data-ttu-id="822dd-795">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-795">Electricity</span></span></td>
<td><span data-ttu-id="822dd-796">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-796">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-797">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="822dd-797">-1,245.71</span></span></td>
<td><span data-ttu-id="822dd-798">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-799">CC002</span><span class="sxs-lookup"><span data-stu-id="822dd-799">CC002</span></span></td>
<td><span data-ttu-id="822dd-800">Finance</span><span class="sxs-lookup"><span data-stu-id="822dd-800">Finance</span></span></td>
<td><span data-ttu-id="822dd-801">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-801">10001</span></span></td>
<td><span data-ttu-id="822dd-802">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-802">Electricity</span></span></td>
<td><span data-ttu-id="822dd-803">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-803">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-804">436.00</span><span class="sxs-lookup"><span data-stu-id="822dd-804">436.00</span></span></td>
<td><span data-ttu-id="822dd-805">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-806">CC003</span><span class="sxs-lookup"><span data-stu-id="822dd-806">CC003</span></span></td>
<td><span data-ttu-id="822dd-807">Sestavení</span><span class="sxs-lookup"><span data-stu-id="822dd-807">Assembly</span></span></td>
<td><span data-ttu-id="822dd-808">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-808">10001</span></span></td>
<td><span data-ttu-id="822dd-809">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-809">Electricity</span></span></td>
<td><span data-ttu-id="822dd-810">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-810">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-811">685.14</span><span class="sxs-lookup"><span data-stu-id="822dd-811">685.14</span></span></td>
<td><span data-ttu-id="822dd-812">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-813">CC004</span><span class="sxs-lookup"><span data-stu-id="822dd-813">CC004</span></span></td>
<td><span data-ttu-id="822dd-814">Balení</span><span class="sxs-lookup"><span data-stu-id="822dd-814">Packaging</span></span></td>
<td><span data-ttu-id="822dd-815">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-815">10001</span></span></td>
<td><span data-ttu-id="822dd-816">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-816">Electricity</span></span></td>
<td><span data-ttu-id="822dd-817">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-817">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-818">124.57</span><span class="sxs-lookup"><span data-stu-id="822dd-818">124.57</span></span></td>
<td><span data-ttu-id="822dd-819">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-820">CC002</span><span class="sxs-lookup"><span data-stu-id="822dd-820">CC002</span></span></td>
<td><span data-ttu-id="822dd-821">Finance</span><span class="sxs-lookup"><span data-stu-id="822dd-821">Finance</span></span></td>
<td><span data-ttu-id="822dd-822">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-822">10001</span></span></td>
<td><span data-ttu-id="822dd-823">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-823">Electricity</span></span></td>
<td><span data-ttu-id="822dd-824">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-824">Fixed cost</span></span></td>
<td><span data-ttu-id="822dd-825">-675,00</span><span class="sxs-lookup"><span data-stu-id="822dd-825">-675.00</span></span></td>
<td><span data-ttu-id="822dd-826">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-827">CC003</span><span class="sxs-lookup"><span data-stu-id="822dd-827">CC003</span></span></td>
<td><span data-ttu-id="822dd-828">Sestavení</span><span class="sxs-lookup"><span data-stu-id="822dd-828">Assembly</span></span></td>
<td><span data-ttu-id="822dd-829">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-829">10001</span></span></td>
<td><span data-ttu-id="822dd-830">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-830">Electricity</span></span></td>
<td><span data-ttu-id="822dd-831">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-831">Fixed cost</span></span></td>
<td><span data-ttu-id="822dd-832">438.75</span><span class="sxs-lookup"><span data-stu-id="822dd-832">438.75</span></span></td>
<td><span data-ttu-id="822dd-833">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-834">CC004</span><span class="sxs-lookup"><span data-stu-id="822dd-834">CC004</span></span></td>
<td><span data-ttu-id="822dd-835">Balení</span><span class="sxs-lookup"><span data-stu-id="822dd-835">Packaging</span></span></td>
<td><span data-ttu-id="822dd-836">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-836">10001</span></span></td>
<td><span data-ttu-id="822dd-837">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-837">Electricity</span></span></td>
<td><span data-ttu-id="822dd-838">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-838">Fixed cost</span></span></td>
<td><span data-ttu-id="822dd-839">236.25</span><span class="sxs-lookup"><span data-stu-id="822dd-839">236.25</span></span></td>
<td><span data-ttu-id="822dd-840">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-841">CC002</span><span class="sxs-lookup"><span data-stu-id="822dd-841">CC002</span></span></td>
<td><span data-ttu-id="822dd-842">Finance</span><span class="sxs-lookup"><span data-stu-id="822dd-842">Finance</span></span></td>
<td><span data-ttu-id="822dd-843">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-843">10001</span></span></td>
<td><span data-ttu-id="822dd-844">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-844">Electricity</span></span></td>
<td><span data-ttu-id="822dd-845">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-845">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-846">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="822dd-846">-8,150.29</span></span></td>
<td><span data-ttu-id="822dd-847">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-848">CC003</span><span class="sxs-lookup"><span data-stu-id="822dd-848">CC003</span></span></td>
<td><span data-ttu-id="822dd-849">Sestavení</span><span class="sxs-lookup"><span data-stu-id="822dd-849">Assembly</span></span></td>
<td><span data-ttu-id="822dd-850">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-850">10001</span></span></td>
<td><span data-ttu-id="822dd-851">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-851">Electricity</span></span></td>
<td><span data-ttu-id="822dd-852">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-852">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="822dd-853">5,297.69</span></span></td>
<td><span data-ttu-id="822dd-854">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-855">CC004</span><span class="sxs-lookup"><span data-stu-id="822dd-855">CC004</span></span></td>
<td><span data-ttu-id="822dd-856">Balení</span><span class="sxs-lookup"><span data-stu-id="822dd-856">Packaging</span></span></td>
<td><span data-ttu-id="822dd-857">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-857">10001</span></span></td>
<td><span data-ttu-id="822dd-858">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-858">Electricity</span></span></td>
<td><span data-ttu-id="822dd-859">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-859">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="822dd-860">2,852.60</span></span></td>
<td><span data-ttu-id="822dd-861">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-862">CC003</span><span class="sxs-lookup"><span data-stu-id="822dd-862">CC003</span></span></td>
<td><span data-ttu-id="822dd-863">Sestavení</span><span class="sxs-lookup"><span data-stu-id="822dd-863">Assembly</span></span></td>
<td><span data-ttu-id="822dd-864">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-864">10001</span></span></td>
<td><span data-ttu-id="822dd-865">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-865">Electricity</span></span></td>
<td><span data-ttu-id="822dd-866">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-866">Fixed cost</span></span></td>
<td><span data-ttu-id="822dd-867">-713,75</span><span class="sxs-lookup"><span data-stu-id="822dd-867">-713.75</span></span></td>
<td><span data-ttu-id="822dd-868">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-869">Prod 1</span><span class="sxs-lookup"><span data-stu-id="822dd-869">Prod 1</span></span></td>
<td><span data-ttu-id="822dd-870">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="822dd-870">Product 1</span></span></td>
<td><span data-ttu-id="822dd-871">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-871">10001</span></span></td>
<td><span data-ttu-id="822dd-872">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-872">Electricity</span></span></td>
<td><span data-ttu-id="822dd-873">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-873">Fixed cost</span></span></td>
<td><span data-ttu-id="822dd-874">535.31</span><span class="sxs-lookup"><span data-stu-id="822dd-874">535.31</span></span></td>
<td><span data-ttu-id="822dd-875">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-876">Prod 2</span><span class="sxs-lookup"><span data-stu-id="822dd-876">Prod 2</span></span></td>
<td><span data-ttu-id="822dd-877">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="822dd-877">Product 2</span></span></td>
<td><span data-ttu-id="822dd-878">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-878">10001</span></span></td>
<td><span data-ttu-id="822dd-879">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-879">Electricity</span></span></td>
<td><span data-ttu-id="822dd-880">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-880">Fixed cost</span></span></td>
<td><span data-ttu-id="822dd-881">178.44</span><span class="sxs-lookup"><span data-stu-id="822dd-881">178.44</span></span></td>
<td><span data-ttu-id="822dd-882">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-883">CC003</span><span class="sxs-lookup"><span data-stu-id="822dd-883">CC003</span></span></td>
<td><span data-ttu-id="822dd-884">Sestavení</span><span class="sxs-lookup"><span data-stu-id="822dd-884">Assembly</span></span></td>
<td><span data-ttu-id="822dd-885">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-885">10001</span></span></td>
<td><span data-ttu-id="822dd-886">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-886">Electricity</span></span></td>
<td><span data-ttu-id="822dd-887">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-887">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-888">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="822dd-888">-5,982.83</span></span></td>
<td><span data-ttu-id="822dd-889">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-890">Prod 1</span><span class="sxs-lookup"><span data-stu-id="822dd-890">Prod 1</span></span></td>
<td><span data-ttu-id="822dd-891">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="822dd-891">Product 1</span></span></td>
<td><span data-ttu-id="822dd-892">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-892">10001</span></span></td>
<td><span data-ttu-id="822dd-893">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-893">Electricity</span></span></td>
<td><span data-ttu-id="822dd-894">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-894">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="822dd-895">4,487.12</span></span></td>
<td><span data-ttu-id="822dd-896">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-897">Prod 2</span><span class="sxs-lookup"><span data-stu-id="822dd-897">Prod 2</span></span></td>
<td><span data-ttu-id="822dd-898">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="822dd-898">Product 2</span></span></td>
<td><span data-ttu-id="822dd-899">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-899">10001</span></span></td>
<td><span data-ttu-id="822dd-900">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-900">Electricity</span></span></td>
<td><span data-ttu-id="822dd-901">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-901">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="822dd-902">1,495.71</span></span></td>
<td><span data-ttu-id="822dd-903">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-904">CC003</span><span class="sxs-lookup"><span data-stu-id="822dd-904">CC003</span></span></td>
<td><span data-ttu-id="822dd-905">Sestavení</span><span class="sxs-lookup"><span data-stu-id="822dd-905">Assembly</span></span></td>
<td><span data-ttu-id="822dd-906">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-906">10001</span></span></td>
<td><span data-ttu-id="822dd-907">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-907">Electricity</span></span></td>
<td><span data-ttu-id="822dd-908">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-908">Fixed cost</span></span></td>
<td><span data-ttu-id="822dd-909">-286,25</span><span class="sxs-lookup"><span data-stu-id="822dd-909">-286.25</span></span></td>
<td><span data-ttu-id="822dd-910">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-911">Prod 1</span><span class="sxs-lookup"><span data-stu-id="822dd-911">Prod 1</span></span></td>
<td><span data-ttu-id="822dd-912">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="822dd-912">Product 1</span></span></td>
<td><span data-ttu-id="822dd-913">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-913">10001</span></span></td>
<td><span data-ttu-id="822dd-914">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-914">Electricity</span></span></td>
<td><span data-ttu-id="822dd-915">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-915">Fixed cost</span></span></td>
<td><span data-ttu-id="822dd-916">241.05</span><span class="sxs-lookup"><span data-stu-id="822dd-916">241.05</span></span></td>
<td><span data-ttu-id="822dd-917">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-918">Prod 2</span><span class="sxs-lookup"><span data-stu-id="822dd-918">Prod 2</span></span></td>
<td><span data-ttu-id="822dd-919">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="822dd-919">Product 2</span></span></td>
<td><span data-ttu-id="822dd-920">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-920">10001</span></span></td>
<td><span data-ttu-id="822dd-921">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-921">Electricity</span></span></td>
<td><span data-ttu-id="822dd-922">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-922">Fixed cost</span></span></td>
<td><span data-ttu-id="822dd-923">45.20</span><span class="sxs-lookup"><span data-stu-id="822dd-923">45.20</span></span></td>
<td><span data-ttu-id="822dd-924">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-925">CC003</span><span class="sxs-lookup"><span data-stu-id="822dd-925">CC003</span></span></td>
<td><span data-ttu-id="822dd-926">Sestavení</span><span class="sxs-lookup"><span data-stu-id="822dd-926">Assembly</span></span></td>
<td><span data-ttu-id="822dd-927">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-927">10001</span></span></td>
<td><span data-ttu-id="822dd-928">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-928">Electricity</span></span></td>
<td><span data-ttu-id="822dd-929">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-929">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-930">-2977,17</span><span class="sxs-lookup"><span data-stu-id="822dd-930">-2,977.17</span></span></td>
<td><span data-ttu-id="822dd-931">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-932">Prod 1</span><span class="sxs-lookup"><span data-stu-id="822dd-932">Prod 1</span></span></td>
<td><span data-ttu-id="822dd-933">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="822dd-933">Product 1</span></span></td>
<td><span data-ttu-id="822dd-934">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-934">10001</span></span></td>
<td><span data-ttu-id="822dd-935">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-935">Electricity</span></span></td>
<td><span data-ttu-id="822dd-936">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-936">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="822dd-937">2,507.09</span></span></td>
<td><span data-ttu-id="822dd-938">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="822dd-939">Prod 2</span><span class="sxs-lookup"><span data-stu-id="822dd-939">Prod 2</span></span></td>
<td><span data-ttu-id="822dd-940">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="822dd-940">Product 2</span></span></td>
<td><span data-ttu-id="822dd-941">10001</span><span class="sxs-lookup"><span data-stu-id="822dd-941">10001</span></span></td>
<td><span data-ttu-id="822dd-942">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="822dd-942">Electricity</span></span></td>
<td><span data-ttu-id="822dd-943">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-943">Variable cost</span></span></td>
<td><span data-ttu-id="822dd-944">470.08</span><span class="sxs-lookup"><span data-stu-id="822dd-944">470.08</span></span></td>
<td><span data-ttu-id="822dd-945">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="822dd-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="822dd-946">Závěr</span><span class="sxs-lookup"><span data-stu-id="822dd-946">Conclusion</span></span>
<span data-ttu-id="822dd-947">Ve finančním účtování se náklady za elektřinu ve výši 10 000 zaúčtují na ID fiktivního nákladového střediska.</span><span class="sxs-lookup"><span data-stu-id="822dd-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="822dd-948">Účetní tak budou vědět, že tento náklad musí být přidělen.</span><span class="sxs-lookup"><span data-stu-id="822dd-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="822dd-949">V nákladovém účetnictví náklady procházejí napříč organizačními jednotkami a úrovněmi, na základě použitých zásad a pravidel.</span><span class="sxs-lookup"><span data-stu-id="822dd-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="822dd-950">Každý náklad byl přidružen k základu přidělení, který poskytuje nejlepší hodnocení pro přidělení nákladů.</span><span class="sxs-lookup"><span data-stu-id="822dd-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="822dd-951">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="822dd-952">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="822dd-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="822dd-953">Celkem</span><span class="sxs-lookup"><span data-stu-id="822dd-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="822dd-954">CC099</span><span class="sxs-lookup"><span data-stu-id="822dd-954">CC099</span></span></th>
<th><span data-ttu-id="822dd-955">CC001</span><span class="sxs-lookup"><span data-stu-id="822dd-955">CC001</span></span></th>
<th><span data-ttu-id="822dd-956">CC002</span><span class="sxs-lookup"><span data-stu-id="822dd-956">CC002</span></span></th>
<th><span data-ttu-id="822dd-957">CC003</span><span class="sxs-lookup"><span data-stu-id="822dd-957">CC003</span></span></th>
<th><span data-ttu-id="822dd-958">CC004</span><span class="sxs-lookup"><span data-stu-id="822dd-958">CC004</span></span></th>
<th><span data-ttu-id="822dd-959">Proj 1</span><span class="sxs-lookup"><span data-stu-id="822dd-959">Proj 1</span></span></th>
<th><span data-ttu-id="822dd-960">Proj 2</span><span class="sxs-lookup"><span data-stu-id="822dd-960">Proj 2</span></span></th>
<th><span data-ttu-id="822dd-961">Prod 1</span><span class="sxs-lookup"><span data-stu-id="822dd-961">Prod 1</span></span></th>
<th><span data-ttu-id="822dd-962">Prod 2</span><span class="sxs-lookup"><span data-stu-id="822dd-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="822dd-963">10001 Elektřina</span><span class="sxs-lookup"><span data-stu-id="822dd-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="822dd-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="822dd-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="822dd-965"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="822dd-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="822dd-966"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="822dd-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="822dd-967"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="822dd-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="822dd-968"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="822dd-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="822dd-969"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="822dd-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="822dd-970"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="822dd-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="822dd-971"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="822dd-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="822dd-972"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="822dd-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="822dd-973">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="822dd-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="822dd-974">0,00</span><span class="sxs-lookup"><span data-stu-id="822dd-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="822dd-975">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="822dd-976">0,00</span><span class="sxs-lookup"><span data-stu-id="822dd-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="822dd-977">0,00</span><span class="sxs-lookup"><span data-stu-id="822dd-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="822dd-978">0,00</span><span class="sxs-lookup"><span data-stu-id="822dd-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="822dd-979">0,00</span><span class="sxs-lookup"><span data-stu-id="822dd-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="822dd-980">0,00</span><span class="sxs-lookup"><span data-stu-id="822dd-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="822dd-981">776.36</span><span class="sxs-lookup"><span data-stu-id="822dd-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="822dd-982">223.64</span><span class="sxs-lookup"><span data-stu-id="822dd-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="822dd-983"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="822dd-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="822dd-984">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="822dd-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="822dd-985">000</span><span class="sxs-lookup"><span data-stu-id="822dd-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="822dd-986">0,00</span><span class="sxs-lookup"><span data-stu-id="822dd-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="822dd-987">0,00</span><span class="sxs-lookup"><span data-stu-id="822dd-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="822dd-988">0,00</span><span class="sxs-lookup"><span data-stu-id="822dd-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="822dd-989">0,00</span><span class="sxs-lookup"><span data-stu-id="822dd-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="822dd-990">30.00</span><span class="sxs-lookup"><span data-stu-id="822dd-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="822dd-991">10,00</span><span class="sxs-lookup"><span data-stu-id="822dd-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="822dd-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="822dd-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="822dd-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="822dd-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="822dd-994"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="822dd-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="822dd-995">Toto téma popisuje, jak primární prvek nákladů, 10001 Elektřina, prochází přes objekty nákladů.</span><span class="sxs-lookup"><span data-stu-id="822dd-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="822dd-996">Tyto režijní náklady tedy budou přiděleny na nejnižší úroveň v organizaci.</span><span class="sxs-lookup"><span data-stu-id="822dd-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="822dd-997">Jinak řečeno, objekty nákladů na nejnižší úrovni ponesou náklady.</span><span class="sxs-lookup"><span data-stu-id="822dd-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="822dd-998">Chcete-li vizuální tok nákladů mezi objekty nákladů, můžete použít pravidla zásad shrnutí nákladů pro vizualizaci jejich toků.</span><span class="sxs-lookup"><span data-stu-id="822dd-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="822dd-999">Podrobnější informace naleznete v tématu Zásady shrnutí nákladů.</span><span class="sxs-lookup"><span data-stu-id="822dd-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="822dd-1000">(Všimněte si, že toto téma ještě není dokončené, ale bud k dispozici již brzy.)</span><span class="sxs-lookup"><span data-stu-id="822dd-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




