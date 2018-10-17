---
title: "Výpočet režijních nákladů"
description: "Toto téma popisuje typické procesy pro výpočet a přidělení režijních nákladů."
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
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
ms.sourcegitcommit: 12ae99c15bafcd9cc08b30903fe3f251f446b17d
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.contentlocale: cs-cz
ms.lasthandoff: 10/05/2018

---

# <a name="overhead-calculation"></a><span data-ttu-id="b867f-103">Výpočet režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b867f-104">Toto téma popisuje typické procesy pro výpočet a přidělení režijních nákladů.</span><span class="sxs-lookup"><span data-stu-id="b867f-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="b867f-105">Definice termínu</span><span class="sxs-lookup"><span data-stu-id="b867f-105">Term definition</span></span>
---------------

<span data-ttu-id="b867f-106">Režijní náklady jsou náklady, které nutně vznikají při chodu podnikání, ale nelze je připsat přímo k žádné konkrétní podnikatelské aktivitě, produktu nebo službě.</span><span class="sxs-lookup"><span data-stu-id="b867f-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="b867f-107">Režijní náklady poskytují důležitou podporu pro generování aktivity přinášejících zisk.</span><span class="sxs-lookup"><span data-stu-id="b867f-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="b867f-108">Následuje několik příkladů režijních nákladů:</span><span class="sxs-lookup"><span data-stu-id="b867f-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="b867f-109">Renta</span><span class="sxs-lookup"><span data-stu-id="b867f-109">Rent</span></span>
-   <span data-ttu-id="b867f-110">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-110">Electricity</span></span>
-   <span data-ttu-id="b867f-111">Administrativní mzdy</span><span class="sxs-lookup"><span data-stu-id="b867f-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="b867f-112">Přehled výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-112">Overhead calculation overview</span></span>
<span data-ttu-id="b867f-113">Výpočet režijních nákladů spustí zásady účtování nákladů ve správném pořadí.</span><span class="sxs-lookup"><span data-stu-id="b867f-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="b867f-114">Výpočet režijních nákladů můžete pro stejné fiskální období spustit mnohokrát, pokud došlo ke změně zásad účtování nákladů nebo zjištění konkrétních chyb.</span><span class="sxs-lookup"><span data-stu-id="b867f-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="b867f-115">Každé spuštění výpočtu režijních nákladů se ukládá a přijímá ID jedinečné verze, které vám umožní porovnávat výpočty v různých verzích.</span><span class="sxs-lookup"><span data-stu-id="b867f-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="b867f-116">Položky nákladů, které generuje výpočet režijních nákladů, přijímá datum účtování.</span><span class="sxs-lookup"><span data-stu-id="b867f-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="b867f-117">Toto datum účtován se shoduje s konvovým datem fiskálního období, které se použije ve výpočtu.</span><span class="sxs-lookup"><span data-stu-id="b867f-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="b867f-118">ID jedinečné verze se skládá z následujících prvků:</span><span class="sxs-lookup"><span data-stu-id="b867f-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="b867f-119">Typ verze</span><span class="sxs-lookup"><span data-stu-id="b867f-119">Version type</span></span>
-   <span data-ttu-id="b867f-120">Datum a čas</span><span class="sxs-lookup"><span data-stu-id="b867f-120">Date and time</span></span>
-   <span data-ttu-id="b867f-121">Hlavní kniha nákladového účetnictví</span><span class="sxs-lookup"><span data-stu-id="b867f-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="b867f-122">Fiskální rok</span><span class="sxs-lookup"><span data-stu-id="b867f-122">Fiscal year</span></span>
-   <span data-ttu-id="b867f-123">Fiskální období</span><span class="sxs-lookup"><span data-stu-id="b867f-123">Fiscal period</span></span>

<span data-ttu-id="b867f-124">Výpočet režijních nákladů se spustí bez ohledu na verzi.</span><span class="sxs-lookup"><span data-stu-id="b867f-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="b867f-125">Proto lze vypočítat rozpočtovou verzi před skutečnou verzí.</span><span class="sxs-lookup"><span data-stu-id="b867f-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="b867f-126">Výpočet režijních nákladů se skládá ze čtyř kroků uvedených na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="b867f-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="b867f-127">V každé fázi je vytvořeno záhlaví deníku, které obsahuje položky deníku.</span><span class="sxs-lookup"><span data-stu-id="b867f-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="b867f-128">Toto záhlaví deníku zachovává vstupní data pro každý krok výpočtu.</span><span class="sxs-lookup"><span data-stu-id="b867f-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="b867f-129">Zásady a pravidla se použijí na každý řádek deníku a položky nákladů jsou generovány jako výstup.</span><span class="sxs-lookup"><span data-stu-id="b867f-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="b867f-130">Máte tedy vždy plnou sledovatelnost.</span><span class="sxs-lookup"><span data-stu-id="b867f-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="b867f-131">[![Výpočet režijních nákladů](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="b867f-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="b867f-132">Výpočet a přidělení režijních nákladů za elektřinu</span><span class="sxs-lookup"><span data-stu-id="b867f-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="b867f-133">Ve finančním účetnictví se některé náklady, jako je například elektřina, registrují jako paušální.</span><span class="sxs-lookup"><span data-stu-id="b867f-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="b867f-134">Podrobný přehled pro vedoucí není tedy pro nákladové účetnictví k dispozici.</span><span class="sxs-lookup"><span data-stu-id="b867f-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="b867f-135">V nákladovém účetnictví musí náklady procházet organizačními jednotkami, aby byl získán správný přehled pro vedoucí napříč všemi jednotkami a úrovněmi organizace.</span><span class="sxs-lookup"><span data-stu-id="b867f-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="b867f-136">Tento tok musí být založen buď na přesném záznamu spotřeby nebo na objektivním hodnocení.</span><span class="sxs-lookup"><span data-stu-id="b867f-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="b867f-137">V hlavní knize mohou být zaúčtovány náklady na elektřinu způsobem znázorněným v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="b867f-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b867f-138">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="b867f-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b867f-139">Nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="b867f-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="b867f-140">Hlavní účet</span><span class="sxs-lookup"><span data-stu-id="b867f-140">Main account</span></span></th>
<th><span data-ttu-id="b867f-141">Částka v zúčtovací měně</span><span class="sxs-lookup"><span data-stu-id="b867f-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b867f-142">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="b867f-143">CC099</span><span class="sxs-lookup"><span data-stu-id="b867f-143">CC099</span></span></td>
<td><span data-ttu-id="b867f-144">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="b867f-144">Default cost center</span></span></td>
<td><span data-ttu-id="b867f-145">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-145">10001</span></span></td>
<td><span data-ttu-id="b867f-146">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-146">Electricity</span></span></td>
<td><span data-ttu-id="b867f-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="b867f-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="b867f-148">Krok 1: Zpracování výpočtu chování nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="b867f-149">Ve výchozím nastavení dostanou při importu položek nákladů z datového zdroje tyto položky v nákladovém účetnictví klasifikaci **Neklasifikované**.</span><span class="sxs-lookup"><span data-stu-id="b867f-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="b867f-150">Použitím pravidla zásad chování nákladů lze reklasifikovat položky nákladů jako **Pevné náklady** nebo **Variabilní náklady**.</span><span class="sxs-lookup"><span data-stu-id="b867f-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="b867f-151">Definice pravidel chování nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-151">Define the cost behavior rule</span></span>

<span data-ttu-id="b867f-152">V některých případech je část nákladů s pevným poplatkem a zbývající náklady jsou založeny na spotřebě.</span><span class="sxs-lookup"><span data-stu-id="b867f-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="b867f-153">Účty za elektřinu často odpovídají této definici.</span><span class="sxs-lookup"><span data-stu-id="b867f-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="b867f-154">Po platbě konkrétního pevného poplatku platíte spotřebu za kilowatthodinu (kWh).</span><span class="sxs-lookup"><span data-stu-id="b867f-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="b867f-155">Pokud je například poplatek pevných nákladů 1 000,00, definuje se pravidlo chování nákladů takto:</span><span class="sxs-lookup"><span data-stu-id="b867f-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="b867f-156">Pevná částka 1 000,00</span><span class="sxs-lookup"><span data-stu-id="b867f-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="b867f-157">0 &lt;= 1 000,00 = Pevná</span><span class="sxs-lookup"><span data-stu-id="b867f-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="b867f-158">1 000,01 &lt; N = Variabilní</span><span class="sxs-lookup"><span data-stu-id="b867f-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="b867f-159">Deník</span><span class="sxs-lookup"><span data-stu-id="b867f-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b867f-160">Deník</span><span class="sxs-lookup"><span data-stu-id="b867f-160">Journal</span></span></th>
<th><span data-ttu-id="b867f-161">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="b867f-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b867f-162">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="b867f-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b867f-163">Verze</span><span class="sxs-lookup"><span data-stu-id="b867f-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b867f-164">00001</span><span class="sxs-lookup"><span data-stu-id="b867f-164">00001</span></span></td>
<td><span data-ttu-id="b867f-165">Deník výpočtu chování nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="b867f-166">Fiskální</span><span class="sxs-lookup"><span data-stu-id="b867f-166">Fiscal</span></span></td>
<td><span data-ttu-id="b867f-167">2017</span><span class="sxs-lookup"><span data-stu-id="b867f-167">2017</span></span></td>
<td><span data-ttu-id="b867f-168">Období 1</span><span class="sxs-lookup"><span data-stu-id="b867f-168">Period 1</span></span></td>
<td><span data-ttu-id="b867f-169">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="b867f-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="b867f-170">Položky deníku (Položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="b867f-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b867f-171">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="b867f-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b867f-172">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b867f-173">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-173">Cost element</span></span></th>
<th><span data-ttu-id="b867f-174">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-174">Cost behavior</span></span></th>
<th><span data-ttu-id="b867f-175">Částka</span><span class="sxs-lookup"><span data-stu-id="b867f-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b867f-176">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="b867f-177">CC099</span><span class="sxs-lookup"><span data-stu-id="b867f-177">CC099</span></span></td>
<td><span data-ttu-id="b867f-178">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="b867f-178">Default cost center</span></span></td>
<td><span data-ttu-id="b867f-179">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-179">10001</span></span></td>
<td><span data-ttu-id="b867f-180">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-180">Electricity</span></span></td>
<td><span data-ttu-id="b867f-181">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="b867f-181">Unclassified</span></span></td>
<td><span data-ttu-id="b867f-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="b867f-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b867f-183">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b867f-184">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b867f-185">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-185">Cost element</span></span></th>
<th><span data-ttu-id="b867f-186">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-186">Cost behavior</span></span></th>
<th><span data-ttu-id="b867f-187">Částka</span><span class="sxs-lookup"><span data-stu-id="b867f-187">Amount</span></span></th>
<th><span data-ttu-id="b867f-188">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="b867f-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b867f-189">CC099</span><span class="sxs-lookup"><span data-stu-id="b867f-189">CC099</span></span></td>
<td><span data-ttu-id="b867f-190">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="b867f-190">Default cost center</span></span></td>
<td><span data-ttu-id="b867f-191">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-191">10001</span></span></td>
<td><span data-ttu-id="b867f-192">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-192">Electricity</span></span></td>
<td><span data-ttu-id="b867f-193">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="b867f-193">Unclassified</span></span></td>
<td><span data-ttu-id="b867f-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="b867f-194">10,000.00</span></span></td>
<td><span data-ttu-id="b867f-195">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-196">CC099</span><span class="sxs-lookup"><span data-stu-id="b867f-196">CC099</span></span></td>
<td><span data-ttu-id="b867f-197">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="b867f-197">Default cost center</span></span></td>
<td><span data-ttu-id="b867f-198">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-198">10001</span></span></td>
<td><span data-ttu-id="b867f-199">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-199">Electricity</span></span></td>
<td><span data-ttu-id="b867f-200">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="b867f-200">Unclassified</span></span></td>
<td><span data-ttu-id="b867f-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="b867f-201">-10,000.00</span></span></td>
<td><span data-ttu-id="b867f-202">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-203">CC099</span><span class="sxs-lookup"><span data-stu-id="b867f-203">CC099</span></span></td>
<td><span data-ttu-id="b867f-204">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="b867f-204">Default cost center</span></span></td>
<td><span data-ttu-id="b867f-205">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-205">10001</span></span></td>
<td><span data-ttu-id="b867f-206">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-206">Electricity</span></span></td>
<td><span data-ttu-id="b867f-207">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-207">Fixed cost</span></span></td>
<td><span data-ttu-id="b867f-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="b867f-208">1,000.00</span></span></td>
<td><span data-ttu-id="b867f-209">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-210">CC099</span><span class="sxs-lookup"><span data-stu-id="b867f-210">CC099</span></span></td>
<td><span data-ttu-id="b867f-211">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="b867f-211">Default cost center</span></span></td>
<td><span data-ttu-id="b867f-212">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-212">10001</span></span></td>
<td><span data-ttu-id="b867f-213">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-213">Electricity</span></span></td>
<td><span data-ttu-id="b867f-214">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-214">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="b867f-215">9,000.00</span></span></td>
<td><span data-ttu-id="b867f-216">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b867f-217">Více informací naleznete v tématu [Vytvoření a přiřazení zásad chování nákladů k jednotce řízení nákladů](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="b867f-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="b867f-218">Krok 2: Zpracování výpočtu distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="b867f-219">Distribuce nákladů se používá k rozdělení nákladů z jednoho objektu nákladů na jeden nebo více dalších objektů nákladů použitím příslušného základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="b867f-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="b867f-220">Distribuce nákladů a přidělení nákladů se liší v tom, že k distribuci nákladů dochází vždy na úrovni primárního prvku nákladů původních nákladů.</span><span class="sxs-lookup"><span data-stu-id="b867f-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="b867f-221">Definice pravidel distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-221">Define the cost distribution rule</span></span>

