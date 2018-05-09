--- 
title: Import akreditivu
description: "Tato procedura vás provede procesem importu akreditivu."
author: kweekley
manager: AnnBe
ms.date: 02/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 38d012fab8dc9ea06b55b960d72578af31291c09
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---
# <a name="import-a-letter-of-credit"></a><span data-ttu-id="49a96-103">Import akreditivu</span><span class="sxs-lookup"><span data-stu-id="49a96-103">Import a letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="49a96-104">Tato procedura vás provede procesem importu akreditivu.</span><span class="sxs-lookup"><span data-stu-id="49a96-104">This procedure walks through the process of importing a letter of credit.</span></span> <span data-ttu-id="49a96-105">Před provedením této procedury je nutné nastavit následující: bankovní zařízení, účetní profily, smlouvu zařízení banky a bankovní údaje dodavatele.</span><span class="sxs-lookup"><span data-stu-id="49a96-105">The following must be set up before completing this procedure: bank facilities, posting profiles, a bank facility agreement and vendor bank details.</span></span>

<span data-ttu-id="49a96-106">Tato procedura používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="49a96-106">This procedure uses the USMF demo company.</span></span>


## <a name="create-a-purchase-order-with-letter-of-credit"></a><span data-ttu-id="49a96-107">Vytvoření nákupní objednávky s akreditivem</span><span class="sxs-lookup"><span data-stu-id="49a96-107">Create a Purchase order with Letter of credit</span></span>
1. <span data-ttu-id="49a96-108">Přejděte na Závazky > Nákupní objednávky > Všechny nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="49a96-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="49a96-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="49a96-109">Click New.</span></span>
3. <span data-ttu-id="49a96-110">V poli Účet dodavatele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="49a96-110">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="49a96-111">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="49a96-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="49a96-112">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="49a96-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="49a96-113">Rozbalte sekci Obecné.</span><span class="sxs-lookup"><span data-stu-id="49a96-113">Expand the General section.</span></span>
7. <span data-ttu-id="49a96-114">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="49a96-114">In the Site field, enter or select a value.</span></span>
8. <span data-ttu-id="49a96-115">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="49a96-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="49a96-116">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="49a96-116">In the Warehouse field, enter or select a value.</span></span>
10. <span data-ttu-id="49a96-117">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="49a96-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="49a96-118">Zadejte datum do pole Datum účtování.</span><span class="sxs-lookup"><span data-stu-id="49a96-118">In the Accounting date field, enter a date.</span></span>
12. <span data-ttu-id="49a96-119">Zadejte datum do pole Datum dodání.</span><span class="sxs-lookup"><span data-stu-id="49a96-119">In the Delivery date field, enter a date.</span></span>
    * <span data-ttu-id="49a96-120">Poznámka: V poli „Typ bankovního dokumentu“ musí být vybrána hodnota „Akreditiv“.</span><span class="sxs-lookup"><span data-stu-id="49a96-120">Note: The 'Bank document type' field should be selected with the value  'Letter of credit'.</span></span>  
