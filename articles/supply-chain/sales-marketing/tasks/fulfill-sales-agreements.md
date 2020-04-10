---
title: Plnění prodejních smluv
description: Tento postup popisuje, jak plnit prodejní smlouvy přidružením prodejní objednávky.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesTableListPage, SalesTable, AgreementLine, SalesCreateOrder,  SalesEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7e32decdd13cb578c1ac026f25a56b37ff7231a9
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146461"
---
# <a name="fulfill-sales-agreements"></a><span data-ttu-id="44d92-103">Plnění prodejních smluv</span><span class="sxs-lookup"><span data-stu-id="44d92-103">Fulfill sales agreements</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="44d92-104">Tento postup popisuje, jak plnit prodejní smlouvy přidružením prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="44d92-104">This procedure shows you how to fulfill a sales agreement by associating sales orders with it.</span></span> <span data-ttu-id="44d92-105">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="44d92-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="44d92-106">Před spuštěním této příručky, zkontrolujte, že máte platnou prodejní smlouvu typu „Závazek – hodnota produktu“.</span><span class="sxs-lookup"><span data-stu-id="44d92-106">Before starting this guide, make sure you have an effective sales agreement of type "Product value commitment".</span></span> <span data-ttu-id="44d92-107">Případně můžete spustit průvodce úkoly nazvaného „Vytvořit prodejní smlouvy“.</span><span class="sxs-lookup"><span data-stu-id="44d92-107">Alternatively, you can run the task guide called "Create sales agreements".</span></span>  




## <a name="release-a-sales-order-from-the-agreement"></a><span data-ttu-id="44d92-108">Vydání prodejní objednávky ze smlouvy</span><span class="sxs-lookup"><span data-stu-id="44d92-108">Release a sales order from the agreement</span></span>
1. <span data-ttu-id="44d92-109">Přejděte na Prodej a marketing > Prodejní smlouvy > Prodejní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="44d92-109">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="44d92-110">V seznamu otevřete smlouvu, pro kterou chcete vydat objednávku.</span><span class="sxs-lookup"><span data-stu-id="44d92-110">In the list, open the agreement against which you want to release the order.</span></span>
3. <span data-ttu-id="44d92-111">V podokně akcí klepněte na možnost Prodejní smlouva.</span><span class="sxs-lookup"><span data-stu-id="44d92-111">On the Action Pane, click Sales agreement.</span></span>
4. <span data-ttu-id="44d92-112">Klepněte na Dílčí objednávka.</span><span class="sxs-lookup"><span data-stu-id="44d92-112">Click Release order.</span></span>
    * <span data-ttu-id="44d92-113">Jak text v horní části stránky Vytvořit dílčí objednávku bodů zdůrazňuje, podrobnosti požadované pro řádky prodejní objednávky se budou lišit podle toho, zda je dohoda založená na množství nebo na hodnotě.</span><span class="sxs-lookup"><span data-stu-id="44d92-113">As the text on top of the  Create release order page points out, the details required for the sales order lines will differ depending on whether the agreement is quantity- or value-based.</span></span>  
    * <span data-ttu-id="44d92-114">Smlouva v této příručce je typu „Závazek – hodnota produktu“.</span><span class="sxs-lookup"><span data-stu-id="44d92-114">The agreement in this guide is of type "Product value commitment".</span></span> <span data-ttu-id="44d92-115">Proto je oddíl Řádky na této stránce prázdný.</span><span class="sxs-lookup"><span data-stu-id="44d92-115">This is why the Lines section of this page is blank.</span></span> <span data-ttu-id="44d92-116">Pokud by se závazek zakládal na množství, informace řádku by byly zkopírovány ze smlouvy.</span><span class="sxs-lookup"><span data-stu-id="44d92-116">If the commitment was based on quantity, the line information would be copied from the agreement.</span></span>  
