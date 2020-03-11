---
title: Entity Common Data Service
description: Microsoft Dynamics 365 Human Resources používá Common Data Service k povolení scénářů rozšiřitelnosti a integrace.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 6879a45dd1fcc1ba718747aaaf0d7936c2eac49f
ms.sourcegitcommit: 3cad15f8ecc257d3a45c1bc1fada7c094ff4bcec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087339"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="abdfa-103">Entity Common Data Service</span><span class="sxs-lookup"><span data-stu-id="abdfa-103">Common Data Service entities</span></span>

<span data-ttu-id="abdfa-104">Microsoft Dynamics 365 Human Resources používá Common Data Service k povolení scénářů rozšiřitelnosti a integrace.</span><span class="sxs-lookup"><span data-stu-id="abdfa-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="abdfa-105">Další informace týkající se Common Data Service získáte v tématu [Co je Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span><span class="sxs-lookup"><span data-stu-id="abdfa-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="abdfa-106">V Common Data Service jsou k dispozici následující entity lidských zdrojů.</span><span class="sxs-lookup"><span data-stu-id="abdfa-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="abdfa-107">Entity zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="abdfa-107">Benefit entities</span></span>

| <span data-ttu-id="abdfa-108">Název</span><span class="sxs-lookup"><span data-stu-id="abdfa-108">Name</span></span> | <span data-ttu-id="abdfa-109">Celek</span><span class="sxs-lookup"><span data-stu-id="abdfa-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="abdfa-110">Interval provádění výpočtu zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="abdfa-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="abdfa-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="abdfa-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="abdfa-112">Platební období – interval provádění výpočtu zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="abdfa-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="abdfa-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="abdfa-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="abdfa-114">Sazba výpočtu zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="abdfa-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="abdfa-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="abdfa-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="abdfa-116">Podrobnosti sazby výpočtu zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="abdfa-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="abdfa-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="abdfa-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="abdfa-118">Možnost zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="abdfa-118">Benefit Option</span></span> | <span data-ttu-id="abdfa-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="abdfa-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="abdfa-120">Plán zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="abdfa-120">Benefit Plan</span></span> | <span data-ttu-id="abdfa-121">cdm_benefitplan (není povoleno pro podporu vlastních polí)</span><span class="sxs-lookup"><span data-stu-id="abdfa-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="abdfa-122">Typ zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="abdfa-122">Benefit Type</span></span> | <span data-ttu-id="abdfa-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="abdfa-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="abdfa-124">Entity úkolů obchodního procesu</span><span class="sxs-lookup"><span data-stu-id="abdfa-124">Business process tasks entities</span></span>

| <span data-ttu-id="abdfa-125">Název</span><span class="sxs-lookup"><span data-stu-id="abdfa-125">Name</span></span> | <span data-ttu-id="abdfa-126">Celek</span><span class="sxs-lookup"><span data-stu-id="abdfa-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="abdfa-127">Kalendář obchodních procesů</span><span class="sxs-lookup"><span data-stu-id="abdfa-127">Business Process Calendar</span></span> | <span data-ttu-id="abdfa-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="abdfa-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="abdfa-129">Přiřazení skupiny obchodních procesů</span><span class="sxs-lookup"><span data-stu-id="abdfa-129">Business Process Group Assignment</span></span> | <span data-ttu-id="abdfa-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="abdfa-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="abdfa-131">Skupina úkolů knihovny obchodních procesů</span><span class="sxs-lookup"><span data-stu-id="abdfa-131">Business Process Library Task Group</span></span> | <span data-ttu-id="abdfa-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="abdfa-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="abdfa-133">Fáze obchodního procesu</span><span class="sxs-lookup"><span data-stu-id="abdfa-133">Business Process Stage</span></span> | <span data-ttu-id="abdfa-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="abdfa-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="abdfa-135">Záhlaví šablony kontrolního seznamu</span><span class="sxs-lookup"><span data-stu-id="abdfa-135">Checklist Template Header</span></span> | <span data-ttu-id="abdfa-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="abdfa-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="abdfa-137">Úkol šablony kontrolního seznamu</span><span class="sxs-lookup"><span data-stu-id="abdfa-137">Checklist Template Task</span></span> | <span data-ttu-id="abdfa-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="abdfa-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="abdfa-139">Entity kompenzace</span><span class="sxs-lookup"><span data-stu-id="abdfa-139">Compensation entities</span></span>

