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
ms.openlocfilehash: 6c045f82f3288dba193721dd80c90e68750af9a7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176801"
---
# <a name="overhead-calculation"></a><span data-ttu-id="10de7-103">Výpočet režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="10de7-104">Toto téma popisuje typické procesy pro výpočet a přidělení režijních nákladů.</span><span class="sxs-lookup"><span data-stu-id="10de7-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="10de7-105">Definice termínu</span><span class="sxs-lookup"><span data-stu-id="10de7-105">Term definition</span></span>
---------------

<span data-ttu-id="10de7-106">Režijní náklady jsou náklady, které nutně vznikají při chodu podnikání, ale nelze je připsat přímo k žádné konkrétní podnikatelské aktivitě, produktu nebo službě.</span><span class="sxs-lookup"><span data-stu-id="10de7-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="10de7-107">Režijní náklady poskytují důležitou podporu pro generování aktivity přinášejících zisk.</span><span class="sxs-lookup"><span data-stu-id="10de7-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="10de7-108">Následuje několik příkladů režijních nákladů:</span><span class="sxs-lookup"><span data-stu-id="10de7-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="10de7-109">Renta</span><span class="sxs-lookup"><span data-stu-id="10de7-109">Rent</span></span>
-   <span data-ttu-id="10de7-110">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-110">Electricity</span></span>
-   <span data-ttu-id="10de7-111">Administrativní mzdy</span><span class="sxs-lookup"><span data-stu-id="10de7-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="10de7-112">Přehled výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-112">Overhead calculation overview</span></span>
<span data-ttu-id="10de7-113">Výpočet režijních nákladů spustí zásady účtování nákladů ve správném pořadí.</span><span class="sxs-lookup"><span data-stu-id="10de7-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="10de7-114">Výpočet režijních nákladů můžete pro stejné fiskální období spustit mnohokrát, pokud došlo ke změně zásad účtování nákladů nebo zjištění konkrétních chyb.</span><span class="sxs-lookup"><span data-stu-id="10de7-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="10de7-115">Každé spuštění výpočtu režijních nákladů se ukládá a přijímá ID jedinečné verze, které vám umožní porovnávat výpočty v různých verzích.</span><span class="sxs-lookup"><span data-stu-id="10de7-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="10de7-116">Položky nákladů, které generuje výpočet režijních nákladů, přijímá datum účtování.</span><span class="sxs-lookup"><span data-stu-id="10de7-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="10de7-117">Toto datum účtován se shoduje s konvovým datem fiskálního období, které se použije ve výpočtu.</span><span class="sxs-lookup"><span data-stu-id="10de7-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="10de7-118">ID jedinečné verze se skládá z následujících prvků:</span><span class="sxs-lookup"><span data-stu-id="10de7-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="10de7-119">Typ verze</span><span class="sxs-lookup"><span data-stu-id="10de7-119">Version type</span></span>
-   <span data-ttu-id="10de7-120">Datum a čas</span><span class="sxs-lookup"><span data-stu-id="10de7-120">Date and time</span></span>
-   <span data-ttu-id="10de7-121">Hlavní kniha nákladového účetnictví</span><span class="sxs-lookup"><span data-stu-id="10de7-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="10de7-122">Fiskální rok</span><span class="sxs-lookup"><span data-stu-id="10de7-122">Fiscal year</span></span>
-   <span data-ttu-id="10de7-123">Fiskální období</span><span class="sxs-lookup"><span data-stu-id="10de7-123">Fiscal period</span></span>

<span data-ttu-id="10de7-124">Výpočet režijních nákladů se spustí bez ohledu na verzi.</span><span class="sxs-lookup"><span data-stu-id="10de7-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="10de7-125">Proto lze vypočítat rozpočtovou verzi před skutečnou verzí.</span><span class="sxs-lookup"><span data-stu-id="10de7-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="10de7-126">Výpočet režijních nákladů se skládá ze čtyř kroků uvedených na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="10de7-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="10de7-127">V každé fázi je vytvořeno záhlaví deníku, které obsahuje položky deníku.</span><span class="sxs-lookup"><span data-stu-id="10de7-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="10de7-128">Toto záhlaví deníku zachovává vstupní data pro každý krok výpočtu.</span><span class="sxs-lookup"><span data-stu-id="10de7-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="10de7-129">Zásady a pravidla se použijí na každý řádek deníku a položky nákladů jsou generovány jako výstup.</span><span class="sxs-lookup"><span data-stu-id="10de7-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="10de7-130">Máte tedy vždy plnou sledovatelnost.</span><span class="sxs-lookup"><span data-stu-id="10de7-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="10de7-131">[![Výpočet režijních nákladů](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="10de7-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="10de7-132">Výpočet a přidělení režijních nákladů za elektřinu</span><span class="sxs-lookup"><span data-stu-id="10de7-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="10de7-133">Ve finančním účetnictví se některé náklady, jako je například elektřina, registrují jako paušální.</span><span class="sxs-lookup"><span data-stu-id="10de7-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="10de7-134">Podrobný přehled pro vedoucí není tedy pro nákladové účetnictví k dispozici.</span><span class="sxs-lookup"><span data-stu-id="10de7-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="10de7-135">V nákladovém účetnictví musí náklady procházet organizačními jednotkami, aby byl získán správný přehled pro vedoucí napříč všemi jednotkami a úrovněmi organizace.</span><span class="sxs-lookup"><span data-stu-id="10de7-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="10de7-136">Tento tok musí být založen buď na přesném záznamu spotřeby nebo na objektivním hodnocení.</span><span class="sxs-lookup"><span data-stu-id="10de7-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="10de7-137">V hlavní knize mohou být zaúčtovány náklady na elektřinu způsobem znázorněným v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="10de7-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="10de7-138">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="10de7-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="10de7-139">Nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="10de7-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="10de7-140">Hlavní účet</span><span class="sxs-lookup"><span data-stu-id="10de7-140">Main account</span></span></th>
<th><span data-ttu-id="10de7-141">Částka v zúčtovací měně</span><span class="sxs-lookup"><span data-stu-id="10de7-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10de7-142">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="10de7-143">CC099</span><span class="sxs-lookup"><span data-stu-id="10de7-143">CC099</span></span></td>
<td><span data-ttu-id="10de7-144">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="10de7-144">Default cost center</span></span></td>
<td><span data-ttu-id="10de7-145">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-145">10001</span></span></td>
<td><span data-ttu-id="10de7-146">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-146">Electricity</span></span></td>
<td><span data-ttu-id="10de7-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="10de7-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="10de7-148">Krok 1: Zpracování výpočtu chování nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="10de7-149">Ve výchozím nastavení dostanou při importu položek nákladů z datového zdroje tyto položky v nákladovém účetnictví klasifikaci **Neklasifikované**.</span><span class="sxs-lookup"><span data-stu-id="10de7-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="10de7-150">Použitím pravidla zásad chování nákladů lze reklasifikovat položky nákladů jako **Pevné náklady** nebo **Variabilní náklady**.</span><span class="sxs-lookup"><span data-stu-id="10de7-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="10de7-151">Definice pravidel chování nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-151">Define the cost behavior rule</span></span>

<span data-ttu-id="10de7-152">V některých případech je část nákladů s pevným poplatkem a zbývající náklady jsou založeny na spotřebě.</span><span class="sxs-lookup"><span data-stu-id="10de7-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="10de7-153">Účty za elektřinu často odpovídají této definici.</span><span class="sxs-lookup"><span data-stu-id="10de7-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="10de7-154">Po platbě konkrétního pevného poplatku platíte spotřebu za kilowatthodinu (kWh).</span><span class="sxs-lookup"><span data-stu-id="10de7-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="10de7-155">Pokud je například poplatek pevných nákladů 1 000,00, definuje se pravidlo chování nákladů takto:</span><span class="sxs-lookup"><span data-stu-id="10de7-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="10de7-156">Pevná částka 1 000,00</span><span class="sxs-lookup"><span data-stu-id="10de7-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="10de7-157">0 &lt;= 1 000,00 = Pevná</span><span class="sxs-lookup"><span data-stu-id="10de7-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="10de7-158">1 000,01 &lt; N = Variabilní</span><span class="sxs-lookup"><span data-stu-id="10de7-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="10de7-159">Deník</span><span class="sxs-lookup"><span data-stu-id="10de7-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="10de7-160">Deník</span><span class="sxs-lookup"><span data-stu-id="10de7-160">Journal</span></span></th>
<th><span data-ttu-id="10de7-161">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="10de7-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="10de7-162">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="10de7-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="10de7-163">Verze</span><span class="sxs-lookup"><span data-stu-id="10de7-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10de7-164">00001</span><span class="sxs-lookup"><span data-stu-id="10de7-164">00001</span></span></td>
<td><span data-ttu-id="10de7-165">Deník výpočtu chování nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="10de7-166">Fiskální</span><span class="sxs-lookup"><span data-stu-id="10de7-166">Fiscal</span></span></td>
<td><span data-ttu-id="10de7-167">2017</span><span class="sxs-lookup"><span data-stu-id="10de7-167">2017</span></span></td>
<td><span data-ttu-id="10de7-168">Období 1</span><span class="sxs-lookup"><span data-stu-id="10de7-168">Period 1</span></span></td>
<td><span data-ttu-id="10de7-169">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="10de7-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="10de7-170">Položky deníku (Položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="10de7-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="10de7-171">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="10de7-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="10de7-172">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="10de7-173">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-173">Cost element</span></span></th>
<th><span data-ttu-id="10de7-174">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-174">Cost behavior</span></span></th>
<th><span data-ttu-id="10de7-175">Částka</span><span class="sxs-lookup"><span data-stu-id="10de7-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10de7-176">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="10de7-177">CC099</span><span class="sxs-lookup"><span data-stu-id="10de7-177">CC099</span></span></td>
<td><span data-ttu-id="10de7-178">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="10de7-178">Default cost center</span></span></td>
<td><span data-ttu-id="10de7-179">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-179">10001</span></span></td>
<td><span data-ttu-id="10de7-180">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-180">Electricity</span></span></td>
<td><span data-ttu-id="10de7-181">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="10de7-181">Unclassified</span></span></td>
<td><span data-ttu-id="10de7-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="10de7-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="10de7-183">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10de7-184">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="10de7-185">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-185">Cost element</span></span></th>
<th><span data-ttu-id="10de7-186">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-186">Cost behavior</span></span></th>
<th><span data-ttu-id="10de7-187">Částka</span><span class="sxs-lookup"><span data-stu-id="10de7-187">Amount</span></span></th>
<th><span data-ttu-id="10de7-188">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="10de7-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10de7-189">CC099</span><span class="sxs-lookup"><span data-stu-id="10de7-189">CC099</span></span></td>
<td><span data-ttu-id="10de7-190">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="10de7-190">Default cost center</span></span></td>
<td><span data-ttu-id="10de7-191">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-191">10001</span></span></td>
<td><span data-ttu-id="10de7-192">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-192">Electricity</span></span></td>
<td><span data-ttu-id="10de7-193">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="10de7-193">Unclassified</span></span></td>
<td><span data-ttu-id="10de7-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="10de7-194">10,000.00</span></span></td>
<td><span data-ttu-id="10de7-195">3. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-196">CC099</span><span class="sxs-lookup"><span data-stu-id="10de7-196">CC099</span></span></td>
<td><span data-ttu-id="10de7-197">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="10de7-197">Default cost center</span></span></td>
<td><span data-ttu-id="10de7-198">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-198">10001</span></span></td>
<td><span data-ttu-id="10de7-199">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-199">Electricity</span></span></td>
<td><span data-ttu-id="10de7-200">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="10de7-200">Unclassified</span></span></td>
<td><span data-ttu-id="10de7-201">-10 000,00</span><span class="sxs-lookup"><span data-stu-id="10de7-201">-10,000.00</span></span></td>
<td><span data-ttu-id="10de7-202">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-203">CC099</span><span class="sxs-lookup"><span data-stu-id="10de7-203">CC099</span></span></td>
<td><span data-ttu-id="10de7-204">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="10de7-204">Default cost center</span></span></td>
<td><span data-ttu-id="10de7-205">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-205">10001</span></span></td>
<td><span data-ttu-id="10de7-206">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-206">Electricity</span></span></td>
<td><span data-ttu-id="10de7-207">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-207">Fixed cost</span></span></td>
<td><span data-ttu-id="10de7-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="10de7-208">1,000.00</span></span></td>
<td><span data-ttu-id="10de7-209">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-210">CC099</span><span class="sxs-lookup"><span data-stu-id="10de7-210">CC099</span></span></td>
<td><span data-ttu-id="10de7-211">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="10de7-211">Default cost center</span></span></td>
<td><span data-ttu-id="10de7-212">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-212">10001</span></span></td>
<td><span data-ttu-id="10de7-213">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-213">Electricity</span></span></td>
<td><span data-ttu-id="10de7-214">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-214">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="10de7-215">9,000.00</span></span></td>
<td><span data-ttu-id="10de7-216">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10de7-217">Více informací naleznete v tématu [Vytvoření a přiřazení zásad chování nákladů k jednotce řízení nákladů](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="10de7-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="10de7-218">Krok 2: Zpracování výpočtu distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="10de7-219">Distribuce nákladů se používá k rozdělení nákladů z jednoho objektu nákladů na jeden nebo více dalších objektů nákladů použitím příslušného základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="10de7-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="10de7-220">Distribuce nákladů a přidělení nákladů se liší v tom, že k distribuci nákladů dochází vždy na úrovni primárního prvku nákladů původních nákladů.</span><span class="sxs-lookup"><span data-stu-id="10de7-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="10de7-221">Definice pravidel distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-221">Define the cost distribution rule</span></span>

