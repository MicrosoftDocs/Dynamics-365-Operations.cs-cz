---
title: Nastavení období vyrovnání DPH
description: Toto téma vysvětluje, jak nastavit období vyrovnání DPH v aplikaci Dynamics 365 Finance.
author: twheeloc
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 83587df3963d215fec020150e6b707e431c1b6eb
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944770"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="c8067-103">Nastavení období vyrovnání DPH</span><span class="sxs-lookup"><span data-stu-id="c8067-103">Set up sales tax settlement periods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c8067-104">Toto téma vysvětluje, jak nastavit období vyrovnání DPH.</span><span class="sxs-lookup"><span data-stu-id="c8067-104">This topic explains how to set up sales tax settlement periods.</span></span> <span data-ttu-id="c8067-105">Období vyrovnání DPH obsahuje informace o intervalech období, pro které se musí DPH vykazovat a platit.</span><span class="sxs-lookup"><span data-stu-id="c8067-105">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="c8067-106">Proces vyrovnání lze spustit pro období vyrovnání pro specifický časový interval.</span><span class="sxs-lookup"><span data-stu-id="c8067-106">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="c8067-107">Všechny kódy daně, které jsou spojené s obdobím vyrovnání, budou vyrovnány.</span><span class="sxs-lookup"><span data-stu-id="c8067-107">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="c8067-108">V závislosti na nastavení souvisejícího finančního úřadu je daňová povinnost zaúčtována pro dodavatele nebo na účet hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="c8067-108">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>

<span data-ttu-id="c8067-109">Tento úkol využívá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="c8067-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="c8067-110">V navigačním podokně přejděte na **Moduly > Daň > Nepřímé daně > DPH > Období vyrovnání DPH**.</span><span class="sxs-lookup"><span data-stu-id="c8067-110">In the navigation pane, go to **Modules > Tax > Indirect taxes > Sales tax > Sales tax settlement periods**.</span></span>
2. <span data-ttu-id="c8067-111">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="c8067-111">Select **New**.</span></span>
3. <span data-ttu-id="c8067-112">Zadejte hodnotu do pole **Období vyrovnání**.</span><span class="sxs-lookup"><span data-stu-id="c8067-112">In the **Settlement period** field, type a value.</span></span>
4. <span data-ttu-id="c8067-113">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="c8067-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="c8067-114">V poli **Úřad** vyberte finanční úřad, který přijímá sestavy a platby, které byly vytvořeny pro období vyrovnání.</span><span class="sxs-lookup"><span data-stu-id="c8067-114">In the **Authority** field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="c8067-115">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="c8067-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="c8067-116">V poli **Platební podmínky** vyberte požadovaný záznam v rozevírací nabídce.</span><span class="sxs-lookup"><span data-stu-id="c8067-116">In the **Terms of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="c8067-117">Související finanční úřad lze nastavit jako dodavatele a vyrovnání DPH vytvoří otevřenou fakturu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="c8067-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="c8067-118">Platební podmínky definují Datum splatnosti pro otevřenou fakturu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="c8067-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
8. <span data-ttu-id="c8067-119">Vyberte typ pro intervaly období vyrovnání.</span><span class="sxs-lookup"><span data-stu-id="c8067-119">Select a type for the settlement period intervals.</span></span>
9. <span data-ttu-id="c8067-120">Zadejte počet jednotek intervalu období pro každé období.</span><span class="sxs-lookup"><span data-stu-id="c8067-120">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="c8067-121">Například čtvrtletí má 3 měsíce.</span><span class="sxs-lookup"><span data-stu-id="c8067-121">For example, a quarter has 3 months.</span></span>
10. <span data-ttu-id="c8067-122">Zaškrtněte nebo zrušte zaškrtnutí políčka **Použít dávkové zpracování pro vyrovnání DPH**.</span><span class="sxs-lookup"><span data-stu-id="c8067-122">Select or clear the **Use batch processing for sales tax settlement** check box.</span></span> <span data-ttu-id="c8067-123">Proces vyrovnání pro období vyrovnání lze zpracovat jako dávkovou úlohu na pozadí.</span><span class="sxs-lookup"><span data-stu-id="c8067-123">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="c8067-124">Tato možnost je vhodná velký počet daňových transakcí v rámci intervalu období.</span><span class="sxs-lookup"><span data-stu-id="c8067-124">This is recommended for a large number of tax transactions within a period interval.</span></span>
11. <span data-ttu-id="c8067-125">Zaškrtněte nebo odškrtněte políčko **Zabránit generování daňové transakce protiúčtu**.</span><span class="sxs-lookup"><span data-stu-id="c8067-125">Select or clear the **Prevent generating offset tax transactions** check box.</span></span> <span data-ttu-id="c8067-126">Ve výchozím nastavení systém generuje daňové transakce protiúčtu během procesu vyrovnání, což může způsobit problémy s výkonností, pokud je v určitém časovém intervalu velký počet daňových transakcí.</span><span class="sxs-lookup"><span data-stu-id="c8067-126">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="c8067-127">Zaškrtněte toto políčko, abyste zabránili generování daňové transakce protiúčtu.</span><span class="sxs-lookup"><span data-stu-id="c8067-127">Select this check box to prevent generating offset tax transactions.</span></span>
12. <span data-ttu-id="c8067-128">Rozbalte kartu **Intervaly období**.</span><span class="sxs-lookup"><span data-stu-id="c8067-128">Expand the **Period intervals** tab.</span></span>
13. <span data-ttu-id="c8067-129">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="c8067-129">Select **Add**.</span></span>
14. <span data-ttu-id="c8067-130">Zadejte datum do pole **Od data** v novém řádku.</span><span class="sxs-lookup"><span data-stu-id="c8067-130">In the **From date** field in the new row, enter a date.</span></span>
15. <span data-ttu-id="c8067-131">Do pole **Do data** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="c8067-131">In the **To date** field, enter a date.</span></span>
16. <span data-ttu-id="c8067-132">Vyberte **Nový interval období**.</span><span class="sxs-lookup"><span data-stu-id="c8067-132">Select **New period interval**.</span></span> <span data-ttu-id="c8067-133">Po zadání prvního intervalu období lze vytvořit automaticky nová období.</span><span class="sxs-lookup"><span data-stu-id="c8067-133">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="c8067-134">Můžete se vrátit a přidat nové intervaly období podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="c8067-134">You can come back and add new period intervals as required.</span></span>  
17. <span data-ttu-id="c8067-135">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c8067-135">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
