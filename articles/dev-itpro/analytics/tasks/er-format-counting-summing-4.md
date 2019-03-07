---
title: Elektronické výkaznictví – konfigurace formátu počítání a sčítání (část 4 - Spuštění formátu)
description: Následující procedura popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) k vytvoření počtu a součtu na základě dat již generovaného textového výstupu.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 17989b7fa2baf14472ec19a041cb5ce7e5c0380d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "336191"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4-run-format"></a><span data-ttu-id="341ce-103">Elektronické výkaznictví – konfigurace formátu počítání a sčítání (část 4: Spuštění formátu)</span><span class="sxs-lookup"><span data-stu-id="341ce-103">ER Configure format to do counting and summing (Part 4: Run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="341ce-104">Následující procedura popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) k vytvoření počtu a součtu na základě dat již generovaného textového výstupu.</span><span class="sxs-lookup"><span data-stu-id="341ce-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="341ce-105">Tyto kroky lze provést v rámci společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="341ce-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="341ce-106">K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Konfigurace formátu na provedení výpočtu a součtu (část 3: Používání výpočtů k vytvoření výstupu).</span><span class="sxs-lookup"><span data-stu-id="341ce-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 3: Use computations to make the output)” procedure.</span></span>

<span data-ttu-id="341ce-107">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="341ce-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="341ce-108">Testování této konfigurace pro generování sestav Intrastat</span><span class="sxs-lookup"><span data-stu-id="341ce-108">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="341ce-109">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="341ce-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="341ce-110">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="341ce-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="341ce-111">Ve stromovém zobrazení rozbalte „Modul Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="341ce-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="341ce-112">Ve stromovém zobrazení rozbalte Modul Intrastat\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="341ce-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="341ce-113">Ve stromovém zobrazení vyberte 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="341ce-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="341ce-114">V podokně akcí klikněte na možnost Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="341ce-114">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="341ce-115">Klikněte na Parametry uživatelů.</span><span class="sxs-lookup"><span data-stu-id="341ce-115">Click User parameters.</span></span>
8. <span data-ttu-id="341ce-116">Vyberte možnost Ano v poli Nastavení běhu.</span><span class="sxs-lookup"><span data-stu-id="341ce-116">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="341ce-117">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="341ce-117">Click OK.</span></span>
10. <span data-ttu-id="341ce-118">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="341ce-118">Click Edit.</span></span>
11. <span data-ttu-id="341ce-119">Vyberte možnost Ano v poli Koncept běhu.</span><span class="sxs-lookup"><span data-stu-id="341ce-119">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="341ce-120">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="341ce-120">Click Save.</span></span>
13. <span data-ttu-id="341ce-121">Přejděte na Daň > Nastavení > Zahraniční obchod > Parametry zahraničního obchodu.</span><span class="sxs-lookup"><span data-stu-id="341ce-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="341ce-122">Rozbalte část Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="341ce-122">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="341ce-123">Do pole Název zadejte hodnotu Konfigurace Intrastat (DE) s výpočty a součty'.</span><span class="sxs-lookup"><span data-stu-id="341ce-123">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
16. <span data-ttu-id="341ce-124">Do pole Název zadejte hodnotu Konfigurace Intrastat (DE) s výpočty a součty'.</span><span class="sxs-lookup"><span data-stu-id="341ce-124">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
17. <span data-ttu-id="341ce-125">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="341ce-125">Click Save.</span></span>
18. <span data-ttu-id="341ce-126">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="341ce-126">Close the page.</span></span>
19. <span data-ttu-id="341ce-127">Přejděte na Daň > Deklarace > Zahraniční obchod > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="341ce-127">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="341ce-128">Klepněte na Výstup.</span><span class="sxs-lookup"><span data-stu-id="341ce-128">Click Output.</span></span>
21. <span data-ttu-id="341ce-129">Klikněte na možnost Sestava.</span><span class="sxs-lookup"><span data-stu-id="341ce-129">Click Report.</span></span>
    * <span data-ttu-id="341ce-130">Spusťte proces generování sestavy Intrastat.</span><span class="sxs-lookup"><span data-stu-id="341ce-130">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="341ce-131">V poli Datum od nastavte datum a čas na „2000-01-01“ .</span><span class="sxs-lookup"><span data-stu-id="341ce-131">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="341ce-132">Definujte počáteční a koncové datum pro období vykazování, které zahrnuje existující transakce formuláře.</span><span class="sxs-lookup"><span data-stu-id="341ce-132">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="341ce-133">V poli Datum do nastavte datum a čas na „2022-12-31“ .</span><span class="sxs-lookup"><span data-stu-id="341ce-133">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="341ce-134">Definujte počáteční a koncové datum pro období vykazování, které zahrnuje existující transakce formuláře.</span><span class="sxs-lookup"><span data-stu-id="341ce-134">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="341ce-135">V poli Směr vyberte hodnotu Dovoz.</span><span class="sxs-lookup"><span data-stu-id="341ce-135">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="341ce-136">Vyberte možnost Ano v poli Generovat soubor.</span><span class="sxs-lookup"><span data-stu-id="341ce-136">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="341ce-137">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="341ce-137">Click OK.</span></span>
    * <span data-ttu-id="341ce-138">Prohlédněte si vytvořený výstup souhrnných řádků v databázi.</span><span class="sxs-lookup"><span data-stu-id="341ce-138">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="341ce-139">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="341ce-139">Click New.</span></span>
