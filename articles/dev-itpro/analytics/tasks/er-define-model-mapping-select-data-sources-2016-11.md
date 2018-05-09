--- 
title: "Definování mapování modelů a výběr zdrojů dat pro elektronické výkaznictví (ER)"
description: "Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vybrat zdroje dat pro datový model Elektronické výkaznictví."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9f0102b17ae4c9f63228f140e65e87c318cbd36e
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---
# <a name="define-model-mapping-and-select-data-sources-for-electronic-reporting-er"></a><span data-ttu-id="89723-103">Definování mapování modelů a výběr zdrojů dat pro elektronické výkaznictví (ER)</span><span class="sxs-lookup"><span data-stu-id="89723-103">Define model mapping and select data sources for electronic reporting (ER)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="89723-104">Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vybrat zdroje dat pro datový model Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="89723-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can select data sources for an Electronic reporting (ER) data model.</span></span> <span data-ttu-id="89723-105">Zdroje dat budou v době návrhu vázány k jednotlivých součástem vybraného datového modelu a za běhu vyplní obchodní data do datového modelu.</span><span class="sxs-lookup"><span data-stu-id="89723-105">The data sources will be bound to individual components of the selected data model at design time and populate business data to that data model at run-time.</span></span> <span data-ttu-id="89723-106">V tomto příkladu budete vybírat zdroje dat pro existující datový model, který byl vytvořen pro vzorovou společnost Litware, Inc. K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu Vytvoření nového datového modelu.</span><span class="sxs-lookup"><span data-stu-id="89723-106">In this example, you will select data sources for an existing data model that has been created for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Create a new data model” procedure.</span></span>


## <a name="open-the-electronic-reporting-configurations-tree"></a><span data-ttu-id="89723-107">Otevření stromu konfigurací elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="89723-107">Open the Electronic Reporting configurations tree</span></span>
1. <span data-ttu-id="89723-108">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="89723-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="89723-109">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="89723-109">Click Reporting configurations.</span></span>

## <a name="insert-a-new-model-mapping"></a><span data-ttu-id="89723-110">Vložení nového mapování modelu</span><span class="sxs-lookup"><span data-stu-id="89723-110">Insert a new model mapping</span></span>
1. <span data-ttu-id="89723-111">Ve stromovém zobrazení vyberte možnost „Platby (zjednodušený model)“.</span><span class="sxs-lookup"><span data-stu-id="89723-111">In the tree, select 'Payments (simplified model)'.</span></span>
2. <span data-ttu-id="89723-112">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="89723-112">Click Designer.</span></span>
3. <span data-ttu-id="89723-113">Klikněte na možnost Mapovat model na datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="89723-113">Click Map model to datasource.</span></span>
4. <span data-ttu-id="89723-114">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="89723-114">Click New.</span></span>
    * <span data-ttu-id="89723-115">Tím vytvoříte nový záznam, který namapuje datový model na zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="89723-115">This will create a new record that will map the data model to data sources.</span></span> <span data-ttu-id="89723-116">V tomto příkladu namapujete datový model na zdroje dat pro požadovaný typ platby: peněžní převod.</span><span class="sxs-lookup"><span data-stu-id="89723-116">In this example, you will map the data model to data sources for the desired payment type: credit transfer.</span></span>     <span data-ttu-id="89723-117">Pro konkrétní datový model lze navrhnout více mapování.</span><span class="sxs-lookup"><span data-stu-id="89723-117">It is possible to design more than one mapping for a particular data model.</span></span> <span data-ttu-id="89723-118">Například můžete vytvořit mapování pro různé typy plateb, jako je například pro přímý debet nebo peněžní převody.</span><span class="sxs-lookup"><span data-stu-id="89723-118">For example, you could create a mapping for the different types of payments, such as for direct debit or for credit transfers.</span></span> <span data-ttu-id="89723-119">V tomto příkladu vytvoříte mapování pro peněžní převody.</span><span class="sxs-lookup"><span data-stu-id="89723-119">In this example, you will create a mapping for credit transfers.</span></span>  