| <span data-ttu-id="abdfa-140">Název</span><span class="sxs-lookup"><span data-stu-id="abdfa-140">Name</span></span> | <span data-ttu-id="abdfa-141">Celek</span><span class="sxs-lookup"><span data-stu-id="abdfa-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="abdfa-142">Fixní plán kompenzace</span><span class="sxs-lookup"><span data-stu-id="abdfa-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="abdfa-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="abdfa-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="abdfa-144">Mřížka kompenzace</span><span class="sxs-lookup"><span data-stu-id="abdfa-144">Compensation Grid</span></span> | <span data-ttu-id="abdfa-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="abdfa-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="abdfa-146">Úroveň kompenzace</span><span class="sxs-lookup"><span data-stu-id="abdfa-146">Compensation Level</span></span> | <span data-ttu-id="abdfa-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="abdfa-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="abdfa-148">Interval plateb kompenzace</span><span class="sxs-lookup"><span data-stu-id="abdfa-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="abdfa-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="abdfa-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="abdfa-150">Nastavení referenčního bodu kompenzace</span><span class="sxs-lookup"><span data-stu-id="abdfa-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="abdfa-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="abdfa-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="abdfa-152">Linie nastavení referenčního bodu kompenzace</span><span class="sxs-lookup"><span data-stu-id="abdfa-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="abdfa-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="abdfa-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="abdfa-154">Oblast kompenzace</span><span class="sxs-lookup"><span data-stu-id="abdfa-154">Compensation Region</span></span> | <span data-ttu-id="abdfa-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="abdfa-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="abdfa-156">Struktura kompenzací</span><span class="sxs-lookup"><span data-stu-id="abdfa-156">Compensation Structure</span></span> | <span data-ttu-id="abdfa-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="abdfa-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="abdfa-158">Plán variabilní kompenzace</span><span class="sxs-lookup"><span data-stu-id="abdfa-158">Compensation Variable Plan</span></span> | <span data-ttu-id="abdfa-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="abdfa-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="abdfa-160">Úroveň plánu variabilní kompenzace</span><span class="sxs-lookup"><span data-stu-id="abdfa-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="abdfa-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="abdfa-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="abdfa-162">Typ plánu variabilní kompenzace</span><span class="sxs-lookup"><span data-stu-id="abdfa-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="abdfa-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="abdfa-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="abdfa-164">Událost fixní kompenzace</span><span class="sxs-lookup"><span data-stu-id="abdfa-164">Fixed Compensation Event</span></span> | <span data-ttu-id="abdfa-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="abdfa-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="abdfa-166">Pravidlo připsání</span><span class="sxs-lookup"><span data-stu-id="abdfa-166">Vesting Rule</span></span> | <span data-ttu-id="abdfa-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="abdfa-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="abdfa-168">Fixní kompenzace pracovníka</span><span class="sxs-lookup"><span data-stu-id="abdfa-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="abdfa-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="abdfa-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="abdfa-170">Entity organizace</span><span class="sxs-lookup"><span data-stu-id="abdfa-170">Organization entities</span></span>

