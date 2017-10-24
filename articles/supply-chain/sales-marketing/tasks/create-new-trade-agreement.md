--- 
title: "Vytvoření nové obchodní smlouvy"
description: "Tento postup popisuje vytvoření obchodní dohody, u které zaregistrujete novou prodejní cenu produktu odsouhlasenou se specifickým odběratelem."
author: omulvad
manager: AnnBe
ms.date: 11/11/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1eb7a945243387f85ec5f38cc3b969d8d030ff25
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="d9e6b-103">Vytvoření nové obchodní smlouvy</span><span class="sxs-lookup"><span data-stu-id="d9e6b-103">Create a new trade agreement</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d9e6b-104">Tento postup popisuje vytvoření obchodní dohody, u které zaregistrujete novou prodejní cenu produktu odsouhlasenou se specifickým odběratelem.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="d9e6b-105">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="d9e6b-106">Při použití vlastních dat před zahájením tohoto průvodce ověřte, že existuje název deníku obchodních smluv, kde je výchozí vztah je nastaven na „Cena (prodej)“.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-106">If you’re using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to “Price (sales)”.</span></span>


## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="d9e6b-107">Vytvoření a zaúčtování nového deníku obchodní smlouvy</span><span class="sxs-lookup"><span data-stu-id="d9e6b-107">Create and post a new trade agreement journal</span></span>
1. <span data-ttu-id="d9e6b-108">Přejděte do nabídky Prodej a marketing > Ceny a slevy > Deníky obchodních smluv.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-108">Go to Sales and marketing > Prices and discounts > Trade agreement journals.</span></span>
2. <span data-ttu-id="d9e6b-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-109">Click New.</span></span>
3. <span data-ttu-id="d9e6b-110">V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="d9e6b-111">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d9e6b-112">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d9e6b-113">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-113">Click Lines.</span></span>
7. <span data-ttu-id="d9e6b-114">V poli Kód účtu vyberte možnost Tabulka.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-114">In the Account code field, select 'Table'.</span></span>
    * <span data-ttu-id="d9e6b-115">V tomto příkladu aktualizujete cenu pro určitého odběratele, což znamená, že je nutné vybrat tabulku.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-115">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="d9e6b-116">Pokud byste aktualizovali katalogovou cenu produktu, vybrali byste Vše, aby nová cena platila pro všechny odběratele.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-116">If you were updating the product's list price, you would select All, so that the new price is valid for all customers.</span></span> <span data-ttu-id="d9e6b-117">Pokud byste používali různé ceny v různých segmentech odběratelů, vybrali byste možnost Skupina.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-117">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="d9e6b-118">Chcete-li vybrat skupinu, musíte nastavit možnost Cenové skupiny odběratele.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-118">To select Group, you must have set up Customer price groups.</span></span>  
8. <span data-ttu-id="d9e6b-119">V poli Výběr účtu kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-119">In the Account selection field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="d9e6b-120">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-120">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="d9e6b-121">V poli Kód položky vyberte položku Tabulka.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-121">In the Item code field, select 'Table'.</span></span>
    * <span data-ttu-id="d9e6b-122">Při zadávání typu obchodní smlouvy Cena (prodej) je nutné vybrat pouze „Tabulka“ v poli Kód položky.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-122">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the Item code field.</span></span> <span data-ttu-id="d9e6b-123">Důvodem je skutečnost, že cena je absolutní hodnota a nesmí být stejná pro všechny produkty nebo skupinu produktů.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-123">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>  
11. <span data-ttu-id="d9e6b-124">V poli Vztah položky kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-124">In the Item relation field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="d9e6b-125">V seznamu vyberte produkt, který chcete do smlouvy zahrnout.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-125">In the list, select the product you want to include in the agreement.</span></span>
    * <span data-ttu-id="d9e6b-126">Poznamenejte produkt, který jste vybrali.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-126">Make a note of which product you've selected.</span></span>  
13. <span data-ttu-id="d9e6b-127">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="d9e6b-128">Zadejte minimální množství do pole Od.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-128">In the From field, enter a minimum quantity.</span></span>
    * <span data-ttu-id="d9e6b-129">Pokud odběratel musí objednávat minimální množství, je třeba zde zadat množství, jinak nebude mít na novou cenu nárok.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-129">If the customer has to order a minimum quantity  before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    * <span data-ttu-id="d9e6b-130">Zadáním hodnoty do pole Do určete maximální množství, nad které nebude cena ve smlouvě platit.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-130">Enter a value in the To field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="d9e6b-131">Pokud nabízíte ceny a slevy založené na několika množstevních kategoriích, zadejte každou množstevní kategorii jako pár minimálního a maximálního množství do polí Od a Do.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-131">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the 'From' and 'To' fields respectively.</span></span>  
15. <span data-ttu-id="d9e6b-132">Zadejte cenu do pole Částka v měně.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-132">In the Amount in currency field, enter a price.</span></span>
16. <span data-ttu-id="d9e6b-133">V poli Od data zadejte datum, od kterého bude tato smlouva platit.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-133">In the From date field, enter a date from which this agreement will be valid.</span></span>
17. <span data-ttu-id="d9e6b-134">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-134">Click Save.</span></span>
18. <span data-ttu-id="d9e6b-135">Klikněte na tlačítko Ověřit.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-135">Click Validate.</span></span>
19. <span data-ttu-id="d9e6b-136">Klikněte na možnost Ověřit vybrané řádky.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-136">Click Validate selected lines.</span></span>
20. <span data-ttu-id="d9e6b-137">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-137">Click OK.</span></span>
21. <span data-ttu-id="d9e6b-138">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-138">Click Post.</span></span>
22. <span data-ttu-id="d9e6b-139">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-139">Click OK.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="d9e6b-140">Zobrazení obchodních smluv pro produkt</span><span class="sxs-lookup"><span data-stu-id="d9e6b-140">View trade agreements for a product</span></span>
1. <span data-ttu-id="d9e6b-141">Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-141">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="d9e6b-142">V seznamu najděte a vyberte produkt, jehož cenu jste právě aktualizovali.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-142">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="d9e6b-143">V podokně akcí klikněte na možnost Prodej.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-143">On the Action Pane, click Sell.</span></span>
4. <span data-ttu-id="d9e6b-144">Klikněte na možnost Zobrazit obchodní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-144">Click View trade agreements.</span></span>
    * <span data-ttu-id="d9e6b-145">Zkontrolujte podrobnosti obchodní smlouvy o cenách, kterou jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-145">Review the details of the price trade agreement you have just created.</span></span>    
5. <span data-ttu-id="d9e6b-146">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-146">Close the page.</span></span>


