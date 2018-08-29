--- 
title: "Úprava modelů a mapování pro generování dokumentů s daty aplikace"
description: "K dokončení kroků v tomto postupu musíte nejprve dokončit postup ER Generování dokumentů s aktualizací dat aplikace (část 2 - generování dokumentů)."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 580f00faf6694dc2da476ffa75f995d9a24e0f8b
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="2ea7f-103">Úprava modelů a mapování pro generování dokumentů s daty aplikace</span><span class="sxs-lookup"><span data-stu-id="2ea7f-103">Modify models and mappings to generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2ea7f-104">K dokončení kroků v tomto postupu musíte nejprve dokončit postup ER Generování dokumentů s aktualizací dat aplikace (část 2: generování dokumentů).</span><span class="sxs-lookup"><span data-stu-id="2ea7f-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 2: Generate documents)”.</span></span> 

<span data-ttu-id="2ea7f-105">Kroky v tomto postupu vysvětlují návrh konfigurace elektronického vykazování (ER) k vygenerování elektronického dokumentu a aktualizaci dat aplikace.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="2ea7f-106">V tomto postupu budete upravovat konfigurace ER tak, aby se začaly používat výhradně ke generování elektronických dokumentů a k aktualizaci dat aplikace.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-106">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="2ea7f-107">Tento postup je vytvořen pro uživatele s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="2ea7f-108">Tyto kroky lze dokončit za použití datové sady DEMF.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-108">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="2ea7f-109">Upravit model dat</span><span class="sxs-lookup"><span data-stu-id="2ea7f-109">Modify data model</span></span>
1. <span data-ttu-id="2ea7f-110">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="2ea7f-111">Ve stromovém zobrazení vyberte Intrastat (modul).</span><span class="sxs-lookup"><span data-stu-id="2ea7f-111">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="2ea7f-112">Údaje se rozšiřují v závislosti na způsobu použití datového modelu.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-112">You will extend how you use the data model.</span></span> <span data-ttu-id="2ea7f-113">Kromě použití jako zdroje dat pro vygenerování sestavy Intrastat se datový model použije ke shromáždění podrobností o procesu vykazování Intrastat.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-113">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="2ea7f-114">Údaje se poté použijí k aktualizaci dat aplikace.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-114">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="2ea7f-115">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-115">Click Designer.</span></span>
4. <span data-ttu-id="2ea7f-116">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-116">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="2ea7f-117">Do pole Nový uzel zadejte Kořen modelu.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-117">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="2ea7f-118">Do pole Název zadejte Pro aktualizaci dat aplikace.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-118">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="2ea7f-119">Pro aktualizaci dat aplikace</span><span class="sxs-lookup"><span data-stu-id="2ea7f-119">For application data update</span></span>  
7. <span data-ttu-id="2ea7f-120">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-120">Click Add.</span></span>
8. <span data-ttu-id="2ea7f-121">Ve stromovém zobrazení vyberte Pro aktualizaci dat aplikace.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-121">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="2ea7f-122">Tato nová kořenová položka bude přidána pro určení toku dat při přesunu dat ze sestavy Intrastat (použité jako datový zdroj) do tabulek aplikace (cíl aktualizace).</span><span class="sxs-lookup"><span data-stu-id="2ea7f-122">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="2ea7f-123">Mějte na paměti, že pro získávání dat, která byla zanesena do odchozího dokumentu musí být použita jiná kořenová položka, než pro získávání dat z dokumentu, který se používá k aktualizaci dat aplikace.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-123">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="2ea7f-124">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="2ea7f-125">Do pole Název zadejte Záhlaví archivu.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-125">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="2ea7f-126">Záhlaví archivu</span><span class="sxs-lookup"><span data-stu-id="2ea7f-126">Archive header</span></span>  
11. <span data-ttu-id="2ea7f-127">V poli Typ položky vyberte Seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-127">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="2ea7f-128">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-128">Click Add.</span></span>
    * <span data-ttu-id="2ea7f-129">Vzhledem k tomu, že chcete vytvořit záznam pro každou vygenerovanou sestavu Intrastat, je nutné pro to vytvořit novou položku.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-129">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="2ea7f-130">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-130">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="2ea7f-131">Do pole Název zadejte Název souboru.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-131">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="2ea7f-132">Název souboru</span><span class="sxs-lookup"><span data-stu-id="2ea7f-132">File name</span></span>  
