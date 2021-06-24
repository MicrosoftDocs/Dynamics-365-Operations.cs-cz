---
title: Uspořádání zaměstnanců pomocí oddělení, prací a pozic
description: Oddělení, úlohy a pozice jsou organizační prvky, které jsou evidovány v rámci modulu Lidské zdroje. Tento článek obsahuje koncepční informace o těchto prvcích.
author: andreabichsel
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmJob, HcmPosition, OMOperatingUnit, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 87933
ms.assetid: eb5dcacb-a5fe-451d-b30a-7ef14da65d81
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 84e7017cb0bd799e27e19fc82009307d2955dea7
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189743"
---
# <a name="organize-your-workforce-by-using-departments-jobs-and-positions"></a><span data-ttu-id="720b9-104">Uspořádání zaměstnanců pomocí oddělení, prací a pozic</span><span class="sxs-lookup"><span data-stu-id="720b9-104">Organize your workforce by using departments, jobs, and positions</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="720b9-105">Oddělení, úlohy a pozice jsou organizační prvky, které jsou evidovány v rámci modulu Lidské zdroje.</span><span class="sxs-lookup"><span data-stu-id="720b9-105">Departments, jobs, and positions are organizational elements that are maintained within Human resources.</span></span> <span data-ttu-id="720b9-106">Tento článek obsahuje koncepční informace o těchto prvcích.</span><span class="sxs-lookup"><span data-stu-id="720b9-106">This article describes conceptual information about these elements.</span></span> 

<span data-ttu-id="720b9-107">Následující příklad slouží k zobrazení konceptů popsaných v tomto článku.</span><span class="sxs-lookup"><span data-stu-id="720b9-107">The following example is used to illustrate the concepts described in this article.</span></span>