<span data-ttu-id="b867f-222">Ve finančním účetnictví se náklady na elektřinu často registrují jako paušální.</span><span class="sxs-lookup"><span data-stu-id="b867f-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="b867f-223">V nákladovém účetnictví není tento přístup dostatečně podrobný.</span><span class="sxs-lookup"><span data-stu-id="b867f-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="b867f-224">Variabilní náklady by měly být distribuovány k jednotlivým objektům nákladů na solidním základě.</span><span class="sxs-lookup"><span data-stu-id="b867f-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="b867f-225">Nejlogičtější základ přidělení je spotřeba elektřiny (kWh).</span><span class="sxs-lookup"><span data-stu-id="b867f-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="b867f-226">Vytvoří se člen statistické dimenzi s názvem Elektřina a zaznamená se elektrické spotřeba.</span><span class="sxs-lookup"><span data-stu-id="b867f-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="b867f-227">Ve výchozím nastavení se všechny členy statistické dimenze stanou dostupnými zpřístupněny jako základy přidělení.</span><span class="sxs-lookup"><span data-stu-id="b867f-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b867f-228">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-228">Cost object</span></span></th>
<th><span data-ttu-id="b867f-229">kWh</span><span class="sxs-lookup"><span data-stu-id="b867f-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b867f-230">CC001</span><span class="sxs-lookup"><span data-stu-id="b867f-230">CC001</span></span></td>
<td><span data-ttu-id="b867f-231">HR</span><span class="sxs-lookup"><span data-stu-id="b867f-231">HR</span></span></td>
<td><span data-ttu-id="b867f-232">1 000</span><span class="sxs-lookup"><span data-stu-id="b867f-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-233">CC002</span><span class="sxs-lookup"><span data-stu-id="b867f-233">CC002</span></span></td>
<td><span data-ttu-id="b867f-234">Finance</span><span class="sxs-lookup"><span data-stu-id="b867f-234">Finance</span></span></td>
<td><span data-ttu-id="b867f-235">6,000</span><span class="sxs-lookup"><span data-stu-id="b867f-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-236">CC003</span><span class="sxs-lookup"><span data-stu-id="b867f-236">CC003</span></span></td>
<td><span data-ttu-id="b867f-237">Sestavení</span><span class="sxs-lookup"><span data-stu-id="b867f-237">Assembly</span></span></td>
<td><span data-ttu-id="b867f-238">0</span><span class="sxs-lookup"><span data-stu-id="b867f-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b867f-239">Následující tabulka zobrazuje výsledek při použití elektrické spotřeby jako základu přidělení pro variabilní náklady.</span><span class="sxs-lookup"><span data-stu-id="b867f-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b867f-240">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-240">Cost object</span></span></th>
<th><span data-ttu-id="b867f-241">Hodnota</span><span class="sxs-lookup"><span data-stu-id="b867f-241">Magnitude</span></span></th>
<th><span data-ttu-id="b867f-242">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="b867f-242">Allocation factor</span></span></th>
<th><span data-ttu-id="b867f-243">Částka</span><span class="sxs-lookup"><span data-stu-id="b867f-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b867f-244">CC001</span><span class="sxs-lookup"><span data-stu-id="b867f-244">CC001</span></span></td>
<td><span data-ttu-id="b867f-245">HR</span><span class="sxs-lookup"><span data-stu-id="b867f-245">HR</span></span></td>
<td><span data-ttu-id="b867f-246">1 000</span><span class="sxs-lookup"><span data-stu-id="b867f-246">1,000</span></span></td>
<td><span data-ttu-id="b867f-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="b867f-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="b867f-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="b867f-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-249">CC002</span><span class="sxs-lookup"><span data-stu-id="b867f-249">CC002</span></span></td>
<td><span data-ttu-id="b867f-250">Finance</span><span class="sxs-lookup"><span data-stu-id="b867f-250">Finance</span></span></td>
<td><span data-ttu-id="b867f-251">6,000</span><span class="sxs-lookup"><span data-stu-id="b867f-251">6,000</span></span></td>
<td><span data-ttu-id="b867f-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="b867f-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="b867f-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="b867f-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-254">CC003</span><span class="sxs-lookup"><span data-stu-id="b867f-254">CC003</span></span></td>
<td><span data-ttu-id="b867f-255">Sestavení</span><span class="sxs-lookup"><span data-stu-id="b867f-255">Assembly</span></span></td>
<td><span data-ttu-id="b867f-256">0</span><span class="sxs-lookup"><span data-stu-id="b867f-256">0</span></span></td>
<td><span data-ttu-id="b867f-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="b867f-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="b867f-258">0,00</span><span class="sxs-lookup"><span data-stu-id="b867f-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b867f-259">Pevné náklady musí být distribuovány rovnoměrně k jednotlivých objektům nákladů, které spotřebovávaly elektřinu.</span><span class="sxs-lookup"><span data-stu-id="b867f-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="b867f-260">Tohoto výsledku můžete dosáhnout pomocí členu statistické dimenze Elektřina v základu přidělení vzorce: (Elektřina &gt; 0,00) Následující tabulka zobrazuje výsledek při použití elektrické spotřeby jako základu přidělení pro variabilní náklady.</span><span class="sxs-lookup"><span data-stu-id="b867f-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b867f-261">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-261">Cost object</span></span></th>
<th><span data-ttu-id="b867f-262">Vzorec</span><span class="sxs-lookup"><span data-stu-id="b867f-262">Formula</span></span></th>
<th><span data-ttu-id="b867f-263">Hodnota</span><span class="sxs-lookup"><span data-stu-id="b867f-263">Magnitude</span></span></th>
<th><span data-ttu-id="b867f-264">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="b867f-264">Allocation factor</span></span></th>
<th><span data-ttu-id="b867f-265">Částka</span><span class="sxs-lookup"><span data-stu-id="b867f-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b867f-266">CC001</span><span class="sxs-lookup"><span data-stu-id="b867f-266">CC001</span></span></td>
<td><span data-ttu-id="b867f-267">HR</span><span class="sxs-lookup"><span data-stu-id="b867f-267">HR</span></span></td>
<td><span data-ttu-id="b867f-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="b867f-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="b867f-269">1</span><span class="sxs-lookup"><span data-stu-id="b867f-269">1</span></span></td>
<td><span data-ttu-id="b867f-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="b867f-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="b867f-271">500.00</span><span class="sxs-lookup"><span data-stu-id="b867f-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-272">CC002</span><span class="sxs-lookup"><span data-stu-id="b867f-272">CC002</span></span></td>
<td><span data-ttu-id="b867f-273">Finance</span><span class="sxs-lookup"><span data-stu-id="b867f-273">Finance</span></span></td>
<td><span data-ttu-id="b867f-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="b867f-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="b867f-275">1</span><span class="sxs-lookup"><span data-stu-id="b867f-275">1</span></span></td>
<td><span data-ttu-id="b867f-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="b867f-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="b867f-277">500.00</span><span class="sxs-lookup"><span data-stu-id="b867f-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-278">CC003</span><span class="sxs-lookup"><span data-stu-id="b867f-278">CC003</span></span></td>
<td><span data-ttu-id="b867f-279">Sestavení</span><span class="sxs-lookup"><span data-stu-id="b867f-279">Assembly</span></span></td>
<td><span data-ttu-id="b867f-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="b867f-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="b867f-281">0</span><span class="sxs-lookup"><span data-stu-id="b867f-281">0</span></span></td>
<td><span data-ttu-id="b867f-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="b867f-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="b867f-283">0,00</span><span class="sxs-lookup"><span data-stu-id="b867f-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="b867f-284">Deník</span><span class="sxs-lookup"><span data-stu-id="b867f-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b867f-285">Deník</span><span class="sxs-lookup"><span data-stu-id="b867f-285">Journal</span></span></th>
<th><span data-ttu-id="b867f-286">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="b867f-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b867f-287">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="b867f-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b867f-288">Verze</span><span class="sxs-lookup"><span data-stu-id="b867f-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b867f-289">00002</span><span class="sxs-lookup"><span data-stu-id="b867f-289">00002</span></span></td>
<td><span data-ttu-id="b867f-290">Deník výpočtu distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="b867f-291">Fiskální</span><span class="sxs-lookup"><span data-stu-id="b867f-291">Fiscal</span></span></td>
<td><span data-ttu-id="b867f-292">2017</span><span class="sxs-lookup"><span data-stu-id="b867f-292">2017</span></span></td>
<td><span data-ttu-id="b867f-293">Období 1</span><span class="sxs-lookup"><span data-stu-id="b867f-293">Period 1</span></span></td>
<td><span data-ttu-id="b867f-294">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="b867f-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="b867f-295">Položky deníku (Položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="b867f-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b867f-296">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="b867f-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b867f-297">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b867f-298">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-298">Cost element</span></span></th>
<th><span data-ttu-id="b867f-299">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-299">Cost behavior</span></span></th>
<th><span data-ttu-id="b867f-300">Částka</span><span class="sxs-lookup"><span data-stu-id="b867f-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b867f-301">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="b867f-302">CC099</span><span class="sxs-lookup"><span data-stu-id="b867f-302">CC099</span></span></td>
<td><span data-ttu-id="b867f-303">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="b867f-303">Default cost center</span></span></td>
<td><span data-ttu-id="b867f-304">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-304">10001</span></span></td>
<td><span data-ttu-id="b867f-305">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-305">Electricity</span></span></td>
<td><span data-ttu-id="b867f-306">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-306">Fixed cost</span></span></td>
<td><span data-ttu-id="b867f-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="b867f-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-308">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="b867f-309">CC099</span><span class="sxs-lookup"><span data-stu-id="b867f-309">CC099</span></span></td>
<td><span data-ttu-id="b867f-310">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="b867f-310">Default cost center</span></span></td>
<td><span data-ttu-id="b867f-311">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-311">10001</span></span></td>
<td><span data-ttu-id="b867f-312">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-312">Electricity</span></span></td>
<td><span data-ttu-id="b867f-313">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-313">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="b867f-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b867f-315">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b867f-316">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b867f-317">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-317">Cost element</span></span></th>
<th><span data-ttu-id="b867f-318">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-318">Cost behavior</span></span></th>
<th><span data-ttu-id="b867f-319">Částka</span><span class="sxs-lookup"><span data-stu-id="b867f-319">Amount</span></span></th>
<th><span data-ttu-id="b867f-320">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="b867f-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b867f-321">CC099</span><span class="sxs-lookup"><span data-stu-id="b867f-321">CC099</span></span></td>
<td><span data-ttu-id="b867f-322">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="b867f-322">Default cost center</span></span></td>
<td><span data-ttu-id="b867f-323">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-323">10001</span></span></td>
<td><span data-ttu-id="b867f-324">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-324">Electricity</span></span></td>
<td><span data-ttu-id="b867f-325">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-325">Fixed cost</span></span></td>
<td><span data-ttu-id="b867f-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="b867f-326">-1,000.00</span></span></td>
<td><span data-ttu-id="b867f-327">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-328">CC001</span><span class="sxs-lookup"><span data-stu-id="b867f-328">CC001</span></span></td>
<td><span data-ttu-id="b867f-329">HR</span><span class="sxs-lookup"><span data-stu-id="b867f-329">HR</span></span></td>
<td><span data-ttu-id="b867f-330">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-330">10001</span></span></td>
<td><span data-ttu-id="b867f-331">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-331">Electricity</span></span></td>
<td><span data-ttu-id="b867f-332">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-332">Fixed cost</span></span></td>
<td><span data-ttu-id="b867f-333">500.00</span><span class="sxs-lookup"><span data-stu-id="b867f-333">500.00</span></span></td>
<td><span data-ttu-id="b867f-334">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-335">CC002</span><span class="sxs-lookup"><span data-stu-id="b867f-335">CC002</span></span></td>
<td><span data-ttu-id="b867f-336">Finance</span><span class="sxs-lookup"><span data-stu-id="b867f-336">Finance</span></span></td>
<td><span data-ttu-id="b867f-337">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-337">10001</span></span></td>
<td><span data-ttu-id="b867f-338">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-338">Electricity</span></span></td>
<td><span data-ttu-id="b867f-339">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-339">Fixed cost</span></span></td>
<td><span data-ttu-id="b867f-340">500.00</span><span class="sxs-lookup"><span data-stu-id="b867f-340">500.00</span></span></td>
<td><span data-ttu-id="b867f-341">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-342">CC099</span><span class="sxs-lookup"><span data-stu-id="b867f-342">CC099</span></span></td>
<td><span data-ttu-id="b867f-343">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="b867f-343">Default cost center</span></span></td>
<td><span data-ttu-id="b867f-344">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-344">10001</span></span></td>
<td><span data-ttu-id="b867f-345">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-345">Electricity</span></span></td>
<td><span data-ttu-id="b867f-346">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-346">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-347">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="b867f-347">-9,000.00</span></span></td>
<td><span data-ttu-id="b867f-348">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-349">CC001</span><span class="sxs-lookup"><span data-stu-id="b867f-349">CC001</span></span></td>
<td><span data-ttu-id="b867f-350">HR</span><span class="sxs-lookup"><span data-stu-id="b867f-350">HR</span></span></td>
<td><span data-ttu-id="b867f-351">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-351">10001</span></span></td>
<td><span data-ttu-id="b867f-352">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-352">Electricity</span></span></td>
<td><span data-ttu-id="b867f-353">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-353">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="b867f-354">1,285.71</span></span></td>
<td><span data-ttu-id="b867f-355">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-356">CC002</span><span class="sxs-lookup"><span data-stu-id="b867f-356">CC002</span></span></td>
<td><span data-ttu-id="b867f-357">Finance</span><span class="sxs-lookup"><span data-stu-id="b867f-357">Finance</span></span></td>
<td><span data-ttu-id="b867f-358">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-358">10001</span></span></td>
<td><span data-ttu-id="b867f-359">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-359">Electricity</span></span></td>
<td><span data-ttu-id="b867f-360">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-360">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="b867f-361">7,714.29</span></span></td>
<td><span data-ttu-id="b867f-362">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b867f-363">Více informací naleznete v tématu [Vytvoření a přiřazení zásad distribuce nákladů k jednotce řízení nákladů](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="b867f-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="b867f-364">Krok 3: Zpracování výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="b867f-365">Režijní náklady se používají k účtování jednoho nebo více konkrétních objektů nákladů.</span><span class="sxs-lookup"><span data-stu-id="b867f-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="b867f-366">Účtování je založeno na předem určené nákladové sazbě a množství z přiřazeného základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="b867f-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="b867f-367">Definice sazby režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-367">Define the overhead rate</span></span>

