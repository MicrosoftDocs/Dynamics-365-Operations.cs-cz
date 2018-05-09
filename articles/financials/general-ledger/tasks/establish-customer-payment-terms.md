--- 
title: "Stanovení platebních podmínek odběratele"
description: "Tento postup definuje platební slevu a nastavení data splatnosti."
author: aprilolson
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3183b00cf2ff4d882399d3f44ca8046e50eda507
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---
# <a name="establish-customer-payment-terms"></a><span data-ttu-id="b2612-103">Stanovení platebních podmínek odběratele</span><span class="sxs-lookup"><span data-stu-id="b2612-103">Establish customer payment terms</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b2612-104">Tento postup definuje platební slevu a nastavení data splatnosti.</span><span class="sxs-lookup"><span data-stu-id="b2612-104">This procedure defines a cash discount and due date setup.</span></span> <span data-ttu-id="b2612-105">Tento průvodce úlohou používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="b2612-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="b2612-106">Přejděte do nabídky Pohledávky > Nastavení platby > Dny platby.</span><span class="sxs-lookup"><span data-stu-id="b2612-106">Go to Accounts receivable > Payments setup > Payment days.</span></span>
    * <span data-ttu-id="b2612-107">Nastavení platebních podmínek je sdíleno pro pohledávky a závazky.</span><span class="sxs-lookup"><span data-stu-id="b2612-107">The setup for the Terms of payment is shared for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="b2612-108">Pokud je definujete v jednom modulu, bude k dispozici i ve druhém modulu.</span><span class="sxs-lookup"><span data-stu-id="b2612-108">If you define it in module, it will be available in the other module also.</span></span> <span data-ttu-id="b2612-109">Pro tohoto průvodce úkolem jsou nastaveny všechny podmínky platby v části Pohledávky.</span><span class="sxs-lookup"><span data-stu-id="b2612-109">For this task guide, I set up all the terms of payment under Accounts receivable.</span></span>  
2. <span data-ttu-id="b2612-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b2612-110">Click New.</span></span>
    * <span data-ttu-id="b2612-111">Vytvořte den platby, pokud vaše platební podmínky vyžadují určitý den v týdnu (pondělí, úterý atd.) nebo určité datum v měsíci (5., 10. atd.).</span><span class="sxs-lookup"><span data-stu-id="b2612-111">Create a payment day if your terms of payment require a specific day of the week (Monday, Tuesday, etc) or a specific date of the month (5th, 10th, etc).</span></span>  
3. <span data-ttu-id="b2612-112">V poli Den platby zadejte ID dne platby do pole se dnem platby.</span><span class="sxs-lookup"><span data-stu-id="b2612-112">In the Payment day field, enter an ID for the Payment day in the payment day field.</span></span>
4. <span data-ttu-id="b2612-113">Do pole Popis zadejte popis dne platby.</span><span class="sxs-lookup"><span data-stu-id="b2612-113">In the Description field, enter a description of the payment day.</span></span>
5. <span data-ttu-id="b2612-114">V poli Týden/Měsíc vyberte týden nebo měsíc.</span><span class="sxs-lookup"><span data-stu-id="b2612-114">In the Week/Month field, select either Week or Month.</span></span>
    * <span data-ttu-id="b2612-115">Pokud chcete zadat den v týdnu, jako je pondělí, vyberte Týden.</span><span class="sxs-lookup"><span data-stu-id="b2612-115">If you want to enter a day of the week, such as Monday, select Week.</span></span> <span data-ttu-id="b2612-116">Pokud chcete zadat datum v měsíci, jako například 10., vyberte Měsíc.</span><span class="sxs-lookup"><span data-stu-id="b2612-116">If you want to enter a date in the month, such as the 10th, select Month.</span></span> <span data-ttu-id="b2612-117">V tomto příkladu vyberte možnost Měsíc.</span><span class="sxs-lookup"><span data-stu-id="b2612-117">Select Month for this example.</span></span>  