<span data-ttu-id="10de7-222">Ve finančním účetnictví se náklady na elektřinu často registrují jako paušální.</span><span class="sxs-lookup"><span data-stu-id="10de7-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="10de7-223">V nákladovém účetnictví není tento přístup dostatečně podrobný.</span><span class="sxs-lookup"><span data-stu-id="10de7-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="10de7-224">Variabilní náklady by měly být distribuovány k jednotlivým objektům nákladů na solidním základě.</span><span class="sxs-lookup"><span data-stu-id="10de7-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="10de7-225">Nejlogičtější základ přidělení je spotřeba elektřiny (kWh).</span><span class="sxs-lookup"><span data-stu-id="10de7-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="10de7-226">Vytvoří se člen statistické dimenzi s názvem Elektřina a zaznamená se elektrické spotřeba.</span><span class="sxs-lookup"><span data-stu-id="10de7-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="10de7-227">Ve výchozím nastavení se všechny členy statistické dimenze stanou dostupnými zpřístupněny jako základy přidělení.</span><span class="sxs-lookup"><span data-stu-id="10de7-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10de7-228">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-228">Cost object</span></span></th>
<th><span data-ttu-id="10de7-229">kWh</span><span class="sxs-lookup"><span data-stu-id="10de7-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10de7-230">CC001</span><span class="sxs-lookup"><span data-stu-id="10de7-230">CC001</span></span></td>
<td><span data-ttu-id="10de7-231">HR</span><span class="sxs-lookup"><span data-stu-id="10de7-231">HR</span></span></td>
<td><span data-ttu-id="10de7-232">1 000</span><span class="sxs-lookup"><span data-stu-id="10de7-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-233">CC002</span><span class="sxs-lookup"><span data-stu-id="10de7-233">CC002</span></span></td>
<td><span data-ttu-id="10de7-234">Finance</span><span class="sxs-lookup"><span data-stu-id="10de7-234">Finance</span></span></td>
<td><span data-ttu-id="10de7-235">6,000</span><span class="sxs-lookup"><span data-stu-id="10de7-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-236">CC003</span><span class="sxs-lookup"><span data-stu-id="10de7-236">CC003</span></span></td>
<td><span data-ttu-id="10de7-237">Sestavení</span><span class="sxs-lookup"><span data-stu-id="10de7-237">Assembly</span></span></td>
<td><span data-ttu-id="10de7-238">0</span><span class="sxs-lookup"><span data-stu-id="10de7-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10de7-239">Následující tabulka zobrazuje výsledek při použití elektrické spotřeby jako základu přidělení pro variabilní náklady.</span><span class="sxs-lookup"><span data-stu-id="10de7-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10de7-240">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-240">Cost object</span></span></th>
<th><span data-ttu-id="10de7-241">Hodnota</span><span class="sxs-lookup"><span data-stu-id="10de7-241">Magnitude</span></span></th>
<th><span data-ttu-id="10de7-242">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="10de7-242">Allocation factor</span></span></th>
<th><span data-ttu-id="10de7-243">Částka</span><span class="sxs-lookup"><span data-stu-id="10de7-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10de7-244">CC001</span><span class="sxs-lookup"><span data-stu-id="10de7-244">CC001</span></span></td>
<td><span data-ttu-id="10de7-245">HR</span><span class="sxs-lookup"><span data-stu-id="10de7-245">HR</span></span></td>
<td><span data-ttu-id="10de7-246">1 000</span><span class="sxs-lookup"><span data-stu-id="10de7-246">1,000</span></span></td>
<td><span data-ttu-id="10de7-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="10de7-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="10de7-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="10de7-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-249">CC002</span><span class="sxs-lookup"><span data-stu-id="10de7-249">CC002</span></span></td>
<td><span data-ttu-id="10de7-250">Finance</span><span class="sxs-lookup"><span data-stu-id="10de7-250">Finance</span></span></td>
<td><span data-ttu-id="10de7-251">6,000</span><span class="sxs-lookup"><span data-stu-id="10de7-251">6,000</span></span></td>
<td><span data-ttu-id="10de7-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="10de7-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="10de7-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="10de7-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-254">CC003</span><span class="sxs-lookup"><span data-stu-id="10de7-254">CC003</span></span></td>
<td><span data-ttu-id="10de7-255">Sestavení</span><span class="sxs-lookup"><span data-stu-id="10de7-255">Assembly</span></span></td>
<td><span data-ttu-id="10de7-256">0</span><span class="sxs-lookup"><span data-stu-id="10de7-256">0</span></span></td>
<td><span data-ttu-id="10de7-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="10de7-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="10de7-258">0,00</span><span class="sxs-lookup"><span data-stu-id="10de7-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10de7-259">Pevné náklady musí být distribuovány rovnoměrně k jednotlivých objektům nákladů, které spotřebovávaly elektřinu.</span><span class="sxs-lookup"><span data-stu-id="10de7-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="10de7-260">Tohoto výsledku můžete dosáhnout pomocí členu statistické dimenze Elektřina v základu přidělení vzorce: (Elektřina &gt; 0,00) Následující tabulka zobrazuje výsledek při použití elektrické spotřeby jako základu přidělení pro variabilní náklady.</span><span class="sxs-lookup"><span data-stu-id="10de7-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10de7-261">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-261">Cost object</span></span></th>
<th><span data-ttu-id="10de7-262">Vzorec</span><span class="sxs-lookup"><span data-stu-id="10de7-262">Formula</span></span></th>
<th><span data-ttu-id="10de7-263">Hodnota</span><span class="sxs-lookup"><span data-stu-id="10de7-263">Magnitude</span></span></th>
<th><span data-ttu-id="10de7-264">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="10de7-264">Allocation factor</span></span></th>
<th><span data-ttu-id="10de7-265">Částka</span><span class="sxs-lookup"><span data-stu-id="10de7-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10de7-266">CC001</span><span class="sxs-lookup"><span data-stu-id="10de7-266">CC001</span></span></td>
<td><span data-ttu-id="10de7-267">HR</span><span class="sxs-lookup"><span data-stu-id="10de7-267">HR</span></span></td>
<td><span data-ttu-id="10de7-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="10de7-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="10de7-269">1</span><span class="sxs-lookup"><span data-stu-id="10de7-269">1</span></span></td>
<td><span data-ttu-id="10de7-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="10de7-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="10de7-271">500.00</span><span class="sxs-lookup"><span data-stu-id="10de7-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-272">CC002</span><span class="sxs-lookup"><span data-stu-id="10de7-272">CC002</span></span></td>
<td><span data-ttu-id="10de7-273">Finance</span><span class="sxs-lookup"><span data-stu-id="10de7-273">Finance</span></span></td>
<td><span data-ttu-id="10de7-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="10de7-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="10de7-275">1</span><span class="sxs-lookup"><span data-stu-id="10de7-275">1</span></span></td>
<td><span data-ttu-id="10de7-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="10de7-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="10de7-277">500.00</span><span class="sxs-lookup"><span data-stu-id="10de7-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-278">CC003</span><span class="sxs-lookup"><span data-stu-id="10de7-278">CC003</span></span></td>
<td><span data-ttu-id="10de7-279">Sestavení</span><span class="sxs-lookup"><span data-stu-id="10de7-279">Assembly</span></span></td>
<td><span data-ttu-id="10de7-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="10de7-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="10de7-281">0</span><span class="sxs-lookup"><span data-stu-id="10de7-281">0</span></span></td>
<td><span data-ttu-id="10de7-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="10de7-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="10de7-283">0,00</span><span class="sxs-lookup"><span data-stu-id="10de7-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="10de7-284">Deník</span><span class="sxs-lookup"><span data-stu-id="10de7-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="10de7-285">Deník</span><span class="sxs-lookup"><span data-stu-id="10de7-285">Journal</span></span></th>
<th><span data-ttu-id="10de7-286">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="10de7-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="10de7-287">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="10de7-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="10de7-288">Verze</span><span class="sxs-lookup"><span data-stu-id="10de7-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10de7-289">00002</span><span class="sxs-lookup"><span data-stu-id="10de7-289">00002</span></span></td>
<td><span data-ttu-id="10de7-290">Deník výpočtu distribuce nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="10de7-291">Fiskální</span><span class="sxs-lookup"><span data-stu-id="10de7-291">Fiscal</span></span></td>
<td><span data-ttu-id="10de7-292">2017</span><span class="sxs-lookup"><span data-stu-id="10de7-292">2017</span></span></td>
<td><span data-ttu-id="10de7-293">Období 1</span><span class="sxs-lookup"><span data-stu-id="10de7-293">Period 1</span></span></td>
<td><span data-ttu-id="10de7-294">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="10de7-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="10de7-295">Položky deníku (Položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="10de7-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="10de7-296">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="10de7-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="10de7-297">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="10de7-298">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-298">Cost element</span></span></th>
<th><span data-ttu-id="10de7-299">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-299">Cost behavior</span></span></th>
<th><span data-ttu-id="10de7-300">Částka</span><span class="sxs-lookup"><span data-stu-id="10de7-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10de7-301">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="10de7-302">CC099</span><span class="sxs-lookup"><span data-stu-id="10de7-302">CC099</span></span></td>
<td><span data-ttu-id="10de7-303">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="10de7-303">Default cost center</span></span></td>
<td><span data-ttu-id="10de7-304">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-304">10001</span></span></td>
<td><span data-ttu-id="10de7-305">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-305">Electricity</span></span></td>
<td><span data-ttu-id="10de7-306">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-306">Fixed cost</span></span></td>
<td><span data-ttu-id="10de7-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="10de7-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-308">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="10de7-309">CC099</span><span class="sxs-lookup"><span data-stu-id="10de7-309">CC099</span></span></td>
<td><span data-ttu-id="10de7-310">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="10de7-310">Default cost center</span></span></td>
<td><span data-ttu-id="10de7-311">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-311">10001</span></span></td>
<td><span data-ttu-id="10de7-312">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-312">Electricity</span></span></td>
<td><span data-ttu-id="10de7-313">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-313">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="10de7-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="10de7-315">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10de7-316">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="10de7-317">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-317">Cost element</span></span></th>
<th><span data-ttu-id="10de7-318">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-318">Cost behavior</span></span></th>
<th><span data-ttu-id="10de7-319">Částka</span><span class="sxs-lookup"><span data-stu-id="10de7-319">Amount</span></span></th>
<th><span data-ttu-id="10de7-320">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="10de7-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10de7-321">CC099</span><span class="sxs-lookup"><span data-stu-id="10de7-321">CC099</span></span></td>
<td><span data-ttu-id="10de7-322">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="10de7-322">Default cost center</span></span></td>
<td><span data-ttu-id="10de7-323">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-323">10001</span></span></td>
<td><span data-ttu-id="10de7-324">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-324">Electricity</span></span></td>
<td><span data-ttu-id="10de7-325">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-325">Fixed cost</span></span></td>
<td><span data-ttu-id="10de7-326">-1 000,00</span><span class="sxs-lookup"><span data-stu-id="10de7-326">-1,000.00</span></span></td>
<td><span data-ttu-id="10de7-327">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-328">CC001</span><span class="sxs-lookup"><span data-stu-id="10de7-328">CC001</span></span></td>
<td><span data-ttu-id="10de7-329">HR</span><span class="sxs-lookup"><span data-stu-id="10de7-329">HR</span></span></td>
<td><span data-ttu-id="10de7-330">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-330">10001</span></span></td>
<td><span data-ttu-id="10de7-331">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-331">Electricity</span></span></td>
<td><span data-ttu-id="10de7-332">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-332">Fixed cost</span></span></td>
<td><span data-ttu-id="10de7-333">500.00</span><span class="sxs-lookup"><span data-stu-id="10de7-333">500.00</span></span></td>
<td><span data-ttu-id="10de7-334">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-335">CC002</span><span class="sxs-lookup"><span data-stu-id="10de7-335">CC002</span></span></td>
<td><span data-ttu-id="10de7-336">Finance</span><span class="sxs-lookup"><span data-stu-id="10de7-336">Finance</span></span></td>
<td><span data-ttu-id="10de7-337">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-337">10001</span></span></td>
<td><span data-ttu-id="10de7-338">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-338">Electricity</span></span></td>
<td><span data-ttu-id="10de7-339">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-339">Fixed cost</span></span></td>
<td><span data-ttu-id="10de7-340">500.00</span><span class="sxs-lookup"><span data-stu-id="10de7-340">500.00</span></span></td>
<td><span data-ttu-id="10de7-341">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-342">CC099</span><span class="sxs-lookup"><span data-stu-id="10de7-342">CC099</span></span></td>
<td><span data-ttu-id="10de7-343">Výchozí nákladové středisko</span><span class="sxs-lookup"><span data-stu-id="10de7-343">Default cost center</span></span></td>
<td><span data-ttu-id="10de7-344">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-344">10001</span></span></td>
<td><span data-ttu-id="10de7-345">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-345">Electricity</span></span></td>
<td><span data-ttu-id="10de7-346">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-346">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-347">-9 000,00</span><span class="sxs-lookup"><span data-stu-id="10de7-347">-9,000.00</span></span></td>
<td><span data-ttu-id="10de7-348">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-349">CC001</span><span class="sxs-lookup"><span data-stu-id="10de7-349">CC001</span></span></td>
<td><span data-ttu-id="10de7-350">HR</span><span class="sxs-lookup"><span data-stu-id="10de7-350">HR</span></span></td>
<td><span data-ttu-id="10de7-351">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-351">10001</span></span></td>
<td><span data-ttu-id="10de7-352">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-352">Electricity</span></span></td>
<td><span data-ttu-id="10de7-353">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-353">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="10de7-354">1,285.71</span></span></td>
<td><span data-ttu-id="10de7-355">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-356">CC002</span><span class="sxs-lookup"><span data-stu-id="10de7-356">CC002</span></span></td>
<td><span data-ttu-id="10de7-357">Finance</span><span class="sxs-lookup"><span data-stu-id="10de7-357">Finance</span></span></td>
<td><span data-ttu-id="10de7-358">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-358">10001</span></span></td>
<td><span data-ttu-id="10de7-359">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-359">Electricity</span></span></td>
<td><span data-ttu-id="10de7-360">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-360">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="10de7-361">7,714.29</span></span></td>
<td><span data-ttu-id="10de7-362">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10de7-363">Více informací naleznete v tématu [Vytvoření a přiřazení zásad distribuce nákladů k jednotce řízení nákladů](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="10de7-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="10de7-364">Krok 3: Zpracování výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="10de7-365">Režijní náklady se používají k účtování jednoho nebo více konkrétních objektů nákladů.</span><span class="sxs-lookup"><span data-stu-id="10de7-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="10de7-366">Účtování je založeno na předem určené nákladové sazbě a množství z přiřazeného základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="10de7-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="10de7-367">Definice sazby režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-367">Define the overhead rate</span></span>

