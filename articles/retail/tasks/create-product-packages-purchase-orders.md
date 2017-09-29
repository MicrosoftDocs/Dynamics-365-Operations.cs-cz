--- 
title: " Vytváření balení produktů pro nákupní objednávky"
description: "Tato procedura vás provede vytvářením balíčku výrobku a jeho použití v nákupní objednávce."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: a3be1e7aca7f0382aea55fa8a371c33c8b53df95
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="76850-103"> Vytváření balení produktů pro nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="76850-103">Create product packages for purchase orders</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="76850-104">Tato procedura vás provede vytvářením balíčku výrobku a jeho použití v nákupní objednávce.</span><span class="sxs-lookup"><span data-stu-id="76850-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="76850-105">Nákupní objednávka se použije k vytvoření objednávky na předdefinování sady produktů.</span><span class="sxs-lookup"><span data-stu-id="76850-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="76850-106">Tato procedura používá data ukázkové společnosti USRT.</span><span class="sxs-lookup"><span data-stu-id="76850-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="76850-107">Vytvoření balení produktů</span><span class="sxs-lookup"><span data-stu-id="76850-107">Create a product package</span></span>
1. <span data-ttu-id="76850-108">Přejděte na Maloobchodní a velkoobchodní prodej > Řízení zásob > Doplnění > Balení produktů.</span><span class="sxs-lookup"><span data-stu-id="76850-108">Go to Retail and commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="76850-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="76850-109">Click New.</span></span>
3. <span data-ttu-id="76850-110">Zadejte hodnotu do pole Číslo balíku.</span><span class="sxs-lookup"><span data-stu-id="76850-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="76850-111">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="76850-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="76850-112">V poli Účet dodavatele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="76850-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="76850-113">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="76850-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="76850-114">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="76850-114">Click Add.</span></span>
8. <span data-ttu-id="76850-115">Do pole Číslo zboží zadejte „0160“.</span><span class="sxs-lookup"><span data-stu-id="76850-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="76850-116">V poli Velikost kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="76850-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="76850-117">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="76850-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="76850-118">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="76850-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="76850-119">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="76850-119">Click Add.</span></span>
13. <span data-ttu-id="76850-120">Do pole Číslo zboží zadejte „0160“.</span><span class="sxs-lookup"><span data-stu-id="76850-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="76850-121">V poli Číslo varianty kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="76850-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="76850-122">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="76850-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="76850-123">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="76850-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="76850-124">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="76850-124">Click Add.</span></span>
18. <span data-ttu-id="76850-125">Do pole Číslo zboží zadejte „0175“.</span><span class="sxs-lookup"><span data-stu-id="76850-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="76850-126">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="76850-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="76850-127">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="76850-127">Click Save.</span></span>
21. <span data-ttu-id="76850-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="76850-128">Close the page.</span></span>

## <a name="add-package-to-puchase-order"></a><span data-ttu-id="76850-129">Přidání balíku k nákupní objednávce</span><span class="sxs-lookup"><span data-stu-id="76850-129">Add package to puchase order</span></span>
1. <span data-ttu-id="76850-130">Přejděte na Závazky > Nákupní objednávky > Všechny nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="76850-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="76850-131">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="76850-131">Click New.</span></span>
3. <span data-ttu-id="76850-132">V poli Účet dodavatele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="76850-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="76850-133">Na seznamu vyberte stejného dodavatele, pro kterého byl balíček dříve vytvořený, pokud byl vybrán dodavatel.</span><span class="sxs-lookup"><span data-stu-id="76850-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="76850-134">Přepněte rozšíření oddílu Obecné.</span><span class="sxs-lookup"><span data-stu-id="76850-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="76850-135">V poli Lokalita kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="76850-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="76850-136">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="76850-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="76850-137">V poli Sklad kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="76850-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="76850-138">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="76850-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="76850-139">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="76850-139">Click OK.</span></span>
11. <span data-ttu-id="76850-140">Přepněte rozšíření oddílu Podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="76850-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="76850-141">Klepněte na kartu Balení produktů.</span><span class="sxs-lookup"><span data-stu-id="76850-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="76850-142">Klikněte na Řádek nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="76850-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="76850-143">Klikněte na Vytvořit řádky z balíků.</span><span class="sxs-lookup"><span data-stu-id="76850-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="76850-144">V rozevíracím seznamu vyhledejte a vyberte balíček produktu vytvořený v předchozím kroku.</span><span class="sxs-lookup"><span data-stu-id="76850-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="76850-145">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="76850-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="76850-146">Klikněte na položku Vytvořit.</span><span class="sxs-lookup"><span data-stu-id="76850-146">Click Create.</span></span>
18. <span data-ttu-id="76850-147">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="76850-147">Click Save.</span></span>


