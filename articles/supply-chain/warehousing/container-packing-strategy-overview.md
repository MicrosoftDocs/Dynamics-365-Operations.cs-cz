---
title: Strategie balení kontejnerů
description: Toto téma popisuje rozdíly mezi strategiemi balení kontejnerů a poskytuje příklady.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: article
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f481f6ca047ee0285fe0e81d8fa96665e9d27cee
ms.sourcegitcommit: 8e846b52763f90d2232ec7d427839f4722570bce
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/22/2021
ms.locfileid: "6292754"
---
# <a name="container-packing-strategies"></a><span data-ttu-id="00480-103">Strategie balení kontejnerů</span><span class="sxs-lookup"><span data-stu-id="00480-103">Container packing strategies</span></span>

<span data-ttu-id="00480-104">*Strategie balení kontejnerů* je strategie, kterou můžete použít k definování přidělení položek napříč kontejnery.</span><span class="sxs-lookup"><span data-stu-id="00480-104">A *container packing strategy* is a strategy that you can use to define item allocations across containers.</span></span> <span data-ttu-id="00480-105">Toto téma vysvětluje rozdíly mezi strategiemi *Zabalit do všech otevřených kontejnerů* a *Zabalit pouze do aktuálního kontejneru*.</span><span class="sxs-lookup"><span data-stu-id="00480-105">This topic explains the differences between the *Pack into all open containers* and *Pack into current container only* strategies.</span></span>

- <span data-ttu-id="00480-106">**Zabalit do všech otevřených kontejnerů** - Systém musí zkontrolovat všechny otevřené kontejnery, které již byly vytvořeny během cyklu kontejnerizace, aby se ujistil, že se položka vejde do jednoho z nich.</span><span class="sxs-lookup"><span data-stu-id="00480-106">**Pack into all open containers** – The system must check all open containers that have already been created during the containerization cycle, to make sure that the item will fit into one of them.</span></span> <span data-ttu-id="00480-107">Během balení systém kontroluje každou položku, aby určil, zda se vejde do některého z dříve vytvořených kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="00480-107">During packing, the system checks each item to determine whether it will fit into any of the previously created containers.</span></span> <span data-ttu-id="00480-108">Pokud se položka nevejde do existujícího kontejneru, systém vytvoří nový kontejner a pokračuje, dokud nedokončí zabalení celé objednávky.</span><span class="sxs-lookup"><span data-stu-id="00480-108">If the item won't fit into an existing container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="00480-109">Například *n* objednaných položek vyžaduje kontejnerizaci.</span><span class="sxs-lookup"><span data-stu-id="00480-109">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="00480-110">V nejhorším případě pokaždé, když systém zpracuje položku, která se nevejde do žádného existujícího kontejneru, provede celkem (\[(*n* - 1) × (*n* + 1)\] ÷ 2) kontrol, zda se položka vejde do existujících kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="00480-110">In the worst case, every time that the system processes an item that doesn't fit into any existing container, it will do a total of (\[(*n* – 1) × (*n* + 1)\] ÷ 2) checks to evaluate whether the item fits into the existing containers.</span></span>

- <span data-ttu-id="00480-111">**Zabalit pouze do aktuálního kontejneru** – Systém musí zkontrolovat pouze naposledy vytvořený kontejner, aby se ujistil, že se do něho položka vejde.</span><span class="sxs-lookup"><span data-stu-id="00480-111">**Pack into current container only** – The system must check only the most recently created container to make sure that the item will fit into it.</span></span> <span data-ttu-id="00480-112">Během balení systém kontroluje každou položku, aby určil, zda se vejde do naposledy vytvořeného kontejneru.</span><span class="sxs-lookup"><span data-stu-id="00480-112">During packing, the system checks each item to determine whether it will fit into the most recently created container.</span></span> <span data-ttu-id="00480-113">Pokud se položka nevejde do kontejneru, systém vytvoří nový kontejner a pokračuje, dokud nedokončí zabalení celé objednávky.</span><span class="sxs-lookup"><span data-stu-id="00480-113">If the item won't fit into that container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="00480-114">Například *n* objednaných položek vyžaduje kontejnerizaci.</span><span class="sxs-lookup"><span data-stu-id="00480-114">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="00480-115">V nejhorším případě systém udělá celkem (*n* - 1) kontrol, zda se předmět vejde do kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="00480-115">In the worst case, the system will do a total of (*n* – 1) checks to evaluate whether the item fits into the containers.</span></span>

## <a name="example-of-the-flow-for-container-packing-strategies"></a><span data-ttu-id="00480-116">Příklad postupu pro strategie balení kontejnerů</span><span class="sxs-lookup"><span data-stu-id="00480-116">Example of the flow for container packing strategies</span></span>

<span data-ttu-id="00480-117">Pro kontejnerizaci jste nastavili následující položky.</span><span class="sxs-lookup"><span data-stu-id="00480-117">You set up the following items for containerization.</span></span>

| <span data-ttu-id="00480-118">Zboží</span><span class="sxs-lookup"><span data-stu-id="00480-118">Item</span></span> | <span data-ttu-id="00480-119">Fyzické rozměry (šířka × hloubka × výška)</span><span class="sxs-lookup"><span data-stu-id="00480-119">Physical dimensions (width × depth × height)</span></span> | <span data-ttu-id="00480-120">Váha</span><span class="sxs-lookup"><span data-stu-id="00480-120">Weight</span></span> |
|---|---|---|
| <span data-ttu-id="00480-121">Kabel HDMI 6'</span><span class="sxs-lookup"><span data-stu-id="00480-121">HDMI Cable 6'</span></span> | <span data-ttu-id="00480-122">1 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="00480-122">1 × 1 × 1</span></span> | <span data-ttu-id="00480-123">1</span><span class="sxs-lookup"><span data-stu-id="00480-123">1</span></span> |
| <span data-ttu-id="00480-124">Kabel HDMI 12'</span><span class="sxs-lookup"><span data-stu-id="00480-124">HDMI Cable 12'</span></span> | <span data-ttu-id="00480-125">2 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="00480-125">2 × 1 × 1</span></span> | <span data-ttu-id="00480-126">1</span><span class="sxs-lookup"><span data-stu-id="00480-126">1</span></span> |
| <span data-ttu-id="00480-127">Kabel HDMI 18'</span><span class="sxs-lookup"><span data-stu-id="00480-127">HDMI Cable 18'</span></span> | <span data-ttu-id="00480-128">3 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="00480-128">3 × 1 × 1</span></span> | <span data-ttu-id="00480-129">2</span><span class="sxs-lookup"><span data-stu-id="00480-129">2</span></span> |

<span data-ttu-id="00480-130">Také nastavíte následující pole, které bude použito pro balení.</span><span class="sxs-lookup"><span data-stu-id="00480-130">You also set up the following box that will be used for packaging.</span></span>

