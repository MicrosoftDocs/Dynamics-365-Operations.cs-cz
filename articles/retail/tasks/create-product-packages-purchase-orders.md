---
title: " Vytváření balení produktů pro nákupní objednávky"
description: Tato procedura vás provede vytvářením balíčku výrobku a jeho použití v nákupní objednávce.
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7a7386a9be15f4eeef7aaab73cb320b71994eea
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "360433"
---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="0a8db-103"> Vytváření balení produktů pro nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="0a8db-103">Create product packages for purchase orders</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="0a8db-104">Tato procedura vás provede vytvářením balíčku výrobku a jeho použití v nákupní objednávce.</span><span class="sxs-lookup"><span data-stu-id="0a8db-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="0a8db-105">Nákupní objednávka se použije k vytvoření objednávky na předdefinování sady produktů.</span><span class="sxs-lookup"><span data-stu-id="0a8db-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="0a8db-106">Tato procedura používá data ukázkové společnosti USRT.</span><span class="sxs-lookup"><span data-stu-id="0a8db-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="0a8db-107">Vytvoření balení produktů</span><span class="sxs-lookup"><span data-stu-id="0a8db-107">Create a product package</span></span>
1. <span data-ttu-id="0a8db-108">Přejděte na Maloobchodní a velkoobchodní prodej > Řízení zásob > Doplnění > Balení produktů.</span><span class="sxs-lookup"><span data-stu-id="0a8db-108">Go to Retail and commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="0a8db-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="0a8db-109">Click New.</span></span>
3. <span data-ttu-id="0a8db-110">Zadejte hodnotu do pole Číslo balíku.</span><span class="sxs-lookup"><span data-stu-id="0a8db-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="0a8db-111">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="0a8db-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0a8db-112">V poli Účet dodavatele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="0a8db-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="0a8db-113">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="0a8db-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="0a8db-114">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="0a8db-114">Click Add.</span></span>
8. <span data-ttu-id="0a8db-115">Do pole Číslo zboží zadejte „0160“.</span><span class="sxs-lookup"><span data-stu-id="0a8db-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="0a8db-116">V poli Velikost kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="0a8db-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="0a8db-117">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="0a8db-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="0a8db-118">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="0a8db-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="0a8db-119">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="0a8db-119">Click Add.</span></span>
13. <span data-ttu-id="0a8db-120">Do pole Číslo zboží zadejte „0160“.</span><span class="sxs-lookup"><span data-stu-id="0a8db-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="0a8db-121">V poli Číslo varianty kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="0a8db-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="0a8db-122">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="0a8db-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="0a8db-123">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="0a8db-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="0a8db-124">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="0a8db-124">Click Add.</span></span>
18. <span data-ttu-id="0a8db-125">Do pole Číslo zboží zadejte „0175“.</span><span class="sxs-lookup"><span data-stu-id="0a8db-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="0a8db-126">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="0a8db-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="0a8db-127">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="0a8db-127">Click Save.</span></span>
21. <span data-ttu-id="0a8db-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0a8db-128">Close the page.</span></span>

## <a name="add-package-to-purchase-order"></a><span data-ttu-id="0a8db-129">Přidání balíku k nákupní objednávce</span><span class="sxs-lookup"><span data-stu-id="0a8db-129">Add package to purchase order</span></span>
1. <span data-ttu-id="0a8db-130">Přejděte na Závazky > Nákupní objednávky > Všechny nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="0a8db-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="0a8db-131">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="0a8db-131">Click New.</span></span>
3. <span data-ttu-id="0a8db-132">V poli Účet dodavatele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="0a8db-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="0a8db-133">Na seznamu vyberte stejného dodavatele, pro kterého byl balíček dříve vytvořený, pokud byl vybrán dodavatel.</span><span class="sxs-lookup"><span data-stu-id="0a8db-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="0a8db-134">Přepněte rozšíření oddílu Obecné.</span><span class="sxs-lookup"><span data-stu-id="0a8db-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="0a8db-135">V poli Lokalita kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="0a8db-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="0a8db-136">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="0a8db-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="0a8db-137">V poli Sklad kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="0a8db-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="0a8db-138">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="0a8db-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="0a8db-139">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0a8db-139">Click OK.</span></span>
11. <span data-ttu-id="0a8db-140">Přepněte rozšíření oddílu Podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="0a8db-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="0a8db-141">Klepněte na kartu Balení produktů.</span><span class="sxs-lookup"><span data-stu-id="0a8db-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="0a8db-142">Klikněte na Řádek nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="0a8db-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="0a8db-143">Klikněte na Vytvořit řádky z balíků.</span><span class="sxs-lookup"><span data-stu-id="0a8db-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="0a8db-144">V rozevíracím seznamu vyhledejte a vyberte balíček produktu vytvořený v předchozím kroku.</span><span class="sxs-lookup"><span data-stu-id="0a8db-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="0a8db-145">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="0a8db-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="0a8db-146">Klikněte na položku Vytvořit.</span><span class="sxs-lookup"><span data-stu-id="0a8db-146">Click Create.</span></span>
18. <span data-ttu-id="0a8db-147">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="0a8db-147">Click Save.</span></span>