|<span data-ttu-id="720b9-108">**Oddělení**</span><span class="sxs-lookup"><span data-stu-id="720b9-108">**Department**</span></span>|<span data-ttu-id="720b9-109">**Pozice**</span><span class="sxs-lookup"><span data-stu-id="720b9-109">**Position**</span></span>|<span data-ttu-id="720b9-110">**Práce**</span><span class="sxs-lookup"><span data-stu-id="720b9-110">**Job**</span></span>|
|---|---|---|
|<span data-ttu-id="720b9-111">**Prodej.**</span><span class="sxs-lookup"><span data-stu-id="720b9-111">**Sales**</span></span>|<span data-ttu-id="720b9-112">Manažer prodeje (východ)</span><span class="sxs-lookup"><span data-stu-id="720b9-112">Sales manager (East)</span></span>|<span data-ttu-id="720b9-113">Manažer prodeje</span><span class="sxs-lookup"><span data-stu-id="720b9-113">Sales manager</span></span>|
|<span data-ttu-id="720b9-114">**Prodej**</span><span class="sxs-lookup"><span data-stu-id="720b9-114">**Sales**</span></span>|<span data-ttu-id="720b9-115">Manažer prodeje (západ)</span><span class="sxs-lookup"><span data-stu-id="720b9-115">Sales manager (West)</span></span>|<span data-ttu-id="720b9-116">Manažer prodeje</span><span class="sxs-lookup"><span data-stu-id="720b9-116">Sales manager</span></span>|
|<span data-ttu-id="720b9-117">**Prodej**</span><span class="sxs-lookup"><span data-stu-id="720b9-117">**Sales**</span></span>|<span data-ttu-id="720b9-118">Manažer prodeje (střed)</span><span class="sxs-lookup"><span data-stu-id="720b9-118">Sales manager (Central)</span></span>|<span data-ttu-id="720b9-119">Manažer prodeje</span><span class="sxs-lookup"><span data-stu-id="720b9-119">Sales manager</span></span>|
|<span data-ttu-id="720b9-120">**Účetnictví**</span><span class="sxs-lookup"><span data-stu-id="720b9-120">**Accounting**</span></span>|<span data-ttu-id="720b9-121">Účetní supervizor</span><span class="sxs-lookup"><span data-stu-id="720b9-121">Accounting supervisor</span></span>|<span data-ttu-id="720b9-122">Účetní manažer</span><span class="sxs-lookup"><span data-stu-id="720b9-122">Accounting manager</span></span>|
|<span data-ttu-id="720b9-123">**Účetnictví**</span><span class="sxs-lookup"><span data-stu-id="720b9-123">**Accounting**</span></span>|<span data-ttu-id="720b9-124">Účetnictví A</span><span class="sxs-lookup"><span data-stu-id="720b9-124">Accounting-A</span></span>|<span data-ttu-id="720b9-125">Účetní</span><span class="sxs-lookup"><span data-stu-id="720b9-125">Accountant</span></span>|
|<span data-ttu-id="720b9-126">**Lidské zdroje**</span><span class="sxs-lookup"><span data-stu-id="720b9-126">**Human resources**</span></span>|<span data-ttu-id="720b9-127">Manažer lidských zdrojů (východ)</span><span class="sxs-lookup"><span data-stu-id="720b9-127">HR manager (East)</span></span>|<span data-ttu-id="720b9-128">Manažer lidských zdrojů</span><span class="sxs-lookup"><span data-stu-id="720b9-128">HR manager</span></span>|
|<span data-ttu-id="720b9-129">**Lidské zdroje**</span><span class="sxs-lookup"><span data-stu-id="720b9-129">**Human resources**</span></span>|<span data-ttu-id="720b9-130">Manažer lidských zdrojů (západ)</span><span class="sxs-lookup"><span data-stu-id="720b9-130">HR manager (West)</span></span>|<span data-ttu-id="720b9-131">Manažer lidských zdrojů</span><span class="sxs-lookup"><span data-stu-id="720b9-131">HR manager</span></span>|
|<span data-ttu-id="720b9-132">**Lidské zdroje**</span><span class="sxs-lookup"><span data-stu-id="720b9-132">**Human resources**</span></span>|<span data-ttu-id="720b9-133">Manažer lidských zdrojů (střed)</span><span class="sxs-lookup"><span data-stu-id="720b9-133">HR manager (Central)</span></span>|<span data-ttu-id="720b9-134">Manažer lidských zdrojů</span><span class="sxs-lookup"><span data-stu-id="720b9-134">HR manager</span></span>|


##  <a name="departments"></a><span data-ttu-id="720b9-135">Oddělení</span><span class="sxs-lookup"><span data-stu-id="720b9-135">Departments</span></span>

<span data-ttu-id="720b9-136">Oddělení je provozní jednotka, která představuje kategorii nebo funkční oblast organizace, která je zodpovědná za určitou oblast organizace, jako například prodej nebo účtování.</span><span class="sxs-lookup"><span data-stu-id="720b9-136">A department is an operating unit that represents a category or functional area of an organization that is responsible for a specific area of the organization, such as sales or accounting.</span></span> <span data-ttu-id="720b9-137">Oddělení slouží k hlášení ve funkčních oblastech a může mít odpovědnost za zisky a ztráty.</span><span class="sxs-lookup"><span data-stu-id="720b9-137">A department is used to report on functional areas and may have profit and loss responsibility.</span></span> <span data-ttu-id="720b9-138">Oddělení také mohou obsahovat i skupinu nákladových středisek.</span><span class="sxs-lookup"><span data-stu-id="720b9-138">Also, a department might include a group of cost centers.</span></span> <span data-ttu-id="720b9-139">Prodej, účtování a lidské zdroje jsou některé příklady oddělení v rámci organizace.</span><span class="sxs-lookup"><span data-stu-id="720b9-139">Sales, accounting, and human resources are some examples of departments in an organization.</span></span>

