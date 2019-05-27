---
title: Vytvoření dokončeného produktu (jen ve verzi z února 2016)
description: Tato úloha je zaměřena na vytvoření dokončeného produktu.
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44f9693e04160ffe9307de5e454d8269ca883679
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570850"
---
# <a name="create-a-finished-product-february-2016-only"></a><span data-ttu-id="e5a83-103">Vytvoření dokončeného produktu (jen ve verzi z února 2016)</span><span class="sxs-lookup"><span data-stu-id="e5a83-103">Create a finished product (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e5a83-104">Tato úloha je zaměřena na vytvoření dokončeného produktu.</span><span class="sxs-lookup"><span data-stu-id="e5a83-104">This task focuses on creating a finished product.</span></span> <span data-ttu-id="e5a83-105">Je to první úloha v řadě Kalkulace kusovníku.</span><span class="sxs-lookup"><span data-stu-id="e5a83-105">It is the first task in the BOM calculation series.</span></span> <span data-ttu-id="e5a83-106">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="e5a83-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="e5a83-107">Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="e5a83-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="e5a83-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e5a83-108">Click New.</span></span>
3. <span data-ttu-id="e5a83-109">Zadejte hodnotu do pole Číslo produktu.</span><span class="sxs-lookup"><span data-stu-id="e5a83-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="e5a83-110">Pro ukázku zadejte BOM_1.</span><span class="sxs-lookup"><span data-stu-id="e5a83-110">For the demonstration, type BOM_1.</span></span>  
4. <span data-ttu-id="e5a83-111">V poli Skupina modelů zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e5a83-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="e5a83-112">Vyberte volbu „STD“.</span><span class="sxs-lookup"><span data-stu-id="e5a83-112">Select STD.</span></span> <span data-ttu-id="e5a83-113">STD zastupuje standardní náklady a je to nejčastěji používaný model při práci s výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="e5a83-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="e5a83-114">V poli Skupina zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e5a83-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="e5a83-115">Vyberte například Audio.</span><span class="sxs-lookup"><span data-stu-id="e5a83-115">For example, select Audio.</span></span> <span data-ttu-id="e5a83-116">To nemá žádný vliv na výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="e5a83-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="e5a83-117">V poli Skupina dimenze úložiště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e5a83-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="e5a83-118">Vyberte SiteWH.</span><span class="sxs-lookup"><span data-stu-id="e5a83-118">Select SiteWH.</span></span> <span data-ttu-id="e5a83-119">Pro ukázku se použije pouze Pracoviště a Sklad.</span><span class="sxs-lookup"><span data-stu-id="e5a83-119">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="e5a83-120">V poli Skupina sledovací dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e5a83-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="e5a83-121">Sledovací dimenze v tomto příkladu nebudou použity, vyberte Žádné.</span><span class="sxs-lookup"><span data-stu-id="e5a83-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="e5a83-122">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="e5a83-122">Click OK.</span></span>
9. <span data-ttu-id="e5a83-123">V podokně akcí klikněte na možnost Spravovat sklad.</span><span class="sxs-lookup"><span data-stu-id="e5a83-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="e5a83-124">Klikněte na Výchozí nastavení objednávky.</span><span class="sxs-lookup"><span data-stu-id="e5a83-124">Click Default order settings.</span></span>
11. <span data-ttu-id="e5a83-125">V poli Výchozí typ objednávky vyberte Výroba.</span><span class="sxs-lookup"><span data-stu-id="e5a83-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="e5a83-126">Protože se jedná o dokončený produkt, který bude vyroben, zvolte Výroba.</span><span class="sxs-lookup"><span data-stu-id="e5a83-126">Because this is a finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="e5a83-127">V poli Nákupní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e5a83-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="e5a83-128">Pro ukázku zvolte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="e5a83-128">For the demonstration, select Site 1.</span></span>  
13. <span data-ttu-id="e5a83-129">V poli Skladové pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e5a83-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="e5a83-130">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="e5a83-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="e5a83-131">V poli Prodejní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e5a83-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="e5a83-132">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="e5a83-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="e5a83-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e5a83-133">Close the page.</span></span>

