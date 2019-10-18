---
title: Definování mapování modelů elektronického výkaznictví a výběr zdrojů dat
description: Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vybrat zdroje dat pro datový model Elektronické výkaznictví.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46dc13416aa094f33879c017c1a1815fc791409d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185099"
---
# <a name="define-er-model-mappings-and-select-data-sources-for-them"></a><span data-ttu-id="b659a-103">Definování mapování modelů elektronického výkaznictví a výběr zdrojů dat</span><span class="sxs-lookup"><span data-stu-id="b659a-103">Define ER model mappings and select data sources for them</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b659a-104">Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vybrat zdroje dat pro datový model Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="b659a-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can select data sources for an Electronic reporting (ER) data model.</span></span> <span data-ttu-id="b659a-105">Zdroje dat budou v době návrhu vázány k jednotlivých součástem vybraného datového modelu a za běhu vyplní obchodní data do datového modelu.</span><span class="sxs-lookup"><span data-stu-id="b659a-105">The data sources will be bound to individual components of the selected data model at design time and populate business data to that data model at run-time.</span></span> <span data-ttu-id="b659a-106">V tomto příkladu budete vybírat zdroje dat pro existující datový model, který byl vytvořen pro vzorovou společnost Litware, Inc. K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu Vytvoření nového datového modelu.</span><span class="sxs-lookup"><span data-stu-id="b659a-106">In this example, you will select data sources for an existing data model that has been created for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Create a new data model” procedure.</span></span>


## <a name="open-the-electronic-reporting-configurations-tree"></a><span data-ttu-id="b659a-107">Otevření stromu konfigurací elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="b659a-107">Open the Electronic Reporting configurations tree</span></span>
1. <span data-ttu-id="b659a-108">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="b659a-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="b659a-109">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="b659a-109">Click Reporting configurations.</span></span>

## <a name="insert-a-new-model-mapping"></a><span data-ttu-id="b659a-110">Vložení nového mapování modelu</span><span class="sxs-lookup"><span data-stu-id="b659a-110">Insert a new model mapping</span></span>
1. <span data-ttu-id="b659a-111">Ve stromovém zobrazení vyberte možnost „Platby (zjednodušený model)“.</span><span class="sxs-lookup"><span data-stu-id="b659a-111">In the tree, select 'Payments (simplified model)'.</span></span>
2. <span data-ttu-id="b659a-112">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="b659a-112">Click Designer.</span></span>
3. <span data-ttu-id="b659a-113">Klikněte na možnost Mapovat model na datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="b659a-113">Click Map model to datasource.</span></span>
4. <span data-ttu-id="b659a-114">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b659a-114">Click New.</span></span>
    * <span data-ttu-id="b659a-115">Tím vytvoříte nový záznam, který namapuje datový model na zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="b659a-115">This will create a new record that will map the data model to data sources.</span></span> <span data-ttu-id="b659a-116">V tomto příkladu namapujete datový model na zdroje dat pro požadovaný typ platby: peněžní převod.</span><span class="sxs-lookup"><span data-stu-id="b659a-116">In this example, you will map the data model to data sources for the desired payment type: credit transfer.</span></span>     <span data-ttu-id="b659a-117">Pro konkrétní datový model lze navrhnout více mapování.</span><span class="sxs-lookup"><span data-stu-id="b659a-117">It is possible to design more than one mapping for a particular data model.</span></span> <span data-ttu-id="b659a-118">Například můžete vytvořit mapování pro různé typy plateb, jako je například pro přímý debet nebo peněžní převody.</span><span class="sxs-lookup"><span data-stu-id="b659a-118">For example, you could create a mapping for the different types of payments, such as for direct debit or for credit transfers.</span></span> <span data-ttu-id="b659a-119">V tomto příkladu vytvoříte mapování pro peněžní převody.</span><span class="sxs-lookup"><span data-stu-id="b659a-119">In this example, you will create a mapping for credit transfers.</span></span>  
5. <span data-ttu-id="b659a-120">Zadejte text „Mapování Dal“ do pole Název.</span><span class="sxs-lookup"><span data-stu-id="b659a-120">In the Name field, type 'CT mapping'.</span></span>
    * <span data-ttu-id="b659a-121">Mapování Dal</span><span class="sxs-lookup"><span data-stu-id="b659a-121">CT mapping</span></span>  