## <a name="jobs-and-positions"></a><span data-ttu-id="720b9-140"> Úlohy a pozice</span><span class="sxs-lookup"><span data-stu-id="720b9-140">Jobs and positions</span></span>
<span data-ttu-id="720b9-141">Úloha je kolekce úkolů a odpovědností, které jsou vyžadovány od osoby, která provádí práci.</span><span class="sxs-lookup"><span data-stu-id="720b9-141">A job is a collection of tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="720b9-142">Pozice je individuální instance práce.</span><span class="sxs-lookup"><span data-stu-id="720b9-142">A position is an individual instance of a job.</span></span> <span data-ttu-id="720b9-143">Oblasti odpovědnosti, pracovní úkoly, pracovní funkce, dovednosti, informace o vzdělání a certifikáty, které jsou požadovány pro úlohu, jsou nutné také pro pozice, které jsou asociovány s určitou pozicí.</span><span class="sxs-lookup"><span data-stu-id="720b9-143">Areas of responsibility, job tasks, job functions, skills, education information, and certificates that are required for a job are also required for positions that are associated with a job.</span></span>
### <a name="job-tasks"></a><span data-ttu-id="720b9-144">Pracovní úkoly</span><span class="sxs-lookup"><span data-stu-id="720b9-144">Job tasks</span></span>

<span data-ttu-id="720b9-145">Můžete vytvořit pracovní úkoly, které popisují základní úlohy, které musí pracovník na pozici této úlohy dokončit.</span><span class="sxs-lookup"><span data-stu-id="720b9-145">You can create job tasks that describe the basic tasks that a worker in a position for that job must complete.</span></span> <span data-ttu-id="720b9-146">Stejnou úlohu lze přidat do více úloh a pozice pro tyto úlohy zdědí tyto úlohy.</span><span class="sxs-lookup"><span data-stu-id="720b9-146">The same job task can be added to multiple jobs, and positions for those jobs will inherit those job tasks.</span></span> <span data-ttu-id="720b9-147">Příklady pracovních úloh jsou uvedeny v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="720b9-147">Examples of job tasks are listed in the following table.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="720b9-148">Úloha</span><span class="sxs-lookup"><span data-stu-id="720b9-148">Job</span></span></th>
<th><span data-ttu-id="720b9-149">Pracovní úkol</span><span class="sxs-lookup"><span data-stu-id="720b9-149">Job task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="720b9-150">Manažer prodeje</span><span class="sxs-lookup"><span data-stu-id="720b9-150">Sales manager</span></span></td>
<td><ul>
<li><span data-ttu-id="720b9-151"><span class="input">Zkontrolovat výkon</span> – zkontrolování výkonu práce jednotlivých prodejců.</span><span class="sxs-lookup"><span data-stu-id="720b9-151"><span class="input">Perf-review</span> – Review each salesperson’s job performance.</span></span></li>
<li><span data-ttu-id="720b9-152"><span class="input">Kontrola absence</span> – schválení nebo odmítnutí požadavků nebo registrace absence jednotlivých prodejců.</span><span class="sxs-lookup"><span data-stu-id="720b9-152"><span class="input">Abs-review</span> – Approve or reject each salesperson’s absence requests or registrations.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="720b9-153">Účetní</span><span class="sxs-lookup"><span data-stu-id="720b9-153">Accountant</span></span></td>
<td><span data-ttu-id="720b9-154"><span class="input">Finanční sestava</span> – předložení týdenních finančních sestav vedoucímu finančního oddělení.</span><span class="sxs-lookup"><span data-stu-id="720b9-154"><span class="input">FIN-Report</span> – Present weekly financial reports to chief financial officer.</span></span></td>
</tr>
</tbody>
</table>

### <a name="job-functions"></a><span data-ttu-id="720b9-155">Pracovní funkce</span><span class="sxs-lookup"><span data-stu-id="720b9-155">Job functions</span></span>

