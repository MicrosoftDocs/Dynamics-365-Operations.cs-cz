--- 
title: "Vytvoření posloupnosti upomínek"
description: "Tento průvodce úkolem slouží k vytvoření posloupnosti upomínek."
author: mikefalkner
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6331c3680169b305c4bfbfada4ba106b619be092
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-collection-letter-sequence"></a><span data-ttu-id="cee93-103">Vytvoření posloupnosti upomínek</span><span class="sxs-lookup"><span data-stu-id="cee93-103">Create a collection letter sequence</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cee93-104">Tento průvodce úkolem slouží k vytvoření posloupnosti upomínek.</span><span class="sxs-lookup"><span data-stu-id="cee93-104">Use this task guide to create a collection letter sequence.</span></span> <span data-ttu-id="cee93-105">Tento úkol používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="cee93-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="cee93-106">Přejděte na Úvěry a inkasa > Nastavení > Nastavit pořadí upomínek.</span><span class="sxs-lookup"><span data-stu-id="cee93-106">Go to Credit and collections > Setup > Set up collection letter sequence.</span></span>
2. <span data-ttu-id="cee93-107">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="cee93-107">Click New.</span></span>
3. <span data-ttu-id="cee93-108">V poli Posloupnost upomínek zadejte ID posloupnosti, které bude představovat číselnou řadu.</span><span class="sxs-lookup"><span data-stu-id="cee93-108">In the Collection letter sequence field, enter a sequence ID that will represent the sequence.</span></span> <span data-ttu-id="cee93-109">Použije se při nastavování profilu zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="cee93-109">It will be used when you set up a posting profile.</span></span>
4. <span data-ttu-id="cee93-110">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="cee93-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="cee93-111">Platební podmínky jsou volitelné.</span><span class="sxs-lookup"><span data-stu-id="cee93-111">The terms of payment is optional.</span></span> <span data-ttu-id="cee93-112">Pokud zde zadáte hodnotu, faktura upomínky na poplatek bude používat platební podmínky namísto podmínek platby, které jsou uloženy pro odběratele.</span><span class="sxs-lookup"><span data-stu-id="cee93-112">If you enter a value here, the collection letter fee invoice will use these terms of payment instead of the terms of payment stored with the customer.</span></span>  
5. <span data-ttu-id="cee93-113">V poli s kódem kolekce upomínky vyberte kód pro první upomínku, kterou chcete odeslat.</span><span class="sxs-lookup"><span data-stu-id="cee93-113">In the collection letter code field, select the code for the first collection letter that you want to send.</span></span>
    * <span data-ttu-id="cee93-114">První upomínka se vytvoří podle data splatnosti na faktuře, hodnoty zadané pro období odkladu v poli Dny na tomto řádku a dalších informací, které zadáte do tohoto řádku.</span><span class="sxs-lookup"><span data-stu-id="cee93-114">The first collection letter is created according to the due date on the invoice, the value that you enter for the grace period in the Days field on this line, and other information that you enter on this line.</span></span>  
6. <span data-ttu-id="cee93-115">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="cee93-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="cee93-116">Měna poplatku je výchozí měnou odběratele.</span><span class="sxs-lookup"><span data-stu-id="cee93-116">The currency for the fee defaults to the customer currency.</span></span> <span data-ttu-id="cee93-117">Kód měny může být jiný, než jaká je měna faktury.</span><span class="sxs-lookup"><span data-stu-id="cee93-117">This currency code can be different than the invoice currency.</span></span>  
7. <span data-ttu-id="cee93-118">Kliknutím na tlačítko Přidat přidejte následující upomínku, která se odešle v řadě</span><span class="sxs-lookup"><span data-stu-id="cee93-118">Click Add to add the next collection letter that will be sent in the sequence</span></span>
    * <span data-ttu-id="cee93-119">V mnoha případech první upomínka je pouze upozornění.</span><span class="sxs-lookup"><span data-stu-id="cee93-119">In many cases, the first collection letter is just a warning.</span></span> <span data-ttu-id="cee93-120">V případě potřeby můžete přidat poplatky.</span><span class="sxs-lookup"><span data-stu-id="cee93-120">You can add fees if needed.</span></span>  
