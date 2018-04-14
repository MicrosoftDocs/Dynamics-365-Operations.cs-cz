--- 
title: "Vytvoření materiálového plánu pro vedlejší produkty"
description: "Plánovač výroby naplánuje materiálové požadavky na položky, které jsou vedlejšími produkty receptury."
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 77fa282401a7c2b0115235f1bd902998e9eed7c1
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="003b8-103">Vytvoření materiálového plánu pro vedlejší produkty</span><span class="sxs-lookup"><span data-stu-id="003b8-103">Create a material plan for co-products</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="003b8-104">Plánovač výroby naplánuje materiálové požadavky na položky, které jsou vedlejšími produkty receptury.</span><span class="sxs-lookup"><span data-stu-id="003b8-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="003b8-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USP2.</span><span class="sxs-lookup"><span data-stu-id="003b8-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="003b8-106">Vytvoření požadavku pro vedlejší produkt</span><span class="sxs-lookup"><span data-stu-id="003b8-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="003b8-107">Přejděte na výchozí řídicí panel.</span><span class="sxs-lookup"><span data-stu-id="003b8-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="003b8-108">Klikněte na Zpracování a dotaz na prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="003b8-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="003b8-109">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="003b8-109">Click New.</span></span>
4. <span data-ttu-id="003b8-110">Klikněte na Prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="003b8-110">Click Sales order.</span></span>
5. <span data-ttu-id="003b8-111">V poli Účet odběratele zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="003b8-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="003b8-112">Příklad: US-001</span><span class="sxs-lookup"><span data-stu-id="003b8-112">Example: US-001</span></span>  
6. <span data-ttu-id="003b8-113">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="003b8-113">Click OK.</span></span>
7. <span data-ttu-id="003b8-114">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="003b8-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="003b8-115">Příklad: P6003</span><span class="sxs-lookup"><span data-stu-id="003b8-115">Example: P6003</span></span>  
8. <span data-ttu-id="003b8-116">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="003b8-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="003b8-117">Příklad: 50000</span><span class="sxs-lookup"><span data-stu-id="003b8-117">Example: 50000</span></span>  
9. <span data-ttu-id="003b8-118">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="003b8-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="003b8-119">Vytvoření materiálového plánu pro vedlejší produkty</span><span class="sxs-lookup"><span data-stu-id="003b8-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="003b8-120">Klikněte na Hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="003b8-120">Click Master planning.</span></span>
2. <span data-ttu-id="003b8-121">V poli Plán kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="003b8-121">In the Plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="003b8-122">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="003b8-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="003b8-123">Příklad: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="003b8-123">Example: MasterPlan</span></span>  
4. <span data-ttu-id="003b8-124">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="003b8-124">Click Run.</span></span>
5. <span data-ttu-id="003b8-125">Rozbalte nebo sbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="003b8-125">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="003b8-126">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="003b8-126">Click Filter.</span></span>
7. <span data-ttu-id="003b8-127">V seznamu vyberte řádek pro pole = číslo položky.</span><span class="sxs-lookup"><span data-stu-id="003b8-127">In the list, select the row for Field = Item number.</span></span>
8. <span data-ttu-id="003b8-128">Zadejte hodnotu do pole Kritéria.</span><span class="sxs-lookup"><span data-stu-id="003b8-128">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="003b8-129">Příklad: P6003</span><span class="sxs-lookup"><span data-stu-id="003b8-129">Example: P6003</span></span>  
9. <span data-ttu-id="003b8-130">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="003b8-130">Click OK.</span></span>
10. <span data-ttu-id="003b8-131">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="003b8-131">Click OK.</span></span>
11. <span data-ttu-id="003b8-132">Klikněte na Plánované objednávky.</span><span class="sxs-lookup"><span data-stu-id="003b8-132">Click Planned orders.</span></span>
12. <span data-ttu-id="003b8-133">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="003b8-133">Use the Quick Filter to find records.</span></span> <span data-ttu-id="003b8-134">Můžete například filtrovat pole Číslo položky pomocí hodnoty „P6000“.</span><span class="sxs-lookup"><span data-stu-id="003b8-134">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="003b8-135">Filtrujte podle položky receptury, která má vedlejší produkt položky, pro kterou jste vytvořili prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="003b8-135">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
13. <span data-ttu-id="003b8-136">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="003b8-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="003b8-137">Vyberte libovolné řádky vrácené filtrem.</span><span class="sxs-lookup"><span data-stu-id="003b8-137">Select any of the rows returned by the filter.</span></span>  
14. <span data-ttu-id="003b8-138">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="003b8-138">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="003b8-139">Rozbalte nebo sbalte oddíl Doložení.</span><span class="sxs-lookup"><span data-stu-id="003b8-139">Expand or collapse the Pegging section.</span></span>
16. <span data-ttu-id="003b8-140">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="003b8-140">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="003b8-141">Plánovaná objednávka je doložena v prodejní objednávce pro vedlejší produkt.</span><span class="sxs-lookup"><span data-stu-id="003b8-141">The planned order is pegged to the sales order for the co-product.</span></span>  
17. <span data-ttu-id="003b8-142">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="003b8-142">Close the page.</span></span>


