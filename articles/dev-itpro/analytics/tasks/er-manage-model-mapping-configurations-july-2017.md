---
title: Správa mapování modelu elektronického výkaznictví v samostatných konfiguracích elektronického výkaznictví
description: Následující procedura vysvětluje, jak uživatel přiřazený k roli Správce systému nebo Návrhář elektronického výkaznictví může spravovat mapování modelu pro elektronické výkaznictví (ER) v samostatné konfiguraci ER.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 24ca4124d190df94e7ca9ac31c2ea757fe9ff242
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "349140"
---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a><span data-ttu-id="6c0a0-103">Správa mapování modelu elektronického výkaznictví v samostatných konfiguracích elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="6c0a0-103">Manage ER model mapping in separate ER configurations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6c0a0-104">Následující procedura vysvětluje, jak uživatel přiřazený k roli Správce systému nebo Návrhář elektronického výkaznictví může spravovat mapování modelu pro elektronické výkaznictví (ER) v samostatné konfiguraci ER.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-104">The following steps explain how a user assigned to the System administrator or Electronic reporting developer role can manage Electronic reporting (ER) model mappings in separate ER configurations.</span></span> <span data-ttu-id="6c0a0-105">V tomto průvodci záznamem úloh vytvoříte požadované ER konfigurace pro vzorovou společnost Litware, Inc. K provedení kroků v tomto průvodci záznamem úloh musíte nejprve dokončit postup z průvodce záznamem úloh ER Vytvoření poskytovatele konfigurace a jeho označení jako aktivního.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-105">In this task guide, you will create required ER configurations for the sample company, Litware, Inc. To complete this task guide, you must first complete the steps in the task guide, “ER Create a configuration provider” and mark it as active.</span></span> 

<span data-ttu-id="6c0a0-106">Vzhledem k tomu, že konfigurace ER se sdílí mezi společnostmi, můžete dokončit tohoto průvodce záznamem úloh za použití sady firemních dat podle vašeho výběru.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-106">Because ER configurations are shared among companies, you can complete this task guide using the company data set of your choice.</span></span> <span data-ttu-id="6c0a0-107">Funkce pro tohoto průvodce záznamem úloh naleznete po instalaci některé z následujících oprav hotfix: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 pro verzi Dynamics AX 7.0 nebo https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 pro verzi Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-107">The functionality for this task guide is available if you have installed one of the following hotfixes: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for the Dynamics AX 7.0 version or https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for the Dynamics 365 for Operations version.</span></span>

1. <span data-ttu-id="6c0a0-108">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="6c0a0-109">Ověřte, zda poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-109">Verify that the configuration provider for the sample company Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="6c0a0-110">Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v průvodci záznamem úloh Vytvoření poskytovatele konfigurace a jeho označení jako aktivního.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-110">If you don’t see this configuration provider, you must first complete the steps in the task guide, Create a configuration provider and mark it as active.</span></span>   

## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="6c0a0-111">Přidání nové konfigurace ER modelu</span><span class="sxs-lookup"><span data-stu-id="6c0a0-111">Add a new ER model configuration</span></span>
1. <span data-ttu-id="6c0a0-112">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-112">Click Reporting configurations.</span></span>
    * <span data-ttu-id="6c0a0-113">Přidejte novou konfiguraci modelu.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-113">Add a new model configuration.</span></span> <span data-ttu-id="6c0a0-114">Název musí být jedinečný ve stromu konfigurace.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-114">The name must be unique in the configurations tree.</span></span>  
2. <span data-ttu-id="6c0a0-115">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-115">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="6c0a0-116">V poli Název zadejte Vzorový datový model.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-116">In the Name field, type 'Sample data model'.</span></span>
    * <span data-ttu-id="6c0a0-117">Vzorový datový model</span><span class="sxs-lookup"><span data-stu-id="6c0a0-117">Sample data model</span></span>  
