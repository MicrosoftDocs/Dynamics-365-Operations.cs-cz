---
title: Použití konfigurací mapování modelu pro agregované výpočty na úrovni databáze
description: Toto téma popisuje, jak navrhnout novou konfiguraci mapování modelu elektronického výkaznictví a použít integrované funkce ER k efektivním agregovaným výpočtům.
author: NickSelin
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 01f48596c30127976d915811ffa8412dcc9b2593
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745368"
---
# <a name="use-model-mapping-configurations-for-aggregate-calculations-at-the-database-level"></a><span data-ttu-id="ff229-103">Použití konfigurací mapování modelu pro agregované výpočty na úrovni databáze</span><span class="sxs-lookup"><span data-stu-id="ff229-103">Use model mapping configurations for aggregate calculations at the database level</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ff229-104">Tento postup poskytuje informace o způsobu navržení nové konfigurace mapování modelu elektronického výkaznictví a použití integrovaných funkcí ER k efektivním agregovaným výpočtům.</span><span class="sxs-lookup"><span data-stu-id="ff229-104">This procedure provides information about how to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="ff229-105">V tomto postupu vytvoříte konfiguraci pro vzorovou společnost Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="ff229-105">In this procedure you will create a configuration for the sample company, Litware, Inc.</span></span> 

<span data-ttu-id="ff229-106">Tento postup je vytvořen pro uživatele s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování.</span><span class="sxs-lookup"><span data-stu-id="ff229-106">This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> <span data-ttu-id="ff229-107">Tyto kroky lze dokončit za použití libovolné datové sady.</span><span class="sxs-lookup"><span data-stu-id="ff229-107">These steps can be completed using any dataset.</span></span>

 <span data-ttu-id="ff229-108">Provedení těchto kroků vyžaduje provedení kroků v postupu „ER vylepšuje efektivitu souhrnných výpočtů provedením na úrovni databáze (část 1: Příprava konfigurace)“.</span><span class="sxs-lookup"><span data-stu-id="ff229-108">To complete these steps, you must first complete the steps in the procedure, "ER improves the efficiency of aggregate calculations by performing them on database level (Part 1: Prepare configurations)."</span></span>

1. <span data-ttu-id="ff229-109">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="ff229-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="ff229-110">Ve stromovém zobrazení rozbalte „Modul Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="ff229-110">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="ff229-111">Ve stromové struktuře vyberte 'Intrastat model\Intrastat sample mapping'.</span><span class="sxs-lookup"><span data-stu-id="ff229-111">In the tree, select 'Intrastat model\Intrastat sample mapping'.</span></span>
4. <span data-ttu-id="ff229-112">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="ff229-112">Click Designer.</span></span>
5. <span data-ttu-id="ff229-113">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="ff229-113">Click Designer.</span></span>
6. <span data-ttu-id="ff229-114">Ve stromovém zobrazení vyberte možnost 'Dynamics 365 for Operations\Záznamy v tabulce'.</span><span class="sxs-lookup"><span data-stu-id="ff229-114">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
7. <span data-ttu-id="ff229-115">Klikněte na možnost Přidat kořen.</span><span class="sxs-lookup"><span data-stu-id="ff229-115">Click Add root.</span></span>
    * <span data-ttu-id="ff229-116">Přidáte nový zdroj dat představující záznamy, které chcete seskupit.</span><span class="sxs-lookup"><span data-stu-id="ff229-116">Add a new data source representing records you want to group.</span></span>  
8. <span data-ttu-id="ff229-117">Zadejte text „Transakce“ do pole Název.</span><span class="sxs-lookup"><span data-stu-id="ff229-117">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="ff229-118">Transakce</span><span class="sxs-lookup"><span data-stu-id="ff229-118">Transactions</span></span>  
9. <span data-ttu-id="ff229-119">Do pole Tabulka zadejte hodnotu „Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="ff229-119">In the Table field, type 'Intrastat'.</span></span>
    * <span data-ttu-id="ff229-120">Systém Intrastat</span><span class="sxs-lookup"><span data-stu-id="ff229-120">Intrastat</span></span>  
