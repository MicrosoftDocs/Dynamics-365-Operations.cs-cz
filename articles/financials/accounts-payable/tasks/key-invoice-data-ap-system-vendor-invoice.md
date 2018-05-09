--- 
title: "Zadání dat faktury do závazků s použitím faktury dodavatele"
description: "Tento průvodce záznamem úloh vám pomůže vytvořit fakturu dodavatele z nákupní objednávky a zobrazit si výsledky párování nákupní objednávky, příjemky a faktury (třícestné párování)."
author: abruer
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
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: bdc0ef1c23bcbe60a126aacef9940acee84dce89
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---
# <a name="key-invoice-data-into-accounts-payable-using-a-vendor-invoice"></a><span data-ttu-id="beda7-103">Zadání dat faktury do závazků s použitím faktury dodavatele</span><span class="sxs-lookup"><span data-stu-id="beda7-103">Key invoice data into accounts payable using a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="beda7-104">Tento průvodce záznamem úloh vám pomůže vytvořit fakturu dodavatele z nákupní objednávky a zobrazit si výsledky párování nákupní objednávky, příjemky a faktury (třícestné párování).</span><span class="sxs-lookup"><span data-stu-id="beda7-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="beda7-105">Vytvoření nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="beda7-105">Create a purchase order</span></span>
1. <span data-ttu-id="beda7-106">Přejděte na Závazky > Nákupní objednávky > Všechny nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="beda7-106">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="beda7-107">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="beda7-107">Click New.</span></span>
3. <span data-ttu-id="beda7-108">V poli Účet dodavatele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="beda7-108">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="beda7-109">Najděte dodavatele, kterého chcete vybrat.</span><span class="sxs-lookup"><span data-stu-id="beda7-109">Find a vendor to select.</span></span> <span data-ttu-id="beda7-110">Například přejděte na US-104.</span><span class="sxs-lookup"><span data-stu-id="beda7-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="beda7-111">Vyberte dodavatele US-104.</span><span class="sxs-lookup"><span data-stu-id="beda7-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="beda7-112">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="beda7-112">Click OK.</span></span>
7. <span data-ttu-id="beda7-113">V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="beda7-113">In the Item number field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="beda7-114">Vyberte skladovou položku.</span><span class="sxs-lookup"><span data-stu-id="beda7-114">Select an inventory item.</span></span> <span data-ttu-id="beda7-115">Například vyberte číslo položky 1000.</span><span class="sxs-lookup"><span data-stu-id="beda7-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="beda7-116">Rozbalte nebo sbalte oddíl Podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="beda7-116">Expand or collapse the Line details section.</span></span>
10. <span data-ttu-id="beda7-117">Klikněte na záložku Nastavení.</span><span class="sxs-lookup"><span data-stu-id="beda7-117">Click the Setup tab.</span></span>
    * <span data-ttu-id="beda7-118">Zásady párování je možné přepsat a párování nepoužít, nebo použít dvoucestné či třícestné párování.</span><span class="sxs-lookup"><span data-stu-id="beda7-118">You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="beda7-119">Rozbalte nebo sbalte oddíl Podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="beda7-119">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="beda7-120">V podokně akcí klikněte na položku Nákup.</span><span class="sxs-lookup"><span data-stu-id="beda7-120">On the Action Pane, click Purchase.</span></span>