4. <span data-ttu-id="6c0a0-118">Klepněte na možnost Vytvořit konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-118">Click Create configuration.</span></span>
5. <span data-ttu-id="6c0a0-119">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-119">Click Designer.</span></span>
6. <span data-ttu-id="6c0a0-120">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-120">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="6c0a0-121">Do pole Název zadejte Kořen.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-121">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="6c0a0-122">Kořen</span><span class="sxs-lookup"><span data-stu-id="6c0a0-122">Root</span></span>  
8. <span data-ttu-id="6c0a0-123">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-123">Click Add.</span></span>
9. <span data-ttu-id="6c0a0-124">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="6c0a0-125">Do pole Název zadejte text „Společnost“.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-125">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="6c0a0-126">Společnost</span><span class="sxs-lookup"><span data-stu-id="6c0a0-126">Company</span></span>  
11. <span data-ttu-id="6c0a0-127">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-127">Click Add.</span></span>
12. <span data-ttu-id="6c0a0-128">V poli Popis zadejte text popisu právnické osoby nebo společnosti, ve které je uživatel přihlášen při spuštění.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-128">In the Description field, enter the text, Description of the legal entity or company in which a user logged at run-time.</span></span> 
    * <span data-ttu-id="6c0a0-129">Popis právnické osoby nebo společnosti, ve které se uživatel po spuštění přihlásil.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-129">Description of the legal entity or company in which a user logged at run-time.</span></span>  
13. <span data-ttu-id="6c0a0-130">Klikněte na Kořenový odkaz.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-130">Click Root reference.</span></span>
14. <span data-ttu-id="6c0a0-131">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-131">Click OK.</span></span>
15. <span data-ttu-id="6c0a0-132">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-132">Click Save.</span></span>
16. <span data-ttu-id="6c0a0-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-133">Close the page.</span></span>
17. <span data-ttu-id="6c0a0-134">Klikněte na položku Změnit stav.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-134">Click Change status.</span></span>
18. <span data-ttu-id="6c0a0-135">Klikněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-135">Click Complete.</span></span>
19. <span data-ttu-id="6c0a0-136">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-136">Click OK.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="6c0a0-137">Přidání nové konfigurace mapování modelu ER</span><span class="sxs-lookup"><span data-stu-id="6c0a0-137">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="6c0a0-138">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="6c0a0-139">V poli Nový zadejte Mapování modelu založené na datovém modelu Vzorový datový model.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-139">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
3. <span data-ttu-id="6c0a0-140">Do pole Název zadejte Vzorové mapování.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-140">In the Name field, type 'Sample mapping'.</span></span>
    * <span data-ttu-id="6c0a0-141">Vzorové mapování</span><span class="sxs-lookup"><span data-stu-id="6c0a0-141">Sample mapping</span></span>  
4. <span data-ttu-id="6c0a0-142">Klepněte na možnost Vytvořit konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-142">Click Create configuration.</span></span>
5. <span data-ttu-id="6c0a0-143">Rozbalte oddíl Předpoklady.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-143">Expand the Prerequisites section.</span></span>
    * <span data-ttu-id="6c0a0-144">Mějte na paměti, že skupina předpokladů implementace již byla automaticky přidána.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-144">Note that the Implementations prerequisites group has been added automatically.</span></span> <span data-ttu-id="6c0a0-145">Skupina obsahuje součást předpokladů, která se vztahuje k nadřazené konfiguraci datového modelu a je označena jako Implementace.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-145">The group contains the prerequisite component that refers to the parent data model configuration and is marked as Implementation.</span></span> <span data-ttu-id="6c0a0-146">To znamená, že tato konfigurace mapování modelu pro vzorový model mapování je považována za implementaci datového modelu – Vzorový datový model.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-146">This means that this Sample mapping model mapping configuration is considered the implementation of the data model, Sample data model.</span></span> <span data-ttu-id="6c0a0-147">Tato součást tedy vynutí u ER stahování konfigurace mapování modelu – Vzorové mapování, z úložiště ER po stažení konfigurace modelu – Vzorový datový model.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-147">Therefore, this component will force ER to download the model mapping configuration, Sample mapping from an ER repository when the model configuration, Sample data model, is downloaded.</span></span>   
6. <span data-ttu-id="6c0a0-148">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-148">Click Designer.</span></span>
    * <span data-ttu-id="6c0a0-149">Všimněte si, že vytvořená konfigurace mapování modelu obsahuje nové prázdné mapování se stejným názvem, jako vytvořená konfigurace.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-149">Note that the created model mapping configuration contains a new blank mapping with the same name as the created configuration.</span></span> <span data-ttu-id="6c0a0-150">Mějte na paměti, že pokud konfigurace vybraného nadřazeného modelu obsahuje mapování modelu, dojde ke zkopírování do nové konfigurace mapování modelu.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-150">Be aware that when a selected parent model configuration contains model mappings, they will be copied to a new model mapping configuration.</span></span>   