5. <span data-ttu-id="89723-120">Zadejte text „Mapování Dal“ do pole Název.</span><span class="sxs-lookup"><span data-stu-id="89723-120">In the Name field, type 'CT mapping'.</span></span>
    * <span data-ttu-id="89723-121">Mapování Dal</span><span class="sxs-lookup"><span data-stu-id="89723-121">CT mapping</span></span>  
6. <span data-ttu-id="89723-122">V poli Popis zadejte „Model platby pro mapování Dal“.</span><span class="sxs-lookup"><span data-stu-id="89723-122">In the Description field, type 'Payment model mapping CT'.</span></span>
    * <span data-ttu-id="89723-123">Model platby pro mapování Dal</span><span class="sxs-lookup"><span data-stu-id="89723-123">Payment model mapping CT</span></span>  
7. <span data-ttu-id="89723-124">Zadejte hodnotu CustomerCreditTransferInitiation do pole Definice.</span><span class="sxs-lookup"><span data-stu-id="89723-124">In the Definition field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="89723-125">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="89723-125">CustomerCreditTransferInitiation</span></span>  
8. <span data-ttu-id="89723-126">ResolveChanges Definice.</span><span class="sxs-lookup"><span data-stu-id="89723-126">ResolveChanges the Definition.</span></span>
9. <span data-ttu-id="89723-127">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="89723-127">Click Save.</span></span>

## <a name="define-required-data-sources-for-the-current-model-mapping"></a><span data-ttu-id="89723-128">Definování požadovaných zdrojů dat pro aktuální mapování modelu</span><span class="sxs-lookup"><span data-stu-id="89723-128">Define required data sources for the current model mapping</span></span>
1. <span data-ttu-id="89723-129">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="89723-129">Click Designer.</span></span>
2. <span data-ttu-id="89723-130">Ve stromové struktuře vyberte Dynamics 365 for Operations\Záznamy tabulky.</span><span class="sxs-lookup"><span data-stu-id="89723-130">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
3. <span data-ttu-id="89723-131">Klikněte na možnost Přidat kořen.</span><span class="sxs-lookup"><span data-stu-id="89723-131">Click Add root.</span></span>
    * <span data-ttu-id="89723-132">Zadejte tento zdroj dat pro přístup k platebním transakcím.</span><span class="sxs-lookup"><span data-stu-id="89723-132">Enter this data source to access payment transactions.</span></span>  
4. <span data-ttu-id="89723-133">Zadejte text „Transakce“ do pole Název.</span><span class="sxs-lookup"><span data-stu-id="89723-133">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="89723-134">Transakce</span><span class="sxs-lookup"><span data-stu-id="89723-134">Transactions</span></span>  
5. <span data-ttu-id="89723-135">Zadejte text „Transakce“ do pole Popisek.</span><span class="sxs-lookup"><span data-stu-id="89723-135">In the Label field, enter 'Transactions'.</span></span>
    * <span data-ttu-id="89723-136">Transakce</span><span class="sxs-lookup"><span data-stu-id="89723-136">Transactions</span></span>  
6. <span data-ttu-id="89723-137">V poli Nápověda zadejte text „Řádky deníku hlavní knihy“.</span><span class="sxs-lookup"><span data-stu-id="89723-137">In the Help field, enter 'Ledger journal lines'.</span></span>
    * <span data-ttu-id="89723-138">Řádky deníku hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="89723-138">Ledger journal lines</span></span>  
7. <span data-ttu-id="89723-139">Vyberte možnost Ano v poli Zeptat se na dotaz.</span><span class="sxs-lookup"><span data-stu-id="89723-139">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="89723-140">Vyberte možnost Ano.</span><span class="sxs-lookup"><span data-stu-id="89723-140">Select Yes.</span></span>  
8. <span data-ttu-id="89723-141">Do pole Tabulka zadejte hodnotu „LedgerJournalTrans“.</span><span class="sxs-lookup"><span data-stu-id="89723-141">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="89723-142">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="89723-142">LedgerJournalTrans</span></span>  
9. <span data-ttu-id="89723-143">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="89723-143">Click OK.</span></span>
    * <span data-ttu-id="89723-144">Vyberte tabulku LedgerJournalTrans jako zdroj dat pro aktuální datový model.</span><span class="sxs-lookup"><span data-stu-id="89723-144">Select the LedgerJournalTrans table as a data source for the current data model.</span></span>  
