--- 
title: "Vytvoření základního produktu"
description: "Vytvořte základní produkt pro předem definované varianty."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f944258e7efdd5c9eba7daf9a80c67058a6cc055
ms.openlocfilehash: 6e5cf92f7736523faf25ac97278a8a273e14ff88
ms.contentlocale: cs-cz
ms.lasthandoff: 10/25/2017

---
# <a name="create-a-product-master"></a><span data-ttu-id="164c3-103">Vytvoření základního produktu</span><span class="sxs-lookup"><span data-stu-id="164c3-103">Create a product master</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="164c3-104">Vytvořte základní produkt pro předem definované varianty.</span><span class="sxs-lookup"><span data-stu-id="164c3-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="164c3-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="164c3-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="164c3-106">Tento postup je určen pro návrháře produktu.</span><span class="sxs-lookup"><span data-stu-id="164c3-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="164c3-107">Vytvoření základního produktu</span><span class="sxs-lookup"><span data-stu-id="164c3-107">Create a new product master</span></span>
1. <span data-ttu-id="164c3-108">Přejděte do nabídky Řízení informací o produktech > Produkty > Základní produkty.</span><span class="sxs-lookup"><span data-stu-id="164c3-108">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="164c3-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="164c3-109">Click New.</span></span>
3. <span data-ttu-id="164c3-110">Zadejte hodnotu do pole Číslo produktu.</span><span class="sxs-lookup"><span data-stu-id="164c3-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="164c3-111">Číslo musí být jedinečné.</span><span class="sxs-lookup"><span data-stu-id="164c3-111">The number must be unique.</span></span> <span data-ttu-id="164c3-112">Číselnou řadu lze nastavit pro pole pro Číslo produktu.</span><span class="sxs-lookup"><span data-stu-id="164c3-112">A number sequence can be set for the Product number field.</span></span> <span data-ttu-id="164c3-113">V tomto případě uživatel nemusí zadat hodnotu.</span><span class="sxs-lookup"><span data-stu-id="164c3-113">In this case, the user doesn't have to enter a value.</span></span>  
4. <span data-ttu-id="164c3-114">Do pole Název produktu zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="164c3-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="164c3-115">Zadejte popisný název produktu.</span><span class="sxs-lookup"><span data-stu-id="164c3-115">Enter a descriptive product name.</span></span> <span data-ttu-id="164c3-116">Vyhledávací název je výchozí hodnota, ale lze ji uživatelem změnit.</span><span class="sxs-lookup"><span data-stu-id="164c3-116">The value defaults to the search name, but this can be changed by the user.</span></span>  
5. <span data-ttu-id="164c3-117">V poli Skupina dimenzí produktů kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="164c3-117">In the Product dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="164c3-118">Skupina dimenzí produktu určuje, které čtyři dimenze produktu lze použít k vytvoření variant produktu.</span><span class="sxs-lookup"><span data-stu-id="164c3-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="164c3-119">V tomto příkladu se používá skupina s barvou a velikostí.</span><span class="sxs-lookup"><span data-stu-id="164c3-119">This example uses a group with color and size.</span></span>  
6. <span data-ttu-id="164c3-120">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="164c3-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="164c3-121">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="164c3-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="164c3-122">Výchozí technologií konfigurace je předem definovaná varianta.</span><span class="sxs-lookup"><span data-stu-id="164c3-122">The default configuration technology is Predefined variant.</span></span> <span data-ttu-id="164c3-123">Bude použita v tomto příkladu.</span><span class="sxs-lookup"><span data-stu-id="164c3-123">This will be used for this example.</span></span>  
8. <span data-ttu-id="164c3-124">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="164c3-124">Click OK.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="164c3-125">Volba skupin dimenzí produktů</span><span class="sxs-lookup"><span data-stu-id="164c3-125">Select product dimension groups</span></span>
1. <span data-ttu-id="164c3-126">V poli Skupina barev kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="164c3-126">In the Color group field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="164c3-127">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="164c3-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="164c3-128">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="164c3-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="164c3-129">V poli Skupina velikostí kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="164c3-129">In the Size group field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="164c3-130">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="164c3-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="164c3-131">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="164c3-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="164c3-132">Přidání skupin dimenzí</span><span class="sxs-lookup"><span data-stu-id="164c3-132">Add dimension groups</span></span>
1. <span data-ttu-id="164c3-133">V podokně akcí klikněte na možnost Produkt.</span><span class="sxs-lookup"><span data-stu-id="164c3-133">On the Action Pane, click Product.</span></span>
2. <span data-ttu-id="164c3-134">Kliknutím na možnost Skupiny dimenzí otevřete dialog Zanechat.</span><span class="sxs-lookup"><span data-stu-id="164c3-134">Click Dimension groups to open the drop dialog.</span></span>
3. <span data-ttu-id="164c3-135">V poli Skupina dimenze úložiště kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="164c3-135">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="164c3-136">Dimenze uskladnění řídí způsob uložení položek ve skladu a jejich vydávání.</span><span class="sxs-lookup"><span data-stu-id="164c3-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="164c3-137">Dimenze uskladnění mohou například zahrnovat pracoviště a sklad.</span><span class="sxs-lookup"><span data-stu-id="164c3-137">For example, a storage dimension can include Site and Warehouse.</span></span>  
4. <span data-ttu-id="164c3-138">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="164c3-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="164c3-139">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="164c3-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="164c3-140">V poli Skupina sledovací dimenze kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="164c3-140">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="164c3-141">Skupina sledovacích dimenzí určuje sledovací dimenze, které je možné přidat k produktu.</span><span class="sxs-lookup"><span data-stu-id="164c3-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="164c3-142">Například číslo dávky a sériové číslo slouží ke sledování skladových položek.</span><span class="sxs-lookup"><span data-stu-id="164c3-142">For example, the batch number and serial number are used to track inventory items.</span></span>  
7. <span data-ttu-id="164c3-143">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="164c3-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="164c3-144">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="164c3-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="164c3-145">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="164c3-145">Click OK.</span></span>
10. <span data-ttu-id="164c3-146">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="164c3-146">Click Save.</span></span>
11. <span data-ttu-id="164c3-147">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="164c3-147">Close the page.</span></span>


