---
title: Interní majetek pro údržbu
description: Toto téma popisuje, jak můžete použít Microsoft Dynamics 365 Field Service k obsluze aktiv zákazníků i interních aktiv.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
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
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: ebda6b5679ec601513fb6d046725b396e69fe0f3
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941407"
---
# <a name="in-house-assets-for-servicing"></a><span data-ttu-id="c2560-103">Interní majetek pro údržbu</span><span class="sxs-lookup"><span data-stu-id="c2560-103">In-house assets for servicing</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="c2560-104">Aplikace Microsoft Dynamics 365 Field Service je navržena pro poskytnutí servisu majetku zákazníků.</span><span class="sxs-lookup"><span data-stu-id="c2560-104">Microsoft Dynamics 365 Field Service is designed to service customer assets.</span></span> <span data-ttu-id="c2560-105">Správa majetku pro Dynamics 365 Supply Chain Management je navržena pro údržbu interního majetku.</span><span class="sxs-lookup"><span data-stu-id="c2560-105">Asset management for Dynamics 365 Supply Chain Management is designed to maintain in-house assets.</span></span> <span data-ttu-id="c2560-106">Integrace těchto dvou aplikací umožňuje používat službu Field Service k poskytnutí servisu pro majetek zákazníků i interního majetku.</span><span class="sxs-lookup"><span data-stu-id="c2560-106">Integration of these two apps lets you use Field Service to service both customer assets and in-house assets.</span></span> <span data-ttu-id="c2560-107">Můžete také klasifikovat majetek na základě funkčního umístění nebo hierarchie a sledovat servis na podrobné úrovni.</span><span class="sxs-lookup"><span data-stu-id="c2560-107">You can also classify the assets, based on functional location or hierarchy, and track the servicing at a detailed level.</span></span>

<span data-ttu-id="c2560-108">Další informace naleznete v tématu [Integrace řešení Dynamics 365 Field Service a Supply Chain Management](/dynamics365/field-service/supply-chain-field-service-integration).</span><span class="sxs-lookup"><span data-stu-id="c2560-108">For more information, see [Integrate Dynamics 365 Field Service and Supply Chain Management](/dynamics365/field-service/supply-chain-field-service-integration).</span></span>

## <a name="templates"></a><span data-ttu-id="c2560-109">Šablony</span><span class="sxs-lookup"><span data-stu-id="c2560-109">Templates</span></span>

