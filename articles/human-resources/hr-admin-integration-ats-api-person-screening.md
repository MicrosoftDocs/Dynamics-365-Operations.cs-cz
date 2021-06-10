---
title: Prověřování osoby
description: Toto téma popisuje entitu Prověřování osoby pro Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9d29b26094e307c3f68d57f297ab3614f3a5ccae
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059273"
---
# <a name="person-screening"></a><span data-ttu-id="bcecb-103">Prověřování osoby</span><span class="sxs-lookup"><span data-stu-id="bcecb-103">Person screening</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="bcecb-104">Toto téma popisuje entitu Prověřování osoby pro Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="bcecb-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="bcecb-105">Fyzický název: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="bcecb-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="bcecb-106">popis</span><span class="sxs-lookup"><span data-stu-id="bcecb-106">Description</span></span>

<span data-ttu-id="bcecb-107">Tato entita popisuje prověřování, která kandidát úspěšně absolvoval nebo musí absolvovat kvůli zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="bcecb-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="bcecb-108">Kód JSON</span><span class="sxs-lookup"><span data-stu-id="bcecb-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="bcecb-109">Vlastnosti</span><span class="sxs-lookup"><span data-stu-id="bcecb-109">Properties</span></span>

| <span data-ttu-id="bcecb-110">Vlastnost</span><span class="sxs-lookup"><span data-stu-id="bcecb-110">Property</span></span><br><span data-ttu-id="bcecb-111">**Fyzický název**</span><span class="sxs-lookup"><span data-stu-id="bcecb-111">**Physical name**</span></span><br><span data-ttu-id="bcecb-112">**_Typ_**</span><span class="sxs-lookup"><span data-stu-id="bcecb-112">**_Type_**</span></span> | <span data-ttu-id="bcecb-113">Použít</span><span class="sxs-lookup"><span data-stu-id="bcecb-113">Use</span></span> | <span data-ttu-id="bcecb-114">popis</span><span class="sxs-lookup"><span data-stu-id="bcecb-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="bcecb-115">**ID entity Prověřování osoby**</span><span class="sxs-lookup"><span data-stu-id="bcecb-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="bcecb-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="bcecb-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="bcecb-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="bcecb-117">*GUID*</span></span> | <span data-ttu-id="bcecb-118">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="bcecb-118">Read-only</span></span><br><span data-ttu-id="bcecb-119">Povinná</span><span class="sxs-lookup"><span data-stu-id="bcecb-119">Required</span></span><br><span data-ttu-id="bcecb-120">Generováno systémem</span><span class="sxs-lookup"><span data-stu-id="bcecb-120">System-generated</span></span> | <span data-ttu-id="bcecb-121">Jedinečný primární identifikátor pro záznam prověřování osoby.</span><span class="sxs-lookup"><span data-stu-id="bcecb-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="bcecb-122">**Číslo strany**</span><span class="sxs-lookup"><span data-stu-id="bcecb-122">**Party Number**</span></span><br><span data-ttu-id="bcecb-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="bcecb-123">mshr_partynumber</span></span><br><span data-ttu-id="bcecb-124">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="bcecb-124">*String*</span></span> | <span data-ttu-id="bcecb-125">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="bcecb-125">Read/write</span></span><br><span data-ttu-id="bcecb-126">Povinná</span><span class="sxs-lookup"><span data-stu-id="bcecb-126">Required</span></span> | <span data-ttu-id="bcecb-127">Číslo strany (osoby) přidružené ke kandidátovi.</span><span class="sxs-lookup"><span data-stu-id="bcecb-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="bcecb-128">**Hodnota ID osoby**</span><span class="sxs-lookup"><span data-stu-id="bcecb-128">**Person ID Value**</span></span><br><span data-ttu-id="bcecb-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="bcecb-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="bcecb-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="bcecb-130">*GUID*</span></span> | <span data-ttu-id="bcecb-131">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="bcecb-131">Read-only</span></span><br><span data-ttu-id="bcecb-132">Povinná</span><span class="sxs-lookup"><span data-stu-id="bcecb-132">Required</span></span><br><span data-ttu-id="bcecb-133">Cizí klíč: mshr_dirpersonentityid entity mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="bcecb-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="bcecb-134">Systémem generovaný jedinečný identifikátor záznamu entity strany (osoby).</span><span class="sxs-lookup"><span data-stu-id="bcecb-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="bcecb-135">**ID typu prověřování**</span><span class="sxs-lookup"><span data-stu-id="bcecb-135">**Screening Type ID**</span></span><br><span data-ttu-id="bcecb-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="bcecb-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="bcecb-137">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="bcecb-137">*String*</span></span> | <span data-ttu-id="bcecb-138">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="bcecb-138">Read/write</span></span><br><span data-ttu-id="bcecb-139">Povinná</span><span class="sxs-lookup"><span data-stu-id="bcecb-139">Required</span></span><br><span data-ttu-id="bcecb-140">Cizí klíč: ScreeningType</span><span class="sxs-lookup"><span data-stu-id="bcecb-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="bcecb-141">Identifikátor typu prověřování definovaného v Human Resources.</span><span class="sxs-lookup"><span data-stu-id="bcecb-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="bcecb-142">**Hodnota ID typu prověřování**</span><span class="sxs-lookup"><span data-stu-id="bcecb-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="bcecb-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="bcecb-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="bcecb-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="bcecb-144">*GUID*</span></span> | <span data-ttu-id="bcecb-145">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="bcecb-145">Read-only</span></span><br><span data-ttu-id="bcecb-146">Povinná</span><span class="sxs-lookup"><span data-stu-id="bcecb-146">Required</span></span><br><span data-ttu-id="bcecb-147">Cizí klíč: mshr_hcmscreeningtypeentityid entity mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="bcecb-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="bcecb-148">Systémem generovaný identifikátor záznamu typu prověřování přidružené entity.</span><span class="sxs-lookup"><span data-stu-id="bcecb-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="bcecb-149">**Požadováno do**</span><span class="sxs-lookup"><span data-stu-id="bcecb-149">**Required By**</span></span><br><span data-ttu-id="bcecb-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="bcecb-150">mshr_requiredby</span></span><br><span data-ttu-id="bcecb-151">*Datum a čas*</span><span class="sxs-lookup"><span data-stu-id="bcecb-151">*Datetime*</span></span> | <span data-ttu-id="bcecb-152">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="bcecb-152">Read/write</span></span><br><span data-ttu-id="bcecb-153">Volitelné</span><span class="sxs-lookup"><span data-stu-id="bcecb-153">Optional</span></span> | <span data-ttu-id="bcecb-154">Datum, do kterého je nutné provést prověřování.</span><span class="sxs-lookup"><span data-stu-id="bcecb-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="bcecb-155">**Stav**</span><span class="sxs-lookup"><span data-stu-id="bcecb-155">**Status**</span></span><br><span data-ttu-id="bcecb-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="bcecb-156">mshr_status</span></span><br><span data-ttu-id="bcecb-157">*Sada možností mshr_hcmcompletionstatus*</span><span class="sxs-lookup"><span data-stu-id="bcecb-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="bcecb-158">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="bcecb-158">Read/write</span></span><br><span data-ttu-id="bcecb-159">Povinná</span><span class="sxs-lookup"><span data-stu-id="bcecb-159">Required</span></span> | <span data-ttu-id="bcecb-160">Poskytuje stav kandidáta pro prověřování.</span><span class="sxs-lookup"><span data-stu-id="bcecb-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="bcecb-161">**Datum dokončení**</span><span class="sxs-lookup"><span data-stu-id="bcecb-161">**Completed Date**</span></span><br><span data-ttu-id="bcecb-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="bcecb-162">mshr_completeddate</span></span><br><span data-ttu-id="bcecb-163">*Datum a čas*</span><span class="sxs-lookup"><span data-stu-id="bcecb-163">*Datetime*</span></span> | <span data-ttu-id="bcecb-164">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="bcecb-164">Read/write</span></span><br><span data-ttu-id="bcecb-165">Volitelné</span><span class="sxs-lookup"><span data-stu-id="bcecb-165">Optional</span></span> | <span data-ttu-id="bcecb-166">Datum dokončení prověřování.</span><span class="sxs-lookup"><span data-stu-id="bcecb-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="bcecb-167">**Poznámky**</span><span class="sxs-lookup"><span data-stu-id="bcecb-167">**Notes**</span></span><br><span data-ttu-id="bcecb-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="bcecb-168">mshr_note</span></span><br><span data-ttu-id="bcecb-169">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="bcecb-169">*String*</span></span> | <span data-ttu-id="bcecb-170">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="bcecb-170">Read/write</span></span><br><span data-ttu-id="bcecb-171">Volitelné</span><span class="sxs-lookup"><span data-stu-id="bcecb-171">Optional</span></span> | <span data-ttu-id="bcecb-172">Poznámky určené pro manažery náboru a náboráře.</span><span class="sxs-lookup"><span data-stu-id="bcecb-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="bcecb-173">Viz také</span><span class="sxs-lookup"><span data-stu-id="bcecb-173">See also</span></span>

[<span data-ttu-id="bcecb-174">Úvod do rozhraní API pro integraci systému sledování žadatelů</span><span class="sxs-lookup"><span data-stu-id="bcecb-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="bcecb-175">Příklad dotazu pro entitu Kandidát k přijetí</span><span class="sxs-lookup"><span data-stu-id="bcecb-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]