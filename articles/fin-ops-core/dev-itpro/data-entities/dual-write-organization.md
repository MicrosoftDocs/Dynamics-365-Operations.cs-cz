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
ms.openlocfilehash: fd159b38f69305dcaecb364ba0ccb3befabb3582
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182018"
---
## <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="f5da7-103">Organizační hierarchie v Common Data Service</span><span class="sxs-lookup"><span data-stu-id="f5da7-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="f5da7-104">Vzhledem k tomu, že Dynamics 365 Finance, je finanční systém, *organizace* je hlavním konceptem a nastavení systému začíná konfigurací hierarchie organizací.</span><span class="sxs-lookup"><span data-stu-id="f5da7-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="f5da7-105">Obchodní finance lze poté sledovat na úrovni organizace a také na libovolné úrovni v hierarchii organizací.</span><span class="sxs-lookup"><span data-stu-id="f5da7-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="f5da7-106">Přestože Common Data Service nemá koncept organizační hierarchie, má několik volných konceptů, například celkový výnos z prodeje.</span><span class="sxs-lookup"><span data-stu-id="f5da7-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="f5da7-107">Jako součást integrace Common Data Service je do Common Data Service přidána datová struktura hierarchie organizací.</span><span class="sxs-lookup"><span data-stu-id="f5da7-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="f5da7-108">Tok dat</span><span class="sxs-lookup"><span data-stu-id="f5da7-108">Data flow</span></span>