5. <span data-ttu-id="44d92-117">Klikněte na položku Vytvořit.</span><span class="sxs-lookup"><span data-stu-id="44d92-117">Click Create.</span></span>
    * <span data-ttu-id="44d92-118">Zpráva vás informuje o tom, že prodejní objednávka byla vytvořena.</span><span class="sxs-lookup"><span data-stu-id="44d92-118">The message informs you that a sales order has been created.</span></span> <span data-ttu-id="44d92-119">Objednávka neobsahuje žádné řádky, a proto je proces uvolnění nutné dokončit přidáním podrobností řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="44d92-119">Since the order does not contain any lines, you must add order line details to complete the release process.</span></span>   
6. <span data-ttu-id="44d92-120">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="44d92-120">Close the page.</span></span>
7. <span data-ttu-id="44d92-121">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="44d92-121">Close the page.</span></span>
8. <span data-ttu-id="44d92-122">Přejděte na Prodej a marketing > Prodejní objednávky > Všechny prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="44d92-122">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
9. <span data-ttu-id="44d92-123">V seznamu vyhledejte a otevřete objednávku, která byla vytvořena jako výsledek vydání objednávky v předchozí úloze.</span><span class="sxs-lookup"><span data-stu-id="44d92-123">In the list, find and open the order that was created as the result of the order release in the previous task.</span></span>
10. <span data-ttu-id="44d92-124">Klikněte na Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="44d92-124">Click Add line.</span></span>
11. <span data-ttu-id="44d92-125">V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="44d92-125">In the Item number field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="44d92-126">Do pole Číslo zboží zadejte nebo vyberte zboží, které je zadáno v přidružené prodejní smlouvě.</span><span class="sxs-lookup"><span data-stu-id="44d92-126">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
13. <span data-ttu-id="44d92-127">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="44d92-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="44d92-128">Ujistěte se, že jste zadali množství, které povede k čisté částce pod hodnotou přidružené prodejní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="44d92-128">Make sure that you enter a quantity that brings the Net amount under the value of the associated sales agreement.</span></span>  
    * <span data-ttu-id="44d92-129">Všimněte si, že když prodejní objednávka je propojena se smlouvou, procento dohodnuté slevy bude použita v řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="44d92-129">Notice that because the sales order is linked to the agreement, the negotiated discount percent is applied to the order line.</span></span>  
14. <span data-ttu-id="44d92-130">Klikněte na položku Aktualizovat řádek.</span><span class="sxs-lookup"><span data-stu-id="44d92-130">Click Update line.</span></span>
15. <span data-ttu-id="44d92-131">Klikněte na položku Připojeno.</span><span class="sxs-lookup"><span data-stu-id="44d92-131">Click Attached.</span></span>
    * <span data-ttu-id="44d92-132">Na stránce připojené smlouvy se zobrazí ID a podmínky smlouvy, ze kterých je řádek vydán.</span><span class="sxs-lookup"><span data-stu-id="44d92-132">The Attached agreement page shows the ID and terms of the agreement from which the line is released.</span></span>  
16. <span data-ttu-id="44d92-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="44d92-133">Close the page.</span></span>
17. <span data-ttu-id="44d92-134">V podokně akcí klikněte na položku Obecné.</span><span class="sxs-lookup"><span data-stu-id="44d92-134">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="44d92-135">Klepněte na Připojená prodejní smlouva.</span><span class="sxs-lookup"><span data-stu-id="44d92-135">Click Attached sales agreement.</span></span>
19. <span data-ttu-id="44d92-136">Rozbalte sekci Podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="44d92-136">Expand the Line details section.</span></span>
20. <span data-ttu-id="44d92-137">Klepněte na kartu Plnění.</span><span class="sxs-lookup"><span data-stu-id="44d92-137">Click the Fulfillment tab.</span></span>
    * <span data-ttu-id="44d92-138">Karta Plnění zobrazuje přehled všech řádků prodejní objednávky, které souvisejí s tímto závazkem a jejich stavem plnění, jakož i částkou nebo množstvím, které ještě nebyly vydány.</span><span class="sxs-lookup"><span data-stu-id="44d92-138">The Fulfillment tab shows a summary of all the sales order lines that are associated with this commitment, and their fulfillment state, as well as the amount or quantity that has not yet been released.</span></span>   
