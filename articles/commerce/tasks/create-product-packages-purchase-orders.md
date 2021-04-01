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
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d16c5c576ce6b35687fb7edab835d52f6f58e6a0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256966"
---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="a47fe-103"> Vytváření balení produktů pro nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="a47fe-103">Create product packages for purchase orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a47fe-104">Tato procedura vás provede vytvářením balíčku výrobku a jeho použití v nákupní objednávce.</span><span class="sxs-lookup"><span data-stu-id="a47fe-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="a47fe-105">Nákupní objednávka se použije k vytvoření objednávky na předdefinování sady produktů.</span><span class="sxs-lookup"><span data-stu-id="a47fe-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="a47fe-106">Tato procedura používá data ukázkové společnosti USRT.</span><span class="sxs-lookup"><span data-stu-id="a47fe-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="a47fe-107">Vytvoření balení produktů</span><span class="sxs-lookup"><span data-stu-id="a47fe-107">Create a product package</span></span>
1. <span data-ttu-id="a47fe-108">Přejděte na Retail and Commerce > Řízení zásob > Doplnění > Balení produktů.</span><span class="sxs-lookup"><span data-stu-id="a47fe-108">Go to Retail and Commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="a47fe-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="a47fe-109">Click New.</span></span>
3. <span data-ttu-id="a47fe-110">Zadejte hodnotu do pole Číslo balíku.</span><span class="sxs-lookup"><span data-stu-id="a47fe-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="a47fe-111">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="a47fe-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a47fe-112">V poli Účet dodavatele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="a47fe-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="a47fe-113">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="a47fe-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="a47fe-114">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="a47fe-114">Click Add.</span></span>
8. <span data-ttu-id="a47fe-115">Do pole Číslo zboží zadejte „0160“.</span><span class="sxs-lookup"><span data-stu-id="a47fe-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="a47fe-116">V poli Velikost kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="a47fe-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="a47fe-117">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="a47fe-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="a47fe-118">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="a47fe-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="a47fe-119">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="a47fe-119">Click Add.</span></span>
13. <span data-ttu-id="a47fe-120">Do pole Číslo zboží zadejte „0160“.</span><span class="sxs-lookup"><span data-stu-id="a47fe-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="a47fe-121">V poli Číslo varianty kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="a47fe-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="a47fe-122">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="a47fe-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="a47fe-123">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="a47fe-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="a47fe-124">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="a47fe-124">Click Add.</span></span>
18. <span data-ttu-id="a47fe-125">Do pole Číslo zboží zadejte „0175“.</span><span class="sxs-lookup"><span data-stu-id="a47fe-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="a47fe-126">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="a47fe-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="a47fe-127">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="a47fe-127">Click Save.</span></span>
21. <span data-ttu-id="a47fe-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a47fe-128">Close the page.</span></span>

## <a name="add-package-to-purchase-order"></a><span data-ttu-id="a47fe-129">Přidání balíku k nákupní objednávce</span><span class="sxs-lookup"><span data-stu-id="a47fe-129">Add package to purchase order</span></span>
1. <span data-ttu-id="a47fe-130">Přejděte na Závazky > Nákupní objednávky > Všechny nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="a47fe-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="a47fe-131">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="a47fe-131">Click New.</span></span>
3. <span data-ttu-id="a47fe-132">V poli Účet dodavatele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="a47fe-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a47fe-133">Na seznamu vyberte stejného dodavatele, pro kterého byl balíček dříve vytvořený, pokud byl vybrán dodavatel.</span><span class="sxs-lookup"><span data-stu-id="a47fe-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="a47fe-134">Přepněte rozšíření oddílu Obecné.</span><span class="sxs-lookup"><span data-stu-id="a47fe-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="a47fe-135">V poli Lokalita kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="a47fe-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="a47fe-136">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="a47fe-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="a47fe-137">V poli Sklad kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="a47fe-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="a47fe-138">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="a47fe-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="a47fe-139">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="a47fe-139">Click OK.</span></span>
11. <span data-ttu-id="a47fe-140">Přepněte rozšíření oddílu Podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="a47fe-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="a47fe-141">Klepněte na kartu Balení produktů.</span><span class="sxs-lookup"><span data-stu-id="a47fe-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="a47fe-142">Klikněte na Řádek nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="a47fe-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="a47fe-143">Klikněte na Vytvořit řádky z balíků.</span><span class="sxs-lookup"><span data-stu-id="a47fe-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="a47fe-144">V rozevíracím seznamu vyhledejte a vyberte balíček produktu vytvořený v předchozím kroku.</span><span class="sxs-lookup"><span data-stu-id="a47fe-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="a47fe-145">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="a47fe-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="a47fe-146">Klikněte na položku Vytvořit.</span><span class="sxs-lookup"><span data-stu-id="a47fe-146">Click Create.</span></span>
18. <span data-ttu-id="a47fe-147">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="a47fe-147">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]