10. <span data-ttu-id="ff229-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ff229-121">Click OK.</span></span>
11. <span data-ttu-id="ff229-122">Ve stromovém zobrazení vyberte možnost „Funkce\Seskupit podle “.</span><span class="sxs-lookup"><span data-stu-id="ff229-122">In the tree, select 'Functions\Group by'.</span></span>
    * <span data-ttu-id="ff229-123">Tento typ zdroje dat slouží k zavedení nového zdroje dat za běhu pro seskupení záznamů a výpočet požadovaných seskupení.</span><span class="sxs-lookup"><span data-stu-id="ff229-123">This data source type is used to introduce a new data source at run-time to group records and to calculate required aggregations.</span></span>  
12. <span data-ttu-id="ff229-124">Klikněte na možnost Přidat kořen.</span><span class="sxs-lookup"><span data-stu-id="ff229-124">Click Add root.</span></span>
13. <span data-ttu-id="ff229-125">Do pole Název zadejte TransactionsGroups.</span><span class="sxs-lookup"><span data-stu-id="ff229-125">In the Name field, type 'TransactionsGroups'.</span></span>
    * <span data-ttu-id="ff229-126">TransactionsGroups</span><span class="sxs-lookup"><span data-stu-id="ff229-126">TransactionsGroups</span></span>  
14. <span data-ttu-id="ff229-127">Klikněte na „Upravit skupinu podle“.</span><span class="sxs-lookup"><span data-stu-id="ff229-127">Click Edit group by.</span></span>
15. <span data-ttu-id="ff229-128">Ve stromovém zobrazení vyberte možnost „Transakce“.</span><span class="sxs-lookup"><span data-stu-id="ff229-128">In the tree, select 'Transactions'.</span></span>
    * <span data-ttu-id="ff229-129">Vyberte přidaný zdroj dat typu Seznam záznamů, který představuje záznamy pro seskupení.</span><span class="sxs-lookup"><span data-stu-id="ff229-129">Select the added data source of the 'Record list' type that represents the records that you want to group.</span></span>  
16. <span data-ttu-id="ff229-130">Klikněte na „Přidat pole do“.</span><span class="sxs-lookup"><span data-stu-id="ff229-130">Click Add field to.</span></span>
17. <span data-ttu-id="ff229-131">Klikněte na „Skupina Co“.</span><span class="sxs-lookup"><span data-stu-id="ff229-131">Click What to group.</span></span>
18. <span data-ttu-id="ff229-132">Ve stromovém zobrazení rozbalte možnost Transakce.</span><span class="sxs-lookup"><span data-stu-id="ff229-132">In the tree, expand 'Transactions'.</span></span>
19. <span data-ttu-id="ff229-133">Ve stromovém zobrazení vyberte možnost 'Transactions\Direction'.</span><span class="sxs-lookup"><span data-stu-id="ff229-133">In the tree, select 'Transactions\Direction'.</span></span>
20. <span data-ttu-id="ff229-134">Klikněte na „Přidat pole do“.</span><span class="sxs-lookup"><span data-stu-id="ff229-134">Click Add field to.</span></span>
21. <span data-ttu-id="ff229-135">Klikněte na „Seskupená pole“.</span><span class="sxs-lookup"><span data-stu-id="ff229-135">Click Grouped fields.</span></span>
    * <span data-ttu-id="ff229-136">Vyberte pole, pro určení úrovně seskupení.</span><span class="sxs-lookup"><span data-stu-id="ff229-136">Select the field to specify the grouping level.</span></span> <span data-ttu-id="ff229-137">Na základě tohoto výběru zdroj dat vrátí v době běhu tolik skupin transakcí, kolik je kódů směrování splněných v tabulce Intrastat.</span><span class="sxs-lookup"><span data-stu-id="ff229-137">Based on this selection, the data source will return at run-time as many groups of transactions as there are direction codes that will be met in the Intrastat table.</span></span>  
22. <span data-ttu-id="ff229-138">Ve stromovém zobrazení vyberte možnost 'Transactions\Invoice amount(AmountMST)'.</span><span class="sxs-lookup"><span data-stu-id="ff229-138">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
    * <span data-ttu-id="ff229-139">Vyberte pole pro určení zdroje k výpočtu seskupení.</span><span class="sxs-lookup"><span data-stu-id="ff229-139">Select the field to specify the source for aggregation calculation.</span></span>  
