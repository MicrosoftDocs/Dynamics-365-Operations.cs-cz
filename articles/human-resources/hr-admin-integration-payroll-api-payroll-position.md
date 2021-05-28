---
title: Podrobnosti mzdy pro pozice
description: Toto téma poskytuje informace a ukázkový dotaz pro entitu detailů výplatní listiny pro pozice v Dynamics 365 Human Resources.
author: jcart
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
ms.openlocfilehash: 7b23ac5d11b18c77109be21afe1570755dccba20
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019315"
---
# <a name="payroll-position"></a><span data-ttu-id="de6ca-103">Pozice mzdy</span><span class="sxs-lookup"><span data-stu-id="de6ca-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="de6ca-104">Toto téma poskytuje informace a ukázkový dotaz pro entitu detailů výplatní listiny pro pozice v Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="de6ca-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="de6ca-105">Vlastnosti</span><span class="sxs-lookup"><span data-stu-id="de6ca-105">Properties</span></span>

| <span data-ttu-id="de6ca-106">Vlastnost</span><span class="sxs-lookup"><span data-stu-id="de6ca-106">Property</span></span><br><span data-ttu-id="de6ca-107">**Fyzický název**</span><span class="sxs-lookup"><span data-stu-id="de6ca-107">**Physical name**</span></span><br><span data-ttu-id="de6ca-108">**_Typ_**</span><span class="sxs-lookup"><span data-stu-id="de6ca-108">**_Type_**</span></span> | <span data-ttu-id="de6ca-109">Použít</span><span class="sxs-lookup"><span data-stu-id="de6ca-109">Use</span></span> | <span data-ttu-id="de6ca-110">popis</span><span class="sxs-lookup"><span data-stu-id="de6ca-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="de6ca-111">**Roční normální hodiny**</span><span class="sxs-lookup"><span data-stu-id="de6ca-111">**Annual regular hours**</span></span><br><span data-ttu-id="de6ca-112">annualregularhours</span><span class="sxs-lookup"><span data-stu-id="de6ca-112">annualregularhours</span></span><br><span data-ttu-id="de6ca-113">*Des. místo*</span><span class="sxs-lookup"><span data-stu-id="de6ca-113">*Decimal*</span></span> | <span data-ttu-id="de6ca-114">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="de6ca-114">Read-only</span></span><br><span data-ttu-id="de6ca-115">Povinná</span><span class="sxs-lookup"><span data-stu-id="de6ca-115">Required</span></span> | <span data-ttu-id="de6ca-116">Roční řádné hodiny definované na pozici.</span><span class="sxs-lookup"><span data-stu-id="de6ca-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="de6ca-117">**ID entity detailů pozice na výplatní listině**</span><span class="sxs-lookup"><span data-stu-id="de6ca-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="de6ca-118">payrollpositiondetailsentityid</span><span class="sxs-lookup"><span data-stu-id="de6ca-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="de6ca-119">*Guid*</span><span class="sxs-lookup"><span data-stu-id="de6ca-119">*Guid*</span></span> | <span data-ttu-id="de6ca-120">Povinná</span><span class="sxs-lookup"><span data-stu-id="de6ca-120">Required</span></span><br><span data-ttu-id="de6ca-121">Generováno systémem.</span><span class="sxs-lookup"><span data-stu-id="de6ca-121">System generated.</span></span> | <span data-ttu-id="de6ca-122">Systémem generovaná hodnota GUID pro jedinečnou identifikaci pozice.</span><span class="sxs-lookup"><span data-stu-id="de6ca-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="de6ca-123">**Primární pole**</span><span class="sxs-lookup"><span data-stu-id="de6ca-123">**Primary field**</span></span><br><span data-ttu-id="de6ca-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="de6ca-124">mshr_primaryfield</span></span><br><span data-ttu-id="de6ca-125">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="de6ca-125">*String*</span></span> | <span data-ttu-id="de6ca-126">Povinná</span><span class="sxs-lookup"><span data-stu-id="de6ca-126">Required</span></span><br><span data-ttu-id="de6ca-127">Generováno systémem</span><span class="sxs-lookup"><span data-stu-id="de6ca-127">System generated</span></span> |  |
| <span data-ttu-id="de6ca-128">**Hodnota ID pracovní pozice**</span><span class="sxs-lookup"><span data-stu-id="de6ca-128">**Position job ID value**</span></span><br><span data-ttu-id="de6ca-129">_mshr_fk_positionjob_id_value</span><span class="sxs-lookup"><span data-stu-id="de6ca-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="de6ca-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="de6ca-130">*GUID*</span></span> | <span data-ttu-id="de6ca-131">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="de6ca-131">Read-only</span></span><br><span data-ttu-id="de6ca-132">Povinná</span><span class="sxs-lookup"><span data-stu-id="de6ca-132">Required</span></span><br><span data-ttu-id="de6ca-133">Cizí klíč: mshr_PayrollPositionJobEntity mshr_payrollpositionjobentity</span><span class="sxs-lookup"><span data-stu-id="de6ca-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="de6ca-134">ID práce přidružené k pozici.</span><span class="sxs-lookup"><span data-stu-id="de6ca-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="de6ca-135">**Hodnota ID pevného plánu kompenzace**</span><span class="sxs-lookup"><span data-stu-id="de6ca-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="de6ca-136">_mshr_fk_fixedcompplan_id_value</span><span class="sxs-lookup"><span data-stu-id="de6ca-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="de6ca-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="de6ca-137">*GUID*</span></span> | <span data-ttu-id="de6ca-138">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="de6ca-138">Read-only</span></span><br><span data-ttu-id="de6ca-139">Povinná</span><span class="sxs-lookup"><span data-stu-id="de6ca-139">Required</span></span><br><span data-ttu-id="de6ca-140">Cizí klíč: mshr_FixedCompPlan_id z mshr_payrollfixedcompensationplanentity</span><span class="sxs-lookup"><span data-stu-id="de6ca-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="de6ca-141">ID plánu pevné kompenzace přidruženého k pozici.</span><span class="sxs-lookup"><span data-stu-id="de6ca-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="de6ca-142">**ID platebního cyklu**</span><span class="sxs-lookup"><span data-stu-id="de6ca-142">**Pay cycle ID**</span></span><br><span data-ttu-id="de6ca-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="de6ca-143">mshr_primaryfield</span></span><br><span data-ttu-id="de6ca-144">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="de6ca-144">*String*</span></span> | <span data-ttu-id="de6ca-145">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="de6ca-145">Read-only</span></span><br><span data-ttu-id="de6ca-146">Povinná</span><span class="sxs-lookup"><span data-stu-id="de6ca-146">Required</span></span> | <span data-ttu-id="de6ca-147">Platební cyklus definovaný na pozici.</span><span class="sxs-lookup"><span data-stu-id="de6ca-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="de6ca-148">**Placené právnickou osobu**</span><span class="sxs-lookup"><span data-stu-id="de6ca-148">**Paid by legal entity**</span></span><br><span data-ttu-id="de6ca-149">paidbylegalentity</span><span class="sxs-lookup"><span data-stu-id="de6ca-149">paidbylegalentity</span></span><br><span data-ttu-id="de6ca-150">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="de6ca-150">*String*</span></span> | <span data-ttu-id="de6ca-151">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="de6ca-151">Read-only</span></span><br><span data-ttu-id="de6ca-152">Povinná</span><span class="sxs-lookup"><span data-stu-id="de6ca-152">Required</span></span> | <span data-ttu-id="de6ca-153">Právnická osoba definovaná na pozici odpovědné za vystavení platby.</span><span class="sxs-lookup"><span data-stu-id="de6ca-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="de6ca-154">**ID pozice**</span><span class="sxs-lookup"><span data-stu-id="de6ca-154">**Position ID**</span></span><br><span data-ttu-id="de6ca-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="de6ca-155">mshr_positionid</span></span><br><span data-ttu-id="de6ca-156">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="de6ca-156">*String*</span></span> | <span data-ttu-id="de6ca-157">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="de6ca-157">Read-only</span></span><br><span data-ttu-id="de6ca-158">Povinná</span><span class="sxs-lookup"><span data-stu-id="de6ca-158">Required</span></span> | <span data-ttu-id="de6ca-159">Identifikace pozice.</span><span class="sxs-lookup"><span data-stu-id="de6ca-159">The ID of the position.</span></span> |
| <span data-ttu-id="de6ca-160">**Platné do**</span><span class="sxs-lookup"><span data-stu-id="de6ca-160">**Valid to**</span></span><br><span data-ttu-id="de6ca-161">validto</span><span class="sxs-lookup"><span data-stu-id="de6ca-161">validto</span></span><br><span data-ttu-id="de6ca-162">*Posun data a času*</span><span class="sxs-lookup"><span data-stu-id="de6ca-162">*Date Time Offset*</span></span> | <span data-ttu-id="de6ca-163">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="de6ca-163">Read-only</span></span><br><span data-ttu-id="de6ca-164">Povinná</span><span class="sxs-lookup"><span data-stu-id="de6ca-164">Required</span></span> |<span data-ttu-id="de6ca-165">Datum, od kterého jsou údaje o poloze platné.</span><span class="sxs-lookup"><span data-stu-id="de6ca-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="de6ca-166">**Platné od**</span><span class="sxs-lookup"><span data-stu-id="de6ca-166">**Valid from**</span></span><br><span data-ttu-id="de6ca-167">validfrom</span><span class="sxs-lookup"><span data-stu-id="de6ca-167">validfrom</span></span><br><span data-ttu-id="de6ca-168">*Posun data a času*</span><span class="sxs-lookup"><span data-stu-id="de6ca-168">*Date Time Offset*</span></span> | <span data-ttu-id="de6ca-169">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="de6ca-169">Read-only</span></span><br><span data-ttu-id="de6ca-170">Povinná</span><span class="sxs-lookup"><span data-stu-id="de6ca-170">Required</span></span> |<span data-ttu-id="de6ca-171">Datum, do kterého jsou údaje o poloze platné.</span><span class="sxs-lookup"><span data-stu-id="de6ca-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="de6ca-172">**Dotaz**</span><span class="sxs-lookup"><span data-stu-id="de6ca-172">**Query**</span></span>

<span data-ttu-id="de6ca-173">**Žádost**</span><span class="sxs-lookup"><span data-stu-id="de6ca-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="de6ca-174">**Odezva**</span><span class="sxs-lookup"><span data-stu-id="de6ca-174">**Response**</span></span>

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
