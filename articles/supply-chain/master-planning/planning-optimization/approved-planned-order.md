---
title: Prohlížení, správa a schvalování plánovaných objednávek
description: Tohle téma poskytuje informace, jak zobrazovat, spravovat a schvalovat plánované objednávky v optimalizaci plánování.
author: ChristianRytt
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 71ec26bea2063bcf8b6d302a7ece804b3ac934b3
ms.sourcegitcommit: 3673eeca1ada0f3e4ec277176515a946706f8a41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304360"
---
# <a name="view-manage-and-approve-planned-orders"></a><span data-ttu-id="5dfa2-103">Prohlížení, správa a schvalování plánovaných objednávek</span><span class="sxs-lookup"><span data-stu-id="5dfa2-103">View, manage, and approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5dfa2-104">Tohle téma poskytuje informace, jak zobrazovat, spravovat a schvalovat plánované objednávky v optimalizaci plánování.</span><span class="sxs-lookup"><span data-stu-id="5dfa2-104">This topic provides information about how to view, manage, and approve planned orders in Planning Optimization.</span></span>

## <a name="view-and-manage-planned-orders"></a><a name="view-planned-orders"></a><span data-ttu-id="5dfa2-105">Prohlížení a správa plánovaných objednávek</span><span class="sxs-lookup"><span data-stu-id="5dfa2-105">View and manage planned orders</span></span>

<span data-ttu-id="5dfa2-106">Plánované objednávky můžete zobrazit a spravovat na jakékoli stránce seznamu plánovaných objednávek.</span><span class="sxs-lookup"><span data-stu-id="5dfa2-106">You can view and manage planned orders on any planned orders list page.</span></span> <span data-ttu-id="5dfa2-107">Přejděte na jedno z následujících míst v závislosti na typu plánovaných objednávek, se kterými chcete pracovat:</span><span class="sxs-lookup"><span data-stu-id="5dfa2-107">Go to one of the following places, depending on the type of planned orders that you want to work with:</span></span>

- <span data-ttu-id="5dfa2-108">Hlavní plánování \> Pracovní prostory \> Hlavní plánování</span><span class="sxs-lookup"><span data-stu-id="5dfa2-108">Master planning \> Workspaces \> Master planning</span></span>
- <span data-ttu-id="5dfa2-109">Hlavní plánování \> Hlavní plánování \> Plánované objednávky</span><span class="sxs-lookup"><span data-stu-id="5dfa2-109">Master planning \> Master planning \> Planned orders</span></span>
- <span data-ttu-id="5dfa2-110">Řízení výroby \> Výrobní zakázky \> Plánované výrobní zakázky</span><span class="sxs-lookup"><span data-stu-id="5dfa2-110">Production control \> Production orders \> Planned production orders</span></span>
- <span data-ttu-id="5dfa2-111">Zásobování a zdroje \> Nákupní objednávky \> Plánované nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="5dfa2-111">Procurement and sourcing \> Purchase orders \> Planned purchase orders</span></span>
- <span data-ttu-id="5dfa2-112">Správa zásob \> Příchozí objednávky \> Plánované převody</span><span class="sxs-lookup"><span data-stu-id="5dfa2-112">Inventory management \> Inbound orders \> Planned transfers</span></span>
- <span data-ttu-id="5dfa2-113">Správa zásob \> Odchozí objednávky \> Plánované převody</span><span class="sxs-lookup"><span data-stu-id="5dfa2-113">Inventory management \> Outbound orders \> Planned transfers</span></span>

## <a name="view-and-edit-the-status-of-planned-orders"></a><span data-ttu-id="5dfa2-114">Zobrazení a úprava stavu plánovaných objednávek</span><span class="sxs-lookup"><span data-stu-id="5dfa2-114">View and edit the status of planned orders</span></span>

<span data-ttu-id="5dfa2-115">Můžete použít pole **Stav** každé plánované objednávky, abyste mohli sledovat svůj postup nebo změnit způsob zpracování plánované objednávky.</span><span class="sxs-lookup"><span data-stu-id="5dfa2-115">You can use the **Status** field of each planned order to help track your progress or change how a planned order will be processed.</span></span> <span data-ttu-id="5dfa2-116">K dispozici jsou následující hodnoty **Stav**:</span><span class="sxs-lookup"><span data-stu-id="5dfa2-116">The following **Status** values are available:</span></span>

