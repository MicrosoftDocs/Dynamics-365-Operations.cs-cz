--- 
title: "Vytváření a úpravy prodejních nabídek"
description: "Tento postup ukazuje, jak vytvořit a aktualizovat prodejní nabídku."
author: omulvad
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SalesQuotationTotals, SalesQuotationPriceSimulation, SalesQuotationEditLines, SrsReportViewerForm, smmSetNumSeqIfManual, CustTable, SalesTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: c5e7164633bbb33b436ab7a6fcd8ff62183c6eb5
ms.contentlocale: cs-cz
ms.lasthandoff: 09/11/2018

---
# <a name="create-and-edit-sales-quotations"></a><span data-ttu-id="d12c3-103">Vytváření a úpravy prodejních nabídek</span><span class="sxs-lookup"><span data-stu-id="d12c3-103">Create and edit sales quotations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d12c3-104">Tento postup ukazuje, jak vytvořit a aktualizovat prodejní nabídku.</span><span class="sxs-lookup"><span data-stu-id="d12c3-104">This procedure demonstrates how to create and update a sales quotation.</span></span> <span data-ttu-id="d12c3-105">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="d12c3-105">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-sales-quotation"></a><span data-ttu-id="d12c3-106">Vytvoření prodejní nabídky</span><span class="sxs-lookup"><span data-stu-id="d12c3-106">Create a sales quotation</span></span>
1. <span data-ttu-id="d12c3-107">Přejděte na Prodej a marketing > Prodejní nabídky > Všechny nabídky.</span><span class="sxs-lookup"><span data-stu-id="d12c3-107">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
2. <span data-ttu-id="d12c3-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="d12c3-108">Click New.</span></span>
3. <span data-ttu-id="d12c3-109">V poli Typ účtu vyberte „Potenciální zákazník“.</span><span class="sxs-lookup"><span data-stu-id="d12c3-109">In the Account type field, select 'Prospect'.</span></span>
4. <span data-ttu-id="d12c3-110">V poli Potenciální zákazník zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d12c3-110">In the Prospect field, enter or select a value.</span></span>
5. <span data-ttu-id="d12c3-111">Rozbalte sekci Obecné.</span><span class="sxs-lookup"><span data-stu-id="d12c3-111">Expand the General section.</span></span>
    * <span data-ttu-id="d12c3-112">Vzhledem k tomu, že jste zvolili vytvoření nabídky z oblasti prodeje a marketingu, je typ nastaven automaticky na prodejní nabídku.</span><span class="sxs-lookup"><span data-stu-id="d12c3-112">Because you chose to create a quotation from the Sales and Marketing area, the type is automatically set to Sales quotation.</span></span> <span data-ttu-id="d12c3-113">K vytvoření nabídky pro projekt k ní musíte mít přístup z modulu Řízení a účetnictví projektů.</span><span class="sxs-lookup"><span data-stu-id="d12c3-113">To create a quotation for a project you must access it from the Project management and accounting module.</span></span>   
6. <span data-ttu-id="d12c3-114">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d12c3-114">Click OK.</span></span>
    * <span data-ttu-id="d12c3-115">Pole a akce pro řádky nabídky se velmi podobají položkám na řádcích prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="d12c3-115">The fields and actions on the quotation lines are very similar to the ones on the sales order lines.</span></span>   <span data-ttu-id="d12c3-116">Stejně jako prodejní objednávky lze nabídky vytvářet pro konkrétní zboží nebo pro neznámé či neexistující číslo zboží, které v době vytvoření nabídky není k dispozici, nabídky lze vytvářet pro kategorii prodeje.</span><span class="sxs-lookup"><span data-stu-id="d12c3-116">Like sales orders, quotations can be created for a specific item or, when item number is not known or does not exist at the time of quotation creation, quotations can be created for a sales category.</span></span>  
