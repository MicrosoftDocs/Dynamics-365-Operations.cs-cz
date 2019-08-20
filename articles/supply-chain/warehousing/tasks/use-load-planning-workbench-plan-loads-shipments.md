---
title: Plánování vytížení a dodávek s použitím pracovní plochy plánování vytížení
description: Toto téma popisuje použití pracovní plochy plánování vytížení k vytvoření vytížení pro prodejní objednávku.
author: ShylaThompson
manager: AnnBe
ms.date: 07/08/2019
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
ms.openlocfilehash: c5e20eef8aa748bb64c6c14dd7e1d92ccf6592e0
ms.sourcegitcommit: 81e6eaa2178fda7f7d086ad978f4c891bc4ec10a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/10/2019
ms.locfileid: "1739058"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="83c4c-103">Plánování vytížení a dodávek s použitím pracovní plochy plánování vytížení</span><span class="sxs-lookup"><span data-stu-id="83c4c-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="83c4c-104">Toto téma popisuje použití pracovní plochy plánování vytížení k vytvoření vytížení pro prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="83c4c-104">This topic shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="83c4c-105">Jako nutnou podmínku si nejprve vytvoříte prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="83c4c-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="83c4c-106">Tento postup je součástí každodenní práce koordinátora přepravy.</span><span class="sxs-lookup"><span data-stu-id="83c4c-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="83c4c-107">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="83c4c-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="83c4c-108">Vytvořit prodejní objednávku</span><span class="sxs-lookup"><span data-stu-id="83c4c-108">Create a sales order</span></span>
1. <span data-ttu-id="83c4c-109">Přejděte na **Navigační podokno > Moduly > Pohledávky > Objednávky > Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="83c4c-109">Go to the **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="83c4c-110">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="83c4c-110">Select **New**.</span></span>
3. <span data-ttu-id="83c4c-111">V poli **Účet odběratele** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="83c4c-111">In the **Customer account** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="83c4c-112">Vyberte účet **US-004**.</span><span class="sxs-lookup"><span data-stu-id="83c4c-112">Select account **US-004**.</span></span>
5. <span data-ttu-id="83c4c-113">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="83c4c-113">Select **OK**.</span></span>
6. <span data-ttu-id="83c4c-114">V poli **Číslo položky** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="83c4c-114">In the **Item number** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="83c4c-115">Vyberte položku **A0001**.</span><span class="sxs-lookup"><span data-stu-id="83c4c-115">Select item **A0001**.</span></span> <span data-ttu-id="83c4c-116">**A0001** je povoleno pro správu přepravy.</span><span class="sxs-lookup"><span data-stu-id="83c4c-116">**A0001** is enabled for transportation management.</span></span>  
8. <span data-ttu-id="83c4c-117">V poli **Pracoviště** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání a potom vyberte položku.</span><span class="sxs-lookup"><span data-stu-id="83c4c-117">In the **Site** field, select the drop-down button to open the lookup, then select an item.</span></span>
9. <span data-ttu-id="83c4c-118">Zadejte číslo do pole **Množství**.</span><span class="sxs-lookup"><span data-stu-id="83c4c-118">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="83c4c-119">Do pole **Sklad** zadejte v tomto příkladu '24'.</span><span class="sxs-lookup"><span data-stu-id="83c4c-119">In the **Warehouse** field, type '24' for this example.</span></span> <span data-ttu-id="83c4c-120">Tento sklad jej povolen pro správu přepravy a rozšířenou správu skladu.</span><span class="sxs-lookup"><span data-stu-id="83c4c-120">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="83c4c-121">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="83c4c-121">Select **Save**.</span></span>
12. <span data-ttu-id="83c4c-122">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="83c4c-122">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="83c4c-123">Vytvoření nového vytížení</span><span class="sxs-lookup"><span data-stu-id="83c4c-123">Create a new load</span></span>
1. <span data-ttu-id="83c4c-124">Přejděte na **Navigační podokno > Moduly > Správa přepravy > Plánování > Pracovní plocha plánování vytížení**.</span><span class="sxs-lookup"><span data-stu-id="83c4c-124">Go to the **Navigation pane > Modules > Transportation management > Planning > Load planning workbench**.</span></span>
2. <span data-ttu-id="83c4c-125">Vyberte kartu **Řádky prodeje**. Nyní budete vytvářet vytížení pro prodejní objednávku, kterou jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="83c4c-125">Select the **Sales lines** tab. Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="83c4c-126">Vytížení lze vytvořit podle nabídky a poptávky z nákupních objednávek, převodních příkazů a prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="83c4c-126">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="83c4c-127">V podokně akcí klikněte na možnost **Nabídka a poptávka**.</span><span class="sxs-lookup"><span data-stu-id="83c4c-127">On the Action Pane, select **Supply and demand**.</span></span>
4. <span data-ttu-id="83c4c-128">Vyberte **Do nového vytížení**.</span><span class="sxs-lookup"><span data-stu-id="83c4c-128">Select **To new load**.</span></span>
5. <span data-ttu-id="83c4c-129">V poli **ID šablony nákladu** vyberte tlačítko rozevíracího seznamu a otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="83c4c-129">In the **Load template ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="83c4c-130">Šablona vytížení definuje maximální měření pro hmotnost a objem celého vytížení.</span><span class="sxs-lookup"><span data-stu-id="83c4c-130">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="83c4c-131">Šablona vytížení může například představovat velikost kontejneru nebo nákladního automobilu.</span><span class="sxs-lookup"><span data-stu-id="83c4c-131">For example, the load template might represent the size of a container or truck.</span></span> <span data-ttu-id="83c4c-132">Vyberte položku.</span><span class="sxs-lookup"><span data-stu-id="83c4c-132">Select an item.</span></span>
6. <span data-ttu-id="83c4c-133">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="83c4c-133">Select **OK**.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="83c4c-134">Hodnocení a směrování vytížení</span><span class="sxs-lookup"><span data-stu-id="83c4c-134">Rate and route the load</span></span>
1. <span data-ttu-id="83c4c-135">Vyberte **Hodnocení a směrování**.</span><span class="sxs-lookup"><span data-stu-id="83c4c-135">Select **Rating and routing**.</span></span>
2. <span data-ttu-id="83c4c-136">Vyberte **Pracovní plocha sazeb trasy**.</span><span class="sxs-lookup"><span data-stu-id="83c4c-136">Select **Rate route workbench**.</span></span>
3. <span data-ttu-id="83c4c-137">Vyberte **Sazba – obchod**.</span><span class="sxs-lookup"><span data-stu-id="83c4c-137">Select **Rate shop**.</span></span>
4. <span data-ttu-id="83c4c-138">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="83c4c-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="83c4c-139">Vyberte **Přiřadit**.</span><span class="sxs-lookup"><span data-stu-id="83c4c-139">Select **Assign**.</span></span>
6. <span data-ttu-id="83c4c-140">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="83c4c-140">Close the page.</span></span>

