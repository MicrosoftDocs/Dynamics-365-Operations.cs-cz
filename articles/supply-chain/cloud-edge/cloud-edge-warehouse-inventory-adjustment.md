---
title: Úprava skladových zásob
description: Toto téma poskytuje informace o deníku úprav skladu a zpracování, když používáte jednotky škálování.
author: perlynne
manager: tfehr
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventoryAdjustmentJournal, InventJournalCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: be386539ea7addf20256ac2b1f8a2a72736fcbec
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938219"
---
# <a name="warehouse-inventory-adjustment"></a><span data-ttu-id="f5e43-103">Úprava skladových zásob</span><span class="sxs-lookup"><span data-stu-id="f5e43-103">Warehouse inventory adjustment</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="f5e43-104">Funkce úpravy skladových zásob se používá při spuštění cloudových a hranových jednotek pro [výrobní úlohy](cloud-edge-workload-manufacturing.md) a [úlohy správy skladu](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="f5e43-104">The Warehouse inventory adjustment feature is used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="f5e43-105">Když pracovník provede úpravu zásob pomocí aplikace skladu proti úloze správy skladu s jednotkou škálování, musí fyzickou aktualizaci skladových zásob zpracovat dávková úloha **Deník úprav skladových zásob**, kterou spustíte a naplánujete přechodem na **Správa skladu > Pravidelné úkoly > Deník úprav skladových zásob**.</span><span class="sxs-lookup"><span data-stu-id="f5e43-105">When a worker does an inventory adjustment using the warehouse app against a scale unit warehouse management workload, the physical on-hand update must be processed by the **Warehouse inventory adjustment journal** batch job, which you run and schedule by going to **Warehouse management > Periodic tasks > Warehouse inventory adjustment journal**.</span></span>

<span data-ttu-id="f5e43-106">Následující pracovní procesy aplikace skladu aktuálně používají **Deník úpravy skladových zásob** na úlohách jednotek škálování:</span><span class="sxs-lookup"><span data-stu-id="f5e43-106">The following warehouse app work processes currently use the **Warehouse inventory adjustment journal** on scale unit workloads:</span></span>

- <span data-ttu-id="f5e43-107">Úprava příchozí/odchozí</span><span class="sxs-lookup"><span data-stu-id="f5e43-107">Adjustment in/out</span></span>
- <span data-ttu-id="f5e43-108">Cyklická inventura</span><span class="sxs-lookup"><span data-stu-id="f5e43-108">Cycle counting</span></span>
- <span data-ttu-id="f5e43-109">Načtení registrační značky</span><span class="sxs-lookup"><span data-stu-id="f5e43-109">License plate loading</span></span>

<span data-ttu-id="f5e43-110">Několik transakcí inventáře je vytvořeno jako součást procesu cloudového a hranového přizpůsobení inventáře, protože nasazení hubu a jednotky škálování sdílejí záznamy inventáře.</span><span class="sxs-lookup"><span data-stu-id="f5e43-110">Several inventory transactions are created as part of cloud and edge an inventory adjustment process because the hub and scale unit deployments share the inventory records.</span></span>

## <a name="inventory-adjustment-example"></a><span data-ttu-id="f5e43-111">Příklad úprav zásob</span><span class="sxs-lookup"><span data-stu-id="f5e43-111">Inventory adjustment example</span></span>

<span data-ttu-id="f5e43-112">V tomto příkladu pracovník skladu použil aplikaci skladu k registraci přidání zásob na skladě.</span><span class="sxs-lookup"><span data-stu-id="f5e43-112">In this example, a warehouse worker has used the warehouse app to register the adding of on-hand inventory.</span></span>

<span data-ttu-id="f5e43-113">Nejprve úloha jednotky škálování vytvoří transakci úpravy skladových zásob pro pozitivní fyzickou úpravu, která se poté synchronizuje s centrem a má za následek zvýšení zásob v centru.</span><span class="sxs-lookup"><span data-stu-id="f5e43-113">First, the scale unit workload creates a warehouse inventory adjustment transaction for the positive physical adjustment, which is then synchronized to the hub and results in an increase of the on-hand inventory on the hub.</span></span>

