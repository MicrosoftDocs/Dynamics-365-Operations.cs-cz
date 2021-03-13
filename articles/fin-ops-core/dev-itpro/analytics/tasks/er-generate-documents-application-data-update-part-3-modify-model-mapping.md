---
title: Úprava modelů a mapování pro generování dokumentů s daty aplikace
description: Toto téma popisuje, jak navrhnout konfigurace vykazování k vygenerování elektronického dokumentu a aktualizaci dat aplikace. (Část 2 - Generování dokumentů).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 025429c8e6775d20634703853df04d63c0651b98
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092890"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="e99ab-104">Úprava modelů a mapování pro generování dokumentů s daty aplikace</span><span class="sxs-lookup"><span data-stu-id="e99ab-104">Modify models and mappings to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e99ab-105">K dokončení kroků v tomto postupu musíte nejprve dokončit postup "ER Generování dokumentů s aktualizací dat aplikace (část 2: generování dokumentů)".</span><span class="sxs-lookup"><span data-stu-id="e99ab-105">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 2: Generate documents)".</span></span> 

<span data-ttu-id="e99ab-106">Kroky v tomto postupu vysvětlují návrh konfigurace elektronického vykazování (ER) k vygenerování elektronického dokumentu a aktualizaci dat aplikace.</span><span class="sxs-lookup"><span data-stu-id="e99ab-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="e99ab-107">V tomto postupu budete upravovat konfigurace ER tak, aby se začaly používat výhradně ke generování elektronických dokumentů a k aktualizaci dat aplikace.</span><span class="sxs-lookup"><span data-stu-id="e99ab-107">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="e99ab-108">Tento postup je vytvořen pro uživatele s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování.</span><span class="sxs-lookup"><span data-stu-id="e99ab-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="e99ab-109">Tyto kroky lze dokončit za použití datové sady DEMF.</span><span class="sxs-lookup"><span data-stu-id="e99ab-109">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="e99ab-110">Upravit model dat</span><span class="sxs-lookup"><span data-stu-id="e99ab-110">Modify data model</span></span>
1. <span data-ttu-id="e99ab-111">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="e99ab-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="e99ab-112">Ve stromovém zobrazení vyberte Intrastat (modul).</span><span class="sxs-lookup"><span data-stu-id="e99ab-112">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="e99ab-113">Údaje se rozšiřují v závislosti na způsobu použití datového modelu.</span><span class="sxs-lookup"><span data-stu-id="e99ab-113">You will extend how you use the data model.</span></span> <span data-ttu-id="e99ab-114">Kromě použití jako zdroje dat pro vygenerování sestavy Intrastat se datový model použije ke shromáždění podrobností o procesu vykazování Intrastat.</span><span class="sxs-lookup"><span data-stu-id="e99ab-114">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="e99ab-115">Údaje se poté použijí k aktualizaci dat aplikace.</span><span class="sxs-lookup"><span data-stu-id="e99ab-115">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="e99ab-116">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="e99ab-116">Click Designer.</span></span>
4. <span data-ttu-id="e99ab-117">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="e99ab-117">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="e99ab-118">Do pole Nový uzel zadejte Kořen modelu.</span><span class="sxs-lookup"><span data-stu-id="e99ab-118">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="e99ab-119">Do pole Název zadejte Pro aktualizaci dat aplikace.</span><span class="sxs-lookup"><span data-stu-id="e99ab-119">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="e99ab-120">Pro aktualizaci dat aplikace</span><span class="sxs-lookup"><span data-stu-id="e99ab-120">For application data update</span></span>  
7. <span data-ttu-id="e99ab-121">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="e99ab-121">Click Add.</span></span>
8. <span data-ttu-id="e99ab-122">Ve stromovém zobrazení vyberte Pro aktualizaci dat aplikace.</span><span class="sxs-lookup"><span data-stu-id="e99ab-122">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="e99ab-123">Tato nová kořenová položka bude přidána pro určení toku dat při přesunu dat ze sestavy Intrastat (použité jako datový zdroj) do tabulek aplikace (cíl aktualizace).</span><span class="sxs-lookup"><span data-stu-id="e99ab-123">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="e99ab-124">Mějte na paměti, že pro získávání dat, která byla zanesena do odchozího dokumentu musí být použita jiná kořenová položka, než pro získávání dat z dokumentu, který se používá k aktualizaci dat aplikace.</span><span class="sxs-lookup"><span data-stu-id="e99ab-124">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="e99ab-125">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="e99ab-125">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="e99ab-126">Do pole Název zadejte Záhlaví archivu.</span><span class="sxs-lookup"><span data-stu-id="e99ab-126">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="e99ab-127">Záhlaví archivu</span><span class="sxs-lookup"><span data-stu-id="e99ab-127">Archive header</span></span>  
11. <span data-ttu-id="e99ab-128">V poli Typ položky vyberte Seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="e99ab-128">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="e99ab-129">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="e99ab-129">Click Add.</span></span>
    * <span data-ttu-id="e99ab-130">Vzhledem k tomu, že chcete vytvořit záznam pro každou vygenerovanou sestavu Intrastat, je nutné pro to vytvořit novou položku.</span><span class="sxs-lookup"><span data-stu-id="e99ab-130">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="e99ab-131">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="e99ab-131">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="e99ab-132">Do pole Název zadejte Název souboru.</span><span class="sxs-lookup"><span data-stu-id="e99ab-132">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="e99ab-133">Název souboru</span><span class="sxs-lookup"><span data-stu-id="e99ab-133">File name</span></span>  
