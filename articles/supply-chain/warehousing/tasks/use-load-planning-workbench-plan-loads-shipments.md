---
title: Plánování vytížení a dodávek s použitím pracovní plochy plánování vytížení
description: Toto téma popisuje použití pracovní plochy plánování vytížení k vytvoření vytížení pro prodejní objednávku.
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f4fdff8bdc383a85d604fa6e545c625d5782241f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976806"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="9bf9e-103">Plánování vytížení a dodávek s použitím pracovní plochy plánování vytížení</span><span class="sxs-lookup"><span data-stu-id="9bf9e-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9bf9e-104">Toto téma popisuje použití pracovní plochy plánování vytížení k vytvoření vytížení pro prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-104">This topic shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="9bf9e-105">Jako nutnou podmínku si nejprve vytvoříte prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="9bf9e-106">Tento postup je součástí každodenní práce koordinátora přepravy.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="9bf9e-107">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="9bf9e-108">Vytvořit prodejní objednávku</span><span class="sxs-lookup"><span data-stu-id="9bf9e-108">Create a sales order</span></span>
1. <span data-ttu-id="9bf9e-109">Přejděte na **Navigační podokno > Moduly > Pohledávky > Objednávky > Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-109">Go to the **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="9bf9e-110">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-110">Select **New**.</span></span>
3. <span data-ttu-id="9bf9e-111">V poli **Účet odběratele** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-111">In the **Customer account** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="9bf9e-112">Vyberte účet **US-004**.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-112">Select account **US-004**.</span></span>
5. <span data-ttu-id="9bf9e-113">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-113">Select **OK**.</span></span>
6. <span data-ttu-id="9bf9e-114">V poli **Číslo položky** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-114">In the **Item number** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="9bf9e-115">Vyberte položku **A0001**.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-115">Select item **A0001**.</span></span> <span data-ttu-id="9bf9e-116">**A0001** je povoleno pro správu přepravy.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-116">**A0001** is enabled for transportation management.</span></span>  
8. <span data-ttu-id="9bf9e-117">V poli **Pracoviště** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání a potom vyberte položku.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-117">In the **Site** field, select the drop-down button to open the lookup, then select an item.</span></span>
9. <span data-ttu-id="9bf9e-118">Zadejte číslo do pole **Množství**.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-118">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="9bf9e-119">Do pole **Sklad** zadejte v tomto příkladu '24'.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-119">In the **Warehouse** field, type '24' for this example.</span></span> <span data-ttu-id="9bf9e-120">Tento sklad jej povolen pro správu přepravy a rozšířenou správu skladu.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-120">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="9bf9e-121">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-121">Select **Save**.</span></span>
12. <span data-ttu-id="9bf9e-122">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-122">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="9bf9e-123">Vytvoření nového vytížení</span><span class="sxs-lookup"><span data-stu-id="9bf9e-123">Create a new load</span></span>
1. <span data-ttu-id="9bf9e-124">Přejděte na **Navigační podokno > Moduly > Správa přepravy > Plánování > Pracovní plocha plánování vytížení**.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-124">Go to the **Navigation pane > Modules > Transportation management > Planning > Load planning workbench**.</span></span>
2. <span data-ttu-id="9bf9e-125">Vyberte kartu **Řádky prodeje**. Nyní budete vytvářet vytížení pro prodejní objednávku, kterou jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-125">Select the **Sales lines** tab. Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="9bf9e-126">Vytížení lze vytvořit podle nabídky a poptávky z nákupních objednávek, převodních příkazů a prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-126">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="9bf9e-127">V podokně akcí klikněte na možnost **Nabídka a poptávka**.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-127">On the Action Pane, select **Supply and demand**.</span></span>
4. <span data-ttu-id="9bf9e-128">Vyberte **Do nového vytížení**.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-128">Select **To new load**.</span></span>
5. <span data-ttu-id="9bf9e-129">V poli **ID šablony nákladu** vyberte tlačítko rozevíracího seznamu a otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-129">In the **Load template ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="9bf9e-130">Šablona vytížení definuje maximální měření pro hmotnost a objem celého vytížení.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-130">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="9bf9e-131">Šablona vytížení může například představovat velikost kontejneru nebo nákladního automobilu.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-131">For example, the load template might represent the size of a container or truck.</span></span> <span data-ttu-id="9bf9e-132">Vyberte položku.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-132">Select an item.</span></span>
6. <span data-ttu-id="9bf9e-133">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-133">Select **OK**.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="9bf9e-134">Hodnocení a směrování vytížení</span><span class="sxs-lookup"><span data-stu-id="9bf9e-134">Rate and route the load</span></span>
1. <span data-ttu-id="9bf9e-135">Vyberte **Hodnocení a směrování**.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-135">Select **Rating and routing**.</span></span>
2. <span data-ttu-id="9bf9e-136">Vyberte **Pracovní plocha sazeb trasy**.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-136">Select **Rate route workbench**.</span></span>
3. <span data-ttu-id="9bf9e-137">Vyberte **Sazba – obchod**.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-137">Select **Rate shop**.</span></span>
4. <span data-ttu-id="9bf9e-138">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="9bf9e-139">Vyberte **Přiřadit**.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-139">Select **Assign**.</span></span>
6. <span data-ttu-id="9bf9e-140">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="9bf9e-140">Close the page.</span></span>

