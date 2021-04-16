---
title: Elektronické výkaznictví – konfigurace formátu počítání a sčítání (část 4 - Spuštění formátu)
description: Toto téma popisuje, jak nakonfigurovat formát elektronického výkaznictví tak, aby počítal a sčítal na základě dat již vygenerovaného textového výstupu. (část 4)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5792505de78aad458bd8745630915cf58f05f73f
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748966"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a><span data-ttu-id="fde4c-104">Elektronické výkaznictví – konfigurace formátu počítání a sčítání (část 4 - Spuštění formátu)</span><span class="sxs-lookup"><span data-stu-id="fde4c-104">ER Configure format to do counting and summing (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fde4c-105">Následující procedura popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) k vytvoření počtu a součtu na základě dat již generovaného textového výstupu.</span><span class="sxs-lookup"><span data-stu-id="fde4c-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="fde4c-106">Tyto kroky lze provést v rámci společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="fde4c-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="fde4c-107">K dokončení těchto kroků je nutné nejprve provést kroky v postupu „Elektronické výkaznictví – Konfigurace formátu na provedení výpočtu a součtu (část 3: Používání výpočtů k vytvoření výstupu)“.</span><span class="sxs-lookup"><span data-stu-id="fde4c-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 3: Use computations to make the output)" procedure.</span></span>

<span data-ttu-id="fde4c-108">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="fde4c-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="fde4c-109">Testování této konfigurace pro generování sestav Intrastat</span><span class="sxs-lookup"><span data-stu-id="fde4c-109">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="fde4c-110">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="fde4c-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="fde4c-111">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="fde4c-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="fde4c-112">Ve stromovém zobrazení rozbalte „Modul Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="fde4c-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="fde4c-113">Ve stromovém zobrazení rozbalte Modul Intrastat\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="fde4c-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="fde4c-114">Ve stromovém zobrazení vyberte 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="fde4c-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="fde4c-115">V podokně akcí klikněte na možnost Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="fde4c-115">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="fde4c-116">Klikněte na Parametry uživatelů.</span><span class="sxs-lookup"><span data-stu-id="fde4c-116">Click User parameters.</span></span>
8. <span data-ttu-id="fde4c-117">Vyberte možnost Ano v poli Nastavení běhu.</span><span class="sxs-lookup"><span data-stu-id="fde4c-117">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="fde4c-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="fde4c-118">Click OK.</span></span>
10. <span data-ttu-id="fde4c-119">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="fde4c-119">Click Edit.</span></span>
11. <span data-ttu-id="fde4c-120">Vyberte možnost Ano v poli Koncept běhu.</span><span class="sxs-lookup"><span data-stu-id="fde4c-120">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="fde4c-121">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="fde4c-121">Click Save.</span></span>
13. <span data-ttu-id="fde4c-122">Přejděte na Daň > Nastavení > Zahraniční obchod > Parametry zahraničního obchodu.</span><span class="sxs-lookup"><span data-stu-id="fde4c-122">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="fde4c-123">Rozbalte část Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="fde4c-123">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="fde4c-124">Zvolte konfiguraci „Intrastat (DE) s výpočty a součty“.</span><span class="sxs-lookup"><span data-stu-id="fde4c-124">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
16. <span data-ttu-id="fde4c-125">Zvolte konfiguraci „Intrastat (DE) s výpočty a součty“.</span><span class="sxs-lookup"><span data-stu-id="fde4c-125">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
17. <span data-ttu-id="fde4c-126">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="fde4c-126">Click Save.</span></span>
18. <span data-ttu-id="fde4c-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="fde4c-127">Close the page.</span></span>
19. <span data-ttu-id="fde4c-128">Přejděte na Daň > Deklarace > Zahraniční obchod > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="fde4c-128">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="fde4c-129">Klepněte na Výstup.</span><span class="sxs-lookup"><span data-stu-id="fde4c-129">Click Output.</span></span>
21. <span data-ttu-id="fde4c-130">Klikněte na možnost Sestava.</span><span class="sxs-lookup"><span data-stu-id="fde4c-130">Click Report.</span></span>
    * <span data-ttu-id="fde4c-131">Spusťte proces generování sestavy Intrastat.</span><span class="sxs-lookup"><span data-stu-id="fde4c-131">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="fde4c-132">V poli Datum od nastavte datum a čas na „2000-01-01“ .</span><span class="sxs-lookup"><span data-stu-id="fde4c-132">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="fde4c-133">Definujte počáteční a koncové datum pro období vykazování, které zahrnuje existující transakce formuláře.</span><span class="sxs-lookup"><span data-stu-id="fde4c-133">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="fde4c-134">V poli Datum do nastavte datum a čas na „2022-12-31“ .</span><span class="sxs-lookup"><span data-stu-id="fde4c-134">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="fde4c-135">Definujte počáteční a koncové datum pro období vykazování, které zahrnuje existující transakce formuláře.</span><span class="sxs-lookup"><span data-stu-id="fde4c-135">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="fde4c-136">V poli Směr vyberte hodnotu Dovoz.</span><span class="sxs-lookup"><span data-stu-id="fde4c-136">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="fde4c-137">Vyberte možnost Ano v poli Generovat soubor.</span><span class="sxs-lookup"><span data-stu-id="fde4c-137">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="fde4c-138">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="fde4c-138">Click OK.</span></span>
    * <span data-ttu-id="fde4c-139">Prohlédněte si vytvořený výstup souhrnných řádků v databázi.</span><span class="sxs-lookup"><span data-stu-id="fde4c-139">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="fde4c-140">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="fde4c-140">Click New.</span></span>