13. <span data-ttu-id="49a96-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="49a96-121">Click OK.</span></span>
14. <span data-ttu-id="49a96-122">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="49a96-122">In the Item number field, enter or select a value.</span></span>
15. <span data-ttu-id="49a96-123">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="49a96-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="49a96-124">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="49a96-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="49a96-125">Rozbalte sekci Podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="49a96-125">Expand the Line details section.</span></span>
18. <span data-ttu-id="49a96-126">Klepněte na kartu Doručení.</span><span class="sxs-lookup"><span data-stu-id="49a96-126">Click the Delivery tab.</span></span>
19. <span data-ttu-id="49a96-127">Zadejte datum do pole Datum dodání.</span><span class="sxs-lookup"><span data-stu-id="49a96-127">In the Delivery date field, enter a date.</span></span>
20. <span data-ttu-id="49a96-128">Zadejte datum do pole Potvrzené datum dodání.</span><span class="sxs-lookup"><span data-stu-id="49a96-128">In the Confirmed delivery date field, enter a date.</span></span>
21. <span data-ttu-id="49a96-129">Zadejte číslo do pole Jednotková cena.</span><span class="sxs-lookup"><span data-stu-id="49a96-129">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="49a96-130">Definujte podrobnosti akreditivu.</span><span class="sxs-lookup"><span data-stu-id="49a96-130">Define the Letter of credit details.</span></span>  
22. <span data-ttu-id="49a96-131">V podokně akcí klepněte na možnost Spravovat.</span><span class="sxs-lookup"><span data-stu-id="49a96-131">On the Action Pane, click Manage.</span></span>
23. <span data-ttu-id="49a96-132">Klikněte na Akreditiv nebo kolekci importu.</span><span class="sxs-lookup"><span data-stu-id="49a96-132">Click Letter of credit / import collection.</span></span>
24. <span data-ttu-id="49a96-133">Do pole Datum použití zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="49a96-133">In the Application date field, enter a date and time.</span></span>
    * <span data-ttu-id="49a96-134">Ověřte, že pole „Bankovní účet“ má výchozí aktivní bankovní účet, který je založen na datu aplikace.</span><span class="sxs-lookup"><span data-stu-id="49a96-134">Verify that the 'Bank account' field has the default active Bank account, which is based on the application date.</span></span>  
25. <span data-ttu-id="49a96-135">Zadejte hodnotu do pole Číslo bankovního dokumentu.</span><span class="sxs-lookup"><span data-stu-id="49a96-135">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="49a96-136">Do pole Datum příjmu zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="49a96-136">In the Date of receipt field, enter a date and time.</span></span>
27. <span data-ttu-id="49a96-137">Rozbalte oddíl Bankovní dokument.</span><span class="sxs-lookup"><span data-stu-id="49a96-137">Expand the Bank document section.</span></span>
28. <span data-ttu-id="49a96-138">Do pole Datum vypršení platnosti zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="49a96-138">In the Expiration date field, enter a date and time.</span></span>
29. <span data-ttu-id="49a96-139">Rozbalte část Bankovní údaje.</span><span class="sxs-lookup"><span data-stu-id="49a96-139">Expand the Bank details section.</span></span>
30. <span data-ttu-id="49a96-140">V poli Avizující banka zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="49a96-140">In the Advising bank field, enter or select a value.</span></span>
31. <span data-ttu-id="49a96-141">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="49a96-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="49a96-142">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="49a96-142">Click Save.</span></span>
33. <span data-ttu-id="49a96-143">Klikněte na možnost Načíst dodávky nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="49a96-143">Click Fetch purchase order shipments.</span></span>
34. <span data-ttu-id="49a96-144">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="49a96-144">Close the page.</span></span>
35. <span data-ttu-id="49a96-145">V podokně akcí klikněte na položku Nákup.</span><span class="sxs-lookup"><span data-stu-id="49a96-145">On the Action Pane, click Purchase.</span></span>
36. <span data-ttu-id="49a96-146">Klikněte na tlačítko Potvrdit.</span><span class="sxs-lookup"><span data-stu-id="49a96-146">Click Confirm.</span></span>
37. <span data-ttu-id="49a96-147">V podokně akcí klepněte na možnost Spravovat.</span><span class="sxs-lookup"><span data-stu-id="49a96-147">On the Action Pane, click Manage.</span></span>
38. <span data-ttu-id="49a96-148">Klikněte na Akreditiv nebo kolekci importu.</span><span class="sxs-lookup"><span data-stu-id="49a96-148">Click Letter of credit / import collection.</span></span>
39. <span data-ttu-id="49a96-149">Klikněte na možnost Zpracovat.</span><span class="sxs-lookup"><span data-stu-id="49a96-149">Click Process.</span></span>
40. <span data-ttu-id="49a96-150">Klikněte na tlačítko Potvrdit.</span><span class="sxs-lookup"><span data-stu-id="49a96-150">Click Confirm.</span></span>
    * <span data-ttu-id="49a96-151">Ověřte, zda Zůstatek zařízení snižuje částku nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="49a96-151">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="49a96-152">V tomto příkladu Nákupní částka = 500,00,  Limit zařízení = 10 000,00,  tedy Zůstatek zařízení = 9 500,00.</span><span class="sxs-lookup"><span data-stu-id="49a96-152">In this example, Purchase amount = 500.00,  Facility limit = 10000.00,  therefore, Facility balance = 9500.00.</span></span>  