<span data-ttu-id="720b9-156">Pracovní funkce jsou stejné jako pracovní úkoly.</span><span class="sxs-lookup"><span data-stu-id="720b9-156">Job functions are like job tasks.</span></span> <span data-ttu-id="720b9-157">Pracovní funkce popisuje jeden nebo více úkolů, povinností nebo odpovědností, které jsou přiřazeny k práci.</span><span class="sxs-lookup"><span data-stu-id="720b9-157">A job function describes one or more tasks, duties or responsibilities that are assigned to a job.</span></span> <span data-ttu-id="720b9-158">Pracovní funkce mohou být přiřazeny k pracím a slouží k nastavení a implementaci pravidel způsobilosti pro plány kompenzace.</span><span class="sxs-lookup"><span data-stu-id="720b9-158">Job functions can be assigned to jobs and used to set up and implement eligibility rules for compensation plans.</span></span> <span data-ttu-id="720b9-159">Příklady pracovních funkcí jsou uvedeny v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="720b9-159">Examples of job functions are listed in the following table.</span></span>

| <span data-ttu-id="720b9-160">Úloha</span><span class="sxs-lookup"><span data-stu-id="720b9-160">Job</span></span>           | <span data-ttu-id="720b9-161">Pracovní funkce</span><span class="sxs-lookup"><span data-stu-id="720b9-161">Job function</span></span>                                                |
|---------------|-------------------------------------------------------------|
| <span data-ttu-id="720b9-162">Manažer prodeje</span><span class="sxs-lookup"><span data-stu-id="720b9-162">Sales manager</span></span> | <span data-ttu-id="720b9-163">Správa osob – správa uživatelů, kteří jsou vám podřízeni.</span><span class="sxs-lookup"><span data-stu-id="720b9-163">Mng-people – Manage people who report to you.</span></span>               |
| <span data-ttu-id="720b9-164">Účetní</span><span class="sxs-lookup"><span data-stu-id="720b9-164">Accountant</span></span>    | <span data-ttu-id="720b9-165">Finanční kontrola – udržování finančních dat pro skupinu účtů.</span><span class="sxs-lookup"><span data-stu-id="720b9-165">FIN-Review – Maintain financial data for a set of accounts.</span></span> |

### <a name="job-types"></a><span data-ttu-id="720b9-166">Typ úloh</span><span class="sxs-lookup"><span data-stu-id="720b9-166">Job types</span></span>

<span data-ttu-id="720b9-167">Používejte typy úloh pro klasifikaci podobných pozic do kategorií.</span><span class="sxs-lookup"><span data-stu-id="720b9-167">Use job types to classify similar jobs into categories.</span></span> <span data-ttu-id="720b9-168">Typy úloh, jako jsou pracovní funkce, mohou být přiřazeny k pozicím a slouží k nastavení a implementaci pravidel způsobilosti pro plány kompenzace.</span><span class="sxs-lookup"><span data-stu-id="720b9-168">Job types, just like job functions, can be assigned to jobs and used to set up and implement eligibility rules for compensation plans.</span></span> <span data-ttu-id="720b9-169">V následujícím seznamu jsou uvedeny některé příklady typů úloh:</span><span class="sxs-lookup"><span data-stu-id="720b9-169">Some examples of job types are included in the following list:</span></span>
-   <span data-ttu-id="720b9-170">Plný úvazek</span><span class="sxs-lookup"><span data-stu-id="720b9-170">Full-time</span></span>
-   <span data-ttu-id="720b9-171">Částečný úvazek</span><span class="sxs-lookup"><span data-stu-id="720b9-171">Part-time</span></span>
-   <span data-ttu-id="720b9-172">Mzda</span><span class="sxs-lookup"><span data-stu-id="720b9-172">Salary</span></span>
-   <span data-ttu-id="720b9-173">Hodinová mzda</span><span class="sxs-lookup"><span data-stu-id="720b9-173">Hourly pay</span></span>

