---
title: Odstraňování problémů s hierarchiemi dávkových a sériových rezervací ve skladu
description: Toto téma popisuje, jak řešit běžné problémy, s nimiž se můžete setkat při práci s hierarchiemi rezervací, které používají dávkové nebo sériové dimenze.
author: perlynne
ms.date: 3/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 3/12/2021
ms.openlocfilehash: 1cd4883cdd95a97f821e0103da910e2c0346a08d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022539"
---
# <a name="troubleshoot-warehouse-batch-and-serial-reservation-hierarchies"></a><span data-ttu-id="a1b43-103">Odstraňování problémů s hierarchiemi dávkových a sériových rezervací ve skladu</span><span class="sxs-lookup"><span data-stu-id="a1b43-103">Troubleshoot warehouse batch and serial reservation hierarchies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1b43-104">Toto téma popisuje, jak řešit běžné problémy, s nimiž se můžete setkat při práci s hierarchiemi rezervací, které používají dávkové nebo sériové dimenze.</span><span class="sxs-lookup"><span data-stu-id="a1b43-104">This topic describes how to fix common issues that you might encounter while you work with reservation hierarchies that use batch or serial dimensions.</span></span>

<span data-ttu-id="a1b43-105">Další informace viz [Flexibilní zásada rezervace dimenze na úrovni skladu](flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="a1b43-105">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>

<span data-ttu-id="a1b43-106">Hierarchie rezervací položky určuje požadavek na dimenze úložiště, které musí být splněny, aby bylo možné přiřadit skladové místo objednávce poptávky.</span><span class="sxs-lookup"><span data-stu-id="a1b43-106">The reservation hierarchy of an item dictates the requirement of storage dimensions that must be fulfilled to assign a location to a demand order.</span></span> <span data-ttu-id="a1b43-107">Tyto dimenze lze popsat jako *dimenze nad skladovým místem* pro všechny dimenze, které musí být splněny před přiřazením skladového místa, a *dimenze pod skladovým umístěním* pro dimenze, které lze přidělit po přiřazení skladového místa objednávce poptávky.</span><span class="sxs-lookup"><span data-stu-id="a1b43-107">These dimensions can be described as *dimensions above location*, for all the dimensions that must be fulfilled before a location is assigned, and *dimensions below location*, for dimensions that can be allocated after a location has been assigned to the demand order.</span></span> <span data-ttu-id="a1b43-108">Tyto hierarchie rezervací jsou také známé jako hierarchie rezervací *batch-above* a *batch-below* nebo *serial-above* a *serial below*.</span><span class="sxs-lookup"><span data-stu-id="a1b43-108">These reservation hierarchies are also known as *batch-above* and *batch-below* reservation hierarchies, or *serial-above* and *serial-below* reservation hierarchies.</span></span>

<span data-ttu-id="a1b43-109">Zásoby lze úspěšně přidělit pouze v případě, že v dimenzích nad skladovým místem nejsou žádné mezery.</span><span class="sxs-lookup"><span data-stu-id="a1b43-109">Inventory can be successfully allocated only if there are no gaps in the dimensions above location.</span></span> <span data-ttu-id="a1b43-110">Například v hierarchii rezervací *batch-above* očekáváte, že na objednávce poptávky budou zadány dimenze **Lokalita**, **Sklad,** a **Číslo dávky**.</span><span class="sxs-lookup"><span data-stu-id="a1b43-110">For example, in a *batch-above* reservation hierarchy, you expect **Site,** **Warehouse,** and **Batch number** dimensions to be specified on the demand order.</span></span> <span data-ttu-id="a1b43-111">Pokud některá z těchto dimenzí chybí, proces přidělení selže.</span><span class="sxs-lookup"><span data-stu-id="a1b43-111">If any of these dimensions are missing, the allocation process will fail.</span></span> <span data-ttu-id="a1b43-112">Naproti tomu v hierarchii rezervací *batch-below* nebo *serial-below* může být na objednávce poptávky uvedeno číslo dávky nebo sériové číslo, ale proces přidělování to nevyžaduje.</span><span class="sxs-lookup"><span data-stu-id="a1b43-112">By contrast, in a *batch-below* or *serial-below* reservation hierarchy, a batch or serial number might be specified on the demand order, but the allocation process doesn't require it.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="a1b43-113">Zobrazuje se následující chybová zpráva: „Aby bylo možné přiřadit vlně, musí řádky nákladu určit rozměry nad umístěním.</span><span class="sxs-lookup"><span data-stu-id="a1b43-113">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="a1b43-114">Chcete-li přiřadit tyto rozměry, zarezervujte a znovu vytvořte řádek nákladu. “</span><span class="sxs-lookup"><span data-stu-id="a1b43-114">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="a1b43-115">Popis problému</span><span class="sxs-lookup"><span data-stu-id="a1b43-115">Issue description</span></span>

<span data-ttu-id="a1b43-116">Pokud používáte položku, která má hierarchii rezervací *batch-above*, příkaz **Uvolnit do skladu** na stránce **Pracovní plocha plánování nákladu** nefunguje, pokus se pokusíte uvolnit náklad pro částečné množství.</span><span class="sxs-lookup"><span data-stu-id="a1b43-116">When you use an item that has a *batch-above* reservation hierarchy, the **Release to warehouse** command on the **Load planning workbench** page doesn't work if you try to release a load for a partial quantity.</span></span> <span data-ttu-id="a1b43-117">Zobrazí se tato chybová zpráva a pro částečné množství se nevytvoří žádná práce.</span><span class="sxs-lookup"><span data-stu-id="a1b43-117">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="a1b43-118">Pokud však použijete položku, která má hierarchii rezervací *batch-below*, můžete uvolnit náklad pro částečné množství ze stránky **Pracovní plocha plánování nákladu**.</span><span class="sxs-lookup"><span data-stu-id="a1b43-118">However, when you use an item that has a *batch-below* reservation hierarchy, you can release a load for a partial quantity from the **Load planning workbench** page.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="a1b43-119">Příčina problému</span><span class="sxs-lookup"><span data-stu-id="a1b43-119">Issue cause</span></span>

<span data-ttu-id="a1b43-120">Když je některá dimenze nad dimenzí **Skladové místo** v hierarchii rezervací, musí být zadána před uvolněním do skladu.</span><span class="sxs-lookup"><span data-stu-id="a1b43-120">When a dimension is above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="a1b43-121">Částečná množství nelze uvolnit, pokud není zadána jedna či více dimenzí nad **skladovým místem**.</span><span class="sxs-lookup"><span data-stu-id="a1b43-121">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

## <a name="the-auto-reservation-prompt-for-a-batch-number-is-triggered-even-though-there-is-available-inventory"></a><span data-ttu-id="a1b43-122">Aktivuje se výzva k automatické rezervaci čísla dávky, i když jsou k dispozici zásoby.</span><span class="sxs-lookup"><span data-stu-id="a1b43-122">The auto-reservation prompt for a batch number is triggered even though there is available inventory.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a1b43-123">Popis problému</span><span class="sxs-lookup"><span data-stu-id="a1b43-123">Issue description</span></span>

<span data-ttu-id="a1b43-124">Když používáte položku, která má hierarchii rezervací *batch-above* ve skladu, který nemá povolené procesy skladu a je povolena automatická rezervace, zobrazí se výzva k automatické rezervaci čísla dávky, i když je pro vyzvednutí k dispozici pouze jedna dávka.</span><span class="sxs-lookup"><span data-stu-id="a1b43-124">When you use an item that has a *batch-above* reservation hierarchy in a warehouse that hasn't enabled warehouse processes, and automatic reservation is enabled, the auto-reservation prompt for a batch number is shown even if only one batch is available for picking.</span></span>

<span data-ttu-id="a1b43-125">Když však použijete stejnou položku ve skladu, kde jsou povoleny procesy skladu, výzva k automatické rezervaci se nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="a1b43-125">However, when you use the same item in a warehouse where warehouse processes are enabled, the auto-reservation prompt isn't shown.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="a1b43-126">Příčina problému</span><span class="sxs-lookup"><span data-stu-id="a1b43-126">Issue cause</span></span>

<span data-ttu-id="a1b43-127">Pokud je hierarchie rezervací definována jako *batch-above* nebo *serial-above*, odkazovaná dimenze (**Číslo dávky** nebo **Sériové číslo**) musí být vždy uvedeno na objednávkách poptávky.</span><span class="sxs-lookup"><span data-stu-id="a1b43-127">If a reservation hierarchy is defined as *batch-above* or *serial-above*, the referenced dimension (**Batch number** or **Serial number**) must always be specified on demand orders.</span></span> <span data-ttu-id="a1b43-128">Procesy skladu mohou být schopny doplnit informace, pokud je k dispozici jedna dávka nebo sériové číslo.</span><span class="sxs-lookup"><span data-stu-id="a1b43-128">Warehouse processes might be able to complete the information if a single batch or serial number is available.</span></span> <span data-ttu-id="a1b43-129">Protože však sklad nemá povoleny procesy skladu, musí uživatel vždy zadat všechny dimenze nad **skladovým místem**.</span><span class="sxs-lookup"><span data-stu-id="a1b43-129">However, because the warehouse isn't enabled for warehouse processes, the user must always specify all the dimensions above **Location**.</span></span>

## <a name="slotting-templates-that-have-the-consider-on-hand-slot-criterion-dont-consider-current-on-hand-inventory-for-batch-enabled-items"></a><span data-ttu-id="a1b43-130">Šablony slottingu, které mají kritérium slotu Zohlednění stavu na skladě, nezohledňují aktuální zásoby na skladě pro položky s povolenou dávkou.</span><span class="sxs-lookup"><span data-stu-id="a1b43-130">Slotting templates that have the Consider on-hand slot criterion don't consider current on-hand inventory for batch-enabled items.</span></span>

<span data-ttu-id="a1b43-131">Další informace viz [Skladový slotting](warehouse-slotting.md).</span><span class="sxs-lookup"><span data-stu-id="a1b43-131">For more information, see [Warehouse slotting](warehouse-slotting.md).</span></span>

### <a name="issue-description"></a><span data-ttu-id="a1b43-132">Popis problému</span><span class="sxs-lookup"><span data-stu-id="a1b43-132">Issue description</span></span>

<span data-ttu-id="a1b43-133">Šablony slottingu, které mají kritérium slotu *Zohlednění stavu na skladě*, nezohledňují aktuální zásoby na skladě pro položky *batch-above*.</span><span class="sxs-lookup"><span data-stu-id="a1b43-133">Slotting templates that have the *Consider on-hand* slot criterion don't consider current on-hand inventory for *batch-above* items.</span></span> <span data-ttu-id="a1b43-134">Zvažují to pouze v případě, že je na řádku prodejní objednávky uvedeno číslo dávky.</span><span class="sxs-lookup"><span data-stu-id="a1b43-134">They consider it only if the batch number is specified on the sales order line.</span></span>

<span data-ttu-id="a1b43-135">Když však použijete položky *batch-below*, aktuální zásoby na skladu jsou očekávány.</span><span class="sxs-lookup"><span data-stu-id="a1b43-135">However, when you use *batch-below* items, the current on-hand inventory is considered as expected.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="a1b43-136">Příčina problému</span><span class="sxs-lookup"><span data-stu-id="a1b43-136">Issue cause</span></span>

<span data-ttu-id="a1b43-137">Záhlaví šablony slottingu lze definovat pro strategii poptávky *Objednáno*, *Rezervováno* nebo *Uvolněno*.</span><span class="sxs-lookup"><span data-stu-id="a1b43-137">The slotting template header can be defined for the *Ordered,* *Reserved*, or *Released* demand strategy.</span></span> <span data-ttu-id="a1b43-138">Pro strategii poptávky *Objednáno* platí stejné požadavky na hierarchii rezervací, jaké platí pro rezervaci nebo uvolnění do procesů skladu.</span><span class="sxs-lookup"><span data-stu-id="a1b43-138">For the *Ordered* demand strategy, the same reservation hierarchy requirements apply that apply to reservation or release to warehouse processes.</span></span> <span data-ttu-id="a1b43-139">Proto pro položky, které mají hierarchii reservací *batch-above* a *serial-below*, musí být na objednávce poptávky (prodej nebo převod) zadáno číslo dávky nebo sériové číslo.</span><span class="sxs-lookup"><span data-stu-id="a1b43-139">Therefore, for items that have *batch-above* and *serial-below* reservation hierarchies, the batch or serial number must be specified on the demand order (sales or transfer).</span></span> <span data-ttu-id="a1b43-140">Případně strategie poptávky *Rezervováno* lze použít k výběru čísla dávky nebo sériového čísla před generováním poptávky skladového slottingu.</span><span class="sxs-lookup"><span data-stu-id="a1b43-140">Alternatively, the *Reserved* demand strategy can be used to select the batch or serial number before the warehouse slotting demand is generated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
