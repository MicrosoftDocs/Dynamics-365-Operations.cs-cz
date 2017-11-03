---
title: "Plány kompenzace"
description: "Manažeři kompenzací a výhod mohou pomocí správy kompenzací udržovat a zpracovávat fixní i variabilní plány kompenzací pro zaměstnance organizace."
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: kherr75
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 405a298ab26e343f50cb8dd80622a414695950a7
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="compensation-plans"></a><span data-ttu-id="55a59-103">Plány kompenzace</span><span class="sxs-lookup"><span data-stu-id="55a59-103">Compensation plans</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="55a59-104">Manažeři kompenzací a výhod mohou pomocí správy kompenzací udržovat a zpracovávat fixní i variabilní plány kompenzací pro zaměstnance organizace.</span><span class="sxs-lookup"><span data-stu-id="55a59-104">Compensation and Benefits Managers can use Compensation management to maintain and process fixed and variable compensation plans for the organization's employees.</span></span>

### <a name="introduction"></a><span data-ttu-id="55a59-105">Úvod</span><span class="sxs-lookup"><span data-stu-id="55a59-105">Introduction</span></span>

<span data-ttu-id="55a59-106">Správa kompenzací se používá k řízení doručení základní mzdy a odměn.</span><span class="sxs-lookup"><span data-stu-id="55a59-106">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="55a59-107">Fixní základní mzda zaměstnance a nárůst odměn za zásluhy jsou řízeny prostřednictvím plánů fixní kompenzace.</span><span class="sxs-lookup"><span data-stu-id="55a59-107">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="55a59-108">Pobídkové platby, jako například výplaty bonusů, výkonnostních odměn, opcí na nákup akcií nebo grantů, a také jednorázové odměny jsou řízeny prostřednictvím plánů variabilní kompenzace.</span><span class="sxs-lookup"><span data-stu-id="55a59-108">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span> 

<span data-ttu-id="55a59-109">Zaměstnance lze zaregistrovat k jednomu i několika plánům obou typů.</span><span class="sxs-lookup"><span data-stu-id="55a59-109">Employees can be enrolled in one or more plans of both types.</span></span> <span data-ttu-id="55a59-110">Aby byl zaměstnanec způsobilý k registraci v plánu kompenzace, musí splňovat tyto předpoklady:</span><span class="sxs-lookup"><span data-stu-id="55a59-110">An employee must meet the following requirements in order to be eligible for enrollment in a compensation plan:</span></span>
-   <span data-ttu-id="55a59-111">Zaměstnanec musí mít přiřazenu aktivní pozici.</span><span class="sxs-lookup"><span data-stu-id="55a59-111">The employee must have an active position assignment.</span></span>
-   <span data-ttu-id="55a59-112">Zaměstnanec musí splňovat kritéria, která jsou definována pravidly způsobilosti pro plán kompenzace.</span><span class="sxs-lookup"><span data-stu-id="55a59-112">The employee must meet the criteria that are defined by eligibility rules for a compensation plan.</span></span>

