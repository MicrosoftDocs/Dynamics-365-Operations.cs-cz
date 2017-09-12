--- 
title: "Správa blokování objednávek"
description: "Tento postup ukazuje, jak blokovat prodejní objednávky odběratele, jak pracovat s rezervacemi blokovaných objednávek a jak odebrat blokování objednávky."
author: omulvad
manager: AnnBe
ms.date: 01/09/2017
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
ms.openlocfilehash: e9a520b2af7cdfef325f1fa96504f2a20078ed80
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="manage-order-holds"></a><span data-ttu-id="5aa89-103">Správa blokování objednávek</span><span class="sxs-lookup"><span data-stu-id="5aa89-103">Manage order holds</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5aa89-104">Tento postup ukazuje, jak blokovat prodejní objednávky odběratele, jak pracovat s rezervacemi blokovaných objednávek a jak odebrat blokování objednávky.</span><span class="sxs-lookup"><span data-stu-id="5aa89-104">This procedure demonstrates how to place customer sales orders on hold, how to work with order hold checkouts, and how to remove order holds.</span></span> <span data-ttu-id="5aa89-105">Objednávka může být blokována z mnoha důvodů.</span><span class="sxs-lookup"><span data-stu-id="5aa89-105">An order might be placed on hold for a variety of reasons.</span></span> <span data-ttu-id="5aa89-106">Můžete například blokovat objednávku, dokud není ověřena adresa odběratele nebo platební metoda nebo dokud správce nezkontroluje úvěrový limit odběratele.</span><span class="sxs-lookup"><span data-stu-id="5aa89-106">For example, you might hold an order until a customer address or payment method can be verified or until a manager can review the customer’s credit limit.</span></span> <span data-ttu-id="5aa89-107">Když je objednávka blokována, nelze ji zpracovat skladem pro expedici.</span><span class="sxs-lookup"><span data-stu-id="5aa89-107">While the order on hold, it cannot be processed by the warehouse for shipping.</span></span> 

<span data-ttu-id="5aa89-108">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="5aa89-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-order-holds"></a><span data-ttu-id="5aa89-109">Nastavení blokování objednávky</span><span class="sxs-lookup"><span data-stu-id="5aa89-109">Set up order holds</span></span>
1. <span data-ttu-id="5aa89-110">Přejděte na Prodej a marketing > Nastavení > Prodejní objednávky > Kódy blokování objednávek.</span><span class="sxs-lookup"><span data-stu-id="5aa89-110">Go to Sales and marketing > Setup > Sales orders > Order hold codes.</span></span>
2. <span data-ttu-id="5aa89-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="5aa89-111">Click New.</span></span>
3. <span data-ttu-id="5aa89-112">V poli Kód blokování zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="5aa89-112">In the Hold code field, type a value.</span></span>
    * <span data-ttu-id="5aa89-113">Zadejte například Zpětné volání.</span><span class="sxs-lookup"><span data-stu-id="5aa89-113">For example, type Call back.</span></span>  
4. <span data-ttu-id="5aa89-114">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="5aa89-114">In the Description field, type a value.</span></span>
    * <span data-ttu-id="5aa89-115">Například blokovaná objednávka čekající na zpětné volání odběratele.</span><span class="sxs-lookup"><span data-stu-id="5aa89-115">For example, Order held waiting for customer callback.</span></span>  
    * <span data-ttu-id="5aa89-116">Volitelně zaškrtněte políčko Odebrat rezervace, abyste odstranili všechny fyzické rezervace z objednávky, když je přidán kód blokování.</span><span class="sxs-lookup"><span data-stu-id="5aa89-116">Optionally, select the Remove reservations check box to remove any physical reservations from the order when this hold code is added.</span></span>  
5. <span data-ttu-id="5aa89-117">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5aa89-117">Click Save.</span></span>

## <a name="place-order-on-hold"></a><span data-ttu-id="5aa89-118">Zablokování objednávky</span><span class="sxs-lookup"><span data-stu-id="5aa89-118">Place order on hold</span></span>
1. <span data-ttu-id="5aa89-119">Přejděte na Prodej a marketing > Prodejní objednávky > Všechny prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="5aa89-119">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="5aa89-120">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="5aa89-120">Click New.</span></span>
3. <span data-ttu-id="5aa89-121">V poli Účet odběratele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="5aa89-121">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="5aa89-122">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="5aa89-122">Click OK.</span></span>
5. <span data-ttu-id="5aa89-123">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="5aa89-123">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="5aa89-124">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="5aa89-124">In the Quantity field, enter a number.</span></span>
7. <span data-ttu-id="5aa89-125">V podokně akcí klikněte na položku Prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="5aa89-125">On the Action Pane, click Sales order.</span></span>
8. <span data-ttu-id="5aa89-126">Klikněte na Blokování objednávky.</span><span class="sxs-lookup"><span data-stu-id="5aa89-126">Click Order holds.</span></span>
9. <span data-ttu-id="5aa89-127">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="5aa89-127">Click New.</span></span>
10. <span data-ttu-id="5aa89-128">V poli Kód blokování vyberte kód, který jste vytvořili v předchozím dílčím úkolu.</span><span class="sxs-lookup"><span data-stu-id="5aa89-128">In the Hold code field, select the code you have created in the previous subtask.</span></span>
11. <span data-ttu-id="5aa89-129">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5aa89-129">Click Save.</span></span>
12. <span data-ttu-id="5aa89-130">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5aa89-130">Close the page.</span></span>
13. <span data-ttu-id="5aa89-131">Přejděte na Prodej a marketing > Prodejní objednávky > Všechny prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="5aa89-131">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
14. <span data-ttu-id="5aa89-132">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="5aa89-132">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="5aa89-133">Objednávky, které jsou aktuálně blokovány, mají označena pole „Nezpracovávat a „Blokace“.</span><span class="sxs-lookup"><span data-stu-id="5aa89-133">Orders that are currently on hold have the "Do not process" and "Hold" fields marked.</span></span>    
15. <span data-ttu-id="5aa89-134">V podokně akcí klikněte na položku Vyskladnit a zabalit.</span><span class="sxs-lookup"><span data-stu-id="5aa89-134">On the Action Pane, click Pick and pack.</span></span>

