---
title: Nastavit období vyrovnání DPH
description: Období vyrovnání DPH obsahuje informace o intervalech období, pro které se musí DPH vykazovat a platit.
author: twheeloc
manager: AnnBe
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8304d9e8997a5d31740ee1203aa4bf0603014056
ms.sourcegitcommit: d0fa8d0140fa81029527edb317623c1a7737c593
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2019
ms.locfileid: "1862981"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="357d7-103">Nastavit období vyrovnání DPH</span><span class="sxs-lookup"><span data-stu-id="357d7-103">Set up sales tax settlement periods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="357d7-104">Období vyrovnání DPH obsahuje informace o intervalech období, pro které se musí DPH vykazovat a platit.</span><span class="sxs-lookup"><span data-stu-id="357d7-104">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="357d7-105">Proces vyrovnání lze spustit pro období vyrovnání pro specifický časový interval.</span><span class="sxs-lookup"><span data-stu-id="357d7-105">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="357d7-106">Všechny kódy daně, které jsou spojené s obdobím vyrovnání, budou vyrovnány.</span><span class="sxs-lookup"><span data-stu-id="357d7-106">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="357d7-107">V závislosti na nastavení souvisejícího finančního úřadu je daňová povinnost zaúčtována pro dodavatele nebo na účet hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="357d7-107">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>



<span data-ttu-id="357d7-108">Tento úkol používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="357d7-108">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="357d7-109">Přejděte na Daň > Nepřímé daně > DPH > Období vyrovnání DPH.</span><span class="sxs-lookup"><span data-stu-id="357d7-109">Go to Tax > Indirect taxes > Sales tax > Sales tax settlement periods.</span></span>
2. <span data-ttu-id="357d7-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="357d7-110">Click New.</span></span>
3. <span data-ttu-id="357d7-111">Zadejte hodnotu do pole Období vyrovnání.</span><span class="sxs-lookup"><span data-stu-id="357d7-111">In the Settlement period field, type a value.</span></span>
4. <span data-ttu-id="357d7-112">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="357d7-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="357d7-113">V poli Úřad vyberte finanční úřad, který přijímá sestavy a platby, které byly vytvořeny pro období vyrovnání.</span><span class="sxs-lookup"><span data-stu-id="357d7-113">In the Authority field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="357d7-114">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="357d7-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="357d7-115">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="357d7-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="357d7-116">V poli Platební podmínky kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="357d7-116">In the Terms of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="357d7-117">Související finanční úřad lze nastavit jako dodavatele a vyrovnání DPH vytvoří otevřenou fakturu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="357d7-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="357d7-118">Platební podmínky definují Datum splatnosti pro otevřenou fakturu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="357d7-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
9. <span data-ttu-id="357d7-119">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="357d7-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="357d7-120">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="357d7-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="357d7-121">Vyberte typ pro intervaly období vyrovnání.</span><span class="sxs-lookup"><span data-stu-id="357d7-121">Select a type for the settlement period intervals.</span></span>
12. <span data-ttu-id="357d7-122">Zadejte počet jednotek intervalu období pro každé období.</span><span class="sxs-lookup"><span data-stu-id="357d7-122">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="357d7-123">Například čtvrtletí má 3 měsíce.</span><span class="sxs-lookup"><span data-stu-id="357d7-123">For example, a quarter has 3 months.</span></span>
13. <span data-ttu-id="357d7-124">Zaškrtněte nebo zrušte zaškrtnutí políčka Použít dávkové zpracování pro vyrovnání DPH.</span><span class="sxs-lookup"><span data-stu-id="357d7-124">Select or clear the Use batch processing for sales tax settlement check box.</span></span>
    * <span data-ttu-id="357d7-125">Proces vyrovnání pro období vyrovnání lze zpracovat jako dávkovou úlohu na pozadí.</span><span class="sxs-lookup"><span data-stu-id="357d7-125">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="357d7-126">Tato možnost je vhodná velký počet daňových transakcí v rámci intervalu období.</span><span class="sxs-lookup"><span data-stu-id="357d7-126">This is recommended for a large number of tax transactions within a period interval.</span></span>  
    > [!NOTE]
    > <span data-ttu-id="357d7-127">V současné době to není podporováno v Rakousku, Belgii, Španělsku, Itálii, Japonsku a Nizozemsku.</span><span class="sxs-lookup"><span data-stu-id="357d7-127">Currently this is not supported in Austria, Belgium, Spain, Italy, Japan, and the Netherlands.</span></span>
14. <span data-ttu-id="357d7-128">Zaškrtněte nebo odškrtněte políčko Zabránit generování daňové transakce protiúčtu.</span><span class="sxs-lookup"><span data-stu-id="357d7-128">Select or clear the Prevent generating offset tax transactions check box.</span></span>
    * <span data-ttu-id="357d7-129">Ve výchozím nastavení systém generuje daňové transakce protiúčtu během procesu vyrovnání, což může způsobit problémy s výkonností, pokud je v určitém časovém intervalu velký počet daňových transakcí.</span><span class="sxs-lookup"><span data-stu-id="357d7-129">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="357d7-130">Zaškrtněte toto políčko, abyste zabránili generování daňové transakce protiúčtu.</span><span class="sxs-lookup"><span data-stu-id="357d7-130">Select this check box to prevent generating offset tax transactions.</span></span>
15. <span data-ttu-id="357d7-131">Rozbalte kartu Intervaly období.</span><span class="sxs-lookup"><span data-stu-id="357d7-131">Expand the Period intervals tab.</span></span>
16. <span data-ttu-id="357d7-132">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="357d7-132">Click Add.</span></span>
17. <span data-ttu-id="357d7-133">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="357d7-133">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="357d7-134">Zadejte datum do pole Od data.</span><span class="sxs-lookup"><span data-stu-id="357d7-134">In the From date field, enter a date.</span></span>
19. <span data-ttu-id="357d7-135">Do pole Do data zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="357d7-135">In the To date field, enter a date.</span></span>
20. <span data-ttu-id="357d7-136">Klikněte na Nový interval období.</span><span class="sxs-lookup"><span data-stu-id="357d7-136">Click New period interval.</span></span>
    * <span data-ttu-id="357d7-137">Po zadání prvního intervalu období lze vytvořit automaticky nová období.</span><span class="sxs-lookup"><span data-stu-id="357d7-137">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="357d7-138">Můžete se vrátit a přidat nové intervaly období podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="357d7-138">You can come back and add new period intervals as required.</span></span>  
21. <span data-ttu-id="357d7-139">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="357d7-139">Close the page.</span></span>

