---
title: Tabulky Dataverse
description: Microsoft Dynamics 365 Human Resources používá Dataverse k povolení scénářů rozšiřitelnosti a integrace.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 325bd8a9de07e3978ff6c513975a0e8db22854e0
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054349"
---
# <a name="dataverse-tables"></a><span data-ttu-id="43dfd-103">Tabulky Dataverse</span><span class="sxs-lookup"><span data-stu-id="43dfd-103">Dataverse tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="43dfd-104">Microsoft Dynamics 365 Human Resources používá Dataverse k povolení scénářů rozšiřitelnosti a integrace.</span><span class="sxs-lookup"><span data-stu-id="43dfd-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="43dfd-105">Entity Human Resources odpovídají Dataverse tabulkám.</span><span class="sxs-lookup"><span data-stu-id="43dfd-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="43dfd-106">Pro více informací o Dataverse (dříve Common Data Service) a aktualizacích terminologie, viz [Co je Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="43dfd-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="43dfd-107">Následující tabulky Dataverse jsou k dispozici na základě entit lidských zdrojů.</span><span class="sxs-lookup"><span data-stu-id="43dfd-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="43dfd-108">Tabulky výhod</span><span class="sxs-lookup"><span data-stu-id="43dfd-108">Benefit tables</span></span>

| <span data-ttu-id="43dfd-109">Jméno</span><span class="sxs-lookup"><span data-stu-id="43dfd-109">Name</span></span> | <span data-ttu-id="43dfd-110">Tabulka</span><span class="sxs-lookup"><span data-stu-id="43dfd-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="43dfd-111">Frekvence výpočtu zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="43dfd-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="43dfd-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="43dfd-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="43dfd-113">Platební období – interval provádění výpočtu zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="43dfd-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="43dfd-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="43dfd-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="43dfd-115">Sazba výpočtu zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="43dfd-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="43dfd-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="43dfd-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="43dfd-117">Podrobnosti sazby výpočtu zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="43dfd-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="43dfd-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="43dfd-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="43dfd-119">Možnost zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="43dfd-119">Benefit Option</span></span> | <span data-ttu-id="43dfd-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="43dfd-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="43dfd-121">Plán zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="43dfd-121">Benefit Plan</span></span> | <span data-ttu-id="43dfd-122">cdm_benefitplan (není povoleno pro podporu vlastních polí)</span><span class="sxs-lookup"><span data-stu-id="43dfd-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="43dfd-123">Typ zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="43dfd-123">Benefit Type</span></span> | <span data-ttu-id="43dfd-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="43dfd-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="43dfd-125">Tabulky úkolů obchodního procesu</span><span class="sxs-lookup"><span data-stu-id="43dfd-125">Business process tasks tables</span></span>

| <span data-ttu-id="43dfd-126">Jméno</span><span class="sxs-lookup"><span data-stu-id="43dfd-126">Name</span></span> | <span data-ttu-id="43dfd-127">Tabulka</span><span class="sxs-lookup"><span data-stu-id="43dfd-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="43dfd-128">Kalendář obchodních procesů</span><span class="sxs-lookup"><span data-stu-id="43dfd-128">Business Process Calendar</span></span> | <span data-ttu-id="43dfd-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="43dfd-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="43dfd-130">Přiřazení skupiny obchodních procesů</span><span class="sxs-lookup"><span data-stu-id="43dfd-130">Business Process Group Assignment</span></span> | <span data-ttu-id="43dfd-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="43dfd-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="43dfd-132">Skupina úkolů knihovny obchodních procesů</span><span class="sxs-lookup"><span data-stu-id="43dfd-132">Business Process Library Task Group</span></span> | <span data-ttu-id="43dfd-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="43dfd-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="43dfd-134">Fáze obchodního procesu</span><span class="sxs-lookup"><span data-stu-id="43dfd-134">Business Process Stage</span></span> | <span data-ttu-id="43dfd-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="43dfd-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="43dfd-136">Záhlaví šablony kontrolního seznamu</span><span class="sxs-lookup"><span data-stu-id="43dfd-136">Checklist Template Header</span></span> | <span data-ttu-id="43dfd-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="43dfd-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="43dfd-138">Úkol šablony kontrolního seznamu</span><span class="sxs-lookup"><span data-stu-id="43dfd-138">Checklist Template Task</span></span> | <span data-ttu-id="43dfd-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="43dfd-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="43dfd-140">Tabulky Kompenzace</span><span class="sxs-lookup"><span data-stu-id="43dfd-140">Compensation tables</span></span>

