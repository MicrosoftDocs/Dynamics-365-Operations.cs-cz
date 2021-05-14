---
title: Operace pro neshody
description: Toto téma popisuje, jak vytvářet a používat operace pro neshody.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6454a56323ea66369696dd6e3310a41b4eb9ee58
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956585"
---
# <a name="operations-for-nonconformances"></a><span data-ttu-id="9de3a-103">Operace pro neshody</span><span class="sxs-lookup"><span data-stu-id="9de3a-103">Operations for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9de3a-104">Toto téma popisuje, jak vytvářet a používat operace pro neshody.</span><span class="sxs-lookup"><span data-stu-id="9de3a-104">This topic describes how to create and use operations for nonconformances.</span></span>

<span data-ttu-id="9de3a-105">Na stránce **Operace** můžete definovat klasifikace práce, které může být provedeny pro schválenou neshodu.</span><span class="sxs-lookup"><span data-stu-id="9de3a-105">You can use the **Operations** page to define classifications of the work that can be performed for an approved nonconformance.</span></span> <span data-ttu-id="9de3a-106">Přiřadíte-li k neshodě související operaci, můžete poskytnout podrobné informace, například o přiřazeném materiálu, pracovní době a poplatcích vyžadovaných pro provedení této operace.</span><span class="sxs-lookup"><span data-stu-id="9de3a-106">When you assign a related operation to a nonconformance, you can provide details such as the associated material, labor hours, and charges that are required to do the operation.</span></span> <span data-ttu-id="9de3a-107">Systém tyto informace používá k výpočtu odhadovaných nákladů na danou operaci.</span><span class="sxs-lookup"><span data-stu-id="9de3a-107">The system uses this information to calculate an estimated cost for the operation.</span></span> <span data-ttu-id="9de3a-108">Podrobné informace a odhad nákladů jsou pouze informativní.</span><span class="sxs-lookup"><span data-stu-id="9de3a-108">The detailed information and estimated costs are for reference.</span></span> <span data-ttu-id="9de3a-109">Související operace pro kvalitu se liší od operací, které lze definovat ve výrobním postupu.</span><span class="sxs-lookup"><span data-stu-id="9de3a-109">The related operations for quality differ from the operations that can be defined for a production route.</span></span>

> [!NOTE]
> <span data-ttu-id="9de3a-110">I když můžete sledovat náklady, čas a položky, které se používají v operaci související s neshodou, zadaná data jsou pouze informativní.</span><span class="sxs-lookup"><span data-stu-id="9de3a-110">Although you can track costs, time, and the items that are used in an operation that is related to a nonconformance, the data that you enter is only informational.</span></span> <span data-ttu-id="9de3a-111">Není automaticky integrován s hlavní knihou, podřízenou knihou inventáře nebo modulu **Čas a ducházka**.</span><span class="sxs-lookup"><span data-stu-id="9de3a-111">It isn't automatically integrated with the general ledger, inventory subledger, or the **Time and attendance** module.</span></span>

## <a name="examples-of-operations"></a><span data-ttu-id="9de3a-112">Příklady operací</span><span class="sxs-lookup"><span data-stu-id="9de3a-112">Examples of operations</span></span>

<span data-ttu-id="9de3a-113">Pracujete pro výrobní společnost.</span><span class="sxs-lookup"><span data-stu-id="9de3a-113">You work for a manufacturing company.</span></span> <span data-ttu-id="9de3a-114">Byla vytvořena a schválena neshoda pro položky, které neprošly testem kvality.</span><span class="sxs-lookup"><span data-stu-id="9de3a-114">A nonconformance was created and approved for items that failed a quality test.</span></span> <span data-ttu-id="9de3a-115">Byla vytvořena oprava, která naznačuje, že problém souvisel se špatným uložením na stroji.</span><span class="sxs-lookup"><span data-stu-id="9de3a-115">A correction was created to indicate that the problem was related to a bad bearing on a machine.</span></span> <span data-ttu-id="9de3a-116">K výměně ložiska je zapotřebí několik kroků a je sledována odpovědnost za každou operaci.</span><span class="sxs-lookup"><span data-stu-id="9de3a-116">Several steps are required to replace the bearing, and the responsibility for each operation is tracked.</span></span> <span data-ttu-id="9de3a-117">Mohou být například vyžadovány následující kroky:</span><span class="sxs-lookup"><span data-stu-id="9de3a-117">For example, the following steps might be required:</span></span>