15. <span data-ttu-id="e99ab-134">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="e99ab-134">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="e99ab-135">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="e99ab-135">Click Add.</span></span>
17. <span data-ttu-id="e99ab-136">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="e99ab-136">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="e99ab-137">Do pole Název zadejte Počet řádků.</span><span class="sxs-lookup"><span data-stu-id="e99ab-137">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="e99ab-138">Počet řádků</span><span class="sxs-lookup"><span data-stu-id="e99ab-138">Number of lines</span></span>  
19. <span data-ttu-id="e99ab-139">V poli Typ položky vyberte Celé číslo.</span><span class="sxs-lookup"><span data-stu-id="e99ab-139">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="e99ab-140">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="e99ab-140">Click Add.</span></span>
    * <span data-ttu-id="e99ab-141">Přidáním této položky můžete reprezentovat počet transakcí Intrastat, které jsou uvedeny vykázány při aktuálním procesu vykazování.</span><span class="sxs-lookup"><span data-stu-id="e99ab-141">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="e99ab-142">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="e99ab-142">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="e99ab-143">Do pole Název zadejte Řádky archivu.</span><span class="sxs-lookup"><span data-stu-id="e99ab-143">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="e99ab-144">Řádky archivu</span><span class="sxs-lookup"><span data-stu-id="e99ab-144">Archive lines</span></span>  
23. <span data-ttu-id="e99ab-145">V poli Typ položky vyberte Seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="e99ab-145">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="e99ab-146">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="e99ab-146">Click Add.</span></span>
    * <span data-ttu-id="e99ab-147">Přidáním této položky můžete reprezentovat seznam transakcí Intrastat, které jsou uvedeny vykázány při aktuálním procesu vykazování.</span><span class="sxs-lookup"><span data-stu-id="e99ab-147">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="e99ab-148">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="e99ab-148">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="e99ab-149">Do pole Název zadejte „Částka“.</span><span class="sxs-lookup"><span data-stu-id="e99ab-149">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="e99ab-150">Množství</span><span class="sxs-lookup"><span data-stu-id="e99ab-150">Amount</span></span>  
