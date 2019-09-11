---
title: Vytvoření žádanky používající požadavek na nabídku
description: Toto téma popisuje postup přidání informací o ceně a dodavateli do nákupní žádanky z procesu požadavku na nabídku.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4429bda6efddbb4f1fa7da06e91e51d885919c05
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914947"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="721ee-103">Vytvoření žádanky používající požadavek na nabídku</span><span class="sxs-lookup"><span data-stu-id="721ee-103">Create a requisition that uses an RFQ</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="721ee-104">Toto téma popisuje postup přidání informací o ceně a dodavateli do nákupní žádanky z procesu požadavku na nabídku.</span><span class="sxs-lookup"><span data-stu-id="721ee-104">This topic explains how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="721ee-105">Příklad uvedený v tomto průvodci lze použít u ukázkových dat společnosti USMF, a vy musíte být k dokončení všech kroků přihlášeni jako správce.</span><span class="sxs-lookup"><span data-stu-id="721ee-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="721ee-106">Úkoly v této příručce obvykle provádí odborníci v oblasti zásobování.</span><span class="sxs-lookup"><span data-stu-id="721ee-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="721ee-107">Vytvoření žádanky</span><span class="sxs-lookup"><span data-stu-id="721ee-107">Create a requisition</span></span>
1. <span data-ttu-id="721ee-108">V navigačním podokně přejděte na **Moduly > Zásobování a zdroje > Nákupní žádanky > Mnou připravené nákupní žádanky**.</span><span class="sxs-lookup"><span data-stu-id="721ee-108">In the navigation pane, go to **Modules > Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me**.</span></span>
2. <span data-ttu-id="721ee-109">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="721ee-109">Select **New**.</span></span>
3. <span data-ttu-id="721ee-110">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="721ee-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="721ee-111">Zadejte datum do pole **Požadované datum**.</span><span class="sxs-lookup"><span data-stu-id="721ee-111">In the **Requested date** field, enter a date.</span></span>
5. <span data-ttu-id="721ee-112">Zadejte datum do pole **Datum účtování**.</span><span class="sxs-lookup"><span data-stu-id="721ee-112">In the **Accounting date** field, enter a date.</span></span>
6. <span data-ttu-id="721ee-113">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="721ee-113">Select **OK**.</span></span>
7. <span data-ttu-id="721ee-114">V poli **Důvod** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="721ee-114">In the **Reason** field, enter or select a value.</span></span>
8. <span data-ttu-id="721ee-115">Vyberte **Přidat řádek**.</span><span class="sxs-lookup"><span data-stu-id="721ee-115">Select **Add line**.</span></span>
9. <span data-ttu-id="721ee-116">V poli **Kategorie zásobování** vyberte ve stromové struktuře kategorii a zvolte **OK**.</span><span class="sxs-lookup"><span data-stu-id="721ee-116">In the **Procurement category** field, select a category in the tree, and then select **OK**.</span></span>
10. <span data-ttu-id="721ee-117">Do pole **Název produktu** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="721ee-117">In the **Product name** field, type a value.</span></span>
11. <span data-ttu-id="721ee-118">Zadejte číslo do pole **Množství**.</span><span class="sxs-lookup"><span data-stu-id="721ee-118">In the **Quantity** field, enter a number.</span></span>
12. <span data-ttu-id="721ee-119">V poli **Jednotka** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="721ee-119">In the **Unit** field, enter or select a value.</span></span>
13. <span data-ttu-id="721ee-120">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="721ee-120">Select **Save**.</span></span>
14. <span data-ttu-id="721ee-121">Kliknutím na možnost **Workflow** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="721ee-121">Select **Workflow** to open the drop dialog.</span></span>
15. <span data-ttu-id="721ee-122">Vyberte **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="721ee-122">Select **Submit**.</span></span>
16. <span data-ttu-id="721ee-123">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="721ee-123">Close the page.</span></span>
17. <span data-ttu-id="721ee-124">Vyberte **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="721ee-124">Select **Submit**.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="721ee-125">Znovu přiřadit úlohu do workflowu</span><span class="sxs-lookup"><span data-stu-id="721ee-125">Reassign a workflow task</span></span>
<span data-ttu-id="721ee-126">Další úkol je vytvořit požadavek na nabídku pro získání nabídek na váš produkt od dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="721ee-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="721ee-127">V ukázkových datech společnosti USMF je workflow žádanky nastaven s pravidlem. Díky tomu pokud dodavatel není vybrán, nebo je jednotková cena na řádku 0, úloha se přiřadí ke konkrétnímu pracovníkovi s cílem vytvořit požadavek na nabídku.</span><span class="sxs-lookup"><span data-stu-id="721ee-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="721ee-128">Chcete-li pokračovat v této příručce, je nutné změnit přiřazení daného úkolu jinému uživateli (vám).</span><span class="sxs-lookup"><span data-stu-id="721ee-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="721ee-129">To můžete provést jen po přihlášení jako správce.</span><span class="sxs-lookup"><span data-stu-id="721ee-129">You can only do this if you are logged in as an Admin.</span></span>  

