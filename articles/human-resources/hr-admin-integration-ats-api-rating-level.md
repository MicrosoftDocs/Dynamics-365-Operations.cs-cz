---
title: Úroveň hodnocení
description: Toto téma popisuje entitu Úroveň hodnocení pro Dynamics 365 Human Resources.
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
ms.openlocfilehash: eac80599de07a045aa233f1cdfd16fe0db8733a2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800326"
---
# <a name="rating-level"></a><span data-ttu-id="f62c6-103">Úroveň hodnocení</span><span class="sxs-lookup"><span data-stu-id="f62c6-103">Rating level</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f62c6-104">Toto téma popisuje entitu Úroveň hodnocení pro Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f62c6-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="f62c6-105">Fyzický název: mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="f62c6-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="f62c6-106">popis</span><span class="sxs-lookup"><span data-stu-id="f62c6-106">Description</span></span>

<span data-ttu-id="f62c6-107">Tato entita poskytuje dostupné úrovně hodnocení dovedností.</span><span class="sxs-lookup"><span data-stu-id="f62c6-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="f62c6-108">Úrovně hodnocení platí pro všechny právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="f62c6-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="f62c6-109">Kód JSON</span><span class="sxs-lookup"><span data-stu-id="f62c6-109">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="f62c6-110">Vlastnosti</span><span class="sxs-lookup"><span data-stu-id="f62c6-110">Properties</span></span>

