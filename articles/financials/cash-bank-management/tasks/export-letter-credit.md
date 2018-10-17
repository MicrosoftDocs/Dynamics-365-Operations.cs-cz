--- 
title: Export akreditivu
description: "Tato procedura vás provede procesem exportního akreditivu."
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 730a6cc6ed4872f8d0ad92b89665587f472f6791
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="export-letter-of-credit"></a><span data-ttu-id="5d383-103">Export akreditivu</span><span class="sxs-lookup"><span data-stu-id="5d383-103">Export letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5d383-104">Tato procedura vás provede procesem exportního akreditivu.</span><span class="sxs-lookup"><span data-stu-id="5d383-104">This procedure walks through the process of the Export letter of credit.</span></span>

<span data-ttu-id="5d383-105">Pojem akreditiv označuje bankovní smlouvu, ve které banka souhlasí se zajištěním platby jménem kupujícího za předpokladu, že jsou splněny podmínky mezi kupujícím a prodávajícím.</span><span class="sxs-lookup"><span data-stu-id="5d383-105">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to ensure payment on behalf of the buyer, if the terms of the agreement between the buyer and seller are met.</span></span>



<span data-ttu-id="5d383-106">Před provedením této procedury spusťte procedury „Nastavení zařízení banky a zaúčtování profilů“ a „Akreditiv_Vytvoření smlouvy o bankovních zařízeních“.</span><span class="sxs-lookup"><span data-stu-id="5d383-106">Run the 'Set up bank facilities and posting profiles' procedure and the 'Letter of Credit_Create a bank facility agreement' procedure prior to this procedure.</span></span> <span data-ttu-id="5d383-107">Abyste mohli úspěšně spustit tuto proceduru, musí být vybrána ukázková společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="5d383-107">The USMF demo company must be selected in order to run this procedure successfully.</span></span>




## <a name="create-sales-order-for-export-letter-of-credit"></a><span data-ttu-id="5d383-108">Vytvoření prodejní objednávky pro exportní akreditiv</span><span class="sxs-lookup"><span data-stu-id="5d383-108">Create Sales Order for Export letter of credit</span></span>
1. <span data-ttu-id="5d383-109">Přejděte na Pohledávky > Objednávky > Všechny prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="5d383-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="5d383-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="5d383-110">Click New.</span></span>
3. <span data-ttu-id="5d383-111">V poli Účet odběratele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="5d383-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="5d383-112">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="5d383-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="5d383-113">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="5d383-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="5d383-114">Rozbalte nebo sbalte oddíl Obecné.</span><span class="sxs-lookup"><span data-stu-id="5d383-114">Expand or collapse the General section.</span></span>
7. <span data-ttu-id="5d383-115">V poli Lokalita kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="5d383-115">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="5d383-116">Umožňuje vybrat nebo zobrazit lokalitu, ve které je uloženo zboží k vydání.</span><span class="sxs-lookup"><span data-stu-id="5d383-116">Select the Site where the item to be issued is stocked.</span></span>  
8. <span data-ttu-id="5d383-117">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="5d383-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="5d383-118">V poli Sklad kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="5d383-118">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="5d383-119">Umožňuje vybrat nebo zobrazit sklad, ve kterém je uloženo zboží k vydání.</span><span class="sxs-lookup"><span data-stu-id="5d383-119">Select the Warehouse where item to be issued is stocked.</span></span>  
10. <span data-ttu-id="5d383-120">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="5d383-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="5d383-121">Poznámka: V poli Typ bankovního dokumentu musí být vybrána hodnota „Akreditiv“.</span><span class="sxs-lookup"><span data-stu-id="5d383-121">Note: The Bank document type field should be selected with the value 'Letter of credit'.</span></span>  
11. <span data-ttu-id="5d383-122">Vyberte v poli Typ bankovního dokumentu možnost „Akreditiv“.</span><span class="sxs-lookup"><span data-stu-id="5d383-122">In the Bank document type field, select 'Letter of credit'.</span></span>
12. <span data-ttu-id="5d383-123">Rozbalte nebo sbalte oddíl Dodání.</span><span class="sxs-lookup"><span data-stu-id="5d383-123">Expand or collapse the Delivery section.</span></span>
    * <span data-ttu-id="5d383-124">Vyberte Řízení data dodání = Žádné.</span><span class="sxs-lookup"><span data-stu-id="5d383-124">Select Delivery date control = None.</span></span>  
