---
title: Úroveň hodnocení
description: Toto téma popisuje entitu Úroveň hodnocení pro Dynamics 365 Human Resources.
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
ms.openlocfilehash: 1ad37c7a5b961bb03d37775168dac91e606d2b08
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125250"
---
# <a name="rating-level"></a><span data-ttu-id="d0b8e-103">Úroveň hodnocení</span><span class="sxs-lookup"><span data-stu-id="d0b8e-103">Rating level</span></span>

<span data-ttu-id="d0b8e-104">Toto téma popisuje entitu Úroveň hodnocení pro Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d0b8e-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="d0b8e-105">Fyzický název: mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="d0b8e-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="d0b8e-106">popis</span><span class="sxs-lookup"><span data-stu-id="d0b8e-106">Description</span></span>

<span data-ttu-id="d0b8e-107">Tato entita poskytuje dostupné úrovně hodnocení dovedností.</span><span class="sxs-lookup"><span data-stu-id="d0b8e-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="d0b8e-108">Úrovně hodnocení platí pro všechny právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="d0b8e-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="d0b8e-109">Kód JSON</span><span class="sxs-lookup"><span data-stu-id="d0b8e-109">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="d0b8e-110">Vlastnosti</span><span class="sxs-lookup"><span data-stu-id="d0b8e-110">Properties</span></span>

