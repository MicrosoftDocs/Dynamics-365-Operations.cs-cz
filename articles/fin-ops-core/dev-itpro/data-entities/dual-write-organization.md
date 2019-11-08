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
ms.openlocfilehash: 9a12ab249129dce24cdca5e29d737fa9f68c0eac
ms.sourcegitcommit: 6e0909e95f38b7487a4b7f68cc62b723f8b59bd4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572442"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="32c65-103">Organizační hierarchie v Common Data Service</span><span class="sxs-lookup"><span data-stu-id="32c65-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="32c65-104">Vzhledem k tomu, že Dynamics 365 Finance, je finanční systém, *organizace* je hlavním konceptem a nastavení systému začíná konfigurací hierarchie organizací.</span><span class="sxs-lookup"><span data-stu-id="32c65-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="32c65-105">Obchodní finance lze poté sledovat na úrovni organizace a také na libovolné úrovni v hierarchii organizací.</span><span class="sxs-lookup"><span data-stu-id="32c65-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="32c65-106">Přestože Common Data Service nemá koncept organizační hierarchie, má několik volných konceptů, například celkový výnos z prodeje.</span><span class="sxs-lookup"><span data-stu-id="32c65-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="32c65-107">Jako součást integrace Common Data Service je do Common Data Service přidána datová struktura hierarchie organizací.</span><span class="sxs-lookup"><span data-stu-id="32c65-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="32c65-108">Tok dat</span><span class="sxs-lookup"><span data-stu-id="32c65-108">Data flow</span></span>

<span data-ttu-id="32c65-109">Podnikatelský ekosystém, který se skládá z aplikací Finance and Operations a Common Data Service bude nadále mít hierarchii organizací.</span><span class="sxs-lookup"><span data-stu-id="32c65-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="32c65-110">Tato hierarchie organizací je postavena na aplikacích Finance and Operations, ale je zpřístupněna v Common Data Service pro informační účely a účely rozšiřitelnosti.</span><span class="sxs-lookup"><span data-stu-id="32c65-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="32c65-111">Následující ilustrace znázorňuje informace o hierarchii organizace, které jsou vystaveny v Common Data Service jako jednosměrný tok dat z aplikací Finance and Operations do Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="32c65-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Obrázek architektury](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="32c65-113">Šablony</span><span class="sxs-lookup"><span data-stu-id="32c65-113">Templates</span></span>

<span data-ttu-id="32c65-114">Mapování entity organizační hierarchie jsou k dispozici pro jednosměrnou synchronizaci dat z aplikací Finance and Operations do Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="32c65-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="32c65-115">Interní účel hierarchie organizací</span><span class="sxs-lookup"><span data-stu-id="32c65-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="32c65-116">Tato šablona poskytuje jednosměrnou synchronizaci entity účel hierarchie organizace z Finance and Operations do dalších aplikací Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="32c65-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="32c65-117">Zdrojové pole</span><span class="sxs-lookup"><span data-stu-id="32c65-117">Source field</span></span> | <span data-ttu-id="32c65-118">Typ mapování</span><span class="sxs-lookup"><span data-stu-id="32c65-118">Map type</span></span> | <span data-ttu-id="32c65-119">Cílové pole</span><span class="sxs-lookup"><span data-stu-id="32c65-119">Destination field</span></span>
---|---|---
<span data-ttu-id="32c65-120">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="32c65-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="32c65-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="32c65-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="32c65-122">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="32c65-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="32c65-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="32c65-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="32c65-124">HIERARCHYPURPOSE</span><span class="sxs-lookup"><span data-stu-id="32c65-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="32c65-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="32c65-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="32c65-126">IMMUTABLE</span><span class="sxs-lookup"><span data-stu-id="32c65-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="32c65-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="32c65-127">msdyn\_immutable</span></span>
<span data-ttu-id="32c65-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="32c65-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="32c65-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="32c65-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="32c65-130">Typ interní organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="32c65-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="32c65-131">Tato šablona poskytuje jednosměrnou synchronizaci entity Typ hierarchie organizace z Finance and Operations do dalších aplikací Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="32c65-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="32c65-132">Zdrojové pole</span><span class="sxs-lookup"><span data-stu-id="32c65-132">Source field</span></span> | <span data-ttu-id="32c65-133">Typ mapování</span><span class="sxs-lookup"><span data-stu-id="32c65-133">Map type</span></span> | <span data-ttu-id="32c65-134">Cílové pole</span><span class="sxs-lookup"><span data-stu-id="32c65-134">Destination field</span></span>
---|---|---
<span data-ttu-id="32c65-135">NÁZEV</span><span class="sxs-lookup"><span data-stu-id="32c65-135">NAME</span></span> | \> | <span data-ttu-id="32c65-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="32c65-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="32c65-137">Interní organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="32c65-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="32c65-138">Tato šablona poskytuje jednosměrnou synchronizaci entity Publikovaná hierarchie organizace z Finance and Operations do dalších aplikací Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="32c65-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="32c65-139">Zdrojové pole</span><span class="sxs-lookup"><span data-stu-id="32c65-139">Source field</span></span> | <span data-ttu-id="32c65-140">Typ mapování</span><span class="sxs-lookup"><span data-stu-id="32c65-140">Map type</span></span> | <span data-ttu-id="32c65-141">Cílové pole</span><span class="sxs-lookup"><span data-stu-id="32c65-141">Destination field</span></span>
---|---|---
<span data-ttu-id="32c65-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="32c65-142">VALIDTO</span></span> | \> | <span data-ttu-id="32c65-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="32c65-143">msdyn\_validto</span></span>
<span data-ttu-id="32c65-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="32c65-144">VALIDFROM</span></span> | \> | <span data-ttu-id="32c65-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="32c65-145">msdyn\_validfrom</span></span>
<span data-ttu-id="32c65-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="32c65-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="32c65-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="32c65-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="32c65-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="32c65-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="32c65-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="32c65-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="32c65-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="32c65-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="32c65-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="32c65-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="32c65-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="32c65-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="32c65-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="32c65-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="32c65-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="32c65-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="32c65-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="32c65-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="32c65-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="32c65-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="32c65-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="32c65-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="32c65-158">Interní organizace</span><span class="sxs-lookup"><span data-stu-id="32c65-158">Internal Organization</span></span>