- <span data-ttu-id="5dfa2-117">**Nezpracováno** – Když hlavní plánování vytvoří naplánované objednávky, mají tento stav.</span><span class="sxs-lookup"><span data-stu-id="5dfa2-117">**Unprocessed** – When master planning generates planned orders, they are given this status.</span></span> <span data-ttu-id="5dfa2-118">Plánované objednávky s tímto stavem budou odstraněny během dalšího běhu plánování.</span><span class="sxs-lookup"><span data-stu-id="5dfa2-118">Planned orders that have this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="5dfa2-119">**Dokončeno** – Tento stav označuje, že plánovaná objednávka byla dokončena.</span><span class="sxs-lookup"><span data-stu-id="5dfa2-119">**Completed** – This status indicates that the planned order has been completed.</span></span> <span data-ttu-id="5dfa2-120">Když se rozhodnete plánovanou objednávku nepotvrdit, ručně změňte stav na *Dokončeno*.</span><span class="sxs-lookup"><span data-stu-id="5dfa2-120">If you decide not to firm a planned order, you can manually change its status to *Completed*.</span></span> <span data-ttu-id="5dfa2-121">Mějte na paměti, že se stavy *Nezpracováno* a *Dokončeno* systém zachází stejně.</span><span class="sxs-lookup"><span data-stu-id="5dfa2-121">Note that the system treats the *Unprocessed* and *Completed* statuses in the same way.</span></span>
- <span data-ttu-id="5dfa2-122">**Schváleno** – Tento stav označuje, že plánovaná objednávka je schválena k potvrzení.</span><span class="sxs-lookup"><span data-stu-id="5dfa2-122">**Approved** – This status indicates that the planned order is approved for firming.</span></span> <span data-ttu-id="5dfa2-123">Chcete-li potvrdit plánovanou objednávku, můžete její stav změnit na *Schváleno*.</span><span class="sxs-lookup"><span data-stu-id="5dfa2-123">If you want to firm a planned order, you can change its status to *Approved*.</span></span> <span data-ttu-id="5dfa2-124">Chcete-li zachovat úpravy, které byly provedeny v plánované objednávce, nebo plánujete-li plánovanou objednávku potvrdit, změňte její stav na *Schváleno*.</span><span class="sxs-lookup"><span data-stu-id="5dfa2-124">If you want to keep the edits that have been made to a planned order, or if you're planning to firm a planned order, change its status to *Approved*.</span></span> <span data-ttu-id="5dfa2-125">Plánované objednávky se stavem *Schváleno* jsou považovány za pevné a očekávané dodávky podle hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="5dfa2-125">Planned orders that have a status of *Approved* are considered fixed and expected supply by master planning.</span></span> <span data-ttu-id="5dfa2-126">Proto se během pozdějších hlavních plánovacích běhů nemění ani neodstraní.</span><span class="sxs-lookup"><span data-stu-id="5dfa2-126">Therefore, they aren't modified or deleted during later master planning runs.</span></span> <span data-ttu-id="5dfa2-127">Pro dosažení tohoto chování, logika plánování zkopíruje plánované objednávky se stavem *Schváleno* z původní verze plánu do nové verze plánu během hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="5dfa2-127">To achieve this behavior, the planning logic copies planned orders that have a status of *Approved* from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="5dfa2-128">Pamatujte si, že plánované objednávky ve stavu *Schváleno* jsou považovány za dodávky pouze v rámci konkrétního hlavního plánu.</span><span class="sxs-lookup"><span data-stu-id="5dfa2-128">Note that planned orders that have a status of *Approved* are considered supply only within the specific master plan.</span></span>

