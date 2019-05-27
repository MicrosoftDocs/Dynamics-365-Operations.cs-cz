---
title: Plánování vytížení a dodávek s použitím pracovní plochy plánování vytížení
description: Tento postup popisuje použití pracovní plochy plánování vytížení k vytvoření vytížení pro prodejní objednávku.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1927cff48beb30f934bd066c32ab48dfb9d06f74
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564782"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="00a62-103">Plánování vytížení a dodávek s použitím pracovní plochy plánování vytížení</span><span class="sxs-lookup"><span data-stu-id="00a62-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="00a62-104">Tento postup popisuje použití pracovní plochy plánování vytížení k vytvoření vytížení pro prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="00a62-104">This procedure shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="00a62-105">Jako nutnou podmínku si nejprve vytvoříte prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="00a62-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="00a62-106">Tento postup je součástí každodenní práce koordinátora přepravy.</span><span class="sxs-lookup"><span data-stu-id="00a62-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="00a62-107">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="00a62-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="00a62-108">Vytvořit prodejní objednávku</span><span class="sxs-lookup"><span data-stu-id="00a62-108">Create a sales order</span></span>
1. <span data-ttu-id="00a62-109">Přejděte na Pohledávky > Objednávky > Všechny prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="00a62-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="00a62-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="00a62-110">Click New.</span></span>
3. <span data-ttu-id="00a62-111">V poli Účet odběratele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="00a62-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="00a62-112">Vyberte účet US-004.</span><span class="sxs-lookup"><span data-stu-id="00a62-112">Select account US-004.</span></span>
5. <span data-ttu-id="00a62-113">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="00a62-113">Click OK.</span></span>
6. <span data-ttu-id="00a62-114">V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="00a62-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="00a62-115">Vyberte položku A0001.</span><span class="sxs-lookup"><span data-stu-id="00a62-115">Select item A0001.</span></span>
    * <span data-ttu-id="00a62-116">A0001 je povoleno pro správu přepravy.</span><span class="sxs-lookup"><span data-stu-id="00a62-116">A0001 is enabled for transportation management.</span></span>  
8. <span data-ttu-id="00a62-117">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="00a62-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="00a62-118">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="00a62-118">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="00a62-119">Zadejte hodnotu 24 do pole Sklad.</span><span class="sxs-lookup"><span data-stu-id="00a62-119">In the Warehouse field, type '24'.</span></span>
    * <span data-ttu-id="00a62-120">V tomto příkladu vyberte sklad 24.</span><span class="sxs-lookup"><span data-stu-id="00a62-120">In this example select warehouse 24.</span></span> <span data-ttu-id="00a62-121">Tento sklad jej povolen pro správu přepravy a rozšířenou správu skladu.</span><span class="sxs-lookup"><span data-stu-id="00a62-121">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="00a62-122">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="00a62-122">Click Save.</span></span>
12. <span data-ttu-id="00a62-123">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="00a62-123">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="00a62-124">Vytvoření nového vytížení</span><span class="sxs-lookup"><span data-stu-id="00a62-124">Create a new load</span></span>
1. <span data-ttu-id="00a62-125">Přejděte do nabídky Správa přepravy > Plánování > Pracovní plocha plánování vytížení.</span><span class="sxs-lookup"><span data-stu-id="00a62-125">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="00a62-126">Klikněte na kartu Řádky prodeje.</span><span class="sxs-lookup"><span data-stu-id="00a62-126">Click the Sales lines tab.</span></span>
    * <span data-ttu-id="00a62-127">Nyní budete vytvářet vytížení pro prodejní objednávku, kterou jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="00a62-127">Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="00a62-128">Vytížení lze vytvořit podle nabídky a poptávky z nákupních objednávek, převodních příkazů a prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="00a62-128">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="00a62-129">V podokně akcí klikněte na možnost Nabídka a poptávka.</span><span class="sxs-lookup"><span data-stu-id="00a62-129">On the Action Pane, click Supply and demand.</span></span>
4. <span data-ttu-id="00a62-130">Klikněte na možnost Do nového vytížení.</span><span class="sxs-lookup"><span data-stu-id="00a62-130">Click To new load.</span></span>
5. <span data-ttu-id="00a62-131">V poli ID šablony nákladu kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="00a62-131">In the Load template ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="00a62-132">Šablona vytížení definuje maximální měření pro hmotnost a objem celého vytížení.</span><span class="sxs-lookup"><span data-stu-id="00a62-132">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="00a62-133">Šablona vytížení může například představovat velikost kontejneru nebo nákladního automobilu.</span><span class="sxs-lookup"><span data-stu-id="00a62-133">For example, the load template might represent the size of a container or truck.</span></span>  
6. <span data-ttu-id="00a62-134">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="00a62-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="00a62-135">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="00a62-135">Click OK.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="00a62-136">Hodnocení a směrování vytížení</span><span class="sxs-lookup"><span data-stu-id="00a62-136">Rate and route the load</span></span>
1. <span data-ttu-id="00a62-137">Klikněte na možnost Hodnocení a směrování.</span><span class="sxs-lookup"><span data-stu-id="00a62-137">Click Rating and routing.</span></span>
2. <span data-ttu-id="00a62-138">Klikněte na možnost Pracovní plocha sazeb trasy.</span><span class="sxs-lookup"><span data-stu-id="00a62-138">Click Rate route workbench.</span></span>
3. <span data-ttu-id="00a62-139">Klikněte na možnost Sazba – obchod.</span><span class="sxs-lookup"><span data-stu-id="00a62-139">Click Rate shop.</span></span>
4. <span data-ttu-id="00a62-140">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="00a62-140">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="00a62-141">Klikněte na možnost Přiřadit.</span><span class="sxs-lookup"><span data-stu-id="00a62-141">Click Assign.</span></span>
6. <span data-ttu-id="00a62-142">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="00a62-142">Close the page.</span></span>
7. <span data-ttu-id="00a62-143">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="00a62-143">Close the page.</span></span>

