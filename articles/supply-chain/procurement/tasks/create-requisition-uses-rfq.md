---
title: Vytvoření žádanky používající požadavek na nabídku
description: Tato příručka popisuje postup přidání informací o ceně a dodavateli do nákupní žádanky z procesu požadavku na nabídku.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a9418b526f992008086f10ce78e95cb682bc164
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547392"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="341ca-103">Vytvoření žádanky používající požadavek na nabídku</span><span class="sxs-lookup"><span data-stu-id="341ca-103">Create a requisition that uses an RFQ</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="341ca-104">Tato příručka popisuje postup přidání informací o ceně a dodavateli do nákupní žádanky z procesu požadavku na nabídku.</span><span class="sxs-lookup"><span data-stu-id="341ca-104">This guide shows how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="341ca-105">Příklad uvedený v tomto průvodci lze použít u ukázkových dat společnosti USMF, a vy musíte být k dokončení všech kroků přihlášeni jako správce.</span><span class="sxs-lookup"><span data-stu-id="341ca-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="341ca-106">Úkoly v této příručce obvykle provádí odborníci v oblasti zásobování.</span><span class="sxs-lookup"><span data-stu-id="341ca-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="341ca-107">Vytvoření žádanky</span><span class="sxs-lookup"><span data-stu-id="341ca-107">Create a requisition</span></span>
1. <span data-ttu-id="341ca-108">Přejděte do nabídky Zásobování a zdroje > Nákupní žádanky > Nákupní žádanky připravené mnou.</span><span class="sxs-lookup"><span data-stu-id="341ca-108">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="341ca-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="341ca-109">Click New.</span></span>
3. <span data-ttu-id="341ca-110">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="341ca-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="341ca-111">Zadejte datum do pole Požadované datum.</span><span class="sxs-lookup"><span data-stu-id="341ca-111">In the Requested date field, enter a date.</span></span>
5. <span data-ttu-id="341ca-112">Zadejte datum do pole Datum účtování.</span><span class="sxs-lookup"><span data-stu-id="341ca-112">In the Accounting date field, enter a date.</span></span>
6. <span data-ttu-id="341ca-113">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="341ca-113">Click OK.</span></span>
7. <span data-ttu-id="341ca-114">V poli Důvod zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="341ca-114">In the Reason field, enter or select a value.</span></span>
8. <span data-ttu-id="341ca-115">Klikněte na položku Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="341ca-115">Click Add line.</span></span>
9. <span data-ttu-id="341ca-116">V poli Kategorie zásobování vyberte ve stromové struktuře kategorii a klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="341ca-116">In the Procurement category field, select a category in the tree, and then click OK.</span></span>
10. <span data-ttu-id="341ca-117">Do pole Název produktu zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="341ca-117">In the Product name field, type a value.</span></span>
11. <span data-ttu-id="341ca-118">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="341ca-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="341ca-119">V poli Jednotka zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="341ca-119">In the Unit field, enter or select a value.</span></span>
13. <span data-ttu-id="341ca-120">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="341ca-120">Click Save.</span></span>
14. <span data-ttu-id="341ca-121">Kliknutím na možnost Workflow otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="341ca-121">Click Workflow to open the drop dialog.</span></span>
15. <span data-ttu-id="341ca-122">Klepněte na tlačítko Odeslat.</span><span class="sxs-lookup"><span data-stu-id="341ca-122">Click Submit.</span></span>
16. <span data-ttu-id="341ca-123">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="341ca-123">Close the page.</span></span>
17. <span data-ttu-id="341ca-124">Klepněte na tlačítko Odeslat.</span><span class="sxs-lookup"><span data-stu-id="341ca-124">Click Submit.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="341ca-125">Znovu přiřadit úlohu do workflowu</span><span class="sxs-lookup"><span data-stu-id="341ca-125">Reassign a workflow task</span></span>
    * <span data-ttu-id="341ca-126">Další úkol je vytvořit požadavek na nabídku pro získání nabídek na váš produkt od dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="341ca-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="341ca-127">V ukázkových datech společnosti USMF je workflow žádanky nastaven s pravidlem. Díky tomu pokud dodavatel není vybrán, nebo je jednotková cena na řádku 0, úloha se přiřadí ke konkrétnímu pracovníkovi s cílem vytvořit požadavek na nabídku.</span><span class="sxs-lookup"><span data-stu-id="341ca-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="341ca-128">Chcete-li pokračovat v této příručce, je nutné změnit přiřazení daného úkolu jinému uživateli (vám).</span><span class="sxs-lookup"><span data-stu-id="341ca-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="341ca-129">To můžete provést jen po přihlášení jako správce.</span><span class="sxs-lookup"><span data-stu-id="341ca-129">You can only do this if you are logged in as an Admin.</span></span>  
