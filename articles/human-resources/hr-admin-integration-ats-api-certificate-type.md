---
title: Typ certifikátu
description: Toto téma popisuje entitu typu Certifikát pro Dynamics 365 Human Resources.
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
ms.openlocfilehash: fe5713b6b5f38ad7f6857b36c6b2f63a1dc0c320
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798385"
---
# <a name="certificate-type"></a><span data-ttu-id="058cf-103">Typ certifikátu</span><span class="sxs-lookup"><span data-stu-id="058cf-103">Certificate type</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="058cf-104">Toto téma popisuje entitu typu Certifikát pro Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="058cf-104">This topic describes the Certificate type entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="058cf-105">Fyzický název: mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="058cf-105">Physical name: mshr_hcmcertificatetypeentity</span></span>

## <a name="description"></a><span data-ttu-id="058cf-106">popis</span><span class="sxs-lookup"><span data-stu-id="058cf-106">Description</span></span>

<span data-ttu-id="058cf-107">Tato entita definuje seznam typů profesionálních certifikátů nastavených v Human Resources.</span><span class="sxs-lookup"><span data-stu-id="058cf-107">This entity defines the list of professional certificate types set up in Human Resources.</span></span> <span data-ttu-id="058cf-108">Entita není specifická pro právnickou osobu (společnost).</span><span class="sxs-lookup"><span data-stu-id="058cf-108">The entity isn't specific to a legal entity (company).</span></span>

## <a name="json-representation"></a><span data-ttu-id="058cf-109">Kód JSON</span><span class="sxs-lookup"><span data-stu-id="058cf-109">JSON representation</span></span>

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="058cf-110">Vlastnosti</span><span class="sxs-lookup"><span data-stu-id="058cf-110">Properties</span></span>

| <span data-ttu-id="058cf-111">Vlastnost</span><span class="sxs-lookup"><span data-stu-id="058cf-111">Property</span></span><br><span data-ttu-id="058cf-112">**Fyzický název**</span><span class="sxs-lookup"><span data-stu-id="058cf-112">**Physical name**</span></span><br><span data-ttu-id="058cf-113">**_Typ_**</span><span class="sxs-lookup"><span data-stu-id="058cf-113">**_Type_**</span></span> | <span data-ttu-id="058cf-114">Použít</span><span class="sxs-lookup"><span data-stu-id="058cf-114">Use</span></span> | <span data-ttu-id="058cf-115">popis</span><span class="sxs-lookup"><span data-stu-id="058cf-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="058cf-116">**ID entity typu certifikátu**</span><span class="sxs-lookup"><span data-stu-id="058cf-116">**Certificate Type Entity ID**</span></span><br><span data-ttu-id="058cf-117">mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="058cf-117">mshr_hcmcertificatetypeentityid</span></span><br><span data-ttu-id="058cf-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="058cf-118">*GUID*</span></span> | <span data-ttu-id="058cf-119">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="058cf-119">Read-only</span></span><br><span data-ttu-id="058cf-120">Povinná</span><span class="sxs-lookup"><span data-stu-id="058cf-120">Required</span></span> 
<span data-ttu-id="058cf-121">Generováno systémem</span><span class="sxs-lookup"><span data-stu-id="058cf-121">System-generated</span></span> | <span data-ttu-id="058cf-122">Jedinečný primární identifikátor pro záznam typu certifikátu.</span><span class="sxs-lookup"><span data-stu-id="058cf-122">Unique primary identifier for the certificate type.</span></span> |
| <span data-ttu-id="058cf-123">**Typ certifikátu**</span><span class="sxs-lookup"><span data-stu-id="058cf-123">**Certificate Type**</span></span><br><span data-ttu-id="058cf-124">mshr_certificatetype</span><span class="sxs-lookup"><span data-stu-id="058cf-124">mshr_certificatetype</span></span><br><span data-ttu-id="058cf-125">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="058cf-125">*String*</span></span> | <span data-ttu-id="058cf-126">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="058cf-126">Read/write</span></span><br><span data-ttu-id="058cf-127">Povinná</span><span class="sxs-lookup"><span data-stu-id="058cf-127">Required</span></span> | <span data-ttu-id="058cf-128">Jedinečný, uživatelem čitelný identifikátor pro typ certifikátu.</span><span class="sxs-lookup"><span data-stu-id="058cf-128">Unique user-readable identifier for the certificate type.</span></span> |
| <span data-ttu-id="058cf-129">**Popis**</span><span class="sxs-lookup"><span data-stu-id="058cf-129">**Description**</span></span><br><span data-ttu-id="058cf-130">mshr_description</span><span class="sxs-lookup"><span data-stu-id="058cf-130">mshr_description</span></span><br><span data-ttu-id="058cf-131">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="058cf-131">*String*</span></span> | <span data-ttu-id="058cf-132">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="058cf-132">Read/write</span></span><br><span data-ttu-id="058cf-133">Povinná</span><span class="sxs-lookup"><span data-stu-id="058cf-133">Required</span></span> | <span data-ttu-id="058cf-134">Popis typu certifikátu.</span><span class="sxs-lookup"><span data-stu-id="058cf-134">Description of the certificate type.</span></span> |
| <span data-ttu-id="058cf-135">**Vyžaduje obnovení**</span><span class="sxs-lookup"><span data-stu-id="058cf-135">**Require Renewal**</span></span><br><span data-ttu-id="058cf-136">mshr_requirerenewal</span><span class="sxs-lookup"><span data-stu-id="058cf-136">mshr_requirerenewal</span></span><br><span data-ttu-id="058cf-137">*Sada možností mshr_noyes*</span><span class="sxs-lookup"><span data-stu-id="058cf-137">*mshr_noyes option set*</span></span> | <span data-ttu-id="058cf-138">Čtení/zápis</span><span class="sxs-lookup"><span data-stu-id="058cf-138">Read/write</span></span><br><span data-ttu-id="058cf-139">Volitelné</span><span class="sxs-lookup"><span data-stu-id="058cf-139">Optional</span></span> | <span data-ttu-id="058cf-140">Označuje, zda je pro certifikát vyžadováno obnovení.</span><span class="sxs-lookup"><span data-stu-id="058cf-140">Indicates whether renewal is required for the certificate.</span></span> |

## <a name="see-also"></a><span data-ttu-id="058cf-141">Viz také</span><span class="sxs-lookup"><span data-stu-id="058cf-141">See also</span></span>

[<span data-ttu-id="058cf-142">Úvod do rozhraní API pro integraci systému sledování žadatelů</span><span class="sxs-lookup"><span data-stu-id="058cf-142">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="058cf-143">Příklad dotazu pro entitu Kandidát k přijetí</span><span class="sxs-lookup"><span data-stu-id="058cf-143">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]