41. <span data-ttu-id="49a96-153">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="49a96-153">Close the page.</span></span>
42. <span data-ttu-id="49a96-154">Zadejte číslo do pole Jednotková cena.</span><span class="sxs-lookup"><span data-stu-id="49a96-154">In the Unit price field, enter a number.</span></span>
43. <span data-ttu-id="49a96-155">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="49a96-155">Click Save.</span></span>
44. <span data-ttu-id="49a96-156">V podokně akcí klikněte na položku Nákup.</span><span class="sxs-lookup"><span data-stu-id="49a96-156">On the Action Pane, click Purchase.</span></span>
45. <span data-ttu-id="49a96-157">Klikněte na tlačítko Potvrdit.</span><span class="sxs-lookup"><span data-stu-id="49a96-157">Click Confirm.</span></span>
    * <span data-ttu-id="49a96-158">Upravte akreditiv z důvodu změny v jednotkové ceně.</span><span class="sxs-lookup"><span data-stu-id="49a96-158">Amend the Letter of credit, due to the change in Unit price.</span></span>  
46. <span data-ttu-id="49a96-159">V podokně akcí klepněte na možnost Spravovat.</span><span class="sxs-lookup"><span data-stu-id="49a96-159">On the Action Pane, click Manage.</span></span>
47. <span data-ttu-id="49a96-160">Klikněte na Akreditiv nebo kolekci importu.</span><span class="sxs-lookup"><span data-stu-id="49a96-160">Click Letter of credit / import collection.</span></span>
    * <span data-ttu-id="49a96-161">Upravte akreditiv z důvodu změny v jednotkové nákupní jednotkové ceně.</span><span class="sxs-lookup"><span data-stu-id="49a96-161">Amend the letter of credit, due to the change in Purchase unit price.</span></span>  
48. <span data-ttu-id="49a96-162">Klikněte na možnost Zpracovat.</span><span class="sxs-lookup"><span data-stu-id="49a96-162">Click Process.</span></span>
49. <span data-ttu-id="49a96-163">Klikněte na možnost Připojit.</span><span class="sxs-lookup"><span data-stu-id="49a96-163">Click Amend.</span></span>
50. <span data-ttu-id="49a96-164">Klepněte na tlačítko Odebrat.</span><span class="sxs-lookup"><span data-stu-id="49a96-164">Click Remove.</span></span>
51. <span data-ttu-id="49a96-165">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="49a96-165">Click Yes.</span></span>
52. <span data-ttu-id="49a96-166">Klikněte na možnost Načíst dodávky nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="49a96-166">Click Fetch purchase order shipments.</span></span>
53. <span data-ttu-id="49a96-167">Klikněte na možnost Zpracovat.</span><span class="sxs-lookup"><span data-stu-id="49a96-167">Click Process.</span></span>
54. <span data-ttu-id="49a96-168">Klikněte na tlačítko Potvrdit.</span><span class="sxs-lookup"><span data-stu-id="49a96-168">Click Confirm.</span></span>
    * <span data-ttu-id="49a96-169">Ověřte, zda Zůstatek zařízení snižuje částku nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="49a96-169">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="49a96-170">V tomto příkladu upravená Nákupní částka = 600,00,  Limit zařízení = 10 000,00,  tedy Zůstatek zařízení = 9 400,00.</span><span class="sxs-lookup"><span data-stu-id="49a96-170">In this example, edited Purchase amount = 600.00,  Facility limit = 10000.00,  therefore, Facility balance = 9400.00.</span></span>  
