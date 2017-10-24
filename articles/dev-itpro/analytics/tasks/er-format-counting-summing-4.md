--- 
title: "Spuštění formátu pro provádění počítání a sčítání pro elektronické výkaznictví (ER)"
description: "Následující procedura popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) k vytvoření počtu a součtu na základě dat již generovaného textového výstupu."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 9f5520dc4e1eddc2fc52a05e5dc386b982d8f5ad
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="run-the-format-to-do-counting-and-summing-for-electronic-reporting-er"></a><span data-ttu-id="c4451-103">Spuštění formátu pro provádění počítání a sčítání pro elektronické výkaznictví (ER)</span><span class="sxs-lookup"><span data-stu-id="c4451-103">Run the format to do counting and summing for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c4451-104">Následující procedura popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) k vytvoření počtu a součtu na základě dat již generovaného textového výstupu.</span><span class="sxs-lookup"><span data-stu-id="c4451-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="c4451-105">Tyto kroky lze provést v rámci společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="c4451-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="c4451-106">K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Konfigurace formátu na provedení výpočtu a součtu (část 3: Používání výpočtů k vytvoření výstupu).</span><span class="sxs-lookup"><span data-stu-id="c4451-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 3: Use computations to make the output)” procedure.</span></span>

<span data-ttu-id="c4451-107">Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="c4451-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="c4451-108">Testování této konfigurace pro generování sestav Intrastat</span><span class="sxs-lookup"><span data-stu-id="c4451-108">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="c4451-109">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="c4451-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="c4451-110">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="c4451-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="c4451-111">Ve stromovém zobrazení rozbalte „Modul Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="c4451-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="c4451-112">Ve stromovém zobrazení rozbalte Modul Intrastat\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="c4451-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="c4451-113">Ve stromovém zobrazení vyberte 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="c4451-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="c4451-114">V podokně akcí klikněte na možnost Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="c4451-114">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="c4451-115">Klikněte na Parametry uživatelů.</span><span class="sxs-lookup"><span data-stu-id="c4451-115">Click User parameters.</span></span>
8. <span data-ttu-id="c4451-116">Vyberte možnost Ano v poli Nastavení běhu.</span><span class="sxs-lookup"><span data-stu-id="c4451-116">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="c4451-117">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c4451-117">Click OK.</span></span>
10. <span data-ttu-id="c4451-118">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="c4451-118">Click Edit.</span></span>
11. <span data-ttu-id="c4451-119">Vyberte možnost Ano v poli Koncept běhu.</span><span class="sxs-lookup"><span data-stu-id="c4451-119">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="c4451-120">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="c4451-120">Click Save.</span></span>
13. <span data-ttu-id="c4451-121">Přejděte na Daň > Nastavení > Zahraniční obchod > Parametry zahraničního obchodu.</span><span class="sxs-lookup"><span data-stu-id="c4451-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="c4451-122">Rozbalte část Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="c4451-122">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="c4451-123">Do pole Název zadejte hodnotu Konfigurace Intrastat (DE) s výpočty a součty'.</span><span class="sxs-lookup"><span data-stu-id="c4451-123">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
16. <span data-ttu-id="c4451-124">Do pole Název zadejte hodnotu Konfigurace Intrastat (DE) s výpočty a součty'.</span><span class="sxs-lookup"><span data-stu-id="c4451-124">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
17. <span data-ttu-id="c4451-125">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="c4451-125">Click Save.</span></span>
18. <span data-ttu-id="c4451-126">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c4451-126">Close the page.</span></span>
19. <span data-ttu-id="c4451-127">Přejděte na Daň > Deklarace > Zahraniční obchod > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="c4451-127">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="c4451-128">Klepněte na Výstup.</span><span class="sxs-lookup"><span data-stu-id="c4451-128">Click Output.</span></span>
21. <span data-ttu-id="c4451-129">Klikněte na možnost Sestava.</span><span class="sxs-lookup"><span data-stu-id="c4451-129">Click Report.</span></span>
    * <span data-ttu-id="c4451-130">Spusťte proces generování sestavy Intrastat.</span><span class="sxs-lookup"><span data-stu-id="c4451-130">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="c4451-131">V poli Datum od nastavte datum a čas na „2000-01-01“ .</span><span class="sxs-lookup"><span data-stu-id="c4451-131">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="c4451-132">Definujte počáteční a koncové datum pro období vykazování, které zahrnuje existující transakce formuláře.</span><span class="sxs-lookup"><span data-stu-id="c4451-132">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="c4451-133">V poli Datum do nastavte datum a čas na „2022-12-31“ .</span><span class="sxs-lookup"><span data-stu-id="c4451-133">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="c4451-134">Definujte počáteční a koncové datum pro období vykazování, které zahrnuje existující transakce formuláře.</span><span class="sxs-lookup"><span data-stu-id="c4451-134">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="c4451-135">V poli Směr vyberte hodnotu Dovoz.</span><span class="sxs-lookup"><span data-stu-id="c4451-135">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="c4451-136">Vyberte možnost Ano v poli Generovat soubor.</span><span class="sxs-lookup"><span data-stu-id="c4451-136">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="c4451-137">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c4451-137">Click OK.</span></span>
    * <span data-ttu-id="c4451-138">Prohlédněte si vytvořený výstup souhrnných řádků v databázi.</span><span class="sxs-lookup"><span data-stu-id="c4451-138">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="c4451-139">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="c4451-139">Click New.</span></span>