<span data-ttu-id="10de7-368">Objekt nákladů CC001 HR přispívá k sadě interních projektů.</span><span class="sxs-lookup"><span data-stu-id="10de7-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="10de7-369">Vytvoří se člen statistické dimenzi s názvem projekty lidských zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="10de7-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10de7-370">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-370">Cost object</span></span></th>
<th><span data-ttu-id="10de7-371">Pracovní doba</span><span class="sxs-lookup"><span data-stu-id="10de7-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10de7-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="10de7-372">Proj 1</span></span></td>
<td><span data-ttu-id="10de7-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="10de7-373">Project 1</span></span></td>
<td><span data-ttu-id="10de7-374">3</span><span class="sxs-lookup"><span data-stu-id="10de7-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="10de7-375">Proj 2</span></span></td>
<td><span data-ttu-id="10de7-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="10de7-376">Project 2</span></span></td>
<td><span data-ttu-id="10de7-377">1</span><span class="sxs-lookup"><span data-stu-id="10de7-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10de7-378">Byla definována předem určená nákladová sazba pro příspěvky k nákladovým projektům.</span><span class="sxs-lookup"><span data-stu-id="10de7-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10de7-379">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-379">Cost object</span></span></th>
<th><span data-ttu-id="10de7-380">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-380">Cost element</span></span></th>
<th><span data-ttu-id="10de7-381">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-381">Cost behavior</span></span></th>
<th><span data-ttu-id="10de7-382">Jednotky</span><span class="sxs-lookup"><span data-stu-id="10de7-382">Units</span></span></th>
<th><span data-ttu-id="10de7-383">Kurz</span><span class="sxs-lookup"><span data-stu-id="10de7-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10de7-384">CC001</span><span class="sxs-lookup"><span data-stu-id="10de7-384">CC001</span></span></td>
<td><span data-ttu-id="10de7-385">HR</span><span class="sxs-lookup"><span data-stu-id="10de7-385">HR</span></span></td>
<td><span data-ttu-id="10de7-386">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-386">10001</span></span></td>
<td><span data-ttu-id="10de7-387">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-387">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-388">1</span><span class="sxs-lookup"><span data-stu-id="10de7-388">1</span></span></td>
<td><span data-ttu-id="10de7-389">10</span><span class="sxs-lookup"><span data-stu-id="10de7-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10de7-390">Následující tabulka zobrazuje výsledek při použití projektů lidských zdrojů jako základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="10de7-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10de7-391">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-391">Cost object</span></span></th>
<th><span data-ttu-id="10de7-392">Hodnota</span><span class="sxs-lookup"><span data-stu-id="10de7-392">Magnitude</span></span></th>
<th><span data-ttu-id="10de7-393">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-393">Cost element</span></span></th>
<th><span data-ttu-id="10de7-394">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="10de7-394">Allocation factor</span></span></th>
<th><span data-ttu-id="10de7-395">Částka</span><span class="sxs-lookup"><span data-stu-id="10de7-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10de7-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="10de7-396">Proj 1</span></span></td>
<td><span data-ttu-id="10de7-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="10de7-397">Project 1</span></span></td>
<td><span data-ttu-id="10de7-398">3</span><span class="sxs-lookup"><span data-stu-id="10de7-398">3</span></span></td>
<td><span data-ttu-id="10de7-399">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-399">10001</span></span></td>
<td><span data-ttu-id="10de7-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="10de7-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="10de7-401">30.00</span><span class="sxs-lookup"><span data-stu-id="10de7-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="10de7-402">Proj 2</span></span></td>
<td><span data-ttu-id="10de7-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="10de7-403">Project 2</span></span></td>
<td><span data-ttu-id="10de7-404">1</span><span class="sxs-lookup"><span data-stu-id="10de7-404">1</span></span></td>
<td><span data-ttu-id="10de7-405">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-405">10001</span></span></td>
<td><span data-ttu-id="10de7-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="10de7-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="10de7-407">10,00</span><span class="sxs-lookup"><span data-stu-id="10de7-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="10de7-408">Deník</span><span class="sxs-lookup"><span data-stu-id="10de7-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="10de7-409">Deník</span><span class="sxs-lookup"><span data-stu-id="10de7-409">Journal</span></span></th>
<th><span data-ttu-id="10de7-410">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="10de7-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="10de7-411">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="10de7-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="10de7-412">Verze</span><span class="sxs-lookup"><span data-stu-id="10de7-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10de7-413">00003</span><span class="sxs-lookup"><span data-stu-id="10de7-413">00003</span></span></td>
<td><span data-ttu-id="10de7-414">Deník výpočtu režijních nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="10de7-415">Fiskální</span><span class="sxs-lookup"><span data-stu-id="10de7-415">Fiscal</span></span></td>
<td><span data-ttu-id="10de7-416">2017</span><span class="sxs-lookup"><span data-stu-id="10de7-416">2017</span></span></td>
<td><span data-ttu-id="10de7-417">Období 1</span><span class="sxs-lookup"><span data-stu-id="10de7-417">Period 1</span></span></td>
<td><span data-ttu-id="10de7-418">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="10de7-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="10de7-419">Položky deníku (položky deníku pro výpočet sazby režijních nákladů)</span><span class="sxs-lookup"><span data-stu-id="10de7-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="10de7-420">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="10de7-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="10de7-421">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-421">Cost object</span></span></th>
<th><span data-ttu-id="10de7-422">Hodnota</span><span class="sxs-lookup"><span data-stu-id="10de7-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10de7-423">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="10de7-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="10de7-424">Proj 1</span></span></td>
<td><span data-ttu-id="10de7-425">Interní projekt 1</span><span class="sxs-lookup"><span data-stu-id="10de7-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="10de7-426">3,00</span><span class="sxs-lookup"><span data-stu-id="10de7-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-427">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="10de7-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="10de7-428">Proj 2</span></span></td>
<td><span data-ttu-id="10de7-429">Interní projekt 2</span><span class="sxs-lookup"><span data-stu-id="10de7-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="10de7-430">1.00</span><span class="sxs-lookup"><span data-stu-id="10de7-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="10de7-431">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10de7-432">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="10de7-433">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-433">Cost element</span></span></th>
<th><span data-ttu-id="10de7-434">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-434">Cost behavior</span></span></th>
<th><span data-ttu-id="10de7-435">Částka</span><span class="sxs-lookup"><span data-stu-id="10de7-435">Amount</span></span></th>
<th><span data-ttu-id="10de7-436">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="10de7-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10de7-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="10de7-437">CC0001</span></span></td>
<td><span data-ttu-id="10de7-438">HR</span><span class="sxs-lookup"><span data-stu-id="10de7-438">HR</span></span></td>
<td><span data-ttu-id="10de7-439">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-439">10001</span></span></td>
<td><span data-ttu-id="10de7-440">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-440">Electricity</span></span></td>
<td><span data-ttu-id="10de7-441">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-441">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="10de7-442">-30.00</span></span></td>
<td><span data-ttu-id="10de7-443">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="10de7-444">Proj 1</span></span></td>
<td><span data-ttu-id="10de7-445">Interní projekt 1</span><span class="sxs-lookup"><span data-stu-id="10de7-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="10de7-446">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-446">10001</span></span></td>
<td><span data-ttu-id="10de7-447">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-447">Electricity</span></span></td>
<td><span data-ttu-id="10de7-448">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-448">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-449">30.00</span><span class="sxs-lookup"><span data-stu-id="10de7-449">30.00</span></span></td>
<td><span data-ttu-id="10de7-450">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-451">CC001</span><span class="sxs-lookup"><span data-stu-id="10de7-451">CC001</span></span></td>
<td><span data-ttu-id="10de7-452">HR</span><span class="sxs-lookup"><span data-stu-id="10de7-452">HR</span></span></td>
<td><span data-ttu-id="10de7-453">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-453">10001</span></span></td>
<td><span data-ttu-id="10de7-454">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-454">Electricity</span></span></td>
<td><span data-ttu-id="10de7-455">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-455">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="10de7-456">-10.00</span></span></td>
<td><span data-ttu-id="10de7-457">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="10de7-458">Proj 2</span></span></td>
<td><span data-ttu-id="10de7-459">Interní projekt 2</span><span class="sxs-lookup"><span data-stu-id="10de7-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="10de7-460">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-460">10001</span></span></td>
<td><span data-ttu-id="10de7-461">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-461">Electricity</span></span></td>
<td><span data-ttu-id="10de7-462">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-462">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-463">10.00</span><span class="sxs-lookup"><span data-stu-id="10de7-463">10.00</span></span></td>
<td><span data-ttu-id="10de7-464">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10de7-465">Další informace naleznete v tématu [Provedení výpočtu režijních nákladů](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="10de7-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="10de7-466">Krok 4: Zpracování výpočtu přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="10de7-467">Přidělení se používá k přidělení zůstatku objektu nákladů do jiných objektů nákladů použitím základu přidělení.</span><span class="sxs-lookup"><span data-stu-id="10de7-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="10de7-468">Aplikace Finance podporuje reciproční metodu přidělování.</span><span class="sxs-lookup"><span data-stu-id="10de7-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="10de7-469">V metodě vzájemného přidělení jsou plně rozpoznány vzájemné služby, které si vyměňují pomocné objekty nákladů.</span><span class="sxs-lookup"><span data-stu-id="10de7-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="10de7-470">Systém automaticky určí provádění přidělení ve správném pořadí.</span><span class="sxs-lookup"><span data-stu-id="10de7-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="10de7-471">Zůstatek objektu nákladů je přidělen jedním základem přidělení.</span><span class="sxs-lookup"><span data-stu-id="10de7-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="10de7-472">Je podporováno přidělování napříč dimenzemi objektů nákladů a jejich příslušných členů.</span><span class="sxs-lookup"><span data-stu-id="10de7-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="10de7-473">Pořadí přidělení je řízeno jednotkou řízení nákladů.</span><span class="sxs-lookup"><span data-stu-id="10de7-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="10de7-474">[![Reciproční metoda](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="10de7-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="10de7-475">Definice přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-475">Define the cost allocation</span></span>

