---
title: Typy prověřování
description: Toto téma popisuje entitu typy prověřování pro Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 361f8c866abb9d34eb3e2be7ea42626e98e34779
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805123"
---
# <a name="screening-types"></a><span data-ttu-id="081ae-103">Typy prověřování</span><span class="sxs-lookup"><span data-stu-id="081ae-103">Screening types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="081ae-104">Toto téma popisuje entitu typy prověřování pro Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="081ae-104">This topic describes the Screening types entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="081ae-105">Fyzický název: mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="081ae-105">Physical name: mshr_hcmscreeningtypeentity</span></span>

## <a name="description"></a><span data-ttu-id="081ae-106">popis</span><span class="sxs-lookup"><span data-stu-id="081ae-106">Description</span></span>

<span data-ttu-id="081ae-107">Tato entita popisuje typy prověřování nastavené společností pro procesy před zaměstnáním a probíhající prověřování zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="081ae-107">This entity describes the screening types set up by the company for pre-employment and ongoing employee screening processes.</span></span>

## <a name="json-representation"></a><span data-ttu-id="081ae-108">JSON reprezentace</span><span class="sxs-lookup"><span data-stu-id="081ae-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="081ae-109">Vlastnosti</span><span class="sxs-lookup"><span data-stu-id="081ae-109">Properties</span></span>