7. <span data-ttu-id="6c0a0-151">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-151">Click Designer.</span></span>
8. <span data-ttu-id="6c0a0-152">Ve stromovém zobrazení vyberte možnost 'Dynamics 365 for Operations\Tabulka'.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-152">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="6c0a0-153">Klikněte na možnost Přidat kořen.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-153">Click Add root.</span></span>
10. <span data-ttu-id="6c0a0-154">Do pole Název zadejte text „Společnost“.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-154">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="6c0a0-155">Společnost</span><span class="sxs-lookup"><span data-stu-id="6c0a0-155">Company</span></span>  
11. <span data-ttu-id="6c0a0-156">Do pole Tabulka zadejte hodnotu „CompanyInfo“.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-156">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="6c0a0-157">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="6c0a0-157">CompanyInfo</span></span>  
12. <span data-ttu-id="6c0a0-158">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-158">Click OK.</span></span>
13. <span data-ttu-id="6c0a0-159">Ve stromovém zobrazení rozbalte Společnost.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-159">In the tree, expand 'Company'.</span></span>
14. <span data-ttu-id="6c0a0-160">Ve stromovém zobrazení rozbalte Company\find().</span><span class="sxs-lookup"><span data-stu-id="6c0a0-160">In the tree, expand 'Company\find()'.</span></span>
15. <span data-ttu-id="6c0a0-161">Ve stromovém zobrazení vyberte Company\find()\Name.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-161">In the tree, select 'Company\find()\Name'.</span></span>
16. <span data-ttu-id="6c0a0-162">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-162">Click Bind.</span></span>
17. <span data-ttu-id="6c0a0-163">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-163">Click Save.</span></span>
18. <span data-ttu-id="6c0a0-164">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-164">Close the page.</span></span>
19. <span data-ttu-id="6c0a0-165">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-165">Close the page.</span></span>
20. <span data-ttu-id="6c0a0-166">V podokně akcí klikněte na možnost Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-166">On the Action Pane, click Configurations.</span></span>
21. <span data-ttu-id="6c0a0-167">Klikněte na Parametry uživatelů.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-167">Click User parameters.</span></span>
22. <span data-ttu-id="6c0a0-168">Vyberte možnost Ano v poli Nastavení běhu.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-168">Select Yes in the Run settings field.</span></span>
23. <span data-ttu-id="6c0a0-169">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-169">Click OK.</span></span>
24. <span data-ttu-id="6c0a0-170">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-170">Click Edit.</span></span>
25. <span data-ttu-id="6c0a0-171">Vyberte možnost Ano v poli Koncept běhu.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-171">Select Yes in the Run Draft field.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="6c0a0-172">Přidání nové konfigurace formátu ER</span><span class="sxs-lookup"><span data-stu-id="6c0a0-172">Add a new ER format configuration</span></span>
1. <span data-ttu-id="6c0a0-173">Ve stromovém zobrazení vyberte Ukázkový datový model.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-173">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="6c0a0-174">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-174">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="6c0a0-175">V poli Nový zadejte Formát založený na datovém modelu Vzorový datový model.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-175">In the New field, enter 'Format based on data model Sample data model'.</span></span>
4. <span data-ttu-id="6c0a0-176">Do pole Název zadejte Ukázkový formát.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-176">In the Name field, type 'Sample format'.</span></span>
    * <span data-ttu-id="6c0a0-177">Ukázkový formát</span><span class="sxs-lookup"><span data-stu-id="6c0a0-177">Sample format</span></span>  
5. <span data-ttu-id="6c0a0-178">Klepněte na možnost Vytvořit konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-178">Click Create configuration.</span></span>
6. <span data-ttu-id="6c0a0-179">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-179">Click Designer.</span></span>
7. <span data-ttu-id="6c0a0-180">Klepnutím na možnost Přidat kořen otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-180">Click Add root to open the drop dialog.</span></span>
8. <span data-ttu-id="6c0a0-181">Ve stromovém zobrazení vyberte „Text\Řetězec“.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-181">In the tree, select 'Text\String'.</span></span>
9. <span data-ttu-id="6c0a0-182">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-182">Click OK.</span></span>
10. <span data-ttu-id="6c0a0-183">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-183">Click the Mapping tab.</span></span>
11. <span data-ttu-id="6c0a0-184">Ve stromovém zobrazení rozbalte „model“.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-184">In the tree, expand 'model'.</span></span>
12. <span data-ttu-id="6c0a0-185">Ve stromu vyberte model\Company.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-185">In the tree, select 'model\Company'.</span></span>
13. <span data-ttu-id="6c0a0-186">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-186">Click Bind.</span></span>
14. <span data-ttu-id="6c0a0-187">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-187">Click Save.</span></span>
15. <span data-ttu-id="6c0a0-188">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-188">Close the page.</span></span>
    * <span data-ttu-id="6c0a0-189">Pro účely testování spusťte pracovní verzi vytvořeného formátu.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-189">Run the draft version of the created format for testing purposes.</span></span>  
