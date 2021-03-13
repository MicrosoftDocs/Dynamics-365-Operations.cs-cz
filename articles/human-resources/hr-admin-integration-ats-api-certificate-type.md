---
title: Typ certifikátu
description: Toto téma popisuje entitu typu Certifikát pro Dynamics 365 Human Resources.
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
ms.openlocfilehash: 1d2d53a628ef43d50bd83fd6b62807f44eddd653
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125706"
---
# <a name="certificate-type"></a><span data-ttu-id="37067-103">Typ certifikátu</span><span class="sxs-lookup"><span data-stu-id="37067-103">Certificate type</span></span>

<span data-ttu-id="37067-104">Toto téma popisuje entitu typu Certifikát pro Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="37067-104">This topic describes the Certificate type entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="37067-105">Fyzický název: mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="37067-105">Physical name: mshr_hcmcertificatetypeentity</span></span>

## <a name="description"></a><span data-ttu-id="37067-106">popis</span><span class="sxs-lookup"><span data-stu-id="37067-106">Description</span></span>

<span data-ttu-id="37067-107">Tato entita definuje seznam typů profesionálních certifikátů nastavených v Human Resources.</span><span class="sxs-lookup"><span data-stu-id="37067-107">This entity defines the list of professional certificate types set up in Human Resources.</span></span> <span data-ttu-id="37067-108">Entita není specifická pro právnickou osobu (společnost).</span><span class="sxs-lookup"><span data-stu-id="37067-108">The entity isn't specific to a legal entity (company).</span></span>

## <a name="json-representation"></a><span data-ttu-id="37067-109">Kód JSON</span><span class="sxs-lookup"><span data-stu-id="37067-109">JSON representation</span></span>

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="37067-110">Vlastnosti</span><span class="sxs-lookup"><span data-stu-id="37067-110">Properties</span></span>

| <span data-ttu-id="37067-111">Vlastnost</span><span class="sxs-lookup"><span data-stu-id="37067-111">Property</span></span><br><span data-ttu-id="37067-112">**Fyzický název**</span><span class="sxs-lookup"><span data-stu-id="37067-112">**Physical name**</span></span><br><span data-ttu-id="37067-113">**_Typ_**</span><span class="sxs-lookup"><span data-stu-id="37067-113">**_Type_**</span></span> | <span data-ttu-id="37067-114">Použít</span><span class="sxs-lookup"><span data-stu-id="37067-114">Use</span></span> | <span data-ttu-id="37067-115">popis</span><span class="sxs-lookup"><span data-stu-id="37067-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="37067-116">**ID entity typu certifikátu**</span><span class="sxs-lookup"><span data-stu-id="37067-116">**Certificate Type Entity ID**</span></span><br><span data-ttu-id="37067-117">mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="37067-117">mshr_hcmcertificatetypeentityid</span></span><br><span data-ttu-id="37067-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="37067-118">*GUID*</span></span> | <span data-ttu-id="37067-119">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="37067-119">Read-only</span></span><br><span data-ttu-id="37067-120">Povinná</span><span class="sxs-lookup"><span data-stu-id="37067-120">Required</span></span> 
<span data-ttu-id="37067-121">Generováno systémem</span><span class="sxs-lookup"><span data-stu-id="37067-121">System-generated</span></span> | <span data-ttu-id="37067-122">Jedinečný primární identifikátor pro záznam typu certifikátu.</span><span class="sxs-lookup"><span data-stu-id="37067-122">Unique primary identifier for the certificate type.</span></span> |
| <span data-ttu-id="37067-123">**Typ certifikátu**</span><span class="sxs-lookup"><span data-stu-id="37067-123">**Certificate Type**</span></span><br><span data-ttu-id="37067-124">mshr_certificatetype</span><span class="sxs-lookup"><span data-stu-id="37067-124">mshr_certificatetype</span></span><br><span data-ttu-id="37067-125">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="37067-125">*String*</span></span> | <span data-ttu-id="37067-126">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="37067-126">Read/write</span></span><br><span data-ttu-id="37067-127">Povinná</span><span class="sxs-lookup"><span data-stu-id="37067-127">Required</span></span> | <span data-ttu-id="37067-128">Jedinečný, uživatelem čitelný identifikátor pro typ certifikátu.</span><span class="sxs-lookup"><span data-stu-id="37067-128">Unique user-readable identifier for the certificate type.</span></span> |
| <span data-ttu-id="37067-129">**Popis**</span><span class="sxs-lookup"><span data-stu-id="37067-129">**Description**</span></span><br><span data-ttu-id="37067-130">mshr_description</span><span class="sxs-lookup"><span data-stu-id="37067-130">mshr_description</span></span><br><span data-ttu-id="37067-131">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="37067-131">*String*</span></span> | <span data-ttu-id="37067-132">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="37067-132">Read/write</span></span><br><span data-ttu-id="37067-133">Povinná</span><span class="sxs-lookup"><span data-stu-id="37067-133">Required</span></span> | <span data-ttu-id="37067-134">Popis typu certifikátu.</span><span class="sxs-lookup"><span data-stu-id="37067-134">Description of the certificate type.</span></span> |
| <span data-ttu-id="37067-135">**Vyžaduje obnovení**</span><span class="sxs-lookup"><span data-stu-id="37067-135">**Require Renewal**</span></span><br><span data-ttu-id="37067-136">mshr_requirerenewal</span><span class="sxs-lookup"><span data-stu-id="37067-136">mshr_requirerenewal</span></span><br><span data-ttu-id="37067-137">*Sada možností mshr_noyes*</span><span class="sxs-lookup"><span data-stu-id="37067-137">*mshr_noyes option set*</span></span> | <span data-ttu-id="37067-138">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="37067-138">Read/write</span></span><br><span data-ttu-id="37067-139">Volitelné</span><span class="sxs-lookup"><span data-stu-id="37067-139">Optional</span></span> | <span data-ttu-id="37067-140">Označuje, zda je pro certifikát vyžadováno obnovení.</span><span class="sxs-lookup"><span data-stu-id="37067-140">Indicates whether renewal is required for the certificate.</span></span> |

## <a name="see-also"></a><span data-ttu-id="37067-141">Viz také</span><span class="sxs-lookup"><span data-stu-id="37067-141">See also</span></span>

[<span data-ttu-id="37067-142">Úvod do rozhraní API pro integraci systému sledování žadatelů</span><span class="sxs-lookup"><span data-stu-id="37067-142">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="37067-143">Příklad dotazu pro entitu Kandidát k přijetí</span><span class="sxs-lookup"><span data-stu-id="37067-143">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