7. <span data-ttu-id="d12c3-117">V poli Zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d12c3-117">In the Item field, enter or select a value.</span></span>
8. <span data-ttu-id="d12c3-118">Zadejte hodnotu do pole Zboží.</span><span class="sxs-lookup"><span data-stu-id="d12c3-118">In the Item field, type a value.</span></span>
9. <span data-ttu-id="d12c3-119">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d12c3-119">Close the page.</span></span>
10. <span data-ttu-id="d12c3-120">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="d12c3-120">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="d12c3-121">Pokud existují platné obchodní smlouvy pro vybrané zboží v řádku, použití cena a slevy se automaticky zkopírují řádku nabídky.</span><span class="sxs-lookup"><span data-stu-id="d12c3-121">If there are valid trade agreements for the item selected on the line, the applicable price and discounts will be automatically copied to the quotation line.</span></span> <span data-ttu-id="d12c3-122">Ujistěte se, že pole Jednotková cena obsahuje hodnotu a chcete-li můžete také zadat hodnotu slevy.</span><span class="sxs-lookup"><span data-stu-id="d12c3-122">Make sure that the Unit price field contains a value and you can also enter discount values if you want to.</span></span>  
11. <span data-ttu-id="d12c3-123">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="d12c3-123">Click Save.</span></span>
12. <span data-ttu-id="d12c3-124">V podokně akcí klikněte na položku Prodejní nabídka.</span><span class="sxs-lookup"><span data-stu-id="d12c3-124">On the Action Pane, click Sales quotation.</span></span>
13. <span data-ttu-id="d12c3-125">Klikněte na položku Součty.</span><span class="sxs-lookup"><span data-stu-id="d12c3-125">Click Totals.</span></span>
14. <span data-ttu-id="d12c3-126">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d12c3-126">Click OK.</span></span>
15. <span data-ttu-id="d12c3-127">Klikněte na položku Řádek prodejní nabídky.</span><span class="sxs-lookup"><span data-stu-id="d12c3-127">Click Sales quotation line.</span></span>
16. <span data-ttu-id="d12c3-128">Klikněte na položku Ceny.</span><span class="sxs-lookup"><span data-stu-id="d12c3-128">Click Prices.</span></span>
    * <span data-ttu-id="d12c3-129">Na stránce Spustit simulaci ceny můžete vyzkoušet úpravami očekávané výnosy nebo ziskovost vaší nabídky na základě požadované jednotkové ceny, částku slevy, procento slevy, celkovou částku, marži nebo příspěvkový poměr.</span><span class="sxs-lookup"><span data-stu-id="d12c3-129">In the Run price simulation page you can experiment with adjusting the expected revenue or profitability of your quotation based on the desired unit price, discount amount, discount percentage, total amount, margin, or contribution ratio.</span></span>   <span data-ttu-id="d12c3-130">Pokud jste spokojeni s cílovými hodnotami, lze návrh použít pro daný řádek nabídky a její pole související s cenami bude odpovídajícím způsobem aktualizováno.</span><span class="sxs-lookup"><span data-stu-id="d12c3-130">When you are satisfied with the target figures, you apply the suggestion to the quotation line, and its price-related fields will be updated accordingly.</span></span>  
    * <span data-ttu-id="d12c3-131">Simulací cen můžete vytvářet, kolik chcete.</span><span class="sxs-lookup"><span data-stu-id="d12c3-131">Y ou can create as many price simulations as you wish.</span></span> <span data-ttu-id="d12c3-132">Klepnete-li na Nový, cenové podmínky z aktuálního řádku nabídky se zkopírují na stránku.</span><span class="sxs-lookup"><span data-stu-id="d12c3-132">When you click New, the price conditions from the current quotation line are copied to the page.</span></span> <span data-ttu-id="d12c3-133">Můžete pak upravit hodnoty v jakémkoli poli souvisejícím s cenami do cílových hodnot.</span><span class="sxs-lookup"><span data-stu-id="d12c3-133">You can then modify values in any of the price-related fields to the target ones.</span></span> <span data-ttu-id="d12c3-134">Změny v jednom z polí spustí přepočet ve všech ostatních polích.</span><span class="sxs-lookup"><span data-stu-id="d12c3-134">A change in one of the fields will trigger recalculation in all the other fields.</span></span> <span data-ttu-id="d12c3-135">Aby systém vypočítal prodejní marže a příspěvkový poměr, musí znát pořizovací cenu produktu.</span><span class="sxs-lookup"><span data-stu-id="d12c3-135">In order for the system to calculate the sales margin and contribution ratio, the product's unit cost has to be known.</span></span> <span data-ttu-id="d12c3-136">Použijte kartu Simulované ceny pro podrobné zobrazení původních cen, navržených změn a jejich vlivu na celkové hodnoty nabídky.</span><span class="sxs-lookup"><span data-stu-id="d12c3-136">Use the Simulated prices tab for a detailed view of the original prices, proposed changes and their effect on the quotation totals.</span></span>   <span data-ttu-id="d12c3-137">Obecně platí, že když simulace určuje nové množství pro daný řádek nabídky, systém přepočítá a zadá novou hodnotu v poli Jednotková cena.</span><span class="sxs-lookup"><span data-stu-id="d12c3-137">As a general rule, when a simulation that sets a new amount is applied to the quotation line, the system recalculates and enters a new value in the Unit price field.</span></span> <span data-ttu-id="d12c3-138">Pokud simulace vychází z nové marže nebo nového příspěvkového poměru, je aktualizováno pouze pole Čistá částka a pole Jednotková cena je prázdné.</span><span class="sxs-lookup"><span data-stu-id="d12c3-138">If the simulation is based on a new margin or a new contribution ratio, only the Net amount field is updated, and the Unit price is blank.</span></span> <span data-ttu-id="d12c3-139">V obou případech budou odstraněny všechny slevy, které byly na řádku nabídky před simulací.</span><span class="sxs-lookup"><span data-stu-id="d12c3-139">In both cases, any discounts that were on the quotation line before simulation will be deleted.</span></span>  
