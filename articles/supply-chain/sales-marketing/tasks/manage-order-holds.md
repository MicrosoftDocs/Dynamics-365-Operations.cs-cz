---
title: Správa blokování objednávek
description: Tento postup ukazuje, jak blokovat prodejní objednávky odběratele, jak pracovat s rezervacemi blokovaných objednávek a jak odebrat blokování objednávky.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans, MCRHoldCheckOutOverride, MCRHoldCodeTable, MCRItemListCopying, MCRItemListTable, MCROMHoldList
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27a5149812a8e478dae1d2385e6c139c9f635202
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010740"
---
# <a name="manage-order-holds"></a><span data-ttu-id="d9e75-103">Správa blokování objednávek</span><span class="sxs-lookup"><span data-stu-id="d9e75-103">Manage order holds</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d9e75-104">Tento postup ukazuje, jak blokovat prodejní objednávky odběratele, jak pracovat s rezervacemi blokovaných objednávek a jak odebrat blokování objednávky.</span><span class="sxs-lookup"><span data-stu-id="d9e75-104">This procedure demonstrates how to place customer sales orders on hold, how to work with order hold checkouts, and how to remove order holds.</span></span> <span data-ttu-id="d9e75-105">Objednávka může být blokována z mnoha důvodů.</span><span class="sxs-lookup"><span data-stu-id="d9e75-105">An order might be placed on hold for a variety of reasons.</span></span> <span data-ttu-id="d9e75-106">Můžete například blokovat objednávku, dokud není ověřena adresa odběratele nebo platební metoda nebo dokud správce nezkontroluje úvěrový limit odběratele.</span><span class="sxs-lookup"><span data-stu-id="d9e75-106">For example, you might hold an order until a customer address or payment method can be verified or until a manager can review the customer's credit limit.</span></span> <span data-ttu-id="d9e75-107">Když je objednávka blokována, nelze ji zpracovat skladem pro expedici.</span><span class="sxs-lookup"><span data-stu-id="d9e75-107">While the order on hold, it cannot be processed by the warehouse for shipping.</span></span> 

<span data-ttu-id="d9e75-108">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="d9e75-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-order-holds"></a><span data-ttu-id="d9e75-109">Nastavení blokování objednávky</span><span class="sxs-lookup"><span data-stu-id="d9e75-109">Set up order holds</span></span>
1. <span data-ttu-id="d9e75-110">Přejděte na **Navigační podokno > Moduly > Prodej a marketing > Nastavení > Prodejní objednávky > Kódy blokování objednávky**.</span><span class="sxs-lookup"><span data-stu-id="d9e75-110">Go to **Navigation pane > Modules > Sales and marketing > Setup > Sales orders > Order hold codes**.</span></span>
2. <span data-ttu-id="d9e75-111">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d9e75-111">Click **New**.</span></span>
3. <span data-ttu-id="d9e75-112">V poli **Kód blokování** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d9e75-112">In the **Hold code** field, type a value.</span></span> <span data-ttu-id="d9e75-113">Zadejte například Zpětné volání.</span><span class="sxs-lookup"><span data-stu-id="d9e75-113">For example, type 'Call back'.</span></span>  
4. <span data-ttu-id="d9e75-114">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="d9e75-114">In the **Description** field, type a value.</span></span>
    - <span data-ttu-id="d9e75-115">Například blokovaná objednávka čekající na zpětné volání odběratele.</span><span class="sxs-lookup"><span data-stu-id="d9e75-115">For example, Order held waiting for customer callback.</span></span>  
    - <span data-ttu-id="d9e75-116">Volitelně zaškrtněte políčko **Odebrat rezervace**, abyste odstranili všechny fyzické rezervace z objednávky, když je přidán kód blokování.</span><span class="sxs-lookup"><span data-stu-id="d9e75-116">Optionally, select the **Remove reservations** check box to remove any physical reservations from the order when this hold code is added.</span></span>  
5. <span data-ttu-id="d9e75-117">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d9e75-117">Click **Save**.</span></span>

## <a name="place-order-on-hold"></a><span data-ttu-id="d9e75-118">Zablokování objednávky</span><span class="sxs-lookup"><span data-stu-id="d9e75-118">Place order on hold</span></span>
1. <span data-ttu-id="d9e75-119">Přejděte na **Navigační podokno > Moduly > Prodej a marketing > Prodejní objednávky > Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="d9e75-119">Go to **Navigation pane > Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="d9e75-120">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d9e75-120">Click **New**.</span></span>
3. <span data-ttu-id="d9e75-121">V poli **Účet odběratele** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d9e75-121">In the **Customer account** field, enter or select a value.</span></span>
4. <span data-ttu-id="d9e75-122">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="d9e75-122">Click **OK**.</span></span>
5. <span data-ttu-id="d9e75-123">V poli **Číslo položky** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d9e75-123">In the **Item number** field, enter or select a value.</span></span>
6. <span data-ttu-id="d9e75-124">Zadejte číslo do pole **Množství**.</span><span class="sxs-lookup"><span data-stu-id="d9e75-124">In the **Quantity** field, enter a number.</span></span>
7. <span data-ttu-id="d9e75-125">V **podokně akcí** klikněte na možnost **Prodejní objednávka**.</span><span class="sxs-lookup"><span data-stu-id="d9e75-125">On the **Action Pane**, click **Sales order**.</span></span>
8. <span data-ttu-id="d9e75-126">Klikněte na **Blokování objednávky**.</span><span class="sxs-lookup"><span data-stu-id="d9e75-126">Click **Order holds**.</span></span>
9. <span data-ttu-id="d9e75-127">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d9e75-127">Click **New**.</span></span>
10. <span data-ttu-id="d9e75-128">V poli **Kód blokování** vyberte kód, který jste vytvořili v předchozím dílčím úkolu.</span><span class="sxs-lookup"><span data-stu-id="d9e75-128">In the **Hold code** field, select the code you have created in the previous subtask.</span></span>
11. <span data-ttu-id="d9e75-129">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d9e75-129">Click **Save**.</span></span>
12. <span data-ttu-id="d9e75-130">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d9e75-130">Close the page.</span></span>
13. <span data-ttu-id="d9e75-131">Přejděte na **Prodej a marketing > Prodejní objednávky > Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="d9e75-131">Go to **Sales and marketing > Sales orders > All sales orders**.</span></span>
14. <span data-ttu-id="d9e75-132">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="d9e75-132">In the list, mark the selected row.</span></span> <span data-ttu-id="d9e75-133">Objednávky, které jsou aktuálně blokovány, mají označena pole „Nezpracovávat a „Blokace“.</span><span class="sxs-lookup"><span data-stu-id="d9e75-133">Orders that are currently on hold have the "Do not process" and "Hold" fields marked.</span></span>
15. <span data-ttu-id="d9e75-134">V podokně akcí klikněte na tlačítko **Vyskladnit a zabalit**.</span><span class="sxs-lookup"><span data-stu-id="d9e75-134">On the Action Pane, click **Pick and pack**.</span></span>