| <span data-ttu-id="00480-131">Kontejner</span><span class="sxs-lookup"><span data-stu-id="00480-131">Container</span></span> | <span data-ttu-id="00480-132">Fyzické rozměry (délka × šířka × výška)</span><span class="sxs-lookup"><span data-stu-id="00480-132">Physical dimensions (length × width × height)</span></span> | <span data-ttu-id="00480-133">Váha</span><span class="sxs-lookup"><span data-stu-id="00480-133">Weight</span></span> | <span data-ttu-id="00480-134">Objem</span><span class="sxs-lookup"><span data-stu-id="00480-134">Volume</span></span> |
|---|---|---|---|
| <span data-ttu-id="00480-135">Střední box</span><span class="sxs-lookup"><span data-stu-id="00480-135">Medium Box</span></span> | <span data-ttu-id="00480-136">6 × 3 × 2</span><span class="sxs-lookup"><span data-stu-id="00480-136">6 × 3 × 2</span></span> | <span data-ttu-id="00480-137">10</span><span class="sxs-lookup"><span data-stu-id="00480-137">10</span></span> | <span data-ttu-id="00480-138">100</span><span class="sxs-lookup"><span data-stu-id="00480-138">100</span></span> |

<span data-ttu-id="00480-139">Nakonec nastavíte objednávku, která obsahuje následující produkty a množství.</span><span class="sxs-lookup"><span data-stu-id="00480-139">Finally, you set up an order that has the following products and quantities.</span></span>

| <span data-ttu-id="00480-140">Řádek prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="00480-140">Sales order line</span></span> | <span data-ttu-id="00480-141">Množství</span><span class="sxs-lookup"><span data-stu-id="00480-141">Quantity</span></span> |
|---|---|
| <span data-ttu-id="00480-142">Kabel HDMI 12'</span><span class="sxs-lookup"><span data-stu-id="00480-142">HDMI Cable 12'</span></span> | <span data-ttu-id="00480-143">9</span><span class="sxs-lookup"><span data-stu-id="00480-143">9</span></span> |
| <span data-ttu-id="00480-144">Kabel HDMI 18'</span><span class="sxs-lookup"><span data-stu-id="00480-144">HDMI Cable 18'</span></span> | <span data-ttu-id="00480-145">8</span><span class="sxs-lookup"><span data-stu-id="00480-145">8</span></span> |
| <span data-ttu-id="00480-146">Kabel HDMI 6'</span><span class="sxs-lookup"><span data-stu-id="00480-146">HDMI Cable 6'</span></span> | <span data-ttu-id="00480-147">13</span><span class="sxs-lookup"><span data-stu-id="00480-147">13</span></span> |

<span data-ttu-id="00480-148">Následující tabulka shrnuje, jak kontejnerizace funguje, když používáte strategii *Zabalit do všech otevřených kontejnerů* a když použijete strategii *Zabalit pouze do aktuálního kontejneru*.</span><span class="sxs-lookup"><span data-stu-id="00480-148">The following table summarizes how containerization works when you use the *Pack into all open containers* strategy and when you use the *Pack into current container only* strategy.</span></span>

| <span data-ttu-id="00480-149">Zabalit do všech otevřených kontejnerů</span><span class="sxs-lookup"><span data-stu-id="00480-149">Pack into all open containers</span></span> | <span data-ttu-id="00480-150">Zabalte do aktuálního kontejneru</span><span class="sxs-lookup"><span data-stu-id="00480-150">Pack into current container</span></span> |
|---|---|
| <p><span data-ttu-id="00480-151">Kabel HDMI 12':</span><span class="sxs-lookup"><span data-stu-id="00480-151">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="00480-152">Vytvoření nového kontejneru CONT0001.</span><span class="sxs-lookup"><span data-stu-id="00480-152">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="00480-153">Vložte 9 ea do kontejneru CONT0001.</span><span class="sxs-lookup"><span data-stu-id="00480-153">Put 9 ea into container CONT0001.</span></span></li></ol> | <p><span data-ttu-id="00480-154">Kabel HDMI 12':</span><span class="sxs-lookup"><span data-stu-id="00480-154">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="00480-155">Vytvoření nového kontejneru CONT0001.</span><span class="sxs-lookup"><span data-stu-id="00480-155">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="00480-156">Vložte 9 ea do kontejneru CONT0001.</span><span class="sxs-lookup"><span data-stu-id="00480-156">Put 9 ea into container CONT0001.</span></span></li></ol> |
| <p><span data-ttu-id="00480-157">Kabel HDMI 18':</span><span class="sxs-lookup"><span data-stu-id="00480-157">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="00480-158">Zkontrolujte, zda se položka vejde do kontejneru CONT0001.</span><span class="sxs-lookup"><span data-stu-id="00480-158">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="00480-159">Vytvoření nového kontejneru CONT0002.</span><span class="sxs-lookup"><span data-stu-id="00480-159">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="00480-160">Vložte 5 ea do kontejneru CONT0002.</span><span class="sxs-lookup"><span data-stu-id="00480-160">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="00480-161">Vytvoření nového kontejneru CONT0003.</span><span class="sxs-lookup"><span data-stu-id="00480-161">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="00480-162">Vložte 3 ea do kontejneru CONT0003.</span><span class="sxs-lookup"><span data-stu-id="00480-162">Put 3 ea into container CONT0003.</span></span></li></ol> | <p><span data-ttu-id="00480-163">Kabel HDMI 18':</span><span class="sxs-lookup"><span data-stu-id="00480-163">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="00480-164">Zkontrolujte, zda se položka vejde do kontejneru CONT0001.</span><span class="sxs-lookup"><span data-stu-id="00480-164">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="00480-165">Vytvoření nového kontejneru CONT0002.</span><span class="sxs-lookup"><span data-stu-id="00480-165">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="00480-166">Vložte 5 ea do kontejneru CONT0002.</span><span class="sxs-lookup"><span data-stu-id="00480-166">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="00480-167">Vytvoření nového kontejneru CONT0003.</span><span class="sxs-lookup"><span data-stu-id="00480-167">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="00480-168">Vložte 3 ea do kontejneru CONT0003.</span><span class="sxs-lookup"><span data-stu-id="00480-168">Put 3 ea into container CONT0003.</span></span></li></ol> |
| <p><span data-ttu-id="00480-169">Kabel HDMI 6':</span><span class="sxs-lookup"><span data-stu-id="00480-169">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="00480-170">Zkontrolujte, zda se položka vejde do kontejneru CONT0001.</span><span class="sxs-lookup"><span data-stu-id="00480-170">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="00480-171">Vložte 1 ea do kontejneru CONT0001.</span><span class="sxs-lookup"><span data-stu-id="00480-171">Put 1 ea into container CONT0001.</span></span></li><li><span data-ttu-id="00480-172">Zkontrolujte, zda se položka vejde do kontejneru CONT0002.</span><span class="sxs-lookup"><span data-stu-id="00480-172">Check whether the item can fit into container CONT0002.</span></span></li><li><span data-ttu-id="00480-173">Zkontrolujte, zda se položka vejde do kontejneru CONT0003.</span><span class="sxs-lookup"><span data-stu-id="00480-173">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="00480-174">Vložte 4 ea do kontejneru CONT0003.</span><span class="sxs-lookup"><span data-stu-id="00480-174">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="00480-175">Vytvoření nového kontejneru CONT0004.</span><span class="sxs-lookup"><span data-stu-id="00480-175">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="00480-176">Vložte 8 ea do kontejneru CONT0004.</span><span class="sxs-lookup"><span data-stu-id="00480-176">Put 8 ea into container CONT0004.</span></span></li></ol> | <p><span data-ttu-id="00480-177">Kabel HDMI 6':</span><span class="sxs-lookup"><span data-stu-id="00480-177">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="00480-178">Zkontrolujte, zda se položka vejde do kontejneru CONT0003.</span><span class="sxs-lookup"><span data-stu-id="00480-178">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="00480-179">Vložte 4 ea do kontejneru CONT0003.</span><span class="sxs-lookup"><span data-stu-id="00480-179">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="00480-180">Vytvoření nového kontejneru CONT0004.</span><span class="sxs-lookup"><span data-stu-id="00480-180">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="00480-181">Vložte 9 ea do kontejneru CONT0004.</span><span class="sxs-lookup"><span data-stu-id="00480-181">Put 9 ea into container CONT0004.</span></span></li></ol> |

