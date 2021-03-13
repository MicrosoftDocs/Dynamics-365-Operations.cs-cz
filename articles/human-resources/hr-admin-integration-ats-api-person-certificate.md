---
title: Certifikát osoby
description: Toto téma popisuje entitu Certifikát osoby pro Dynamics 365 Human Resources.
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
ms.openlocfilehash: fa4582dc00341a647f1ea43ed16d9dce8bfcf688
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125346"
---
# <a name="person-certificate"></a><span data-ttu-id="a44f3-103">Certifikát osoby</span><span class="sxs-lookup"><span data-stu-id="a44f3-103">Person certificate</span></span>

<span data-ttu-id="a44f3-104">Toto téma popisuje entitu Certifikát osoby pro Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a44f3-104">This topic describes the Person certificate entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="a44f3-105">Fyzický název: mshr_hcmpersoncertificateentity</span><span class="sxs-lookup"><span data-stu-id="a44f3-105">Physical name: mshr_hcmpersoncertificateentity</span></span>

## <a name="description"></a><span data-ttu-id="a44f3-106">popis</span><span class="sxs-lookup"><span data-stu-id="a44f3-106">Description</span></span>

<span data-ttu-id="a44f3-107">Tato entita popisuje profesní certifikáty kandidáta.</span><span class="sxs-lookup"><span data-stu-id="a44f3-107">This entity describes the professional certificates of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="a44f3-108">Kód JSON</span><span class="sxs-lookup"><span data-stu-id="a44f3-108">JSON representation</span></span>

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="a44f3-109">Vlastnosti</span><span class="sxs-lookup"><span data-stu-id="a44f3-109">Properties</span></span>