6. <span data-ttu-id="b2612-118">Do pole Den v měsíci zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="b2612-118">In the Day of month field, enter a date.</span></span>
    * <span data-ttu-id="b2612-119">Datum by mělo být zadáno jako číslo, jako například „10“ a nikoli „10.“.</span><span class="sxs-lookup"><span data-stu-id="b2612-119">The date should be entered as a number, such as '10', and not as '10th'.</span></span>  
7. <span data-ttu-id="b2612-120">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b2612-120">Click Save.</span></span>
8. <span data-ttu-id="b2612-121">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b2612-121">Close the page.</span></span>
9. <span data-ttu-id="b2612-122">Přejděte do nabídky Pohledávky > Nastavení platby > Platební podmínky.</span><span class="sxs-lookup"><span data-stu-id="b2612-122">Go to Accounts receivable > Payments setup > Terms of payment.</span></span>
10. <span data-ttu-id="b2612-123">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b2612-123">Click New.</span></span>
    * <span data-ttu-id="b2612-124">Podmínky platby lze použít pro definování způsobu výpočtu dat splatnosti.</span><span class="sxs-lookup"><span data-stu-id="b2612-124">Terms of payment is used to define how the due dates will be calculated.</span></span> <span data-ttu-id="b2612-125">Nastavení data platební slevy je definováno na samostatné stránce.</span><span class="sxs-lookup"><span data-stu-id="b2612-125">The cash discount date setup is defined in a separate page.</span></span>  
11. <span data-ttu-id="b2612-126">V poli Platební podmínky zadejte ID do pole Platební podmínky.</span><span class="sxs-lookup"><span data-stu-id="b2612-126">In the Terms of payment field, enter an ID in the Terms of payment field.</span></span>
12. <span data-ttu-id="b2612-127">Zadejte popis do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="b2612-127">In the Description field, enter a description.</span></span>
13. <span data-ttu-id="b2612-128">Vyberte způsob platby, jako například platbu na dobírku, netto, aktuální měsíc atd.</span><span class="sxs-lookup"><span data-stu-id="b2612-128">Select a Payment method such as COD, Net, Current month, etc.</span></span>
    * <span data-ttu-id="b2612-129">Způsob platby lze použít pro definování začátku způsobu výpočtu data splatnosti.</span><span class="sxs-lookup"><span data-stu-id="b2612-129">The Payment method is used to define the start of how the due will be calculated.</span></span>  <span data-ttu-id="b2612-130">Například Netto se používá v případě, že datum splatnosti bude vždy pevný počet měsíců nebo dnů po datu faktury.</span><span class="sxs-lookup"><span data-stu-id="b2612-130">For example, Net is used if the due date is always a set number of months or days after the invoice date.</span></span> <span data-ttu-id="b2612-131">Platbu na dobírku lze použít v případě, že platba je požadována při fakturaci, takže neproběhne výpočet data splatnosti.</span><span class="sxs-lookup"><span data-stu-id="b2612-131">COD can be used to when payment is required upon invoice, so a due date wouldn't be calculated.</span></span> <span data-ttu-id="b2612-132">Pro tohoto průvodce úkolem vyberte Aktuální měsíc.</span><span class="sxs-lookup"><span data-stu-id="b2612-132">Select Current month for this task guide.</span></span>  
14. <span data-ttu-id="b2612-133">Zvolte Den platby, jsou-li určitý den týdne nebo datum zahrnuty do výpočtu.</span><span class="sxs-lookup"><span data-stu-id="b2612-133">Select a Payment day if a specific day of the  week or date are included in the calculation.</span></span>
    * <span data-ttu-id="b2612-134">V závislosti na vašich platebních podmínkách můžete zadat množství do pole Měsíce a Dny Nebo můžete použít pole Platební kalendář nebo Platební den a přidat je na konec metody platby.</span><span class="sxs-lookup"><span data-stu-id="b2612-134">Depending on your terms of payment, you may enter a quantity in Months or Days.</span></span> <span data-ttu-id="b2612-135">Pokud datum splatnosti bude vždy 10.</span><span class="sxs-lookup"><span data-stu-id="b2612-135">Or you can use the Payment schedule or Payment day to 'add' to the end of the Payment method.</span></span> <span data-ttu-id="b2612-136">den dalšího měsíce, vyberte v poli Platební den hodnotu „10“.</span><span class="sxs-lookup"><span data-stu-id="b2612-136">If the due date will always be the 10th of the next month, select a Payment day of the 10th.</span></span>  