16. <span data-ttu-id="6c0a0-190">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-190">Click Run.</span></span>
    * <span data-ttu-id="6c0a0-191">Na pevné záložce Verze klepněte na tlačítko Spustit.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-191">On the Versions FastTab, click Run.</span></span>  
17. <span data-ttu-id="6c0a0-192">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-192">Click OK.</span></span>
    * <span data-ttu-id="6c0a0-193">Zkontrolujte výstup, zda obsahuje název společnosti, ve které je přihlášen uživatel, který spouští tuto konfiguraci formátu.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-193">Review the output that contains the name of the company in which the user who is running this format configuration is logged into.</span></span> <span data-ttu-id="6c0a0-194">Poznámka: vytvářená konfigurace mapování modelu je použita v této konfiguraci formátu, protože je k dispozici pouze jedna konfigurace, která obsahuje požadované mapování modelu.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-194">Note that the created model mapping configuration is used by this format configuration because there is only one configuration available that contains required model mappings.</span></span>   

## <a name="add-alternative-er-model-mapping-configuration"></a><span data-ttu-id="6c0a0-195">Přidání alternativní konfigurace mapování modelu ER</span><span class="sxs-lookup"><span data-stu-id="6c0a0-195">Add alternative ER model mapping configuration</span></span>
1. <span data-ttu-id="6c0a0-196">Ve stromovém zobrazení vyberte Ukázkový datový model.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-196">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="6c0a0-197">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-197">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="6c0a0-198">V poli Nový zadejte Mapování modelu založené na datovém modelu Vzorový datový model.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-198">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
4. <span data-ttu-id="6c0a0-199">V poli Název zadejte Vzorové mapování (alternativní).</span><span class="sxs-lookup"><span data-stu-id="6c0a0-199">In the Name field, type 'Sample mapping (alternative)'.</span></span>
    * <span data-ttu-id="6c0a0-200">Vzorové mapování (alternativní)</span><span class="sxs-lookup"><span data-stu-id="6c0a0-200">Sample mapping (alternative)</span></span>  
5. <span data-ttu-id="6c0a0-201">Klepněte na možnost Vytvořit konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-201">Click Create configuration.</span></span>
6. <span data-ttu-id="6c0a0-202">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-202">Click Designer.</span></span>
7. <span data-ttu-id="6c0a0-203">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-203">Click Designer.</span></span>
8. <span data-ttu-id="6c0a0-204">Ve stromovém zobrazení vyberte možnost 'Dynamics 365 for Operations\Tabulka'.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-204">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="6c0a0-205">Klikněte na možnost Přidat kořen.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-205">Click Add root.</span></span>
10. <span data-ttu-id="6c0a0-206">Do pole Název zadejte text „Společnost“.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-206">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="6c0a0-207">Společnost</span><span class="sxs-lookup"><span data-stu-id="6c0a0-207">Company</span></span>  
11. <span data-ttu-id="6c0a0-208">Do pole Tabulka zadejte hodnotu „CompanyInfo“.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-208">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="6c0a0-209">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="6c0a0-209">CompanyInfo</span></span>  
12. <span data-ttu-id="6c0a0-210">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-210">Click OK.</span></span>
13. <span data-ttu-id="6c0a0-211">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-211">Click Edit.</span></span>
14. <span data-ttu-id="6c0a0-212">Ve stromovém zobrazení vyberte možnost „Řetězec\SLOUČIT“.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-212">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="6c0a0-213">Klikněte na možnost Přidat funkci.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-213">Click Add function.</span></span>
16. <span data-ttu-id="6c0a0-214">Ve stromovém zobrazení rozbalte Společnost.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-214">In the tree, expand 'Company'.</span></span>
17. <span data-ttu-id="6c0a0-215">Ve stromovém zobrazení rozbalte Company\find().</span><span class="sxs-lookup"><span data-stu-id="6c0a0-215">In the tree, expand 'Company\find()'.</span></span>
18. <span data-ttu-id="6c0a0-216">Ve stromovém zobrazení vyberte Company\find()\Name.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-216">In the tree, select 'Company\find()\Name'.</span></span>
19. <span data-ttu-id="6c0a0-217">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-217">Click Add data source.</span></span>
20. <span data-ttu-id="6c0a0-218">Zadejte hodnotu do pole Receptura.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-218">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="6c0a0-219">CONCATENATE(Company.'find()'.Name, ";",</span><span class="sxs-lookup"><span data-stu-id="6c0a0-219">CONCATENATE(Company.'find()'.Name, ";",</span></span>  
21. <span data-ttu-id="6c0a0-220">Ve stromovém zobrazení vyberte Company\find()\Company(DataArea).</span><span class="sxs-lookup"><span data-stu-id="6c0a0-220">In the tree, select 'Company\find()\Company(DataArea)'.</span></span>
22. <span data-ttu-id="6c0a0-221">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-221">Click Add data source.</span></span>
23. <span data-ttu-id="6c0a0-222">Zadejte hodnotu do pole Receptura.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-222">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="6c0a0-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span><span class="sxs-lookup"><span data-stu-id="6c0a0-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span></span>  
24. <span data-ttu-id="6c0a0-224">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-224">Click Save.</span></span>
25. <span data-ttu-id="6c0a0-225">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-225">Close the page.</span></span>
26. <span data-ttu-id="6c0a0-226">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-226">Click Save.</span></span>
27. <span data-ttu-id="6c0a0-227">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-227">Close the page.</span></span>
28. <span data-ttu-id="6c0a0-228">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-228">Close the page.</span></span>
29. <span data-ttu-id="6c0a0-229">Vyberte možnost Ano v poli Koncept běhu.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-229">Select Yes in the Run Draft field.</span></span>