6. <span data-ttu-id="b659a-122">V poli Popis zadejte „Model platby pro mapování Dal“.</span><span class="sxs-lookup"><span data-stu-id="b659a-122">In the Description field, type 'Payment model mapping CT'.</span></span>
    * <span data-ttu-id="b659a-123">Model platby pro mapování Dal</span><span class="sxs-lookup"><span data-stu-id="b659a-123">Payment model mapping CT</span></span>  
7. <span data-ttu-id="b659a-124">Zadejte hodnotu CustomerCreditTransferInitiation do pole Definice.</span><span class="sxs-lookup"><span data-stu-id="b659a-124">In the Definition field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="b659a-125">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="b659a-125">CustomerCreditTransferInitiation</span></span>  
8. <span data-ttu-id="b659a-126">ResolveChanges Definice.</span><span class="sxs-lookup"><span data-stu-id="b659a-126">ResolveChanges the Definition.</span></span>
9. <span data-ttu-id="b659a-127">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b659a-127">Click Save.</span></span>

## <a name="define-required-data-sources-for-the-current-model-mapping"></a><span data-ttu-id="b659a-128">Definování požadovaných zdrojů dat pro aktuální mapování modelu</span><span class="sxs-lookup"><span data-stu-id="b659a-128">Define required data sources for the current model mapping</span></span>
1. <span data-ttu-id="b659a-129">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="b659a-129">Click Designer.</span></span>
2. <span data-ttu-id="b659a-130">Ve stromovém zobrazení vyberte možnost 'Dynamics 365 for Operations\Záznamy v tabulce'.</span><span class="sxs-lookup"><span data-stu-id="b659a-130">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
3. <span data-ttu-id="b659a-131">Klikněte na možnost Přidat kořen.</span><span class="sxs-lookup"><span data-stu-id="b659a-131">Click Add root.</span></span>
    * <span data-ttu-id="b659a-132">Zadejte tento zdroj dat pro přístup k platebním transakcím.</span><span class="sxs-lookup"><span data-stu-id="b659a-132">Enter this data source to access payment transactions.</span></span>  
4. <span data-ttu-id="b659a-133">Zadejte text „Transakce“ do pole Název.</span><span class="sxs-lookup"><span data-stu-id="b659a-133">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="b659a-134">Transakce</span><span class="sxs-lookup"><span data-stu-id="b659a-134">Transactions</span></span>  
5. <span data-ttu-id="b659a-135">Zadejte text „Transakce“ do pole Popisek.</span><span class="sxs-lookup"><span data-stu-id="b659a-135">In the Label field, enter 'Transactions'.</span></span>
    * <span data-ttu-id="b659a-136">Transakce</span><span class="sxs-lookup"><span data-stu-id="b659a-136">Transactions</span></span>  
6. <span data-ttu-id="b659a-137">V poli Nápověda zadejte text „Řádky deníku hlavní knihy“.</span><span class="sxs-lookup"><span data-stu-id="b659a-137">In the Help field, enter 'Ledger journal lines'.</span></span>
    * <span data-ttu-id="b659a-138">Řádky deníku hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="b659a-138">Ledger journal lines</span></span>  
7. <span data-ttu-id="b659a-139">Vyberte možnost Ano v poli Zeptat se na dotaz.</span><span class="sxs-lookup"><span data-stu-id="b659a-139">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="b659a-140">Vyberte možnost Ano.</span><span class="sxs-lookup"><span data-stu-id="b659a-140">Select Yes.</span></span>  
8. <span data-ttu-id="b659a-141">Do pole Tabulka zadejte hodnotu „LedgerJournalTrans“.</span><span class="sxs-lookup"><span data-stu-id="b659a-141">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="b659a-142">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="b659a-142">LedgerJournalTrans</span></span>  
9. <span data-ttu-id="b659a-143">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b659a-143">Click OK.</span></span>
    * <span data-ttu-id="b659a-144">Vyberte tabulku LedgerJournalTrans jako zdroj dat pro aktuální datový model.</span><span class="sxs-lookup"><span data-stu-id="b659a-144">Select the LedgerJournalTrans table as a data source for the current data model.</span></span>  