<span data-ttu-id="b867f-368">Objekt nákladů CC001 HR přispívá k sadě interních projektů.</span><span class="sxs-lookup"><span data-stu-id="b867f-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="b867f-369">Vytvoří se člen statistické dimenzi s názvem projekty lidských zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="b867f-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b867f-370">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-370">Cost object</span></span></th>
<th><span data-ttu-id="b867f-371">Pracovní doba</span><span class="sxs-lookup"><span data-stu-id="b867f-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b867f-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="b867f-372">Proj 1</span></span></td>
<td><span data-ttu-id="b867f-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="b867f-373">Project 1</span></span></td>
<td><span data-ttu-id="b867f-374">3</span><span class="sxs-lookup"><span data-stu-id="b867f-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="b867f-375">Proj 2</span></span></td>
<td><span data-ttu-id="b867f-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="b867f-376">Project 2</span></span></td>
<td><span data-ttu-id="b867f-377">1</span><span class="sxs-lookup"><span data-stu-id="b867f-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b867f-378">Byla definována předem určená nákladová sazba pro příspěvky k nákladovým projektům.</span><span class="sxs-lookup"><span data-stu-id="b867f-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b867f-379">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-379">Cost object</span></span></th>
<th><span data-ttu-id="b867f-380">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-380">Cost element</span></span></th>
<th><span data-ttu-id="b867f-381">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-381">Cost behavior</span></span></th>
<th><span data-ttu-id="b867f-382">Jednotky</span><span class="sxs-lookup"><span data-stu-id="b867f-382">Units</span></span></th>
<th><span data-ttu-id="b867f-383">Kurz</span><span class="sxs-lookup"><span data-stu-id="b867f-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b867f-384">CC001</span><span class="sxs-lookup"><span data-stu-id="b867f-384">CC001</span></span></td>
<td><span data-ttu-id="b867f-385">HR</span><span class="sxs-lookup"><span data-stu-id="b867f-385">HR</span></span></td>
<td><span data-ttu-id="b867f-386">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-386">10001</span></span></td>
<td><span data-ttu-id="b867f-387">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-387">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-388">1</span><span class="sxs-lookup"><span data-stu-id="b867f-388">1</span></span></td>
<td><span data-ttu-id="b867f-389">10</span><span class="sxs-lookup"><span data-stu-id="b867f-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b867f-390">Následující tabulka zobrazuje výsledek při použití projektů lidských zdrojů jako základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="b867f-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b867f-391">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-391">Cost object</span></span></th>
<th><span data-ttu-id="b867f-392">Hodnota</span><span class="sxs-lookup"><span data-stu-id="b867f-392">Magnitude</span></span></th>
<th><span data-ttu-id="b867f-393">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-393">Cost element</span></span></th>
<th><span data-ttu-id="b867f-394">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="b867f-394">Allocation factor</span></span></th>
<th><span data-ttu-id="b867f-395">Částka</span><span class="sxs-lookup"><span data-stu-id="b867f-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b867f-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="b867f-396">Proj 1</span></span></td>
<td><span data-ttu-id="b867f-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="b867f-397">Project 1</span></span></td>
<td><span data-ttu-id="b867f-398">3</span><span class="sxs-lookup"><span data-stu-id="b867f-398">3</span></span></td>
<td><span data-ttu-id="b867f-399">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-399">10001</span></span></td>
<td><span data-ttu-id="b867f-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="b867f-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="b867f-401">30.00</span><span class="sxs-lookup"><span data-stu-id="b867f-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="b867f-402">Proj 2</span></span></td>
<td><span data-ttu-id="b867f-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="b867f-403">Project 2</span></span></td>
<td><span data-ttu-id="b867f-404">1</span><span class="sxs-lookup"><span data-stu-id="b867f-404">1</span></span></td>
<td><span data-ttu-id="b867f-405">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-405">10001</span></span></td>
<td><span data-ttu-id="b867f-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="b867f-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="b867f-407">10,00</span><span class="sxs-lookup"><span data-stu-id="b867f-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="b867f-408">Deník</span><span class="sxs-lookup"><span data-stu-id="b867f-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b867f-409">Deník</span><span class="sxs-lookup"><span data-stu-id="b867f-409">Journal</span></span></th>
<th><span data-ttu-id="b867f-410">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="b867f-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b867f-411">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="b867f-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b867f-412">Verze</span><span class="sxs-lookup"><span data-stu-id="b867f-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b867f-413">00003</span><span class="sxs-lookup"><span data-stu-id="b867f-413">00003</span></span></td>
<td><span data-ttu-id="b867f-414">Deník výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="b867f-415">Fiskální</span><span class="sxs-lookup"><span data-stu-id="b867f-415">Fiscal</span></span></td>
<td><span data-ttu-id="b867f-416">2017</span><span class="sxs-lookup"><span data-stu-id="b867f-416">2017</span></span></td>
<td><span data-ttu-id="b867f-417">Období 1</span><span class="sxs-lookup"><span data-stu-id="b867f-417">Period 1</span></span></td>
<td><span data-ttu-id="b867f-418">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="b867f-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="b867f-419">Položky deníku (položky deníku pro výpočet sazby režijních nákladů)</span><span class="sxs-lookup"><span data-stu-id="b867f-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b867f-420">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="b867f-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b867f-421">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-421">Cost object</span></span></th>
<th><span data-ttu-id="b867f-422">Hodnota</span><span class="sxs-lookup"><span data-stu-id="b867f-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b867f-423">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="b867f-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="b867f-424">Proj 1</span></span></td>
<td><span data-ttu-id="b867f-425">Interní projekt 1</span><span class="sxs-lookup"><span data-stu-id="b867f-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="b867f-426">3,00</span><span class="sxs-lookup"><span data-stu-id="b867f-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-427">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="b867f-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="b867f-428">Proj 2</span></span></td>
<td><span data-ttu-id="b867f-429">Interní projekt 2</span><span class="sxs-lookup"><span data-stu-id="b867f-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="b867f-430">1.00</span><span class="sxs-lookup"><span data-stu-id="b867f-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b867f-431">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b867f-432">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b867f-433">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-433">Cost element</span></span></th>
<th><span data-ttu-id="b867f-434">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-434">Cost behavior</span></span></th>
<th><span data-ttu-id="b867f-435">Částka</span><span class="sxs-lookup"><span data-stu-id="b867f-435">Amount</span></span></th>
<th><span data-ttu-id="b867f-436">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="b867f-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b867f-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="b867f-437">CC0001</span></span></td>
<td><span data-ttu-id="b867f-438">HR</span><span class="sxs-lookup"><span data-stu-id="b867f-438">HR</span></span></td>
<td><span data-ttu-id="b867f-439">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-439">10001</span></span></td>
<td><span data-ttu-id="b867f-440">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-440">Electricity</span></span></td>
<td><span data-ttu-id="b867f-441">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-441">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="b867f-442">-30.00</span></span></td>
<td><span data-ttu-id="b867f-443">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="b867f-444">Proj 1</span></span></td>
<td><span data-ttu-id="b867f-445">Interní projekt 1</span><span class="sxs-lookup"><span data-stu-id="b867f-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="b867f-446">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-446">10001</span></span></td>
<td><span data-ttu-id="b867f-447">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-447">Electricity</span></span></td>
<td><span data-ttu-id="b867f-448">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-448">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-449">30.00</span><span class="sxs-lookup"><span data-stu-id="b867f-449">30.00</span></span></td>
<td><span data-ttu-id="b867f-450">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-451">CC001</span><span class="sxs-lookup"><span data-stu-id="b867f-451">CC001</span></span></td>
<td><span data-ttu-id="b867f-452">HR</span><span class="sxs-lookup"><span data-stu-id="b867f-452">HR</span></span></td>
<td><span data-ttu-id="b867f-453">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-453">10001</span></span></td>
<td><span data-ttu-id="b867f-454">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-454">Electricity</span></span></td>
<td><span data-ttu-id="b867f-455">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-455">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="b867f-456">-10.00</span></span></td>
<td><span data-ttu-id="b867f-457">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="b867f-458">Proj 2</span></span></td>
<td><span data-ttu-id="b867f-459">Interní projekt 2</span><span class="sxs-lookup"><span data-stu-id="b867f-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="b867f-460">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-460">10001</span></span></td>
<td><span data-ttu-id="b867f-461">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-461">Electricity</span></span></td>
<td><span data-ttu-id="b867f-462">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-462">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-463">10.00</span><span class="sxs-lookup"><span data-stu-id="b867f-463">10.00</span></span></td>
<td><span data-ttu-id="b867f-464">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b867f-465">Další informace naleznete v tématu [Provedení výpočtu režijních nákladů](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="b867f-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="b867f-466">Krok 4: Zpracování výpočtu přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="b867f-467">Přidělení se používá k přidělení zůstatku objektu nákladů do jiných objektů nákladů použitím základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="b867f-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="b867f-468">Aplikace Finance and Operations podporuje reciproční metodu přidělování.</span><span class="sxs-lookup"><span data-stu-id="b867f-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="b867f-469">V metodě vzájemného přidělení jsou plně rozpoznány vzájemné služby, které si vyměňují pomocné objekty nákladů.</span><span class="sxs-lookup"><span data-stu-id="b867f-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="b867f-470">Systém automaticky určí provádění přidělení ve správném pořadí.</span><span class="sxs-lookup"><span data-stu-id="b867f-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="b867f-471">Zůstatek objektu nákladů je přidělen jedním základem přidělení.</span><span class="sxs-lookup"><span data-stu-id="b867f-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="b867f-472">Je podporováno přidělování napříč dimenzemi objektů nákladů a jejich příslušných členů.</span><span class="sxs-lookup"><span data-stu-id="b867f-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="b867f-473">Pořadí přidělení je řízeno jednotkou řízení nákladů.</span><span class="sxs-lookup"><span data-stu-id="b867f-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="b867f-474">[![Reciproční metoda](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="b867f-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="b867f-475">Definice přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-475">Define the cost allocation</span></span>