10. <span data-ttu-id="89723-145">Ve stromovém zobrazení vyberte možnost „Funkce\Počítané pole“.</span><span class="sxs-lookup"><span data-stu-id="89723-145">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="89723-146">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="89723-146">Click Add.</span></span>
    * <span data-ttu-id="89723-147">Kliknutím na tlačítko Přidat přidejte nové vypočítané pole.</span><span class="sxs-lookup"><span data-stu-id="89723-147">Click Add to add a new calculated field.</span></span>  
12. <span data-ttu-id="89723-148">Zadejte text „$EndToEndID“ do pole Název.</span><span class="sxs-lookup"><span data-stu-id="89723-148">In the Name field, type '$EndToEndID'.</span></span>
    * <span data-ttu-id="89723-149">$EndToEndID</span><span class="sxs-lookup"><span data-stu-id="89723-149">$EndToEndID</span></span>  
13. <span data-ttu-id="89723-150">Klikněte na možnost Upravit vzorec.</span><span class="sxs-lookup"><span data-stu-id="89723-150">Click Edit formula.</span></span>
14. <span data-ttu-id="89723-151">Ve stromovém zobrazení vyberte možnost „Řetězec\SLOUČIT“.</span><span class="sxs-lookup"><span data-stu-id="89723-151">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="89723-152">Klikněte na možnost Přidat funkci.</span><span class="sxs-lookup"><span data-stu-id="89723-152">Click Add function.</span></span>
16. <span data-ttu-id="89723-153">Ve stromovém zobrazení rozbalte možnost Transakce.</span><span class="sxs-lookup"><span data-stu-id="89723-153">In the tree, expand 'Transactions'.</span></span>
17. <span data-ttu-id="89723-154">Ve stromovém zobrazení vyberte možnost „Transakce\Doklad“.</span><span class="sxs-lookup"><span data-stu-id="89723-154">In the tree, select 'Transactions\Voucher'.</span></span>
18. <span data-ttu-id="89723-155">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="89723-155">Click Add data source.</span></span>
19. <span data-ttu-id="89723-156">V poli Vzorec zadejte 'CONCATENATE(Transactions.Voucher, "-", '.</span><span class="sxs-lookup"><span data-stu-id="89723-156">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", '.</span></span>
    * <span data-ttu-id="89723-157">Na konci receptury zadejte [ , “-“, ].</span><span class="sxs-lookup"><span data-stu-id="89723-157">Type [ , “-“, ] at the end of the formula.</span></span>  
20. <span data-ttu-id="89723-158">Ve stromovém zobrazení vyberte možnost „Řetězec\TEXT“.</span><span class="sxs-lookup"><span data-stu-id="89723-158">In the tree, select 'String\TEXT'.</span></span>
21. <span data-ttu-id="89723-159">Klikněte na možnost Přidat funkci.</span><span class="sxs-lookup"><span data-stu-id="89723-159">Click Add function.</span></span>
22. <span data-ttu-id="89723-160">Ve stromovém zobrazení vyberte možnost "Transakce\ID záznamu(RecId)".</span><span class="sxs-lookup"><span data-stu-id="89723-160">In the tree, select 'Transactions\Record-ID(RecId)'.</span></span>
23. <span data-ttu-id="89723-161">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="89723-161">Click Add data source.</span></span>
24. <span data-ttu-id="89723-162">V poli Vzorec zadejte 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span><span class="sxs-lookup"><span data-stu-id="89723-162">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span></span>
    * <span data-ttu-id="89723-163">Na konci receptury zadejte [))].</span><span class="sxs-lookup"><span data-stu-id="89723-163">Type [))] at the end of the formula.</span></span>  
25. <span data-ttu-id="89723-164">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="89723-164">Click Save.</span></span>
    * <span data-ttu-id="89723-165">Ověřte, že ve vytvořené receptuře nejsou žádné chyby.</span><span class="sxs-lookup"><span data-stu-id="89723-165">Make sure that no errors have been discovered for the created formula.</span></span> <span data-ttu-id="89723-166">Podívejte se na kartu CHYBY pod ovládacím prvkem editoru receptury.</span><span class="sxs-lookup"><span data-stu-id="89723-166">See the ERRORS tab below the formula editor control.</span></span>  