| <span data-ttu-id="43dfd-141">Jméno</span><span class="sxs-lookup"><span data-stu-id="43dfd-141">Name</span></span> | <span data-ttu-id="43dfd-142">Tabulka</span><span class="sxs-lookup"><span data-stu-id="43dfd-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="43dfd-143">Fixní plán kompenzace</span><span class="sxs-lookup"><span data-stu-id="43dfd-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="43dfd-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="43dfd-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="43dfd-145">Mřížka kompenzace</span><span class="sxs-lookup"><span data-stu-id="43dfd-145">Compensation Grid</span></span> | <span data-ttu-id="43dfd-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="43dfd-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="43dfd-147">Úroveň kompenzace</span><span class="sxs-lookup"><span data-stu-id="43dfd-147">Compensation Level</span></span> | <span data-ttu-id="43dfd-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="43dfd-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="43dfd-149">Interval plateb kompenzace</span><span class="sxs-lookup"><span data-stu-id="43dfd-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="43dfd-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="43dfd-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="43dfd-151">Nastavení referenčního bodu kompenzace</span><span class="sxs-lookup"><span data-stu-id="43dfd-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="43dfd-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="43dfd-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="43dfd-153">Linie nastavení referenčního bodu kompenzace</span><span class="sxs-lookup"><span data-stu-id="43dfd-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="43dfd-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="43dfd-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="43dfd-155">Oblast kompenzace</span><span class="sxs-lookup"><span data-stu-id="43dfd-155">Compensation Region</span></span> | <span data-ttu-id="43dfd-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="43dfd-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="43dfd-157">Struktura kompenzací</span><span class="sxs-lookup"><span data-stu-id="43dfd-157">Compensation Structure</span></span> | <span data-ttu-id="43dfd-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="43dfd-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="43dfd-159">Plán variabilní kompenzace</span><span class="sxs-lookup"><span data-stu-id="43dfd-159">Compensation Variable Plan</span></span> | <span data-ttu-id="43dfd-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="43dfd-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="43dfd-161">Úroveň plánu variabilní kompenzace</span><span class="sxs-lookup"><span data-stu-id="43dfd-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="43dfd-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="43dfd-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="43dfd-163">Typ plánu variabilní kompenzace</span><span class="sxs-lookup"><span data-stu-id="43dfd-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="43dfd-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="43dfd-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="43dfd-165">Událost fixní kompenzace</span><span class="sxs-lookup"><span data-stu-id="43dfd-165">Fixed Compensation Event</span></span> | <span data-ttu-id="43dfd-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="43dfd-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="43dfd-167">Pravidlo připsání</span><span class="sxs-lookup"><span data-stu-id="43dfd-167">Vesting Rule</span></span> | <span data-ttu-id="43dfd-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="43dfd-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="43dfd-169">Fixní kompenzace pracovníka</span><span class="sxs-lookup"><span data-stu-id="43dfd-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="43dfd-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="43dfd-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="43dfd-171">Organizační tabulky</span><span class="sxs-lookup"><span data-stu-id="43dfd-171">Organization tables</span></span>