28. <span data-ttu-id="341ce-140">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="341ce-140">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="341ce-141">V poli Směr vyberte hodnotu Expedice.</span><span class="sxs-lookup"><span data-stu-id="341ce-141">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="341ce-142">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="341ce-142">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="341ce-143">V poli Komodita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="341ce-143">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="341ce-144">Nastavte hodnotu Váha na 10.</span><span class="sxs-lookup"><span data-stu-id="341ce-144">Set Weight to '10'.</span></span>
33. <span data-ttu-id="341ce-145">Nastavte hodnotu Částka k fakturaci na 10000.</span><span class="sxs-lookup"><span data-stu-id="341ce-145">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="341ce-146">Nastavte hodnotu Statistická částka na 10000.</span><span class="sxs-lookup"><span data-stu-id="341ce-146">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="341ce-147">Klepněte na Výstup.</span><span class="sxs-lookup"><span data-stu-id="341ce-147">Click Output.</span></span>
36. <span data-ttu-id="341ce-148">Klikněte na možnost Sestava.</span><span class="sxs-lookup"><span data-stu-id="341ce-148">Click Report.</span></span>
37. <span data-ttu-id="341ce-149">V poli Směr vyberte hodnotu Expedice.</span><span class="sxs-lookup"><span data-stu-id="341ce-149">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="341ce-150">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="341ce-150">Click OK.</span></span>
    * <span data-ttu-id="341ce-151">Prohlédněte si vytvořený výstup souhrnných řádků v databázi.</span><span class="sxs-lookup"><span data-stu-id="341ce-151">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="341ce-152">Všimněte si, že byl změněn ve srovnání s prvním spuštěním.</span><span class="sxs-lookup"><span data-stu-id="341ce-152">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="341ce-153">Spuštění této konfigurace v režimu ladění ke kontrole společného počítání a sčítání dat</span><span class="sxs-lookup"><span data-stu-id="341ce-153">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="341ce-154">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="341ce-154">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="341ce-155">Ve stromovém zobrazení rozbalte „Modul Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="341ce-155">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="341ce-156">Ve stromovém zobrazení rozbalte Modul Intrastat\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="341ce-156">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="341ce-157">Ve stromovém zobrazení vyberte 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="341ce-157">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="341ce-158">V podokně akcí klikněte na možnost Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="341ce-158">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="341ce-159">Klikněte na Parametry uživatelů.</span><span class="sxs-lookup"><span data-stu-id="341ce-159">Click User parameters.</span></span>
7. <span data-ttu-id="341ce-160">Vyberte možnost Ano v poli Spustit v režimu ladění.</span><span class="sxs-lookup"><span data-stu-id="341ce-160">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="341ce-161">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="341ce-161">Click OK.</span></span>
9. <span data-ttu-id="341ce-162">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="341ce-162">Close the page.</span></span>
10. <span data-ttu-id="341ce-163">Přejděte na Daň > Deklarace > Zahraniční obchod > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="341ce-163">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="341ce-164">Klepněte na Výstup.</span><span class="sxs-lookup"><span data-stu-id="341ce-164">Click Output.</span></span>
12. <span data-ttu-id="341ce-165">Klikněte na možnost Sestava.</span><span class="sxs-lookup"><span data-stu-id="341ce-165">Click Report.</span></span>
13. <span data-ttu-id="341ce-166">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="341ce-166">Click OK.</span></span>
14. <span data-ttu-id="341ce-167">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="341ce-167">Close the page.</span></span>
15. <span data-ttu-id="341ce-168">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="341ce-168">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="341ce-169">Ve stromovém zobrazení rozbalte „Modul Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="341ce-169">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="341ce-170">Ve stromovém zobrazení rozbalte Modul Intrastat\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="341ce-170">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="341ce-171">Ve stromovém zobrazení vyberte 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="341ce-171">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="341ce-172">Klikněte na Protokoly ladění.</span><span class="sxs-lookup"><span data-stu-id="341ce-172">Click Debug logs.</span></span>
    * <span data-ttu-id="341ce-173">Všimněte si, že záznam protokolu ladění byl vytvořen pro proces spuštění vybrané konfigurace.</span><span class="sxs-lookup"><span data-stu-id="341ce-173">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="341ce-174">Klikněte na možnost Připojit.</span><span class="sxs-lookup"><span data-stu-id="341ce-174">Click Attach.</span></span>
21. <span data-ttu-id="341ce-175">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="341ce-175">Click Open.</span></span>
    * <span data-ttu-id="341ce-176">Zkontrolujte vytvořený soubor XML, který obsahuje podrobnosti o počítání a sčítání, které byly shromážděny během provádění vybrané konfigurace.</span><span class="sxs-lookup"><span data-stu-id="341ce-176">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  

