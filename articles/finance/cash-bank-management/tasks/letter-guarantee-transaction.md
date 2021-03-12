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
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f13ea1f9acd48cc1e7dce794369e89901bdb582
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976312"
---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="bdc6d-103">Transakce záruční listiny</span><span class="sxs-lookup"><span data-stu-id="bdc6d-103">Letter of guarantee transaction</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bdc6d-104">Tato procedura vás provede procesem Záruční listina.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="bdc6d-105">Před provedením této procedury je nutné dokončit následující úlohy:</span><span class="sxs-lookup"><span data-stu-id="bdc6d-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="bdc6d-106">Nastavení bankovních zařízení a účetních profilů pro záruční listinu.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="bdc6d-107">Vytvoření smlouvy bankovního zařízení pro záruční listinu.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="bdc6d-108">Tato procedura používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="bdc6d-109">Tvorba prodejní objednávky se záruční listinou</span><span class="sxs-lookup"><span data-stu-id="bdc6d-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="bdc6d-110">Přejděte na Pohledávky > Objednávky > Všechny prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="bdc6d-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-111">Click New.</span></span>
3. <span data-ttu-id="bdc6d-112">V poli Účet odběratele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="bdc6d-113">Rozbalte sekci Obecné.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-113">Expand the General section.</span></span>
5. <span data-ttu-id="bdc6d-114">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="bdc6d-115">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="bdc6d-116">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="bdc6d-117">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="bdc6d-118">Vyberte v poli Typ bankovního dokumentu možnost „Záruční listina“.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="bdc6d-119">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-119">Click OK.</span></span>
11. <span data-ttu-id="bdc6d-120">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="bdc6d-121">Zadejte číslo do pole Jednotková cena.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="bdc6d-122">Rozbalte sekci Podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="bdc6d-123">Klikněte na záložku Dodání.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="bdc6d-124">Poznámka: Vyberte Řízení data dodání = Žádné.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="bdc6d-125">Zadejte datum do pole Požadované datum expedice.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="bdc6d-126">Zadejte datum do pole Potvrzené datum expedice.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guarantee_request"></a><span data-ttu-id="bdc6d-127">Zpracovat příkaz záruční listina_Požadavek</span><span class="sxs-lookup"><span data-stu-id="bdc6d-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="bdc6d-128">V podokně akcí klepněte na možnost Spravovat.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="bdc6d-129">Klikněte na možnost Záruční listina.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="bdc6d-130">V podokně akcí klikněte na možnost Záruční listina.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="bdc6d-131">Kliknutím na možnost Požadavek otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="bdc6d-132">V poli Typ zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="bdc6d-133">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="bdc6d-134">Zadejte číslo do pole Hodnota.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="bdc6d-135">Do pole Datum vypršení platnosti zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="bdc6d-136">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-136">Click OK.</span></span>
10. <span data-ttu-id="bdc6d-137">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-137">Close the page.</span></span>

## <a name="process-letter-of-guarantee_submit-to-bank"></a><span data-ttu-id="bdc6d-138">Zpracovat příkaz záruční listina_Odeslat do banky</span><span class="sxs-lookup"><span data-stu-id="bdc6d-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="bdc6d-139">Přejděte na možnost Pokladna a banka > Záruční listiny > Záruční listiny.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="bdc6d-140">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="bdc6d-141">Kliknutím na Odeslat do banky otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="bdc6d-142">V poli Bankovní účet zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="bdc6d-143">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="bdc6d-144">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-144">Click OK.</span></span>

