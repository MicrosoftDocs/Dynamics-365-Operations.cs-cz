--- 
title: "Expedování prodejních objednávek bez skladování"
description: "Tato příručka ukazuje, jak aktualizovat prodejní objednávku, když jsou výrobky odeslány odběrateli."
author: omulvad
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d0ad0869907b23ce5e0b44e3e9ecee3f2cd34ede
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="ship-sales-orders-without-warehousing"></a><span data-ttu-id="b19a0-103">Expedování prodejních objednávek bez skladování</span><span class="sxs-lookup"><span data-stu-id="b19a0-103">Ship sales orders without warehousing</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b19a0-104">Tato příručka ukazuje, jak aktualizovat prodejní objednávku, když jsou výrobky odeslány odběrateli.</span><span class="sxs-lookup"><span data-stu-id="b19a0-104">This guide demonstrates how to update a sales order when products are shipped to the customer.</span></span> <span data-ttu-id="b19a0-105">Průvodce lze použít pro tok plnění, který není nastaven pro správu skladu (ani základní ani rozšířené funkce skladu), a proto nevyžaduje zaregistrování výdeje produktu mají před dodávkou.</span><span class="sxs-lookup"><span data-stu-id="b19a0-105">The guide is applicable to the fulfillment flow that is not set up for warehouse management (neither basic or advanced warehousing), and therefore does not require product picking to be registered before shipment.</span></span> <span data-ttu-id="b19a0-106">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="b19a0-106">You can run this procedure on your own data or in demo data company USMF.</span></span> <span data-ttu-id="b19a0-107">V obou případech před spuštěním této úlohy vytvořte prodejní objednávku pro produkt na skladě s množstvím větším než 1.</span><span class="sxs-lookup"><span data-stu-id="b19a0-107">In both cases, before you start this task, create a sales order for an inventoried product with a quantity of greater than 1.</span></span> <span data-ttu-id="b19a0-108">Abyste předešli chybě zaúčtování, je třeba zkontrolovat, že množství produktu na skladě na pracovišti a ve skladu, které jste vybrali na objednávce, zahrnuje množství objednávky.</span><span class="sxs-lookup"><span data-stu-id="b19a0-108">To avoid a posting error, you need to check that the product's on-hand quantity in the site and warehouse that you’ve selected on the order covers the order quantity.</span></span>


## <a name="post-packing-slip-for-an-order"></a><span data-ttu-id="b19a0-109">Zaúčtování dodacího listu pro objednávku</span><span class="sxs-lookup"><span data-stu-id="b19a0-109">Post packing slip for an order</span></span>
1. <span data-ttu-id="b19a0-110">Přejděte na Prodej a marketing > Prodejní objednávky > Všechny prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="b19a0-110">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="b19a0-111">V seznamu vyhledejte a vyberte objednávku, kterou jste vytvořili pro tento úkol.</span><span class="sxs-lookup"><span data-stu-id="b19a0-111">In the list, find and select the order you have created for this task.</span></span>
3. <span data-ttu-id="b19a0-112">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="b19a0-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b19a0-113">V podokně akcí klikněte na tlačítko Vyskladnit a zabalit.</span><span class="sxs-lookup"><span data-stu-id="b19a0-113">On the Action Pane, click Pick and pack.</span></span>
5. <span data-ttu-id="b19a0-114">Klikněte na Zaúčtovat dodací list.</span><span class="sxs-lookup"><span data-stu-id="b19a0-114">Click Post packing slip.</span></span>
6. <span data-ttu-id="b19a0-115">Rozbalte nebo sbalte oddíl Parametry.</span><span class="sxs-lookup"><span data-stu-id="b19a0-115">Expand or collapse the Parameters section.</span></span>
7. <span data-ttu-id="b19a0-116">V poli Množství vyberte možnost Vše.</span><span class="sxs-lookup"><span data-stu-id="b19a0-116">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="b19a0-117">Ostatní možnosti zahrnují Dodat nyní a Vyskladněno.</span><span class="sxs-lookup"><span data-stu-id="b19a0-117">Other options include Deliver now and Picked.</span></span> <span data-ttu-id="b19a0-118">Pokud řádek objednávky má být částečně dodán a pole Dodat nyní v řádku objednávky obsahuje nějaké množství, vybrali byste Dodat nyní.</span><span class="sxs-lookup"><span data-stu-id="b19a0-118">If the order line is to be shipped partially and the Deliver now field on the order line contains a quantity, you would select Deliver now.</span></span> <span data-ttu-id="b19a0-119">Pokud tok plnění vaší organizace zahrnuje výdej jako samostatný proces, který je spravován a zaregistrován ve výdejce, měli byste vybrat Vyskladněno.</span><span class="sxs-lookup"><span data-stu-id="b19a0-119">If your organization's fulfillment flow includes picking as a separate process that is managed by and registered with a picking list, you would select Picked.</span></span>  
    * <span data-ttu-id="b19a0-120">Zkontrolujte, zda je Možnost zaúčtování nastavena na hodnotu Ano.</span><span class="sxs-lookup"><span data-stu-id="b19a0-120">Check that the Posting option is set to Yes.</span></span>  