| <span data-ttu-id="d0b8e-111">Vlastnost</span><span class="sxs-lookup"><span data-stu-id="d0b8e-111">Property</span></span><br><span data-ttu-id="d0b8e-112">**Fyzický název**</span><span class="sxs-lookup"><span data-stu-id="d0b8e-112">**Physical name**</span></span><br><span data-ttu-id="d0b8e-113">**_Typ_**</span><span class="sxs-lookup"><span data-stu-id="d0b8e-113">**_Type_**</span></span> | <span data-ttu-id="d0b8e-114">Použít</span><span class="sxs-lookup"><span data-stu-id="d0b8e-114">Use</span></span> | <span data-ttu-id="d0b8e-115">popis</span><span class="sxs-lookup"><span data-stu-id="d0b8e-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d0b8e-116">**ID entity úrovně hodnocení**</span><span class="sxs-lookup"><span data-stu-id="d0b8e-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="d0b8e-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="d0b8e-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="d0b8e-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="d0b8e-118">*GUID*</span></span> | <span data-ttu-id="d0b8e-119">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="d0b8e-119">Read-only</span></span><br><span data-ttu-id="d0b8e-120">Povinná</span><span class="sxs-lookup"><span data-stu-id="d0b8e-120">Required</span></span><br><span data-ttu-id="d0b8e-121">Generováno systémem</span><span class="sxs-lookup"><span data-stu-id="d0b8e-121">System-generated</span></span> | <span data-ttu-id="d0b8e-122">Systémem generovaný jedinečný identifikátor úrovně.</span><span class="sxs-lookup"><span data-stu-id="d0b8e-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="d0b8e-123">**ID úrovně hodnocení**</span><span class="sxs-lookup"><span data-stu-id="d0b8e-123">**Rating Level ID**</span></span><br><span data-ttu-id="d0b8e-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="d0b8e-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="d0b8e-125">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="d0b8e-125">*String*</span></span> | <span data-ttu-id="d0b8e-126">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="d0b8e-126">Read/write</span></span><br><span data-ttu-id="d0b8e-127">Povinná</span><span class="sxs-lookup"><span data-stu-id="d0b8e-127">Required</span></span> | <span data-ttu-id="d0b8e-128">Jedinečný, uživatelem čitelný identifikátor úrovně.</span><span class="sxs-lookup"><span data-stu-id="d0b8e-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="d0b8e-129">**ID modelu hodnocení**</span><span class="sxs-lookup"><span data-stu-id="d0b8e-129">**Rating Model ID**</span></span><br><span data-ttu-id="d0b8e-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="d0b8e-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="d0b8e-131">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="d0b8e-131">*String*</span></span> | <span data-ttu-id="d0b8e-132">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="d0b8e-132">Read/write</span></span><br><span data-ttu-id="d0b8e-133">Povinná</span><span class="sxs-lookup"><span data-stu-id="d0b8e-133">Required</span></span> | <span data-ttu-id="d0b8e-134">Model hodnocení, ke kterému patří úroveň hodnocení.</span><span class="sxs-lookup"><span data-stu-id="d0b8e-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="d0b8e-135">**ID entity modelu hodnocení**</span><span class="sxs-lookup"><span data-stu-id="d0b8e-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="d0b8e-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="d0b8e-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="d0b8e-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="d0b8e-137">*GUID*</span></span> | <span data-ttu-id="d0b8e-138">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="d0b8e-138">Read-only</span></span><br><span data-ttu-id="d0b8e-139">Povinná</span><span class="sxs-lookup"><span data-stu-id="d0b8e-139">Required</span></span><br><span data-ttu-id="d0b8e-140">Cizí klíč: mshr_hcmratingmodelentityid entity mshr_hcmratingmodelentity</span><span class="sxs-lookup"><span data-stu-id="d0b8e-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="d0b8e-141">Systémem generovaný identifikátor pro model hodnocení, ke kterému patří úroveň hodnocení.</span><span class="sxs-lookup"><span data-stu-id="d0b8e-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="d0b8e-142">**Popis**</span><span class="sxs-lookup"><span data-stu-id="d0b8e-142">**Description**</span></span><br><span data-ttu-id="d0b8e-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="d0b8e-143">mshr_description</span></span><br><span data-ttu-id="d0b8e-144">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="d0b8e-144">*String*</span></span> | <span data-ttu-id="d0b8e-145">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="d0b8e-145">Read/write</span></span><br><span data-ttu-id="d0b8e-146">Povinná</span><span class="sxs-lookup"><span data-stu-id="d0b8e-146">Required</span></span> | <span data-ttu-id="d0b8e-147">Popis vybrané úrovně hodnocení.</span><span class="sxs-lookup"><span data-stu-id="d0b8e-147">The description of the rating level.</span></span> |
| <span data-ttu-id="d0b8e-148">**Koeficient**</span><span class="sxs-lookup"><span data-stu-id="d0b8e-148">**Factor**</span></span><br><span data-ttu-id="d0b8e-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="d0b8e-149">mshr_factor</span></span><br><span data-ttu-id="d0b8e-150">*Celé číslo*</span><span class="sxs-lookup"><span data-stu-id="d0b8e-150">*Integer*</span></span> | <span data-ttu-id="d0b8e-151">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="d0b8e-151">Read/write</span></span><br><span data-ttu-id="d0b8e-152">Povinná</span><span class="sxs-lookup"><span data-stu-id="d0b8e-152">Required</span></span> | <span data-ttu-id="d0b8e-153">Koeficient pro úroveň hodnocení.</span><span class="sxs-lookup"><span data-stu-id="d0b8e-153">The factor for the rating level.</span></span> <span data-ttu-id="d0b8e-154">Při porovnání položek s různým počtem úrovní hodnocení je možné vyrovnávat stav pomocí koeficientu.</span><span class="sxs-lookup"><span data-stu-id="d0b8e-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="d0b8e-155">Hodnota musí být celé číslo mezi 0 a 9.</span><span class="sxs-lookup"><span data-stu-id="d0b8e-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="d0b8e-156">**Poznámka**</span><span class="sxs-lookup"><span data-stu-id="d0b8e-156">**Note**</span></span><br><span data-ttu-id="d0b8e-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="d0b8e-157">mshr_note</span></span><br><span data-ttu-id="d0b8e-158">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="d0b8e-158">*String*</span></span> | <span data-ttu-id="d0b8e-159">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="d0b8e-159">Read/write</span></span><br><span data-ttu-id="d0b8e-160">Volitelné</span><span class="sxs-lookup"><span data-stu-id="d0b8e-160">Optional</span></span> | <span data-ttu-id="d0b8e-161">Jakékoli poznámky přidružené k úrovni hodnocení.</span><span class="sxs-lookup"><span data-stu-id="d0b8e-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="d0b8e-162">**Primární pole**</span><span class="sxs-lookup"><span data-stu-id="d0b8e-162">**Primary Field**</span></span><br><span data-ttu-id="d0b8e-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="d0b8e-163">mshr_primaryfield</span></span><br><span data-ttu-id="d0b8e-164">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="d0b8e-164">*String*</span></span> | <span data-ttu-id="d0b8e-165">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="d0b8e-165">Read-only</span></span><br><span data-ttu-id="d0b8e-166">Povinná</span><span class="sxs-lookup"><span data-stu-id="d0b8e-166">Required</span></span> | <span data-ttu-id="d0b8e-167">Pole, které se použije jako identifikátor záznamu entity.</span><span class="sxs-lookup"><span data-stu-id="d0b8e-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="d0b8e-168">Kombinace ID úrovně hodnocení a ID modelu hodnocení.</span><span class="sxs-lookup"><span data-stu-id="d0b8e-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="d0b8e-169">Viz také</span><span class="sxs-lookup"><span data-stu-id="d0b8e-169">See also</span></span>

[<span data-ttu-id="d0b8e-170">Úvod do rozhraní API pro integraci systému sledování žadatelů</span><span class="sxs-lookup"><span data-stu-id="d0b8e-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="d0b8e-171">Příklad dotazu pro entitu Kandidát k přijetí</span><span class="sxs-lookup"><span data-stu-id="d0b8e-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

