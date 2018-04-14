--- 
title: "Výpočet kusovníku pomocí jednoúrovňové struktury (jen ve verzi z února 2016)"
description: "Tento postup ukazuje, jak vypočítat náklady na dokončený výrobek s použitím jednoúrovňového rozpadu založeného na nákladovém formuláři."
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: dcc5008bb12d27bfd44e0b5af3b961abc8820c63
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016-only"></a><span data-ttu-id="f9d2f-103">Výpočet kusovníku pomocí jednoúrovňové struktury (jen ve verzi z února 2016)</span><span class="sxs-lookup"><span data-stu-id="f9d2f-103">Calculate a BOM by using a single level structure (February 2016 only)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f9d2f-104">Tento postup ukazuje, jak vypočítat náklady na dokončený výrobek s použitím jednoúrovňového rozpadu založeného na nákladovém formuláři.</span><span class="sxs-lookup"><span data-stu-id="f9d2f-104">This procedure shows how to calculate the cost of a finished product by using single level explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="f9d2f-105">Je to šestá úloha v řadě Kalkulace kusovníku.</span><span class="sxs-lookup"><span data-stu-id="f9d2f-105">This is the sixth task in the BOM calculation series.</span></span> <span data-ttu-id="f9d2f-106">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="f9d2f-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="f9d2f-107">Přejděte na Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="f9d2f-107">Go to Released products.</span></span>
2. <span data-ttu-id="f9d2f-108">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="f9d2f-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f9d2f-109">Vyberte produkt BOM_1.</span><span class="sxs-lookup"><span data-stu-id="f9d2f-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="f9d2f-110">V podokně akcí klikněte na možnost Spravovat náklady.</span><span class="sxs-lookup"><span data-stu-id="f9d2f-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="f9d2f-111">Klikněte na možnost Cena položky.</span><span class="sxs-lookup"><span data-stu-id="f9d2f-111">Click Item price.</span></span>
5. <span data-ttu-id="f9d2f-112">Klikněte na Vypočítat náklady na zboží.</span><span class="sxs-lookup"><span data-stu-id="f9d2f-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="f9d2f-113">Můžete kliknout na tlačítko se třemi tečkami (...) a v horní nabídce se zobrazí tato možnost.</span><span class="sxs-lookup"><span data-stu-id="f9d2f-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="f9d2f-114">V poli Nákladová verze klikněte na tlačítko rozevíracího seznamu a otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="f9d2f-114">In the Costing version field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f9d2f-115">V této ukázce vyberte 10.</span><span class="sxs-lookup"><span data-stu-id="f9d2f-115">For this demo, select 10.</span></span> <span data-ttu-id="f9d2f-116">Jedná se o stejnou nákladovou verzi sloužící k přidání nákladové ceny ke komponentám.</span><span class="sxs-lookup"><span data-stu-id="f9d2f-116">This is the same costing version used for adding the cost price to the components.</span></span>  
7. <span data-ttu-id="f9d2f-117">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="f9d2f-117">Click OK.</span></span>
8. <span data-ttu-id="f9d2f-118">Klepněte na Zobrazit podrobnosti výpočtu.</span><span class="sxs-lookup"><span data-stu-id="f9d2f-118">Click View calculation details.</span></span>
    * <span data-ttu-id="f9d2f-119">Můžete kliknout na tlačítko se třemi tečkami (...) a v horní nabídce se zobrazí tato možnost.</span><span class="sxs-lookup"><span data-stu-id="f9d2f-119">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>    <span data-ttu-id="f9d2f-120">Zde je složení nákladů::  •    10 je odvozeno z ITEM_A, 10 z ITEM_B, 10 z BOM_2.</span><span class="sxs-lookup"><span data-stu-id="f9d2f-120">Here's the composition of the cost:  •    10 is derived from ITEM_A, 10 from ITEM_B, 10 from BOM_2.</span></span> <span data-ttu-id="f9d2f-121">V tomto případě nejsou žádné podrobnosti pro BOM_2, protože tato položka byla zadána jako standardní náklady 10, ale nebyl proveden výpočet.</span><span class="sxs-lookup"><span data-stu-id="f9d2f-121">In this case there are no details for BOM_2 because it was entered as a standard cost of 10 but not done through calculation.</span></span>  <span data-ttu-id="f9d2f-122">•  7 je odvozeno z přípravného času, který je konstantním nákladem, a dalších 7 pochází z operace běhu (procesu).</span><span class="sxs-lookup"><span data-stu-id="f9d2f-122">•  7 is derived from the setup time, which is a constant cost, and additional 7 is derived from the run-time operation (Process).</span></span>  <span data-ttu-id="f9d2f-123">•   Existují i jiné částky, které odpovídají nepřímým nákladům.</span><span class="sxs-lookup"><span data-stu-id="f9d2f-123">•   There are also other amounts that correspond to indirect costs.</span></span>  
9. @SysTaskRecorder:_RequestClose