28. <span data-ttu-id="c4451-140">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="c4451-140">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="c4451-141">V poli Směr vyberte hodnotu Expedice.</span><span class="sxs-lookup"><span data-stu-id="c4451-141">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="c4451-142">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c4451-142">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="c4451-143">V poli Komodita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c4451-143">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="c4451-144">Nastavte hodnotu Váha na 10.</span><span class="sxs-lookup"><span data-stu-id="c4451-144">Set Weight to '10'.</span></span>
33. <span data-ttu-id="c4451-145">Nastavte hodnotu Částka k fakturaci na 10000.</span><span class="sxs-lookup"><span data-stu-id="c4451-145">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="c4451-146">Nastavte hodnotu Statistická částka na 10000.</span><span class="sxs-lookup"><span data-stu-id="c4451-146">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="c4451-147">Klepněte na Výstup.</span><span class="sxs-lookup"><span data-stu-id="c4451-147">Click Output.</span></span>
36. <span data-ttu-id="c4451-148">Klikněte na možnost Sestava.</span><span class="sxs-lookup"><span data-stu-id="c4451-148">Click Report.</span></span>
37. <span data-ttu-id="c4451-149">V poli Směr vyberte hodnotu Expedice.</span><span class="sxs-lookup"><span data-stu-id="c4451-149">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="c4451-150">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c4451-150">Click OK.</span></span>
    * <span data-ttu-id="c4451-151">Prohlédněte si vytvořený výstup souhrnných řádků v databázi.</span><span class="sxs-lookup"><span data-stu-id="c4451-151">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="c4451-152">Všimněte si, že byl změněn ve srovnání s prvním spuštěním.</span><span class="sxs-lookup"><span data-stu-id="c4451-152">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="c4451-153">Spuštění této konfigurace v režimu ladění ke kontrole společného počítání a sčítání dat</span><span class="sxs-lookup"><span data-stu-id="c4451-153">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="c4451-154">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="c4451-154">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="c4451-155">Ve stromovém zobrazení rozbalte „Modul Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="c4451-155">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="c4451-156">Ve stromovém zobrazení rozbalte Modul Intrastat\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="c4451-156">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="c4451-157">Ve stromovém zobrazení vyberte 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="c4451-157">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="c4451-158">V podokně akcí klikněte na možnost Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="c4451-158">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="c4451-159">Klikněte na Parametry uživatelů.</span><span class="sxs-lookup"><span data-stu-id="c4451-159">Click User parameters.</span></span>
7. <span data-ttu-id="c4451-160">Vyberte možnost Ano v poli Spustit v režimu ladění.</span><span class="sxs-lookup"><span data-stu-id="c4451-160">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="c4451-161">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c4451-161">Click OK.</span></span>
9. <span data-ttu-id="c4451-162">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c4451-162">Close the page.</span></span>
10. <span data-ttu-id="c4451-163">Přejděte na Daň > Deklarace > Zahraniční obchod > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="c4451-163">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="c4451-164">Klepněte na Výstup.</span><span class="sxs-lookup"><span data-stu-id="c4451-164">Click Output.</span></span>
12. <span data-ttu-id="c4451-165">Klikněte na možnost Sestava.</span><span class="sxs-lookup"><span data-stu-id="c4451-165">Click Report.</span></span>
13. <span data-ttu-id="c4451-166">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c4451-166">Click OK.</span></span>
14. <span data-ttu-id="c4451-167">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c4451-167">Close the page.</span></span>
15. <span data-ttu-id="c4451-168">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="c4451-168">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="c4451-169">Ve stromovém zobrazení rozbalte „Modul Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="c4451-169">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="c4451-170">Ve stromovém zobrazení rozbalte Modul Intrastat\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="c4451-170">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="c4451-171">Ve stromovém zobrazení vyberte 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="c4451-171">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="c4451-172">Klikněte na Protokoly ladění.</span><span class="sxs-lookup"><span data-stu-id="c4451-172">Click Debug logs.</span></span>
    * <span data-ttu-id="c4451-173">Všimněte si, že záznam protokolu ladění byl vytvořen pro proces spuštění vybrané konfigurace.</span><span class="sxs-lookup"><span data-stu-id="c4451-173">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="c4451-174">Klikněte na možnost Připojit.</span><span class="sxs-lookup"><span data-stu-id="c4451-174">Click Attach.</span></span>
21. <span data-ttu-id="c4451-175">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="c4451-175">Click Open.</span></span>
    * <span data-ttu-id="c4451-176">Zkontrolujte vytvořený soubor XML, který obsahuje podrobnosti o počítání a sčítání, které byly shromážděny během provádění vybrané konfigurace.</span><span class="sxs-lookup"><span data-stu-id="c4451-176">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  