| <span data-ttu-id="abdfa-171">Název</span><span class="sxs-lookup"><span data-stu-id="abdfa-171">Name</span></span> | <span data-ttu-id="abdfa-172">Celek</span><span class="sxs-lookup"><span data-stu-id="abdfa-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="abdfa-173">Oddělení</span><span class="sxs-lookup"><span data-stu-id="abdfa-173">Department</span></span> | <span data-ttu-id="abdfa-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="abdfa-174">cdm_department</span></span> |
| <span data-ttu-id="abdfa-175">Zaměstnání</span><span class="sxs-lookup"><span data-stu-id="abdfa-175">Employment</span></span> | <span data-ttu-id="abdfa-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="abdfa-176">cdm_employment</span></span> |
| <span data-ttu-id="abdfa-177">Společnost</span><span class="sxs-lookup"><span data-stu-id="abdfa-177">Company</span></span> | <span data-ttu-id="abdfa-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="abdfa-178">cdm_company</span></span> |
| <span data-ttu-id="abdfa-179">Pozice</span><span class="sxs-lookup"><span data-stu-id="abdfa-179">Job</span></span> | <span data-ttu-id="abdfa-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="abdfa-180">cdm_job</span></span> |
| <span data-ttu-id="abdfa-181">Pracovní funkce</span><span class="sxs-lookup"><span data-stu-id="abdfa-181">Job Function</span></span> | <span data-ttu-id="abdfa-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="abdfa-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="abdfa-183">Pracovní pozice</span><span class="sxs-lookup"><span data-stu-id="abdfa-183">Job Position</span></span> | <span data-ttu-id="abdfa-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="abdfa-184">cdm_jobposition</span></span> |
| <span data-ttu-id="abdfa-185">Typ pozice</span><span class="sxs-lookup"><span data-stu-id="abdfa-185">Position Type</span></span> | <span data-ttu-id="abdfa-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="abdfa-186">cdm_positiontype</span></span> |
| <span data-ttu-id="abdfa-187">Přiřazení pracovníka k pozici</span><span class="sxs-lookup"><span data-stu-id="abdfa-187">Position Worker Assignment</span></span> | <span data-ttu-id="abdfa-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="abdfa-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="abdfa-189">Typ práce</span><span class="sxs-lookup"><span data-stu-id="abdfa-189">Job Type</span></span> | <span data-ttu-id="abdfa-190">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="abdfa-190">cdm_jobtype</span></span> |
| <span data-ttu-id="abdfa-191">Jazyk</span><span class="sxs-lookup"><span data-stu-id="abdfa-191">Language</span></span> | <span data-ttu-id="abdfa-192">cdm_language</span><span class="sxs-lookup"><span data-stu-id="abdfa-192">cdm_language</span></span> |

## <a name="leave-and-absence-entities"></a><span data-ttu-id="abdfa-193">Entity pracovního volna a absence</span><span class="sxs-lookup"><span data-stu-id="abdfa-193">Leave and absence entities</span></span>

| <span data-ttu-id="abdfa-194">Název</span><span class="sxs-lookup"><span data-stu-id="abdfa-194">Name</span></span> | <span data-ttu-id="abdfa-195">Celek</span><span class="sxs-lookup"><span data-stu-id="abdfa-195">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="abdfa-196">Opustit bankovní transakci</span><span class="sxs-lookup"><span data-stu-id="abdfa-196">Leave Bank Transaction</span></span> | <span data-ttu-id="abdfa-197">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="abdfa-197">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="abdfa-198">Opustit zápis</span><span class="sxs-lookup"><span data-stu-id="abdfa-198">Leave Enrollment</span></span> | <span data-ttu-id="abdfa-199">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="abdfa-199">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="abdfa-200">Plán pracovního volna</span><span class="sxs-lookup"><span data-stu-id="abdfa-200">Leave Plan</span></span> | <span data-ttu-id="abdfa-201">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="abdfa-201">cdm_leaveplan</span></span> |
| <span data-ttu-id="abdfa-202">Žádost o pracovní volno</span><span class="sxs-lookup"><span data-stu-id="abdfa-202">Leave Request</span></span> | <span data-ttu-id="abdfa-203">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="abdfa-203">cdm_leaverequest</span></span> |
| <span data-ttu-id="abdfa-204">Podrobnosti o požadavku na dovolenou</span><span class="sxs-lookup"><span data-stu-id="abdfa-204">Leave Request Detail</span></span> | <span data-ttu-id="abdfa-205">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="abdfa-205">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="abdfa-206">Typ pracovního volna</span><span class="sxs-lookup"><span data-stu-id="abdfa-206">Leave Type</span></span> | <span data-ttu-id="abdfa-207">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="abdfa-207">cdm_leavetype</span></span> |
| <span data-ttu-id="abdfa-208">Kód důvodu typu volna</span><span class="sxs-lookup"><span data-stu-id="abdfa-208">Leave Type Reason Code</span></span> | <span data-ttu-id="abdfa-209">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="abdfa-209">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="abdfa-210">Entita mzdy</span><span class="sxs-lookup"><span data-stu-id="abdfa-210">Payroll entities</span></span>