| <span data-ttu-id="43dfd-172">Jméno</span><span class="sxs-lookup"><span data-stu-id="43dfd-172">Name</span></span> | <span data-ttu-id="43dfd-173">Tabulka</span><span class="sxs-lookup"><span data-stu-id="43dfd-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="43dfd-174">Oddělení</span><span class="sxs-lookup"><span data-stu-id="43dfd-174">Department</span></span> | <span data-ttu-id="43dfd-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="43dfd-175">cdm_department</span></span> |
| <span data-ttu-id="43dfd-176">Zaměstnání</span><span class="sxs-lookup"><span data-stu-id="43dfd-176">Employment</span></span> | <span data-ttu-id="43dfd-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="43dfd-177">cdm_employment</span></span> |
| <span data-ttu-id="43dfd-178">Společnost</span><span class="sxs-lookup"><span data-stu-id="43dfd-178">Company</span></span> | <span data-ttu-id="43dfd-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="43dfd-179">cdm_company</span></span> |
| <span data-ttu-id="43dfd-180">Pozice</span><span class="sxs-lookup"><span data-stu-id="43dfd-180">Job</span></span> | <span data-ttu-id="43dfd-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="43dfd-181">cdm_job</span></span> |
| <span data-ttu-id="43dfd-182">Pracovní funkce</span><span class="sxs-lookup"><span data-stu-id="43dfd-182">Job Function</span></span> | <span data-ttu-id="43dfd-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="43dfd-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="43dfd-184">Pracovní pozice</span><span class="sxs-lookup"><span data-stu-id="43dfd-184">Job Position</span></span> | <span data-ttu-id="43dfd-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="43dfd-185">cdm_jobposition</span></span> |
| <span data-ttu-id="43dfd-186">Typ pozice</span><span class="sxs-lookup"><span data-stu-id="43dfd-186">Position Type</span></span> | <span data-ttu-id="43dfd-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="43dfd-187">cdm_positiontype</span></span> |
| <span data-ttu-id="43dfd-188">Přiřazení pracovníka k pozici</span><span class="sxs-lookup"><span data-stu-id="43dfd-188">Position Worker Assignment</span></span> | <span data-ttu-id="43dfd-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="43dfd-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="43dfd-190">Dimenze pracovních pozic</span><span class="sxs-lookup"><span data-stu-id="43dfd-190">Job Position Dimension</span></span> | <span data-ttu-id="43dfd-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="43dfd-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="43dfd-192">Typ práce</span><span class="sxs-lookup"><span data-stu-id="43dfd-192">Job Type</span></span> | <span data-ttu-id="43dfd-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="43dfd-193">cdm_jobtype</span></span> |
| <span data-ttu-id="43dfd-194">Jazyk</span><span class="sxs-lookup"><span data-stu-id="43dfd-194">Language</span></span> | <span data-ttu-id="43dfd-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="43dfd-195">cdm_language</span></span> |
| <span data-ttu-id="43dfd-196">Pozice</span><span class="sxs-lookup"><span data-stu-id="43dfd-196">Title</span></span> | <span data-ttu-id="43dfd-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="43dfd-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="43dfd-198">Finanční dimenze pro **Typ pozice**, **Přiřazení pracovníka poziec** a **Zaměstnání** poskytují integraci v jediném směru do Dataverse.</span><span class="sxs-lookup"><span data-stu-id="43dfd-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="43dfd-199">Aktualizace finančních dimenzí nelze v současné době synchronizovat z Dataverse do modulu Human Resources.</span><span class="sxs-lookup"><span data-stu-id="43dfd-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="43dfd-200">Tabulky Pracovní volno a absence</span><span class="sxs-lookup"><span data-stu-id="43dfd-200">Leave and absence tables</span></span>

| <span data-ttu-id="43dfd-201">Jméno</span><span class="sxs-lookup"><span data-stu-id="43dfd-201">Name</span></span> | <span data-ttu-id="43dfd-202">Tabulka</span><span class="sxs-lookup"><span data-stu-id="43dfd-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="43dfd-203">Transakce fondu pracovního volna</span><span class="sxs-lookup"><span data-stu-id="43dfd-203">Leave Bank Transaction</span></span> | <span data-ttu-id="43dfd-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="43dfd-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="43dfd-205">Registrace pracovního volna</span><span class="sxs-lookup"><span data-stu-id="43dfd-205">Leave Enrollment</span></span> | <span data-ttu-id="43dfd-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="43dfd-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="43dfd-207">Plán pracovního volna</span><span class="sxs-lookup"><span data-stu-id="43dfd-207">Leave Plan</span></span> | <span data-ttu-id="43dfd-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="43dfd-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="43dfd-209">Žádost o pracovní volno</span><span class="sxs-lookup"><span data-stu-id="43dfd-209">Leave Request</span></span> | <span data-ttu-id="43dfd-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="43dfd-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="43dfd-211">Podrobnosti o požadavku na dovolenou</span><span class="sxs-lookup"><span data-stu-id="43dfd-211">Leave Request Detail</span></span> | <span data-ttu-id="43dfd-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="43dfd-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="43dfd-213">Typ pracovního volna</span><span class="sxs-lookup"><span data-stu-id="43dfd-213">Leave Type</span></span> | <span data-ttu-id="43dfd-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="43dfd-214">cdm_leavetype</span></span> |
| <span data-ttu-id="43dfd-215">Kód důvodu typu volna</span><span class="sxs-lookup"><span data-stu-id="43dfd-215">Leave Type Reason Code</span></span> | <span data-ttu-id="43dfd-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="43dfd-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="43dfd-217">Výplatní tabulky</span><span class="sxs-lookup"><span data-stu-id="43dfd-217">Payroll tables</span></span>

