--- 
title: "Zadání dat faktury do systému závazků s použitím evidence faktur"
description: "Tento průvodce úkolem popisuje postup použití registru faktur k vytvoření faktur."
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
ms.openlocfilehash: a1273593f221963064c15a6404d4d92453f69d40
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="36635-103">Zadání dat faktury do systému závazků s použitím evidence faktur</span><span class="sxs-lookup"><span data-stu-id="36635-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="36635-104">Tento průvodce úkolem popisuje postup použití registru faktur k vytvoření faktur.</span><span class="sxs-lookup"><span data-stu-id="36635-104">This task guide will show you how to use the invoice register to create invoices.</span></span>  <span data-ttu-id="36635-105">Potom použije evidenci faktur pro spárování faktury s nákupní objednávkou a dokončení výdajů na stránce faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="36635-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="36635-106">Vytvoření nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="36635-106">Create a purchase order</span></span>
1. <span data-ttu-id="36635-107">Přejděte na Závazky > Nákupní objednávky > Nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="36635-107">Go to Accounts payable > Purchase orders > Purchase orders.</span></span>
2. <span data-ttu-id="36635-108">Klepnutím na příkaz Nový vytvořte nákupní objednávku.</span><span class="sxs-lookup"><span data-stu-id="36635-108">Click New to create a purchase order.</span></span>
3. <span data-ttu-id="36635-109">V poli Účet dodavatele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="36635-109">In the Vendor account field, click the drop down button to open the lookup.</span></span>
4. <span data-ttu-id="36635-110">Vyberte dodavatele ze seznamu.</span><span class="sxs-lookup"><span data-stu-id="36635-110">Select the vendor from the list.</span></span> <span data-ttu-id="36635-111">Příklad dodavatele 1001.</span><span class="sxs-lookup"><span data-stu-id="36635-111">For example, vendor 1001.</span></span>
5. <span data-ttu-id="36635-112">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="36635-112">Click OK.</span></span>
6. <span data-ttu-id="36635-113">V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="36635-113">In the Item number field, click the drop down button to open the lookup.</span></span>
7. <span data-ttu-id="36635-114">najděte v seznamu číslo položky služby.</span><span class="sxs-lookup"><span data-stu-id="36635-114">Find the services item number in the list.</span></span> <span data-ttu-id="36635-115">Vyberte například S0001.</span><span class="sxs-lookup"><span data-stu-id="36635-115">For example, select S0001.</span></span>
8. <span data-ttu-id="36635-116">Klepněte číslo položky a vyberte je.</span><span class="sxs-lookup"><span data-stu-id="36635-116">Click on the item number and select it.</span></span>
    * <span data-ttu-id="36635-117">Čistá částka je 75,00.</span><span class="sxs-lookup"><span data-stu-id="36635-117">The net amount is 75.00.</span></span>  <span data-ttu-id="36635-118">Jedná se o částku, která se očekává na faktuře.</span><span class="sxs-lookup"><span data-stu-id="36635-118">That is the amount that we will expect on the invoice.</span></span>  