## <a name="example-scenario-pack-single-orders-per-container"></a><span data-ttu-id="00480-182">Příklad scénáře: Balení jednotlivých objednávek na kontejner</span><span class="sxs-lookup"><span data-stu-id="00480-182">Example scenario: Pack single orders per container</span></span>

<span data-ttu-id="00480-183">Tato část představuje scénář, kdy je systém nastaven na konsolidaci více objednávek do jedné zásilky.</span><span class="sxs-lookup"><span data-stu-id="00480-183">This section presents a scenario where the system is set up to consolidate multiple orders into one shipment.</span></span> <span data-ttu-id="00480-184">Proto bude kontejnerizace provedena z prodejní objednávky, aby bylo zajištěno, že každá objednávka, která obsahuje více produktů, je zabalena do vlastního kontejneru.</span><span class="sxs-lookup"><span data-stu-id="00480-184">Therefore, containerization will be done from the sales order to ensure that every order that contains multiple products is packed into its own container.</span></span>

<span data-ttu-id="00480-185">Tato funkce umožňuje zpracovávat scénáře, kdy musíte do každého kontejneru zabalit pouze jednu prodejní objednávku, aby distribuční centrum mohlo provést cross docking plných kontejnerů mezi maloobchodními prodejnami.</span><span class="sxs-lookup"><span data-stu-id="00480-185">This functionality lets you handle scenarios where you must pack only one sales order into each container, so that the distribution center can cross-dock full containers between retail stores.</span></span> <span data-ttu-id="00480-186">Kromě scénářů maloobchodu (objednávka na maloobchod a dodávka do distribučního centra pro cross-docking) se tato technika také běžně používá v štíhlých dodavatelských řetězcích (prodejní objednávka na výrobní linku just-in-time).</span><span class="sxs-lookup"><span data-stu-id="00480-186">In addition to the retail scenarios (order per retail store and shipping to a distribution center for cross-docking) this technique is also commonly used in lean supply chains (sales order per just-in-time production line).</span></span>

<span data-ttu-id="00480-187">Tento scénář ukazuje, jak můžete pomocí aplikace snížit počet kontejnerů, které jsou vyhodnocovány během balení pomocí strategi *Zabalit pouze do aktuálního kontejneru* pro kontejnerizaci.</span><span class="sxs-lookup"><span data-stu-id="00480-187">This scenario shows how you can decrease the number of containers that are evaluated during packing by using the *Pack into current container only* strategy for containerization.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="00480-188">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="00480-188">Prerequisites</span></span>

#### <a name="turn-on-the-consolidate-shipments-feature-in-your-system"></a><span data-ttu-id="00480-189">Zapněte ve svém systému funkci Konsolidovat zásilky</span><span class="sxs-lookup"><span data-stu-id="00480-189">Turn on the Consolidate shipments feature in your system</span></span>