15. <span data-ttu-id="b2612-137">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b2612-137">Click Save.</span></span>
16. <span data-ttu-id="b2612-138">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b2612-138">Close the page.</span></span>
17. <span data-ttu-id="b2612-139">Přejděte do nabídky Pohledávky > Nastavení plateb > Platební slevy.</span><span class="sxs-lookup"><span data-stu-id="b2612-139">Go to Accounts receivable > Payments setup > Cash discounts.</span></span>
18. <span data-ttu-id="b2612-140">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b2612-140">Click New.</span></span>
    * <span data-ttu-id="b2612-141">Tato stránka se nepoužívá při definování způsobu výpočtu data platební slevy.</span><span class="sxs-lookup"><span data-stu-id="b2612-141">This page is used to define how the cash discount date will be calculated.</span></span>  
19. <span data-ttu-id="b2612-142">V poli Platební sleva zadejte ID do pole Platební sleva.</span><span class="sxs-lookup"><span data-stu-id="b2612-142">In the Cash discount field, enter an ID in the Cash discount field.</span></span>
20. <span data-ttu-id="b2612-143">Zadejte popis do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="b2612-143">In the Description field, enter a description.</span></span>
21. <span data-ttu-id="b2612-144">Pokud jsou k dispozici vrstvené platební slevy, vyberte Další kód slevy, který následuje za touto novou platební slevou.</span><span class="sxs-lookup"><span data-stu-id="b2612-144">If a tiered cash discount is available, select the Next discount code that is relevant after this new cash discount.</span></span>
22. <span data-ttu-id="b2612-145">Zadejte počet dní, které se používají k výpočtu data platební slevy.</span><span class="sxs-lookup"><span data-stu-id="b2612-145">Enter the number of days used to calculate the cash discount date.</span></span>
    * <span data-ttu-id="b2612-146">Pokud byla vybrána možnost Pravidlo Netto, počet dnů bude přidán k datu faktury pro výpočet data platební slevy.</span><span class="sxs-lookup"><span data-stu-id="b2612-146">If Net principle is selected, the number of days will be added to the invoice date to calculate the cash discount date.</span></span>  
23. <span data-ttu-id="b2612-147">Zadejte procentuální hodnotu platební slevy.</span><span class="sxs-lookup"><span data-stu-id="b2612-147">Enter the percentage of the cash discount.</span></span>
24. <span data-ttu-id="b2612-148">Zadejte hlavního účtu, ke kterému bude platební sleva zaúčtována pro faktury odběratele.</span><span class="sxs-lookup"><span data-stu-id="b2612-148">Enter the main account to which the cash discount will post for customer invoices.</span></span>
25. <span data-ttu-id="b2612-149">V poli Slevové protiúčty vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="b2612-149">In the Discount offset accounts field, select an option.</span></span>
    * <span data-ttu-id="b2612-150">Pokud vyberete možnost Účty na řádcích faktury, platební sleva se zaúčtuje do stejného hlavního účtu majetku / nákladů na řádky faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="b2612-150">If you select 'Accounts on the invoice lines', the cash discount will post to the same asset/expense main account on the lines of the vendor invoice.</span></span> <span data-ttu-id="b2612-151">Použít vyberete možnost Použít hlavní účet pro faktury dodavatele, platební slevy se zaúčtují do hlavního účtu, který definujete v části Hlavní účet pro faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="b2612-151">If you select 'Use main account for vendor invoices', the cash discount will post to the main account you define in the 'Main account for vendor invoices'.</span></span> <span data-ttu-id="b2612-152">V tomto příkladu vyberte možnost Použít hlavní účet pro faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="b2612-152">For this example, select 'Use main account for vendor invoices.'</span></span>  
26. <span data-ttu-id="b2612-153">Zadejte hlavního účtu, ke kterému bude platební sleva zaúčtována pro faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="b2612-153">Enter the main account to which the cash discount will post for vendor invoices.</span></span>
27. <span data-ttu-id="b2612-154">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b2612-154">Click Save.</span></span>


