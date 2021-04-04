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
ms.openlocfilehash: caf8b0a5d0b24ef3619f45a6d236acae6d29c8ab
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465215"
---
# <a name="dataverse-tables"></a><span data-ttu-id="dc46c-103">Tabulky Dataverse</span><span class="sxs-lookup"><span data-stu-id="dc46c-103">Dataverse tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="dc46c-104">Microsoft Dynamics 365 Human Resources používá Dataverse k povolení scénářů rozšiřitelnosti a integrace.</span><span class="sxs-lookup"><span data-stu-id="dc46c-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="dc46c-105">Entity Human Resources odpovídají Dataverse tabulkám.</span><span class="sxs-lookup"><span data-stu-id="dc46c-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="dc46c-106">Pro více informací o Dataverse (dříve Common Data Service) a aktualizacích terminologie, viz [Co je Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="dc46c-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="dc46c-107">Následující tabulky Dataverse jsou k dispozici na základě entit lidských zdrojů.</span><span class="sxs-lookup"><span data-stu-id="dc46c-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="dc46c-108">Tabulky výhod</span><span class="sxs-lookup"><span data-stu-id="dc46c-108">Benefit tables</span></span>

| <span data-ttu-id="dc46c-109">Jméno</span><span class="sxs-lookup"><span data-stu-id="dc46c-109">Name</span></span> | <span data-ttu-id="dc46c-110">Tabulka</span><span class="sxs-lookup"><span data-stu-id="dc46c-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="dc46c-111">Frekvence výpočtu zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="dc46c-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="dc46c-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="dc46c-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="dc46c-113">Platební období – interval provádění výpočtu zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="dc46c-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="dc46c-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="dc46c-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="dc46c-115">Sazba výpočtu zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="dc46c-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="dc46c-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="dc46c-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="dc46c-117">Podrobnosti sazby výpočtu zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="dc46c-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="dc46c-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="dc46c-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="dc46c-119">Možnost zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="dc46c-119">Benefit Option</span></span> | <span data-ttu-id="dc46c-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="dc46c-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="dc46c-121">Plán zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="dc46c-121">Benefit Plan</span></span> | <span data-ttu-id="dc46c-122">cdm_benefitplan (není povoleno pro podporu vlastních polí)</span><span class="sxs-lookup"><span data-stu-id="dc46c-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="dc46c-123">Typ zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="dc46c-123">Benefit Type</span></span> | <span data-ttu-id="dc46c-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="dc46c-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="dc46c-125">Tabulky úkolů obchodního procesu</span><span class="sxs-lookup"><span data-stu-id="dc46c-125">Business process tasks tables</span></span>

| <span data-ttu-id="dc46c-126">Jméno</span><span class="sxs-lookup"><span data-stu-id="dc46c-126">Name</span></span> | <span data-ttu-id="dc46c-127">Tabulka</span><span class="sxs-lookup"><span data-stu-id="dc46c-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="dc46c-128">Kalendář obchodních procesů</span><span class="sxs-lookup"><span data-stu-id="dc46c-128">Business Process Calendar</span></span> | <span data-ttu-id="dc46c-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="dc46c-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="dc46c-130">Přiřazení skupiny obchodních procesů</span><span class="sxs-lookup"><span data-stu-id="dc46c-130">Business Process Group Assignment</span></span> | <span data-ttu-id="dc46c-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="dc46c-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="dc46c-132">Skupina úkolů knihovny obchodních procesů</span><span class="sxs-lookup"><span data-stu-id="dc46c-132">Business Process Library Task Group</span></span> | <span data-ttu-id="dc46c-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="dc46c-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="dc46c-134">Fáze obchodního procesu</span><span class="sxs-lookup"><span data-stu-id="dc46c-134">Business Process Stage</span></span> | <span data-ttu-id="dc46c-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="dc46c-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="dc46c-136">Záhlaví šablony kontrolního seznamu</span><span class="sxs-lookup"><span data-stu-id="dc46c-136">Checklist Template Header</span></span> | <span data-ttu-id="dc46c-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="dc46c-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="dc46c-138">Úkol šablony kontrolního seznamu</span><span class="sxs-lookup"><span data-stu-id="dc46c-138">Checklist Template Task</span></span> | <span data-ttu-id="dc46c-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="dc46c-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="dc46c-140">Tabulky Kompenzace</span><span class="sxs-lookup"><span data-stu-id="dc46c-140">Compensation tables</span></span>