21. <span data-ttu-id="44d92-139">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="44d92-139">Close the page.</span></span>
22. <span data-ttu-id="44d92-140">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="44d92-140">Close the page.</span></span>
23. <span data-ttu-id="44d92-141">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="44d92-141">Close the page.</span></span>

## <a name="apply-sales-agreement-in-the-order-process"></a><span data-ttu-id="44d92-142">Použití prodejní smlouvy v procesu objednávky</span><span class="sxs-lookup"><span data-stu-id="44d92-142">Apply sales agreement in the order process</span></span>
1. <span data-ttu-id="44d92-143">Přejděte na Prodej a marketing > Prodejní objednávky > Všechny prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="44d92-143">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="44d92-144">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="44d92-144">Click New.</span></span>
3. <span data-ttu-id="44d92-145">V poli Účet odběratele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="44d92-145">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="44d92-146">V seznamu vyhledejte a vyberte odběratele určeného v prodejní smlouvě.</span><span class="sxs-lookup"><span data-stu-id="44d92-146">In the list, find and select the customer specified on the sales agreement.</span></span>
5. <span data-ttu-id="44d92-147">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="44d92-147">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="44d92-148">Rozbalte sekci Obecné.</span><span class="sxs-lookup"><span data-stu-id="44d92-148">Expand the General section.</span></span>
7. <span data-ttu-id="44d92-149">V poli ID prodejní smlouvy klepněte na tlačítko rozevíracího seznamu a otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="44d92-149">In the Sales agreement ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="44d92-150">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="44d92-150">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="44d92-151">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="44d92-151">Click Yes.</span></span>
10. <span data-ttu-id="44d92-152">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="44d92-152">Click OK.</span></span>
11. <span data-ttu-id="44d92-153">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="44d92-153">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="44d92-154">V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="44d92-154">In the Item number field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="44d92-155">Do pole Číslo zboží zadejte nebo vyberte zboží, které je zadáno v přidružené prodejní smlouvě.</span><span class="sxs-lookup"><span data-stu-id="44d92-155">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
14. <span data-ttu-id="44d92-156">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="44d92-156">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="44d92-157">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="44d92-157">Click Save.</span></span>
16. <span data-ttu-id="44d92-158">V podokně akcí klikněte na položku Vyskladnit a zabalit.</span><span class="sxs-lookup"><span data-stu-id="44d92-158">On the Action Pane, click Pick and pack.</span></span>
17. <span data-ttu-id="44d92-159">Klikněte na položku Zaúčtovat dodací list.</span><span class="sxs-lookup"><span data-stu-id="44d92-159">Click Post packing slip.</span></span>
18. <span data-ttu-id="44d92-160">Rozbalte sekci Parametry.</span><span class="sxs-lookup"><span data-stu-id="44d92-160">Expand the Parameters section.</span></span>
19. <span data-ttu-id="44d92-161">Vyberte možnost Ano v poli Účtování.</span><span class="sxs-lookup"><span data-stu-id="44d92-161">Select Yes in the Posting field.</span></span>
20. <span data-ttu-id="44d92-162">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="44d92-162">Click OK.</span></span>
21. <span data-ttu-id="44d92-163">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="44d92-163">Click OK.</span></span>
22. <span data-ttu-id="44d92-164">V podokně akcí klikněte na položku Obecné.</span><span class="sxs-lookup"><span data-stu-id="44d92-164">On the Action Pane, click General.</span></span>
23. <span data-ttu-id="44d92-165">Klepněte na Připojená prodejní smlouva.</span><span class="sxs-lookup"><span data-stu-id="44d92-165">Click Attached sales agreement.</span></span>
24. <span data-ttu-id="44d92-166">Klepněte na kartu Plnění.</span><span class="sxs-lookup"><span data-stu-id="44d92-166">Click the Fulfillment tab.</span></span>

