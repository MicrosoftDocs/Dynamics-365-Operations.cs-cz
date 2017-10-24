--- 
title: "Nastavit období vyrovnání DPH"
description: "Období vyrovnání DPH obsahuje informace o intervalech období, pro které se musí DPH vykazovat a platit."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: ab7d3a00a327f42a9f70c954d9b64a360a7f9163
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="29939-103">Nastavit období vyrovnání DPH</span><span class="sxs-lookup"><span data-stu-id="29939-103">Set up sales tax settlement periods</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="29939-104">Období vyrovnání DPH obsahuje informace o intervalech období, pro které se musí DPH vykazovat a platit.</span><span class="sxs-lookup"><span data-stu-id="29939-104">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="29939-105">Proces vyrovnání lze spustit pro období vyrovnání pro specifický časový interval.</span><span class="sxs-lookup"><span data-stu-id="29939-105">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="29939-106">Všechny kódy daně, které jsou spojené s obdobím vyrovnání, budou vyrovnány.</span><span class="sxs-lookup"><span data-stu-id="29939-106">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="29939-107">V závislosti na nastavení souvisejícího finančního úřadu je daňová povinnost zaúčtována pro dodavatele nebo na účet hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="29939-107">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>



<span data-ttu-id="29939-108">Tento úkol používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="29939-108">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="29939-109">Přejděte na Daň > Nepřímé daně > DPH > Období vyrovnání DPH.</span><span class="sxs-lookup"><span data-stu-id="29939-109">Go to Tax > Indirect taxes > Sales tax > Sales tax settlement periods.</span></span>
2. <span data-ttu-id="29939-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="29939-110">Click New.</span></span>
3. <span data-ttu-id="29939-111">Zadejte hodnotu do pole Období vyrovnání.</span><span class="sxs-lookup"><span data-stu-id="29939-111">In the Settlement period field, type a value.</span></span>
4. <span data-ttu-id="29939-112">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="29939-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="29939-113">V poli Úřad vyberte finanční úřad, který přijímá sestavy a platby, které byly vytvořeny pro období vyrovnání.</span><span class="sxs-lookup"><span data-stu-id="29939-113">In the Authority field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="29939-114">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="29939-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="29939-115">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="29939-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="29939-116">V poli Platební podmínky kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="29939-116">In the Terms of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="29939-117">Související finanční úřad lze nastavit jako dodavatele a vyrovnání DPH vytvoří otevřenou fakturu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="29939-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="29939-118">Platební podmínky definují Datum splatnosti pro otevřenou fakturu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="29939-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
9. <span data-ttu-id="29939-119">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="29939-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="29939-120">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="29939-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="29939-121">Vyberte typ pro intervaly období vyrovnání.</span><span class="sxs-lookup"><span data-stu-id="29939-121">Select a type for the settlement period intervals.</span></span>
12. <span data-ttu-id="29939-122">Zadejte počet jednotek intervalu období pro každé období.</span><span class="sxs-lookup"><span data-stu-id="29939-122">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="29939-123">Například čtvrtletí má 3 měsíce.</span><span class="sxs-lookup"><span data-stu-id="29939-123">For example, a quarter has 3 months.</span></span>
13. <span data-ttu-id="29939-124">Zaškrtněte nebo zrušte zaškrtnutí políčka Použít dávkové zpracování pro vyrovnání DPH.</span><span class="sxs-lookup"><span data-stu-id="29939-124">Select or clear the Use batch processing for sales tax settlement check box.</span></span>
    * <span data-ttu-id="29939-125">Proces vyrovnání pro období vyrovnání lze zpracovat jako dávkovou úlohu na pozadí.</span><span class="sxs-lookup"><span data-stu-id="29939-125">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="29939-126">Tato možnost je vhodná velký počet daňových transakcí v rámci intervalu období.</span><span class="sxs-lookup"><span data-stu-id="29939-126">This is recommended for a large number of tax transactions within a period interval.</span></span>  
14. <span data-ttu-id="29939-127">Rozbalte kartu Intervaly období.</span><span class="sxs-lookup"><span data-stu-id="29939-127">Expand the Period intervals tab.</span></span>
15. <span data-ttu-id="29939-128">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="29939-128">Click Add.</span></span>
16. <span data-ttu-id="29939-129">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="29939-129">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="29939-130">Zadejte datum do pole Od data.</span><span class="sxs-lookup"><span data-stu-id="29939-130">In the From date field, enter a date.</span></span>
18. <span data-ttu-id="29939-131">Do pole Do data zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="29939-131">In the To date field, enter a date.</span></span>
19. <span data-ttu-id="29939-132">Klikněte na Nový interval období.</span><span class="sxs-lookup"><span data-stu-id="29939-132">Click New period interval.</span></span>
    * <span data-ttu-id="29939-133">Po zadání prvního intervalu období lze vytvořit automaticky nová období.</span><span class="sxs-lookup"><span data-stu-id="29939-133">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="29939-134">Můžete se vrátit a přidat nové intervaly období podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="29939-134">You can come back and add new period intervals as required.</span></span>  
20. <span data-ttu-id="29939-135">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="29939-135">Close the page.</span></span>