1. <span data-ttu-id="721ee-130">Kliknutím na možnost **Workflow** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="721ee-130">Select **Workflow** to open the drop dialog.</span></span>
2. <span data-ttu-id="721ee-131">Zvolte **Zobrazit historii**.</span><span class="sxs-lookup"><span data-stu-id="721ee-131">Select **View history**.</span></span>
3. <span data-ttu-id="721ee-132">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="721ee-132">Refresh the page.</span></span>
4. <span data-ttu-id="721ee-133">Rozbalte část **Sledování podrobností**.</span><span class="sxs-lookup"><span data-stu-id="721ee-133">Expand the **Tracking details** section.</span></span>
5. <span data-ttu-id="721ee-134">Ve stromovém zobrazení vyberte řádek začínající na „Workflow řádku bylo aktivováno v“.</span><span class="sxs-lookup"><span data-stu-id="721ee-134">In the tree, select the line that starts with “Line workflow activated on”.</span></span>
6. <span data-ttu-id="721ee-135">Zvolte **Zobrazit podrobnosti workflowu**.</span><span class="sxs-lookup"><span data-stu-id="721ee-135">Select **View workflow details**.</span></span>
7. <span data-ttu-id="721ee-136">Rozbalte sekci **Pracovní položky**.</span><span class="sxs-lookup"><span data-stu-id="721ee-136">Expand the **Work items** section.</span></span>
8. <span data-ttu-id="721ee-137">Vyberte **Opětovně přiřadit**.</span><span class="sxs-lookup"><span data-stu-id="721ee-137">Select **Reassign**.</span></span>
9. <span data-ttu-id="721ee-138">V poli **Uživatel** vyberte možnost **Správce**.</span><span class="sxs-lookup"><span data-stu-id="721ee-138">In the **User** field, select **Admin**.</span></span>
10. <span data-ttu-id="721ee-139">Vyberte **Opětovně přiřadit**.</span><span class="sxs-lookup"><span data-stu-id="721ee-139">Select **Reassign**.</span></span>
11. <span data-ttu-id="721ee-140">Zavřete dvě stránky.</span><span class="sxs-lookup"><span data-stu-id="721ee-140">Close the two pages.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="721ee-141">Vytvoření požadavku na nabídku</span><span class="sxs-lookup"><span data-stu-id="721ee-141">Create an RFQ</span></span>