| <span data-ttu-id="abdfa-211">Název</span><span class="sxs-lookup"><span data-stu-id="abdfa-211">Name</span></span> | <span data-ttu-id="abdfa-212">Celek</span><span class="sxs-lookup"><span data-stu-id="abdfa-212">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="abdfa-213">Platební cyklus</span><span class="sxs-lookup"><span data-stu-id="abdfa-213">Pay Cycle</span></span> | <span data-ttu-id="abdfa-214">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="abdfa-214">cdm_paycycle</span></span> |
| <span data-ttu-id="abdfa-215">Mzdové období</span><span class="sxs-lookup"><span data-stu-id="abdfa-215">Pay Period</span></span> | <span data-ttu-id="abdfa-216">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="abdfa-216">cdm_payperiod</span></span> |
| <span data-ttu-id="abdfa-217">Kód příjmů mzdy</span><span class="sxs-lookup"><span data-stu-id="abdfa-217">Payroll Earning Code</span></span> | <span data-ttu-id="abdfa-218">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="abdfa-218">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="abdfa-219">Úhrady na bankovní účet</span><span class="sxs-lookup"><span data-stu-id="abdfa-219">Bank Account Disbursement</span></span> | <span data-ttu-id="abdfa-220">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="abdfa-220">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="abdfa-221">Daňová oblast</span><span class="sxs-lookup"><span data-stu-id="abdfa-221">Tax Region</span></span> | <span data-ttu-id="abdfa-222">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="abdfa-222">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="abdfa-223">Entity pracovníků</span><span class="sxs-lookup"><span data-stu-id="abdfa-223">Worker entities</span></span>

| <span data-ttu-id="abdfa-224">Název</span><span class="sxs-lookup"><span data-stu-id="abdfa-224">Name</span></span> | <span data-ttu-id="abdfa-225">Celek</span><span class="sxs-lookup"><span data-stu-id="abdfa-225">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="abdfa-226">Pracovní podproces</span><span class="sxs-lookup"><span data-stu-id="abdfa-226">Worker</span></span> | <span data-ttu-id="abdfa-227">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="abdfa-227">cdm_worker</span></span> |
| <span data-ttu-id="abdfa-228">Adresa pracovníka</span><span class="sxs-lookup"><span data-stu-id="abdfa-228">Worker Address</span></span> | <span data-ttu-id="abdfa-229">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="abdfa-229">cdm_workeraddress</span></span> |
| <span data-ttu-id="abdfa-230">Osobní údaj pracovníka</span><span class="sxs-lookup"><span data-stu-id="abdfa-230">Worker Personal Detail</span></span> | <span data-ttu-id="abdfa-231">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="abdfa-231">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="abdfa-232">Osobní identifikační číslo pracovníka</span><span class="sxs-lookup"><span data-stu-id="abdfa-232">Worker Person Identification Number</span></span> | <span data-ttu-id="abdfa-233">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="abdfa-233">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="abdfa-234">Typ osobní identifikace pracovníka</span><span class="sxs-lookup"><span data-stu-id="abdfa-234">Worker Person Identification Type</span></span> | <span data-ttu-id="abdfa-235">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="abdfa-235">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="abdfa-236">Pracovní kalendář</span><span class="sxs-lookup"><span data-stu-id="abdfa-236">Work Calendar</span></span> | <span data-ttu-id="abdfa-237">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="abdfa-237">cdm_workcalendar</span></span> |
| <span data-ttu-id="abdfa-238">Datum pracovního kalendáře</span><span class="sxs-lookup"><span data-stu-id="abdfa-238">Work Calendar Day</span></span> | <span data-ttu-id="abdfa-239">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="abdfa-239">cdm_workcalendarday</span></span> |
| <span data-ttu-id="abdfa-240">Svátek pracovního kalendáře</span><span class="sxs-lookup"><span data-stu-id="abdfa-240">Work Calendar Holiday</span></span> |<span data-ttu-id="abdfa-241">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="abdfa-241">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="abdfa-242">Řádek data pracovního kalendáře</span><span class="sxs-lookup"><span data-stu-id="abdfa-242">Work Calendar Holiday Line</span></span> | <span data-ttu-id="abdfa-243">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="abdfa-243">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="abdfa-244">Časový interval pracovního kalenáře</span><span class="sxs-lookup"><span data-stu-id="abdfa-244">Work Calendar Time Interval</span></span> | <span data-ttu-id="abdfa-245">cdm_workcalendartimeinterval (není povoleno pro podporu vlastních polí)</span><span class="sxs-lookup"><span data-stu-id="abdfa-245">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="abdfa-246">Bankovní účet pracovníka</span><span class="sxs-lookup"><span data-stu-id="abdfa-246">Worker Bank Account</span></span> | <span data-ttu-id="abdfa-247">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="abdfa-247">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="abdfa-248">Entity nastavení pracovníků</span><span class="sxs-lookup"><span data-stu-id="abdfa-248">Worker setup entities</span></span>