10. <span data-ttu-id="b659a-145">Ve stromovém zobrazení vyberte možnost „Funkce\Počítané pole“.</span><span class="sxs-lookup"><span data-stu-id="b659a-145">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="b659a-146">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="b659a-146">Click Add.</span></span>
    * <span data-ttu-id="b659a-147">Kliknutím na tlačítko Přidat přidejte nové vypočítané pole.</span><span class="sxs-lookup"><span data-stu-id="b659a-147">Click Add to add a new calculated field.</span></span>  
12. <span data-ttu-id="b659a-148">Zadejte text „$EndToEndID“ do pole Název.</span><span class="sxs-lookup"><span data-stu-id="b659a-148">In the Name field, type '$EndToEndID'.</span></span>
    * <span data-ttu-id="b659a-149">$EndToEndID</span><span class="sxs-lookup"><span data-stu-id="b659a-149">$EndToEndID</span></span>  
13. <span data-ttu-id="b659a-150">Klikněte na možnost Upravit vzorec.</span><span class="sxs-lookup"><span data-stu-id="b659a-150">Click Edit formula.</span></span>
14. <span data-ttu-id="b659a-151">Ve stromovém zobrazení vyberte možnost „Řetězec\SLOUČIT“.</span><span class="sxs-lookup"><span data-stu-id="b659a-151">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="b659a-152">Klikněte na možnost Přidat funkci.</span><span class="sxs-lookup"><span data-stu-id="b659a-152">Click Add function.</span></span>
16. <span data-ttu-id="b659a-153">Ve stromovém zobrazení rozbalte možnost Transakce.</span><span class="sxs-lookup"><span data-stu-id="b659a-153">In the tree, expand 'Transactions'.</span></span>
17. <span data-ttu-id="b659a-154">Ve stromovém zobrazení vyberte možnost „Transakce\Doklad“.</span><span class="sxs-lookup"><span data-stu-id="b659a-154">In the tree, select 'Transactions\Voucher'.</span></span>
18. <span data-ttu-id="b659a-155">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="b659a-155">Click Add data source.</span></span>
19. <span data-ttu-id="b659a-156">V poli Vzorec zadejte 'CONCATENATE(Transactions.Voucher, "-", '.</span><span class="sxs-lookup"><span data-stu-id="b659a-156">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", '.</span></span>
    * <span data-ttu-id="b659a-157">Na konci receptury zadejte [ , “-“, ].</span><span class="sxs-lookup"><span data-stu-id="b659a-157">Type [ , “-“, ] at the end of the formula.</span></span>  
20. <span data-ttu-id="b659a-158">Ve stromovém zobrazení vyberte možnost „Řetězec\TEXT“.</span><span class="sxs-lookup"><span data-stu-id="b659a-158">In the tree, select 'String\TEXT'.</span></span>
21. <span data-ttu-id="b659a-159">Klikněte na možnost Přidat funkci.</span><span class="sxs-lookup"><span data-stu-id="b659a-159">Click Add function.</span></span>
22. <span data-ttu-id="b659a-160">Ve stromovém zobrazení vyberte možnost "Transakce\ID záznamu(RecId)".</span><span class="sxs-lookup"><span data-stu-id="b659a-160">In the tree, select 'Transactions\Record-ID(RecId)'.</span></span>
23. <span data-ttu-id="b659a-161">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="b659a-161">Click Add data source.</span></span>
24. <span data-ttu-id="b659a-162">V poli Vzorec zadejte 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span><span class="sxs-lookup"><span data-stu-id="b659a-162">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span></span>
    * <span data-ttu-id="b659a-163">Na konci receptury zadejte [))].</span><span class="sxs-lookup"><span data-stu-id="b659a-163">Type [))] at the end of the formula.</span></span>  
25. <span data-ttu-id="b659a-164">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b659a-164">Click Save.</span></span>
    * <span data-ttu-id="b659a-165">Ověřte, že ve vytvořené receptuře nejsou žádné chyby.</span><span class="sxs-lookup"><span data-stu-id="b659a-165">Make sure that no errors have been discovered for the created formula.</span></span> <span data-ttu-id="b659a-166">Podívejte se na kartu CHYBY pod ovládacím prvkem editoru receptury.</span><span class="sxs-lookup"><span data-stu-id="b659a-166">See the ERRORS tab below the formula editor control.</span></span>  