15. <span data-ttu-id="2ea7f-133">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-133">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="2ea7f-134">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-134">Click Add.</span></span>
17. <span data-ttu-id="2ea7f-135">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-135">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="2ea7f-136">Do pole Název zadejte Počet řádků.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-136">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="2ea7f-137">Počet řádků</span><span class="sxs-lookup"><span data-stu-id="2ea7f-137">Number of lines</span></span>  
19. <span data-ttu-id="2ea7f-138">V poli Typ položky vyberte Celé číslo.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-138">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="2ea7f-139">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-139">Click Add.</span></span>
    * <span data-ttu-id="2ea7f-140">Přidáním této položky můžete reprezentovat počet transakcí Intrastat, které jsou uvedeny vykázány při aktuálním procesu vykazování.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-140">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="2ea7f-141">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-141">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="2ea7f-142">Do pole Název zadejte Řádky archivu.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-142">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="2ea7f-143">Řádky archivu</span><span class="sxs-lookup"><span data-stu-id="2ea7f-143">Archive lines</span></span>  
23. <span data-ttu-id="2ea7f-144">V poli Typ položky vyberte Seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-144">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="2ea7f-145">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-145">Click Add.</span></span>
    * <span data-ttu-id="2ea7f-146">Přidáním této položky můžete reprezentovat seznam transakcí Intrastat, které jsou uvedeny vykázány při aktuálním procesu vykazování.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-146">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="2ea7f-147">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-147">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="2ea7f-148">Do pole Název zadejte „Částka“.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-148">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="2ea7f-149">Množství</span><span class="sxs-lookup"><span data-stu-id="2ea7f-149">Amount</span></span>  
27. <span data-ttu-id="2ea7f-150">V poli Typ položky vyberte Reálný.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-150">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="2ea7f-151">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-151">Click Add.</span></span>
29. <span data-ttu-id="2ea7f-152">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-152">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="2ea7f-153">Do pole Název zadejte ID záznamu komodity.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-153">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="2ea7f-154">ID záznamu komodity</span><span class="sxs-lookup"><span data-stu-id="2ea7f-154">Commodity rec id</span></span>  
31. <span data-ttu-id="2ea7f-155">V poli Typ položky vyberte Int64.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-155">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="2ea7f-156">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-156">Click Add.</span></span>
33. <span data-ttu-id="2ea7f-157">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-157">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="2ea7f-158">Do pole Název zadejte Číslo položky.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-158">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="2ea7f-159">Č. položky</span><span class="sxs-lookup"><span data-stu-id="2ea7f-159">Item number</span></span>  
35. <span data-ttu-id="2ea7f-160">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-160">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="2ea7f-161">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-161">Click Add.</span></span>
37. <span data-ttu-id="2ea7f-162">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-162">Click Save.</span></span>
38. <span data-ttu-id="2ea7f-163">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-163">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="2ea7f-164">Úprava mapování modelu</span><span class="sxs-lookup"><span data-stu-id="2ea7f-164">Modify model mapping</span></span>
1. <span data-ttu-id="2ea7f-165">Ve stromovém zobrazení rozbalte Intrastat (model).</span><span class="sxs-lookup"><span data-stu-id="2ea7f-165">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="2ea7f-166">Ve stromové struktuře vyberte Intrastat (model)\Intrastat (mapping).</span><span class="sxs-lookup"><span data-stu-id="2ea7f-166">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="2ea7f-167">Upravte stávající mapování modelu a začněte je používat pro aktualizaci dat aplikace a k archivaci podrobností vykazování Intrastat.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-167">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="2ea7f-168">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-168">Click Designer.</span></span>
4. <span data-ttu-id="2ea7f-169">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-169">Click New.</span></span>
5. <span data-ttu-id="2ea7f-170">Do pole Název zadejte Aktualizovat archiv.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-170">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="2ea7f-171">Aktualizace archivu</span><span class="sxs-lookup"><span data-stu-id="2ea7f-171">Update archive</span></span>  
6. <span data-ttu-id="2ea7f-172">V poli Směr vyberte hodnotu Do cíle.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-172">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="2ea7f-173">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-173">Click Save.</span></span>
    * <span data-ttu-id="2ea7f-174">Toto nové mapování určuje tok dat při přesunu dat (podrobnosti sestavy Intrastat) z datového modelu do tabulek aplikace (cíl aktualizace).</span><span class="sxs-lookup"><span data-stu-id="2ea7f-174">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="2ea7f-175">Mějte na paměti, že pro získávání dat z aplikace pro proces vykazování musí být použita jiná kořenová položka modelu, než pro použití dat z modelu dat pro aktualizaci dat aplikace.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-175">Note that different model’s root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="2ea7f-176">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-176">Click Designer.</span></span>
