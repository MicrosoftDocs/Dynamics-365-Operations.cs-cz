---
title: Vytvoření záznamu deníku pomocí šablony
description: Zaúčtované deníky lze uložit jako šablony dokladů a použít v novém dokladu deníku.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransVoucherTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 234cfb98cc07f6c8c81821584e4e1d509d033477
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988567"
---
# <a name="create-a-journal-entry-using-template"></a><span data-ttu-id="53ca7-103">Vytvoření záznamu deníku pomocí šablony</span><span class="sxs-lookup"><span data-stu-id="53ca7-103">Create a journal entry using template</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="53ca7-104">Zaúčtované deníky lze uložit jako šablony dokladů a použít v novém dokladu deníku.</span><span class="sxs-lookup"><span data-stu-id="53ca7-104">Posted journal vouchers can be saved as Voucher templates and applied in a new journal voucher.</span></span> <span data-ttu-id="53ca7-105">Tato procedura používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="53ca7-105">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="53ca7-106">Přejděte na **Navigační podokno > Moduly > Hlavní kniha > Položky deníku > Hlavní deníky**.</span><span class="sxs-lookup"><span data-stu-id="53ca7-106">Go to **Navigation pane > Modules > General ledger > Journal entries > General journals**.</span></span>
2. <span data-ttu-id="53ca7-107">V **podokně akcí** klikněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="53ca7-107">On the **Action pane**, click **New**.</span></span> <span data-ttu-id="53ca7-108">Tento postup se spustí vytvořením a zaúčtováním dokladu deníku, ale ne všechny dříve zaúčtované doklady deníku lze uložit jako šablonu.</span><span class="sxs-lookup"><span data-stu-id="53ca7-108">This procedure starts by creating and posting a journal voucher, but any previously posted journal voucher can be saved as a template.</span></span>  
3. <span data-ttu-id="53ca7-109">V poli **Název** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="53ca7-109">In the **Name** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="53ca7-110">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="53ca7-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="53ca7-111">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="53ca7-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="53ca7-112">Klikněte na možnost **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="53ca7-112">Click **Lines**.</span></span>
7. <span data-ttu-id="53ca7-113">Zadejte hodnotu do pole **Typ účtu**.</span><span class="sxs-lookup"><span data-stu-id="53ca7-113">In the **Account type** field, type a value.</span></span>
8. <span data-ttu-id="53ca7-114">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="53ca7-114">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="53ca7-115">Zadejte hodnotu do pole **Má dáti**.</span><span class="sxs-lookup"><span data-stu-id="53ca7-115">In the **Debit** field, type a value.</span></span>
10. <span data-ttu-id="53ca7-116">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="53ca7-116">Click **New**.</span></span>
11. <span data-ttu-id="53ca7-117">Zadejte hodnotu do pole **Typ účtu**.</span><span class="sxs-lookup"><span data-stu-id="53ca7-117">In the **Account type** field, type a value.</span></span>
12. <span data-ttu-id="53ca7-118">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="53ca7-118">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="53ca7-119">Zadejte hodnotu do pole **Má dáti**.</span><span class="sxs-lookup"><span data-stu-id="53ca7-119">In the **Debit** field, type a value.</span></span>
14. <span data-ttu-id="53ca7-120">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="53ca7-120">Click **New**.</span></span>
14. <span data-ttu-id="53ca7-121">Zadejte požadované hodnoty do pole **Účet**.</span><span class="sxs-lookup"><span data-stu-id="53ca7-121">In the **Account** field, specify the desired values.</span></span>
15. <span data-ttu-id="53ca7-122">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="53ca7-122">In the **Description** field, type a value.</span></span>
16. <span data-ttu-id="53ca7-123">V poli **Dal** zadejte hodnotu pro vyrovnání dokladu.</span><span class="sxs-lookup"><span data-stu-id="53ca7-123">In the **Credit** field, type a value to balance the voucher.</span></span>
17. <span data-ttu-id="53ca7-124">V **podokně akcí** klikněte na **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="53ca7-124">On the **Action pane**, click **Post**.</span></span>
18. <span data-ttu-id="53ca7-125">Klikněte na **Funkce**.</span><span class="sxs-lookup"><span data-stu-id="53ca7-125">Click **Functions**.</span></span>
19. <span data-ttu-id="53ca7-126">Klikněte na šablonu **Uložit doklad**.</span><span class="sxs-lookup"><span data-stu-id="53ca7-126">Click **Save voucher** template.</span></span>
20. <span data-ttu-id="53ca7-127">Tento postup předpokládá, že je typ šablony **Procento**.</span><span class="sxs-lookup"><span data-stu-id="53ca7-127">This procedure assumes a **Percent Template** type.</span></span> <span data-ttu-id="53ca7-128">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="53ca7-128">Click OK.</span></span>
    - <span data-ttu-id="53ca7-129">Procento: částky v dokladu jsou převedeny na procentuální faktory, což umožní při výběru šablony dokladu použít jakoukoli částku.</span><span class="sxs-lookup"><span data-stu-id="53ca7-129">Percent: The amounts in the voucher are converted into percentage factors, which allows any amount to be applied when the Voucher template is selected.</span></span>
    - <span data-ttu-id="53ca7-130">Částka: skutečné částky, které budou uloženy a použity.</span><span class="sxs-lookup"><span data-stu-id="53ca7-130">Amount: The actual amounts will be stored and applied.</span></span>  
21. <span data-ttu-id="53ca7-131">Klikněte na **Hlavní deníky**.</span><span class="sxs-lookup"><span data-stu-id="53ca7-131">Click **General journals**.</span></span>
22. <span data-ttu-id="53ca7-132">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="53ca7-132">Click **New**.</span></span>
23. <span data-ttu-id="53ca7-133">V poli **Název** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="53ca7-133">In the **Name** field, click the drop-down button to open the lookup.</span></span>
24. <span data-ttu-id="53ca7-134">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="53ca7-134">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="53ca7-135">Klikněte na možnost **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="53ca7-135">Click **Lines**.</span></span>
26. <span data-ttu-id="53ca7-136">Klikněte na **Funkce**.</span><span class="sxs-lookup"><span data-stu-id="53ca7-136">Click **Functions**.</span></span>
27. <span data-ttu-id="53ca7-137">Klikněte na **Vybrat šablonu dokladu**.</span><span class="sxs-lookup"><span data-stu-id="53ca7-137">Click **Select voucher template**.</span></span>
28. <span data-ttu-id="53ca7-138">Vyberte šablonu, kterou jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="53ca7-138">Find the template that you created earlier.</span></span> <span data-ttu-id="53ca7-139">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="53ca7-139">Click **OK**.</span></span> <span data-ttu-id="53ca7-140">Může být nutné kliknout na **předchozí krok** a poté vybrat správnou šablonu, pokud existují další šablony.</span><span class="sxs-lookup"><span data-stu-id="53ca7-140">You may need to click **Previous step** and then select the correct template if other templates exist.</span></span>  
29. <span data-ttu-id="53ca7-141">V poli **Částka** zadejte částku, kterou chcete použít pro doklad.</span><span class="sxs-lookup"><span data-stu-id="53ca7-141">In the **Amount** field, enter the amount to be applied to the voucher.</span></span> <span data-ttu-id="53ca7-142">Pole **Částka** se zobrazí pouze pokud je typ šablony dokladu Procento.</span><span class="sxs-lookup"><span data-stu-id="53ca7-142">The **Amount** field is only displayed if the voucher template is of type Percent.</span></span>  
30. <span data-ttu-id="53ca7-143">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="53ca7-143">Click **OK**.</span></span>