8. <span data-ttu-id="cee93-121">V poli s kódem kolekce upomínky vyberte další upomínku, kterou chcete odeslat v posloupnosti.</span><span class="sxs-lookup"><span data-stu-id="cee93-121">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
9. <span data-ttu-id="cee93-122">Zadejte hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="cee93-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="cee93-123">V poli hlavního účtu vyberte účet výnosů, který bude použit pro poplatky.</span><span class="sxs-lookup"><span data-stu-id="cee93-123">In the main account field, select the revenue account that will be used for fees.</span></span>
11. <span data-ttu-id="cee93-124">Zadejte poplatek, který bude účtován po zaúčtování této upomínky.</span><span class="sxs-lookup"><span data-stu-id="cee93-124">Enter the fee that will be charged when this collection letter is posted.</span></span>
12. <span data-ttu-id="cee93-125">V poli Skupina DPH zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="cee93-125">In the Item sales tax group field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="cee93-126">Vyberte skupinu DPH položky, pokud DPH musí být vypočítáno u poplatku.</span><span class="sxs-lookup"><span data-stu-id="cee93-126">Select an item sales tax group if sales taxes must be calculated on the fee.</span></span>  
13. <span data-ttu-id="cee93-127">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="cee93-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="cee93-128">Zadejte minimální zůstatek po datu splatnosti požadovaný před odesláním upomínky.</span><span class="sxs-lookup"><span data-stu-id="cee93-128">Enter the minimum overdue balance required before a collection letter is sent.</span></span>
15. <span data-ttu-id="cee93-129">Zadejte počet dnů odkladu, které povolíte.</span><span class="sxs-lookup"><span data-stu-id="cee93-129">Enter the number of grace days that you will allow.</span></span>
    * <span data-ttu-id="cee93-130">Toto je počet dnů po datu splatnosti, ve které mohou být generovány upomínky.</span><span class="sxs-lookup"><span data-stu-id="cee93-130">This is the number of days after the due date that a collection letter can be generated.</span></span> <span data-ttu-id="cee93-131">Datum splatnosti použité pro výpočet závisí na pozici upomínky v posloupnosti upomínek:   ⦁   Období odkladu pro upomínku 1 je relativní k datu splatnosti faktury.</span><span class="sxs-lookup"><span data-stu-id="cee93-131">The due date that is used for the calculation depends on the position of the collection letter in the collection letter sequence:   ⦁    The grace period for collection letter 1 is relative to the due date on the invoice.</span></span>  <span data-ttu-id="cee93-132">⦁ Období odkladu pro upomínky 2 a výše vychází z data zaúčtování nebo tisku upomínky, v závislosti na výběru v poli Aktualizovat kód upomínky na stránce Parametry pohledávek.</span><span class="sxs-lookup"><span data-stu-id="cee93-132">⦁ The grace period for collection letters 2 and higher is relative to the date that the previous collection letter is posted or printed, depending on the selection in the Update collection letter code field in the Accounts receivable parameters page.</span></span>  
16. <span data-ttu-id="cee93-133">Kliknutím na tlačítko Přidat přidejte poslední upomínku v řadě.</span><span class="sxs-lookup"><span data-stu-id="cee93-133">Click Add to add the last collection letter in the sequence.</span></span>
    * <span data-ttu-id="cee93-134">Pro posloupnost upomínek můžete přidat až pět kódů upomínek.</span><span class="sxs-lookup"><span data-stu-id="cee93-134">You can add up to five collection letter codes for a collection letter sequence.</span></span>  
17. <span data-ttu-id="cee93-135">V poli s kódem kolekce upomínky vyberte další upomínku, kterou chcete odeslat v posloupnosti.</span><span class="sxs-lookup"><span data-stu-id="cee93-135">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
18. <span data-ttu-id="cee93-136">Zadejte hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="cee93-136">In the Description field, type a value.</span></span>
19. <span data-ttu-id="cee93-137">Zadejte požadované hodnoty do pole Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="cee93-137">In the Main account field, specify the desired values.</span></span>
20. <span data-ttu-id="cee93-138">Zadejte číslo do pole Poplatek v měně.</span><span class="sxs-lookup"><span data-stu-id="cee93-138">In the Fee in currency field, enter a number.</span></span>
21. <span data-ttu-id="cee93-139">V poli Skupina DPH zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="cee93-139">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="cee93-140">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="cee93-140">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="cee93-141">V poli Minimální zůstatek po datu splatnosti zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="cee93-141">In the Minimum overdue balance field, enter a number.</span></span>
24. <span data-ttu-id="cee93-142">Zadejte číslo do pole Dny.</span><span class="sxs-lookup"><span data-stu-id="cee93-142">In the Days field, enter a number.</span></span>
25. <span data-ttu-id="cee93-143">Zaškrtnutím tohoto políčka se zablokují další dodávky a fakturace pro odběratele.</span><span class="sxs-lookup"><span data-stu-id="cee93-143">Select this check box to stop the customer from additional deliveries and invoicing.</span></span>
    * <span data-ttu-id="cee93-144">Pro odblokování účtu vyberte možnost Ne v poli Fakturace a dodávka na stránce Odběratelé.</span><span class="sxs-lookup"><span data-stu-id="cee93-144">To unblock the account, select No in the Invoicing and delivery on hold field in the Customers page.</span></span>  
26. <span data-ttu-id="cee93-145">Rozbalte pevnou záložku Poznámka.</span><span class="sxs-lookup"><span data-stu-id="cee93-145">Expand the Note fasttab.</span></span>
27. <span data-ttu-id="cee93-146">Zadejte text, který se má zobrazit v upomínce pro vybraný kód upomínky.</span><span class="sxs-lookup"><span data-stu-id="cee93-146">Enter the text to appear on the collection letter for the selected collection letter code.</span></span>
    * <span data-ttu-id="cee93-147">Tento text lze přeložit do několika jazyků pomocí nabídky Překlady nad polem.</span><span class="sxs-lookup"><span data-stu-id="cee93-147">You can translate this text in to multiple languages using the Translations menu above the note box.</span></span>  