| <span data-ttu-id="43dfd-218">Jméno</span><span class="sxs-lookup"><span data-stu-id="43dfd-218">Name</span></span> | <span data-ttu-id="43dfd-219">Tabulka</span><span class="sxs-lookup"><span data-stu-id="43dfd-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="43dfd-220">Platební cyklus</span><span class="sxs-lookup"><span data-stu-id="43dfd-220">Pay Cycle</span></span> | <span data-ttu-id="43dfd-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="43dfd-221">cdm_paycycle</span></span> |
| <span data-ttu-id="43dfd-222">Platební období</span><span class="sxs-lookup"><span data-stu-id="43dfd-222">Pay Period</span></span> | <span data-ttu-id="43dfd-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="43dfd-223">cdm_payperiod</span></span> |
| <span data-ttu-id="43dfd-224">Kód příjmů mzdy</span><span class="sxs-lookup"><span data-stu-id="43dfd-224">Payroll Earning Code</span></span> | <span data-ttu-id="43dfd-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="43dfd-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="43dfd-226">Úhrady na bankovní účet</span><span class="sxs-lookup"><span data-stu-id="43dfd-226">Bank Account Disbursement</span></span> | <span data-ttu-id="43dfd-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="43dfd-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="43dfd-228">Daňová oblast</span><span class="sxs-lookup"><span data-stu-id="43dfd-228">Tax Region</span></span> | <span data-ttu-id="43dfd-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="43dfd-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="43dfd-230">Tabulky pracovníků</span><span class="sxs-lookup"><span data-stu-id="43dfd-230">Worker tables</span></span>

| <span data-ttu-id="43dfd-231">Jméno</span><span class="sxs-lookup"><span data-stu-id="43dfd-231">Name</span></span> | <span data-ttu-id="43dfd-232">Tabulka</span><span class="sxs-lookup"><span data-stu-id="43dfd-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="43dfd-233">Pracovní podproces</span><span class="sxs-lookup"><span data-stu-id="43dfd-233">Worker</span></span> | <span data-ttu-id="43dfd-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="43dfd-234">cdm_worker</span></span> |
| <span data-ttu-id="43dfd-235">Adresa pracovníka</span><span class="sxs-lookup"><span data-stu-id="43dfd-235">Worker Address</span></span> | <span data-ttu-id="43dfd-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="43dfd-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="43dfd-237">Osobní údaj pracovníka</span><span class="sxs-lookup"><span data-stu-id="43dfd-237">Worker Personal Detail</span></span> | <span data-ttu-id="43dfd-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="43dfd-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="43dfd-239">Osobní identifikační číslo pracovníka</span><span class="sxs-lookup"><span data-stu-id="43dfd-239">Worker Person Identification Number</span></span> | <span data-ttu-id="43dfd-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="43dfd-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="43dfd-241">Typ osobní identifikace pracovníka</span><span class="sxs-lookup"><span data-stu-id="43dfd-241">Worker Person Identification Type</span></span> | <span data-ttu-id="43dfd-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="43dfd-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="43dfd-243">Pracovní kalendář</span><span class="sxs-lookup"><span data-stu-id="43dfd-243">Work Calendar</span></span> | <span data-ttu-id="43dfd-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="43dfd-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="43dfd-245">Datum pracovního kalendáře</span><span class="sxs-lookup"><span data-stu-id="43dfd-245">Work Calendar Day</span></span> | <span data-ttu-id="43dfd-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="43dfd-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="43dfd-247">Svátek pracovního kalendáře</span><span class="sxs-lookup"><span data-stu-id="43dfd-247">Work Calendar Holiday</span></span> |<span data-ttu-id="43dfd-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="43dfd-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="43dfd-249">Řádek data pracovního kalendáře</span><span class="sxs-lookup"><span data-stu-id="43dfd-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="43dfd-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="43dfd-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="43dfd-251">Časový interval pracovního kalenáře</span><span class="sxs-lookup"><span data-stu-id="43dfd-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="43dfd-252">cdm_workcalendartimeinterval (není povoleno pro podporu vlastních polí)</span><span class="sxs-lookup"><span data-stu-id="43dfd-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="43dfd-253">Bankovní účet pracovníka</span><span class="sxs-lookup"><span data-stu-id="43dfd-253">Worker Bank Account</span></span> | <span data-ttu-id="43dfd-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="43dfd-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="43dfd-255">Tabulky nastavení pracovníků</span><span class="sxs-lookup"><span data-stu-id="43dfd-255">Worker setup tables</span></span>