## <a name="use-an-existing-er-model-mapping-configuration"></a><span data-ttu-id="6c0a0-230">Použití existující konfigurace mapování modelu ER</span><span class="sxs-lookup"><span data-stu-id="6c0a0-230">Use an existing ER model mapping configuration</span></span>
1. <span data-ttu-id="6c0a0-231">Ve stromovém zobrazení vyberte Sample data model\Sample format</span><span class="sxs-lookup"><span data-stu-id="6c0a0-231">In the tree, select 'Sample data model\Sample format'.</span></span>
2. <span data-ttu-id="6c0a0-232">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-232">Click Run.</span></span>
    * <span data-ttu-id="6c0a0-233">Všimněte si, že vybranou pracovní verzi konfigurace formátu ER nelze spustit, protože je k dispozici více než jedna konfigurace mapování modelu pro nedefinovaný datový model, který byl vybrán jako zdroj dat používaného formátu ER.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-233">Note that the selected draft version of the ER format configuration can’t be executed because there is more than one model mapping configuration available for the undefined data model that has been selected as the data source of the running ER format.</span></span>   
    * <span data-ttu-id="6c0a0-234">Dále definujete konfiguraci alternativního mapování modelu jako tu, ze které se použije mapování modelu pro zdroj dat používaného formátu ER.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-234">Next, you will define the alternative model mapping configuration as the one from which model mappings will be used as data sources for running ER format.</span></span>   
3. <span data-ttu-id="6c0a0-235">Ve stromovém zobrazení vyberte Sample data model\Sample mapping (alternative).</span><span class="sxs-lookup"><span data-stu-id="6c0a0-235">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
4. <span data-ttu-id="6c0a0-236">Vyberte možnost Ano v položce Výchozí pro pole mapování modelu.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-236">Select Yes in the Default for model mapping field.</span></span>
5. <span data-ttu-id="6c0a0-237">Ve stromovém zobrazení vyberte Sample data model\Sample format</span><span class="sxs-lookup"><span data-stu-id="6c0a0-237">In the tree, select 'Sample data model\Sample format'.</span></span>
6. <span data-ttu-id="6c0a0-238">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-238">Click Run.</span></span>
7. <span data-ttu-id="6c0a0-239">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="6c0a0-239">Click OK.</span></span>
    * <span data-ttu-id="6c0a0-240">Všimněte si, že výchozí konfigurace mapování modelu se používá v této konfiguraci formátu pro generování elektronických dokumentů (vytvořený výstup obsahuje kód společnosti).</span><span class="sxs-lookup"><span data-stu-id="6c0a0-240">Note that the default model mapping configuration is used by this format configuration for generating the electronic document (the created output contains the company code).</span></span>  