| <span data-ttu-id="081ae-110">Vlastnost</span><span class="sxs-lookup"><span data-stu-id="081ae-110">Property</span></span><br><span data-ttu-id="081ae-111">**Fyzický název**</span><span class="sxs-lookup"><span data-stu-id="081ae-111">**Physical name**</span></span><br><span data-ttu-id="081ae-112">**_Typ_**</span><span class="sxs-lookup"><span data-stu-id="081ae-112">**_Type_**</span></span> | <span data-ttu-id="081ae-113">Použít</span><span class="sxs-lookup"><span data-stu-id="081ae-113">Use</span></span> | <span data-ttu-id="081ae-114">popis</span><span class="sxs-lookup"><span data-stu-id="081ae-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="081ae-115">**ID entity typu prověřování**</span><span class="sxs-lookup"><span data-stu-id="081ae-115">**Screening Type Entity ID**</span></span><br><span data-ttu-id="081ae-116">mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="081ae-116">mshr_hcmscreeningtypeentityid</span></span><br><span data-ttu-id="081ae-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="081ae-117">*GUID*</span></span> | <span data-ttu-id="081ae-118">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="081ae-118">Read-only</span></span><br><span data-ttu-id="081ae-119">Povinná</span><span class="sxs-lookup"><span data-stu-id="081ae-119">Required</span></span><br><span data-ttu-id="081ae-120">Generováno systémem</span><span class="sxs-lookup"><span data-stu-id="081ae-120">System-generated</span></span> | <span data-ttu-id="081ae-121">Jedinečný primární identifikátor pro záznam typu prověřování.</span><span class="sxs-lookup"><span data-stu-id="081ae-121">Unique primary identifier for the screening type record.</span></span> |
| <span data-ttu-id="081ae-122">**ID typu prověřování**</span><span class="sxs-lookup"><span data-stu-id="081ae-122">**Screening Type ID**</span></span><br><span data-ttu-id="081ae-123">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="081ae-123">mshr_screeningtypeid</span></span><br><span data-ttu-id="081ae-124">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="081ae-124">*String*</span></span> | <span data-ttu-id="081ae-125">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="081ae-125">Read/write</span></span><br><span data-ttu-id="081ae-126">Povinná</span><span class="sxs-lookup"><span data-stu-id="081ae-126">Required</span></span> | <span data-ttu-id="081ae-127">Uživatelem určený jedinečný identifikátor pro typ prověřování.</span><span class="sxs-lookup"><span data-stu-id="081ae-127">User-defined unique identifier for the screening type.</span></span> |
| <span data-ttu-id="081ae-128">**Popis**</span><span class="sxs-lookup"><span data-stu-id="081ae-128">**Description**</span></span><br><span data-ttu-id="081ae-129">mshr_description</span><span class="sxs-lookup"><span data-stu-id="081ae-129">mshr_description</span></span><br><span data-ttu-id="081ae-130">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="081ae-130">*String*</span></span> | <span data-ttu-id="081ae-131">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="081ae-131">Read/write</span></span><br><span data-ttu-id="081ae-132">Povinná</span><span class="sxs-lookup"><span data-stu-id="081ae-132">Required</span></span> | <span data-ttu-id="081ae-133">Popis typu prověřování.</span><span class="sxs-lookup"><span data-stu-id="081ae-133">The description of the screening type.</span></span> |
| <span data-ttu-id="081ae-134">**Jednotka četnosti**</span><span class="sxs-lookup"><span data-stu-id="081ae-134">**Frequency Unit**</span></span><br><span data-ttu-id="081ae-135">mshr_frequencyunit</span><span class="sxs-lookup"><span data-stu-id="081ae-135">mshr_frequencyunit</span></span><br><span data-ttu-id="081ae-136">*nastavená možnost mshr_hcmfrequencyunit*</span><span class="sxs-lookup"><span data-stu-id="081ae-136">*mshr_hcmfrequencyunit option set*</span></span> | <span data-ttu-id="081ae-137">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="081ae-137">Read/write</span></span><br><span data-ttu-id="081ae-138">Povinná</span><span class="sxs-lookup"><span data-stu-id="081ae-138">Required</span></span> | <span data-ttu-id="081ae-139">Popisuje frekvenci, s jakou musí být u přiřazené osoby provedeno prověření.</span><span class="sxs-lookup"><span data-stu-id="081ae-139">Describes the frequency with which the screening must be completed for the assigned person.</span></span> |
| <span data-ttu-id="081ae-140">**Generovat z**</span><span class="sxs-lookup"><span data-stu-id="081ae-140">**Generate From**</span></span><br><span data-ttu-id="081ae-141">mshr_generatefrom</span><span class="sxs-lookup"><span data-stu-id="081ae-141">mshr_generatefrom</span></span><br><span data-ttu-id="081ae-142">*nastavená možnost mshr_hcmfrequencygeneratefrom*</span><span class="sxs-lookup"><span data-stu-id="081ae-142">*mshr_hcmfrequencygeneratefrom option set*</span></span> | <span data-ttu-id="081ae-143">Čtení-zápis</span><span class="sxs-lookup"><span data-stu-id="081ae-143">Read-write</span></span><br><span data-ttu-id="081ae-144">Povinná</span><span class="sxs-lookup"><span data-stu-id="081ae-144">Required</span></span> | <span data-ttu-id="081ae-145">Pokud je hodnota četnosti jakákoli jiná hodnota než „Pouze jednorázově“, určuje hodnota GenerateFrom datum, od kterého se má vypočítat další prověřovací událost.</span><span class="sxs-lookup"><span data-stu-id="081ae-145">If the Frequency value is any value other than “One-time only”, the GenerateFrom value determines the date from which to calculate the next screening event.</span></span> |
| <span data-ttu-id="081ae-146">**Interval četnosti**</span><span class="sxs-lookup"><span data-stu-id="081ae-146">**Frequency Interval**</span></span><br><span data-ttu-id="081ae-147">mshr_frequencyinterval</span><span class="sxs-lookup"><span data-stu-id="081ae-147">mshr_frequencyinterval</span></span><br><span data-ttu-id="081ae-148">*Celé číslo*</span><span class="sxs-lookup"><span data-stu-id="081ae-148">*Integer*</span></span> | <span data-ttu-id="081ae-149">Čtení-zápis</span><span class="sxs-lookup"><span data-stu-id="081ae-149">Read-write</span></span><br><span data-ttu-id="081ae-150">Povinná</span><span class="sxs-lookup"><span data-stu-id="081ae-150">Required</span></span> | <span data-ttu-id="081ae-151">Pokud je hodnota četnosti jiná než „Pouze jednorázově“, musíte definovat interval pro jednotky času mezi každou prověřovací událostí.</span><span class="sxs-lookup"><span data-stu-id="081ae-151">If the Frequency value is any value other than “One-time only”, you must define an interval for the units of time between each screening event.</span></span> |

## <a name="see-also"></a><span data-ttu-id="081ae-152">Viz také</span><span class="sxs-lookup"><span data-stu-id="081ae-152">See also</span></span>

[<span data-ttu-id="081ae-153">Úvod do rozhraní API pro integraci systému sledování žadatelů</span><span class="sxs-lookup"><span data-stu-id="081ae-153">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="081ae-154">Příklad dotazu pro entitu Kandidát k přijetí</span><span class="sxs-lookup"><span data-stu-id="081ae-154">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]