13. <span data-ttu-id="5d383-125">Zadejte datum do pole Požadované datum příjmu.</span><span class="sxs-lookup"><span data-stu-id="5d383-125">In the Requested receipt date field, enter a date.</span></span>
14. <span data-ttu-id="5d383-126">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="5d383-126">Click OK.</span></span>
15. <span data-ttu-id="5d383-127">V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="5d383-127">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="5d383-128">Vyberte požadované zboží k výdeji nebo prodeji.</span><span class="sxs-lookup"><span data-stu-id="5d383-128">Select the required item to be Issued/Sold.</span></span>  
16. <span data-ttu-id="5d383-129">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="5d383-129">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="5d383-130">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="5d383-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="5d383-131">Zadejte číslo do pole Jednotková cena.</span><span class="sxs-lookup"><span data-stu-id="5d383-131">In the Unit price field, enter a number.</span></span>
19. <span data-ttu-id="5d383-132">Rozbalte nebo sbalte oddíl Podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="5d383-132">Expand or collapse the Line details section.</span></span>
20. <span data-ttu-id="5d383-133">Klepněte na kartu Doručení.</span><span class="sxs-lookup"><span data-stu-id="5d383-133">Click the Delivery tab.</span></span>
21. <span data-ttu-id="5d383-134">Zadejte datum do pole Požadované datum expedice.</span><span class="sxs-lookup"><span data-stu-id="5d383-134">In the Requested ship date field, enter a date.</span></span>
22. <span data-ttu-id="5d383-135">Zadejte datum do pole Potvrzené datum expedice.</span><span class="sxs-lookup"><span data-stu-id="5d383-135">In the Confirmed ship date field, enter a date.</span></span>
23. <span data-ttu-id="5d383-136">V podokně akcí klepněte na možnost Spravovat.</span><span class="sxs-lookup"><span data-stu-id="5d383-136">On the Action Pane, click Manage.</span></span>
24. <span data-ttu-id="5d383-137">Klikněte na možnost Akreditiv.</span><span class="sxs-lookup"><span data-stu-id="5d383-137">Click Letter of credit.</span></span>
25. <span data-ttu-id="5d383-138">Zadejte hodnotu do pole Číslo bankovního dokumentu.</span><span class="sxs-lookup"><span data-stu-id="5d383-138">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="5d383-139">Do pole Datum vypršení platnosti zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="5d383-139">In the Expiration date field, enter a date and time.</span></span>
27. <span data-ttu-id="5d383-140">Rozbalte nebo sbalte oddíl Bankovní údaje.</span><span class="sxs-lookup"><span data-stu-id="5d383-140">Expand or collapse the Bank details section.</span></span>
28. <span data-ttu-id="5d383-141">V poli Vydávající banka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="5d383-141">In the Issuing bank field, click the drop-down button to open the lookup.</span></span>
29. <span data-ttu-id="5d383-142">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="5d383-142">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="5d383-143">V poli Avizující banka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="5d383-143">In the Advising bank field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="5d383-144">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="5d383-144">In the list, find and select the desired record.</span></span>
32. <span data-ttu-id="5d383-145">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="5d383-145">In the list, click the link in the selected row.</span></span>
33. <span data-ttu-id="5d383-146">Klikněte na možnost Načíst dodávky prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="5d383-146">Click Fetch sales order shipments.</span></span>
34. <span data-ttu-id="5d383-147">Klikněte na možnost Vydat bankovní dokument.</span><span class="sxs-lookup"><span data-stu-id="5d383-147">Click Issue bank document.</span></span>
35. <span data-ttu-id="5d383-148">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5d383-148">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="5d383-149">Zaúčtovat dodací list</span><span class="sxs-lookup"><span data-stu-id="5d383-149">Post Packing slip</span></span>
1. <span data-ttu-id="5d383-150">V podokně akcí klikněte na položku Vyskladnit a zabalit.</span><span class="sxs-lookup"><span data-stu-id="5d383-150">On the Action Pane, click Pick and pack.</span></span>
2. <span data-ttu-id="5d383-151">Klikněte na položku Zaúčtovat dodací list.</span><span class="sxs-lookup"><span data-stu-id="5d383-151">Click Post packing slip.</span></span>
3. <span data-ttu-id="5d383-152">Rozbalte nebo sbalte oddíl Parametry.</span><span class="sxs-lookup"><span data-stu-id="5d383-152">Expand or collapse the Parameters section.</span></span>
4. <span data-ttu-id="5d383-153">V poli Množství vyberte možnost „Vše“.</span><span class="sxs-lookup"><span data-stu-id="5d383-153">In the Quantity field, select 'All'.</span></span>
5. <span data-ttu-id="5d383-154">Rozbalte nebo sbalte oddíl Nastavení.</span><span class="sxs-lookup"><span data-stu-id="5d383-154">Expand or collapse the Setup section.</span></span>
6. <span data-ttu-id="5d383-155">Do pole Datum dodacího listu zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="5d383-155">In the Packing slip date field, enter a date.</span></span>
7. <span data-ttu-id="5d383-156">Vyberte číslo dodávky.</span><span class="sxs-lookup"><span data-stu-id="5d383-156">Select the Shipment number.</span></span>
8. <span data-ttu-id="5d383-157">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="5d383-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="5d383-158">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="5d383-158">Click OK.</span></span>
10. <span data-ttu-id="5d383-159">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="5d383-159">Click OK.</span></span>