1. <span data-ttu-id="341ca-130">Kliknutím na možnost Workflow otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="341ca-130">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="341ca-131">Klikněte na Zobrazit historii.</span><span class="sxs-lookup"><span data-stu-id="341ca-131">Click View history.</span></span>
3. <span data-ttu-id="341ca-132">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="341ca-132">Refresh the page.</span></span>
4. <span data-ttu-id="341ca-133">Rozbalte část Sledování podrobností.</span><span class="sxs-lookup"><span data-stu-id="341ca-133">Expand the Tracking details section.</span></span>
5. <span data-ttu-id="341ca-134">Ve stromovém zobrazení vyberte „řádek začínající na Workflow řádku byl aktivován v“.</span><span class="sxs-lookup"><span data-stu-id="341ca-134">In the tree, select 'the line that starts with “Line workflow activated on”'.</span></span>
6. <span data-ttu-id="341ca-135">Klikněte na Zobrazit podrobnosti workflowu.</span><span class="sxs-lookup"><span data-stu-id="341ca-135">Click View workflow details.</span></span>
7. <span data-ttu-id="341ca-136">Rozbalte sekci Pracovní položky.</span><span class="sxs-lookup"><span data-stu-id="341ca-136">Expand the Work items section.</span></span>
8. <span data-ttu-id="341ca-137">Klepněte na tlačítko Změnit přiřazení.</span><span class="sxs-lookup"><span data-stu-id="341ca-137">Click Reassign.</span></span>
9. <span data-ttu-id="341ca-138">V poli Uživatel vyberte možnost Správce.</span><span class="sxs-lookup"><span data-stu-id="341ca-138">In the User field, select Admin.</span></span>
10. <span data-ttu-id="341ca-139">Klepněte na tlačítko Změnit přiřazení.</span><span class="sxs-lookup"><span data-stu-id="341ca-139">Click Reassign.</span></span>
11. <span data-ttu-id="341ca-140">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="341ca-140">Close the page.</span></span>
12. <span data-ttu-id="341ca-141">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="341ca-141">Close the page.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="341ca-142">Vytvoření požadavku na nabídku</span><span class="sxs-lookup"><span data-stu-id="341ca-142">Create an RFQ</span></span>
1. <span data-ttu-id="341ca-143">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="341ca-143">Refresh the page.</span></span>
2. <span data-ttu-id="341ca-144">Klikněte na Požadavek na nabídku.</span><span class="sxs-lookup"><span data-stu-id="341ca-144">Click Request for quotation.</span></span>
3. <span data-ttu-id="341ca-145">V poli Kupující právnická osoba vyberte možnost USMF.</span><span class="sxs-lookup"><span data-stu-id="341ca-145">In the Buying legal entity field, select USMF.</span></span>
    * <span data-ttu-id="341ca-146">Je nutné vybrat stejnou právnickou osobu, která je uvedena na řádku požadavku.</span><span class="sxs-lookup"><span data-stu-id="341ca-146">You must select the same legal entity that’s on the requisition line.</span></span>  
4. <span data-ttu-id="341ca-147">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="341ca-147">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="341ca-148">Pokud máte více řádků v nákupní žádance, vyberte všechny řádky, které chcete přidat do požadavku na nabídku.</span><span class="sxs-lookup"><span data-stu-id="341ca-148">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="341ca-149">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="341ca-149">Click OK.</span></span>
6. <span data-ttu-id="341ca-150">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="341ca-150">Refresh the page.</span></span>
7. <span data-ttu-id="341ca-151">Otevřete okno s fakty a rozbalte oddíl Související dokumenty.</span><span class="sxs-lookup"><span data-stu-id="341ca-151">Open the FactBox and then expand the Related documents section.</span></span>
    * <span data-ttu-id="341ca-152">Okno s fakty je již pravděpodobně otevřené.</span><span class="sxs-lookup"><span data-stu-id="341ca-152">You may already have the FactBox open.</span></span> <span data-ttu-id="341ca-153">Vyhledejte ikonu se šipkou napravo od tlačítka Přepnout řádky a záhlaví.</span><span class="sxs-lookup"><span data-stu-id="341ca-153">Look for the icon with an arrow on it, to the right of the Lines/Header toggle buttons.</span></span> <span data-ttu-id="341ca-154">Pokud šipka ukazuje vpravo, okno s fakty je již otevřeno.</span><span class="sxs-lookup"><span data-stu-id="341ca-154">If the arrow is pointing to the right, the FactBox is already open.</span></span> <span data-ttu-id="341ca-155">Pokud šipka ukazuje doleva, kliknutím na ni okno s fakty otevřete.</span><span class="sxs-lookup"><span data-stu-id="341ca-155">If the arrow points to the left, click it to open the FactBox.</span></span>  