| <span data-ttu-id="f62c6-111">Vlastnost</span><span class="sxs-lookup"><span data-stu-id="f62c6-111">Property</span></span><br><span data-ttu-id="f62c6-112">**Fyzický název**</span><span class="sxs-lookup"><span data-stu-id="f62c6-112">**Physical name**</span></span><br><span data-ttu-id="f62c6-113">**_Typ_**</span><span class="sxs-lookup"><span data-stu-id="f62c6-113">**_Type_**</span></span> | <span data-ttu-id="f62c6-114">Použít</span><span class="sxs-lookup"><span data-stu-id="f62c6-114">Use</span></span> | <span data-ttu-id="f62c6-115">popis</span><span class="sxs-lookup"><span data-stu-id="f62c6-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f62c6-116">**ID entity úrovně hodnocení**</span><span class="sxs-lookup"><span data-stu-id="f62c6-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="f62c6-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="f62c6-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="f62c6-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f62c6-118">*GUID*</span></span> | <span data-ttu-id="f62c6-119">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="f62c6-119">Read-only</span></span><br><span data-ttu-id="f62c6-120">Povinná</span><span class="sxs-lookup"><span data-stu-id="f62c6-120">Required</span></span><br><span data-ttu-id="f62c6-121">Generováno systémem</span><span class="sxs-lookup"><span data-stu-id="f62c6-121">System-generated</span></span> | <span data-ttu-id="f62c6-122">Systémem generovaný jedinečný identifikátor úrovně.</span><span class="sxs-lookup"><span data-stu-id="f62c6-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="f62c6-123">**ID úrovně hodnocení**</span><span class="sxs-lookup"><span data-stu-id="f62c6-123">**Rating Level ID**</span></span><br><span data-ttu-id="f62c6-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="f62c6-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="f62c6-125">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="f62c6-125">*String*</span></span> | <span data-ttu-id="f62c6-126">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="f62c6-126">Read/write</span></span><br><span data-ttu-id="f62c6-127">Povinná</span><span class="sxs-lookup"><span data-stu-id="f62c6-127">Required</span></span> | <span data-ttu-id="f62c6-128">Jedinečný, uživatelem čitelný identifikátor úrovně.</span><span class="sxs-lookup"><span data-stu-id="f62c6-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="f62c6-129">**ID modelu hodnocení**</span><span class="sxs-lookup"><span data-stu-id="f62c6-129">**Rating Model ID**</span></span><br><span data-ttu-id="f62c6-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="f62c6-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="f62c6-131">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="f62c6-131">*String*</span></span> | <span data-ttu-id="f62c6-132">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="f62c6-132">Read/write</span></span><br><span data-ttu-id="f62c6-133">Povinná</span><span class="sxs-lookup"><span data-stu-id="f62c6-133">Required</span></span> | <span data-ttu-id="f62c6-134">Model hodnocení, ke kterému patří úroveň hodnocení.</span><span class="sxs-lookup"><span data-stu-id="f62c6-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="f62c6-135">**ID entity modelu hodnocení**</span><span class="sxs-lookup"><span data-stu-id="f62c6-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="f62c6-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="f62c6-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="f62c6-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f62c6-137">*GUID*</span></span> | <span data-ttu-id="f62c6-138">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="f62c6-138">Read-only</span></span><br><span data-ttu-id="f62c6-139">Povinná</span><span class="sxs-lookup"><span data-stu-id="f62c6-139">Required</span></span><br><span data-ttu-id="f62c6-140">Cizí klíč: mshr_hcmratingmodelentityid entity mshr_hcmratingmodelentity</span><span class="sxs-lookup"><span data-stu-id="f62c6-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="f62c6-141">Systémem generovaný identifikátor pro model hodnocení, ke kterému patří úroveň hodnocení.</span><span class="sxs-lookup"><span data-stu-id="f62c6-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="f62c6-142">**Popis**</span><span class="sxs-lookup"><span data-stu-id="f62c6-142">**Description**</span></span><br><span data-ttu-id="f62c6-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="f62c6-143">mshr_description</span></span><br><span data-ttu-id="f62c6-144">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="f62c6-144">*String*</span></span> | <span data-ttu-id="f62c6-145">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="f62c6-145">Read/write</span></span><br><span data-ttu-id="f62c6-146">Povinná</span><span class="sxs-lookup"><span data-stu-id="f62c6-146">Required</span></span> | <span data-ttu-id="f62c6-147">Popis vybrané úrovně hodnocení.</span><span class="sxs-lookup"><span data-stu-id="f62c6-147">The description of the rating level.</span></span> |
| <span data-ttu-id="f62c6-148">**Koeficient**</span><span class="sxs-lookup"><span data-stu-id="f62c6-148">**Factor**</span></span><br><span data-ttu-id="f62c6-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="f62c6-149">mshr_factor</span></span><br><span data-ttu-id="f62c6-150">*Celé číslo*</span><span class="sxs-lookup"><span data-stu-id="f62c6-150">*Integer*</span></span> | <span data-ttu-id="f62c6-151">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="f62c6-151">Read/write</span></span><br><span data-ttu-id="f62c6-152">Povinná</span><span class="sxs-lookup"><span data-stu-id="f62c6-152">Required</span></span> | <span data-ttu-id="f62c6-153">Koeficient pro úroveň hodnocení.</span><span class="sxs-lookup"><span data-stu-id="f62c6-153">The factor for the rating level.</span></span> <span data-ttu-id="f62c6-154">Při porovnání položek s různým počtem úrovní hodnocení je možné vyrovnávat stav pomocí koeficientu.</span><span class="sxs-lookup"><span data-stu-id="f62c6-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="f62c6-155">Hodnota musí být celé číslo mezi 0 a 9.</span><span class="sxs-lookup"><span data-stu-id="f62c6-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="f62c6-156">**Poznámka**</span><span class="sxs-lookup"><span data-stu-id="f62c6-156">**Note**</span></span><br><span data-ttu-id="f62c6-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="f62c6-157">mshr_note</span></span><br><span data-ttu-id="f62c6-158">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="f62c6-158">*String*</span></span> | <span data-ttu-id="f62c6-159">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="f62c6-159">Read/write</span></span><br><span data-ttu-id="f62c6-160">Volitelné</span><span class="sxs-lookup"><span data-stu-id="f62c6-160">Optional</span></span> | <span data-ttu-id="f62c6-161">Jakékoli poznámky přidružené k úrovni hodnocení.</span><span class="sxs-lookup"><span data-stu-id="f62c6-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="f62c6-162">**Primární pole**</span><span class="sxs-lookup"><span data-stu-id="f62c6-162">**Primary Field**</span></span><br><span data-ttu-id="f62c6-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="f62c6-163">mshr_primaryfield</span></span><br><span data-ttu-id="f62c6-164">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="f62c6-164">*String*</span></span> | <span data-ttu-id="f62c6-165">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="f62c6-165">Read-only</span></span><br><span data-ttu-id="f62c6-166">Povinná</span><span class="sxs-lookup"><span data-stu-id="f62c6-166">Required</span></span> | <span data-ttu-id="f62c6-167">Pole, které se použije jako identifikátor záznamu entity.</span><span class="sxs-lookup"><span data-stu-id="f62c6-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="f62c6-168">Kombinace ID úrovně hodnocení a ID modelu hodnocení.</span><span class="sxs-lookup"><span data-stu-id="f62c6-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="f62c6-169">Viz také</span><span class="sxs-lookup"><span data-stu-id="f62c6-169">See also</span></span>

[<span data-ttu-id="f62c6-170">Úvod do rozhraní API pro integraci systému sledování žadatelů</span><span class="sxs-lookup"><span data-stu-id="f62c6-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="f62c6-171">Příklad dotazu pro entitu Kandidát k přijetí</span><span class="sxs-lookup"><span data-stu-id="f62c6-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]