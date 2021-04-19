---
title: Nákupní žádanky
description: Toto téma popisuje, jak jsou v optimalizaci plánování podporovány nákupní žádanky.
author: ChristianRytt
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 564f87fe78e79107feb103f953ed4769e4734aa1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808033"
---
# <a name="purchase-requisitions"></a><span data-ttu-id="8affe-103">Nákupní žádanky</span><span class="sxs-lookup"><span data-stu-id="8affe-103">Purchase requisitions</span></span>

<span data-ttu-id="8affe-104">Hlavní plánování může doplnit schválené nákupní žádanky.</span><span class="sxs-lookup"><span data-stu-id="8affe-104">Master planning can replenish approved purchase requisitions.</span></span> <span data-ttu-id="8affe-105">K pokrytí nákupních žádanek proto uživatelé nemusí k vytváření nákupních objednávek používat workflow.</span><span class="sxs-lookup"><span data-stu-id="8affe-105">Therefore, to cover purchase requisitions, users don't have to use a workflow to create purchase orders.</span></span> <span data-ttu-id="8affe-106">Místo toho lze nákupní žádanky pokrýt hlavním plánováním.</span><span class="sxs-lookup"><span data-stu-id="8affe-106">Instead, purchase requisitions can be covered by master planning.</span></span> <span data-ttu-id="8affe-107">Z důvodu této funkce může nákupní žádanka vyprodukovat nákupní objednávku, objednávku převodu nebo výrobní zakázku v závislosti na hodnotě **Plánovaný typ objednávky**, která je nastavena pro související produkt.</span><span class="sxs-lookup"><span data-stu-id="8affe-107">Because of this functionality, a purchase requisition can produce a purchase order, a transfer order, or a production order, depending on the **Planned order type** value that is set for the related product.</span></span>

## <a name="enable-master-plans-to-include-requisitions"></a><span data-ttu-id="8affe-108">Povolení hlavních plánů pro zahrnutí žádanek</span><span class="sxs-lookup"><span data-stu-id="8affe-108">Enable master plans to include requisitions</span></span>

<span data-ttu-id="8affe-109">Chcete-li během výpočtu pokrytí hlavního plánu zahrnout požadavky, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="8affe-109">To include requisitions during the coverage calculation for a master plan, follow these steps.</span></span>

1. <span data-ttu-id="8affe-110">Přejděte na **Hlavní plánování** \> **Nastavení** \> **Plány** \> **Hlavní plány**.</span><span class="sxs-lookup"><span data-stu-id="8affe-110">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="8affe-111">Vyberte nebo vytvořte hlavní plán.</span><span class="sxs-lookup"><span data-stu-id="8affe-111">Create or select a master plan.</span></span>
1. <span data-ttu-id="8affe-112">Na pevné záložce **Obecné** nastavte možnost **Zahrnout žádanky** na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="8affe-112">On the **General** FastTab, set the **Include requisitions** option to *Yes*.</span></span>
1. <span data-ttu-id="8affe-113">Opakujte kroky 2 a 3 pro každý další hlavní plán, do něhož chcete zahrnout žádosti.</span><span class="sxs-lookup"><span data-stu-id="8affe-113">Repeat steps 2 and 3 for each additional master plan where you want to include requisitions.</span></span>

## <a name="approved-requisitions-time-fence"></a><span data-ttu-id="8affe-114">Ochranná doba schválených žádanek</span><span class="sxs-lookup"><span data-stu-id="8affe-114">Approved requisitions time fence</span></span>

<span data-ttu-id="8affe-115">*Ochranná doba schválených žádanek* stanoví, jak daleko zpět (ve dnech) bude hlavní plán zahrnovat požadavek ze schválených požadavků na doplnění.</span><span class="sxs-lookup"><span data-stu-id="8affe-115">The *approved requisitions time fence* establishes how far back (in days) a master plan will include demand from approved replenishment requisitions.</span></span> <span data-ttu-id="8affe-116">Ochrannou lhůtu schváleného požadavku můžete nastavit jak na úrovni skupiny pokrytí, tak na úrovni hlavního plánu.</span><span class="sxs-lookup"><span data-stu-id="8affe-116">You can set an approved requisitions time fence at both the coverage group level and the master plan level.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a><span data-ttu-id="8affe-117">Nastavení ochranné lhůty schválené žádosti pro skupinu pokrytí</span><span class="sxs-lookup"><span data-stu-id="8affe-117">Set the approved requisitions time fence for a coverage group</span></span>

