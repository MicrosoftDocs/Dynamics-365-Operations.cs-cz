---
title: Organizační hierarchie v Common Data Service
description: Toto téma popisuje integraci dat organizace mezi aplikacemi Finance and Operations a Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ca2ac0f9dbb8544b12f23a271423a43b0e601272
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789163"
---
## <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="26280-103">Organizační hierarchie v Common Data Service</span><span class="sxs-lookup"><span data-stu-id="26280-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="26280-104">Vzhledem k tomu, že Microsoft Dynamics 365 for Finance and Operations, je finanční systém, *organizace* je hlavním konceptem a nastavení systému začíná konfigurací hierarchie organizací.</span><span class="sxs-lookup"><span data-stu-id="26280-104">Because Microsoft Dynamics 365 for Finance and Operations is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="26280-105">Obchodní finance a operace lze poté sledovat na úrovni organizace a také na libovolné úrovni v hierarchii organizací.</span><span class="sxs-lookup"><span data-stu-id="26280-105">Business financials and operations can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="26280-106">Přestože Common Data Service nemá koncept organizační hierarchie, má několik volných konceptů, například celkový výnos z prodeje.</span><span class="sxs-lookup"><span data-stu-id="26280-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="26280-107">Jako součást integrace Common Data Service je do Common Data Service přidána datová struktura hierarchie organizací.</span><span class="sxs-lookup"><span data-stu-id="26280-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="26280-108">Tok dat</span><span class="sxs-lookup"><span data-stu-id="26280-108">Data flow</span></span>

<span data-ttu-id="26280-109">Podnikatelský ekosystém, který se skládá z Finance and Operations a Common Data Service bude nadále mít hierarchii organizací.</span><span class="sxs-lookup"><span data-stu-id="26280-109">A business ecosystem that consists of Finance and Operations and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="26280-110">Tato hierarchie organizací je postavena na Finance and Operations, ale je zpřístupněna v Common Data Service pro informační účely a účely rozšiřitelnosti.</span><span class="sxs-lookup"><span data-stu-id="26280-110">This organization hierarchy is built on Finance and Operations, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="26280-111">Následující ilustrace znázorňuje informace o hierarchii organizace, které jsou vystaveny v Common Data Service jako jednosměrný tok dat z Finance and Operations do Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="26280-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations to Common Data Service.</span></span>