## <a name="process-letter-of-guarantee_receive-from-bank"></a><span data-ttu-id="bdc6d-145">Zpracovat příkaz záruční listina_Přijmout z banky</span><span class="sxs-lookup"><span data-stu-id="bdc6d-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="bdc6d-146">Kliknutím na Přijmout z banky otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="bdc6d-147">Zadejte hodnotu do pole Číslo banky.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="bdc6d-148">Ověřte hodnoty ve vypočtených polích Marže a výdaje.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="bdc6d-149">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-149">Click OK.</span></span>
4. <span data-ttu-id="bdc6d-150">Rozbalte sekci Akce.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="bdc6d-151">Ověřte záznam „Přijmout z banky“.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="bdc6d-152">Klepnutím přejdete na odkaz v poli Číslo dávky deníku.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="bdc6d-153">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-153">Click Lines.</span></span>
    * <span data-ttu-id="bdc6d-154">Ověřte záznamy zaúčtování deníku.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="bdc6d-155">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-155">Close the page.</span></span>

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a><span data-ttu-id="bdc6d-156">Zpracovat příkaz záruční listina_Předat příjemci</span><span class="sxs-lookup"><span data-stu-id="bdc6d-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="bdc6d-157">Přejděte na Pohledávky > Objednávky > Všechny prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="bdc6d-158">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="bdc6d-159">V podokně akcí klepněte na možnost Spravovat.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="bdc6d-160">Klikněte na možnost Záruční listina.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="bdc6d-161">V podokně akcí klikněte na možnost Záruční listina.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="bdc6d-162">Kliknutím na Dát příjemci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="bdc6d-163">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-163">Click OK.</span></span>
8. <span data-ttu-id="bdc6d-164">Přejděte na možnost Pokladna a banka > Záruční listiny > Záruční listiny.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="bdc6d-165">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="bdc6d-166">Kliknutím na Dát příjemci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="bdc6d-167">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-167">Click OK.</span></span>
12. <span data-ttu-id="bdc6d-168">Rozbalte sekci Akce.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="bdc6d-169">Ověřte záznam „Dát příjemci“.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guarantee_increase-value"></a><span data-ttu-id="bdc6d-170">Zpracovat příkaz záruční listina_Zvýšit hodnotu</span><span class="sxs-lookup"><span data-stu-id="bdc6d-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="bdc6d-171">Přejděte na Pohledávky > Objednávky > Všechny prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="bdc6d-172">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="bdc6d-173">V podokně akcí klepněte na možnost Spravovat.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="bdc6d-174">Klikněte na možnost Záruční listina.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="bdc6d-175">V podokně akcí klikněte na možnost Záruční listina.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="bdc6d-176">Kliknutím na možnost Zvýšit hodnotu otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="bdc6d-177">Zadejte číslo do pole Hodnota k navýšení.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="bdc6d-178">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-178">Click OK.</span></span>
9. <span data-ttu-id="bdc6d-179">Přejděte na možnost Pokladna a banka > Záruční listiny > Záruční listiny.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="bdc6d-180">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="bdc6d-181">Kliknutím na možnost Zvýšit hodnotu otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="bdc6d-182">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-182">Click OK.</span></span>
13. <span data-ttu-id="bdc6d-183">Rozbalte sekci Akce.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="bdc6d-184">Ověřte záznam „Zvýšit hodnotu“.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="bdc6d-185">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="bdc6d-186">Klepnutím přejdete na odkaz v poli Číslo dávky deníku.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="bdc6d-187">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-187">Click Lines.</span></span>
    * <span data-ttu-id="bdc6d-188">Ověřte zaúčtované záznamy deníku.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guarantee_liquidate"></a><span data-ttu-id="bdc6d-189">Zpracovat příkaz záruční listina_Likvidovat</span><span class="sxs-lookup"><span data-stu-id="bdc6d-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="bdc6d-190">Přejděte na Pohledávky > Objednávky > Všechny prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="bdc6d-191">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="bdc6d-192">V podokně akcí klepněte na možnost Spravovat.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="bdc6d-193">Klikněte na možnost Záruční listina.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="bdc6d-194">V podokně akcí klikněte na možnost Záruční listina.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="bdc6d-195">Otevřete dialogové okno kliknutím na možnost Likvidovat.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="bdc6d-196">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-196">Click OK.</span></span>
8. <span data-ttu-id="bdc6d-197">Přejděte na možnost Pokladna a banka > Záruční listiny > Záruční listiny.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="bdc6d-198">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="bdc6d-199">Otevřete dialogové okno kliknutím na možnost Likvidovat.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="bdc6d-200">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-200">Click OK.</span></span>
12. <span data-ttu-id="bdc6d-201">Rozbalte sekci Akce.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="bdc6d-202">Ověřte záznam „Likvidovat“.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="bdc6d-203">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="bdc6d-204">Klepnutím přejdete na odkaz v poli Číslo dávky deníku.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="bdc6d-205">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-205">Click Lines.</span></span>
    * <span data-ttu-id="bdc6d-206">Ověřte zaúčtované záznamy deníku.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="bdc6d-207">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="bdc6d-207">Close the page.</span></span>