26. <span data-ttu-id="b659a-167">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b659a-167">Close the page.</span></span>
27. <span data-ttu-id="b659a-168">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b659a-168">Click OK.</span></span>
    * <span data-ttu-id="b659a-169">Přidejte vypočítané pole k tomuto datovému zdroji.</span><span class="sxs-lookup"><span data-stu-id="b659a-169">Add the calculated field to this data source.</span></span>  
28. <span data-ttu-id="b659a-170">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="b659a-170">Click Add.</span></span>
    * <span data-ttu-id="b659a-171">Kliknutím na tlačítko Přidat přidejte nové vypočítané pole.</span><span class="sxs-lookup"><span data-stu-id="b659a-171">Click Add to add a new calculated field.</span></span>  
29. <span data-ttu-id="b659a-172">Do pole Název zadejte „$Amount“.</span><span class="sxs-lookup"><span data-stu-id="b659a-172">In the Name field, type '$Amount'.</span></span>
    * <span data-ttu-id="b659a-173">$Částka</span><span class="sxs-lookup"><span data-stu-id="b659a-173">$Amount</span></span>  
30. <span data-ttu-id="b659a-174">Klikněte na možnost Upravit vzorec.</span><span class="sxs-lookup"><span data-stu-id="b659a-174">Click Edit formula.</span></span>
31. <span data-ttu-id="b659a-175">Ve stromovém zobrazení rozbalte možnost Transakce.</span><span class="sxs-lookup"><span data-stu-id="b659a-175">In the tree, expand 'Transactions'.</span></span>
32. <span data-ttu-id="b659a-176">Ve stromovém zobrazení vyberte možnost "Transakce\Má dáti(AmountCurDebit)".</span><span class="sxs-lookup"><span data-stu-id="b659a-176">In the tree, select 'Transactions\Debit(AmountCurDebit)'.</span></span>
33. <span data-ttu-id="b659a-177">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="b659a-177">Click Add data source.</span></span>
34. <span data-ttu-id="b659a-178">V poli Vzorec zadejte 'Transactions.AmountCurDebit - '.</span><span class="sxs-lookup"><span data-stu-id="b659a-178">In the Formula field, enter 'Transactions.AmountCurDebit - '.</span></span>
    * <span data-ttu-id="b659a-179">Na konci receptury zadejte [ - ].</span><span class="sxs-lookup"><span data-stu-id="b659a-179">Type [ - ] at the end of the formula.</span></span>  
35. <span data-ttu-id="b659a-180">Ve stromovém zobrazení vyberte možnost "Transakce\Dal(AmountCurCredit)".</span><span class="sxs-lookup"><span data-stu-id="b659a-180">In the tree, select 'Transactions\Credit(AmountCurCredit)'.</span></span>
36. <span data-ttu-id="b659a-181">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="b659a-181">Click Add data source.</span></span>
37. <span data-ttu-id="b659a-182">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b659a-182">Click Save.</span></span>
38. <span data-ttu-id="b659a-183">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b659a-183">Close the page.</span></span>
39. <span data-ttu-id="b659a-184">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b659a-184">Click OK.</span></span>
    * <span data-ttu-id="b659a-185">Tím se přidá vypočtené pole $Amount k vybranému zdroji dat pro aktuální datový model.</span><span class="sxs-lookup"><span data-stu-id="b659a-185">This will add the $Amount calculated field to the selected data source for the current data model.</span></span>  
