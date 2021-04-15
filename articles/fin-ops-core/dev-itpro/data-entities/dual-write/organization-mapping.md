---
title: Organizační hierarchie v Dataverse
description: Toto téma popisuje integraci dat organizace mezi aplikacemi Finance and Operations a Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8b147c27b9309b1b3597f1194c415fbb2e2b7ad2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750805"
---
# <a name="organization-hierarchy-in-dataverse"></a><span data-ttu-id="f3eae-103">Organizační hierarchie v Dataverse</span><span class="sxs-lookup"><span data-stu-id="f3eae-103">Organization hierarchy in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f3eae-104">Vzhledem k tomu, že Dynamics 365 Finance, je finanční systém, *organizace* je hlavním konceptem a nastavení systému začíná konfigurací hierarchie organizací.</span><span class="sxs-lookup"><span data-stu-id="f3eae-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="f3eae-105">Obchodní finance lze poté sledovat na úrovni organizace a také na libovolné úrovni v hierarchii organizací.</span><span class="sxs-lookup"><span data-stu-id="f3eae-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="f3eae-106">Přestože Dataverse nemá koncept organizační hierarchie, má několik volných konceptů, například celkový výnos z prodeje.</span><span class="sxs-lookup"><span data-stu-id="f3eae-106">Although Dataverse doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="f3eae-107">Jako součást integrace Dataverse je do Dataverse přidána datová struktura hierarchie organizací.</span><span class="sxs-lookup"><span data-stu-id="f3eae-107">As part of Dataverse integration, the organization hierarchy data structure is added to Dataverse.</span></span>

## <a name="data-flow"></a><span data-ttu-id="f3eae-108">Tok dat</span><span class="sxs-lookup"><span data-stu-id="f3eae-108">Data flow</span></span>

<span data-ttu-id="f3eae-109">Podnikatelský ekosystém, který se skládá z aplikací Finance and Operations a Dataverse, bude nadále mít hierarchii organizací.</span><span class="sxs-lookup"><span data-stu-id="f3eae-109">A business ecosystem that consists of Finance and Operations apps and Dataverse will continue to have an organization hierarchy.</span></span> <span data-ttu-id="f3eae-110">Tato hierarchie organizací je postavena na aplikacích Finance and Operations, ale je zpřístupněna v Dataverse pro informační účely a účely rozšiřitelnosti.</span><span class="sxs-lookup"><span data-stu-id="f3eae-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Dataverse for informational and extensibility purposes.</span></span> <span data-ttu-id="f3eae-111">Následující ilustrace znázorňuje informace o hierarchii organizace, které jsou vystaveny v Dataverse jako jednosměrný tok dat z aplikací Finance and Operations do Dataverse.</span><span class="sxs-lookup"><span data-stu-id="f3eae-111">The following illustration shows the organization hierarchy information that is exposed in Dataverse as a one-way data flow from Finance and Operations apps to Dataverse.</span></span>

![Obrázek architektury](media/dual-write-data-flow.png)

<span data-ttu-id="f3eae-113">Mapování tabulky organizační hierarchie je k dispozici pro jednosměrnou synchronizaci dat z aplikací Finance and Operations do Dataverse.</span><span class="sxs-lookup"><span data-stu-id="f3eae-113">Organization hierarchy table maps are available for one-way synchronization of data from Finance and Operations apps to Dataverse.</span></span>

## <a name="templates"></a><span data-ttu-id="f3eae-114">Šablony</span><span class="sxs-lookup"><span data-stu-id="f3eae-114">Templates</span></span>

<span data-ttu-id="f3eae-115">Informace o produktu obsahují všechny informace související s produktem a jeho definici, jako jsou například dimenze produktů nebo dimenze sledování a úložiště.</span><span class="sxs-lookup"><span data-stu-id="f3eae-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="f3eae-116">Jak je ukázáno v následující tabulce, je vytvořena kolekce map tabulek pro synchronizaci produktů a souvisejících informací.</span><span class="sxs-lookup"><span data-stu-id="f3eae-116">As the following table shows, a collection of table maps is created to sync products and related information.</span></span>

<span data-ttu-id="f3eae-117">Aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f3eae-117">Finance and Operations apps</span></span> | <span data-ttu-id="f3eae-118">Jiné aplikace Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="f3eae-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="f3eae-119">popis</span><span class="sxs-lookup"><span data-stu-id="f3eae-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="f3eae-120">Účely organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="f3eae-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="f3eae-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="f3eae-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="f3eae-122">Tato šablona poskytuje jednosměrnou synchronizaci tabulky účelu hierarchie organizace.</span><span class="sxs-lookup"><span data-stu-id="f3eae-122">This template provides one-way synchronization of the Organization Hierarchy Purpose table.</span></span>
<span data-ttu-id="f3eae-123">Typ organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="f3eae-123">Organization hierarchy type</span></span> | <span data-ttu-id="f3eae-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="f3eae-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="f3eae-125">Tato šablona poskytuje jednosměrnou synchronizaci tabulky typu hierarchie organizace.</span><span class="sxs-lookup"><span data-stu-id="f3eae-125">This template provides one-way synchronization of the Organization Hierarchy Type table.</span></span>
<span data-ttu-id="f3eae-126">Organizační hierarchie - publikovaná</span><span class="sxs-lookup"><span data-stu-id="f3eae-126">Organization hierarchy - published</span></span> | <span data-ttu-id="f3eae-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="f3eae-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="f3eae-128">Tato šablona poskytuje jednosměrnou synchronizaci tabulky publikované hierarchie organizace.</span><span class="sxs-lookup"><span data-stu-id="f3eae-128">This template provides one-way synchronization of the Organization Hierarchy Published table.</span></span>
<span data-ttu-id="f3eae-129">Provozní jednotka</span><span class="sxs-lookup"><span data-stu-id="f3eae-129">Operating unit</span></span> | <span data-ttu-id="f3eae-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="f3eae-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="f3eae-131">Právnické osoby</span><span class="sxs-lookup"><span data-stu-id="f3eae-131">Legal entities</span></span> | <span data-ttu-id="f3eae-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="f3eae-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="f3eae-133">Právnické osoby</span><span class="sxs-lookup"><span data-stu-id="f3eae-133">Legal entities</span></span> | <span data-ttu-id="f3eae-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="f3eae-134">cdm_companies</span></span> | <span data-ttu-id="f3eae-135">Poskytuje obousměrnou synchronizaci informací o právnické osobě (společnosti).</span><span class="sxs-lookup"><span data-stu-id="f3eae-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="f3eae-136">Interní organizace</span><span class="sxs-lookup"><span data-stu-id="f3eae-136">Internal Organization</span></span>

<span data-ttu-id="f3eae-137">Informace o interní organizaci v Dataverse pocházejí ze dvou tabulek, **provozní jednotka** a **právnická osoba**.</span><span class="sxs-lookup"><span data-stu-id="f3eae-137">Internal organization information in Dataverse comes from two tables, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]