27. <span data-ttu-id="e99ab-151">V poli Typ položky vyberte Reálný.</span><span class="sxs-lookup"><span data-stu-id="e99ab-151">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="e99ab-152">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="e99ab-152">Click Add.</span></span>
29. <span data-ttu-id="e99ab-153">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="e99ab-153">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="e99ab-154">Do pole Název zadejte ID záznamu komodity.</span><span class="sxs-lookup"><span data-stu-id="e99ab-154">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="e99ab-155">ID záznamu komodity</span><span class="sxs-lookup"><span data-stu-id="e99ab-155">Commodity rec id</span></span>  
31. <span data-ttu-id="e99ab-156">V poli Typ položky vyberte Int64.</span><span class="sxs-lookup"><span data-stu-id="e99ab-156">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="e99ab-157">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="e99ab-157">Click Add.</span></span>
33. <span data-ttu-id="e99ab-158">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="e99ab-158">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="e99ab-159">Do pole Název zadejte Číslo položky.</span><span class="sxs-lookup"><span data-stu-id="e99ab-159">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="e99ab-160">Č. položky</span><span class="sxs-lookup"><span data-stu-id="e99ab-160">Item number</span></span>  
35. <span data-ttu-id="e99ab-161">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="e99ab-161">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="e99ab-162">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="e99ab-162">Click Add.</span></span>
37. <span data-ttu-id="e99ab-163">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="e99ab-163">Click Save.</span></span>
38. <span data-ttu-id="e99ab-164">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e99ab-164">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="e99ab-165">Úprava mapování modelu</span><span class="sxs-lookup"><span data-stu-id="e99ab-165">Modify model mapping</span></span>
1. <span data-ttu-id="e99ab-166">Ve stromovém zobrazení rozbalte Intrastat (model).</span><span class="sxs-lookup"><span data-stu-id="e99ab-166">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="e99ab-167">Ve stromové struktuře vyberte Intrastat (model)\Intrastat (mapping).</span><span class="sxs-lookup"><span data-stu-id="e99ab-167">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="e99ab-168">Upravte stávající mapování modelu a začněte je používat pro aktualizaci dat aplikace a k archivaci podrobností vykazování Intrastat.</span><span class="sxs-lookup"><span data-stu-id="e99ab-168">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="e99ab-169">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="e99ab-169">Click Designer.</span></span>
4. <span data-ttu-id="e99ab-170">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e99ab-170">Click New.</span></span>
5. <span data-ttu-id="e99ab-171">Do pole Název zadejte Aktualizovat archiv.</span><span class="sxs-lookup"><span data-stu-id="e99ab-171">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="e99ab-172">Aktualizace archivu</span><span class="sxs-lookup"><span data-stu-id="e99ab-172">Update archive</span></span>  
6. <span data-ttu-id="e99ab-173">V poli Směr vyberte hodnotu Do cíle.</span><span class="sxs-lookup"><span data-stu-id="e99ab-173">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="e99ab-174">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="e99ab-174">Click Save.</span></span>
    * <span data-ttu-id="e99ab-175">Toto nové mapování určuje tok dat při přesunu dat (podrobnosti sestavy Intrastat) z datového modelu do tabulek aplikace (cíl aktualizace).</span><span class="sxs-lookup"><span data-stu-id="e99ab-175">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="e99ab-176">Mějte na paměti, že pro získávání dat z aplikace pro proces vykazování musí být použita jiná kořenová položka modelu, než pro použití dat z modelu dat pro aktualizaci dat aplikace.</span><span class="sxs-lookup"><span data-stu-id="e99ab-176">Note that different model's root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="e99ab-177">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="e99ab-177">Click Designer.</span></span>
9. <span data-ttu-id="e99ab-178">Ve stromovém zobrazení vyberte Data model\Data model.</span><span class="sxs-lookup"><span data-stu-id="e99ab-178">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="e99ab-179">Přidejte požadovaný zdroj dat.</span><span class="sxs-lookup"><span data-stu-id="e99ab-179">Add the required data source.</span></span> <span data-ttu-id="e99ab-180">Jedná se o datový model, který obsahuje podrobnosti o nahlášených transakcích systému Intrastat, které musí být archivovány.</span><span class="sxs-lookup"><span data-stu-id="e99ab-180">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="e99ab-181">Klikněte na možnost Přidat kořen.</span><span class="sxs-lookup"><span data-stu-id="e99ab-181">Click Add root.</span></span>
11. <span data-ttu-id="e99ab-182">Do pole Název zadejte Model.</span><span class="sxs-lookup"><span data-stu-id="e99ab-182">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="e99ab-183">model</span><span class="sxs-lookup"><span data-stu-id="e99ab-183">model</span></span>  
12. <span data-ttu-id="e99ab-184">V poli Definice zadejte nebo vyberte hodnotu 'Pro aktualizaci dat aplikace'.</span><span class="sxs-lookup"><span data-stu-id="e99ab-184">In the Definition field, enter or select the value 'For application data update'.</span></span>
    * <span data-ttu-id="e99ab-185">Pro aktualizaci dat aplikace</span><span class="sxs-lookup"><span data-stu-id="e99ab-185">For application data update</span></span>  
13. <span data-ttu-id="e99ab-186">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="e99ab-186">Click OK.</span></span>
14. <span data-ttu-id="e99ab-187">Ve stromovém zobrazení rozbalte „model“.</span><span class="sxs-lookup"><span data-stu-id="e99ab-187">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="e99ab-188">Ve stromovém zobrazení vyberte možnost „Funkce\Počítané pole“.</span><span class="sxs-lookup"><span data-stu-id="e99ab-188">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="e99ab-189">Ve stromovém zobrazení vyberte model\Archive header.</span><span class="sxs-lookup"><span data-stu-id="e99ab-189">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="e99ab-190">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="e99ab-190">Click Add.</span></span>
    * <span data-ttu-id="e99ab-191">Vzhledem k tomu, že chcete vytvořit výčet nahlášené transakce Intrastat pro archivaci, je nutné přidat odpovídacími zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="e99ab-191">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="e99ab-192">Do pole Název zadejte Výčet řádků.</span><span class="sxs-lookup"><span data-stu-id="e99ab-192">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="e99ab-193">Řádky z výčtu</span><span class="sxs-lookup"><span data-stu-id="e99ab-193">Enumerated lines</span></span>  