## <a name="compensation-setup"></a><span data-ttu-id="55a59-113"> Nastavení kompenzace</span><span class="sxs-lookup"><span data-stu-id="55a59-113">Compensation setup</span></span>
<span data-ttu-id="55a59-114">V následující tabulce jsou uvedeny komponenty procesu kompenzace, které mohou nedílnou součástí nastavování plánů kompenzace ve vaší společnosti.</span><span class="sxs-lookup"><span data-stu-id="55a59-114">The following table lists components of the compensation process that can be integral in setting up your company's compensation plans.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="55a59-115">Součást</span><span class="sxs-lookup"><span data-stu-id="55a59-115">Component</span></span></th>
<th><span data-ttu-id="55a59-116">Více informací…</span><span class="sxs-lookup"><span data-stu-id="55a59-116">More information…</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="55a59-117">Akce fixní kompenzace</span><span class="sxs-lookup"><span data-stu-id="55a59-117">Fixed compensation actions</span></span></td>
<td><span data-ttu-id="55a59-118">Akce fixních kompenzací mají dva účely:</span><span class="sxs-lookup"><span data-stu-id="55a59-118">Fixed compensation actions accomplish two purposes:</span></span>
<ul>
<li><span data-ttu-id="55a59-119">Akce může určit druh informací, které musí být zaznamenány při změně kompenzace zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="55a59-119">Actions can specify the kind of information that must be recorded when an employee’s compensation changes.</span></span> <span data-ttu-id="55a59-120">Můžete například požadovat, aby byl zaznamenán důvody změny, jako třeba povýšení nebo naopak degradace.</span><span class="sxs-lookup"><span data-stu-id="55a59-120">For example, you can require that the reason a change, such as a promotion or a demotion be recorded.</span></span></li>
<li><span data-ttu-id="55a59-121">Akce mohou zajišťovat to, že se při zpracování plánů fixních kompenzací použijí výpočty.</span><span class="sxs-lookup"><span data-stu-id="55a59-121">Actions can ensure that a calculation is applied when fixed compensation plans are processed.</span></span>  <span data-ttu-id="55a59-122">Například akce typu Jmění porovná mzdu zaměstnance s minimálním referenčním bodem pro úroveň zaměstnance a zkontroluje, zda je zaměstnanci vypláceno alespoň minimum.</span><span class="sxs-lookup"><span data-stu-id="55a59-122">For example, actions of type Equity will compare the employees pay to the minimum reference point for the level on the employee's and ensure the employee is getting paid at least the minimum.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55a59-123">Úrovně</span><span class="sxs-lookup"><span data-stu-id="55a59-123">Levels</span></span></td>
<td><span data-ttu-id="55a59-124">Úrovně jsou přiřazeny k úlohám a všem pozicím souvisejícím s odkazy na úlohy.</span><span class="sxs-lookup"><span data-stu-id="55a59-124">Levels are associated with jobs and any positions that are related to a job reference.</span></span> <span data-ttu-id="55a59-125">Můžete vytvořit diskrétní úrovně pro tři typy plánů kompenzace: Třída, Pásmo a Krok.</span><span class="sxs-lookup"><span data-stu-id="55a59-125">You can create discrete levels for the three types of compensation plans: Grade, Band, and Step.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55a59-126">Matice využití rozsahu</span><span class="sxs-lookup"><span data-stu-id="55a59-126">Range utilization matrix</span></span></td>
<td><span data-ttu-id="55a59-127">Matice využití rozsahu pomáhá s přenosem zaměstnanců do kontrolního bodu pro jejich úlohu.</span><span class="sxs-lookup"><span data-stu-id="55a59-127">A range utilization matrix helps you transition employees to the control point for their jobs.</span></span> <span data-ttu-id="55a59-128">Díky využití rozsahu lze také řídit sazbu jmění ve společnosti bez ohledu na výkon jednotlivých zaměstnanců a celkový výkon společnosti.</span><span class="sxs-lookup"><span data-stu-id="55a59-128">You can also use range utilization to control pay rate equity in the company without regard to an individual employee's performance or the overall performance of the company.</span></span> <span data-ttu-id="55a59-129">Například zaměstnanci, kteří jsou ve svém rozsahu placeni méně, získají vyšší procentuální navýšení než zaměstnanci, kteří jsou ve svém rozsahu placeni více.</span><span class="sxs-lookup"><span data-stu-id="55a59-129">For example, employees who are paid lower in their range get higher percentage increases than employees who are paid higher in the range.</span></span> <span data-ttu-id="55a59-130">Tímto způsobem lze systematicky posunovat rozdíly ve jmění.</span><span class="sxs-lookup"><span data-stu-id="55a59-130">In this manner, you can systematically offset equity differences.</span></span> <span data-ttu-id="55a59-131">Výpočet využití rozsahu se provádí takto: (pevná mzdová sazba – minimum rozsahu) ÷ (maximum rozsahu – minimum rozsahu).</span><span class="sxs-lookup"><span data-stu-id="55a59-131">The range utilization is calculated as follows: (Fixed Pay Rate - Range Minimum) ÷ (Range Maximum - Range Minimum).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55a59-132">Nastavení referenčních bodů</span><span class="sxs-lookup"><span data-stu-id="55a59-132">Reference point setups</span></span></td>
<td><span data-ttu-id="55a59-133">Nastavení referenčních bodů zahrnuje sadu referenčních bodů představující rozsahy v matici.</span><span class="sxs-lookup"><span data-stu-id="55a59-133">A reference point setup includes a set of reference points that represent ranges in a matrix.</span></span> <span data-ttu-id="55a59-134">Každý rozsah lze přidružit k mzdové sazbě.</span><span class="sxs-lookup"><span data-stu-id="55a59-134">Each range can be associated with a pay rate.</span></span> <span data-ttu-id="55a59-135">Stupňové plány například často obsahují referenční body Minimum, Střední bod a Maximum.</span><span class="sxs-lookup"><span data-stu-id="55a59-135">For example, grade plans will often have reference points of Minimum, Midpoint, and Maximum.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55a59-136">Matice kompenzace</span><span class="sxs-lookup"><span data-stu-id="55a59-136">Compensation matrix</span></span></td>
<td><span data-ttu-id="55a59-137">Matice kompenzace je sada referenčních bodů a úrovní, které slouží k vytváření struktury kompenzací.</span><span class="sxs-lookup"><span data-stu-id="55a59-137">A compensation matrix is the set of reference points and levels that you use to create a compensation structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55a59-138">Struktura kompenzací</span><span class="sxs-lookup"><span data-stu-id="55a59-138">Compensation structure</span></span></td>
<td><span data-ttu-id="55a59-139">Struktura kompenzace je matice kompenzace s mzdovými sazbami přidruženými k referenčním bodům pro každou úroveň.</span><span class="sxs-lookup"><span data-stu-id="55a59-139">A compensation structure is a compensation matrix that has pay rates associated with the reference points for each level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55a59-140">Pravidla způsobilosti</span><span class="sxs-lookup"><span data-stu-id="55a59-140">Eligibility rules</span></span></td>
<td><span data-ttu-id="55a59-141">Pravidla způsobilosti slouží k určení pracovníků s určitými úlohami, pracovními funkcemi, typy úloh, odbory nebo oblastmi kompenzace, které jsou kryty danými plány kompenzace.</span><span class="sxs-lookup"><span data-stu-id="55a59-141">Eligibility rules are used to identify employees in specific jobs, job functions, job types, departments, labor unions, or compensation regions that are covered by specific compensation plans.</span></span> <span data-ttu-id="55a59-142">Chcete-li zařadit zaměstnance do plánu, je nutné vytvořit pravidla způsobilosti pro plány variabilní i fixní kompenzace.</span><span class="sxs-lookup"><span data-stu-id="55a59-142">You must create eligibility rules for both variable and fixed compensation plans in order to enroll employees in the plan.</span></span> <span data-ttu-id="55a59-143">Po určení pravidel způsobilosti pro plán kompenzace můžete definovat úrovně, které mají být použity pro úlohy kryté plánem.</span><span class="sxs-lookup"><span data-stu-id="55a59-143">After eligibility rules are specified for a compensation plan, you can define the levels that should apply to the jobs that are covered by the plan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55a59-144">Interval plateb</span><span class="sxs-lookup"><span data-stu-id="55a59-144">Pay frequencies</span></span></td>
<td><span data-ttu-id="55a59-145">Intervaly plateb se používají k určení časového období, pro které je zadána kompenzace.</span><span class="sxs-lookup"><span data-stu-id="55a59-145">Pay frequencies are used to define the time period for which the compensation is specified.</span></span>  <span data-ttu-id="55a59-146">Interval plateb například pomáhá s pochopením toho, jestli je částka kompenzace určována jako roční plat nebo jako hodinová mzda.</span><span class="sxs-lookup"><span data-stu-id="55a59-146">For example, the pay frequency helps you understand if the compensation amount is specified as an annual salary versus an hourly pay rate.</span></span> <span data-ttu-id="55a59-147">Intervaly plateb se také používají k nastavení koeficientů převodu pro převod částek kompenzace z měsíční, týdenní, čtrnáctidenní nebo hodinové sazby na roční interval plateb.</span><span class="sxs-lookup"><span data-stu-id="55a59-147">Pay frequencies are also used to set up conversion factors to convert compensation amounts from monthly, weekly, biweekly and hourly pay frequencies to an annual pay frequency.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55a59-148">Oblasti kompenzací</span><span class="sxs-lookup"><span data-stu-id="55a59-148">Compensation regions</span></span></td>
<td><span data-ttu-id="55a59-149">Oblasti kompenzace slouží k určení kompenzace zaměstnance na základě umístění pracovního prostředí.</span><span class="sxs-lookup"><span data-stu-id="55a59-149">Compensation regions are used to specify employee compensation based on the location of the workplace.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55a59-150">Kontrolní bod</span><span class="sxs-lookup"><span data-stu-id="55a59-150">Control point</span></span></td>
<td><span data-ttu-id="55a59-151">Kontrolní bod určuje to, co považujete za ideální sazbu pro všechny zaměstnance na úrovni kompenzace.</span><span class="sxs-lookup"><span data-stu-id="55a59-151">The control point defines what you consider to be the ideal pay rate for all employees at a compensation level.</span></span> <span data-ttu-id="55a59-152">U struktur plánů tříd jsou kontrolní body obvykle středním bodem rozsahu.</span><span class="sxs-lookup"><span data-stu-id="55a59-152">For grade plan structures, control points are typically the midpoint of the ranges.</span></span> <span data-ttu-id="55a59-153">Struktury pásma kontrolní body používají jen zřídka.</span><span class="sxs-lookup"><span data-stu-id="55a59-153">Band structures rarely use control points.</span></span> <span data-ttu-id="55a59-154">Kontrolní bod pro plán fixní kompenzace můžete určit ve formuláři Plány fixní kompenzace.</span><span class="sxs-lookup"><span data-stu-id="55a59-154">You can specify the control point for a fixed compensation plan in the Fixed compensation plans form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55a59-155">Pracovní funkce</span><span class="sxs-lookup"><span data-stu-id="55a59-155">Job functions</span></span></td>
<td><span data-ttu-id="55a59-156">Pracovní funkce se používají ke klasifikaci a k filtrování plánů kompenzací pro určité úlohy.</span><span class="sxs-lookup"><span data-stu-id="55a59-156">Job functions are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55a59-157">Typ úloh</span><span class="sxs-lookup"><span data-stu-id="55a59-157">Job types</span></span></td>
<td><span data-ttu-id="55a59-158">Typy úloh se používají ke klasifikaci a k filtrování plánů kompenzací pro určité úlohy.</span><span class="sxs-lookup"><span data-stu-id="55a59-158">Job types are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55a59-159">Typy variabilních kompenzací</span><span class="sxs-lookup"><span data-stu-id="55a59-159">Variable compensation types</span></span></td>
<td><span data-ttu-id="55a59-160">Typy variabilní kompenzace (například odměny v akciích nebo finanční bonusy) se nastavují v plánu variabilní kompenzace.</span><span class="sxs-lookup"><span data-stu-id="55a59-160">Variable compensation types, such as stock awards or cash award bonuses, are set up in variable compensation plans.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55a59-161">Kompenzační mřížky</span><span class="sxs-lookup"><span data-stu-id="55a59-161">Compensation grids</span></span></td>
<td><span data-ttu-id="55a59-162">Kompenzační mřížky obsahují strukturu kompenzací.</span><span class="sxs-lookup"><span data-stu-id="55a59-162">Compensation grids contain the compensation structure.</span></span>  <span data-ttu-id="55a59-163">Kompenzační mřížky mohou být použity jedním i několika plány kompenzace.</span><span class="sxs-lookup"><span data-stu-id="55a59-163">Compensation grids can be used by one or more compensation plans.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55a59-164">Plány výkonnosti</span><span class="sxs-lookup"><span data-stu-id="55a59-164">Performance plans</span></span></td>
<td><span data-ttu-id="55a59-165">Plány výkonnosti slouží k přidružení výkonu k matici přidělení, aby bylo možné plán použít ve strategii výkonnostní složky.</span><span class="sxs-lookup"><span data-stu-id="55a59-165">Performance plans are used to associate performance with an allocation matrix, so that you can use the plan in a pay-for-performance strategy.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55a59-166">Hodnocení výkonnosti</span><span class="sxs-lookup"><span data-stu-id="55a59-166">Performance ratings</span></span></td>
<td><span data-ttu-id="55a59-167">Hodnocení výkonnosti se používá v plánech výkonnosti k určení částky odměny za zásluhy nebo odměny za výkonnost.</span><span class="sxs-lookup"><span data-stu-id="55a59-167">Performance ratings are used in performance plans to determine the amount of a merit award or performance award.</span></span></td>
</tr>
</tbody>
</table>