## <a name="post-sales-invoice"></a><span data-ttu-id="5d383-160">Zaúčtovat prodejní fakturu</span><span class="sxs-lookup"><span data-stu-id="5d383-160">Post sales invoice</span></span>
1. <span data-ttu-id="5d383-161">V podokně akcí klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="5d383-161">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="5d383-162">Klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="5d383-162">Click Invoice.</span></span>
3. <span data-ttu-id="5d383-163">Rozbalte nebo sbalte oddíl Přehled.</span><span class="sxs-lookup"><span data-stu-id="5d383-163">Expand or collapse the Overview section.</span></span>
4. <span data-ttu-id="5d383-164">Vyberte číslo dodávky.</span><span class="sxs-lookup"><span data-stu-id="5d383-164">Select the Shipment number.</span></span>
5. <span data-ttu-id="5d383-165">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="5d383-165">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="5d383-166">Rozbalte nebo sbalte oddíl Nastavení.</span><span class="sxs-lookup"><span data-stu-id="5d383-166">Expand or collapse the Setup section.</span></span>
7. <span data-ttu-id="5d383-167">Do pole Datum faktury zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="5d383-167">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="5d383-168">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="5d383-168">Click OK.</span></span>
9. <span data-ttu-id="5d383-169">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="5d383-169">Click OK.</span></span>

## <a name="shipment-document-submitted-status"></a><span data-ttu-id="5d383-170">Stav odeslaného dodacího dokladu</span><span class="sxs-lookup"><span data-stu-id="5d383-170">Shipment document submitted status</span></span>
1. <span data-ttu-id="5d383-171">V podokně akcí klepněte na možnost Spravovat.</span><span class="sxs-lookup"><span data-stu-id="5d383-171">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="5d383-172">Klikněte na možnost Akreditiv.</span><span class="sxs-lookup"><span data-stu-id="5d383-172">Click Letter of credit.</span></span>
3. <span data-ttu-id="5d383-173">Rozbalte nebo sbalte oddíl Řádky.</span><span class="sxs-lookup"><span data-stu-id="5d383-173">Expand or collapse the Lines section.</span></span>
    * <span data-ttu-id="5d383-174">Poznámka: Pole Dokument odeslán je nastaveno na hodnotu „Ano“.</span><span class="sxs-lookup"><span data-stu-id="5d383-174">Note: The 'Document submitted' field should be set to 'Yes'.</span></span>  

