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
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
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
ms.openlocfilehash: 954e0669c3d24bcc20fe667c22b7dcc367aba1e7
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770797"
---
# <a name="overhead-calculation"></a><span data-ttu-id="e4d85-103">Výpočet režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e4d85-104">Toto téma popisuje typické procesy pro výpočet a přidělení režijních nákladů.</span><span class="sxs-lookup"><span data-stu-id="e4d85-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="e4d85-105">Definice termínu</span><span class="sxs-lookup"><span data-stu-id="e4d85-105">Term definition</span></span>
---------------

<span data-ttu-id="e4d85-106">Režijní náklady jsou náklady, které nutně vznikají při chodu podnikání, ale nelze je připsat přímo k žádné konkrétní podnikatelské aktivitě, produktu nebo službě.</span><span class="sxs-lookup"><span data-stu-id="e4d85-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="e4d85-107">Režijní náklady poskytují důležitou podporu pro generování aktivity přinášejících zisk.</span><span class="sxs-lookup"><span data-stu-id="e4d85-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="e4d85-108">Následuje několik příkladů režijních nákladů:</span><span class="sxs-lookup"><span data-stu-id="e4d85-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="e4d85-109">Renta</span><span class="sxs-lookup"><span data-stu-id="e4d85-109">Rent</span></span>
-   <span data-ttu-id="e4d85-110">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-110">Electricity</span></span>
-   <span data-ttu-id="e4d85-111">Administrativní mzdy</span><span class="sxs-lookup"><span data-stu-id="e4d85-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="e4d85-112">Přehled výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-112">Overhead calculation overview</span></span>
<span data-ttu-id="e4d85-113">Výpočet režijních nákladů spustí zásady účtování nákladů ve správném pořadí.</span><span class="sxs-lookup"><span data-stu-id="e4d85-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="e4d85-114">Výpočet režijních nákladů můžete pro stejné fiskální období spustit mnohokrát, pokud došlo ke změně zásad účtování nákladů nebo zjištění konkrétních chyb.</span><span class="sxs-lookup"><span data-stu-id="e4d85-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="e4d85-115">Každé spuštění výpočtu režijních nákladů se ukládá a přijímá ID jedinečné verze, které vám umožní porovnávat výpočty v různých verzích.</span><span class="sxs-lookup"><span data-stu-id="e4d85-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="e4d85-116">Položky nákladů, které generuje výpočet režijních nákladů, přijímá datum účtování.</span><span class="sxs-lookup"><span data-stu-id="e4d85-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="e4d85-117">Toto datum účtován se shoduje s konvovým datem fiskálního období, které se použije ve výpočtu.</span><span class="sxs-lookup"><span data-stu-id="e4d85-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="e4d85-118">ID jedinečné verze se skládá z následujících prvků:</span><span class="sxs-lookup"><span data-stu-id="e4d85-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="e4d85-119">Typ verze</span><span class="sxs-lookup"><span data-stu-id="e4d85-119">Version type</span></span>
-   <span data-ttu-id="e4d85-120">Datum a čas</span><span class="sxs-lookup"><span data-stu-id="e4d85-120">Date and time</span></span>
-   <span data-ttu-id="e4d85-121">Hlavní kniha nákladového účetnictví</span><span class="sxs-lookup"><span data-stu-id="e4d85-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="e4d85-122">Fiskální rok</span><span class="sxs-lookup"><span data-stu-id="e4d85-122">Fiscal year</span></span>
-   <span data-ttu-id="e4d85-123">Fiskální období</span><span class="sxs-lookup"><span data-stu-id="e4d85-123">Fiscal period</span></span>

<span data-ttu-id="e4d85-124">Výpočet režijních nákladů se spustí bez ohledu na verzi.</span><span class="sxs-lookup"><span data-stu-id="e4d85-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="e4d85-125">Proto lze vypočítat rozpočtovou verzi před skutečnou verzí.</span><span class="sxs-lookup"><span data-stu-id="e4d85-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="e4d85-126">Výpočet režijních nákladů se skládá ze čtyř kroků uvedených na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="e4d85-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="e4d85-127">V každé fázi je vytvořeno záhlaví deníku, které obsahuje položky deníku.</span><span class="sxs-lookup"><span data-stu-id="e4d85-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="e4d85-128">Toto záhlaví deníku zachovává vstupní data pro každý krok výpočtu.</span><span class="sxs-lookup"><span data-stu-id="e4d85-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="e4d85-129">Zásady a pravidla se použijí na každý řádek deníku a položky nákladů jsou generovány jako výstup.</span><span class="sxs-lookup"><span data-stu-id="e4d85-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="e4d85-130">Máte tedy vždy plnou sledovatelnost.</span><span class="sxs-lookup"><span data-stu-id="e4d85-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="e4d85-131">[![Výpočet režijních nákladů](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="e4d85-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="e4d85-132">Výpočet a přidělení režijních nákladů za elektřinu</span><span class="sxs-lookup"><span data-stu-id="e4d85-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="e4d85-133">Ve finančním účetnictví se některé náklady, jako je například elektřina, registrují jako paušální.</span><span class="sxs-lookup"><span data-stu-id="e4d85-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="e4d85-134">Podrobný přehled pro vedoucí není tedy pro nákladové účetnictví k dispozici.</span><span class="sxs-lookup"><span data-stu-id="e4d85-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="e4d85-135">V nákladovém účetnictví musí náklady procházet organizačními jednotkami, aby byl získán správný přehled pro vedoucí napříč všemi jednotkami a úrovněmi organizace.</span><span class="sxs-lookup"><span data-stu-id="e4d85-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="e4d85-136">Tento tok musí být založen buď na přesném záznamu spotřeby nebo na objektivním hodnocení.</span><span class="sxs-lookup"><span data-stu-id="e4d85-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="e4d85-137">V hlavní knize mohou být zaúčtovány náklady na elektřinu způsobem znázorněným v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="e4d85-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e4d85-138">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="e4d85-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e4d85-139">Nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="e4d85-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="e4d85-140">Hlavní účet</span><span class="sxs-lookup"><span data-stu-id="e4d85-140">Main account</span></span></th>
<th><span data-ttu-id="e4d85-141">Částka v zúčtovací měně</span><span class="sxs-lookup"><span data-stu-id="e4d85-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4d85-142">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="e4d85-143">CC099</span><span class="sxs-lookup"><span data-stu-id="e4d85-143">CC099</span></span></td>
<td><span data-ttu-id="e4d85-144">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="e4d85-144">Default cost center</span></span></td>
<td><span data-ttu-id="e4d85-145">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-145">10001</span></span></td>
<td><span data-ttu-id="e4d85-146">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-146">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="e4d85-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="e4d85-148">Krok 1: Zpracování výpočtu chování nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="e4d85-149">Ve výchozím nastavení dostanou při importu položek nákladů z datového zdroje tyto položky v nákladovém účetnictví klasifikaci **Neklasifikované**.</span><span class="sxs-lookup"><span data-stu-id="e4d85-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="e4d85-150">Použitím pravidla zásad chování nákladů lze reklasifikovat položky nákladů jako **Pevné náklady** nebo **Variabilní náklady**.</span><span class="sxs-lookup"><span data-stu-id="e4d85-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="e4d85-151">Definice pravidel chování nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-151">Define the cost behavior rule</span></span>