### <a name="areas-of-responsibility"></a><span data-ttu-id="720b9-174">Oblasti odpovědnosti</span><span class="sxs-lookup"><span data-stu-id="720b9-174">Areas of responsibility</span></span>

<span data-ttu-id="720b9-175">Za pomoci oblastí odpovědnosti můžete určit pracovní role, procesy a produkty, za které je pracovník na dané pozici odpovědný.</span><span class="sxs-lookup"><span data-stu-id="720b9-175">Use areas of responsibility to indicate the work roles, processes, and products that a worker in a position for that job would be responsible for.</span></span> <span data-ttu-id="720b9-176">příkladem oblasti odpovědnosti pro práci s názvem "Účetní" může být "Finanční vykazování pro produkt A".</span><span class="sxs-lookup"><span data-stu-id="720b9-176">An example of an area of responsibility for a job titled “Accountant” might be “Financial reporting for Product A”.</span></span>

## <a name="positions"></a><span data-ttu-id="720b9-177">Pozice</span><span class="sxs-lookup"><span data-stu-id="720b9-177">Positions</span></span>

<span data-ttu-id="720b9-178">Pozice jsou důležitým prvkem nižší úrovně hierarchie organizace.</span><span class="sxs-lookup"><span data-stu-id="720b9-178">Positions are an important element of the lower level of an organization hierarchy.</span></span> <span data-ttu-id="720b9-179">Pozice je individuální instance práce.</span><span class="sxs-lookup"><span data-stu-id="720b9-179">A position is an individual instance of a job.</span></span> <span data-ttu-id="720b9-180">Například pozice „Manažer prodeje (východ)“ je pouze jednou pozicí, která je přidružena k úloze „Manažer prodeje“.</span><span class="sxs-lookup"><span data-stu-id="720b9-180">For example, the position, “Sales manager (East),” is just one of the positions that is associated with the job, “Sales manager.”</span></span> <span data-ttu-id="720b9-181">Pozice existují v oddělení a jsou přiřazeny pracovníkům.</span><span class="sxs-lookup"><span data-stu-id="720b9-181">Positions exist in a department and are assigned to workers.</span></span>
### <a name="position-creation-and-maintenance"></a><span data-ttu-id="720b9-182">Vytváření a údržba pozic</span><span class="sxs-lookup"><span data-stu-id="720b9-182">Position creation and maintenance</span></span>

-   <span data-ttu-id="720b9-183">Historii systémových změn pozic můžete zobrazit na snadno dostupné stránce.</span><span class="sxs-lookup"><span data-stu-id="720b9-183">You can view a history of position-related system changes in an easy-to-access list page.</span></span>
-   <span data-ttu-id="720b9-184">Můžete vytvořit kódy důvodů, které mohou uživatelé vybrat při vytváření a změně pozic.</span><span class="sxs-lookup"><span data-stu-id="720b9-184">You can create reason codes that your users can select when they create or modify positions.</span></span>
-   <span data-ttu-id="720b9-185">Můžete vytvořit typy akcí personálu a přiřadit k uživatelským akcím číselné řady.</span><span class="sxs-lookup"><span data-stu-id="720b9-185">You can create personnel action types and assign a number sequence to personnel actions.</span></span>
-   <span data-ttu-id="720b9-186">Workflow lze nastavit tak, aby přidání a změny pozic bude vyžadovat schválení.</span><span class="sxs-lookup"><span data-stu-id="720b9-186">You can set up workflow so that position additions and changes can require approval.</span></span>

### <a name="position-duration"></a><span data-ttu-id="720b9-187">Doba trvání pozice</span><span class="sxs-lookup"><span data-stu-id="720b9-187">Position duration</span></span>