![Obrázek architektury](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="26280-113">Šablony</span><span class="sxs-lookup"><span data-stu-id="26280-113">Templates</span></span>

<span data-ttu-id="26280-114">Mapování entity organizační hierarchie jsou k dispozici pro jednosměrnou synchronizaci dat z Finance and Operations do Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="26280-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="26280-115">Interní účel hierarchie organizací</span><span class="sxs-lookup"><span data-stu-id="26280-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="26280-116">Tato šablona poskytuje jednosměrnou synchronizaci entity účel hierarchie organizace z Finance and Operations do Dynamics 365 for Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="26280-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to Dynamics 365 for Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="26280-117">Zdrojové pole</span><span class="sxs-lookup"><span data-stu-id="26280-117">Source field</span></span> | <span data-ttu-id="26280-118">Typ mapování</span><span class="sxs-lookup"><span data-stu-id="26280-118">Map type</span></span> | <span data-ttu-id="26280-119">Cílové pole</span><span class="sxs-lookup"><span data-stu-id="26280-119">Destination field</span></span>
---|---|---
<span data-ttu-id="26280-120">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="26280-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="26280-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="26280-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="26280-122">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="26280-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="26280-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="26280-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="26280-124">HIERARCHYPURPOSE</span><span class="sxs-lookup"><span data-stu-id="26280-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="26280-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="26280-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="26280-126">IMMUTABLE</span><span class="sxs-lookup"><span data-stu-id="26280-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="26280-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="26280-127">msdyn\_immutable</span></span>
<span data-ttu-id="26280-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="26280-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="26280-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="26280-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="26280-130">Typ interní organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="26280-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="26280-131">Tato šablona poskytuje jednosměrnou synchronizaci entity typ hierarchie organizace z Finance and Operations do Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="26280-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="26280-132">Zdrojové pole</span><span class="sxs-lookup"><span data-stu-id="26280-132">Source field</span></span> | <span data-ttu-id="26280-133">Typ mapování</span><span class="sxs-lookup"><span data-stu-id="26280-133">Map type</span></span> | <span data-ttu-id="26280-134">Cílové pole</span><span class="sxs-lookup"><span data-stu-id="26280-134">Destination field</span></span>
---|---|---
<span data-ttu-id="26280-135">NÁZEV</span><span class="sxs-lookup"><span data-stu-id="26280-135">NAME</span></span> | \> | <span data-ttu-id="26280-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="26280-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="26280-137">Interní organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="26280-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="26280-138">Tato šablona poskytuje jednosměrnou synchronizaci entity publikovaná hierarchie organizace z Finance and Operations do Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="26280-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="26280-139">Zdrojové pole</span><span class="sxs-lookup"><span data-stu-id="26280-139">Source field</span></span> | <span data-ttu-id="26280-140">Typ mapování</span><span class="sxs-lookup"><span data-stu-id="26280-140">Map type</span></span> | <span data-ttu-id="26280-141">Cílové pole</span><span class="sxs-lookup"><span data-stu-id="26280-141">Destination field</span></span>
---|---|---
<span data-ttu-id="26280-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="26280-142">VALIDTO</span></span> | \> | <span data-ttu-id="26280-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="26280-143">msdyn\_validto</span></span>
<span data-ttu-id="26280-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="26280-144">VALIDFROM</span></span> | \> | <span data-ttu-id="26280-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="26280-145">msdyn\_validfrom</span></span>
<span data-ttu-id="26280-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="26280-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="26280-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="26280-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="26280-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="26280-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="26280-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="26280-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="26280-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="26280-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="26280-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="26280-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="26280-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="26280-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="26280-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="26280-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="26280-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="26280-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="26280-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="26280-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="26280-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="26280-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="26280-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="26280-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="26280-158">Interní organizace</span><span class="sxs-lookup"><span data-stu-id="26280-158">Internal Organization</span></span>

<span data-ttu-id="26280-159">Informace o interní organizaci v Common Data Service pocházejí ze dvou entit aplikace Finance and Operations, **provozní jednotka** a **právnická osoba**.</span><span class="sxs-lookup"><span data-stu-id="26280-159">Internal organization information in Common Data Service comes from two Finance and Operations entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="26280-160">Provozní jednotka</span><span class="sxs-lookup"><span data-stu-id="26280-160">Operating unit</span></span>

<span data-ttu-id="26280-161">Zdrojové pole</span><span class="sxs-lookup"><span data-stu-id="26280-161">Source field</span></span> | <span data-ttu-id="26280-162">Typ mapování</span><span class="sxs-lookup"><span data-stu-id="26280-162">Map type</span></span> | <span data-ttu-id="26280-163">Cílové pole</span><span class="sxs-lookup"><span data-stu-id="26280-163">Destination field</span></span>
---|---|---
<span data-ttu-id="26280-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="26280-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="26280-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="26280-165">msdyn\_languageid</span></span>
<span data-ttu-id="26280-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="26280-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="26280-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="26280-167">msdyn\_namealias</span></span>
<span data-ttu-id="26280-168">NÁZEV</span><span class="sxs-lookup"><span data-stu-id="26280-168">NAME</span></span> | \> | <span data-ttu-id="26280-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="26280-169">msdyn\_name</span></span>
<span data-ttu-id="26280-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="26280-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="26280-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="26280-171">msdyn\_partynumber</span></span>
<span data-ttu-id="26280-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="26280-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="26280-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="26280-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="26280-174">Právnická osoba</span><span class="sxs-lookup"><span data-stu-id="26280-174">Legal entity</span></span>

<span data-ttu-id="26280-175">Zdrojové pole</span><span class="sxs-lookup"><span data-stu-id="26280-175">Source field</span></span> | <span data-ttu-id="26280-176">Typ mapování</span><span class="sxs-lookup"><span data-stu-id="26280-176">Map type</span></span> | <span data-ttu-id="26280-177">Cílové pole</span><span class="sxs-lookup"><span data-stu-id="26280-177">Destination field</span></span>
---|---|---
<span data-ttu-id="26280-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="26280-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="26280-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="26280-179">msdyn\_namealias</span></span>
<span data-ttu-id="26280-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="26280-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="26280-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="26280-181">msdyn\_languageid</span></span>
<span data-ttu-id="26280-182">NÁZEV</span><span class="sxs-lookup"><span data-stu-id="26280-182">NAME</span></span> | \> | <span data-ttu-id="26280-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="26280-183">msdyn\_name</span></span>
<span data-ttu-id="26280-184">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="26280-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="26280-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="26280-185">msdyn\_partynumber</span></span>
<span data-ttu-id="26280-186">žádná</span><span class="sxs-lookup"><span data-stu-id="26280-186">none</span></span> | \>\> | <span data-ttu-id="26280-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="26280-187">msdyn\_type</span></span>
<span data-ttu-id="26280-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="26280-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="26280-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="26280-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="26280-190">Společnost</span><span class="sxs-lookup"><span data-stu-id="26280-190">Company</span></span>

<span data-ttu-id="26280-191">Poskytuje obousměrnou synchronizaci informací o právnické osobě (společnosti) mezi Finance and Operations a Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="26280-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="26280-192">Zdrojové pole</span><span class="sxs-lookup"><span data-stu-id="26280-192">Source field</span></span> | <span data-ttu-id="26280-193">Typ mapování</span><span class="sxs-lookup"><span data-stu-id="26280-193">Map type</span></span> | <span data-ttu-id="26280-194">Cílové pole</span><span class="sxs-lookup"><span data-stu-id="26280-194">Destination field</span></span>
---|---|---
<span data-ttu-id="26280-195">NÁZEV</span><span class="sxs-lookup"><span data-stu-id="26280-195">NAME</span></span> | = | <span data-ttu-id="26280-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="26280-196">cdm\_name</span></span>
<span data-ttu-id="26280-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="26280-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="26280-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="26280-198">cdm\_companycode</span></span>
