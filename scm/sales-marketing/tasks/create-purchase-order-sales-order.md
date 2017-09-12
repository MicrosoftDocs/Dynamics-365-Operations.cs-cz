--- 
title: "Vytvoření nákupní objednávky z prodejní objednávky"
description: "Tento postup zobrazuje, jak vytvořit nákupní objednávku na základě plánu prodejní objednávky."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 412a8c7acca06fc1be073019f91144e2a3f1c94b
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-purchase-order-from-a-sales-order"></a><span data-ttu-id="b0502-103">Vytvoření nákupní objednávky z prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="b0502-103">Create a purchase order from a sales order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b0502-104">Tento postup zobrazuje, jak vytvořit nákupní objednávku na základě plánu prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="b0502-104">This procedure shows you how to create a purchase order that is based on a sales order.</span></span> <span data-ttu-id="b0502-105">Množství produktu na nákupní objednávce je pak označeno k uspokojení poptávky původní prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="b0502-105">The product's quantities on the purchase order are then designated to fulfill the demand of the originating sales order.</span></span> <span data-ttu-id="b0502-106">Plnění prodejní poptávky tímto způsobem je alternativou k více srozumitelné a optimalizované metodě požadavků plánování distribuce.</span><span class="sxs-lookup"><span data-stu-id="b0502-106">Fulfilling sales demand this way is an alternative to a more comprehensive and optimized method of Distribution Requirements Planning.</span></span> <span data-ttu-id="b0502-107">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="b0502-107">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-a-purchase-order-from-a-sales-order"></a><span data-ttu-id="b0502-108">Vytvoření nákupní objednávky z prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="b0502-108">Create a purchase order from a sales order</span></span>
1. <span data-ttu-id="b0502-109">Přejděte na Prodej a marketing > Prodejní objednávky > Všechny prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="b0502-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="b0502-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b0502-110">Click New.</span></span>
3. <span data-ttu-id="b0502-111">V poli Účet odběratele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="b0502-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b0502-112">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="b0502-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="b0502-113">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b0502-113">Click OK.</span></span>
6. <span data-ttu-id="b0502-114">V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="b0502-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="b0502-115">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="b0502-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b0502-116">Pokud používáte data USMF, můžete vybrat položku D0001.</span><span class="sxs-lookup"><span data-stu-id="b0502-116">If you're using USMF, you could select D0001.</span></span>  
8. <span data-ttu-id="b0502-117">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="b0502-117">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="b0502-118">Klikněte na položku Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="b0502-118">Click Add line.</span></span>
10. <span data-ttu-id="b0502-119">V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="b0502-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="b0502-120">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="b0502-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b0502-121">Pokud používáte data USMF, můžete vybrat položku T0020.</span><span class="sxs-lookup"><span data-stu-id="b0502-121">If you're using USMF, you could select T0020.</span></span>  
12. <span data-ttu-id="b0502-122">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="b0502-122">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="b0502-123">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="b0502-123">In the Quantity field, enter a number.</span></span>
14. <span data-ttu-id="b0502-124">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="b0502-124">Click Save.</span></span>
15. <span data-ttu-id="b0502-125">V podokně akcí klikněte na položku Prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="b0502-125">On the Action Pane, click Sales order.</span></span>
16. <span data-ttu-id="b0502-126">Klikněte na Nákupní objednávku.</span><span class="sxs-lookup"><span data-stu-id="b0502-126">Click Purchase order.</span></span>
    * <span data-ttu-id="b0502-127">Vytvoření seznamů stránek nákupních objednávek všech otevřených řádků prodejních objednávek, které byly zkopírovány z prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="b0502-127">The Create purchase order page lists all the open sales order lines which have been copied from the sales order.</span></span> <span data-ttu-id="b0502-128">Je možné zkontrolovat podrobnosti o objednávce, a v případě potřeby můžete upravit vybrané informace, například nákupní množství a cenách podmínek předtím, než vytvoříte objednávku.</span><span class="sxs-lookup"><span data-stu-id="b0502-128">You can review the order details, and if required, you can modify selected details such purchase quantity and pricing terms, before you create the purchases.</span></span>  
17. <span data-ttu-id="b0502-129">Vyberte možnost Zahrnout vše.</span><span class="sxs-lookup"><span data-stu-id="b0502-129">Select the Include all option.</span></span>
    * <span data-ttu-id="b0502-130">Pokud chcete generovat nákupní objednávku pouze pro podmnožinu řádků prodejních objednávek, vyberte je jednotlivě.</span><span class="sxs-lookup"><span data-stu-id="b0502-130">If you want to generate purchase orders for only a subset of the sales order lines, select these individually.</span></span>  
    * <span data-ttu-id="b0502-131">Pole účtu dodavatele může nebo nemusí být vyplněno číslem dodavatele.</span><span class="sxs-lookup"><span data-stu-id="b0502-131">The Vendor account field may or may not already be populated with a vendor number.</span></span> <span data-ttu-id="b0502-132">Pokud bude výchozí dodavatele nastaven pro produkt (v přidružené disponibilitě položky), pak do řádku bude zkopírován tento dodavatel.</span><span class="sxs-lookup"><span data-stu-id="b0502-132">If the default vendor is set up for the product (on the associated Item coverage) then this vendor will be copied  to the line.</span></span> <span data-ttu-id="b0502-133">V ostatních případech musíte dodavatele zadat ručně.</span><span class="sxs-lookup"><span data-stu-id="b0502-133">Otherwise, you must enter a vendor manually.</span></span>  <span data-ttu-id="b0502-134">V této příručce bez ohledu na to, zda pole účtu dodavatele již obsahuje hodnotu či nikoli, vám další kroky poradí, jak vybrat nového dodavatele, který se liší pro každý řádek.</span><span class="sxs-lookup"><span data-stu-id="b0502-134">In this guide, regardless of whether the Vendor account field already contains a value or not, the following steps instruct you to select a new vendor which is different for each line.</span></span>  
