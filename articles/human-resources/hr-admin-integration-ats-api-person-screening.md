---
title: Prověřování osoby
description: Toto téma popisuje entitu Prověřování osoby pro Dynamics 365 Human Resources.
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
ms.openlocfilehash: d76bb57d85ee16f4faa0bb9cfec77047feb7df5f
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125370"
---
# <a name="person-screening"></a><span data-ttu-id="748a4-103">Prověřování osoby</span><span class="sxs-lookup"><span data-stu-id="748a4-103">Person screening</span></span>

<span data-ttu-id="748a4-104">Toto téma popisuje entitu Prověřování osoby pro Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="748a4-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="748a4-105">Fyzický název: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="748a4-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="748a4-106">popis</span><span class="sxs-lookup"><span data-stu-id="748a4-106">Description</span></span>

<span data-ttu-id="748a4-107">Tato entita popisuje prověřování, která kandidát úspěšně absolvoval nebo musí absolvovat kvůli zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="748a4-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="748a4-108">Kód JSON</span><span class="sxs-lookup"><span data-stu-id="748a4-108">JSON representation</span></span>

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a><span data-ttu-id="748a4-109">Vlastnosti</span><span class="sxs-lookup"><span data-stu-id="748a4-109">Properties</span></span>

| <span data-ttu-id="748a4-110">Vlastnost</span><span class="sxs-lookup"><span data-stu-id="748a4-110">Property</span></span><br><span data-ttu-id="748a4-111">**Fyzický název**</span><span class="sxs-lookup"><span data-stu-id="748a4-111">**Physical name**</span></span><br><span data-ttu-id="748a4-112">**_Typ_**</span><span class="sxs-lookup"><span data-stu-id="748a4-112">**_Type_**</span></span> | <span data-ttu-id="748a4-113">Použít</span><span class="sxs-lookup"><span data-stu-id="748a4-113">Use</span></span> | <span data-ttu-id="748a4-114">popis</span><span class="sxs-lookup"><span data-stu-id="748a4-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="748a4-115">**ID entity Prověřování osoby**</span><span class="sxs-lookup"><span data-stu-id="748a4-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="748a4-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="748a4-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="748a4-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="748a4-117">*GUID*</span></span> | <span data-ttu-id="748a4-118">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="748a4-118">Read-only</span></span><br><span data-ttu-id="748a4-119">Povinná</span><span class="sxs-lookup"><span data-stu-id="748a4-119">Required</span></span><br><span data-ttu-id="748a4-120">Generováno systémem</span><span class="sxs-lookup"><span data-stu-id="748a4-120">System-generated</span></span> | <span data-ttu-id="748a4-121">Jedinečný primární identifikátor pro záznam prověřování osoby.</span><span class="sxs-lookup"><span data-stu-id="748a4-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="748a4-122">**Číslo strany**</span><span class="sxs-lookup"><span data-stu-id="748a4-122">**Party Number**</span></span><br><span data-ttu-id="748a4-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="748a4-123">mshr_partynumber</span></span><br><span data-ttu-id="748a4-124">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="748a4-124">*String*</span></span> | <span data-ttu-id="748a4-125">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="748a4-125">Read/write</span></span><br><span data-ttu-id="748a4-126">Povinná</span><span class="sxs-lookup"><span data-stu-id="748a4-126">Required</span></span> | <span data-ttu-id="748a4-127">Číslo strany (osoby) přidružené ke kandidátovi.</span><span class="sxs-lookup"><span data-stu-id="748a4-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="748a4-128">**Hodnota ID osoby**</span><span class="sxs-lookup"><span data-stu-id="748a4-128">**Person ID Value**</span></span><br><span data-ttu-id="748a4-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="748a4-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="748a4-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="748a4-130">*GUID*</span></span> | <span data-ttu-id="748a4-131">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="748a4-131">Read-only</span></span><br><span data-ttu-id="748a4-132">Povinná</span><span class="sxs-lookup"><span data-stu-id="748a4-132">Required</span></span><br><span data-ttu-id="748a4-133">Cizí klíč: mshr_dirpersonentityid entity mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="748a4-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="748a4-134">Systémem generovaný jedinečný identifikátor záznamu entity strany (osoby).</span><span class="sxs-lookup"><span data-stu-id="748a4-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="748a4-135">**ID typu prověřování**</span><span class="sxs-lookup"><span data-stu-id="748a4-135">**Screening Type ID**</span></span><br><span data-ttu-id="748a4-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="748a4-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="748a4-137">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="748a4-137">*String*</span></span> | <span data-ttu-id="748a4-138">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="748a4-138">Read/write</span></span><br><span data-ttu-id="748a4-139">Povinná</span><span class="sxs-lookup"><span data-stu-id="748a4-139">Required</span></span><br><span data-ttu-id="748a4-140">Cizí klíč: ScreeningType</span><span class="sxs-lookup"><span data-stu-id="748a4-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="748a4-141">Identifikátor typu prověřování definovaného v Human Resources.</span><span class="sxs-lookup"><span data-stu-id="748a4-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="748a4-142">**Hodnota ID typu prověřování**</span><span class="sxs-lookup"><span data-stu-id="748a4-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="748a4-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="748a4-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="748a4-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="748a4-144">*GUID*</span></span> | <span data-ttu-id="748a4-145">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="748a4-145">Read-only</span></span><br><span data-ttu-id="748a4-146">Povinná</span><span class="sxs-lookup"><span data-stu-id="748a4-146">Required</span></span><br><span data-ttu-id="748a4-147">Cizí klíč: mshr_hcmscreeningtypeentityid entity mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="748a4-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="748a4-148">Systémem generovaný identifikátor záznamu typu prověřování přidružené entity.</span><span class="sxs-lookup"><span data-stu-id="748a4-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="748a4-149">**Požadováno do**</span><span class="sxs-lookup"><span data-stu-id="748a4-149">**Required By**</span></span><br><span data-ttu-id="748a4-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="748a4-150">mshr_requiredby</span></span><br><span data-ttu-id="748a4-151">*Datum a čas*</span><span class="sxs-lookup"><span data-stu-id="748a4-151">*Datetime*</span></span> | <span data-ttu-id="748a4-152">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="748a4-152">Read/write</span></span><br><span data-ttu-id="748a4-153">Volitelné</span><span class="sxs-lookup"><span data-stu-id="748a4-153">Optional</span></span> | <span data-ttu-id="748a4-154">Datum, do kterého je nutné provést prověřování.</span><span class="sxs-lookup"><span data-stu-id="748a4-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="748a4-155">**Stav**</span><span class="sxs-lookup"><span data-stu-id="748a4-155">**Status**</span></span><br><span data-ttu-id="748a4-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="748a4-156">mshr_status</span></span><br><span data-ttu-id="748a4-157">*Sada možností mshr_hcmcompletionstatus*</span><span class="sxs-lookup"><span data-stu-id="748a4-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="748a4-158">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="748a4-158">Read/write</span></span><br><span data-ttu-id="748a4-159">Povinná</span><span class="sxs-lookup"><span data-stu-id="748a4-159">Required</span></span> | <span data-ttu-id="748a4-160">Poskytuje stav kandidáta pro prověřování.</span><span class="sxs-lookup"><span data-stu-id="748a4-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="748a4-161">**Datum dokončení**</span><span class="sxs-lookup"><span data-stu-id="748a4-161">**Completed Date**</span></span><br><span data-ttu-id="748a4-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="748a4-162">mshr_completeddate</span></span><br><span data-ttu-id="748a4-163">*Datum a čas*</span><span class="sxs-lookup"><span data-stu-id="748a4-163">*Datetime*</span></span> | <span data-ttu-id="748a4-164">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="748a4-164">Read/write</span></span><br><span data-ttu-id="748a4-165">Volitelné</span><span class="sxs-lookup"><span data-stu-id="748a4-165">Optional</span></span> | <span data-ttu-id="748a4-166">Datum dokončení prověřování.</span><span class="sxs-lookup"><span data-stu-id="748a4-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="748a4-167">**Poznámky**</span><span class="sxs-lookup"><span data-stu-id="748a4-167">**Notes**</span></span><br><span data-ttu-id="748a4-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="748a4-168">mshr_note</span></span><br><span data-ttu-id="748a4-169">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="748a4-169">*String*</span></span> | <span data-ttu-id="748a4-170">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="748a4-170">Read/write</span></span><br><span data-ttu-id="748a4-171">Volitelné</span><span class="sxs-lookup"><span data-stu-id="748a4-171">Optional</span></span> | <span data-ttu-id="748a4-172">Poznámky určené pro manažery náboru a náboráře.</span><span class="sxs-lookup"><span data-stu-id="748a4-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="748a4-173">Viz také</span><span class="sxs-lookup"><span data-stu-id="748a4-173">See also</span></span>

[<span data-ttu-id="748a4-174">Úvod do rozhraní API pro integraci systému sledování žadatelů</span><span class="sxs-lookup"><span data-stu-id="748a4-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="748a4-175">Příklad dotazu pro entitu Kandidát k přijetí</span><span class="sxs-lookup"><span data-stu-id="748a4-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