| <span data-ttu-id="f5e43-114">Typ</span><span class="sxs-lookup"><span data-stu-id="f5e43-114">Type</span></span>                                    | <span data-ttu-id="f5e43-115">Jednotka škálování</span><span class="sxs-lookup"><span data-stu-id="f5e43-115">Scale unit</span></span> | <span data-ttu-id="f5e43-116">Směr</span><span class="sxs-lookup"><span data-stu-id="f5e43-116">Direction</span></span> | <span data-ttu-id="f5e43-117">Centrum</span><span class="sxs-lookup"><span data-stu-id="f5e43-117">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="f5e43-118">Úprava skladových zásob</span><span class="sxs-lookup"><span data-stu-id="f5e43-118">Warehouse inventory adjustment</span></span>          | <span data-ttu-id="f5e43-119">+1</span><span class="sxs-lookup"><span data-stu-id="f5e43-119">+1</span></span>         | ->        | <span data-ttu-id="f5e43-120">+1</span><span class="sxs-lookup"><span data-stu-id="f5e43-120">+1</span></span>  |

<span data-ttu-id="f5e43-121">Centrum poté zpracuje účtování deníku počítání, které je přijímáno prostřednictvím [zprávy procesoru zpráv](cloud-edge-message-processor-messages.md).</span><span class="sxs-lookup"><span data-stu-id="f5e43-121">The hub then processes a counting journal posting, which is received through [message processor messages](cloud-edge-message-processor-messages.md).</span></span> <span data-ttu-id="f5e43-122">Tím se aktualizují další dostupné zásoby.</span><span class="sxs-lookup"><span data-stu-id="f5e43-122">This updates the additional inventory on hand.</span></span> <span data-ttu-id="f5e43-123">Aby se předešlo zdvojení skladových zásob, centrum vytvoří v rámci tohoto procesu transakci offsetu a odstraní dříve zaznamenané zásoby, které souvisí s úpravou skladu.</span><span class="sxs-lookup"><span data-stu-id="f5e43-123">To prevent double inventory on hand, the hub creates an offset transaction as part of this process and removes the previously recorded on-hand inventory that is related to the warehouse inventory adjustment.</span></span>

| <span data-ttu-id="f5e43-124">Typ</span><span class="sxs-lookup"><span data-stu-id="f5e43-124">Type</span></span>                                    | <span data-ttu-id="f5e43-125">Jednotka škálování</span><span class="sxs-lookup"><span data-stu-id="f5e43-125">Scale unit</span></span> | <span data-ttu-id="f5e43-126">Směr</span><span class="sxs-lookup"><span data-stu-id="f5e43-126">Direction</span></span> | <span data-ttu-id="f5e43-127">Centrum</span><span class="sxs-lookup"><span data-stu-id="f5e43-127">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="f5e43-128">Inventura</span><span class="sxs-lookup"><span data-stu-id="f5e43-128">Counting</span></span>                                | <span data-ttu-id="f5e43-129">+1</span><span class="sxs-lookup"><span data-stu-id="f5e43-129">+1</span></span>         | <-        | <span data-ttu-id="f5e43-130">+1</span><span class="sxs-lookup"><span data-stu-id="f5e43-130">+1</span></span>  |
| <span data-ttu-id="f5e43-131">Úpravy skladu (offset)</span><span class="sxs-lookup"><span data-stu-id="f5e43-131">Warehouse inventory adjustment (Offset)</span></span> | <span data-ttu-id="f5e43-132">-1</span><span class="sxs-lookup"><span data-stu-id="f5e43-132">-1</span></span>         | <-        | <span data-ttu-id="f5e43-133">-1</span><span class="sxs-lookup"><span data-stu-id="f5e43-133">-1</span></span>  |

<span data-ttu-id="f5e43-134">Po vytvoření jednotky škálování **Deník úpravy skladu** na centru můžete zkontrolovat **Deníku počítání** i **Ofsetový deník**, které jsou vytvářeny centrem jako součást procesu úpravy.</span><span class="sxs-lookup"><span data-stu-id="f5e43-134">After a scale unit has created a **Warehouse inventory adjustment journal** on the hub, you can review both the **Counting journal** and the **Offset journal**, which are created by the hub as part of the adjustment process.</span></span>