19. <span data-ttu-id="e99ab-194">Klikněte na možnost Upravit vzorec.</span><span class="sxs-lookup"><span data-stu-id="e99ab-194">Click Edit formula.</span></span>
20. <span data-ttu-id="e99ab-195">Ve stromovém zobrazení vyberte List\ENUMERATE.</span><span class="sxs-lookup"><span data-stu-id="e99ab-195">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="e99ab-196">Klikněte na možnost Přidat funkci.</span><span class="sxs-lookup"><span data-stu-id="e99ab-196">Click Add function.</span></span>
22. <span data-ttu-id="e99ab-197">Ve stromovém zobrazení rozbalte „model“.</span><span class="sxs-lookup"><span data-stu-id="e99ab-197">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="e99ab-198">Ve stromovém zobrazení rozbalte možnost model\Archive header.</span><span class="sxs-lookup"><span data-stu-id="e99ab-198">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="e99ab-199">Ve stromovém zobrazení vyberte model\Archive header\Archive lines.</span><span class="sxs-lookup"><span data-stu-id="e99ab-199">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="e99ab-200">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="e99ab-200">Click Add data source.</span></span>
26. <span data-ttu-id="e99ab-201">V poli Receptura zadejte ENUMERATE(model.'Archive header'.'Archive lines').</span><span class="sxs-lookup"><span data-stu-id="e99ab-201">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="e99ab-202">ENUMERATE(model.'Archive header'.'Archive lines')</span><span class="sxs-lookup"><span data-stu-id="e99ab-202">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="e99ab-203">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="e99ab-203">Click Save.</span></span>
28. <span data-ttu-id="e99ab-204">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e99ab-204">Close the page.</span></span>
29. <span data-ttu-id="e99ab-205">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="e99ab-205">Click OK.</span></span>
30. <span data-ttu-id="e99ab-206">Klikněte na možnost Přidat cíl.</span><span class="sxs-lookup"><span data-stu-id="e99ab-206">Click Add destination.</span></span>
    * <span data-ttu-id="e99ab-207">Přidejte tabulky aplikace jako požadované cíle, které vyžadují aktualizace podrobností archivace nahlášených transakcí Intrastat.</span><span class="sxs-lookup"><span data-stu-id="e99ab-207">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="e99ab-208">Do pole Název zadejte Archiv.</span><span class="sxs-lookup"><span data-stu-id="e99ab-208">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="e99ab-209">Archivovat</span><span class="sxs-lookup"><span data-stu-id="e99ab-209">Archive</span></span>  
32. <span data-ttu-id="e99ab-210">Do pole Tabulka zadejte IntrastatArchiveGeneral.</span><span class="sxs-lookup"><span data-stu-id="e99ab-210">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="e99ab-211">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="e99ab-211">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="e99ab-212">Ponechte akci záznamu 'Vložit', aby bylo možné přidat záznamy během archivace podrobností pro každý proces vykazování Intrastat.</span><span class="sxs-lookup"><span data-stu-id="e99ab-212">Keep the record action 'Insert' so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="e99ab-213">Vyberte možnost Ano v poli Informační protokol o záznamu.</span><span class="sxs-lookup"><span data-stu-id="e99ab-213">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="e99ab-214">Výběrem možnosti Ano získáte informace o problémech s aktualizací dat aplikace.</span><span class="sxs-lookup"><span data-stu-id="e99ab-214">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="e99ab-215">Vyberte možnost Ano v poli Ověření akce přeskočení záznamu.</span><span class="sxs-lookup"><span data-stu-id="e99ab-215">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="e99ab-216">Výběrem možnosti Ano potlačíte chyby v ověření prázdného pole 'ID archivu Intrastat'.</span><span class="sxs-lookup"><span data-stu-id="e99ab-216">Select Yes to suppress validation errors about the empty 'Intrastat archive ID' field.</span></span> <span data-ttu-id="e99ab-217">Tato akce proběhne po přidání záznamů na základě nastavení pořadového čísla pro tuto tabulku ve formuláři Parametry zahraničního obchodu.</span><span class="sxs-lookup"><span data-stu-id="e99ab-217">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="e99ab-218">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="e99ab-218">Click OK.</span></span>
    * <span data-ttu-id="e99ab-219">Vytvořte vazbu přidaného zdroje dat (filtrovaný model založený na vybrané kořenové položce) s prvky z přidaného cíle.</span><span class="sxs-lookup"><span data-stu-id="e99ab-219">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="e99ab-220">Ve stromovém zobrazení rozbalte Archiv.</span><span class="sxs-lookup"><span data-stu-id="e99ab-220">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="e99ab-221">Ve stromovém zobrazení rozbalte Archive\<Relations.</span><span class="sxs-lookup"><span data-stu-id="e99ab-221">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="e99ab-222">Ve stromovém zobrazení rozbalte Archive\<Relations\IntrastatArchiveDetail.</span><span class="sxs-lookup"><span data-stu-id="e99ab-222">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="e99ab-223">Ve stromovém zobrazení vyberte Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST).</span><span class="sxs-lookup"><span data-stu-id="e99ab-223">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="e99ab-224">Ve stromovém zobrazení rozbalte model\Archive header\Enumerated lines.</span><span class="sxs-lookup"><span data-stu-id="e99ab-224">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="e99ab-225">Ve stromovém zobrazení rozbalte model\Archive header\Enumerated lines\Value.</span><span class="sxs-lookup"><span data-stu-id="e99ab-225">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="e99ab-226">Ve stromovém zobrazení vyberte model\Archive header\Enumerated lines\Value\Amount.</span><span class="sxs-lookup"><span data-stu-id="e99ab-226">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="e99ab-227">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="e99ab-227">Click Bind.</span></span>