8. <span data-ttu-id="b19a0-121">Nastavte možnost Tisk dodacího listu na Ano.</span><span class="sxs-lookup"><span data-stu-id="b19a0-121">Set the Print packing slip option to Yes.</span></span>
    * <span data-ttu-id="b19a0-122">Karta Přehled obsahuje seznam dodacích listů k vygenerování v tomto zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="b19a0-122">The Overview tab contains a list of packing slips to be generated in this posting.</span></span> <span data-ttu-id="b19a0-123">Pokud dodáváte jednotlivé objednávky, obvykle bude jeden dodací list.</span><span class="sxs-lookup"><span data-stu-id="b19a0-123">If you are shipping an individual order, there will typically be one packing slip.</span></span> <span data-ttu-id="b19a0-124">Avšak jsou-li řádky objednávky, která má být expedována, z různých pracovišť, zaúčtování bude automaticky rozděleno na příslušný počet dokumentů.</span><span class="sxs-lookup"><span data-stu-id="b19a0-124">However, if that order's lines are to be shipped from different sites, posting will automatically be split into the appropriate number of documents.</span></span> <span data-ttu-id="b19a0-125">Jedná se o povinnou podmínku, kterou nelze změnit.</span><span class="sxs-lookup"><span data-stu-id="b19a0-125">This is a mandatory condition that cannot be changed.</span></span> <span data-ttu-id="b19a0-126">Obdobně platí, že zaúčtování bude rovněž rozděleno do několika dokumentů, pokud mají řádky objednávky k dodání různé doručovací adresy a nastavení zásad expedice vyžaduje rozdělení.</span><span class="sxs-lookup"><span data-stu-id="b19a0-126">Similarly, the posting will also be split into multiple documents if the order’s lines are to be shipped to different delivery addresses, and the shipping policy is set up to require a split.</span></span>  
9. <span data-ttu-id="b19a0-127">Na kartě Řádky vyberte řádek pro řádek objednávky k expedici.</span><span class="sxs-lookup"><span data-stu-id="b19a0-127">On the Lines tab, select the row for the order line to be shipped.</span></span>
10. <span data-ttu-id="b19a0-128">V poli Aktualizace zadejte číslo menší než původní množství.</span><span class="sxs-lookup"><span data-stu-id="b19a0-128">In the Update field, enter a number lower than the original quantity.</span></span>
11. <span data-ttu-id="b19a0-129">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b19a0-129">Click OK.</span></span>
12. <span data-ttu-id="b19a0-130">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="b19a0-130">Click Yes.</span></span>
13. <span data-ttu-id="b19a0-131">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b19a0-131">Close the page.</span></span>
14. <span data-ttu-id="b19a0-132">V podokně akcí klikněte na Možnosti.</span><span class="sxs-lookup"><span data-stu-id="b19a0-132">On the Action Pane, click Options.</span></span>
15. <span data-ttu-id="b19a0-133">Klikněte na tlačítko Změnit zobrazení.</span><span class="sxs-lookup"><span data-stu-id="b19a0-133">Click Change view.</span></span>
16. <span data-ttu-id="b19a0-134">Klikněte na možnost Zobrazení záhlaví.</span><span class="sxs-lookup"><span data-stu-id="b19a0-134">Click Header view.</span></span>
    * <span data-ttu-id="b19a0-135">Pokud byly plně expedovány všechny řádky objednávky, stav zakázky se změní z otevřeného na dodáno.</span><span class="sxs-lookup"><span data-stu-id="b19a0-135">If all of the lines on the order have been fully shipped, the order status changes from Open to Delivered.</span></span>  
    * <span data-ttu-id="b19a0-136">V tomto případě byl řádek objednávky expedován částečně.</span><span class="sxs-lookup"><span data-stu-id="b19a0-136">In this example, the order line has been shipped partially.</span></span> <span data-ttu-id="b19a0-137">Toto je důvod, proč stav objednávky zůstane otevřený.</span><span class="sxs-lookup"><span data-stu-id="b19a0-137">This is why the order status remains Open.</span></span>     
    * <span data-ttu-id="b19a0-138">Pole Stav dokumentu je nastaveno na Dodací list, protože alespoň jeden z řádků objednávky byl dodán.</span><span class="sxs-lookup"><span data-stu-id="b19a0-138">The Document status field is set to Packing slip because at least one of the order lines have been shipped.</span></span>  
17. <span data-ttu-id="b19a0-139">V podokně akcí klikněte na položku Obecné.</span><span class="sxs-lookup"><span data-stu-id="b19a0-139">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="b19a0-140">Klepněte na Množství řádků.</span><span class="sxs-lookup"><span data-stu-id="b19a0-140">Click Line quantity.</span></span>
19. <span data-ttu-id="b19a0-141">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b19a0-141">Close the page.</span></span>
20. <span data-ttu-id="b19a0-142">V podokně akcí klikněte na položku Vyskladnit a zabalit.</span><span class="sxs-lookup"><span data-stu-id="b19a0-142">On the Action Pane, click Pick and pack.</span></span>
21. <span data-ttu-id="b19a0-143">Klepněte na Dodací list.</span><span class="sxs-lookup"><span data-stu-id="b19a0-143">Click Packing slip.</span></span>
    * <span data-ttu-id="b19a0-144">Stránka deníku dodacího listu obsahuje všechny dokumenty dodacího listu, které byly vygenerovány pro vaši objednávku.</span><span class="sxs-lookup"><span data-stu-id="b19a0-144">The Packing slip journal page contains all the packing slip documents that were generated for your order.</span></span> <span data-ttu-id="b19a0-145">Můžete zkontrolovat podrobnosti o jednotlivých dokumentech a vytisknout je v případě potřeby.</span><span class="sxs-lookup"><span data-stu-id="b19a0-145">You can review details of each document and print them, if needed.</span></span>  


