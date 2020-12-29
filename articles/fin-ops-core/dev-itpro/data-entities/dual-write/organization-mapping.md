---
title: Organizační hierarchie v Dataverse
description: Toto téma popisuje integraci dat organizace mezi aplikacemi Finance and Operations a Dataverse.
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
ms.openlocfilehash: e2b652f11db62eb58ffc2ec2fc4322149e7d45d1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680065"
---
# <a name="organization-hierarchy-in-dataverse"></a><span data-ttu-id="a8664-103">Organizační hierarchie v Dataverse</span><span class="sxs-lookup"><span data-stu-id="a8664-103">Organization hierarchy in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a8664-104">Vzhledem k tomu, že Dynamics 365 Finance, je finanční systém, *organizace* je hlavním konceptem a nastavení systému začíná konfigurací hierarchie organizací.</span><span class="sxs-lookup"><span data-stu-id="a8664-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="a8664-105">Obchodní finance lze poté sledovat na úrovni organizace a také na libovolné úrovni v hierarchii organizací.</span><span class="sxs-lookup"><span data-stu-id="a8664-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="a8664-106">Přestože Dataverse nemá koncept organizační hierarchie, má několik volných konceptů, například celkový výnos z prodeje.</span><span class="sxs-lookup"><span data-stu-id="a8664-106">Although Dataverse doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="a8664-107">Jako součást integrace Dataverse je do Dataverse přidána datová struktura hierarchie organizací.</span><span class="sxs-lookup"><span data-stu-id="a8664-107">As part of Dataverse integration, the organization hierarchy data structure is added to Dataverse.</span></span>

## <a name="data-flow"></a><span data-ttu-id="a8664-108">Tok dat</span><span class="sxs-lookup"><span data-stu-id="a8664-108">Data flow</span></span>

<span data-ttu-id="a8664-109">Podnikatelský ekosystém, který se skládá z aplikací Finance and Operations a Dataverse, bude nadále mít hierarchii organizací.</span><span class="sxs-lookup"><span data-stu-id="a8664-109">A business ecosystem that consists of Finance and Operations apps and Dataverse will continue to have an organization hierarchy.</span></span> <span data-ttu-id="a8664-110">Tato hierarchie organizací je postavena na aplikacích Finance and Operations, ale je zpřístupněna v Dataverse pro informační účely a účely rozšiřitelnosti.</span><span class="sxs-lookup"><span data-stu-id="a8664-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Dataverse for informational and extensibility purposes.</span></span> <span data-ttu-id="a8664-111">Následující ilustrace znázorňuje informace o hierarchii organizace, které jsou vystaveny v Dataverse jako jednosměrný tok dat z aplikací Finance and Operations do Dataverse.</span><span class="sxs-lookup"><span data-stu-id="a8664-111">The following illustration shows the organization hierarchy information that is exposed in Dataverse as a one-way data flow from Finance and Operations apps to Dataverse.</span></span>

![Obrázek architektury](media/dual-write-data-flow.png)

<span data-ttu-id="a8664-113">Mapování tabulky organizační hierarchie je k dispozici pro jednosměrnou synchronizaci dat z aplikací Finance and Operations do Dataverse.</span><span class="sxs-lookup"><span data-stu-id="a8664-113">Organization hierarchy table maps are available for one-way synchronization of data from Finance and Operations apps to Dataverse.</span></span>

## <a name="templates"></a><span data-ttu-id="a8664-114">Šablony</span><span class="sxs-lookup"><span data-stu-id="a8664-114">Templates</span></span>

<span data-ttu-id="a8664-115">Informace o produktu obsahují všechny informace související s produktem a jeho definici, jako jsou například dimenze produktů nebo dimenze sledování a úložiště.</span><span class="sxs-lookup"><span data-stu-id="a8664-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="a8664-116">Jak je ukázáno v následující tabulce, je vytvořena kolekce map tabulek pro synchronizaci produktů a souvisejících informací.</span><span class="sxs-lookup"><span data-stu-id="a8664-116">As the following table shows, a collection of table maps is created to sync products and related information.</span></span>

<span data-ttu-id="a8664-117">Aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a8664-117">Finance and Operations apps</span></span> | <span data-ttu-id="a8664-118">Jiné aplikace Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a8664-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="a8664-119">popis</span><span class="sxs-lookup"><span data-stu-id="a8664-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="a8664-120">Účely organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="a8664-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="a8664-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="a8664-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="a8664-122">Tato šablona poskytuje jednosměrnou synchronizaci entity účelu hierarchie organizace.</span><span class="sxs-lookup"><span data-stu-id="a8664-122">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="a8664-123">Typ organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="a8664-123">Organization hierarchy type</span></span> | <span data-ttu-id="a8664-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="a8664-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="a8664-125">Tato šablona poskytuje jednosměrnou synchronizaci entity typu hierarchie organizace.</span><span class="sxs-lookup"><span data-stu-id="a8664-125">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="a8664-126">Organizační hierarchie - publikovaná</span><span class="sxs-lookup"><span data-stu-id="a8664-126">Organization hierarchy - published</span></span> | <span data-ttu-id="a8664-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="a8664-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="a8664-128">Tato šablona poskytuje jednosměrnou synchronizaci entity publikované hierarchie organizace.</span><span class="sxs-lookup"><span data-stu-id="a8664-128">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="a8664-129">Provozní jednotka</span><span class="sxs-lookup"><span data-stu-id="a8664-129">Operating unit</span></span> | <span data-ttu-id="a8664-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="a8664-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="a8664-131">Právnické osoby</span><span class="sxs-lookup"><span data-stu-id="a8664-131">Legal entities</span></span> | <span data-ttu-id="a8664-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="a8664-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="a8664-133">Právnické osoby</span><span class="sxs-lookup"><span data-stu-id="a8664-133">Legal entities</span></span> | <span data-ttu-id="a8664-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="a8664-134">cdm_companies</span></span> | <span data-ttu-id="a8664-135">Poskytuje obousměrnou synchronizaci informací o právnické osobě (společnosti).</span><span class="sxs-lookup"><span data-stu-id="a8664-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="a8664-136">Interní organizace</span><span class="sxs-lookup"><span data-stu-id="a8664-136">Internal Organization</span></span>

<span data-ttu-id="a8664-137">Informace o interní organizaci v Dataverse pocházejí ze dvou tabulek, **provozní jednotka** a **právnická osoba**.</span><span class="sxs-lookup"><span data-stu-id="a8664-137">Internal organization information in Dataverse comes from two tables, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]