| <span data-ttu-id="43dfd-256">Jméno</span><span class="sxs-lookup"><span data-stu-id="43dfd-256">Name</span></span> | <span data-ttu-id="43dfd-257">Tabulka</span><span class="sxs-lookup"><span data-stu-id="43dfd-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="43dfd-258">Stav veterána</span><span class="sxs-lookup"><span data-stu-id="43dfd-258">Veteran Status</span></span> | <span data-ttu-id="43dfd-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="43dfd-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="43dfd-260">Etnický původ</span><span class="sxs-lookup"><span data-stu-id="43dfd-260">Ethnic Origin</span></span> | <span data-ttu-id="43dfd-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="43dfd-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="43dfd-262">Kód důvodu</span><span class="sxs-lookup"><span data-stu-id="43dfd-262">Reason Code</span></span> | <span data-ttu-id="43dfd-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="43dfd-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="43dfd-264">Úřad vydávající identifikaci osoby</span><span class="sxs-lookup"><span data-stu-id="43dfd-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="43dfd-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="43dfd-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="43dfd-266">Tabulky kompetencí</span><span class="sxs-lookup"><span data-stu-id="43dfd-266">Competency tables</span></span>

| <span data-ttu-id="43dfd-267">Jméno</span><span class="sxs-lookup"><span data-stu-id="43dfd-267">Name</span></span> | <span data-ttu-id="43dfd-268">Tabulka</span><span class="sxs-lookup"><span data-stu-id="43dfd-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="43dfd-269">Typ dovednosti</span><span class="sxs-lookup"><span data-stu-id="43dfd-269">Skill Type</span></span> | <span data-ttu-id="43dfd-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="43dfd-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="43dfd-271">Modely vztahů tabulek</span><span class="sxs-lookup"><span data-stu-id="43dfd-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="43dfd-272">Pracovní podproces</span><span class="sxs-lookup"><span data-stu-id="43dfd-272">Worker</span></span>

![Pracovní podproces](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="43dfd-274">Práce a pracovní pozice</span><span class="sxs-lookup"><span data-stu-id="43dfd-274">Job and Job Position</span></span>

![Práce a pracovní pozice](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="43dfd-276">Zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="43dfd-276">Benefits</span></span>

![Zaměstnanecké výhody](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="43dfd-278">Kompenzace</span><span class="sxs-lookup"><span data-stu-id="43dfd-278">Compensation</span></span>

![Kompenzace](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="43dfd-280">Odejít</span><span class="sxs-lookup"><span data-stu-id="43dfd-280">Leave</span></span>

![Odejít](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="43dfd-282">Pracovní kalendář</span><span class="sxs-lookup"><span data-stu-id="43dfd-282">Work Calendar</span></span>

![Pracovní kalendář](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="43dfd-284">Viz také</span><span class="sxs-lookup"><span data-stu-id="43dfd-284">See also</span></span>

[<span data-ttu-id="43dfd-285">Volba technologie integrace dat</span><span class="sxs-lookup"><span data-stu-id="43dfd-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="43dfd-286">Konfigurace integrace s Dataverse</span><span class="sxs-lookup"><span data-stu-id="43dfd-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="43dfd-287">Konfigurace virtuálních tabulek Dataverse</span><span class="sxs-lookup"><span data-stu-id="43dfd-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="43dfd-288">Virtuální tabulky lidských zdrojů - časté dotazy</span><span class="sxs-lookup"><span data-stu-id="43dfd-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="43dfd-289">Co je Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="43dfd-289">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="43dfd-290">Aktualizace terminologie</span><span class="sxs-lookup"><span data-stu-id="43dfd-290">Terminology updates</span></span>](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]