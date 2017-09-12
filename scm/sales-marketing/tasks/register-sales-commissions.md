--- 
title: "Registrace prodejních provizí"
description: "Tento postup popisuje, jak jsou vypočítány a registrovány prodejní provize."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f195f9e466eab3cf87afea2b5d430d0ea25c5a83
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="register-sales-commissions"></a><span data-ttu-id="27fe5-103">Registrace prodejních provizí</span><span class="sxs-lookup"><span data-stu-id="27fe5-103">Register sales commissions</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="27fe5-104">Tento postup popisuje, jak jsou vypočítány a registrovány prodejní provize.</span><span class="sxs-lookup"><span data-stu-id="27fe5-104">This procedure shows you how sales commissions are calculated and registered.</span></span> <span data-ttu-id="27fe5-105">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="27fe5-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="27fe5-106">Před spuštěním této příručky, spusťte průvodce s názvem „Nastavení pravidel prodejní provize“ abyste měli všechna nezbytná nastavení výpočtu provize.</span><span class="sxs-lookup"><span data-stu-id="27fe5-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="27fe5-107">Poznamenejte si čísla odběratele a zboží, které jste zvolili pro proces provize a použijte je, když budete v této příručce vyzváni k vytvoření prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="27fe5-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="27fe5-108">Faktura prodejní objednávky, která opravňuje prodejce získat provizi</span><span class="sxs-lookup"><span data-stu-id="27fe5-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="27fe5-109">Přejděte na Prodej a marketing > Prodejní objednávky > Všechny prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="27fe5-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="27fe5-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="27fe5-110">Click New.</span></span>
3. <span data-ttu-id="27fe5-111">V poli Účet odběratele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="27fe5-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="27fe5-112">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="27fe5-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="27fe5-113">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="27fe5-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="27fe5-114">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="27fe5-114">Click OK.</span></span>
7. <span data-ttu-id="27fe5-115">V podokně akcí klikněte na Možnosti.</span><span class="sxs-lookup"><span data-stu-id="27fe5-115">On the Action Pane, click Options.</span></span>
8. <span data-ttu-id="27fe5-116">Klikněte na tlačítko Změnit zobrazení.</span><span class="sxs-lookup"><span data-stu-id="27fe5-116">Click Change view.</span></span>
9. <span data-ttu-id="27fe5-117">Klikněte na možnost Zobrazení záhlaví.</span><span class="sxs-lookup"><span data-stu-id="27fe5-117">Click Header view.</span></span>
10. <span data-ttu-id="27fe5-118">Rozbalte sekci Nastavení.</span><span class="sxs-lookup"><span data-stu-id="27fe5-118">Expand the Setup section.</span></span>
    * <span data-ttu-id="27fe5-119">Hodnota v poli Prodejní skupina představuje skupinu s jedním nebo více přiřazenými prodejními zástupci.</span><span class="sxs-lookup"><span data-stu-id="27fe5-119">The value in the Sales group field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="27fe5-120">Uživatelé ve skupině jsou ti, kteří po vyfakturování objednávky podle předdefinované sazby a distribuce obdrží provizi.</span><span class="sxs-lookup"><span data-stu-id="27fe5-120">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   <span data-ttu-id="27fe5-121">Hodnota se zkopíruje z karty zákazníka, ale pokud chcete, lze ji změnit.</span><span class="sxs-lookup"><span data-stu-id="27fe5-121">The value is copied from the Customer card, but you can change it if you wish.</span></span>  <span data-ttu-id="27fe5-122">Skupina prodeje se zkopíruje také do řádku prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="27fe5-122">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="27fe5-123">Můžete ji změnit tak, že se může lišit od skupiny uvedené v záhlaví a/nebo mezi řádky.</span><span class="sxs-lookup"><span data-stu-id="27fe5-123">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    * <span data-ttu-id="27fe5-124">Hodnota v poli skupiny provize představuje skupinu, kterou jste vytvořili pro jednoho nebo více odběratelů za účelem sledování provizí.</span><span class="sxs-lookup"><span data-stu-id="27fe5-124">The value in the Commission group field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   <span data-ttu-id="27fe5-125">Hodnota se zkopíruje z karty zákazníka, ale pokud chcete, lze ji změnit.</span><span class="sxs-lookup"><span data-stu-id="27fe5-125">The value is copied from the Customer card, but you can change it if you wish.</span></span>   
