---
title: Typy prověřování
description: Toto téma popisuje entitu typy prověřování pro Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 227c15acb44e020ea9858961e45c11ad07e18a74
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126163"
---
# <a name="screening-types"></a><span data-ttu-id="c594e-103">Typy prověřování</span><span class="sxs-lookup"><span data-stu-id="c594e-103">Screening types</span></span>

<span data-ttu-id="c594e-104">Toto téma popisuje entitu typy prověřování pro Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c594e-104">This topic describes the Screening types entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="c594e-105">Fyzický název: mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="c594e-105">Physical name: mshr_hcmscreeningtypeentity</span></span>

## <a name="description"></a><span data-ttu-id="c594e-106">popis</span><span class="sxs-lookup"><span data-stu-id="c594e-106">Description</span></span>

<span data-ttu-id="c594e-107">Tato entita popisuje typy prověřování nastavené společností pro procesy před zaměstnáním a probíhající prověřování zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="c594e-107">This entity describes the screening types set up by the company for pre-employment and ongoing employee screening processes.</span></span>

## <a name="json-representation"></a><span data-ttu-id="c594e-108">JSON reprezentace</span><span class="sxs-lookup"><span data-stu-id="c594e-108">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="c594e-109">Vlastnosti</span><span class="sxs-lookup"><span data-stu-id="c594e-109">Properties</span></span>