1. <span data-ttu-id="8affe-118">Přejděte na **Hlavní plánování** \> **Nastavení** \> **Disponibilita** \> **Skupiny disponibility**.</span><span class="sxs-lookup"><span data-stu-id="8affe-118">Go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**.</span></span>
1. <span data-ttu-id="8affe-119">Vytvořte nebo vyberte skupinu pokrytí.</span><span class="sxs-lookup"><span data-stu-id="8affe-119">Create or select a coverage group.</span></span>
1. <span data-ttu-id="8affe-120">Na kartě s náhledem **Ostatní** nastavte pole **Ochranná lhůta schválených žádanek (dny)** na počet dní pro zahrnutí ochranné lhůty.</span><span class="sxs-lookup"><span data-stu-id="8affe-120">On the **Other** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="8affe-121">Opakujte kroky 2 a 3 pro každou další skupinu pokrytí, kde chcete nastavit ochrannou lhůtu schválených žádostí.</span><span class="sxs-lookup"><span data-stu-id="8affe-121">Repeat steps 2 and 3 for each additional coverage group where you want to set an approved requisitions time fence.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a><span data-ttu-id="8affe-122">Nastavení ochranné lhůty schválené žádosti pro individuální hlavní plány</span><span class="sxs-lookup"><span data-stu-id="8affe-122">Set the approved requisitions time fence for individual master plans</span></span>

<span data-ttu-id="8affe-123">Když nastavíte časové ohraničení schváleného požadavku pro jednotlivý hlavní plán, nastavení přepíše nastavení časového ohraničení pro jakoukoli příslušnou skupinu pokrytí.</span><span class="sxs-lookup"><span data-stu-id="8affe-123">When you set an approved requisitions time fence for an individual master plan, the setting overrides the time fence setting for any applicable coverage group.</span></span>

1. <span data-ttu-id="8affe-124">Přejděte na **Hlavní plánování** \> **Nastavení** \> **Plány** \> **Hlavní plány**.</span><span class="sxs-lookup"><span data-stu-id="8affe-124">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="8affe-125">Vyberte nebo vytvořte hlavní plán.</span><span class="sxs-lookup"><span data-stu-id="8affe-125">Create or select a master plan.</span></span>
1. <span data-ttu-id="8affe-126">Na kartě s náhledem **Ochranná lhůta ve dnech** nastavte pole **Ochranná lhůta schválených žádanek (dny)** na počet dní pro zahrnutí ochranné lhůty.</span><span class="sxs-lookup"><span data-stu-id="8affe-126">On the **TIme fences in days** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="8affe-127">Opakujte kroky 2 a 3 pro každý další hlavní plán, kde chcete nastavit ochrannou lhůtu schválených žádostí.</span><span class="sxs-lookup"><span data-stu-id="8affe-127">Repeat steps 2 and 3 for each additional master plan where you want to set an approved requisitions time fence.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8affe-128">**Již brzy:** Schválené ochranné lhůty na žádosti nejsou dosud pro optimalizaci plánování podporovány.</span><span class="sxs-lookup"><span data-stu-id="8affe-128">**Coming soon:** Approved requisitions time fences aren't yet supported for Planning Optimization.</span></span> <span data-ttu-id="8affe-129">Dokud nebudou podporovány, všechny hodnoty, které zadáte do pole **Schválené ochranné lhůty žádanky (dny)**, bude pole ignorováno.</span><span class="sxs-lookup"><span data-stu-id="8affe-129">Until they are supported, all values that you enter in the **Approved requisitions time fence (days)** field will be ignored.</span></span>

## <a name="independent-supply-regardless-of-coverage-code"></a><span data-ttu-id="8affe-130">Nezávislá dodávka bez ohledu na kód pokrytí</span><span class="sxs-lookup"><span data-stu-id="8affe-130">Independent supply, regardless of coverage code</span></span>

<span data-ttu-id="8affe-131">Požadavky na nákup jsou vždy pokryty nezávislými plánovanými objednávkami, bez ohledu na kód pokrytí.</span><span class="sxs-lookup"><span data-stu-id="8affe-131">Purchase requisitions are always covered by independent planned orders, regardless of the coverage code.</span></span> <span data-ttu-id="8affe-132">Toto chování zajišťuje jasnou sledovatelnost a pracovní toky mezi požadavky na objednávku a objednávkami na doplnění.</span><span class="sxs-lookup"><span data-stu-id="8affe-132">This behavior ensures clear traceability and workflows between purchase requisitions and replenishment orders.</span></span>

### <a name="example-1"></a><span data-ttu-id="8affe-133">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="8affe-133">Example 1</span></span>

<span data-ttu-id="8affe-134">Produkt je nastaven tak, aby měl hodnotu **Kód pokrytí** *Min./max*. Má následující stavy zásob a požadavků:</span><span class="sxs-lookup"><span data-stu-id="8affe-134">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="8affe-135">Množství zásob na skladě = 10.</span><span class="sxs-lookup"><span data-stu-id="8affe-135">Inventory on-hand quantity = 10.</span></span>
- <span data-ttu-id="8affe-136">Minimální množství zásob = 15.</span><span class="sxs-lookup"><span data-stu-id="8affe-136">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="8affe-137">Maximální množství zásob = 20.</span><span class="sxs-lookup"><span data-stu-id="8affe-137">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="8affe-138">Existuje požadavek na nákup jednoho kusu.</span><span class="sxs-lookup"><span data-stu-id="8affe-138">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="8affe-139">Má požadované datum dnes.</span><span class="sxs-lookup"><span data-stu-id="8affe-139">It has a requested date of today.</span></span>