1. <span data-ttu-id="721ee-142">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="721ee-142">Refresh the page.</span></span>
2. <span data-ttu-id="721ee-143">Zvolte **Požadavek na nabídku**.</span><span class="sxs-lookup"><span data-stu-id="721ee-143">Select **Request for quotation**.</span></span>
3. <span data-ttu-id="721ee-144">V poli **Kupující právnická osoba** vyberte možnost **USMF**.</span><span class="sxs-lookup"><span data-stu-id="721ee-144">In the **Buying legal entity** field, select **USMF**.</span></span> <span data-ttu-id="721ee-145">Je nutné vybrat stejnou právnickou osobu, která je uvedena na řádku požadavku.</span><span class="sxs-lookup"><span data-stu-id="721ee-145">You must select the same legal entity that’s on the requisition line.</span></span>  
4. <span data-ttu-id="721ee-146">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="721ee-146">In the list, mark the selected row.</span></span> <span data-ttu-id="721ee-147">Pokud máte více řádků v nákupní žádance, vyberte všechny řádky, které chcete přidat do požadavku na nabídku.</span><span class="sxs-lookup"><span data-stu-id="721ee-147">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="721ee-148">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="721ee-148">Select **OK**.</span></span>
6. <span data-ttu-id="721ee-149">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="721ee-149">Refresh the page.</span></span>
7. <span data-ttu-id="721ee-150">Zajistěte, že je otevřené okno s fakty, a rozbalte oddíl **Související dokumenty**.</span><span class="sxs-lookup"><span data-stu-id="721ee-150">Ensure that the FactBox is open, then expand the **Related documents** section.</span></span>
8. <span data-ttu-id="721ee-151">Zvolte odkaz v poli **Požadavek na nabídku** a otevřete tak požadavek na nabídku, který jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="721ee-151">Select the link in the **Request for quotation** field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="721ee-152">Vyberte **Záhlaví**.</span><span class="sxs-lookup"><span data-stu-id="721ee-152">Select **Header**.</span></span>
10. <span data-ttu-id="721ee-153">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="721ee-153">Select **Add**.</span></span>
11. <span data-ttu-id="721ee-154">V poli **Účet dodavatele** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="721ee-154">In the **Vendor account** field, enter or select a value.</span></span>
12. <span data-ttu-id="721ee-155">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="721ee-155">Select **Add**.</span></span>
13. <span data-ttu-id="721ee-156">V poli **Účet dodavatele** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="721ee-156">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="721ee-157">Zvolte **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="721ee-157">Select **Send**.</span></span>
15. <span data-ttu-id="721ee-158">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="721ee-158">Select **OK**.</span></span>
16. <span data-ttu-id="721ee-159">Vyberte **Zadat odpověď**.</span><span class="sxs-lookup"><span data-stu-id="721ee-159">Select **Enter reply**.</span></span>
17. <span data-ttu-id="721ee-160">V podokně akcí zvolte **Odpovědět**.</span><span class="sxs-lookup"><span data-stu-id="721ee-160">On the Action Pane, select **Reply**.</span></span>
18. <span data-ttu-id="721ee-161">Zvolte **Kopírovat data do odpovědi**.</span><span class="sxs-lookup"><span data-stu-id="721ee-161">Select **Copy data to reply**.</span></span> <span data-ttu-id="721ee-162">Dojde tak ke zkopírování dat, jako je množství a data, z požadavku na nabídku do odpovědi.</span><span class="sxs-lookup"><span data-stu-id="721ee-162">This copies data, such as the quantity and dates, from the RFQ to the reply.</span></span>  
19. <span data-ttu-id="721ee-163">Zadejte číslo do pole **Jednotková cena**.</span><span class="sxs-lookup"><span data-stu-id="721ee-163">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="721ee-164">Jedná se o cenu, kterou jste obdrželi od dodavatele.</span><span class="sxs-lookup"><span data-stu-id="721ee-164">This is the price that you’ve received from the vendor.</span></span> <span data-ttu-id="721ee-165">Můžete také zadat doplňující informace od dodavatele.</span><span class="sxs-lookup"><span data-stu-id="721ee-165">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="721ee-166">Zvolte **Přijmout**.</span><span class="sxs-lookup"><span data-stu-id="721ee-166">Select **Accept**.</span></span>
21. <span data-ttu-id="721ee-167">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="721ee-167">Select **OK**.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="721ee-168">Ověřte, že dodavatel a cena byly převedeny do požadavku</span><span class="sxs-lookup"><span data-stu-id="721ee-168">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="721ee-169">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="721ee-169">Close the page.</span></span>
2. <span data-ttu-id="721ee-170">Vybrat **řádky**.</span><span class="sxs-lookup"><span data-stu-id="721ee-170">Select **Lines**.</span></span>
3. <span data-ttu-id="721ee-171">Vyberte **Související informace**.</span><span class="sxs-lookup"><span data-stu-id="721ee-171">Select **Related information**.</span></span>
4. <span data-ttu-id="721ee-172">Zvolte **Nákupní žádanka**.</span><span class="sxs-lookup"><span data-stu-id="721ee-172">Select **Purchase requisition**.</span></span>
5. <span data-ttu-id="721ee-173">Vyberte řádek, který byl převeden na požadavek na nabídku.</span><span class="sxs-lookup"><span data-stu-id="721ee-173">Select the line that was transferred to the RFQ.</span></span> <span data-ttu-id="721ee-174">Ověřte, že cena i dodavatel byly zkopírováni do žádanky.</span><span class="sxs-lookup"><span data-stu-id="721ee-174">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="721ee-175">Kliknutím na možnost **Workflow** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="721ee-175">Select **Workflow** to open the drop dialog.</span></span>
7. <span data-ttu-id="721ee-176">Zvolte Dokončeno.</span><span class="sxs-lookup"><span data-stu-id="721ee-176">Select Complete.</span></span>
8. <span data-ttu-id="721ee-177">Vyberte stránku.</span><span class="sxs-lookup"><span data-stu-id="721ee-177">Select the page.</span></span>
9. <span data-ttu-id="721ee-178">Zvolte Dokončeno.</span><span class="sxs-lookup"><span data-stu-id="721ee-178">Select Complete.</span></span>

