---
title: Nastavení období vyrovnání DPH
description: Toto téma vysvětluje, jak nastavit období vyrovnání DPH v aplikaci Dynamics 365 Finance.
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
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5068c121e921c1586dc6ae003c0021bf41d2254
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441162"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="6c156-103">Nastavení období vyrovnání DPH</span><span class="sxs-lookup"><span data-stu-id="6c156-103">Set up sales tax settlement periods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6c156-104">Toto téma vysvětluje, jak nastavit období vyrovnání DPH.</span><span class="sxs-lookup"><span data-stu-id="6c156-104">This topic explains how to set up sales tax settlement periods.</span></span> <span data-ttu-id="6c156-105">Období vyrovnání DPH obsahuje informace o intervalech období, pro které se musí DPH vykazovat a platit.</span><span class="sxs-lookup"><span data-stu-id="6c156-105">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="6c156-106">Proces vyrovnání lze spustit pro období vyrovnání pro specifický časový interval.</span><span class="sxs-lookup"><span data-stu-id="6c156-106">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="6c156-107">Všechny kódy daně, které jsou spojené s obdobím vyrovnání, budou vyrovnány.</span><span class="sxs-lookup"><span data-stu-id="6c156-107">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="6c156-108">V závislosti na nastavení souvisejícího finančního úřadu je daňová povinnost zaúčtována pro dodavatele nebo na účet hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="6c156-108">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>

<span data-ttu-id="6c156-109">Tento úkol využívá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="6c156-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="6c156-110">V navigačním podokně přejděte na **Moduly > Daň > Nepřímé daně > DPH > Období vyrovnání DPH**.</span><span class="sxs-lookup"><span data-stu-id="6c156-110">In the navigation pane, go to **Modules > Tax > Indirect taxes > Sales tax > Sales tax settlement periods**.</span></span>
2. <span data-ttu-id="6c156-111">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="6c156-111">Select **New**.</span></span>
3. <span data-ttu-id="6c156-112">Zadejte hodnotu do pole **Období vyrovnání**.</span><span class="sxs-lookup"><span data-stu-id="6c156-112">In the **Settlement period** field, type a value.</span></span>
4. <span data-ttu-id="6c156-113">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="6c156-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="6c156-114">V poli **Úřad** vyberte finanční úřad, který přijímá sestavy a platby, které byly vytvořeny pro období vyrovnání.</span><span class="sxs-lookup"><span data-stu-id="6c156-114">In the **Authority** field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="6c156-115">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="6c156-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="6c156-116">V poli **Platební podmínky** vyberte požadovaný záznam v rozevírací nabídce.</span><span class="sxs-lookup"><span data-stu-id="6c156-116">In the **Terms of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="6c156-117">Související finanční úřad lze nastavit jako dodavatele a vyrovnání DPH vytvoří otevřenou fakturu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="6c156-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="6c156-118">Platební podmínky definují Datum splatnosti pro otevřenou fakturu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="6c156-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
8. <span data-ttu-id="6c156-119">Vyberte typ pro intervaly období vyrovnání.</span><span class="sxs-lookup"><span data-stu-id="6c156-119">Select a type for the settlement period intervals.</span></span>
9. <span data-ttu-id="6c156-120">Zadejte počet jednotek intervalu období pro každé období.</span><span class="sxs-lookup"><span data-stu-id="6c156-120">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="6c156-121">Například čtvrtletí má 3 měsíce.</span><span class="sxs-lookup"><span data-stu-id="6c156-121">For example, a quarter has 3 months.</span></span>
10. <span data-ttu-id="6c156-122">Zaškrtněte nebo zrušte zaškrtnutí políčka **Použít dávkové zpracování pro vyrovnání DPH**.</span><span class="sxs-lookup"><span data-stu-id="6c156-122">Select or clear the **Use batch processing for sales tax settlement** check box.</span></span> <span data-ttu-id="6c156-123">Proces vyrovnání pro období vyrovnání lze zpracovat jako dávkovou úlohu na pozadí.</span><span class="sxs-lookup"><span data-stu-id="6c156-123">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="6c156-124">Tato možnost je vhodná velký počet daňových transakcí v rámci intervalu období.</span><span class="sxs-lookup"><span data-stu-id="6c156-124">This is recommended for a large number of tax transactions within a period interval.</span></span>  
    > [!NOTE]
    > <span data-ttu-id="6c156-125">V současné době to není podporováno ve Španělsku, Japonsku a Nizozemsku.</span><span class="sxs-lookup"><span data-stu-id="6c156-125">Currently this is not supported in Spain, Japan, and the Netherlands.</span></span>
11. <span data-ttu-id="6c156-126">Zaškrtněte nebo odškrtněte políčko **Zabránit generování daňové transakce protiúčtu**.</span><span class="sxs-lookup"><span data-stu-id="6c156-126">Select or clear the **Prevent generating offset tax transactions** check box.</span></span> <span data-ttu-id="6c156-127">Ve výchozím nastavení systém generuje daňové transakce protiúčtu během procesu vyrovnání, což může způsobit problémy s výkonností, pokud je v určitém časovém intervalu velký počet daňových transakcí.</span><span class="sxs-lookup"><span data-stu-id="6c156-127">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="6c156-128">Zaškrtněte toto políčko, abyste zabránili generování daňové transakce protiúčtu.</span><span class="sxs-lookup"><span data-stu-id="6c156-128">Select this check box to prevent generating offset tax transactions.</span></span>
12. <span data-ttu-id="6c156-129">Rozbalte kartu **Intervaly období**.</span><span class="sxs-lookup"><span data-stu-id="6c156-129">Expand the **Period intervals** tab.</span></span>
13. <span data-ttu-id="6c156-130">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="6c156-130">Select **Add**.</span></span>
14. <span data-ttu-id="6c156-131">Zadejte datum do pole **Od data** v novém řádku.</span><span class="sxs-lookup"><span data-stu-id="6c156-131">In the **From date** field in the new row, enter a date.</span></span>
15. <span data-ttu-id="6c156-132">Do pole **Do data** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="6c156-132">In the **To date** field, enter a date.</span></span>
16. <span data-ttu-id="6c156-133">Vyberte **Nový interval období**.</span><span class="sxs-lookup"><span data-stu-id="6c156-133">Select **New period interval**.</span></span> <span data-ttu-id="6c156-134">Po zadání prvního intervalu období lze vytvořit automaticky nová období.</span><span class="sxs-lookup"><span data-stu-id="6c156-134">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="6c156-135">Můžete se vrátit a přidat nové intervaly období podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="6c156-135">You can come back and add new period intervals as required.</span></span>  
17. <span data-ttu-id="6c156-136">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="6c156-136">Close the page.</span></span>

