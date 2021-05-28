---
title: Chybí nastavení pole při kopírování skupin modelů položek do jiné právnické osoby
description: Chybí nastavení pole při kopírování skupin modelů položek do jiné právnické osoby.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f6fdfef0bc377418ed8a9c8830e74526a0b95eb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026332"
---
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a><span data-ttu-id="6c99f-103">Chybí nastavení pole při kopírování skupin modelů položek do jiné právnické osoby</span><span class="sxs-lookup"><span data-stu-id="6c99f-103">Missing field settings when item model groups are copied to another legal entity</span></span>

<span data-ttu-id="6c99f-104">Číslo článku znalostní báze: 4612800</span><span class="sxs-lookup"><span data-stu-id="6c99f-104">KB number: 4612800</span></span>

## <a name="symptoms"></a><span data-ttu-id="6c99f-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="6c99f-105">Symptoms</span></span>

<span data-ttu-id="6c99f-106">Když kopírujete skupiny modelů položek do jiné právnické osoby (společnosti) pomocí entity *Zásady skupinových zásob modelu položky*, některá nastavení pole (například model a popis zásob) chybí v nové skupině modelů v cílové právnické osobě.</span><span class="sxs-lookup"><span data-stu-id="6c99f-106">When you copy item model groups to another legal entity (company) by using the *Item model group inventory policies* entity, some field settings (for example, the inventory model and description) are missing in the new model group in the destination legal entity.</span></span>

## <a name="resolution"></a><span data-ttu-id="6c99f-107">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="6c99f-107">Resolution</span></span>

<span data-ttu-id="6c99f-108">Chcete-li vytvořit úplnou kopii skupiny modelů položek do jiné právnické osoby, musíte také vybrat obě zásady zásob skupiny modelů položek (`InventInventoryPolicyEntity`) a zásady převzetí toků nákladů (`InventCostFlowAssumptionPolicyEntity`), které jsou přidruženy ke skupině modelů položek.</span><span class="sxs-lookup"><span data-stu-id="6c99f-108">To create a complete copy of an item model group to another legal entity, you must also select both the item model group inventory policies (`InventInventoryPolicyEntity`) and the cost flow assumption policies (`InventCostFlowAssumptionPolicyEntity`) that are associated with the item model group.</span></span>
