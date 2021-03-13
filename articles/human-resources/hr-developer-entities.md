---
title: Tabulky Dataverse
description: Microsoft Dynamics 365 Human Resources používá Dataverse k povolení scénářů rozšiřitelnosti a integrace.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2f075a8e96af55b1363d2d51db377c5b25c38775
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111818"
---
# <a name="dataverse-tables"></a><span data-ttu-id="92dbd-103">Tabulky Dataverse</span><span class="sxs-lookup"><span data-stu-id="92dbd-103">Dataverse tables</span></span>

<span data-ttu-id="92dbd-104">Microsoft Dynamics 365 Human Resources používá Dataverse k povolení scénářů rozšiřitelnosti a integrace.</span><span class="sxs-lookup"><span data-stu-id="92dbd-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="92dbd-105">Entity Human Resources odpovídají Dataverse tabulkám.</span><span class="sxs-lookup"><span data-stu-id="92dbd-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="92dbd-106">Pro více informací o Dataverse (dříve Common Data Service) a aktualizacích terminologie, viz [Co je Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="92dbd-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="92dbd-107">Následující tabulky Dataverse jsou k dispozici na základě entit lidských zdrojů.</span><span class="sxs-lookup"><span data-stu-id="92dbd-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="92dbd-108">Tabulky výhod</span><span class="sxs-lookup"><span data-stu-id="92dbd-108">Benefit tables</span></span>

| <span data-ttu-id="92dbd-109">Jméno</span><span class="sxs-lookup"><span data-stu-id="92dbd-109">Name</span></span> | <span data-ttu-id="92dbd-110">Tabulka</span><span class="sxs-lookup"><span data-stu-id="92dbd-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="92dbd-111">Frekvence výpočtu zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="92dbd-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="92dbd-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="92dbd-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="92dbd-113">Platební období – interval provádění výpočtu zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="92dbd-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="92dbd-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="92dbd-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="92dbd-115">Sazba výpočtu zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="92dbd-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="92dbd-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="92dbd-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="92dbd-117">Podrobnosti sazby výpočtu zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="92dbd-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="92dbd-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="92dbd-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="92dbd-119">Možnost zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="92dbd-119">Benefit Option</span></span> | <span data-ttu-id="92dbd-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="92dbd-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="92dbd-121">Plán zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="92dbd-121">Benefit Plan</span></span> | <span data-ttu-id="92dbd-122">cdm_benefitplan (není povoleno pro podporu vlastních polí)</span><span class="sxs-lookup"><span data-stu-id="92dbd-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="92dbd-123">Typ zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="92dbd-123">Benefit Type</span></span> | <span data-ttu-id="92dbd-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="92dbd-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="92dbd-125">Tabulky úkolů obchodního procesu</span><span class="sxs-lookup"><span data-stu-id="92dbd-125">Business process tasks tables</span></span>

| <span data-ttu-id="92dbd-126">Jméno</span><span class="sxs-lookup"><span data-stu-id="92dbd-126">Name</span></span> | <span data-ttu-id="92dbd-127">Tabulka</span><span class="sxs-lookup"><span data-stu-id="92dbd-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="92dbd-128">Kalendář obchodních procesů</span><span class="sxs-lookup"><span data-stu-id="92dbd-128">Business Process Calendar</span></span> | <span data-ttu-id="92dbd-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="92dbd-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="92dbd-130">Přiřazení skupiny obchodních procesů</span><span class="sxs-lookup"><span data-stu-id="92dbd-130">Business Process Group Assignment</span></span> | <span data-ttu-id="92dbd-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="92dbd-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="92dbd-132">Skupina úkolů knihovny obchodních procesů</span><span class="sxs-lookup"><span data-stu-id="92dbd-132">Business Process Library Task Group</span></span> | <span data-ttu-id="92dbd-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="92dbd-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="92dbd-134">Fáze obchodního procesu</span><span class="sxs-lookup"><span data-stu-id="92dbd-134">Business Process Stage</span></span> | <span data-ttu-id="92dbd-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="92dbd-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="92dbd-136">Záhlaví šablony kontrolního seznamu</span><span class="sxs-lookup"><span data-stu-id="92dbd-136">Checklist Template Header</span></span> | <span data-ttu-id="92dbd-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="92dbd-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="92dbd-138">Úkol šablony kontrolního seznamu</span><span class="sxs-lookup"><span data-stu-id="92dbd-138">Checklist Template Task</span></span> | <span data-ttu-id="92dbd-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="92dbd-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="92dbd-140">Tabulky Kompenzace</span><span class="sxs-lookup"><span data-stu-id="92dbd-140">Compensation tables</span></span>

| <span data-ttu-id="92dbd-141">Jméno</span><span class="sxs-lookup"><span data-stu-id="92dbd-141">Name</span></span> | <span data-ttu-id="92dbd-142">Tabulka</span><span class="sxs-lookup"><span data-stu-id="92dbd-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="92dbd-143">Fixní plán kompenzace</span><span class="sxs-lookup"><span data-stu-id="92dbd-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="92dbd-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="92dbd-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="92dbd-145">Mřížka kompenzace</span><span class="sxs-lookup"><span data-stu-id="92dbd-145">Compensation Grid</span></span> | <span data-ttu-id="92dbd-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="92dbd-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="92dbd-147">Úroveň kompenzace</span><span class="sxs-lookup"><span data-stu-id="92dbd-147">Compensation Level</span></span> | <span data-ttu-id="92dbd-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="92dbd-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="92dbd-149">Interval plateb kompenzace</span><span class="sxs-lookup"><span data-stu-id="92dbd-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="92dbd-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="92dbd-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="92dbd-151">Nastavení referenčního bodu kompenzace</span><span class="sxs-lookup"><span data-stu-id="92dbd-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="92dbd-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="92dbd-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="92dbd-153">Linie nastavení referenčního bodu kompenzace</span><span class="sxs-lookup"><span data-stu-id="92dbd-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="92dbd-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="92dbd-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="92dbd-155">Oblast kompenzace</span><span class="sxs-lookup"><span data-stu-id="92dbd-155">Compensation Region</span></span> | <span data-ttu-id="92dbd-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="92dbd-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="92dbd-157">Struktura kompenzací</span><span class="sxs-lookup"><span data-stu-id="92dbd-157">Compensation Structure</span></span> | <span data-ttu-id="92dbd-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="92dbd-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="92dbd-159">Plán variabilní kompenzace</span><span class="sxs-lookup"><span data-stu-id="92dbd-159">Compensation Variable Plan</span></span> | <span data-ttu-id="92dbd-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="92dbd-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="92dbd-161">Úroveň plánu variabilní kompenzace</span><span class="sxs-lookup"><span data-stu-id="92dbd-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="92dbd-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="92dbd-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="92dbd-163">Typ plánu variabilní kompenzace</span><span class="sxs-lookup"><span data-stu-id="92dbd-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="92dbd-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="92dbd-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="92dbd-165">Událost fixní kompenzace</span><span class="sxs-lookup"><span data-stu-id="92dbd-165">Fixed Compensation Event</span></span> | <span data-ttu-id="92dbd-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="92dbd-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="92dbd-167">Pravidlo připsání</span><span class="sxs-lookup"><span data-stu-id="92dbd-167">Vesting Rule</span></span> | <span data-ttu-id="92dbd-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="92dbd-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="92dbd-169">Fixní kompenzace pracovníka</span><span class="sxs-lookup"><span data-stu-id="92dbd-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="92dbd-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="92dbd-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="92dbd-171">Organizační tabulky</span><span class="sxs-lookup"><span data-stu-id="92dbd-171">Organization tables</span></span>

| <span data-ttu-id="92dbd-172">Jméno</span><span class="sxs-lookup"><span data-stu-id="92dbd-172">Name</span></span> | <span data-ttu-id="92dbd-173">Tabulka</span><span class="sxs-lookup"><span data-stu-id="92dbd-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="92dbd-174">Oddělení</span><span class="sxs-lookup"><span data-stu-id="92dbd-174">Department</span></span> | <span data-ttu-id="92dbd-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="92dbd-175">cdm_department</span></span> |
| <span data-ttu-id="92dbd-176">Zaměstnání</span><span class="sxs-lookup"><span data-stu-id="92dbd-176">Employment</span></span> | <span data-ttu-id="92dbd-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="92dbd-177">cdm_employment</span></span> |
| <span data-ttu-id="92dbd-178">Společnost</span><span class="sxs-lookup"><span data-stu-id="92dbd-178">Company</span></span> | <span data-ttu-id="92dbd-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="92dbd-179">cdm_company</span></span> |
| <span data-ttu-id="92dbd-180">Pozice</span><span class="sxs-lookup"><span data-stu-id="92dbd-180">Job</span></span> | <span data-ttu-id="92dbd-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="92dbd-181">cdm_job</span></span> |
| <span data-ttu-id="92dbd-182">Pracovní funkce</span><span class="sxs-lookup"><span data-stu-id="92dbd-182">Job Function</span></span> | <span data-ttu-id="92dbd-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="92dbd-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="92dbd-184">Pracovní pozice</span><span class="sxs-lookup"><span data-stu-id="92dbd-184">Job Position</span></span> | <span data-ttu-id="92dbd-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="92dbd-185">cdm_jobposition</span></span> |
| <span data-ttu-id="92dbd-186">Typ pozice</span><span class="sxs-lookup"><span data-stu-id="92dbd-186">Position Type</span></span> | <span data-ttu-id="92dbd-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="92dbd-187">cdm_positiontype</span></span> |
| <span data-ttu-id="92dbd-188">Přiřazení pracovníka k pozici</span><span class="sxs-lookup"><span data-stu-id="92dbd-188">Position Worker Assignment</span></span> | <span data-ttu-id="92dbd-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="92dbd-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="92dbd-190">Dimenze pracovních pozic</span><span class="sxs-lookup"><span data-stu-id="92dbd-190">Job Position Dimension</span></span> | <span data-ttu-id="92dbd-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="92dbd-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="92dbd-192">Typ práce</span><span class="sxs-lookup"><span data-stu-id="92dbd-192">Job Type</span></span> | <span data-ttu-id="92dbd-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="92dbd-193">cdm_jobtype</span></span> |
| <span data-ttu-id="92dbd-194">Jazyk</span><span class="sxs-lookup"><span data-stu-id="92dbd-194">Language</span></span> | <span data-ttu-id="92dbd-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="92dbd-195">cdm_language</span></span> |
| <span data-ttu-id="92dbd-196">Pozice</span><span class="sxs-lookup"><span data-stu-id="92dbd-196">Title</span></span> | <span data-ttu-id="92dbd-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="92dbd-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="92dbd-198">Finanční dimenze pro **Typ pozice**, **Přiřazení pracovníka poziec** a **Zaměstnání** poskytují integraci v jediném směru do Dataverse.</span><span class="sxs-lookup"><span data-stu-id="92dbd-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="92dbd-199">Aktualizace finančních dimenzí nelze v současné době synchronizovat z Dataverse do modulu Human Resources.</span><span class="sxs-lookup"><span data-stu-id="92dbd-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="92dbd-200">Tabulky Pracovní volno a absence</span><span class="sxs-lookup"><span data-stu-id="92dbd-200">Leave and absence tables</span></span>

| <span data-ttu-id="92dbd-201">Jméno</span><span class="sxs-lookup"><span data-stu-id="92dbd-201">Name</span></span> | <span data-ttu-id="92dbd-202">Tabulka</span><span class="sxs-lookup"><span data-stu-id="92dbd-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="92dbd-203">Transakce fondu pracovního volna</span><span class="sxs-lookup"><span data-stu-id="92dbd-203">Leave Bank Transaction</span></span> | <span data-ttu-id="92dbd-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="92dbd-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="92dbd-205">Registrace pracovního volna</span><span class="sxs-lookup"><span data-stu-id="92dbd-205">Leave Enrollment</span></span> | <span data-ttu-id="92dbd-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="92dbd-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="92dbd-207">Plán pracovního volna</span><span class="sxs-lookup"><span data-stu-id="92dbd-207">Leave Plan</span></span> | <span data-ttu-id="92dbd-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="92dbd-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="92dbd-209">Žádost o pracovní volno</span><span class="sxs-lookup"><span data-stu-id="92dbd-209">Leave Request</span></span> | <span data-ttu-id="92dbd-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="92dbd-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="92dbd-211">Podrobnosti o požadavku na dovolenou</span><span class="sxs-lookup"><span data-stu-id="92dbd-211">Leave Request Detail</span></span> | <span data-ttu-id="92dbd-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="92dbd-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="92dbd-213">Typ pracovního volna</span><span class="sxs-lookup"><span data-stu-id="92dbd-213">Leave Type</span></span> | <span data-ttu-id="92dbd-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="92dbd-214">cdm_leavetype</span></span> |
| <span data-ttu-id="92dbd-215">Kód důvodu typu volna</span><span class="sxs-lookup"><span data-stu-id="92dbd-215">Leave Type Reason Code</span></span> | <span data-ttu-id="92dbd-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="92dbd-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="92dbd-217">Výplatní tabulky</span><span class="sxs-lookup"><span data-stu-id="92dbd-217">Payroll tables</span></span>

| <span data-ttu-id="92dbd-218">Jméno</span><span class="sxs-lookup"><span data-stu-id="92dbd-218">Name</span></span> | <span data-ttu-id="92dbd-219">Tabulka</span><span class="sxs-lookup"><span data-stu-id="92dbd-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="92dbd-220">Platební cyklus</span><span class="sxs-lookup"><span data-stu-id="92dbd-220">Pay Cycle</span></span> | <span data-ttu-id="92dbd-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="92dbd-221">cdm_paycycle</span></span> |
| <span data-ttu-id="92dbd-222">Platební období</span><span class="sxs-lookup"><span data-stu-id="92dbd-222">Pay Period</span></span> | <span data-ttu-id="92dbd-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="92dbd-223">cdm_payperiod</span></span> |
| <span data-ttu-id="92dbd-224">Kód příjmů mzdy</span><span class="sxs-lookup"><span data-stu-id="92dbd-224">Payroll Earning Code</span></span> | <span data-ttu-id="92dbd-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="92dbd-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="92dbd-226">Úhrady na bankovní účet</span><span class="sxs-lookup"><span data-stu-id="92dbd-226">Bank Account Disbursement</span></span> | <span data-ttu-id="92dbd-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="92dbd-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="92dbd-228">Daňová oblast</span><span class="sxs-lookup"><span data-stu-id="92dbd-228">Tax Region</span></span> | <span data-ttu-id="92dbd-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="92dbd-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="92dbd-230">Tabulky pracovníků</span><span class="sxs-lookup"><span data-stu-id="92dbd-230">Worker tables</span></span>

| <span data-ttu-id="92dbd-231">Jméno</span><span class="sxs-lookup"><span data-stu-id="92dbd-231">Name</span></span> | <span data-ttu-id="92dbd-232">Tabulka</span><span class="sxs-lookup"><span data-stu-id="92dbd-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="92dbd-233">Pracovní podproces</span><span class="sxs-lookup"><span data-stu-id="92dbd-233">Worker</span></span> | <span data-ttu-id="92dbd-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="92dbd-234">cdm_worker</span></span> |
| <span data-ttu-id="92dbd-235">Adresa pracovníka</span><span class="sxs-lookup"><span data-stu-id="92dbd-235">Worker Address</span></span> | <span data-ttu-id="92dbd-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="92dbd-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="92dbd-237">Osobní údaj pracovníka</span><span class="sxs-lookup"><span data-stu-id="92dbd-237">Worker Personal Detail</span></span> | <span data-ttu-id="92dbd-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="92dbd-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="92dbd-239">Osobní identifikační číslo pracovníka</span><span class="sxs-lookup"><span data-stu-id="92dbd-239">Worker Person Identification Number</span></span> | <span data-ttu-id="92dbd-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="92dbd-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="92dbd-241">Typ osobní identifikace pracovníka</span><span class="sxs-lookup"><span data-stu-id="92dbd-241">Worker Person Identification Type</span></span> | <span data-ttu-id="92dbd-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="92dbd-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="92dbd-243">Pracovní kalendář</span><span class="sxs-lookup"><span data-stu-id="92dbd-243">Work Calendar</span></span> | <span data-ttu-id="92dbd-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="92dbd-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="92dbd-245">Datum pracovního kalendáře</span><span class="sxs-lookup"><span data-stu-id="92dbd-245">Work Calendar Day</span></span> | <span data-ttu-id="92dbd-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="92dbd-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="92dbd-247">Svátek pracovního kalendáře</span><span class="sxs-lookup"><span data-stu-id="92dbd-247">Work Calendar Holiday</span></span> |<span data-ttu-id="92dbd-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="92dbd-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="92dbd-249">Řádek data pracovního kalendáře</span><span class="sxs-lookup"><span data-stu-id="92dbd-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="92dbd-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="92dbd-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="92dbd-251">Časový interval pracovního kalenáře</span><span class="sxs-lookup"><span data-stu-id="92dbd-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="92dbd-252">cdm_workcalendartimeinterval (není povoleno pro podporu vlastních polí)</span><span class="sxs-lookup"><span data-stu-id="92dbd-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="92dbd-253">Bankovní účet pracovníka</span><span class="sxs-lookup"><span data-stu-id="92dbd-253">Worker Bank Account</span></span> | <span data-ttu-id="92dbd-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="92dbd-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="92dbd-255">Tabulky nastavení pracovníků</span><span class="sxs-lookup"><span data-stu-id="92dbd-255">Worker setup tables</span></span>

| <span data-ttu-id="92dbd-256">Jméno</span><span class="sxs-lookup"><span data-stu-id="92dbd-256">Name</span></span> | <span data-ttu-id="92dbd-257">Tabulka</span><span class="sxs-lookup"><span data-stu-id="92dbd-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="92dbd-258">Stav veterána</span><span class="sxs-lookup"><span data-stu-id="92dbd-258">Veteran Status</span></span> | <span data-ttu-id="92dbd-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="92dbd-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="92dbd-260">Etnický původ</span><span class="sxs-lookup"><span data-stu-id="92dbd-260">Ethnic Origin</span></span> | <span data-ttu-id="92dbd-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="92dbd-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="92dbd-262">Kód důvodu</span><span class="sxs-lookup"><span data-stu-id="92dbd-262">Reason Code</span></span> | <span data-ttu-id="92dbd-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="92dbd-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="92dbd-264">Úřad vydávající identifikaci osoby</span><span class="sxs-lookup"><span data-stu-id="92dbd-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="92dbd-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="92dbd-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="92dbd-266">Tabulky kompetencí</span><span class="sxs-lookup"><span data-stu-id="92dbd-266">Competency tables</span></span>

| <span data-ttu-id="92dbd-267">Jméno</span><span class="sxs-lookup"><span data-stu-id="92dbd-267">Name</span></span> | <span data-ttu-id="92dbd-268">Tabulka</span><span class="sxs-lookup"><span data-stu-id="92dbd-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="92dbd-269">Typ dovednosti</span><span class="sxs-lookup"><span data-stu-id="92dbd-269">Skill Type</span></span> | <span data-ttu-id="92dbd-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="92dbd-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="92dbd-271">Modely vztahů tabulek</span><span class="sxs-lookup"><span data-stu-id="92dbd-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="92dbd-272">Pracovní podproces</span><span class="sxs-lookup"><span data-stu-id="92dbd-272">Worker</span></span>

![Pracovní podproces](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="92dbd-274">Práce a pracovní pozice</span><span class="sxs-lookup"><span data-stu-id="92dbd-274">Job and Job Position</span></span>

![Práce a pracovní pozice](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="92dbd-276">Zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="92dbd-276">Benefits</span></span>

![Zaměstnanecké výhody](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="92dbd-278">Kompenzace</span><span class="sxs-lookup"><span data-stu-id="92dbd-278">Compensation</span></span>

![Kompenzace](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="92dbd-280">Odejít</span><span class="sxs-lookup"><span data-stu-id="92dbd-280">Leave</span></span>

![Odejít](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="92dbd-282">Pracovní kalendář</span><span class="sxs-lookup"><span data-stu-id="92dbd-282">Work Calendar</span></span>

![Pracovní kalendář](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="92dbd-284">Viz také</span><span class="sxs-lookup"><span data-stu-id="92dbd-284">See also</span></span>

[<span data-ttu-id="92dbd-285">Volba technologie integrace dat</span><span class="sxs-lookup"><span data-stu-id="92dbd-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="92dbd-286">Konfigurace integrace s Dataverse</span><span class="sxs-lookup"><span data-stu-id="92dbd-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="92dbd-287">Konfigurace virtuálních tabulek Dataverse</span><span class="sxs-lookup"><span data-stu-id="92dbd-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="92dbd-288">Virtuální tabulky lidských zdrojů - časté dotazy</span><span class="sxs-lookup"><span data-stu-id="92dbd-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="92dbd-289">Co je Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="92dbd-289">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="92dbd-290">Aktualizace terminologie</span><span class="sxs-lookup"><span data-stu-id="92dbd-290">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)