| <span data-ttu-id="dc46c-141">Jméno</span><span class="sxs-lookup"><span data-stu-id="dc46c-141">Name</span></span> | <span data-ttu-id="dc46c-142">Tabulka</span><span class="sxs-lookup"><span data-stu-id="dc46c-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="dc46c-143">Fixní plán kompenzace</span><span class="sxs-lookup"><span data-stu-id="dc46c-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="dc46c-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="dc46c-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="dc46c-145">Mřížka kompenzace</span><span class="sxs-lookup"><span data-stu-id="dc46c-145">Compensation Grid</span></span> | <span data-ttu-id="dc46c-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="dc46c-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="dc46c-147">Úroveň kompenzace</span><span class="sxs-lookup"><span data-stu-id="dc46c-147">Compensation Level</span></span> | <span data-ttu-id="dc46c-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="dc46c-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="dc46c-149">Interval plateb kompenzace</span><span class="sxs-lookup"><span data-stu-id="dc46c-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="dc46c-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="dc46c-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="dc46c-151">Nastavení referenčního bodu kompenzace</span><span class="sxs-lookup"><span data-stu-id="dc46c-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="dc46c-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="dc46c-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="dc46c-153">Linie nastavení referenčního bodu kompenzace</span><span class="sxs-lookup"><span data-stu-id="dc46c-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="dc46c-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="dc46c-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="dc46c-155">Oblast kompenzace</span><span class="sxs-lookup"><span data-stu-id="dc46c-155">Compensation Region</span></span> | <span data-ttu-id="dc46c-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="dc46c-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="dc46c-157">Struktura kompenzací</span><span class="sxs-lookup"><span data-stu-id="dc46c-157">Compensation Structure</span></span> | <span data-ttu-id="dc46c-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="dc46c-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="dc46c-159">Plán variabilní kompenzace</span><span class="sxs-lookup"><span data-stu-id="dc46c-159">Compensation Variable Plan</span></span> | <span data-ttu-id="dc46c-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="dc46c-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="dc46c-161">Úroveň plánu variabilní kompenzace</span><span class="sxs-lookup"><span data-stu-id="dc46c-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="dc46c-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="dc46c-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="dc46c-163">Typ plánu variabilní kompenzace</span><span class="sxs-lookup"><span data-stu-id="dc46c-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="dc46c-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="dc46c-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="dc46c-165">Událost fixní kompenzace</span><span class="sxs-lookup"><span data-stu-id="dc46c-165">Fixed Compensation Event</span></span> | <span data-ttu-id="dc46c-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="dc46c-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="dc46c-167">Pravidlo připsání</span><span class="sxs-lookup"><span data-stu-id="dc46c-167">Vesting Rule</span></span> | <span data-ttu-id="dc46c-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="dc46c-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="dc46c-169">Fixní kompenzace pracovníka</span><span class="sxs-lookup"><span data-stu-id="dc46c-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="dc46c-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="dc46c-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="dc46c-171">Organizační tabulky</span><span class="sxs-lookup"><span data-stu-id="dc46c-171">Organization tables</span></span>