<span data-ttu-id="00480-190">Tento scénář používá funkci *Konsolidovat zásilky*.</span><span class="sxs-lookup"><span data-stu-id="00480-190">This scenario uses the *Consolidate shipments* feature.</span></span> <span data-ttu-id="00480-191">Pokud tato funkce ve vašem systému již není k dispozici, musíte ji zapnout pomocí [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="00480-191">If that feature isn't already available in your system, you must turn it on by using [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

#### <a name="make-demo-data-available"></a><span data-ttu-id="00480-192">Zpřístupnění ukázkových dat</span><span class="sxs-lookup"><span data-stu-id="00480-192">Make demo data available</span></span>

<span data-ttu-id="00480-193">Tento scénář odkazuje na hodnoty a záznamy, které jsou součástí standardních ukázkových dat poskytovaných pro aplikaci Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="00480-193">This scenario references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="00480-194">Pokud chcete při cvičení použít hodnoty, které jsou zde uvedeny, nezapomeňte pracovat v prostředí, ve kterém jsou nainstalovaná ukázková data, a nastavte právnickou osobu na **USMF**, než začnete.</span><span class="sxs-lookup"><span data-stu-id="00480-194">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

### <a name="inspect-or-create-container-types"></a><span data-ttu-id="00480-195">Zkontrolujte nebo vytvořte typy kontejnerů</span><span class="sxs-lookup"><span data-stu-id="00480-195">Inspect or create container types</span></span>

<span data-ttu-id="00480-196">Chcete-li zkontrolovat typy kontejnerů nebo vytvořit nové typy kontejnerů, pokud jsou požadovány, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="00480-196">To inspect your container types, or to create new container types if they are required, follow these steps.</span></span>

1. <span data-ttu-id="00480-197">Přejděte na **Řízení skladu** \> **Nastavení** \> **Kontejnery** \> **Typy kontejnerů**.</span><span class="sxs-lookup"><span data-stu-id="00480-197">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>
1. <span data-ttu-id="00480-198">Ujistěte se, že ve vašich ukázkových datech je k dispozici každý z následujících typů kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="00480-198">Make sure that each of the following container types is available in your demo data.</span></span> <span data-ttu-id="00480-199">Podle potřeby upravte nebo vytvořte typy kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="00480-199">Edit or create container types as required.</span></span>

    - <span data-ttu-id="00480-200">typ kontejneru 1:</span><span class="sxs-lookup"><span data-stu-id="00480-200">Container type 1:</span></span>

        - <span data-ttu-id="00480-201">**Kód typu kontejneru:** *Velká krabice*</span><span class="sxs-lookup"><span data-stu-id="00480-201">**Container type code:** *Box-Large*</span></span>
        - <span data-ttu-id="00480-202">**Popis:** *Velká krabice*</span><span class="sxs-lookup"><span data-stu-id="00480-202">**Description:** *Large Box*</span></span>
        - <span data-ttu-id="00480-203">**Maximální čistá hmotnost** *100*</span><span class="sxs-lookup"><span data-stu-id="00480-203">**Maximum net weight:** *100*</span></span>
        - <span data-ttu-id="00480-204">**Objem** *400*</span><span class="sxs-lookup"><span data-stu-id="00480-204">**Volume:** *400*</span></span>
        - <span data-ttu-id="00480-205">**Délka:** *4*</span><span class="sxs-lookup"><span data-stu-id="00480-205">**Length:** *4*</span></span>
        - <span data-ttu-id="00480-206">**Šířka:** *10*</span><span class="sxs-lookup"><span data-stu-id="00480-206">**Width:** *10*</span></span>
        - <span data-ttu-id="00480-207">**Výška:** *10*</span><span class="sxs-lookup"><span data-stu-id="00480-207">**Height:** *10*</span></span>

    - <span data-ttu-id="00480-208">typ kontejneru 2:</span><span class="sxs-lookup"><span data-stu-id="00480-208">Container type 2:</span></span>

        - <span data-ttu-id="00480-209">**Kód typu kontejneru:** *Střední krabice*</span><span class="sxs-lookup"><span data-stu-id="00480-209">**Container type code:** *Box-Medium*</span></span>
        - <span data-ttu-id="00480-210">**Popis:** *Střední box*</span><span class="sxs-lookup"><span data-stu-id="00480-210">**Description:** *Medium Box*</span></span>
        - <span data-ttu-id="00480-211">**Maximální čistá hmotnost** *50*</span><span class="sxs-lookup"><span data-stu-id="00480-211">**Maximum net weight:** *50*</span></span>
        - <span data-ttu-id="00480-212">**Objem** *200*</span><span class="sxs-lookup"><span data-stu-id="00480-212">**Volume:** *200*</span></span>
        - <span data-ttu-id="00480-213">**Délka:** *2*</span><span class="sxs-lookup"><span data-stu-id="00480-213">**Length:** *2*</span></span>
        - <span data-ttu-id="00480-214">**Šířka:** *10*</span><span class="sxs-lookup"><span data-stu-id="00480-214">**Width:** *10*</span></span>
        - <span data-ttu-id="00480-215">**Výška:** *10*</span><span class="sxs-lookup"><span data-stu-id="00480-215">**Height:** *10*</span></span>

    - <span data-ttu-id="00480-216">typ kontejneru 3:</span><span class="sxs-lookup"><span data-stu-id="00480-216">Container type 3:</span></span>

        - <span data-ttu-id="00480-217">**Kód typu kontejneru:** *Malá krabice*</span><span class="sxs-lookup"><span data-stu-id="00480-217">**Container type code:** *Box-Small*</span></span>
        - <span data-ttu-id="00480-218">**Popis:** *Malá krabice*</span><span class="sxs-lookup"><span data-stu-id="00480-218">**Description:** *Small Box*</span></span>
        - <span data-ttu-id="00480-219">**Maximální čistá hmotnost** *20*</span><span class="sxs-lookup"><span data-stu-id="00480-219">**Maximum net weight:** *20*</span></span>
        - <span data-ttu-id="00480-220">**Objem** *100*</span><span class="sxs-lookup"><span data-stu-id="00480-220">**Volume:** *100*</span></span>
        - <span data-ttu-id="00480-221">**Délka:** *1*</span><span class="sxs-lookup"><span data-stu-id="00480-221">**Length:** *1*</span></span>
        - <span data-ttu-id="00480-222">**Šířka:** *10*</span><span class="sxs-lookup"><span data-stu-id="00480-222">**Width:** *10*</span></span>
        - <span data-ttu-id="00480-223">**Výška:** *10*</span><span class="sxs-lookup"><span data-stu-id="00480-223">**Height:** *10*</span></span>

### <a name="inspect-or-create-container-groups"></a><span data-ttu-id="00480-224">Zkontrolujte nebo vytvořte skupiny kontejnerů</span><span class="sxs-lookup"><span data-stu-id="00480-224">Inspect or create container groups</span></span>

<span data-ttu-id="00480-225">Chcete-li zkontrolovat skupiny kontejnerů nebo vytvořit nové skupiny kontejnerů, pokud jsou požadovány, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="00480-225">To inspect your container groups, or to create new container groups if they are required, follow these steps.</span></span>

1. <span data-ttu-id="00480-226">Přejděte na **Řízení skladu** \> **Nastavení** \> **Kontejnery** \> **Skupiny kontejnerů**.</span><span class="sxs-lookup"><span data-stu-id="00480-226">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**.</span></span>
1. <span data-ttu-id="00480-227">Ujistěte se, že ve vašich ukázkových datech je k dispozici každá z následujících skupin kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="00480-227">Make sure that the following container group is available in your demo data.</span></span> <span data-ttu-id="00480-228">Pokud není k dispozici, vyberte **Nový** a vytvořte jej.</span><span class="sxs-lookup"><span data-stu-id="00480-228">If it isn't available, select **New** to create it.</span></span>

    - <span data-ttu-id="00480-229">**ID skupiny kontejnerů:** *Krabice*</span><span class="sxs-lookup"><span data-stu-id="00480-229">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="00480-230">**Popis:** *Velikosti krabic*</span><span class="sxs-lookup"><span data-stu-id="00480-230">**Description:** *Box sizes*</span></span>

1. <span data-ttu-id="00480-231">Na pevné záložce **Podrobnosti** pro skupinu kontejnerů *Krabice* se ujistěte, že existují následující řádky.</span><span class="sxs-lookup"><span data-stu-id="00480-231">On the **Details** FastTab for the *Boxes* container group, make sure that the following lines exist.</span></span> <span data-ttu-id="00480-232">Pokud ne, vyberte **Nový** a přidejte je.</span><span class="sxs-lookup"><span data-stu-id="00480-232">If they don't, select **New** to add them.</span></span>

    - <span data-ttu-id="00480-233">Řádek 1:</span><span class="sxs-lookup"><span data-stu-id="00480-233">Line 1:</span></span>

        - <span data-ttu-id="00480-234">**Pořadové číslo:** *1*</span><span class="sxs-lookup"><span data-stu-id="00480-234">**Sequence number:** *1*</span></span>
        - <span data-ttu-id="00480-235">**Typ kontejneru:** *Velká krabice*</span><span class="sxs-lookup"><span data-stu-id="00480-235">**Container type:** *Box-Large*</span></span>
        - <span data-ttu-id="00480-236">**Procento využití kontejneru:** *100*</span><span class="sxs-lookup"><span data-stu-id="00480-236">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="00480-237">Řádek 2:</span><span class="sxs-lookup"><span data-stu-id="00480-237">Line 2:</span></span>

        - <span data-ttu-id="00480-238">**Pořadové číslo:** *2*</span><span class="sxs-lookup"><span data-stu-id="00480-238">**Sequence number:** *2*</span></span>
        - <span data-ttu-id="00480-239">**Typ kontejneru:** *Střední krabice*</span><span class="sxs-lookup"><span data-stu-id="00480-239">**Container type:** *Box-Medium*</span></span>
        - <span data-ttu-id="00480-240">**Procento využití kontejneru:** *100*</span><span class="sxs-lookup"><span data-stu-id="00480-240">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="00480-241">Řádek 3:</span><span class="sxs-lookup"><span data-stu-id="00480-241">Line 3:</span></span>

        - <span data-ttu-id="00480-242">**Pořadové číslo:** *3*</span><span class="sxs-lookup"><span data-stu-id="00480-242">**Sequence number:** *3*</span></span>
        - <span data-ttu-id="00480-243">**Typ kontejneru:** *Malá krabice*</span><span class="sxs-lookup"><span data-stu-id="00480-243">**Container type:** *Box-Small*</span></span>
        - <span data-ttu-id="00480-244">**Procento využití kontejneru:** *100*</span><span class="sxs-lookup"><span data-stu-id="00480-244">**Container utilization percentage:** *100*</span></span>

### <a name="create-a-new-container-build-template"></a><span data-ttu-id="00480-245">Vytvořte novou šablonu sestavení kontejneru</span><span class="sxs-lookup"><span data-stu-id="00480-245">Create a new container build template</span></span>

<span data-ttu-id="00480-246">Chcete-li vytvořit novou šablonu sestavení kontejneru, postupujte podle následujících pokynů.</span><span class="sxs-lookup"><span data-stu-id="00480-246">To create a new container build template, follow these steps.</span></span>

1. <span data-ttu-id="00480-247">Přejděte na **Řízení skladu** \> **Nastavení** \> **Kontejnery** \> **Šablona sestavení kontejneru**.</span><span class="sxs-lookup"><span data-stu-id="00480-247">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container build template**.</span></span>
1. <span data-ttu-id="00480-248">Vyberte **Nový** k vytvoření šablony sestavení kontejneru, která má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="00480-248">Select **New** to create a container build template that has the following settings:</span></span>

    - <span data-ttu-id="00480-249">**Pořadové číslo:** *1*</span><span class="sxs-lookup"><span data-stu-id="00480-249">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="00480-250">**ID šablony kontejneru:** *Krabice*</span><span class="sxs-lookup"><span data-stu-id="00480-250">**Container template ID:** *Box*</span></span>
    - <span data-ttu-id="00480-251">**ID skupiny kontejnerů:** *Krabice*</span><span class="sxs-lookup"><span data-stu-id="00480-251">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="00480-252">**Základní typy dotazů:** *Řádek přidělení prodeje*</span><span class="sxs-lookup"><span data-stu-id="00480-252">**Base query types:** *Sales allocation line*</span></span>
    - <span data-ttu-id="00480-253">**Kód kroku vlny:** *234*</span><span class="sxs-lookup"><span data-stu-id="00480-253">**Wave step code:** *234*</span></span>
    - <span data-ttu-id="00480-254">**Povolit rozdělení výdejů:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="00480-254">**Allow split picks:** *Yes*</span></span>
    - <span data-ttu-id="00480-255">**Strategie balení kontejneru:** *Zabalit pouze do aktuálního kontejneru*</span><span class="sxs-lookup"><span data-stu-id="00480-255">**Container packing strategy:** *Pack into current container only*</span></span>
    - <span data-ttu-id="00480-256">**Balení podle direktivní jednotky:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="00480-256">**Pack by directive unit:** *No*</span></span>

1. <span data-ttu-id="00480-257">Zatímco je stále vybrán řádek pro novou šablonu, vyberte v podokně akcí možnost **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="00480-257">While the row for the new template is still selected, select **Edit query** on the Action Pane.</span></span>
1. <span data-ttu-id="00480-258">Zobrazí se standardní dialogové okno editoru dotazů.</span><span class="sxs-lookup"><span data-stu-id="00480-258">A standard query editor dialog box appears.</span></span> <span data-ttu-id="00480-259">Na kartě **Řazení** vyberte **Přidat** a přidejte řádek, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="00480-259">On the **Sorting** tab, select **Add** to add a row that has the following settings:</span></span>

    - <span data-ttu-id="00480-260">**Tabulka:** *Dočasné pracovní transakce*</span><span class="sxs-lookup"><span data-stu-id="00480-260">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="00480-261">**Odvozená tabulka:** *Dočasné pracovní transakce*</span><span class="sxs-lookup"><span data-stu-id="00480-261">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="00480-262">**Pole:** *Číslo objednávky*</span><span class="sxs-lookup"><span data-stu-id="00480-262">**Field:** *Order number*</span></span>
    - <span data-ttu-id="00480-263">**Směr hledání:** *Vzestupně*</span><span class="sxs-lookup"><span data-stu-id="00480-263">**Search direction:** *Ascending*</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="00480-264">Chcete-li se vyhnout cyklování nad všemi ostatními otevřenými kontejnery a urychlit proces kontrolou jednoho kontejneru po druhém, použijte strategii *Zabalit pouze do aktuálního kontejneru* kromě třídění podle čísla objednávky.</span><span class="sxs-lookup"><span data-stu-id="00480-264">To avoid cycling over all the other open containers, and to speed up the process by checking one container at a time, use the *Pack into current container only* strategy in addition to sorting by order number.</span></span> <span data-ttu-id="00480-265">Tato kombinace bude fungovat jako pracovní přestávka na pracovní šabloně.</span><span class="sxs-lookup"><span data-stu-id="00480-265">This combination will work like a work break on a work template.</span></span>

1. <span data-ttu-id="00480-266">Vyberte **OK** a dialogové okno editor dotazu zavřete.</span><span class="sxs-lookup"><span data-stu-id="00480-266">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="00480-267">Zatímco je stále vybrán řádek pro novou šablonu, vyberte v podokně akcí možnost **Omezení kombinování obsahu kontejnerů**.</span><span class="sxs-lookup"><span data-stu-id="00480-267">While the row for the new template is still selected, select **Container mixing constraints** on the Action Pane.</span></span>

    <span data-ttu-id="00480-268">Nyní přidáte omezení, které vloží položky z jedné objednávky do jednoho kontejneru.</span><span class="sxs-lookup"><span data-stu-id="00480-268">You will now add a constraint that puts items from a single order into a single container.</span></span> <span data-ttu-id="00480-269">Položky z jakékoli jiné objednávky budou vloženy do samostatného kontejneru.</span><span class="sxs-lookup"><span data-stu-id="00480-269">Items from any other order will be put into a separate container.</span></span>

1. <span data-ttu-id="00480-270">Vyberte **Nový** k vytvoření omezení kombinování, které má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="00480-270">Select **New** to create a mixing constraint that has the following settings:</span></span>

    - <span data-ttu-id="00480-271">**Tabulka:** *Prodejní objednávky*</span><span class="sxs-lookup"><span data-stu-id="00480-271">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="00480-272">**Výběr pole:** *SalesId* (Pole se zobrazí jako *Prodejní objednávka* v mřížce.)</span><span class="sxs-lookup"><span data-stu-id="00480-272">**Field select:** *SalesId* (The field will appear as *Sales order* in the grid.)</span></span>

1. <span data-ttu-id="00480-273">Zvolte **OK** pro přidání omezení.</span><span class="sxs-lookup"><span data-stu-id="00480-273">Select **OK** to add the constraint.</span></span>
1. <span data-ttu-id="00480-274">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="00480-274">Close the page.</span></span>

### <a name="set-up-a-wave-template-for-containerization"></a><span data-ttu-id="00480-275">Nastavení šablony vlny pro rozdělení do kontejnerů</span><span class="sxs-lookup"><span data-stu-id="00480-275">Set up a wave template for containerization</span></span>

<span data-ttu-id="00480-276">Chcete-li nastavit šablonu vlny, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="00480-276">To set up a wave template, follow these steps.</span></span>

1. <span data-ttu-id="00480-277">Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny**.</span><span class="sxs-lookup"><span data-stu-id="00480-277">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="00480-278">V podokně seznamů nastavte v poli **Typ šablony vlny** na hodnotu *Dodávka*.</span><span class="sxs-lookup"><span data-stu-id="00480-278">In the list pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="00480-279">Vyberte šablonu **Kontejnerizace 63** v seznamu.</span><span class="sxs-lookup"><span data-stu-id="00480-279">Select the **63 Containerization** template in the list.</span></span>
1. <span data-ttu-id="00480-280">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="00480-280">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="00480-281">Na pevné záložce **Metody** ve sloupci **Vybrané metody** najděte následující řádek:</span><span class="sxs-lookup"><span data-stu-id="00480-281">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="00480-282">**Název metody:** *kontejnerizace*</span><span class="sxs-lookup"><span data-stu-id="00480-282">**Method name:** *containerization*</span></span>
    - <span data-ttu-id="00480-283">**Název:** *Kontejnerizace*</span><span class="sxs-lookup"><span data-stu-id="00480-283">**Name:** *Containerization*</span></span>

1. <span data-ttu-id="00480-284">Nastavte pole **Kód kroku vlny** pro řádek na *234*.</span><span class="sxs-lookup"><span data-stu-id="00480-284">Set the **Wave step code** field for the line to *234*.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="00480-285">Nastavit šablonu práce</span><span class="sxs-lookup"><span data-stu-id="00480-285">Set up a work template</span></span>

<span data-ttu-id="00480-286">Chcete-li nastavit šablonu práce, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="00480-286">To set up a work template, follow these steps.</span></span>

1. <span data-ttu-id="00480-287">Přejděte do **Řízení skladu \> Nastavení \> Práce \> Pracovní šablony**.</span><span class="sxs-lookup"><span data-stu-id="00480-287">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="00480-288">Pole **Typ pracovního příkazu** nastavte na *Prodejní objednávky*.</span><span class="sxs-lookup"><span data-stu-id="00480-288">Set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="00480-289">V mřížce **Přehled** vyhledejte a vyberte pracovní šablonu, která by měla být použita pro balení jednorázových objednávek na kontejner.</span><span class="sxs-lookup"><span data-stu-id="00480-289">In the **Overview** grid, find and select the work template that should be used for packing single orders per container.</span></span> <span data-ttu-id="00480-290">V tomto scénáři vyberte šablonu **63 vydat pro kontejner**.</span><span class="sxs-lookup"><span data-stu-id="00480-290">For this scenario, select the **63 Pick to container** template.</span></span>
1. <span data-ttu-id="00480-291">V podokně akcí vyberte **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="00480-291">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="00480-292">Zobrazí se standardní dialogové okno editoru dotazů.</span><span class="sxs-lookup"><span data-stu-id="00480-292">A standard query editor dialog box appears.</span></span> <span data-ttu-id="00480-293">Na kartě **Řazení** přidejte následující řádky:</span><span class="sxs-lookup"><span data-stu-id="00480-293">On the **Sorting** tab, add the following lines:</span></span>

    - <span data-ttu-id="00480-294">Řádek 1:</span><span class="sxs-lookup"><span data-stu-id="00480-294">Line 1:</span></span>

        - <span data-ttu-id="00480-295">**Tabulka:** *Dočasné pracovní transakce*</span><span class="sxs-lookup"><span data-stu-id="00480-295">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="00480-296">**Odvozená tabulka:** *Dočasné pracovní transakce*</span><span class="sxs-lookup"><span data-stu-id="00480-296">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="00480-297">**Pole:** *ID dodávky*</span><span class="sxs-lookup"><span data-stu-id="00480-297">**Field:** *Shipment ID*</span></span>
        - <span data-ttu-id="00480-298">**Směr hledání:** *Vzestupně*</span><span class="sxs-lookup"><span data-stu-id="00480-298">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="00480-299">Řádek 2:</span><span class="sxs-lookup"><span data-stu-id="00480-299">Line 2:</span></span>

        - <span data-ttu-id="00480-300">**Tabulka:** *Dočasné pracovní transakce*</span><span class="sxs-lookup"><span data-stu-id="00480-300">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="00480-301">**Odvozená tabulka:** *Dočasné pracovní transakce*</span><span class="sxs-lookup"><span data-stu-id="00480-301">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="00480-302">**Pole:** *Číslo objednávky*</span><span class="sxs-lookup"><span data-stu-id="00480-302">**Field:** *Order number*</span></span>
        - <span data-ttu-id="00480-303">**Směr hledání:** *Vzestupně*</span><span class="sxs-lookup"><span data-stu-id="00480-303">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="00480-304">Řádek 3:</span><span class="sxs-lookup"><span data-stu-id="00480-304">Line 3:</span></span>

        - <span data-ttu-id="00480-305">**Tabulka:** *Dočasné pracovní transakce*</span><span class="sxs-lookup"><span data-stu-id="00480-305">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="00480-306">**Odvozená tabulka:** *Dočasné pracovní transakce*</span><span class="sxs-lookup"><span data-stu-id="00480-306">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="00480-307">**Pole:** *ID kontejneru*</span><span class="sxs-lookup"><span data-stu-id="00480-307">**Field:** *Container ID*</span></span>
        - <span data-ttu-id="00480-308">**Směr hledání:** *Vzestupně*</span><span class="sxs-lookup"><span data-stu-id="00480-308">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="00480-309">Vyberte **OK** a dialogové okno editor dotazu zavřete.</span><span class="sxs-lookup"><span data-stu-id="00480-309">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="00480-310">Může se zobrazit následující zpráva: „Seskupení bude resetováno, pokračovat?“</span><span class="sxs-lookup"><span data-stu-id="00480-310">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="00480-311">Pokračujte výběrem tlačítka **Ano**.</span><span class="sxs-lookup"><span data-stu-id="00480-311">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="00480-312">Zatímco šablona **63 Výdej do kontejneru** je stále vybrána, vyberte **Přerušení pracovního záhlaví** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="00480-312">While the **63 Pick to container** template is still selected, select **Work header breaks** on the Action Pane.</span></span>

    <span data-ttu-id="00480-313">Nyní použijete nastavení pro přerušení práce tak, aby každý kontejner v objednávce byl propojen s jedním pracovním příkazem.</span><span class="sxs-lookup"><span data-stu-id="00480-313">You will now apply settings to break the work so that each container in the order is linked to one work order.</span></span>

1. <span data-ttu-id="00480-314">Zaškrtněte políčko **Seskupit podle tohoto pole** pro každý řádek na stránce **Přerušení pracovního záhlaví** (**ID zásilky**, **Číslo objednávky** a **ID kontejneru**).</span><span class="sxs-lookup"><span data-stu-id="00480-314">Select the **Group by this field** checkbox for each row on the **Work header breaks** page (**Shipment ID**, **Order number**, and **Container ID**).</span></span>
1. <span data-ttu-id="00480-315">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="00480-315">Close the page.</span></span>

### <a name="set-up-shipment-consolidation-policies"></a><span data-ttu-id="00480-316">Nastavit zásady konsolidace dodávek</span><span class="sxs-lookup"><span data-stu-id="00480-316">Set up shipment consolidation policies</span></span>

<span data-ttu-id="00480-317">Pokud chcete nastavit zásady konsolidace dodávky, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="00480-317">To set up a shipment consolidation policy, follow these steps.</span></span>

1. <span data-ttu-id="00480-318">Přejděte na **Řízení skladu \> Nastavit \> Uvolnění do skladu \> Zásady konsolidace dodávek**.</span><span class="sxs-lookup"><span data-stu-id="00480-318">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="00480-319">V podokně seznamu nastavte pole **Typ zásad** na *Prodejní objednávky*.</span><span class="sxs-lookup"><span data-stu-id="00480-319">In the list pane, set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="00480-320">Vyberte **Výchozí** zásady v seznamu.</span><span class="sxs-lookup"><span data-stu-id="00480-320">Select the **Default** policy in the list.</span></span>
1. <span data-ttu-id="00480-321">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="00480-321">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="00480-322">Na záložce s náhledem **Pole konsolidace** v seznamu **Vybraná pole** vyberte řádek, ve kterém je pole **Název pole** nastaveno na *Číslo objednávky*.</span><span class="sxs-lookup"><span data-stu-id="00480-322">On the **Consolidation fields** FastTab, in the **Selected fields** list, select the row where the **Field name** field is set to *Order number*.</span></span>
1. <span data-ttu-id="00480-323">Vyberte tlačítko **Odebrat** ![Levá šipka](media/backward-button.png) a přesuňte do seznamu **Zbývající pole**.</span><span class="sxs-lookup"><span data-stu-id="00480-323">Select the **Remove** button ![Left arrow](media/backward-button.png) to move the field to the **Remaining fields** list.</span></span>
1. <span data-ttu-id="00480-324">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="00480-324">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-physical-dimensions-for-the-product"></a><span data-ttu-id="00480-325">Nastavit fyzické rozměry produktu.</span><span class="sxs-lookup"><span data-stu-id="00480-325">Set up physical dimensions for the product</span></span>

<span data-ttu-id="00480-326">Chcete-li nastavit fyzické dimenze pro produkty, které budou použity v tomto scénáři, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="00480-326">To set up physical dimensions for the products that will be used in this scenario, follow these steps.</span></span>

1. <span data-ttu-id="00480-327">Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="00480-327">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="00480-328">Vyberte produkt, kde je pole **Číslo položky** nastaveno na *A0001*.</span><span class="sxs-lookup"><span data-stu-id="00480-328">Select the product where the **Item number** field is set to *A0001*.</span></span>
1. <span data-ttu-id="00480-329">V podokně Akce na kartě **Správa zásob** ve skupině **Sklad** vyberte **Fyzické rozměry**.</span><span class="sxs-lookup"><span data-stu-id="00480-329">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="00480-330">Na stránce **Fyzické rozměry** byste měli vidět následující řádek v mřížce:</span><span class="sxs-lookup"><span data-stu-id="00480-330">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="00480-331">**Jednotka:** *ks*</span><span class="sxs-lookup"><span data-stu-id="00480-331">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="00480-332">**Hrubá hmotnost:** *3.00*</span><span class="sxs-lookup"><span data-stu-id="00480-332">**Gross weight:** *3.00*</span></span>
    - <span data-ttu-id="00480-333">**Šířka:** *2.00*</span><span class="sxs-lookup"><span data-stu-id="00480-333">**Width:** *2.00*</span></span>
    - <span data-ttu-id="00480-334">**Hloubka:** *2.00*</span><span class="sxs-lookup"><span data-stu-id="00480-334">**Depth:** *2.00*</span></span>
    - <span data-ttu-id="00480-335">**Výška:** *4.00*</span><span class="sxs-lookup"><span data-stu-id="00480-335">**Height:** *4.00*</span></span>
    - <span data-ttu-id="00480-336">**Objem** *16.00*</span><span class="sxs-lookup"><span data-stu-id="00480-336">**Volume:** *16.00*</span></span>

1. <span data-ttu-id="00480-337">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="00480-337">Close the page.</span></span>
1. <span data-ttu-id="00480-338">Vyberte produkt, kde je pole **Číslo položky** nastaveno na *A0002*.</span><span class="sxs-lookup"><span data-stu-id="00480-338">Select the product where the **Item number** field is set to *A0002*.</span></span>
1. <span data-ttu-id="00480-339">V podokně Akce na kartě **Správa zásob** ve skupině **Sklad** vyberte **Fyzické rozměry**.</span><span class="sxs-lookup"><span data-stu-id="00480-339">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="00480-340">Na stránce **Fyzické rozměry** byste měli vidět následující řádek v mřížce:</span><span class="sxs-lookup"><span data-stu-id="00480-340">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="00480-341">**Jednotka:** *ks*</span><span class="sxs-lookup"><span data-stu-id="00480-341">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="00480-342">**Hrubá hmotnost:** *4.00*</span><span class="sxs-lookup"><span data-stu-id="00480-342">**Gross weight:** *4.00*</span></span>
    - <span data-ttu-id="00480-343">**Šířka:** *3.00*</span><span class="sxs-lookup"><span data-stu-id="00480-343">**Width:** *3.00*</span></span>
    - <span data-ttu-id="00480-344">**Hloubka:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="00480-344">**Depth:** *1.00*</span></span>
    - <span data-ttu-id="00480-345">**Výška:** *3.00*</span><span class="sxs-lookup"><span data-stu-id="00480-345">**Height:** *3.00*</span></span>
    - <span data-ttu-id="00480-346">**Objem** *9.00*</span><span class="sxs-lookup"><span data-stu-id="00480-346">**Volume:** *9.00*</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="00480-347">Vytvoření prodejní objednávky 1</span><span class="sxs-lookup"><span data-stu-id="00480-347">Create sales order 1</span></span>

<span data-ttu-id="00480-348">Chcete-li vytvořit prodejní objednávku, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="00480-348">To create a sales order, follow these steps.</span></span>

1. <span data-ttu-id="00480-349">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="00480-349">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="00480-350">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="00480-350">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="00480-351">Zobrazí se dialogové okno pro vytvoření nové prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="00480-351">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="00480-352">Nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="00480-352">Set the following values:</span></span>

    - <span data-ttu-id="00480-353">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="00480-353">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="00480-354">**Sklad:** *63*</span><span class="sxs-lookup"><span data-stu-id="00480-354">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="00480-355">Vyberte **OK**, prodejní objednávka se vytvoří a dialogové okno se zavře.</span><span class="sxs-lookup"><span data-stu-id="00480-355">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="00480-356">Otevře se nová prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="00480-356">The new sales order is opened.</span></span> <span data-ttu-id="00480-357">Na kartě s náhledem **Řádky prodejní objednávky** přidejte následující prodejní řádky:</span><span class="sxs-lookup"><span data-stu-id="00480-357">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="00480-358">Řádek 1:</span><span class="sxs-lookup"><span data-stu-id="00480-358">Line 1:</span></span>

        - <span data-ttu-id="00480-359">**Číslo položky:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="00480-359">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="00480-360">**Množství:** *2*</span><span class="sxs-lookup"><span data-stu-id="00480-360">**Quantity:** *2*</span></span>

    - <span data-ttu-id="00480-361">Řádek 2:</span><span class="sxs-lookup"><span data-stu-id="00480-361">Line 2:</span></span>

        - <span data-ttu-id="00480-362">**Číslo položky:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="00480-362">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="00480-363">**Množství:** *2*</span><span class="sxs-lookup"><span data-stu-id="00480-363">**Quantity:** *2*</span></span>

1. <span data-ttu-id="00480-364">Vyberte první řádek a poté vyberte **Zásoby \> Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="00480-364">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="00480-365">Na stránce **Rezervace** vyberte možnost **Rezervovat šarži**.</span><span class="sxs-lookup"><span data-stu-id="00480-365">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="00480-366">Poté stránku zavřete.</span><span class="sxs-lookup"><span data-stu-id="00480-366">Then close the page.</span></span>
1. <span data-ttu-id="00480-367">Opakujte předchozí dva kroky pro druhý řádek.</span><span class="sxs-lookup"><span data-stu-id="00480-367">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="00480-368">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="00480-368">Close the page.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="00480-369">Vytvoření prodejní objednávky 2</span><span class="sxs-lookup"><span data-stu-id="00480-369">Create sales order 2</span></span>

<span data-ttu-id="00480-370">Chcete-li vytvořit druhou prodejní objednávku, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="00480-370">To create a second sales order, follow these steps.</span></span>

1. <span data-ttu-id="00480-371">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="00480-371">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="00480-372">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="00480-372">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="00480-373">Zobrazí se dialogové okno pro vytvoření nové prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="00480-373">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="00480-374">Nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="00480-374">Set the following values:</span></span>

    - <span data-ttu-id="00480-375">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="00480-375">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="00480-376">**Sklad:** *63*</span><span class="sxs-lookup"><span data-stu-id="00480-376">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="00480-377">Vyberte **OK**, prodejní objednávka se vytvoří a dialogové okno se zavře.</span><span class="sxs-lookup"><span data-stu-id="00480-377">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="00480-378">Otevře se nová prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="00480-378">The new sales order is opened.</span></span> <span data-ttu-id="00480-379">Na kartě s náhledem **Řádky prodejní objednávky** přidejte následující prodejní řádky:</span><span class="sxs-lookup"><span data-stu-id="00480-379">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="00480-380">Řádek 1:</span><span class="sxs-lookup"><span data-stu-id="00480-380">Line 1:</span></span>

        - <span data-ttu-id="00480-381">**Číslo položky:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="00480-381">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="00480-382">**Množství:** *4*</span><span class="sxs-lookup"><span data-stu-id="00480-382">**Quantity:** *4*</span></span>

    - <span data-ttu-id="00480-383">Řádek 2:</span><span class="sxs-lookup"><span data-stu-id="00480-383">Line 2:</span></span>

        - <span data-ttu-id="00480-384">**Číslo položky:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="00480-384">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="00480-385">**Množství:** *4*</span><span class="sxs-lookup"><span data-stu-id="00480-385">**Quantity:** *4*</span></span>

1. <span data-ttu-id="00480-386">Vyberte první řádek a poté vyberte **Zásoby \> Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="00480-386">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="00480-387">Na stránce **Rezervace** vyberte možnost **Rezervovat šarži**.</span><span class="sxs-lookup"><span data-stu-id="00480-387">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="00480-388">Poté stránku zavřete.</span><span class="sxs-lookup"><span data-stu-id="00480-388">Then close the page.</span></span>
1. <span data-ttu-id="00480-389">Opakujte předchozí dva kroky pro druhý řádek.</span><span class="sxs-lookup"><span data-stu-id="00480-389">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="00480-390">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="00480-390">Close the page.</span></span>

### <a name="create-the-load"></a><span data-ttu-id="00480-391">Vytvoření vytížení</span><span class="sxs-lookup"><span data-stu-id="00480-391">Create the load</span></span>

<span data-ttu-id="00480-392">Chcete-li vytvořit náklad pro každou sadu objednávek, kterou jste vytvořili pro tento scénář, a poté ji uvolnit do skladu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="00480-392">To create a load for each order that you created for this scenario and then release it to the warehouse, follow these steps.</span></span>

1. <span data-ttu-id="00480-393">Přejděte do **Řízení skladu \> Náklady \> Pracovní plocha plánování nákladu**.</span><span class="sxs-lookup"><span data-stu-id="00480-393">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="00480-394">Na kartě **Řádky prodeje** najděte a vyberte všechny řádky prodejních objednávek z prodejních objednávek, které jste pro tento scénář vytvořili.</span><span class="sxs-lookup"><span data-stu-id="00480-394">On the **Sales lines** tab, find and select all the sales order lines from the sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="00480-395">V podokně Akce na kartě **Nabídka a poptávka** vyberte ve skupině **Přidat** možnost **Do nového vytížení**.</span><span class="sxs-lookup"><span data-stu-id="00480-395">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span> <span data-ttu-id="00480-396">Vybrané řádky objednávky se přidají k novému nákladu.</span><span class="sxs-lookup"><span data-stu-id="00480-396">The selected order lines are added to a new load.</span></span>
1. <span data-ttu-id="00480-397">V dialogovém okně **Přiřazení šablony nákladu** v poli **ID šablony nákladu** vyberte šablonu nákladu, například *Kontejner 40'*.</span><span class="sxs-lookup"><span data-stu-id="00480-397">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *40' Container*.</span></span>
1. <span data-ttu-id="00480-398">Zvolte **OK** a zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="00480-398">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="00480-399">V části **Náklady** vyhledejte a vyberte náklad, který jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="00480-399">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="00480-400">Vyberte **Uvolnění \> Uvolnění do skladu**.</span><span class="sxs-lookup"><span data-stu-id="00480-400">Select **Release \> Release to warehouse**.</span></span>
1. <span data-ttu-id="00480-401">V dialogovém okně **Uvolnění do skladu** vyberte **OK** pro uvolnění vybraného nákladu do skladu.</span><span class="sxs-lookup"><span data-stu-id="00480-401">In the **Release to warehouse** dialog box, select **OK** to release the selected load to the warehouse.</span></span>

### <a name="verify-the-shipments-and-containers"></a><span data-ttu-id="00480-402">Ověřte zásilky a kontejnery</span><span class="sxs-lookup"><span data-stu-id="00480-402">Verify the shipments and containers</span></span>

<span data-ttu-id="00480-403">Následující postup vám umožní ověřit vytvořené zásilky.</span><span class="sxs-lookup"><span data-stu-id="00480-403">The following procedure lets you verify the shipments that have been created.</span></span> <span data-ttu-id="00480-404">Použijte jej ke kontrole objednávky, kterou jste vytvořili pro tento scénář, abyste se ujistili, že jste získali očekávané výsledky.</span><span class="sxs-lookup"><span data-stu-id="00480-404">Use it to review the order that you created for this scenario, to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="00480-405">Přejděte na **Řízení skladu \> Dodávky \> Všechny dodávky**.</span><span class="sxs-lookup"><span data-stu-id="00480-405">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="00480-406">Najděte a vyberte zásilku, která byla vytvořena pro náklad, který jste právě uvolnili.</span><span class="sxs-lookup"><span data-stu-id="00480-406">Find and select the shipment that was created for the load that you just released.</span></span>
1. <span data-ttu-id="00480-407">V podokně akcí na kartě **Doprava** vyberte **Zobrazit kontejnery**.</span><span class="sxs-lookup"><span data-stu-id="00480-407">On the Action Pane, on the **Transportation** tab, select **View containers**.</span></span>
1. <span data-ttu-id="00480-408">Potvrďte, že položky z prodejních objednávek byly kontejnerizovány do dvou různých kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="00480-408">Confirm that the items from the sales orders were containerized into two different containers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="00480-409">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="00480-409">Additional resources</span></span>

- [<span data-ttu-id="00480-410">Vytváření kontejnerů</span><span class="sxs-lookup"><span data-stu-id="00480-410">Containerization</span></span>](wave-containerization.md)