55. <span data-ttu-id="49a96-171">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="49a96-171">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="49a96-172">Zaúčtovat dodací list</span><span class="sxs-lookup"><span data-stu-id="49a96-172">Post Packing slip</span></span>
1. <span data-ttu-id="49a96-173">V podokně akcí klikněte na položku Přijmout.</span><span class="sxs-lookup"><span data-stu-id="49a96-173">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="49a96-174">Klikněte na položku Příjemka produktu.</span><span class="sxs-lookup"><span data-stu-id="49a96-174">Click Product receipt.</span></span>
3. <span data-ttu-id="49a96-175">Zadejte hodnotu do pole PurchParmTable_Num.</span><span class="sxs-lookup"><span data-stu-id="49a96-175">In the PurchParmTable_Num field, type a value.</span></span>
    * <span data-ttu-id="49a96-176">Vyberte číslo dodávky vytvořené s odkazem na akreditiv.</span><span class="sxs-lookup"><span data-stu-id="49a96-176">Select the Shipment number created with reference to the Letter of credit.</span></span>  
4. <span data-ttu-id="49a96-177">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="49a96-177">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="49a96-178">Zadejte datum do pole Příjemka produktu.</span><span class="sxs-lookup"><span data-stu-id="49a96-178">In the Product receipt date field, enter a date.</span></span>
6. <span data-ttu-id="49a96-179">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="49a96-179">Click OK.</span></span>
7. <span data-ttu-id="49a96-180">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="49a96-180">Close the page.</span></span>
8. <span data-ttu-id="49a96-181">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="49a96-181">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="49a96-182">Ověření stavu importního akreditivu</span><span class="sxs-lookup"><span data-stu-id="49a96-182">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="49a96-183">Přejděte na Pokladna a banka > Akreditivy > Importovat akreditiv a kolekci importu.</span><span class="sxs-lookup"><span data-stu-id="49a96-183">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="49a96-184">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="49a96-184">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="49a96-185">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="49a96-185">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="49a96-186">Ověřte stav importního akreditivu.</span><span class="sxs-lookup"><span data-stu-id="49a96-186">Verify the Import letter of credit status.</span></span>  
4. <span data-ttu-id="49a96-187">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="49a96-187">Close the page.</span></span>
5. <span data-ttu-id="49a96-188">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="49a96-188">Close the page.</span></span>

## <a name="post-purchase-invoice"></a><span data-ttu-id="49a96-189">Zaúčtování nákupní faktury</span><span class="sxs-lookup"><span data-stu-id="49a96-189">Post purchase invoice</span></span>
1. <span data-ttu-id="49a96-190">Přejděte na Závazky > Nákupní objednávky > Všechny nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="49a96-190">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
    * <span data-ttu-id="49a96-191">Vyberte nákupní objednávku, která byla vytvořena s akreditivem.</span><span class="sxs-lookup"><span data-stu-id="49a96-191">Select the purchase order that was created with letter of credit.</span></span>  
