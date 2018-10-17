--- 
title: "Vytvoření záznamu deníku pomocí šablony"
description: "Zaúčtované deníky lze uložit jako šablony dokladů a použít v novém dokladu deníku."
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransVoucherTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 4a749740b62e39202d502a112f947679f85ca085
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-journal-entry-using-template"></a><span data-ttu-id="c732d-103">Vytvoření záznamu deníku pomocí šablony</span><span class="sxs-lookup"><span data-stu-id="c732d-103">Create a journal entry using template</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c732d-104">Zaúčtované deníky lze uložit jako šablony dokladů a použít v novém dokladu deníku.</span><span class="sxs-lookup"><span data-stu-id="c732d-104">Posted journal vouchers can be saved as Voucher templates and applied in a new journal voucher.</span></span> <span data-ttu-id="c732d-105">Tato procedura používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="c732d-105">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="c732d-106">Hlavní kniha > Položky deníku > Hlavní deníky.</span><span class="sxs-lookup"><span data-stu-id="c732d-106">General ledger > Journal entries > General journals.</span></span> <span data-ttu-id="c732d-107">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="c732d-107">Click New.</span></span>
    * <span data-ttu-id="c732d-108">Tento postup se spustí vytvořením a zaúčtováním dokladu deníku, ale ne všechny dříve zaúčtované doklady deníku lze uložit jako šablonu.</span><span class="sxs-lookup"><span data-stu-id="c732d-108">This procedure starts by creating and posting a journal voucher, but any previously posted journal voucher can be saved as a template.</span></span>  
2. <span data-ttu-id="c732d-109">V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="c732d-109">In the Name field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="c732d-110">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="c732d-110">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="c732d-111">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="c732d-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="c732d-112">Klikněte na možnost Řádky.</span><span class="sxs-lookup"><span data-stu-id="c732d-112">Click Lines.</span></span>
6. <span data-ttu-id="c732d-113">Zadejte účet pro typ účtu.</span><span class="sxs-lookup"><span data-stu-id="c732d-113">Enter an account for the Account type.</span></span>
7. <span data-ttu-id="c732d-114">Zadejte hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="c732d-114">In the Description field, type a value.</span></span>
8. <span data-ttu-id="c732d-115">Zadejte částku v poli Má dáti.</span><span class="sxs-lookup"><span data-stu-id="c732d-115">Enter an amount in the Debit field.</span></span>
9. <span data-ttu-id="c732d-116">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="c732d-116">Click New.</span></span>
10. <span data-ttu-id="c732d-117">Zadejte jiný účet pro typ účtu.</span><span class="sxs-lookup"><span data-stu-id="c732d-117">Enter a different account for the Account type.</span></span>
11. <span data-ttu-id="c732d-118">Zadejte hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="c732d-118">In the Description field, type a value.</span></span>
12. <span data-ttu-id="c732d-119">Zadejte částku v poli Má dáti.</span><span class="sxs-lookup"><span data-stu-id="c732d-119">Enter an amount in the Debit field.</span></span>
13. <span data-ttu-id="c732d-120">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="c732d-120">Click New.</span></span>
14. <span data-ttu-id="c732d-121">Zadejte požadované hodnoty do pole Účet.</span><span class="sxs-lookup"><span data-stu-id="c732d-121">In the Account field, specify the desired values.</span></span>
15. <span data-ttu-id="c732d-122">Zadejte hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="c732d-122">In the Description field, type a value.</span></span>
16. <span data-ttu-id="c732d-123">V poli Dobropis zadejte částku pro vyrovnání dokladu.</span><span class="sxs-lookup"><span data-stu-id="c732d-123">Enter an amount in the Credit field to balance the voucher.</span></span>
17. <span data-ttu-id="c732d-124">Klikněte na možnost Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="c732d-124">Click Post.</span></span>
18. <span data-ttu-id="c732d-125">Klepněte na možnost Funkce.</span><span class="sxs-lookup"><span data-stu-id="c732d-125">Click Functions.</span></span>
19. <span data-ttu-id="c732d-126">Klikněte na Uložit šablonu dokladu.</span><span class="sxs-lookup"><span data-stu-id="c732d-126">Click Save voucher template.</span></span>
20. <span data-ttu-id="c732d-127">Tento postup předpokládá, že je typ šablony Procento.</span><span class="sxs-lookup"><span data-stu-id="c732d-127">This procedure assumes a Percent Template type.</span></span> <span data-ttu-id="c732d-128">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c732d-128">Click OK.</span></span>
    * <span data-ttu-id="c732d-129">• Procento: částky v dokladu jsou převedeny na procentuální faktory, což umožní při výběru šablony dokladu použít jakoukoli částku.</span><span class="sxs-lookup"><span data-stu-id="c732d-129">• Percent: The amounts in the voucher are converted into percentage factors, which allows any amount to be applied when the Voucher template is selected.</span></span>  <span data-ttu-id="c732d-130">• Částka: skutečné částky, které budou uloženy a použity.</span><span class="sxs-lookup"><span data-stu-id="c732d-130">• Amount: The actual amounts will be stored and applied.</span></span>  
21. <span data-ttu-id="c732d-131">Klikněte na Hlavní deníky.</span><span class="sxs-lookup"><span data-stu-id="c732d-131">Click General journals.</span></span>
22. <span data-ttu-id="c732d-132">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="c732d-132">Click New.</span></span>
23. <span data-ttu-id="c732d-133">V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="c732d-133">In the Name field, click the drop-down button to open the lookup.</span></span>
24. <span data-ttu-id="c732d-134">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="c732d-134">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="c732d-135">Klikněte na možnost Řádky.</span><span class="sxs-lookup"><span data-stu-id="c732d-135">Click Lines.</span></span>
26. <span data-ttu-id="c732d-136">Klepněte na možnost Funkce.</span><span class="sxs-lookup"><span data-stu-id="c732d-136">Click Functions.</span></span>
27. <span data-ttu-id="c732d-137">Klikněte na Vybrat šablonu dokladu.</span><span class="sxs-lookup"><span data-stu-id="c732d-137">Click Select voucher template.</span></span>
28. <span data-ttu-id="c732d-138">Vyberte šablonu, kterou jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="c732d-138">Find the template that you created earlier.</span></span> <span data-ttu-id="c732d-139">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c732d-139">Click OK.</span></span>
    * <span data-ttu-id="c732d-140">Může být nutné kliknout na předchozí krok a poté vybrat správnou šablonu, pokud existují další šablony.</span><span class="sxs-lookup"><span data-stu-id="c732d-140">You may need to click Previous step and then select the correct template if other templates exist.</span></span>  
29. <span data-ttu-id="c732d-141">V poli Částka zadejte částku, kterou chcete použít pro doklad.</span><span class="sxs-lookup"><span data-stu-id="c732d-141">In the Amount field, enter the amount to be applied to the voucher.</span></span>
    * <span data-ttu-id="c732d-142">Pole Částka se zobrazí pouze pokud je typ šablony dokladu Procento.</span><span class="sxs-lookup"><span data-stu-id="c732d-142">The amount field is only displayed if the voucher template is of type Percent.</span></span>  
30. <span data-ttu-id="c732d-143">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c732d-143">Click OK.</span></span>