26. <span data-ttu-id="89723-167">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="89723-167">Close the page.</span></span>
27. <span data-ttu-id="89723-168">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="89723-168">Click OK.</span></span>
    * <span data-ttu-id="89723-169">Přidejte vypočítané pole k tomuto datovému zdroji.</span><span class="sxs-lookup"><span data-stu-id="89723-169">Add the calculated field to this data source.</span></span>  
28. <span data-ttu-id="89723-170">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="89723-170">Click Add.</span></span>
    * <span data-ttu-id="89723-171">Kliknutím na tlačítko Přidat přidejte nové vypočítané pole.</span><span class="sxs-lookup"><span data-stu-id="89723-171">Click Add to add a new calculated field.</span></span>  
29. <span data-ttu-id="89723-172">Do pole Název zadejte „$Amount“.</span><span class="sxs-lookup"><span data-stu-id="89723-172">In the Name field, type '$Amount'.</span></span>
    * <span data-ttu-id="89723-173">$Částka</span><span class="sxs-lookup"><span data-stu-id="89723-173">$Amount</span></span>  
30. <span data-ttu-id="89723-174">Klikněte na možnost Upravit vzorec.</span><span class="sxs-lookup"><span data-stu-id="89723-174">Click Edit formula.</span></span>
31. <span data-ttu-id="89723-175">Ve stromovém zobrazení rozbalte možnost Transakce.</span><span class="sxs-lookup"><span data-stu-id="89723-175">In the tree, expand 'Transactions'.</span></span>
32. <span data-ttu-id="89723-176">Ve stromovém zobrazení vyberte možnost "Transakce\Má dáti(AmountCurDebit)".</span><span class="sxs-lookup"><span data-stu-id="89723-176">In the tree, select 'Transactions\Debit(AmountCurDebit)'.</span></span>
33. <span data-ttu-id="89723-177">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="89723-177">Click Add data source.</span></span>
34. <span data-ttu-id="89723-178">V poli Vzorec zadejte 'Transactions.AmountCurDebit - '.</span><span class="sxs-lookup"><span data-stu-id="89723-178">In the Formula field, enter 'Transactions.AmountCurDebit - '.</span></span>
    * <span data-ttu-id="89723-179">Na konci receptury zadejte [ - ].</span><span class="sxs-lookup"><span data-stu-id="89723-179">Type [ - ] at the end of the formula.</span></span>  
35. <span data-ttu-id="89723-180">Ve stromovém zobrazení vyberte možnost "Transakce\Dal(AmountCurCredit)".</span><span class="sxs-lookup"><span data-stu-id="89723-180">In the tree, select 'Transactions\Credit(AmountCurCredit)'.</span></span>
36. <span data-ttu-id="89723-181">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="89723-181">Click Add data source.</span></span>
37. <span data-ttu-id="89723-182">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="89723-182">Click Save.</span></span>
38. <span data-ttu-id="89723-183">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="89723-183">Close the page.</span></span>
39. <span data-ttu-id="89723-184">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="89723-184">Click OK.</span></span>
    * <span data-ttu-id="89723-185">Tím se přidá vypočtené pole $Amount k vybranému zdroji dat pro aktuální datový model.</span><span class="sxs-lookup"><span data-stu-id="89723-185">This will add the $Amount calculated field to the selected data source for the current data model.</span></span>  