<span data-ttu-id="720b9-188">Každá pozice má časový interval, kdy je pozice platná.</span><span class="sxs-lookup"><span data-stu-id="720b9-188">Every position has a length of time that the position is effective.</span></span> <span data-ttu-id="720b9-189">Tento časový interval se nazývá trvání.</span><span class="sxs-lookup"><span data-stu-id="720b9-189">This length of time is referred to as duration.</span></span> <span data-ttu-id="720b9-190">Například můžete mít letní pozici s trváním od 1. května 2015 do 31. srpna 2015.</span><span class="sxs-lookup"><span data-stu-id="720b9-190">For example, summer positions might have duration of May 1, 2015 until August 31, 2015.</span></span>

### <a name="worker-assignments"></a><span data-ttu-id="720b9-191">Přiřazení pracovníků</span><span class="sxs-lookup"><span data-stu-id="720b9-191">Worker assignments</span></span>

<span data-ttu-id="720b9-192">Po přiřazení pracovníka k pozici dojde k zaplnění této pozice.</span><span class="sxs-lookup"><span data-stu-id="720b9-192">When you assign a worker to a position, you fill that position.</span></span> <span data-ttu-id="720b9-193">Zaměstnance lze přiřadit do více pozic, ale pouze jeden pracovní může být přiřazen na pozici současně.</span><span class="sxs-lookup"><span data-stu-id="720b9-193">You can assign workers to multiple positions, but only one worker can be assigned to a position at the same time.</span></span>

### <a name="reporting-relationships"></a><span data-ttu-id="720b9-194">Vztahy sestav</span><span class="sxs-lookup"><span data-stu-id="720b9-194">Reporting relationships</span></span>

<span data-ttu-id="720b9-195">Pozice jsou důležitým prvkem nižší úrovně hierarchie organizace.</span><span class="sxs-lookup"><span data-stu-id="720b9-195">Positions are important elements of the lower level of an organization hierarchy.</span></span> <span data-ttu-id="720b9-196">Ve formuláři Pozice můžete určit pozici, která je nadřízená vaší pozici.</span><span class="sxs-lookup"><span data-stu-id="720b9-196">In the Position form, you can specify the position that a position reports to.</span></span> <span data-ttu-id="720b9-197">Po přiřazení pracovníka k pozici, která je podřízena jiné pozici, můžete vytvořit vztah vykazování mezi zaměstnanci, kteří jsou přiřazeni do dvou pozic.</span><span class="sxs-lookup"><span data-stu-id="720b9-197">When you assign a worker to a position that reports to another position, you create a reporting relationship between the workers who are assigned to the two positions.</span></span> <span data-ttu-id="720b9-198">Například pozice "Účetní A" vykazuje do pozice "Účetní supervizor"</span><span class="sxs-lookup"><span data-stu-id="720b9-198">For example, position “Accountant-A” reports to position “Accounting Supervisor”.</span></span> <span data-ttu-id="720b9-199">Kim Akers je přiřazen na pozici "Účetní supervizor" a Sanjay Patel je přiřazen na pozici "Účetní A".</span><span class="sxs-lookup"><span data-stu-id="720b9-199">Kim Akers is assigned to position “Accounting Supervisor” and Sanjay Patel is assigned to position “Accountant-A”.</span></span> <span data-ttu-id="720b9-200">To znamená, že Sanjay Patel je podřízen uživateli Kim Akers.</span><span class="sxs-lookup"><span data-stu-id="720b9-200">This means that Sanjay Patel reports to Kim Akers.</span></span> 