44. <span data-ttu-id="e99ab-228">Ve stromovém zobrazení vyberte Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity).</span><span class="sxs-lookup"><span data-stu-id="e99ab-228">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="e99ab-229">Ve stromovém zobrazení vyberte model\Archive header\Enumerated lines\Value\Commodity rec id.</span><span class="sxs-lookup"><span data-stu-id="e99ab-229">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="e99ab-230">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="e99ab-230">Click Bind.</span></span>
47. <span data-ttu-id="e99ab-231">Ve stromovém zobrazení vyberte Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId).</span><span class="sxs-lookup"><span data-stu-id="e99ab-231">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="e99ab-232">Ve stromovém zobrazení vyberte model\Archive header\Enumerated lines\Value\Item number.</span><span class="sxs-lookup"><span data-stu-id="e99ab-232">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="e99ab-233">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="e99ab-233">Click Bind.</span></span>
50. <span data-ttu-id="e99ab-234">Ve stromovém zobrazení vyberte Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber).</span><span class="sxs-lookup"><span data-stu-id="e99ab-234">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="e99ab-235">Ve stromovém zobrazení vyberte model\Archive header\Enumerated lines\Number.</span><span class="sxs-lookup"><span data-stu-id="e99ab-235">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="e99ab-236">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="e99ab-236">Click Bind.</span></span>
53. <span data-ttu-id="e99ab-237">Ve stromovém zobrazení vyberte Archive\<Relations\IntrastatArchiveDetail.</span><span class="sxs-lookup"><span data-stu-id="e99ab-237">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="e99ab-238">Ve stromovém zobrazení vyberte model\Archive header\Enumerated line.</span><span class="sxs-lookup"><span data-stu-id="e99ab-238">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="e99ab-239">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="e99ab-239">Click Bind.</span></span>
56. <span data-ttu-id="e99ab-240">Ve stromovém zobrazení vyberte Archive\File name(FileName).</span><span class="sxs-lookup"><span data-stu-id="e99ab-240">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="e99ab-241">Ve stromovém zobrazení vyberte model\Archive header\File name.</span><span class="sxs-lookup"><span data-stu-id="e99ab-241">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="e99ab-242">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="e99ab-242">Click Bind.</span></span>
59. <span data-ttu-id="e99ab-243">Ve stromovém zobrazení vyberte Archive\Number of lines(NumberOfLines).</span><span class="sxs-lookup"><span data-stu-id="e99ab-243">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="e99ab-244">Ve stromovém zobrazení vyberte model\Archive header\Number of lines.</span><span class="sxs-lookup"><span data-stu-id="e99ab-244">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="e99ab-245">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="e99ab-245">Click Bind.</span></span>
62. <span data-ttu-id="e99ab-246">Ve stromu vyberte Archiv.</span><span class="sxs-lookup"><span data-stu-id="e99ab-246">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="e99ab-247">Ve stromovém zobrazení vyberte model\Archive header.</span><span class="sxs-lookup"><span data-stu-id="e99ab-247">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="e99ab-248">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="e99ab-248">Click Bind.</span></span>
65. <span data-ttu-id="e99ab-249">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="e99ab-249">Click Save.</span></span>
66. <span data-ttu-id="e99ab-250">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e99ab-250">Close the page.</span></span>
67. <span data-ttu-id="e99ab-251">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e99ab-251">Close the page.</span></span>