40. <span data-ttu-id="89723-186">Ve stromovém zobrazení vyberte možnost Transactions\$Amount.</span><span class="sxs-lookup"><span data-stu-id="89723-186">In the tree, select 'Transactions\$Amount'.</span></span>
41. <span data-ttu-id="89723-187">Ve stromovém zobrazení rozbalte možnost Transakce.</span><span class="sxs-lookup"><span data-stu-id="89723-187">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="89723-188">Ve stromové struktuře rozbalte nebo sbalte Transactions\$Amount.</span><span class="sxs-lookup"><span data-stu-id="89723-188">In the tree, expand or collapse 'Transactions\$Amount'.</span></span>
43. <span data-ttu-id="89723-189">Ve stromové struktuře rozbalte nebo sbalte 'Transakce'.</span><span class="sxs-lookup"><span data-stu-id="89723-189">In the tree, expand or collapse 'Transactions'.</span></span>
44. <span data-ttu-id="89723-190">Ve stromové struktuře vyberte Dynamics 365 for Operations\Záznamy tabulky.</span><span class="sxs-lookup"><span data-stu-id="89723-190">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
45. <span data-ttu-id="89723-191">Klikněte na možnost Přidat kořen.</span><span class="sxs-lookup"><span data-stu-id="89723-191">Click Add root.</span></span>
    * <span data-ttu-id="89723-192">Zadejte tento zdroj dat pro přístup k podrobnostem o bankovním účtu společnosti.</span><span class="sxs-lookup"><span data-stu-id="89723-192">Enter this data source to access the company’s bank account details.</span></span>  
46. <span data-ttu-id="89723-193">Zadejte text „BankAccount“ do pole Název.</span><span class="sxs-lookup"><span data-stu-id="89723-193">In the Name field, type 'BankAccount'.</span></span>
    * <span data-ttu-id="89723-194">Bankovní účet</span><span class="sxs-lookup"><span data-stu-id="89723-194">BankAccount</span></span>  
47. <span data-ttu-id="89723-195">Zadejte text „Bankovní účet“ do pole Popisek.</span><span class="sxs-lookup"><span data-stu-id="89723-195">In the Label field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="89723-196">Bankovní účet</span><span class="sxs-lookup"><span data-stu-id="89723-196">Bank Account</span></span>  
48. <span data-ttu-id="89723-197">Zadejte text „Bankovní účet“ do pole Nápověda.</span><span class="sxs-lookup"><span data-stu-id="89723-197">In the Help field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="89723-198">Bankovní účet</span><span class="sxs-lookup"><span data-stu-id="89723-198">Bank Account</span></span>  
49. <span data-ttu-id="89723-199">Vyberte možnost Ano v poli Zeptat se na dotaz.</span><span class="sxs-lookup"><span data-stu-id="89723-199">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="89723-200">Vyberte možnost Ano.</span><span class="sxs-lookup"><span data-stu-id="89723-200">Select Yes.</span></span>  
50. <span data-ttu-id="89723-201">Do pole Tabulka zadejte hodnotu „BankAccountTable“.</span><span class="sxs-lookup"><span data-stu-id="89723-201">In the Table field, type 'BankAccountTable'.</span></span>
    * <span data-ttu-id="89723-202">BankAccountTable</span><span class="sxs-lookup"><span data-stu-id="89723-202">BankAccountTable</span></span>  
51. <span data-ttu-id="89723-203">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="89723-203">Click OK.</span></span>
    * <span data-ttu-id="89723-204">Vyberte tabulku BankAccountTable jako zdroj dat pro aktuální datový model.</span><span class="sxs-lookup"><span data-stu-id="89723-204">Select the BankAccountTable table as a data source for the current data model.</span></span>  
52. <span data-ttu-id="89723-205">Klikněte na možnost Přidat kořen.</span><span class="sxs-lookup"><span data-stu-id="89723-205">Click Add root.</span></span>
    * <span data-ttu-id="89723-206">Zadejte tento zdroj dat pro přístup k požadavkům společnosti.</span><span class="sxs-lookup"><span data-stu-id="89723-206">Enter this data source to access the company’s requisites.</span></span>  
53. <span data-ttu-id="89723-207">Do pole Název zadejte text „Společnost“.</span><span class="sxs-lookup"><span data-stu-id="89723-207">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="89723-208">Společnost</span><span class="sxs-lookup"><span data-stu-id="89723-208">Company</span></span>  
54. <span data-ttu-id="89723-209">Zadejte hodnotu do pole Popisek.</span><span class="sxs-lookup"><span data-stu-id="89723-209">In the Label field, type a value.</span></span>
    * <span data-ttu-id="89723-210">Informace o společnosti</span><span class="sxs-lookup"><span data-stu-id="89723-210">Company information</span></span>  