<span data-ttu-id="f5da7-109">Podnikatelský ekosystém, který se skládá z aplikací Finance and Operations a Common Data Service bude nadále mít hierarchii organizací.</span><span class="sxs-lookup"><span data-stu-id="f5da7-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="f5da7-110">Tato hierarchie organizací je postavena na aplikacích Finance and Operations, ale je zpřístupněna v Common Data Service pro informační účely a účely rozšiřitelnosti.</span><span class="sxs-lookup"><span data-stu-id="f5da7-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="f5da7-111">Následující ilustrace znázorňuje informace o hierarchii organizace, které jsou vystaveny v Common Data Service jako jednosměrný tok dat z aplikací Finance and Operations do Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f5da7-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Obrázek architektury](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="f5da7-113">Šablony</span><span class="sxs-lookup"><span data-stu-id="f5da7-113">Templates</span></span>

<span data-ttu-id="f5da7-114">Mapování entity organizační hierarchie jsou k dispozici pro jednosměrnou synchronizaci dat z aplikací Finance and Operations do Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f5da7-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="f5da7-115">Interní účel hierarchie organizací</span><span class="sxs-lookup"><span data-stu-id="f5da7-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="f5da7-116">Tato šablona poskytuje jednosměrnou synchronizaci entity účel hierarchie organizace z Finance and Operations do dalších aplikací Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f5da7-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="f5da7-117">Zdrojové pole</span><span class="sxs-lookup"><span data-stu-id="f5da7-117">Source field</span></span> | <span data-ttu-id="f5da7-118">Typ mapování</span><span class="sxs-lookup"><span data-stu-id="f5da7-118">Map type</span></span> | <span data-ttu-id="f5da7-119">Cílové pole</span><span class="sxs-lookup"><span data-stu-id="f5da7-119">Destination field</span></span>
---|---|---
<span data-ttu-id="f5da7-120">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="f5da7-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="f5da7-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="f5da7-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="f5da7-122">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="f5da7-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="f5da7-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="f5da7-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="f5da7-124">HIERARCHYPURPOSE</span><span class="sxs-lookup"><span data-stu-id="f5da7-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="f5da7-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="f5da7-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="f5da7-126">IMMUTABLE</span><span class="sxs-lookup"><span data-stu-id="f5da7-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="f5da7-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="f5da7-127">msdyn\_immutable</span></span>
<span data-ttu-id="f5da7-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="f5da7-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="f5da7-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="f5da7-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="f5da7-130">Typ interní organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="f5da7-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="f5da7-131">Tato šablona poskytuje jednosměrnou synchronizaci entity Typ hierarchie organizace z Finance and Operations do dalších aplikací Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f5da7-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="f5da7-132">Zdrojové pole</span><span class="sxs-lookup"><span data-stu-id="f5da7-132">Source field</span></span> | <span data-ttu-id="f5da7-133">Typ mapování</span><span class="sxs-lookup"><span data-stu-id="f5da7-133">Map type</span></span> | <span data-ttu-id="f5da7-134">Cílové pole</span><span class="sxs-lookup"><span data-stu-id="f5da7-134">Destination field</span></span>
---|---|---
<span data-ttu-id="f5da7-135">NÁZEV</span><span class="sxs-lookup"><span data-stu-id="f5da7-135">NAME</span></span> | \> | <span data-ttu-id="f5da7-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="f5da7-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="f5da7-137">Interní organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="f5da7-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="f5da7-138">Tato šablona poskytuje jednosměrnou synchronizaci entity Publikovaná hierarchie organizace z Finance and Operations do dalších aplikací Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f5da7-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="f5da7-139">Zdrojové pole</span><span class="sxs-lookup"><span data-stu-id="f5da7-139">Source field</span></span> | <span data-ttu-id="f5da7-140">Typ mapování</span><span class="sxs-lookup"><span data-stu-id="f5da7-140">Map type</span></span> | <span data-ttu-id="f5da7-141">Cílové pole</span><span class="sxs-lookup"><span data-stu-id="f5da7-141">Destination field</span></span>
---|---|---
<span data-ttu-id="f5da7-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="f5da7-142">VALIDTO</span></span> | \> | <span data-ttu-id="f5da7-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="f5da7-143">msdyn\_validto</span></span>
<span data-ttu-id="f5da7-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="f5da7-144">VALIDFROM</span></span> | \> | <span data-ttu-id="f5da7-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="f5da7-145">msdyn\_validfrom</span></span>
<span data-ttu-id="f5da7-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="f5da7-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="f5da7-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="f5da7-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="f5da7-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="f5da7-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="f5da7-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="f5da7-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="f5da7-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="f5da7-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="f5da7-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="f5da7-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="f5da7-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="f5da7-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="f5da7-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="f5da7-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="f5da7-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="f5da7-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="f5da7-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="f5da7-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="f5da7-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="f5da7-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="f5da7-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="f5da7-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="f5da7-158">Interní organizace</span><span class="sxs-lookup"><span data-stu-id="f5da7-158">Internal Organization</span></span>

<span data-ttu-id="f5da7-159">Informace o interní organizaci v Common Data Service pocházejí ze dvou entit, **provozní jednotka** a **právnická osoba**.</span><span class="sxs-lookup"><span data-stu-id="f5da7-159">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="f5da7-160">Provozní jednotka</span><span class="sxs-lookup"><span data-stu-id="f5da7-160">Operating unit</span></span>

<span data-ttu-id="f5da7-161">Zdrojové pole</span><span class="sxs-lookup"><span data-stu-id="f5da7-161">Source field</span></span> | <span data-ttu-id="f5da7-162">Typ mapování</span><span class="sxs-lookup"><span data-stu-id="f5da7-162">Map type</span></span> | <span data-ttu-id="f5da7-163">Cílové pole</span><span class="sxs-lookup"><span data-stu-id="f5da7-163">Destination field</span></span>
---|---|---
<span data-ttu-id="f5da7-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="f5da7-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="f5da7-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="f5da7-165">msdyn\_languageid</span></span>
<span data-ttu-id="f5da7-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="f5da7-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="f5da7-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="f5da7-167">msdyn\_namealias</span></span>
<span data-ttu-id="f5da7-168">NÁZEV</span><span class="sxs-lookup"><span data-stu-id="f5da7-168">NAME</span></span> | \> | <span data-ttu-id="f5da7-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="f5da7-169">msdyn\_name</span></span>
<span data-ttu-id="f5da7-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="f5da7-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="f5da7-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="f5da7-171">msdyn\_partynumber</span></span>
<span data-ttu-id="f5da7-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="f5da7-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="f5da7-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="f5da7-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="f5da7-174">Právnická osoba</span><span class="sxs-lookup"><span data-stu-id="f5da7-174">Legal entity</span></span>

<span data-ttu-id="f5da7-175">Zdrojové pole</span><span class="sxs-lookup"><span data-stu-id="f5da7-175">Source field</span></span> | <span data-ttu-id="f5da7-176">Typ mapování</span><span class="sxs-lookup"><span data-stu-id="f5da7-176">Map type</span></span> | <span data-ttu-id="f5da7-177">Cílové pole</span><span class="sxs-lookup"><span data-stu-id="f5da7-177">Destination field</span></span>
---|---|---
<span data-ttu-id="f5da7-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="f5da7-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="f5da7-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="f5da7-179">msdyn\_namealias</span></span>
<span data-ttu-id="f5da7-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="f5da7-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="f5da7-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="f5da7-181">msdyn\_languageid</span></span>
<span data-ttu-id="f5da7-182">NÁZEV</span><span class="sxs-lookup"><span data-stu-id="f5da7-182">NAME</span></span> | \> | <span data-ttu-id="f5da7-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="f5da7-183">msdyn\_name</span></span>
<span data-ttu-id="f5da7-184">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="f5da7-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="f5da7-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="f5da7-185">msdyn\_partynumber</span></span>
<span data-ttu-id="f5da7-186">žádná</span><span class="sxs-lookup"><span data-stu-id="f5da7-186">none</span></span> | \>\> | <span data-ttu-id="f5da7-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="f5da7-187">msdyn\_type</span></span>
<span data-ttu-id="f5da7-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="f5da7-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="f5da7-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="f5da7-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="f5da7-190">Společnost</span><span class="sxs-lookup"><span data-stu-id="f5da7-190">Company</span></span>

<span data-ttu-id="f5da7-191">Poskytuje obousměrnou synchronizaci informací o právnické osobě (společnosti) mezi Finance and Operations a dalšími aplikacemi Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f5da7-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="f5da7-192">Zdrojové pole</span><span class="sxs-lookup"><span data-stu-id="f5da7-192">Source field</span></span> | <span data-ttu-id="f5da7-193">Typ mapování</span><span class="sxs-lookup"><span data-stu-id="f5da7-193">Map type</span></span> | <span data-ttu-id="f5da7-194">Cílové pole</span><span class="sxs-lookup"><span data-stu-id="f5da7-194">Destination field</span></span>
---|---|---
<span data-ttu-id="f5da7-195">NÁZEV</span><span class="sxs-lookup"><span data-stu-id="f5da7-195">NAME</span></span> | = | <span data-ttu-id="f5da7-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="f5da7-196">cdm\_name</span></span>
<span data-ttu-id="f5da7-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="f5da7-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="f5da7-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="f5da7-198">cdm\_companycode</span></span>
