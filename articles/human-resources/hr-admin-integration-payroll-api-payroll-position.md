---
title: Podrobnosti mzdy pro pozice
description: Toto téma poskytuje informace a ukázkový dotaz pro entitu detailů výplatní listiny pro pozice v Dynamics 365 Human Resources.
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f6c4bb0e2f4521e8c870f6c4fb645e2ce506138c
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881940"
---
# <a name="payroll-position"></a><span data-ttu-id="82705-103">Pozice mzdy</span><span class="sxs-lookup"><span data-stu-id="82705-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="82705-104">Toto téma poskytuje informace a ukázkový dotaz pro entitu detailů výplatní listiny pro pozice v Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="82705-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="82705-105">Vlastnosti</span><span class="sxs-lookup"><span data-stu-id="82705-105">Properties</span></span>

| <span data-ttu-id="82705-106">Vlastnost</span><span class="sxs-lookup"><span data-stu-id="82705-106">Property</span></span><br><span data-ttu-id="82705-107">**Fyzický název**</span><span class="sxs-lookup"><span data-stu-id="82705-107">**Physical name**</span></span><br><span data-ttu-id="82705-108">**_Typ_**</span><span class="sxs-lookup"><span data-stu-id="82705-108">**_Type_**</span></span> | <span data-ttu-id="82705-109">Použít</span><span class="sxs-lookup"><span data-stu-id="82705-109">Use</span></span> | <span data-ttu-id="82705-110">popis</span><span class="sxs-lookup"><span data-stu-id="82705-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="82705-111">**Roční normální hodiny**</span><span class="sxs-lookup"><span data-stu-id="82705-111">**Annual regular hours**</span></span><br><span data-ttu-id="82705-112">annualregularhours</span><span class="sxs-lookup"><span data-stu-id="82705-112">annualregularhours</span></span><br><span data-ttu-id="82705-113">*Des. místo*</span><span class="sxs-lookup"><span data-stu-id="82705-113">*Decimal*</span></span> | <span data-ttu-id="82705-114">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="82705-114">Read-only</span></span><br><span data-ttu-id="82705-115">Povinná</span><span class="sxs-lookup"><span data-stu-id="82705-115">Required</span></span> | <span data-ttu-id="82705-116">Roční řádné hodiny definované na pozici.</span><span class="sxs-lookup"><span data-stu-id="82705-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="82705-117">**ID entity detailů pozice na výplatní listině**</span><span class="sxs-lookup"><span data-stu-id="82705-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="82705-118">payrollpositiondetailsentityid</span><span class="sxs-lookup"><span data-stu-id="82705-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="82705-119">*Guid*</span><span class="sxs-lookup"><span data-stu-id="82705-119">*Guid*</span></span> | <span data-ttu-id="82705-120">Povinná</span><span class="sxs-lookup"><span data-stu-id="82705-120">Required</span></span><br><span data-ttu-id="82705-121">Generováno systémem.</span><span class="sxs-lookup"><span data-stu-id="82705-121">System generated.</span></span> | <span data-ttu-id="82705-122">Systémem generovaná hodnota GUID pro jedinečnou identifikaci pozice.</span><span class="sxs-lookup"><span data-stu-id="82705-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="82705-123">**Primární pole**</span><span class="sxs-lookup"><span data-stu-id="82705-123">**Primary field**</span></span><br><span data-ttu-id="82705-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="82705-124">mshr_primaryfield</span></span><br><span data-ttu-id="82705-125">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="82705-125">*String*</span></span> | <span data-ttu-id="82705-126">Povinná</span><span class="sxs-lookup"><span data-stu-id="82705-126">Required</span></span><br><span data-ttu-id="82705-127">Generováno systémem</span><span class="sxs-lookup"><span data-stu-id="82705-127">System generated</span></span> |  |
| <span data-ttu-id="82705-128">**Hodnota ID pracovní pozice**</span><span class="sxs-lookup"><span data-stu-id="82705-128">**Position job ID value**</span></span><br><span data-ttu-id="82705-129">_mshr_fk_positionjob_id_value</span><span class="sxs-lookup"><span data-stu-id="82705-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="82705-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="82705-130">*GUID*</span></span> | <span data-ttu-id="82705-131">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="82705-131">Read-only</span></span><br><span data-ttu-id="82705-132">Povinná</span><span class="sxs-lookup"><span data-stu-id="82705-132">Required</span></span><br><span data-ttu-id="82705-133">Cizí klíč: mshr_PayrollPositionJobEntity mshr_payrollpositionjobentity</span><span class="sxs-lookup"><span data-stu-id="82705-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="82705-134">ID práce přidružené k pozici.</span><span class="sxs-lookup"><span data-stu-id="82705-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="82705-135">**Hodnota ID pevného plánu kompenzace**</span><span class="sxs-lookup"><span data-stu-id="82705-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="82705-136">_mshr_fk_fixedcompplan_id_value</span><span class="sxs-lookup"><span data-stu-id="82705-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="82705-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="82705-137">*GUID*</span></span> | <span data-ttu-id="82705-138">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="82705-138">Read-only</span></span><br><span data-ttu-id="82705-139">Povinná</span><span class="sxs-lookup"><span data-stu-id="82705-139">Required</span></span><br><span data-ttu-id="82705-140">Cizí klíč: mshr_FixedCompPlan_id z mshr_payrollfixedcompensationplanentity</span><span class="sxs-lookup"><span data-stu-id="82705-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="82705-141">ID plánu pevné kompenzace přidruženého k pozici.</span><span class="sxs-lookup"><span data-stu-id="82705-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="82705-142">**ID platebního cyklu**</span><span class="sxs-lookup"><span data-stu-id="82705-142">**Pay cycle ID**</span></span><br><span data-ttu-id="82705-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="82705-143">mshr_primaryfield</span></span><br><span data-ttu-id="82705-144">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="82705-144">*String*</span></span> | <span data-ttu-id="82705-145">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="82705-145">Read-only</span></span><br><span data-ttu-id="82705-146">Povinná</span><span class="sxs-lookup"><span data-stu-id="82705-146">Required</span></span> | <span data-ttu-id="82705-147">Platební cyklus definovaný na pozici.</span><span class="sxs-lookup"><span data-stu-id="82705-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="82705-148">**Placené právnickou osobu**</span><span class="sxs-lookup"><span data-stu-id="82705-148">**Paid by legal entity**</span></span><br><span data-ttu-id="82705-149">paidbylegalentity</span><span class="sxs-lookup"><span data-stu-id="82705-149">paidbylegalentity</span></span><br><span data-ttu-id="82705-150">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="82705-150">*String*</span></span> | <span data-ttu-id="82705-151">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="82705-151">Read-only</span></span><br><span data-ttu-id="82705-152">Povinná</span><span class="sxs-lookup"><span data-stu-id="82705-152">Required</span></span> | <span data-ttu-id="82705-153">Právnická osoba definovaná na pozici odpovědné za vystavení platby.</span><span class="sxs-lookup"><span data-stu-id="82705-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="82705-154">**ID pozice**</span><span class="sxs-lookup"><span data-stu-id="82705-154">**Position ID**</span></span><br><span data-ttu-id="82705-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="82705-155">mshr_positionid</span></span><br><span data-ttu-id="82705-156">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="82705-156">*String*</span></span> | <span data-ttu-id="82705-157">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="82705-157">Read-only</span></span><br><span data-ttu-id="82705-158">Povinná</span><span class="sxs-lookup"><span data-stu-id="82705-158">Required</span></span> | <span data-ttu-id="82705-159">Identifikace pozice.</span><span class="sxs-lookup"><span data-stu-id="82705-159">The ID of the position.</span></span> |
| <span data-ttu-id="82705-160">**Platné do**</span><span class="sxs-lookup"><span data-stu-id="82705-160">**Valid to**</span></span><br><span data-ttu-id="82705-161">validto</span><span class="sxs-lookup"><span data-stu-id="82705-161">validto</span></span><br><span data-ttu-id="82705-162">*Posun data a času*</span><span class="sxs-lookup"><span data-stu-id="82705-162">*Date Time Offset*</span></span> | <span data-ttu-id="82705-163">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="82705-163">Read-only</span></span><br><span data-ttu-id="82705-164">Povinná</span><span class="sxs-lookup"><span data-stu-id="82705-164">Required</span></span> |<span data-ttu-id="82705-165">Datum, od kterého jsou údaje o poloze platné.</span><span class="sxs-lookup"><span data-stu-id="82705-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="82705-166">**Platné od**</span><span class="sxs-lookup"><span data-stu-id="82705-166">**Valid from**</span></span><br><span data-ttu-id="82705-167">validfrom</span><span class="sxs-lookup"><span data-stu-id="82705-167">validfrom</span></span><br><span data-ttu-id="82705-168">*Posun data a času*</span><span class="sxs-lookup"><span data-stu-id="82705-168">*Date Time Offset*</span></span> | <span data-ttu-id="82705-169">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="82705-169">Read-only</span></span><br><span data-ttu-id="82705-170">Povinná</span><span class="sxs-lookup"><span data-stu-id="82705-170">Required</span></span> |<span data-ttu-id="82705-171">Datum, do kterého jsou údaje o poloze platné.</span><span class="sxs-lookup"><span data-stu-id="82705-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="82705-172">**Dotaz**</span><span class="sxs-lookup"><span data-stu-id="82705-172">**Query**</span></span>

<span data-ttu-id="82705-173">**Žádost**</span><span class="sxs-lookup"><span data-stu-id="82705-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="82705-174">**Odezva**</span><span class="sxs-lookup"><span data-stu-id="82705-174">**Response**</span></span>

```json
{
            "mshr_positionid": "000276",
            "mshr_paycycleid": "w",
            "mshr_annualregularhours": 3000,
            "mshr_paidbylegalentity": "USMF",
            "mshr_validfrom": "2021-03-14T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_primaryfield": "000276 | 3/14/2021",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```