| <span data-ttu-id="dc46c-172">Jméno</span><span class="sxs-lookup"><span data-stu-id="dc46c-172">Name</span></span> | <span data-ttu-id="dc46c-173">Tabulka</span><span class="sxs-lookup"><span data-stu-id="dc46c-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="dc46c-174">Oddělení</span><span class="sxs-lookup"><span data-stu-id="dc46c-174">Department</span></span> | <span data-ttu-id="dc46c-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="dc46c-175">cdm_department</span></span> |
| <span data-ttu-id="dc46c-176">Zaměstnání</span><span class="sxs-lookup"><span data-stu-id="dc46c-176">Employment</span></span> | <span data-ttu-id="dc46c-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="dc46c-177">cdm_employment</span></span> |
| <span data-ttu-id="dc46c-178">Společnost</span><span class="sxs-lookup"><span data-stu-id="dc46c-178">Company</span></span> | <span data-ttu-id="dc46c-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="dc46c-179">cdm_company</span></span> |
| <span data-ttu-id="dc46c-180">Pozice</span><span class="sxs-lookup"><span data-stu-id="dc46c-180">Job</span></span> | <span data-ttu-id="dc46c-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="dc46c-181">cdm_job</span></span> |
| <span data-ttu-id="dc46c-182">Pracovní funkce</span><span class="sxs-lookup"><span data-stu-id="dc46c-182">Job Function</span></span> | <span data-ttu-id="dc46c-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="dc46c-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="dc46c-184">Pracovní pozice</span><span class="sxs-lookup"><span data-stu-id="dc46c-184">Job Position</span></span> | <span data-ttu-id="dc46c-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="dc46c-185">cdm_jobposition</span></span> |
| <span data-ttu-id="dc46c-186">Typ pozice</span><span class="sxs-lookup"><span data-stu-id="dc46c-186">Position Type</span></span> | <span data-ttu-id="dc46c-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="dc46c-187">cdm_positiontype</span></span> |
| <span data-ttu-id="dc46c-188">Přiřazení pracovníka k pozici</span><span class="sxs-lookup"><span data-stu-id="dc46c-188">Position Worker Assignment</span></span> | <span data-ttu-id="dc46c-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="dc46c-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="dc46c-190">Dimenze pracovních pozic</span><span class="sxs-lookup"><span data-stu-id="dc46c-190">Job Position Dimension</span></span> | <span data-ttu-id="dc46c-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="dc46c-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="dc46c-192">Typ práce</span><span class="sxs-lookup"><span data-stu-id="dc46c-192">Job Type</span></span> | <span data-ttu-id="dc46c-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="dc46c-193">cdm_jobtype</span></span> |
| <span data-ttu-id="dc46c-194">Jazyk</span><span class="sxs-lookup"><span data-stu-id="dc46c-194">Language</span></span> | <span data-ttu-id="dc46c-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="dc46c-195">cdm_language</span></span> |
| <span data-ttu-id="dc46c-196">Pozice</span><span class="sxs-lookup"><span data-stu-id="dc46c-196">Title</span></span> | <span data-ttu-id="dc46c-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="dc46c-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="dc46c-198">Finanční dimenze pro **Typ pozice**, **Přiřazení pracovníka poziec** a **Zaměstnání** poskytují integraci v jediném směru do Dataverse.</span><span class="sxs-lookup"><span data-stu-id="dc46c-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="dc46c-199">Aktualizace finančních dimenzí nelze v současné době synchronizovat z Dataverse do modulu Human Resources.</span><span class="sxs-lookup"><span data-stu-id="dc46c-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="dc46c-200">Tabulky Pracovní volno a absence</span><span class="sxs-lookup"><span data-stu-id="dc46c-200">Leave and absence tables</span></span>

| <span data-ttu-id="dc46c-201">Jméno</span><span class="sxs-lookup"><span data-stu-id="dc46c-201">Name</span></span> | <span data-ttu-id="dc46c-202">Tabulka</span><span class="sxs-lookup"><span data-stu-id="dc46c-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="dc46c-203">Transakce fondu pracovního volna</span><span class="sxs-lookup"><span data-stu-id="dc46c-203">Leave Bank Transaction</span></span> | <span data-ttu-id="dc46c-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="dc46c-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="dc46c-205">Registrace pracovního volna</span><span class="sxs-lookup"><span data-stu-id="dc46c-205">Leave Enrollment</span></span> | <span data-ttu-id="dc46c-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="dc46c-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="dc46c-207">Plán pracovního volna</span><span class="sxs-lookup"><span data-stu-id="dc46c-207">Leave Plan</span></span> | <span data-ttu-id="dc46c-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="dc46c-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="dc46c-209">Žádost o pracovní volno</span><span class="sxs-lookup"><span data-stu-id="dc46c-209">Leave Request</span></span> | <span data-ttu-id="dc46c-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="dc46c-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="dc46c-211">Podrobnosti o požadavku na dovolenou</span><span class="sxs-lookup"><span data-stu-id="dc46c-211">Leave Request Detail</span></span> | <span data-ttu-id="dc46c-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="dc46c-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="dc46c-213">Typ pracovního volna</span><span class="sxs-lookup"><span data-stu-id="dc46c-213">Leave Type</span></span> | <span data-ttu-id="dc46c-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="dc46c-214">cdm_leavetype</span></span> |
| <span data-ttu-id="dc46c-215">Kód důvodu typu volna</span><span class="sxs-lookup"><span data-stu-id="dc46c-215">Leave Type Reason Code</span></span> | <span data-ttu-id="dc46c-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="dc46c-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="dc46c-217">Výplatní tabulky</span><span class="sxs-lookup"><span data-stu-id="dc46c-217">Payroll tables</span></span>