9. <span data-ttu-id="36635-119">V podokně akcí klikněte na možnost Zakoupit.</span><span class="sxs-lookup"><span data-stu-id="36635-119">On the action pane, click Purchase.</span></span>
10. <span data-ttu-id="36635-120">Klikněte na tlačítko Potvrdit.</span><span class="sxs-lookup"><span data-stu-id="36635-120">Click Confirm.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="36635-121">Vytvoření a zaúčtování faktury</span><span class="sxs-lookup"><span data-stu-id="36635-121">Create and post and invoice</span></span>
1. <span data-ttu-id="36635-122">Přejděte na Závazky > Faktury > Registr faktur.</span><span class="sxs-lookup"><span data-stu-id="36635-122">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="36635-123">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="36635-123">Click New.</span></span>
3. <span data-ttu-id="36635-124">Otevřete vyhledávání a vyberte název registru faktury, který chcete použít.</span><span class="sxs-lookup"><span data-stu-id="36635-124">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="36635-125">Vyberte název registru faktury, který chcete použít.</span><span class="sxs-lookup"><span data-stu-id="36635-125">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="36635-126">Kliknutím na Řádky otevřete registr a zadejte řádky výdajů.</span><span class="sxs-lookup"><span data-stu-id="36635-126">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="36635-127">Ve vyhledávání vyberte dodavatele.</span><span class="sxs-lookup"><span data-stu-id="36635-127">In the lookup, select a vendor.</span></span> <span data-ttu-id="36635-128">Například klepněte na dodavatele 1001.</span><span class="sxs-lookup"><span data-stu-id="36635-128">For example, click on vendor 1001.</span></span>
7. <span data-ttu-id="36635-129">Do pole Faktura zadejte číslo faktury.</span><span class="sxs-lookup"><span data-stu-id="36635-129">In the Invoice field, enter the invoice number.</span></span>
8. <span data-ttu-id="36635-130">Zadejte hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="36635-130">In the Description field, type a value.</span></span>
9. <span data-ttu-id="36635-131">V poli Dobropis zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="36635-131">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="36635-132">V poli Nákupní objednávka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="36635-132">In the Purchase order field, click the drop down button to open the lookup.</span></span>
11. <span data-ttu-id="36635-133">Vyberte nákupní objednávku, kterou jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="36635-133">Select the purchase order that you created earlier.</span></span>
12. <span data-ttu-id="36635-134">V poli Schválil(a) kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="36635-134">In the Approved by field, click the drop down button to open the lookup.</span></span>
13. <span data-ttu-id="36635-135">Vyberte schvalujícího a kliknutím na tlačítko Vybrat tohoto schvalovatele vyberte.</span><span class="sxs-lookup"><span data-stu-id="36635-135">Highlight an approver and click Select to select that approver.</span></span>
14. <span data-ttu-id="36635-136">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="36635-136">Click Post.</span></span>
15. <span data-ttu-id="36635-137">Zavřete formulář.</span><span class="sxs-lookup"><span data-stu-id="36635-137">Close the form.</span></span>
16. <span data-ttu-id="36635-138">Zavřete formulář.</span><span class="sxs-lookup"><span data-stu-id="36635-138">Close the form.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="36635-139">otevřete fakturu z evidence a spárujte ji s nákupní objednávkou pro dokončení procesu fakturace</span><span class="sxs-lookup"><span data-stu-id="36635-139">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="36635-140">Přejděte na Závazky > Faktury > Evidence faktur.</span><span class="sxs-lookup"><span data-stu-id="36635-140">Go to Accounts payable > Invoices > Invoice pool.</span></span>
2. <span data-ttu-id="36635-141">Kliknutím na nákupní objednávku vytvořte fakturu dodavatele z faktury v evidenci.</span><span class="sxs-lookup"><span data-stu-id="36635-141">Click Purchase order to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="36635-142">Vyberte fakturu, kterou chcete zkontrolovat.</span><span class="sxs-lookup"><span data-stu-id="36635-142">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="36635-143">Klepnutím na tlačítko Aktualizovat stav párování dokončete párování.</span><span class="sxs-lookup"><span data-stu-id="36635-143">Click Update match status to complete the matching.</span></span>
5. <span data-ttu-id="36635-144">V podokně akcí klikněte na Možnosti.</span><span class="sxs-lookup"><span data-stu-id="36635-144">On the action pane, click Options.</span></span>
6. <span data-ttu-id="36635-145">Klikněte na tlačítko Změnit zobrazení.</span><span class="sxs-lookup"><span data-stu-id="36635-145">Click Change view.</span></span>
7. <span data-ttu-id="36635-146">Klikněte na Zobrazení mřížky.</span><span class="sxs-lookup"><span data-stu-id="36635-146">Click Grid view.</span></span>
8. <span data-ttu-id="36635-147">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="36635-147">Click Post.</span></span>
9. <span data-ttu-id="36635-148">Zavřete formulář.</span><span class="sxs-lookup"><span data-stu-id="36635-148">Close the form.</span></span>
10. <span data-ttu-id="36635-149">Přejděte do části Závazky > Dodavatelé > Dodavatelé.</span><span class="sxs-lookup"><span data-stu-id="36635-149">Go to Accounts payable > Vendors > Vendors.</span></span>
11. <span data-ttu-id="36635-150">Vyberte dodavatele, který se nacházel na nákupní objednávce.</span><span class="sxs-lookup"><span data-stu-id="36635-150">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="36635-151">Vyberte například dodavatele 1001.</span><span class="sxs-lookup"><span data-stu-id="36635-151">For example, select vendor 1001.</span></span>
12. <span data-ttu-id="36635-152">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="36635-152">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="36635-153">V podokně akcí klikněte na možnost Dodavatel.</span><span class="sxs-lookup"><span data-stu-id="36635-153">On the action pane, click Vendor.</span></span>
14. <span data-ttu-id="36635-154">Klikněte na Transakce.</span><span class="sxs-lookup"><span data-stu-id="36635-154">Click Transactions.</span></span>
15. <span data-ttu-id="36635-155">Vyberte fakturu, kterou jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="36635-155">Select the invoice that you created.</span></span>
    * <span data-ttu-id="36635-156">Časové rozlišení registru faktur bylo stornováno a zaúčtováno na příslušný účet výdajů.</span><span class="sxs-lookup"><span data-stu-id="36635-156">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  


