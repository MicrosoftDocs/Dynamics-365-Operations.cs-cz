--- 
title: "Výpočet kusovníku pomocí víceúrovňové struktury (jen ve verzi z února 2016)"
description: "Tento postup ukazuje, jak vypočítat náklady na dokončený výrobek s použitím víceúrovňového rozpadu založeného na nákladovém formuláři."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 514cefdb78000eafc0dee7c91fc2d8181e9285e4
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016-only"></a><span data-ttu-id="1caab-103">Výpočet kusovníku pomocí víceúrovňové struktury (jen ve verzi z února 2016)</span><span class="sxs-lookup"><span data-stu-id="1caab-103">Calculate a BOM by using a multilevel structure (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1caab-104">Tento postup ukazuje, jak vypočítat náklady na dokončený výrobek s použitím víceúrovňového rozpadu založeného na nákladovém formuláři.</span><span class="sxs-lookup"><span data-stu-id="1caab-104">This procedure shows how to calculate the cost of a finished product by using multilevel explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="1caab-105">Je to sedmá úloha v řadě Kalkulace kusovníku.</span><span class="sxs-lookup"><span data-stu-id="1caab-105">It is the seventh task in the BOM calculation series.</span></span> <span data-ttu-id="1caab-106">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="1caab-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="1caab-107">Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="1caab-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="1caab-108">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="1caab-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1caab-109">Vyberte produkt BOM_1.</span><span class="sxs-lookup"><span data-stu-id="1caab-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="1caab-110">V podokně akcí klikněte na možnost Spravovat náklady.</span><span class="sxs-lookup"><span data-stu-id="1caab-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="1caab-111">Klikněte na možnost Cena položky.</span><span class="sxs-lookup"><span data-stu-id="1caab-111">Click Item price.</span></span>
5. <span data-ttu-id="1caab-112">Klikněte na Vypočítat náklady na zboží.</span><span class="sxs-lookup"><span data-stu-id="1caab-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="1caab-113">Můžete kliknout na tlačítko se třemi tečkami (...) a v horní nabídce se zobrazí tato možnost.</span><span class="sxs-lookup"><span data-stu-id="1caab-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="1caab-114">V poli Nákladová verze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1caab-114">In the Costing version field, enter or select a value.</span></span>
    * <span data-ttu-id="1caab-115">Zvolte položku Nákladová verze 20, protože se jedná o typ Plánované náklady a Režim rozpadu je Víceúrovňový.</span><span class="sxs-lookup"><span data-stu-id="1caab-115">Select Costing version 20, because it's Planned cost type and Explosion mode is Multilevel.</span></span>   <span data-ttu-id="1caab-116">Režim rozpadu na více úrovních je pro plánované náklady a simulace.</span><span class="sxs-lookup"><span data-stu-id="1caab-116">The Multilevel explosion mode is for planned costs and simulations.</span></span> <span data-ttu-id="1caab-117">Nepoužívá se pro standardní náklady.</span><span class="sxs-lookup"><span data-stu-id="1caab-117">It is not used for standard cost.</span></span>  
7. <span data-ttu-id="1caab-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="1caab-118">Click OK.</span></span>
8. <span data-ttu-id="1caab-119">Klepněte na Zobrazit podrobnosti výpočtu.</span><span class="sxs-lookup"><span data-stu-id="1caab-119">Click View calculation details.</span></span>
    * <span data-ttu-id="1caab-120">Můžete kliknout na tlačítko se třemi tečkami (...) a v horní nabídce se zobrazí tato možnost.</span><span class="sxs-lookup"><span data-stu-id="1caab-120">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  <span data-ttu-id="1caab-121">V takovém případě si všimněte, jak byl BOM_2 vypočítán s ohledem na suroviny, proces a režii s celkovým nákladem 29,40 namísto standardního nákladu 10, který byl aktivován v počátečním průvodci záznamem úloh v této řadě.</span><span class="sxs-lookup"><span data-stu-id="1caab-121">In this case, notice how BOM_2 has been calculated taking into account the raw material, process, and overhead with a total of 29,40 instead of the standard cost of 10 that was activated in the initial task guide in this series.</span></span>  
9. <span data-ttu-id="1caab-122">Klikněte na kartu Nákladový formulář.</span><span class="sxs-lookup"><span data-stu-id="1caab-122">Click the Costing sheet tab.</span></span>
    * <span data-ttu-id="1caab-123">Když se přesuneme na kartu Nákladový formulář, součty podle nákladových skupin se liší ve srovnání s výpočtem provedeným v předchozím průvodci záznamem úloh.</span><span class="sxs-lookup"><span data-stu-id="1caab-123">Moving to the Costing sheet tab, the totals per cost group are different compared to the calculation done in previous task guide.</span></span>  
10. <span data-ttu-id="1caab-124">V poli Úroveň vyberte 'Vícenásobná'.</span><span class="sxs-lookup"><span data-stu-id="1caab-124">In the Level field, select 'Multi'.</span></span>
    * <span data-ttu-id="1caab-125">Pokud vyberete Vícenásobné, jsou náklady klasifikovány podle složení BOM_2, kde 10 je odvozeno od M1 nákladové skupiny (ITEM_C) a 15,60 je odvozeno od jeho výroby, kde nákladová skupina je L2.</span><span class="sxs-lookup"><span data-stu-id="1caab-125">When selecting Multi, the costs are classified according to the composition of BOM_2, where 10 is derived from the M1 cost group (ITEM_C), and 15,60 is derived from its manufacturing where the cost group is L2.</span></span> <span data-ttu-id="1caab-126">Nepřímé náklady se též liší.</span><span class="sxs-lookup"><span data-stu-id="1caab-126">Indirect costs also vary.</span></span>  
11. <span data-ttu-id="1caab-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1caab-127">Close the page.</span></span>
12. <span data-ttu-id="1caab-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1caab-128">Close the page.</span></span>


