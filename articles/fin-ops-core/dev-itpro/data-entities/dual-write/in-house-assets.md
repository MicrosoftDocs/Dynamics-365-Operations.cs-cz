---
title: Interní majetek pro údržbu
description: Tento článek popisuje, jak můžete použít Microsoft Dynamics 365 Field Service k obsluze aktiv zákazníků i interních aktiv.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: c946af11737a77c4dadd824893e6cc1e4c77b587
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858615"
---
# <a name="in-house-assets-for-servicing"></a>Interní majetek pro údržbu

[!include [banner](../../includes/banner.md)]

Aplikace Microsoft Dynamics 365 Field Service je navržena pro poskytnutí servisu majetku zákazníků. Správa majetku pro Dynamics 365 Supply Chain Management je navržena pro údržbu interního majetku. Integrace těchto dvou aplikací umožňuje používat službu Field Service k poskytnutí servisu pro majetek zákazníků i interního majetku. Můžete také klasifikovat majetek na základě funkčního umístění nebo hierarchie a sledovat servis na podrobné úrovni.

Další informace naleznete v tématu [Integrace řešení Dynamics 365 Field Service a Supply Chain Management](/dynamics365/field-service/supply-chain-field-service-integration).

## <a name="templates"></a>Šablony

Interní majetek zahrnuje kolekci základních map tabulek, které pracují společně během interakce s daty zákazníka, jak je uvedeno v následující tabulce.

| Aplikace Finance and Operations | Aplikace Customer Engagement | popis |
|-----------------------------|-----------------------------------|-------------|
[Správa majetku – modely životního cyklu majetku](mapping-reference.md#119) | msdyn_assetlifecyclemodels | |
[Správa majetku – stavy životního cyklu majetku](mapping-reference.md#120) | msdyn_assetlifecyclestates | |
[Správa majetku – typy majetku](mapping-reference.md#124) | msdyn_customerassetcategories | |
[Správa majetku – majetek](mapping-reference.md#125) | msdyn_customerassets | |
[Správa majetku – funkční místa – modely životního cyklu](mapping-reference.md#134) | msdyn_functionallocationlifecyclemodels | |
[Správa majetku – funkční místa – stavy životního cyklu](mapping-reference.md#135) | msdyn_functionallocationlifecyclestates | |
[Správa majetku – typy funkčních míst](mapping-reference.md#137) | msdyn_functionallocationtypes | |
[Správa majetku – funkční místa](mapping-reference.md#136) | msdyn_functionallocations | |
[Správa majetku – výrobci](mapping-reference.md#153) | msdyn_manufacturers | |
[Správa majetku – modely](mapping-reference.md#154) | msdyn_models | |
[Správa majetku – záruka](mapping-reference.md#209) | msdyn_warranties | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