55. <span data-ttu-id="89723-211">Do pole Nápověda zadejte „Informace o společnosti“.</span><span class="sxs-lookup"><span data-stu-id="89723-211">In the Help field, enter 'Company information'.</span></span>
    * <span data-ttu-id="89723-212">Informace o společnosti</span><span class="sxs-lookup"><span data-stu-id="89723-212">Company information</span></span>  
56. <span data-ttu-id="89723-213">Vyberte možnost Ano v poli Zeptat se na dotaz.</span><span class="sxs-lookup"><span data-stu-id="89723-213">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="89723-214">Vyberte možnost Ano.</span><span class="sxs-lookup"><span data-stu-id="89723-214">Select Yes.</span></span>  
57. <span data-ttu-id="89723-215">Do pole Tabulka zadejte hodnotu „CompanyInfo“.</span><span class="sxs-lookup"><span data-stu-id="89723-215">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="89723-216">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="89723-216">CompanyInfo</span></span>  
58. <span data-ttu-id="89723-217">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="89723-217">Click OK.</span></span>
    * <span data-ttu-id="89723-218">Vyberte tabulku CompanyInfo jako zdroj dat pro aktuální datový model.</span><span class="sxs-lookup"><span data-stu-id="89723-218">Select the CompanyInfo table as a data source for the current data model.</span></span>  
59. <span data-ttu-id="89723-219">Ve stromovém zobrazení vyberte možnost „Funkce\Počítané pole“.</span><span class="sxs-lookup"><span data-stu-id="89723-219">In the tree, select 'Functions\Calculated field'.</span></span>
60. <span data-ttu-id="89723-220">Klikněte na možnost Přidat kořen.</span><span class="sxs-lookup"><span data-stu-id="89723-220">Click Add root.</span></span>
    * <span data-ttu-id="89723-221">Vložte vypočítané pole jako nový zdroj dat.</span><span class="sxs-lookup"><span data-stu-id="89723-221">Insert a calculated field as a new data source.</span></span>  
61. <span data-ttu-id="89723-222">Do pole Název zadejte „ProcessingDateTime“.</span><span class="sxs-lookup"><span data-stu-id="89723-222">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="89723-223">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="89723-223">ProcessingDateTime</span></span>  
62. <span data-ttu-id="89723-224">Do pole Popisek zadejte „Datum a čas zpracování“.</span><span class="sxs-lookup"><span data-stu-id="89723-224">In the Label field, enter 'Processing date & time'.</span></span>
    * <span data-ttu-id="89723-225">Datum a čas zpracování</span><span class="sxs-lookup"><span data-stu-id="89723-225">Processing date & time</span></span>  
63. <span data-ttu-id="89723-226">Klikněte na možnost Upravit vzorec.</span><span class="sxs-lookup"><span data-stu-id="89723-226">Click Edit formula.</span></span>
64. <span data-ttu-id="89723-227">Ve stromové struktuře vyberte 'Datum/čas\SESSIONNOW'.</span><span class="sxs-lookup"><span data-stu-id="89723-227">In the tree, select 'Date/time\SESSIONNOW'.</span></span>
65. <span data-ttu-id="89723-228">Klikněte na možnost Přidat funkci.</span><span class="sxs-lookup"><span data-stu-id="89723-228">Click Add function.</span></span>
66. <span data-ttu-id="89723-229">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="89723-229">Click Save.</span></span>
67. <span data-ttu-id="89723-230">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="89723-230">Close the page.</span></span>
68. <span data-ttu-id="89723-231">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="89723-231">Click OK.</span></span>
    * <span data-ttu-id="89723-232">Přidejte vypočítané pole ProcessingDateTime jako zdroj dat pro aktuální model data.</span><span class="sxs-lookup"><span data-stu-id="89723-232">Add the ProcessingDateTime calculated field as a data source for the current data model.</span></span>  
69. <span data-ttu-id="89723-233">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="89723-233">Click Save.</span></span>
70. <span data-ttu-id="89723-234">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="89723-234">Close the page.</span></span>
71. <span data-ttu-id="89723-235">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="89723-235">Close the page.</span></span>
72. <span data-ttu-id="89723-236">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="89723-236">Close the page.</span></span>