<span data-ttu-id="8affe-140">Při spuštění hlavního plánování se vytvoří dvě plánované objednávky: jedna na 10 kusů k doplnění zásob na maximální množství a jedna na jeden kus k doplnění požadavku na nákup.</span><span class="sxs-lookup"><span data-stu-id="8affe-140">When master planning runs, two planned orders are created: one for 10 pieces to replenish inventory to the maximum quantity, and one for one piece to replenish the purchase requisition.</span></span>

### <a name="example-2"></a><span data-ttu-id="8affe-141">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="8affe-141">Example 2</span></span>

<span data-ttu-id="8affe-142">Produkt je nastaven tak, aby měl hodnotu **Kód pokrytí** *Min./max*. Má následující stavy zásob a požadavků:</span><span class="sxs-lookup"><span data-stu-id="8affe-142">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="8affe-143">Množství zásob na skladě = 17.</span><span class="sxs-lookup"><span data-stu-id="8affe-143">Inventory on-hand quantity = 17.</span></span>
- <span data-ttu-id="8affe-144">Minimální množství zásob = 15.</span><span class="sxs-lookup"><span data-stu-id="8affe-144">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="8affe-145">Maximální množství zásob = 20.</span><span class="sxs-lookup"><span data-stu-id="8affe-145">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="8affe-146">Existuje požadavek na nákup jednoho kusu.</span><span class="sxs-lookup"><span data-stu-id="8affe-146">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="8affe-147">Má požadované datum dnes.</span><span class="sxs-lookup"><span data-stu-id="8affe-147">It has a requested date of today.</span></span>

<span data-ttu-id="8affe-148">Když běží hlavní plánování, vytvoří se jedna plánovaná objednávka pro jeden kus, aby se doplnila objednávka.</span><span class="sxs-lookup"><span data-stu-id="8affe-148">When master planning runs, one planned order for one piece is created to replenish the purchase requisition.</span></span>

### <a name="example-3"></a><span data-ttu-id="8affe-149">Příklad 3</span><span class="sxs-lookup"><span data-stu-id="8affe-149">Example 3</span></span>

<span data-ttu-id="8affe-150">Produkt je nastaven tak, aby měl hodnotu **Kód pokrytí** *Období* a období sedm dní.</span><span class="sxs-lookup"><span data-stu-id="8affe-150">A product is set up so that it has a **Coverage code** value of *Period* and a period length of seven days.</span></span> <span data-ttu-id="8affe-151">Má následující stavy zásob, prodejní objednávky a požadavku:</span><span class="sxs-lookup"><span data-stu-id="8affe-151">It has the following inventory, sales order, and requisition statuses:</span></span>

- <span data-ttu-id="8affe-152">Množství zásob na skladě = 0.</span><span class="sxs-lookup"><span data-stu-id="8affe-152">Inventory on-hand quantity = 0.</span></span>
- <span data-ttu-id="8affe-153">Existuje prodejní objednávka na pět kusů.</span><span class="sxs-lookup"><span data-stu-id="8affe-153">A sales order for five pieces exists.</span></span> <span data-ttu-id="8affe-154">Má očekávané datum expedice dnes plus jeden den.</span><span class="sxs-lookup"><span data-stu-id="8affe-154">It has an expected ship date of today plus one day.</span></span>
- <span data-ttu-id="8affe-155">Existuje požadavek na nákup tří kusů.</span><span class="sxs-lookup"><span data-stu-id="8affe-155">A purchase requisition for three pieces exists.</span></span> <span data-ttu-id="8affe-156">Má požadované datum dnes plus tři dny.</span><span class="sxs-lookup"><span data-stu-id="8affe-156">It has a requested date of today plus three days.</span></span>

<span data-ttu-id="8affe-157">Při spuštění hlavního plánování se vytvoří dvě plánované objednávky: jedna na tři kusy k doplnění zásob na maximální množství a jedna na pět kusů k doplnění požadavku na nákupní objednávku.</span><span class="sxs-lookup"><span data-stu-id="8affe-157">When master planning runs, two planned orders are created: one for three pieces to replenish the purchase requisition and one for five pieces to replenish sales order demand.</span></span>

> [!NOTE]
> <span data-ttu-id="8affe-158">Po spuštění plánované objednávky, která je vázána na nákupní objednávku, plánovací modul udržuje vázání na nákupní objednávku.</span><span class="sxs-lookup"><span data-stu-id="8affe-158">After a planned order that is pegged to a purchase requisition is firmed, the planning engine keeps the pegging to the purchase requisition.</span></span> <span data-ttu-id="8affe-159">Pokud později zjistíte, že ve schválené objednávce chybí určité množství, které je nutné ke splnění požadavku na nákup, systém vytvoří novou plánovanou objednávku rozdílu.</span><span class="sxs-lookup"><span data-stu-id="8affe-159">If the firmed order is later found to be missing some quantity that is required to fulfill the purchase requisition, the system will create a new planned order for the difference.</span></span>

<span data-ttu-id="8affe-160">Další obecné informace o nákupních žádankách naleznete v tématu [Přehled nákupní žádanky](../../procurement/purchase-requisitions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8affe-160">For more information about purchase requisitions, see [Purchase requisition overview](../../procurement/purchase-requisitions-overview.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]