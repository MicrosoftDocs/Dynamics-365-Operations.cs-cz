---
title: Transakce záruční listiny
description: Tato procedura vás provede procesem Záruční listina.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05abad6898c2b97cf66abdff21b30407dacd6488
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141780"
---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="138a8-103">Transakce záruční listiny</span><span class="sxs-lookup"><span data-stu-id="138a8-103">Letter of guarantee transaction</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="138a8-104">Tato procedura vás provede procesem Záruční listina.</span><span class="sxs-lookup"><span data-stu-id="138a8-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="138a8-105">Před provedením této procedury je nutné dokončit následující úlohy:</span><span class="sxs-lookup"><span data-stu-id="138a8-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="138a8-106">Nastavení bankovních zařízení a účetních profilů pro záruční listinu.</span><span class="sxs-lookup"><span data-stu-id="138a8-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="138a8-107">Vytvoření smlouvy bankovního zařízení pro záruční listinu.</span><span class="sxs-lookup"><span data-stu-id="138a8-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="138a8-108">Tato procedura používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="138a8-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="138a8-109">Tvorba prodejní objednávky se záruční listinou</span><span class="sxs-lookup"><span data-stu-id="138a8-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="138a8-110">Přejděte na Pohledávky > Objednávky > Všechny prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="138a8-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="138a8-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="138a8-111">Click New.</span></span>
3. <span data-ttu-id="138a8-112">V poli Účet odběratele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="138a8-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="138a8-113">Rozbalte sekci Obecné.</span><span class="sxs-lookup"><span data-stu-id="138a8-113">Expand the General section.</span></span>
5. <span data-ttu-id="138a8-114">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="138a8-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="138a8-115">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="138a8-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="138a8-116">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="138a8-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="138a8-117">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="138a8-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="138a8-118">Vyberte v poli Typ bankovního dokumentu možnost „Záruční listina“.</span><span class="sxs-lookup"><span data-stu-id="138a8-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="138a8-119">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="138a8-119">Click OK.</span></span>
11. <span data-ttu-id="138a8-120">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="138a8-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="138a8-121">Zadejte číslo do pole Jednotková cena.</span><span class="sxs-lookup"><span data-stu-id="138a8-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="138a8-122">Rozbalte sekci Podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="138a8-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="138a8-123">Klikněte na záložku Dodání.</span><span class="sxs-lookup"><span data-stu-id="138a8-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="138a8-124">Poznámka: Vyberte Řízení data dodání = Žádné.</span><span class="sxs-lookup"><span data-stu-id="138a8-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="138a8-125">Zadejte datum do pole Požadované datum expedice.</span><span class="sxs-lookup"><span data-stu-id="138a8-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="138a8-126">Zadejte datum do pole Potvrzené datum expedice.</span><span class="sxs-lookup"><span data-stu-id="138a8-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guarantee_request"></a><span data-ttu-id="138a8-127">Zpracovat příkaz záruční listina_Požadavek</span><span class="sxs-lookup"><span data-stu-id="138a8-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="138a8-128">V podokně akcí klepněte na možnost Spravovat.</span><span class="sxs-lookup"><span data-stu-id="138a8-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="138a8-129">Klikněte na možnost Záruční listina.</span><span class="sxs-lookup"><span data-stu-id="138a8-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="138a8-130">V podokně akcí klikněte na možnost Záruční listina.</span><span class="sxs-lookup"><span data-stu-id="138a8-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="138a8-131">Kliknutím na možnost Požadavek otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="138a8-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="138a8-132">V poli Typ zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="138a8-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="138a8-133">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="138a8-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="138a8-134">Zadejte číslo do pole Hodnota.</span><span class="sxs-lookup"><span data-stu-id="138a8-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="138a8-135">Do pole Datum vypršení platnosti zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="138a8-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="138a8-136">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="138a8-136">Click OK.</span></span>
10. <span data-ttu-id="138a8-137">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="138a8-137">Close the page.</span></span>