8. <span data-ttu-id="341ca-156">Klepněte na odkaz v poli Požadavek na nabídku a otevřete tak požadavek na nabídku, který jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="341ca-156">Click the link in the Request for quotation field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="341ca-157">Klikněte na Záhlaví.</span><span class="sxs-lookup"><span data-stu-id="341ca-157">Click Header.</span></span>
10. <span data-ttu-id="341ca-158">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="341ca-158">Click Add.</span></span>
11. <span data-ttu-id="341ca-159">V poli Účet dodavatele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="341ca-159">In the Vendor account field, enter or select a value.</span></span>
12. <span data-ttu-id="341ca-160">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="341ca-160">Click Add.</span></span>
13. <span data-ttu-id="341ca-161">V poli Účet dodavatele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="341ca-161">In the Vendor account field, enter or select a value.</span></span>
14. <span data-ttu-id="341ca-162">Klepněte na tlačítko Odeslat.</span><span class="sxs-lookup"><span data-stu-id="341ca-162">Click Send.</span></span>
15. <span data-ttu-id="341ca-163">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="341ca-163">Click OK.</span></span>
16. <span data-ttu-id="341ca-164">Klikněte na Zadat odpověď.</span><span class="sxs-lookup"><span data-stu-id="341ca-164">Click Enter reply.</span></span>
17. <span data-ttu-id="341ca-165">V podokně akcí klikněte na možnost Odpovědět.</span><span class="sxs-lookup"><span data-stu-id="341ca-165">On the Action Pane, click Reply.</span></span>
18. <span data-ttu-id="341ca-166">Klikněte na Kopírovat data do odpovědi.</span><span class="sxs-lookup"><span data-stu-id="341ca-166">Click Copy data to reply.</span></span>
    * <span data-ttu-id="341ca-167">Dojde tak ke zkopírování dat, jako je množství a data, z požadavku na nabídku do odpovědi.</span><span class="sxs-lookup"><span data-stu-id="341ca-167">This copies data, such as the quantity and dates, from the RFQ to the reply .</span></span>  
19. <span data-ttu-id="341ca-168">Zadejte číslo do pole Jednotková cena.</span><span class="sxs-lookup"><span data-stu-id="341ca-168">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="341ca-169">Jedná se o cenu, kterou jste obdrželi od dodavatele.</span><span class="sxs-lookup"><span data-stu-id="341ca-169">This is the price that you’ve received from the vendor.</span></span> <span data-ttu-id="341ca-170">Můžete také zadat doplňující informace od dodavatele.</span><span class="sxs-lookup"><span data-stu-id="341ca-170">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="341ca-171">Klepněte na možnost Akceptovat.</span><span class="sxs-lookup"><span data-stu-id="341ca-171">Click Accept.</span></span>
21. <span data-ttu-id="341ca-172">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="341ca-172">Click OK.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="341ca-173">Ověřte, že dodavatel a cena byly převedeny do požadavku</span><span class="sxs-lookup"><span data-stu-id="341ca-173">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="341ca-174">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="341ca-174">Close the page.</span></span>
2. <span data-ttu-id="341ca-175">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="341ca-175">Click Lines.</span></span>
3. <span data-ttu-id="341ca-176">Klepněte na položku Související informace.</span><span class="sxs-lookup"><span data-stu-id="341ca-176">Click Related information.</span></span>
4. <span data-ttu-id="341ca-177">Klikněte na Nákupní žádanka.</span><span class="sxs-lookup"><span data-stu-id="341ca-177">Click Purchase requisition.</span></span>
5. <span data-ttu-id="341ca-178">Vyberte řádek, který byl převeden na požadavek na nabídku.</span><span class="sxs-lookup"><span data-stu-id="341ca-178">Select the line that was transferred to the RFQ.</span></span>
    * <span data-ttu-id="341ca-179">Ověřte, že cena i dodavatel byly zkopírováni do žádanky.</span><span class="sxs-lookup"><span data-stu-id="341ca-179">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="341ca-180">Kliknutím na možnost Workflow otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="341ca-180">Click Workflow to open the drop dialog.</span></span>
7. <span data-ttu-id="341ca-181">Klikněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="341ca-181">Click Complete.</span></span>
8. <span data-ttu-id="341ca-182">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="341ca-182">Close the page.</span></span>
9. <span data-ttu-id="341ca-183">Klikněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="341ca-183">Click Complete.</span></span>