2. <span data-ttu-id="49a96-192">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="49a96-192">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="49a96-193">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="49a96-193">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="49a96-194">V podokně akcí klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="49a96-194">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="49a96-195">Klepněte na Faktura.</span><span class="sxs-lookup"><span data-stu-id="49a96-195">Click Invoice.</span></span>
6. <span data-ttu-id="49a96-196">Zadejte hodnotu do pole Číslo.</span><span class="sxs-lookup"><span data-stu-id="49a96-196">In the Number field, type a value.</span></span>
7. <span data-ttu-id="49a96-197">V poli Číslo dodávky zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="49a96-197">In the Shipment number field, enter or select a value.</span></span>
8. <span data-ttu-id="49a96-198">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="49a96-198">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="49a96-199">Do pole Datum faktury zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="49a96-199">In the Invoice date field, enter a date.</span></span>
10. <span data-ttu-id="49a96-200">Klikněte na položku Aktualizovat stav párování.</span><span class="sxs-lookup"><span data-stu-id="49a96-200">Click Update match status.</span></span>
11. <span data-ttu-id="49a96-201">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="49a96-201">Click Post.</span></span>
12. <span data-ttu-id="49a96-202">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="49a96-202">Close the page.</span></span>
13. <span data-ttu-id="49a96-203">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="49a96-203">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="49a96-204">Ověření stavu importního akreditivu</span><span class="sxs-lookup"><span data-stu-id="49a96-204">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="49a96-205">Přejděte na Pokladna a banka > Akreditivy > Importovat akreditiv a kolekci importu.</span><span class="sxs-lookup"><span data-stu-id="49a96-205">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="49a96-206">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="49a96-206">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="49a96-207">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="49a96-207">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="49a96-208">Ověřte stav akreditivu2.</span><span class="sxs-lookup"><span data-stu-id="49a96-208">Verify the Import letter of credit2.</span></span>  
    * <span data-ttu-id="49a96-209">Ověřit:  Stav dodávky =  Fakturováno Podronmosti bankovního zařízení</span><span class="sxs-lookup"><span data-stu-id="49a96-209">Validate :  Shipment status = Invoiced  Bank facility details</span></span>  
4. <span data-ttu-id="49a96-210">Klikněte na možnost Zobrazit.</span><span class="sxs-lookup"><span data-stu-id="49a96-210">Click View.</span></span>
5. <span data-ttu-id="49a96-211">Klikněte na možnost Tisk přihlášky.</span><span class="sxs-lookup"><span data-stu-id="49a96-211">Click Print application.</span></span>
6. <span data-ttu-id="49a96-212">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="49a96-212">Click OK.</span></span>
    * <span data-ttu-id="49a96-213">Ověřte, že se přihláška akreditivu vytiskne.</span><span class="sxs-lookup"><span data-stu-id="49a96-213">Verify that the Letter of credit application gets printed.</span></span>  
7. <span data-ttu-id="49a96-214">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="49a96-214">Close the page.</span></span>
8. <span data-ttu-id="49a96-215">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="49a96-215">Close the page.</span></span>
9. <span data-ttu-id="49a96-216">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="49a96-216">Close the page.</span></span>

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a><span data-ttu-id="49a96-217">Zaúčtovat deník plateb dodavatele pro vytvořené nákupní faktury s akreditivem</span><span class="sxs-lookup"><span data-stu-id="49a96-217">Post Vendor payment journal for the created purchase invoice with letter of credit</span></span>
1. <span data-ttu-id="49a96-218">Přejděte na Závazky > Platby > Deník plateb.</span><span class="sxs-lookup"><span data-stu-id="49a96-218">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="49a96-219">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="49a96-219">Click New.</span></span>
3. <span data-ttu-id="49a96-220">V poli Název zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="49a96-220">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="49a96-221">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="49a96-221">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="49a96-222">Klikněte na možnost Řádky.</span><span class="sxs-lookup"><span data-stu-id="49a96-222">Click Lines.</span></span>
6. <span data-ttu-id="49a96-223">Do pole Datum zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="49a96-223">In the Date field, enter a date.</span></span>
7. <span data-ttu-id="49a96-224">Zadejte požadované hodnoty do pole Účet.</span><span class="sxs-lookup"><span data-stu-id="49a96-224">In the Account field, specify the desired values.</span></span>
8. <span data-ttu-id="49a96-225">Klikněte na možnost Vyrovnat transakce.</span><span class="sxs-lookup"><span data-stu-id="49a96-225">Click Settle transactions.</span></span>
9. <span data-ttu-id="49a96-226">Rozbalte část Součty.</span><span class="sxs-lookup"><span data-stu-id="49a96-226">Expand the Totals section.</span></span>
10. <span data-ttu-id="49a96-227">Vyberte možnost v poli Zobrazit.</span><span class="sxs-lookup"><span data-stu-id="49a96-227">In the Show field, select an option.</span></span>
    * <span data-ttu-id="49a96-228">Ověřte, aby byla aktualizovány pole Číslo bankovního dokumentu a Číslo dodávky.</span><span class="sxs-lookup"><span data-stu-id="49a96-228">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