<span data-ttu-id="720b9-201">Pokud vaše společnost používá hierarchii matice nebo jinou vlastní hierarchii, můžete nastavit typy hierarchií pozic a přidat vztahy podřízenosti k pozicím pro každý nastavený typ hierarchie.</span><span class="sxs-lookup"><span data-stu-id="720b9-201">If your organization uses a matrix hierarchy or another custom hierarchy, you can set up position hierarchy types and then add reporting relationships to positions for each hierarchy type that you set up.</span></span> <span data-ttu-id="720b9-202">Například Lori Penor je hlavní manažer společnosti Adventure Works a je přiřazený na pozici "Generální ředitel".</span><span class="sxs-lookup"><span data-stu-id="720b9-202">For example, Lori Penor is a general manager at Adventure Works and is assigned to the “General Manager” position.</span></span> <span data-ttu-id="720b9-203">Lori spravuje vývoj produktu, který slouží k vymazání pomůcek.</span><span class="sxs-lookup"><span data-stu-id="720b9-203">Lori manages the development of a product that is used to clean widgets.</span></span> <span data-ttu-id="720b9-204">Lori vyžaduje pomoc účetního s financemi pro vývoj produktu.</span><span class="sxs-lookup"><span data-stu-id="720b9-204">Lori requires an accountant to help with the finances for developing the product.</span></span> <span data-ttu-id="720b9-205">Proto najala Sanjay Patel jako svého účetního.</span><span class="sxs-lookup"><span data-stu-id="720b9-205">Therefore, she has recruited Sanjay Patel to be the accountant.</span></span> <span data-ttu-id="720b9-206">Sanjay je podřízen přímo pro Kim Akers, ale také pracuje s Lori Penor na jeho práci související s financemi pro vývoj produktu pro čištění pomůcek.</span><span class="sxs-lookup"><span data-stu-id="720b9-206">Sanjay reports directly to Kim Akers, but also works with Lori Penor on his work related to the finances for developing the widget cleaner.</span></span> 

<span data-ttu-id="720b9-207">V předchozím příkladu byste při nastavení pracovních vztahů mezi Sanjay Patel a Lori Penor provedli následující úkony:</span><span class="sxs-lookup"><span data-stu-id="720b9-207">For the previous example, you would complete the following tasks to set up the working relationship between Sanjay Patel and Lori Penor:</span></span>
1.  <span data-ttu-id="720b9-208">Vytvoření vlastního typu hierarchie pozice s názvem "Pomůcka" pro vytvoření hierarchie, která zahrnuje pozice odpovědné za práci na produktu pro čištění pomůcek.</span><span class="sxs-lookup"><span data-stu-id="720b9-208">Create a custom position hierarchy type called “Widget” to create a hierarchy that includes positions responsible for working on the widget cleaner product.</span></span>
2.  <span data-ttu-id="720b9-209">Přiřazení pozice Generální ředitel na pozici, která je nadřazena pozici Účetní A v hierarchie Pomůcka.</span><span class="sxs-lookup"><span data-stu-id="720b9-209">Assign the General Manager position to be the position that the Accountant-A position reports to in the Widget hierarchy.</span></span>

<span data-ttu-id="720b9-210">Použití hierarchie pozic pro zobrazení struktury hlášení pozic.</span><span class="sxs-lookup"><span data-stu-id="720b9-210">Use the position hierarchy to view the reporting structure of positions.</span></span> <span data-ttu-id="720b9-211">Pokud máte více hierarchií pozic, můžete zobrazit hierarchii pro každý typ hierarchie v hierarchii pozic.</span><span class="sxs-lookup"><span data-stu-id="720b9-211">If you have multiple position hierarchies, you can view the hierarchy for each hierarchy type in the position hierarchy.</span></span> <span data-ttu-id="720b9-212">Dále můžete vyhledávat pozici podle ID pozice nebo podle jména pracovníka, který je přiřazený na pozici.</span><span class="sxs-lookup"><span data-stu-id="720b9-212">Also, you can search for a position by position ID or by the name of the worker who is assigned to the position.</span></span> <span data-ttu-id="720b9-213">Hierarchie pozice je organizační hierarchie.</span><span class="sxs-lookup"><span data-stu-id="720b9-213">The position hierarchy is an organizational hierarchy.</span></span>