| <span data-ttu-id="dc46c-218">Jméno</span><span class="sxs-lookup"><span data-stu-id="dc46c-218">Name</span></span> | <span data-ttu-id="dc46c-219">Tabulka</span><span class="sxs-lookup"><span data-stu-id="dc46c-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="dc46c-220">Platební cyklus</span><span class="sxs-lookup"><span data-stu-id="dc46c-220">Pay Cycle</span></span> | <span data-ttu-id="dc46c-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="dc46c-221">cdm_paycycle</span></span> |
| <span data-ttu-id="dc46c-222">Platební období</span><span class="sxs-lookup"><span data-stu-id="dc46c-222">Pay Period</span></span> | <span data-ttu-id="dc46c-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="dc46c-223">cdm_payperiod</span></span> |
| <span data-ttu-id="dc46c-224">Kód příjmů mzdy</span><span class="sxs-lookup"><span data-stu-id="dc46c-224">Payroll Earning Code</span></span> | <span data-ttu-id="dc46c-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="dc46c-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="dc46c-226">Úhrady na bankovní účet</span><span class="sxs-lookup"><span data-stu-id="dc46c-226">Bank Account Disbursement</span></span> | <span data-ttu-id="dc46c-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="dc46c-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="dc46c-228">Daňová oblast</span><span class="sxs-lookup"><span data-stu-id="dc46c-228">Tax Region</span></span> | <span data-ttu-id="dc46c-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="dc46c-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="dc46c-230">Tabulky pracovníků</span><span class="sxs-lookup"><span data-stu-id="dc46c-230">Worker tables</span></span>

| <span data-ttu-id="dc46c-231">Jméno</span><span class="sxs-lookup"><span data-stu-id="dc46c-231">Name</span></span> | <span data-ttu-id="dc46c-232">Tabulka</span><span class="sxs-lookup"><span data-stu-id="dc46c-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="dc46c-233">Pracovní podproces</span><span class="sxs-lookup"><span data-stu-id="dc46c-233">Worker</span></span> | <span data-ttu-id="dc46c-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="dc46c-234">cdm_worker</span></span> |
| <span data-ttu-id="dc46c-235">Adresa pracovníka</span><span class="sxs-lookup"><span data-stu-id="dc46c-235">Worker Address</span></span> | <span data-ttu-id="dc46c-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="dc46c-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="dc46c-237">Osobní údaj pracovníka</span><span class="sxs-lookup"><span data-stu-id="dc46c-237">Worker Personal Detail</span></span> | <span data-ttu-id="dc46c-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="dc46c-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="dc46c-239">Osobní identifikační číslo pracovníka</span><span class="sxs-lookup"><span data-stu-id="dc46c-239">Worker Person Identification Number</span></span> | <span data-ttu-id="dc46c-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="dc46c-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="dc46c-241">Typ osobní identifikace pracovníka</span><span class="sxs-lookup"><span data-stu-id="dc46c-241">Worker Person Identification Type</span></span> | <span data-ttu-id="dc46c-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="dc46c-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="dc46c-243">Pracovní kalendář</span><span class="sxs-lookup"><span data-stu-id="dc46c-243">Work Calendar</span></span> | <span data-ttu-id="dc46c-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="dc46c-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="dc46c-245">Datum pracovního kalendáře</span><span class="sxs-lookup"><span data-stu-id="dc46c-245">Work Calendar Day</span></span> | <span data-ttu-id="dc46c-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="dc46c-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="dc46c-247">Svátek pracovního kalendáře</span><span class="sxs-lookup"><span data-stu-id="dc46c-247">Work Calendar Holiday</span></span> |<span data-ttu-id="dc46c-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="dc46c-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="dc46c-249">Řádek data pracovního kalendáře</span><span class="sxs-lookup"><span data-stu-id="dc46c-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="dc46c-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="dc46c-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="dc46c-251">Časový interval pracovního kalenáře</span><span class="sxs-lookup"><span data-stu-id="dc46c-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="dc46c-252">cdm_workcalendartimeinterval (není povoleno pro podporu vlastních polí)</span><span class="sxs-lookup"><span data-stu-id="dc46c-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="dc46c-253">Bankovní účet pracovníka</span><span class="sxs-lookup"><span data-stu-id="dc46c-253">Worker Bank Account</span></span> | <span data-ttu-id="dc46c-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="dc46c-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="dc46c-255">Tabulky nastavení pracovníků</span><span class="sxs-lookup"><span data-stu-id="dc46c-255">Worker setup tables</span></span>