23. <span data-ttu-id="ff229-140">Klikněte na „Přidat pole do“.</span><span class="sxs-lookup"><span data-stu-id="ff229-140">Click Add field to.</span></span>
24. <span data-ttu-id="ff229-141">Klikněte na „Seskupená pole“.</span><span class="sxs-lookup"><span data-stu-id="ff229-141">Click Aggregation fields.</span></span>
25. <span data-ttu-id="ff229-142">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="ff229-142">In the list, mark the selected row.</span></span>
26. <span data-ttu-id="ff229-143">V poli Metoda vyberte možnost Součet.</span><span class="sxs-lookup"><span data-stu-id="ff229-143">In the Method field, select 'Sum'.</span></span>
    * <span data-ttu-id="ff229-144">Vyberte typ seskupení.</span><span class="sxs-lookup"><span data-stu-id="ff229-144">Select the aggregation type.</span></span>  
27. <span data-ttu-id="ff229-145">Do pole Název napište 'SumOfAmountMST'.</span><span class="sxs-lookup"><span data-stu-id="ff229-145">In the Name field, type 'SumOfAmountMST'.</span></span>
    * <span data-ttu-id="ff229-146">Zadejte název tohoto seskupení v konfigurovaném zdroji dat.</span><span class="sxs-lookup"><span data-stu-id="ff229-146">Specify the name of this aggregation in the configured data source.</span></span>  
28. <span data-ttu-id="ff229-147">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="ff229-147">Click Save.</span></span>
    * <span data-ttu-id="ff229-148">Pole Provedení v označuje, že toto seskupení bude provedeno v době běhu v databázi SQL.</span><span class="sxs-lookup"><span data-stu-id="ff229-148">Note that the 'Execution at' field indicates that this grouping will be performed at run-time in the SQL database.</span></span>  
