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
ms.openlocfilehash: 988fa0b6d39a49b973626a8a0abe83c546f42297
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529999"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="1eea1-103">Entity Common Data Service</span><span class="sxs-lookup"><span data-stu-id="1eea1-103">Common Data Service entities</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="1eea1-104">Microsoft Dynamics 365 Human Resources používá Common Data Service k povolení scénářů rozšiřitelnosti a integrace.</span><span class="sxs-lookup"><span data-stu-id="1eea1-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="1eea1-105">Další informace týkající se Common Data Service získáte v tématu [Co je Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span><span class="sxs-lookup"><span data-stu-id="1eea1-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="1eea1-106">V Common Data Service jsou k dispozici následující entity lidských zdrojů.</span><span class="sxs-lookup"><span data-stu-id="1eea1-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="1eea1-107">Entity zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="1eea1-107">Benefit entities</span></span>

| <span data-ttu-id="1eea1-108">Název</span><span class="sxs-lookup"><span data-stu-id="1eea1-108">Name</span></span> | <span data-ttu-id="1eea1-109">Celek</span><span class="sxs-lookup"><span data-stu-id="1eea1-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1eea1-110">Interval provádění výpočtu zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="1eea1-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="1eea1-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="1eea1-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="1eea1-112">Platební období – interval provádění výpočtu zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="1eea1-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="1eea1-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="1eea1-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="1eea1-114">Sazba výpočtu zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="1eea1-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="1eea1-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="1eea1-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="1eea1-116">Podrobnosti sazby výpočtu zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="1eea1-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="1eea1-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="1eea1-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="1eea1-118">Možnost zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="1eea1-118">Benefit Option</span></span> | <span data-ttu-id="1eea1-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="1eea1-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="1eea1-120">Plán zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="1eea1-120">Benefit Plan</span></span> | <span data-ttu-id="1eea1-121">cdm_benefitplan (není povoleno pro podporu vlastních polí)</span><span class="sxs-lookup"><span data-stu-id="1eea1-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="1eea1-122">Typ zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="1eea1-122">Benefit Type</span></span> | <span data-ttu-id="1eea1-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="1eea1-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="1eea1-124">Entity úkolů obchodního procesu</span><span class="sxs-lookup"><span data-stu-id="1eea1-124">Business process tasks entities</span></span>

| <span data-ttu-id="1eea1-125">Název</span><span class="sxs-lookup"><span data-stu-id="1eea1-125">Name</span></span> | <span data-ttu-id="1eea1-126">Celek</span><span class="sxs-lookup"><span data-stu-id="1eea1-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1eea1-127">Kalendář obchodních procesů</span><span class="sxs-lookup"><span data-stu-id="1eea1-127">Business Process Calendar</span></span> | <span data-ttu-id="1eea1-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="1eea1-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="1eea1-129">Přiřazení skupiny obchodních procesů</span><span class="sxs-lookup"><span data-stu-id="1eea1-129">Business Process Group Assignment</span></span> | <span data-ttu-id="1eea1-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="1eea1-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="1eea1-131">Skupina úkolů knihovny obchodních procesů</span><span class="sxs-lookup"><span data-stu-id="1eea1-131">Business Process Library Task Group</span></span> | <span data-ttu-id="1eea1-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="1eea1-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="1eea1-133">Fáze obchodního procesu</span><span class="sxs-lookup"><span data-stu-id="1eea1-133">Business Process Stage</span></span> | <span data-ttu-id="1eea1-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="1eea1-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="1eea1-135">Záhlaví šablony kontrolního seznamu</span><span class="sxs-lookup"><span data-stu-id="1eea1-135">Checklist Template Header</span></span> | <span data-ttu-id="1eea1-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="1eea1-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="1eea1-137">Úkol šablony kontrolního seznamu</span><span class="sxs-lookup"><span data-stu-id="1eea1-137">Checklist Template Task</span></span> | <span data-ttu-id="1eea1-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="1eea1-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="1eea1-139">Entity kompenzace</span><span class="sxs-lookup"><span data-stu-id="1eea1-139">Compensation entities</span></span>

| <span data-ttu-id="1eea1-140">Název</span><span class="sxs-lookup"><span data-stu-id="1eea1-140">Name</span></span> | <span data-ttu-id="1eea1-141">Celek</span><span class="sxs-lookup"><span data-stu-id="1eea1-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1eea1-142">Fixní plán kompenzace</span><span class="sxs-lookup"><span data-stu-id="1eea1-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="1eea1-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="1eea1-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="1eea1-144">Mřížka kompenzace</span><span class="sxs-lookup"><span data-stu-id="1eea1-144">Compensation Grid</span></span> | <span data-ttu-id="1eea1-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="1eea1-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="1eea1-146">Úroveň kompenzace</span><span class="sxs-lookup"><span data-stu-id="1eea1-146">Compensation Level</span></span> | <span data-ttu-id="1eea1-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="1eea1-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="1eea1-148">Interval plateb kompenzace</span><span class="sxs-lookup"><span data-stu-id="1eea1-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="1eea1-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="1eea1-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="1eea1-150">Nastavení referenčního bodu kompenzace</span><span class="sxs-lookup"><span data-stu-id="1eea1-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="1eea1-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="1eea1-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="1eea1-152">Linie nastavení referenčního bodu kompenzace</span><span class="sxs-lookup"><span data-stu-id="1eea1-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="1eea1-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="1eea1-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="1eea1-154">Oblast kompenzace</span><span class="sxs-lookup"><span data-stu-id="1eea1-154">Compensation Region</span></span> | <span data-ttu-id="1eea1-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="1eea1-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="1eea1-156">Struktura kompenzací</span><span class="sxs-lookup"><span data-stu-id="1eea1-156">Compensation Structure</span></span> | <span data-ttu-id="1eea1-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="1eea1-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="1eea1-158">Plán variabilní kompenzace</span><span class="sxs-lookup"><span data-stu-id="1eea1-158">Compensation Variable Plan</span></span> | <span data-ttu-id="1eea1-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="1eea1-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="1eea1-160">Úroveň plánu variabilní kompenzace</span><span class="sxs-lookup"><span data-stu-id="1eea1-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="1eea1-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="1eea1-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="1eea1-162">Typ plánu variabilní kompenzace</span><span class="sxs-lookup"><span data-stu-id="1eea1-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="1eea1-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="1eea1-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="1eea1-164">Událost fixní kompenzace</span><span class="sxs-lookup"><span data-stu-id="1eea1-164">Fixed Compensation Event</span></span> | <span data-ttu-id="1eea1-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="1eea1-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="1eea1-166">Pravidlo připsání</span><span class="sxs-lookup"><span data-stu-id="1eea1-166">Vesting Rule</span></span> | <span data-ttu-id="1eea1-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="1eea1-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="1eea1-168">Fixní kompenzace pracovníka</span><span class="sxs-lookup"><span data-stu-id="1eea1-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="1eea1-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="1eea1-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="1eea1-170">Entity organizace</span><span class="sxs-lookup"><span data-stu-id="1eea1-170">Organization entities</span></span>

| <span data-ttu-id="1eea1-171">Název</span><span class="sxs-lookup"><span data-stu-id="1eea1-171">Name</span></span> | <span data-ttu-id="1eea1-172">Celek</span><span class="sxs-lookup"><span data-stu-id="1eea1-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1eea1-173">Oddělení</span><span class="sxs-lookup"><span data-stu-id="1eea1-173">Department</span></span> | <span data-ttu-id="1eea1-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="1eea1-174">cdm_department</span></span> |
| <span data-ttu-id="1eea1-175">Zaměstnání</span><span class="sxs-lookup"><span data-stu-id="1eea1-175">Employment</span></span> | <span data-ttu-id="1eea1-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="1eea1-176">cdm_employment</span></span> |
| <span data-ttu-id="1eea1-177">Společnost</span><span class="sxs-lookup"><span data-stu-id="1eea1-177">Company</span></span> | <span data-ttu-id="1eea1-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="1eea1-178">cdm_company</span></span> |
| <span data-ttu-id="1eea1-179">Pozice</span><span class="sxs-lookup"><span data-stu-id="1eea1-179">Job</span></span> | <span data-ttu-id="1eea1-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="1eea1-180">cdm_job</span></span> |
| <span data-ttu-id="1eea1-181">Pracovní funkce</span><span class="sxs-lookup"><span data-stu-id="1eea1-181">Job Function</span></span> | <span data-ttu-id="1eea1-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="1eea1-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="1eea1-183">Pracovní pozice</span><span class="sxs-lookup"><span data-stu-id="1eea1-183">Job Position</span></span> | <span data-ttu-id="1eea1-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="1eea1-184">cdm_jobposition</span></span> |
| <span data-ttu-id="1eea1-185">Typ pozice</span><span class="sxs-lookup"><span data-stu-id="1eea1-185">Position Type</span></span> | <span data-ttu-id="1eea1-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="1eea1-186">cdm_positiontype</span></span> |
| <span data-ttu-id="1eea1-187">Přiřazení pracovníka k pozici</span><span class="sxs-lookup"><span data-stu-id="1eea1-187">Position Worker Assignment</span></span> | <span data-ttu-id="1eea1-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="1eea1-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="1eea1-189">Dimenze pracovních pozic</span><span class="sxs-lookup"><span data-stu-id="1eea1-189">Job Position Dimension</span></span> | <span data-ttu-id="1eea1-190">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="1eea1-190">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="1eea1-191">Typ práce</span><span class="sxs-lookup"><span data-stu-id="1eea1-191">Job Type</span></span> | <span data-ttu-id="1eea1-192">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="1eea1-192">cdm_jobtype</span></span> |
| <span data-ttu-id="1eea1-193">Jazyk</span><span class="sxs-lookup"><span data-stu-id="1eea1-193">Language</span></span> | <span data-ttu-id="1eea1-194">cdm_language</span><span class="sxs-lookup"><span data-stu-id="1eea1-194">cdm_language</span></span> |
| <span data-ttu-id="1eea1-195">Pozice</span><span class="sxs-lookup"><span data-stu-id="1eea1-195">Title</span></span> | <span data-ttu-id="1eea1-196">cdm_title</span><span class="sxs-lookup"><span data-stu-id="1eea1-196">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="1eea1-197">Finanční dimenze pro **Typ pozice**, **Přiřazení pracovníka poziec** a **Zaměstnání** poskytují integraci v jediném směru do Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="1eea1-197">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Common Data Service.</span></span> <span data-ttu-id="1eea1-198">Aktualizace finančních dimenzí nelze v současné době synchronizovat z Common Data Service do modulu Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1eea1-198">Financial dimensions updates currently can't synchronize from Common Data Service to Human Resources.</span></span> 

## <a name="leave-and-absence-entities"></a><span data-ttu-id="1eea1-199">Entity pracovního volna a absence</span><span class="sxs-lookup"><span data-stu-id="1eea1-199">Leave and absence entities</span></span>

| <span data-ttu-id="1eea1-200">Jméno</span><span class="sxs-lookup"><span data-stu-id="1eea1-200">Name</span></span> | <span data-ttu-id="1eea1-201">Celek</span><span class="sxs-lookup"><span data-stu-id="1eea1-201">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1eea1-202">Transakce fondu pracovního volna</span><span class="sxs-lookup"><span data-stu-id="1eea1-202">Leave Bank Transaction</span></span> | <span data-ttu-id="1eea1-203">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="1eea1-203">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="1eea1-204">Opustit zápis</span><span class="sxs-lookup"><span data-stu-id="1eea1-204">Leave Enrollment</span></span> | <span data-ttu-id="1eea1-205">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="1eea1-205">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="1eea1-206">Plán pracovního volna</span><span class="sxs-lookup"><span data-stu-id="1eea1-206">Leave Plan</span></span> | <span data-ttu-id="1eea1-207">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="1eea1-207">cdm_leaveplan</span></span> |
| <span data-ttu-id="1eea1-208">Žádost o pracovní volno</span><span class="sxs-lookup"><span data-stu-id="1eea1-208">Leave Request</span></span> | <span data-ttu-id="1eea1-209">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="1eea1-209">cdm_leaverequest</span></span> |
| <span data-ttu-id="1eea1-210">Podrobnosti o požadavku na dovolenou</span><span class="sxs-lookup"><span data-stu-id="1eea1-210">Leave Request Detail</span></span> | <span data-ttu-id="1eea1-211">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="1eea1-211">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="1eea1-212">Typ pracovního volna</span><span class="sxs-lookup"><span data-stu-id="1eea1-212">Leave Type</span></span> | <span data-ttu-id="1eea1-213">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="1eea1-213">cdm_leavetype</span></span> |
| <span data-ttu-id="1eea1-214">Kód důvodu typu volna</span><span class="sxs-lookup"><span data-stu-id="1eea1-214">Leave Type Reason Code</span></span> | <span data-ttu-id="1eea1-215">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="1eea1-215">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="1eea1-216">Entita mzdy</span><span class="sxs-lookup"><span data-stu-id="1eea1-216">Payroll entities</span></span>

| <span data-ttu-id="1eea1-217">Název</span><span class="sxs-lookup"><span data-stu-id="1eea1-217">Name</span></span> | <span data-ttu-id="1eea1-218">Celek</span><span class="sxs-lookup"><span data-stu-id="1eea1-218">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1eea1-219">Platební cyklus</span><span class="sxs-lookup"><span data-stu-id="1eea1-219">Pay Cycle</span></span> | <span data-ttu-id="1eea1-220">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="1eea1-220">cdm_paycycle</span></span> |
| <span data-ttu-id="1eea1-221">Mzdové období</span><span class="sxs-lookup"><span data-stu-id="1eea1-221">Pay Period</span></span> | <span data-ttu-id="1eea1-222">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="1eea1-222">cdm_payperiod</span></span> |
| <span data-ttu-id="1eea1-223">Kód příjmů mzdy</span><span class="sxs-lookup"><span data-stu-id="1eea1-223">Payroll Earning Code</span></span> | <span data-ttu-id="1eea1-224">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="1eea1-224">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="1eea1-225">Úhrady na bankovní účet</span><span class="sxs-lookup"><span data-stu-id="1eea1-225">Bank Account Disbursement</span></span> | <span data-ttu-id="1eea1-226">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="1eea1-226">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="1eea1-227">Daňová oblast</span><span class="sxs-lookup"><span data-stu-id="1eea1-227">Tax Region</span></span> | <span data-ttu-id="1eea1-228">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="1eea1-228">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="1eea1-229">Entity pracovníků</span><span class="sxs-lookup"><span data-stu-id="1eea1-229">Worker entities</span></span>

| <span data-ttu-id="1eea1-230">Název</span><span class="sxs-lookup"><span data-stu-id="1eea1-230">Name</span></span> | <span data-ttu-id="1eea1-231">Celek</span><span class="sxs-lookup"><span data-stu-id="1eea1-231">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1eea1-232">Pracovní podproces</span><span class="sxs-lookup"><span data-stu-id="1eea1-232">Worker</span></span> | <span data-ttu-id="1eea1-233">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="1eea1-233">cdm_worker</span></span> |
| <span data-ttu-id="1eea1-234">Adresa pracovníka</span><span class="sxs-lookup"><span data-stu-id="1eea1-234">Worker Address</span></span> | <span data-ttu-id="1eea1-235">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="1eea1-235">cdm_workeraddress</span></span> |
| <span data-ttu-id="1eea1-236">Osobní údaj pracovníka</span><span class="sxs-lookup"><span data-stu-id="1eea1-236">Worker Personal Detail</span></span> | <span data-ttu-id="1eea1-237">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="1eea1-237">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="1eea1-238">Osobní identifikační číslo pracovníka</span><span class="sxs-lookup"><span data-stu-id="1eea1-238">Worker Person Identification Number</span></span> | <span data-ttu-id="1eea1-239">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="1eea1-239">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="1eea1-240">Typ osobní identifikace pracovníka</span><span class="sxs-lookup"><span data-stu-id="1eea1-240">Worker Person Identification Type</span></span> | <span data-ttu-id="1eea1-241">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="1eea1-241">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="1eea1-242">Pracovní kalendář</span><span class="sxs-lookup"><span data-stu-id="1eea1-242">Work Calendar</span></span> | <span data-ttu-id="1eea1-243">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="1eea1-243">cdm_workcalendar</span></span> |
| <span data-ttu-id="1eea1-244">Datum pracovního kalendáře</span><span class="sxs-lookup"><span data-stu-id="1eea1-244">Work Calendar Day</span></span> | <span data-ttu-id="1eea1-245">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="1eea1-245">cdm_workcalendarday</span></span> |
| <span data-ttu-id="1eea1-246">Svátek pracovního kalendáře</span><span class="sxs-lookup"><span data-stu-id="1eea1-246">Work Calendar Holiday</span></span> |<span data-ttu-id="1eea1-247">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="1eea1-247">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="1eea1-248">Řádek data pracovního kalendáře</span><span class="sxs-lookup"><span data-stu-id="1eea1-248">Work Calendar Holiday Line</span></span> | <span data-ttu-id="1eea1-249">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="1eea1-249">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="1eea1-250">Časový interval pracovního kalenáře</span><span class="sxs-lookup"><span data-stu-id="1eea1-250">Work Calendar Time Interval</span></span> | <span data-ttu-id="1eea1-251">cdm_workcalendartimeinterval (není povoleno pro podporu vlastních polí)</span><span class="sxs-lookup"><span data-stu-id="1eea1-251">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="1eea1-252">Bankovní účet pracovníka</span><span class="sxs-lookup"><span data-stu-id="1eea1-252">Worker Bank Account</span></span> | <span data-ttu-id="1eea1-253">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="1eea1-253">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="1eea1-254">Entity nastavení pracovníků</span><span class="sxs-lookup"><span data-stu-id="1eea1-254">Worker setup entities</span></span>

| <span data-ttu-id="1eea1-255">Název</span><span class="sxs-lookup"><span data-stu-id="1eea1-255">Name</span></span> | <span data-ttu-id="1eea1-256">Celek</span><span class="sxs-lookup"><span data-stu-id="1eea1-256">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1eea1-257">Stav veterána</span><span class="sxs-lookup"><span data-stu-id="1eea1-257">Veteran Status</span></span> | <span data-ttu-id="1eea1-258">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="1eea1-258">cdm_veteranstatus</span></span> |
| <span data-ttu-id="1eea1-259">Etnický původ</span><span class="sxs-lookup"><span data-stu-id="1eea1-259">Ethnic Origin</span></span> | <span data-ttu-id="1eea1-260">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="1eea1-260">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="1eea1-261">Kód důvodu</span><span class="sxs-lookup"><span data-stu-id="1eea1-261">Reason Code</span></span> | <span data-ttu-id="1eea1-262">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="1eea1-262">cdm_reasoncode</span></span> |
| <span data-ttu-id="1eea1-263">Subjekt vydávající identifikaci osob</span><span class="sxs-lookup"><span data-stu-id="1eea1-263">Person Identification Issuing Agency</span></span> | <span data-ttu-id="1eea1-264">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="1eea1-264">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="1eea1-265">Entity kompetence</span><span class="sxs-lookup"><span data-stu-id="1eea1-265">Competency entities</span></span>

| <span data-ttu-id="1eea1-266">Název</span><span class="sxs-lookup"><span data-stu-id="1eea1-266">Name</span></span> | <span data-ttu-id="1eea1-267">Celek</span><span class="sxs-lookup"><span data-stu-id="1eea1-267">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1eea1-268">Typ dovednosti</span><span class="sxs-lookup"><span data-stu-id="1eea1-268">Skill Type</span></span> | <span data-ttu-id="1eea1-269">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="1eea1-269">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="1eea1-270">Modely vztahu entity</span><span class="sxs-lookup"><span data-stu-id="1eea1-270">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="1eea1-271">Pracovní podproces</span><span class="sxs-lookup"><span data-stu-id="1eea1-271">Worker</span></span>

![Pracovní podproces](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="1eea1-273">Práce a pracovní pozice</span><span class="sxs-lookup"><span data-stu-id="1eea1-273">Job and Job Position</span></span>

![Práce a pracovní pozice](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="1eea1-275">Zaměstnanecké výhody</span><span class="sxs-lookup"><span data-stu-id="1eea1-275">Benefits</span></span>

![Zaměstnanecké výhody](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="1eea1-277">Kompenzace</span><span class="sxs-lookup"><span data-stu-id="1eea1-277">Compensation</span></span>

![Kompenzace](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="1eea1-279">Odejít</span><span class="sxs-lookup"><span data-stu-id="1eea1-279">Leave</span></span>

![Odejít](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="1eea1-281">Pracovní kalendář</span><span class="sxs-lookup"><span data-stu-id="1eea1-281">Work Calendar</span></span>

![Pracovní kalendář](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="1eea1-283">Viz také</span><span class="sxs-lookup"><span data-stu-id="1eea1-283">See also</span></span>

[<span data-ttu-id="1eea1-284">Volba technologie integrace dat</span><span class="sxs-lookup"><span data-stu-id="1eea1-284">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="1eea1-285">Konfigurace integrace s Common Data Service</span><span class="sxs-lookup"><span data-stu-id="1eea1-285">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)