| <span data-ttu-id="dc46c-256">Jméno</span><span class="sxs-lookup"><span data-stu-id="dc46c-256">Name</span></span> | <span data-ttu-id="dc46c-257">Tabulka</span><span class="sxs-lookup"><span data-stu-id="dc46c-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="dc46c-258">Stav veterána</span><span class="sxs-lookup"><span data-stu-id="dc46c-258">Veteran Status</span></span> | <span data-ttu-id="dc46c-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="dc46c-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="dc46c-260">Etnický původ</span><span class="sxs-lookup"><span data-stu-id="dc46c-260">Ethnic Origin</span></span> | <span data-ttu-id="dc46c-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="dc46c-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="dc46c-262">Kód důvodu</span><span class="sxs-lookup"><span data-stu-id="dc46c-262">Reason Code</span></span> | <span data-ttu-id="dc46c-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="dc46c-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="dc46c-264">Úřad vydávající identifikaci osoby</span><span class="sxs-lookup"><span data-stu-id="dc46c-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="dc46c-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="dc46c-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="dc46c-266">Tabulky kompetencí</span><span class="sxs-lookup"><span data-stu-id="dc46c-266">Competency tables</span></span>

| <span data-ttu-id="dc46c-267">Jméno</span><span class="sxs-lookup"><span data-stu-id="dc46c-267">Name</span></span> | <span data-ttu-id="dc46c-268">Tabulka</span><span class="sxs-lookup"><span data-stu-id="dc46c-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="dc46c-269">Typ dovednosti</span><span class="sxs-lookup"><span data-stu-id="dc46c-269">Skill Type</span></span> | <span data-ttu-id="dc46c-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="dc46c-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="dc46c-271">Modely vztahů tabulek</span><span class="sxs-lookup"><span data-stu-id="dc46c-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="dc46c-272">Pracovní podproces</span><span class="sxs-lookup"><span data-stu-id="dc46c-272">Worker</span></span>

![Pracovní podproces](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="dc46c-274">Práce a pracovní pozice</span><span class="sxs-lookup"><span data-stu-id="dc46c-274">Job and Job Position</span></span>

![Práce a pracovní pozice](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="dc46c-276">Zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="dc46c-276">Benefits</span></span>

![Zaměstnanecké výhody](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="dc46c-278">Kompenzace</span><span class="sxs-lookup"><span data-stu-id="dc46c-278">Compensation</span></span>

![Kompenzace](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="dc46c-280">Odejít</span><span class="sxs-lookup"><span data-stu-id="dc46c-280">Leave</span></span>

![Odejít](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="dc46c-282">Pracovní kalendář</span><span class="sxs-lookup"><span data-stu-id="dc46c-282">Work Calendar</span></span>

![Pracovní kalendář](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="dc46c-284">Viz také</span><span class="sxs-lookup"><span data-stu-id="dc46c-284">See also</span></span>

[<span data-ttu-id="dc46c-285">Volba technologie integrace dat</span><span class="sxs-lookup"><span data-stu-id="dc46c-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="dc46c-286">Konfigurace integrace s Dataverse</span><span class="sxs-lookup"><span data-stu-id="dc46c-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="dc46c-287">Konfigurace virtuálních tabulek Dataverse</span><span class="sxs-lookup"><span data-stu-id="dc46c-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="dc46c-288">Virtuální tabulky lidských zdrojů - časté dotazy</span><span class="sxs-lookup"><span data-stu-id="dc46c-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="dc46c-289">Co je Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="dc46c-289">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="dc46c-290">Aktualizace terminologie</span><span class="sxs-lookup"><span data-stu-id="dc46c-290">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]