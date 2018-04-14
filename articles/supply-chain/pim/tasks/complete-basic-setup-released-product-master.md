--- 
title: "Základní nastavení uvolněného základního produktu"
description: "Tento postup popisuje, jak dokončit minimální požadované nastavení před použitím základního produktu ve verzích kusovníku."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
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
ms.openlocfilehash: d52b337d9062fa8051e02144df5d064e54a6784d
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="5f6cf-103">Základní nastavení uvolněného základního produktu</span><span class="sxs-lookup"><span data-stu-id="5f6cf-103">Complete basic setup of a released product master</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5f6cf-104">Tento postup popisuje, jak dokončit minimální požadované nastavení před použitím základního produktu ve verzích kusovníku.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-104">This procedure shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="5f6cf-105">Jedná se o třetí postup z osmi, který vysvětluje vytvoření kombinací konfigurace založené na dimenzích.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="5f6cf-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="5f6cf-107">Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="5f6cf-108">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5f6cf-109">Vyberte základní produkt, který jste uvolnili v druhém postupu.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="5f6cf-110">Tento základní produkt je vytvořen s technologií konfigurace založené na dimenzích.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="5f6cf-111">V podokně akcí klikněte na možnost Produkt.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-111">On the Action Pane, click Product.</span></span>
4. <span data-ttu-id="5f6cf-112">Kliknutím na možnost Skupiny dimenzí otevřete dialog Zanechat.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-112">Click Dimension groups to open the drop dialog.</span></span>
5. <span data-ttu-id="5f6cf-113">V poli Skupina dimenze úložiště kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-113">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="5f6cf-114">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5f6cf-115">Skupina dimenze úložiště určuje, které dimenze úložiště jsou použity pro transakci produktu.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="5f6cf-116">Pro tento postup vyberte Lokalita.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-116">Select Site for this procedure.</span></span>  
7. <span data-ttu-id="5f6cf-117">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-117">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="5f6cf-118">V poli Skupina sledovací dimenze kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-118">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="5f6cf-119">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5f6cf-120">Skupina sledovacích dimenzí určuje, které sledovací dimenze jsou použity pro transakci produktu.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-120">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="5f6cf-121">Pro tento postup vyberte Žádné.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-121">Select None for this procedure.</span></span>  
10. <span data-ttu-id="5f6cf-122">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-122">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="5f6cf-123">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-123">Click OK.</span></span>
12. <span data-ttu-id="5f6cf-124">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="5f6cf-125">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-125">Click Edit.</span></span>
    * <span data-ttu-id="5f6cf-126">Otevřete formulář Podrobnosti o uvolněném produktu a pokračujte v nastavování.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-126">Open the Released product details form to continue the setup task.</span></span>  
14. <span data-ttu-id="5f6cf-127">V poli Skupina modelů položek kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-127">In the Item model group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="5f6cf-128">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5f6cf-129">Skupiny modelů položek obsahují nastavení určující, jak jsou položky kontrolovány a zpracovávány při příjmu a výdeji položek.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-129">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="5f6cf-130">Také určují způsob výpočtu spotřeby položek.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-130">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="5f6cf-131">Pro tento postup vyberte FIFO.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-131">Select   FIFO for this procedure.</span></span>  
16. <span data-ttu-id="5f6cf-132">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-132">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="5f6cf-133">Rozbalte nebo sbalte oddíl Správa nákladů.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-133">Expand or collapse the Manage costs section.</span></span>
18. <span data-ttu-id="5f6cf-134">V poli Skupina položek kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-134">In the Item group field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="5f6cf-135">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-135">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5f6cf-136">Skupiny zboží se používají ke správě skladových zásob tak, že se skladové položky rozdělí na skupiny.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-136">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="5f6cf-137">Pro tento postup vyberte CarAudio.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-137">Select   CarAudio for this procedure.</span></span>  
20. <span data-ttu-id="5f6cf-138">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-138">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="5f6cf-139">V podokně akcí klikněte na položku Plán.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-139">On the Action Pane, click Plan.</span></span>
22. <span data-ttu-id="5f6cf-140">Klikněte na Výchozí nastavení objednávky.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-140">Click Default order settings.</span></span>
23. <span data-ttu-id="5f6cf-141">V poli Výchozí typ objednávky vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-141">In the Default order type field, select an option.</span></span>
    * <span data-ttu-id="5f6cf-142">Zvolením možnosti Výroba zadejte, že výchozí možností zásob pro tento základní produkt je jeho výroba.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-142">Select Production to specify that the default supply option for this product master is to produce it.</span></span>  
24. <span data-ttu-id="5f6cf-143">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-143">Close the page.</span></span>
25. <span data-ttu-id="5f6cf-144">Zavřete formulář Podrobnosti o uvolněném produktu.</span><span class="sxs-lookup"><span data-stu-id="5f6cf-144">Close the Released product details form.</span></span>