## <a name="process-events"></a><span data-ttu-id="55a59-168">Procesní události</span><span class="sxs-lookup"><span data-stu-id="55a59-168">Process events</span></span>
<span data-ttu-id="55a59-169">Procesní události vypočítá informace o kompenzaci za dané časové období pro všechny zaměstnance, kteří jsou přihlášeni v jednom nebo několika plánech fixní nebo variabilní kompenzace.</span><span class="sxs-lookup"><span data-stu-id="55a59-169">A process event calculates compensation information for a specific period for all employees who are enrolled in one or more fixed or variable compensation plans.</span></span> <span data-ttu-id="55a59-170">Procesní událost lze spouštět opakovaně a tím otestovat nebo aktualizovat vypočítané výsledky kompenzace.</span><span class="sxs-lookup"><span data-stu-id="55a59-170">You can run a process event repeatedly to test or update calculated compensation results.</span></span>

<a name="compensation-events"></a><span data-ttu-id="55a59-171">Události kompenzace</span><span class="sxs-lookup"><span data-stu-id="55a59-171">Compensation events</span></span>
-------------------

<span data-ttu-id="55a59-172">Při každém spuštění procesní události se vytvoří událost kompenzace.</span><span class="sxs-lookup"><span data-stu-id="55a59-172">Each time a process event is run, a compensation event is created.</span></span>  <span data-ttu-id="55a59-173">Události kompenzace obsahují výsledky procesu kompenzace pro každého zaměstnance zahrnutého do této události procesu.</span><span class="sxs-lookup"><span data-stu-id="55a59-173">Compensation events contain the results of the compensation process for each employee included in that process event.</span></span>  <span data-ttu-id="55a59-174">Pokud jsou výpočty správné, můžete načtením události kompenzace aktualizovat záznamy kompenzace pro zaměstnance, kteří jsou ovlivněny danou procesní událostí.</span><span class="sxs-lookup"><span data-stu-id="55a59-174">When the calculations are correct, you can load the compensation event to update the compensation records for the employees who are affected by the process event.</span></span>

## <a name="recommendations"></a><span data-ttu-id="55a59-175"> Doporučení</span><span class="sxs-lookup"><span data-stu-id="55a59-175">Recommendations</span></span>
<span data-ttu-id="55a59-176">Po spuštění procesní události můžete doporučit úpravy nárůstu zásluh zaměstnance nebo částku odměny na základě vypočtených směrnic procesní události.</span><span class="sxs-lookup"><span data-stu-id="55a59-176">After you run a process event, you can recommend adjustments to an employee’s merit increase or award amount, based on the calculated guidelines of the process event.</span></span> <span data-ttu-id="55a59-177">Aby bylo možné dívat doporučení pro zaměstnance, je nutné povolit doporučení při nastavování plánů kompenzace nebo při vytváření procesní události.</span><span class="sxs-lookup"><span data-stu-id="55a59-177">To make recommendations for employees, you must enable recommendations when you set up compensation plans or when you set up the process event.</span></span>