40. <span data-ttu-id="b659a-186">Ve stromovém zobrazení vyberte možnost Transactions\$Amount.</span><span class="sxs-lookup"><span data-stu-id="b659a-186">In the tree, select 'Transactions\$Amount'.</span></span>
41. <span data-ttu-id="b659a-187">Ve stromovém zobrazení rozbalte možnost Transakce.</span><span class="sxs-lookup"><span data-stu-id="b659a-187">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="b659a-188">Ve stromové struktuře rozbalte nebo sbalte Transactions\$Amount.</span><span class="sxs-lookup"><span data-stu-id="b659a-188">In the tree, expand or collapse 'Transactions\$Amount'.</span></span>
43. <span data-ttu-id="b659a-189">Ve stromové struktuře rozbalte nebo sbalte 'Transakce'.</span><span class="sxs-lookup"><span data-stu-id="b659a-189">In the tree, expand or collapse 'Transactions'.</span></span>
44. <span data-ttu-id="b659a-190">Ve stromovém zobrazení vyberte možnost 'Dynamics 365 for Operations\Záznamy v tabulce'.</span><span class="sxs-lookup"><span data-stu-id="b659a-190">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
45. <span data-ttu-id="b659a-191">Klikněte na možnost Přidat kořen.</span><span class="sxs-lookup"><span data-stu-id="b659a-191">Click Add root.</span></span>
    * <span data-ttu-id="b659a-192">Zadejte tento zdroj dat pro přístup k podrobnostem o bankovním účtu společnosti.</span><span class="sxs-lookup"><span data-stu-id="b659a-192">Enter this data source to access the company’s bank account details.</span></span>  
46. <span data-ttu-id="b659a-193">Zadejte text „BankAccount“ do pole Název.</span><span class="sxs-lookup"><span data-stu-id="b659a-193">In the Name field, type 'BankAccount'.</span></span>
    * <span data-ttu-id="b659a-194">Bankovní účet</span><span class="sxs-lookup"><span data-stu-id="b659a-194">BankAccount</span></span>  
47. <span data-ttu-id="b659a-195">Zadejte text „Bankovní účet“ do pole Popisek.</span><span class="sxs-lookup"><span data-stu-id="b659a-195">In the Label field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="b659a-196">Bankovní účet</span><span class="sxs-lookup"><span data-stu-id="b659a-196">Bank Account</span></span>  
48. <span data-ttu-id="b659a-197">Zadejte text „Bankovní účet“ do pole Nápověda.</span><span class="sxs-lookup"><span data-stu-id="b659a-197">In the Help field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="b659a-198">Bankovní účet</span><span class="sxs-lookup"><span data-stu-id="b659a-198">Bank Account</span></span>  
49. <span data-ttu-id="b659a-199">Vyberte možnost Ano v poli Zeptat se na dotaz.</span><span class="sxs-lookup"><span data-stu-id="b659a-199">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="b659a-200">Vyberte možnost Ano.</span><span class="sxs-lookup"><span data-stu-id="b659a-200">Select Yes.</span></span>  
50. <span data-ttu-id="b659a-201">Do pole Tabulka zadejte hodnotu „BankAccountTable“.</span><span class="sxs-lookup"><span data-stu-id="b659a-201">In the Table field, type 'BankAccountTable'.</span></span>
    * <span data-ttu-id="b659a-202">BankAccountTable</span><span class="sxs-lookup"><span data-stu-id="b659a-202">BankAccountTable</span></span>  
51. <span data-ttu-id="b659a-203">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b659a-203">Click OK.</span></span>
    * <span data-ttu-id="b659a-204">Vyberte tabulku BankAccountTable jako zdroj dat pro aktuální datový model.</span><span class="sxs-lookup"><span data-stu-id="b659a-204">Select the BankAccountTable table as a data source for the current data model.</span></span>  
52. <span data-ttu-id="b659a-205">Klikněte na možnost Přidat kořen.</span><span class="sxs-lookup"><span data-stu-id="b659a-205">Click Add root.</span></span>
    * <span data-ttu-id="b659a-206">Zadejte tento zdroj dat pro přístup k požadavkům společnosti.</span><span class="sxs-lookup"><span data-stu-id="b659a-206">Enter this data source to access the company’s requisites.</span></span>  
53. <span data-ttu-id="b659a-207">Do pole Název zadejte text „Společnost“.</span><span class="sxs-lookup"><span data-stu-id="b659a-207">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="b659a-208">Společnost</span><span class="sxs-lookup"><span data-stu-id="b659a-208">Company</span></span>  
54. <span data-ttu-id="b659a-209">Zadejte hodnotu do pole Popisek.</span><span class="sxs-lookup"><span data-stu-id="b659a-209">In the Label field, type a value.</span></span>
    * <span data-ttu-id="b659a-210">Informace o společnosti</span><span class="sxs-lookup"><span data-stu-id="b659a-210">Company information</span></span>  