## <a name="verify-export-letter-of-credit"></a><span data-ttu-id="5d383-175">Ověřit exportní akreditiv</span><span class="sxs-lookup"><span data-stu-id="5d383-175">Verify Export letter of credit</span></span>
1. <span data-ttu-id="5d383-176">Přejděte na Pokladna a banka > Akreditivy > Exportovat akreditiv a kolekci importu.</span><span class="sxs-lookup"><span data-stu-id="5d383-176">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="5d383-177">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="5d383-177">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="5d383-178">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="5d383-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="5d383-179">Ověřte, že exportní akreditiv má stav dodávky „Fakturováno“.</span><span class="sxs-lookup"><span data-stu-id="5d383-179">Verify that the Export letter of credit has a Shipment status of 'Invoiced'.</span></span>  

## <a name="customer-payment"></a><span data-ttu-id="5d383-180">Platba odběratele</span><span class="sxs-lookup"><span data-stu-id="5d383-180">Customer payment</span></span>
1. <span data-ttu-id="5d383-181">Přejděte na Pohledávky > Platby > Deník plateb.</span><span class="sxs-lookup"><span data-stu-id="5d383-181">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="5d383-182">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="5d383-182">Click New.</span></span>
3. <span data-ttu-id="5d383-183">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="5d383-183">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="5d383-184">V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="5d383-184">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="5d383-185">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="5d383-185">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="5d383-186">Klikněte na možnost Řádky.</span><span class="sxs-lookup"><span data-stu-id="5d383-186">Click Lines.</span></span>
7. <span data-ttu-id="5d383-187">Do pole Datum zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="5d383-187">In the Date field, enter a date.</span></span>
8. <span data-ttu-id="5d383-188">Zadejte požadované hodnoty do pole Účet.</span><span class="sxs-lookup"><span data-stu-id="5d383-188">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="5d383-189">Klepněte na vyrovnání.</span><span class="sxs-lookup"><span data-stu-id="5d383-189">Click Settlement.</span></span>
10. <span data-ttu-id="5d383-190">Zaškrtněte políčko záhlaví součtů.</span><span class="sxs-lookup"><span data-stu-id="5d383-190">Select the check box on the header of Totals.</span></span>
    * <span data-ttu-id="5d383-191">Poznámka: Nastavte možnost Zobrazit pole na hodnotu „akreditiv“.</span><span class="sxs-lookup"><span data-stu-id="5d383-191">Note: Set the Show field to 'Letter of credit'.</span></span>  
11. <span data-ttu-id="5d383-192">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="5d383-192">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="5d383-193">Zaškrtněte políčko Označit nebo jeho zaškrtnutí zrušte.</span><span class="sxs-lookup"><span data-stu-id="5d383-193">Select or clear the Mark check box.</span></span>
13. <span data-ttu-id="5d383-194">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="5d383-194">Click OK.</span></span>
14. <span data-ttu-id="5d383-195">Klikněte na kartu Platba.</span><span class="sxs-lookup"><span data-stu-id="5d383-195">Click the Payment tab.</span></span>
    * <span data-ttu-id="5d383-196">Ověření čísla bankovního dokumentu čísla dokladu a podrobností o čísle dodávky</span><span class="sxs-lookup"><span data-stu-id="5d383-196">Verify Bank document number and Shipment number details</span></span>  
15. <span data-ttu-id="5d383-197">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="5d383-197">Click Post.</span></span>

## <a name="verify-export-letter-of-credit-after-payment"></a><span data-ttu-id="5d383-198">Ověřit exportní akreditiv po platbě</span><span class="sxs-lookup"><span data-stu-id="5d383-198">Verify Export letter of credit after payment</span></span>
1. <span data-ttu-id="5d383-199">Přejděte na Pokladna a banka > Akreditivy > Exportovat akreditiv a kolekci importu.</span><span class="sxs-lookup"><span data-stu-id="5d383-199">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="5d383-200">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="5d383-200">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="5d383-201">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="5d383-201">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="5d383-202">Ověřit stav dodávky = přijaté platby a částka zůstatku = 0,00.</span><span class="sxs-lookup"><span data-stu-id="5d383-202">Verify Shipment status = Payment received and balance amount = 0.00.</span></span>  