| <span data-ttu-id="abdfa-249">Název</span><span class="sxs-lookup"><span data-stu-id="abdfa-249">Name</span></span> | <span data-ttu-id="abdfa-250">Celek</span><span class="sxs-lookup"><span data-stu-id="abdfa-250">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="abdfa-251">Stav veterána</span><span class="sxs-lookup"><span data-stu-id="abdfa-251">Veteran Status</span></span> | <span data-ttu-id="abdfa-252">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="abdfa-252">cdm_veteranstatus</span></span> |
| <span data-ttu-id="abdfa-253">Etnický původ</span><span class="sxs-lookup"><span data-stu-id="abdfa-253">Ethnic Origin</span></span> | <span data-ttu-id="abdfa-254">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="abdfa-254">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="abdfa-255">Kód důvodu</span><span class="sxs-lookup"><span data-stu-id="abdfa-255">Reason Code</span></span> | <span data-ttu-id="abdfa-256">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="abdfa-256">cdm_reasoncode</span></span> |
| <span data-ttu-id="abdfa-257">Subjekt vydávající identifikaci osob</span><span class="sxs-lookup"><span data-stu-id="abdfa-257">Person Identification Issuing Agency</span></span> | <span data-ttu-id="abdfa-258">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="abdfa-258">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="abdfa-259">Entity kompetence</span><span class="sxs-lookup"><span data-stu-id="abdfa-259">Competency entities</span></span>

| <span data-ttu-id="abdfa-260">Název</span><span class="sxs-lookup"><span data-stu-id="abdfa-260">Name</span></span> | <span data-ttu-id="abdfa-261">Celek</span><span class="sxs-lookup"><span data-stu-id="abdfa-261">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="abdfa-262">Typ dovednosti</span><span class="sxs-lookup"><span data-stu-id="abdfa-262">Skill Type</span></span> | <span data-ttu-id="abdfa-263">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="abdfa-263">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="abdfa-264">Modely vztahu entity</span><span class="sxs-lookup"><span data-stu-id="abdfa-264">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="abdfa-265">Pracovní podproces</span><span class="sxs-lookup"><span data-stu-id="abdfa-265">Worker</span></span>

![Pracovní podproces](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="abdfa-267">Práce a pracovní pozice</span><span class="sxs-lookup"><span data-stu-id="abdfa-267">Job and Job Position</span></span>

![Práce a pracovní pozice](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="abdfa-269">Zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="abdfa-269">Benefits</span></span>

![Zaměstnanecké výhody](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="abdfa-271">Kompenzace</span><span class="sxs-lookup"><span data-stu-id="abdfa-271">Compensation</span></span>

![Kompenzace](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="abdfa-273">Odejít</span><span class="sxs-lookup"><span data-stu-id="abdfa-273">Leave</span></span>

![Odejít](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="abdfa-275">Pracovní kalendář</span><span class="sxs-lookup"><span data-stu-id="abdfa-275">Work Calendar</span></span>

![Pracovní kalendář](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="abdfa-277">Viz také</span><span class="sxs-lookup"><span data-stu-id="abdfa-277">See also</span></span>

[<span data-ttu-id="abdfa-278">Volba technologie integrace dat</span><span class="sxs-lookup"><span data-stu-id="abdfa-278">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="abdfa-279">Konfigurace integrace s Common Data Service</span><span class="sxs-lookup"><span data-stu-id="abdfa-279">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)