<span data-ttu-id="5dfa2-129">Chcete-li změnit stav jedné plánované objednávky, [otevřete stránku se seznamem plánovaných objednávek](#view-planned-orders), otevřete objednávku a proveďte jeden z těchto kroků:</span><span class="sxs-lookup"><span data-stu-id="5dfa2-129">To change the status of a single planned order, [open any planned orders list page](#view-planned-orders), open the order, and then follow one of these steps:</span></span>

- <span data-ttu-id="5dfa2-130">Na rychlé kartě **Obecné** změňte hodnotu pole **Stav**.</span><span class="sxs-lookup"><span data-stu-id="5dfa2-130">On the **General** FastTab, change the value of the **Status** field.</span></span>
- <span data-ttu-id="5dfa2-131">V podokně akcí na kartě **Plánovaná objednávka** ve skupině **Zpracovat** vyberte **Změnit stav**.</span><span class="sxs-lookup"><span data-stu-id="5dfa2-131">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="5dfa2-132">V podokně akcí vyberte možnost **Schválit** a označte objednávku jako schválenou.</span><span class="sxs-lookup"><span data-stu-id="5dfa2-132">On the Action Pane, select **Approve** to mark the order as approved.</span></span>

<span data-ttu-id="5dfa2-133">Chcete-li změnit stav několika plánovaných objednávek současně, [otevřete stránku se seznamem plánovaných objednávek](#view-planned-orders), zaškrtněte políčko u každé objednávky, kterou chcete změnit, a poté proveďte jeden z těchto kroků:</span><span class="sxs-lookup"><span data-stu-id="5dfa2-133">To change the status of several planned orders at the same time, [open any planned orders list page](#view-planned-orders), select the check box for each order that you want to change, and then follow one of these steps:</span></span>

- <span data-ttu-id="5dfa2-134">V podokně akcí na kartě **Plánovaná objednávka** ve skupině **Zpracovat** vyberte **Změnit stav**.</span><span class="sxs-lookup"><span data-stu-id="5dfa2-134">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="5dfa2-135">V podokně akcí vyberte možnost **Schválit** a označte objednávky jako schválené.</span><span class="sxs-lookup"><span data-stu-id="5dfa2-135">On the Action Pane, select **Approve** to mark the orders as approved.</span></span>

## <a name="approve-planned-orders"></a><span data-ttu-id="5dfa2-136">Schválení plánovaných objednávek</span><span class="sxs-lookup"><span data-stu-id="5dfa2-136">Approve planned orders</span></span>

<span data-ttu-id="5dfa2-137">Schválení plánovaných objednávek je volitelným krokem v procesu vytvoření potvrzené objednávky z plánované objednávky.</span><span class="sxs-lookup"><span data-stu-id="5dfa2-137">Approval of planned orders is an optional step in the process of creating a firmed order from a planned order.</span></span>

<span data-ttu-id="5dfa2-138">Následující ilustrace ukazuje, jak můžete použít hodnotu **Stav** hodnota, která je přiřazena každé plánované objednávce k implementaci pracovního toku schválení.</span><span class="sxs-lookup"><span data-stu-id="5dfa2-138">The following illustration shows how you can use the **Status** value that is assigned to each planned order to implement an approval workflow.</span></span> <span data-ttu-id="5dfa2-139">Chcete-li implementovat proces schválení, ručně upravte hodnotu **Stav** pro každou plánovanou objednávku, jak je popsáno v předchozí části.</span><span class="sxs-lookup"><span data-stu-id="5dfa2-139">To implement an approval process, manually adjust the **Status** value for each planned order as described in the previous section.</span></span>

![Tok plánované objednávky](media/approved-planned-orders-1.png)

> [!TIP]
> <span data-ttu-id="5dfa2-141">Doporučujeme vám schválit všechny upravené plánované objednávky.</span><span class="sxs-lookup"><span data-stu-id="5dfa2-141">We recommend that you approve any modified planned orders.</span></span> <span data-ttu-id="5dfa2-142">Jinak budou úpravy při příštím spuštění plánování ignorovány a přepsány.</span><span class="sxs-lookup"><span data-stu-id="5dfa2-142">Otherwise, the edits will be ignored and overwritten by the next planning run.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5dfa2-143">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="5dfa2-143">Additional resources</span></span>

- [<span data-ttu-id="5dfa2-144">Potvrdit plánované objednávky</span><span class="sxs-lookup"><span data-stu-id="5dfa2-144">Firm planned orders</span></span>](planned-order-firming.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