17. <span data-ttu-id="d12c3-140">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d12c3-140">Close the page.</span></span>
18. <span data-ttu-id="d12c3-141">V podokně akcí klikněte na položku Nabídka.</span><span class="sxs-lookup"><span data-stu-id="d12c3-141">On the Action Pane, click Quotation.</span></span>
19. <span data-ttu-id="d12c3-142">Klikněte na položku Odeslat nabídku.</span><span class="sxs-lookup"><span data-stu-id="d12c3-142">Click Send quotation.</span></span>
20. <span data-ttu-id="d12c3-143">Vyberte možnost Ano v poli Tisk nabídky.</span><span class="sxs-lookup"><span data-stu-id="d12c3-143">Select Yes in the Print quotation field.</span></span>
21. <span data-ttu-id="d12c3-144">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d12c3-144">Click OK.</span></span>
    * <span data-ttu-id="d12c3-145">Generování sestavy může trvat několik minut.</span><span class="sxs-lookup"><span data-stu-id="d12c3-145">The report may take a minute to generate.</span></span> <span data-ttu-id="d12c3-146">Dokud proces nebude dokončen, stránku nezavírejte.</span><span class="sxs-lookup"><span data-stu-id="d12c3-146">Don’t close the page until it does so.</span></span>  
22. <span data-ttu-id="d12c3-147">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d12c3-147">Close the page.</span></span>

## <a name="update-a-sales-quotation"></a><span data-ttu-id="d12c3-148">Aktualizace prodejní nabídky</span><span class="sxs-lookup"><span data-stu-id="d12c3-148">Update a sales quotation</span></span>
1. <span data-ttu-id="d12c3-149">V podokně akcí klikněte na položku Zpracovat.</span><span class="sxs-lookup"><span data-stu-id="d12c3-149">On the Action Pane, click Follow up.</span></span>
2. <span data-ttu-id="d12c3-150">Klepněte na Převést na odběratele.</span><span class="sxs-lookup"><span data-stu-id="d12c3-150">Click Convert to customer.</span></span>
3. <span data-ttu-id="d12c3-151">V poli Účet odběratele zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d12c3-151">In the Customer account field, type a value.</span></span>
4. <span data-ttu-id="d12c3-152">Klepněte na možnost Kontrola.</span><span class="sxs-lookup"><span data-stu-id="d12c3-152">Click Check.</span></span>
    * <span data-ttu-id="d12c3-153">Ujistěte se, že se zobrazí zpráva, že číslo účtu, které jste zadali, lze volně použít.</span><span class="sxs-lookup"><span data-stu-id="d12c3-153">Make sure you see a message that the account number you typed in is free to use.</span></span>  
5. <span data-ttu-id="d12c3-154">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d12c3-154">Click OK.</span></span>
    * <span data-ttu-id="d12c3-155">Systém právě vytvořil účet nového odběratele pro potenciálního zákazníka z nabídky.</span><span class="sxs-lookup"><span data-stu-id="d12c3-155">The system has now created a new customer account for the prospect on the quotation.</span></span>  
6. <span data-ttu-id="d12c3-156">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d12c3-156">Close the page.</span></span>
7. <span data-ttu-id="d12c3-157">V podokně akcí klikněte na položku Zpracovat.</span><span class="sxs-lookup"><span data-stu-id="d12c3-157">On the Action Pane, click Follow up.</span></span>
8. <span data-ttu-id="d12c3-158">Klikněte na tlačítko Potvrdit.</span><span class="sxs-lookup"><span data-stu-id="d12c3-158">Click Confirm.</span></span>
9. <span data-ttu-id="d12c3-159">V poli Důvod zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d12c3-159">In the Reason field, enter or select a value.</span></span>
10. <span data-ttu-id="d12c3-160">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d12c3-160">Click OK.</span></span>
11. <span data-ttu-id="d12c3-161">V podokně akcí klikněte na položku Obecné.</span><span class="sxs-lookup"><span data-stu-id="d12c3-161">On the Action Pane, click General.</span></span>
12. <span data-ttu-id="d12c3-162">Klikněte na položku Prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="d12c3-162">Click Sales orders.</span></span>
13. <span data-ttu-id="d12c3-163">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d12c3-163">Close the page.</span></span>