<span data-ttu-id="f5e43-135">Každou z těchto položek deníku a transakce ve Supply Chain Management můžete zkontrolovat pomocí následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="f5e43-135">You can review each of these journal entries and transaction in Supply Chain Management by doing the following steps:</span></span>

1. <span data-ttu-id="f5e43-136">Přihlaste se k jednotce škálování.</span><span class="sxs-lookup"><span data-stu-id="f5e43-136">Sign in on the scale unit.</span></span>
1. <span data-ttu-id="f5e43-137">Přejděte na **Správa skladu \> Periodické úkoly \> Deník úprav skladových zásob**.</span><span class="sxs-lookup"><span data-stu-id="f5e43-137">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="f5e43-138">Na stránce **Deník úprav skladových zásob** najděte a otevřete deník, který zaznamenal změnu dostupných zásob.</span><span class="sxs-lookup"><span data-stu-id="f5e43-138">On the **Warehouse inventory adjustment journal** page, find and open the journal that recorded the on-hand inventory change.</span></span> <span data-ttu-id="f5e43-139">Část **Řádky deníku** část ukazuje každou úpravu zaznamenanou tímto deníkem.</span><span class="sxs-lookup"><span data-stu-id="f5e43-139">The **Journal lines** section shows each adjustment recorded by this journal.</span></span>
1. <span data-ttu-id="f5e43-140">Přihlaste se k centru.</span><span class="sxs-lookup"><span data-stu-id="f5e43-140">Sign in on the hub.</span></span>
1. <span data-ttu-id="f5e43-141">Přejděte na **Správa skladu \> Periodické úkoly \> Deník úprav skladových zásob**.</span><span class="sxs-lookup"><span data-stu-id="f5e43-141">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="f5e43-142">Na stránce **Deník úpravy skladových zásob**, pokud jste synchronizovali centrum a jednotku měřítka, měli byste vidět stejný deník.</span><span class="sxs-lookup"><span data-stu-id="f5e43-142">On the **Warehouse inventory adjustment journal** page, you should see the same journal listed if the hub and scale unit have synced.</span></span>
1. <span data-ttu-id="f5e43-143">Otevřít deník.</span><span class="sxs-lookup"><span data-stu-id="f5e43-143">Open the journal.</span></span> <span data-ttu-id="f5e43-144">Pokud byly [zprávy procesoru zprávy](cloud-edge-message-processor-messages.md) zpracovány, uvidíte odkazy na **Deník počítání** a **Ofsetový deník** v záhlaví.</span><span class="sxs-lookup"><span data-stu-id="f5e43-144">If the [message processor messages](cloud-edge-message-processor-messages.md) have been processed, you will see links to the **Counting journal** and the **Offset journal** in the header.</span></span>
    - <span data-ttu-id="f5e43-145">**Deník počítání** by měl zobrazovat stejné hodnoty dimenzí jako řádky deníku.</span><span class="sxs-lookup"><span data-stu-id="f5e43-145">The **Counting journal** should show the same dimension values as the journal lines.</span></span>
    - <span data-ttu-id="f5e43-146">**Ofsetový deník** by měl zobrazit offset, který odstraní úpravu zdvojení zásob.</span><span class="sxs-lookup"><span data-stu-id="f5e43-146">The **Offset journal** should show the offset, which removes the double inventory adjustment.</span></span>
    > [!NOTE]
    > <span data-ttu-id="f5e43-147">Když jsou veškerá synchronizace a zpracování dokončeny, **Deník počítání** a **Ofsetový deník** jsou synchronizovány zpět do jednotky škálování.</span><span class="sxs-lookup"><span data-stu-id="f5e43-147">When all syncing and processing is complete, the **Counting journal** and the **Offset journal** are synced back to the scale unit.</span></span> <span data-ttu-id="f5e43-148">Ty lze také zobrazit na příslušné stránce **Deník úpravy skladových zásob**.</span><span class="sxs-lookup"><span data-stu-id="f5e43-148">These can also be viewed from the relevant **Warehouse inventory adjustment journal** page.</span></span>