| <span data-ttu-id="c594e-110">Vlastnost</span><span class="sxs-lookup"><span data-stu-id="c594e-110">Property</span></span><br><span data-ttu-id="c594e-111">**Fyzický název**</span><span class="sxs-lookup"><span data-stu-id="c594e-111">**Physical name**</span></span><br><span data-ttu-id="c594e-112">**_Typ_**</span><span class="sxs-lookup"><span data-stu-id="c594e-112">**_Type_**</span></span> | <span data-ttu-id="c594e-113">Použít</span><span class="sxs-lookup"><span data-stu-id="c594e-113">Use</span></span> | <span data-ttu-id="c594e-114">popis</span><span class="sxs-lookup"><span data-stu-id="c594e-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="c594e-115">**ID entity typu prověřování**</span><span class="sxs-lookup"><span data-stu-id="c594e-115">**Screening Type Entity ID**</span></span><br><span data-ttu-id="c594e-116">mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="c594e-116">mshr_hcmscreeningtypeentityid</span></span><br><span data-ttu-id="c594e-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="c594e-117">*GUID*</span></span> | <span data-ttu-id="c594e-118">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="c594e-118">Read-only</span></span><br><span data-ttu-id="c594e-119">Povinná</span><span class="sxs-lookup"><span data-stu-id="c594e-119">Required</span></span><br><span data-ttu-id="c594e-120">Generováno systémem</span><span class="sxs-lookup"><span data-stu-id="c594e-120">System-generated</span></span> | <span data-ttu-id="c594e-121">Jedinečný primární identifikátor pro záznam typu prověřování.</span><span class="sxs-lookup"><span data-stu-id="c594e-121">Unique primary identifier for the screening type record.</span></span> |
| <span data-ttu-id="c594e-122">**ID typu prověřování**</span><span class="sxs-lookup"><span data-stu-id="c594e-122">**Screening Type ID**</span></span><br><span data-ttu-id="c594e-123">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="c594e-123">mshr_screeningtypeid</span></span><br><span data-ttu-id="c594e-124">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="c594e-124">*String*</span></span> | <span data-ttu-id="c594e-125">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="c594e-125">Read/write</span></span><br><span data-ttu-id="c594e-126">Povinná</span><span class="sxs-lookup"><span data-stu-id="c594e-126">Required</span></span> | <span data-ttu-id="c594e-127">Uživatelem určený jedinečný identifikátor pro typ prověřování.</span><span class="sxs-lookup"><span data-stu-id="c594e-127">User-defined unique identifier for the screening type.</span></span> |
| <span data-ttu-id="c594e-128">**Popis**</span><span class="sxs-lookup"><span data-stu-id="c594e-128">**Description**</span></span><br><span data-ttu-id="c594e-129">mshr_description</span><span class="sxs-lookup"><span data-stu-id="c594e-129">mshr_description</span></span><br><span data-ttu-id="c594e-130">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="c594e-130">*String*</span></span> | <span data-ttu-id="c594e-131">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="c594e-131">Read/write</span></span><br><span data-ttu-id="c594e-132">Povinná</span><span class="sxs-lookup"><span data-stu-id="c594e-132">Required</span></span> | <span data-ttu-id="c594e-133">Popis typu prověřování.</span><span class="sxs-lookup"><span data-stu-id="c594e-133">The description of the screening type.</span></span> |
| <span data-ttu-id="c594e-134">**Jednotka četnosti**</span><span class="sxs-lookup"><span data-stu-id="c594e-134">**Frequency Unit**</span></span><br><span data-ttu-id="c594e-135">mshr_frequencyunit</span><span class="sxs-lookup"><span data-stu-id="c594e-135">mshr_frequencyunit</span></span><br><span data-ttu-id="c594e-136">*nastavená možnost mshr_hcmfrequencyunit*</span><span class="sxs-lookup"><span data-stu-id="c594e-136">*mshr_hcmfrequencyunit option set*</span></span> | <span data-ttu-id="c594e-137">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="c594e-137">Read/write</span></span><br><span data-ttu-id="c594e-138">Povinná</span><span class="sxs-lookup"><span data-stu-id="c594e-138">Required</span></span> | <span data-ttu-id="c594e-139">Popisuje frekvenci, s jakou musí být u přiřazené osoby provedeno prověření.</span><span class="sxs-lookup"><span data-stu-id="c594e-139">Describes the frequency with which the screening must be completed for the assigned person.</span></span> |
| <span data-ttu-id="c594e-140">**Generovat z**</span><span class="sxs-lookup"><span data-stu-id="c594e-140">**Generate From**</span></span><br><span data-ttu-id="c594e-141">mshr_generatefrom</span><span class="sxs-lookup"><span data-stu-id="c594e-141">mshr_generatefrom</span></span><br><span data-ttu-id="c594e-142">*nastavená možnost mshr_hcmfrequencygeneratefrom*</span><span class="sxs-lookup"><span data-stu-id="c594e-142">*mshr_hcmfrequencygeneratefrom option set*</span></span> | <span data-ttu-id="c594e-143">Čtení-zápis</span><span class="sxs-lookup"><span data-stu-id="c594e-143">Read-write</span></span><br><span data-ttu-id="c594e-144">Povinná</span><span class="sxs-lookup"><span data-stu-id="c594e-144">Required</span></span> | <span data-ttu-id="c594e-145">Pokud je hodnota četnosti jakákoli jiná hodnota než „Pouze jednorázově“, určuje hodnota GenerateFrom datum, od kterého se má vypočítat další prověřovací událost.</span><span class="sxs-lookup"><span data-stu-id="c594e-145">If the Frequency value is any value other than “One-time only”, the GenerateFrom value determines the date from which to calculate the next screening event.</span></span> |
| <span data-ttu-id="c594e-146">**Interval četnosti**</span><span class="sxs-lookup"><span data-stu-id="c594e-146">**Frequency Interval**</span></span><br><span data-ttu-id="c594e-147">mshr_frequencyinterval</span><span class="sxs-lookup"><span data-stu-id="c594e-147">mshr_frequencyinterval</span></span><br><span data-ttu-id="c594e-148">*Celé číslo*</span><span class="sxs-lookup"><span data-stu-id="c594e-148">*Integer*</span></span> | <span data-ttu-id="c594e-149">Čtení-zápis</span><span class="sxs-lookup"><span data-stu-id="c594e-149">Read-write</span></span><br><span data-ttu-id="c594e-150">Povinná</span><span class="sxs-lookup"><span data-stu-id="c594e-150">Required</span></span> | <span data-ttu-id="c594e-151">Pokud je hodnota četnosti jiná než „Pouze jednorázově“, musíte definovat interval pro jednotky času mezi každou prověřovací událostí.</span><span class="sxs-lookup"><span data-stu-id="c594e-151">If the Frequency value is any value other than “One-time only”, you must define an interval for the units of time between each screening event.</span></span> |

## <a name="see-also"></a><span data-ttu-id="c594e-152">Viz také</span><span class="sxs-lookup"><span data-stu-id="c594e-152">See also</span></span>

[<span data-ttu-id="c594e-153">Úvod do rozhraní API pro integraci systému sledování žadatelů</span><span class="sxs-lookup"><span data-stu-id="c594e-153">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="c594e-154">Příklad dotazu pro entitu Kandidát k přijetí</span><span class="sxs-lookup"><span data-stu-id="c594e-154">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
