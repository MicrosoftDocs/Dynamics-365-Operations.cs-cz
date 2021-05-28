---
title: Mzdový plán fixní kompenzace
description: Toto téma poskytuje informace a ukázkový dotaz pro entitu pevného plánu kompenzace v Dynamics 365 Human Resources.
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
ms.openlocfilehash: 85cfce6f626090adab422ea6c60fc0778fd1ac67
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021289"
---
# <a name="payroll-fixed-compensation-plan"></a><span data-ttu-id="ea200-103">Mzdový plán fixní kompenzace</span><span class="sxs-lookup"><span data-stu-id="ea200-103">Payroll fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ea200-104">Toto téma poskytuje informace a ukázkový dotaz pro entitu pevného plánu kompenzace v Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ea200-104">This topic provides details and an example query for the Payroll fixed compensation plan entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="ea200-105">Vlastnosti</span><span class="sxs-lookup"><span data-stu-id="ea200-105">Properties</span></span>

| <span data-ttu-id="ea200-106">Vlastnost</span><span class="sxs-lookup"><span data-stu-id="ea200-106">Property</span></span><br><span data-ttu-id="ea200-107">**Fyzický název**</span><span class="sxs-lookup"><span data-stu-id="ea200-107">**Physical name**</span></span><br><span data-ttu-id="ea200-108">**_Typ_**</span><span class="sxs-lookup"><span data-stu-id="ea200-108">**_Type_**</span></span> | <span data-ttu-id="ea200-109">Použít</span><span class="sxs-lookup"><span data-stu-id="ea200-109">Use</span></span> | <span data-ttu-id="ea200-110">popis</span><span class="sxs-lookup"><span data-stu-id="ea200-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ea200-111">**ID zaměstnance**</span><span class="sxs-lookup"><span data-stu-id="ea200-111">**Employee ID**</span></span><br><span data-ttu-id="ea200-112">mshr_fk_employee_id_value</span><span class="sxs-lookup"><span data-stu-id="ea200-112">mshr_fk_employee_id_value</span></span><br><span data-ttu-id="ea200-113">*GUID*</span><span class="sxs-lookup"><span data-stu-id="ea200-113">*GUID*</span></span> | <span data-ttu-id="ea200-114">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="ea200-114">Read-only</span></span><br><span data-ttu-id="ea200-115">Povinná</span><span class="sxs-lookup"><span data-stu-id="ea200-115">Required</span></span><br><span data-ttu-id="ea200-116">Cizí klíč: mshr_Employee_id z entity mshr_payrollemployeeentity</span><span class="sxs-lookup"><span data-stu-id="ea200-116">Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity</span></span>  | <span data-ttu-id="ea200-117">ID zaměstnance</span><span class="sxs-lookup"><span data-stu-id="ea200-117">Employee ID</span></span> |
| <span data-ttu-id="ea200-118">**Mzdová sazba**</span><span class="sxs-lookup"><span data-stu-id="ea200-118">**Pay rate**</span></span><br><span data-ttu-id="ea200-119">mshr_payrate</span><span class="sxs-lookup"><span data-stu-id="ea200-119">mshr_payrate</span></span><br><span data-ttu-id="ea200-120">*Des. místo*</span><span class="sxs-lookup"><span data-stu-id="ea200-120">*Decimal*</span></span> | <span data-ttu-id="ea200-121">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="ea200-121">Read-only</span></span><br><span data-ttu-id="ea200-122">Povinná</span><span class="sxs-lookup"><span data-stu-id="ea200-122">Required</span></span> | <span data-ttu-id="ea200-123">Mzdová sazba definovaná v plánu pevné kompenzace.</span><span class="sxs-lookup"><span data-stu-id="ea200-123">Pay rate defined in fixed compensation plan.</span></span> |
| <span data-ttu-id="ea200-124">**ID plánu**</span><span class="sxs-lookup"><span data-stu-id="ea200-124">**Plan ID**</span></span><br><span data-ttu-id="ea200-125">mshr_planid</span><span class="sxs-lookup"><span data-stu-id="ea200-125">mshr_planid</span></span><br><span data-ttu-id="ea200-126">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="ea200-126">*String*</span></span> | <span data-ttu-id="ea200-127">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="ea200-127">Read-only</span></span><br><span data-ttu-id="ea200-128">Povinná</span><span class="sxs-lookup"><span data-stu-id="ea200-128">Required</span></span> |<span data-ttu-id="ea200-129">Určuje plán kompenzace.</span><span class="sxs-lookup"><span data-stu-id="ea200-129">Specifies the compensation plan.</span></span>  |
| <span data-ttu-id="ea200-130">**Platné od**</span><span class="sxs-lookup"><span data-stu-id="ea200-130">**Valid from**</span></span><br><span data-ttu-id="ea200-131">mshr_validfrom</span><span class="sxs-lookup"><span data-stu-id="ea200-131">mshr_validfrom</span></span><br><span data-ttu-id="ea200-132">*Posun data a času*</span><span class="sxs-lookup"><span data-stu-id="ea200-132">*Date Time Offset*</span></span> |  <span data-ttu-id="ea200-133">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="ea200-133">Read-only</span></span><br><span data-ttu-id="ea200-134">Povinná</span><span class="sxs-lookup"><span data-stu-id="ea200-134">Required</span></span> |<span data-ttu-id="ea200-135">Datum začátku platnosti pevné kompenzace zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="ea200-135">Date the employee fixed compensation is valid from.</span></span>  |
| <span data-ttu-id="ea200-136">**Entita mzdového plánu fixní kompenzace**</span><span class="sxs-lookup"><span data-stu-id="ea200-136">**Payroll Fixed Compensation Plan entity**</span></span><br><span data-ttu-id="ea200-137">mshr_payrollfixedcompensationplanentityid</span><span class="sxs-lookup"><span data-stu-id="ea200-137">mshr_payrollfixedcompensationplanentityid</span></span><br><span data-ttu-id="ea200-138">*GUID*</span><span class="sxs-lookup"><span data-stu-id="ea200-138">*GUID*</span></span> | <span data-ttu-id="ea200-139">Povinná</span><span class="sxs-lookup"><span data-stu-id="ea200-139">Required</span></span><br><span data-ttu-id="ea200-140">Generováno systémem</span><span class="sxs-lookup"><span data-stu-id="ea200-140">Sytem generated</span></span> | <span data-ttu-id="ea200-141">Systémem generovaná hodnota GUID pro jedinečnou identifikaci plánu kompenzace.</span><span class="sxs-lookup"><span data-stu-id="ea200-141">A system-generated GUID value to uniquely identify the compensation plan.</span></span> |
| <span data-ttu-id="ea200-142">**Interval plateb**</span><span class="sxs-lookup"><span data-stu-id="ea200-142">**Pay frequency**</span></span><br><span data-ttu-id="ea200-143">mshr_payfrequency</span><span class="sxs-lookup"><span data-stu-id="ea200-143">mshr_payfrequency</span></span><br><span data-ttu-id="ea200-144">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="ea200-144">*String*</span></span> | <span data-ttu-id="ea200-145">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="ea200-145">Read-only</span></span><br><span data-ttu-id="ea200-146">Povinná</span><span class="sxs-lookup"><span data-stu-id="ea200-146">Required</span></span> |<span data-ttu-id="ea200-147">Četnost, kdy bude zaměstnanec placen.</span><span class="sxs-lookup"><span data-stu-id="ea200-147">The frequency the employee will be paid.</span></span>  |
| <span data-ttu-id="ea200-148">**Platné do**</span><span class="sxs-lookup"><span data-stu-id="ea200-148">**Valid to**</span></span><br><span data-ttu-id="ea200-149">mshr_validto</span><span class="sxs-lookup"><span data-stu-id="ea200-149">mshr_validto</span></span><br><span data-ttu-id="ea200-150">*Posun data a času*</span><span class="sxs-lookup"><span data-stu-id="ea200-150">*Date Time Offset*</span></span> | <span data-ttu-id="ea200-151">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="ea200-151">Read-only</span></span> <br><span data-ttu-id="ea200-152">Povinná</span><span class="sxs-lookup"><span data-stu-id="ea200-152">Required</span></span> | <span data-ttu-id="ea200-153">Datum konce platnosti pevné kompenzace zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="ea200-153">Date the employee fixed compensation is valid to.</span></span> |
| <span data-ttu-id="ea200-154">**ID pozice**</span><span class="sxs-lookup"><span data-stu-id="ea200-154">**Position ID**</span></span><br><span data-ttu-id="ea200-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="ea200-155">mshr_positionid</span></span><br><span data-ttu-id="ea200-156">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="ea200-156">*String*</span></span> | <span data-ttu-id="ea200-157">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="ea200-157">Read-only</span></span> <br><span data-ttu-id="ea200-158">Povinná</span><span class="sxs-lookup"><span data-stu-id="ea200-158">Required</span></span> | <span data-ttu-id="ea200-159">ID pozice spojené s registrací zaměstnance a plánu pevné kompenzace.</span><span class="sxs-lookup"><span data-stu-id="ea200-159">Postion ID associated with the employee and fixed compensation plan enrollment.</span></span> |
| <span data-ttu-id="ea200-160">**Měna**</span><span class="sxs-lookup"><span data-stu-id="ea200-160">**Currency**</span></span><br><span data-ttu-id="ea200-161">mshr_currency</span><span class="sxs-lookup"><span data-stu-id="ea200-161">mshr_currency</span></span><br><span data-ttu-id="ea200-162">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="ea200-162">*String*</span></span> | <span data-ttu-id="ea200-163">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="ea200-163">Read-only</span></span> <br><span data-ttu-id="ea200-164">Povinná</span><span class="sxs-lookup"><span data-stu-id="ea200-164">Required</span></span> |<span data-ttu-id="ea200-165">Měna definovaná pro plán pevné kompenzace</span><span class="sxs-lookup"><span data-stu-id="ea200-165">The currency defined for the fixed compensation plan</span></span>   |
| <span data-ttu-id="ea200-166">**Číslo pracovníka**</span><span class="sxs-lookup"><span data-stu-id="ea200-166">**Personnel number**</span></span><br><span data-ttu-id="ea200-167">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="ea200-167">mshr_personnelnumber</span></span><br><span data-ttu-id="ea200-168">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="ea200-168">*String*</span></span> | <span data-ttu-id="ea200-169">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="ea200-169">Read-only</span></span><br><span data-ttu-id="ea200-170">Povinná</span><span class="sxs-lookup"><span data-stu-id="ea200-170">Required</span></span> |<span data-ttu-id="ea200-171">Jedinečné osobní číslo zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="ea200-171">The employee's unique personnel number.</span></span>  |

<span data-ttu-id="ea200-172">**Dotaz**</span><span class="sxs-lookup"><span data-stu-id="ea200-172">**Query**</span></span>

<span data-ttu-id="ea200-173">**Žádost**</span><span class="sxs-lookup"><span data-stu-id="ea200-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="ea200-174">**Odezva**</span><span class="sxs-lookup"><span data-stu-id="ea200-174">**Response**</span></span>

```json
{
            "mshr_planid": "GradeC",
            "mshr_personnelnumber": "000041",
            "mshr_payrate": 75200,
            "mshr_positionid": "000276",
            "mshr_validfrom": "2011-04-05T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_payfrequency": "Annual",
            "mshr_currency": "USD",
            "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
            "_mshr_fk_payroll_id_value": null
}
```