13. <span data-ttu-id="beda7-121">Klikněte na tlačítko Potvrdit.</span><span class="sxs-lookup"><span data-stu-id="beda7-121">Click Confirm.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="beda7-122">Příjem produktů</span><span class="sxs-lookup"><span data-stu-id="beda7-122">Receive the products</span></span>
1. <span data-ttu-id="beda7-123">V podokně akcí klikněte na položku Přijmout.</span><span class="sxs-lookup"><span data-stu-id="beda7-123">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="beda7-124">Klikněte na položku Příjemka produktu.</span><span class="sxs-lookup"><span data-stu-id="beda7-124">Click Product receipt.</span></span>
3. <span data-ttu-id="beda7-125">V poli Příjemka produktu zadejte číslo příjemky produktu.</span><span class="sxs-lookup"><span data-stu-id="beda7-125">In the Product receipt field, enter the product receipt number.</span></span> <span data-ttu-id="beda7-126">Zadejte například PR123.</span><span class="sxs-lookup"><span data-stu-id="beda7-126">For example, enter PR123.</span></span>
4. <span data-ttu-id="beda7-127">Kliknutím na tlačítko OK zaúčtujte příjemku produktu.</span><span class="sxs-lookup"><span data-stu-id="beda7-127">Click OK to post the product receipt.</span></span>
5. <span data-ttu-id="beda7-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="beda7-128">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="beda7-129">Vytvoření faktury dodavatele</span><span class="sxs-lookup"><span data-stu-id="beda7-129">Create a vendor invoice</span></span>
1. <span data-ttu-id="beda7-130">Přejděte na Závazky > Nákupní objednávky > Přijaté nákupní objednávky, které nejsou fakturované.</span><span class="sxs-lookup"><span data-stu-id="beda7-130">Go to Accounts payable > Purchase orders > Purchase orders received but not invoiced.</span></span>
2. <span data-ttu-id="beda7-131">Vyberte nákupní objednávku, kterou jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="beda7-131">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="beda7-132">V podokně akcí klikněte na možnost Faktura.</span><span class="sxs-lookup"><span data-stu-id="beda7-132">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="beda7-133">Klepněte na Faktura.</span><span class="sxs-lookup"><span data-stu-id="beda7-133">Click Invoice.</span></span>
5. <span data-ttu-id="beda7-134">Do pole Číslo zadejte číslo faktury.</span><span class="sxs-lookup"><span data-stu-id="beda7-134">In the Number field, enter the invoice number.</span></span>
6. <span data-ttu-id="beda7-135">Do pole Popis faktury zadejte nějakou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="beda7-135">In the Invoice description field, type a value.</span></span>
7. <span data-ttu-id="beda7-136">Do pole Datum faktury zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="beda7-136">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="beda7-137">Zadejte číslo 1200 do pole Jednotková cena.</span><span class="sxs-lookup"><span data-stu-id="beda7-137">In the Unit price field, enter 1200.</span></span>
9. <span data-ttu-id="beda7-138">Klikněte na Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="beda7-138">Click Add line.</span></span>
10. <span data-ttu-id="beda7-139">V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="beda7-139">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="beda7-140">V seznamu najděte číslo položky pro instalační náklady.</span><span class="sxs-lookup"><span data-stu-id="beda7-140">In the list, find the installation charge item number.</span></span> <span data-ttu-id="beda7-141">Například S0001</span><span class="sxs-lookup"><span data-stu-id="beda7-141">For example, S0001</span></span>
12. <span data-ttu-id="beda7-142">Vyberte číslo položky pro instalační náklady.</span><span class="sxs-lookup"><span data-stu-id="beda7-142">Select the installation charge item number.</span></span>
    * <span data-ttu-id="beda7-143">Všimněte si, že od okamžiku, kdy jste změny provedli, nebylo provedeno párování.</span><span class="sxs-lookup"><span data-stu-id="beda7-143">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="beda7-144">Klikněte na položku Aktualizovat stav párování.</span><span class="sxs-lookup"><span data-stu-id="beda7-144">Click Update match status.</span></span>
14. <span data-ttu-id="beda7-145">V podokně akcí klikněte na položku Přehled.</span><span class="sxs-lookup"><span data-stu-id="beda7-145">On the Action Pane, click Review.</span></span>
15. <span data-ttu-id="beda7-146">Klikněte na položku Párování – podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="beda7-146">Click Matching details.</span></span>
    * <span data-ttu-id="beda7-147">Nový řádek se službami se nemusí párovat a stav tak uvádí Neprovedeno.</span><span class="sxs-lookup"><span data-stu-id="beda7-147">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="beda7-148">Vyberte příjemku produktu pro skladovou položku, kterou jste obdrželi.</span><span class="sxs-lookup"><span data-stu-id="beda7-148">Select the product receipt for the inventory item that you received.</span></span>
    * <span data-ttu-id="beda7-149">Řádek s příjemkou produktu byl spárován, ale neodpovídá množství nebo cena, a proto došlo k chybě.</span><span class="sxs-lookup"><span data-stu-id="beda7-149">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="beda7-150">Zadejte číslo do pole Jednotková cena.</span><span class="sxs-lookup"><span data-stu-id="beda7-150">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="beda7-151">Když nyní odpovídá jednotková cena, stav se aktualizuje na Úspěch.</span><span class="sxs-lookup"><span data-stu-id="beda7-151">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="beda7-152">Pokud zásady umožňují nesrovnalosti nebo pokud párování plní pouze funkci upozornění, lze fakturu přesto zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="beda7-152">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="beda7-153">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="beda7-153">Close the page.</span></span>
19. <span data-ttu-id="beda7-154">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="beda7-154">Click Post.</span></span>
20. <span data-ttu-id="beda7-155">Zavřete formulář.</span><span class="sxs-lookup"><span data-stu-id="beda7-155">Close the form.</span></span>
    * <span data-ttu-id="beda7-156">Všimněte si, že nákupní objednávka již není uvedena jako přijatá a nefakturovaná.</span><span class="sxs-lookup"><span data-stu-id="beda7-156">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  