<span data-ttu-id="10de7-476">Toto je jednoduchý příklad, který vysvětluje, jakým způsobem lze sledovat tok nákladů.</span><span class="sxs-lookup"><span data-stu-id="10de7-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="10de7-477">Objekt nákladů objektu CC001 HR přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="10de7-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="10de7-478">Vytvoří se člen statistické dimenzi s názvem služby lidských zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="10de7-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10de7-479">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-479">Cost object</span></span></th>
<th><span data-ttu-id="10de7-480">Služby HR</span><span class="sxs-lookup"><span data-stu-id="10de7-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10de7-481">CC002</span><span class="sxs-lookup"><span data-stu-id="10de7-481">CC002</span></span></td>
<td><span data-ttu-id="10de7-482">Finance</span><span class="sxs-lookup"><span data-stu-id="10de7-482">Finance</span></span></td>
<td><span data-ttu-id="10de7-483">35</span><span class="sxs-lookup"><span data-stu-id="10de7-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-484">CC003</span><span class="sxs-lookup"><span data-stu-id="10de7-484">CC003</span></span></td>
<td><span data-ttu-id="10de7-485">Sestavení</span><span class="sxs-lookup"><span data-stu-id="10de7-485">Assembly</span></span></td>
<td><span data-ttu-id="10de7-486">55</span><span class="sxs-lookup"><span data-stu-id="10de7-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-487">CC004</span><span class="sxs-lookup"><span data-stu-id="10de7-487">CC004</span></span></td>
<td><span data-ttu-id="10de7-488">Balení</span><span class="sxs-lookup"><span data-stu-id="10de7-488">Packaging</span></span></td>
<td><span data-ttu-id="10de7-489">10</span><span class="sxs-lookup"><span data-stu-id="10de7-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10de7-490">Objekt nákladů objektu CC002 Finance přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="10de7-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="10de7-491">Vytvoří se člen statistické dimenzi s názvem Finanční služby k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="10de7-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10de7-492">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-492">Cost object</span></span></th>
<th><span data-ttu-id="10de7-493">Finanční služby</span><span class="sxs-lookup"><span data-stu-id="10de7-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10de7-494">CC003</span><span class="sxs-lookup"><span data-stu-id="10de7-494">CC003</span></span></td>
<td><span data-ttu-id="10de7-495">Sestavení</span><span class="sxs-lookup"><span data-stu-id="10de7-495">Assembly</span></span></td>
<td><span data-ttu-id="10de7-496">65</span><span class="sxs-lookup"><span data-stu-id="10de7-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-497">CC004</span><span class="sxs-lookup"><span data-stu-id="10de7-497">CC004</span></span></td>
<td><span data-ttu-id="10de7-498">Balení</span><span class="sxs-lookup"><span data-stu-id="10de7-498">Packaging</span></span></td>
<td><span data-ttu-id="10de7-499">35</span><span class="sxs-lookup"><span data-stu-id="10de7-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10de7-500">Objekt nákladů objektu CC003 Sestavení přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="10de7-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="10de7-501">Vytvoří se člen statistické dimenzi s názvem Služby sestavení zdrojů k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="10de7-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10de7-502">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-502">Cost object</span></span></th>
<th><span data-ttu-id="10de7-503">Služby sestavení (v hodinách)</span><span class="sxs-lookup"><span data-stu-id="10de7-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10de7-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="10de7-504">Prod 1</span></span></td>
<td><span data-ttu-id="10de7-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="10de7-505">Product 1</span></span></td>
<td><span data-ttu-id="10de7-506">60</span><span class="sxs-lookup"><span data-stu-id="10de7-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="10de7-507">Prod 2</span></span></td>
<td><span data-ttu-id="10de7-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="10de7-508">Product 2</span></span></td>
<td><span data-ttu-id="10de7-509">20</span><span class="sxs-lookup"><span data-stu-id="10de7-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10de7-510">Objekt nákladů objektu CC004 Balení přispívá k několika objektům nákladů.</span><span class="sxs-lookup"><span data-stu-id="10de7-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="10de7-511">Vytvoří se člen statistické dimenzi s názvem Služby balení k měření spotřebovaného množství.</span><span class="sxs-lookup"><span data-stu-id="10de7-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10de7-512">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-512">Cost object</span></span></th>
<th><span data-ttu-id="10de7-513">Služby balení (v hodinách)</span><span class="sxs-lookup"><span data-stu-id="10de7-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10de7-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="10de7-514">Prod 1</span></span></td>
<td><span data-ttu-id="10de7-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="10de7-515">Product 1</span></span></td>
<td><span data-ttu-id="10de7-516">80</span><span class="sxs-lookup"><span data-stu-id="10de7-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="10de7-517">Prod 2</span></span></td>
<td><span data-ttu-id="10de7-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="10de7-518">Product 2</span></span></td>
<td><span data-ttu-id="10de7-519">15</span><span class="sxs-lookup"><span data-stu-id="10de7-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="10de7-520">Statistická měření, jako je například výrobní doba spotřebovaná produktem, lze odvodit z datového zdroje.</span><span class="sxs-lookup"><span data-stu-id="10de7-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="10de7-521">Více informací naleznete v části [Šablona poskytovatele statistického měření](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="10de7-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="10de7-522">V následující tabulce je uveden výsledek při použití služeb HR jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="10de7-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10de7-523">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-523">Cost object</span></span></th>
<th><span data-ttu-id="10de7-524">Hodnota</span><span class="sxs-lookup"><span data-stu-id="10de7-524">Magnitude</span></span></th>
<th><span data-ttu-id="10de7-525">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="10de7-525">Allocation factor</span></span></th>
<th><span data-ttu-id="10de7-526">Částka</span><span class="sxs-lookup"><span data-stu-id="10de7-526">Amount</span></span></th>
<th><span data-ttu-id="10de7-527">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10de7-528">CC002</span><span class="sxs-lookup"><span data-stu-id="10de7-528">CC002</span></span></td>
<td><span data-ttu-id="10de7-529">Finance</span><span class="sxs-lookup"><span data-stu-id="10de7-529">Finance</span></span></td>
<td><span data-ttu-id="10de7-530">35</span><span class="sxs-lookup"><span data-stu-id="10de7-530">35</span></span></td>
<td><span data-ttu-id="10de7-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="10de7-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="10de7-532">175.00</span><span class="sxs-lookup"><span data-stu-id="10de7-532">175.00</span></span></td>
<td><span data-ttu-id="10de7-533">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-534">CC003</span><span class="sxs-lookup"><span data-stu-id="10de7-534">CC003</span></span></td>
<td><span data-ttu-id="10de7-535">Sestavení</span><span class="sxs-lookup"><span data-stu-id="10de7-535">Assembly</span></span></td>
<td><span data-ttu-id="10de7-536">55</span><span class="sxs-lookup"><span data-stu-id="10de7-536">55</span></span></td>
<td><span data-ttu-id="10de7-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="10de7-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="10de7-538">275.00</span><span class="sxs-lookup"><span data-stu-id="10de7-538">275.00</span></span></td>
<td><span data-ttu-id="10de7-539">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-540">CC004</span><span class="sxs-lookup"><span data-stu-id="10de7-540">CC004</span></span></td>
<td><span data-ttu-id="10de7-541">Balení</span><span class="sxs-lookup"><span data-stu-id="10de7-541">Packaging</span></span></td>
<td><span data-ttu-id="10de7-542">10</span><span class="sxs-lookup"><span data-stu-id="10de7-542">10</span></span></td>
<td><span data-ttu-id="10de7-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="10de7-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="10de7-544">50,00</span><span class="sxs-lookup"><span data-stu-id="10de7-544">50.00</span></span></td>
<td><span data-ttu-id="10de7-545">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-546">CC002</span><span class="sxs-lookup"><span data-stu-id="10de7-546">CC002</span></span></td>
<td><span data-ttu-id="10de7-547">Finance</span><span class="sxs-lookup"><span data-stu-id="10de7-547">Finance</span></span></td>
<td><span data-ttu-id="10de7-548">35</span><span class="sxs-lookup"><span data-stu-id="10de7-548">35</span></span></td>
<td><span data-ttu-id="10de7-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="10de7-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="10de7-550">436.00</span><span class="sxs-lookup"><span data-stu-id="10de7-550">436.00</span></span></td>
<td><span data-ttu-id="10de7-551">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-552">CC003</span><span class="sxs-lookup"><span data-stu-id="10de7-552">CC003</span></span></td>
<td><span data-ttu-id="10de7-553">Sestavení</span><span class="sxs-lookup"><span data-stu-id="10de7-553">Assembly</span></span></td>
<td><span data-ttu-id="10de7-554">55</span><span class="sxs-lookup"><span data-stu-id="10de7-554">55</span></span></td>
<td><span data-ttu-id="10de7-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="10de7-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="10de7-556">685.14</span><span class="sxs-lookup"><span data-stu-id="10de7-556">685.14</span></span></td>
<td><span data-ttu-id="10de7-557">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-558">CC004</span><span class="sxs-lookup"><span data-stu-id="10de7-558">CC004</span></span></td>
<td><span data-ttu-id="10de7-559">Balení</span><span class="sxs-lookup"><span data-stu-id="10de7-559">Packaging</span></span></td>
<td><span data-ttu-id="10de7-560">10</span><span class="sxs-lookup"><span data-stu-id="10de7-560">10</span></span></td>
<td><span data-ttu-id="10de7-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="10de7-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="10de7-562">124.57</span><span class="sxs-lookup"><span data-stu-id="10de7-562">124.57</span></span></td>
<td><span data-ttu-id="10de7-563">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10de7-564">V následující tabulce je uveden výsledek při použití Finančních služeb Finance jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="10de7-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10de7-565">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-565">Cost object</span></span></th>
<th><span data-ttu-id="10de7-566">Hodnota</span><span class="sxs-lookup"><span data-stu-id="10de7-566">Magnitude</span></span></th>
<th><span data-ttu-id="10de7-567">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="10de7-567">Allocation factor</span></span></th>
<th><span data-ttu-id="10de7-568">Částka</span><span class="sxs-lookup"><span data-stu-id="10de7-568">Amount</span></span></th>
<th><span data-ttu-id="10de7-569">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10de7-570">CC003</span><span class="sxs-lookup"><span data-stu-id="10de7-570">CC003</span></span></td>
<td><span data-ttu-id="10de7-571">Sestavení</span><span class="sxs-lookup"><span data-stu-id="10de7-571">Assembly</span></span></td>
<td><span data-ttu-id="10de7-572">65</span><span class="sxs-lookup"><span data-stu-id="10de7-572">65</span></span></td>
<td><span data-ttu-id="10de7-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="10de7-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="10de7-574">438.75</span><span class="sxs-lookup"><span data-stu-id="10de7-574">438.75</span></span></td>
<td><span data-ttu-id="10de7-575">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-576">CC004</span><span class="sxs-lookup"><span data-stu-id="10de7-576">CC004</span></span></td>
<td><span data-ttu-id="10de7-577">Balení</span><span class="sxs-lookup"><span data-stu-id="10de7-577">Packaging</span></span></td>
<td><span data-ttu-id="10de7-578">35</span><span class="sxs-lookup"><span data-stu-id="10de7-578">35</span></span></td>
<td><span data-ttu-id="10de7-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="10de7-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="10de7-580">236.25</span><span class="sxs-lookup"><span data-stu-id="10de7-580">236.25</span></span></td>
<td><span data-ttu-id="10de7-581">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-582">CC003</span><span class="sxs-lookup"><span data-stu-id="10de7-582">CC003</span></span></td>
<td><span data-ttu-id="10de7-583">Sestavení</span><span class="sxs-lookup"><span data-stu-id="10de7-583">Assembly</span></span></td>
<td><span data-ttu-id="10de7-584">65</span><span class="sxs-lookup"><span data-stu-id="10de7-584">65</span></span></td>
<td><span data-ttu-id="10de7-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="10de7-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="10de7-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="10de7-586">5,297.69</span></span></td>
<td><span data-ttu-id="10de7-587">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-588">CC004</span><span class="sxs-lookup"><span data-stu-id="10de7-588">CC004</span></span></td>
<td><span data-ttu-id="10de7-589">Balení</span><span class="sxs-lookup"><span data-stu-id="10de7-589">Packaging</span></span></td>
<td><span data-ttu-id="10de7-590">35</span><span class="sxs-lookup"><span data-stu-id="10de7-590">35</span></span></td>
<td><span data-ttu-id="10de7-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="10de7-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="10de7-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="10de7-592">2,852.60</span></span></td>
<td><span data-ttu-id="10de7-593">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10de7-594">V následující tabulce je uveden výsledek při použití Služeb sestavení jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="10de7-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10de7-595">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-595">Cost object</span></span></th>
<th><span data-ttu-id="10de7-596">Hodnota</span><span class="sxs-lookup"><span data-stu-id="10de7-596">Magnitude</span></span></th>
<th><span data-ttu-id="10de7-597">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="10de7-597">Allocation factor</span></span></th>
<th><span data-ttu-id="10de7-598">Částka</span><span class="sxs-lookup"><span data-stu-id="10de7-598">Amount</span></span></th>
<th><span data-ttu-id="10de7-599">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10de7-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="10de7-600">Prod 1</span></span></td>
<td><span data-ttu-id="10de7-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="10de7-601">Product 1</span></span></td>
<td><span data-ttu-id="10de7-602">60</span><span class="sxs-lookup"><span data-stu-id="10de7-602">60</span></span></td>
<td><span data-ttu-id="10de7-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="10de7-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="10de7-604">535.31</span><span class="sxs-lookup"><span data-stu-id="10de7-604">535.31</span></span></td>
<td><span data-ttu-id="10de7-605">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="10de7-606">Prod 2</span></span></td>
<td><span data-ttu-id="10de7-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="10de7-607">Product 2</span></span></td>
<td><span data-ttu-id="10de7-608">20</span><span class="sxs-lookup"><span data-stu-id="10de7-608">20</span></span></td>
<td><span data-ttu-id="10de7-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="10de7-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="10de7-610">178.44</span><span class="sxs-lookup"><span data-stu-id="10de7-610">178.44</span></span></td>
<td><span data-ttu-id="10de7-611">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="10de7-612">Prod 1</span></span></td>
<td><span data-ttu-id="10de7-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="10de7-613">Product 1</span></span></td>
<td><span data-ttu-id="10de7-614">60</span><span class="sxs-lookup"><span data-stu-id="10de7-614">60</span></span></td>
<td><span data-ttu-id="10de7-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="10de7-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="10de7-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="10de7-616">4,487.12</span></span></td>
<td><span data-ttu-id="10de7-617">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="10de7-618">Prod 2</span></span></td>
<td><span data-ttu-id="10de7-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="10de7-619">Product 2</span></span></td>
<td><span data-ttu-id="10de7-620">20</span><span class="sxs-lookup"><span data-stu-id="10de7-620">20</span></span></td>
<td><span data-ttu-id="10de7-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="10de7-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="10de7-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="10de7-622">1,495.71</span></span></td>
<td><span data-ttu-id="10de7-623">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10de7-624">V následující tabulce je uveden výsledek při použití Služeb balení jako základu přidělení pro celkové náklady (pevné náklady a variabilní náklady).</span><span class="sxs-lookup"><span data-stu-id="10de7-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10de7-625">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-625">Cost object</span></span></th>
<th><span data-ttu-id="10de7-626">Hodnota</span><span class="sxs-lookup"><span data-stu-id="10de7-626">Magnitude</span></span></th>
<th><span data-ttu-id="10de7-627">Koeficient přidělení</span><span class="sxs-lookup"><span data-stu-id="10de7-627">Allocation factor</span></span></th>
<th><span data-ttu-id="10de7-628">Částka</span><span class="sxs-lookup"><span data-stu-id="10de7-628">Amount</span></span></th>
<th><span data-ttu-id="10de7-629">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10de7-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="10de7-630">Prod 1</span></span></td>
<td><span data-ttu-id="10de7-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="10de7-631">Product 1</span></span></td>
<td><span data-ttu-id="10de7-632">80</span><span class="sxs-lookup"><span data-stu-id="10de7-632">80</span></span></td>
<td><span data-ttu-id="10de7-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="10de7-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="10de7-634">241.05</span><span class="sxs-lookup"><span data-stu-id="10de7-634">241.05</span></span></td>
<td><span data-ttu-id="10de7-635">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="10de7-636">Prod 2</span></span></td>
<td><span data-ttu-id="10de7-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="10de7-637">Product 2</span></span></td>
<td><span data-ttu-id="10de7-638">15</span><span class="sxs-lookup"><span data-stu-id="10de7-638">15</span></span></td>
<td><span data-ttu-id="10de7-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="10de7-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="10de7-640">45.20</span><span class="sxs-lookup"><span data-stu-id="10de7-640">45.20</span></span></td>
<td><span data-ttu-id="10de7-641">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="10de7-642">Prod 1</span></span></td>
<td><span data-ttu-id="10de7-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="10de7-643">Product 1</span></span></td>
<td><span data-ttu-id="10de7-644">80</span><span class="sxs-lookup"><span data-stu-id="10de7-644">80</span></span></td>
<td><span data-ttu-id="10de7-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="10de7-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="10de7-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="10de7-646">2,507.09</span></span></td>
<td><span data-ttu-id="10de7-647">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="10de7-648">Prod 2</span></span></td>
<td><span data-ttu-id="10de7-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="10de7-649">Product 2</span></span></td>
<td><span data-ttu-id="10de7-650">15</span><span class="sxs-lookup"><span data-stu-id="10de7-650">15</span></span></td>
<td><span data-ttu-id="10de7-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="10de7-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="10de7-652">470.08</span><span class="sxs-lookup"><span data-stu-id="10de7-652">470.08</span></span></td>
<td><span data-ttu-id="10de7-653">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="10de7-654">Položky deníku (položky deníku pro zůstatek objektu nákladů)</span><span class="sxs-lookup"><span data-stu-id="10de7-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="10de7-655">Deník</span><span class="sxs-lookup"><span data-stu-id="10de7-655">Journal</span></span></th>
<th><span data-ttu-id="10de7-656">Typ deníku</span><span class="sxs-lookup"><span data-stu-id="10de7-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="10de7-657">Fiskální kalendářní období</span><span class="sxs-lookup"><span data-stu-id="10de7-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="10de7-658">Verze</span><span class="sxs-lookup"><span data-stu-id="10de7-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10de7-659">00004</span><span class="sxs-lookup"><span data-stu-id="10de7-659">00004</span></span></td>
<td><span data-ttu-id="10de7-660">Deník přidělení nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="10de7-661">Fiskální</span><span class="sxs-lookup"><span data-stu-id="10de7-661">Fiscal</span></span></td>
<td><span data-ttu-id="10de7-662">2017</span><span class="sxs-lookup"><span data-stu-id="10de7-662">2017</span></span></td>
<td><span data-ttu-id="10de7-663">Období 1</span><span class="sxs-lookup"><span data-stu-id="10de7-663">Period 1</span></span></td>
<td><span data-ttu-id="10de7-664">Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1</span><span class="sxs-lookup"><span data-stu-id="10de7-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="10de7-665">Řádky deníku</span><span class="sxs-lookup"><span data-stu-id="10de7-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="10de7-666">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="10de7-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="10de7-667">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="10de7-668">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-668">Cost element</span></span></th>
<th><span data-ttu-id="10de7-669">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-669">Cost behavior</span></span></th>
<th><span data-ttu-id="10de7-670">Částka</span><span class="sxs-lookup"><span data-stu-id="10de7-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10de7-671">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="10de7-672">CC001</span><span class="sxs-lookup"><span data-stu-id="10de7-672">CC001</span></span></td>
<td><span data-ttu-id="10de7-673">HR</span><span class="sxs-lookup"><span data-stu-id="10de7-673">HR</span></span></td>
<td><span data-ttu-id="10de7-674">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-674">10001</span></span></td>
<td><span data-ttu-id="10de7-675">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-675">Electricity</span></span></td>
<td><span data-ttu-id="10de7-676">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-676">Fixed cost</span></span></td>
<td><span data-ttu-id="10de7-677">500.00</span><span class="sxs-lookup"><span data-stu-id="10de7-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-678">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="10de7-679">CC001</span><span class="sxs-lookup"><span data-stu-id="10de7-679">CC001</span></span></td>
<td><span data-ttu-id="10de7-680">HR</span><span class="sxs-lookup"><span data-stu-id="10de7-680">HR</span></span></td>
<td><span data-ttu-id="10de7-681">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-681">10001</span></span></td>
<td><span data-ttu-id="10de7-682">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-682">Electricity</span></span></td>
<td><span data-ttu-id="10de7-683">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-683">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="10de7-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-685">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="10de7-686">CC002</span><span class="sxs-lookup"><span data-stu-id="10de7-686">CC002</span></span></td>
<td><span data-ttu-id="10de7-687">Finance</span><span class="sxs-lookup"><span data-stu-id="10de7-687">Finance</span></span></td>
<td><span data-ttu-id="10de7-688">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-688">10001</span></span></td>
<td><span data-ttu-id="10de7-689">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-689">Electricity</span></span></td>
<td><span data-ttu-id="10de7-690">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-690">Fixed cost</span></span></td>
<td><span data-ttu-id="10de7-691">675.00</span><span class="sxs-lookup"><span data-stu-id="10de7-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-692">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="10de7-693">CC002</span><span class="sxs-lookup"><span data-stu-id="10de7-693">CC002</span></span></td>
<td><span data-ttu-id="10de7-694">Finance</span><span class="sxs-lookup"><span data-stu-id="10de7-694">Finance</span></span></td>
<td><span data-ttu-id="10de7-695">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-695">10001</span></span></td>
<td><span data-ttu-id="10de7-696">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-696">Electricity</span></span></td>
<td><span data-ttu-id="10de7-697">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-697">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="10de7-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-699">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="10de7-700">CC003</span><span class="sxs-lookup"><span data-stu-id="10de7-700">CC003</span></span></td>
<td><span data-ttu-id="10de7-701">Sestavení</span><span class="sxs-lookup"><span data-stu-id="10de7-701">Assembly</span></span></td>
<td><span data-ttu-id="10de7-702">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-702">10001</span></span></td>
<td><span data-ttu-id="10de7-703">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-703">Electricity</span></span></td>
<td><span data-ttu-id="10de7-704">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-704">Fixed cost</span></span></td>
<td><span data-ttu-id="10de7-705">713.75</span><span class="sxs-lookup"><span data-stu-id="10de7-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-706">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="10de7-707">CC003</span><span class="sxs-lookup"><span data-stu-id="10de7-707">CC003</span></span></td>
<td><span data-ttu-id="10de7-708">Sestavení</span><span class="sxs-lookup"><span data-stu-id="10de7-708">Assembly</span></span></td>
<td><span data-ttu-id="10de7-709">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-709">10001</span></span></td>
<td><span data-ttu-id="10de7-710">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-710">Electricity</span></span></td>
<td><span data-ttu-id="10de7-711">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-711">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="10de7-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-713">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="10de7-714">CC003</span><span class="sxs-lookup"><span data-stu-id="10de7-714">CC003</span></span></td>
<td><span data-ttu-id="10de7-715">Balení</span><span class="sxs-lookup"><span data-stu-id="10de7-715">Packaging</span></span></td>
<td><span data-ttu-id="10de7-716">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-716">10001</span></span></td>
<td><span data-ttu-id="10de7-717">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-717">Electricity</span></span></td>
<td><span data-ttu-id="10de7-718">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-718">Fixed cost</span></span></td>
<td><span data-ttu-id="10de7-719">286.25</span><span class="sxs-lookup"><span data-stu-id="10de7-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-720">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="10de7-721">CC003</span><span class="sxs-lookup"><span data-stu-id="10de7-721">CC003</span></span></td>
<td><span data-ttu-id="10de7-722">Balení</span><span class="sxs-lookup"><span data-stu-id="10de7-722">Packaging</span></span></td>
<td><span data-ttu-id="10de7-723">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-723">10001</span></span></td>
<td><span data-ttu-id="10de7-724">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-724">Electricity</span></span></td>
<td><span data-ttu-id="10de7-725">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-725">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="10de7-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-727">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="10de7-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="10de7-728">Prod 1</span></span></td>
<td><span data-ttu-id="10de7-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="10de7-729">Product 1</span></span></td>
<td><span data-ttu-id="10de7-730">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-730">10001</span></span></td>
<td><span data-ttu-id="10de7-731">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-731">Electricity</span></span></td>
<td><span data-ttu-id="10de7-732">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-732">Fixed cost</span></span></td>
<td><span data-ttu-id="10de7-733">776.36</span><span class="sxs-lookup"><span data-stu-id="10de7-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-734">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="10de7-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="10de7-735">Prod 1</span></span></td>
<td><span data-ttu-id="10de7-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="10de7-736">Product 1</span></span></td>
<td><span data-ttu-id="10de7-737">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-737">10001</span></span></td>
<td><span data-ttu-id="10de7-738">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-738">Electricity</span></span></td>
<td><span data-ttu-id="10de7-739">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-739">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="10de7-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-741">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="10de7-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="10de7-742">Prod 2</span></span></td>
<td><span data-ttu-id="10de7-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="10de7-743">Product 1</span></span></td>
<td><span data-ttu-id="10de7-744">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-744">10001</span></span></td>
<td><span data-ttu-id="10de7-745">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-745">Electricity</span></span></td>
<td><span data-ttu-id="10de7-746">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-746">Fixed cost</span></span></td>
<td><span data-ttu-id="10de7-747">223.64</span><span class="sxs-lookup"><span data-stu-id="10de7-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-748">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="10de7-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="10de7-749">Prod 2</span></span></td>
<td><span data-ttu-id="10de7-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="10de7-750">Product 1</span></span></td>
<td><span data-ttu-id="10de7-751">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-751">10001</span></span></td>
<td><span data-ttu-id="10de7-752">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-752">Electricity</span></span></td>
<td><span data-ttu-id="10de7-753">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-753">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="10de7-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="10de7-755">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="10de7-756">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="10de7-757">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-757">Cost element</span></span></th>
<th><span data-ttu-id="10de7-758">Chování nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-758">Cost behavior</span></span></th>
<th><span data-ttu-id="10de7-759">Částka</span><span class="sxs-lookup"><span data-stu-id="10de7-759">Amount</span></span></th>
<th><span data-ttu-id="10de7-760">Datum účtování</span><span class="sxs-lookup"><span data-stu-id="10de7-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="10de7-761">CC001</span><span class="sxs-lookup"><span data-stu-id="10de7-761">CC001</span></span></td>
<td><span data-ttu-id="10de7-762">HR</span><span class="sxs-lookup"><span data-stu-id="10de7-762">HR</span></span></td>
<td><span data-ttu-id="10de7-763">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-763">10001</span></span></td>
<td><span data-ttu-id="10de7-764">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-764">Electricity</span></span></td>
<td><span data-ttu-id="10de7-765">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-765">Fixed cost</span></span></td>
<td><span data-ttu-id="10de7-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="10de7-766">-500.00</span></span></td>
<td><span data-ttu-id="10de7-767">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-768">CC002</span><span class="sxs-lookup"><span data-stu-id="10de7-768">CC002</span></span></td>
<td><span data-ttu-id="10de7-769">Finance</span><span class="sxs-lookup"><span data-stu-id="10de7-769">Finance</span></span></td>
<td><span data-ttu-id="10de7-770">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-770">10001</span></span></td>
<td><span data-ttu-id="10de7-771">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-771">Electricity</span></span></td>
<td><span data-ttu-id="10de7-772">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-772">Fixed cost</span></span></td>
<td><span data-ttu-id="10de7-773">175.00</span><span class="sxs-lookup"><span data-stu-id="10de7-773">175.00</span></span></td>
<td><span data-ttu-id="10de7-774">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-775">CC003</span><span class="sxs-lookup"><span data-stu-id="10de7-775">CC003</span></span></td>
<td><span data-ttu-id="10de7-776">Sestavení</span><span class="sxs-lookup"><span data-stu-id="10de7-776">Assembly</span></span></td>
<td><span data-ttu-id="10de7-777">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-777">10001</span></span></td>
<td><span data-ttu-id="10de7-778">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-778">Electricity</span></span></td>
<td><span data-ttu-id="10de7-779">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-779">Fixed cost</span></span></td>
<td><span data-ttu-id="10de7-780">275.00</span><span class="sxs-lookup"><span data-stu-id="10de7-780">275.00</span></span></td>
<td><span data-ttu-id="10de7-781">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-782">CC004</span><span class="sxs-lookup"><span data-stu-id="10de7-782">CC004</span></span></td>
<td><span data-ttu-id="10de7-783">Balení</span><span class="sxs-lookup"><span data-stu-id="10de7-783">Packaging</span></span></td>
<td><span data-ttu-id="10de7-784">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-784">10001</span></span></td>
<td><span data-ttu-id="10de7-785">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-785">Electricity</span></span></td>
<td><span data-ttu-id="10de7-786">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-786">Fixed cost</span></span></td>
<td><span data-ttu-id="10de7-787">50,00</span><span class="sxs-lookup"><span data-stu-id="10de7-787">50,00</span></span></td>
<td><span data-ttu-id="10de7-788">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-789">CC001</span><span class="sxs-lookup"><span data-stu-id="10de7-789">CC001</span></span></td>
<td><span data-ttu-id="10de7-790">HR</span><span class="sxs-lookup"><span data-stu-id="10de7-790">HR</span></span></td>
<td><span data-ttu-id="10de7-791">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-791">10001</span></span></td>
<td><span data-ttu-id="10de7-792">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-792">Electricity</span></span></td>
<td><span data-ttu-id="10de7-793">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-793">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-794">-1 245,71</span><span class="sxs-lookup"><span data-stu-id="10de7-794">-1,245.71</span></span></td>
<td><span data-ttu-id="10de7-795">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-796">CC002</span><span class="sxs-lookup"><span data-stu-id="10de7-796">CC002</span></span></td>
<td><span data-ttu-id="10de7-797">Finance</span><span class="sxs-lookup"><span data-stu-id="10de7-797">Finance</span></span></td>
<td><span data-ttu-id="10de7-798">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-798">10001</span></span></td>
<td><span data-ttu-id="10de7-799">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-799">Electricity</span></span></td>
<td><span data-ttu-id="10de7-800">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-800">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-801">436.00</span><span class="sxs-lookup"><span data-stu-id="10de7-801">436.00</span></span></td>
<td><span data-ttu-id="10de7-802">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-803">CC003</span><span class="sxs-lookup"><span data-stu-id="10de7-803">CC003</span></span></td>
<td><span data-ttu-id="10de7-804">Sestavení</span><span class="sxs-lookup"><span data-stu-id="10de7-804">Assembly</span></span></td>
<td><span data-ttu-id="10de7-805">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-805">10001</span></span></td>
<td><span data-ttu-id="10de7-806">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-806">Electricity</span></span></td>
<td><span data-ttu-id="10de7-807">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-807">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-808">685.14</span><span class="sxs-lookup"><span data-stu-id="10de7-808">685.14</span></span></td>
<td><span data-ttu-id="10de7-809">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-810">CC004</span><span class="sxs-lookup"><span data-stu-id="10de7-810">CC004</span></span></td>
<td><span data-ttu-id="10de7-811">Balení</span><span class="sxs-lookup"><span data-stu-id="10de7-811">Packaging</span></span></td>
<td><span data-ttu-id="10de7-812">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-812">10001</span></span></td>
<td><span data-ttu-id="10de7-813">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-813">Electricity</span></span></td>
<td><span data-ttu-id="10de7-814">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-814">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-815">124.57</span><span class="sxs-lookup"><span data-stu-id="10de7-815">124.57</span></span></td>
<td><span data-ttu-id="10de7-816">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-817">CC002</span><span class="sxs-lookup"><span data-stu-id="10de7-817">CC002</span></span></td>
<td><span data-ttu-id="10de7-818">Finance</span><span class="sxs-lookup"><span data-stu-id="10de7-818">Finance</span></span></td>
<td><span data-ttu-id="10de7-819">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-819">10001</span></span></td>
<td><span data-ttu-id="10de7-820">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-820">Electricity</span></span></td>
<td><span data-ttu-id="10de7-821">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-821">Fixed cost</span></span></td>
<td><span data-ttu-id="10de7-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="10de7-822">-675.00</span></span></td>
<td><span data-ttu-id="10de7-823">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-824">CC003</span><span class="sxs-lookup"><span data-stu-id="10de7-824">CC003</span></span></td>
<td><span data-ttu-id="10de7-825">Sestavení</span><span class="sxs-lookup"><span data-stu-id="10de7-825">Assembly</span></span></td>
<td><span data-ttu-id="10de7-826">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-826">10001</span></span></td>
<td><span data-ttu-id="10de7-827">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-827">Electricity</span></span></td>
<td><span data-ttu-id="10de7-828">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-828">Fixed cost</span></span></td>
<td><span data-ttu-id="10de7-829">438.75</span><span class="sxs-lookup"><span data-stu-id="10de7-829">438.75</span></span></td>
<td><span data-ttu-id="10de7-830">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-831">CC004</span><span class="sxs-lookup"><span data-stu-id="10de7-831">CC004</span></span></td>
<td><span data-ttu-id="10de7-832">Balení</span><span class="sxs-lookup"><span data-stu-id="10de7-832">Packaging</span></span></td>
<td><span data-ttu-id="10de7-833">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-833">10001</span></span></td>
<td><span data-ttu-id="10de7-834">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-834">Electricity</span></span></td>
<td><span data-ttu-id="10de7-835">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-835">Fixed cost</span></span></td>
<td><span data-ttu-id="10de7-836">236.25</span><span class="sxs-lookup"><span data-stu-id="10de7-836">236.25</span></span></td>
<td><span data-ttu-id="10de7-837">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-838">CC002</span><span class="sxs-lookup"><span data-stu-id="10de7-838">CC002</span></span></td>
<td><span data-ttu-id="10de7-839">Finance</span><span class="sxs-lookup"><span data-stu-id="10de7-839">Finance</span></span></td>
<td><span data-ttu-id="10de7-840">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-840">10001</span></span></td>
<td><span data-ttu-id="10de7-841">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-841">Electricity</span></span></td>
<td><span data-ttu-id="10de7-842">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-842">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-843">-8 150,29</span><span class="sxs-lookup"><span data-stu-id="10de7-843">-8,150.29</span></span></td>
<td><span data-ttu-id="10de7-844">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-845">CC003</span><span class="sxs-lookup"><span data-stu-id="10de7-845">CC003</span></span></td>
<td><span data-ttu-id="10de7-846">Sestavení</span><span class="sxs-lookup"><span data-stu-id="10de7-846">Assembly</span></span></td>
<td><span data-ttu-id="10de7-847">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-847">10001</span></span></td>
<td><span data-ttu-id="10de7-848">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-848">Electricity</span></span></td>
<td><span data-ttu-id="10de7-849">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-849">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="10de7-850">5,297.69</span></span></td>
<td><span data-ttu-id="10de7-851">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-852">CC004</span><span class="sxs-lookup"><span data-stu-id="10de7-852">CC004</span></span></td>
<td><span data-ttu-id="10de7-853">Balení</span><span class="sxs-lookup"><span data-stu-id="10de7-853">Packaging</span></span></td>
<td><span data-ttu-id="10de7-854">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-854">10001</span></span></td>
<td><span data-ttu-id="10de7-855">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-855">Electricity</span></span></td>
<td><span data-ttu-id="10de7-856">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-856">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="10de7-857">2,852.60</span></span></td>
<td><span data-ttu-id="10de7-858">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-859">CC003</span><span class="sxs-lookup"><span data-stu-id="10de7-859">CC003</span></span></td>
<td><span data-ttu-id="10de7-860">Sestavení</span><span class="sxs-lookup"><span data-stu-id="10de7-860">Assembly</span></span></td>
<td><span data-ttu-id="10de7-861">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-861">10001</span></span></td>
<td><span data-ttu-id="10de7-862">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-862">Electricity</span></span></td>
<td><span data-ttu-id="10de7-863">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-863">Fixed cost</span></span></td>
<td><span data-ttu-id="10de7-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="10de7-864">-713.75</span></span></td>
<td><span data-ttu-id="10de7-865">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="10de7-866">Prod 1</span></span></td>
<td><span data-ttu-id="10de7-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="10de7-867">Product 1</span></span></td>
<td><span data-ttu-id="10de7-868">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-868">10001</span></span></td>
<td><span data-ttu-id="10de7-869">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-869">Electricity</span></span></td>
<td><span data-ttu-id="10de7-870">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-870">Fixed cost</span></span></td>
<td><span data-ttu-id="10de7-871">535.31</span><span class="sxs-lookup"><span data-stu-id="10de7-871">535.31</span></span></td>
<td><span data-ttu-id="10de7-872">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="10de7-873">Prod 2</span></span></td>
<td><span data-ttu-id="10de7-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="10de7-874">Product 2</span></span></td>
<td><span data-ttu-id="10de7-875">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-875">10001</span></span></td>
<td><span data-ttu-id="10de7-876">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-876">Electricity</span></span></td>
<td><span data-ttu-id="10de7-877">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-877">Fixed cost</span></span></td>
<td><span data-ttu-id="10de7-878">178.44</span><span class="sxs-lookup"><span data-stu-id="10de7-878">178.44</span></span></td>
<td><span data-ttu-id="10de7-879">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-880">CC003</span><span class="sxs-lookup"><span data-stu-id="10de7-880">CC003</span></span></td>
<td><span data-ttu-id="10de7-881">Sestavení</span><span class="sxs-lookup"><span data-stu-id="10de7-881">Assembly</span></span></td>
<td><span data-ttu-id="10de7-882">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-882">10001</span></span></td>
<td><span data-ttu-id="10de7-883">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-883">Electricity</span></span></td>
<td><span data-ttu-id="10de7-884">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-884">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-885">-5 982,83</span><span class="sxs-lookup"><span data-stu-id="10de7-885">-5,982.83</span></span></td>
<td><span data-ttu-id="10de7-886">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="10de7-887">Prod 1</span></span></td>
<td><span data-ttu-id="10de7-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="10de7-888">Product 1</span></span></td>
<td><span data-ttu-id="10de7-889">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-889">10001</span></span></td>
<td><span data-ttu-id="10de7-890">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-890">Electricity</span></span></td>
<td><span data-ttu-id="10de7-891">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-891">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="10de7-892">4,487.12</span></span></td>
<td><span data-ttu-id="10de7-893">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="10de7-894">Prod 2</span></span></td>
<td><span data-ttu-id="10de7-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="10de7-895">Product 2</span></span></td>
<td><span data-ttu-id="10de7-896">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-896">10001</span></span></td>
<td><span data-ttu-id="10de7-897">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-897">Electricity</span></span></td>
<td><span data-ttu-id="10de7-898">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-898">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="10de7-899">1,495.71</span></span></td>
<td><span data-ttu-id="10de7-900">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-901">CC003</span><span class="sxs-lookup"><span data-stu-id="10de7-901">CC003</span></span></td>
<td><span data-ttu-id="10de7-902">Sestavení</span><span class="sxs-lookup"><span data-stu-id="10de7-902">Assembly</span></span></td>
<td><span data-ttu-id="10de7-903">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-903">10001</span></span></td>
<td><span data-ttu-id="10de7-904">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-904">Electricity</span></span></td>
<td><span data-ttu-id="10de7-905">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-905">Fixed cost</span></span></td>
<td><span data-ttu-id="10de7-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="10de7-906">-286.25</span></span></td>
<td><span data-ttu-id="10de7-907">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="10de7-908">Prod 1</span></span></td>
<td><span data-ttu-id="10de7-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="10de7-909">Product 1</span></span></td>
<td><span data-ttu-id="10de7-910">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-910">10001</span></span></td>
<td><span data-ttu-id="10de7-911">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-911">Electricity</span></span></td>
<td><span data-ttu-id="10de7-912">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-912">Fixed cost</span></span></td>
<td><span data-ttu-id="10de7-913">241.05</span><span class="sxs-lookup"><span data-stu-id="10de7-913">241.05</span></span></td>
<td><span data-ttu-id="10de7-914">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="10de7-915">Prod 2</span></span></td>
<td><span data-ttu-id="10de7-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="10de7-916">Product 2</span></span></td>
<td><span data-ttu-id="10de7-917">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-917">10001</span></span></td>
<td><span data-ttu-id="10de7-918">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-918">Electricity</span></span></td>
<td><span data-ttu-id="10de7-919">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-919">Fixed cost</span></span></td>
<td><span data-ttu-id="10de7-920">45.20</span><span class="sxs-lookup"><span data-stu-id="10de7-920">45.20</span></span></td>
<td><span data-ttu-id="10de7-921">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-922">CC003</span><span class="sxs-lookup"><span data-stu-id="10de7-922">CC003</span></span></td>
<td><span data-ttu-id="10de7-923">Sestavení</span><span class="sxs-lookup"><span data-stu-id="10de7-923">Assembly</span></span></td>
<td><span data-ttu-id="10de7-924">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-924">10001</span></span></td>
<td><span data-ttu-id="10de7-925">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-925">Electricity</span></span></td>
<td><span data-ttu-id="10de7-926">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-926">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-927">-2977,17</span><span class="sxs-lookup"><span data-stu-id="10de7-927">-2,977.17</span></span></td>
<td><span data-ttu-id="10de7-928">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="10de7-929">Prod 1</span></span></td>
<td><span data-ttu-id="10de7-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="10de7-930">Product 1</span></span></td>
<td><span data-ttu-id="10de7-931">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-931">10001</span></span></td>
<td><span data-ttu-id="10de7-932">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-932">Electricity</span></span></td>
<td><span data-ttu-id="10de7-933">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-933">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="10de7-934">2,507.09</span></span></td>
<td><span data-ttu-id="10de7-935">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="10de7-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="10de7-936">Prod 2</span></span></td>
<td><span data-ttu-id="10de7-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="10de7-937">Product 2</span></span></td>
<td><span data-ttu-id="10de7-938">10001</span><span class="sxs-lookup"><span data-stu-id="10de7-938">10001</span></span></td>
<td><span data-ttu-id="10de7-939">Elektrické energie</span><span class="sxs-lookup"><span data-stu-id="10de7-939">Electricity</span></span></td>
<td><span data-ttu-id="10de7-940">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-940">Variable cost</span></span></td>
<td><span data-ttu-id="10de7-941">470.08</span><span class="sxs-lookup"><span data-stu-id="10de7-941">470.08</span></span></td>
<td><span data-ttu-id="10de7-942">31. ledna 2017</span><span class="sxs-lookup"><span data-stu-id="10de7-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="10de7-943">Závěr</span><span class="sxs-lookup"><span data-stu-id="10de7-943">Conclusion</span></span>
<span data-ttu-id="10de7-944">Ve finančním účtování se náklady za elektřinu ve výši 10 000 zaúčtují na ID fiktivního nákladového střediska.</span><span class="sxs-lookup"><span data-stu-id="10de7-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="10de7-945">Účetní tak budou vědět, že tento náklad musí být přidělen.</span><span class="sxs-lookup"><span data-stu-id="10de7-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="10de7-946">V nákladovém účetnictví náklady procházejí napříč organizačními jednotkami a úrovněmi, na základě použitých zásad a pravidel.</span><span class="sxs-lookup"><span data-stu-id="10de7-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="10de7-947">Každý náklad byl přidružen k základu přidělení, který poskytuje nejlepší hodnocení pro přidělení nákladů.</span><span class="sxs-lookup"><span data-stu-id="10de7-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="10de7-948">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="10de7-949">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="10de7-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="10de7-950">Celkem</span><span class="sxs-lookup"><span data-stu-id="10de7-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="10de7-951">CC099</span><span class="sxs-lookup"><span data-stu-id="10de7-951">CC099</span></span></th>
<th><span data-ttu-id="10de7-952">CC001</span><span class="sxs-lookup"><span data-stu-id="10de7-952">CC001</span></span></th>
<th><span data-ttu-id="10de7-953">CC002</span><span class="sxs-lookup"><span data-stu-id="10de7-953">CC002</span></span></th>
<th><span data-ttu-id="10de7-954">CC003</span><span class="sxs-lookup"><span data-stu-id="10de7-954">CC003</span></span></th>
<th><span data-ttu-id="10de7-955">CC004</span><span class="sxs-lookup"><span data-stu-id="10de7-955">CC004</span></span></th>
<th><span data-ttu-id="10de7-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="10de7-956">Proj 1</span></span></th>
<th><span data-ttu-id="10de7-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="10de7-957">Proj 2</span></span></th>
<th><span data-ttu-id="10de7-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="10de7-958">Prod 1</span></span></th>
<th><span data-ttu-id="10de7-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="10de7-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="10de7-960">10001 Elektřina</span><span class="sxs-lookup"><span data-stu-id="10de7-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10de7-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="10de7-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="10de7-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="10de7-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="10de7-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="10de7-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="10de7-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="10de7-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="10de7-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="10de7-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="10de7-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="10de7-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="10de7-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="10de7-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="10de7-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="10de7-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="10de7-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="10de7-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="10de7-970">Neklasifikované</span><span class="sxs-lookup"><span data-stu-id="10de7-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10de7-971">0,00</span><span class="sxs-lookup"><span data-stu-id="10de7-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="10de7-972">Pevné náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10de7-973">0,00</span><span class="sxs-lookup"><span data-stu-id="10de7-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10de7-974">0,00</span><span class="sxs-lookup"><span data-stu-id="10de7-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10de7-975">0,00</span><span class="sxs-lookup"><span data-stu-id="10de7-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10de7-976">0,00</span><span class="sxs-lookup"><span data-stu-id="10de7-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10de7-977">0,00</span><span class="sxs-lookup"><span data-stu-id="10de7-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="10de7-978">776.36</span><span class="sxs-lookup"><span data-stu-id="10de7-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10de7-979">223.64</span><span class="sxs-lookup"><span data-stu-id="10de7-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10de7-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="10de7-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="10de7-981">Variabilní náklady</span><span class="sxs-lookup"><span data-stu-id="10de7-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10de7-982">000</span><span class="sxs-lookup"><span data-stu-id="10de7-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10de7-983">0,00</span><span class="sxs-lookup"><span data-stu-id="10de7-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10de7-984">0,00</span><span class="sxs-lookup"><span data-stu-id="10de7-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10de7-985">0,00</span><span class="sxs-lookup"><span data-stu-id="10de7-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10de7-986">0,00</span><span class="sxs-lookup"><span data-stu-id="10de7-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10de7-987">30.00</span><span class="sxs-lookup"><span data-stu-id="10de7-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10de7-988">10,00</span><span class="sxs-lookup"><span data-stu-id="10de7-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10de7-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="10de7-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10de7-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="10de7-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="10de7-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="10de7-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="10de7-992">Toto téma popisuje, jak primární prvek nákladů, 10001 Elektřina, prochází přes objekty nákladů.</span><span class="sxs-lookup"><span data-stu-id="10de7-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="10de7-993">Tyto režijní náklady tedy budou přiděleny na nejnižší úroveň v organizaci.</span><span class="sxs-lookup"><span data-stu-id="10de7-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="10de7-994">Jinak řečeno, objekty nákladů na nejnižší úrovni ponesou náklady.</span><span class="sxs-lookup"><span data-stu-id="10de7-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="10de7-995">Chcete-li vizuální tok nákladů mezi objekty nákladů, můžete použít pravidla zásad shrnutí nákladů pro vizualizaci jejich toků.</span><span class="sxs-lookup"><span data-stu-id="10de7-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="10de7-996">Podrobnější informace naleznete v tématu [Zásady shrnutí nákladů](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="10de7-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