9. <span data-ttu-id="2ea7f-177">Ve stromovém zobrazení vyberte Data model\Data model.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-177">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="2ea7f-178">Přidejte požadovaný zdroj dat.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-178">Add the required data source.</span></span> <span data-ttu-id="2ea7f-179">Jedná se o datový model, který obsahuje podrobnosti o nahlášených transakcích systému Intrastat, které musí být archivovány.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-179">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="2ea7f-180">Klikněte na možnost Přidat kořen.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-180">Click Add root.</span></span>
11. <span data-ttu-id="2ea7f-181">Do pole Název zadejte Model.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-181">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="2ea7f-182">model</span><span class="sxs-lookup"><span data-stu-id="2ea7f-182">model</span></span>  
12. <span data-ttu-id="2ea7f-183">V poli Definice zadejte nebo vyberte hodnotu Pro aktualizaci dat aplikace.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-183">In the Definition field, enter or select the value ‘For application data update’.</span></span>
    * <span data-ttu-id="2ea7f-184">Pro aktualizaci dat aplikace</span><span class="sxs-lookup"><span data-stu-id="2ea7f-184">For application data update</span></span>  
13. <span data-ttu-id="2ea7f-185">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-185">Click OK.</span></span>
14. <span data-ttu-id="2ea7f-186">Ve stromovém zobrazení rozbalte „model“.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-186">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="2ea7f-187">Ve stromovém zobrazení vyberte možnost „Funkce\Počítané pole“.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-187">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="2ea7f-188">Ve stromovém zobrazení vyberte model\Archive header.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-188">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="2ea7f-189">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-189">Click Add.</span></span>
    * <span data-ttu-id="2ea7f-190">Vzhledem k tomu, že chcete vytvořit výčet nahlášené transakce Intrastat pro archivaci, je nutné přidat odpovídacími zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-190">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="2ea7f-191">Do pole Název zadejte Výčet řádků.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-191">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="2ea7f-192">Řádky z výčtu</span><span class="sxs-lookup"><span data-stu-id="2ea7f-192">Enumerated lines</span></span>  
19. <span data-ttu-id="2ea7f-193">Klikněte na možnost Upravit vzorec.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-193">Click Edit formula.</span></span>
20. <span data-ttu-id="2ea7f-194">Ve stromovém zobrazení vyberte List\ENUMERATE.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-194">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="2ea7f-195">Klikněte na možnost Přidat funkci.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-195">Click Add function.</span></span>
22. <span data-ttu-id="2ea7f-196">Ve stromovém zobrazení rozbalte „model“.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-196">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="2ea7f-197">Ve stromovém zobrazení rozbalte možnost model\Archive header.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-197">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="2ea7f-198">Ve stromovém zobrazení vyberte model\Archive header\Archive lines.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-198">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="2ea7f-199">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-199">Click Add data source.</span></span>
26. <span data-ttu-id="2ea7f-200">V poli Receptura zadejte ENUMERATE(model.'Archive header'.'Archive lines').</span><span class="sxs-lookup"><span data-stu-id="2ea7f-200">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="2ea7f-201">ENUMERATE(model.'Archive header'.'Archive lines')</span><span class="sxs-lookup"><span data-stu-id="2ea7f-201">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="2ea7f-202">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-202">Click Save.</span></span>
28. <span data-ttu-id="2ea7f-203">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-203">Close the page.</span></span>
29. <span data-ttu-id="2ea7f-204">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-204">Click OK.</span></span>
30. <span data-ttu-id="2ea7f-205">Klikněte na možnost Přidat cíl.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-205">Click Add destination.</span></span>
    * <span data-ttu-id="2ea7f-206">Přidejte tabulky aplikace jako požadované cíle, které vyžadují aktualizace podrobností archivace nahlášených transakcí Intrastat.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-206">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="2ea7f-207">Do pole Název zadejte Archiv.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-207">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="2ea7f-208">Archivovat</span><span class="sxs-lookup"><span data-stu-id="2ea7f-208">Archive</span></span>  