## <a name="process-letter-of-guarantee_submit-to-bank"></a><span data-ttu-id="138a8-138">Zpracovat příkaz záruční listina_Odeslat do banky</span><span class="sxs-lookup"><span data-stu-id="138a8-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="138a8-139">Přejděte na možnost Pokladna a banka > Záruční listiny > Záruční listiny.</span><span class="sxs-lookup"><span data-stu-id="138a8-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="138a8-140">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="138a8-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="138a8-141">Kliknutím na Odeslat do banky otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="138a8-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="138a8-142">V poli Bankovní účet zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="138a8-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="138a8-143">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="138a8-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="138a8-144">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="138a8-144">Click OK.</span></span>

## <a name="process-letter-of-guarantee_receive-from-bank"></a><span data-ttu-id="138a8-145">Zpracovat příkaz záruční listina_Přijmout z banky</span><span class="sxs-lookup"><span data-stu-id="138a8-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="138a8-146">Kliknutím na Přijmout z banky otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="138a8-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="138a8-147">Zadejte hodnotu do pole Číslo banky.</span><span class="sxs-lookup"><span data-stu-id="138a8-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="138a8-148">Ověřte hodnoty ve vypočtených polích Marže a výdaje.</span><span class="sxs-lookup"><span data-stu-id="138a8-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="138a8-149">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="138a8-149">Click OK.</span></span>
4. <span data-ttu-id="138a8-150">Rozbalte sekci Akce.</span><span class="sxs-lookup"><span data-stu-id="138a8-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="138a8-151">Ověřte záznam „Přijmout z banky“.</span><span class="sxs-lookup"><span data-stu-id="138a8-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="138a8-152">Klepnutím přejdete na odkaz v poli Číslo dávky deníku.</span><span class="sxs-lookup"><span data-stu-id="138a8-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="138a8-153">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="138a8-153">Click Lines.</span></span>
    * <span data-ttu-id="138a8-154">Ověřte záznamy zaúčtování deníku.</span><span class="sxs-lookup"><span data-stu-id="138a8-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="138a8-155">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="138a8-155">Close the page.</span></span>

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a><span data-ttu-id="138a8-156">Zpracovat příkaz záruční listina_Předat příjemci</span><span class="sxs-lookup"><span data-stu-id="138a8-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="138a8-157">Přejděte na Pohledávky > Objednávky > Všechny prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="138a8-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="138a8-158">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="138a8-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="138a8-159">V podokně akcí klepněte na možnost Spravovat.</span><span class="sxs-lookup"><span data-stu-id="138a8-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="138a8-160">Klikněte na možnost Záruční listina.</span><span class="sxs-lookup"><span data-stu-id="138a8-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="138a8-161">V podokně akcí klikněte na možnost Záruční listina.</span><span class="sxs-lookup"><span data-stu-id="138a8-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="138a8-162">Kliknutím na Dát příjemci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="138a8-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="138a8-163">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="138a8-163">Click OK.</span></span>
8. <span data-ttu-id="138a8-164">Přejděte na možnost Pokladna a banka > Záruční listiny > Záruční listiny.</span><span class="sxs-lookup"><span data-stu-id="138a8-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="138a8-165">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="138a8-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="138a8-166">Kliknutím na Dát příjemci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="138a8-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="138a8-167">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="138a8-167">Click OK.</span></span>
12. <span data-ttu-id="138a8-168">Rozbalte sekci Akce.</span><span class="sxs-lookup"><span data-stu-id="138a8-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="138a8-169">Ověřte záznam „Dát příjemci“.</span><span class="sxs-lookup"><span data-stu-id="138a8-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guarantee_increase-value"></a><span data-ttu-id="138a8-170">Zpracovat příkaz záruční listina_Zvýšit hodnotu</span><span class="sxs-lookup"><span data-stu-id="138a8-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="138a8-171">Přejděte na Pohledávky > Objednávky > Všechny prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="138a8-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="138a8-172">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="138a8-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="138a8-173">V podokně akcí klepněte na možnost Spravovat.</span><span class="sxs-lookup"><span data-stu-id="138a8-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="138a8-174">Klikněte na možnost Záruční listina.</span><span class="sxs-lookup"><span data-stu-id="138a8-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="138a8-175">V podokně akcí klikněte na možnost Záruční listina.</span><span class="sxs-lookup"><span data-stu-id="138a8-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="138a8-176">Kliknutím na možnost Zvýšit hodnotu otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="138a8-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="138a8-177">Zadejte číslo do pole Hodnota k navýšení.</span><span class="sxs-lookup"><span data-stu-id="138a8-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="138a8-178">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="138a8-178">Click OK.</span></span>
9. <span data-ttu-id="138a8-179">Přejděte na možnost Pokladna a banka > Záruční listiny > Záruční listiny.</span><span class="sxs-lookup"><span data-stu-id="138a8-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="138a8-180">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="138a8-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="138a8-181">Kliknutím na možnost Zvýšit hodnotu otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="138a8-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="138a8-182">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="138a8-182">Click OK.</span></span>
13. <span data-ttu-id="138a8-183">Rozbalte sekci Akce.</span><span class="sxs-lookup"><span data-stu-id="138a8-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="138a8-184">Ověřte záznam „Zvýšit hodnotu“.</span><span class="sxs-lookup"><span data-stu-id="138a8-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="138a8-185">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="138a8-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="138a8-186">Klepnutím přejdete na odkaz v poli Číslo dávky deníku.</span><span class="sxs-lookup"><span data-stu-id="138a8-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="138a8-187">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="138a8-187">Click Lines.</span></span>
    * <span data-ttu-id="138a8-188">Ověřte zaúčtované záznamy deníku.</span><span class="sxs-lookup"><span data-stu-id="138a8-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guarantee_liquidate"></a><span data-ttu-id="138a8-189">Zpracovat příkaz záruční listina_Likvidovat</span><span class="sxs-lookup"><span data-stu-id="138a8-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="138a8-190">Přejděte na Pohledávky > Objednávky > Všechny prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="138a8-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="138a8-191">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="138a8-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="138a8-192">V podokně akcí klepněte na možnost Spravovat.</span><span class="sxs-lookup"><span data-stu-id="138a8-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="138a8-193">Klikněte na možnost Záruční listina.</span><span class="sxs-lookup"><span data-stu-id="138a8-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="138a8-194">V podokně akcí klikněte na možnost Záruční listina.</span><span class="sxs-lookup"><span data-stu-id="138a8-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="138a8-195">Otevřete dialogové okno kliknutím na možnost Likvidovat.</span><span class="sxs-lookup"><span data-stu-id="138a8-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="138a8-196">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="138a8-196">Click OK.</span></span>
8. <span data-ttu-id="138a8-197">Přejděte na možnost Pokladna a banka > Záruční listiny > Záruční listiny.</span><span class="sxs-lookup"><span data-stu-id="138a8-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="138a8-198">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="138a8-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="138a8-199">Otevřete dialogové okno kliknutím na možnost Likvidovat.</span><span class="sxs-lookup"><span data-stu-id="138a8-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="138a8-200">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="138a8-200">Click OK.</span></span>
12. <span data-ttu-id="138a8-201">Rozbalte sekci Akce.</span><span class="sxs-lookup"><span data-stu-id="138a8-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="138a8-202">Ověřte záznam „Likvidovat“.</span><span class="sxs-lookup"><span data-stu-id="138a8-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="138a8-203">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="138a8-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="138a8-204">Klepnutím přejdete na odkaz v poli Číslo dávky deníku.</span><span class="sxs-lookup"><span data-stu-id="138a8-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="138a8-205">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="138a8-205">Click Lines.</span></span>
    * <span data-ttu-id="138a8-206">Ověřte zaúčtované záznamy deníku.</span><span class="sxs-lookup"><span data-stu-id="138a8-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="138a8-207">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="138a8-207">Close the page.</span></span>