<span data-ttu-id="e4d85-152">V některých případech je část nákladů s pevným poplatkem a zbývající náklady jsou založeny na spotřebě.</span><span class="sxs-lookup"><span data-stu-id="e4d85-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="e4d85-153">Účty za elektřinu často odpovídají této definici.</span><span class="sxs-lookup"><span data-stu-id="e4d85-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="e4d85-154">Po platbě konkrétního pevného poplatku platíte spotřebu za kilowatthodinu (kWh).</span><span class="sxs-lookup"><span data-stu-id="e4d85-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="e4d85-155">Pokud je například poplatek pevných nákladů 1 000,00, definuje se pravidlo chování nákladů takto:</span><span class="sxs-lookup"><span data-stu-id="e4d85-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="e4d85-156">Pevná částka 1 000,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="e4d85-157">0 &lt;= 1 000,00 = Pevná</span><span class="sxs-lookup"><span data-stu-id="e4d85-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="e4d85-158">1 000,01 &lt; N = Variabilní</span><span class="sxs-lookup"><span data-stu-id="e4d85-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="e4d85-159">Deník</span><span class="sxs-lookup"><span data-stu-id="e4d85-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e4d85-160">Deník</span><span class="sxs-lookup"><span data-stu-id="e4d85-160">Journal</span></span></th>
<th><span data-ttu-id="e4d85-161">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="e4d85-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e4d85-162">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="e4d85-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e4d85-163">Verze</span><span class="sxs-lookup"><span data-stu-id="e4d85-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4d85-164">00001</span><span class="sxs-lookup"><span data-stu-id="e4d85-164">00001</span></span></td>
<td><span data-ttu-id="e4d85-165">Deník výpočtu chování nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="e4d85-166">Fiskální</span><span class="sxs-lookup"><span data-stu-id="e4d85-166">Fiscal</span></span></td>
<td><span data-ttu-id="e4d85-167">2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-167">2017</span></span></td>
<td><span data-ttu-id="e4d85-168">Období 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-168">Period 1</span></span></td>
<td><span data-ttu-id="e4d85-169">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="e4d85-170">Položky deníku (Položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="e4d85-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e4d85-171">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="e4d85-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e4d85-172">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e4d85-173">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-173">Cost element</span></span></th>
<th><span data-ttu-id="e4d85-174">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-174">Cost behavior</span></span></th>
<th><span data-ttu-id="e4d85-175">Částka</span><span class="sxs-lookup"><span data-stu-id="e4d85-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4d85-176">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="e4d85-177">CC099</span><span class="sxs-lookup"><span data-stu-id="e4d85-177">CC099</span></span></td>
<td><span data-ttu-id="e4d85-178">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="e4d85-178">Default cost center</span></span></td>
<td><span data-ttu-id="e4d85-179">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-179">10001</span></span></td>
<td><span data-ttu-id="e4d85-180">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-180">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-181">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="e4d85-181">Unclassified</span></span></td>
<td><span data-ttu-id="e4d85-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="e4d85-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e4d85-183">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4d85-184">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e4d85-185">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-185">Cost element</span></span></th>
<th><span data-ttu-id="e4d85-186">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-186">Cost behavior</span></span></th>
<th><span data-ttu-id="e4d85-187">Částka</span><span class="sxs-lookup"><span data-stu-id="e4d85-187">Amount</span></span></th>
<th><span data-ttu-id="e4d85-188">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="e4d85-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4d85-189">CC099</span><span class="sxs-lookup"><span data-stu-id="e4d85-189">CC099</span></span></td>
<td><span data-ttu-id="e4d85-190">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="e4d85-190">Default cost center</span></span></td>
<td><span data-ttu-id="e4d85-191">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-191">10001</span></span></td>
<td><span data-ttu-id="e4d85-192">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-192">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-193">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="e4d85-193">Unclassified</span></span></td>
<td><span data-ttu-id="e4d85-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="e4d85-194">10,000.00</span></span></td>
<td><span data-ttu-id="e4d85-195">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-196">CC099</span><span class="sxs-lookup"><span data-stu-id="e4d85-196">CC099</span></span></td>
<td><span data-ttu-id="e4d85-197">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="e4d85-197">Default cost center</span></span></td>
<td><span data-ttu-id="e4d85-198">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-198">10001</span></span></td>
<td><span data-ttu-id="e4d85-199">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-199">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-200">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="e4d85-200">Unclassified</span></span></td>
<td><span data-ttu-id="e4d85-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-201">-10,000.00</span></span></td>
<td><span data-ttu-id="e4d85-202">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-203">CC099</span><span class="sxs-lookup"><span data-stu-id="e4d85-203">CC099</span></span></td>
<td><span data-ttu-id="e4d85-204">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="e4d85-204">Default cost center</span></span></td>
<td><span data-ttu-id="e4d85-205">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-205">10001</span></span></td>
<td><span data-ttu-id="e4d85-206">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-206">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-207">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-207">Fixed cost</span></span></td>
<td><span data-ttu-id="e4d85-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-208">1,000.00</span></span></td>
<td><span data-ttu-id="e4d85-209">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-210">CC099</span><span class="sxs-lookup"><span data-stu-id="e4d85-210">CC099</span></span></td>
<td><span data-ttu-id="e4d85-211">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="e4d85-211">Default cost center</span></span></td>
<td><span data-ttu-id="e4d85-212">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-212">10001</span></span></td>
<td><span data-ttu-id="e4d85-213">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-213">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-214">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-214">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="e4d85-215">9,000.00</span></span></td>
<td><span data-ttu-id="e4d85-216">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e4d85-217">Více informací naleznete v tématu [Vytvoření a přiřazení zásad chování nákladů k jednotce řízení nákladů](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="e4d85-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="e4d85-218">Krok 2: Zpracování výpočtu distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="e4d85-219">Distribuce nákladů se používá k rozdělení nákladů z jednoho objektu nákladů na jeden nebo více dalších objektů nákladů použitím příslušného základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="e4d85-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="e4d85-220">Distribuce nákladů a přidělení nákladů se liší v tom, že k distribuci nákladů dochází vždy na úrovni primárního prvku nákladů původních nákladů.</span><span class="sxs-lookup"><span data-stu-id="e4d85-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="e4d85-221">Definice pravidel distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-221">Define the cost distribution rule</span></span>

<span data-ttu-id="e4d85-222">Ve finančním účetnictví se náklady na elektřinu často registrují jako paušální.</span><span class="sxs-lookup"><span data-stu-id="e4d85-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="e4d85-223">V nákladovém účetnictví není tento přístup dostatečně podrobný.</span><span class="sxs-lookup"><span data-stu-id="e4d85-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="e4d85-224">Variabilní náklady by měly být distribuovány k jednotlivým objektům nákladů na solidním základě.</span><span class="sxs-lookup"><span data-stu-id="e4d85-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="e4d85-225">Nejlogičtější základ přidělení je spotřeba elektřiny (kWh).</span><span class="sxs-lookup"><span data-stu-id="e4d85-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="e4d85-226">Vytvoří se člen statistické dimenzi s názvem Elektřina a zaznamená se elektrické spotřeba.</span><span class="sxs-lookup"><span data-stu-id="e4d85-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="e4d85-227">Ve výchozím nastavení se všechny členy statistické dimenze stanou dostupnými zpřístupněny jako základy přidělení.</span><span class="sxs-lookup"><span data-stu-id="e4d85-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4d85-228">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-228">Cost object</span></span></th>
<th><span data-ttu-id="e4d85-229">kWh</span><span class="sxs-lookup"><span data-stu-id="e4d85-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4d85-230">CC001</span><span class="sxs-lookup"><span data-stu-id="e4d85-230">CC001</span></span></td>
<td><span data-ttu-id="e4d85-231">HR</span><span class="sxs-lookup"><span data-stu-id="e4d85-231">HR</span></span></td>
<td><span data-ttu-id="e4d85-232">1 000</span><span class="sxs-lookup"><span data-stu-id="e4d85-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-233">CC002</span><span class="sxs-lookup"><span data-stu-id="e4d85-233">CC002</span></span></td>
<td><span data-ttu-id="e4d85-234">Finance</span><span class="sxs-lookup"><span data-stu-id="e4d85-234">Finance</span></span></td>
<td><span data-ttu-id="e4d85-235">6,000</span><span class="sxs-lookup"><span data-stu-id="e4d85-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-236">CC003</span><span class="sxs-lookup"><span data-stu-id="e4d85-236">CC003</span></span></td>
<td><span data-ttu-id="e4d85-237">Sestavení</span><span class="sxs-lookup"><span data-stu-id="e4d85-237">Assembly</span></span></td>
<td><span data-ttu-id="e4d85-238">0</span><span class="sxs-lookup"><span data-stu-id="e4d85-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e4d85-239">Následující tabulka zobrazuje výsledek při použití elektrické spotřeby jako základu přidělení pro variabilní náklady.</span><span class="sxs-lookup"><span data-stu-id="e4d85-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4d85-240">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-240">Cost object</span></span></th>
<th><span data-ttu-id="e4d85-241">Hodnota</span><span class="sxs-lookup"><span data-stu-id="e4d85-241">Magnitude</span></span></th>
<th><span data-ttu-id="e4d85-242">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="e4d85-242">Allocation factor</span></span></th>
<th><span data-ttu-id="e4d85-243">Částka</span><span class="sxs-lookup"><span data-stu-id="e4d85-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4d85-244">CC001</span><span class="sxs-lookup"><span data-stu-id="e4d85-244">CC001</span></span></td>
<td><span data-ttu-id="e4d85-245">HR</span><span class="sxs-lookup"><span data-stu-id="e4d85-245">HR</span></span></td>
<td><span data-ttu-id="e4d85-246">1 000</span><span class="sxs-lookup"><span data-stu-id="e4d85-246">1,000</span></span></td>
<td><span data-ttu-id="e4d85-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="e4d85-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="e4d85-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-249">CC002</span><span class="sxs-lookup"><span data-stu-id="e4d85-249">CC002</span></span></td>
<td><span data-ttu-id="e4d85-250">Finance</span><span class="sxs-lookup"><span data-stu-id="e4d85-250">Finance</span></span></td>
<td><span data-ttu-id="e4d85-251">6,000</span><span class="sxs-lookup"><span data-stu-id="e4d85-251">6,000</span></span></td>
<td><span data-ttu-id="e4d85-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="e4d85-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="e4d85-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-254">CC003</span><span class="sxs-lookup"><span data-stu-id="e4d85-254">CC003</span></span></td>
<td><span data-ttu-id="e4d85-255">Sestavení</span><span class="sxs-lookup"><span data-stu-id="e4d85-255">Assembly</span></span></td>
<td><span data-ttu-id="e4d85-256">0</span><span class="sxs-lookup"><span data-stu-id="e4d85-256">0</span></span></td>
<td><span data-ttu-id="e4d85-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="e4d85-258">0,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e4d85-259">Pevné náklady musí být distribuovány rovnoměrně k jednotlivých objektům nákladů, které spotřebovávaly elektřinu.</span><span class="sxs-lookup"><span data-stu-id="e4d85-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="e4d85-260">Tohoto výsledku můžete dosáhnout pomocí členu statistické dimenze Elektřina v základu přidělení vzorce: (Elektřina &gt; 0,00) Následující tabulka zobrazuje výsledek při použití elektrické spotřeby jako základu přidělení pro variabilní náklady.</span><span class="sxs-lookup"><span data-stu-id="e4d85-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4d85-261">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-261">Cost object</span></span></th>
<th><span data-ttu-id="e4d85-262">Vzorec</span><span class="sxs-lookup"><span data-stu-id="e4d85-262">Formula</span></span></th>
<th><span data-ttu-id="e4d85-263">Hodnota</span><span class="sxs-lookup"><span data-stu-id="e4d85-263">Magnitude</span></span></th>
<th><span data-ttu-id="e4d85-264">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="e4d85-264">Allocation factor</span></span></th>
<th><span data-ttu-id="e4d85-265">Částka</span><span class="sxs-lookup"><span data-stu-id="e4d85-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4d85-266">CC001</span><span class="sxs-lookup"><span data-stu-id="e4d85-266">CC001</span></span></td>
<td><span data-ttu-id="e4d85-267">HR</span><span class="sxs-lookup"><span data-stu-id="e4d85-267">HR</span></span></td>
<td><span data-ttu-id="e4d85-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="e4d85-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="e4d85-269">1</span><span class="sxs-lookup"><span data-stu-id="e4d85-269">1</span></span></td>
<td><span data-ttu-id="e4d85-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="e4d85-271">500.00</span><span class="sxs-lookup"><span data-stu-id="e4d85-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-272">CC002</span><span class="sxs-lookup"><span data-stu-id="e4d85-272">CC002</span></span></td>
<td><span data-ttu-id="e4d85-273">Finance</span><span class="sxs-lookup"><span data-stu-id="e4d85-273">Finance</span></span></td>
<td><span data-ttu-id="e4d85-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="e4d85-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="e4d85-275">1</span><span class="sxs-lookup"><span data-stu-id="e4d85-275">1</span></span></td>
<td><span data-ttu-id="e4d85-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="e4d85-277">500.00</span><span class="sxs-lookup"><span data-stu-id="e4d85-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-278">CC003</span><span class="sxs-lookup"><span data-stu-id="e4d85-278">CC003</span></span></td>
<td><span data-ttu-id="e4d85-279">Sestavení</span><span class="sxs-lookup"><span data-stu-id="e4d85-279">Assembly</span></span></td>
<td><span data-ttu-id="e4d85-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="e4d85-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="e4d85-281">0</span><span class="sxs-lookup"><span data-stu-id="e4d85-281">0</span></span></td>
<td><span data-ttu-id="e4d85-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="e4d85-283">0,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="e4d85-284">Deník</span><span class="sxs-lookup"><span data-stu-id="e4d85-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e4d85-285">Deník</span><span class="sxs-lookup"><span data-stu-id="e4d85-285">Journal</span></span></th>
<th><span data-ttu-id="e4d85-286">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="e4d85-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e4d85-287">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="e4d85-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e4d85-288">Verze</span><span class="sxs-lookup"><span data-stu-id="e4d85-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4d85-289">00002</span><span class="sxs-lookup"><span data-stu-id="e4d85-289">00002</span></span></td>
<td><span data-ttu-id="e4d85-290">Deník výpočtu distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="e4d85-291">Fiskální</span><span class="sxs-lookup"><span data-stu-id="e4d85-291">Fiscal</span></span></td>
<td><span data-ttu-id="e4d85-292">2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-292">2017</span></span></td>
<td><span data-ttu-id="e4d85-293">Období 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-293">Period 1</span></span></td>
<td><span data-ttu-id="e4d85-294">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="e4d85-295">Položky deníku (Položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="e4d85-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e4d85-296">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="e4d85-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e4d85-297">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e4d85-298">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-298">Cost element</span></span></th>
<th><span data-ttu-id="e4d85-299">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-299">Cost behavior</span></span></th>
<th><span data-ttu-id="e4d85-300">Částka</span><span class="sxs-lookup"><span data-stu-id="e4d85-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4d85-301">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4d85-302">CC099</span><span class="sxs-lookup"><span data-stu-id="e4d85-302">CC099</span></span></td>
<td><span data-ttu-id="e4d85-303">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="e4d85-303">Default cost center</span></span></td>
<td><span data-ttu-id="e4d85-304">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-304">10001</span></span></td>
<td><span data-ttu-id="e4d85-305">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-305">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-306">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-306">Fixed cost</span></span></td>
<td><span data-ttu-id="e4d85-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-308">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4d85-309">CC099</span><span class="sxs-lookup"><span data-stu-id="e4d85-309">CC099</span></span></td>
<td><span data-ttu-id="e4d85-310">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="e4d85-310">Default cost center</span></span></td>
<td><span data-ttu-id="e4d85-311">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-311">10001</span></span></td>
<td><span data-ttu-id="e4d85-312">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-312">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-313">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-313">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="e4d85-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e4d85-315">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4d85-316">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e4d85-317">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-317">Cost element</span></span></th>
<th><span data-ttu-id="e4d85-318">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-318">Cost behavior</span></span></th>
<th><span data-ttu-id="e4d85-319">Částka</span><span class="sxs-lookup"><span data-stu-id="e4d85-319">Amount</span></span></th>
<th><span data-ttu-id="e4d85-320">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="e4d85-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4d85-321">CC099</span><span class="sxs-lookup"><span data-stu-id="e4d85-321">CC099</span></span></td>
<td><span data-ttu-id="e4d85-322">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="e4d85-322">Default cost center</span></span></td>
<td><span data-ttu-id="e4d85-323">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-323">10001</span></span></td>
<td><span data-ttu-id="e4d85-324">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-324">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-325">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-325">Fixed cost</span></span></td>
<td><span data-ttu-id="e4d85-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-326">-1,000.00</span></span></td>
<td><span data-ttu-id="e4d85-327">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-328">CC001</span><span class="sxs-lookup"><span data-stu-id="e4d85-328">CC001</span></span></td>
<td><span data-ttu-id="e4d85-329">HR</span><span class="sxs-lookup"><span data-stu-id="e4d85-329">HR</span></span></td>
<td><span data-ttu-id="e4d85-330">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-330">10001</span></span></td>
<td><span data-ttu-id="e4d85-331">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-331">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-332">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-332">Fixed cost</span></span></td>
<td><span data-ttu-id="e4d85-333">500.00</span><span class="sxs-lookup"><span data-stu-id="e4d85-333">500.00</span></span></td>
<td><span data-ttu-id="e4d85-334">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-335">CC002</span><span class="sxs-lookup"><span data-stu-id="e4d85-335">CC002</span></span></td>
<td><span data-ttu-id="e4d85-336">Finance</span><span class="sxs-lookup"><span data-stu-id="e4d85-336">Finance</span></span></td>
<td><span data-ttu-id="e4d85-337">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-337">10001</span></span></td>
<td><span data-ttu-id="e4d85-338">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-338">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-339">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-339">Fixed cost</span></span></td>
<td><span data-ttu-id="e4d85-340">500.00</span><span class="sxs-lookup"><span data-stu-id="e4d85-340">500.00</span></span></td>
<td><span data-ttu-id="e4d85-341">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-342">CC099</span><span class="sxs-lookup"><span data-stu-id="e4d85-342">CC099</span></span></td>
<td><span data-ttu-id="e4d85-343">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="e4d85-343">Default cost center</span></span></td>
<td><span data-ttu-id="e4d85-344">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-344">10001</span></span></td>
<td><span data-ttu-id="e4d85-345">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-345">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-346">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-346">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-347">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-347">-9,000.00</span></span></td>
<td><span data-ttu-id="e4d85-348">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-349">CC001</span><span class="sxs-lookup"><span data-stu-id="e4d85-349">CC001</span></span></td>
<td><span data-ttu-id="e4d85-350">HR</span><span class="sxs-lookup"><span data-stu-id="e4d85-350">HR</span></span></td>
<td><span data-ttu-id="e4d85-351">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-351">10001</span></span></td>
<td><span data-ttu-id="e4d85-352">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-352">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-353">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-353">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="e4d85-354">1,285.71</span></span></td>
<td><span data-ttu-id="e4d85-355">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-356">CC002</span><span class="sxs-lookup"><span data-stu-id="e4d85-356">CC002</span></span></td>
<td><span data-ttu-id="e4d85-357">Finance</span><span class="sxs-lookup"><span data-stu-id="e4d85-357">Finance</span></span></td>
<td><span data-ttu-id="e4d85-358">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-358">10001</span></span></td>
<td><span data-ttu-id="e4d85-359">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-359">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-360">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-360">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="e4d85-361">7,714.29</span></span></td>
<td><span data-ttu-id="e4d85-362">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e4d85-363">Více informací naleznete v tématu [Vytvoření a přiřazení zásad distribuce nákladů k jednotce řízení nákladů](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="e4d85-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="e4d85-364">Krok 3: Zpracování výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="e4d85-365">Režijní náklady se používají k účtování jednoho nebo více konkrétních objektů nákladů.</span><span class="sxs-lookup"><span data-stu-id="e4d85-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="e4d85-366">Účtování je založeno na předem určené nákladové sazbě a množství z přiřazeného základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="e4d85-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="e4d85-367">Definice sazby režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-367">Define the overhead rate</span></span>

<span data-ttu-id="e4d85-368">Objekt nákladů CC001 HR přispívá k sadě interních projektů.</span><span class="sxs-lookup"><span data-stu-id="e4d85-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="e4d85-369">Vytvoří se člen statistické dimenzi s názvem projekty lidských zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="e4d85-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4d85-370">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-370">Cost object</span></span></th>
<th><span data-ttu-id="e4d85-371">Pracovní doba</span><span class="sxs-lookup"><span data-stu-id="e4d85-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4d85-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-372">Proj 1</span></span></td>
<td><span data-ttu-id="e4d85-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-373">Project 1</span></span></td>
<td><span data-ttu-id="e4d85-374">3</span><span class="sxs-lookup"><span data-stu-id="e4d85-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-375">Proj 2</span></span></td>
<td><span data-ttu-id="e4d85-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-376">Project 2</span></span></td>
<td><span data-ttu-id="e4d85-377">1</span><span class="sxs-lookup"><span data-stu-id="e4d85-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e4d85-378">Byla definována předem určená nákladová sazba pro příspěvky k nákladovým projektům.</span><span class="sxs-lookup"><span data-stu-id="e4d85-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4d85-379">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-379">Cost object</span></span></th>
<th><span data-ttu-id="e4d85-380">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-380">Cost element</span></span></th>
<th><span data-ttu-id="e4d85-381">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-381">Cost behavior</span></span></th>
<th><span data-ttu-id="e4d85-382">Jednotky</span><span class="sxs-lookup"><span data-stu-id="e4d85-382">Units</span></span></th>
<th><span data-ttu-id="e4d85-383">Kurz</span><span class="sxs-lookup"><span data-stu-id="e4d85-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4d85-384">CC001</span><span class="sxs-lookup"><span data-stu-id="e4d85-384">CC001</span></span></td>
<td><span data-ttu-id="e4d85-385">HR</span><span class="sxs-lookup"><span data-stu-id="e4d85-385">HR</span></span></td>
<td><span data-ttu-id="e4d85-386">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-386">10001</span></span></td>
<td><span data-ttu-id="e4d85-387">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-387">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-388">1</span><span class="sxs-lookup"><span data-stu-id="e4d85-388">1</span></span></td>
<td><span data-ttu-id="e4d85-389">10</span><span class="sxs-lookup"><span data-stu-id="e4d85-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e4d85-390">Následující tabulka zobrazuje výsledek při použití projektů lidských zdrojů jako základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="e4d85-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4d85-391">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-391">Cost object</span></span></th>
<th><span data-ttu-id="e4d85-392">Hodnota</span><span class="sxs-lookup"><span data-stu-id="e4d85-392">Magnitude</span></span></th>
<th><span data-ttu-id="e4d85-393">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-393">Cost element</span></span></th>
<th><span data-ttu-id="e4d85-394">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="e4d85-394">Allocation factor</span></span></th>
<th><span data-ttu-id="e4d85-395">Částka</span><span class="sxs-lookup"><span data-stu-id="e4d85-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4d85-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-396">Proj 1</span></span></td>
<td><span data-ttu-id="e4d85-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-397">Project 1</span></span></td>
<td><span data-ttu-id="e4d85-398">3</span><span class="sxs-lookup"><span data-stu-id="e4d85-398">3</span></span></td>
<td><span data-ttu-id="e4d85-399">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-399">10001</span></span></td>
<td><span data-ttu-id="e4d85-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="e4d85-401">30.00</span><span class="sxs-lookup"><span data-stu-id="e4d85-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-402">Proj 2</span></span></td>
<td><span data-ttu-id="e4d85-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-403">Project 2</span></span></td>
<td><span data-ttu-id="e4d85-404">1</span><span class="sxs-lookup"><span data-stu-id="e4d85-404">1</span></span></td>
<td><span data-ttu-id="e4d85-405">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-405">10001</span></span></td>
<td><span data-ttu-id="e4d85-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="e4d85-407">10,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="e4d85-408">Deník</span><span class="sxs-lookup"><span data-stu-id="e4d85-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e4d85-409">Deník</span><span class="sxs-lookup"><span data-stu-id="e4d85-409">Journal</span></span></th>
<th><span data-ttu-id="e4d85-410">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="e4d85-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e4d85-411">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="e4d85-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e4d85-412">Verze</span><span class="sxs-lookup"><span data-stu-id="e4d85-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4d85-413">00003</span><span class="sxs-lookup"><span data-stu-id="e4d85-413">00003</span></span></td>
<td><span data-ttu-id="e4d85-414">Deník výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="e4d85-415">Fiskální</span><span class="sxs-lookup"><span data-stu-id="e4d85-415">Fiscal</span></span></td>
<td><span data-ttu-id="e4d85-416">2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-416">2017</span></span></td>
<td><span data-ttu-id="e4d85-417">Období 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-417">Period 1</span></span></td>
<td><span data-ttu-id="e4d85-418">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="e4d85-419">Položky deníku (položky deníku pro výpočet sazby režijních nákladů)</span><span class="sxs-lookup"><span data-stu-id="e4d85-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e4d85-420">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="e4d85-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e4d85-421">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-421">Cost object</span></span></th>
<th><span data-ttu-id="e4d85-422">Hodnota</span><span class="sxs-lookup"><span data-stu-id="e4d85-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4d85-423">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4d85-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-424">Proj 1</span></span></td>
<td><span data-ttu-id="e4d85-425">Interní projekt 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="e4d85-426">3,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-427">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4d85-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-428">Proj 2</span></span></td>
<td><span data-ttu-id="e4d85-429">Interní projekt 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="e4d85-430">1.00</span><span class="sxs-lookup"><span data-stu-id="e4d85-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e4d85-431">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4d85-432">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e4d85-433">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-433">Cost element</span></span></th>
<th><span data-ttu-id="e4d85-434">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-434">Cost behavior</span></span></th>
<th><span data-ttu-id="e4d85-435">Částka</span><span class="sxs-lookup"><span data-stu-id="e4d85-435">Amount</span></span></th>
<th><span data-ttu-id="e4d85-436">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="e4d85-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4d85-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="e4d85-437">CC0001</span></span></td>
<td><span data-ttu-id="e4d85-438">HR</span><span class="sxs-lookup"><span data-stu-id="e4d85-438">HR</span></span></td>
<td><span data-ttu-id="e4d85-439">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-439">10001</span></span></td>
<td><span data-ttu-id="e4d85-440">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-440">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-441">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-441">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-442">-30.00</span></span></td>
<td><span data-ttu-id="e4d85-443">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-444">Proj 1</span></span></td>
<td><span data-ttu-id="e4d85-445">Interní projekt 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="e4d85-446">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-446">10001</span></span></td>
<td><span data-ttu-id="e4d85-447">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-447">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-448">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-448">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-449">30.00</span><span class="sxs-lookup"><span data-stu-id="e4d85-449">30.00</span></span></td>
<td><span data-ttu-id="e4d85-450">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-451">CC001</span><span class="sxs-lookup"><span data-stu-id="e4d85-451">CC001</span></span></td>
<td><span data-ttu-id="e4d85-452">HR</span><span class="sxs-lookup"><span data-stu-id="e4d85-452">HR</span></span></td>
<td><span data-ttu-id="e4d85-453">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-453">10001</span></span></td>
<td><span data-ttu-id="e4d85-454">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-454">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-455">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-455">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-456">-10.00</span></span></td>
<td><span data-ttu-id="e4d85-457">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-458">Proj 2</span></span></td>
<td><span data-ttu-id="e4d85-459">Interní projekt 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="e4d85-460">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-460">10001</span></span></td>
<td><span data-ttu-id="e4d85-461">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-461">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-462">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-462">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-463">10.00</span><span class="sxs-lookup"><span data-stu-id="e4d85-463">10.00</span></span></td>
<td><span data-ttu-id="e4d85-464">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e4d85-465">Další informace naleznete v tématu [Provedení výpočtu režijních nákladů](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="e4d85-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="e4d85-466">Krok 4: Zpracování výpočtu přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="e4d85-467">Přidělení se používá k přidělení zůstatku objektu nákladů do jiných objektů nákladů použitím základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="e4d85-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="e4d85-468">Aplikace Finance podporuje reciproční metodu přidělování.</span><span class="sxs-lookup"><span data-stu-id="e4d85-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="e4d85-469">V metodě vzájemného přidělení jsou plně rozpoznány vzájemné služby, které si vyměňují pomocné objekty nákladů.</span><span class="sxs-lookup"><span data-stu-id="e4d85-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="e4d85-470">Systém automaticky určí provádění přidělení ve správném pořadí.</span><span class="sxs-lookup"><span data-stu-id="e4d85-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="e4d85-471">Zůstatek objektu nákladů je přidělen jedním základem přidělení.</span><span class="sxs-lookup"><span data-stu-id="e4d85-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="e4d85-472">Je podporováno přidělování napříč dimenzemi objektů nákladů a jejich příslušných členů.</span><span class="sxs-lookup"><span data-stu-id="e4d85-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="e4d85-473">Pořadí přidělení je řízeno jednotkou řízení nákladů.</span><span class="sxs-lookup"><span data-stu-id="e4d85-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="e4d85-474">[![Reciproční metoda](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="e4d85-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="e4d85-475">Definice přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-475">Define the cost allocation</span></span>

<span data-ttu-id="e4d85-476">Toto je jednoduchý příklad, který vysvětluje, jakým způsobem lze sledovat tok nákladů.</span><span class="sxs-lookup"><span data-stu-id="e4d85-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="e4d85-477">Objekt nákladů objektu CC001 HR přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="e4d85-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="e4d85-478">Vytvoří se člen statistické dimenzi s názvem služby lidských zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="e4d85-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4d85-479">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-479">Cost object</span></span></th>
<th><span data-ttu-id="e4d85-480">Služby HR</span><span class="sxs-lookup"><span data-stu-id="e4d85-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4d85-481">CC002</span><span class="sxs-lookup"><span data-stu-id="e4d85-481">CC002</span></span></td>
<td><span data-ttu-id="e4d85-482">Finance</span><span class="sxs-lookup"><span data-stu-id="e4d85-482">Finance</span></span></td>
<td><span data-ttu-id="e4d85-483">35</span><span class="sxs-lookup"><span data-stu-id="e4d85-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-484">CC003</span><span class="sxs-lookup"><span data-stu-id="e4d85-484">CC003</span></span></td>
<td><span data-ttu-id="e4d85-485">Sestavení</span><span class="sxs-lookup"><span data-stu-id="e4d85-485">Assembly</span></span></td>
<td><span data-ttu-id="e4d85-486">55</span><span class="sxs-lookup"><span data-stu-id="e4d85-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-487">CC004</span><span class="sxs-lookup"><span data-stu-id="e4d85-487">CC004</span></span></td>
<td><span data-ttu-id="e4d85-488">Balení</span><span class="sxs-lookup"><span data-stu-id="e4d85-488">Packaging</span></span></td>
<td><span data-ttu-id="e4d85-489">10</span><span class="sxs-lookup"><span data-stu-id="e4d85-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e4d85-490">Objekt nákladů objektu CC002 Finance přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="e4d85-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="e4d85-491">Vytvoří se člen statistické dimenzi s názvem Finanční služby k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="e4d85-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4d85-492">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-492">Cost object</span></span></th>
<th><span data-ttu-id="e4d85-493">Finanční služby</span><span class="sxs-lookup"><span data-stu-id="e4d85-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4d85-494">CC003</span><span class="sxs-lookup"><span data-stu-id="e4d85-494">CC003</span></span></td>
<td><span data-ttu-id="e4d85-495">Sestavení</span><span class="sxs-lookup"><span data-stu-id="e4d85-495">Assembly</span></span></td>
<td><span data-ttu-id="e4d85-496">65</span><span class="sxs-lookup"><span data-stu-id="e4d85-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-497">CC004</span><span class="sxs-lookup"><span data-stu-id="e4d85-497">CC004</span></span></td>
<td><span data-ttu-id="e4d85-498">Balení</span><span class="sxs-lookup"><span data-stu-id="e4d85-498">Packaging</span></span></td>
<td><span data-ttu-id="e4d85-499">35</span><span class="sxs-lookup"><span data-stu-id="e4d85-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e4d85-500">Objekt nákladů objektu CC003 Sestavení přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="e4d85-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="e4d85-501">Vytvoří se člen statistické dimenzi s názvem Služby sestavení zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="e4d85-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4d85-502">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-502">Cost object</span></span></th>
<th><span data-ttu-id="e4d85-503">Služby sestavení (v hodinách)</span><span class="sxs-lookup"><span data-stu-id="e4d85-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4d85-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-504">Prod 1</span></span></td>
<td><span data-ttu-id="e4d85-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-505">Product 1</span></span></td>
<td><span data-ttu-id="e4d85-506">60</span><span class="sxs-lookup"><span data-stu-id="e4d85-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-507">Prod 2</span></span></td>
<td><span data-ttu-id="e4d85-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-508">Product 2</span></span></td>
<td><span data-ttu-id="e4d85-509">20</span><span class="sxs-lookup"><span data-stu-id="e4d85-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e4d85-510">Objekt nákladů objektu CC004 Balení přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="e4d85-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="e4d85-511">Vytvoří se člen statistické dimenzi s názvem Služby balení k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="e4d85-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4d85-512">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-512">Cost object</span></span></th>
<th><span data-ttu-id="e4d85-513">Služby balení (v hodinách)</span><span class="sxs-lookup"><span data-stu-id="e4d85-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4d85-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-514">Prod 1</span></span></td>
<td><span data-ttu-id="e4d85-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-515">Product 1</span></span></td>
<td><span data-ttu-id="e4d85-516">80</span><span class="sxs-lookup"><span data-stu-id="e4d85-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-517">Prod 2</span></span></td>
<td><span data-ttu-id="e4d85-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-518">Product 2</span></span></td>
<td><span data-ttu-id="e4d85-519">15</span><span class="sxs-lookup"><span data-stu-id="e4d85-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="e4d85-520">Statistická měření, jako je například výrobní doba spotřebovaná produktem, lze odvodit z datového zdroje.</span><span class="sxs-lookup"><span data-stu-id="e4d85-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="e4d85-521">Více informací naleznete v části [Šablona poskytovatele statistického měření](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="e4d85-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="e4d85-522">V následující tabulce je uveden výsledek při použití služeb HR jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="e4d85-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4d85-523">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-523">Cost object</span></span></th>
<th><span data-ttu-id="e4d85-524">Hodnota</span><span class="sxs-lookup"><span data-stu-id="e4d85-524">Magnitude</span></span></th>
<th><span data-ttu-id="e4d85-525">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="e4d85-525">Allocation factor</span></span></th>
<th><span data-ttu-id="e4d85-526">Částka</span><span class="sxs-lookup"><span data-stu-id="e4d85-526">Amount</span></span></th>
<th><span data-ttu-id="e4d85-527">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4d85-528">CC002</span><span class="sxs-lookup"><span data-stu-id="e4d85-528">CC002</span></span></td>
<td><span data-ttu-id="e4d85-529">Finance</span><span class="sxs-lookup"><span data-stu-id="e4d85-529">Finance</span></span></td>
<td><span data-ttu-id="e4d85-530">35</span><span class="sxs-lookup"><span data-stu-id="e4d85-530">35</span></span></td>
<td><span data-ttu-id="e4d85-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="e4d85-532">175.00</span><span class="sxs-lookup"><span data-stu-id="e4d85-532">175.00</span></span></td>
<td><span data-ttu-id="e4d85-533">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-534">CC003</span><span class="sxs-lookup"><span data-stu-id="e4d85-534">CC003</span></span></td>
<td><span data-ttu-id="e4d85-535">Sestavení</span><span class="sxs-lookup"><span data-stu-id="e4d85-535">Assembly</span></span></td>
<td><span data-ttu-id="e4d85-536">55</span><span class="sxs-lookup"><span data-stu-id="e4d85-536">55</span></span></td>
<td><span data-ttu-id="e4d85-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="e4d85-538">275.00</span><span class="sxs-lookup"><span data-stu-id="e4d85-538">275.00</span></span></td>
<td><span data-ttu-id="e4d85-539">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-540">CC004</span><span class="sxs-lookup"><span data-stu-id="e4d85-540">CC004</span></span></td>
<td><span data-ttu-id="e4d85-541">Balení</span><span class="sxs-lookup"><span data-stu-id="e4d85-541">Packaging</span></span></td>
<td><span data-ttu-id="e4d85-542">10</span><span class="sxs-lookup"><span data-stu-id="e4d85-542">10</span></span></td>
<td><span data-ttu-id="e4d85-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="e4d85-544">50,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-544">50.00</span></span></td>
<td><span data-ttu-id="e4d85-545">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-546">CC002</span><span class="sxs-lookup"><span data-stu-id="e4d85-546">CC002</span></span></td>
<td><span data-ttu-id="e4d85-547">Finance</span><span class="sxs-lookup"><span data-stu-id="e4d85-547">Finance</span></span></td>
<td><span data-ttu-id="e4d85-548">35</span><span class="sxs-lookup"><span data-stu-id="e4d85-548">35</span></span></td>
<td><span data-ttu-id="e4d85-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="e4d85-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="e4d85-550">436.00</span><span class="sxs-lookup"><span data-stu-id="e4d85-550">436.00</span></span></td>
<td><span data-ttu-id="e4d85-551">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-552">CC003</span><span class="sxs-lookup"><span data-stu-id="e4d85-552">CC003</span></span></td>
<td><span data-ttu-id="e4d85-553">Sestavení</span><span class="sxs-lookup"><span data-stu-id="e4d85-553">Assembly</span></span></td>
<td><span data-ttu-id="e4d85-554">55</span><span class="sxs-lookup"><span data-stu-id="e4d85-554">55</span></span></td>
<td><span data-ttu-id="e4d85-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="e4d85-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="e4d85-556">685.14</span><span class="sxs-lookup"><span data-stu-id="e4d85-556">685.14</span></span></td>
<td><span data-ttu-id="e4d85-557">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-558">CC004</span><span class="sxs-lookup"><span data-stu-id="e4d85-558">CC004</span></span></td>
<td><span data-ttu-id="e4d85-559">Balení</span><span class="sxs-lookup"><span data-stu-id="e4d85-559">Packaging</span></span></td>
<td><span data-ttu-id="e4d85-560">10</span><span class="sxs-lookup"><span data-stu-id="e4d85-560">10</span></span></td>
<td><span data-ttu-id="e4d85-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="e4d85-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="e4d85-562">124.57</span><span class="sxs-lookup"><span data-stu-id="e4d85-562">124.57</span></span></td>
<td><span data-ttu-id="e4d85-563">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e4d85-564">V následující tabulce je uveden výsledek při použití Finančních služeb Finance jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="e4d85-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4d85-565">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-565">Cost object</span></span></th>
<th><span data-ttu-id="e4d85-566">Hodnota</span><span class="sxs-lookup"><span data-stu-id="e4d85-566">Magnitude</span></span></th>
<th><span data-ttu-id="e4d85-567">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="e4d85-567">Allocation factor</span></span></th>
<th><span data-ttu-id="e4d85-568">Částka</span><span class="sxs-lookup"><span data-stu-id="e4d85-568">Amount</span></span></th>
<th><span data-ttu-id="e4d85-569">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4d85-570">CC003</span><span class="sxs-lookup"><span data-stu-id="e4d85-570">CC003</span></span></td>
<td><span data-ttu-id="e4d85-571">Sestavení</span><span class="sxs-lookup"><span data-stu-id="e4d85-571">Assembly</span></span></td>
<td><span data-ttu-id="e4d85-572">65</span><span class="sxs-lookup"><span data-stu-id="e4d85-572">65</span></span></td>
<td><span data-ttu-id="e4d85-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="e4d85-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="e4d85-574">438.75</span><span class="sxs-lookup"><span data-stu-id="e4d85-574">438.75</span></span></td>
<td><span data-ttu-id="e4d85-575">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-576">CC004</span><span class="sxs-lookup"><span data-stu-id="e4d85-576">CC004</span></span></td>
<td><span data-ttu-id="e4d85-577">Balení</span><span class="sxs-lookup"><span data-stu-id="e4d85-577">Packaging</span></span></td>
<td><span data-ttu-id="e4d85-578">35</span><span class="sxs-lookup"><span data-stu-id="e4d85-578">35</span></span></td>
<td><span data-ttu-id="e4d85-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="e4d85-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="e4d85-580">236.25</span><span class="sxs-lookup"><span data-stu-id="e4d85-580">236.25</span></span></td>
<td><span data-ttu-id="e4d85-581">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-582">CC003</span><span class="sxs-lookup"><span data-stu-id="e4d85-582">CC003</span></span></td>
<td><span data-ttu-id="e4d85-583">Sestavení</span><span class="sxs-lookup"><span data-stu-id="e4d85-583">Assembly</span></span></td>
<td><span data-ttu-id="e4d85-584">65</span><span class="sxs-lookup"><span data-stu-id="e4d85-584">65</span></span></td>
<td><span data-ttu-id="e4d85-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="e4d85-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="e4d85-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="e4d85-586">5,297.69</span></span></td>
<td><span data-ttu-id="e4d85-587">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-588">CC004</span><span class="sxs-lookup"><span data-stu-id="e4d85-588">CC004</span></span></td>
<td><span data-ttu-id="e4d85-589">Balení</span><span class="sxs-lookup"><span data-stu-id="e4d85-589">Packaging</span></span></td>
<td><span data-ttu-id="e4d85-590">35</span><span class="sxs-lookup"><span data-stu-id="e4d85-590">35</span></span></td>
<td><span data-ttu-id="e4d85-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="e4d85-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="e4d85-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="e4d85-592">2,852.60</span></span></td>
<td><span data-ttu-id="e4d85-593">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e4d85-594">V následující tabulce je uveden výsledek při použití Služeb sestavení jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="e4d85-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4d85-595">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-595">Cost object</span></span></th>
<th><span data-ttu-id="e4d85-596">Hodnota</span><span class="sxs-lookup"><span data-stu-id="e4d85-596">Magnitude</span></span></th>
<th><span data-ttu-id="e4d85-597">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="e4d85-597">Allocation factor</span></span></th>
<th><span data-ttu-id="e4d85-598">Částka</span><span class="sxs-lookup"><span data-stu-id="e4d85-598">Amount</span></span></th>
<th><span data-ttu-id="e4d85-599">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4d85-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-600">Prod 1</span></span></td>
<td><span data-ttu-id="e4d85-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-601">Product 1</span></span></td>
<td><span data-ttu-id="e4d85-602">60</span><span class="sxs-lookup"><span data-stu-id="e4d85-602">60</span></span></td>
<td><span data-ttu-id="e4d85-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="e4d85-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="e4d85-604">535.31</span><span class="sxs-lookup"><span data-stu-id="e4d85-604">535.31</span></span></td>
<td><span data-ttu-id="e4d85-605">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-606">Prod 2</span></span></td>
<td><span data-ttu-id="e4d85-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-607">Product 2</span></span></td>
<td><span data-ttu-id="e4d85-608">20</span><span class="sxs-lookup"><span data-stu-id="e4d85-608">20</span></span></td>
<td><span data-ttu-id="e4d85-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="e4d85-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="e4d85-610">178.44</span><span class="sxs-lookup"><span data-stu-id="e4d85-610">178.44</span></span></td>
<td><span data-ttu-id="e4d85-611">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-612">Prod 1</span></span></td>
<td><span data-ttu-id="e4d85-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-613">Product 1</span></span></td>
<td><span data-ttu-id="e4d85-614">60</span><span class="sxs-lookup"><span data-stu-id="e4d85-614">60</span></span></td>
<td><span data-ttu-id="e4d85-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="e4d85-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="e4d85-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="e4d85-616">4,487.12</span></span></td>
<td><span data-ttu-id="e4d85-617">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-618">Prod 2</span></span></td>
<td><span data-ttu-id="e4d85-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-619">Product 2</span></span></td>
<td><span data-ttu-id="e4d85-620">20</span><span class="sxs-lookup"><span data-stu-id="e4d85-620">20</span></span></td>
<td><span data-ttu-id="e4d85-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="e4d85-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="e4d85-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="e4d85-622">1,495.71</span></span></td>
<td><span data-ttu-id="e4d85-623">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e4d85-624">V následující tabulce je uveden výsledek při použití Služeb balení jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="e4d85-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4d85-625">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-625">Cost object</span></span></th>
<th><span data-ttu-id="e4d85-626">Hodnota</span><span class="sxs-lookup"><span data-stu-id="e4d85-626">Magnitude</span></span></th>
<th><span data-ttu-id="e4d85-627">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="e4d85-627">Allocation factor</span></span></th>
<th><span data-ttu-id="e4d85-628">Částka</span><span class="sxs-lookup"><span data-stu-id="e4d85-628">Amount</span></span></th>
<th><span data-ttu-id="e4d85-629">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4d85-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-630">Prod 1</span></span></td>
<td><span data-ttu-id="e4d85-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-631">Product 1</span></span></td>
<td><span data-ttu-id="e4d85-632">80</span><span class="sxs-lookup"><span data-stu-id="e4d85-632">80</span></span></td>
<td><span data-ttu-id="e4d85-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="e4d85-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="e4d85-634">241.05</span><span class="sxs-lookup"><span data-stu-id="e4d85-634">241.05</span></span></td>
<td><span data-ttu-id="e4d85-635">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-636">Prod 2</span></span></td>
<td><span data-ttu-id="e4d85-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-637">Product 2</span></span></td>
<td><span data-ttu-id="e4d85-638">15</span><span class="sxs-lookup"><span data-stu-id="e4d85-638">15</span></span></td>
<td><span data-ttu-id="e4d85-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="e4d85-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="e4d85-640">45.20</span><span class="sxs-lookup"><span data-stu-id="e4d85-640">45.20</span></span></td>
<td><span data-ttu-id="e4d85-641">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-642">Prod 1</span></span></td>
<td><span data-ttu-id="e4d85-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-643">Product 1</span></span></td>
<td><span data-ttu-id="e4d85-644">80</span><span class="sxs-lookup"><span data-stu-id="e4d85-644">80</span></span></td>
<td><span data-ttu-id="e4d85-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="e4d85-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="e4d85-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="e4d85-646">2,507.09</span></span></td>
<td><span data-ttu-id="e4d85-647">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-648">Prod 2</span></span></td>
<td><span data-ttu-id="e4d85-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-649">Product 2</span></span></td>
<td><span data-ttu-id="e4d85-650">15</span><span class="sxs-lookup"><span data-stu-id="e4d85-650">15</span></span></td>
<td><span data-ttu-id="e4d85-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="e4d85-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="e4d85-652">470.08</span><span class="sxs-lookup"><span data-stu-id="e4d85-652">470.08</span></span></td>
<td><span data-ttu-id="e4d85-653">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="e4d85-654">Položky deníku (položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="e4d85-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e4d85-655">Deník</span><span class="sxs-lookup"><span data-stu-id="e4d85-655">Journal</span></span></th>
<th><span data-ttu-id="e4d85-656">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="e4d85-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e4d85-657">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="e4d85-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e4d85-658">Verze</span><span class="sxs-lookup"><span data-stu-id="e4d85-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4d85-659">00004</span><span class="sxs-lookup"><span data-stu-id="e4d85-659">00004</span></span></td>
<td><span data-ttu-id="e4d85-660">Deník přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="e4d85-661">Fiskální</span><span class="sxs-lookup"><span data-stu-id="e4d85-661">Fiscal</span></span></td>
<td><span data-ttu-id="e4d85-662">2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-662">2017</span></span></td>
<td><span data-ttu-id="e4d85-663">Období 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-663">Period 1</span></span></td>
<td><span data-ttu-id="e4d85-664">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="e4d85-665">Řádky deníku</span><span class="sxs-lookup"><span data-stu-id="e4d85-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e4d85-666">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="e4d85-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e4d85-667">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e4d85-668">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-668">Cost element</span></span></th>
<th><span data-ttu-id="e4d85-669">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-669">Cost behavior</span></span></th>
<th><span data-ttu-id="e4d85-670">Částka</span><span class="sxs-lookup"><span data-stu-id="e4d85-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4d85-671">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4d85-672">CC001</span><span class="sxs-lookup"><span data-stu-id="e4d85-672">CC001</span></span></td>
<td><span data-ttu-id="e4d85-673">HR</span><span class="sxs-lookup"><span data-stu-id="e4d85-673">HR</span></span></td>
<td><span data-ttu-id="e4d85-674">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-674">10001</span></span></td>
<td><span data-ttu-id="e4d85-675">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-675">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-676">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-676">Fixed cost</span></span></td>
<td><span data-ttu-id="e4d85-677">500.00</span><span class="sxs-lookup"><span data-stu-id="e4d85-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-678">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4d85-679">CC001</span><span class="sxs-lookup"><span data-stu-id="e4d85-679">CC001</span></span></td>
<td><span data-ttu-id="e4d85-680">HR</span><span class="sxs-lookup"><span data-stu-id="e4d85-680">HR</span></span></td>
<td><span data-ttu-id="e4d85-681">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-681">10001</span></span></td>
<td><span data-ttu-id="e4d85-682">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-682">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-683">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-683">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="e4d85-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-685">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4d85-686">CC002</span><span class="sxs-lookup"><span data-stu-id="e4d85-686">CC002</span></span></td>
<td><span data-ttu-id="e4d85-687">Finance</span><span class="sxs-lookup"><span data-stu-id="e4d85-687">Finance</span></span></td>
<td><span data-ttu-id="e4d85-688">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-688">10001</span></span></td>
<td><span data-ttu-id="e4d85-689">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-689">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-690">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-690">Fixed cost</span></span></td>
<td><span data-ttu-id="e4d85-691">675.00</span><span class="sxs-lookup"><span data-stu-id="e4d85-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-692">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4d85-693">CC002</span><span class="sxs-lookup"><span data-stu-id="e4d85-693">CC002</span></span></td>
<td><span data-ttu-id="e4d85-694">Finance</span><span class="sxs-lookup"><span data-stu-id="e4d85-694">Finance</span></span></td>
<td><span data-ttu-id="e4d85-695">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-695">10001</span></span></td>
<td><span data-ttu-id="e4d85-696">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-696">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-697">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-697">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="e4d85-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-699">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4d85-700">CC003</span><span class="sxs-lookup"><span data-stu-id="e4d85-700">CC003</span></span></td>
<td><span data-ttu-id="e4d85-701">Sestavení</span><span class="sxs-lookup"><span data-stu-id="e4d85-701">Assembly</span></span></td>
<td><span data-ttu-id="e4d85-702">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-702">10001</span></span></td>
<td><span data-ttu-id="e4d85-703">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-703">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-704">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-704">Fixed cost</span></span></td>
<td><span data-ttu-id="e4d85-705">713.75</span><span class="sxs-lookup"><span data-stu-id="e4d85-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-706">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4d85-707">CC003</span><span class="sxs-lookup"><span data-stu-id="e4d85-707">CC003</span></span></td>
<td><span data-ttu-id="e4d85-708">Sestavení</span><span class="sxs-lookup"><span data-stu-id="e4d85-708">Assembly</span></span></td>
<td><span data-ttu-id="e4d85-709">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-709">10001</span></span></td>
<td><span data-ttu-id="e4d85-710">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-710">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-711">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-711">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="e4d85-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-713">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4d85-714">CC003</span><span class="sxs-lookup"><span data-stu-id="e4d85-714">CC003</span></span></td>
<td><span data-ttu-id="e4d85-715">Balení</span><span class="sxs-lookup"><span data-stu-id="e4d85-715">Packaging</span></span></td>
<td><span data-ttu-id="e4d85-716">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-716">10001</span></span></td>
<td><span data-ttu-id="e4d85-717">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-717">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-718">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-718">Fixed cost</span></span></td>
<td><span data-ttu-id="e4d85-719">286.25</span><span class="sxs-lookup"><span data-stu-id="e4d85-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-720">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4d85-721">CC003</span><span class="sxs-lookup"><span data-stu-id="e4d85-721">CC003</span></span></td>
<td><span data-ttu-id="e4d85-722">Balení</span><span class="sxs-lookup"><span data-stu-id="e4d85-722">Packaging</span></span></td>
<td><span data-ttu-id="e4d85-723">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-723">10001</span></span></td>
<td><span data-ttu-id="e4d85-724">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-724">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-725">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-725">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="e4d85-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-727">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4d85-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-728">Prod 1</span></span></td>
<td><span data-ttu-id="e4d85-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-729">Product 1</span></span></td>
<td><span data-ttu-id="e4d85-730">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-730">10001</span></span></td>
<td><span data-ttu-id="e4d85-731">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-731">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-732">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-732">Fixed cost</span></span></td>
<td><span data-ttu-id="e4d85-733">776.36</span><span class="sxs-lookup"><span data-stu-id="e4d85-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-734">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4d85-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-735">Prod 1</span></span></td>
<td><span data-ttu-id="e4d85-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-736">Product 1</span></span></td>
<td><span data-ttu-id="e4d85-737">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-737">10001</span></span></td>
<td><span data-ttu-id="e4d85-738">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-738">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-739">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-739">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="e4d85-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-741">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4d85-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-742">Prod 2</span></span></td>
<td><span data-ttu-id="e4d85-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-743">Product 1</span></span></td>
<td><span data-ttu-id="e4d85-744">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-744">10001</span></span></td>
<td><span data-ttu-id="e4d85-745">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-745">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-746">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-746">Fixed cost</span></span></td>
<td><span data-ttu-id="e4d85-747">223.64</span><span class="sxs-lookup"><span data-stu-id="e4d85-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-748">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4d85-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-749">Prod 2</span></span></td>
<td><span data-ttu-id="e4d85-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-750">Product 1</span></span></td>
<td><span data-ttu-id="e4d85-751">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-751">10001</span></span></td>
<td><span data-ttu-id="e4d85-752">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-752">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-753">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-753">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="e4d85-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e4d85-755">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4d85-756">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e4d85-757">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-757">Cost element</span></span></th>
<th><span data-ttu-id="e4d85-758">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-758">Cost behavior</span></span></th>
<th><span data-ttu-id="e4d85-759">Částka</span><span class="sxs-lookup"><span data-stu-id="e4d85-759">Amount</span></span></th>
<th><span data-ttu-id="e4d85-760">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="e4d85-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4d85-761">CC001</span><span class="sxs-lookup"><span data-stu-id="e4d85-761">CC001</span></span></td>
<td><span data-ttu-id="e4d85-762">HR</span><span class="sxs-lookup"><span data-stu-id="e4d85-762">HR</span></span></td>
<td><span data-ttu-id="e4d85-763">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-763">10001</span></span></td>
<td><span data-ttu-id="e4d85-764">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-764">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-765">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-765">Fixed cost</span></span></td>
<td><span data-ttu-id="e4d85-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-766">-500.00</span></span></td>
<td><span data-ttu-id="e4d85-767">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-768">CC002</span><span class="sxs-lookup"><span data-stu-id="e4d85-768">CC002</span></span></td>
<td><span data-ttu-id="e4d85-769">Finance</span><span class="sxs-lookup"><span data-stu-id="e4d85-769">Finance</span></span></td>
<td><span data-ttu-id="e4d85-770">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-770">10001</span></span></td>
<td><span data-ttu-id="e4d85-771">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-771">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-772">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-772">Fixed cost</span></span></td>
<td><span data-ttu-id="e4d85-773">175.00</span><span class="sxs-lookup"><span data-stu-id="e4d85-773">175.00</span></span></td>
<td><span data-ttu-id="e4d85-774">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-775">CC003</span><span class="sxs-lookup"><span data-stu-id="e4d85-775">CC003</span></span></td>
<td><span data-ttu-id="e4d85-776">Sestavení</span><span class="sxs-lookup"><span data-stu-id="e4d85-776">Assembly</span></span></td>
<td><span data-ttu-id="e4d85-777">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-777">10001</span></span></td>
<td><span data-ttu-id="e4d85-778">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-778">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-779">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-779">Fixed cost</span></span></td>
<td><span data-ttu-id="e4d85-780">275.00</span><span class="sxs-lookup"><span data-stu-id="e4d85-780">275.00</span></span></td>
<td><span data-ttu-id="e4d85-781">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-782">CC004</span><span class="sxs-lookup"><span data-stu-id="e4d85-782">CC004</span></span></td>
<td><span data-ttu-id="e4d85-783">Balení</span><span class="sxs-lookup"><span data-stu-id="e4d85-783">Packaging</span></span></td>
<td><span data-ttu-id="e4d85-784">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-784">10001</span></span></td>
<td><span data-ttu-id="e4d85-785">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-785">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-786">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-786">Fixed cost</span></span></td>
<td><span data-ttu-id="e4d85-787">50,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-787">50,00</span></span></td>
<td><span data-ttu-id="e4d85-788">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-789">CC001</span><span class="sxs-lookup"><span data-stu-id="e4d85-789">CC001</span></span></td>
<td><span data-ttu-id="e4d85-790">HR</span><span class="sxs-lookup"><span data-stu-id="e4d85-790">HR</span></span></td>
<td><span data-ttu-id="e4d85-791">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-791">10001</span></span></td>
<td><span data-ttu-id="e4d85-792">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-792">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-793">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-793">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-794">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="e4d85-794">-1,245.71</span></span></td>
<td><span data-ttu-id="e4d85-795">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-796">CC002</span><span class="sxs-lookup"><span data-stu-id="e4d85-796">CC002</span></span></td>
<td><span data-ttu-id="e4d85-797">Finance</span><span class="sxs-lookup"><span data-stu-id="e4d85-797">Finance</span></span></td>
<td><span data-ttu-id="e4d85-798">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-798">10001</span></span></td>
<td><span data-ttu-id="e4d85-799">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-799">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-800">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-800">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-801">436.00</span><span class="sxs-lookup"><span data-stu-id="e4d85-801">436.00</span></span></td>
<td><span data-ttu-id="e4d85-802">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-803">CC003</span><span class="sxs-lookup"><span data-stu-id="e4d85-803">CC003</span></span></td>
<td><span data-ttu-id="e4d85-804">Sestavení</span><span class="sxs-lookup"><span data-stu-id="e4d85-804">Assembly</span></span></td>
<td><span data-ttu-id="e4d85-805">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-805">10001</span></span></td>
<td><span data-ttu-id="e4d85-806">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-806">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-807">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-807">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-808">685.14</span><span class="sxs-lookup"><span data-stu-id="e4d85-808">685.14</span></span></td>
<td><span data-ttu-id="e4d85-809">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-810">CC004</span><span class="sxs-lookup"><span data-stu-id="e4d85-810">CC004</span></span></td>
<td><span data-ttu-id="e4d85-811">Balení</span><span class="sxs-lookup"><span data-stu-id="e4d85-811">Packaging</span></span></td>
<td><span data-ttu-id="e4d85-812">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-812">10001</span></span></td>
<td><span data-ttu-id="e4d85-813">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-813">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-814">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-814">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-815">124.57</span><span class="sxs-lookup"><span data-stu-id="e4d85-815">124.57</span></span></td>
<td><span data-ttu-id="e4d85-816">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-817">CC002</span><span class="sxs-lookup"><span data-stu-id="e4d85-817">CC002</span></span></td>
<td><span data-ttu-id="e4d85-818">Finance</span><span class="sxs-lookup"><span data-stu-id="e4d85-818">Finance</span></span></td>
<td><span data-ttu-id="e4d85-819">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-819">10001</span></span></td>
<td><span data-ttu-id="e4d85-820">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-820">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-821">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-821">Fixed cost</span></span></td>
<td><span data-ttu-id="e4d85-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-822">-675.00</span></span></td>
<td><span data-ttu-id="e4d85-823">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-824">CC003</span><span class="sxs-lookup"><span data-stu-id="e4d85-824">CC003</span></span></td>
<td><span data-ttu-id="e4d85-825">Sestavení</span><span class="sxs-lookup"><span data-stu-id="e4d85-825">Assembly</span></span></td>
<td><span data-ttu-id="e4d85-826">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-826">10001</span></span></td>
<td><span data-ttu-id="e4d85-827">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-827">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-828">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-828">Fixed cost</span></span></td>
<td><span data-ttu-id="e4d85-829">438.75</span><span class="sxs-lookup"><span data-stu-id="e4d85-829">438.75</span></span></td>
<td><span data-ttu-id="e4d85-830">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-831">CC004</span><span class="sxs-lookup"><span data-stu-id="e4d85-831">CC004</span></span></td>
<td><span data-ttu-id="e4d85-832">Balení</span><span class="sxs-lookup"><span data-stu-id="e4d85-832">Packaging</span></span></td>
<td><span data-ttu-id="e4d85-833">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-833">10001</span></span></td>
<td><span data-ttu-id="e4d85-834">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-834">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-835">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-835">Fixed cost</span></span></td>
<td><span data-ttu-id="e4d85-836">236.25</span><span class="sxs-lookup"><span data-stu-id="e4d85-836">236.25</span></span></td>
<td><span data-ttu-id="e4d85-837">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-838">CC002</span><span class="sxs-lookup"><span data-stu-id="e4d85-838">CC002</span></span></td>
<td><span data-ttu-id="e4d85-839">Finance</span><span class="sxs-lookup"><span data-stu-id="e4d85-839">Finance</span></span></td>
<td><span data-ttu-id="e4d85-840">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-840">10001</span></span></td>
<td><span data-ttu-id="e4d85-841">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-841">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-842">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-842">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-843">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="e4d85-843">-8,150.29</span></span></td>
<td><span data-ttu-id="e4d85-844">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-845">CC003</span><span class="sxs-lookup"><span data-stu-id="e4d85-845">CC003</span></span></td>
<td><span data-ttu-id="e4d85-846">Sestavení</span><span class="sxs-lookup"><span data-stu-id="e4d85-846">Assembly</span></span></td>
<td><span data-ttu-id="e4d85-847">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-847">10001</span></span></td>
<td><span data-ttu-id="e4d85-848">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-848">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-849">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-849">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="e4d85-850">5,297.69</span></span></td>
<td><span data-ttu-id="e4d85-851">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-852">CC004</span><span class="sxs-lookup"><span data-stu-id="e4d85-852">CC004</span></span></td>
<td><span data-ttu-id="e4d85-853">Balení</span><span class="sxs-lookup"><span data-stu-id="e4d85-853">Packaging</span></span></td>
<td><span data-ttu-id="e4d85-854">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-854">10001</span></span></td>
<td><span data-ttu-id="e4d85-855">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-855">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-856">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-856">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="e4d85-857">2,852.60</span></span></td>
<td><span data-ttu-id="e4d85-858">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-859">CC003</span><span class="sxs-lookup"><span data-stu-id="e4d85-859">CC003</span></span></td>
<td><span data-ttu-id="e4d85-860">Sestavení</span><span class="sxs-lookup"><span data-stu-id="e4d85-860">Assembly</span></span></td>
<td><span data-ttu-id="e4d85-861">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-861">10001</span></span></td>
<td><span data-ttu-id="e4d85-862">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-862">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-863">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-863">Fixed cost</span></span></td>
<td><span data-ttu-id="e4d85-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="e4d85-864">-713.75</span></span></td>
<td><span data-ttu-id="e4d85-865">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-866">Prod 1</span></span></td>
<td><span data-ttu-id="e4d85-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-867">Product 1</span></span></td>
<td><span data-ttu-id="e4d85-868">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-868">10001</span></span></td>
<td><span data-ttu-id="e4d85-869">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-869">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-870">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-870">Fixed cost</span></span></td>
<td><span data-ttu-id="e4d85-871">535.31</span><span class="sxs-lookup"><span data-stu-id="e4d85-871">535.31</span></span></td>
<td><span data-ttu-id="e4d85-872">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-873">Prod 2</span></span></td>
<td><span data-ttu-id="e4d85-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-874">Product 2</span></span></td>
<td><span data-ttu-id="e4d85-875">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-875">10001</span></span></td>
<td><span data-ttu-id="e4d85-876">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-876">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-877">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-877">Fixed cost</span></span></td>
<td><span data-ttu-id="e4d85-878">178.44</span><span class="sxs-lookup"><span data-stu-id="e4d85-878">178.44</span></span></td>
<td><span data-ttu-id="e4d85-879">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-880">CC003</span><span class="sxs-lookup"><span data-stu-id="e4d85-880">CC003</span></span></td>
<td><span data-ttu-id="e4d85-881">Sestavení</span><span class="sxs-lookup"><span data-stu-id="e4d85-881">Assembly</span></span></td>
<td><span data-ttu-id="e4d85-882">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-882">10001</span></span></td>
<td><span data-ttu-id="e4d85-883">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-883">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-884">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-884">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-885">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="e4d85-885">-5,982.83</span></span></td>
<td><span data-ttu-id="e4d85-886">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-887">Prod 1</span></span></td>
<td><span data-ttu-id="e4d85-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-888">Product 1</span></span></td>
<td><span data-ttu-id="e4d85-889">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-889">10001</span></span></td>
<td><span data-ttu-id="e4d85-890">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-890">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-891">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-891">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="e4d85-892">4,487.12</span></span></td>
<td><span data-ttu-id="e4d85-893">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-894">Prod 2</span></span></td>
<td><span data-ttu-id="e4d85-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-895">Product 2</span></span></td>
<td><span data-ttu-id="e4d85-896">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-896">10001</span></span></td>
<td><span data-ttu-id="e4d85-897">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-897">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-898">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-898">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="e4d85-899">1,495.71</span></span></td>
<td><span data-ttu-id="e4d85-900">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-901">CC003</span><span class="sxs-lookup"><span data-stu-id="e4d85-901">CC003</span></span></td>
<td><span data-ttu-id="e4d85-902">Sestavení</span><span class="sxs-lookup"><span data-stu-id="e4d85-902">Assembly</span></span></td>
<td><span data-ttu-id="e4d85-903">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-903">10001</span></span></td>
<td><span data-ttu-id="e4d85-904">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-904">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-905">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-905">Fixed cost</span></span></td>
<td><span data-ttu-id="e4d85-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="e4d85-906">-286.25</span></span></td>
<td><span data-ttu-id="e4d85-907">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-908">Prod 1</span></span></td>
<td><span data-ttu-id="e4d85-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-909">Product 1</span></span></td>
<td><span data-ttu-id="e4d85-910">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-910">10001</span></span></td>
<td><span data-ttu-id="e4d85-911">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-911">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-912">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-912">Fixed cost</span></span></td>
<td><span data-ttu-id="e4d85-913">241.05</span><span class="sxs-lookup"><span data-stu-id="e4d85-913">241.05</span></span></td>
<td><span data-ttu-id="e4d85-914">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-915">Prod 2</span></span></td>
<td><span data-ttu-id="e4d85-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-916">Product 2</span></span></td>
<td><span data-ttu-id="e4d85-917">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-917">10001</span></span></td>
<td><span data-ttu-id="e4d85-918">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-918">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-919">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-919">Fixed cost</span></span></td>
<td><span data-ttu-id="e4d85-920">45.20</span><span class="sxs-lookup"><span data-stu-id="e4d85-920">45.20</span></span></td>
<td><span data-ttu-id="e4d85-921">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-922">CC003</span><span class="sxs-lookup"><span data-stu-id="e4d85-922">CC003</span></span></td>
<td><span data-ttu-id="e4d85-923">Sestavení</span><span class="sxs-lookup"><span data-stu-id="e4d85-923">Assembly</span></span></td>
<td><span data-ttu-id="e4d85-924">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-924">10001</span></span></td>
<td><span data-ttu-id="e4d85-925">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-925">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-926">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-926">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="e4d85-927">-2,977.17</span></span></td>
<td><span data-ttu-id="e4d85-928">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-929">Prod 1</span></span></td>
<td><span data-ttu-id="e4d85-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-930">Product 1</span></span></td>
<td><span data-ttu-id="e4d85-931">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-931">10001</span></span></td>
<td><span data-ttu-id="e4d85-932">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-932">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-933">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-933">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="e4d85-934">2,507.09</span></span></td>
<td><span data-ttu-id="e4d85-935">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4d85-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-936">Prod 2</span></span></td>
<td><span data-ttu-id="e4d85-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-937">Product 2</span></span></td>
<td><span data-ttu-id="e4d85-938">10001</span><span class="sxs-lookup"><span data-stu-id="e4d85-938">10001</span></span></td>
<td><span data-ttu-id="e4d85-939">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="e4d85-939">Electricity</span></span></td>
<td><span data-ttu-id="e4d85-940">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-940">Variable cost</span></span></td>
<td><span data-ttu-id="e4d85-941">470.08</span><span class="sxs-lookup"><span data-stu-id="e4d85-941">470.08</span></span></td>
<td><span data-ttu-id="e4d85-942">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="e4d85-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="e4d85-943">Závěr</span><span class="sxs-lookup"><span data-stu-id="e4d85-943">Conclusion</span></span>
<span data-ttu-id="e4d85-944">Ve finančním účtování se náklady za elektřinu ve výši 10 000 zaúčtují na ID fiktivního nákladového střediska.</span><span class="sxs-lookup"><span data-stu-id="e4d85-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="e4d85-945">Účetní tak budou vědět, že tento náklad musí být přidělen.</span><span class="sxs-lookup"><span data-stu-id="e4d85-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="e4d85-946">V nákladovém účetnictví náklady procházejí napříč organizačními jednotkami a úrovněmi, na základě použitých zásad a pravidel.</span><span class="sxs-lookup"><span data-stu-id="e4d85-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="e4d85-947">Každý náklad byl přidružen k základu přidělení, který poskytuje nejlepší hodnocení pro přidělení nákladů.</span><span class="sxs-lookup"><span data-stu-id="e4d85-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="e4d85-948">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="e4d85-949">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="e4d85-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="e4d85-950">Celkem</span><span class="sxs-lookup"><span data-stu-id="e4d85-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="e4d85-951">CC099</span><span class="sxs-lookup"><span data-stu-id="e4d85-951">CC099</span></span></th>
<th><span data-ttu-id="e4d85-952">CC001</span><span class="sxs-lookup"><span data-stu-id="e4d85-952">CC001</span></span></th>
<th><span data-ttu-id="e4d85-953">CC002</span><span class="sxs-lookup"><span data-stu-id="e4d85-953">CC002</span></span></th>
<th><span data-ttu-id="e4d85-954">CC003</span><span class="sxs-lookup"><span data-stu-id="e4d85-954">CC003</span></span></th>
<th><span data-ttu-id="e4d85-955">CC004</span><span class="sxs-lookup"><span data-stu-id="e4d85-955">CC004</span></span></th>
<th><span data-ttu-id="e4d85-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-956">Proj 1</span></span></th>
<th><span data-ttu-id="e4d85-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-957">Proj 2</span></span></th>
<th><span data-ttu-id="e4d85-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e4d85-958">Prod 1</span></span></th>
<th><span data-ttu-id="e4d85-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e4d85-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="e4d85-960">10001 Elektřina</span><span class="sxs-lookup"><span data-stu-id="e4d85-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4d85-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="e4d85-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4d85-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="e4d85-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4d85-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="e4d85-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4d85-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="e4d85-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="e4d85-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="e4d85-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4d85-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="e4d85-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4d85-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="e4d85-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4d85-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="e4d85-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4d85-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="e4d85-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="e4d85-970">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="e4d85-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4d85-971">0,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="e4d85-972">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4d85-973">0,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4d85-974">0,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4d85-975">0,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4d85-976">0,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4d85-977">0,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="e4d85-978">776.36</span><span class="sxs-lookup"><span data-stu-id="e4d85-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4d85-979">223.64</span><span class="sxs-lookup"><span data-stu-id="e4d85-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4d85-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="e4d85-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="e4d85-981">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="e4d85-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4d85-982">000</span><span class="sxs-lookup"><span data-stu-id="e4d85-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4d85-983">0,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4d85-984">0,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4d85-985">0,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4d85-986">0,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4d85-987">30.00</span><span class="sxs-lookup"><span data-stu-id="e4d85-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4d85-988">10,00</span><span class="sxs-lookup"><span data-stu-id="e4d85-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4d85-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="e4d85-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4d85-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="e4d85-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4d85-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="e4d85-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="e4d85-992">Toto téma popisuje, jak primární prvek nákladů, 10001 Elektřina, prochází přes objekty nákladů.</span><span class="sxs-lookup"><span data-stu-id="e4d85-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="e4d85-993">Tyto režijní náklady tedy budou přiděleny na nejnižší úroveň v organizaci.</span><span class="sxs-lookup"><span data-stu-id="e4d85-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="e4d85-994">Jinak řečeno, objekty nákladů na nejnižší úrovni ponesou náklady.</span><span class="sxs-lookup"><span data-stu-id="e4d85-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="e4d85-995">Chcete-li vizuální tok nákladů mezi objekty nákladů, můžete použít pravidla zásad shrnutí nákladů pro vizualizaci jejich toků.</span><span class="sxs-lookup"><span data-stu-id="e4d85-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="e4d85-996">Další informace naleznete v tématu [Zásady shrnutí nákladů a výpočet režijních nákladů](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="e4d85-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



