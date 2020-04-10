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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 1e423199d0639db5e403e280880036b590149095
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172939"
---
# <a name="in-house-assets-for-servicing"></a>Interní majetek pro údržbu

[!include [banner](../../includes/banner.md)]



Aplikace Microsoft Dynamics 365 Field Service je navržena pro poskytnutí servisu majetku zákazníků. Správa majetku pro Dynamics 365 Supply Chain Management je navržena pro údržbu interního majetku. Integrace těchto dvou aplikací umožňuje používat službu Field Service k poskytnutí servisu pro majetek zákazníků i interního majetku. Můžete také klasifikovat majetek na základě funkčního umístění nebo hierarchie a sledovat servis na podrobné úrovni.

Další informace naleznete v tématu [Integrace řešení Dynamics 365 Field Service a Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).

## <a name="templates"></a>Šablony

Interní majetek zahrnuje kolekci základních map entit, které pracují společně během interakce s daty zákazníka, jak je uvedeno v následující tabulce.

| Aplikace Finance and Operations | Modelem řízené aplikace v Dynamics 365 | popis |
|-----------------------------|-----------------------------------|-------------|
| Správa majetku – modely životního cyklu majetku | msdyn\_assetlifecyclemodels | |
| Správa majetku – stavy životního cyklu majetku | msdyn\_assetlifecyclestates | |
| Správa majetku – majetek | msdyn\_customerassets | |
| Správa majetku – typy majetku | msdyn\_customerassetcategories | |
| Správa majetku – funkční místa – modely životního cyklu | msdyn\_functionallocationlifecyclemodels | |
| Správa majetku – funkční místa – stavy životního cyklu | msdyn\_functionallocationlifecyclestates | |
| Správa majetku – funkční místa | msdyn\_functionallocations | |
| Správa majetku – typy funkčních míst | msdyn\_functionallocationtypes | |
| Správa majetku – výrobci | msdyn\_manufacturers | |
| Správa majetku – modely | msdyn\_models | |
| Správa majetku – záruka | msdyn\_warranties | |

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
