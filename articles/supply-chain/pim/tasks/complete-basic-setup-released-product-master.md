---
title: Základní nastavení uvolněného základního produktu
description: Toto téma popisuje, jak dokončit minimální požadované nastavení před použitím základního produktu ve verzích kusovníku.
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ac4ceeb3e21ab089eb16565bb6e38c7eb44be80
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986400"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="a3d95-103">Základní nastavení uvolněného základního produktu</span><span class="sxs-lookup"><span data-stu-id="a3d95-103">Complete basic setup of a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a3d95-104">Toto téma popisuje, jak dokončit minimální požadované nastavení před použitím základního produktu ve verzích kusovníku.</span><span class="sxs-lookup"><span data-stu-id="a3d95-104">This topic shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="a3d95-105">Jedná se o třetí postup z osmi, který vysvětluje vytvoření kombinací konfigurace založené na dimenzích.</span><span class="sxs-lookup"><span data-stu-id="a3d95-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="a3d95-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="a3d95-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="a3d95-107">Klikněte na **Navigační podokno > Moduly > Řízení informací o produktech > Produkty > Vydané produkty** .</span><span class="sxs-lookup"><span data-stu-id="a3d95-107">Go to **Navigation pane > Modules > Product information management > Products > Released products** .</span></span>
2. <span data-ttu-id="a3d95-108">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="a3d95-108">In the list, find and select the desired record.</span></span> <span data-ttu-id="a3d95-109">Vyberte základní produkt, který jste uvolnili v druhém postupu.</span><span class="sxs-lookup"><span data-stu-id="a3d95-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="a3d95-110">Tento základní produkt je vytvořen s technologií konfigurace založené na dimenzích.</span><span class="sxs-lookup"><span data-stu-id="a3d95-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="a3d95-111">V podokně akcí klikněte na možnost **Produkt** .</span><span class="sxs-lookup"><span data-stu-id="a3d95-111">On the Action Pane, select **Product** .</span></span>
4. <span data-ttu-id="a3d95-112">Kliknutím na možnost **Skupiny dimenzí** otevřete dialog Zanechat.</span><span class="sxs-lookup"><span data-stu-id="a3d95-112">Select **Dimension groups** to open the drop dialog.</span></span>
5. <span data-ttu-id="a3d95-113">V poli **Skupina dimenze úložiště** výběrem tlačítka rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="a3d95-113">In the **Storage dimension group** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="a3d95-114">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="a3d95-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="a3d95-115">Skupina dimenze úložiště určuje, které dimenze úložiště jsou použity pro transakci produktu.</span><span class="sxs-lookup"><span data-stu-id="a3d95-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="a3d95-116">Pro tento postup vyberte **Lokalita** .</span><span class="sxs-lookup"><span data-stu-id="a3d95-116">Select **Site** for this procedure.</span></span>  
7. <span data-ttu-id="a3d95-117">V poli **Skupina sledovací dimenze** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="a3d95-117">In the **Tracking dimension group** field, select the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="a3d95-118">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="a3d95-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="a3d95-119">Skupina sledovacích dimenzí určuje, které sledovací dimenze jsou použity pro transakci produktu.</span><span class="sxs-lookup"><span data-stu-id="a3d95-119">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="a3d95-120">Pro tento postup vyberte **Žádné** .</span><span class="sxs-lookup"><span data-stu-id="a3d95-120">Select **None** for this procedure.</span></span>  
9. <span data-ttu-id="a3d95-121">Klikněte na tlačítko **OK** .</span><span class="sxs-lookup"><span data-stu-id="a3d95-121">Click **OK** .</span></span>
10. <span data-ttu-id="a3d95-122">Klikněte na možnost **Upravit** .</span><span class="sxs-lookup"><span data-stu-id="a3d95-122">Click **Edit** .</span></span>
11. <span data-ttu-id="a3d95-123">V poli **Skupina modelů položek** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="a3d95-123">In the **Item model group** field, select the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="a3d95-124">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="a3d95-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="a3d95-125">Skupiny modelů položek obsahují nastavení určující, jak jsou položky kontrolovány a zpracovávány při příjmu a výdeji položek.</span><span class="sxs-lookup"><span data-stu-id="a3d95-125">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="a3d95-126">Také určují způsob výpočtu spotřeby položek.</span><span class="sxs-lookup"><span data-stu-id="a3d95-126">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="a3d95-127">Pro tento postup vyberte **FIFO** .</span><span class="sxs-lookup"><span data-stu-id="a3d95-127">Select **FIFO** for this procedure.</span></span>  
13. <span data-ttu-id="a3d95-128">Rozbalte oblast **Správa nákladů** .</span><span class="sxs-lookup"><span data-stu-id="a3d95-128">Expand the **Manage costs** section.</span></span>
14. <span data-ttu-id="a3d95-129">V poli **Skupina položek** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="a3d95-129">In the **Item group** field, select the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="a3d95-130">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="a3d95-130">In the list, find and select the desired record.</span></span> <span data-ttu-id="a3d95-131">Skupiny zboží se používají ke správě skladových zásob tak, že se skladové položky rozdělí na skupiny.</span><span class="sxs-lookup"><span data-stu-id="a3d95-131">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="a3d95-132">Pro tento postup vyberte **CarAudio** .</span><span class="sxs-lookup"><span data-stu-id="a3d95-132">Select **CarAudio** for this procedure.</span></span>  
16. <span data-ttu-id="a3d95-133">V podokně akcí zvolte **Plán** .</span><span class="sxs-lookup"><span data-stu-id="a3d95-133">On the Action Pane, select **Plan** .</span></span>
17. <span data-ttu-id="a3d95-134">Vyberte **Výchozí nastavení pořadí produktů** .</span><span class="sxs-lookup"><span data-stu-id="a3d95-134">Select **Default order settings** .</span></span>
18. <span data-ttu-id="a3d95-135">V poli **Výchozí typ objednávky** vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="a3d95-135">In the **Default order type field** , select an option.</span></span> <span data-ttu-id="a3d95-136">Zvolením možnosti **Výroba** zadejte, že výchozí možností zásob pro tento základní produkt je jeho výroba.</span><span class="sxs-lookup"><span data-stu-id="a3d95-136">Select **Production** to specify that the default supply option for this product master is to produce it.</span></span>  
19. <span data-ttu-id="a3d95-137">Zvolte **Uložit** .</span><span class="sxs-lookup"><span data-stu-id="a3d95-137">Select **Save** .</span></span>
20. <span data-ttu-id="a3d95-138">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a3d95-138">Close the page.</span></span>
21. <span data-ttu-id="a3d95-139">Zavřete formulář **Podrobnosti o uvolněném produktu** .</span><span class="sxs-lookup"><span data-stu-id="a3d95-139">Close the **Released product details** form.</span></span>