## <a name="manage-order-holds"></a><span data-ttu-id="5aa89-135">Správa blokování objednávek</span><span class="sxs-lookup"><span data-stu-id="5aa89-135">Manage order holds</span></span>
1. <span data-ttu-id="5aa89-136">Přejděte na Prodej a marketing > Prodejní objednávky > Otevřené objednávky > Blokování objednávky.</span><span class="sxs-lookup"><span data-stu-id="5aa89-136">Go to Sales and marketing > Sales orders > Open orders > Order holds.</span></span>
    * <span data-ttu-id="5aa89-137">Stránka s blokovanými objednávkami funguje jako pracovní plocha, kde můžete získat přehled všech aktuálních a zpracovaných blokování, se kterými zde můžete pracovat, a přidružených prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="5aa89-137">Order holds page functions as a workbench where you can get an overview of all the current and processed holds, and handle them and associated sales orders.</span></span>      
2. <span data-ttu-id="5aa89-138">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="5aa89-138">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="5aa89-139">V podokně akcí klikněte na Rezervace blokování.</span><span class="sxs-lookup"><span data-stu-id="5aa89-139">On the Action Pane, click Hold checkout.</span></span>
4. <span data-ttu-id="5aa89-140">Klikněte na možnost Rezervace.</span><span class="sxs-lookup"><span data-stu-id="5aa89-140">Click Check out.</span></span>
5. <span data-ttu-id="5aa89-141">Odznačte vybraný řádek na seznamu.</span><span class="sxs-lookup"><span data-stu-id="5aa89-141">In the list, unmark the selected row.</span></span>
    * <span data-ttu-id="5aa89-142">Pole Rezervovat komu nyní zobrazuje vaše uživatelské ID.</span><span class="sxs-lookup"><span data-stu-id="5aa89-142">The Checkout out to field now shows your user ID.</span></span>   
6. <span data-ttu-id="5aa89-143">Klikněte na možnost Vymazat rezervaci.</span><span class="sxs-lookup"><span data-stu-id="5aa89-143">Click Clear checkout.</span></span>
7. <span data-ttu-id="5aa89-144">V podokně akcí klikněte na možnost Vymazat blokování.</span><span class="sxs-lookup"><span data-stu-id="5aa89-144">On the Action Pane, click Clear hold.</span></span>
    * <span data-ttu-id="5aa89-145">Když jste připraveni odebrat blokování a umožnit objednávce, aby pokračovala k dalšímu kroku plnění, musíte blokování vymazat.</span><span class="sxs-lookup"><span data-stu-id="5aa89-145">When you are ready to remove the hold and allow the order to proceed to the next fulfilment step, you must clear the hold.</span></span> <span data-ttu-id="5aa89-146">Nevyžaduje-li objednávka žádné změny, můžete spustit akci Vymazat blokování.</span><span class="sxs-lookup"><span data-stu-id="5aa89-146">If the order requires no changes, you can run the Clear holds action.</span></span> <span data-ttu-id="5aa89-147">Můžete však použít akci Vymazat a upravit, pokud je třeba při vymazání blokování objednávku aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="5aa89-147">However, you can use the Clear and modify action if, when clearing a hold, the order has to be updated.</span></span>      
    * <span data-ttu-id="5aa89-148">Akce Vymazat a odeslat je použitelná pouze při použití funkce kontaktního střediska.</span><span class="sxs-lookup"><span data-stu-id="5aa89-148">The Clear and submit action is only applicable when you use Call center functionality.</span></span>  
8. <span data-ttu-id="5aa89-149">Klikněte na možnost Vymazat blokování.</span><span class="sxs-lookup"><span data-stu-id="5aa89-149">Click Clear holds.</span></span>
    * <span data-ttu-id="5aa89-150">Blokování nyní bylo z objednávky vymazáno a odebráno ze seznamu aktivních blokací.</span><span class="sxs-lookup"><span data-stu-id="5aa89-150">The hold has now been cleared from the order and removed from the list of Active holds.</span></span> <span data-ttu-id="5aa89-151">Všechna blokování a jejich podmnožinu podle specifického stavu zobrazíte změnou hodnoty v poli Zobrazit.</span><span class="sxs-lookup"><span data-stu-id="5aa89-151">To see all the holds or their subset according to a specific status, change the value in the Show field.</span></span>     