55. <span data-ttu-id="b659a-211">Do pole Nápověda zadejte „Informace o společnosti“.</span><span class="sxs-lookup"><span data-stu-id="b659a-211">In the Help field, enter 'Company information'.</span></span>
    * <span data-ttu-id="b659a-212">Informace o společnosti</span><span class="sxs-lookup"><span data-stu-id="b659a-212">Company information</span></span>  
56. <span data-ttu-id="b659a-213">Vyberte možnost Ano v poli Zeptat se na dotaz.</span><span class="sxs-lookup"><span data-stu-id="b659a-213">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="b659a-214">Vyberte možnost Ano.</span><span class="sxs-lookup"><span data-stu-id="b659a-214">Select Yes.</span></span>  
57. <span data-ttu-id="b659a-215">Do pole Tabulka zadejte hodnotu „CompanyInfo“.</span><span class="sxs-lookup"><span data-stu-id="b659a-215">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="b659a-216">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="b659a-216">CompanyInfo</span></span>  
58. <span data-ttu-id="b659a-217">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b659a-217">Click OK.</span></span>
    * <span data-ttu-id="b659a-218">Vyberte tabulku CompanyInfo jako zdroj dat pro aktuální datový model.</span><span class="sxs-lookup"><span data-stu-id="b659a-218">Select the CompanyInfo table as a data source for the current data model.</span></span>  
59. <span data-ttu-id="b659a-219">Ve stromovém zobrazení vyberte možnost „Funkce\Počítané pole“.</span><span class="sxs-lookup"><span data-stu-id="b659a-219">In the tree, select 'Functions\Calculated field'.</span></span>
60. <span data-ttu-id="b659a-220">Klikněte na možnost Přidat kořen.</span><span class="sxs-lookup"><span data-stu-id="b659a-220">Click Add root.</span></span>
    * <span data-ttu-id="b659a-221">Vložte vypočítané pole jako nový zdroj dat.</span><span class="sxs-lookup"><span data-stu-id="b659a-221">Insert a calculated field as a new data source.</span></span>  
61. <span data-ttu-id="b659a-222">Do pole Název zadejte „ProcessingDateTime“.</span><span class="sxs-lookup"><span data-stu-id="b659a-222">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="b659a-223">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="b659a-223">ProcessingDateTime</span></span>  
62. <span data-ttu-id="b659a-224">Do pole Popisek zadejte „Datum a čas zpracování“.</span><span class="sxs-lookup"><span data-stu-id="b659a-224">In the Label field, enter 'Processing date & time'.</span></span>
    * <span data-ttu-id="b659a-225">Datum a čas zpracování</span><span class="sxs-lookup"><span data-stu-id="b659a-225">Processing date & time</span></span>  
63. <span data-ttu-id="b659a-226">Klikněte na možnost Upravit vzorec.</span><span class="sxs-lookup"><span data-stu-id="b659a-226">Click Edit formula.</span></span>
64. <span data-ttu-id="b659a-227">Ve stromové struktuře vyberte 'Datum/čas\SESSIONNOW'.</span><span class="sxs-lookup"><span data-stu-id="b659a-227">In the tree, select 'Date/time\SESSIONNOW'.</span></span>
65. <span data-ttu-id="b659a-228">Klikněte na možnost Přidat funkci.</span><span class="sxs-lookup"><span data-stu-id="b659a-228">Click Add function.</span></span>
66. <span data-ttu-id="b659a-229">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b659a-229">Click Save.</span></span>
67. <span data-ttu-id="b659a-230">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b659a-230">Close the page.</span></span>
68. <span data-ttu-id="b659a-231">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b659a-231">Click OK.</span></span>
    * <span data-ttu-id="b659a-232">Přidejte vypočítané pole ProcessingDateTime jako zdroj dat pro aktuální model data.</span><span class="sxs-lookup"><span data-stu-id="b659a-232">Add the ProcessingDateTime calculated field as a data source for the current data model.</span></span>  
69. <span data-ttu-id="b659a-233">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b659a-233">Click Save.</span></span>
70. <span data-ttu-id="b659a-234">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b659a-234">Close the page.</span></span>
71. <span data-ttu-id="b659a-235">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b659a-235">Close the page.</span></span>
72. <span data-ttu-id="b659a-236">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b659a-236">Close the page.</span></span>

