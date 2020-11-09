---
title: Interní majetek pro údržbu
description: V tomto tématu je popsán způsob použití služby Microsoft Dynamics 365 Field Service k poskytnutí servisu pro majetek zákazníka i interního majetku.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
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
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 0e87a3d645c19fab3bb0560ba5114d193e2d0be7
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997163"
---
# <a name="in-house-assets-for-servicing"></a><span data-ttu-id="d4cc9-103">Interní majetek pro údržbu</span><span class="sxs-lookup"><span data-stu-id="d4cc9-103">In-house assets for servicing</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="d4cc9-104">Aplikace Microsoft Dynamics 365 Field Service je navržena pro poskytnutí servisu majetku zákazníků.</span><span class="sxs-lookup"><span data-stu-id="d4cc9-104">Microsoft Dynamics 365 Field Service is designed to service customer assets.</span></span> <span data-ttu-id="d4cc9-105">Správa majetku pro Dynamics 365 Supply Chain Management je navržena pro údržbu interního majetku.</span><span class="sxs-lookup"><span data-stu-id="d4cc9-105">Asset management for Dynamics 365 Supply Chain Management is designed to maintain in-house assets.</span></span> <span data-ttu-id="d4cc9-106">Integrace těchto dvou aplikací umožňuje používat službu Field Service k poskytnutí servisu pro majetek zákazníků i interního majetku.</span><span class="sxs-lookup"><span data-stu-id="d4cc9-106">Integration of these two apps lets you use Field Service to service both customer assets and in-house assets.</span></span> <span data-ttu-id="d4cc9-107">Můžete také klasifikovat majetek na základě funkčního umístění nebo hierarchie a sledovat servis na podrobné úrovni.</span><span class="sxs-lookup"><span data-stu-id="d4cc9-107">You can also classify the assets, based on functional location or hierarchy, and track the servicing at a detailed level.</span></span>

<span data-ttu-id="d4cc9-108">Další informace naleznete v tématu [Integrace řešení Dynamics 365 Field Service a Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span><span class="sxs-lookup"><span data-stu-id="d4cc9-108">For more information, see [Integrate Dynamics 365 Field Service and Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span></span>

## <a name="templates"></a><span data-ttu-id="d4cc9-109">Šablony</span><span class="sxs-lookup"><span data-stu-id="d4cc9-109">Templates</span></span>

<span data-ttu-id="d4cc9-110">Interní majetek zahrnuje kolekci základních map entit, které pracují společně během interakce s daty zákazníka, jak je uvedeno v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="d4cc9-110">In-house-assets include a collection of core entity maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="d4cc9-111">Aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d4cc9-111">Finance and Operations apps</span></span> | <span data-ttu-id="d4cc9-112">Modelem řízené aplikace v Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="d4cc9-112">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="d4cc9-113">popis</span><span class="sxs-lookup"><span data-stu-id="d4cc9-113">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="d4cc9-114">Správa majetku – modely životního cyklu majetku</span><span class="sxs-lookup"><span data-stu-id="d4cc9-114">Asset management asset lifecycle models</span></span> | <span data-ttu-id="d4cc9-115">msdyn\_assetlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="d4cc9-115">msdyn\_assetlifecyclemodels</span></span> | |
| <span data-ttu-id="d4cc9-116">Správa majetku – stavy životního cyklu majetku</span><span class="sxs-lookup"><span data-stu-id="d4cc9-116">Asset management asset lifecycle states</span></span> | <span data-ttu-id="d4cc9-117">msdyn\_assetlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="d4cc9-117">msdyn\_assetlifecyclestates</span></span> | |
| <span data-ttu-id="d4cc9-118">Správa majetku – majetek</span><span class="sxs-lookup"><span data-stu-id="d4cc9-118">Asset management assets</span></span> | <span data-ttu-id="d4cc9-119">msdyn\_customerassets</span><span class="sxs-lookup"><span data-stu-id="d4cc9-119">msdyn\_customerassets</span></span> | |
| <span data-ttu-id="d4cc9-120">Správa majetku – typy majetku</span><span class="sxs-lookup"><span data-stu-id="d4cc9-120">Asset management asset types</span></span> | <span data-ttu-id="d4cc9-121">msdyn\_customerassetcategories</span><span class="sxs-lookup"><span data-stu-id="d4cc9-121">msdyn\_customerassetcategories</span></span> | |
| <span data-ttu-id="d4cc9-122">Správa majetku – funkční místa – modely životního cyklu</span><span class="sxs-lookup"><span data-stu-id="d4cc9-122">Asset management functional location lifecycle models</span></span> | <span data-ttu-id="d4cc9-123">msdyn\_functionallocationlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="d4cc9-123">msdyn\_functionallocationlifecyclemodels</span></span> | |
| <span data-ttu-id="d4cc9-124">Správa majetku – funkční místa – stavy životního cyklu</span><span class="sxs-lookup"><span data-stu-id="d4cc9-124">Asset management functional location lifecycle states</span></span> | <span data-ttu-id="d4cc9-125">msdyn\_functionallocationlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="d4cc9-125">msdyn\_functionallocationlifecyclestates</span></span> | |
| <span data-ttu-id="d4cc9-126">Správa majetku – funkční místa</span><span class="sxs-lookup"><span data-stu-id="d4cc9-126">Asset management functional locations</span></span> | <span data-ttu-id="d4cc9-127">msdyn\_functionallocations</span><span class="sxs-lookup"><span data-stu-id="d4cc9-127">msdyn\_functionallocations</span></span> | |
| <span data-ttu-id="d4cc9-128">Správa majetku – typy funkčních míst</span><span class="sxs-lookup"><span data-stu-id="d4cc9-128">Asset management functional location types</span></span> | <span data-ttu-id="d4cc9-129">msdyn\_functionallocationtypes</span><span class="sxs-lookup"><span data-stu-id="d4cc9-129">msdyn\_functionallocationtypes</span></span> | |
| <span data-ttu-id="d4cc9-130">Správa majetku – výrobci</span><span class="sxs-lookup"><span data-stu-id="d4cc9-130">Asset management manufacturers</span></span> | <span data-ttu-id="d4cc9-131">msdyn\_manufacturers</span><span class="sxs-lookup"><span data-stu-id="d4cc9-131">msdyn\_manufacturers</span></span> | |
| <span data-ttu-id="d4cc9-132">Správa majetku – modely</span><span class="sxs-lookup"><span data-stu-id="d4cc9-132">Asset management models</span></span> | <span data-ttu-id="d4cc9-133">msdyn\_models</span><span class="sxs-lookup"><span data-stu-id="d4cc9-133">msdyn\_models</span></span> | |
| <span data-ttu-id="d4cc9-134">Správa majetku – záruka</span><span class="sxs-lookup"><span data-stu-id="d4cc9-134">Asset management warranty</span></span> | <span data-ttu-id="d4cc9-135">msdyn\_warranties</span><span class="sxs-lookup"><span data-stu-id="d4cc9-135">msdyn\_warranties</span></span> | |

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