## <a name="manage-order-holds"></a><span data-ttu-id="d9e75-135">Správa blokování objednávek</span><span class="sxs-lookup"><span data-stu-id="d9e75-135">Manage order holds</span></span>
1. <span data-ttu-id="d9e75-136">Přejděte na **Prodej a marketing > Prodejní objednávky > Otevřené objednávky > Blokování objednávky**.</span><span class="sxs-lookup"><span data-stu-id="d9e75-136">Go to **Sales and marketing > Sales orders > Open orders > Order holds**.</span></span> <span data-ttu-id="d9e75-137">Stránka s **blokovanými objednávkami** funguje jako pracovní plocha, kde můžete získat přehled všech aktuálních a zpracovaných blokování, se kterými zde můžete pracovat, a přidružených prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="d9e75-137">**Order holds** page functions as a workbench where you can get an overview of all the current and processed holds, and handle them and associated sales orders.</span></span>     
2. <span data-ttu-id="d9e75-138">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="d9e75-138">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="d9e75-139">V **podokně akcí** klikněte na **Rezervace blokování**.</span><span class="sxs-lookup"><span data-stu-id="d9e75-139">On the **Action Pane**, click **Hold checkout**.</span></span>
4. <span data-ttu-id="d9e75-140">Klikněte na možnost **Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="d9e75-140">Click **Check out**.</span></span>
5. <span data-ttu-id="d9e75-141">Odznačte vybraný řádek na seznamu.</span><span class="sxs-lookup"><span data-stu-id="d9e75-141">In the list, unmark the selected row.</span></span> <span data-ttu-id="d9e75-142">Pole **Rezervovat komu** nyní zobrazuje vaše uživatelské ID.</span><span class="sxs-lookup"><span data-stu-id="d9e75-142">The **Checkout out to** field now shows your user ID.</span></span>   
6. <span data-ttu-id="d9e75-143">Klikněte na možnost **Vymazat rezervaci**.</span><span class="sxs-lookup"><span data-stu-id="d9e75-143">Click **Clear checkout**.</span></span>
7. <span data-ttu-id="d9e75-144">V **podokně akcí** klikněte na možnost **Vymazat blokování**.</span><span class="sxs-lookup"><span data-stu-id="d9e75-144">On the **Action Pane**, click **Clear hold**.</span></span>
    - <span data-ttu-id="d9e75-145">Když jste připraveni odebrat blokování a umožnit objednávce, aby pokračovala k dalšímu kroku plnění, musíte blokování vymazat.</span><span class="sxs-lookup"><span data-stu-id="d9e75-145">When you are ready to remove the hold and allow the order to proceed to the next fulfilment step, you must clear the hold.</span></span> <span data-ttu-id="d9e75-146">Nevyžaduje-li objednávka žádné změny, můžete spustit akci Vymazat blokování.</span><span class="sxs-lookup"><span data-stu-id="d9e75-146">If the order requires no changes, you can run the Clear holds action.</span></span> <span data-ttu-id="d9e75-147">Můžete však použít akci Vymazat a upravit, pokud je třeba při vymazání blokování objednávku aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="d9e75-147">However, you can use the Clear and modify action if, when clearing a hold, the order has to be updated.</span></span>      
    - <span data-ttu-id="d9e75-148">Akce **Vymazat a odeslat** je použitelná pouze při použití funkce kontaktního střediska.</span><span class="sxs-lookup"><span data-stu-id="d9e75-148">The **Clear and submit** action is only applicable when you use Call center functionality.</span></span>  
8. <span data-ttu-id="d9e75-149">Klikněte na možnost **Vymazat blokování**.</span><span class="sxs-lookup"><span data-stu-id="d9e75-149">Click **Clear holds**.</span></span> <span data-ttu-id="d9e75-150">Blokování nyní bylo z objednávky vymazáno a odebráno ze seznamu aktivních blokací.</span><span class="sxs-lookup"><span data-stu-id="d9e75-150">The hold has now been cleared from the order and removed from the list of Active holds.</span></span> <span data-ttu-id="d9e75-151">Všechna blokování a jejich podmnožinu podle specifického stavu zobrazíte změnou hodnoty v poli Zobrazit.</span><span class="sxs-lookup"><span data-stu-id="d9e75-151">To see all the holds or their subset according to a specific status, change the value in the Show field.</span></span>     