| <span data-ttu-id="a44f3-110">Vlastnost</span><span class="sxs-lookup"><span data-stu-id="a44f3-110">Property</span></span><br><span data-ttu-id="a44f3-111">**Fyzický název**</span><span class="sxs-lookup"><span data-stu-id="a44f3-111">**Physical name**</span></span><br><span data-ttu-id="a44f3-112">**_Typ_**</span><span class="sxs-lookup"><span data-stu-id="a44f3-112">**_Type_**</span></span> | <span data-ttu-id="a44f3-113">Použít</span><span class="sxs-lookup"><span data-stu-id="a44f3-113">Use</span></span> | <span data-ttu-id="a44f3-114">popis</span><span class="sxs-lookup"><span data-stu-id="a44f3-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="a44f3-115">**ID entity Certifikát osoby**</span><span class="sxs-lookup"><span data-stu-id="a44f3-115">**Person Certificate Entity ID**</span></span><br><span data-ttu-id="a44f3-116">mshr_hcmpersoncertificateentityid</span><span class="sxs-lookup"><span data-stu-id="a44f3-116">mshr_hcmpersoncertificateentityid</span></span><br><span data-ttu-id="a44f3-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="a44f3-117">*GUID*</span></span> | <span data-ttu-id="a44f3-118">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="a44f3-118">Read-only</span></span><br><span data-ttu-id="a44f3-119">Povinná</span><span class="sxs-lookup"><span data-stu-id="a44f3-119">Required</span></span> | <span data-ttu-id="a44f3-120">Systémem generovaný jedinečný identifikátor pro záznam entity certifikátu osoby.</span><span class="sxs-lookup"><span data-stu-id="a44f3-120">System-generated unique identifier for the person certificate entity record.</span></span> |
| <span data-ttu-id="a44f3-121">**Číslo strany**</span><span class="sxs-lookup"><span data-stu-id="a44f3-121">**Party Number**</span></span><br><span data-ttu-id="a44f3-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="a44f3-122">mshr_partynumber</span></span><br><span data-ttu-id="a44f3-123">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="a44f3-123">*String*</span></span> | <span data-ttu-id="a44f3-124">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="a44f3-124">Read/write</span></span><br><span data-ttu-id="a44f3-125">Povinná</span><span class="sxs-lookup"><span data-stu-id="a44f3-125">Required</span></span> | <span data-ttu-id="a44f3-126">ID strany (osoby), která je kandidátem.</span><span class="sxs-lookup"><span data-stu-id="a44f3-126">The party (person) ID of the candidate.</span></span> |
| <span data-ttu-id="a44f3-127">**Hodnota ID osoby**</span><span class="sxs-lookup"><span data-stu-id="a44f3-127">**Person ID Value**</span></span><br><span data-ttu-id="a44f3-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="a44f3-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="a44f3-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="a44f3-129">*GUID*</span></span> | <span data-ttu-id="a44f3-130">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="a44f3-130">Read-only</span></span><br><span data-ttu-id="a44f3-131">Povinná</span><span class="sxs-lookup"><span data-stu-id="a44f3-131">Required</span></span><br><span data-ttu-id="a44f3-132">Cizí klíč: mshr_dirpersonentityid entity mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="a44f3-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="a44f3-133">Systémem generovaný jedinečný identifikátor záznamu entity strany (osoby).</span><span class="sxs-lookup"><span data-stu-id="a44f3-133">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="a44f3-134">**ID typu certifikátu**</span><span class="sxs-lookup"><span data-stu-id="a44f3-134">**Certificate Type ID**</span></span><br><span data-ttu-id="a44f3-135">mshr_certificatetypeid</span><span class="sxs-lookup"><span data-stu-id="a44f3-135">mshr_certificatetypeid</span></span><br><span data-ttu-id="a44f3-136">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="a44f3-136">*String*</span></span> | <span data-ttu-id="a44f3-137">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="a44f3-137">Read/write</span></span><br><span data-ttu-id="a44f3-138">Povinná</span><span class="sxs-lookup"><span data-stu-id="a44f3-138">Required</span></span> |  <span data-ttu-id="a44f3-139">Identifikátor typu certifikátu definovaného v Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a44f3-139">The identifier of the certificate type defined in Human Resources.</span></span> |
| <span data-ttu-id="a44f3-140">**Hodnota ID typu certifikátu**</span><span class="sxs-lookup"><span data-stu-id="a44f3-140">**Certificate Type ID Value**</span></span><br><span data-ttu-id="a44f3-141">_mshr_fk_certificatetype_id_value</span><span class="sxs-lookup"><span data-stu-id="a44f3-141">_mshr_fk_certificatetype_id_value</span></span><br><span data-ttu-id="a44f3-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="a44f3-142">*GUID*</span></span> | <span data-ttu-id="a44f3-143">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="a44f3-143">Read-only</span></span><br><span data-ttu-id="a44f3-144">Povinná</span><span class="sxs-lookup"><span data-stu-id="a44f3-144">Required</span></span><br><span data-ttu-id="a44f3-145">Cizí klíč: mshr_hcmcertificatetypeentityid entity mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="a44f3-145">Foreign key: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity</span></span> | <span data-ttu-id="a44f3-146">Systémem generovaný jedinečný identifikátor typu certifikátu přidružené entity.</span><span class="sxs-lookup"><span data-stu-id="a44f3-146">System-generated unique identifier of the certificate type in the associated entity.</span></span> |
| <span data-ttu-id="a44f3-147">**Počáteční datum**</span><span class="sxs-lookup"><span data-stu-id="a44f3-147">**Start Date**</span></span><br><span data-ttu-id="a44f3-148">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="a44f3-148">mshr_startdate</span></span><br><span data-ttu-id="a44f3-149">*Datum a čas*</span><span class="sxs-lookup"><span data-stu-id="a44f3-149">*Datetime*</span></span> | <span data-ttu-id="a44f3-150">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="a44f3-150">Read/write</span></span><br><span data-ttu-id="a44f3-151">Povinná</span><span class="sxs-lookup"><span data-stu-id="a44f3-151">Required</span></span> | <span data-ttu-id="a44f3-152">Datum vystavení certifikátu.</span><span class="sxs-lookup"><span data-stu-id="a44f3-152">The date at which the certificate was issued.</span></span> |
| <span data-ttu-id="a44f3-153">**Koncové datum**</span><span class="sxs-lookup"><span data-stu-id="a44f3-153">**End Date**</span></span><br><span data-ttu-id="a44f3-154">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="a44f3-154">mshr_enddate</span></span><br><span data-ttu-id="a44f3-155">*Datum a čas*</span><span class="sxs-lookup"><span data-stu-id="a44f3-155">*Datetime*</span></span> | <span data-ttu-id="a44f3-156">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="a44f3-156">Read/write</span></span><br><span data-ttu-id="a44f3-157">Volitelné</span><span class="sxs-lookup"><span data-stu-id="a44f3-157">Optional</span></span> | <span data-ttu-id="a44f3-158">Datum konce platnosti certifikátu.</span><span class="sxs-lookup"><span data-stu-id="a44f3-158">The date at which the certificate will expire.</span></span> |
| <span data-ttu-id="a44f3-159">**Poznámky**</span><span class="sxs-lookup"><span data-stu-id="a44f3-159">**Notes**</span></span><br><span data-ttu-id="a44f3-160">mshr_notes</span><span class="sxs-lookup"><span data-stu-id="a44f3-160">mshr_notes</span></span><br><span data-ttu-id="a44f3-161">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="a44f3-161">*String*</span></span> | <span data-ttu-id="a44f3-162">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="a44f3-162">Read/write</span></span><br><span data-ttu-id="a44f3-163">Volitelné</span><span class="sxs-lookup"><span data-stu-id="a44f3-163">Optional</span></span> | <span data-ttu-id="a44f3-164">Poznámky určené pro manažery náboru a náboráře.</span><span class="sxs-lookup"><span data-stu-id="a44f3-164">Notes for use by hiring managers and recruiters.</span></span> |
| <span data-ttu-id="a44f3-165">**Primární pole**</span><span class="sxs-lookup"><span data-stu-id="a44f3-165">**Primary Field**</span></span><br><span data-ttu-id="a44f3-166">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="a44f3-166">mshr_primaryfield</span></span><br><span data-ttu-id="a44f3-167">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="a44f3-167">*String*</span></span> | <span data-ttu-id="a44f3-168">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="a44f3-168">Read-only</span></span><br><span data-ttu-id="a44f3-169">Povinná</span><span class="sxs-lookup"><span data-stu-id="a44f3-169">Required</span></span> |  <span data-ttu-id="a44f3-170">Pole, které se použije jako identifikátor záznamu entity.</span><span class="sxs-lookup"><span data-stu-id="a44f3-170">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="a44f3-171">Kombinace čísla strany, ID typu certifikátu a počátečního data.</span><span class="sxs-lookup"><span data-stu-id="a44f3-171">Combination of party number, certificate type ID, and start date.</span></span> |

## <a name="see-also"></a><span data-ttu-id="a44f3-172">Viz také</span><span class="sxs-lookup"><span data-stu-id="a44f3-172">See also</span></span>

[<span data-ttu-id="a44f3-173">Úvod do rozhraní API pro integraci systému sledování žadatelů</span><span class="sxs-lookup"><span data-stu-id="a44f3-173">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="a44f3-174">Příklad dotazu pro entitu Kandidát k přijetí</span><span class="sxs-lookup"><span data-stu-id="a44f3-174">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