29. <span data-ttu-id="ff229-149">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ff229-149">Close the page.</span></span>
30. <span data-ttu-id="ff229-150">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ff229-150">Click OK.</span></span>
31. <span data-ttu-id="ff229-151">Ve stromu rozbalte 'Totals'.</span><span class="sxs-lookup"><span data-stu-id="ff229-151">In the tree, expand 'Totals'.</span></span>
32. <span data-ttu-id="ff229-152">Ve stromu rozbalte 'TransactionsGroups'.</span><span class="sxs-lookup"><span data-stu-id="ff229-152">In the tree, expand 'TransactionsGroups'.</span></span>
33. <span data-ttu-id="ff229-153">Ve stromovém zobrazení rozbalte 'TransactionsGroups\aggregated'.</span><span class="sxs-lookup"><span data-stu-id="ff229-153">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
34. <span data-ttu-id="ff229-154">Ve stromovém zobrazení vyberte 'TransactionsGroups\aggregated\SumOfAmountMST'.</span><span class="sxs-lookup"><span data-stu-id="ff229-154">In the tree, select 'TransactionsGroups\aggregated\SumOfAmountMST'.</span></span>
35. <span data-ttu-id="ff229-155">Ve stromovém zobrazení vyberte 'Totals\Total invoice value(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')'.</span><span class="sxs-lookup"><span data-stu-id="ff229-155">In the tree, select 'Totals\Total invoice value(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')'.</span></span>
36. <span data-ttu-id="ff229-156">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="ff229-156">Click Bind.</span></span>
    * <span data-ttu-id="ff229-157">Na základě tohoto nastavení tento zdroj dat vypočítá součet hodnot v poli 'AmountMST' pro jednotlivé skupiny transakcí.</span><span class="sxs-lookup"><span data-stu-id="ff229-157">Based on this setting, this data source will calculate the sum of values of the 'AmountMST' field for each groups of transactions.</span></span> <span data-ttu-id="ff229-158">Tento výpočet seskupení bude k dispozici jako položka TransactionsGroups.aggregated.TotalAmount.</span><span class="sxs-lookup"><span data-stu-id="ff229-158">This aggregation calculation will be available as TransactionsGroups.aggregated.TotalAmount item.</span></span>  
37. <span data-ttu-id="ff229-159">Ve stromu rozbalte 'TransactionsGroups'.</span><span class="sxs-lookup"><span data-stu-id="ff229-159">In the tree, expand 'TransactionsGroups'.</span></span>
38. <span data-ttu-id="ff229-160">Ve stromovém zobrazení vyberte 'TransactionsGroups'.</span><span class="sxs-lookup"><span data-stu-id="ff229-160">In the tree, select 'TransactionsGroups'.</span></span>
39. <span data-ttu-id="ff229-161">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="ff229-161">Click Edit.</span></span>
40. <span data-ttu-id="ff229-162">Klikněte na „Upravit skupinu podle“.</span><span class="sxs-lookup"><span data-stu-id="ff229-162">Click Edit group by.</span></span>
41. <span data-ttu-id="ff229-163">Ve stromovém zobrazení rozbalte možnost Transakce.</span><span class="sxs-lookup"><span data-stu-id="ff229-163">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="ff229-164">Ve stromovém zobrazení vyberte možnost 'Transactions\Invoice amount(AmountMST)'.</span><span class="sxs-lookup"><span data-stu-id="ff229-164">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
43. <span data-ttu-id="ff229-165">Klikněte na „Přidat pole do“.</span><span class="sxs-lookup"><span data-stu-id="ff229-165">Click Add field to.</span></span>
44. <span data-ttu-id="ff229-166">Klikněte na „Seskupená pole“.</span><span class="sxs-lookup"><span data-stu-id="ff229-166">Click Aggregation fields.</span></span>
45. <span data-ttu-id="ff229-167">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="ff229-167">In the list, mark the selected row.</span></span>
46. <span data-ttu-id="ff229-168">V poli Metoda vyberte možnost Max.</span><span class="sxs-lookup"><span data-stu-id="ff229-168">In the Method field, select 'Max'.</span></span>
47. <span data-ttu-id="ff229-169">V poli název zadejte 'MaxOfAmountMST'.</span><span class="sxs-lookup"><span data-stu-id="ff229-169">In the Name field, type 'MaxOfAmountMST'.</span></span>
48. <span data-ttu-id="ff229-170">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="ff229-170">Click Save.</span></span>
    * <span data-ttu-id="ff229-171">V současné době lze přeložit provedení zdrojů dat GROUPBY na úrovni databáze SQL s určitými omezeními.</span><span class="sxs-lookup"><span data-stu-id="ff229-171">Currently, the execution of GROUPBY data sources can be translated to the SQL database level with some limitations.</span></span> <span data-ttu-id="ff229-172">Převod lze provést buď pro zdroje dat typu Seznam záznamů, nebo pro zdroje dat vyjádřené jako výraz pomocí funkce FILTER.</span><span class="sxs-lookup"><span data-stu-id="ff229-172">Translation can be done for either data sources of the 'Record list' type or data sources represented as an expression using the FILTER function.</span></span> <span data-ttu-id="ff229-173">Lze jej provést také, pouze pokud je nakonfigurována jedna agregace pro jedno pole záznamů seskupení.</span><span class="sxs-lookup"><span data-stu-id="ff229-173">It can also be done when the only one aggregation is configured for a single field of the grouping records.</span></span>  
    * <span data-ttu-id="ff229-174">Všimněte si, že i když bylo pro pole AmountMST nakonfigurováno více seskupení, pole Provedení v stále označuje, že bude toto seskupení provedeno v době běhu v databázi SQL.</span><span class="sxs-lookup"><span data-stu-id="ff229-174">Note that even though more than one aggregation was configured for the AmountMST field, the 'Execution at' field still indicates that this grouping will be performed at run-time in the SQL database.</span></span> <span data-ttu-id="ff229-175">Důvodem je skutečnost, že pouze jedno seskupení má vazbu na položku datového modelu a bude použito při spuštění k získání dat z tohoto zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="ff229-175">This is because only one aggregation is bound to the data model item and will be used at run-time to pull data from this data source.</span></span>  
49. <span data-ttu-id="ff229-176">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ff229-176">Close the page.</span></span>
50. <span data-ttu-id="ff229-177">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ff229-177">Click OK.</span></span>
51. <span data-ttu-id="ff229-178">Ve stromu rozbalte 'TransactionsGroups'.</span><span class="sxs-lookup"><span data-stu-id="ff229-178">In the tree, expand 'TransactionsGroups'.</span></span>
52. <span data-ttu-id="ff229-179">Ve stromovém zobrazení rozbalte 'TransactionsGroups\aggregated'.</span><span class="sxs-lookup"><span data-stu-id="ff229-179">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
53. <span data-ttu-id="ff229-180">Ve stromovém zobrazení vyberte 'TransactionsGroups\aggregated\MaxOfAmountMST'.</span><span class="sxs-lookup"><span data-stu-id="ff229-180">In the tree, select 'TransactionsGroups\aggregated\MaxOfAmountMST'.</span></span>
54. <span data-ttu-id="ff229-181">Ve stromovém zobrazení vyberte 'Totals\Total statistical value(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')'.</span><span class="sxs-lookup"><span data-stu-id="ff229-181">In the tree, select 'Totals\Total statistical value(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')'.</span></span>
55. <span data-ttu-id="ff229-182">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="ff229-182">Click Bind.</span></span>
56. <span data-ttu-id="ff229-183">Ve stromu rozbalte 'TransactionsGroups'.</span><span class="sxs-lookup"><span data-stu-id="ff229-183">In the tree, expand 'TransactionsGroups'.</span></span>
57. <span data-ttu-id="ff229-184">Ve stromovém zobrazení vyberte 'TransactionsGroups'.</span><span class="sxs-lookup"><span data-stu-id="ff229-184">In the tree, select 'TransactionsGroups'.</span></span>
58. <span data-ttu-id="ff229-185">Klikněte na možnost Upravit.</span><span class="sxs-lookup"><span data-stu-id="ff229-185">Click Edit.</span></span>
59. <span data-ttu-id="ff229-186">Klikněte na „Upravit skupinu podle“.</span><span class="sxs-lookup"><span data-stu-id="ff229-186">Click Edit group by.</span></span>
    * <span data-ttu-id="ff229-187">Poznámka: pole 'Provedení v' označuje, že toto seskupení se provede v době běhu v paměti vzhledem k tomu, že obě seskupení stejného pole jsou vázána na položky datového modelu.</span><span class="sxs-lookup"><span data-stu-id="ff229-187">Note that the 'Execution at' field indicates that this grouping will be performed at run-time in memory because both aggregations of the same field are bound to the data model items.</span></span>   
60. <span data-ttu-id="ff229-188">V seznamu označte všechny řádky nebo jejich označení zrušte.</span><span class="sxs-lookup"><span data-stu-id="ff229-188">In the list, mark or unmark all rows.</span></span>
61. <span data-ttu-id="ff229-189">Klikněte na tlačítko Odstranit.</span><span class="sxs-lookup"><span data-stu-id="ff229-189">Click Delete.</span></span>
62. <span data-ttu-id="ff229-190">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="ff229-190">Click Yes.</span></span>
63. <span data-ttu-id="ff229-191">Klikněte na tlačítko Odstranit.</span><span class="sxs-lookup"><span data-stu-id="ff229-191">Click Delete.</span></span>
64. <span data-ttu-id="ff229-192">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="ff229-192">Click Yes.</span></span>
65. <span data-ttu-id="ff229-193">Klikněte na „Přidat pole do“.</span><span class="sxs-lookup"><span data-stu-id="ff229-193">Click Add field to.</span></span>
66. <span data-ttu-id="ff229-194">Klikněte na „Skupina Co“.</span><span class="sxs-lookup"><span data-stu-id="ff229-194">Click What to group.</span></span>
67. <span data-ttu-id="ff229-195">Ve stromovém zobrazení rozbalte 'Commodity record(Intrastat)'.</span><span class="sxs-lookup"><span data-stu-id="ff229-195">In the tree, expand 'Commodity record(Intrastat)'.</span></span>
68. <span data-ttu-id="ff229-196">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="ff229-196">Click Save.</span></span>
    * <span data-ttu-id="ff229-197">Poznámka: pole 'Provedení v' označuje, že toto seskupení se provede při spuštění v paměti i v případě, že neexistují žádná seskupení definovaná ve vybraném zdroji dat a vybraný zdroj dat tabulky záznamů typu se vztahuje na stejnou tabulku 'systému Intrastat.</span><span class="sxs-lookup"><span data-stu-id="ff229-197">Note that the 'Execution at' field indicates that this grouping will be performed at run-time in memory even though there are no aggregations defined and the selected data source of 'Table records' type refers to the same 'Intrastat' table.</span></span> <span data-ttu-id="ff229-198">Důvodem je skutečnost, že zdroj dat obsahuje některá vypočítaná pole, která nelze ještě převést na úrovni databáze SQL.</span><span class="sxs-lookup"><span data-stu-id="ff229-198">This is because the data source contains some calculated fields which can't yet be translated to the SQL database level.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]