<span data-ttu-id="c2560-110">Interní majetek zahrnuje kolekci základních map tabulek, které pracují společně během interakce s daty zákazníka, jak je uvedeno v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="c2560-110">In-house-assets include a collection of core table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="c2560-111">Aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c2560-111">Finance and Operations apps</span></span> | <span data-ttu-id="c2560-112">Modelem řízené aplikace v Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="c2560-112">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="c2560-113">popis</span><span class="sxs-lookup"><span data-stu-id="c2560-113">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="c2560-114">Správa majetku – modely životního cyklu majetku</span><span class="sxs-lookup"><span data-stu-id="c2560-114">Asset management asset lifecycle models</span></span> | <span data-ttu-id="c2560-115">msdyn\_assetlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="c2560-115">msdyn\_assetlifecyclemodels</span></span> | |
| <span data-ttu-id="c2560-116">Správa majetku – stavy životního cyklu majetku</span><span class="sxs-lookup"><span data-stu-id="c2560-116">Asset management asset lifecycle states</span></span> | <span data-ttu-id="c2560-117">msdyn\_assetlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="c2560-117">msdyn\_assetlifecyclestates</span></span> | |
| <span data-ttu-id="c2560-118">Správa majetku – majetek</span><span class="sxs-lookup"><span data-stu-id="c2560-118">Asset management assets</span></span> | <span data-ttu-id="c2560-119">msdyn\_customerassets</span><span class="sxs-lookup"><span data-stu-id="c2560-119">msdyn\_customerassets</span></span> | |
| <span data-ttu-id="c2560-120">Správa majetku – typy majetku</span><span class="sxs-lookup"><span data-stu-id="c2560-120">Asset management asset types</span></span> | <span data-ttu-id="c2560-121">msdyn\_customerassetcategories</span><span class="sxs-lookup"><span data-stu-id="c2560-121">msdyn\_customerassetcategories</span></span> | |
| <span data-ttu-id="c2560-122">Správa majetku – funkční místa – modely životního cyklu</span><span class="sxs-lookup"><span data-stu-id="c2560-122">Asset management functional location lifecycle models</span></span> | <span data-ttu-id="c2560-123">msdyn\_functionallocationlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="c2560-123">msdyn\_functionallocationlifecyclemodels</span></span> | |
| <span data-ttu-id="c2560-124">Správa majetku – funkční místa – stavy životního cyklu</span><span class="sxs-lookup"><span data-stu-id="c2560-124">Asset management functional location lifecycle states</span></span> | <span data-ttu-id="c2560-125">msdyn\_functionallocationlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="c2560-125">msdyn\_functionallocationlifecyclestates</span></span> | |
| <span data-ttu-id="c2560-126">Správa majetku – funkční místa</span><span class="sxs-lookup"><span data-stu-id="c2560-126">Asset management functional locations</span></span> | <span data-ttu-id="c2560-127">msdyn\_functionallocations</span><span class="sxs-lookup"><span data-stu-id="c2560-127">msdyn\_functionallocations</span></span> | |
| <span data-ttu-id="c2560-128">Správa majetku – typy funkčních míst</span><span class="sxs-lookup"><span data-stu-id="c2560-128">Asset management functional location types</span></span> | <span data-ttu-id="c2560-129">msdyn\_functionallocationtypes</span><span class="sxs-lookup"><span data-stu-id="c2560-129">msdyn\_functionallocationtypes</span></span> | |
| <span data-ttu-id="c2560-130">Správa majetku – výrobci</span><span class="sxs-lookup"><span data-stu-id="c2560-130">Asset management manufacturers</span></span> | <span data-ttu-id="c2560-131">msdyn\_manufacturers</span><span class="sxs-lookup"><span data-stu-id="c2560-131">msdyn\_manufacturers</span></span> | |
| <span data-ttu-id="c2560-132">Správa majetku – modely</span><span class="sxs-lookup"><span data-stu-id="c2560-132">Asset management models</span></span> | <span data-ttu-id="c2560-133">msdyn\_models</span><span class="sxs-lookup"><span data-stu-id="c2560-133">msdyn\_models</span></span> | |
| <span data-ttu-id="c2560-134">Správa majetku – záruka</span><span class="sxs-lookup"><span data-stu-id="c2560-134">Asset management warranty</span></span> | <span data-ttu-id="c2560-135">msdyn\_warranties</span><span class="sxs-lookup"><span data-stu-id="c2560-135">msdyn\_warranties</span></span> | |

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [lifecycle models](includes/AssetManagementAssetLifecycleModels-msdyn-assetlifecyclemodels.md)]

[!include [lifecycle states](includes/AssetManagementAssetLifecycleStates-msdyn-assetlifecyclestates.md)]

[!include [assets](includes/AssetManagementAssets-msdyn-customerassets.md)]

[!include [asset types](includes/AssetManagementAssetTypes-msdyn-customerassetcategories.md)]

[!include [functional location lifecycle models](includes/AssetManagementFunctionalLocationLifecycleModels-msdyn-functionallocationlifecyclemodels.md)]

[!include [functional location lifecycle states](includes/AssetManagementFunctionalLocationLifecycleStates-msdyn-functionallocationlifecyclestates.md)]

[!include [functional locations](includes/AssetManagementFunctionalLocations-msdyn-functionallocations.md)]

[!include [functional location types](includes/AssetManagementFunctionalLocationTypes-msdyn-functionallocationtypes.md)]

[!include [manufacturers](includes/AssetManagementManufacturers-msdyn-manufacturers.md)]

[!include [models](includes/AssetManagementModels-msdyn-models.md)]

[!include [warranty](includes/AssetManagementWarranty-msdyn-warranties.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]