## <a name="date-effective-records"></a><span data-ttu-id="720b9-214">Časově platné záznamy</span><span class="sxs-lookup"><span data-stu-id="720b9-214">Date effective records</span></span>
<span data-ttu-id="720b9-215">Pro některé záznamy můžete určit budoucí změny tohoto záznamu.</span><span class="sxs-lookup"><span data-stu-id="720b9-215">For some records, you can specify future changes to the record.</span></span> <span data-ttu-id="720b9-216">Následující informace jsou časově platné.</span><span class="sxs-lookup"><span data-stu-id="720b9-216">The following information is date effective.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="720b9-217">Záznamy</span><span class="sxs-lookup"><span data-stu-id="720b9-217">Records</span></span></th>
<th><span data-ttu-id="720b9-218">Datum platnosti pracovníka</span><span class="sxs-lookup"><span data-stu-id="720b9-218">Date effective information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="720b9-219">Práce</span><span class="sxs-lookup"><span data-stu-id="720b9-219">Jobs</span></span></td>
<td><ul>
<li><span data-ttu-id="720b9-220">Některé podrobné informace o úloze</span><span class="sxs-lookup"><span data-stu-id="720b9-220">Some detailed job information</span></span></li>
<li><span data-ttu-id="720b9-221">Informace o klasifikaci úlohy</span><span class="sxs-lookup"><span data-stu-id="720b9-221">Job classification information</span></span></li>
<li><span data-ttu-id="720b9-222">Informace o kompenzaci</span><span class="sxs-lookup"><span data-stu-id="720b9-222">Compensation information</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="720b9-223">Pozice</span><span class="sxs-lookup"><span data-stu-id="720b9-223">Positions</span></span></td>
<td><ul>
<li><span data-ttu-id="720b9-224">Některé podrobné informace o pozici</span><span class="sxs-lookup"><span data-stu-id="720b9-224">Some detailed position information</span></span></li>
<li><span data-ttu-id="720b9-225">Přiřazení pracovníků</span><span class="sxs-lookup"><span data-stu-id="720b9-225">Worker assignments</span></span></li>
<li><span data-ttu-id="720b9-226">Doby trvání pozice</span><span class="sxs-lookup"><span data-stu-id="720b9-226">Position durations</span></span></li>
<li><span data-ttu-id="720b9-227">Hierarchie pozic</span><span class="sxs-lookup"><span data-stu-id="720b9-227">Position hierarchies</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="720b9-228">Můžete upravovat údaje uvedené v předchozí tabulce pro pozice nebo úlohy a zadat datum, kdy by se změny pozice pro vybrané úlohy měly projevit.</span><span class="sxs-lookup"><span data-stu-id="720b9-228">You can modify the information mentioned in the previous table for a position or a job and specify a date when the modifications to the position or job should take effect.</span></span> <span data-ttu-id="720b9-229">Například pozice lze přiřadit pouze jednomu pracovníkovi, ale Sanjay Patel, který je přiřazený k pozici Účetní A odchází za dva týdny.</span><span class="sxs-lookup"><span data-stu-id="720b9-229">For example, a position can only be assigned to one worker, but Sanjay Patel, who is assigned to the position Accountant-A, will be leaving in two weeks.</span></span> <span data-ttu-id="720b9-230">Joe Healy nahradí Sanjay Patel po jeho odchodu.</span><span class="sxs-lookup"><span data-stu-id="720b9-230">Joe Healy will replace Sanjay Patel when Sanjay leaves.</span></span> <span data-ttu-id="720b9-231">Přestože Sanjay je i nadále přiřazen na svoji pozici, můžete přiřadit Jan Healy na stejnou pozici tak, aby přiřazení nabylo platnosti až po posledním dni Sanjay.</span><span class="sxs-lookup"><span data-stu-id="720b9-231">Even though Sanjay is still assigned to his position, you can assign Joe Healy to the same position so that the assignment is effective only after Sanjay’s last day.</span></span>







[!INCLUDE[footer-include](../includes/footer-banner.md)]