28. <span data-ttu-id="fde4c-141">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="fde4c-141">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="fde4c-142">V poli Směr vyberte hodnotu Expedice.</span><span class="sxs-lookup"><span data-stu-id="fde4c-142">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="fde4c-143">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fde4c-143">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="fde4c-144">V poli Komodita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fde4c-144">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="fde4c-145">Nastavte hodnotu Váha na 10.</span><span class="sxs-lookup"><span data-stu-id="fde4c-145">Set Weight to '10'.</span></span>
33. <span data-ttu-id="fde4c-146">Nastavte hodnotu Částka k fakturaci na 10000.</span><span class="sxs-lookup"><span data-stu-id="fde4c-146">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="fde4c-147">Nastavte hodnotu Statistická částka na 10000.</span><span class="sxs-lookup"><span data-stu-id="fde4c-147">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="fde4c-148">Klepněte na Výstup.</span><span class="sxs-lookup"><span data-stu-id="fde4c-148">Click Output.</span></span>
36. <span data-ttu-id="fde4c-149">Klikněte na možnost Sestava.</span><span class="sxs-lookup"><span data-stu-id="fde4c-149">Click Report.</span></span>
37. <span data-ttu-id="fde4c-150">V poli Směr vyberte hodnotu Expedice.</span><span class="sxs-lookup"><span data-stu-id="fde4c-150">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="fde4c-151">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="fde4c-151">Click OK.</span></span>
    * <span data-ttu-id="fde4c-152">Prohlédněte si vytvořený výstup souhrnných řádků v databázi.</span><span class="sxs-lookup"><span data-stu-id="fde4c-152">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="fde4c-153">Všimněte si, že byl změněn ve srovnání s prvním spuštěním.</span><span class="sxs-lookup"><span data-stu-id="fde4c-153">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="fde4c-154">Spuštění této konfigurace v režimu ladění ke kontrole společného počítání a sčítání dat</span><span class="sxs-lookup"><span data-stu-id="fde4c-154">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="fde4c-155">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="fde4c-155">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="fde4c-156">Ve stromovém zobrazení rozbalte „Modul Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="fde4c-156">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="fde4c-157">Ve stromovém zobrazení rozbalte Modul Intrastat\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="fde4c-157">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="fde4c-158">Ve stromovém zobrazení vyberte 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="fde4c-158">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="fde4c-159">V podokně akcí klikněte na možnost Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="fde4c-159">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="fde4c-160">Klikněte na Parametry uživatelů.</span><span class="sxs-lookup"><span data-stu-id="fde4c-160">Click User parameters.</span></span>
7. <span data-ttu-id="fde4c-161">Vyberte možnost Ano v poli Spustit v režimu ladění.</span><span class="sxs-lookup"><span data-stu-id="fde4c-161">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="fde4c-162">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="fde4c-162">Click OK.</span></span>
9. <span data-ttu-id="fde4c-163">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="fde4c-163">Close the page.</span></span>
10. <span data-ttu-id="fde4c-164">Přejděte na Daň > Deklarace > Zahraniční obchod > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="fde4c-164">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="fde4c-165">Klepněte na Výstup.</span><span class="sxs-lookup"><span data-stu-id="fde4c-165">Click Output.</span></span>
12. <span data-ttu-id="fde4c-166">Klikněte na možnost Sestava.</span><span class="sxs-lookup"><span data-stu-id="fde4c-166">Click Report.</span></span>
13. <span data-ttu-id="fde4c-167">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="fde4c-167">Click OK.</span></span>
14. <span data-ttu-id="fde4c-168">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="fde4c-168">Close the page.</span></span>
15. <span data-ttu-id="fde4c-169">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="fde4c-169">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="fde4c-170">Ve stromovém zobrazení rozbalte „Modul Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="fde4c-170">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="fde4c-171">Ve stromovém zobrazení rozbalte Modul Intrastat\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="fde4c-171">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="fde4c-172">Ve stromovém zobrazení vyberte 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="fde4c-172">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="fde4c-173">Klikněte na Protokoly ladění.</span><span class="sxs-lookup"><span data-stu-id="fde4c-173">Click Debug logs.</span></span>
    * <span data-ttu-id="fde4c-174">Všimněte si, že záznam protokolu ladění byl vytvořen pro proces spuštění vybrané konfigurace.</span><span class="sxs-lookup"><span data-stu-id="fde4c-174">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="fde4c-175">Klikněte na možnost Připojit.</span><span class="sxs-lookup"><span data-stu-id="fde4c-175">Click Attach.</span></span>
21. <span data-ttu-id="fde4c-176">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="fde4c-176">Click Open.</span></span>
    * <span data-ttu-id="fde4c-177">Zkontrolujte vytvořený soubor XML, který obsahuje podrobnosti o počítání a sčítání, které byly shromážděny během provádění vybrané konfigurace.</span><span class="sxs-lookup"><span data-stu-id="fde4c-177">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]