11. <span data-ttu-id="49a96-229">Vyberte Zaškrtnout políčko.</span><span class="sxs-lookup"><span data-stu-id="49a96-229">Select the Mark check box.</span></span>
12. <span data-ttu-id="49a96-230">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="49a96-230">Click OK.</span></span>
13. <span data-ttu-id="49a96-231">Klikněte na kartu Platba.</span><span class="sxs-lookup"><span data-stu-id="49a96-231">Click the Payment tab.</span></span>
    * <span data-ttu-id="49a96-232">Ověřte, aby byla aktualizovány pole Číslo bankovního dokumentu a Číslo dodávky.</span><span class="sxs-lookup"><span data-stu-id="49a96-232">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
14. <span data-ttu-id="49a96-233">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="49a96-233">Click Post.</span></span>
15. <span data-ttu-id="49a96-234">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="49a96-234">Close the page.</span></span>
16. <span data-ttu-id="49a96-235">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="49a96-235">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a><span data-ttu-id="49a96-236">Po zaplacení faktury ověřte stav importního akreditivu</span><span class="sxs-lookup"><span data-stu-id="49a96-236">Verify Import letter of credit status after Invoice paid</span></span>
1. <span data-ttu-id="49a96-237">Přejděte na Pokladna a banka > Akreditivy > Importovat akreditiv a kolekci importu.</span><span class="sxs-lookup"><span data-stu-id="49a96-237">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="49a96-238">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="49a96-238">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="49a96-239">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="49a96-239">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="49a96-240">Ověřte stav importního akreditivu.</span><span class="sxs-lookup"><span data-stu-id="49a96-240">Verify the Import letter of credit status.</span></span>   
4. <span data-ttu-id="49a96-241">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="49a96-241">Close the page.</span></span>

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a><span data-ttu-id="49a96-242">Ověření limitu bankovního zařízení a sestavu využití</span><span class="sxs-lookup"><span data-stu-id="49a96-242">Verify the Bank facility limit and utilization report</span></span>
1. <span data-ttu-id="49a96-243">Přejděte na Pokladna a banka > Dotazy a sestavy > Akreditivy a záruční listiny > Sestava zařízení banky a využití.</span><span class="sxs-lookup"><span data-stu-id="49a96-243">Go to Cash and bank management > Inquiries and reports > Letters of credit or guarantee > Bank facilities and utilization report.</span></span>
2. <span data-ttu-id="49a96-244">Rozbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="49a96-244">Expand the Records to include section.</span></span>
3. <span data-ttu-id="49a96-245">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="49a96-245">Click Filter.</span></span>
    * <span data-ttu-id="49a96-246">Definujte pole Kritéria pomocí požadovaného bankovního účtu.</span><span class="sxs-lookup"><span data-stu-id="49a96-246">Define the Criteria field with the required bank account.</span></span>  
4. <span data-ttu-id="49a96-247">V poli Kritéria zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="49a96-247">In the Criteria field, enter or select a value.</span></span>
5. <span data-ttu-id="49a96-248">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="49a96-248">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="49a96-249">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="49a96-249">Click OK.</span></span>
7. <span data-ttu-id="49a96-250">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="49a96-250">Click OK.</span></span>
    * <span data-ttu-id="49a96-251">Ověřte sestavu, která obsahuje seznam transakcí.</span><span class="sxs-lookup"><span data-stu-id="49a96-251">Verify the report which lists the transactions.</span></span>  
    * <span data-ttu-id="49a96-252">Ověřte že sestava obsahuje seznam transakcí s číslem bankovního dokladu, limitem zařízení, využitou částkou a částkou zůstatku zařízení.</span><span class="sxs-lookup"><span data-stu-id="49a96-252">Verify the report lists the transactions with Bank document number, Facility limit, utilized amount and the facility balance amount.</span></span>  
8. <span data-ttu-id="49a96-253">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="49a96-253">Close the page.</span></span>