<span data-ttu-id="32c65-159">Informace o interní organizaci v Common Data Service pocházejí ze dvou entit, **provozní jednotka** a **právnická osoba**.</span><span class="sxs-lookup"><span data-stu-id="32c65-159">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="32c65-160">Provozní jednotka</span><span class="sxs-lookup"><span data-stu-id="32c65-160">Operating unit</span></span>

<span data-ttu-id="32c65-161">Zdrojové pole</span><span class="sxs-lookup"><span data-stu-id="32c65-161">Source field</span></span> | <span data-ttu-id="32c65-162">Typ mapování</span><span class="sxs-lookup"><span data-stu-id="32c65-162">Map type</span></span> | <span data-ttu-id="32c65-163">Cílové pole</span><span class="sxs-lookup"><span data-stu-id="32c65-163">Destination field</span></span>
---|---|---
<span data-ttu-id="32c65-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="32c65-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="32c65-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="32c65-165">msdyn\_languageid</span></span>
<span data-ttu-id="32c65-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="32c65-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="32c65-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="32c65-167">msdyn\_namealias</span></span>
<span data-ttu-id="32c65-168">NÁZEV</span><span class="sxs-lookup"><span data-stu-id="32c65-168">NAME</span></span> | \> | <span data-ttu-id="32c65-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="32c65-169">msdyn\_name</span></span>
<span data-ttu-id="32c65-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="32c65-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="32c65-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="32c65-171">msdyn\_partynumber</span></span>
<span data-ttu-id="32c65-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="32c65-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="32c65-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="32c65-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="32c65-174">Právnická osoba</span><span class="sxs-lookup"><span data-stu-id="32c65-174">Legal entity</span></span>

<span data-ttu-id="32c65-175">Zdrojové pole</span><span class="sxs-lookup"><span data-stu-id="32c65-175">Source field</span></span> | <span data-ttu-id="32c65-176">Typ mapování</span><span class="sxs-lookup"><span data-stu-id="32c65-176">Map type</span></span> | <span data-ttu-id="32c65-177">Cílové pole</span><span class="sxs-lookup"><span data-stu-id="32c65-177">Destination field</span></span>
---|---|---
<span data-ttu-id="32c65-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="32c65-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="32c65-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="32c65-179">msdyn\_namealias</span></span>
<span data-ttu-id="32c65-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="32c65-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="32c65-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="32c65-181">msdyn\_languageid</span></span>
<span data-ttu-id="32c65-182">NÁZEV</span><span class="sxs-lookup"><span data-stu-id="32c65-182">NAME</span></span> | \> | <span data-ttu-id="32c65-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="32c65-183">msdyn\_name</span></span>
<span data-ttu-id="32c65-184">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="32c65-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="32c65-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="32c65-185">msdyn\_partynumber</span></span>
<span data-ttu-id="32c65-186">žádná</span><span class="sxs-lookup"><span data-stu-id="32c65-186">none</span></span> | \>\> | <span data-ttu-id="32c65-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="32c65-187">msdyn\_type</span></span>
<span data-ttu-id="32c65-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="32c65-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="32c65-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="32c65-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="32c65-190">Společnost</span><span class="sxs-lookup"><span data-stu-id="32c65-190">Company</span></span>

<span data-ttu-id="32c65-191">Poskytuje obousměrnou synchronizaci informací o právnické osobě (společnosti) mezi Finance and Operations a dalšími aplikacemi Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="32c65-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="32c65-192">Zdrojové pole</span><span class="sxs-lookup"><span data-stu-id="32c65-192">Source field</span></span> | <span data-ttu-id="32c65-193">Typ mapování</span><span class="sxs-lookup"><span data-stu-id="32c65-193">Map type</span></span> | <span data-ttu-id="32c65-194">Cílové pole</span><span class="sxs-lookup"><span data-stu-id="32c65-194">Destination field</span></span>
---|---|---
<span data-ttu-id="32c65-195">NÁZEV</span><span class="sxs-lookup"><span data-stu-id="32c65-195">NAME</span></span> | = | <span data-ttu-id="32c65-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="32c65-196">cdm\_name</span></span>
<span data-ttu-id="32c65-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="32c65-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="32c65-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="32c65-198">cdm\_companycode</span></span>