1. <span data-ttu-id="9de3a-118">Výrobní linka je zastavena a je provedena rutina vyčištění.</span><span class="sxs-lookup"><span data-stu-id="9de3a-118">The production line is stopped, and the clean-out routine is performed.</span></span>
1. <span data-ttu-id="9de3a-119">Personál údržby vyměňte ložisko.</span><span class="sxs-lookup"><span data-stu-id="9de3a-119">Maintenance personnel replace the bearing.</span></span>
1. <span data-ttu-id="9de3a-120">Pracovníci zajišťující kvalitu zkontrolují stroj před jeho opětovným zapnutím.</span><span class="sxs-lookup"><span data-stu-id="9de3a-120">Quality assurance personnel inspect the machine before it's turned back on.</span></span>

<span data-ttu-id="9de3a-121">V tomto příkladu lze vytvořit následující operace představující práci, kterou je třeba provést:</span><span class="sxs-lookup"><span data-stu-id="9de3a-121">For this example, the following operations can be created to represent the work that must be done:</span></span>

- <span data-ttu-id="9de3a-122">Zastavení výrobní linky.</span><span class="sxs-lookup"><span data-stu-id="9de3a-122">Stop the production line.</span></span>
- <span data-ttu-id="9de3a-123">Vyčistění výrobní linky.</span><span class="sxs-lookup"><span data-stu-id="9de3a-123">Clean out the production line.</span></span>
- <span data-ttu-id="9de3a-124">Provedení údržby stroje.</span><span class="sxs-lookup"><span data-stu-id="9de3a-124">Perform machine maintenance.</span></span>
- <span data-ttu-id="9de3a-125">Zkontrolování stroje.</span><span class="sxs-lookup"><span data-stu-id="9de3a-125">Inspect the machine.</span></span>

## <a name="create-an-operation"></a><span data-ttu-id="9de3a-126">Vytvoření operace</span><span class="sxs-lookup"><span data-stu-id="9de3a-126">Create an operation</span></span>

1. <span data-ttu-id="9de3a-127">Přejděte na **Řízení zásob \> Nastavení \> Správa kvality \> Operace**.</span><span class="sxs-lookup"><span data-stu-id="9de3a-127">Go to **Inventory management \> Setup \> Quality management \> Operations**.</span></span>
1. <span data-ttu-id="9de3a-128">V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="9de3a-128">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="9de3a-129">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="9de3a-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="9de3a-130">**Operace** - Zadejte jedinečné ID nebo název operace.</span><span class="sxs-lookup"><span data-stu-id="9de3a-130">**Operation** – Enter a unique ID or name for the operation.</span></span>
    - <span data-ttu-id="9de3a-131">**Popis** - Zadejte podrobný popis operace.</span><span class="sxs-lookup"><span data-stu-id="9de3a-131">**Description** – Enter a detailed description of the operation.</span></span>
    - <span data-ttu-id="9de3a-132">**Typ** - Pokud lze operaci použít pouze u neshod, které souvisejí s konkrétním typem objednávky, vyberte typ objednávky (*Nákupní objednávka* nebo *Zakázka odběratele*).</span><span class="sxs-lookup"><span data-stu-id="9de3a-132">**Type** – If the operation can be used only with nonconformances that are related to a specific type of order, select the order type (*Purchase order* or *Sales order*).</span></span>

1. <span data-ttu-id="9de3a-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="9de3a-133">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9de3a-134">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="9de3a-134">Additional resources</span></span>

- [<span data-ttu-id="9de3a-135">Přehled správy kvality</span><span class="sxs-lookup"><span data-stu-id="9de3a-135">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="9de3a-136">Povolit správu kvality a neshod</span><span class="sxs-lookup"><span data-stu-id="9de3a-136">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="9de3a-137">Vytvoření a zpracování neshod</span><span class="sxs-lookup"><span data-stu-id="9de3a-137">Create and process nonconformances</span></span>](tasks/create-process-non-conformance.md)
- [<span data-ttu-id="9de3a-138">Zaměstnanci odpovědní za schvalování neshod</span><span class="sxs-lookup"><span data-stu-id="9de3a-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="9de3a-139">Karanténní zóny pro neshody</span><span class="sxs-lookup"><span data-stu-id="9de3a-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="9de3a-140">Diagnostické typy pro neshody</span><span class="sxs-lookup"><span data-stu-id="9de3a-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="9de3a-141">Kódy kvality pro náklady.</span><span class="sxs-lookup"><span data-stu-id="9de3a-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="9de3a-142">Typy problémů pro neshody</span><span class="sxs-lookup"><span data-stu-id="9de3a-142">Problem types for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="9de3a-143">Správa kvality pro procesy skladu</span><span class="sxs-lookup"><span data-stu-id="9de3a-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