32. <span data-ttu-id="2ea7f-209">Do pole Tabulka zadejte IntrastatArchiveGeneral.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-209">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="2ea7f-210">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="2ea7f-210">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="2ea7f-211">Ponechte akci záznamu Vložit, aby bylo možné přidat záznamy během archivace podrobností pro každý proces vykazování Intrastat.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-211">Keep the record action ‘Insert’ so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="2ea7f-212">Vyberte možnost Ano v poli Informační protokol o záznamu.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-212">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="2ea7f-213">Výběrem možnosti Ano získáte informace o problémech s aktualizací dat aplikace.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-213">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="2ea7f-214">Vyberte možnost Ano v poli Ověření akce přeskočení záznamu.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-214">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="2ea7f-215">Výběrem možnosti Ano potlačíte chyby v ověření prázdného pole ID archivu Intrastat.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-215">Select Yes to suppress validation errors about the empty ‘Intrastat archive ID’ field.</span></span> <span data-ttu-id="2ea7f-216">Tato akce proběhne po přidání záznamů na základě nastavení pořadového čísla pro tuto tabulku ve formuláři Parametry zahraničního obchodu.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-216">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="2ea7f-217">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-217">Click OK.</span></span>
    * <span data-ttu-id="2ea7f-218">Vytvořte vazbu přidaného zdroje dat (filtrovaný model založený na vybrané kořenové položce) s prvky z přidaného cíle.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-218">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="2ea7f-219">Ve stromovém zobrazení rozbalte Archiv.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-219">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="2ea7f-220">Ve stromovém zobrazení rozbalte Archive\<Relations.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-220">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="2ea7f-221">Ve stromovém zobrazení rozbalte Archive\<Relations\IntrastatArchiveDetail.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-221">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="2ea7f-222">Ve stromovém zobrazení vyberte Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST).</span><span class="sxs-lookup"><span data-stu-id="2ea7f-222">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="2ea7f-223">Ve stromovém zobrazení rozbalte model\Archive header\Enumerated lines.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-223">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="2ea7f-224">Ve stromovém zobrazení rozbalte model\Archive header\Enumerated lines\Value.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-224">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="2ea7f-225">Ve stromovém zobrazení vyberte model\Archive header\Enumerated lines\Value\Amount.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-225">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="2ea7f-226">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-226">Click Bind.</span></span>
44. <span data-ttu-id="2ea7f-227">Ve stromovém zobrazení vyberte Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity).</span><span class="sxs-lookup"><span data-stu-id="2ea7f-227">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="2ea7f-228">Ve stromovém zobrazení vyberte model\Archive header\Enumerated lines\Value\Commodity rec id.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-228">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="2ea7f-229">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-229">Click Bind.</span></span>
47. <span data-ttu-id="2ea7f-230">Ve stromovém zobrazení vyberte Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId).</span><span class="sxs-lookup"><span data-stu-id="2ea7f-230">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="2ea7f-231">Ve stromovém zobrazení vyberte model\Archive header\Enumerated lines\Value\Item number.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-231">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="2ea7f-232">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-232">Click Bind.</span></span>
50. <span data-ttu-id="2ea7f-233">Ve stromovém zobrazení vyberte Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber).</span><span class="sxs-lookup"><span data-stu-id="2ea7f-233">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="2ea7f-234">Ve stromovém zobrazení vyberte model\Archive header\Enumerated lines\Number.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-234">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="2ea7f-235">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-235">Click Bind.</span></span>
53. <span data-ttu-id="2ea7f-236">Ve stromovém zobrazení vyberte Archive\<Relations\IntrastatArchiveDetail.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-236">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="2ea7f-237">Ve stromovém zobrazení vyberte model\Archive header\Enumerated line.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-237">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="2ea7f-238">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-238">Click Bind.</span></span>
56. <span data-ttu-id="2ea7f-239">Ve stromovém zobrazení vyberte Archive\File name(FileName).</span><span class="sxs-lookup"><span data-stu-id="2ea7f-239">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="2ea7f-240">Ve stromovém zobrazení vyberte model\Archive header\File name.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-240">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="2ea7f-241">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-241">Click Bind.</span></span>
59. <span data-ttu-id="2ea7f-242">Ve stromovém zobrazení vyberte Archive\Number of lines(NumberOfLines).</span><span class="sxs-lookup"><span data-stu-id="2ea7f-242">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="2ea7f-243">Ve stromovém zobrazení vyberte model\Archive header\Number of lines.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-243">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="2ea7f-244">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-244">Click Bind.</span></span>
62. <span data-ttu-id="2ea7f-245">Ve stromu vyberte Archiv.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-245">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="2ea7f-246">Ve stromovém zobrazení vyberte model\Archive header.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-246">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="2ea7f-247">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-247">Click Bind.</span></span>
65. <span data-ttu-id="2ea7f-248">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-248">Click Save.</span></span>
66. <span data-ttu-id="2ea7f-249">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-249">Close the page.</span></span>
67. <span data-ttu-id="2ea7f-250">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2ea7f-250">Close the page.</span></span>