<span data-ttu-id="b867f-476">Toto je jednoduchý příklad, který vysvětluje, jakým způsobem lze sledovat tok nákladů.</span><span class="sxs-lookup"><span data-stu-id="b867f-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="b867f-477">Objekt nákladů objektu CC001 HR přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="b867f-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="b867f-478">Vytvoří se člen statistické dimenzi s názvem služby lidských zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="b867f-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b867f-479">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-479">Cost object</span></span></th>
<th><span data-ttu-id="b867f-480">Služby HR</span><span class="sxs-lookup"><span data-stu-id="b867f-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b867f-481">CC002</span><span class="sxs-lookup"><span data-stu-id="b867f-481">CC002</span></span></td>
<td><span data-ttu-id="b867f-482">Finance</span><span class="sxs-lookup"><span data-stu-id="b867f-482">Finance</span></span></td>
<td><span data-ttu-id="b867f-483">35</span><span class="sxs-lookup"><span data-stu-id="b867f-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-484">CC003</span><span class="sxs-lookup"><span data-stu-id="b867f-484">CC003</span></span></td>
<td><span data-ttu-id="b867f-485">Sestavení</span><span class="sxs-lookup"><span data-stu-id="b867f-485">Assembly</span></span></td>
<td><span data-ttu-id="b867f-486">55</span><span class="sxs-lookup"><span data-stu-id="b867f-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-487">CC004</span><span class="sxs-lookup"><span data-stu-id="b867f-487">CC004</span></span></td>
<td><span data-ttu-id="b867f-488">Balení</span><span class="sxs-lookup"><span data-stu-id="b867f-488">Packaging</span></span></td>
<td><span data-ttu-id="b867f-489">10</span><span class="sxs-lookup"><span data-stu-id="b867f-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b867f-490">Objekt nákladů objektu CC002 Finance přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="b867f-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="b867f-491">Vytvoří se člen statistické dimenzi s názvem Finanční služby k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="b867f-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b867f-492">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-492">Cost object</span></span></th>
<th><span data-ttu-id="b867f-493">Finanční služby</span><span class="sxs-lookup"><span data-stu-id="b867f-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b867f-494">CC003</span><span class="sxs-lookup"><span data-stu-id="b867f-494">CC003</span></span></td>
<td><span data-ttu-id="b867f-495">Sestavení</span><span class="sxs-lookup"><span data-stu-id="b867f-495">Assembly</span></span></td>
<td><span data-ttu-id="b867f-496">65</span><span class="sxs-lookup"><span data-stu-id="b867f-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-497">CC004</span><span class="sxs-lookup"><span data-stu-id="b867f-497">CC004</span></span></td>
<td><span data-ttu-id="b867f-498">Balení</span><span class="sxs-lookup"><span data-stu-id="b867f-498">Packaging</span></span></td>
<td><span data-ttu-id="b867f-499">35</span><span class="sxs-lookup"><span data-stu-id="b867f-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b867f-500">Objekt nákladů objektu CC003 Sestavení přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="b867f-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="b867f-501">Vytvoří se člen statistické dimenzi s názvem Služby sestavení zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="b867f-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b867f-502">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-502">Cost object</span></span></th>
<th><span data-ttu-id="b867f-503">Služby sestavení (v hodinách)</span><span class="sxs-lookup"><span data-stu-id="b867f-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b867f-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b867f-504">Prod 1</span></span></td>
<td><span data-ttu-id="b867f-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="b867f-505">Product 1</span></span></td>
<td><span data-ttu-id="b867f-506">60</span><span class="sxs-lookup"><span data-stu-id="b867f-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b867f-507">Prod 2</span></span></td>
<td><span data-ttu-id="b867f-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="b867f-508">Product 2</span></span></td>
<td><span data-ttu-id="b867f-509">20</span><span class="sxs-lookup"><span data-stu-id="b867f-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b867f-510">Objekt nákladů objektu CC004 Balení přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="b867f-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="b867f-511">Vytvoří se člen statistické dimenzi s názvem Služby balení k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="b867f-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b867f-512">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-512">Cost object</span></span></th>
<th><span data-ttu-id="b867f-513">Služby balení (v hodinách)</span><span class="sxs-lookup"><span data-stu-id="b867f-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b867f-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b867f-514">Prod 1</span></span></td>
<td><span data-ttu-id="b867f-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="b867f-515">Product 1</span></span></td>
<td><span data-ttu-id="b867f-516">80</span><span class="sxs-lookup"><span data-stu-id="b867f-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b867f-517">Prod 2</span></span></td>
<td><span data-ttu-id="b867f-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="b867f-518">Product 2</span></span></td>
<td><span data-ttu-id="b867f-519">září</span><span class="sxs-lookup"><span data-stu-id="b867f-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="b867f-520">V aplikaci Finance and Operations lze odvodit statistická měření, jako je například výrobní doba spotřebovaná produktem, z datového zdroje.</span><span class="sxs-lookup"><span data-stu-id="b867f-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="b867f-521">Více informací naleznete v části [Šablona poskytovatele statistického měření](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="b867f-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="b867f-522">V následující tabulce je uveden výsledek při použití služeb HR jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="b867f-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b867f-523">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-523">Cost object</span></span></th>
<th><span data-ttu-id="b867f-524">Hodnota</span><span class="sxs-lookup"><span data-stu-id="b867f-524">Magnitude</span></span></th>
<th><span data-ttu-id="b867f-525">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="b867f-525">Allocation factor</span></span></th>
<th><span data-ttu-id="b867f-526">Částka</span><span class="sxs-lookup"><span data-stu-id="b867f-526">Amount</span></span></th>
<th><span data-ttu-id="b867f-527">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b867f-528">CC002</span><span class="sxs-lookup"><span data-stu-id="b867f-528">CC002</span></span></td>
<td><span data-ttu-id="b867f-529">Finance</span><span class="sxs-lookup"><span data-stu-id="b867f-529">Finance</span></span></td>
<td><span data-ttu-id="b867f-530">35</span><span class="sxs-lookup"><span data-stu-id="b867f-530">35</span></span></td>
<td><span data-ttu-id="b867f-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="b867f-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="b867f-532">175.00</span><span class="sxs-lookup"><span data-stu-id="b867f-532">175.00</span></span></td>
<td><span data-ttu-id="b867f-533">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-534">CC003</span><span class="sxs-lookup"><span data-stu-id="b867f-534">CC003</span></span></td>
<td><span data-ttu-id="b867f-535">Sestavení</span><span class="sxs-lookup"><span data-stu-id="b867f-535">Assembly</span></span></td>
<td><span data-ttu-id="b867f-536">55</span><span class="sxs-lookup"><span data-stu-id="b867f-536">55</span></span></td>
<td><span data-ttu-id="b867f-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="b867f-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="b867f-538">275.00</span><span class="sxs-lookup"><span data-stu-id="b867f-538">275.00</span></span></td>
<td><span data-ttu-id="b867f-539">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-540">CC004</span><span class="sxs-lookup"><span data-stu-id="b867f-540">CC004</span></span></td>
<td><span data-ttu-id="b867f-541">Balení</span><span class="sxs-lookup"><span data-stu-id="b867f-541">Packaging</span></span></td>
<td><span data-ttu-id="b867f-542">10</span><span class="sxs-lookup"><span data-stu-id="b867f-542">10</span></span></td>
<td><span data-ttu-id="b867f-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="b867f-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="b867f-544">50,00</span><span class="sxs-lookup"><span data-stu-id="b867f-544">50.00</span></span></td>
<td><span data-ttu-id="b867f-545">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-546">CC002</span><span class="sxs-lookup"><span data-stu-id="b867f-546">CC002</span></span></td>
<td><span data-ttu-id="b867f-547">Finance</span><span class="sxs-lookup"><span data-stu-id="b867f-547">Finance</span></span></td>
<td><span data-ttu-id="b867f-548">35</span><span class="sxs-lookup"><span data-stu-id="b867f-548">35</span></span></td>
<td><span data-ttu-id="b867f-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="b867f-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="b867f-550">436.00</span><span class="sxs-lookup"><span data-stu-id="b867f-550">436.00</span></span></td>
<td><span data-ttu-id="b867f-551">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-552">CC003</span><span class="sxs-lookup"><span data-stu-id="b867f-552">CC003</span></span></td>
<td><span data-ttu-id="b867f-553">Sestavení</span><span class="sxs-lookup"><span data-stu-id="b867f-553">Assembly</span></span></td>
<td><span data-ttu-id="b867f-554">55</span><span class="sxs-lookup"><span data-stu-id="b867f-554">55</span></span></td>
<td><span data-ttu-id="b867f-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="b867f-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="b867f-556">685.14</span><span class="sxs-lookup"><span data-stu-id="b867f-556">685.14</span></span></td>
<td><span data-ttu-id="b867f-557">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-558">CC004</span><span class="sxs-lookup"><span data-stu-id="b867f-558">CC004</span></span></td>
<td><span data-ttu-id="b867f-559">Balení</span><span class="sxs-lookup"><span data-stu-id="b867f-559">Packaging</span></span></td>
<td><span data-ttu-id="b867f-560">10</span><span class="sxs-lookup"><span data-stu-id="b867f-560">10</span></span></td>
<td><span data-ttu-id="b867f-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="b867f-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="b867f-562">124.57</span><span class="sxs-lookup"><span data-stu-id="b867f-562">124.57</span></span></td>
<td><span data-ttu-id="b867f-563">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b867f-564">V následující tabulce je uveden výsledek při použití Finančních služeb Finance jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="b867f-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b867f-565">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-565">Cost object</span></span></th>
<th><span data-ttu-id="b867f-566">Hodnota</span><span class="sxs-lookup"><span data-stu-id="b867f-566">Magnitude</span></span></th>
<th><span data-ttu-id="b867f-567">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="b867f-567">Allocation factor</span></span></th>
<th><span data-ttu-id="b867f-568">Částka</span><span class="sxs-lookup"><span data-stu-id="b867f-568">Amount</span></span></th>
<th><span data-ttu-id="b867f-569">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b867f-570">CC003</span><span class="sxs-lookup"><span data-stu-id="b867f-570">CC003</span></span></td>
<td><span data-ttu-id="b867f-571">Sestavení</span><span class="sxs-lookup"><span data-stu-id="b867f-571">Assembly</span></span></td>
<td><span data-ttu-id="b867f-572">65</span><span class="sxs-lookup"><span data-stu-id="b867f-572">65</span></span></td>
<td><span data-ttu-id="b867f-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="b867f-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="b867f-574">438.75</span><span class="sxs-lookup"><span data-stu-id="b867f-574">438.75</span></span></td>
<td><span data-ttu-id="b867f-575">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-576">CC004</span><span class="sxs-lookup"><span data-stu-id="b867f-576">CC004</span></span></td>
<td><span data-ttu-id="b867f-577">Balení</span><span class="sxs-lookup"><span data-stu-id="b867f-577">Packaging</span></span></td>
<td><span data-ttu-id="b867f-578">35</span><span class="sxs-lookup"><span data-stu-id="b867f-578">35</span></span></td>
<td><span data-ttu-id="b867f-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="b867f-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="b867f-580">236.25</span><span class="sxs-lookup"><span data-stu-id="b867f-580">236.25</span></span></td>
<td><span data-ttu-id="b867f-581">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-582">CC003</span><span class="sxs-lookup"><span data-stu-id="b867f-582">CC003</span></span></td>
<td><span data-ttu-id="b867f-583">Sestavení</span><span class="sxs-lookup"><span data-stu-id="b867f-583">Assembly</span></span></td>
<td><span data-ttu-id="b867f-584">65</span><span class="sxs-lookup"><span data-stu-id="b867f-584">65</span></span></td>
<td><span data-ttu-id="b867f-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="b867f-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="b867f-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="b867f-586">5,297.69</span></span></td>
<td><span data-ttu-id="b867f-587">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-588">CC004</span><span class="sxs-lookup"><span data-stu-id="b867f-588">CC004</span></span></td>
<td><span data-ttu-id="b867f-589">Balení</span><span class="sxs-lookup"><span data-stu-id="b867f-589">Packaging</span></span></td>
<td><span data-ttu-id="b867f-590">35</span><span class="sxs-lookup"><span data-stu-id="b867f-590">35</span></span></td>
<td><span data-ttu-id="b867f-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="b867f-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="b867f-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="b867f-592">2,852.60</span></span></td>
<td><span data-ttu-id="b867f-593">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b867f-594">V následující tabulce je uveden výsledek při použití Služeb sestavení jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="b867f-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b867f-595">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-595">Cost object</span></span></th>
<th><span data-ttu-id="b867f-596">Hodnota</span><span class="sxs-lookup"><span data-stu-id="b867f-596">Magnitude</span></span></th>
<th><span data-ttu-id="b867f-597">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="b867f-597">Allocation factor</span></span></th>
<th><span data-ttu-id="b867f-598">Částka</span><span class="sxs-lookup"><span data-stu-id="b867f-598">Amount</span></span></th>
<th><span data-ttu-id="b867f-599">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b867f-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b867f-600">Prod 1</span></span></td>
<td><span data-ttu-id="b867f-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="b867f-601">Product 1</span></span></td>
<td><span data-ttu-id="b867f-602">60</span><span class="sxs-lookup"><span data-stu-id="b867f-602">60</span></span></td>
<td><span data-ttu-id="b867f-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="b867f-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="b867f-604">535.31</span><span class="sxs-lookup"><span data-stu-id="b867f-604">535.31</span></span></td>
<td><span data-ttu-id="b867f-605">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b867f-606">Prod 2</span></span></td>
<td><span data-ttu-id="b867f-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="b867f-607">Product 2</span></span></td>
<td><span data-ttu-id="b867f-608">20</span><span class="sxs-lookup"><span data-stu-id="b867f-608">20</span></span></td>
<td><span data-ttu-id="b867f-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="b867f-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="b867f-610">178.44</span><span class="sxs-lookup"><span data-stu-id="b867f-610">178.44</span></span></td>
<td><span data-ttu-id="b867f-611">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b867f-612">Prod 1</span></span></td>
<td><span data-ttu-id="b867f-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="b867f-613">Product 1</span></span></td>
<td><span data-ttu-id="b867f-614">60</span><span class="sxs-lookup"><span data-stu-id="b867f-614">60</span></span></td>
<td><span data-ttu-id="b867f-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="b867f-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="b867f-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="b867f-616">4,487.12</span></span></td>
<td><span data-ttu-id="b867f-617">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b867f-618">Prod 2</span></span></td>
<td><span data-ttu-id="b867f-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="b867f-619">Product 2</span></span></td>
<td><span data-ttu-id="b867f-620">20</span><span class="sxs-lookup"><span data-stu-id="b867f-620">20</span></span></td>
<td><span data-ttu-id="b867f-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="b867f-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="b867f-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="b867f-622">1,495.71</span></span></td>
<td><span data-ttu-id="b867f-623">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b867f-624">V následující tabulce je uveden výsledek při použití Služeb balení jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="b867f-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b867f-625">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-625">Cost object</span></span></th>
<th><span data-ttu-id="b867f-626">Hodnota</span><span class="sxs-lookup"><span data-stu-id="b867f-626">Magnitude</span></span></th>
<th><span data-ttu-id="b867f-627">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="b867f-627">Allocation factor</span></span></th>
<th><span data-ttu-id="b867f-628">Částka</span><span class="sxs-lookup"><span data-stu-id="b867f-628">Amount</span></span></th>
<th><span data-ttu-id="b867f-629">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b867f-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b867f-630">Prod 1</span></span></td>
<td><span data-ttu-id="b867f-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="b867f-631">Product 1</span></span></td>
<td><span data-ttu-id="b867f-632">80</span><span class="sxs-lookup"><span data-stu-id="b867f-632">80</span></span></td>
<td><span data-ttu-id="b867f-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="b867f-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="b867f-634">241.05</span><span class="sxs-lookup"><span data-stu-id="b867f-634">241.05</span></span></td>
<td><span data-ttu-id="b867f-635">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b867f-636">Prod 2</span></span></td>
<td><span data-ttu-id="b867f-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="b867f-637">Product 2</span></span></td>
<td><span data-ttu-id="b867f-638">15</span><span class="sxs-lookup"><span data-stu-id="b867f-638">15</span></span></td>
<td><span data-ttu-id="b867f-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="b867f-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="b867f-640">45.20</span><span class="sxs-lookup"><span data-stu-id="b867f-640">45.20</span></span></td>
<td><span data-ttu-id="b867f-641">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b867f-642">Prod 1</span></span></td>
<td><span data-ttu-id="b867f-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="b867f-643">Product 1</span></span></td>
<td><span data-ttu-id="b867f-644">80</span><span class="sxs-lookup"><span data-stu-id="b867f-644">80</span></span></td>
<td><span data-ttu-id="b867f-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="b867f-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="b867f-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="b867f-646">2,507.09</span></span></td>
<td><span data-ttu-id="b867f-647">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b867f-648">Prod 2</span></span></td>
<td><span data-ttu-id="b867f-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="b867f-649">Product 2</span></span></td>
<td><span data-ttu-id="b867f-650">15</span><span class="sxs-lookup"><span data-stu-id="b867f-650">15</span></span></td>
<td><span data-ttu-id="b867f-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="b867f-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="b867f-652">470.08</span><span class="sxs-lookup"><span data-stu-id="b867f-652">470.08</span></span></td>
<td><span data-ttu-id="b867f-653">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="b867f-654">Položky deníku (položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="b867f-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b867f-655">Deník</span><span class="sxs-lookup"><span data-stu-id="b867f-655">Journal</span></span></th>
<th><span data-ttu-id="b867f-656">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="b867f-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b867f-657">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="b867f-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b867f-658">Verze</span><span class="sxs-lookup"><span data-stu-id="b867f-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b867f-659">00004</span><span class="sxs-lookup"><span data-stu-id="b867f-659">00004</span></span></td>
<td><span data-ttu-id="b867f-660">Deník přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="b867f-661">Fiskální</span><span class="sxs-lookup"><span data-stu-id="b867f-661">Fiscal</span></span></td>
<td><span data-ttu-id="b867f-662">2017</span><span class="sxs-lookup"><span data-stu-id="b867f-662">2017</span></span></td>
<td><span data-ttu-id="b867f-663">Období 1</span><span class="sxs-lookup"><span data-stu-id="b867f-663">Period 1</span></span></td>
<td><span data-ttu-id="b867f-664">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="b867f-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="b867f-665">Řádky deníku</span><span class="sxs-lookup"><span data-stu-id="b867f-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b867f-666">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="b867f-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b867f-667">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b867f-668">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-668">Cost element</span></span></th>
<th><span data-ttu-id="b867f-669">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-669">Cost behavior</span></span></th>
<th><span data-ttu-id="b867f-670">Částka</span><span class="sxs-lookup"><span data-stu-id="b867f-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b867f-671">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="b867f-672">CC001</span><span class="sxs-lookup"><span data-stu-id="b867f-672">CC001</span></span></td>
<td><span data-ttu-id="b867f-673">HR</span><span class="sxs-lookup"><span data-stu-id="b867f-673">HR</span></span></td>
<td><span data-ttu-id="b867f-674">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-674">10001</span></span></td>
<td><span data-ttu-id="b867f-675">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-675">Electricity</span></span></td>
<td><span data-ttu-id="b867f-676">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-676">Fixed cost</span></span></td>
<td><span data-ttu-id="b867f-677">500.00</span><span class="sxs-lookup"><span data-stu-id="b867f-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-678">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="b867f-679">CC001</span><span class="sxs-lookup"><span data-stu-id="b867f-679">CC001</span></span></td>
<td><span data-ttu-id="b867f-680">HR</span><span class="sxs-lookup"><span data-stu-id="b867f-680">HR</span></span></td>
<td><span data-ttu-id="b867f-681">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-681">10001</span></span></td>
<td><span data-ttu-id="b867f-682">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-682">Electricity</span></span></td>
<td><span data-ttu-id="b867f-683">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-683">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="b867f-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-685">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="b867f-686">CC002</span><span class="sxs-lookup"><span data-stu-id="b867f-686">CC002</span></span></td>
<td><span data-ttu-id="b867f-687">Finance</span><span class="sxs-lookup"><span data-stu-id="b867f-687">Finance</span></span></td>
<td><span data-ttu-id="b867f-688">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-688">10001</span></span></td>
<td><span data-ttu-id="b867f-689">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-689">Electricity</span></span></td>
<td><span data-ttu-id="b867f-690">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-690">Fixed cost</span></span></td>
<td><span data-ttu-id="b867f-691">675.00</span><span class="sxs-lookup"><span data-stu-id="b867f-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-692">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="b867f-693">CC002</span><span class="sxs-lookup"><span data-stu-id="b867f-693">CC002</span></span></td>
<td><span data-ttu-id="b867f-694">Finance</span><span class="sxs-lookup"><span data-stu-id="b867f-694">Finance</span></span></td>
<td><span data-ttu-id="b867f-695">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-695">10001</span></span></td>
<td><span data-ttu-id="b867f-696">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-696">Electricity</span></span></td>
<td><span data-ttu-id="b867f-697">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-697">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="b867f-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-699">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="b867f-700">CC003</span><span class="sxs-lookup"><span data-stu-id="b867f-700">CC003</span></span></td>
<td><span data-ttu-id="b867f-701">Sestavení</span><span class="sxs-lookup"><span data-stu-id="b867f-701">Assembly</span></span></td>
<td><span data-ttu-id="b867f-702">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-702">10001</span></span></td>
<td><span data-ttu-id="b867f-703">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-703">Electricity</span></span></td>
<td><span data-ttu-id="b867f-704">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-704">Fixed cost</span></span></td>
<td><span data-ttu-id="b867f-705">713.75</span><span class="sxs-lookup"><span data-stu-id="b867f-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-706">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="b867f-707">CC003</span><span class="sxs-lookup"><span data-stu-id="b867f-707">CC003</span></span></td>
<td><span data-ttu-id="b867f-708">Sestavení</span><span class="sxs-lookup"><span data-stu-id="b867f-708">Assembly</span></span></td>
<td><span data-ttu-id="b867f-709">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-709">10001</span></span></td>
<td><span data-ttu-id="b867f-710">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-710">Electricity</span></span></td>
<td><span data-ttu-id="b867f-711">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-711">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="b867f-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-713">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="b867f-714">CC003</span><span class="sxs-lookup"><span data-stu-id="b867f-714">CC003</span></span></td>
<td><span data-ttu-id="b867f-715">Balení</span><span class="sxs-lookup"><span data-stu-id="b867f-715">Packaging</span></span></td>
<td><span data-ttu-id="b867f-716">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-716">10001</span></span></td>
<td><span data-ttu-id="b867f-717">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-717">Electricity</span></span></td>
<td><span data-ttu-id="b867f-718">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-718">Fixed cost</span></span></td>
<td><span data-ttu-id="b867f-719">286.25</span><span class="sxs-lookup"><span data-stu-id="b867f-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-720">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="b867f-721">CC003</span><span class="sxs-lookup"><span data-stu-id="b867f-721">CC003</span></span></td>
<td><span data-ttu-id="b867f-722">Balení</span><span class="sxs-lookup"><span data-stu-id="b867f-722">Packaging</span></span></td>
<td><span data-ttu-id="b867f-723">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-723">10001</span></span></td>
<td><span data-ttu-id="b867f-724">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-724">Electricity</span></span></td>
<td><span data-ttu-id="b867f-725">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-725">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="b867f-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-727">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="b867f-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b867f-728">Prod 1</span></span></td>
<td><span data-ttu-id="b867f-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="b867f-729">Product 1</span></span></td>
<td><span data-ttu-id="b867f-730">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-730">10001</span></span></td>
<td><span data-ttu-id="b867f-731">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-731">Electricity</span></span></td>
<td><span data-ttu-id="b867f-732">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-732">Fixed cost</span></span></td>
<td><span data-ttu-id="b867f-733">776.36</span><span class="sxs-lookup"><span data-stu-id="b867f-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-734">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="b867f-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b867f-735">Prod 1</span></span></td>
<td><span data-ttu-id="b867f-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="b867f-736">Product 1</span></span></td>
<td><span data-ttu-id="b867f-737">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-737">10001</span></span></td>
<td><span data-ttu-id="b867f-738">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-738">Electricity</span></span></td>
<td><span data-ttu-id="b867f-739">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-739">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="b867f-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-741">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="b867f-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b867f-742">Prod 2</span></span></td>
<td><span data-ttu-id="b867f-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="b867f-743">Product 1</span></span></td>
<td><span data-ttu-id="b867f-744">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-744">10001</span></span></td>
<td><span data-ttu-id="b867f-745">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-745">Electricity</span></span></td>
<td><span data-ttu-id="b867f-746">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-746">Fixed cost</span></span></td>
<td><span data-ttu-id="b867f-747">223.64</span><span class="sxs-lookup"><span data-stu-id="b867f-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-748">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="b867f-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b867f-749">Prod 2</span></span></td>
<td><span data-ttu-id="b867f-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="b867f-750">Product 1</span></span></td>
<td><span data-ttu-id="b867f-751">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-751">10001</span></span></td>
<td><span data-ttu-id="b867f-752">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-752">Electricity</span></span></td>
<td><span data-ttu-id="b867f-753">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-753">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="b867f-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b867f-755">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b867f-756">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b867f-757">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-757">Cost element</span></span></th>
<th><span data-ttu-id="b867f-758">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-758">Cost behavior</span></span></th>
<th><span data-ttu-id="b867f-759">Částka</span><span class="sxs-lookup"><span data-stu-id="b867f-759">Amount</span></span></th>
<th><span data-ttu-id="b867f-760">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="b867f-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b867f-761">CC001</span><span class="sxs-lookup"><span data-stu-id="b867f-761">CC001</span></span></td>
<td><span data-ttu-id="b867f-762">HR</span><span class="sxs-lookup"><span data-stu-id="b867f-762">HR</span></span></td>
<td><span data-ttu-id="b867f-763">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-763">10001</span></span></td>
<td><span data-ttu-id="b867f-764">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-764">Electricity</span></span></td>
<td><span data-ttu-id="b867f-765">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-765">Fixed cost</span></span></td>
<td><span data-ttu-id="b867f-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="b867f-766">-500.00</span></span></td>
<td><span data-ttu-id="b867f-767">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-768">CC002</span><span class="sxs-lookup"><span data-stu-id="b867f-768">CC002</span></span></td>
<td><span data-ttu-id="b867f-769">Finance</span><span class="sxs-lookup"><span data-stu-id="b867f-769">Finance</span></span></td>
<td><span data-ttu-id="b867f-770">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-770">10001</span></span></td>
<td><span data-ttu-id="b867f-771">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-771">Electricity</span></span></td>
<td><span data-ttu-id="b867f-772">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-772">Fixed cost</span></span></td>
<td><span data-ttu-id="b867f-773">175.00</span><span class="sxs-lookup"><span data-stu-id="b867f-773">175.00</span></span></td>
<td><span data-ttu-id="b867f-774">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-775">CC003</span><span class="sxs-lookup"><span data-stu-id="b867f-775">CC003</span></span></td>
<td><span data-ttu-id="b867f-776">Sestavení</span><span class="sxs-lookup"><span data-stu-id="b867f-776">Assembly</span></span></td>
<td><span data-ttu-id="b867f-777">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-777">10001</span></span></td>
<td><span data-ttu-id="b867f-778">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-778">Electricity</span></span></td>
<td><span data-ttu-id="b867f-779">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-779">Fixed cost</span></span></td>
<td><span data-ttu-id="b867f-780">275.00</span><span class="sxs-lookup"><span data-stu-id="b867f-780">275.00</span></span></td>
<td><span data-ttu-id="b867f-781">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-782">CC004</span><span class="sxs-lookup"><span data-stu-id="b867f-782">CC004</span></span></td>
<td><span data-ttu-id="b867f-783">Balení</span><span class="sxs-lookup"><span data-stu-id="b867f-783">Packaging</span></span></td>
<td><span data-ttu-id="b867f-784">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-784">10001</span></span></td>
<td><span data-ttu-id="b867f-785">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-785">Electricity</span></span></td>
<td><span data-ttu-id="b867f-786">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-786">Fixed cost</span></span></td>
<td><span data-ttu-id="b867f-787">50,00</span><span class="sxs-lookup"><span data-stu-id="b867f-787">50,00</span></span></td>
<td><span data-ttu-id="b867f-788">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-789">CC001</span><span class="sxs-lookup"><span data-stu-id="b867f-789">CC001</span></span></td>
<td><span data-ttu-id="b867f-790">HR</span><span class="sxs-lookup"><span data-stu-id="b867f-790">HR</span></span></td>
<td><span data-ttu-id="b867f-791">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-791">10001</span></span></td>
<td><span data-ttu-id="b867f-792">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-792">Electricity</span></span></td>
<td><span data-ttu-id="b867f-793">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-793">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-794">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="b867f-794">-1,245.71</span></span></td>
<td><span data-ttu-id="b867f-795">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-796">CC002</span><span class="sxs-lookup"><span data-stu-id="b867f-796">CC002</span></span></td>
<td><span data-ttu-id="b867f-797">Finance</span><span class="sxs-lookup"><span data-stu-id="b867f-797">Finance</span></span></td>
<td><span data-ttu-id="b867f-798">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-798">10001</span></span></td>
<td><span data-ttu-id="b867f-799">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-799">Electricity</span></span></td>
<td><span data-ttu-id="b867f-800">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-800">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-801">436.00</span><span class="sxs-lookup"><span data-stu-id="b867f-801">436.00</span></span></td>
<td><span data-ttu-id="b867f-802">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-803">CC003</span><span class="sxs-lookup"><span data-stu-id="b867f-803">CC003</span></span></td>
<td><span data-ttu-id="b867f-804">Sestavení</span><span class="sxs-lookup"><span data-stu-id="b867f-804">Assembly</span></span></td>
<td><span data-ttu-id="b867f-805">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-805">10001</span></span></td>
<td><span data-ttu-id="b867f-806">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-806">Electricity</span></span></td>
<td><span data-ttu-id="b867f-807">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-807">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-808">685.14</span><span class="sxs-lookup"><span data-stu-id="b867f-808">685.14</span></span></td>
<td><span data-ttu-id="b867f-809">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-810">CC004</span><span class="sxs-lookup"><span data-stu-id="b867f-810">CC004</span></span></td>
<td><span data-ttu-id="b867f-811">Balení</span><span class="sxs-lookup"><span data-stu-id="b867f-811">Packaging</span></span></td>
<td><span data-ttu-id="b867f-812">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-812">10001</span></span></td>
<td><span data-ttu-id="b867f-813">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-813">Electricity</span></span></td>
<td><span data-ttu-id="b867f-814">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-814">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-815">124.57</span><span class="sxs-lookup"><span data-stu-id="b867f-815">124.57</span></span></td>
<td><span data-ttu-id="b867f-816">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-817">CC002</span><span class="sxs-lookup"><span data-stu-id="b867f-817">CC002</span></span></td>
<td><span data-ttu-id="b867f-818">Finance</span><span class="sxs-lookup"><span data-stu-id="b867f-818">Finance</span></span></td>
<td><span data-ttu-id="b867f-819">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-819">10001</span></span></td>
<td><span data-ttu-id="b867f-820">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-820">Electricity</span></span></td>
<td><span data-ttu-id="b867f-821">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-821">Fixed cost</span></span></td>
<td><span data-ttu-id="b867f-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="b867f-822">-675.00</span></span></td>
<td><span data-ttu-id="b867f-823">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-824">CC003</span><span class="sxs-lookup"><span data-stu-id="b867f-824">CC003</span></span></td>
<td><span data-ttu-id="b867f-825">Sestavení</span><span class="sxs-lookup"><span data-stu-id="b867f-825">Assembly</span></span></td>
<td><span data-ttu-id="b867f-826">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-826">10001</span></span></td>
<td><span data-ttu-id="b867f-827">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-827">Electricity</span></span></td>
<td><span data-ttu-id="b867f-828">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-828">Fixed cost</span></span></td>
<td><span data-ttu-id="b867f-829">438.75</span><span class="sxs-lookup"><span data-stu-id="b867f-829">438.75</span></span></td>
<td><span data-ttu-id="b867f-830">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-831">CC004</span><span class="sxs-lookup"><span data-stu-id="b867f-831">CC004</span></span></td>
<td><span data-ttu-id="b867f-832">Balení</span><span class="sxs-lookup"><span data-stu-id="b867f-832">Packaging</span></span></td>
<td><span data-ttu-id="b867f-833">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-833">10001</span></span></td>
<td><span data-ttu-id="b867f-834">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-834">Electricity</span></span></td>
<td><span data-ttu-id="b867f-835">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-835">Fixed cost</span></span></td>
<td><span data-ttu-id="b867f-836">236.25</span><span class="sxs-lookup"><span data-stu-id="b867f-836">236.25</span></span></td>
<td><span data-ttu-id="b867f-837">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-838">CC002</span><span class="sxs-lookup"><span data-stu-id="b867f-838">CC002</span></span></td>
<td><span data-ttu-id="b867f-839">Finance</span><span class="sxs-lookup"><span data-stu-id="b867f-839">Finance</span></span></td>
<td><span data-ttu-id="b867f-840">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-840">10001</span></span></td>
<td><span data-ttu-id="b867f-841">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-841">Electricity</span></span></td>
<td><span data-ttu-id="b867f-842">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-842">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-843">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="b867f-843">-8,150.29</span></span></td>
<td><span data-ttu-id="b867f-844">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-845">CC003</span><span class="sxs-lookup"><span data-stu-id="b867f-845">CC003</span></span></td>
<td><span data-ttu-id="b867f-846">Sestavení</span><span class="sxs-lookup"><span data-stu-id="b867f-846">Assembly</span></span></td>
<td><span data-ttu-id="b867f-847">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-847">10001</span></span></td>
<td><span data-ttu-id="b867f-848">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-848">Electricity</span></span></td>
<td><span data-ttu-id="b867f-849">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-849">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="b867f-850">5,297.69</span></span></td>
<td><span data-ttu-id="b867f-851">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-852">CC004</span><span class="sxs-lookup"><span data-stu-id="b867f-852">CC004</span></span></td>
<td><span data-ttu-id="b867f-853">Balení</span><span class="sxs-lookup"><span data-stu-id="b867f-853">Packaging</span></span></td>
<td><span data-ttu-id="b867f-854">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-854">10001</span></span></td>
<td><span data-ttu-id="b867f-855">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-855">Electricity</span></span></td>
<td><span data-ttu-id="b867f-856">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-856">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="b867f-857">2,852.60</span></span></td>
<td><span data-ttu-id="b867f-858">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-859">CC003</span><span class="sxs-lookup"><span data-stu-id="b867f-859">CC003</span></span></td>
<td><span data-ttu-id="b867f-860">Sestavení</span><span class="sxs-lookup"><span data-stu-id="b867f-860">Assembly</span></span></td>
<td><span data-ttu-id="b867f-861">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-861">10001</span></span></td>
<td><span data-ttu-id="b867f-862">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-862">Electricity</span></span></td>
<td><span data-ttu-id="b867f-863">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-863">Fixed cost</span></span></td>
<td><span data-ttu-id="b867f-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="b867f-864">-713.75</span></span></td>
<td><span data-ttu-id="b867f-865">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b867f-866">Prod 1</span></span></td>
<td><span data-ttu-id="b867f-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="b867f-867">Product 1</span></span></td>
<td><span data-ttu-id="b867f-868">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-868">10001</span></span></td>
<td><span data-ttu-id="b867f-869">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-869">Electricity</span></span></td>
<td><span data-ttu-id="b867f-870">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-870">Fixed cost</span></span></td>
<td><span data-ttu-id="b867f-871">535.31</span><span class="sxs-lookup"><span data-stu-id="b867f-871">535.31</span></span></td>
<td><span data-ttu-id="b867f-872">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b867f-873">Prod 2</span></span></td>
<td><span data-ttu-id="b867f-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="b867f-874">Product 2</span></span></td>
<td><span data-ttu-id="b867f-875">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-875">10001</span></span></td>
<td><span data-ttu-id="b867f-876">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-876">Electricity</span></span></td>
<td><span data-ttu-id="b867f-877">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-877">Fixed cost</span></span></td>
<td><span data-ttu-id="b867f-878">178.44</span><span class="sxs-lookup"><span data-stu-id="b867f-878">178.44</span></span></td>
<td><span data-ttu-id="b867f-879">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-880">CC003</span><span class="sxs-lookup"><span data-stu-id="b867f-880">CC003</span></span></td>
<td><span data-ttu-id="b867f-881">Sestavení</span><span class="sxs-lookup"><span data-stu-id="b867f-881">Assembly</span></span></td>
<td><span data-ttu-id="b867f-882">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-882">10001</span></span></td>
<td><span data-ttu-id="b867f-883">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-883">Electricity</span></span></td>
<td><span data-ttu-id="b867f-884">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-884">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-885">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="b867f-885">-5,982.83</span></span></td>
<td><span data-ttu-id="b867f-886">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b867f-887">Prod 1</span></span></td>
<td><span data-ttu-id="b867f-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="b867f-888">Product 1</span></span></td>
<td><span data-ttu-id="b867f-889">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-889">10001</span></span></td>
<td><span data-ttu-id="b867f-890">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-890">Electricity</span></span></td>
<td><span data-ttu-id="b867f-891">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-891">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="b867f-892">4,487.12</span></span></td>
<td><span data-ttu-id="b867f-893">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b867f-894">Prod 2</span></span></td>
<td><span data-ttu-id="b867f-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="b867f-895">Product 2</span></span></td>
<td><span data-ttu-id="b867f-896">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-896">10001</span></span></td>
<td><span data-ttu-id="b867f-897">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-897">Electricity</span></span></td>
<td><span data-ttu-id="b867f-898">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-898">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="b867f-899">1,495.71</span></span></td>
<td><span data-ttu-id="b867f-900">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-901">CC003</span><span class="sxs-lookup"><span data-stu-id="b867f-901">CC003</span></span></td>
<td><span data-ttu-id="b867f-902">Sestavení</span><span class="sxs-lookup"><span data-stu-id="b867f-902">Assembly</span></span></td>
<td><span data-ttu-id="b867f-903">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-903">10001</span></span></td>
<td><span data-ttu-id="b867f-904">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-904">Electricity</span></span></td>
<td><span data-ttu-id="b867f-905">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-905">Fixed cost</span></span></td>
<td><span data-ttu-id="b867f-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="b867f-906">-286.25</span></span></td>
<td><span data-ttu-id="b867f-907">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b867f-908">Prod 1</span></span></td>
<td><span data-ttu-id="b867f-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="b867f-909">Product 1</span></span></td>
<td><span data-ttu-id="b867f-910">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-910">10001</span></span></td>
<td><span data-ttu-id="b867f-911">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-911">Electricity</span></span></td>
<td><span data-ttu-id="b867f-912">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-912">Fixed cost</span></span></td>
<td><span data-ttu-id="b867f-913">241.05</span><span class="sxs-lookup"><span data-stu-id="b867f-913">241.05</span></span></td>
<td><span data-ttu-id="b867f-914">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b867f-915">Prod 2</span></span></td>
<td><span data-ttu-id="b867f-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="b867f-916">Product 2</span></span></td>
<td><span data-ttu-id="b867f-917">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-917">10001</span></span></td>
<td><span data-ttu-id="b867f-918">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-918">Electricity</span></span></td>
<td><span data-ttu-id="b867f-919">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-919">Fixed cost</span></span></td>
<td><span data-ttu-id="b867f-920">45.20</span><span class="sxs-lookup"><span data-stu-id="b867f-920">45.20</span></span></td>
<td><span data-ttu-id="b867f-921">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-922">CC003</span><span class="sxs-lookup"><span data-stu-id="b867f-922">CC003</span></span></td>
<td><span data-ttu-id="b867f-923">Sestavení</span><span class="sxs-lookup"><span data-stu-id="b867f-923">Assembly</span></span></td>
<td><span data-ttu-id="b867f-924">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-924">10001</span></span></td>
<td><span data-ttu-id="b867f-925">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-925">Electricity</span></span></td>
<td><span data-ttu-id="b867f-926">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-926">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="b867f-927">-2,977.17</span></span></td>
<td><span data-ttu-id="b867f-928">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b867f-929">Prod 1</span></span></td>
<td><span data-ttu-id="b867f-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="b867f-930">Product 1</span></span></td>
<td><span data-ttu-id="b867f-931">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-931">10001</span></span></td>
<td><span data-ttu-id="b867f-932">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-932">Electricity</span></span></td>
<td><span data-ttu-id="b867f-933">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-933">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="b867f-934">2,507.09</span></span></td>
<td><span data-ttu-id="b867f-935">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b867f-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b867f-936">Prod 2</span></span></td>
<td><span data-ttu-id="b867f-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="b867f-937">Product 2</span></span></td>
<td><span data-ttu-id="b867f-938">10001</span><span class="sxs-lookup"><span data-stu-id="b867f-938">10001</span></span></td>
<td><span data-ttu-id="b867f-939">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="b867f-939">Electricity</span></span></td>
<td><span data-ttu-id="b867f-940">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-940">Variable cost</span></span></td>
<td><span data-ttu-id="b867f-941">470.08</span><span class="sxs-lookup"><span data-stu-id="b867f-941">470.08</span></span></td>
<td><span data-ttu-id="b867f-942">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="b867f-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="b867f-943">Závěr</span><span class="sxs-lookup"><span data-stu-id="b867f-943">Conclusion</span></span>
<span data-ttu-id="b867f-944">Ve finančním účtování se náklady za elektřinu ve výši 10 000 zaúčtují na ID fiktivního nákladového střediska.</span><span class="sxs-lookup"><span data-stu-id="b867f-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="b867f-945">Účetní tak budou vědět, že tento náklad musí být přidělen.</span><span class="sxs-lookup"><span data-stu-id="b867f-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="b867f-946">V nákladovém účetnictví náklady procházejí napříč organizačními jednotkami a úrovněmi, na základě použitých zásad a pravidel.</span><span class="sxs-lookup"><span data-stu-id="b867f-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="b867f-947">Každý náklad byl přidružen k základu přidělení, který poskytuje nejlepší hodnocení pro přidělení nákladů.</span><span class="sxs-lookup"><span data-stu-id="b867f-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="b867f-948">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="b867f-949">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="b867f-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="b867f-950">Celkem</span><span class="sxs-lookup"><span data-stu-id="b867f-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="b867f-951">CC099</span><span class="sxs-lookup"><span data-stu-id="b867f-951">CC099</span></span></th>
<th><span data-ttu-id="b867f-952">CC001</span><span class="sxs-lookup"><span data-stu-id="b867f-952">CC001</span></span></th>
<th><span data-ttu-id="b867f-953">CC002</span><span class="sxs-lookup"><span data-stu-id="b867f-953">CC002</span></span></th>
<th><span data-ttu-id="b867f-954">CC003</span><span class="sxs-lookup"><span data-stu-id="b867f-954">CC003</span></span></th>
<th><span data-ttu-id="b867f-955">CC004</span><span class="sxs-lookup"><span data-stu-id="b867f-955">CC004</span></span></th>
<th><span data-ttu-id="b867f-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="b867f-956">Proj 1</span></span></th>
<th><span data-ttu-id="b867f-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="b867f-957">Proj 2</span></span></th>
<th><span data-ttu-id="b867f-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b867f-958">Prod 1</span></span></th>
<th><span data-ttu-id="b867f-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b867f-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="b867f-960">10001 Elektřina</span><span class="sxs-lookup"><span data-stu-id="b867f-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b867f-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="b867f-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b867f-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="b867f-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b867f-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="b867f-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b867f-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="b867f-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="b867f-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="b867f-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b867f-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="b867f-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b867f-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="b867f-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b867f-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="b867f-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b867f-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="b867f-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="b867f-970">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="b867f-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b867f-971">0,00</span><span class="sxs-lookup"><span data-stu-id="b867f-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="b867f-972">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b867f-973">0,00</span><span class="sxs-lookup"><span data-stu-id="b867f-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b867f-974">0,00</span><span class="sxs-lookup"><span data-stu-id="b867f-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b867f-975">0,00</span><span class="sxs-lookup"><span data-stu-id="b867f-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b867f-976">0,00</span><span class="sxs-lookup"><span data-stu-id="b867f-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b867f-977">0,00</span><span class="sxs-lookup"><span data-stu-id="b867f-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="b867f-978">776.36</span><span class="sxs-lookup"><span data-stu-id="b867f-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b867f-979">223.64</span><span class="sxs-lookup"><span data-stu-id="b867f-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b867f-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="b867f-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="b867f-981">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="b867f-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b867f-982">000</span><span class="sxs-lookup"><span data-stu-id="b867f-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b867f-983">0,00</span><span class="sxs-lookup"><span data-stu-id="b867f-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b867f-984">0,00</span><span class="sxs-lookup"><span data-stu-id="b867f-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b867f-985">0,00</span><span class="sxs-lookup"><span data-stu-id="b867f-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b867f-986">0,00</span><span class="sxs-lookup"><span data-stu-id="b867f-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b867f-987">30.00</span><span class="sxs-lookup"><span data-stu-id="b867f-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b867f-988">10,00</span><span class="sxs-lookup"><span data-stu-id="b867f-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b867f-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="b867f-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b867f-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="b867f-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b867f-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="b867f-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="b867f-992">Toto téma popisuje, jak primární prvek nákladů, 10001 Elektřina, prochází přes objekty nákladů.</span><span class="sxs-lookup"><span data-stu-id="b867f-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="b867f-993">Tyto režijní náklady tedy budou přiděleny na nejnižší úroveň v organizaci.</span><span class="sxs-lookup"><span data-stu-id="b867f-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="b867f-994">Jinak řečeno, objekty nákladů na nejnižší úrovni ponesou náklady.</span><span class="sxs-lookup"><span data-stu-id="b867f-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="b867f-995">Chcete-li vizuální tok nákladů mezi objekty nákladů, můžete použít pravidla zásad shrnutí nákladů pro vizualizaci jejich toků.</span><span class="sxs-lookup"><span data-stu-id="b867f-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="b867f-996">Podrobnější informace naleznete v tématu [Zásady shrnutí nákladů](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="b867f-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>




