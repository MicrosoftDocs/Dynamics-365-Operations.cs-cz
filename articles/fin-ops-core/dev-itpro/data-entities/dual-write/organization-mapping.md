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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: f502519ba419cb8fa322eb1d22f06d2b805f5f05
ms.sourcegitcommit: afc43699c0edc4ff2be310cb37add2ab586b64c0
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/14/2020
ms.locfileid: "4000727"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="60241-103">Organizační hierarchie v Common Data Service</span><span class="sxs-lookup"><span data-stu-id="60241-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="60241-104">Vzhledem k tomu, že Dynamics 365 Finance, je finanční systém, *organizace* je hlavním konceptem a nastavení systému začíná konfigurací hierarchie organizací.</span><span class="sxs-lookup"><span data-stu-id="60241-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="60241-105">Obchodní finance lze poté sledovat na úrovni organizace a také na libovolné úrovni v hierarchii organizací.</span><span class="sxs-lookup"><span data-stu-id="60241-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="60241-106">Přestože Common Data Service nemá koncept organizační hierarchie, má několik volných konceptů, například celkový výnos z prodeje.</span><span class="sxs-lookup"><span data-stu-id="60241-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="60241-107">Jako součást integrace Common Data Service je do Common Data Service přidána datová struktura hierarchie organizací.</span><span class="sxs-lookup"><span data-stu-id="60241-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="60241-108">Tok dat</span><span class="sxs-lookup"><span data-stu-id="60241-108">Data flow</span></span>

<span data-ttu-id="60241-109">Podnikatelský ekosystém, který se skládá z aplikací Finance and Operations a Common Data Service, bude nadále mít hierarchii organizací.</span><span class="sxs-lookup"><span data-stu-id="60241-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="60241-110">Tato hierarchie organizací je postavena na aplikacích Finance and Operations, ale je zpřístupněna v Common Data Service pro informační účely a účely rozšiřitelnosti.</span><span class="sxs-lookup"><span data-stu-id="60241-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="60241-111">Následující ilustrace znázorňuje informace o hierarchii organizace, které jsou vystaveny v Common Data Service jako jednosměrný tok dat z aplikací Finance and Operations do Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="60241-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Obrázek architektury](media/dual-write-data-flow.png)

<span data-ttu-id="60241-113">Mapování entity organizační hierarchie jsou k dispozici pro jednosměrnou synchronizaci dat z aplikací Finance and Operations do Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="60241-113">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

## <a name="templates"></a><span data-ttu-id="60241-114">Šablony</span><span class="sxs-lookup"><span data-stu-id="60241-114">Templates</span></span>

<span data-ttu-id="60241-115">Informace o produktu obsahují všechny informace související s produktem a jeho definici, jako jsou například dimenze produktů nebo dimenze sledování a úložiště.</span><span class="sxs-lookup"><span data-stu-id="60241-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="60241-116">Jak je ukázáno v následující tabulce, je vytvořena kolekce map entit pro synchronizaci produktů a souvisejících informací.</span><span class="sxs-lookup"><span data-stu-id="60241-116">As the following table shows, a collection of entity maps is created to sync products and related information.</span></span>

<span data-ttu-id="60241-117">Aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="60241-117">Finance and Operations apps</span></span> | <span data-ttu-id="60241-118">Jiné aplikace Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="60241-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="60241-119">popis</span><span class="sxs-lookup"><span data-stu-id="60241-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="60241-120">Účely organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="60241-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="60241-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="60241-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="60241-122">Tato šablona poskytuje jednosměrnou synchronizaci entity účelu hierarchie organizace.</span><span class="sxs-lookup"><span data-stu-id="60241-122">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="60241-123">Typ organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="60241-123">Organization hierarchy type</span></span> | <span data-ttu-id="60241-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="60241-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="60241-125">Tato šablona poskytuje jednosměrnou synchronizaci entity typu hierarchie organizace.</span><span class="sxs-lookup"><span data-stu-id="60241-125">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="60241-126">Organizační hierarchie - publikovaná</span><span class="sxs-lookup"><span data-stu-id="60241-126">Organization hierarchy - published</span></span> | <span data-ttu-id="60241-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="60241-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="60241-128">Tato šablona poskytuje jednosměrnou synchronizaci entity publikované hierarchie organizace.</span><span class="sxs-lookup"><span data-stu-id="60241-128">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="60241-129">Provozní jednotka</span><span class="sxs-lookup"><span data-stu-id="60241-129">Operating unit</span></span> | <span data-ttu-id="60241-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="60241-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="60241-131">Právnické osoby</span><span class="sxs-lookup"><span data-stu-id="60241-131">Legal entities</span></span> | <span data-ttu-id="60241-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="60241-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="60241-133">Právnické osoby</span><span class="sxs-lookup"><span data-stu-id="60241-133">Legal entities</span></span> | <span data-ttu-id="60241-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="60241-134">cdm_companies</span></span> | <span data-ttu-id="60241-135">Poskytuje obousměrnou synchronizaci informací o právnické osobě (společnosti).</span><span class="sxs-lookup"><span data-stu-id="60241-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="60241-136">Interní organizace</span><span class="sxs-lookup"><span data-stu-id="60241-136">Internal Organization</span></span>

<span data-ttu-id="60241-137">Informace o interní organizaci v Common Data Service pocházejí ze dvou entit, **provozní jednotka** a **právnická osoba**.</span><span class="sxs-lookup"><span data-stu-id="60241-137">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]