11. <span data-ttu-id="27fe5-126">V podokně akcí klikněte na Možnosti.</span><span class="sxs-lookup"><span data-stu-id="27fe5-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="27fe5-127">Klikněte na tlačítko Změnit zobrazení.</span><span class="sxs-lookup"><span data-stu-id="27fe5-127">Click Change view.</span></span>
13. <span data-ttu-id="27fe5-128">Klepněte na možnost Řádkové zobrazení.</span><span class="sxs-lookup"><span data-stu-id="27fe5-128">Click Line view.</span></span>
14. <span data-ttu-id="27fe5-129">V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="27fe5-129">In the Item number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="27fe5-130">V seznamu vyberte položku, kterou jste pro provize nastavili.</span><span class="sxs-lookup"><span data-stu-id="27fe5-130">In the list, select the item you have set up for commissions.</span></span> 
16. <span data-ttu-id="27fe5-131">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="27fe5-131">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="27fe5-132">Udělejte si poznámku o řádku Čistá částka.</span><span class="sxs-lookup"><span data-stu-id="27fe5-132">Take note of the line's Net amount.</span></span> <span data-ttu-id="27fe5-133">Ta představuje výnosy z prodeje, které v tomto příkladu jsou základem pro výpočet provize.</span><span class="sxs-lookup"><span data-stu-id="27fe5-133">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
17. <span data-ttu-id="27fe5-134">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="27fe5-134">Click Save.</span></span>
18. <span data-ttu-id="27fe5-135">V podokně akcí klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="27fe5-135">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="27fe5-136">Klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="27fe5-136">Click Invoice.</span></span>
20. <span data-ttu-id="27fe5-137">Rozbalte sekci Parametry.</span><span class="sxs-lookup"><span data-stu-id="27fe5-137">Expand the Parameters section.</span></span>
21. <span data-ttu-id="27fe5-138">V poli Množství vyberte možnost Vše.</span><span class="sxs-lookup"><span data-stu-id="27fe5-138">In the Quantity field, select 'All'.</span></span>
22. <span data-ttu-id="27fe5-139">Vyberte možnost Ano v poli Účtování.</span><span class="sxs-lookup"><span data-stu-id="27fe5-139">Select Yes in the Posting field.</span></span>
23. <span data-ttu-id="27fe5-140">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="27fe5-140">Click OK.</span></span>
24. <span data-ttu-id="27fe5-141">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="27fe5-141">Click OK.</span></span>
    * <span data-ttu-id="27fe5-142">Zaúčtování transakce může trvat kolem minuty.</span><span class="sxs-lookup"><span data-stu-id="27fe5-142">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="27fe5-143">K dokončení povolte zpracování a nezavírejte stránku.</span><span class="sxs-lookup"><span data-stu-id="27fe5-143">Allow the processing to complete and don’t close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="27fe5-144">Zobrazení registrovaných provizí z prodeje</span><span class="sxs-lookup"><span data-stu-id="27fe5-144">Review the registered sales commissions</span></span>
1. <span data-ttu-id="27fe5-145">V podokně akcí klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="27fe5-145">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="27fe5-146">Klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="27fe5-146">Click Invoice.</span></span>
3. <span data-ttu-id="27fe5-147">V podokně akcí klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="27fe5-147">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="27fe5-148">Klepněte na Transakce provizí.</span><span class="sxs-lookup"><span data-stu-id="27fe5-148">Click Commission transactions.</span></span>
    * <span data-ttu-id="27fe5-149">Na kartě Přehled jsou zobrazeny řádky představující částky provize vyplacené prodejním zástupcům, kteří jsou přiřazeni k vyfakturované prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="27fe5-149">The Overview tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="27fe5-150">Zkontrolujme si podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="27fe5-150">Let's review the details.</span></span>     
    * <span data-ttu-id="27fe5-151">Pokud jste použili průvodce „Nastavení pravidel prodejní provize“ k nastavení prodejní skupiny, existují dva prodejci, kteří obdrží provizi, a provize bude mezi nimi rozdělena stejnoměrně.</span><span class="sxs-lookup"><span data-stu-id="27fe5-151">If you used the "Set up sales commission rules" guide to set up the Commission sales group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    * <span data-ttu-id="27fe5-152">V tomto příkladu se vypočítává celková částka provize jako procento výnosu z prodeje (čistá částka řádku objednávky).</span><span class="sxs-lookup"><span data-stu-id="27fe5-152">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>   
5. <span data-ttu-id="27fe5-153">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="27fe5-153">Close the page.</span></span>
6. <span data-ttu-id="27fe5-154">Klikněte na možnost Doklad.</span><span class="sxs-lookup"><span data-stu-id="27fe5-154">Click Voucher.</span></span>
    * <span data-ttu-id="27fe5-155">Transakce dokladu můžete zkontrolovat pro částky provize, které byly zaúčtované do předdefinovaných výdajů a účtů vyplacené provize.</span><span class="sxs-lookup"><span data-stu-id="27fe5-155">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  