18. <span data-ttu-id="b0502-135">V poli Účet dodavatele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="b0502-135">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="b0502-136">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="b0502-136">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="b0502-137">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="b0502-137">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="b0502-138">Vyberte druhý řádek objednávky.</span><span class="sxs-lookup"><span data-stu-id="b0502-138">Select the second order line.</span></span>
22. <span data-ttu-id="b0502-139">V poli Účet dodavatele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="b0502-139">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="b0502-140">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="b0502-140">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="b0502-141">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="b0502-141">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="b0502-142">Klikněte na tlačítko Ověřit.</span><span class="sxs-lookup"><span data-stu-id="b0502-142">Click Validate.</span></span>
26. <span data-ttu-id="b0502-143">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b0502-143">Click OK.</span></span>
    * <span data-ttu-id="b0502-144">Zpráva vás informuje o tom, že jedna nebo více nákupních objednávek nyní bylo vytvořeno.</span><span class="sxs-lookup"><span data-stu-id="b0502-144">The message informs you that one or more purchase orders have been created.</span></span> <span data-ttu-id="b0502-145">Systém vygeneruje jednotlivou nákupní objednávku pro každého dodavatele, kterého jste určili pro řádky prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="b0502-145">The system generates a separate purchase order for each vendor that you specified for the sales order lines.</span></span> <span data-ttu-id="b0502-146">To znamená, že pokud několik řádků prodejní objednávky má být zásobováno stejným dodavatelem, bude vygenerována jedna nákupní objednávka s více řádky.</span><span class="sxs-lookup"><span data-stu-id="b0502-146">This means that if several sales order lines are to be supplied by the same vendor, a single purchase order with multiple lines will be generated.</span></span>  

## <a name="review-purchase-orders-created-from-sales-orders"></a><span data-ttu-id="b0502-147">Zkontrolujte nákupní objednávky vytvořené z prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="b0502-147">Review purchase orders created from sales orders</span></span>
1. <span data-ttu-id="b0502-148">V podokně akcí klikněte na položku Obecné.</span><span class="sxs-lookup"><span data-stu-id="b0502-148">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="b0502-149">Klepněte na Související objednávky.</span><span class="sxs-lookup"><span data-stu-id="b0502-149">Click Related orders.</span></span>
    * <span data-ttu-id="b0502-150">Stránky se seznamem souvisejících objednávek všech objednávek, které byly vytvořeny z prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="b0502-150">The Related orders page lists all the orders that were created from the sales order.</span></span> <span data-ttu-id="b0502-151">V tomto příkladu jsou dvě nákupní objednávky, které jsou generovány pro dva různé dodavatele v uvedeném pořadí.</span><span class="sxs-lookup"><span data-stu-id="b0502-151">In this example, there are two purchase orders generated for two different vendors respectively.</span></span>  
3. <span data-ttu-id="b0502-152">Kliknutím přejdete na odkaz v poli Nákupní objednávka.</span><span class="sxs-lookup"><span data-stu-id="b0502-152">Click to follow the link in the Purchase order field.</span></span>
    * <span data-ttu-id="b0502-153">Každý řádek nákupní objednávky je přidružen k řádku prodejní objednávky, který k nákupu vedl.</span><span class="sxs-lookup"><span data-stu-id="b0502-153">Each purchase order line is associated with the sales order line that led to the purchase.</span></span> <span data-ttu-id="b0502-154">Vztah k prodejní objednávce je označen na kartě produktu na pevné kartě Podrobnosti řádku v polích Typ odkazu, Číslo odkazu a Odkaz na šarži.</span><span class="sxs-lookup"><span data-stu-id="b0502-154">The relation to the sales order is indicated on the Product tab in the Line details FastTab, in the Reference type, Reference number, and Reference lot fields.</span></span>  
4. <span data-ttu-id="b0502-155">Rozbalte nebo sbalte oddíl Podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="b0502-155">Expand or collapse the Line details section.</span></span>
5. <span data-ttu-id="b0502-156">Klepněte na kartu Produkt.</span><span class="sxs-lookup"><span data-stu-id="b0502-156">Click the Product tab.</span></span>
    * <span data-ttu-id="b0502-157">Odkaz na šarži zajišťuje, že náklady aktuálního nákupu budu zpoplatněny na připojené prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="b0502-157">The Reference lot guarantees that the costs from the current purchase are charged on the attached sales order.</span></span>  
    * <span data-ttu-id="b0502-158">Otevřením odkazu v poli referenční číslo můžete přejít na původní prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="b0502-158">You can navigate to the originating sales order by opening the link in the Reference number field.</span></span>  


